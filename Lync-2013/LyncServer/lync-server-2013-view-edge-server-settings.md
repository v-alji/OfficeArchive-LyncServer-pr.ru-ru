---
title: 'Lync Server 2013: Просмотр параметров пограничного сервера'
description: 'Lync Server 2013: Просмотр параметров пограничного сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Edge Server settings
ms:assetid: 684154cc-cffc-4d2e-8baa-be52c625e5d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747890(v=OCS.15)
ms:contentKeyID: 63969612
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4318b8c97f53f267bb79953af504977f6437214d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446287"
---
# <a name="view-edge-server-settings-in-lync-server-2013"></a><span data-ttu-id="e8103-103">Просмотр параметров пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8103-103">View Edge Server settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8103-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8103-104">

<span> </span></span></span>

<span data-ttu-id="e8103-105">_**Тема последнего изменения:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="e8103-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="e8103-106">Общие конфигурации пограничного сервера следует проверять на основе данных в базе данных управления конфигурацией, чтобы гарантировать, что все изменения будут документированы в соответствии с определенными процедурами управления изменениями.</span><span class="sxs-lookup"><span data-stu-id="e8103-106">General Edge Server configurations should be reviewed against the data in the configuration management database—to help guarantee that all changes were documented as per the defined change control procedures.</span></span>

<span data-ttu-id="e8103-107">Дополнительные проверки могут включать в себя те, которые описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="e8103-107">Additional checks could include those that are described in the following sections:</span></span>

<div>

## <a name="verify-the-allow-and-block-lists"></a><span data-ttu-id="e8103-108">Проверка списка разрешенных и заблокированных списков</span><span class="sxs-lookup"><span data-stu-id="e8103-108">Verify the Allow and block lists</span></span>

<span data-ttu-id="e8103-109">Убедитесь, что указанные пространства имен по-прежнему являются допустимыми списками URI SIP "Allow" и "Block" для федеративных доменов.</span><span class="sxs-lookup"><span data-stu-id="e8103-109">Verify the SIP URI "Allow" and "Block" lists for Federated domains—to determine whether listed namespaces are still valid.</span></span>

<span data-ttu-id="e8103-110">Вы можете использовать Windows PowerShell для просмотра списка разрешенных и заблокированных списков.</span><span class="sxs-lookup"><span data-stu-id="e8103-110">You can use Windows PowerShell to view the allowed and blocked lists.</span></span> <span data-ttu-id="e8103-111">Чтобы просмотреть домены в списке разрешенные домены, выполните следующую команду Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e8103-111">To review the domains on the Allowed Domains list, run the following Windows PowerShell command:</span></span>

`Get-CsAllowedDomain`

<span data-ttu-id="e8103-112">Эта команда возвращает сведения о доменах в списке разрешенные домены, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e8103-112">That command returns information similar to this for the domains on the Allowed Domains list:</span></span>

<span data-ttu-id="e8103-113">Identity: contoso.com</span><span class="sxs-lookup"><span data-stu-id="e8103-113">Identity : contoso.com</span></span>

<span data-ttu-id="e8103-114">Domain (домен): contoso.com</span><span class="sxs-lookup"><span data-stu-id="e8103-114">Domain : contoso.com</span></span>

<span data-ttu-id="e8103-115">ProxyFqdn :</span><span class="sxs-lookup"><span data-stu-id="e8103-115">ProxyFqdn :</span></span>

<span data-ttu-id="e8103-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8103-116">Comment :</span></span>

<span data-ttu-id="e8103-117">MarkForMonitoring: false</span><span class="sxs-lookup"><span data-stu-id="e8103-117">MarkForMonitoring : False</span></span>

<span data-ttu-id="e8103-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8103-118">Comment :</span></span>

<span data-ttu-id="e8103-119">Чтобы просмотреть домены в списке блокируемых доменов, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e8103-119">To review the domains on the blocked domains list, use this command:</span></span>

`Get-CsBlockedDomain`

<span data-ttu-id="e8103-120">В свою очередь, вы получите такие сведения, как, например, для всех блокируемых доменов.</span><span class="sxs-lookup"><span data-stu-id="e8103-120">In turn, you'll receive information such as this for each blocked domain:</span></span>

<span data-ttu-id="e8103-121">Identity: tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="e8103-121">Identity : tailspintoys.com</span></span>

<span data-ttu-id="e8103-122">Domain (домен): tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="e8103-122">Domain : tailspintoys.com</span></span>

<span data-ttu-id="e8103-123">Кроме того, Windows PowerShell позволяет убедиться, что вы можете подключиться к доменам в списке разрешенные домены.</span><span class="sxs-lookup"><span data-stu-id="e8103-123">Windows PowerShell also enables you to verify that you can connection to the domains on your Allowed Domains list.</span></span> <span data-ttu-id="e8103-124">Например, эта команда проверяет соединение между пограничным сервером (TargetFqdn) и федеративным доменом contoso.com:</span><span class="sxs-lookup"><span data-stu-id="e8103-124">For example, this command verifies the connection between your Edge Server (the TargetFqdn) and the federated domain contoso.com:</span></span>

`Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"`

<span data-ttu-id="e8103-125">Эта команда проверяет подключение между пограничным сервером и всеми доменами, которые находятся в списке разрешенных доменов:</span><span class="sxs-lookup"><span data-stu-id="e8103-125">And this command verifies the connection between your Edge Server and all of the domains found on your Allowed Domains list:</span></span>

`Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Domain}`

</div>

<div>

## <a name="verify-multiple-edge-servers-are-identical"></a><span data-ttu-id="e8103-126">Проверка того, что несколько пограничных серверов идентичны</span><span class="sxs-lookup"><span data-stu-id="e8103-126">Verify multiple Edge Servers are identical</span></span>

<span data-ttu-id="e8103-127">Если в массиве с балансировкой нагрузки развернут несколько пограничных серверов, мы рекомендуем проверить, настроены ли все пограничные серверы в массиве одинаковым образом.</span><span class="sxs-lookup"><span data-stu-id="e8103-127">If multiple Edge Servers are deployed in a load balanced array, we recommend verifying that all Edge Servers in the array are configured in the same manner.</span></span>

<span data-ttu-id="e8103-128">Параметры для пограничных серверов можно просмотреть в области сведений в расширении Lync Server 2013 для оснастки управления компьютером.</span><span class="sxs-lookup"><span data-stu-id="e8103-128">You can view settings for Edge Servers in the details pane of the Lync Server 2013 extension for the Computer Management snap-in.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e8103-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e8103-129">See Also</span></span>


[<span data-ttu-id="e8103-130">Get-CsAllowedDomain</span><span class="sxs-lookup"><span data-stu-id="e8103-130">Get-CsAllowedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAllowedDomain)  
[<span data-ttu-id="e8103-131">Get-CsBlockedDomain</span><span class="sxs-lookup"><span data-stu-id="e8103-131">Get-CsBlockedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsBlockedDomain)  
[<span data-ttu-id="e8103-132">Test-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="e8103-132">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
  

<span data-ttu-id="e8103-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8103-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

