---
title: 'Lync Server 2013: анализатор соответствия рекомендациям для Lync Server'
description: 'Lync Server 2013: анализатор соответствия рекомендациям для Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Best Practices Analyzer
ms:assetid: 3124be9d-ad21-4a70-9c21-d2fc1adb3386
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558584(v=OCS.15)
ms:contentKeyID: 48183768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22c162dc73ce92ada18ee98d6956b7ed3e5c07a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426286"
---
# <a name="lync-server-2013-best-practices-analyzer"></a><span data-ttu-id="e0f11-103">Анализатор соответствия рекомендациям Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f11-103">Lync Server 2013 Best Practices Analyzer</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0f11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0f11-104">

<span> </span></span></span>

<span data-ttu-id="e0f11-105">_**Тема последнего изменения:** 2012-06-13_</span><span class="sxs-lookup"><span data-stu-id="e0f11-105">_**Topic Last Modified:** 2012-06-13_</span></span>

<span data-ttu-id="e0f11-106">Lync Server 2013, анализатор соответствия рекомендациям — средство диагностики, которое собирает сведения о конфигурации из сред Lync Server 2013 и определяет, задана ли конфигурация в соответствии с рекомендациями Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e0f11-106">Lync Server 2013, Best Practices Analyzer is a diagnostic tool that gathers configuration information from Lync Server 2013 environments and determines whether the configuration is set according to Microsoft best practices.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e0f11-107">Lync Server 2013, анализатор соответствия рекомендациям проверяет и сообщает о проблемах только в компонентах Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0f11-107">Lync Server 2013, Best Practices Analyzer scans and reports issues only with Lync Server 2013 components.</span></span> <span data-ttu-id="e0f11-108">Если в развертывании есть компоненты Lync Server 2010 или Office Communications Server 2007 R2, используйте анализатор соответствия рекомендациям более ранней версии, чтобы проанализировать эти компоненты.</span><span class="sxs-lookup"><span data-stu-id="e0f11-108">If your deployment includes Lync Server 2010 or Office Communications Server 2007 R2 components, use the previous version of Best Practices Analyzer to analyze those components.</span></span> <span data-ttu-id="e0f11-109">Дополнительные сведения можно найти <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">в разделе Требования для анализатора соответствия рекомендациям в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e0f11-109">For details, see <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">Requirements for running Best Practices Analyzer in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e0f11-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="e0f11-110">In This Section</span></span>

  - [<span data-ttu-id="e0f11-111">Обзор анализатора соответствия рекомендациям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f11-111">Overview of Best Practices Analyzer in Lync Server 2013</span></span>](lync-server-2013-overview-of-best-practices-analyzer.md)

  - [<span data-ttu-id="e0f11-112">Подготовка и установка анализатора соответствия рекомендациям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f11-112">Preparing for and installing Best Practices Analyzer in Lync Server 2013</span></span>](lync-server-2013-preparing-for-and-installing-best-practices-analyzer.md)

  - [<span data-ttu-id="e0f11-113">Использование анализатора соответствия рекомендациям для выявления потенциальных проблем, возникающих при развертывании Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f11-113">Using Best Practices Analyzer to identify potential issues in your Lync Server 2013 deployment</span></span>](lync-server-2013-using-best-practices-analyzer-to-identify-potential-issues-in-your-deployment.md)

  - [<span data-ttu-id="e0f11-114">Использование результатов сканирования для анализа и устранения проблем, обнаруженных анализатором соответствия рекомендациям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f11-114">Using scan results to analyze and resolve issues reported by Best Practices Analyzer in Lync Server 2013</span></span>](lync-server-2013-using-scan-results-to-analyze-and-resolve-issues-reported-by-best-practices-analyzer.md)

<span data-ttu-id="e0f11-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0f11-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

