---
title: 'Lync Server 2013: настройка чатов'
description: 'Lync Server 2013: Настройка помещений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure rooms
ms:assetid: 8956bd2c-c863-4704-bc65-5c0d83556258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205067(v=OCS.15)
ms:contentKeyID: 48184750
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e9f5b2ece8cf436fe69c000da73871cb92686d82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399361"
---
# <a name="configure-rooms-in-lync-server-2013"></a><span data-ttu-id="3d5e4-103">Настройка чатов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3d5e4-103">Configure rooms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d5e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d5e4-104">

<span> </span></span></span>

<span data-ttu-id="3d5e4-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="3d5e4-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="3d5e4-106">Настройка постоянных комнат чатов обычно обрабатывают пользователи или другие центральные группы с помощью интерфейса командной строки Windows PowerShell; Администратор, как правило, не управляет помещениями чата.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-106">Configuring Persistent Chat rooms is commonly handled by users or other central teams by using Windows PowerShell command-line interface; an administrator typically does not manage chat rooms.</span></span> <span data-ttu-id="3d5e4-107">Тем не менее, если вам нужно создать комнаты чата и управлять ими, вы можете воспользоваться интерфейсом командной строки Windows PowerShell или добавить себя как участника в комнату чата и использовать клиент Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-107">However, if you have to create and manage chat rooms, you can use the Windows PowerShell command-line interface, or add yourself as a member to a chat room and use the Lync 2013 client.</span></span>

<span data-ttu-id="3d5e4-108">Дополнительные сведения о настройке комнат чата с помощью интерфейса командной строки Windows PowerShell можно найти в разделе Управление комнатой на странице [Настройка сохраняемого сервера чата с помощью командлетов Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="3d5e4-108">For details about configuring chat rooms by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<div>

## <a name="managing-data-in-chat-rooms"></a><span data-ttu-id="3d5e4-109">Управление данными в комнатах чата</span><span class="sxs-lookup"><span data-stu-id="3d5e4-109">Managing Data in Chat Rooms</span></span>

<span data-ttu-id="3d5e4-110">Сервер сохраняемого чата позволяет пользователям работать совместно, подмещая сообщения в сохраняемые комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-110">Persistent Chat Server lets users collaborate by posting messages into Persistent Chat rooms.</span></span> <span data-ttu-id="3d5e4-111">Данные сохраняются на сервере, а участники комнаты могут иметь доступ к данным, в том числе к данным с предысторией.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-111">The data is persisted on the server, and members of the room can have access to the data, including historical data.</span></span> <span data-ttu-id="3d5e4-112">Тем не менее, пользователи с разными ролями имеют разный доступ к сохраненным данным, как описано в приведенном ниже списке.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-112">However, users with different roles have different access to the persisted data, as outlined in the following list.</span></span>

  - <span data-ttu-id="3d5e4-113">Администраторы могут удалять старое содержимое (например, содержимое, размещенное до определенной даты) из любой комнаты чата, чтобы база данных сильно не увеличивалась в размерах.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-113">Administrators can delete earlier content (for example, content that was posted before a certain date) from any chat room to keep the database from growing too large.</span></span> <span data-ttu-id="3d5e4-114">Кроме того, они могут удалять или заменять сообщения, которые считаются неприемлемыми для определенной комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-114">Or, they can remove or replace messages that are considered inappropriate for a particular chat room.</span></span>

  - <span data-ttu-id="3d5e4-115">Сами пользователи, включая авторов сообщений, не могут удалять содержимое комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-115">End users, including message authors, cannot delete content from any chat room.</span></span>

  - <span data-ttu-id="3d5e4-116">Руководители комнаты чата могут отключить помещения, но не могут удалять помещения.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-116">Chat room managers can disable rooms, but cannot delete rooms.</span></span> <span data-ttu-id="3d5e4-117">Только администраторы могут удалить комнату чата после того, как она будет создана.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-117">Only administrators can delete a chat room after it has been created.</span></span>

<span data-ttu-id="3d5e4-118">После удаления сообщения отменить это действие невозможно.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-118">When a message is deleted, you cannot undo the action.</span></span> <span data-ttu-id="3d5e4-119">Однако удаленные сообщения могут быть восстановлены при наличии резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-119">However, deleted messages can be restored if there is a backup.</span></span> <span data-ttu-id="3d5e4-120">Если включен постоянный сервер соответствия чатов, старые сообщения сохраняются в базе данных соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-120">If a Persistent Chat Compliance server is enabled, old messages are persisted in the compliance database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3d5e4-121">Это использование данных в комнате чата распространяется на приложение Lync Server 2013, сохраняемый серверный чат, за исключением случаев, когда вовлечена роль администратора.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-121">This chat room data usage applies to the Lync Server 2013, Persistent Chat Server API application, except for the case when the administrator role is involved.</span></span> <span data-ttu-id="3d5e4-122">Серверный API постоянного чата не может использоваться для выполнения каких-либо действий администратора.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-122">The Persistent Chat Server API cannot be used to do any of the administrator’s operations.</span></span> <span data-ttu-id="3d5e4-123">Эти операции необходимо выполнять в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="3d5e4-123">You must perform these operations in the Lync Server Management Shell.</span></span>



<span data-ttu-id="3d5e4-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d5e4-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

