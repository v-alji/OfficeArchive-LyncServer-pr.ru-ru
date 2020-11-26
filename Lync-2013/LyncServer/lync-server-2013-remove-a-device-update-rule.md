---
title: 'Lync Server 2013: Удаление правила обновления устройства'
description: 'Lync Server 2013: Удаление правила обновления устройства.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove a Device Update rule
ms:assetid: ad6e0c6a-cda4-4147-92d5-48bc393ac456
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994066(v=OCS.15)
ms:contentKeyID: 51803977
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f0ed7436331377200a5b8719cf32a8195179402
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436498"
---
# <a name="remove-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="e580d-103">Удаление правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e580d-103">Remove a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e580d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e580d-104">

<span> </span></span></span>

<span data-ttu-id="e580d-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e580d-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e580d-106">При удалении правила обновления устройства все равно удаляются из очереди обновления устройства.</span><span class="sxs-lookup"><span data-stu-id="e580d-106">Removing a device update rule takes it permanently out of the device update queue.</span></span>

<span data-ttu-id="e580d-107">Удаление правила отличается от удаления обновления с устройств в вашем развертывании или с тестовых устройств.</span><span class="sxs-lookup"><span data-stu-id="e580d-107">Removing a rule is different from uninstalling an update from the devices in your deployment or from your test devices.</span></span> <span data-ttu-id="e580d-108">Чтобы удалить одобренное обновление из развертывания, *восстановите* правило обновления устройства.</span><span class="sxs-lookup"><span data-stu-id="e580d-108">To uninstall an approved update from your deployment, you *restore* the device update rule.</span></span> <span data-ttu-id="e580d-109">Подробности можно найти [в разделе Восстановление правила обновления устройства в Lync Server 2013](lync-server-2013-restore-a-device-update-rule.md).</span><span class="sxs-lookup"><span data-stu-id="e580d-109">For details, see [Restore a Device Update rule in Lync Server 2013](lync-server-2013-restore-a-device-update-rule.md).</span></span> <span data-ttu-id="e580d-110">Для удаления обновления, которое вы еще не утвердили на тестовых устройствах, вы можете *сбросить* его.</span><span class="sxs-lookup"><span data-stu-id="e580d-110">To uninstall an update you haven’t approved from your test devices, you *reset* it.</span></span> <span data-ttu-id="e580d-111">Подробности можно найти [в разделе Сброс правила обновления устройства в Lync Server 2013](lync-server-2013-reset-a-device-update-rule.md).</span><span class="sxs-lookup"><span data-stu-id="e580d-111">For details, see [Reset a Device Update rule in Lync Server 2013](lync-server-2013-reset-a-device-update-rule.md).</span></span>

<span data-ttu-id="e580d-112">Вы можете удалить правило обновления устройства с помощью панели управления Lync Server или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e580d-112">You can remove a device update rule by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>

## <a name="to-remove-device-update-rules-by-using-lync-server-control-panel"></a><span data-ttu-id="e580d-113">Удаление правил обновления устройства с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="e580d-113">To remove device update rules by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="e580d-114">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="e580d-114">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e580d-115">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e580d-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e580d-116">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e580d-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e580d-117">На панели навигации слева выберите пункт **Клиенты** и нажмите кнопку Навигация по **обновлению устройства** .</span><span class="sxs-lookup"><span data-stu-id="e580d-117">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span>

4.  <span data-ttu-id="e580d-118">На странице **обновление устройства** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="e580d-118">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="e580d-119">Чтобы удалить одно правило, выберите правило, которое вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="e580d-119">To remove one rule, select the rule you want to delete.</span></span>
    
      - <span data-ttu-id="e580d-120">Чтобы удалить все правила, откройте меню **Правка** и выберите команду **выделить все**.</span><span class="sxs-lookup"><span data-stu-id="e580d-120">To remove all rules, click the **Edit** menu, and then click **Select All**.</span></span>

5.  <span data-ttu-id="e580d-121">Нажмите **Изменить**, затем кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e580d-121">Click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-device-update-rules-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e580d-122">Удаление правил обновления устройства с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e580d-122">Removing Device Update Rules by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e580d-123">Кроме того, вы можете удалить правила обновления устройства с помощью Windows PowerShell и командлета **Remove-CsDeviceUpdateRule** .</span><span class="sxs-lookup"><span data-stu-id="e580d-123">Device update rules can also be removed by using Windows PowerShell and the **Remove-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="e580d-124">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e580d-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e580d-125">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="e580d-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-single-device-update-rule-from-a-server"></a><span data-ttu-id="e580d-126">Удаление правила обновления отдельного устройства с сервера</span><span class="sxs-lookup"><span data-stu-id="e580d-126">To remove a single device update rule from a server</span></span>

  - <span data-ttu-id="e580d-127">Следующая команда удаляет правило обновления устройства d5ce3c10-2588-420A-82ac-dc2d9b1222ff9 с веб-сервера в atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="e580d-127">The following command removes the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 from the Web server on atl-cs-001.litwareinc.com.</span></span>
    
        Remove-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-remove-all-the-device-update-rules-from-a-server"></a><span data-ttu-id="e580d-128">Удаление всех правил обновления устройства с сервера</span><span class="sxs-lookup"><span data-stu-id="e580d-128">To remove all the device update rules from a server</span></span>

  - <span data-ttu-id="e580d-129">Эта команда удаляет все правила обновления устройства на веб-сервере atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="e580d-129">This command removes all the device update rules from the web server on atl-cs-001.litwareinc.com.</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*" | Remove-CsDeviceUpdateRule

</div>

<span data-ttu-id="e580d-130">Дополнительные сведения можно найти в разделе справки по командлету [Remove-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateRule) .</span><span class="sxs-lookup"><span data-stu-id="e580d-130">For details, see the Help topic for the [Remove-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e580d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e580d-131">See Also</span></span>


[<span data-ttu-id="e580d-132">Утверждение правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e580d-132">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="e580d-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e580d-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

