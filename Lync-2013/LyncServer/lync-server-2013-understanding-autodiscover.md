---
title: 'Lync Server 2013: Общие сведения о автообнаружения'
description: 'Lync Server 2013: Общие сведения о автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Autodiscover
ms:assetid: d70a15b7-750b-4e0f-9a7f-0254d6d486c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945654(v=OCS.15)
ms:contentKeyID: 51541522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 295aba4bffbe5d17070702203cfd933284cb12c0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399493"
---
# <a name="understanding-autodiscover-in-lync-server-2013"></a><span data-ttu-id="f0953-103">Общие сведения о автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0953-103">Understanding Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0953-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0953-104">

<span> </span></span></span>

<span data-ttu-id="f0953-105">_**Тема последнего изменения:** 2013-06-03_</span><span class="sxs-lookup"><span data-stu-id="f0953-105">_**Topic Last Modified:** 2013-06-03_</span></span>

<span data-ttu-id="f0953-106">Служба автообнаружения Lync Server 2013 — это функция, которая первоначально появилась в Microsoft Lync Server 2010 в рамках накопительного обновления для Lync Server 2010: Ноябрь 2011 г.</span><span class="sxs-lookup"><span data-stu-id="f0953-106">The Lync Server 2013 Autodiscover Service is a feature that was originally introduced in Microsoft Lync Server 2010 as part of the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="f0953-107">Помимо исправлений, это накопительное обновление доставлено поддержку клиентам Lync Mobile и Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f0953-107">In addition to fixes, this cumulative update delivered support for Lync Mobile and Lync 2013 clients.</span></span>

<span data-ttu-id="f0953-108">В Lync Server 2013 служба автообнаружения является неотъемлемой частью функционирования внешних и внутренних мобильных клиентов, а также расширяет возможности автообнаружения для новых клиентов, например недавно появившегося приложения Lync из Магазина Windows для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0953-108">In Lync Server 2013, the Autodiscover Service is an integral part of the operation of external and internal mobile clients, and Autodiscover is also extended to new clients, such as the recently introduced Lync Windows Store app for Windows 8.</span></span> <span data-ttu-id="f0953-109">Автообнаружение также используется клиентами Lync 2013 для настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f0953-109">Autodiscover is also used by the Lync 2013 desktop clients.</span></span> <span data-ttu-id="f0953-110">Служба автообнаружения распознается в Lync Server требуемыми записями DNS (Domain Name System) **lyncdiscover. \<domain\>**</span><span class="sxs-lookup"><span data-stu-id="f0953-110">Autodiscover is recognized in Lync Server by the required domain name system (DNS) records **lyncdiscover.\<domain\>**</span></span> <span data-ttu-id="f0953-111">и **lyncdiscoverinternal. \<domain\>**.</span><span class="sxs-lookup"><span data-stu-id="f0953-111">and **lyncdiscoverinternal.\<domain\>**.</span></span> <span data-ttu-id="f0953-112">Кроме того, более новые версии Lync 2010 и Lync 2013 для настольных компьютеров предпочитают автообнаружения на SRV-записях DNS (Domain Name System), используя DNS SRV-записи только в том случае, если lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="f0953-112">Additionally, newer versions of the Lync 2010 and Lync 2013 desktop client prefer Autodiscover over the domain name system (DNS) SRV records, using DNS SRV records only if lyncdiscover.\<domain\></span></span> <span data-ttu-id="f0953-113">или lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="f0953-113">or lyncdiscoverinternal.\<domain\></span></span> <span data-ttu-id="f0953-114">не отвечает на запросы и не разрешается.</span><span class="sxs-lookup"><span data-stu-id="f0953-114">does not respond or does not resolve.</span></span> <span data-ttu-id="f0953-115">Приложение Lync из Магазина Windows для Windows 8 и Lync Mobile использует функцию автообнаружения исключительно и не будет ссылаться на традиционные DNS SRV-записи.</span><span class="sxs-lookup"><span data-stu-id="f0953-115">The Lync Windows Store app for Windows 8 and Lync Mobile uses Autodiscover exclusively and will not refer to the traditional DNS SRV records.</span></span>

<span data-ttu-id="f0953-116">В Lync Server 2013 функция автообнаружения расширяется для связи с клиентом, какие элементы, функции и методы связи доступны для клиента.</span><span class="sxs-lookup"><span data-stu-id="f0953-116">In Lync Server 2013, Autodiscover is expanded to communicate to the client which elements, features, and communication methods are available to the client.</span></span> <span data-ttu-id="f0953-117">Информация передается через запрос, отправленный клиентом, и веб-службы Lync Server отвечают на явно определенный ответ, который называет сведения о доступности клиента, и о том, как обращаться к этим функциям в формате документа ответа автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="f0953-117">The information is communicated through a request that is sent from the client, and the Lync Server web services responds with a clearly defined response that names what is available to the client, and how to contact those features in the format of the Autodiscover Response document.</span></span>

<span data-ttu-id="f0953-118">Лучший способ понять документ ответа автообнаружения, в том числе о том, как веб-службы обмениваются функциями с клиентами через этот документ, — это dissect и определять каждую строку в типичном ответе от документа ответа автообнаружения веб-службы Lync.</span><span class="sxs-lookup"><span data-stu-id="f0953-118">The best way to understand the Autodiscover response document, including how the web services communicate features to clients through this document, is to dissect and define each line in a typical response from the Lync web service Autodiscover response document.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="f0953-119">В приведенных ниже сведениях пользователь уже прошел проверку подлинности на основном сервере, отвечая на запрос проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f0953-119">In the details that follow, the user has already authenticated to the home server by responding to an authentication request.</span></span>



</div>

<div class="">


> [!NOTE]  
> <span data-ttu-id="f0953-120">Веб-служба автообнаружения Lync определена в <STRONG>протоколах Microsoft Office</STRONG> в разделе " <STRONG>открытые спецификации</STRONG> " библиотеки <STRONG>Microsoft Developer Network</STRONG> (MSDN).</span><span class="sxs-lookup"><span data-stu-id="f0953-120">The Lync Autodiscover Web Service is defined in the <STRONG>Microsoft Office Protocols</STRONG> in the <STRONG>Open Specifications</STRONG> section of the <STRONG>Microsoft Developer Network</STRONG> (MSDN) library.</span></span> <span data-ttu-id="f0953-121">Подробнее смотрите документ полную спецификацию "протокол веб-службы автообнаружения Lync" по адресу: <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A> .</span><span class="sxs-lookup"><span data-stu-id="f0953-121">For details, see the full specification document, "Lync Autodiscover Web Service Protocol," at: <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A>.</span></span> <span data-ttu-id="f0953-122">Подробные сведения о проверке подлинности можно найти в разделе "протокол веб-службы проверки подлинности OC" <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A> .</span><span class="sxs-lookup"><span data-stu-id="f0953-122">For details about authentication, see "OC Authentication Web Service Protocol" at <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A>.</span></span>



</div>

<div>

## <a name="the-lync-server-web-service-autodiscover-response"></a><span data-ttu-id="f0953-123">Ответ автообнаружения веб-службы Lync Server</span><span class="sxs-lookup"><span data-stu-id="f0953-123">The Lync Server Web Service Autodiscover Response</span></span>

<span data-ttu-id="f0953-124">Ответ, возвращенный при отправке запроса автообнаружения, одинаков для внутреннего или внешнего клиента.</span><span class="sxs-lookup"><span data-stu-id="f0953-124">The response returned when the Autodiscover request is sent is the same for an internal or an external client.</span></span> <span data-ttu-id="f0953-125">Некоторые параметры, которые являются положениями, могут меняться.</span><span class="sxs-lookup"><span data-stu-id="f0953-125">Some parameters that are location–aware may change.</span></span> <span data-ttu-id="f0953-126">Если запрос на получение клиента получен, но реальный пул отличается от того, с которым был установлен связь, для этого пользователя будет задан главный пул пользователей.</span><span class="sxs-lookup"><span data-stu-id="f0953-126">If a client request is received, but the actual pool is other than the one that has been contacted, the user’s home pool will be set for that user.</span></span> <span data-ttu-id="f0953-127">Коллега с учетной записью пользователя в другом пуле, но вход из него может слегка отличаться от того, который входит в состав одного и того же офиса.</span><span class="sxs-lookup"><span data-stu-id="f0953-127">A colleague whose user account is on a different pool, but logging in from the same office, would get a slightly different response.</span></span> <span data-ttu-id="f0953-128">Ответ указывает на правильный сервер переднего плана или пул переднего плана для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0953-128">The response indicates the correct Front End Server or Front End pool for that user.</span></span>

<span data-ttu-id="f0953-129">Пример документа ответа автообнаружения:</span><span class="sxs-lookup"><span data-stu-id="f0953-129">An example of an Autodiscover Response document:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">
       <User>
          <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>
          <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>
          <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>
          <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>
          <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>
          <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>
          <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>
          <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>
          <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>
          <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>
          <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>
          <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>
          <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>
       </User>
    </AutodiscoverResponse>

<div>

## <a name="autodiscover-response-document-details"></a><span data-ttu-id="f0953-130">Сведения о документе для ответа автообнаружения</span><span class="sxs-lookup"><span data-stu-id="f0953-130">Autodiscover Response Document Details</span></span>

<span data-ttu-id="f0953-131">Документ ответа автообнаружения может иметь один из двух форматов.</span><span class="sxs-lookup"><span data-stu-id="f0953-131">The Autodiscover Response document can be in one of two formats.</span></span> <span data-ttu-id="f0953-132">Формат по умолчанию — нотация объекта JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="f0953-132">The default format is a JavaScript Object Notation (JSON).</span></span> <span data-ttu-id="f0953-133">Другой формат — документ в формате Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="f0953-133">The other format is extensible markup language (XML) document.</span></span> <span data-ttu-id="f0953-134">В этом примере используется XML.</span><span class="sxs-lookup"><span data-stu-id="f0953-134">The XML is used for this example.</span></span> <span data-ttu-id="f0953-135">Запрос и ответ предсказуемы, так как в документе определена схема, определяющая формат.</span><span class="sxs-lookup"><span data-stu-id="f0953-135">The request and response are predictable because the document has a defined schema that determines the format.</span></span> <span data-ttu-id="f0953-136">Строка в документе, описывающая используемую схему, является первой строкой запроса или ответа.</span><span class="sxs-lookup"><span data-stu-id="f0953-136">The line in the document that describes the schema used is the first line in the request or response:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">

<span data-ttu-id="f0953-137">Определение **AccessLocation = "External"** указывает на то, что запрос выполнен от внешнего пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0953-137">The definition of **AccessLocation=”External”** indicates that the request was made from an external user.</span></span>

    <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>

&nbsp;

    <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>

<span data-ttu-id="f0953-138">SipServerInternalAccess и SipServerExternalAccess в настоящее время не используются.</span><span class="sxs-lookup"><span data-stu-id="f0953-138">SipServerInternalAccess and SipServerExternalAccess are currently not used.</span></span> <span data-ttu-id="f0953-139">Эти записи зарезервированы для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="f0953-139">These entries are reserved for future use.</span></span>

    <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>

&nbsp;

    <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>

<span data-ttu-id="f0953-140">SipClientInternalAccess и SipClientExternalAccess описывают полные доменные имена и порты, которые будет использовать внутренний или внешний клиент для доступа к определенному серверу SIP.</span><span class="sxs-lookup"><span data-stu-id="f0953-140">SipClientInternalAccess and SipClientExternalAccess describe the fully qualified domain name and port that an internal or external client will use to access the defined SIP Server.</span></span> <span data-ttu-id="f0953-141">Клиент Lync для настольных компьютеров и приложение Lync из Магазина Windows используют эти записи, основываясь на их расположении (внутреннем или внешнем), чтобы найти сервер директоров или интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f0953-141">The Lync desktop client and the Lync Windows Store app use these entries, based on their location (internal or external) to find the Director or Front End Server.</span></span>

    <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>

&nbsp;

    <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>

<span data-ttu-id="f0953-142">`Autodiscover`Ссылки содержат точки входа в службу автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="f0953-142">The `Autodiscover` references contain the service entry points for the Autodiscover service.</span></span> <span data-ttu-id="f0953-143">Атрибут Token содержит имя службы, а href — URL-адрес, который определяет клиента, на котором может быть найдена служба.</span><span class="sxs-lookup"><span data-stu-id="f0953-143">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="f0953-144">Клиенты во внешней сети используют `External/Autodiscover` .</span><span class="sxs-lookup"><span data-stu-id="f0953-144">Clients on an external network use the `External/Autodiscover`.</span></span> <span data-ttu-id="f0953-145">Служба автообнаружения устанавливается как часть процесса развертывания.</span><span class="sxs-lookup"><span data-stu-id="f0953-145">The Autodiscover service is installed as part of the deployment process.</span></span> <span data-ttu-id="f0953-146">`Internal/Autodiscover` в настоящее время не используется и зарезервирован для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="f0953-146">`Internal/Autodiscover` is not currently used, and is reserved for future use.</span></span>

    <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>

&nbsp;

    <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>

<span data-ttu-id="f0953-147">`AuthBroker`Ссылки содержат точки входа службы для внутренней и внешней службы посредника проверки подлинности, в данном случае SIP. svc.</span><span class="sxs-lookup"><span data-stu-id="f0953-147">The `AuthBroker` references contain the service entry points for the internal and the external authentication broker service, in this case, sip.svc.</span></span> <span data-ttu-id="f0953-148">Атрибут Token содержит имя службы, а href — URL-адрес, который определяет клиента, на котором может быть найдена служба.</span><span class="sxs-lookup"><span data-stu-id="f0953-148">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="f0953-149">Клиенты во внутренней сети с использованием `Internal/AuthBroker` .</span><span class="sxs-lookup"><span data-stu-id="f0953-149">Clients on the internal network with use `Internal/AuthBroker`.</span></span> <span data-ttu-id="f0953-150">Клиенты во внешней сети используют `External/AuthBroker` .</span><span class="sxs-lookup"><span data-stu-id="f0953-150">Clients on an external network use the `External/AuthBroker`.</span></span> <span data-ttu-id="f0953-151">Служба AuthBroker устанавливается в рамках процесса развертывания внутренней веб-службы развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f0953-151">The AuthBroker service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>

&nbsp;

    <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>

<span data-ttu-id="f0953-152">Этот `WebScheduler` маркер ссылается на URL-адреса для доступа клиента к Интернет-календарному планированию для конференций на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f0953-152">The `WebScheduler` token references the URLs for client access to the web-based scheduling for Lync Server conferences.</span></span> <span data-ttu-id="f0953-153">В настоящее время используется только элемент `External/WebScheduler` .</span><span class="sxs-lookup"><span data-stu-id="f0953-153">Currently, only the `External/WebScheduler` is used.</span></span> <span data-ttu-id="f0953-154">Служба веб-планировщика устанавливается как часть процесса развертывания внутренней версии сервера Lync Server 2013 для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f0953-154">The WebScheduler is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>

&nbsp;

    <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>

<span data-ttu-id="f0953-155">`Internal/Mcx` и `External/Mcx` находятся расположения служб Mobility Service, представленные в накопительном обновлении для Lync Server 2010: ноябрь 2011.</span><span class="sxs-lookup"><span data-stu-id="f0953-155">`Internal/Mcx` and `External/Mcx` are the locations of the Mobility services, introduced in Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="f0953-156">Эти ссылки будут продолжать использоваться в Lync 2010 Mobile на всех поддерживаемых устройствах.</span><span class="sxs-lookup"><span data-stu-id="f0953-156">These references will continue to be used by Lync 2010 Mobile on all supported devices.</span></span> <span data-ttu-id="f0953-157">Служба MCX устанавливается в рамках процесса развертывания внутренней веб-службы развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f0953-157">The Mcx service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>

&nbsp;

    <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

&nbsp;

    <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

<span data-ttu-id="f0953-158">ФУНКЦИИ **internal/Ucwa**, **External/Ucwa** и **Ucwa** предоставляют клиентам доступ к интерфейсу прикладного программирования (API для Ucwa или просто Ucwa) для веб-приложений единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f0953-158">**Internal/Ucwa**, **External/Ucwa** and **Ucwa** provide a means for clients to access the Unified Communications Web Application Programming Interface (UCWA API, or simply UCWA).</span></span> <span data-ttu-id="f0953-159">`Internal/Ucwa``External/Ucwa`виртуальные каталоги — это точки доступа, которые зарезервированы для будущего улучшения функций и не используются.</span><span class="sxs-lookup"><span data-stu-id="f0953-159">`Internal/Ucwa` and `External/Ucwa` virtual directories are access points reserved for future feature enhancement, and are not used.</span></span> <span data-ttu-id="f0953-160">`Ucwa`Виртуальный каталог используется для Microsoft Lync Mobile (представленный в Lync Server 2013) на всех поддерживаемых устройствах.</span><span class="sxs-lookup"><span data-stu-id="f0953-160">The `Ucwa` virtual directory is used for Microsoft Lync Mobile (introduced with Lync Server 2013) on all supported devices.</span></span> <span data-ttu-id="f0953-161">Служба UCWA устанавливается в рамках процесса развертывания внутренней веб-службы развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f0953-161">The UCWA service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

<span data-ttu-id="f0953-162">`Internal/XFrame`, **External/Xframe** и **Xframe** предоставляют доступ к серверным приложениям на базе UCWA.</span><span class="sxs-lookup"><span data-stu-id="f0953-162">`Internal/XFrame`, **External/XFrame** and **XFrame** provide access for UCWA-based server applications.</span></span> <span data-ttu-id="f0953-163">XFrame устанавливается в рамках процесса развертывания внутренней веб-службы развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f0953-163">XFrame is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>

<span data-ttu-id="f0953-164">`Self`Маркер ссылается на сведения, специфичные для клиента (тип ответа пользователя), который создает запрос.</span><span class="sxs-lookup"><span data-stu-id="f0953-164">The `Self` token refers to information specific to the client (user response type) that is making the request.</span></span> <span data-ttu-id="f0953-165">Клиент, который сделал этот запрос внешним, и этот указатель автообнаружения относится к пользовательской части службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="f0953-165">The client that made this request was external, and this Autodiscover reference is to the user portion of the Autodiscover service.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f0953-166">См. также</span><span class="sxs-lookup"><span data-stu-id="f0953-166">See Also</span></span>


[<span data-ttu-id="f0953-167">Системные требования для компонентов доступа внешних пользователей для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0953-167">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)  
[<span data-ttu-id="f0953-168">Планирование автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0953-168">Planning for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-planning-for-autodiscover.md)  
  

<span data-ttu-id="f0953-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0953-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

