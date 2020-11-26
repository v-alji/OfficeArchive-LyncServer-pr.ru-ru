---
title: 'Lync Server 2013: запущенный сервер Lync Server на виртуальных серверах'
description: 'Lync Server 2013: запущенный сервер Lync Server на виртуальных серверах.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running Lync Server on virtual servers
ms:assetid: e83c0f7f-88ec-434f-b35e-adedec3c318a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399035(v=OCS.15)
ms:contentKeyID: 49733856
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 377c481ac149f556fc950a29a0c5054097f3b0e2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442203"
---
# <a name="running-lync-server-2013-on-virtual-servers"></a><span data-ttu-id="edf33-103">Запуск Lync Server 2013 на виртуальных серверах</span><span class="sxs-lookup"><span data-stu-id="edf33-103">Running Lync Server 2013 on virtual servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="edf33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="edf33-104">

<span> </span></span></span>

<span data-ttu-id="edf33-105">_**Тема последнего изменения:** 2014-03-13_</span><span class="sxs-lookup"><span data-stu-id="edf33-105">_**Topic Last Modified:** 2014-03-13_</span></span>

<span data-ttu-id="edf33-106">Lync Server 2013 поддерживает топологии виртуализации, поддерживающие все рабочие нагрузки Lync Server, в том числе обмен мгновенными сообщениями и присутствие, Конференции, голосовую связь, мониторинг, архивацию и сохраняемый чат.</span><span class="sxs-lookup"><span data-stu-id="edf33-106">Lync Server 2013 supports virtualization topologies that support all Lync Server workloads, including instant messaging (IM) and presence, conferencing, Enterprise Voice, Monitoring, Archiving, and Persistent Chat.</span></span> <span data-ttu-id="edf33-107">Обратите внимание на то, что производительность Lync Server для виртуальных топологий может сильно различаться в зависимости от используемой рабочей нагрузки, количества пользователей и оборудования узла.</span><span class="sxs-lookup"><span data-stu-id="edf33-107">Note that Lync Server performance on virtual topologies can vary greatly depending on the workloads being used, the number of users, and the host hardware.</span></span> <span data-ttu-id="edf33-108">Подробное руководство по работе с Lync Server 2013 на виртуальных серверах можно найти в техническом документе [Планирование развертывания Lync server 2013 на виртуальных серверах](https://www.microsoft.com/download/details.aspx?id=41936).</span><span class="sxs-lookup"><span data-stu-id="edf33-108">For detailed guidance about running Lync Server 2013 on virtual servers, see the white paper [Planning a Lync Server 2013 Deployment on Virtual Servers](https://www.microsoft.com/download/details.aspx?id=41936).</span></span>

<span data-ttu-id="edf33-109">Lync Server 2013 поддерживается на платформе Hyper-V и на любой платформе виртуализации, которая поддерживается программой проверки виртуализации Windows Server.</span><span class="sxs-lookup"><span data-stu-id="edf33-109">Lync Server 2013 is supported on the Hyper-V platform, and on any virtualization platform that is supported under the Windows Server Virtualization Validation Program.</span></span> <span data-ttu-id="edf33-110">Сведения об этой программе можно найти в разделе <http://www.windowsservercatalog.com/svvp.aspx> .</span><span class="sxs-lookup"><span data-stu-id="edf33-110">For information on this program, see <http://www.windowsservercatalog.com/svvp.aspx>.</span></span>

<div id="sectionSection0" class="section">

</div><span data-ttu-id="edf33-111">

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="edf33-111">

</div>

<span> </span>

</div>

</div>

</span></span></div>

