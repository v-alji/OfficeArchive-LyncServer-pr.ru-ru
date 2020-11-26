---
title: 'Lync Server 2013: компоненты VoIP сервера переднего плана'
description: 'Lync Server 2013: компоненты VoIP сервера переднего плана.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Front End Server VoIP components
ms:assetid: 310e81a7-da45-47d4-95d0-92837e386502
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425812(v=OCS.15)
ms:contentKeyID: 48183765
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9390d06cf6277ef79ec2ec785bad4b497bc04a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428043"
---
# <a name="front-end-server-voip-components-for-lync-server-2013"></a><span data-ttu-id="19b98-103">Компоненты VoIP сервера переднего плана для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19b98-103">Front End Server VoIP components for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19b98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19b98-104">

<span> </span></span></span>

<span data-ttu-id="19b98-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="19b98-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="19b98-106">Ниже указаны компоненты VoIP, расположенные на серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19b98-106">The VoIP components located on Front End Servers are as follows:</span></span>

  - <span data-ttu-id="19b98-107">cлужба перевода</span><span class="sxs-lookup"><span data-stu-id="19b98-107">Translation Service</span></span>

  - <span data-ttu-id="19b98-108">компонент маршрутизации входящих вызовов;</span><span class="sxs-lookup"><span data-stu-id="19b98-108">Inbound Routing component</span></span>

  - <span data-ttu-id="19b98-109">компонент маршрутизации исходящих вызовов;</span><span class="sxs-lookup"><span data-stu-id="19b98-109">Outbound Routing component</span></span>

  - <span data-ttu-id="19b98-110">компонент маршрутизации единой системы обмена сообщениями Exchange;</span><span class="sxs-lookup"><span data-stu-id="19b98-110">Exchange UM Routing component</span></span>

  - <span data-ttu-id="19b98-111">компонент маршрутизации между кластерами.</span><span class="sxs-lookup"><span data-stu-id="19b98-111">Intercluster Routing component</span></span>

  - [<span data-ttu-id="19b98-112">Компонент сервера «исправления» в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19b98-112">Mediation Server component in Lync Server 2013</span></span>](lync-server-2013-mediation-server-component.md)

<div>

## <a name="translation-service"></a><span data-ttu-id="19b98-113">Служба перевода</span><span class="sxs-lookup"><span data-stu-id="19b98-113">Translation Service</span></span>

<span data-ttu-id="19b98-p101">Служба перевода — это серверный компонент, который отвечает за преобразование набираемого номера в формат E.164 или другой формат согласно правилам нормализации, определенным администратором. Служба перевода может преобразовывать номера и в другие форматы, не только E.164, если ваша организация использует частную систему нумерации или шлюз или УАТС, которые не поддерживают формат E.164.</span><span class="sxs-lookup"><span data-stu-id="19b98-p101">The Translation Service is the server component that is responsible for translating a dialed number into the E.164 format or another format, according to the normalization rules that are defined by the administrator. The Translation Service can translate to formats other than E.164 if your organization uses a private numbering system or uses a gateway or PBX that does not support E.164.</span></span>

</div>

<div>

## <a name="inbound-routing-component"></a><span data-ttu-id="19b98-116">Компонент маршрутизации входящих пакетов</span><span class="sxs-lookup"><span data-stu-id="19b98-116">Inbound Routing Component</span></span>

<span data-ttu-id="19b98-117">Компонент маршрутизации входящей почты обрабатывает входящие звонки в значительной степени согласно настройкам, заданным пользователями на клиентских голосовых клиентах.</span><span class="sxs-lookup"><span data-stu-id="19b98-117">The Inbound Routing component handles incoming calls largely according to preferences that are specified by users on their Enterprise Voice clients.</span></span> <span data-ttu-id="19b98-118">Он также обеспечивает делегирование вызовов и одновременные вызовы, если эти функции настроены пользователем.</span><span class="sxs-lookup"><span data-stu-id="19b98-118">It also facilitates delegate ringing and simultaneous ringing, if configured by the user.</span></span> <span data-ttu-id="19b98-119">Например, пользователи задают требуемое действие для вызовов, оставшихся без ответа: переадресацию или регистрацию для уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b98-119">For example, users specify whether unanswered calls are forwarded or simply logged for notification.</span></span> <span data-ttu-id="19b98-120">Если включена переадресация звонков, пользователи могут указать, следует ли перенаправлять неотвеченные звонки на другой или сервер Exchange UM, настроенный для обеспечения ответа на звонки.</span><span class="sxs-lookup"><span data-stu-id="19b98-120">If call forwarding is enabled, users can specify whether unanswered calls should be forwarded to another number or to a Exchange UM server that has been configured to provide call answering.</span></span> <span data-ttu-id="19b98-121">Компонент маршрутизации входящих подключений устанавливается по умолчанию на всех серверах Standard Edition и серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19b98-121">The Inbound Routing component is installed by default on all Standard Edition server and Front End Servers.</span></span>

</div>

<div>

## <a name="outbound-routing-component"></a><span data-ttu-id="19b98-122">Компонент маршрутизации исходящих вызовов</span><span class="sxs-lookup"><span data-stu-id="19b98-122">Outbound Routing Component</span></span>

<span data-ttu-id="19b98-123">Компонент маршрутизации входящих вызовов предназначен для маршрутизации вызовов в УАТС или ТСОП.</span><span class="sxs-lookup"><span data-stu-id="19b98-123">The Outbound Routing component routes calls to PBX or PSTN destinations.</span></span> <span data-ttu-id="19b98-124">Он обеспечивает применение к вызывающим абонентам правил авторизации вызовов, определяемых пользовательской политикой голосовой связи, и выбор оптимального шлюза ТСОП для маршрутизации каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="19b98-124">It applies call authorization rules, as defined by the user’s voice policy, to callers and determines the optimal PSTN gateway for routing each call.</span></span> <span data-ttu-id="19b98-125">Компонент маршрутизации исходящих подключений устанавливается по умолчанию на всех серверах Standard Edition Server и интерфейсах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19b98-125">The Outbound Routing component is installed by default on all Standard Edition server and Front End Servers.</span></span>

<span data-ttu-id="19b98-126">Логика маршрутизации, используемая компонентом маршрутизации исходящих вызовов, в значительной степени настраивается сетью или администраторами телефонной связи в соответствии с требованиями организации.</span><span class="sxs-lookup"><span data-stu-id="19b98-126">The routing logic that is used by the Outbound Routing component is in large measure configured by network or telephony administrators according to the requirements of their organizations.</span></span>

</div>

<div>

## <a name="exchange-um-routing-component"></a><span data-ttu-id="19b98-127">Компонент маршрутизации единой системы обмена сообщениями Exchange</span><span class="sxs-lookup"><span data-stu-id="19b98-127">Exchange UM Routing Component</span></span>

<span data-ttu-id="19b98-128">Компонент маршрутизации UM Exchange обрабатывает маршрутизацию между сервером Lync и серверами, на которых работает единая система обмена сообщениями (UM), для интеграции Lync Server с функциями единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="19b98-128">The Exchange UM routing component handles routing between Lync Server and servers running Exchange Unified Messaging (UM), to integrate Lync Server with Unified Messaging features.</span></span>

<span data-ttu-id="19b98-129">Компонент маршрутизации UM Exchange также обрабатывает перенаправление голосовой почты через КТСОП в случае недоступности серверов Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="19b98-129">The Exchange UM routing component also handles rerouting of voice mail over the PSTN if Exchange UM servers are unavailable.</span></span> <span data-ttu-id="19b98-130">Если у вас есть корпоративная голосовая связь на сайтах филиалов, не имеющих отказоустойчивой глобальной сети на центральном сайте, работающее устройство филиала, которое развертывается на сайте филиала, обеспечивает бесперебойность голосовой почты для пользователей филиала во время отключения глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="19b98-130">If you have Enterprise Voice users at branch sites that do not have a resilient WAN link to a central site, the Survivable Branch Appliance that you deploy at the branch site provides voice mail survivability for branch users during a WAN outage.</span></span> <span data-ttu-id="19b98-131">Если ссылка на глобальную сеть недоступна, устройство с бесперебойной связью делает следующее:</span><span class="sxs-lookup"><span data-stu-id="19b98-131">When the WAN link is unavailable, the Survivable Branch Appliance does the following:</span></span>

  - <span data-ttu-id="19b98-132">переадресует неотвеченные вызовы по ТСОП на сервер единой системы обмена сообщениями Exchange в центральном узле;</span><span class="sxs-lookup"><span data-stu-id="19b98-132">reroutes unanswered calls over the PSTN to the Exchange Unified Messaging server in the central site</span></span>

  - <span data-ttu-id="19b98-133">обеспечивает пользователю возможность получения сообщений голосовой почты через ТСОП;</span><span class="sxs-lookup"><span data-stu-id="19b98-133">provides the ability for a user to retrieve voice mail messages over the PSTN</span></span>

  - <span data-ttu-id="19b98-134">ставит в очередь уведомления о пропущенных звонках, а затем загружает их на сервер единой системы обмена сообщениями Exchange при восстановлении канала глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="19b98-134">queues missed call notifications, and then uploads them to the Exchange UM server when the WAN link is restored.</span></span>

<span data-ttu-id="19b98-135">Чтобы включить перенаправление голосовой почты, мы рекомендуем администраторам Exchange настроить автосекретарь Exchange UM так, чтобы он принимал только сообщения.</span><span class="sxs-lookup"><span data-stu-id="19b98-135">To enable voice mail rerouting, we recommend that your Exchange administrator configure Exchange UM Auto Attendant (AA) to accept messages only.</span></span>

<span data-ttu-id="19b98-136">Подробнее об этих возможностях вы найдете [в разделе Планирование интеграции единой системы обмена сообщениями Exchange в Lync server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) и [Планирование устойчивости к корпоративной голосовой связи в Lync Server 2013](lync-server-2013-planning-for-enterprise-voice-resiliency.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="19b98-136">For details about these features, see [Planning for Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) and [Planning for Enterprise Voice resiliency in Lync Server 2013](lync-server-2013-planning-for-enterprise-voice-resiliency.md), respectively.</span></span>

</div>

<div>

## <a name="intercluster-routing-component"></a><span data-ttu-id="19b98-137">Компонент маршрутизации между кластерами</span><span class="sxs-lookup"><span data-stu-id="19b98-137">Intercluster Routing Component</span></span>

<span data-ttu-id="19b98-p105">Компонент маршрутизации между кластерами отвечает за маршрутизацию вызовов в основном пуле регистраторов вызываемого абонента. Если это недоступно, компонент перенаправляет вызов на резервный пул регистраторов. Если основной и резервный пулы регистраторов недоступны по сети IP, компонент маршрутизации между кластерами переадресует вызов по ТСОП на номер телефона пользователя.</span><span class="sxs-lookup"><span data-stu-id="19b98-p105">The Intercluster routing component is responsible for routing calls to the callee’s primary Registrar pool. If that is unavailable, the component routes the call to the callee’s backup Registrar pool. If the callee’s primary and backup Registrar pools are unreachable over the IP network, the Intercluster routing component reroutes the call over the PSTN to the user’s telephone number.</span></span>

</div>

<div>

## <a name="other-front-end-server-components-required-for-voip"></a><span data-ttu-id="19b98-141">Другие компоненты интерфейсных серверов, необходимые для VoIP</span><span class="sxs-lookup"><span data-stu-id="19b98-141">Other Front End Server Components Required for VoIP</span></span>

<span data-ttu-id="19b98-142">Другие компоненты, находящиеся на сервере или в директоре переднего плана, которые предоставляют важную поддержку для VoIP, но не являются компонентами VoIP, включают в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="19b98-142">Other components residing on the Front End Server or Director that provide essential support for VoIP, but are not themselves VoIP components, include the following:</span></span>

  - <span data-ttu-id="19b98-143">**Пользовательские службы.**</span><span class="sxs-lookup"><span data-stu-id="19b98-143">**User Services.**</span></span> <span data-ttu-id="19b98-144">Выполняют поиск обратного номера для целевого телефонного номера каждого входящего вызова и сопоставляют этот номер с SIP URI конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="19b98-144">Perform reverse number lookup on the destination phone number of each incoming call and match that number to the SIP URI of the destination user.</span></span> <span data-ttu-id="19b98-145">С помощью этой информации компонент маршрутизации входящих вызовов направляет вызов зарегистрированным конечным точкам SIP пользователя.</span><span class="sxs-lookup"><span data-stu-id="19b98-145">Using this information, the Inbound Routing component distributes the call to that user’s registered SIP endpoints.</span></span> <span data-ttu-id="19b98-146">Пользовательские службы — это основной компонент всех серверов и режиссеров переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19b98-146">User Services is a core component on all Front End Servers and Directors.</span></span>

  - <span data-ttu-id="19b98-147">**Репликатор пользователей.**</span><span class="sxs-lookup"><span data-stu-id="19b98-147">**User Replicator.**</span></span> <span data-ttu-id="19b98-148">Извлекает номера пользователей из доменных служб Active Directory и записывает их в таблицы в базе данных RTC, где они доступны для служб пользователей и сервера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="19b98-148">Extracts user phone numbers from Active Directory Domain Services and writes them to tables in the RTC database, where they are available to User Services and Address Book Server.</span></span> <span data-ttu-id="19b98-149">Репликатор пользователей — это основной компонент всех серверов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19b98-149">User Replicator is a core component on all Front End Servers.</span></span>

  - <span data-ttu-id="19b98-150">**Сервер адресной книги.**</span><span class="sxs-lookup"><span data-stu-id="19b98-150">**Address Book Server.**</span></span> <span data-ttu-id="19b98-151">Предоставление сведений о глобальном списке адресов из доменных служб Active Directory для клиентов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="19b98-151">Provides global address list information from Active Directory Domain Services to Lync Server clients.</span></span> <span data-ttu-id="19b98-152">Она также извлекает сведения о пользователях и контактах из базы данных RTC, записывает их в файлы адресной книги, а затем сохраняет их в общей папке, в которой они загружаются клиентами Lync.</span><span class="sxs-lookup"><span data-stu-id="19b98-152">It also retrieves user and contact information from the RTC database, writes the information to the Address Book files, and then stores the files on a shared folder where they are downloaded by Lync clients.</span></span> <span data-ttu-id="19b98-153">Сервер адресной книги записывает данные в базу данных RTCAb, которая используется службой веб-запросов в адресной книге для ответа на запросы на поиск пользователей из Microsoft Lync 2010 Mobile.</span><span class="sxs-lookup"><span data-stu-id="19b98-153">The Address Book Server writes the information to the RTCAb database, which is used by the Address Book Web Query service to respond to user search queries from Microsoft Lync 2010 Mobile.</span></span> <span data-ttu-id="19b98-154">При необходимости вы можете нормализовать номера корпоративных телефонов пользователей, которые записываются в базу данных RTC, для подготовки контактных лиц пользователей в Lync.</span><span class="sxs-lookup"><span data-stu-id="19b98-154">It optionally normalizes enterprise user phone numbers that are written to the RTC database for the purpose of provisioning user contacts in Lync.</span></span> <span data-ttu-id="19b98-155">Служба адресной книги устанавливается по умолчанию на всех серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19b98-155">The Address Book service is installed by default on all Front End Servers.</span></span> <span data-ttu-id="19b98-156">Служба веб-запросов по адресной книге устанавливается по умолчанию с веб-службами на каждом из серверов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="19b98-156">The Address Book Web Query service is installed by default with the Web services on each Front End Servers.</span></span>

<span data-ttu-id="19b98-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19b98-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

