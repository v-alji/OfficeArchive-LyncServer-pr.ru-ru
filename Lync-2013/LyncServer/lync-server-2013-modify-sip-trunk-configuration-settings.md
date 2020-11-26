---
title: 'Lync Server 2013: изменение параметров конфигурации магистральной магистрали SIP'
description: 'Lync Server 2013: изменение параметров конфигурации магистральной магистрали SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify SIP trunk configuration settings
ms:assetid: 7d68b09c-9ea0-43bd-997c-df887869d607
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688104(v=OCS.15)
ms:contentKeyID: 49733703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42cb213211a11494a96b5a762734a2b5db49dfbb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425453"
---
# <a name="modify-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="30f6e-103">Изменение параметров конфигурации магистральной магистрали SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30f6e-103">Modify SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30f6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30f6e-104">

<span> </span></span></span>

<span data-ttu-id="30f6e-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="30f6e-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="30f6e-106">Параметры конфигурации магистральной магистрали SIP определяют связь и возможности между сервером-посредником и шлюзом коммутируемой телефонной сети (PSTN), Интернет-ПРОТОКОЛом (УАТС) или контроллером границ сеанса (SBC) в поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="30f6e-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="30f6e-107">Эти параметры, в частности, определяют следующее:</span><span class="sxs-lookup"><span data-stu-id="30f6e-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="30f6e-108">следует включать ли обход сервера-посредника на магистралях;</span><span class="sxs-lookup"><span data-stu-id="30f6e-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="30f6e-109">Условия, при которых отправляются пакеты протокола управления транспортом в реальном времени (RTCP).</span><span class="sxs-lookup"><span data-stu-id="30f6e-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="30f6e-110">Требуется ли шифрование на всех магистральах в режиме реального времени (SRTP).</span><span class="sxs-lookup"><span data-stu-id="30f6e-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="30f6e-111">При установке Microsoft Lync Server 2013 создается глобальная коллекция параметров конфигурации магистральной магистрали SIP.</span><span class="sxs-lookup"><span data-stu-id="30f6e-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="30f6e-112">Кроме того, администраторы могут создавать пользовательские коллекции настроек на уровне сайта или службы (только для службы шлюза ТСОП).</span><span class="sxs-lookup"><span data-stu-id="30f6e-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span> <span data-ttu-id="30f6e-113">Любую из этих коллекций позже можно будет изменить с помощью панели управления Lync Server или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30f6e-113">Any of these collections can later be modified using either Lync Server Control Panel or Windows PowerShell.</span></span>

<span data-ttu-id="30f6e-114">При изменении параметров конфигурации магистральной магистрали SIP с помощью панели управления Lync Server вы можете воспользоваться следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="30f6e-114">When modifying SIP trunk configuration settings using Lync Server Control Panel, the following options are available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30f6e-115">Параметр пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="30f6e-115">UI Setting</span></span></th>
<th><span data-ttu-id="30f6e-116">Параметр PowerShell</span><span class="sxs-lookup"><span data-stu-id="30f6e-116">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="30f6e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="30f6e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-118">Имя</span><span class="sxs-lookup"><span data-stu-id="30f6e-118">Name</span></span></p></td>
<td><p><span data-ttu-id="30f6e-119">Identity</span><span class="sxs-lookup"><span data-stu-id="30f6e-119">Identity</span></span></p></td>
<td><p><span data-ttu-id="30f6e-p103">Уникальный идентификатор для коллекции. Это свойство только для чтения; вы не можете изменить идентификатор коллекции параметров настройки магистральной линии связи.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p103">Unique identifier for the collection. This property is read-only; you cannot change the Identity of a collection of trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-122">Описание</span><span class="sxs-lookup"><span data-stu-id="30f6e-122">Description</span></span></p></td>
<td><p><span data-ttu-id="30f6e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="30f6e-123">Description</span></span></p></td>
<td><p><span data-ttu-id="30f6e-124">Предоставляет администраторам возможность сохранять дополнительную информацию о параметрах (например, сведения о цели настройки магистральной линии связи).</span><span class="sxs-lookup"><span data-stu-id="30f6e-124">Provides a way for administrators to store addition information about the settings (for example, the purpose of the trunk configuration).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-125">Максимальное количество поддерживаемых предварительных диалогов</span><span class="sxs-lookup"><span data-stu-id="30f6e-125">Maximum early dialogs supported</span></span></p></td>
<td><p><span data-ttu-id="30f6e-126">MaxEarlyDialogs</span><span class="sxs-lookup"><span data-stu-id="30f6e-126">MaxEarlyDialogs</span></span></p></td>
<td><p><span data-ttu-id="30f6e-127">Максимальное количество разветвляющихся ответов, которое шлюз ТСОП, IP-PBX или пограничный контроллер сеансов (SBC) на стороне поставщика службы может получить на приглашение, отправленное серверу-посреднику.</span><span class="sxs-lookup"><span data-stu-id="30f6e-127">The maximum number of forked responses a PSTN gateway, IP-PBX, or SBC at the service provider can receive to an Invite that it sent to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-128">Уровень поддержки шифрования</span><span class="sxs-lookup"><span data-stu-id="30f6e-128">Encryption support level</span></span></p></td>
<td><p><span data-ttu-id="30f6e-129">SRTPMode</span><span class="sxs-lookup"><span data-stu-id="30f6e-129">SRTPMode</span></span></p></td>
<td><p><span data-ttu-id="30f6e-130">Указывает уровень поддержки для защиты трафика сервера-посредника между сервером-посредником и шлюзом ТСОП, IP-PBX или пограничным контроллером сеансов на стороне поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="30f6e-130">Indicates the level of support for protecting media traffic between the Mediation Server and the PSTN Gateway, IP-PBX, or SBC at the service provider.</span></span> <span data-ttu-id="30f6e-131">Для случаев обхода сервера-посредника это значение должно быть совместимо с параметром EncryptionLevel в настройке сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="30f6e-131">For media bypass cases, this value must be compatible with the EncryptionLevel setting in the media configuration.</span></span> <span data-ttu-id="30f6e-132">Настройка мультимедиа задается с помощью командлетов <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> и <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">Set-CsMediaConfiguration</a> .</span><span class="sxs-lookup"><span data-stu-id="30f6e-132">Media configuration is set by using the <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> and <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">Set-CsMediaConfiguration</a> cmdlets.</span></span></p>
<p><span data-ttu-id="30f6e-133">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="30f6e-133">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="30f6e-134">Требуется: должно использоваться шифрование SRTP.</span><span class="sxs-lookup"><span data-stu-id="30f6e-134">Required: SRTP encryption must be used.</span></span></p></li>
<li><p><span data-ttu-id="30f6e-135">Необязательно: SRTP будет использоваться, если поддерживается шлюзом.</span><span class="sxs-lookup"><span data-stu-id="30f6e-135">Optional: SRTP will be used if the gateway supports it.</span></span></p></li>
<li><p><span data-ttu-id="30f6e-136">Не поддерживается: шифрование SRTP не поддерживается и поэтому не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="30f6e-136">Not Supported: SRTP encryption is not supported and therefore will not be used.</span></span></p></li>
</ul>
<p><span data-ttu-id="30f6e-p105">Параметр SRTPMode используется, только в случае, если шлюз настроен на использование протокола TLS. Если шлюз настроен на использование в качестве транспорта протокола TCP, для параметра SRTPMode внутренним образом задается значение Not Supported.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p105">SRTPMode is used only if the gateway is configured to use Transport Layer Security (TLS). If the gateway is configured with Transmission Control Protocol (TCP) as the transport, SRTPMode is internally set to Not Supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-139">Поддержка ссылки</span><span class="sxs-lookup"><span data-stu-id="30f6e-139">Refer support</span></span></p></td>
<td><p><span data-ttu-id="30f6e-140">Enable3pccRefer</span><span class="sxs-lookup"><span data-stu-id="30f6e-140">Enable3pccRefer</span></span></p>
<p><span data-ttu-id="30f6e-141">EnableReferSupport</span><span class="sxs-lookup"><span data-stu-id="30f6e-141">EnableReferSupport</span></span></p></td>
<td><p><span data-ttu-id="30f6e-142">Если задано <strong>Разрешить отправку ссылки шлюзу</strong>, это указывает на то, что магистральная линия связи поддерживает получение запросов ссылки от сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="30f6e-142">If set to <strong>Enable sending refer to the gateway</strong>, indicates that the trunk supports receiving Refer requests from the Mediation Server.</span></span></p>
<p><span data-ttu-id="30f6e-143">Если задано <strong>Разрешить ссылку с использованием стороннего контроля вызовов</strong>, это указывает на то, что протокол 3pcc может использоваться, чтобы разрешить переключенным звонкам обходить размещенный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="30f6e-143">If set to <strong>Enable refer using third-party call control</strong>, indicates that the 3pcc protocol can be used to allow transferred calls to bypass the hosted site.</span></span> <span data-ttu-id="30f6e-144">3pcc также называется &quot; третьим элементом управления &quot; и происходит, когда третья сторона используется для подключения к паре вызывающих абонентов (например, оператором, который помещает звонок от человека к человеку B).</span><span class="sxs-lookup"><span data-stu-id="30f6e-144">3pcc is also known as &quot;third party control,&quot; and occurs when a third-party is used to connect a pair of callers (for example, an operator placing a call from person A to person B).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-145">Разрешить обход сервера-посредника</span><span class="sxs-lookup"><span data-stu-id="30f6e-145">Enable media bypass</span></span></p></td>
<td><p><span data-ttu-id="30f6e-146">EnableBypass</span><span class="sxs-lookup"><span data-stu-id="30f6e-146">EnableBypass</span></span></p></td>
<td><p><span data-ttu-id="30f6e-p107">Указывает, включен обход сервера-посредника для этой магистральной линии связи. Обход сервера-посредника может быть включен только в случае, если также включен параметр <strong>Централизованная обработка мультимедиа</strong>.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p107">Indicates whether media bypass is enabled for this trunk. Media bypass can only be enabled if <strong>Centralized media processing</strong> is also enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-149">Централизованная обработка мультимедиа</span><span class="sxs-lookup"><span data-stu-id="30f6e-149">Centralized media processing</span></span></p></td>
<td><p><span data-ttu-id="30f6e-150">ConcentratedTopology</span><span class="sxs-lookup"><span data-stu-id="30f6e-150">ConcentratedTopology</span></span></p></td>
<td><p><span data-ttu-id="30f6e-p108">Enable RTP latching имеется ли известная точка терминирования медиаданных. (Примером известной точки терминирования медиаданных может являться шлюз ТСОП, где у точки терминирования медиаданных такой же IP-адрес, что и у точки терминирования сигналов.)</span><span class="sxs-lookup"><span data-stu-id="30f6e-p108">Indicates whether there is a well-known media termination point. (An example of a well-known media termination point would be a PSTN gateway where the media termination has the same IP as the signaling termination.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-153">Разрешить блокирование RTP</span><span class="sxs-lookup"><span data-stu-id="30f6e-153">Enable RTP latching</span></span></p></td>
<td><p><span data-ttu-id="30f6e-154">EnableRTPLatching</span><span class="sxs-lookup"><span data-stu-id="30f6e-154">EnableRTPLatching</span></span></p></td>
<td><p><span data-ttu-id="30f6e-p109">Указывает, поддерживают ли магистральные линии связи SIP блокирование RTP. Блокирование RTP является технологией, позволяющей выполнять подключение по протоколу RTP/RTCP через устройство NAT (преобразование сетевых адресов) или брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p109">Indicates whether or not the SIP trunks support RTP latching. RTP latching is a technology that enables RTP/RTCP connectivity through a NAT (network address translator) device or firewall.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-157">Включить журнал переадресации звонков</span><span class="sxs-lookup"><span data-stu-id="30f6e-157">Enable forward call history</span></span></p></td>
<td><p><span data-ttu-id="30f6e-158">ForwardCallHistory</span><span class="sxs-lookup"><span data-stu-id="30f6e-158">ForwardCallHistory</span></span></p></td>
<td><p><span data-ttu-id="30f6e-159">Означает, будет ли переадресовываться по магистральному каналу сведения о журнале звонков.</span><span class="sxs-lookup"><span data-stu-id="30f6e-159">Indicates whether call history information will be forwarded through the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-160">Включить данные переадресации P-Asserted-Identity</span><span class="sxs-lookup"><span data-stu-id="30f6e-160">Enable forward P-Asserted-Identity data</span></span></p></td>
<td><p><span data-ttu-id="30f6e-161">ForwardPAI</span><span class="sxs-lookup"><span data-stu-id="30f6e-161">ForwardPAI</span></span></p></td>
<td><p><span data-ttu-id="30f6e-p110">Указывает, будет ли переадресовываться заголовок P-Asserted-Identity (PAI) одновременно с вызовом. Заголовок PAI предоставляет способ проверки удостоверения абонемента.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p110">Indicates whether the P-Asserted-Identity (PAI) header will be forwarded along with the call. The PAI header provides a way to verify the identity of the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-164">Включить таймер отработки отказа внешней маршрутизации</span><span class="sxs-lookup"><span data-stu-id="30f6e-164">Enable outbound routing failover timer</span></span></p></td>
<td><p><span data-ttu-id="30f6e-165">EnableFastFailoverTimer</span><span class="sxs-lookup"><span data-stu-id="30f6e-165">EnableFastFailoverTimer</span></span></p></td>
<td><p><span data-ttu-id="30f6e-p111">Указывает, будут ли вызовы, на которые не был получен ответ от шлюза в течение 10 секунд, маршрутизироваться следующей доступной магистральной линии связи; если дополнительная магистральная линия связи отсутствует, вызов будет автоматически пропущен. В организации с медленными ответами сетей и шлюзов, это может приводить к необязательному пропуску вызовов.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p111">Indicates whether outbound calls that are not answered by the gateway within 10 seconds will be routed to the next available trunk; if there are no additional trunks then the call will automatically be dropped. In an organization with slow networks and gateway responses, that could potentially result in calls being dropped unnecessarily.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-168">Связанные использования ТСОП</span><span class="sxs-lookup"><span data-stu-id="30f6e-168">Associated PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="30f6e-169">PSTNUsages</span><span class="sxs-lookup"><span data-stu-id="30f6e-169">PSTNUsages</span></span></p></td>
<td><p><span data-ttu-id="30f6e-170">Коллекция режимов PSTN, привязываемых к магистральному каналу.</span><span class="sxs-lookup"><span data-stu-id="30f6e-170">Collection of PSTN usages assigned to the trunk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-171">Преобразованный номер для проверки</span><span class="sxs-lookup"><span data-stu-id="30f6e-171">Translated number to test</span></span></p></td>
<td><p><span data-ttu-id="30f6e-172">Н/Д</span><span class="sxs-lookup"><span data-stu-id="30f6e-172">N/A</span></span></p></td>
<td><p><span data-ttu-id="30f6e-173">Телефонный номер, который может использоваться для выполнения специального теста настроек конфигурации магистрали.</span><span class="sxs-lookup"><span data-stu-id="30f6e-173">Phone number that can be used to do an ad hoc test of the trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-174">Связанные правила преобразования</span><span class="sxs-lookup"><span data-stu-id="30f6e-174">Associated translation rules</span></span></p></td>
<td><p><span data-ttu-id="30f6e-175">OutboundTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="30f6e-175">OutboundTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="30f6e-176">Коллекция правил преобразования телефонных номеров, которые применяются к вызовам, обрабатываемым службой маршрутизации исходящих вызовов (вызовы, направляемые по конечным адресам УАТС или ТСОП).</span><span class="sxs-lookup"><span data-stu-id="30f6e-176">Collection of phone number translation rules that apply to calls handled by Outbound Routing (calls routed to PBX or PSTN destinations).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-177">Правила преобразования вызываемого номера</span><span class="sxs-lookup"><span data-stu-id="30f6e-177">Called number translation rules</span></span></p></td>
<td><p><span data-ttu-id="30f6e-178">OutboundCallingNumberTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="30f6e-178">OutboundCallingNumberTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="30f6e-179">Коллекция правил преобразования исходящих вызовов, привязываемая к магистральному каналу.</span><span class="sxs-lookup"><span data-stu-id="30f6e-179">Collection of outbound calling number translation rules assigned to the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-180">Проверяемый номер телефона</span><span class="sxs-lookup"><span data-stu-id="30f6e-180">Phone number to test</span></span></p></td>
<td><p><span data-ttu-id="30f6e-181">Н/Д</span><span class="sxs-lookup"><span data-stu-id="30f6e-181">N/A</span></span></p></td>
<td><p><span data-ttu-id="30f6e-182">Номер телефона, который может использоваться для выполнения специального теста правил преобразования.</span><span class="sxs-lookup"><span data-stu-id="30f6e-182">Phone number that can be used to do an ad hoc test of the translation rules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f6e-183">Номер вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="30f6e-183">Calling number</span></span></p></td>
<td><p><span data-ttu-id="30f6e-184">Н/Д</span><span class="sxs-lookup"><span data-stu-id="30f6e-184">N/A</span></span></p></td>
<td><p><span data-ttu-id="30f6e-185">Показывает, что проверяемый номер телефона является номером телефона вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="30f6e-185">Indicates that the phone number to test is the phone number of the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f6e-186">Вызываемый номер</span><span class="sxs-lookup"><span data-stu-id="30f6e-186">Called number</span></span></p></td>
<td><p><span data-ttu-id="30f6e-187">Н/Д</span><span class="sxs-lookup"><span data-stu-id="30f6e-187">N/A</span></span></p></td>
<td><p><span data-ttu-id="30f6e-188">Показывает, что проверяемый номер телефона является номером телефона вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="30f6e-188">Indicates that the phone number to test is the phone number of the person being called.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="30f6e-189">Командлеты Lync Server CsTrunkConfiguration поддерживают дополнительные свойства, не отображаемые на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="30f6e-189">The Lync Server CsTrunkConfiguration cmdlets support additional properties not shown in Lync Server Control Panel.</span></span> <span data-ttu-id="30f6e-190">Дополнительные сведения можно найти в разделе справки по командлету <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsTrunkConfiguration">Set-CsTrunkConfiguration</A> .</span><span class="sxs-lookup"><span data-stu-id="30f6e-190">For more information, see the help topic for the <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsTrunkConfiguration">Set-CsTrunkConfiguration</A> cmdlet.</span></span>



</div>

<div>

## <a name="to-modify-sip-trunk-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="30f6e-191">Изменение параметров конфигурации магистральной магистрали SIP с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="30f6e-191">To modify SIP trunk configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="30f6e-192">На панели управления Lync Server нажмите кнопку **Маршрутизация голоса** и выберите пункт **Настройка магистрали**.</span><span class="sxs-lookup"><span data-stu-id="30f6e-192">In Lync Server Control Panel, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="30f6e-p113">На вкладке **Конфигурация линии связи** дважды щелкните параметры, которые нужно изменить. Обратите внимание, что можно изменить только одну коллекция настроек за раз. Если вы хотите изменить несколько коллекций, используйте Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p113">On the **Trunk Configuration** tab, double-click the trunk configuration settings to be modified. Note that you can only edit one collection of settings at a time. If you would like to make the same changes on multiple collections, use Windows PowerShell instead.</span></span>

3.  <span data-ttu-id="30f6e-196">Выберите нужные параметры в диалоговом окне **Изменение конфигурации линии связи** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="30f6e-196">In the **Edit Trunk Configuration** dialog, make the appropriate selections and then click **OK**.</span></span>

4.  <span data-ttu-id="30f6e-p114">Свойство **Состояние** для коллекции будет обновлено до **Не сохранено**. Чтобы зафиксировать изменения и удалить коллекцию, щелкните **Сохранить**, а затем выберите **Сохранить все**.</span><span class="sxs-lookup"><span data-stu-id="30f6e-p114">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

5.  <span data-ttu-id="30f6e-199">В диалоговом окне **Несохраненные параметры настройки голосовой связи** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="30f6e-199">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="30f6e-200">В диалоговом окне " **Панель управления" Microsoft Lync Server 2013** нажмите кнопку " **ОК**".</span><span class="sxs-lookup"><span data-stu-id="30f6e-200">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

<span data-ttu-id="30f6e-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30f6e-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

