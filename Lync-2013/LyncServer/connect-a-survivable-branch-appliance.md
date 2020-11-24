---
title: Подключение Survivable Branch Appliance
description: Подключите устройство с бесперебойной подразделением.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect a Survivable Branch Appliance
ms:assetid: fe3167e2-d1b1-4cd4-bf30-262e0e7d14e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721948(v=OCS.15)
ms:contentKeyID: 49733886
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5bbf9e1a4189d3c80d6dec449adf68b82cd3691
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398347"
---
# <a name="connect-a-survivable-branch-appliance"></a><span data-ttu-id="bf401-103">Подключение Survivable Branch Appliance</span><span class="sxs-lookup"><span data-stu-id="bf401-103">Connect a Survivable Branch Appliance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf401-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf401-104">

<span> </span></span></span>

<span data-ttu-id="bf401-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="bf401-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="bf401-106">Каждое работающее устройство филиала (SBA) связано с пулом переднего плана, который выступает в качестве регистратора резервных копий для SBA.</span><span class="sxs-lookup"><span data-stu-id="bf401-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool which serves as a backup registrar for the SBA.</span></span> <span data-ttu-id="bf401-107">Когда пул переднего плана переносится на Lync Server 2013, SBA должен быть сопоставлен с пулом внешних интерфейсов Lync Server 2010 при обновлении пула, после того как пул будет перенесен на Lync Server 2013, SBA может быть повторно связан с обновленным пулом переднего плана.</span><span class="sxs-lookup"><span data-stu-id="bf401-107">When the Front End pool is migrated to Lync Server 2013, the SBA must be disassociated from the Lync Server 2010 Front End pool while the pool is upgraded, Once the pool has been migrated to Lync Server 2013, the SBA can be re-associated with the upgraded Front End pool.</span></span> <span data-ttu-id="bf401-108">Это связано с тем, что удаление SBA из старой топологии сервера Lync 2010 в построителе топологии и добавление SBA в топологию Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bf401-108">This involves deleting the SBA from the legacy Lync Server 2010 topology in Topology Builder and then adding the SBA to the Lync Server 2013 topology.</span></span> <span data-ttu-id="bf401-109">Пользователи, расположенные на устаревшем Lync Server 2010 SBA, должны сначала переместиться в другой пул переднего плана, прежде чем удалять SBA из топологии.</span><span class="sxs-lookup"><span data-stu-id="bf401-109">Users homed on the legacy Lync Server 2010 SBA must first be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="bf401-110">После того как SBA добавляется в топологию Lync Server 2013, эти пользователи затем могут быть возвращены в SBA.</span><span class="sxs-lookup"><span data-stu-id="bf401-110">Once the SBA is added to the Lync Server 2013 topology, those users can then be moved back to the SBA.</span></span> <span data-ttu-id="bf401-111">Эти действия описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="bf401-111">These steps are summarized below:</span></span>

1.  <span data-ttu-id="bf401-112">Переместить пользователей филиалов, расположенные на устаревшем SBA Lync Server 2010, в другой пул переднего плана.</span><span class="sxs-lookup"><span data-stu-id="bf401-112">Move branch users homed on the legacy SBA Lync Server 2010 to another Front End pool.</span></span>

2.  <span data-ttu-id="bf401-113">Удалите SBA из устаревшей топологии Lync Server 2010, чтобы отключить существующий пул переднего плана в качестве регистратора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="bf401-113">Remove SBA from the legacy Lync Server 2010 topology to disconnect the existing Front End pool as a backup registrar.</span></span>

3.  <span data-ttu-id="bf401-114">Добавьте SBA в топологию Lync Server 2013 и настройте этот новый пул переднего плана в качестве регистратора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="bf401-114">Add SBA to the Lync Server 2013 topology and configure this new Front End pool as the backup registrar.</span></span>

4.  <span data-ttu-id="bf401-115">Переместите пользователей филиалов на новый сервер Lync Server 2013 SBA.</span><span class="sxs-lookup"><span data-stu-id="bf401-115">Move the branch users to the new Lync Server 2013 SBA.</span></span>

<span data-ttu-id="bf401-116">**Добавление сайта ответвления Lync Server 2010 SBA в топологию**</span><span class="sxs-lookup"><span data-stu-id="bf401-116">**Add Lync Server 2010 SBA Branch Site to Your Topology**</span></span>

1.  <span data-ttu-id="bf401-117">Открытие **построителя топологии**.</span><span class="sxs-lookup"><span data-stu-id="bf401-117">Open **Topology Builder**.</span></span>

2.  <span data-ttu-id="bf401-118">На левой панели щелкните правой кнопкой мыши **узлы филиалов** и выберите команду **создать сайт филиала**.</span><span class="sxs-lookup"><span data-stu-id="bf401-118">In the left pane right-click **Branch sites**, and then click **New Branch Site**.</span></span>

3.  <span data-ttu-id="bf401-119">В диалоговом окне **Определение нового сайта ветви** щелкните **имя** и введите имя сайта ветви.</span><span class="sxs-lookup"><span data-stu-id="bf401-119">In the **Define New Branch Site** dialog box, click **Name**, and then type the name of the branch site.</span></span>

4.  <span data-ttu-id="bf401-120">Необязательно Нажмите кнопку **Описание** и введите понятное описание сайта филиала.</span><span class="sxs-lookup"><span data-stu-id="bf401-120">(Optional) Click **Description**, and then type a meaningful description for the branch site.</span></span>

5.  <span data-ttu-id="bf401-121">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf401-121">Click **Next**.</span></span>

6.  <span data-ttu-id="bf401-122">Необязательно В диалоговом окне **Определение нового сайта ветви** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="bf401-122">(Optional) In the next **Define New Branch Site** dialog box, do any of the following:</span></span>
    
    1.  <span data-ttu-id="bf401-123">Щелкните **город** и введите имя города, в котором находится сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="bf401-123">Click **City**, and then type the name of the city in which the branch site is located.</span></span>
    
    2.  <span data-ttu-id="bf401-124">Щелкните область или **регион**, а затем введите имя состояния или региона, в котором находится сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="bf401-124">Click **State/Region**, and then type the name of the state or region in which the branch site is located.</span></span>
    
    3.  <span data-ttu-id="bf401-125">Щелкните **код страны**, а затем введите четырехзначный код звонка для страны или региона, в котором расположен сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="bf401-125">Click **Country Code**, and then type the two-digit calling code for the country/region in which the branch site is located.</span></span>

7.  <span data-ttu-id="bf401-126">Нажмите кнопку **Далее**, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="bf401-126">Click **Next**, and then do one of the following:</span></span>
    
    1.  <span data-ttu-id="bf401-127">Если вы используете устройство с бесперебойной подразделением Lync 2010 или сервер на этом сайте, не забудьте снять флажок **открывать новый бесперебойный мастер, когда мастер закроет этот** параметр.</span><span class="sxs-lookup"><span data-stu-id="bf401-127">If you are using a Lync 2010 Survivable Branch Appliance or Server at this site, be sure to uncheck the **Open the New Survivable Wizard when this wizard closes** option.</span></span> <span data-ttu-id="bf401-128">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bf401-128">Click **Finish**.</span></span>

8.  <span data-ttu-id="bf401-129">Чтобы сопоставить старый сервер Lync Server 2010 SBA с пулом внешних интерфейсов Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="bf401-129">To associate the legacy Lync Server 2010 SBA to the Lync Server 2013 Front End pool:</span></span>
    
    1.  <span data-ttu-id="bf401-130">Разверните созданный сайт ветви.</span><span class="sxs-lookup"><span data-stu-id="bf401-130">Expand the branch site that has been created.</span></span>
    
    2.  <span data-ttu-id="bf401-131">Щелкните правой кнопкой мыши на **Lync Server 2010** и выберите команду **создать**.</span><span class="sxs-lookup"><span data-stu-id="bf401-131">Right click on **Lync Server 2010** and then click **New**.</span></span>
    
    3.  <span data-ttu-id="bf401-132">Щелкните **устройство для бесперебойной ветви..** .</span><span class="sxs-lookup"><span data-stu-id="bf401-132">Click **Survivable Branch Appliance…**</span></span>

9.  <span data-ttu-id="bf401-133">Следуйте указаниям в открывшемся мастере.</span><span class="sxs-lookup"><span data-stu-id="bf401-133">Follow the directions in the wizard that opens.</span></span> <span data-ttu-id="bf401-134">Сведения об элементах мастера можно найти [в разделе Определение работающего устройства филиала или сервера в Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="bf401-134">For information about wizard items, see [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bf401-135">Бесперебойно работающее устройство филиалов Lync Server 2010 можно связать только с хранилищем мониторинга Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="bf401-135">A Lync Server 2010 Survivable Branch Appliance can only be associated with a Lync Server 2010 Monitoring Store.</span></span>

    
    </div>

10. <span data-ttu-id="bf401-136">Если вы не используете бесперебойно работающее устройство или сервер филиала на этом сайте, снимите флажок **открыть новый бесперебойный мастер, когда мастер закроется** , и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bf401-136">If you are not using a Survivable Branch Appliance or Server at this site, clear the **Open the New Survivable Wizard when this wizard closes** check box, and then click **Finish**.</span></span>

11. <span data-ttu-id="bf401-137">Повторите описанные выше действия для всех сайтов филиалов, которые нужно добавить в топологию.</span><span class="sxs-lookup"><span data-stu-id="bf401-137">Repeat the previous steps for each branch site you want to add to the topology.</span></span>

<span data-ttu-id="bf401-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf401-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

