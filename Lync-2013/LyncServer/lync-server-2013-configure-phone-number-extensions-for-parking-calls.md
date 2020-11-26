---
title: 'Lync Server 2013: Настройка расширений номеров телефонов для вызовов парковки'
description: 'Lync Server 2013: Настройка расширений телефонных номеров для вызовов парковки.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure phone number extensions for parking calls
ms:assetid: fbf97624-9587-42a6-b276-1b69c574a74d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182611(v=OCS.15)
ms:contentKeyID: 48185980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6219e04243d0c19bc37251f7d113f7ebdd09fb72
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433810"
---
# <a name="configure-phone-number-extensions-for-parking-calls-in-lync-server-2013"></a>Настройка расширений номеров телефонов для вызовов парковки в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-10_

Приложение "присоединение к звонку" использует номера добавочных номеров в таблице "парковки на орбиту", чтобы приостановить звонки. Вам нужно настроить таблицу на приостановку соединения с диапазонами добавочных номеров, которые ваша организация резервирует для припаркованных звонков. Эти добавочные номера должны быть виртуальными (то есть не иметь назначенного пользователя или назначенный телефон). Каждый пул Lync Server, в котором развернут и настроено приложение для приостановки звонков, может иметь один или несколько диапазонов по орбите. Диапазоны орбиты должны быть глобально уникальными в рамках развертывания Lync Server.

<div>


> [!IMPORTANT]  
> Для использования функции "Приостановка звонка" необходимо установить флажок " <STRONG>включить приостановку звонка</STRONG> " в политике голосовой связи. По умолчанию этот флажок не установлен.



</div>

<div>

## <a name="in-this-section"></a>Содержание

  - [Создание или изменение диапазона орбиты на расстоянии вверх на сервере Lync Server 2013](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

  - [Удаление диапазона орбиты на расстоянии вверх на сервере Lync Server 2013](lync-server-2013-delete-a-call-park-orbit-range.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

