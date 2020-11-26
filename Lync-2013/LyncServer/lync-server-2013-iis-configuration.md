---
title: 'Lync Server 2013: конфигурация IIS'
description: 'Lync Server 2013: Настройка IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS configuration
ms:assetid: b458babf-bf64-43f0-8a8e-612f5096b63c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412871(v=OCS.15)
ms:contentKeyID: 48185169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 901aca7bf5ff8824b54e93754569a6ef5defc10e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427434"
---
# <a name="iis-configuration-in-lync-server-2013"></a><span data-ttu-id="661b9-103">Конфигурация IIS в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="661b9-103">IIS configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="661b9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="661b9-104">

<span> </span></span></span>

<span data-ttu-id="661b9-105">_**Тема последнего изменения:** 2014-02-17_</span><span class="sxs-lookup"><span data-stu-id="661b9-105">_**Topic Last Modified:** 2014-02-17_</span></span>

<span data-ttu-id="661b9-106">Для успешного выполнения этой процедуры необходимо войти на сервер с минимальным уровнем прав локального администратора и пользователя домена.</span><span class="sxs-lookup"><span data-stu-id="661b9-106">To successfully complete this procedure, you should be logged on to the server minimally as a local administrator and a domain user.</span></span>

<span data-ttu-id="661b9-107">Перед настройкой и установкой сервера переднего плана для Lync Server 2013, Standard Edition или первого сервера переднего плана в пуле вы устанавливаете и настраиваете роль сервера и веб-службы для служб IIS.</span><span class="sxs-lookup"><span data-stu-id="661b9-107">Before you configure and install the Front End Server for Lync Server 2013, Standard Edition or the first Front End Server in a pool, you install and configure the server role and Web Services for Internet Information Services (IIS).</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="661b9-108">Если в вашей организации требуется найти IIS и все веб-службы на диске, отличном от системного, вы можете изменить путь к папке установки для файлов Lync Server 2013 в диалоговом окне настройки при первоначальной установке средств администрирования Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="661b9-108">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box when you initially install the Lync Server 2013 Administrative tools.</span></span> <span data-ttu-id="661b9-109">Перед установкой IIS необходимо установить средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="661b9-109">You install the Administrative tools before installing IIS.</span></span> <span data-ttu-id="661b9-110">Если вы установили файлы установки по этому пути, включая OCSCore.msi, остальные файлы Lync Server 2013 будут развернуты на этом диске.</span><span class="sxs-lookup"><span data-stu-id="661b9-110">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span> <span data-ttu-id="661b9-111">Dtails можно найти в разделе <A href="lync-server-2013-install-lync-server-administrative-tools.md">Установка средств администрирования Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="661b9-111">For dtails, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A>.</span></span> <span data-ttu-id="661b9-112">Сведения о том, как переместить INETPUB, развернутый диспетчером Windows Server Manager при установке IIS, можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> .</span><span class="sxs-lookup"><span data-stu-id="661b9-112">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>



</div>

<span data-ttu-id="661b9-113">В приведенной ниже таблице указаны необходимые службы ролей IIS 7,5.</span><span class="sxs-lookup"><span data-stu-id="661b9-113">The following table indicates the required IIS 7.5 role services.</span></span>

### <a name="iis-75-role-services"></a><span data-ttu-id="661b9-114">Службы ролей IIS 7,5</span><span class="sxs-lookup"><span data-stu-id="661b9-114">IIS 7.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="661b9-115">Заголовок роли</span><span class="sxs-lookup"><span data-stu-id="661b9-115">Role Heading</span></span></th>
<th><span data-ttu-id="661b9-116">Служба ролей</span><span class="sxs-lookup"><span data-stu-id="661b9-116">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="661b9-117">Стандартные компоненты HTTP установлены</span><span class="sxs-lookup"><span data-stu-id="661b9-117">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="661b9-118">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="661b9-118">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-119">Стандартные компоненты HTTP установлены</span><span class="sxs-lookup"><span data-stu-id="661b9-119">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="661b9-120">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="661b9-120">Default document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-121">Стандартные компоненты HTTP установлены</span><span class="sxs-lookup"><span data-stu-id="661b9-121">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="661b9-122">Ошибки HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-122">HTTP errors</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-123">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-123">Application development</span></span></p></td>
<td><p><span data-ttu-id="661b9-124">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="661b9-124">ASP.NET</span></span></p>
<p><span data-ttu-id="661b9-125">Для Windows Server 2012 также требуется ASP. NET 4.5</span><span class="sxs-lookup"><span data-stu-id="661b9-125">Windows Server 2012 also requires ASP.NET4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-126">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-126">Application development</span></span></p></td>
<td><p><span data-ttu-id="661b9-127">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="661b9-127">.NET extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-128">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-128">Application development</span></span></p></td>
<td><p><span data-ttu-id="661b9-129">Расширения ISAPI (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="661b9-129">Internet Server API (ISAPI) extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-130">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-130">Application development</span></span></p></td>
<td><p><span data-ttu-id="661b9-131">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="661b9-131">ISAPI filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-132">Исправность и диагностика</span><span class="sxs-lookup"><span data-stu-id="661b9-132">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="661b9-133">Ведение журнала HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-133">HTTP logging</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-134">Исправность и диагностика</span><span class="sxs-lookup"><span data-stu-id="661b9-134">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="661b9-135">Средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="661b9-135">Logging tools</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-136">Исправность и диагностика</span><span class="sxs-lookup"><span data-stu-id="661b9-136">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="661b9-137">Трассировка</span><span class="sxs-lookup"><span data-stu-id="661b9-137">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-138">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-138">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-139">Анонимная проверка подлинности (установлен и включен по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="661b9-139">Anonymous authentication (installed and enabled by default)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-140">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-140">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-141">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="661b9-141">Windows authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-142">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-142">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-143">Проверка подлинности сопоставления сертификатов клиентов</span><span class="sxs-lookup"><span data-stu-id="661b9-143">Client Certificate Mapping authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-144">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-144">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-145">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="661b9-145">Request filtering</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-146">Производительность</span><span class="sxs-lookup"><span data-stu-id="661b9-146">Performance</span></span></p></td>
<td><p><span data-ttu-id="661b9-147">Сжатие статического содержимого</span><span class="sxs-lookup"><span data-stu-id="661b9-147">Static content compression</span></span></p>
<p><span data-ttu-id="661b9-148">Сжатие динамического содержимого</span><span class="sxs-lookup"><span data-stu-id="661b9-148">Dynamic content compression</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-149">Средства управления</span><span class="sxs-lookup"><span data-stu-id="661b9-149">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="661b9-150">Консоль управления IIS</span><span class="sxs-lookup"><span data-stu-id="661b9-150">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-151">Средства управления</span><span class="sxs-lookup"><span data-stu-id="661b9-151">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="661b9-152">Сценарии и средства управления для служб IIS</span><span class="sxs-lookup"><span data-stu-id="661b9-152">IIS Management Scripts and Tools</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="661b9-153">В операционной системе Windows Server 2008 R2 с пакетом обновления 1 (SP1) можно использовать Windows PowerShell 2,0.</span><span class="sxs-lookup"><span data-stu-id="661b9-153">On the Windows Server 2008 R2 SP1 x64 operating system, you can use Windows PowerShell 2.0.</span></span> <span data-ttu-id="661b9-154">Сначала нужно импортировать модуль ServerManager, а затем установить роль сервера IIS 7,5 и службы ролей.</span><span class="sxs-lookup"><span data-stu-id="661b9-154">You must first import the ServerManager module, and then install the IIS 7.5 role and role services.</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Scripting-Tools, Web-Windows-Auth, Web-Asp-Net, Web-Log-Libraries, Web-Http-Tracing, Web-Stat-Compression, Web-Dyn-Compression, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Errors, Web-Http-Logging, Web-Net-Ext, Web-Client-Auth, Web-Filtering, Web-Mgmt-Console
   ```

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="661b9-155">Анонимная проверка подлинности устанавливается по умолчанию с ролью сервера IIS.</span><span class="sxs-lookup"><span data-stu-id="661b9-155">Anonymous authentication is installed by default with the IIS server role.</span></span> <span data-ttu-id="661b9-156">Вы можете управлять анонимной проверкой подлинности после установки IIS.</span><span class="sxs-lookup"><span data-stu-id="661b9-156">You can manage anonymous authentication after the installation of IIS.</span></span> <span data-ttu-id="661b9-157">Дополнительные сведения можно найти в разделе "включить анонимную проверку подлинности (IIS 7)" <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A> .</span><span class="sxs-lookup"><span data-stu-id="661b9-157">For details, see “Enable Anonymous Authentication (IIS 7)” at <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A>.</span></span>



</div>

<span data-ttu-id="661b9-158">В таблице ниже указаны обязательные службы ролей IIS 8,0 и IIS 8,5 для Windows Server 2012 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="661b9-158">The following table indicates the required IIS 8.0 and IIS 8.5 role services for Windows Server 2012 and Windows Server 2012 R2.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="661b9-159">Для Windows Server 2012 и Windows Server 2012 R2 командлет Add-WindowsFeature был заменен командлетом Install-WindowsFeature.</span><span class="sxs-lookup"><span data-stu-id="661b9-159">For Windows Server 2012 and Windows Server 2012 R2, the Add-WindowsFeature cmdlet has been replaced by the Install-WindowsFeature cmdlet.</span></span> <span data-ttu-id="661b9-160">Подробности можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-WindowsFeature</A>.</span><span class="sxs-lookup"><span data-stu-id="661b9-160">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-WindowsFeature</A>.</span></span>



</div>

### <a name="iis-80-and-iis-85-role-services"></a><span data-ttu-id="661b9-161">Службы ролей IIS 8,0 и IIS 8,5</span><span class="sxs-lookup"><span data-stu-id="661b9-161">IIS 8.0 and IIS 8.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="661b9-162">Заголовок роли</span><span class="sxs-lookup"><span data-stu-id="661b9-162">Role Heading</span></span></th>
<th><span data-ttu-id="661b9-163">Служба ролей</span><span class="sxs-lookup"><span data-stu-id="661b9-163">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="661b9-164">Веб-сервер (IIS)</span><span class="sxs-lookup"><span data-stu-id="661b9-164">Web Server (IIS)</span></span></p></td>
<td><p><span data-ttu-id="661b9-165">Веб-сервер</span><span class="sxs-lookup"><span data-stu-id="661b9-165">Web Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-166">Основные возможности HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-166">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-167">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="661b9-167">Default Document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-168">Основные возможности HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-168">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-169">Просмотр каталога</span><span class="sxs-lookup"><span data-stu-id="661b9-169">Directory Browsing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-170">Основные возможности HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-170">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-171">Ошибки HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-171">HTTP Errors</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-172">Основные возможности HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-172">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-173">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="661b9-173">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-174">Основные возможности HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-174">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-175">Перенаправление HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-175">HTTP Redirection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-176">Работоспособность и диагностика</span><span class="sxs-lookup"><span data-stu-id="661b9-176">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="661b9-177">Ведение журнала HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-177">HTTP Logging</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-178">Работоспособность и диагностика</span><span class="sxs-lookup"><span data-stu-id="661b9-178">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="661b9-179">Средства ведения журналов</span><span class="sxs-lookup"><span data-stu-id="661b9-179">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-180">Работоспособность и диагностика</span><span class="sxs-lookup"><span data-stu-id="661b9-180">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="661b9-181">Монитор запросов</span><span class="sxs-lookup"><span data-stu-id="661b9-181">Request Monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-182">Работоспособность и диагностика</span><span class="sxs-lookup"><span data-stu-id="661b9-182">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="661b9-183">Трассировка</span><span class="sxs-lookup"><span data-stu-id="661b9-183">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-184">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-184">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-185">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="661b9-185">Request Filtering</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-186">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-186">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-187">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="661b9-187">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-188">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-188">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-189">Проверка подлинности с сопоставлением сертификатов клиентов</span><span class="sxs-lookup"><span data-stu-id="661b9-189">Client Certificate Mapping Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-190">Безопасность</span><span class="sxs-lookup"><span data-stu-id="661b9-190">Security</span></span></p></td>
<td><p><span data-ttu-id="661b9-191">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="661b9-191">Windows Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-192">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-192">Application Development</span></span></p></td>
<td><p><span data-ttu-id="661b9-193">Расширяемость .NET 3,5</span><span class="sxs-lookup"><span data-stu-id="661b9-193">.Net Extensibility 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-194">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-194">Application Development</span></span></p></td>
<td><p><span data-ttu-id="661b9-195">Расширяемость .NET 4,5</span><span class="sxs-lookup"><span data-stu-id="661b9-195">.Net Extensibility 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-196">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-196">Application Development</span></span></p></td>
<td><p><span data-ttu-id="661b9-197">ASP.Net 3,5</span><span class="sxs-lookup"><span data-stu-id="661b9-197">ASP.Net 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-198">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-198">Application Development</span></span></p></td>
<td><p><span data-ttu-id="661b9-199">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="661b9-199">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-200">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-200">Application Development</span></span></p></td>
<td><p><span data-ttu-id="661b9-201">Расширения ISAPI</span><span class="sxs-lookup"><span data-stu-id="661b9-201">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-202">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-202">Application Development</span></span></p></td>
<td><p><span data-ttu-id="661b9-203">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="661b9-203">ISAPI Filters</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-204">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="661b9-204">Application Development</span></span></p></td>
<td><p><span data-ttu-id="661b9-205">Включения на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="661b9-205">Server Side Includes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-206">Средства управления</span><span class="sxs-lookup"><span data-stu-id="661b9-206">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="661b9-207">Консоль управления IIS</span><span class="sxs-lookup"><span data-stu-id="661b9-207">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-208">Средства управления</span><span class="sxs-lookup"><span data-stu-id="661b9-208">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="661b9-209">Совместимость метабазы IIS 6</span><span class="sxs-lookup"><span data-stu-id="661b9-209">IIS 6 Metabase compatibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-210">Средства управления</span><span class="sxs-lookup"><span data-stu-id="661b9-210">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="661b9-211">Сценарии и средства управления для служб IIS</span><span class="sxs-lookup"><span data-stu-id="661b9-211">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-212">Возможности .NET 3,5 Framework</span><span class="sxs-lookup"><span data-stu-id="661b9-212">.Net 3.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-213">.NET 3,5 Framework</span><span class="sxs-lookup"><span data-stu-id="661b9-213">.Net 3.5 Framework</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-214">Возможности .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="661b9-214">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-215">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="661b9-215">.Net Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-216">Возможности .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="661b9-216">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-217">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="661b9-217">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-218">Возможности .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="661b9-218">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-219">Активация HTTP</span><span class="sxs-lookup"><span data-stu-id="661b9-219">HTTP Activation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-220">Возможности .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="661b9-220">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="661b9-221">Общий доступ к портам TCP</span><span class="sxs-lookup"><span data-stu-id="661b9-221">TCP Port Sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-222">Фоновая интеллектуальная служба передачи</span><span class="sxs-lookup"><span data-stu-id="661b9-222">Background Intelligent Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="661b9-223">Серверные расширения IIS</span><span class="sxs-lookup"><span data-stu-id="661b9-223">IIS Server Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-224">Службы рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="661b9-224">Ink and Handwriting Services</span></span></p></td>
<td><p><span data-ttu-id="661b9-225">Службы рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="661b9-225">Ink and Handwriting Services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-226">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="661b9-226">Media Foundation</span></span></p></td>
<td><p><span data-ttu-id="661b9-227">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="661b9-227">Media Foundation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-228">Пользовательские интерфейсы и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="661b9-228">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="661b9-229">Графические средства управления и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="661b9-229">Graphical Management Tools and Infrastructure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-230">Пользовательские интерфейсы и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="661b9-230">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="661b9-231">Работа с рабочим столом</span><span class="sxs-lookup"><span data-stu-id="661b9-231">Desktop Experience</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-232">Пользовательские интерфейсы и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="661b9-232">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="661b9-233">Графическая консоль сервера</span><span class="sxs-lookup"><span data-stu-id="661b9-233">Server Graphical Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-234">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="661b9-234">Windows Identity Foundation 3.5</span></span></p></td>
<td><p><span data-ttu-id="661b9-235">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="661b9-235">Windows Identity Foundation 3.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661b9-236">Служба активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="661b9-236">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="661b9-237">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="661b9-237">Process Model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661b9-238">Служба активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="661b9-238">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="661b9-239">API конфигурации</span><span class="sxs-lookup"><span data-stu-id="661b9-239">Configuration APIs</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="661b9-240">В Windows Server 2012 и Windows Server 2012 R2 для установки требований к службам IIS можно использовать Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="661b9-240">In Windows Server 2012 and Windows Server 2012 R2, you can use Windows PowerShell 3.0 to install the IIS Requirements.</span></span> <span data-ttu-id="661b9-241">С помощью модуля ServerManager в Windows PowerShell 3,0 введите:</span><span class="sxs-lookup"><span data-stu-id="661b9-241">Using the ServerManager module in Windows PowerShell 3.0, type:</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-Framework-45-Core, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Console, Web-Mgmt-Compat, Windows-Identity-Foundation, Server-Media-Foundation, BITS -Source D:\sources\sxs
   ```

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="661b9-242">Новая возможность в Windows Server 2012 — это параметр – source, который определяет, где можно найти исходный носитель Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="661b9-242">New with Windows Server 2012 is the –Source parameter that defines where the Windows Server 2012 source media can be found.</span></span> <span data-ttu-id="661b9-243">Этот носитель можно задать в качестве DVD-дисковода (например, D:\Sources\Sxs) или сетевого общего доступа, в который были скопированы файлы мультимедиа (например, \\ fileserver\windows2012\sources\Sxs).</span><span class="sxs-lookup"><span data-stu-id="661b9-243">The media can be defined as a DVD drive (for example, D:\Sources\Sxs), or to a network share that the media files have been copied (for example, \\fileserver\windows2012\sources\Sxs).</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="661b9-244">См. также</span><span class="sxs-lookup"><span data-stu-id="661b9-244">See Also</span></span>


[<span data-ttu-id="661b9-245">Требования IIS для пулов переднего плана и серверов Standard Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="661b9-245">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)  
  

<span data-ttu-id="661b9-246"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="661b9-246"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

