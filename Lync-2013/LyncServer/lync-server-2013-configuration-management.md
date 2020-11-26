---
title: 'Lync Server 2013: Управление конфигурацией'
description: 'Lync Server 2013: Управление конфигурацией.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration management
ms:assetid: 00ea1196-cb40-427f-99a4-5e8037cbf367
ms:mtpsurl: https://technet.microsoft.com/library/Dn720316(v=OCS.15)
ms:contentKeyID: 63969570
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5999708811cc4a34cf846a1ddd481ba38e07c62
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434251"
---
# <a name="configuration-management-in-lync-server-2013"></a><span data-ttu-id="035ce-103">Управление конфигурацией в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="035ce-103">Configuration management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="035ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="035ce-104">

<span> </span></span></span>

<span data-ttu-id="035ce-105">_**Тема последнего изменения:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="035ce-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="035ce-106">Управление конфигурацией — это процесс записи и отслеживания аппаратных и программных ресурсов и сведений о конфигурации системы.</span><span class="sxs-lookup"><span data-stu-id="035ce-106">Configuration management is the process of recording and tracking hardware and software assets and system configuration information.</span></span> <span data-ttu-id="035ce-107">Она обычно используется для отслеживания лицензий на программное обеспечение, обслуживания стандартных аппаратных и программных сборок для клиентских компьютеров и серверов и определения стандартов именования для новых компьютеров.</span><span class="sxs-lookup"><span data-stu-id="035ce-107">It is generally used to track software licenses, maintain a standard hardware and software build for client computers and servers, and define naming standards for new computers.</span></span> <span data-ttu-id="035ce-108">В управлении конфигурацией обычно рассматриваются следующие категории:</span><span class="sxs-lookup"><span data-stu-id="035ce-108">Configuration management generally covers the following categories:</span></span>

  - <span data-ttu-id="035ce-109">**Оборудование**   В этой категории отслеживается оборудование, которому принадлежит ИТ – организация, где находится оборудование, а также кто использует оборудование.</span><span class="sxs-lookup"><span data-stu-id="035ce-109">**Hardware**   This category tracks the pieces of equipment that the IT organization owns, where equipment is located, and who uses equipment.</span></span> <span data-ttu-id="035ce-110">Эта информация позволяет организациям планировать и возобновлять обновления, поддерживать стандартные сборки оборудования, сообщать о стоимости информационных ресурсов в целях учета и помогать в предотвращении хищения.</span><span class="sxs-lookup"><span data-stu-id="035ce-110">This information enables an organization to plan and budget for upgrades, maintain standard hardware builds, report on the value of IT assets for accounting purposes, and help prevent theft.</span></span>

  - <span data-ttu-id="035ce-111">**Software (программное обеспечение**   )   Эта категория отслеживает программное обеспечение, которое установлено на каждом компьютере, Номера версий и места проведения лицензий.</span><span class="sxs-lookup"><span data-stu-id="035ce-111">**Software**   This category tracks software that is installed on each computer, the version numbers, and where the licenses are held.</span></span> <span data-ttu-id="035ce-112">Эти сведения помогают планировать обновления, обеспечивать лицензирование программного обеспечения и определять наличие неавторизованного (и нелицензированного) программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="035ce-112">This information helps plan upgrades, to ensure that software is licensed, and detect the presence of unauthorized (and unlicensed) software.</span></span>

  - <span data-ttu-id="035ce-113">**Стандартные сборки**   В этой категории отслеживается текущая стандартная сборка для клиентских компьютеров и серверов и находятся ли клиентские компьютеры и серверы в соответствии с этим стандартом.</span><span class="sxs-lookup"><span data-stu-id="035ce-113">**Standard Builds**   This category tracks the current standard build for the client computers and servers and whether the client computers and servers meet this standard.</span></span> <span data-ttu-id="035ce-114">Определение и принудительное использование стандартных сборок помогает специалистам службы поддержки, так как персонал обязан поддерживать только ограниченное количество версий каждой части программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="035ce-114">Defining and enforcing standard builds helps support staff because the staff is required to maintain only a limited number of versions of each piece of software.</span></span>

  - <span data-ttu-id="035ce-115">**Накопительные обновления и исправления**   Эта категория отслеживает, какие пакеты обновления проверены и утверждены для использования и какие компьютеры обновлены.</span><span class="sxs-lookup"><span data-stu-id="035ce-115">**Cumulative Updates and Hotfixes**   This category tracks which service packs are tested and approved for use and which computers are up to date.</span></span> <span data-ttu-id="035ce-116">Эта информация важна для снижения риска нарушения безопасности компьютеров и обнаружения пользователей с установленными неодобренными обновлениями.</span><span class="sxs-lookup"><span data-stu-id="035ce-116">This information is important to reduce the risk of computers being compromised and to detect users who have installed unapproved updates.</span></span>

  - <span data-ttu-id="035ce-117">**Сведения о конфигурации системы**   В этой категории отслеживается функция системы, взаимодействие между системными элементами и процессы, зависящие от системы, в которой выполняется плавный запуск.</span><span class="sxs-lookup"><span data-stu-id="035ce-117">**System Configuration Information**   This category tracks the function of a system, the interaction between system elements, and the processes that depend on a system that is running smoothly.</span></span> <span data-ttu-id="035ce-118">Например, прокси-сервер стороннего поставщика можно настроить на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="035ce-118">For example, third-party proxy server may be configured on a single server.</span></span> <span data-ttu-id="035ce-119">При возникновении сбоя может потребоваться, чтобы прокси-сервер был заблокирован на этом сервере и планы на непредвиденные случаи.</span><span class="sxs-lookup"><span data-stu-id="035ce-119">The proxy server’s dependence on this server should be understood and contingency plans may be required if there is a failure.</span></span> <span data-ttu-id="035ce-120">Если прокси-сервер можно настроить так, чтобы он также мог взаимодействовать с другим сервером переднего плана, зависимости и планы на непредвиденные случаи, скорее всего, изменятся.</span><span class="sxs-lookup"><span data-stu-id="035ce-120">If the proxy server can be configured to also communicate with another front-end server, dependencies and contingency plans will probably change.</span></span>

<div>

## <a name="implementing-configuration-management"></a><span data-ttu-id="035ce-121">Реализация управления конфигурацией</span><span class="sxs-lookup"><span data-stu-id="035ce-121">Implementing configuration management</span></span>

<span data-ttu-id="035ce-122">Определив элементы, необходимые для управления, реализуйте управление конфигурацией, собирая данные и отчеты.</span><span class="sxs-lookup"><span data-stu-id="035ce-122">After you determine what items need managing, implement configuration management by collecting data and reporting data.</span></span> <span data-ttu-id="035ce-123">Самый простой подход для малых организаций — собирать данные вручную (номер и модель клиентских компьютеров, операционную систему, установленное программное обеспечение) и сохранять их в документе Office Word или Office Excel.</span><span class="sxs-lookup"><span data-stu-id="035ce-123">The simplest approach for small organizations is to collect data manually (number and model of client computers, operating system, installed software) and save it in an Office Word or Office Excel document.</span></span> <span data-ttu-id="035ce-124">Для более крупных, более сложных и постоянно меняющихся систем обнаружение ресурсов и сбор подробных данных должно выполняться автоматически.</span><span class="sxs-lookup"><span data-stu-id="035ce-124">For larger, more complex, and constantly changing systems, the discovery of assets and collection of detailed information must be automated.</span></span> <span data-ttu-id="035ce-125">Определите, какая информация важна для вашей организации, и записывайте ее в базу данных.</span><span class="sxs-lookup"><span data-stu-id="035ce-125">Decide what information is relevant to your organization and record it in a database.</span></span>

<span data-ttu-id="035ce-126">База данных управления конфигурацией — это полезный инструмент для поддержки персонала и управления в указанных ниже областях.</span><span class="sxs-lookup"><span data-stu-id="035ce-126">The configuration management database is a useful tool for support staff and management in the following areas:</span></span>

  - <span data-ttu-id="035ce-127">**Аудит безопасности**   База данных позволяет идентифицировать серверы, на которых работают системы Lync Server и клиентские компьютеры, на которых должны быть установлены исправления, или у которых пропущена Установка пакета обновления или последних обновлений антивирусной программы.</span><span class="sxs-lookup"><span data-stu-id="035ce-127">**Security Audits**   The database enables you to identify servers that are running Lync Server and client computer systems that must have hotfixes applied or that have missed the installation of a service pack or the latest antivirus updates.</span></span>

  - <span data-ttu-id="035ce-128">**Установка программного обеспечения**   Определение версий и отслеживание клиентских программного обеспечения помогает администраторам планировать обновления версий и новые установки, а также помогать в документации и соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="035ce-128">**Software Installation**   Identifying client software versions and tracking them will aid administrators in planning version updates and new installs and also by helping with licensing documentation and compliance.</span></span>

  - <span data-ttu-id="035ce-129">**Сведения о конфигурации**   Если вы сохраняете актуальный список всех параметров, которые были изменены по умолчанию, вы сможете быстро и эффективнее устранить неполадки.</span><span class="sxs-lookup"><span data-stu-id="035ce-129">**Configuration Information**   If you maintain an up-to-date list of all settings that were changed from their default, then you'll be able to troubleshoot issues quickly and more effectively.</span></span>

  - <span data-ttu-id="035ce-130">**Планирование обновлений**   Если в ходе проверки производительности выясняется, что на серверах баз данных Lync требуется дополнительное дисковое пространство, важно знать, имеет ли каждый сервер внутренний RAID-контроллер.</span><span class="sxs-lookup"><span data-stu-id="035ce-130">**Planning Upgrades**   If a capacity review reveals that additional storage space is required on your Lync database servers, it’s important to know whether each server has an internal RAID controller.</span></span> <span data-ttu-id="035ce-131">Если это так, то они являются одной и той же моделью.</span><span class="sxs-lookup"><span data-stu-id="035ce-131">If they do, then are they the same model?</span></span> <span data-ttu-id="035ce-132">Установлено ли на них одинаковое число дисков?</span><span class="sxs-lookup"><span data-stu-id="035ce-132">Do they have the same number of disks installed?</span></span> <span data-ttu-id="035ce-133">База данных управления конфигурацией будет указывать тип диска, который можно установить, номер и путь обновления в каждом случае.</span><span class="sxs-lookup"><span data-stu-id="035ce-133">The configuration management database will indicate the type of disk that can be installed, the number, and the upgrade path in each case.</span></span>

</div>

<div>

## <a name="tools-used-for-configuration-management"></a><span data-ttu-id="035ce-134">Инструменты, используемые для управления конфигурацией</span><span class="sxs-lookup"><span data-stu-id="035ce-134">Tools used for configuration management</span></span>

<span data-ttu-id="035ce-135">Существует множество инструментов для работы с ресурсами, аудита и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="035ce-135">There are many tools to discover, audit, and report assets.</span></span> <span data-ttu-id="035ce-136">Некоторые из этих средств обсуждаются в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="035ce-136">Some of these tools are discussed in this section.</span></span>

  - <span data-ttu-id="035ce-137">**Автоматические сценарии**   Вы можете создавать простые сценарии, чтобы сообщать такие элементы, как операционная система, уровень пакета обновления и наличие программного обеспечения на определенном наборе компьютеров.</span><span class="sxs-lookup"><span data-stu-id="035ce-137">**Automated Scripts**   You can write simple scripts to report items such as the operating system, service pack level, and whether software exists on a specific set of computers.</span></span> <span data-ttu-id="035ce-138">Эти сценарии можно писать на конкретные требования Организации.</span><span class="sxs-lookup"><span data-stu-id="035ce-138">You can write these scripts to an organization’s exact requirements.</span></span> <span data-ttu-id="035ce-139">Тем не менее, требуемое количество сценариев и их сложность может усложнить создание и обслуживание сценариев.</span><span class="sxs-lookup"><span data-stu-id="035ce-139">However, the required number of scripts and their complexity can make scripts expensive to create and maintain.</span></span>

  - <span data-ttu-id="035ce-140">**Автоматические инструменты**   В зависимости от размера вашего бизнеса и потребностей Организации вы можете использовать автоматизированные средства.</span><span class="sxs-lookup"><span data-stu-id="035ce-140">**Automated Tools**   Depending on the size of your business and your organizational needs, you may want to consider using automated tools.</span></span> <span data-ttu-id="035ce-141">Такие инструменты, как Microsoft Endpoint Configuration Manager, включают стандартные шаблоны отчетов (например, уровень пакета обновления), а также позволяют создавать пользовательские отчеты, например, для пользовательского приложения.</span><span class="sxs-lookup"><span data-stu-id="035ce-141">Tools such as Microsoft Endpoint Configuration Manager incorporate standard report templates (such as service pack level) and also enable you to create customized reports, for example, for a custom application.</span></span> <span data-ttu-id="035ce-142">Диспетчер конфигурации конечных точек Майкрософт также можно использовать для создания отчетов о конфигурациях оборудования и программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="035ce-142">The Microsoft Endpoint Configuration Manager can also be used to report on hardware and software configurations.</span></span>

</div>

<div>

## <a name="relationship-with-change-management"></a><span data-ttu-id="035ce-143">Связь с управлением изменениями</span><span class="sxs-lookup"><span data-stu-id="035ce-143">Relationship with change management</span></span>

<span data-ttu-id="035ce-144">Управление конфигурацией тесно связано с управлением изменениями.</span><span class="sxs-lookup"><span data-stu-id="035ce-144">Configuration management is closely related to change management.</span></span> <span data-ttu-id="035ce-145">Управление конфигурацией определяет необходимость изменения и идентификации и записи, внесенные в ходе изменения.</span><span class="sxs-lookup"><span data-stu-id="035ce-145">Configuration management identifies the need for change and identifies and records that a change has occurred.</span></span> <span data-ttu-id="035ce-146">Например, можно использовать базу данных управления конфигурацией для идентификации серверов, которым требуется исправление.</span><span class="sxs-lookup"><span data-stu-id="035ce-146">For example, the configuration management database can be used to identify servers that require a hotfix.</span></span> <span data-ttu-id="035ce-147">Управление изменениями затем определяет процесс применения исправления.</span><span class="sxs-lookup"><span data-stu-id="035ce-147">Change management then defines the process for applying the hotfix.</span></span>

<span data-ttu-id="035ce-148">И наоборот, если вы выйдете новое накопительное обновление, процесс управления изменениями должен предоставить эту информацию системе управления конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="035ce-148">Conversely, if a new cumulative update is rolled out, the change management process should supply this information to the configuration management system.</span></span> <span data-ttu-id="035ce-149">Средства управления конфигурацией, скорее всего, должны быть настроены для идентификации нового программного обеспечения, чтобы они могли находить и отслеживать, где и когда развертывается программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="035ce-149">The configuration management tools will probably need to be configured to identify the new software so that they can discover and track where and when the software is deployed.</span></span>

<span data-ttu-id="035ce-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="035ce-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

