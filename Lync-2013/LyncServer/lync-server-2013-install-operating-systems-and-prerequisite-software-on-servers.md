---
title: Установка операционных систем и необходимого программного обеспечения на серверы
description: Установка операционной системы и необходимого программного обеспечения на серверы.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install operating systems and prerequisite software on servers
ms:assetid: 055991e0-5aeb-43fc-a7ba-d4b02316d73b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398103(v=OCS.15)
ms:contentKeyID: 48183288
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2bae9e57db9c2f1d3f3bde7ce9cc7071b73aa01d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427175"
---
# <a name="install-operating-systems-and-prerequisite-software-on-servers-for-lync-server-2013"></a><span data-ttu-id="a6de6-103">Установка операционных систем и необходимого программного обеспечения на серверы для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6de6-103">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6de6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6de6-104">

<span> </span></span></span>

<span data-ttu-id="a6de6-105">_**Тема последнего изменения:** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="a6de6-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="a6de6-106">После того как вы настроили аппаратную и системную инфраструктуру, вам нужно установить соответствующие операционные системы и обновления Windows в дополнение ко всем остальным обязательным программам на каждом сервере, который вы развертываете.</span><span class="sxs-lookup"><span data-stu-id="a6de6-106">After you have set up the hardware and system infrastructure, you need to install the appropriate Windows operating systems and updates, in addition to all other prerequisite software on each server that you are deploying.</span></span> <span data-ttu-id="a6de6-107">Сюда входят все серверные роли Lync Server 2013 и любые дополнительные серверы инфраструктуры или серверы SQL Server, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="a6de6-107">This includes each Lync Server 2013 server role and any additional infrastructure servers or servers running SQL Server that are required for your deployment.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="a6de6-108">В этом разделе описывается установка операционной системы и необходимого программного обеспечения для внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="a6de6-108">This section describes installation of operating systems and prerequisite software for internal servers.</span></span> <span data-ttu-id="a6de6-109">Если вы развертываете пограничные серверы для поддержки внешних пользователей, вам также потребуется установить операционную систему и необходимое программное обеспечение для этих серверов, в том числе на пограничные серверы и обратное прокси-серверы.</span><span class="sxs-lookup"><span data-stu-id="a6de6-109">If you are deploying Edge Servers to support external user access, you also need to install operating systems and prerequisite software for those servers, including Edge Servers and reverse proxy servers.</span></span> <span data-ttu-id="a6de6-110">Подробнее о том, как подготовить серверы к поддержке внешних пользователей, можно найти в разделе <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Подготовка к установке серверов в демилитаризованной зоне для Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="a6de6-110">For details about preparing servers to support external user access, see <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Preparing for installation of servers in the perimeter network for Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="install-windows-operating-systems-on-servers"></a><span data-ttu-id="a6de6-111">Установка операционных систем Windows на серверах</span><span class="sxs-lookup"><span data-stu-id="a6de6-111">Install Windows Operating Systems on Servers</span></span>

<span data-ttu-id="a6de6-112">На каждом сервере, который вы развертываете, установите соответствующую операционную систему Windows, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="a6de6-112">On each server that you are deploying, install the appropriate Windows operating system as follows:</span></span>

  - <span data-ttu-id="a6de6-113">**Серверы, на которых запущен Lync Server 2013**   Сведения о требованиях к операционной системе для серверов, на которых работает Lync Server 2013, можно найти в документации поддержка [серверов и инструментальных средств операционной системы в Lync server 2013](lync-server-2013-server-and-tools-operating-system-support.md) .</span><span class="sxs-lookup"><span data-stu-id="a6de6-113">**Servers running Lync Server 2013**   For details about the operating system requirements for servers running Lync Server 2013, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="a6de6-114">**Серверы баз данных**   Сведения о требованиях к операционной системе для серверов баз данных, включая серверную базу данных, архивированную базу данных и контрольную базу данных, можно найти в документации по SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a6de6-114">**Database servers**   For details about operating system requirements for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server documentation.</span></span> <span data-ttu-id="a6de6-115">Сведения о SQL Server 2012 можно найти в книге SQL Server 2012 на сайте [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="a6de6-115">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="a6de6-116">Если вы устанавливаете Lync Server 2013 на Windows Server &nbsp; 2008 &nbsp; R2 с пакетом обновления 1 (SP1), необходимо сначала установить обновление, описанное в статье Microsoft Knowledge on 2646886, исправление: повреждение кучи возникает, когда модуль вызывает метод INSERTENTITYBODY в службах IIS 7,5 ", по адресу. <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp kbid = 2646886</A>.</span><span class="sxs-lookup"><span data-stu-id="a6de6-116">If you are installing Lync Server 2013 on Windows Server&nbsp;2008&nbsp;R2 with SP1, you must first install the update described in the Microsoft Knowledge Based article 2646886, “FIX: Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5”, at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=2646886</A>.</span></span><BR><span data-ttu-id="a6de6-117">Кроме того, необходимо внести изменения в реестр, как описано в статье KB, <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">события с кодами 32402, 61045 записываются в журнал на Lync server 2013 серверы переднего плана, установленные в Windows server 2012 R2</A>.</span><span class="sxs-lookup"><span data-stu-id="a6de6-117">You must also modify the registry as described in the KB article, <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Event IDs 32402, 61045 are logged in Lync Server 2013 Front End servers that are installed in Windows Server 2012 R2</A>.</span></span>



</div>

</div>

<div>

## <a name="install-windows-update-on-servers"></a><span data-ttu-id="a6de6-118">Установка центра обновления Windows на серверах</span><span class="sxs-lookup"><span data-stu-id="a6de6-118">Install Windows Update on Servers</span></span>

<span data-ttu-id="a6de6-119">Установите на каждом сервере следующие обновления из центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="a6de6-119">Install the following updates from Windows Update on each server:</span></span>

  - <span data-ttu-id="a6de6-120">**Обновление Windows для серверов с Lync Server 2013**   Подробные сведения об обновлениях из центра обновления Windows, необходимых для серверов с Lync Server 2013, приведены в разделе [Дополнительные требования к программному обеспечению для Lync server 2013](lync-server-2013-additional-software-requirements.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="a6de6-120">**Windows Update for servers running Lync Server 2013**   For details about the updates from Windows Update that are required for servers running Lync Server 2013, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="a6de6-121">**Серверы баз данных**   Сведения об обновлениях, которые необходимы для серверов баз данных, включая серверную базу данных, архивированную базу данных и контрольную базу данных, можно найти в документации по SQL Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a6de6-121">**Database servers**   For details about the updates from Windows Update that are required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation.</span></span> <span data-ttu-id="a6de6-122">Сведения о SQL Server 2012 можно найти в книге SQL Server 2012 на сайте [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="a6de6-122">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

</div>

<div>

## <a name="install-other-prerequisite-software-on-servers"></a><span data-ttu-id="a6de6-123">Установка другого программного обеспечения на серверах</span><span class="sxs-lookup"><span data-stu-id="a6de6-123">Install Other Prerequisite Software on Servers</span></span>

<span data-ttu-id="a6de6-124">Для установки Lync Server 2013 требуется установить следующее дополнительное программное обеспечение на серверах:</span><span class="sxs-lookup"><span data-stu-id="a6de6-124">Lync Server 2013 requires the installation of the following additional software on servers:</span></span>

  - <span data-ttu-id="a6de6-125">**Необходимое программное обеспечение для серверов с Lync Server 2013**   Дополнительные требования к программному обеспечению для серверов, на которых работает Lync Server 2013, зависят от того, какая роль сервера развертывается.</span><span class="sxs-lookup"><span data-stu-id="a6de6-125">**Prerequisite software for servers running Lync Server 2013**   The additional software prerequisites for servers running Lync Server 2013 depend on the server role being deployed.</span></span> <span data-ttu-id="a6de6-126">Подробные сведения о конкретных требованиях к программному обеспечению для каждого сервера можно найти в разделе [Дополнительные требования к программному обеспечению для Lync server 2013](lync-server-2013-additional-software-requirements.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="a6de6-126">For details about the specific software requirements for each server, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="a6de6-127">**Windows Identity Foundation**   Для поддержки сценариев проверки подлинности серверов на сервере Lync Server 2013 требуется установка Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="a6de6-127">**Windows Identity Foundation**   Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server-to-server authentication scenarios.</span></span> <span data-ttu-id="a6de6-128">Чтобы убедиться, что она уже установлена на вашем компьютере, откройте панель управления, выберите пункты **программы и компоненты**, **Просмотреть установленные обновления** и просмотрите раздел **Microsoft Windows**.</span><span class="sxs-lookup"><span data-stu-id="a6de6-128">To verify that it has already been installed on your computer, go to Control Panel, click **Programs and Features**, **View installed updates**, and look under **Microsoft Windows**.</span></span> <span data-ttu-id="a6de6-129">Подробнее об установке Windows Identity Foundation можно узнать в статье [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="a6de6-129">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="a6de6-130">**Microsoft .NET Framework 4,5**   Для Lync Server 2013 требуется 64-разрядная версия Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="a6de6-130">**Microsoft .NET Framework 4.5**   The 64-bit edition of Microsoft .NET Framework 4.5 is required for Lync Server 2013.</span></span>

  - <span data-ttu-id="a6de6-131">**Необходимое программное обеспечение для серверов баз данных**   Подробные сведения о Windows Update, необходимых для серверов баз данных, включая серверную базу данных, архивированную базу данных и контрольную базу данных, можно найти в документации по SQL Server 2012 по адресу [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="a6de6-131">**Prerequisite software for database servers**   For details about the Windows Update required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="a6de6-132">Lync Server 2013 автоматически устанавливает Microsoft SQL Server 2012 Express на каждом стандартном сервере выпуска и каждый сервер, на котором работает Lync Server 2013, на котором расположено локальное хранилище конфигураций.</span><span class="sxs-lookup"><span data-stu-id="a6de6-132">Lync Server 2013 automatically installs Microsoft SQL Server 2012 Express on each Standard Edition server and each server running Lync Server 2013 on which the local configuration store is located.</span></span>

    
    </div>

  - <span data-ttu-id="a6de6-133">**Среда выполнения формата Windows Media**   Все серверы переднего плана и стандартные серверы выпусков, на которых будут развертываться конференции, должны иметь установленную среду выполнения формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a6de6-133">**Windows Media Format Runtime**   All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed.</span></span> <span data-ttu-id="a6de6-134">Для работы с файлами Windows Media Audio (WMA), которые воспринимаются приложениями для приема, объявления и ответа, воспроизводится для объявлений и музыкальных файлов, которые требуются в среде выполнения формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a6de6-134">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="a6de6-135">Для Windows Server 2012 и Windows Server 2012 R2 среда выполнения формата Windows Media устанавливается вместе с Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a6de6-135">For Windows Server 2012 and Windows Server 2012 R2 the Windows Media Format Runtime installs with Microsoft Media Foundation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="a6de6-136">Для Windows Server &nbsp; 2008 и Windows server &nbsp; 2008 &nbsp; R2 среда выполнения формата Windows Media устанавливается в составе рабочего стола Windows.</span><span class="sxs-lookup"><span data-stu-id="a6de6-136">For Windows Server&nbsp;2008 and Windows Server&nbsp;2008&nbsp;R2 the Windows Media Format Runtime installs as part of the Windows Desktop Experience.</span></span> <span data-ttu-id="a6de6-137">Перед установкой Lync Server 2013 рекомендуется установить возможности рабочего стола Windows.</span><span class="sxs-lookup"><span data-stu-id="a6de6-137">It is recommended that you install Windows Desktop Experience before you install Lync Server 2013.</span></span> <span data-ttu-id="a6de6-138">Если Lync Server 2013 не находит это программное обеспечение на сервере, вам будет предложено установить его, а затем необходимо перезапустить сервер, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="a6de6-138">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

    
    <span data-ttu-id="a6de6-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6de6-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

