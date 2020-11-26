---
title: Сброс контроля допуска звонков
description: Сброс управления допуском звонков.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4539cda453de6249be3a9b9b61521ecf478cb70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443624"
---
# <a name="reset-call-admission-control"></a><span data-ttu-id="1680d-103">Сброс контроля допуска звонков</span><span class="sxs-lookup"><span data-stu-id="1680d-103">Reset call admission control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1680d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1680d-104">

<span> </span></span></span>

<span data-ttu-id="1680d-105">_**Тема последнего изменения:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="1680d-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="1680d-106">Если в пуле внешних интерфейсов Lync Server 2010 (CAC) размещен элемент управления допускной передачей, необходимо переместить сервер CAC на пул Lync Server 2013, прежде чем можно будет удалить пул внешних интерфейсов Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="1680d-106">If a Lync Server 2010 Front End pool is hosting call admission control (CAC), you must move CAC hosting to a Lync Server 2013 pool before you can remove the Lync Server 2010 Front End pool.</span></span>

<div>

## <a name="to-reset-cac"></a><span data-ttu-id="1680d-107">Чтобы сбросить параметры CAC</span><span class="sxs-lookup"><span data-stu-id="1680d-107">To reset CAC</span></span>

1.  <span data-ttu-id="1680d-108">Открытие построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="1680d-108">Open Topology Builder.</span></span>

2.  <span data-ttu-id="1680d-109">Щелкните правой кнопкой мыши узел сайта и выберите команду **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="1680d-109">Right-click the site node, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="1680d-110">Убедитесь, что в разделе **параметр управления** допуском звонков установлен флажок **включить управление допуском звонков** .</span><span class="sxs-lookup"><span data-stu-id="1680d-110">Under **Call Admission Control setting**, make sure **Enable Call Admission Control** is selected.</span></span>

4.  <span data-ttu-id="1680d-111">В разделе **пул переднего плана, чтобы запустить управление допуском звонков (CAC)**, выберите пул Lync Server 2013, который будет размещаться в CAC, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1680d-111">Under **Front End pool to run call admission control (CAC)**, select the Lync Server 2013 pool that is to host CAC, and then click **OK**.</span></span>

5.  <span data-ttu-id="1680d-112">Опубликуйте топологию.</span><span class="sxs-lookup"><span data-stu-id="1680d-112">Publish the topology.</span></span>

<span data-ttu-id="1680d-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1680d-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

