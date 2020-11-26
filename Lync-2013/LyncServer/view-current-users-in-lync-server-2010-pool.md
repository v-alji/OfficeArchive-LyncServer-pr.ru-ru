---
title: Просмотр текущих пользователей в пуле Lync Server 2010
description: Просмотр текущих пользователей в пуле Lync Server 2010.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View current users in Lync Server 2010 pool
ms:assetid: c0986800-8ee4-4d50-9e9c-39f7c4e67bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721870(v=OCS.15)
ms:contentKeyID: 49733804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55d328bf03c34db632f239bd9d3221ef942cd463
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438752"
---
# <a name="view-current-users-in-lync-server-2010-pool"></a><span data-ttu-id="2d15e-103">Просмотр текущих пользователей в пуле Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="2d15e-103">View current users in Lync Server 2010 pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d15e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d15e-104">

<span> </span></span></span>

<span data-ttu-id="2d15e-105">_**Тема последнего изменения:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="2d15e-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="2d15e-106">Прежде чем изучать различные способы перемещения пользователей между пулами, необходимо сначала определить, какие пользователи находятся в устаревшем пуле Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="2d15e-106">Prior to learning the various ways you can move users between pools, we must first determine what users exist in the legacy Lync Server 2010 pool.</span></span> <span data-ttu-id="2d15e-107">На изображении ниже в столбце регистратор пула выводятся шесть пользователей, которые настроены для устаревшего пула Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="2d15e-107">In the image below, the Registrar pool column identifies six users who are configured for the legacy Lync Server 2010 pool.</span></span> <span data-ttu-id="2d15e-108">Это тестовые пользователи, которые мы перейдем к пулу Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2d15e-108">These are the test users we will move to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="2d15e-109">**Просмотр списка пользователей в пуле Lync Server 2010**</span><span class="sxs-lookup"><span data-stu-id="2d15e-109">**To see the list of users in the Lync Server 2010 pool**</span></span>

1.  <span data-ttu-id="2d15e-110">Войдите на сервер переднего плана Lync Server 2010 с помощью учетной записи, которая является членом группы RTCUniversalServerAdmins или участником административной роли CsAdministrator или CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="2d15e-110">Log on to the Lync Server 2010 Front End Server with an account that is a member of the RTCUniversalServerAdmins group or a member of the CsAdministrator or CsUserAdministrator administrative role.</span></span>

2.  <span data-ttu-id="2d15e-111">Откройте **Панель управления Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2d15e-111">Open **Lync Server Control Panel**.</span></span>

3.  <span data-ttu-id="2d15e-112">Нажмите **Пользователи**, затем "Поиск" и **Найти**.</span><span class="sxs-lookup"><span data-stu-id="2d15e-112">Click **Users**, click Search, and then click **Find**.</span></span>

<span data-ttu-id="2d15e-113">**Панель управления Lync Server 15**</span><span class="sxs-lookup"><span data-stu-id="2d15e-113">**The Lync Server 15 Control Panel**</span></span>

<span data-ttu-id="2d15e-114">![Панель управления Lync Server, диалоговое окно перемещения пользователя](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Панель управления Lync Server, диалоговое окно перемещения пользователя")</span><span class="sxs-lookup"><span data-stu-id="2d15e-114">![Lync Server Control Panel, Move User dialog](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server Control Panel, Move User dialog")</span></span>

<span data-ttu-id="2d15e-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d15e-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

