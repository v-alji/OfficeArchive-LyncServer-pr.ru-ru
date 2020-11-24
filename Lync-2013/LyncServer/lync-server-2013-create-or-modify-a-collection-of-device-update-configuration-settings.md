---
title: Создание или изменение коллекции параметров конфигурации центра обновления устройства
description: Создание или изменение коллекции параметров конфигурации центра обновления устройства.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of Device Update configuration settings
ms:assetid: 3e8ce95f-a8c8-417c-b1f7-0f759a567aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994029(v=OCS.15)
ms:contentKeyID: 51803938
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593a1a0cb0f68254748ee48440cda18c78989780
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398779"
---
# <a name="create-or-modify-a-collection-of-device-update-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="2b019-103">Создание или изменение коллекции параметров конфигурации обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b019-103">Create or modify a collection of Device Update configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b019-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b019-104">

<span> </span></span></span>

<span data-ttu-id="2b019-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="2b019-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="2b019-106">Параметры конфигурации обновления устройства можно создать (только на уровне сайта) с помощью Windows PowerShell и командлета **New-CsDeviceUpdateConfiguration** , а затем изменить с помощью командлета **Set-CsDeviceUpdateConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="2b019-106">Device update configuration settings can be created (at the site scope only) by using Windows PowerShell and the **New-CsDeviceUpdateConfiguration** cmdlet and modified by using the **Set-CsDeviceUpdateConfiguration** cmdlet.</span></span> <span data-ttu-id="2b019-107">Эти командлеты можно запускать либо из командной консоли Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b019-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="2b019-108">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="2b019-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="to-create-device-update-configuration-settings-that-use-the-default-values"></a><span data-ttu-id="2b019-109">Создание параметров конфигурации обновления устройства, использующих значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2b019-109">To create device update configuration settings that use the default values</span></span>

  - <span data-ttu-id="2b019-110">Эта команда создает новый набор параметров конфигурации обновления устройства для сайта Redmond.</span><span class="sxs-lookup"><span data-stu-id="2b019-110">This command creates a new set of device update configuration settings for the Redmond site:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond"
    
    <span data-ttu-id="2b019-111">Поскольку в предыдущей команде не указаны никакие параметры, кроме обязательных параметров, Новая коллекция параметров конфигурации будет использовать значения по умолчанию для всех его свойств.</span><span class="sxs-lookup"><span data-stu-id="2b019-111">Because no parameters other than the mandatory Identity parameter were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span>

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-device-update-configuration-settings"></a><span data-ttu-id="2b019-112">Изменение значения отдельного свойства при создании параметров конфигурации обновления устройства</span><span class="sxs-lookup"><span data-stu-id="2b019-112">To change a single property value when creating device update configuration settings</span></span>

  - <span data-ttu-id="2b019-113">Чтобы создать параметры, использующие другие значения свойств, просто включите соответствующий параметр и его значение.</span><span class="sxs-lookup"><span data-stu-id="2b019-113">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="2b019-114">Например, чтобы создать коллекцию параметров конфигурации обновления для устройств, которые по умолчанию удаляют старые файлы журнала каждые 21 дня, используйте команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="2b019-114">For example, to create a collection of device update configuration settings that, by default, deletes old log files every 21 days, use a command like this one:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00"

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-device-update-configuration-settings"></a><span data-ttu-id="2b019-115">Изменение нескольких значений свойства при создании параметров конфигурации обновления устройства</span><span class="sxs-lookup"><span data-stu-id="2b019-115">To change multiple property values when creating device update configuration settings</span></span>

  - <span data-ttu-id="2b019-116">Чтобы изменить несколько значений свойств, можно включить несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="2b019-116">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="2b019-117">Например, эта команда задает для интервала очистки журнала значение 21 дня, а интервал сброса журнала — 30 минут.</span><span class="sxs-lookup"><span data-stu-id="2b019-117">For example, this command sets the log cleanup interval to 21 days and the log flush interval to 30 minutes:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00" -LogFlushInterval "00:30:00"

</div>

<span data-ttu-id="2b019-118">Подробнее об изменении существующих параметров конфигурации устройств можно узнать в разделе справки по командлету [Set-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg398320(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="2b019-118">For details about modifying existing device configuration settings, see the Help topic for the [Set-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg398320(v=OCS.15)) cmdlet.</span></span> <span data-ttu-id="2b019-119">Дополнительные сведения о создании коллекций параметров конфигурации можно найти в разделе справки для командлета [New-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg425761(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="2b019-119">For details about creating collections of configuration settings, see the Help topic for the [New-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg425761(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="2b019-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b019-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

