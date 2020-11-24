---
title: 'Lync Server 2013: Настройка основного сервера управления'
description: 'Lync Server 2013: Настройка основного сервера управления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the primary management server
ms:assetid: 44e2e9a8-c130-4c66-9871-80b1ff11b27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204844(v=OCS.15)
ms:contentKeyID: 48183986
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43f986f4f03e96cafa27dfdd302bb98a00d8b2ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400036"
---
# <a name="configuring-the-primary-management-server-in-lync-server-2013"></a><span data-ttu-id="d4e70-103">Настройка основного сервера управления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4e70-103">Configuring the primary management server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4e70-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4e70-104">

<span> </span></span></span>

<span data-ttu-id="d4e70-105">_**Тема последнего изменения:** 2014-03-19_</span><span class="sxs-lookup"><span data-stu-id="d4e70-105">_**Topic Last Modified:** 2014-03-19_</span></span>

<span data-ttu-id="d4e70-106">Чтобы воспользоваться всеми преимуществами новых возможностей мониторинга работоспособности, включенных в Microsoft Lync Server 2013, администраторы должны сначала назначить компьютер для работы в качестве основного сервера управления; на этом компьютере необходимо установить System Center Operations Manager 2007 R2 или System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="d4e70-106">In order to take full advantage of the new health monitoring capabilities included in Microsoft Lync Server 2013 administrators must first designate a computer to act as your primary management server; on that computer you must then install System Center Operations Manager 2007 R2 or System Center Operations Manager 2012.</span></span> <span data-ttu-id="d4e70-107">Кроме того, необходимо установить поддерживаемую версию SQL Server, которая будет выступать в качестве серверной базы данных Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="d4e70-107">In addition, you must install a supported version of SQL Server to function as your Operations Manager back-end database.</span></span> <span data-ttu-id="d4e70-108">Если вы используете System Center Operations Manager 2012, вы можете использовать в качестве серверной базы данных любую из указанных ниже версий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d4e70-108">If you are using System Center Operations Manager 2012 you can use any of the following versions of SQL Server as your back-end database:</span></span>

  - <span data-ttu-id="d4e70-109">SQL Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="d4e70-109">SQL Server 2008 R2 Service Pack 1</span></span>

  - <span data-ttu-id="d4e70-110">SQL Server 2008 R2 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="d4e70-110">SQL Server 2008 R2 Service Pack 2</span></span>

<span data-ttu-id="d4e70-111">Если вы используете System Center Operations Manager 2007 R2, рекомендуется установить либо SQL Server 2005 с пакетом обновления 4, либо SQL Server 2008 с пакетом обновления 3.</span><span class="sxs-lookup"><span data-stu-id="d4e70-111">If you are using System Center Operations Manager 2007 R2 it is recommended that you install either SQL Server 2005 Service Pack 4 or SQL Server 2008 Service Pack 3.</span></span> <span data-ttu-id="d4e70-112">Вы также можете использовать SQL Server 2008 R2 в качестве серверной базы данных для System Center Operations Manager 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4e70-112">You can also use SQL Server 2008 R2 as the backend database for System Center Operations Manager 2007 R2.</span></span> <span data-ttu-id="d4e70-113">Более подробную информацию о настройке SQL Server 2008 R2 для работы с System Center Operations Manager 2007 R2 можно найти в приложении 1 из этой документации.</span><span class="sxs-lookup"><span data-stu-id="d4e70-113">See Appendix 1 of this documentation for more information on configuring SQL Server 2008 R2 to work with System Center Operations Manager 2007 R2.</span></span>

<span data-ttu-id="d4e70-114">При установке System Center Operations Manager 2012 или System Center Operations Manager 2007 R2 вам нужно установить все компоненты этого продукта, в том числе:</span><span class="sxs-lookup"><span data-stu-id="d4e70-114">When you install System Center Operations Manager 2012 or System Center Operations Manager 2007 R2 you need to install all the components of that product, including:</span></span>

  - <span data-ttu-id="d4e70-115">рабочую базу данных;</span><span class="sxs-lookup"><span data-stu-id="d4e70-115">Operational database</span></span>

  - <span data-ttu-id="d4e70-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="d4e70-116">Server</span></span>

  - <span data-ttu-id="d4e70-117">консоль;</span><span class="sxs-lookup"><span data-stu-id="d4e70-117">Console</span></span>

  - <span data-ttu-id="d4e70-118">Командлеты Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4e70-118">Windows PowerShell cmdlets</span></span>

  - <span data-ttu-id="d4e70-119">веб-консоль;</span><span class="sxs-lookup"><span data-stu-id="d4e70-119">Web console</span></span>

  - <span data-ttu-id="d4e70-120">отчеты;</span><span class="sxs-lookup"><span data-stu-id="d4e70-120">Reporting</span></span>

  - <span data-ttu-id="d4e70-121">хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="d4e70-121">Data warehouse</span></span>

<span data-ttu-id="d4e70-122">Эти компоненты и их установка не будут подробно рассмотрены в этом документе.</span><span class="sxs-lookup"><span data-stu-id="d4e70-122">These components and their installation will not be discussed in detail in this document.</span></span> <span data-ttu-id="d4e70-123">Подробные сведения о System Center Operations Manager 2007 R2 можно найти в документации Operations Manager 2007 R2 на странице <https://go.microsoft.com/fwlink/p/?linkid=257526> System Center Operations manager 2012 по адресу <https://go.microsoft.com/fwlink/p/?linkid=257527> .</span><span class="sxs-lookup"><span data-stu-id="d4e70-123">For details about System Center Operations Manager 2007 R2, see the Operations Manager 2007 R2 documentation at <https://go.microsoft.com/fwlink/p/?linkid=257526> and the System Center Operations Manager 2012 documentation at <https://go.microsoft.com/fwlink/p/?linkid=257527>.</span></span> <span data-ttu-id="d4e70-124">Следуйте этим инструкциям, если вы планируете использовать сервер SQL Server 2005 или SQL Server 2008 с пакетом обновления 1 в качестве серверной части базы данных.</span><span class="sxs-lookup"><span data-stu-id="d4e70-124">You should follow those instructions if you are going to use SQL Server 2005 or SQL Server 2008 Service Pack 1 as your back-end database.</span></span>

<span data-ttu-id="d4e70-125">Если вы используете System Center Operations Manager 2012, то можете использовать SQL Server 2012 в качестве серверной базы данных.</span><span class="sxs-lookup"><span data-stu-id="d4e70-125">If you are using System Center Operations Manager 2012 then you can use SQL Server 2012 as your back-end database.</span></span> <span data-ttu-id="d4e70-126">Подробные сведения о SQL Server 2012 можно найти в книге электронная документация по SQL Server 2012 по адресу [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528) .</span><span class="sxs-lookup"><span data-stu-id="d4e70-126">For details about SQL Server 2012, see Books Online for SQL Server 2012 at [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528).</span></span>

<span data-ttu-id="d4e70-127">Имейте в виду, что для развертывания Lync Server вы можете использовать только один основной сервер управления.</span><span class="sxs-lookup"><span data-stu-id="d4e70-127">Keep in mind that you can only have a single Primary Management Server per Lync Server deployment.</span></span> <span data-ttu-id="d4e70-128">Кроме того, несмотря на то что вы можете использовать System Center Operations Manager 2012 или System Center Operations Manager 2007 R2, вы не сможете запускать два приложения одновременно — вы можете выбрать одно из них или другое.</span><span class="sxs-lookup"><span data-stu-id="d4e70-128">Also, while you can use either System Center Operations Manager 2012 or System Center Operations Manager 2007 R2, you cannot run the two applications simultaneously—you must choose one or the other.</span></span> <span data-ttu-id="d4e70-129">Например, если вы используете System Center Operations Manager 2012, то все агенты System Center должны быть также запущены с помощью System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="d4e70-129">For example, if you are running System Center Operations Manager 2012 then all your System Center agents must also be running System Center Operations Manager 2012.</span></span> <span data-ttu-id="d4e70-130">У вас не может быть некоторых агентов, использующих System Center Operations Manager 2012, а другие агенты работают под управлением System Center Operations Manager 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4e70-130">You cannot have some agents running System Center Operations Manager 2012 and other agents running System Center Operations Manager 2007 R2.</span></span>

<span data-ttu-id="d4e70-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4e70-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

