---
title: Стандартный сценарий миграции — высокоуровневый
description: Стандартный сценарий миграции — высокий уровень.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Standard migration scenario - high-level
ms:assetid: e768a7ca-44e3-4969-a6d9-7ed3e7029c5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205354(v=OCS.15)
ms:contentKeyID: 48185709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a931b76e528b7e6468f6b7e7b9a718724d27501f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438759"
---
# <a name="standard-migration-scenario---high-level"></a><span data-ttu-id="28203-103">Стандартный сценарий миграции — высокоуровневый</span><span class="sxs-lookup"><span data-stu-id="28203-103">Standard migration scenario - high-level</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28203-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28203-104">

<span> </span></span></span>

<span data-ttu-id="28203-105">_**Тема последнего изменения:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="28203-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="28203-106">Используйте следующие элементы в качестве отправной точки при переносе Lync Server 2010, групповой чат или Office Communications Server 2007 R2 Group Chat на Lync Server 2013 и на сервер сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="28203-106">Use the following items as a starting point when migrating Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="28203-107">Стандартный путь миграции Lync Server 2013 выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28203-107">The standard Lync Server 2013 migration path is as follows:</span></span>

  - <span data-ttu-id="28203-108">Ваша организация ранее развернула Lync Server 2010, групповой чат или Office Communications Server 2007 R2 Group чата, и вы хотите развернуть Lync Server 2013 на сервере сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="28203-108">Your organization has previously deployed Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat, and you want to deploy Lync Server 2013, Persistent Chat Server.</span></span>

  - <span data-ttu-id="28203-109">Разверните Lync Server 2013, а затем разверните пулы серверов сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="28203-109">Deploy Lync Server 2013, and then deploy Persistent Chat Server pool(s).</span></span>

  - <span data-ttu-id="28203-110">Подготовьте и запланируйте миграцию сохраненных комнат чатов и определите, какое время нужно выключить систему для миграции.</span><span class="sxs-lookup"><span data-stu-id="28203-110">Prepare and plan for migration of your Persistent Chat rooms, and determine an appropriate time to shut down the system for migration.</span></span>

  - <span data-ttu-id="28203-111">Запустите командлеты Windows PowerShell для миграции (**Export-CsPersistentChatData** и **Import-CsPersistentChatData**), чтобы переместить содержимое на сохраняемый сервер чата.</span><span class="sxs-lookup"><span data-stu-id="28203-111">Run the Windows PowerShell cmdlets for migration (**Export-CsPersistentChatData** and **Import-CsPersistentChatData**) to move content to Persistent Chat Server.</span></span>

  - <span data-ttu-id="28203-112">Убедитесь, что миграция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="28203-112">Verify that migration has succeeded.</span></span>

  - <span data-ttu-id="28203-113">Списание устаревшего развертывания.</span><span class="sxs-lookup"><span data-stu-id="28203-113">Decommission your legacy deployment.</span></span>

  - <span data-ttu-id="28203-114">Настройте сохраняемый сервер чата таким образом, чтобы устаревшие клиенты могли подключаться к Lync Server 2013, серверу сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="28203-114">Configure Persistent Chat Server so that legacy clients can connect to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="28203-115">Это необходимо, так как требуется время для развертывания новых клиентов, и вы хотите разрешить существующим пользователям старых клиентов получить доступ к своим комнатам чата, как только это станет возможным.</span><span class="sxs-lookup"><span data-stu-id="28203-115">This is necessary because it takes time to deploy new clients, and you want to enable existing users with legacy clients to have access to their chat rooms as soon as possible.</span></span>

  - <span data-ttu-id="28203-116">Развертывайте новые клиенты, продолжая обеспечивать доступ к своим комнатам чата сотрудникам с помощью устаревшего группового чата (клиентов).</span><span class="sxs-lookup"><span data-stu-id="28203-116">Deploy new clients, while continuing to help ensure that workers with legacy Group Chat (clients) can get to their chat rooms.</span></span>

<span data-ttu-id="28203-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28203-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

