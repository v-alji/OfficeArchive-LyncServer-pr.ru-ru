---
title: 'Lync Server 2013: сведения о сертификате — автообнаружение'
description: 'Lync Server 2013: сведения о сертификате — автообнаружение.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Autodiscover
ms:assetid: 16ac96bb-882a-4141-b75c-9530637548d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945616(v=OCS.15)
ms:contentKeyID: 51541451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae421401421434a4c4069c1d90ee287dfb016997
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435351"
---
# <a name="certificate-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="9a843-103">Сведения о сертификате: обнаружение автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a843-103">Certificate summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a843-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a843-104">

<span> </span></span></span>

<span data-ttu-id="9a843-105">_**Тема последнего изменения:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="9a843-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="9a843-106">Служба автообнаружения Lync Server 2013 работает на серверах пула и интерфейсах, а также при публикации в DNS может использоваться клиентами Lync для поиска служб сервера и пользователей.</span><span class="sxs-lookup"><span data-stu-id="9a843-106">The Lync Server 2013 Autodiscover Service runs on the Director and Front End pool servers, and when published in DNS, can be used by Lync clients to locate server and user services.</span></span> <span data-ttu-id="9a843-107">Если вы обновляете приложение Lync Server 2010 и не разрешили мобильность, то перед тем как клиенты смогут использовать автоматическое обнаружение, необходимо изменить список альтернативных имен субъектов сертификата на любом сетевом сервере и на внешнем интерфейсе, на котором запущена служба автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="9a843-107">If you are upgrading from Lync Server 2010 and did not deploy Mobility, before clients can use automatic discovery, you must modify certificate subject alternative name lists on any Director and Front End Server running the Autodiscover Service.</span></span> <span data-ttu-id="9a843-108">Кроме того, может потребоваться изменить список альтернативных имен субъектов в сертификатах, используемых для использования внешних правил публикации веб-службы на обратных прокси.</span><span class="sxs-lookup"><span data-stu-id="9a843-108">In addition, it may be necessary to modify the subject alternative name lists on certificates used for external web service publishing rules on reverse proxies.</span></span>

<span data-ttu-id="9a843-109">Решение о том, следует ли использовать списки альтернативных имен для субъектов в обратных прокси-серверах, зависит от того, публикуются ли служба автообнаружения для порта 80 или для порта 443:</span><span class="sxs-lookup"><span data-stu-id="9a843-109">The decision about whether to use subject alternative name lists on reverse proxies is based on whether you publish the Autodiscover Service on port 80 or on port 443:</span></span>

  - <span data-ttu-id="9a843-110">**Опубликовано на порте 80**   Если первый запрос к службе автообнаружения находится на порту 80, никаких изменений в сертификате не требуется.</span><span class="sxs-lookup"><span data-stu-id="9a843-110">**Published on port 80**   No certificate changes are required if the initial query to the Autodiscover Service occurs over port 80.</span></span> <span data-ttu-id="9a843-111">Это связано с тем, что мобильные устройства Lync обращаются к обратному прокси-серверу на порте 80 извне, а затем подсоединены к директору или серверу переднего плана с помощью внутреннего порта 8080.</span><span class="sxs-lookup"><span data-stu-id="9a843-111">This is because mobile devices running Lync will access the reverse proxy on port 80 externally and then be bridged to a Director or Front End Server on port 8080 internally.</span></span> <span data-ttu-id="9a843-112">Дополнительные сведения можно найти в разделе "начальный процесс автообнаружения с помощью порта 80" [технические требования для мобильных устройств в Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="9a843-112">For details, see the "Initial Autodiscover Process Using Port 80" section [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="9a843-113">**Опубликовано на порте 443**   Список альтернативных имен субъектов в сертификатах, используемых внешним правилом публикации веб-служб, должен содержать *lyncdiscover. \<sipdomain\>*</span><span class="sxs-lookup"><span data-stu-id="9a843-113">**Published on port 443**   The subject alternative name list on certificates used by the external web services publishing rule must contain a *lyncdiscover.\<sipdomain\>*</span></span> <span data-ttu-id="9a843-114">запись для каждого домена SIP в Организации.</span><span class="sxs-lookup"><span data-stu-id="9a843-114">entry for each SIP domain within your organization.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9a843-115">Мы настоятельно рекомендуем использовать HTTPS через HTTP.</span><span class="sxs-lookup"><span data-stu-id="9a843-115">We highly recommend using HTTPS over HTTP.</span></span> <span data-ttu-id="9a843-116">Протокол HTTPS использует сертификаты для шифрования трафика.</span><span class="sxs-lookup"><span data-stu-id="9a843-116">HTTPS uses certificates to encrypt traffic.</span></span> <span data-ttu-id="9a843-117">HTTP не обеспечивает шифрование, а все отправленные данные будут представлять собой обычный текст.</span><span class="sxs-lookup"><span data-stu-id="9a843-117">HTTP does not provide for encryption, and any data sent will be plain text.</span></span>

    
    </div>

<span data-ttu-id="9a843-118">Повторное выдача сертификатов с помощью внутреннего центра сертификации обычно является простым процессом.</span><span class="sxs-lookup"><span data-stu-id="9a843-118">Reissuing certificates by using an internal certificate authority is typically a simple process.</span></span> <span data-ttu-id="9a843-119">Но для общедоступных сертификатов, используемых в правиле публикации веб-службы, добавление нескольких записей альтернативных имен может быть дорогостоящим.</span><span class="sxs-lookup"><span data-stu-id="9a843-119">But for public certificates used on the web service publishing rule, adding multiple subject alternative name entries can become expensive.</span></span> <span data-ttu-id="9a843-120">Для решения этой проблемы мы поддерживаем начальное подключение автоматического обнаружения через порт 80, который затем перенаправляется на порт 8080 на сервере директора или на внешнем клиенте.</span><span class="sxs-lookup"><span data-stu-id="9a843-120">To work around this issue, we support the initial automatic discovery connection over port 80, which is then redirected to port 8080 on the Director or Front End Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9a843-121">Если ваша инфраструктура Lync Server 2013 использует внутренние сертификаты, выданные внутренним центром сертификации (ЦС), и вы планируете поддерживать беспроводное подключение к мобильным устройствам, на них должны быть установлены корневые цепочки сертификатов из внутреннего ЦС или необходимо изменить общедоступный сертификат в инфраструктуре Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9a843-121">If your Lync Server 2013 infrastructure uses internal certificates that are issued from an internal certification authority (CA) and you plan to support mobile devices connecting wirelessly, either the root certificate chain from the internal CA must be installed on the mobile devices or you must change to a public certificate on your Lync Server 2013 infrastructure.</span></span>



</div>

<span data-ttu-id="9a843-122">В этой статье описаны дополнительные имена субъектов, необходимые для режиссера, сервера переднего плана и обратного прокси.</span><span class="sxs-lookup"><span data-stu-id="9a843-122">This topic describes the added subject alternative names required for the Director, Front End Server and reverse proxy.</span></span> <span data-ttu-id="9a843-123">На него ссылаются только добавленные дополнительные имена субъектов (SAN).</span><span class="sxs-lookup"><span data-stu-id="9a843-123">Only the added subject alternative names (SAN) are referenced.</span></span> <span data-ttu-id="9a843-124">Ознакомьтесь с разделом Планирование, в котором вы найдете инструкции по использованию других операций с сертификатами.</span><span class="sxs-lookup"><span data-stu-id="9a843-124">Refer to the planning sections for guidance on the other entries on certificates.</span></span> <span data-ttu-id="9a843-125">Дополнительные сведения можно найти [в разделе сценарии для режиссера в Lync server 2013](lync-server-2013-scenarios-for-the-director.md), [сценарии для внешних пользователей Access в Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md)и [сценарии обратной прокси-сервера в Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="9a843-125">For details, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md), [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md), and [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span></span>

<span data-ttu-id="9a843-126">В следующих таблицах определяются записи автообнаружения для службы каталогов, пула интерфейсов и обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="9a843-126">The following tables define the Autodiscover SAN entries for the Director pool, the Front End pool, and the reverse proxy:</span></span>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="9a843-127">Требования к сертификатам пула директоров</span><span class="sxs-lookup"><span data-stu-id="9a843-127">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a843-128">Описание</span><span class="sxs-lookup"><span data-stu-id="9a843-128">Description</span></span></th>
<th><span data-ttu-id="9a843-129">Запись альтернативного имени субъекта</span><span class="sxs-lookup"><span data-stu-id="9a843-129">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a843-130">URL-адрес внутренней службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="9a843-130">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9a843-131">SAN = lyncdiscoverinternal. &lt; внутреннее доменное имя&gt;</span><span class="sxs-lookup"><span data-stu-id="9a843-131">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a843-132">Внешний URL-адрес службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="9a843-132">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9a843-133">SAN=lyncdiscover.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="9a843-133">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="9a843-134">Вы назначаете новому обновленному сертификату новый элемент SAN на сертификат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a843-134">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="9a843-135">Кроме того, вы можете использовать сеть SAN = \*. &lt; sipdomain &gt; .</span><span class="sxs-lookup"><span data-stu-id="9a843-135">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;.</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="9a843-136">Требования к сертификату пула переднего плана</span><span class="sxs-lookup"><span data-stu-id="9a843-136">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a843-137">Описание</span><span class="sxs-lookup"><span data-stu-id="9a843-137">Description</span></span></th>
<th><span data-ttu-id="9a843-138">Запись альтернативного имени субъекта</span><span class="sxs-lookup"><span data-stu-id="9a843-138">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a843-139">URL-адрес внутренней службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="9a843-139">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9a843-140">SAN = lyncdiscoverinternal. &lt; внутреннее доменное имя&gt;</span><span class="sxs-lookup"><span data-stu-id="9a843-140">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a843-141">Внешний URL-адрес службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="9a843-141">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9a843-142">SAN=lyncdiscover.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="9a843-142">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="9a843-143">Вы назначаете новому обновленному сертификату новый элемент SAN на сертификат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a843-143">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="9a843-144">Кроме того, вы можете использовать сеть SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9a843-144">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="9a843-145">Требования сертификата по обратному прокси (общедоступному центру сертификации)</span><span class="sxs-lookup"><span data-stu-id="9a843-145">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a843-146">Описание</span><span class="sxs-lookup"><span data-stu-id="9a843-146">Description</span></span></th>
<th><span data-ttu-id="9a843-147">Запись альтернативного имени субъекта</span><span class="sxs-lookup"><span data-stu-id="9a843-147">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a843-148">Внешний URL-адрес службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="9a843-148">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9a843-149">SAN=lyncdiscover.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="9a843-149">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="9a843-150">Вы назначаете новый обновленный сертификат для новой записи SAN в прослушиватель SSL на обратном прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="9a843-150">You assign the newly updated certificate with the new SAN entry to the SSL Listener on the reverse proxy.</span></span>



<span data-ttu-id="9a843-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a843-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

