---
title: Настройка политик для архивации при использовании интеграции с Exchange Server
description: Настройка политик для архивации при использовании интеграции с Exchange Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up policies for Archiving when using Exchange Server integration
ms:assetid: 8b9b2bad-a4b3-42e1-85a7-04022e9442ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205063(v=OCS.15)
ms:contentKeyID: 48184742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8281d27101c049b1029a2005ed062a934438afc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444723"
---
# <a name="setting-up-policies-for-archiving-in-lync-server-2013-when-using-exchange-server-integration"></a><span data-ttu-id="9c9b4-103">Настройка политик для архивации в Lync Server 2013 при использовании интеграции с Exchange Server</span><span class="sxs-lookup"><span data-stu-id="9c9b4-103">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c9b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c9b4-104">

<span> </span></span></span>

<span data-ttu-id="9c9b4-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="9c9b4-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="9c9b4-106">Если для пользователей, исходящих в Exchange 2013, почтовые ящики помещаются на In-Place удержание, политики In-Place удержания управляют архивированием для этих пользователей.</span><span class="sxs-lookup"><span data-stu-id="9c9b4-106">If users homed on Exchange 2013 have their mailboxes put on In-Place Hold, Exchange In-Place Hold policies control archiving for those users.</span></span> <span data-ttu-id="9c9b4-107">Если вы используете Microsoft Exchange Integration для развертывания, политики Exchange 2013 переопределяют политики архивации Lync Server для пользователей, использующих Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="9c9b4-107">If you use Microsoft Exchange integration for your deployment, Exchange 2013 policies override Lync Server Archiving policies for users who are homed on Exchange 2013.</span></span> <span data-ttu-id="9c9b4-108">Сведения о настройке политик архивации Exchange можно найти в документации по Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="9c9b4-108">For information about configuring Exchange Archiving policies, see the Exchange 2013 documentation.</span></span> <span data-ttu-id="9c9b4-109">Подробные сведения о настройке политик пользователей для пользователей, размещенных на Lync Server 2013, приведены в разделе [Настройка политик пользователей для архивации в Lync server 2013](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="9c9b4-109">For details about setting up user policies for users homed on Lync Server 2013, see [Setting up user policies for Archiving in Lync Server 2013](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md) in the Deployment documentation.</span></span> <span data-ttu-id="9c9b4-110">Сведения о том, как работают политики, приведены в разделе [как работает архивация в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="9c9b4-110">For details about how policies work, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="9c9b4-111">Если вы разворачиваете Exchange 2013 и Lync Server 2013 в том же лесе, политики хранения для Exchange 2013 In-Place управления хранением.</span><span class="sxs-lookup"><span data-stu-id="9c9b4-111">If you deploy Exchange 2013 and Lync Server 2013 in the same forest, your Exchange 2013 In-Place Hold policies control archiving.</span></span> <span data-ttu-id="9c9b4-112">Если вы разворачиваете Exchange 2013 и Lync Server 2013 в разных лесах, ознакомьтесь с разворачиванием в разделе "развертывание Lync Server и Microsoft Exchange в разных лесах" в <A href="lync-server-2013-deployment-checklist-for-archiving.md">контрольном списке развертывания для архивации в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9c9b4-112">If you deploy Exchange 2013 and Lync Server 2013 in separate forests, see “Deploying Lync Server and Microsoft Exchange in Different Forests” in <A href="lync-server-2013-deployment-checklist-for-archiving.md">Deployment checklist for Archiving in Lync Server 2013</A>.</span></span>



<span data-ttu-id="9c9b4-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c9b4-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

