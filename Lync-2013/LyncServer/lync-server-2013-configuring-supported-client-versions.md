---
title: 'Lync Server 2013: Настройка поддерживаемых версий клиента'
description: 'Lync Server 2013: Настройка поддерживаемых версий клиентов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring supported client versions
ms:assetid: aebf7b48-9aa2-4a06-adc5-0c9d11b6358d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412832(v=OCS.15)
ms:contentKeyID: 48185137
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74396314cae864fae134531b71375c750be8d3da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432599"
---
# <a name="configuring-supported-client-versions-in-lync-server-2013"></a><span data-ttu-id="6f5e4-103">Настройка поддерживаемых клиентских версий в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f5e4-103">Configuring supported client versions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f5e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f5e4-104">

<span> </span></span></span>

<span data-ttu-id="6f5e4-105">_**Тема последнего изменения:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="6f5e4-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="6f5e4-106">В Lync Server 2013 можно настроить политики версии клиента, чтобы указать версии клиентов, которые поддерживаются в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-106">In Lync Server 2013, you can set up client version policies to specify the versions of clients that are supported in your environment.</span></span> <span data-ttu-id="6f5e4-107">Кроме того, вы можете использовать конфигурацию глобальной версии клиента, чтобы указать действие по умолчанию для клиентов, у которых нет определенной политики версий, и поэтому они явно не поддерживаются или не ограничены.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-107">Additionally, you can use the global client version configuration to specify a default action for clients that do not already have a version policy defined and, therefore, are not explicitly supported or restricted.</span></span>

<span data-ttu-id="6f5e4-108">Вы также можете использовать политики версии клиента для управления обновлениями клиентов.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-108">You can also use client version policies to manage client updates.</span></span> <span data-ttu-id="6f5e4-109">Если вы настроили политику версии клиента и с помощью параметров **разрешены и обновлены** и **заблокированы и обновлены**, клиенты будут получать обновленное программное обеспечение от службы обновления Windows Server (если вы используете эту службу) или из центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-109">When you set a client version policy and use the options **Allow and upgrade** and **Block and upgrade**, clients will receive updated software from the Windows Server Update Service (if you are using this service) or from Microsoft Update.</span></span>

<div>

## <a name="client-version-policy-settings"></a><span data-ttu-id="6f5e4-110">Параметры политики версии клиента</span><span class="sxs-lookup"><span data-stu-id="6f5e4-110">Client Version Policy Settings</span></span>

<span data-ttu-id="6f5e4-111">Политика версии клиента по умолчанию требует, чтобы все клиенты выполняли Lync.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-111">The default client version policy requires that all clients run Lync.</span></span> <span data-ttu-id="6f5e4-112">Если на клиентах вашей среды запущены более ранние версии Communicator, может потребоваться перенастройка правил клиентской версии, чтобы предотвратить неожиданное блокирование и обновление клиентов и устройств при подключении к Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-112">If clients in your environment are running earlier versions of Communicator, you may need to reconfigure the Client Version rules to prevent clients and devices from being unexpectedly blocked or updated when connecting to Lync Server 2013.</span></span> <span data-ttu-id="6f5e4-113">Вы можете изменить правило по умолчанию или добавить правило, находящихся выше в списке политики версии клиента, для переопределения правила по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-113">You can modify the default rule, or you can add a rule higher in the Client Version Policy list to override the default rule.</span></span> <span data-ttu-id="6f5e4-114">Кроме того, как выпускаются накопительные обновления (CUs), необходимо настроить политику версии клиента, чтобы затребовать последние обновления.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-114">Additionally, as Cumulative Updates (CUs) are released, you should configure the Client Version Policy to require the latest updates.</span></span> <span data-ttu-id="6f5e4-115">Подробные сведения о том, как [указать клиентские приложения, которые можно использовать для входа на Lync Server 2013,](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md) находятся в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-115">For details, see [Specifying the client applications that can be used to log on to Lync Server 2013](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md) in the Operations documentation.</span></span>

<span data-ttu-id="6f5e4-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f5e4-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

