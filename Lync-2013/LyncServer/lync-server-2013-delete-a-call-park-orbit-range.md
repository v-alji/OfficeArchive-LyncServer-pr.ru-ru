---
title: 'Lync Server 2013: Удаление диапазона на орбите с помощью кнопки "приостановить Звонок"'
description: 'Lync Server 2013: Удаление диапазона на орбите.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Call Park orbit range
ms:assetid: 85e9f916-062d-450d-ac0a-aeaefc0f7cdc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182546(v=OCS.15)
ms:contentKeyID: 48184713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5fb0bbd34a1f151b32067b7375948f712fa6d902
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430751"
---
# <a name="delete-a-call-park-orbit-range-in-lync-server-2013"></a><span data-ttu-id="65942-103">Удаление диапазона орбиты на расстоянии вверх на сервере Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65942-103">Delete a Call Park orbit range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65942-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65942-104">

<span> </span></span></span>

<span data-ttu-id="65942-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="65942-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="65942-106">Для удаления диапазона на расстоянии по орбите воспользуйтесь одной из описанных ниже процедур.</span><span class="sxs-lookup"><span data-stu-id="65942-106">Use one of the following procedures to delete a Call Park orbit range.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-a-call-park-orbit-range"></a><span data-ttu-id="65942-107">Использование панели управления Lync Server для удаления диапазона орбиты с приостановкой</span><span class="sxs-lookup"><span data-stu-id="65942-107">To use Lync Server Control Panel to delete a Call Park orbit range</span></span>

1.  <span data-ttu-id="65942-108">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="65942-108">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="65942-109">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="65942-109">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="65942-110">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="65942-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="65942-111">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="65942-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="65942-112">На панели навигации слева щелкните пункт **Функции голосовой связи**, а затем щелкните **Парковка вызовов**.</span><span class="sxs-lookup"><span data-stu-id="65942-112">In the left navigation bar, click **Voice Features** and then click **Call Park**.</span></span>

4.  <span data-ttu-id="65942-113">На странице "Приостановка **звонка** " в поле "Поиск" введите имя или часть названия диапазона на орбите, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="65942-113">On the **Call Park** page, in the search field, type all or part of the name of the orbit range that you want to delete.</span></span>

5.  <span data-ttu-id="65942-114">В появившемся списке орбит нажмите на орбиту, выберите команду **изменить**, а затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="65942-114">In the resulting list of orbits, click the orbit, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="65942-115">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="65942-115">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-call-park-orbit-range"></a><span data-ttu-id="65942-116">Использование Windows PowerShell для удаления диапазона на расстоянии по орбите</span><span class="sxs-lookup"><span data-stu-id="65942-116">To use Windows PowerShell to delete a Call Park orbit range</span></span>

1.  <span data-ttu-id="65942-117">Войдите на компьютер, на котором установлена командная консоль Lync Server Management Shell, в группу RTCUniversalServerAdmins или с необходимыми правами пользователя, как описано в разделе [Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="65942-117">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="65942-118">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="65942-118">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="65942-119">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="65942-119">At the command line, type:</span></span>
    
        Remove-CsCallParkOrbit -Identity "<orbit range name>" 
    
    <span data-ttu-id="65942-120">Например:</span><span class="sxs-lookup"><span data-stu-id="65942-120">For example:</span></span>
    
        Remove-CsCallParkOrbit -Identity "Redmond orbit 1"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="65942-121">Подробнее о дополнительных параметрах можно найти в разделе <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span><span class="sxs-lookup"><span data-stu-id="65942-121">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="65942-122">См. также</span><span class="sxs-lookup"><span data-stu-id="65942-122">See Also</span></span>


[<span data-ttu-id="65942-123">Создание или изменение диапазона орбиты на расстоянии вверх на сервере Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65942-123">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)  


[<span data-ttu-id="65942-124">Remove-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="65942-124">Remove-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit)  
[<span data-ttu-id="65942-125">Get-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="65942-125">Get-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCallParkOrbit)  
  

<span data-ttu-id="65942-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65942-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

