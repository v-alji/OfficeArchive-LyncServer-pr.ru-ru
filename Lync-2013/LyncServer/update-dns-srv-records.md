---
title: Обновление записей DNS SRV
description: Обновите записи DNS SRV.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Update DNS SRV records
ms:assetid: 9542b91a-108c-4980-89ec-634905cbbf26
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688139(v=OCS.15)
ms:contentKeyID: 49733739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24161074e8f3bcf7e296a957588eeb59d5f2ad1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446551"
---
# <a name="update-dns-srv-records"></a><span data-ttu-id="2a677-103">Обновление записей DNS SRV</span><span class="sxs-lookup"><span data-stu-id="2a677-103">Update DNS SRV records</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a677-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a677-104">

<span> </span></span></span>

<span data-ttu-id="2a677-105">_**Тема последнего изменения:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="2a677-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="2a677-106">Для успешного выполнения этой процедуры необходимо войти на сервер или домен в группу администраторов домена или в группу пользователей DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="2a677-106">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="2a677-107">В этой статье описано, как обновить записи DNS после перехода на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2a677-107">This topic describes how to update the Domain Name System (DNS) records after migrating to Lync Server 2013.</span></span> <span data-ttu-id="2a677-108">После того как все пользователи будут перемещены на Lync Server 2013, но до этого устаревшего пула или режиссера Lync Server 2010, необходимо обновить записи DNS SRV во внутренней службе DNS для каждого домена SIP.</span><span class="sxs-lookup"><span data-stu-id="2a677-108">After all users have been moved to Lync Server 2013, but before the legacy Lync Server 2010 pool or Director is decommissioned, you must update the DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="2a677-109">В этой процедуре предполагается, что в вашей внутренней DNS-зоне есть зоны для доменов пользователей SIP.</span><span class="sxs-lookup"><span data-stu-id="2a677-109">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<span data-ttu-id="2a677-110">**Настройка DNS-записи SRV**</span><span class="sxs-lookup"><span data-stu-id="2a677-110">**To configure a DNS SRV record**</span></span>

1.  <span data-ttu-id="2a677-111">На DNS-сервере нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **DNS**.</span><span class="sxs-lookup"><span data-stu-id="2a677-111">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="2a677-112">В дереве консоли для вашего домена SIP разверните раздел **зоны прямого просмотра**, РАЗВЕРНИТЕ домен SIP, в котором установлен Lync Server 2013, и перейдите к параметру **\_ TCP** .</span><span class="sxs-lookup"><span data-stu-id="2a677-112">In the console tree for your SIP domain, expand **Forward Lookup Zones**, expand the SIP domain in which Lync Server 2013 is installed, and navigate to the **\_tcp** setting.</span></span>

3.  <span data-ttu-id="2a677-113">В правой области щелкните правой кнопкой мыши **\_ sipinternaltls** и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="2a677-113">In the right pane, right click **\_sipinternaltls** and select **Properties**.</span></span>

4.  <span data-ttu-id="2a677-114">В **узле, предлагающем эту службу**, обновите полное доменное имя узла, чтобы оно указывало на пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2a677-114">In **Host offering this service**, update the host FQDN to point to the Lync Server 2013 pool.</span></span>

5.  <span data-ttu-id="2a677-115">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a677-115">Click **OK**.</span></span>

<span data-ttu-id="2a677-116">**Проверка возможности разрешения полных доменных имен в пуле или сервере Standard Edition**</span><span class="sxs-lookup"><span data-stu-id="2a677-116">**To verify that the FQDN of the Front End pool or Standard Edition server can be resolved**</span></span>

1.  <span data-ttu-id="2a677-117">Войдите в домен на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="2a677-117">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="2a677-118">В меню **Пуск** выберите пункт **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="2a677-118">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="2a677-119">В поле **Открыть** введите **cmd** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a677-119">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="2a677-120">В командной строке введите **nslookup** \<FQDN of the Front End pool\> или и нажмите \<FQDN of the Standard Edition server\> клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="2a677-120">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="2a677-121">Убедитесь в том, что вы получили ответ на соответствующий IP-адрес для полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="2a677-121">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="2a677-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a677-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

