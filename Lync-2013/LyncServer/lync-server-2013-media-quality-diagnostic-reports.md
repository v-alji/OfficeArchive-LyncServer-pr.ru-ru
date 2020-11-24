---
title: 'Lync Server 2013: отчеты диагностики качества мультимедиа'
description: 'Lync Server 2013: отчеты диагностики качества мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Diagnostic Reports
ms:assetid: ea61428e-a1d5-4189-aae6-3db19ddc5cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615044(v=OCS.15)
ms:contentKeyID: 48185935
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2e346d0f9b8997158cb926ad830d5477950e846d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400015"
---
# <a name="media-quality-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="25e97-103">Отчеты диагностики качества мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25e97-103">Media Quality Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25e97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25e97-104">

<span> </span></span></span>

<span data-ttu-id="25e97-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="25e97-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="25e97-106">Диагностический отчет по качеству мультимедиа предоставляет сведения о качестве вызовов, а также диагностические сведения для неудачных вызовов.</span><span class="sxs-lookup"><span data-stu-id="25e97-106">The Media Quality Diagnostic Reports provide information about call quality, and diagnostic and troubleshooting information for failed calls.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="25e97-107">Содержание</span><span class="sxs-lookup"><span data-stu-id="25e97-107">In This Section</span></span>

  - <span data-ttu-id="25e97-108">[Сводный отчет о качестве качества мультимедиа в Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Обеспечивает общие данные по качеству для разных типов конечных точек, в том числе одноранговых звонков для корпоративной голосовой связи, голосовых звонков и звонков, которые зависят от общедоступной коммутируемой телефонной сети (PSTN).</span><span class="sxs-lookup"><span data-stu-id="25e97-108">[Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Provides overall quality data for different endpoint types, including Enterprise Voice peer-to-peer calls, Enterprise Voice conference calls, and calls that rely, at least in part, on the public switched telephone network (PSTN).</span></span>

  - <span data-ttu-id="25e97-109">[Отчет о сравнении качества мультимедиа в Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Сравнение значений качества звонков для разных типов голосовых вызовов (например, звонки, совершенные по беспроводной сети, и звонки, совершенные через проводное соединение).</span><span class="sxs-lookup"><span data-stu-id="25e97-109">[Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Provides a comparison of call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

  - <span data-ttu-id="25e97-110">[Отчет о производительности сервера в Lync server 2013](lync-server-2013-server-performance-report.md)   В этой статье перечислены серверы, на которых возникли проблемы в большинстве случаев, в зависимости от измерения таких показателей качества, как снижение производительности, потерь пакетов и колебаний.</span><span class="sxs-lookup"><span data-stu-id="25e97-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md)   Lists the servers that have experienced the most problems, based on measurements of such key quality metrics as degradation, packet loss, and jitter.</span></span>

  - <span data-ttu-id="25e97-111">[Отчет о расположении в Lync Server 2013](lync-server-2013-location-report.md)   Список сетевых расположений и краткий обзор качества звонков, происходящих в каждом месте.</span><span class="sxs-lookup"><span data-stu-id="25e97-111">[Location Report in Lync Server 2013](lync-server-2013-location-report.md)   Provides a list of network locations and a summary of the media quality of the calls that occur at each location.</span></span> <span data-ttu-id="25e97-112">В данном отчете расположения основываются на IP-адресах подсетей.</span><span class="sxs-lookup"><span data-stu-id="25e97-112">For purposes of this report, locations are based on IP subnets.</span></span>

  - <span data-ttu-id="25e97-113">[Отчет об устройстве в Lync Server 2013](lync-server-2013-device-report.md)   Общие сведения об устройствах, используемых для корпоративных голосовых звонков, а также среднее качество звонков на устройстве.</span><span class="sxs-lookup"><span data-stu-id="25e97-113">[Device Report in Lync Server 2013](lync-server-2013-device-report.md)   Provides a summary of devices that are used for Enterprise Voice calls and it includes the average media quality of the calls by device.</span></span>

  - <span data-ttu-id="25e97-114">[Отчет "список обзвона" в Lync Server 2013](lync-server-2013-call-list-report.md)   Подробная информация о телефонных звонках, совершенных и полученных в Организации.</span><span class="sxs-lookup"><span data-stu-id="25e97-114">[Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md)   Provides detailed information about phone calls made or received within your organization.</span></span>

  - <span data-ttu-id="25e97-115">[Подробный отчет о звонке в Lync Server 2013](lync-server-2013-call-detail-report.md)   Подробная информация о телефонных звонках, полученных от Организации.</span><span class="sxs-lookup"><span data-stu-id="25e97-115">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md)   Provides detailed information about phone calls made from or received within your organization.</span></span>

  - <span data-ttu-id="25e97-116">[Отчет о тенденциях качества сервера мультимедиа в Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Предоставляет способ для графического сравнения до 5 серверов в метриках качества взаимодействия, таких как громкость звонка, некачественный процент звонков, потеря пакетов и нарушение колебаний.</span><span class="sxs-lookup"><span data-stu-id="25e97-116">[Server Media Quality Trend Report in Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span>

  - <span data-ttu-id="25e97-117">[Отчет о распределении метрик качества мультимедиа в Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Диаграмма, на которой показаны значения распространения для метрики качества взаимодействия, такие как нарушение или потеря пакетов.</span><span class="sxs-lookup"><span data-stu-id="25e97-117">[The Media Quality Metrics Distribution Report in Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Provides a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss.</span></span>

  - <span data-ttu-id="25e97-118">[Отчет о тенденциях расположения в Lync Server 2013](lync-server-2013-location-trend-report.md)   Предоставляет сведения о тенденциях качества связи для сетевых местоположений.</span><span class="sxs-lookup"><span data-stu-id="25e97-118">[Location Trend Report in Lync Server 2013](lync-server-2013-location-trend-report.md)   Provides call quality trend information for network locations.</span></span>

<span data-ttu-id="25e97-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25e97-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

