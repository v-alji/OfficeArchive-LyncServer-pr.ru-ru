---
title: 'Lync Server 2013: Просмотр сведений о абонентской группе'
description: 'Lync Server 2013: Просмотр сведений о абонентской группе.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View dial plan information
ms:assetid: 25ed0112-a8a7-418a-8c2c-580081be692a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687997(v=OCS.15)
ms:contentKeyID: 49733587
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b4473302b182b8de4ea6aad12d7993cb5d442b7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423395"
---
# <a name="view-dial-plan-information-in-lync-server-2013"></a><span data-ttu-id="14599-103">Просмотр сведений о абонентской схеме в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14599-103">View dial plan information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14599-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14599-104">

<span> </span></span></span>

<span data-ttu-id="14599-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="14599-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="14599-106">Чтобы просмотреть сведения о существующей абонентской группе, выполните действия, описанные в описанной ниже процедуре.</span><span class="sxs-lookup"><span data-stu-id="14599-106">To view information for an existing dial plan, perform the steps in the following procedure.</span></span> <span data-ttu-id="14599-107">Если вы хотите создать новую абонентскую группу, ознакомьтесь со сведениями [Создание абонентской группы в Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="14599-107">If you want to create a new dial plan, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<div>

## <a name="to-view-information-about-a-dial-plan-from-lync-server-control-panel"></a><span data-ttu-id="14599-108">Просмотр сведений о абонентской группе из панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="14599-108">To view information about a dial plan from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="14599-109">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="14599-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="14599-110">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="14599-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="14599-111">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="14599-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="14599-112">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="14599-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="14599-113">В левой панели навигации щелкните **Маршрутизация голосовой связи** и затем щелкните **Абонентская группа**.</span><span class="sxs-lookup"><span data-stu-id="14599-113">In the left navigation bar, click **Voice Routing** and then click **Dial Plan**.</span></span>

4.  <span data-ttu-id="14599-114">На странице **Абонентская группа** дважды щелкните имя абонентской группы.</span><span class="sxs-lookup"><span data-stu-id="14599-114">On the **Dial Plan** page, double-click a dial plan name.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="14599-115">Вы можете просматривать сведения только для одной абонентской группы за раз.</span><span class="sxs-lookup"><span data-stu-id="14599-115">You can view information for only one dial plan at a time.</span></span>

    
    </div>

</div>

<div>

## <a name="to-view-dial-plans-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="14599-116">Просмотр абонентских планов с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="14599-116">To view dial plans by using Windows PowerShell cmdlets</span></span>

  - <span data-ttu-id="14599-117">Абонентские группы можно просмотреть с помощью интерфейса командной строки Windows PowerShell и командлета **Get-CsDialPlan** .</span><span class="sxs-lookup"><span data-stu-id="14599-117">Dial plans can be viewed by using the Windows PowerShell command-line interface and the **Get-CsDialPlan** cmdlet.</span></span> <span data-ttu-id="14599-118">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14599-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="14599-119">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="14599-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="14599-120">Чтобы просмотреть сведения обо всех абонентских тарифах, введите в командной консоли Lync Server следующую команду и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="14599-120">To view information about all your dial plans, type the following command in the Lync Server Management Shell, and then press ENTER:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="14599-121">Эта команда возвратит примерно такую информацию:</span><span class="sxs-lookup"><span data-stu-id="14599-121">That command will return information similar to this:</span></span>
    
        Identity                 : Global
        Description              :
        DialinConferencingRegion :
        NormalizationRules       : {Description=;
                                   Pattern=^(\d+)$;Translation=$1;Name=
                                   KeepAll;IsInternalExtension=False}
        CountryCode              :
        State                    :
        City                     :
        ExternalAccessPrefix     :
        SimpleName               : DefaultProfile
        OptimizeDeviceDialing    : False

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="14599-122">См. также</span><span class="sxs-lookup"><span data-stu-id="14599-122">See Also</span></span>


[<span data-ttu-id="14599-123">Создание абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14599-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="14599-124">Изменение абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14599-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
  

<span data-ttu-id="14599-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14599-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

