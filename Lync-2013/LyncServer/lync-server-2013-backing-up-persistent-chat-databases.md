---
title: 'Lync Server 2013: резервное копирование сохраненных баз данных чата'
description: 'Lync Server 2013: резервное копирование сохраненных баз данных чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Persistent Chat databases
ms:assetid: b99ebdc0-a025-44d7-9d74-37a7365f330d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945646(v=OCS.15)
ms:contentKeyID: 51541507
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9885eaf0065f5b558922c056fb1f669a5b821460
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438024"
---
# <a name="backing-up-persistent-chat-databases-in-lync-server-2013"></a><span data-ttu-id="f2f06-103">Резервное копирование сохраненных баз данных чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2f06-103">Backing up Persistent Chat databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2f06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2f06-104">

<span> </span></span></span>

<span data-ttu-id="f2f06-105">_**Тема последнего изменения:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="f2f06-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="f2f06-106">Сохраняемый контент комнаты чата хранится в базе данных сохраняемого чата (MGC. mdf).</span><span class="sxs-lookup"><span data-stu-id="f2f06-106">Persistent Chat room content is stored in the Persistent Chat database (Mgc.mdf).</span></span> <span data-ttu-id="f2f06-107">Необходимо регулярно создавать резервные копии этих критически важных для бизнеса данных.</span><span class="sxs-lookup"><span data-stu-id="f2f06-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="f2f06-108">В дополнение к содержимому комнаты чата, в ней также хранятся сведения об участниках (например, пользователи и группы пользователей), ролях и доступе, которым они необходимы для общения с комнатой и комнатой чата.</span><span class="sxs-lookup"><span data-stu-id="f2f06-108">In addition to the chat room content, the Persistent Chat database also stores information about the principals (such as users and user groups), and the roles and access that they have to chat rooms and chat room.</span></span>

<span data-ttu-id="f2f06-109">Существует два способа резервного копирования данных сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="f2f06-109">There are two ways of backing up Persistent Chat data.</span></span>

  - <span data-ttu-id="f2f06-110">Резервное копирование SQL Server</span><span class="sxs-lookup"><span data-stu-id="f2f06-110">SQL Server Backup</span></span>

  - <span data-ttu-id="f2f06-111">`Export-CsPersistentChatData`Командлет, который экспортирует сохраняемые данные чата в виде файла</span><span class="sxs-lookup"><span data-stu-id="f2f06-111">The `Export-CsPersistentChatData` cmdlet, which exports Persistent Chat data as a file</span></span>

<span data-ttu-id="f2f06-112">Для данных, созданных с помощью резервной копии SQL Server, требуется значительно больше места на диске (возможно, 20 больше), чем создано `Export-CsPersistentChatData` , но в резервной копии SQL Server более вероятна процедура, с помощью которой администраторы знакомы.</span><span class="sxs-lookup"><span data-stu-id="f2f06-112">Data that is created by using SQL Server backup requires significantly more disk space—possibly 20 times more—than that created by `Export-CsPersistentChatData`, but SQL Server backup is more likely to be a procedure that administrators are familiar with.</span></span>

<span data-ttu-id="f2f06-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2f06-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

