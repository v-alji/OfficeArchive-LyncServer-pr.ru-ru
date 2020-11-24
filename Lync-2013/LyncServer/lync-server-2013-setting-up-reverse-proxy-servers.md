---
title: 'Lync Server 2013: настройка обратных прокси-серверов'
description: 'Lync Server 2013: Настройка обратного прокси-сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up reverse proxy servers
ms:assetid: 00bc138a-243f-4389-bfa5-9c62fcc95132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398069(v=OCS.15)
ms:contentKeyID: 48183225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8cd5842e4d735637406f6d0fa4f467f1cb8ed03
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399646"
---
# <a name="setting-up-reverse-proxy-servers-for-lync-server-2013"></a><span data-ttu-id="b351f-103">Настройка обратных прокси-серверов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-103">Setting up reverse proxy servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b351f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b351f-104">

<span> </span></span></span>

<span data-ttu-id="b351f-105">_**Тема последнего изменения:** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="b351f-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="b351f-106">Для развертывания Microsoft Lync Server 2013 Edge Server в демилитаризованной зоне требуется обратный прокси-сервер HTTPS для внешних клиентов на доступ к веб-службам Lync Server 2013 (именуемым *веб-компонентам* в Office Communications Server) в директории и домашнем пуле пользователей.</span><span class="sxs-lookup"><span data-stu-id="b351f-106">For Microsoft Lync Server 2013 Edge Server deployments, an HTTPS reverse proxy in the perimeter network is required for external clients to access the Lync Server 2013 Web Services (called *Web Components* in Office Communications Server) on the Director and the user’s home pool.</span></span> <span data-ttu-id="b351f-107">Ниже перечислены некоторые функции, для которых требуется внешний доступ через обратный прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="b351f-107">Some of the features that require external access through a reverse proxy include the following:</span></span>

  - <span data-ttu-id="b351f-108">Включение внешних пользователей для загрузки содержимого собраний для собраний.</span><span class="sxs-lookup"><span data-stu-id="b351f-108">Enabling external users to download meeting content for your meetings.</span></span>

  - <span data-ttu-id="b351f-109">Разрешение внешних пользователей на развертывание групп рассылки.</span><span class="sxs-lookup"><span data-stu-id="b351f-109">Enabling external users to expand distribution groups.</span></span>

  - <span data-ttu-id="b351f-110">Разрешение удаленным пользователям загружать файлы из службы адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b351f-110">Enabling remote users to download files from the Address Book service.</span></span>

  - <span data-ttu-id="b351f-111">Доступ к клиенту Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="b351f-111">Accessing the Lync Web App client.</span></span>

  - <span data-ttu-id="b351f-112">Доступ к веб-странице параметров конференций с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="b351f-112">Accessing the Dial-in Conferencing Settings webpage.</span></span>

  - <span data-ttu-id="b351f-113">Разрешение внешним устройствам подключаться к веб-службе обновления устройств и получать обновления.</span><span class="sxs-lookup"><span data-stu-id="b351f-113">Enabling external devices to connect to Device Update web service and obtain updates.</span></span>

  - <span data-ttu-id="b351f-114">Включение мобильных приложений для автоматического открытия и использования URL-адресов Mobility (MCX) из Интернета.</span><span class="sxs-lookup"><span data-stu-id="b351f-114">Enabling mobile applications to automatically discover and use the mobility (Mcx) URLs from the Internet.</span></span>

  - <span data-ttu-id="b351f-115">Включение клиента Lync 2013, приложения Lync из Магазина Windows и мобильного клиента Lync 2013 для поиска URL-адресов для поиска Lync (автообнаружения) и использования веб-интерфейса единой системы обмена сообщениями (UCWA).</span><span class="sxs-lookup"><span data-stu-id="b351f-115">Enabling the Lync 2013 client, Lync Windows Store app and Lync 2013 Mobile client to locate the Lync Discover (autodiscover) URLs and use Unified Communications Web API (UCWA).</span></span>

<span data-ttu-id="b351f-116">Мы рекомендуем настроить обратный прокси HTTP для публикации всех веб-служб во всех пулах.</span><span class="sxs-lookup"><span data-stu-id="b351f-116">We recommend that you configure your HTTP reverse proxy to publish all Web Services in all pools.</span></span> <span data-ttu-id="b351f-117">Публикация https://ExternalFQDN/ \* публикации всех виртуальных каталогов IIS для пула.</span><span class="sxs-lookup"><span data-stu-id="b351f-117">Publishing https:// ExternalFQDN/\* publishes all IIS virtual directories for a pool.</span></span> <span data-ttu-id="b351f-118">Для каждого сервера Standard Edition, пула переднего плана или режиссера или режиссера в Организации необходимо одно правило публикации.</span><span class="sxs-lookup"><span data-stu-id="b351f-118">You need one publishing rule for each Standard Edition server, Front End pool, or Director or Director pool in your organization.</span></span>

<span data-ttu-id="b351f-119">Кроме того, необходимо опубликовать простые URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b351f-119">In addition, you need to publish the simple URLs.</span></span> <span data-ttu-id="b351f-120">Если в Организации есть режиссер или Director, прокси-сервер HTTP прослушивает запросы HTTP/HTTPS на простые URL-адреса и использует их в виртуальном каталоге внешних служб.</span><span class="sxs-lookup"><span data-stu-id="b351f-120">If the organization has a Director or Director pool, the HTTP reverse proxy listens for HTTP/HTTPS requests to the simple URLs and proxies them to the external Web Services virtual directory on the Director or Director pool.</span></span> <span data-ttu-id="b351f-121">Если вы не развернули режиссер, необходимо назначить один пул для обработки запросов на простые URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b351f-121">If you have not deployed a Director, you need to designate one pool to handle requests to the simple URLs.</span></span> <span data-ttu-id="b351f-122">(Если этот пул не является доменом пользователя, он перенаправит их в веб-службы в домашнем пуле пользователя).</span><span class="sxs-lookup"><span data-stu-id="b351f-122">(If this is not the user’s home pool, it will redirect them onward to the Web Services on the user’s home pool).</span></span> <span data-ttu-id="b351f-123">Простые URL-адреса обрабатываются с помощью выделенного правила публикации в Интернете или добавляются к общедоступным именам правил веб-публикации для режиссера.</span><span class="sxs-lookup"><span data-stu-id="b351f-123">The simple URLs can be handled by a dedicated web publishing rule, or you can add it to the public names of the web publishing rule for the Director.</span></span> <span data-ttu-id="b351f-124">Кроме того, необходимо опубликовать внешний URL-адрес службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="b351f-124">You also need to publish the external Autodiscover Service URL.</span></span>

<span data-ttu-id="b351f-125">Вы можете использовать службу Microsoft Forefront Threat Management Gateway 2010, Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1 или Internet Information Server 7,0, 7,5 или 8,0 с маршрутизацией запросов приложений (IIS ARR) в качестве обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="b351f-125">You can use Microsoft Forefront Threat Management Gateway 2010, Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, or Internet Information Server 7.0, 7.5 or 8.0 with Application Request Routing (IIS ARR) as a reverse proxy.</span></span> <span data-ttu-id="b351f-126">Подробное описание действий, описанных в этом разделе, объясняет, как настроить Forefront Threat Management Gateway 2010, а также действия для настройки ISA Server 2006 практически идентичны.</span><span class="sxs-lookup"><span data-stu-id="b351f-126">The detailed steps in this section describe how to configure Forefront Threat Management Gateway 2010, and the steps for configuring ISA Server 2006 are almost identical.</span></span> <span data-ttu-id="b351f-127">Кроме того, предоставляется руководство по службам IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="b351f-127">Guidance is also provided for IIS ARR.</span></span> <span data-ttu-id="b351f-128">Если вы используете другой обратный прокси-сервер, ознакомьтесь с документацией по этому продукту и сопоставьте требования, описанные в этой статье, с соответствующими функциями в других обратных посредниках.</span><span class="sxs-lookup"><span data-stu-id="b351f-128">If you are using a different reverse proxy, consult the documentation for that product and map the requirements defined here to the associated features in other reverse proxies.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b351f-129">Маршрутизация запросов приложений сервера Интернет-служб (IIS ARR) — полностью протестированный и поддерживаемый способ реализации обратной прокси-сервера для Lync Server 2010 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b351f-129">Internet Information Server Application Request Routing (IIS ARR) is a fully tested and supported option for implementing a reverse proxy for Lync Server 2010 and Lync Server 2013.</span></span> <span data-ttu-id="b351f-130">В ноябре 2012 г. Корпорация Майкрософт перестала лицензировать продажи шлюза ForeFront Threat Management 2010 или TMG.</span><span class="sxs-lookup"><span data-stu-id="b351f-130">In November, 2012, Microsoft ceased license sales of ForeFront Threat Management Gateway 2010, or TMG.</span></span> <span data-ttu-id="b351f-131">TMG по-прежнему является полностью поддерживаемым продуктом и по-прежнему доступен для продажи на устройствах, продаваемых третьими лицами.</span><span class="sxs-lookup"><span data-stu-id="b351f-131">TMG is still a fully supported product, and is still available for sale on appliances sold by third parties.</span></span> <span data-ttu-id="b351f-132">Кроме того, многие сторонние подсистемы балансировки нагрузки оборудования и брандмауэры обеспечивают обратную поддержку прокси.</span><span class="sxs-lookup"><span data-stu-id="b351f-132">Also, many third party hardware load balancers and firewalls provide reverse proxy support.</span></span> <span data-ttu-id="b351f-133">Для аппаратных подсистем балансировки нагрузки и брандмауэров, обеспечивающих обратные функции прокси-сервера, обратитесь к своему поставщику за инструкциями по настройке продукта для обеспечения обратной поддержки прокси-сервера для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b351f-133">For hardware load balancers and firewalls that provide reverse proxy features, check with your vendor for specific instructions on how to configure their product to provide reverse proxy support for Lync Server.</span></span> <span data-ttu-id="b351f-134">Вы также можете просмотреть третьи лица, которые отправили свои продукты корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b351f-134">You can also view third parties that have submitted documentation for their product to Microsoft.</span></span> <span data-ttu-id="b351f-135">Поддержка обеспечивается третьим абонентом для решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="b351f-135">Support is provided by the third party for their solution.</span></span> <span data-ttu-id="b351f-136">Чтобы увидеть, какие сторонние компании активны для предоставления решений, ознакомьтесь с разрешениями <A href="https://go.microsoft.com/fwlink/?linkid=268730">инфраструктуры для Microsoft Lync</A>.</span><span class="sxs-lookup"><span data-stu-id="b351f-136">To see third parties that are active in providing solutions, see <A href="https://go.microsoft.com/fwlink/?linkid=268730">Infrastructure qualified for Microsoft Lync</A>.</span></span>



</div>

<span data-ttu-id="b351f-137">В следующих разделах и процедурах используются службы Forefront Threat Management Gateway 2010 и IIS ARR в качестве основы для процедуры развертывания и настройки.</span><span class="sxs-lookup"><span data-stu-id="b351f-137">The following topics and procedures use Forefront Threat Management Gateway 2010 and IIS ARR as the basis for the deployment and configuration procedures.</span></span>

  - [<span data-ttu-id="b351f-138">Настройка полных доменных имен в веб-ферме для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-138">Configure web farm FQDNs for Lync Server 2013</span></span>](lync-server-2013-configure-web-farm-fqdns.md)

  - [<span data-ttu-id="b351f-139">Настройка сетевых адаптеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-139">Configure network adapters in Lync Server 2013</span></span>](lync-server-2013-configure-network-adapters.md)

  - [<span data-ttu-id="b351f-140">Запрос и настройка сертификата для обратного HTTP-прокси в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-140">Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013</span></span>](lync-server-2013-request-and-configure-a-certificate-for-your-reverse-http-proxy.md)

  - [<span data-ttu-id="b351f-141">Настройка правил веб-публикации для единого внутреннего пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-141">Configure web publishing rules for a single internal pool in Lync Server 2013</span></span>](lync-server-2013-configure-web-publishing-rules-for-a-single-internal-pool.md)

  - [<span data-ttu-id="b351f-142">Проверка и настройка проверки подлинности и сертификатов для виртуальных каталогов IIS в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-142">Verify or configure authentication and certification on IIS virtual directories in Lync Server 2013</span></span>](lync-server-2013-verify-or-configure-authentication-and-certification-on-iis-virtual-directories.md)

  - [<span data-ttu-id="b351f-143">Создание DNS-записей для обратных прокси-серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-143">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)

  - [<span data-ttu-id="b351f-144">Проверка доступа через обратный прокси-сервер в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b351f-144">Verify access through your reverse proxy in Lync Server 2013</span></span>](lync-server-2013-verify-access-through-your-reverse-proxy.md)

<div>

## <a name="before-you-begin"></a><span data-ttu-id="b351f-145">Подготовка</span><span class="sxs-lookup"><span data-stu-id="b351f-145">Before You Begin</span></span>

<span data-ttu-id="b351f-146">Чтобы успешно развернуть шлюз Forefront Threat Management 2010 в качестве обратного прокси-сервера, необходимо настроить сервер, используя необходимые компоненты и требования к оборудованию, определенные в документации Forefront Threat Management Gateway 2010.</span><span class="sxs-lookup"><span data-stu-id="b351f-146">To successfully deploy Forefront Threat Management Gateway 2010 as your reverse proxy, you need to setup and configure a server, using the prerequisites and hardware requirements defined in the Forefront Threat Management Gateway 2010 documentation.</span></span> <span data-ttu-id="b351f-147">Ознакомьтесь со следующими разделами, чтобы правильно настроить оборудование и установить шлюз Forefront Threat Management 2010 на сервере, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="b351f-147">See the following topic set to properly configure the hardware and to install Forefront Threat Management Gateway 2010 on the server before proceeding.</span></span>

  - <span></span>  
    [<span data-ttu-id="b351f-148">Forefront Threat Management Gateway (TMG) 2010</span><span class="sxs-lookup"><span data-stu-id="b351f-148">Forefront Threat Management Gateway (TMG) 2010</span></span>](https://go.microsoft.com/fwlink/?linkid=291292)

  - <span></span>  
    [<span data-ttu-id="b351f-149">Рекомендации по оборудованию Forefront TMG 2010</span><span class="sxs-lookup"><span data-stu-id="b351f-149">Forefront TMG 2010 hardware recommendations</span></span>](https://go.microsoft.com/fwlink/?linkid=291293)

<span data-ttu-id="b351f-150">Для успешного развертывания IIS ARR в качестве обратного прокси ознакомьтесь со следующими разделами, чтобы настроить оборудование и программное обеспечение, необходимое для установки оборудования.</span><span class="sxs-lookup"><span data-stu-id="b351f-150">To successfully deploy IIS ARR as your reverse proxy, review the following topics to configure the hardware and the prerequisite software.</span></span>

  - <span></span>  
    <span data-ttu-id="b351f-151">Установка служб IIS на Windows Server 2008 или Windows Server 2008 R2 описана в разделе [Установка служб IIS 7 на Windows server 2008 или Windows server 2008 R2](https://go.microsoft.com/fwlink/?linkid=291296)</span><span class="sxs-lookup"><span data-stu-id="b351f-151">To install IIS on Windows Server 2008 or Windows Server 2008 R2, see [Installing IIS 7 on Windows Server 2008 or Windows Server 2008 R2](https://go.microsoft.com/fwlink/?linkid=291296)</span></span>

  - <span></span>  
    <span data-ttu-id="b351f-152">Установка служб IIS на Windows Server 2012 описана [в разделе Установка служб IIS 8 на Windows server 2012](https://go.microsoft.com/fwlink/?linkid=291297)</span><span class="sxs-lookup"><span data-stu-id="b351f-152">To install IIS on Windows Server 2012, see [Installing IIS 8 on Windows Server 2012](https://go.microsoft.com/fwlink/?linkid=291297)</span></span>

  - <span></span>  
    <span data-ttu-id="b351f-153">Установка служб IIS на Windows Server 2012 R2 описана в разделе [Установка iis 8,5 на Windows server 2012 R2](https://go.microsoft.com/fwlink/?linkid=330687)</span><span class="sxs-lookup"><span data-stu-id="b351f-153">To install IIS on Windows Server 2012 R2, see [Installing IIS 8.5 on Windows Server 2012 R2](https://go.microsoft.com/fwlink/?linkid=330687)</span></span>

  - <span></span>  
    <span data-ttu-id="b351f-154">Чтобы загрузить расширение маршрутизации запросов приложений для IIS, следуйте инструкциям в разделе [Загрузка маршрута](https://go.microsoft.com/fwlink/?linkid=291298) на этапе Application</span><span class="sxs-lookup"><span data-stu-id="b351f-154">To download the Application Request Routing extension for IIS, follow the instructions at [Application Request Routing v2.5 Download](https://go.microsoft.com/fwlink/?linkid=291298)</span></span>

  - <span></span>  
    <span data-ttu-id="b351f-155">Инструкции по установке программы ARR для инструкций, описанных в разделе [Установка маршрута запроса приложения, версия 2](https://go.microsoft.com/fwlink/?linkid=291299)</span><span class="sxs-lookup"><span data-stu-id="b351f-155">To install ARR, for the instructions at [Install Application Request Routing Version 2](https://go.microsoft.com/fwlink/?linkid=291299)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b351f-156">В настоящее время опубликованы инструкции для ARR 2,0.</span><span class="sxs-lookup"><span data-stu-id="b351f-156">The instructions currently posted are for ARR 2.0.</span></span> <span data-ttu-id="b351f-157">Для установки расширения не существует разницы между двумя версиями.</span><span class="sxs-lookup"><span data-stu-id="b351f-157">For installation of the extension, there is no difference between the two versions.</span></span>

    
    <span data-ttu-id="b351f-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b351f-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

