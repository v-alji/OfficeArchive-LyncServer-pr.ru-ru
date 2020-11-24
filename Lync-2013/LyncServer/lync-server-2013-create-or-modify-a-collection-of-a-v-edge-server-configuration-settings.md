---
title: Создание или изменение коллекции параметров конфигурации пограничного сервера
description: Создание или изменение коллекции параметров конфигурации пограничного сервера.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of A/V Edge Server configuration settings
ms:assetid: 43899518-59c6-4be4-8892-d6f6207bfaab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688039(v=OCS.15)
ms:contentKeyID: 49733630
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cdf7dca19446f4eac584564eed776f7fde47bfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399355"
---
# <a name="create-or-modify-a-collection-of-av-edge-server-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="4e44e-103">Создание и изменение коллекции параметров конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e44e-103">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4e44e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4e44e-104">

<span> </span></span></span>

<span data-ttu-id="4e44e-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="4e44e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="4e44e-106">Служба "A/V Edge" обеспечивает способ предоставления внутренних пользователей (пользователей, вошедших в вашу организационную сеть) для совместного использования звуковых и видеофайлов с внешними пользователями (пользователям, которые не вошли в свою организационную сеть).</span><span class="sxs-lookup"><span data-stu-id="4e44e-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="4e44e-107">Служба EDGE (A/V) главным образом управляется с помощью параметров конфигурации краев/V, параметров, которые можно настроить в области сайта или в области службы (то есть можно настроить для отдельного пограничного сервера A/V).</span><span class="sxs-lookup"><span data-stu-id="4e44e-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="4e44e-108">При установке сервера Lync Server для вас создается глобальная коллекция параметров конфигурации Edge-V.</span><span class="sxs-lookup"><span data-stu-id="4e44e-108">When you install Lync Server, a global collection of A/V Edge configuration settings is created for you.</span></span> <span data-ttu-id="4e44e-109">Кроме того, вы можете использовать командлеты Windows PowerShell и New-CsAVEdgeConfiguration для создания новых параметров в области сайта или области службы (то есть для конкретного пограничного сервера A/V).</span><span class="sxs-lookup"><span data-stu-id="4e44e-109">In addition to that, you can use the Windows PowerShell and the New-CsAVEdgeConfiguration cmdlet to create new settings at the site scope or the service scope (that is, for an individual A/V Edge server).</span></span> <span data-ttu-id="4e44e-110">Если вы создаете новые параметры, имейте в виду, что:</span><span class="sxs-lookup"><span data-stu-id="4e44e-110">If you create new settings keep in mind that:</span></span>

  - <span data-ttu-id="4e44e-111">Параметры, настроенные для области службы (то есть на отдельном сервере), имеют приоритет над всеми.</span><span class="sxs-lookup"><span data-stu-id="4e44e-111">Settings configured at the service scope (that is, on an individual server) take priority over everything.</span></span>

  - <span data-ttu-id="4e44e-112">Параметры, настроенные в области сайта, имеют приоритет над параметрами, настроенными в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="4e44e-112">Settings configured at the site scope take priority over settings configured at the global scope.</span></span> <span data-ttu-id="4e44e-113">Однако параметры области служб также будут заменять параметры области сайта.</span><span class="sxs-lookup"><span data-stu-id="4e44e-113">However, service scope settings will also supersede site-scope settings.</span></span>

  - <span data-ttu-id="4e44e-114">Параметры в глобальной области будут использоваться только в том случае, если на отдельном сервере не настроены параметры службы и для сайта, на котором находится этот сервер, отсутствуют параметры сайта.</span><span class="sxs-lookup"><span data-stu-id="4e44e-114">Settings at the global scope will be used only if there are no service settings configured on the individual server and if there are no site settings for the site where that server is located.</span></span>

<span data-ttu-id="4e44e-115">После этого любой из параметров можно будет изменить с помощью командлета Set-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4e44e-115">Any of your settings can then be modified by using the Set-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="4e44e-116">Дополнительные сведения можно найти в разделах справки, посвященных командлетам [New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15)) и [Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="4e44e-116">For more information, see the help topics for the [New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15)) and the [Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15)) cmdlets.</span></span>

<div>

## <a name="to-create-new-av-edge-configuration-settings-at-the-site-scope"></a><span data-ttu-id="4e44e-117">Создание новых параметров конфигурации EDGE на странице "область сайта"</span><span class="sxs-lookup"><span data-stu-id="4e44e-117">To create new A/V Edge configuration settings at the site scope</span></span>

  - <span data-ttu-id="4e44e-118">Следующая команда создает новую коллекцию параметров конфигурации Edge для сайта Redmond.</span><span class="sxs-lookup"><span data-stu-id="4e44e-118">The following command creates a new collection of A/V Edge configuration settings for the Redmond site:</span></span>
    
        New-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-custom-av-edge-configuration-settings-at-the-site-scope"></a><span data-ttu-id="4e44e-119">Создание настраиваемых параметров конфигурации краев/V в области сайта</span><span class="sxs-lookup"><span data-stu-id="4e44e-119">To create custom A/V Edge configuration settings at the site scope</span></span>

  - <span data-ttu-id="4e44e-120">Так как дополнительные параметры не были включены, эти новые параметры будут использовать значения по умолчанию для службы EDGE (A/V).</span><span class="sxs-lookup"><span data-stu-id="4e44e-120">Because no additional parameters were included, these new settings will use the default values for the A/V Edge service.</span></span> <span data-ttu-id="4e44e-121">Кроме того, вы можете добавить дополнительные параметры и значения параметров для создания настраиваемой коллекции.</span><span class="sxs-lookup"><span data-stu-id="4e44e-121">Alternatively, you can add additional parameters and parameter values to create a custom collection.</span></span> <span data-ttu-id="4e44e-122">Например, эта команда задает для свойства MaxTokenLifetime значение 4 часа (04 часа: 00 мин: 00 с):</span><span class="sxs-lookup"><span data-stu-id="4e44e-122">For example, this command sets the MaxTokenLifetime property to 4 hours (04 hours : 00 minutes : 00 seconds):</span></span>
    
        New-CsAVEdgeConfiguration -Identity "site:Redmond" -MaxTokenLifetime "04:00:00"

</div>

<div>

## <a name="to-create-custom-av-edge-configuration-settings-at-the-service-scope"></a><span data-ttu-id="4e44e-123">Создание настраиваемых параметров конфигурации краев/V на уровне службы</span><span class="sxs-lookup"><span data-stu-id="4e44e-123">To create custom A/V Edge configuration settings at the service scope</span></span>

  - <span data-ttu-id="4e44e-124">Эта команда создает сходную коллекцию, примененную к пограничного сервера atl-edge-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="4e44e-124">This command creates a similar collection applied to the A/V Edge server atl-edge-001.litwareinc.com:</span></span>
    
        New-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com" -MaxTokenLifetime "04:00:00"

</div>

<div>

## <a name="to-modify-existing-av-edge-configuration-settings"></a><span data-ttu-id="4e44e-125">Изменение существующих параметров конфигурации краев/V</span><span class="sxs-lookup"><span data-stu-id="4e44e-125">To modify existing A/V Edge configuration settings</span></span>

  - <span data-ttu-id="4e44e-126">В этом примере командлет Set-CsAVEdgeConfiguration используется для изменения максимального срока действия маркера для сайта Redmond на 12 часов.</span><span class="sxs-lookup"><span data-stu-id="4e44e-126">In this example, the Set-CsAVEdgeConfiguration cmdlet is used to change the maximum token lifetime for the Redmond site to 12 hours:</span></span>
    
        Set-CsAVEdgeConfiguration -Identity "site:Redmond" -MaxTokenLifetime "12:00:00"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4e44e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4e44e-127">See Also</span></span>


[<span data-ttu-id="4e44e-128">Возврат сведений о конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e44e-128">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)  
[<span data-ttu-id="4e44e-129">Удаление существующей коллекции параметров конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e44e-129">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="4e44e-130">Пограничные серверы для аудио-и видеоустройств (A/V) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e44e-130">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
<span data-ttu-id="4e44e-131">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="4e44e-131">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span></span>  
<span data-ttu-id="4e44e-132">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="4e44e-132">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span></span>  
  

<span data-ttu-id="4e44e-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4e44e-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

