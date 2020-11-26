---
title: 'Общие сведения о сертификате: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями'
description: 'Сведения о сертификате: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - SIP, XMPP federation, and public instant messaging
ms:assetid: 933d6351-cfa6-4432-b3ed-1aff3ac92065
ms:mtpsurl: https://technet.microsoft.com/library/JJ618372(v=OCS.15)
ms:contentKeyID: 49105659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565d3b935d304aa09588688bd8d71948b1b3ec3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435189"
---
# <a name="certificate-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="fd0bf-103">Общие сведения о сертификате: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd0bf-103">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd0bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd0bf-104">

<span> </span></span></span>

<span data-ttu-id="fd0bf-105">_**Тема последнего изменения:** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="fd0bf-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="fd0bf-106">Сертификаты, необходимые для Федерации с Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server, обычно удовлетворяют требованиям для настройки, запроса и назначения серверу пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-106">The certificates that you need for federating with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server will typically be met by the certificates that you configure, request and assign to your Edge Server.</span></span>

<span data-ttu-id="fd0bf-107">Требования к сертификатам для включения и установления связи с партнерами по протоколу расширенного обмена сообщениями (XMPP) требуют добавления записей для доменов XMPP.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-107">Certificate requirements for enabling and establishing communications with extensible messaging and presence protocol (XMPP) partners require addition of entries for your XMPP domains.</span></span> <span data-ttu-id="fd0bf-108">Запись, включенная в сертификат в качестве дополнительного имени субъекта (SAN), будет являться доменом, который может принимать участие в XMPP обмене сообщениями.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-108">The record that is included on the certificate as a subject alternative name (SAN) will be the domain that can participate in XMPP communications.</span></span> <span data-ttu-id="fd0bf-109">Домен может быть доменом корневого уровня (например, contoso.com), если вы хотите включить XMPP для всего домена или выбрать его дочерние домены (например, corp.contoso.com, finance.contoso.com), если вы включаете XMPP для подмножества пользователей.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-109">The domain can be the root-level domain (for example, contoso.com) if you want to enable XMPP for your entire domain, or can be selected child domains (for example, corp.contoso.com, finance.contoso.com) if you are enabling XMPP for a subset of users.</span></span>

<span data-ttu-id="fd0bf-110">Чтобы настроить сертификаты для общедоступной службы обмена мгновенными сообщениями, обратите внимание на то, что ничего не отличается от других типов Федерации SIP или даже стандартных сертификатов пограничного сервера, за исключением того, что в Skype Online (AOL) требуется, чтобы сертификат или сертификаты (в случае пограничного пула) также содержали клиентское EKU.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-110">To configure certificates for public Instant Messaging connectivity, note that there is nothing different from other SIP federation types or even standard Edge Server certificates, except that America Online (AOL) requires a the certificate or certificates (in the case of an Edge pool) to also contain the client EKU.</span></span> <span data-ttu-id="fd0bf-111">Клиентское EKU является дополнением к сертификату и является частью внешнего общедоступного сертификата, назначенного пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-111">The client EKU is an addition to the certificate, and is part of the external public certificate that is assigned to your Edge Server.</span></span>

<span data-ttu-id="fd0bf-112">Чтобы убедиться в том, что требования к сертификату для развертывания пограничного сервера выполнены правильно, ознакомьтесь с разделами, приведенными в разделе, озаглавленном **также**.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-112">To confirm that you have met the correct certificate requirements for your Edge Server deployment, review the topics listed in the section titled **See Also**.</span></span>

<div>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd0bf-113">Компонент</span><span class="sxs-lookup"><span data-stu-id="fd0bf-113">Component</span></span></th>
<th><span data-ttu-id="fd0bf-114">Имя субъекта</span><span class="sxs-lookup"><span data-stu-id="fd0bf-114">Subject name</span></span></th>
<th><span data-ttu-id="fd0bf-115">Дополнительные имена субъектов (SAN)</span><span class="sxs-lookup"><span data-stu-id="fd0bf-115">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="fd0bf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd0bf-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd0bf-117">Внешний край и доступ</span><span class="sxs-lookup"><span data-stu-id="fd0bf-117">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="fd0bf-118">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fd0bf-118">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="fd0bf-119">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fd0bf-119">sip.contoso.com</span></span></p>
<p><span data-ttu-id="fd0bf-120">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fd0bf-120">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="fd0bf-121">contoso.com</span><span class="sxs-lookup"><span data-stu-id="fd0bf-121">contoso.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="fd0bf-122">Поддержка пространства имен contoso.com XMPP</span><span class="sxs-lookup"><span data-stu-id="fd0bf-122">To support the contoso.com XMPP namespace</span></span>


<p><span data-ttu-id="fd0bf-123">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fd0bf-123">sip.fabrikam.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="fd0bf-124">Поддержка пространства имен SIP fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fd0bf-124">To support the fabrikam.com SIP namespace</span></span>


<p><span data-ttu-id="fd0bf-125">fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fd0bf-125">fabrikam.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="fd0bf-126">Поддержка пространства имен fabrikam.com XMPP</span><span class="sxs-lookup"><span data-stu-id="fd0bf-126">To support the fabrikam.com XMPP namespace</span></span>

</td>
<td><p><span data-ttu-id="fd0bf-127">Сертификат должен находиться в общедоступном центре сертификации, а также в том случае, если вы разворачиваете общедоступную службу обмена мгновенными сообщениями с AOL, и у вас должен быть серверный EKU</span><span class="sxs-lookup"><span data-stu-id="fd0bf-127">The certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="fd0bf-128">Сертификат назначается внешним интерфейсам пограничного сервера для следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="fd0bf-128">The certificate is assigned to the external Edge Server interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="fd0bf-129">доступа</span><span class="sxs-lookup"><span data-stu-id="fd0bf-129">Access Edge service</span></span></p></li>
<li><p><span data-ttu-id="fd0bf-130">веб-конференций</span><span class="sxs-lookup"><span data-stu-id="fd0bf-130">Web Conferencing Edge service</span></span></p></li>
<li><p><span data-ttu-id="fd0bf-131">передачи аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="fd0bf-131">A/V Edge service</span></span></p></li>
</ul>



> [!NOTE]
> <span data-ttu-id="fd0bf-132">Технически сертификат не назначается для A/V Edge.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-132">Technically, a certificate is not assigned to the A/V Edge.</span></span> <span data-ttu-id="fd0bf-133">Безопасная связь и проверка подлинности управляются службой проверки подлинности в Media Relay (MRAS).</span><span class="sxs-lookup"><span data-stu-id="fd0bf-133">Secure communication and authentication is managed by way of the Media Relay Authentication Service (MRAS).</span></span> <span data-ttu-id="fd0bf-134">MRAS использует сертификат, назначенный внутреннему интерфейсу пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-134">MRAS uses the certificate assigned to the Edge Server internal interface.</span></span>


<p><span data-ttu-id="fd0bf-135">Обратите внимание, что сети SAN автоматически добавляются к сертификату на основе определений в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-135">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="fd0bf-136">Вы добавляете записи SAN по мере необходимости для дополнительных доменов SIP и других элементов, которые необходимо поддерживать.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-136">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="fd0bf-137">Имя субъекта реплицируется в сети SAN и должно быть представлено для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-137">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fd0bf-138">См. также</span><span class="sxs-lookup"><span data-stu-id="fd0bf-138">See Also</span></span>


[<span data-ttu-id="fd0bf-139">Пример конфигурации XMPP в Lync Server 2013 — федерация XMPP с Google Talk</span><span class="sxs-lookup"><span data-stu-id="fd0bf-139">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="fd0bf-140">Планирование сертификатов пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd0bf-140">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  
[<span data-ttu-id="fd0bf-141">Сводка по сертификатам — единая консолидированная пограничная топология с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd0bf-141">Certificate summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)  
[<span data-ttu-id="fd0bf-142">Сводка по сертификатам — единая консолидированная пограничная топология с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd0bf-142">Certificate summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-public-ip-addresses.md)  
[<span data-ttu-id="fd0bf-143">Сводка по сертификатам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd0bf-143">Certificate summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-private-ip.md)  
[<span data-ttu-id="fd0bf-144">Сводка по сертификатам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd0bf-144">Certificate summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)  
[<span data-ttu-id="fd0bf-145">Сводка по сертификатам — масштабируемая консолидированная пограничная топология с аппаратными балансировщиками нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd0bf-145">Certificate summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)  
  

<span data-ttu-id="fd0bf-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd0bf-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

