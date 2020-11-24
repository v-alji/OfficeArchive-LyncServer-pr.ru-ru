---
title: Настройка доверенных серверов приложений
description: Настройка доверенных серверов приложений.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure trusted application servers
ms:assetid: 20c3815f-3048-4940-8c0f-cdfcd0801d5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204735(v=OCS.15)
ms:contentKeyID: 48183592
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39f439ea3e5996e0a3464540069024b70c415e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398860"
---
# <a name="configure-trusted-application-servers"></a><span data-ttu-id="aedb8-103">Настройка доверенных серверов приложений</span><span class="sxs-lookup"><span data-stu-id="aedb8-103">Configure trusted application servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aedb8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aedb8-104">

<span> </span></span></span>

<span data-ttu-id="aedb8-105">_**Тема последнего изменения:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="aedb8-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="aedb8-106">В смешанной среде, если вы создаете новый доверенный сервер приложений, необходимо задать пул следующего прыжка в качестве пула Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aedb8-106">In a mixed environment, if you create a new trusted application server, you must set the next hop pool to be a Lync Server 2013 pool.</span></span> <span data-ttu-id="aedb8-107">В смешанной среде в раскрывающемся списке отображаются стандартный пул Lync Server 2010 и пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aedb8-107">In a mixed environment, both the legacy Lync Server 2010 pool and the Lync Server 2013 pool appear in the drop down list.</span></span> <span data-ttu-id="aedb8-108">Выбор устаревшего пула не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aedb8-108">Selecting the legacy pool is not supported.</span></span>

<span data-ttu-id="aedb8-109">**Выбор пункта Lync Server 2013 в качестве следующего прыжка при создании надежного сервера приложений**</span><span class="sxs-lookup"><span data-stu-id="aedb8-109">**Select Lync Server 2013 as next hop when creating a Trusted application server**</span></span>

1.  <span data-ttu-id="aedb8-110">Открытие построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="aedb8-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="aedb8-111">В левой области щелкните правой кнопкой мыши **Доверенные серверы приложений** и выберите команду **создать доверенный пул приложений**.</span><span class="sxs-lookup"><span data-stu-id="aedb8-111">In the left pane, right click **Trusted application servers** and click **New Trusted Application Pool**.</span></span>

3.  <span data-ttu-id="aedb8-112">Введите **полное доменное имя пула** для доверенного пула приложений и укажите, будет ли он одним или несколькими серверами.</span><span class="sxs-lookup"><span data-stu-id="aedb8-112">Enter the **Pool FQDN** of the trusted application pool and select whether it will be a single-server or multiple-server.</span></span>

4.  <span data-ttu-id="aedb8-113">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aedb8-113">Click **Next**.</span></span>

5.  <span data-ttu-id="aedb8-114">На странице **Выбор следующего прыжка** в списке выберите пул внешних интерфейсов Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aedb8-114">On the **Select the next hop** page, from the list, select the Lync Server 2013 Front End pool.</span></span>

6.  <span data-ttu-id="aedb8-115">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="aedb8-115">Click **Finish**.</span></span>

7.  <span data-ttu-id="aedb8-116">Выберите верхний узел **Lync Server** , а затем в меню **действия** выберите команду **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="aedb8-116">Select the top node **Lync Server** and from the **Action** menu, select **Publish**.</span></span>
    
    <span data-ttu-id="aedb8-117">Убедитесь, что **доверенный пул приложений** успешно создан и связан с правильным пулом переднего плана.</span><span class="sxs-lookup"><span data-stu-id="aedb8-117">Verify the **Trusted Application Pool** has been created successfully and is associated with the correct Front End pool.</span></span>

<span data-ttu-id="aedb8-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aedb8-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

