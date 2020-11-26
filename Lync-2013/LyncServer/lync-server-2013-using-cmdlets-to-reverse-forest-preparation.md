---
title: 'Lync Server 2013: использование командлетов для отмены подготовки леса'
description: 'Lync Server 2013: использование командлетов для обратной подготовки леса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse forest preparation
ms:assetid: f48c7eb3-ccb0-48e6-ac79-ab7c7062b9d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413024(v=OCS.15)
ms:contentKeyID: 48185822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: acac87bdaeb7e730f93401fa62ea2678a713bb8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439641"
---
# <a name="using-cmdlets-to-reverse-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="ab742-103">Использование командлетов для отмены подготовки леса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab742-103">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab742-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab742-104">

<span> </span></span></span>

<span data-ttu-id="ab742-105">_**Тема последнего изменения:** 2013-06-19_</span><span class="sxs-lookup"><span data-stu-id="ab742-105">_**Topic Last Modified:** 2013-06-19_</span></span>

<span data-ttu-id="ab742-106">Используйте командлет **Disable-CsAdForest** для реверсирования этапа подготовки леса.</span><span class="sxs-lookup"><span data-stu-id="ab742-106">Use the **Disable-CsAdForest** cmdlet to reverse the forest preparation step.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="ab742-107">Если запустить командлет <STRONG>Disable-CsAdForest</STRONG> в среде, где также уже развернута Предыдущая версия Lync Server, будут также удалены глобальные параметры для предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="ab742-107">If you run the <STRONG>Disable-CsAdForest</STRONG> cmdlet in an environment where you also have a previous version of Lync Server deployed, the global settings for the previous version will also be deleted.</span></span>



</div>

<div>

## <a name="to-use-cmdlets-to-reverse-forest-preparation"></a><span data-ttu-id="ab742-108">Использование командлетов для обратной подготовки леса</span><span class="sxs-lookup"><span data-stu-id="ab742-108">To use cmdlets to reverse forest preparation</span></span>

1.  <span data-ttu-id="ab742-109">Войдите в систему на компьютере, который входит в состав домена, в качестве члена группы администраторов домена в корневом домене леса.</span><span class="sxs-lookup"><span data-stu-id="ab742-109">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="ab742-110">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="ab742-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ab742-111">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ab742-111">Run:</span></span>
    
        Disable-CsAdForest [-Force] [-GroupDomain <FQDN of the domain in which universal groups were created>]
    
    <span data-ttu-id="ab742-112">Например:</span><span class="sxs-lookup"><span data-stu-id="ab742-112">For example:</span></span>
    
        Disable-CsAdForest -Force -GroupDomain contoso.net
    
    <span data-ttu-id="ab742-113">Параметр Force указывает, требуется ли принудительное выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="ab742-113">The Force parameter specifies whether to force running the task.</span></span> <span data-ttu-id="ab742-114">Если этот параметр не указан, команда не будет выполняться, если даже один домен в лесу все еще подготовлен для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ab742-114">If this parameter is not present, the command will not run if even one domain in the forest is still prepared for Lync Server 2013.</span></span> <span data-ttu-id="ab742-115">Если указан параметр Force, действие будет продолжено независимо от состояния других доменов в лесу.</span><span class="sxs-lookup"><span data-stu-id="ab742-115">If the Force parameter is specified, the action will continue regardless of the state of other domains in the forest.</span></span>
    
    <span data-ttu-id="ab742-116">Если параметр GroupDomain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="ab742-116">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ab742-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ab742-117">See Also</span></span>


[<span data-ttu-id="ab742-118">Проведение подготовки леса для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab742-118">Running forest preparation for Lync Server 2013</span></span>](lync-server-2013-running-forest-preparation.md)  


[<span data-ttu-id="ab742-119">Подготовка леса для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab742-119">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="ab742-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab742-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

