---
title: 'Lync Server 2013: технические требования для организации мобильной работы'
description: 'Lync Server 2013: технические требования для мобильных устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for mobility
ms:assetid: 831be681-4de0-4e42-b04f-8879ca4dcd23
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690030(v=OCS.15)
ms:contentKeyID: 48184679
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6fc9c262ec8253b83a5bda5a47087579f5adc7d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441348"
---
# <a name="technical-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="ced94-103">Технические требования для организации мобильной работы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ced94-103">Technical requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ced94-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ced94-104">

<span> </span></span></span>

<span data-ttu-id="ced94-105">_**Тема последнего изменения:** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="ced94-105">_**Topic Last Modified:** 2014-07-24_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="ced94-106">Мобильные пользователи сталкиваются с различными сценариями мобильных приложений, для которых требуется специальное планирование.</span><span class="sxs-lookup"><span data-stu-id="ced94-106">Mobile users encounter various mobile application scenarios that require special planning.</span></span> <span data-ttu-id="ced94-107">Например, кто-то может начать использовать мобильное приложение во время отсутствия на работе, подключивсь к сети 3G, а затем переключиться на корпоративную Wi-Fiную сеть при поступлении на работу, а затем переключиться на 3G в случае выхода из здания.</span><span class="sxs-lookup"><span data-stu-id="ced94-107">For example, someone might start using a mobile application while away from work by connecting through the 3G network, then switch to the corporate Wi-Fi network when arriving at work, and then switch back to 3G when leaving the building.</span></span> <span data-ttu-id="ced94-108">Вам нужно спланировать среду для поддержки таких переходов сети и обеспечить согласованное взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="ced94-108">You need to plan your environment to support such network transitions and guarantee a consistent user experience.</span></span> <span data-ttu-id="ced94-109">В этом разделе описаны требования к инфраструктуре, которые необходимы для поддержки мобильных приложений и автоматического обнаружения ресурсов мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="ced94-109">This section describes the infrastructure requirements that you must have in order to support mobile applications and automatic discovery of mobility resources.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ced94-110">Несмотря на то, что мобильные приложения также могут подключаться к другим службам Lync Server 2013, требование для отправки всех веб-запросов мобильных приложений в одно и то же внешнее доменное имя (FQDN) относится только к службе мобильной связи Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ced94-110">Although mobile applications can also connect to other Lync Server 2013 services, the requirement to send all mobile application web requests to the same external web fully qualified domain name (FQDN) applies only to the Lync Server 2013 Mobility Service.</span></span> <span data-ttu-id="ced94-111">Другие службы Mobility Service не требуют этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ced94-111">Other mobility services do not require this configuration.</span></span>



</div>

<span data-ttu-id="ced94-112">Требование схожести файлов cookie в балансировщикх аппаратной нагрузки значительно снижается, и вы заменяете сходство по протоколу TCP, если вы используете Lync Mobile, предоставленный в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ced94-112">The requirement for cookie affinity in hardware load balancers is dramatically reduced, and you substitute Transmission Control Protocol (TCP) affinity if you are using the Lync Mobile delivered with Lync Server 2013.</span></span> <span data-ttu-id="ced94-113">Сходство файлов cookie по-прежнему можно использовать, но для веб-служб больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="ced94-113">Cookie affinity can still be used, but the web services no longer require it.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ced94-114">Весь трафик службы Mobility Service проходит через обратный прокси-сервер, независимо от того, где находится точка происхождения (внутренняя или внешняя).</span><span class="sxs-lookup"><span data-stu-id="ced94-114">All Mobility Service traffic goes through the reverse proxy, regardless of where the origination point is—internal or external.</span></span> <span data-ttu-id="ced94-115">В случае одиночного обратного прокси-сервера или фермы обратных прокси или устройства, предоставляющего функцию обратного прокси, может возникнуть ошибка, когда внутренний трафик egressing через интерфейс и пытается немедленно войти в тот же интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ced94-115">In the case of a single reverse proxy or a farm of reverse proxies, or a device that is providing the reverse proxy function, an issue can arise when the internal traffic is egressing through an interface and attempting to immediately ingress on the same interface.</span></span> <span data-ttu-id="ced94-116">Это часто приводит к нарушению правила безопасности, известному как подмена TCP-пакетов или просто подмена.</span><span class="sxs-lookup"><span data-stu-id="ced94-116">This often leads to a Security rule violation known as TCP packet spoofing or just spoofing.</span></span> <span data-ttu-id="ced94-117">Для работы мобильных устройств необходимо использовать <EM>закрепление перекрестных</EM> и непосредственных входов пакета или ряда пакетов.</span><span class="sxs-lookup"><span data-stu-id="ced94-117"><EM>Hair pinning</EM> (the egress and immediate ingress of a packet or series of packets) must be allowed in order for mobility to function.</span></span> <span data-ttu-id="ced94-118">Один из способов решения этой проблемы — использовать обратный прокси-сервер, который отделен от брандмауэра (правило предотвращения подмены должно всегда быть принудительно применено на брандмауэре, в целях обеспечения безопасности).</span><span class="sxs-lookup"><span data-stu-id="ced94-118">One way to resolve this issue is to use a reverse proxy that is separate from the firewall (the spoofing prevention rule should always be enforced at the firewall, for security purposes).</span></span> <span data-ttu-id="ced94-119">Разворот может находиться на внешнем интерфейсе обратного прокси-сервера, а не на внешнем интерфейсе межсетевого экрана.</span><span class="sxs-lookup"><span data-stu-id="ced94-119">The hairpin can occur at the external interface of the reverse proxy instead of the firewall external interface.</span></span> <span data-ttu-id="ced94-120">Вы определяете подделку на брандмауэре и ослабляете правило на обратном прокси-сервере, тем самым обеспечивая тем самым разворот, что это требуется для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="ced94-120">You detect the spoofing at the firewall, and relax the rule at the reverse proxy, thereby allowing the hairpin that mobility requires.</span></span><BR><span data-ttu-id="ced94-121">Используйте DNS-узел или записи CNAME, чтобы задать обратный прокси для поведения разворот (но не брандмауэра), если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ced94-121">Use the Domain Name System (DNS) host or CNAME records to define the reverse proxy for the hairpin behavior (not the firewall), if at all possible.</span></span>



</div>

<span data-ttu-id="ced94-122">Lync Server 2013 поддерживает службы Mobility Service для мобильных клиентов Lync 2010 для мобильных устройств и Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="ced94-122">Lync Server 2013 supports mobility services for Lync 2010 Mobile and Lync 2013 mobile clients.</span></span> <span data-ttu-id="ced94-123">Оба клиента используют службу автообнаружения Lync Server 2013, чтобы найти ее точку входа, но она отличается от того, в какой службе мобильности они используются.</span><span class="sxs-lookup"><span data-stu-id="ced94-123">Both clients use the Lync Server 2013 Autodiscover Service to find its mobility entry point, but differ on which mobility service they use.</span></span> <span data-ttu-id="ced94-124">Lync 2010 Mobile использует службу Mobility Service, известную как *MCX*, которая представлена в накопительном обновлении для Lync Server 2010: Ноябрь 2011.</span><span class="sxs-lookup"><span data-stu-id="ced94-124">Lync 2010 Mobile uses the Mobility Service known as *Mcx*, introduced with the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="ced94-125">Мобильные клиенты Lync 2013 используют веб-API единой системы обмена сообщениями или *UCWA* в качестве поставщика услуг мобильной связи.</span><span class="sxs-lookup"><span data-stu-id="ced94-125">Lync 2013 mobile clients use the Unified Communications Web API, or *UCWA*, as their mobility service provider.</span></span>

<div>

## <a name="internal-and-external-dns-configuration"></a><span data-ttu-id="ced94-126">Внутренняя и внешняя конфигурации DNS</span><span class="sxs-lookup"><span data-stu-id="ced94-126">Internal and External DNS Configuration</span></span>

<span data-ttu-id="ced94-127">В MCX службах Mobility Service (для Lync Server 2010: Ноябрь 2011) и UCWA (введенные в накопительные обновления для Lync Server 2013: Февраль 2013) используйте DNS таким же образом.</span><span class="sxs-lookup"><span data-stu-id="ced94-127">The Mobility Services Mcx (introduced with the Cumulative Update for Lync Server 2010: November 2011) and UCWA (introduced in the Cumulative Updates for Lync Server 2013: February 2013) use DNS in the same way.</span></span>

<span data-ttu-id="ced94-128">При использовании автоматического обнаружения мобильные устройства используют DNS для поиска ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ced94-128">When you use Automatic Discovery, mobile devices use DNS to locate resources.</span></span> <span data-ttu-id="ced94-129">При просмотре DNS сначала предпринимается попытка подключиться к полному доменному имени, связанному с внутренней записью DNS (lyncdiscoverinternal. \<internal domain name\> ).</span><span class="sxs-lookup"><span data-stu-id="ced94-129">During the DNS lookup, a connection is first attempted to the FQDN that is associated with the internal DNS record (lyncdiscoverinternal.\<internal domain name\>).</span></span> <span data-ttu-id="ced94-130">Если не удается установить соединение с помощью внутренней записи DNS, попытка подключения осуществляется с помощью внешней записи DNS (lyncdiscover. \<sipdomain\> ).</span><span class="sxs-lookup"><span data-stu-id="ced94-130">If a connection cannot be made by using the internal DNS record, a connection is attempted by using the external DNS record (lyncdiscover.\<sipdomain\>).</span></span> <span data-ttu-id="ced94-131">Мобильное устройство, которое является внутренним по отношению к сети, подключается к URL-адресу внутренней службы автообнаружения, и мобильное устройство, внешнее по сети, подключается к внешнему URL-адресу службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="ced94-131">A mobile device that is internal to the network connects to the internal Autodiscover Service URL, and a mobile device that is external to the network connects to the external Autodiscover Service URL.</span></span> <span data-ttu-id="ced94-132">Внешние запросы автообнаружения проходят через обратный прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="ced94-132">External Autodiscover requests go through the reverse proxy.</span></span> <span data-ttu-id="ced94-133">Служба автообнаружения для Lync Server 2013 возвращает все URL-адреса для домашнего пула пользователей, включая URL-адреса службы Mobility Service (MCX и UCWA).</span><span class="sxs-lookup"><span data-stu-id="ced94-133">The Lync Server 2013 Autodiscover Service returns all Web Services URLs for the user's home pool, including the Mobility Service (Mcx and UCWA) URLs.</span></span> <span data-ttu-id="ced94-134">Однако URL-адрес службы внутренних мобильных устройств и внешний URL-адрес службы Mobility Service связаны с полным доменным именем внешних веб-служб.</span><span class="sxs-lookup"><span data-stu-id="ced94-134">However, both the internal Mobility Service URL and the external Mobility Service URL are associated with the external Web Services FQDN.</span></span> <span data-ttu-id="ced94-135">Таким образом, независимо от того, является ли мобильное устройство внутренним или внешним по отношению к сети, устройство всегда подключается к службе Mobility Service Lync Server 2013 извне через обратный прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="ced94-135">Therefore, regardless of whether a mobile device is internal or external to the network, the device always connects to the Lync Server 2013 Mobility Service externally through the reverse proxy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ced94-136">Важно понимать, что развертывание может состоять из нескольких различных пространств имен для внутреннего и внешнего использования.</span><span class="sxs-lookup"><span data-stu-id="ced94-136">It is important to understand that your deployment can consist of multiple distinct namespaces for internal and external use.</span></span> <span data-ttu-id="ced94-137">Имя домена SIP может отличаться от имени внутреннего домена развертывания.</span><span class="sxs-lookup"><span data-stu-id="ced94-137">Your SIP domain name may be different than the internal deployment domain name.</span></span> <span data-ttu-id="ced94-138">Например, ваш домен SIP может быть <STRONG>contoso.com</STRONG>, в то время как внутреннее развертывание может быть <STRONG>contoso.NET</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ced94-138">For example, your SIP domain may be <STRONG>contoso.com</STRONG>, while your internal deployment may be <STRONG>contoso.net</STRONG>.</span></span> <span data-ttu-id="ced94-139">Пользователи, которые входят в состав Lync Server, будут использовать доменное имя SIP, например <STRONG>john@contoso.com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ced94-139">Users who log in to Lync Server will use the SIP domain name, such as <STRONG>john@contoso.com</STRONG>.</span></span> <span data-ttu-id="ced94-140">При обращении к внешним веб-службам (определенным в построителе топологии как <STRONG>внешние веб-службы</STRONG>) имя домена и имя домена SIP будут соответствовать друг другу, как определено в DNS.</span><span class="sxs-lookup"><span data-stu-id="ced94-140">When addressing the external web services (defined in Topology Builder as <STRONG>External web services</STRONG>), the domain name and the SIP domain name will be consistent, as defined in DNS.</span></span> <span data-ttu-id="ced94-141">При обращении к внутренним веб-службам (определенным в Topology Builder как <STRONG>внутренние веб-службы</STRONG>) по умолчанию для внутренних веб-служб задается полное доменное имя сервера переднего плана, пула, режиссера или режиссера pool.</span><span class="sxs-lookup"><span data-stu-id="ced94-141">When addressing the internal Web services (defined in Topology Builder as <STRONG>Internal web services</STRONG>), the default name of the internal web services will be the FQDN of the Front End Server, Front End pool, Director, or Director pool.</span></span> <span data-ttu-id="ced94-142">У вас есть возможность переопределить внутреннее имя веб-служб.</span><span class="sxs-lookup"><span data-stu-id="ced94-142">You have the option to override the internal web services name.</span></span> <span data-ttu-id="ced94-143">Для внутренних веб-служб следует использовать внутреннее доменное имя (а не имя домена SIP) и задать DNS-узлу A (или, для IPv6-записи), чтобы отобразить переопределенное имя.</span><span class="sxs-lookup"><span data-stu-id="ced94-143">You should use the internal domain name (and not the SIP domain name) for internal web services and define the DNS host A (or, for IPv6, AAAA) record to reflect the overridden name.</span></span> <span data-ttu-id="ced94-144">Например, доменные имена внутренних веб-служб по умолчанию могут быть <STRONG>pool01.contoso.NET</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ced94-144">For example, the default internal web services FQDN may be <STRONG>pool01.contoso.net</STRONG>.</span></span> <span data-ttu-id="ced94-145">Переопределенное полное доменное имя внутренней веб-службы может быть <STRONG>webpool.contoso.NET</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ced94-145">An overridden internal web services FQDN may be <STRONG>webpool.contoso.net</STRONG>.</span></span> <span data-ttu-id="ced94-146">Таким образом, определение веб-служб помогает удостовериться в том, что внутренние и внешние локальные возможности служб, а не их локальность пользователя, наблюдаются.</span><span class="sxs-lookup"><span data-stu-id="ced94-146">Defining the web services in this way helps to ensure that the internal and external locality of the services—and not the locality of the user who is using them—is observed.</span></span><BR><span data-ttu-id="ced94-147">Тем не менее, поскольку веб-службы определены в построителе топологии и внутреннее имя веб-службы могут быть переопределены, при условии, что имя результирующих веб-служб, сертификат, определяющее его, и записи DNS, которые определяют его, является действительным, вы можете задать внутренние веб-службы с любым доменным именем, в том числе с именем домена SIP — это нужно.</span><span class="sxs-lookup"><span data-stu-id="ced94-147">However, because the web services are defined in Topology Builder and the internal web services name can be overridden, as long as the resulting web services name, the certificate that validates it, and the DNS records that define it, are consistent, you can define the internal web services with any domain name—including the SIP domain name—that you want.</span></span> <span data-ttu-id="ced94-148">В конечном итоге разрешение имени для IP-адреса определяется записями узлов DNS и последовательным пространством имен.</span><span class="sxs-lookup"><span data-stu-id="ced94-148">Ultimately, the resolution for the name to the IP address is determined by DNS host records and a consistent namespace.</span></span><BR><span data-ttu-id="ced94-149">В целях, описанных в этом разделе, и примерах для иллюстрации топологии и определений DNS используется внутреннее доменное имя.</span><span class="sxs-lookup"><span data-stu-id="ced94-149">For the purposes of this topic and the examples, the internal domain name is used to illustrate the topology and the DNS definitions.</span></span>



</div>

<span data-ttu-id="ced94-150">На приведенной ниже схеме показан поток веб-запросов мобильных приложений для службы Mobility Service и для службы автообнаружения при использовании внутренней и внешней конфигурации DNS.</span><span class="sxs-lookup"><span data-stu-id="ced94-150">The following diagram illustrates the flow of mobile application web requests for the Mobility Service and for the Autodiscover Service when using an internal and external DNS configuration.</span></span>

<span data-ttu-id="ced94-151">**Поток обслуживания мобильных устройств с помощью автообнаружения**</span><span class="sxs-lookup"><span data-stu-id="ced94-151">**Mobility service flow using AutoDiscover**</span></span>

<span data-ttu-id="ced94-152">![cdb96424-96f2-4abf-88d7-1d32d1010ffd](images/Hh690030.cdb96424-96f2-4abf-88d7-1d32d1010ffd(OCS.15).jpg "cdb96424-96f2-4abf-88d7-1d32d1010ffd")</span><span class="sxs-lookup"><span data-stu-id="ced94-152">![cdb96424-96f2-4abf-88d7-1d32d1010ffd](images/Hh690030.cdb96424-96f2-4abf-88d7-1d32d1010ffd(OCS.15).jpg "cdb96424-96f2-4abf-88d7-1d32d1010ffd")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ced94-153">На схеме показаны общие веб-службы.</span><span class="sxs-lookup"><span data-stu-id="ced94-153">The diagram illustrates generic web services.</span></span> <span data-ttu-id="ced94-154">Виртуальный каталог Mobility описывает службы Mobility Services MCX и/или UCWA.</span><span class="sxs-lookup"><span data-stu-id="ced94-154">A virtual directory named Mobility depicts the Mobility services Mcx and/or UCWA.</span></span> <span data-ttu-id="ced94-155">Если вы не применили накопительные обновления для Lync Server 2013: Февраль 2013, возможно, у вас или не установлен виртуальный каталог Ucwa, определенный во внутренней и внешней веб-службах.</span><span class="sxs-lookup"><span data-stu-id="ced94-155">If you have not applied the Cumulative Updates for Lync Server 2013: February 2013, you may or may not have the virtual directory Ucwa defined on your internal and external Web services.</span></span> <span data-ttu-id="ced94-156">У вас будет автообнаружение виртуальных каталогов, и у вас может быть виртуальный каталог MCX.</span><span class="sxs-lookup"><span data-stu-id="ced94-156">You will have a virtual directory Autodiscover, and you may have a virtual directory Mcx.</span></span><BR><span data-ttu-id="ced94-157">Автообнаружение и обнаружение служб работают одинаково независимо от того, какая технология служб Mobility Services была развернута.</span><span class="sxs-lookup"><span data-stu-id="ced94-157">Autodiscover and the discovery of services work the same way, regardless of the mobility services technology that you have deployed.</span></span>



</div>

<span data-ttu-id="ced94-158">Для поддержки мобильных пользователей как внутри организации, так и за ее пределами, внутренние и внешние геодоменные имена веб-сайтов должны соответствовать определенным требованиям.</span><span class="sxs-lookup"><span data-stu-id="ced94-158">To support mobile users from both inside and outside the corporate network, your internal and external web FQDNs must meet some prerequisites.</span></span> <span data-ttu-id="ced94-159">Кроме того, вам может потребоваться выполнить другие требования в зависимости от того, какие функции вы выбираете для реализации:</span><span class="sxs-lookup"><span data-stu-id="ced94-159">In addition, you may need to meet other requirements, depending on the features you choose to implement:</span></span>

  - <span data-ttu-id="ced94-160">Создание записей DNS, CNAME или A (узел, если записи IPv6, AAAA) для автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="ced94-160">New DNS, CNAME or A (host, if IPv6, AAAA) records, for automatic discovery.</span></span>

  - <span data-ttu-id="ced94-161">новое правило брандмауэра, если необходимо обеспечить поддержку push-уведомлений в сети Wi-Fi;</span><span class="sxs-lookup"><span data-stu-id="ced94-161">New firewall rule, if you want to support push notifications through your Wi-Fi network.</span></span>

  - <span data-ttu-id="ced94-162">Дополнительные имена субъектов во внутренних сертификатах сервера и обратные сертификаты прокси-сервера для автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="ced94-162">Subject alternative names on internal server certificates and reverse proxy certificates, for automatic discovery.</span></span>

  - <span data-ttu-id="ced94-163">Конфигурация подсистемы балансировки нагрузки для серверного оборудования переднего плана изменяет сходство источников.</span><span class="sxs-lookup"><span data-stu-id="ced94-163">Front End Server hardware load balancer configuration changes source affinity.</span></span>

<span data-ttu-id="ced94-164">Ваша топология должна соответствовать следующим требованиям для поддержки службы Mobility Service и службы автообнаружения:</span><span class="sxs-lookup"><span data-stu-id="ced94-164">Your topology must meet the following requirements to support the Mobility Service and the Autodiscover Service:</span></span>

  - <span data-ttu-id="ced94-165">Полное доменное имя внутренней веб-сайта пула переднего плана должно отличаться от полного доменного имени внешнего веб-сайта пула.</span><span class="sxs-lookup"><span data-stu-id="ced94-165">The Front End pool internal web FQDN must be distinct from the Front End pool external web FQDN.</span></span>

  - <span data-ttu-id="ced94-166">Внутреннее полное доменное имя веб-сайта должно быть доступно только в корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="ced94-166">The internal web FQDN must only resolve to and be accessible from inside the corporate network.</span></span>

  - <span data-ttu-id="ced94-167">Внешнее полное доменное имя веб-сайта должно быть разрешено только в Интернете и доступно только через Интернет.</span><span class="sxs-lookup"><span data-stu-id="ced94-167">The external web FQDN must only resolve to and be accessible from the Internet.</span></span>

  - <span data-ttu-id="ced94-168">Для пользователя, который входит в корпоративную сеть, URL-адрес службы Mobility Service должен быть адресован внешнему доменному имени сайта.</span><span class="sxs-lookup"><span data-stu-id="ced94-168">For a user who is inside the corporate network, the Mobility Service URL must be addressed to the external web FQDN.</span></span> <span data-ttu-id="ced94-169">Это требование относится к службе Mobility Service и применяется только к этому URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="ced94-169">This requirement is for the Mobility Service and applies only to this URL.</span></span>

  - <span data-ttu-id="ced94-170">Для пользователя, находящегося за пределами корпоративной сети, запрос должен перейти на внешнее полное доменное имя пула или режиссера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="ced94-170">For a user who is outside the corporate network, the request must go to the external web FQDN of the Front End pool or Director.</span></span>

<span data-ttu-id="ced94-171">Если вы поддерживаете автоматическое обнаружение, вам нужно создать следующие записи DNS для каждого домена SIP:</span><span class="sxs-lookup"><span data-stu-id="ced94-171">If you support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="ced94-172">Внутренняя запись DNS для поддержки мобильных пользователей, подключающихся из сети Организации.</span><span class="sxs-lookup"><span data-stu-id="ced94-172">An internal DNS record to support mobile users who connect from within your organization's network.</span></span>

  - <span data-ttu-id="ced94-173">Внешняя (или общедоступная) запись DNS для поддержки мобильных пользователей, подключающихся через Интернет.</span><span class="sxs-lookup"><span data-stu-id="ced94-173">An external, or public, DNS record to support mobile users who connect from the Internet.</span></span>

<span data-ttu-id="ced94-174">Внутренний URL-адрес автоматического обнаружения не должен быть адресом за пределами вашей сети.</span><span class="sxs-lookup"><span data-stu-id="ced94-174">The internal automatic discovery URL should not be addressable from outside your network.</span></span> <span data-ttu-id="ced94-175">URL-адрес внешнего автоматического обнаружения не должен быть адресом в сети.</span><span class="sxs-lookup"><span data-stu-id="ced94-175">The external automatic discovery URL should not be addressable from within your network.</span></span> <span data-ttu-id="ced94-176">Тем не менее, если вы не можете выполнить это требование для внешнего URL-адреса, то мобильный клиент, скорее всего, не повлияет, так как внутренний URL-адрес всегда пытается выполниться раньше.</span><span class="sxs-lookup"><span data-stu-id="ced94-176">However, if you cannot meet this requirement for the external URL, mobile client functionally will probably not be affected, because the internal URL is always tried first.</span></span>

<span data-ttu-id="ced94-177">DNS-записи могут быть либо записями CNAME, либо записями (Host, если IPv6, AAAA).</span><span class="sxs-lookup"><span data-stu-id="ced94-177">The DNS records can be either CNAME records or A (host, if IPv6, AAAA) records.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ced94-178">Клиенты мобильных устройств не поддерживают несколько сертификатов SSL (Secure Sockets Layer) из разных доменов.</span><span class="sxs-lookup"><span data-stu-id="ced94-178">Mobile device clients do not support multiple Secure Sockets Layer (SSL) certificates from different domains.</span></span> <span data-ttu-id="ced94-179">Таким образом, перенаправление CNAME на разные домены не поддерживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ced94-179">Therefore, CNAME redirection to different domains is not supported over HTTPS.</span></span> <span data-ttu-id="ced94-180">Например, запись DNS CNAME для lyncdiscover.contoso.com, которая перенаправляет адрес director.contoso.net, не поддерживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ced94-180">For example, a DNS CNAME record for lyncdiscover.contoso.com that redirects to an address of director.contoso.net is not supported over HTTPS.</span></span> <span data-ttu-id="ced94-181">В такой топологии клиенту на мобильном устройстве необходимо использовать HTTP для первого запроса, чтобы перенаправление CNAME было разрешено через HTTP.</span><span class="sxs-lookup"><span data-stu-id="ced94-181">In such a topology, a mobile device client needs to use HTTP for the first request, so that the CNAME redirection is resolved over HTTP.</span></span> <span data-ttu-id="ced94-182">Затем последующие запросы используют протокол HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ced94-182">Subsequent requests then use HTTPS.</span></span> <span data-ttu-id="ced94-183">Для поддержки этого сценария необходимо настроить обратный прокси с помощью правила веб-публикации для порта 80 (HTTP).</span><span class="sxs-lookup"><span data-stu-id="ced94-183">To support this scenario, you need to configure your reverse proxy with a web publishing rule for port 80 (HTTP).</span></span> <span data-ttu-id="ced94-184">Дополнительные сведения можно найти в разделе "Создание правила веб-публикации для порта 80" при <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">настройке обратного прокси-сервера для мобильных устройств в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ced94-184">For details, see "To create a web publishing rule for port 80" in <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="ced94-185">Перенаправление CNAME на тот же домен поддерживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ced94-185">CNAME redirection to the same domain is supported over HTTPS.</span></span> <span data-ttu-id="ced94-186">В этом случае сертификат конечного домена охватывает исходный домен.</span><span class="sxs-lookup"><span data-stu-id="ced94-186">In this case, the destination domain's certificate covers the originating domain.</span></span>



</div>

<span data-ttu-id="ced94-187">Дополнительные сведения о DNS-записях, необходимых для вашего сценария, приведены [в разделе Сводка DNS — автообнаружение в Lync Server 2013](lync-server-2013-dns-summary-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="ced94-187">For details about the DNS records required for your scenario, see [DNS summary - Autodiscover in Lync Server 2013](lync-server-2013-dns-summary-autodiscover.md).</span></span>

</div>

<div>

## <a name="port-and-firewall-requirements"></a><span data-ttu-id="ced94-188">Требования к портам и брандмауэрам</span><span class="sxs-lookup"><span data-stu-id="ced94-188">Port and Firewall Requirements</span></span>

<span data-ttu-id="ced94-189">Если вы поддерживаете push-уведомления и хотите, чтобы мобильные устройства Apple получали push-уведомления по сети Wi-Fi, нужно также открыть порт 5223 в корпоративной сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="ced94-189">If you support push notifications and want Apple mobile devices to receive push notifications over your Wi-Fi network, you also need to open port 5223 on your enterprise Wi-Fi network.</span></span> <span data-ttu-id="ced94-190">Порт 5223 является исходящим TCP-портом, используемым службой push-уведомлений Apple (APNS).</span><span class="sxs-lookup"><span data-stu-id="ced94-190">Port 5223 is an outbound TCP port used by the Apple Push Notification Service (APNS).</span></span> <span data-ttu-id="ced94-191">На мобильном устройстве инициируется подключение.</span><span class="sxs-lookup"><span data-stu-id="ced94-191">The mobile device initiates the connection.</span></span> <span data-ttu-id="ced94-192">Подробности можно найти в разделе [http://support.apple.com/kb/TS1629](http://support.apple.com/kb/ts1629) .</span><span class="sxs-lookup"><span data-stu-id="ced94-192">For details, see [http://support.apple.com/kb/TS1629](http://support.apple.com/kb/ts1629) .</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="ced94-193">На устройствах Apple, использующих мобильный клиент Lync 2013, отправка push-уведомлений не требуется.</span><span class="sxs-lookup"><span data-stu-id="ced94-193">An Apple device using the Lync 2013 Mobile client does not require push notifications.</span></span>



</div>

<span data-ttu-id="ced94-194">Обратите внимание, что если пользователь размещается на устройстве с бесперебойной подразделением (SBA), необходимы следующие порты:</span><span class="sxs-lookup"><span data-stu-id="ced94-194">Note that if a user is homed on a Survivable Branch Appliance (SBA) then the following ports are required:</span></span>

  - <span data-ttu-id="ced94-195">Для UcwaSipExternalListeningPort требуется порт 5088</span><span class="sxs-lookup"><span data-stu-id="ced94-195">UcwaSipExternalListeningPort requires port 5088</span></span>

  - <span data-ttu-id="ced94-196">Для UcwaSipPrimaryListeningPort требуется порт 5089</span><span class="sxs-lookup"><span data-stu-id="ced94-196">UcwaSipPrimaryListeningPort requires port 5089</span></span>

<span data-ttu-id="ced94-197">Дополнительные сведения о требованиях к портам и протоколам для автообнаружения можно найти [в статье сведения о портах: обнаружение автообнаружения в Lync Server 2013](lync-server-2013-port-summary-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="ced94-197">For additional details and guidance on port and protocol requirements for Autodiscover, see [Port summary - Autodiscover in Lync Server 2013](lync-server-2013-port-summary-autodiscover.md).</span></span>

</div>

<div>

## <a name="certificate-requirements"></a><span data-ttu-id="ced94-198">Требования к сертификатам</span><span class="sxs-lookup"><span data-stu-id="ced94-198">Certificate Requirements</span></span>

<span data-ttu-id="ced94-199">Если вы поддерживаете автоматическое обнаружение для мобильных клиентов Lync, вам нужно будет изменить список альтернативных имен субъектов в сертификатах, чтобы поддерживать безопасные подключения из мобильных клиентов.</span><span class="sxs-lookup"><span data-stu-id="ced94-199">If you support automatic discovery for Lync mobile clients, you need to modify the subject alternative name lists on certificates to support secure connections from the mobile clients.</span></span> <span data-ttu-id="ced94-200">Вам нужно запросить и назначить новые сертификаты, добавив записи альтернативных имен для субъектов, описанные в этом разделе, для каждого сервера переднего плана и режиссера, на котором запускается служба автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="ced94-200">You need to request and assign new certificates, adding the subject alternative name entries described in this section, for each Front End Server and Director that runs the Autodiscover Service.</span></span> <span data-ttu-id="ced94-201">Рекомендуемый подход — также изменить списки альтернативных имен субъектов в сертификатах для обратных прокси.</span><span class="sxs-lookup"><span data-stu-id="ced94-201">The recommended approach is to also modify the subject alternative names lists on certificates for your reverse proxies.</span></span> <span data-ttu-id="ced94-202">Для каждого домена SIP в Организации необходимо добавить записи альтернативных имен для субъектов.</span><span class="sxs-lookup"><span data-stu-id="ced94-202">You need to add subject alternative name entries for every SIP domain in your organization.</span></span>

<span data-ttu-id="ced94-203">Повторное выдача сертификатов с помощью внутреннего центра сертификации обычно является простым процессом, но добавление нескольких записей альтернативных имен субъектов в общедоступные сертификаты, используемые обратным прокси, может быть дорогостоящим.</span><span class="sxs-lookup"><span data-stu-id="ced94-203">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="ced94-204">Если у вас много доменов SIP, что значительно затрудняет Добавление альтернативных имен субъектов, вы можете настроить обратный прокси, чтобы сделать запрос на получение службы автообнаружения через порт 80 с помощью HTTP вместо порта 443 с использованием HTTPS (конфигурация по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ced94-204">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to make the initial Autodiscover Service request over port 80 using HTTP, instead of port 443 using HTTPS (the default configuration).</span></span> <span data-ttu-id="ced94-205">Затем запрос перенаправляется на порт 8080 в пуле на стороне директора и на передней стороне.</span><span class="sxs-lookup"><span data-stu-id="ced94-205">The request is then redirected to port 8080 on the Director or Front End pool.</span></span> <span data-ttu-id="ced94-206">При публикации исходного запроса на обслуживание автообнаружения на порту 80 вам не нужно изменять сертификаты для обратного прокси-сервера, так как запрос использует HTTP, а не HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ced94-206">When you publish the initial Autodiscover Service request on port 80, you do not need to change certificates for the reverse proxy, because the request uses HTTP rather than HTTPS.</span></span> <span data-ttu-id="ced94-207">Этот подход поддерживается, но мы не рекомендуем использовать его.</span><span class="sxs-lookup"><span data-stu-id="ced94-207">This approach is supported, but we do not recommend it.</span></span>

</div>

<div>

## <a name="internet-information-services-iis-requirements"></a><span data-ttu-id="ced94-208">Требования к службам IIS</span><span class="sxs-lookup"><span data-stu-id="ced94-208">Internet Information Services (IIS) Requirements</span></span>

<span data-ttu-id="ced94-209">Для мобильных устройств мы рекомендуем использовать IIS 7,5, IIS 8,0 или IIS 8,5.</span><span class="sxs-lookup"><span data-stu-id="ced94-209">We recommend that you use IIS 7.5, IIS 8.0, or IIS 8.5 for mobility.</span></span> <span data-ttu-id="ced94-210">Установщик службы Mobility устанавливает флаги в ASP.NET для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="ced94-210">The Mobility Service installer sets flags in ASP.NET to improve performance.</span></span> <span data-ttu-id="ced94-211">Службы IIS 7,5 установлены по умолчанию в Windows Server 2008 R2, IIS 8,0 установлен на Windows Server 2012, а IIS 8,5 установлен на Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ced94-211">IIS 7.5 is installed by default on Windows Server 2008 R2, IIS 8.0 is installed on Windows Server 2012, and IIS 8.5 is installed on Windows Server 2012 R2.</span></span> <span data-ttu-id="ced94-212">Установщик службы Mobility Service автоматически изменяет параметры ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="ced94-212">The Mobility Service installer automatically changes the ASP.NET settings.</span></span>

</div>

<div>

## <a name="hardware-load-balancer-requirements"></a><span data-ttu-id="ced94-213">Требования к подсистеме балансировки нагрузки оборудования</span><span class="sxs-lookup"><span data-stu-id="ced94-213">Hardware Load Balancer Requirements</span></span>

<span data-ttu-id="ced94-214">На оборудовании аппаратной подсистемы балансировки нагрузки, поддерживающем пул переднего плана, для трафика веб-служб необходимо настроить внешние IP-адреса внешних служб.</span><span class="sxs-lookup"><span data-stu-id="ced94-214">On the hardware load balancer that is supporting the Front End pool, the external Web Services virtual IPs (VIPs) for Web Services traffic must be configured for source.</span></span> <span data-ttu-id="ced94-215">Сопоставление исходного кода помогает убедиться, что несколько подключений от одного клиента отправляются на один сервер для сохранения состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="ced94-215">Source affinity helps to ensure that multiple connections from a single client are sent to one server to maintain session state.</span></span> <span data-ttu-id="ced94-216">Дополнительные сведения о требованиях к схожести можно найти в разделе [требования к балансировке нагрузки для Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ced94-216">For details about affinity requirements, see [Load balancing requirements for Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span></span>

<span data-ttu-id="ced94-217">Если вы планируете поддерживать мобильные клиенты Lync только в рамках внутренней сети Wi-Fi, необходимо настроить для источника IP-адрес внутренней службы в соответствии с описанием для VIP внешних веб-служб.</span><span class="sxs-lookup"><span data-stu-id="ced94-217">If you plan to support Lync mobile clients only over your internal Wi-Fi network, you should configure the internal Web Services VIPS for source as described for external Web Services VIPs.</span></span> <span data-ttu-id="ced94-218">В этой ситуации следует использовать \_ сходство исходного адреса (или TCP) для VIP внутренних веб-служб на оборудовании аппаратной балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ced94-218">In this situation, you should use source\_addr (or TCP) affinity for the internal Web Services VIPs on the hardware load balancer.</span></span> <span data-ttu-id="ced94-219">Подробности можно найти в разделе [требования балансировки нагрузки для Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ced94-219">For details, see [Load balancing requirements for Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span></span>

</div>

<div>

## <a name="reverse-proxy-requirements"></a><span data-ttu-id="ced94-220">Обратные требования прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ced94-220">Reverse Proxy Requirements</span></span>

<span data-ttu-id="ced94-221">Если вы поддерживаете автоматическое обнаружение для мобильных клиентов Lync, вам нужно обновить текущее правило публикации, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="ced94-221">If you support automatic discovery for Lync mobile clients, you need to update the current publishing rule as follows:</span></span>

  - <span data-ttu-id="ced94-222">Если вы решите обновить списки альтернативных имен тем в обратных сертификатах прокси-сервера и использовать HTTPS для первоначального запроса на обслуживание автообнаружения, вы должны обновить правило веб-публикации для lyncdiscover. \<sipdomain\> .</span><span class="sxs-lookup"><span data-stu-id="ced94-222">If you decide to update the subject alternative names lists on the reverse proxy certificates and use HTTPS for the initial Autodiscover Service request, you must update the web publishing rule for lyncdiscover.\<sipdomain\>.</span></span> <span data-ttu-id="ced94-223">Обычно этот параметр сочетается с правилом публикации для URL-адреса внешней веб-службы в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="ced94-223">Typically, this is combined with the publishing rule for the external Web Services URL on the Front End pool.</span></span>

  - <span data-ttu-id="ced94-224">Если вы решили использовать HTTP для первоначального запроса на обслуживание автообнаружения, так что вам не нужно обновлять список альтернативных имен для некоторых прокси-сертификатов, необходимо создать новое правило веб-публикации для порта HTTP/TCP 80, если оно еще не существует.</span><span class="sxs-lookup"><span data-stu-id="ced94-224">If you decide to use HTTP for the initial Autodiscover Service request so that you do not need to update the subject alternative names list on the reverse proxy certificates, you must create a new web publishing rule for port HTTP/TCP 80, if one does not already exist.</span></span> <span data-ttu-id="ced94-225">Если правило для HTTP/TCP 80 уже существует, вы можете изменить правило, чтобы включить lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="ced94-225">If a rule for HTTP/TCP 80 does already exist, you can update that rule to include the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="ced94-226">Вход.</span><span class="sxs-lookup"><span data-stu-id="ced94-226">entry.</span></span>

<span data-ttu-id="ced94-227"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ced94-227"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

