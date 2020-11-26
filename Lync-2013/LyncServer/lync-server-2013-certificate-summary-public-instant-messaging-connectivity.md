---
title: 'Lync Server 2013: сведения о сертификате-общедоступная служба обмена мгновенными сообщениями'
description: 'Lync Server 2013: сведения о сертификате — общедоступная служба обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Public instant messaging connectivity
ms:assetid: 2b3687ee-50c2-4c1c-880e-8dcf8bd4f309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618370(v=OCS.15)
ms:contentKeyID: 49105657
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: abf5a01bdeb03da158e221c623417a1b42cc82f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435294"
---
# <a name="certificate-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="71c49-103">Сведения о сертификате: общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71c49-103">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71c49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71c49-104">

<span> </span></span></span>

<span data-ttu-id="71c49-105">_**Тема последнего изменения:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="71c49-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="71c49-106">Чтобы настроить сертификаты для подключения к общедоступной службе мгновенных сообщений, необходимо сначала обратить внимание на то, что ничего не отличается от других типов Федерации SIP или даже стандартных сертификатов пограничного сервера, за исключением того, что для America Online (AOL) требуется уникальная конфигурация сертификата.</span><span class="sxs-lookup"><span data-stu-id="71c49-106">To configure certificates for public Instant Messaging connectivity, you should first notice that there is nothing different from other SIP federation types or even standard Edge Server certificates, except that America Online (AOL) requires a unique certificate configuration.</span></span> <span data-ttu-id="71c49-107">В дополнение к стандартному расширенному использованию серверного ключа (EKU) для Skype Online требуется, чтобы сертификат или сертификаты (в случае пограничного пула) также содержали клиентское EKU.</span><span class="sxs-lookup"><span data-stu-id="71c49-107">In addition to the usual server enhanced key usage (EKU), America Online requires the certificate or certificates (in the case of an Edge pool) to also contain the client EKU.</span></span> <span data-ttu-id="71c49-108">Клиентское EKU является дополнением к сертификату и является частью внешнего общедоступного сертификата, назначенного пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="71c49-108">The client EKU is an addition to the certificate, and is part of the external public certificate that is assigned to your Edge Server.</span></span>

<div>

## <a name="certificate-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="71c49-109">Сведения о сертификате: общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="71c49-109">Certificate Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71c49-110">Компонент</span><span class="sxs-lookup"><span data-stu-id="71c49-110">Component</span></span></th>
<th><span data-ttu-id="71c49-111">Имя субъекта</span><span class="sxs-lookup"><span data-stu-id="71c49-111">Subject name</span></span></th>
<th><span data-ttu-id="71c49-112">Замещающий имена субъектов (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="71c49-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="71c49-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71c49-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71c49-114">Внешний край и доступ</span><span class="sxs-lookup"><span data-stu-id="71c49-114">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="71c49-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="71c49-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="71c49-116">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="71c49-116">sip.contoso.com</span></span></p>
<p><span data-ttu-id="71c49-117">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="71c49-117">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="71c49-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="71c49-118">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="71c49-119">Сертификат должен находиться в общедоступном центре сертификации, а также в том случае, если вы разворачиваете общедоступную службу обмена мгновенными сообщениями с AOL, и у вас должен быть серверный EKU</span><span class="sxs-lookup"><span data-stu-id="71c49-119">The certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="71c49-120">Сертификат назначается внешним интерфейсам пограничного сервера для следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="71c49-120">The certificate is assigned to the external Edge Server interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="71c49-121">доступа</span><span class="sxs-lookup"><span data-stu-id="71c49-121">Access Edge service</span></span></p></li>
<li><p><span data-ttu-id="71c49-122">веб-конференций</span><span class="sxs-lookup"><span data-stu-id="71c49-122">Web Conferencing Edge service</span></span></p></li>
<li><p><span data-ttu-id="71c49-123">передачи аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="71c49-123">A/V Edge service</span></span></p></li>
</ul>
<p><span data-ttu-id="71c49-124">Обратите внимание, что сети SAN автоматически добавляются к сертификату на основе определений в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="71c49-124">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="71c49-125">Вы добавляете записи SAN по мере необходимости для дополнительных доменов SIP и других элементов, которые необходимо поддерживать.</span><span class="sxs-lookup"><span data-stu-id="71c49-125">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="71c49-126">Имя субъекта реплицируется в сети SAN и должно быть представлено для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="71c49-126">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="71c49-127">См. также</span><span class="sxs-lookup"><span data-stu-id="71c49-127">See Also</span></span>


[<span data-ttu-id="71c49-128">Сценарии доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71c49-128">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
  

<span data-ttu-id="71c49-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71c49-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

