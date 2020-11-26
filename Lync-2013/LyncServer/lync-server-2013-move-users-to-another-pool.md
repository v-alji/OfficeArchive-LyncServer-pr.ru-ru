---
title: 'Lync Server 2013: перемещение пользователей в другой пул'
description: 'Lync Server 2013: перемещение пользователей в другой пул.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move users to another pool
ms:assetid: e7b4968c-0e9d-4d56-b5f1-9edf0f7206f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182600(v=OCS.15)
ms:contentKeyID: 48185879
ms.date: 02/09/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 21012e0df7567a79bca018d194878c85b8653ae4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425285"
---
# <a name="move-users-to-another-pool-in-lync-server-2013"></a><span data-ttu-id="d1476-103">Перемещение пользователей в другой пул в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1476-103">Move users to another pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1476-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1476-104">

<span> </span></span></span>

<span data-ttu-id="d1476-105">_**Тема последнего изменения:** 2018-02-09_</span><span class="sxs-lookup"><span data-stu-id="d1476-105">_**Topic Last Modified:** 2018-02-09_</span></span>

<span data-ttu-id="d1476-106">Вы можете назначить пользователей для определенного сервера или пула с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1476-106">You can use Lync Server Control Panel to assign users to a specific server or pool.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="d1476-107">Перемещение всех существующих пользователей из исходного пула, на котором работает Lync Server 2010 или более ранней версии, в составе пула Lync Server 2013 в сложной среде Active Directory может привести к более медленной репликации Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d1476-107">Moving all existing users from a source pool that is running Lync Server 2010 or earlier to a Lync Server 2013 destination pool in a complex Active Directory environment might result in slower Active Directory replication.</span></span> <span data-ttu-id="d1476-108">Чтобы избежать этого, вы можете использовать фильтры поиска для перемещения пользователей из пулов, использующих Lync Server 2010 или более ранней версии, или с помощью командной консоли Lync Server для перемещения пользователей с помощью командлетов.</span><span class="sxs-lookup"><span data-stu-id="d1476-108">To avoid this, you can use search filters to move users from pools that are running Lync Server 2010 or earlier separately, or you can use Lync Server Management Shell to move users with cmdlets.</span></span> <span data-ttu-id="d1476-109">Кроме того, функции фильтра работают с пользователями Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d1476-109">Also, the filter functionality works with Lync Server 2013 users.</span></span>



</div>

<div>

## <a name="to-move-selected-users-to-a-different-server-or-pool"></a><span data-ttu-id="d1476-110">Перемещение выбранных пользователей на другой сервер или в пул</span><span class="sxs-lookup"><span data-stu-id="d1476-110">To move selected users to a different server or pool</span></span>

1.  <span data-ttu-id="d1476-111">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d1476-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d1476-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1476-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d1476-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d1476-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d1476-114">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="d1476-114">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="d1476-115">В поле **Поиск пользователей** введите все или первую часть отображаемого имени, имя, фамилию, диспетчер учетных записей безопасности (SAM), имя учетной записи, адрес SIP или универсальный код ресурса (URI) нужной учетной записи пользователя, а затем нажмите кнопку **найти**.</span><span class="sxs-lookup"><span data-stu-id="d1476-115">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want, and then click **Find**.</span></span>

5.  <span data-ttu-id="d1476-116">В таблице выберите определенного пользователя или пользователей из списка.</span><span class="sxs-lookup"><span data-stu-id="d1476-116">In the table, select a specific user or users in the list.</span></span>

6.  <span data-ttu-id="d1476-117">В меню **действие** выберите пункт **переместить выбранных пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="d1476-117">On the **Action** menu, click **Move selected users to pool**.</span></span>

7.  <span data-ttu-id="d1476-118">В разделе **Перемещение пользователей** выберите пул, в который вы хотите переместить пользователей, в **пул конечных регистраторов**.</span><span class="sxs-lookup"><span data-stu-id="d1476-118">In **Move Users**, select the pool that you want to move the users to in **Destination registrar pool**.</span></span>

8.  <span data-ttu-id="d1476-119">Необязательно Если целевой сервер или пул недоступны, установите флажок **принудительно** .</span><span class="sxs-lookup"><span data-stu-id="d1476-119">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="d1476-120">Если выбрать параметр <STRONG>принудительно</STRONG>, учетная запись пользователя будет перемещена, но связанные данные пользователя, такие как запланированные конференции и контакты, не будут перемещены.</span><span class="sxs-lookup"><span data-stu-id="d1476-120">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-all-users-from-one-server-or-pool-to-a-different-server-or-pool"></a><span data-ttu-id="d1476-121">Перемещение всех пользователей с одного сервера или пула на другой</span><span class="sxs-lookup"><span data-stu-id="d1476-121">To move all users from one server or pool to a different server or pool</span></span>

1.  <span data-ttu-id="d1476-122">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d1476-122">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d1476-123">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1476-123">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d1476-124">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d1476-124">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d1476-125">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="d1476-125">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="d1476-126">В меню **действие** выберите пункт **переместить всех пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="d1476-126">On the **Action** menu, click **Move all users to pool**.</span></span>

5.  <span data-ttu-id="d1476-127">В разделе **Перемещение пользователей** выберите пул, содержащий учетные записи пользователей, которые вы хотите переместить в **пуле исходного регистратора**.</span><span class="sxs-lookup"><span data-stu-id="d1476-127">In **Move Users**, select the pool that contains the user accounts that you want to move in **Source registrar pool**.</span></span>

6.  <span data-ttu-id="d1476-128">В **пуле конечных регистраторов** выберите пул, на который вы хотите переместить пользователей.</span><span class="sxs-lookup"><span data-stu-id="d1476-128">In **Destination registrar pool**, select the pool that you want to move the users to.</span></span>

7.  <span data-ttu-id="d1476-129">Необязательно Если целевой сервер или пул недоступны, установите флажок **принудительно** .</span><span class="sxs-lookup"><span data-stu-id="d1476-129">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="d1476-130">Если выбрать параметр <STRONG>принудительно</STRONG>, учетная запись пользователя будет перемещена, но связанные данные пользователя, такие как запланированные конференции и контакты, не будут перемещены.</span><span class="sxs-lookup"><span data-stu-id="d1476-130">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-users-from-one-pool-to-a-different-pool-by-using-a-filter"></a><span data-ttu-id="d1476-131">Перемещение пользователей из одного пула в другой с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="d1476-131">To move users from one pool to a different pool by using a filter</span></span>

1.  <span data-ttu-id="d1476-132">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d1476-132">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d1476-133">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1476-133">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d1476-134">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d1476-134">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d1476-135">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="d1476-135">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="d1476-136">В окне **Поиск пользователей** нажмите кнопку **Поиск** и выберите команду **Добавить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="d1476-136">In **User Search**, click **Search**, and then click **Add Filter**.</span></span>

5.  <span data-ttu-id="d1476-137">В условия поиска выберите пункт **пул регистраторов**, нажмите **кнопку равно**, выберите значение **Текущее полное доменное имя пула** и нажмите кнопку **найти**.</span><span class="sxs-lookup"><span data-stu-id="d1476-137">In the Search criteria, select **Registrar Pool**, select **Equal to**, select **Current Pool FQDN**, and then click **Find**.</span></span>

6.  <span data-ttu-id="d1476-138">В меню **действие** выберите пункт **переместить всех пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="d1476-138">On the **Action** menu, click **Move all users to pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d1476-139">Если фильтр применяется к существующему набору пользователей, параметр <STRONG>перемещает всех пользователей в пул</STRONG> в контексте фильтрованного подмножества пользователей, а не <STRONG><EM>всех</EM></STRONG> возможных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d1476-139">When a filter is applied to an existing set of users, the option <STRONG>Move all users to pool</STRONG> is in the context of the filtered subset of users, not <STRONG><EM>all</EM></STRONG> possible users.</span></span>

    
    </div>

7.  <span data-ttu-id="d1476-140">В разделе **Перемещение пользователей** выберите пул, содержащий учетные записи пользователей, которые вы хотите переместить в **пуле исходного регистратора**.</span><span class="sxs-lookup"><span data-stu-id="d1476-140">In **Move Users**, select the pool that contains the user accounts that you want to move in **Source registrar pool**.</span></span>

8.  <span data-ttu-id="d1476-141">В **пуле конечных регистраторов** выберите пул, куда вы хотите переместить пользователей.</span><span class="sxs-lookup"><span data-stu-id="d1476-141">In **Destination registrar pool**, select the pool where you want to move the users.</span></span>

9.  <span data-ttu-id="d1476-142">Необязательно Если целевой сервер или пул недоступны, установите флажок **принудительно** .</span><span class="sxs-lookup"><span data-stu-id="d1476-142">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="d1476-143">Если выбрать параметр <STRONG>принудительно</STRONG>, учетная запись пользователя будет перемещена, но связанные данные пользователя, такие как запланированные конференции и контакты, не будут перемещены.</span><span class="sxs-lookup"><span data-stu-id="d1476-143">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-users-from-one-pool-to-another-using-windows-powershell-cmdlets"></a><span data-ttu-id="d1476-144">Перемещение пользователей из одной группы в другую с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1476-144">To move users from one pool to another using Windows PowerShell cmdlets</span></span>

1.  <span data-ttu-id="d1476-145">В зависимости от того, как выполняются команды Windows PowerShell (локально или удаленно), необходимо войти в систему в качестве участника правильной административной роли Lync Server 2013, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="d1476-145">Depending on how you run Windows PowerShell commands (that is, locally or remotely), you need to log on as a member of the correct Lync Server 2013 administrative roles as follows:</span></span>
    
    1.  <span data-ttu-id="d1476-146">Если вы выполняете команды на локальном компьютере (например, входите на сервер переднего плана): Войдите в систему на компьютере, на котором установлена оболочка Lync Server Management Shell, в качестве участника группы RTCUniversalServerAdmins или с необходимыми правами, как описано в разделе [Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d1476-146">If you are running the commands on the local machine (for example, you log on directly to a Front End Server): Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>
    
    2.  <span data-ttu-id="d1476-147">Если вы запускаете команды удаленно на другом компьютере (например, входите на компьютер и выполняете команды удаленно на стандартном внешнем сервере выпуска): от учетной записи пользователя, которой назначена роль CsUserAdministrator или роли CsAdministrator, войдите на любой компьютер во внутренней среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="d1476-147">If you are running the commands remotely on another computer (for example, you log on to your computer and run the commands remotely on a Standard Edition Front End Server): From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d1476-148">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="d1476-148">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d1476-149">Для перемещения отдельных пользователей используйте командлет Move-CsUser, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="d1476-149">To move single users, use the Move-CsUser cmdlet as follows:</span></span>
    
        Move-CsUser -Identity "Pilar Ackerman" -Target "pool01.contoso.net"
    
    <span data-ttu-id="d1476-150">Там, где пользователь может перемещаться — пользователь почтового Вронский, и пользователь перемещается из текущего назначенного домашнего пула в пул pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d1476-150">Where the user to move is the user Pilar Ackerman, and the user will be moved from their currently assigned home pool to the pool pool01.contoso.net</span></span>

4.  <span data-ttu-id="d1476-151">Чтобы переместить большое количество пользователей, используйте фильтры с командлетом **Get-CsUser** и передавайте получившийся набор пользователей для перемещения. **CsUser**:</span><span class="sxs-lookup"><span data-stu-id="d1476-151">To move a large number of users, use filters with the **Get-CsUser** cmdlet and pass the resulting set of users to **Move-CsUser**:</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "CurrentPoolFqdn"} | Move-CsUser -Target "TargetPoolFQDN"
    
    <span data-ttu-id="d1476-152">Объединенные команды **Get-CsUser** и **Move-CsUser** могут привести к следующим результатам:</span><span class="sxs-lookup"><span data-stu-id="d1476-152">The combined commands of the **Get-CsUser** and **Move-CsUser** might result in this:</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "pool02.contoso.net"} | Move-CsUser -Target "pool01.contoso.net"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d1476-153">См. также</span><span class="sxs-lookup"><span data-stu-id="d1476-153">See Also</span></span>


[<span data-ttu-id="d1476-154">Изменение свойств учетной записи пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1476-154">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)  
  

<span data-ttu-id="d1476-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1476-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

