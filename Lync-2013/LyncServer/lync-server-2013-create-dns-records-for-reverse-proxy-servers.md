---
title: 'Lync Server 2013: создание DNS-записей для обратных прокси-серверов'
description: 'Lync Server 2013: создание записей DNS для обратного прокси-сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create DNS records for reverse proxy servers
ms:assetid: b3513339-e49b-4665-80f1-b5a1c81a0e2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429719(v=OCS.15)
ms:contentKeyID: 48185181
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef785ebbd7160274b631a2d2b6b1f1dcc866e5fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431948"
---
# <a name="create-dns-records-for-reverse-proxy-servers-in-lync-server-2013"></a><span data-ttu-id="89ad3-103">Создание DNS-записей для обратных прокси-серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89ad3-103">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89ad3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89ad3-104">

<span> </span></span></span>

<span data-ttu-id="89ad3-105">_**Тема последнего изменения:** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="89ad3-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="89ad3-106">Создание внешних DNS-записей, указывающих на открытый внешний интерфейс сервера ISA Server 2006 SP1, сервер или Маршрутизация запросов приложений Forefront Threat Management Gateway 2010, как описано в разделе [Настройка DNS для поддержки EDGE в Lync Server 2013](lync-server-2013-configure-dns-for-edge-support.md).</span><span class="sxs-lookup"><span data-stu-id="89ad3-106">Create external DNS A records that point to the public external interface of your Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, Forefront Threat Management Gateway 2010 Server or Internet Information Server Application Request Routing, as described in [Configure DNS for edge support in Lync Server 2013](lync-server-2013-configure-dns-for-edge-support.md).</span></span> <span data-ttu-id="89ad3-107">Вам понадобятся записи DNS для полных доменных имен веб-служб для каждого пула, режиссера (или режиссера) и каждого простого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="89ad3-107">You need DNS records for the external Web Service FQDNs for each pool, the Director (or Director pool), and each simple URL.</span></span>

<span data-ttu-id="89ad3-108">Минимальный набор DNS-записей для разрешения клиента на обратный прокси, должны быть созданы следующие записи:</span><span class="sxs-lookup"><span data-stu-id="89ad3-108">The minimum DNS records for client resolution to the reverse proxy, the following records must be created:</span></span>

  - <span data-ttu-id="89ad3-109">Записи узла (A), которые определяют опубликованные внешние веб-службы для режиссеров и пулов директоров (например, **webdirext.contoso.com**).</span><span class="sxs-lookup"><span data-stu-id="89ad3-109">Host (A) record(s) that define the published external web services for Directors and Director pools (for example, **webdirext.contoso.com**)</span></span>

  - <span data-ttu-id="89ad3-110">Записи узла (A), которые определяют опубликованные внешние веб-службы для внешних веб-служб, размещенных на любых интерфейсных пулах и ролях сервера Standard Edition (например, **webext.contoso.com**).</span><span class="sxs-lookup"><span data-stu-id="89ad3-110">Host (A) record(s) that define the published external web services for external web services hosted on the any Front End pools and Standard Edition server roles (for example, **webext.contoso.com**)</span></span>

  - <span data-ttu-id="89ad3-111">Записи узла (A) для простых URL-адресов (например, **Dialin.contoso.com** и **Meet.contoso.com**).</span><span class="sxs-lookup"><span data-stu-id="89ad3-111">Host (A) records for the Simple URLs (for example, **dialin.contoso.com** and **meet.contoso.com**)</span></span>

  - <span data-ttu-id="89ad3-112">Запись узла (A) для внешней записи Lync Discover, а также предоставляет указатель на автообнаружение для всех веб-приложений, включая Lync Web App, планировщик и мобильность (например, **lyncdiscover.contoso.com**).</span><span class="sxs-lookup"><span data-stu-id="89ad3-112">Host (A) record for the Lync Discover External record, and also provides pointer to AutoDiscover for all Web apps, including the Lync Web App, scheduler and Mobility (for example, **lyncdiscover.contoso.com**)</span></span>

  - <span data-ttu-id="89ad3-113">Записи узла (A) для URL-адреса сервера Office Web Apps (например, **officewebapp01.contoso.com**);</span><span class="sxs-lookup"><span data-stu-id="89ad3-113">Host (A) records for the Office Web Apps Server URL (for example **officewebapp01.contoso.com**)</span></span>

<span data-ttu-id="89ad3-114">Подробности можно найти [в разделе Сводка DNS — обратный прокси-сервер в Lync Server 2013](lync-server-2013-dns-summary-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="89ad3-114">For details, see [DNS summary - Reverse proxy in Lync Server 2013](lync-server-2013-dns-summary-reverse-proxy.md).</span></span>

<span data-ttu-id="89ad3-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89ad3-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

