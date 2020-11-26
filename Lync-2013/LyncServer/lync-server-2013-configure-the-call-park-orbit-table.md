---
title: 'Lync Server 2013: настройка таблицы орбит парковки вызовов'
description: 'Lync Server 2013: Настройка таблицы "приостановить Звонок".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Call Park orbit table
ms:assetid: e5cc0c19-7b2c-48e7-a21d-cfb23c842f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399020(v=OCS.15)
ms:contentKeyID: 48185666
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce9fb35c2958a426888d83d075064c88ddae4bfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433635"
---
# <a name="configure-the-call-park-orbit-table-in-lync-server-2013"></a><span data-ttu-id="fbe4a-103">Настройка таблицы орбит парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbe4a-103">Configure the Call Park orbit table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fbe4a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fbe4a-104">

<span> </span></span></span>

<span data-ttu-id="fbe4a-105">_**Тема последнего изменения:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="fbe4a-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="fbe4a-106">Метод парковки использует орбиты для вызовов парковки.</span><span class="sxs-lookup"><span data-stu-id="fbe4a-106">Call Park uses orbits for parking calls.</span></span> <span data-ttu-id="fbe4a-107">Прежде чем пользователи смогут приступить к приостановке и получению звонков, необходимо настроить таблицу "Орбита".</span><span class="sxs-lookup"><span data-stu-id="fbe4a-107">Before users can park and retrieve calls, you must configure the Call Park orbit table.</span></span> <span data-ttu-id="fbe4a-108">Вы должны указать диапазоны добавочных номеров (орбиты), которые ваша организация резервирует для звонков на стоянку, и определить маршрут для этих диапазонов, указав, какой пул приостановки вызова обрабатывает каждый из диапазонов.</span><span class="sxs-lookup"><span data-stu-id="fbe4a-108">You need to specify the ranges of extension numbers (orbits) that your organization will reserve for parking calls and define the routing for those ranges by specifying which Call Park pool handles each range.</span></span> <span data-ttu-id="fbe4a-109">When you define orbit ranges, the goal is to have enough orbits so that any one orbit is not reused too quickly, but not so many orbits that you limit the number of extensions available for users or other services.</span><span class="sxs-lookup"><span data-stu-id="fbe4a-109">When you define orbit ranges, the goal is to have enough orbits so that any one orbit is not reused too quickly, but not so many orbits that you limit the number of extensions available for users or other services.</span></span> <span data-ttu-id="fbe4a-110">Вы можете создать несколько диапазонов орбиты на приостановку для каждого пула серверов Lync Server, в котором развернуто приложение для приостановки звонков.</span><span class="sxs-lookup"><span data-stu-id="fbe4a-110">You can create multiple Call Park orbit ranges for each Lync Server pool where the Call Park application is deployed.</span></span> <span data-ttu-id="fbe4a-111">Для каждого диапазона орбиты на линии с приостановкой на начало работы должны быть заданы глобально уникальное имя и уникальный набор расширений.</span><span class="sxs-lookup"><span data-stu-id="fbe4a-111">Each Call Park orbit range must have a globally unique name and a unique set of extensions.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="fbe4a-p102">Обычно диапазон орбит содержит 100 или менее орбит. Каждый из диапазонов может быть значительно больше, максимальные значения составляют не более 10000 орбит на диапазон и менее 50000 орбит на пул. Если диапазон слишком мал, орбиты используются повторно с большей частотой.</span><span class="sxs-lookup"><span data-stu-id="fbe4a-p102">An orbit range typically encompasses 100 or fewer orbits. Each range can be much larger, as long as it is smaller than the maximum of 10,000 orbits per range and you have fewer than 50,000 orbits per pool. If a range is too small, the orbits are reused more quickly.</span></span>



</div>

<span data-ttu-id="fbe4a-115">Для своих диапазонов орбит используйте блоки виртуальных добавочных номеров (которым не назначен телефон или пользователь).</span><span class="sxs-lookup"><span data-stu-id="fbe4a-115">Use blocks of virtual extensions (extensions that have no user or phone assigned to them) for your orbit ranges.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fbe4a-116">Не поддерживается назначение прямых и непосредственных номеров для нумерации на орбите в таблице "набрать на орбиту".</span><span class="sxs-lookup"><span data-stu-id="fbe4a-116">Assigning Direct Inward Dialing (DID) numbers as orbit numbers in the Call Park orbit table is not supported.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fbe4a-117">Содержание</span><span class="sxs-lookup"><span data-stu-id="fbe4a-117">In This Section</span></span>

[<span data-ttu-id="fbe4a-118">Создание или изменение диапазона орбиты на расстоянии вверх на сервере Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbe4a-118">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

<span data-ttu-id="fbe4a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fbe4a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

