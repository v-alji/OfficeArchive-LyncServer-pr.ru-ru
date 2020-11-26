---
title: 'Lync Server 2013: доступ к данным наблюдения'
description: 'Lync Server 2013: доступ к данным мониторинга.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Accessing monitoring data
ms:assetid: 845385ca-5532-4fa2-91b9-51c6de6fec91
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688116(v=OCS.15)
ms:contentKeyID: 49733714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c183a66c98072f2ab30bb49e561f9f95c753142f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439501"
---
# <a name="accessing-monitoring-data-in-lync-server-2013"></a><span data-ttu-id="5c620-103">Доступ к данным мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c620-103">Accessing monitoring data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c620-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c620-104">

<span> </span></span></span>

<span data-ttu-id="5c620-105">_**Тема последнего изменения:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="5c620-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="5c620-p101">Данные мониторинга хранятся в двух базах данных SQL Server: LcsCdr для данных регистрации звонков и QoEMetrics для данных качества взаимодействия. Эти базы данных ничем особенным не выделяются, т. е. доступ к данным в них можно получить с помощью любого средства, которое вы обычно используете для просмотра и анализа данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c620-p101">Monitoring data is stored in a pair of SQL Server databases: LcsCdr for call detail recording data, and QoEMetrics for Quality of Experience data. There is nothing special about these two databases; that means that the data stored in those databases can be accessed using any of the tools you typically use for accessing and analyzing SQL Server data.</span></span>

<span data-ttu-id="5c620-108">Для получения доступа к данным наблюдения и анализа данных мониторинга необходимо предусмотреть один из инструментов, которые являются отчетами мониторинга Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5c620-108">One tool you should consider for accessing and analyzing monitoring data is the Lync Server Monitoring Reports.</span></span> <span data-ttu-id="5c620-109">Отчеты мониторинга — это набор стандартных отчетов, публикуемых службой Microsoft SQL Server Reporting Service.</span><span class="sxs-lookup"><span data-stu-id="5c620-109">Monitoring Reports are a set of standard reports that are published by Microsoft SQL Server Reporting Service.</span></span> <span data-ttu-id="5c620-110">Эти отчеты, доступные в браузере, предоставляют сведения об использовании, диагностики звонков и качестве медиаданных на основе записей регистрации вызовов (CDR) и качества взаимодействия (QoE) в базе данных CDR и QoE.</span><span class="sxs-lookup"><span data-stu-id="5c620-110">These reports, which are accessible by using a web browser, provide usage, call diagnostic information, and media quality information, all based on call detail recording (CDR) and Quality of Experience (QoE) records stored in the CDR and QoE databases.</span></span> <span data-ttu-id="5c620-111">Отчеты мониторинга поставляются с Lync Server 2013 и могут быть установлены с помощью мастера развертывания Lync Server после установки Lync Server и настройки мониторинга.</span><span class="sxs-lookup"><span data-stu-id="5c620-111">Monitoring Reports ship with Lync Server 2013 and can be installed from the Lync Server Deployment Wizard after Lync Server has been installed and monitoring has been configured.</span></span>

<span data-ttu-id="5c620-p103">Как было отмечено, для отчетов мониторинга требуется служба SQL Server Reporting Service, которую можно установить вместе с SQL Server в любое время после установки SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c620-p103">As noted, Monitoring Reports requires the use of SQL Server Reporting Service. SQL Server Reporting Service can be installed at the same time you install SQL Server or can be installed any time after SQL Server itself has been installed.</span></span>

<span data-ttu-id="5c620-114">Дополнительные сведения можно найти в разделе [Установка сервера Lync server 2013 мониторинг отчетов](lync-server-2013-installing-lync-server-2013-monitoring-reports.md) в руководстве по развертыванию lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5c620-114">For more information, see the topic [Installing Lync Server 2013 Monitoring Reports](lync-server-2013-installing-lync-server-2013-monitoring-reports.md) in the Lync Server 2013 deployment guide.</span></span>

<span data-ttu-id="5c620-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c620-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

