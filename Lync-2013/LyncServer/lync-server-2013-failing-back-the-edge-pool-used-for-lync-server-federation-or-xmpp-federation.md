---
title: Отработка отказа для пограничного пула, используемого для федерации Lync Server или федерации XMPP
description: Не удается вернуть пул EDGE, используемый для Федерации Lync Server Federation или XMPP Federation.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back the Edge pool used for Lync Server federation or XMPP federation
ms:assetid: d40097a1-1bed-44dc-aeb6-0871927ab2b9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721897(v=OCS.15)
ms:contentKeyID: 49733831
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 137910d71de1d6177356e0b7bacbd6d17022d71d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428302"
---
# <a name="failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="aa1cc-103">Отработка отказа для пограничного пула, используемого для федерации Lync Server или федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa1cc-103">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aa1cc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aa1cc-104">

<span> </span></span></span>

<span data-ttu-id="aa1cc-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="aa1cc-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="aa1cc-106">После того как пул пограничного пула, который использовался для размещения Федерации, станет доступен в сети, выполните описанные ниже действия, чтобы восстановить маршрут Федерации Lync Server и/или XMPP Федерации для повторного использования этого восстановленного пограничного пула.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-106">After a failed Edge pool that used to host federation has been brought back online, use this procedure to fail back the Lync Server federation route and/or the XMPP federation route to again use this restored Edge pool.</span></span>

<div>

## <a name="failing-back-federation-to-a-restored-edge-pool"></a><span data-ttu-id="aa1cc-107">Сбой обратной интеграции в восстановленный пул Edge</span><span class="sxs-lookup"><span data-stu-id="aa1cc-107">Failing Back Federation to a Restored Edge Pool</span></span>

1.  <span data-ttu-id="aa1cc-108">В пуле EDGE, который теперь доступен еще раз, запустите службы Edge.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-108">On the Edge pool that is now available again, start the Edge Services.</span></span>

2.  <span data-ttu-id="aa1cc-109">Если вы хотите вернуть маршрут Федерации Lync Server для использования восстановленного пограничного сервера, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-109">If you want to fail back the Lync Server federation route to use the restored Edge Server, do the following:</span></span>
    
      - <span data-ttu-id="aa1cc-110">На сервере переднего плана откройте окно Построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-110">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="aa1cc-111">Разверните узел **Edge** Pools, а затем щелкните правой кнопкой мыши граничный сервер пограничного сервера или пул пограничного сервера, настроенный на данный момент для Федерации.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-111">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="aa1cc-112">Нажмите кнопку **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-112">Select **Edit properties**.</span></span>
    
      - <span data-ttu-id="aa1cc-113">В диалоговом окне **изменение свойств** в разделе **Общие** снимите флажок **включить федерацию для этого пограничного пула (порт 5061)**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-113">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="aa1cc-114">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-114">Click **OK**.</span></span>
    
      - <span data-ttu-id="aa1cc-115">Разверните узел **Edge** Pools, а затем щелкните правой кнопкой мыши исходный сервер пограничного сервера или пул пограничного сервера, который вы снова хотите использовать для Федерации.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-115">Expand **Edge pools**, then right click the original Edge server or Edge server pool that you again want to use for Federation.</span></span> <span data-ttu-id="aa1cc-116">Нажмите кнопку **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-116">Select **Edit properties**.</span></span>
    
      - <span data-ttu-id="aa1cc-117">В диалоговом окне **изменение свойств** в разделе **Общие** установите флажок **включить федерацию для этого пограничного пула (порт 5061)**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-117">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="aa1cc-118">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-118">Click **OK**.</span></span>
    
      - <span data-ttu-id="aa1cc-119">Нажмите кнопку **действие**, выберите пункт **топология**, нажмите кнопку **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-119">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="aa1cc-120">При появлении запроса на **публикацию топологии** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-120">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="aa1cc-121">Завершив публикацию, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-121">When the Publish is finished, click **Finish**.</span></span>
    
      - <span data-ttu-id="aa1cc-122">На пограничном сервере откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-122">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="aa1cc-123">Щелкните **Установка или обновление операционной системы Lync Server**, а затем нажмите кнопку **Настройка или удалите компоненты Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-123">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="aa1cc-124">Нажмите кнопку **выполнить еще раз**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-124">Click **Run Again**.</span></span>
    
      - <span data-ttu-id="aa1cc-125">В разделе Настройка серверных компонентов Lync нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-125">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="aa1cc-126">На экране сводки будут показаны действия по мере их выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-126">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="aa1cc-127">После завершения развертывания щелкните **Просмотреть журнал** , чтобы просмотреть доступные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-127">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="aa1cc-128">Нажмите кнопку **Готово** , чтобы завершить развертывание.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-128">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="aa1cc-129">Если вы хотите восстановить маршрут Федерации XMPP для использования восстановленного пограничного сервера, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-129">If you want to fail back the XMPP federation route to use the restored Edge Server, do the following:</span></span>
    
      - <span data-ttu-id="aa1cc-130">Запустите следующий командлет, чтобы перенаправить маршрут Федерации XMPP на Граничный пул, который будет размещен XMPP Federation (в этом примере — EdgeServer1):</span><span class="sxs-lookup"><span data-stu-id="aa1cc-130">Run the following cmdlet to repoint the XMPP federation route to the Edge pool which will now host XMPP federation (in this example, EdgeServer1):</span></span>
        
            Set-CsSite Site1 -XmppExternalFederationRoute EdgeServer1.contoso.com
        
        <span data-ttu-id="aa1cc-131">В этом примере site1 — сайт с пулом EDGE, который теперь будет размещаться на маршруте Федерации XMPP, а EdgeServer1.contoso.com — это полное доменное имя пограничного сервера в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-131">In this example, Site1 is the site containing the Edge pool which will now host the XMPP federation route, and EdgeServer1.contoso.com is the FQDN of an Edge Server in that pool.</span></span>
    
      - <span data-ttu-id="aa1cc-132">Если у вас еще нет DNS-записи SRV для Федерации XMPP, которая разрешается в пул EDGE, который теперь будет размещаться в XMPP Федерации, необходимо добавить его, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-132">If you do not already have a DNS SRV record for XMPP federation which resolves to the Edge pool which will now host XMPP federation, you must add it, as in the following example.</span></span> <span data-ttu-id="aa1cc-133">Для этой записи SRV должно быть задано значение Port 5269.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-133">This SRV record must have a port value of 5269.</span></span>
        
            _xmpp-server._tcp.contoso.com
    
      - <span data-ttu-id="aa1cc-134">На внешнем DNS-сервере измените запись DNS A для Федерации XMPP, чтобы она указывала на EdgeServer2.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-134">On the external DNS server, change the DNS A record for XMPP federation to point to EdgeServer2.contoso.com.</span></span>
    
      - <span data-ttu-id="aa1cc-135">Убедитесь, что в пуле EDGE, на котором будет размещена XMPP Федерация, есть порт 5269, Открытый извне.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-135">Verify that the Edge pool which will now host XMPP federation has port 5269 open externally.</span></span>

4.  <span data-ttu-id="aa1cc-136">Если на веб-сайте, содержащем пул пограничного сервера, не удалось выполнить все неудачные и восстановленные интерфейсы, следует обновить службу веб-конференций и службу Конференции/V на этих интерфейсных пулах с помощью пулов EDGE на своем локальном сайте.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-136">If the Front End pools remained running in the site containing the Edge pool that failed and has been restored, you should update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to again use the Edge pools at their local site.</span></span> <span data-ttu-id="aa1cc-137">Дополнительные сведения можно найти [в разделе Изменение пула EDGE, связанного с пулом переднего плана в Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="aa1cc-137">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

5.  <span data-ttu-id="aa1cc-138">Если пул переднего плана на сайте, на котором произошла ошибка, также завершился сбоем, вы можете использовать Invoke – CsPoolFailback для возврата пула переднего плана.</span><span class="sxs-lookup"><span data-stu-id="aa1cc-138">If the Front End pool at the same site as the failed Edge pool also failed, you can now use Invoke–CsPoolFailback to fail back the Front End pool.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="aa1cc-139">См. также</span><span class="sxs-lookup"><span data-stu-id="aa1cc-139">See Also</span></span>


[<span data-ttu-id="aa1cc-140">Отработка отказа для пограничного пула, используемого для федерации Lync Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa1cc-140">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md)  
[<span data-ttu-id="aa1cc-141">Отработка отказа для пограничного пула, используемого для федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa1cc-141">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  


[<span data-ttu-id="aa1cc-142">Аварийное восстановление пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa1cc-142">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="aa1cc-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aa1cc-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

