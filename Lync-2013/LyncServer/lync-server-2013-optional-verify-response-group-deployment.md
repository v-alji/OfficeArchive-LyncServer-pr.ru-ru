---
title: 'Lync Server 2013: (необязательно) Проверка развертывания группы ответа'
description: 'Lync Server 2013: (необязательно) Проверьте развертывание группы ответа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Response Group deployment
ms:assetid: 202ca4ab-8e6d-44a4-b7c8-071133074feb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687989(v=OCS.15)
ms:contentKeyID: 49733579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cfe15026bc1fcfbe10b593987d2717fc0dc8104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424851"
---
# <a name="optional-verify-response-group-deployment-in-lync-server-2013"></a><span data-ttu-id="f33cf-103">Необязательно Проверка развертывания группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f33cf-103">(Optional) Verify Response Group deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f33cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f33cf-104">

<span> </span></span></span>

<span data-ttu-id="f33cf-105">_**Тема последнего изменения:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="f33cf-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="f33cf-106">После настройки группы ответа необходимо проверить конфигурацию, чтобы убедиться, что группы ответа работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="f33cf-106">After you configure Response Group, you need to verify the configuration to make sure your response groups work as expected.</span></span> <span data-ttu-id="f33cf-107">Необходимо проверить работу, как минимум, следующих сценариев, используя следующие типы пользователей:</span><span class="sxs-lookup"><span data-stu-id="f33cf-107">At minimum, verify the following scenarios by using the following types of users:</span></span>

<span data-ttu-id="f33cf-108">**Пользователи**</span><span class="sxs-lookup"><span data-stu-id="f33cf-108">**Users**</span></span>

  - <span data-ttu-id="f33cf-109">Пользователь, который размещен на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f33cf-109">A user who is homed on Lync Server 2013</span></span>

  - <span data-ttu-id="f33cf-110">Внешний пользователь, использующий телефонную сеть общего пользования (ТСОП)</span><span class="sxs-lookup"><span data-stu-id="f33cf-110">An external user who uses the public switched telephone network (PSTN)</span></span>

  - <span data-ttu-id="f33cf-111">Агент, размещенный на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f33cf-111">An agent who is homed on Lync Server 2013</span></span>

<span data-ttu-id="f33cf-112">**Сценарии**</span><span class="sxs-lookup"><span data-stu-id="f33cf-112">**Scenarios**</span></span>

  - <span data-ttu-id="f33cf-113">Пользователь Lync Server 2013 вызывает группу ответа.</span><span class="sxs-lookup"><span data-stu-id="f33cf-113">The Lync Server 2013 user calls the response group.</span></span>

  - <span data-ttu-id="f33cf-114">Внешний пользователь вызывает группу ответа.</span><span class="sxs-lookup"><span data-stu-id="f33cf-114">The external user calls the response group.</span></span>

  - <span data-ttu-id="f33cf-115">Пользователь вызывает группу ответа в то время, как агент обрабатывает другой вызов и переходит в очередь.</span><span class="sxs-lookup"><span data-stu-id="f33cf-115">A user calls the response group while the agent is on another call and goes to the queue.</span></span>

<span data-ttu-id="f33cf-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f33cf-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

