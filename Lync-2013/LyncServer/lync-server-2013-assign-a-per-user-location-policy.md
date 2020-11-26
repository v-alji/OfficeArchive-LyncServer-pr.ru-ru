---
title: 'Lync Server 2013: назначение политики расположения для отдельных пользователей'
description: 'Lync Server 2013: назначение политики расположения для каждого пользователя.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user location policy
ms:assetid: 343f2de3-a0ae-4403-8456-6e520b579d32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520974(v=OCS.15)
ms:contentKeyID: 48183794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81631740e0a6c908c392ccacb6b37d7033d9224c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443218"
---
# <a name="assign-a-per-user-location-policy-in-lync-server-2013"></a><span data-ttu-id="37999-103">Назначение политики местоположения для каждого пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37999-103">Assign a per-user location policy in Lync Server 2013</span></span>

 


<span data-ttu-id="37999-104">Политика расположения — это один из параметров учетной записи пользователя, которую можно настроить на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="37999-104">The location policy is one of the individual settings of a user account that you can configure in the Lync Server Control Panel.</span></span>

<span data-ttu-id="37999-105">Развертывание одной или нескольких политик на расположение пользователей не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="37999-105">Deploying one or more per-user location policies is optional.</span></span> <span data-ttu-id="37999-106">Вы также можете развернуть только политику глобального уровня расположения или расположение на уровне подсети.</span><span class="sxs-lookup"><span data-stu-id="37999-106">You can also deploy only a global-level location policy or subnet-level location policy.</span></span> <span data-ttu-id="37999-107">Если выполняется развертывание политик на пользователя, необходимо явно назначить их пользователям, группам или контактным объектам.</span><span class="sxs-lookup"><span data-stu-id="37999-107">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact object.</span></span> <span data-ttu-id="37999-108">Улучшенные параметры 9-1-1 (E9-1-1) автоматически по умолчанию заданы в соответствии с политикой расположения глобального уровня, если не назначена ни одна политика для подсети или отдельно для пользователя.</span><span class="sxs-lookup"><span data-stu-id="37999-108">Enhanced 9-1-1 (E9-1-1) settings automatically default to those defined in the global-level location policy when no specific subnet-level or per-user policy is assigned.</span></span>

<span data-ttu-id="37999-109">После того как вы создадите хотя бы одну политику для каждого пользователя, выполните описанные в этой статье действия, чтобы назначить политике, указывающую параметры, которые должны применяться сервером для экстренных вызовов, размещенных конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="37999-109">After creating at least one per-user location policy, use the procedures in this topic to assign to the policy that specifies the settings that you want the server to apply for emergency calls placed by a particular user.</span></span>

<span data-ttu-id="37999-110">Список всех доступных параметров политики местоположения описан [в разделе Определение политики расположения для Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="37999-110">For a list of all available location policy settings, see [Defining the location policy for Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span></span>

<span data-ttu-id="37999-111">Подробнее о создании политик местоположений можно узнать [в статьях создание политик местоположений в Lync Server 2013](lync-server-2013-create-location-policies.md).</span><span class="sxs-lookup"><span data-stu-id="37999-111">For details about creating location policies, see [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md).</span></span>

## <a name="to-assign-a-per-user-location-policy-with-the-lync-server-control-panel"></a><span data-ttu-id="37999-112">Назначение политики местоположения для пользователя с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="37999-112">To assign a per-user location policy with the Lync Server Control Panel</span></span>

1.  <span data-ttu-id="37999-113">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="37999-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="37999-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="37999-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="37999-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="37999-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="37999-116">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="37999-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="37999-117">Используйте один из следующих методов для обнаружения пользователя:</span><span class="sxs-lookup"><span data-stu-id="37999-117">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="37999-118">В поле **Поиск пользователей** введите отображаемое имя (полностью или первую его часть), имя, фамилию, имя учетной записи SAM (Security Accounts Manager — диспетчер учетных записей безопасности), SIP-адрес или линейный идентификатор URI (Uniform Resource Identifier — универсальный код ресурса) учетной записи пользователя, а затем щелкните **Найти**.</span><span class="sxs-lookup"><span data-stu-id="37999-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="37999-119">Если у вас есть сохраненный запрос, щелкните значок **Открыть запрос**. С помощью диалогового окна **Открыть** загрузите запрос (файл .usf), а затем щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="37999-119">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="37999-120">(Необязательно) Задайте дополнительные критерии поиска, чтобы сократить количество результатов:</span><span class="sxs-lookup"><span data-stu-id="37999-120">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="37999-121">Щелкните **Добавить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="37999-121">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="37999-122">Введите свойства пользователя; для это введите его или щелкните стрелку в раскрывающемся списке, чтобы выбрать свойство.</span><span class="sxs-lookup"><span data-stu-id="37999-122">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="37999-123">В раскрывающемся списке **Равно** щелкните оператор (например, **Равно** или **Не равно**).</span><span class="sxs-lookup"><span data-stu-id="37999-123">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="37999-124">В зависимости от выбранного свойства пользователя введите критерии, которые необходимо использовать для фильтрации результатов поиска; для это введите его или щелкните стрелку в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="37999-124">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="37999-125">Чтобы добавить в запрос дополнительные условия поиска, щелкните <STRONG>Добавить фильтр</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="37999-125">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="37999-126">Щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="37999-126">Click **Find**.</span></span>

6.  <span data-ttu-id="37999-127">Выберите пользователя в списке результатов поиска, щелкните **Действие**, а затем **Назначить политики**.</span><span class="sxs-lookup"><span data-stu-id="37999-127">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="37999-128">Если вы хотите применить одну и ту же политику расположения пользователей для нескольких пользователей, выберите в результатах поиска нескольких пользователей, а затем нажмите кнопку <STRONG>действия</STRONG>и выберите команду <STRONG>назначить политики</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="37999-128">If you want the same per-user location policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="37999-129">В группе **назначение политик** в разделе **Политика расположения** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="37999-129">In **Assign Policies**, under **Location policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="37999-130">Из <STRONG> &lt; - &gt; </STRONG> за нескольких политик, которые можно настроить с помощью диалогового окна <STRONG>назначение политик</STRONG> , по умолчанию для каждой политики в диалоговом окне выбрать пункт Сохранить как.</span><span class="sxs-lookup"><span data-stu-id="37999-130">Because there are multiple policies that you can configure by using the <STRONG>Assign Policies</STRONG> dialog box, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="37999-131">Чтобы продолжить использование политики, назначенной пользователю ранее, не вносите никаких изменений в эти настройки.</span><span class="sxs-lookup"><span data-stu-id="37999-131">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="37999-132">Разрешение Lync Server 2013 для автоматического выбора политики глобального уровня или, если определено, политики на уровне подсети.</span><span class="sxs-lookup"><span data-stu-id="37999-132">Allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the subnet-level policy.</span></span>
    
      - <span data-ttu-id="37999-133">Щелкните имя политики местонахождения пользователей, которая ранее была определена, запустив командлет **New-CsLocationPolicy** .</span><span class="sxs-lookup"><span data-stu-id="37999-133">Click the name of a per-user location policy you previously defined by running the **New-CsLocationPolicy** cmdlet.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="37999-134">Чтобы выбрать политику, которую вы хотите назначить, после выбора имени политики нажмите кнопку <STRONG>Просмотр</STRONG> , чтобы просмотреть права и разрешения пользователей, определенные в политике.</span><span class="sxs-lookup"><span data-stu-id="37999-134">To help you decide the policy that you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="37999-135">По завершении щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37999-135">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-location-policy-by-using-lync-server-management-shell-cmdlets"></a><span data-ttu-id="37999-136">Назначение политики расположения Per-User с помощью командлетов командной консоли Lync Server</span><span class="sxs-lookup"><span data-stu-id="37999-136">Assigning a Per-User Location Policy by Using Lync Server Management Shell Cmdlets</span></span>

<span data-ttu-id="37999-137">Политики местоположения для каждого пользователя можно назначить с помощью командлета Grant-CsLocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="37999-137">You can assign per-user location policies by using the Grant-CsLocationPolicy cmdlet.</span></span> <span data-ttu-id="37999-138">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="37999-138">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="37999-139">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="37999-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-location-policy-to-a-single-user"></a><span data-ttu-id="37999-140">Назначение политики местоположения каждому пользователю для одного пользователя</span><span class="sxs-lookup"><span data-stu-id="37999-140">To assign a per-user location policy to a single user</span></span>

  - <span data-ttu-id="37999-141">Указанную ниже команду можно назначить политику расположения пользователя, RedmondLocationPolicy с пользователем Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="37999-141">The following command assigns the per-user location policy RedmondLocationPolicy to the user Ken Myer.</span></span>
    
        Grant-CsLocationPolicy -Identity "Ken Myer" -PolicyName "RedmondLocationPolicy"

## <a name="to-assign-a-per-user-location-policy-to-multiple-users"></a><span data-ttu-id="37999-142">Назначение политики местоположения каждому пользователю для нескольких пользователей</span><span class="sxs-lookup"><span data-stu-id="37999-142">To assign a per-user location policy to multiple users</span></span>

  - <span data-ttu-id="37999-143">Эта команда назначает политику "на расположение пользователя" AccountingDepartmentLocationPolicy всем пользователям, которые работают в отделе бухгалтерского учета.</span><span class="sxs-lookup"><span data-stu-id="37999-143">This command assigns the per-user location policy AccountingDepartmentLocationPolicy to all the users who work for the Accounting department.</span></span> <span data-ttu-id="37999-144">Дополнительные сведения о параметре LdapFilter, используемом в этой команде, можно найти в документации по командлету [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="37999-144">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=Accounting" | Grant-CsLocationPolicy -PolicyName "AccountingDepartmentLocationPolicy"

## <a name="to-unassign-a-per-user-location-policy"></a><span data-ttu-id="37999-145">Отмена политики местоположения для пользователя</span><span class="sxs-lookup"><span data-stu-id="37999-145">To unassign a per-user location policy</span></span>

  - <span data-ttu-id="37999-146">Следующая команда отменяет назначение каждой политики местонахождения пользователя, ранее назначенной для Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="37999-146">The following command unassigns any per-user location policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="37999-147">После отмены назначения для Кена Майера будет автоматически действовать глобальная политика или локальная политика сайта, если такая существует.</span><span class="sxs-lookup"><span data-stu-id="37999-147">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="37999-148">Политика сайта имеет приоритет над глобальной политикой.</span><span class="sxs-lookup"><span data-stu-id="37999-148">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsLocationPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="37999-149">Дополнительные сведения можно найти в разделе справки о командлете [Grant-CsLocationPolicy](https://technet.microsoft.com/library/gg413049\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="37999-149">For more information, see the help topic for the [Grant-CsLocationPolicy](https://technet.microsoft.com/library/gg413049\(v=ocs.15\)) cmdlet.</span></span>

