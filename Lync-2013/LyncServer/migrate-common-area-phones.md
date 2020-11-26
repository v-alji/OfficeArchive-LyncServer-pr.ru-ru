---
title: Миграция телефонов общего пользования
description: Перенесите общие Телефоны на телефонную сеть.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443827"
---
# <a name="migrate-common-area-phones"></a><span data-ttu-id="e50fc-103">Миграция телефонов общего пользования</span><span class="sxs-lookup"><span data-stu-id="e50fc-103">Migrate Common Area Phones</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e50fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e50fc-104">

<span> </span></span></span>

<span data-ttu-id="e50fc-105">_**Тема последнего изменения:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="e50fc-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="e50fc-106">Обычные телефоны — это IP-телефоны, которые чаще всего находятся в общей рабочей области или в общей области, например в зале ожидания, кухни или фабрики.</span><span class="sxs-lookup"><span data-stu-id="e50fc-106">Common Area Phones are IP phones that most often reside in a shared workspace or common area, like a lobby, kitchen, or factory floor.</span></span> <span data-ttu-id="e50fc-107">Для обеспечения функций UC для Lync Server не нужно подключаться к компьютеру с помощью обычных телефонов.</span><span class="sxs-lookup"><span data-stu-id="e50fc-107">Common Area Phones do not need to be connected to a computer to provide Lync Server UC functionality.</span></span> <span data-ttu-id="e50fc-108">После миграции развертывания Lync Server 2010 на Lync Server 2013 необходимо также перенести объекты контактов, связанные с устаревшим стандартным телефоном.</span><span class="sxs-lookup"><span data-stu-id="e50fc-108">After migrating an Lync Server 2010 deployment to Lync Server 2013, you must also migrate the contact objects associated with the legacy Common Area Phone.</span></span> <span data-ttu-id="e50fc-109">С помощью командной консоли Lync Server вы сначала получите все объекты контактов, связанные с Lync Server 2010 Common Area Phone, а затем переместите эти объекты в пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e50fc-109">Using Lync Server Management Shell you will first retrieve all contact objects associated with the Lync Server 2010 Common Area Phones, and then move those objects to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="e50fc-110">**Миграция телефонов общего пользования**</span><span class="sxs-lookup"><span data-stu-id="e50fc-110">**Migrate Common Area Phones**</span></span>

1.  <span data-ttu-id="e50fc-111">На сервере переднего плана Lync Server 2013 откройте консоль управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e50fc-111">From the Lync Server 2013 Front End server, open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="e50fc-112">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e50fc-112">From the command line, type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  <span data-ttu-id="e50fc-113">Чтобы убедиться в том, что все объекты контакта были перемещены в пул Lync Server 2013, в командной консоли Lync Server Management Shell введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e50fc-113">To verify all contact objects have been moved to the Lync Server 2013 pool, from the Lync Server Management Shell type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    <span data-ttu-id="e50fc-114">Убедитесь, что все объекты контакта теперь связаны с пулом Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e50fc-114">Verify all contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="e50fc-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e50fc-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

