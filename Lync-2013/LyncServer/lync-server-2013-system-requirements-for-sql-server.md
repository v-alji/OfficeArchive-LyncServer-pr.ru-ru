---
title: 'Lync Server 2013: системные требования для SQL Server'
description: 'Lync Server 2013: требования к системе для SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: System requirements for SQL Server
ms:assetid: 9c235085-cbfa-4e9e-9cec-3f5749039a6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205112(v=OCS.15)
ms:contentKeyID: 48184904
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 524136174be8798aed1dc7d5d236dbb45ab18330
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444555"
---
# <a name="system-requirements-for-sql-server-in-lync-server-2013"></a><span data-ttu-id="af708-103">Системные требования для SQL Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af708-103">System requirements for SQL Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af708-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af708-104">

<span> </span></span></span>

<span data-ttu-id="af708-105">_**Тема последнего изменения:** 2013-10-25_</span><span class="sxs-lookup"><span data-stu-id="af708-105">_**Topic Last Modified:** 2013-10-25_</span></span>

<span data-ttu-id="af708-106">Перед развертыванием сервера Enterprise Edition установите Microsoft SQL Server 2008 R2 или Microsoft SQL Server 2012 на выделенный компьютер, соответствующий требованиям к оборудованию.</span><span class="sxs-lookup"><span data-stu-id="af708-106">Before you deploy Enterprise Edition server, install Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 on a dedicated computer that meets the hardware requirements.</span></span> <span data-ttu-id="af708-107">Сведения о требованиях к оборудованию можно найти в документации [серверные платформы для Lync server 2013](lync-server-2013-server-hardware-platforms.md) .</span><span class="sxs-lookup"><span data-stu-id="af708-107">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span> <span data-ttu-id="af708-108">Сведения о требованиях к программному обеспечению можно найти в разделе [Поддержка программного обеспечения баз данных в Lync Server 2013](lync-server-2013-database-software-support.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="af708-108">For details about software requirements, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="af708-109">Сведения о разрешениях, необходимых для развертывания, содержатся [в разделе разрешения на развертывание для SQL Server в Lync server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="af708-109">For information about the permissions necessary for deployment, see [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span></span>

<span data-ttu-id="af708-110">Перед созданием пула переднего плана необходимо также настроить брандмауэр Windows, чтобы разрешить доступ к SQL Server для Lync Server 2013 через определенные порты, определив порты сервера с помощью диспетчера конфигурации SQL Server и открыв порты в брандмауэре Windows с дополнительной безопасностью.</span><span class="sxs-lookup"><span data-stu-id="af708-110">Before you create the Front End pool, you must also configure Windows Firewall to allow Lync Server 2013 access to SQL Server over specific ports by defining ports for the server using SQL Server Configuration Manager and opening ports in Windows Firewall with Advanced Security.</span></span>

<span data-ttu-id="af708-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af708-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

