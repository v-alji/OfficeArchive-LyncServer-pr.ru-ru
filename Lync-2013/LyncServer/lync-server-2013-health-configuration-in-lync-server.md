---
title: 'Lync Server 2013: Настройка работоспособности в Lync Server'
description: 'Lync Server 2013: Конфигурация работоспособности в Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Health configuration in Lync Server 2013
ms:assetid: c00a8c8e-c2d2-4557-8c42-211c7cc96550
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205234(v=OCS.15)
ms:contentKeyID: 48185305
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 999a6d5401cb34382a4120f9255c91c846f72422
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427650"
---
# <a name="health-configuration-in-lync-server-2013"></a><span data-ttu-id="3daa7-103">Конфигурация работоспособности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3daa7-103">Health configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3daa7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3daa7-104">

<span> </span></span></span>

<span data-ttu-id="3daa7-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="3daa7-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="3daa7-106">С помощью различных веб-сайтов, статей базы знаний Майкрософт и средств пакета ресурсов Lync Server администраторы, которые сталкиваются с проблемами при работе с Lync Server, никогда не смогут решить эти проблемы.</span><span class="sxs-lookup"><span data-stu-id="3daa7-106">Between various websites, Microsoft Knowledge Base articles, and Lync Server Resource Kit tools, administrators who encounter problems when running Lync Server are never far from a way to solve those problems.</span></span>

<span data-ttu-id="3daa7-107">Очевидно, что у вас нет возможности гарантировать отсутствие проблем с Lync Server 2013, так как Lync Server может повлиять на многие вещи, такие как сбои сети и сбои оборудования, которые сам продукт не может контролировать.</span><span class="sxs-lookup"><span data-stu-id="3daa7-107">Obviously there is no way to guarantee that you will never encounter problems with Lync Server 2013 because Lync Server can be affected by many things—like network crashes and hardware failures—that the product itself cannot control.</span></span> <span data-ttu-id="3daa7-108">Выполнив мониторинг работоспособности, администраторы могут выявить потенциальные проблемы, прежде чем они будут переключаться на реальные проблемы.</span><span class="sxs-lookup"><span data-stu-id="3daa7-108">By implementing health monitoring, administrators can identify potential problems before they turn into actual problems.</span></span> <span data-ttu-id="3daa7-109">Например, администраторы могут использовать функцию мониторинга сервера Lync Server для выявления тенденций и Tendencies.</span><span class="sxs-lookup"><span data-stu-id="3daa7-109">For example, administrators can use Lync Server monitoring to identify trends and tendencies.</span></span> <span data-ttu-id="3daa7-110">Например, при постоянном увеличении количества аудио-и видеоконференций может возникнуть необходимость добавить емкость, прежде чем система станет перегруженной.</span><span class="sxs-lookup"><span data-stu-id="3daa7-110">For example, a steady increase in the number of audio/video conferences might suggest a need to add capacity before the system becomes overloaded.</span></span>

<span data-ttu-id="3daa7-111">Аналогичным образом, администраторы могут использовать System Center Operations Manager для выполнения таких задач, как выявление предупреждений в реальном времени при возникновении указанных событий, а также выполнение искусственных транзакций для упреждающего тестирования системы.</span><span class="sxs-lookup"><span data-stu-id="3daa7-111">In a similar fashion, administrators can use System Center Operations Manager to do such things as issue real-time alerts when specified events occur, and to run synthetic transactions that proactively test the system.</span></span> <span data-ttu-id="3daa7-112">Синтетические транзакции используются в Lync Server, чтобы убедиться в том, что пользователи смогут успешно выполнять типичные задачи, такие как вход в систему, Обмен мгновенными сообщениями и звонки на телефоны, находящиеся в коммутируемой телефонной сети с открытым коммутируемым подключением (КТСОП).</span><span class="sxs-lookup"><span data-stu-id="3daa7-112">Synthetic transactions are used in Lync Server to verify that users are able to successfully complete common tasks such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="3daa7-113">Например, периодические выполнение этих тестов может оповещать вас о потенциальных проблемах с входом в Lync Server, а также о том, как устранить проблему, прежде чем служба поддержки будет передаваться с вызовами пользователей, которые не смогут установить соединение.</span><span class="sxs-lookup"><span data-stu-id="3daa7-113">For example, periodically running these tests can alert you to potential problems with users logging on to Lync Server, and give you a chance to correct the problem before your support team is flooded with calls from users unable to make a connection.</span></span> <span data-ttu-id="3daa7-114">С помощью System Center Operations Manager для выполнения этих искусственных транзакций администраторы могут регулярно отслеживать развертывание Lync Server в течение 24 часов в каждый день, не требуя от них каких-либо действий, Кроме того, чтобы отвечать на любые оповещения, которые могут быть выпущены.</span><span class="sxs-lookup"><span data-stu-id="3daa7-114">By using System Center Operations Manager to run these synthetic transactions, administrators can routinely monitor their deployment of Lync Server continuously for 24 hours every day without having to do much of anything beyond responding to any alerts that might be issued.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3daa7-115">Для Lync Server 2013 пакет управления System Center Operations Manager также может выявить проблемы внешнего сервера, которые могут негативно сказаться на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3daa7-115">For Lync Server 2013, the Management Pack for System Center Operations Manager is also able to detect "external" issues that can adversely affect Lync Server.</span></span> <span data-ttu-id="3daa7-116">Например, администраторы могут получать уведомления о том, что службы IIS переходят в автономный режим, системные ресурсы на компьютере Lync Server делятся ниже заданной величины, или на сервере Lync Server происходит сбой оборудования.</span><span class="sxs-lookup"><span data-stu-id="3daa7-116">For example, administrators can be notified if Internet Information Services (IIS) goes offline, system resources on a Lync Server computer fall below a specified amount, or a Lync Server computer experiences a hardware failure.</span></span>



</div>

<span data-ttu-id="3daa7-117">Конфигурация работоспособности в Lync Server 2013 встроена в System Center Operations Manager и использует пакеты управления Lync Server Management.</span><span class="sxs-lookup"><span data-stu-id="3daa7-117">Health configuration in Lync Server 2013 is built around System Center Operations Manager and the use of Lync Server Management Packs.</span></span> <span data-ttu-id="3daa7-118">Эти пакеты управления включают ряд новых функций и улучшений, в том числе:</span><span class="sxs-lookup"><span data-stu-id="3daa7-118">These Management Packs include a number of new features and enhancements, including:</span></span>

  - <span data-ttu-id="3daa7-119">**Доступность сценария из любого места.**</span><span class="sxs-lookup"><span data-stu-id="3daa7-119">**Scenario availability from any location.**</span></span> <span data-ttu-id="3daa7-120">В пакете управления Lync Server 2010 представлена концепция мониторинга доступности сценариев конечных пользователей с помощью искусственных транзакций.</span><span class="sxs-lookup"><span data-stu-id="3daa7-120">The Lync Server 2010 Management Pack introduced the concept of monitoring end user scenario availability with synthetic transactions.</span></span> <span data-ttu-id="3daa7-121">В Lync Server 2013 эти агенты содержат больше искусственных транзакций, и их можно запускать из различных расположений внутри предприятия, из удаленных географических расположений за пределами Организации, а также с помощью приложений филиалов и развертываний Lync Server 2010 для добавления покрытия в развертывания прежних версий.</span><span class="sxs-lookup"><span data-stu-id="3daa7-121">In Lync Server 2013, these agents have more synthetic transactions and can be run from a variety of locations inside the enterprise, from remote geographic locations outside of the enterprise, against branch office appliances and against Lync Server 2010 deployments to add coverage to legacy Edge deployments.</span></span>

  - <span data-ttu-id="3daa7-122">**Журналы виртуальных транзакций.**</span><span class="sxs-lookup"><span data-stu-id="3daa7-122">**Synthetic transaction logs.**</span></span> <span data-ttu-id="3daa7-123">Если виртуальная транзакция завершается сбоем, администраторы имеют доступ к журналам HTML, чтобы определить, что не удалось.</span><span class="sxs-lookup"><span data-stu-id="3daa7-123">When a synthetic transaction fails, administrators have access to HTML logs to help determine what failed.</span></span> <span data-ttu-id="3daa7-124">Сюда входит определение того, какое действие завершилось сбоем, задержка каждого действия, Командная строка, используемая для выполнения теста, и обнаружена ошибка.</span><span class="sxs-lookup"><span data-stu-id="3daa7-124">This includes understanding which action failed, the latency of each action, the command-line used to run the test, and the error that was encountered.</span></span>

  - <span data-ttu-id="3daa7-125">**Повышенная надежность звонков.**</span><span class="sxs-lookup"><span data-stu-id="3daa7-125">**Increased call reliability coverage.**</span></span> <span data-ttu-id="3daa7-126">Пакет управления Lync Server 2010 предлагает уведомления о надежности звонков для обнаружения проблем с серьезным подключением, которые влияют на голосовые звонки конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3daa7-126">The Lync Server 2010 Management Pack introduced call reliability alerting to detect severe connectivity issues that affect the audio calls of end users.</span></span> <span data-ttu-id="3daa7-127">В пакетах управления Lync Server 2013 вы можете добавлять сведения о том, как обмениваться мгновенными сообщениями в одноранговой сети и другим простыми возможностями конференции, обеспечивая более высокое качество и уменьшая шум.</span><span class="sxs-lookup"><span data-stu-id="3daa7-127">The Lync Server 2013 Management Packs add coverage for peer-to-peer instant messaging (IM) and other basic conferencing features to maximize coverage while reducing noise.</span></span>

  - <span data-ttu-id="3daa7-128">**Мониторинг зависимостей.**</span><span class="sxs-lookup"><span data-stu-id="3daa7-128">**Dependency monitoring.**</span></span> <span data-ttu-id="3daa7-129">Сценарии Lync Server могут завершаться сбоем из-за различных внешних факторов, таких как IIS, которые не подключены к сети, ограниченные ресурсы процессора и памяти, а также проблемы с диском.</span><span class="sxs-lookup"><span data-stu-id="3daa7-129">Lync Server scenarios can fail due to a variety of external factors such as IIS being offline, limited CPU and memory resources, and disk issues.</span></span> <span data-ttu-id="3daa7-130">Новые пакеты управления проверяют несколько критических зависимостей, чтобы администраторы могли узнать их влияние.</span><span class="sxs-lookup"><span data-stu-id="3daa7-130">The new management packs check several critical dependencies to ensure administrators are aware of their impact.</span></span>

  - <span data-ttu-id="3daa7-131">**Расширенные возможности создания отчетов.**</span><span class="sxs-lookup"><span data-stu-id="3daa7-131">**Enhanced reporting.**</span></span> <span data-ttu-id="3daa7-132">Набор отчетов, помогающих администраторам оценить доступность сценария, спланировать емкость и узнать, какие компоненты сталкиваются с наибольшим количеством проблем.</span><span class="sxs-lookup"><span data-stu-id="3daa7-132">A set of reports to help administrators estimate scenario availability, plan for capacity, and see which components are experiencing the most issues.</span></span>

<span data-ttu-id="3daa7-133">Пакеты управления включают в себя множество функций, помогающих найти и диагностировать, обеспечивая доступность в режиме реального времени для развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3daa7-133">The Management Packs also include a variety of features to help detect and diagnose provide real-time visibility into the health your Lync Server deployment.</span></span> <span data-ttu-id="3daa7-134">Эти функции перечислены в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3daa7-134">These features are listed in the following table.</span></span>

### <a name="management-pack-features"></a><span data-ttu-id="3daa7-135">Функции пакета управления</span><span class="sxs-lookup"><span data-stu-id="3daa7-135">Management Pack Features</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3daa7-136">Компонент</span><span class="sxs-lookup"><span data-stu-id="3daa7-136">Feature</span></span></th>
<th><span data-ttu-id="3daa7-137">Описание</span><span class="sxs-lookup"><span data-stu-id="3daa7-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3daa7-138">Искусственные транзакции</span><span class="sxs-lookup"><span data-stu-id="3daa7-138">Synthetic Transactions</span></span></p></td>
<td><p><span data-ttu-id="3daa7-139">Командлеты Windows PowerShell, которые можно запускать из различных местоположений, чтобы конечные пользователи могли использовать сценарии конечного пользователя, такие как вход, присутствие, мгновенные сообщения и конференции.</span><span class="sxs-lookup"><span data-stu-id="3daa7-139">Windows PowerShell cmdlets that can be run from various locations to ensure that end user scenarios such as sign-in, presence, IM, and conferencing are readily available to end users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3daa7-140">Оповещения о надежности звонков</span><span class="sxs-lookup"><span data-stu-id="3daa7-140">Call Reliability Alerts</span></span></p></td>
<td><p><span data-ttu-id="3daa7-141">Запросы к базе данных для записей с подробными сведениями о звонке (CDR).</span><span class="sxs-lookup"><span data-stu-id="3daa7-141">Database queries for Call Detail Records (CDR).</span></span> <span data-ttu-id="3daa7-142">Эти записи записываются серверами переднего плана, чтобы показать, удалось ли конечным пользователям подключаться к звонку или почему звонок был прерван.</span><span class="sxs-lookup"><span data-stu-id="3daa7-142">These records are written by Front End Servers to reflect whether end users were able to connect to a call or why a call was terminated.</span></span> <span data-ttu-id="3daa7-143">В этих запросах выводятся оповещения о том, что при подключении к одноранговой сети или основных функциях конференц-связи с большим количеством конечных пользователей возникают проблемы с подключением.</span><span class="sxs-lookup"><span data-stu-id="3daa7-143">These queries result in alerts that indicate when a wide range of end users are experiencing connectivity issues for peer-to-peer calls or basic conferencing functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3daa7-144">Уведомления о качестве мультимедиа</span><span class="sxs-lookup"><span data-stu-id="3daa7-144">Media Quality Alerts</span></span></p></td>
<td><p><span data-ttu-id="3daa7-145">Запросы к базам данных, которые проявляются отчетами качества взаимодействия (QoE), опубликованными клиентами в конце каждого звонка.</span><span class="sxs-lookup"><span data-stu-id="3daa7-145">Database queries that look at Quality of Experience (QoE) reports published by clients at the end of each call.</span></span> <span data-ttu-id="3daa7-146">В этих запросах выводятся уведомления о том, что при звонках и конференциях пользователи могут столкнуться с низким качеством мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3daa7-146">These queries result in alerts that pinpoint scenarios where users are likely to be experiencing poor media quality during calls and conferences.</span></span> <span data-ttu-id="3daa7-147">Данные строятся на основе метрик ключа, таких как задержка и потери пакетов, метрики, которые непосредственно влияют на качество связи.</span><span class="sxs-lookup"><span data-stu-id="3daa7-147">The data is built upon key metrics such as packet latency and loss, metrics that are known to directly contribute to call quality.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3daa7-148">Работоспособность компонента</span><span class="sxs-lookup"><span data-stu-id="3daa7-148">Component Health</span></span></p></td>
<td><p><span data-ttu-id="3daa7-149">Отдельные серверные компоненты создают оповещения с помощью журналов событий и счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="3daa7-149">Individual server components raise alerts by using event logs and performance counters.</span></span> <span data-ttu-id="3daa7-150">Эти оповещения указывают на ошибки, которые могут значительно повлиять на один или несколько сценариев конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3daa7-150">These alerts indicate failure conditions that can severely impact one or more end user scenarios.</span></span> <span data-ttu-id="3daa7-151">Эти оповещения также могут указывать на различные другие условия сбоя, в том числе на незапущенные службы, высокую частоту сбоев, высокую задержку сообщений или проблемы с подключением.</span><span class="sxs-lookup"><span data-stu-id="3daa7-151">These alerts can also indicate a variety of other failure conditions, including services not running, high failure rates, high message latency, or connectivity issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3daa7-152">Состояние зависимостей</span><span class="sxs-lookup"><span data-stu-id="3daa7-152">Dependency Health</span></span></p></td>
<td><p><span data-ttu-id="3daa7-153">Ошибки могут возникать по нескольким внешним причинам.</span><span class="sxs-lookup"><span data-stu-id="3daa7-153">Failures can occur for a variety of external reasons.</span></span> <span data-ttu-id="3daa7-154">Пакеты управления теперь отслеживают и собирают данные для некоторых критических внешних зависимостей, которые могут указывать на серьезные проблемы, в том числе сведения о доступности, ЦП и использовании памяти серверами, процессами и метриками дисков.</span><span class="sxs-lookup"><span data-stu-id="3daa7-154">The management packs now monitor and collect data for some of the critical external dependencies that might indicate severe issues, including IIS availability, CPU and memory usage of servers and processes, and disk metrics.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3daa7-155">Оповещения, выданные системой, отнесены на три основные категории:</span><span class="sxs-lookup"><span data-stu-id="3daa7-155">The alerts issued by the system have been classified into three general categories:</span></span>

  - <span data-ttu-id="3daa7-156">**Оповещения с высоким приоритетом.**</span><span class="sxs-lookup"><span data-stu-id="3daa7-156">**High-priority Alerts.**</span></span> <span data-ttu-id="3daa7-157">Эти оповещения указывают условия, которые приводят к сбою обслуживания для больших групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="3daa7-157">These alerts indicate conditions that will cause service outages for large groups of users.</span></span> <span data-ttu-id="3daa7-158">Например, сбой компонента на одном компьютере не является предупреждением высокого приоритета, так как Lync Server 2013 имеет встроенные функции высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="3daa7-158">For example, a component failure on a single machine is not a high-priority alert because Lync Server 2013 has built-in high availability features.</span></span> <span data-ttu-id="3daa7-159">Вместо этого оповещения с высоким приоритетом представляют проблемы, достаточно важные для администраторов по ночам.</span><span class="sxs-lookup"><span data-stu-id="3daa7-159">Instead, high-priority alerts represent problems serious enough “to wake up administrators at night.”</span></span> <span data-ttu-id="3daa7-160">Сообщения о нарушениях, обнаруженных искусственными транзакциями и автономными службами (например, аудио-и видеоконференцией), определяются как высокоприоритетные оповещения.</span><span class="sxs-lookup"><span data-stu-id="3daa7-160">Outages detected by synthetic transactions and offline services (for example, audio/video conferencing) qualify as high-priority alerts.</span></span>

  - <span data-ttu-id="3daa7-161">**Оповещения среднего приоритета.**..</span><span class="sxs-lookup"><span data-stu-id="3daa7-161">**Medium-priority alerts.**.</span></span> <span data-ttu-id="3daa7-162">Эти оповещения определяют условия, влияющие на подмножество пользователей или означающие снижение качества связи.</span><span class="sxs-lookup"><span data-stu-id="3daa7-162">These alerts indicate conditions that affect a subset of users or indicate call quality degradation.</span></span> <span data-ttu-id="3daa7-163">, В том числе проблемы, такие как сбои компонентов, задержка при звонке или снижение качества звука во время звонка.</span><span class="sxs-lookup"><span data-stu-id="3daa7-163">That includes problems such as component failures, latency in call establishment, or degraded audio quality in call.</span></span> <span data-ttu-id="3daa7-164">Оповещения в этой категории представляют собой состояние, которое указывает на текущее состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="3daa7-164">Alerts in this category are stateful and indicate the current status of the issue.</span></span> <span data-ttu-id="3daa7-165">Например, предположим, что срок вашего звонка превышает порог оповещения.</span><span class="sxs-lookup"><span data-stu-id="3daa7-165">For example, suppose your call establishment times exceed the alert threshold.</span></span> <span data-ttu-id="3daa7-166">Если при установленном звонке возвращаются значения Normal, эти оповещения будут автоматически устранены в System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="3daa7-166">If call establishment times return to normal, these alerts will be auto-resolved in System Center Operations Manager.</span></span> <span data-ttu-id="3daa7-167">Ожидание этих оповещений заключается в том, что администратор будет просматривать их в одном и том же деловом дне.</span><span class="sxs-lookup"><span data-stu-id="3daa7-167">The expectation for these alerts is that an administrator will look at them on the same business day.</span></span>

  - <span data-ttu-id="3daa7-168">**Другие оповещения.**</span><span class="sxs-lookup"><span data-stu-id="3daa7-168">**Other alerts.**</span></span> <span data-ttu-id="3daa7-169">Это оповещения от компонентов, которые могут повлиять на определенного пользователя или на подмножество пользователей.</span><span class="sxs-lookup"><span data-stu-id="3daa7-169">These are alerts from components that might affect a specific user or subset of users.</span></span> <span data-ttu-id="3daa7-170">Например, возможно, службе адресной книги не удалось проанализировать запись Active Directory для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3daa7-170">For example, perhaps the Address Book service could not parse the Active Directory entry of a given user.</span></span> <span data-ttu-id="3daa7-171">Ожидание этих оповещений заключается в том, что администраторы получают доступ к ним, когда они доступны.</span><span class="sxs-lookup"><span data-stu-id="3daa7-171">The expectation for these alerts is that administrators will get to them when they have time available.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3daa7-172">Содержание</span><span class="sxs-lookup"><span data-stu-id="3daa7-172">In This Section</span></span>

  - [<span data-ttu-id="3daa7-173">Настройка Lync Server 2013 для работы с System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="3daa7-173">Configuring Lync Server 2013 to work with System Center Operations Manager</span></span>](lync-server-2013-configuring-lync-server-to-work-with-system-center-operations-manager.md)

  - [<span data-ttu-id="3daa7-174">Использование расширенного ведения журнала для виртуальных транзакций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3daa7-174">Using rich logging for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-using-rich-logging-for-synthetic-transactions.md)

  - [<span data-ttu-id="3daa7-175">Использование Microsoft SQL Server 2008 R2 в качестве базы данных System Center Operations Manager для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3daa7-175">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>](lync-server-2013-using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database.md)

<span data-ttu-id="3daa7-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3daa7-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

