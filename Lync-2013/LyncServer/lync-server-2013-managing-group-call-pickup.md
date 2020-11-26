---
title: 'Lync Server 2013: Управление обсоединением групп'
description: 'Lync Server 2013: Управление обсоединением группового звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Group Call Pickup
ms:assetid: 85846a25-e175-4854-b31f-528f219f9a05
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945640(v=OCS.15)
ms:contentKeyID: 51541494
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a30ab3081d87d5a138000cb6581999923c816857
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437464"
---
# <a name="managing-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="6991e-103">Управление обсоединением групп в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6991e-103">Managing Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6991e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6991e-104">

<span> </span></span></span>

<span data-ttu-id="6991e-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="6991e-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="6991e-106">Накопительное обновление для Lync Server 2013: Февраль 2013 вводит функцию отправки группового звонка в качестве новой функции голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="6991e-106">Cumulative update for Lync Server 2013: February 2013 introduces Group Call Pickup as a new Enterprise Voice feature.</span></span> <span data-ttu-id="6991e-107">Отправка группового звонка пользователи предприятий голосовой связи смогут совершать звонки, которые поступают за другие пользователи, набрав номер группы для отправки звонков.</span><span class="sxs-lookup"><span data-stu-id="6991e-107">Group Call Pickup enables Enterprise Voice users to pick up calls that are ringing for another user by dialing a call pickup group number.</span></span>

<span data-ttu-id="6991e-108">В этой статье приведены пошаговые инструкции для задач, которые необходимо выполнить для настройки отправки групповых звонков в развертывании.</span><span class="sxs-lookup"><span data-stu-id="6991e-108">Topics in this section provide step-by-step procedures for tasks that you perform to configure Group Call Pickup in your deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6991e-109">Содержание</span><span class="sxs-lookup"><span data-stu-id="6991e-109">In This Section</span></span>

  - [<span data-ttu-id="6991e-110">Настройка диапазонов номеров для группового приема звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6991e-110">Configure Group Call Pickup number ranges in Lync Server 2013</span></span>](lync-server-2013-configure-group-call-pickup-number-ranges.md)

  - [<span data-ttu-id="6991e-111">Назначение номеров группового звонка пользователям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6991e-111">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)

  - [<span data-ttu-id="6991e-112">Включение и отключение отправки группового звонка для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6991e-112">Enable or disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-group-call-pickup-for-users.md)

  - [<span data-ttu-id="6991e-113">Управление расведением группового звонка во время восстановления после аварии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6991e-113">Manage Group Call Pickup during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-group-call-pickup-during-disaster-recovery.md)

<span data-ttu-id="6991e-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6991e-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

