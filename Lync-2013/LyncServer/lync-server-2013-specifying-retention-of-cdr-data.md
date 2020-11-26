---
title: 'Lync Server 2013: указание хранения данных CDR'
description: 'Lync Server 2013: указание хранения данных CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Specifying retention of CDR data
ms:assetid: c0fd6056-87bc-4136-902a-f1b37cd3a1ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182581(v=OCS.15)
ms:contentKeyID: 48185299
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9367721a2390ad701702818590ac14e69da0df9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423787"
---
# <a name="specifying-retention-of-cdr-data-in-lync-server-2013"></a><span data-ttu-id="77ea7-103">Определение хранения данных CDR в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77ea7-103">Specifying retention of CDR data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="77ea7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="77ea7-104">

<span> </span></span></span>

<span data-ttu-id="77ea7-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="77ea7-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="77ea7-p101">По умолчанию данные регистрации вызовов (CDR) удаляются по прошествии 60 дней. Можно использовать параметры на странице **Регистрация вызовов**, чтобы задать хранение данных в течение большего или меньшего времени. Если отключить CDR, то данные, которые были записаны до включения CDR, также будут удаляться.</span><span class="sxs-lookup"><span data-stu-id="77ea7-p101">By default, call detail recording (CDR) data is purged after 60 days. You can use the settings on the **Call Detail Recording** page to retain the data for a longer or shorter period of time. If you disable CDR, data that was captured before CDR was enabled will also be subject to purging.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="77ea7-p102">Необходимо настроить CDR и качество взаимодействия (QoE) для хранения данных в течении одинакового числа дней. Каждый звонок в отчетах CDR, доступных на веб-странице отчетов сервера мониторинга, включает сведения CDR и качества взаимодействия. Если время для удаления данных CDR и качества взаимодействия отличается, некоторые звонки могут содержать только данные CDR, а другие могут содержать только данные качества взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="77ea7-p102">You should configure CDR and Quality of Experience (QoE) to retain data for the same number of days. Each call in the call detail reports (CDRs), available from the Monitoring Server Reports webpage, includes CDR and QoE information. If the purging duration for CDR and QoE is different, some calls might only include CDR data, while other may only include QoE data.</span></span>



</div>

<span data-ttu-id="77ea7-112">Для настройки параметров очистки данных CDR используется следующая процедура.</span><span class="sxs-lookup"><span data-stu-id="77ea7-112">Use the following procedures to configure purge settings for CDR data.</span></span>

<div>

## <a name="to-specify-retention-of-cdr-data"></a><span data-ttu-id="77ea7-113">Настройка хранения данных CDR</span><span class="sxs-lookup"><span data-stu-id="77ea7-113">To specify retention of CDR data</span></span>

1.  <span data-ttu-id="77ea7-114">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="77ea7-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="77ea7-115">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="77ea7-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="77ea7-116">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="77ea7-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="77ea7-117">В левой панели навигации щелкните **Мониторинг и архивирование**, а затем — **Регистрация вызовов**.</span><span class="sxs-lookup"><span data-stu-id="77ea7-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="77ea7-118">На странице **Регистрация вызовов** в таблице щелкните необходимый сайт, щелкните **Правка**, а затем — **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="77ea7-118">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="77ea7-119">Чтобы включить удаление, выберите параметр **Enable Purging of CDRs** (Включить очистку CDR).</span><span class="sxs-lookup"><span data-stu-id="77ea7-119">To turn on purging, select **Enable purging of CDRs**.</span></span>

6.  <span data-ttu-id="77ea7-120">В параметре **Keep call detail recordings CDRs for maximum duration (days):** (Сохранять CDR не более (дней)) выберите максимальное число дней, в течение которых должны храниться данные регистрации вызовов.</span><span class="sxs-lookup"><span data-stu-id="77ea7-120">In **Keep CDRs for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="77ea7-121">В параметре **Хранить сведения отчетов об ошибках максимум в течение (дней):** выберите максимальное число дней, в течение которых должны храниться данные отчетов об ошибках.</span><span class="sxs-lookup"><span data-stu-id="77ea7-121">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="77ea7-122">Щелкните **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="77ea7-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="specifying-cdr-retention-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="77ea7-123">Указание хранения CDR с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="77ea7-123">Specifying CDR Retention by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="77ea7-124">Вы можете создать параметры хранения CDR с помощью Windows PowerShell и командлета Set-CsCdrConfiguration.</span><span class="sxs-lookup"><span data-stu-id="77ea7-124">You can create CDR retention settings by using Windows PowerShell and the Set-CsCdrConfiguration cmdlet.</span></span> <span data-ttu-id="77ea7-125">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77ea7-125">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="77ea7-126">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="77ea7-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-specify-cdr-retention-for-a-specific-location"></a><span data-ttu-id="77ea7-127">Задание параметров хранения CDR для конкретного расположения</span><span class="sxs-lookup"><span data-stu-id="77ea7-127">To specify CDR retention for a specific location</span></span>

  - <span data-ttu-id="77ea7-128">Эта команда позволяет очищать данные CDR для сайта Redmond и настраивает сайт для обслуживания данных CDR и данных отчетов об ошибках в течение 20 дней.</span><span class="sxs-lookup"><span data-stu-id="77ea7-128">This command enables purging of CDR data for the Redmond site, and configures the site to maintain both CDR data and error reports data for 20 days.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<div>

## <a name="to-specify-cdr-retention-for-multiple-locations"></a><span data-ttu-id="77ea7-129">Задание параметров хранения CDR для нескольких расположений</span><span class="sxs-lookup"><span data-stu-id="77ea7-129">To specify CDR retention for multiple locations</span></span>

  - <span data-ttu-id="77ea7-130">Эта команда настраивает параметры хранения CDR для всех параметров конфигурации CDR, используемых в организации.</span><span class="sxs-lookup"><span data-stu-id="77ea7-130">This command configures CDR retention for all the CDR configuration settings in use in an organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration-EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<span data-ttu-id="77ea7-131">Дополнительные сведения можно найти в разделе справки по командлету [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="77ea7-131">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="77ea7-132">См. также</span><span class="sxs-lookup"><span data-stu-id="77ea7-132">See Also</span></span>


[<span data-ttu-id="77ea7-133">Запись сведений о звонке (CDR) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77ea7-133">Call detail recording (CDR) in Lync Server 2013</span></span>](lync-server-2013-call-detail-recording-cdr.md)  
  

<span data-ttu-id="77ea7-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="77ea7-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

