---
title: Настройка политики качества обслуживания для пограничного сервера/V Edge
description: Настройка политики качества обслуживания для пограничного сервера/V.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a Quality of Service policy for your A/V Edge Servers
ms:assetid: 119ee1f5-45b9-40ba-98e5-c694dd2fc5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204681(v=OCS.15)
ms:contentKeyID: 48183444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec1f012260aa32df984925a86882a3201e07db0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433509"
---
# <a name="configuring-a-quality-of-service-policy-for-your-av-edge-servers-in-lync-server-2013"></a><span data-ttu-id="4f127-103">Настройка политики качества обслуживания для пограничного сервера/V в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f127-103">Configuring a Quality of Service policy for your A/V Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f127-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f127-104">

<span> </span></span></span>

<span data-ttu-id="4f127-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="4f127-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="4f127-106">Кроме того, чтобы создавать политики QoS для конференций, приложений и серверов исправлений, вам также необходимо создать как голосовые, так и видеополитики для внутренней стороны пограничных серверов A/V.</span><span class="sxs-lookup"><span data-stu-id="4f127-106">In addition to creating QoS policies for your Conferencing, Application, and Mediation servers, you must also create both audio and video policies for the internal side of your A/V Edge servers.</span></span> <span data-ttu-id="4f127-107">Тем не менее политики, используемые на пограничных серверах, отличаются от политик, используемых на серверах конференц-связи, приложений и исправлений.</span><span class="sxs-lookup"><span data-stu-id="4f127-107">However, the policies used on your Edge servers are different from the policies used on your Conferencing, Application, and Mediation servers.</span></span> <span data-ttu-id="4f127-108">Для серверов конференций, приложений и исправлений вы указали диапазон портов источника; При использовании пограничных серверов необходимо указать диапазон портов назначения.</span><span class="sxs-lookup"><span data-stu-id="4f127-108">For the Conferencing, Application, and Mediation servers you specified a source port range; with Edge servers, you need to specify a destination port range.</span></span> <span data-ttu-id="4f127-109">Из-за того, что вы не можете просто применить политики качества обслуживания для конференц-связи, приложений и сервера исправлений на пограничные серверы: эти политики просто не работают.</span><span class="sxs-lookup"><span data-stu-id="4f127-109">Because of that you cannot simply apply the Conferencing, Application, and Mediation server QoS policies to your Edge servers: these policies simply won't work.</span></span> <span data-ttu-id="4f127-110">Вместо этого необходимо создать новые политики и применить эти политики только к пограничным серверам.</span><span class="sxs-lookup"><span data-stu-id="4f127-110">Instead, you must create new policies and apply those policies to your Edge servers only.</span></span>

<span data-ttu-id="4f127-111">Ниже описаны действия, которые необходимо выполнить для создания объектов групповой политики Active Directory, которые можно использовать для управления качеством обслуживания на пограничных серверах.</span><span class="sxs-lookup"><span data-stu-id="4f127-111">The following procedure describes the process for creating Active Directory Group Policy objects that can be used to manage Quality of Service on Edge Servers.</span></span> <span data-ttu-id="4f127-112">Разумеется, возможно, что пограничные серверы — это изолированные серверы, у которых нет учетных записей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f127-112">Of course, it's possible that your Edge servers are stand-alone servers that do not have Active Directory accounts.</span></span> <span data-ttu-id="4f127-113">В этом случае вы можете использовать локальную групповую политику вместо групповой политики Active Directory: Единственная разница заключается в том, что вы должны создавать эти локальные политики с помощью редактора локальных групповых политик и отдельно создавать одинаковый набор политик на каждом пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="4f127-113">If that's the case, you can use local Group Policy instead of Active Directory Group Policy: the only difference is that you must create these local policies using the Local Group Policy Editor, and must individually create the same set of policies on each Edge Server.</span></span> <span data-ttu-id="4f127-114">Чтобы запустить редактор локальной групповой политики на пограничном сервере, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4f127-114">To start the Local Group Policy Editor on an Edge server do the following:</span></span>

1.  <span data-ttu-id="4f127-115">Нажмите кнопку **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="4f127-115">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="4f127-116">В диалоговом окне **выполнить** введите **gpedit. msc** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="4f127-116">In the **Run** dialog box, type **gpedit.msc** and then press ENTER.</span></span>

<span data-ttu-id="4f127-117">Если вы создаете политики на основе Active Directory, вы должны войти на компьютер, на котором установлен компонент управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="4f127-117">If you are creating Active Directory-based policies, then you should log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="4f127-118">В этом случае откройте управление групповыми политиками (нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Управление групповой политикой**) и выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4f127-118">In that case, open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following steps:</span></span>

1.  <span data-ttu-id="4f127-119">В разделе Управление групповой политикой найдите контейнер, в котором нужно создать новую политику.</span><span class="sxs-lookup"><span data-stu-id="4f127-119">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="4f127-120">Например, если все компьютеры Lync Server находятся в подразделении с именем Lync Server, новую политику следует создать в OU сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4f127-120">For example, if all your Lync Server computers are located in an OU named Lync Server then the new policy should be created in the Lync Server OU.</span></span>

2.  <span data-ttu-id="4f127-121">Щелкните правой кнопкой мыши соответствующий контейнер и выберите команду **создать объект групповой политики в этом домене и свяжите его**.</span><span class="sxs-lookup"><span data-stu-id="4f127-121">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="4f127-122">В диалоговом окне **создание GPO** введите имя нового объекта групповой политики в поле **имя** (например, **Lync Server Audio**) и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4f127-122">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Server Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="4f127-123">Щелкните созданную политику правой кнопкой мыши и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="4f127-123">Right-click the newly-created policy and then click **Edit**.</span></span>

<span data-ttu-id="4f127-124">Здесь процесс идентичен, независимо от того, создается ли вы политика Active Directory или локальная политика.</span><span class="sxs-lookup"><span data-stu-id="4f127-124">From here the process is identical regardless of whether you are creating an Active Directory policy or a local policy:</span></span>

1.  <span data-ttu-id="4f127-125">В редакторе управления групповыми политиками или в редакторе локальных групповых политик разверните раздел **Конфигурация компьютера**, затем — **политики**, разверните раздел **Параметры Windows**, щелкните правой кнопкой мыши службу **QoS на основе политики**, а затем выберите команду **создать новую политику**.</span><span class="sxs-lookup"><span data-stu-id="4f127-125">In the Group Policy Management Editor or the Local Group Policy Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

2.  <span data-ttu-id="4f127-126">В диалоговом окне **QoS на основе политики** на первой странице в поле **имя** введите имя новой политики (например, **Lync Server Audio**).</span><span class="sxs-lookup"><span data-stu-id="4f127-126">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Server Audio**) in the **Name** box.</span></span> <span data-ttu-id="4f127-127">Выберите **задать значение DSCP** и задайте значение **46**.</span><span class="sxs-lookup"><span data-stu-id="4f127-127">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="4f127-128">Оставьте параметр **задать частоту исходящих подключений** невыбранным и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4f127-128">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

3.  <span data-ttu-id="4f127-129">На следующей странице убедитесь, что выбраны **все приложения** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4f127-129">On the next page, make sure that **All applications** is selected and then click **Next**.</span></span> <span data-ttu-id="4f127-130">Этот параметр предписывает сети искать все пакеты с разметкой DSCP для 46, а не только пакеты, созданные определенным приложением.</span><span class="sxs-lookup"><span data-stu-id="4f127-130">This setting instructs the network to look for all packets with a DSCP marking of 46, not just packets created by a specific application.</span></span>

4.  <span data-ttu-id="4f127-131">На третьей странице убедитесь, что выбраны оба **IP-адреса источника** и **конечный IP-адрес** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4f127-131">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="4f127-132">Эти два параметра гарантируют, что пакеты будут управляться независимо от того, на каком компьютере (IP-адрес) отправили эти пакеты, и какой компьютер (IP-адрес) будет получать эти пакеты.</span><span class="sxs-lookup"><span data-stu-id="4f127-132">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

5.  <span data-ttu-id="4f127-133">На четвертой странице в раскрывающемся списке выберите протокол **TCP и UDP** , который будет **применяться этой политикой QoS** .</span><span class="sxs-lookup"><span data-stu-id="4f127-133">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="4f127-134">Протокол TCP и протокол UDP (User Datagram Protocol) — это два сетевых протокола, которые чаще всего используются в Lync Server и клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="4f127-134">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

6.  <span data-ttu-id="4f127-135">В разделе заголовков **укажите номер порта назначения**, выберите один **из конечных портов или диапазонов**.</span><span class="sxs-lookup"><span data-stu-id="4f127-135">Under the heading **Specify the destination port number**, select **From this destination port or range**.</span></span> <span data-ttu-id="4f127-136">В сопроводительном текстовом поле введите диапазон портов, зарезервированный для передачи звука.</span><span class="sxs-lookup"><span data-stu-id="4f127-136">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="4f127-137">Например, если вы зарезервированы порты 49152 – порты 57500 для звукового трафика, введите диапазон портов в следующем формате: **49152:57500**.</span><span class="sxs-lookup"><span data-stu-id="4f127-137">For example, if you reserved ports 49152 through ports 57500 for audio traffic then enter the port range using this format: **49152:57500**.</span></span> <span data-ttu-id="4f127-138">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="4f127-138">Click **Finish**.</span></span>

<span data-ttu-id="4f127-139">После создания политики QoS для звукового трафика вы должны создать вторую политику для видеосеанса.</span><span class="sxs-lookup"><span data-stu-id="4f127-139">After you have created the QoS policy for audio traffic you should create a second policy for video traffic.</span></span> <span data-ttu-id="4f127-140">Чтобы создать политику для видео, выполните те же действия, что и при создании политики звука, заменив указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="4f127-140">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="4f127-141">Используйте другое (и уникальное) имя политики (например, **Lync Server Video**).</span><span class="sxs-lookup"><span data-stu-id="4f127-141">Use a different (and unique) policy name (for example, **Lync Server Video**).</span></span>

  - <span data-ttu-id="4f127-142">Задайте для параметра DSCP значение **34** вместо 46.</span><span class="sxs-lookup"><span data-stu-id="4f127-142">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="4f127-143">(Обратите внимание, что вам не нужно использовать значение DSCP для 34.</span><span class="sxs-lookup"><span data-stu-id="4f127-143">(Note that you do not have to use a DSCP value of 34.</span></span> <span data-ttu-id="4f127-144">Единственным требованием является использование другого значения DSCP для видео, чем вы использовали для звука.</span><span class="sxs-lookup"><span data-stu-id="4f127-144">The only requirement is that you use a different DSCP value for video than you used for audio.)</span></span>

  - <span data-ttu-id="4f127-145">Используйте ранее настроенный диапазон портов для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="4f127-145">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="4f127-146">Например, если у вас есть резервированные порты 57501 – 65535 для видео, задайте диапазон портов следующим образом: **57501:65535**.</span><span class="sxs-lookup"><span data-stu-id="4f127-146">For example, if you have reserved ports 57501 through 65535 for video, then set the port range to this: **57501:65535**.</span></span> <span data-ttu-id="4f127-147">Опять же, это значение должно быть задано в качестве диапазона портов назначения.</span><span class="sxs-lookup"><span data-stu-id="4f127-147">Again, this should be configured as the destination port range.</span></span>

<span data-ttu-id="4f127-148">Если вы решили создать политику для управления трафиком общего доступа к приложениям, вы должны создать третью политику, заменив указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="4f127-148">If you decide to create a policy for managing application sharing traffic you must create a third policy, making the following substitutions:</span></span>

  - <span data-ttu-id="4f127-149">Используйте другое (и уникальное) имя политики (например, **общий доступ к приложениям Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="4f127-149">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="4f127-150">Задайте для параметра DSCP значение **24** , а не 46.</span><span class="sxs-lookup"><span data-stu-id="4f127-150">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="4f127-151">(Опять же, вам не нужно использовать значение DSCP, равное 24.</span><span class="sxs-lookup"><span data-stu-id="4f127-151">(Again, you do not have to use a DSCP value of 24.</span></span> <span data-ttu-id="4f127-152">Единственным требованием является использование другого значения DSCP для общего пользования приложениями, чем при использовании звука или видео.)</span><span class="sxs-lookup"><span data-stu-id="4f127-152">The only requirement is that you use a different DSCP value for application sharing than you used for audio or for video.)</span></span>

  - <span data-ttu-id="4f127-153">Используйте ранее настроенный диапазон портов для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="4f127-153">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="4f127-154">Например, если у вас есть резервированные порты 40803 – 49151 для совместного использования приложений, задайте диапазон портов следующим образом: **40803:49151**.</span><span class="sxs-lookup"><span data-stu-id="4f127-154">For example, if you have reserved ports 40803 through 49151 for application sharing, then set the port range to this: **40803:49151**.</span></span>

<span data-ttu-id="4f127-155">Новые политики, созданные вами, вступят в силу только после обновления групповой политики на серверах пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="4f127-155">The new policies you have created will not take effect until Group Policy has been refreshed on your Edge servers.</span></span> <span data-ttu-id="4f127-156">Хотя групповая политика периодически обновляется сама, вы можете обновить ее принудительно, запустив на каждом нужном компьютере следующую команду.</span><span class="sxs-lookup"><span data-stu-id="4f127-156">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="4f127-157">Эту команду можно выполнить из Lync Server или из окна команд, которое запущено с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="4f127-157">This command can be run from within the Lync Server or from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="4f127-158">Чтобы открыть такое окно с правами администратора, в меню **Пуск** правой кнопкой мыши щелкните **Командная строка** и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="4f127-158">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span> <span data-ttu-id="4f127-159">Обратите внимание, что пограничный сервер может потребоваться перезапустить даже после запуска Gpudate.exe.</span><span class="sxs-lookup"><span data-stu-id="4f127-159">Note that you might need to restart the Edge server even after running Gpudate.exe.</span></span>

<span data-ttu-id="4f127-160">Чтобы убедиться в том, что сетевые пакеты помечены с использованием соответствующего значения DSCP, необходимо также создать новый параметр реестра на каждом компьютере, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4f127-160">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="4f127-161">Нажмите кнопку **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="4f127-161">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="4f127-162">В диалоговом окне " **выполнить** " введите **regedit** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="4f127-162">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="4f127-163">В редакторе реестра разверните раздел **hKey \_ локальный \_ компьютер**, разверните раздел **система**, разверните **CurrentControlSet**, затем — **службы**, а затем — значок **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="4f127-163">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="4f127-164">Щелкните правой кнопкой мыши **tcpip**, наведите указатель на пункт **создать** и выберите **клавишу**.</span><span class="sxs-lookup"><span data-stu-id="4f127-164">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="4f127-165">После создания нового раздела реестра введите **QoS** и нажмите клавишу ВВОД, чтобы переименовать раздел.</span><span class="sxs-lookup"><span data-stu-id="4f127-165">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="4f127-166">Щелкните правой кнопкой мыши **QoS**, наведите указатель на пункт **создать** и выберите **строковое значение**.</span><span class="sxs-lookup"><span data-stu-id="4f127-166">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="4f127-167">После создания нового значения реестра введите команду не **использовать NLA** и нажмите клавишу ВВОД, чтобы переименовать значение.</span><span class="sxs-lookup"><span data-stu-id="4f127-167">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="4f127-168">Дважды щелкните пункт **не использовать NLA**.</span><span class="sxs-lookup"><span data-stu-id="4f127-168">Double-click **Do no use NLA**.</span></span> <span data-ttu-id="4f127-169">В диалоговом окне **изменение строки** введите **1** в поле **значение** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4f127-169">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="4f127-170">Закройте редактор реестра и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="4f127-170">Close the Registry Editor and then reboot your computer.</span></span>

<span data-ttu-id="4f127-171"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f127-171"></div>

<span> </span>

</div>

</div>

</span></span></div>

