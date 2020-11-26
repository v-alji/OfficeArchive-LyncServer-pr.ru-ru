---
title: Развертывание устройства или сервера для обеспечения связи в филиалах — задачи центрального сайта
description: Развертывание бесперебойно работающего устройства филиалов или задач серверного веб-сайта.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server - central site tasks
ms:assetid: 0f631a36-fc2e-41cd-8a0d-f27e84f4a89e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398189(v=OCS.15)
ms:contentKeyID: 48183422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4460ea215d6fc80ee89f1ca9bc42f08ac5d14617
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430135"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013---central-site-tasks"></a><span data-ttu-id="d72f7-103">Развертывание устройства или сервера для обеспечения связи в филиалах с помощью Lync Server 2013 — задачи центрального сайта</span><span class="sxs-lookup"><span data-stu-id="d72f7-103">Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d72f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d72f7-104">

<span> </span></span></span>

<span data-ttu-id="d72f7-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="d72f7-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="d72f7-106">Выполните задачи, описанные в этом разделе, на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="d72f7-106">Complete the tasks in this section at the central site.</span></span> <span data-ttu-id="d72f7-107">Если вы развертываете бесперебойный сервер филиала, пропустите первую задачу.</span><span class="sxs-lookup"><span data-stu-id="d72f7-107">If you’re deploying a Survivable Branch Server, skip the first task.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="d72f7-108">Перед выполнением задач, описанных в этом разделе, должны быть выполнены следующие условия:</span><span class="sxs-lookup"><span data-stu-id="d72f7-108">Before you perform the tasks in this section, the following conditions must be in place:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="d72f7-109">Сервер Lync Server должен быть настроен на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="d72f7-109">Lync Server must be set up at the central site.</span></span></P>
> <LI>
> <P><span data-ttu-id="d72f7-110">Специалист по установке на сайте филиала должен быть добавлен в группу RTCUniversalSBATechnicians.</span><span class="sxs-lookup"><span data-stu-id="d72f7-110">An installation technician at the branch site must be added to the RTCUniversalSBATechnicians group.</span></span></P></LI></UL><span data-ttu-id="d72f7-111">Кроме того, мы рекомендуем вам выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d72f7-111">In addition, we recommend that you do the following:</span></span>
> <UL>
> <LI>
> <P><span data-ttu-id="d72f7-112">Разверните DHCP-сервер на каждом сайте филиала, чтобы разрешить клиентам получать IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="d72f7-112">Deploy a DHCP server at each branch site to enable clients to obtain IP addresses.</span></span></P>
> <LI>
> <P><span data-ttu-id="d72f7-113">Кроме того, чтобы развернуть DHCP-сервер на каждом сайте филиала, включите службу DHCP для Lync Server на устройстве с бесперебойной ветвью или работающем сервере филиала с помощью командлета оболочки Lync Server Management Shell <STRONG>Set-CsRegistrarConfiguration-EnableDHCPServer $true</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d72f7-113">As an alternative to deploying a DHCP server at each branch site, enable Lync Server DHCP on the Survivable Branch Appliance or Survivable Branch Server by using the Lync Server Management Shell cmdlet <STRONG>Set-CsRegistrarConfiguration –EnableDHCPServer $true</STRONG>.</span></span> <span data-ttu-id="d72f7-114">Подробные сведения можно найти в разделе Требования к оборудованию и программному обеспечению <A href="lync-server-2013-branch-site-resiliency-requirements.md">для обеспечения устойчивости сайтов для Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="d72f7-114">For details, see the “Hardware and Software Requirements” section of <A href="lync-server-2013-branch-site-resiliency-requirements.md">Branch-site resiliency requirements for Lync Server 2013</A> in the Planning documentation.</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d72f7-115">Содержание</span><span class="sxs-lookup"><span data-stu-id="d72f7-115">In This Section</span></span>

  - [<span data-ttu-id="d72f7-116">Добавление устройства для обеспечения связи в филиалах к Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d72f7-116">Add a Survivable Branch Appliance to Active Directory in Lync Server 2013</span></span>](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md)

  - [<span data-ttu-id="d72f7-117">Добавление сайтов филиалов в топологию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d72f7-117">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="d72f7-118">Определение устройства или сервера для обеспечения связи в филиалах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d72f7-118">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="d72f7-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d72f7-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

