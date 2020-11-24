---
title: 'Lync Server 2013: планирование и развертывание видео'
description: 'Lync Server 2013: планирование и развертывание видео.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning and deploying video
ms:assetid: dadfb7f3-dfd6-4847-b137-17dacafd7368
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205307(v=OCS.15)
ms:contentKeyID: 48185558
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9fd8a93f890295daebd2bc887414a2417b86395
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398458"
---
# <a name="planning-and-deploying-video-in-lync-server-2013"></a><span data-ttu-id="06ffd-103">Планирование и развертывание видео в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06ffd-103">Planning and deploying video in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06ffd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06ffd-104">

<span> </span></span></span>

<span data-ttu-id="06ffd-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="06ffd-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="06ffd-106">В Lync Server 2013 появились следующие новые функции видео:</span><span class="sxs-lookup"><span data-stu-id="06ffd-106">Lync Server 2013 introduces the following new video features:</span></span>

  - <span data-ttu-id="06ffd-107">**Видео**   в формате HD   Пользователи могут столкнуться с разрешениями до полного высокого разрешения (HD) (1920 x 1080) во входящих звонках и многосторонних конференциях.</span><span class="sxs-lookup"><span data-stu-id="06ffd-107">**HD video**   Users can experience resolutions up to full high definition (HD) (that is, 1920 x 1080) in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="06ffd-108">**Представление коллекции**   В видеоконференциях с более чем двумя людьми пользователи могут просматривать видео участников Конференции.</span><span class="sxs-lookup"><span data-stu-id="06ffd-108">**Gallery View**   In video conferences that have more than two people, users can see videos of participants in the conference.</span></span> <span data-ttu-id="06ffd-109">Если на Конференции установлено более пяти участников собрания, в верхней строке отображаются только самые активные участники, а для других участников — фотография.</span><span class="sxs-lookup"><span data-stu-id="06ffd-109">If the conference has more than five participants, video of only the most active participants appears in the top row, and a photo appears for the other participants.</span></span>

  - <span data-ttu-id="06ffd-110">**H. 264 видео**   Видеокодек H. 264 теперь используется по умолчанию для кодирования видео на клиентах Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="06ffd-110">**H.264 video**   The H.264 video codec is now the default for encoding video on Lync 2013 clients.</span></span> <span data-ttu-id="06ffd-111">Видео H. 264 поддерживает широкий спектр разрешений и частот кадров, а затем повышает масштабируемость видео.</span><span class="sxs-lookup"><span data-stu-id="06ffd-111">H.264 video supports a greater range of resolutions and frame rates, and improves video scalability.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="06ffd-112">Lync Server 2013 по-прежнему поддерживает кодек VC1 для взаимодействия с предыдущими версиями Lync.</span><span class="sxs-lookup"><span data-stu-id="06ffd-112">Lync Server 2013 still supports the VC1 codec for interoperability with previous versions of Lync.</span></span> <span data-ttu-id="06ffd-113">Сведения и общие сведения о новом видеокоде можно найти в статье Schertz в блоге об использовании видео в Lync 2013 <A class=uri href="http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/">http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/</A> .</span><span class="sxs-lookup"><span data-stu-id="06ffd-113">For details and background information about the new video codec, see Jeff Schertz's Blog article, "Video Interoperability in Lync 2013," at <A class=uri href="http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/">http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/</A>.</span></span>

    
    </div>

<span data-ttu-id="06ffd-114">В этом разделе рассказывается, как управлять пропускной способностью видео в Lync Server 2013 и настраивать возможности видео.</span><span class="sxs-lookup"><span data-stu-id="06ffd-114">This section describes how to manage bandwidth for video in Lync Server 2013 and how to configure video features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="06ffd-115">Содержание</span><span class="sxs-lookup"><span data-stu-id="06ffd-115">In This Section</span></span>

  - [<span data-ttu-id="06ffd-116">Настройка пропускной способности видео в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06ffd-116">Configuring video bandwidth in Lync Server 2013</span></span>](lync-server-2013-configuring-video-bandwidth.md)

  - [<span data-ttu-id="06ffd-117">Настройка представления коллекции в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06ffd-117">Configuring Gallery View in Lync Server 2013</span></span>](lync-server-2013-configuring-gallery-view.md)

  - [<span data-ttu-id="06ffd-118">Настройка примеров видеороликов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06ffd-118">Configuring video example scenarios for Lync Server 2013</span></span>](lync-server-2013-configuring-video-example-scenarios.md)

  - [<span data-ttu-id="06ffd-119">Рекомендации по взаимодействию при видеоконференциях в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06ffd-119">Interoperability considerations for video conferencing in Lync Server 2013</span></span>](lync-server-2013-interoperability-considerations-for-video-conferencing.md)

<span data-ttu-id="06ffd-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06ffd-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

