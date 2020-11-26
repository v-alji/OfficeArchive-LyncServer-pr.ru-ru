---
title: 'Lync Server 2013: Настройка параметров архивации на глобальном уровне'
description: 'Lync Server 2013: Настройка параметров архивации на глобальном уровне.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options at the global level
ms:assetid: bfe415f7-2abf-41ee-a1cb-cf48b2d59c0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205233(v=OCS.15)
ms:contentKeyID: 48185303
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44b8939ec95d00afa2aa7632f4555bc6fef89834
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433341"
---
# <a name="configuring-archiving-options-at-the-global-level-in-lync-server-2013"></a><span data-ttu-id="b1b62-103">Настройка параметров архивации на глобальном уровне в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b62-103">Configuring Archiving options at the global level in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1b62-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1b62-104">

<span> </span></span></span>

<span data-ttu-id="b1b62-105">_**Тема последнего изменения:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="b1b62-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="b1b62-106">При добавлении архивации в топологию и публикации топологии сервер Lync Server создает глобальную конфигурацию для архивирования.</span><span class="sxs-lookup"><span data-stu-id="b1b62-106">When you add Archiving to your topology and publish the topology, Lync Server creates a global configuration for Archiving.</span></span> <span data-ttu-id="b1b62-107">По умолчанию в глобальной конфигурации не включены параметры архивирования.</span><span class="sxs-lookup"><span data-stu-id="b1b62-107">By default, no Archiving options are enabled in the global configuration.</span></span> <span data-ttu-id="b1b62-108">Глобальная конфигурация определяет параметры, включенные для развертывания в целом, если не заданы конфигурации на уровне сайта или пула, переопределяющие глобальную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b1b62-108">The global configuration controls which options are enabled for your entire deployment, unless you set up site or pool configurations, which override the global configuration.</span></span>

<span data-ttu-id="b1b62-109">Подробнее о том, как работают конфигурации архивации, включая иерархию конфигураций Global, site и pool, вы узнаете, [как работает архивация в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="b1b62-109">For details about how Archiving configurations work, including the hierarchy for global, site, and pool configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b1b62-110">Перед включением архивации необходимо указать все соответствующие параметры в разделе конфигурации архивации.</span><span class="sxs-lookup"><span data-stu-id="b1b62-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span>



</div>

<div>

## <a name="to-configure-archiving-options-at-the-global-level"></a><span data-ttu-id="b1b62-111">Настройка параметров архивации на глобальном уровне</span><span class="sxs-lookup"><span data-stu-id="b1b62-111">To configure archiving options at the global level</span></span>

1.  <span data-ttu-id="b1b62-112">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="b1b62-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b1b62-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b1b62-113">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="b1b62-114">Дополнительные сведения о различных способах запуска панели управления Lync Server 2013 можно найти в разделе [Открытие средства администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b1b62-114">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b1b62-115">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Конфигурация архивации**.</span><span class="sxs-lookup"><span data-stu-id="b1b62-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="b1b62-116">На странице **Конфигурация архивации** щелкните **Глобальная** и **Изменить**, затем **Показать сведения**.</span><span class="sxs-lookup"><span data-stu-id="b1b62-116">On the **Archiving Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="b1b62-117">В разделе **Изменение настройки архивации — глобальная** выберите в раскрывающемся списке **Настройки архивации** один из следующих параметров архивации.</span><span class="sxs-lookup"><span data-stu-id="b1b62-117">In **Edit Archiving Setting - Global**, in the **Archiving setting** drop-down list, select one of the following archiving options:</span></span>
    
      - <span data-ttu-id="b1b62-118">**Отключить архивацию**</span><span class="sxs-lookup"><span data-stu-id="b1b62-118">**Disable archiving**</span></span>
    
      - <span data-ttu-id="b1b62-119">**Архивировать сеансы мгновенных сообщений**</span><span class="sxs-lookup"><span data-stu-id="b1b62-119">**Archive IM sessions**</span></span>
    
      - <span data-ttu-id="b1b62-120">**Архивировать сеансы мгновенных сообщений и веб-конференций**</span><span class="sxs-lookup"><span data-stu-id="b1b62-120">**Archive IM and web conferencing sessions**</span></span>

6.  <span data-ttu-id="b1b62-121">На странице **Изменение настройки архивации — глобальная** можно также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b1b62-121">Also on the **Edit Archiving Setting – Global** page, do the following:</span></span>
    
      - <span data-ttu-id="b1b62-122">Для запрета действия при невозможности архивации установите флажок **При сбое архивации заблокировать обмен мгновенными сообщениями или сеансы веб-конференции**.</span><span class="sxs-lookup"><span data-stu-id="b1b62-122">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="b1b62-123">Чтобы использовать сервер Microsoft Exchange для хранения данных для архивации, установите флажок **интеграция Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="b1b62-123">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="b1b62-124">Для включения функции удаления данных установите флажок **Разрешить удаление данных архивации**, затем выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="b1b62-124">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="b1b62-125">Для настройки удаления записей по истечении заданного срока (в днях) щелкните **Очищать экспортированные данные архивации, а также данные архивации по окончании максимального срока хранения (дн.)**, затем укажите количество дней.</span><span class="sxs-lookup"><span data-stu-id="b1b62-125">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="b1b62-126">Для удаления только экспортированных данных выберите **Удалять только экспортированные данные архивации**.</span><span class="sxs-lookup"><span data-stu-id="b1b62-126">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

7.  <span data-ttu-id="b1b62-127">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="b1b62-127">Click **Commit**.</span></span>

<span data-ttu-id="b1b62-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1b62-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

