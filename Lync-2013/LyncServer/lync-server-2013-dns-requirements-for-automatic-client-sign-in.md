---
title: 'Lync Server 2013: требования DNS для автоматического входа клиента'
description: 'Lync Server 2013: требования DNS для автоматического входа клиента.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for automatic client sign-in
ms:assetid: 3bcd4bb3-a022-4ffa-b005-1a95ad2b1796
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425884(v=OCS.15)
ms:contentKeyID: 48183873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2247c955e0a563a22fb5d0ec20735291a836cdfc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399748"
---
# <a name="dns-requirements-for-automatic-client-sign-in-in-lync-server-2013"></a><span data-ttu-id="c807d-103">Требования DNS для автоматического входа клиента в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c807d-103">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c807d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c807d-104">

<span> </span></span></span>

<span data-ttu-id="c807d-105">_**Тема последнего изменения:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="c807d-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="c807d-106">В этом разделе объясняются DNS-записи, необходимые для автоматического входа в систему клиента.</span><span class="sxs-lookup"><span data-stu-id="c807d-106">This section explains the Domain Name System (DNS) records that are required for automatic client sign-in.</span></span> <span data-ttu-id="c807d-107">При развертывании серверов стандартных выпусков или пулов переднего плана можно настроить клиентские компьютеры на использование автоматического обнаружения для входа на соответствующий сервер Standard Edition или пул внешних интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="c807d-107">When you deploy your Standard Edition servers or Front End pools, you can configure your clients to use automatic discovery to sign in to the appropriate Standard Edition server or Front End pool.</span></span> <span data-ttu-id="c807d-108">Если требуется, чтобы клиенты подключались к Lync Server 2013 вручную, вы можете пропустить этот раздел.</span><span class="sxs-lookup"><span data-stu-id="c807d-108">If you plan to require your clients to connect manually to Lync Server 2013, you can skip this topic.</span></span>

<span data-ttu-id="c807d-109">Для поддержки автоматического входа в клиент необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c807d-109">To support automatic client sign-in, you must:</span></span>

  - <span data-ttu-id="c807d-110">Назначение одного сервера или пула для распространения и проверки подлинности запросов на вход в клиент.</span><span class="sxs-lookup"><span data-stu-id="c807d-110">Designate a single server or pool to distribute and authenticate client sign-in requests.</span></span> <span data-ttu-id="c807d-111">Это может быть существующий сервер или пул в Организации, на котором размещаются пользователи, или вы можете назначить выделенный сервер или пул для этой цели, где нет пользователей.</span><span class="sxs-lookup"><span data-stu-id="c807d-111">This can be an existing server or pool in your organization that hosts users, or you can designate a dedicated server or pool for this purpose that hosts no users.</span></span> <span data-ttu-id="c807d-112">Для обеспечения высокой доступности мы рекомендуем указать пул переднего плана для этой функции.</span><span class="sxs-lookup"><span data-stu-id="c807d-112">For high availability, we recommend that you designate a Front End pool for this function.</span></span>

  - <span data-ttu-id="c807d-113">Создание внутренней записи SRV DNS для поддержки автоматического входа клиента для этого сервера или пула.</span><span class="sxs-lookup"><span data-stu-id="c807d-113">Create an internal DNS SRV record to support automatic client sign-in for this server or pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c807d-114">В следующих требованиях к записям домен SIP относится к части URI SIP, назначенной пользователям.</span><span class="sxs-lookup"><span data-stu-id="c807d-114">In the following record requirements, SIP domain refers to the host portion of the SIP URIs assigned to users.</span></span> <span data-ttu-id="c807d-115">Например, если URI SIP имеет форму \* @contoso. com, contoso.com — это домен SIP.</span><span class="sxs-lookup"><span data-stu-id="c807d-115">For example, if SIP URIs are of the form \*@contoso.com, contoso.com is the SIP domain.</span></span> <span data-ttu-id="c807d-116">Домен SIP часто отличается от внутреннего домена Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c807d-116">The SIP domain is often different from the internal Active Directory domain.</span></span> <span data-ttu-id="c807d-117">Организация также может поддерживать несколько доменов SIP.</span><span class="sxs-lookup"><span data-stu-id="c807d-117">An organization can also support multiple SIP domains.</span></span>

    
    </div>

<span data-ttu-id="c807d-118">Чтобы включить автоматическую настройку для клиентов, необходимо создать внутреннюю SRV-запись DNS, которая сопоставляет одну из указанных ниже записей с полным доменным именем (FQDN) переднего плана или сервера Standard Edition, который распространяет запросы на вход из клиентов Lync:</span><span class="sxs-lookup"><span data-stu-id="c807d-118">To enable automatic configuration for your clients, you must create an internal DNS SRV record that maps one of the following records to the fully qualified domain name (FQDN) of the Front End pool or Standard Edition server that distributes sign-in requests from Lync clients:</span></span>

  - <span data-ttu-id="c807d-119">\_sipinternaltls. \_ Номера.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c807d-119">\_sipinternaltls.\_tcp.\<domain\></span></span> <span data-ttu-id="c807d-120">-для внутренних подключений TLS</span><span class="sxs-lookup"><span data-stu-id="c807d-120">- for internal TLS connections</span></span>

<span data-ttu-id="c807d-121">Вам нужно только создать единственную запись SRV для пула переднего плана или сервера Standard Edition либо которая будет распространять запросы на вход.</span><span class="sxs-lookup"><span data-stu-id="c807d-121">You only need to create a single SRV record for the Front End pool or Standard Edition server or that will distribute sign-in requests.</span></span>

<span data-ttu-id="c807d-122">В следующей таблице показаны некоторые примеры записей, необходимых для вымышленной компании Contoso, которая поддерживает домены SIP для contoso.com и retail.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c807d-122">The following table shows some example records required for the fictitious company Contoso, which supports SIP domains of contoso.com and retail.contoso.com.</span></span>

### <a name="example-of-dns-records-required-for-automatic-client-sign-in-with-multiple-sip-domains"></a><span data-ttu-id="c807d-123">Пример DNS-записей, необходимых для автоматического входа в клиент с несколькими доменами SIP</span><span class="sxs-lookup"><span data-stu-id="c807d-123">Example of DNS Records Required for Automatic Client Sign-in with Multiple SIP Domains</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c807d-124">Полное доменное имя пула переднего плана, используемое для распространения запросов на вход</span><span class="sxs-lookup"><span data-stu-id="c807d-124">FQDN of Front End pool used to distribute sign-in requests</span></span></th>
<th><span data-ttu-id="c807d-125">Домен SIP</span><span class="sxs-lookup"><span data-stu-id="c807d-125">SIP domain</span></span></th>
<th><span data-ttu-id="c807d-126">SRV-запись DNS</span><span class="sxs-lookup"><span data-stu-id="c807d-126">DNS SRV record</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c807d-127">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c807d-127">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c807d-128">contoso.com</span><span class="sxs-lookup"><span data-stu-id="c807d-128">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c807d-129">SRV-запись для домена _sipinternaltls. _tcp. contoso. com по порту 5061, сопоставленная с pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c807d-129">An SRV record for _sipinternaltls._tcp.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c807d-130">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c807d-130">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c807d-131">retail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c807d-131">retail.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c807d-132">SRV-запись для домена _sipinternaltls. _tcp. Retail. contoso. com по порту 5061, сопоставленная с pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c807d-132">An SRV record for _sipinternaltls._tcp.retail.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="c807d-133">По умолчанию запросы DNS-записей соответствуют строгому сопоставлению доменных имен между доменом в имени пользователя и записи SRV.</span><span class="sxs-lookup"><span data-stu-id="c807d-133">By default, queries for DNS records adhere to strict domain name matching between the domain in the user name and the SRV record.</span></span> <span data-ttu-id="c807d-134">Если вы предпочитаете, чтобы клиентские DNS-запросы вместо этого использовали соответствующие суффиксы, вы можете настроить групповую политику DisableStrictDNSNaming.</span><span class="sxs-lookup"><span data-stu-id="c807d-134">If you prefer that client DNS queries use suffix matching instead, you can configure the DisableStrictDNSNaming Group Policy.</span></span> <span data-ttu-id="c807d-135">Подробные сведения можно найти <A href="lync-server-2013-planning-for-clients-and-devices.md">в разделе Планирование клиентов и устройств в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="c807d-135">For details, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="example-of-the-certificates-and-dns-records-required-for-automatic-client-sign-in"></a><span data-ttu-id="c807d-136">Пример сертификатов и записей DNS, необходимых для автоматических клиентских Sign-In</span><span class="sxs-lookup"><span data-stu-id="c807d-136">Example of the Certificates and DNS Records Required for Automatic Client Sign-In</span></span>

<span data-ttu-id="c807d-137">В этом примере используются те же примеры имен из приведенной выше таблицы.</span><span class="sxs-lookup"><span data-stu-id="c807d-137">This example uses the same example names in the preceding table.</span></span> <span data-ttu-id="c807d-138">Организация Contoso поддерживает домены SIP для contoso.com и retail.contoso.com, а все его пользователи имеют URI SIP в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="c807d-138">The Contoso organization supports the SIP domains of contoso.com and retail.contoso.com, and all of its users have a SIP URI in one of the following forms:</span></span>

  - <span data-ttu-id="c807d-139">\<user\>@retail. contoso.com</span><span class="sxs-lookup"><span data-stu-id="c807d-139">\<user\>@retail.contoso.com</span></span>

  - <span data-ttu-id="c807d-140">\<user\>@contoso. com</span><span class="sxs-lookup"><span data-stu-id="c807d-140">\<user\>@contoso.com</span></span>

<span data-ttu-id="c807d-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c807d-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

