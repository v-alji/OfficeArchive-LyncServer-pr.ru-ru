---
title: Настройка сервера обновлений
description: Настройка сервера обновлений.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure Mediation Server
ms:assetid: 583236fd-33cd-4045-81df-baa58ed07779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204913(v=OCS.15)
ms:contentKeyID: 48184207
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5723d9446122b85f7bd1812f7c6f411c5c1c9dbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398866"
---
# <a name="configure-mediation-server"></a><span data-ttu-id="f95a5-103">Настройка сервера обновлений</span><span class="sxs-lookup"><span data-stu-id="f95a5-103">Configure Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f95a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f95a5-104">

<span> </span></span></span>

<span data-ttu-id="f95a5-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f95a5-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f95a5-106">В этой процедуре описаны действия, которые необходимо выполнить, чтобы настроить пул Lync Server 2013 на использование сервера обновлений Lync Server 2013 вместо устаревшего сервера Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="f95a5-106">This procedure details the steps to configure the Lync Server 2013 pool to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<span data-ttu-id="f95a5-107">Чтобы успешно публиковать, включать и отключать топологию при добавлении или удалении роли сервера, вы должны войти в систему как пользователь, который является членом группы администраторов RTCUniversalServerAdmins и domain.</span><span class="sxs-lookup"><span data-stu-id="f95a5-107">To successfully publish, enable, or disable a topology when adding or removing a server role, you should be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="f95a5-108">Кроме того, можно делегировать права администратора и разрешения на Добавление ролей сервера.</span><span class="sxs-lookup"><span data-stu-id="f95a5-108">It is also possible to delegate the proper administrator rights and permissions for adding server roles.</span></span> <span data-ttu-id="f95a5-109">Дополнительные сведения можно найти в разделе Делегирование разрешений на настройку на сервере Standard Edition или в документации по развертыванию сервера Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="f95a5-109">For details, see Delegate Setup Permissions in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="f95a5-110">Для других изменений конфигурации требуется только членство в группе RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f95a5-110">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f95a5-111">Последние сведения о том, как найти квалифицированные шлюзы PSTN, IP-АТС и службы магистральных каналов SIP, которые работают с Lync Server 2013, можно найти в разделе "Единая программа для Microsoft Unified Communications Open для взаимодействия" <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A> .</span><span class="sxs-lookup"><span data-stu-id="f95a5-111">For the latest information on finding qualified PSTN gateways, IP-PBXs, and SIP trunking services that work with Lync Server 2013, see "Microsoft Unified Communications Open Interoperability Program" at <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A>.</span></span>



</div>

<div>

## <a name="to-configure-mediation-server-using-topology-builder"></a><span data-ttu-id="f95a5-112">Настройка сервера обновлений с помощью построителя топологии</span><span class="sxs-lookup"><span data-stu-id="f95a5-112">To configure Mediation Server Using Topology Builder</span></span>

1.  <span data-ttu-id="f95a5-113">Откройте существующую топологию из построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="f95a5-113">Open an existing topology from Topology Builder.</span></span>

2.  <span data-ttu-id="f95a5-114">В левой области выберите **шлюзы PSTN**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-114">In the left pane, navigate to **PSTN gateways**.</span></span>

3.  <span data-ttu-id="f95a5-115">Щелкните правой кнопкой **шлюзы PSTN** и выберите команду **создать шлюз IP/КТСОП**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-115">Right-click **PSTN gateways**, and then click **New IP/PSTN Gateway**.</span></span>

4.  <span data-ttu-id="f95a5-116">На странице **Определение нового шлюза IP/КТСОП** введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="f95a5-116">Complete the **Define New IP/PSTN Gateway** page with the following information:</span></span>
    
      - <span data-ttu-id="f95a5-117">Введите полное доменное имя или IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="f95a5-117">Enter the gateway FQDN or IP address.</span></span> <span data-ttu-id="f95a5-118">Полное доменное имя шлюза является обязательным, если шлюз использует протокол TLS.</span><span class="sxs-lookup"><span data-stu-id="f95a5-118">The FQDN of the gateway is required if the gateway uses the TLS protocol.</span></span>
    
      - <span data-ttu-id="f95a5-119">Принимаете значение по умолчанию **для прослушивающего порта IP/КТСОП** или введите новый порт для прослушивания, если он был изменен.</span><span class="sxs-lookup"><span data-stu-id="f95a5-119">Accept the default value of the **Listening port for IP/PSTN gateway** or enter the new listening port if it was modified.</span></span>
    
      - <span data-ttu-id="f95a5-120">Настройте **транспортный протокол SIP**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-120">Set the **Sip Transport Protocol**.</span></span>

5.  <span data-ttu-id="f95a5-121">На левой панели перейдите к **внешнему интерфейсу пула Enterprise Edition** или **серверу Standard Edition**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-121">In the left pane, navigate to the **Enterprise Edition Front End pool** or the **Standard Edition Server**.</span></span>

6.  <span data-ttu-id="f95a5-122">Щелкните пул правой кнопкой мыши и выберите команду **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-122">Right-click the pool, and then click **Edit Properties**.</span></span>

7.  <span data-ttu-id="f95a5-123">В разделе **сервер исправлений** настройте **порты прослушивания**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-123">Under **Mediation Server**, set the **Listening ports**.</span></span>

8.  <span data-ttu-id="f95a5-124">Затем свяжите вновь созданный шлюз PSTN, выделив его и нажав кнопку " **Добавить**".</span><span class="sxs-lookup"><span data-stu-id="f95a5-124">Next, associate the newly created PSTN gateway by selecting it and clicking **Add**.</span></span>

9.  <span data-ttu-id="f95a5-125">В **построителе топологии** выберите самый верхний узел **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-125">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

10. <span data-ttu-id="f95a5-126">В меню **действие** выберите пункт **топология публикации** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f95a5-126">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

11. <span data-ttu-id="f95a5-127">После завершения работы **мастера публикации** нажмите кнопку **Готово** , чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="f95a5-127">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f95a5-128">Важно выполнить следующий раздел, <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">изменить маршруты голосовой связи, чтобы использовать новый сервер исправлений Lync server 2013</A> , чтобы убедиться, что маршруты голосовой связи указывают на нужный сервер.</span><span class="sxs-lookup"><span data-stu-id="f95a5-128">It is important that you complete the next topic, <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">Change voice routes to use the new Lync Server 2013 Mediation Server</A> to ensure that the voice routes are pointing to the correct Mediation Server.</span></span>



<span data-ttu-id="f95a5-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f95a5-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

