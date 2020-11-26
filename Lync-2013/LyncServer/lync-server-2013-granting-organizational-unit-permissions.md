---
title: 'Lync Server 2013: предоставление разрешений организационного подразделения'
description: 'Lync Server 2013: предоставление разрешений на доступ к организационному подразделению.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting organizational unit permissions
ms:assetid: 95ee5ffa-39b1-4d80-87a2-27bb364f7396
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398763(v=OCS.15)
ms:contentKeyID: 48184849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47ad862241e409190620afa7dbf4fa73adf339de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427899"
---
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a><span data-ttu-id="e64f7-103">Предоставление разрешений организационного подразделения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e64f7-103">Granting organizational unit permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e64f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e64f7-104">

<span> </span></span></span>

<span data-ttu-id="e64f7-105">_**Тема последнего изменения:** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="e64f7-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="e64f7-106">Командлет **Grant-CsOuPermission** можно использовать, чтобы предоставить разрешения на доступ к объектам в указанных организационных подразделениях (OU) таким образом, чтобы пользователи универсальных групп RTC, созданные с помощью подготовки леса, могли получать к ним доступа, не прибегая к группе администраторов домена.</span><span class="sxs-lookup"><span data-stu-id="e64f7-106">You can use the **Grant-CsOuPermission** cmdlet to grant permissions to objects in specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access them without being members of the Domain Admins group.</span></span> <span data-ttu-id="e64f7-107">Разрешения, добавленные в указанный ОРГАНИЗАЦИОНный элемент, являются теми же разрешениями, которые командлет **Enable-CsAdDomain** добавляет к контейнерам компьютеров и пользователей во время подготовки домена.</span><span class="sxs-lookup"><span data-stu-id="e64f7-107">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users containers during domain preparation.</span></span>

<span data-ttu-id="e64f7-108">Используйте командлет **Test-CsOuPermission** для проверки разрешений, настроенных с помощью командлета **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="e64f7-108">Use the **Test-CsOuPermission** cmdlet to verify the permissions you set up by using the **Grant-CsOuPermission** cmdlet.</span></span>

<span data-ttu-id="e64f7-109">Командлет **REVOKE-CsOuPermission** можно использовать для удаления разрешений, предоставленных с помощью командлета **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="e64f7-109">You can use the **Revoke-CsOuPermission** cmdlet to remove permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-ou-permissions"></a><span data-ttu-id="e64f7-110">Предоставление разрешений на доступ к подразделению</span><span class="sxs-lookup"><span data-stu-id="e64f7-110">To grant OU permissions</span></span>

1.  <span data-ttu-id="e64f7-111">Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите предоставить разрешения на доступ к подразделению.</span><span class="sxs-lookup"><span data-stu-id="e64f7-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant OU permissions.</span></span> <span data-ttu-id="e64f7-112">Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.</span><span class="sxs-lookup"><span data-stu-id="e64f7-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="e64f7-113">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="e64f7-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e64f7-114">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e64f7-114">Run:</span></span>
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="e64f7-115">Если параметр Domain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="e64f7-115">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-ou-permissions"></a><span data-ttu-id="e64f7-116">Проверка разрешений на доступ к подразделению</span><span class="sxs-lookup"><span data-stu-id="e64f7-116">To verify OU permissions</span></span>

1.  <span data-ttu-id="e64f7-117">Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите проверить разрешения на доступ к подразделению, предоставленные с помощью командлета **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="e64f7-117">Log on to a computer running Lync Server 2013 in the domain where you want to verify OU permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="e64f7-118">Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.</span><span class="sxs-lookup"><span data-stu-id="e64f7-118">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="e64f7-119">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="e64f7-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e64f7-120">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e64f7-120">Run:</span></span>
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="e64f7-121">Если параметр Domain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="e64f7-121">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-ou-permissions"></a><span data-ttu-id="e64f7-122">Отмена разрешений на доступ к подразделению</span><span class="sxs-lookup"><span data-stu-id="e64f7-122">To revoke OU permissions</span></span>

1.  <span data-ttu-id="e64f7-123">Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите отозвать разрешения на доступ к подразделению, предоставленные командлетом **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="e64f7-123">Log on to a computer running Lync Server 2013 in the domain where you want to revoke OU permissions that were granted by the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="e64f7-124">Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.</span><span class="sxs-lookup"><span data-stu-id="e64f7-124">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="e64f7-125">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="e64f7-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e64f7-126">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e64f7-126">Run:</span></span>
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="e64f7-127">Если параметр Domain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="e64f7-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="e64f7-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e64f7-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

