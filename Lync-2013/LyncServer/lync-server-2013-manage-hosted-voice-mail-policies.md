---
title: 'Lync Server 2013: управление политиками размещенной голосовой почты'
description: 'Lync Server 2013: Управление политиками размещенной голосовой почты.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage hosted voice mail policies
ms:assetid: 50ff22e3-9c8b-4a33-a72f-d149892acf53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398332(v=OCS.15)
ms:contentKeyID: 48184139
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcb5e98884d37540d5e75cc8cb6b1b419e4e75e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426097"
---
# <a name="manage-hosted-voice-mail-policies-in-lync-server-2013"></a><span data-ttu-id="c1de1-103">Управление политиками размещенной голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1de1-103">Manage hosted voice mail policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c1de1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c1de1-104">

<span> </span></span></span>

<span data-ttu-id="c1de1-105">_**Тема последнего изменения:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="c1de1-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="c1de1-106">*Политика размещенной голосовой почты* предоставляет информацию в приложение Lync Server 2013 ExUM о том, где следует перенаправлять звонки для пользователей, чьи почтовые ящики находятся на размещенной службе Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1de1-106">A *hosted voice mail policy* provides information to the Lync Server 2013 ExUM Routing application about where to route calls for users whose mailboxes are located on a hosted Exchange service.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c1de1-107">Как правило, требуется только одна политика размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="c1de1-107">Typically, only one hosted voice mail policy is required.</span></span> <span data-ttu-id="c1de1-108">Во многих случаях вы можете изменить глобальную политику в соответствии с вашими потребностями.</span><span class="sxs-lookup"><span data-stu-id="c1de1-108">In many cases, you can modify the global policy to meet all your needs.</span></span> <span data-ttu-id="c1de1-109">Если вы создаете политику с областью сайта, она автоматически назначается всем пользователям, расположенным на указанном сайте.</span><span class="sxs-lookup"><span data-stu-id="c1de1-109">If you create a policy with site scope, it is assigned automatically to all users homed at the specified site.</span></span> <span data-ttu-id="c1de1-110">Если вы создаете политику с областью "на пользователя", необходимо явным образом назначать ее пользователям, группам и контактным объектам.</span><span class="sxs-lookup"><span data-stu-id="c1de1-110">If you create a policy with per-user scope, you must explicitly assign it to users, groups, and contact objects.</span></span> <span data-ttu-id="c1de1-111">Вы можете развернуть несколько политик размещенной голосовой почты, но в таком случае политики должны быть назначены для каждого пользователя отдельно.</span><span class="sxs-lookup"><span data-stu-id="c1de1-111">It is possible to deploy multiple hosted voice mail policies, but in that case the policies must be assigned on a per-user basis.</span></span>



</div>

<span data-ttu-id="c1de1-112">Дополнительные сведения о планировании политик размещенной голосовой почты можно найти [в разделе политики размещенной голосовой почты в Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="c1de1-112">For details about planning hosted voice mail policies, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c1de1-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="c1de1-113">In This Section</span></span>

  - [<span data-ttu-id="c1de1-114">Изменение политики глобальной размещенной голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1de1-114">Modify the global hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-modify-the-global-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="c1de1-115">Создание политики размещенной голосовой почты на уровне сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1de1-115">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-site-level-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="c1de1-116">Создание политики размещенной голосовой почты для каждого пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1de1-116">Create a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-per-user-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="c1de1-117">Назначение политики размещенной голосовой почты для отдельных пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1de1-117">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)

<span data-ttu-id="c1de1-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c1de1-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

