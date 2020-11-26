---
title: 'Lync Server 2013: требования службы автоматического обнаружения'
description: 'Lync Server 2013: требования к службе автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Autodiscover service requirements
ms:assetid: 0ac5dbf7-9acd-4d25-b21a-932022b8b983
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690012(v=OCS.15)
ms:contentKeyID: 48183368
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61e963bc9e921cc0a571f63d4be50f09d237c2dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438129"
---
# <a name="autodiscover-service-requirements-for-lync-server-2013"></a><span data-ttu-id="2589c-103">Требования службы автоматического обнаружения для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2589c-103">Autodiscover service requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2589c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2589c-104">

<span> </span></span></span>

<span data-ttu-id="2589c-105">_**Тема последнего изменения:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="2589c-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="2589c-106">Служба автообнаружения Microsoft Lync Server 2013 работает на серверах пула и интерфейсах, а также при публикации в DNS может использоваться мобильными устройствами Lync Mobile для поиска служб Mobility Service.</span><span class="sxs-lookup"><span data-stu-id="2589c-106">The Microsoft Lync Server 2013 Autodiscover Service runs on the Director and Front End pool servers, and when published in DNS, can be used by mobile devices running Lync Mobile to locate mobility services.</span></span> <span data-ttu-id="2589c-107">Перед тем как мобильные устройства с Lync Mobile смогут использовать преимущества автоматического обнаружения, вам нужно будет изменить список альтернативных имен субъектов сертификата на любом сетевом сервере, на котором запущена служба автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="2589c-107">Before mobile devices running Lync Mobile can take advantage of automatic discovery, you need to modify certificate subject alternative name lists on any Director and Front End Server running the Autodiscover Service.</span></span> <span data-ttu-id="2589c-108">Кроме того, может потребоваться изменить список альтернативных имен субъектов в сертификатах, используемых для использования внешних правил публикации веб-службы на обратных прокси.</span><span class="sxs-lookup"><span data-stu-id="2589c-108">In addition, it may be necessary to modify the subject alternative name lists on certificates used for external web service publishing rules on reverse proxies.</span></span>

<span data-ttu-id="2589c-109">Дополнительные сведения об элементах альтернативных имен тем, необходимых для режиссеров, серверов переднего плана и обратного доступа, можно найти в статьях [технические требования для мобильных устройств в Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md) в планирование для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2589c-109">For details about the subject alternative name entries that are required for Directors, Front End Servers, and reverse proxies, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md) in Planning for Mobility.</span></span>

<span data-ttu-id="2589c-110">Решение о том, как использовать списки альтернативных имен для субъектов в обратных прокси-серверах, зависит от того, публикуются ли служба автообнаружения для порта 80 или для порта 443:</span><span class="sxs-lookup"><span data-stu-id="2589c-110">The decision about using subject alternative name lists on reverse proxies is based on whether you publish the Autodiscover Service on port 80 or on port 443:</span></span>

  - <span data-ttu-id="2589c-111">**Опубликовано на порте 80**   Если первый запрос к службе автообнаружения находится на порту 80, никаких изменений в сертификате не требуется.</span><span class="sxs-lookup"><span data-stu-id="2589c-111">**Published on port 80**   No certificate changes are required if the initial query to the Autodiscover Service occurs over port 80.</span></span> <span data-ttu-id="2589c-112">Это связано с тем, что мобильные устройства Lync будут получать доступ к обратному прокси-серверу на порте 80 извне, а затем перенаправляться на директорию или сервер переднего плана с помощью внутреннего порта 8080.</span><span class="sxs-lookup"><span data-stu-id="2589c-112">This is because mobile devices running Lync will access the reverse proxy on port 80 externally and then be redirected to a Director or Front End Server on port 8080 internally.</span></span> <span data-ttu-id="2589c-113">Подробнее читайте в разделе "начальный процесс автообнаружения с помощью порта 80" ниже в этой статье.</span><span class="sxs-lookup"><span data-stu-id="2589c-113">For details, see the “Initial Autodiscover Process Using Port 80” section later in this topic.</span></span>

  - <span data-ttu-id="2589c-114">**Опубликовано на порте 443**   Список альтернативных имен субъектов в сертификатах, используемых внешним правилом публикации веб-служб, должен содержать *lyncdiscover. \<sipdomain\>*</span><span class="sxs-lookup"><span data-stu-id="2589c-114">**Published on port 443**   The subject alternative name list on certificates used by the external web services publishing rule must contain a *lyncdiscover.\<sipdomain\>*</span></span> <span data-ttu-id="2589c-115">запись для каждого домена SIP в Организации.</span><span class="sxs-lookup"><span data-stu-id="2589c-115">entry for each SIP domain within your organization.</span></span>

<span data-ttu-id="2589c-116">Повторное выдача сертификатов с помощью внутреннего центра сертификации обычно является простым процессом, но для общедоступных сертификатов, используемых в правиле публикации веб-службы, может привести к дорогостоящему вводу нескольких альтернативных имен субъектов.</span><span class="sxs-lookup"><span data-stu-id="2589c-116">Reissuing certificates using an internal certificate authority is typically a simple process but for public certificates used on the web service publishing rule, adding multiple subject alternative name entries can become expensive.</span></span> <span data-ttu-id="2589c-117">Для решения этой проблемы мы поддерживаем начальное подключение автоматического обнаружения через порт 80, который затем перенаправляется на порт 8080 на сервере директора или на внешнем клиенте.</span><span class="sxs-lookup"><span data-stu-id="2589c-117">To work around this issue, we support the initial automatic discovery connection over port 80, which is then redirected to port 8080 on the Director or Front End Server.</span></span>

<span data-ttu-id="2589c-118">Например, предположим, что мобильный клиент, на котором запущен Lync Mobile, настроен для входа на Lync Server 2013 с помощью функции автоматического обнаружения, использующей HTTP для первоначального запроса.</span><span class="sxs-lookup"><span data-stu-id="2589c-118">For example, assume that a mobile client running Lync Mobile is configured to sign in to Lync Server 2013 using the automatic discovery feature using HTTP for the initial request.</span></span>

<div>

## <a name="initial-autodiscover-process-for-mobile-devices-using-port-80"></a><span data-ttu-id="2589c-119">Первоначальный процесс автообнаружения для мобильных устройств с помощью порта 80</span><span class="sxs-lookup"><span data-stu-id="2589c-119">Initial Autodiscover Process for Mobile Devices Using Port 80</span></span>

1.  <span data-ttu-id="2589c-120">Мобильное устройство, на котором работает Lync Mobile, ищет lyncdiscover.contoso.com с помощью DNS, где есть запись A.</span><span class="sxs-lookup"><span data-stu-id="2589c-120">Mobile device running Lync Mobile looks up lyncdiscover.contoso.com using DNS, where an A record exists.</span></span>

2.  <span data-ttu-id="2589c-121">Внешняя служба DNS возвращает клиенту IP-адрес внешней веб-службы.</span><span class="sxs-lookup"><span data-stu-id="2589c-121">External DNS returns the IP address for the external web services to the client.</span></span>

3.  <span data-ttu-id="2589c-122">Мобильное устройство, на котором работает Lync Mobile, отправляет запрос http://lyncdiscover.contoso.com?sipuri=lyncUser1@contoso.com обратному прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="2589c-122">Mobile device running Lync Mobile sends request http://lyncdiscover.contoso.com?sipuri=lyncUser1@contoso.com to the reverse proxy</span></span>

4.  <span data-ttu-id="2589c-123">Правило веб-публикации будет переносить запрос с порта 80 извне на порт 8080 для внутренних целей, который затем будет перенаправлен на сервер, на котором разносится режиссер.</span><span class="sxs-lookup"><span data-stu-id="2589c-123">The web publishing rule will bridge the request from port 80 externally to port 8080 internally, which will then route it to either a Director or Front End Server.</span></span>
    
    <span data-ttu-id="2589c-124">Так как запрос является HTTP и не HTTPS, сертификат в правиле публикации внешней веб-службы не требует никаких изменений для поддержки службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="2589c-124">Since the request is HTTP and not HTTPS, no modifications are needed to the certificate on the external web service publishing rule to support the Autodiscover Service.</span></span>

5.  <span data-ttu-id="2589c-125">Служба автообнаружения возвращает URL-адреса внешней веб-службы (в формате HTTPS).</span><span class="sxs-lookup"><span data-stu-id="2589c-125">The Autodiscover Service returns the external web service URLs (in HTTPS format).</span></span>

6.  <span data-ttu-id="2589c-126">Мобильное устройство, работающее под управлением Lync Mobile, может повторно подключиться к обратному прокси-серверу на порте 443 и перенаправляться на службу Mobility Service, запущенную на домашнем пуле пользователей, в 4443.</span><span class="sxs-lookup"><span data-stu-id="2589c-126">The mobile device running Lync Mobile can then reconnect to the reverse proxy on port 443 and is redirected over 4443 to the mobility service running on the user’s home pool.</span></span>
    
    <span data-ttu-id="2589c-127">Поскольку запрос HTTPS относится к URL-адресу внешней веб-службы или URL-адресу службы автообнаружения, он завершается успешно, так как сертификат уже содержит записи альтернативного имени для внешних доменных имен (FQDN) внешней веб-службы.</span><span class="sxs-lookup"><span data-stu-id="2589c-127">Since the HTTPS query is to the external web services URL vs. the Autodiscover Service URL, it succeeds because the certificate will already contain subject alternative name entries for the external web services fully qualified domain names (FQDNs).</span></span>
    
    <span data-ttu-id="2589c-128">В этом сценарии для поддержки мобильных устройств не требуется никаких изменений сертификата.</span><span class="sxs-lookup"><span data-stu-id="2589c-128">In this scenario, there are no certificate changes required to support mobility.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2589c-129">Если на целевом веб-сервере есть сертификат, у которого нет совпадающего значения для lyncdiscover.contoso.com в качестве альтернативного значения списка имен субъектов:</span><span class="sxs-lookup"><span data-stu-id="2589c-129">If the target web server has a certificate that does not have a matching value for lyncdiscover.contoso.com as a subject alternative name list value:</span></span><BR><span data-ttu-id="2589c-130">а. &nbsp; &nbsp; &nbsp; Веб-сервер отвечает на запросы "сервер Hello" и не имеет сертификата.</span><span class="sxs-lookup"><span data-stu-id="2589c-130">a.&nbsp;&nbsp;&nbsp;Web server responds with a “Server Hello” and no certificate.</span></span><BR><span data-ttu-id="2589c-131">b. &nbsp; &nbsp; &nbsp; Мобильное устройство с Lync Mobile немедленно завершает сеанс.</span><span class="sxs-lookup"><span data-stu-id="2589c-131">b.&nbsp;&nbsp;&nbsp;Mobile device running Lync Mobile immediately terminates the session.</span></span><BR><span data-ttu-id="2589c-132">Если на целевом веб-сервере есть сертификат, включающий lyncdiscover.contoso.com в качестве альтернативного значения списка имен, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2589c-132">If the target web server has a certificate that includes lyncdiscover.contoso.com as a subject alternative name list value:</span></span><BR><span data-ttu-id="2589c-133">а. &nbsp; &nbsp; &nbsp; Веб-сервер отвечает на запросы "Hello Server" и сертификат.</span><span class="sxs-lookup"><span data-stu-id="2589c-133">a.&nbsp;&nbsp;&nbsp;Web server responds with a “Server hello” and a certificate.</span></span><BR><span data-ttu-id="2589c-134">b. &nbsp; &nbsp; &nbsp; Мобильное устройство, на котором работает Lync Mobile, проверяет сертификат и завершает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2589c-134">b.&nbsp;&nbsp;&nbsp;Mobile device running Lync Mobile validates the certificate and completes the handshake.</span></span>

    
    </div>

<span data-ttu-id="2589c-135">Для поддержки первоначального подключения к службе автообнаружения с помощью порта 80 на обратном прокси-сервере вы можете создать правило публикации HTTP, аналогичное приведенному в этом примере для правила обратной прокси-публикации шлюза Forefront Threat Management 2010:</span><span class="sxs-lookup"><span data-stu-id="2589c-135">To support an initial connection to the Autodiscover Service using port 80 on your reverse proxy server, you can create an http publishing rule similar to this example for a Forefront Threat Management Gateway 2010 reverse proxy web publishing rule:</span></span>

1.  <span data-ttu-id="2589c-136">Создайте новое правило веб-публикации (например, **Lync Server автообнаружения (http)**).</span><span class="sxs-lookup"><span data-stu-id="2589c-136">Create a new web publishing rule (for example, **Lync Server Autodiscover (HTTP)**).</span></span>

2.  <span data-ttu-id="2589c-137">В **общедоступном имени** введите lyncdiscover.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="2589c-137">In **Public Name**, enter lyncdiscover.contoso.com.</span></span>

3.  <span data-ttu-id="2589c-138">На вкладке **мосты** выберите только один из вариантов: переносить запросы с порта 80 на 8080.</span><span class="sxs-lookup"><span data-stu-id="2589c-138">On the **Bridging** tab, select only the option to bridge requests from Port 80 to Port 8080.</span></span>

4.  <span data-ttu-id="2589c-139">На вкладке **Проверка подлинности** выберите вариант **без проверки подлинности**, и **клиент не может пройти проверку подлинности напрямую**.</span><span class="sxs-lookup"><span data-stu-id="2589c-139">On the **Authentication** tab, select **No authentication**, and **Client cannot authenticate directly**.</span></span>

5.  <span data-ttu-id="2589c-140">Зафиксировать изменения и переместить правило в верхнюю часть списка правил Lync (первый в заказе на обработку).</span><span class="sxs-lookup"><span data-stu-id="2589c-140">Commit changes, and move the rule to the top of the list of Lync rules (first in processing order).</span></span>

</div>

<div>

## <a name="mobility-for-the-split-domain-deployment"></a><span data-ttu-id="2589c-141">Мобильность для раздельного развертывания доменов</span><span class="sxs-lookup"><span data-stu-id="2589c-141">Mobility for the Split Domain Deployment</span></span>

<span data-ttu-id="2589c-142">Общее адресное пространство SIP, также называемое *разделенным доменом*, или *гибридное развертывание* — это конфигурация, в которой пользователи развертываются в рамках локального развертывания и в веб-среде.</span><span class="sxs-lookup"><span data-stu-id="2589c-142">A shared SIP address space, also known as a *split-domain*, or a *hybrid deployment* is a configuration where users are deployed across an on-premise deployment and an online environment.</span></span> <span data-ttu-id="2589c-143">Желаемый результат состоит в том, что пользователь, независимо от того, где расположен домашний сервер (локально или в сети), может войти в развертывание и перенаправить его на расположение на основном сервере.</span><span class="sxs-lookup"><span data-stu-id="2589c-143">The desired outcome is to have a user, regardless of where their home server is located (on-premise or online), to log into the deployment and be redirected to their home server location.</span></span> <span data-ttu-id="2589c-144">Для этого функция автообнаружения Microsoft Lync Server 2013 используется для перенаправления пользователя Online в Интернет-топологию.</span><span class="sxs-lookup"><span data-stu-id="2589c-144">To accomplish this, the Autodiscover feature of Microsoft Lync Server 2013 is used to redirect the online user to the online topology.</span></span> <span data-ttu-id="2589c-145">Это можно сделать, настроив указатель URL-адреса автообнаружения с помощью командной консоли Lync Server Management Shell и командлетов **Get-CsHostingProvider** и **Set-CsHostingProvider**.</span><span class="sxs-lookup"><span data-stu-id="2589c-145">This is done by configuring the Autodiscover uniform resource locator (URL) by using the Lync Server Management Shell and the cmdlets **Get-CsHostingProvider** and **Set-CsHostingProvider**.</span></span>

<span data-ttu-id="2589c-146">Вам потребуется собрать и записать следующие развернутые атрибуты:</span><span class="sxs-lookup"><span data-stu-id="2589c-146">You will need to collect and record the following deployed attributes:</span></span>

  - <span data-ttu-id="2589c-147">В командной консоли Lync Server введите</span><span class="sxs-lookup"><span data-stu-id="2589c-147">From the Lync Server Management Shell, type</span></span>
    
        Get-CsHostingProvider

  - <span data-ttu-id="2589c-148">В результатах найдите Интернет-провайдер с атрибутом **ProxyFQDN**.</span><span class="sxs-lookup"><span data-stu-id="2589c-148">In the results, find the online provider with the attribute **ProxyFQDN**.</span></span> <span data-ttu-id="2589c-149">Например, sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="2589c-149">For example, sipfed.online.lync.com</span></span>

  - <span data-ttu-id="2589c-150">Запишите значение элемента ProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="2589c-150">Record the value of the ProxyFQDN</span></span>

  - <span data-ttu-id="2589c-151">Включите Федерацию на локальной панели управления Lync Server, разрешая Федерацию с помощью веб-поставщика.</span><span class="sxs-lookup"><span data-stu-id="2589c-151">Enable federation in the on-premise Lync Server Control Panel, allowing federation with the online provider</span></span>

  - <span data-ttu-id="2589c-152">Включите Федерацию для поставщика услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="2589c-152">Enable federation for the online provider.</span></span> <span data-ttu-id="2589c-153">По умолчанию все пользователи в сети включены в доменную Федерацию и могут взаимодействовать со всеми доменами.</span><span class="sxs-lookup"><span data-stu-id="2589c-153">By default, all online users are enabled for domain federation and can communicate with all domains</span></span>

  - <span data-ttu-id="2589c-154">Если вы определяете блокируемые и разрешенные домены, определите домены, которые будут явно разрешены или явно заблокированы</span><span class="sxs-lookup"><span data-stu-id="2589c-154">If you will define blocked and allowed domains, determine the domains that you will explicitly allow or explicitly block</span></span>

  - <span data-ttu-id="2589c-155">Для Интернет-интеграции необходимо планировать исключения брандмауэра, сертификаты и узел DNS (A или AAAA, если используется IPv6).</span><span class="sxs-lookup"><span data-stu-id="2589c-155">For online federation, you must plan for firewall exceptions, certificates and DNS host (A or AAAA, if using IPv6) records.</span></span> <span data-ttu-id="2589c-156">Кроме того, необходимо настроить политики Федерации.</span><span class="sxs-lookup"><span data-stu-id="2589c-156">Additionally, you must configure federation policies.</span></span> <span data-ttu-id="2589c-157">Подробные сведения можно найти в разделе [планирование для Lync server 2013 и Office Communications Server Federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md)</span><span class="sxs-lookup"><span data-stu-id="2589c-157">For details, see [Planning for Lync Server 2013 and Office Communications Server federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md)</span></span>

<span data-ttu-id="2589c-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2589c-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

