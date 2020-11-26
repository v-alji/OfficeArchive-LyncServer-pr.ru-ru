---
title: Промежуточное хранение и сертификаты OAuth с использованием Set-CsCertificate
description: Выведите на экран набор сертификатов AV и OAuth с помощью Set-CsCertificate.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Staging AV and OAuth certificates using -Roll in Set-CsCertificate
ms:assetid: 22dec3cc-4b6b-4df2-b269-5b35df4731a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ660292(v=OCS.15)
ms:contentKeyID: 49354387
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3732c4adb4327cc1e4111307ab2d72ed080cf221
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423779"
---
# <a name="staging-av-and-oauth-certificates-in-lync-server-2013-using--roll-in-set-cscertificate"></a><span data-ttu-id="86fae-103">Промежуточное хранение и сертификаты OAuth в Lync Server 2013 с помощью Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="86fae-103">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86fae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86fae-104">

<span> </span></span></span>

<span data-ttu-id="86fae-105">_**Тема последнего изменения:** 2012-11-13_</span><span class="sxs-lookup"><span data-stu-id="86fae-105">_**Topic Last Modified:** 2012-11-13_</span></span>

<span data-ttu-id="86fae-106">Аудио-и видеосвязь (A/V) — это ключевой компонент Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86fae-106">Audio/Video (A/V) communications is a key component of Microsoft Lync Server 2013.</span></span> <span data-ttu-id="86fae-107">Такие функции, как общий доступ к приложениям, а также аудио-и видеоконференции, основываются на сертификатах, назначенных службе EDGE (a/V), а именно службе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="86fae-107">Features such as application sharing and audio and video conferencing rely on the certificates assigned to the A/V Edge service, specifically the A/V Authentication service.</span></span>

<div>


> [!IMPORTANT]
> <OL>
> <LI>
> <P><span data-ttu-id="86fae-108">Эта новая функция разработана для работы со службой EDGE (A/V) и сертификатом <EM>OAuthTokenIssuer</EM> .</span><span class="sxs-lookup"><span data-stu-id="86fae-108">This new feature is designed to work for the A/V Edge service and the <EM>OAuthTokenIssuer</EM> certificate.</span></span> <span data-ttu-id="86fae-109">Другие типы сертификатов могут быть предоставлены вместе со службой EDGE (A/V) и типом сертификата OAuth, но это не выгодно из-за сосуществования сертификата службы Edge.</span><span class="sxs-lookup"><span data-stu-id="86fae-109">Other certificate types can be provisioned along with the A/V Edge service and OAuth certificate type, but will not benefit from the coexistence behavior that the A/V Edge service certificate will.</span></span></P>
> <LI>
> <P><span data-ttu-id="86fae-110">Командлеты PowerShell среды управления сервером Lync Server, используемые для управления сертификатами Microsoft Lync Server 2013, относятся к сертификату службы EDGE в качестве типа сертификата <EM>AudioVideoAuthentication</EM> и сертификата OAuthServer в качестве типа <EM>OAuthTokenIssuer</EM>.</span><span class="sxs-lookup"><span data-stu-id="86fae-110">The Lync Server Management Shell PowerShell cmdlets used to manage Microsoft Lync Server 2013 certificates refers to the A/V Edge service certificate as the <EM>AudioVideoAuthentication</EM> certificate type and the OAuthServer certificate as type <EM>OAuthTokenIssuer</EM>.</span></span> <span data-ttu-id="86fae-111">В оставшейся части этого раздела и однозначном определении сертификатов они будут обращаться к одному и тому же идентификатору, <EM>AudioVideoAuthentication</EM> и <EM>OAuthTokenIssuer</EM>.</span><span class="sxs-lookup"><span data-stu-id="86fae-111">For the rest of this topic and to uniquely identify the certificates, they will be referred to by the same identifier type, <EM>AudioVideoAuthentication</EM> and <EM>OAuthTokenIssuer</EM>.</span></span></P></LI></OL>



</div>

<span data-ttu-id="86fae-112">Служба проверки подлинности A/V отвечает за выдачу маркеров, используемых клиентами и другими пользователями/V.</span><span class="sxs-lookup"><span data-stu-id="86fae-112">The A/V Authentication service is responsible for issuing tokens that are used by clients and other A/V consumers.</span></span> <span data-ttu-id="86fae-113">Маркеры генерируются из атрибутов сертификата, и при истечении срока действия сертификата теряется соединение и требование для повторного присоединения с новым маркером, созданным новым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="86fae-113">The tokens are generated from attributes on the certificate, and when the certificate expires, loss of connection and requirement to rejoin with a new token generated by the new certificate will result.</span></span> <span data-ttu-id="86fae-114">Новая функция в Lync Server 2013 поможет решить эту проблему — возможность размещения нового сертификата в начале срока действия старого, и предоставление обоих сертификатов для продолжения работы в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="86fae-114">A new feature in Lync Server 2013 will alleviate this problem – the ability to stage a new certificate in advance of the old one expiring and allowing both certificates to continue to function for a period of time.</span></span> <span data-ttu-id="86fae-115">Эта функция использует обновленные функции в командлете Set-CsCertificate Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="86fae-115">This feature uses updated functionality in the Set-CsCertificate Lync Server Management Shell cmdlet.</span></span> <span data-ttu-id="86fae-116">Новый параметр — рулон с существующим параметром — EffectiveDate будет размещать новый сертификат AudioVideoAuthentication в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="86fae-116">The new parameter –Roll, with the existing parameter –EffectiveDate, will place the new AudioVideoAuthentication certificate in the certificate store.</span></span> <span data-ttu-id="86fae-117">Старый сертификат AudioVideoAuthentication останется для проверки выпущенных маркеров.</span><span class="sxs-lookup"><span data-stu-id="86fae-117">The older AudioVideoAuthentication certificate will still remain for issued tokens to be validated against.</span></span> <span data-ttu-id="86fae-118">Начиная с размещения нового сертификата AudioVideoAuthentication, произойдет следующая серия событий:</span><span class="sxs-lookup"><span data-stu-id="86fae-118">Beginning with putting the new AudioVideoAuthentication certificate in place, the following series of events will occur:</span></span>

<div>


> [!TIP]
> <span data-ttu-id="86fae-119">С помощью командлетов командной консоли Lync Server для управления сертификатами вы можете запросить отдельные и разные сертификаты для каждой цели на пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="86fae-119">Using the Lync Server Management Shell cmdlets for managing certificates, you can request separate and distinct certificates for each purpose on the Edge Server.</span></span> <span data-ttu-id="86fae-120">Использование мастера сертификатов в мастере развертывания Lync Server помогает создавать сертификаты, но обычно имеет тип <STRONG>по умолчанию</STRONG> , который прикрепляет все сертификаты для пограничного сервера к одному сертификату.</span><span class="sxs-lookup"><span data-stu-id="86fae-120">Using the Certificate Wizard in the Lync Server Deployment Wizard assists you in creating certificates, but is typically of the <STRONG>default</STRONG> type which couples all certificate uses for the Edge Server onto a single certificate.</span></span> <span data-ttu-id="86fae-121">Если вы собираетесь использовать функцию межсертификатного сертификата, рекомендуется отключать сертификат AudioVideoAuthentication из других целей сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-121">The recommended practice if you are going to use the rolling certificate feature is to decouple the AudioVideoAuthentication certificate from the other certificate purposes.</span></span> <span data-ttu-id="86fae-122">Вы можете подготавливать сертификат по умолчанию и пополнить его, но только часть AudioVideoAuthentication комбинированного сертификата будет полезна при выуровне.</span><span class="sxs-lookup"><span data-stu-id="86fae-122">You can provision and stage a certificate of the Default type, but only the AudioVideoAuthentication portion of the combined certificate will benefit from the staging.</span></span> <span data-ttu-id="86fae-123">Если при истечении срока действия сертификата пользователь приходил к разговору (например), вам потребуется выйти из системы и снова войти в систему, чтобы использовать новый сертификат, связанный с службой Edge Access.</span><span class="sxs-lookup"><span data-stu-id="86fae-123">A user involved in (for example) an instant messaging conversation when the certificate expires will need to log out and log back in to make use of the new certificate associated with the Access Edge service.</span></span> <span data-ttu-id="86fae-124">Аналогичное поведение может возникнуть для пользователя, участвующего в веб-конференции с помощью службы Edge для веб-конференций.</span><span class="sxs-lookup"><span data-stu-id="86fae-124">Similar behavior will occur for a user involved in a Web conference using the Web Conferencing Edge service.</span></span> <span data-ttu-id="86fae-125">Сертификат OAuthTokenIssuer — это конкретный тип, который является общим для всех серверов.</span><span class="sxs-lookup"><span data-stu-id="86fae-125">The OAuthTokenIssuer certificate is a specific type that is shared across all servers.</span></span> <span data-ttu-id="86fae-126">Вы создаете сертификат и управляете им в одном расположении, и сертификат хранится в хранилище Центрального управления для всех остальных серверов.</span><span class="sxs-lookup"><span data-stu-id="86fae-126">You create and manage the certificate in one place and the certificate is stored in the Central Management store for all other servers.</span></span>



</div>

<span data-ttu-id="86fae-127">Дополнительные сведения необходимы для полного понимания параметров и требований при использовании командлета Set-CsCertificate и его использования для размещения сертификатов до истечения срока действия текущего сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-127">Additional detail is needed to fully understand your options and requirements when using the Set-CsCertificate cmdlet and using it to stage certificates prior to the current certificate expiring.</span></span> <span data-ttu-id="86fae-128">Параметр-рулон важен, но фактически является единственной целью.</span><span class="sxs-lookup"><span data-stu-id="86fae-128">The –Roll parameter is important, but essentially single purpose.</span></span> <span data-ttu-id="86fae-129">Если вы задаете его в качестве параметра, вы указываете Set-CsCertificate, что вы будете предоставлять сведения о сертификате, который будет зависеть от-Type (например, AudioVideoAuthentication и OAuthTokenIssuer), когда сертификат станет эффективнее, определяемым на – EffectiveDate.</span><span class="sxs-lookup"><span data-stu-id="86fae-129">If you define it as a parameter, you are telling Set-CsCertificate that you will be providing information about the certificate that will be affected defined by –Type (for example AudioVideoAuthentication and OAuthTokenIssuer), when the certificate will become effective defined by –EffectiveDate.</span></span>

<span data-ttu-id="86fae-130">**-Сведение:** Параметр – рулон является обязательным и имеет зависимости, которые должны быть предоставлены вместе с ним.</span><span class="sxs-lookup"><span data-stu-id="86fae-130">**-Roll:** The –Roll parameter is required and has dependencies that must be supplied along with it.</span></span> <span data-ttu-id="86fae-131">Обязательные параметры, позволяющие полностью определить, какие сертификаты будут затронуты и как они будут применены.</span><span class="sxs-lookup"><span data-stu-id="86fae-131">Required parameters to fully define which certificates will be affected and how they will be applied:</span></span>

<span data-ttu-id="86fae-132">**-EffectiveDate:** Параметр — EffectiveDate определяет, когда новый сертификат становится совместен с текущим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="86fae-132">**-EffectiveDate:** The parameter –EffectiveDate defines when the new certificate will become co-active with the current certificate.</span></span> <span data-ttu-id="86fae-133">Приложение – EffectiveDate может быть близко к сроку действия текущего сертификата или может быть больше времени.</span><span class="sxs-lookup"><span data-stu-id="86fae-133">The –EffectiveDate can be close to the expiry time of the current certificate, or it can be a longer period of time.</span></span> <span data-ttu-id="86fae-134">Рекомендуемый минимум — EffectiveDate для сертификата AudioVideoAuthentication — это 8 часов, который является временем жизни токенов, выпущенных по умолчанию для маркеров служебной программы ребра EDGE, выданных с помощью сертификата AudioVideoAuthentication.</span><span class="sxs-lookup"><span data-stu-id="86fae-134">A recommended minimum –EffectiveDate for the AudioVideoAuthentication certificate would be 8 hours, which is the default token lifetime for AV Edge service tokens issued using the AudioVideoAuthentication certificate.</span></span>

<span data-ttu-id="86fae-135">При использовании промежуточных сертификатов OAuthTokenIssuer для времени опережения могут быть разные требования, прежде чем сертификат станет эффективнее.</span><span class="sxs-lookup"><span data-stu-id="86fae-135">When staging OAuthTokenIssuer certificates, there are different requirements for the lead time before the certificate can become effective.</span></span> <span data-ttu-id="86fae-136">Минимальное время, в течение которого должен быть сертификат OAuthTokenIssuer для своего периода ожидания, составляет 24 часа до окончания срока действия текущего сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-136">The minimum time that the OAuthTokenIssuer certificate should have for its lead time is 24 hours before the expiration time of the current certificate.</span></span> <span data-ttu-id="86fae-137">Расширенное время упреждения для сосуществования связано с тем, что в связи с другими ролями сервера, которые зависят от сертификата OAuthTokenIssuer (например, Exchange Server), которое имеет более длительное время хранения для сертификата, созданного для проверки подлинности и ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="86fae-137">The extended lead time for the coexistence is because of other server roles that are dependent on the OAuthTokenIssuer certificate (Exchange Server, for example) which has a longer retention time for certificate created authentication and encryption key materials.</span></span>

<span data-ttu-id="86fae-138">**-Отпечаток:** Отпечаток — это атрибут сертификата, уникальный для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-138">**-Thumbprint:** The thumbprint is an attribute on the certificate that is unique to that certificate.</span></span> <span data-ttu-id="86fae-139">Параметр – Thumbprint используется для идентификации сертификата, который повлияет на действия, выполняемые командлетом Set-CsCertificate.</span><span class="sxs-lookup"><span data-stu-id="86fae-139">The –Thumbprint parameter is used to identify the certificate that will be affected by the actions of the Set-CsCertificate cmdlet.</span></span>

<span data-ttu-id="86fae-140">**-Type (тип):** Параметр – Type может использовать один тип использования сертификата или список типов использования сертификатов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="86fae-140">**-Type:** The –Type parameter can accept a single certificate usage type or a comma separated list of certificate usage types.</span></span> <span data-ttu-id="86fae-141">Типы сертификатов — это те, которые определяют для командлета и сервера назначение сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-141">The certificate types are those that identify to the cmdlet and to the server what the purpose of the certificate is.</span></span> <span data-ttu-id="86fae-142">Например, введите AudioVideoAuthentication для использования службой Edge/V и службой проверки подлинности AV.</span><span class="sxs-lookup"><span data-stu-id="86fae-142">For example, type AudioVideoAuthentication is for use by the A/V Edge service and the AV Authentication service.</span></span> <span data-ttu-id="86fae-143">Если вы решите поэтапное резервное рабочее время и выложить сертификаты другого типа, вы должны оценить максимально необходимое минимальное количество времени упреждения для сертификатов.</span><span class="sxs-lookup"><span data-stu-id="86fae-143">If you decide to stage and provision certificates of a different type at the same time, you must consider the longest required minimum effective lead time for the certificates.</span></span> <span data-ttu-id="86fae-144">Например, необходимо выполнить поэтапную настройку сертификатов типа AudioVideoAuthentication и OAuthTokenIssuer.</span><span class="sxs-lookup"><span data-stu-id="86fae-144">For example, you need to stage certificates of type AudioVideoAuthentication and OAuthTokenIssuer.</span></span> <span data-ttu-id="86fae-145">Минимальное значение – EffectiveDate должно быть большим из двух сертификатов, в этом случае OAuthTokenIssuer, в котором минимальное время упреждения — 24 часа.</span><span class="sxs-lookup"><span data-stu-id="86fae-145">Your minimum –EffectiveDate must be the greater of the two certificates, in this case the OAuthTokenIssuer, which has a minimum lead time of 24 hours.</span></span> <span data-ttu-id="86fae-146">Если вы не хотите пополнить сертификат AudioVideoAuthentication с временем опережения в 24 часа, поэтапировать его отдельно с помощью EffectiveDate, который больше ваших требований.</span><span class="sxs-lookup"><span data-stu-id="86fae-146">If you do not want to stage the AudioVideoAuthentication certificate with a lead time of 24 hours, stage it separately with an EffectiveDate that is more to your requirements.</span></span>

<div>

## <a name="to-update-or-renew-an-av-edge-service-certificate-with-a-roll-and--effectivedate-parameters"></a><span data-ttu-id="86fae-147">Обновление и возобновление сертификата службы EDGE (A/V) с помощью параметров – рулон и-EffectiveDate</span><span class="sxs-lookup"><span data-stu-id="86fae-147">To update or renew an A/V Edge service certificate with a –Roll and -EffectiveDate parameters</span></span>

1.  <span data-ttu-id="86fae-148">Войдите на локальный компьютер как член группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="86fae-148">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="86fae-149">Запрос возобновления или нового сертификата AudioVideoAuthentication с экспортируемым закрытым ключом для существующего сертификата в службе EDGE (A/V).</span><span class="sxs-lookup"><span data-stu-id="86fae-149">Request a renewal or new AudioVideoAuthentication certificate with exportable private key for the existing certificate on the A/V Edge service.</span></span>

3.  <span data-ttu-id="86fae-150">Импортируйте новый сертификат AudioVideoAuthentication на пограничный сервер и весь другой пограничный сервер в пуле (если у вас есть пул).</span><span class="sxs-lookup"><span data-stu-id="86fae-150">Import the new AudioVideoAuthentication certificate to the Edge Server and all other Edge Server in your pool (if you have a pool deployed).</span></span>

4.  <span data-ttu-id="86fae-151">Настройте импортированный сертификат с помощью командлета Set-CsCertificate и используйте параметр – рулон с параметром – EffectiveDate.</span><span class="sxs-lookup"><span data-stu-id="86fae-151">Configure the imported certificate with the Set-CsCertificate cmdlet and use the –Roll parameter with the –EffectiveDate parameter.</span></span> <span data-ttu-id="86fae-152">Дата вступления в силу должна быть задана в качестве срока действия текущего сертификата (14:00:00 или 2:00:00) минус время жизни токена (по умолчанию восемь часов).</span><span class="sxs-lookup"><span data-stu-id="86fae-152">The effective date should be defined as the current certificate expire time (14:00:00, or 2:00:00 PM) minus token lifetime (by default eight hours).</span></span> <span data-ttu-id="86fae-153">Это дает нам время, в течение которого сертификат должен быть активным, а именно – EffectiveDate \<string\> : "7/22/2012 6:00:00 AM".</span><span class="sxs-lookup"><span data-stu-id="86fae-153">This gives us a time that the certificate must be set to active, and is the –EffectiveDate \<string\>: “7/22/2012 6:00:00 AM”.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="86fae-154">Для пула пограничного сервера необходимо, чтобы все сертификаты AudioVideoAuthentication развернутые и выводились с помощью даты и времени первого развернутого сертификата, чтобы избежать возможного нарушения обмена данными из-за того, что истек срок действия более ранней версии сертификата, после того как все маркеры клиента и потребителя будут обновлены с помощью нового сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-154">For an Edge pool, you must have all AudioVideoAuthentication certificates deployed and provisioned by the date and time defined by the –EffectiveDate parameter of the first certificate deployed to avoid possible A/V communications disruption due to the older certificate expiring before all client and consumer tokens have been renewed using the new certificate.</span></span>

    
    </div>
    
    <span data-ttu-id="86fae-155">Команда Set-CsCertificate с параметром – рулон и – EffectiveTime:</span><span class="sxs-lookup"><span data-stu-id="86fae-155">The Set-CsCertificate command with the –Roll and –EffectiveTime parameter:</span></span>
    
        Set-CsCertificate -Type AudioVideoAuthentication -Thumbprint <thumb print of new certificate> -Roll -EffectiveDate <date and time for certificate to become active>
    
    <span data-ttu-id="86fae-156">Пример Set-CsCertificate команды:</span><span class="sxs-lookup"><span data-stu-id="86fae-156">An example Set-CsCertificate command:</span></span>
    
        Set-CsCertificate -Type AudioVideoAuthentication -Thumbprint "B142918E463981A76503828BB1278391B716280987B" -Roll -EffectiveDate "7/22/2012 6:00:00 AM"
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="86fae-157">EffectiveDate должен быть отформатирован в соответствии с регионом сервера и языковыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="86fae-157">The EffectiveDate must be formatted to match your server’s region and language settings.</span></span> <span data-ttu-id="86fae-158">В примере используются языковые параметры США и Language.</span><span class="sxs-lookup"><span data-stu-id="86fae-158">The example uses the US English Region and Language settings</span></span>

    
    </div>

<span data-ttu-id="86fae-159">Чтобы еще лучше понять процесс, который задается с помощью функции Set-CsCertificate,-рулон и – EffectiveDate, используется для создания нового сертификата для выпуска новых маркеров AudioVideoAuthentication и по-прежнему использовать существующий сертификат для проверки AudioVideoAuthentication, используемых потребителями, визуальная временная шкала является эффективным средством понимания процесса.</span><span class="sxs-lookup"><span data-stu-id="86fae-159">To further understand the process that Set-CsCertificate, -Roll, and –EffectiveDate use to stage a new certificate for issuing new AudioVideoAuthentication tokens while still using an existing certificate to validate AudioVideoAuthentication that are in use by consumers, a visual timeline is an effective means of understanding the process.</span></span>

<span data-ttu-id="86fae-160">В приведенном ниже примере администратор определяет, что срок действия сертификата службы EDGE (A/V) истек в 2:00:00 PM на 07/22/2012.</span><span class="sxs-lookup"><span data-stu-id="86fae-160">In the following example, the administrator determines that the A/V Edge service certificate is due to expire at 2:00:00 PM on 07/22/2012.</span></span> <span data-ttu-id="86fae-161">Он запрашивает и получает новый сертификат и импортирует его на каждый пограничный сервер в его пуле.</span><span class="sxs-lookup"><span data-stu-id="86fae-161">He requests and receives a new certificate and imports it to each Edge Server in his pool.</span></span> <span data-ttu-id="86fae-162">В 07/22/2012 начинается выполнение Get-CsCertificate с параметром – рулон,-Thumbprint, равным строке отпечатка нового сертификата, а для параметра – EffectiveTime — 07/22/2012 6:00:00 AM.</span><span class="sxs-lookup"><span data-stu-id="86fae-162">At 2 AM on 07/22/2012, he begins running Get-CsCertificate with –Roll, -Thumbprint equal to the thumbprint string of the new certificate, and –EffectiveTime set to 07/22/2012 6:00:00 AM.</span></span> <span data-ttu-id="86fae-163">Он запускает эту команду на каждом пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="86fae-163">He runs this command on each Edge Server.</span></span>

<span data-ttu-id="86fae-164">![Использование параметров Roll и EffectiveDate.](images/JJ660292.21d51a76-0d03-4ed7-a37e-a7c14940265f(OCS.15).jpg "Использование параметров Roll и EffectiveDate.")</span><span class="sxs-lookup"><span data-stu-id="86fae-164">![Using the Roll and the EffectiveDate parameters.](images/JJ660292.21d51a76-0d03-4ed7-a37e-a7c14940265f(OCS.15).jpg "Using the Roll and the EffectiveDate parameters.")</span></span>

<span data-ttu-id="86fae-165">По истечении срока действия (7/22/2012 6:00:00 AM) все новые маркеры выдаются новым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="86fae-165">When the effective time is reached (7/22/2012 6:00:00 AM), all new tokens are issued by the new certificate.</span></span> <span data-ttu-id="86fae-166">При проверке маркеров сначала проверяются маркеры для нового сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-166">When validating tokens, tokens will first be validated against the new certificate.</span></span> <span data-ttu-id="86fae-167">Если проверка завершится ошибкой, будет произведена попытка использования старого сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-167">If the validation fails, the old certificate is tried.</span></span> <span data-ttu-id="86fae-168">Процесс попытки нового и прекращения работы старого сертификата будет продолжаться до тех пор, пока не истечет срок действия старого сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-168">The process of trying the new and falling back to the old certificate will continue until the expiry time of the old certificate.</span></span> <span data-ttu-id="86fae-169">После истечения срока действия старого сертификата (7/22/2012 2:00:00 PM) маркеры будут проверяться только новым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="86fae-169">Once the old certificate has expired (7/22/2012 2:00:00 PM), tokens will only be validated by the new certificate.</span></span> <span data-ttu-id="86fae-170">Старый сертификат можно безопасно удалить с помощью командлета Remove-CsCertificate с параметром – Previous.</span><span class="sxs-lookup"><span data-stu-id="86fae-170">The old certificate can be safely removed using the Remove-CsCertificate cmdlet with the –Previous parameter.</span></span>

    Remove-CsCertificate -Type AudioVideoAuthentication -Previous

</div>

<div>

## <a name="to-update-or-renew-an-oauthtokenissuer-certificate-with-a-roll-and--effectivedate-parameters"></a><span data-ttu-id="86fae-171">Обновление сертификата OAuthTokenIssuer с помощью параметров – рулон и EffectiveDate</span><span class="sxs-lookup"><span data-stu-id="86fae-171">To update or renew an OAuthTokenIssuer certificate with a –Roll and -EffectiveDate parameters</span></span>

1.  <span data-ttu-id="86fae-172">Войдите на локальный компьютер как член группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="86fae-172">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="86fae-173">Запрос возобновления или нового сертификата OAuthTokenIssuer с экспортируемым закрытым ключом для существующего сертификата в службе EDGE (A/V).</span><span class="sxs-lookup"><span data-stu-id="86fae-173">Request a renewal or new OAuthTokenIssuer certificate with exportable private key for the existing certificate on the A/V Edge service.</span></span>

3.  <span data-ttu-id="86fae-174">Импортируйте новый сертификат OAuthTokenIssuer на сервер переднего плана в пуле (если у вас развернут пул).</span><span class="sxs-lookup"><span data-stu-id="86fae-174">Import the new OAuthTokenIssuer certificate to a Front End Server in your pool (if you have a pool deployed).</span></span> <span data-ttu-id="86fae-175">Сертификат OAuthTokenIssuer реплицируется глобально и нуждается в обновлении и обновлении на любом сервере в развертывании.</span><span class="sxs-lookup"><span data-stu-id="86fae-175">The OAuthTokenIssuer certificate is replicated globally and only needs to be updated and renewed at any server in your deployment.</span></span> <span data-ttu-id="86fae-176">В качестве примера используется сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="86fae-176">The Front End Server is used as an example.</span></span>

4.  <span data-ttu-id="86fae-177">Настройте импортированный сертификат с помощью командлета Set-CsCertificate и используйте параметр – рулон с параметром – EffectiveDate.</span><span class="sxs-lookup"><span data-stu-id="86fae-177">Configure the imported certificate with the Set-CsCertificate cmdlet and use the –Roll parameter with the –EffectiveDate parameter.</span></span> <span data-ttu-id="86fae-178">Дата вступления в силу должна быть указана как срок действия текущего сертификата (14:00:00 или 2:00:00), но не менее 24 часов.</span><span class="sxs-lookup"><span data-stu-id="86fae-178">The effective date should be defined as the current certificate expire time (14:00:00, or 2:00:00 PM) minus a minimum of 24 hours.</span></span>
    
    <span data-ttu-id="86fae-179">Команда Set-CsCertificate с параметром – рулон и – EffectiveTime:</span><span class="sxs-lookup"><span data-stu-id="86fae-179">The Set-CsCertificate command with the –Roll and –EffectiveTime parameter:</span></span>
    
        Set-CsCertificate -Type OAuthTokenIssuer -Thumbprint <thumb print of new certificate> -Roll -EffectiveDate <date and time for certificate to become active>
    
    <span data-ttu-id="86fae-180">Пример Set-CsCertificate команды:</span><span class="sxs-lookup"><span data-stu-id="86fae-180">An example Set-CsCertificate command:</span></span>
    
        Set-CsCertificate -Type OAuthTokenIssuer -Thumbprint "B142918E463981A76503828BB1278391B716280987B" -Roll -EffectiveDate "7/21/2012 1:00:00 PM"
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="86fae-181">EffectiveDate должен быть отформатирован в соответствии с регионом сервера и языковыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="86fae-181">The EffectiveDate must be formatted to match your server’s region and language settings.</span></span> <span data-ttu-id="86fae-182">В примере используются языковые параметры США и Language.</span><span class="sxs-lookup"><span data-stu-id="86fae-182">The example uses the US English Region and Language settings</span></span>

    
    </div>

<span data-ttu-id="86fae-183">По истечении срока действия (7/21/2012 1:00:00 AM) все новые маркеры выдаются новым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="86fae-183">When the effective time is reached (7/21/2012 1:00:00 AM), all new tokens are issued by the new certificate.</span></span> <span data-ttu-id="86fae-184">При проверке маркеров сначала проверяются маркеры для нового сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-184">When validating tokens, tokens will first be validated against the new certificate.</span></span> <span data-ttu-id="86fae-185">Если проверка завершится ошибкой, будет произведена попытка использования старого сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-185">If the validation fails, the old certificate is tried.</span></span> <span data-ttu-id="86fae-186">Процесс попытки нового и прекращения работы старого сертификата будет продолжаться до тех пор, пока не истечет срок действия старого сертификата.</span><span class="sxs-lookup"><span data-stu-id="86fae-186">The process of trying the new and falling back to the old certificate will continue until the expiry time of the old certificate.</span></span> <span data-ttu-id="86fae-187">После истечения срока действия старого сертификата (7/22/2012 2:00:00 PM) маркеры будут проверяться только новым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="86fae-187">Once the old certificate has expired (7/22/2012 2:00:00 PM), tokens will only be validated by the new certificate.</span></span> <span data-ttu-id="86fae-188">Старый сертификат можно безопасно удалить с помощью командлета Remove-CsCertificate с параметром – Previous.</span><span class="sxs-lookup"><span data-stu-id="86fae-188">The old certificate can be safely removed using the Remove-CsCertificate cmdlet with the –Previous parameter.</span></span>

    Remove-CsCertificate -Type OAuthTokenIssuer -Previous

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="86fae-189">См. также</span><span class="sxs-lookup"><span data-stu-id="86fae-189">See Also</span></span>


[<span data-ttu-id="86fae-190">Планирование сертификатов пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86fae-190">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  
[<span data-ttu-id="86fae-191">Управление проверкой подлинности между сервером (OAuth) и приложениями-партнерами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86fae-191">Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013</span></span>](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md)  


[<span data-ttu-id="86fae-192">Настройка сертификатов пограничного сервера для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86fae-192">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)  
<span data-ttu-id="86fae-193">[Set-CsCertificate](https://technet.microsoft.com/library/Gg398518(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="86fae-193">[Set-CsCertificate](https://technet.microsoft.com/library/Gg398518(v=OCS.15))</span></span>  
<span data-ttu-id="86fae-194">[Remove-CsCertificate](https://technet.microsoft.com/library/Gg412895(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="86fae-194">[Remove-CsCertificate](https://technet.microsoft.com/library/Gg412895(v=OCS.15))</span></span>  
  

<span data-ttu-id="86fae-195"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86fae-195"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

