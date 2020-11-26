---
title: 'Lync Server 2013: удаление чата или категории'
description: 'Lync Server 2013: удаление комнаты или категории чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a chat room or category
ms:assetid: adccb869-0015-4eba-ac73-718bac7843b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215881(v=OCS.15)
ms:contentKeyID: 48706009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ef89802171a1eeca7de18ff0a4eb8eb3895f1b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430415"
---
# <a name="deleting-a-chat-room-or-category-in-lync-server-2013"></a><span data-ttu-id="5e82b-103">Удаление чата или категории в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e82b-103">Deleting a chat room or category in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e82b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e82b-104">

<span> </span></span></span>

<span data-ttu-id="5e82b-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5e82b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5e82b-106">Сохраняемые комнаты чата могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="5e82b-106">Persistent Chat rooms can be deleted.</span></span> <span data-ttu-id="5e82b-107">Если у вас есть комната чата, которая больше не используется, ее можно отключить.</span><span class="sxs-lookup"><span data-stu-id="5e82b-107">If you have a chat room that is no longer being used, you can disable it.</span></span> <span data-ttu-id="5e82b-108">Подробности можно найти [в разделе Отключение и включение комнаты чата в Lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span><span class="sxs-lookup"><span data-stu-id="5e82b-108">For details, see [Disabling or enabling a chat room in Lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span></span>

<span data-ttu-id="5e82b-109">Администратор сохраняемого чата может запрашивать отключенные комнаты чата, а также периодически очищать и удалять комнаты чата с помощью командлета Windows PowerShell **Remove-CsPersistentChatRoom**.</span><span class="sxs-lookup"><span data-stu-id="5e82b-109">A Persistent Chat administrator can query for disabled chat rooms, and can periodically purge and permanently delete the chat rooms, by using the Windows PowerShell cmdlet, **Remove-CsPersistentChatRoom**.</span></span>

<span data-ttu-id="5e82b-110">Категории можно удалить.</span><span class="sxs-lookup"><span data-stu-id="5e82b-110">Categories can be deleted.</span></span> <span data-ttu-id="5e82b-111">Тем не менее, чтобы удалить категорию, необходимо сначала удалить из нее все комнаты чата или переместить комнаты чата в новую категорию, оставив пустую категорию для удаления.</span><span class="sxs-lookup"><span data-stu-id="5e82b-111">However, to delete a category, you must first either delete all chat rooms under it or move the chat rooms to a new category, leaving an empty category for deletion.</span></span> <span data-ttu-id="5e82b-112">На сервере сохраняемого чата не разрешается удалять категории, содержащие комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="5e82b-112">Persistent Chat Server does not allow you to delete a category that contains chat rooms.</span></span> <span data-ttu-id="5e82b-113">Подробности можно найти [в разделе Перемещение комнаты чата из одной категории в другую в Lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="5e82b-113">For details, see [Moving a chat room from one category to another in Lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span></span>

<span data-ttu-id="5e82b-114">Подробнее об удалении пустых категорий с помощью интерфейса командной строки Windows PowerShell можно узнать в разделе Управление комнатой на странице [Настройка сохраняемого сервера чата с помощью командлетов Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="5e82b-114">For details about deleting empty categories by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<span data-ttu-id="5e82b-115">Дополнительные сведения о комнатах и категориях чата в разделе [Настройка комнат в Lync server 2013](lync-server-2013-configure-rooms.md) и [Настройка категорий в Lync Server 2013](lync-server-2013-configure-categories.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="5e82b-115">For details about chat rooms and categories, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) and [Configure categories in Lync Server 2013](lync-server-2013-configure-categories.md) in the Deployment documentation.</span></span>

<span data-ttu-id="5e82b-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e82b-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

