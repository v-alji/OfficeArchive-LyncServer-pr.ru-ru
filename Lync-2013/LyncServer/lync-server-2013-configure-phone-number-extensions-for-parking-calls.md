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
# <a name="configure-phone-number-extensions-for-parking-calls-in-lync-server-2013"></a><span data-ttu-id="789d6-103">Настройка расширений номеров телефонов для вызовов парковки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="789d6-103">Configure phone number extensions for parking calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="789d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="789d6-104">

<span> </span></span></span>

<span data-ttu-id="789d6-105">_**Тема последнего изменения:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="789d6-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="789d6-106">Приложение "присоединение к звонку" использует номера добавочных номеров в таблице "парковки на орбиту", чтобы приостановить звонки.</span><span class="sxs-lookup"><span data-stu-id="789d6-106">The Call Park application uses extension numbers in the Call Park orbit table to park calls.</span></span> <span data-ttu-id="789d6-107">Вам нужно настроить таблицу на приостановку соединения с диапазонами добавочных номеров, которые ваша организация резервирует для припаркованных звонков.</span><span class="sxs-lookup"><span data-stu-id="789d6-107">You need to configure the Call Park orbit table with the ranges of extension numbers that your organization reserves for parked calls.</span></span> <span data-ttu-id="789d6-108">Эти добавочные номера должны быть виртуальными (то есть не иметь назначенного пользователя или назначенный телефон).</span><span class="sxs-lookup"><span data-stu-id="789d6-108">These extensions need to be virtual extensions (that is, extensions that have no user or phone assigned to them).</span></span> <span data-ttu-id="789d6-109">Каждый пул Lync Server, в котором развернут и настроено приложение для приостановки звонков, может иметь один или несколько диапазонов по орбите.</span><span class="sxs-lookup"><span data-stu-id="789d6-109">Each Lync Server pool where a Call Park application is deployed and configured can have one or more orbit ranges.</span></span> <span data-ttu-id="789d6-110">Диапазоны орбиты должны быть глобально уникальными в рамках развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="789d6-110">Orbit ranges must be globally unique across the Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="789d6-111">Для использования функции "Приостановка звонка" необходимо установить флажок " <STRONG>включить приостановку звонка</STRONG> " в политике голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="789d6-111">You must select the <STRONG>Enable call park</STRONG> check box in your voice policy before you can use Call Park.</span></span> <span data-ttu-id="789d6-112">По умолчанию этот флажок не установлен.</span><span class="sxs-lookup"><span data-stu-id="789d6-112">By default, this option is not selected.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="789d6-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="789d6-113">In This Section</span></span>

  - [<span data-ttu-id="789d6-114">Создание или изменение диапазона орбиты на расстоянии вверх на сервере Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="789d6-114">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

  - [<span data-ttu-id="789d6-115">Удаление диапазона орбиты на расстоянии вверх на сервере Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="789d6-115">Delete a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-delete-a-call-park-orbit-range.md)

<span data-ttu-id="789d6-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="789d6-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

