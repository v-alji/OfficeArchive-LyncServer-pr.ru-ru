---
title: 'Lync Server 2013: Создание политики размещенной голосовой почты на уровне сайта'
description: 'Lync Server 2013: Создание политики размещенной голосовой почты на уровне сайта.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a site-level hosted voice mail policy
ms:assetid: 145892c8-a6ca-45fb-9e83-786f709dd775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398216(v=OCS.15)
ms:contentKeyID: 48183481
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8cd578359a8d20562e8887b61b86d53332e6f8d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432116"
---
# <a name="create-a-site-level-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="bf87c-103">Создание политики размещенной голосовой почты на уровне сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf87c-103">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf87c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf87c-104">

<span> </span></span></span>

<span data-ttu-id="bf87c-105">_**Тема последнего изменения:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="bf87c-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="bf87c-106">Политика *сайта* может влиять на всех пользователей, которые размещены на сайте, для которого определена политика.</span><span class="sxs-lookup"><span data-stu-id="bf87c-106">A *site* policy can impact all users that are homed on the site for which the policy is defined.</span></span> <span data-ttu-id="bf87c-107">Если пользователь настроен на доступ к размещенной единой системе обмена сообщениями в UM и для него не назначена политика на уровне пользователя, применяется политика сайта.</span><span class="sxs-lookup"><span data-stu-id="bf87c-107">If a user is configured for hosted Exchange UM access and has not been assigned a Per-user policy, the site policy applies.</span></span> <span data-ttu-id="bf87c-108">Если вы не развернули политику сайта, она будет применена к глобальной политике.</span><span class="sxs-lookup"><span data-stu-id="bf87c-108">If you have not deployed a site policy, the global policy applies.</span></span>

<span data-ttu-id="bf87c-109">Дополнительные сведения о настройке политик сайтов можно найти в документации по оболочке управления Lync Server для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="bf87c-109">For details about configuring site policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="bf87c-110">New-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="bf87c-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="bf87c-111">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="bf87c-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="bf87c-112">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="bf87c-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-site-hosted-voice-mail-policy"></a><span data-ttu-id="bf87c-113">Создание политики размещенной голосовой почты сайта</span><span class="sxs-lookup"><span data-stu-id="bf87c-113">To create a site hosted voice mail policy</span></span>

1.  <span data-ttu-id="bf87c-114">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="bf87c-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="bf87c-115">Запустите командлет New-CsHostedVoicemailPolicy, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="bf87c-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="bf87c-116">Например, выполните командлет:</span><span class="sxs-lookup"><span data-stu-id="bf87c-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity site:Redmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for the Redmond site." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="bf87c-117">В этом примере создается политика размещенной голосовой почты с областью сайта и устанавливаются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="bf87c-117">This example creates a hosted voice mail policy with site scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="bf87c-118">**Identity** — уникальный идентификатор для политики, включающий область.</span><span class="sxs-lookup"><span data-stu-id="bf87c-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="bf87c-119">Для политики с областью сайта значение параметра удостоверения должно быть задано в формате `site:` *\<name\>* , например `site:Redmond` .</span><span class="sxs-lookup"><span data-stu-id="bf87c-119">For a policy with site scope, the Identity parameter value must be specified in the format `site:`*\<name\>*, for example, `site:Redmond`.</span></span>
    
      - <span data-ttu-id="bf87c-120">**Destination** указывает полное доменное имя (FQDN) размещенной службы единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bf87c-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="bf87c-121">Этот параметр является необязательным, но при попытке включить пользователя для размещенной голосовой почты и назначенной пользователю политики не может быть задано значение "включить".</span><span class="sxs-lookup"><span data-stu-id="bf87c-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="bf87c-122">**Описание** — необязательные описательные сведения о политике.</span><span class="sxs-lookup"><span data-stu-id="bf87c-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="bf87c-123">**Организация** : список клиентов Exchange, разделенных запятыми, которые пользователи Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bf87c-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="bf87c-124">Каждый клиент должен быть указан в качестве полного доменного имени этого клиента в размещенной службе единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bf87c-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

<span data-ttu-id="bf87c-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf87c-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

