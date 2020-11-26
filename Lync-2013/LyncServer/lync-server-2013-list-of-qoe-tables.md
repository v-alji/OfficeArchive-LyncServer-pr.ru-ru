---
title: 'Lync Server 2013: список таблиц качества взаимодействия'
description: 'Lync Server 2013: список таблиц QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of QoE tables
ms:assetid: 176194d7-d184-4e23-94bb-cb62b4db47f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398236(v=OCS.15)
ms:contentKeyID: 48183512
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 871babf246f616d306a03f84f9134605dd595999
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426573"
---
# <a name="list-of-qoe-tables-in-lync-server-2013"></a><span data-ttu-id="903f5-103">Список таблиц качества взаимодействия в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="903f5-103">List of QoE tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="903f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="903f5-104">

<span> </span></span></span>

<span data-ttu-id="903f5-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="903f5-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="903f5-106">Схема базы данных состоит из следующих таблиц.</span><span class="sxs-lookup"><span data-stu-id="903f5-106">The database schema consists of the following tables.</span></span>

<span data-ttu-id="903f5-107">**Вспомогательные таблицы**</span><span class="sxs-lookup"><span data-stu-id="903f5-107">**Supporting Tables**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="903f5-108"><strong>Таблица</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-108"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="903f5-109"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-109"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="903f5-110"><a href="lync-server-2013-appsharingmetricsthreshold-table.md">Таблица AppSharingMetricsThreshold в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-110"><a href="lync-server-2013-appsharingmetricsthreshold-table.md">AppSharingMetricsThreshold table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-111">Хранение оптимальных и приемлемых значений для показателей качества взаимодействия, используемых совместно с приложением.</span><span class="sxs-lookup"><span data-stu-id="903f5-111">Stores optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-112"><a href="lync-server-2013-codecdescription-table.md">Таблица CodecDescription в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-112"><a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-113">Сопоставляет уникальные идентификаторы кодека с соответствующими кодеками.</span><span class="sxs-lookup"><span data-stu-id="903f5-113">Maps unique codec identifiers to their corresponding codec.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-114"><a href="lync-server-2013-ipaddress-table.md">Таблица IP-адреса в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-114"><a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-115">Сопоставляет IP-адреса с уникальными идентификаторами IP-адресов, которые используются в базе данных качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="903f5-115">Maps IP addresses to the unique IP address identifiers used elsewhere in the Quality of Experience database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-116"><a href="lync-server-2013-networkconnectiondetail-table.md">Таблица NetworkConnectionDetail в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-116"><a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-117">Сопоставляет типы сетевых подключений с идентификаторами сетевых подключений, используемыми в базе данных качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="903f5-117">Maps network connection types to the network connection identifiers used elsewhere in the Quality of Experience database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-118"><a href="lync-server-2013-purgesettings-table-qoe.md">PurgeSettings Table (QoE) в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-118"><a href="lync-server-2013-purgesettings-table-qoe.md">PurgeSettings table (QoE) in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-119">Хранит сведения о том, что (и когда) устаревшие записи качества обслуживания будут автоматически удалены из базы данных QoE.</span><span class="sxs-lookup"><span data-stu-id="903f5-119">Stores information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-120"><a href="lync-server-2013-traceroute-table.md">Таблица использованием Traceroute в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-120"><a href="lync-server-2013-traceroute-table.md">TraceRoute table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-121">Хранит сведения о маршрутизации для звонков.</span><span class="sxs-lookup"><span data-stu-id="903f5-121">Stores routing information for calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-122"><a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef Table (QoE) в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-122"><a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-123">Сопоставляет идентификаторы агента пользователя с описательными именами агента.</span><span class="sxs-lookup"><span data-stu-id="903f5-123">Maps user agent identifiers to the agent’s descriptive names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-124"><a href="lync-server-2013-videometricsthreshold-table.md">Таблица VideoMetricsThreshold в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-124"><a href="lync-server-2013-videometricsthreshold-table.md">VideoMetricsThreshold table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-125">Хранение оптимальных и приемлемых значений для показателей качества взаимодействия, используемых с видеозвонками.</span><span class="sxs-lookup"><span data-stu-id="903f5-125">Stores optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-126"><a href="lync-server-2013-useragent-table.md">Таблица UserAgent в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-126"><a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-127">В сеансах голосовой и видеосвязи для протоколов SIP (UA) User Agent (агент запуска сеанса) хранятся строки и типы UA.</span><span class="sxs-lookup"><span data-stu-id="903f5-127">Stores Session Initiation Protocol (SIP) User Agent (UA) strings and UA types used in audio and video sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-128"><a href="lync-server-2013-user-table.md">Таблица User в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-128"><a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-129">Хранит URI пользователей, конференций и телефонных номеров, используемых в сеансах голосовой связи и видео.</span><span class="sxs-lookup"><span data-stu-id="903f5-129">Stores user, conference, and phone URIs used in audio and video sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-130"><a href="lync-server-2013-endpoint-table.md">Таблица Endpoint в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-130"><a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-131">Хранит полные доменные имена конечных точек, участвующих в звуковых и видеосеансах.</span><span class="sxs-lookup"><span data-stu-id="903f5-131">Stores FQDN computer names of endpoints participating in audio and video sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-132"><a href="lync-server-2013-pool-table.md">Таблица Pool в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-132"><a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-133">Хранит имена пулов, которым принадлежат данные метрик.</span><span class="sxs-lookup"><span data-stu-id="903f5-133">Stores the names of pools to which metrics data belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-134"><a href="lync-server-2013-device-table.md">Таблица Device в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-134"><a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-135">Хранит устройства захвата и устройства рендеринга, используемые в голосовых и видеозвонках.</span><span class="sxs-lookup"><span data-stu-id="903f5-135">Stores capture devices and render devices which are used in an audio/video calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-136"><a href="lync-server-2013-devicedriver-table.md">Таблица DeviceDriver в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-136"><a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-137">Хранит драйвер устройства захвата и устройство рендеринга, которое используется в голосовых и видеозвонках.</span><span class="sxs-lookup"><span data-stu-id="903f5-137">Stores driver for the capture device and the render device which are used in audio/video calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-138"><a href="lync-server-2013-conference-table.md">Таблица Conference в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-138"><a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-139">Хранит коды URI конференций для сценариев конференции или DialogID для других сценариев.</span><span class="sxs-lookup"><span data-stu-id="903f5-139">Stores Conference URIs for conference scenarios or DialogID for other scenarios.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-140"><a href="lync-server-2013-sessioncorrelation-table.md">Таблица SessionCorrelation в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-140"><a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-141">Содержит сведения о корреляции для КОММУТИРУЕМых звонков.</span><span class="sxs-lookup"><span data-stu-id="903f5-141">Stores CorrelationID for PSTN calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-142"><a href="lync-server-2013-payloaddescription-table.md">Таблица PayloadDescription в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-142"><a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-143">Хранит кодек, используемый в голосовых и видеозвонках.</span><span class="sxs-lookup"><span data-stu-id="903f5-143">Stores the Codec used in audio/video calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-144"><a href="lync-server-2013-appliedbandwidthsource-table.md">Таблица AppliedBandwidthSource в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-144"><a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-145">Сохранение источника пропускной способности, используемой в голосовых и видеозвонках.</span><span class="sxs-lookup"><span data-stu-id="903f5-145">Stores the bandwidth source used in audio/video calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-146"><a href="lync-server-2013-macaddress-table.md">Таблица MacAddress в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-146"><a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-147">Хранит MAC-адрес конечных точек, участвующих в сеансах аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="903f5-147">Stores the MAC address of the endpoints participating in audio and video sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-148"><a href="lync-server-2013-dialog-table.md">Таблица Dialog в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-148"><a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-149">Хранит идентификатор диалога для звуковых и видеосеансов.</span><span class="sxs-lookup"><span data-stu-id="903f5-149">Stores the Dialog ID of audio and video sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-150"><a href="lync-server-2013-region-table.md">Таблица Region в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-150"><a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-151">Хранит сетевой регион, определенный в параметрах NC.</span><span class="sxs-lookup"><span data-stu-id="903f5-151">Stores the network region defined in NCS setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-152"><a href="lync-server-2013-usersite-table.md">Таблица UserSite в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-152"><a href="lync-server-2013-usersite-table.md">UserSite table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-153">Сохранение сетевого сайта, определенного в параметрах NC.</span><span class="sxs-lookup"><span data-stu-id="903f5-153">Stores the network site defined in NCS setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-154"><a href="lync-server-2013-subnet-table.md">Таблица Subnet в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-154"><a href="lync-server-2013-subnet-table.md">Subnet table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-155">Хранит подсеть, определенную в параметрах NC.</span><span class="sxs-lookup"><span data-stu-id="903f5-155">Stores the subnet defined in NCS setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-156"><a href="lync-server-2013-monitoredregionlink-table.md">Таблица MonitoredRegionLink в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-156"><a href="lync-server-2013-monitoredregionlink-table.md">MonitoredRegionLink table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-157">Хранит ссылку на регион, определенную в параметрах NC.</span><span class="sxs-lookup"><span data-stu-id="903f5-157">Stores the region link defined in NCS setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-158"><a href="monitoredusersitelink-table.md">Таблица MonitoredUserSiteLink</a></span><span class="sxs-lookup"><span data-stu-id="903f5-158"><a href="monitoredusersitelink-table.md">MonitoredUserSiteLink table</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-159">Хранит ссылки на сайты сети, определенные в параметрах NC.</span><span class="sxs-lookup"><span data-stu-id="903f5-159">Stores the network site links defined in NCS setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-160"><a href="lync-server-2013-endpointsubnet-table.md">Таблица EndpointSubnet в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-160"><a href="lync-server-2013-endpointsubnet-table.md">EndpointSubnet table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-161">Хранит подсеть конечной точки, участвующей в звуковых и видеосеансах.</span><span class="sxs-lookup"><span data-stu-id="903f5-161">Stores the subnet of the endpoint participating in an audio and video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-162"><a href="lync-server-2013-server-table.md">Таблица Server в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-162"><a href="lync-server-2013-server-table.md">Server table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-163">Хранит полное доменное имя или IP-адрес сервера, через который восходит носитель.</span><span class="sxs-lookup"><span data-stu-id="903f5-163">Stores the FQDN or IP address of the server the media goes through.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="903f5-164">**Таблицы для данных метрик**</span><span class="sxs-lookup"><span data-stu-id="903f5-164">**Tables for metrics data**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="903f5-165"><strong>Таблица</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-165"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="903f5-166"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-166"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="903f5-167"><a href="lync-server-2013-appsharingstream-table.md">Таблица AppSharingStream в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-167"><a href="lync-server-2013-appsharingstream-table.md">AppSharingStream table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-168">Хранение метрик качества для сетевых потоков, используемых для совместного использования приложений.</span><span class="sxs-lookup"><span data-stu-id="903f5-168">Stores Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="903f5-169">Показатели качества взаимодействия для сетевых потоков, используемых для совместного использования приложений.</span><span class="sxs-lookup"><span data-stu-id="903f5-169">Quality of Experience metrics for the network streams used for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-170"><a href="lync-server-2013-session-table.md">Таблица Session в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-170"><a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-171">Хранит общие сведения о звуковых и видеофайлах, а также о звуковых и видеосеансах.</span><span class="sxs-lookup"><span data-stu-id="903f5-171">Stores overall information about an audio or audio/video session.</span></span> <span data-ttu-id="903f5-172">Сеанс определяется как звуковое или видеодиалоговое окно SIP между двумя конечными точками.</span><span class="sxs-lookup"><span data-stu-id="903f5-172">A session is defined as an audio or video SIP dialog between two endpoints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-173"><a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-173"><a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-174">Хранит сведения о каждой строке мультимедиа в сеансе.</span><span class="sxs-lookup"><span data-stu-id="903f5-174">Stores information about each media line in a session.</span></span> <span data-ttu-id="903f5-175">Линия мультимедиа — это коллекция из одного или нескольких звуковых и видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="903f5-175">A media line is a collection of one or more audio and video streams.</span></span> <span data-ttu-id="903f5-176">Обычно в одной линии есть два потока: аудио-или видеофайлы.</span><span class="sxs-lookup"><span data-stu-id="903f5-176">Typically, a single media line will have two streams, either audio or video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-177"><a href="lync-server-2013-audiostream-table.md">Таблица AudioStream в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-177"><a href="lync-server-2013-audiostream-table.md">AudioStream table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-178">Хранит метрики качества звукового файла в линии мультимедиа для каждого звукового потока.</span><span class="sxs-lookup"><span data-stu-id="903f5-178">Stores audio media quality metrics for each audio stream in the media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-179"><a href="lync-server-2013-audiosignal-table.md">Таблица AudioSignal в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-179"><a href="lync-server-2013-audiosignal-table.md">AudioSignal table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-180">Сохраняет метрики качества звукового файла в линии мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="903f5-180">Stores audio media quality metrics in the media line.</span></span> <span data-ttu-id="903f5-181">Это включает в себя метрики для подавления эха (AEC) и автоматических показателей контроля усиления (AGC).</span><span class="sxs-lookup"><span data-stu-id="903f5-181">This includes acoustic echo cancellation (AEC) and automatic gain control (AGC) metrics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-182"><a href="lync-server-2013-videostream-table.md">Таблица VideoStream в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-182"><a href="lync-server-2013-videostream-table.md">VideoStream table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-183">Хранит метрики качества видео для каждого звукового потока в строке мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="903f5-183">Stores video media quality metrics for each audio stream in the media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-184"><a href="lync-server-2013-audioclientevent-table.md">Таблица AudioClientEvent в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-184"><a href="lync-server-2013-audioclientevent-table.md">AudioClientEvent table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-185">Сохраняет показатели качества звуковых файлов мультимедиа, полученные из клиентского события.</span><span class="sxs-lookup"><span data-stu-id="903f5-185">Stores audio media quality metrics collected from the client event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-186"><a href="lync-server-2013-videoclientevent-table.md">Таблица VideoClientEvent в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="903f5-186"><a href="lync-server-2013-videoclientevent-table.md">VideoClientEvent table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="903f5-187">Хранит метрики качества видео, собранные из клиентского события.</span><span class="sxs-lookup"><span data-stu-id="903f5-187">Stores video media quality metrics collected from the client event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-188"><strong>Таблица DiagnosticData</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-188"><strong>DiagnosticData Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-189">Хранит диагностические данные, предназначенные только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-189">Stores diagnostic data which is for internal use only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="903f5-190">**Таблицы для сводных данных**</span><span class="sxs-lookup"><span data-stu-id="903f5-190">**Tables for summary data**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="903f5-191"><strong>Таблица</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-191"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="903f5-192"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-192"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="903f5-193"><strong>Таблица ServerSummary</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-193"><strong>ServerSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-194">Хранит сводные данные для серверов, эти данные используются только для отчетов о качестве опыта (QoE).</span><span class="sxs-lookup"><span data-stu-id="903f5-194">Stores summary data for the servers, these data is used for Quality of Experience (QoE) reporting only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-195"><strong>Таблица UserSummary</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-195"><strong>UserSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-196">Хранит сводные данные для пользователей, эти данные используются только для отчетов QoE.</span><span class="sxs-lookup"><span data-stu-id="903f5-196">Stores summary data for users, these data is used for QoE reporting only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-197"><strong>Таблица CallTypeSummary</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-197"><strong>CallTypeSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-198">Хранить сводные данные для типов звонков эти данные используются только для отчетов QoE.</span><span class="sxs-lookup"><span data-stu-id="903f5-198">Store summary data for call types, these data is used for QoE reporting only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="903f5-199">**Таблицы для внутреннего использования сервером мониторинга**</span><span class="sxs-lookup"><span data-stu-id="903f5-199">**Tables for Internal Use by Monitoring Server**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="903f5-200"><strong>Таблица</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-200"><strong>Table</strong></span></span></th>
<th><span data-ttu-id="903f5-201"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-201"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="903f5-202"><strong>DbConfigDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-202"><strong>DbConfigDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-203">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-203">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-204"><strong>DbConfigInt</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-204"><strong>DbConfigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-205">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-205">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-206"><strong>Интерфейсная таблица</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-206"><strong>FrontEnd Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-207">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-207">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-208"><strong>Таблица задач</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-208"><strong>Task Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-209">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-209">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-210"><strong>SummaryTableConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-210"><strong>SummaryTableConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-211">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-211">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-212"><strong>DbErrorMessage</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-212"><strong>DbErrorMessage</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-213">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-213">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-214"><strong>MetricsThreshold</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-214"><strong>MetricsThreshold</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-215">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-215">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-216"><strong>DaylightSavingYears</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-216"><strong>DaylightSavingYears</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-217">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-217">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-218"><strong>TimeZoneConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-218"><strong>TimeZoneConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-219">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-219">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-220"><strong>Часовых поясов</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-220"><strong>TimeZones</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-221">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-221">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-222"><strong>Таблица CallSummary</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-222"><strong>CallSummary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-223">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-223">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-224"><strong>Таблица DeviceCallSumary</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-224"><strong>DeviceCallSumary Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-225">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-225">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-226"><strong>Таблица "клиент"</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-226"><strong>Tenant Table</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-227">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-227">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="903f5-228"><strong>VideoCallSummaryTable</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-228"><strong>VideoCallSummaryTable</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-229">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-229">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="903f5-230"><strong>ASCallSummaryTable</strong></span><span class="sxs-lookup"><span data-stu-id="903f5-230"><strong>ASCallSummaryTable</strong></span></span></p></td>
<td><p><span data-ttu-id="903f5-231">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="903f5-231">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="903f5-232">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="903f5-232">


</div>

<span> </span>

</div>

</div>

</span></span></div>

