---
title: 'Lync Server 2013: перемещение чата из одной категории в другую'
description: 'Lync Server 2013: перемещение комнаты чата из одной категории в другую.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Moving a chat room from one category to another
ms:assetid: 7e93b8f6-5a18-4476-a432-3918e01bcfa6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215877(v=OCS.15)
ms:contentKeyID: 48706004
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4066732a90a94414b55d6a567fde0d496e4faf13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425271"
---
# <a name="moving-a-chat-room-from-one-category-to-another-in-lync-server-2013"></a><span data-ttu-id="f8bc9-103">Перемещение чата из одной категории в другую в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8bc9-103">Moving a chat room from one category to another in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8bc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8bc9-104">

<span> </span></span></span>

<span data-ttu-id="f8bc9-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f8bc9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f8bc9-106">Мы не рекомендуем менять категорию сохраняемой комнаты чата после создания комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-106">We recommend that you do not change the category of a Persistent Chat room after the chat room is created.</span></span> <span data-ttu-id="f8bc9-107">Тем не менее, если у руководителя комнаты чата есть полномочия **создателя** в другой категории, он может переместить комнату из одной категории в другую.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-107">However, if the chat room manager has **Creator** privileges in another category, he or she can move the room from one category to another.</span></span> <span data-ttu-id="f8bc9-108">Комната не удаляется и воссоздается.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-108">The room is not deleted and recreated.</span></span> <span data-ttu-id="f8bc9-109">Это изменение связи с базой данных.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-109">It is a change of association within the database.</span></span>

<span data-ttu-id="f8bc9-110">Изменение категории комнаты чата может выполняться редко.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-110">Changing a chat room category should be done rarely.</span></span> <span data-ttu-id="f8bc9-111">Категория определяет разрешенное членство в комнате чата, поэтому при перемещении комнаты чата в другую категорию все системные списки управления доступом (SACL), которые более не поддерживаются новой категорией, очищаются.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-111">A category determines the allowed membership for the chat room, so when a chat room is moved to another category, all the system access control lists (SACLs) that are no longer supported by the new category are purged.</span></span> <span data-ttu-id="f8bc9-112">Например, если пользователь был участником комнаты и больше не является **AllowedMember** в новой категории, принадлежность к комнате будет изменена, и пользователь будет удален из комнаты.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-112">For example, if a user was a member of the room and is no longer an **AllowedMember** in the new category, the room membership will be modified and the user will be removed from the room.</span></span>

<span data-ttu-id="f8bc9-113">Подробнее о перемещении комнаты чата с помощью интерфейса командной строки Windows PowerShell можно узнать в разделе Управление комнатой на странице [Настройка сохраняемого сервера чата с помощью командлетов Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="f8bc9-113">For details about moving a chat room by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<span data-ttu-id="f8bc9-114">Дополнительные сведения о настройке комнат чатов можно найти в разделе [Настройка комнат в Lync Server 2013](lync-server-2013-configure-rooms.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="f8bc9-114">For details about configuring chat rooms, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) in the Deployment documentation.</span></span>

<span data-ttu-id="f8bc9-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8bc9-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

