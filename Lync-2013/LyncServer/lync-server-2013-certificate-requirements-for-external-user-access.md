---
title: 'Lync Server 2013: требования к сертификатам для доступа внешних пользователей'
description: 'Lync Server 2013: требования к сертификату для внешних пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for external user access
ms:assetid: d45b6b10-556f-4b10-b1a7-fb0d0a64a498
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398920(v=OCS.15)
ms:contentKeyID: 48185503
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4701037aeba3ab6a4e51bf117efaa3aecc0f5084
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435371"
---
# <a name="certificate-requirements-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="b03b8-103">Требования к сертификатам для доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b03b8-103">Certificate requirements for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b03b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b03b8-104">

<span> </span></span></span>

<span data-ttu-id="b03b8-105">_**Тема последнего изменения:** 2016-03-29_</span><span class="sxs-lookup"><span data-stu-id="b03b8-105">_**Topic Last Modified:** 2016-03-29_</span></span>

<span data-ttu-id="b03b8-106">Коммуникационное программное обеспечение Microsoft Lync Server 2013 поддерживает использование единого общедоступного сертификата для доступа к внешним интерфейсам Access и веб-конференций EDGE, а также службы проверки подлинности (V).</span><span class="sxs-lookup"><span data-stu-id="b03b8-106">Microsoft Lync Server 2013 communications software supports the use of a single public certificate for access and web conferencing Edge external interfaces, plus the A/V Authentication service.</span></span> <span data-ttu-id="b03b8-107">Внутренний интерфейс EDGE обычно использует частный сертификат, выданный внутренним центром сертификации (ЦС), но также может использовать общедоступный сертификат, если он предоставлен доверенным общедоступным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="b03b8-107">The Edge internal interface typically uses a private certificate issued by an internal certification authority (CA), but can also use a public certificate, provided that it is from a trusted public CA.</span></span> <span data-ttu-id="b03b8-108">При обратном прокси-сервере в развертывании используется общедоступный сертификат и шифруются данные, передаваемые через обратное прокси-сервер, на внутренние серверы с помощью HTTP (то есть для обеспечения безопасности транспортного уровня по протоколу HTTP).</span><span class="sxs-lookup"><span data-stu-id="b03b8-108">The reverse proxy in your deployment uses a public certificate and encrypts the communication from the reverse proxy to clients and the reverse proxy to internal servers by using HTTP (that is, Transport Layer Security over HTTP).</span></span>

<span data-ttu-id="b03b8-109">Ниже приведены требования для общедоступного сертификата, используемого для внешних интерфейсов Access и веб-конференций, а также службы для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b03b8-109">Following are the requirements for the public certificate used for access and web conferencing Edge external interfaces, and the A/V authentication service:</span></span>

  - <span data-ttu-id="b03b8-110">Сертификат должен быть выдан утвержденным общедоступным центром сертификации, который поддерживает дополнительное имя субъекта.</span><span class="sxs-lookup"><span data-stu-id="b03b8-110">The certificate must be issued by an approved public CA that supports subject alternative name.</span></span> <span data-ttu-id="b03b8-111">Дополнительные сведения можно найти в статье 929395 базы знаний Майкрософт "партнеры по сертификатам единой системы связи для Exchange Server и Communications Server" на [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) .</span><span class="sxs-lookup"><span data-stu-id="b03b8-111">For details, see Microsoft Knowledge Base article 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

  - <span data-ttu-id="b03b8-112">Если сертификат будет использоваться в пуле EDGE, он должен быть создан как экспортируемый с использованием того же сертификата, который используется на каждом пограничном сервере в пуле Edge.</span><span class="sxs-lookup"><span data-stu-id="b03b8-112">If the certificate will be used on an Edge pool, it must be created as exportable, with the same certificate used on each Edge Server in the Edge pool.</span></span> <span data-ttu-id="b03b8-113">Требование для экспорта закрытого ключа предназначено для работы со службой проверки подлинности A/V, которая должна использовать один и тот же закрытый ключ для всех пограничных серверов в пуле.</span><span class="sxs-lookup"><span data-stu-id="b03b8-113">The exportable private key requirement is for the purposes of the A/V Authentication service, which must use the same private key across all Edge Servers in the pool.</span></span>

  - <span data-ttu-id="b03b8-114">Если вы хотите максимально увеличить время бесперебойной работы для аудио-и видеослужб, ознакомьтесь с требованиями к сертификату для реализации сертификата службы пограничного сервера (то есть отдельного сертификата службы EDGE в других внешних целях сертификации).</span><span class="sxs-lookup"><span data-stu-id="b03b8-114">If you want to maximize the uptime for your Audio/Video services, review the certificate requirements for implementing a decoupled A/V Edge service certificate (that is, a separate A/V Edge service certificate from the other External Edge certificate purposes).</span></span> <span data-ttu-id="b03b8-115">Дополнительные сведения можно найти [в разделе изменения в Lync server 2013, которые влияют на планирование пограничного сервера](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md), [Планирование сертификатов пограничного сервера в Lync Server 2013](lync-server-2013-plan-for-edge-server-certificates.md) и [промежуточный выпуск и сертификаты OAuth в Lync Server 2013 с помощью Set-CsCertificate](lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate).</span><span class="sxs-lookup"><span data-stu-id="b03b8-115">For details, see [Changes in Lync Server 2013 that affect Edge Server planning](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md), [Plan for Edge Server certificates in Lync Server 2013](lync-server-2013-plan-for-edge-server-certificates.md) and [Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate](lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate).</span></span>

  - <span data-ttu-id="b03b8-116">Имя субъекта сертификата — это полное доменное имя (FQDN) или IP-адрес аппаратной подсистемы балансировки нагрузки (например, access.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="b03b8-116">The subject name of the certificate is the Access Edge service external interface fully qualified domain name (FQDN) or hardware load balancer VIP (for example, access.contoso.com).</span></span> <span data-ttu-id="b03b8-117">).</span><span class="sxs-lookup"><span data-stu-id="b03b8-117">).</span></span> <span data-ttu-id="b03b8-118">Имя субъекта не может содержать подстановочный знак, оно должно быть явным именем.</span><span class="sxs-lookup"><span data-stu-id="b03b8-118">The subject name can’t have a wildcard character, it must be an explicit name.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b03b8-119">Для Lync Server 2013 этот параметр больше не является обязательным, но рекомендуется для обеспечения совместимости с Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="b03b8-119">For Lync Server 2013, this is no longer a requirement, but it is still recommended for compatibility with Office Communications Server.</span></span>

    
    </div>

  - <span data-ttu-id="b03b8-120">В списке "альтернативное имя темы" указаны полные доменные имена для указанных ниже элементов.</span><span class="sxs-lookup"><span data-stu-id="b03b8-120">The subject alternative name list contains the FQDNs of the following:</span></span>
    
      - <span data-ttu-id="b03b8-121">IP-адрес внешнего интерфейса службы EDGE или подсистемы балансировки нагрузки для оборудования (например, sip.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="b03b8-121">The Access Edge service external interface or hardware load balancer VIP (for example, sip.contoso.com).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="b03b8-122">Несмотря на то, что имя субъекта сертификата совпадает с полным доменным именем для доступа, альтернативное имя субъекта должно также содержать доступ к краю, так как для проверки подлинности имени субъекта используются записи альтернативного имени субъекта (TLS).</span><span class="sxs-lookup"><span data-stu-id="b03b8-122">Even though the certificate subject name is equal to the access Edge FQDN, the subject alternative name must also contain the access Edge FQDN because Transport Layer Security (TLS) ignores the subject name and uses the subject alternative name entries for validation.</span></span>

        
        </div>
    
      - <span data-ttu-id="b03b8-123">Внешний интерфейс или VIP подсистемы балансировки нагрузки для веб-конференций (например, webcon.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="b03b8-123">The web conferencing Edge external interface or hardware load balancer VIP (for example, webcon.contoso.com).</span></span>
    
      - <span data-ttu-id="b03b8-124">Если вы используете клиентскую автоматическую настройку или Федерацию, включите также доменные имена SIP, используемые в вашей компании (например, sip.contoso.com, sip.fabrikam.com).</span><span class="sxs-lookup"><span data-stu-id="b03b8-124">If you are using client auto-configuration or federation, also include any SIP domain FQDNs used within your company (for example, sip.contoso.com, sip.fabrikam.com).</span></span>
    
      - <span data-ttu-id="b03b8-125">Служба EDGE (A/V) не использует имя субъекта или записи альтернативных имен субъектов.</span><span class="sxs-lookup"><span data-stu-id="b03b8-125">The A/V Edge service does not use the subject name or the subject alternative names entries.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b03b8-126">Порядок полных доменных имен в списке "альтернативные имена субъектов" не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="b03b8-126">The order of the FQDNs in the subject alternative names list does not matter.</span></span>

    
    </div>

<span data-ttu-id="b03b8-127">Если вы развертываете на сайте несколько высокодоступных пограничных серверов, сертификат службы проверки подлинности A/V, установленный на каждом пограничном сервере, должен находиться в одном центре сертификации и использовать один и тот же закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="b03b8-127">If you are deploying multiple, load-balanced Edge Servers at a site, the A/V authentication service certificate that is installed on each Edge Server must be from the same CA and must use the same private key.</span></span> <span data-ttu-id="b03b8-128">Обратите внимание, что закрытый ключ сертификата должен быть экспортирован, независимо от того, используется ли он на одном пограничном сервере или на нескольких пограничных серверах.</span><span class="sxs-lookup"><span data-stu-id="b03b8-128">Note that the certificate's private key must be exportable, regardless of whether it is used on one Edge Server or many Edge Servers.</span></span> <span data-ttu-id="b03b8-129">Кроме того, он должен быть экспортирован, если вы запрашиваете сертификат на любом компьютере, кроме пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="b03b8-129">It must also be exportable if you request the certificate from any computer other than the Edge Server.</span></span> <span data-ttu-id="b03b8-130">Поскольку служба проверки подлинности A/V не использует имя субъекта или альтернативное имя субъекта, вы можете повторно использовать сертификат EDGE, пока для него выполняются требования к имени субъекта и тематике, а закрытый ключ сертификата является экспортируемым.</span><span class="sxs-lookup"><span data-stu-id="b03b8-130">Because the A/V authentication service does not use the subject name or subject alternative name, you can reuse the access Edge certificate as long as the subject name and subject alternative name requirements are met for the access Edge and the web conferencing Edge and the certificate’s private key is exportable.</span></span>

<span data-ttu-id="b03b8-131">Требования для частного (или общего) сертификата, используемого для внутреннего интерфейса EDGE, описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="b03b8-131">Requirements for the private (or public) certificate used for the Edge internal interface are as follows:</span></span>

  - <span data-ttu-id="b03b8-132">Сертификат может быть выдан внутренним центром сертификации или утвержденным центром сертификации общедоступного сертификата.</span><span class="sxs-lookup"><span data-stu-id="b03b8-132">The certificate can be issued by an internal CA or an approved public certificate CA.</span></span>

  - <span data-ttu-id="b03b8-133">Имя субъекта сертификата обычно является полным доменным именем внутренней или аппаратной подсистемой балансировки нагрузки (например, lsedge.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="b03b8-133">The subject name of the certificate is typically the Edge internal interface FQDN or hardware load balancer VIP (for example, lsedge.contoso.com).</span></span> <span data-ttu-id="b03b8-134">Однако вы можете использовать для внутренних целей сертификат с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="b03b8-134">However, you can use a wildcard certificate on the Edge internal.</span></span>

  - <span data-ttu-id="b03b8-135">Список альтернативных имен для темы не требуется.</span><span class="sxs-lookup"><span data-stu-id="b03b8-135">No subject alternative name list is required.</span></span>

<span data-ttu-id="b03b8-136">Обратный прокси-сервер в запросах служб развертывания:</span><span class="sxs-lookup"><span data-stu-id="b03b8-136">The reverse proxy in your deployment services requests for:</span></span>

  - <span data-ttu-id="b03b8-137">Доступ внешних пользователей к содержимому собраний для собраний</span><span class="sxs-lookup"><span data-stu-id="b03b8-137">External user access to meeting content for meetings</span></span>

  - <span data-ttu-id="b03b8-138">Доступ внешних пользователей к развернутым и отображаемым членам групп рассылки</span><span class="sxs-lookup"><span data-stu-id="b03b8-138">External user access to expand and display members of distribution groups</span></span>

  - <span data-ttu-id="b03b8-139">Доступ внешних пользователей к файлам, загружаемым из службы адресной книги</span><span class="sxs-lookup"><span data-stu-id="b03b8-139">External user access to downloadable files from the Address Book Service</span></span>

  - <span data-ttu-id="b03b8-140">Доступ внешних пользователей к клиенту Lync Web App</span><span class="sxs-lookup"><span data-stu-id="b03b8-140">External user access to the Lync Web App client</span></span>

  - <span data-ttu-id="b03b8-141">Доступ внешних пользователей к веб-странице параметров конференций с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="b03b8-141">External user access to the Dial-in Conferencing Settings web page</span></span>

  - <span data-ttu-id="b03b8-142">Доступ внешних пользователей к службе сведений о расположении</span><span class="sxs-lookup"><span data-stu-id="b03b8-142">External user access to the Location Information Service</span></span>

  - <span data-ttu-id="b03b8-143">Доступ к службе обновления устройства и получение обновлений на внешнем устройстве</span><span class="sxs-lookup"><span data-stu-id="b03b8-143">External device access to the Device Update Service and obtain updates</span></span>

<span data-ttu-id="b03b8-144">Обратный прокси публикует URL-адреса внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="b03b8-144">The reverse proxy publishes the internal server Web Components URLs.</span></span> <span data-ttu-id="b03b8-145">URL-адреса сайтов определяются на сайте режиссера, внешнем сервере или пуле переднего плана в качестве **внешних веб-служб** в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="b03b8-145">The Web Components URLs are defined on the Director, Front End Server or Front End pool as the **External web services** in Topology Builder.</span></span>

<span data-ttu-id="b03b8-146">Подстановочные знаки поддерживаются в поле «альтернативное имя темы» сертификата, назначенного обратному прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="b03b8-146">Wildcard entries are supported in the subject alternative name field of the certificate assigned to the reverse proxy.</span></span> <span data-ttu-id="b03b8-147">Подробнее о том, как настроить запрос на сертификат для обратного прокси-сервера, см. [в разделе запрос и Настройка сертификата для обратного прокси-сервера HTTP в Lync Server 2013](lync-server-2013-request-and-configure-a-certificate-for-your-reverse-http-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="b03b8-147">For details about how to configure the certificate request for the reverse proxy, see [Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013](lync-server-2013-request-and-configure-a-certificate-for-your-reverse-http-proxy.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="b03b8-148">См. также</span><span class="sxs-lookup"><span data-stu-id="b03b8-148">See Also</span></span>


[<span data-ttu-id="b03b8-149">Поддержка групповых сертификатов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b03b8-149">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="b03b8-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b03b8-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

