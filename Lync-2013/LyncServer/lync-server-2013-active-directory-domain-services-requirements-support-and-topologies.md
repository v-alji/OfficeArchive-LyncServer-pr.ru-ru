---
title: Требования к доменным службам Active Directory, поддержка и топология
description: Требования, поддержка и топологии доменных служб Active Directory.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory Domain Services requirements, support, and topologies
ms:assetid: 95bd160f-bcea-4014-a050-8a3cd2f699c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398760(v=OCS.15)
ms:contentKeyID: 48184902
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e6f729a635ac05f56bd12f72d052b39975cd5165
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439424"
---
# <a name="active-directory-domain-services-requirements-support-and-topologies-in-lync-server-2013"></a><span data-ttu-id="c000d-103">Требования к доменным службам Active Directory, поддержка и топология в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c000d-103">Active Directory Domain Services requirements, support, and topologies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c000d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c000d-104">

<span> </span></span></span>

<span data-ttu-id="c000d-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="c000d-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="c000d-106">До Lync Server 2010 в Lync Server для хранения всех глобальных параметров и групп, необходимых для развертывания Lync Server, и управления ими используются доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c000d-106">Prior to Lync Server 2010, Lync Server relied on Active Directory Domain Services to store all the global settings and groups necessary to deploy and manage Lync Server.</span></span> <span data-ttu-id="c000d-107">Теперь многие данные хранятся в главном хранилище управления, а не в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c000d-107">Now much of this information is stored in the Central Management store instead of AD DS.</span></span> <span data-ttu-id="c000d-108">Однако расширения схемы объектов пользователя, в том числе расширения Lync Server 2013, Lync Server 2010 и Office Communications Server 2007 R2, по-прежнему хранятся в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c000d-108">However, user object schema extensions, including Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2 schema extensions, are still stored in AD DS.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c000d-109">Содержание</span><span class="sxs-lookup"><span data-stu-id="c000d-109">In This Section</span></span>

  - [<span data-ttu-id="c000d-110">Поддержка доменных служб Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c000d-110">Active Directory Domain Services support in Lync Server 2013</span></span>](lync-server-2013-active-directory-domain-services-support.md)

  - [<span data-ttu-id="c000d-111">Поддерживаемые топологии Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c000d-111">Supported Active Directory topologies in Lync Server 2013</span></span>](lync-server-2013-supported-active-directory-topologies.md)

  - [<span data-ttu-id="c000d-112">Требования к инфраструктуре Active Directory для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c000d-112">Active Directory infrastructure requirements for Lync Server 2013</span></span>](lync-server-2013-active-directory-infrastructure-requirements.md)

<span data-ttu-id="c000d-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c000d-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

