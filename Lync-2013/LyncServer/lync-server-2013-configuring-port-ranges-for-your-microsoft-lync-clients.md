---
title: 'Lync Server 2013: Настройка диапазонов портов для клиентов Microsoft Lync'
description: 'Lync Server 2013: Настройка диапазонов портов для клиентов Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Microsoft Lync clients
ms:assetid: 287d5cea-7ada-461c-9b4a-9da2af315e71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204760(v=OCS.15)
ms:contentKeyID: 48183694
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e7fcabf81f8e0110010b1a4fb8e697fb0da986c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432732"
---
# <a name="configuring-port-ranges-for-your-microsoft-lync-clients-in-lync-server-2013"></a><span data-ttu-id="60c03-103">Настройка диапазонов портов для клиентов Microsoft Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60c03-103">Configuring port ranges for your Microsoft Lync clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="60c03-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="60c03-104">

<span> </span></span></span>

<span data-ttu-id="60c03-105">_**Тема последнего изменения:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="60c03-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="60c03-106">По умолчанию клиентские приложения Lync могут использовать любой порт между портами 1024 и 65535 при включении в сеанс связи. Это происходит из-за того, что определенные диапазоны портов не включены автоматически для клиентов.</span><span class="sxs-lookup"><span data-stu-id="60c03-106">By default, Lync client applications can use any port between ports 1024 and 65535 when involved in a communication session; this is because specific port ranges are not automatically enabled for clients.</span></span> <span data-ttu-id="60c03-107">Тем не менее, чтобы использовать качество обслуживания, вам потребуется переназначить различные типы трафика (звук, видео, мультимедиа, общий доступ к приложениям и передачу файлов) на ряд уникальных диапазонов портов.</span><span class="sxs-lookup"><span data-stu-id="60c03-107">In order to use Quality of Service, however, you will need to reassign the various traffic types (audio, video, media, application sharing, and file transfer) to a series of unique port ranges.</span></span> <span data-ttu-id="60c03-108">Это можно сделать с помощью командлета Set-CsConferencingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="60c03-108">This can be done by using the Set-CsConferencingConfiguration cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="60c03-109">Конечные пользователи не могут вносить эти изменения.</span><span class="sxs-lookup"><span data-stu-id="60c03-109">End users cannot make these changes themselves.</span></span> <span data-ttu-id="60c03-110">Изменения портов могут вносить только администраторы с помощью командлета Set-CsConferencingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="60c03-110">Port changes can only be made by administrators using the Set-CsConferencingConfiguration cmdlet.</span></span>



</div>

<span data-ttu-id="60c03-111">Вы можете определить, какие диапазоны портов используются в сеансах связи, выполнив следующую команду в командной консоли Microsoft Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="60c03-111">You can determine which port ranges are currently used for communication sessions by running the following command from within the Microsoft Lync Server 2013 Management Shell:</span></span>

    Get-CsConferencingConfiguration

<span data-ttu-id="60c03-112">Если вы не внесли никаких изменений в параметры конференц-связи после установки Lync Server 2013, вы должны получить информацию, которая включает следующие значения свойств.</span><span class="sxs-lookup"><span data-stu-id="60c03-112">Assuming that you have not made any changes to your conferencing settings since you installed Lync Server 2013, you should get back information that includes these property values:</span></span>

    ClientMediaPortRangeEnabled : False
    ClientAudioPort             : 5350
    ClientAudioPortRange        : 40
    ClientVideoPort             : 5350
    ClientVideoPortRange        : 40
    ClientAppSharingPort        : 5350
    ClientAppSharingPortRange   : 40
    ClientFileTransferPort      : 5350
    ClientTransferPortRange     : 40

<span data-ttu-id="60c03-113">Если вы ближе просмотрит предыдущий результат, вы увидите два важных элемента.</span><span class="sxs-lookup"><span data-stu-id="60c03-113">If you look closely at the preceding output, you'll see two things of importance.</span></span> <span data-ttu-id="60c03-114">Сначала свойство ClientMediaPortRangeEnabled имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="60c03-114">First, the ClientMediaPortRangeEnabled property is set to False:</span></span>

    ClientMediaPortRangeEnabled : False

<span data-ttu-id="60c03-115">Это важно, так как, если для этого свойства задано значение false, клиенты Lync будут использовать любой доступный порт между портами 1024 и 65535 при включении в сеанс связи. Это справедливо независимо от других параметров порта (например, ClientMediaPort или ClientVideoPort).</span><span class="sxs-lookup"><span data-stu-id="60c03-115">That's important because, when this property is set to False, Lync clients will use any available port between ports 1024 and 65535 when involved in a communication session; this is true regardless of any other port settings (for example, ClientMediaPort or ClientVideoPort).</span></span> <span data-ttu-id="60c03-116">Если вы хотите ограничить использование заданным набором портов (и это нужно сделать, если вы планируете реализовать качество обслуживания), необходимо сначала включить диапазоны портов клиента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="60c03-116">If you want to restrict usage to a specified set of ports (and this is something you do want to do if you plan on implementing Quality of Service) then you must first enable client media port ranges.</span></span> <span data-ttu-id="60c03-117">Это можно сделать с помощью следующей команды Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="60c03-117">That can be done using the following Windows PowerShell command:</span></span>

    Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True

<span data-ttu-id="60c03-118">Предыдущая команда включает диапазоны порта клиента мультимедиа для глобальной коллекции параметров конфигурации конференций. Однако эти параметры также можно применять к области действия сайта и (или) области службы (только для службы сервера конференц-связи).</span><span class="sxs-lookup"><span data-stu-id="60c03-118">The preceding command enables client media port ranges for the global collection of conferencing configuration settings; however, these settings can also be applied to the site scope and/or the service scope (for the Conferencing Server service only).</span></span> <span data-ttu-id="60c03-119">Чтобы включить диапазон портов клиента мультимедиа для определенного сайта или сервера, укажите удостоверение этого сайта или сервера при вызове Set-CsConferencingConfiguration:</span><span class="sxs-lookup"><span data-stu-id="60c03-119">To enable client media port ranges for a specific site or server, specify the Identity of that site or server when calling Set-CsConferencingConfiguration:</span></span>

    Set-CsConferencingConfiguration -Identity "site:Redmond" -ClientMediaPortRangeEnabled $True

<span data-ttu-id="60c03-120">Кроме того, вы можете использовать эту команду для одновременного включения диапазонов портов для всех параметров настройки конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="60c03-120">Alternatively, you can use this command to simultaneously enable port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration  -ClientMediaPortRangeEnabled $True

<span data-ttu-id="60c03-121">Во втором случае важно заметить, что в примере вывода показано, что по умолчанию диапазоны портов мультимедиа, заданные для каждого типа сетевого трафика, идентичны:</span><span class="sxs-lookup"><span data-stu-id="60c03-121">The second thing of importance you will notice is that the sample output shows that, by default, the media port ranges set for each type of network traffic are identical:</span></span>

    ClientAudioPort             : 5350
    ClientVideoPort             : 5350
    ClientAppSharingPort        : 5350
    ClientFileTransferPort      : 5350

<span data-ttu-id="60c03-122">Для реализации QoS каждый из этих диапазонов должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="60c03-122">In order to implement QoS, each of these port ranges will need to be unique.</span></span> <span data-ttu-id="60c03-123">Например, вы можете настроить диапазоны портов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="60c03-123">For example, you might configure the port ranges like this:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60c03-124">Тип трафика клиента</span><span class="sxs-lookup"><span data-stu-id="60c03-124">Client Traffic Type</span></span></th>
<th><span data-ttu-id="60c03-125">Начало порта</span><span class="sxs-lookup"><span data-stu-id="60c03-125">Port Start</span></span></th>
<th><span data-ttu-id="60c03-126">Диапазон портов</span><span class="sxs-lookup"><span data-stu-id="60c03-126">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60c03-127">Звук</span><span class="sxs-lookup"><span data-stu-id="60c03-127">Audio</span></span></p></td>
<td><p><span data-ttu-id="60c03-128">50020</span><span class="sxs-lookup"><span data-stu-id="60c03-128">50020</span></span></p></td>
<td><p><span data-ttu-id="60c03-129">средняя</span><span class="sxs-lookup"><span data-stu-id="60c03-129">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c03-130">Видео</span><span class="sxs-lookup"><span data-stu-id="60c03-130">Video</span></span></p></td>
<td><p><span data-ttu-id="60c03-131">58000</span><span class="sxs-lookup"><span data-stu-id="60c03-131">58000</span></span></p></td>
<td><p><span data-ttu-id="60c03-132">средняя</span><span class="sxs-lookup"><span data-stu-id="60c03-132">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c03-133">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="60c03-133">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="60c03-134">42000</span><span class="sxs-lookup"><span data-stu-id="60c03-134">42000</span></span></p></td>
<td><p><span data-ttu-id="60c03-135">средняя</span><span class="sxs-lookup"><span data-stu-id="60c03-135">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c03-136">Передача файлов</span><span class="sxs-lookup"><span data-stu-id="60c03-136">File transfer</span></span></p></td>
<td><p><span data-ttu-id="60c03-137">42020</span><span class="sxs-lookup"><span data-stu-id="60c03-137">42020</span></span></p></td>
<td><p><span data-ttu-id="60c03-138">средняя</span><span class="sxs-lookup"><span data-stu-id="60c03-138">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60c03-139">В приведенной выше таблице диапазоны портов клиента представляют собой подмножество диапазонов портов, настроенных для серверов.</span><span class="sxs-lookup"><span data-stu-id="60c03-139">In the preceding table, client port ranges represent a subset of the port ranges configured for your servers.</span></span> <span data-ttu-id="60c03-140">Например, на серверах общий доступ к приложениям настроен на использование портов 40803 – 49151; на клиентских компьютерах общий доступ к приложениям настроен на использование портов 42000 – 42019.</span><span class="sxs-lookup"><span data-stu-id="60c03-140">For example, on the servers, application sharing was configured to use ports 40803 through 49151; on the client computers, application sharing is configured to use ports 42000 through 42019.</span></span> <span data-ttu-id="60c03-141">Это также необходимо сделать, чтобы упростить администрирование QoS: портам клиента не нужно представлять подмножество портов, используемых на сервере.</span><span class="sxs-lookup"><span data-stu-id="60c03-141">This, too is done primarily to make administration of QoS easier: client ports do not have to represent a subset of the ports used on the server.</span></span> <span data-ttu-id="60c03-142">(Например, на клиентских компьютерах вы можете настроить общий доступ к приложениям, например, с помощью портов 10000 – 10019.) Тем не менее рекомендуется сделать порт клиента подмножеством диапазонов портов сервера.</span><span class="sxs-lookup"><span data-stu-id="60c03-142">(For example, on the client computers you could configure application sharing to use, say, ports 10000 through 10019.) However, it is recommended that you make your client port ranges a subset of your server port ranges.</span></span>

<span data-ttu-id="60c03-143">Кроме того, вы могли заметить, что порты 8348 были настроены для совместного использования приложений на серверах, но для совместного использования приложений на клиентских компьютерах задано только 20 портов.</span><span class="sxs-lookup"><span data-stu-id="60c03-143">In addition, you might have noticed that 8348 ports were set aside for application sharing on the servers, but only 20 ports were set aside for application sharing on the clients.</span></span> <span data-ttu-id="60c03-144">Это, как правило, рекомендуется, но не является жесткой и быстрой.</span><span class="sxs-lookup"><span data-stu-id="60c03-144">This, too is recommended, but is not a hard-and-fast rule.</span></span> <span data-ttu-id="60c03-145">Как правило, вы можете использовать каждый доступный порт для представления одного сеанса связи: Если в диапазоне портов есть доступные порты 100, то в любой момент времени компьютер может принимать участие в сеансах связи 100.</span><span class="sxs-lookup"><span data-stu-id="60c03-145">In general, you can consider each available port to represent a single communication session: if you have 100 ports available in a port range that means that the computer in question could participate in, at most, 100 communication sessions at any given time.</span></span> <span data-ttu-id="60c03-146">Поскольку серверы, скорее чем, будут работать в большинстве сеансов, чем клиенты, имеет смысл открыть на серверах больше портов, чем на клиентах.</span><span class="sxs-lookup"><span data-stu-id="60c03-146">Because servers will likely take part in many more conversations than clients, it makes sense to open many more ports on servers than on clients.</span></span> <span data-ttu-id="60c03-147">Настройка 20 портов для совместного использования приложений на клиенте означает, что пользователь может принимать участие в 20 сеансах общего разделения приложений на указанном устройстве и одновременно.</span><span class="sxs-lookup"><span data-stu-id="60c03-147">Setting aside 20 ports for application sharing on a client means that a user could participate in 20 application sharing sessions on the specified device, and all at the same time.</span></span> <span data-ttu-id="60c03-148">Это должно быть достаточно для самых разнообразных пользователей.</span><span class="sxs-lookup"><span data-stu-id="60c03-148">That should prove sufficient for the vast majority of your users.</span></span>

<span data-ttu-id="60c03-149">Чтобы назначить предыдущие диапазоны портов для глобальной коллекции параметров настройки конференц-связи, вы можете использовать следующую команду оболочки Lync Server Management Shell:</span><span class="sxs-lookup"><span data-stu-id="60c03-149">To assign the preceding port ranges to your global collection of conferencing configuration settings you can use the following Lync Server Management Shell command:</span></span>

    Set-CsConferencingConfiguration -Identity global -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="60c03-150">Кроме того, можно использовать эту команду для назначения одинаковых диапазонов портов для всех параметров настройки конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="60c03-150">Or, use this command to assign these same port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="60c03-151">Чтобы изменения вступили в силу, пользователи должны выйти из Lync, а затем снова войти в систему.</span><span class="sxs-lookup"><span data-stu-id="60c03-151">Individual users must log off from Lync and then log back on before these changes will actually take effect.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="60c03-152">Вы также можете включить диапазоны портов клиента мультимедиа, а затем назначить эти диапазоны портов с помощью одной команды.</span><span class="sxs-lookup"><span data-stu-id="60c03-152">You can also enable client media port ranges, and then assign those port ranges, using a single command.</span></span> <span data-ttu-id="60c03-153">Например:</span><span class="sxs-lookup"><span data-stu-id="60c03-153">For example:</span></span><BR><CODE>Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 -ClientFileTransferPort 42020 -ClientFileTransferPortRange 20</CODE>



<span data-ttu-id="60c03-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="60c03-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

