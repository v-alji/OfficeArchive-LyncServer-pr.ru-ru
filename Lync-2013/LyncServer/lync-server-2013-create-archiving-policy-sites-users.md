---
title: 'Lync Server 2013: Создание политики архивации для включения и отключения архивации внутренних или внешних сообщений определенных сайтов и пользователей'
description: 'Lync Server 2013: Создание политики архивации, позволяющей включать и отключать внутренние или внешние коммуникации для определенных сайтов или пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431990"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a><span data-ttu-id="ea275-103">Создание политики архивации в Lync Server 2013 для включения и отключения архивации внутренних или внешних сообщений определенных сайтов и пользователей</span><span class="sxs-lookup"><span data-stu-id="ea275-103">Creating an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for specific sites or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea275-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea275-104">

<span> </span></span></span>

<span data-ttu-id="ea275-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ea275-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ea275-106">В Lync Server 2013 вы используете политики для включения и отключения архивирования для внутренних коммуникаций и внешней связи для пользователей, размещенных на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ea275-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="ea275-107">К ним относятся следующие политики архивации:</span><span class="sxs-lookup"><span data-stu-id="ea275-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="ea275-108">Глобальная политика, созданная по умолчанию при развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ea275-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="ea275-109">Необязательные политики уровня сайта и уровня пользователя, которые можно создавать и использовать для определения способа реализации архивации для конкретных сайтов или пользователей.</span><span class="sxs-lookup"><span data-stu-id="ea275-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="ea275-110">Изначально политики архивации были настроены при развертывании архивации, но вы можете изменить, добавить и удалить политики после развертывания.</span><span class="sxs-lookup"><span data-stu-id="ea275-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="ea275-111">В панели управления Lync Server 2013 вы можете управлять политиками на глобальном уровне, уровне сайта и на уровне пользователей с помощью страницы **политики архивации** в группе **Архивация и мониторинг** .</span><span class="sxs-lookup"><span data-stu-id="ea275-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="ea275-112">Если вы интегрирует хранилище Lync Server с хранилищем Exchange 2013, политики пользователей Exchange имеют приоритет над политиками архивации Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ea275-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="ea275-113">Сведения о том, как реализованы политики, в том числе об иерархии политик, описаны [в разделе Работа с архивацией в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="ea275-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="ea275-114">Чтобы управлять реализацией архивации, необходимо указать параметры в конфигурациях архивации, например, следует ли архивировать сообщения или конференции, использовать критический режим и параметры очистки.</span><span class="sxs-lookup"><span data-stu-id="ea275-114">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="ea275-115">По умолчанию параметры не включены в глобальной конфигурации архивации или конфигурации архивации сайта или пула.</span><span class="sxs-lookup"><span data-stu-id="ea275-115">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="ea275-116">Прежде чем включать архивирование для внутренних или внешних сообщений в политиках архивации, необходимо задать все соответствующие параметры в параметрах конфигурации архивации.</span><span class="sxs-lookup"><span data-stu-id="ea275-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="ea275-117">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Управление параметрами конфигурации архивации в Lync Server 2013 для Организации, сайты и пулы</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="ea275-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="ea275-118">Если вы включили интеграцию Microsoft Exchange для развертывания, политики Exchange определяют, включено ли архивирование для пользователей, использующих Exchange 2013, и почтовые ящики помещаются на In-Place удержание.</span><span class="sxs-lookup"><span data-stu-id="ea275-118">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="ea275-119">Подробности можно найти в разделе <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Настройка политик архивации в Lync server 2013 при использовании интеграции с Exchange Server</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="ea275-119">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a><span data-ttu-id="ea275-120">Создание политики архивации для сайта или пользователей</span><span class="sxs-lookup"><span data-stu-id="ea275-120">To create an archiving policy for a site or users</span></span>

1.  <span data-ttu-id="ea275-121">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ea275-121">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ea275-122">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ea275-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ea275-123">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ea275-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ea275-124">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Политика архивации**.</span><span class="sxs-lookup"><span data-stu-id="ea275-124">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="ea275-125">Нажмите кнопку **Создать**, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="ea275-125">Click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="ea275-126">Чтобы создать политику архивации на уровне сайта, нажмите кнопку **Политика сайта** , а затем в списке **выберите сайт** выберите сайт, к которому нужно применить политику.</span><span class="sxs-lookup"><span data-stu-id="ea275-126">To create a site-level archiving policy, click **Site policy** and then, in **Select a site**, click the site to which the policy is to be applied.</span></span>
    
      - <span data-ttu-id="ea275-127">Чтобы создать политику архивации на уровне пользователя, щелкните **Политика пользователя**.</span><span class="sxs-lookup"><span data-stu-id="ea275-127">To create a user-level archiving policy, click **User policy**.</span></span>

5.  <span data-ttu-id="ea275-128">В области **Создать политику архивации** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ea275-128">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="ea275-129">В разделе **Имя** укажите имя новой политики (например, externalContoso).</span><span class="sxs-lookup"><span data-stu-id="ea275-129">In **Name**, specify a name for the new policy (for example, externalContoso).</span></span>
    
      - <span data-ttu-id="ea275-130">В разделе **Описание** приведите подробные сведения о том, что представляет собой политика (например, внешняя политика архивации на уровне пользователя для компании Contoso).</span><span class="sxs-lookup"><span data-stu-id="ea275-130">In **Description**, provide details about what the policy is (for example, External user archiving policy for Contoso).</span></span>
    
      - <span data-ttu-id="ea275-131">Для управления архивацией операций обмена данными с внутренними пользователями установите или снимите флажок **Архивация внутренних взаимодействий**.</span><span class="sxs-lookup"><span data-stu-id="ea275-131">To control archiving of communications with internal users, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="ea275-132">Для управления архивацией операций обмена данными с внешними пользователями установите или снимите флажок **Архивация внешних взаимодействий**.</span><span class="sxs-lookup"><span data-stu-id="ea275-132">To control archiving of communications with external users, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="ea275-133">Щелкните **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="ea275-133">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="ea275-134">Параметры политики пользователя применяются только к тем пользователям и группам пользователей, к которым применяется политика.</span><span class="sxs-lookup"><span data-stu-id="ea275-134">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="ea275-135">Подробнее смотрите в разделе <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">применение политики архивации для пользователей в Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="ea275-135">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ea275-136">Создание политики архивации с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ea275-136">Creating an Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ea275-137">Политики архивации можно создать с помощью Windows PowerShell и командлета **Remove-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="ea275-137">Archiving policies can be created by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="ea275-138">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea275-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ea275-139">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ea275-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a><span data-ttu-id="ea275-140">Создание новой политики архивации в области сайта</span><span class="sxs-lookup"><span data-stu-id="ea275-140">To create a new archiving policy at the site scope</span></span>

  - <span data-ttu-id="ea275-141">Данная команда создает новую политику архивации для сайта Redmond:</span><span class="sxs-lookup"><span data-stu-id="ea275-141">This command creates a new archiving policy for the Redmond site:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a><span data-ttu-id="ea275-142">Создание новой политики архивации в области "на пользователя"</span><span class="sxs-lookup"><span data-stu-id="ea275-142">To create a new archiving policy at the per-user scope</span></span>

  - <span data-ttu-id="ea275-143">Чтобы создать новую политику архивации в области "на пользователя", просто укажите уникальный идентификатор при создании политики.</span><span class="sxs-lookup"><span data-stu-id="ea275-143">To create a new archiving policy at the per-user scope, simply specify a unique Identity when creating the policy:</span></span>
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a><span data-ttu-id="ea275-144">Порядок создания новой политики архивации, которая включает архивацию сеансов внутренней связи</span><span class="sxs-lookup"><span data-stu-id="ea275-144">To create a new archiving policy that enables archiving of internal communication sessions</span></span>

  - <span data-ttu-id="ea275-145">Так как никакие параметры (кроме обязательного параметра Identity) не были указаны в приведенных ранее командах, новые политики будут использовать значения по умолчанию для всех своих свойств.</span><span class="sxs-lookup"><span data-stu-id="ea275-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding commands, the new policies will use the default values for all their properties.</span></span> <span data-ttu-id="ea275-146">Чтобы создать политики, использующие другие значения свойств, просто включите соответствующий параметр и его значение.</span><span class="sxs-lookup"><span data-stu-id="ea275-146">To create policies that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="ea275-147">Например, чтобы создать политику архивации, разрешающую архивирование внутренних сеансов обмена мгновенными сообщениями, выполните указанные ниже команды.</span><span class="sxs-lookup"><span data-stu-id="ea275-147">For example, to create an archiving policy that permits archiving of internal instant messaging sessions use a command like this:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="ea275-148">Порядок создания новой политики архивации, которая включает архивацию сеансов внутренней и внешней связи</span><span class="sxs-lookup"><span data-stu-id="ea275-148">To create a new archiving policy that enables archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="ea275-149">Несколько значений свойств могут быть изменены путем включения нескольких параметров.</span><span class="sxs-lookup"><span data-stu-id="ea275-149">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="ea275-150">Например, эта команда настраивает новую политику для архивации как внутренних, так и внешних сеансов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ea275-150">For example, this command configures the new policy to archiving both internal and external instant messaging sessions:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

<span data-ttu-id="ea275-151">Дополнительные сведения можно найти в разделе справки по командлету [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="ea275-151">For more information, see the help topic for the [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ea275-152">См. также</span><span class="sxs-lookup"><span data-stu-id="ea275-152">See Also</span></span>


[<span data-ttu-id="ea275-153">Управление архивированием внутренней и внешней связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ea275-153">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="ea275-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea275-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

