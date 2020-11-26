---
title: 'Lync Server 2013: Просмотр и анализ отчетов сервера мониторинга'
description: 'Lync Server 2013: Просмотр и анализ отчетов сервера мониторинга.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing and analyzing monitoring server reports
ms:assetid: 4dd448f1-01d2-49b2-b109-0728f36566b7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720332(v=OCS.15)
ms:contentKeyID: 63969599
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f2a1812d76a49d487bea35acae3e22ea403f105
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444009"
---
# <a name="viewing-and-analyzing-monitoring-server-reports-in-lync-server-2013"></a><span data-ttu-id="3249e-103">Просмотр и анализ отчетов сервера мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3249e-103">Viewing and analyzing monitoring server reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3249e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3249e-104">

<span> </span></span></span>

<span data-ttu-id="3249e-105">_**Тема последнего изменения:** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="3249e-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="3249e-106">Мониторинг серверных отчетов предоставляет несколько разных показателей качества голоса для наблюдения за QoE, которые доставляются конечным пользователям.</span><span class="sxs-lookup"><span data-stu-id="3249e-106">Monitoring Server reports provides several different measures of voice quality to monitor the QoE that is being delivered to end-users.</span></span> <span data-ttu-id="3249e-107">Кроме того, сервер мониторинга включает несколько встроенных отчетов, которые ваша организация может использовать для отслеживания использования и тенденций качества мультимедиа в сети организации, а также для устранения проблем с качеством мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3249e-107">Additionally, Monitoring Server includes several built-in reports that your organization can use to watch usage and media quality trends on your organization's network and troubleshoot media quality issues that arise.</span></span>

<span data-ttu-id="3249e-108">Основная часть хранения серверных отчетов, представляющих собой ежедневные и еженедельные операции, — просмотр и анализ отчетов о качестве мультимедиа в частности:</span><span class="sxs-lookup"><span data-stu-id="3249e-108">A primary part of keeping Monitoring Server Reports interesting for daily and weekly operations is viewing and analyzing Media Quality Reports, in particular:</span></span>

  - <span data-ttu-id="3249e-109">QoE/отчеты о тенденциях</span><span class="sxs-lookup"><span data-stu-id="3249e-109">QoE Summary/Trend Reports</span></span>

  - <span data-ttu-id="3249e-110">Отчеты о производительности QoE</span><span class="sxs-lookup"><span data-stu-id="3249e-110">QoE Performance Reports</span></span>

<div>

## <a name="view-reports-from-the-monitoring-server"></a><span data-ttu-id="3249e-111">Просмотр отчетов на сервере мониторинга</span><span class="sxs-lookup"><span data-stu-id="3249e-111">View reports from the monitoring server</span></span>

1.  <span data-ttu-id="3249e-112">В веб-браузере найдите серверы, на которых размещены службы отчетов SQL.</span><span class="sxs-lookup"><span data-stu-id="3249e-112">From a web browser, locate your servers hosting the SQL reporting services.</span></span>

2.  <span data-ttu-id="3249e-113">Просмотрите необходимые отчеты в окне браузера.</span><span class="sxs-lookup"><span data-stu-id="3249e-113">View the required reports from the browser screen.</span></span>

3.  <span data-ttu-id="3249e-114">Необязательно Экспортируйте отчет, выбрав параметр Экспорт и требуемый выходной формат.</span><span class="sxs-lookup"><span data-stu-id="3249e-114">(Optional) Export a report by selecting the export option and the required output format.</span></span>

</div>

<div>

## <a name="configure-call-detail-recording-cdr"></a><span data-ttu-id="3249e-115">Настройка записи сведений о звонке (CDR)</span><span class="sxs-lookup"><span data-stu-id="3249e-115">Configure call detail recording (CDR)</span></span>

1.  <span data-ttu-id="3249e-116">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные разрешения) либо назначьте роль CsServerAdministrator или CsAdministrator, войдя на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3249e-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent permissions), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="3249e-117">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3249e-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="3249e-118">В левой панели навигации щелкните **Мониторинг и архивирование**, а затем — **Регистрация вызовов**.</span><span class="sxs-lookup"><span data-stu-id="3249e-118">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="3249e-119">На странице **Регистрация вызовов** в таблице щелкните необходимый сайт, щелкните **Правка**, а затем — **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="3249e-119">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="3249e-120">Чтобы включить очистку, установите флажок **включить очистку для серверов мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="3249e-120">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="3249e-121">В разделе **хранить подробные сведения о вызове (в днях)** выберите максимальное количество дней, в течение которых следует хранить записи с подробными сведениями о звонке.</span><span class="sxs-lookup"><span data-stu-id="3249e-121">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="3249e-122">В параметре **Хранить сведения отчетов об ошибках максимум в течение (дней):** выберите максимальное число дней, в течение которых должны храниться данные отчетов об ошибках.</span><span class="sxs-lookup"><span data-stu-id="3249e-122">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="3249e-123">Щелкните **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="3249e-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="configure-qoe"></a><span data-ttu-id="3249e-124">Настройка QoE</span><span class="sxs-lookup"><span data-stu-id="3249e-124">Configure QoE</span></span>

1.  <span data-ttu-id="3249e-125">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3249e-125">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="3249e-126">Дополнительные сведения см. в разделе Delegate Setup Permissions.</span><span class="sxs-lookup"><span data-stu-id="3249e-126">For details, see Delegate Setup Permissions.</span></span>

2.  <span data-ttu-id="3249e-127">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3249e-127">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="3249e-128">На панели навигации слева нажмите **Мониторинг и архивация**, затем выберите **Данные о качестве взаимодействия**.</span><span class="sxs-lookup"><span data-stu-id="3249e-128">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="3249e-129">На странице **Данные о качестве взаимодействия** выберите требуемый сайт в таблице, нажмите **Изменить** и выберите **Показать сведения**.</span><span class="sxs-lookup"><span data-stu-id="3249e-129">On the **Quality of Experience Data** page, click the appropriate site from the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="3249e-130">Чтобы включить очистку, установите флажок **включить очистку для серверов мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="3249e-130">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="3249e-131">В разделе **хранить сведения о звонке для максимальной длительности (дни):** выберите максимальное количество дней, в течение которых QoE данные должны оставаться на удержании.</span><span class="sxs-lookup"><span data-stu-id="3249e-131">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that QoE data should be retained.</span></span>

7.  <span data-ttu-id="3249e-132">Нажмите Исполнить.</span><span class="sxs-lookup"><span data-stu-id="3249e-132">Click Commit.</span></span>

</div>

<div>

## <a name="change-the-archiving-policy"></a><span data-ttu-id="3249e-133">Изменение политики архивации</span><span class="sxs-lookup"><span data-stu-id="3249e-133">Change the archiving policy</span></span>

1.  <span data-ttu-id="3249e-134">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3249e-134">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3249e-135">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3249e-135">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="3249e-136">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Политика архивации**.</span><span class="sxs-lookup"><span data-stu-id="3249e-136">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="3249e-137">Нажмите пункт **Глобальная** в списке политик, выберите **Изменить**, затем **Показать сведения**.</span><span class="sxs-lookup"><span data-stu-id="3249e-137">Click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="3249e-138">На странице **Изменить политику архивации — глобальная** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3249e-138">In **Edit Archiving Policy - Global**, do the following:</span></span>

6.  <span data-ttu-id="3249e-139">Чтобы включить или отключить внутреннее архивирование для развертывания, установите или снимите флажок **Архивировать внутреннюю связь** .</span><span class="sxs-lookup"><span data-stu-id="3249e-139">To enable or disable internal archiving for the deployment, select or clear the **Archive internal communications** check box.</span></span>

7.  <span data-ttu-id="3249e-140">Чтобы включить или отключить внешнее архивирование для развертывания, установите или снимите флажок **Архивировать внешние связи** .</span><span class="sxs-lookup"><span data-stu-id="3249e-140">To enable or disable external archiving for the deployment, select or clear the **Archive external communications** check box.</span></span>

8.  <span data-ttu-id="3249e-141">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="3249e-141">Click **Commit**.</span></span>

</div>

<div>

## <a name="apply-an-archiving-policy-to-a-user"></a><span data-ttu-id="3249e-142">Применение к пользователю политики архивации</span><span class="sxs-lookup"><span data-stu-id="3249e-142">Apply an archiving policy to a user</span></span>

1.  <span data-ttu-id="3249e-143">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3249e-143">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3249e-144">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3249e-144">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="3249e-145">В левой панели навигации нажмите **Пользователи** и выполните поиск учетной записи, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="3249e-145">In the left navigation bar, click **Users**, and then search on the user account that you want to configure.</span></span>

4.  <span data-ttu-id="3249e-146">В таблице с результатами поиска выберите нужную учетную запись, нажмите кнопку **Изменить** и выберите пункт **Показать сведения**.</span><span class="sxs-lookup"><span data-stu-id="3249e-146">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="3249e-147">В диалоговом окне **изменение пользователя Lync Server** в разделе **Политика архивации** выберите политику архивации пользователей, которую вы хотите применить.</span><span class="sxs-lookup"><span data-stu-id="3249e-147">In **Edit Lync Server User** under **Archiving policy**, select the archiving user policy that you want to apply.</span></span>

6.  <span data-ttu-id="3249e-148">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="3249e-148">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3249e-149">См. также</span><span class="sxs-lookup"><span data-stu-id="3249e-149">See Also</span></span>


[<span data-ttu-id="3249e-150">Использование отчетов мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3249e-150">Using Monitoring Reports in Lync Server 2013</span></span>](lync-server-2013-using-monitoring-reports.md)  
[<span data-ttu-id="3249e-151">Отчет о производительности сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3249e-151">Server Performance Report in Lync Server 2013</span></span>](lync-server-2013-server-performance-report.md)  
[<span data-ttu-id="3249e-152">Отчет о сравнении качества мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3249e-152">Media Quality Comparison Report in Lync Server 2013</span></span>](lync-server-2013-media-quality-comparison-report.md)  
  

<span data-ttu-id="3249e-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3249e-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

