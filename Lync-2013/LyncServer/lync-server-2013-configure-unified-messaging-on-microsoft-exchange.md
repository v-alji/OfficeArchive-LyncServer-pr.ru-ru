---
title: 'Lync Server 2013: Настройка единой системы обмена сообщениями на сервере Microsoft Exchange'
description: 'Lync Server 2013: Настройте единую систему обмена сообщениями на сервере Microsoft Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Unified Messaging on Microsoft Exchange
ms:assetid: 07547968-c59b-4dde-ace4-9fd286933759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398129(v=OCS.15)
ms:contentKeyID: 48183311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8db43bbe50061a1a044bdd34b637ba86f626ca85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400069"
---
# <a name="configure-unified-messaging-on-microsoft-exchange-for-lync-server-2013"></a><span data-ttu-id="13833-103">Настройка единой системы обмена сообщениями в Microsoft Exchange для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13833-103">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13833-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13833-104">

<span> </span></span></span>

<span data-ttu-id="13833-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="13833-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="13833-106">В этой статье описано, как настроить единую систему обмена сообщениями Exchange (UM) на сервере Microsoft Exchange для использования с корпоративной голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="13833-106">This topic describes how to configure Exchange Unified Messaging (UM) on a Microsoft Exchange Server for use with Enterprise Voice.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="13833-107">Примеры командлетов в этом разделе содержат синтаксис для версии Exchange 2007 среды Exchange Management Shell.</span><span class="sxs-lookup"><span data-stu-id="13833-107">The cmdlet examples in this topic provide syntax for the Exchange 2007 version of Exchange Management Shell.</span></span> <span data-ttu-id="13833-108">Если вы используете Exchange 2010 или Exchange 2013, ознакомьтесь с соответствующей документацией в соответствии с указанными ссылками.</span><span class="sxs-lookup"><span data-stu-id="13833-108">If you are running Exchange 2010 or Exchange 2013, see the appropriate documentation as referenced.</span></span>



</div>

<div>

## <a name="to-configure-a-server-running-exchange-server-um"></a><span data-ttu-id="13833-109">Настройка сервера, на котором работает UM-сервер Exchange</span><span class="sxs-lookup"><span data-stu-id="13833-109">To configure a server running Exchange Server UM</span></span>

1.  <span data-ttu-id="13833-110">Создайте абонентскую группу SIP (универсального кода ресурса) для каждого из профилей местоположения вашего голоса.</span><span class="sxs-lookup"><span data-stu-id="13833-110">Create a UM Session Initiation Protocol (SIP) Uniform Resource Identifier (URI) dial plan for each of your Enterprise Voice location profiles.</span></span> <span data-ttu-id="13833-111">Если вы решили использовать консоль управления Exchange, создайте новую абонентскую группу с защищенным параметром безопасности **(предпочтительно)**.</span><span class="sxs-lookup"><span data-stu-id="13833-111">If you choose to use the Exchange Management Console, create a new dial plan with the security setting **Secured (preferred)**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="13833-112">Если для параметра безопасности задано значение " <STRONG>SIP secures</STRONG> ", для которого требуется шифрование только за трафик SIP, как было рекомендовано, обратите внимание на то, что этот параметр безопасности для абонентской группы недостаточен, если для пула переднего плана задано шифрование, что означает, что для пула требуется шифрование для трафика SIP и RTP.</span><span class="sxs-lookup"><span data-stu-id="13833-112">If you set your security setting value to <STRONG>SIP Secured</STRONG> to require encryption for SIP traffic only, as previously recommended, note that this security setting on a dial plan is insufficient if the Front End pool is configured to require encryption, which means the pool requires encryption for both SIP and RTP traffic.</span></span> <span data-ttu-id="13833-113">Если параметры безопасности для абонентской группы и пула несовместимы, все звонки на Exchange UM из пула переднего плана будут завершаться сбоем, что приведет к ошибке, указывающей на то, что у вас есть несовместимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="13833-113">When the dial plan and pool security settings are not compatible, all calls to Exchange UM from the Front End pool will fail, resulting in an error indicating that you have an "Incompatible security setting."</span></span>

    
    </div>
    
    <span data-ttu-id="13833-114">Если вы используете консоль управления Exchange, введите:</span><span class="sxs-lookup"><span data-stu-id="13833-114">If you use the Exchange Management Shell, type:</span></span>
    ```powershell
     New-UMDialPlan -Name <dial plan name> -UriType "SipName" -VoipSecurity <SIPSecured|Unsecured|Secured> -NumberOfDigitsInExtension <number of digits> -AccessTelephoneNumbers <access number in E.164 format>
    ```
    <span data-ttu-id="13833-115">Для получения дополнительных сведений см.:</span><span class="sxs-lookup"><span data-stu-id="13833-115">For details, see:</span></span>
    
      - <span data-ttu-id="13833-116">В Office Communications Server 2007 вы можете ознакомиться с разрешениями "Создание абонентской группы SIP для единой системы обмена сообщениями" [https://go.microsoft.com/fwlink/p/?LinkId=268632](https://go.microsoft.com/fwlink/p/?linkid=268632) и "New-UMDialPlan: Exchange 2007" [https://go.microsoft.com/fwlink/p/?LinkId=268666](https://go.microsoft.com/fwlink/p/?linkid=268666) .</span><span class="sxs-lookup"><span data-stu-id="13833-116">For Office Communications Server 2007, see "How to Create a Unified Messaging SIP URI Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268632](https://go.microsoft.com/fwlink/p/?linkid=268632) and "New-UMDialplan: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268666](https://go.microsoft.com/fwlink/p/?linkid=268666).</span></span>
    
      - <span data-ttu-id="13833-117">В Exchange 2010 вы видите раздел "Создание абонентской группы единой системы обмена сообщениями" на странице " [https://go.microsoft.com/fwlink/p/?LinkId=268674](https://go.microsoft.com/fwlink/p/?linkid=268674) New-UMDialPlan: Exchange 2010" [https://go.microsoft.com/fwlink/p/?LinkId=268680](https://go.microsoft.com/fwlink/p/?linkid=268680) .</span><span class="sxs-lookup"><span data-stu-id="13833-117">For Exchange 2010, see "Create a UM Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268674](https://go.microsoft.com/fwlink/p/?linkid=268674) and "New-UMDialplan: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268680](https://go.microsoft.com/fwlink/p/?linkid=268680).</span></span>
    
      - <span data-ttu-id="13833-118">Для Exchange 2013 следует ознакомиться в разделе "Единая система обмена сообщениями" [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) .</span><span class="sxs-lookup"><span data-stu-id="13833-118">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="13833-119">Выбор уровня безопасности <STRONG>SIPSecured</STRONG> или <STRONG>Защита</STRONG> зависит от того, активирована или деактивирована ли протокол передачи данных в режиме реального времени (SRTP) для шифрования мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="13833-119">Whether you select a security level of <STRONG>SIPSecured</STRONG> or <STRONG>Secured</STRONG> depends on whether secure real-time transport protocol (SRTP) is activated or deactivated for media encryption.</span></span> <span data-ttu-id="13833-120">Интеграция с единой системой обмена сообщениями Exchange для интеграции с Lync Server 2010 соответствует уровню шифрования в конфигурации мультимедиа Lync Server.</span><span class="sxs-lookup"><span data-stu-id="13833-120">For the Lync Server 2010 integration with Exchange UM, this should correspond to the encryption level in the Lync Server media configuration.</span></span> <span data-ttu-id="13833-121">Чтобы просмотреть конфигурацию мультимедиа Lync Server, запустите командлет <STRONG>Get-CsMediaConfiguration</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="13833-121">The Lync Server media configuration can be viewed by running the <STRONG>Get-CsMediaConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="13833-122">Подробные сведения можно найти в разделе Get-CsMediaConfiguration в документации по среде управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="13833-122">For details, see Get-CsMediaConfiguration in the Lync Server Management Shell documentation.</span></span><BR><span data-ttu-id="13833-123">Подробнее о том, как выбрать соответствующий параметр безопасности в службе VoIP, можно найти <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">в разделе процесс развертывания для интеграции локальной системы обработки сообщений и Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="13833-123">For details about selecting the appropriate VoIP Security setting, see <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="13833-124">Чтобы получить полное доменное имя (FQDN) для каждой абонентской группы единой системы обмена сообщениями, выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="13833-124">Run the following cmdlet to obtain the fully qualified domain name (FQDN) for each UM dial plan:</span></span>
    
    ```powershell
    (Get-UMDialPlan <dialplanname>).PhoneContext  
    ```
    
    <span data-ttu-id="13833-125">Для получения дополнительных сведений см.:</span><span class="sxs-lookup"><span data-stu-id="13833-125">For details, see:</span></span>
    
      - <span data-ttu-id="13833-126">Дополнительные сведения об Exchange 2007 можно найти в статье "Get-UMDialplan: Exchange 2007" [https://go.microsoft.com/fwlink/p/?LinkId=268678](https://go.microsoft.com/fwlink/p/?linkid=268678) .</span><span class="sxs-lookup"><span data-stu-id="13833-126">For Exchange 2007, see "Get-UMDialplan: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268678](https://go.microsoft.com/fwlink/p/?linkid=268678).</span></span>
    
      - <span data-ttu-id="13833-127">Дополнительные сведения об Exchange 2010 можно найти в статье "Get-UMDialplan: Exchange 2010" [https://go.microsoft.com/fwlink/p/?LinkId=268679](https://go.microsoft.com/fwlink/p/?linkid=268679) .</span><span class="sxs-lookup"><span data-stu-id="13833-127">For Exchange 2010, see "Get-UMDialplan: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268679](https://go.microsoft.com/fwlink/p/?linkid=268679).</span></span>
    
      - <span data-ttu-id="13833-128">Для Exchange 2013 следует ознакомиться в разделе "Единая система обмена сообщениями" [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) .</span><span class="sxs-lookup"><span data-stu-id="13833-128">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>

3.  <span data-ttu-id="13833-129">Запишите имя абонентской группы для каждой абонентской группы единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="13833-129">Record the dial plan name of each UM dial plan.</span></span> <span data-ttu-id="13833-130">В зависимости от используемой версии Exchange Server может потребоваться использовать полное доменное имя каждого имени абонентского плана в соответствии с именем каждой соответствующей абонентской группы Lync Server, чтобы имена абонентских групп соответствовали друг другу.</span><span class="sxs-lookup"><span data-stu-id="13833-130">Depending on your version of Exchange Server, you may need to use the FQDN of each dial plan name later as the name of each UM dial plan’s corresponding Lync Server dial plan so that the dial plan names match.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="13833-131">Имена абонентской группы Lync Server должны совпадать с именами абонентских групп UM только в том случае, если абонентская группа UM работает в более <EM>ранней</EM> версии Exchange, чем Exchange 2010 с пакетом обновления 1.</span><span class="sxs-lookup"><span data-stu-id="13833-131">Lync Server dial plan names must match UM dial plan names only if the UM dial plan is running on a version of Exchange <EM>earlier</EM> than Exchange 2010 SP1.</span></span>

    
    </div>

4.  <span data-ttu-id="13833-132">Добавьте абонентскую группу на сервер, на котором запущена служба Exchange UM, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="13833-132">Add the dial plan to the server running Exchange UM as follows:</span></span>
    
      - <span data-ttu-id="13833-133">Если вы решили использовать консоль управления Exchange, вы можете добавить абонентскую группу из страницы свойств сервера.</span><span class="sxs-lookup"><span data-stu-id="13833-133">If you choose to use the Exchange Management Console, you can add the dial plan from the property sheet for the server.</span></span> <span data-ttu-id="13833-134">Конкретные инструкции можно найти в документации по продукту Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13833-134">For specific instructions, see the Exchange Server product documentation.</span></span>
        
        <span data-ttu-id="13833-135">Сведения о том, как добавить сервер единой системы обмена сообщениями в абонентскую группу Exchange 2007, можно найти по адресу " [https://go.microsoft.com/fwlink/p/?LinkId=268681](https://go.microsoft.com/fwlink/p/?linkid=268681) .</span><span class="sxs-lookup"><span data-stu-id="13833-135">For Exchange 2007, see "How to Add Unified Messaging Server to a Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268681](https://go.microsoft.com/fwlink/p/?linkid=268681).</span></span>
        
        <span data-ttu-id="13833-136">Для Exchange 2010 вы увидите в разделе "Просмотр или Настройка свойств сервера UM" [https://go.microsoft.com/fwlink/p/?LinkId=268682](https://go.microsoft.com/fwlink/p/?linkid=268682) .</span><span class="sxs-lookup"><span data-stu-id="13833-136">For Exchange 2010, see "View or Configure the Properties of a UM Server" at [https://go.microsoft.com/fwlink/p/?LinkId=268682](https://go.microsoft.com/fwlink/p/?linkid=268682).</span></span>
        
        <span data-ttu-id="13833-137">Для Exchange 2013 следует ознакомиться в разделе "Единая система обмена сообщениями" [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) .</span><span class="sxs-lookup"><span data-stu-id="13833-137">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>
    
      - <span data-ttu-id="13833-138">Если вы используете командную консоль Exchange, выполните указанные ниже действия для каждого из серверов Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="13833-138">If you use the Exchange Management Shell, run the following for each of your Exchange UM servers:</span></span>
        ```powershell
        $ums=get-umserver; 
        $dp=get-umdialplan -id <name of dial-plan created in step 1>; 
        $ums[0].DialPlans +=$dp.Identity; 
        set-umservice -instance $ums[0]
        ```
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="13833-139">Перед выполнением следующего действия Убедитесь в том, что все пользователи организации голосовой связи настроены с помощью почтового ящика Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13833-139">Before you perform the following step, make sure that all Enterprise Voice users have been configured with an Exchange Server mailbox.</span></span><BR><span data-ttu-id="13833-140">Сведения об Exchange 2007 можно найти в библиотеке TechNet на сайте Exchange Server 2007 <A href="https://go.microsoft.com/fwlink/p/?linkid=268685">https://go.microsoft.com/fwlink/p/?LinkId=268685</A> .</span><span class="sxs-lookup"><span data-stu-id="13833-140">For Exchange 2007, see the Exchange Server 2007 TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268685">https://go.microsoft.com/fwlink/p/?LinkId=268685</A>.</span></span><BR><span data-ttu-id="13833-141">Сведения об Exchange 2010 можно найти в библиотеке TechNet на сайте Exchange Server 2010 <A href="https://go.microsoft.com/fwlink/p/?linkid=268686">https://go.microsoft.com/fwlink/p/?LinkId=268686</A> .</span><span class="sxs-lookup"><span data-stu-id="13833-141">For Exchange 2010, see the Exchange Server 2010 TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268686">https://go.microsoft.com/fwlink/p/?LinkId=268686</A>.</span></span><BR><span data-ttu-id="13833-142">При указании политики почтовых ящиков для каждой абонентской группы, созданной в действии 1, выберите либо политику по умолчанию, либо ее созданную.</span><span class="sxs-lookup"><span data-stu-id="13833-142">When specifying a mailbox policy for each dial plan that you created in step 1, select either the default policy or one that you have created.</span></span>

    
    </div>

5.  <span data-ttu-id="13833-143">Перейдите к разделу \<Exchange installation directory\> \\ сценарии, а затем, если Exchange развернут в одном лесе, введите:</span><span class="sxs-lookup"><span data-stu-id="13833-143">Navigate to \<Exchange installation directory\>\\Scripts, and then if Exchange is deployed in a single forest, type:</span></span>
    ```console
    exchucutil.ps1
    ```
    <span data-ttu-id="13833-144">Если Exchange развернут в нескольких лесах, введите:</span><span class="sxs-lookup"><span data-stu-id="13833-144">Or, if Exchange is deployed in multiple forests, type:</span></span>
    ```console
    exchucutil.ps1 -Forest:"<forest FQDN>"
    ```
    <span data-ttu-id="13833-145">где полное доменное имя леса определяет лес, в котором развернут Lync Server.</span><span class="sxs-lookup"><span data-stu-id="13833-145">where forest FQDN specifies the forest in which Lync Server is deployed.</span></span>
    
    <span data-ttu-id="13833-146">Если у вас есть одна или несколько абонентских групп UM, которые связаны с несколькими IP-шлюзами, перейдите к действию 6.</span><span class="sxs-lookup"><span data-stu-id="13833-146">If you have one or more UM dial plans that are associated with multiple IP gateways, continue to step 6.</span></span> <span data-ttu-id="13833-147">Если абонентские группы связаны только с одним IP-шлюзом, пропустите шаг 6.</span><span class="sxs-lookup"><span data-stu-id="13833-147">If your dial plans are each associated with only a single IP gateway, skip step 6.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="13833-148">Не забудьте перезапустить службу <STRONG>переднего плана Lync Server</STRONG> (rtcsrv.exe) <EM>после</EM> запуска exchucutil.ps1.</span><span class="sxs-lookup"><span data-stu-id="13833-148">Be sure to restart the <STRONG>Lync Server Front-End</STRONG> service (rtcsrv.exe) <EM>after</EM> you run exchucutil.ps1.</span></span> <span data-ttu-id="13833-149">В противном случае Lync Server не будет определять единую систему обмена сообщениями в топологии.</span><span class="sxs-lookup"><span data-stu-id="13833-149">Otherwise, Lync Server will not detect Unified Messaging in the topology.</span></span>

    
    </div>

6.  <span data-ttu-id="13833-150">Используя среду управления Exchange или консоль управления Exchange, отключите исходящие вызовы для всех IP-шлюзов, связанных с каждой из ваших абонентских планов.</span><span class="sxs-lookup"><span data-stu-id="13833-150">Using either the Exchange Management Shell or Exchange Management Console, disable outbound calling for all but one of the IP gateways associated with each of your dial plans.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="13833-151">Этот этап необходим для того, чтобы убедиться в том, что исходящие вызовы на сервере, на котором работает единая система обмена сообщениями Exchange, (например, как в случае с сценариями воспроизведения на телефоне) надежно просматривают корпоративный брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="13833-151">This step is necessary to make sure that outbound calls by the server running Exchange Server Unified Messaging to external users (for example, as is the case with play-on-phone scenarios) reliably traverse the corporate firewall.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="13833-152">При выборе IP-шлюза UM, через который разрешены исходящие вызовы, выберите тот, который скорее всего будет обрабатывать весь трафик.</span><span class="sxs-lookup"><span data-stu-id="13833-152">When selecting the UM IP gateway through which to allow outgoing calls, choose the one that is likely to handle the most traffic.</span></span> <span data-ttu-id="13833-153">Не разрешать исходящий трафик через шлюз IP, который подключается к группе режиссеров Lync Server.</span><span class="sxs-lookup"><span data-stu-id="13833-153">Do not allow outgoing traffic through an IP gateway that connects to a pool of Lync Server Directors.</span></span> <span data-ttu-id="13833-154">Также Избегайте пулов на другом центральном сайте или сайте ветви.</span><span class="sxs-lookup"><span data-stu-id="13833-154">Also avoid pools in another central site or a branch site.</span></span> <span data-ttu-id="13833-155">Для блокирования исходящих звонков через шлюз IP можно использовать один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="13833-155">You can use either of the following methods to block outgoing calls from passing through an IP gateway:</span></span>

    
    </div>
    
      - <span data-ttu-id="13833-156">Если вы используете консоль управления Exchange, отключите каждый шлюз IP, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="13833-156">If you use the Exchange Management Shell, disable each IP gateway by running the following command:</span></span>
        ```powershell
        Set-UMIPGateway <gatewayname> -OutcallsAllowed $false
        ```
        <span data-ttu-id="13833-157">Инструкции для Exchange 2007 можно найти в разделе "Set-UMIPGateway: Exchange 2007 Help" [https://go.microsoft.com/fwlink/p/?LinkId=268687](https://go.microsoft.com/fwlink/p/?linkid=268687) .</span><span class="sxs-lookup"><span data-stu-id="13833-157">For Exchange 2007, see "Set-UMIPGateway: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268687](https://go.microsoft.com/fwlink/p/?linkid=268687).</span></span>
        
        <span data-ttu-id="13833-158">Инструкции для Exchange 2010 можно найти в разделе "Set-UMIPGateway: Exchange 2010 Help" [https://go.microsoft.com/fwlink/p/?LinkId=268688](https://go.microsoft.com/fwlink/p/?linkid=268688) .</span><span class="sxs-lookup"><span data-stu-id="13833-158">For Exchange 2010, see "Set-UMIPGateway: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268688](https://go.microsoft.com/fwlink/p/?linkid=268688).</span></span>
    
      - <span data-ttu-id="13833-159">Если вы используете консоль управления Exchange, снимите флажок **Разрешить исходящие вызовы через этот IP-шлюз** .</span><span class="sxs-lookup"><span data-stu-id="13833-159">If you use the Exchange Management Console, clear the **Allow outgoing calls through this IP gateway** check box.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="13833-160">Если абонентская группа SIP для обмена сообщениями с URI связана только с одним IP-шлюзом, не запретите исходящие вызовы через этот шлюз.</span><span class="sxs-lookup"><span data-stu-id="13833-160">If your UM SIP URI dial plan is associated with only a single IP gateway, do not disallow outgoing calls through this gateway.</span></span>

    
    </div>

7.  <span data-ttu-id="13833-161">Создание автосекретаря UM для каждой абонентской группы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="13833-161">Create a UM auto-attendant for each Lync Server dial plan.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="13833-162">Не включайте пробелы в имя автосекретаря.</span><span class="sxs-lookup"><span data-stu-id="13833-162">Do not include any spaces in the name of the auto attendant.</span></span>

    
    </div>
    
    ```powershell
    New-umautoattendant -name <auto attendant name> -umdialplan < name of dial plan created in step 1> -PilotIdentifierList <auto attendant phone number in E.164 format> -SpeechEnabled $true -Status Enabled
    ```
    <span data-ttu-id="13833-163">Для получения дополнительных сведений см.:</span><span class="sxs-lookup"><span data-stu-id="13833-163">For details, see:</span></span>
    
      - <span data-ttu-id="13833-164">Дополнительные сведения об Exchange 2007 можно найти в статье "New-UMAutoAttendant: Exchange 2007" [https://go.microsoft.com/fwlink/p/?LinkId=268689](https://go.microsoft.com/fwlink/p/?linkid=268689) .</span><span class="sxs-lookup"><span data-stu-id="13833-164">For Exchange 2007, see "New-UMAutoAttendant: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268689](https://go.microsoft.com/fwlink/p/?linkid=268689).</span></span>
    
      - <span data-ttu-id="13833-165">Дополнительные сведения об Exchange 2010 можно найти в статье "New-UMAutoAttendant: Exchange 2010" [https://go.microsoft.com/fwlink/p/?LinkId=268690](https://go.microsoft.com/fwlink/p/?linkid=268690) .</span><span class="sxs-lookup"><span data-stu-id="13833-165">For Exchange 2010, see "New-UMAutoAttendant: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268690](https://go.microsoft.com/fwlink/p/?linkid=268690).</span></span>
    
    <span data-ttu-id="13833-166">Необходимо выполнить описанные ниже действия для каждого пользователя, если вы включили пользователей Lync Server для корпоративного голосовой связи и знаете их URI SIP.</span><span class="sxs-lookup"><span data-stu-id="13833-166">The following step should be performed for each user after you have enabled Lync Server users for Enterprise Voice and know their SIP URIs.</span></span>

8.  <span data-ttu-id="13833-167">Свяжите пользователей Exchange UM (каждый из которых должен быть настроен с помощью почтового ящика Exchange) с абонентской группой UM и создайте универсальный код ресурса (URI) SIP для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="13833-167">Associate Exchange UM users (each of whom should be configured with an Exchange mail box) with the UM dial plan and create a SIP URI for each user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="13833-168"><STRONG>SIPResourceIdentifier</STRONG> в следующем примере должен быть адресом SIP пользователя Lync Server.</span><span class="sxs-lookup"><span data-stu-id="13833-168">The <STRONG>SIPResourceIdentifier</STRONG> in the following sample must be the SIP address of the Lync Server user.</span></span>

    
    </div>
    
    ```powershell
    enable-ummailbox -id <user name> -ummailboxpolicy <name of the mailbox policy for the dial plan created in step 1> -Extensions <extension> -SIPResourceIdentifier "<user name>@<full domain name>" -PIN <user pin>
    ```
    <span data-ttu-id="13833-169">Для получения дополнительных сведений см.:</span><span class="sxs-lookup"><span data-stu-id="13833-169">For details, see:</span></span>
    
      - <span data-ttu-id="13833-170">Дополнительные сведения об Exchange 2007 можно найти в статье "Enable-UMMailbox: Exchange 2007 Help" [https://go.microsoft.com/fwlink/p/?LinkId=268691](https://go.microsoft.com/fwlink/p/?linkid=268691) .</span><span class="sxs-lookup"><span data-stu-id="13833-170">For Exchange 2007, see "Enable-UMMailbox: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268691](https://go.microsoft.com/fwlink/p/?linkid=268691).</span></span>
    
      - <span data-ttu-id="13833-171">Дополнительные сведения об Exchange 2010 можно найти в статье "Enable-UMMailbox: Exchange 2010 Help" [https://go.microsoft.com/fwlink/p/?LinkId=268692](https://go.microsoft.com/fwlink/p/?linkid=268692) .</span><span class="sxs-lookup"><span data-stu-id="13833-171">For Exchange 2010, see "Enable-UMMailbox: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268692](https://go.microsoft.com/fwlink/p/?linkid=268692).</span></span>

<span data-ttu-id="13833-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13833-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

