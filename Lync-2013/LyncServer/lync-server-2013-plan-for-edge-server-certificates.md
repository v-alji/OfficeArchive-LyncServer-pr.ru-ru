---
title: 'Lync Server 2013: планирование сертификатов пограничного сервера'
description: 'Lync Server 2013: Планирование сертификатов пограничного сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Plan for Edge Server certificates
ms:assetid: f1dfe220-2398-4ac8-ba4c-206c8c0cbc50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413010(v=OCS.15)
ms:contentKeyID: 48185798
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22ec3743256fe3e4c55dba0f6357a85b1ad81cd0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437134"
---
# <a name="plan-for-edge-server-certificates-in-lync-server-2013"></a><span data-ttu-id="4a2c2-103">Планирование сертификатов пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a2c2-103">Plan for Edge Server certificates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a2c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a2c2-104">

<span> </span></span></span>

<span data-ttu-id="4a2c2-105">_**Тема последнего изменения:** 2012-11-05_</span><span class="sxs-lookup"><span data-stu-id="4a2c2-105">_**Topic Last Modified:** 2012-11-05_</span></span>

<span data-ttu-id="4a2c2-106">Создание сертификатов для Edge упрощено в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-106">Certificate creation for Edge is simplified in Lync Server 2013.</span></span>

<span data-ttu-id="4a2c2-107">**Блок-схема сертификации для пограничного сервера**</span><span class="sxs-lookup"><span data-stu-id="4a2c2-107">**Certificates Flow Chart for Edge Server**</span></span>

<span data-ttu-id="4a2c2-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span><span class="sxs-lookup"><span data-stu-id="4a2c2-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span></span>

<span data-ttu-id="4a2c2-109">Создание единого общедоступного сертификата убедитесь, что у вас есть закрытый ключ, определенный для этого сертификата, и назначьте его следующим внешним интерфейсам пограничного сервера с помощью мастера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-109">Create a single public certificate, ensure that you have an exportable private key defined for the certificate, and assign it to the following Edge Server external interfaces using the certificate wizard:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="4a2c2-110">Сертификаты с подстановочными знаками не поддерживаются в Lync Server, за исключением тех случаев, когда используются для суммирования простых URL-адресов с помощью обратного прокси.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-110">Wildcard certificates are not supported in Lync Server, except where used to summarize the Simple URLs through the reverse proxy.</span></span> <span data-ttu-id="4a2c2-111">Для каждого доменного имени SIP, службы Edge для веб-конференций, службы Edge/V и XMPP домена, предлагаемого вашим развертыванием, необходимо определить разные имена альтернативных субъектов (SAN).</span><span class="sxs-lookup"><span data-stu-id="4a2c2-111">You must define distinct subject alternate names (SANs) for each SIP domain name, Web Conferencing Edge service, A/V Edge service and XMPP domain offered by your deployment.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="4a2c2-112">Впервые введены в Lync Server 2013, для хранения сертификатов проверки подлинности звука и видео в предварительной версии для текущего сертификата требуется дополнительное планирование.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-112">Introduced in Lync Server 2013, staging Audio/Video Authentication certificates in advance of the expiration time of the current certificate requires some additional planning.</span></span> <span data-ttu-id="4a2c2-113">Вместо одного сертификата с несколькими целями доступа к внешнему интерфейсу Edge вам потребуется два сертификата, один из которых назначается службе Edge Access и служба Edge для веб-конференций, а также один сертификат для службы EDGE (/V).</span><span class="sxs-lookup"><span data-stu-id="4a2c2-113">Instead of one certificate with multiple purposes for the external Edge interface, you will require two certificates, one assigned to the Access Edge service and Web Conferencing Edge service, and one certificate for the A/V Edge service.</span></span> <span data-ttu-id="4a2c2-114">Дополнительные сведения можно найти в разделе " <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">промежуточный выпуск и сертификаты OAuth" в Lync Server 2013 с помощью Set-CsCertificate</A></span><span class="sxs-lookup"><span data-stu-id="4a2c2-114">For additional details, see <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</A></span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="4a2c2-115">В случае с пулом пограничных серверов вы экспортируете сертификат с закрытым ключом на каждый пограничный сервер и назначаете этот сертификат для каждой службы пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-115">In the event of a pool of Edge Servers, you export the certificate with the private key to each Edge Server and assign the certificate to each Edge Server service.</span></span> <span data-ttu-id="4a2c2-116">Сделайте то же самое для внутреннего сертификата пограничного сервера, экспортируйте сертификат с закрытым ключом и назначая каждый внутренний интерфейс EDGE.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-116">Do the same for the internal Edge Server certificate, exporting the certificate with the private key and assigning to each internal Edge interface.</span></span>



</div>

  - <span data-ttu-id="4a2c2-117">Убедитесь, что у вас есть закрытый ключ, назначаемый для экспорта сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-117">Ensure that you have an exportable private key assigned for the certificate</span></span>

  - <span data-ttu-id="4a2c2-118">Служба пограничного доступа (в мастере сертификатов), называемая **внешним доступом к SIP Edge**</span><span class="sxs-lookup"><span data-stu-id="4a2c2-118">Access Edge service (referred to as **SIP Access Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="4a2c2-119">Служба веб-конференций EDGE (в мастере сертификатов), называемая **внешними веб-Конференцией** .</span><span class="sxs-lookup"><span data-stu-id="4a2c2-119">Web Conferencing Edge service (referred to as **Web Conferencing Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="4a2c2-120">Служба проверки подлинности (/V) (в мастере сертификатов она ссылается на **внешний край** )</span><span class="sxs-lookup"><span data-stu-id="4a2c2-120">A/V Authentication service (referred to as **A/V Edge External** in the certificate wizard)</span></span>

<span data-ttu-id="4a2c2-121">Создайте единый внутренний сертификат с экспортируемым закрытым ключом, скопируйте и назначьте его каждому из внутренних интерфейсов пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-121">Create a single internal certificate with exportable private key, copy and assign it to each of the Edge Server internal interfaces:</span></span>

  - <span data-ttu-id="4a2c2-122">Пограничный сервер (в мастере сертификатов называемый **внутренним краем** )</span><span class="sxs-lookup"><span data-stu-id="4a2c2-122">Edge Server (referred to as **Edge Internal** in the certificate wizard)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="4a2c2-123">Для каждой службы пограничного сервера можно использовать отдельные сертификаты.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-123">It is possible to use separate and distinct certificates for each Edge Server service.</span></span> <span data-ttu-id="4a2c2-124">Правильная причина выбора разных сертификатов — если вы хотите использовать новую функцию многопроходного сертификата для сертификата службы Edge.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-124">A good reason to choose separate certificates is if you want to use the new rolling certificate feature for the A/V Edge service certificate.</span></span> <span data-ttu-id="4a2c2-125">В случае использования этой функции рекомендуется установить связь с сертификатом службы EDGE в службе пограничного доступа и веб-конференции с пограничным соединением.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-125">In the case of this feature, decoupling the A/V Edge service certificate from the Access Edge service and Web Conferencing Edge service is recommended.</span></span> <span data-ttu-id="4a2c2-126">Если вы решите запросить, получить и назначить отдельные сертификаты для каждой службы, вы должны запросить разрешение экспорта закрытого ключа для службы Edge/V (опять же, это является службой проверки подлинности) и назначить один и тот же сертификат внешнему интерфейсу A/V на пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="4a2c2-126">If you choose to request, acquire and assign separate certificates for each service, you must request that the private key be exportable for the A/V Edge service (again, this is in actuality the A/V Authentication service) and assign the same certificate to the A/V Edge External interface on each Edge Server.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4a2c2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4a2c2-127">See Also</span></span>


[<span data-ttu-id="4a2c2-128">Промежуточный выпуск и сертификаты OAuth в Lync Server 2013 с помощью Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="4a2c2-128">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</span></span>](lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  


[<span data-ttu-id="4a2c2-129">Изменения Lync Server 2013, затрагивающие планирование пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="4a2c2-129">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)  
  

<span data-ttu-id="4a2c2-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a2c2-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

