---
title: 'Lync Server 2013: требования для веб-конференций'
description: 'Lync Server 2013: требования для веб-конференций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Web conferencing requirements
ms:assetid: 125f847c-58ab-450f-ae43-41219fd38477
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619171(v=OCS.15)
ms:contentKeyID: 49733559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6c1fce932d3cc02ac29364d53d04ec336693e43b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398650"
---
# <a name="web-conferencing-requirements-in-lync-server-2013"></a><span data-ttu-id="fa040-103">Требования для веб-конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa040-103">Web conferencing requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa040-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa040-104">

<span> </span></span></span>

<span data-ttu-id="fa040-105">_**Тема последнего изменения:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="fa040-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="fa040-106">Если принято решение включить функции веб-конференций, должны быть спланированы следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="fa040-106">If you have chosen to enable web conferencing, you need to plan for the following:</span></span>

  - <span></span>  
    <span data-ttu-id="fa040-107">Доступ к хранилищу файлов, которое используется для хранения содержимого веб-конференций.</span><span class="sxs-lookup"><span data-stu-id="fa040-107">Access to the file store, which is used for storing web conferencing content.</span></span>

  - <span></span>  
    <span data-ttu-id="fa040-108">Взаимодействие с сервером с Office Web Apps, необходимое для предоставления доступа к файлам PowerPoint во время конференции.</span><span class="sxs-lookup"><span data-stu-id="fa040-108">Integration with Office Web Apps Server, which is necessary in order to share PowerPoint files during a conference.</span></span>

<div>

## <a name="file-store"></a><span data-ttu-id="fa040-109">файлов</span><span class="sxs-lookup"><span data-stu-id="fa040-109">File Store</span></span>

<span data-ttu-id="fa040-110">Служба веб-конференций Lync Server 2013 хранит содержимое, к которому предоставлен общий доступ во время собраний в хранилище файлов.</span><span class="sxs-lookup"><span data-stu-id="fa040-110">The Lync Server 2013 web conferencing service stores content shared during meetings in the file store.</span></span> <span data-ttu-id="fa040-111">В рамках развертывания необходимо указать общую файловую группу, которая будет использоваться в качестве хранилища файлов для пула стандартных интерфейсов сервера Standard Edition или Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="fa040-111">As part of deployment, you must specify a file share to be used as the file store for the either Standard Edition server or Enterprise Edition Front End pool.</span></span> <span data-ttu-id="fa040-112">Вы можете использовать существующую общую папку для хранения файлов или задать новую общую папку, указав полное доменное имя (FQDN) файлового сервера, для которого нужно найти общую папку, и имя папки для нового общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="fa040-112">You can use an existing file share for the file store or you can specify a new file share by specifying the fully qualified domain name (FQDN) of the file server on which the file share is to be located and a folder name for the new file share.</span></span>  <span data-ttu-id="fa040-113">Дополнительные сведения можно найти в разделе Topology Builder — определение хранилища файлов для интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa040-113">For more information, see Topology Builder – Define the File Store for the Front End.</span></span> <span data-ttu-id="fa040-114">Перед сохранением материалов в хранилище файлов службы веб-конференций эти материалы шифруются.</span><span class="sxs-lookup"><span data-stu-id="fa040-114">The web conferencing service encrypts the content before it stores the content in the file store.</span></span>

<span data-ttu-id="fa040-115">Lync Server 2013 поддерживает использование общих папок в хранилище с прямым подключением (DAS) или в сети хранения данных (SAN), включая распределенную файловую систему (DFS) и на избыточный массив независимых дисков (RAID) для хранения файлов.</span><span class="sxs-lookup"><span data-stu-id="fa040-115">Lync Server 2013 supports using file shares on either direct attached storage (DAS) or a storage area network (SAN), including Distributed File System (DFS) and on a redundant array of independent disks (RAID) for file stores.</span></span> <span data-ttu-id="fa040-116">После того как мастер развертывания Lync Server заопределил расположение общего файлового ресурса, Lync Server создаст структуру папок в общей папке, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fa040-116">After the Lync Server Deployment Wizard has defined the location of the file share, Lync Server creates a folder structure within the file share similar to:</span></span>

  - <span data-ttu-id="fa040-117">1-ApplicationServer-1</span><span class="sxs-lookup"><span data-stu-id="fa040-117">1-ApplicationServer-1</span></span>

  - <span data-ttu-id="fa040-118">1-CentralMgmt-1</span><span class="sxs-lookup"><span data-stu-id="fa040-118">1-CentralMgmt-1</span></span>

  - <span data-ttu-id="fa040-119">1-WebServices-1</span><span class="sxs-lookup"><span data-stu-id="fa040-119">1-WebServices-1</span></span>
    
      - <span data-ttu-id="fa040-120">CollabContent</span><span class="sxs-lookup"><span data-stu-id="fa040-120">CollabContent</span></span>
    
      - <span data-ttu-id="fa040-121">CollabMetadata</span><span class="sxs-lookup"><span data-stu-id="fa040-121">CollabMetadata</span></span>
    
      - <span data-ttu-id="fa040-122">DataConf</span><span class="sxs-lookup"><span data-stu-id="fa040-122">DataConf</span></span>

<span data-ttu-id="fa040-123">После этого содержимое, такое как слайды PowerPoint, доски, опросы и вложения, сохраняется службой веб-конференций в папках "CollabContent" и "CollabMetadata", расположенных в папке "WebServices".</span><span class="sxs-lookup"><span data-stu-id="fa040-123">The web conferencing service then stores content such as PowerPoint slides, whiteboards, polls, and attachments in the CollabContent and CollabMetadata folders, located in the WebServices folder.</span></span>

<span data-ttu-id="fa040-124">Администратор должен установить разрешения на доступ к общему файловому файлу, чтобы группы на часах имели необходимые права на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="fa040-124">The administrator must set permissions on the file share so that RTC groups have the necessary read and write access.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="fa040-125">Если у вас возникли ошибки с разрешениями, откройте конфигуратор топологии, скачайте и повторно опубликуйте существующую топологию.</span><span class="sxs-lookup"><span data-stu-id="fa040-125">If you encounter any errors with the permissions, open Topology Builder, download and republish the existing topology.</span></span> <span data-ttu-id="fa040-126">При публикации топологии будут проверены разрешения на доступ к файлам и при необходимости сбросить их.</span><span class="sxs-lookup"><span data-stu-id="fa040-126">Publishing the topology will verify the file share permissions and reset them if needed.</span></span>



</div>

<span data-ttu-id="fa040-127">Ниже перечислены параметры, которые можно использовать для управления хранением контента для собраний.</span><span class="sxs-lookup"><span data-stu-id="fa040-127">You can use the following settings to manage how content is stored for a meeting:</span></span>

  - <span data-ttu-id="fa040-128">**ContentGracePeriod**, который находится в [Set-CsConferencingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsConferencingConfiguration), задает время, в течение которого содержимое веб-конференций останется на сервере после завершения собрания.</span><span class="sxs-lookup"><span data-stu-id="fa040-128">**ContentGracePeriod**, located in [Set-CsConferencingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsConferencingConfiguration), sets how long web conferencing content will remain on the server after the meeting has ended.</span></span>

  - <span data-ttu-id="fa040-129">**MaxContentStorageMb**, расположенная в [Set-CsConferencingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsConferencingConfiguration), задает максимальный объем дискового пространства, разрешенного для хранения содержимого во время одного собрания.</span><span class="sxs-lookup"><span data-stu-id="fa040-129">**MaxContentStorageMb**, located in [Set-CsConferencingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsConferencingConfiguration), sets the maximum amount of file space allowed for the storage of content during a single meeting.</span></span>

<span data-ttu-id="fa040-130">**MaxUploadFileSizeMb** не ограничивает параметр отправки файлов для Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="fa040-130">**MaxUploadFileSizeMb** does not limit the file upload setting for Lync Web App.</span></span> <span data-ttu-id="fa040-131">Для приложения Lync Web App задано значение около 30MB и оно управляется файлом IIS web.config:/DataCollabWeb/Int \[ ext \] /handler/web.config. Чтобы настроить предельный размер для отправки файлов в Lync Web App, обновите его `maxRequestLength` и `maxAllowedContentLength` в файл web.config, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fa040-131">The file size upload limit for Lync Web App is set to approximately 30MB and is controlled by the IIS web.config file: /DataCollabWeb/Int\[Ext\]/Handler/web.config. To configure the file size upload limit for Lync Web App, update `maxRequestLength` and `maxAllowedContentLength` in the web.config file as shown below.</span></span>

    <system.web>
        <!-- 
            Since this handler is used to upload files to DMCU the request size (in kilobytes) 
            has to fit max allowed file size uploaded by Lync Web App client.
            The timeout has to reflect the min client bandwidth. Timeout of 600 secs 
            and 512 Kbits of *client* bandwidth would result into aproximately 30 Mbytes 
            for Lync Web App upload size limit.
        -->
          <httpRuntime maxRequestLength="500000" executionTimeout="600" />
    
    
    
                    <security>
                    <requestFiltering>
                               <requestLimits maxAllowedContentLength="524288000" />
                    </requestFiltering>
                    </security>

<span data-ttu-id="fa040-132">Вы должны обновить файл web.config для каждого сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="fa040-132">You must update the web.config file for each Front End Server.</span></span>

</div>

<div>

## <a name="office-web-apps-server"></a><span data-ttu-id="fa040-133">Сервер Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="fa040-133">Office Web Apps Server</span></span>

<span data-ttu-id="fa040-134">Для использования этих новых возможностей администраторы должны установить Office Web Apps Server, и они должны настроить Lync Server 2013 для взаимодействия с сервером Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="fa040-134">In order to use these new capabilities administrators must install Office Web Apps Server and they must configure Lync Server 2013 to communicate with Office Web Apps Server.</span></span> <span data-ttu-id="fa040-135">В этой документации содержатся сведения о том, как настроить Lync Server 2013 для работы с сервером Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="fa040-135">This documentation provides information on how to configure Lync Server 2013 to work with Office Web Apps Server.</span></span> <span data-ttu-id="fa040-136">Сведения о том, как установить Office Web Apps, приведены в этой документации.</span><span class="sxs-lookup"><span data-stu-id="fa040-136">What this documentation does not provide is information about how to install Office Web Apps Server.</span></span> <span data-ttu-id="fa040-137">Дополнительные сведения об установке можно найти на веб-сайте развертывания Microsoft Office Web Apps по адресу <https://go.microsoft.com/fwlink/p/?linkid=257525> .</span><span class="sxs-lookup"><span data-stu-id="fa040-137">For installation details, see the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span> <span data-ttu-id="fa040-138">Это руководство содержит полные сведения о предварительных требованиях для сервера Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="fa040-138">That guide includes complete prerequisite information for Office Web Apps Server.</span></span> <span data-ttu-id="fa040-139">Обратите внимание на то, что сервер Office Web Apps необходимо установить на отдельном компьютере, на котором не установлен Lync Server, SQL Server или другое серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="fa040-139">Note that Office Web Apps Server should be installed on a stand-alone computer that is not running Lync Server, SQL Server, or any other server application.</span></span> <span data-ttu-id="fa040-140">(На компьютере не должна быть установлена какая-либо версия Office.) На любом компьютере, который использовался для запуска Office Web Apps, должен быть установлен определенный набор программного обеспечения (включая .NET Framework 4,5 и Windows PowerShell 3,0).</span><span class="sxs-lookup"><span data-stu-id="fa040-140">(You must not have any version of Office installed on that computer.) Any computer used to run Office Web Apps Server must also have a specific set of software installed (including .NET Framework 4.5 and Windows PowerShell 3.0).</span></span> <span data-ttu-id="fa040-141">Эти требования, а также сведения о настройке сертификатов и информационных служб Интернета (IIS) подробно описаны на веб-сайте развертывания Microsoft Office Web Apps по адресу <https://go.microsoft.com/fwlink/p/?linkid=257525> .</span><span class="sxs-lookup"><span data-stu-id="fa040-141">These requirements, along with information about configuring certificates and Internet Information Services (IIS), are discussed in detail in the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fa040-142">См. также</span><span class="sxs-lookup"><span data-stu-id="fa040-142">See Also</span></span>


[<span data-ttu-id="fa040-143">Общие сведения о веб-конференциях в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa040-143">Overview of web conferencing in Lync Server 2013</span></span>](lync-server-2013-web-conferencing-overview.md)  
[<span data-ttu-id="fa040-144">Контрольный список развертывания для веб-конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa040-144">Deployment checklist for web conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-web-conferencing.md)  
  

<span data-ttu-id="fa040-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa040-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

