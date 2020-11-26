---
title: 'Lync Server 2013: отработка отказа для пограничного пула, используемого для федерации XMPP'
description: 'Lync Server 2013: сбой в пуле EDGE, используемом для XMPP Федерации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for XMPP federation
ms:assetid: 587e7829-a26b-46f8-8aad-b78a7b325b55
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688065(v=OCS.15)
ms:contentKeyID: 49733659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccdfe119258b4d09ddedefb22d0272d72003bf04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428253"
---
# <a name="failing-over-the-edge-pool-used-for-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="c654a-103">Отработка отказа для пограничного пула, используемого для федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c654a-103">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c654a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c654a-104">

<span> </span></span></span>

<span data-ttu-id="c654a-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="c654a-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="c654a-106">В вашей организации используется один пул краев, назначенный пулом для XMPP Федерации.</span><span class="sxs-lookup"><span data-stu-id="c654a-106">In your organization, there is one Edge pool designated as the pool to use for XMPP federation.</span></span> <span data-ttu-id="c654a-107">Если этот пул отключается, необходимо отдать отказ на XMPP Федерацию для использования другого пула Edge перед тем, как XMPP Федерация сможет снова работать.</span><span class="sxs-lookup"><span data-stu-id="c654a-107">If this pool goes down, you must fail over XMPP federation to use a different Edge pool before XMPP federation can work again.</span></span>

<span data-ttu-id="c654a-108">После установки пулов EDGE и включения XMPP Федерации вы можете упростить процесс аварийного восстановления, настроив внешние записи DNS SRV для всех пулов Edge для XMPP Федерации, а не только для одной из них.</span><span class="sxs-lookup"><span data-stu-id="c654a-108">When you first install Edge pools and enable XMPP Federation, you can simplify the disaster recovery process by setting up external DNS SRV records for all of your Edge pools for XMPP federation, instead of just one.</span></span> <span data-ttu-id="c654a-109">Для каждой из этих записей SRV должен быть установлен другой приоритет.</span><span class="sxs-lookup"><span data-stu-id="c654a-109">Each of these SRV records must have a different priority set.</span></span> <span data-ttu-id="c654a-110">Весь трафик Федерации XMPP проходит через пул с записью SRV с самым высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="c654a-110">All XMPP federation traffic goes through the pool with the SRV record with the highest priority.</span></span> <span data-ttu-id="c654a-111">Дополнительные сведения о том, как включить и настроить федерацию XMPP, можно найти [в разделе Настройка XMPP Федерации в Lync Server 2013](lync-server-2013-setting-up-xmpp-federation.md).</span><span class="sxs-lookup"><span data-stu-id="c654a-111">For more information on enabling and setting up XMPP federation, see [Setting up XMPP federation in Lync Server 2013](lync-server-2013-setting-up-xmpp-federation.md).</span></span>

<span data-ttu-id="c654a-112">В описанной ниже процедуре EdgePool1 — пул, изначально размещенный XMPP Federation, и EdgePool2 — пул, который теперь будет размещен XMPP Федерации.</span><span class="sxs-lookup"><span data-stu-id="c654a-112">In the following procedure, EdgePool1 is the pool which originally hosted XMPP federation, and EdgePool2 is the pool which will now host XMPP federation.</span></span>

<div>

## <a name="failing-over-the-edge-pool-used-for-xmpp-federation"></a><span data-ttu-id="c654a-113">Сбой в пуле EDGE, используемом для Федерации XMPP</span><span class="sxs-lookup"><span data-stu-id="c654a-113">Failing Over the Edge Pool Used for XMPP Federation</span></span>

1.  <span data-ttu-id="c654a-114">Если вы еще не развернули другой пул пограничных кромок (Кроме того, который в данный момент не работает), разверните этот пул.</span><span class="sxs-lookup"><span data-stu-id="c654a-114">If you don’t already have another Edge pool deployed (besides the one which is currently down), deploy that pool.</span></span> <span data-ttu-id="c654a-115">Подробные сведения можно найти [в разделе Развертывание внешних пользователей Access в Lync Server 2013](lync-server-2013-deploying-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="c654a-115">For details, see [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md).</span></span>

2.  <span data-ttu-id="c654a-116">На каждом пограничном сервере в новом пограничном пуле, на котором будет размещена XMPP Федерация (EdgePool2), запустите следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="c654a-116">On each Edge Server in the new Edge pool which will now host XMPP federation (EdgePool2), run the following cmdlet:</span></span>
    
        Stop-CsWindowsService

3.  <span data-ttu-id="c654a-117">Чтобы перенаправить маршрут Федерации XMPP на EdgePool2, выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="c654a-117">Run the following cmdlet to repoint the XMPP federation route to EdgePool2:</span></span>
    
        Set-CsSite Site2 -XmppExternalFederationRoute EdgeServer2.contoso.com
    
    <span data-ttu-id="c654a-118">В этом примере Site2 — сайт с пулом EDGE, который теперь будет размещаться на маршруте Федерации XMPP, а EdgeServer2.contoso.com — это полное доменное имя пограничного сервера в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="c654a-118">In this example, Site2 is the site containing the Edge pool which will now host the XMPP federation route, and EdgeServer2.contoso.com is the FQDN of an Edge Server in that pool.</span></span>

4.  <span data-ttu-id="c654a-119">На внешнем DNS-сервере измените запись DNS A для Федерации XMPP, чтобы она указывала на EdgeServer2.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c654a-119">On the external DNS server, change the DNS A record for XMPP federation to point to EdgeServer2.contoso.com.</span></span>

5.  <span data-ttu-id="c654a-120">Если у вас еще нет DNS-записи SRV для Федерации XMPP, которая разрешается в пул EDGE, который теперь будет размещаться в XMPP Федерации, необходимо добавить его, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="c654a-120">If you do not already have a DNS SRV record for XMPP federation which resolves to the Edge pool which will now host XMPP federation, you must add it, as in the following example.</span></span> <span data-ttu-id="c654a-121">Для этой записи SRV должно быть задано значение Port 5269.</span><span class="sxs-lookup"><span data-stu-id="c654a-121">This SRV record must have a port value of 5269.</span></span>
    
        _xmpp-server._tcp.contoso.com

6.  <span data-ttu-id="c654a-122">Убедитесь, что в пуле EDGE, на котором будет размещена XMPP Федерация, есть порт 5269, Открытый извне.</span><span class="sxs-lookup"><span data-stu-id="c654a-122">Verify that the Edge pool which will now host XMPP federation has port 5269 open externally.</span></span>

7.  <span data-ttu-id="c654a-123">Запустите службы на всех пограничных серверах в пограничном пуле, где будет размещаться Федерация XMPP:</span><span class="sxs-lookup"><span data-stu-id="c654a-123">Start the services on all Edge Servers in the Edge pool which will now host XMPP federation:</span></span>
    
        Start-CsWindowsService

<span data-ttu-id="c654a-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c654a-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

