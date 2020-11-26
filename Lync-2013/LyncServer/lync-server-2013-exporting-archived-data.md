---
title: 'Lync Server 2013: экспорт архивных данных'
description: 'Lync Server 2013: экспорт архивных данных.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting archived data
ms:assetid: 09450d54-769b-4741-924b-e390664d506f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204657(v=OCS.15)
ms:contentKeyID: 48183347
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 656751f1a2d03b50f0c938a8501ba3e95e304cff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428337"
---
# <a name="exporting-archived-data-from-lync-server-2013"></a><span data-ttu-id="ae474-103">Экспорт архивных данных из Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae474-103">Exporting archived data from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae474-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae474-104">

<span> </span></span></span>

<span data-ttu-id="ae474-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ae474-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ae474-106">Данные, заархивированные в архивных базах данных, не доступны для поиска или чтения, но можно использовать командлет Export-CsArchivingData для извлечения записей из базы данных и их сохранения в виде файла EML (Outlook Electronic Mail).</span><span class="sxs-lookup"><span data-stu-id="ae474-106">Data archived in Archiving databases is not searchable or in a readable format, but you can use the Export-CsArchivingData cmdlet to extract records from the database and save them as an Outlook Electronic Mail (EML) file.</span></span> <span data-ttu-id="ae474-107">Подробнее об экспорте архивных данных можно найти в разделе [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="ae474-107">For details about exporting archived data, see [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) in the Operations documentation.</span></span>

<span data-ttu-id="ae474-108">При включении интеграции с Microsoft Exchange данные архивируются в хранилищах Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ae474-108">If you enable Microsoft Exchange integration, data is archived in Exchange 2013 stores.</span></span> <span data-ttu-id="ae474-109">Данные, сохраненные в Exchange 2013, можно найти и обнаруживаемые.</span><span class="sxs-lookup"><span data-stu-id="ae474-109">Data archived in Exchange 2013 is searchable and discoverable.</span></span> <span data-ttu-id="ae474-110">Дополнительные сведения о поддержке интегрированной связи для Exchange 2013 и Lync Server 2013 можно найти в разделе Документация по поддержке [Exchange Server и интеграции с SharePoint в Lync server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) .</span><span class="sxs-lookup"><span data-stu-id="ae474-110">For details about support for integrated communications for Exchange 2013 and Lync Server 2013, see [Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="ae474-111">Подробные сведения о доступе к данным, архивированным в Exchange, можно найти в документации по Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ae474-111">For details about accessing data that is archived in Exchange, see the Exchange 2013 documentation.</span></span>

<div>

## <a name="exporting-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ae474-112">Экспорт данных архивации с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae474-112">Exporting Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ae474-113">Данные для архивации можно экспортировать с помощью командлета Export-CSArchivingData.</span><span class="sxs-lookup"><span data-stu-id="ae474-113">Archiving data can be exported by using the Export-CSArchivingData cmdlet.</span></span> <span data-ttu-id="ae474-114">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae474-114">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ae474-115">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ae474-115">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<span data-ttu-id="ae474-116">**Экспорт данных архивации**</span><span class="sxs-lookup"><span data-stu-id="ae474-116">**To export archiving data**</span></span>

  - <span data-ttu-id="ae474-117">Эта команда экспортирует все данные архивации, внесенные в базу данных архивации atl-sql-001.litwareinc.com с 1 июня 2012 г.</span><span class="sxs-lookup"><span data-stu-id="ae474-117">This command exports all the archiving data written to the archiving database atl-sql-001.litwareinc.com since June 1, 2012.</span></span> <span data-ttu-id="ae474-118">Получившийся выходной файл будет храниться в папке C: \\ ArchivingExports.</span><span class="sxs-lookup"><span data-stu-id="ae474-118">The resulting output file will be stored in the folder C:\\ArchivingExports.</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports"

<span data-ttu-id="ae474-119">**Экспорт данных архивации для одного пользователя**</span><span class="sxs-lookup"><span data-stu-id="ae474-119">**To export archiving data for a single user**</span></span>

  - <span data-ttu-id="ae474-120">Следующая команда экспортирует данные архивации для одного пользователя: kenmyer@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="ae474-120">The following command exports archiving data for a single user: kenmyer@litwareinc.com.</span></span> <span data-ttu-id="ae474-121">Для этого задается параметр UserUri, после которого указывается SIP-адрес пользователя.</span><span class="sxs-lookup"><span data-stu-id="ae474-121">This is done by including the UserUri parameter followed by the user’s SIP address.</span></span> <span data-ttu-id="ae474-122">Пример:</span><span class="sxs-lookup"><span data-stu-id="ae474-122">For example:</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports" -UserUri "sip:kenmyer@litwareinc.com"

<span data-ttu-id="ae474-123">Дополнительные сведения можно найти в разделе справки по командлету [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) .</span><span class="sxs-lookup"><span data-stu-id="ae474-123">For more information, see the help topic for the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ae474-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ae474-124">See Also</span></span>


[<span data-ttu-id="ae474-125">Поддержка интеграции Exchange Server и SharePoint в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae474-125">Exchange Server and SharePoint integration support in Lync Server 2013</span></span>](lync-server-2013-exchange-and-sharepoint-integration-support.md)  


[<span data-ttu-id="ae474-126">Export-CsArchivingData</span><span class="sxs-lookup"><span data-stu-id="ae474-126">Export-CsArchivingData</span></span>](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)  
[<span data-ttu-id="ae474-127">Управление архивированием Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae474-127">Managing Lync Server 2013 Archiving</span></span>](lync-server-2013-managing-archiving.md)  
  

<span data-ttu-id="ae474-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae474-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

