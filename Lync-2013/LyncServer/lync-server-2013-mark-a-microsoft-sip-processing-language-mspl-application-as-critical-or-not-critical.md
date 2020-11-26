---
title: 'Lync Server 2013: Пометка приложения на языке обработки Microsoft SIP (MSPL) как критическое или некритическое'
description: 'Lync Server 2013: Пометка приложения на языке обработки Microsoft SIP (MSPL) как критическое или не критическое.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mark a Microsoft SIP Processing Language (MSPL) application as critical or not critical
ms:assetid: df68fdc6-b7e6-4f07-acdc-0cd4c2c888a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182598(v=OCS.15)
ms:contentKeyID: 48185622
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1f59fb6614416c1b0e4f49a766a1373483f509d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425761"
---
# <a name="mark-a-microsoft-sip-processing-language-mspl-application-as-critical-or-not-critical-in-lync-server-2013"></a><span data-ttu-id="a7433-103">Пометка приложения на языке обработки Microsoft SIP (MSPL) как критическое или некритическое в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7433-103">Mark a Microsoft SIP Processing Language (MSPL) application as critical or not critical in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7433-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7433-104">

<span> </span></span></span>

<span data-ttu-id="a7433-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a7433-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a7433-106">Серверные приложения Microsoft SIP Language (MSPL) — это приложения только сценария, использующие язык сценариев MSPL вместо Microsoft Lync 2010 API.</span><span class="sxs-lookup"><span data-stu-id="a7433-106">Microsoft SIP Processing Language (MSPL) server applications are script-only applications that use the MSPL scripting language instead of the Microsoft Lync 2010 API.</span></span> <span data-ttu-id="a7433-107">Некоторые серверные приложения MSPL задаются как критические.</span><span class="sxs-lookup"><span data-stu-id="a7433-107">Some MSPL server applications are specified as critical.</span></span> <span data-ttu-id="a7433-108">Если сценарий является критическим, во время запуска системы необходимо запустить сценарий, чтобы Lync Server 2013 начал работу.</span><span class="sxs-lookup"><span data-stu-id="a7433-108">If a script is critical, the script must start during system startup in order for Lync Server 2013 to start.</span></span> <span data-ttu-id="a7433-109">Если при запуске Lync Server происходит сбой сценария, сервер не завершает работу, но перестает передавать трафик сценариям и записывает ошибки в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="a7433-109">If the script fails while Lync Server is running, the server does not shut down, but it stops sending traffic to the script, and it writes errors in the event log.</span></span>

<span data-ttu-id="a7433-110">С помощью панели управления Lync Server можно помечать серверные приложения на языке обработки Microsoft SIP (MSPL) как критические или не помечать их.</span><span class="sxs-lookup"><span data-stu-id="a7433-110">You can use Lync Server Control Panel to mark Microsoft SIP Processing Language (MSPL) server applications as critical or unmark them.</span></span>

<span data-ttu-id="a7433-111">Этот параметр поддерживают не все сценарии.</span><span class="sxs-lookup"><span data-stu-id="a7433-111">Not all scripts support this option.</span></span> <span data-ttu-id="a7433-112">Например, сценарий DefaultRouting помечается как критический, и этот параметр невозможно изменить для DefaultRouting.</span><span class="sxs-lookup"><span data-stu-id="a7433-112">For example, the DefaultRouting script is marked as critical, and this option cannot be changed for DefaultRouting.</span></span>

<div>

## <a name="to-mark-or-unmark-an-mspl-server-application-as-critical"></a><span data-ttu-id="a7433-113">Пометка или снятие пометки приложения сервера MSPL как критического</span><span class="sxs-lookup"><span data-stu-id="a7433-113">To mark or unmark an MSPL server application as critical</span></span>

1.  <span data-ttu-id="a7433-114">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a7433-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="a7433-115">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a7433-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a7433-116">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a7433-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a7433-117">На панели навигации слева выберите пункт **топология** и щелкните **серверное приложение**.</span><span class="sxs-lookup"><span data-stu-id="a7433-117">In the left navigation bar, click **Topology** and then click **Server Application**.</span></span>

4.  <span data-ttu-id="a7433-118">На странице **серверное приложение** щелкните заголовок столбца, чтобы отсортировать приложения, если необходимо, а затем выберите серверное приложение, которое вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="a7433-118">On the **Server Application** page, click a column heading to sort the applications, if needed, and then click the server application that you want to modify.</span></span>

5.  <span data-ttu-id="a7433-119">Нажмите кнопку **действие**.</span><span class="sxs-lookup"><span data-stu-id="a7433-119">Click **Action**.</span></span>

6.  <span data-ttu-id="a7433-120">Выберите команду **помечать как критические** или **снимите флажок как критический** (то есть, если сценарий поддерживает этот параметр).</span><span class="sxs-lookup"><span data-stu-id="a7433-120">Click **Mark as critical** or **Unselect as critical** (that is, if the script supports this option).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a7433-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a7433-121">See Also</span></span>


[<span data-ttu-id="a7433-122">Включение и отключение серверного приложения Microsoft SIP Languageing (MSPL) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7433-122">Enable or disable a Microsoft SIP Processing Language (MSPL) server application in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-a-microsoft-sip-processing-language-mspl-server-application.md)  


[<span data-ttu-id="a7433-123">Просмотр серверных приложений Microsoft SIP Processing Language (MSPL) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7433-123">View Microsoft SIP Processing Language (MSPL) server applications in Lync Server 2013</span></span>](lync-server-2013-view-microsoft-sip-processing-language-mspl-server-applications.md)  


[<span data-ttu-id="a7433-124">Управление топологией Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7433-124">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="a7433-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7433-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

