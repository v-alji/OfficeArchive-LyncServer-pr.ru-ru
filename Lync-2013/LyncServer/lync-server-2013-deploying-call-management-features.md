---
title: 'Lync Server 2013: развертывание функций управления звонками'
description: 'Lync Server 2013: развертывание функций управления звонками.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying call management features
ms:assetid: 1667cfe4-76fa-4e10-91bb-b3efbedbf759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204706(v=OCS.15)
ms:contentKeyID: 48183504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa89b75dbcae9de1069daf99986076b66e0411cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430072"
---
# <a name="deploying-call-management-features-in-lync-server-2013"></a><span data-ttu-id="dcafa-103">Развертывание функций управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcafa-103">Deploying call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dcafa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dcafa-104">

<span> </span></span></span>

<span data-ttu-id="dcafa-105">_**Тема последнего изменения:** 2012-12-18_</span><span class="sxs-lookup"><span data-stu-id="dcafa-105">_**Topic Last Modified:** 2012-12-18_</span></span>

<span data-ttu-id="dcafa-106">Возможности управления голосом на корпоративном звонке определяют маршрутизацию и ответ на входящие звонки.</span><span class="sxs-lookup"><span data-stu-id="dcafa-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="dcafa-107">Lync Server 2013 обеспечивает следующие функции управления звонками:</span><span class="sxs-lookup"><span data-stu-id="dcafa-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="dcafa-108">**Припаркованный звонок:** Позволяет голосовым пользователям временно приостановить звонок, а затем выбрать его на другом телефоне.</span><span class="sxs-lookup"><span data-stu-id="dcafa-108">**Call Park:** Enables voice users to temporarily park a call and then pick it up from the same phone or another phone.</span></span>

  - <span data-ttu-id="dcafa-109">**Отправка групп:** Позволяет пользователям отвечать на звонки, выполненные другим пользователям, которые назначены в группу раскладки с помощью набора номера группы для отправки звонков.</span><span class="sxs-lookup"><span data-stu-id="dcafa-109">**Group Pickup:** Enables users to answer calls made to another user who is assigned to a pickup group by dialing the call pickup group number.</span></span>

  - <span data-ttu-id="dcafa-110">**Группа ответа:** Маршрутизация входящих звонков на группы агентов с помощью групп слежения и ответов на вопросы и ответы в интерактивный автоответчик.</span><span class="sxs-lookup"><span data-stu-id="dcafa-110">**Response Group:** Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="dcafa-111">**Объявление:** Воспроизводит сообщение для звонков, выполненных на неназначенные номера, или направляет Звонок на другое место.</span><span class="sxs-lookup"><span data-stu-id="dcafa-111">**Announcement:** Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="dcafa-112">В этом разделе рассказывается о том, как настроить эти функции управления звонками при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="dcafa-112">This section describes how to configure these call management features during an Enterprise Voice deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="dcafa-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="dcafa-113">In This Section</span></span>

  - [<span data-ttu-id="dcafa-114">Настройка парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcafa-114">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)

  - [<span data-ttu-id="dcafa-115">Настройка отправки группового звонка в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcafa-115">Configuring Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-configuring-group-call-pickup.md)

  - [<span data-ttu-id="dcafa-116">Настройка группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcafa-116">Configuring Response Group in Lync Server 2013</span></span>](lync-server-2013-configuring-response-group.md)

  - [<span data-ttu-id="dcafa-117">Настройка объявлений для неназначенных номеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcafa-117">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)

<span data-ttu-id="dcafa-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dcafa-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

