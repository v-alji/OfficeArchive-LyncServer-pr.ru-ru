---
title: 'Lync Server 2013: отработка отказа для пограничного пула, используемого для федерации Lync Server'
description: 'Lync Server 2013: Сбой пограничного пула EDGE, используемого для Lync Server Federation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for Lync Server federation
ms:assetid: 5c9da0f2-7429-40bb-bb3c-5cc4ecb5a13d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688071(v=OCS.15)
ms:contentKeyID: 49733665
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1e7e13ccd35a653d38174f55ace9dc6637ded04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398470"
---
# <a name="failing-over-the-edge-pool-used-for-lync-server-federation-in-lync-server-2013"></a><span data-ttu-id="fa493-103">Отработка отказа для пограничного пула, используемого для федерации Lync Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa493-103">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa493-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa493-104">

<span> </span></span></span>

<span data-ttu-id="fa493-105">_**Тема последнего изменения:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="fa493-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="fa493-106">Если пул пограничного пула, на котором настроена сервер Lync Server Federation, не работает, необходимо изменить Федерацию для использования другого пула Edge для работы Федерации.</span><span class="sxs-lookup"><span data-stu-id="fa493-106">If the Edge pool where you have Lync Server federation configured goes down, you must change federation to use a different Edge pool for federation to work.</span></span>

<div>

## <a name="failing-over-the-edge-pool-used-for-lync-server-federation"></a><span data-ttu-id="fa493-107">Сбой в пуле EDGE, используемом для интеграции с Lync Server</span><span class="sxs-lookup"><span data-stu-id="fa493-107">Failing Over the Edge Pool Used for Lync Server Federation</span></span>

1.  <span data-ttu-id="fa493-108">На сервере переднего плана откройте окно Построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="fa493-108">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="fa493-109">Разверните узел **Edge** Pools, а затем щелкните правой кнопкой мыши граничный сервер пограничного сервера или пул пограничного сервера, настроенный на данный момент для Федерации.</span><span class="sxs-lookup"><span data-stu-id="fa493-109">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="fa493-110">Нажмите кнопку **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="fa493-110">Select **Edit properties**.</span></span>

2.  <span data-ttu-id="fa493-111">В диалоговом окне **изменение свойств** в разделе **Общие** снимите флажок **включить федерацию для этого пограничного пула (порт 5061)**.</span><span class="sxs-lookup"><span data-stu-id="fa493-111">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="fa493-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fa493-112">Click **OK**.</span></span>

3.  <span data-ttu-id="fa493-113">Разверните узел **Edge** Pools, а затем щелкните правой кнопкой мыши граничный сервер пограничного сервера или пул пограничного сервера, который вы хотите использовать для Федерации.</span><span class="sxs-lookup"><span data-stu-id="fa493-113">Expand **Edge pools**, then right click the Edge server or Edge server pool that you now want to use for Federation.</span></span> <span data-ttu-id="fa493-114">Нажмите кнопку **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="fa493-114">Select **Edit properties**.</span></span>

4.  <span data-ttu-id="fa493-115">В диалоговом окне **изменение свойств** в разделе **Общие** установите флажок **включить федерацию для этого пограничного пула (порт 5061)**.</span><span class="sxs-lookup"><span data-stu-id="fa493-115">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="fa493-116">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fa493-116">Click **OK**.</span></span>

5.  <span data-ttu-id="fa493-117">Нажмите кнопку **действие**, выберите пункт **топология**, нажмите кнопку **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="fa493-117">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="fa493-118">При появлении запроса на **публикацию топологии** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fa493-118">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="fa493-119">Завершив публикацию, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="fa493-119">When the Publish is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="fa493-120">На пограничном сервере откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fa493-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="fa493-121">Щелкните **Установка или обновление операционной системы Lync Server**, а затем нажмите кнопку **Настройка или удалите компоненты Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="fa493-121">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="fa493-122">Нажмите кнопку **выполнить еще раз**.</span><span class="sxs-lookup"><span data-stu-id="fa493-122">Click **Run Again**.</span></span>

7.  <span data-ttu-id="fa493-123">В разделе Настройка серверных компонентов Lync нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fa493-123">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="fa493-124">На экране сводки будут показаны действия по мере их выполнения.</span><span class="sxs-lookup"><span data-stu-id="fa493-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="fa493-125">После завершения развертывания щелкните **Просмотреть журнал** , чтобы просмотреть доступные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="fa493-125">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="fa493-126">Нажмите кнопку **Готово** , чтобы завершить развертывание.</span><span class="sxs-lookup"><span data-stu-id="fa493-126">Click **Finish** to complete the deployment.</span></span>
    
    <span data-ttu-id="fa493-127">Если сайт, содержащий неисправный пул, содержит серверы переднего плана, которые еще не запущены, для использования пула EDGE на удаленном сайте, который еще не работает, необходимо обновить службу веб-конференций и службу Конференции/V на этих интерфейсных пулах.</span><span class="sxs-lookup"><span data-stu-id="fa493-127">If the site containing the failed Edge pool contains Front End Servers that are still running, you must update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to use an Edge pool in a remote site that is still running.</span></span> <span data-ttu-id="fa493-128">Дополнительные сведения можно найти [в разделе Изменение пула EDGE, связанного с пулом переднего плана в Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="fa493-128">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fa493-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fa493-129">See Also</span></span>


[<span data-ttu-id="fa493-130">Отработка отказа для пограничного пула, используемого для федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa493-130">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  
[<span data-ttu-id="fa493-131">Отработка отказа для пограничного пула, используемого для федерации Lync Server или федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa493-131">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation.md)  


[<span data-ttu-id="fa493-132">Аварийное восстановление пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa493-132">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="fa493-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa493-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

