---
title: 'Lync Server 2013: Управление качеством обслуживания (QoS)'
description: 'Lync Server 2013: Управление качеством обслуживания (QoS).'
ms.reviewer: ''
f1.keywords:
- NOCSH
TOCTitle: Managing Quality of Service (QoS)
author: lanachin
ms.author: v-lanac
ms.manager: serdars
ms:assetid: ab1051c3-8380-4d72-86df-37a61b1e4a41
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg405409(v=OCS.15)
ms:contentKeyID: 48185049
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: df0e84389cc030cd63fe04c46929bd981a074aec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437282"
---
# <a name="managing-quality-of-service-qos-in-lync-server-2013"></a><span data-ttu-id="284d7-103">Управление качеством обслуживания (QoS) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="284d7-103">Managing Quality of Service (QoS) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="284d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="284d7-104">

<span> </span></span></span>

<span data-ttu-id="284d7-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="284d7-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="284d7-106">Качество обслуживания (QoS) — это сетевая технология, используемая в некоторых организациях для обеспечения оптимального взаимодействия с пользователем для голосовой и видеосвязи.</span><span class="sxs-lookup"><span data-stu-id="284d7-106">Quality of Service (QoS) is a networking technology used in some organizations to help provide an optimal end-user experience for audio and video communications.</span></span> <span data-ttu-id="284d7-107">Чаще всего Служба QoS используется в сетях, в которых пропускная способность ограничена: с большим количеством сетевых пакетов, которые конкурирует за сравнительно небольшой объем доступной пропускной способности, качество обслуживания позволяет администраторам назначать более высокие приоритеты для пакетов, включающих звуковые и видеоданные.</span><span class="sxs-lookup"><span data-stu-id="284d7-107">QoS is most-commonly used on networks where bandwidth is limited: with a large number of network packets competing for a relatively small amount of available bandwidth, Quality of Service provides a way for administrators to assign higher priorities to packets carrying audio or video data.</span></span> <span data-ttu-id="284d7-108">Предоставляя этим пакетам более высокий приоритет, голосовые и видеосообщения обычно загружаются быстрее, и с меньшим перерывом, чем сетевые сеансы, такие как передача файлов, просмотр веб-страниц или резервные копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="284d7-108">By giving these packets a higher priority, audio and video communications are likely to complete faster, and with less interruption, than network sessions involving things like file transfers, web browsing, or database backups.</span></span> <span data-ttu-id="284d7-109">Это связано с тем, что сетевые пакеты, используемые для передачи файлов или резервных копий базы данных, получают приоритет "Лучший объем работы".</span><span class="sxs-lookup"><span data-stu-id="284d7-109">That's because network packets used for file transfers or database backups are assigned a "best effort" priority.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="284d7-110">Как правило, качество обслуживания применимо только к сеансам связи во внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="284d7-110">As a general rule, Quality of Service applies only to communication sessions on your internal network.</span></span> <span data-ttu-id="284d7-111">При реализации QoS вы можете настроить серверы и маршрутизаторы так, чтобы они поддерживали маркировку пакетов. Однако эти устройства можно настроить так, чтобы они поддерживали отметку пакетов определенным образом.</span><span class="sxs-lookup"><span data-stu-id="284d7-111">When you implement QoS, you configure your servers and routers to support packet marking; however, you configure these devices to support packet marking in a particular manner.</span></span> <span data-ttu-id="284d7-112">Вы не можете предположить, что качество обслуживания будет поддерживаться в Интернете или в других сетях.</span><span class="sxs-lookup"><span data-stu-id="284d7-112">You cannot assume that Quality of Service will be supported on the Internet or on other networks.</span></span> <span data-ttu-id="284d7-113">Даже если служба поддерживается в других сетях, не существует гарантии того, что качество обслуживания будет настроено таким же образом, как и служба в сети.</span><span class="sxs-lookup"><span data-stu-id="284d7-113">Even if Quality if Service is supported on other networks, there is no guarantee that QoS will be configured the same way that you configured the service on your network.</span></span>



</div>

<span data-ttu-id="284d7-114">Для Microsoft Lync Server 2013 не требуется качество обслуживания; Если вы сейчас не используете QoS, вам не требуется устанавливать службу перед установкой Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="284d7-114">Microsoft Lync Server 2013 does not require Quality of Service; if you do not currently use QoS there is no requirement that you install the service before installing Lync Server 2013.</span></span> <span data-ttu-id="284d7-115">Если в вашей сети возникла значительная потеря пакетов, рекомендуем решить эту проблему, добавив дополнительную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="284d7-115">If you experience a considerable amount of packet loss on your network the recommended way to alleviate this problem is to add additional bandwidth.</span></span> <span data-ttu-id="284d7-116">Если не удается добавить дополнительную пропускную способность, вам может потребоваться реализовать качество обслуживания.</span><span class="sxs-lookup"><span data-stu-id="284d7-116">If adding more bandwidth is not possible, then you might want to implement Quality of Service instead.</span></span>

<span data-ttu-id="284d7-117">Lync Server 2013 обеспечивает полную поддержку качества обслуживания: это означает, что Организации, уже использующие QoS, могут легко интегрировать сервер Lync Server с существующей сетевой инфраструктурой.</span><span class="sxs-lookup"><span data-stu-id="284d7-117">Lync Server 2013 offers full support for Quality of Service: that means that organizations that are already using QoS can easily integrate Lync Server into their existing network infrastructure.</span></span> <span data-ttu-id="284d7-118">Для этого необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="284d7-118">In order to do this you must perform the following tasks:</span></span>

  - <span data-ttu-id="284d7-119">[Активация QoS в Lync Server 2013 для устройств, которые не основаны на Windows](lync-server-2013-enabling-qos-for-devices-that-are-not-based-on-windows.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-119">[Enabling QoS in Lync Server 2013 for devices that are not based on Windows](lync-server-2013-enabling-qos-for-devices-that-are-not-based-on-windows.md).</span></span> <span data-ttu-id="284d7-120">По умолчанию качество обслуживания отключено для компьютеров и других устройств (например, iPhones), работающих под управлением ОС, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="284d7-120">By default, QoS is disabled for computers and other devices (such as iPhones) that run other operating systems.</span></span> <span data-ttu-id="284d7-121">Несмотря на то что вы можете использовать Lync Server для включения и отключения качества обслуживания для устройств, обычно нельзя использовать продукт для изменения кодов DSCP, используемых этими устройствами.</span><span class="sxs-lookup"><span data-stu-id="284d7-121">Although you can use Lync Server to enable and disable Quality of Service for devices, you typically cannot use the product to modify the DSCP codes used by these devices.</span></span>

  - <span data-ttu-id="284d7-122">[Настройка диапазонов портов в Lync Server 2013 для серверов конференц-связи, приложений и исправлений](lync-server-2013-configuring-port-ranges-for-your-conferencing-application-and-mediation-servers.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-122">[Configuring port ranges in Lync Server 2013 for your Conferencing, Application, and Mediation servers](lync-server-2013-configuring-port-ranges-for-your-conferencing-application-and-mediation-servers.md).</span></span> <span data-ttu-id="284d7-123">Вам необходимо зарезервировать уникальный набор портов для разных типов пакетов, например аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="284d7-123">You must reserve a unique set of ports for different packet types, such as audio and video.</span></span> <span data-ttu-id="284d7-124">В Lync Server 2013 вы не можете включить или отключить качество обслуживания, скажем, задать значение свойства true или false.</span><span class="sxs-lookup"><span data-stu-id="284d7-124">With Lync Server 2013 you do not enable or disable Quality of Service by, say, setting a property value to True or to False.</span></span> <span data-ttu-id="284d7-125">Вместо этого вы включите качество обслуживания, настроив диапазоны портов и создав и применяя групповую политику.</span><span class="sxs-lookup"><span data-stu-id="284d7-125">Instead, you enable Quality of Service by configuring port ranges and then creating and applying Group Policy.</span></span> <span data-ttu-id="284d7-126">Если в дальнейшем вы решите не использовать QoS, вы можете отключить качество обслуживания, удалив соответствующие объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="284d7-126">If you later decide not to use QoS you can “disable” Quality of Service simply by removing the appropriate Group Policy objects.</span></span>

  - <span data-ttu-id="284d7-127">[Настройка диапазонов портов для пограничных серверов в Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-edge-servers.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-127">[Configuring port ranges for your Edge Servers in Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-edge-servers.md).</span></span> <span data-ttu-id="284d7-128">Вы можете использовать на пограничных серверах и остальных серверах одни и те же диапазоны портов, хотя это необязательно.</span><span class="sxs-lookup"><span data-stu-id="284d7-128">Although not required, you can configure your Edge servers to use the same port ranges as your other servers.</span></span>

  - <span data-ttu-id="284d7-129">[Настройка диапазонов портов для клиентов Microsoft Lync в Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-microsoft-lync-clients.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-129">[Configuring port ranges for your Microsoft Lync clients in Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-microsoft-lync-clients.md).</span></span> <span data-ttu-id="284d7-130">Эти диапазоны портов применяются только к клиентским компьютерам и, как правило, не совпадают с диапазонами портов, настроенными на серверах.</span><span class="sxs-lookup"><span data-stu-id="284d7-130">These port ranges apply only to client computers and are typically not the same as the port ranges configured on your servers.</span></span>

  - <span data-ttu-id="284d7-131">[Настройка политики качества обслуживания в Lync Server 2013 для серверов конференц-связи, приложений и исправлений](lync-server-2013-configuring-a-quality-of-service-policy-for-your-conferencing-application-and-mediation-servers.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-131">[Configuring a Quality of Service policy in Lync Server 2013 for your Conferencing, Application, and Mediation servers](lync-server-2013-configuring-a-quality-of-service-policy-for-your-conferencing-application-and-mediation-servers.md).</span></span> <span data-ttu-id="284d7-132">Эти политики определяют коды DSCP, которые применяются к разным типам пакетов.</span><span class="sxs-lookup"><span data-stu-id="284d7-132">These policies determine the DSCP codes that are applied to different packet types.</span></span>

  - <span data-ttu-id="284d7-133">[Настройка политики качества обслуживания для пограничного сервера/V в Lync Server 2013](lync-server-2013-configuring-a-quality-of-service-policy-for-your-a-v-edge-servers.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-133">[Configuring a Quality of Service policy for your A/V Edge Servers in Lync Server 2013](lync-server-2013-configuring-a-quality-of-service-policy-for-your-a-v-edge-servers.md).</span></span> <span data-ttu-id="284d7-134">Это можно сделать только для внутренней стороны пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="284d7-134">This should only be done for the internal side of your Edge servers.</span></span> <span data-ttu-id="284d7-135">Это связано с тем, что качество обслуживания предназначено для использования во внутренней сети, а не в Интернете.</span><span class="sxs-lookup"><span data-stu-id="284d7-135">That's because Quality of Service is designed for use on your internal network and not on the Internet.</span></span>

  - <span data-ttu-id="284d7-136">[Настройка политик качества обслуживания в Lync Server 2013 для клиентов, работающих под управлением Windows 7 или Windows 8](lync-server-2013-configuring-quality-of-service-policies-for-clients-running-on-windows-7-or-windows-8.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-136">[Configuring Quality of Service policies in Lync Server 2013 for clients running on Windows 7 or Windows 8](lync-server-2013-configuring-quality-of-service-policies-for-clients-running-on-windows-7-or-windows-8.md).</span></span> <span data-ttu-id="284d7-137">Обратите внимание, что Microsoft Lync Server 2013 не поддерживает QoS для других операционных систем Windows, таких как Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="284d7-137">Note that Microsoft Lync Server 2013 does not support QoS for other Windows operating systems, such as Windows Vista or Windows XP.</span></span>

  - <span data-ttu-id="284d7-138">[Настройка качества обслуживания на устройствах Microsoft Lync Phone Edition в Lync Server 2013](lync-server-2013-configuring-quality-of-service-on-microsoft-lync-phone-edition-devices.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-138">[Configuring Quality of Service on Microsoft Lync Phone Edition devices in Lync Server 2013](lync-server-2013-configuring-quality-of-service-on-microsoft-lync-phone-edition-devices.md).</span></span> <span data-ttu-id="284d7-139">По умолчанию QoS включена для устройств Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="284d7-139">By default, QoS is enabled for Lync Phone Edition devices.</span></span> <span data-ttu-id="284d7-140">Тем не менее может потребоваться изменить значение DSCP по умолчанию, чтобы гарантировать, что все звуковые пакеты в вашей организации используют один и тот же код DSCP.</span><span class="sxs-lookup"><span data-stu-id="284d7-140">However, you might want to change the default DSCP value in order to ensure that all audio packets in your organization use the same DSCP code.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="284d7-141">Если вы используете Microsoft Windows Server 2012 или Windows Server 2012 R2, вам может потребоваться новый набор командлетов Windows PowerShell, которые можно использовать для управления качеством обслуживания на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="284d7-141">If you are using Microsoft Windows Server 2012 or Windows Server 2012 R2 you might be interested in the new set of Windows PowerShell cmdlets available for managing Quality of Service on that platform.</span></span> <span data-ttu-id="284d7-142">Дополнительные сведения можно найти в разделе командлетов качества обслуживания сети в Windows PowerShell [https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps](https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps) .</span><span class="sxs-lookup"><span data-stu-id="284d7-142">For more information, see Network Quality of Service Cmdlets in Windows PowerShell at [https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps](https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps).</span></span>



<span data-ttu-id="284d7-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="284d7-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

