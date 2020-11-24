---
title: 'Lync Server 2013: поддержка групповых сертификатов'
description: Поддержка подстановочных сертификатов в Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Wildcard certificate support
ms:assetid: 0bae2aa8-b6dc-46f5-a3be-3fe7581809d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202161(v=OCS.15)
ms:contentKeyID: 48183382
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46cc362eb925a86b5e90d51569db6d425ba88fa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398914"
---
# <a name="wildcard-certificate-support-in-lync-server-2013"></a><span data-ttu-id="ab480-103">Поддержка групповых сертификатов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-103">Wildcard certificate support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab480-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab480-104">

<span> </span></span></span>

<span data-ttu-id="ab480-105">_**Тема последнего изменения:** 2013-03-21_</span><span class="sxs-lookup"><span data-stu-id="ab480-105">_**Topic Last Modified:** 2013-03-21_</span></span>

<span data-ttu-id="ab480-106">Lync Server 2013 использует сертификаты для обеспечения шифрования связи и проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="ab480-106">Lync Server 2013 uses certificates to provide communications encryption and server identity authentication.</span></span> <span data-ttu-id="ab480-107">В некоторых случаях, например, веб-публикации с помощью обратного прокси, не требуется полное доменное имя (FQDN) сервера, на котором не указана служба.</span><span class="sxs-lookup"><span data-stu-id="ab480-107">In some cases, such as web publishing through the reverse proxy, strong subject alternative name (SAN) entry matching to the fully qualified domain name (FQDN) of the server presenting the service is not required.</span></span> <span data-ttu-id="ab480-108">В этих случаях вы можете использовать сертификаты с подстановочными знаками SAN (обычно называемыми подстановочными сертификатами), чтобы снизить стоимость сертификата, запрашиваемого общедоступным центром сертификации, и уменьшить сложность процесса планирования для сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ab480-108">In these cases, you can use certificates with wildcard SAN entries (commonly known as “wildcard certificates”) to reduce the cost of a certificate requested from a public certification authority and to reduce the complexity of the planning process for certificates.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="ab480-109">Чтобы сохранить функциональность устройств с единым коммуникационным подключением (например, стационарных телефонов), необходимо тщательно протестировать развернутый сертификат, чтобы убедиться, что устройства правильно работают после реализации сертификата с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="ab480-109">To retain the functionality of unified communications (UC) devices (for example, desk phones), you should test the deployed certificate carefully to ensure that devices function properly after you implement a wildcard certificate.</span></span>



</div>

<span data-ttu-id="ab480-110">В качестве имени субъекта (также называемого общим именем или CN) отсутствует поддержка подстановочных знаков для любой роли.</span><span class="sxs-lookup"><span data-stu-id="ab480-110">There is no support for a wildcard entry as the subject name (also referred to as the common name or CN) for any role.</span></span> <span data-ttu-id="ab480-111">При использовании подстановочных элементов в сети хранения данных поддерживаются следующие роли сервера.</span><span class="sxs-lookup"><span data-stu-id="ab480-111">The following server roles are supported when using wildcard entries in the SAN:</span></span>

  - <span></span>  
    <span data-ttu-id="ab480-112">**Обратный прокси-сервер.**</span><span class="sxs-lookup"><span data-stu-id="ab480-112">**Reverse proxy.**</span></span>   <span data-ttu-id="ab480-113">Подстановочные знаки в сети хранения данных поддерживаются для простого сертификата публикации URL-адреса (сопоставления и набора номера).</span><span class="sxs-lookup"><span data-stu-id="ab480-113">Wildcard SAN entry is supported for Simple URL (meet and dialin) publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="ab480-114">**Обратный прокси-сервер.**</span><span class="sxs-lookup"><span data-stu-id="ab480-114">**Reverse proxy.**</span></span>   <span data-ttu-id="ab480-115">Запись с подстановочными знаками в сети SAN поддерживается для записей SAN для LyncDiscover сертификата публикации.</span><span class="sxs-lookup"><span data-stu-id="ab480-115">Wildcard SAN entry is supported for the SAN entries for LyncDiscover on the publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="ab480-116">**Папка.**</span><span class="sxs-lookup"><span data-stu-id="ab480-116">**Director.**</span></span>   <span data-ttu-id="ab480-117">Подстановочные знаки в сети хранения данных поддерживаются для простых URL-адресов (для звонков и набора номера) и для записей SAN для LyncDiscover и LyncDiscoverInternal в компонентах Director.</span><span class="sxs-lookup"><span data-stu-id="ab480-117">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Director web components.</span></span>

  - <span></span>  
    <span data-ttu-id="ab480-118">**Сервер переднего плана (стандартный выпуск) и пул переднего плана (Enterprise Edition).**</span><span class="sxs-lookup"><span data-stu-id="ab480-118">**Front End Server (Standard Edition) and Front End pool (Enterprise Edition).**</span></span> <span data-ttu-id="ab480-119">Подстановочные знаки в сети хранения данных поддерживаются для простых URL-адресов (для звонков и набора номера) и для записей SAN для LyncDiscover и LyncDiscoverInternal на веб-компонентах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="ab480-119">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Front End web components.</span></span>

  - <span></span>  
    <span data-ttu-id="ab480-120">**Единая система обмена сообщениями Exchange (UM).**</span><span class="sxs-lookup"><span data-stu-id="ab480-120">**Exchange Unified Messaging (UM).**</span></span>   <span data-ttu-id="ab480-121">Сервер не использует записи SAN при развертывании в качестве изолированного сервера.</span><span class="sxs-lookup"><span data-stu-id="ab480-121">The server does not use SAN entries when deployed as a stand-alone server.</span></span>

  - <span></span>  
    <span data-ttu-id="ab480-122">**Сервер клиентского доступа Microsoft Exchange Server.**</span><span class="sxs-lookup"><span data-stu-id="ab480-122">**Microsoft Exchange Server Client Access server.**</span></span>   <span data-ttu-id="ab480-123">Записи с подстановочными знаками в сети хранения данных поддерживаются для внутренних и внешних клиентов.</span><span class="sxs-lookup"><span data-stu-id="ab480-123">Wildcard entries in the SAN are supported for internal and external clients.</span></span>

  - <span></span>  
    <span data-ttu-id="ab480-124">**Единая система обмена сообщениями (UM) и сервер клиентского доступа Microsoft Exchange Server на одном и том же сервере.**</span><span class="sxs-lookup"><span data-stu-id="ab480-124">**Exchange Unified Messaging (UM) and Microsoft Exchange Server Client Access server on same server.**</span></span>   <span data-ttu-id="ab480-125">Поддерживаются записи с подстановочными знаками в сети хранения данных.</span><span class="sxs-lookup"><span data-stu-id="ab480-125">Wildcard SAN entries are supported.</span></span>

<span data-ttu-id="ab480-126">Роли сервера, не описанные в этом разделе:</span><span class="sxs-lookup"><span data-stu-id="ab480-126">Server roles that are not addressed in this topic:</span></span>

  - <span data-ttu-id="ab480-127">Внутренние роли сервера (в том числе сервер-посредник, Архивация и мониторинг сервера, бесперебойно работающего филиала, а также бесперебойно работающего сервера филиалов)</span><span class="sxs-lookup"><span data-stu-id="ab480-127">Internal server roles (including, but not limited to the Mediation Server, Archiving and Monitoring Server, Survivable Branch Appliance, or Survivable Branch Server)</span></span>

  - <span data-ttu-id="ab480-128">Внешние интерфейсы пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="ab480-128">External Edge Server interfaces</span></span>

  - <span data-ttu-id="ab480-129">Внутренний пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="ab480-129">Internal Edge Server</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ab480-130">В интерфейсе внутренней серверной граничного сервера можно назначить элементу SAN подстановочный знак и поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="ab480-130">For the internal Edge Server interface, a wildcard entry can be assigned to the SAN, and is supported.</span></span> <span data-ttu-id="ab480-131">Сеть хранения данных на внутреннем пограничном сервере не запрашивается, а для записи с подстановочными знаками в сети хранения данных — ограниченные значения.</span><span class="sxs-lookup"><span data-stu-id="ab480-131">The SAN on the internal Edge Server is not queried, and a wildcard SAN entry is of limited value.</span></span>

    
    </div>

<span data-ttu-id="ab480-132">Дополнительные сведения о конфигурациях сертификатов, в том числе использование подстановочных знаков в сертификатах, можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="ab480-132">For details about certificate configurations, including the use of wildcards in certificates, see the following topics:</span></span>

  - [<span data-ttu-id="ab480-133">Требования к сертификатам для внутренних серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-133">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="ab480-134">Требования к сертификатам для доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-134">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="ab480-135">Сводка по сертификатам — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-135">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="ab480-136">Сводка по сертификатам — единственный директор в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-136">Certificate summary - Single Director in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-director.md)

  - [<span data-ttu-id="ab480-137">Сводка по сертификатам — масштабированный пул директоров, аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-137">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="ab480-138">Сводка по сертификатам — обратный прокси-сервер в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-138">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="ab480-139">Рекомендации по интеграции локальной единой системы обмена сообщениями и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab480-139">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="ab480-140">Дополнительные сведения о настройке сертификатов для Exchange, в том числе использование подстановочных знаков, можно найти в документации по продукту Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ab480-140">For details about configuring certificates for Exchange, including the use of wildcards, see the Exchange 2013 product documentation.</span></span>

<span data-ttu-id="ab480-141"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab480-141"></div>

<span> </span>

</div>

</div>

</span></span></div>

