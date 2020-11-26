---
title: 'Lync Server 2013: поддерживаемые пути миграции и сценарии сосуществования серверов'
description: 'Lync Server 2013: Поддерживаемые пути миграции сервера и сосуществования.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server migration paths and coexistence scenarios
ms:assetid: 2a6a730f-7f80-45f9-9540-3edfdaa265fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425764(v=OCS.15)
ms:contentKeyID: 48183686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d0a40ac6cc6570cf79b56dc896277c83909b5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423633"
---
# <a name="supported-server-migration-paths-and-coexistence-scenarios-in-lync-server-2013"></a><span data-ttu-id="fd393-103">Поддерживаемые пути миграции и сценарии сосуществования серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd393-103">Supported server migration paths and coexistence scenarios in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd393-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd393-104">

<span> </span></span></span>

<span data-ttu-id="fd393-105">_**Тема последнего изменения:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="fd393-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="fd393-106">Lync Server 2013 поддерживает миграцию с любого из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="fd393-106">Lync Server 2013 supports migration from either of the following:</span></span>

  - <span data-ttu-id="fd393-107">Microsoft Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="fd393-107">Microsoft Lync Server 2010</span></span>

  - <span data-ttu-id="fd393-108">Microsoft Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="fd393-108">Microsoft Office Communications Server 2007 R2</span></span>

<span data-ttu-id="fd393-109">Миграция из среды, использующей оба эти предыдущих версии, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fd393-109">Migration from an environment running both of these previous versions is not supported.</span></span> <span data-ttu-id="fd393-110">Миграция с более ранних версий, например Microsoft Office Communications Server 2007 или Live Communications Server 2005, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fd393-110">Migration from earlier versions, such as Microsoft Office Communications Server 2007 or Live Communications Server 2005, is not supported.</span></span> <span data-ttu-id="fd393-111">Если Ваше прежнее развертывание включало групповой чат, его необходимо перенести отдельно.</span><span class="sxs-lookup"><span data-stu-id="fd393-111">If your previous deployment included Group Chat, you must migrate it separately.</span></span>

<div>

## <a name="migration-methods"></a><span data-ttu-id="fd393-112">Способы миграции</span><span class="sxs-lookup"><span data-stu-id="fd393-112">Migration Methods</span></span>

<span data-ttu-id="fd393-113">Поддерживается миграция всех топологий Lync Server и серверных ролей.</span><span class="sxs-lookup"><span data-stu-id="fd393-113">Migration of all Lync Server topologies and server roles is supported.</span></span> <span data-ttu-id="fd393-114">Вы можете выполнить миграцию из одной топологии в другую, например с сервера Standard Edition на сервер Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="fd393-114">You can migrate from one topology to a different topology, including from Standard Edition server to Enterprise Edition server.</span></span>

<span data-ttu-id="fd393-115">Lync Server 2013 поддерживает только следующий способ миграции:</span><span class="sxs-lookup"><span data-stu-id="fd393-115">Lync Server 2013 supports only the following migration method:</span></span>

  - <span></span>  
    <span data-ttu-id="fd393-116">**Переход с одной стороны на другую.**</span><span class="sxs-lookup"><span data-stu-id="fd393-116">**Side-by-side migration.**</span></span> <span data-ttu-id="fd393-117">При переходе по отдельности Lync Server 2013 разворачивается вместе с существующим развертыванием Microsoft Lync Server 2010 или Office Communications Server 2007 R2, а затем переносятся на новые серверы и перемещаются на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fd393-117">In side-by-side migration, Lync Server 2013 is deployed alongside an existing Microsoft Lync Server 2010 or Office Communications Server 2007 R2 deployment, and then you transfer operations to the new servers and move users to Lync Server 2013.</span></span> <span data-ttu-id="fd393-118">Для использования этого метода требуются дополнительные серверные платформы, в том числе оборудование и программное обеспечение, и имена систем и пулов различаются в новой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fd393-118">This method requires additional server platforms, including hardware and software, during migration, and system names and pool names are different in the new configuration.</span></span> <span data-ttu-id="fd393-119">Если вы хотите вернуться к предыдущей версии, вы можете переместить операции обратно на предыдущие серверы.</span><span class="sxs-lookup"><span data-stu-id="fd393-119">If it becomes necessary to roll back to the previous version, you can shift operations back to the previous servers.</span></span>

<span data-ttu-id="fd393-120">Миграция в лесах доменных служб Active Directory не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fd393-120">Migration across Active Directory Domain Services forests is not supported.</span></span>

<span data-ttu-id="fd393-121">Рекомендуемый путь миграции — поэтапный подход.</span><span class="sxs-lookup"><span data-stu-id="fd393-121">The recommended migration path is a phased approach.</span></span> <span data-ttu-id="fd393-122">Сведения о переходе с более ранней версии, включая соответствующие фазирование развертывания компонентов, можно найти в следующих статьях в документации по миграции.</span><span class="sxs-lookup"><span data-stu-id="fd393-122">For details about migrating from a previous release, including the appropriate phasing of component deployment, see the following topics in the Migration documentation:</span></span>

  - [<span data-ttu-id="fd393-123">Миграция с Lync Server 2010 на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd393-123">Migration from Lync Server 2010 to Lync Server 2013</span></span>](migration-from-lync-server-2010-to-lync-server-2013.md)

  - [<span data-ttu-id="fd393-124">Миграция с Office Communications Server 2007 R2 на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd393-124">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md)

  - [<span data-ttu-id="fd393-125">Миграция с групповой беседы в Lync Server 2010 или Office Communications Server 2007 R2 на сервер сохраняемого сеанса беседы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd393-125">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)

</div>

<span id="BKMK_PhasedMigration"></span>

<div>

## <a name="coexistence-scenarios"></a><span data-ttu-id="fd393-126">Сценарии сосуществования</span><span class="sxs-lookup"><span data-stu-id="fd393-126">Coexistence Scenarios</span></span>

<span data-ttu-id="fd393-127">Lync Server 2013 может сосуществовать с компонентами либо развертыванием Lync Server 2010, либо развертыванием Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="fd393-127">Lync Server 2013 can coexist with components of either a Lync Server 2010 deployment or an Office Communications Server 2007 R2 deployment.</span></span> <span data-ttu-id="fd393-128">Одновременное развертывание Lync Server 2013 с помощью Lync Server 2010 и Office Communications Server 2007 R2 (параллельное развертывание всех трех версий) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fd393-128">Concurrent deployment of Lync Server 2013 with both Lync Server 2010 and Office Communications Server 2007 R2 (concurrent deployment of all three versions) is not supported.</span></span>

<span data-ttu-id="fd393-129">При поэтапной миграции, когда более раннее развертывание Lync Server 2010 или Office Communications Server 2007 R2 входит в состав нового развертывания Lync Server 2013, поддержка маршрутизации для смешанной версии ограничена.</span><span class="sxs-lookup"><span data-stu-id="fd393-129">During a phased migration in which a previous Lync Server 2010 or Office Communications Server 2007 R2 deployment coexists temporarily with the new Lync Server 2013 deployment, support for mixed version routing is limited.</span></span> <span data-ttu-id="fd393-130">Подробности можно найти в документации по миграции.</span><span class="sxs-lookup"><span data-stu-id="fd393-130">For details, see the Migration documentation.</span></span>

<span data-ttu-id="fd393-131">Для экземпляров базы данных Lync Server 2013 вы должны использовать отдельные и различные компьютеры с Microsoft SQL Server 2008 R2 или Microsoft SQL Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fd393-131">You must use separate and distinct computers running Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 for your Lync Server 2013 database instances.</span></span> <span data-ttu-id="fd393-132">Вы не можете использовать один и тот же экземпляр SQL Server для пула внешних интерфейсов Lync Server 2013, который вы используете для пула интерфейсов Lync Server 2010 или Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="fd393-132">You cannot use the same instance of SQL Server for a Lync Server 2013 Front End pool that you use for a Lync Server 2010 or Office Communications Server 2007 R2 Front End pool.</span></span> <span data-ttu-id="fd393-133">Если вы определили и настроили Lync Server 2013 в построителе топологии для развертывания, в котором уже установлено приложение Lync Server 2010 или Office Communications Server 2007 R2, построитель топологии не позволит определить экземпляр Lync Server 2013, который уже используется в топологии.</span><span class="sxs-lookup"><span data-stu-id="fd393-133">If you define and configure Lync Server 2013 in Topology Builder for a deployment that already has Lync Server 2010 or Office Communications Server 2007 R2 deployed, Topology Builder will not allow you to define an instance of a Lync Server 2013 that is already in use in the topology.</span></span>

<span data-ttu-id="fd393-134">В построителе топологии появится следующее сообщение об этой ошибке: " \[ полное доменное имя SQL Server сервера \] уже включает в себя роль размещения экземпляров SQL" User Store ".</span><span class="sxs-lookup"><span data-stu-id="fd393-134">Topology Builder will display the following message to inform you of this issue: "The SQL server \[FQDN of the server\] already contains a SQL instance hosting role 'User Store."</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fd393-135">Если вы планируете развертывать роли сервера, новые для развертывания Lync Server 2013, необходимо сначала обновить существующее развертывание в соответствии с документацией о миграции и документацией по развертыванию, а затем развернуть новые роли сервера в соответствии с документацией по планированию и развертыванием.</span><span class="sxs-lookup"><span data-stu-id="fd393-135">If you intend to deploy server roles that are new to your Lync Server 2013 deployment, you should first upgrade your existing deployment as described in the Migration documentation and the Deployment documentation, and then deploy the new server roles as described in the Planning documentation and Deployment documentation.</span></span> <span data-ttu-id="fd393-136">Если вы переносите предыдущую версию группового чата, перенесите ее в последнюю очередь после завершения процесса миграции всех остальных компонентов из Lync Server 2010 или Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="fd393-136">If you are migrating a previous version of Group Chat, migrate it last, after completing the process for migrating all other components from Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<span data-ttu-id="fd393-137">Для конкретных требований сосуществования и других сведений о сосуществовании и миграции компонентов Lync Server 2010 или Office Communications Server 2007 R2 и Lync Server 2013 ознакомьтесь со статьей [Переход с Lync server 2010 на Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) и [Переход с Office Communications Server 2007 R2 на](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md) Lync Server 2013 в документации по миграции.</span><span class="sxs-lookup"><span data-stu-id="fd393-137">For specific coexistence requirements and other details about coexistence and migration of Lync Server 2010 or Office Communications Server 2007 R2 and Lync Server 2013 components, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md) in the Migration documentation.</span></span> <span data-ttu-id="fd393-138">Подробнее о поддержке клиентов смешанной версии можно узнать [в разделе Поддерживаемые клиенты предыдущих развертываний в Lync Server 2013](lync-server-2013-supported-clients-from-previous-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="fd393-138">For details about mixed version support for clients, see [Supported clients from previous deployments in Lync Server 2013](lync-server-2013-supported-clients-from-previous-deployments.md).</span></span>

<span data-ttu-id="fd393-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd393-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

