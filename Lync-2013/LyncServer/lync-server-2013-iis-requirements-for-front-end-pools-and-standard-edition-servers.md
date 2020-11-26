---
title: Требования IIS для пулов переднего плана и серверов Standard Edition
description: Требования к службам IIS для пулов интерфейсных и стандартных серверов выпусков.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS requirements for Front End pools and Standard Edition servers
ms:assetid: e8a6c7ac-b6d5-4c7e-abe9-d8ea5eedbc62
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399038(v=OCS.15)
ms:contentKeyID: 48185888
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f56452c7e47352333ac3ac5a51d649b0828a0ff9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427427"
---
# <a name="iis-requirements-for-front-end-pools-and-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="90219-103">Требования IIS для пулов переднего плана и серверов Standard Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90219-103">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90219-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90219-104">

<span> </span></span></span>

<span data-ttu-id="90219-105">_**Тема последнего изменения:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="90219-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="90219-106">Для серверов Standard Edition и серверов, а также режиссеров и директоров, программа Lync Server 2013 создает виртуальные каталоги в службах IIS для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="90219-106">For Standard Edition servers and Front End Servers, and Directors, the Lync Server 2013 installer creates virtual directories in Internet Information Services (IIS) for the following purposes:</span></span>

  - <span data-ttu-id="90219-107">Предоставление пользователям возможности загружать файлы из службы адресной книги</span><span class="sxs-lookup"><span data-stu-id="90219-107">To enable users to download files from the Address Book Service</span></span>

  - <span data-ttu-id="90219-108">Предоставление клиентам разрешения на получение обновлений</span><span class="sxs-lookup"><span data-stu-id="90219-108">To enable clients to obtain updates</span></span>

  - <span data-ttu-id="90219-109">Включение конференций</span><span class="sxs-lookup"><span data-stu-id="90219-109">To enable conferencing</span></span>

  - <span data-ttu-id="90219-110">Предоставление пользователям возможности загружать содержимое собрания</span><span class="sxs-lookup"><span data-stu-id="90219-110">To enable users to download meeting content</span></span>

  - <span data-ttu-id="90219-111">Предоставление пользователям разрешения на развертывание групп рассылки</span><span class="sxs-lookup"><span data-stu-id="90219-111">To enable users to expand distribution groups</span></span>

  - <span data-ttu-id="90219-112">Включение телефонной конференции</span><span class="sxs-lookup"><span data-stu-id="90219-112">To enable phone conferencing</span></span>

  - <span data-ttu-id="90219-113">Включение функций группы ответа</span><span class="sxs-lookup"><span data-stu-id="90219-113">To enable response group features</span></span>

<span data-ttu-id="90219-114">Кроме того, накопительный пакет обновления для Lync Server 2010: Ноябрь 2011 создает виртуальные каталоги в службах IIS для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="90219-114">In addition, the cumulative update for Lync Server 2010: November 2011 installer creates virtual directories in IIS for the following purposes:</span></span>

  - <span data-ttu-id="90219-115">На серверах переднего плана или стандартных серверах выпуска для поддержки мобильных функций, таких как обмен мгновенными сообщениями и присутствие, на мобильных устройствах</span><span class="sxs-lookup"><span data-stu-id="90219-115">On Front End Servers or Standard Edition servers to support mobility functionality, such as instant messaging (IM) and presence, on mobile devices</span></span>

  - <span data-ttu-id="90219-116">На серверах переднего плана или стандартных серверах и режиссерах, позволяющих мобильным устройствам автоматически определять мобильные ресурсы</span><span class="sxs-lookup"><span data-stu-id="90219-116">On Front End Servers or Standard Edition servers and on Directors to enable mobile devices to automatically discover mobility resources</span></span>



> [!NOTE]
> <span data-ttu-id="90219-117">При развертывании мобильных устройств рекомендуется использовать IIS 7,5.</span><span class="sxs-lookup"><span data-stu-id="90219-117">If you are deploying mobility, we recommend that you use IIS 7.5.</span></span> <span data-ttu-id="90219-118">Установщик службы Lync Server Mobility Service устанавливает некоторые флаги ASP.NET для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="90219-118">The Lync Server Mobility Service installer sets some ASP.NET flags to improve performance.</span></span> <span data-ttu-id="90219-119">Службы IIS 7,5 установлены по умолчанию в Windows Server 2008 R2, и установщик службы Mobility Service автоматически изменяет параметры ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="90219-119">IIS 7.5 is installed by default on Windows Server 2008 R2, and the Mobility Service installer automatically changes the ASP.NET settings.</span></span> <span data-ttu-id="90219-120">Если вы используете IIS 7,0 в Windows Server 2008, вам потребуется вручную изменить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="90219-120">If you use IIS 7.0 on Windows Server 2008, you need to manually change these settings.</span></span>



<span data-ttu-id="90219-121">Lync Server требует установки следующих модулей IIS:</span><span class="sxs-lookup"><span data-stu-id="90219-121">Lync Server requires the following IIS modules to be installed:</span></span>


> [!IMPORTANT]
> <span data-ttu-id="90219-122">Если в вашей организации требуется найти IIS и все веб-службы на диске, отличном от системного, вы можете изменить путь к папке установки для файлов Lync Server в диалоговом окне Настройка.</span><span class="sxs-lookup"><span data-stu-id="90219-122">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server files in the Setup dialog box.</span></span> <span data-ttu-id="90219-123">Если вы установили файлы установки по этому пути, включая OCSCore.msi, остальные файлы сервера Lync будут развернуты и на этом диске.</span><span class="sxs-lookup"><span data-stu-id="90219-123">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server files will be deployed to this drive as well.</span></span> <span data-ttu-id="90219-124">Сведения о том, как переместить INETPUB, развернутый диспетчером Windows Server Manager при установке IIS, можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> .</span><span class="sxs-lookup"><span data-stu-id="90219-124">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>


  - <span data-ttu-id="90219-125">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="90219-125">Static Content</span></span>

  - <span data-ttu-id="90219-126">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="90219-126">Default Document</span></span>

  - <span data-ttu-id="90219-127">Ошибки HTTP</span><span class="sxs-lookup"><span data-stu-id="90219-127">HTTP Errors</span></span>

  - <span data-ttu-id="90219-128">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="90219-128">ASP.NET</span></span>

  - <span data-ttu-id="90219-129">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="90219-129">.NET Extensibility</span></span>

  - <span data-ttu-id="90219-130">Расширения ISAPI (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="90219-130">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="90219-131">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="90219-131">ISAPI Filters</span></span>

  - <span data-ttu-id="90219-132">Ведение журнала HTTP</span><span class="sxs-lookup"><span data-stu-id="90219-132">HTTP Logging</span></span>

  - <span data-ttu-id="90219-133">Средства ведения журналов</span><span class="sxs-lookup"><span data-stu-id="90219-133">Logging Tools</span></span>

  - <span data-ttu-id="90219-134">Трассировка</span><span class="sxs-lookup"><span data-stu-id="90219-134">Tracing</span></span>

  - <span data-ttu-id="90219-135">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="90219-135">Windows Authentication</span></span>

  - <span data-ttu-id="90219-136">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="90219-136">Request Filtering</span></span>

  - <span data-ttu-id="90219-137">Сжатие статического содержимого</span><span class="sxs-lookup"><span data-stu-id="90219-137">Static Content Compression</span></span>

  - <span data-ttu-id="90219-138">Сжатие динамического содержимого</span><span class="sxs-lookup"><span data-stu-id="90219-138">Dynamic Content Compression</span></span>

  - <span data-ttu-id="90219-139">Консоль управления IIS</span><span class="sxs-lookup"><span data-stu-id="90219-139">IIS Management Console</span></span>

  - <span data-ttu-id="90219-140">Сценарии и средства управления для служб IIS</span><span class="sxs-lookup"><span data-stu-id="90219-140">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="90219-141">Анонимная проверка подлинности (устанавливается по умолчанию при установке IIS)</span><span class="sxs-lookup"><span data-stu-id="90219-141">Anonymous Authentication (installed by default when IIS is installed)</span></span>

  - <span data-ttu-id="90219-142">Проверка подлинности с сопоставлением сертификатов клиентов</span><span class="sxs-lookup"><span data-stu-id="90219-142">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="90219-143">В таблице ниже перечислены URI для виртуальных каталогов внутреннего доступа и ресурсов файловой системы, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="90219-143">The following table lists the URIs for the virtual directories for internal access and the file system resources to which they refer.</span></span>

### <a name="virtual-directories-for-internal-access"></a><span data-ttu-id="90219-144">Виртуальные каталоги для внутреннего доступа</span><span class="sxs-lookup"><span data-stu-id="90219-144">Virtual Directories for Internal Access</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90219-145">Компонент</span><span class="sxs-lookup"><span data-stu-id="90219-145">Feature</span></span></th>
<th><span data-ttu-id="90219-146">Универсальный код ресурса (URI) виртуального каталога</span><span class="sxs-lookup"><span data-stu-id="90219-146">Virtual directory URI</span></span></th>
<th><span data-ttu-id="90219-147">Ссылка на</span><span class="sxs-lookup"><span data-stu-id="90219-147">Refers to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90219-148">адресной книги</span><span class="sxs-lookup"><span data-stu-id="90219-148">Address Book Server</span></span></p></td>
<td><p><span data-ttu-id="90219-149">&lt;Внутренняя доменная HTTPS:// &gt; /ABS/int/Handler</span><span class="sxs-lookup"><span data-stu-id="90219-149">https://&lt;Internal FQDN&gt;/ABS/int/Handler</span></span></p></td>
<td><p><span data-ttu-id="90219-150">Расположение файлов для скачивания внутренних пользователей на сервер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="90219-150">Location of Address Book Server download files for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90219-151">Служба автообнаружения</span><span class="sxs-lookup"><span data-stu-id="90219-151">Autodiscover Service</span></span></p></td>
<td><p><span data-ttu-id="90219-152">&lt;Внутренняя доменная HTTPS:// &gt; /autodiscover</span><span class="sxs-lookup"><span data-stu-id="90219-152">https://&lt;Internal FQDN&gt;/Autodiscover</span></span></p></td>
<td><p><span data-ttu-id="90219-153">Расположение службы автообнаружения Lync Server, в которой находятся ресурсы для мобильных устройств, которые можно найти для внутренних пользователей.</span><span class="sxs-lookup"><span data-stu-id="90219-153">Location of the Lync Server Autodiscover Service that locates mobility resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90219-154">Обновления клиента</span><span class="sxs-lookup"><span data-stu-id="90219-154">Client updates</span></span></p></td>
<td><p><span data-ttu-id="90219-155">&lt;Внутренняя доменная http:// &gt; /AutoUpdate/int</span><span class="sxs-lookup"><span data-stu-id="90219-155">http://&lt;Internal FQDN&gt;/AutoUpdate/Int</span></span></p></td>
<td><p><span data-ttu-id="90219-156">Расположение файлов обновлений для внутренних клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="90219-156">Location of update files for internal computer-based clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90219-157">CONF</span><span class="sxs-lookup"><span data-stu-id="90219-157">Conf</span></span></p></td>
<td><p><span data-ttu-id="90219-158">&lt;Внутренняя доменная http:// &gt; /conf/int</span><span class="sxs-lookup"><span data-stu-id="90219-158">http://&lt;Internal FQDN&gt;/Conf/Int</span></span></p></td>
<td><p><span data-ttu-id="90219-159">Расположение ресурсов конференций для внутренних пользователей.</span><span class="sxs-lookup"><span data-stu-id="90219-159">Location of conferencing resources for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90219-160">Обновления устройства</span><span class="sxs-lookup"><span data-stu-id="90219-160">Device updates</span></span></p></td>
<td><p><span data-ttu-id="90219-161"> http:// &lt; внутреннее доменное имя &gt; /DeviceUpdateFiles_Int</span><span class="sxs-lookup"><span data-stu-id="90219-161">http://&lt;Internal FQDN&gt;/DeviceUpdateFiles_Int</span></span></p></td>
<td><p><span data-ttu-id="90219-162">Расположение файлов обновления устройства единой системы обмена сообщениями (UC) для внутренних устройств UC.</span><span class="sxs-lookup"><span data-stu-id="90219-162">Location of unified communications (UC) device update files for internal UC devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90219-163">Собрание</span><span class="sxs-lookup"><span data-stu-id="90219-163">Meeting</span></span></p></td>
<td><p><span data-ttu-id="90219-164">&lt;Внутренняя доменная http:// &gt; /etc/Place/null</span><span class="sxs-lookup"><span data-stu-id="90219-164">http://&lt;Internal FQDN&gt;/etc/place/null</span></span></p></td>
<td><p><span data-ttu-id="90219-165">Расположение содержимого собраний для внутренних пользователей.</span><span class="sxs-lookup"><span data-stu-id="90219-165">Location of meeting content for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90219-166">Служба Mobility Service</span><span class="sxs-lookup"><span data-stu-id="90219-166">Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="90219-167">&lt;Внутренняя доменная HTTPS:// &gt; /MCX</span><span class="sxs-lookup"><span data-stu-id="90219-167">https://&lt;Internal FQDN&gt;/Mcx</span></span></p></td>
<td><p><span data-ttu-id="90219-168">Расположение ресурсов службы Mobility Service для внутренних пользователей мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90219-168">Location of Mobility Service resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90219-169">Служба веб-запросов расширения групп и адресной книги</span><span class="sxs-lookup"><span data-stu-id="90219-169">Group Expansion and Address Book Web Query service</span></span></p></td>
<td><p><span data-ttu-id="90219-170">&lt;Внутренняя доменная http:// &gt; /GroupExpansion/int/Service.asmx</span><span class="sxs-lookup"><span data-stu-id="90219-170">http://&lt;Internal FQDN&gt;/GroupExpansion/int/service.asmx</span></span></p></td>
<td><p><span data-ttu-id="90219-171">Расположение веб-службы, обеспечивающей расширение группы для внутренних пользователей.</span><span class="sxs-lookup"><span data-stu-id="90219-171">Location of the Web service that enables group expansion for internal users.</span></span> <span data-ttu-id="90219-172">Кроме того, расположение службы веб-запросов адресной книги, предоставляющей глобальные сведения о списке адресов внутренним клиентам Lync Mobile Microsoft Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="90219-172">Also, the location of the Address Book Web Query service that provides global address list information to internal Lync Mobile Microsoft Lync 2010 Mobile clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90219-173">Телефонные конференции</span><span class="sxs-lookup"><span data-stu-id="90219-173">Phone Conferencing</span></span></p></td>
<td><p><span data-ttu-id="90219-174">&lt;Внутренняя доменная http:// &gt; /PhoneConferencing/int</span><span class="sxs-lookup"><span data-stu-id="90219-174">http://&lt;Internal FQDN&gt;/PhoneConferencing/Int</span></span></p></td>
<td><p><span data-ttu-id="90219-175">Расположение данных телефонной конференции для внутренних пользователей.</span><span class="sxs-lookup"><span data-stu-id="90219-175">Location of phone conferencing data for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90219-176">Обновления устройства</span><span class="sxs-lookup"><span data-stu-id="90219-176">Device updates</span></span></p></td>
<td><p><span data-ttu-id="90219-177">&lt;Внутренняя доменная http:// &gt; /RequestHandler</span><span class="sxs-lookup"><span data-stu-id="90219-177">http://&lt;Internal FQDN&gt;/RequestHandler</span></span></p></td>
<td><p><span data-ttu-id="90219-178">Расположение обработчика запросов веб-службы обновления устройства, который позволяет внутренним устройствам UC отправлять журналы и проверять наличие обновлений.</span><span class="sxs-lookup"><span data-stu-id="90219-178">Location of the Device Update Web service Request Handler that enables internal UC devices to upload logs and check for updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90219-179">"Группа ответа"</span><span class="sxs-lookup"><span data-stu-id="90219-179">Response Group application</span></span></p></td>
<td><p><span data-ttu-id="90219-180">&lt;Внутренняя доменная http:// &gt; /RgsConfig</span><span class="sxs-lookup"><span data-stu-id="90219-180">http://&lt;Internal FQDN&gt;/RgsConfig</span></span></p>
<p><span data-ttu-id="90219-181">&lt;Внутренняя доменная http:// &gt; /RgsClients</span><span class="sxs-lookup"><span data-stu-id="90219-181">http://&lt;Internal FQDN&gt;/RgsClients</span></span></p></td>
<td><p><span data-ttu-id="90219-182">Расположение средства настройки группы ответа.</span><span class="sxs-lookup"><span data-stu-id="90219-182">Location of Response Group Configuration Tool.</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="90219-183">Для пулов переднего плана в консолидированной конфигурации необходимо развернуть IIS, прежде чем можно будет добавить серверы в пул.</span><span class="sxs-lookup"><span data-stu-id="90219-183">For Front End pools in a consolidated configuration, you must deploy IIS before you can add servers to the pool.</span></span>


<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="разрешения" alt="security" /><span data-ttu-id="90219-185">Примечание о безопасности:</span><span class="sxs-lookup"><span data-stu-id="90219-185">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90219-186">Для назначения сертификата, используемого сервером веб-компонентов IIS, необходимо использовать оснастку администрирования IIS.</span><span class="sxs-lookup"><span data-stu-id="90219-186">You must use the IIS administrative snap-in to assign the certificate used by the IIS web component server.</span></span></td>
</tr>
</tbody>
</table><span data-ttu-id="90219-187">



</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90219-187">



</div>

<span> </span>

</div>

</div>

</span></span></div>

