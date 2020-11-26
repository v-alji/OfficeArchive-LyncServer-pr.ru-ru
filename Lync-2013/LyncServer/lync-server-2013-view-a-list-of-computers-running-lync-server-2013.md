---
title: 'Lync Server 2013: Просмотр списка компьютеров с Lync Server 2013'
description: 'Lync Server 2013: Просмотр списка компьютеров с Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View a list of computers running Lync Server 2013
ms:assetid: 44eeec27-8b99-44f0-b0bd-622c12393d34
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520987(v=OCS.15)
ms:contentKeyID: 48184030
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: baeb2d8e926b1597c463259378332e0c9f50268f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440425"
---
# <a name="view-a-list-of-computers-running-lync-server-2013"></a><span data-ttu-id="3f093-103">Просмотр списка компьютеров с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f093-103">View a list of computers running Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f093-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f093-104">

<span> </span></span></span>

<span data-ttu-id="3f093-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="3f093-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="3f093-106">Вы можете использовать панель управления Lync Server 2013 для просмотра списка всех компьютеров с операционной системой Lync Server 2013 в вашей топологии и просмотра состояния службы каждого из них.</span><span class="sxs-lookup"><span data-stu-id="3f093-106">You can use Lync Server 2013 Control Panel to view a list of all the computers that are running Lync Server 2013 in your topology and see the service status of each.</span></span> <span data-ttu-id="3f093-107">Вы можете отсортировать список по компьютеру, пулу или сайту.</span><span class="sxs-lookup"><span data-stu-id="3f093-107">You can sort the list by computer, pool, or site.</span></span>

<div>

## <a name="to-view-a-list-of-computers-running-lync-server"></a><span data-ttu-id="3f093-108">Просмотр списка компьютеров с Lync Server</span><span class="sxs-lookup"><span data-stu-id="3f093-108">To view a list of computers running Lync Server</span></span>

1.  <span data-ttu-id="3f093-109">Из учетной записи пользователя, назначенной какой-либо из предопределенных административных ролей для Lync Server 2013, войдите на любой компьютер во внутренней среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="3f093-109">From a user account that is assigned to any of the predefined administrative roles for Lync Server 2013, log on to any computer in your internal deployment.</span></span> <span data-ttu-id="3f093-110">Подробные сведения о стандартных ролях администратора, доступных в Lync Server 2013, можно найти [в разделе Планирование управления доступом на основе ролей в Lync server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="3f093-110">For details about the predefined administrative roles available in Lync Server 2013, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span></span>

2.  <span data-ttu-id="3f093-111">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3f093-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3f093-112">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3f093-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3f093-113">На панели навигации слева щелкните **топология** и выберите **состояние**.</span><span class="sxs-lookup"><span data-stu-id="3f093-113">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="3f093-114">На странице " **состояние** " выполните любое из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="3f093-114">On the **Status** page, do any of the following as needed:</span></span>
    
      - <span data-ttu-id="3f093-115">Чтобы отсортировать список, щелкните заголовок столбца **компьютер**, **пул** или **сайт** , а затем нажмите стрелку вверх или стрелка вниз.</span><span class="sxs-lookup"><span data-stu-id="3f093-115">Sort the list by clicking the **Computer**, **Pool**, or **Site** column heading, and then clicking the up arrow or the down arrow.</span></span>
    
      - <span data-ttu-id="3f093-116">Нажмите кнопку **Обновить** , чтобы просмотреть список самых последних обновлений.</span><span class="sxs-lookup"><span data-stu-id="3f093-116">Click **Refresh** to view the most up-to-date list.</span></span>
    
      - <span data-ttu-id="3f093-117">Поиск определенного компьютера с помощью ввода имени компьютера в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="3f093-117">Search for a specific computer by typing the computer name in the search field.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3f093-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3f093-118">See Also</span></span>


[<span data-ttu-id="3f093-119">Управление топологией Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f093-119">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="3f093-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f093-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

