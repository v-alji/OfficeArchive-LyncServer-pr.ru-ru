---
title: 'Lync Server 2013: планирование автообнаружения'
description: 'Lync Server 2013: планирование автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Autodiscover
ms:assetid: 51f1ff94-1d64-4e6d-a878-b86fa07edc2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945628(v=OCS.15)
ms:contentKeyID: 51541474
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e28a6a3a317f063151eadde7c5de51b02a46b482
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437079"
---
# <a name="planning-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="30294-103">Планирование автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30294-103">Planning for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30294-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30294-104">

<span> </span></span></span>

<span data-ttu-id="30294-105">_**Тема последнего изменения:** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="30294-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="30294-106">Средство автообнаружения было представлено для Lync Server в накопительном обновлении для Lync Server 2010: Ноябрь 2011.</span><span class="sxs-lookup"><span data-stu-id="30294-106">Autodiscover was introduced for Lync Server in the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="30294-107">Основным предназначением для этой первоначальной реализации автообнаружения было предоставление средств Lync Mobile поиска службы Mobility Service (MCX).</span><span class="sxs-lookup"><span data-stu-id="30294-107">The primary purpose for this initial implementation of Autodiscover was to provide a means for Lync Mobile to locate the Mobility service (Mcx).</span></span> <span data-ttu-id="30294-108">Служба автообнаружения в Lync Server 2013 теперь является службой, используемой всеми клиентами для поиска серверных и пользовательских служб.</span><span class="sxs-lookup"><span data-stu-id="30294-108">The Autodiscover service in Lync Server 2013 is now a service used by all clients to locate server and user services.</span></span> <span data-ttu-id="30294-109">Служба автообнаружения Microsoft Lync Server 2013 работает на директориях и серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="30294-109">The Microsoft Lync Server 2013 Autodiscover service runs on Directors and Front End Servers.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="30294-110">Дополнительные сведения о автообнаружения и возможностях, которые передается клиентам, приведены в разделе <A href="lync-server-2013-understanding-autodiscover.md">Общие сведения о автообнаружения в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="30294-110">For a more technical understanding of Autodiscover and what is communicated to clients, see <A href="lync-server-2013-understanding-autodiscover.md">Understanding Autodiscover in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="30294-111">Мобильность по-прежнему является особым сценарием, а для служб Mobility по-прежнему требуется специальное планирование.</span><span class="sxs-lookup"><span data-stu-id="30294-111">Mobility is still a distinct scenario and the Mobility services still require some special planning.</span></span> <span data-ttu-id="30294-112">Дополнительные сведения можно найти <A href="lync-server-2013-planning-for-mobility.md">в разделе Планирование мобильных устройств в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="30294-112">For additional details, see <A href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="30294-113">При вводе автообнаружения в Lync Server 2010 для реализации службы, требующей потенциальных изменений сертификатов на существующем сервере, находились нарушения, которые необходимо было сделать.</span><span class="sxs-lookup"><span data-stu-id="30294-113">When Autodiscover was introduced in Lync Server 2010, there were compromises that needed to be made in order to implement a service that required potential certificate changes to existing server deployments.</span></span> <span data-ttu-id="30294-114">Функцию автообнаружения можно использовать для порта TCP 443 для HTTPS или порта TCP 80 для HTTP.</span><span class="sxs-lookup"><span data-stu-id="30294-114">Autodiscover could be used over port TCP 443 for HTTPS or over port TCP 80 for HTTP.</span></span> <span data-ttu-id="30294-115">Если вы принимаете решение использовать HTTPS, сертификаты на обратных прокси-серверах, режиссерах и серверах переднего плана должны быть повторно выпущены для размещения необходимых `lyncdiscover.<domain>` и `lyncdiscoverinternal.<domain>` DNS-записей.</span><span class="sxs-lookup"><span data-stu-id="30294-115">If the decision was made to use HTTPS, certificates on reverse proxies, Directors, and Front End Servers needed to be reissued in order to accommodate the required `lyncdiscover.<domain>` and `lyncdiscoverinternal.<domain>` DNS records.</span></span> <span data-ttu-id="30294-116">Если вы хотите использовать HTTP, повторные выдаче сертификатов могут быть невозможны с помощью записей CNAME DNS (или псевдонима) для использования существующих имен в сертификатах.</span><span class="sxs-lookup"><span data-stu-id="30294-116">If the decision was to use HTTP, the reissue of certificates could be avoided by using DNS CNAME (or alias) records to use existing names on the certificates.</span></span> <span data-ttu-id="30294-117">Использование HTTP означает, что начальные соединения не были зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="30294-117">Using HTTP did mean that the initial communications were unencrypted.</span></span>

<span data-ttu-id="30294-118">Поскольку Lync Server 2013 использует функцию автообнаружения для всех клиентов, основным сценарием является использование HTTPS исключительно и создание сертификатов с помощью lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="30294-118">Because Lync Server 2013 uses Autodiscover for all clients, the main scenario is to use HTTPS exclusively and to create certificates with lyncdiscover.\<domain\></span></span> <span data-ttu-id="30294-119">в рамках настройки обратной прокси-сервера, режиссеров и серверов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="30294-119">as part of the configuration of reverse proxies, Directors and Front End Servers.</span></span> <span data-ttu-id="30294-120">Если вы реализуете автообнаружение в обновленном развертывании с Lync Server 2010, вам может потребоваться использовать HTTP, чтобы избежать повторной сертификации сертификатов.</span><span class="sxs-lookup"><span data-stu-id="30294-120">If you are implementing Autodiscover into an upgraded deployment from Lync Server 2010, you may want to use HTTP to avoid reissuing certificates.</span></span> <span data-ttu-id="30294-121">Руководство по обоим сценариям приведено в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="30294-121">Guidance for both scenarios is provided in the following sections.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="30294-122">Список альтернативных имен субъектов в сертификатах, используемых внешним правилом публикации веб-служб, должен содержать <EM>lyncdiscover. &lt; sipdomain &gt; </EM> запись для каждого домена SIP в Организации.</span><span class="sxs-lookup"><span data-stu-id="30294-122">The subject alternative name list on certificates used by the external web services publishing rule must contain a <EM>lyncdiscover.&lt;sipdomain&gt;</EM> entry for each SIP domain within your organization.</span></span> <span data-ttu-id="30294-123">Дополнительные сведения об элементах альтернативных имен тем, которые требуются для режиссеров, серверов переднего плана и обратного доступа, приведены <A href="lync-server-2013-certificate-summary-autodiscover.md">в разделе сведения о сертификате: автообнаружение в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="30294-123">For details about the subject alternative name entries that are required for Directors, Front End Servers, and reverse proxies, see <A href="lync-server-2013-certificate-summary-autodiscover.md">Certificate summary - Autodiscover in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="30294-124">Содержание</span><span class="sxs-lookup"><span data-stu-id="30294-124">In This Section</span></span>

  - [<span data-ttu-id="30294-125">Сведения о сертификате: обнаружение автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30294-125">Certificate summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-autodiscover.md)

  - [<span data-ttu-id="30294-126">Сводка порта: автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30294-126">Port summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-port-summary-autodiscover.md)

  - [<span data-ttu-id="30294-127">Сводка DNS: обнаружение автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30294-127">DNS summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-dns-summary-autodiscover.md)

  - [<span data-ttu-id="30294-128">Гибридная и Разделяемая доменные возможности автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30294-128">Hybrid and split-domain - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-hybrid-and-split-domain-autodiscover.md)

<span data-ttu-id="30294-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30294-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

