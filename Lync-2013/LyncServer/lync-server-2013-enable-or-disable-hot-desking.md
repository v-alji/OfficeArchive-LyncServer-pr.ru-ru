---
title: 'Lync Server 2013: Включение и отключение поддержки горячей замены'
description: 'Lync Server 2013: Включение и отключение поддержки горячей замены.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable hot desking
ms:assetid: 93a7fed6-f61a-4b41-9336-a8320afa87cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994057(v=OCS.15)
ms:contentKeyID: 51803968
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3fd22c9bf51078324cfe5e215bd154503c2d9b57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398182"
---
# <a name="enable-or-disable-hot-desking-in-lync-server-2013"></a><span data-ttu-id="896e1-103">Включение и отключение функции поддержки горячей замены в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="896e1-103">Enable or disable hot desking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="896e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="896e1-104">

<span> </span></span></span>

<span data-ttu-id="896e1-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="896e1-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="896e1-106">Вы можете настроить стандартные телефоны как *стационарные телефоны*.</span><span class="sxs-lookup"><span data-stu-id="896e1-106">You can set up common area phones as *hot-desk phones*.</span></span> <span data-ttu-id="896e1-107">С помощью стационарных телефонов пользователи могут входить в свою учетную запись пользователя и после входа в нее использовать возможности сервера Lync и собственные параметры профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="896e1-107">With hot-desk phones, users can log on to their own user account, and, after they are logged on, use Lync Server features and their own user profile settings.</span></span> <span data-ttu-id="896e1-108">Управление горячим подключением осуществляется с помощью политик клиента: чтобы включить или отключить функцию горячей замены, необходимо изменить политики клиента, используемые вашими стандартными телефонами.</span><span class="sxs-lookup"><span data-stu-id="896e1-108">Hot desking is managed by using client policies: to enable or disable hot desking, you need to modify the client policies that are used by your common area phones.</span></span> <span data-ttu-id="896e1-109">Подробные сведения о том, как определить политики конференц-связи, назначенные на обычные телефоны, можно найти [в статьях Просмотр сведений о телефонах в Lync Server 2013](lync-server-2013-view-common-area-phone-information.md).</span><span class="sxs-lookup"><span data-stu-id="896e1-109">For details about how to determine the conferencing policies that have been assigned to your common area phones, see [View common area phone information in Lync Server 2013](lync-server-2013-view-common-area-phone-information.md).</span></span>

<span data-ttu-id="896e1-110">Вы можете использовать параметр EnableHotdesking командлета **New-CSClientPolicy** или командлет **Set-CSClientPolicy** , чтобы включить или отключить функцию горячей замены на телефоне, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="896e1-110">You use the EnableHotdesking parameter of the **New-CSClientPolicy** cmdlet or the **Set-CSClientPolicy** cmdlet to enable or disable hot desking on a phone, as follows.</span></span> <span data-ttu-id="896e1-111">Выполните эти командлеты либо из командной консоли Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="896e1-111">Run these cmdlets from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="896e1-112">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="896e1-112">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="enabling-hot-desking"></a><span data-ttu-id="896e1-113">Включение поддержки горячей замены</span><span class="sxs-lookup"><span data-stu-id="896e1-113">Enabling hot desking</span></span>

  - <span data-ttu-id="896e1-114">Чтобы включить функцию горячего подключения для обычного телефонного телефона, необходимо изменить политику клиента, назначенную этому телефону (или набору телефонов).</span><span class="sxs-lookup"><span data-stu-id="896e1-114">To enable hot desking for a common area phone, you must modify the client policy that has been assigned to that phone (or collection of phones).</span></span>
    
    <span data-ttu-id="896e1-115">После того как вы определили политику, которую необходимо изменить, далее следует использовать командлет **Set-CsClientPolicy** , чтобы установить для параметра EnableHotdesking значение true.</span><span class="sxs-lookup"><span data-stu-id="896e1-115">After you have identified the policy that needs to be modified, the next step is to use the **Set-CsClientPolicy** cmdlet to set the EnableHotdesking parameter to True.</span></span> <span data-ttu-id="896e1-116">Например:</span><span class="sxs-lookup"><span data-stu-id="896e1-116">For example:</span></span>
    
        Set-CsClientPolicy -Identity "CommonAreaPhonePolicy" - EnableHotdesking $True

  - <span data-ttu-id="896e1-117">Кроме того, вы можете использовать командлет **New-CsClientPolicy** для создания новой политики клиента, обеспечивающей поддержку горячего рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="896e1-117">Alternatively, you can use the **New-CsClientPolicy** cmdlet to create a new client policy that enables hot desking.</span></span> <span data-ttu-id="896e1-118">Например:</span><span class="sxs-lookup"><span data-stu-id="896e1-118">For example:</span></span>
    
        New-CsClientPolicy -Identity "NewCommonAreaPhonePolicy" - EnableHotdesking $True

</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="896e1-119">После того как эта политика создана, вы должны назначить ее соответствующим телефонам.</span><span class="sxs-lookup"><span data-stu-id="896e1-119">After this policy has been created, you must assign it to the appropriate common area phones.</span></span> <span data-ttu-id="896e1-120">Подробности можно найти <A href="lync-server-2013-assign-policies-to-a-common-area-phone.md">в разделе назначение политик в Lync Server 2013 на общем телефоне с областями</A>.</span><span class="sxs-lookup"><span data-stu-id="896e1-120">For details, see <A href="lync-server-2013-assign-policies-to-a-common-area-phone.md">Assign policies in Lync Server 2013 to a common area phone</A>.</span></span>



</div>

<div>

## <a name="disabling-hot-desking"></a><span data-ttu-id="896e1-121">Отключение поддержки горячей замены</span><span class="sxs-lookup"><span data-stu-id="896e1-121">Disabling hot desking</span></span>

  - <span data-ttu-id="896e1-122">Чтобы отключить функцию горячего подключения для обычного телефонного телефона, сбросьте параметр EnableHotdesking командлета **Set-CsClientPolicy** в значение по умолчанию, равное false.</span><span class="sxs-lookup"><span data-stu-id="896e1-122">To disable hot desking for a common area phone, reset the EnableHotdesking parameter of the **Set-CsClientPolicy** cmdlet to the default value of False.</span></span> <span data-ttu-id="896e1-123">Например:</span><span class="sxs-lookup"><span data-stu-id="896e1-123">For example:</span></span>
    
        Set-CsClientPolicy -Identity "CommonAreaPhonePolicy" - EnableHotdesking $False

</div>

<span data-ttu-id="896e1-124">Подробные сведения можно найти в разделах справки по командлетам [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) и командлету [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) .</span><span class="sxs-lookup"><span data-stu-id="896e1-124">For details, see the Help topics for the [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) cmdlet and the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) cmdlet.</span></span>

<span data-ttu-id="896e1-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="896e1-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

