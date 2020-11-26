---
title: 'Lync Server 2013: восстановление сервера участника Enterprise Edition'
description: 'Lync Server 2013: восстановление сервера участника Enterprise Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring an Enterprise Edition member server
ms:assetid: d960b19c-2104-4719-b736-0d940f254d42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202191(v=OCS.15)
ms:contentKeyID: 51541523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f9838f030205d92988e185798d982f835122c9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436211"
---
# <a name="restoring-an-enterprise-edition-member-server-in-lync-server-2013"></a><span data-ttu-id="cec38-103">Восстановление сервера участника Enterprise Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cec38-103">Restoring an Enterprise Edition member server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cec38-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cec38-104">

<span> </span></span></span>

<span data-ttu-id="cec38-105">_**Тема последнего изменения:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="cec38-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="cec38-106">Если сервер, на котором запущен один из указанных ниже ролей сервера, не проходит, выполните процедуру, описанную в этой статье, чтобы восстановить сервер.</span><span class="sxs-lookup"><span data-stu-id="cec38-106">If a server running one of the following server roles fails, follow the procedure in this topic to restore the server.</span></span> <span data-ttu-id="cec38-107">Если несколько серверов не обменяются независимо друг от друга, выполните действия, описанные для каждого сервера.</span><span class="sxs-lookup"><span data-stu-id="cec38-107">If multiple servers fail independently, follow the procedure for each server.</span></span>

  - <span data-ttu-id="cec38-108">переднего плана</span><span class="sxs-lookup"><span data-stu-id="cec38-108">Front End Server</span></span>

  - <span data-ttu-id="cec38-109">Сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="cec38-109">Mediation Server</span></span>

  - <span data-ttu-id="cec38-110">Директор</span><span class="sxs-lookup"><span data-stu-id="cec38-110">Director</span></span>

  - <span data-ttu-id="cec38-111">Сервер сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="cec38-111">Persistent Chat Server</span></span>

  - <span data-ttu-id="cec38-112">Пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="cec38-112">Edge Server</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="cec38-113">Прежде чем начать восстановление, мы рекомендуем использовать копию системы с изображением.</span><span class="sxs-lookup"><span data-stu-id="cec38-113">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="cec38-114">Вы можете использовать это изображение как точку отката, если что-то пойдет не так во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="cec38-114">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="cec38-115">После установки операционной системы и сервера SQL Server вы можете использовать копию изображения, а также восстановить или подать заявку на сертификаты.</span><span class="sxs-lookup"><span data-stu-id="cec38-115">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-a-member-server"></a><span data-ttu-id="cec38-116">Восстановление рядового сервера</span><span class="sxs-lookup"><span data-stu-id="cec38-116">To restore a member server</span></span>

1.  <span data-ttu-id="cec38-117">Начните с чистого или нового сервера с таким же полным доменным именем (FQDN), как и у сервера, на котором произошел сбой, установите операционную систему, а затем восстановите или порегистрируйте сертификаты.</span><span class="sxs-lookup"><span data-stu-id="cec38-117">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed server, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cec38-118">Следуйте инструкциям по развертыванию сервера в своей организации, чтобы выполнить этот шаг.</span><span class="sxs-lookup"><span data-stu-id="cec38-118">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="cec38-119">Войдите в учетную запись пользователя, которая входит в группу RTCUniversalServerAdmins, на сервере, который вы хотите восстановить.</span><span class="sxs-lookup"><span data-stu-id="cec38-119">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="cec38-120">Перейдите к папке установки Lync Server или к носителю, а затем запустите мастер развертывания Lync Server, расположенный на странице \\ Setup \\ amd64 \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="cec38-120">Browse to the Lync Server installation folder or media, and start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span>

4.  <span data-ttu-id="cec38-121">Следуйте указаниям мастера развертывания, чтобы выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cec38-121">Follow the Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="cec38-122">Выполните **Шаг 1: установите локальное хранилище конфигураций** , чтобы установить локальные файлы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cec38-122">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="cec38-123">Запустите **Шаг 2: Настройка или удаление компонентов Lync Server** , чтобы установить роль сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cec38-123">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server role.</span></span>
    
    3.  <span data-ttu-id="cec38-124">Запустите **Шаг 3: запросите, установите или назначьте сертификаты** для назначения сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cec38-124">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="cec38-125">Выполните **Шаг 4: запуск служб** для запуска служб на сервере.</span><span class="sxs-lookup"><span data-stu-id="cec38-125">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="cec38-126">Дополнительные сведения о запуске мастера развертывания можно найти в документации по развертыванию роли сервера, которую вы восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="cec38-126">For details about running the Deployment Wizard, see the Deployment documentation for the server role that you are restoring.</span></span>

<span data-ttu-id="cec38-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cec38-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

