---
title: 'Lync Server 2013: создание топологии пограничных серверов и директора'
description: 'Lync Server 2013: создание топологии EDGE и Director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Building an edge and Director topology
ms:assetid: 11e5759e-d69f-4c39-8994-f467c279c558
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398202(v=OCS.15)
ms:contentKeyID: 48183451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcb2d422136cf0a421c68ebc2adba50f03c5cc85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435938"
---
# <a name="building-an-edge-and-director-topology-in-lync-server-2013"></a><span data-ttu-id="b36cc-103">Создание топологии пограничных серверов и директора в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b36cc-103">Building an edge and Director topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b36cc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b36cc-104">

<span> </span></span></span>

<span data-ttu-id="b36cc-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="b36cc-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="b36cc-106">Построение топологии включает следующие задачи планирования и развертывания.</span><span class="sxs-lookup"><span data-stu-id="b36cc-106">Building the topology involves the following planning and deployment tasks:</span></span>

  - <span data-ttu-id="b36cc-107">**Планирование**   Необходимо определить подходящую топологию для своей организации и определить компоненты, необходимые для ее развертывания.</span><span class="sxs-lookup"><span data-stu-id="b36cc-107">**Planning**   You need to define an appropriate topology for your organization and identify the components required to deploy it.</span></span> <span data-ttu-id="b36cc-108">Это стандартные действия, которые можно выполнить в процессе планирования.</span><span class="sxs-lookup"><span data-stu-id="b36cc-108">These are standard steps in the planning process.</span></span> <span data-ttu-id="b36cc-109">Microsoft Lync Server 2013, средство планирования, предоставленное в Lync Server 2013, упрощает процесс планирования, а также позволяет легко вносить изменения при завершении требований и планов.</span><span class="sxs-lookup"><span data-stu-id="b36cc-109">The Microsoft Lync Server 2013, Planning Tool provided with Lync Server 2013 makes it easy to start the planning process, as well as including the ability to easily make changes as your requirements and plans are finalized.</span></span>

  - <span data-ttu-id="b36cc-110">**Развертывание**   Топология, определенная с помощью Topology Builder, очень важна для развертывания любого сервера Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b36cc-110">**Deployment**   The topology that you define using Topology Builder is essential to the deployment of any Lync Server 2013 server.</span></span> <span data-ttu-id="b36cc-111">Если вы не закончите определение и публикацию топологии с помощью построителя топологии в ходе планирования, необходимо завершить ее и опубликовать топологию перед развертыванием пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="b36cc-111">If you do not finish defining and publishing your topology by using Topology Builder as part of your planning efforts, you must complete it and publish the topology before you deploy your Edge Servers.</span></span>

<span data-ttu-id="b36cc-112">Вы не можете развертывать компоненты пограничного сервера, пока не разворачиваете по крайней мере один внутренний пул, и вам необходимо установить построитель топологии, чтобы развернуть внутренний пул.</span><span class="sxs-lookup"><span data-stu-id="b36cc-112">You cannot deploy Edge Server components until you have deployed at least one internal pool, and you must install Topology Builder to deploy an internal pool.</span></span> <span data-ttu-id="b36cc-113">В этом разделе не рассматривается установка Topology Builder, так как это является частью процесса установки внутреннего пула.</span><span class="sxs-lookup"><span data-stu-id="b36cc-113">This section does not cover installation of Topology Builder because that is part of the installation process for the internal pool.</span></span>

<span data-ttu-id="b36cc-114">Подробнее об этих средствах см. [в разделе Контрольный список развертывания для внешних пользователей Access в Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="b36cc-114">For details about these tools, see [Deployment checklist for external user access in Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b36cc-115">Если вы ранее использовали Topology Builder, чтобы определить полную топологию, включая топологию пограничного, вы можете пропустить <A href="lync-server-2013-define-your-edge-topology.md">Определение топологии пограничного сервера в Lync server 2013</A> и <A href="lync-server-2013-publish-your-topology.md">опубликовать свою топологию в Lync Server 2013</A> для задач, описанных в этом разделе, но вам нужно выполнить <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">экспорт топологии сервера Lync Server 2013 и скопировать ее на внешние носители для установки пограничного устройства</A> .</span><span class="sxs-lookup"><span data-stu-id="b36cc-115">If you previously used Topology Builder to define a complete topology, including the edge topology, you do can skip the <A href="lync-server-2013-define-your-edge-topology.md">Define your edge topology in Lync Server 2013</A> and <A href="lync-server-2013-publish-your-topology.md">Publish your topology in Lync Server 2013</A> tasks in this section, but you do need to complete the <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A> task.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b36cc-116">Содержание</span><span class="sxs-lookup"><span data-stu-id="b36cc-116">In This Section</span></span>

  - [<span data-ttu-id="b36cc-117">Определение пограничной топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b36cc-117">Define your edge topology in Lync Server 2013</span></span>](lync-server-2013-define-your-edge-topology.md)

  - [<span data-ttu-id="b36cc-118">Определение дополнительных топологий директоров в топологии для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b36cc-118">Define optional Director topologies in your topology for Lync Server 2013</span></span>](lync-server-2013-define-optional-director-topologies-in-your-topology.md)

  - [<span data-ttu-id="b36cc-119">Публикация топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b36cc-119">Publish your topology in Lync Server 2013</span></span>](lync-server-2013-publish-your-topology.md)

  - [<span data-ttu-id="b36cc-120">Экспорт топологии Lync Server 2013 и ее копирование на внешние носители для установки в пограничной топологии</span><span class="sxs-lookup"><span data-stu-id="b36cc-120">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

<span data-ttu-id="b36cc-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b36cc-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

