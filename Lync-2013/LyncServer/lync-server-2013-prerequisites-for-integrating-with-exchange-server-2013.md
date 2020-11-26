---
title: 'Lync Server 2013: предварительные требования для интеграции с Exchange Server 2013'
description: 'Lync Server 2013: предварительные требования для интеграции с Exchange Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for integrating Lync Server 2013 and Exchange Server 2013
ms:assetid: ea22beb9-c02e-47cb-836d-97a556969052
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721919(v=OCS.15)
ms:contentKeyID: 49733853
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5872fe3ec546997cd0633383fdda7e0549bec83f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436918"
---
# <a name="prerequisites-for-integrating-microsoft-lync-server-2013-and-microsoft-exchange-server-2013"></a><span data-ttu-id="309f6-103">Необходимые условия для интеграции Microsoft Lync Server 2013 и Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="309f6-103">Prerequisites for integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="309f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="309f6-104">

<span> </span></span></span>

<span data-ttu-id="309f6-105">_**Тема последнего изменения:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="309f6-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="309f6-106">Прежде чем приступить к интеграции Microsoft Lync Server 2013 и Microsoft Exchange Server 2013, необходимо убедиться, что выполнены все необходимые меры.</span><span class="sxs-lookup"><span data-stu-id="309f6-106">Before you can integrate Microsoft Lync Server 2013 and Microsoft Exchange Server 2013 you must ensure that all the prerequisite steps have been completed.</span></span> <span data-ttu-id="309f6-107">Как и раньше, интеграция не может быть выполнена, пока не будут полностью установлены и запущены Exchange 2013 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="309f6-107">As you might expect, integration cannot take place until both Exchange 2013 and Lync Server 2013 are fully installed and up and running.</span></span> <span data-ttu-id="309f6-108">Подробнее об установке Exchange можно найти в документации по планированию и развертыванию Exchange 2013 [https://go.microsoft.com/fwlink/p/?LinkId=268539](https://go.microsoft.com/fwlink/p/?linkid=268539) .</span><span class="sxs-lookup"><span data-stu-id="309f6-108">For details about installing Exchange, see the Exchange 2013 Planning and Deployment documentation at [https://go.microsoft.com/fwlink/p/?LinkId=268539](https://go.microsoft.com/fwlink/p/?linkid=268539).</span></span> <span data-ttu-id="309f6-109">Подробные сведения об установке Lync Server 2013 можно найти в документации по планированию и развертыванию [https://go.microsoft.com/fwlink/p/?LinkId=254806](https://go.microsoft.com/fwlink/p/?linkid=254806) .</span><span class="sxs-lookup"><span data-stu-id="309f6-109">For details about installing Lync Server 2013, see the planning and deployment documentation at [https://go.microsoft.com/fwlink/p/?LinkId=254806](https://go.microsoft.com/fwlink/p/?linkid=254806).</span></span>

<span data-ttu-id="309f6-110">После того как серверы будут установлены и запущены, необходимо назначить сертификаты проверки подлинности серверов для Lync Server 2013 и Exchange 2013; Эти сертификаты позволяют Lync Server и Exchange обмениваться информацией и взаимодействовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="309f6-110">After the servers are up and running you must assign server-to-server authentication certificates to both Lync Server 2013 and Exchange 2013; these certificates allow Lync Server and Exchange to exchange information and to communicate with one another.</span></span> <span data-ttu-id="309f6-111">При установке Exchange 2013 создается самозаверяющий сертификат с именем сертификата для проверки подлинности сервера Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="309f6-111">When you install Exchange 2013, a self-signed certificate with the name Microsoft Exchange Server Auth Certificate is created for you.</span></span> <span data-ttu-id="309f6-112">Этот сертификат, который можно найти в хранилище сертификатов локального компьютера, должен использоваться для проверки подлинности серверов на сервере Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="309f6-112">This certificate, which can be found in the local computer certificate store, should be used for server-to-server authentication on Exchange 2013.</span></span> <span data-ttu-id="309f6-113">Сведения о назначении сертификатов в Exchange 2013 можно найти в разделе "Настройка потока обработки почты и доступа клиентов" [https://go.microsoft.com/fwlink/p/?LinkId=268540](https://go.microsoft.com/fwlink/p/?linkid=268540) .</span><span class="sxs-lookup"><span data-stu-id="309f6-113">For details about assigning certificates in Exchange 2013, see "Configure Mail Flow and Client Access" at [https://go.microsoft.com/fwlink/p/?LinkId=268540](https://go.microsoft.com/fwlink/p/?linkid=268540).</span></span>

<span data-ttu-id="309f6-114">Для Lync Server 2013 вы можете использовать существующий сертификат сервера Lync Server в качестве сертификата для проверки подлинности сервера. Например, сертификат по умолчанию также можно использовать в качестве сертификата OAuthTokenIssuer.</span><span class="sxs-lookup"><span data-stu-id="309f6-114">For Lync Server 2013 you can use an existing Lync Server certificate as your server-to-server authentication certificate; for example, your default certificate can also be used as the OAuthTokenIssuer certificate.</span></span> <span data-ttu-id="309f6-115">Lync Server 2013 позволяет использовать любой сертификат веб-сервера в качестве сертификата для проверки подлинности серверов и серверов, если:</span><span class="sxs-lookup"><span data-stu-id="309f6-115">Lync Server 2013 allows you to use any Web server certificate as the certificate for server-to-server authentication provided that:</span></span>

  - <span data-ttu-id="309f6-116">этот сертификат содержит имя домена SIP в поле "Тема";</span><span class="sxs-lookup"><span data-stu-id="309f6-116">The certificate includes the name of your SIP domain in the Subject field.</span></span>

  - <span data-ttu-id="309f6-117">тот же сертификат настроен как сертификат OAuthTokenIssuer на всех интерфейсных серверах;</span><span class="sxs-lookup"><span data-stu-id="309f6-117">The same certificate is configured as the OAuthTokenIssuer certificate on all of your Front End Servers.</span></span>

  - <span data-ttu-id="309f6-118">длина сертификата составляет не менее 2048 бит.</span><span class="sxs-lookup"><span data-stu-id="309f6-118">The certificate has a length of at least 2048 bits.</span></span>

<span data-ttu-id="309f6-119">Подробнее о сертификатах проверки подлинности серверов для Microsoft Lync Server 2013: [назначение сертификата проверки подлинности серверов и серверов для Microsoft Lync server 2013](lync-server-2013-assigning-a-server-to-server-authentication-certificate-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="309f6-119">For details about server-to-server authentication certificates for Microsoft Lync Server 2013, see [Assigning a server-to-server authentication certificate to Microsoft Lync Server 2013](lync-server-2013-assigning-a-server-to-server-authentication-certificate-to-lync-server-2013.md).</span></span>

<span data-ttu-id="309f6-120">После назначения сертификатов необходимо настроить службу автообнаружения в Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="309f6-120">After the certificates have been assigned you must then configure the autodiscover service on Exchange 2013.</span></span> <span data-ttu-id="309f6-121">В Exchange 2013 служба автообнаружения настраивает профили пользователей и предоставляет доступ к службам Exchange при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="309f6-121">In Exchange 2013, the autodiscover service configures user profiles and provides access to Exchange services when users log on to the system.</span></span> <span data-ttu-id="309f6-122">Пользователи предоставляют службе автообнаружения свой адрес электронной почты и пароль; в свою очередь службы предоставляют пользователям следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="309f6-122">Users present the autodiscover service with their email address and password; in turn, the services provide the user with information such as:</span></span>

  - <span data-ttu-id="309f6-123">Сведения о соединении как внутренних, так и внешних подключений к Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="309f6-123">Connection information for both internal and external connectivity to Exchange 2013.</span></span>

  - <span data-ttu-id="309f6-124">расположение сервера почтовых ящиков пользователя;</span><span class="sxs-lookup"><span data-stu-id="309f6-124">The location of the user’s Mailbox server.</span></span>

  - <span data-ttu-id="309f6-125">URL-адреса для компонентов Outlook, таких как сведения о доступности, единой системе обмена сообщениями, а также автономной адресной книге;</span><span class="sxs-lookup"><span data-stu-id="309f6-125">URLs for Outlook features such as free/busy information, Unified Messaging, and the offline address book.</span></span>

  - <span data-ttu-id="309f6-126">параметры сервера мобильного Outlook.</span><span class="sxs-lookup"><span data-stu-id="309f6-126">Outlook Anywhere server settings.</span></span>

<span data-ttu-id="309f6-127">Для интеграции Lync Server 2013 и Exchange 2013 необходимо настроить службу автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="309f6-127">The autodiscover service must be configured before you can integrate Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="309f6-128">Вы можете проверить, настроена ли служба автообнаружения, выполнив следующую команду в командной консоли Exchange и установив значение свойства AutoDiscoverServiceInternalUri:</span><span class="sxs-lookup"><span data-stu-id="309f6-128">You can verify whether or not the autodiscover service has been configured by running the following command from the Exchange Management Shell and checking the value of the AutoDiscoverServiceInternalUri property:</span></span>

    Get-ClientAccessServer | Select-Object Name, AutoDiscoverServiceInternalUri | Format-List

<span data-ttu-id="309f6-p106">Если это значение пусто, необходимо назначить URI службе автообнаружения. Обычно этот URI выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="309f6-p106">If this value is blank, you must assign a URI to the autodiscover service. Typically this URI will look similar to this:</span></span>

    https://autodiscover.litwareinc.com/autodiscover/autodiscover.xml

<span data-ttu-id="309f6-131">URI автообнаружения можно назначить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="309f6-131">You can assign the autodiscover URI by running a command similar to this:</span></span>

    Get-ClientAccessServer | Set-ClientAccessServer -AutoDiscoverServiceInternalUri "https://autodiscover.litwareinc.com/autodiscover/autodiscover.xml"

<span data-ttu-id="309f6-132">Подробные сведения о службе автообнаружения можно найти в разделе Общие сведения о службе автообнаружения [https://go.microsoft.com/fwlink/p/?LinkId=268542](https://go.microsoft.com/fwlink/p/?linkid=268542) .</span><span class="sxs-lookup"><span data-stu-id="309f6-132">For details about the autodiscover service, see "Understanding the Autodiscover Service" at [https://go.microsoft.com/fwlink/p/?LinkId=268542](https://go.microsoft.com/fwlink/p/?linkid=268542).</span></span>

<span data-ttu-id="309f6-133">После настройки службы автообнаружения необходимо изменить параметры конфигурации OAuth сервера Lync. Это гарантирует, что Lync Server знает, где найти службу автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="309f6-133">After the autodiscover service has been configured you must then modify the Lync Server OAuth configuration settings; this ensures that Lync Server knows where to find the autodiscover service.</span></span> <span data-ttu-id="309f6-134">Чтобы изменить параметры конфигурации OAuth в Lync Server 2013, выполните следующую команду в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="309f6-134">To modify the OAuth configuration settings in Lync Server 2013, run the following command from within the Lync Server Management Shell.</span></span> <span data-ttu-id="309f6-135">При выполнении этой команды убедитесь, что вы указали универсальный код ресурса (URI) для службы автообнаружения, запущенной на сервере Exchange, и что вы используете функцию **автообнаружения. svc** для указания расположения службы вместо **autodiscover.xml** (указывающего на XML-файл, используемый службой):</span><span class="sxs-lookup"><span data-stu-id="309f6-135">When running this command, be sure that you specify the URI to the autodiscover service running on your Exchange server, and that you use **autodiscover.svc** to point to the service location instead of **autodiscover.xml** (which points to the XML file used by the service):</span></span>

    Set-CsOAuthConfiguration -Identity global -ExchangeAutodiscoverUrl "https://autodiscover.litwareinc.com/autodiscover/autodiscover.svc"

<div>


> [!NOTE]  
> <span data-ttu-id="309f6-136">Параметр Identity в предыдущей команде является необязательным; Это связано с тем, что Lync Server позволяет только использовать единственную глобальную коллекцию параметров конфигурации OAuth.</span><span class="sxs-lookup"><span data-stu-id="309f6-136">The Identity parameter in the preceding command is optional; that's because Lync Server only allows you to have a single, global collection of OAuth configuration settings.</span></span> <span data-ttu-id="309f6-137">Помимо прочего, это означает, что вы можете настроить URL-адрес автообнаружения, используя это немного более простую команду:</span><span class="sxs-lookup"><span data-stu-id="309f6-137">Among other things, that means that you can configure the autodiscover URL by using this slightly-simpler command:</span></span><BR><span data-ttu-id="309f6-138">Set-CsOAuthConfiguration – ExchangeAutodiscoverUrl " https://autodiscover.litwareinc.com/autodiscover/autodiscover.svc "</span><span class="sxs-lookup"><span data-stu-id="309f6-138">Set-CsOAuthConfiguration–ExchangeAutodiscoverUrl "https://autodiscover.litwareinc.com/autodiscover/autodiscover.svc"</span></span><BR><span data-ttu-id="309f6-p109">Если вы не знакомы с этой технологией, OAuth — это стандартный протокол авторизации, который применяется на различных крупных веб-сайтах. При использовании OAuth учетные данные и пароли пользователей не переносятся с одного компьютера на другой. Вместо этого проверка подлинности и авторизация основаны на обмене маркерами безопасности, которые предоставляют доступ к определенному набору ресурсов в течение определенного промежутка времени.</span><span class="sxs-lookup"><span data-stu-id="309f6-p109">If you are unfamiliar with the technology, OAuth is a standard authorization protocol used by a number of major websites. With OAuth, user credentials and passwords are not passed from one computer to another. Instead, authentication and authorization is based on the exchange of security tokens; these tokens grant access to a specific set of resources for a specific amount of time.</span></span>



</div>

<span data-ttu-id="309f6-142">Помимо настройки службы автообнаружения, необходимо также создать DNS-запись для службы, указывающей на сервер Exchange.</span><span class="sxs-lookup"><span data-stu-id="309f6-142">In addition to configuring the autodiscover service, you must also create a DNS record for the service that points to your Exchange server.</span></span> <span data-ttu-id="309f6-143">Например, если служба автообнаружения находится на autodiscover.litwareinc.com, вам потребуется создать запись DNS для autodiscover.litwareinc.com, которая разрешается в полное доменное имя сервера Exchange (например, atl-exchange-001.litwareinc.com).</span><span class="sxs-lookup"><span data-stu-id="309f6-143">For example, if your autodiscover service is located at autodiscover.litwareinc.com you will need to create a DNS record for autodiscover.litwareinc.com that resolves to the fully qualified domain name of your Exchange server (for example, atl-exchange-001.litwareinc.com).</span></span>

<span data-ttu-id="309f6-144"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="309f6-144"></div>

<span> </span>

</div>

</div>

</span></span></div>

