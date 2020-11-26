---
title: 'Lync Server 2013: включение для пользователей единого хранилища контактов'
description: 'Lync Server 2013: включение пользователей для единого хранилища контактов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for unified contact store
ms:assetid: 7b46a01f-beb5-4a33-adb0-35f0502b168d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205024(v=OCS.15)
ms:contentKeyID: 48184599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2249249d314e13d840b276e46f1fe38ad271664a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428820"
---
# <a name="enable-users-for-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="52845-103">Включение для пользователей единого хранилища контактов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52845-103">Enable users for unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52845-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52845-104">

<span> </span></span></span>

<span data-ttu-id="52845-105">_**Тема последнего изменения:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="52845-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="52845-106">При развертывании сервера Lync Server 2013 и публикации топологии единое хранилище контактов включается для всех пользователей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52845-106">When you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="52845-107">Вам не нужно предпринимать никаких дополнительных действий, чтобы активировать единое хранилище контактов после развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="52845-107">You do not need to take any additional action to enable unified contact store after you deploy Lync Server 2013.</span></span> <span data-ttu-id="52845-108">Однако вы можете использовать командлет **Set-CsUserServicesPolicy** , чтобы настроить, какие пользователи будут доступны в едином хранилище контактов.</span><span class="sxs-lookup"><span data-stu-id="52845-108">However, you can use the **Set-CsUserServicesPolicy** cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="52845-109">Вы можете включить эту функцию глобально, по сайту, по клиенту или по отдельным пользователям или группам пользователей.</span><span class="sxs-lookup"><span data-stu-id="52845-109">You can enable this feature globally, by site, by tenant, or by individuals or groups of individuals.</span></span>

<div>

## <a name="to-enable-users-for-unified-contact-store"></a><span data-ttu-id="52845-110">Включение пользователей в едином хранилище контактов</span><span class="sxs-lookup"><span data-stu-id="52845-110">To enable users for unified contact store</span></span>

1.  <span data-ttu-id="52845-111">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="52845-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="52845-112">Выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="52845-112">Do any of the following:</span></span>
    
      - <span data-ttu-id="52845-113">Чтобы включить единое хранилище контактов глобально для всех пользователей Lync Server, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="52845-113">To enable unified contact store globally for all Lync Server users, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Identity global -UcsAllowed $True
    
      - <span data-ttu-id="52845-114">Чтобы включить единое хранилище контактов для пользователей на определенном сайте, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="52845-114">To enable unified contact store for the users at a specific site, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity site:<site name> -UcsAllowed $True
        
        <span data-ttu-id="52845-115">Например:</span><span class="sxs-lookup"><span data-stu-id="52845-115">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity site:Redmond -UcsAllowed $True
    
      - <span data-ttu-id="52845-116">Чтобы включить единое хранилище контактов по клиенту, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="52845-116">To enable unified contact store by tenant, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Tenant <tenantId> -UcsAllowed $True
        
        <span data-ttu-id="52845-117">Например:</span><span class="sxs-lookup"><span data-stu-id="52845-117">For example:</span></span>
        
            Set-CsUserServicesPolicy -Tenant "38aad667-af54-4397-aaa7-e94c79ec2308" -UcsAllowed $True
    
      - <span data-ttu-id="52845-118">Чтобы включить единое хранилище контактов для определенных пользователей, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="52845-118">To enable unified contact store for specific users, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "<user display name>" -PolicyName <"policy name">
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="52845-119">Вы также можете использовать псевдонимы пользователя или URI SIP вместо отображаемого имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="52845-119">You can also use user alias or SIP URI instead of the user display name.</span></span>

        
        </div>
        
        <span data-ttu-id="52845-120">Например:</span><span class="sxs-lookup"><span data-stu-id="52845-120">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "Ken Myer" -PolicyName "UCS Enabled Users"
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="52845-121">В предыдущем примере первая команда создает новую политику для пользователей с <EM>включенным управлением UCS</EM> , при этом для флага UcsAllowed задано значение true.</span><span class="sxs-lookup"><span data-stu-id="52845-121">In the preceding example, the first command creates a new per-user policy named <EM>UCS Enabled Users</EM> with the UcsAllowed flag set to True.</span></span> <span data-ttu-id="52845-122">Вторая команда назначает пользователю политику с отображаемым именем Кен Myer, что означает, что Кен Myer теперь включен для единого магазина контактов.</span><span class="sxs-lookup"><span data-stu-id="52845-122">The second command assigns the policy to the user with the display name Ken Myer, which means that Ken Myer is now enabled for unified contact store.</span></span>

        
        <span data-ttu-id="52845-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52845-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

