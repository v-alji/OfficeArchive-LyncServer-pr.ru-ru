---
title: 'Lync Server 2013: технические требования для групп ответа'
description: 'Lync Server 2013: технические требования для группы ответа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Response Group
ms:assetid: 477488bd-124f-437b-9327-732a0d7271ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204863(v=OCS.15)
ms:contentKeyID: 48184044
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f3125ed8c732960e23970229e99bf5a8487eb96a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441300"
---
# <a name="technical-requirements-for-response-group-in-lync-server-2013"></a><span data-ttu-id="9b6f8-103">Технические требования для групп ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b6f8-103">Technical requirements for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b6f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b6f8-104">

<span> </span></span></span>

<span data-ttu-id="9b6f8-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="9b6f8-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="9b6f8-106">В этом разделе описаны указанные ниже технические требования к приложению группы ответа.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-106">This section describes the following technical requirements for the Response Group application:</span></span>

  - <span data-ttu-id="9b6f8-107">Требования к оборудованию</span><span class="sxs-lookup"><span data-stu-id="9b6f8-107">Hardware requirements</span></span>

  - <span data-ttu-id="9b6f8-108">Требования к программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="9b6f8-108">Software requirements</span></span>

  - <span data-ttu-id="9b6f8-109">Требования к портам</span><span class="sxs-lookup"><span data-stu-id="9b6f8-109">Port requirements</span></span>

  - <span data-ttu-id="9b6f8-110">Требования к звуковым файлам</span><span class="sxs-lookup"><span data-stu-id="9b6f8-110">Audio file requirements</span></span>

  - <span data-ttu-id="9b6f8-111">Требования к инструментам настройки группы ответа</span><span class="sxs-lookup"><span data-stu-id="9b6f8-111">Response Group configuration tool requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="9b6f8-112">Требования к оборудованию</span><span class="sxs-lookup"><span data-stu-id="9b6f8-112">Hardware Requirements</span></span>

<span data-ttu-id="9b6f8-113">Приложение группы ответа имеет те же аппаратные требования, что и сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-113">The Response Group application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="9b6f8-114">Сведения о требованиях к оборудованию можно найти в документации [серверные платформы для Lync server 2013](lync-server-2013-server-hardware-platforms.md) .</span><span class="sxs-lookup"><span data-stu-id="9b6f8-114">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="9b6f8-115">Требования к программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="9b6f8-115">Software Requirements</span></span>

<span data-ttu-id="9b6f8-116">Приложение группы ответа имеет те же требования к операционной системе и необходимые компоненты по отношению к серверам переднего плана.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-116">The Response Group application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="9b6f8-117">Подробные сведения о требованиях к программному обеспечению можно найти [в разделе Поддержка серверов и средств операционной системы в Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-117">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="9b6f8-118">Если вы используете файлы Windows Media Audio (WMA) для музыкального сопровождения и объявлений группы ответа, все серверы переднего плана и стандартные серверы выпусков, на которых запускается приложение группы ответа, должны иметь установленную среду выполнения формата Windows Media для серверов с операционной системой Windows Server 2008 R2 или Microsoft Media Foundation для серверов под управлением Windows Server 2012 или Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-118">If you use Windows Media Audio (.wma) files for Response Group music and announcements, all Front End Servers or Standard Editions servers that run the Response Group application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="9b6f8-119">В операционной системе Windows Server 2008 R2 на компьютере с Windows можно установить среду выполнения формата Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-119">For Windows Server 2008 R2, Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span>

<span data-ttu-id="9b6f8-120">Дополнительные сведения о требованиях к аудио можно найти в разделе "требования к звуковым файлам" ниже.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-120">For more details about audio requirements, see "Audio File Requirements" later in this section.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="9b6f8-121">Требования к портам</span><span class="sxs-lookup"><span data-stu-id="9b6f8-121">Port Requirements</span></span>

<span data-ttu-id="9b6f8-122">Приложение "группа ответа" использует следующие порты:</span><span class="sxs-lookup"><span data-stu-id="9b6f8-122">The Response Group application uses the following ports:</span></span>

  - <span data-ttu-id="9b6f8-123">**Порт 5071**   используется для запросов прослушивания SIP</span><span class="sxs-lookup"><span data-stu-id="9b6f8-123">**Port 5071**   Used for SIP listening requests</span></span>

  - <span data-ttu-id="9b6f8-124">**Порт 8404**   используется для межсерверного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-124">**Port 8404**   Used for interserver communications</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9b6f8-125">Этот порт используется для проверки соответствия требованиям и является обязательным, если приложение группы ответа развернуто в пуле, который содержит более одного сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-125">This port is used for the Match Making service and is required when the Response Group application is deployed in a pool that has more than one Front End Server.</span></span>

    
    </div>

<div>


> [!NOTE]  
> <span data-ttu-id="9b6f8-126">Эти порты являются установками по умолчанию, которые можно изменить с помощью командлета <STRONG>Set-CsApplicationServer</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-126">These ports are default settings that you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="9b6f8-127">Подробные сведения об этом командлете можно найти в документации по оболочке Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-127">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="9b6f8-128">Требования к аудиофайлам</span><span class="sxs-lookup"><span data-stu-id="9b6f8-128">Audio File Requirements</span></span>

<span data-ttu-id="9b6f8-129">Приложение "группа ответа" поддерживает формат файла Wave (WAV) и формат Windows Media Audio (WMA) для сообщений группы ответа, хранения музыки и интерактивных голосовых ответов (интерактивный автоответчик).</span><span class="sxs-lookup"><span data-stu-id="9b6f8-129">The Response Group application supports wave (.wav) file format and Windows Media audio (.wma) file format for Response Group messages, on-hold music, or interactive voice response (IVR) questions.</span></span>

<span data-ttu-id="9b6f8-130">Для формата звуковых файлов Windows Media требуется, чтобы среда выполнения формата Windows Media была установлена на серверах переднего плана под управлением Windows Server 2008 R2 и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-130">The Windows Media audio file format requires that the Windows Media Format Runtime is installed on Front End Servers running Windows Server 2008 R2 and Windows Server 2008.</span></span> <span data-ttu-id="9b6f8-131">Более подробно см. выше в подразделе "Требования к программному обеспечению".</span><span class="sxs-lookup"><span data-stu-id="9b6f8-131">For more details, see "Software Requirements" earlier in this section.</span></span>

<div>

## <a name="supported-wave-file-formats"></a><span data-ttu-id="9b6f8-132">Поддерживаемые форматы файлов WAV</span><span class="sxs-lookup"><span data-stu-id="9b6f8-132">Supported Wave File Formats</span></span>

<span data-ttu-id="9b6f8-133">Все файлы WAV должны удовлетворять следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-133">All wave files must meet the following requirements:</span></span>

  - <span data-ttu-id="9b6f8-134">8-разрядный или 16-разрядный файл</span><span class="sxs-lookup"><span data-stu-id="9b6f8-134">8-bit or 16-bit file</span></span>

  - <span data-ttu-id="9b6f8-135">Формат линейной импульсно-кодовой модуляции, A-Law или mu-Law</span><span class="sxs-lookup"><span data-stu-id="9b6f8-135">Linear pulse code modulation (LPCM), A-Law, or mu-Law format</span></span>

  - <span data-ttu-id="9b6f8-136">Моно или стерео</span><span class="sxs-lookup"><span data-stu-id="9b6f8-136">Mono or stereo</span></span>

  - <span data-ttu-id="9b6f8-137">4 МБ или меньше</span><span class="sxs-lookup"><span data-stu-id="9b6f8-137">4MB or less</span></span>

<span data-ttu-id="9b6f8-138">Для обеспечения наилучшей производительности файлов WAV рекомендуется использовать монофонический 16-разрядный файл WAV с частотой 16 кГц.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-138">For the best performance of wave files, a 16 kHz, mono, 16-bit Wave file is recommended.</span></span>

</div>

<div>

## <a name="supported-windows-media-audio-file-formats"></a><span data-ttu-id="9b6f8-139">Поддерживаемые форматы файлов WMA</span><span class="sxs-lookup"><span data-stu-id="9b6f8-139">Supported Windows Media Audio File Formats</span></span>

<span data-ttu-id="9b6f8-140">Если вы используете файл WMA, рекомендуется применять низкие скорости и проверить производительность системы под нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-140">If you use a Windows Media audio file, consider using low bit rates, and verify the performance of your system under load.</span></span>

<span data-ttu-id="9b6f8-141">Вы можете использовать Microsoft Expression Encoder 4 для преобразования файла в звуковой формат Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-141">You can use the Microsoft Expression Encoder 4 to convert a file to the Windows Media Audio format.</span></span> <span data-ttu-id="9b6f8-142">Чтобы скачать Expression Encoder 4, ознакомьтесь с разрядом [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) .</span><span class="sxs-lookup"><span data-stu-id="9b6f8-142">To download Expression Encoder 4, see [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843).</span></span>

</div>

</div>

<div>

## <a name="response-group-configuration-tool-requirements"></a><span data-ttu-id="9b6f8-143">Требования к средствам настройки группы ответа</span><span class="sxs-lookup"><span data-stu-id="9b6f8-143">Response Group Configuration Tool Requirements</span></span>

<span data-ttu-id="9b6f8-144">Средство настройки группы ответа поддерживает комбинации операционных систем и веб-браузеров, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-144">The Response Group Configuration Tool supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9b6f8-p107">Поддерживаются 32-разрядная или 64-разрядная версии операционных систем. Поддерживаются только 32-разрядные версии Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-p107">32-bit or 64-bit versions of the operating systems are supported. Only 32-bit versions of Internet Explorer are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="9b6f8-147">Поддерживаемые операционные системы и веб-браузеры</span><span class="sxs-lookup"><span data-stu-id="9b6f8-147">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b6f8-148">Операционная система</span><span class="sxs-lookup"><span data-stu-id="9b6f8-148">Operating system</span></span></th>
<th><span data-ttu-id="9b6f8-149">Веб-браузер</span><span class="sxs-lookup"><span data-stu-id="9b6f8-149">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b6f8-150">Windows Vista с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-150">Windows Vista with Service Pack (SP) 2</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-151">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="9b6f8-151">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="9b6f8-152">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-152">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-153">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-153">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b6f8-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b6f8-154">Windows 7</span></span></p>
<p><span data-ttu-id="9b6f8-155">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-155">Windows 7 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-156">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-156">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-157">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-157">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b6f8-158">Windows Server 2008 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-158">Windows Server 2008 with Service Pack 2</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-159">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="9b6f8-159">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="9b6f8-160">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-160">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-161">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-161">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b6f8-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b6f8-162">Windows Server 2008 R2</span></span></p>
<p><span data-ttu-id="9b6f8-163">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-163">Windows Server 2008 R2 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-164">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-164">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-165">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-165">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="response-group-agent-console"></a><span data-ttu-id="9b6f8-166">Консоль агента группы ответа</span><span class="sxs-lookup"><span data-stu-id="9b6f8-166">Response Group Agent Console</span></span>

<span data-ttu-id="9b6f8-167">Консоль агента поддерживает сочетания операционной системы и веб-браузера, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-167">The agent console supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9b6f8-p108">Поддерживаются 32-разрядная или 64-разрядная версии операционных систем. Поддерживаются только 32-разрядные версии Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9b6f8-p108">32-bit or 64-bit versions of the operating systems are supported. Only 32-bit versions of Internet Explorer are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="9b6f8-170">Поддерживаемые операционные системы и веб-браузеры</span><span class="sxs-lookup"><span data-stu-id="9b6f8-170">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b6f8-171">Операционная система</span><span class="sxs-lookup"><span data-stu-id="9b6f8-171">Operating system</span></span></th>
<th><span data-ttu-id="9b6f8-172">Веб-браузер</span><span class="sxs-lookup"><span data-stu-id="9b6f8-172">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b6f8-173">Windows Vista с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-173">Windows Vista with Service Pack (SP) 2</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-174">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="9b6f8-174">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="9b6f8-175">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-175">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-176">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-176">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b6f8-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b6f8-177">Windows 7</span></span></p>
<p><span data-ttu-id="9b6f8-178">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-178">Windows 7 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-179">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-179">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-180">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-180">Internet Explorer 9 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-181">Firefox 10.0</span><span class="sxs-lookup"><span data-stu-id="9b6f8-181">Firefox 10.0</span></span></p>
<p><span data-ttu-id="9b6f8-182">Chrome 18.0</span><span class="sxs-lookup"><span data-stu-id="9b6f8-182">Chrome 18.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b6f8-183">Windows Server 2008 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-183">Windows Server 2008 with Service Pack 2</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-184">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="9b6f8-184">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="9b6f8-185">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-185">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-186">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-186">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b6f8-187">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b6f8-187">Windows Server 2008 R2</span></span></p>
<p><span data-ttu-id="9b6f8-188">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-188">Windows Server 2008 R2 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="9b6f8-189">Internet Explorer 8 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-189">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-190">Internet Explorer 9 (основной режим)</span><span class="sxs-lookup"><span data-stu-id="9b6f8-190">Internet Explorer 9 (native mode)</span></span></p>
<p><span data-ttu-id="9b6f8-191">Firefox 10.0</span><span class="sxs-lookup"><span data-stu-id="9b6f8-191">Firefox 10.0</span></span></p>
<p><span data-ttu-id="9b6f8-192">Chrome 18.0</span><span class="sxs-lookup"><span data-stu-id="9b6f8-192">Chrome 18.0</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="9b6f8-193">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b6f8-193">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

