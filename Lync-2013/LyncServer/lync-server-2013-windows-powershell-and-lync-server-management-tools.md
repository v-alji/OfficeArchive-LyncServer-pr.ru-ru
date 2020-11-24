---
title: 'Lync Server 2013: средства управления для Windows PowerShell и Lync Server 2013'
description: 'Lync Server 2013: средства управления Windows PowerShell и Lync Server Management Tools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows PowerShell and Lync Server 2013 management tools
ms:assetid: 6a285f7c-0ef5-4cab-9976-d03be276e35d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481130(v=OCS.15)
ms:contentKeyID: 59893869
ms.date: 07/20/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c8d63974ad05a041eb446182cbc7f9336044b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398902"
---
# <a name="windows-powershell-and-lync-server-2013-management-tools"></a><span data-ttu-id="12fcd-103">Средства управления для Windows PowerShell и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12fcd-103">Windows PowerShell and Lync Server 2013 management tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12fcd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12fcd-104">

<span> </span></span></span>

<span data-ttu-id="12fcd-105">_**Тема последнего изменения:** 2016-07-20_</span><span class="sxs-lookup"><span data-stu-id="12fcd-105">_**Topic Last Modified:** 2016-07-20_</span></span>

<span data-ttu-id="12fcd-106">В Microsoft Lync Server 2013 средства управления реализованы с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="12fcd-106">In Microsoft Lync Server 2013, management tools are implemented using Windows PowerShell.</span></span> <span data-ttu-id="12fcd-107">Windows PowerShell включает среду командной строки, команды, связанные с продуктом, и полный язык сценариев.</span><span class="sxs-lookup"><span data-stu-id="12fcd-107">Windows PowerShell includes a command-line environment, product-specific commands, and a full scripting language.</span></span> <span data-ttu-id="12fcd-108">Средства Lync Server 2013, реализованные с помощью Windows PowerShell, включают следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="12fcd-108">Lync Server 2013 tools that are implemented using Windows PowerShell include the following:</span></span>

  - <span data-ttu-id="12fcd-109">**Построитель топологии**.</span><span class="sxs-lookup"><span data-stu-id="12fcd-109">**Topology Builder**.</span></span> <span data-ttu-id="12fcd-110">С помощью Topology Builder вы можете создавать, изменять и публиковать плановую топологию, а также проверять топологию до начала установки сервера.</span><span class="sxs-lookup"><span data-stu-id="12fcd-110">You use Topology Builder to create, adjust, and publish your planned topology, and it validates your topology before you begin server installations.</span></span> <span data-ttu-id="12fcd-111">При установке Lync Server 2013 на отдельных серверах серверы считывают опубликованную топологию в процессе установки, и программа установки развертывает сервер в соответствии с топологией.</span><span class="sxs-lookup"><span data-stu-id="12fcd-111">When you install Lync Server 2013 on individual servers, the servers read the published topology as part of the installation process, and the installation program deploys the server as directed in the topology.</span></span> <span data-ttu-id="12fcd-112">После установки сведения о конфигурации автоматически реплицируются на все серверы.</span><span class="sxs-lookup"><span data-stu-id="12fcd-112">After setup, configuration information is automatically replicated to all servers.</span></span> <span data-ttu-id="12fcd-113">Компоненты можно добавлять в развертывание только с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="12fcd-113">Components can be added to your deployment only by using Topology Builder.</span></span>

  - <span data-ttu-id="12fcd-114">**Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="12fcd-114">**Lync Server Management Shell**.</span></span> <span data-ttu-id="12fcd-115">Вы можете использовать командную консоль Lync Server для управления развертыванием с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="12fcd-115">You can use Lync Server Management Shell for full command-line management of your deployment.</span></span>

  - <span data-ttu-id="12fcd-116">**Панель управления Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="12fcd-116">**Lync Server Control Panel**.</span></span> <span data-ttu-id="12fcd-117">Вы можете использовать пользовательский интерфейс панели управления Microsoft Lync Server 2013 для управления наиболее распространенными задачами в развертывании.</span><span class="sxs-lookup"><span data-stu-id="12fcd-117">You can use the Microsoft Lync Server 2013 Control Panel user interface to manage the most common tasks in your deployment.</span></span>

<span data-ttu-id="12fcd-118">Эти средства используют командлеты Windows PowerShell для управления развертыванием, в том числе с помощью командлетов для работы с конкретными продуктами 550.</span><span class="sxs-lookup"><span data-stu-id="12fcd-118">These tools use Windows PowerShell cmdlets for management of your deployment, including close to 550 product-specific cmdlets.</span></span> <span data-ttu-id="12fcd-119">Командлеты безопасности, включенные в Lync Server 2013, главным образом используются для управления проверкой подлинности, а также правами и разрешениями пользователей.</span><span class="sxs-lookup"><span data-stu-id="12fcd-119">The security cmdlets included in Lync Server 2013 are primarily used to manage authentication, and user rights and permissions.</span></span> <span data-ttu-id="12fcd-120">Широкий спектр командлетов доступен для управления проверкой подлинности, включая командлеты для проверки подлинности с помощью сертификатов и персональных идентификационных номеров (ПИН-кодов).</span><span class="sxs-lookup"><span data-stu-id="12fcd-120">A wide variety of cmdlets are available for managing authentication, including cmdlets for certificate and personal identification number (PIN) authentication.</span></span> <span data-ttu-id="12fcd-121">Кроме того, несколько командлетов позволяют использовать новый компонент управления доступом Role-Based (RBAC) для делегирования административного управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="12fcd-121">In addition, a number of cmdlets enable you to use the new Role-Based Access Control (RBAC) feature to delegate administrative control of Lync Server 2013.</span></span> <span data-ttu-id="12fcd-122">Дополнительные сведения о командлетах Lync Server можно найти в [командной консоли Lync server 2013](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="12fcd-122">For details about the Lync Server cmdlets, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

<span data-ttu-id="12fcd-123">Функции безопасности сценариев для Windows PowerShell специально разработаны для помощи в предотвращении некоторых связанных с написанием сценариев проблем безопасности старых топологий, включая сценарии VBScript.</span><span class="sxs-lookup"><span data-stu-id="12fcd-123">The script security features for Windows PowerShell are specifically designed to help prevent some of the scripting-related security problems of older technologies, including Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="12fcd-124">Функции безопасности Windows PowerShell предназначены для создания среды, в которой пользователи не могут легко или непреднамеренно запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="12fcd-124">The Windows PowerShell security features are intended to create an environment in which users cannot easily or unknowingly run scripts.</span></span> <span data-ttu-id="12fcd-125">По умолчанию функции безопасности Windows PowerShell включены.</span><span class="sxs-lookup"><span data-stu-id="12fcd-125">By default, Windows PowerShell security features are enabled.</span></span> <span data-ttu-id="12fcd-126">Состояние этих функций можно изменять в соответствии с требованиями написания сценариев и различными целями безопасности.</span><span class="sxs-lookup"><span data-stu-id="12fcd-126">You can modify the state of those features to accommodate your scripting needs and a variety of security goals.</span></span> <span data-ttu-id="12fcd-127">Это не означает, что оболочка делает запуск сценариев невозможным для пользователей.</span><span class="sxs-lookup"><span data-stu-id="12fcd-127">This is not to say that the shell makes it impossible for users to run scripts.</span></span> <span data-ttu-id="12fcd-128">Напротив, оболочка по умолчанию затрудняет для пользователей запуск сценариев без понимания того, что они делают.</span><span class="sxs-lookup"><span data-stu-id="12fcd-128">Rather, the shell makes it difficult—by default—for users to run scripts without realizing they are doing so.</span></span> <span data-ttu-id="12fcd-129">Дополнительные сведения можно найти в разделе Безопасность сценариев Windows PowerShell [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145) .</span><span class="sxs-lookup"><span data-stu-id="12fcd-129">For details, see Windows PowerShell Script Security at [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145).</span></span>

<span data-ttu-id="12fcd-130"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12fcd-130"></div>

<span> </span>

</div>

</div>

</span></span></div>

