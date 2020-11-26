---
title: 'Lync Server 2013: прямые соединения SIP'
description: 'Lync Server 2013: прямые соединения SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Direct SIP connections
ms:assetid: 0a37737d-9628-4e36-b27b-c134fa5a3882
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398151(v=OCS.15)
ms:contentKeyID: 48183357
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebc42cd26472bbb19c7ef886a9449ab453b90680
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429135"
---
# <a name="direct-sip-connections-in-lync-server-2013"></a><span data-ttu-id="1c7f5-103">Прямые подключения по протоколу SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c7f5-103">Direct SIP connections in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c7f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c7f5-104">

<span> </span></span></span>

<span data-ttu-id="1c7f5-105">_**Тема последнего изменения:** 2012-08-13_</span><span class="sxs-lookup"><span data-stu-id="1c7f5-105">_**Topic Last Modified:** 2012-08-13_</span></span>

<span data-ttu-id="1c7f5-106">Вы можете использовать *прямые подключения* по протоколу SIP, чтобы подключить сервер Lync Server к одной из указанных ниже учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1c7f5-106">You can use *direct SIP connections* to connect Lync Server to either of the following:</span></span>

  - <span data-ttu-id="1c7f5-107">IP-УАТС (Дополнительные сведения можно найти [в разделе Параметры развертывания Direct SIP в Lync Server 2013](lync-server-2013-direct-sip-deployment-options.md)).</span><span class="sxs-lookup"><span data-stu-id="1c7f5-107">An IP-PBX (for details, see [Direct SIP deployment options in Lync Server 2013](lync-server-2013-direct-sip-deployment-options.md)).</span></span>

  - <span data-ttu-id="1c7f5-108">Шлюз PSTN (Дополнительные сведения можно найти [в разделе Параметры развертывания шлюза PSTN в Lync Server 2013](lync-server-2013-pstn-gateway-deployment-options.md)).</span><span class="sxs-lookup"><span data-stu-id="1c7f5-108">A PSTN gateway (for details, see [PSTN gateway deployment options in Lync Server 2013](lync-server-2013-pstn-gateway-deployment-options.md)).</span></span>

<span data-ttu-id="1c7f5-109">Чтобы реализовать прямую связь по SIP, необходимо выполнить, по существу, те же действия по развертыванию, что и при реализации магистрали SIP.</span><span class="sxs-lookup"><span data-stu-id="1c7f5-109">To implement a direct SIP connection, you follow essentially the same deployment steps as you would to implement a SIP trunk.</span></span> <span data-ttu-id="1c7f5-110">В обоих случаях подключение реализуется с помощью внешнего интерфейса сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="1c7f5-110">In both cases, you implement the connection by using the external interface of a Mediation Server.</span></span> <span data-ttu-id="1c7f5-111">Единственное отличие заключается в том, что магистрали SIP подключаются к внешнему объекту, например шлюзу поставщика услуг Интернет-телефонии, а прямая связь по SIP устанавливается путем подключения к внутреннему объекту локальной сети, например к IP-УАТС или шлюзу телефонной сети общего пользования (ТСОП).</span><span class="sxs-lookup"><span data-stu-id="1c7f5-111">The only difference is that you connect SIP trunks to an external entity, such as an ITSP gateway, and you connect direct SIP connections to an internal entity within your local network, such as an IP-PBX or a public switched telephone network (PSTN) gateway.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1c7f5-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="1c7f5-112">In This Section</span></span>

  - [<span data-ttu-id="1c7f5-113">Варианты развертывания прямого SIP-подключения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c7f5-113">Direct SIP deployment options in Lync Server 2013</span></span>](lync-server-2013-direct-sip-deployment-options.md)

  - [<span data-ttu-id="1c7f5-114">Параметры развертывания шлюза ТСОП в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c7f5-114">PSTN gateway deployment options in Lync Server 2013</span></span>](lync-server-2013-pstn-gateway-deployment-options.md)

<span data-ttu-id="1c7f5-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c7f5-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

