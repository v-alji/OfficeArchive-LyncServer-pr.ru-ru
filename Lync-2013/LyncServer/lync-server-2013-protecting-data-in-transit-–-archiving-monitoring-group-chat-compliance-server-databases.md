---
title: 'Lync Server 2013: защита данных при передаче — архивирование, мониторинг, группирование баз данных сервера совместимости чатов'
description: 'Lync Server 2013: защита данных в пути — архивирование, отслеживание, группировка баз данных сервера соответствия требованиям группового чата.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436848"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a><span data-ttu-id="0ddc5-103">Защита данных при передаче — архивирование, мониторинг, группирование баз данных сервера совместимости чатов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ddc5-103">Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ddc5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ddc5-104">

<span> </span></span></span>

<span data-ttu-id="0ddc5-105">_**Тема последнего изменения:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="0ddc5-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="0ddc5-106">Microsoft Lync Server 2013 Архивирование сервера и сервера мониторинга используют как служба очереди сообщений (также называемая MSMQ) для сбора и надежного перемещения сообщений данных из коллекции на серверы репозитория.</span><span class="sxs-lookup"><span data-stu-id="0ddc5-106">Microsoft Lync Server 2013 Archiving Server and Monitoring Server both use the Message Queuing (also known as MSMQ) service to collect and reliably move data messages from the collection point to the repository servers.</span></span> <span data-ttu-id="0ddc5-107">Служба соответствия собирает данные вместе с сервером группового чата, который также использует очередь сообщений.</span><span class="sxs-lookup"><span data-stu-id="0ddc5-107">Compliance service collects data in conjunction with the Group Chat Server, which also uses Message Queuing.</span></span>

<span data-ttu-id="0ddc5-108">В Lync Server 2013 отсутствует внутренняя защита для данных по каналу связи. Тем не менее, если требуется защитить этот трафик, служба очереди сообщений может обеспечивать шифрование на уровне сообщений в очереди отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="0ddc5-108">In Lync Server 2013, there is no internal protection for data on the wire; however, if there is a requirement to secure this traffic, the Message Queuing service can provide encryption at a message level on the sending message queue.</span></span> <span data-ttu-id="0ddc5-109">Это делается с помощью сертификатов, управляемых доменными службами Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0ddc5-109">This is accomplished using certificates that are managed by the Active Directory Domain Services.</span></span> <span data-ttu-id="0ddc5-110">Подробные сведения можно найти в статье приложение г: очередь сообщений и связь через Интернет в Windows Server 2008 в [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) или приложении I: очередь сообщений и Интернет-связь в Windows server 2008 R2 [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) для windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0ddc5-110">For details, see Appendix D: Message Queuing and Internet Communication in Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) or Appendix I: Message Queuing and Internet Communication in Windows Server 2008 R2 at [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) for Windows Server 2008 R2.</span></span>

<span data-ttu-id="0ddc5-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ddc5-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

