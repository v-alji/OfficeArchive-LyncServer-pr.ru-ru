---
title: 'Lync Server 2013: назначение политик для пользователей'
description: 'Lync Server 2013: назначение политик для пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user policies
ms:assetid: a4ed0120-d9e5-4eb2-acfd-8de2cb503652
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182561(v=OCS.15)
ms:contentKeyID: 48184971
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a99156f9413926251c27dfee40677976b80b7ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438297"
---
# <a name="assigning-per-user-policies-in-lync-server-2013"></a><span data-ttu-id="9385f-103">Назначение политик для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-103">Assigning per-user policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9385f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9385f-104">

<span> </span></span></span>

<span data-ttu-id="9385f-105">_**Тема последнего изменения:** 2012-10-14_</span><span class="sxs-lookup"><span data-stu-id="9385f-105">_**Topic Last Modified:** 2012-10-14_</span></span>

<span data-ttu-id="9385f-106">Вы можете назначать определенные политики пользователю или группе пользователей, чтобы указать конкретные параметры, которые отличаются от параметров, определенных в политиках, назначенных другим пользователям, например глобальные политики.</span><span class="sxs-lookup"><span data-stu-id="9385f-106">You can assign certain policies to a user or a group of users in order to specify particular settings that deviate from the settings defined in policies assigned to other users, such as global policies.</span></span> <span data-ttu-id="9385f-107">Эти политики называются политиками для пользователей.</span><span class="sxs-lookup"><span data-stu-id="9385f-107">These policies are called per-user policies.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9385f-108">Содержание</span><span class="sxs-lookup"><span data-stu-id="9385f-108">In This Section</span></span>

  - [<span data-ttu-id="9385f-109">Назначение политики конференций для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-109">Assign a per-user conferencing policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-conferencing-policy.md)

  - [<span data-ttu-id="9385f-110">Назначение политики клиентской версии для пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-110">Assign a per-user client version policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-client-version-policy.md)

  - [<span data-ttu-id="9385f-111">Назначение политики PIN-кода для пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-111">Assign a per-user PIN policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-pin-policy.md)

  - [<span data-ttu-id="9385f-112">Назначение политики доступа внешних пользователей пользователю, разрешенному для Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-112">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)

  - [<span data-ttu-id="9385f-113">Назначение политики архивации по пользователям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-113">Assign a per-user archiving policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-archiving-policy.md)

  - [<span data-ttu-id="9385f-114">Назначение политики местоположения для каждого пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-114">Assign a per-user location policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-location-policy.md)

  - [<span data-ttu-id="9385f-115">Назначение политики мобильности на мобильные пользователи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-115">Assign a per-user mobility policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-mobility-policy.md)

  - [<span data-ttu-id="9385f-116">Назначение политики постоянного чата для каждого пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-116">Assign a per-user Persistent Chat policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-persistent-chat-policy.md)

  - [<span data-ttu-id="9385f-117">Назначение политики абонентской группы для пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-117">Assign a per-user dial plan policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-dial-plan-policy.md)

  - [<span data-ttu-id="9385f-118">Назначение политики голосовой связи для пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-118">Assign a per-user voice policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-voice-policy.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9385f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9385f-119">See Also</span></span>


[<span data-ttu-id="9385f-120">Управление пользователями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9385f-120">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="9385f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9385f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

