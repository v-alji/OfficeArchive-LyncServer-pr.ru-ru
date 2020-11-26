---
title: 'Lync Server 2013: новые функции виртуализации'
description: 'Lync Server 2013: новые функции виртуализации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New virtualization features
ms:assetid: edeb2c41-765e-47b8-8a2b-7a7ce09de2ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721926(v=OCS.15)
ms:contentKeyID: 49733861
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac15b8592d158d84807ff9e665dd6da50b699059
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424984"
---
# <a name="new-virtualization-features-in-lync-server-2013"></a><span data-ttu-id="38915-103">Новые функции виртуализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="38915-103">New virtualization features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="38915-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="38915-104">

<span> </span></span></span>

<span data-ttu-id="38915-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="38915-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="38915-106">Lync Server 2013 поддерживает виртуализацию как на Windows Server 2012, так и в Windows Server 2012 R2, так и в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="38915-106">Lync Server 2013 supports virtualization on both Windows Server 2012, Windows Server 2012 R2, and Windows Server 2008 R2.</span></span> <span data-ttu-id="38915-107">Поддержка в Windows Server 2012 и Windows Server 2012 R2 включает в себя поддержку одной из корневых возможностей виртуализации ввода-вывода (SR-IOV).</span><span class="sxs-lookup"><span data-stu-id="38915-107">Support on Windows Server 2012 and Windows Server 2012 R2 includes support for the Single Root I/O Virtualization (SR-IOV) capabilities.</span></span> <span data-ttu-id="38915-108">С помощью SR-IOV виртуальная функция физического сетевого адаптера назначается непосредственно виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="38915-108">With SR-IOV, the virtual function of a physical network adapter is assigned directly to a virtual machine.</span></span> <span data-ttu-id="38915-109">Это повышает пропускную способность сети и сокращает время задержки сети, а также сокращает дополнительные ресурсы ЦП узла, необходимые для обработки сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="38915-109">This increases network throughput and reduces network latency while also reducing the host CPU overhead that is required for processing network traffic.</span></span> <span data-ttu-id="38915-110">Чтобы воспользоваться преимуществами SR-IOV, необходимо использовать сервер узла, на котором установлен BIOS, поддерживающий SR-IOV, а также сетевые адаптеры, поддерживающие SR-IOV.</span><span class="sxs-lookup"><span data-stu-id="38915-110">To take advantage of SR-IOV, you must use a host server which has BIOS which supports SR-IOV, as well as use network adapters that support SR-IOV.</span></span>

<span data-ttu-id="38915-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="38915-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

