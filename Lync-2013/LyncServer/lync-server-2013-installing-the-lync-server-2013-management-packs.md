---
title: 'Lync Server 2013: Установка пакетов управления Lync Server 2013'
description: 'Lync Server 2013: Установка пакетов управления Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: nstalling the Lync Server 2013 management packs
ms:assetid: b800d4ab-fdc8-4c72-a76a-b78932779fe3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205202(v=OCS.15)
ms:contentKeyID: 48185233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbb50146474211c12dbd95801ed2b20f6bbfd8c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426930"
---
# <a name="installing-the-lync-server-2013-management-packs"></a><span data-ttu-id="defe9-103">Установка пакетов управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="defe9-103">Installing the Lync Server 2013 management packs</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="defe9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="defe9-104">

<span> </span></span></span>

<span data-ttu-id="defe9-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="defe9-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="defe9-106">Сама по себе, System Center Operations Manager может отслеживать только небольшую часть операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="defe9-106">By itself, System Center Operations Manager has the ability to monitor only a small portion of the Windows operating system.</span></span> <span data-ttu-id="defe9-107">Однако вы можете расширять возможности System Center Operations Manager, устанавливая пакеты управления, программное обеспечение, которое определяет, какие элементы отслеживается System Center Operations Manager, в том числе сведения о том, как должны отслеживаться эти элементы, а также о том, как должны быть активированы и переданы оповещения.</span><span class="sxs-lookup"><span data-stu-id="defe9-107">However, you can extend the capabilities of System Center Operations Manager by installing management packs, software that dictates which items System Center Operations Manager can monitor, including how those items should be monitored and how alerts should be triggered and reported.</span></span> <span data-ttu-id="defe9-108">Microsoft Lync Server 2013 включает два пакета управления System Center Operations Manager, которые предоставляют следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="defe9-108">Microsoft Lync Server 2013 includes two System Center Operations Manager management packs that provide the following capabilities:</span></span>

  - <span data-ttu-id="defe9-109">Пакет управления компонентом и пользовательским интерфейсом (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) отслеживает проблемы Lync Server, записанные счетчиками производительности, которые регистрируются в журналах событий или записываются в записи сведений о вызовах (CDR) или в базе данных качества взаимодействия (QoE).</span><span class="sxs-lookup"><span data-stu-id="defe9-109">The Component and User Management Pack (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) tracks Lync Server issues recorded in event logs, registered by performance counters, or logged in the call detail records (CDR) or the Quality of Experience (QoE) databases.</span></span> <span data-ttu-id="defe9-110">Для критических проблем можно настроить System Center Operations Manager для немедленного уведомления администраторов с помощью электронной почты, обмена мгновенными сообщениями или службы коротких сообщений (SMS).</span><span class="sxs-lookup"><span data-stu-id="defe9-110">For critical problems, System Center Operations Manager can be configured to immediately notify administrators via email, instant message, or Short Message Service (SMS) messaging.</span></span> <span data-ttu-id="defe9-111">SMS — это технология, используемая для отправки текстовых сообщений с одного мобильного устройства на другое.</span><span class="sxs-lookup"><span data-stu-id="defe9-111">SMS is the technology used to send text messages from one mobile device to another.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="defe9-112">Дополнительные сведения о настройке уведомлений Operations Manager можно найти в разделе Настройка уведомлений в библиотеке TechNet по адресу <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A> .</span><span class="sxs-lookup"><span data-stu-id="defe9-112">For more information on configuring Operations Manager notification, see Configuring Notification in the TechNet Library at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A>.</span></span>

    
    </div>

  - <span data-ttu-id="defe9-113">Активный пакет мониторинга (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) проактивно проверяет ключевые компоненты сервера Lync, такие как вход в систему, Обмен мгновенными сообщениями и звонки на телефон, находящийся в коммутируемой телефонной сети с открытым коммутируемым подключением (КТСОП).</span><span class="sxs-lookup"><span data-stu-id="defe9-113">The Active Monitoring Pack (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) proactively tests key Lync Server components such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="defe9-114">Эти тесты выполняются с помощью виртуальных командлетов транзакций Lync Server.</span><span class="sxs-lookup"><span data-stu-id="defe9-114">These tests are conducted using the Lync Server synthetic transaction cmdlets.</span></span> <span data-ttu-id="defe9-115">Например, командлет **Test-CsIM** позволяет смоделировать сеанс обмена мгновенными сообщениями между двумя тестовыми пользователями.</span><span class="sxs-lookup"><span data-stu-id="defe9-115">For example, the **Test-CsIM** cmdlet is used to simulate an instant messaging conversation between a pair of test users.</span></span> <span data-ttu-id="defe9-116">Если имитируемый разговор о сообщениях завершается сбоем, будет создано предупреждение.</span><span class="sxs-lookup"><span data-stu-id="defe9-116">If this simulated messaging conversation fails an alert will be generated.</span></span>

<span data-ttu-id="defe9-117">В число двух пакетов управления, включенных в Lync Server 2013, входит большое количество улучшений по сравнению с пакетами управления, используемыми в Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="defe9-117">The two management packs included with Lync Server 2013 include a large number of enhancements over the management packs used with Microsoft Lync Server 2010.</span></span> <span data-ttu-id="defe9-118">Например, пакет управления компонентом Lync Server 2013 не ограничивается только мониторингом сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="defe9-118">For example, the Lync Server 2013 Component Management Pack is not limited to monitoring Lync Server itself.</span></span> <span data-ttu-id="defe9-119">В дополнение к мониторингу журналов событий и счетчиков производительности для Lync Server пакет управления компонентом также может отслеживать производительность и уведомления об ошибках, важных элементов, таких как:</span><span class="sxs-lookup"><span data-stu-id="defe9-119">In addition to monitoring event logs and performance counters for Lync Server, the Component Management pack can also track the performance of, and issue alerts for, crucial items such as:</span></span>

  - <span data-ttu-id="defe9-120">**Информационные службы Интернета (IIS)**   Если службы IIS переходят в автономный режим, оповещения будут выдаваться.</span><span class="sxs-lookup"><span data-stu-id="defe9-120">**Internet Information Services (IIS)**   Alerts will be issued if Internet Information Services goes offline.</span></span> <span data-ttu-id="defe9-121">Это важно, поскольку веб-службы Lync Server основываются на службах IIS.</span><span class="sxs-lookup"><span data-stu-id="defe9-121">This is important, because the Lync Server web services rely on IIS.</span></span>

  - <span data-ttu-id="defe9-122">**Использование процесса**   Если все ресурсы системы (например, доступная память) начинают работать достаточно, оповещения будут выдаваться.</span><span class="sxs-lookup"><span data-stu-id="defe9-122">**Process usage**   Alerts will be issued if system resources (such as available memory) begin to run low.</span></span> <span data-ttu-id="defe9-123">Эти оповещения будут выпускаться, даже если сервер Lync Server не отвечает за высокое использование системы.</span><span class="sxs-lookup"><span data-stu-id="defe9-123">These alerts will be issued even if Lync Server is not responsible for the high system usage.</span></span>

  - <span data-ttu-id="defe9-124">**События сбоя компьютера**   Оповещения выдаются в случае проблем с оборудованием и программным обеспечением, которые могут угрожать жизнеспособности сервера.</span><span class="sxs-lookup"><span data-stu-id="defe9-124">**Computer failure events**   Alerts will be issued in case of a hardware or software issue that threatens the viability of a server.</span></span> <span data-ttu-id="defe9-125">Например, администраторы сервера Lync Server получат уведомление о том, что сервер не подвержен опасности сбоя жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="defe9-125">For example, Lync Server administrators will be notified if a server appears to be in danger of experiencing a hard disk failure.</span></span>

<span data-ttu-id="defe9-126">Новые пакеты управления также расширяют возможности создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="defe9-126">The new management packs also feature enhanced reporting.</span></span> <span data-ttu-id="defe9-127">Новые отчеты для Lync Server 2013 включают:</span><span class="sxs-lookup"><span data-stu-id="defe9-127">New reports for Lync Server 2013 include:</span></span>

  - <span data-ttu-id="defe9-128">**Отчет о доступности сценариев "на**   конец"   В этом отчете подробно описана доступность и время бесперебойной работы для основных служб Lync Server, таких как регистрация или присутствие.</span><span class="sxs-lookup"><span data-stu-id="defe9-128">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="defe9-129">**Отчет о произв**   .   С помощью данных счетчиков производительности этот отчет показывает тенденции для системных компонентов, таких как доступность памяти и использование процессора.</span><span class="sxs-lookup"><span data-stu-id="defe9-129">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="defe9-130">**Отчет о компонентах**   В этом отчете перечислены основные генераторы оповещений, сгруппированные по компоненту Lync Server.</span><span class="sxs-lookup"><span data-stu-id="defe9-130">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="defe9-131">Помимо этих предустановленных отчетов, пакеты управления для Lync Server 2013 автоматически сообщают об оповещениях для обеспечения надежности обоих вызовов (метрики, измеряемые сведениями о вызовах) и состояния QoE (показатели измеряются качеством качества).</span><span class="sxs-lookup"><span data-stu-id="defe9-131">In addition to these predesigned reports, the management packs for Lync Server 2013 automatically report alerts for both Call Reliability (metrics measured by Call Detail Recording) and QoE states (metrics measured by Quality of Experience).</span></span> <span data-ttu-id="defe9-132">Если вы включили запись с подробными сведениями о вызовах, вы можете просмотреть оповещения о надежности звонков, выполнив следующую процедуру на консоли System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="defe9-132">If you have enabled Call Detail Recording, you can review Call Reliability alerts by completing the following procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="defe9-133">Разверните раздел **мониторинг**, разверните **Microsoft Lync Server 2013 Health**, разверните элемент **надежность и качество передачи**, а затем выберите пункт **надежность звонка**.</span><span class="sxs-lookup"><span data-stu-id="defe9-133">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then click **Call Reliability**.</span></span>

<span data-ttu-id="defe9-134">Чтобы просмотреть оповещения о QoS, выполните эту процедуру на консоли System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="defe9-134">To view Quality of Experience alerts, complete this procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="defe9-135">Разверните раздел **мониторинг**, разверните **Microsoft Lync Server 2013 Health**, разверните элемент **надежность и качество цветопередачи**, а затем разверните **качество мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="defe9-135">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then expand **Media Quality**.</span></span>

<span data-ttu-id="defe9-136">Пакеты управления для Lync Server 2013 теперь используют обнаружение на уровне компьютера вместо центрального механизма обнаружения, используемого в Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="defe9-136">The management packs for Lync Server 2013 now use machine-level discovery instead of the central discovery mechanism used in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="defe9-137">Это означает, что каждый агент System Center, по сути, выводит себя и сообщает о существовании основного сервера управления.</span><span class="sxs-lookup"><span data-stu-id="defe9-137">This means that each System Center agent essentially discovers itself and reports its existence to the Central Management Server.</span></span> <span data-ttu-id="defe9-138">Использование обнаружения на уровне компьютера упрощает администрирование инфраструктуры System Center, а также позволяет другим версиям пакетов управления Lync Server (например, пакетов управления для Lync Server 2010 и пакетов управления для Lync Server 2013) сосуществовать.</span><span class="sxs-lookup"><span data-stu-id="defe9-138">Using machine-level discovery simplifies administration of your System Center infrastructure and also allows different versions of the Lync Server management packs (for example, management packs for Lync Server 2010 and management packs for Lync Server 2013) to coexist.</span></span>

<span data-ttu-id="defe9-139"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="defe9-139"></div>

<span> </span>

</div>

</div>

</span></span></div>

