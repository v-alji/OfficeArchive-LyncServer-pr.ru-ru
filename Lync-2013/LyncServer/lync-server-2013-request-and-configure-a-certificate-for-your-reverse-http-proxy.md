---
title: Запрос и настройка сертификата для обратного HTTP-прокси
description: Запросите сертификат и настройте его для обратного HTTP-прокси.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Request and configure a certificate for your reverse HTTP proxy
ms:assetid: 4b70991e-5f10-40a3-b069-0b227c3a3a0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429704(v=OCS.15)
ms:contentKeyID: 48184085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdeaa080e3ccb6a9895e18a6ac02084e99a1e33e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442749"
---
# <a name="request-and-configure-a-certificate-for-your-reverse-http-proxy-in-lync-server-2013"></a><span data-ttu-id="facda-103">Запрос и настройка сертификата для обратного HTTP-прокси в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="facda-103">Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="facda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="facda-104">

<span> </span></span></span>

<span data-ttu-id="facda-105">_**Тема последнего изменения:** 2014-02-14_</span><span class="sxs-lookup"><span data-stu-id="facda-105">_**Topic Last Modified:** 2014-02-14_</span></span>

<span data-ttu-id="facda-106">Необходимо установить сертификат корневого центра сертификации (ЦС) на сервере под управлением Microsoft Forefront Threat Management Gateway 2010 или IIS ARR для инфраструктуры ЦС, выдавшего сертификаты сервера на внутренние серверы, на которых запущено приложение Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="facda-106">You need to install the root certification authority (CA) certificate on the server running Microsoft Forefront Threat Management Gateway 2010 or IIS ARR for the CA infrastructure that issued the server certificates to the internal servers running Microsoft Lync Server 2013.</span></span>

<span data-ttu-id="facda-107">Кроме того, необходимо установить общедоступный сертификат веб-сервера на обратном прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="facda-107">You also must install a public web server certificate on your reverse proxy server.</span></span> <span data-ttu-id="facda-108">Альтернативные имена субъектов этого сертификата должны содержать опубликованные внешние полные доменные имена для каждого пула, который является доменом для пользователей, для которых разрешен удаленный доступ, и внешнее FQDN всех режиссеров и пулов, которые будут использоваться в этой инфраструктуре пограничного приложения.</span><span class="sxs-lookup"><span data-stu-id="facda-108">This certificate’s subject alternative names should contain the published external fully qualified domain names (FQDNs) of each pool that is home to users enabled for remote access, and the external FQDNs of all Directors or Director pools that will be used within that Edge infrastructure.</span></span> <span data-ttu-id="facda-109">Альтернативное имя темы также должно содержать простой URL-адрес для собрания, простой URL-адрес для телефонного подключения и, если вы развертываете мобильные приложения, и запланировать использование автоматического обнаружения, URL-адрес службы внешнего автообнаружения, как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="facda-109">The subject alternative name must also contain the meeting simple URL, the dial-in simple URL, and, if you are deploying mobile applications and plan to use automatic discovery, the external Autodiscover Service URL as shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="facda-110">Значение</span><span class="sxs-lookup"><span data-stu-id="facda-110">Value</span></span></th>
<th><span data-ttu-id="facda-111">Пример</span><span class="sxs-lookup"><span data-stu-id="facda-111">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="facda-112">Имя субъекта</span><span class="sxs-lookup"><span data-stu-id="facda-112">Subject name</span></span></p></td>
<td><p><span data-ttu-id="facda-113">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="facda-113">Pool FQDN</span></span></p></td>
<td><p><span data-ttu-id="facda-114">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="facda-114">webext.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="facda-115">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="facda-115">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="facda-116">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="facda-116">Pool FQDN</span></span></p></td>
<td><p><span data-ttu-id="facda-117">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="facda-117">webext.contoso.com</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="facda-118">Имя субъекта должно быть указано в альтернативном имени субъекта.</span><span class="sxs-lookup"><span data-stu-id="facda-118">The subject name must also be present in the subject alternative name.</span></span>

</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="facda-119">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="facda-119">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="facda-120">Необязательные веб-службы режиссера (если режиссер развернут)</span><span class="sxs-lookup"><span data-stu-id="facda-120">Optional Director Web Services (if Director is deployed)</span></span></p></td>
<td><p><span data-ttu-id="facda-121">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="facda-121">webdirext.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="facda-122">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="facda-122">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="facda-123">Простой URL-адрес для собрания</span><span class="sxs-lookup"><span data-stu-id="facda-123">Meeting simple URL</span></span></p>



> [!NOTE]
> <span data-ttu-id="facda-124">Все простые URL-адреса собраний должны находиться в альтернативном имени субъекта.</span><span class="sxs-lookup"><span data-stu-id="facda-124">All meeting simple URLs must be in the subject alternative name.</span></span> <span data-ttu-id="facda-125">У каждого домена SIP должен быть хотя бы один активный простой URL-адрес для собрания.</span><span class="sxs-lookup"><span data-stu-id="facda-125">Each SIP domain must have at least one active meeting simple URL.</span></span>

</td>
<td><p><span data-ttu-id="facda-126">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="facda-126">meet.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="facda-127">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="facda-127">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="facda-128">Простой URL-адрес для телефонного подключения</span><span class="sxs-lookup"><span data-stu-id="facda-128">Dial-in simple URL</span></span></p></td>
<td><p><span data-ttu-id="facda-129">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="facda-129">dialin.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="facda-130">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="facda-130">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="facda-131">Сервер Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="facda-131">Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="facda-132">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="facda-132">officewebapps01.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="facda-133">Альтернативное имя субъекта</span><span class="sxs-lookup"><span data-stu-id="facda-133">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="facda-134">Внешний URL-адрес службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="facda-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="facda-135">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="facda-135">lyncdiscover.contoso.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="facda-136">Если вы также используете Microsoft Exchange Server, вам также потребуется настроить обратные правила прокси-сервера для URL-адресов автообнаружения Exchange и Web Services.</span><span class="sxs-lookup"><span data-stu-id="facda-136">If you are also using Microsoft Exchange Server you will also need to configure reverse proxy rules for the Exchange autodiscover and web services URLs.</span></span>

</td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]
> <span data-ttu-id="facda-137">Если внутреннее развертывание состоит из более чем одного стандартного сервера выпуска или пула переднего плана, необходимо настроить правила веб-публикации для каждого полного доменного имени внешней веб-фермы, а для каждого из них требуется сертификат и веб-прослушиватель либо необходимо получить сертификат, для которого есть дополнительное имя субъекта, чтобы назначить его веб-прослушивателем. и поделиться им с другими правилами веб-публикации.</span><span class="sxs-lookup"><span data-stu-id="facda-137">If your internal deployment consists of more than one Standard Edition server or Front End pool, you must configure web publishing rules for each external web farm FQDN and you will either need a certificate and web listener for each, or you must obtain a certificate whose subject alternative name contains the names used by all of the pools, assign it to a web listener, and share it among multiple web publishing rules.</span></span>



</div>

<div>

## <a name="create-a-certificate-request"></a><span data-ttu-id="facda-138">Создание запроса на сертификат</span><span class="sxs-lookup"><span data-stu-id="facda-138">Create a Certificate Request</span></span>

<span data-ttu-id="facda-139">Вы создаете запрос на сертификат на обратном прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="facda-139">You create a certificate request on the reverse proxy.</span></span> <span data-ttu-id="facda-140">Вы создаете запрос на другом компьютере, но хотите экспортировать подписанный сертификат с закрытым ключом и импортировать его на обратный прокси-сервер после того, как вы получили его от общедоступного центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="facda-140">You create a request on another computer, but you must export the signed certificate with the private key and import it onto the reverse proxy once you have received it from the public certification authority.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="facda-141">Запрос на сертификат или запрос подписи сертификата (CSR) — это запрос доверенного общедоступного центра сертификации (ЦС) для проверки и подписывания открытого ключа компьютера-запроса.</span><span class="sxs-lookup"><span data-stu-id="facda-141">A certificate request or a certificate signing request (CSR) is a request to a trusted public certification authority (CA) to validate and sign the requesting computer’s public key.</span></span> <span data-ttu-id="facda-142">При создании сертификата создается открытый ключ и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="facda-142">When a certificate is generated, a public key and a private key are created.</span></span> <span data-ttu-id="facda-143">Только открытый ключ является общим и подписанным.</span><span class="sxs-lookup"><span data-stu-id="facda-143">Only the public key is shared and signed.</span></span> <span data-ttu-id="facda-144">Как указано в имени, Открытый ключ предоставляется любому общедоступному запросу.</span><span class="sxs-lookup"><span data-stu-id="facda-144">As the name implies, the public key is made available to any public request.</span></span> <span data-ttu-id="facda-145">Открытый ключ предназначен для использования клиентами, серверами и другими инициаторами запроса, которые должны безопасно обмениваться сведениями и проверять удостоверение компьютера.</span><span class="sxs-lookup"><span data-stu-id="facda-145">The public key is for use by clients, servers and other requesters that need to exchange information securely and validate a computer’s identity.</span></span> <span data-ttu-id="facda-146">Закрытый ключ защищен и используется только компьютером, который создал пару ключей для расшифровки сообщений, зашифрованных с помощью открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="facda-146">The private key is kept secured and is used only by the computer that created the key pair to decrypt messages encrypted with its public key.</span></span> <span data-ttu-id="facda-147">Закрытый ключ можно использовать для других целей.</span><span class="sxs-lookup"><span data-stu-id="facda-147">The private key can be used for other purposes.</span></span> <span data-ttu-id="facda-148">Для обратной идентификации прокси-сервера используется шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="facda-148">For reverse proxy purposes, data encipherment is the primary use.</span></span> <span data-ttu-id="facda-149">Secondarily, проверка подлинности сертификата на уровне ключа сертификата является другой, и она ограничивается только подтверждением того, что у инициатора запроса есть открытый ключ компьютера, и что компьютер, на котором он открыт, действительно является компьютером, на котором он находится.</span><span class="sxs-lookup"><span data-stu-id="facda-149">Secondarily, the certificate authentication at the certificate key level is another use, and is limited only to validation that a requester has the computer’s public key, or that the computer that you have a public key for is actually the computer that it claims to be.</span></span>



</div>

<div>


> [!TIP]
> <span data-ttu-id="facda-150">Если вы планируете одновременное планирование сертификатов пограничного сервера и прокси-сертификатов, следует обратить внимание на то, что между двумя требованиями к сертификатам есть большое отношение.</span><span class="sxs-lookup"><span data-stu-id="facda-150">If you plan your Edge Server certificates and your reverse proxy certificates at the same time, you should notice that there is a great deal of similarity between the two certificate requirements.</span></span> <span data-ttu-id="facda-151">Если вы настраиваете и запрашиваете сертификат пограничного сервера, объедините пограничный сервер и альтернативные имена субъектов для обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="facda-151">When you configure and request your Edge Server certificate, combine the Edge Server and the reverse proxy subject alternative names.</span></span> <span data-ttu-id="facda-152">Вы можете использовать один и тот же сертификат для обратного прокси-сервера в случае экспорта сертификата и закрытого ключа и копирования экспортированного файла в обратный прокси и импорта сертификата или ключа и назначения его в соответствии с предстоящимй процедурой.</span><span class="sxs-lookup"><span data-stu-id="facda-152">You can use the same certificate for your reverse proxy if you export the certificate and the private key and copy the exported file to the reverse proxy and then import the certificate/key pair and assign it as needed in the upcoming procedures.</span></span> <span data-ttu-id="facda-153">Ознакомьтесь со сведениями о требованиях к сертификатам для плана пограничного сервера &nbsp; <A href="lync-server-2013-plan-for-edge-server-certificates.md">в lync Server 2013</A> и обратной связи <A href="lync-server-2013-certificate-summary-reverse-proxy.md">сертификата прокси-сервера в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="facda-153">Refer to the certificate requirements for the Edge Server&nbsp;<A href="lync-server-2013-plan-for-edge-server-certificates.md">Plan for Edge Server certificates in Lync Server 2013</A> and the reverse proxy <A href="lync-server-2013-certificate-summary-reverse-proxy.md">Certificate summary - Reverse proxy in Lync Server 2013</A>.</span></span> <span data-ttu-id="facda-154">Убедитесь, что вы создали сертификат с экспортируемым закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="facda-154">Make sure that you create the certificate with an exportable private key.</span></span> <span data-ttu-id="facda-155">Создание сертификата и запроса на сертификат с экспортируемым закрытым ключом требуется для пограничного сервера пула, поэтому этот параметр является стандартным и мастером сертификатов в мастере развертывания Lync Server на пограничном сервере позволит вам установить флаг для <STRONG>экспорта закрытого ключа</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="facda-155">Creating the certificate and certificate request with an exportable private key is required for pooled Edge Servers, so this is a normal practice and the Certificate Wizard in the Lync Server Deployment Wizard for the Edge Server will allow you to set the <STRONG>Make private key exportable</STRONG> flag.</span></span> <span data-ttu-id="facda-156">После получения запроса на сертификат из общедоступного центра сертификации вы будете экспортировать сертификат и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="facda-156">Once you receive the certificate request back from the public certification authority, you will export the certificate and the private key.</span></span> <span data-ttu-id="facda-157">Сведения о том, как создать и экспортировать сертификат с закрытым ключом, можно найти в разделе "Экспорт сертификата с закрытым ключом для пограничных серверов в пуле" в разделе <A href="lync-server-2013-set-up-certificates-for-the-external-edge-interface.md">Настройка сертификатов для внешнего интерфейса Edge для Lync Server 2013</A> .</span><span class="sxs-lookup"><span data-stu-id="facda-157">See the section “To export the certificate with the private key for Edge Servers in a pool” in the topic <A href="lync-server-2013-set-up-certificates-for-the-external-edge-interface.md">Set up certificates for the external edge interface for Lync Server 2013</A> for details on how to create and export your certificate with a private key.</span></span> <span data-ttu-id="facda-158">Расширение сертификата должно иметь тип <STRONG>PFX</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="facda-158">The extension of the certificate should be of type <STRONG>.pfx</STRONG>.</span></span>



</div>

<span data-ttu-id="facda-159">Чтобы создать запрос на подписывание сертификата на компьютере, на котором будет назначаться сертификат и закрытый ключ, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="facda-159">To generate a certificate signing request on the computer where the certificate and private key will be assigned, you do the following:</span></span>

<span data-ttu-id="facda-160">**Создание запроса на подписывание сертификата**</span><span class="sxs-lookup"><span data-stu-id="facda-160">**Creating a certificate signing request**</span></span>

1.  <span data-ttu-id="facda-161">Откройте консоль управления (MMC) и добавьте оснастку "сертификаты" и выберите пункт " **Компьютеры**", а затем — " **Личные**".</span><span class="sxs-lookup"><span data-stu-id="facda-161">Open the Microsoft Management Console (MMC) and add the Certificates snap-in and select **Computers**, then expand **Personal**.</span></span> <span data-ttu-id="facda-162">Подробнее о том, как создать консоль сертификатов в консоли управления Майкрософт (MMC), можно найти в разделе [https://go.microsoft.com/fwlink/?LinkId=282616](https://go.microsoft.com/fwlink/?linkid=282616) .</span><span class="sxs-lookup"><span data-stu-id="facda-162">For details on how to create a certificates console in the Microsoft Management Console (MMC), see [https://go.microsoft.com/fwlink/?LinkId=282616](https://go.microsoft.com/fwlink/?linkid=282616).</span></span>

2.  <span data-ttu-id="facda-163">Щелкните правой кнопкой мыши пункт **Сертификаты**, выберите **все задачи**, а затем **Дополнительные операции**, нажмите **создать настраиваемый запрос**.</span><span class="sxs-lookup"><span data-stu-id="facda-163">Right-click **Certificates**, click **All Tasks**, click **Advanced Operations**, click **Create Custom Request**.</span></span>

3.  <span data-ttu-id="facda-164">На странице " **регистрация сертификата** " нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="facda-164">On the **Certificate Enrollment** page, click **Next**.</span></span>

4.  <span data-ttu-id="facda-165">На странице " **Выбор политики регистрации сертификатов** " в разделе **настраиваемый запрос** выберите вариант **Продолжить без политики регистрации**.</span><span class="sxs-lookup"><span data-stu-id="facda-165">On the **Select Certificate Enrollment Policy** page under **Custom Request**, select **Proceed without enrollment policy**.</span></span> <span data-ttu-id="facda-166">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="facda-166">Click **Next**.</span></span>

5.  <span data-ttu-id="facda-167">На странице " **настраиваемый запрос** " для **шаблона** выбор **устаревшего ключа (без шаблона)**.</span><span class="sxs-lookup"><span data-stu-id="facda-167">On the **Custom Request** page, for **Template** select **(No template) Legacy key**.</span></span> <span data-ttu-id="facda-168">Если поставщик сертификата не направляет иное, оставьте флажок не проверять **расширения по умолчанию** и выберите **Формат запроса** в **PKCS \# 10**.</span><span class="sxs-lookup"><span data-stu-id="facda-168">Unless otherwise directed by your certificate provider, leave **Suppress default extensions** unchecked and the **Request format** selection on **PKCS \#10**.</span></span> <span data-ttu-id="facda-169">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="facda-169">Click **Next**.</span></span>

6.  <span data-ttu-id="facda-170">На странице **сведения о сертификате** нажмите кнопку **сведения** и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="facda-170">On the **Certificate Information** page, click **Details**, then click **Properties**.</span></span>

7.  <span data-ttu-id="facda-171">На странице **Свойства сертификата** на вкладке **Общие** в поле **понятное имя** введите имя этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="facda-171">On the **Certificate Properties** page on the **General** tab in the **Friendly Name** field, type a name for this certificate.</span></span> <span data-ttu-id="facda-172">При необходимости введите описание в поле **Описание** .</span><span class="sxs-lookup"><span data-stu-id="facda-172">Optionally, type a description in the **Description** field.</span></span> <span data-ttu-id="facda-173">Понятное имя и описание обычно используются администратором, чтобы определить назначение сертификата, например **обратный прослушиватель прокси-сервера для Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="facda-173">The Friendly Name and description are typically used by the Administrator to identify what the certificate purpose is, such as **Reverse Proxy Listener for Lync Server**.</span></span>

8.  <span data-ttu-id="facda-174">Откройте вкладку **Тема** . В разделе **имя субъекта** для **типа** выберите пункт **Общее имя** для типа имени субъекта.</span><span class="sxs-lookup"><span data-stu-id="facda-174">Select the **Subject** tab. Under **Subject name** for the **Type**, select **Common name** for the Subject name type.</span></span> <span data-ttu-id="facda-175">В качестве **значения** введите имя субъекта, которое будет использоваться для обратного прокси-сервера, и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="facda-175">For the **Value**, type the subject name that you will use for the reverse proxy, and then click **Add**.</span></span> <span data-ttu-id="facda-176">В примере, приведенном в таблице в этом разделе, имя субъекта — webext.contoso.com, и оно будет введено в поле Value (значение) для имени субъекта.</span><span class="sxs-lookup"><span data-stu-id="facda-176">In the example provided in the table in this topic, the subject name is webext.contoso.com and would be typed into the Value field for the Subject name.</span></span>

9.  <span data-ttu-id="facda-177">На вкладке **Тема** в разделе **альтернативное имя** выберите **DNS** в раскрывающемся списке **тип**.</span><span class="sxs-lookup"><span data-stu-id="facda-177">On the **Subject** tab under **Alternative name**, select **DNS** from the drop down for **Type**.</span></span> <span data-ttu-id="facda-178">Введите полное доменное имя для каждого определенного имени, которое требуется использовать в сертификате, и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="facda-178">For each defined subject alternative name that you require on the certificate, type the fully qualified domain name, then click **Add**.</span></span> <span data-ttu-id="facda-179">Например, в таблице есть три альтернативных имени субъекта, meet.contoso.com, dialin.contoso.com и lyncdiscover.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="facda-179">For example, in the table there are three subject alternative names, meet.contoso.com, dialin.contoso.com, and lyncdiscover.contoso.com.</span></span> <span data-ttu-id="facda-180">В поле " **значение** " введите Meet.contoso.com и нажмите кнопку " **Добавить**".</span><span class="sxs-lookup"><span data-stu-id="facda-180">In the **Value** field, type meet.contoso.com, then click **Add**.</span></span> <span data-ttu-id="facda-181">Повторите эти действия для каждой темы, которую нужно определить.</span><span class="sxs-lookup"><span data-stu-id="facda-181">Repeat for each subject alternative names that you need to define.</span></span>

10. <span data-ttu-id="facda-182">На странице " **Свойства сертификата** " откройте вкладку " **расширения** ". На этой странице вы будете определять цели криптографических ключей в **использовании ключа** и использование расширенного ключа в **расширенном использовании ключа (политики приложений)**.</span><span class="sxs-lookup"><span data-stu-id="facda-182">On the **Certificate Properties** page, click the **Extensions** tab. On this page, you will define the cryptographic key purposes in **Key usage** and the extended key usage in **Extended Key Usage (application policies)**.</span></span>

11. <span data-ttu-id="facda-183">Щелкните стрелку " **Использование ключа** ", чтобы показать **Доступные параметры**.</span><span class="sxs-lookup"><span data-stu-id="facda-183">Click the **Key usage** arrow to show the **Available options**.</span></span> <span data-ttu-id="facda-184">В разделе Доступные параметры выберите пункт **Цифровая подпись** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="facda-184">Under Available options, click **Digital signature**, then click **Add**.</span></span> <span data-ttu-id="facda-185">Выберите **Шифрование ключей** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="facda-185">Click **Key encipherment**, then click **Add**.</span></span> <span data-ttu-id="facda-186">Если флажок **установить критические данные об использовании ключа** не установлен, установите флажок.</span><span class="sxs-lookup"><span data-stu-id="facda-186">If the checkbox for **Make these key usages critical** is unchecked, select the checkbox.</span></span>

12. <span data-ttu-id="facda-187">Щелкните стрелку **расширенного использования ключа (политики применения)** , чтобы отобразить **Доступные параметры**.</span><span class="sxs-lookup"><span data-stu-id="facda-187">Click the **Extended Key Usage (application policies)** arrow to show the **Available options**.</span></span> <span data-ttu-id="facda-188">В разделе Доступные параметры выберите **Проверка подлинности сервера** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="facda-188">Under Available options, click **Server Authentication**, then click **Add**.</span></span> <span data-ttu-id="facda-189">Выберите **Проверка подлинности клиента**, а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="facda-189">Click **Client Authentication**, then click **Add**.</span></span> <span data-ttu-id="facda-190">Если флажок **сделать обязательным использование расширенных ключей** установлен, снимите флажок.</span><span class="sxs-lookup"><span data-stu-id="facda-190">If the check box for **Make the Extended Key Usages critical** is checked, unselect the checkbox.</span></span> <span data-ttu-id="facda-191">Напротив, флажок использование ключа (должен быть установлен) необходимо убедиться, что флажок расширенного ключа использования не установлен.</span><span class="sxs-lookup"><span data-stu-id="facda-191">Contrary to the Key usage checkbox (which must be checked) you must be sure that the Extended Key Usage checkbox is not checked.</span></span>

13. <span data-ttu-id="facda-192">На странице " **Свойства сертификата** " откройте вкладку **закрытые ключи** . Щелкните стрелку **Параметры клавиш** .</span><span class="sxs-lookup"><span data-stu-id="facda-192">On the **Certificate Properties** page, click the **Private Key** tab. Click the **Key options** arrow.</span></span> <span data-ttu-id="facda-193">В раскрывающемся списке **Размер ключа** выберите **2048** .</span><span class="sxs-lookup"><span data-stu-id="facda-193">For **Key size**, select **2048** from the drop down.</span></span> <span data-ttu-id="facda-194">Если вы создаете пару ключей и CSR на компьютере, отличном от обратного прокси-сервера, для которого предназначен этот сертификат, установите флажок **сделать закрытым ключ экспортируемым**.</span><span class="sxs-lookup"><span data-stu-id="facda-194">If you are generating this key pair and CSR on a computer other than the reverse proxy that this certificate is intended for, select **Make private key exportable**.</span></span>
    
    <div>
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg398321.security(OCS.15).gif" title="разрешения" alt="security" /><span data-ttu-id="facda-196">Примечание о безопасности:</span><span class="sxs-lookup"><span data-stu-id="facda-196">Security Note:</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="facda-197">Выбор варианта <strong>экспорта закрытого ключа</strong> обычно рекомендуется использовать, если в ферме есть несколько обратных прокси-серверов, так как вы будете копировать сертификат и закрытый ключ на каждый компьютер в ферме.</span><span class="sxs-lookup"><span data-stu-id="facda-197">Selecting <strong>Make a private key exportable</strong> is generally advised when you have more than one reverse proxy in a farm because you will copy the certificate and the private key to each machine in the farm.</span></span> <span data-ttu-id="facda-198">Если вы разрешены для экспортируемого закрытого ключа, вы должны уделять особой осторожности с сертификатом и компьютером, на котором он был создан.</span><span class="sxs-lookup"><span data-stu-id="facda-198">If you do allow for an exportable private key, you must take extra care with the certificate and the computer that it is generated on.</span></span> <span data-ttu-id="facda-199">Закрытый ключ, если он скомпрометирован, будет вырисовывать бесполезный сертификат, а также может предоставить компьютеру или компьютерам внешний доступ и другие уязвимости системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="facda-199">The private key, if compromised, will render the certificate useless as well as potentially expose the computer or computers to external access and other security vulnerabilities.</span></span></td>
    </tr>
    </tbody>
    </table>
    
    </div>

14. <span data-ttu-id="facda-200">На вкладке **закрытые ключи** щелкните стрелку **тип ключа** .</span><span class="sxs-lookup"><span data-stu-id="facda-200">On the **Private Key** tab, click the **Key type** arrow.</span></span> <span data-ttu-id="facda-201">Выберите параметр **Exchange** .</span><span class="sxs-lookup"><span data-stu-id="facda-201">Select the **Exchange** option.</span></span>

15. <span data-ttu-id="facda-202">Нажмите кнопку **ОК** , чтобы сохранить заданные **Свойства сертификата** .</span><span class="sxs-lookup"><span data-stu-id="facda-202">Click **OK** to save the **Certificate Properties** that you have set.</span></span>

16. <span data-ttu-id="facda-203">На странице " **регистрация сертификата** " нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="facda-203">On the **Certificate Enrollment** page, click **Next**.</span></span>

17. <span data-ttu-id="facda-204">На странице **где вы хотите сохранить автономный запрос?** вам будет предложено указать **имя файла** и **Формат файла** для сохранения запроса подписи сертификата.</span><span class="sxs-lookup"><span data-stu-id="facda-204">On the **Where do you want to save the offline request?** page, you are prompted for a **File Name** and a **File Format** for saving the certificate signing request.</span></span>

18. <span data-ttu-id="facda-205">В поле **имя файла** введите путь и имя файла запроса или нажмите кнопку **Обзор** , чтобы выбрать расположение для файла, и введите имя файла для запроса.</span><span class="sxs-lookup"><span data-stu-id="facda-205">In the **File Name** entry field, type a path and filename for the request, or click **Browse** to select a location for the file and type the filename for the request.</span></span>

19. <span data-ttu-id="facda-206">В качестве **формата файла** выберите значение **base 64** или **binary**.</span><span class="sxs-lookup"><span data-stu-id="facda-206">For **File format**, click either **Base 64** or **Binary**.</span></span> <span data-ttu-id="facda-207">Выберите **Base 64** , если вы не указали, что в противном случае поставщик для ваших сертификатов.</span><span class="sxs-lookup"><span data-stu-id="facda-207">Select **Base 64** unless you are instructed otherwise by the vendor for your certificates.</span></span>

20. <span data-ttu-id="facda-208">Найдите файл запроса, сохраненный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="facda-208">Locate the request file that you saved in the previous step.</span></span> <span data-ttu-id="facda-209">Отправьте свой общедоступный центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="facda-209">Submit to your public certification authority.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="facda-210">Корпорация Майкрософт выявила общедоступные центры сертификации, удовлетворяющие требованиям для объединенных коммуникаций.</span><span class="sxs-lookup"><span data-stu-id="facda-210">Microsoft has identified Public CAs that meets the requirements for Unified Communications purposes.</span></span> <span data-ttu-id="facda-211">Список сохранен в следующей статье базы знаний.</span><span class="sxs-lookup"><span data-stu-id="facda-211">A list is maintained in the following knowledge base article.</span></span> <A href="https://go.microsoft.com/fwlink/?linkid=282625">https://go.microsoft.com/fwlink/?LinkId=282625</A>

    
    <span data-ttu-id="facda-212"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="facda-212"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

