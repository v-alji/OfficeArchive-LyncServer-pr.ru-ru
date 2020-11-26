---
title: Проверка того, что все объекты контактов Exchange UM удалены из устаревшего пула
description: Убедитесь, что все объекты контакта Exchange UM удалены из устаревшего пула.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440138"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a><span data-ttu-id="0a4a3-103">Проверка того, что все объекты контактов Exchange UM удалены из устаревшего пула</span><span class="sxs-lookup"><span data-stu-id="0a4a3-103">Verify that all Exchange UM Contact objects are removed from the legacy pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a4a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a4a3-104">

<span> </span></span></span>

<span data-ttu-id="0a4a3-105">_**Тема последнего изменения:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="0a4a3-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="0a4a3-106">С помощью средства **OCSUmUtil** или командлета **Get-CsExumContact** убедитесь в том, что объекты контактов Exchange UM были удалены из устаревшего пула Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-106">Use either the **OCSUmUtil** tool or the **Get-CsExumContact** cmdlet to verify that Exchange UM contact objects have been removed from the legacy Office Communications Server 2007 R2 pool.</span></span> <span data-ttu-id="0a4a3-107">**OCSUmUtil** находится в следующей папке:</span><span class="sxs-lookup"><span data-stu-id="0a4a3-107">**OCSUmUtil** is located in the following folder:</span></span>

<span data-ttu-id="0a4a3-108">% Программных файлов% \\ распространенных файлов \\ Lync Server 2013 \\ support \\OcsUMUtil.exe</span><span class="sxs-lookup"><span data-stu-id="0a4a3-108">%Program Files%\\Common Files\\Lync Server 2013\\Support\\OcsUMUtil.exe</span></span>

<span data-ttu-id="0a4a3-109">**OCSUmUtil** необходимо запускать из учетной записи пользователя:</span><span class="sxs-lookup"><span data-stu-id="0a4a3-109">**OCSUmUtil** must be run from a user account that has:</span></span>

  - <span data-ttu-id="0a4a3-110">Членство в группе RTCUniversalServerAdmins и RTCUniversalUserAdmins (которая включает права на чтение параметров единой системы обмена сообщениями Exchange Server)</span><span class="sxs-lookup"><span data-stu-id="0a4a3-110">Membership in the RTCUniversalServerAdmins and RTCUniversalUserAdmins group (which includes rights to read Exchange Server Unified Messaging settings)</span></span>

  - <span data-ttu-id="0a4a3-111">Права домена на создание объектов контакта в указанном контейнере подразделения</span><span class="sxs-lookup"><span data-stu-id="0a4a3-111">Domain rights to create contact objects in the specified organizational unit (OU) container</span></span>

<span data-ttu-id="0a4a3-112">Дополнительные сведения об использовании командлета **Get-CsExumContact** можно найти в документации [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-112">For details about using the **Get-CsExumContact** cmdlet, see [Get-CsExUmContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="0a4a3-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a4a3-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

