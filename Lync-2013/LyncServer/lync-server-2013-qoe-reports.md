---
title: 'Lync Server 2013: отчеты QoE'
description: 'Lync Server 2013: отчеты QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398998"
---
# <a name="qoe-reports-in-lync-server-2013"></a><span data-ttu-id="70066-103">QoE отчеты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70066-103">QoE reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70066-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70066-104">

<span> </span></span></span>

<span data-ttu-id="70066-105">_**Тема последнего изменения:** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="70066-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<div>

## <a name="qoe-summarytrend-reports"></a><span data-ttu-id="70066-106">QoE/отчеты о тенденциях</span><span class="sxs-lookup"><span data-stu-id="70066-106">QoE summary/trend reports</span></span>

<span data-ttu-id="70066-107">Отчеты о сводных данных и тенденциях QoE помогают найти пиковое время использования и проанализировать качество мультимедиа в течение этого периода, чтобы убедиться в том, что сетевые ресурсы Организации достаточны.</span><span class="sxs-lookup"><span data-stu-id="70066-107">The QoE summary/trends reports are useful for finding the peak usage times of day and examining the media quality during those times to help assure that your organization's network resources are sufficient.</span></span> <span data-ttu-id="70066-108">В организации также могут использоваться многочисленные фильтры, доступные в отчете, чтобы изолировать номера производительности для определенных местоположений, типов клиентов и устройств и серверов.</span><span class="sxs-lookup"><span data-stu-id="70066-108">Your organization can also use the many filters available in the report to isolate performance numbers for certain locations, client and device types, and servers.</span></span>

<span data-ttu-id="70066-109">QoE отчеты о тенденциях и тенденции состоят из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="70066-109">QoE summary/trend reports consist of:</span></span>

  - <span data-ttu-id="70066-110">Отчет о сводных данных и тенденциях UC-связи</span><span class="sxs-lookup"><span data-stu-id="70066-110">UC-to-UC Summary/Trend Report</span></span>

  - <span data-ttu-id="70066-111">Отчет о PSTN и тенденциях</span><span class="sxs-lookup"><span data-stu-id="70066-111">PSTN Summary/Trend Report</span></span>

  - <span data-ttu-id="70066-112">Отчет о конференциях и тенденциях</span><span class="sxs-lookup"><span data-stu-id="70066-112">Conference Summary/Trend Report</span></span>

</div>

<div>

## <a name="qoe-performance-reports"></a><span data-ttu-id="70066-113">Отчеты о производительности QoE</span><span class="sxs-lookup"><span data-stu-id="70066-113">QoE performance reports</span></span>

<span data-ttu-id="70066-114">В отчетах о производительности QoE содержатся сведения об этих трех отчетах, которые сосредоточены на QoE производительности серверов-конференций, серверах Конференции и расположениях конечных точек.</span><span class="sxs-lookup"><span data-stu-id="70066-114">QoE performance reports provide details about the three reports that concentrate on the QoE performance of Mediation Servers, A/V Conferencing Servers, and endpoint locations.</span></span>

</div>

<div>

## <a name="mediation-server-performance-report"></a><span data-ttu-id="70066-115">Отчет о производительности сервера «исправление»</span><span class="sxs-lookup"><span data-stu-id="70066-115">Mediation server performance report</span></span>

<span data-ttu-id="70066-116">В отчете "производительность сервера исправлений" перечислены метрики, достигнутые одним или несколькими исправлениями за указанный период времени.</span><span class="sxs-lookup"><span data-stu-id="70066-116">The Mediation Server Performance report lists the metrics achieved by one or more Mediation during the specified time period.</span></span> <span data-ttu-id="70066-117">Метрики сервера единой системы обмена сообщениями (UC), а также сведения о том, как перенаправляться между шлюзами, выводятся отдельно для каждого звонка.</span><span class="sxs-lookup"><span data-stu-id="70066-117">The metrics for the unified communications (UC)-to-Mediation Server leg and the Mediation Server-to-Gateway leg of each call are reported separately.</span></span> <span data-ttu-id="70066-118">С помощью этого отчета вы можете сравнить объем и производительность различных серверов-посредников вашей организации.</span><span class="sxs-lookup"><span data-stu-id="70066-118">Use this report to compare the volume and performance of your organization's various Mediation Servers.</span></span>

<span data-ttu-id="70066-119">Для каждого сервера-посредника (и для каждого участка звонка) в отчете выводятся следующие данные:</span><span class="sxs-lookup"><span data-stu-id="70066-119">For each Mediation Server (and for each call leg), the report displays the following:</span></span>

  - <span data-ttu-id="70066-120">Число звонков</span><span class="sxs-lookup"><span data-stu-id="70066-120">Number of calls</span></span>

  - <span data-ttu-id="70066-121">Packet Loss (Потеря пакетов)</span><span class="sxs-lookup"><span data-stu-id="70066-121">Packet Loss</span></span>

  - <span data-ttu-id="70066-122">Время круга</span><span class="sxs-lookup"><span data-stu-id="70066-122">Round Trip Time</span></span>

  - <span data-ttu-id="70066-123">Искажение</span><span class="sxs-lookup"><span data-stu-id="70066-123">Jitter</span></span>

  - <span data-ttu-id="70066-124">Предметный балл — Оценка вашего мнения (MOS)</span><span class="sxs-lookup"><span data-stu-id="70066-124">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="70066-125">Отправка MOS</span><span class="sxs-lookup"><span data-stu-id="70066-125">Sending MOS</span></span>

  - <span data-ttu-id="70066-126">Прослушивание MOS</span><span class="sxs-lookup"><span data-stu-id="70066-126">Listening MOS</span></span>

  - <span data-ttu-id="70066-127">Сетевые MOS</span><span class="sxs-lookup"><span data-stu-id="70066-127">Network MOS</span></span>

  - <span data-ttu-id="70066-128">Сетевое MOS падение</span><span class="sxs-lookup"><span data-stu-id="70066-128">Network MOS Degradation</span></span>

  - <span data-ttu-id="70066-129">Echo Return</span><span class="sxs-lookup"><span data-stu-id="70066-129">Echo Return</span></span>

  - <span data-ttu-id="70066-130">Уровень сигнала</span><span class="sxs-lookup"><span data-stu-id="70066-130">Signal Level</span></span>

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a><span data-ttu-id="70066-131">Отчет о производительности сервера конференций/V</span><span class="sxs-lookup"><span data-stu-id="70066-131">A/V conferencing server performance report</span></span>

<span data-ttu-id="70066-132">Отчет о производительности сервера конференц-связи "A/V" предоставляет списки метрик, достигнутые одним или несколькими серверами конференц-связи в течение заданного периода времени.</span><span class="sxs-lookup"><span data-stu-id="70066-132">The A/V Conferencing Server Performance report provides lists of metrics achieved by one or more A/V Conferencing Servers during the specified time period.</span></span> <span data-ttu-id="70066-133">Этот отчет можно использовать для сравнения объема и производительности различных серверов конференц-связи в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="70066-133">This report can be used to compare the volume and performance of your organization’s various A/V Conferencing Servers.</span></span> <span data-ttu-id="70066-134">В организации также можно изолировать отчет, чтобы отображались только сведения о конкретных типах клиентов, например клиентах Lync и клиентах PSTN.</span><span class="sxs-lookup"><span data-stu-id="70066-134">Your organization can also isolate the report to show only the experience for specific client types, such as Lync clients or PSTN clients.</span></span>

<span data-ttu-id="70066-135">Для каждого сервера конференций/V в отчете выводятся следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="70066-135">For each A/V Conferencing Server, the report displays the following:</span></span>

  - <span data-ttu-id="70066-136">Количество конференций</span><span class="sxs-lookup"><span data-stu-id="70066-136">Number of conferences</span></span>

  - <span data-ttu-id="70066-137">Packet Loss (Потеря пакетов)</span><span class="sxs-lookup"><span data-stu-id="70066-137">Packet Loss</span></span>

  - <span data-ttu-id="70066-138">Время круга</span><span class="sxs-lookup"><span data-stu-id="70066-138">Round Trip Time</span></span>

  - <span data-ttu-id="70066-139">Искажение</span><span class="sxs-lookup"><span data-stu-id="70066-139">Jitter</span></span>

  - <span data-ttu-id="70066-140">Предметный балл — Оценка вашего мнения (MOS)</span><span class="sxs-lookup"><span data-stu-id="70066-140">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="70066-141">Отправка MOS</span><span class="sxs-lookup"><span data-stu-id="70066-141">Sending MOS</span></span>

  - <span data-ttu-id="70066-142">Прослушивание MOS</span><span class="sxs-lookup"><span data-stu-id="70066-142">Listening MOS</span></span>

  - <span data-ttu-id="70066-143">Сетевые MOS</span><span class="sxs-lookup"><span data-stu-id="70066-143">Network MOS</span></span>

  - <span data-ttu-id="70066-144">Сетевое MOS падение</span><span class="sxs-lookup"><span data-stu-id="70066-144">Network MOS Degradation</span></span>

  - <span data-ttu-id="70066-145">Echo Return</span><span class="sxs-lookup"><span data-stu-id="70066-145">Echo Return</span></span>

  - <span data-ttu-id="70066-146">Уровень сигнала</span><span class="sxs-lookup"><span data-stu-id="70066-146">Signal Level</span></span>

</div>

<div>

## <a name="location-based-performance-report"></a><span data-ttu-id="70066-147">Отчет о производительности на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="70066-147">Location-based performance report</span></span>

<span data-ttu-id="70066-148">Отчет о производительности Location-Based содержит список сетевых расположений и для каждого местоположения показывает количество звонков в каждом из предварительно определенных диапазонов качества.</span><span class="sxs-lookup"><span data-stu-id="70066-148">The Location-Based Performance report provides a list of network locations and for each location shows the number of calls in each pre-determined range of quality.</span></span> <span data-ttu-id="70066-149">Цель этого отчета — предоставить подробное представление о качестве массовых телефонных звонков в вашей организации для различных местоположений, чтобы можно было выявить неработающие места и узнать о различных оценках качества мультимедиа в разных расположениях Организации.</span><span class="sxs-lookup"><span data-stu-id="70066-149">The goal of this report is to provide insight into the media quality of the bulk of your organization’s telephone calls for various locations so that you can identify poorly performing locations, and see the different grades of media quality in your organization’s different locations.</span></span>

<span data-ttu-id="70066-150">При отображении отчета появятся различные таблицы метрик — по одной таблице для каждой метрики, на которую вы решаете сообщить в Организации.</span><span class="sxs-lookup"><span data-stu-id="70066-150">When displaying the report, different tables of metrics appear—one table for each metric your organization decides to report on.</span></span> <span data-ttu-id="70066-151">Для этого отчета можно выбрать следующие метрики:</span><span class="sxs-lookup"><span data-stu-id="70066-151">You can choose from the following metrics for this report:</span></span>

  - <span data-ttu-id="70066-152">Предметный балл — Оценка вашего мнения (MOS)</span><span class="sxs-lookup"><span data-stu-id="70066-152">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="70066-153">Сетевые MOS</span><span class="sxs-lookup"><span data-stu-id="70066-153">Network MOS</span></span>

  - <span data-ttu-id="70066-154">Сетевое MOS падение</span><span class="sxs-lookup"><span data-stu-id="70066-154">Network MOS Degradation</span></span>

  - <span data-ttu-id="70066-155">Отправка MOS</span><span class="sxs-lookup"><span data-stu-id="70066-155">Sending MOS</span></span>

  - <span data-ttu-id="70066-156">Прослушивание MOS</span><span class="sxs-lookup"><span data-stu-id="70066-156">Listening MOS</span></span>

  - <span data-ttu-id="70066-157">Packet Loss (Потеря пакетов)</span><span class="sxs-lookup"><span data-stu-id="70066-157">Packet Loss</span></span>

  - <span data-ttu-id="70066-158">Искажение</span><span class="sxs-lookup"><span data-stu-id="70066-158">Jitter</span></span>

  - <span data-ttu-id="70066-159">Задержка</span><span class="sxs-lookup"><span data-stu-id="70066-159">Latency</span></span>

<span data-ttu-id="70066-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70066-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

