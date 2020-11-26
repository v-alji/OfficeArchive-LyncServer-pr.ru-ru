---
title: 'Lync Server 2013: Настройка политик качества обслуживания для клиентов, работающих в Windows 7 или Windows 8'
description: 'Lync Server 2013: Настройка политик качества обслуживания для клиентов, работающих под управлением Windows 7 или Windows 8.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service policies for clients running on Windows 7 or Windows 8
ms:assetid: efff2b98-b3fb-4183-a4f0-329a9105ce2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205371(v=OCS.15)
ms:contentKeyID: 48185785
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: faba5fc54ef73bfc738f94ee7209fc46a7cdc208
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432697"
---
# <a name="configuring-quality-of-service-policies-in-lync-server-2013-for-clients-running-on-windows-7-or-windows-8"></a><span data-ttu-id="5f699-103">Настройка политик качества обслуживания в Lync Server 2013 для клиентов, работающих под управлением Windows 7 или Windows 8</span><span class="sxs-lookup"><span data-stu-id="5f699-103">Configuring Quality of Service policies in Lync Server 2013 for clients running on Windows 7 or Windows 8</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f699-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f699-104">

<span> </span></span></span>

<span data-ttu-id="5f699-105">_**Тема последнего изменения:** 2016-03-29_</span><span class="sxs-lookup"><span data-stu-id="5f699-105">_**Topic Last Modified:** 2016-03-29_</span></span>

<span data-ttu-id="5f699-106">Помимо задания диапазонов портов для использования клиентами Lync, необходимо также создать отдельные политики качества обслуживания, которые будут применяться на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="5f699-106">In addition to specifying port ranges for use by your Lync clients you must also create separate Quality of Service policies that will be applied to client computers.</span></span> <span data-ttu-id="5f699-107">(Политики качества обслуживания, созданные для конференций, приложений и серверов-исправлений, не следует применять на клиентских компьютерах.) Эти сведения применимы только к компьютерам, на которых установлен клиент Lync 2013 и Windows 7 или Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f699-107">(The Quality of Service policies created for Conferencing, Application, and Mediation servers should not be applied to client computers.) This information applies only to computers running the Lync 2013 client and either Windows 7 or Windows 8.</span></span>

<span data-ttu-id="5f699-108">В следующем примере используется набор диапазонов портов для создания политики голосовой и видеополитики.</span><span class="sxs-lookup"><span data-stu-id="5f699-108">The following example uses this set of port ranges to create an audio policy and a video policy:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f699-109">Тип трафика клиента</span><span class="sxs-lookup"><span data-stu-id="5f699-109">Client Traffic Type</span></span></th>
<th><span data-ttu-id="5f699-110">Начало порта</span><span class="sxs-lookup"><span data-stu-id="5f699-110">Port Start</span></span></th>
<th><span data-ttu-id="5f699-111">Диапазон портов</span><span class="sxs-lookup"><span data-stu-id="5f699-111">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f699-112">Звук</span><span class="sxs-lookup"><span data-stu-id="5f699-112">Audio</span></span></p></td>
<td><p><span data-ttu-id="5f699-113">50020</span><span class="sxs-lookup"><span data-stu-id="5f699-113">50020</span></span></p></td>
<td><p><span data-ttu-id="5f699-114">средняя</span><span class="sxs-lookup"><span data-stu-id="5f699-114">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f699-115">Видео</span><span class="sxs-lookup"><span data-stu-id="5f699-115">Video</span></span></p></td>
<td><p><span data-ttu-id="5f699-116">58000</span><span class="sxs-lookup"><span data-stu-id="5f699-116">58000</span></span></p></td>
<td><p><span data-ttu-id="5f699-117">средняя</span><span class="sxs-lookup"><span data-stu-id="5f699-117">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f699-118">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="5f699-118">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="5f699-119">42000</span><span class="sxs-lookup"><span data-stu-id="5f699-119">42000</span></span></p></td>
<td><p><span data-ttu-id="5f699-120">средняя</span><span class="sxs-lookup"><span data-stu-id="5f699-120">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f699-121">Передача файлов</span><span class="sxs-lookup"><span data-stu-id="5f699-121">File transfer</span></span></p></td>
<td><p><span data-ttu-id="5f699-122">42020</span><span class="sxs-lookup"><span data-stu-id="5f699-122">42020</span></span></p></td>
<td><p><span data-ttu-id="5f699-123">средняя</span><span class="sxs-lookup"><span data-stu-id="5f699-123">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f699-124">Чтобы создать политику звука качества обслуживания для компьютеров с Windows 7 или Windows 8, сначала войдите на компьютер, на котором установлен компонент управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="5f699-124">To create a Quality of Service audio policy for Windows 7 or Windows 8 computers, first log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="5f699-125">Откройте средство управления групповыми политиками (нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Управление групповыми политиками**), а затем выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5f699-125">Open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following procedure:</span></span>

1.  <span data-ttu-id="5f699-126">В разделе Управление групповой политикой найдите контейнер, в котором нужно создать новую политику.</span><span class="sxs-lookup"><span data-stu-id="5f699-126">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="5f699-127">Например, если все клиентские компьютеры находятся в подразделении "клиенты", в подразделении клиента следует создать новую политику.</span><span class="sxs-lookup"><span data-stu-id="5f699-127">For example, if all your client computers are located in an OU named Clients then the new policy should be created in the Client OU.</span></span>

2.  <span data-ttu-id="5f699-128">Щелкните правой кнопкой мыши соответствующий контейнер и выберите команду **создать объект групповой политики в этом домене и свяжите его**.</span><span class="sxs-lookup"><span data-stu-id="5f699-128">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="5f699-129">В диалоговом окне **создание GPO** введите имя нового объекта групповой политики в поле **имя** (например, в **Lync Audio**) и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f699-129">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="5f699-130">Щелкните созданную политику правой кнопкой мыши и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="5f699-130">Right-click the newly-created policy and then click **Edit**.</span></span>

5.  <span data-ttu-id="5f699-131">В редакторе управления групповыми политиками разверните узел **Конфигурация компьютера**, выберите пункт **политики**, разверните раздел **Параметры Windows**, щелкните правой кнопкой мыши службу **QoS на основе политики** и выберите команду **создать новую политику**.</span><span class="sxs-lookup"><span data-stu-id="5f699-131">In the Group Policy Management Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

6.  <span data-ttu-id="5f699-132">В диалоговом окне **QoS на основе политики** на первой странице в поле **имя** введите имя новой политики (например, в **Lync Audio**).</span><span class="sxs-lookup"><span data-stu-id="5f699-132">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Audio**) in the **Name** box.</span></span> <span data-ttu-id="5f699-133">Выберите **задать значение DSCP** и задайте значение **46**.</span><span class="sxs-lookup"><span data-stu-id="5f699-133">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="5f699-134">Оставьте параметр **задать частоту исходящих подключений** невыбранным и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5f699-134">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

7. <span data-ttu-id="5f699-135">На следующей странице выберите **только приложения с именем исполняемого файла** и введите имя **Lync.exe** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5f699-135">On the next page, select **Only applications with this executable name** and enter the name **Lync.exe**, and then click **Next**.</span></span> <span data-ttu-id="5f699-136">Этот параметр дает политике приоритет только для трафика, соответствующего клиенту Lync.</span><span class="sxs-lookup"><span data-stu-id="5f699-136">This setting instructs the policy to only prioritize matching traffic from the Lync client.</span></span>

8.  <span data-ttu-id="5f699-137">На третьей странице убедитесь, что выбраны оба **IP-адреса источника** и **конечный IP-адрес** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5f699-137">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="5f699-138">Эти два параметра гарантируют, что пакеты будут управляться независимо от того, на каком компьютере (IP-адрес) отправили эти пакеты, и какой компьютер (IP-адрес) будет получать эти пакеты.</span><span class="sxs-lookup"><span data-stu-id="5f699-138">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

9.  <span data-ttu-id="5f699-139">На четвертой странице в раскрывающемся списке выберите протокол **TCP и UDP** , который будет **применяться этой политикой QoS** .</span><span class="sxs-lookup"><span data-stu-id="5f699-139">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="5f699-140">Протокол TCP и протокол UDP (User Datagram Protocol) — это два сетевых протокола, которые чаще всего используются в Lync Server и клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="5f699-140">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

10. <span data-ttu-id="5f699-141">Под заголовком **укажите номер исходного порта**, выберите **из этого исходного порта или диапазона**.</span><span class="sxs-lookup"><span data-stu-id="5f699-141">Under the heading **Specify the source port number**, select **From this source port or range**.</span></span> <span data-ttu-id="5f699-142">В сопроводительном текстовом поле введите диапазон портов, зарезервированный для передачи звука.</span><span class="sxs-lookup"><span data-stu-id="5f699-142">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="5f699-143">Например, если вы зарезервированы порты 50020 через порты 50039 для звукового трафика, введите диапазон портов в следующем формате: **50020:50039**.</span><span class="sxs-lookup"><span data-stu-id="5f699-143">For example, if you reserved ports 50020 through ports 50039 for audio traffic enter the port range using this format: **50020:50039**.</span></span> <span data-ttu-id="5f699-144">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="5f699-144">Click **Finish**.</span></span>

<span data-ttu-id="5f699-145">После создания политики качества обслуживания для звука вы должны создать вторую политику для видео.</span><span class="sxs-lookup"><span data-stu-id="5f699-145">After you have created the QoS policy for audio you should then create a second policy for video.</span></span> <span data-ttu-id="5f699-146">Чтобы создать политику для видео, выполните те же действия, что и при создании политики звука, заменив указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="5f699-146">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="5f699-147">Используйте другое (и уникальное) имя политики (например, **видео Lync**).</span><span class="sxs-lookup"><span data-stu-id="5f699-147">Use a different (and unique) policy name (for example, **Lync Video**).</span></span>

  - <span data-ttu-id="5f699-148">Задайте для параметра DSCP значение **34** вместо 46.</span><span class="sxs-lookup"><span data-stu-id="5f699-148">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="5f699-149">(Как отмечалось ранее, вам не нужно использовать значение DSCP 34; вы просто должны назначить другое значение DSCP, отличное от используемого для звука.)</span><span class="sxs-lookup"><span data-stu-id="5f699-149">(As noted previously, you do not have to use the DSCP value 34; you simply must assign a different DSCP value than the one used for audio.)</span></span>

  - <span data-ttu-id="5f699-150">Используйте ранее настроенный диапазон портов для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="5f699-150">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="5f699-151">Например, если у вас есть резервированные порты 58000 – 58019 для видео, задайте диапазон портов следующим образом: **58000:58019**.</span><span class="sxs-lookup"><span data-stu-id="5f699-151">For example, if you have reserved ports 58000 through 58019 for video, then set the port range to this: **58000:58019**.</span></span>

<span data-ttu-id="5f699-152">Если вы решили создать политику для управления трафиком общего использования приложений, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="5f699-152">If you decide to create a policy for managing application sharing traffic make these substitutions:</span></span>

  - <span data-ttu-id="5f699-153">Используйте другое (и уникальное) имя политики (например, **общий доступ к приложениям Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="5f699-153">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="5f699-154">Задайте для параметра DSCP значение **24** , а не 46.</span><span class="sxs-lookup"><span data-stu-id="5f699-154">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="5f699-155">(Опять же, это значение не обязательно должно быть 24; оно будет отличаться от значений DSCP, используемых для аудио-и видеофайлов.)</span><span class="sxs-lookup"><span data-stu-id="5f699-155">(Again, this value does not have to be 24; it simply must be different than the DSCP values used for audio and for video.)</span></span>

  - <span data-ttu-id="5f699-156">Используйте ранее настроенный диапазон портов для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="5f699-156">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="5f699-157">Например, если у вас есть резервированные порты 42000 – 42019 для совместного использования приложений, задайте диапазон портов следующим образом: **42000:42019**.</span><span class="sxs-lookup"><span data-stu-id="5f699-157">For example, if you have reserved ports 42000 through 42019 for application sharing, then set the port range to this: **42000:42019**.</span></span>

<span data-ttu-id="5f699-158">Для политики передачи файлов выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5f699-158">For a file transfer policy:</span></span>

  - <span data-ttu-id="5f699-159">Используйте другое (и уникальное) имя политики (например, " **Передача файлов в Lync Server**").</span><span class="sxs-lookup"><span data-stu-id="5f699-159">Use a different (and unique) policy name (for example, **Lync Server File Transfers**).</span></span>

  - <span data-ttu-id="5f699-160">Задайте для параметра DSCP значение **14**.</span><span class="sxs-lookup"><span data-stu-id="5f699-160">Set the DSCP value to **14**.</span></span> <span data-ttu-id="5f699-161">(Опять же, это значение не обязательно должно быть 14; оно просто должен быть уникальным кодом DSCP.)</span><span class="sxs-lookup"><span data-stu-id="5f699-161">(Again, this value does not have to be 14; it simply must be a unique DSCP code.)</span></span>

  - <span data-ttu-id="5f699-162">Используйте ранее настроенный диапазон портов для приложения.</span><span class="sxs-lookup"><span data-stu-id="5f699-162">Use the previously-configured port range for application.</span></span> <span data-ttu-id="5f699-163">Например, если у вас есть резервированные порты 42020 – 42039 для совместного использования приложений, задайте диапазон портов следующим образом: **42020:42039**.</span><span class="sxs-lookup"><span data-stu-id="5f699-163">For example, if you have reserved ports 42020 through 42039 for application sharing, then set the port range to this: **42020:42039**.</span></span>

<span data-ttu-id="5f699-164">Новые политики, созданные вами, вступят в силу только после обновления групповой политики на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="5f699-164">The new policies you have created will not take effect until Group Policy has been refreshed on your client computers.</span></span> <span data-ttu-id="5f699-165">Хотя групповая политика периодически обновляется сама, вы можете обновить ее принудительно, запустив на каждом нужном компьютере следующую команду.</span><span class="sxs-lookup"><span data-stu-id="5f699-165">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="5f699-166">Команду можно выполнить в любом командном окне, запущенном от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="5f699-166">This command can be run from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="5f699-167">Чтобы открыть такое окно с правами администратора, в меню **Пуск** правой кнопкой мыши щелкните **Командная строка** и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="5f699-167">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="5f699-168">Имейте в виду, что эти политики должны быть нацелены на клиентские компьютеры.</span><span class="sxs-lookup"><span data-stu-id="5f699-168">Keep in mind that these policies should be targeted towards your client computers.</span></span> <span data-ttu-id="5f699-169">Они не должны применяться к серверам, использующим Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5f699-169">They should not be applied to servers running Lync Server.</span></span>

<span data-ttu-id="5f699-170">Чтобы убедиться в том, что сетевые пакеты помечены с использованием соответствующего значения DSCP, необходимо также создать новый параметр реестра на каждом компьютере, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5f699-170">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="5f699-171">Нажмите кнопку **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="5f699-171">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="5f699-172">В диалоговом окне " **выполнить** " введите **regedit** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="5f699-172">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="5f699-173">В редакторе реестра разверните раздел **hKey \_ локальный \_ компьютер**, разверните раздел **система**, разверните **CurrentControlSet**, затем — **службы**, а затем — значок **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="5f699-173">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="5f699-174">Щелкните правой кнопкой мыши **tcpip**, наведите указатель на пункт **создать** и выберите **клавишу**.</span><span class="sxs-lookup"><span data-stu-id="5f699-174">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="5f699-175">После создания нового раздела реестра введите **QoS** и нажмите клавишу ВВОД, чтобы переименовать раздел.</span><span class="sxs-lookup"><span data-stu-id="5f699-175">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="5f699-176">Щелкните правой кнопкой мыши **QoS**, наведите указатель на пункт **создать** и выберите **строковое значение**.</span><span class="sxs-lookup"><span data-stu-id="5f699-176">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="5f699-177">После создания нового значения реестра введите команду не **использовать NLA** и нажмите клавишу ВВОД, чтобы переименовать значение.</span><span class="sxs-lookup"><span data-stu-id="5f699-177">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="5f699-178">Дважды щелкните **не использовать NLA**.</span><span class="sxs-lookup"><span data-stu-id="5f699-178">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="5f699-179">В диалоговом окне **изменение строки** введите **1** в поле **значение** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f699-179">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="5f699-180">Закройте редактор реестра и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="5f699-180">Close the Registry Editor and then reboot your computer.</span></span>

<div>

## <a name="configuring-quality-of-service-on-computers-with-multiple-network-adapters"></a><span data-ttu-id="5f699-181">Настройка качества обслуживания на компьютерах с несколькими сетевыми адаптерами</span><span class="sxs-lookup"><span data-stu-id="5f699-181">Configuring Quality of Service on Computers with Multiple Network Adapters</span></span>

<span data-ttu-id="5f699-182">Если у вас есть компьютер с несколькими сетевыми адаптерами, вы можете столкнуться с проблемами, где значения DSCP отображаются как 0x00, а не как настроенное значение.</span><span class="sxs-lookup"><span data-stu-id="5f699-182">If you have a computer that has multiple network adapters you might occasionally run into issues where DSCP values are shown as 0x00 rather than the configured value.</span></span> <span data-ttu-id="5f699-183">Обычно это происходит на компьютерах, на которых один или несколько сетевых адаптеров не могут получить доступ к домену Active Directory (например, если эти адаптеры используются для частной сети).</span><span class="sxs-lookup"><span data-stu-id="5f699-183">This will typically occur on computers where one or more of the network adapters are not able to access your Active Directory domain (for example, if these adapters are used for a private network).</span></span> <span data-ttu-id="5f699-184">В таких случаях значения DSCP будут помечены для адаптеров, которые могут получить доступ к домену, но не будут помечены для адаптеров, которые не могут получить доступ к домену.</span><span class="sxs-lookup"><span data-stu-id="5f699-184">In cases like that, DSCP values will be tagged for the adapters that can access the domain, but will not be tagged for adapters that cannot access the domain.</span></span>

<span data-ttu-id="5f699-185">Если вы хотите пометить значения DSCP для всех сетевых адаптеров на компьютере, в том числе для тех, у которых нет доступа к вашему домену, вам нужно будет добавить в реестр значение и настроить его.</span><span class="sxs-lookup"><span data-stu-id="5f699-185">If you would like to tag DSCP values for all the network adapters in a computer, including adapters that do not have access to your domain, then you will need to add and configure a value to the registry.</span></span> <span data-ttu-id="5f699-186">Это можно сделать, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5f699-186">That can be done by completing the following procedure:</span></span>

1.  <span data-ttu-id="5f699-187">Нажмите кнопку **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="5f699-187">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="5f699-188">В диалоговом окне " **выполнить** " введите **regedit** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="5f699-188">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="5f699-189">В редакторе реестра разверните раздел **hKey \_ локальный \_ компьютер**, разверните раздел **система**, разверните **CurrentControlSet**, затем — **службы**, а затем — значок **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="5f699-189">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="5f699-190">Если вы не видите раздел реестра с меткой **QoS** , щелкните правой кнопкой мыши **tcpip** и выберите пункт **создать**, а затем — **раздел**.</span><span class="sxs-lookup"><span data-stu-id="5f699-190">If you do not see a registry key labeled **QoS** then right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="5f699-191">После создания нового ключа введите **QoS** и нажмите клавишу ВВОД, чтобы переименовать раздел.</span><span class="sxs-lookup"><span data-stu-id="5f699-191">After the new key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="5f699-192">Щелкните правой кнопкой мыши **QoS**, наведите указатель на пункт **создать** и выберите **строковое значение**.</span><span class="sxs-lookup"><span data-stu-id="5f699-192">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="5f699-193">После создания нового значения реестра введите команду не **использовать NLA** и нажмите клавишу ВВОД, чтобы переименовать значение.</span><span class="sxs-lookup"><span data-stu-id="5f699-193">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="5f699-194">Дважды щелкните **не использовать NLA**.</span><span class="sxs-lookup"><span data-stu-id="5f699-194">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="5f699-195">В диалоговом окне **изменение строки** введите **1** в поле **значение** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f699-195">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

<span data-ttu-id="5f699-196">После создания и настройки нового значения реестра вам потребуется перезагрузить компьютер, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="5f699-196">After creating and configuring the new registry value you will need to reboot your computer in order for the changes to take effect.</span></span>

<span data-ttu-id="5f699-197"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f699-197"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

