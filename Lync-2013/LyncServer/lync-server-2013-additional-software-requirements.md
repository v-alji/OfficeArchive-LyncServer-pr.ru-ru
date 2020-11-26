---
title: 'Lync Server 2013: дополнительные требования к программному обеспечению'
description: 'Lync Server 2013: дополнительные требования к программному обеспечению.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Additional software requirements
ms:assetid: 87b318e3-03ae-41f7-af5e-29bb294f6af0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398686(v=OCS.15)
ms:contentKeyID: 48184731
ms.date: 12/09/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbc36f23a2246c9d653e47954064182c756f0dff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443156"
---
# <a name="additional-software-requirements-for-lync-server-2013"></a><span data-ttu-id="8ecfa-103">Дополнительные требования к программному обеспечению для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ecfa-103">Additional software requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ecfa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ecfa-104">

<span> </span></span></span>

<span data-ttu-id="8ecfa-105">_**Тема последнего изменения:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="8ecfa-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="8ecfa-106">В дополнение к требованиям к оборудованию и операционной системе для серверных платформ Lync Server 2013 требует установки дополнительного программного обеспечения на серверах, которые вы развертываете.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-106">In addition to the hardware and operating system requirements for server platforms, Lync Server 2013 requires the installation of additional software on the servers that you deploy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8ecfa-107">Сведения о требованиях к платформе для серверов Lync Server можно найти в разделе <A href="lync-server-2013-server-hardware-platforms.md">аппаратные платформы сервера для Lync server 2013</A> и <A href="lync-server-2013-server-and-tools-operating-system-support.md">серверных и инструментальных средств, поддерживаемых операционной системой в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-107">For details about the platform requirements for servers running Lync Server, see <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A> and <A href="lync-server-2013-server-and-tools-operating-system-support.md">Server and tools operating system support in Lync Server 2013</A>.</span></span> <span data-ttu-id="8ecfa-108">Дополнительные сведения о требованиях к системе для клиентских компьютеров и устройств можно найти <A href="lync-server-2013-planning-for-clients-and-devices.md">в разделе Планирование клиентов и устройств в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-108">For details about system requirements for client computers and devices, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span> <span data-ttu-id="8ecfa-109">Сведения о требованиях к программному обеспечению для администрирования описаны <A href="lync-server-2013-administrative-tools-software-requirements.md">в разделе Требования к программному обеспечению для администраторов в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-109">For details about software requirements for administrative tools, see <A href="lync-server-2013-administrative-tools-software-requirements.md">Administrative tools software requirements in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="additional-software-necessary-for-all-internal-server-roles"></a><span data-ttu-id="8ecfa-110">Дополнительное программное обеспечение, необходимое для всех внутренних серверных ролей</span><span class="sxs-lookup"><span data-stu-id="8ecfa-110">Additional Software Necessary for All Internal Server Roles</span></span>

<span data-ttu-id="8ecfa-111">В этом разделе перечислены программы, необходимые для всех внутренних ролей сервера, которые являются всеми ролями сервера Lync Server, кроме пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-111">This section lists software necessary on all internal server roles, which are all Lync Server server roles except for Edge Server.</span></span> <span data-ttu-id="8ecfa-112">Требования к пограничным серверам и пулам Edge перечислены ниже в разделе **дополнительное программное обеспечение для пограничного сервера**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-112">The requirements for the Edge Servers and Edge pools are listed later in this topic under **Additional Software for Edge Servers**.</span></span>

</div>

<div>

## <a name="windows-powershell-30"></a><span data-ttu-id="8ecfa-113">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="8ecfa-113">Windows PowerShell 3.0</span></span>

<span data-ttu-id="8ecfa-114">На каждом сервере, на котором работает Lync Server 2013, должны быть установлены правильные выпуски Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-114">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="8ecfa-115">Подробные сведения можно найти в разделе [Установка Windows PowerShell 3,0 для Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="8ecfa-115">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

</div>

<div>

## <a name="microsoft-net-framework-45"></a><span data-ttu-id="8ecfa-116">Платформа Microsoft .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-116">Microsoft .NET Framework 4.5</span></span>

<span data-ttu-id="8ecfa-117">Lync Server требует Microsoft .NET Framework 4,5 для всех внутренних серверных ролей и на любом компьютере, на котором выполняются средства администрирования сервера Lync Server или Microsoft Lync Server 2013; средство планирования.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-117">Lync Server requires Microsoft .NET Framework 4.5 on all internal server roles and on any computer where you will run the Lync Server administrative tools or Microsoft Lync Server 2013, Planning Tool.</span></span> <span data-ttu-id="8ecfa-118">Для Lync Server 2013 необходимо вручную установить 64-разрядную версию Microsoft .NET Framework 4,5 на сервере перед установкой Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-118">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="8ecfa-119">Чтобы установить ее вручную, скачайте Microsoft .NET 4,5 Framework из центра загрузки Майкрософт по адресу [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="8ecfa-119">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

<div>

## <a name="installing-microsoft-net-framework-45-on-servers-running-windows-server-2012"></a><span data-ttu-id="8ecfa-120">Установка Microsoft .NET Framework 4,5 на серверах под управлением Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ecfa-120">Installing Microsoft .NET Framework 4.5 on Servers Running Windows Server 2012</span></span>

<span data-ttu-id="8ecfa-121">При установке Microsoft .NET Framework 4,5 на сервер, на котором работают Lync Server 2013 и Windows Server 2012, необходимо выполнить одно из дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-121">When you install Microsoft .NET Framework 4.5 on servers that will run Lync Server 2013 and Windows Server 2012, you must perform one additional step.</span></span> <span data-ttu-id="8ecfa-122">После установки .NET Framework 4,5 Используйте Диспетчер серверов для установки активации HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-122">After .NET Framework 4.5 is installed, use Server Manager to install HTTP Activation.</span></span>

<span data-ttu-id="8ecfa-123">**Установка активации .NET 4,5 HTTP в Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8ecfa-123">**To Install .NET 4.5 HTTP Activation on Windows Server 2012**</span></span>

1.  <span data-ttu-id="8ecfa-124">В меню **Пуск** выберите пункт **программы**, а затем — **Администрирование**, а затем — **Диспетчер серверов**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-124">From the **Start** menu, click **Programs**, then click **Administrative Tools**, then click **Server Manager**.</span></span>

2.  <span data-ttu-id="8ecfa-125">В диспетчере серверов в разделе **Сводка по компонентам** выберите **Добавить функции**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-125">In Server Manager, under **Features Summary**, choose **Add Features**.</span></span>

3.  <span data-ttu-id="8ecfa-126">Разверните **.NET Framework 4,5**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-126">Expand **.NET Framework 4.5**.</span></span>

4.  <span data-ttu-id="8ecfa-127">Выберите **Активация WCF** , если она еще не выбрана.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-127">Select **WCF Activation** if it isn’t already selected.</span></span> <span data-ttu-id="8ecfa-128">Затем выберите **Активация HTTP**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-128">Then select **HTTP Activation**.</span></span>

5.  <span data-ttu-id="8ecfa-129">Нажмите кнопку **Далее** и следуйте инструкциям, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-129">Click **Next** and follow the prompts to finish the installation.</span></span>

</div>

</div>

<div>

## <a name="windows-identity-foundation"></a><span data-ttu-id="8ecfa-130">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="8ecfa-130">Windows Identity Foundation</span></span>

<span data-ttu-id="8ecfa-131">Для поддержки сценариев проверки подлинности сервера и **сервера в Lync** Server 2013 необходимо установить Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-131">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="8ecfa-132">Для Windows Server 2008 R2 и Windows Server 2012 требуется выполнить различные процедуры для установки Windows Identify Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-132">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="8ecfa-133">Выберите серверную операционную систему из следующего списка:</span><span class="sxs-lookup"><span data-stu-id="8ecfa-133">Select your server operating system from the following list:</span></span>

  - <span data-ttu-id="8ecfa-134">Windows Server 2008 R2 для Windows Server 2008 R2 — убедитесь, что она уже установлена на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-134">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="8ecfa-135">Для этого выберите элемент **Установка и удаление программ**, **Просмотрите установленные обновления** и найдите в разделе **Windows** **удостоверение для Windows (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-135">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="8ecfa-136">Подробнее об установке Windows Identity Foundation можно узнать в статье [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="8ecfa-136">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="8ecfa-137">Windows Server 2012 для Windows Server 2012 вы используете **Диспетчер серверов** для установки Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-137">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="8ecfa-138">В **мастере добавления ролей и компонентов** в диспетчере серверов выберите **компоненты**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-138">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="8ecfa-139">В списке выберите **Windows Identity Foundation 3,5** .</span><span class="sxs-lookup"><span data-stu-id="8ecfa-139">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="8ecfa-140">Нажмите кнопку **Далее**, а затем — **установить**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-140">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="additional-software-for-all-front-end-servers-and-standard-edition-servers"></a><span data-ttu-id="8ecfa-141">Дополнительное программное обеспечение для всех серверов переднего плана и стандартных серверов выпусков</span><span class="sxs-lookup"><span data-stu-id="8ecfa-141">Additional Software for All Front End Servers and Standard Edition Servers</span></span>

<span data-ttu-id="8ecfa-142">На всех серверах переднего плана и стандартных серверах выпусков также должны выполняться службы IIS с определенными модулями.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-142">All Front End Servers and Standard Edition servers must also run Internet Information Services (IIS) with certain modules.</span></span> <span data-ttu-id="8ecfa-143">Кроме того, все серверы переднего плана и серверы стандартных выпусков, для которых развернута Конференц-связь, приложение для присоединения к приостановке, объявление и группа ответа, должны запускать среду выполнения формата Windows Media</span><span class="sxs-lookup"><span data-stu-id="8ecfa-143">Additionally, all Front End Servers and Standard Edition servers where conferencing, Call Park application, Announcement, or Response Groups are deployed must run Windows Media Format Runtime.</span></span>

<div>

## <a name="internet-information-services-iis"></a><span data-ttu-id="8ecfa-144">Службы IIS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-144">Internet Information Services (IIS)</span></span>

<span data-ttu-id="8ecfa-145">Для серверов переднего плана и стандартных серверов выпусков должны выполняться службы IIS со следующими модулями:</span><span class="sxs-lookup"><span data-stu-id="8ecfa-145">Front End Servers and Standard Edition servers must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="8ecfa-146">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="8ecfa-146">Static Content</span></span>

  - <span data-ttu-id="8ecfa-147">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8ecfa-147">Default Document</span></span>

  - <span data-ttu-id="8ecfa-148">Ошибки HTTP</span><span class="sxs-lookup"><span data-stu-id="8ecfa-148">HTTP Errors</span></span>

  - <span data-ttu-id="8ecfa-149">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="8ecfa-149">ASP.NET</span></span>

  - <span data-ttu-id="8ecfa-150">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="8ecfa-150">.NET Extensibility</span></span>

  - <span data-ttu-id="8ecfa-151">Расширения ISAPI (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="8ecfa-151">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="8ecfa-152">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="8ecfa-152">ISAPI Filters</span></span>

  - <span data-ttu-id="8ecfa-153">Ведение журнала HTTP</span><span class="sxs-lookup"><span data-stu-id="8ecfa-153">HTTP Logging</span></span>

  - <span data-ttu-id="8ecfa-154">Средства ведения журналов</span><span class="sxs-lookup"><span data-stu-id="8ecfa-154">Logging Tools</span></span>

  - <span data-ttu-id="8ecfa-155">Трассировка</span><span class="sxs-lookup"><span data-stu-id="8ecfa-155">Tracing</span></span>

  - <span data-ttu-id="8ecfa-156">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="8ecfa-156">Windows Authentication</span></span>

  - <span data-ttu-id="8ecfa-157">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="8ecfa-157">Request Filtering</span></span>

  - <span data-ttu-id="8ecfa-158">Сжатие статического содержимого</span><span class="sxs-lookup"><span data-stu-id="8ecfa-158">Static Content Compression</span></span>

  - <span data-ttu-id="8ecfa-159">Сжатие динамического содержимого</span><span class="sxs-lookup"><span data-stu-id="8ecfa-159">Dynamic Content Compression</span></span>

  - <span data-ttu-id="8ecfa-160">Консоль управления IIS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-160">IIS Management Console</span></span>

  - <span data-ttu-id="8ecfa-161">Сценарии и средства управления для служб IIS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-161">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="8ecfa-162">Анонимная проверка подлинности (устанавливается по умолчанию при установке IIS).</span><span class="sxs-lookup"><span data-stu-id="8ecfa-162">Anonymous Authentication (this is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="8ecfa-163">Проверка подлинности с сопоставлением сертификатов клиентов</span><span class="sxs-lookup"><span data-stu-id="8ecfa-163">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="windows-media-format-runtime-and-windows-desktop-experience"></a><span data-ttu-id="8ecfa-164">Среда выполнения формата Windows Media и возможности рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="8ecfa-164">Windows Media Format Runtime and Windows Desktop Experience</span></span>

<span data-ttu-id="8ecfa-165">**Возможности рабочего стола Windows** Все серверы переднего плана и стандартные серверы выпусков, на которых будет развернута конференция, должны иметь установленную среду выполнения формата Windows Media (за исключением Windows Server 2012, установленной в составе рабочего стола Windows.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-165">**Windows Desktop Experience** All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed, which, except for Windows Server 2012 is installed as part of the Windows desktop experience.</span></span> <span data-ttu-id="8ecfa-166">Для Windows Server 2012 требуется Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-166">Windows Server 2012 requires Microsoft Media Foundation.</span></span> <span data-ttu-id="8ecfa-167">Для работы с файлами Windows Media Audio (WMA), которые воспринимаются приложениями для приема, объявления и ответа, воспроизводится для объявлений и музыкальных файлов, которые требуются в среде выполнения формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-167">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>

<span data-ttu-id="8ecfa-168">Перед установкой Lync Server 2013 рекомендуется установить возможности рабочего стола Windows.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-168">We recommend that you install Windows desktop experience before you install Lync Server 2013.</span></span> <span data-ttu-id="8ecfa-169">Если Lync Server 2013 не находит это программное обеспечение на сервере, вам будет предложено установить его, а затем необходимо перезапустить сервер, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-169">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

</div>

</div>

<div>

## <a name="additional-software-for-front-end-servers-and-standard-edition-servers-running-on-windows-server-2012"></a><span data-ttu-id="8ecfa-170">Дополнительное программное обеспечение для серверов переднего плана и серверов Standard Edition, работающих под управлением Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ecfa-170">Additional Software for Front End Servers and Standard Edition Servers Running on Windows Server 2012</span></span>

<span data-ttu-id="8ecfa-171">Для серверов с внешними интерфейсами требуется .NET 3,5, который не установлен по умолчанию в Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-171">Front End Servers require .NET 3.5, which is not installed by default on Windows Server 2012.</span></span> <span data-ttu-id="8ecfa-172">Чтобы установить его, вставьте установочный носитель Windows Server 2012 в дисковод D и введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8ecfa-172">To install it, put your Windows Server 2012 installation media in Drive D and type the following:</span></span>

    Add-WindowsFeature RSAT-ADDS, Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Compat, Desktop-Experience, Telnet-Client, BITS -Source D:\sources\sxs

<span data-ttu-id="8ecfa-173">Подробные сведения об установке .NET 3,5 на серверах под управлением Windows Server 2012 можно найти в разделе "вопросы по развертыванию Microsoft .NET Framework 3,5" <https://go.microsoft.com/fwlink/p/?linkid=275032> .</span><span class="sxs-lookup"><span data-stu-id="8ecfa-173">For details about installing .NET 3.5 on servers running Windows Server 2012, see "Microsoft .NET Framework 3.5 Deployment Considerations" at <https://go.microsoft.com/fwlink/p/?linkid=275032>.</span></span>

</div>

<div>

## <a name="additional-software-for-directors"></a><span data-ttu-id="8ecfa-174">Дополнительное программное обеспечение для режиссеров</span><span class="sxs-lookup"><span data-stu-id="8ecfa-174">Additional Software for Directors</span></span>

<span data-ttu-id="8ecfa-175">Режиссеры должны запускать службы IIS со следующими модулями:</span><span class="sxs-lookup"><span data-stu-id="8ecfa-175">Directors must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="8ecfa-176">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="8ecfa-176">Static Content</span></span>

  - <span data-ttu-id="8ecfa-177">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8ecfa-177">Default Document</span></span>

  - <span data-ttu-id="8ecfa-178">Ошибки HTTP</span><span class="sxs-lookup"><span data-stu-id="8ecfa-178">HTTP Errors</span></span>

  - <span data-ttu-id="8ecfa-179">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="8ecfa-179">ASP.NET</span></span>

  - <span data-ttu-id="8ecfa-180">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="8ecfa-180">.NET Extensibility</span></span>

  - <span data-ttu-id="8ecfa-181">Расширения ISAPI (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="8ecfa-181">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="8ecfa-182">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="8ecfa-182">ISAPI Filters</span></span>

  - <span data-ttu-id="8ecfa-183">Ведение журнала HTTP</span><span class="sxs-lookup"><span data-stu-id="8ecfa-183">HTTP Logging</span></span>

  - <span data-ttu-id="8ecfa-184">Средства ведения журналов</span><span class="sxs-lookup"><span data-stu-id="8ecfa-184">Logging Tools</span></span>

  - <span data-ttu-id="8ecfa-185">Трассировка</span><span class="sxs-lookup"><span data-stu-id="8ecfa-185">Tracing</span></span>

  - <span data-ttu-id="8ecfa-186">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="8ecfa-186">Windows Authentication</span></span>

  - <span data-ttu-id="8ecfa-187">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="8ecfa-187">Request Filtering</span></span>

  - <span data-ttu-id="8ecfa-188">Сжатие статического содержимого</span><span class="sxs-lookup"><span data-stu-id="8ecfa-188">Static Content Compression</span></span>

  - <span data-ttu-id="8ecfa-189">Консоль управления IIS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-189">IIS Management Console</span></span>

  - <span data-ttu-id="8ecfa-190">Сценарии и средства управления для служб IIS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-190">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="8ecfa-191">Анонимная проверка подлинности (устанавливается по умолчанию при установке IIS).</span><span class="sxs-lookup"><span data-stu-id="8ecfa-191">Anonymous Authentication (This is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="8ecfa-192">Проверка подлинности с сопоставлением сертификатов клиентов</span><span class="sxs-lookup"><span data-stu-id="8ecfa-192">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="additional-software-for-persistent-chat-front-end-servers"></a><span data-ttu-id="8ecfa-193">Дополнительное программное обеспечение для серверов клиентского чата с постоянным подключением</span><span class="sxs-lookup"><span data-stu-id="8ecfa-193">Additional Software for Persistent Chat Front End Servers</span></span>

<span data-ttu-id="8ecfa-194">На серверах, использующих сохраняемый чат, должны быть запущены очередь сообщений (также называемая MSMQ), которая является компонентом Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-194">Persistent Chat Front End Servers must run Message Queuing (also known as MSMQ), which is a component of Windows Server.</span></span>

<span data-ttu-id="8ecfa-195">Чтобы узнать, как включить MSMQ, [нажмите здесь.](https://technet.microsoft.com/library/cc771474.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ecfa-195">For information on enabling MSMQ, [click here.](https://technet.microsoft.com/library/cc771474.aspx)</span></span>

</div>

<div>

## <a name="additional-software-for-edge-servers"></a><span data-ttu-id="8ecfa-196">Дополнительное программное обеспечение для пограничных серверов</span><span class="sxs-lookup"><span data-stu-id="8ecfa-196">Additional Software for Edge Servers</span></span>

<span data-ttu-id="8ecfa-197">Для пограничных серверов требуется следующее программное обеспечение:</span><span class="sxs-lookup"><span data-stu-id="8ecfa-197">Edge Servers require the following software:</span></span>

  - <span data-ttu-id="8ecfa-198">На каждом сервере, на котором работает Lync Server 2013, должны быть установлены правильные выпуски Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-198">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="8ecfa-199">Подробные сведения можно найти в разделе [Установка Windows PowerShell 3,0 для Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="8ecfa-199">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

  - <span data-ttu-id="8ecfa-200">Для Lync Server требуется Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-200">Lync Server requires Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="8ecfa-201">Для Lync Server 2013, установленного в Windows Server 2008 R2, перед установкой Lync Server 2013 необходимо вручную установить версию 64-bit Microsoft .NET Framework 4,5 на сервере.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-201">For Lync Server 2013 installed on Windows Server 2008 R2, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="8ecfa-202">Чтобы установить ее вручную, скачайте Microsoft .NET 4,5 Framework из центра загрузки Майкрософт по адресу [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="8ecfa-202">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

  - <span data-ttu-id="8ecfa-203">Для поддержки сценариев проверки подлинности сервера и **сервера в Lync** Server 2013 необходимо установить Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-203">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="8ecfa-204">Для Windows Server 2008 R2 и Windows Server 2012 требуется выполнить различные процедуры для установки Windows Identify Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-204">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="8ecfa-205">Выберите серверную операционную систему из следующего списка:</span><span class="sxs-lookup"><span data-stu-id="8ecfa-205">Select your server operating system from the following list:</span></span>
    
      - <span data-ttu-id="8ecfa-206">Windows Server 2008 R2 для Windows Server 2008 R2 — убедитесь, что она уже установлена на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-206">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="8ecfa-207">Для этого выберите элемент **Установка и удаление программ**, **Просмотрите установленные обновления** и найдите в разделе **Windows** **удостоверение для Windows (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-207">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="8ecfa-208">Подробнее об установке Windows Identity Foundation можно узнать в статье [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="8ecfa-208">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>
    
      - <span data-ttu-id="8ecfa-209">Windows Server 2012 для Windows Server 2012 вы используете **Диспетчер серверов** для установки Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-209">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="8ecfa-210">В **мастере добавления ролей и компонентов** в диспетчере серверов выберите **компоненты**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-210">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="8ecfa-211">В списке выберите **Windows Identity Foundation 3,5** .</span><span class="sxs-lookup"><span data-stu-id="8ecfa-211">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="8ecfa-212">Нажмите кнопку **Далее**, а затем — **установить**.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-212">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="do-not-install-layered-socket-providers-on-media-servers"></a><span data-ttu-id="8ecfa-213">Не устанавливайте провайдеры многоуровневых соединителей на серверах мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8ecfa-213">Do Not Install Layered Socket Providers on Media Servers</span></span>

<span data-ttu-id="8ecfa-214">Не устанавливайте клиентское программное обеспечение сервера Microsoft Internet Security and Acceleration (ISA) или любое другое программное обеспечение, которое можно получить с любого другого поставщика многоуровневой службы (LSP), на любом сервере переднего плана или отдельном сервере.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-214">Do not install any Microsoft Internet Security and Acceleration (ISA) Server client software, or any other Winsock Layered Service Providers (LSP) software, on any Front End Servers or stand-alone Mediation Servers.</span></span> <span data-ttu-id="8ecfa-215">Установка этого программного обеспечения может привести к ухудшению производительности мультимедийного трафика.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-215">Installing this software could cause poor media traffic performance.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8ecfa-216">См. также</span><span class="sxs-lookup"><span data-stu-id="8ecfa-216">See Also</span></span>


[<span data-ttu-id="8ecfa-217">Программные требования для средств администрирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ecfa-217">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
  

<span data-ttu-id="8ecfa-218"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ecfa-218"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

