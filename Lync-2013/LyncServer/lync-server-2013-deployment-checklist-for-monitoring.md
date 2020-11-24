---
title: 'Lync Server 2013: развертывание контрольного списка для мониторинга'
description: 'Lync Server 2013: контрольный список развертывания для мониторинга.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for monitoring
ms:assetid: 4e798370-277c-4391-84b4-13a972b45ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204874(v=OCS.15)
ms:contentKeyID: 48184080
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe3d3293accf6e25c20ae8391f9107ae75fef338
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399142"
---
# <a name="deployment-checklist-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="e9fd1-103">Развертывание контрольного списка для мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9fd1-103">Deployment checklist for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9fd1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9fd1-104">

<span> </span></span></span>

<span data-ttu-id="e9fd1-105">_**Тема последнего изменения:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="e9fd1-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="e9fd1-106">Несмотря на то, что мониторинг уже установлен и активирован на каждом сервере переднего плана, вы по-прежнему можете выполнить несколько действий, которые необходимо предпринять, прежде чем вы сможете собирать данные мониторинга для Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-106">Although monitoring is already installed and activated on each Front End server, there are still several steps that you must undertake before you can actually being to collect monitoring data for Microsoft Lync Server 2013.</span></span> <span data-ttu-id="e9fd1-107">Эти действия приведены в следующем контрольном списке.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-107">These steps are outlined in the following checklist:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9fd1-108">Этап</span><span class="sxs-lookup"><span data-stu-id="e9fd1-108">Phase</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-109">Шаги</span><span class="sxs-lookup"><span data-stu-id="e9fd1-109">Steps</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-110">Членство в роли и группе</span><span class="sxs-lookup"><span data-stu-id="e9fd1-110">Role and group membership</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-111">Документация</span><span class="sxs-lookup"><span data-stu-id="e9fd1-111">Documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9fd1-112"><strong>Установка необходимого оборудования и программного обеспечения</strong></span><span class="sxs-lookup"><span data-stu-id="e9fd1-112"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="e9fd1-113">Установка поддерживаемой версии Microsoft SQL Server на компьютере, который будет работать в качестве внутреннего хранилища данных для мониторинга.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-113">Install a supported version of Microsoft SQL Server on the computer that will act as the backend data store for monitoring.</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-114">Пользователь домена, который также является членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-114">Domain user who is also a member of the local administrators group.</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-115"><a href="lync-server-2013-supported-hardware.md">Поддерживаемое оборудование для Lync Server 2013</a> в руководстве по поддержке</span><span class="sxs-lookup"><span data-stu-id="e9fd1-115"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability guide</span></span></p>
<p><span data-ttu-id="e9fd1-116"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Поддержка серверного программного обеспечения и инфраструктуры в Lync Server 2013</a> в руководстве по поддержке</span><span class="sxs-lookup"><span data-stu-id="e9fd1-116"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability Guide</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9fd1-117"><strong>Создание подходящей внутренней топологии для поддержки мониторинга</strong></span><span class="sxs-lookup"><span data-stu-id="e9fd1-117"><strong>Create the appropriate internal topology to support monitoring</strong></span></span></p></td>
<td><p><span data-ttu-id="e9fd1-118">Используйте построитель топологии Lync Server 2013 для добавления в топологию баз данных мониторинга и публикации обновленной топологии.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-118">Use Lync Server 2013 Topology Builder to add monitoring databases to the topology, then published the updated topology.</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-119">Чтобы определить топологию, пользователь, который является членом локальной группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-119">To define a topology, a user who is a member of the local users group.</span></span></p>
<p><span data-ttu-id="e9fd1-120">Чтобы опубликовать топологию, пользователь, который является членом группы администраторов домена и группы RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-120">To publish the topology, a user who is a member if the domain administrators group and the RTCUniversalServerAdmins group.</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-121"><a href="lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md">Связывание хранилища мониторинга с пулом переднего плана в Lync Server 2013</a> в руководстве по развертыванию</span><span class="sxs-lookup"><span data-stu-id="e9fd1-121"><a href="lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md">Associating a monitoring store with a Front End pool in Lync Server 2013</a> in the Deployment guide</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9fd1-122"><strong>Включение подходящих параметров мониторинга</strong></span><span class="sxs-lookup"><span data-stu-id="e9fd1-122"><strong>Enable the appropriate monitoring settings</strong></span></span></p></td>
<td><p><span data-ttu-id="e9fd1-123">Включите мониторинг для записи сведений о вызовах (CDR) и/или качества (QoE) в глобальной и (или) масштабах сайта.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-123">Enable call detail recording (CDR) and/or Quality of Experience (QoE) monitoring at the global and/or the site scopes.</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-124">Пользователь, который является членом группы RTCUniversalServerAdmins или которому была назначена роль RBAC, предоставляющая доступ к командлетам CsCdrConfiguration и CsQoEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e9fd1-124">A user who is a member of the RTCUniversalServerAdmins group or who has been assigned an RBAC role that provides access to the CsCdrConfiguration and CsQoEConfiguration cmdlets.</span></span></p></td>
<td><p><span data-ttu-id="e9fd1-125"><a href="lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md">Настройка записи сведений о звонке и параметров качества обслуживания в Lync Server 2013</a> в руководстве по эксплуатации</span><span class="sxs-lookup"><span data-stu-id="e9fd1-125"><a href="lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</a> in the Operations guide</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e9fd1-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9fd1-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

