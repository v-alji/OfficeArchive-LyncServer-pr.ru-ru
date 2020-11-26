---
title: 'Lync Server 2013: настройка политика качества обслуживания для серверов конференц-связи, приложений и серверов-посредников'
description: 'Lync Server 2013: Настройка политики качества обслуживания для конференций, приложений и серверов-исправлений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a Quality of Service policy for your Conferencing, Application, and Mediation servers
ms:assetid: 8adcbbc5-c9f5-476d-ab7f-72e61859cacf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205076(v=OCS.15)
ms:contentKeyID: 48184769
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ee82c5f1f6b3025c4052b7e27c1013e0624b756
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433488"
---
# <a name="configuring-a-quality-of-service-policy-in-lync-server-2013-for-your-conferencing-application-and-mediation-servers"></a><span data-ttu-id="c763f-103">Настройка политика качества обслуживания в Lync Server 2013 для серверов конференц-связи, приложений и серверов-посредников</span><span class="sxs-lookup"><span data-stu-id="c763f-103">Configuring a Quality of Service policy in Lync Server 2013 for your Conferencing, Application, and Mediation servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c763f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c763f-104">

<span> </span></span></span>

<span data-ttu-id="c763f-105">_**Тема последнего изменения:** 2014-06-23_</span><span class="sxs-lookup"><span data-stu-id="c763f-105">_**Topic Last Modified:** 2014-06-23_</span></span>

<span data-ttu-id="c763f-106">Настройка диапазонов портов упрощает использование качества обслуживания, гарантируя, что весь трафик определенного типа (например, весь звуковой трафик) проходит через один и тот же набор портов.</span><span class="sxs-lookup"><span data-stu-id="c763f-106">Configuring port ranges facilitates the use of Quality of Service by ensuring that all traffic of a specified type (for example, all audio traffic) travels through the same set of ports.</span></span> <span data-ttu-id="c763f-107">Это упрощает для системы определение и пометку определенного пакета: Если порт 49152 зарезервирован для звукового трафика, любой пакет, переданный через порт 49152, можно пометить с помощью кода DSCP, указывающего на то, что это звуковой пакет.</span><span class="sxs-lookup"><span data-stu-id="c763f-107">This makes it easy for the system to identify and mark a given packet: if port 49152 is reserved for audio traffic, then any packet traveling through port 49152 can be marked with a DSCP code that indicates that this is an audio packet.</span></span> <span data-ttu-id="c763f-108">В свою очередь, это позволяет маршрутизаторам идентифицировать пакет в качестве звукового пакета и давать ему более высокий приоритет, чем непомеченные пакеты (например, пакеты, используемые для копирования файла с одного сервера на другой).</span><span class="sxs-lookup"><span data-stu-id="c763f-108">In turn, this enables routers to identify the packet as an audio packet, and give it higher priority than unmarked packets (such as packets used to copy a file from one server to another).</span></span>

<span data-ttu-id="c763f-109">Тем не менее, если запретить набор портов для определенного типа трафика, пакеты, передаваемые через эти порты, не помечаются соответствующим кодом DSCP.</span><span class="sxs-lookup"><span data-stu-id="c763f-109">However, simply restricting a set of ports to a specific type of traffic does not result in packets traveling through those ports being marked with the appropriate DSCP code.</span></span> <span data-ttu-id="c763f-110">В дополнение к определению диапазонов портов необходимо также создать политики качества обслуживания, определяющие код DSCP, связанный с каждым диапазоном портов.</span><span class="sxs-lookup"><span data-stu-id="c763f-110">In addition to defining port ranges you must also create Quality of Service policies that specify the DSCP code to be associated with each port range.</span></span> <span data-ttu-id="c763f-111">Для Microsoft Lync Server 2013, который обычно означает создание двух политик: один для звука и для видео.</span><span class="sxs-lookup"><span data-stu-id="c763f-111">For Microsoft Lync Server 2013 that typically means creating two policies: one for audio and one for video.</span></span>

<span data-ttu-id="c763f-112">Проще всего создавать политики качества обслуживания, а также управлять ими с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c763f-112">Quality of Service policies are most-easily created, and managed, by using Group Policy.</span></span> <span data-ttu-id="c763f-113">(Эти же политики также можно создать с помощью локальной политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="c763f-113">(These same policies can also be created by using local security policies.</span></span> <span data-ttu-id="c763f-114">Тем не менее, это необходимо для того, чтобы повторять одну и ту же процедуру на каждом и каждом компьютере.) Первоначальный набор политик QoS (для звуковых и видеофайлов) должен применяться только к компьютерам Lync Server, на которых запущен сервер конференц-связи, сервер приложений и (или) сервер служб исправлений.</span><span class="sxs-lookup"><span data-stu-id="c763f-114">However, that requires you to repeat the same procedure on each and every computer.) Your initial set of QoS policies (one for audio and one for video) should be applied only to Lync Server computers running the Conferencing server, Application server, and/or Mediation server services.</span></span> <span data-ttu-id="c763f-115">Если все эти компьютеры находятся в одном и том же OU Active Directory, вы можете просто назначить этому подразделению новый объект групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="c763f-115">If all of these computers are located in the same Active Directory OU then you can simply assign the new Group Policy object (GPO) to that OU.</span></span> <span data-ttu-id="c763f-116">Кроме того, вы можете выполнить другие действия, чтобы назначить новую политику для указанных компьютеров; Например, вы можете поместить соответствующие компьютеры в группу безопасности, а затем применить их только к этой группе безопасности с помощью фильтрации безопасности групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c763f-116">Alternatively, you can take other steps to target the new policy to the specified computers; for example, you can place the appropriate computers in a security group, then use Group Policy security filtering to apply the GPO just to that security group.</span></span>

<span data-ttu-id="c763f-117">Чтобы создать политику качества обслуживания для управления звуковым подключением, войдите на компьютер, на котором установлен компонент управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="c763f-117">In order to create a Quality of Service policy for managing audio, log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="c763f-118">Откройте средство управления групповыми политиками (нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Управление групповыми политиками**), а затем выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c763f-118">Open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following procedure:</span></span>

1.  <span data-ttu-id="c763f-119">В разделе Управление групповой политикой найдите контейнер, в котором нужно создать новую политику.</span><span class="sxs-lookup"><span data-stu-id="c763f-119">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="c763f-120">Например, если все компьютеры Lync Server находятся в подразделении с именем Lync Server, новую политику следует создать в OU сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c763f-120">For example, if all your Lync Server computers are located in an OU named Lync Server then the new policy should be created in the Lync Server OU.</span></span>

2.  <span data-ttu-id="c763f-121">Щелкните правой кнопкой мыши соответствующий контейнер и выберите команду **создать объект групповой политики в этом домене и свяжите его**.</span><span class="sxs-lookup"><span data-stu-id="c763f-121">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="c763f-122">В диалоговом окне **создание GPO** введите имя нового объекта групповой политики в поле **имя** (например, **Lync Server QoS**), а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c763f-122">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Server QoS**) and then click **OK**.</span></span>

4.  <span data-ttu-id="c763f-123">Щелкните созданную политику правой кнопкой мыши и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="c763f-123">Right-click the newly-created policy and then click **Edit**.</span></span>

5.  <span data-ttu-id="c763f-124">В редакторе управления групповыми политиками разверните узел **Конфигурация компьютера**, выберите пункт **политики**, разверните раздел **Параметры Windows**, щелкните правой кнопкой мыши службу **QoS на основе политики** и выберите команду **создать новую политику**.</span><span class="sxs-lookup"><span data-stu-id="c763f-124">In the Group Policy Management Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

6.  <span data-ttu-id="c763f-125">В диалоговом окне **QoS на основе политики** на первой странице в поле **имя** введите имя новой политики (например, **Lync Server QoS**).</span><span class="sxs-lookup"><span data-stu-id="c763f-125">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Server QoS**) in the **Name** box.</span></span> <span data-ttu-id="c763f-126">Выберите **задать значение DSCP** и задайте значение **46**.</span><span class="sxs-lookup"><span data-stu-id="c763f-126">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="c763f-127">Оставьте параметр **задать частоту исходящих подключений** невыбранным и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c763f-127">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

7.  <span data-ttu-id="c763f-128">На следующей странице убедитесь, что выбраны **все приложения** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c763f-128">On the next page, make sure that **All applications** is selected and then click **Next**.</span></span> <span data-ttu-id="c763f-129">Это гарантирует, что все приложения будут соответствовать пакеты из указанного диапазона портов с указанным кодом DSCP.</span><span class="sxs-lookup"><span data-stu-id="c763f-129">This simply ensures that all applications will match packets from the specified port range with the specified DSCP code.</span></span>

8.  <span data-ttu-id="c763f-130">На третьей странице убедитесь, что выбраны оба **IP-адреса источника и конечный IP-адрес** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c763f-130">On the third page, make sure that both **Any source IP address and Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="c763f-131">Эти два параметра гарантируют, что пакеты будут управляться независимо от того, на каком компьютере (IP-адрес) отправили эти пакеты, и какой компьютер (IP-адрес) будет получать эти пакеты.</span><span class="sxs-lookup"><span data-stu-id="c763f-131">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

9.  <span data-ttu-id="c763f-132">На четвертой странице в раскрывающемся списке выберите протокол **TCP и UDP** , который будет **применяться этой политикой QoS** .</span><span class="sxs-lookup"><span data-stu-id="c763f-132">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="c763f-133">Протокол TCP и протокол UDP (User Datagram Protocol) — это два сетевых протокола, которые чаще всего используются в Lync Server и клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="c763f-133">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

10. <span data-ttu-id="c763f-134">Под заголовком **укажите номер исходного порта**, выберите **из этого исходного порта или диапазона**.</span><span class="sxs-lookup"><span data-stu-id="c763f-134">Under the heading **Specify the source port number**, select **From this source port or range**.</span></span> <span data-ttu-id="c763f-135">В сопроводительном текстовом поле введите диапазон портов, зарезервированный для передачи звука.</span><span class="sxs-lookup"><span data-stu-id="c763f-135">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="c763f-136">Например, если вы зарезервированы порты 49152 через порты 57500 для звукового трафика, введите диапазон портов в следующем формате: **49152:57500**.</span><span class="sxs-lookup"><span data-stu-id="c763f-136">For example, if you reserved ports 49152 through ports 57500 for audio traffic enter the port range using this format: **49152:57500**.</span></span> <span data-ttu-id="c763f-137">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="c763f-137">Click **Finish**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c763f-138">Значение DSCP для 46 является несколько случайным: хотя для пометки пакетов звука часто используется DSCP 46, вам не нужно использовать DSCP 46 для голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="c763f-138">The DSCP value of 46 is somewhat arbitrary: although DSCP 46 is often used for marking audio packets, you do not have to use DSCP 46 for audio communications.</span></span> <span data-ttu-id="c763f-139">Если вы уже реализовали качество обслуживания и используете другой код DSCP (например, DSCP 40), следует настроить политику качества обслуживания таким образом, чтобы она использовала тот же код (то есть 40 для звука).</span><span class="sxs-lookup"><span data-stu-id="c763f-139">If you have already implemented QoS and you are using a different DSCP code for audio (for example, DSCP 40) then you should configure your Quality of Service policy to use that same code (i.e., 40 for audio).</span></span> <span data-ttu-id="c763f-140">Если вы только что сейчас реализуете качество обслуживания, рекомендуется использовать DSCP 46 для звука, просто потому, что это значение обычно используется для пометки звуковых пакетов.</span><span class="sxs-lookup"><span data-stu-id="c763f-140">If you are just now implementing Quality of Service, then it is recommended that you use DSCP 46 for audio, simply because that value is commonly used to mark audio packets.</span></span>



</div>

<span data-ttu-id="c763f-141">После создания политики QoS для звукового трафика вы должны создать вторую политику для видеотрафика (и, при необходимости, третью политику для управления трафиком о совместном доступе к приложениям).</span><span class="sxs-lookup"><span data-stu-id="c763f-141">After you have created the QoS policy for audio traffic you should then create a second policy for video traffic (and, optionally, a third policy for managing application sharing traffic).</span></span> <span data-ttu-id="c763f-142">Чтобы создать политику для видео, выполните те же действия, что и при создании политики звука, заменив указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="c763f-142">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="c763f-143">Используйте другое (и уникальное) имя политики (например, **Lync Server Video**).</span><span class="sxs-lookup"><span data-stu-id="c763f-143">Use a different (and unique) policy name (for example, **Lync Server Video**).</span></span>

  - <span data-ttu-id="c763f-144">Задайте для параметра DSCP значение **34** вместо 46.</span><span class="sxs-lookup"><span data-stu-id="c763f-144">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="c763f-145">(Обратите внимание, что вам не нужно использовать значение DSCP для 34.</span><span class="sxs-lookup"><span data-stu-id="c763f-145">(Note that you do not have to use a DSCP value of 34.</span></span> <span data-ttu-id="c763f-146">Единственным требованием является использование другого значения DSCP для видео, чем вы использовали для звука.</span><span class="sxs-lookup"><span data-stu-id="c763f-146">The only requirement is that you use a different DSCP value for video than you used for audio.)</span></span>

  - <span data-ttu-id="c763f-147">Используйте ранее настроенный диапазон портов для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="c763f-147">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="c763f-148">Например, если у вас есть резервированные порты 57501 – 65535 для видео, задайте диапазон портов следующим образом: **57501:65535**.</span><span class="sxs-lookup"><span data-stu-id="c763f-148">For example, if you have reserved ports 57501 through 65535 for video, then set the port range to this: **57501:65535**.</span></span>

<span data-ttu-id="c763f-149">Если вы решили создать политику для управления трафиком общего доступа к приложениям, вы должны создать третью политику, заменив указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="c763f-149">If you decide to create a policy for managing application sharing traffic you must create a third policy, making the following substitutions:</span></span>

  - <span data-ttu-id="c763f-150">Используйте другое (и уникальное) имя политики (например, **общий доступ к приложениям Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="c763f-150">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="c763f-151">Задайте для параметра DSCP значение **24** , а не 46.</span><span class="sxs-lookup"><span data-stu-id="c763f-151">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="c763f-152">(Опять же, вам не нужно использовать значение DSCP, равное 24.</span><span class="sxs-lookup"><span data-stu-id="c763f-152">(Again, you do not have to use a DSCP value of 24.</span></span> <span data-ttu-id="c763f-153">Единственным требованием является использование другого значения DSCP для общего пользования приложениями, чем при использовании звука или видео.)</span><span class="sxs-lookup"><span data-stu-id="c763f-153">The only requirement is that you use a different DSCP value for application sharing than you used for audio or for video.)</span></span>

  - <span data-ttu-id="c763f-154">Используйте ранее настроенный диапазон портов для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="c763f-154">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="c763f-155">Например, если у вас есть резервированные порты 40803 – 49151 для совместного использования приложений, задайте диапазон портов следующим образом: **40803:49151**.</span><span class="sxs-lookup"><span data-stu-id="c763f-155">For example, if you have reserved ports 40803 through 49151 for application sharing, then set the port range to this: **40803:49151**.</span></span>

<span data-ttu-id="c763f-156">Новые политики, созданные вами, вступят в силу только после обновления групповой политики на компьютерах Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c763f-156">The new policies you have created will not take effect until Group Policy has been refreshed on your Lync Server computers.</span></span> <span data-ttu-id="c763f-157">Хотя групповая политика периодически обновляется сама, вы можете обновить ее принудительно, запустив на каждом нужном компьютере следующую команду.</span><span class="sxs-lookup"><span data-stu-id="c763f-157">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpupdate.exe /force

<span data-ttu-id="c763f-158">Эту команду можно выполнять в командной консоли Lync Server или из любого окна команд, которое выполняется в контексте учетных данных администратора.</span><span class="sxs-lookup"><span data-stu-id="c763f-158">This command can be run from within the Lync Server Management Shell or from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="c763f-159">Чтобы открыть такое окно с правами администратора, в меню **Пуск** правой кнопкой мыши щелкните **Командная строка** и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="c763f-159">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="c763f-160">Чтобы убедиться в том, что новые политики качества обслуживания применены, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c763f-160">To verify that the new QoS policies have been applied, do the following:</span></span>

1.  <span data-ttu-id="c763f-161">На компьютере Lync Server нажмите кнопку **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="c763f-161">On a Lync Server computer, click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="c763f-162">В диалоговом окне " **выполнить** " введите **regedit** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c763f-162">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="c763f-163">В редакторе реестра разверните узел **компьютер**, разверните раздел **hKey \_ локальный \_ компьютер**, разверните раздел программы **, а затем** разверните раздел **Microsoft**, затем разверните раздел **Windows** и выберите команду **QoS**. **SOFTWARE**</span><span class="sxs-lookup"><span data-stu-id="c763f-163">In Registry Editor, expand **Computer**, expand **HKEY\_LOCAL\_MACHINE**, expand **SOFTWARE**, expand **Policies**, expand **Microsoft**, expand **Windows**, and then click **QoS**.</span></span> <span data-ttu-id="c763f-164">В разделе **QoS** для каждой созданной политики QoS должны отображаться разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="c763f-164">Under **QoS** you should see registry keys for each of the QoS policies you just created.</span></span> <span data-ttu-id="c763f-165">Например, если вы создали две новые политики (один из которых называется Lync Server Audio QoS и другое название — качество обслуживания видео Lync Server), вы должны иметь в реестре записи для Lync Server Audio QoS и Lync Server Video QoS.</span><span class="sxs-lookup"><span data-stu-id="c763f-165">For example, if you created two new policies (one named Lync Server Audio QoS and the other named Lync Server Video QoS) you should registry entries for Lync Server Audio QoS and Lync Server Video QoS.</span></span>

<span data-ttu-id="c763f-166">Чтобы убедиться в том, что сетевые пакеты помечены с использованием соответствующего значения DSCP, необходимо также создать новый параметр реестра на каждом компьютере, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c763f-166">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="c763f-167">Нажмите кнопку **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="c763f-167">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="c763f-168">В диалоговом окне " **выполнить** " введите **regedit** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c763f-168">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="c763f-169">В редакторе реестра разверните раздел **hKey \_ локальный \_ компьютер**, разверните раздел **система**, разверните **CurrentControlSet**, затем — **службы**, а затем — значок **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="c763f-169">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="c763f-170">Щелкните правой кнопкой мыши **tcpip**, наведите указатель на пункт **создать** и выберите **клавишу**.</span><span class="sxs-lookup"><span data-stu-id="c763f-170">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="c763f-171">После создания нового раздела реестра введите **QoS** и нажмите клавишу ВВОД, чтобы переименовать раздел.</span><span class="sxs-lookup"><span data-stu-id="c763f-171">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="c763f-172">Щелкните правой кнопкой мыши **QoS**, наведите указатель на пункт **создать** и выберите **строковое значение**.</span><span class="sxs-lookup"><span data-stu-id="c763f-172">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="c763f-173">После создания нового значения реестра введите команду не **использовать NLA** и нажмите клавишу ВВОД, чтобы переименовать значение.</span><span class="sxs-lookup"><span data-stu-id="c763f-173">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="c763f-174">Дважды щелкните **не использовать NLA**.</span><span class="sxs-lookup"><span data-stu-id="c763f-174">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="c763f-175">В диалоговом окне **изменение строки** введите **1** в поле **значение** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c763f-175">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="c763f-176">Закройте редактор реестра и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="c763f-176">Close the Registry Editor and then reboot your computer.</span></span>

<span data-ttu-id="c763f-177"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c763f-177"></div>

<span> </span>

</div>

</div>

</span></span></div>

