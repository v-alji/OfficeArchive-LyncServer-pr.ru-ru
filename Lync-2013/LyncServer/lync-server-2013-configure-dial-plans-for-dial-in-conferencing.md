---
title: 'Lync Server 2013: настройка абонентских групп для конференц-связи с телефонным подключением'
description: 'Lync Server 2013: Настройте абонентские группы для конференц-связи с телефонным подключением.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial plans for dial-in conferencing
ms:assetid: a3e0958e-384f-43e5-b4c9-686b6ecac7ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412768(v=OCS.15)
ms:contentKeyID: 48185051
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28123f905288ce35b6f470168962a3d8e6faa22b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399901"
---
# <a name="configure-dial-plans-for-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="43521-103">Настройка абонентских групп для конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43521-103">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="43521-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="43521-104">

<span> </span></span></span>

<span data-ttu-id="43521-105">_**Тема последнего изменения:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="43521-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="43521-106">При развертывании конференц-связи с телефонным подключением необходимо создать или изменить одну или несколько абонентских групп для маршрутизации номеров доступа к конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="43521-106">When you deploy dial-in conferencing, you need to create or modify one or more dial plans for routing dial-in access phone numbers.</span></span> <span data-ttu-id="43521-107">Убедитесь, что по крайней мере одно правило нормализации в каждой абонентской группе преобразует телефонные расширения в полные телефонные номера в формате E. 164.</span><span class="sxs-lookup"><span data-stu-id="43521-107">Make sure that at least one normalization rule in each dial plan converts telephone extensions into complete phone numbers in E.164 format.</span></span> <span data-ttu-id="43521-108">Пользователи конференц-связи с телефонным подключением присоединяются к конференциям в качестве пользователей предприятия, прошедших проверку подлинности, путем ввода ПИН-кода и номера телефона.</span><span class="sxs-lookup"><span data-stu-id="43521-108">Users of dial-in conferencing join conferences as authenticated enterprise users by entering their personal identification number (PIN) and their phone number.</span></span> <span data-ttu-id="43521-109">Для преобразования добавочных номеров в полные номера телефонов требуется правило нормализации, чтобы пользователи могли для прохождения проверки подлинности вводить только добавочный номер.</span><span class="sxs-lookup"><span data-stu-id="43521-109">You need a normalization rule to convert extensions into complete phone numbers so that users can be authenticated when they enter just a telephone extension.</span></span>

<span data-ttu-id="43521-110">Чтобы настроить абонентские группы для конференц-связи с телефонным подключением, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="43521-110">To set up dial plans for dial-in conferencing, do the following:</span></span>

  - <span data-ttu-id="43521-111">Независимо от того, развертываете ли вы корпоративную голосовую связь, добавьте в глобальную абонентскую группу регион конференц-связи с телефонным подключением и убедитесь, что правило нормализации правильно преобразует номера доступа к конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="43521-111">Whether or not you deploy Enterprise Voice, modify the global dial plan to add a dial-in conferencing region and to make sure that a normalization rule accurately converts your dial-in access numbers.</span></span> <span data-ttu-id="43521-112">Подробные инструкции можно найти [в разделе Изменение абонентской группы в Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="43521-112">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

  - <span data-ttu-id="43521-113">Если развертывание корпоративной голосовой связь не планируется, то создайте абонентские группы для номеров доступа к конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="43521-113">If you did not deploy Enterprise Voice, create dial plans for your dial-in conferencing access numbers.</span></span> <span data-ttu-id="43521-114">Не забудьте добавить регион конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="43521-114">Be sure to include a dial-in conferencing region.</span></span> <span data-ttu-id="43521-115">Подробные инструкции можно найти [в разделе Создание абонентской группы в Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="43521-115">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

  - <span data-ttu-id="43521-116">Если вы развернули корпоративную голосовую связь, добавьте в ее абонентские группы регионы и используйте соответствующие правила нормализации для номеров доступа к конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="43521-116">If you deployed Enterprise Voice, modify Enterprise Voice dial plans as necessary to include regions and use appropriate normalization rules for dial-in access numbers.</span></span> <span data-ttu-id="43521-117">Подробные инструкции можно найти [в разделе Изменение абонентской группы в Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="43521-117">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span> <span data-ttu-id="43521-118">Кроме того, вы также можете создать выделенные абонентские группы, которые используются только для номеров доступа к конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="43521-118">You can also create dedicated dial plans that are used only for dial-in access numbers.</span></span> <span data-ttu-id="43521-119">Подробные инструкции можно найти [в разделе Создание абонентской группы в Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="43521-119">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<span data-ttu-id="43521-120">Подробнее о регионах планирования можно узнать [в разделе Требования к конференциям с телефонным подключением в Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="43521-120">For details about planning regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="43521-121">Содержание</span><span class="sxs-lookup"><span data-stu-id="43521-121">In This Section</span></span>

  - [<span data-ttu-id="43521-122">Просмотр сведений о абонентской схеме в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43521-122">View dial plan information in Lync Server 2013</span></span>](lync-server-2013-view-dial-plan-information.md)

  - [<span data-ttu-id="43521-123">Создание абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43521-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)

  - [<span data-ttu-id="43521-124">Изменение абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43521-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)

  - [<span data-ttu-id="43521-125">Определение правил нормализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43521-125">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)

<span data-ttu-id="43521-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="43521-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

