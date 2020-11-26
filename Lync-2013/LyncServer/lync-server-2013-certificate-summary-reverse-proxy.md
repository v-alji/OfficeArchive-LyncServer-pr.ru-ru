---
title: 'Lync Server 2013: сводка по сертификатам — обратный прокси-сервер'
description: 'Lync Server 2013: сведения о сертификате — обратный прокси-сервер.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Reverse proxy
ms:assetid: f2b9a53f-aead-413d-81e9-4a294a010fbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205381(v=OCS.15)
ms:contentKeyID: 48185820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cc250d6de2eb1a0b6c3ad3495c8df62942f9a81
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435279"
---
# <a name="certificate-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="35f39-103">Сводка по сертификатам — обратный прокси-сервер в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35f39-103">Certificate summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="35f39-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="35f39-104">

<span> </span></span></span>

<span data-ttu-id="35f39-105">_**Тема последнего изменения:** 2012-11-14_</span><span class="sxs-lookup"><span data-stu-id="35f39-105">_**Topic Last Modified:** 2012-11-14_</span></span>

<span data-ttu-id="35f39-106">Требования к сертификатам для обратного прокси-сервера значительно проще, чем для пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="35f39-106">Certificate requirements for the reverse proxy are much simpler than that for the Edge Servers.</span></span> <span data-ttu-id="35f39-107">В предоставленных блок-схемах представлены необходимые требования.</span><span class="sxs-lookup"><span data-stu-id="35f39-107">The provided flowchart presents the requirements necessary.</span></span> <span data-ttu-id="35f39-108">Сопутствующая таблица представляет собой типичное имя субъекта сертификата и альтернативные имена субъектов в отношении сценариев, которые мы проверили в обсуждениях пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="35f39-108">The accompanying table presents typical certificate subject name and subject alternative names in relation to the scenarios that we have been reviewed in the Edge Server discussions.</span></span> <span data-ttu-id="35f39-109">Более подробную информацию о сценариях пограничного сервера можно найти [в разделе сценарии доступа внешних пользователей в Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="35f39-109">For more details on the Edge Server scenarios, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="35f39-110">**Блок-схема "сертификаты" для обратного прокси**</span><span class="sxs-lookup"><span data-stu-id="35f39-110">**Certificates Flow Chart for Reverse Proxy**</span></span>

<span data-ttu-id="35f39-111">![Блок-схема сертификации для пограничного сервера](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Блок-схема сертификации для пограничного сервера")</span><span class="sxs-lookup"><span data-stu-id="35f39-111">![Certificates Flow Chart for Edge Server](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Certificates Flow Chart for Edge Server")</span></span>

### <a name="reverse-proxy-external-interface"></a><span data-ttu-id="35f39-112">Обратный прокси: внешний интерфейс</span><span class="sxs-lookup"><span data-stu-id="35f39-112">Reverse Proxy: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35f39-113">Компонент</span><span class="sxs-lookup"><span data-stu-id="35f39-113">Component</span></span></th>
<th><span data-ttu-id="35f39-114">Имя субъекта</span><span class="sxs-lookup"><span data-stu-id="35f39-114">Subject name</span></span></th>
<th><span data-ttu-id="35f39-115">Замещающий имя субъекта (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="35f39-115">Subject alternative name (SAN)/Order</span></span></th>
<th><span data-ttu-id="35f39-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35f39-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35f39-117">Обратный прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="35f39-117">Reverse Proxy</span></span></p></td>
<td><p><span data-ttu-id="35f39-118">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-118">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="35f39-119">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-119">webext.contoso.com</span></span></p>
<p><span data-ttu-id="35f39-120">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-120">webdirext.contoso.com</span></span></p>
<p><span data-ttu-id="35f39-121">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-121">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="35f39-122">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-122">meet.contoso.com</span></span></p>
<p><span data-ttu-id="35f39-123">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-123">officewebapps01.contoso.com</span></span></p>
<p><span data-ttu-id="35f39-124">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-124">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="35f39-125">(Необязательно):\*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="35f39-125">(Optional):\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="35f39-126">Сертификат должен быть выдан общедоступным центром сертификации и в серверном EKU.</span><span class="sxs-lookup"><span data-stu-id="35f39-126">Certificate must be issued by a public CA and with the server EKU.</span></span> <span data-ttu-id="35f39-127">Службы включают в себя службу адресной книги, развертывание групп рассылки Office Web Apps для конференций и правила публикации для IP-устройств Lync.</span><span class="sxs-lookup"><span data-stu-id="35f39-127">Services include Address Book Service, distribution group expansion Office Web Apps for conferencing, and Lync IP Device publishing rules.</span></span> <span data-ttu-id="35f39-128">Ниже указаны дополнительные имена субъектов.</span><span class="sxs-lookup"><span data-stu-id="35f39-128">Subject alternative name includes:</span></span></p>
<ul>
<li><p><span data-ttu-id="35f39-129">Полное доменное имя внешней веб-службы для пула серверов переднего плана или внешнего интерфейса</span><span class="sxs-lookup"><span data-stu-id="35f39-129">External Web Services FQDN for Front End Server or Front End pool</span></span></p></li>
<li><p><span data-ttu-id="35f39-130">Полное доменное имя внешней веб-службы для режиссера или режиссера</span><span class="sxs-lookup"><span data-stu-id="35f39-130">External Web Services FQDN for Director or Director pool</span></span></p></li>
<li><p><span data-ttu-id="35f39-131">Конференц-связь с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="35f39-131">Dial-in conferencing</span></span></p></li>
<li><p><span data-ttu-id="35f39-132">Правило публикации для собрания по сети</span><span class="sxs-lookup"><span data-stu-id="35f39-132">Online meeting publishing rule</span></span></p></li>
<li><p><span data-ttu-id="35f39-133">Office Web Apps для конференций</span><span class="sxs-lookup"><span data-stu-id="35f39-133">Office Web Apps for conferencing</span></span></p></li>
<li><p><span data-ttu-id="35f39-134">Lyncdiscover (автообнаружение)</span><span class="sxs-lookup"><span data-stu-id="35f39-134">Lyncdiscover (Autodiscover)</span></span></p></li>
</ul>
<p><span data-ttu-id="35f39-135">Необязательный подстановочный знак заменяет и соответствие требованиям к сети SAN</span><span class="sxs-lookup"><span data-stu-id="35f39-135">The optional wildcard replaces both meet and dialin SAN</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="35f39-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="35f39-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

