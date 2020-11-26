---
title: 'Lync Server 2013: события UCWA'
description: 'Lync Server 2013: события UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UCWA events
ms:assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945621(v=OCS.15)
ms:contentKeyID: 51541461
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8104ce9c7533350f40ce194e1cde205bc3692792
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440467"
---
# <a name="ucwa-events-in-lync-server-2013"></a><span data-ttu-id="9093b-103">События UCWA в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9093b-103">UCWA events in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9093b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9093b-104">

<span> </span></span></span>

<span data-ttu-id="9093b-105">_**Тема последнего изменения:** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="9093b-105">_**Topic Last Modified:** 2013-02-15_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="9093b-106">Lync Server 2013 использует веб-API единой системы обмена сообщениями (UCWA) в нескольких целях, от доступа к Microsoft Exchange для поиска контактов для обновления сведений о присутствии для мобильных клиентов.</span><span class="sxs-lookup"><span data-stu-id="9093b-106">Lync Server 2013 uses the Unified Communications Web API (UCWA) for a number of purposes, from accessing Microsoft Exchange for contact searches to updating presence for mobile clients.</span></span>

<span data-ttu-id="9093b-p101">UCWA занесет записи о рабочем поведении с типами событий "Информационный", "Предупреждение" и "Ошибка". В следующей таблице описываются события, которые могут регистрироваться компонентами UCWA.</span><span class="sxs-lookup"><span data-stu-id="9093b-p101">UCWA will write records of operational behavior as event types Informational, Warning, and Error. The following table describes the events that can be written by the UCWA components.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9093b-109">Идентификатор события</span><span class="sxs-lookup"><span data-stu-id="9093b-109">Event ID</span></span></th>
<th><span data-ttu-id="9093b-110">Тип события</span><span class="sxs-lookup"><span data-stu-id="9093b-110">Event Type</span></span></th>
<th><span data-ttu-id="9093b-111">Заключение</span><span class="sxs-lookup"><span data-stu-id="9093b-111">Summary</span></span></th>
<th><span data-ttu-id="9093b-112">Причина и решение проблемы</span><span class="sxs-lookup"><span data-stu-id="9093b-112">Cause and Resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9093b-113">20001</span><span class="sxs-lookup"><span data-stu-id="9093b-113">20001</span></span></p></td>
<td><p><span data-ttu-id="9093b-114">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-114">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-115">Инициализировано UCWA</span><span class="sxs-lookup"><span data-stu-id="9093b-115">UCWA initialized</span></span></p></td>
<td><p><span data-ttu-id="9093b-116">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-116">N/A</span></span></p>
<p><span data-ttu-id="9093b-117">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-117">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-118">20002</span><span class="sxs-lookup"><span data-stu-id="9093b-118">20002</span></span></p></td>
<td><p><span data-ttu-id="9093b-119">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-119">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-120">Во время инициализации UCWA возникло неожиданное исключение</span><span class="sxs-lookup"><span data-stu-id="9093b-120">UCWA encountered an unexpected exception during initialization</span></span></p></td>
<td><p><span data-ttu-id="9093b-121">Во время инициализации возникла неожиданная ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-121">An unexpected error has occurred during initialization</span></span></p>
<p><span data-ttu-id="9093b-122">Изучите сведения об исключении в соответствующей записи журнала событий, чтобы определить возможную причину</span><span class="sxs-lookup"><span data-stu-id="9093b-122">Examine the exception details in the associated event log entry to determine the possible cause</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-123">20003</span><span class="sxs-lookup"><span data-stu-id="9093b-123">20003</span></span></p></td>
<td><p><span data-ttu-id="9093b-124">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-124">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-125">В UCWA возникло необработанное исключение</span><span class="sxs-lookup"><span data-stu-id="9093b-125">UCWA encountered an unhandled exception</span></span></p></td>
<td><p><span data-ttu-id="9093b-126">Возникло необработанное исключение</span><span class="sxs-lookup"><span data-stu-id="9093b-126">An unhandled exception happened</span></span></p>
<p><span data-ttu-id="9093b-p102">Перезапустите сервер. Если проблема не устранена, обратитесь в службу поддержки продукта.</span><span class="sxs-lookup"><span data-stu-id="9093b-p102">Restart the server. If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-129">20004</span><span class="sxs-lookup"><span data-stu-id="9093b-129">20004</span></span></p></td>
<td><p><span data-ttu-id="9093b-130">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-130">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-131">Не удается получить доступ к Exchange для фотографии с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="9093b-131">Cannot access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="9093b-132">Недоступно подключение к Exchange</span><span class="sxs-lookup"><span data-stu-id="9093b-132">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="9093b-133">Убедитесь в доступности соединения с Exchange</span><span class="sxs-lookup"><span data-stu-id="9093b-133">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-134">20005</span><span class="sxs-lookup"><span data-stu-id="9093b-134">20005</span></span></p></td>
<td><p><span data-ttu-id="9093b-135">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-135">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-136">Восстановление после сбоя доступа к Exchange для фотографии с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="9093b-136">Recovered from failing to access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="9093b-137">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-137">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-138">20006</span><span class="sxs-lookup"><span data-stu-id="9093b-138">20006</span></span></p></td>
<td><p><span data-ttu-id="9093b-139">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-139">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-140">Не удается получить доступ к Exchange для поиска контакта</span><span class="sxs-lookup"><span data-stu-id="9093b-140">Cannot access Exchange for contact search</span></span></p></td>
<td><p><span data-ttu-id="9093b-141">Недоступно подключение к Exchange</span><span class="sxs-lookup"><span data-stu-id="9093b-141">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="9093b-142">Убедитесь в доступности соединения с Exchange</span><span class="sxs-lookup"><span data-stu-id="9093b-142">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-143">20007</span><span class="sxs-lookup"><span data-stu-id="9093b-143">20007</span></span></p></td>
<td><p><span data-ttu-id="9093b-144">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-144">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-145">Восстановление после сбоя поиска контакта в Exchange</span><span class="sxs-lookup"><span data-stu-id="9093b-145">Recovered from failing to search contact in Exchange</span></span></p></td>
<td><p><span data-ttu-id="9093b-146">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-147">20008</span><span class="sxs-lookup"><span data-stu-id="9093b-147">20008</span></span></p></td>
<td><p><span data-ttu-id="9093b-148">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="9093b-148">Warning</span></span></p></td>
<td><p><span data-ttu-id="9093b-149">Попытка оформления числа подписок, превышающего допустимое количество подписок на сведения о присутствии для приложения</span><span class="sxs-lookup"><span data-stu-id="9093b-149">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p></td>
<td><p><span data-ttu-id="9093b-150">Попытка оформления числа подписок, превышающего допустимое количество подписок на сведения о присутствии для приложения</span><span class="sxs-lookup"><span data-stu-id="9093b-150">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p>
<p><span data-ttu-id="9093b-151">Проверьте клиенты на наличие лишних подписок</span><span class="sxs-lookup"><span data-stu-id="9093b-151">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-152">20009</span><span class="sxs-lookup"><span data-stu-id="9093b-152">20009</span></span></p></td>
<td><p><span data-ttu-id="9093b-153">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="9093b-153">Warning</span></span></p></td>
<td><p><span data-ttu-id="9093b-154">Попытка оформления числа подписок, превышающего допустимое количество подписок на сведения о присутствии для пакета</span><span class="sxs-lookup"><span data-stu-id="9093b-154">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p></td>
<td><p><span data-ttu-id="9093b-155">Попытка оформления числа подписок, превышающего допустимое количество подписок на сведения о присутствии для пакета</span><span class="sxs-lookup"><span data-stu-id="9093b-155">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p>
<p><span data-ttu-id="9093b-156">Проверьте клиенты на наличие лишних подписок</span><span class="sxs-lookup"><span data-stu-id="9093b-156">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-157">20010</span><span class="sxs-lookup"><span data-stu-id="9093b-157">20010</span></span></p></td>
<td><p><span data-ttu-id="9093b-158">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-158">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-159">Не удается получить внутриполосные данные</span><span class="sxs-lookup"><span data-stu-id="9093b-159">Cannot retrieve inband data</span></span></p></td>
<td><p><span data-ttu-id="9093b-160">Не удается получить внутриполосные данные</span><span class="sxs-lookup"><span data-stu-id="9093b-160">Cannot retrieve inband data</span></span></p>
<p><span data-ttu-id="9093b-161">Если проблема не устранена, обратитесь в службу поддержки продукта.</span><span class="sxs-lookup"><span data-stu-id="9093b-161">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-162">20011</span><span class="sxs-lookup"><span data-stu-id="9093b-162">20011</span></span></p></td>
<td><p><span data-ttu-id="9093b-163">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-163">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-164">Не удается подписаться на сведения о присутствии</span><span class="sxs-lookup"><span data-stu-id="9093b-164">Cannot subscribe presence</span></span></p></td>
<td><p><span data-ttu-id="9093b-165">Не удается подписаться на сведения о присутствии</span><span class="sxs-lookup"><span data-stu-id="9093b-165">Cannot subscribe presence</span></span></p>
<p><span data-ttu-id="9093b-166">Если проблема не устранена, обратитесь в службу поддержки продукта.</span><span class="sxs-lookup"><span data-stu-id="9093b-166">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-167">20012</span><span class="sxs-lookup"><span data-stu-id="9093b-167">20012</span></span></p></td>
<td><p><span data-ttu-id="9093b-168">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-168">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-169">Не удалось зарегистрировать конечную точку</span><span class="sxs-lookup"><span data-stu-id="9093b-169">Failed to register endpoint</span></span></p></td>
<td><p><span data-ttu-id="9093b-170">Не удалось зарегистрировать конечную точку</span><span class="sxs-lookup"><span data-stu-id="9093b-170">Failed to register endpoint</span></span></p>
<p><span data-ttu-id="9093b-171">Если проблема не устранена, обратитесь в службу поддержки продукта.</span><span class="sxs-lookup"><span data-stu-id="9093b-171">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-172">20013</span><span class="sxs-lookup"><span data-stu-id="9093b-172">20013</span></span></p></td>
<td><p><span data-ttu-id="9093b-173">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-173">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-174">IM MCU недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-174">IM MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="9093b-175">IM MCU недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-175">IM MCU is unavailable</span></span></p>
<p><span data-ttu-id="9093b-176">Проверьте, запущен ли IM MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-176">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-177">20014</span><span class="sxs-lookup"><span data-stu-id="9093b-177">20014</span></span></p></td>
<td><p><span data-ttu-id="9093b-178">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-178">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-179">Восстановление после сбоя подключения к IM MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-179">Recovered from failing to connect to IM MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-180">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-181">20015</span><span class="sxs-lookup"><span data-stu-id="9093b-181">20015</span></span></p></td>
<td><p><span data-ttu-id="9093b-182">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-182">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-183">AV MCU недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-183">AV MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="9093b-184">AV MCU недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-184">AV MCU is unavailable</span></span></p>
<p><span data-ttu-id="9093b-185">Проверьте, запущен ли AV MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-185">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-186">20016</span><span class="sxs-lookup"><span data-stu-id="9093b-186">20016</span></span></p></td>
<td><p><span data-ttu-id="9093b-187">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-187">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-188">Восстановление после сбоя подключения к AV MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-188">Recovered from failing to connect to AV MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-189">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-189">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-190">20017</span><span class="sxs-lookup"><span data-stu-id="9093b-190">20017</span></span></p></td>
<td><p><span data-ttu-id="9093b-191">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-191">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-192">AS MCU недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-192">AS MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="9093b-193">AS MCU недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-193">AS MCU is unavailable</span></span></p>
<p><span data-ttu-id="9093b-194">Проверьте, запущен ли AS MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-194">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-195">20018</span><span class="sxs-lookup"><span data-stu-id="9093b-195">20018</span></span></p></td>
<td><p><span data-ttu-id="9093b-196">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-196">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-197">Восстановление после сбоя подключения к AS MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-197">Recovered from failing to connect to AS MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-198">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-198">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-199">20019</span><span class="sxs-lookup"><span data-stu-id="9093b-199">20019</span></span></p></td>
<td><p><span data-ttu-id="9093b-200">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-200">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-201">MCU данных недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-201">Data MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="9093b-202">MCU данных недоступен</span><span class="sxs-lookup"><span data-stu-id="9093b-202">Data MCU is unavailable</span></span></p>
<p><span data-ttu-id="9093b-203">Проверьте, запущен ли MCU данных</span><span class="sxs-lookup"><span data-stu-id="9093b-203">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-204">20020</span><span class="sxs-lookup"><span data-stu-id="9093b-204">20020</span></span></p></td>
<td><p><span data-ttu-id="9093b-205">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-205">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-206">Восстановление после сбоя подключения к MCU данных</span><span class="sxs-lookup"><span data-stu-id="9093b-206">Recovered from failing to connect to Data MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-207">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-207">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-208">20021</span><span class="sxs-lookup"><span data-stu-id="9093b-208">20021</span></span></p></td>
<td><p><span data-ttu-id="9093b-209">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-209">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-210">Не удается присоединиться к IM MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-210">Cannot join IM MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-211">Не удается присоединиться к IM MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-211">Cannot join IM MCU</span></span></p>
<p><span data-ttu-id="9093b-212">Проверьте, запущен ли IM MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-212">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-213">20022</span><span class="sxs-lookup"><span data-stu-id="9093b-213">20022</span></span></p></td>
<td><p><span data-ttu-id="9093b-214">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-214">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-215">Не удается присоединиться к AV MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-215">Cannot join AV MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-216">Не удается присоединиться к AV MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-216">Cannot join AV MCU</span></span></p>
<p><span data-ttu-id="9093b-217">Проверьте, запущен ли AV MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-217">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-218">20023</span><span class="sxs-lookup"><span data-stu-id="9093b-218">20023</span></span></p></td>
<td><p><span data-ttu-id="9093b-219">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-219">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-220">Не удается присоединиться к AS MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-220">Cannot join AS MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-221">Не удается присоединиться к AS MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-221">Cannot join AS MCU</span></span></p>
<p><span data-ttu-id="9093b-222">Проверьте, запущен ли AS MCU</span><span class="sxs-lookup"><span data-stu-id="9093b-222">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-223">20024</span><span class="sxs-lookup"><span data-stu-id="9093b-223">20024</span></span></p></td>
<td><p><span data-ttu-id="9093b-224">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-224">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-225">Не удается присоединиться к MCU данных</span><span class="sxs-lookup"><span data-stu-id="9093b-225">Cannot join Data MCU</span></span></p></td>
<td><p><span data-ttu-id="9093b-226">Не удается присоединиться к MCU данных</span><span class="sxs-lookup"><span data-stu-id="9093b-226">Cannot join Data MCU</span></span></p>
<p><span data-ttu-id="9093b-227">Проверьте, запущен ли MCU данных</span><span class="sxs-lookup"><span data-stu-id="9093b-227">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-228">20025</span><span class="sxs-lookup"><span data-stu-id="9093b-228">20025</span></span></p></td>
<td><p><span data-ttu-id="9093b-229">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9093b-229">Error</span></span></p></td>
<td><p><span data-ttu-id="9093b-230">Не удается получить доступ к Active Directory для фотографии</span><span class="sxs-lookup"><span data-stu-id="9093b-230">Cannot access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="9093b-231">Недоступно подключение к Active Directory</span><span class="sxs-lookup"><span data-stu-id="9093b-231">Connection to active directory is not available</span></span></p>
<p><span data-ttu-id="9093b-232">Убедитесь в доступности соединения с Active Directory</span><span class="sxs-lookup"><span data-stu-id="9093b-232">Make sure the connection to active directory is available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9093b-233">20026</span><span class="sxs-lookup"><span data-stu-id="9093b-233">20026</span></span></p></td>
<td><p><span data-ttu-id="9093b-234">Информационный</span><span class="sxs-lookup"><span data-stu-id="9093b-234">Informational</span></span></p></td>
<td><p><span data-ttu-id="9093b-235">Восстановление после сбоя доступа к Active Directory для фотографии</span><span class="sxs-lookup"><span data-stu-id="9093b-235">Recovered from failing to access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="9093b-236">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9093b-236">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9093b-237">20027</span><span class="sxs-lookup"><span data-stu-id="9093b-237">20027</span></span></p></td>
<td><p><span data-ttu-id="9093b-238">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="9093b-238">Warning</span></span></p></td>
<td><p><span data-ttu-id="9093b-239">Не удается выполнить десериализацию</span><span class="sxs-lookup"><span data-stu-id="9093b-239">Cannot deserialize</span></span></p></td>
<td><p><span data-ttu-id="9093b-240">Не удается выполнить десериализацию</span><span class="sxs-lookup"><span data-stu-id="9093b-240">Cannot deserialize</span></span></p>
<p><span data-ttu-id="9093b-241">Если проблема не устранена, обратитесь в службу поддержки продукта.</span><span class="sxs-lookup"><span data-stu-id="9093b-241">If the problem persists contact product support</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9093b-242">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9093b-242">


</div>

<span> </span>

</div>

</div>

</span></span></div>

