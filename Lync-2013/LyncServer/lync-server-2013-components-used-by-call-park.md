---
title: 'Lync Server 2013: компоненты, используемые парковкой вызовов'
description: 'Lync Server 2013: компоненты, используемые при приостановке звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398527"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a><span data-ttu-id="879d4-103">Компоненты, используемые парковкой вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="879d4-103">Components used by Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="879d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="879d4-104">

<span> </span></span></span>

<span data-ttu-id="879d4-105">_**Тема последнего изменения:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="879d4-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="879d4-106">Приложение для парковки звонков устанавливается автоматически при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="879d4-106">The Call Park application is automatically installed when you deploy Enterprise Voice.</span></span> <span data-ttu-id="879d4-107">Вы включаете приостановку звонков с помощью настройки политики голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="879d4-107">You enable Call Park by configuring voice policy.</span></span> <span data-ttu-id="879d4-108">Следующие компоненты Lync Server 2013 поддерживают приложение для парковки звонков.</span><span class="sxs-lookup"><span data-stu-id="879d4-108">The following Lync Server 2013 components support the Call Park application:</span></span>

  - <span data-ttu-id="879d4-109">**Служба приложений**   Служба приложений предоставляет платформу для развертывания, размещения и управления едиными приложениями для обмена информацией, например с помощью приложения для приостановки звонков.</span><span class="sxs-lookup"><span data-stu-id="879d4-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="879d4-110">Служба приложений устанавливается автоматически на каждый сервер переднего плана в пуле переднего плана и на каждом сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="879d4-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="879d4-111">**Приложение для приостановки звонков**   Приложение для парковки звонков — это одно из Объединенных приложений для обмена данными, размещенных в службе приложений.</span><span class="sxs-lookup"><span data-stu-id="879d4-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="879d4-112">Она включается автоматически при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="879d4-112">It is included automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="879d4-113">Звоните в парки и загружает звонки и управляет орбитами.</span><span class="sxs-lookup"><span data-stu-id="879d4-113">Call Park parks and retrieves calls and manages call park orbits.</span></span>

  - <span data-ttu-id="879d4-114">**Музыкальный файл на удержании**   Если включена музыка, музыкальный файл воспроизводится во время приостановки звонка.</span><span class="sxs-lookup"><span data-stu-id="879d4-114">**Music-on hold-file**   If music in enabled, the music file is played while a call is parked.</span></span> <span data-ttu-id="879d4-115">Музыкальный файл по умолчанию включается, когда установлено приложение для парковки звонков.</span><span class="sxs-lookup"><span data-stu-id="879d4-115">A default music file is included when the Call Park application is installed.</span></span>

  - <span data-ttu-id="879d4-116">**Хранилище файлов**   Приложение для парковки звонков использует хранилище файлов для хранения настраиваемых звуковых файлов.</span><span class="sxs-lookup"><span data-stu-id="879d4-116">**File Store**   The Call Park application uses File Store to hold custom audio files.</span></span>

  - <span data-ttu-id="879d4-117">**Панель управления Lync Server**   С помощью панели управления Lync Server вы можете настроить таблицу "приостановить Звонок" и включить приостановку звонков для пользователей.</span><span class="sxs-lookup"><span data-stu-id="879d4-117">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the call park orbit table and to enable Call Park for users.</span></span>

  - <span data-ttu-id="879d4-118">**Командная консоль Lync Server Management Shell**   Все настройки приложения с приостановкой звонков можно выполнить с помощью командлетов командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="879d4-118">**Lync Server Management Shell**   All Call Park application configuration can be performed by using Lync Server Management Shell cmdlets.</span></span>

<span data-ttu-id="879d4-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="879d4-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

