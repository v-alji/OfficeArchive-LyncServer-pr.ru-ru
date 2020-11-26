---
title: 'Lync Server 2013: регионы сети'
description: 'Lync Server 2013: регионы сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network regions
ms:assetid: 1818e9d2-bbb7-420a-93ea-4c3da3a55ad3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687979(v=OCS.15)
ms:contentKeyID: 49733567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3506f3c543c0728f27bd091b9cd63991c4633da7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425162"
---
# <a name="network-regions-in-lync-server-2013"></a><span data-ttu-id="f9085-103">Регионы сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9085-103">Network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9085-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9085-104">

<span> </span></span></span>

<span data-ttu-id="f9085-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f9085-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f9085-106">*Регионы сетей* — это сетевые разветвители и одинарные кости, используемые в настройке управления допуском звонков, E9-1-1 и мультимедийными пропусками.</span><span class="sxs-lookup"><span data-stu-id="f9085-106">*Network regions* are the network hubs or backbones used in the configuration of call admission control, E9-1-1, and media bypass.</span></span> <span data-ttu-id="f9085-107">Следующие процедуры служат для просмотра, создания и изменения областей сети.</span><span class="sxs-lookup"><span data-stu-id="f9085-107">Use the following procedures to view, create, or modify network regions.</span></span> <span data-ttu-id="f9085-108">Например, если вы уже создали сетевые регионы для одной голосовой связи, вам не нужно создавать новые сетевые регионы; другие дополнительные функции для корпоративной голосовой связи будут использовать те же сетевые регионы.</span><span class="sxs-lookup"><span data-stu-id="f9085-108">For example, if you have already created network regions for one Voice feature, you do not need to create new network regions; other advanced Enterprise Voice features will use those same network regions.</span></span> <span data-ttu-id="f9085-109">Однако вам может потребоваться изменить существующее определение области сети для применения параметров, относящихся к функции.</span><span class="sxs-lookup"><span data-stu-id="f9085-109">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="f9085-110">Например, если вы создали области сети для службы E9-1-1, для которой не требуется связанный центральный сайт, и затем развернули службу контроля допуска звонков, вам потребуется изменить определения областей сети, чтобы указать центральный сайт.</span><span class="sxs-lookup"><span data-stu-id="f9085-110">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and you then deploy call admission control, you need to modify the network region definitions to specify a central site.</span></span> <span data-ttu-id="f9085-111">Подробности можно найти [в разделе Настройка регионов сети для CAC в Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="f9085-111">For details, see [Configure network regions for CAC in Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f9085-112">Любые особые требования к функциональным возможностям для определений сетевых областей описаны в разделе Развертывание для этой функции.</span><span class="sxs-lookup"><span data-stu-id="f9085-112">Any feature-specific requirements for network region definitions are documented in the Deployment topics for the feature.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f9085-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="f9085-113">In This Section</span></span>

  - [<span data-ttu-id="f9085-114">Просмотр сведений о сетевом регионе в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9085-114">Viewing network region information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-region-information.md)

  - [<span data-ttu-id="f9085-115">Создание и изменение областей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9085-115">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)

  - [<span data-ttu-id="f9085-116">Удаление существующих областей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9085-116">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)

</div>

<div>

## <a name="reference"></a><span data-ttu-id="f9085-117">Справка</span><span class="sxs-lookup"><span data-stu-id="f9085-117">Reference</span></span>

[<span data-ttu-id="f9085-118">Развертывание улучшенных функций голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9085-118">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

<span data-ttu-id="f9085-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9085-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

