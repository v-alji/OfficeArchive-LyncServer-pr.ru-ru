---
title: Настройка сценариев Lync Server 2013
description: Настройте сценарии Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Lync Server 2013 Scenarios
ms:assetid: 6705346b-1512-4af3-85e4-64dfa6ee6f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945596(v=OCS.15)
ms:contentKeyID: 51541420
ms.date: 12/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4a5b7bd271191067779ac358807cc54918b16bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440075"
---
# <a name="configure-lync-server-2013-scenarios"></a><span data-ttu-id="967f3-103">Настройка сценариев Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="967f3-103">Configure Lync Server 2013 Scenarios</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="967f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="967f3-104">

<span> </span></span></span>

<span data-ttu-id="967f3-105">_**Тема последнего изменения:** 2016-12-28_</span><span class="sxs-lookup"><span data-stu-id="967f3-105">_**Topic Last Modified:** 2016-12-28_</span></span>

<span data-ttu-id="967f3-106">Для запуска средства нагрузки и производительности Lync Server 2013 (LyncPerfTool) необходимо сначала настроить топологию Lync Server 2013 для сценариев, которые будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="967f3-106">To run the Lync Server 2013 Stress and Performance Tool (LyncPerfTool), the Lync Server 2013 topology must first be configured for the scenarios that will be executed.</span></span> <span data-ttu-id="967f3-107">Если Lync Server 2013 не настроен или настроен неправильно, в большинстве случаев происходит сбой нагрузочного моделирования.</span><span class="sxs-lookup"><span data-stu-id="967f3-107">If Lync Server 2013 is not configured or is configured incorrectly, load simulation will fail in most cases.</span></span> <span data-ttu-id="967f3-108">С помощью средства нагрузки и производительности Lync Server 2013 мы предоставили примеры сценариев командной консоли Lync Server Management Shell и базовых файлов ресурсов, которые можно использовать в качестве отправной точки для настройки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="967f3-108">With the Lync Server 2013 Stress and Performance Tool, we have provided example Lync Server Management Shell scripts and basic resource files that can be used as a starting point for configuring Lync Server 2013.</span></span> <span data-ttu-id="967f3-109">В этом разделе описаны указанные примеры Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="967f3-109">This topic describes the Windows PowerShell examples provided.</span></span> <span data-ttu-id="967f3-110">Обратите внимание, что этот раздел не предназначен для того, чтобы описать, как настроить Lync Server 2013 в целом.</span><span class="sxs-lookup"><span data-stu-id="967f3-110">Note that it is not the goal of this topic to describe how to configure Lync Server 2013 in general.</span></span> <span data-ttu-id="967f3-111">Подробные сведения о работе с Windows PowerShell в Lync Server 2013 можно найти в документации по оболочке Lync Server Management Shell по адресу <https://technet.microsoft.com/library/gg398474.aspx> .</span><span class="sxs-lookup"><span data-stu-id="967f3-111">For details about working with Windows PowerShell in Lync Server 2013, see the Lync Server Management Shell documentation at <https://technet.microsoft.com/library/gg398474.aspx>.</span></span>

<div>

## <a name="about-running-lync-server-management-shell-scripts"></a><span data-ttu-id="967f3-112">Сведения о выполнении сценариев оболочки Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="967f3-112">About Running Lync Server Management Shell Scripts</span></span>

<span data-ttu-id="967f3-113">Мы предоставили примеры сценариев командной консоли Lync Server, которые можно использовать для подготовки к запуску моделирования нагрузки.</span><span class="sxs-lookup"><span data-stu-id="967f3-113">We have provided example Lync Server Management Shell scripts that may be used in preparation for running load simulation.</span></span> <span data-ttu-id="967f3-114">Так как сценарии предназначены для моделирования нагрузки, они являются простыми и разрешительнои и, следовательно, могут быть не подходящими к производству.</span><span class="sxs-lookup"><span data-stu-id="967f3-114">Because the scripts are intended for load simulation, they are simple and permissive, and therefore may not be appropriate for production.</span></span> <span data-ttu-id="967f3-115">Все сценарии являются примерами и должны быть проверены, а в некоторых случаях — в соответствии с вашей топологией.</span><span class="sxs-lookup"><span data-stu-id="967f3-115">All scripts are examples and must be reviewed, and, in some cases, modified to reflect your topology.</span></span> <span data-ttu-id="967f3-116">Как минимум, мы ожидаем, что сценарий службы группы ответа потребуется изменить, чтобы указать агенты, назначенные группам агента.</span><span class="sxs-lookup"><span data-stu-id="967f3-116">At a minimum, we expect that the Response Group Service (RGS) scenario would need to be modified to specify the agents that are assigned to the agent groups.</span></span> <span data-ttu-id="967f3-117">Однако у вас есть возможность не моделировать эту загрузку.</span><span class="sxs-lookup"><span data-stu-id="967f3-117">However, you have the option to not simulate this load.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="967f3-118">Будьте внимательны и позаботьтесь о том, как ознакомиться с приведенными примерами.</span><span class="sxs-lookup"><span data-stu-id="967f3-118">Take care in reviewing and understanding the examples provided.</span></span> <span data-ttu-id="967f3-119">Сценарии будут переопределять любые существующие параметры в топологии.</span><span class="sxs-lookup"><span data-stu-id="967f3-119">Scripts will overwrite any existing settings in the topology.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="967f3-120">Подробнее об использовании Windows PowerShell и командной консоли Lync Server можно найти в блоге Lync Server 2013 Windows PowerShell по адресу <A href="https://go.microsoft.com/fwlink/?linkid=203150">https://go.microsoft.com/fwlink/?LinkId=203150</A> .</span><span class="sxs-lookup"><span data-stu-id="967f3-120">For details about using Windows PowerShell and the Lync Server Management Shell, see the Lync Server 2013 Windows PowerShell Blog at <A href="https://go.microsoft.com/fwlink/?linkid=203150">https://go.microsoft.com/fwlink/?LinkId=203150</A>.</span></span>



</div>

</div>

<div>

## <a name="stress-and-performance-tool-client-version-monikers"></a><span data-ttu-id="967f3-121">Специальные имена в клиентской программе для средства нагрузки и производительности</span><span class="sxs-lookup"><span data-stu-id="967f3-121">Stress and Performance Tool Client Version Monikers</span></span>

<span data-ttu-id="967f3-122">Если вы изменили настройки из значений по умолчанию, вам может потребоваться настроить политику проверки версии клиента.</span><span class="sxs-lookup"><span data-stu-id="967f3-122">You may need to configure the Client Version Check policy if you have changed the settings from the default values.</span></span> <span data-ttu-id="967f3-123">Подробные сведения можно найти в разделе "Настройка поддерживаемых клиентских версий" <https://technet.microsoft.com/library/gg412832(v=ocs.15).aspx> .</span><span class="sxs-lookup"><span data-stu-id="967f3-123">For details, see “Configuring supported client versions” at <https://technet.microsoft.com/library/gg412832(v=ocs.15).aspx>.</span></span> <span data-ttu-id="967f3-124">При общении с Lync Server 2013 средство "стресс и производительность" Lync Server 2013 по умолчанию использует следующие версии агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="967f3-124">The Lync Server 2013 Stress and Performance Tool uses the following User Agent Versions by default when communicating with Lync Server 2013:</span></span>

  - <span data-ttu-id="967f3-125">LSPT/15.0.0.0 (средство для Lync Server 2013 с функцией нагрузки и производительности)</span><span class="sxs-lookup"><span data-stu-id="967f3-125">LSPT/15.0.0.0 (Lync Server 2013 Stress and Performance Tool)</span></span>

  - <span data-ttu-id="967f3-126">OCPHONE/.0.522</span><span class="sxs-lookup"><span data-stu-id="967f3-126">OCPHONE/.0.522</span></span>

<span data-ttu-id="967f3-127">Они предназначены для клиента Mobility (UCWA) в LyncPerfTool:</span><span class="sxs-lookup"><span data-stu-id="967f3-127">These are for the Mobility (UCWA) client in LyncPerfTool:</span></span>

  - <span data-ttu-id="967f3-128">Средство для Ucwa производительности и веб-конференции</span><span class="sxs-lookup"><span data-stu-id="967f3-128">Ucwa Perf Tool/Web Conference</span></span>

  - <span data-ttu-id="967f3-129">Средство для Ucwa производительности и мобильные телефоны</span><span class="sxs-lookup"><span data-stu-id="967f3-129">Ucwa Perf Tool/Mobile</span></span>

<span data-ttu-id="967f3-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="967f3-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

