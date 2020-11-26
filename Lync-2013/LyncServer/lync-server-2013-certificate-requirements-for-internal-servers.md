---
title: 'Lync Server 2013: требования к сертификатам для внутренних серверов'
description: 'Lync Server 2013: требования к сертификатам для внутренних серверов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for internal servers
ms:assetid: 0444cdbd-538c-43b1-b9a1-9d7d6cf818d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398094(v=OCS.15)
ms:contentKeyID: 48183270
ms.date: 02/17/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc1a627dd762c849b848087a96e00e19d320ef01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435357"
---
# <a name="certificate-requirements-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="c00fa-103">Требования к сертификатам для внутренних серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c00fa-103">Certificate requirements for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c00fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c00fa-104">

<span> </span></span></span>

<span data-ttu-id="c00fa-105">_**Тема последнего изменения:** 2017-02-17_</span><span class="sxs-lookup"><span data-stu-id="c00fa-105">_**Topic Last Modified:** 2017-02-17_</span></span>

<span data-ttu-id="c00fa-106">Внутренние серверы, на которых работает Lync Server и которым требуются сертификаты, включают сервер Standard Edition Server, сервер доменных служб Enterprise Edition, сервер обновлений и режиссер.</span><span class="sxs-lookup"><span data-stu-id="c00fa-106">Internal servers that are running Lync Server and that require certificates include Standard Edition server, Enterprise Edition Front End Server, Mediation Server, and Director.</span></span> <span data-ttu-id="c00fa-107">В следующей таблице приведены требования к сертификатам для этих серверов.</span><span class="sxs-lookup"><span data-stu-id="c00fa-107">The following table shows the certificate requirements for these servers.</span></span> <span data-ttu-id="c00fa-108">Вы можете запросить эти сертификаты с помощью мастера сертификатов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c00fa-108">You can use the Lync Server certificate wizard to request these certificates.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="c00fa-109">Сертификаты с подстановочными знаками поддерживаются для альтернативных имен субъектов, связанных с простыми URL-адресами в пуле переднего плана, сервере переднего плана или режиссере.</span><span class="sxs-lookup"><span data-stu-id="c00fa-109">Wildcard certificates are supported for the subject alternative names associated with the simple URLs on the Front End pool, Front End Server, or Director.</span></span> <span data-ttu-id="c00fa-110">Дополнительные сведения о поддержке сертификата с подстановочными знаками можно найти <A href="lync-server-2013-wildcard-certificate-support.md">в разделе Поддержка сертификатов подстановочных знаков в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c00fa-110">For details about wildcard certificate support, see <A href="lync-server-2013-wildcard-certificate-support.md">Wildcard certificate support in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="c00fa-111">Несмотря на то, что для внутренних серверов рекомендуется использовать внутренний центр сертификации (ЦС) предприятия, вы также можете воспользоваться общедоступным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="c00fa-111">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="c00fa-112">Список общедоступных центров сертификации, предоставляющих сертификаты, соответствующие конкретным требованиям для сертификатов с единым коммуникационным подключением (UC) и связанных с корпорацией Майкрософт, чтобы убедиться в том, что они работают с мастером сертификатов Lync Server, можно найти в статье Microsoft Knowledge Base 929395, "Партнеры сертификата единой системы связи для Exchange Server и на коммуникационном сервере" at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) .</span><span class="sxs-lookup"><span data-stu-id="c00fa-112">For a list of public CAs that provide certificates that comply with specific requirements for unified communications (UC) certificates and have partnered with Microsoft to ensure they work with the Lync Server Certificate Wizard, see article Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<span data-ttu-id="c00fa-113">Для связи с другими приложениями и серверами, такими как Exchange 2013, требуется сертификат, который поддерживается другими приложениями и продуктами.</span><span class="sxs-lookup"><span data-stu-id="c00fa-113">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="c00fa-114">В выпуске 2013, Lync Server 2013 и других серверных продуктах Microsoft, включая Exchange 2013 и SharePoint Server, поддерживается протокол OAuth для проверки подлинности и авторизации сервера и сервера.</span><span class="sxs-lookup"><span data-stu-id="c00fa-114">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="c00fa-115">Дополнительные сведения можно найти [в разделе Управление проверкой подлинности серверов (OAuth) и партнерским приложением в Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) в документации по развертыванию или документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="c00fa-115">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="c00fa-116">Для подключений клиентов, работающих под управлением операционной системы Windows 7, Windows Server 2008, операционная система Windows Server 2008 R2, операционная система Windows Vista и Microsoft Lync Phone Edition, Lync Server 2013 включает поддержку (но не обязательно) сертификатов, подписанных с помощью криптографической хэш-функции SHA-256.</span><span class="sxs-lookup"><span data-stu-id="c00fa-116">For connections from clients running Windows 7 operating system, Windows Server 2008 operating system, Windows Server 2008 R2 operating system, Windows Vista operating system, and Microsoft Lync Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="c00fa-117">Для поддержки внешнего доступа с помощью SHA-256 внешний сертификат выдается общедоступным центром сертификации с помощью SHA-256.</span><span class="sxs-lookup"><span data-stu-id="c00fa-117">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="c00fa-118">В приведенных ниже таблицах показаны требования к сертификатам для серверных пулов и серверов стандартных выпусков.</span><span class="sxs-lookup"><span data-stu-id="c00fa-118">The following tables show certificate requirements by server role for Front End pools and Standard Edition servers.</span></span> <span data-ttu-id="c00fa-119">Все они являются стандартными сертификатами веб-сервера, закрытым ключом, но не экспортируемым.</span><span class="sxs-lookup"><span data-stu-id="c00fa-119">All these are standard web server certificates, private key, non-exportable.</span></span>

<span data-ttu-id="c00fa-120">Обратите внимание на то, что при использовании мастера сертификатов для запроса сертификатов автоматически настраивается расширенное использование ключа (EKU) сервера.</span><span class="sxs-lookup"><span data-stu-id="c00fa-120">Note that server enhanced key usage (EKU) is automatically configured when you use the certificate wizard to request certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c00fa-121">Каждое понятное имя сертификата должно быть уникальным в магазине компьютера.</span><span class="sxs-lookup"><span data-stu-id="c00fa-121">Each certificate Friendly Name must be unique in the computer store.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="c00fa-122">Если вы настроили sipinternal.contoso.com или sipexternal.contoso.com в своей службе DNS, вам нужно будет добавить их в альтернативное имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c00fa-122">If you have configured sipinternal.contoso.com or sipexternal.contoso.com in your DNS, you will need to add them in the certificate’s Subject Alternative Name.</span></span>



</div>

### <a name="certificates-for-standard-edition-server"></a><span data-ttu-id="c00fa-123">Сертификаты для сервера Standard Edition</span><span class="sxs-lookup"><span data-stu-id="c00fa-123">Certificates for Standard Edition Server</span></span>

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
<th><span data-ttu-id="c00fa-124">Сертификат</span><span class="sxs-lookup"><span data-stu-id="c00fa-124">Certificate</span></span></th>
<th><span data-ttu-id="c00fa-125">Имя субъекта/общее имя</span><span class="sxs-lookup"><span data-stu-id="c00fa-125">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="c00fa-126">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="c00fa-126">Subject alternative name</span></span></th>
<th><span data-ttu-id="c00fa-127">Пример</span><span class="sxs-lookup"><span data-stu-id="c00fa-127">Example</span></span></th>
<th><span data-ttu-id="c00fa-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c00fa-128">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-129">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c00fa-129">Default</span></span></p></td>
<td><p><span data-ttu-id="c00fa-130">Полное доменное имя (FQDN) пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-130">Fully qualified domain name (FQDN) of the pool</span></span></p></td>
<td><p><span data-ttu-id="c00fa-131">Полное доменное имя пула и полное доменное имя сервера</span><span class="sxs-lookup"><span data-stu-id="c00fa-131">FQDN of the pool and the FQDN of the server</span></span></p>
<p><span data-ttu-id="c00fa-132">Если существует несколько доменов SIP и включена автоматическая настройка клиента, мастер сертификатов обнаруживает все поддерживаемые полные доменные имена SIP.</span><span class="sxs-lookup"><span data-stu-id="c00fa-132">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="c00fa-133">Если этот пул является сервером для автоматического входа клиентов и для групповой политики требуется строгое сопоставление DNS-имен, также необходимы записи для sip.sipdomain (для каждого домена SIP).</span><span class="sxs-lookup"><span data-stu-id="c00fa-133">If this pool is the auto-logon server for clients and strict Domain Name System (DNS) matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="c00fa-134">SN=se01.contoso.com; SAN=se01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-134">SN=se01.contoso.com; SAN=se01.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-135">Если этот пул предназначен для сервера автоматического входа для клиентов, а в групповой политике требуется строгое сопоставление DNS, необходимо также добавить строки SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-135">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="c00fa-136">На сервере Standard Edition полное доменное имя сервера такое же, как полное доменное имя пула.</span><span class="sxs-lookup"><span data-stu-id="c00fa-136">On Standard Edition server, the server FQDN is the same as the pool FQDN.</span></span></p>
<p><span data-ttu-id="c00fa-137">Мастер обнаруживает все домены SIP, указанные вами во время установки, и автоматически добавляет их в альтернативное имя субъекта.</span><span class="sxs-lookup"><span data-stu-id="c00fa-137">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="c00fa-138">Вы также можете использовать этот сертификат для проверки подлинности между серверами.</span><span class="sxs-lookup"><span data-stu-id="c00fa-138">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c00fa-139">Внутренняя сеть</span><span class="sxs-lookup"><span data-stu-id="c00fa-139">Web internal</span></span></p></td>
<td><p><span data-ttu-id="c00fa-140">Полное доменное имя сервера</span><span class="sxs-lookup"><span data-stu-id="c00fa-140">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="c00fa-141">Каждое из следующих:</span><span class="sxs-lookup"><span data-stu-id="c00fa-141">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c00fa-142">Полное доменное имя внутренней сети (которое совпадает с полным доменным именем сервера)</span><span class="sxs-lookup"><span data-stu-id="c00fa-142">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="c00fa-143">Простые URL-адреса собрания</span><span class="sxs-lookup"><span data-stu-id="c00fa-143">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="c00fa-144">Простой URL-адрес для телефонного подключения</span><span class="sxs-lookup"><span data-stu-id="c00fa-144">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-145">Простой URL-адрес администратора</span><span class="sxs-lookup"><span data-stu-id="c00fa-145">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-146">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="c00fa-146">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c00fa-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-148">Использование групповых сертификатов:</span><span class="sxs-lookup"><span data-stu-id="c00fa-148">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="c00fa-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c00fa-150">Невозможно переопределить внутреннее ДОМЕНное имя веб-сайта в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="c00fa-150">You cannot override the Internal web FQDN in Topology Builder.</span></span></p>
<p><span data-ttu-id="c00fa-151">При наличии нескольких простых URL-адресов собрания необходимо включить их все как альтернативные имена субъекта.</span><span class="sxs-lookup"><span data-stu-id="c00fa-151">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="c00fa-152">Для простых URL-адресов поддерживаются подстановочные записи.</span><span class="sxs-lookup"><span data-stu-id="c00fa-152">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-153">Внешняя сеть</span><span class="sxs-lookup"><span data-stu-id="c00fa-153">Web external</span></span></p></td>
<td><p><span data-ttu-id="c00fa-154">Полное доменное имя сервера</span><span class="sxs-lookup"><span data-stu-id="c00fa-154">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="c00fa-155">Каждое из следующих:</span><span class="sxs-lookup"><span data-stu-id="c00fa-155">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c00fa-156">Полное доменное имя внешней сети</span><span class="sxs-lookup"><span data-stu-id="c00fa-156">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="c00fa-157">Простой URL-адрес для телефонного подключения</span><span class="sxs-lookup"><span data-stu-id="c00fa-157">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-158">Простые URL-адреса собраний для каждого домена SIP</span><span class="sxs-lookup"><span data-stu-id="c00fa-158">Meet simple URLs per SIP domain</span></span></p></li>
<li><p><span data-ttu-id="c00fa-159">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="c00fa-159">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c00fa-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-161">Использование групповых сертификатов:</span><span class="sxs-lookup"><span data-stu-id="c00fa-161">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="c00fa-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c00fa-163">При наличии нескольких простых URL-адресов собрания необходимо включить их все как альтернативные имена субъекта.</span><span class="sxs-lookup"><span data-stu-id="c00fa-163">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="c00fa-164">Для простых URL-адресов поддерживаются подстановочные записи.</span><span class="sxs-lookup"><span data-stu-id="c00fa-164">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-front-end-server-in-a-front-end-pool"></a><span data-ttu-id="c00fa-165">Сертификаты для сервера переднего плана в пуле переднего плана</span><span class="sxs-lookup"><span data-stu-id="c00fa-165">Certificates for Front End Server in a Front End Pool</span></span>

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
<th><span data-ttu-id="c00fa-166">Сертификат</span><span class="sxs-lookup"><span data-stu-id="c00fa-166">Certificate</span></span></th>
<th><span data-ttu-id="c00fa-167">Имя субъекта/общее имя</span><span class="sxs-lookup"><span data-stu-id="c00fa-167">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="c00fa-168">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="c00fa-168">Subject alternative name</span></span></th>
<th><span data-ttu-id="c00fa-169">Пример</span><span class="sxs-lookup"><span data-stu-id="c00fa-169">Example</span></span></th>
<th><span data-ttu-id="c00fa-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c00fa-170">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-171">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c00fa-171">Default</span></span></p></td>
<td><p><span data-ttu-id="c00fa-172">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-172">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="c00fa-173">Полное доменное имя пула и полного доменного имени сервера.</span><span class="sxs-lookup"><span data-stu-id="c00fa-173">FQDN of the pool and FQDN of the server.</span></span></p>
<p><span data-ttu-id="c00fa-174">Если существует несколько доменов SIP и включена автоматическая настройка клиента, мастер сертификатов обнаруживает все поддерживаемые полные доменные имена SIP.</span><span class="sxs-lookup"><span data-stu-id="c00fa-174">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="c00fa-175">Если этот пул является сервером автоматического входа для клиентов и в групповой политике требуется строгое сопоставление DNS, вам также понадобятся записи SIP. sipdomain (для каждого домена SIP).</span><span class="sxs-lookup"><span data-stu-id="c00fa-175">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="c00fa-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-177">Если этот пул предназначен для сервера автоматического входа для клиентов, а в групповой политике требуется строгое сопоставление DNS, необходимо также добавить строки SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-177">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="c00fa-178">Мастер обнаруживает все домены SIP, указанные вами во время установки, и автоматически добавляет их в альтернативное имя субъекта.</span><span class="sxs-lookup"><span data-stu-id="c00fa-178">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="c00fa-179">Вы также можете использовать этот сертификат для проверки подлинности между серверами.</span><span class="sxs-lookup"><span data-stu-id="c00fa-179">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c00fa-180">Внутренние веб-страницы</span><span class="sxs-lookup"><span data-stu-id="c00fa-180">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="c00fa-181">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-181">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="c00fa-182">Каждое из следующих:</span><span class="sxs-lookup"><span data-stu-id="c00fa-182">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c00fa-183">Полное доменное имя внутренней сети (которое НЕ совпадает с полным доменным именем сервера)</span><span class="sxs-lookup"><span data-stu-id="c00fa-183">Internal web FQDN (which is NOT the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="c00fa-184">Полное доменное имя сервера</span><span class="sxs-lookup"><span data-stu-id="c00fa-184">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="c00fa-185">Полное доменное имя пула Lync</span><span class="sxs-lookup"><span data-stu-id="c00fa-185">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="c00fa-186">Простые URL-адреса собрания</span><span class="sxs-lookup"><span data-stu-id="c00fa-186">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="c00fa-187">Простой URL-адрес для телефонного подключения</span><span class="sxs-lookup"><span data-stu-id="c00fa-187">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-188">Простой URL-адрес администратора</span><span class="sxs-lookup"><span data-stu-id="c00fa-188">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-189">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="c00fa-189">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c00fa-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-191">Использование групповых сертификатов:</span><span class="sxs-lookup"><span data-stu-id="c00fa-191">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="c00fa-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c00fa-193">При наличии нескольких простых URL-адресов собрания необходимо включить их все как альтернативные имена субъекта.</span><span class="sxs-lookup"><span data-stu-id="c00fa-193">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="c00fa-194">Для простых URL-адресов поддерживаются подстановочные записи.</span><span class="sxs-lookup"><span data-stu-id="c00fa-194">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-195">Внешняя сеть</span><span class="sxs-lookup"><span data-stu-id="c00fa-195">Web external</span></span></p></td>
<td><p><span data-ttu-id="c00fa-196">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-196">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="c00fa-197">Каждое из следующих:</span><span class="sxs-lookup"><span data-stu-id="c00fa-197">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c00fa-198">Полное доменное имя внешней сети</span><span class="sxs-lookup"><span data-stu-id="c00fa-198">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="c00fa-199">Простой URL-адрес для телефонного подключения</span><span class="sxs-lookup"><span data-stu-id="c00fa-199">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-200">Простой URL-адрес администратора</span><span class="sxs-lookup"><span data-stu-id="c00fa-200">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-201">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="c00fa-201">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c00fa-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-203">Использование групповых сертификатов:</span><span class="sxs-lookup"><span data-stu-id="c00fa-203">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="c00fa-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c00fa-205">При наличии нескольких простых URL-адресов собрания необходимо включить их все как альтернативные имена субъекта.</span><span class="sxs-lookup"><span data-stu-id="c00fa-205">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="c00fa-206">Для простых URL-адресов поддерживаются подстановочные записи.</span><span class="sxs-lookup"><span data-stu-id="c00fa-206">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-director"></a><span data-ttu-id="c00fa-207">Сертификаты для режиссера</span><span class="sxs-lookup"><span data-stu-id="c00fa-207">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c00fa-208">Сертификат</span><span class="sxs-lookup"><span data-stu-id="c00fa-208">Certificate</span></span></th>
<th><span data-ttu-id="c00fa-209">Имя субъекта/общее имя</span><span class="sxs-lookup"><span data-stu-id="c00fa-209">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="c00fa-210">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="c00fa-210">Subject alternative name</span></span></th>
<th><span data-ttu-id="c00fa-211">Пример</span><span class="sxs-lookup"><span data-stu-id="c00fa-211">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-212">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c00fa-212">Default</span></span></p></td>
<td><p><span data-ttu-id="c00fa-213">Полное доменное имя директора пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-213">FQDN of the Director pool</span></span></p></td>
<td><p><span data-ttu-id="c00fa-214">Полное доменное имя режиссера в качестве полного доменного имени директора пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-214">FQDN of the Director, FQDN of the Director pool</span></span></p>
<p><span data-ttu-id="c00fa-215">Если этот пул является сервером автоматического входа для клиентов и в групповой политике требуется строгое сопоставление DNS, вам также понадобятся записи SIP. sipdomain (для каждого домена SIP).</span><span class="sxs-lookup"><span data-stu-id="c00fa-215">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="c00fa-216">SN = dir-pool.contoso.com; Сеть хранения данных = Dir-pool.contoso.com; SAN = dir01. contoso. com</span><span class="sxs-lookup"><span data-stu-id="c00fa-216">SN=dir-pool.contoso.com; SAN=dir-pool.contoso.com; SAN=dir01.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-217">Если этот пул директоров предназначен для сервера автоматического входа для клиентов, а в групповой политике требуется строгое сопоставление DNS, необходимо также добавить строки SAN=contoso.com SIP; SAN=fabrikam.com SIP.</span><span class="sxs-lookup"><span data-stu-id="c00fa-217">If this Director pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c00fa-218">Внутренние веб-страницы</span><span class="sxs-lookup"><span data-stu-id="c00fa-218">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="c00fa-219">Полное доменное имя сервера</span><span class="sxs-lookup"><span data-stu-id="c00fa-219">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="c00fa-220">Каждое из следующих:</span><span class="sxs-lookup"><span data-stu-id="c00fa-220">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c00fa-221">Полное доменное имя внутренней сети (которое совпадает с полным доменным именем сервера)</span><span class="sxs-lookup"><span data-stu-id="c00fa-221">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="c00fa-222">Полное доменное имя сервера</span><span class="sxs-lookup"><span data-stu-id="c00fa-222">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="c00fa-223">Полное доменное имя пула Lync</span><span class="sxs-lookup"><span data-stu-id="c00fa-223">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="c00fa-224">Простые URL-адреса собрания</span><span class="sxs-lookup"><span data-stu-id="c00fa-224">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="c00fa-225">Простой URL-адрес для телефонного подключения</span><span class="sxs-lookup"><span data-stu-id="c00fa-225">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-226">Простой URL-адрес администратора</span><span class="sxs-lookup"><span data-stu-id="c00fa-226">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-227">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="c00fa-227">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c00fa-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-230">Внешняя сеть</span><span class="sxs-lookup"><span data-stu-id="c00fa-230">Web external</span></span></p></td>
<td><p><span data-ttu-id="c00fa-231">Полное доменное имя сервера</span><span class="sxs-lookup"><span data-stu-id="c00fa-231">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="c00fa-232">Каждое из следующих:</span><span class="sxs-lookup"><span data-stu-id="c00fa-232">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c00fa-233">Полное доменное имя внешней сети</span><span class="sxs-lookup"><span data-stu-id="c00fa-233">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="c00fa-234">Простой URL-адрес для телефонного подключения</span><span class="sxs-lookup"><span data-stu-id="c00fa-234">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-235">Простой URL-адрес администратора</span><span class="sxs-lookup"><span data-stu-id="c00fa-235">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="c00fa-236">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="c00fa-236">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c00fa-237">Полное доменное имя внешней сети директора должно отличаться от пула переднего плана и сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="c00fa-237">The Director external web FQDN must be different from the Front End pool or Front End Server.</span></span></p>
<p><span data-ttu-id="c00fa-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="c00fa-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c00fa-240">Если у вас есть независимый пул серверов с исправлениями, для каждого из них необходимы сертификаты, указанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c00fa-240">If you have a stand-alone Mediation Server pool, the Mediation Servers in it each need the certificates listed in the following table.</span></span> <span data-ttu-id="c00fa-241">Если вы развернули сервер обновлений с помощью серверов переднего плана, вам достаточно сертификатов, указанных в таблице "сертификаты для сервера переднего плана в пуле переднего плана", описанном выше в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="c00fa-241">If you collocate Mediation Server with the Front End Servers, the certificates listed in the “Certificates for Front End Server in Front End Pool” table earlier in this topic are sufficient.</span></span>

### <a name="certificates-for-stand-alone-mediation-server"></a><span data-ttu-id="c00fa-242">Сертификаты для сервера автономных обновлений</span><span class="sxs-lookup"><span data-stu-id="c00fa-242">Certificates for Stand-alone Mediation Server</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c00fa-243">Сертификат</span><span class="sxs-lookup"><span data-stu-id="c00fa-243">Certificate</span></span></th>
<th><span data-ttu-id="c00fa-244">Имя субъекта/общее имя</span><span class="sxs-lookup"><span data-stu-id="c00fa-244">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="c00fa-245">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="c00fa-245">Subject alternative name</span></span></th>
<th><span data-ttu-id="c00fa-246">Пример</span><span class="sxs-lookup"><span data-stu-id="c00fa-246">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-247">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c00fa-247">Default</span></span></p></td>
<td><p><span data-ttu-id="c00fa-248">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-248">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="c00fa-249">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-249">FQDN of the pool</span></span></p>
<p><span data-ttu-id="c00fa-250">Полное доменное имя сервера участника пула</span><span class="sxs-lookup"><span data-stu-id="c00fa-250">FQDN of pool member server</span></span></p></td>
<td><p><span data-ttu-id="c00fa-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c00fa-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-survivable-branch-appliance"></a><span data-ttu-id="c00fa-252">Сертификаты для устройства с бесперебойной подразделением</span><span class="sxs-lookup"><span data-stu-id="c00fa-252">Certificates for Survivable Branch Appliance</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c00fa-253">Сертификат</span><span class="sxs-lookup"><span data-stu-id="c00fa-253">Certificate</span></span></th>
<th><span data-ttu-id="c00fa-254">Имя субъекта/общее имя</span><span class="sxs-lookup"><span data-stu-id="c00fa-254">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="c00fa-255">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="c00fa-255">Subject alternative name</span></span></th>
<th><span data-ttu-id="c00fa-256">Пример</span><span class="sxs-lookup"><span data-stu-id="c00fa-256">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c00fa-257">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c00fa-257">Default</span></span></p></td>
<td><p><span data-ttu-id="c00fa-258">Полное доменное имя устройства</span><span class="sxs-lookup"><span data-stu-id="c00fa-258">FQDN of the appliance</span></span></p></td>
<td><p><span data-ttu-id="c00fa-259">SIP. &lt; sipdomain &gt; (требуется одна запись для каждого домена SIP)</span><span class="sxs-lookup"><span data-stu-id="c00fa-259">SIP.&lt;sipdomain&gt; (need one entry per SIP domain)</span></span></p></td>
<td><p><span data-ttu-id="c00fa-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="c00fa-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="c00fa-261">См. также</span><span class="sxs-lookup"><span data-stu-id="c00fa-261">See Also</span></span>


[<span data-ttu-id="c00fa-262">Поддержка групповых сертификатов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c00fa-262">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="c00fa-263"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c00fa-263"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

