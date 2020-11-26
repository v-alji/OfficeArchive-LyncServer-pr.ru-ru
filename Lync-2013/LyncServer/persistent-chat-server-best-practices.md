---
title: Рекомендации по работе с сервером сохраняемого чата
description: Рекомендации по работе с сервером для сохраняемого чата.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server best practices
ms:assetid: dc18e7f7-599b-4d32-abf7-cd9e691426a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398970(v=OCS.15)
ms:contentKeyID: 48185612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c575c0afa0366e88748eadfcf4c04fccb20b375
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438787"
---
# <a name="persistent-chat-server-best-practices"></a><span data-ttu-id="bfa35-103">Рекомендации по работе с сервером сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="bfa35-103">Persistent Chat Server best practices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfa35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfa35-104">

<span> </span></span></span>

<span data-ttu-id="bfa35-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="bfa35-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="bfa35-106">По мере создания категорий и сохраненных комнат чатов, а также для оформления областей и членства в них могут помочь следующие советы.</span><span class="sxs-lookup"><span data-stu-id="bfa35-106">As you create your categories and Persistent Chat rooms and design your scoping and membership, the following tips can help your planning:</span></span>

  - <span data-ttu-id="bfa35-107">Если в вашей компании не требуется безупречная стенка, не Ограничьте область в дереве категорий.</span><span class="sxs-lookup"><span data-stu-id="bfa35-107">If your company does not require an ethical wall, do not narrow the scope in your category tree.</span></span> <span data-ttu-id="bfa35-108">Наведите всех пользователей в область одной категории и создайте все комнаты чата в этой категории.</span><span class="sxs-lookup"><span data-stu-id="bfa35-108">Put all your users in the scope of one category, and create all chat rooms in that category.</span></span> <span data-ttu-id="bfa35-109">Затем вы можете предоставить или ограничить доступ к каждой комнате чата с помощью списков участников.</span><span class="sxs-lookup"><span data-stu-id="bfa35-109">Subsequently, use only membership lists to grant or restrict access to each chat room.</span></span>

  - <span data-ttu-id="bfa35-110">В большинстве случаев необходимо разрешить пользователям создавать новые комнаты чата, чтобы обсуждения новых тем могли начаться в любое время.</span><span class="sxs-lookup"><span data-stu-id="bfa35-110">In most cases, you should enable users to create new chat rooms so that discussions about new topics can be started any time.</span></span> <span data-ttu-id="bfa35-111">Для этого сделайте список **создателей** таким же, как и в списке **AllowedMembers** .</span><span class="sxs-lookup"><span data-stu-id="bfa35-111">Do this by making the **Creators** list the same as the **AllowedMembers** list.</span></span> <span data-ttu-id="bfa35-112">Тем не менее, если вы хотите разрешить создавать комнаты только для Центральной группы поддержки или для определенных пользователей, сделайте список **создателями** подходящим набором.</span><span class="sxs-lookup"><span data-stu-id="bfa35-112">However, if you want to allow only a central support team or designated users to create rooms, then make the **Creators** list as the appropriate subset.</span></span>

  - <span data-ttu-id="bfa35-113">Присвойте каждому из них полное имя и описание, описывающее, где он подходит для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="bfa35-113">Give each chat room a complete name and description summary that describes where it fits in with your organization.</span></span> <span data-ttu-id="bfa35-114">Поскольку пользователи не видят название категории при использовании комнаты чата, нельзя полагаться на название категории, чтобы помочь пользователям определить предполагаемый форум обсуждений для комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="bfa35-114">Because users cannot see the category name when they use the chat room, you cannot rely on the category name to help users determine the intended discussion forum for the chat room.</span></span>

  - <span data-ttu-id="bfa35-115">Возможно, потребуется создать настраиваемый рабочий процесс создания комнаты, если у вас есть определенные соглашения об именовании или другие элементы управления доступом или проверки для реализации.</span><span class="sxs-lookup"><span data-stu-id="bfa35-115">You may want to have a custom room creation workflow if you have certain naming conventions or other access controls or validations to implement.</span></span> <span data-ttu-id="bfa35-116">Настройка сохраняемого чата позволяет настроить **RoomManagementUrl** на то, что вы размещаете.</span><span class="sxs-lookup"><span data-stu-id="bfa35-116">The Persistent Chat configuration enables you to customize the **RoomManagementUrl** to something that you host.</span></span> <span data-ttu-id="bfa35-117">Например, при нажатии кнопки **создать комнату** в клиенте Lync они могут быть перенаправлены в свое собственное решение.</span><span class="sxs-lookup"><span data-stu-id="bfa35-117">For example, when users click **Create a room** in their Lync client, they can be redirected to your custom solution.</span></span>

  - <span data-ttu-id="bfa35-118">Создавайте разнообразные надстройки, которые помогут вам улучшить взаимодействие комнат чата, приведя другие бизнес-данные в комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="bfa35-118">Create a variety of add-ins that help to enhance the experience of chat rooms by bringing in other business data into chat rooms.</span></span> <span data-ttu-id="bfa35-119">Администраторы должны зарегистрировать надстройки, которые должны быть разрешены в системе.</span><span class="sxs-lookup"><span data-stu-id="bfa35-119">Administrators must register the add-ins that they want to allow in the system.</span></span> <span data-ttu-id="bfa35-120">С помощью списка разрешенных надстроек для общения и создателей можно выбрать один из предложенных для них для соответствующих комнат.</span><span class="sxs-lookup"><span data-stu-id="bfa35-120">Chat room managers and creators can choose from the list of allowed add-ins for the ones most relevant to their respective rooms.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="bfa35-121">См. также</span><span class="sxs-lookup"><span data-stu-id="bfa35-121">See Also</span></span>


[<span data-ttu-id="bfa35-122">Управление категориями, чатами и надстройками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfa35-122">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>](lync-server-2013-managing-categories-rooms-and-add-ins.md)  
  

<span data-ttu-id="bfa35-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfa35-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

