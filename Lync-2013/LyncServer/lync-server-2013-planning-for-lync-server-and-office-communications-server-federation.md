---
title: Планирование интеграции Lync Server и Office Communications Server
description: Планирование интеграции сервера Lync Server и Office Communications Server Federation.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Lync Server and Office Communications Server federation
ms:assetid: c9eaf06b-054f-41a4-ad0c-499400d6c4c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205335(v=OCS.15)
ms:contentKeyID: 48185640
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d7385b8fde27446fb0648802544a8840a0f6276
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424543"
---
# <a name="planning-for-lync-server-2013-and-office-communications-server-federation"></a><span data-ttu-id="fa1f5-103">Планирование для Lync Server 2013 и Office Communications Server Federation</span><span class="sxs-lookup"><span data-stu-id="fa1f5-103">Planning for Lync Server 2013 and Office Communications Server federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa1f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa1f5-104">

<span> </span></span></span>

<span data-ttu-id="fa1f5-105">_**Тема последнего изменения:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="fa1f5-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="fa1f5-106">Федерация между Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server поддерживает одноранговые и многосторонние коммуникации.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-106">Federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server supports peer-to-peer and multi-party communications.</span></span> <span data-ttu-id="fa1f5-107">Одноранговые беседы могут быть переданы в беседы с несколькими участниками, что позволяет проводить нерегламентированные собрания.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-107">Peer-to-peer conversations can be escalated to multi-party conversations, allowing for ad hoc meetings.</span></span> <span data-ttu-id="fa1f5-108">Собрания: веб-конференции или звуковые и визуальные конференции — можно запланировать включение контактов внутри организации, а также контактов в партнерах, с которыми вы хотите выполнить федерацию.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-108">Meetings – Web conferencing or audio/visual conferences – can be scheduled to include contacts inside your organization as well as contacts in partners that you federate with.</span></span>

<span data-ttu-id="fa1f5-109">Федерация впервые появилась в Microsoft Office Live Communications Server 2005 и поддерживала один и тот же вариант интеграции, прямая Федерация.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-109">Federation first appeared in Microsoft Office Live Communications Server 2005 and supported one kind of federation, Direct Federation.</span></span> <span data-ttu-id="fa1f5-110">Прямая Федерация требует узнать домен SIP и полное доменное имя партнера (FQDN) для пограничного сервера участника.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-110">Direct Federation required you to know the federation partner’s session initiation protocol (SIP) domain and the fully qualified domain name (FQDN) of the partner’s Edge Server.</span></span> <span data-ttu-id="fa1f5-111">Сервер Live Communications Server 2005 с пакетом обновления 1 (SP1) предлагает дополнительные типы Федерации, которые должны быть опубликованы федеративным партнером для поиска пограничного сервера в службе доменных имен (DNS).</span><span class="sxs-lookup"><span data-stu-id="fa1f5-111">Live Communications Server 2005 with SP1 introduced additional federation types, all of which required domain name system (DNS) SRV records to be published by the federated partner to locate their Edge Server.</span></span> <span data-ttu-id="fa1f5-112">Терминология для этого выпуска:</span><span class="sxs-lookup"><span data-stu-id="fa1f5-112">The terminology for that release was:</span></span>

  - <span data-ttu-id="fa1f5-113">*Открыть улучшенную Федерацию*: Принимайте доменные имена SIP и используйте DNS SRV для поиска пограничного сервера партнера</span><span class="sxs-lookup"><span data-stu-id="fa1f5-113">*Open Enhanced Federation*: Accept any SIP domain name and use DNS SRV to locate the partner Edge Server</span></span>

  - <span data-ttu-id="fa1f5-114">*Улучшенная федерация*: Настройте имя домена SIP партнера как партнера Федерации для своей организации и используйте DNS SRV для поиска пограничного сервера партнера.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-114">*Enhanced Federation*: Configure the partner’s SIP domain name as a federation partner for your organization and use DNS SRV to find the partner Edge Server</span></span>

  - <span data-ttu-id="fa1f5-115">*Прямая Федерация*: Настройте имя домена SIP партнера и FQDN на пограничный сервер партнера.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-115">*Direct Federation*: Configure the partner’s SIP domain name and the FQDN to the partner’s Edge Server</span></span>

  - <span data-ttu-id="fa1f5-116">*Список разрешенных серверов*: принимать любой домен, использовать DNS SRV для поиска пограничного сервера поставщика услуг размещения или общедоступного службы обмена мгновенными сообщениями (IM)</span><span class="sxs-lookup"><span data-stu-id="fa1f5-116">*Server Allow List*: Accept any domain, use DNS SRV to find the Edge Server of a hosting provider or a public instant messaging (IM) connectivity provider</span></span>

<span data-ttu-id="fa1f5-117">Microsoft Office Communications Server 2007 представил обновленные наименования для типов Федерации, чтобы лучше определить, что именно обеспечивается для каждого типа Федерации.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-117">Microsoft Office Communications Server 2007 introduced updated naming for federation types to better define what each federation type actually accomplished:</span></span>

  - <span data-ttu-id="fa1f5-118">Открыть улучшенную Федерацию, которая стала известна как *обнаруженный домен партнера*</span><span class="sxs-lookup"><span data-stu-id="fa1f5-118">Open Enhanced Federation became known as *Discovered Partner Domain*</span></span>

  - <span data-ttu-id="fa1f5-119">Улучшенная Федерация стала известна как *разрешенный домен партнера*</span><span class="sxs-lookup"><span data-stu-id="fa1f5-119">Enhanced Federation became known as *Allowed Partner Domain*</span></span>

  - <span data-ttu-id="fa1f5-120">Прямая Федерация стала известна как *разрешенный сервер-партнер*</span><span class="sxs-lookup"><span data-stu-id="fa1f5-120">Direct Federation became known as *Allowed Partner Server*</span></span>

  - <span data-ttu-id="fa1f5-121">Список разрешенных серверов стал известным поставщиком *услуг размещения* и *общедоступным поставщиком мгновенных сообщений*</span><span class="sxs-lookup"><span data-stu-id="fa1f5-121">Server Allow List became known as *Hosting Provider* and *Public IM Provider*</span></span>

<span data-ttu-id="fa1f5-122">Microsoft Lync Server 2010 предлагает более узкое определение поставщика услуг размещения в соответствии с Microsoft Lync Online 2010 и Microsoft Office 365, а также сделал его допустимым списком разрешенных доменных доменов разрешенных партнеров.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-122">Microsoft Lync Server 2010 introduced a narrower definition of Hosting Provider in accordance with Microsoft Lync Online 2010 and Microsoft Office 365 and also made it subject to the same allowed list defined by the Allowed Partner Domain federation type.</span></span>

<span data-ttu-id="fa1f5-123">При включении Федерации между Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server для обеспечения правил и разрешенных доменных доменов используются пограничные серверы и обратные прокси-серверы.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-123">Enabling federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server uses the Edge Servers and reverse proxies to enforce the rules and allowed partner domains that you define.</span></span> <span data-ttu-id="fa1f5-124">С точки зрения планирования, в которой вы планируете использовать другие серверы Lync Server, для Office Communications Server требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="fa1f5-124">From a planning perspective, federating with other Lync Server, Office Communications Server requires the following:</span></span>

  - <span data-ttu-id="fa1f5-125">Включите Федерацию в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-125">Enable federation in Topology Builder.</span></span> <span data-ttu-id="fa1f5-126">Подробные сведения можно найти в разделе Развертывание [: Настройка Федерации SIP, XMPP Федерации и общедоступной службы обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="fa1f5-126">For details, see the Deployment topic [Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="fa1f5-127">Определите требования для обнаружения федеративного домена.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-127">Determine your requirements for federated domain discovery:</span></span>
    
      - <span></span>  
        <span data-ttu-id="fa1f5-128">Для ручной настройки федерации необходимо иметь полное доменное имя (FQDN) сервера граничного и доменного имени партнера или доменное имя домена, которое вводится на панели управления Lync Server, **Федерации и внешнего доступа, а** также в **федеративных доменах SIP**.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-128">For manual configuration of federation, you must have the fully qualified domain name (FQDN) of the partner’s Edge Server and domain name, or online domain name, which is entered in the Lync Server Control Panel, **Federation and External Access**, **SIP Federated Domains**.</span></span> <span data-ttu-id="fa1f5-129">Создание **новой** политики или **изменение** существующей политики для разрешения или блокировки доменов по полному доменному имени.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-129">Create a **New** policy or **Edit** an existing policy to either allow or block domains by FQDN.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="fa1f5-130">Ручная настройка пограничного сервера партнера Федерации может привести к сбою в событии, которое партнер изменяет IP-адрес пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-130">Manual configuration of a federation partner’s Edge Server is prone to failure in the event that the partner changes the IP address of their Edge Server.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="fa1f5-131">Для <STRONG>новых федеративных доменов SIP</STRONG>необходимо указать <STRONG>доменное имя (или FQDN)</STRONG> для Microsoft Lync Online и microsoft 365 или Office 365.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-131">For <STRONG>New SIP Federated Domains</STRONG>, you must provide the <STRONG>Domain name (or FQDN)</STRONG> for Microsoft Lync Online and Microsoft 365 or Office 365.</span></span> <span data-ttu-id="fa1f5-132">Для Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server также необходимо предоставить <STRONG>службу пограничного доступа (FQDN)</STRONG></span><span class="sxs-lookup"><span data-stu-id="fa1f5-132">For Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server you must also provide an <STRONG>Access Edge service (FQDN)</STRONG></span></span>

        
        </div>
    
      - <span></span>  
        <span data-ttu-id="fa1f5-133">Для обнаруженной Федерации партнеров, где партнеры могут найти пограничный сервер, вы создаете запись SRV в внешней службе DNS- \_ sipfederationtls. \_ tcp.contoso.com – это указывает на порт 5061 и запись узла (A) пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-133">For discovered partner federation, where partners can discover your Edge Server, you create an SRV record in your external DNS - \_sipfederationtls.\_tcp.contoso.com – which points to the port 5061 and the host (A) record of your Edge Server</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="fa1f5-134">Если вы используете клиент Microsoft Lync Mobile на Windows Phone или Apple iPhone, iPad и других устройствах Apple, а также используете службу push-уведомлений или службу push-уведомлений, вы должны спланировать использование _sipfederationtls. _tcp.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-134">If you are supporting Microsoft Lync Mobile clients on either Windows Phone or Apple iPhone, iPad, or other Apple devices and are using the Push Notification Service or Push Notification Service, you must plan for _sipfederationtls._tcp.</span></span> <span data-ttu-id="fa1f5-135">&lt;SRV- &gt; записи домена SIP для каждого домена SIP, на котором установлены мобильные клиенты Lync.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-135">&lt;SIP domain&gt; SRV records for each SIP domain that you have Lync Mobile clients.</span></span> <span data-ttu-id="fa1f5-136">Для Android и Nokia Symbian Lync Mobile не следует использовать push-уведомления и не подвергаться этим требованиям.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-136">Android and Nokia Symbian Lync Mobile do not use push notification and are not subject to this requirement.</span></span>

        
        </div>

  - <span data-ttu-id="fa1f5-137">Настройка политик доступа внешних пользователей для поддержки федеративных доменов</span><span class="sxs-lookup"><span data-stu-id="fa1f5-137">Configure external user access policies to support federated domains</span></span>

  - <span data-ttu-id="fa1f5-138">Откройте порты брандмауэра для протокола запуска сеансов (SIP), веб-конференций, аудио-и видеосвязи, чтобы включить в нее Федерацию или контакты.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-138">Open firewall ports for session initiation protocol (SIP), web conferencing and audio/visual to accommodate the federation or contacts that you are enabling.</span></span> <span data-ttu-id="fa1f5-139">Подробности можно найти в статье [Определение внешних параметров брандмауэра/V и портов для Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="fa1f5-139">For details, see: [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span></span>

<span data-ttu-id="fa1f5-140">Ниже приведены сведения, которые помогут вам определить требования к сертификатам, портам и протоколам и DNS для Федерации с Microsoft Lync Server 2013 и Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-140">The following information will aid you in defining the certificate, port/protocol and DNS requirements for federation with Microsoft Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="fa1f5-141">Планирование сертификатов, брандмауэров и требований к портам и протоколам и требованиям DNS обычно является прямым перенаправленным процессом, если вы планируете или развернули сервер Microsoft Lync Server 2013 Edge.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-141">Planning for certificates, firewall and port/protocol requirements and DNS requirements is generally a straight forward process if you have planned or deployed your Microsoft Lync Server 2013 Edge Servers.</span></span> <span data-ttu-id="fa1f5-142">Поскольку Федерация — это дополнительная функция, использующая существующий пограничный сервер, требования к планированию обычно выполняются планированием и развертыванием пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-142">Because federation is an additional feature that uses the existing Edge Server, the planning requirements are generally met by the Edge Server planning and deployment.</span></span> <span data-ttu-id="fa1f5-143">Для определения соответствия требованиям и внесения изменений в порт/протокол и DNS следует использовать приведенные ниже таблицы.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-143">You should use the following tables to determine that your requirements are met and make changes in port/protocol and DNS accordingly.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="fa1f5-144">Если у вас есть пул пограничных серверов и вы используете сервер Lync Server 2013 или Lync Server 2010, вы можете использовать либо балансировку нагрузки DNS, либо подсистему балансировки нагрузки для оборудования на внутренних и внешних сторонах пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-144">If you have a pool of Edge Servers and are federating with Lync Server 2013 or Lync Server 2010 partners, then you can use either DNS load balancing or hardware load balancers on the internal and external facing sides of the Edge Servers.</span></span> <span data-ttu-id="fa1f5-145">Если вы предоставляете Федерацию с Office Communications Server 2007 или Office Communications Server 2007 R2, аппаратная балансировка нагрузки обеспечивает поддержку перехода на другой ресурс в случае пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-145">If you are federating with Office Communications Server 2007 or Office Communications Server 2007 R2, hardware load balancing will provide failover support in the event of an Edge Server.</span></span> <span data-ttu-id="fa1f5-146">Office Communications Server 2007 и Office Communications Server 2007 R2 не поддерживают балансировку нагрузки DNS.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-146">Office Communications Server 2007 and Office Communications Server 2007 R2 are not DNS load balancing aware.</span></span> <span data-ttu-id="fa1f5-147">Пограничные серверы партнеров будут устанавливать связь с первым пограничным сервером в пуле, который отвечает.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-147">The partner Edge Servers will establish communication with the first Edge Server in your pool that responds.</span></span> <span data-ttu-id="fa1f5-148">Если пограничный сервер завершается сбоем, Обмен данными не выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-148">If that Edge Server fails, communication does not automatically failover.</span></span>



</div>

<span data-ttu-id="fa1f5-149">Требования к сертификатам обычно выполняются с помощью планирования сертификатов для выбранного пограничного сервера или плана пограничного сервера в пуле.</span><span class="sxs-lookup"><span data-stu-id="fa1f5-149">Certificate requirements are typically met through the planning of certificates for your chosen Edge Server or pooled Edge Server plan.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fa1f5-150">Содержание</span><span class="sxs-lookup"><span data-stu-id="fa1f5-150">In This Section</span></span>

  - [<span data-ttu-id="fa1f5-151">Общие сведения о сертификате: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-151">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="fa1f5-152">Общие сведения о портах: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-152">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="fa1f5-153">Сводка DNS-SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-153">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fa1f5-154">См. также</span><span class="sxs-lookup"><span data-stu-id="fa1f5-154">See Also</span></span>


[<span data-ttu-id="fa1f5-155">Настройка политик управления доступом федеративных пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-155">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  


[<span data-ttu-id="fa1f5-156">Сценарии доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-156">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="fa1f5-157">Определение требований к внешнему брандмауэру аудио- и видеосвязи и портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-157">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
[<span data-ttu-id="fa1f5-158">Определение требований DNS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-158">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="fa1f5-159">Управление конфигурацией пограничного сервера в организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-159">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-access-edge-configuration-for-your-organization.md)  
[<span data-ttu-id="fa1f5-160">Управление федеративными доменами SIP для организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-160">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="fa1f5-161">Управление федеративными поставщиками SIP в организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa1f5-161">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
  

<span data-ttu-id="fa1f5-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa1f5-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

