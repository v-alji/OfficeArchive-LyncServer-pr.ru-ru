---
title: Командлеты отчетности в Skype для бизнеса Online и веб-служба RESTFUL
description: Командлеты отчетности в Skype для бизнеса Online и веб-служба RESTFUL.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: The Skype for Business Online reporting cmdlets and REST web service
ms:assetid: cadd73a7-c08a-4102-b73a-ccb3ad4987bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362845(v=OCS.15)
ms:contentKeyID: 56563409
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2160e0910d42f811ec8b03fa50450d5f73c59b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423409"
---
# <a name="the-skype-for-business-online-reporting-cmdlets-and-rest-web-service"></a><span data-ttu-id="6208e-103">Командлеты отчетности в Skype для бизнеса Online и веб-служба RESTFUL</span><span class="sxs-lookup"><span data-stu-id="6208e-103">The Skype for Business Online reporting cmdlets and REST web service</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6208e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6208e-104">

<span> </span></span></span>

<span data-ttu-id="6208e-105">_**Тема последнего изменения:** 2014-09-05_</span><span class="sxs-lookup"><span data-stu-id="6208e-105">_**Topic Last Modified:** 2014-09-05_</span></span>

<span data-ttu-id="6208e-106">В сочетании с функциями отчетов Skype для бизнеса Online предоставляет доступ к пяти командлетам Windows PowerShell, которые помогают создавать эти отчеты, и они также могут использоваться администраторами, чтобы возвращать настраиваемые данные отчетов.</span><span class="sxs-lookup"><span data-stu-id="6208e-106">In conjunction with the reporting features, Skype for Business Online provides access to five Windows PowerShell cmdlets that help generate those reports and are also can be used by administrators to return customized reporting data.</span></span> <span data-ttu-id="6208e-107">Skype для бизнеса Online также включает в себя (функцию пересылки состояния представления), которая может быть использована разработчиками для получения персональных данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="6208e-107">Skype for Business Online also includes the REST (Representational State Transfer), which can be used by developers to retrieve customized reporting information.</span></span>

<span data-ttu-id="6208e-108">Ниже перечислены командлеты отчетов, доступные для администраторов.</span><span class="sxs-lookup"><span data-stu-id="6208e-108">The reporting cmdlets available to administrators include:</span></span>

  - <span data-ttu-id="6208e-109">Get-CsActiveUserReport, который предоставляет сведения о количестве активных пользователей (пользователей, которые вошли в Skype для бизнеса Online и участвовали хотя бы в одной конференции или одноранговом сеансе связи).</span><span class="sxs-lookup"><span data-stu-id="6208e-109">Get-CsActiveUserReport, which provides information about the number of active users (that is, users who have logged on to Skype for Business Online and participated in at least one conference or peer-to-peer communication session).</span></span>

  - <span data-ttu-id="6208e-110">Get-CsAVConferenceTimeReport, который предоставляет сведения о течение времени (в минутах) пользователей, затраченных на аудио-и видеоконференции.</span><span class="sxs-lookup"><span data-stu-id="6208e-110">Get-CsAVConferenceTimeReport, which provides information about the amount of time (in minutes) users spent in audio/video conferences.</span></span>

  - <span data-ttu-id="6208e-111">Get-CsConferenceReport, который предоставляет сведения о количестве и типах конференций, в которых участвовали пользователи.</span><span class="sxs-lookup"><span data-stu-id="6208e-111">Get-CsConferenceReport, which provides information about the number and type of conferences that users participated in.</span></span>

  - <span data-ttu-id="6208e-112">Get-CsP2PAVTimeReport, который предоставляет сведения о течение времени (в минутах) пользователей, затраченных на одноранговые сеансы, которые включают звук и/или видео.</span><span class="sxs-lookup"><span data-stu-id="6208e-112">Get-CsP2PAVTimeReport, which provides information about the amount of time (in minutes) users spent in peer-to-peer sessions that included audio and/or video.</span></span>

  - <span data-ttu-id="6208e-113">Get-CsP2PSessionReport, который предоставляет сведения о количестве и типе одноранговых сеансов, в которых участвовали пользователи.</span><span class="sxs-lookup"><span data-stu-id="6208e-113">Get-CsP2PSessionReport, which provides information about the number and type of peer-to-peer sessions that users participated in.</span></span>

<span data-ttu-id="6208e-114">Большинство администраторов будут использовать отчеты, доступные в центре администрирования Microsoft 365: не только те, которые автоматически генерируются, но и предоставляют графическое представление данных, которые часто проще интерпретировать, чем необработанные значения, возвращаемые командлетами для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="6208e-114">Most administrators will use the reports available in the Microsoft 365 admin center: not only are those reports auto-generated, but they also provide a graphical representation of the data that is often easier to interpret than the raw number values returned by the reporting cmdlets.</span></span> <span data-ttu-id="6208e-115">Однако администраторы, знакомые с Windows PowerShell, могут использовать командлеты отчетов, чтобы возвращать данные, которые не будут доступны в отчетах Lync Online.</span><span class="sxs-lookup"><span data-stu-id="6208e-115">However, administrators familiar with Windows PowerShell can use the reporting cmdlets to return data that is not readily available from the Lync Online reports.</span></span> <span data-ttu-id="6208e-116">Например, командлеты для работы с отчетами возвращают сведения о длительности сеанса (в минутах), в течение которых lasted сеанса.</span><span class="sxs-lookup"><span data-stu-id="6208e-116">For example, the reporting cmdlets return information about session duration (the amount of time, in minutes, that each session lasted).</span></span> <span data-ttu-id="6208e-117">Некоторые длительности сеанса недоступны в отчетах Lync Online.</span><span class="sxs-lookup"><span data-stu-id="6208e-117">Individual session durations are not available using the Lync Online reports.</span></span> <span data-ttu-id="6208e-118">Аналогичным образом, в представлении ежедневно в отчете Lync Online отображаются данные только за предшествующие 14 дней.</span><span class="sxs-lookup"><span data-stu-id="6208e-118">Likewise, in daily view the Lync Online reports display information only for the preceding 14 days.</span></span> <span data-ttu-id="6208e-119">Если вы хотите просмотреть ежедневные итоги за другой день (например, дату за четыре месяца назад), вы можете использовать командлеты для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="6208e-119">If you would like to review the daily totals for a different day (for example, a date from four months ago) you can do so by using the reporting cmdlets.</span></span>

<span data-ttu-id="6208e-120">Администраторы могут также заинтересовать статью, [используя Excel для получения данных отчетов office 365](https://msdn.microsoft.com/library/dn781442.aspx), в котором объясняется, как использовать функцию запроса данных OData в Microsoft Excel для создания настраиваемого отчета Office 365.</span><span class="sxs-lookup"><span data-stu-id="6208e-120">Administrators might also be interested in the article [Using Excel to Retrieve Office 365 Reporting Data](https://msdn.microsoft.com/library/dn781442.aspx), which explains how to use the OData data querying feature in Microsoft Excel to create custom office 365 report.</span></span> <span data-ttu-id="6208e-121">Пользовательские отчеты позволяют определять, какие данные (и сколько данных) будут возвращаться из службы отчетов Office 365.</span><span class="sxs-lookup"><span data-stu-id="6208e-121">Custom reports give you the ability to dictate which data (and how much data) is returned from the Office 365 reporting service.</span></span> <span data-ttu-id="6208e-122">Пользовательские отчеты также позволяют выполнять такие задачи, как определение порядка сортировки и группировки данных и предоставление доступа к сведениям, которые не отображаются в центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="6208e-122">Custom reports also enable you to do such things as specify how the data should be sorted and grouped, and provide access to information that is not displayed in the admin center.</span></span>

<span data-ttu-id="6208e-123">Администраторы с фоном разработки могут использовать веб-службу RESTFUL для получения сведений, которые не отображаются в центре администрирования Skype для бизнеса Online.</span><span class="sxs-lookup"><span data-stu-id="6208e-123">Administrators with a development background can use the REST web service to obtain information not displayed in the Skype for Business Online admin center.</span></span> <span data-ttu-id="6208e-124">Служба RESTFUL аналогична службе SOAP, так как каждая технология предоставляет способ передачи данных XML между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6208e-124">The REST service is similar to the SOAP service, in that each technology provides a way to transfer XML data between a client and a server.</span></span> <span data-ttu-id="6208e-125">Однако у службы RESTFUL есть по крайней мере два преимущества, чем служба SOAP.</span><span class="sxs-lookup"><span data-stu-id="6208e-125">However, the REST service has at least two advantages over the SOAP service.</span></span> <span data-ttu-id="6208e-126">Для одного из них функции RESTFUL выполняют передачу данных XML, используя стандартизированный формат, известный как формат объединения ATOM.</span><span class="sxs-lookup"><span data-stu-id="6208e-126">For one, REST performs XML data transfers using a standardized format known as the ATOM syndication format.</span></span> <span data-ttu-id="6208e-127">По сравнению с передачей данных протокол SOAP использует нестандартный формат.</span><span class="sxs-lookup"><span data-stu-id="6208e-127">By contrast, SOAP using a non-standard format when transferring data.</span></span> <span data-ttu-id="6208e-128">Кроме того, остальное может передавать данные через сети, которые блокируют HTTP-глаголы, отличные от GET и POST.</span><span class="sxs-lookup"><span data-stu-id="6208e-128">In addition, REST is able to transfer data across networks that block HTTP verbs other than GET and POST.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="6208e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="6208e-129">See Also</span></span>


<span data-ttu-id="6208e-130">[Отчеты Lync Online](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="6208e-130">[Lync Online reporting](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span></span>  


[<span data-ttu-id="6208e-131">Веб-служба отчетов Office 365</span><span class="sxs-lookup"><span data-stu-id="6208e-131">The Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984325.aspx)  
[<span data-ttu-id="6208e-132">Знакомство с веб-службой отчетов Office 365</span><span class="sxs-lookup"><span data-stu-id="6208e-132">Learning About the Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984321.aspx)  
<span data-ttu-id="6208e-133">[Командлеты отчетов Exchange Online](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span><span class="sxs-lookup"><span data-stu-id="6208e-133">[The Exchange Online Reporting Cmdlets](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span></span>  
[<span data-ttu-id="6208e-134">Получение данных отчетов Office 365 с помощью Excel</span><span class="sxs-lookup"><span data-stu-id="6208e-134">Using Excel to Retrieve Office 365 Reporting Data</span></span>](https://msdn.microsoft.com/library/dn781442.aspx)  
  

<span data-ttu-id="6208e-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6208e-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

