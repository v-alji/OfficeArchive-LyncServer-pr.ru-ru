---
title: 'Lync Server 2013: Общие сведения о мониторинге'
description: 'Lync Server 2013: Общие сведения о мониторинге.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of monitoring
ms:assetid: 5d5eb658-7fe0-42e6-acaf-700051d0a823
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204937(v=OCS.15)
ms:contentKeyID: 48184261
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 64f27d6aff71442c6193c220154af231481399ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445108"
---
# <a name="overview-of-monitoring-in-lync-server-2013"></a><span data-ttu-id="a6b46-103">Общие сведения об отслеживании в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6b46-103">Overview of monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6b46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6b46-104">

<span> </span></span></span>

<span data-ttu-id="a6b46-105">_**Тема последнего изменения:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="a6b46-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="a6b46-106">В Microsoft Lync Server 2013 контроль используется для сбора сведений об использовании и данных качества (QoE) для сеансов связи, в которых участвуют ваши пользователи.</span><span class="sxs-lookup"><span data-stu-id="a6b46-106">In Microsoft Lync Server 2013, monitoring is used to collect usage information and Quality of Experience (QoE) data about the communication sessions that your users are involved in.</span></span> <span data-ttu-id="a6b46-107">Сеанс — это обобщенный термин, который охватывает подключение пользователя к:</span><span class="sxs-lookup"><span data-stu-id="a6b46-107">A session is a generic term that covers a user’s connection to a:</span></span>

  - <span data-ttu-id="a6b46-108">Конференция</span><span class="sxs-lookup"><span data-stu-id="a6b46-108">Conference</span></span>

  - <span data-ttu-id="a6b46-109">Модальность конференции (например, аудио/видео или совместный доступ к приложениям)</span><span class="sxs-lookup"><span data-stu-id="a6b46-109">Conferencing modality (such as Audio/Video or Application Sharing)</span></span>

  - <span data-ttu-id="a6b46-110">Другой пользователь через одноранговую беседу, например через обмен мгновенными сообщениями или аудиовызов</span><span class="sxs-lookup"><span data-stu-id="a6b46-110">Another user via a peer-to-peer conversation such as instant messaging or an audio call</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6b46-111">Lync Server 2013 отслеживает сведения о каждом сеансе: кто вызвал пользователей; конечные точки, которые использовались в сеансе; время последнего сеанса; Каково воспринимаемое качество сеанса; и т. д.</span><span class="sxs-lookup"><span data-stu-id="a6b46-111">Lync Server 2013 keeps track of information about each session: who called who; which endpoints were used in the session; how long did the session last; what was the perceived quality of the session; and so on.</span></span> <span data-ttu-id="a6b46-112">Однако Lync Server не записывает и не сохраняет сам фактический звонок.</span><span class="sxs-lookup"><span data-stu-id="a6b46-112">However, Lync Server does not record and store the actual call itself.</span></span> <span data-ttu-id="a6b46-113">Кроме того, в том числе сеансы обмена мгновенными сообщениями: Несмотря на то, что в Lync Server записываются сведения о сеансах обмена мгновенными сообщениями, они не поддерживают запись всех сообщений, отправленных в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="a6b46-113">That includes instant messaging sessions as well: although Lync Server records information about instant messaging sessions, it does not maintain a record of each instant message that was sent during the session.</span></span>



</div>

<span data-ttu-id="a6b46-114">Сведения о звонках, собираемые Lync Server, можно использовать для любого количества применений, в том числе:</span><span class="sxs-lookup"><span data-stu-id="a6b46-114">The call detail information collected by Lync Server can be employed for any number of uses, including:</span></span>

  - <span data-ttu-id="a6b46-115">Рентабельность **инвестиций**.</span><span class="sxs-lookup"><span data-stu-id="a6b46-115">**Return on Investment (ROI)**.</span></span> <span data-ttu-id="a6b46-116">Администраторы могут сравнивать данные об использовании, собранные сервером мониторинга, на похожие данные, собранные для предыдущей системы телефонной связи, чтобы показать экономию затрат и получить помощь по выравниванию развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a6b46-116">Administrators can compare the usage data collected by Monitoring Server to similar data collected for their previous telephony system in order to show cost savings and help justify the deployment of Lync Server.</span></span>

  - <span data-ttu-id="a6b46-117">**Управление инвентаризацией устройств**.</span><span class="sxs-lookup"><span data-stu-id="a6b46-117">**Device Inventory Management**.</span></span> <span data-ttu-id="a6b46-118">Сведения об управлении активами помогают администраторам идентифицировать старые устройства, которые необходимо заменить, а также определять ресурсоемкие устройства, которые не будут использоваться вообще.</span><span class="sxs-lookup"><span data-stu-id="a6b46-118">Asset management information helps administrators identify old devices still in use that need to be replaced, as well as identify expensive devices that do not appear to be getting used at all.</span></span>

  - <span data-ttu-id="a6b46-119">Службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="a6b46-119">Help Desk.</span></span> <span data-ttu-id="a6b46-120">Данные по устранению неполадок позволяют специалистам службы поддержки определить, почему не удается выполнить звонок пользователя, и не нужно собирать журналы на стороне сервера или клиента.</span><span class="sxs-lookup"><span data-stu-id="a6b46-120">Troubleshooting data enables support engineers to determine why a user’s call failed, and to do so without having to collect server or client side logs.</span></span> <span data-ttu-id="a6b46-121">Эти сведения можно легко получить и обучены специалистами службы поддержки, которые не имеют глубоких технических знаний о Microsoft Lync 2013 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6b46-121">This information can be readily accessed and understood by support personnel who do not have a deep technical knowledge of Microsoft Lync 2013 and Lync Server 2013.</span></span>

  - <span data-ttu-id="a6b46-p106">**Устранение системных неполадок**. Администраторы могут определять серьезные неполадки, которые приведут к невозможности пользователей выполнять базовые задачи, например присоединяться к конференции, выполнять вызов или отправлять мгновенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="a6b46-p106">**System Troubleshooting**. Enables administrators to detect major issues that might prevent end users from performing basic tasks like joining a conference, establishing a call, or sending an instant message.</span></span>

<span data-ttu-id="a6b46-124">В дополнение к этим базовым сведениям о вызовах сервер мониторинга также предоставляет механизм, разрешающий конечные точки SIP (например, Lync 2013) для предоставления сведений для устранения неполадок, доступ к которым в противном случае не имеет доступа к этому серверу:</span><span class="sxs-lookup"><span data-stu-id="a6b46-124">In addition to this basic call information, the Monitoring Server also provides a mechanism that allows SIP endpoints (such as Lync 2013) to provide troubleshooting information that the server would not otherwise have access to:</span></span>

  - <span data-ttu-id="a6b46-125">**Показатели мультимедиа, влияющие на качество**.</span><span class="sxs-lookup"><span data-stu-id="a6b46-125">**Media Metrics that Impact Quality**.</span></span> <span data-ttu-id="a6b46-126">Эти показатели связаны с фактической передачей самого звонка; Это значит, что они предоставляют журнал командировок в качестве поездки на звонки по сети.</span><span class="sxs-lookup"><span data-stu-id="a6b46-126">These metrics deal with the actual transmission of the call itself; that is, they provide a sort of travel log as the call journeys across the network.</span></span> <span data-ttu-id="a6b46-127">Эти показатели (в том числе такие вещи, как потери пакетов, колебаний и время приема-передачи) предоставляют сведения о том, что произошло с моментом, когда он оставил конечную точку, на момент ее прибытия на конечную точку другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6b46-127">These metrics (which include such things as packet loss, jitter, and round trip times) provide information on what happened to the call from the time it left your endpoint to the time it arrived at the other person's endpoint.</span></span>

  - <span data-ttu-id="a6b46-128">**Ошибки, о которых было сообщено пользователю**.</span><span class="sxs-lookup"><span data-stu-id="a6b46-128">**Issues Reported to the End User**.</span></span> <span data-ttu-id="a6b46-129">Эти показатели включают недокачественные уведомления, которые Lync 2013 представляет конечные пользователи в тех случаях, когда они слишком далеко от микрофона, говорят, что они слишком тихо, плохо подключены к сети или имеют низкое качество, так как другая программа на компьютере потребляет доступные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a6b46-129">These metrics include poor quality notifications that Lync 2013 presents to end users in cases where they are too far from a microphone, speaking too softly, have a poor network connection, or are experiencing poor quality because another program on the computer is consuming the available resources.</span></span>

  - <span data-ttu-id="a6b46-p109">**Сведения о среде**. Сюда входят показатели, которые описывают такие факторы качества связи, как используемый тип микрофона и динамиков, подключается ли пользователь через VPN, используется ли беспроводное подключение.</span><span class="sxs-lookup"><span data-stu-id="a6b46-p109">**Environment Information**. These metrics detail call quality factors such as the type of microphone and speakers being used, whether the user is connected through a VPN connection, and whether the user is on a wireless connection.</span></span>

<span data-ttu-id="a6b46-132">В конце каждого звонка конечные точки, совместимые с SIP, автоматически передают эти данные на сервер переднего плана, который упрощает этот звонок.</span><span class="sxs-lookup"><span data-stu-id="a6b46-132">At the end of each call, SIP-compliant endpoints automatically transmit this information to the Front End server that facilitated the call.</span></span> <span data-ttu-id="a6b46-133">Нет необходимости предпринимать какие-либо действия для передачи этих сведений с конечных точек, так как подобное поведение характерно для протокола SIP.</span><span class="sxs-lookup"><span data-stu-id="a6b46-133">You don't have to do anything to get endpoints to transmit that information; that behavior is built into the SIP protocol.</span></span> <span data-ttu-id="a6b46-134">Однако если необходимо собрать и сохранить эти данные, необходимо установить и включить компонент мониторинга.</span><span class="sxs-lookup"><span data-stu-id="a6b46-134">However, if you want to collect and store that information, then you need to install and enable monitoring.</span></span> <span data-ttu-id="a6b46-135">В этом случае сведения о вызовах будут собираться агентами, работающими на сервере переднего плана, и заноситься в две базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a6b46-135">If you do install and enable monitoring, then call information is gathered by agents running on the Front End server and relayed to a pair of SQL Server databases.</span></span>

<span data-ttu-id="a6b46-136">Обратите внимание на то, что процесс установки и настройки мониторинга упрощен в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6b46-136">Note that the process of installing and configuring monitoring has been simplified in Lync Server 2013.</span></span> <span data-ttu-id="a6b46-137">В предыдущих версиях программного обеспечения для мониторинга требуется отдельная роль сервера мониторинга, что обычно означает отдельный компьютер, который можно использовать в качестве сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="a6b46-137">In prior versions of the software, monitoring required a separate Monitoring Server role, which typically meant a separate computer set aside for use as the Monitoring Server.</span></span> <span data-ttu-id="a6b46-138">Однако в Lync Server 2013 роль сервера мониторинга была исключена.</span><span class="sxs-lookup"><span data-stu-id="a6b46-138">In Lync Server 2013, however, the Monitoring Server role has been eliminated.</span></span> <span data-ttu-id="a6b46-139">Вместо этого служба мониторинга (в виде "агенты Объединенного сбора данных") была выровнена на всех серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="a6b46-139">Instead, the monitoring service (in the form of "unified data collection agents") has been collocated into all Front End servers.</span></span> <span data-ttu-id="a6b46-140">Это по крайней мере два основных преимущества.</span><span class="sxs-lookup"><span data-stu-id="a6b46-140">This has at least two major benefits.</span></span> <span data-ttu-id="a6b46-141">Совыровнение службы мониторинга:</span><span class="sxs-lookup"><span data-stu-id="a6b46-141">Collocation of the monitoring service:</span></span>

  - <span data-ttu-id="a6b46-142">Уменьшает количество ролей сервера, необходимых при внедрении Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6b46-142">Decreases the number of server roles required when implementing Lync Server 2013.</span></span> <span data-ttu-id="a6b46-143">Уменьшение расходов на роль сервера мониторинга также способствует снижению затрат, устраняя необходимость поддерживать выделенные серверы для наблюдения.</span><span class="sxs-lookup"><span data-stu-id="a6b46-143">Decrementing the Monitoring Server role also helps reduce costs by eliminating the need to maintain dedicated servers for monitoring.</span></span>

  - <span data-ttu-id="a6b46-144">Сокращает сложность настройки и администрирования Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6b46-144">Reduces the complexity of Lync Server 2013 setup and administration.</span></span> <span data-ttu-id="a6b46-145">Выполнив разгруппировку служб наблюдения на каждом сервере переднего плана, вам больше не нужно устанавливать и настраивать роль сервера мониторинга, а также управлять ею.</span><span class="sxs-lookup"><span data-stu-id="a6b46-145">By collocating the monitoring services on each Front End server you no longer have to install, configure, and manage the Monitoring Server role.</span></span>

<span data-ttu-id="a6b46-146">Дополнительные сведения содержатся в разделе [развертывание мониторинга в Lync server 2013](lync-server-2013-deploying-monitoring.md) в руководстве по развертыванию lync Server 2013 2013.</span><span class="sxs-lookup"><span data-stu-id="a6b46-146">For more information see the topic [Deploying monitoring in Lync Server 2013](lync-server-2013-deploying-monitoring.md) in the Lync Server 2013 2013 deployment guide.</span></span>

<span data-ttu-id="a6b46-147"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6b46-147"></div>

<span> </span>

</div>

</div>

</span></span></div>

