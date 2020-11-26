---
title: 'Lync Server 2013: сведения о сертификате — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP)'
description: 'Lync Server 2013: сведения о сертификате — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: b059a34e-99df-40af-91fe-fe2aa52841f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618374(v=OCS.15)
ms:contentKeyID: 49105661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e2bb593d909c2eec6032dc89c07cc5f5b1a72db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435301"
---
# <a name="certificate-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="41364-103">Сведения о сертификате — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41364-103">Certificate summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41364-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41364-104">

<span> </span></span></span>

<span data-ttu-id="41364-105">_**Тема последнего изменения:** 2012-12-23_</span><span class="sxs-lookup"><span data-stu-id="41364-105">_**Topic Last Modified:** 2012-12-23_</span></span>

<span data-ttu-id="41364-106">Требования к сертификатам для включения и установления связи с партнерами по протоколу расширенного обмена сообщениями (XMPP) требуют дополнительной записи доменов XMPP.</span><span class="sxs-lookup"><span data-stu-id="41364-106">Certificate requirements for enabling and establishing communications with extensible messaging and presence protocol (XMPP) partners require the additional record of your XMPP domains.</span></span> <span data-ttu-id="41364-107">Запись, включенная в сертификат в качестве дополнительного имени субъекта (SAN), будет являться доменом, который может принимать участие в XMPP обмене сообщениями.</span><span class="sxs-lookup"><span data-stu-id="41364-107">The record that is included on the certificate as a subject alternative name (SAN) will be the domain that can participate in XMPP communications.</span></span> <span data-ttu-id="41364-108">Домен может быть доменом корневого уровня (например, contoso.com), если вы хотите включить XMPP для всего домена или выбрать его дочерние домены (например, corp.contoso.com, finance.contoso.com), если вы включаете XMPP для подмножества пользователей.</span><span class="sxs-lookup"><span data-stu-id="41364-108">The domain can be the root-level domain (for example, contoso.com) if you want to enable XMPP for your entire domain, or can be selected child domains (for example, corp.contoso.com, finance.contoso.com) if you are enabling XMPP for a subset of users.</span></span>

<div>

## <a name="certificate-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="41364-109">Сведения о сертификате для протокола расширенного обмена сообщениями и присутствия</span><span class="sxs-lookup"><span data-stu-id="41364-109">Certificate Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41364-110">Компонент</span><span class="sxs-lookup"><span data-stu-id="41364-110">Component</span></span></th>
<th><span data-ttu-id="41364-111">Имя субъекта</span><span class="sxs-lookup"><span data-stu-id="41364-111">Subject name</span></span></th>
<th><span data-ttu-id="41364-112">Замещающий имена субъектов (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="41364-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="41364-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41364-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41364-114">Назначение доступа к службе Edge пограничного сервера или пограничного пула</span><span class="sxs-lookup"><span data-stu-id="41364-114">Assign to Access Edge service of Edge Server or Edge pool</span></span></p></td>
<td><p><span data-ttu-id="41364-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="41364-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="41364-116">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="41364-116">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="41364-117">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="41364-117">sip.contoso.com</span></span></p>
<p><span data-ttu-id="41364-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="41364-118">sip.fabrikam.com</span></span></p>
<p><span data-ttu-id="41364-119">contoso.com</span><span class="sxs-lookup"><span data-stu-id="41364-119">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="41364-120">Первые три элемента сети SAN — это стандартные записи в сети SAN для полного пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="41364-120">The first three SAN entries are the normal SAN entries for a full Edge Server.</span></span> <span data-ttu-id="41364-121">Contoso.com — это запись, необходимая для Федерации с партнером XMPP на уровне корневого домена.</span><span class="sxs-lookup"><span data-stu-id="41364-121">The contoso.com is the entry required for federation with the XMPP partner at the root domain level.</span></span> <span data-ttu-id="41364-122">Эта запись позволит XMPP всем доменам с суффиксом contoso.com.</span><span class="sxs-lookup"><span data-stu-id="41364-122">This entry will allow XMPP for all domains with the suffix contoso.com.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="41364-123">См. также</span><span class="sxs-lookup"><span data-stu-id="41364-123">See Also</span></span>


[<span data-ttu-id="41364-124">Пример конфигурации XMPP в Lync Server 2013 — федерация XMPP с Google Talk</span><span class="sxs-lookup"><span data-stu-id="41364-124">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="41364-125">Планирование сертификатов пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41364-125">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  


[<span data-ttu-id="41364-126">Настройка сертификатов пограничного сервера для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41364-126">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)  
[<span data-ttu-id="41364-127">Request-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="41364-127">Request-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate)  
[<span data-ttu-id="41364-128">Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="41364-128">Set-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  
  

<span data-ttu-id="41364-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41364-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

