---
title: 'Lync Server 2013: создание конфигурации архивации для управления архивированием для определенных сайтов или пулов'
description: 'Lync Server 2013: создание конфигурации архивации для управления архивированием для определенных сайтов или пулов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving configuration to manage Archiving for specific sites or pools
ms:assetid: c5c864a6-96c7-4bbb-ab7c-61eb1744246c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205251(v=OCS.15)
ms:contentKeyID: 48185361
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ab19f2d8900693ef0fcb14d8f6d862b22c355bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431535"
---
# <a name="creating-an-archiving-configuration-in-lync-server-2013-to-manage-archiving-for-specific-sites-or-pools"></a><span data-ttu-id="d1182-103">Создание конфигурации архивации в Lync Server 2013 для управления архивированием определенных сайтов и пулов</span><span class="sxs-lookup"><span data-stu-id="d1182-103">Creating an Archiving configuration in Lync Server 2013 to manage Archiving for specific sites or pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1182-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1182-104">

<span> </span></span></span>

<span data-ttu-id="d1182-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="d1182-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="d1182-106">В панели управления Lync Server 2013 вы можете управлять реализацией архивации в развертывании с помощью конфигураций архивации.</span><span class="sxs-lookup"><span data-stu-id="d1182-106">In Lync Server 2013 Control Panel, you use Archiving configurations to control how archiving is implemented in your deployment.</span></span> <span data-ttu-id="d1182-107">К ним относятся следующие конфигурации архивации:</span><span class="sxs-lookup"><span data-stu-id="d1182-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="d1182-108">Глобальная конфигурация, создаваемая по умолчанию при развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d1182-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="d1182-109">Необязательные конфигурации уровня сайта и пула, которые можно создать и использовать для определения способа реализации архивации для конкретных сайтов или пулов.</span><span class="sxs-lookup"><span data-stu-id="d1182-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="d1182-110">Первоначально конфигурации архивации задаются при развертывании архивации, но вы можете изменить, добавить и удалить настройки после развертывания.</span><span class="sxs-lookup"><span data-stu-id="d1182-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="d1182-111">Сведения о том, как работают конфигурации архивации, в том числе о параметрах, которые можно указать и в иерархии конфигураций архивации, описаны в разделе [Использование архивации в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="d1182-111">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d1182-112">Чтобы использовать архивацию, необходимо настроить политики архивации, чтобы указать, следует ли включать архивирование для внутренней связи, для внешней связи или для пользователей, расположенных на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d1182-112">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for users homed on Lync Server 2013.</span></span> <span data-ttu-id="d1182-113">По умолчанию архивация не включена для внутренней и внешней связи.</span><span class="sxs-lookup"><span data-stu-id="d1182-113">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="d1182-114">Перед включением архивации в любых политиках следует задать соответствующие конфигурации архивации для развертывания и (необязательно) для определенных сайтов и пулов, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d1182-114">Before enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="d1182-115">Подробнее о том, как включить архивацию, можно найти <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">в разделе Настройка и назначение политик архивации в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="d1182-115">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="d1182-116">Если вы решите после развертывания архивации, для которой вы хотите использовать интеграцию с Microsoft Exchange для хранения данных и файлов на серверах Exchange 2013, а все ваши пользователи находятся на серверах Exchange 2013, необходимо удалить конфигурацию базы данных SQL Server из топологии.</span><span class="sxs-lookup"><span data-stu-id="d1182-116">If you decide after you deploy Archiving that you want to use Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers and all your users are homed on your Exchange 2013 servers, you should remove the SQL Server database configuration from your topology.</span></span> <span data-ttu-id="d1182-117">Для этого необходимо использовать Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="d1182-117">You must use Topology Builder to do this.</span></span> <span data-ttu-id="d1182-118">Подробнее смотрите в разделе <A href="lync-server-2013-changing-archiving-database-options.md">изменение параметров базы данных для архивации в Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="d1182-118">For details, see <A href="lync-server-2013-changing-archiving-database-options.md">Changing Archiving database options in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-configuration-for-a-site-or-pool"></a><span data-ttu-id="d1182-119">Создание конфигурации архивации для сайта или пула</span><span class="sxs-lookup"><span data-stu-id="d1182-119">To create an archiving configuration for a site or pool</span></span>

1.  <span data-ttu-id="d1182-120">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d1182-120">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d1182-121">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1182-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d1182-122">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d1182-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d1182-123">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Конфигурация архивации**.</span><span class="sxs-lookup"><span data-stu-id="d1182-123">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="d1182-124">На странице **Конфигурация архивации** нажмите **Создать**, а затем выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="d1182-124">On the **Archiving Configuration** page, click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="d1182-125">Чтобы создать конфигурацию архивации сайта, нажмите кнопку **Конфигурация сайта** , а затем в списке **выберите сайт** выберите сайт, который нужно настроить для архивации.</span><span class="sxs-lookup"><span data-stu-id="d1182-125">To create a site archiving configuration, click **Site Configuration** and then, in **Select a site**, select the site to be configured for archiving.</span></span>
    
      - <span data-ttu-id="d1182-126">Чтобы создать конфигурацию архивации пула, нажмите кнопку **Конфигурация пула** , а затем в **группе Выбор пула** выберите пул, для которого нужно настроить архивирование.</span><span class="sxs-lookup"><span data-stu-id="d1182-126">To create a pool archiving configuration, click **Pool Configuration** and then, in **Select a pool**, select the pool to be configured for archiving.</span></span>

5.  <span data-ttu-id="d1182-127">В разделе **Создание новой настройки архивации** выберите в раскрывающемся списке **Настройки архивации** один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="d1182-127">In **New Archiving Setting**, in the **Archiving setting** drop-down list box, do one of the following:</span></span>
    
      - <span data-ttu-id="d1182-128">Чтобы включить архивирование только для сеансов обмена мгновенными сообщениями, нажмите **Архивировать сеансы мгновенных сообщений**.</span><span class="sxs-lookup"><span data-stu-id="d1182-128">To enable archiving only for instant messaging (IM) sessions, click **Archive IM sessions**.</span></span>
    
      - <span data-ttu-id="d1182-129">Чтобы включить архивирование для обмена мгновенными сообщениями и веб-конференций, нажмите элемент **Архивировать сеансы мгновенных сообщений и веб-конференций**.</span><span class="sxs-lookup"><span data-stu-id="d1182-129">To enable archiving for both IM sessions and web conferences, click **Archive IM and web conferencing sessions**.</span></span>
    
      - <span data-ttu-id="d1182-130">Если требуется запретить архивацию для данной политики, щелкните **Отключить архивацию**.</span><span class="sxs-lookup"><span data-stu-id="d1182-130">To disable archiving for the policy, click **Disable archiving**.</span></span>

6.  <span data-ttu-id="d1182-131">На странице **Создание новой настройки архивации** можно также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d1182-131">Also in **New Archiving Setting**, do the following:</span></span>
    
      - <span data-ttu-id="d1182-132">Для запрета действия при невозможности архивации установите флажок **При сбое архивации заблокировать обмен мгновенными сообщениями или сеансы веб-конференции**.</span><span class="sxs-lookup"><span data-stu-id="d1182-132">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="d1182-133">Чтобы использовать сервер Microsoft Exchange для хранения данных для архивации, установите флажок **интеграция Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="d1182-133">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="d1182-134">Для включения функции удаления данных установите флажок **Разрешить удаление данных архивации**, затем выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="d1182-134">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="d1182-135">Для настройки удаления записей по истечении заданного срока (в днях) щелкните **Очищать экспортированные данные архивации, а также данные архивации по окончании максимального срока хранения (дн.)**, затем укажите количество дней.</span><span class="sxs-lookup"><span data-stu-id="d1182-135">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="d1182-136">Для удаления только экспортированных данных выберите **Удалять только экспортированные данные архивации**.</span><span class="sxs-lookup"><span data-stu-id="d1182-136">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

7.  <span data-ttu-id="d1182-137">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="d1182-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-archiving-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d1182-138">Создание параметров конфигурации архивации с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1182-138">Creating Archiving Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d1182-139">Параметры конфигурации архивации можно создать с помощью Windows PowerShell и командлета New-CsArchivingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d1182-139">Archiving configuration settings can be created by using Windows PowerShell and the New-CsArchivingConfiguration cmdlet.</span></span> <span data-ttu-id="d1182-140">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d1182-140">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d1182-141">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d1182-141">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-archiving-configuration-settings-for-a-site"></a><span data-ttu-id="d1182-142">Создание новой коллекции параметров конфигурации архивации для сайта</span><span class="sxs-lookup"><span data-stu-id="d1182-142">To create a new collection of archiving configuration settings for a site</span></span>

  - <span data-ttu-id="d1182-143">Следующая команда создает новую коллекцию параметров конфигурации архивации для сайта Redmond:</span><span class="sxs-lookup"><span data-stu-id="d1182-143">The following command creates a new collection of archiving configuration settings for the Redmond site:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-collection-of-archiving-configuration-settings-that-only-allow-im-archiving"></a><span data-ttu-id="d1182-144">Создание нового набора параметров конфигурации архивации, разрешающего только архивирование мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="d1182-144">To create a new collection of archiving configuration settings that only allow IM archiving</span></span>

  - <span data-ttu-id="d1182-145">Поскольку в предыдущей команде не было указано никаких параметров, кроме обязательного параметра Identity, новая коллекция параметров конфигурации будет использовать значения по умолчанию для всех своих свойств.</span><span class="sxs-lookup"><span data-stu-id="d1182-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span> <span data-ttu-id="d1182-146">Чтобы создать параметры, использующие другие значения свойств, просто включите соответствующий параметр и его значение.</span><span class="sxs-lookup"><span data-stu-id="d1182-146">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="d1182-147">Например, чтобы создать коллекцию параметров конфигурации архивации, которые по умолчанию разрешают архивирование сеансов обмена мгновенными сообщениями, используйте такую команду:</span><span class="sxs-lookup"><span data-stu-id="d1182-147">For example, to create a collection of archiving configuration settings that, by default, allow archiving of instant messaging sessions, only use a command like this:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly"

</div>

<div>

## <a name="to-specify-multiple-property-values-when-creating-archiving-configuration-settings"></a><span data-ttu-id="d1182-148">Указание нескольких значений свойства при создании параметров конфигурации архивации</span><span class="sxs-lookup"><span data-stu-id="d1182-148">To specify multiple property values when creating archiving configuration settings</span></span>

  - <span data-ttu-id="d1182-p108">Чтобы изменить несколько значений свойств, можно включить несколько параметров. Например, следующая команда настраивает новые параметры для архивации сеансов обмена мгновенными сообщениями и для блокирования обмена мгновенными сообщениями при недоступности службы архивации:</span><span class="sxs-lookup"><span data-stu-id="d1182-p108">Multiple property values can be modified by including multiple parameters. For example, this command configures the new settings to archive instant messaging sessions and to block instant messaging of the archiving service is not available:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly" -BlockOnArchiveFailure $True

</div>

<span data-ttu-id="d1182-151">Дополнительные сведения можно найти в разделе справки по командлету [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="d1182-151">For more information, see the help topic for the [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d1182-152">См. также</span><span class="sxs-lookup"><span data-stu-id="d1182-152">See Also</span></span>


[<span data-ttu-id="d1182-153">Как работает архивация в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1182-153">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="d1182-154">Управление параметрами конфигурации архивации в Lync Server 2013 для Организации, сайтов и пулов</span><span class="sxs-lookup"><span data-stu-id="d1182-154">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

<span data-ttu-id="d1182-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1182-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

