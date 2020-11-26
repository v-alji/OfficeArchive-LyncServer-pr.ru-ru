---
title: 'Lync Server 2013: Настройка компьютеров с Lync Server, которые будут отслеживаться'
description: 'Lync Server 2013: Настройка компьютеров с Lync Server, которые будут отслеживаться.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computers that will be monitored
ms:assetid: 9f1b2b91-d5af-42ad-a27d-b0815f762ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205118(v=OCS.15)
ms:contentKeyID: 48184927
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 742bd8a67eb42472e598c45619514e9407cb29cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432557"
---
# <a name="configuring-the-lync-server-computers-that-will-be-monitored-in-lync-server-2013"></a><span data-ttu-id="ae88d-103">Настройка компьютеров с Lync Server, которые будут отслеживаться в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae88d-103">Configuring the Lync Server computers that will be monitored in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae88d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae88d-104">

<span> </span></span></span>

<span data-ttu-id="ae88d-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="ae88d-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="ae88d-106">Поскольку Lync Server 2013 не использует процесс центрального обнаружения, используемый в Microsoft Lync Server 2010, каждый сервер Lync Server 2013, на котором вы хотите наблюдать, должен иметь возможность самостоятельно сообщать о существовании сервера управления.</span><span class="sxs-lookup"><span data-stu-id="ae88d-106">Because Lync Server 2013 does not use the central discovery process used in Microsoft Lync Server 2010, each Lync Server 2013 computer that you want to monitor must be able to self-report its existence to the management server.</span></span> <span data-ttu-id="ae88d-107">Чтобы сделать это возможным, необходимо установить файлы агента Operations Manager на каждом из компьютеров, которые нужно отслеживать.</span><span class="sxs-lookup"><span data-stu-id="ae88d-107">To make this possible, you must install the Operations Manager agent files on each of the computers to be monitored.</span></span> <span data-ttu-id="ae88d-108">После установки файлов агента необходимо настроить компьютер так, чтобы он действовал как прокси System Center.</span><span class="sxs-lookup"><span data-stu-id="ae88d-108">After the agent files have been installed, you must configure the computer to act as a System Center proxy.</span></span> <span data-ttu-id="ae88d-109">Обратите внимание на то, что эти процедуры должны выполняться после установки и настройки сервера Lync Server на этих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="ae88d-109">Note that these procedures should be carried out after you have installed and configured Lync Server on these computers.</span></span>

<span data-ttu-id="ae88d-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae88d-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

