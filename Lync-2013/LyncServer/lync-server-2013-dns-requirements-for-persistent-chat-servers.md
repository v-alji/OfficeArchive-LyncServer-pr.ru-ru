---
title: 'Lync Server 2013: требования DNS для хранимых серверов чата'
description: 'Lync Server 2013: требования DNS для хранимых серверов чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Persistent Chat Servers
ms:assetid: f7531374-d7ed-4b63-ae81-02294cb4496a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205391(v=OCS.15)
ms:contentKeyID: 48185857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01bfc126ab588542ef5160a0eabe0c839dcf0e44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429058"
---
# <a name="dns-requirements-for-persistent-chat-servers-in-lync-server-2013"></a><span data-ttu-id="0409c-103">Требования DNS к сохраняемым серверам чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0409c-103">DNS requirements for Persistent Chat Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0409c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0409c-104">

<span> </span></span></span>

<span data-ttu-id="0409c-105">_**Тема последнего изменения:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="0409c-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="0409c-106">В этом разделе описаны записи DNS, необходимые для развертывания сохраненных серверов чата.</span><span class="sxs-lookup"><span data-stu-id="0409c-106">This section describes the Domain Name System (DNS) records that are required for deployment of Persistent Chat Servers.</span></span>

<div>

## <a name="dns-records-for-persistent-chat-servers"></a><span data-ttu-id="0409c-107">Записи DNS для постоянных серверов чата</span><span class="sxs-lookup"><span data-stu-id="0409c-107">DNS Records for Persistent Chat Servers</span></span>

<span data-ttu-id="0409c-108">В приведенной ниже таблице указаны требования DNS для развертывания сервера для сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="0409c-108">The following table specifies DNS requirements for Persistent Chat Server deployment.</span></span>

### <a name="dns-requirements-for-a-persistent-chat-server"></a><span data-ttu-id="0409c-109">Требования к DNS для сервера сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="0409c-109">DNS Requirements for a Persistent Chat Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0409c-110">Сценарий развертывания</span><span class="sxs-lookup"><span data-stu-id="0409c-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="0409c-111">Требование DNS</span><span class="sxs-lookup"><span data-stu-id="0409c-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0409c-112">Один сервер сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="0409c-112">One Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="0409c-113">Внутренняя запись A, разрешающая полное доменное имя сервера в IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0409c-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0409c-114">Пул сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="0409c-114">Persistent Chat pool</span></span></p></td>
<td><p><span data-ttu-id="0409c-115">Внутренняя запись, разрешающая полное доменное имя (FQDN) серверов в свой IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0409c-115">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="0409c-116"><strong>Пример</strong></span><span class="sxs-lookup"><span data-stu-id="0409c-116"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="0409c-117">PersistentChatServer01.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="0409c-117">PersistentChatServer01.contoso.com     10.10.10.1</span></span></p>
<p><span data-ttu-id="0409c-118">PersistentChatServer02.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="0409c-118">PersistentChatServer02.contoso.com     10.10.10.2</span></span></p>
<p><span data-ttu-id="0409c-119">Внутренняя запись, разрешающая полное доменное имя (FQDN) серверов в свой IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0409c-119">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="0409c-120"><strong>Пример</strong></span><span class="sxs-lookup"><span data-stu-id="0409c-120"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="0409c-121">PersistentChatPool.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="0409c-121">PersistentChatPool.contoso.com    10.10.10.1</span></span></p>
<p><span data-ttu-id="0409c-122">PersistentChatPool.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="0409c-122">PersistentChatPool.contoso.com    10.10.10.2</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0409c-123">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0409c-123">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

