---
title: 'Lync Server 2013: Просмотр отчетов из анализатора соответствия рекомендациям'
description: 'Lync Server 2013: Просмотр отчетов из анализатора соответствия рекомендациям.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing reports from Best Practices Analyzer
ms:assetid: 7217a47b-36b1-4923-81ea-df754cff29bb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg607690(v=OCS.15)
ms:contentKeyID: 48184465
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44e0f1ed8d48f5c8fb7e35187ecdda2778091407
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398929"
---
# <a name="viewing-reports-from-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="6088b-103">Просмотр отчетов в анализаторе соответствия рекомендациям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6088b-103">Viewing reports from Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6088b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6088b-104">

<span> </span></span></span>

<span data-ttu-id="6088b-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="6088b-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="6088b-106">При использовании анализатора соответствия рекомендациям для проверки среды укажите имя для проверки.</span><span class="sxs-lookup"><span data-stu-id="6088b-106">When you use Best Practices Analyzer to scan your environment, you specify a name for the scan.</span></span> <span data-ttu-id="6088b-107">После того как анализатор соответствия рекомендациям завершит проверку, он сохранит результаты проверки в отчетах и сохранит их под именем проверки.</span><span class="sxs-lookup"><span data-stu-id="6088b-107">After Best Practices Analyzer completes a scan, it stores the scan results in reports and saves them under the name of the scan.</span></span> <span data-ttu-id="6088b-108">После завершения сканирования вы можете просмотреть отчеты, созданные для этой проверки, щелкнув **Просмотреть отчет по этим рекомендациям** на странице Проверка **завершенных** проверок.</span><span class="sxs-lookup"><span data-stu-id="6088b-108">Upon completion of the scan, you can view the reports generated for that scan by clicking **View a report of this Best Practices scan** directly from the **Scanning Completed** page.</span></span> <span data-ttu-id="6088b-109">Кроме того, вы можете просматривать отчеты из этой проверки или предыдущих просмотров позже.</span><span class="sxs-lookup"><span data-stu-id="6088b-109">You can also view the reports from that scan or previous scans at a later time.</span></span> <span data-ttu-id="6088b-110">Вы можете просматривать отчеты на локальном компьютере, на котором выполнялась проверка, импортировать результаты сканирования с другого компьютера или экспортировать результаты сканирования для просмотра отчетов на другом компьютере, на котором установлен анализатор соответствия рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="6088b-110">You can view reports on the local computer on which the scan was run, import scan results from another computer, or export scan results to view the reports on another computer on which Best Practices Analyzer is installed.</span></span>

<span data-ttu-id="6088b-111">Результаты проверки отображаются в отчетах следующих типов:</span><span class="sxs-lookup"><span data-stu-id="6088b-111">Scan results are presented in the following types of reports:</span></span>

  - <span data-ttu-id="6088b-112">Список отчетов</span><span class="sxs-lookup"><span data-stu-id="6088b-112">List reports</span></span>

  - <span data-ttu-id="6088b-113">Отчеты по дереву</span><span class="sxs-lookup"><span data-stu-id="6088b-113">Tree reports</span></span>

  - <span data-ttu-id="6088b-114">Другие отчеты</span><span class="sxs-lookup"><span data-stu-id="6088b-114">Other reports</span></span>

<span data-ttu-id="6088b-115">Эти отчеты включают ошибки, предупреждения и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="6088b-115">These reports include errors, warnings, and other information.</span></span> <span data-ttu-id="6088b-116">Подробные сведения о каждом из этих типов отчетов и проблем можно найти [в разделе сведения об отчетах, созданных анализатором соответствия рекомендациям в Lync Server 2013](lync-server-2013-understanding-reports-created-by-best-practices-analyzer.md).</span><span class="sxs-lookup"><span data-stu-id="6088b-116">For details about each of these types of reports and issues, see [Understanding reports created by Best Practices Analyzer in Lync Server 2013](lync-server-2013-understanding-reports-created-by-best-practices-analyzer.md).</span></span>

<span data-ttu-id="6088b-117">Для просмотра результатов сканирования, созданных анализатором соответствия рекомендациям, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6088b-117">Use the following procedure to view scan results previously generated by Best Practices Analyzer.</span></span>

<div>

## <a name="to-view-reports-from-a-previous-scan"></a><span data-ttu-id="6088b-118">Просмотр отчетов из предыдущей проверки</span><span class="sxs-lookup"><span data-stu-id="6088b-118">To view reports from a previous scan</span></span>

1.  <span data-ttu-id="6088b-119">Войдите на компьютер, на котором установлен анализатор соответствия рекомендациям, с помощью учетной записи, которая является членом локальной учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6088b-119">Log on to a computer on which Best Practices Analyzer is installed using an account that is a member of the local User account.</span></span>
    
    > [!NOTE]  
    > <span data-ttu-id="6088b-120">Вы можете просматривать результаты проверки с помощью учетной записи, которая входит в локальную группу администраторов, но вы не можете выполнить проверку, если у вас есть соответствующие права и разрешения.</span><span class="sxs-lookup"><span data-stu-id="6088b-120">You can view the results of a scan using an account that is a member of the local Administrators group, but you cannot run a scan unless you have appropriate user rights and permissions.</span></span> <span data-ttu-id="6088b-121">Подробные сведения можно найти <A href="lync-server-2013-group-memberships-and-user-rights-requirements-for-best-practices-analyzer.md">в разделе членство в группах и требования к правам пользователей для анализатора соответствия рекомендациям в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6088b-121">For details, see <A href="lync-server-2013-group-memberships-and-user-rights-requirements-for-best-practices-analyzer.md">Group memberships and user rights requirements for Best Practices Analyzer in Lync Server 2013</A>.</span></span>

2.  <span data-ttu-id="6088b-122">Нажмите кнопку **Пуск**, наведите указатель на пункт **все программы**, выберите **Microsoft Lync Server 2013**, а затем — **анализатор соответствия рекомендациям**.</span><span class="sxs-lookup"><span data-stu-id="6088b-122">Click **Start**, point to **All Programs**, click **Microsoft Lync Server 2013**, and then click **Best Practices Analyzer**.</span></span>

3.  <span data-ttu-id="6088b-123">На экране **приветствия** щелкните **выбрать результаты проверки для просмотра**.</span><span class="sxs-lookup"><span data-stu-id="6088b-123">On the **Welcome** screen, click **Select the scan results to view**.</span></span>

4.  <span data-ttu-id="6088b-124">На странице **выберите способ сканирования, который нужно просмотреть** , выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="6088b-124">On the **Select a Best Practices Scan to View** page, do one of the following:</span></span>
    
      - <span data-ttu-id="6088b-125">Чтобы просмотреть отчеты из списка локально сохраненных результатов сканирования, выберите имя проверки, а затем нажмите кнопку **Просмотр отчета об этом сканировании**.</span><span class="sxs-lookup"><span data-stu-id="6088b-125">To view reports from the list of locally stored scan results, click the name of scan, and then click **View a report of this scan**.</span></span>
        
        > [!NOTE]  
        > <span data-ttu-id="6088b-126">Анализатор соответствия рекомендациям создает список локальных файлов из папки &lt; systemDrive &gt; \\ Documents and Settings \\ &lt; user &gt; \Application Data\Microsoft\RtcBPA.</span><span class="sxs-lookup"><span data-stu-id="6088b-126">The Best Practices Analyzer creates the list of local files from the folder &lt;systemDrive&gt;\\Documents and Settings\\&lt;user&gt;\Application Data\Microsoft\RtcBPA.</span></span>
    
      - <span data-ttu-id="6088b-127">Чтобы просмотреть отчеты для результатов сканирования, которые хранятся в другом месте, нажмите кнопку **Импорт сканирования**, найдите файл, содержащий результаты проверки, и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="6088b-127">To view reports for results of a scan that are stored at another location, click **Import scan**, locate the file containing the scan results, and then click **Open**.</span></span>
        
        > [!NOTE]  
        > <span data-ttu-id="6088b-128">Если версия анализатора соответствия рекомендациям на этом компьютере не совпадает с версией, которая использовалась для сбора данных в импортированном файле, средство на компьютере может снова выполнить анализ файла после его импорта.</span><span class="sxs-lookup"><span data-stu-id="6088b-128">If the version of Best Practices Analyzer on this computer does not match the version that was used to collect the data in the imported file, the tool on your computer might analyze the file again, after it is imported.</span></span>

5.  <span data-ttu-id="6088b-129">На странице **отчета** советы и рекомендации выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="6088b-129">On the **View Best Practices Report** page, do one of the following:</span></span>
    
      - <span data-ttu-id="6088b-130">Чтобы просмотреть отчеты в списке, упорядоченном по серверному компоненту, щелкните **список отчетов**, а затем откройте вкладку **все проблемы** или вкладку **информационные элементы** .</span><span class="sxs-lookup"><span data-stu-id="6088b-130">To view reports in a list organized by server component, click **List Reports**, and then click either the **All Issues** tab or the **Informational Items** tab.</span></span>
    
      - <span data-ttu-id="6088b-131">Чтобы просмотреть отчеты в виде иерархического списка, упорядоченного по типам результатов, нажмите кнопку **отчеты по дереву**, а затем откройте вкладку **подробное представление** или **представление Сводка** .</span><span class="sxs-lookup"><span data-stu-id="6088b-131">To view reports as a hierarchical list organized by types of results, click **Tree Reports**, and then click either the **Detailed View** tab or the **Summary View** tab.</span></span>
    
      - <span data-ttu-id="6088b-132">Чтобы просмотреть другие отчеты, выберите пункт **другие отчеты**.</span><span class="sxs-lookup"><span data-stu-id="6088b-132">To view other reports, click **Other Reports**.</span></span>
    
    > [!NOTE]  
    > <span data-ttu-id="6088b-133">Подробные сведения об отчетах анализатора соответствия рекомендациям и выявленных проблемах можно найти <A href="lync-server-2013-viewing-and-working-with-reports-created-by-best-practices-analyzer.md">в разделе Просмотр и работа с отчетами, созданными анализатором соответствия рекомендациям в Lync server 2013</A> , а также <A href="lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md">анализ и устранение проблем, определенных анализатором соответствия рекомендациям в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6088b-133">For details about the Best Practices Analyzer reports and the issues that they identify, see <A href="lync-server-2013-viewing-and-working-with-reports-created-by-best-practices-analyzer.md">Viewing and working with reports created by Best Practices Analyzer in Lync Server 2013</A> and <A href="lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md">Analyzing and resolving issues identified by Best Practices Analyzer in Lync Server 2013</A>.</span></span>

</div>

</div>

</div>

</div>

</div>

