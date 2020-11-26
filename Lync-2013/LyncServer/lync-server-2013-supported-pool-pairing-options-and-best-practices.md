---
title: Возможности и рекомендации по связыванию групп, поддерживаемых в Lync Server 2013
description: В Lync Server 2013 поддерживаются варианты связывания пулов и советы и рекомендации.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported pool pairing options and best practices
ms:assetid: 142caf34-0f20-47f3-9d32-ce25ab622fad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204697(v=OCS.15)
ms:contentKeyID: 48183478
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76d0f8331c0b6998008efff8af70ae3c4b43a9c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441419"
---
# <a name="supported-pool-pairing-options-and-best-practices-for-lync-server-2013"></a><span data-ttu-id="d95de-103">Поддерживаемые варианты связывания пулов и рекомендации для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d95de-103">Supported pool pairing options and best practices for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d95de-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d95de-104">

<span> </span></span></span>

<span data-ttu-id="d95de-105">_**Тема последнего изменения:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="d95de-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="d95de-106">На расстояние между двумя центрами обработки данных нет ограничений, которые должны включать в себя пулы интерфейсных служб, связанные друг с другом.</span><span class="sxs-lookup"><span data-stu-id="d95de-106">There is no restriction on the distance between two data centers that are to include Front End pools paired with each other.</span></span> <span data-ttu-id="d95de-107">Мы рекомендуем использовать два центра обработки данных в одном регионе мира, с высокоскоростными связями между ними.</span><span class="sxs-lookup"><span data-stu-id="d95de-107">We recommend that you use two data centers in the same world region, with high-speed links between them.</span></span> <span data-ttu-id="d95de-108">Лучше использовать два центра обработки данных, чтобы избежать одновременных попаданий на один и тот же случай.</span><span class="sxs-lookup"><span data-stu-id="d95de-108">It is best if the two data centers are separated enough to avoid a single disaster hitting both at the same time.</span></span>

<span data-ttu-id="d95de-109">Возможно, у вас есть два центра обработки данных в разных регионах мира, но это может привести к более высокой потере данных из-за задержки в репликации данных.</span><span class="sxs-lookup"><span data-stu-id="d95de-109">Having two data centers across world regions is possible, but could incur higher data loss due to latency in data replication.</span></span>

<span data-ttu-id="d95de-110">При планировании пулов, которые необходимо связать, следует помнить о том, что поддерживаются только следующие связывания.</span><span class="sxs-lookup"><span data-stu-id="d95de-110">When you plan which pools to pair, you must keep in mind that only the following pairings are supported:</span></span>

  - <span data-ttu-id="d95de-111">Пулы Enterprise Edition можно связывать только с другими пулами Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="d95de-111">Enterprise Edition pools can be paired only with other Enterprise Edition pools.</span></span> <span data-ttu-id="d95de-112">Аналогично, пулы Standard Edition можно связать только с другими пулами Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d95de-112">Similarly, Standard Edition pools can be paired only with other Standard Edition pools.</span></span>

  - <span data-ttu-id="d95de-113">Физические пулы можно связать только с другими физическими пулами.</span><span class="sxs-lookup"><span data-stu-id="d95de-113">Physical pools can be paired only with other physical pools.</span></span> <span data-ttu-id="d95de-114">Аналогично, виртуальные пулы можно связать только с другими виртуальными пулами.</span><span class="sxs-lookup"><span data-stu-id="d95de-114">Similarly, virtual pools can be paired only with other virtual pools.</span></span>

  - <span data-ttu-id="d95de-115">Пулы, Объединенные вместе, должны работать под управлением одной и той же операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d95de-115">Pools that are paired together must be running the same operating system.</span></span>

<span data-ttu-id="d95de-p104">Ни построитель топологии, ни средство проверки топологии не запрещает связывание двух пулов вопреки этим рекомендациям. Например, построитель топологий позволяет связать пул Enterprise Edition с пулом Standard Edition. Однако эти типы связываний не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d95de-p104">Neither Topology Builder nor topology validation will prohibit pairing two pools in a way that does not follow these recommendations. For example, Topology Builder allows you to pair an Enterprise Edition pool with a Standard Edition pool. However, these types of pairings are not supported.</span></span>

<span data-ttu-id="d95de-119">Каждый пул в паре должен иметь емкость для обслуживания всех пользователей из обоих пулов в случае аварии.</span><span class="sxs-lookup"><span data-stu-id="d95de-119">Each pool in a pair should have the capacity to serve all users from both pools in the event of a disaster.</span></span>

<span data-ttu-id="d95de-120">При связывании пулов Enterprise Edition вы также можете реализовать высокий уровень доступности на серверном сервере, но для пар стандартных пулов выпусков доступны только меры по восстановлению после аварии.</span><span class="sxs-lookup"><span data-stu-id="d95de-120">If you pair Enterprise Edition pools, you can also implement high availability on the Back End Servers, but for pairs of Standard Edition pools only the disaster recovery measures are available.</span></span>

<span data-ttu-id="d95de-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d95de-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

