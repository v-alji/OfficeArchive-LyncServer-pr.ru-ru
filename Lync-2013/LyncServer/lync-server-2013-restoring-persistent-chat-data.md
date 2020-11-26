---
title: 'Lync Server 2013: восстановление сохраняемых данных чата'
description: 'Lync Server 2013: восстановление сохраняемых данных чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442511"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a><span data-ttu-id="760df-103">Восстановление данных из сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="760df-103">Restoring Persistent Chat data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="760df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="760df-104">

<span> </span></span></span>

<span data-ttu-id="760df-105">_**Тема последнего изменения:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="760df-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="760df-106">Сохраняемый контент комнаты чата хранится в базе данных сохраняемого чата (MGC. mdf).</span><span class="sxs-lookup"><span data-stu-id="760df-106">Persistent Chat room content is stored in the Persistent Chat database (mgc.mdf).</span></span> <span data-ttu-id="760df-107">Необходимо регулярно создавать резервные копии этих критически важных для бизнеса данных.</span><span class="sxs-lookup"><span data-stu-id="760df-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="760df-108">В дополнение к содержимому комнаты чата, участникам (например, пользователям и группам), а также ролям и Access, которые им нужно общаться с комнатами и разговаривать с содержимым комнаты чата, в базе данных сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="760df-108">In addition to the chat room content, principals (such as users and groups) and the roles and access that they have to chat rooms and chat room content, is also stored in the Persistent Chat database.</span></span>

<span data-ttu-id="760df-109">Способ восстановления сохраняемых данных чата зависит от того, какой метод вы использовали для архивации.</span><span class="sxs-lookup"><span data-stu-id="760df-109">How you restore your Persistent Chat data depends on the method that you used to back it up.</span></span>

  - <span data-ttu-id="760df-110">Если были использованы процедуры резервного копирования SQL Server, необходимо использовать процедуры восстановления SQL Server.</span><span class="sxs-lookup"><span data-stu-id="760df-110">If you used SQL Server backup procedures, you must use SQL Server restore procedures.</span></span>

  - <span data-ttu-id="760df-111">Если вы использовали командлет **Export-CsPersistentChatData** для резервного копирования сохраненных данных чата, необходимо использовать командлет **Import-CsPersistentChatData** для восстановления данных.</span><span class="sxs-lookup"><span data-stu-id="760df-111">If you used the **Export-CsPersistentChatData** cmdlet to back up Persistent Chat data, then you must use the **Import-CsPersistentChatData** cmdlet to restore the data.</span></span>

<span data-ttu-id="760df-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="760df-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

