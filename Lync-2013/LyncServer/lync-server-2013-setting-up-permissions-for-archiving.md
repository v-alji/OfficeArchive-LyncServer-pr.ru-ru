---
title: 'Lync Server 2013: Настройка разрешений для архивации'
description: 'Lync Server 2013: Настройка разрешений для архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up permissions for Archiving
ms:assetid: 67f97c94-52f5-4a83-a35c-8c307d5de9a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204961(v=OCS.15)
ms:contentKeyID: 48184364
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1f06c4fb48772a41621ece765dcc90555f0cd2d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399808"
---
# <a name="setting-up-permissions-for-archiving-in-lync-server-2013"></a><span data-ttu-id="537f7-103">Настройка разрешений для архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="537f7-103">Setting up permissions for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="537f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="537f7-104">

<span> </span></span></span>

<span data-ttu-id="537f7-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="537f7-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="537f7-106">В Lync Server 2013 для выполнения конкретных задач по-прежнему требуется, чтобы пользователи, которые выполняют эти задачи, были членами одной или нескольких конкретных групп.</span><span class="sxs-lookup"><span data-stu-id="537f7-106">In Lync Server 2013, specific tasks still require that users who perform those tasks be members of one or more specific groups.</span></span> <span data-ttu-id="537f7-107">Однако вы также можете использовать управление доступом на основе ролей (RBAC) для предоставления привилегий путем назначения пользователям стандартных административных ролей Lync Server. Перед развертыванием архивации убедитесь, что для этой роли назначены соответствующие права и разрешения пользователей, а также все пользователи, которым нужно назначить определенную роль RBAC.</span><span class="sxs-lookup"><span data-stu-id="537f7-107">However, you can also use role-based access control (RBAC) to grant privileges by assigning users to predefined Lync Server administrative roles.Before you deploy Archiving, be sure that the appropriate user rights and permissions are in place, and that any users who you want to assign to a specific RBAC role have been assigned to that role.</span></span> <span data-ttu-id="537f7-108">Подробные сведения о правах пользователей, разрешениях и ролях для развертывания поддержки архивации можно найти в разделе [Контрольный список развертывания для архивации в Lync Server 2013](lync-server-2013-deployment-checklist-for-archiving.md), который доступен в документации по планированию и документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="537f7-108">For details about the user rights, permissions, and roles for deploying support for Archiving, see [Deployment checklist for Archiving in Lync Server 2013](lync-server-2013-deployment-checklist-for-archiving.md), which is available in the Planning documentation and the Deployment documentation.</span></span> <span data-ttu-id="537f7-109">Подробнее об использовании RBAC можно узнать [в разделе Планирование управления доступом на основе ролей в Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="537f7-109">For details about RBAC, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="537f7-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="537f7-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

