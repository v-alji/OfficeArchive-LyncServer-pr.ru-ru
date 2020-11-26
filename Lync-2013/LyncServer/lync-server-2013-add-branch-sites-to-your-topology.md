---
title: 'Lync Server 2013: добавление сайтов филиалов в топологию'
description: 'Lync Server 2013: Добавление сайтов филиалов в топологию.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add branch sites to your topology
ms:assetid: b9c35fb0-0081-4aeb-8f95-ac2fcc6c3335
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412905(v=OCS.15)
ms:contentKeyID: 48185216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c7a12373c6a60a2902ee451d39c99f756e2b2f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439368"
---
# <a name="add-branch-sites-to-your-topology-in-lync-server-2013"></a><span data-ttu-id="99f7a-103">Добавление сайтов филиалов в топологию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99f7a-103">Add branch sites to your topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99f7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99f7a-104">

<span> </span></span></span>

<span data-ttu-id="99f7a-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="99f7a-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="99f7a-106">Сайты филиалов представляют физические офисы подразделений, которые подключены к основным офисам по ГЛОБАЛЬным каналам связи.</span><span class="sxs-lookup"><span data-stu-id="99f7a-106">Branch sites represent physical branch offices that are connected to your main offices over a WAN link.</span></span> <span data-ttu-id="99f7a-107">Чтобы добавить сайт филиалов в свою топологию Lync, выполните эту процедуру на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="99f7a-107">To add a branch site to your Lync topology, perform this procedure at the central site.</span></span>

<div>

## <a name="to-add-branch-sites-to-your-topology"></a><span data-ttu-id="99f7a-108">Добавление сайтов филиалов в топологию</span><span class="sxs-lookup"><span data-stu-id="99f7a-108">To add branch sites to your topology</span></span>

1.  <span data-ttu-id="99f7a-109">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server**, а затем — **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="99f7a-109">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="99f7a-110">В дереве консоли разверните узел центрального сайта, щелкните правой кнопкой мыши **узлы филиалов** и выберите команду **создать сайт ветви**.</span><span class="sxs-lookup"><span data-stu-id="99f7a-110">In the console tree, expand the central site, right-click **Branch Sites**, and then click **New Branch Site**.</span></span>

3.  <span data-ttu-id="99f7a-111">В диалоговом окне **Определение нового сайта ветви** щелкните **имя** и введите имя сайта ветви.</span><span class="sxs-lookup"><span data-stu-id="99f7a-111">In the **Define New Branch Site** dialog box, click **Name**, and then type the name of the branch site.</span></span>

4.  <span data-ttu-id="99f7a-112">Необязательно Нажмите кнопку **Описание** и введите понятное описание сайта филиала.</span><span class="sxs-lookup"><span data-stu-id="99f7a-112">(Optional) Click **Description**, and then type a meaningful description for the branch site.</span></span>

5.  <span data-ttu-id="99f7a-113">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="99f7a-113">Click **Next**.</span></span>

6.  <span data-ttu-id="99f7a-114">Необязательно В диалоговом окне **Определение нового сайта ветви** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="99f7a-114">(Optional) In the next **Define New Branch Site** dialog box, do any of the following:</span></span>
    
      - <span data-ttu-id="99f7a-115">Щелкните **город** и введите имя города, в котором находится сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="99f7a-115">Click **City**, and then type the name of the city in which the branch site is located.</span></span>
    
      - <span data-ttu-id="99f7a-116">Щелкните область или **регион**, а затем введите имя состояния или региона, в котором находится сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="99f7a-116">Click **State/Region**, and then type the name of the state or region in which the branch site is located.</span></span>
    
      - <span data-ttu-id="99f7a-117">Щелкните **код страны**, а затем введите четырехзначный код звонка для страны или региона, в котором расположен сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="99f7a-117">Click **Country Code**, and then type the two-digit calling code for the country/region in which the branch site is located.</span></span>

7.  <span data-ttu-id="99f7a-118">Нажмите кнопку **Далее**, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="99f7a-118">Click **Next**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="99f7a-119">Если вы используете работающее устройство филиала или сервер на этом сайте, убедитесь, что установлен флажок **открыть новый бесперебойный мастер, когда этот мастер закроется** , нажмите кнопку **Готово**, а затем следуйте указаниям в открывшемся мастере.</span><span class="sxs-lookup"><span data-stu-id="99f7a-119">If you are using a Survivable Branch Appliance or Server at this site, be sure that the **Open the New Survivable Wizard when this wizard closes** check box is selected, click **Finish**, and then follow the directions in the wizard that opens.</span></span> <span data-ttu-id="99f7a-120">Сведения об элементах мастера можно найти [в разделе Определение работающего устройства филиала или сервера в Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="99f7a-120">For information about wizard items, see [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span></span>
    
      - <span data-ttu-id="99f7a-121">Если вы не используете бесперебойно работающее устройство или сервер филиала на этом сайте, снимите флажок **открыть новый бесперебойный мастер, когда мастер закроется** , и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="99f7a-121">If you are not using a Survivable Branch Appliance or Server at this site, clear the **Open the New Survivable Wizard when this wizard closes** check box, and then click **Finish**.</span></span>

8.  <span data-ttu-id="99f7a-122">Повторите описанные выше действия для всех сайтов филиалов, которые нужно добавить в топологию.</span><span class="sxs-lookup"><span data-stu-id="99f7a-122">Repeat the previous steps for each branch site that you want to add to the topology.</span></span>

<span data-ttu-id="99f7a-123">**Следующий шаг:**</span><span class="sxs-lookup"><span data-stu-id="99f7a-123">**Next step:**</span></span>

<span data-ttu-id="99f7a-124">Для бесперебойно работающих устройств или серверов филиалов: определение работающего [устройства филиала или сервера в Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)</span><span class="sxs-lookup"><span data-stu-id="99f7a-124">For Survivable Branch Appliances or Servers: [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)</span></span>

<span data-ttu-id="99f7a-125">Для неустойчивой КОММУТИРУЕМой связи: [определение шлюза PSTN для сайта филиала в Lync server 2013](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md), [Настройка канала с помощью мультимедиа для обхода в Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md)или [Настройка канала без пропуска мультимедиа в Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md)</span><span class="sxs-lookup"><span data-stu-id="99f7a-125">For non-resilient PSTN connectivity: [Define a PSTN gateway for a branch site in Lync Server 2013](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md), [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md), or [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md)</span></span>

<span data-ttu-id="99f7a-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99f7a-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

