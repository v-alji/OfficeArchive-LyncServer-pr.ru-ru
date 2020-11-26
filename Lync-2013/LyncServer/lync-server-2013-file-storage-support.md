---
title: 'Lync Server 2013: поддержка хранения файлов'
description: Поддержка хранения файлов в Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: File storage support
ms:assetid: ed66430d-3c19-4267-938c-956a51005073
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399073(v=OCS.15)
ms:contentKeyID: 48185743
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03b7c3379c6aad6283f6a55b991ebaec50044bda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428183"
---
# <a name="file-storage-support-in-lync-server-2013"></a><span data-ttu-id="4c25f-103">Поддержка хранения файлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c25f-103">File storage support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c25f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c25f-104">

<span> </span></span></span>

<span data-ttu-id="4c25f-105">_**Тема последнего изменения:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="4c25f-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="4c25f-106">Lync Server 2013 использует одно и то же хранилище файлов для хранения всех файлов.</span><span class="sxs-lookup"><span data-stu-id="4c25f-106">Lync Server 2013 uses the same file store for all file storage.</span></span> <span data-ttu-id="4c25f-107">Поддержка хранения файлов включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="4c25f-107">File storage support includes the following:</span></span>

  - <span data-ttu-id="4c25f-108">Файловый общий доступ на запоминающем устройстве (DAS) или в сети хранения данных (SAN), включая распределенную файловую систему (DFS), а также на резервный массив независимых дисков (RAID) для хранения файлов.</span><span class="sxs-lookup"><span data-stu-id="4c25f-108">A file share on either direct attached storage (DAS) or a storage area network (SAN), including Distributed File System (DFS), and on a redundant array of independent disks (RAID) for file stores.</span></span> <span data-ttu-id="4c25f-109">Сведения о требованиях к хранению можно найти в статьях [технические требования к серверам переднего плана, мгновенным сообщениям и сведениям о присутствии в Lync server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) , а также [о требованиях к оборудованию и программному обеспечению для директора в Lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md)</span><span class="sxs-lookup"><span data-stu-id="4c25f-109">For details about storage requirements, see [Technical requirements for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) and [Hardware and software requirements for the Director in Lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md) in the Planning documentation.</span></span> <span data-ttu-id="4c25f-110">Подробные сведения о DFS для операционной системы Windows Server 2008 можно найти в пошаговом руководстве по DFS для Windows Server 2008 по адресу [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) .</span><span class="sxs-lookup"><span data-stu-id="4c25f-110">For details about DFS for Windows Server 2008 operating system, see the DFS Step-by-Step Guide for Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835).</span></span>

  - <span data-ttu-id="4c25f-111">Общий кластер для общего доступа к файлам.</span><span class="sxs-lookup"><span data-stu-id="4c25f-111">A shared cluster for the file share.</span></span> <span data-ttu-id="4c25f-112">Если вы пользуетесь общим кластером, вы должны использовать кластерные серверы под управлением Windows Server 2008 или Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4c25f-112">If you use a shared cluster, you should use cluster servers running Windows Server 2008 or Windows Server 2008 R2.</span></span> <span data-ttu-id="4c25f-113">Использование серверов кластера, работающих под управлением более ранней версии Windows, может привести к проблемам с разрешениями, которые не позволяют получить доступ к некоторым функциям.</span><span class="sxs-lookup"><span data-stu-id="4c25f-113">Using cluster servers running an older version of Windows may result in permission issues that prevent some features from being available.</span></span> <span data-ttu-id="4c25f-114">Для создания общих файловых ресурсов используйте администратор кластеров.</span><span class="sxs-lookup"><span data-stu-id="4c25f-114">Use the Cluster Administrator to create the file shares.</span></span> <span data-ttu-id="4c25f-115">Подробнее об использовании администратора кластера можно найти в статье 284838 базы знаний Майкрософт, посвященной созданию общего файлового файла кластера сервера с Cluster.exe " [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899) .</span><span class="sxs-lookup"><span data-stu-id="4c25f-115">For details about using the Cluster Administrator, see Microsoft Knowledge Base article 284838, "How to Create a Server Cluster File Share with Cluster.exe" at [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899).</span></span>

<span data-ttu-id="4c25f-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c25f-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

