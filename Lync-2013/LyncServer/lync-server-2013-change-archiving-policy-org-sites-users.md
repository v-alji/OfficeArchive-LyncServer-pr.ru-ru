---
title: 'Lync Server 2013: изменение политики архивации для включения и отключения архивирования внутренней или внешней связи для Организации, сайтов и пользователей'
description: 'Lync Server 2013: изменение политики архивации для включения или отключения архивирования внутренней или внешней связи для Организации, сайтов или пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435182"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a><span data-ttu-id="0a911-103">Изменение политики архивации в Lync Server 2013 для включения и отключения архивирования внутренней или внешней связи для Организации, сайтов и пользователей</span><span class="sxs-lookup"><span data-stu-id="0a911-103">Changing an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for your organization, sites, or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a911-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a911-104">

<span> </span></span></span>

<span data-ttu-id="0a911-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="0a911-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="0a911-106">В Lync Server 2013 вы используете политики для включения и отключения архивирования для внутренних коммуникаций и внешней связи для пользователей, размещенных на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0a911-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="0a911-107">К ним относятся следующие политики архивации:</span><span class="sxs-lookup"><span data-stu-id="0a911-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="0a911-108">Глобальная политика, созданная по умолчанию при развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0a911-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="0a911-109">Необязательные политики уровня сайта и уровня пользователя, которые можно создавать и использовать для определения способа реализации архивации для конкретных сайтов или пользователей.</span><span class="sxs-lookup"><span data-stu-id="0a911-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="0a911-110">Изначально политики архивации были настроены при развертывании архивации, но вы можете изменить, добавить и удалить политики после развертывания.</span><span class="sxs-lookup"><span data-stu-id="0a911-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="0a911-111">В панели управления Lync Server 2013 вы можете управлять политиками на глобальном уровне, уровне сайта и на уровне пользователей с помощью страницы **политики архивации** в группе **Архивация и мониторинг** .</span><span class="sxs-lookup"><span data-stu-id="0a911-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="0a911-112">Если вы интегрирует хранилище Lync Server с хранилищем Exchange 2013, политики пользователей Exchange имеют приоритет над политиками архивации Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0a911-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="0a911-113">Сведения о том, как реализованы политики, в том числе об иерархии политик, описаны [в разделе Работа с архивацией в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="0a911-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0a911-114">Если вы включили интеграцию Microsoft Exchange для развертывания, политики Exchange определяют, включено ли архивирование для пользователей, использующих Exchange 2013, и почтовые ящики помещаются на In-Place удержание.</span><span class="sxs-lookup"><span data-stu-id="0a911-114">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="0a911-115">Подробности можно найти в разделе <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Настройка политик архивации в Lync server 2013 при использовании интеграции с Exchange Server</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="0a911-115">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="0a911-116">Перед включением архивации необходимо указать все соответствующие параметры в разделе конфигурации архивации.</span><span class="sxs-lookup"><span data-stu-id="0a911-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="0a911-117">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Управление параметрами конфигурации архивации в Lync Server 2013 для Организации, сайты и пулы</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="0a911-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-change-an-archiving-policy"></a><span data-ttu-id="0a911-118">Изменение политики архивации</span><span class="sxs-lookup"><span data-stu-id="0a911-118">To change an archiving policy</span></span>

1.  <span data-ttu-id="0a911-119">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="0a911-119">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0a911-120">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0a911-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0a911-121">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0a911-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0a911-122">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Политика архивации**.</span><span class="sxs-lookup"><span data-stu-id="0a911-122">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="0a911-123">В списке политик выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="0a911-123">In the list of policies, do one of the following:</span></span>
    
      - <span data-ttu-id="0a911-124">Чтобы изменить политику для всего развертывания, в списке политик щелкните **Global** (Глобальная), щелкните **Edit** (Изменить), а затем — **Show details** (Показать сведения).</span><span class="sxs-lookup"><span data-stu-id="0a911-124">To change the policy for your entire deployment, click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="0a911-125">Чтобы изменить политику для одного сайта, выберите имя сайта в списке политик, щелкните **Edit** (Изменить) и затем щелкните **Show details** (Показать сведения).</span><span class="sxs-lookup"><span data-stu-id="0a911-125">To change the policy for a single site, click the site name in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="0a911-126">Чтобы изменить политику для отдельного пользователя или группы пользователей, выберите имя пользователя или группы пользователей в списке политик, щелкните **Edit** (Изменить) и затем щелкните **Show details** (Показать сведения).</span><span class="sxs-lookup"><span data-stu-id="0a911-126">To change the policy for a single user or user group, click the user or user group name in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="0a911-127">На странице **Edit Archiving Policy** (Изменение политики архивации) выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0a911-127">On the **Edit Archiving Policy** page, do the following:</span></span>
    
      - <span data-ttu-id="0a911-128">Чтобы включить или отключить архивацию внутренних коммуникаций, установите или снимите флажок **Archive internal communications** (Архивировать внутренние коммуникации).</span><span class="sxs-lookup"><span data-stu-id="0a911-128">To enable or disable internal archiving for the policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="0a911-129">Чтобы включить или отключить архивацию внешних коммуникаций, установите или снимите флажок **Archive external communications** (Архивировать внешние коммуникации).</span><span class="sxs-lookup"><span data-stu-id="0a911-129">To enable or disable external archiving for the policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="0a911-130">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="0a911-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0a911-131">Параметры политики пользователя применяются только к тем пользователям и группам пользователей, к которым применяется политика.</span><span class="sxs-lookup"><span data-stu-id="0a911-131">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="0a911-132">Подробнее смотрите в разделе <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">применение политики архивации для пользователей в Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="0a911-132">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="0a911-133">Включение и отключение архивации с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a911-133">Enabling and Disabling Archiving by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="0a911-134">Архивация может быть включена и отключена (как для внутренних, так и для внешних сеансов связи) с помощью командлета **Set-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="0a911-134">Archiving can be enabled and disabled (for both internal and external communication sessions) by using the **Set-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="0a911-135">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a911-135">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="0a911-136">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="0a911-136">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a><span data-ttu-id="0a911-137">Включение архивации внутренних сеансов связи</span><span class="sxs-lookup"><span data-stu-id="0a911-137">To enable the archiving of internal communication sessions</span></span>

  - <span data-ttu-id="0a911-138">Чтобы включить архивацию внутренних сеансов связи, установите для свойства **ArchiveInternal** значение True ($true).</span><span class="sxs-lookup"><span data-stu-id="0a911-138">To enable archiving of internal communication sessions, set the value of the **ArchiveInternal** property to True ($True).</span></span> <span data-ttu-id="0a911-139">Например:</span><span class="sxs-lookup"><span data-stu-id="0a911-139">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a><span data-ttu-id="0a911-140">Включение архивации внешних сеансов связи</span><span class="sxs-lookup"><span data-stu-id="0a911-140">To enable the archiving of external communication sessions</span></span>

  - <span data-ttu-id="0a911-141">Чтобы включить архивацию внешних сеансов связи, задайте для свойства **ArchiveExternal** значение True ($true).</span><span class="sxs-lookup"><span data-stu-id="0a911-141">To enable archiving of external communication sessions, set the value of the **ArchiveExternal** property to True ($True).</span></span> <span data-ttu-id="0a911-142">Например:</span><span class="sxs-lookup"><span data-stu-id="0a911-142">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="0a911-143">Включение архивации как внутренних, так и внешних сеансов связи</span><span class="sxs-lookup"><span data-stu-id="0a911-143">To enable the archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="0a911-144">Чтобы включить архивацию внутренних и внешних сеансов связи, задайте для свойств **ArchiveInternal** и **ArchiveExternal** значение true:</span><span class="sxs-lookup"><span data-stu-id="0a911-144">To enable archiving of both internal and external communications sessions, set both the **ArchiveInternal** and the **ArchiveExternal** properties to True:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a><span data-ttu-id="0a911-145">Отключение архивации</span><span class="sxs-lookup"><span data-stu-id="0a911-145">To disable archiving</span></span>

  - <span data-ttu-id="0a911-146">Чтобы вообще отключить архивацию, установите для свойств **ArchiveInternal** и **ArchiveExternal** значение false ($false).</span><span class="sxs-lookup"><span data-stu-id="0a911-146">To disable archiving altogether, set both the **ArchiveInternal** and **ArchiveExternal** properties to False ($False).</span></span> <span data-ttu-id="0a911-147">Например:</span><span class="sxs-lookup"><span data-stu-id="0a911-147">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

<span data-ttu-id="0a911-148">Дополнительные сведения можно найти в разделе справки по командлету [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="0a911-148">For more information, see the help topic for the [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0a911-149">См. также</span><span class="sxs-lookup"><span data-stu-id="0a911-149">See Also</span></span>


[<span data-ttu-id="0a911-150">Управление архивированием внутренней и внешней связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0a911-150">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="0a911-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a911-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

