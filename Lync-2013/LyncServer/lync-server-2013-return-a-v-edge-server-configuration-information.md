---
title: 'Lync Server 2013: возврат сведений о конфигурации пограничного сервера/V'
description: 'Lync Server 2013: возвращают сведения о конфигурации пограничного сервера/V.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Return A/V Edge Server configuration information
ms:assetid: b041f5a4-2387-4075-846c-ec4f99640903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721850(v=OCS.15)
ms:contentKeyID: 49733783
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4f72fccfe51b946dc0dc285aee12a07e59c844b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442476"
---
# <a name="return-av-edge-server-configuration-information-in-lync-server-2013"></a><span data-ttu-id="33eff-103">Возврат сведений о конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33eff-103">Return A/V Edge Server configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33eff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33eff-104">

<span> </span></span></span>

<span data-ttu-id="33eff-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="33eff-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="33eff-106">Служба "A/V Edge" обеспечивает способ предоставления внутренних пользователей (пользователей, вошедших в вашу организационную сеть) для совместного использования звуковых и видеофайлов с внешними пользователями (пользователям, которые не вошли в свою организационную сеть).</span><span class="sxs-lookup"><span data-stu-id="33eff-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="33eff-107">Служба EDGE (A/V) главным образом управляется с помощью параметров конфигурации краев/V, параметров, которые можно настроить в области сайта или в области службы (то есть можно настроить для отдельного пограничного сервера A/V).</span><span class="sxs-lookup"><span data-stu-id="33eff-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="33eff-108">Чтобы получить сведения о параметрах конфигурации краев, используемых в вашей организации, необходимо использовать Windows PowerShell и командлет Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="33eff-108">To return information about the A/V Edge configuration settings in use in your organization, you must use Windows PowerShell and the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="33eff-109">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="33eff-109">For more information, see the help topic for the [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) cmdlet.</span></span>

<span data-ttu-id="33eff-110">Информация, возвращаемая командлетом Get-CsAVEdgeConfiguration, будет выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="33eff-110">Information returned from the Get-CsAVEdgeConfiguration cmdlet will look similar to this:</span></span>

    Identity              : Global
    MaxTokenLifetime      : 08:00:00
    MaxBandwidthPerUserKb : 10000
    MaxBandwidthPerPortKb : 3000

<div>

## <a name="to-return-information-for-all-your-av-edge-configuration-settings"></a><span data-ttu-id="33eff-111">Получение сведений о всех параметрах конфигурации Edge</span><span class="sxs-lookup"><span data-stu-id="33eff-111">To return information for all your A/V Edge configuration settings</span></span>

  - <span data-ttu-id="33eff-112">Следующая команда возвращает сведения обо всех параметрах, которые используются в вашей организации в качестве параметров конфигурации Edge для/V.</span><span class="sxs-lookup"><span data-stu-id="33eff-112">The following command returns information about all the A/V Edge configuration settings currently in use in your organization:</span></span>
    
        Get-CsAVEdgeConfiguration

</div>

<div>

## <a name="to-return-information-for-site-scoped-av-edge-configuration-settings"></a><span data-ttu-id="33eff-113">Возврат сведений о параметрах конфигурации сайта в качестве границы области</span><span class="sxs-lookup"><span data-stu-id="33eff-113">To return information for site-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="33eff-114">Чтобы получить сведения о конкретной коллекции параметров конфигурации краев/V, укажите удостоверение этой коллекции при запуске командлета Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="33eff-114">To return information about a specific collection of A/V Edge configuration settings, specify the Identity of that collection when running the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="33eff-115">Например, эта команда возвращает сведения только о параметрах, примененных к сайту Redmond.</span><span class="sxs-lookup"><span data-stu-id="33eff-115">For example, this command returns information only for the settings applied to the Redmond site:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-return-information-for-service-scoped-av-edge-configuration-settings"></a><span data-ttu-id="33eff-116">Возврат сведений о параметрах конфигурации краев, заданных в пределах службы</span><span class="sxs-lookup"><span data-stu-id="33eff-116">To return information for service-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="33eff-117">Эта команда возвращает данные только для параметров, примененных к конкретному пограничному серверу/V.</span><span class="sxs-lookup"><span data-stu-id="33eff-117">And this command returns information only for settings applied the a specific A/V Edge server:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="33eff-118">См. также</span><span class="sxs-lookup"><span data-stu-id="33eff-118">See Also</span></span>


[<span data-ttu-id="33eff-119">Создание и изменение коллекции параметров конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33eff-119">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  
[<span data-ttu-id="33eff-120">Удаление существующей коллекции параметров конфигурации пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33eff-120">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="33eff-121">Пограничные серверы для аудио-и видеоустройств (A/V) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33eff-121">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
  

<span data-ttu-id="33eff-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33eff-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

