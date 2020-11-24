---
title: 'Lync Server 2013: отчеты о диагностике звонков'
description: 'Lync Server 2013: отчеты о диагностике звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Reports
ms:assetid: 8d362dd9-a119-4601-a3b4-3e7ed0aaa92e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615013(v=OCS.15)
ms:contentKeyID: 48184794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6acc41585414e134eebde1635729b470c7f3472c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399409"
---
# <a name="call-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="6b13a-103">Диагностические отчеты о звонках в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b13a-103">Call Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b13a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b13a-104">

<span> </span></span></span>

<span data-ttu-id="6b13a-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="6b13a-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="6b13a-106">Диагностические отчеты по вызовам предоставляют сводные сведения и диагностические данные для неудачных одноранговых сеансов связи и сеансов конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="6b13a-106">The Call Diagnostic Reports provide summary information and diagnostic data for failed peer-to-peer and conferencing sessions.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6b13a-107">Содержание</span><span class="sxs-lookup"><span data-stu-id="6b13a-107">In This Section</span></span>

  - <span data-ttu-id="6b13a-108">[Сводный отчет о звонке в Lync Server 2013](lync-server-2013-call-diagnostic-summary-report.md)   Общие сведения об ошибках одноранговых сеансов и сеансов конференций.</span><span class="sxs-lookup"><span data-stu-id="6b13a-108">[Call Diagnostic Summary Report in Lync Server 2013](lync-server-2013-call-diagnostic-summary-report.md)   Provides an overall summary of failed peer-to-peer sessions and conference sessions.</span></span> <span data-ttu-id="6b13a-109">Одноранговые сеансы – это сеансы, в которых только два участника.</span><span class="sxs-lookup"><span data-stu-id="6b13a-109">Peer-to-peer sessions are sessions that involve just two participants.</span></span> <span data-ttu-id="6b13a-110">Сеансы конференц-связи включают не менее трех участников.</span><span class="sxs-lookup"><span data-stu-id="6b13a-110">Conferencing sessions involve three or more participants.</span></span>

  - <span data-ttu-id="6b13a-111">[Диагностический отчет о действиях одноранговой сети в Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   Обеспечивает общее представление тенденций неудачных одноранговых сеансов.</span><span class="sxs-lookup"><span data-stu-id="6b13a-111">[Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   Provides an overall trend view of failed peer-to-peer sessions.</span></span> <span data-ttu-id="6b13a-112">В одноранговых сеансах имеется только два участника.</span><span class="sxs-lookup"><span data-stu-id="6b13a-112">A peer-to-peer session involves just two participants.</span></span>

  - <span data-ttu-id="6b13a-113">[Диагностический отчет на Конференции в Lync Server 2013](lync-server-2013-conference-diagnostic-report.md)   Предоставляет общее представление о неудачных сеансах и представлениях тенденций для всех модальных конференций.</span><span class="sxs-lookup"><span data-stu-id="6b13a-113">[Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md)   Provides an overall trend view of failed conferencing sessions and trend views for each conference modality.</span></span> <span data-ttu-id="6b13a-114">Сеансы конференц-связи включают не менее трех участников.</span><span class="sxs-lookup"><span data-stu-id="6b13a-114">Conferencing sessions involve at least three participants.</span></span>

  - <span data-ttu-id="6b13a-115">[Отчет об ошибках верхнего уровня в Lync Server 2013](lync-server-2013-top-failures-report.md)   Список наиболее часто используемых сбоев и тенденций их тенденции с течением времени.</span><span class="sxs-lookup"><span data-stu-id="6b13a-115">[Top Failures Report in Lync Server 2013](lync-server-2013-top-failures-report.md)   Provides a list of the most frequent failures and their trends over time.</span></span>

  - <span data-ttu-id="6b13a-116">[Отчет о распределении отказов в Lync Server 2013](lync-server-2013-failure-distribution-report.md)   Обеспечивает анализ неудачных сеансов.</span><span class="sxs-lookup"><span data-stu-id="6b13a-116">[Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md)   Provides an analysis of failed sessions.</span></span>

  - <span data-ttu-id="6b13a-117">[Отчет о списке отказов в Lync Server 2013](lync-server-2013-failure-list-report.md)   Подробные сведения об отдельных участниках, вовлеченных в неудачную конференцию.</span><span class="sxs-lookup"><span data-stu-id="6b13a-117">[Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md)   Provides detailed information about the individual participants involved in a failed conference.</span></span>

  - <span data-ttu-id="6b13a-118">[Диагностический отчет в Lync Server 2013](lync-server-2013-diagnostic-report.md)   Сведения о диагностике и устранении неполадок (в том числе коды ответов SIP и диагностические заголовки и идентификаторы) для сеансов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="6b13a-118">[Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md)   Provides diagnostic and troubleshooting information (including SIP response codes and diagnostic headers and IDs) for failed sessions.</span></span>

<span data-ttu-id="6b13a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b13a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

