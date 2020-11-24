---
title: Настройка DNS-записей для развертывания пилотного пула
description: Настройка записей DNS для развертывания пилотного пула.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398872"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a><span data-ttu-id="8a00b-103">Настройка DNS-записей для развертывания пилотного пула</span><span class="sxs-lookup"><span data-stu-id="8a00b-103">Configure DNS records for pilot pool deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a00b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a00b-104">

<span> </span></span></span>

<span data-ttu-id="8a00b-105">_**Тема последнего изменения:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="8a00b-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="8a00b-106">Перед развертыванием пула проектов Lync Server 2013 Pilot необходимо обновить записи узла DNS для пилотного пула.</span><span class="sxs-lookup"><span data-stu-id="8a00b-106">Prior to deploying the Lync Server 2013 pilot pool, you must update the DNS Host A entries for the pilot pool.</span></span> <span data-ttu-id="8a00b-107">Для успешного выполнения этой процедуры необходимо войти на сервер или домен в группу администраторов домена или в группу пользователей DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="8a00b-107">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="8a00b-108">**Настройка записей узла DNS**</span><span class="sxs-lookup"><span data-stu-id="8a00b-108">**To configure DNS Host A records**</span></span>

1.  <span data-ttu-id="8a00b-109">На сервере доменных имен (DNS) нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **DNS**.</span><span class="sxs-lookup"><span data-stu-id="8a00b-109">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="8a00b-110">В дереве консоли для вашего домена разверните раздел **зоны прямого просмотра** и щелкните правой кнопкой мыши домен, в котором будет установлен Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8a00b-110">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="8a00b-111">Выберите команду **создать узел (A или AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="8a00b-111">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="8a00b-112">Щелкните **Name (имя**), введите имя узла для пула Lync Server 2013 (доменное имя будет указано в той зоне, в которой она определена, и ее не нужно вводить как часть записи A).</span><span class="sxs-lookup"><span data-stu-id="8a00b-112">Click **Name**, type the host name for the Lync Server 2013 pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="8a00b-113">Щелкните **IP-адрес**, введите IP-адрес пула переднего плана.</span><span class="sxs-lookup"><span data-stu-id="8a00b-113">Click **IP Address**, type the IP address for the Front End pool.</span></span>

6.  <span data-ttu-id="8a00b-114">Нажмите кнопку **Добавить узел** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8a00b-114">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="8a00b-115">Когда все будет готово, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="8a00b-115">When you are finished, click **Done**.</span></span>

<span data-ttu-id="8a00b-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a00b-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

