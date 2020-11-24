---
title: 'Lync Server 2013: запуск Lync из другого приложения'
description: 'Lync Server 2013: запуск Lync из другого приложения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Starting Lync from another application
ms:assetid: 573b30b1-6590-4b24-8e96-a41be57cb0ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398376(v=OCS.15)
ms:contentKeyID: 48184184
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd64b8b9f335638b54a0bf6473b5d159c97a0e7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398131"
---
# <a name="starting-lync-from-another-application"></a><span data-ttu-id="c0e42-103">Запуск Lync из другого приложения</span><span class="sxs-lookup"><span data-stu-id="c0e42-103">Starting Lync from another application</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0e42-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0e42-104">

<span> </span></span></span>

<span data-ttu-id="c0e42-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="c0e42-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="c0e42-106">Вы можете использовать параметры командной строки для быстрого запуска Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="c0e42-106">You can use command-line parameters to quick-start Lync 2013.</span></span> <span data-ttu-id="c0e42-107">Например, если пользователь щелкает номер телефона в другом приложении, приложение может запустить экземпляр Lync 2013 и инициировать Звонок на этот номер.</span><span class="sxs-lookup"><span data-stu-id="c0e42-107">For example, if a user clicks a phone number in another application, the application can start an instance of Lync 2013 and initiate a call to that number.</span></span>

<span data-ttu-id="c0e42-108">Lync 2013 также может распознать список имен контактов, разделенных точкой с запятой, для односторонних конференций.</span><span class="sxs-lookup"><span data-stu-id="c0e42-108">Lync 2013 can also recognize a semicolon-delimited list of contact names for multiparty conferencing.</span></span>

<span data-ttu-id="c0e42-109">Если Lync 2013 настроен на автоматический вход при запуске, то при запуске Lync 2013 с параметрами командной строки откроется главное окно Lync.</span><span class="sxs-lookup"><span data-stu-id="c0e42-109">If Lync 2013 is configured to automatically sign in when started, then starting Lync 2013 with command-line parameters will open the Lync main window.</span></span> <span data-ttu-id="c0e42-110">Если Lync не настроен для автоматического входа при запуске, откроется окно входа.</span><span class="sxs-lookup"><span data-stu-id="c0e42-110">If Lync is not configured to automatically sign in when started, the sign-in window opens.</span></span>

<span data-ttu-id="c0e42-111">В приведенной ниже таблице показаны доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="c0e42-111">The following table shows the available parameters.</span></span>

### <a name="lync-2013-command-line-parameters"></a><span data-ttu-id="c0e42-112">Параметры Lync 2013 Command-Line</span><span class="sxs-lookup"><span data-stu-id="c0e42-112">Lync 2013 Command-Line Parameters</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0e42-113">Добавоч</span><span class="sxs-lookup"><span data-stu-id="c0e42-113">Extension</span></span></th>
<th><span data-ttu-id="c0e42-114">Формат данных</span><span class="sxs-lookup"><span data-stu-id="c0e42-114">Format of Data</span></span></th>
<th><span data-ttu-id="c0e42-115">Действие</span><span class="sxs-lookup"><span data-stu-id="c0e42-115">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0e42-116">Tel</span><span class="sxs-lookup"><span data-stu-id="c0e42-116">tel:</span></span></p></td>
<td><p><span data-ttu-id="c0e42-117">универсальный код ресурса (URI) Tel</span><span class="sxs-lookup"><span data-stu-id="c0e42-117">tel URI</span></span></p></td>
<td><p><span data-ttu-id="c0e42-118">Открытие окна беседы для голосовой связи, но не набирает указанный номер.</span><span class="sxs-lookup"><span data-stu-id="c0e42-118">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0e42-119">тегом "callto</span><span class="sxs-lookup"><span data-stu-id="c0e42-119">callto:</span></span></p></td>
<td><p><span data-ttu-id="c0e42-120">URI TEL:, SIP: или Type Tel</span><span class="sxs-lookup"><span data-stu-id="c0e42-120">tel:, sip:, or typeable tel URI</span></span></p></td>
<td><p><span data-ttu-id="c0e42-121">Открытие окна беседы для голосовой связи, но не набирает указанный номер.</span><span class="sxs-lookup"><span data-stu-id="c0e42-121">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0e42-122">Установка</span><span class="sxs-lookup"><span data-stu-id="c0e42-122">sip:</span></span></p></td>
<td><p><span data-ttu-id="c0e42-123">Универсальный код ресурса SIP</span><span class="sxs-lookup"><span data-stu-id="c0e42-123">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="c0e42-124">Открытие окна беседы с указанным универсальным кодом ресурса (URI) SIP в списке участников.</span><span class="sxs-lookup"><span data-stu-id="c0e42-124">Opens the Conversation window with the specified SIP Uniform Resource Identifier (URI) in the participant list.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0e42-125">Протоколов</span><span class="sxs-lookup"><span data-stu-id="c0e42-125">Sips:</span></span></p></td>
<td><p><span data-ttu-id="c0e42-126">Универсальный код ресурса SIP</span><span class="sxs-lookup"><span data-stu-id="c0e42-126">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="c0e42-127">Если Lync 2013 настроен на использование протокола TLS, функция работает точно так же, как SIP:.</span><span class="sxs-lookup"><span data-stu-id="c0e42-127">If Lync 2013 is configured to use the Transport Layer Security (TLS) protocol, functions exactly like sip:.</span></span> <span data-ttu-id="c0e42-128">Если TLS не используется, откроется диалоговое окно с уведомлением о том, что требуется более высокий уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="c0e42-128">If TLS is not being used, displays a dialog box informing the user that a higher level of security is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0e42-129">CONF</span><span class="sxs-lookup"><span data-stu-id="c0e42-129">conf:</span></span></p></td>
<td><p><span data-ttu-id="c0e42-130">Универсальный код ресурса (URI) для присоединения к Конференции</span><span class="sxs-lookup"><span data-stu-id="c0e42-130">SIP URI of conference to join</span></span></p></td>
<td><p><span data-ttu-id="c0e42-131">Если URI является самосозданием, он создает фокус и выводит представление только для списка.</span><span class="sxs-lookup"><span data-stu-id="c0e42-131">If URI is self, instantiates the focus and brings up roster-only view.</span></span> <span data-ttu-id="c0e42-132">В противном случае выводится представление списка, но приглашение не отправляется.</span><span class="sxs-lookup"><span data-stu-id="c0e42-132">Otherwise, brings up roster view but does not send INVITE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0e42-133">бесед</span><span class="sxs-lookup"><span data-stu-id="c0e42-133">im:</span></span></p></td>
<td><p><span data-ttu-id="c0e42-134">Универсальный код ресурса SIP</span><span class="sxs-lookup"><span data-stu-id="c0e42-134">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="c0e42-135">Отображается окно беседы с помощью URI SIP (только для обмена мгновенными сообщениями).</span><span class="sxs-lookup"><span data-stu-id="c0e42-135">Displays an instant messaging (IM)-only Conversation window with the SIP URI.</span></span> <span data-ttu-id="c0e42-136">Принимает несколько URI SIP, указанных в угловых скобках ( &lt; &gt; ) без разделителя.</span><span class="sxs-lookup"><span data-stu-id="c0e42-136">Accepts multiple SIP URIs specified inside angle brackets (&lt;&gt;) without any separator.</span></span></p>
<pre><code>im:&lt;sip:user1@host&gt;&lt;sip:user2@host&gt;</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0e42-137">В таблице ниже приведены примеры этих параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="c0e42-137">The following table provides examples of these command-line parameters.</span></span>

### <a name="command-line-parameter-examples"></a><span data-ttu-id="c0e42-138">Примеры параметров Command-Line</span><span class="sxs-lookup"><span data-stu-id="c0e42-138">Command-Line Parameter Examples</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0e42-139">Примеру</span><span class="sxs-lookup"><span data-stu-id="c0e42-139">Instance</span></span></th>
<th><span data-ttu-id="c0e42-140">Поиска</span><span class="sxs-lookup"><span data-stu-id="c0e42-140">Results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0e42-141">Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="c0e42-141">Tel:+14255550101</span></span></p></td>
<td><p><span data-ttu-id="c0e42-142">Открытие представления "только для телефона" с + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="c0e42-142">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0e42-143">Тегом "callto: Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="c0e42-143">Callto:tel:+ 14255550101</span></span></p></td>
<td><p><span data-ttu-id="c0e42-144">Открытие представления "только для телефона" с + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="c0e42-144">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0e42-145">Callto:sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c0e42-145">Callto:sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="c0e42-146">Открытие представления "только для телефона" с kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="c0e42-146">Opens a phone-only view with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0e42-147">sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c0e42-147">sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="c0e42-148">Открытие окна беседы с помощью kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="c0e42-148">Opens a Conversation window with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0e42-149">conf: SIP:https://meet.contoso.com/kazuto/7322994</span><span class="sxs-lookup"><span data-stu-id="c0e42-149">conf:sip:https://meet.contoso.com/kazuto/7322994</span></span></p></td>
<td><p><span data-ttu-id="c0e42-150">Открытие окна беседы и отображение параметров присоединения к звуковому каналу собрания.</span><span class="sxs-lookup"><span data-stu-id="c0e42-150">Opens a Conversation window and displays meeting audio join options.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c0e42-151">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0e42-151">


</div>

<span> </span>

</div>

</div>

</span></span></div>

