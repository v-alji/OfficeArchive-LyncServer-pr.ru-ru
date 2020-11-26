---
title: 'Lync Server 2013: назначение политики доступа внешних пользователей пользователю, разрешенному для Lync'
description: 'Lync Server 2013: назначение внешней политики доступа пользователей для пользователя с поддержкой Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign an external user access policy to a Lync enabled user
ms:assetid: 736fcaad-9f95-4896-b767-e199d86a00a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398551(v=OCS.15)
ms:contentKeyID: 48184483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2be3ea52e6e44400b3967d7c3346da2297220675
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443498"
---
# <a name="assign-an-external-user-access-policy-to-a-lync-enabled-user-in-lync-server-2013"></a><span data-ttu-id="5c299-103">Назначение политики доступа внешних пользователей пользователю, разрешенному для Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c299-103">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c299-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c299-104">

<span> </span></span></span>

<span data-ttu-id="5c299-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="5c299-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="5c299-106">Если для пользователя разрешено использование Lync Server, вы можете настроить федерацию SIP, Федерацию XMPP, удаленный доступ к данным и обмен мгновенными сообщениями на панели управления Lync Server, применив соответствующие политики для конкретных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5c299-106">If a user has been enabled for Lync Server, you can configure SIP federation, XMPP federation, remote user access, and public instant messaging (IM) connectivity in the Lync Server Control Panel by applying the appropriate policies to specific users.</span></span> <span data-ttu-id="5c299-107">Например, если вы создали политику для поддержки удаленного доступа пользователей, необходимо применить ее к пользователю, прежде чем пользователь сможет подключиться к серверу Lync Server из удаленного местоположения и будет работать совместно с внешними пользователями из удаленного местоположения.</span><span class="sxs-lookup"><span data-stu-id="5c299-107">For example, if you created a policy to support remote user access, you must apply it to the user before the user can connect to Lync Server from a remote location and collaborate with internal users from the remote location.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5c299-108">Для поддержки внешнего доступа пользователей необходимо включить поддержку для каждого типа внешних пользователей, которые будут поддерживаться, и настроить соответствующие политики и другие параметры для управления его использованием.</span><span class="sxs-lookup"><span data-stu-id="5c299-108">To support external user access, you must enable support for each type of external user access you want to support, and configure the appropriate policies and other options to control its use.</span></span> <span data-ttu-id="5c299-109">Подробности можно найти в разделе <A href="lync-server-2013-configuring-support-for-external-user-access.md">Настройка поддержки внешних пользователей в Lync server 2013</A> в документации по развертыванию или <A href="lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md">Управление интеграцией и внешним доступом к Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="5c299-109">For details, see <A href="lync-server-2013-configuring-support-for-external-user-access.md">Configuring support for external user access in Lync Server 2013</A> in the Deployment documentation or <A href="lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md">Managing federation and external access to Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<span data-ttu-id="5c299-110">В этой статье описана процедура применения ранее созданной политики доступа внешних пользователей к одной или нескольким учетным записям пользователей.</span><span class="sxs-lookup"><span data-stu-id="5c299-110">Use the procedure in this topic to apply a previously created external user access policy to one or more user accounts.</span></span>

<div>

## <a name="to-apply-an-external-user-policy-to-a-user-account"></a><span data-ttu-id="5c299-111">Применение политики внешних пользователей к учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="5c299-111">To apply an external user policy to a user account</span></span>

1.  <span data-ttu-id="5c299-112">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="5c299-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5c299-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5c299-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5c299-114">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5c299-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5c299-115">В левой панели навигации нажмите **Пользователи** и выполните поиск учетной записи, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="5c299-115">In the left navigation bar, click **Users**, and then search on the user account that you want to configure.</span></span>

4.  <span data-ttu-id="5c299-116">В таблице с результатами поиска выберите нужную учетную запись, нажмите кнопку **Изменить** и выберите пункт **Показать сведения**.</span><span class="sxs-lookup"><span data-stu-id="5c299-116">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="5c299-117">В диалоговом окне **изменение пользователя Lync Server** в разделе " **Политика внешнего доступа**" выберите политику пользователей, которую вы хотите применить.</span><span class="sxs-lookup"><span data-stu-id="5c299-117">In **Edit Lync Server User** under **External access policy**, select the user policy that you want to apply.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5c299-118">Параметры <STRONG> &lt; автоматической &gt; </STRONG> настройки применяются к параметрам сервера или глобальной политики, используемым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c299-118">The <STRONG>&lt;Automatic&gt;</STRONG> settings apply the default server or global policy settings.</span></span>

    
    </div>

</div>

<div>

## <a name="assigning-per-user-external-access-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="5c299-119">Назначение Per-User политик внешнего доступа с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c299-119">Assigning Per-User External Access Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="5c299-120">Политики внешнего доступа для каждого пользователя можно назначить с помощью Windows PowerShell и командлета Grant-CsExternalAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="5c299-120">Per-user external access policies can be assigned by using Windows PowerShell and the Grant-CsExternalAccessPolicy cmdlet.</span></span> <span data-ttu-id="5c299-121">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5c299-121">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="5c299-122">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="5c299-122">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-assign-a-per-user-external-access-policy-to-a-single-user"></a><span data-ttu-id="5c299-123">Назначение политики внешнего доступа для отдельных пользователей одному пользователю</span><span class="sxs-lookup"><span data-stu-id="5c299-123">To assign a per-user external access policy to a single user</span></span>

  - <span data-ttu-id="5c299-124">Эта команда назначает политику внешнего доступа для каждого пользователя, RedmondExternalAccessPolicy пользователю Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="5c299-124">This command assigns the per-user external access policy RedmondExternalAccessPolicy to the user Ken Myer.</span></span>
    
        Grant-CsExternalAccessPolicy -Identity "Ken Myer" -PolicyName "RedmondExternalAccessPolicy"

</div>

<div>

## <a name="to-assign-a-per-user-external-access-policy-to-multiple-users"></a><span data-ttu-id="5c299-125">Назначение политики внешнего доступа для каждого пользователя нескольким пользователям</span><span class="sxs-lookup"><span data-stu-id="5c299-125">To assign a per-user external access policy to multiple users</span></span>

  - <span data-ttu-id="5c299-126">Эта команда назначает политику внешнего доступа "на пользователя" USAExternalAccessPolicy всем пользователям, у которых есть учетные записи в подразделении "США" в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5c299-126">This command assigns the per-user external access policy USAExternalAccessPolicy to all the users who have accounts in the UnitedStates OU in Active Directory.</span></span> <span data-ttu-id="5c299-127">Дополнительные сведения о параметре OU, используемом в этой команде, можно найти в документации по командлету [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) .</span><span class="sxs-lookup"><span data-stu-id="5c299-127">For more information on the OU parameter used in this command, see the documentation for the [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) cmdlet.</span></span>
    
        Get-CsUser -OU "ou=UnitedStates,dc=litwareinc,dc=com" | Grant-CsExternalAccessPolicy -PolicyName "USAExternalAccessPolicy"

</div>

<div>

## <a name="to-unassign-a-per-user-external-access-policy"></a><span data-ttu-id="5c299-128">Отмена назначения политики внешнего доступа для каждого пользователя</span><span class="sxs-lookup"><span data-stu-id="5c299-128">To unassign a per-user external access policy</span></span>

  - <span data-ttu-id="5c299-129">Эта команда отменяет назначение любой пользовательской политики внешнего доступа, ранее назначенной для Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="5c299-129">This command unassigns any per-user external access policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="5c299-130">После отмены назначения для Кена Майера будет автоматически действовать глобальная политика или локальная политика сайта, если такая существует.</span><span class="sxs-lookup"><span data-stu-id="5c299-130">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="5c299-131">Политика сайта имеет приоритет над глобальной политикой.</span><span class="sxs-lookup"><span data-stu-id="5c299-131">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsExternalAccessPolicy -Identity "Ken Myer" -PolicyName $Null

</div>

<span data-ttu-id="5c299-132">Дополнительные сведения можно найти в разделе справки о командлете [Grant-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsExternalAccessPolicy) .</span><span class="sxs-lookup"><span data-stu-id="5c299-132">For more information, see the help topic for the [Grant-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsExternalAccessPolicy) cmdlet.</span></span>

<span data-ttu-id="5c299-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c299-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

