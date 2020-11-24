---
title: 'Lync Server 2013: средства управления для Windows PowerShell и Lync Server 2013'
description: 'Lync Server 2013: средства управления Windows PowerShell и Lync Server Management Tools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows PowerShell and Lync Server 2013 management tools
ms:assetid: 6a285f7c-0ef5-4cab-9976-d03be276e35d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481130(v=OCS.15)
ms:contentKeyID: 59893869
ms.date: 07/20/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c8d63974ad05a041eb446182cbc7f9336044b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398902"
---
# <a name="windows-powershell-and-lync-server-2013-management-tools"></a>Средства управления для Windows PowerShell и Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2016-07-20_

В Microsoft Lync Server 2013 средства управления реализованы с помощью Windows PowerShell. Windows PowerShell включает среду командной строки, команды, связанные с продуктом, и полный язык сценариев. Средства Lync Server 2013, реализованные с помощью Windows PowerShell, включают следующие компоненты:

  - **Построитель топологии**. С помощью Topology Builder вы можете создавать, изменять и публиковать плановую топологию, а также проверять топологию до начала установки сервера. При установке Lync Server 2013 на отдельных серверах серверы считывают опубликованную топологию в процессе установки, и программа установки развертывает сервер в соответствии с топологией. После установки сведения о конфигурации автоматически реплицируются на все серверы. Компоненты можно добавлять в развертывание только с помощью построителя топологии.

  - **Командная консоль Lync Server Management Shell**. Вы можете использовать командную консоль Lync Server для управления развертыванием с помощью командной строки.

  - **Панель управления Lync Server**. Вы можете использовать пользовательский интерфейс панели управления Microsoft Lync Server 2013 для управления наиболее распространенными задачами в развертывании.

Эти средства используют командлеты Windows PowerShell для управления развертыванием, в том числе с помощью командлетов для работы с конкретными продуктами 550. Командлеты безопасности, включенные в Lync Server 2013, главным образом используются для управления проверкой подлинности, а также правами и разрешениями пользователей. Широкий спектр командлетов доступен для управления проверкой подлинности, включая командлеты для проверки подлинности с помощью сертификатов и персональных идентификационных номеров (ПИН-кодов). Кроме того, несколько командлетов позволяют использовать новый компонент управления доступом Role-Based (RBAC) для делегирования административного управления Lync Server 2013. Дополнительные сведения о командлетах Lync Server можно найти в [командной консоли Lync server 2013](lync-server-2013-lync-server-management-shell.md).

Функции безопасности сценариев для Windows PowerShell специально разработаны для помощи в предотвращении некоторых связанных с написанием сценариев проблем безопасности старых топологий, включая сценарии VBScript. Функции безопасности Windows PowerShell предназначены для создания среды, в которой пользователи не могут легко или непреднамеренно запускать сценарии. По умолчанию функции безопасности Windows PowerShell включены. Состояние этих функций можно изменять в соответствии с требованиями написания сценариев и различными целями безопасности. Это не означает, что оболочка делает запуск сценариев невозможным для пользователей. Напротив, оболочка по умолчанию затрудняет для пользователей запуск сценариев без понимания того, что они делают. Дополнительные сведения можно найти в разделе Безопасность сценариев Windows PowerShell [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145) .

</div>

<span> </span>

</div>

</div>

</div>

