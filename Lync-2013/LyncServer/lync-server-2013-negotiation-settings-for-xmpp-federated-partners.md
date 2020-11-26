---
title: 'Lync Server 2013: параметры согласования для федеративных XMPP-партнеров'
description: 'Lync Server 2013: параметры согласования для федеративных партнеров XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445590"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="e04c6-103">Параметры согласования для федеративных XMPP-партнеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e04c6-103">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e04c6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e04c6-104">

<span> </span></span></span>

<span data-ttu-id="e04c6-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="e04c6-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="e04c6-106">Параметры типов согласования в конфигурации XMPP партнера имеют широкий спектр возможных комбинаций.</span><span class="sxs-lookup"><span data-stu-id="e04c6-106">The settings for the negotiation types in the configuration of an XMPP Partner have a wide variety of possible combinations.</span></span> <span data-ttu-id="e04c6-107">Не все из этих сочетаний являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="e04c6-107">Not all of these combinations are valid.</span></span> <span data-ttu-id="e04c6-108">В таблице, подробно описанной в этом разделе, определяются допустимые и недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="e04c6-108">The table detailed in this topic will define the valid and not valid settings.</span></span> <span data-ttu-id="e04c6-109">Общие конфигурации представлены в первой таблице, во второй — на всех возможных комбинациях.</span><span class="sxs-lookup"><span data-stu-id="e04c6-109">Common configurations are presented in the first table, the second table detailing all possible combinations.</span></span> <span data-ttu-id="e04c6-110">Обратите внимание на то, что вы не можете использовать *простую проверку подлинности и уровень безопасности* (SASL), **если** также не доступен TLS- *Безопасность* .</span><span class="sxs-lookup"><span data-stu-id="e04c6-110">Note that you cannot have *Simple Authentication and Security Layer* (SASL) **unless** *Transport Layer Security* (TLS) is also available.</span></span> <span data-ttu-id="e04c6-111">SASL отправляется в незашифрованном (читаемом) формате, и его не следует передавать, если только они не защищены другим способом, например TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-111">SASL is sent in an unencrypted (readable) format and should never be transmitted unless protected by another means, such as TLS.</span></span>

### <a name="common-xmpp-federation-negotiation-methods"></a><span data-ttu-id="e04c6-112">Распространенные методы согласования XMPP Федерации</span><span class="sxs-lookup"><span data-stu-id="e04c6-112">Common XMPP Federation Negotiation Methods</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e04c6-113">Безопасность уровня транспорта (TLS)</span><span class="sxs-lookup"><span data-stu-id="e04c6-113">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="e04c6-114">Простая проверка подлинности и уровень безопасности (SASL)</span><span class="sxs-lookup"><span data-stu-id="e04c6-114">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="e04c6-115">Проверка подлинности Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-115">Dialback Authentication</span></span></th>
<th><span data-ttu-id="e04c6-116">Ожидаемый метод проверки подлинности (-ов)</span><span class="sxs-lookup"><span data-stu-id="e04c6-116">Expected Authentication Method(s)</span></span></th>
<th><span data-ttu-id="e04c6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e04c6-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-118"> Обязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-118">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-119">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-120">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-120">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-121">SASL по протоколу TLS</span><span class="sxs-lookup"><span data-stu-id="e04c6-121">SASL over TLS</span></span></p></td>
<td><p><span data-ttu-id="e04c6-122">TLS и SASL должны обеспечивать безопасность потока сообщений SASL.</span><span class="sxs-lookup"><span data-stu-id="e04c6-122">TLS and SASL required helps to ensure that the SASL message stream is secure.</span></span> <span data-ttu-id="e04c6-123">Dialback недоступен и не может использоваться для резервного метода в том случае, если для федеративного партнера XMPP не задано обязательное или необязательное значение TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-123">Dialback is not available and cannot be used for a fallback method if the XMPP federated partner has not set TLS to required or optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-124">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-125">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-126">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-126">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-127">SASL over TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-127">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="e04c6-128">Если для федеративного партнера XMPP задано значение SASL для необязательного или требуемого SASL, используется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-128">By requiring TLS, if the XMPP federated partner has set SASL to optional or required SASL is used.</span></span> <span data-ttu-id="e04c6-129">Если SASL недоступен, будет использоваться Dialback по TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-129">If SASL is not available, Dialback over TLS will be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-130">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-131">Необязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-132">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-132">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-133">SASL over TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-133">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="e04c6-134">Несмотря на то, что предлагаемые методы согласования очень гибки, эти параметры основываются на параметрах партнера XMPP Федерации.</span><span class="sxs-lookup"><span data-stu-id="e04c6-134">While very flexible in the negotiation methods offered, these settings rely on the XMPP federation partner’s settings.</span></span> <span data-ttu-id="e04c6-135">Если у партнера есть TLS, необязательный или обязательный, но SASL не поддерживается, TLS Dialback будет доступен.</span><span class="sxs-lookup"><span data-stu-id="e04c6-135">If the partner has TLS optional or required but SASL is not supported, TLS Dialback will be available.</span></span> <span data-ttu-id="e04c6-136">Если у партнера есть TLS и SASL, для которых установлен необязательный или обязательный вариант, используется оптимальный выбор TLS более SASL.</span><span class="sxs-lookup"><span data-stu-id="e04c6-136">If the partner has TLS and SASL set to optional or required, the optimal selection of TLS over SASL is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-137">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-137">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-138">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-138">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-139">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-139">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-140">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-140">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="e04c6-141">Во многих случаях TCP Dialback является единственным возможным решением.</span><span class="sxs-lookup"><span data-stu-id="e04c6-141">In many cases, TCP Dialback is the only possible solution.</span></span> <span data-ttu-id="e04c6-142">Менее предпочтительнее, чем другие параметры, она обеспечивает некоторый уровень доверия.</span><span class="sxs-lookup"><span data-stu-id="e04c6-142">Less desirable than other options, it does provide some level of trust.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a><span data-ttu-id="e04c6-143">Матрица методов согласования XMPP Федерации — завершено</span><span class="sxs-lookup"><span data-stu-id="e04c6-143">XMPP Federation Negotiation Methods Matrix - Complete</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e04c6-144">Безопасность уровня транспорта (TLS)</span><span class="sxs-lookup"><span data-stu-id="e04c6-144">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="e04c6-145">Простая проверка подлинности и уровень безопасности (SASL)</span><span class="sxs-lookup"><span data-stu-id="e04c6-145">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="e04c6-146">Проверка подлинности Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-146">Dialback Authentication</span></span></th>
<th><span data-ttu-id="e04c6-147">Ожидаемый метод проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="e04c6-147">Expected Authentication Method</span></span></th>
<th><span data-ttu-id="e04c6-148">Заметки, предупреждение или ошибка для недействительной конфигурации</span><span class="sxs-lookup"><span data-stu-id="e04c6-148">Notes, Warning or Error for Not Valid Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-149"> Обязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-149">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-150">Обязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-150">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-151">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-151">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-152">SASL по протоколу TLS</span><span class="sxs-lookup"><span data-stu-id="e04c6-152">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-153">Dialback не будет работать, если требуются оба SASL и TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-153">Dialback will not operate if both SASL and TLS are required.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-154"> Обязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-154">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-155">Обязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-155">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-156">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-156">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-157">SASL по протоколу TLS</span><span class="sxs-lookup"><span data-stu-id="e04c6-157">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-158">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-158">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-159">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-160">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-160">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-161">SASL over TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-161">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-162">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-162">SASL requires TLS.</span></span> <span data-ttu-id="e04c6-163">Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.</span><span class="sxs-lookup"><span data-stu-id="e04c6-163">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-164">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-164">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-165">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-165">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-166">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-166">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-167">SASL по протоколу TLS</span><span class="sxs-lookup"><span data-stu-id="e04c6-167">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-168">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-168">SASL requires TLS.</span></span> <span data-ttu-id="e04c6-169">Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.</span><span class="sxs-lookup"><span data-stu-id="e04c6-169">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-170">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-170">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-171">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-171">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-172">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-172">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-173">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-173">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-174">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-174">SASL requires TLS.</span></span> <span data-ttu-id="e04c6-175">Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.</span><span class="sxs-lookup"><span data-stu-id="e04c6-175">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-176">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-176">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-177">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-177">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-178">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-178">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-179">Недействительная конфигурация</span><span class="sxs-lookup"><span data-stu-id="e04c6-179">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-180">Так как для SASL требуется протокол TLS, а протокол TLS недоступен, SASL/TLS выполнить не удастся.</span><span class="sxs-lookup"><span data-stu-id="e04c6-180">Because SASL requires TLS, and TLS is not available, SASL/TLS cannot succeed.</span></span> <span data-ttu-id="e04c6-181">Для TCP Dialback задано значение false, и его нельзя использовать.</span><span class="sxs-lookup"><span data-stu-id="e04c6-181">TCP Dialback is set to false, and cannot be used.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-182">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-182">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-183">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-183">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-184">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-184">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-185">SASL over TLS, Dialback TLS</span><span class="sxs-lookup"><span data-stu-id="e04c6-185">SASL over TLS, TLS Dialback</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-186">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-186">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-187">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-187">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-188">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-188">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-189">SASL по протоколу TLS</span><span class="sxs-lookup"><span data-stu-id="e04c6-189">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-190">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-190">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-191">Необязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-191">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-192">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-192">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-193">SASL over TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-193">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-194">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-194">SASL requires TLS.</span></span> <span data-ttu-id="e04c6-195">Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.</span><span class="sxs-lookup"><span data-stu-id="e04c6-195">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-196">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-196">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-197">Необязательно</span><span class="sxs-lookup"><span data-stu-id="e04c6-197">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-198">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-198">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-199">SASL по протоколу TLS</span><span class="sxs-lookup"><span data-stu-id="e04c6-199">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-200">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-200">SASL requires TLS.</span></span> <span data-ttu-id="e04c6-201">Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.</span><span class="sxs-lookup"><span data-stu-id="e04c6-201">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-202">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-202">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-203">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-203">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-204">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-204">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-205">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-205">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-206">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-206">SASL requires TLS.</span></span> <span data-ttu-id="e04c6-207">Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.</span><span class="sxs-lookup"><span data-stu-id="e04c6-207">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-208">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-208">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-209">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-209">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-210">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-210">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-211">Недействительная конфигурация</span><span class="sxs-lookup"><span data-stu-id="e04c6-211">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-212">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="e04c6-212">SASL requires TLS.</span></span> <span data-ttu-id="e04c6-213">Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.</span><span class="sxs-lookup"><span data-stu-id="e04c6-213">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-214">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-214">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-215">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-215">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-216">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-216">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-217">TLS Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-217">TLS Dialback</span></span></p></td>
<td><p><span data-ttu-id="e04c6-218">Настройка позволяет TLS Dialback.</span><span class="sxs-lookup"><span data-stu-id="e04c6-218">Configuration allows for TLS Dialback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-219">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e04c6-219">Required</span></span></p></td>
<td><p><span data-ttu-id="e04c6-220">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-220">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-221">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-221">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-222">Недействительная конфигурация</span><span class="sxs-lookup"><span data-stu-id="e04c6-222">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-223">Необходимо включить SASL или Dialback.</span><span class="sxs-lookup"><span data-stu-id="e04c6-223">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-224">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-224">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-225">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-225">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-226">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-226">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-227">TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-227">TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="e04c6-228">На основе вариантов согласования для другой конечной точки, TCP или TLS Dialback будут приняты.</span><span class="sxs-lookup"><span data-stu-id="e04c6-228">Based on negotiation choices of the other end point, TCP or TLS Dialback will be accepted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-229">Необязательно </span><span class="sxs-lookup"><span data-stu-id="e04c6-229">Optional</span></span></p></td>
<td><p><span data-ttu-id="e04c6-230">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-230">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-231">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-231">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-232">Недействительная конфигурация</span><span class="sxs-lookup"><span data-stu-id="e04c6-232">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-233">Необходимо включить SASL или Dialback.</span><span class="sxs-lookup"><span data-stu-id="e04c6-233">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c6-234">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-234">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-235">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-235">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-236">Верно</span><span class="sxs-lookup"><span data-stu-id="e04c6-236">True</span></span></p></td>
<td><p><span data-ttu-id="e04c6-237">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="e04c6-237">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="e04c6-238">Протокол TCP Dialback является единственным доступным способом согласования</span><span class="sxs-lookup"><span data-stu-id="e04c6-238">TCP Dialback is the only negotiation method available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c6-239">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-239">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-240">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e04c6-240">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="e04c6-241">False</span><span class="sxs-lookup"><span data-stu-id="e04c6-241">False</span></span></p></td>
<td><p><span data-ttu-id="e04c6-242">Недействительная конфигурация</span><span class="sxs-lookup"><span data-stu-id="e04c6-242">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="e04c6-243">Необходимо включить SASL или Dialback.</span><span class="sxs-lookup"><span data-stu-id="e04c6-243">SASL or Dialback must be enabled.</span></span>


<span data-ttu-id="e04c6-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e04c6-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

