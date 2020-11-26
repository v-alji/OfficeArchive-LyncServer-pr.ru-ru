---
title: 'Lync Server 2013: изменение политики голосовой связи и настройка записей об использовании PSTN'
description: 'Lync Server 2013: изменение политики голосовой связи и настройка записей об использовании КТСОП.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify a voice policy and configure PSTN usage records
ms:assetid: 6c53aaf5-218b-4bd4-8cea-31bc9d53f1bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398511(v=OCS.15)
ms:contentKeyID: 48184419
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e26d6c8654ebf758f8b5a185c21468443e0451a9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445780"
---
# <a name="modify-a-voice-policy-and-configure-pstn-usage-records-in-lync-server-2013"></a><span data-ttu-id="1ac25-103">Изменение политики голосовой связи и настройка записей использования PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-103">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1ac25-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1ac25-104">

<span> </span></span></span>

<span data-ttu-id="1ac25-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1ac25-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1ac25-106">Если вы хотите изменить политику голосовой связи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1ac25-106">Follow these steps if you want to modify a voice policy.</span></span> <span data-ttu-id="1ac25-107">Если вы хотите создать новую политику голосовой связи, ознакомьтесь со сведениями [Создание политики голосовой связи и настройка записей использования PSTN в Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md) для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="1ac25-107">If you want to create a new voice policy, see [Create a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md) for the procedure.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1ac25-108">Если пользователю, которому назначена политика голосовой связи, не назначены записи использования общественной коммутируемой телефонной сети (КТСОП), пользователь не сможет звонить по исходящим звонкам.</span><span class="sxs-lookup"><span data-stu-id="1ac25-108">If a user is assigned to a voice policy has no associated public switched telephone network (PSTN) usage records, the user cannot place outbound calls.</span></span> <span data-ttu-id="1ac25-109">Список всех записей об использовании PSTN, доступных в вашем развертывании вашего корпоративного голоса, и просмотр их свойств можно найти <A href="lync-server-2013-view-pstn-usage-records.md">в разделе Просмотр записей об использовании PSTN в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1ac25-109">For a listing of all PSTN usage records available in your Enterprise Voice deployment and view their properties, see <A href="lync-server-2013-view-pstn-usage-records.md">View PSTN usage records in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-modify-a-voice-policy"></a><span data-ttu-id="1ac25-110">Изменение политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="1ac25-110">To modify a voice policy</span></span>

1.  <span data-ttu-id="1ac25-111">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="1ac25-111">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="1ac25-112">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="1ac25-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1ac25-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1ac25-114">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1ac25-115">В левой области навигации щелкните **Маршрутизация голосовой связи**, затем **Политика голосовой связи**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-115">In the left navigation bar, click **Voice Routing**, and then click **Voice Policy**.</span></span>

4.  <span data-ttu-id="1ac25-116">На странице **Политика голосовой связи** дважды щелкните имя политики голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="1ac25-116">On the **Voice Policy** page, double-click a voice policy name.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1ac25-p105">Область и имя политики устанавливаются при создании политики голосовой связи. Изменить их нельзя.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p105">The scope and name were set when the voice policy was created. They cannot be changed.</span></span>

    
    </div>

5.  <span data-ttu-id="1ac25-119">В разделе **изменения политики голосовой связи** введите дополнительное описание политики голосовой связи (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="1ac25-119">(Optional) In **Edit Voice Policy**, enter additional descriptive information for the voice policy.</span></span>

6.  <span data-ttu-id="1ac25-120">Установите или снимите следующие флажки для включения или отключения соответствующих **функций вызова**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-120">Select or clear the following check boxes to enable or disable each of the **Calling features**:</span></span>
    
      - <span data-ttu-id="1ac25-121">**Отключение от голосовой почты** предотвращает немедленное перенаправление вызовов в систему голосовой почты на мобильном телефоне пользователя, если разрешено одновременное поступление вызовов, а телефон отключен, разряжен или находится вне зоны действия сети.</span><span class="sxs-lookup"><span data-stu-id="1ac25-121">**Voice mail escape** prevents calls from being immediately routed to the user’s mobile phone voice mail system when simultaneous ringing is configured and the phone is turned off, out of battery, or out of range.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1ac25-122">Эту функцию можно настроить только с помощью командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="1ac25-122">This feature is only configurable through the Lync Server Management Shell</span></span>

        
        </div>
    
      - <span data-ttu-id="1ac25-123">**Переадресация звонков** позволяет пользователям переадресовывать звонки на другие телефоны и устройства клиента.</span><span class="sxs-lookup"><span data-stu-id="1ac25-123">**Call forwarding** enables users to forward calls to other phones and client devices.</span></span> <span data-ttu-id="1ac25-124">Lync Server 2013 предоставляет значительно более широкий спектр параметров настройки переадресации звонков.</span><span class="sxs-lookup"><span data-stu-id="1ac25-124">Lync Server 2013 provides a significantly wider range of configuration options for call forwarding.</span></span> <span data-ttu-id="1ac25-125">Например, если в организации требуется запретить внешнюю переадресацию входящих вызовов в ТСОП, администратор может применить особую политику голосовой связи для реализации этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="1ac25-125">For example, if an organization does not want to allow incoming calls to be forwarded externally to the PSTN, an administrator can apply a special voice policy to deploy this restriction.</span></span> <span data-ttu-id="1ac25-126">По умолчанию эта функция включена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-126">Enabled by default.</span></span>
    
      - <span data-ttu-id="1ac25-127">**Делегирование** позволяет пользователям указывать других пользователей, которые могут выполнять и принимать звонки от их имени.</span><span class="sxs-lookup"><span data-stu-id="1ac25-127">**Delegation** enables users to specify other users to send and receive calls on their behalf.</span></span> <span data-ttu-id="1ac25-128">В Lync Server 2013 делегат может настраивать одновременные звонки, позволяющие входящим звонкам своему начальнику звонить всем абонентам одновременных звонков.</span><span class="sxs-lookup"><span data-stu-id="1ac25-128">In Lync Server 2013, a delegate can configure simultaneous ringing that enables incoming calls to his or her manager to ring all of the delegate’s simultaneous ringing targets.</span></span> <span data-ttu-id="1ac25-129">Это расширяет возможность уполномоченного отвечать на вызовы, адресованные руководителю.</span><span class="sxs-lookup"><span data-stu-id="1ac25-129">This provides the delegate with greater flexibility in responding to calls directed to the manager.</span></span> <span data-ttu-id="1ac25-130">По умолчанию эта функция включена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-130">Enabled by default.</span></span>
    
      - <span data-ttu-id="1ac25-p108">**Переключение звонка** позволяет пользователям передать звонок другим пользователям. По умолчанию данная возможность включена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p108">**Call transfer** enables users to transfer calls to other users. Enabled by default.</span></span>
    
      - <span data-ttu-id="1ac25-p109">**Приостановка вызовов** позволяет пользователям переводить вызовы в режим удержания, а затем принимать такой вызов с другого телефона или клиента. По умолчанию эта функция отключена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p109">**Call park** enables users to park calls on hold, and then pick up the call from a different phone or client. Disabled by default.</span></span>
    
      - <span data-ttu-id="1ac25-135">**Одновременный звонок** позволяет принимать входящие звонки на другие телефоны (например, на мобильный телефон) и другие оконечные устройства.</span><span class="sxs-lookup"><span data-stu-id="1ac25-135">**Simultaneous ringing** enables incoming calls to ring on additional phones (for example, a mobile phone) or other endpoint devices.</span></span> <span data-ttu-id="1ac25-136">Lync Server 2013 предоставляет значительно более широкий спектр вариантов настройки для одновременных звонков.</span><span class="sxs-lookup"><span data-stu-id="1ac25-136">Lync Server 2013 provides a significantly wider range of configuration options for simultaneous ringing.</span></span> <span data-ttu-id="1ac25-137">По умолчанию данная возможность включена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-137">Enabled by default.</span></span>
    
      - <span data-ttu-id="1ac25-138">**Групповой звонок** позволяет пользователям из заданной группы отвечать на звонки, предназначенные другим членам этой группы.</span><span class="sxs-lookup"><span data-stu-id="1ac25-138">**Team call** enables users on a defined team to answer calls for other members of the team.</span></span> <span data-ttu-id="1ac25-139">По умолчанию данная возможность включена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-139">Enabled by default.</span></span>
    
      - <span data-ttu-id="1ac25-140">**Переадресация через коммутируемые** линии позволяет перенаправлять звонки, сделанные пользователями, которым назначена эта политика, другим пользователям организации, если она перегружена или недоступна.</span><span class="sxs-lookup"><span data-stu-id="1ac25-140">**PSTN re-route** enables calls made by users who are assigned this policy to other enterprise users to be rerouted on the public switched telephone network (PSTN) if the WAN is congested or unavailable.</span></span> <span data-ttu-id="1ac25-141">По умолчанию данная возможность включена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-141">Enabled by default.</span></span>
    
      - <span data-ttu-id="1ac25-142">**Переопределение политики пропускной способности** позволяет администраторам переопределять решения политики управления допуском (CAC) для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ac25-142">**Bandwidth policy override** enables administrators to override call admission control (CAC) policy decisions for a particular user.</span></span> <span data-ttu-id="1ac25-143">По умолчанию данная возможность отключена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-143">Disabled by default.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1ac25-p114">Эта политика будет переопределяться только для входящих вызовов пользователя, но не для исходящих вызовов, размещаемых пользователем. После установки сеанса будет точно учитываться использование потребление полосы пропускания. Этот параметр следует использовать с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p114">The policy will be overridden only for incoming calls to the user and not for outgoing calls that are placed by the user. After the session is established, the bandwidth consumption will be accurately recorded. This setting should be used sparingly.</span></span>

        
        </div>
    
      - <span data-ttu-id="1ac25-147">С помощью функции **отслеживания вредоносных вызовов** пользователи смогут сообщать о вредоносных вызовах (например, о угрозах Bomb), используя пользовательский интерфейс клиента, который в свою очередь вызывает эти записи в записях (CDRs).</span><span class="sxs-lookup"><span data-stu-id="1ac25-147">**Malicious call tracing** enables users to report malicious calls (such as bomb threats) using the client UI, which in turn flags the calls in the call detail records (CDRs).</span></span> <span data-ttu-id="1ac25-148">По умолчанию эта функция отключена.</span><span class="sxs-lookup"><span data-stu-id="1ac25-148">Disabled by default.</span></span>

7.  <span data-ttu-id="1ac25-149">Чтобы сопоставить и настроить записи использования ТСОП для этой политики голосовой связи, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="1ac25-149">To associate and configure PSTN usage records for this voice policy, do any of the following:</span></span>
    
      - <span data-ttu-id="1ac25-p116">Для выбора одной или нескольких записей в списке записей о режимах работы с ТСОП, доступных в данном развертывании корпоративной голосовой связи, нажмите кнопку **Выбрать** Выделите записи, которые требуется связать с данной политикой голосовой связи, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p116">To choose one or more records from a list of all PSTN usage records available in your Enterprise Voice deployment, click **Select**. Highlight the records that you want to associate with this voice policy, and then click **OK**.</span></span>
    
      - <span data-ttu-id="1ac25-152">Для удаления записи о режиме работы с ТСОП из политики голосовой связи выделите эту запись и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-152">To remove a PSTN usage record from this voice policy, highlight the record and click **Remove**.</span></span>
    
      - <span data-ttu-id="1ac25-153">Чтобы определить новую запись использования ТСОП и сопоставить ее с политикой голосовой связи, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1ac25-153">To define a new PSTN usage record and associate it with this voice policy, do the following:</span></span>
        
        1.  <span data-ttu-id="1ac25-154">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-154">Click **New**.</span></span>
        
        2.  <span data-ttu-id="1ac25-p117">В поле **Имя** введите уникальное информативное имя записи. Например, можно создать запись о режиме работы с ТСОП для штатных сотрудников в Редмонде и назвать ее **Redmond**, а также создать другую запись для внештатных сотрудников и назвать ее **RedmondTemps**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p117">In the **Name** field, enter a unique descriptive name for the record. For example, you may want to create a PSTN usage record named **Redmond** for full-time employees located in Redmond, and another record named **RedmondTemps** for temporary employees.</span></span>
            
            <div>
            

            > [!NOTE]  
            > <span data-ttu-id="1ac25-p118">Имя записи о режиме работы с ТСОП не должно повторяться в пределах развертывания корпоративной голосовой связи. После сохранения записи поле <STRONG>Имя</STRONG> не доступно для редактирования.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p118">The PSTN usage record name must be unique within the Enterprise Voice deployment. After the record is saved, the <STRONG>Name</STRONG> field cannot be edited.</span></span>

            
            </div>
        
        3.  <span data-ttu-id="1ac25-159">Используйте любой из описанных ниже методов, чтобы сопоставить и настроить маршруты для данной записи использования ТСОП:</span><span class="sxs-lookup"><span data-stu-id="1ac25-159">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="1ac25-160">Для выбора одного или нескольких маршрутов из списка доступных маршрутов в развертывании корпоративной голосовой связи нажмите кнопку **Выбрать** и выделите маршруты, которые требуется связать с данной записью о режиме работы с ТСОП, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-160">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes that you want to associate with this PSTN usage record, and then click **OK**.</span></span>
            
              - <span data-ttu-id="1ac25-161">Для удаления маршрута из записи о режиме работы с ТСОП выделите маршрут и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-161">To remove a route from the PSTN usage record, highlight the route and click **Remove**.</span></span>
            
              - <span data-ttu-id="1ac25-162">Чтобы определить новый маршрут и связать его с этой записью использования PSTN, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-162">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="1ac25-163">Дополнительные сведения можно найти [в разделе Создание голосовых маршрутов в Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-163">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="1ac25-164">Для изменения маршрута, уже связанного с данной записью о режиме работы с ТСОП, выделите его и щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-164">To edit a route that is already associated with this PSTN usage record, highlight the route and click **Show details**.</span></span> <span data-ttu-id="1ac25-165">Подробности можно найти [в разделе Изменение голосового маршрута в Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-165">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        4.  <span data-ttu-id="1ac25-166">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-166">Click **OK**.</span></span>
    
      - <span data-ttu-id="1ac25-167">Чтобы изменить запись использования ТСОП, которая уже сопоставлена с этой политикой голосовой связи, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1ac25-167">To edit a PSTN usage record that is already associated with this voice policy, do the following:</span></span>
        
        1.  <span data-ttu-id="1ac25-168">Выделите запись о режиме работы с ТСОП, которую требуется изменить, и нажмите кнопку **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-168">Highlight the PSTN usage record that you want to edit and click **Show details**.</span></span>
        
        2.  <span data-ttu-id="1ac25-169">Используйте любой из описанных ниже методов, чтобы сопоставить и настроить маршруты для данной записи использования ТСОП:</span><span class="sxs-lookup"><span data-stu-id="1ac25-169">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="1ac25-170">Для выбора одного или нескольких маршрутов из списка доступных маршрутов в развертывании корпоративной голосовой связи нажмите кнопку **Выбрать** и выделите маршруты, которые требуется связать с данной записью о режиме работы с ТСОП, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-170">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes that you want to associate with this PSTN usage record, and then click **OK**.</span></span>
            
              - <span data-ttu-id="1ac25-171">Для удаления маршрута из данной записи о режиме работы с ТСОП выделите маршрут и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-171">To remove a route from this PSTN usage record, highlight the route and click **Remove**.</span></span>
            
              - <span data-ttu-id="1ac25-172">Чтобы определить новый маршрут и связать его с этой записью использования PSTN, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-172">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="1ac25-173">Дополнительные сведения можно найти [в разделе Создание голосовых маршрутов в Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-173">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="1ac25-174">Для изменения маршрута, уже связанного с данной записью о режиме работы с ТСОП, выделите его и щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-174">To edit a route that is already associated with this PSTN usage record, highlight the route and click **Show details**.</span></span> <span data-ttu-id="1ac25-175">Подробности можно найти [в разделе Изменение голосового маршрута в Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-175">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        3.  <span data-ttu-id="1ac25-176">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-176">Click **OK**.</span></span>

8.  <span data-ttu-id="1ac25-p123">Упорядочите записи использования ТСОП для достижений оптимальной производительности. Чтобы изменить положение записи в списке, выделите ее имя и щелкните стрелку вверх или вниз.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p123">Arrange the PSTN usage records for optimum performance. To change a record’s position in the list, highlight the record name and click the up or down arrow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1ac25-179">Порядок записей о режиме работы с ТСОП в голосовой политике имеет значение.</span><span class="sxs-lookup"><span data-stu-id="1ac25-179">The order in which PSTN usage records are listed in the voice policy is significant.</span></span> <span data-ttu-id="1ac25-180">Lync Server обходит список сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="1ac25-180">Lync Server traverses the list from the top down.</span></span> <span data-ttu-id="1ac25-181">Рекомендуется упорядочить список по частоте использования, например: RedmondLocal, RedmondLongDist, RedmondInternational, RedmondBackup.</span><span class="sxs-lookup"><span data-stu-id="1ac25-181">We recommend that you organize the list by frequency of use, for example: RedmondLocal, RedmondLongDist, RedmondInternational, RedmondBackup.</span></span>

    
    </div>

9.  <span data-ttu-id="1ac25-182">Чтобы сопоставить и настроить записи использования ТСОП для переадресации звонков и одновременных звонков в этой политике голосовой связи, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="1ac25-182">To associate and configure PSTN usage records for call forwarding and simultaneous ringing in this voice policy, do any of the following:</span></span>
    
      - <span data-ttu-id="1ac25-183">Если для переадресации вызовов и одновременного поступления вызовов требуется применять те же записи о режиме работы с ТСОП, что и в данной политике голосовой связи, выберите **Направлять с помощью применения ТСОП звонка** в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="1ac25-183">To use the same PSTN usage records for call forwarding and simultaneous ringing as this voice policy, select the option **Route using the call PSTN usages** from the drop-down menu.</span></span>
    
      - <span data-ttu-id="1ac25-184">Чтобы разрешить переадресацию звонков и одновременный звонок только внутренним пользователям Lync, выберите в раскрывающемся меню пункт **направить только внутренним пользователям Lync** .</span><span class="sxs-lookup"><span data-stu-id="1ac25-184">To allow call forwarding and simultaneous ringing to internal Lync users only, select **Route to internal Lync users only** from the drop-down menu.</span></span> <span data-ttu-id="1ac25-185">Calls will not be forwarded to external PSTN numbers.</span><span class="sxs-lookup"><span data-stu-id="1ac25-185">Calls will not be forwarded to external PSTN numbers.</span></span>
    
      - <span data-ttu-id="1ac25-p126">Если для переадресации вызовов и одновременного поступления вызовов требуется применять записи о режиме работы с ТСОП, отличные от применяемых в данной политике голосовой связи, выберите **Направлять с помощью пользовательского применения ТСОП** в раскрывающемся меню. Отображается элемент управления, позволяющий выбирать существующие и создавать новые записи о режимах работы с ТСОП специально для переадресации вызовов и одновременного поступления вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p126">To specify different PSTN usage records for call forwarding and simultaneous ringing than those used for this voice policy, select the option **Route using custom PSTN usages** from the drop-down menu. This option displays a control to select existing PSTN usage records or to create new PSTN usage records, specifically for call forwarding and simultaneous ringing.</span></span>
        
          - <span data-ttu-id="1ac25-p127">Для выбора в списке одной или нескольких записей о режимах работы с ТСОП применительно к переадресации вызовов и одновременному поступлению вызовов нажмите кнопку **Выбрать**. Выделите записи, которые требуется связать с данной политикой переадресации вызовов и одновременного поступления вызовов, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p127">To choose one or more records from a list of PSTN usage records for call forwarding and simultaneous ringing, click **Select**. Highlight the records that you want to associate with this call forwarding and simultaneous ringing policy, and then click **OK**.</span></span>
        
          - <span data-ttu-id="1ac25-190">Для удаления записи о режиме работы с ТСОП из данной политики переадресации вызовов и одновременного поступления вызовов выделите эту запись и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-190">To remove a PSTN usage record from this call forwarding and simultaneous ringing policy, highlight the record and click **Remove**.</span></span>
        
          - <span data-ttu-id="1ac25-191">Чтобы определить новую запись использования ТСОП и сопоставить ее с этой политикой для переадресации звонков и одновременных звонков, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1ac25-191">To define a new PSTN usage record and associate it with this call forwarding and simultaneous ringing policy, do the following:</span></span>
            
            1.  <span data-ttu-id="1ac25-192">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-192">Click **New**.</span></span>
            
            2.  <span data-ttu-id="1ac25-193">В поле **Имя** введите уникальное информативное имя записи.</span><span class="sxs-lookup"><span data-stu-id="1ac25-193">In the **Name** field, enter a unique descriptive name for the record.</span></span>
                
                <div>
                

                > [!NOTE]  
                > <span data-ttu-id="1ac25-p128">Имя записи о режиме работы с ТСОП не должно повторяться в пределах развертывания корпоративной голосовой связи. После сохранения записи поле <STRONG>Имя</STRONG> не доступно для редактирования.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p128">The PSTN usage record name must be unique within the Enterprise Voice deployment. After the record is saved, the <STRONG>Name</STRONG> field cannot be edited.</span></span>

                
                </div>
            
            3.  <span data-ttu-id="1ac25-196">Используйте любой из описанных ниже методов, чтобы сопоставить и настроить маршруты для данной записи использования ТСОП:</span><span class="sxs-lookup"><span data-stu-id="1ac25-196">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
                
                  - <span data-ttu-id="1ac25-197">Для выбора одного или нескольких маршрутов из списка доступных маршрутов в развертывании корпоративной голосовой связи нажмите кнопку **Выбрать** и выделите маршруты, которые требуется связать с данной записью о режиме работы с ТСОП, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-197">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes that you want to associate with this PSTN usage record, and then click **OK**.</span></span>
                
                  - <span data-ttu-id="1ac25-198">Для удаления маршрута из записи о режиме работы с ТСОП выделите маршрут и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-198">To remove a route from the PSTN usage record, highlight the route and click **Remove**.</span></span>
                
                  - <span data-ttu-id="1ac25-199">Чтобы определить новый маршрут и связать его с этой записью использования PSTN, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-199">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="1ac25-200">Дополнительные сведения можно найти [в разделе Создание голосовых маршрутов в Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-200">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
                
                  - <span data-ttu-id="1ac25-201">Чтобы изменить маршрут, который уже связан с этой записью об использовании PSTN, выделите его и нажмите кнопку **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-201">To edit a route that is already associated with this PSTN usage record, highlight the route, and then click **Show details**.</span></span> <span data-ttu-id="1ac25-202">Подробности можно найти [в разделе Изменение голосового маршрута в Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-202">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
            
            4.  <span data-ttu-id="1ac25-203">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-203">Click **OK**.</span></span>
        
          - <span data-ttu-id="1ac25-204">Чтобы изменить запись использования ТСОП, которая уже сопоставлена с этой политикой голосовой связи, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1ac25-204">To edit a PSTN usage record that is already associated with this voice policy, do the following:</span></span>
            
            1.  <span data-ttu-id="1ac25-205">Выделите запись о режиме работы с ТСОП, которую требуется изменить, и нажмите кнопку **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-205">Highlight the PSTN usage record that you want to edit and click **Show details**.</span></span>
            
            2.  <span data-ttu-id="1ac25-206">Используйте любой из описанных ниже методов, чтобы сопоставить и настроить маршруты для данной записи использования ТСОП:</span><span class="sxs-lookup"><span data-stu-id="1ac25-206">Use any of the following methods to associate and configure routes for this PSTN usage record:</span></span>
                
                  - <span data-ttu-id="1ac25-207">Для выбора одного или нескольких маршрутов из списка доступных маршрутов в развертывании корпоративной голосовой связи нажмите кнопку **Выбрать** и выделите маршруты, которые требуется связать с данной записью о режиме работы с ТСОП, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-207">To choose one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**, highlight the routes you want to associate with this PSTN usage record, and then click **OK**.</span></span>
                
                  - <span data-ttu-id="1ac25-208">Для удаления маршрута из данной записи о режиме работы с ТСОП выделите маршрут и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-208">To remove a route from this PSTN usage record, highlight the route and click **Remove**.</span></span>
                
                  - <span data-ttu-id="1ac25-209">Чтобы определить новый маршрут и связать его с этой записью использования PSTN, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-209">To define a new route and associate it with this PSTN usage record, click **New**.</span></span> <span data-ttu-id="1ac25-210">Дополнительные сведения можно найти [в разделе Создание голосовых маршрутов в Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-210">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
                
                  - <span data-ttu-id="1ac25-211">Для изменения маршрута, уже связанного с данной записью о режиме работы с ТСОП, выделите его и щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-211">To edit a route that is already associated with this PSTN usage record, highlight the route and click **Show details**.</span></span> <span data-ttu-id="1ac25-212">Подробности можно найти [в разделе Изменение голосового маршрута в Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-212">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
            
            3.  <span data-ttu-id="1ac25-213">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-213">Click **OK**.</span></span>

10. <span data-ttu-id="1ac25-p133">(Необязательно) Введите число для проверки политики голосовой связи и нажмите кнопку **Начать** (не обязательно). Результаты проверки отображаются в разделе **Преобразованный номер для проверки**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-p133">(Optional) Enter a number to test the voice policy and click **Go**. The test results are displayed under **Translated number to test**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1ac25-216">Вы можете сохранить политику голосовой связи, которая еще не пройдет проверку, а затем настроить ее позже.</span><span class="sxs-lookup"><span data-stu-id="1ac25-216">You can save a voice policy that does not yet pass the test and then reconfigure it later.</span></span> <span data-ttu-id="1ac25-217">Подробные сведения можно найти <A href="lync-server-2013-test-voice-routing.md">в разделе Проверка маршрутизации голосовой связи в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1ac25-217">For details, see <A href="lync-server-2013-test-voice-routing.md">Test voice routing in Lync Server 2013</A>.</span></span>

    
    </div>

11. <span data-ttu-id="1ac25-218">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-218">Click **OK**.</span></span>

12. <span data-ttu-id="1ac25-219">На странице **Политика голосовой связи** (Политика голосовой связи) нажмите кнопку **Сохранить**, затем **Сохранить все**.</span><span class="sxs-lookup"><span data-stu-id="1ac25-219">On the **Voice Policy** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1ac25-220">Каждый раз, когда вы создаете или изменяете политику голосовой связи, необходимо выполнить команду <STRONG>commit all</STRONG> , чтобы опубликовать изменение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1ac25-220">Whenever you create or modify a voice policy, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="1ac25-221">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="1ac25-221">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

13. <span data-ttu-id="1ac25-222">Функция отключения голосовой почты обеспечивает распознавание немедленного ответа на вызов из голосовой почты на мобильном телефоне пользователя и завершение связи с голосовой почтой (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="1ac25-222">(Optional) Voicemail Escape detects that a call was immediately answered by the user’s mobile phone voice mail, and disconnects the call to the mobile phone voice mail.</span></span> <span data-ttu-id="1ac25-223">Благодаря этому вызов продолжает поступать на другие оконечные устройства пользователя, что позволяет ему ответить на вызов.</span><span class="sxs-lookup"><span data-stu-id="1ac25-223">This allows the call to continue to ring on the user’s other endpoints giving the user the opportunity to answer the call.</span></span> <span data-ttu-id="1ac25-224">Дополнительные сведения о настройке политики голосовой почты можно найти [в разделе Настройка функции переключения голосовой почты в Lync Server 2013](lync-server-2013-configuring-voice-mail-escape.md).</span><span class="sxs-lookup"><span data-stu-id="1ac25-224">For details about how to configure a voice mail policy, see [Configuring voice mail escape in Lync Server 2013](lync-server-2013-configuring-voice-mail-escape.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1ac25-225">См. также</span><span class="sxs-lookup"><span data-stu-id="1ac25-225">See Also</span></span>


[<span data-ttu-id="1ac25-226">Создание политики голосовой связи и настройка записей об использовании PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-226">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)  
[<span data-ttu-id="1ac25-227">Просмотр записей использования PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-227">View PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-view-pstn-usage-records.md)  
[<span data-ttu-id="1ac25-228">Создание голосового маршрута в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-228">Create a voice route in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-route.md)  
[<span data-ttu-id="1ac25-229">Изменение маршрута голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-229">Modify a voice route in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-route.md)  
[<span data-ttu-id="1ac25-230">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-230">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  
[<span data-ttu-id="1ac25-231">Настройка escape-последовательности голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-231">Configuring voice mail escape in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-mail-escape.md)  


[<span data-ttu-id="1ac25-232">Тестирование голосовой маршрутизации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ac25-232">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="1ac25-233"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1ac25-233"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

