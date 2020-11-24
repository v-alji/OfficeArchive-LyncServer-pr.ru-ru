---
title: 'Lync Server 2013: управление топологией Lync Server'
description: 'Lync Server 2013: Управление топологией Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Lync Server 2013 topology
ms:assetid: 323ef486-c907-4036-a2bf-c869b1d7f288
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520973(v=OCS.15)
ms:contentKeyID: 48183784
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba460dc3129d7004964b1a7d783413a85d06f2c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400018"
---
# <a name="managing-the-lync-server-2013-topology"></a><span data-ttu-id="2f3de-103">Управление топологией Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-103">Managing the Lync Server 2013 topology</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f3de-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f3de-104">

<span> </span></span></span>

<span data-ttu-id="2f3de-105">_**Тема последнего изменения:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="2f3de-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="2f3de-106">В этой статье приведены пошаговые инструкции для задач, которые можно выполнить с помощью страницы **Topology** на панели управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2f3de-106">Topics in this section provide step-by-step procedures for tasks you can perform using the **Topology** page in Lync Server 2013 Control Panel.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2f3de-107">Содержание</span><span class="sxs-lookup"><span data-stu-id="2f3de-107">In This Section</span></span>

  - [<span data-ttu-id="2f3de-108">Просмотр списка компьютеров с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-108">View a list of computers running Lync Server 2013</span></span>](lync-server-2013-view-a-list-of-computers-running-lync-server-2013.md)

  - [<span data-ttu-id="2f3de-109">Просмотр состояния служб, запущенных на компьютере в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-109">View the status of services running on a computer in Lync Server 2013</span></span>](lync-server-2013-view-the-status-of-services-running-on-a-computer.md)

  - [<span data-ttu-id="2f3de-110">Просмотр подробных сведений о службе в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-110">View details about a service in Lync Server 2013</span></span>](lync-server-2013-view-details-about-a-service.md)

  - [<span data-ttu-id="2f3de-111">Запуск и остановка служб Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-111">Start or stop Lync Server 2013 services</span></span>](lync-server-2013-start-or-stop-lync-server-services.md)

  - [<span data-ttu-id="2f3de-112">Предотвращение сеансов для служб в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-112">Prevent sessions for services in Lync Server 2013</span></span>](lync-server-2013-prevent-sessions-for-services.md)

  - [<span data-ttu-id="2f3de-113">Upgrade or update Front End Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-113">Upgrade or update Front End Servers in Lync Server 2013</span></span>](lync-server-2013-upgrade-or-update-front-end-servers.md)

  - [<span data-ttu-id="2f3de-114">Add or remove a Front End Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-114">Add or remove a Front End Server in Lync Server 2013</span></span>](lync-server-2013-add-or-remove-a-front-end-server.md)

  - [<span data-ttu-id="2f3de-115">Обновление или обновление серверного сервера или стандартного выпуска Standard в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-115">Upgrade or update a Back End Server or Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-upgrade-or-update-a-back-end-server-or-standard-edition-server.md)

  - [<span data-ttu-id="2f3de-116">Управление приложениями языка обработки Microsoft SIP (MSPL) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-116">Managing Microsoft SIP Processing Language (MSPL) applications in Lync Server 2013</span></span>](lync-server-2013-managing-microsoft-sip-processing-language-mspl-applications.md)

  - [<span data-ttu-id="2f3de-117">Управление простыми URL-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f3de-117">Managing simple URLs in Lync Server 2013</span></span>](lync-server-2013-managing-simple-urls.md)

<span data-ttu-id="2f3de-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f3de-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

