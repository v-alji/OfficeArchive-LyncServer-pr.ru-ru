---
title: 'Lync Server 2013: Общие сведения о маршрутизации Location-Based для конференц-связи'
description: 'Lync Server 2013: Общие сведения о маршрутизации Location-Based для конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing for conferencing
ms:assetid: 8b86740e-db95-4304-bb83-64d0cbb91d47
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362815(v=OCS.15)
ms:contentKeyID: 56335084
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a8fe9cdf4a797243c3ec04b3466011f374fb0d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399682"
---
# <a name="overview-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="07df1-103">Общие сведения о маршрутизации Location-Based для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07df1-103">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07df1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07df1-104">

<span> </span></span></span>

<span data-ttu-id="07df1-105">_**Тема последнего изменения:** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="07df1-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="07df1-106">Приложение для конференц-связи с Location-Based предоставляет в Lync конференции механизм предотвращения бесплатных бесплатных обпереговоров.</span><span class="sxs-lookup"><span data-stu-id="07df1-106">The Location-Based Routing Conferencing application provides to Lync Conferences a mechanism for the prevention of PSTN toll bypass.</span></span> <span data-ttu-id="07df1-107">Приложение отслеживает активные Конференции и применяет Location-Based ограничениям маршрутизации на основе расположения участвующих пользователей Lync.</span><span class="sxs-lookup"><span data-stu-id="07df1-107">The application monitors active conferences and enforces Location-Based Routing restrictions based on the location of the Lync users participating.</span></span>

<span data-ttu-id="07df1-108">Приложение для конференц-связи Location-Based определяет, следует ли применять маршрутизацию Location-Based на собрании Lync, если выполняются указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="07df1-108">The Location-Based Routing Conferencing application determines whether Location-Based Routing is to be enforced on a Lync meeting if the following criteria are met:</span></span>

  - <span data-ttu-id="07df1-109">Организатор собрания включен для Location-Based маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="07df1-109">The meeting organizer is enabled for Location-Based Routing.</span></span> <span data-ttu-id="07df1-110">Location-Based ограничения маршрутизации будут применяться только к конференциям, упорядоченным по пользователям, для которых разрешена Location-Based маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="07df1-110">Location-Based Routing restrictions will be applied only to conferences that are organized by users who are enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="07df1-111">Хотя бы один участник собрания является конечной точкой ТСОП.</span><span class="sxs-lookup"><span data-stu-id="07df1-111">At least one meeting participant is a PSTN endpoint.</span></span> <span data-ttu-id="07df1-112">Location-Based ограничения маршрутизации применимы только к конференциям, включающих конечные точки PSTN.</span><span class="sxs-lookup"><span data-stu-id="07df1-112">Location-Based Routing restrictions are applicable only for conferences that include PSTN endpoints.</span></span>

  - <span data-ttu-id="07df1-113">Сетевой сайт, где находится шлюз ТСОП, используемый для подключения конференции к ТСОП, а также сетевые сайты, из которых подключаются организаторы и участники.</span><span class="sxs-lookup"><span data-stu-id="07df1-113">The network site where the PSTN gateway used to bridge the conference to the PSTN is located as well as the network sites where the organizers and participants are connecting from.</span></span>

<span data-ttu-id="07df1-114">Приложение для конференц-связи Location-Based предотвращает участие пользователей Lync и конечных точек PSTN с разных сетевых сайтов для одной конференции.</span><span class="sxs-lookup"><span data-stu-id="07df1-114">The Location-Based Routing Conferencing application prevents the participation of Lync users and PSTN endpoints from different network sites to the same conference.</span></span> <span data-ttu-id="07df1-115">Если организатор собрания включен для Location-Based маршрутизации, приложение для конференц-связи накладывает указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="07df1-115">If the organizer of a meeting is enabled for Location-Based Routing, the Conferencing application enforces the following restrictions:</span></span>

  - <span data-ttu-id="07df1-116">Конечные точки, которые могут присоединиться к собранию Lync, зависят от конечных точек, которые уже присоединились к Конференции, и это ограничение настраивается так, чтобы присоединиться к Конференции и добавить конечные точки.</span><span class="sxs-lookup"><span data-stu-id="07df1-116">The endpoints that can join a Lync meeting depend on the endpoints that already joined the conference, and this restriction adjusts as joined endpoints leave and new endpoints join the conference.</span></span> <span data-ttu-id="07df1-117">Если организаторов и участники присоединяются к собранию Lync с помощью того же сайта сети, конечная точка PSTN, другой участник того же сетевого сайта или другой участник из другого сайта сети могут присоединиться к сети.</span><span class="sxs-lookup"><span data-stu-id="07df1-117">If organizers and participants are joining a Lync meeting from the same network site, then a PSTN endpoint, another participant from the same network site, another participant from a different network site or a participant from an unknown network site are allowed to join.</span></span>

  - <span data-ttu-id="07df1-118">Если организаторы и участники присоединились к собранию из разных или неизвестных сетевых сайтов, конечной точке ТСОП запрещено присоединяться к собранию в случае, если звонок ТСОП поступает из магистрали SIP, для которой включена маршрутизация на основе расположения.</span><span class="sxs-lookup"><span data-stu-id="07df1-118">If organizers and participants are joining the meeting from different or unknown network sites, a PSTN endpoint is not allowed to join the meeting if the PSTN call ingresses from a SIP trunk enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="07df1-119">Если организаторов и участники присоединяются к собранию из того же сайта сети, а участники, присоединяющиеся к этому же собранию, не могут присоединиться к собранию, в конечную точку Lync с другого сайта сети.</span><span class="sxs-lookup"><span data-stu-id="07df1-119">If organizers and participants are all joining the meeting from the same network site and there are participants joining the same meeting from the PSTN, a Lync endpoint from a different network site is not allowed to join the meeting.</span></span>

<span data-ttu-id="07df1-120">Эти ограничения на конференциях Location-Based описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="07df1-120">These conferencing Location-Based Routing restrictions are summarized in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07df1-121">Пользователи конференции на данный момент</span><span class="sxs-lookup"><span data-stu-id="07df1-121">User(s) in a conference at any given point</span></span></p></td>
<td><p><span data-ttu-id="07df1-122">Пользователи, которым разрешено присоединяться к конференции</span><span class="sxs-lookup"><span data-stu-id="07df1-122">User(s) allowed to join the conference</span></span></p></td>
<td><p><span data-ttu-id="07df1-123">Пользователи, которым запрещено присоединяться к конференции</span><span class="sxs-lookup"><span data-stu-id="07df1-123">User(s) not allowed to join the conference</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07df1-124">Пользователи клиентов Lync VoIP с одного сайта сети</span><span class="sxs-lookup"><span data-stu-id="07df1-124">Lync VoIP client user(s) from a single network site</span></span></p></td>
<td><p><span data-ttu-id="07df1-125">Пользовательский клиент Lync VoIP с того же сайта сети</span><span class="sxs-lookup"><span data-stu-id="07df1-125">Lync VoIP client user from the same network site</span></span></p>
<p><span data-ttu-id="07df1-126">Пользовательский клиент Lync VoIP с другого сайта сети</span><span class="sxs-lookup"><span data-stu-id="07df1-126">Lync VoIP client user from a different network site</span></span></p>
<p><span data-ttu-id="07df1-127">Пользовательский клиент Lync VoIP с неизвестного сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="07df1-127">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="07df1-128">Пользователь федеративного клиента Lync VoIP</span><span class="sxs-lookup"><span data-stu-id="07df1-128">Federated Lync VoIP client user</span></span></p>
<p><span data-ttu-id="07df1-129">Пользователь, присоединяющийся с помощью конечной точки ТСОП</span><span class="sxs-lookup"><span data-stu-id="07df1-129">User joining from a PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="07df1-130">Нет</span><span class="sxs-lookup"><span data-stu-id="07df1-130">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07df1-131">Пользователи клиентов Lync VoIP с неизвестного сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="07df1-131">Lync VoIP client user(s) from an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="07df1-132">Пользовательский клиент Lync VoIP с любого сайта</span><span class="sxs-lookup"><span data-stu-id="07df1-132">Lync VoIP client user from any site</span></span></p>
<p><span data-ttu-id="07df1-133">Пользователь Lync для клиента VoIP с неизвестного сайта</span><span class="sxs-lookup"><span data-stu-id="07df1-133">Lync VoIP client user from an unknown site</span></span></p>
<p><span data-ttu-id="07df1-134">Пользователь федеративного клиента Lync VoIP</span><span class="sxs-lookup"><span data-stu-id="07df1-134">Federated Lync VoIP client user</span></span></p></td>
<td><p><span data-ttu-id="07df1-135">Пользователь, присоединяющийся с помощью конечной точки ТСОП</span><span class="sxs-lookup"><span data-stu-id="07df1-135">User joining via a PSTN endpoint</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07df1-136">Пользователи клиентов Lync VoIP с разных сетевых сайтов</span><span class="sxs-lookup"><span data-stu-id="07df1-136">Lync VoIP client users from different network sites</span></span></p></td>
<td><p><span data-ttu-id="07df1-137">Пользовательский клиент Lync VoIP с любого сайта сети</span><span class="sxs-lookup"><span data-stu-id="07df1-137">Lync VoIP client user from any network site</span></span></p>
<p><span data-ttu-id="07df1-138">Пользовательский клиент Lync VoIP с неизвестного сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="07df1-138">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="07df1-139">Пользователь федеративного клиента Lync VoIP</span><span class="sxs-lookup"><span data-stu-id="07df1-139">Federated Lync VoIP client user</span></span></p></td>
<td><p><span data-ttu-id="07df1-140">Пользователь, присоединяющийся с помощью конечной точки ТСОП</span><span class="sxs-lookup"><span data-stu-id="07df1-140">User joining via a PSTN endpoint</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07df1-141">Пользователи пользователей Lync VoIP с одного сайта сети и пользователями, присоединенными из конечной точки PSTN</span><span class="sxs-lookup"><span data-stu-id="07df1-141">Lync VoIP client user(s) from a single network site and users joining from a PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="07df1-142">Пользовательский клиент Lync VoIP с того же сайта сети</span><span class="sxs-lookup"><span data-stu-id="07df1-142">Lync VoIP client user from the same network site</span></span></p></td>
<td><p><span data-ttu-id="07df1-143">Пользовательский клиент Lync VoIP с другого сайта сети</span><span class="sxs-lookup"><span data-stu-id="07df1-143">Lync VoIP client user from a different network site</span></span></p>
<p><span data-ttu-id="07df1-144">Пользовательский клиент Lync VoIP с неизвестного сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="07df1-144">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="07df1-145">Пользователь федеративного клиента Lync VoIP</span><span class="sxs-lookup"><span data-stu-id="07df1-145">Federated Lync VoIP client user</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="07df1-146">Ниже описаны дополнительные характеристики приложения для конференц-связи Location-Based.</span><span class="sxs-lookup"><span data-stu-id="07df1-146">The following are additional characteristics of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="07df1-147">Если пользователю не разрешено присоединиться к Конференции, заданной Location-Based ограничениям маршрутизации, пользователи, вызывающие конференцию, будут отвергнуты, а клиент Lync сообщит о том, что звонок не был завершен или закончился.</span><span class="sxs-lookup"><span data-stu-id="07df1-147">When a user is not allowed to join a conference given Location-Based Routing restrictions, the users call to the conference will be rejected and his Lync Client will report that the call was not completed or has ended.</span></span>

  - <span data-ttu-id="07df1-148">Конечная точка PSTN, присоединяющаяся к Конференции с Location-Based принудительной маршрутизацией, не сможет присоединиться к Конференции вне зависимости от ее состояния, если конечная точка присоединяется по каналу, для которого не включена Location-Based маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="07df1-148">A PSTN endpoint joining a conference with Location-Based Routing enforcements will not be restricted to join the conference regardless of its state if the endpoint joins via a trunk that is not enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="07df1-149">Система УАТС, подключенная к серверу-источнику данных, на магистральной магистрали SIP, не использующая звонки в КТСОП, будет выполнять те же принудительные применения, что и пользователи Lync, находящиеся на веб-сайте, на котором определена магистральная сеть SIP.</span><span class="sxs-lookup"><span data-stu-id="07df1-149">A PBX system connected to a Mediations Server over a SIP trunk that does not egress calls to the PSTN will have the same enforcements as Lync users located in the same network site where the SIP trunk is defined.</span></span> <span data-ttu-id="07df1-150">Например, конечная точка PSTN сможет присоединиться к Конференции с помощью пользователя УАТС и пользователя Lync, если они находятся на одном сайте сети. в противном случае конечной точке PSTN не будет разрешено присоединиться к Конференции, если пользователь УАТС находится на другом сайте сети, чем пользователь Lync.</span><span class="sxs-lookup"><span data-stu-id="07df1-150">For example, a PSTN endpoint will be able to join a conference with a PBX user and a Lync user if they are located in the same network site; otherwise, the PSTN endpoint will not be allowed to join the conference if the PBX user is in a different network site than the Lync user.</span></span>

<span data-ttu-id="07df1-151"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07df1-151"></div>

<span> </span>

</div>

</div>

</span></span></div>

