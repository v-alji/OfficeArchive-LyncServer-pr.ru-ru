---
title: 'Lync Server 2013: шифрование'
description: 'Lync Server 2013: шифрование.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Encryption for Lync Server 2013
ms:assetid: d18c74a6-385b-407b-98eb-0d525fa38fea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481135(v=OCS.15)
ms:contentKeyID: 59893874
ms.date: 09/14/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ab2c46af16cfdbb9a01631777e65219acb2ceb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428722"
---
# <a name="encryption-for-lync-server-2013"></a><span data-ttu-id="55462-103">Шифрование для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55462-103">Encryption for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55462-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55462-104">

<span> </span></span></span>

<span data-ttu-id="55462-105">_**Тема последнего изменения:** 2017-09-14_</span><span class="sxs-lookup"><span data-stu-id="55462-105">_**Topic Last Modified:** 2017-09-14_</span></span>

<span data-ttu-id="55462-106">Microsoft Lync Server 2013 использует TLS и MTLS для шифрования мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="55462-106">Microsoft Lync Server 2013 uses TLS and MTLS to encrypt instant messages.</span></span> <span data-ttu-id="55462-107">Весь межсерверный трафик требует использования MTLS независимо от того, ограничен ли трафик внутренней сетью или пересекает периметр внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="55462-107">All server-to-server traffic requires MTLS, regardless of whether the traffic is confined to the internal network or crosses the internal network perimeter.</span></span> <span data-ttu-id="55462-108">TLS является необязательным, но настоятельно рекомендуется между сервером и шлюзом мультимедийных обновлений.</span><span class="sxs-lookup"><span data-stu-id="55462-108">TLS is optional but strongly recommended between the Mediation Server and media gateway.</span></span> <span data-ttu-id="55462-109">If TLS is configured on this link, MTLS is required.</span><span class="sxs-lookup"><span data-stu-id="55462-109">If TLS is configured on this link, MTLS is required.</span></span> <span data-ttu-id="55462-110">Таким образом, шлюз должен быть настроен на сертификат от центра сертификации, которому доверяет сервер-посредник.</span><span class="sxs-lookup"><span data-stu-id="55462-110">Therefore, the gateway must be configured with a certificate from a CA that is trusted by the Mediation Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="55462-111">Советы по безопасности в отношении SSL 3.0 были опубликованы в 2014 г.</span><span class="sxs-lookup"><span data-stu-id="55462-111">A security advisory regarding SSL 3.0 was published in 2014.</span></span> <span data-ttu-id="55462-112">Отключение SSL 3,0 в Lync Server 2013 является поддерживаемым вариантом.</span><span class="sxs-lookup"><span data-stu-id="55462-112">Disabling SSL 3.0 in Lync Server 2013 is a supported option.</span></span> <span data-ttu-id="55462-113">Дополнительные сведения о рекомендациях по безопасности можно найти в разделе <A class=uri href="https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/">https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/</A> .</span><span class="sxs-lookup"><span data-stu-id="55462-113">To learn more about the security advisory, see <A class=uri href="https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/">https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/</A>.</span></span>



</div>

<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="разрешения" alt="security" /><span data-ttu-id="55462-115">Примечание о безопасности:</span><span class="sxs-lookup"><span data-stu-id="55462-115">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55462-116">Для обеспечения использования наиболее надежного криптографических протоколов Lync Server 2013 предлагает клиентам протоколы TLS Encryption в следующем порядке: <strong>tls 1,2</strong> , <strong>TLS 1,1</strong>, <strong>TLS 1,0</strong>.</span><span class="sxs-lookup"><span data-stu-id="55462-116">To ensure the strongest cryptographic protocol is used, Lync Server 2013 will offer TLS encryption protocols in the following order to clients: <strong>TLS 1.2</strong> , <strong>TLS 1.1</strong>, <strong>TLS 1.0</strong>.</span></span> <span data-ttu-id="55462-117">Протокол TLS является важнейшим аспектом Lync Server 2013, поэтому он необходим для поддержки поддерживаемой среды.</span><span class="sxs-lookup"><span data-stu-id="55462-117">TLS is a critical aspect of Lync Server 2013 and thus it is required in order to maintain a supported environment.</span></span></td>
</tr>
</tbody>
</table>


</div>

<span data-ttu-id="55462-118">Требования к трафику "клиент-клиент" зависят от того, пересекает ли этот трафик внутренний корпоративный брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="55462-118">Requirements for client-to-client traffic depend on whether that traffic crosses the internal corporate firewall.</span></span> <span data-ttu-id="55462-119">Строго внутренний трафик может использовать TLS, и в этом случае обмен мгновенными сообщениями будет шифроваться или TCP, в этом случае это не так.</span><span class="sxs-lookup"><span data-stu-id="55462-119">Strictly internal traffic can use either TLS, in which case the instant message is encrypted, or TCP, in which case it is not.</span></span>

<span data-ttu-id="55462-120">В следующей таблице представлена сводка требований протокола для каждого типа трафика.</span><span class="sxs-lookup"><span data-stu-id="55462-120">The following table summarizes the protocol requirements for each type of traffic.</span></span>

### <a name="traffic-protection"></a><span data-ttu-id="55462-121">Защита трафика</span><span class="sxs-lookup"><span data-stu-id="55462-121">Traffic Protection</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55462-122">Тип трафика</span><span class="sxs-lookup"><span data-stu-id="55462-122">Traffic type</span></span></th>
<th><span data-ttu-id="55462-123">Защита</span><span class="sxs-lookup"><span data-stu-id="55462-123">Protected by</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55462-124">Сервер-сервер</span><span class="sxs-lookup"><span data-stu-id="55462-124">Server-to-server</span></span></p></td>
<td><p><span data-ttu-id="55462-125">MTLS</span><span class="sxs-lookup"><span data-stu-id="55462-125">MTLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55462-126">Клиент-сервер</span><span class="sxs-lookup"><span data-stu-id="55462-126">Client-to-server</span></span></p></td>
<td><p><span data-ttu-id="55462-127">TLS</span><span class="sxs-lookup"><span data-stu-id="55462-127">TLS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55462-128">Мгновенные сообщения и присутствие</span><span class="sxs-lookup"><span data-stu-id="55462-128">Instant messaging and presence</span></span></p></td>
<td><p><span data-ttu-id="55462-129">TLS (если настроено для TLS)</span><span class="sxs-lookup"><span data-stu-id="55462-129">TLS (if configured for TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55462-130">Аудио/видео и рабочий стол для общего доступа к мультимедиа</span><span class="sxs-lookup"><span data-stu-id="55462-130">Audio and video and desktop sharing of media</span></span></p></td>
<td><p><span data-ttu-id="55462-131">SRTP</span><span class="sxs-lookup"><span data-stu-id="55462-131">SRTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55462-132">Общий доступ к рабочему столу (передача сигналов)</span><span class="sxs-lookup"><span data-stu-id="55462-132">Desktop sharing (signaling)</span></span></p></td>
<td><p><span data-ttu-id="55462-133">TLS</span><span class="sxs-lookup"><span data-stu-id="55462-133">TLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55462-134">веб-конференции</span><span class="sxs-lookup"><span data-stu-id="55462-134">Web conferencing</span></span></p></td>
<td><p><span data-ttu-id="55462-135">TLS</span><span class="sxs-lookup"><span data-stu-id="55462-135">TLS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55462-136">Загрузка содержимого собрания, загрузка адресной книги, расширение группы рассылки</span><span class="sxs-lookup"><span data-stu-id="55462-136">Meeting content download, address book download, distribution group expansion</span></span></p></td>
<td><p><span data-ttu-id="55462-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="55462-137">HTTPS</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="media-encryption"></a><span data-ttu-id="55462-138">Шифрование мультимедиа</span><span class="sxs-lookup"><span data-stu-id="55462-138">Media Encryption</span></span>

<span data-ttu-id="55462-139">Трафик мультимедиа шифруется по протоколу SRTP, профилю протокола RTP, который обеспечивает конфиденциальность, проверку подлинности и защиту от атак с повторением пакетов для трафика RTP.</span><span class="sxs-lookup"><span data-stu-id="55462-139">Media traffic is encrypted using Secure RTP (SRTP), a profile of Real-Time Transport Protocol (RTP) that provides confidentiality, authentication, and replay attack protection to RTP traffic.</span></span> <span data-ttu-id="55462-140">Кроме того, потоки мультимедиа в обоих направлениях между сервером-посредником и его внутренним узлом следующего прыжка также шифруются с помощью SRTP.</span><span class="sxs-lookup"><span data-stu-id="55462-140">In addition, media flowing in both directions between the Mediation Server and its internal next hop is also encrypted using SRTP.</span></span> <span data-ttu-id="55462-141">Поток мультимедиа в обоих направлениях между сервером-посредником и шлюзом мультимедиа по умолчанию не шифруется.</span><span class="sxs-lookup"><span data-stu-id="55462-141">Media flowing in both directions between the Mediation Server and a media gateway is not encrypted by default.</span></span> <span data-ttu-id="55462-142">Сервер-посредник может обеспечивать шифрование на медиашлюзе, однако шлюз должен поддерживать MTLS и хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="55462-142">The Mediation Server can support encryption to the media gateway, but the gateway must support MTLS and storage of a certificate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="55462-143">Аудио/видео (A/V) поддерживается новой версией Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="55462-143">Audio/Video (A/V) is supported with the new version of Windows Live Messenger.</span></span> <span data-ttu-id="55462-144">Если вы реализуете Федерацию/V с Windows Live Messenger, необходимо также изменить уровень шифрования Lync Server.</span><span class="sxs-lookup"><span data-stu-id="55462-144">If you are implementing A/V federation with Windows Live Messenger, you must also modify the Lync Server encryption level.</span></span> <span data-ttu-id="55462-145">By default, the encryption level is Required.</span><span class="sxs-lookup"><span data-stu-id="55462-145">By default, the encryption level is Required.</span></span> <span data-ttu-id="55462-146">Вы должны изменить этот параметр так, чтобы он поддерживался с помощью командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="55462-146">You must change this setting to Supported by using the Lync Server Management Shell.</span></span> <span data-ttu-id="55462-147">Дополнительные сведения можно найти <A href="lync-server-2013-deploying-external-user-access.md">в разделе Развертывание внешних пользователей Access в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="55462-147">For more information, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="55462-148">Трафик аудио и видеофайла не шифруется между клиентами Microsoft Lync 2013 и Windows Live.</span><span class="sxs-lookup"><span data-stu-id="55462-148">Audio and video media traffic is not encrypted between Microsoft Lync 2013 and Windows Live clients.</span></span>

</div>

<div>

## <a name="fips"></a><span data-ttu-id="55462-149">FIPS</span><span class="sxs-lookup"><span data-stu-id="55462-149">FIPS</span></span>

<span data-ttu-id="55462-150">Lync Server 2013 и Microsoft Exchange Server 2013 работают с поддержкой алгоритмов стандартизации стандарта обработки информации (FIPS) 140-2, если серверные операционные системы Windows настроены на использование алгоритмов FIPS 140-2 для системы криптографии.</span><span class="sxs-lookup"><span data-stu-id="55462-150">Lync Server 2013 and Microsoft Exchange Server 2013 operate with support for Federal Information Processing Standard (FIPS) 140-2 algorithms if the Windows Server operating systems are configured to use the FIPS 140-2 algorithms for system cryptography.</span></span> <span data-ttu-id="55462-151">Для реализации поддержки FIPS необходимо настроить каждый сервер, на котором работает Lync Server 2013, чтобы его поддерживать.</span><span class="sxs-lookup"><span data-stu-id="55462-151">To implement FIPS support, you must configure each server running Lync Server 2013 to support it.</span></span> <span data-ttu-id="55462-152">Подробнее об использовании алгоритмов, совместимых с FIPS, и о том, как реализовать поддержку FIPS, можно найти в статье 811833 базы знаний Майкрософт, которая влияет на параметры безопасности "Системная криптография: использование алгоритмов, совместимых с FIPS для шифрования, хеширования и подписи" в Windows XP и более поздних версиях Windows [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833) .</span><span class="sxs-lookup"><span data-stu-id="55462-152">For details about the use of FIPS-compliant algorithms and how to implement FIPS support, see Microsoft Knowledge Base article 811833, The effects of enabling the “System cryptography: Use FIPS compliant algorithms for encryption, hashing, and signing" security setting in Windows XP and in later versions of Windows at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833).</span></span> <span data-ttu-id="55462-153">Дополнительные сведения о поддержке FIPS 140-2 и ограничениях в Exchange 2010 можно найти в статьях Exchange 2010 SP1 и поддержка алгоритмов, совместимых с FIPS [https://go.microsoft.com/fwlink/p/?LinkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335) .</span><span class="sxs-lookup"><span data-stu-id="55462-153">For details about FIPS 140-2 support and limitations in Exchange 2010, see Exchange 2010 SP1 and Support for FIPS Compliant Algorithms at [https://go.microsoft.com/fwlink/p/?LinkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335).</span></span>

<span data-ttu-id="55462-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55462-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

