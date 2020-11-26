---
title: Запрещение новых подключений к серверу Lync Server для обслуживания сервера
description: Запрещение новых подключений к серверу Lync Server для обслуживания сервера.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent new connections to Lync Server for server maintenance
ms:assetid: 22b27adf-a590-43bd-9306-a5789ae108d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520964(v=OCS.15)
ms:contentKeyID: 48183625
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd676467cdd6b5bb430f972e48c2f3a53f3f6f14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436899"
---
# <a name="prevent-new-connections-to-lync-server-2013-for-server-maintenance"></a><span data-ttu-id="559e1-103">Запрещение новых подключений к Lync Server 2013 для обслуживания сервера</span><span class="sxs-lookup"><span data-stu-id="559e1-103">Prevent new connections to Lync Server 2013 for server maintenance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="559e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="559e1-104">

<span> </span></span></span>

<span data-ttu-id="559e1-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="559e1-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="559e1-106">Lync Server позволяет перевести сервер в автономный режим (например, для применения обновлений программного обеспечения или оборудования) без потери обслуживания пользователей.</span><span class="sxs-lookup"><span data-stu-id="559e1-106">Lync Server enables you to take a server offline (for example, to apply software or hardware upgrades) without any loss of service to users.</span></span>

<span data-ttu-id="559e1-107">Если вы укажете параметр для предотвращения новых подключений и звонков на сервер в пуле, он перестанет выполнять новые подключения и вызовы, как только вы реализуете этот параметр.</span><span class="sxs-lookup"><span data-stu-id="559e1-107">When you specify the option to prevent new connections or calls to a server in a pool, it stops taking any new connections and calls as soon as you implement this option.</span></span> <span data-ttu-id="559e1-108">Эти новые подключения и звонки перенаправляются через другие серверы в пуле.</span><span class="sxs-lookup"><span data-stu-id="559e1-108">These new connections and calls are routed through other servers in the pool.</span></span> <span data-ttu-id="559e1-109">Сервер, который препятствует новым подключениям, допускает продолжение сеансов в существующих соединениях, пока не завершится.</span><span class="sxs-lookup"><span data-stu-id="559e1-109">A server that is preventing new connections allows its sessions on existing connections to continue until they naturally end.</span></span> <span data-ttu-id="559e1-110">После того как все существующие сеансы будут завершены, сервер будет готов к переходу в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="559e1-110">When all existing sessions have ended, the server is ready to be taken offline.</span></span>

<span data-ttu-id="559e1-111">Если вы не можете помешать новым подключениям к серверу переднего плана, некоторые возможности и службы Lync Server используют балансировку нагрузки DNS для обеспечения правильной работы.</span><span class="sxs-lookup"><span data-stu-id="559e1-111">When you prevent new connections to a Front End Server, some Lync Server features and services rely on DNS load balancing to ensure that it functions properly.</span></span> <span data-ttu-id="559e1-112">Если вы не используете в пуле функцию балансировки нагрузки DNS, то при подключении через эти службы может не перенаправляться к другим серверам в течение периода, в течение которого сервер препятствует новым подключениям, и поэтому, когда сервер переводится в автономный режим, некоторые сеансы и звонки могут быть прерваны.</span><span class="sxs-lookup"><span data-stu-id="559e1-112">If you are not using DNS load balancing on the pool, connections through these services may not be re-routed to other servers during the period that the server is preventing new connections, and thus when the server is taken offline some sessions and calls may be interrupted.</span></span> <span data-ttu-id="559e1-113">Возможности, которые используют балансировку нагрузки DNS для обеспечения правильного функционирования этого параметра, описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="559e1-113">The features that rely on DNS load balancing to ensure that this option operates properly are as follows:</span></span>

  - <span data-ttu-id="559e1-114">Attendant</span><span class="sxs-lookup"><span data-stu-id="559e1-114">Attendant</span></span>

  - <span data-ttu-id="559e1-115">оповещений для конференц-связи</span><span class="sxs-lookup"><span data-stu-id="559e1-115">Conferencing Announcement application</span></span>

  - <span data-ttu-id="559e1-116">"Группа ответа"</span><span class="sxs-lookup"><span data-stu-id="559e1-116">Response Group application</span></span>

  - <span data-ttu-id="559e1-117">"Объявление"</span><span class="sxs-lookup"><span data-stu-id="559e1-117">Announcement application</span></span>

  - <span data-ttu-id="559e1-118">приостановки вызовов</span><span class="sxs-lookup"><span data-stu-id="559e1-118">Call Park application</span></span>

<span data-ttu-id="559e1-119">Подробные сведения о балансировке нагрузки DNS можно найти [в разделе Балансировка нагрузки DNS в Lync Server 2013](lync-server-2013-dns-load-balancing.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="559e1-119">For details about DNS load balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<span data-ttu-id="559e1-120">В дополнение к предотвращению новых подключений для всех служб на сервере Lync Server вы также можете запретить новые подключения для отдельных служб Lync Server.</span><span class="sxs-lookup"><span data-stu-id="559e1-120">In addition to preventing new connections for all services on a server running Lync Server, you can also prevent new connections for individual Lync Server services.</span></span> <span data-ttu-id="559e1-121">Например, этот метод полезен в ситуации, когда необходимо применить обновление для Lync Server, не требующее завершения работы всего сервера.</span><span class="sxs-lookup"><span data-stu-id="559e1-121">For example, this method is useful in a situation where you need to apply a Lync Server update that does not require the whole server to be shut down.</span></span> <span data-ttu-id="559e1-122">Обратите внимание, что при предотвращении подключений для одной службы необходимо выбрать службу, которая будет сгруппирована и отображена в списке служб Windows.</span><span class="sxs-lookup"><span data-stu-id="559e1-122">Note that when you prevent connections for one service, you must select a service as it is grouped and displayed in the Windows list of services.</span></span> <span data-ttu-id="559e1-123">Например, служба Lync Server Front-End и агент сбора данных для мониторинга являются отдельными службами Lync Server, но в списке служб Windows они консолидируются и отображаются как служба переднего плана Lync Server.</span><span class="sxs-lookup"><span data-stu-id="559e1-123">For example, the Lync Server Front-End service and the data collection agent for Monitoring are separate Lync Server services, but in the Windows services list they are consolidated and shown as the Lync Server Front End service.</span></span> <span data-ttu-id="559e1-124">Вы можете запретить новые соединения для службы переднего плана Lync Server, но вы не сможете помешать новым подключениям для этих двух отдельных служб Lync Server отдельно.</span><span class="sxs-lookup"><span data-stu-id="559e1-124">You can prevent new connections for the Lync Server Front End service, but you cannot prevent new connections for these two individual underlying Lync Server services separately.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="559e1-125">Если вы настроили сервер для предотвращения новых подключений, а затем перезагрузите сервер, по умолчанию будет сразу же приступить к приему новых подключений после его запуска.</span><span class="sxs-lookup"><span data-stu-id="559e1-125">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="559e1-126">Чтобы не допустить этого, настройте сервер на приостановку и возобновление вручную, прежде чем перезапустить сервер.</span><span class="sxs-lookup"><span data-stu-id="559e1-126">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>



</div>

<div>

## <a name="to-prevent-new-connections-to-lync-server"></a><span data-ttu-id="559e1-127">Чтобы запретить создание подключений к серверу Lync Server, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="559e1-127">To prevent new connections to Lync Server:</span></span>

1.  <span data-ttu-id="559e1-128">Войдите на локальный компьютер как член группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="559e1-128">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="559e1-129">Откройте консоль оснастки "службы": нажмите кнопку **Пуск**, наведите указатель на пункт **все программы**, выберите пункт **Администрирование**, а затем — пункт **службы**.</span><span class="sxs-lookup"><span data-stu-id="559e1-129">Open the Services snap-in console: Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **Services**.</span></span>

3.  <span data-ttu-id="559e1-130">В списке дважды щелкните службу Windows сервера Lync Server, для которой вы хотите запретить новые подключения.</span><span class="sxs-lookup"><span data-stu-id="559e1-130">In the list, double-click the Lync Server Windows service to which you want to prevent new connections.</span></span>

4.  <span data-ttu-id="559e1-131">В диалоговом окне Свойства в разделе **состояние службы: запущено** выберите команду **приостановить**.</span><span class="sxs-lookup"><span data-stu-id="559e1-131">In the Properties dialog box, under **Service status: Started**, click **Pause**.</span></span>

5.  <span data-ttu-id="559e1-132">(Необязательно), но рекомендуется, рядом с полем **Тип запуска** выберите пункт **вручную**.</span><span class="sxs-lookup"><span data-stu-id="559e1-132">Optionally, but recommended, next to **Startup type**, click **Manual**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="559e1-133">Если вы настроили сервер для предотвращения новых подключений, а затем перезагрузите сервер, по умолчанию будет сразу же приступить к приему новых подключений после его запуска.</span><span class="sxs-lookup"><span data-stu-id="559e1-133">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="559e1-134">Чтобы не допустить этого, настройте сервер на приостановку и возобновление вручную, прежде чем перезапустить сервер.</span><span class="sxs-lookup"><span data-stu-id="559e1-134">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>

    
    </div>

6.  <span data-ttu-id="559e1-135">По завершении щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="559e1-135">When you are finished, click **OK**.</span></span>

<span data-ttu-id="559e1-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="559e1-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

