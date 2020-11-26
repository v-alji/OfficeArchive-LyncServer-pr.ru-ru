---
title: 'Lync Server 2013: Настройка диапазонов портов для конференций, приложений и серверов-исправлений'
description: 'Lync Server 2013: Настройка диапазонов портов для конференций, приложений и серверов-исправлений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Conferencing, Application, and Mediation servers
ms:assetid: 4d6eaa5d-0127-453f-be6a-e55384772d83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204872(v=OCS.15)
ms:contentKeyID: 48184074
ms.date: 05/01/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eb3f51e42c86b667b6990f41640bf09e12e840c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432760"
---
# <a name="configuring-port-ranges-in-lync-server-2013-for-your-conferencing-application-and-mediation-servers"></a><span data-ttu-id="69591-103">Настройка диапазонов портов в Lync Server 2013 для конференций, приложений и серверов-исправлений</span><span class="sxs-lookup"><span data-stu-id="69591-103">Configuring port ranges in Lync Server 2013 for your Conferencing, Application, and Mediation servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69591-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69591-104">

<span> </span></span></span>

<span data-ttu-id="69591-105">_**Тема последнего изменения:** 2015-04-30_</span><span class="sxs-lookup"><span data-stu-id="69591-105">_**Topic Last Modified:** 2015-04-30_</span></span>

<span data-ttu-id="69591-106">Для реализации качества обслуживания следует настроить идентичные диапазоны портов для голосовой связи, видео и совместного использования приложений на серверах конференций, приложений и исправлений. Кроме того, эти диапазоны портов не должны перекрываться.</span><span class="sxs-lookup"><span data-stu-id="69591-106">In order to implement Quality of Service, you should configure identical port ranges for audio, video, and application sharing on your Conferencing, Application, and Mediation servers; furthermore, those port ranges must not overlap in any way.</span></span> <span data-ttu-id="69591-107">Чтобы использовать простой пример, предположим, что вы используете порты 10000 – 10999 для видео на серверах конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="69591-107">To use a simple example, suppose you use ports 10000 through 10999 for video on your Conferencing servers.</span></span> <span data-ttu-id="69591-108">Это означает, что вы также должны резервировать порты 10000 – 10999 для видео на серверах приложений и исправлений.</span><span class="sxs-lookup"><span data-stu-id="69591-108">That means that you must also reserve ports 10000 through 10999 for video on your Application and Mediation servers.</span></span> <span data-ttu-id="69591-109">В противном случае качество обслуживания не будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="69591-109">If you do not, QoS will not work as expected.</span></span>

<span data-ttu-id="69591-110">Аналогичным образом, предположим, что вы резервируете порты 10000 – 10999 для видео, а затем Зарезервируйте порты 10500 – 11999 для звука.</span><span class="sxs-lookup"><span data-stu-id="69591-110">Similarly, suppose you reserve ports 10000 through 10999 for video, but then reserve ports 10500 through 11999 for audio.</span></span> <span data-ttu-id="69591-111">Это может создавать проблемы со службой качества обслуживания, так как диапазоны портов перекрываются.</span><span class="sxs-lookup"><span data-stu-id="69591-111">This can create problems for Quality of Service, because the port ranges overlap.</span></span> <span data-ttu-id="69591-112">При использовании QoS у каждого модальности должен быть уникальный набор портов: Если вы используете порты 10000 – 10999 для видео, вам придется использовать другой диапазон (например, с 11000 по 11999 для звука).</span><span class="sxs-lookup"><span data-stu-id="69591-112">With QoS, each modality must have a unique set of ports: if you use ports 10000 through 10999 for video, then you'll have to use a different range (for example, 11000 through 11999 for audio).</span></span>

<span data-ttu-id="69591-113">По умолчанию диапазоны звуковых и видеопортов не перекрываются в Microsoft Lync Server 2013; Однако диапазоны портов, назначаемые для общего разделения приложений, перекрываются с диапазонами звуковых и видеопортов.</span><span class="sxs-lookup"><span data-stu-id="69591-113">By default, audio and video port ranges do not overlap in Microsoft Lync Server 2013; however, the port ranges assigned to application sharing overlap with both the audio and video port ranges.</span></span> <span data-ttu-id="69591-114">(В свою очередь, это означает, что ни один из этих диапазонов не уникален.) Вы можете проверить существующие диапазоны портов для серверов конференций, приложений и исправлений, запустив в командной консоли Lync Server 2013 следующие три команды:</span><span class="sxs-lookup"><span data-stu-id="69591-114">(Which, in turn, means that none of these ranges are unique.) You can verify the existing port ranges for your Conferencing, Application, and Mediation servers by running the following three commands from within the Lync Server 2013 Management Shell:</span></span>

    Get-CsService -ConferencingServer | Select-Object Identity, AudioPortStart, AudioPortCount, VideoPortStart, VideoPortCount, AppSharingPortStart, AppSharingPortCount
    
    Get-CsService -ApplicationServer | Select-Object Identity, AudioPortStart, AudioPortCount
    
    Get-CsService -MediationServer | Select-Object Identity, AudioPortStart, AudioPortCount

<div>


> [!WARNING]  
> <span data-ttu-id="69591-115">Как видно из предыдущих команд, для каждого типа порта — звук, видео и общий доступ к приложениям — каждому из них назначается два отдельных значения: начало порта и число портов.</span><span class="sxs-lookup"><span data-stu-id="69591-115">As you can see in the preceding commands, each port type – audio, video, and application sharing – is assigned two separate property values: the port start and the port count.</span></span> <span data-ttu-id="69591-116">Начало порта указывает первый порт, используемый для этого модального. Например, если начало звукового порта равно 50000, то первым портом, используемым для звукового трафика, является порт 50000.</span><span class="sxs-lookup"><span data-stu-id="69591-116">The port start indicates the first port used for that modality; for example, if the audio port start is equal to 50000 that means that the first port used for audio traffic is port 50000.</span></span> <span data-ttu-id="69591-117">Если счетчик звуковых портов равен 2 (то есть не является допустимым значением, но используется здесь для иллюстрации), это означает, что для звука выделено только 2 порта.</span><span class="sxs-lookup"><span data-stu-id="69591-117">If the audio port count is 2 (which is not a valid value, but is used here for illustration purposes) that means that only 2 ports are allocated for audio.</span></span> <span data-ttu-id="69591-118">Если первый порт является портом 50000 и есть два порта, это означает, что второй порт должен быть портом 50001 (диапазоны портов должны быть непрерывными).</span><span class="sxs-lookup"><span data-stu-id="69591-118">If the first port is port 50000 and there are a total of two ports, that means the second port must be port 50001 (port ranges have to be contiguous).</span></span> <span data-ttu-id="69591-119">Как следствие, диапазон портов для звука — порты 50000 – 50001 включительно.</span><span class="sxs-lookup"><span data-stu-id="69591-119">As a result, the port range for audio would be ports 50000 through 50001, inclusive.</span></span><BR><span data-ttu-id="69591-120">Обратите внимание, что сервер приложений и сервер исправлений поддерживают только QoS для звука; Вам не нужно изменять порты общего использования видео или приложений на серверах приложений или серверах исправлений.</span><span class="sxs-lookup"><span data-stu-id="69591-120">Note, too that Application server and Mediation server only support QoS for audio; you do not need to change video or application sharing ports in your Application servers or Mediation servers.</span></span>



</div>

<span data-ttu-id="69591-121">Если вы запустили три команды, вы увидите, что значения порта по умолчанию для Lync Server 2013 настраиваются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="69591-121">If you run the preceding three commands you'll see that the default port values for Lync Server 2013 are configured like this:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69591-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="69591-122">Property</span></span></th>
<th><span data-ttu-id="69591-123">Сервер конференц-связи</span><span class="sxs-lookup"><span data-stu-id="69591-123">Conferencing Server</span></span></th>
<th><span data-ttu-id="69591-124">Сервер приложений</span><span class="sxs-lookup"><span data-stu-id="69591-124">Application Server</span></span></th>
<th><span data-ttu-id="69591-125">Сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="69591-125">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69591-126">AudioPortStart</span><span class="sxs-lookup"><span data-stu-id="69591-126">AudioPortStart</span></span></p></td>
<td><p><span data-ttu-id="69591-127">49152</span><span class="sxs-lookup"><span data-stu-id="69591-127">49152</span></span></p></td>
<td><p><span data-ttu-id="69591-128">49152</span><span class="sxs-lookup"><span data-stu-id="69591-128">49152</span></span></p></td>
<td><p><span data-ttu-id="69591-129">49152</span><span class="sxs-lookup"><span data-stu-id="69591-129">49152</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69591-130">AudioPortCount</span><span class="sxs-lookup"><span data-stu-id="69591-130">AudioPortCount</span></span></p></td>
<td><p><span data-ttu-id="69591-131">8348</span><span class="sxs-lookup"><span data-stu-id="69591-131">8348</span></span></p></td>
<td><p><span data-ttu-id="69591-132">8348</span><span class="sxs-lookup"><span data-stu-id="69591-132">8348</span></span></p></td>
<td><p><span data-ttu-id="69591-133">8348</span><span class="sxs-lookup"><span data-stu-id="69591-133">8348</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69591-134">VideoPortStart</span><span class="sxs-lookup"><span data-stu-id="69591-134">VideoPortStart</span></span></p></td>
<td><p><span data-ttu-id="69591-135">57501</span><span class="sxs-lookup"><span data-stu-id="69591-135">57501</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69591-136">VideoPortCount</span><span class="sxs-lookup"><span data-stu-id="69591-136">VideoPortCount</span></span></p></td>
<td><p><span data-ttu-id="69591-137">8034</span><span class="sxs-lookup"><span data-stu-id="69591-137">8034</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69591-138">ApplicationSharingPortStart</span><span class="sxs-lookup"><span data-stu-id="69591-138">ApplicationSharingPortStart</span></span></p></td>
<td><p><span data-ttu-id="69591-139">49152</span><span class="sxs-lookup"><span data-stu-id="69591-139">49152</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69591-140">ApplicationSharingPortCount</span><span class="sxs-lookup"><span data-stu-id="69591-140">ApplicationSharingPortCount</span></span></p></td>
<td><p><span data-ttu-id="69591-141">16383</span><span class="sxs-lookup"><span data-stu-id="69591-141">16383</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69591-142">Как отмечалось ранее, при настройке портов сервера Lync Server для QoS вы должны убедиться, что: 1) параметры звукового порта идентичны на серверах конференций, приложений и исправлений. и 2) диапазоны портов не перекрываются.</span><span class="sxs-lookup"><span data-stu-id="69591-142">As noted previously, when configuring Lync Server ports for QoS, you should ensure that: 1) audio port settings are identical across yours Conferencing, Application, and Mediation servers; and, 2) port ranges do not overlap.</span></span> <span data-ttu-id="69591-143">Если вы внимательно посмотрите на приведенную выше таблицу, вы увидите, что диапазоны портов идентичны для трех типов серверов.</span><span class="sxs-lookup"><span data-stu-id="69591-143">If you look closely at the preceding table, you will see that the port ranges are identical across the three server types.</span></span> <span data-ttu-id="69591-144">Например, для начального звукового порта установлен порт 49152 на каждом из типов серверов, а общее количество портов, зарезервированных для звука на каждом сервере, также совпадает: 8348.</span><span class="sxs-lookup"><span data-stu-id="69591-144">For example, the starting audio port is set to port 49152 on each server type, and the total number of ports reserved for audio in each server is also identical: 8348.</span></span> <span data-ttu-id="69591-145">Однако диапазоны портов перекрываются: Аудиопорты начинаются с порта 49152, но это значит, что порты можно настроить для совместного использования приложений.</span><span class="sxs-lookup"><span data-stu-id="69591-145">However, the port ranges overlap: audio ports start at port 49152, but so do the ports set aside for application sharing.</span></span> <span data-ttu-id="69591-146">Чтобы обеспечить оптимальное использование качества обслуживания, необходимо повторно настроить общий доступ к приложениям, чтобы использовать уникальный диапазон портов.</span><span class="sxs-lookup"><span data-stu-id="69591-146">In order to make optimal use of Quality of Service, application sharing should be reconfigured to use a unique port range.</span></span> <span data-ttu-id="69591-147">Например, можно настроить общий доступ к приложениям с порта 40803 и использовать порт 8348.</span><span class="sxs-lookup"><span data-stu-id="69591-147">For example, you could configure application sharing to start at port 40803 and to use 8348 ports.</span></span> <span data-ttu-id="69591-148">(Зачем 8348 порт?</span><span class="sxs-lookup"><span data-stu-id="69591-148">(Why 8348 ports?</span></span> <span data-ttu-id="69591-149">Если вы добавите эти значения вместе--40803 + 8348--это значит, что общий доступ к приложениям будет использовать порты 40803 через порт 49150.</span><span class="sxs-lookup"><span data-stu-id="69591-149">If you add those values together -- 40803 + 8348 -- that means that application sharing will use ports 40803 through port 49150.</span></span> <span data-ttu-id="69591-150">Так как порты не начинаются с порта 49152, перекрывающиеся диапазоны портов больше не будут перекрываться.)</span><span class="sxs-lookup"><span data-stu-id="69591-150">Because audio ports do not begin until port 49152, you will no longer have any overlapping port ranges.)</span></span>

<span data-ttu-id="69591-151">После выбора нового диапазона портов для совместного использования приложений вы можете внести изменения с помощью командлета Set-CsConferencingServer.</span><span class="sxs-lookup"><span data-stu-id="69591-151">After you have selected the new port range for application sharing you can make your change by using the Set-CsConferencingServer cmdlet.</span></span> <span data-ttu-id="69591-152">Это изменение не нужно вносить на серверах приложений или на серверах-посредниках, так как эти серверы не обрабатывают трафик общего обмена приложениями.</span><span class="sxs-lookup"><span data-stu-id="69591-152">This change does not need to be made on your Application servers or on your Mediation servers, because these servers do not handle application sharing traffic.</span></span> <span data-ttu-id="69591-153">Если вы решите переназначить порты, используемые для звукового трафика, вам нужно изменить только значения порта на этих серверах.</span><span class="sxs-lookup"><span data-stu-id="69591-153">You only need to change port values on these servers if you decide to reassign the ports used for audio traffic.</span></span>

<span data-ttu-id="69591-154">Чтобы изменить значения портов для совместного использования приложений на одном сервере конференц-связи, выполните в командной консоли Lync Server следующую команду:</span><span class="sxs-lookup"><span data-stu-id="69591-154">To modify the port values for application sharing on a single Conferencing server run a command similar to this from within the Lync Server Management Shell:</span></span>

    Set-CsConferenceServer -Identity ConferencingServer:atl-cs-001.litwareinc.com -AppSharingPortStart 40803 -AppSharingPortCount 8348

<span data-ttu-id="69591-155">Если вы хотите внести эти изменения на всех серверах конференц-связи, вы можете выполнить эту команду:</span><span class="sxs-lookup"><span data-stu-id="69591-155">If you want to make these changes on all your Conferencing servers you can run this command instead:</span></span>

    Get-CsService -ConferencingServer | ForEach-Object {Set-CsConferenceServer -Identity $_.Identity -AppSharingPortStart 40803 -AppSharingPortCount 8348}

<span data-ttu-id="69591-156">После изменения параметров порта следует остановить, а затем перезапустить каждую службу, на которую повлияли изменения.</span><span class="sxs-lookup"><span data-stu-id="69591-156">After changing port settings you should stop and then restart each service affected by the changes.</span></span>

<span data-ttu-id="69591-157">Не обязательно, чтобы сервер конференц-связи, серверы приложений и серверы исправлений совместно применялись к одному и тому же диапазону портов; единственное истинное требование состоит в том, что вы настроили уникальные диапазоны портов на всех серверах.</span><span class="sxs-lookup"><span data-stu-id="69591-157">It is not mandatory that your Conferencing servers, Application servers, and Mediation servers share the exact same port range; the only true requirement is that you set aside unique port ranges on all your servers.</span></span> <span data-ttu-id="69591-158">Тем не менее, администрирование обычно будет проще, если вы используете один и тот же набор портов на всех серверах.</span><span class="sxs-lookup"><span data-stu-id="69591-158">However, administration will typically be easier if you use the same set of ports on all your servers.</span></span>

<span data-ttu-id="69591-159"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69591-159"></div>

<span> </span>

</div>

</div>

</span></span></div>

