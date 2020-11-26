---
title: 'Lync Server 2013: Командная консоль Lync Server Management Shell'
description: 'Lync Server 2013: Командная консоль Lync Server Management Shell.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server Management Shell
ms:assetid: 674b523b-c0b7-4ed6-9e67-afa6e8ac7e12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398474(v=OCS.15)
ms:contentKeyID: 48184386
ms.date: 09/20/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45727c42899defcf20ce36e2a27a9268a52ecd71
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426267"
---
# <a name="lync-server-2013-management-shell"></a><span data-ttu-id="86bad-103">командная консоль Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86bad-103">Lync Server 2013 Management Shell</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86bad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86bad-104">

<span> </span></span></span>

<span data-ttu-id="86bad-105">_**Тема последнего изменения:** 2017-09-20_</span><span class="sxs-lookup"><span data-stu-id="86bad-105">_**Topic Last Modified:** 2017-09-20_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="86bad-106">Справочник по командлетам Skype для бизнеса перенесен на веб-сайт docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="86bad-106">Skype for Business cmdlet reference has moved to docs.microsoft.com.</span></span> <span data-ttu-id="86bad-107">По представленным ниже ссылкам вы можете перейти на новую страницу портала docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="86bad-107">Clicking on the links below will take you to the new docs.microsoft.com page.</span></span> <span data-ttu-id="86bad-108">Теперь весь контент предлагается с открытым исходным кодом и доступен в сообществе GitHub.</span><span class="sxs-lookup"><span data-stu-id="86bad-108">The content is now open sourced and available for community contributions through GitHub.</span></span> <span data-ttu-id="86bad-109">Хотите принять участие в работе с ним?</span><span class="sxs-lookup"><span data-stu-id="86bad-109">Interested in contributing?</span></span> <span data-ttu-id="86bad-110">Ознакомьтесь с ФАЙЛОМ README в репозитории здесь: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span><span class="sxs-lookup"><span data-stu-id="86bad-110">Check out the README in the repo here: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span></span>



</div>

<span data-ttu-id="86bad-111">Microsoft Lync Server 2010 представил обширный набор новых и улучшенных функций по сравнению с тем, что было доступно в Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="86bad-111">Microsoft Lync Server 2010 introduced a large set of new and improved features compared to what was available in Microsoft Office Communications Server 2007 R2.</span></span> <span data-ttu-id="86bad-112">Одним из улучшений является способ управления реализацией.</span><span class="sxs-lookup"><span data-stu-id="86bad-112">One improvement is the way in which you manage your implementation.</span></span> <span data-ttu-id="86bad-113">Например, новый пользовательский интерфейс, называемый панелью управления Lync Server, — это большая смена, с которой работают другие люди с помощью консоли управления (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="86bad-113">For example, there’s a new user interface, called the Lync Server Control Panel, which represents a big shift from what most people are used to with the Microsoft Management Console.</span></span> <span data-ttu-id="86bad-114">Другим серьезным улучшением управления является включение Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="86bad-114">The other major improvement to manageability is the inclusion of Windows PowerShell.</span></span>

<span data-ttu-id="86bad-115">Windows PowerShell позволяет управлять приложениями Майкрософт из командной строки.</span><span class="sxs-lookup"><span data-stu-id="86bad-115">Windows PowerShell allows you to manage Microsoft applications from the command line.</span></span> <span data-ttu-id="86bad-116">Она включает среду командной строки, команды для определенного продукта и полный язык сценариев.</span><span class="sxs-lookup"><span data-stu-id="86bad-116">It includes a command-line environment, product-specific commands, and a full scripting language.</span></span> <span data-ttu-id="86bad-117">Windows PowerShell впервые была представлена в качестве загружаемого выпуска для операционной системы Windows с опозданием в 2006 и была включена в интерфейс командной строки для управляемости сервера Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="86bad-117">Windows PowerShell was first introduced as a downloadable release for the Windows operating system late in 2006, and was incorporated as the command-line interface for manageability of Microsoft Exchange Server 2007.</span></span> <span data-ttu-id="86bad-118">С этого момента она продолжает расти, и она была включена в большинство серверных продуктов Майкрософт, последние из которых представляют собой Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86bad-118">From that point it continued to grow, and it has been incorporated into most of the Microsoft Server products, the most recent of these being Microsoft Lync Server 2013.</span></span> <span data-ttu-id="86bad-119">В Lync Server 2010 появились командлеты 550 для определенного продукта, которые можно использовать для управления всеми аспектами развертывания.</span><span class="sxs-lookup"><span data-stu-id="86bad-119">Lync Server 2010 introduced close to 550 product-specific cmdlets that you can use to manage every aspect of your deployment.</span></span>

<span data-ttu-id="86bad-120">В следующих разделах представлен список командлетов и их описание.</span><span class="sxs-lookup"><span data-stu-id="86bad-120">The following sections contain a list of cmdlets and their descriptions.</span></span> <span data-ttu-id="86bad-121">Эта информация также доступна напрямую из командной строки.</span><span class="sxs-lookup"><span data-stu-id="86bad-121">This information is also available directly from the command line.</span></span> <span data-ttu-id="86bad-122">Просто введите следующую команду в командной строке оболочки Lync Server Management Shell:</span><span class="sxs-lookup"><span data-stu-id="86bad-122">Simply type the following at the Lync Server Management Shell command prompt:</span></span>

    Get-Help <cmdlet name> -Full

<span data-ttu-id="86bad-123">Например, чтобы получить справку по командлету **New-CsVoicePolicy** из командной строки, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="86bad-123">For example, to retrieve help from the command prompt on the **New-CsVoicePolicy** cmdlet, type the following:</span></span>

    Get-Help New-CsVoicePolicy -Full

<span data-ttu-id="86bad-124">Что нужно знать о Windows PowerShell в Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="86bad-124">Things to know about Windows PowerShell in Lync Server 2013:</span></span>

  - <span data-ttu-id="86bad-125">Чтобы запустить командлеты Lync Server, откройте консоль управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="86bad-125">To run the Lync Server cmdlets, open the Lync Server Management Shell.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="86bad-126">Если вы открыли окно Windows PowerShell, а не консоль управления Lync Server, по умолчанию вы не сможете запускать командлеты Lync Server.</span><span class="sxs-lookup"><span data-stu-id="86bad-126">If you open a Windows PowerShell window rather than the Lync Server Management Shell, by default you will not be able to run the Lync Server cmdlets.</span></span> <span data-ttu-id="86bad-127">Чтобы выполнить командлеты Lync Server из Windows PowerShell, сначала введите следующую команду в командной строке Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="86bad-127">To run the Lync Server cmdlets from within Windows PowerShell, first type the following at the Windows PowerShell command prompt:</span></span><BR><span data-ttu-id="86bad-128">Import-Module Lync</span><span class="sxs-lookup"><span data-stu-id="86bad-128">Import-Module Lync</span></span>

    
    </div>

  - <span data-ttu-id="86bad-129">Оболочка Lync Server Management Shell автоматически устанавливается на каждый сервер переднего плана Lync Server Enterprise Edition или Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="86bad-129">Lync Server Management Shell is automatically installed on every Lync Server Enterprise Edition Front End Server or Standard Edition server.</span></span>

  - <span data-ttu-id="86bad-130">Новые и обновленные сведения, примеры сценариев и Справка по началу работы с Windows PowerShell и Microsoft Lync Server 2013 доступны в блоге Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=203150](https://go.microsoft.com/fwlink/p/?linkid=203150) .</span><span class="sxs-lookup"><span data-stu-id="86bad-130">New and updated information, sample scripts, and help for getting started and learning more about Windows PowerShell and Microsoft Lync Server 2013 cmdlets is available at the Lync Server Windows PowerShell Blog [https://go.microsoft.com/fwlink/p/?linkId=203150](https://go.microsoft.com/fwlink/p/?linkid=203150).</span></span>

<span data-ttu-id="86bad-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86bad-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

