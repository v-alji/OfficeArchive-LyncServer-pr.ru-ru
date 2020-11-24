---
title: 'Lync Server 2013: обзор требований к брандмауэру для SQL Server'
description: 'Lync Server 2013: Общие сведения о требованиях брандмауэра SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding firewall requirements for SQL Server
ms:assetid: 31d7df2c-589f-465e-be74-cf6767db190d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425818(v=OCS.15)
ms:contentKeyID: 48183781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c434474b36ced0fe64b9398f7d0e6136ff523a93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399484"
---
# <a name="understanding-firewall-requirements-for-sql-server-with-lync-server-2013"></a><span data-ttu-id="ef244-103">Обзор требований к брандмауэру для SQL Server с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef244-103">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef244-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef244-104">

<span> </span></span></span>

<span data-ttu-id="ef244-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ef244-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ef244-106">Для развертывания в стандартном выпуске исключения брандмауэра создаются автоматически во время установки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef244-106">For a Standard Edition deployment, firewall exceptions are created automatically during Lync Server 2013 Setup.</span></span> <span data-ttu-id="ef244-107">Тем не менее, для развертывания выпуска Enterprise Edition необходимо вручную настроить исключения брандмауэра на сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ef244-107">However, for Enterprise Edition deployments, you must configure the firewall exceptions manually on the SQL Server Back End Server.</span></span> <span data-ttu-id="ef244-108">Протокол TCP/IP позволяет использовать конкретный порт для определенного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ef244-108">The TCP/IP protocol allows for a given port to be used once for a given IP address.</span></span> <span data-ttu-id="ef244-109">Это означает, что для сервера SQL Server вы можете назначить экземпляру базы данных по умолчанию порт 1433 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef244-109">This means that for the SQL Server-based server you can assign the default database instance the default TCP port 1433.</span></span> <span data-ttu-id="ef244-110">Для всех других экземпляров вам потребуется использовать диспетчер конфигурации SQL Server для назначения уникальных и неиспользуемых портов.</span><span class="sxs-lookup"><span data-stu-id="ef244-110">For any other instances you will need to use the SQL Server Configuration Manager to assign unique and unused ports.</span></span> <span data-ttu-id="ef244-111">В этой статье рассматриваются следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="ef244-111">This topic covers:</span></span>

  - <span data-ttu-id="ef244-112">Требования к исключению брандмауэра при использовании экземпляра по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ef244-112">Requirements for a firewall exception when using the default instance</span></span>

  - <span data-ttu-id="ef244-113">Требования к исключению межсетевого экрана для службы браузера SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef244-113">Requirements for a firewall exception for the SQL Server Browser service</span></span>

  - <span data-ttu-id="ef244-114">Требования к статическим портам для прослушивания при использовании именованных экземпляров</span><span class="sxs-lookup"><span data-stu-id="ef244-114">Requirements for static listening ports when using named instances</span></span>

<div>

## <a name="requirements-for-a-firewall-exception-when-using-the-default-instance"></a><span data-ttu-id="ef244-115">Требования к исключению брандмауэра при использовании экземпляра по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ef244-115">Requirements for a Firewall Exception When Using the Default Instance</span></span>

<span data-ttu-id="ef244-116">Если вы используете экземпляр SQL Server по умолчанию для любой базы данных при развертывании Lync Server 2013, для обеспечения взаимодействия из пула переднего плана с экземпляром SQL Server по умолчанию используются следующие требования правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ef244-116">If you are using the SQL Server default instance for any database when deploying Lync Server 2013, the following firewall rule requirements are used to help ensure communication from the Front End pool to the SQL Server default instance.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef244-117">Протокол</span><span class="sxs-lookup"><span data-stu-id="ef244-117">Protocol</span></span></th>
<th><span data-ttu-id="ef244-118">Порт</span><span class="sxs-lookup"><span data-stu-id="ef244-118">Port</span></span></th>
<th><span data-ttu-id="ef244-119">Направление</span><span class="sxs-lookup"><span data-stu-id="ef244-119">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef244-120">TCP</span><span class="sxs-lookup"><span data-stu-id="ef244-120">TCP</span></span></p></td>
<td><p><span data-ttu-id="ef244-121">1433</span><span class="sxs-lookup"><span data-stu-id="ef244-121">1433</span></span></p></td>
<td><p><span data-ttu-id="ef244-122">Входящий на сервер SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef244-122">Inbound to SQL Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-a-firewall-exception-for-the-sql-server-browser-service"></a><span data-ttu-id="ef244-123">Требования к исключению межсетевого экрана для службы браузера SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef244-123">Requirements for a Firewall Exception for the SQL Server Browser Service</span></span>

<span data-ttu-id="ef244-124">Служба "Обозреватель SQL Server" обнаружит экземпляры базы данных и настроит порт, для которого настроен экземпляр (с именем или по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ef244-124">The SQL Server Browser service will locate database instances and communicate the port that the instance (named or default) is configured to use.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef244-125">Протокол</span><span class="sxs-lookup"><span data-stu-id="ef244-125">Protocol</span></span></th>
<th><span data-ttu-id="ef244-126">Порт</span><span class="sxs-lookup"><span data-stu-id="ef244-126">Port</span></span></th>
<th><span data-ttu-id="ef244-127">Направление</span><span class="sxs-lookup"><span data-stu-id="ef244-127">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef244-128">UDP</span><span class="sxs-lookup"><span data-stu-id="ef244-128">UDP</span></span></p></td>
<td><p><span data-ttu-id="ef244-129">1434</span><span class="sxs-lookup"><span data-stu-id="ef244-129">1434</span></span></p></td>
<td><p><span data-ttu-id="ef244-130">443</span><span class="sxs-lookup"><span data-stu-id="ef244-130">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-static-listening-ports-when-using-named-instances"></a><span data-ttu-id="ef244-131">Требования к статическим портам для прослушивания при использовании именованных экземпляров</span><span class="sxs-lookup"><span data-stu-id="ef244-131">Requirements for Static Listening Ports When Using Named Instances</span></span>

<span data-ttu-id="ef244-132">При использовании именованных экземпляров в конфигурации SQL Server для баз данных, поддерживающих Lync Server 2013, вы конфигурируете статические порты с помощью диспетчера конфигурации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ef244-132">When using named instances in the SQL Server configuration for databases supporting Lync Server 2013, you configure static ports by using SQL Server Configuration Manager.</span></span> <span data-ttu-id="ef244-133">После того как статические порты будут назначены каждому именованному экземпляру, вы создаете исключения для каждого статического порта в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="ef244-133">After the static ports have been assigned to each named instance, you create exceptions for each static port in the firewall.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef244-134">Протокол</span><span class="sxs-lookup"><span data-stu-id="ef244-134">Protocol</span></span></th>
<th><span data-ttu-id="ef244-135">Порт</span><span class="sxs-lookup"><span data-stu-id="ef244-135">Port</span></span></th>
<th><span data-ttu-id="ef244-136">Направление</span><span class="sxs-lookup"><span data-stu-id="ef244-136">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef244-137">TCP</span><span class="sxs-lookup"><span data-stu-id="ef244-137">TCP</span></span></p></td>
<td><p><span data-ttu-id="ef244-138">Статическое определение</span><span class="sxs-lookup"><span data-stu-id="ef244-138">Statically defined</span></span></p></td>
<td><p><span data-ttu-id="ef244-139">443</span><span class="sxs-lookup"><span data-stu-id="ef244-139">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sql-server-documentation"></a><span data-ttu-id="ef244-140">Документация по SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef244-140">SQL Server Documentation</span></span>

<span data-ttu-id="ef244-141">Документация по Microsoft SQL Server 2012 содержит подробные инструкции по настройке доступа к межсетевому экрану для баз данных.</span><span class="sxs-lookup"><span data-stu-id="ef244-141">Microsoft SQL Server 2012 documentation provides detailed guidance on how to configure firewall access for databases.</span></span> <span data-ttu-id="ef244-142">Подробные сведения о Microsoft SQL Server 2012 можно найти в разделе "Настройка брандмауэра Windows для обеспечения доступа к SQL Server" [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031) .</span><span class="sxs-lookup"><span data-stu-id="ef244-142">For details about Microsoft SQL Server 2012, see “Configuring the Windows Firewall to Allow SQL Server Access” at [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031).</span></span>

<span data-ttu-id="ef244-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef244-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

