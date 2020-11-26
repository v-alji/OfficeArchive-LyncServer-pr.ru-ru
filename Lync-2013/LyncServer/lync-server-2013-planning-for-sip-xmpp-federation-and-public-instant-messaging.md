---
title: Планирование SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями
description: Планирование SIP, Федерации XMPP и общедоступной службы обмена мгновенными сообщениями.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for SIP, XMPP federation, and public instant messaging
ms:assetid: 3b234d92-b9ff-4b1d-910e-084c6f17e751
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204825(v=OCS.15)
ms:contentKeyID: 48183918
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c28c9c75310c884ea00117be2458384d408daae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424424"
---
# <a name="planning-for-sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="31f57-103">Планирование SIP, Федерации XMPP и общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-103">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31f57-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31f57-104">

<span> </span></span></span>

<span data-ttu-id="31f57-105">_**Тема последнего изменения:** 2013-10-28_</span><span class="sxs-lookup"><span data-stu-id="31f57-105">_**Topic Last Modified:** 2013-10-28_</span></span>

<span data-ttu-id="31f57-106">Пограничные серверы могут быть настроены таким образом, чтобы разрешить внутренним и внешним пользователям доступ к контактам в организациях или службах партнера.</span><span class="sxs-lookup"><span data-stu-id="31f57-106">Edge Servers can be configured to allow your internal and external users access to contacts at partner organizations or services.</span></span> <span data-ttu-id="31f57-107">Федерации, поскольку эти лицензионные соглашения известны, могут предоставлять любые или все указанные ниже данные контактам в вашей организации в Федерации и контактах в Федерации партнеров.</span><span class="sxs-lookup"><span data-stu-id="31f57-107">Federations, as these partner agreements are known, can provide any or all of the following to the contacts in your organization on the partner federation or contacts in the partner federation to yours:</span></span>

  - <span data-ttu-id="31f57-108">Мгновенные сообщения и присутствие</span><span class="sxs-lookup"><span data-stu-id="31f57-108">Instant messaging and presence</span></span>

  - <span data-ttu-id="31f57-109">Совместная работа и конференции, например веб-конференции</span><span class="sxs-lookup"><span data-stu-id="31f57-109">Collaboration and conferencing, for example – Web conferencing</span></span>

  - <span data-ttu-id="31f57-110">Голосовые конференции, видеоконференции и т. д.</span><span class="sxs-lookup"><span data-stu-id="31f57-110">Audio conferencing, video conferencing, or both</span></span>

<span data-ttu-id="31f57-111">В некоторых случаях связь, например обмен мгновенными сообщениями и присутствие между Microsoft Lync Server 2013 и контактом по протоколу XMPP, является одноранговой только для вашего федеративного партнера и только для него и контакта.</span><span class="sxs-lookup"><span data-stu-id="31f57-111">In some cases the communication, for example instant messaging (IM) and presence between a Microsoft Lync Server 2013 and an extensible messaging and presence protocol (XMPP) contact, is peer-to-peer only - supporting only you and the contact at the federated partner.</span></span> <span data-ttu-id="31f57-112">В других случаях, таких как Lync Server, Lync Server 2010 и Lync Server 2013 Федерация, для присоединения к беседе может быть приглашено несколько участников.</span><span class="sxs-lookup"><span data-stu-id="31f57-112">In other cases, such as a Lync Server, Lync Server 2010 to Lync Server 2013 federation, multiple participants can be invited to join into the conversation.</span></span>

<div>

## <a name="lync-server-and-office-communications-server-federation"></a><span data-ttu-id="31f57-113">Lync Server и Office Communications Server Federation</span><span class="sxs-lookup"><span data-stu-id="31f57-113">Lync Server and Office Communications Server Federation</span></span>

<span data-ttu-id="31f57-114">Федерация между Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server поддерживает одноранговые и многосторонние коммуникации.</span><span class="sxs-lookup"><span data-stu-id="31f57-114">Federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server supports peer-to-peer and multi-party communications.</span></span> <span data-ttu-id="31f57-115">Одноранговые беседы могут быть переданы в беседы с несколькими участниками, что позволяет проводить нерегламентированные собрания.</span><span class="sxs-lookup"><span data-stu-id="31f57-115">Peer-to-peer conversations can be escalated to multi-party conversations, allowing for ad hoc meetings.</span></span> <span data-ttu-id="31f57-116">Собрания: веб-конференции или звуковые и визуальные конференции — можно запланировать включение контактов внутри организации, а также контактов в партнерах, с которыми вы хотите выполнить федерацию.</span><span class="sxs-lookup"><span data-stu-id="31f57-116">Meetings – Web conferencing or audio/visual conferences – can be scheduled to include contacts inside your organization as well as contacts in partners that you federate with.</span></span>

<span data-ttu-id="31f57-117">Федерация впервые появилась в Microsoft Office Live Communications Server 2005 и поддерживала один и тот же вариант интеграции, прямая Федерация.</span><span class="sxs-lookup"><span data-stu-id="31f57-117">Federation first appeared in Microsoft Office Live Communications Server 2005 and supported one kind of federation, Direct Federation.</span></span> <span data-ttu-id="31f57-118">Прямая Федерация требует узнать домен SIP и полное доменное имя партнера (FQDN) для пограничного сервера участника.</span><span class="sxs-lookup"><span data-stu-id="31f57-118">Direct Federation required you to know the federation partner’s session initiation protocol (SIP) domain and the fully qualified domain name (FQDN) of the partner’s Edge Server.</span></span> <span data-ttu-id="31f57-119">Сервер Live Communications Server 2005 с пакетом обновления 1 (SP1) предлагает дополнительные типы Федерации, которые должны быть опубликованы федеративным партнером для поиска пограничного сервера в службе доменных имен (DNS).</span><span class="sxs-lookup"><span data-stu-id="31f57-119">Live Communications Server 2005 with SP1 introduced additional federation types, all of which required domain name system (DNS) SRV records to be published by the federated partner to locate their Edge Server.</span></span> <span data-ttu-id="31f57-120">Терминология для этого выпуска:</span><span class="sxs-lookup"><span data-stu-id="31f57-120">The terminology for that release was:</span></span>

  - <span data-ttu-id="31f57-121">*Открыть улучшенную Федерацию*: Принимайте доменные имена SIP и используйте DNS SRV для поиска пограничного сервера партнера</span><span class="sxs-lookup"><span data-stu-id="31f57-121">*Open Enhanced Federation*: Accept any SIP domain name and use DNS SRV to locate the partner Edge Server</span></span>

  - <span data-ttu-id="31f57-122">*Улучшенная федерация*: Настройте имя домена SIP партнера как партнера Федерации для своей организации и используйте DNS SRV для поиска пограничного сервера партнера.</span><span class="sxs-lookup"><span data-stu-id="31f57-122">*Enhanced Federation*: Configure the partner’s SIP domain name as a federation partner for your organization and use DNS SRV to find the partner Edge Server</span></span>

  - <span data-ttu-id="31f57-123">*Прямая Федерация*: Настройте имя домена SIP партнера и FQDN на пограничный сервер партнера.</span><span class="sxs-lookup"><span data-stu-id="31f57-123">*Direct Federation*: Configure the partner’s SIP domain name and the FQDN to the partner’s Edge Server</span></span>

  - <span data-ttu-id="31f57-124">*Список разрешенных серверов*: принимать любой домен, использовать DNS SRV для поиска пограничного сервера поставщика услуг размещения или общедоступного службы обмена мгновенными сообщениями (IM)</span><span class="sxs-lookup"><span data-stu-id="31f57-124">*Server Allow List*: Accept any domain, use DNS SRV to find the Edge Server of a hosting provider or a public instant messaging (IM) connectivity provider</span></span>

<span data-ttu-id="31f57-125">Microsoft Office Communications Server 2007 представил обновленные наименования для типов Федерации, чтобы лучше определить, что именно обеспечивается для каждого типа Федерации.</span><span class="sxs-lookup"><span data-stu-id="31f57-125">Microsoft Office Communications Server 2007 introduced updated naming for federation types to better define what each federation type actually accomplished:</span></span>

  - <span data-ttu-id="31f57-126">Открыть улучшенную Федерацию, которая стала известна как *обнаруженный домен партнера*</span><span class="sxs-lookup"><span data-stu-id="31f57-126">Open Enhanced Federation became known as *Discovered Partner Domain*</span></span>

  - <span data-ttu-id="31f57-127">Улучшенная Федерация стала известна как *разрешенный домен партнера*</span><span class="sxs-lookup"><span data-stu-id="31f57-127">Enhanced Federation became known as *Allowed Partner Domain*</span></span>

  - <span data-ttu-id="31f57-128">Прямая Федерация стала известна как *разрешенный сервер-партнер*</span><span class="sxs-lookup"><span data-stu-id="31f57-128">Direct Federation became known as *Allowed Partner Server*</span></span>

  - <span data-ttu-id="31f57-129">Список разрешенных серверов стал известным поставщиком *услуг размещения* и *общедоступным поставщиком мгновенных сообщений*</span><span class="sxs-lookup"><span data-stu-id="31f57-129">Server Allow List became known as *Hosting Provider* and *Public IM Provider*</span></span>

<span data-ttu-id="31f57-130">Microsoft Lync Server 2010 предлагает более узкое определение поставщика услуг размещения в соответствии с Microsoft Lync Online 2010 и Microsoft Office 365, а также сделал его допустимым списком разрешенных доменных доменов разрешенных партнеров.</span><span class="sxs-lookup"><span data-stu-id="31f57-130">Microsoft Lync Server 2010 introduced a narrower definition of Hosting Provider in accordance with Microsoft Lync Online 2010 and Microsoft Office 365 and also made it subject to the same allowed list defined by the Allowed Partner Domain federation type.</span></span>

<span data-ttu-id="31f57-131">При включении Федерации между Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server для обеспечения правил и разрешенных доменных доменов используются пограничные серверы и обратные прокси-серверы.</span><span class="sxs-lookup"><span data-stu-id="31f57-131">Enabling federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server uses the Edge Servers and reverse proxies to enforce the rules and allowed partner domains that you define.</span></span> <span data-ttu-id="31f57-132">С точки зрения планирования, в которой вы планируете использовать другие серверы Lync Server, для Office Communications Server требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="31f57-132">From a planning perspective, federating with other Lync Server, Office Communications Server requires the following:</span></span>

  - <span data-ttu-id="31f57-133">Включите Федерацию в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="31f57-133">Enable federation in Topology Builder.</span></span> <span data-ttu-id="31f57-134">Подробные сведения можно найти в разделе Развертывание [: Настройка Федерации SIP, XMPP Федерации и общедоступной службы обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="31f57-134">For details, see the Deployment topic [Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="31f57-135">Определите требования для обнаружения федеративного домена.</span><span class="sxs-lookup"><span data-stu-id="31f57-135">Determine your requirements for federated domain discovery:</span></span>
    
      - <span></span>  
        <span data-ttu-id="31f57-136">Для ручной настройки федерации необходимо иметь полное доменное имя (FQDN) сервера граничного и доменного имени партнера или доменное имя домена, которое вводится на панели управления Lync Server, **Федерации и внешнего доступа, а** также в **федеративных доменах SIP**.</span><span class="sxs-lookup"><span data-stu-id="31f57-136">For manual configuration of federation, you must have the fully qualified domain name (FQDN) of the partner’s Edge Server and domain name, or online domain name, which is entered in the Lync Server Control Panel, **Federation and External Access**, **SIP Federated Domains**.</span></span> <span data-ttu-id="31f57-137">Создание **новой** политики или **изменение** существующей политики для разрешения или блокировки доменов по полному доменному имени.</span><span class="sxs-lookup"><span data-stu-id="31f57-137">Create a **New** policy or **Edit** an existing policy to either allow or block domains by FQDN.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="31f57-138">Ручная настройка пограничного сервера партнера Федерации может привести к сбою в событии, которое партнер изменяет IP-адрес пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="31f57-138">Manual configuration of a federation partner’s Edge Server is prone to failure in the event that the partner changes the IP address of their Edge Server.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="31f57-139">Для <STRONG>новых федеративных доменов SIP</STRONG>необходимо указать <STRONG>доменное имя (или FQDN)</STRONG> для Microsoft Lync Online и microsoft 365 или Office 365.</span><span class="sxs-lookup"><span data-stu-id="31f57-139">For <STRONG>New SIP Federated Domains</STRONG>, you must provide the <STRONG>Domain name (or FQDN)</STRONG> for Microsoft Lync Online and Microsoft 365 or Office 365.</span></span> <span data-ttu-id="31f57-140">Для Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server также необходимо предоставить <STRONG>службу пограничного доступа (FQDN)</STRONG></span><span class="sxs-lookup"><span data-stu-id="31f57-140">For Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server you must also provide an <STRONG>Access Edge service (FQDN)</STRONG></span></span>

        
        </div>
    
      - <span></span>  
        <span data-ttu-id="31f57-141">Для обнаруженной Федерации партнеров, где партнеры могут найти пограничный сервер, вы создаете запись SRV в внешней службе DNS- \_ sipfederationtls. \_ tcp.contoso.com – это указывает на порт 5061 и запись узла (A) пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="31f57-141">For discovered partner federation, where partners can discover your Edge Server, you create an SRV record in your external DNS - \_sipfederationtls.\_tcp.contoso.com – which points to the port 5061 and the host (A) record of your Edge Server</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="31f57-142">Если вы используете клиент Microsoft Lync Mobile на Windows Phone или Apple iPhone, iPad и других устройствах Apple, а также используете службу push-уведомлений или службу push-уведомлений, вы должны спланировать использование _sipfederationtls. _tcp.</span><span class="sxs-lookup"><span data-stu-id="31f57-142">If you are supporting Microsoft Lync Mobile clients on either Windows Phone or Apple iPhone, iPad, or other Apple devices and are using the Push Notification Service or Push Notification Service, you must plan for _sipfederationtls._tcp.</span></span> <span data-ttu-id="31f57-143">&lt;SRV- &gt; записи домена SIP для каждого домена SIP, на котором установлены мобильные клиенты Lync.</span><span class="sxs-lookup"><span data-stu-id="31f57-143">&lt;SIP domain&gt; SRV records for each SIP domain that you have Lync Mobile clients.</span></span> <span data-ttu-id="31f57-144">Для Android и Nokia Symbian Lync Mobile не следует использовать push-уведомления и не подвергаться этим требованиям.</span><span class="sxs-lookup"><span data-stu-id="31f57-144">Android and Nokia Symbian Lync Mobile do not use push notification and are not subject to this requirement.</span></span>

        
        </div>

  - <span data-ttu-id="31f57-145">Настройка политик доступа внешних пользователей для поддержки федеративных доменов</span><span class="sxs-lookup"><span data-stu-id="31f57-145">Configure external user access policies to support federated domains</span></span>

  - <span data-ttu-id="31f57-146">Откройте порты брандмауэра для протокола запуска сеансов (SIP), веб-конференций, аудио-и видеосвязи, чтобы включить в нее Федерацию или контакты.</span><span class="sxs-lookup"><span data-stu-id="31f57-146">Open firewall ports for session initiation protocol (SIP), web conferencing and audio/visual to accommodate the federation or contacts that you are enabling.</span></span> <span data-ttu-id="31f57-147">Подробности можно найти в статье [Определение внешних параметров брандмауэра/V и портов для Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="31f57-147">For details, see: [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span></span>

<span data-ttu-id="31f57-148">Ниже приведены сведения, которые помогут вам определить требования к сертификатам, портам и протоколам и DNS для Федерации с Microsoft Lync Server 2013 и Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="31f57-148">The following information will aid you in defining the certificate, port/protocol and DNS requirements for federation with Microsoft Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="31f57-149">Планирование сертификатов, брандмауэров и требований к портам и протоколам и требованиям DNS обычно является прямым перенаправленным процессом, если вы планируете или развернули сервер Microsoft Lync Server 2013 Edge.</span><span class="sxs-lookup"><span data-stu-id="31f57-149">Planning for certificates, firewall and port/protocol requirements and DNS requirements is generally a straight forward process if you have planned or deployed your Microsoft Lync Server 2013 Edge Servers.</span></span> <span data-ttu-id="31f57-150">Поскольку Федерация — это дополнительная функция, использующая существующий пограничный сервер, требования к планированию обычно выполняются планированием и развертыванием пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="31f57-150">Because federation is an additional feature that uses the existing Edge Server, the planning requirements are generally met by the Edge Server planning and deployment.</span></span> <span data-ttu-id="31f57-151">Для определения соответствия требованиям и внесения изменений в порт/протокол и DNS следует использовать приведенные ниже таблицы.</span><span class="sxs-lookup"><span data-stu-id="31f57-151">You should use the following tables to determine that your requirements are met and make changes in port/protocol and DNS accordingly.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="31f57-152">Если у вас есть пул пограничных серверов и вы используете сервер Lync Server 2013 или Lync Server 2010, вы можете использовать либо балансировку нагрузки DNS, либо подсистему балансировки нагрузки для оборудования на внутренних и внешних сторонах пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="31f57-152">If you have a pool of Edge Servers and are federating with Lync Server 2013 or Lync Server 2010 partners, then you can use either DNS load balancing or hardware load balancers on the internal and external facing sides of the Edge Servers.</span></span> <span data-ttu-id="31f57-153">Если вы предоставляете Федерацию с Office Communications Server 2007 или Office Communications Server 2007 R2, аппаратная балансировка нагрузки обеспечивает поддержку перехода на другой ресурс в случае пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="31f57-153">If you are federating with Office Communications Server 2007 or Office Communications Server 2007 R2, hardware load balancing will provide failover support in the event of an Edge Server.</span></span> <span data-ttu-id="31f57-154">Office Communications Server 2007 и Office Communications Server 2007 R2 не поддерживают балансировку нагрузки DNS.</span><span class="sxs-lookup"><span data-stu-id="31f57-154">Office Communications Server 2007 and Office Communications Server 2007 R2 are not DNS load balancing aware.</span></span> <span data-ttu-id="31f57-155">Пограничные серверы партнеров будут устанавливать связь с первым пограничным сервером в пуле, который отвечает.</span><span class="sxs-lookup"><span data-stu-id="31f57-155">The partner Edge Servers will establish communication with the first Edge Server in your pool that responds.</span></span> <span data-ttu-id="31f57-156">Если пограничный сервер завершается сбоем, Обмен данными не выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="31f57-156">If that Edge Server fails, communication does not automatically failover.</span></span>



</div>

<span data-ttu-id="31f57-157">Требования к сертификатам обычно выполняются с помощью планирования сертификатов для выбранного пограничного сервера или плана пограничного сервера в пуле.</span><span class="sxs-lookup"><span data-stu-id="31f57-157">Certificate requirements are typically met through the planning of certificates for your chosen Edge Server or pooled Edge Server plan.</span></span>

</div>

<div>

## <a name="public-instant-messaging-connectivity"></a><span data-ttu-id="31f57-158">Общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="31f57-158">Public Instant Messaging Connectivity</span></span>

<span data-ttu-id="31f57-159">Общедоступная служба обмена мгновенными сообщениями является классом Федерации и настроена на разрешение внутренних и внешних пользователей Lync Server 2013 для добавления контактов из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="31f57-159">Public Instant Messaging Connectivity is a class of federation, and is configured to allow your internal and external Lync Server 2013 users to add contacts from any of the following:</span></span>

  - <span data-ttu-id="31f57-160">Контакты Messenger</span><span class="sxs-lookup"><span data-stu-id="31f57-160">Messenger contacts</span></span>

  - <span data-ttu-id="31f57-161">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="31f57-161">Yahoo\!</span></span> <span data-ttu-id="31f57-162">контакты,</span><span class="sxs-lookup"><span data-stu-id="31f57-162">contacts</span></span>

  - <span data-ttu-id="31f57-163">Контакты из Skype Online (AOL)</span><span class="sxs-lookup"><span data-stu-id="31f57-163">America Online (AOL) contacts</span></span>

<div>


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="31f57-164">За Сентябрь 1 сентября 2012 г. Лицензия на подписку на общедоступные пользователи Microsoft Lync (PIC USL) больше не доступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="31f57-164">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="31f57-165">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="31f57-165">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="31f57-166">Messenger, пока не задействуется Дата завершения работы (Точная дата все еще не решена, но не раньше июня 2013).</span><span class="sxs-lookup"><span data-stu-id="31f57-166">Messenger until the service shutdown date (exact date is still to be decided, but no sooner than June 2013).</span></span></P>
> <LI>
> <P><span data-ttu-id="31f57-167">USL PIC является лицензией на подписку "на пользователя", которая требуется для использования Lync Server или Office Communications Server для Федерации с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="31f57-167">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="31f57-168">Messenger.</span><span class="sxs-lookup"><span data-stu-id="31f57-168">Messenger.</span></span> <span data-ttu-id="31f57-169">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого она не будет продлена.</span><span class="sxs-lookup"><span data-stu-id="31f57-169">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="31f57-170">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="31f57-170">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="31f57-171">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="31f57-171">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="31f57-172">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут получать сотни миллионов людей с помощью голосовой почты и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="31f57-172">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="31f57-173">Для этого класса Федерации требуются следующие вопросы планирования:</span><span class="sxs-lookup"><span data-stu-id="31f57-173">This class of federation requires the following planning considerations:</span></span>

  - <span data-ttu-id="31f57-174">Пользователи Windows Live Messenger могут иметь доступ к одноранговой голосовой и видеосвязи с пользователями Lync Server 2013, а также обмениваться мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="31f57-174">Windows Live Messenger users can have peer-to-peer audio/visual communication with Lync Server 2013 users, in addition to instant messaging.</span></span> <span data-ttu-id="31f57-175">Пограничные серверы должны соответствовать конкретным требованиям к порту и протоколу.</span><span class="sxs-lookup"><span data-stu-id="31f57-175">Your Edge Servers must meet specific port and protocol requirements.</span></span> <span data-ttu-id="31f57-176">Подробности можно найти [в разделе Определение внешних параметров брандмауэра/V и требований к портам для Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="31f57-176">For details, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

  - <span data-ttu-id="31f57-177">В обмене сообщениями Yahoo нет уникальных требований, кроме тех, которые обычно используются при планировании и развертывании типичного пограничного сервера, предоставляющего Федерацию.</span><span class="sxs-lookup"><span data-stu-id="31f57-177">Yahoo instant messaging has no unique requirements, other than those typically used in the planning and deployment of the typical Edge Server that is providing federation.</span></span>

  - <span data-ttu-id="31f57-178">Для использования Skype Online требуется, чтобы сертификат пограничного сервера, назначенный службе EDGE, использовал улучшенное использование ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="31f57-178">America Online requires that your Edge Server certificate assigned to the Access Edge service has a client enhanced key usage (EKU).</span></span>

</div>

<div>

## <a name="extensible-messaging-and-presence-protocol-xmpp-federation"></a><span data-ttu-id="31f57-179">Интеграция расширяемых сообщений и протоколов присутствия (XMPP)</span><span class="sxs-lookup"><span data-stu-id="31f57-179">Extensible Messaging and Presence Protocol (XMPP) Federation</span></span>

<span data-ttu-id="31f57-180">Предыдущие версии Lync Server и Office Communications Server предоставили шлюз расширенных сообщений и протоколов доступа (XMPP), который можно развернуть как отдельную серверную роль, разрешающую Федерацию с помощью XMPPных развертываний.</span><span class="sxs-lookup"><span data-stu-id="31f57-180">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="31f57-181">В Microsoft Lync Server 2013 функциональность XMPP может быть развернута как функция.</span><span class="sxs-lookup"><span data-stu-id="31f57-181">In Microsoft Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="31f57-182">Функции XMPP устанавливаются в двух частях: прокси-сервер XMPP, который работает на пограничном сервере и шлюз XMPP, который работает на серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31f57-182">XMPP functionality is installed in two parts: an XMPP proxy that runs on the Edge Server and the XMPP gateway that runs on the Front End Servers.</span></span>

<span data-ttu-id="31f57-183">Развертывание и Настройка XMPP рассматривается при [развертывании внешних пользователей в Lync Server 2013](lync-server-2013-deploying-external-user-access.md) вы планируете поддерживать XMPP в вашей организации, определяя правила порта и протоколов в брандмауэре, настройку сертификатов и добавление записей DNS.</span><span class="sxs-lookup"><span data-stu-id="31f57-183">Deployment and configuration of XMPP is covered in [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) You plan for supporting XMPP in your organization by defining port and protocol rules on your firewall, configuration of certificates, and adding DNS records.</span></span> <span data-ttu-id="31f57-184">В следующих разделах приведены сведения о том, как вам потребуется успешно спланировать XMPP Федерацию для развертывания.</span><span class="sxs-lookup"><span data-stu-id="31f57-184">The following topics in this section summarize the information that you will need to successfully plan XMPP federation for your deployment.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="31f57-p120">Возможность XMPP сервера Lync Server 2013 была протестирована корпорацией Microsoft и поддерживается в части федеративного обмена мгновенными сообщениями с использованием Google Talk. По вопросам использования других XMPP-систем обращайтесь к сторонним поставщикам, чтобы выяснить, поддерживают ли они федерацию с Lync Server 2013, а также чтобы получить рекомендации по вопросам, связанным с устранением неполадок и развертыванием.</span><span class="sxs-lookup"><span data-stu-id="31f57-p120">The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.</span></span>



</div>

<div>


> [!IMPORTANT]
> <span data-ttu-id="31f57-187">XMPP Федерация не поддерживается для пользователей, которые размещаются на устройствах с возможностью бесперебойной ветви.</span><span class="sxs-lookup"><span data-stu-id="31f57-187">XMPP federation is not supported for users who are homed on survivable branch appliances.</span></span> <span data-ttu-id="31f57-188">Это относится и к сведениям о присутствии, и по обмену МГНОВЕНными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="31f57-188">This applies to both seeing presence information and exchanging IM messages.</span></span>



</div>

</div>

<div id="sectionSection3" class="section">

<span data-ttu-id="31f57-189">В следующих разделах содержатся инструкции по определению сертификатов, портов брандмауэра и DNS-записей для типов поддерживаемых сценариев Федерации.</span><span class="sxs-lookup"><span data-stu-id="31f57-189">In the following topics contain guidance for defining certificates, firewall ports and DNS entries for the types of supported federation scenarios.</span></span>

  - <span></span>  
    [<span data-ttu-id="31f57-190">Общие сведения о сертификате: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-190">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - <span></span>  
    [<span data-ttu-id="31f57-191">Общие сведения о портах: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-191">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - <span></span>  
    [<span data-ttu-id="31f57-192">Сводка DNS-SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-192">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="31f57-193">См. также</span><span class="sxs-lookup"><span data-stu-id="31f57-193">See Also</span></span>


[<span data-ttu-id="31f57-194">Настройка политик управления доступом федеративных пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-194">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  


[<span data-ttu-id="31f57-195">Сценарии доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-195">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="31f57-196">Определение требований к внешнему брандмауэру аудио- и видеосвязи и портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-196">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
[<span data-ttu-id="31f57-197">Определение требований DNS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-197">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="31f57-198">Управление конфигурацией пограничного сервера в организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-198">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-access-edge-configuration-for-your-organization.md)  
[<span data-ttu-id="31f57-199">Управление федеративными доменами SIP для организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-199">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="31f57-200">Управление федеративными поставщиками SIP в организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f57-200">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
  

<span data-ttu-id="31f57-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31f57-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

