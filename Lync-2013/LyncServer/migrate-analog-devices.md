---
title: Перенос аналоговых устройств
description: Перенесите аналоговые устройства.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63f7f92142fb6a3ced37cded1a223038ec1876d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443834"
---
# <a name="migrate-analog-devices"></a><span data-ttu-id="eafbf-103">Перенос аналоговых устройств</span><span class="sxs-lookup"><span data-stu-id="eafbf-103">Migrate analog devices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eafbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eafbf-104">

<span> </span></span></span>

<span data-ttu-id="eafbf-105">_**Тема последнего изменения:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="eafbf-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="eafbf-106">Lync Server обеспечивает поддержку аналоговых устройств.</span><span class="sxs-lookup"><span data-stu-id="eafbf-106">Lync Server provides support for analog devices.</span></span> <span data-ttu-id="eafbf-107">В частности, поддерживаются аналоговые устройства аналогового и аналогового факсимильного аппарата.</span><span class="sxs-lookup"><span data-stu-id="eafbf-107">Specifically, the supported analog devices are analog audio phones and analog fax machines.</span></span> <span data-ttu-id="eafbf-108">Вы можете настроить полные шлюзы для поддержки использования аналоговых устройств в среде Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eafbf-108">You can configure the qualified gateways to support the use of analog devices in your Lync Server environment.</span></span> <span data-ttu-id="eafbf-109">После перехода с Lync Server 2010 на Lync Server 2013 необходимо также перенести объекты контактов, связанные с аналоговыми устройствами.</span><span class="sxs-lookup"><span data-stu-id="eafbf-109">After you migrate from Lync Server 2010 to Lync Server 2013, you must also migrate the contact objects associated with the analog devices.</span></span> <span data-ttu-id="eafbf-110">Используйте командную консоль Lync Server Management Shell, чтобы сначала получить все объекты контактов, связанные с аналоговыми устройствами Lync Server 2010, а затем переместить эти объекты в пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eafbf-110">Use Lync Server Management Shell to first retrieve all contact objects associated with the Lync Server 2010 analog devices, and then move those objects to the Lync Server 2013 pool.</span></span>

<div>

## <a name="to-migrate-analog-devices"></a><span data-ttu-id="eafbf-111">Миграция аналоговых устройств</span><span class="sxs-lookup"><span data-stu-id="eafbf-111">To migrate analog devices</span></span>

1.  <span data-ttu-id="eafbf-112">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="eafbf-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="eafbf-113">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="eafbf-113">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  <span data-ttu-id="eafbf-114">Убедитесь, что все объекты контакта были перемещены в пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eafbf-114">Verify that all contact objects have been moved to the Lync Server 2013 pool.</span></span> <span data-ttu-id="eafbf-115">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="eafbf-115">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  <span data-ttu-id="eafbf-116">Убедитесь, что все объекты контакта теперь связаны с пулом Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eafbf-116">Verify that all the contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="eafbf-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eafbf-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

