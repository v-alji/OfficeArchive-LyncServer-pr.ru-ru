---
title: 'Lync Server 2013: контрольный список развертывания для контроля допуска звонков'
description: 'Lync Server 2013: контрольный список развертывания для управления допуском звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for call admission control
ms:assetid: 7e56a169-3e63-44ab-bf28-1fdeb52381c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398631(v=OCS.15)
ms:contentKeyID: 48184621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea5b16d41228faf01637e7e0d78f5ce56f950a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397942"
---
# <a name="deployment-checklist-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="fdd41-103">Контрольный список развертывания для контроля допуска звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fdd41-103">Deployment checklist for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fdd41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fdd41-104">

<span> </span></span></span>

<span data-ttu-id="fdd41-105">_**Тема последнего изменения:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="fdd41-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="fdd41-106">Чтобы эффективно спланировать управление допуском звонков (CAC), необходимо принять во все указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fdd41-106">To plan effectively for call admission control (CAC), you need to consider the following:</span></span>

  - <span data-ttu-id="fdd41-107">Необходимые условия для развертывания CAC.</span><span class="sxs-lookup"><span data-stu-id="fdd41-107">Prerequisites for deploying CAC.</span></span>

  - <span data-ttu-id="fdd41-108">Информация, необходимая для решений CAC и конфигурации, которые необходимо выполнить перед развертыванием.</span><span class="sxs-lookup"><span data-stu-id="fdd41-108">Information required for CAC and configuration decisions that you must make in advance of deployment.</span></span>

<div>

## <a name="deployment-prerequisites-for-call-admission-control"></a><span data-ttu-id="fdd41-109">Предварительные требования к развертыванию для управления допуском звонков</span><span class="sxs-lookup"><span data-stu-id="fdd41-109">Deployment Prerequisites for Call Admission Control</span></span>

<span data-ttu-id="fdd41-110">Прежде чем развертывать управление допуском звонков, необходимо предварительно развернуть внутренние серверы Lync Server 2013, в том числе либо интерфейсный пул, либо сервер Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="fdd41-110">Before you deploy call admission control, you must already have deployed your Lync Server 2013 internal servers, including either a Front End pool or a Standard Edition server.</span></span>

</div>

<div>

## <a name="information-requirements-for-call-admission-control"></a><span data-ttu-id="fdd41-111">Требования к сведениям для управления допуском звонков</span><span class="sxs-lookup"><span data-stu-id="fdd41-111">Information Requirements for Call Admission Control</span></span>

<span data-ttu-id="fdd41-112">В таблице ниже приведены сведения, необходимые для развертывания управления допуском звонков.</span><span class="sxs-lookup"><span data-stu-id="fdd41-112">The following table summarizes the required information for deploying call admission control.</span></span>

### <a name="information-requirements-for-call-admission-control-deployment"></a><span data-ttu-id="fdd41-113">Требования к сведениям для развертывания управления допуском звонков</span><span class="sxs-lookup"><span data-stu-id="fdd41-113">Information Requirements for Call Admission Control Deployment</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fdd41-114">Информация</span><span class="sxs-lookup"><span data-stu-id="fdd41-114">Information</span></span></th>
<th><span data-ttu-id="fdd41-115">Сводка данных, необходимых</span><span class="sxs-lookup"><span data-stu-id="fdd41-115">Summary of Information Required</span></span></th>
<th><span data-ttu-id="fdd41-116">Документация</span><span class="sxs-lookup"><span data-stu-id="fdd41-116">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdd41-117">Возможности Lync Server, необходимые для Организации</span><span class="sxs-lookup"><span data-stu-id="fdd41-117">Lync Server capabilities required by your organization</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fdd41-118">Возможности, которые должны поддерживаться вашей организацией</span><span class="sxs-lookup"><span data-stu-id="fdd41-118">Capabilities to be supported by your organization</span></span></p></li>
<li><p><span data-ttu-id="fdd41-119">Возможности, которые должны быть включены для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="fdd41-119">Capabilities to be enabled for individual users</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fdd41-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Определение своих требований для контроля допуска звонков в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fdd41-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdd41-121">Топологии и компоненты, которые нужно развернуть</span><span class="sxs-lookup"><span data-stu-id="fdd41-121">Topologies and components to be deployed</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fdd41-122">Компоненты, связанные с CAC, автоматически устанавливаются в составе Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fdd41-122">CAC related components are automatically installed as part of Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fdd41-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Определение своих требований для контроля допуска звонков в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fdd41-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdd41-124">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="fdd41-124">System requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fdd41-125">Требования к оборудованию</span><span class="sxs-lookup"><span data-stu-id="fdd41-125">Hardware requirements</span></span></p></li>
<li><p><span data-ttu-id="fdd41-126">Требования к программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="fdd41-126">Software requirements</span></span></p></li>
<li><p><span data-ttu-id="fdd41-127">Требования к выровнению</span><span class="sxs-lookup"><span data-stu-id="fdd41-127">Collocation requirements</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fdd41-128"><a href="lync-server-2013-determining-your-system-requirements.md">Определение требований к системе для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fdd41-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdd41-129">Требования к инфраструктуре</span><span class="sxs-lookup"><span data-stu-id="fdd41-129">Infrastructure requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fdd41-130">Для CAC не требуются особые требования к инфраструктуре</span><span class="sxs-lookup"><span data-stu-id="fdd41-130">No specific infrastructure requirements are necessary for CAC</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fdd41-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Требования к инфраструктуре для контроля допуска звонков в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fdd41-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Infrastructure requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdd41-132">Требования к сетевому интерфейсу</span><span class="sxs-lookup"><span data-stu-id="fdd41-132">Network interface requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fdd41-133">Сведения о внутреннем и внешнем интерфейсе</span><span class="sxs-lookup"><span data-stu-id="fdd41-133">Internal and external interface information</span></span></p></li>
<li><p><span data-ttu-id="fdd41-134">Сведения о маршрутизации (в том числе сведения в блоге на странице <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a> Microsoft Lync Server Teams в канале ответа клиента)</span><span class="sxs-lookup"><span data-stu-id="fdd41-134">Routing information (including information on the NextHop blog at <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a>, Microsoft Lync Server team’s customer response channel)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fdd41-135"><a href="lync-server-2013-deploying-external-user-access.md">Развертывание доступа внешних пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fdd41-135"><a href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdd41-136">Стратегия развертывания</span><span class="sxs-lookup"><span data-stu-id="fdd41-136">Deployment strategy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fdd41-137">Последовательность развертывания</span><span class="sxs-lookup"><span data-stu-id="fdd41-137">Deployment sequence</span></span></p></li>
<li><p><span data-ttu-id="fdd41-138">Рабочая группа или домен</span><span class="sxs-lookup"><span data-stu-id="fdd41-138">Workgroup or domain</span></span></p></li>
<li><p><span data-ttu-id="fdd41-139">Безопасность</span><span class="sxs-lookup"><span data-stu-id="fdd41-139">Security</span></span></p></li>
<li><p><span data-ttu-id="fdd41-140">Мониторинг и аудит</span><span class="sxs-lookup"><span data-stu-id="fdd41-140">Monitoring and auditing</span></span></p></li>
<li><p><span data-ttu-id="fdd41-141">Рекомендации по оборудованию</span><span class="sxs-lookup"><span data-stu-id="fdd41-141">Hardware considerations</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fdd41-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Рекомендации по контролю допуска звонков в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fdd41-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Best practices for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdd41-143">Процесс развертывания</span><span class="sxs-lookup"><span data-stu-id="fdd41-143">Deployment process</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fdd41-144">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="fdd41-144">Prerequisites</span></span></p></li>
<li><p><span data-ttu-id="fdd41-145">Требования к информации</span><span class="sxs-lookup"><span data-stu-id="fdd41-145">Information requirements</span></span></p></li>
<li><p><span data-ttu-id="fdd41-146">Процесс и процедуры</span><span class="sxs-lookup"><span data-stu-id="fdd41-146">Process and procedures</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fdd41-147"><a href="lync-server-2013-configure-call-admission-control.md">Настройка управления допуском звонков в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fdd41-147"><a href="lync-server-2013-configure-call-admission-control.md">Configure call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fdd41-148">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fdd41-148">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

