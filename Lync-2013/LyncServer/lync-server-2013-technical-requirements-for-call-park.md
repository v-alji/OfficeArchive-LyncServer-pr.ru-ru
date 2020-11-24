---
title: 'Lync Server 2013: технические требования к парковке вызовов'
description: 'Lync Server 2013: технические требования для приостановки звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Call Park
ms:assetid: 38bcf302-2b72-4492-9266-f6dc31b566e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204818(v=OCS.15)
ms:contentKeyID: 48183897
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ddc17b40f78c42c090d1a87b4580ebdad0a07f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399232"
---
# <a name="technical-requirements-for-call-park-in-lync-server-2013"></a><span data-ttu-id="d374b-103">Технические требования к парковке вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d374b-103">Technical requirements for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d374b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d374b-104">

<span> </span></span></span>

<span data-ttu-id="d374b-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="d374b-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="d374b-106">В этом разделе описаны указанные ниже технические требования к приостановке звонков.</span><span class="sxs-lookup"><span data-stu-id="d374b-106">This section describes the following technical requirements for Call Park:</span></span>

  - <span data-ttu-id="d374b-107">Требования к оборудованию</span><span class="sxs-lookup"><span data-stu-id="d374b-107">Hardware requirements</span></span>

  - <span data-ttu-id="d374b-108">Требования к программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="d374b-108">Software requirements</span></span>

  - <span data-ttu-id="d374b-109">Требования к портам</span><span class="sxs-lookup"><span data-stu-id="d374b-109">Port requirements</span></span>

  - <span data-ttu-id="d374b-110">Требования к звуковым файлам</span><span class="sxs-lookup"><span data-stu-id="d374b-110">Audio file requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="d374b-111">Требования к оборудованию</span><span class="sxs-lookup"><span data-stu-id="d374b-111">Hardware Requirements</span></span>

<span data-ttu-id="d374b-112">Приложение для парковки звонков имеет те же аппаратные требования, что и внешние серверы.</span><span class="sxs-lookup"><span data-stu-id="d374b-112">The Call Park application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="d374b-113">Сведения о требованиях к оборудованию можно найти в документации [серверные платформы для Lync server 2013](lync-server-2013-server-hardware-platforms.md) .</span><span class="sxs-lookup"><span data-stu-id="d374b-113">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="d374b-114">Требования к программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="d374b-114">Software Requirements</span></span>

<span data-ttu-id="d374b-115">Приложение для парковки звонков имеет те же требования к операционной системе и необходимые компоненты по отношению к серверам переднего плана.</span><span class="sxs-lookup"><span data-stu-id="d374b-115">The Call Park application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="d374b-116">Подробные сведения о требованиях к программному обеспечению можно найти [в разделе Поддержка серверов и средств операционной системы в Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="d374b-116">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="d374b-117">На всех серверах переднего плана и стандартных серверах, где развернуто приложение для остановки приема звонков, должна быть установлена среда выполнения формата Windows Media для серверов с операционной системой Windows Server 2008 R2 или Microsoft Media Foundation для серверов под управлением Windows Server 2012 или Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d374b-117">All Front End Servers and Standard Edition servers where the Call Park application is deployed must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="d374b-118">В операционной системе Windows Server 2008 R2 на компьютере с Windows можно установить среду выполнения формата Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d374b-118">For Windows Server 2008 R2, Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span> <span data-ttu-id="d374b-119">Формат среды выполнения Windows Media Audio (WMA), необходимый для воспроизведений музыкальных файлов, используется для воспроизведения музыки на удержании.</span><span class="sxs-lookup"><span data-stu-id="d374b-119">Windows Media Format Runtime or Microsoft Media Foundation is required for Windows Media Audio (.wma) files that Call Park plays for music on hold.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="d374b-120">Требования к портам</span><span class="sxs-lookup"><span data-stu-id="d374b-120">Port Requirements</span></span>

<span data-ttu-id="d374b-121">Приложение для парковки звонков использует следующий порт:</span><span class="sxs-lookup"><span data-stu-id="d374b-121">The Call Park application uses the following port:</span></span>

  - <span data-ttu-id="d374b-122">**Порт 5075**   Служит для запросов на прослушивание по протоколу SIP.</span><span class="sxs-lookup"><span data-stu-id="d374b-122">**Port 5075**   Used for SIP listening requests.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d374b-123">Этот порт — это параметр по умолчанию, который можно изменить с помощью командлета <STRONG>Set-CsApplicationServer</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="d374b-123">This port is a default setting that you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="d374b-124">Подробные сведения об этом командлете можно найти в документации по оболочке Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="d374b-124">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="d374b-125">Требования к аудиофайлам</span><span class="sxs-lookup"><span data-stu-id="d374b-125">Audio File Requirements</span></span>

<span data-ttu-id="d374b-126">Приложение для парковки звонков поддерживает только файлы Windows Media Audio (WMA) для музыки на удержании.</span><span class="sxs-lookup"><span data-stu-id="d374b-126">The Call Park application supports only Windows Media Audio (.wma) files for music on hold.</span></span> <span data-ttu-id="d374b-127">Чтобы настроить файлы для воспроизведения в качестве музыки в режиме удержания, можно использовать Microsoft Expression Encoder 4.</span><span class="sxs-lookup"><span data-stu-id="d374b-127">You can use the Microsoft Expression Encoder 4 to customize files for music on hold.</span></span> <span data-ttu-id="d374b-128">Загрузить Expression Encoder 4 можно в разделе "Expression Encoder 4" [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) .</span><span class="sxs-lookup"><span data-stu-id="d374b-128">To download Expression Encoder 4, see "Expression Encoder 4" at [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843).</span></span> <span data-ttu-id="d374b-129">Это средство используется для преобразования файлов в формат WMA.</span><span class="sxs-lookup"><span data-stu-id="d374b-129">Use the tool to convert the file to a .wma format.</span></span> <span data-ttu-id="d374b-130">Рекомендуемый формат музыкальных файлов на входе в службу для парковки — это Media Audio 9, 44 кГц, 16 бит, моно, CBR, 32 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="d374b-130">The recommended format for Call Park music-on-hold files is Media Audio 9, 44 kHz, 16 bits, Mono, CBR, 32 kbps.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d374b-131">Преобразованный файл воспроизводится на телефоне только при 16 кГц, даже если он был записан при 44 кГц.</span><span class="sxs-lookup"><span data-stu-id="d374b-131">The converted file plays over the phone only at 16 kHz, even if it was recorded at 44 kHz.</span></span>



<span data-ttu-id="d374b-132"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d374b-132"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

