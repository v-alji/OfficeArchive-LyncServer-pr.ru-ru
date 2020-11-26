---
title: Перемещение объектов контактов единой системы обмена сообщениями Exchange
description: Перемещение объектов контактов для единой системы обмена сообщениями Exchange.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move Exchange Unified Messaging Contact objects
ms:assetid: 35c7e987-41b5-4798-b617-3303f20e52e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688022(v=OCS.15)
ms:contentKeyID: 49733612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e3353427f407523a8778585d27201355714a3085
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438449"
---
# <a name="move-exchange-unified-messaging-contact-objects"></a><span data-ttu-id="56a3a-103">Перемещение объектов контактов единой системы обмена сообщениями Exchange</span><span class="sxs-lookup"><span data-stu-id="56a3a-103">Move Exchange Unified Messaging Contact objects</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56a3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56a3a-104">

<span> </span></span></span>

<span data-ttu-id="56a3a-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="56a3a-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="56a3a-106">Для миграции объектов контактов для автосекретаря (AA) и доступа к подписчикам (SA) на новый сервер Lync Server 2013 сначала нужно переместить объекты из устаревшего развертывания Office Communications Server 2007 R2 на новое развертывание Lync Server 2013 с помощью командлетов **Get-CsExUmContact** и **Move-CsExUmContact** .</span><span class="sxs-lookup"><span data-stu-id="56a3a-106">To migrate Auto Attendant (AA) and Subscriber Access (SA) contact objects to the new Lync Server 2013 deployment, you first move the objects from the legacy Office Communications Server 2007 R2 deployment to the new the Lync Server 2013 deployment using the **Get-CsExUmContact** and **Move-CsExUmContact** cmdlets.</span></span> <span data-ttu-id="56a3a-107">На сервере Exchange Server вы можете запустить сценарий Windows PowerShell **ExchUCUtil** , чтобы сделать следующее для вновь развернутого пула Lync:</span><span class="sxs-lookup"><span data-stu-id="56a3a-107">On the Exchange Server, you then run the **ExchUCUtil** Windows PowerShell script to do the following for the newly deployed Lync pool:</span></span>

  - <span data-ttu-id="56a3a-108">Добавьте его в IP-шлюз единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="56a3a-108">Add it to the Unified Messaging IP gateways.</span></span>

  - <span data-ttu-id="56a3a-109">Добавьте его в группу слежения единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="56a3a-109">Add it to the Unified Messaging hunt groups.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="56a3a-110">Чтобы использовать командлеты <STRONG>Get-CsExUmContact</STRONG> и <STRONG>Move-CsExUmContact</STRONG> , вы должны быть участником группы RTCUNIVERSALUSERADMINS и иметь разрешение OU на подразделение, в котором хранятся объекты контактов.</span><span class="sxs-lookup"><span data-stu-id="56a3a-110">In order to use the <STRONG>Get-CsExUmContact</STRONG> and <STRONG>Move-CsExUmContact</STRONG> cmdlets, you must be a member of the RTCUniversalUserAdmins group and have organizational unit (OU) permission to the OU where the contacts objects are stored.</span></span> <span data-ttu-id="56a3a-111">Разрешение OU можно предоставить с помощью командлета <STRONG>Grant-OUPermission</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="56a3a-111">OU permission can be granted using the <STRONG>Grant-OUPermission</STRONG> cmdlet.</span></span>



</div>

<div>

## <a name="to-move-contact-objects-by-using-the-lync-server-management-shell"></a><span data-ttu-id="56a3a-112">Перемещение объектов контакта с помощью командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="56a3a-112">To move contact objects by using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="56a3a-113">Откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="56a3a-113">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="56a3a-114">Для каждого пула, зарегистрированного в единой системе обмена сообщениями Exchange (где pool1.contoso.net — это пул из конфигурации Office Communications Server 2007 R2 и pool2.contoso.net — это пул из развертывания Lync Server 2013), введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="56a3a-114">For each pool registered with Exchange UM (where pool1.contoso.net is a pool from the Office Communications Server 2007 R2 deployment and pool2.contoso.net is the pool from the Lync Server 2013 deployment) at the command line, type the following:</span></span>
    
        Get-CsExUmContact -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsExUmContact -Target pool02.contoso.net
    
    <span data-ttu-id="56a3a-115">Чтобы убедиться в том, что объекты контакта перемещены, выполните командлет **Get-CsExumContact** и убедитесь, что в **RegistrarPool** указывает на новый пул.</span><span class="sxs-lookup"><span data-stu-id="56a3a-115">To verify that the contact objects are moved, run the **Get-CsExumContact** cmdlet and confirm that **RegistrarPool** is now pointing to the new pool.</span></span>

</div>

<div>

## <a name="to-run-the-exchucutil-windows-powershell-script"></a><span data-ttu-id="56a3a-116">Выполнение сценария Windows PowerShell ExchUCUtil</span><span class="sxs-lookup"><span data-stu-id="56a3a-116">To run the ExchUCUtil Windows PowerShell script</span></span>

1.  <span data-ttu-id="56a3a-117">Войдите на сервер Exchange UM как пользователь с правами администратора организации Exchange.</span><span class="sxs-lookup"><span data-stu-id="56a3a-117">Log on to the Exchange UM Server as a user with Exchange Organization Administrator privileges.</span></span>

2.  <span data-ttu-id="56a3a-118">Перейдите на ExchUCUtil сценарий Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="56a3a-118">Navigate to the ExchUCUtil Windows PowerShell script.</span></span>
    
    <span data-ttu-id="56a3a-119">В Exchange 2007 ExchUCUtil.ps1 расположен по адресу: **% Program Files \\ % \\ сценариев Microsoft Exchange Server \\ \\ExchUCUtil.ps1**</span><span class="sxs-lookup"><span data-stu-id="56a3a-119">In Exchange 2007, ExchUCUtil.ps1 is located at: **%Program Files%\\Microsoft\\Exchange Server\\Scripts\\ExchUCUtil.ps1**</span></span>
    
    <span data-ttu-id="56a3a-120">В Exchange 2010 ExchUCUtil.ps1 расположен по адресу: **% Program Files \\ % \\ \\ V14 \\ Scripts \\ for Microsoft Exchange ServerExchUCUtil.ps1**</span><span class="sxs-lookup"><span data-stu-id="56a3a-120">In Exchange 2010, ExchUCUtil.ps1 is located at: **%Program Files%\\Microsoft\\Exchange Server\\V14\\Scripts\\ExchUCUtil.ps1**</span></span>

3.  <span data-ttu-id="56a3a-121">Если Exchange развернут в одном лесе, введите:</span><span class="sxs-lookup"><span data-stu-id="56a3a-121">If Exchange is deployed in a single forest, type:</span></span>
    
        exchucutil.ps1
    
    <span data-ttu-id="56a3a-122">Если Exchange развернут в нескольких лесах, введите:</span><span class="sxs-lookup"><span data-stu-id="56a3a-122">Or, if Exchange is deployed in multiple forests, type:</span></span>
    
        exchucutil.ps1 -Forest:" <forest FQDN>"
    
    <span data-ttu-id="56a3a-123">где полное доменное имя леса определяет лес, в котором развернут Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="56a3a-123">where forest FQDN specifies the forest in which Lync Server 2013 is deployed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="56a3a-124">Не забудьте перезапустить службу <STRONG>переднего плана Lync Server</STRONG> (rtcsrv.exe) <EM>после</EM> запуска exchucutil.ps1.</span><span class="sxs-lookup"><span data-stu-id="56a3a-124">Be sure to restart the <STRONG>Lync Server Front-End</STRONG> service (rtcsrv.exe) <EM>after</EM> you run exchucutil.ps1.</span></span> <span data-ttu-id="56a3a-125">В противном случае Lync Server 2013 не будет определять единую систему обмена сообщениями в топологии.</span><span class="sxs-lookup"><span data-stu-id="56a3a-125">Otherwise, Lync Server 2013 will not detect Unified Messaging in the topology.</span></span>

    
    <span data-ttu-id="56a3a-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56a3a-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

