---
title: 'Lync Server 2013: операционные зависимости'
description: 'Lync Server 2013: операционные зависимости.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operational dependencies
ms:assetid: 450b6be2-7fb3-47d7-8b0b-c05faa331e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720559(v=OCS.15)
ms:contentKeyID: 63969597
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e240981f5dfded7c27f123c8483794ea3ffedff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445297"
---
# <a name="operational-dependencies-in-lync-server-2013"></a><span data-ttu-id="6652b-103">Операционные зависимости в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6652b-103">Operational dependencies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6652b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6652b-104">

<span> </span></span></span>

<span data-ttu-id="6652b-105">_**Тема последнего изменения:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="6652b-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="6652b-106">Эталонная архитектура, обсуждаемая в этом документе, поможет вам убедиться в том, что у вас есть развертывание Lync Server 2013, которое не только масштабируется по требованиям Организации, но является архитектором в соответствии с рекомендациями Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6652b-106">The Reference Architecture discussed in this document will help ensure that you have a Lync Server 2013 deployment that not only scales to the organization’s requirements but is architected as per Microsoft best practices.</span></span> <span data-ttu-id="6652b-107">Это может быть так, что в случае, если реализация Lync Server 2013 является динамической службой, а также в любой другой службе в предприятии для обеспечения высокого уровня доступности и качества обслуживания для бизнеса требуется мониторинг и профилактическое управление.</span><span class="sxs-lookup"><span data-stu-id="6652b-107">Be that as it may the Lync Server 2013 implementation is a dynamic service and like any other service in the enterprise still requires monitoring and proactive management to maintain high level of service availability and service quality to the business.</span></span>

<span data-ttu-id="6652b-108">Поскольку Lync Server 2013 становится детально неструктурированными в повседневной деятельности Организации, важно, чтобы служба управлялась точным и материальным уровнем обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6652b-108">As Lync Server 2013 becomes deeply ingrained in the organization’s everyday business it is important that the service be managed by accurate and tangible service level management.</span></span> <span data-ttu-id="6652b-109">Архитектура системы Lync может быть сложной и интегрированной, а также для обеспечения эффективной управления уровнем обслуживания и определения соглашений об оценках эффективности для Lync Server 2013, что важно для понимания зависимостей системы на других платформах и серверах.</span><span class="sxs-lookup"><span data-stu-id="6652b-109">The Lync system architecture can become complex and very integrated and in order to maintain effective service level management and establish SLAs for Lync Server 2013 it becomes critical to understand the system’s dependencies on other platforms and servers.</span></span> <span data-ttu-id="6652b-110">Важно отметить, какие бизнес-службы, например интегрированные приложения для голосовой связи и Объединенных коммуникаций, стали зависеть от Lync.</span><span class="sxs-lookup"><span data-stu-id="6652b-110">Equally important is to note which business services, such as voice and UC integrated applications, become dependent on Lync.</span></span>

<span data-ttu-id="6652b-111">Необходимо установить Lync Server 2013, указывая все просказанные зависимости.</span><span class="sxs-lookup"><span data-stu-id="6652b-111">Lync Server 2013 must be established noting all the said dependencies.</span></span> <span data-ttu-id="6652b-112">Карта обслуживания позволит вам сформулировать соглашение об уровне обслуживания между Lync и зависимой службой, а также предоставить начальное место для согласования SLA.</span><span class="sxs-lookup"><span data-stu-id="6652b-112">The service map will allow you to formulate a SLA between Lync and its dependent service and provide a starting place for SLA negotiation.</span></span>

<span data-ttu-id="6652b-113">В следующей таблице перечислены типичные службы зависимостей для инфраструктуры Lync.</span><span class="sxs-lookup"><span data-stu-id="6652b-113">The following table lists the typical dependency services for a Lync infrastructure.</span></span> <span data-ttu-id="6652b-114">Каждая из этих технологий должна иметь собственный активный мониторинг.</span><span class="sxs-lookup"><span data-stu-id="6652b-114">Each of these technologies should have its own proactive monitoring.</span></span>

### <a name="typical-dependency-services"></a><span data-ttu-id="6652b-115">Типичные службы зависимостей</span><span class="sxs-lookup"><span data-stu-id="6652b-115">Typical dependency services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6652b-116">Служба зависимостей</span><span class="sxs-lookup"><span data-stu-id="6652b-116">Dependency Service</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6652b-117">Операционные системы</span><span class="sxs-lookup"><span data-stu-id="6652b-117">Operating systems</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-118">Оборудование сервера</span><span class="sxs-lookup"><span data-stu-id="6652b-118">Server Hardware</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-119">Active Directory</span><span class="sxs-lookup"><span data-stu-id="6652b-119">Active Directory</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-120">Инфраструктура открытых ключей</span><span class="sxs-lookup"><span data-stu-id="6652b-120">Public Key Infrastructure</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-121">Служба именования доменов</span><span class="sxs-lookup"><span data-stu-id="6652b-121">Domain Naming Service</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-122">Службы баз данных</span><span class="sxs-lookup"><span data-stu-id="6652b-122">Database Services</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-123">Службы хранилища</span><span class="sxs-lookup"><span data-stu-id="6652b-123">Storage Services</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-124">Управление системой — мониторинг и распространение</span><span class="sxs-lookup"><span data-stu-id="6652b-124">System Management – Monitoring and distribution</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-125">Службы безопасности — антивирусная программа</span><span class="sxs-lookup"><span data-stu-id="6652b-125">Security Services - Antivirus</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-126">Сетевая инфраструктура — Интернет</span><span class="sxs-lookup"><span data-stu-id="6652b-126">Network Infrastructure - Internet</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-127">Сетевая инфраструктура – внутренняя (ЛВС/WAN)</span><span class="sxs-lookup"><span data-stu-id="6652b-127">Network Infrastructure – Internal (LAN/WAN)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-128">Инфраструктура телефонии — IP-УАТС и шлюзы</span><span class="sxs-lookup"><span data-stu-id="6652b-128">Telephony Infrastructure – IP-PBX and Gateways</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-129">Облачные службы</span><span class="sxs-lookup"><span data-stu-id="6652b-129">Cloud Services</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6652b-130">Предполагается, что Организация работает в соответствии с основными функциями управления уровнем обслуживания, такими как изменение, инцидент и управление выпуском, как это было предписано MOF.</span><span class="sxs-lookup"><span data-stu-id="6652b-130">It is assumed that the organization is operationally mature in exercising basic service level management functions such as change, incident and release management as prescribed by the MOF.</span></span> <span data-ttu-id="6652b-131">Решение Lync должно быть принято с помощью этих функций и может быть подвергнуто тем же процессам управления в рабочем процессе.</span><span class="sxs-lookup"><span data-stu-id="6652b-131">The Lync solution should be adopted by these functions and become subject to the same operational management processes.</span></span>

<span data-ttu-id="6652b-132">Создание на приведенных выше данных позволяет получить более общее представление о том, что может повлиять на работу службы Lync в предприятии.</span><span class="sxs-lookup"><span data-stu-id="6652b-132">Building on the information obtained above we now have a greater understanding of what can impact the Lync service in the enterprise.</span></span> <span data-ttu-id="6652b-133">Чтобы обеспечить доступность и качество обслуживания в Lync Server 2013, следующие средства мониторинга должны сопровождаться развертыванием эталонной архитектуры.</span><span class="sxs-lookup"><span data-stu-id="6652b-133">To help ensure Lync Server 2013 service availability and quality, the following monitoring tools must accompany the reference architecture deployment:</span></span>

### <a name="monitoring-tools"></a><span data-ttu-id="6652b-134">Средства наблюдения</span><span class="sxs-lookup"><span data-stu-id="6652b-134">Monitoring tools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6652b-135">Компонент</span><span class="sxs-lookup"><span data-stu-id="6652b-135">Component</span></span></th>
<th><span data-ttu-id="6652b-136">Описание</span><span class="sxs-lookup"><span data-stu-id="6652b-136">Description</span></span></th>
<th><span data-ttu-id="6652b-137">Соответствующий сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-137">Applicable Site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6652b-138">Сервер мониторинга Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6652b-138">Lync Server 2013 Monitoring Server</span></span></p></td>
<td><p><span data-ttu-id="6652b-139">Разверните по крайней мере одну роль сервера Lync Server 2013 для каждого центрального сайта и настройте пакет подготовки отчетов о качестве опыта работы (QoE).</span><span class="sxs-lookup"><span data-stu-id="6652b-139">Deploy at least one Lync Server 2013 Monitoring Server role per Central site and configure Quality of Experience (QoE) Reporting Pack.</span></span></p>
<p><span data-ttu-id="6652b-140">Дополнительные сведения можно найти в документации по развертыванию Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6652b-140">Refer to the Lync Server 2013 Deployment documentation for further details:</span></span></p>
<p><span data-ttu-id="6652b-141"><a href="lync-server-2013-deploying-monitoring.md">Развертывание мониторинга в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6652b-141"><a href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="6652b-142">Центральные сайты</span><span class="sxs-lookup"><span data-stu-id="6652b-142">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="6652b-143">Модем каждый из них является ближайшим экземпляром роли сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="6652b-143">Tether each pool to its nearest instance of the Monitoring Server role.</span></span></p></td>
<td><p><span data-ttu-id="6652b-144">Центральные сайты</span><span class="sxs-lookup"><span data-stu-id="6652b-144">Central sites</span></span></p>
<p><span data-ttu-id="6652b-145">Сайты филиалов</span><span class="sxs-lookup"><span data-stu-id="6652b-145">Branch sites</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-146">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="6652b-146">System Center Operations Manager 2012</span></span></p></td>
<td><p><span data-ttu-id="6652b-147">System Center Operations Manager 2012 с импортированным пакетом управления Microsoft Lync Server 2013 (MP).</span><span class="sxs-lookup"><span data-stu-id="6652b-147">System Center Operations Manager 2012 with the Microsoft Lync Server 2013 Management Pack (MP) imported.</span></span></p>
<p><span data-ttu-id="6652b-148">Пакет управления реализует традиционный журнал событий и инструментарий на основе счетчиков производительности, а также возможность для новых доступных инструментов в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6652b-148">The Management Pack implements traditional Event Log and Performance counter based instrumentation is utilized as well as enabling newly available instrumentation in Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="6652b-149">Центральные сайты</span><span class="sxs-lookup"><span data-stu-id="6652b-149">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="6652b-150">Убедитесь, что центральное обнаружение для обнаружения ролей и компонентов, которые необходимо отслеживать, выполняется автоматически на основе основного сценария обнаружения, который считывает документ Topology, опубликованный в базе данных централизованного управления.</span><span class="sxs-lookup"><span data-stu-id="6652b-150">Make sure that Central Discovery to discovery of roles and components that need to be monitored are automatically completed based on a central discovery script that reads the topology document published in Central Management Database.</span></span></p></td>
<td><p><span data-ttu-id="6652b-151">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-151">Central Site</span></span></p>
<p><span data-ttu-id="6652b-152">Сайт ветви</span><span class="sxs-lookup"><span data-stu-id="6652b-152">Branch Site</span></span></p>
<p><span data-ttu-id="6652b-153">Сайт Edge</span><span class="sxs-lookup"><span data-stu-id="6652b-153">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="6652b-154">Развертывание агентов System Centre Operations Manager 2007 для всех развернутых серверов с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6652b-154">Deploy System Centre Operations Manager 2007 agents to all deployed servers running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="6652b-155">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-155">Central Site</span></span></p>
<p><span data-ttu-id="6652b-156">Сайт ветви</span><span class="sxs-lookup"><span data-stu-id="6652b-156">Branch Site</span></span></p>
<p><span data-ttu-id="6652b-157">Сайт Edge</span><span class="sxs-lookup"><span data-stu-id="6652b-157">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="6652b-158">Убедитесь, что для уведомлений заданы приоритеты оповещений:</span><span class="sxs-lookup"><span data-stu-id="6652b-158">Make sure Prioritized Alerts are configured for notification:</span></span></p>
<p><span data-ttu-id="6652b-159">Оповещения с высоким приоритетом</span><span class="sxs-lookup"><span data-stu-id="6652b-159">High Priority Alerts</span></span></p>
<p><span data-ttu-id="6652b-160">Оповещения среднего приоритета</span><span class="sxs-lookup"><span data-stu-id="6652b-160">Medium Priority Alerts</span></span></p>
<p><span data-ttu-id="6652b-161">Другие оповещения.</span><span class="sxs-lookup"><span data-stu-id="6652b-161">Other Alerts.</span></span></p></td>
<td><p><span data-ttu-id="6652b-162">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-162">Central Site</span></span></p>
<p><span data-ttu-id="6652b-163">Сайт ветви</span><span class="sxs-lookup"><span data-stu-id="6652b-163">Branch Site</span></span></p>
<p><span data-ttu-id="6652b-164">Сайт Edge</span><span class="sxs-lookup"><span data-stu-id="6652b-164">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="6652b-165">Настройте мониторинг порта для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6652b-165">Configure Port monitoring for your deployment.</span></span></p></td>
<td><p><span data-ttu-id="6652b-166">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-166">Central Site</span></span></p>
<p><span data-ttu-id="6652b-167">Сайт ветви</span><span class="sxs-lookup"><span data-stu-id="6652b-167">Branch Site</span></span></p>
<p><span data-ttu-id="6652b-168">Сайт Edge</span><span class="sxs-lookup"><span data-stu-id="6652b-168">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="6652b-169">Настройка мониторинга URL-адресов для развертывания</span><span class="sxs-lookup"><span data-stu-id="6652b-169">Configure URL monitoring for your deployment</span></span></p></td>
<td><p><span data-ttu-id="6652b-170">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-170">Central Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-171">Интеграция Lync и System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="6652b-171">Lync and System Center Operations Manager integration</span></span></p></td>
<td><p><span data-ttu-id="6652b-172">Развертывание повышает надежность и качество цветопередачи MonitoringCall надежность и контроль качества мультимедиа. для наблюдения за надежностью и качеством звонков для Lync Server используйте компьютер сервера мониторинга в качестве узла-наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="6652b-172">Deploy Call Reliability and Media Quality MonitoringCall reliability and media quality monitoring use the Monitoring Server computer as their watcher node to monitor call reliability and media quality of Lync Server.</span></span> <span data-ttu-id="6652b-173">Обе эти функции запрашивают анализ баз данных сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="6652b-173">Both of these features query the Monitoring Server databases to do analysis.</span></span></p></td>
<td><p><span data-ttu-id="6652b-174">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-174">Central Site</span></span></p>
<p><span data-ttu-id="6652b-175">Сайт ветви</span><span class="sxs-lookup"><span data-stu-id="6652b-175">Branch Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="6652b-176">Убедитесь в том, что пороговые значения предупреждений для качества мультимедиа заданы правильно.</span><span class="sxs-lookup"><span data-stu-id="6652b-176">Ensure Media Quality warning thresholds are accurately configured.</span></span> <span data-ttu-id="6652b-177">В приведенной ниже таблице показано, как с помощью кодека узнать о максимальном прохождении в сети.</span><span class="sxs-lookup"><span data-stu-id="6652b-177">The following table indicates the maximum Network Mean Opinion Scores by Codec.</span></span> <span data-ttu-id="6652b-178">В производстве эти показатели следует отслеживать в течение установленного периода, а приемлемые пороги должны быть установлены на основе NMOSных показателей Организации.</span><span class="sxs-lookup"><span data-stu-id="6652b-178">In production these scores should be monitored for a set period and acceptable thresholds must be established based on the organization specific NMOS scores.</span></span></p></td>
<td><p><span data-ttu-id="6652b-179">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-179">Central Site</span></span></p>
<p><span data-ttu-id="6652b-180">Сайт ветви</span><span class="sxs-lookup"><span data-stu-id="6652b-180">Branch Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-181">Наблюдатель виртуальных транзакций Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6652b-181">Lync Server 2013 Synthetic Transaction Watcher</span></span></p></td>
<td><p><span data-ttu-id="6652b-182">Развертывание выделенного сервера Lync Server для использования в качестве средства наблюдения за искусственными транзакциями.</span><span class="sxs-lookup"><span data-stu-id="6652b-182">Deploy a dedicated Lync Server to be a synthetic transaction watcher.</span></span></p>
<p><span data-ttu-id="6652b-183">Синтетические транзакции — это Lync Server 2013 командлеты Windows PowerShell, которые автоматически инициируются пакетом управления в предопределенном интервале.</span><span class="sxs-lookup"><span data-stu-id="6652b-183">Synthetic transactions are Lync Server 2013 Windows PowerShell cmdlets that are automatically triggered by the management pack on a predefined interval.</span></span> <span data-ttu-id="6652b-184">Эти данные выполняются на узле наблюдения искусственных транзакций, который является назначенным администратором сервером, ответственным за обнаружение и выполнение STs для каждого пула.</span><span class="sxs-lookup"><span data-stu-id="6652b-184">These are executed on a synthetic transaction watcher node which is an administrator designated server responsible for discovery and execution of STs for each pool.</span></span></p>
<p><span data-ttu-id="6652b-185">Мы не рекомендуем использовать существующий сервер Microsoft Lync Server 2013 в качестве искусственного узла наблюдения за транзакциями.</span><span class="sxs-lookup"><span data-stu-id="6652b-185">We do not recommend that you use an existing Microsoft Lync Server 2013 server as a synthetic transaction watcher node.</span></span> <span data-ttu-id="6652b-186">Это происходит из-за высокой требований к использованию памяти и ЦП для работы STs.</span><span class="sxs-lookup"><span data-stu-id="6652b-186">This is due to the high CPU/memory usage requirements for running STs.</span></span> <span data-ttu-id="6652b-187">Используйте новый серверный компьютер (или виртуальный сервер) для узла контрольных виртуальных транзакций.</span><span class="sxs-lookup"><span data-stu-id="6652b-187">Use a new server computer (or a virtual server) for the synthetic transaction watcher node.</span></span></p></td>
<td><p><span data-ttu-id="6652b-188">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-188">Central Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="6652b-189">Развертывание узла наблюдателя виртуальных транзакций.</span><span class="sxs-lookup"><span data-stu-id="6652b-189">Deploying synthetic transactions watcher node.</span></span></p>
<p><span data-ttu-id="6652b-190">Обратитесь к документу MonitoringCS_withSCOM.docx из документации UCTAP Connect.</span><span class="sxs-lookup"><span data-stu-id="6652b-190">Refer to the MonitoringCS_withSCOM.docx document from UCTAP connect documentation.</span></span></p></td>
<td><p><span data-ttu-id="6652b-191">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="6652b-191">Central Site</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="maximum-network-mos-scores-per-codec"></a><span data-ttu-id="6652b-192">Максимальная оценка сетевого MOS на кодек</span><span class="sxs-lookup"><span data-stu-id="6652b-192">Maximum Network MOS scores per codec</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6652b-193">Сценарий</span><span class="sxs-lookup"><span data-stu-id="6652b-193">Scenario</span></span></th>
<th><span data-ttu-id="6652b-194">Кодек</span><span class="sxs-lookup"><span data-stu-id="6652b-194">Codec</span></span></th>
<th><span data-ttu-id="6652b-195">Максимальная NMOS</span><span class="sxs-lookup"><span data-stu-id="6652b-195">Max NMOS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6652b-196">Звонок UC</span><span class="sxs-lookup"><span data-stu-id="6652b-196">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="6652b-197">RTAudio WB</span><span class="sxs-lookup"><span data-stu-id="6652b-197">RTAudio WB</span></span></p></td>
<td><p><span data-ttu-id="6652b-198">4,10</span><span class="sxs-lookup"><span data-stu-id="6652b-198">4.10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-199">Звонок UC</span><span class="sxs-lookup"><span data-stu-id="6652b-199">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="6652b-200">RTAudio имена NetBIOS</span><span class="sxs-lookup"><span data-stu-id="6652b-200">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="6652b-201">2,95</span><span class="sxs-lookup"><span data-stu-id="6652b-201">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-202">Конференц-связь</span><span class="sxs-lookup"><span data-stu-id="6652b-202">Conference call</span></span></p></td>
<td><p><span data-ttu-id="6652b-203">Siren</span><span class="sxs-lookup"><span data-stu-id="6652b-203">Siren</span></span></p></td>
<td><p><span data-ttu-id="6652b-204">3,72</span><span class="sxs-lookup"><span data-stu-id="6652b-204">3.72</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6652b-205">Звонок UC-КТСОП</span><span class="sxs-lookup"><span data-stu-id="6652b-205">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="6652b-206">RTAudio имена NetBIOS</span><span class="sxs-lookup"><span data-stu-id="6652b-206">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="6652b-207">2,95</span><span class="sxs-lookup"><span data-stu-id="6652b-207">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6652b-208">Звонок UC-КТСОП</span><span class="sxs-lookup"><span data-stu-id="6652b-208">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="6652b-209">G-711</span><span class="sxs-lookup"><span data-stu-id="6652b-209">G-711</span></span></p></td>
<td><p><span data-ttu-id="6652b-210">3,61</span><span class="sxs-lookup"><span data-stu-id="6652b-210">3.61</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6652b-211">Более ранние и более поздние версии. задачи обслуживания должны выполняться для центральных, краевых и посторонних сайтов на повторяющиеся ежедневные, еженедельные и ежемесячные данные, определенные в руководстве по работе с Lync RA.</span><span class="sxs-lookup"><span data-stu-id="6652b-211">Over and above the previous pro-active monitoring activities, maintenance tasks should be executed for Central, Edge and Branch sites on a recurring daily, weekly and monthly basis as defined in the Lync RA Operations Guide.</span></span>

<span data-ttu-id="6652b-212"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6652b-212"></div>

<span> </span>

</div>

</div>

</span></span></div>

