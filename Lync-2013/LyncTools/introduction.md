---
title: Введение
description: Представления.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Introduction
ms:assetid: 276395be-93df-4a16-97e2-cb468cd0f2e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945588(v=OCS.15)
ms:contentKeyID: 51541414
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8eb847c499bde077ccaf2aa050de801ceeedcc6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438745"
---
# <a name="introduction"></a><span data-ttu-id="5e38f-103">Введение</span><span class="sxs-lookup"><span data-stu-id="5e38f-103">Introduction</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e38f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e38f-104">

<span> </span></span></span>

<span data-ttu-id="5e38f-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="5e38f-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="5e38f-106">С помощью средства нагрузки и производительности Lync Server 2013 (называемого также LyncPerfTool) можно смоделировать нагрузку на следующие типы:</span><span class="sxs-lookup"><span data-stu-id="5e38f-106">The Lync Server 2013 Stress and Performance Tool (referred to as LyncPerfTool) can simulate user load of the following types:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e38f-107">Обмен мгновенными сообщениями и присутствие</span><span class="sxs-lookup"><span data-stu-id="5e38f-107">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="5e38f-108">Аудиоконференции</span><span class="sxs-lookup"><span data-stu-id="5e38f-108">Audio conferencing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e38f-109">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="5e38f-109">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="5e38f-110">Голосовая связь по протоколу IP (VoIP), включая эмуляцию коммутируемой телефонной сети (PSTN)</span><span class="sxs-lookup"><span data-stu-id="5e38f-110">Voice over IP (VoIP), including public switched telephone network (PSTN) simulation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e38f-111">Конференции на клиентах веб-доступа к Интернету</span><span class="sxs-lookup"><span data-stu-id="5e38f-111">Web Access Client conferencing</span></span></p></td>
<td><p><span data-ttu-id="5e38f-112">Помощник Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="5e38f-112">Microsoft Lync 2013 Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e38f-113">Группы ответа</span><span class="sxs-lookup"><span data-stu-id="5e38f-113">Response Groups</span></span></p></td>
<td><p><span data-ttu-id="5e38f-114">Развертывание списка рассылки</span><span class="sxs-lookup"><span data-stu-id="5e38f-114">Distribution list expansion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e38f-115">Запрос на загрузку и адресную книгу в адресной книге</span><span class="sxs-lookup"><span data-stu-id="5e38f-115">Address book download and address book query</span></span></p></td>
<td><p><span data-ttu-id="5e38f-116">Улучшенный 9-1-1 (E9-1-1) звонки и профили местоположения (абонентская группа)</span><span class="sxs-lookup"><span data-stu-id="5e38f-116">Enhanced 9-1-1 (E9-1-1) calls and location profile (dial plan)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e38f-117">Многорежимный Просмотр</span><span class="sxs-lookup"><span data-stu-id="5e38f-117">MultiView</span></span></p></td>
<td><p><span data-ttu-id="5e38f-118">Просмотр нескольких потоков на Конференции</span><span class="sxs-lookup"><span data-stu-id="5e38f-118">Viewing multiple streams from a conference</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e38f-119">Инструмент Lync Server 2013 поддерживает создание и использование нагрузки между пулами и интеграцией только с помощью расширенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5e38f-119">The Lync Server 2013 Stress and Performance Tool supports cross-pool load generation and federation through advanced configuration only.</span></span>

<span data-ttu-id="5e38f-120">Кроме того, это средство не моделирует загрузку пользователей для следующих клиентов:</span><span class="sxs-lookup"><span data-stu-id="5e38f-120">The tool also does not simulate user load for the following clients:</span></span>

  - <span data-ttu-id="5e38f-121">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="5e38f-121">Office Live Meeting 2007</span></span>

  - <span data-ttu-id="5e38f-122">Lync 2013 сохраняемый чат</span><span class="sxs-lookup"><span data-stu-id="5e38f-122">Lync 2013 Persistent Chat</span></span>

<span data-ttu-id="5e38f-123">В результате средство Lync Server 2013 и производительность не будут поддерживать тестирование следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="5e38f-123">As a result, the Lync Server 2013 Stress and Performance Tool will not support testing the following components:</span></span>

  - <span data-ttu-id="5e38f-124">Lync 2013 сохраняемый чат</span><span class="sxs-lookup"><span data-stu-id="5e38f-124">Lync 2013 Persistent Chat</span></span>

  - <span data-ttu-id="5e38f-125">Сценарии интеграции с Exchange</span><span class="sxs-lookup"><span data-stu-id="5e38f-125">Exchange integration scenarios</span></span>

<div>

## <a name="applications-and-files-included-with-the-lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="5e38f-126">Приложения и файлы, входящие в состав средства быстрой и производительной нагрузки Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e38f-126">Applications and Files Included with the Lync Server 2013 Stress and Performance Tool</span></span>

<span data-ttu-id="5e38f-127">Ниже перечислены приложения, которые входят в состав средства быстрой и высокопроизводительной нагрузки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5e38f-127">The following applications are included in the Lync Server 2013 Stress and Performance Tool:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e38f-128">Средств</span><span class="sxs-lookup"><span data-stu-id="5e38f-128">Tool</span></span></th>
<th><span data-ttu-id="5e38f-129">Описание</span><span class="sxs-lookup"><span data-stu-id="5e38f-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e38f-130">UserProvisioningTool.exe</span><span class="sxs-lookup"><span data-stu-id="5e38f-130">UserProvisioningTool.exe</span></span></p></td>
<td><p><span data-ttu-id="5e38f-131">Средство подготовки пользователей Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5e38f-131">The Lync Server 2013 User Provisioning tool.</span></span> <span data-ttu-id="5e38f-132">Это средство используется для создания пользователей и контактов.</span><span class="sxs-lookup"><span data-stu-id="5e38f-132">This tool is used to create users and contacts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e38f-133">UserProfileGenerator.exe</span><span class="sxs-lookup"><span data-stu-id="5e38f-133">UserProfileGenerator.exe</span></span></p></td>
<td><p><span data-ttu-id="5e38f-134">Средство настройки загрузки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5e38f-134">The Lync Server 2013 Load Configuration Tool.</span></span> <span data-ttu-id="5e38f-135">Это средство используется для настройки характеристик пользовательской нагрузки для имитации.</span><span class="sxs-lookup"><span data-stu-id="5e38f-135">This tool is used to configure the characteristics of the user load to simulate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e38f-136">LyncPerfTool.exe</span><span class="sxs-lookup"><span data-stu-id="5e38f-136">LyncPerfTool.exe</span></span></p></td>
<td><p><span data-ttu-id="5e38f-137">Средство "стресс и производительность" Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5e38f-137">The Lync Server 2013 Stress and Performance Tool.</span></span> <span data-ttu-id="5e38f-138">LyncPerfTool — это инструмент, который имитирует пользовательскую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="5e38f-138">LyncPerfTool is the tool that simulates the user load.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e38f-139">Default. TMX</span><span class="sxs-lookup"><span data-stu-id="5e38f-139">Default.tmx</span></span></p></td>
<td><p><span data-ttu-id="5e38f-140">Значение Default. TMX является обязательным для использования средства ведения журнала в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5e38f-140">Default.tmx is required to use the Lync Server 2013 Logging Tool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e38f-141">Примеры сценариев подготовки</span><span class="sxs-lookup"><span data-stu-id="5e38f-141">Example provisioning scripts</span></span></p></td>
<td><p><span data-ttu-id="5e38f-142">Эти примеры используются для настройки топологии для выполняющихся нагрузочных тестов на основе определенных сценариев.</span><span class="sxs-lookup"><span data-stu-id="5e38f-142">These examples are used to configure the topology for running load tests, based on specific scenarios</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5e38f-143">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e38f-143">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

