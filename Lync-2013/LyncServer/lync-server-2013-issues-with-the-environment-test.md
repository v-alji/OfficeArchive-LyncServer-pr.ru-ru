---
title: 'Lync Server 2013: проблемы с проверкой среды'
description: 'Lync Server 2013: проблемы с проверкой среды.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the environment test
ms:assetid: ff1fe0d3-35b2-41ef-87e7-6a61e9e1d2ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205421(v=OCS.15)
ms:contentKeyID: 48185970
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 551d7e914480e178e0558c1d17eefcf060c0688e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426720"
---
# <a name="issues-with-the-environment-test-in-lync-server-2013"></a><span data-ttu-id="33a6f-103">Проблемы, связанные с проверкой среды в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33a6f-103">Issues with the environment test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33a6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33a6f-104">

<span> </span></span></span>

<span data-ttu-id="33a6f-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="33a6f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="33a6f-106">Анализатор соответствия рекомендациям позволяет удостовериться в том, что ваша среда Lync Server 2013 является поддерживаемой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="33a6f-106">Best Practices Analyzer provides a way for you to verify that your Lync Server 2013 environment is a supported configuration.</span></span> <span data-ttu-id="33a6f-107">В рамках проверки доменных служб Active Directory анализатор соответствия рекомендациям делает следующее:</span><span class="sxs-lookup"><span data-stu-id="33a6f-107">As part of the Active Directory Domain Services check, Best Practices Analyzer does the following:</span></span>

  - <span data-ttu-id="33a6f-108">Проверка леса доменных служб Active Directory и подготовки схемы.</span><span class="sxs-lookup"><span data-stu-id="33a6f-108">Verifies the Active Directory Domain Services forest and schema preparation.</span></span>

  - <span data-ttu-id="33a6f-109">Определяет количество сайтов и доменов доменных служб Active Directory в развертывании.</span><span class="sxs-lookup"><span data-stu-id="33a6f-109">Identifies the number of Active Directory Domain Services sites and domains in the deployment.</span></span>

  - <span data-ttu-id="33a6f-110">Проверка уровней леса и домена.</span><span class="sxs-lookup"><span data-stu-id="33a6f-110">Checks the forest and domain levels.</span></span>

  - <span data-ttu-id="33a6f-111">Проверяет версию контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="33a6f-111">Checks the domain controller version.</span></span>

  - <span data-ttu-id="33a6f-112">Определяет контекст именования домена, конфигурации и схемы.</span><span class="sxs-lookup"><span data-stu-id="33a6f-112">Identifies the domain, configuration, and schema naming context.</span></span>

  - <span data-ttu-id="33a6f-113">Определяет количество включенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="33a6f-113">Identifies the number of enabled users.</span></span>

  - <span data-ttu-id="33a6f-114">Проверка хранения глобальных параметров доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33a6f-114">Checks where the global Active Directory Domain Services settings are stored.</span></span>

  - <span data-ttu-id="33a6f-115">Проверка точек соединения службы (SCPs) для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="33a6f-115">Checks for the service connection points (SCPs) for Lync Server.</span></span>

  - <span data-ttu-id="33a6f-116">Определяет версию базы данных.</span><span class="sxs-lookup"><span data-stu-id="33a6f-116">Identifies the database version.</span></span>

<div>

## <a name="resolving-issues-with-the-environment"></a><span data-ttu-id="33a6f-117">Устранение проблем с окружающей средой</span><span class="sxs-lookup"><span data-stu-id="33a6f-117">Resolving Issues with the Environment</span></span>

<span data-ttu-id="33a6f-118">Если при тестировании среды обнаружены проблемы с вашей средой, это может быть вызвано проблемами с конфигурацией Active Directory или уровнем программного обеспечения, запущенного на определенных серверах.</span><span class="sxs-lookup"><span data-stu-id="33a6f-118">If the environment test found problems with your environment, these problems are probably caused by issues with your Active Directory configuration or the level of software running on specific servers.</span></span> <span data-ttu-id="33a6f-119">Например, если анализатор соответствия рекомендациям определяет контроллеры домена в среде под управлением Windows Server 2000, он выдаст предупреждение, и вам потребуется обновить эти контроллеры домена до поддерживаемой версии Windows Server.</span><span class="sxs-lookup"><span data-stu-id="33a6f-119">For example, if Best Practices Analyzer identifies any domain controllers in your environment that are running Windows Server 2000, it will issue a warning and you will need to upgrade those domain controllers to a supported version of Windows Server.</span></span>

<span data-ttu-id="33a6f-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33a6f-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

