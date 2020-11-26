---
title: 'Lync Server 2013: обзор типов IP-адресов'
description: 'Lync Server 2013: Общие сведения о типах IP-адресов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of IP address types for Lync Server
ms:assetid: ee9a695f-5cf5-441e-94fb-6adeca50e8d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205363(v=OCS.15)
ms:contentKeyID: 48185759
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81492b2e006a6f44f6deb78e6a0560f6e319992f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445136"
---
# <a name="overview-of-ip-address-types-for-lync-server-2013"></a><span data-ttu-id="a44e7-103">Обзор типов IP-адресов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a44e7-103">Overview of IP address types for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a44e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a44e7-104">

<span> </span></span></span>

<span data-ttu-id="a44e7-105">_**Тема последнего изменения:** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="a44e7-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="a44e7-106">При настройке IP-адресов в Lync Server 2013 у вас есть три варианта.</span><span class="sxs-lookup"><span data-stu-id="a44e7-106">You have three options when configuring IP addresses in Lync Server 2013.</span></span> <span data-ttu-id="a44e7-107">Вы можете настроить Lync Server 2013 таким образом, чтобы он поддерживал только IP версии 4 (IPv4), только IP версии 6 (IPv6) или сочетание обеих (называемых *двойных стеков*).</span><span class="sxs-lookup"><span data-stu-id="a44e7-107">You can configure Lync Server 2013 to support only IP version 4 (IPv4), only IP version 6 (IPv6), or a combination of both (known as a *dual stack*).</span></span> <span data-ttu-id="a44e7-108">Для каждого типа конфигурации существует некоторое количество проблем, которые необходимо принимать во внимание.</span><span class="sxs-lookup"><span data-stu-id="a44e7-108">There are several issues to consider with each type of configuration:</span></span>

  - <span data-ttu-id="a44e7-109">**Только IPv4**   Был создан протокол IPv6, так как в мире использующих IPv4-адреса.</span><span class="sxs-lookup"><span data-stu-id="a44e7-109">**IPv4 only**   IPv6 was created because the world is running out of IPv4 addresses.</span></span> <span data-ttu-id="a44e7-110">В конечном итоге IPv6 будет полностью поддерживаться во всем мире, но в настоящее время многие компании и устройства, с которыми, возможно, приходится иметь дело вашей организации, пока не поддерживают IPv6, и не будут поддерживать еще какое-то время.</span><span class="sxs-lookup"><span data-stu-id="a44e7-110">Ultimately, IPv6 will be fully supported worldwide, but at this time, many companies and devices that your enterprise might need to communicate with do not yet support IPv6, and may not for some time.</span></span> <span data-ttu-id="a44e7-111">Конфигурация, поддерживающая только IPv4-адреса, гарантирует, что реализация Lync Server сможет взаимодействовать с самыми существующими устройствами.</span><span class="sxs-lookup"><span data-stu-id="a44e7-111">An IPv4-only configuration will help to ensure that your Lync Server implementation can communicate with most existing devices.</span></span>

  - <span data-ttu-id="a44e7-112">**Только IPv6**   И наоборот, полная реализация IPv6 в настоящее время будет исключить связь с большим количеством существующих устройств.</span><span class="sxs-lookup"><span data-stu-id="a44e7-112">**IPv6 only**   Conversely, a full IPv6 implementation, at this time, will exclude communication with many existing devices.</span></span>

  - <span data-ttu-id="a44e7-113">**Двойная стопка**   Двухканальный стек — это сеть, в которой разрешены и IPv4, и IPv6-адреса.</span><span class="sxs-lookup"><span data-stu-id="a44e7-113">**Dual Stack**   Dual stack is a network where both IPv4 and IPv6 addresses are enabled.</span></span> <span data-ttu-id="a44e7-114">Эта конфигурация поддерживается в Lync Server 2013, так как в большинстве случаев переход с полной-IPv4 на полный-IPv6 займет несколько лет.</span><span class="sxs-lookup"><span data-stu-id="a44e7-114">This configuration is supported in Lync Server 2013 because in most cases the transition from full-IPv4 to full-IPv6 will take several years.</span></span>

<span data-ttu-id="a44e7-115">В следующих разделах описаны вопросы, касающиеся этих трех конфигураций для различных функций Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a44e7-115">The following sections outline the compatibility among these three configurations for various Lync Server features.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a44e7-p104">Клиентская или серверная конфигурация только с IPv6 поддерживается только для целей проверки или обучения. Конфигурация только с IPv6 не поддерживается в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="a44e7-p104">Client or server configuration with IPv6 only is supported only for lab or validation purposes. IPv6 only configuration is not supported in the production deployment.</span></span>



</div>

<div>

## <a name="client-registration"></a><span data-ttu-id="a44e7-118">Регистрация клиентов</span><span class="sxs-lookup"><span data-stu-id="a44e7-118">Client Registration</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44e7-119">Сеть конечной точки клиента</span><span class="sxs-lookup"><span data-stu-id="a44e7-119">Client endpoint network</span></span></th>
<th><span data-ttu-id="a44e7-120">Сеть сервера</span><span class="sxs-lookup"><span data-stu-id="a44e7-120">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-121">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-121">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-122">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-122">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-123">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-123">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-124">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-124">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-125">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-125">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-126">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-126">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-127">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-127">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-128">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-128">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-129">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-129">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-130">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-130">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-131">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-131">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-132">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-132">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-133">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-133">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-134">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-134">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="peer-to-peer-client"></a><span data-ttu-id="a44e7-135">Одноранговый клиент</span><span class="sxs-lookup"><span data-stu-id="a44e7-135">Peer-to-Peer Client</span></span>

<span data-ttu-id="a44e7-p105">Одноранговые коммуникации включают звуковую связь, видеосвязь, общий доступ к приложениям и передачу файлов. После успешной регистрации обоих клиентов поддерживаются следующие комбинации.</span><span class="sxs-lookup"><span data-stu-id="a44e7-p105">Peer-to-peer communications include audio, audio/video, application sharing, and file transfer. After both clients have successfully registered, the following combinations are supported.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44e7-138">Конечная точка клиента 1</span><span class="sxs-lookup"><span data-stu-id="a44e7-138">Client endpoint 1</span></span></th>
<th><span data-ttu-id="a44e7-139">Конечная точка клиента 2</span><span class="sxs-lookup"><span data-stu-id="a44e7-139">Client endpoint 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-140">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-140">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-141">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-141">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-142">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-142">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-143">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-143">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-144">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-144">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-145">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-145">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-146">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-147">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-147">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-148">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-148">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-149">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="conferencing"></a><span data-ttu-id="a44e7-150">конференц-связь</span><span class="sxs-lookup"><span data-stu-id="a44e7-150">Conferencing</span></span>

<span data-ttu-id="a44e7-151">Конференции включают звук и видео, общий доступ к приложениям и совместную работу с данными (доска и общий доступ к файлам).</span><span class="sxs-lookup"><span data-stu-id="a44e7-151">Conferencing includes audio/video, application sharing, and data collaboration (whiteboarding and file sharing).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44e7-152">Сеть конечной точки клиента</span><span class="sxs-lookup"><span data-stu-id="a44e7-152">Client endpoint network</span></span></th>
<th><span data-ttu-id="a44e7-153">Сеть сервера</span><span class="sxs-lookup"><span data-stu-id="a44e7-153">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-154">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-154">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-155">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-155">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-156">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-156">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-157">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-157">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-158">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-158">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-159">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-159">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-160">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-160">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-161">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-161">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-162">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-162">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-163">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-163">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-164">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-164">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-165">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-165">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-166">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-166">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-167">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-167">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="mediation-serverpstn"></a><span data-ttu-id="a44e7-168">Сервер-посредник/ТСОП</span><span class="sxs-lookup"><span data-stu-id="a44e7-168">Mediation Server/PSTN</span></span>

<span data-ttu-id="a44e7-169">Lync Server 2013 не поддерживает обмен мультимедийными звонками для коммутируемых коммутируемых телефонных сетей (PSTN), если трафик проходит через интерфейс IPv6.</span><span class="sxs-lookup"><span data-stu-id="a44e7-169">Lync Server 2013 does not support media bypass for public switched telephone network (PSTN) calls if the traffic is through an IPv6 interface.</span></span> <span data-ttu-id="a44e7-170">Если требуется обход сервера-посредника, то рекомендуется настроить шлюз ТСОП для IPv4.</span><span class="sxs-lookup"><span data-stu-id="a44e7-170">If media bypass is required, we recommend that the PSTN gateway is configured to IPv4.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44e7-171">Основной интерфейс\*</span><span class="sxs-lookup"><span data-stu-id="a44e7-171">Primary interface\*</span></span></th>
<th><span data-ttu-id="a44e7-172">Интерфейс ТСОП (на сервере-посреднике)</span><span class="sxs-lookup"><span data-stu-id="a44e7-172">PSTN interface (on Mediation Server)</span></span></th>
<th><span data-ttu-id="a44e7-173">Настройка шлюза ТСОП</span><span class="sxs-lookup"><span data-stu-id="a44e7-173">PSTN gateway setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-174">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-174">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-175">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-175">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-176">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-176">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-177">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-177">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-178">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-178">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-179">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-179">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-180">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-180">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-181">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-181">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-182">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-182">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a44e7-183">\* Основным интерфейсом является интерфейс, который взаимодействует с компонентами Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a44e7-183">\* The primary interface is the interface that communicates with the Lync Server components.</span></span>

</div>

<div>

## <a name="remote-user-peer-to-peer-communications"></a><span data-ttu-id="a44e7-184">Одноранговые коммуникации с удаленными пользователями</span><span class="sxs-lookup"><span data-stu-id="a44e7-184">Remote User Peer-to-Peer Communications</span></span>

<span data-ttu-id="a44e7-185">Одноранговые коммуникации с удаленными пользователями включают обмен мгновенными сообщениями, видеосвязь, общий доступ к приложениям и передачу файлов.</span><span class="sxs-lookup"><span data-stu-id="a44e7-185">Peer-to-peer communications with remote users include instant messaging, audio/video, application sharing, and file transfer.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44e7-186">Сеть удаленного пользователя</span><span class="sxs-lookup"><span data-stu-id="a44e7-186">Remote user network</span></span></th>
<th><span data-ttu-id="a44e7-187">Пограничный сервер (внешний периметр)</span><span class="sxs-lookup"><span data-stu-id="a44e7-187">Edge server (External edge)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-188">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-188">IPv4</span></span></p></td>
<td><p><span data-ttu-id="a44e7-189">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-189">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-190">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-190">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-191">IPv4</span><span class="sxs-lookup"><span data-stu-id="a44e7-191">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-192">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-192">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="a44e7-193">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-193">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-194">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-194">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-195">Двойной стек</span><span class="sxs-lookup"><span data-stu-id="a44e7-195">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-196">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-196">IPv6</span></span></p></td>
<td><p><span data-ttu-id="a44e7-197">IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-197">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-pool-and-edge-pool-configuration"></a><span data-ttu-id="a44e7-198">Конфигурация интерфейсного пула и пограничного пула</span><span class="sxs-lookup"><span data-stu-id="a44e7-198">Front End Pool and Edge Pool Configuration</span></span>

<span data-ttu-id="a44e7-199">В таблице ниже показана матрица поддержки между пулом сервер переднего плана и внутренним пулом пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="a44e7-199">The following table shows the support matrix between the Front End Server pool and the internal Edge Server pool.</span></span>

### <a name="front-end-pool-and-edge-pool-internal-edge-matrix"></a><span data-ttu-id="a44e7-200">Матрица интерфейсного пула и пограничного пула (внутренний периметр)</span><span class="sxs-lookup"><span data-stu-id="a44e7-200">Front End Pool and Edge Pool (Internal Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="a44e7-201"><strong>Пограничный пул: IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-201"><strong>Edge Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-202"><strong>Пограничный пул: двойной стек</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-202"><strong>Edge Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-203"><strong>Пограничный пул: IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-203"><strong>Edge Pool: IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-204"><strong>Интерфейсный пул: IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-204"><strong>Front End Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-205">Да</span><span class="sxs-lookup"><span data-stu-id="a44e7-205">Yes</span></span></p></td>
<td><p><span data-ttu-id="a44e7-206">Да</span><span class="sxs-lookup"><span data-stu-id="a44e7-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="a44e7-207">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-208"><strong>Интерфейсный пул: двойной стек</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-208"><strong>Front End Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-209">Да</span><span class="sxs-lookup"><span data-stu-id="a44e7-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="a44e7-210">Да</span><span class="sxs-lookup"><span data-stu-id="a44e7-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="a44e7-211">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-212"><strong>Интерфейсный пул: IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-212"><strong>Front End Pool: IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-213">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-213">No</span></span></p></td>
<td><p><span data-ttu-id="a44e7-214">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-214">No</span></span></p></td>
<td><p><span data-ttu-id="a44e7-215">Да\*</span><span class="sxs-lookup"><span data-stu-id="a44e7-215">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a44e7-216">\* Используйте это сочетание только в лабораторной среде.</span><span class="sxs-lookup"><span data-stu-id="a44e7-216">\* Use this combination only in a lab environment.</span></span>

<span data-ttu-id="a44e7-217">В следующей таблице представлена матрица поддерживаемых комбинаций интерфейсов внешнего и внутреннего периметра.</span><span class="sxs-lookup"><span data-stu-id="a44e7-217">The following table is a matrix of the supported combinations of internal and external edge interfaces.</span></span>

### <a name="edge-pool-internal-edge-and-edge-pool-external-edge-matrix"></a><span data-ttu-id="a44e7-218">Матрица пограничного пула внутреннего периметра и пограничного пула внешнего периметра</span><span class="sxs-lookup"><span data-stu-id="a44e7-218">Edge Pool (Internal Edge) and Edge pool (External Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="a44e7-219"><strong>Пограничный пул (внешний периметр): IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-219"><strong>Edge Pool (External Edge) : IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-220"><strong>Пограничный пул (внешний периметр): двойной стек</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-220"><strong>Edge Pool (External Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-221"><strong>Пограничный пул (внешний периметр): IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-221"><strong>Edge Pool (External Edge): IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-222"><strong>Пограничный пул (внутренний периметр): IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-222"><strong>Edge Pool (Internal Edge): IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-223">Да</span><span class="sxs-lookup"><span data-stu-id="a44e7-223">Yes</span></span></p></td>
<td><p><span data-ttu-id="a44e7-224">Да</span><span class="sxs-lookup"><span data-stu-id="a44e7-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="a44e7-225">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-225">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e7-226"><strong>Пограничный пул (внутренний периметр): двойной стек</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-226"><strong>Edge Pool (Internal Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-227">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-227">No</span></span></p></td>
<td><p><span data-ttu-id="a44e7-228">Да</span><span class="sxs-lookup"><span data-stu-id="a44e7-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="a44e7-229">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-229">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e7-230"><strong>Пограничный пул (внутренний периметр): IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="a44e7-230"><strong>Edge Pool (Internal Edge): IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e7-231">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-231">No</span></span></p></td>
<td><p><span data-ttu-id="a44e7-232">Нет</span><span class="sxs-lookup"><span data-stu-id="a44e7-232">No</span></span></p></td>
<td><p><span data-ttu-id="a44e7-233">Да\*</span><span class="sxs-lookup"><span data-stu-id="a44e7-233">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a44e7-234">\* Используйте это сочетание только в лабораторной среде.</span><span class="sxs-lookup"><span data-stu-id="a44e7-234">\* Use this combination only in a lab environment.</span></span>

</div>

<div>

## <a name="advanced-enterprise-voice-support-for-ipv6"></a><span data-ttu-id="a44e7-235">Улучшенная поддержка корпоративной голосовой связи для IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-235">Advanced Enterprise Voice Support for IPv6</span></span>

<span data-ttu-id="a44e7-236">Развертывания, включающие контроль допуска звонков (CAC), Enhanced 9-1-1 (E9-1-1) или обход сервера-посредника, должны настраиваться как реализация только IPv4 или реализация двойного стека.</span><span class="sxs-lookup"><span data-stu-id="a44e7-236">Deployments that include call admission control (CAC), Enhanced 9-1-1 (E9-1-1), or media bypass must be configured as IPv4 only or as a dual-stacked implementation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a44e7-237">В двухсерверной среде, даже если клиент Lync подключается к серверу Lync Server с помощью IPv6, Lync обеспечивает наилучший способ сопоставления соответствующего адреса IPv4 для поддержки E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="a44e7-237">In a dual-stacked deployment, even if a Lync client connects to a Lync Server by using IPv6, Lync will make a best effort to map an appropriate IPv4 address to support E9-1-1.</span></span>



</div>

<span data-ttu-id="a44e7-238">Служба сведений о расположении с IPv6-адресами не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a44e7-238">Location Information service with IPv6 addresses is not supported.</span></span>

<span data-ttu-id="a44e7-p107">Единая система обмена сообщениями Exchange не поддерживает IPv6. Для единой системы обмена сообщениями Exchange следует убедиться, что DNS-разрешение не возвращает IPv6-адрес. Использование IPv6 может привести к сбою при отправке вызовов в голосовую почту.</span><span class="sxs-lookup"><span data-stu-id="a44e7-p107">Exchange Unified Messaging (UM) does not support IPv6. For Exchange UM, be sure that DNS resolution does not return an IPv6 address. Using IPv6 may cause failure when calls are sent to voice mail.</span></span>

</div>

<div>

## <a name="other-lync-server-2013-feature-support-for-ipv6"></a><span data-ttu-id="a44e7-242">Другие поддерживаемые возможности Lync Server 2013 для IPv6</span><span class="sxs-lookup"><span data-stu-id="a44e7-242">Other Lync Server 2013 Feature Support for IPv6</span></span>

<span data-ttu-id="a44e7-243">Помимо описанных выше функций и компонентов, Lync Server 2013 поддерживает IPv6 для следующих функций:</span><span class="sxs-lookup"><span data-stu-id="a44e7-243">In addition to the features and components mentioned previously, Lync Server 2013 supports IPv6 for the following features:</span></span>

  - <span data-ttu-id="a44e7-244">**Сохраняемый чат**</span><span class="sxs-lookup"><span data-stu-id="a44e7-244">**Persistent Chat**</span></span>
    
    <span data-ttu-id="a44e7-245">Вы можете настроить IPv6 для сохраняемого чата с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="a44e7-245">You configure IPv6 for Persistent Chat by using Topology Builder.</span></span> <span data-ttu-id="a44e7-246">Сведения о настройке сохраняемого чата можно найти в документации развертывание сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="a44e7-246">For details about configuring Persistent Chat, see the Deploying Persistent Chat Server documentation.</span></span>

  - <span data-ttu-id="a44e7-247">**Отчеты качества взаимодействия (QoE) и регистрации вызовов (CDR).**</span><span class="sxs-lookup"><span data-stu-id="a44e7-247">**Quality of Experience (QoE) and call detail recording (CDR) reports**</span></span>
    
    <span data-ttu-id="a44e7-248">Отчеты мониторинга включают IP-адрес в том виде, в каком он хранится в базе данных сервера мониторинга, типа IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="a44e7-248">Monitoring reports include the IP address as it is stored in the Monitoring Server database, whether of type IPv4 or IPv6.</span></span>

<span data-ttu-id="a44e7-249"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a44e7-249"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

