---
title: 'Lync Server 2013: обновление списка включения Outlook'
description: 'Lync Server 2013: обновление списка включения Outlook.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Updating the Outlook enable list
ms:assetid: 5db120dc-52f9-4dde-acb9-3824ae245086
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215438(v=OCS.15)
ms:contentKeyID: 48242739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96edc327fa1b63d5da95eb6ea36a2296659910d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399472"
---
# <a name="updating-the-outlook-enable-list-in-lync-server-2013"></a><span data-ttu-id="80e92-103">Обновление списка включения Outlook в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80e92-103">Updating the Outlook enable list in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80e92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80e92-104">

<span> </span></span></span>

<span data-ttu-id="80e92-105">_**Тема последнего изменения:** 2013-01-07_</span><span class="sxs-lookup"><span data-stu-id="80e92-105">_**Topic Last Modified:** 2013-01-07_</span></span>

<span data-ttu-id="80e92-106">Вы можете сделать так, чтобы надстройка сетевого собрания для Microsoft Lync 2013 всегда оставалась включена для пользователей путем создания политики, которая включает ее в список управления надстройками для Outlook.</span><span class="sxs-lookup"><span data-stu-id="80e92-106">You can ensure that Online Meeting Add-in for Microsoft Lync 2013 always remains enabled for users by creating a policy that includes it in the Add-in Management List for Outlook.</span></span> <span data-ttu-id="80e92-107">Политика списка управления надстройками входит в файлы административных шаблонов Office для консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="80e92-107">The Add-in Management List policy is included in the Office administrative template files for the Group Policy Management Console.</span></span> <span data-ttu-id="80e92-108">Он создает раздел реестра в разделе \\ политики программного обеспечения HKCU \\ \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ устойчивость \\ AddinList.</span><span class="sxs-lookup"><span data-stu-id="80e92-108">It creates a registry key under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList.</span></span> <span data-ttu-id="80e92-109">Вы можете добавить в этот раздел значение ucaddin.dll и настроить ucaddin.dll значение так, чтобы оно всегда было включено и пользователи не могли отключить его вручную.</span><span class="sxs-lookup"><span data-stu-id="80e92-109">You can add a value for the ucaddin.dll to this key, and configure the ucaddin.dll value so that it is always enabled and so that users cannot manually disable it</span></span>

<div>

## <a name="to-add-ucaddindll-to-the-outlook-add-in-list"></a><span data-ttu-id="80e92-110">Добавление ucaddin.dll в список надстроек для Outlook</span><span class="sxs-lookup"><span data-stu-id="80e92-110">To Add ucaddin.dll to the Outlook Add-in List</span></span>

  - <span data-ttu-id="80e92-111">В раздел реестра AddinList, который находится в разделе \\ политики программного обеспечения HKCU \\ \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ устойчивость \\ AddinList, добавьте следующее значение:</span><span class="sxs-lookup"><span data-stu-id="80e92-111">To the AddinList registry key, located under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList, add the following value:</span></span>
    
      - <span data-ttu-id="80e92-112">Тип реестра = REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="80e92-112">Registry Type = REG\_SZ</span></span>
    
      - <span data-ttu-id="80e92-113">Name = ucaddin.dll</span><span class="sxs-lookup"><span data-stu-id="80e92-113">Name = ucaddin.dll</span></span>
    
      - <span data-ttu-id="80e92-114">Value = 1 (указывает, что надстройка всегда включена и не может управляться конечным пользователем)</span><span class="sxs-lookup"><span data-stu-id="80e92-114">Value = 1 (specifies that the add-in is always enabled and cannot be managed by the end user)</span></span>

<span data-ttu-id="80e92-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80e92-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

