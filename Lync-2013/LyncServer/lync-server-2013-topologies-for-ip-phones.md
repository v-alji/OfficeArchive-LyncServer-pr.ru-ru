---
title: 'Lync Server 2013: топологии для IP-телефонов'
description: 'Lync Server 2013: топологии для IP-телефонов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies for IP phones
ms:assetid: 26ebffcf-43ff-4e70-847d-0fbc90e94e57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425740(v=OCS.15)
ms:contentKeyID: 48183662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a151a83a69e1f7e14dcbed8d8ab1038157fa839
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439668"
---
# <a name="topologies-for-ip-phones-in-lync-server-2013"></a><span data-ttu-id="f45b5-103">Топологии для IP-телефонов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f45b5-103">Topologies for IP phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f45b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f45b5-104">

<span> </span></span></span>

<span data-ttu-id="f45b5-105">_**Тема последнего изменения:** 2012-06-21_</span><span class="sxs-lookup"><span data-stu-id="f45b5-105">_**Topic Last Modified:** 2012-06-21_</span></span>

<span data-ttu-id="f45b5-106">В этом разделе представлен обзор процесса подключения и описаны различия между подключением IP-телефона к внутренней и внешней сети.</span><span class="sxs-lookup"><span data-stu-id="f45b5-106">This section provides an overview of the connectivity process and explains the differences between how an IP phone connects in an internal and external network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f45b5-107">Lync Server поддерживает следующие IP-телефоны: Aastra 6721ip Common Area Phone, Aastra 6725ip стационарный телефон, HP 4110 IP Phone (на стационарном телефоне), HP 4120 IP-телефон (на устройстве с телефонным аппаратом), Polycom CX600 IP Desk Phone, Polycom CX700 IP-телефонной сети, Polycom CX500 IP с телефонным телефоном и Polycom CX3000 IP.</span><span class="sxs-lookup"><span data-stu-id="f45b5-107">Lync Server provides support for the following IP phones: the Aastra 6721ip common area phone, Aastra 6725ip desk phone, HP 4110 IP Phone (common area phone), HP 4120 IP Phone (desk phone), Polycom CX600 IP desk phone, Polycom CX700 IP desk phone, Polycom CX500 IP common area phone, and Polycom CX3000 IP conference phone.</span></span> <span data-ttu-id="f45b5-108">Из этих телефонов все, кроме Polycom CX700, могут запускать Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="f45b5-108">Of those phones, all but the Polycom CX700 can run Lync Phone Edition.</span></span>



</div>

<span data-ttu-id="f45b5-109">На приведенной ниже схеме описаны все компоненты, связанные с подключением к устройствам в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="f45b5-109">The following diagram describes all the components involved in device connectivity within the corporate environment.</span></span>

<span data-ttu-id="f45b5-110">**Внутренняя топология**</span><span class="sxs-lookup"><span data-stu-id="f45b5-110">**Internal Topology**</span></span>

<span data-ttu-id="f45b5-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span><span class="sxs-lookup"><span data-stu-id="f45b5-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f45b5-112">Предыдущий рисунок является логическим представлением, а не физическим обзором.</span><span class="sxs-lookup"><span data-stu-id="f45b5-112">The previous figure is a logical representation, not a physical overview.</span></span> <span data-ttu-id="f45b5-113">Например, доменные службы Active Directory (AD DS) редко находятся на том же компьютере, что и любые компоненты сервера Lync.</span><span class="sxs-lookup"><span data-stu-id="f45b5-113">For example, Active Directory Domain Services (AD DS) is rarely located on the same machine as any Lync Server components.</span></span> <span data-ttu-id="f45b5-114">Хранилище пользователей может находиться на сервере или на серверах архивации и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="f45b5-114">The user store can be located on the Back End Server or on the Archiving and Monitoring Servers.</span></span> <span data-ttu-id="f45b5-115">Консоль управления Lync Server, веб-сервер и службы обновления являются частью роли сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="f45b5-115">The Lync Server Management Shell, web server, and update services are all part of the Front End Server role.</span></span>



</div>

<span data-ttu-id="f45b5-116">На приведенной ниже схеме представлен обзор компонентов, которые используются, если устройство находится за пределами корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="f45b5-116">The following diagram provides an overview of the components involved when the device is located outside the corporate network.</span></span>

<span data-ttu-id="f45b5-117">**Внешняя топология**</span><span class="sxs-lookup"><span data-stu-id="f45b5-117">**External Topology**</span></span>

<span data-ttu-id="f45b5-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span><span class="sxs-lookup"><span data-stu-id="f45b5-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f45b5-119">Веб-служба обновления устройств обеспечивает внешний и внутренний веб-сайт, но здесь показан только внешний.</span><span class="sxs-lookup"><span data-stu-id="f45b5-119">The Device Update Web service provides an external and internal website, but only the external one is shown here.</span></span><BR><span data-ttu-id="f45b5-120">Чтобы включить внешний доступ, необходимо опубликовать в службе DNS расположение регистратора и URL-адрес службы обновления устройства для Организации.</span><span class="sxs-lookup"><span data-stu-id="f45b5-120">The location of the Registrar and the URL of the Device Update Web service for the organization must be published in DNS if external access is to be enabled.</span></span> <span data-ttu-id="f45b5-121">Кроме того, пограничный сервер должен быть развернут и правильно настроен для разрешения внешней связи с устройства в корпоративную среду и обратно.</span><span class="sxs-lookup"><span data-stu-id="f45b5-121">Additionally, the Edge Server must be deployed and correctly configured to allow external communications from the device to the corporate environment and back.</span></span> <span data-ttu-id="f45b5-122">Этот параметр не указан на предыдущей схеме, так как развертывание EDGE не предназначено для подключения устройства.</span><span class="sxs-lookup"><span data-stu-id="f45b5-122">This is omitted from the previous diagram because Edge deployment is not specific to device connectivity.</span></span>



<span data-ttu-id="f45b5-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f45b5-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

