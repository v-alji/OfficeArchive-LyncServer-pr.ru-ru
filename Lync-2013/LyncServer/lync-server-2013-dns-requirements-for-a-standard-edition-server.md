---
title: 'Lync Server 2013: Требования DNS для сервера Standard Edition'
description: 'Lync Server 2013: требования к DNS для сервера Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399751"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="cde9b-103">Требования DNS для сервера Standard Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cde9b-103">DNS requirements for a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cde9b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cde9b-104">

<span> </span></span></span>

<span data-ttu-id="cde9b-105">_**Тема последнего изменения:** 22.02.2013_</span><span class="sxs-lookup"><span data-stu-id="cde9b-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="cde9b-106">В этом разделе описаны записи службы доменных имен (DNS), необходимые для развертывания серверов Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="cde9b-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="cde9b-107">DNS Records for Standard Edition Servers</span><span class="sxs-lookup"><span data-stu-id="cde9b-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="cde9b-108">В следующей таблице указаны требования к DNS для развертывания сервера Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="cde9b-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cde9b-109">Сценарий развертывания</span><span class="sxs-lookup"><span data-stu-id="cde9b-109">Deployment scenario</span></span></th>
<th><span data-ttu-id="cde9b-110">Требование DNS</span><span class="sxs-lookup"><span data-stu-id="cde9b-110">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cde9b-111">Standard Edition</span><span class="sxs-lookup"><span data-stu-id="cde9b-111">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="cde9b-112">Внутренняя запись A, разрешающая полное доменное имя сервера в IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cde9b-112">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cde9b-113">Автоматический вход в клиент</span><span class="sxs-lookup"><span data-stu-id="cde9b-113">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="cde9b-114">Для каждого поддерживаемых домена SIP записи SRV для _sipinternaltls._tcp. &lt; домен через порт 5061, который сопопишется с FQDN сервера Standard Edition, который аутентификация и перенаправляет запросы клиентов на &gt; вход.</span><span class="sxs-lookup"><span data-stu-id="cde9b-114">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="cde9b-115">Подробные сведения см. в требованиях К DNS для автоматического входов <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">клиентов в Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="cde9b-115">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cde9b-116">Обнаружение веб-службы обновления устройств на устройствах единой коммуникации</span><span class="sxs-lookup"><span data-stu-id="cde9b-116">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="cde9b-117">Внутренняя запись A с именем ucupdates-r2. &lt; Домен SIP, который передается на IP-адрес веб-службы обновления устройства standard Edition на сервере Standard &gt; Edition.</span><span class="sxs-lookup"><span data-stu-id="cde9b-117">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="cde9b-118">В ситуации, когда устройство UC включено, но пользователь никогда не вошел в систему, запись A позволяет устройству найти веб-службу обновления устройства на сервере и получить обновления.</span><span class="sxs-lookup"><span data-stu-id="cde9b-118">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="cde9b-119">В противном случае устройство получает сведения о сервере посредством автоматической подготовки при первом входе пользователя.</span><span class="sxs-lookup"><span data-stu-id="cde9b-119">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span> <span data-ttu-id="cde9b-120">Подробные сведения см. в веб-службе обновления устройств <a href="lync-server-2013-device-update-web-service.md">в Lync Server 2013</a> в документации "Операции".</span><span class="sxs-lookup"><span data-stu-id="cde9b-120">For details, see <a href="lync-server-2013-device-update-web-service.md">Device Update Web service in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cde9b-121">Обратный прокси-сервер для поддержки HTTP-трафика</span><span class="sxs-lookup"><span data-stu-id="cde9b-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="cde9b-122">Внешняя запись A, которая устраняет FQDN внешней веб-фермы с внешним IP-адресом обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cde9b-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="cde9b-123">Клиенты и устройства UC используют эту запись для подключения к обратному прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="cde9b-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="cde9b-124">Подробные сведения см. в документации по планированию определения требований К DNS для <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="cde9b-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cde9b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="cde9b-125">See Also</span></span>


[<span data-ttu-id="cde9b-126">Требования К DNS для автоматического входов клиентов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cde9b-126">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[<span data-ttu-id="cde9b-127">Определение требований DNS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cde9b-127">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="cde9b-128">Веб-служба обновления устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cde9b-128">Device Update Web service in Lync Server 2013</span></span>](lync-server-2013-device-update-web-service.md)  
  

<span data-ttu-id="cde9b-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cde9b-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

