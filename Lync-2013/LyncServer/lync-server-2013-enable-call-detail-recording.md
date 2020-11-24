---
title: 'Lync Server 2013: включение записи сведений о звонке'
description: 'Lync Server 2013: включение записи сведений о звонке.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable call detail recording
ms:assetid: 3b28e432-596f-45a5-a070-577d6fa748d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520980(v=OCS.15)
ms:contentKeyID: 48183865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d565c78571e34cead61777381875c9c8d23dae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399307"
---
# <a name="enable-call-detail-recording-in-lync-server-2013"></a><span data-ttu-id="f29a4-103">Включение записи сведений о вызовах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f29a4-103">Enable call detail recording in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f29a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f29a4-104">

<span> </span></span></span>

<span data-ttu-id="f29a4-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f29a4-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f29a4-p101">Функция регистрации вызовов (CDR) записывает сведения об использовании и диагностические данные для одноранговых операций, включая обмен мгновенными сообщениями, звонки VoIP, общий доступ к приложениям, передачу файлов и собрания. С помощью данных об использовании можно вычислить рентабельность инвестиций, а диагностические данные можно использовать при поиске и устранении проблем с одноранговыми операциями и собраниями.</span><span class="sxs-lookup"><span data-stu-id="f29a4-p101">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings. The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span>

<span data-ttu-id="f29a4-108">Используйте следующую процедуру, чтобы включить регистрацию вызовов для всей своей организации или каждого ее сайта.</span><span class="sxs-lookup"><span data-stu-id="f29a4-108">Use the following procedure to enable CDR for your whole organization or each site in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f29a4-109">Чтобы включить CDR, необходимо сначала настроить мониторинг и базу данных мониторинга.</span><span class="sxs-lookup"><span data-stu-id="f29a4-109">In order to enable CDR you must configure monitoring and a monitoring database.</span></span> <span data-ttu-id="f29a4-110">Подробные сведения можно найти <A href="lync-server-2013-deploying-monitoring.md">в разделе Развертывание мониторинга в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f29a4-110">For details, see <A href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-cdr-with-lync-server-control-panel"></a><span data-ttu-id="f29a4-111">Включение CDR с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="f29a4-111">To enable CDR with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="f29a4-112">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f29a4-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="f29a4-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f29a4-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f29a4-114">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f29a4-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f29a4-115">В левой панели навигации щелкните **Мониторинг и архивирование**, а затем — **Регистрация вызовов**.</span><span class="sxs-lookup"><span data-stu-id="f29a4-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="f29a4-116">На странице **Служба регистрации вызовов** выберите соответствующий сайт в таблице, щелкните элемент **Действие** и затем **Включить CDR**.</span><span class="sxs-lookup"><span data-stu-id="f29a4-116">On the **Call Detail Recording** page, click the appropriate site from the table, click **Action**, and then click **Enable CDR**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f29a4-117">По умолчанию функция CDR включена.</span><span class="sxs-lookup"><span data-stu-id="f29a4-117">CDR is enabled by default.</span></span>

    
    </div>

</div>

<div>

## <a name="enabling-cdr-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f29a4-118">Включение CDR с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f29a4-118">Enabling CDR by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f29a4-119">Вы можете включить CDR с помощью Windows PowerShell и командлета **Set-CsCdrConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f29a4-119">You can enable CDR by using Windows PowerShell and the **Set-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="f29a4-120">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f29a4-120">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f29a4-121">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="f29a4-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-cdr-for-a-single-location"></a><span data-ttu-id="f29a4-122">Включение CDR для отдельного места</span><span class="sxs-lookup"><span data-stu-id="f29a4-122">To enable CDR for a single location</span></span>

  - <span data-ttu-id="f29a4-123">Чтобы отключить CDR, задайте для параметра EnableCDR значение True ($True).</span><span class="sxs-lookup"><span data-stu-id="f29a4-123">To disable CDR, set the EnableCDR parameter to True ($True).</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $True

</div>

<div>

## <a name="to-disable-cdr-for-a-single-location"></a><span data-ttu-id="f29a4-124">Чтобы отключить CDR для отдельного места</span><span class="sxs-lookup"><span data-stu-id="f29a4-124">To disable CDR for a single location</span></span>

  - <span data-ttu-id="f29a4-p105">Чтобы отключить CDR, задайте для параметра EnableCDR значение False ($False). Отключение CDR не приводит к удалению мониторинга. Оно приостанавливает сбор и сохранение данных CDR.</span><span class="sxs-lookup"><span data-stu-id="f29a4-p105">To disable CDR, set the EnableCDR parameter to False ($False). Disabling CDR does not uninstall monitoring. It pauses the collection and storage of CDR data.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

</div>

<div>

## <a name="to-use-a-single-command-to-enable-cdr-in-multiple-locations"></a><span data-ttu-id="f29a4-128">Чтобы использовать отдельную команду для включения CDR в нескольких местах, выполните следующие действия</span><span class="sxs-lookup"><span data-stu-id="f29a4-128">To use a single command to enable CDR in multiple locations</span></span>

  - <span data-ttu-id="f29a4-129">Эта команда включает CDR для всех параметров конфигурации CDR, используемых в настоящее время в организации.</span><span class="sxs-lookup"><span data-stu-id="f29a4-129">This command enables CDR for all the CDR configuration settings currently in use in your organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration "site:Redmond" -EnableCDR $True

</div>

<span data-ttu-id="f29a4-130">Дополнительные сведения можно найти в разделе справки по командлету [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="f29a4-130">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f29a4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f29a4-131">See Also</span></span>


[<span data-ttu-id="f29a4-132">Планирование мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f29a4-132">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)  
[<span data-ttu-id="f29a4-133">Развертывание мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f29a4-133">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="f29a4-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f29a4-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

