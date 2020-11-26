---
title: 'Lync Server 2013: необходимые условия для включения проверки подлинности Kerberos'
description: 'Lync Server 2013: предварительные условия для включения проверки подлинности Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for enabling Kerberos authentication
ms:assetid: 3f276a21-7476-4bc0-9fd1-59e844d2e9c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425909(v=OCS.15)
ms:contentKeyID: 48183945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65a45bad0eb249fdbc717fe05f080ce737c87c6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436974"
---
# <a name="prerequisites-for-enabling-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="e54cf-103">Необходимые условия для включения проверки подлинности Kerberos в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e54cf-103">Prerequisites for enabling Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e54cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e54cf-104">

<span> </span></span></span>

<span data-ttu-id="e54cf-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="e54cf-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="e54cf-106">Перед включением проверки подлинности Kerberos убедитесь, что выполнены все необходимые требования к конфигурации и инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="e54cf-106">Before enabling Kerberos authentication, make sure that you complete all prerequisite configuration and infrastructure preparations:</span></span>

  - <span data-ttu-id="e54cf-107">Схема Active Directory расширена для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e54cf-107">Active Directory schema is extended for Lync Server 2013.</span></span>

  - <span data-ttu-id="e54cf-108">Подготовка леса Active Directory для Lync Server 2013 завершена.</span><span class="sxs-lookup"><span data-stu-id="e54cf-108">Active Directory forest preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="e54cf-109">Подготовка домена Active Directory для Lync Server 2013 завершена.</span><span class="sxs-lookup"><span data-stu-id="e54cf-109">Active Directory domain preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="e54cf-110">Хранилище Central Management успешно установлено и доступно.</span><span class="sxs-lookup"><span data-stu-id="e54cf-110">Central Management store is successfully installed and available.</span></span>

  - <span data-ttu-id="e54cf-111">Топология создана и опубликована с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="e54cf-111">The topology has been created and published by using Topology Builder.</span></span>

  - <span data-ttu-id="e54cf-112">Серверы и роли, для которых требуются веб-службы, были определены и развернуты, в том числе серверы переднего плана, серверы Standard Edition и режиссеры.</span><span class="sxs-lookup"><span data-stu-id="e54cf-112">Servers and roles that require Web Services have been defined and deployed, including Front End Servers, Standard Edition servers, and Directors.</span></span>

  - <span data-ttu-id="e54cf-113">Службы IIS настраиваются и развертываются с помощью рекомендованных служб ролей для поддержки веб-служб в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e54cf-113">Internet Information Services (IIS) is configured and deployed with the recommended role services to support Web Services in Lync Server 2013.</span></span>

<span data-ttu-id="e54cf-114">После выполнения необходимых условий вы должны будете создать одну или несколько учетных записей для веб-служб, которые будут использоваться для проверки подлинности Kerberos для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e54cf-114">After the prerequisites have been met, you should be ready to create one or more accounts for Web Services to use for Kerberos authentication for your deployment.</span></span> <span data-ttu-id="e54cf-115">Как минимум, вам нужно создать для каждого развертывания один из учетных записей проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e54cf-115">At a minimum, you need to create one Kerberos authentication account for each deployment.</span></span> <span data-ttu-id="e54cf-116">Однако вы можете создать учетную запись для каждого сайта, чтобы предоставить локальную проверку подлинности Kerberos на сайте.</span><span class="sxs-lookup"><span data-stu-id="e54cf-116">However, you can create an account for each site to provide local Kerberos authentication at the site.</span></span> <span data-ttu-id="e54cf-117">Вы можете указать только одну учетную запись для проверки подлинности Kerberos для сайта.</span><span class="sxs-lookup"><span data-stu-id="e54cf-117">You can only specify one Kerberos authentication account per site.</span></span>

<span data-ttu-id="e54cf-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e54cf-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

