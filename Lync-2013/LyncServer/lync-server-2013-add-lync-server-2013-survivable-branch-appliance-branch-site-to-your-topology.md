---
title: Добавление в топологию сайта филиала устройства для обеспечения связи в филиалах Lync Server 2013
description: Добавьте в топологию сайт Lync Server 2013, который можно передать на филиале устройства.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add Lync Server 2013 Survivable Branch Appliance branch site to your topology
ms:assetid: d3142a37-4606-456d-8ea9-6cc0e51e55f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721896(v=OCS.15)
ms:contentKeyID: 49733830
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b50c03dd53c7637fcf0914db290b3e452b64b83
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439312"
---
# <a name="add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology"></a><span data-ttu-id="0552c-103">Добавление в топологию сайта филиала устройства для обеспечения связи в филиалах Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0552c-103">Add Lync Server 2013 Survivable Branch Appliance branch site to your topology</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0552c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0552c-104">

<span> </span></span></span>

<span data-ttu-id="0552c-105">_**Тема последнего изменения:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="0552c-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="0552c-106">Microsoft Lync Server 2013 (SBA) не может быть связан с пулом переднего плана Microsoft Lync Server 2010 в качестве регистратора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0552c-106">Microsoft Lync Server 2013 Survivable Branch Appliances (SBA) cannot be associated to a Microsoft Lync Server 2010 Front End pool as a backup Registrar.</span></span> <span data-ttu-id="0552c-107">SBA должен быть связан с пулом внешних интерфейсов Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0552c-107">The SBA must be associated with a Microsoft Lync Server 2013 Front End pool.</span></span> <span data-ttu-id="0552c-108">Эти действия предполагают наличие Microsoft Lync Server 2013 SBA.</span><span class="sxs-lookup"><span data-stu-id="0552c-108">These steps assume a Microsoft Lync Server 2013 SBA.</span></span> <span data-ttu-id="0552c-109">Выполните эту процедуру на центральном веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="0552c-109">Perform this procedure at the central site.</span></span>

<div>

## <a name="to-add-branch-sites-with-microsoft-lync-server-2013-sba-to-your-topology"></a><span data-ttu-id="0552c-110">Добавление сайтов филиалов с Microsoft Lync Server 2013 SBA в топологию</span><span class="sxs-lookup"><span data-stu-id="0552c-110">To add branch sites with Microsoft Lync Server 2013 SBA to your topology</span></span>

1.  <span data-ttu-id="0552c-111">Запустить построитель топологии: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="0552c-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="0552c-112">В дереве консоли разверните узел центрального сайта, разверните узел **сайты филиалов** и выберите пункт **создать сайт филиала**.</span><span class="sxs-lookup"><span data-stu-id="0552c-112">In the console tree, expand the central site, expand **Branch Sites**, and then click **New Branch Site**.</span></span>

3.  <span data-ttu-id="0552c-113">В диалоговом окне **Определение нового сайта ветви** щелкните **имя** и введите имя для нового сайта ветви.</span><span class="sxs-lookup"><span data-stu-id="0552c-113">In the **Define New Branch Site** dialog box, click **Name**, and then type a name for the new branch site.</span></span>

4.  <span data-ttu-id="0552c-114">Необязательно Нажмите кнопку **Описание** и введите понятное описание сайта филиала.</span><span class="sxs-lookup"><span data-stu-id="0552c-114">(Optional) Click **Description**, and then type a meaningful description for the branch site.</span></span>

5.  <span data-ttu-id="0552c-115">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0552c-115">Click **Next**.</span></span>

6.  <span data-ttu-id="0552c-116">Необязательно В диалоговом окне **Определение нового сайта ветви** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="0552c-116">(Optional) In the next **Define New Branch Site** dialog box, do any of the following:</span></span>
    
      - <span data-ttu-id="0552c-117">Щелкните **город** и введите имя города, в котором находится сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="0552c-117">Click **City**, and then type the name of the city in which the branch site is located.</span></span>
    
      - <span data-ttu-id="0552c-118">Щелкните область или **регион**, а затем введите имя состояния или региона, в котором находится сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="0552c-118">Click **State/Region**, and then type the name of the state or region in which the branch site is located.</span></span>
    
      - <span data-ttu-id="0552c-119">Щелкните **код страны**, а затем введите четырехзначный код звонка для страны или региона, в котором расположен сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="0552c-119">Click **Country Code**, and then type the two-digit calling code for the country/region in which the branch site is located.</span></span>

7.  <span data-ttu-id="0552c-120">Нажмите кнопку **Далее**, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="0552c-120">Click **Next**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="0552c-121">Если вы используете работающее работающее устройство филиала или его временный сервер филиала на этом сайте, убедитесь, что установлен флажок **открыть новый бесперебойный мастер при закрытом окне мастера** .</span><span class="sxs-lookup"><span data-stu-id="0552c-121">If you are using a Survivable Branch Appliance or Survivable Branch Server at this site, be sure that the **Open the New Survivable Wizard when this wizard closes** check box is selected.</span></span>
    
      - <span data-ttu-id="0552c-122">Если вы не используете работающее работающее устройство филиала или бесперебойную подразделение сервера на этом сайте, снимите флажок **открыть новый бесперебойный мастер, когда этот мастер закроется** .</span><span class="sxs-lookup"><span data-stu-id="0552c-122">If you are not using a Survivable Branch Appliance or Survivable Branch Server at this site, clear the **Open the New Survivable Wizard when this wizard closes** check box.</span></span>
    
      - <span data-ttu-id="0552c-123">Нажмите кнопку **Готово**, а затем следуйте указаниям в открывшемся мастере.</span><span class="sxs-lookup"><span data-stu-id="0552c-123">Click **Finish**, and then follow the directions in the wizard that opens.</span></span> <span data-ttu-id="0552c-124">Сведения об элементах мастера можно найти [в разделе Определение работающего устройства филиала или сервера в Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="0552c-124">For information about wizard items, see [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span></span>

8.  <span data-ttu-id="0552c-125">Повторите описанные выше действия для всех сайтов филиалов, которые нужно добавить в топологию.</span><span class="sxs-lookup"><span data-stu-id="0552c-125">Repeat the previous steps for each branch site that you want to add to the topology.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0552c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0552c-126">See Also</span></span>


[<span data-ttu-id="0552c-127">Определение устройства или сервера для обеспечения связи в филиалах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0552c-127">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)  
[<span data-ttu-id="0552c-128">Определение шлюза ТСОП для сайта филиала в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0552c-128">Define a PSTN gateway for a branch site in Lync Server 2013</span></span>](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md)  
[<span data-ttu-id="0552c-129">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0552c-129">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="0552c-130">Настройка магистрали без обхода мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0552c-130">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  
  

<span data-ttu-id="0552c-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0552c-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

