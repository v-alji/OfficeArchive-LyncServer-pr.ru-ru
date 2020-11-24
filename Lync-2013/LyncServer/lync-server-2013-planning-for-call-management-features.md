---
title: 'Lync Server 2013: Планирование функций управления звонками'
description: 'Lync Server 2013: Планирование функций управления звонками.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call management features
ms:assetid: 5f557345-5a04-45d6-b274-c02dbfe41b33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398421(v=OCS.15)
ms:contentKeyID: 48184298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec990aad40baf33365e92e78ee8071216a2add1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397879"
---
# <a name="planning-for-call-management-features-in-lync-server-2013"></a><span data-ttu-id="a8f57-103">Планирование функций управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8f57-103">Planning for call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8f57-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8f57-104">

<span> </span></span></span>

<span data-ttu-id="a8f57-105">_**Тема последнего изменения:** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="a8f57-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="a8f57-106">Возможности управления голосом на корпоративном звонке определяют маршрутизацию и ответ на входящие звонки.</span><span class="sxs-lookup"><span data-stu-id="a8f57-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="a8f57-107">Lync Server 2013 обеспечивает следующие функции управления звонками:</span><span class="sxs-lookup"><span data-stu-id="a8f57-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="a8f57-108">**Парковка вызовов**:   предоставляет пользователям голосовой связи возможность временно запарковать вызов, а затем ответить на него с того же или с другого телефона.</span><span class="sxs-lookup"><span data-stu-id="a8f57-108">**Call Park**:   Enables voice users to temporarily park a call and then pick it up from the same or another phone.</span></span>

  - <span data-ttu-id="a8f57-109">**Групповой ответ**:   позволяет пользователям голосовой связи отвечать на звонки, которые адресованы другим пользователям, назначенным группам ответа на звонки.</span><span class="sxs-lookup"><span data-stu-id="a8f57-109">**Group Pickup**:   Enables voice users to pick up calls that are ringing for other voice users who are assigned to call pickup groups.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a8f57-110">Отправка групп — это новая платформа с накопительными обновлениями для Lync Server 2013: Февраль 2013.</span><span class="sxs-lookup"><span data-stu-id="a8f57-110">Group Pickup is new with Cumulative Updates for Lync Server 2013: February 2013.</span></span>

    
    </div>

  - <span data-ttu-id="a8f57-111">**Группа ответа**:    направляет входящие звонки в группы агентов с помощью сервисных групп или вопросов и ответов интерактивного автоответчика (IVR).</span><span class="sxs-lookup"><span data-stu-id="a8f57-111">**Response Group**:   Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="a8f57-112">**Объявление:**    Воспроизводит сообщение для звонков, выполненных на неназначенные номера, или направляет Звонок на другое место.</span><span class="sxs-lookup"><span data-stu-id="a8f57-112">**Announcement:**    Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="a8f57-113">Если планируется развертывание корпоративной голосовой связи, то можно указать, какие из этих функций управления вызовами следует реализовать.</span><span class="sxs-lookup"><span data-stu-id="a8f57-113">If you plan to deploy Enterprise Voice, you can choose to implement any or all of these call management features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a8f57-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="a8f57-114">In This Section</span></span>

  - [<span data-ttu-id="a8f57-115">Планирование парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8f57-115">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)

  - [<span data-ttu-id="a8f57-116">Планирование отправки группового звонка в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8f57-116">Planning for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-planning-for-group-call-pickup.md)

  - [<span data-ttu-id="a8f57-117">Планирование групп ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8f57-117">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)

  - [<span data-ttu-id="a8f57-118">Планирование объявлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8f57-118">Planning for announcements in Lync Server 2013</span></span>](lync-server-2013-planning-for-announcements.md)

<span data-ttu-id="a8f57-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8f57-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

