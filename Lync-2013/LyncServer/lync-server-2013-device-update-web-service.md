---
title: 'Lync Server 2013: веб-служба обновления устройств'
description: 'Lync Server 2013: веб-служба обновления устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update Web service
ms:assetid: 036f473d-a131-431f-8051-76ccadc5cfba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994015(v=OCS.15)
ms:contentKeyID: 51803921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45511d34ab99f295481472f2a3c14bf21da32ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429369"
---
# <a name="device-update-web-service-in-lync-server-2013"></a><span data-ttu-id="be596-103">Веб-служба обновления устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be596-103">Device Update Web service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be596-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be596-104">

<span> </span></span></span>

<span data-ttu-id="be596-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="be596-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="be596-106">Lync Server включает веб-службу обновления устройств, которая автоматически устанавливается как часть роли веб-служб.</span><span class="sxs-lookup"><span data-stu-id="be596-106">Lync Server includes the Device Update Web service, which is automatically installed as part of the Web Services role.</span></span> <span data-ttu-id="be596-107">Эта служба позволяет загрузить обновления из Microsoft, проверить их, а затем развернуть их на IP-телефоны в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="be596-107">This service lets you download updates from Microsoft, test them, and then deploy the updates to IP phones in your organization.</span></span> <span data-ttu-id="be596-108">Кроме того, с помощью веб-службы обновления устройств можно выполнить откат устройств к предыдущим версиям программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="be596-108">You can also use Device Update Web service to roll back devices to previous software versions.</span></span>

<span data-ttu-id="be596-109">В этом разделе приводятся сведения о том, как управлять веб-службой обновления устройств и развернутыми обновлениями с помощью журналов обновлений для устройств, правил (Lync Phone Edition использует *правила* для связи обновлений микропрограмм) и параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="be596-109">This section provides details about how to manage the Device Update Web service and deployed updates by using device update logs, rules (Lync Phone Edition uses *rules* to associate firmware version updates with hardware devices), and configuration settings.</span></span>

<span data-ttu-id="be596-110">Подробные сведения о процессе и возможностях веб-службы обновления устройств можно найти в разделе [обновление устройств](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) в библиотеке TechNet 2010 для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="be596-110">For details about the Device Update Web service process and features, see [Updating Devices](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="be596-111">(Обратите внимание, что веб-служба обновления устройства, как и все компоненты Lync Phone Edition, работает аналогично с Lync Server 2013, как это происходит в Lync Server 2010.)</span><span class="sxs-lookup"><span data-stu-id="be596-111">(Note that the Device Update Web service, like all Lync Phone Edition components, works the same way with Lync Server 2013 as it does with Lync Server 2010.)</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="be596-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="be596-112">In This Section</span></span>

  - [<span data-ttu-id="be596-113">Журналы и файлы обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be596-113">Device Update logs and files in Lync Server 2013</span></span>](lync-server-2013-device-update-logs-and-files.md)

  - [<span data-ttu-id="be596-114">Правила обновления устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be596-114">Device Update rules in Lync Server 2013</span></span>](lync-server-2013-device-update-rules.md)

  - [<span data-ttu-id="be596-115">Параметры конфигурации обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be596-115">Device Update configuration settings in Lync Server 2013</span></span>](lync-server-2013-device-update-configuration-settings.md)

  - [<span data-ttu-id="be596-116">Просмотр обновлений программного обеспечения для устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be596-116">View software updates for devices in Lync Server 2013</span></span>](lync-server-2013-view-software-updates-for-devices-in-your-organization.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="be596-117">См. также</span><span class="sxs-lookup"><span data-stu-id="be596-117">See Also</span></span>


<span data-ttu-id="be596-118">[Инструменты и службы для управления устройствами и устранения неполадок](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span><span class="sxs-lookup"><span data-stu-id="be596-118">[Tools and Services for Managing and Troubleshooting Devices](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span></span>  
  

<span data-ttu-id="be596-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be596-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

