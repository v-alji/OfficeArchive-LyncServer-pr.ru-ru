---
title: 'Lync Server 2013: качество взаимодействия (QoE)'
description: 'Lync Server 2013: качество взаимодействия (QoE).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Quality of Experience (QoE)
ms:assetid: 097fb65e-4a3e-45ff-a88c-d6022dc8f872
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687963(v=OCS.15)
ms:contentKeyID: 49733548
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eaec463cf5e3316b9a4105aa2d03ba6d1d459111
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436715"
---
# <a name="quality-of-experience-qoe-in-lync-server-2013"></a><span data-ttu-id="fcf0a-103">Качество работы (QoE) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcf0a-103">Quality of Experience (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fcf0a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fcf0a-104">

<span> </span></span></span>

<span data-ttu-id="fcf0a-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="fcf0a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="fcf0a-106">Служба отслеживания качества взаимодействия (QoE) записывает числовые данные, которые показывают качество мультимедиа-данных, и сведения об участниках, именах устройств, драйверах, IP-адресах и типах конечных точек, использованных во время звонка или сеанса.</span><span class="sxs-lookup"><span data-stu-id="fcf0a-106">Quality of Experience (QoE) records numeric data that indicates the media quality and information about participants, device names, drivers, IP addresses, and endpoint types involved in calls and sessions.</span></span> <span data-ttu-id="fcf0a-107">При установке Lync Server 2013 Вы также устанавливаете предопределенную коллекцию глобальных параметров конфигурации для QoE.</span><span class="sxs-lookup"><span data-stu-id="fcf0a-107">When you install Lync Server 2013, you will also install a predefined collection of global configuration settings for QoE.</span></span> <span data-ttu-id="fcf0a-108">Используйте разделы этой главы для настройки значений QoE.</span><span class="sxs-lookup"><span data-stu-id="fcf0a-108">Use the topics in this section to configure QoE settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fcf0a-109">Содержание</span><span class="sxs-lookup"><span data-stu-id="fcf0a-109">In This Section</span></span>

  - [<span data-ttu-id="fcf0a-110">Создание параметров конфигурации качества взаимодействия в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcf0a-110">Create Quality of Experience configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-quality-of-experience-configuration-settings.md)

  - [<span data-ttu-id="fcf0a-111">Обеспечение качества взаимодействия в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcf0a-111">Enable Quality of Experience in Lync Server 2013</span></span>](lync-server-2013-enable-quality-of-experience.md)

  - [<span data-ttu-id="fcf0a-112">Изменение параметров качества взаимодействия в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcf0a-112">Modify Quality of Experience settings in Lync Server 2013</span></span>](lync-server-2013-modify-quality-of-experience-settings.md)

  - [<span data-ttu-id="fcf0a-113">Удаление параметров конфигурации качества взаимодействия в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcf0a-113">Delete Quality of Experience configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-quality-of-experience-configuration-settings.md)

  - [<span data-ttu-id="fcf0a-114">Ручная очистка записи сведений о звонке и баз данных качества обслуживания в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcf0a-114">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>](lync-server-2013-manually-purging-the-call-detail-recording-and-quality-of-experience-databases.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fcf0a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="fcf0a-115">See Also</span></span>


[<span data-ttu-id="fcf0a-116">Настройка записи сведений о звонке и параметров качества обслуживания в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcf0a-116">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md)  
  

<span data-ttu-id="fcf0a-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fcf0a-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

