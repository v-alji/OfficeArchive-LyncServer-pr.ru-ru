---
title: 'Lync Server 2013: Управление параметрами конфигурации архивации для Организации, сайтов и пулов'
description: 'Lync Server 2013: Управление параметрами конфигурации архивации для Организации, сайтов и пулов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Archiving configuration options for your organization, sites, and pools
ms:assetid: 377a6f80-5f2b-4bc1-b507-e930a461fb1d
ms:mtpsurl: https://technet.microsoft.com/library/JJ204802(v=OCS.15)
ms:contentKeyID: 48183830
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41eca448fcb9863f117bcb7e52e3290270fefa47
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425985"
---
# <a name="managing-archiving-configuration-options-in-lync-server-2013-for-your-organization-sites-and-pools"></a><span data-ttu-id="f7fbd-103">Управление параметрами конфигурации архивации в Lync Server 2013 для Организации, сайтов и пулов</span><span class="sxs-lookup"><span data-stu-id="f7fbd-103">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7fbd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7fbd-104">

<span> </span></span></span>

<span data-ttu-id="f7fbd-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f7fbd-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f7fbd-106">В панели управления Lync Server 2013 вы можете настроить способ реализации архивации с помощью конфигураций архивации.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-106">In Lync Server 2013 Control Panel, you use Archiving configurations to specify how archiving is implemented.</span></span> <span data-ttu-id="f7fbd-107">К ним относятся следующие конфигурации архивации:</span><span class="sxs-lookup"><span data-stu-id="f7fbd-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="f7fbd-108">Глобальная конфигурация, создаваемая по умолчанию при развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="f7fbd-109">Необязательные конфигурации уровня сайта и пула, которые можно создать и использовать для определения способа реализации архивации для конкретных сайтов или пулов.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="f7fbd-110">Первоначально конфигурации архивации задаются при развертывании архивации, но вы можете изменить, добавить и удалить настройки после развертывания.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="f7fbd-111">В панели управления Lync Server 2013 можно использовать страницу **Конфигурация архивации** в группе **Архивация и мониторинг** для управления конфигурациями на глобальном уровне, уровне сайта и уровне пула.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-111">In Lync Server 2013 Control Panel, you can use the **Archiving Configuration** page of the **Archiving and Monitoring** group to manage configurations at the global level, site level, and pool level.</span></span> <span data-ttu-id="f7fbd-112">Сведения о том, как работают конфигурации архивации, в том числе о том, какие параметры вы можете указать, а также о иерархии конфигураций архивации, описаны в разделе [Использование архивации в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-112">For details about how Archiving configurations are implemented, including which options you can specify, and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7fbd-113">Чтобы использовать архивацию, необходимо настроить политики архивации, чтобы указать, следует ли включать архивирование для внутренней связи, для внешней связи или для всех пользователей, расположенных на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-113">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for all users homed on Lync Server 2013.</span></span> <span data-ttu-id="f7fbd-114">По умолчанию архивация не включена для внутренней и внешней связи.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-114">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="f7fbd-115">Если вы используете Microsoft Exchange Integration, вы должны включить и настроить Exchange 2013 для поддержки архивирования для всех пользователей, размещенных на сервере Exchange 2013, чьи почтовые ящики помещаются на In-Place удержание.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-115">If you use Microsoft Exchange integration, you must enable and configure Exchange 2013 to support archiving for all users homed on Exchange 2013 who have had their mailboxes put on In-Place Hold.</span></span><BR><span data-ttu-id="f7fbd-116">Перед включением архивации следует задать соответствующие конфигурации архивации для развертывания и, при необходимости, для определенных сайтов и пулов, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-116">Prior to enabling Archiving, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="f7fbd-117">Подробнее о том, как включить архивацию, можно найти <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">в разделе Настройка и назначение политик архивации в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-117">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="f7fbd-118">**Просмотр сведений о конфигурации архивации с помощью командлетов Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="f7fbd-118">**To view archiving configuration information by using Windows PowerShell cmdlets**</span></span>

  - <span data-ttu-id="f7fbd-119">Вы можете просматривать сведения о конфигурации архивации с помощью Windows PowerShell и командлета **Get-CsArchivingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f7fbd-119">You can view Archiving configuration information by using Windows PowerShell and the **Get-CsArchivingConfiguration** cmdlet.</span></span> <span data-ttu-id="f7fbd-120">Этот командлет можно выполнить либо из командной консоли Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-120">You can run this cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f7fbd-121">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="f7fbd-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="f7fbd-122">В командной консоли Lync Server выполните следующую команду, чтобы просмотреть сведения о всех параметрах конфигурации архивирования.</span><span class="sxs-lookup"><span data-stu-id="f7fbd-122">In the Lync Server Management Shell, use the following command to view information about all of your archiving configuration settings:</span></span>
    
        Get-CsArchivingConfiguration

<div>

## <a name="in-this-section"></a><span data-ttu-id="f7fbd-123">Содержание</span><span class="sxs-lookup"><span data-stu-id="f7fbd-123">In This Section</span></span>

  - [<span data-ttu-id="f7fbd-124">Создание конфигурации архивации в Lync Server 2013 для управления архивированием определенных сайтов и пулов</span><span class="sxs-lookup"><span data-stu-id="f7fbd-124">Creating an Archiving configuration in Lync Server 2013 to manage Archiving for specific sites or pools</span></span>](lync-server-2013-creating-an-archiving-configuration-to-manage-archiving-for-specific-sites-or-pools.md)

  - [<span data-ttu-id="f7fbd-125">Включение и отключение архивирования сеансов обмена мгновенными сообщениями и конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7fbd-125">Enabling or disabling Archiving of IM or conferencing sessions in Lync Server 2013</span></span>](lync-server-2013-enabling-or-disabling-archiving-of-im-or-conferencing-sessions.md)

  - [<span data-ttu-id="f7fbd-126">Включение и отключение очистки архивированных данных в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7fbd-126">Enabling or disabling the purging of archived data in Lync Server 2013</span></span>](lync-server-2013-enabling-or-disabling-the-purging-of-archived-data.md)

  - [<span data-ttu-id="f7fbd-127">Включение и отключение критического режима в Lync Server 2013 для блокирования и разрешения сеансов обмена мгновенными сообщениями и веб-конференций в случае сбоя архивации</span><span class="sxs-lookup"><span data-stu-id="f7fbd-127">Enabling or disabling critical mode in Lync Server 2013 to block or allow IM and web conferencing sessions if Archiving fails</span></span>](lync-server-2013-enable-disable-critical-mode.md)

  - [<span data-ttu-id="f7fbd-128">Включение и отключение отправки отказа от архивирования федеративным партнерам в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7fbd-128">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

  - [<span data-ttu-id="f7fbd-129">Включение и отключение интеграции Lync Server 2013 с хранилищем Exchange</span><span class="sxs-lookup"><span data-stu-id="f7fbd-129">Enabling or disabling integration of Lync Server 2013 with Exchange storage</span></span>](lync-server-2013-enabling-or-disabling-integration-with-exchange-storage.md)

  - [<span data-ttu-id="f7fbd-130">Удаление конфигурации архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7fbd-130">Deleting an Archiving configuration in Lync Server 2013</span></span>](lync-server-2013-deleting-an-archiving-configuration.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f7fbd-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f7fbd-131">See Also</span></span>


[<span data-ttu-id="f7fbd-132">Управление архивированием Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7fbd-132">Managing Lync Server 2013 Archiving</span></span>](lync-server-2013-managing-archiving.md)  
  

<span data-ttu-id="f7fbd-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7fbd-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

