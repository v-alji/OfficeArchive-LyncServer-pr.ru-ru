---
title: 'Lync Server 2013: Настройка параметров архивации для сайта'
description: 'Lync Server 2013: Настройка параметров архивирования для сайта.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options for a site
ms:assetid: 59b48fd9-d5fc-40b4-abae-e9cf89ee5573
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204930(v=OCS.15)
ms:contentKeyID: 48184247
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2db164d7c4c1cdda158387be62c0eb535fac662f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433334"
---
# <a name="configuring-archiving-options-for-a-site-in-lync-server-2013"></a><span data-ttu-id="3bfb7-103">Настройка параметров архивации для сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bfb7-103">Configuring Archiving options for a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3bfb7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3bfb7-104">

<span> </span></span></span>

<span data-ttu-id="3bfb7-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="3bfb7-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="3bfb7-106">Вы можете указать параметры архивации для определенных сайтов, создав и настроив параметры конфигурации архивации для каждого из этих сайтов.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-106">You can specify Archiving options to be applied to specific sites by creating and configuring options in an Archiving configuration for each of those sites.</span></span> <span data-ttu-id="3bfb7-107">Конфигурация сайта переопределяет глобальную конфигурацию, но только для сайта, указанного в конфигурации сайта.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-107">A site configuration overrides the global configuration, but only for the site specified in the site configuration.</span></span> <span data-ttu-id="3bfb7-108">Конфигурации пулов. Переопределение конфигураций сайтов</span><span class="sxs-lookup"><span data-stu-id="3bfb7-108">Pool configurations override site configurations</span></span>

<span data-ttu-id="3bfb7-109">Подробнее о том, как работают конфигурации архивации, включая иерархию конфигураций Global, site и pool, вы узнаете, [как работает архивация в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-109">For details about how Archiving configurations work, including the hierarchy for global, site, and pool configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3bfb7-110">Перед включением архивации необходимо указать все соответствующие параметры в разделе конфигурации архивации.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3bfb7-111">Для активации архивации необходимо сначала указать политики архивации для управления архивацией внутренних и внешних взаимодействий на глобальном уровне и при необходимости на уровне сайтов и пользователей.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-111">To enable archiving, you must specify archiving policies to control the archiving of internal and external communications at the global level and, if appropriate, at site and user levels.</span></span> <span data-ttu-id="3bfb7-112">При настройке политик на уровне пользователей необходимо также назначить пользовательские политики определенным пользователям.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-112">If you configure user-level policies, you must also assign the user policies to specific users.</span></span> <span data-ttu-id="3bfb7-113">Дополнительные сведения о создании и настройке политик архивации можно найти в разделе <A href="lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md">Управление архивацией внутренней и внешней связи в Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-113">For details about creating and configuring archiving policies, see <A href="lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md">Managing the Archiving of internal and external communications in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-configure-archiving-options-at-the-site-level"></a><span data-ttu-id="3bfb7-114">Настройка параметров архивации на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="3bfb7-114">To configure archiving options at the site level</span></span>

1.  <span data-ttu-id="3bfb7-115">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-115">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3bfb7-116">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-116">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="3bfb7-117">Дополнительные сведения о различных способах запуска панели управления Lync Server 2013 можно найти в разделе [Открытие средства администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3bfb7-117">For details about the different methods you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3bfb7-118">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Конфигурация архивации**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-118">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="3bfb7-119">На странице **Конфигурация архивации** нажмите кнопку **Создать**, затем выберите **Конфигурация сайта**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-119">On the **Archiving Configuration** page, click **New**, and then click **Site Configuration**.</span></span>

5.  <span data-ttu-id="3bfb7-120">В разделе **Выбор службы** выберите сайт для настройки архивации.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-120">In **Select a Site**, select the site to be configured for archiving.</span></span>

6.  <span data-ttu-id="3bfb7-121">В разделе **Создание новой настройки архивации** выберите в раскрывающемся списке **Настройки архивации** один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-121">In **New Archiving Setting**, in the **Archiving setting** drop-down list box, do one of the following:</span></span>
    
      - <span data-ttu-id="3bfb7-122">Если требуется разрешить архивацию только для сеансов обмена мгновенными сообщениями, щелкните **Архивировать сеансы мгновенных сообщений**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-122">To enable archiving only for instant messaging (IM) sessions, click **Archive IM sessions**.</span></span>
    
      - <span data-ttu-id="3bfb7-123">Если требуется разрешить архивацию как для сеансов обмена мгновенными сообщениями, как и для конференц-связи, щелкните **Архивировать сеансы мгновенных сообщений и веб-конференций**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-123">To enable archiving for both IM sessions and conferences, click **Archive IM and web conferencing sessions**.</span></span>
    
      - <span data-ttu-id="3bfb7-124">Если требуется запретить архивацию для данной политики, щелкните **Отключить архивацию**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-124">To disable archiving for the policy, click **Disable archiving**.</span></span>

7.  <span data-ttu-id="3bfb7-125">На странице **Создание новой настройки архивации** можно также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-125">Also in **New Archiving Setting**, do the following:</span></span>
    
      - <span data-ttu-id="3bfb7-126">Для запрета действия при невозможности архивации установите флажок **При сбое архивации заблокировать обмен мгновенными сообщениями или сеансы веб-конференции**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-126">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="3bfb7-127">Чтобы использовать сервер Microsoft Exchange для хранения данных для архивации, установите флажок **интеграция Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="3bfb7-127">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="3bfb7-128">Для включения функции удаления данных установите флажок **Разрешить удаление данных архивации**, затем выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-128">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="3bfb7-129">Для настройки удаления записей по истечении заданного срока (в днях) щелкните **Очищать экспортированные данные архивации, а также данные архивации по окончании максимального срока хранения (дн.)**, затем укажите количество дней.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-129">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="3bfb7-130">Для удаления только экспортированных данных выберите **Удалять только экспортированные данные архивации**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-130">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

8.  <span data-ttu-id="3bfb7-131">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="3bfb7-131">Click **Commit**.</span></span>

<span data-ttu-id="3bfb7-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3bfb7-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

