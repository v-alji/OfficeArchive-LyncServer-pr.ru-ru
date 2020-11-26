---
title: 'Lync Server 2013: обзор процесса развертывания для корпоративной голосовой связи'
description: 'Lync Server 2013: обзор процесса развертывания для корпоративной голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process overview for Enterprise Voice
ms:assetid: cf92adbe-aa90-4b05-8e1a-f3794ca68132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398878(v=OCS.15)
ms:contentKeyID: 48185526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c8163dae21435490badd5633ae799e651ab2def
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429617"
---
# <a name="deployment-process-overview-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="c2add-103">Обзор процесса развертывания для корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-103">Deployment process overview for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2add-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2add-104">

<span> </span></span></span>

<span data-ttu-id="c2add-105">_**Тема последнего изменения:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="c2add-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="c2add-106">Действия по развертыванию и настройке, которые необходимо выполнить, зависят от функции голосовой связи или функциональных возможностей, которые вы добавляете в среду Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2add-106">The deployment and configuration steps that you need to follow are dependent on the Enterprise Voice feature or functionality you are adding to your Lync Server 2013 environment.</span></span>

<div>

## <a name="feature-deployment-overviews"></a><span data-ttu-id="c2add-107">Обзоры развертывания компонентов</span><span class="sxs-lookup"><span data-stu-id="c2add-107">Feature Deployment Overviews</span></span>

<span data-ttu-id="c2add-108">Общие сведения о развертывании сети PSTN можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c2add-108">For an overview of deploying PSTN connectivity, see the following:</span></span>

  - [<span data-ttu-id="c2add-109">Контрольный список развертывания для каналов SIP для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-109">SIP trunk deployment checklist for Lync Server 2013</span></span>](lync-server-2013-sip-trunk-deployment-checklist.md)

  - [<span data-ttu-id="c2add-110">Варианты развертывания прямого SIP-подключения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-110">Direct SIP deployment options in Lync Server 2013</span></span>](lync-server-2013-direct-sip-deployment-options.md)

  - [<span data-ttu-id="c2add-111">Планирование маршрутизации исходящей голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-111">Planning outbound voice routing in Lync Server 2013</span></span>](lync-server-2013-planning-outbound-voice-routing.md)

<span data-ttu-id="c2add-112">Общие сведения о развертывании единой системы обмена сообщениями Exchange (UM) можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c2add-112">For an overview of deploying Exchange Unified Messaging (UM), see the following:</span></span>

  - [<span data-ttu-id="c2add-113">Процесс развертывания для интеграции локальной единой системы обмена сообщениями и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-113">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="c2add-114">Общие сведения о развертывании средств управления допуском звонков можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c2add-114">For an overview of deploying call admission control, see the following topics:</span></span>

  - [<span data-ttu-id="c2add-115">Контрольный список развертывания для контроля допуска звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-115">Deployment checklist for call admission control in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-call-admission-control.md)

<span data-ttu-id="c2add-116">Обзор процесса развертывания экстренных служб можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c2add-116">For an overview of the deployment process for Emergency Services, see the following:</span></span>

  - [<span data-ttu-id="c2add-117">Определение требований для экстренных вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-117">Defining your requirements for emergency calls in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-emergency-calls.md)

  - [<span data-ttu-id="c2add-118">Выбор поставщика услуг E9-1-1 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-118">Choosing an E9-1-1 service provider for Lync Server 2013</span></span>](lync-server-2013-choosing-an-e9-1-1-service-provider.md)

  - [<span data-ttu-id="c2add-119">Контрольный список развертывания для E9-1-1 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-119">Deployment checklist for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-e9-1-1.md)

<span data-ttu-id="c2add-120">Общие сведения о развертывании частных телефонных линий можно найти в разделе "личные телефонные линии в смешанных развертываниях" [планирования для частных телефонных линий с помощью Lync Server 2013](lync-server-2013-planning-for-private-telephone-lines.md).</span><span class="sxs-lookup"><span data-stu-id="c2add-120">For an overview of deploying private telephone lines, see the “Private Telephone Lines in Mixed Deployments” section of [Planning for private telephone lines with Lync Server 2013](lync-server-2013-planning-for-private-telephone-lines.md).</span></span>

<span data-ttu-id="c2add-121">Общие сведения о развертывании возможностей обработки звонков (стоянка звонков, приложения для объявлений и группы ответа) можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c2add-121">For an overview of the deployment of call handling features (call parking, announcement application, and response groups), see the following:</span></span>

  - [<span data-ttu-id="c2add-122">Процесс развертывания для парковки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-122">Deployment process for Call Park in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-call-park.md)

  - [<span data-ttu-id="c2add-123">Процесс развертывания приложения для объявлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2add-123">Deployment process for the Announcement application in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-the-announcement-application.md)

<span data-ttu-id="c2add-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2add-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

