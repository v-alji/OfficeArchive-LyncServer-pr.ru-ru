---
title: 'Lync Server 2013: делегирование административного управления Lync Server'
description: 'Lync Server 2013: делегирование административного управления Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegating administrative control of Lync Server 2013
ms:assetid: 0f378eff-8ef4-4c60-9fd2-67d7ee259ef8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520951(v=OCS.15)
ms:contentKeyID: 48183418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8d3710af2d194a5aa4ebdd7291be2ee58176507
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430765"
---
# <a name="delegating-administrative-control-of-lync-server-2013"></a><span data-ttu-id="07995-103">Делегирование административного управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07995-103">Delegating administrative control of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07995-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07995-104">

<span> </span></span></span>

<span data-ttu-id="07995-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="07995-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="07995-106">В Lync Server 2013 задачи администрирования делегируются пользователям с помощью новой функции управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="07995-106">In Lync Server 2013, administrative tasks are delegated to users by using the new role-based access control (RBAC) feature.</span></span> <span data-ttu-id="07995-107">При установке сервера Lync Server создаются несколько ролей RBAC.</span><span class="sxs-lookup"><span data-stu-id="07995-107">When you install Lync Server, a number of RBAC roles are created for you.</span></span> <span data-ttu-id="07995-108">These roles correspond to universal security groups in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="07995-108">These roles correspond to universal security groups in Active Directory Domain Services.</span></span> <span data-ttu-id="07995-109">Например, роль RBAC CsHelpDesk соответствует группе CsHelpDesk, которая находится в контейнере Users доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07995-109">For example, the RBAC role CsHelpDesk corresponds to the CsHelpDesk group found in the Users container in Active Directory Domain Services.</span></span> <span data-ttu-id="07995-110">Кроме того, каждая роль RBAC связана с набором командлетов Windows PowerShell для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="07995-110">In addition, each RBAC role is associated with a set of Lync Server Windows PowerShell cmdlets.</span></span> <span data-ttu-id="07995-111">Эти командлеты представляют задачи, которые могут быть выполнены пользователями, которым назначена данная роль RBAC.</span><span class="sxs-lookup"><span data-stu-id="07995-111">These cmdlets represent the tasks that can be carried out by users who have been assigned the given RBAC role.</span></span> <span data-ttu-id="07995-112">Например, роль CsHelpDesk назначила командлеты Lock-CsClientPin и UnlockCsClientPin.</span><span class="sxs-lookup"><span data-stu-id="07995-112">For example, the CsHelpDesk role has been assigned the Lock-CsClientPin and UnlockCsClientPin cmdlets.</span></span> <span data-ttu-id="07995-113">Это означает, что пользователи, которым назначена роль CsHelpDesk, могут блокировать и разблокирование PIN-кодов пользователей.</span><span class="sxs-lookup"><span data-stu-id="07995-113">That means users who have been assigned the CsHelpDesk role can lock and unlock user PIN numbers.</span></span> <span data-ttu-id="07995-114">Однако роль CsHelpDesk не назначила командлету New-CsVoicePolicy.</span><span class="sxs-lookup"><span data-stu-id="07995-114">However, the CsHelpDesk role has not been assigned the New-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="07995-115">Это означает, что пользователи, которым назначена роль CsHelpDesk, не могут создавать новые политики голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="07995-115">That means that users who have been assigned the CsHelpDesk role cannot create new voice policies.</span></span>

<div>

## <a name="viewing-information-about-rbac-roles"></a><span data-ttu-id="07995-116">Просмотр сведений о ролях RBAC</span><span class="sxs-lookup"><span data-stu-id="07995-116">Viewing Information about RBAC Roles</span></span>

<span data-ttu-id="07995-117">Вы можете получить основные сведения о ролях RBAC, выполнив в командной консоли Lync Server следующую команду:</span><span class="sxs-lookup"><span data-stu-id="07995-117">You can retrieve basic information about your RBAC roles by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRole

<span data-ttu-id="07995-118">Имейте в виду, что идентификатор роли RBAC (например, CsVoiceAdministrator) имеет прямое сопоставление с группой безопасности, обнаруженной в контейнере Users доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07995-118">Keep in mind that the Identity of the RBAC role (for example, CsVoiceAdministrator) has a direct mapping to a security group found in the Users container in Active Directory Domain Services.</span></span>

<span data-ttu-id="07995-119">Чтобы просмотреть список командлетов, назначенных для роли, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="07995-119">To view a list of the cmdlets that have been assigned to a role, use a command similar to this:</span></span>

    Get-CsAdminRole -Identity "CsHelpDesk" | Select-Object -ExpandProperty Cmdlets

</div>

<div>

## <a name="assigning-an-rbac-role-to-a-user"></a><span data-ttu-id="07995-120">Назначение роли RBAC пользователю</span><span class="sxs-lookup"><span data-stu-id="07995-120">Assigning an RBAC Role to a User</span></span>

<span data-ttu-id="07995-121">Чтобы назначить пользователю роль RBAC, необходимо добавить этого пользователя в соответствующую группу безопасности Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07995-121">To assign an RBAC role to a user, you must add that user to the appropriate Active Directory security group.</span></span> <span data-ttu-id="07995-122">Например, чтобы назначить пользователю роль CsLocationAdministrator, необходимо добавить этого пользователя в группу CsLocationAdministrator.</span><span class="sxs-lookup"><span data-stu-id="07995-122">For example, to assign the CsLocationAdministrator role to a user, you must add that user to the CsLocationAdministrator group.</span></span> <span data-ttu-id="07995-123">Это можно сделать, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="07995-123">That can be done by carrying out the following procedure:</span></span>

<span data-ttu-id="07995-124">**Назначение пользователя группе безопасности**</span><span class="sxs-lookup"><span data-stu-id="07995-124">**To assign a user to a security group**</span></span>

1.  <span data-ttu-id="07995-125">Используя учетную запись, которая имеет разрешение на изменение членства группы Active Directory, войдите в систему на компьютере, на котором установлен компонент "пользователи и компьютеры Active Directory".</span><span class="sxs-lookup"><span data-stu-id="07995-125">Using an account that has permission to modify the membership of an Active Directory group, log on to a computer where Active Directory Users and Computers has been installed.</span></span>

2.  <span data-ttu-id="07995-126">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Администрирование**, а затем — **Пользователи и компьютеры Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="07995-126">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

3.  <span data-ttu-id="07995-127">В окне "пользователи и компьютеры Active Directory" разверните имя своего домена и щелкните контейнер " **Пользователи** ".</span><span class="sxs-lookup"><span data-stu-id="07995-127">In Active Directory Users and Computers, expand the name of your domain and click the **Users** container.</span></span>

4.  <span data-ttu-id="07995-128">Щелкните правой кнопкой мыши группу безопасности **CsLocationAdministrator** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="07995-128">Right-click the security group **CsLocationAdministrator**, and then click **Properties**.</span></span>

5.  <span data-ttu-id="07995-129">В диалоговом окне **Свойства** на вкладке **члены** нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="07995-129">In the **Properties** dialog box, on the **Members** tab, click **Add**.</span></span>

6.  <span data-ttu-id="07995-130">В диалоговом окне **Выбор пользователей, компьютеров, контактов или групп** введите имя пользователя или отображаемое имя пользователя, которого нужно добавить в группу (например, **Кен Myer**) в поле **Введите имена объектов, которые нужно выделить** , и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="07995-130">In the **Select Users, Computers, Contacts, or Groups** dialog box, type the user name or display name of the user to be added to the group (for example, **Ken Myer**) in the **Enter the object names to select** box and then click **OK**.</span></span>

7.  <span data-ttu-id="07995-131">В диалоговом окне " **Свойства** " нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="07995-131">In the **Properties** dialog box, click **OK**.</span></span>

<span data-ttu-id="07995-132">Чтобы убедиться в том, что роль RBAC назначена, используйте командлет [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) , передав командлету значение SAMAccountName (имя для входа в службу каталогов Active Directory) для пользователя.</span><span class="sxs-lookup"><span data-stu-id="07995-132">To verify that the RBAC role has been assigned, use the [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) cmdlet, passing the cmdlet the SamAccountName (Active Directory logon name) of the user.</span></span> <span data-ttu-id="07995-133">Например, выполните эту команду в командной консоли Lync Server Management Shell:</span><span class="sxs-lookup"><span data-stu-id="07995-133">For example, run this command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRoleAssignment  -Identity "kenmyer"

<span data-ttu-id="07995-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07995-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

