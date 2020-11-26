---
title: Удаление существующей коллекции параметров конфигурации пограничного сервера/V
description: Удаление существующей коллекции параметров конфигурации пограничного сервера.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of A/V Edge Server configuration settings
ms:assetid: 668d3613-e464-4b68-967a-cfff90b9ce4b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688077(v=OCS.15)
ms:contentKeyID: 49733673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7fe444e8bcb7e7e8e2633e59c23aeb2e80e9b98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430576"
---
# <a name="delete-an-existing-collection-of-av-edge-server-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="9108f-103">Удаление существующей коллекции параметров конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9108f-103">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9108f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9108f-104">

<span> </span></span></span>

<span data-ttu-id="9108f-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9108f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9108f-106">Служба "A/V Edge" обеспечивает способ предоставления внутренних пользователей (пользователей, вошедших в вашу организационную сеть) для совместного использования звуковых и видеофайлов с внешними пользователями (пользователям, которые не вошли в свою организационную сеть).</span><span class="sxs-lookup"><span data-stu-id="9108f-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="9108f-107">Служба EDGE (A/V) главным образом управляется с помощью параметров конфигурации краев/V, параметров, которые можно настроить в области сайта или в области службы (то есть можно настроить для отдельного пограничного сервера A/V).</span><span class="sxs-lookup"><span data-stu-id="9108f-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="9108f-108">При установке сервера Lync Server для вас создается глобальная коллекция параметров конфигурации Edge-V.</span><span class="sxs-lookup"><span data-stu-id="9108f-108">When you install Lync Server, a global collection of A/V Edge configuration settings is created for you.</span></span> <span data-ttu-id="9108f-109">Эту глобальную коллекцию нельзя удалить.</span><span class="sxs-lookup"><span data-stu-id="9108f-109">This global collection cannot be deleted.</span></span> <span data-ttu-id="9108f-110">Однако вы можете использовать командлет Windows PowerShell и Remove-CsAVEdgeConfiguration для "сброса" глобальной коллекции; Это означает, что все значения свойств в глобальной коллекции будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9108f-110">However, you can use the Windows PowerShell and the Remove-CsAVEdgeConfiguration cmdlet to "reset" the global collection; that simply means that all the property values in the global collection will be reset to their default value.</span></span> <span data-ttu-id="9108f-111">Например, если для свойства MaxTokenLifetime задано значение 16 часов, для этого свойства по умолчанию будет назначено 8 часов.</span><span class="sxs-lookup"><span data-stu-id="9108f-111">For example, if you have set the MaxTokenLifetime property for 16 hours, that property will be reset to its default value of 8 hours.</span></span>

<span data-ttu-id="9108f-112">Тем не менее, пользовательские коллекции параметров, созданные на уровне сайта или в области службы, можно удалить с помощью командлета Remove-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9108f-112">However, custom settings collections that you have created at either the site scope or the service scope can be deleted by using the Remove-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="9108f-113">Если вы удалите параметры сайта, то на них будут управлять серверы пограничного сервера/V с помощью глобальных параметров.</span><span class="sxs-lookup"><span data-stu-id="9108f-113">If you delete site settings then A/V Edge servers in that site will be managed by the global settings.</span></span> <span data-ttu-id="9108f-114">Если вы удалили параметры области службы, то этот сервер будет управляться с помощью параметров сайта, если они существуют, или с помощью глобальных параметров, если параметры сайта недоступны.</span><span class="sxs-lookup"><span data-stu-id="9108f-114">If you delete service-scope settings,, that server will then be managed by its site settings, if they exist, or by the global settings if no site settings are available.</span></span>

<span data-ttu-id="9108f-115">Дополнительные сведения можно найти в разделе справки по командлету [Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="9108f-115">For more information, see the help topic for the [Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15)) cmdlet.</span></span>

<div>

## <a name="to-reset-the-global-collection"></a><span data-ttu-id="9108f-116">Сброс глобальной коллекции</span><span class="sxs-lookup"><span data-stu-id="9108f-116">To reset the global collection</span></span>

  - <span data-ttu-id="9108f-117">Следующая команда сбрасывает глобальную коллекцию для параметров конфигурации Edge/V.</span><span class="sxs-lookup"><span data-stu-id="9108f-117">The following command resets the global collection of A/V Edge configuration settings:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "global"

</div>

<div>

## <a name="to-remove-a-collection-from-the-site-scope"></a><span data-ttu-id="9108f-118">Удаление коллекции из области сайта</span><span class="sxs-lookup"><span data-stu-id="9108f-118">To remove a collection from the site scope</span></span>

  - <span data-ttu-id="9108f-119">Эта команда удаляет параметры конфигурации Edge/V, примененные к сайту Redmond.</span><span class="sxs-lookup"><span data-stu-id="9108f-119">This command removes the A/V Edge configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-a-collection-from-the-service-scope"></a><span data-ttu-id="9108f-120">Удаление коллекции из области служб</span><span class="sxs-lookup"><span data-stu-id="9108f-120">To remove a collection from the service scope</span></span>

  - <span data-ttu-id="9108f-121">Эта команда удаляет параметры, примененные к серверу пограничного сервера/V atl-edge-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="9108f-121">This command removes the settings applied to the A/V Edge server atl-edge-001.litwareinc.com:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9108f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9108f-122">See Also</span></span>


[<span data-ttu-id="9108f-123">Возврат сведений о конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9108f-123">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)  
[<span data-ttu-id="9108f-124">Создание и изменение коллекции параметров конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9108f-124">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="9108f-125">Пограничные серверы для аудио-и видеоустройств (A/V) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9108f-125">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
<span data-ttu-id="9108f-126">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9108f-126">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span></span>  
  

<span data-ttu-id="9108f-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9108f-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

