---
title: 'Lync Server 2013: Настройка управления допуском звонков'
description: 'Lync Server 2013: Настройка управления допуском звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure call admission control
ms:assetid: ce3e6e71-1e33-4cff-849a-c0468e61fef6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398870(v=OCS.15)
ms:contentKeyID: 48185464
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c6da7e20f45e61f7364af3e8b749def05bd29fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399613"
---
# <a name="configure-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="a3da8-103">Настройка управления допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-103">Configure call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3da8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3da8-104">

<span> </span></span></span>

<span data-ttu-id="a3da8-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="a3da8-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="a3da8-106">Система контроля допуска звонков обеспечивает проверку возможности установления сеанса связи в реальном времени без ухудшения качества видео- и голосовой связи в перегруженных сетях.</span><span class="sxs-lookup"><span data-stu-id="a3da8-106">Call admission control (CAC) is a solution that determines whether a real-time session can be established based on the available bandwidth to help prevent poor audio/video quality for users on congested networks.</span></span> <span data-ttu-id="a3da8-107">Управление трафиком в реальном времени осуществляется только для звуковых и видеофайлов и не влияет на трафик данных.</span><span class="sxs-lookup"><span data-stu-id="a3da8-107">CAC controls real-time traffic only for audio and video, and does not affect data traffic.</span></span> <span data-ttu-id="a3da8-108">CAC может перенаправлять Звонок через Интернет-путь, если путь к глобальной сети по умолчанию не имеет необходимой пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="a3da8-108">CAC may route the call through an Internet path when the default WAN path does not have the required bandwidth.</span></span> <span data-ttu-id="a3da8-109">Подробнее смотрите в разделе [Планирование управления допуском звонков в Lync Server 2013](lync-server-2013-planning-for-call-admission-control.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="a3da8-109">For details, see [Planning for call admission control in Lync Server 2013](lync-server-2013-planning-for-call-admission-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="a3da8-110">В этом разделе представлен набор примеров процедур, демонстрирующих способы развертывания и управления CAC в сети.</span><span class="sxs-lookup"><span data-stu-id="a3da8-110">This section provides a set of example procedures that illustrate how to deploy and manage CAC in your network.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a3da8-111">Перед развертыванием CAC необходимо собрать все необходимые данные для топологии корпоративной сети, как описано в <A href="lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md">примере. сбор требований для управления допуском звонков в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="a3da8-111">Before you deploy CAC, you must gather all of the required information for your enterprise network topology, as described in <A href="lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md">Example: Gathering your requirements for call admission control in Lync Server 2013</A> in the Planning documentation.</span></span> <span data-ttu-id="a3da8-112">Кроме того, убедитесь, что компоненты CAC установлены и активированы, как описано в разделе <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Определение и Настройка внешнего пула и сервера Standard Edition в Lync server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="a3da8-112">Also be sure that CAC components have been installed and activated, as described in <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="a3da8-113">Все примеры развертывания и управления CAC в этом разделе выполняются с помощью командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="a3da8-113">All CAC deployment and management examples in this section are performed by using the Lync Server Management Shell.</span></span> <span data-ttu-id="a3da8-114">Кроме того, вы можете использовать раздел " <STRONG>Настройка сети</STRONG> " панели управления Lync Server для управления CAC.</span><span class="sxs-lookup"><span data-stu-id="a3da8-114">As an alternative, you can also use the <STRONG>Network Configuration</STRONG> section of Lync Server Control Panel to manage CAC.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a3da8-115">Содержание</span><span class="sxs-lookup"><span data-stu-id="a3da8-115">In This Section</span></span>

  - [<span data-ttu-id="a3da8-116">Настройка регионов сети для CAC в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-116">Configure network regions for CAC in Lync Server 2013</span></span>](lync-server-2013-configure-network-regions-for-cac.md)

  - [<span data-ttu-id="a3da8-117">Создание профилей политики пропускной способности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-117">Create bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-create-bandwidth-policy-profiles.md)

  - [<span data-ttu-id="a3da8-118">Настройка сетевых сайтов для CAC в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-118">Configure network sites for CAC in Lync Server 2013</span></span>](lync-server-2013-configure-network-sites-for-cac.md)

  - [<span data-ttu-id="a3da8-119">Связывание подсетей с сетевыми сайтами для CAC в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-119">Associate subnets with network sites for CAC in Lync Server 2013</span></span>](lync-server-2013-associate-subnets-with-network-sites-for-cac.md)

  - [<span data-ttu-id="a3da8-120">Создание ссылок на сетевой регион в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-120">Create network region links in Lync Server 2013</span></span>](lync-server-2013-create-network-region-links.md)

  - [<span data-ttu-id="a3da8-121">Создание маршрутов между межсетевыми регионах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-121">Create network interregion routes in Lync Server 2013</span></span>](lync-server-2013;-create-network-interregion-routes.md)

  - [<span data-ttu-id="a3da8-122">Создание политик межсайтовой сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-122">Create network intersite policies in Lync Server 2013</span></span>](lync-server-2013-create-network-intersite-policies.md)

  - [<span data-ttu-id="a3da8-123">Включение управления допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-123">Enable call admission control in Lync Server 2013</span></span>](lync-server-2013-enable-call-admission-control.md)

  - [<span data-ttu-id="a3da8-124">Контрольный список развертывания управления допуском звонков для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3da8-124">Call admission control deployment checklist for Lync Server 2013</span></span>](lync-server-2013-call-admission-control-deployment-checklist.md)

<span data-ttu-id="a3da8-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3da8-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

