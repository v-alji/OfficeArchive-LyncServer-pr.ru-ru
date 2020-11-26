---
title: 'Lync Server 2013: назначение политики конференций для отдельных пользователей'
description: 'Lync Server 2013: назначение политики конференц-связи пользователей по каждому пользователю.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user conferencing policy
ms:assetid: 72f12c72-65f7-44fe-ab81-0f57cb2f87d1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521015(v=OCS.15)
ms:contentKeyID: 48184475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 819d1431a2a7a921ff8c306c47c8b5f86bf5d5bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440516"
---
# <a name="assign-a-per-user-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="db387-103">Назначение политики конференций для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db387-103">Assign a per-user conferencing policy in Lync Server 2013</span></span>

 


<span data-ttu-id="db387-104">Политика конференц-связи — это один из параметров учетной записи пользователя, которую можно настроить на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="db387-104">The conferencing policy is one of the individual settings of a user account that you can configure in Lync Server Control Panel.</span></span>

<span data-ttu-id="db387-105">Развертывание одной или нескольких политик конференц-связи для пользователей не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="db387-105">Deploying one or more per-user conferencing policies is optional.</span></span> <span data-ttu-id="db387-106">Вы также можете развернуть только политику Конференции глобального уровня или политику конференций на уровне сайта.</span><span class="sxs-lookup"><span data-stu-id="db387-106">You can also deploy only a global-level conferencing policy or site-level conferencing policy.</span></span> <span data-ttu-id="db387-107">Если вы выполняете развертывание политик для пользователей, необходимо явным образом назначать их пользователям, группам и контактным объектам.</span><span class="sxs-lookup"><span data-stu-id="db387-107">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact objects.</span></span> <span data-ttu-id="db387-108">Пользовательские права и разрешения для конференций автоматически определяются по умолчанию в соответствии с политикой Конференции глобального уровня, если не назначено ни одного определенного уровня сайта или политики пользователя.</span><span class="sxs-lookup"><span data-stu-id="db387-108">Conferencing user rights and permissions automatically default to those defined in the global-level conferencing policy when no specific site-level or per-user policy is assigned.</span></span>

<span data-ttu-id="db387-109">После того как вы создадите хотя бы одну политику конференций для пользователя, выполните описанные в этой статье действия, чтобы назначить политику, которая определяет права и разрешения пользователей, которые нужно предоставить серверу собраниям, упорядоченным определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="db387-109">After creating at least one per-user conferencing policy, use the procedures in this topic to assign the policy that specifies the user rights and permissions that you want the server to grant to the meetings organized by a particular user.</span></span>

<span data-ttu-id="db387-110">Список всех доступных параметров политики конференций приведен в [справочнике параметры политики конференц-связи для Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span><span class="sxs-lookup"><span data-stu-id="db387-110">For a list of all available conferencing policy settings, see [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<span data-ttu-id="db387-111">Дополнительные сведения о создании политик конференц-связи можно найти в статьях [Создание и изменение политики конференций в Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span><span class="sxs-lookup"><span data-stu-id="db387-111">For details about creating conferencing policies, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy"></a><span data-ttu-id="db387-112">Назначение политики конференции для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="db387-112">To assign a per-user conferencing policy</span></span>

1.  <span data-ttu-id="db387-113">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="db387-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="db387-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="db387-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="db387-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="db387-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="db387-116">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="db387-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="db387-117">Используйте один из следующих методов для обнаружения пользователя:</span><span class="sxs-lookup"><span data-stu-id="db387-117">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="db387-118">В поле **Поиск пользователей** введите отображаемое имя (полностью или первую его часть), имя, фамилию, имя учетной записи SAM (Security Accounts Manager — диспетчер учетных записей безопасности), SIP-адрес или линейный идентификатор URI (Uniform Resource Identifier — универсальный код ресурса) учетной записи пользователя, а затем щелкните **Найти**.</span><span class="sxs-lookup"><span data-stu-id="db387-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="db387-119">Если у вас есть сохраненный запрос, щелкните значок **Открыть запрос**. С помощью диалогового окна **Открыть** загрузите запрос (файл .usf), а затем щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="db387-119">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="db387-120">(Необязательно) Задайте дополнительные критерии поиска, чтобы сократить количество результатов:</span><span class="sxs-lookup"><span data-stu-id="db387-120">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="db387-121">Щелкните **Добавить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="db387-121">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="db387-122">Введите свойства пользователя; для это введите его или щелкните стрелку в раскрывающемся списке, чтобы выбрать свойство.</span><span class="sxs-lookup"><span data-stu-id="db387-122">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="db387-123">В раскрывающемся списке **Равно** щелкните оператор (например, **Равно** или **Не равно**).</span><span class="sxs-lookup"><span data-stu-id="db387-123">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="db387-124">В зависимости от выбранного свойства пользователя введите критерии, которые необходимо использовать для фильтрации результатов поиска; для это введите его или щелкните стрелку в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="db387-124">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="db387-125">Чтобы добавить в запрос дополнительные условия поиска, щелкните <STRONG>Добавить фильтр</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="db387-125">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="db387-126">Щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="db387-126">Click **Find**.</span></span>

6.  <span data-ttu-id="db387-127">Выберите пользователя в списке результатов поиска, щелкните **Действие**, а затем **Назначить политики**.</span><span class="sxs-lookup"><span data-stu-id="db387-127">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="db387-128">Если вы хотите применить одну и ту же политику конференций для нескольких пользователей, выберите в результатах поиска нескольких пользователей, а затем нажмите кнопку <STRONG>действия</STRONG>и выберите команду <STRONG>назначить политики</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="db387-128">If you want the same per-user conferencing policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="db387-129">В группе **назначение политик** в разделе **Политика Конференц**-связи выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="db387-129">In **Assign Policies**, under **Conferencing policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="db387-130">Поскольку есть несколько политик, которые можно настроить в разделе <STRONG>назначение политик</STRONG>, для каждой из них в диалоговом окне по умолчанию выбран параметр <STRONG> &lt; &gt; Сохранить как</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="db387-130">Because there are multiple policies that you can configure in <STRONG>Assign Policies</STRONG>, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="db387-131">Чтобы продолжить использование политики, назначенной пользователю ранее, не вносите никаких изменений в эти настройки.</span><span class="sxs-lookup"><span data-stu-id="db387-131">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="db387-132">Выберите этот параметр, **\<Automatic\>** чтобы разрешить в Lync Server 2013 автоматический выбор политики глобального уровня или, если она определена, в соответствии с политикой уровня сайта.</span><span class="sxs-lookup"><span data-stu-id="db387-132">Select **\<Automatic\>** to allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the site-level policy.</span></span>
    
      - <span data-ttu-id="db387-133">Щелкните имя политики конференц-связи пользователей, которая ранее определена на странице " **Политика Конференц** -связи".</span><span class="sxs-lookup"><span data-stu-id="db387-133">Click the name of a per-user conferencing policy you previously defined on the **Conferencing Policy** page.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="db387-134">Чтобы с легкостью определить политику, которую необходимо назначить, после выбора названия политики щелкните <STRONG>Просмотр</STRONG> для просмотра прав и разрешений пользователя, заданных в политике.</span><span class="sxs-lookup"><span data-stu-id="db387-134">To help you decide the policy you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="db387-135">По завершении щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="db387-135">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-conferencing-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="db387-136">Назначение политики конференц-связи Per-User с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="db387-136">Assigning a Per-User Conferencing Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="db387-137">Политики конференции для пользователей можно назначить с помощью Windows PowerShell и командлета Grant-CsConferencingPolicy.</span><span class="sxs-lookup"><span data-stu-id="db387-137">Per-user conferencing policies can be assigned by using Windows PowerShell and the Grant-CsConferencingPolicy cmdlet.</span></span> <span data-ttu-id="db387-138">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db387-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="db387-139">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="db387-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy-to-a-single-user"></a><span data-ttu-id="db387-140">Назначение индивидуальной политики конференц-связи с пользователями для одного пользователя</span><span class="sxs-lookup"><span data-stu-id="db387-140">To assign a per-user conferencing policy to a single user</span></span>

  - <span data-ttu-id="db387-141">Следующая команда назначает пользователю RedmondConferencingPolicy политику конференций "на пользователя" для Myer.</span><span class="sxs-lookup"><span data-stu-id="db387-141">The following command assigns the per-user conferencing policy RedmondConferencingPolicy to the user Ken Myer.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName "RedmondConferencingPolicy"

## <a name="to-assign-a-per-user-conferencing-policy-to-multiple-users"></a><span data-ttu-id="db387-142">Назначение политики конференц-связи с пользователями нескольким пользователям</span><span class="sxs-lookup"><span data-stu-id="db387-142">To assign a per-user conferencing policy to multiple users</span></span>

  - <span data-ttu-id="db387-143">Эта команда назначает политику конференц-связи пользователей HRConferencingPolicy всем пользователям, которые работают в отделе кадров.</span><span class="sxs-lookup"><span data-stu-id="db387-143">This command assigns the per-user conferencing policy HRConferencingPolicy to all the users who work for the Human Resources department.</span></span> <span data-ttu-id="db387-144">Дополнительные сведения о параметре LdapFilter, используемом в этой команде, можно найти в документации по командлету [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="db387-144">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=Human Resources" | Grant-CsConferencingPolicy -PolicyName "HRConferencingPolicy"

## <a name="to-unassign-a-per-user-conferencing-policy"></a><span data-ttu-id="db387-145">Отмена политики конференции для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="db387-145">To unassign a per-user conferencing policy</span></span>

  - <span data-ttu-id="db387-146">Следующая команда отменяет назначение каждой политики конференц-связи пользователей, ранее назначенной для Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="db387-146">The following command unassigns any per-user conferencing policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="db387-147">После отмены назначения для Кена Майера будет автоматически действовать глобальная политика или локальная политика сайта, если такая существует.</span><span class="sxs-lookup"><span data-stu-id="db387-147">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="db387-148">Политика сайта имеет приоритет над глобальной политикой.</span><span class="sxs-lookup"><span data-stu-id="db387-148">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="db387-149">Дополнительные сведения можно найти в разделе справки о командлете [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="db387-149">For more information, see the help topic for the [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="db387-150">См. также</span><span class="sxs-lookup"><span data-stu-id="db387-150">See Also</span></span>


[<span data-ttu-id="db387-151">Создание и изменение политики конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db387-151">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)  


[<span data-ttu-id="db387-152">Назначение политик для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db387-152">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

