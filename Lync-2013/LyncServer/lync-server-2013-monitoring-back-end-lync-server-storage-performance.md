---
title: 'Lync Server 2013: Мониторинг производительности сервера Lync Server Storage'
description: 'Lync Server 2013: Мониторинг производительности системы хранения данных Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398467"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a><span data-ttu-id="8afff-103">Мониторинг производительности сервера Lync Server 2013 в серверной части</span><span class="sxs-lookup"><span data-stu-id="8afff-103">Monitoring back end Lync Server 2013 storage performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8afff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8afff-104">

<span> </span></span></span>

<span data-ttu-id="8afff-105">_**Тема последнего изменения:** 2014-05-02_</span><span class="sxs-lookup"><span data-stu-id="8afff-105">_**Topic Last Modified:** 2014-05-02_</span></span>

<span data-ttu-id="8afff-106">Серверные базы данных Lync Server 2013 являются важной частью развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8afff-106">The Lync Server 2013 back-end databases are a very important part of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="8afff-107">Мы рекомендуем постоянно отслеживать базы данных и соответствующие журналы транзакций, чтобы обеспечить оптимальное выполнение серверной части Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8afff-107">We recommend constantly monitoring the databases and respective transaction logs to help to make sure that the Lync Server 2013 back end is performing optimally.</span></span>

<span data-ttu-id="8afff-108">В приведенной ниже таблице указаны счетчики производительности, которые необходимо отслеживать для получения сведений о производительности хранилища.</span><span class="sxs-lookup"><span data-stu-id="8afff-108">The following table identifies performance counters that should be monitored to learn information about Storage Performance.</span></span> <span data-ttu-id="8afff-109">Базовые значения для этих счетчиков должны определяться первыми (когда система находится в обычном режиме, ожидаемая загрузка) для понимания изменений производительности при напряжении системы.</span><span class="sxs-lookup"><span data-stu-id="8afff-109">The baseline values for these counters must be determined first (when system is at its normal, expected load) to understand the performance changes when system is stressed.</span></span>

### <a name="performance-counters-to-be-monitored"></a><span data-ttu-id="8afff-110">Наблюдаемые счетчики производительности</span><span class="sxs-lookup"><span data-stu-id="8afff-110">Performance counters to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8afff-111">Счетчик производительности</span><span class="sxs-lookup"><span data-stu-id="8afff-111">Performance Counter</span></span></th>
<th><span data-ttu-id="8afff-112">Пороговые значения базового плана</span><span class="sxs-lookup"><span data-stu-id="8afff-112">Baseline thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8afff-113">Транзакций в секунду (RTC)</span><span class="sxs-lookup"><span data-stu-id="8afff-113">Transactions/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afff-114">Транзакций в секунду (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="8afff-114">Transactions/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afff-115">Транзакций в секунду (база данных tempdb)</span><span class="sxs-lookup"><span data-stu-id="8afff-115">Transactions/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afff-116">Сбросов журнала в секунду (RTC)</span><span class="sxs-lookup"><span data-stu-id="8afff-116">Log Flushes/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afff-117">Сбросов журнала в секунду (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="8afff-117">Log Flushes/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afff-118">Сбросов журнала в секунду (tempdb)</span><span class="sxs-lookup"><span data-stu-id="8afff-118">Log Flushes/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afff-119">Обращений к диску/сек (чтение и запись) — запись данных RTC.</span><span class="sxs-lookup"><span data-stu-id="8afff-119">Disk Transfers/sec (read+write) - RTC db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afff-120">Обмен данными с диском/сек-журнал событий реального времени</span><span class="sxs-lookup"><span data-stu-id="8afff-120">Disk Transfers/sec - RTC log</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afff-121">Обращений к диску в секунду — RTCDyn DB</span><span class="sxs-lookup"><span data-stu-id="8afff-121">Disk Transfers/sec - rtcdyn db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afff-122">Обращений к диску/сек-журнал RTCDyn</span><span class="sxs-lookup"><span data-stu-id="8afff-122">Disk Transfers/sec - rtcdyn log</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="8afff-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8afff-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

