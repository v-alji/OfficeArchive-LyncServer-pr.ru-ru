---
title: 'Lync Server 2013: Создание политики для размещенной голосовой почты для отдельных пользователей'
description: 'Lync Server 2013: Создание политики размещенной голосовой почты для отдельных пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a per-user hosted voice mail policy
ms:assetid: 39018a7c-e0c3-46a2-be4e-05604ec67a50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425867(v=OCS.15)
ms:contentKeyID: 48183902
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de528ceb9bc01114948c276c27f99039658aee38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432130"
---
# <a name="create-a-per-user-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="a67ac-103">Создание политики размещенной голосовой почты для каждого пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a67ac-103">Create a per-user hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a67ac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a67ac-104">

<span> </span></span></span>

<span data-ttu-id="a67ac-105">_**Тема последнего изменения:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="a67ac-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="a67ac-106">Политика *для пользователей* может влиять только на отдельных пользователей, группы и объекты контактов.</span><span class="sxs-lookup"><span data-stu-id="a67ac-106">A *per-user* policy can only impact individual users, groups, and contact objects.</span></span> <span data-ttu-id="a67ac-107">Чтобы развернуть политику для пользователя, необходимо явно назначить ее одному или нескольким пользователям, группам или контактным объектам.</span><span class="sxs-lookup"><span data-stu-id="a67ac-107">To deploy a per-user policy, you must explicitly assign the policy to one or more users, groups, or contact objects.</span></span> <span data-ttu-id="a67ac-108">Подробности можно найти [в разделе Назначение политики размещенной голосовой почты для отдельных пользователей в Lync Server 2013](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md).</span><span class="sxs-lookup"><span data-stu-id="a67ac-108">For details, see [Assign a per-user hosted voice mail policy in Lync Server 2013](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md).</span></span>

<span data-ttu-id="a67ac-109">Дополнительные сведения о работе с политиками голосовой почты для отдельных пользователей можно найти в документации по оболочки управления Lync Server для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a67ac-109">For details about working with per-user hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="a67ac-110">New-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="a67ac-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="a67ac-111">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="a67ac-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="a67ac-112">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="a67ac-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-per-user-hosted-voice-mail-policy"></a><span data-ttu-id="a67ac-113">Создание политики размещенной голосовой почты для пользователя</span><span class="sxs-lookup"><span data-stu-id="a67ac-113">To create a per-user hosted voice mail policy</span></span>

1.  <span data-ttu-id="a67ac-114">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="a67ac-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a67ac-115">Запустите командлет New-CsHostedVoicemailPolicy, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="a67ac-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="a67ac-116">Например, выполните командлет:</span><span class="sxs-lookup"><span data-stu-id="a67ac-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity ExRedmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for Redmond users." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="a67ac-117">В предыдущем примере создается политика размещенной голосовой почты с областью "на пользователя" и устанавливаются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a67ac-117">The previous example creates a hosted voice mail policy with per-user scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="a67ac-118">**Identity** — уникальный идентификатор для политики, включающий область.</span><span class="sxs-lookup"><span data-stu-id="a67ac-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="a67ac-119">Для политики с областью "на пользователя" Этот параметр указывает на простое строковое значение, например ExRedmond.</span><span class="sxs-lookup"><span data-stu-id="a67ac-119">For a policy with per-user scope, this parameter value is specified as a simple string, for example, ExRedmond.</span></span>
    
      - <span data-ttu-id="a67ac-120">**Destination** указывает полное доменное имя (FQDN) размещенной службы единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a67ac-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="a67ac-121">Этот параметр является необязательным, но при попытке включить пользователя для размещенной голосовой почты и назначенной пользователю политики не может быть задано значение "включить".</span><span class="sxs-lookup"><span data-stu-id="a67ac-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="a67ac-122">**Описание** — необязательные описательные сведения о политике.</span><span class="sxs-lookup"><span data-stu-id="a67ac-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="a67ac-123">**Организация** : список клиентов Exchange, разделенных запятыми, которые пользователи Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a67ac-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="a67ac-124">Каждый клиент должен быть указан в качестве полного доменного имени этого клиента в размещенной службе единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a67ac-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a67ac-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a67ac-125">See Also</span></span>


[<span data-ttu-id="a67ac-126">Назначение политики размещенной голосовой почты для отдельных пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a67ac-126">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)  
  

<span data-ttu-id="a67ac-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a67ac-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

