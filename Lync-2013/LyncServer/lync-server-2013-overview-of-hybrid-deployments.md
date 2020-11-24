---
title: 'Lync Server 2013: обзор гибридных развертываний'
description: 'Lync Server 2013: Общие сведения о гибридных развертываниях.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of hybrid deployments
ms:assetid: f6610f2f-c804-4f36-81fc-7aa3297bb4a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205386(v=OCS.15)
ms:contentKeyID: 48185845
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98fce595614484fdc56fe84d5ad6076c9becc4e8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399544"
---
# <a name="overview-of-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="2b3ab-103">Обзор гибридных развертываний Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b3ab-103">Overview of Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b3ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b3ab-104">

<span> </span></span></span>

<span data-ttu-id="2b3ab-105">_**Тема последнего изменения:** 2016-05-25_</span><span class="sxs-lookup"><span data-stu-id="2b3ab-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="2b3ab-106">Гибридное развертывание Lync Server — это развертывание, при котором пользователи домена (например, contoso.com) разделятся между локальным сервером Lync Server и Microsoft Lync Online.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-106">A Lync Server hybrid deployment is a deployment where users of a domain, such as contoso.com, are split between using Lync Server on-premises and Microsoft Lync Online.</span></span> <span data-ttu-id="2b3ab-107">Некоторые пользователи домена размещены на локальном сервере Lync, а некоторые пользователи находятся в Skype для бизнеса Online.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-107">Some of the domain users are homed on the on-premises Lync Server, and some users are homed in Skype for Business Online.</span></span>

<span data-ttu-id="2b3ab-108">Вы можете настроить локальное развертывание Lync для гибридной работы в Skype для бизнеса Online и использовать синхронизацию Active Directory, чтобы синхронизировать локальные и сетевые пользователи.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-108">You can configure your on-premises Lync deployment for hybrid with Skype for Business Online and use Active Directory Synchronization to keep your on-premises and online users synchronized.</span></span> <span data-ttu-id="2b3ab-109">Вы также можете настроить Гибридные развертывания для интеграции с локальным сервером Exchange и SharePoint либо с приложениями Microsoft 365 и Office 365, включая Exchange Online и SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-109">You can also configure hybrid deployments for integration with on-premises Exchange and SharePoint, or with Microsoft 365 and Office 365 applications, including Exchange Online and SharePoint Online.</span></span>

<span data-ttu-id="2b3ab-110">В этом разделе рассказывается, как развертывать приложения, необходимые для гибридного развертывания Lync Server, а затем настраивать развертывание для управления пользователями между приложением Lync Server в локальной среде и Skype для бизнеса Online.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-110">This section guides you through deploying the applications required for a Lync Server hybrid deployment, and then configuring your deployment to manage users between Lync Server on-premises and Skype for Business Online.</span></span>

<span data-ttu-id="2b3ab-111">Сведения о настройке локального развертывания Lync Server для гибридной работы в Skype для бизнеса Online можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b3ab-111">For information about configuring your on-premises Lync Server deployment for hybrid with Skype for Business Online see the following topics:</span></span>

  - [<span data-ttu-id="2b3ab-112">Планирование гибридных развертываний Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b3ab-112">Planning for Lync Server 2013 hybrid deployments</span></span>](lync-server-2013-planning-for-hybrid-deployments.md)

  - [<span data-ttu-id="2b3ab-113">Настройка гибридных развертываний для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b3ab-113">Configuring Lync Server 2013 hybrid deployments</span></span>](lync-server-2013-configuring-hybrid-deployments.md)

<span data-ttu-id="2b3ab-114">Дополнительные сведения о Skype для бизнеса Online можно найти в [Lync Online](https://go.microsoft.com/fwlink/p/?linkid=282396).</span><span class="sxs-lookup"><span data-stu-id="2b3ab-114">For more information about Skype for Business Online, see [Lync Online](https://go.microsoft.com/fwlink/p/?linkid=282396).</span></span>

<span data-ttu-id="2b3ab-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b3ab-115"></div>

<span> </span>

</div>

</div>

</span></span></div>
