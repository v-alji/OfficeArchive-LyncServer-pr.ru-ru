---
title: 'Lync Server 2013: настройка SQL Server для Lync Server'
description: 'Lync Server 2013: Настройка SQL Server для Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure SQL Server for Lync Server 2013
ms:assetid: 375e5cc4-e436-46dc-9b02-5063f35cdcc1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425848(v=OCS.15)
ms:contentKeyID: 48183869
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9ac7d8f14c64f3b7935df3f48602a6df1791c7a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433712"
---
# <a name="configure-sql-server-for-lync-server-2013"></a><span data-ttu-id="42be0-103">Настройка SQL Server для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42be0-103">Configure SQL Server for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42be0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42be0-104">

<span> </span></span></span>

<span data-ttu-id="42be0-105">_**Тема последнего изменения:** 2013-08-12_</span><span class="sxs-lookup"><span data-stu-id="42be0-105">_**Topic Last Modified:** 2013-08-12_</span></span>

<span data-ttu-id="42be0-106">В этом разделе объясняется, как развернуть и настроить SQL Server для развертывания в среде Lync Server.</span><span class="sxs-lookup"><span data-stu-id="42be0-106">The topics in this section discuss how to deploy and configure SQL Server to use in an Enterprise deployment of Lync Server.</span></span> <span data-ttu-id="42be0-107">Серверы стандартных выпусков используют размещенную версию SQL Server Express на выровненном по размеру для рабочих нагрузок сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="42be0-107">Standard Edition servers use a collocated SQL Server Express version of SQL Server that is right sized for the workloads of a Standard Edition server.</span></span>

<span data-ttu-id="42be0-108">Хранилище Lync Server 2013 Central Management содержит данные пользователей для всех серверов выпуска Enterprise Edition в рамках пула и предназначено для размещения на сервере SQL Server с интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="42be0-108">The Lync Server 2013 Central Management store holds user data for all Enterprise Edition servers within a pool, and is designed to be located on a SQL Server -based Back End Server.</span></span> <span data-ttu-id="42be0-109">Централизованное хранилище не может быть установлено на том же компьютере, что и любая другая роль Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="42be0-109">As a centralized repository, the Central Management store cannot be installed on the same computer as any other Lync Server 2013 role.</span></span> <span data-ttu-id="42be0-110">Хранилище Центрального управления не может находиться на сервере Enterprise Edition в пуле.</span><span class="sxs-lookup"><span data-stu-id="42be0-110">The Central Management store cannot reside on an Enterprise Edition server in the pool.</span></span> <span data-ttu-id="42be0-111">Хранилище Центрального управления создается автоматически при первой публикации топологии и выбирается для создания баз данных.</span><span class="sxs-lookup"><span data-stu-id="42be0-111">The Central Management store is created automatically when you publish the topology for the first time and select to create the databases.</span></span> <span data-ttu-id="42be0-112">Чтобы установка прошла успешно, на компьютере, который вы указываете как сервер заднего использования, должно быть установлено программное обеспечение SQL Server Database.</span><span class="sxs-lookup"><span data-stu-id="42be0-112">The computer that you designate as the Back End Server must already be running SQL Server database software in order for the installation to succeed.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="42be0-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="42be0-113">In This Section</span></span>

  - [<span data-ttu-id="42be0-114">Размещение данных и файла журнала SQL Server для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42be0-114">SQL Server data and log file placement for Lync Server 2013</span></span>](lync-server-2013-sql-server-data-and-log-file-placement.md)

  - [<span data-ttu-id="42be0-115">Настройка SQL Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42be0-115">Configure SQL Server in Lync Server 2013</span></span>](lync-server-2013-configure-sql-server.md)

  - [<span data-ttu-id="42be0-116">Разрешения на развертывание для SQL Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42be0-116">Deployment permissions for SQL Server in Lync Server 2013</span></span>](lync-server-2013-deployment-permissions-for-sql-server.md)

  - [<span data-ttu-id="42be0-117">Установка базы данных с помощью командной консоли Lync Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42be0-117">Database installation using Lync Server Management Shell in Lync Server 2013</span></span>](lync-server-2013-database-installation-using-lync-server-management-shell.md)

  - [<span data-ttu-id="42be0-118">Обзор требований к брандмауэру для SQL Server с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42be0-118">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>](lync-server-2013-understanding-firewall-requirements-for-sql-server.md)

  - [<span data-ttu-id="42be0-119">Настройка кластеризации SQL Server для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42be0-119">Configure SQL Server clustering for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-clustering.md)

<span data-ttu-id="42be0-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42be0-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

