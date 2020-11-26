---
title: 'Lync Server 2013: Удаление группы агента'
description: 'Lync Server 2013: Удаление группы агента.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an agent group
ms:assetid: df385fd1-62f4-42b7-a349-4eb38dea50c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182597(v=OCS.15)
ms:contentKeyID: 48185670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dded2db0957e37a624d7e8bf3a06e102f8d35cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430646"
---
# <a name="delete-an-agent-group-in-lync-server-2013"></a><span data-ttu-id="ca609-103">Удаление группы агента в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca609-103">Delete an agent group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ca609-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ca609-104">

<span> </span></span></span>

<span data-ttu-id="ca609-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ca609-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ca609-106">Для удаления группы агента воспользуйтесь одной из описанных ниже процедур.</span><span class="sxs-lookup"><span data-stu-id="ca609-106">Use one of the following procedures to delete an agent group.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-agent-group"></a><span data-ttu-id="ca609-107">Удаление группы агента с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="ca609-107">To use Lync Server Control Panel to delete an agent group</span></span>

1.  <span data-ttu-id="ca609-108">Выполните вход как член группы RTCUniversalServerAdmins или одной из предварительно заданных административных ролей, поддерживающих группу ответа.</span><span class="sxs-lookup"><span data-stu-id="ca609-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="ca609-109">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ca609-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ca609-110">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ca609-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ca609-111">В левой области навигации щелкните **Группы ответа**, затем **Группа**.</span><span class="sxs-lookup"><span data-stu-id="ca609-111">In the left navigation bar, click **Response Groups**, and then click **Group**.</span></span>

4.  <span data-ttu-id="ca609-112">На странице **группы ответа** введите имя или часть имени группы агента, которую вы хотите удалить, в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="ca609-112">On the **Response Groups** page, type all or part of the name of the agent group that you want to delete in the search field.</span></span>

5.  <span data-ttu-id="ca609-113">В списке результатов выберите группу, которую вы хотите удалить, и нажмите кнопку **изменить**, а затем — **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="ca609-113">In the resulting list, click the group that you want to delete, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="ca609-114">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ca609-114">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-agent-group"></a><span data-ttu-id="ca609-115">Использование Windows PowerShell для удаления группы агента</span><span class="sxs-lookup"><span data-stu-id="ca609-115">To use Windows PowerShell to delete an agent group</span></span>

1.  <span data-ttu-id="ca609-116">Выполните вход как член группы RTCUniversalServerAdmins или одной из предварительно заданных административных ролей, поддерживающих группу ответа.</span><span class="sxs-lookup"><span data-stu-id="ca609-116">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="ca609-117">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="ca609-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ca609-118">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ca609-118">At the command line, run:</span></span>
    
        Get-CsRgsAgentGroup -Identity <Application Server service> -Name "<name of agent group>" | Remove-CsRgsAgentGroup
    
    <span data-ttu-id="ca609-119">Например:</span><span class="sxs-lookup"><span data-stu-id="ca609-119">For example:</span></span>
    
        Get-CsRgsAgentGroup -Identity service:ApplicationServer:redmond.contoso.com -Name "Human Resources" | Remove-CsRgsAgentGroup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ca609-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ca609-120">See Also</span></span>


[<span data-ttu-id="ca609-121">Создание или изменение группы агента в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca609-121">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  


[<span data-ttu-id="ca609-122">Remove-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="ca609-122">Remove-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsAgentGroup)  
[<span data-ttu-id="ca609-123">Get-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="ca609-123">Get-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsAgentGroup)  
  

<span data-ttu-id="ca609-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ca609-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

