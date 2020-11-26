---
title: Перенос федерации XMPP
description: Миграция XMPP Федерации.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating XMPP federation
ms:assetid: b8d2b4b9-d0ed-4b48-820a-2c257fbdd2fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721861(v=OCS.15)
ms:contentKeyID: 49733794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e63c9f6fd3f1c1d45de77c27417987505678f74b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440362"
---
# <a name="migrating-xmpp-federation"></a><span data-ttu-id="d393e-103">Перенос федерации XMPP</span><span class="sxs-lookup"><span data-stu-id="d393e-103">Migrating XMPP federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d393e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d393e-104">

<span> </span></span></span>

<span data-ttu-id="d393e-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="d393e-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="d393e-106">Предыдущие версии Lync Server и Office Communications Server предоставили шлюз расширенных сообщений и протоколов доступа (XMPP), который можно развернуть как отдельную серверную роль, разрешающую Федерацию с помощью XMPPных развертываний.</span><span class="sxs-lookup"><span data-stu-id="d393e-106">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="d393e-107">В Lync Server 2013 функциональность XMPP может быть развернута как функция.</span><span class="sxs-lookup"><span data-stu-id="d393e-107">In Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="d393e-108">Функции XMPP устанавливаются в виде прокси-сервера XMPP, который работает на пограничном сервере Lync Server 2013 и шлюз XMPP, который работает на сервере переднего плана Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d393e-108">XMPP functionality is installed in two parts: as an XMPP proxy that runs on the Lync Server 2013 Edge Server, and the XMPP Gateway that runs on the Lync Server 2013 Front End Server.</span></span>

<span data-ttu-id="d393e-109">С точки зрения миграции учетная запись пользователя Lync Server может быть перемещена в пул Lync Server 2013 и продолжать использовать устаревший шлюз XMPP.</span><span class="sxs-lookup"><span data-stu-id="d393e-109">From a migration perspective, a Lync Server user account can be moved to a Lync Server 2013 pool and continue to use the legacy XMPP gateway.</span></span> <span data-ttu-id="d393e-110">Это возможно, только если для федеративного партнера XMPP не настроена платформа Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d393e-110">This is possible only when the XMPP federated partner is not configured in Lync Server 2013.</span></span>

<span data-ttu-id="d393e-111">В сводке, если Lync Server 2010 был развернут с помощью шлюза Office Communications Server 2007 R2 XMPP Gateway и XMPP Federation для пользователей Lync Server 2010, чтобы перенести XMPPную Федерацию на Lync Server 2013, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d393e-111">In summary, if Lync Server 2010 has been deployed with the Office Communications Server 2007 R2 XMPP Gateway and XMPP federation has been enabled for legacy Lync Server 2010 users, to migrate the XMPP federation to Lync Server 2013:</span></span>

1.  <span data-ttu-id="d393e-112">Развертывание пула Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d393e-112">Deploy a Lync Server 2013 pool.</span></span>

2.  <span data-ttu-id="d393e-113">Разверните сервер Lync Server 2013 Edge.</span><span class="sxs-lookup"><span data-stu-id="d393e-113">Deploy a Lync Server 2013 Edge server.</span></span>

3.  <span data-ttu-id="d393e-114">Перемещение всех пользователей в пул Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d393e-114">Move all users to the Lync Server 2013 pool</span></span>

4.  <span data-ttu-id="d393e-115">Создавайте политики доступа XMPP и сертификаты для пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="d393e-115">Create XMPP access policies and certificates for the Edge Server.</span></span>

5.  <span data-ttu-id="d393e-116">Включите Федерацию XMPP в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d393e-116">Enable XMPP federation in Lync Server 2013.</span></span> 

6.  <span data-ttu-id="d393e-117">Обновите записи DNS, чтобы они указывали на сервер Lync Server 2013 XMPP Gateway.</span><span class="sxs-lookup"><span data-stu-id="d393e-117">Update the DNS entries to point to the Lync Server 2013 XMPP Gateway.</span></span>

<span data-ttu-id="d393e-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d393e-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

