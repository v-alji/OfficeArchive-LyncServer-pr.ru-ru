---
title: 'Lync Server 2013: сброс правила обновления устройства'
description: 'Lync Server 2013: сброс правила обновления устройства.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reset a Device Update rule
ms:assetid: d1f597e7-dffd-4756-af07-10613a5d8729
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994069(v=OCS.15)
ms:contentKeyID: 51803980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8a4d42b6aee8f4cb3fd93839b4a8575059ba71cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436372"
---
# <a name="reset-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="3b0d1-103">Сброс правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b0d1-103">Reset a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b0d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b0d1-104">

<span> </span></span></span>

<span data-ttu-id="3b0d1-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="3b0d1-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="3b0d1-106">Если вы не хотите, чтобы обновление работало на тестовом устройстве, вы можете сбросить правило обновления устройства, которое удаляет состояние ожидания правила и удаление обновления с тестовых устройств.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-106">If you don’t like the way that an update works on your test devices, you can reset the device update rule, which removes the rule’s pending status and uninstalls the update from the test devices.</span></span>

<span data-ttu-id="3b0d1-107">Вы можете удалить правило обновления устройства с помощью панели управления Lync Server или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-107">You can remove a device update rule by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3b0d1-108">Чтобы удалить правило, которое вы уже утвердили (то есть выпало из него), восстановите его.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-108">To uninstall a rule that you’ve already approved (that is, rolled out), restore it.</span></span> <span data-ttu-id="3b0d1-109">Подробности можно найти <A href="lync-server-2013-restore-a-device-update-rule.md">в разделе Восстановление правила обновления устройства в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-109">For details, see <A href="lync-server-2013-restore-a-device-update-rule.md">Restore a Device Update rule in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-device-update-rule-by-using-lync-server-control-panel"></a><span data-ttu-id="3b0d1-110">Сброс правила обновления устройства с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="3b0d1-110">To reset a device update rule by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="3b0d1-111">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3b0d1-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3b0d1-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3b0d1-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3b0d1-114">На панели навигации слева выберите пункт **Клиенты** и нажмите кнопку Навигация по **обновлению устройства** .</span><span class="sxs-lookup"><span data-stu-id="3b0d1-114">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span>

4.  <span data-ttu-id="3b0d1-115">На странице **обновление устройства** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-115">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="3b0d1-116">Чтобы сбросить одно правило, выберите правило, которое вы хотите сбросить.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-116">To reset one rule, select the rule you want to reset.</span></span>
    
      - <span data-ttu-id="3b0d1-117">Чтобы сбросить все правила, в меню **Правка** выберите команду **выделить все**.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-117">To reset all rules, on the **Edit** menu, click **Select All**.</span></span>
    
      - <span data-ttu-id="3b0d1-118">Чтобы сбросить все правила для одной торговой марки, используйте меню столбец " **бренд** ".</span><span class="sxs-lookup"><span data-stu-id="3b0d1-118">To reset all rules for one brand, use the **Brand** column menu.</span></span>

5.  <span data-ttu-id="3b0d1-119">Нажмите кнопку **действие** и выберите пункт **отменить ожидающие обновления**.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-119">Click **Action**, and then click **Cancel pending updates**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="3b0d1-120">Если вы уверены в том, что вы не хотите выгрузить правила обновления устройства, которые вы отменили, возможно, потребуется удалить их.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-120">If you’re sure you’ll never want to roll out the device update rule(s) that you cancelled, you might want to delete them.</span></span> <span data-ttu-id="3b0d1-121">Подробности можно найти <A href="lync-server-2013-remove-a-device-update-rule.md">в разделе Удаление правила обновления устройства в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-121">For details, see <A href="lync-server-2013-remove-a-device-update-rule.md">Remove a Device Update rule in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="resetting-a-device-update-rule-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="3b0d1-122">Сброс правила обновления устройства с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b0d1-122">Resetting a Device Update Rule by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="3b0d1-123">Кроме того, вы можете сбросить правила обновления устройства с помощью Windows PowerShell и командлета **Reset-CsDeviceUpdateRule** .</span><span class="sxs-lookup"><span data-stu-id="3b0d1-123">Device update rules can also be reset by using Windows PowerShell and the **Reset-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="3b0d1-124">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3b0d1-125">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="3b0d1-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-specific-device-update-rule-on-a-server"></a><span data-ttu-id="3b0d1-126">Сброс правила обновления для определенного устройства на сервере</span><span class="sxs-lookup"><span data-stu-id="3b0d1-126">To reset a specific device update rule on a server</span></span>

  - <span data-ttu-id="3b0d1-127">Следующая команда сбрасывает правило обновления устройства d5ce3c10-2588-420A-82ac-dc2d9b1222ff9 на веб-сервере atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="3b0d1-127">The following command resets the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Reset-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-reset-all-the-device-update-rules-on-a-server"></a><span data-ttu-id="3b0d1-128">Сброс всех правил обновления устройства на сервере</span><span class="sxs-lookup"><span data-stu-id="3b0d1-128">To reset all the device update rules on a server</span></span>

  - <span data-ttu-id="3b0d1-129">Эта команда сбрасывает все правила обновления устройства на веб-сервере atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="3b0d1-129">This command resets all the device update rules on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*"  | Reset-CsDeviceUpdateRule

</div>

<div>

## <a name="to-reset-all-the-device-updates-rules-that-have-a-specific-brand"></a><span data-ttu-id="3b0d1-130">Сброс всех правил обновления устройства, для которых определена фирменная символика</span><span class="sxs-lookup"><span data-stu-id="3b0d1-130">To reset all the device updates rules that have a specific brand</span></span>

  - <span data-ttu-id="3b0d1-131">В этом примере все обновления для устройств, на которых установлен Межфирменная символика (Майкрософт), сбрасываются.</span><span class="sxs-lookup"><span data-stu-id="3b0d1-131">In this example, all the device updates throughout the organization that have a Brand equal to Microsoft are reset:</span></span>
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Reset-CsDeviceUpdateRule

</div>

<span data-ttu-id="3b0d1-132">Дополнительные сведения можно найти в разделе справки по командлету [Reset-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) .</span><span class="sxs-lookup"><span data-stu-id="3b0d1-132">For details, see the Help topic for the [Reset-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3b0d1-133">См. также</span><span class="sxs-lookup"><span data-stu-id="3b0d1-133">See Also</span></span>


[<span data-ttu-id="3b0d1-134">Утверждение правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b0d1-134">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="3b0d1-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b0d1-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

