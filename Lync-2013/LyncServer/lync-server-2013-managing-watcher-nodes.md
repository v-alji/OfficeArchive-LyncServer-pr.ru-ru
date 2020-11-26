---
title: 'Lync Server 2013: Управление узлами наблюдения'
description: 'Lync Server 2013: Управление узлами наблюдения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing watcher nodes
ms:assetid: 66deaf49-a71f-4a6e-ada0-ea8b688ee921
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688078(v=OCS.15)
ms:contentKeyID: 49733674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1795b09bbca73d8157cf796ceeaaeafb9cc2ebc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425831"
---
# <a name="managing-watcher-nodes-in-lync-server-2013"></a><span data-ttu-id="cc946-103">Управление узлами наблюдения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc946-103">Managing watcher nodes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc946-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc946-104">

<span> </span></span></span>

<span data-ttu-id="cc946-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="cc946-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="cc946-106">Помимо изменения искусственных транзакций, которые выполняются на узле-наблюдателе, администраторы также могут использовать командлет **Set-CsWatcherNodeConfiguration** для выполнения двух других важных задач: Включение и отключение узла-наблюдателя, а также настройка узла-наблюдателя на использование внутренних URL или внешних URL-адресов при выполнении тестов.</span><span class="sxs-lookup"><span data-stu-id="cc946-106">In addition to modifying the synthetic transactions that are executed on a watcher node, administrators can also use the **Set-CsWatcherNodeConfiguration** cmdlet to carry out two other important tasks: enabling and disabling the watcher node, and configuring the watcher node to use either internal URLs or external URLs when running its tests.</span></span>

<span data-ttu-id="cc946-107">По умолчанию узлы-наблюдатели периодически запускают все включенные искусственные транзакции.</span><span class="sxs-lookup"><span data-stu-id="cc946-107">By default, watcher nodes are designed to periodically run all their enabled synthetic transactions.</span></span> <span data-ttu-id="cc946-108">Однако иногда вам может потребоваться приостановить эти транзакции.</span><span class="sxs-lookup"><span data-stu-id="cc946-108">Sometimes, however, you may need to suspend those transactions.</span></span> <span data-ttu-id="cc946-109">Например, если узел-наблюдатель временно отключился от сети, у него больше нет причин запускать искусственные транзакции.</span><span class="sxs-lookup"><span data-stu-id="cc946-109">For example, if the watcher node is temporarily disconnected from the network, then there is no reason to run the synthetic transactions.</span></span> <span data-ttu-id="cc946-110">При отсутствии подключения к сети эти транзакции гарантировано завершаются сбоем.</span><span class="sxs-lookup"><span data-stu-id="cc946-110">Without network connectivity, those transactions are guaranteed to fail.</span></span> <span data-ttu-id="cc946-111">Если вы хотите временно отключить узел наблюдателя, выполните следующую команду в командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cc946-111">If you want to temporarily disable a watcher node, run a command similar to this from the Lync Server Management Shell:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -Enabled $False

<span data-ttu-id="cc946-112">Эта команда отключит выполнение виртуальных транзакций на узле наблюдателя ATL-Watch-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="cc946-112">This command will disable the execution of synthetic transactions on the watcher node atl-watcher- 001.litwareinc.com.</span></span> <span data-ttu-id="cc946-113">Чтобы возобновить выполнение искусственных транзакций, снова задайте для свойства Enabled значение True ($True):</span><span class="sxs-lookup"><span data-stu-id="cc946-113">To resume execution of the synthetic transactions, set the Enabled property back to True ($True):</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -Enabled $True

<div>


> [!NOTE]  
> <span data-ttu-id="cc946-p103">Свойство Enabled может использоваться для включения или отключения узлов-наблюдателей. Если нет необходимости временно удалять узел-наблюдатель, используйте командлет <STRONG>Remove-CsWatcherNodeConfiguration</STRONG>:</span><span class="sxs-lookup"><span data-stu-id="cc946-p103">The Enabled property can be used to turn watcher nodes on or off. If you want to permanently delete a watcher node, use the <STRONG>Remove-CsWatcherNodeConfiguration</STRONG> cmdlet:</span></span><BR><span data-ttu-id="cc946-116">Remove-CsWatcherNodeConfiguration — Identity "atl-watcher-001.litwareinc.com"</span><span class="sxs-lookup"><span data-stu-id="cc946-116">Remove-CsWatcherNodeConfiguration –Identity "atl-watcher-001.litwareinc.com"</span></span><BR><span data-ttu-id="cc946-117">Эта команда удаляет все параметры конфигурации узла-наблюдателя с указанного компьютера, что предотвращает автоматическое выполнение виртуальных транзакций на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cc946-117">That command removes all the watcher node configuration settings from the specified computer, which prevents the computer from automatically running synthetic transactions.</span></span> <span data-ttu-id="cc946-118">Тем не менее, команда не удаляет файлы агента System Center и системные файлы Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc946-118">However, the command does not uninstall the System Center agent files or the Lync Server 2013 system files.</span></span>



</div>

<span data-ttu-id="cc946-119">По умолчанию узлы-наблюдатели используют внешние URL-адреса организации при проведении тестов.</span><span class="sxs-lookup"><span data-stu-id="cc946-119">By default, watcher nodes use an organization's external URLs when conducting their tests.</span></span> <span data-ttu-id="cc946-120">Однако узлы-наблюдатели также могут быть настроены на использование внутренних URL в Организации.</span><span class="sxs-lookup"><span data-stu-id="cc946-120">However, watcher nodes can also be configured to use the organization's internal URLs.</span></span> <span data-ttu-id="cc946-121">Это позволит администраторам проверить доступ к URL-адресам тех пользователей, которые находятся внутри сети периметра.</span><span class="sxs-lookup"><span data-stu-id="cc946-121">This enables administrators to verify URL access for users located inside the perimeter network.</span></span> <span data-ttu-id="cc946-122">Чтобы настроить узел наблюдателя для использования внутренних URL-адресов вместо внешних URL-адресов, задайте для свойства UseInternalWebUrls значение true ($True):</span><span class="sxs-lookup"><span data-stu-id="cc946-122">To configure a watcher node to use internal URLs instead of external URLs, set the UseInternalWebUrls property to True ($True):</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -UseInternalWebUrls $True

<span data-ttu-id="cc946-123">Если вы переустановили для этого свойства значение по умолчанию, равное false ($False), наблюдатель будет использовать внешние URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="cc946-123">If you reset this property to the default value of False ($False), the watcher will then use the external URLs:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -UseInternalWebUrls $False

<span data-ttu-id="cc946-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc946-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

