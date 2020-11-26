---
title: Назначение сертификата проверки подлинности серверов на сервер Lync Server 2013
description: Назначение сертификата проверки подлинности серверов на сервер Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning a server-to-server authentication certificate to Microsoft Lync Server 2013
ms:assetid: c7413954-2504-47f4-a073-44548aff1c0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205253(v=OCS.15)
ms:contentKeyID: 48185367
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 042158167f89dc2b6e743e8db94149d4f1cbc1a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438325"
---
# <a name="assigning-a-server-to-server-authentication-certificate-to-microsoft-lync-server-2013"></a><span data-ttu-id="31541-103">Назначение сертификата проверки подлинности сервера серверу Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31541-103">Assigning a server-to-server authentication certificate to Microsoft Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31541-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31541-104">

<span> </span></span></span>

<span data-ttu-id="31541-105">_**Тема последнего изменения:** 2013-10-24_</span><span class="sxs-lookup"><span data-stu-id="31541-105">_**Topic Last Modified:** 2013-10-24_</span></span>

<span data-ttu-id="31541-106">Чтобы определить, назначен ли сертификат проверки подлинности "сервер-сервер" для Microsoft Lync Server 2013, выполните следующую команду в командной консоли Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="31541-106">To determine whether or not a server-to-server authentication certificate has already been assigned to Microsoft Lync Server 2013, run the following command from the Lync Server 2013 Management Shell:</span></span>

    Get-CsCertificate -Type OAuthTokenIssuer

<span data-ttu-id="31541-107">Если сведения о сертификате не возвращаются, для проверки подлинности между серверами необходимо сначала назначить сертификат издателя маркеров.</span><span class="sxs-lookup"><span data-stu-id="31541-107">If no certificate information is returned you must assign a token issuer certificate before you can use server-to-server authentication.</span></span> <span data-ttu-id="31541-108">Как правило, любой сертификат Lync Server 2013 можно использовать в качестве сертификата OAuthTokenIssuer; Например, вы также можете использовать сертификат по умолчанию Lync Server 2013 в качестве сертификата OAuthTokenIssuer.</span><span class="sxs-lookup"><span data-stu-id="31541-108">As a general rule, any Lync Server 2013 certificate can be used as your OAuthTokenIssuer certificate; for example, your Lync Server 2013 default certificate can also be used as the OAuthTokenIssuer certificate.</span></span> <span data-ttu-id="31541-109">(Сертификат OAUthTokenIssuer также может представлять собой любой сертификат веб-сервера, включающий имя вашего домена SIP в поле субъекта.) Ниже указаны основные требования к сертификату, используемому для проверки подлинности серверов и сервера: 1) один и тот же сертификат должен быть настроен как сертификат OAuthTokenIssuer на всех серверах переднего плана; и 2) сертификат должен составлять не менее 2048 бит.</span><span class="sxs-lookup"><span data-stu-id="31541-109">(The OAUthTokenIssuer certificate can also be any Web server certificate that includes the name of your SIP domain in the Subject field.) The primary two requirements for the certificate used for server-to-server authentication are these: 1)the same certificate must be configured as the OAuthTokenIssuer certificate on all of your Front End Servers; and, 2) the certificate must be at least 2048 bits.</span></span>

<span data-ttu-id="31541-110">При отсутствии сертификата, позволяющего проверять подлинность между серверами, можно получить новый сертификат, импортировать его и затем применять для проверки подлинности между серверами.</span><span class="sxs-lookup"><span data-stu-id="31541-110">If you do not have a certificate that can be used for server-to-server authentication you can obtain a new certificate, import the new certificate, and then use that certificate for server-to-server authentication.</span></span> <span data-ttu-id="31541-111">После запроса и получения нового сертификата вы можете войти на любой из своих серверов переднего плана и с помощью команды Windows PowerShell, аналогичной этой, для импорта и назначения этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="31541-111">After you have requested and obtained the new certificate you can then log on to any one of your Front End Servers and use a Windows PowerShell command similar to this one to import and assign that certificate:</span></span>

    Import-CsCertificate -Identity global -Type OAuthTokenIssuer -Path C:\Certificates\ServerToServerAuth.pfx  -Password "P@ssw0rd"

<span data-ttu-id="31541-112">В предыдущей команде параметр Path представляет полный путь к файлу сертификата, а параметр Password – пароль, назначенный сертификату.</span><span class="sxs-lookup"><span data-stu-id="31541-112">In the preceding command the Path parameter represents the full path to the certificate file, and the Password parameter represents the password that was assigned to the certificate.</span></span> <span data-ttu-id="31541-113">Эту процедуру необходимо выполнить только один раз: служба репликации Lync Server автоматически создаст набор запланированных задач, которые будут расшифровывать и развертывать сертификат на всех серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31541-113">This procedure should be run just one time: Lync Server's replication service will then automatically create a set of scheduled tasks that will decrypt and deploy the certificate to all your Front End Servers.</span></span>

<span data-ttu-id="31541-114">Можно также задать в качестве сертификата проверки подлинности между серверами существующий сертификат.</span><span class="sxs-lookup"><span data-stu-id="31541-114">Alternatively, you can use an existing certificate as your server-to-server authentication certificate.</span></span> <span data-ttu-id="31541-115">(Как отмечено, сертификат по умолчанию можно использовать в качестве сертификата для проверки подлинности сервера и сервера.) В следующей паре команд Windows PowerShell извлекается значение свойства Thumbprint сертификата по умолчанию, а затем используйте это значение, чтобы сделать сертификат по умолчанию сертификатом проверки подлинности сервера и сервера.</span><span class="sxs-lookup"><span data-stu-id="31541-115">(As noted, the default certificate can be used as the server-to-server authentication certificate.) The following pair of Windows PowerShell commands retrieve the value of the default certificate's Thumbprint property, then use that value to make the default certificate the server-to-server authentication certificate:</span></span>

    $x = (Get-CsCertificate -Type Default).Thumbprint
    Set-CsCertificate -Identity global -Type OAuthTokenIssuer -Thumbprint $x

<span data-ttu-id="31541-116">В предыдущей команде полученный сертификат настроен для функционирования глобального сертификата проверки подлинности серверов и серверов; Это означает, что сертификат будет реплицирован и использоваться всеми серверами переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31541-116">In the preceding command, the retrieved certificate is configured to function as the global server-to-server authentication certificate; that means that the certificate will be replicated to, and used by, all your Front End Servers.</span></span> <span data-ttu-id="31541-117">Эту команду можно выполнить только один раз и только на одном из ваших серверов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31541-117">Again, this command should only be run one time, and only on one of your Front End Servers.</span></span> <span data-ttu-id="31541-118">Несмотря на то, что все серверы переднего плана должны использовать один и тот же сертификат, не следует настраивать сертификат OAuthTokenIssuer на каждом сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31541-118">Although all Front End Servers must use the same certificate, you should not configure the OAuthTokenIssuer certificate on each Front End Server.</span></span> <span data-ttu-id="31541-119">Вместо этого настройте сертификат один раз, а затем разрешите серверу репликации Lync Server скопировать этот сертификат на каждый сервер.</span><span class="sxs-lookup"><span data-stu-id="31541-119">Instead, configure the certificate once, then let Lync Server's replication server take care of copying that certificate to each server.</span></span>

<span data-ttu-id="31541-120">Командлет Set-CsCertificate берет на вопрос сертификат и сразу же настраивает этот сертификат для использования в качестве текущего сертификата OAuthTokenIssuer.</span><span class="sxs-lookup"><span data-stu-id="31541-120">The Set-CsCertificate cmdlet takes the certificate in question and immediately configures that certificate to act as the current OAuthTokenIssuer certificate.</span></span> <span data-ttu-id="31541-121">(Lync Server 2013 хранит две копии типа сертификата: текущий сертификат и предыдущий сертификат). Если вы хотите, чтобы новый сертификат сразу же начал действовать в качестве сертификата OAuthTokenIssuer, следует использовать командлет Set-CsCertificate.</span><span class="sxs-lookup"><span data-stu-id="31541-121">(Lync Server 2013 keeps two copies of a certificate type: the current certificate and the previous certificate.) If you need the new certificate to immediately begin to act as the OAuthTokenIssuer certificate then you should use the Set-CsCertificate cmdlet.</span></span>

<span data-ttu-id="31541-122">Можно также воспользоваться командлетом Set-CsCertificate, чтобы "накатить" новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="31541-122">You can also use the Set-CsCertificate cmdlet to "roll" a new certificate.</span></span> <span data-ttu-id="31541-123">"Накат" означает, что новый сертификат станет текущим сертификатом OAuthTokenIssuer в некоторый определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="31541-123">"Rolling" a certificate simply means that you configure a new certificate to become the current OAuthTokenIssuer certificate at a specified point in time.</span></span> <span data-ttu-id="31541-124">Например, эта команда извлекает сертификат по умолчанию, а затем настраивает этот сертификат для использования в качестве текущего сертификата OAuthTokenIssuer на 1 июля 2012 г.:</span><span class="sxs-lookup"><span data-stu-id="31541-124">For example, this command retrieves the default certificate and then configure that certificate to take over as the current OAuthTokenIssuer certificate as of July 1, 2012:</span></span>

    $x = (Get-CsCertificate -Type Default).Thumbprint
    Set-CsCertificate -Identity global -Type OAuthTokenIssuer -Thumbprint $x -EffectiveDate "7/1/2012" -Roll

<span data-ttu-id="31541-125">На 1 июля 2012 новый сертификат будет настроен в качестве текущего сертификата OAuthTokenIssuer и сертификат OAuthTokenIssuer "старый" будет настроен как предыдущий сертификат.</span><span class="sxs-lookup"><span data-stu-id="31541-125">On July 1, 2012 the new certificate will be configured as the current OAuthTokenIssuer certificate and the "old" OAuthTokenIssuer certificate will be configured as the previous certificate.</span></span>

<span data-ttu-id="31541-126">Если вы не хотите использовать Windows PowerShell, вы также можете экспортировать сертификат с первого сервера переднего плана с помощью консоли MMC "сертификаты", а затем импортировать этот же сертификат на все другие серверы переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31541-126">If you do not want to use Windows PowerShell you can also use the Certificates MMC console to export a certificate from one Front End Server and then import that same certificate on all your other Front End Servers.</span></span> <span data-ttu-id="31541-127">При этом вместе с сертификатом необходимо экспортировать закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="31541-127">If you do this, make sure that you export the private key along with the certificate itself.</span></span>

<div>


> [!WARNING]
> <span data-ttu-id="31541-128">В этом случае процедура должна выполняться на каждом сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31541-128">In this case, the procedure must be performed on each Front End Server.</span></span> <span data-ttu-id="31541-129">При экспорте и импорте сертификатов таким образом, Lync Server 2013 не будет реплицировать этот сертификат на каждый сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="31541-129">When exporting and importing certificates in this manner Lync Server 2013 will not replicate that certificate to each Front End Server.</span></span>



</div>

<span data-ttu-id="31541-130">После импорта сертификата на все серверы переднего плана этот сертификат может быть назначен с помощью мастера развертывания Lync Server, а не Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31541-130">After the certificate has been imported to all your Front End Servers, that certificate can then be assigned by using the Lync Server Deployment Wizard instead of Windows PowerShell.</span></span> <span data-ttu-id="31541-131">Для назначения сертификата с помощью мастера развертывания выполните следующие действия на компьютере, где установлен мастер развертывания.</span><span class="sxs-lookup"><span data-stu-id="31541-131">To assign a certificate by using the Deployment Wizard, complete the following steps on a computer where the Deployment Wizard has been installed:</span></span>

1.  <span data-ttu-id="31541-132">Нажмите кнопку Пуск, выберите все программы, а затем — **Microsoft Lync server 2013**, а затем — **Мастер развертывания Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="31541-132">Click Start, click All Programs, click **Microsoft Lync Server 2013**, and then click **Lync Server Deployment Wizard**.</span></span>

2.  <span data-ttu-id="31541-133">В мастере развертывания нажмите кнопку **Установка или обновление системы Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="31541-133">In the Deployment Wizard, click **Install or Update Lync Server System**.</span></span>

3.  <span data-ttu-id="31541-134">На странице Microsoft Lync Server 2013 нажмите кнопку **выполнить** под заголовком **Шаг 3: запрос, установка и назначение сертификатов**.</span><span class="sxs-lookup"><span data-stu-id="31541-134">On the Microsoft Lync Server 2013 page, click the **Run** button under the heading **Step 3: Request, Install or Assign Certificates**.</span></span> <span data-ttu-id="31541-135">(Примечание. Если вы уже установили сертификаты на этом компьютере, нажмите кнопку " **выполнить** ", чтобы пометить **ее.)**</span><span class="sxs-lookup"><span data-stu-id="31541-135">(Note: If you have already installed certificates on this computer then the **Run** button will be labeled **Run Again**.)</span></span>

4.  <span data-ttu-id="31541-136">В мастере сертификатов выберите сертификат **OAuthTokenIssuer**, затем нажмите кнопку **Назначить**.</span><span class="sxs-lookup"><span data-stu-id="31541-136">In the Certificate Wizard, select the **OAuthTokenIssuer** certificate and then click **Assign**.</span></span>

5.  <span data-ttu-id="31541-137">В мастере назначения сертификатов на странице **Назначение сертификатов** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="31541-137">In the Certificate Assignment wizard, on the **Certificate Assignment** page, click **Next**.</span></span>

6.  <span data-ttu-id="31541-138">На странице **Хранилище сертификатов** выберите сертификат для применения при проверке подлинности между серверами, затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="31541-138">On the **Certificate Store** page, select the certificate to be used for server-to-server authentication and then click **Next**.</span></span>

7.  <span data-ttu-id="31541-139">На странице "Сводка по назначениям сертификатов" нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="31541-139">On the Certificate Assignment Summary page, click **Next**.</span></span>

8.  <span data-ttu-id="31541-140">На странице "Выполнение команд" нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="31541-140">On the Executing Commands page, click **Finish**.</span></span>

9.  <span data-ttu-id="31541-141">Закройте мастер сертификатов и мастер развертывания.</span><span class="sxs-lookup"><span data-stu-id="31541-141">Close the Certificate Wizard and the Deployment Wizard.</span></span>

<span data-ttu-id="31541-142"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31541-142"></div>

<span> </span>

</div>

</div>

</span></span></div>

