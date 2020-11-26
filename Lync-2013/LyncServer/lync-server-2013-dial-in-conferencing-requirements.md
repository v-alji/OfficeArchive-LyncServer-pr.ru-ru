---
title: Требования Lync Server 2013 к конференц-связи с телефонным подключением
description: Требования Lync Server 2013 к конференц-связи с телефонным подключением.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing requirements
ms:assetid: 9aff949e-3dac-481a-be46-a180c72e8066
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398802(v=OCS.15)
ms:contentKeyID: 48184969
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0850204993935998c4c098bc7c2866a8a6f3fa1e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429229"
---
# <a name="dial-in-conferencing-requirements-in-lync-server-2013"></a><span data-ttu-id="b70c3-103">Требования к конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b70c3-103">Dial-in conferencing requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b70c3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b70c3-104">

<span> </span></span></span>

<span data-ttu-id="b70c3-105">_**Тема последнего изменения:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="b70c3-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="b70c3-106">Прежде чем приступить к работе с Lync Server 2013, вам нужно спланировать указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="b70c3-106">Before you start the Lync Server 2013 deployment process you need to plan for the following:</span></span>

  - <span data-ttu-id="b70c3-107">Конфигурация, используемая для подключения к телефонной сети с открытым коммутируемым подключением (КТСОП)</span><span class="sxs-lookup"><span data-stu-id="b70c3-107">The configuration to use for connecting to the public switched telephone network (PSTN)</span></span>

  - <span data-ttu-id="b70c3-108">Стратегия назначения областей конференц-связи с телефонным подключением для номеров доступа с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="b70c3-108">Your strategy for assigning dial-in conferencing regions to dial-in access numbers</span></span>

  - <span data-ttu-id="b70c3-109">Стратегия создания каталогов конференций</span><span class="sxs-lookup"><span data-stu-id="b70c3-109">Your strategy for creating conference directories</span></span>

<div>

## <a name="planning-for-dial-in-pstn-connectivity"></a><span data-ttu-id="b70c3-110">Планирование подключений с телефонным подключением через коммутируемую сеть</span><span class="sxs-lookup"><span data-stu-id="b70c3-110">Planning for Dial-in PSTN Connectivity</span></span>

<span data-ttu-id="b70c3-111">Для конференц-связи с телефонным подключением необходим хотя бы один сервер-посредник и хотя бы один шлюз PSTN.</span><span class="sxs-lookup"><span data-stu-id="b70c3-111">Dial-in conferencing requires at least one Mediation Server and at least one PSTN gateway.</span></span>

<span data-ttu-id="b70c3-112">Сервер-посредник можно развернуть на центральном сайте или на сайте филиала.</span><span class="sxs-lookup"><span data-stu-id="b70c3-112">You can deploy a Mediation Server in a central site or in a branch site.</span></span> <span data-ttu-id="b70c3-113">На центральном сайте сервер-посредник можно разместить в пуле переднего плана или на сервере стандартного выпуска; его также можно развернуть его на изолированном сервере или в изолированном пуле.</span><span class="sxs-lookup"><span data-stu-id="b70c3-113">In a central site, you can collocate a Mediation Server on a Front End pool or Standard Edition server, or you can deploy it on a stand-alone server or pool.</span></span> <span data-ttu-id="b70c3-114">На сайте филиала можно развернуть сервер-посредник на изолированном сервере или как компонент системы обеспечения связи в филиалах.</span><span class="sxs-lookup"><span data-stu-id="b70c3-114">In a branch site, you can deploy a Mediation Server on a stand-alone server or as a component of the Survivable Branch Appliance.</span></span>

<span data-ttu-id="b70c3-p102">Шлюз ТСОП можно развернуть на центральном сайте или на сайте филиала. На сайте филиала шлюз ТСОП может быть изолированным или служить компонентом системы обеспечения связи в филиалах.</span><span class="sxs-lookup"><span data-stu-id="b70c3-p102">You can deploy a PSTN gateway in a central site or in a branch site. In a branch site, the PSTN gateway can be stand-alone or a component of the Survivable Branch Appliance.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b70c3-117">В конференц-связи с телефонным подключением не используется обход мультимедиа, так как сервер конференций/V не поддерживает мультимедийный обход.</span><span class="sxs-lookup"><span data-stu-id="b70c3-117">Dial-in conferencing does not use media bypass because A/V Conferencing Server do not support media bypass.</span></span>



</div>

<span data-ttu-id="b70c3-118">Подробные сведения о планировании конфигурации сервера-посредников и шлюзов PSTN для конференц-связи с телефонным подключением можно найти в разделе [компоненты и топологии для сервера-посредника в Lync server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="b70c3-118">For details about planning your configuration for Mediation Server and PSTN gateways for dial-in conferencing, see [Components and topologies for Mediation Server in Lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) in the Planning documentation.</span></span>

</div>

<span id="bkmk_PlanningforDialinConferencingRegions"></span>

<div>

## <a name="planning-for-dial-in-conferencing-regions"></a><span data-ttu-id="b70c3-119">Планирование областей конференц-связи с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="b70c3-119">Planning for Dial-in Conferencing Regions</span></span>

<span data-ttu-id="b70c3-120">Во время настройки телефонного подключения создаются абонентские группы и номера доступа для конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="b70c3-120">During dial-in configuration, you create dial plans and dial-in conferencing access numbers.</span></span> <span data-ttu-id="b70c3-121">Абонентские группы — это наборы правил нормализации, задающих число и количество цифр в номере телефона, а также перевод номера телефона в стандартный формат E. 164 для маршрутизации звонков.</span><span class="sxs-lookup"><span data-stu-id="b70c3-121">Dial plans are sets of normalization rules that specify the number and pattern of digits in a phone number and translate the phone number into the standard E.164 format for call routing.</span></span> <span data-ttu-id="b70c3-122">Номера доступа к конференции с телефонным подключением — это номера, которые набирают участники, чтобы присоединиться к конференции.</span><span class="sxs-lookup"><span data-stu-id="b70c3-122">Dial-in conferencing access numbers are the numbers participants call to join a conference.</span></span>

<span data-ttu-id="b70c3-123">Каждый номер доступа к конференции с телефонным подключением должен быть связан хотя бы с одной абонентской группой.</span><span class="sxs-lookup"><span data-stu-id="b70c3-123">Every dial-in conferencing access number must be associated with at least one dial plan.</span></span> <span data-ttu-id="b70c3-124">Регионы конференц-связи с телефонным подключением связывают номер доступа конференц-связи с телефонным подключением и абонентской группы.</span><span class="sxs-lookup"><span data-stu-id="b70c3-124">Dial-in conferencing regions associate a dial-in conferencing access number with its dial plans.</span></span> <span data-ttu-id="b70c3-125">Когда вы настраиваете абонентскую группу, вы указываете область конференц-связи с телефонным подключением, которая относится к абонентской группе.</span><span class="sxs-lookup"><span data-stu-id="b70c3-125">When you set up a dial plan, you specify the dial-in conferencing region that applies to the dial plan.</span></span> <span data-ttu-id="b70c3-126">При создании номера доступа по телефонной линии следует выбрать регион, связывающий номер доступа с подходящими абонентскими группами.</span><span class="sxs-lookup"><span data-stu-id="b70c3-126">When you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="b70c3-127">Когда вы создаете абонентскую группу, вы указываете область абонентской группы: область пользователя, область пула или область сайта.</span><span class="sxs-lookup"><span data-stu-id="b70c3-127">When you create a dial plan, you specify the scope of the dial plan: user scope, pool scope, or site scope.</span></span> <span data-ttu-id="b70c3-128">Каждому пользователю назначается применимая к нему абонентская группа наиболее узкой области действия.</span><span class="sxs-lookup"><span data-stu-id="b70c3-128">Every user is assigned the dial plan from the narrowest scope that applies to the user.</span></span> <span data-ttu-id="b70c3-129">Например, если применима абонентская группа уровня пользователя, назначается эта абонентская группа.</span><span class="sxs-lookup"><span data-stu-id="b70c3-129">For example, a user is assigned a user-level dial plan, if one applies.</span></span> <span data-ttu-id="b70c3-130">Если она не применима, пользователю назначается абонентская группа уровня пула.</span><span class="sxs-lookup"><span data-stu-id="b70c3-130">If a user-level dial plan does not apply, the user is assigned a pool-level dial plan.</span></span> <span data-ttu-id="b70c3-131">Если абонентская группа уровня пула также не применима, назначается абонентская группа уровня сайта.</span><span class="sxs-lookup"><span data-stu-id="b70c3-131">If a pool-level dial plan does not apply, the user is assigned a site-level dial plan.</span></span> <span data-ttu-id="b70c3-132">Если и эта абонентская группа не применима, назначается глобальная абонентская группа.</span><span class="sxs-lookup"><span data-stu-id="b70c3-132">If a site-level dial plan does not apply, the user is assigned the global dial plan.</span></span>

<span data-ttu-id="b70c3-p106">Перед настройкой абонентских групп важно понять, как лучше назвать и использовать области. следующие соображения относятся к областям конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="b70c3-p106">Before you configure the dial plans, is it important to plan how you want to name and use regions. The following considerations apply to dial-in conferencing regions:</span></span>

  - <span data-ttu-id="b70c3-135">Обычно область — это географическая область, связанная с офисом или группой офисов.</span><span class="sxs-lookup"><span data-stu-id="b70c3-135">A region is typically a geographical area that is associated with an office or group of offices.</span></span>

  - <span data-ttu-id="b70c3-p107">Языки связываются с номерами доступа для телефонного подключения. Если поддерживаются географические области, имеющие несколько языков, то следует решить, как следует задать области для поддержки нескольких языков. Например, можно задать несколько областей исходя из комбинации географической области и языка, или задать одну область исходя из географической области, а затем задать разные номера доступа для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="b70c3-p107">Languages are associated with dial-in access numbers. If you support geographical areas that have multiple languages, you should decide how you want to define regions to support the multiple languages. For example, you might define multiple regions based on a combination of geography and language, or you might define a single region based on geography and have a different dial-in access numbers for each language.</span></span>

  - <span data-ttu-id="b70c3-139">Когда пользователь планирует собрание, по умолчанию это собрание использует область, указанную абонентской группой этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b70c3-139">When a user schedules a meeting, by default the meeting uses the region specified by that user's dial plan.</span></span>

  - <span data-ttu-id="b70c3-140">По умолчанию все номера доступа для телефонного подключения для региона включаются в приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="b70c3-140">By default, the all of the dial-in access numbers for the region are included in the meeting invitation.</span></span>

  - <span data-ttu-id="b70c3-141">It is important to name regions so that they are clearly recognizable.</span><span class="sxs-lookup"><span data-stu-id="b70c3-141">It is important to name regions so that they are clearly recognizable.</span></span> <span data-ttu-id="b70c3-142">The user can use the names of the regions to change a meeting's region so that different access numbers are included in the invitation.</span><span class="sxs-lookup"><span data-stu-id="b70c3-142">The user can use the names of the regions to change a meeting's region so that different access numbers are included in the invitation.</span></span> <span data-ttu-id="b70c3-143">(Когда пользователи используют Outlook для планирования собрания, пользователь использует надстройку "собрание по сети" для Lync 2013, чтобы изменить регион).</span><span class="sxs-lookup"><span data-stu-id="b70c3-143">(When users use Outlook to schedule a meeting, the user uses the Online Meeting Add-in for Lync 2013 to change the region).</span></span>

  - <span data-ttu-id="b70c3-144">Области должны быть построены таким образом, чтобы любой приглашенный, желающий присоединиться к собранию, мог видеть локальный номер доступа в приглашении на конференцию.</span><span class="sxs-lookup"><span data-stu-id="b70c3-144">Regions should be designed so that any invitee who wants to dial into a conference can see a local access number in the conference invitation.</span></span>

  - <span data-ttu-id="b70c3-145">Вы можете настроить порядок, в котором номера доступа в регионе отображаются на странице параметров конференц-связи с телефонным подключением (и, соответственно, в том порядке, в котором они отображаются в приглашении на конференцию) с помощью командлетов командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b70c3-145">You can configure the order in which access numbers within a region appear on the Dial-in Conferencing Settings page (and, therefore, the order in which they appear in the conference invitation) by using Lync Server Management Shell cmdlets.</span></span>

  - <span data-ttu-id="b70c3-146">Любой пользователь из любого расположения может набрать любой номер доступа для присоединения к конференции.</span><span class="sxs-lookup"><span data-stu-id="b70c3-146">Any user from any location can call any dial-in access number to join a conference.</span></span>

</div>

<div>

## <a name="planning-for-conference-directories"></a><span data-ttu-id="b70c3-147">Планирование каталогов конференций</span><span class="sxs-lookup"><span data-stu-id="b70c3-147">Planning for Conference Directories</span></span>

<span data-ttu-id="b70c3-148">В каталогах конференций поддерживается сопоставление буквенно-цифровых ИДЕНТИФИКАТОРов собраний, используемых участниками для присоединения к Конференции с помощью Lync 2013, а также идентификатора конференции, который используется участниками конференц-связи с телефонным подключением для присоединения к Конференции.</span><span class="sxs-lookup"><span data-stu-id="b70c3-148">Conference directories maintain a mapping between the alphanumeric meeting ID that a participant uses to join a conference when using Lync 2013, and the numeric-only conference ID that a dial-in conferencing participant uses to join the conference.</span></span> <span data-ttu-id="b70c3-149">Идентификатор конференции представлен в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="b70c3-149">The format of the conference ID is as follows:</span></span>

    <housekeeping digit (1 digit)><conference directory (usually 1-2 digits)><conference number (variable number of digits><check digit (1 digit)>

<span data-ttu-id="b70c3-150">Создание нескольких каталогов конференций позволяет присваивать конференциям короткие идентификаторы, если количество конференций не слишком велико.</span><span class="sxs-lookup"><span data-stu-id="b70c3-150">Creating multiple conference directories will ensure that conference IDs will stay short until a significant amount of conferences have been created.</span></span> <span data-ttu-id="b70c3-151">В организациях, где количество конференций на каждого пользователя находится в обычных пределах, рекомендуется создавать по одному каталогу конференций для каждых 999 пользователей в пуле.</span><span class="sxs-lookup"><span data-stu-id="b70c3-151">In an organization with a typical number of conferences per user, we recommend that you create one conference directory for every 999 users in the pool.</span></span> <span data-ttu-id="b70c3-152">С помощью этого правила идентификаторы конференций обычно можно оставлять небольшим.</span><span class="sxs-lookup"><span data-stu-id="b70c3-152">Using this guideline the conference IDs can generally be kept small.</span></span> <span data-ttu-id="b70c3-153">Однако, если каталогов конференций (во всех пулах) больше девяти, для поддержки дополнительных конференции назначаются боле длинные идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="b70c3-153">However, once the number of conference directories (across the pools) exceed 9, the Conference ID number will grow to support additional conferences.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b70c3-154">См. также</span><span class="sxs-lookup"><span data-stu-id="b70c3-154">See Also</span></span>


[<span data-ttu-id="b70c3-155">Компонент сервера «исправления» в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b70c3-155">Mediation Server component in Lync Server 2013</span></span>](lync-server-2013-mediation-server-component.md)  
[<span data-ttu-id="b70c3-156">Абонентские группы и правила нормализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b70c3-156">Dial plans and normalization rules in Lync Server 2013</span></span>](lync-server-2013-dial-plans-and-normalization-rules.md)  
  

<span data-ttu-id="b70c3-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b70c3-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

