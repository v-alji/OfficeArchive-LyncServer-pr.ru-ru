---
title: 'Lync Server 2013: проверьте физическую среду'
description: 'Lync Server 2013: проверьте физическую среду.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Performing physical environmental checks
ms:assetid: 153aee5e-3adf-4dbf-bf41-53e4fba51fb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720558(v=OCS.15)
ms:contentKeyID: 63969582
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d963485b109e0afdf21b3a9085fa28884dfc3100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435000"
---
# <a name="performing-physical-environmental-checks"></a><span data-ttu-id="f8dc7-103">Выполнение физических проверок окружающей среды</span><span class="sxs-lookup"><span data-stu-id="f8dc7-103">Performing physical environmental checks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8dc7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8dc7-104">

<span> </span></span></span>

<span data-ttu-id="f8dc7-105">_**Тема последнего изменения:** 2014-04-30_</span><span class="sxs-lookup"><span data-stu-id="f8dc7-105">_**Topic Last Modified:** 2014-04-30_</span></span>

<span data-ttu-id="f8dc7-106">Прежде чем проверять производительность, доступность и функциональные возможности развертывания Lync Server 2013, необходимо проверить физическую среду.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-106">Before checking the performance, availability, and functionality of the Lync Server 2013 deployment, you should check the physical environment.</span></span> <span data-ttu-id="f8dc7-107">Например, может потребоваться уменьшить температуру в комнате сервера или заменить сетевой кабель.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-107">For example, the server room temperature might have to be lowered, or a network cable might have to be replaced.</span></span> <span data-ttu-id="f8dc7-108">Для достижения наилучших результатов выполните следующие физические проверки среды.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-108">For best results, perform the following physical environmental inspections:</span></span>

  - <span data-ttu-id="f8dc7-109">**Физические меры безопасности**   Физическая защита безопасности, например блокировки, дверцы и ограниченные комнаты доступа, должна быть защищена.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-109">**Physical security measures**   Physical security protection such as locks, doors, and restricted-access rooms must be secured.</span></span> <span data-ttu-id="f8dc7-110">Проверьте наличие неавторизованных и принудительных операций и признаки повреждений оборудования.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-110">Check for any unauthorized and forced entries and signs of equipment damage.</span></span>

  - <span data-ttu-id="f8dc7-111">**Температура и влажность**   Высокая температура, плохой поток воздуха и влажность могут привести к тому, что аппаратные компоненты overheat.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-111">**Temperature and humidity**   High temperature, poor air flow, and humidity can cause hardware components to overheat.</span></span> <span data-ttu-id="f8dc7-112">Проверьте температуру и влажности, чтобы убедиться в том, что системы окружающей среды, такие как нагревательные и воздушные условия, могут поддерживать приемлемые условия и работать в соответствии с требованиями производителя оборудования.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-112">Check temperature and humidity to help to make sure that the environmental systems such as heating and air conditioning can maintain acceptable conditions and function within the hardware manufacturer's specifications.</span></span> <span data-ttu-id="f8dc7-113">После установки нового оборудования также убедитесь, что воздушный поток как к серверу, так и от него не соответствует спецификации изготовителя.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-113">When new equipment has recently been installed, also check that air flow both to and from the servers is unimpeded and meets manufacturer spec.</span></span>

  - <span data-ttu-id="f8dc7-114">**Устройства и компоненты**   В Организации Lync Server 2013 используется работающая физическая сеть и связанное с ним оборудование.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-114">**Devices and components**   The Lync Server 2013 organization relies on a functioning physical network and related hardware.</span></span> <span data-ttu-id="f8dc7-115">Убедитесь, что на маршрутизаторах, коммутаторах, концентраторах, физических кабелях и соединительных линиях работают.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-115">Make sure that routers, switches, hubs, physical cables, and connectors are operational.</span></span>

<span data-ttu-id="f8dc7-116">Сведения о том, как выполнять эти проверки, будут сильно зависеть от вашего сайта установки и выбранного оборудования сервера.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-116">The specifics on how to perform these checks will depend greatly on your installation site and the server hardware that was chosen.</span></span> <span data-ttu-id="f8dc7-117">При первом выполнении этой проверки ознакомьтесь с документацией оборудования и запишите необходимые параметры для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="f8dc7-117">The first time that you perform this check, refer to the hardware documentation and note the desired parameters for future reference.</span></span>

### <a name="desired-server-space-environment"></a><span data-ttu-id="f8dc7-118">Нужная среда сервера</span><span class="sxs-lookup"><span data-stu-id="f8dc7-118">Desired server space environment</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8dc7-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="f8dc7-119">Parameter</span></span></th>
<th><span data-ttu-id="f8dc7-120">Нужное значение или диапазон</span><span class="sxs-lookup"><span data-stu-id="f8dc7-120">Desired value or range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8dc7-121">Допустим</span><span class="sxs-lookup"><span data-stu-id="f8dc7-121">Temperature</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8dc7-122">Зарегистрирован</span><span class="sxs-lookup"><span data-stu-id="f8dc7-122">Humidity</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8dc7-123">Лицевой стороной сервера</span><span class="sxs-lookup"><span data-stu-id="f8dc7-123">Front of server faces</span></span></p></td>
<td><p><span data-ttu-id="f8dc7-124">Горячий проход/холодный проход</span><span class="sxs-lookup"><span data-stu-id="f8dc7-124">Hot aisle / cold aisle</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8dc7-125">Нехватка зазоров</span><span class="sxs-lookup"><span data-stu-id="f8dc7-125">Unimpeded exhaust clearance</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="f8dc7-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8dc7-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

