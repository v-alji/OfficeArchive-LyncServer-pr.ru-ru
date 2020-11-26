---
title: Перенос существующих собраний и содержимого собраний
description: Перенос существующих собраний и содержимого собраний.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443806"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a><span data-ttu-id="60651-103">Перенос существующих собраний и содержимого собраний</span><span class="sxs-lookup"><span data-stu-id="60651-103">Migrate existing meetings and meeting content</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="60651-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="60651-104">

<span> </span></span></span>

<span data-ttu-id="60651-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="60651-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="60651-106">При перемещении учетной записи пользователя из Lync Server 2010 на сервер Lync Server 2013 переносятся следующие данные с учетной записью пользователя:</span><span class="sxs-lookup"><span data-stu-id="60651-106">When a user account is moved from Lync Server 2010 to a Lync Server 2013 server, the following information is moved with that user account:</span></span>

  - <span data-ttu-id="60651-107">**Собрания, уже запланированные пользователем**.</span><span class="sxs-lookup"><span data-stu-id="60651-107">**Meetings already scheduled by the user**.</span></span> <span data-ttu-id="60651-108">Сюда входит перемещение каталогов конференций и данных конференций.</span><span class="sxs-lookup"><span data-stu-id="60651-108">This includes moving the conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="60651-109">**Персональный идентификационный номер пользователя (ПИН-код)**.</span><span class="sxs-lookup"><span data-stu-id="60651-109">**User’s personal identification number (PIN)**.</span></span> <span data-ttu-id="60651-110">Текущий ПИН-код пользователя продолжает работать, пока не истечет срок действия или пользователь запросит новый ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="60651-110">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="60651-111">Указанные ниже сведения об учетной записи пользователя не перемещаются на новый сервер.</span><span class="sxs-lookup"><span data-stu-id="60651-111">The following user account information does not move to the new server.</span></span>

  - <span data-ttu-id="60651-112">**Содержимое собрания**.</span><span class="sxs-lookup"><span data-stu-id="60651-112">**Meeting content**.</span></span> <span data-ttu-id="60651-113">Чтобы переместить содержимое, совместно используемое во время собрания, например PowerPoint, доска, вложения или данные опроса, используйте параметр **-MoveConferenceData** в составе командлета **Move-CsUser** .</span><span class="sxs-lookup"><span data-stu-id="60651-113">In order to move the content shared during a meeting, for example PowerPoint, Whiteboard, attachments or poll data, use the **-MoveConferenceData** parameter as part of the **Move-CsUser** cmdlet.</span></span>

<span data-ttu-id="60651-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="60651-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

