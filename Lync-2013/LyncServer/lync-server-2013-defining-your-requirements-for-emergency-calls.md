---
title: 'Lync Server 2013: определение требований для экстренных вызовов'
description: 'Lync Server 2013: определение требований для вызова экстренной помощи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for emergency calls
ms:assetid: 5c12b517-9be6-41d0-83e2-11c78793620c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398404(v=OCS.15)
ms:contentKeyID: 48184276
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d3c9908dcb4008a1442af86971e42eb4096a98b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430835"
---
# <a name="defining-your-requirements-for-emergency-calls-in-lync-server-2013"></a><span data-ttu-id="a3a29-103">Определение требований для экстренных вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-103">Defining your requirements for emergency calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3a29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3a29-104">

<span> </span></span></span>

<span data-ttu-id="a3a29-105">_**Тема последнего изменения:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="a3a29-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="a3a29-106">Прежде чем приступить к установке Microsoft Lync Server 2013 E9-1-1, вы должны получить ответы на вопросы, описанные в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="a3a29-106">Before you begin a Microsoft Lync Server 2013 E9-1-1 deployment, you should first be able to answer the questions detailed in the following sections.</span></span> <span data-ttu-id="a3a29-107">Необходимое планирование зависит от типа решения E9-1-1, которое планируется разворачивать — канал SIP для подключения к поставщику услуг E9-1-1 или шлюз ELIN.</span><span class="sxs-lookup"><span data-stu-id="a3a29-107">The planning you need to do depends on the type of E9-1-1 solution that you choose to deploy—a SIP trunk E9-1-1 service provider or an Emergency Location Identification Number (ELIN) gateway.</span></span> <span data-ttu-id="a3a29-108">В следующей таблице приведены разделы данного руководства по планированию, которые необходимо изучить для каждого из этих решений.</span><span class="sxs-lookup"><span data-stu-id="a3a29-108">The following table identifies the sections in this planning workbook that you’ll need to review for each of those solutions.</span></span>

### <a name="planning-steps-by-type-of-e9-1-1-solution"></a><span data-ttu-id="a3a29-109">Этапы планирования типа решения E9-1-1</span><span class="sxs-lookup"><span data-stu-id="a3a29-109">Planning Steps by Type of E9-1-1 Solution</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3a29-110">Поставщик услуг по каналу SIP</span><span class="sxs-lookup"><span data-stu-id="a3a29-110">SIP trunk service provider</span></span></th>
<th><span data-ttu-id="a3a29-111">Шлюз ELIN</span><span class="sxs-lookup"><span data-stu-id="a3a29-111">ELIN gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3a29-112"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Определение области развертывания E9-1-1 в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-112"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Defining the scope of the E9-1-1 deployment in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-113"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Определение области развертывания E9-1-1 в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-113"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Defining the scope of the E9-1-1 deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a29-114"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Определение сетевых элементов, используемых для определения расположения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-114"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Defining the network elements used to determine location in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-115"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Определение сетевых элементов, используемых для определения расположения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-115"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Defining the network elements used to determine location in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a29-116"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Включение пользователей для E9-1-1 в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-116"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Enabling users for E9-1-1 in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-117"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Включение пользователей для E9-1-1 в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-117"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Enabling users for E9-1-1 in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a29-118"><a href="lync-server-2013-managing-locations-for-sip-trunk-service-providers.md">Управление расположением для поставщиков услуг магистральной магистрали SIP в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-118"><a href="lync-server-2013-managing-locations-for-sip-trunk-service-providers.md">Managing locations for SIP trunk service providers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-119"><a href="lync-server-2013-managing-locations-for-elin-gateways.md">Управление расположением для шлюзов ELIN в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-119"><a href="lync-server-2013-managing-locations-for-elin-gateways.md">Managing locations for ELIN gateways in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a29-120"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Определение взаимодействия с пользователем при получении расположения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-120"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Defining the user experience for manually acquiring a location in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-121"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Определение взаимодействия с пользователем при получении расположения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-121"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Defining the user experience for manually acquiring a location in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a29-122"><a href="lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md">Проектирование магистральной магистрали SIP для E9-1-1 в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-122"><a href="lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md">Designing the SIP trunk for E9-1-1 in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-123"><a href="lync-server-2013-including-the-security-desk.md">Включая службу безопасности в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-123"><a href="lync-server-2013-including-the-security-desk.md">Including the security desk in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a29-124"><a href="lync-server-2013-including-the-security-desk.md">Включая службу безопасности в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-124"><a href="lync-server-2013-including-the-security-desk.md">Including the security desk in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-125"><a href="lync-server-2013-defining-the-location-policy.md">Определение политики расположения для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-125"><a href="lync-server-2013-defining-the-location-policy.md">Defining the location policy for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a29-126"><a href="lync-server-2013-choosing-an-e9-1-1-service-provider.md">Выбор поставщика услуг E9-1-1 для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-126"><a href="lync-server-2013-choosing-an-e9-1-1-service-provider.md">Choosing an E9-1-1 service provider for Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a3a29-127"><a href="lync-server-2013-assigning-location-policy-scope.md">Назначение области политики расположения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-127"><a href="lync-server-2013-assigning-location-policy-scope.md">Assigning location policy scope in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a29-128"><a href="lync-server-2013-defining-the-location-policy.md">Определение политики расположения для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-128"><a href="lync-server-2013-defining-the-location-policy.md">Defining the location policy for Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a29-129"><a href="lync-server-2013-assigning-location-policy-scope.md">Назначение области политики расположения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a3a29-129"><a href="lync-server-2013-assigning-location-policy-scope.md">Assigning location policy scope in Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="a3a29-130">Содержание</span><span class="sxs-lookup"><span data-stu-id="a3a29-130">In This Section</span></span>

  - [<span data-ttu-id="a3a29-131">Определение области развертывания E9-1-1 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-131">Defining the scope of the E9-1-1 deployment in Lync Server 2013</span></span>](lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md)

  - [<span data-ttu-id="a3a29-132">Определение сетевых элементов, используемых для определения расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-132">Defining the network elements used to determine location in Lync Server 2013</span></span>](lync-server-2013-defining-the-network-elements-used-to-determine-location.md)

  - [<span data-ttu-id="a3a29-133">Включение пользователей для E9-1-1 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-133">Enabling users for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-enabling-users-for-e9-1-1.md)

  - [<span data-ttu-id="a3a29-134">Управление расположением для поставщиков услуг магистральной магистрали SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-134">Managing locations for SIP trunk service providers in Lync Server 2013</span></span>](lync-server-2013-managing-locations-for-sip-trunk-service-providers.md)

  - [<span data-ttu-id="a3a29-135">Управление расположением для шлюзов ELIN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-135">Managing locations for ELIN gateways in Lync Server 2013</span></span>](lync-server-2013-managing-locations-for-elin-gateways.md)

  - [<span data-ttu-id="a3a29-136">Определение взаимодействия с пользователем при получении расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-136">Defining the user experience for manually acquiring a location in Lync Server 2013</span></span>](lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md)

  - [<span data-ttu-id="a3a29-137">Проектирование магистральной магистрали SIP для E9-1-1 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-137">Designing the SIP trunk for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md)

  - [<span data-ttu-id="a3a29-138">Включая службу безопасности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-138">Including the security desk in Lync Server 2013</span></span>](lync-server-2013-including-the-security-desk.md)

  - [<span data-ttu-id="a3a29-139">Выбор поставщика услуг E9-1-1 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-139">Choosing an E9-1-1 service provider for Lync Server 2013</span></span>](lync-server-2013-choosing-an-e9-1-1-service-provider.md)

  - [<span data-ttu-id="a3a29-140">Определение политики расположения для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-140">Defining the location policy for Lync Server 2013</span></span>](lync-server-2013-defining-the-location-policy.md)

  - [<span data-ttu-id="a3a29-141">Назначение области политики расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3a29-141">Assigning location policy scope in Lync Server 2013</span></span>](lync-server-2013-assigning-location-policy-scope.md)

<span data-ttu-id="a3a29-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3a29-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

