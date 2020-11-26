---
title: 'Lync Server 2013: Настройка параметров диапазона портов мультимедиа'
description: 'Lync Server 2013: Настройка параметров диапазона портов мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring media port range settings
ms:assetid: 2c4b7c0b-0dce-48f4-a489-336d6e526f7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204770(v=OCS.15)
ms:contentKeyID: 48183723
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a7670284c593197068c366f43bbb3faaaad8f63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432915"
---
# <a name="configuring-media-port-range-settings-in-lync-server-2013"></a><span data-ttu-id="cf744-103">Настройка параметров диапазона портов мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf744-103">Configuring media port range settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf744-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf744-104">

<span> </span></span></span>

<span data-ttu-id="cf744-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="cf744-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="cf744-106">Параметры диапазона портов мультимедиа могут значительно повлиять на производительность клиента и должны настраиваться.</span><span class="sxs-lookup"><span data-stu-id="cf744-106">Media port range settings can significantly impact client performance and should be configured.</span></span> <span data-ttu-id="cf744-107">Эти параметры можно настроить с помощью командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="cf744-107">You can configure these settings by using Lync Server Management Shell.</span></span>

### <a name="media-port-range-settings"></a><span data-ttu-id="cf744-108">Параметры диапазона портов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cf744-108">Media Port Range Settings</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf744-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="cf744-109">Setting</span></span></th>
<th><span data-ttu-id="cf744-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cf744-110">Description</span></span></th>
<th><span data-ttu-id="cf744-111">Командлет командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="cf744-111">Lync Server Management Shell cmdlet</span></span></th>
<th><span data-ttu-id="cf744-112">Параметры командлета</span><span class="sxs-lookup"><span data-stu-id="cf744-112">Cmdlet parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf744-113">Portrange\Enabled</span><span class="sxs-lookup"><span data-stu-id="cf744-113">Portrange\Enabled</span></span></p></td>
<td><p><span data-ttu-id="cf744-114">Указывает, следует ли использовать для мультимедиа и сигналов диапазоны портов, отправленные сервером.</span><span class="sxs-lookup"><span data-stu-id="cf744-114">Specifies whether the port ranges sent by the server should be used by the client for media and signaling.</span></span> <span data-ttu-id="cf744-115">Используется вместе с подзначениями MinMediaPort и MaxMediaPort.</span><span class="sxs-lookup"><span data-stu-id="cf744-115">Used in conjunction with the subvalues MinMediaPort and MaxMediaPort.</span></span></p></td>
<td><p><span data-ttu-id="cf744-116"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="cf744-116"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="cf744-117">ClientMediaPortRangeEnabled</span><span class="sxs-lookup"><span data-stu-id="cf744-117">ClientMediaPortRangeEnabled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf744-118">Portrange\MinMediaPort</span><span class="sxs-lookup"><span data-stu-id="cf744-118">Portrange\MinMediaPort</span></span></p></td>
<td><p><span data-ttu-id="cf744-119">Задает начальный номер порта, который будет использоваться для мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cf744-119">Specifies the starting port number to use for media.</span></span> <span data-ttu-id="cf744-120">Объединяется с MaxMediaPort, чтобы указать диапазон портов.</span><span class="sxs-lookup"><span data-stu-id="cf744-120">Combines with MaxMediaPort to specify the range of ports.</span></span> <span data-ttu-id="cf744-121">Рекомендуемый минимальный диапазон составляет 40 портов.</span><span class="sxs-lookup"><span data-stu-id="cf744-121">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="cf744-122"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="cf744-122"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="cf744-123">ClientMediaPort (представляет начальный номер порта, используемый для мультимедиа клиента).</span><span class="sxs-lookup"><span data-stu-id="cf744-123">ClientMediaPort (represents the starting port number to use for client media)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf744-124">Portrange\MaxMediaPort</span><span class="sxs-lookup"><span data-stu-id="cf744-124">Portrange\MaxMediaPort</span></span></p></td>
<td><p><span data-ttu-id="cf744-125">Указывает самый высокий номер порта, который будет использоваться для мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cf744-125">Specifies the highest port number to use for media.</span></span> <span data-ttu-id="cf744-126">Объединяется с MinMediaPort, чтобы указать диапазон портов.</span><span class="sxs-lookup"><span data-stu-id="cf744-126">Combines with MinMediaPort to specify the range of ports.</span></span> <span data-ttu-id="cf744-127">Рекомендуемый минимальный диапазон составляет 40 портов.</span><span class="sxs-lookup"><span data-stu-id="cf744-127">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="cf744-128"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="cf744-128"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="cf744-129">ClientMediaPortRange (указывает общее количество портов, доступных для клиентского носителя; значение по умолчанию — 40).</span><span class="sxs-lookup"><span data-stu-id="cf744-129">ClientMediaPortRange (indicates the total number of ports available for client media; default is 40)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-media-port-range-settings"></a><span data-ttu-id="cf744-130">Настройка параметров диапазона портов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cf744-130">To Configure Media Port Range Settings</span></span>

1.  <span data-ttu-id="cf744-131">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="cf744-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="cf744-132">Выполнить следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="cf744-132">Run the following cmdlet:</span></span>
    
        Get-CsConferencingConfiguration
    
    <span data-ttu-id="cf744-133">Этот командлет возвращает параметры конфигурации Конференции.</span><span class="sxs-lookup"><span data-stu-id="cf744-133">This cmdlet returns the conferencing configuration settings.</span></span>

3.  <span data-ttu-id="cf744-134">Выполните следующий командлет с параметрами и значениями, которые вы хотите изменить (Дополнительные сведения о параметрах этого командлета можно найти в документации на Lync Server Management Shell).</span><span class="sxs-lookup"><span data-stu-id="cf744-134">Run the following cmdlet with the parameters and values you want to change (for details about the parameters for this cmdlet, see the Lync Server Management Shell documentation):</span></span>
    
        Set-CsConferencingConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cf744-135">Вы можете создавать дополнительные наборы параметров настройки конференц-связи для определенных сайтов.</span><span class="sxs-lookup"><span data-stu-id="cf744-135">You can create additional sets of conferencing configuration settings for specific sites.</span></span> <span data-ttu-id="cf744-136">Используйте командлет <STRONG>New-CsConferencingConfiguration</STRONG> с удостоверением сайта.</span><span class="sxs-lookup"><span data-stu-id="cf744-136">Use the <STRONG>New- CsConferencingConfiguration</STRONG> cmdlet with a site identity.</span></span> <span data-ttu-id="cf744-137">При создании новых параметров конфигурации конференций для сайтов параметры сайта имеют приоритет над глобальными параметрами.</span><span class="sxs-lookup"><span data-stu-id="cf744-137">When you create new conferencing configuration settings for sites, the site settings take precedence over the global settings.</span></span> <span data-ttu-id="cf744-138">Подробные сведения можно найти в руководстве по среде Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="cf744-138">For details, see the Lync Server Management Shell documentation.</span></span>

    
    <span data-ttu-id="cf744-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf744-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

