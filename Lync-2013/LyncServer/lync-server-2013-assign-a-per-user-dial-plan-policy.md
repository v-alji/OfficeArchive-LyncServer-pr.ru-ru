---
title: 'Lync Server 2013: назначение политики абонентской группы для отдельных пользователей'
description: 'Lync Server 2013: назначение политики абонентской группы для отдельных пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user dial plan policy
ms:assetid: 9fea861f-7770-4cae-9b1f-2a960595bfc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688156(v=OCS.15)
ms:contentKeyID: 49733760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 654c1f15ccb1efa4d1aa35d957df7a2654fa41d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443204"
---
# <a name="assign-a-per-user-dial-plan-policy-in-lync-server-2013"></a><span data-ttu-id="ed03d-103">Назначение политики абонентской группы для пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed03d-103">Assign a per-user dial plan policy in Lync Server 2013</span></span>

 


<span data-ttu-id="ed03d-104">Чтобы завершить настройку учетной записи пользователя либо для пользователей корпоративной голосовой связи, либо для пользователей конференц-связи с телефонным подключением, пользователю должна быть назначена абонентская группа.</span><span class="sxs-lookup"><span data-stu-id="ed03d-104">To complete user account configuration for either users of Enterprise Voice or users of dial-in conferencing, the user must be assigned a dial plan.</span></span> <span data-ttu-id="ed03d-105">Учетные записи пользователей будут автоматически использовать глобальную абонентскую группу или, если таковая существует, абонентская группа на уровне сайта, если вы не хотите явным образом назначать существующий абонентский набор для пользователей.</span><span class="sxs-lookup"><span data-stu-id="ed03d-105">User accounts will automatically use the global dial plan or, if one exists, the site-level dial plan when you do not explicitly assign an existing per-user dial plan.</span></span> <span data-ttu-id="ed03d-106">Если вы хотите использовать глобальную или общую абонентскую группу для всех пользователей, для которых разрешена Корпоративная голосовая связь, вы можете пропустить этот раздел.</span><span class="sxs-lookup"><span data-stu-id="ed03d-106">If you want to use the global or site dial plan for all users that are enabled for Enterprise Voice, you can skip this section.</span></span>

## <a name="to-assign-a-dial-plan-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="ed03d-107">Назначение абонентской группы с помощью панели управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed03d-107">To assign a dial plan by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="ed03d-108">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ed03d-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ed03d-109">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ed03d-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ed03d-110">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ed03d-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ed03d-111">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="ed03d-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="ed03d-112">В поле **Поиск пользователей** введите отображаемое имя или его начальный фрагмент, имя, фамилию, имя учетной записи (диспетчера учетных записей безопасности (SAM), SIP-адрес или строку универсального кода ресурса (URI) из учетной записи пользователя, которому требуется предоставить доступ, затем нажмите кнопку **Найти**.</span><span class="sxs-lookup"><span data-stu-id="ed03d-112">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="ed03d-113">В таблице выберите учетную запись пользователя, которому вы хотите назначить абонентскую группу.</span><span class="sxs-lookup"><span data-stu-id="ed03d-113">In the table, click the user account that you want to assign a dial plan.</span></span>

6.  <span data-ttu-id="ed03d-114">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="ed03d-114">On the **Edit** menu, click **Show details**.</span></span>

7.  <span data-ttu-id="ed03d-115">На странице " **изменение пользователя Lync Server** " в разделе **телефония** выберите **Корпоративный голосовой звонок**.</span><span class="sxs-lookup"><span data-stu-id="ed03d-115">On the **Edit Lync Server User** page, under **Telephony**, click **Enterprise Voice**.</span></span>

8.  <span data-ttu-id="ed03d-116">Нажмите кнопку **Политика набора номера**, а затем выберите нужную абонентскую группу.</span><span class="sxs-lookup"><span data-stu-id="ed03d-116">Click **Dial plan policy**, and then choose the desired dial plan.</span></span>

9.  <span data-ttu-id="ed03d-117">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="ed03d-117">Click **Commit**.</span></span>

<span data-ttu-id="ed03d-118">Дополнительные сведения о настройке абонентской группы можно найти в разделе [Настройка абонентских группа в Lync Server 2013](lync-server-2013-configuring-dial-plans.md) .</span><span class="sxs-lookup"><span data-stu-id="ed03d-118">For details about configuring dial plans, see the [Configuring dial plans in Lync Server 2013](lync-server-2013-configuring-dial-plans.md) topic.</span></span>

## <a name="assign-a-per-user-dial-plan-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ed03d-119">Назначение Per-User абонентской группы с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed03d-119">Assign a Per-User Dial Plan by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ed03d-120">Вы можете назначить абонентские планы для пользователей с помощью Windows PowerShell и командлетом **Grant-CsdialPlan** .</span><span class="sxs-lookup"><span data-stu-id="ed03d-120">You can assign per-user dial plans with Windows PowerShell and the **Grant-CsdialPlan** cmdlet.</span></span> <span data-ttu-id="ed03d-121">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ed03d-121">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ed03d-122">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ed03d-122">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-dial-plan-to-a-single-user"></a><span data-ttu-id="ed03d-123">Назначение абонентской группы на уровне пользователей отдельному пользователю</span><span class="sxs-lookup"><span data-stu-id="ed03d-123">To assign a per-user dial plan to a single user</span></span>

  - <span data-ttu-id="ed03d-124">Следующая команда назначает пользователю RedmondDialPlanную абонентскую группу, которую пользователь Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="ed03d-124">The following command assigns the per-user dial plan RedmondDialPlan to the user Ken Myer.</span></span>
    
        Grant-CsDialPlan -Identity "Ken Myer" -PolicyName "RedmondDialPlan"

## <a name="to-assign-a-per-user-dial-plan-to-multiple-users"></a><span data-ttu-id="ed03d-125">Назначение абонентской группы на уровне пользователей нескольким пользователям</span><span class="sxs-lookup"><span data-stu-id="ed03d-125">To assign a per-user dial plan to multiple users</span></span>

  - <span data-ttu-id="ed03d-126">Эта команда назначает абонентскую группу для пользователей RedmondDialPlan всем пользователям, которые работают в городе Redmond.</span><span class="sxs-lookup"><span data-stu-id="ed03d-126">This command assigns the per-user dial plan RedmondDialPlan to all the users who work in the city of Redmond.</span></span> <span data-ttu-id="ed03d-127">Дополнительные сведения о параметре LdapFilter, используемом в этой команде, можно найти в документации по командлету [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="ed03d-127">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "l=Redmond" | Grant-CsDialPlan -PolicyName "RedmondDialPlan"

## <a name="to-unassign-a-per-user-dial-plan"></a><span data-ttu-id="ed03d-128">Назначение абонентской группы на уровне пользователей</span><span class="sxs-lookup"><span data-stu-id="ed03d-128">To unassign a per-user dial plan</span></span>

  - <span data-ttu-id="ed03d-129">Следующая команда отменяет назначение каждого абонентского плана, ранее назначенного Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="ed03d-129">The following command unassigns any per-user dial plan previously assigned to Ken Myer.</span></span> <span data-ttu-id="ed03d-130">После того как абонентская группа не будет назначена, Кен Myer будет автоматически управляться с помощью глобальной абонентской группы, локальной абонентской группы (если она существует) или абонентской группы, назначенной своему регистратору или шлюзу PSTN.</span><span class="sxs-lookup"><span data-stu-id="ed03d-130">After the per-user dial plan is unassigned, Ken Myer will automatically be managed by using the global dial plan, his local site dial plan (if one exists), or the service-scope dial plan assigned to his Registrar or PSTN gateway.</span></span> <span data-ttu-id="ed03d-131">Абонентская группа, использующая область обслуживания, имеет приоритет перед любой абонентской панелью и имеет приоритет над глобальной абонентской панелью.</span><span class="sxs-lookup"><span data-stu-id="ed03d-131">A service scope dial plan takes precedence over any site dial plan, and a site dial plan takes precedence over the global dial plan.</span></span>
    
        Grant-CsDialPlan -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="ed03d-132">Дополнительные сведения можно найти в разделе справки о командлете [Grant-CsDialPlan](https://technet.microsoft.com/library/gg398547\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="ed03d-132">For more information, see the help topic for the [Grant-CsDialPlan](https://technet.microsoft.com/library/gg398547\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed03d-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ed03d-133">See Also</span></span>


[<span data-ttu-id="ed03d-134">Настройка абонентских групп в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed03d-134">Configuring dial plans in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-plans.md)  
[<span data-ttu-id="ed03d-135">Учетные записи пользователей, включенные для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed03d-135">User accounts enabled for Lync Server 2013</span></span>](lync-server-2013-user-accounts-enabled-for-lync-server.md)

