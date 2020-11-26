---
title: Средство тестирования нагрузки и производительности Lync Server 2013
description: Инструмент для Lync Server 2013, погрузка и производительность.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Stress and Performance Tool
ms:assetid: dc03db19-d104-402e-9951-240681b3fb69
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945609(v=OCS.15)
ms:contentKeyID: 51541435
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 073aa49b8c9002ff23cfea61904735cdc0144cfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446446"
---
# <a name="lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="9b0b9-103">Средство тестирования нагрузки и производительности Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b0b9-103">Lync Server 2013 Stress and Performance Tool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b0b9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b0b9-104">

<span> </span></span></span>

<span data-ttu-id="9b0b9-105">_**Тема последнего изменения:** 2013-01-25_</span><span class="sxs-lookup"><span data-stu-id="9b0b9-105">_**Topic Last Modified:** 2013-01-25_</span></span>

<span data-ttu-id="9b0b9-106">Инструмент Lync Server 2013 содержит инструменты, упрощающие планирование производственных мощностей для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-106">The Lync Server 2013 Stress and Performance Tool includes tools that simplify capacity planning for Lync Server 2013.</span></span> <span data-ttu-id="9b0b9-107">С помощью средства нагрузки и производительности Lync Server 2013 вы можете:</span><span class="sxs-lookup"><span data-stu-id="9b0b9-107">The Lync Server 2013 Stress and Performance Tool will help you to:</span></span>

  - <span data-ttu-id="9b0b9-108">Упростите планирование оборудования для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-108">Simplify your hardware planning for Lync Server 2013 .</span></span>

  - <span data-ttu-id="9b0b9-109">Предоставьте вам расширенные знания и рекомендации по настройке производительности.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-109">Provide you with increased knowledge and best practices for performance tuning.</span></span>

  - <span data-ttu-id="9b0b9-110">Измерьте производительность намеченных развертываний Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9b0b9-110">Measure the performance of your intended Lync Server 2013 deployments.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9b0b9-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="9b0b9-111">In This Section</span></span>

1.  [<span data-ttu-id="9b0b9-112">Введение</span><span class="sxs-lookup"><span data-stu-id="9b0b9-112">Introduction</span></span>](introduction.md)

2.  [<span data-ttu-id="9b0b9-113">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="9b0b9-113">Prerequisites</span></span>](prerequisites.md)

3.  [<span data-ttu-id="9b0b9-114">Установка</span><span class="sxs-lookup"><span data-stu-id="9b0b9-114">Setup</span></span>](setup.md)

4.  [<span data-ttu-id="9b0b9-115">Настройка сценариев Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b0b9-115">Configure Lync Server 2013 Scenarios</span></span>](configure-lync-server-2013-scenarios.md)

5.  [<span data-ttu-id="9b0b9-116">Создание пользователей и контактов</span><span class="sxs-lookup"><span data-stu-id="9b0b9-116">Create Users and Contacts</span></span>](create-users-and-contacts.md)

6.  [<span data-ttu-id="9b0b9-117">Настройка профиля пользователя</span><span class="sxs-lookup"><span data-stu-id="9b0b9-117">Configure User Profile</span></span>](configure-user-profile.md)

7.  [<span data-ttu-id="9b0b9-118">Запуск LyncPerfTool</span><span class="sxs-lookup"><span data-stu-id="9b0b9-118">Run LyncPerfTool</span></span>](run-lyncperftool.md)

8.  [<span data-ttu-id="9b0b9-119">Интерпретация результатов</span><span class="sxs-lookup"><span data-stu-id="9b0b9-119">Interpreting the Results</span></span>](interpreting-the-results.md)

9.  [<span data-ttu-id="9b0b9-120">Вопросы и ответы по работе с Lync Server 2013 с помощью средств нагрузки и производительности</span><span class="sxs-lookup"><span data-stu-id="9b0b9-120">Lync Server 2013 Stress and Performance Tool FAQ</span></span>](lync-server-2013-stress-and-performance-tool-faq.md)

<span data-ttu-id="9b0b9-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b0b9-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

