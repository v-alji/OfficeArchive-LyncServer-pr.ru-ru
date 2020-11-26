---
title: 'Lync Server 2013: использование расширенного ведения журнала для искусственных транзакций'
description: 'Lync Server 2013: использование расширенного ведения журнала для искусственных транзакций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using rich logging for synthetic transactions
ms:assetid: 32714a71-9f42-4d5b-a508-e176d8f08bbf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204798(v=OCS.15)
ms:contentKeyID: 48183812
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5fd984386985bced64265ebedfd57c56a84a4443
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440754"
---
# <a name="using-rich-logging-for-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="41f2e-103">Использование расширенного ведения журнала для виртуальных транзакций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41f2e-103">Using rich logging for synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41f2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41f2e-104">

<span> </span></span></span>

<span data-ttu-id="41f2e-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="41f2e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="41f2e-106">Синтетические транзакции (введенные в Microsoft Lync Server 2010) предоставляют администраторам способ проверки того, что пользователи могут успешно выполнять типичные задачи, такие как вход в систему, Обмен мгновенными сообщениями и звонки на телефоны, находящиеся в коммутируемой телефонной сети с открытым коммутируемым подключением (КТСОП).</span><span class="sxs-lookup"><span data-stu-id="41f2e-106">Synthetic transactions (introduced in Microsoft Lync Server 2010) provide a way for administrators to verify that users are able to successfully complete common tasks such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="41f2e-107">Эти тесты (которые упаковываются в набор командлетов Windows PowerShell для Lync Server) могут быть проведены вручную администратором или автоматически запускаться приложением, таким как System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="41f2e-107">These tests (which are packaged as a set of Lync Server Windows PowerShell cmdlets) can be conducted manually by an administrator, or they can be automatically run by an application such as System Center Operations Manager.</span></span>

<span data-ttu-id="41f2e-108">В Lync Server 2010 искусственные транзакции доносятся чрезвычайно полезными для облегчения администраторам выявления проблем системы.</span><span class="sxs-lookup"><span data-stu-id="41f2e-108">In Lync Server 2010, synthetic transactions proved extremely useful in helping administrators to identify problems with the system.</span></span> <span data-ttu-id="41f2e-109">Например, командлет **Test-CsRegistration** может оповещать администраторов о том, что некоторые пользователи столкнулись с проблемами при регистрации в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="41f2e-109">For example, the **Test-CsRegistration** cmdlet could alert administrators to the fact that some users were having difficulty registering with Lync Server.</span></span> <span data-ttu-id="41f2e-110">Тем не менее, эти искусственные транзакции не помогают администраторам определить, почему пользователи столкнулись с проблемами при регистрации в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="41f2e-110">However, the synthetic transactions were somewhat less useful in helping administrators determine why these users were having difficulty registering with Lync Server.</span></span> <span data-ttu-id="41f2e-111">Это произошло из-за того, что искусственные транзакции не предоставили подробные сведения для ведения журнала, которые могут помочь администраторам устранить проблемы с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="41f2e-111">This was due to the fact that the synthetic transactions did not provide detailed logging information that could help administrators troubleshoot problems with Lync Server.</span></span> <span data-ttu-id="41f2e-112">Лучше всего получить подробный вывод из искусственной транзакции с пошаговыми инструкциями, которые могут позволить администратору создать обоснованное предположение, в котором может возникнуть проблема.</span><span class="sxs-lookup"><span data-stu-id="41f2e-112">At best, the verbose output from a synthetic transaction provided step-by-step information that might enable an administrator to make an educated guess as to where a problem likely occurred.</span></span>

<span data-ttu-id="41f2e-113">В Microsoft Lync Server 2013 искусственные транзакции, созданные с богатым протоколированием, сконструированы заново.</span><span class="sxs-lookup"><span data-stu-id="41f2e-113">In Microsoft Lync Server 2013, synthetic transactions have been re-architected to provide rich logging.</span></span> <span data-ttu-id="41f2e-114">"Ведение подробного протоколирования" означает, что для каждого действия, которое занимает виртуальная транзакция, такие данные будут записаны следующим образом:</span><span class="sxs-lookup"><span data-stu-id="41f2e-114">"Rich logging" means that, for each activity that a synthetic transaction undertakes, information such as this will be recorded:</span></span>

  - <span data-ttu-id="41f2e-115">Время начала действия</span><span class="sxs-lookup"><span data-stu-id="41f2e-115">The time that the activity started</span></span>

  - <span data-ttu-id="41f2e-116">Время завершения действия</span><span class="sxs-lookup"><span data-stu-id="41f2e-116">The time that the activity finished</span></span>

  - <span data-ttu-id="41f2e-117">Выполняемое действие (например, создание, присоединение или выход из конференции; вход на сервер Lync Server; Отправка мгновенного сообщения и т. д.)</span><span class="sxs-lookup"><span data-stu-id="41f2e-117">The action that was performed (for example, creating, joining, or leaving a conference; signing on to Lync Server; sending an instant message; and so on)</span></span>

  - <span data-ttu-id="41f2e-118">Информационные, подробные сообщения, предупреждения или сообщения об ошибках, которые были созданы при выполнении операции</span><span class="sxs-lookup"><span data-stu-id="41f2e-118">Informational, verbose, warning, or error messages generated when the activity ran</span></span>

  - <span data-ttu-id="41f2e-119">Сообщения регистрации SIP</span><span class="sxs-lookup"><span data-stu-id="41f2e-119">SIP registration messages</span></span>

  - <span data-ttu-id="41f2e-120">Записи исключений или коды диагностики, созданные при выполнении действия</span><span class="sxs-lookup"><span data-stu-id="41f2e-120">Exception records or diagnostic codes generated when the activity ran</span></span>

  - <span data-ttu-id="41f2e-121">Итоговый результат выполнения действия</span><span class="sxs-lookup"><span data-stu-id="41f2e-121">The net result of running the activity</span></span>

<span data-ttu-id="41f2e-122">Эта информация создается автоматически каждый раз при выполнении искусственной транзакции.</span><span class="sxs-lookup"><span data-stu-id="41f2e-122">This information is automatically generated each time a synthetic transaction is run.</span></span> <span data-ttu-id="41f2e-123">Однако эти сведения не отображаются и не сохраняются в файле журнала автоматически.</span><span class="sxs-lookup"><span data-stu-id="41f2e-123">However, the information is not automatically displayed or saved to a log file.</span></span> <span data-ttu-id="41f2e-124">Вместо этого администраторы, которые вручную загружают искусственную транзакцию, могут использовать параметр OutLoggerVariable для указания переменной Windows PowerShell, в которой будут храниться данные.</span><span class="sxs-lookup"><span data-stu-id="41f2e-124">Instead, administrators who are manually running a synthetic transaction can use the OutLoggerVariable parameter to specify a Windows PowerShell variable in which the information will be stored.</span></span> <span data-ttu-id="41f2e-125">После этого администраторы могут использовать пару методов, которые позволяют им сохранять и (или) просматривать расширенный журнал в формате XML или HTML.</span><span class="sxs-lookup"><span data-stu-id="41f2e-125">From there, administrators can then use a pair of methods that enable them to save and/or view the rich log in either XML or HTML format.</span></span>

<span data-ttu-id="41f2e-126">Например, для Lync Server 2010 администраторы могут выполнить командлет **Test-CsRegistration** , выполнив команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="41f2e-126">For example, Lync Server 2010 administrators might run the **Test-CsRegistration** cmdlet by using a command similar to the following:</span></span>

    Test-CsRegistration -TargetFqdn atl-cs-001.litwareinc.com

<span data-ttu-id="41f2e-127">Администраторы могут включить параметр OutLoggerVariable, за которым следует имя переменной, выбирая указанные ниже значения.</span><span class="sxs-lookup"><span data-stu-id="41f2e-127">Administrators have the option of including the OutLoggerVariable parameter followed by a variable name of their choosing:</span></span>

    Test-CsRegistration -TargetFqdn atl-cs-001.litwareinc.com -OutLoggerVariable RegistrationTest

> [!NOTE]  
> <span data-ttu-id="41f2e-128">Не дополняйте перед именем переменной символа $.</span><span class="sxs-lookup"><span data-stu-id="41f2e-128">Do not preface the variable name with the $ character.</span></span> <span data-ttu-id="41f2e-129">Используйте имя переменной, например RegistrationTest, а не $RegistrationTest.</span><span class="sxs-lookup"><span data-stu-id="41f2e-129">Use a variable name like RegistrationTest and not $RegistrationTest.</span></span>

<span data-ttu-id="41f2e-130">Предыдущая команда выводит содержимое, подобное следующему:</span><span class="sxs-lookup"><span data-stu-id="41f2e-130">The preceding command outputs content similar to the following:</span></span>

    Target Fqdn   : atl-cs-001.litwareinc.com
    Result        : Failure
    Latency       : 00:00:00
    Error Message : This machine does not have any assigned certificates.
    Diagnosis     :

<span data-ttu-id="41f2e-131">Тем не менее, в этой ошибке есть больше подробных сведений, чем просто сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="41f2e-131">However, much more detailed information is available for this failure than just the error message shown above.</span></span> <span data-ttu-id="41f2e-132">Чтобы получить доступ к этим сведениям в формате HTML, используйте следующую команду для сохранения данных, сохраненных в переменной RegistrationTest, в HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="41f2e-132">To access that information in HTML format, use a command similar to this in order to save the information stored in the variable RegistrationTest to an HTML file:</span></span>

    $RegistrationTest.ToHTML() | Out-File C:\Logs\Registration.html

<span data-ttu-id="41f2e-133">Можно также использовать метод ToXML() для сохранения данных в файл XML:</span><span class="sxs-lookup"><span data-stu-id="41f2e-133">Alternatively, you can use the ToXML() method to save the data to an XML file:</span></span>

    $RegistrationTest.ToXML() | Out-File C:\Logs\Registration.xml

<span data-ttu-id="41f2e-134">Эти файлы можно будет просматривать с помощью Internet Explorer, Visual Studio или других приложений, которые могут открывать HTML-и XML-файлы.</span><span class="sxs-lookup"><span data-stu-id="41f2e-134">These files can then be viewed using Internet Explorer, Visual Studio, or any other application capable of opening HTML/XML files.</span></span>

<span data-ttu-id="41f2e-135">Синтетические транзакции, выполненные из системы System Center Operations Manager, будут автоматически создавать эти файлы журнала для сбоев.</span><span class="sxs-lookup"><span data-stu-id="41f2e-135">Synthetic transactions run from inside of System Center Operations Manager will automatically generate these log files for failures.</span></span> <span data-ttu-id="41f2e-136">Однако эти журналы не будут создаваться, если выполнение завершается сбоем до того, как Windows PowerShell сможет загрузить и выполнить виртуальную транзакцию.</span><span class="sxs-lookup"><span data-stu-id="41f2e-136">However, these logs will not be generated if the execution fails before Windows PowerShell is able to load and run the synthetic transaction.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="41f2e-137">По умолчанию Lync Server 2013 сохраняет файлы журнала в папке, к которой не предоставлен общий доступ.</span><span class="sxs-lookup"><span data-stu-id="41f2e-137">By default, Lync Server 2013 saves log files to a folder that is not shared.</span></span> <span data-ttu-id="41f2e-138">Чтобы сделать эти журналы общедоступными, нужно поделиться этой папкой (например, \\ \\ ATL-наблюдатель-001. плана litwareinc. com\WatcherNode.</span><span class="sxs-lookup"><span data-stu-id="41f2e-138">To make these logs readily accessible, you should share this folder (for example, \\\\atl-watcher-001.litwareinc.com\WatcherNode.</span></span>


</div>

</div>

</div>

</div>

