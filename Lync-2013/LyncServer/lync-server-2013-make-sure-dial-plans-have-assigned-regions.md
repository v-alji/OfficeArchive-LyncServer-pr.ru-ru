---
title: 'Lync Server 2013: проверка назначения регионов абонентским группам'
description: 'Lync Server 2013: Убедитесь, что для абонентских тарифов назначены регионы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Make sure dial plans have assigned regions
ms:assetid: 3da3a907-0dbf-4440-b12f-370f94dd4c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425903(v=OCS.15)
ms:contentKeyID: 48183937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c055eda221bc03de449631ba38483165a8621773
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426153"
---
# <a name="make-sure-dial-plans-lync-server-2013-have-assigned-regions"></a><span data-ttu-id="891f2-103">Проверка абонентских планов Lync Server 2013 назначенные регионы</span><span class="sxs-lookup"><span data-stu-id="891f2-103">Make sure dial plans Lync Server 2013 have assigned regions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="891f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="891f2-104">

<span> </span></span></span>

<span data-ttu-id="891f2-105">_**Тема последнего изменения:** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="891f2-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="891f2-106">Для абонентской группы, используемой для конференц-связи с телефонным подключением, необходимо указать **регион Конференц** -связи с телефонным подключением, чтобы связать номера доступа для конференц-связи с телефонным подключением с помощью соответствующей абонентской группы.</span><span class="sxs-lookup"><span data-stu-id="891f2-106">Dial plans that are used for dial-in conferencing need to have a **Dial-in conferencing region** specified to associate dial-in conferencing access numbers with the appropriate dial plan.</span></span> <span data-ttu-id="891f2-107">При создании абонентской группы следует задать регион конференц-связи с телефонным подключением, применяемый к этой абонентской группе.</span><span class="sxs-lookup"><span data-stu-id="891f2-107">When you set up a dial plan, you specify the dial-in conferencing region that applies to that dial plan.</span></span> <span data-ttu-id="891f2-108">Затем, когда вы создадите номер доступа для телефонного подключения, вы выбираете регионы, связывающие номер доступа с соответствующими абонентской абонентской панелью.</span><span class="sxs-lookup"><span data-stu-id="891f2-108">Then, when you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="891f2-109">Так как важно указать регион для всех абонентов, мы рекомендуем использовать эту процедуру, чтобы убедиться, что все абонентские группы имеют регионы.</span><span class="sxs-lookup"><span data-stu-id="891f2-109">Because it important to specify a region for all dial plans, we recommend that you use this procedure to verify that all dial plans have regions.</span></span> <span data-ttu-id="891f2-110">Этот шаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="891f2-110">This step is optional.</span></span>

<span data-ttu-id="891f2-111">С помощью командлета **Get-CsDialPlan** убедитесь, что регион задан для всех абонентских планов для конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="891f2-111">Use the **Get-CsDialPlan** cmdlet to verify whether the region is set for all dial-in conferencing dial plans.</span></span> <span data-ttu-id="891f2-112">If the region is missing from dial plans, you can use the **Set-CsDialPlan** cmdlet to set the region.</span><span class="sxs-lookup"><span data-stu-id="891f2-112">If the region is missing from dial plans, you can use the **Set-CsDialPlan** cmdlet to set the region.</span></span> <span data-ttu-id="891f2-113">Вы также можете использовать панель управления Lync Server для обновления региона в существующих абонентских тарифах.</span><span class="sxs-lookup"><span data-stu-id="891f2-113">You can also use Lync Server Control Panel to update the region in existing dial plans.</span></span> <span data-ttu-id="891f2-114">Подробнее об использовании панели управления Lync Server можно найти [в разделе Изменение абонентской группы в Lync server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="891f2-114">For details about using Lync Server Control Panel, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

<div>

## <a name="to-verify-whether-dial-plans-have-the-region-property-set"></a><span data-ttu-id="891f2-115">Проверка правильности задания регионов для абонентских групп</span><span class="sxs-lookup"><span data-stu-id="891f2-115">To verify whether dial plans have the region property set</span></span>

1.  <span data-ttu-id="891f2-116">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** или **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="891f2-116">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="891f2-117">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="891f2-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="891f2-118">Выполните следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="891f2-118">Run the following at the command prompt:</span></span>
    
        Get-CsDialPlan [-Identity <Identifier of the dial plans to be retrieved>]
    
    <span data-ttu-id="891f2-119">Например:</span><span class="sxs-lookup"><span data-stu-id="891f2-119">For example:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="891f2-120">В данном примере возвращаются все абонентские группы, настроенные для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="891f2-120">In this example, all the dial plans configured for your organization are returned.</span></span>

4.  <span data-ttu-id="891f2-121">Просмотрите возвращенные абонентские группы, чтобы выявить те из них, для которых не задан регион конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="891f2-121">Review the returned dial plans to identify any that are missing the dial-in conferencing region.</span></span> <span data-ttu-id="891f2-122">Подробные сведения можно найти в руководстве по среде Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="891f2-122">For details, see the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-set-the-region-property-for-a-dial-plan"></a><span data-ttu-id="891f2-123">Установка свойства региона для абонентской группы</span><span class="sxs-lookup"><span data-stu-id="891f2-123">To set the region property for a dial plan</span></span>

1.  <span data-ttu-id="891f2-124">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** или **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="891f2-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="891f2-125">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="891f2-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="891f2-126">Для всех абонентских групп, у которых не задан регион конференц-связи с телефонным подключением, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="891f2-126">For any dial plans that are missing the dial-in conferencing region, run:</span></span>
    
        Set-CsDialPlan [-Identity <Identity of the dial plan to be modified>] -DialinConferencingRegion "<new region>"
    
    <span data-ttu-id="891f2-127">Например:</span><span class="sxs-lookup"><span data-stu-id="891f2-127">For example:</span></span>
    
        Set-CsDialPlan -Identity Redmond -DialinConferencingRegion "US West Coast"
    
    <span data-ttu-id="891f2-128">В данном примере изменяется абонентская группа с идентификатором Redmond –  для ее свойства DialinConferencingRegion устанавливается значение «US West Coast».</span><span class="sxs-lookup"><span data-stu-id="891f2-128">In this example, the dial plan with the Identity of Redmond is modified to set the DialinConferencingRegion property to "US West Coast".</span></span> <span data-ttu-id="891f2-129">Подробные сведения можно найти в руководстве по среде Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="891f2-129">For details, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="891f2-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="891f2-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

