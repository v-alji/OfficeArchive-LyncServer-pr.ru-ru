---
title: 'Lync Server 2013: поддерживаемое выровненное размещение серверов для пограничных компонентов'
description: 'Lync Server 2013: Поддерживаемые расвыровнения серверов для компонентов Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423640"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a><span data-ttu-id="8f06f-103">Поддерживаемое выровненное размещение серверов для пограничных компонентов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f06f-103">Supported server collocation for edge components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f06f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f06f-104">

<span> </span></span></span>

<span data-ttu-id="8f06f-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="8f06f-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="8f06f-106">Служба пограничного доступа, служба Edge для веб-конференций, служба EDGE и служба XMPP proxy размещаются на пограничных серверах.</span><span class="sxs-lookup"><span data-stu-id="8f06f-106">The Access Edge service, Web Conferencing Edge service, A/V Edge service and XMPP Proxy service are collocated on the Edge Servers.</span></span> <span data-ttu-id="8f06f-107">Следующие серверы предоставляют функции, необходимые для доступа внешних пользователей, и должны развертываться как выделенные серверы:</span><span class="sxs-lookup"><span data-stu-id="8f06f-107">The following servers provide functions needed for external user access and must be deployed as dedicated servers:</span></span>

  - <span data-ttu-id="8f06f-108">Пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="8f06f-108">Edge Server</span></span>

  - <span data-ttu-id="8f06f-109">Режиссер (необязательно)</span><span class="sxs-lookup"><span data-stu-id="8f06f-109">Director (Optional)</span></span>

  - <span data-ttu-id="8f06f-110">Сертификат обратного прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="8f06f-110">Reverse proxy</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8f06f-111">Обратный прокси-сервер не требуется специально для обслуживания только сервера Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f06f-111">The reverse proxy does not need to be dedicated to serving only Lync Server 2013.</span></span> <span data-ttu-id="8f06f-112">Например, вы можете предоставить услуги для публикации веб-служб Lync Server и одновременно предоставить опубликованный веб-сайт для другого веб-сайта, на котором не установлено Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8f06f-112">For example, you can provide services to publish the Lync Server Web services, and concurrently provide a published Web site for another Web site that has no bearing on Lync Server at all.</span></span> <span data-ttu-id="8f06f-113">Если у вас уже есть обратный прокси-сервер в демилитаризованной зоне для поддержки других служб, вы можете использовать его для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f06f-113">If you already have a reverse proxy server in the perimeter network to support other services, you can use it for Lync Server 2013.</span></span>



<span data-ttu-id="8f06f-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f06f-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

