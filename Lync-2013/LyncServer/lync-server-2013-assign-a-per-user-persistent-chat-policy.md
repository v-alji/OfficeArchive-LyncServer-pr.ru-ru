---
title: 'Lync Server 2013: назначение политики постоянного чата для отдельных пользователей'
description: 'Lync Server 2013: назначение политики постоянного чата для отдельных пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user Persistent Chat policy
ms:assetid: e22168f2-fde1-4f0a-b194-1fc881436822
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721908(v=OCS.15)
ms:contentKeyID: 49733842
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 637f1947fff7f4e919e5f9c252c047b2d0e60392
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443197"
---
# <a name="assign-a-per-user-persistent-chat-policy-in-lync-server-2013"></a><span data-ttu-id="20d72-103">Назначение политики постоянного чата для каждого пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20d72-103">Assign a per-user Persistent Chat policy in Lync Server 2013</span></span>

 


<span data-ttu-id="20d72-104">Вы можете назначить политику постоянного чата для отдельных пользователей с помощью панели управления Lync Server 2013 или оболочки управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20d72-104">You can assign a per-user persistent chat policy with either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="20d72-105">Дополнительные сведения о создании политик пользователей для постоянного сервера чата содержатся [в разделе Создание политики пользователей для сохраняемого чата в Lync Server 2013](lync-server-2013-create-a-user-policy-for-persistent-chat.md).</span><span class="sxs-lookup"><span data-stu-id="20d72-105">For details on creating user policies for Persistent Chat Server, see [Create a user policy for Persistent Chat in Lync Server 2013](lync-server-2013-create-a-user-policy-for-persistent-chat.md).</span></span>

## <a name="to-assign-a-per-user-persistent-chat-policy-with-lync-server-control-panel"></a><span data-ttu-id="20d72-106">Назначение политики постоянного чата для каждого пользователя с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="20d72-106">To assign a per-user persistent chat policy with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="20d72-107">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="20d72-107">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="20d72-108">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="20d72-108">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="20d72-109">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="20d72-109">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="20d72-110">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="20d72-110">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="20d72-111">Используйте один из следующих методов для обнаружения пользователя:</span><span class="sxs-lookup"><span data-stu-id="20d72-111">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="20d72-112">В поле **Поиск пользователей** введите отображаемое имя (полностью или первую его часть), имя, фамилию, имя учетной записи SAM (Security Accounts Manager — диспетчер учетных записей безопасности), SIP-адрес или линейный идентификатор URI (Uniform Resource Identifier — универсальный код ресурса) учетной записи пользователя, а затем щелкните **Найти**.</span><span class="sxs-lookup"><span data-stu-id="20d72-112">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="20d72-113">Если у вас есть сохраненный запрос, щелкните значок **Открыть запрос**. С помощью диалогового окна **Открыть** загрузите запрос (файл .usf), а затем щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="20d72-113">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="20d72-114">(Необязательно) Задайте дополнительные критерии поиска, чтобы сократить количество результатов:</span><span class="sxs-lookup"><span data-stu-id="20d72-114">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="20d72-115">Щелкните **Добавить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="20d72-115">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="20d72-116">Введите свойства пользователя; для это введите его или щелкните стрелку в раскрывающемся списке, чтобы выбрать свойство.</span><span class="sxs-lookup"><span data-stu-id="20d72-116">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="20d72-117">В раскрывающемся списке **Равно** щелкните оператор (например, **Равно** или **Не равно**).</span><span class="sxs-lookup"><span data-stu-id="20d72-117">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="20d72-118">В зависимости от выбранного свойства пользователя введите критерии, которые необходимо использовать для фильтрации результатов поиска; для это введите его или щелкните стрелку в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="20d72-118">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="20d72-119">Чтобы добавить в запрос дополнительные условия поиска, щелкните <STRONG>Добавить фильтр</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="20d72-119">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="20d72-120">Щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="20d72-120">Click **Find**.</span></span>

6.  <span data-ttu-id="20d72-121">Выберите пользователя в списке результатов поиска, щелкните **Действие**, а затем **Назначить политики**.</span><span class="sxs-lookup"><span data-stu-id="20d72-121">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="20d72-122">Если вы хотите применить одну и ту же политику постоянного чата для нескольких пользователей, выберите в результатах поиска нескольких пользователей, а затем нажмите кнопку <STRONG>действия</STRONG>и выберите команду <STRONG>назначить политики</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="20d72-122">If you want the same per-user persistent Chat policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="20d72-123">В группе **назначение политик** в разделе **Политика сохраняемого чата** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="20d72-123">In **Assign Policies**, under **Persistent Chat policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="20d72-124">Из <STRONG> &lt; - &gt; </STRONG> за нескольких политик, которые можно настроить с помощью диалогового окна <STRONG>назначение политик</STRONG> , по умолчанию для каждой политики в диалоговом окне выбрать пункт Сохранить как.</span><span class="sxs-lookup"><span data-stu-id="20d72-124">Because there are multiple policies that you can configure by using the <STRONG>Assign Policies</STRONG> dialog box, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="20d72-125">Чтобы продолжить использование политики, назначенной пользователю ранее, не вносите никаких изменений в эти настройки.</span><span class="sxs-lookup"><span data-stu-id="20d72-125">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="20d72-126">Выберите этот параметр, **\<Automatic\>** чтобы разрешить в Lync Server 2013 автоматический выбор политики глобального уровня или, если она определена, в соответствии с политикой уровня сайта.</span><span class="sxs-lookup"><span data-stu-id="20d72-126">Select **\<Automatic\>** to allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the site-level policy.</span></span>
    
      - <span data-ttu-id="20d72-127">Щелкните имя политики сохраняемого пользователя, который вы ранее определили на странице " **Политика сохраняемого чата** ".</span><span class="sxs-lookup"><span data-stu-id="20d72-127">Click the name of a per-user Persistent Chat policy you previously defined on the **Persistent Chat Policy** page.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="20d72-128">Чтобы с легкостью определить политику, которую необходимо назначить, после выбора названия политики щелкните <STRONG>Просмотр</STRONG> для просмотра прав и разрешений пользователя, заданных в политике.</span><span class="sxs-lookup"><span data-stu-id="20d72-128">To help you decide the policy you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="20d72-129">По завершении щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="20d72-129">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-persistent-chat-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="20d72-130">Назначение Per-User политики сохраняемого чата с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="20d72-130">Assigning a Per-User Persistent Chat Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="20d72-131">Вы также можете назначить политики постоянного чата для пользователей с помощью командлета **Grant-CsPersistentChatPolicy** .</span><span class="sxs-lookup"><span data-stu-id="20d72-131">You can also assign per-user persistent chat policies by using the **Grant-CsPersistentChatPolicy** cmdlet.</span></span> <span data-ttu-id="20d72-132">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20d72-132">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="20d72-133">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="20d72-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-persistent-chat-policy-to-a-single-user"></a><span data-ttu-id="20d72-134">Назначение политики постоянного чата для каждого пользователя одному пользователю</span><span class="sxs-lookup"><span data-stu-id="20d72-134">To assign a per-user persistent chat policy to a single user</span></span>

  - <span data-ttu-id="20d72-135">Указанная ниже команда назначает политику постоянного чата для каждого пользователя, RedmondPersistentChatPolicy с пользователем Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="20d72-135">The following command assigns the per-user Persistent Chat policy RedmondPersistentChatPolicy to the user Ken Myer.</span></span>
    
        Grant-CsPersistentChatPolicy -Identity "Ken Myer" -PolicyName "RedmondPersistentChatPolicy"

## <a name="to-assign-a-per-user-persistent-chat-policy-to-multiple-users"></a><span data-ttu-id="20d72-136">Назначение политики постоянного чата для каждого пользователя нескольким пользователям</span><span class="sxs-lookup"><span data-stu-id="20d72-136">To assign a per-user persistent chat policy to multiple users</span></span>

  - <span data-ttu-id="20d72-137">Эта команда назначает политику постоянного чата для отдельных пользователей, RedmondUsersPersistentChatPolicy всем пользователям, которые работают в ИТ-отделе.</span><span class="sxs-lookup"><span data-stu-id="20d72-137">This command assigns the per-user Persistent Chat policy RedmondUsersPersistentChatPolicy to all the users who work for the IT department.</span></span> <span data-ttu-id="20d72-138">Дополнительные сведения о параметре LdapFilter, используемом в этой команде, можно найти в документации по командлету [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="20d72-138">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=IT" | Grant-CsPersistentChatPolicy -PolicyName "RedmondUsersPersistentChatPolicy"

## <a name="to-unassign-a-per-user-persistent-chat-policy"></a><span data-ttu-id="20d72-139">Отмена назначения политики постоянного чата для каждого пользователя</span><span class="sxs-lookup"><span data-stu-id="20d72-139">To unassign a per-user persistent chat policy</span></span>

  - <span data-ttu-id="20d72-140">Следующая команда отменяет назначение любой политики постоянного чата для каждого пользователя, ранее назначенной для Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="20d72-140">The following command unassigns any per-user Persistent Chat policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="20d72-141">После отмены назначения для Кена Майера будет автоматически действовать глобальная политика или локальная политика сайта, если такая существует.</span><span class="sxs-lookup"><span data-stu-id="20d72-141">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="20d72-142">Политика сайта имеет приоритет над глобальной политикой.</span><span class="sxs-lookup"><span data-stu-id="20d72-142">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsPersistentChatPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="20d72-143">Дополнительные сведения можно найти в разделе справки о командлете [Grant-CsPersistentChatPolicy](https://technet.microsoft.com/library/jj204907\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="20d72-143">For more information, see the help topic for the [Grant-CsPersistentChatPolicy](https://technet.microsoft.com/library/jj204907\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="20d72-144">См. также</span><span class="sxs-lookup"><span data-stu-id="20d72-144">See Also</span></span>


[<span data-ttu-id="20d72-145">Создание пользовательской политики для сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20d72-145">Create a user policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-user-policy-for-persistent-chat.md)

