---
title: 'Lync Server 2013: определение и настройка топологии'
description: 'Lync Server 2013: определение и Настройка топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining and configuring the topology
ms:assetid: 51d1601e-4f83-48d4-ad08-3b4d5e2003aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398339(v=OCS.15)
ms:contentKeyID: 48184146
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec444a1ddf434c5a80fdc2d56bdba27573da14ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431003"
---
# <a name="defining-and-configuring-the-topology-in-lync-server-2013"></a><span data-ttu-id="bfaa3-103">Определение и настройка топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfaa3-103">Defining and configuring the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfaa3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfaa3-104">

<span> </span></span></span>

<span data-ttu-id="bfaa3-105">_**Тема последнего изменения:** 2012-09-14_</span><span class="sxs-lookup"><span data-stu-id="bfaa3-105">_**Topic Last Modified:** 2012-09-14_</span></span>

<span data-ttu-id="bfaa3-106">Вы определяете топологию и настраиваете ее с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-106">You define and configure your topology by using Topology Builder.</span></span> <span data-ttu-id="bfaa3-107">Для Topology Builder не требуется входить в локальную группу администраторов или привилегированную группу домена (например, Администраторы домена).</span><span class="sxs-lookup"><span data-stu-id="bfaa3-107">Topology Builder does not require you to be a member of the local Administrators group or a privileged domain group (such as Domain Admins).</span></span> <span data-ttu-id="bfaa3-108">Вы можете определить свою топологию как обычный пользователь.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-108">You can define your topology as a standard user.</span></span> <span data-ttu-id="bfaa3-109">Когда вы запускаете построитель топологии при первом использовании и последующих сеансах редактирования, вам будет предложено указать расположение, в которое построитель топологии должен загрузить текущий документ конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-109">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="bfaa3-110">Доступны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="bfaa3-110">The choices are the following:</span></span>

  - <span data-ttu-id="bfaa3-111">загрузка топологии из существующего развертывания;</span><span class="sxs-lookup"><span data-stu-id="bfaa3-111">Download topology from existing deployment</span></span>

  - <span data-ttu-id="bfaa3-112">Открытие топологии из локального файла</span><span class="sxs-lookup"><span data-stu-id="bfaa3-112">Open topology from a local file</span></span>

  - <span data-ttu-id="bfaa3-113">Новая топология</span><span class="sxs-lookup"><span data-stu-id="bfaa3-113">New topology</span></span>

<span data-ttu-id="bfaa3-114">Если вы уже определили топологию и установили хранилище Центрального управления, необходимо выбрать загрузку топологии из существующего развертывания.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-114">If you have already defined a topology and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="bfaa3-115">Построитель топологии будет считывать базу данных и получать текущее определение.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-115">Topology Builder will read the database and retrieve the current definition.</span></span> <span data-ttu-id="bfaa3-116">Если у вас есть хранилище Центрального управления, всегда выбирайте этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-116">If you have an existing Central Management store, you should always choose this option.</span></span>

<span data-ttu-id="bfaa3-117">Если вы не установили центральное хранилище для управления и хотите изменить ранее сохраненную конфигурацию, необходимо открыть топологию из локального файла.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-117">If you have not established a Central Management store and want to edit a previously saved configuration, you should choose to open the topology from a local file.</span></span> <span data-ttu-id="bfaa3-118">Откроется файл конфигурации, сохраненный в предыдущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-118">The file that you will open would be the configuration file that was saved in a previous session.</span></span> <span data-ttu-id="bfaa3-119">Вы можете использовать этот параметр, чтобы изменить ранее сохраненную топологию.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-119">You can use this option to edit the previously saved topology.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="bfaa3-120">Если у вас уже есть опубликованная топология, не загружайте локальный файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-120">If you already have a published topology, you should not load a local configuration file.</span></span> <span data-ttu-id="bfaa3-121">Необходимо выбрать загрузку топологии из существующего развертывания.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-121">You should choose to download the topology from an existing deployment.</span></span>



</div>

<span data-ttu-id="bfaa3-122">Выберите, чтобы создать новую топологию, если вы хотите создать новую конфигурацию построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-122">Choose to create a new topology, if you want to create a new Topology Builder configuration.</span></span> <span data-ttu-id="bfaa3-123">Ранее сохраненный макет не перезаписывается, пока вы не решите сохранить его в том же файле, который вы создали в более раннем сеансе конструирования.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-123">A previously saved design is not overwritten unless you choose to save it as the same file that you created in an earlier design session.</span></span>

<span data-ttu-id="bfaa3-124">В каждом из этих параметров вам будет предложено указать расположение для хранения файла конфигурации построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-124">In each of these options, you will be prompted for a location to store the Topology Builder configuration file.</span></span> <span data-ttu-id="bfaa3-125">Для файла может быть задано локальное расположение, общее расположение в установленном файловом ресурсе или съемном носителе.</span><span class="sxs-lookup"><span data-stu-id="bfaa3-125">The location for the file could be a local location, a shared location on an established file share, or removable media.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bfaa3-126">Содержание</span><span class="sxs-lookup"><span data-stu-id="bfaa3-126">In This Section</span></span>

  - [<span data-ttu-id="bfaa3-127">Определение и настройка топологии в средстве построения топологии для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfaa3-127">Define and configure a topology in Topology Builder for Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md)

  - [<span data-ttu-id="bfaa3-128">Определение и настройка пула переднего плана или сервера Standard Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfaa3-128">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="bfaa3-129">Развертывание сопоставленных пулов переднего плана для аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfaa3-129">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-deploying-paired-front-end-pools-for-disaster-recovery.md)

  - [<span data-ttu-id="bfaa3-130">Развертывание зеркального отображения SQL Server для обеспечения высокой доступности внутреннего сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfaa3-130">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)

  - [<span data-ttu-id="bfaa3-131">Изменить или настроить простые URL-адреса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfaa3-131">Edit or configure simple URLs in Lync Server 2013</span></span>](lync-server-2013-edit-or-configure-simple-urls.md)

  - [<span data-ttu-id="bfaa3-132">Выбор центрального сервера управления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfaa3-132">Select the Central Management Server in Lync Server 2013</span></span>](lync-server-2013-select-the-central-management-server.md)

<span data-ttu-id="bfaa3-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfaa3-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

