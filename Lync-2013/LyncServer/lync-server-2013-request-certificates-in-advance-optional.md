---
title: 'Lync Server 2013: заблаговременный запрос сертификатов (необязательно)'
description: 'Lync Server 2013: запрашивать сертификаты заранее (необязательно).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Request certificates in advance (optional)
ms:assetid: 9d6d7de6-ff2a-46da-b1b7-a354c8e383e4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412733(v=OCS.15)
ms:contentKeyID: 48184915
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92ac9b68012487d07f25f08649689611117202
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442721"
---
# <a name="request-certificates-in-advance-optional-for-lync-server-2013"></a><span data-ttu-id="ef538-103">Заблаговременный запрос сертификатов для Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="ef538-103">Request certificates in advance (optional) for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef538-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef538-104">

<span> </span></span></span>

<span data-ttu-id="ef538-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ef538-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ef538-106">Сертификаты необходимы для всех внутренних серверов, на которых работает Lync Server 2013, включая каждый сервер переднего плана Enterprise Edition, сервер Standard Edition, режиссер, пограничный сервер и изолированный сервер-посредник.</span><span class="sxs-lookup"><span data-stu-id="ef538-106">Certificates are required for all internal servers that are running Lync Server 2013, including each Enterprise Edition Front End Server, Standard Edition server, Director, Edge Server and stand-alone Mediation Server.</span></span> <span data-ttu-id="ef538-107">Несмотря на то, что для внутренних серверов рекомендуется использовать внутренний центр сертификации (ЦС) предприятия, вы также можете воспользоваться общедоступным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="ef538-107">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="ef538-108">Сведения о требованиях к сертификатам и об использовании общедоступного центра сертификации можно найти в разделе [требования к сертификатам внутренних серверов в Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="ef538-108">For details about certificate requirements and about the use of a public CA, see [Certificate requirements for internal servers in Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) in the Planning documentation.</span></span>

<span data-ttu-id="ef538-109">Lync Server 2013 Setup включает мастер сертификатов, который упрощает задачи запроса, назначения и установки сертификатов во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="ef538-109">Lync Server 2013 setup includes the Certificate Wizard, which facilitates the tasks of requesting, assigning, and installing certificates during deployment.</span></span> <span data-ttu-id="ef538-110">Если вы хотите запросить сертификаты перед установкой серверов (например, для экономии времени на реальном развертывании серверов), это можно сделать с помощью компьютера, на котором установлены средства администрирования Lync Server 2013, или с помощью процедуры запроса сертификата, определенной в вашей организации, при условии, что сертификаты будут экспортированы и содержат все необходимые дополнительные имена субъектов.</span><span class="sxs-lookup"><span data-stu-id="ef538-110">If you want to request certificates prior to installing servers (for instance, to save time during actual deployment of servers), you can do so by using a computer on which the Lync Server 2013 administrative tools are installed or by using a certificate request procedure defined in your organization, as long as you make sure that the certificates are exportable and contain all the required subject alternative names.</span></span> <span data-ttu-id="ef538-111">Предварительный запрос сертификатов не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ef538-111">Requesting certificates in advance is optional.</span></span> <span data-ttu-id="ef538-112">Если вы не запрашиваете их заранее, вы должны запросить их в ходе настройки каждого сервера, которому требуется сертификат.</span><span class="sxs-lookup"><span data-stu-id="ef538-112">If you do not request them in advance, you must request them as part of the setup of each server that requires a certificate.</span></span>

<span data-ttu-id="ef538-113">В этой документации по развертыванию содержатся инструкции по использованию мастера сертификатов для запроса сертификатов в процессе установки, как описано в разделе [Настройка сертификатов для сервера в Lync server 2013](lync-server-2013-configure-certificates-for-servers.md), [Настройка сертификатов для режиссера](lync-server-2013-configure-certificates-for-the-director.md)в Lync сервер 2013 и [Установка сервера исправлений в Lync Server 2013 в](lync-server-2013-install-the-files-for-mediation-server.md) разделах этой документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="ef538-113">This Deployment documentation provides procedures for using the Certificate Wizard to request certificates as part of the setup process, as described in the [Configure certificates for servers in Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md), [Configure certificates for the Director in Lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md), and [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md) sections of this Deployment documentation.</span></span> <span data-ttu-id="ef538-114">Если вы захотите предварительно запросить сертификаты, вы должны изменить процедуры развертывания сертификата в этих разделах так, чтобы они были импортированы и назначены для импорта и назначения сертификатов, а не для их запроса во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="ef538-114">If you request certificates in advance, you must modify the certificate deployment procedures in those sections as appropriate to importing and assigning the certificates instead of requesting them at the time of deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ef538-115">Lync Server 2013 включает поддержку сертификатов SHA-256 для подключений клиентов, работающих под управлением операционных систем Windows Vista, Windows Server &nbsp; 2008, Windows server &nbsp; 2008 &nbsp; R2 и Windows 7, а также Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="ef538-115">Lync Server 2013 includes support for SHA-256 certificates for connections from clients running the Windows Vista, Windows Server&nbsp;2008, Windows Server&nbsp;2008&nbsp;R2, and Windows 7 operating systems, and Lync Phone Edition.</span></span> <span data-ttu-id="ef538-116">Для поддержки внешнего доступа с помощью SHA-256 внешний сертификат выдается общедоступным центром сертификации с помощью SHA-256.</span><span class="sxs-lookup"><span data-stu-id="ef538-116">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>



<span data-ttu-id="ef538-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef538-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

