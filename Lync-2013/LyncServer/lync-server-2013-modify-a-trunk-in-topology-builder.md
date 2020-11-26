---
title: 'Lync Server 2013: изменение магистрали в построителе топологии'
description: 'Lync Server 2013: изменение магистрали в построителе топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify a trunk in Topology Builder
ms:assetid: 81055a82-c6f8-47b2-9779-223b1d842f36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688110(v=OCS.15)
ms:contentKeyID: 49733709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f453997664dbe3048a7aa915732b4d95a932dd9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425544"
---
# <a name="modify-a-trunk-in-topology-builder-in-lync-server-2013"></a><span data-ttu-id="acbe7-103">Изменение магистрали в построителе топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="acbe7-103">Modify a trunk in Topology Builder in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="acbe7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="acbe7-104">

<span> </span></span></span>

<span data-ttu-id="acbe7-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="acbe7-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="acbe7-106">Выполните указанные ниже действия, чтобы изменить дополнительный IP-адрес и отказаться от использования идентификатора межсетевого связи.</span><span class="sxs-lookup"><span data-stu-id="acbe7-106">Follow these steps to modify the alternate media IP address and alternate bypass identifier of a trunk.</span></span>

<div>

## <a name="to-modify-the-alternate-media-ip-address-of-a-trunk"></a><span data-ttu-id="acbe7-107">Изменение альтернативного IP-адреса носителя для магистрали</span><span class="sxs-lookup"><span data-stu-id="acbe7-107">To Modify the Alternate Media IP Address of a Trunk</span></span>

1.  <span data-ttu-id="acbe7-108">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="acbe7-108">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="acbe7-109">Запустите командлет Set-CsPstnGateway и измените поле AlternateBypassId в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="acbe7-109">Run the Set-CsPstnGateway cmdlet and modify the AlternateBypassId field in the Lync Server Management Shell.</span></span>
    
        Set-CsPstnGateway -Identity "PstnGateway:<peer FQDN> -RepresentativeMediaIP <IP address>

</div>

<div>

## <a name="to-modify-the-alternate-bypassid-of-a-trunk"></a><span data-ttu-id="acbe7-110">Изменение альтернативных BypassID на магистральной магистрали</span><span class="sxs-lookup"><span data-stu-id="acbe7-110">To Modify the Alternate BypassID of a Trunk</span></span>

1.  <span data-ttu-id="acbe7-111">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="acbe7-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="acbe7-112">Запустите командлет Set-CsPstnGateway и измените поле AlternateBypassId в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="acbe7-112">Run the Set-CsPstnGateway cmdlet and modify the AlternateBypassId field in the Lync Server Management Shell.</span></span>
    
        Set-CsPstnGateway -Identity "PstnGateway:<peer FQDN> -AlternateBypassID <identifier>

<span data-ttu-id="acbe7-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="acbe7-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

