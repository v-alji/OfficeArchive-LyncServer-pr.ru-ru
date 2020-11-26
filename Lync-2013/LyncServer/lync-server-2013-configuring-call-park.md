---
title: 'Lync Server 2013: настройка парковки вызовов'
description: 'Lync Server 2013: Настройка парковки звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Call Park
ms:assetid: e4c5da53-7f6c-4535-bc9b-9da2026caec8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399014(v=OCS.15)
ms:contentKeyID: 48185732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2708f26fae5706afc31aa195b9fdb82536247b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433250"
---
# <a name="configuring-call-park-in-lync-server-2013"></a><span data-ttu-id="9e9bd-103">Настройка парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-103">Configuring Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e9bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e9bd-104">

<span> </span></span></span>

<span data-ttu-id="9e9bd-105">_**Тема последнего изменения:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="9e9bd-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="9e9bd-106">Метод парковки позволяет корпоративному голосовому пользователю перевести звонок на удержание с одного телефона и затем получить его позже, набрав внутренний номер (например, *орбита на обороте*) с любого телефона.</span><span class="sxs-lookup"><span data-stu-id="9e9bd-106">Call Park enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later by dialing an internal number (known as a Call Park *orbit*) from any telephone.</span></span>

<span data-ttu-id="9e9bd-107">Компоненты, используемые при использовании функции парковки, автоматически устанавливаются и включаются на сервере переднего плана или стандартном сервере Standard Edition при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="9e9bd-107">The components that Call Park uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="9e9bd-108">Однако вы должны настроить приостановку звонков, прежде чем она будет доступна для пользователей.</span><span class="sxs-lookup"><span data-stu-id="9e9bd-108">However, you must configure Call Park before it is available to users.</span></span>

<span data-ttu-id="9e9bd-109">В этом разделе рассказывается, как настроить приостановку звонка.</span><span class="sxs-lookup"><span data-stu-id="9e9bd-109">This section guides you through the configuration of Call Park.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9e9bd-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="9e9bd-110">In This Section</span></span>

  - [<span data-ttu-id="9e9bd-111">Необходимые условия и права пользователя для настройки парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-111">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-call-park-configuration-prerequisites-and-user-rights.md)

  - [<span data-ttu-id="9e9bd-112">Процесс развертывания для парковки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-112">Deployment process for Call Park in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-call-park.md)

  - [<span data-ttu-id="9e9bd-113">Настройка таблицы орбит парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-113">Configure the Call Park orbit table in Lync Server 2013</span></span>](lync-server-2013-configure-the-call-park-orbit-table.md)

  - [<span data-ttu-id="9e9bd-114">Настройка параметров парковки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-114">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="9e9bd-115">Настройка музыкального сопровождения для приема звонков на удержании в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-115">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="9e9bd-116">Включение приостановки звонков для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-116">Enable Call Park for users in Lync Server 2013</span></span>](lync-server-2013-enable-call-park-for-users.md)

  - [<span data-ttu-id="9e9bd-117">Проверка правил нормализации для парковки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-117">Verify normalization rules for Call Park in Lync Server 2013</span></span>](lync-server-2013-verify-normalization-rules-for-call-park.md)

  - [<span data-ttu-id="9e9bd-118">Необязательно Проверка развертывания парковки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e9bd-118">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-call-park-deployment.md)

<span data-ttu-id="9e9bd-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e9bd-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

