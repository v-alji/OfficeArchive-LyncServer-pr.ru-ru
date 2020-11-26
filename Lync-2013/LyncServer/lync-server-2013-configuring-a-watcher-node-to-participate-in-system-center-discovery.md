---
title: Настройка узла-наблюдателя для участия в обнаружении System Center
description: Настройка узла-наблюдателя для участия в обнаружении System Center.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to participate in System Center discovery
ms:assetid: 15c5dcfd-603b-47ea-af1b-8714c2ec08af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204704(v=OCS.15)
ms:contentKeyID: 48183500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6a42ae77e0c8bde8b8e4de4461180ad00380a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433473"
---
# <a name="configuring-a-watcher-node-in-lync-server-2013-to-participate-in-system-center-discovery"></a><span data-ttu-id="dbd2f-103">Настройка узла-наблюдателя в Lync Server 2013 для участия в обнаружении System Center</span><span class="sxs-lookup"><span data-stu-id="dbd2f-103">Configuring a watcher node in Lync Server 2013 to participate in System Center discovery</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dbd2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dbd2f-104">

<span> </span></span></span>

<span data-ttu-id="dbd2f-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="dbd2f-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="dbd2f-106">Чтобы убедиться в том, что узел-наблюдатель участвует в процессе обнаружения для System Center Operations Manager, необходимо выполнить описанные ниже действия на компьютере с установленной консолью System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="dbd2f-106">To make sure that your watcher node participates in the discovery process for System Center Operations Manager, you must complete the following procedure on a computer where the System Center Operations Manager console has been installed:</span></span>

1.  <span data-ttu-id="dbd2f-107">На вкладке **Администрирование** выберите пункт **управляемая агентом**.</span><span class="sxs-lookup"><span data-stu-id="dbd2f-107">On the **Administration** tab, click **Agent Managed**.</span></span>

2.  <span data-ttu-id="dbd2f-108">Щелкните правой кнопкой мыши имя компьютера узла-наблюдателя и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="dbd2f-108">Right-click the name of the watcher node computer, and then click **Properties**.</span></span> <span data-ttu-id="dbd2f-109">В диалоговом окне **Свойства** на вкладке **Безопасность** выберите **Разрешить этому агенту выступать в качестве прокси-сервера и найдите управляемые объекты на других компьютерах**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dbd2f-109">In the **Properties** dialog box, on the **Security** tab, select **Allow this agent to act as a proxy and discover managed objects on other computers**, and then click **OK**.</span></span>

<span data-ttu-id="dbd2f-110">После того как вы настраиваете узел наблюдателя для работы в качестве прокси-сервера, перезагрузите компьютер с узлом-наблюдателем.</span><span class="sxs-lookup"><span data-stu-id="dbd2f-110">After configuring the watcher node to act as a proxy, reboot the watcher node computer.</span></span> <span data-ttu-id="dbd2f-111">После перезагрузки компьютера убедитесь в том, что в журнал событий Operations Manager на этом компьютере не записываются события об ошибках.</span><span class="sxs-lookup"><span data-stu-id="dbd2f-111">After the computer has rebooted, verify that no error events are being recorded in the Operations Manager event log on that computer.</span></span> <span data-ttu-id="dbd2f-112">После запуска компьютера в течение 15 минут или с помощью консоли Operations Manager убедитесь, что компьютеры Lync Server указаны в категории **Lync** .</span><span class="sxs-lookup"><span data-stu-id="dbd2f-112">After the computer has been running for 15 minutes or so, use the Operations Manager console to verify that your Lync Server computers are listed under the **Lync** category.</span></span>

<span data-ttu-id="dbd2f-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dbd2f-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

