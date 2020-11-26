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
# <a name="backing-up-persistent-chat-databases-in-lync-server-2013"></a>Резервное копирование сохраненных баз данных чата в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-17_

Сохраняемый контент комнаты чата хранится в базе данных сохраняемого чата (MGC. mdf). Необходимо регулярно создавать резервные копии этих критически важных для бизнеса данных. В дополнение к содержимому комнаты чата, в ней также хранятся сведения об участниках (например, пользователи и группы пользователей), ролях и доступе, которым они необходимы для общения с комнатой и комнатой чата.

Существует два способа резервного копирования данных сохраняемого чата.

  - Резервное копирование SQL Server

  - `Export-CsPersistentChatData`Командлет, который экспортирует сохраняемые данные чата в виде файла

Для данных, созданных с помощью резервной копии SQL Server, требуется значительно больше места на диске (возможно, 20 больше), чем создано `Export-CsPersistentChatData` , но в резервной копии SQL Server более вероятна процедура, с помощью которой администраторы знакомы.

</div>

<span> </span>

</div>

</div>

</div>

