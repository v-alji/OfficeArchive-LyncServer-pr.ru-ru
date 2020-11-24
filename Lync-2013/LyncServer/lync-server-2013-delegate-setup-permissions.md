---
title: 'Lync Server 2013: делегирование разрешений на установку'
description: 'Lync Server 2013: Делегирование разрешений на настройку.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegate setup permissions
ms:assetid: 9dca1683-4c69-4534-8ebe-6bd635cbae49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412735(v=OCS.15)
ms:contentKeyID: 48184997
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a7038cf729bad459dbcd2a84a308b14aa56b68dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398233"
---
# <a name="delegate-setup-permissions-in-lync-server-2013"></a><span data-ttu-id="92944-103">Делегирование разрешений на установку в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="92944-103">Delegate setup permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="92944-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="92944-104">

<span> </span></span></span>

<span data-ttu-id="92944-105">_**Тема последнего изменения:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="92944-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="92944-106">Если вы не хотите предоставлять членство в группе "Администраторы домена" пользователям или группам, которые развертывают Lync Server 2013, вы можете включить членов группы RTCUniversalServerAdmins для запуска командлета Windows PowerShell **Enable-CsTopology** на серверах с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="92944-106">If you do not want to grant membership in the Domain Admins group to users or groups who are deploying Lync Server 2013, you can enable members of the RTCUniversalServerAdmins group to run the **Enable-CsTopology** Windows PowerShell cmdlet on servers running Lync Server 2013.</span></span> <span data-ttu-id="92944-107">По умолчанию участники группы RTCUniversalServerAdmins не могут выполнять этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92944-107">By default, members of the RTCUniversalServerAdmins group do not have the ability to run this cmdlet.</span></span> <span data-ttu-id="92944-108">Вы можете предоставить права администратора и разрешения на запуск команды **Enable-CsTopology** на серверах с Lync Server, используя командлет **Grant-CsSetupPermission** и УКАЗАВ подразделение (OU), в котором находятся объекты компьютеров для сервера с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="92944-108">You grant administrator rights and permissions to run **Enable-CsTopology** on servers running Lync Server by using the **Grant-CsSetupPermission** cmdlet and specifying an organizational unit (OU) where computer objects for the server running Lync Server 2013 are located.</span></span>

<span data-ttu-id="92944-109">Подготовка домена, которая выполняется при установке Lync Server, не добавляет автоматически разрешения, позволяющие членам группы RTCUniversalServerAdmins запускать командлеты Enable-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="92944-109">The domain preparation that takes place when you install Lync Server does not automatically add the permissions that enable members of the RTCUniversalServerAdmins group to run the Enable-CsTopology cmdlet.</span></span> <span data-ttu-id="92944-110">Это означает, что по умолчанию вы должны быть администратором домена, чтобы включить топологию.</span><span class="sxs-lookup"><span data-stu-id="92944-110">That means that, by default, you must be a domain administrator in order to enable a topology.</span></span> <span data-ttu-id="92944-111">Чтобы предоставить участникам группы RTCUniversalServerAdmins право на включение топологии, необходимо выполнить командлет Grant-CsSetupPermissions.</span><span class="sxs-lookup"><span data-stu-id="92944-111">To give members of the RTCUniversalServerAdmins group the right to enable a topology you must run the Grant-CsSetupPermissions cmdlet.</span></span> <span data-ttu-id="92944-112">Кроме того, вам потребуется выполнить этот командлет для каждого контейнера Active Directory, который используется для работы компьютеров с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="92944-112">In addition, you will need to run this cmdlet against each Active Directory container that houses computers running Lync Server.</span></span>

<span data-ttu-id="92944-113">Имейте в виду, что этот командлет предоставляет разрешения только группе RTCUniversalServerAdmins; Этот командлет не может использоваться для предоставления разрешений другим группам безопасности или отдельным пользователям.</span><span class="sxs-lookup"><span data-stu-id="92944-113">Keep in mind that this cmdlet only grants permissions to the RTCUniversalServerAdmins group; the cmdlet cannot be used to grant permissions to other security groups or to individual users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="92944-114"><STRONG>Enable-CsTopology</STRONG> — это ключевой командлет, позволяющий членам группы RTCUniversalServerAdmins настраивать и развертывать Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="92944-114"><STRONG>Enable-CsTopology</STRONG> is the key cmdlet to allow the RTCUniversalServerAdmins group members to set up and deploy Lync Server 2013.</span></span>



</div>

<div>

## <a name="to-add-the-ability-to-run-enable-cstopology-to-the-rtcuniversalserveradmins-group"></a><span data-ttu-id="92944-115">Добавление в группу RTCUniversalServerAdmins возможности запуска Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="92944-115">To add the ability to run Enable-CsTopology to the RTCUniversalServerAdmins group</span></span>

1.  <span data-ttu-id="92944-116">Войдите на сервер в качестве участника группы "Администраторы домена" для домена, на котором делегированный пользователь будет выполнять **функцию Enable-CsTopology**.</span><span class="sxs-lookup"><span data-stu-id="92944-116">Log on to a server as a member of the Domain Admins group for the domain on which the delegated user will run **Enable-CsTopology**.</span></span>

2.  <span data-ttu-id="92944-117">Откройте консоль управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="92944-117">Open the Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="92944-118">Управляющая консоль Lync Server 2013 автоматически устанавливается на каждый сервер переднего плана или на любой компьютер, на котором установлены средства администрирования Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="92944-118">The Lync Server 2013 Management Shell is automatically installed on each Front End Server or any computer where the Lync Server 2013 administrative tools have been installed.</span></span> <span data-ttu-id="92944-119">Подробные сведения о командной консоли Lync Server 2013 можно найти в руководстве по [управлению Lync server 2013](lync-server-2013-lync-server-management-shell.md) в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="92944-119">For details about the Lync Server 2013 Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) in the Operations documentation.</span></span>

3.  <span data-ttu-id="92944-120">Запустите из командной консоли Lync Server 2013 следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="92944-120">Run the following cmdlet from the Lync Server 2013 Management Shell:</span></span>
    
        Grant-CsSetupPermission -ComputerOU <DN of the OU> -Domain <Domain FQDN>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="92944-121">Если подразделение имеет верхний уровень, необходимо указать полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="92944-121">If the OU is not top level, you must provide the full domain name.</span></span>

    
    </div>
    
    <span data-ttu-id="92944-122">В приведенном ниже примере подразделением является "серверы Lync", которые находятся в домене contoso.com.</span><span class="sxs-lookup"><span data-stu-id="92944-122">In the following example, the OU is “Lync Servers,” which is in the contoso.com domain.</span></span>
    
        Grant-CsSetupPermission -ComputerOU "OU=Lync Servers" -Domain contoso.com

<span data-ttu-id="92944-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="92944-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

