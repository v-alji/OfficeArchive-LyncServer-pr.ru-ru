---
title: 'Lync Server 2013: Управление доступом на основе ролей (RBAC)'
description: 'Lync Server 2013: Управление доступом на основе ролей (RBAC).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Role-based access control (RBAC) for Lync Server 2013
ms:assetid: d01fba36-eb7e-4de9-9bba-5102ae157820
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481134(v=OCS.15)
ms:contentKeyID: 59893872
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6586517083ff6cd2c4e20d83e9b8f861edf800c0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442349"
---
# <a name="role-based-access-control-rbac-for-lync-server-2013"></a><span data-ttu-id="06878-103">Управление доступом на основе ролей (RBAC) для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06878-103">Role-based access control (RBAC) for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06878-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06878-104">

<span> </span></span></span>

<span data-ttu-id="06878-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="06878-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="06878-106">Microsoft Lync Server 2013 включает в себя группы Role-Based управления доступом (RBAC), позволяющие делегировать задачи администрирования, обеспечивая высокий стандарт безопасности.</span><span class="sxs-lookup"><span data-stu-id="06878-106">Microsoft Lync Server 2013 includes Role-Based Access Control (RBAC) groups to enable you to delegate administrative tasks while maintaining high standards for security.</span></span> <span data-ttu-id="06878-107">Эти группы создаются в процессе подготовки леса.</span><span class="sxs-lookup"><span data-stu-id="06878-107">These groups are created during forest preparation.</span></span> <span data-ttu-id="06878-108">Подробнее о подготовке леса можно узнать в статьях [доменных служб Active Directory для Lync Server 2013](lync-server-2013-active-directory-domain-services-for-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="06878-108">For details about forest preparation, see [Active Directory Domain Services for Lync Server 2013](lync-server-2013-active-directory-domain-services-for-lync-server.md).</span></span> <span data-ttu-id="06878-109">Подробные сведения о конкретных группах, созданных с помощью подготовки леса, приведены в разделе [изменения, внесенные в процессе подготовки леса в Lync Server 2013](lync-server-2013-changes-made-by-forest-preparation.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="06878-109">For details about the specific groups created by forest preparation, see [Changes made by forest preparation in Lync Server 2013](lync-server-2013-changes-made-by-forest-preparation.md) in the Deployment documentation.</span></span>

<span data-ttu-id="06878-110">С помощью RBAC права администратора предоставлены путем назначения пользователей предварительно определенным административным ролям, включая 11 предопределенных ролей, которые охватывают многие общие задачи администрирования.</span><span class="sxs-lookup"><span data-stu-id="06878-110">With RBAC, administrative privilege is granted by assigning users to pre-defined administrative roles, including the 11 predefined roles that cover many common administrative tasks.</span></span> <span data-ttu-id="06878-111">Каждая роль связана с определенным списком командлетов командной консоли для Lync Server, для которых разрешено выполнение пользователей этой роли.</span><span class="sxs-lookup"><span data-stu-id="06878-111">Each role is associated with a specific list of Lync Server Management Shell cmdlets that users in that role are allowed to run.</span></span> <span data-ttu-id="06878-112">Можно использовать RBAC для выполнения принципа "наименьших привилегий", в котором пользователям предоставляются только возможности администрирования, необходимые для работы.</span><span class="sxs-lookup"><span data-stu-id="06878-112">You can use RBAC to follow the principle of "least privilege," in which users are given only the administrative abilities that their jobs require.</span></span> <span data-ttu-id="06878-113">Подробности можно найти [в разделе Планирование управления доступом на основе ролей в Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="06878-113">For details, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="06878-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06878-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

