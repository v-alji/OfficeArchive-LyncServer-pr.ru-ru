---
title: 'Lync Server 2013: предоставление разрешений на установку'
description: 'Lync Server 2013: предоставление разрешений на настройку.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting setup permissions
ms:assetid: 15982bfe-6844-44f6-815a-72dcaf0e4d21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398225(v=OCS.15)
ms:contentKeyID: 48183491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5523494219d07907caeefc1bd139c41856effa54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427902"
---
# <a name="granting-setup-permissions-in-lync-server-2013"></a><span data-ttu-id="dd5e5-103">Предоставление разрешений на установку в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd5e5-103">Granting setup permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd5e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd5e5-104">

<span> </span></span></span>

<span data-ttu-id="dd5e5-105">_**Тема последнего изменения:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="dd5e5-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="dd5e5-106">Вы можете использовать командлет **Grant-CsSetupPermission** , чтобы добавить разрешения на чтение, запись, ReadSPN и WriteSPN для группы RTCUniversalServerAdmins для указанного организационного подразделения Active Directory (OU).</span><span class="sxs-lookup"><span data-stu-id="dd5e5-106">You can use the **Grant-CsSetupPermission** cmdlet to add Read, Write, ReadSPN, and WriteSPN permissions to the RTCUniversalServerAdmins group for a specified Active Directory organizational unit (OU).</span></span> <span data-ttu-id="dd5e5-107">Затем члены группы RTCUniversalServerAdmins в этом подразделении могут устанавливать серверы, на которых запущен Lync Server 2013 в указанном домене, и не входить в группу администраторов домена.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-107">Then members of the RTCUniversalServerAdmins group in that OU can install servers running Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="dd5e5-108">Используйте командлет **Test-CsSetupPermission** для проверки разрешений, настроенных с помощью командлета **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="dd5e5-108">Use the **Test-CsSetupPermission** cmdlet to verify the permissions you set up by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<span data-ttu-id="dd5e5-109">Командлет **REVOKE-CsSetupPermission** можно использовать для удаления разрешений, предоставленных с помощью командлета **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="dd5e5-109">You can use the **Revoke-CsSetupPermission** cmdlet to remove permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-setup-permissions"></a><span data-ttu-id="dd5e5-110">Предоставление разрешений на настройку</span><span class="sxs-lookup"><span data-stu-id="dd5e5-110">To grant setup permissions</span></span>

1.  <span data-ttu-id="dd5e5-111">Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите предоставить разрешения на установку.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant setup permissions.</span></span> <span data-ttu-id="dd5e5-112">Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="dd5e5-113">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="dd5e5-114">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dd5e5-114">Run:</span></span>
    
        Grant-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="dd5e5-115">Параметр ComputerOu можно задать относительно контекста именования по умолчанию для указанного домена (например, CN = Computers).</span><span class="sxs-lookup"><span data-stu-id="dd5e5-115">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="dd5e5-116">Кроме того, вы можете указать этот параметр в качестве полного различающегося имени OU (DN), например "CN = Computers, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="dd5e5-116">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="dd5e5-117">В последнем случае необходимо указать различающееся имя OU, соответствующее указанному домену.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-117">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="dd5e5-118">Если параметр Domain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-118">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-setup-permissions"></a><span data-ttu-id="dd5e5-119">Проверка разрешений на установку</span><span class="sxs-lookup"><span data-stu-id="dd5e5-119">To verify setup permissions</span></span>

1.  <span data-ttu-id="dd5e5-120">Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите проверить разрешения на установку, предоставленные с помощью командлета **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="dd5e5-120">Log on to a computer running Lync Server 2013 in the domain where you want to verify setup permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="dd5e5-121">Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-121">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="dd5e5-122">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="dd5e5-123">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dd5e5-123">Run:</span></span>
    
        Test-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="dd5e5-124">Параметр ComputerOu можно задать относительно контекста именования по умолчанию для указанного домена (например, CN = Computers).</span><span class="sxs-lookup"><span data-stu-id="dd5e5-124">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="dd5e5-125">Кроме того, вы можете указать этот параметр в качестве полного различающегося имени OU (DN), например "CN = Computers, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="dd5e5-125">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="dd5e5-126">В последнем случае необходимо указать различающееся имя OU, соответствующее указанному домену.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-126">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="dd5e5-127">Если параметр Domain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-setup-permissions"></a><span data-ttu-id="dd5e5-128">Отмена разрешений на установку</span><span class="sxs-lookup"><span data-stu-id="dd5e5-128">To revoke setup permissions</span></span>

1.  <span data-ttu-id="dd5e5-129">Войдите на компьютер, на котором работает Lync Server 2013, в домен, для которого вы хотите отозвать разрешения на установку, предоставленные командлетом **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="dd5e5-129">Log on to a computer running Lync Server 2013 in the domain where you want to revoke setup permissions that were granted by the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="dd5e5-130">Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-130">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="dd5e5-131">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="dd5e5-132">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dd5e5-132">Run:</span></span>
    
        Revoke-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="dd5e5-133">Параметр ComputerOu можно задать относительно контекста именования по умолчанию для указанного домена (например, CN = Computers).</span><span class="sxs-lookup"><span data-stu-id="dd5e5-133">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="dd5e5-134">Кроме того, вы можете указать этот параметр в качестве полного различающегося имени OU (DN), например "CN = Computers, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="dd5e5-134">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="dd5e5-135">В последнем случае необходимо указать различающееся имя OU, соответствующее указанному домену.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-135">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="dd5e5-136">Если параметр Domain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="dd5e5-136">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="dd5e5-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd5e5-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

