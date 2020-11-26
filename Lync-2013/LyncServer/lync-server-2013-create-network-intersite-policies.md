---
title: 'Lync Server 2013: создание политик межсайтовой сети'
description: 'Lync Server 2013: создание политик межсетевого соединения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create network intersite policies
ms:assetid: b0714aae-55dc-4587-b718-34a03f596b22
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412844(v=OCS.15)
ms:contentKeyID: 48185148
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9666efcb9c6da459a8e50eeae66cd1a513b46f65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431941"
---
# <a name="create-network-intersite-policies-in-lync-server-2013"></a><span data-ttu-id="a8c8b-103">Создание политик межсайтовой сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8c8b-103">Create network intersite policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8c8b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8c8b-104">

<span> </span></span></span>

<span data-ttu-id="a8c8b-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="a8c8b-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="a8c8b-106">*Политика межсетевое* соединение определяет ограничения пропускной способности между сайтами, которые имеют прямые WAN-ссылки между ними.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-106">A *network intersite policy* defines bandwidth limitations between sites that have direct WAN links between them.</span></span>

<span data-ttu-id="a8c8b-107">Дополнительные сведения можно найти в документации по оболочке управления Lync Server для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a8c8b-107">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="a8c8b-108">New-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a8c8b-108">New-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="a8c8b-109">Get-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a8c8b-109">Get-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="a8c8b-110">Set-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a8c8b-110">Set-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="a8c8b-111">Remove-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a8c8b-111">Remove-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a8c8b-112">Политика межсетевого сайта требуется <EM>только</EM> в том случае, если имеется прямая перекрестная связь между двумя сетевыми сайтами.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-112">A network intersite policy is required <EM>only</EM> if there is a direct cross link between two network sites.</span></span>



</div>

<span data-ttu-id="a8c8b-113">В примере в Северной Америке для топологии есть прямая связь между сайтами Reno и Альбукерке.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-113">In the example topology North America region, there is a direct link between the Reno and Albuquerque sites.</span></span> <span data-ttu-id="a8c8b-114">Для этих двух сайтов требуется межсайтовая политика, которая применяет соответствующий профиль политики пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-114">These two sites require an intersite policy that applies an appropriate bandwidth policy profile.</span></span> <span data-ttu-id="a8c8b-115">В следующем примере используется \_ профиль ссылки 20Mb.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-115">The following example applies the 20Mb\_Link profile.</span></span>

<div>

## <a name="to-create-a-network-intersite-policy"></a><span data-ttu-id="a8c8b-116">Создание политики межсетевого соединения</span><span class="sxs-lookup"><span data-stu-id="a8c8b-116">To create a network intersite policy</span></span>

1.  <span data-ttu-id="a8c8b-117">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a8c8b-118">Запустите командлет New-CsNetworkInterSitePolicy, чтобы создать политики межсетевого сайта и применить соответствующий профиль политики пропускной способности для двух сайтов с прямой перекрестной связью.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-118">Run the New-CsNetworkInterSitePolicy cmdlet to create network intersite policies and apply an appropriate bandwidth policy profile for two sites that have a direct cross link.</span></span> <span data-ttu-id="a8c8b-119">Например, выполните командлет:</span><span class="sxs-lookup"><span data-stu-id="a8c8b-119">For example, run:</span></span>
    
        New-CsNetworkInterSitePolicy -InterNetworkSitePolicyID Reno_Albuquerque -NetworkSiteID1 Reno -NetworkSiteID2 Albuquerque -BWPolicyProfileID 20Mb_Link

3.  <span data-ttu-id="a8c8b-120">При необходимости повторите шаг 2, чтобы создать политики межсетевого сайта для всех пар сетевых сайтов, имеющих прямую перекрестную ссылку.</span><span class="sxs-lookup"><span data-stu-id="a8c8b-120">Repeat step 2 as needed to create network intersite policies for all network sites pairs that have a direct cross link.</span></span>

<span data-ttu-id="a8c8b-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8c8b-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

