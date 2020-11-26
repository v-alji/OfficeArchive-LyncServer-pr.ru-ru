---
title: Контрольный список развертывания Lync Server 2013 для конференц-связи с телефонным видео
description: Контрольный список развертывания Lync Server 2013 для конференций/V.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for A/V conferencing
ms:assetid: 6d47426f-6559-407b-9ac1-2453f0b7a2a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619183(v=OCS.15)
ms:contentKeyID: 49733684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9a4584172ed4c01eb163ea51aa4f62c2ce75185
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429757"
---
# <a name="deployment-checklist-for-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="c45de-103">Контрольный список развертывания для конференций/V в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c45de-103">Deployment checklist for A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c45de-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c45de-104">

<span> </span></span></span>

<span data-ttu-id="c45de-105">_**Тема последнего изменения:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="c45de-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="c45de-106">Как и при развертывании других компонентов Lync Server 2013, при развертывании конференции с помощью Topology Builder требуется создать и опубликовать топологию, в которой используются Конференции.</span><span class="sxs-lookup"><span data-stu-id="c45de-106">As with deployment of your other Lync Server 2013 components, deployment of A/V conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="c45de-107">Последовательность развертывания</span><span class="sxs-lookup"><span data-stu-id="c45de-107">Deployment Sequence</span></span>

<span data-ttu-id="c45de-108">Вы можете разворачивать конференции одновременно с развертыванием начальной топологии или после развертывания по крайней мере одного пула переднего плана или сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="c45de-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="c45de-109">Процесс развертывания конференций</span><span class="sxs-lookup"><span data-stu-id="c45de-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="c45de-110">В таблице ниже представлен обзор шагов, необходимых для развертывания конференций в существующей топологии.</span><span class="sxs-lookup"><span data-stu-id="c45de-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c45de-111">Этап</span><span class="sxs-lookup"><span data-stu-id="c45de-111">Phase</span></span></th>
<th><span data-ttu-id="c45de-112">Шаги</span><span class="sxs-lookup"><span data-stu-id="c45de-112">Steps</span></span></th>
<th><span data-ttu-id="c45de-113">Роли и членство в группах</span><span class="sxs-lookup"><span data-stu-id="c45de-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="c45de-114">Документация</span><span class="sxs-lookup"><span data-stu-id="c45de-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c45de-115"><strong>Установка необходимого оборудования и программного обеспечения</strong></span><span class="sxs-lookup"><span data-stu-id="c45de-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="c45de-116">Конференции выполняются на серверах переднего плана и серверах стандартных выпусков.</span><span class="sxs-lookup"><span data-stu-id="c45de-116">Conferencing runs on Front End Servers of a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="c45de-117">Для нее не существует дополнительных требований к оборудованию или программному обеспечению помимо требований для установки этих серверов.</span><span class="sxs-lookup"><span data-stu-id="c45de-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="c45de-118">Lync Server 2013 использует Office Web Apps и сервер Office Web Apps для обработки общего просмотра и отрисовки презентаций PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="c45de-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="c45de-119">Подробнее об установке и настройке сервера Office Web Apps можно узнать в разделе <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Настройка интеграции с Office Web Apps Server и Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c45de-119">For details about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="c45de-120">Пользователь домена, являющийся членом локальной группы "Администраторы"</span><span class="sxs-lookup"><span data-stu-id="c45de-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="c45de-121"><a href="lync-server-2013-supported-hardware.md">Поддерживаемое оборудование для Lync Server 2013</a> в документации по поддержке</span><span class="sxs-lookup"><span data-stu-id="c45de-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="c45de-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Поддержка серверного программного обеспечения и инфраструктуры в Lync Server 2013</a> в документации по поддержке</span><span class="sxs-lookup"><span data-stu-id="c45de-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="c45de-123"><a href="lync-server-2013-determining-your-system-requirements.md">Определение требований к системе для Lync Server 2013</a> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="c45de-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="c45de-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Технические требования для архивации в Lync Server 2013</a> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="c45de-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45de-125"><strong>Создание соответствующей внутренней топологии для поддержки конференц-связи</strong></span><span class="sxs-lookup"><span data-stu-id="c45de-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="c45de-126">Запустите построитель топологии, чтобы добавить в топологию Конференц-связь, а затем опубликуйте топологию.</span><span class="sxs-lookup"><span data-stu-id="c45de-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="c45de-127">Для определения топологии требуется учетная запись члена локальной группы "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="c45de-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="c45de-128">Чтобы опубликовать топологию, учетную запись, которая является членом группы "Администраторы домена" и RTCUniversalServerAdmins, и у нее есть разрешения полного доступа (чтение/запись и изменение) в общей папке, которая будет использоваться для хранения файлов Lync Server 2013 (чтобы Topology Builder мог настроить нужные DACL),</span><span class="sxs-lookup"><span data-stu-id="c45de-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="c45de-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Определите и настройте топологию в построителе топологии для Lync Server 2013</a> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="c45de-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45de-130"><strong>Настройка политик конференц-связи и поддержки</strong></span><span class="sxs-lookup"><span data-stu-id="c45de-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="c45de-131">Настройте параметры конференц-связи с помощью панели управления Lync Server 2013 или командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="c45de-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="c45de-132">Группа RTCUniversalServerAdmins (только для Windows PowerShell) или назначение пользователей для роли [] или CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="c45de-132">RTCUniversalServerAdmins group (Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="c45de-133"><a href="lync-server-2013-conferencing-policies.md">Политики конференций в Lync Server 2013</a> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="c45de-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c45de-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c45de-134">See Also</span></span>


[<span data-ttu-id="c45de-135">Обзор конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c45de-135">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)  
[<span data-ttu-id="c45de-136">Определение требований для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c45de-136">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)  
  

<span data-ttu-id="c45de-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c45de-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

