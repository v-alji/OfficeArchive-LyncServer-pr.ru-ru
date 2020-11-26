---
title: 'Lync Server 2013: Мониторинг сервера Lync с помощью System Center Operations Manager'
description: 'Lync Server 2013: Мониторинг сервера Lync с помощью System Center Operations Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Lync 2013 with SCOM
ms:assetid: a74bde92-97ff-4d90-acb9-7a70272f0f31
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720343(v=OCS.15)
ms:contentKeyID: 63969636
ms.date: 05/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ad93c47ab8d157b1e18b4bccc5094408f3d68ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425411"
---
# <a name="monitoring-lync-server-2013-with-system-center-operations-manager"></a><span data-ttu-id="b33ce-103">Мониторинг сервера Lync Server 2013 с помощью System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="b33ce-103">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b33ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b33ce-104">

<span> </span></span></span>

<span data-ttu-id="b33ce-105">_**Тема последнего изменения:** 2015-05-06_</span><span class="sxs-lookup"><span data-stu-id="b33ce-105">_**Topic Last Modified:** 2015-05-06_</span></span>

<span data-ttu-id="b33ce-106">Пакет управления Lync Server Management Pack (MP) — это решение для мониторинга, которое можно выбирать для наблюдения за развертыванием Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b33ce-106">The Lync Server Management Pack (MP) is your monitoring solution of choice for monitoring any Lync Server deployment.</span></span>

<span data-ttu-id="b33ce-107">MP реализует традиционный журнал событий и инструментарий на основе счетчиков, а также включает новые доступные инструментария в Lync Server, такие как связывание событий (сбоев и успехов) для нескольких ключевых индикаторов работоспособности, и полностью применяет новые синтетические транзакции ( \* командлеты Windows PowerShell для тестирования и проверки).</span><span class="sxs-lookup"><span data-stu-id="b33ce-107">The MP implements traditional Event Log and Performance counter-based instrumentation and enables newly available instrumentation in Lync Server, such as pair events (failure/success) for several Key Health Indicators, and also fully implements the new Synthetic Transactions (Test-Cs\* Windows PowerShell cmdlets).</span></span>

<span data-ttu-id="b33ce-108">Пакет управления Lync Server 2013 и связанные с ним документы можно найти по адресу [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468) .</span><span class="sxs-lookup"><span data-stu-id="b33ce-108">You can find the Lync Server 2013 Management Pack and its related documentation at [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468).</span></span> <span data-ttu-id="b33ce-109">Это рекомендуется, если вы используете System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="b33ce-109">This is recommended if you are running System Center Operations Manager 2012.</span></span>

<span data-ttu-id="b33ce-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b33ce-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

