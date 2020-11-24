---
title: 'Lync Server 2013: Устранение неполадок с командлетами ролей и служб сервера'
description: 'Lync Server 2013: Устранение неполадок с командлетами ролей и служб сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting server roles and services cmdlets
ms:assetid: 03be4cae-bf35-40b2-8e02-477b64afa4c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415628(v=OCS.15)
ms:contentKeyID: 48183268
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c524ca800445e6b23175ba13621b52c71bc4335f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398713"
---
# <a name="troubleshooting-server-roles-and-services-cmdlets-in-lync-server-2013"></a><span data-ttu-id="38ff8-103">Устранение неполадок с командлетами ролей и служб сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="38ff8-103">Troubleshooting server roles and services cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="38ff8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="38ff8-104">

<span> </span></span></span>

<span data-ttu-id="38ff8-105">_**Тема последнего изменения:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="38ff8-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="38ff8-106">Командлеты по устранению неполадок предоставляют различные способы проверки правильности работы Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="38ff8-106">The troubleshooting cmdlets provide different ways to verify that Microsoft Lync Server 2013 is working as expected.</span></span> <span data-ttu-id="38ff8-107">Например, командлеты CsHealthMonitoringConfiguration позволяют настроить учетные записи для пулов регистраторов и директоров.</span><span class="sxs-lookup"><span data-stu-id="38ff8-107">For example, the CsHealthMonitoringConfiguration cmdlets enable you to set up test accounts for Registrar and Director pools.</span></span> <span data-ttu-id="38ff8-108">В свою очередь, вы можете использовать эти тестовые учетные записи, чтобы убедиться в том, что пользователи могут успешно выполнять типичные задачи, такие как вход в систему, Обмен мгновенными сообщениями и звонки на телефоны, находящиеся в коммутируемой телефонной сети с открытым коммутируемым подключением (КТСОП).</span><span class="sxs-lookup"><span data-stu-id="38ff8-108">In turn, you can then use those test accounts to verify that users are able to successfully complete common tasks such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="38ff8-109">Дополнительные сведения о командлетах можно найти в блоге Lync Server &nbsp; Windows PowerShell по адресу <A href="https://go.microsoft.com/fwlink/p/?linkid=263432">https://go.microsoft.com/fwlink/p/?linkId=263432</A> .</span><span class="sxs-lookup"><span data-stu-id="38ff8-109">For additional information about cmdlets, see the Lync Server&nbsp;Windows PowerShell Blog at <A href="https://go.microsoft.com/fwlink/p/?linkid=263432">https://go.microsoft.com/fwlink/p/?linkId=263432</A>.</span></span> <span data-ttu-id="38ff8-110">Содержимое всех блогов и их URL-адреса могут быть изменены без уведомления.</span><span class="sxs-lookup"><span data-stu-id="38ff8-110">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

<div>

## <a name="server-roles-and-services-cmdlets"></a><span data-ttu-id="38ff8-111">Командлеты служб и ролей сервера</span><span class="sxs-lookup"><span data-stu-id="38ff8-111">Server Roles and Services Cmdlets</span></span>

<span data-ttu-id="38ff8-112">Ниже приведен список командлетов, предназначенных для устранения неполадок, связанных с серверными ролями и службами.</span><span class="sxs-lookup"><span data-stu-id="38ff8-112">The following is a list of cmdlets that relate directly to troubleshooting server roles and services:</span></span>

<span data-ttu-id="38ff8-113">**Устранение неполадок с ролями и службами сервера**</span><span class="sxs-lookup"><span data-stu-id="38ff8-113">**Troubleshooting Server Roles and Services**</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-114">[Get-CsAudioTestServiceApplication](https://technet.microsoft.com/library/Gg412984(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-114">[Get-CsAudioTestServiceApplication](https://technet.microsoft.com/library/Gg412984(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-115">[Set-CsAudioTestServiceApplication](https://technet.microsoft.com/library/Gg398907(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-115">[Set-CsAudioTestServiceApplication](https://technet.microsoft.com/library/Gg398907(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="38ff8-116">[Get-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg398667(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-116">[Get-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg398667(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-117">[New-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg398718(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-117">[New-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg398718(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-118">[Remove-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg425794(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-118">[Remove-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg425794(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-119">[Set-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg425847(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-119">[Set-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg425847(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="38ff8-120">[Get-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg413034(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-120">[Get-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg413034(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-121">[New-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg398733(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-121">[New-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg398733(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-122">[Remove-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg412853(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-122">[Remove-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg412853(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-123">[Set-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg425734(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-123">[Set-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg425734(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="38ff8-124">[New-CsDiagnosticsFilter](https://technet.microsoft.com/library/Gg413009(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-124">[New-CsDiagnosticsFilter](https://technet.microsoft.com/library/Gg413009(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="38ff8-125">[Get-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg412774(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-125">[Get-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg412774(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-126">[New-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg398350(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-126">[New-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg398350(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-127">[Remove-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg398941(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-127">[Remove-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg398941(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="38ff8-128">[Set-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg399045(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="38ff8-128">[Set-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg399045(v=OCS.15))</span></span>

<span data-ttu-id="38ff8-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="38ff8-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

