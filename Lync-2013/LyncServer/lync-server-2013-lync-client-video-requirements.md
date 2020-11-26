---
title: 'Lync Server 2013: требования к клиентскому видеоролику Lync'
description: 'Lync Server 2013: требования к клиентскому видеоролику Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync client video requirements
ms:assetid: 8f68f4c2-3194-487c-bd2f-fbe71ba8ad70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688132(v=OCS.15)
ms:contentKeyID: 49733731
ms.date: 01/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea1d4a993650ec8102d8b66ea5aa936ad1613f20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426440"
---
# <a name="lync-client-video-requirements-for-lync-server-2013"></a><span data-ttu-id="2275d-103">Требования к видео в Lync для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2275d-103">Lync client video requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2275d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2275d-104">

<span> </span></span></span>

<span data-ttu-id="2275d-105">_**Тема последнего изменения:** 2016-01-29_</span><span class="sxs-lookup"><span data-stu-id="2275d-105">_**Topic Last Modified:** 2016-01-29_</span></span>

<span data-ttu-id="2275d-106">В этом разделе рассказывается о поддержке видео для видеозвонков Lync 2013 и описано, как определить ожидаемое качество видео для различных конфигураций компьютера, планшета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2275d-106">This section describes video hardware support for Lync 2013 video calls and describes how to determine the expected video quality for various computer, tablet, and mobile device configurations.</span></span>

<div>

## <a name="windows-desktop-and-tablet-video-requirements-and-capabilities"></a><span data-ttu-id="2275d-107">Требования и возможности для настольных систем Windows и планшетных видео</span><span class="sxs-lookup"><span data-stu-id="2275d-107">Windows Desktop and Tablet Video Requirements and Capabilities</span></span>

<span data-ttu-id="2275d-108">Lync 2013 представляет аппаратное ускорение для кодирования и декодирования видео, основанное на стандарте H. 264/MPEG-4 части 10 расширенного кодирования видео.</span><span class="sxs-lookup"><span data-stu-id="2275d-108">Lync 2013 introduces hardware acceleration for video encoding and decoding based on the H.264/MPEG-4 Part 10 Advanced Video Coding standard.</span></span> <span data-ttu-id="2275d-109">Эта возможность позволяет компьютерам с более низкой скоростью ЦП кодировать и декодировать видео с более высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="2275d-109">This feature allows computers with lower CPU clock speeds to encode and decode higher resolution video.</span></span> <span data-ttu-id="2275d-110">Требования к видеоустройствам зависят от конфигурации компьютера и необходимого разрешения видео.</span><span class="sxs-lookup"><span data-stu-id="2275d-110">Video hardware requirements vary depending on the computer configuration and the video resolution wanted.</span></span>

<div>

## <a name="video-hardware-requirements"></a><span data-ttu-id="2275d-111">Требования к видеооборудованию</span><span class="sxs-lookup"><span data-stu-id="2275d-111">Video Hardware Requirements</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2275d-112">Функция</span><span class="sxs-lookup"><span data-stu-id="2275d-112">Feature</span></span></th>
<th><span data-ttu-id="2275d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2275d-113">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2275d-114">Аппаратное ускорение декодирования H.264 с помощью DirectX Video Acceleration (DXVA)</span><span class="sxs-lookup"><span data-stu-id="2275d-114">Hardware accelerated H.264 decoding using DirectX Video Acceleration (DXVA)</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2275d-115">Графическая карта должна поддерживать DirectX 9.0 и работать в режиме декодирования DXVA2_ModeH264_VLD_NoFGT.</span><span class="sxs-lookup"><span data-stu-id="2275d-115">Graphics card must support DirectX 9.0 and must expose the DXVA2_ModeH264_VLD_NoFGT decoding mode.</span></span></p></li>
<li><p><span data-ttu-id="2275d-116">Должен быть установлен последний драйвер графической карты.</span><span class="sxs-lookup"><span data-stu-id="2275d-116">The latest graphics card driver must be installed.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="2275d-117">Подробные сведения о режимах декодирования можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A> .</span><span class="sxs-lookup"><span data-stu-id="2275d-117">For details about decoding modes, see <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A>.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-118">Аппаратное ускорение кодирования H.264: требования к набору микросхем</span><span class="sxs-lookup"><span data-stu-id="2275d-118">Hardware accelerated H.264 encoding: Chipset Requirements</span></span></p></td>
<td><p><span data-ttu-id="2275d-119">Поддерживаются перечисленные ниже решения Intel для кодирования видео с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="2275d-119">The following Intel hardware accelerated video encoding solutions are supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="2275d-120">Вторая и третья графическая плата Intel HD 2000, 2500, 3000 и 4000 наборы микросхем (или более поздних версий) с интегрированными аппаратными кодировщиками.</span><span class="sxs-lookup"><span data-stu-id="2275d-120">Second and third generation Intel HD Graphics 2000, 2500, 3000, and 4000 chipsets (or later versions) with integrated hardware video encoders.</span></span> <span data-ttu-id="2275d-121">Требуется установка драйвера Intel HD Graphics 15.28.9.2884 или более поздней версии с перечисленными ниже компонентами</span><span class="sxs-lookup"><span data-stu-id="2275d-121">Installation of the Intel HD Graphics driver 15.28.9.2884 or the latest driver containing the following is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="2275d-122">Драйвер дисплея 9.17.10.2884 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2275d-122">Display driver 9.17.10.2884 or the latest driver</span></span></p></li>
<li><p><span data-ttu-id="2275d-123">Платформа HMFT 3.12.10.31 или последней версии</span><span class="sxs-lookup"><span data-stu-id="2275d-123">Hardware media foundation transform (HMFT) version 3.12.10.31 or the latest HMFT</span></span></p></li>
</ul></li>
</ul>
<p><span data-ttu-id="2275d-124">Поддерживаются следующие решения для кодирования видео с аппаратным ускорением AMD (требуется обновление CU1 для Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="2275d-124">The following AMD hardware accelerated video encoding solutions are supported (requires CU1 Updates for Lync Server 2013):</span></span></p>
<ul>
<li><p><span data-ttu-id="2275d-p103">Модуль видеокодеков AMD Video Codec Engine, имеющийся в некоторых адаптерах дискретной графики, а также во встроенных блоках ускоренной обработки серии AMD A-Series Accelerated Processors. Должен быть установлен драйвер AMD Video Codec Engine 9.12.0.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2275d-p103">AMD Video Codec Engine, which is available in several discrete graphics cards and in integrated accelerated processing units of AMD A-Series Accelerated Processors. The AMD Video Codec Engine driver 9.12.0.0 or higher must be installed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2275d-127">Аппаратное ускорение кодирования H.264: требования к камере</span><span class="sxs-lookup"><span data-stu-id="2275d-127">Hardware accelerated H.264 encoding: Camera Requirements</span></span></p></td>
<td><p><span data-ttu-id="2275d-128">Видеокамеры USB со встроенным аппаратным кодировщиком H.264, поддерживающие спецификацию USB Video Class (UVC) версии 1.5.</span><span class="sxs-lookup"><span data-stu-id="2275d-128">USB video cameras with integrated H.264 hardware encoder that conforms to the USB Video Class (UVC) specification version 1.5.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="2275d-129">Lync 2013 поддерживает камеры UVC 1,5 в Windows 8 или Windows 8,1, в том числе поддержка UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="2275d-129">Lync 2013 supports UVC 1.5 cameras with Windows 8 or Windows 8.1, which includes support for UVC 1.5.</span></span> <span data-ttu-id="2275d-130">Так как в Windows 7 не входит поддержка UVC 1,5, Lync 2013 рассматривает камеры UVC 1,5 как обычные камеры без поддержки аппаратной кодировки.</span><span class="sxs-lookup"><span data-stu-id="2275d-130">Because Windows 7 does not include support for UVC 1.5, Lync 2013 treats UVC 1.5 cameras as regular cameras with no hardware encoding support.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="determining-h264-video-encoding-and-decoding-capabilities"></a><span data-ttu-id="2275d-131">Определение возможностей кодирования и декодирования видео в 264</span><span class="sxs-lookup"><span data-stu-id="2275d-131">Determining H.264 Video Encoding and Decoding Capabilities</span></span>

<span data-ttu-id="2275d-132">В общем случае максимальная производительность кодирования и декодирования для конкретной конфигурации компьютера определяется четырьмя основными факторами:</span><span class="sxs-lookup"><span data-stu-id="2275d-132">Generally, there are four major factors that determine the maximum encoding and decoding capability of a particular computer configuration:</span></span>

  - <span data-ttu-id="2275d-133">поддержка аппаратного ускорения декодирования с помощью DXVA;</span><span class="sxs-lookup"><span data-stu-id="2275d-133">Support for hardware accelerated decoding by using DXVA</span></span>

  - <span data-ttu-id="2275d-134">поддержка аппаратного ускорения кодирования;</span><span class="sxs-lookup"><span data-stu-id="2275d-134">Support for hardware accelerated encoding</span></span>

  - <span data-ttu-id="2275d-135">количество физических ядер;</span><span class="sxs-lookup"><span data-stu-id="2275d-135">Number of physical cores</span></span>

  - <span data-ttu-id="2275d-136">индекс производительности Windows (WEI).</span><span class="sxs-lookup"><span data-stu-id="2275d-136">Windows Experience Index (WEI)</span></span>

<span data-ttu-id="2275d-137">Средство оценки производительности WinSAT определяет индекс WEI.</span><span class="sxs-lookup"><span data-stu-id="2275d-137">The Windows System Assessment Tool (WinSAT) determines the WEI.</span></span> <span data-ttu-id="2275d-138">При запуске средства WinSAT создается формальный XML-документ. Оценка на компьютере в каталоге% WINDIR% с \\ производительностью WinSAT с \\ \\ хранилищем хранилищ.</span><span class="sxs-lookup"><span data-stu-id="2275d-138">When you run the WinSAT tool, it generates a Formal.Assessment XML document on the computer in the %windir%\\Performance\\WinSAT\\DataStore directory.</span></span> <span data-ttu-id="2275d-139">В этом XML-файле представлены два показателя, на основании которых можно определить возможности кодирования и декодирования:</span><span class="sxs-lookup"><span data-stu-id="2275d-139">This XML file contains the following two scores that are of particular importance for determining encoding and decoding capabilities:</span></span>

  - <span data-ttu-id="2275d-140">значение VideoEncodeScore показывает производительность компьютера по программному кодированию видео;</span><span class="sxs-lookup"><span data-stu-id="2275d-140">The VideoEncodeScore indicates the software-based video encoding capability of the computer.</span></span>

  - <span data-ttu-id="2275d-141">значение GraphicsScore показывает производительность компьютера по кодированию видео с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="2275d-141">The GraphicsScore value indicates the hardware accelerated encoding capability of the computer.</span></span>

<span data-ttu-id="2275d-p106">В следующих таблицах приводится максимальная производительность кодирования и декодирования для нескольких типов ПК в зависимости от поддержки аппаратного ускорения. Для разрешения 640x360 и выше максимальная поддерживаемая частота кадров составляет 30 кадров в секунду (кадр/с). Для разрешений ниже 640x360 максимальная поддерживаемая частота кадров составляет 15 кадр/с.</span><span class="sxs-lookup"><span data-stu-id="2275d-p106">The following three tables explain the maximum encoding and decoding capability for different PC types depending on what hardware acceleration they support. For resolutions of 640x360 and higher, the maximum supported frame rate is 30 frames per second (fps). For resolutions lower than 640x360, the maximum supported frame rate is 15 fps.</span></span>

### <a name="computer-without-dxva-and-without-hardware-accelerated-encoder"></a><span data-ttu-id="2275d-145">Компьютер без DXVA и без аппаратного ускорения кодирования</span><span class="sxs-lookup"><span data-stu-id="2275d-145">Computer Without DXVA And Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2275d-146">Поддерживаемое разрешение кодировщика</span><span class="sxs-lookup"><span data-stu-id="2275d-146">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="2275d-147">Поддерживаемое разрешение декодера</span><span class="sxs-lookup"><span data-stu-id="2275d-147">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="2275d-148">Требование</span><span class="sxs-lookup"><span data-stu-id="2275d-148">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2275d-149">424x240</span><span class="sxs-lookup"><span data-stu-id="2275d-149">424x240</span></span></p></td>
<td><p><span data-ttu-id="2275d-150">424x240 (640x360 при 15 кадр/с только для приема)</span><span class="sxs-lookup"><span data-stu-id="2275d-150">424x240 (640x360 at 15fps for receive only scenarios)</span></span></p></td>
<td><p><span data-ttu-id="2275d-151">1 ядро и VideoEncodeScore ≥ 4.0</span><span class="sxs-lookup"><span data-stu-id="2275d-151">1 Core and VideoEncodeScore ≥ 4.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-152">640x360</span><span class="sxs-lookup"><span data-stu-id="2275d-152">640x360</span></span></p></td>
<td><p><span data-ttu-id="2275d-153">640x360</span><span class="sxs-lookup"><span data-stu-id="2275d-153">640x360</span></span></p></td>
<td><p><span data-ttu-id="2275d-154">2 ядра и VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="2275d-154">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2275d-155">640x360</span><span class="sxs-lookup"><span data-stu-id="2275d-155">640x360</span></span></p></td>
<td><p><span data-ttu-id="2275d-156">1280x720</span><span class="sxs-lookup"><span data-stu-id="2275d-156">1280x720</span></span></p></td>
<td><p><span data-ttu-id="2275d-157">2 ядра и VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="2275d-157">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-158">640x360</span><span class="sxs-lookup"><span data-stu-id="2275d-158">640x360</span></span></p></td>
<td><p><span data-ttu-id="2275d-159">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-159">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-160">4 ядра и VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="2275d-160">4 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2275d-161">1280x720</span><span class="sxs-lookup"><span data-stu-id="2275d-161">1280x720</span></span></p></td>
<td><p><span data-ttu-id="2275d-162">1280x720</span><span class="sxs-lookup"><span data-stu-id="2275d-162">1280x720</span></span></p></td>
<td><p><span data-ttu-id="2275d-163">4 ядра и VideoEncodeScore ≥ 7.3</span><span class="sxs-lookup"><span data-stu-id="2275d-163">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-164">1280x720</span><span class="sxs-lookup"><span data-stu-id="2275d-164">1280x720</span></span></p></td>
<td><p><span data-ttu-id="2275d-165">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-165">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-166">4 ядра и VideoEncodeScore ≥ 7.3</span><span class="sxs-lookup"><span data-stu-id="2275d-166">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2275d-167">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-167">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-168">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-168">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2275d-169">N/A</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="computer-with-dxva-but-without-hardware-accelerated-encoder"></a><span data-ttu-id="2275d-170">Компьютер с DXVA, но без аппаратного ускорения кодирования</span><span class="sxs-lookup"><span data-stu-id="2275d-170">Computer With DXVA But Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2275d-171">Поддерживаемое разрешение кодировщика</span><span class="sxs-lookup"><span data-stu-id="2275d-171">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="2275d-172">Поддерживаемое разрешение декодера</span><span class="sxs-lookup"><span data-stu-id="2275d-172">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="2275d-173">Требование</span><span class="sxs-lookup"><span data-stu-id="2275d-173">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2275d-174">424x240</span><span class="sxs-lookup"><span data-stu-id="2275d-174">424x240</span></span></p></td>
<td><p><span data-ttu-id="2275d-175">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-175">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-176">1 ядро и VideoEncodeScore ≥ 3.0</span><span class="sxs-lookup"><span data-stu-id="2275d-176">1 Core and VideoEncodeScore ≥ 3.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-177">640x360</span><span class="sxs-lookup"><span data-stu-id="2275d-177">640x360</span></span></p></td>
<td><p><span data-ttu-id="2275d-178">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-178">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-179">2 ядра и VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="2275d-179">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2275d-180">960x540</span><span class="sxs-lookup"><span data-stu-id="2275d-180">960x540</span></span></p></td>
<td><p><span data-ttu-id="2275d-181">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-181">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-182">2 ядра и VideoEncodeScore ≥ 6.0</span><span class="sxs-lookup"><span data-stu-id="2275d-182">2 Cores and VideoEncodeScore ≥ 6.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-183">1280x720</span><span class="sxs-lookup"><span data-stu-id="2275d-183">1280x720</span></span></p></td>
<td><p><span data-ttu-id="2275d-184">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-184">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-185">4 ядра и VideoEncodeScore ≥ 6.7</span><span class="sxs-lookup"><span data-stu-id="2275d-185">4 Cores and VideoEncodeScore ≥ 6.7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2275d-186">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-186">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-187">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-187">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-188">4 ядра и VideoEncodeScore ≥ 8.2</span><span class="sxs-lookup"><span data-stu-id="2275d-188">4 Cores and VideoEncodeScore ≥ 8.2</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="2275d-p107">В Windows 7 максимальное значение показателя WinSAT составляет 7,9, поэтому такая производительность кодирования для компьютера без аппаратного ускорения может быть достигнута только в Windows 8 или Windows 8.1, где максимальное значение показателя WinSAT составляет 9,9.</span><span class="sxs-lookup"><span data-stu-id="2275d-p107">The WinSAT score on Windows 7 is limited to a maximum of 7.9. Therefore, the encoding capability for a computer without a hardware accelerated encoder can only be achieved on Windows 8 or Windows 8.1, where the maximum WinSAT score is 9.9.</span></span>



</div>

### <a name="computer-with-dxva-and-with-intel-hd-graphics-hardware-accelerated-encoder"></a><span data-ttu-id="2275d-191">Компьютер с DXVA и с аппаратным ускорителем кодирования Intel HD Graphics</span><span class="sxs-lookup"><span data-stu-id="2275d-191">Computer With DXVA And With Intel HD Graphics Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2275d-192">Поддерживаемое разрешение кодировщика</span><span class="sxs-lookup"><span data-stu-id="2275d-192">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="2275d-193">Поддерживаемое разрешение декодера</span><span class="sxs-lookup"><span data-stu-id="2275d-193">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="2275d-194">Требование</span><span class="sxs-lookup"><span data-stu-id="2275d-194">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2275d-195">1280x720</span><span class="sxs-lookup"><span data-stu-id="2275d-195">1280x720</span></span></p></td>
<td><p><span data-ttu-id="2275d-196">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-196">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-197">Все графические карты Intel HD Graphics второго и третьего поколения</span><span class="sxs-lookup"><span data-stu-id="2275d-197">All 2nd and 3rd generation Intel HD Graphics</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-198">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-198">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-199">1920x1080</span><span class="sxs-lookup"><span data-stu-id="2275d-199">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="2275d-200">Графические карты Intel HD Graphics второго и третьего поколения и GraphicsScore ≥ 5.0</span><span class="sxs-lookup"><span data-stu-id="2275d-200">2nd and 3rd generation Intel HD Graphics and GraphicsScore ≥ 5.0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="mobile-device-video-capabilities"></a><span data-ttu-id="2275d-201">Видео о возможностях мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="2275d-201">Mobile Device Video Capabilities</span></span>

<span data-ttu-id="2275d-202">В следующей таблице описываются максимальные возможности видеосвязи для поддерживаемых мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2275d-202">The following table describes the maximum video capabilities for supported mobile devices.</span></span> <span data-ttu-id="2275d-203">Дополнительные сведения о поддержке мобильных устройств можно найти [в разделе Планирование мобильных клиентов в Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span><span class="sxs-lookup"><span data-stu-id="2275d-203">For more information about mobile device support, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2275d-204">Функция</span><span class="sxs-lookup"><span data-stu-id="2275d-204">Feature</span></span></th>
<th><span data-ttu-id="2275d-205">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="2275d-205">Windows Phone</span></span></th>
<th><span data-ttu-id="2275d-206">iPhone</span><span class="sxs-lookup"><span data-stu-id="2275d-206">iPhone</span></span></th>
<th><span data-ttu-id="2275d-207">iPad</span><span class="sxs-lookup"><span data-stu-id="2275d-207">iPad</span></span></th>
<th><span data-ttu-id="2275d-208">Android</span><span class="sxs-lookup"><span data-stu-id="2275d-208">Android</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2275d-209">Максимальное разрешение при кодировании H.264</span><span class="sxs-lookup"><span data-stu-id="2275d-209">H.264 encoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="2275d-210">VGA</span><span class="sxs-lookup"><span data-stu-id="2275d-210">VGA</span></span></p></td>
<td><p><span data-ttu-id="2275d-211">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="2275d-211">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="2275d-212">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="2275d-212">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="2275d-213">720p: iPhone 5S и более новые модели</span><span class="sxs-lookup"><span data-stu-id="2275d-213">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="2275d-214">VGA: iPad 2 и более новые модели/iPad mini 1 и более новые модели</span><span class="sxs-lookup"><span data-stu-id="2275d-214">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="2275d-215">720p: iPad Air/iPad mini 2/iPad Pro и более новые модели</span><span class="sxs-lookup"><span data-stu-id="2275d-215">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="2275d-216">До VGA (в зависимости от модели устройства)</span><span class="sxs-lookup"><span data-stu-id="2275d-216">Up to VGA depending on device model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2275d-217">Максимальное разрешение при декодировании H.264</span><span class="sxs-lookup"><span data-stu-id="2275d-217">H.264 decoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="2275d-218">VGA</span><span class="sxs-lookup"><span data-stu-id="2275d-218">VGA</span></span></p></td>
<td><p><span data-ttu-id="2275d-219">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="2275d-219">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="2275d-220">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="2275d-220">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="2275d-221">720p: iPhone 5S и более новые модели</span><span class="sxs-lookup"><span data-stu-id="2275d-221">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="2275d-222">VGA: iPad 2 и более новые модели/iPad mini 1 и более новые модели</span><span class="sxs-lookup"><span data-stu-id="2275d-222">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="2275d-223">720p: iPad Air/iPad mini 2/iPad Pro и более новые модели</span><span class="sxs-lookup"><span data-stu-id="2275d-223">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="2275d-224">До VGA (в зависимости от модели устройства)</span><span class="sxs-lookup"><span data-stu-id="2275d-224">Up to VGA depending on device model</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2275d-225">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2275d-225">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

