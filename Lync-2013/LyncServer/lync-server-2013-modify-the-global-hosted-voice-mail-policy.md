---
title: 'Lync Server 2013: изменение политики глобальной размещенной голосовой почты'
description: 'Lync Server 2013: измените политику глобальной размещенной голосовой почты.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the global hosted voice mail policy
ms:assetid: f059b3ce-a7d8-4ea9-b10b-0052222ec2ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412994(v=OCS.15)
ms:contentKeyID: 48185757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9cd5e16c78049ce79abd936a79b2025a14e45943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445703"
---
# <a name="modify-the-global-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="6f74d-103">Изменение политики глобальной размещенной голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f74d-103">Modify the global hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f74d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f74d-104">

<span> </span></span></span>

<span data-ttu-id="6f74d-105">_**Тема последнего изменения:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="6f74d-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="6f74d-106">Политика *глобальной* размещенной голосовой почты устанавливается вместе с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6f74d-106">The *global* hosted voice mail policy is installed with Lync Server 2013.</span></span> <span data-ttu-id="6f74d-107">Вы можете изменить его в соответствии с вашими потребностями, но переименовать или удалить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="6f74d-107">You can modify it to meet your needs, but you cannot rename or delete it.</span></span> <span data-ttu-id="6f74d-108">Чтобы изменить глобальную политику, используйте командлет Set-CsHostedVoicemailPolicy, чтобы установить для параметров соответствующие значения для конкретного развертывания.</span><span class="sxs-lookup"><span data-stu-id="6f74d-108">To modify the global policy, you use the Set-CsHostedVoicemailPolicy cmdlet to set the parameters to appropriate values for your specific deployment.</span></span>

<span data-ttu-id="6f74d-109">Дополнительные сведения о командлете [Set-CsHostedVoicemailPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy) можно найти в документации по оболочке Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="6f74d-109">For details about the [Set-CsHostedVoicemailPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>

## <a name="to-modify-the-global-hosted-voice-mail-policy"></a><span data-ttu-id="6f74d-110">Изменение политики глобальной размещенной голосовой почты</span><span class="sxs-lookup"><span data-stu-id="6f74d-110">To modify the global hosted voice mail policy</span></span>

1.  <span data-ttu-id="6f74d-111">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="6f74d-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="6f74d-112">Запустите командлет Set-CsHostedVoicemailPolicy, чтобы настроить параметры глобальной политики для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="6f74d-112">Run the Set-CsHostedVoicemailPolicy cmdlet to set the global policy parameters for your environment.</span></span> <span data-ttu-id="6f74d-113">Например, выполните командлет:</span><span class="sxs-lookup"><span data-stu-id="6f74d-113">For example, run:</span></span>
    
        Set-CsHostedVoicemailPolicy -Destination ExUM.fabrikam.com -Organization "corp1.litwareinc.com"
    
    <span data-ttu-id="6f74d-114">Так как эта команда не задает параметр удостоверения политики, интерфейс командной строки Windows PowerShell задает указанные ниже значения для политики глобальной размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="6f74d-114">Because this command does not specify the policy’s Identity parameter, Windows PowerShell command-line interface sets the following values on the global hosted voice mail policy:</span></span>
    
      - <span data-ttu-id="6f74d-115">**Destination** указывает полное доменное имя (FQDN) размещенной службы единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6f74d-115">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="6f74d-116">Этот параметр является необязательным, но при попытке включить пользователя для размещенной голосовой почты и назначенной пользователю политики не может быть задано значение "включить".</span><span class="sxs-lookup"><span data-stu-id="6f74d-116">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="6f74d-117">В разделе **Организация** указывается список клиентов Exchange, разделенных запятыми, которые пользователи Lync Server имеют дома.</span><span class="sxs-lookup"><span data-stu-id="6f74d-117">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server users.</span></span> <span data-ttu-id="6f74d-118">Каждый клиент должен быть указан в качестве полного доменного имени этого клиента в размещенной службе единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6f74d-118">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6f74d-119">В предыдущем примере значение "corp1.litwareinc.com" заменяет любое значение, которое может быть уже представлено в параметре "Организация".</span><span class="sxs-lookup"><span data-stu-id="6f74d-119">In the previous example cmdlet, the value “corp1.litwareinc.com” replaces any value that might already be present in the Organization parameter.</span></span> <span data-ttu-id="6f74d-120">Например, если в политике уже указан список организаций с разделителями-запятыми, весь список будет заменен.</span><span class="sxs-lookup"><span data-stu-id="6f74d-120">For example, if the policy already contains a comma-separated list of organizations, the full list would be replaced.</span></span> <span data-ttu-id="6f74d-121">Если вы хотите добавить в список организацию вместо замены всего списка, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="6f74d-121">If you want to add an organization to the list rather than replace the entire list, run a command similar to the following.</span></span>

    
    </div>
    
        $a = Get-CsHostedVoicemailPolicy
        $a.Organization += ",corp3.litwareinc.com"
        Set-CsHostedVoicemailPolicy -Organization $a.Organization

<span data-ttu-id="6f74d-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f74d-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

