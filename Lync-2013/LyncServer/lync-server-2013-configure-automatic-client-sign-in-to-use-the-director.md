---
title: 'Lync Server 2013: настройка автоматического входа клиента для использования директора'
description: 'Lync Server 2013: Настройка автоматических клиентских Sign-In для использования режиссера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Automatic Client Sign-In to use the Director
ms:assetid: 85369ffc-53ae-43be-8a23-84a094faecff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398678(v=OCS.15)
ms:contentKeyID: 48184703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9c45a1a677d3a30704d8dca1771ef865cef29ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399619"
---
# <a name="configure-automatic-client-sign-in-to-use-the-director-in-lync-server-2013"></a><span data-ttu-id="08c96-103">Настройка автоматического входа клиента для использования директора в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="08c96-103">Configure Automatic Client Sign-In to use the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="08c96-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="08c96-104">

<span> </span></span></span>

<span data-ttu-id="08c96-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="08c96-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="08c96-106">При развертывании Lync Server 2013, Director или пула директоров рекомендуется использовать функцию автоматического клиентского Sign-In.</span><span class="sxs-lookup"><span data-stu-id="08c96-106">When you deploy a Lync Server 2013, Director or a pool of Directors, we recommend that you use Automatic Client Sign-In as a best practice.</span></span> <span data-ttu-id="08c96-107">Дополнительные сведения о том, как настроить DNS-серверы для автоматического входа в клиент, приведены в разделе [требования к DNS для автоматического входа в службу в Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="08c96-107">For details about how to configure DNS servers for automatic client sign-in, see [DNS requirements for automatic client sign-in in Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) in the Planning documentation.</span></span>

<span data-ttu-id="08c96-108">Если вы уже развернули функцию автоматического входа в систему, ознакомьтесь со следующими разделами, чтобы настроить ее для вашего режиссера (-ов).</span><span class="sxs-lookup"><span data-stu-id="08c96-108">If you have already deployed Automatic Client Sign-In, see the following sections to configure it on your Director(s).</span></span>

<div>

## <a name="single-director-instance"></a><span data-ttu-id="08c96-109">Один экземпляр режиссера</span><span class="sxs-lookup"><span data-stu-id="08c96-109">Single Director Instance</span></span>

<span data-ttu-id="08c96-110">Если вы уже развернули клиентские Sign-In с автоматическим подключением и указываете на сервер переднего плана или пул переднего плана, вам нужно изменить DNS-запись SRV, чтобы она указывала на режиссер.</span><span class="sxs-lookup"><span data-stu-id="08c96-110">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director.</span></span>

</div>

<div>

## <a name="director-pool"></a><span data-ttu-id="08c96-111">Пул режиссеров</span><span class="sxs-lookup"><span data-stu-id="08c96-111">Director Pool</span></span>

<span data-ttu-id="08c96-112">Если вы уже развернули автоматически клиентские Sign-In и указываете на сервер переднего плана или пул переднего плана, вам нужно изменить DNS-запись SRV, чтобы она указывала на этот пул.</span><span class="sxs-lookup"><span data-stu-id="08c96-112">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director pool.</span></span>

<span data-ttu-id="08c96-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="08c96-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

