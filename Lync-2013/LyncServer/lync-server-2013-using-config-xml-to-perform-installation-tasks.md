---
title: 'Lync Server 2013: использование Config.xml для выполнения задач установки'
description: 'Lync Server 2013: использование Config.xml для выполнения задач установки.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Config.xml to perform installation tasks
ms:assetid: 0813184a-ab40-417c-b3a3-c2090766b831
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204651(v=OCS.15)
ms:contentKeyID: 48183332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22fff14e21a120c3a0ee2cd6432fd1eba2bbee5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438955"
---
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a><span data-ttu-id="8bce1-103">Использование Config.xml для выполнения задач установки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8bce1-103">Using Config.xml to perform installation tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8bce1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8bce1-104">

<span> </span></span></span>

<span data-ttu-id="8bce1-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="8bce1-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="8bce1-p101">Хотя Центр развертывания Office является основным средством настраиваемой установки, администраторы могут использовать файл Config.xml, чтобы задать для установки дополнительные инструкции, недоступные в Центре развертывания Office. Следующие настройки выполнимы только с помощью файла Config.xml:</span><span class="sxs-lookup"><span data-stu-id="8bce1-p101">Although the Office Customization Tool (OCT) is the primary tool for customization installation, administrators can use the Config.xml file to specify additional installation instructions that are not available in the OCT. The following customizations can only be made by using the Config.xml file:</span></span>

  - <span data-ttu-id="8bce1-108">задание пути для точки сетевой установки;</span><span class="sxs-lookup"><span data-stu-id="8bce1-108">Specify the path of the network installation point.</span></span>

  - <span data-ttu-id="8bce1-109">выбор устанавливаемых продуктов;</span><span class="sxs-lookup"><span data-stu-id="8bce1-109">Select the products to install.</span></span>

  - <span data-ttu-id="8bce1-110">настройка ведения журнала и местоположения файла настроек установки и обновлений ПО;</span><span class="sxs-lookup"><span data-stu-id="8bce1-110">Configure logging and the location of the Setup customization file and software updates.</span></span>

  - <span data-ttu-id="8bce1-111">задание параметров установки, таких как имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="8bce1-111">Specify installation options, such as user name.</span></span>

  - <span data-ttu-id="8bce1-112">копирование локального источника установки на компьютер пользователя без установки Office;</span><span class="sxs-lookup"><span data-stu-id="8bce1-112">Copy the local installation source (LIS) to the user's computer without installing Office.</span></span>

  - <span data-ttu-id="8bce1-113">добавление и удаления языков из установки.</span><span class="sxs-lookup"><span data-stu-id="8bce1-113">Add or remove languages from the installation.</span></span>

<span data-ttu-id="8bce1-114">Для настройки автоматической установки Lync 2013 рекомендуется использовать файл Config.xml.</span><span class="sxs-lookup"><span data-stu-id="8bce1-114">We recommend that you use the Config.xml file to configure Lync 2013 silent installation.</span></span>

<span data-ttu-id="8bce1-115">По умолчанию файл Config.xml, хранящийся в основной папке продукта (например, \\ Product. WW) направляет настройку для установки этого продукта.</span><span class="sxs-lookup"><span data-stu-id="8bce1-115">By default, the Config.xml file that is stored in the core product folder (for example, \\product.WW) directs Setup to install that product.</span></span> <span data-ttu-id="8bce1-116">Например, файл Config.xml в следующей папке устанавливает Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="8bce1-116">For example, the Config.xml file in the following folder installs Lync 2013:</span></span>

  - <span data-ttu-id="8bce1-117">\\\\\\общий доступ к серверу \\ Lync15 \\ Lync. WW \\Config.xml</span><span class="sxs-lookup"><span data-stu-id="8bce1-117">\\\\server\\share\\Lync15\\Lync.WW \\Config.xml</span></span>

<span data-ttu-id="8bce1-118">Элементы Config.xml, наиболее часто используемые при установке Lync 2013, перечислены в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8bce1-118">The Config.xml elements most commonly used for Lync 2013 installation are listed in the following table.</span></span>

### <a name="configxml-elements"></a><span data-ttu-id="8bce1-119">Элементы Config.xml</span><span class="sxs-lookup"><span data-stu-id="8bce1-119">Config.xml elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8bce1-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="8bce1-120">Element</span></span></th>
<th><span data-ttu-id="8bce1-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8bce1-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bce1-122">Configuration</span><span class="sxs-lookup"><span data-stu-id="8bce1-122">Configuration</span></span></p></td>
<td><p><span data-ttu-id="8bce1-123">Элемент верхнего уровня (обязательно).</span><span class="sxs-lookup"><span data-stu-id="8bce1-123">Top-level element (required).</span></span> <span data-ttu-id="8bce1-124">Имеет атрибут Product, например: Product = Lync</span><span class="sxs-lookup"><span data-stu-id="8bce1-124">Contains the Product attribute, for example: Product=Lync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bce1-125">OptionState</span><span class="sxs-lookup"><span data-stu-id="8bce1-125">OptionState</span></span></p></td>
<td><p><span data-ttu-id="8bce1-126">Определяет, как при установке будут обрабатываться компоненты конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="8bce1-126">Specifies how specific product features are handled during installation.</span></span> <span data-ttu-id="8bce1-127">Следующие атрибуты используются для предотвращения установки служб Business Connectivity Services, включая общие компоненты, которые мешают работе Outlook 2010:</span><span class="sxs-lookup"><span data-stu-id="8bce1-127">Use the following attributes to prevent installation of Business Connectivity Services, which includes shared components that interfere with Outlook 2010:</span></span></p>
<ul>
<li><p><span data-ttu-id="8bce1-128">ID = &quot; LOBiMain&quot;</span><span class="sxs-lookup"><span data-stu-id="8bce1-128">Id=&quot;LOBiMain&quot;</span></span></p></li>
<li><p><span data-ttu-id="8bce1-129">Штат = &quot; отсутствует&quot;</span><span class="sxs-lookup"><span data-stu-id="8bce1-129">State=&quot;Absent&quot;</span></span></p></li>
<li><p><span data-ttu-id="8bce1-130">Дочерние элементы = &quot; Force&quot;</span><span class="sxs-lookup"><span data-stu-id="8bce1-130">Children=&quot;Force&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bce1-131">Display</span><span class="sxs-lookup"><span data-stu-id="8bce1-131">Display</span></span></p></td>
<td><p><span data-ttu-id="8bce1-p105">Уровень пользовательского интерфейса, отображаемого пользователю программой установки. Обычно используются следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="8bce1-p105">The level of UI that Setup displays to the user. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8bce1-134">CompletionNotice = &quot; Да &quot;  |  &quot; нет &quot; (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bce1-134">CompletionNotice=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
<li><p><span data-ttu-id="8bce1-135">Атрибута AcceptEULA = &quot; Да &quot;  |  &quot; нет &quot; (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bce1-135">AcceptEula=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bce1-136">Logging</span><span class="sxs-lookup"><span data-stu-id="8bce1-136">Logging</span></span></p></td>
<td><p><span data-ttu-id="8bce1-p106">Параметры ведения журнала программой установки. Обычно используются следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="8bce1-p106">Options for the kind of logging that Setup performs. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8bce1-139">Type = &quot; Off &quot;  |  &quot; Standard &quot; (по умолчанию) | &quot; Подробный&quot;</span><span class="sxs-lookup"><span data-stu-id="8bce1-139">Type =&quot;Off&quot; | &quot;Standard&quot;(default) | &quot;Verbose&quot;</span></span></p></li>
<li><p><span data-ttu-id="8bce1-140">Template="filename.txt" (имя файла журнала)</span><span class="sxs-lookup"><span data-stu-id="8bce1-140">Template=”filename.txt” (the name of the log file)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bce1-141">Setting</span><span class="sxs-lookup"><span data-stu-id="8bce1-141">Setting</span></span></p></td>
<td><p><span data-ttu-id="8bce1-p107">Определяет значения для свойств программы установщика Windows. Обычно используются следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="8bce1-p107">Specifies values for Windows Installer properties. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8bce1-144">Параметр ID = &quot; Name &quot; (имя свойства установщика Windows)</span><span class="sxs-lookup"><span data-stu-id="8bce1-144">Setting Id=&quot;name&quot; (the name of the Windows Installer property)</span></span></p></li>
<li><p><span data-ttu-id="8bce1-145">Value = &quot; value &quot; (значение, которое нужно присвоить свойству)</span><span class="sxs-lookup"><span data-stu-id="8bce1-145">Value=&quot;value&quot; (the value to assign to the property)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bce1-146">DistributionPoint</span><span class="sxs-lookup"><span data-stu-id="8bce1-146">DistributionPoint</span></span></p></td>
<td><p><span data-ttu-id="8bce1-p108">Полный доменный путь точки сетевой установки, из которой запускается установка. Содержит атрибут Location:</span><span class="sxs-lookup"><span data-stu-id="8bce1-p108">The fully qualified path of the network installation point from which the installation is to run. Includes the Location attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="8bce1-149">Location="path"</span><span class="sxs-lookup"><span data-stu-id="8bce1-149">Location=”path”</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8bce1-150">В следующем примере показан файл Config.xml для типичной автоматической установки Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="8bce1-150">The following example shows a Config.xml file for a typical silent installation of Lync 2013.</span></span>

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

<span data-ttu-id="8bce1-151">Подробные сведения об использовании файла Config.xml для выполнения задач по установке и сопровождению Office можно найти по адресу <https://go.microsoft.com/fwlink/p/?linkid=267514> .</span><span class="sxs-lookup"><span data-stu-id="8bce1-151">Detailed information about using the Config.xml file to perform Office installation and maintenance tasks is available at <https://go.microsoft.com/fwlink/p/?linkid=267514>.</span></span>

<div>

## <a name="to-customize-the-configxml-file"></a><span data-ttu-id="8bce1-152">Изменение файла Config.xml</span><span class="sxs-lookup"><span data-stu-id="8bce1-152">To customize the Config.xml file</span></span>

1.  <span data-ttu-id="8bce1-153">Откройте файл Config.xml с помощью текстового редактора, такого как "Блокнот".</span><span class="sxs-lookup"><span data-stu-id="8bce1-153">Open the Config.xml file by using a text editor tool, such as Notepad.</span></span>

2.  <span data-ttu-id="8bce1-154">Найдите строки, содержащие элементы, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="8bce1-154">Locate the lines that contain the elements you want to change.</span></span>

3.  <span data-ttu-id="8bce1-155">Измените запись для элемента, используя нужные значения параметров автоматической установки.</span><span class="sxs-lookup"><span data-stu-id="8bce1-155">Modify the element entry with the silent options that you want to use.</span></span> <span data-ttu-id="8bce1-156">Убедитесь, что вы удалите разделители комментариев, " \<\!--" and "--\> ".</span><span class="sxs-lookup"><span data-stu-id="8bce1-156">Make sure that you remove the comment delimiters, "\<\!--" and "--\>".</span></span> <span data-ttu-id="8bce1-157">Например, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="8bce1-157">For example, use the following syntax:</span></span>
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  <span data-ttu-id="8bce1-158">Сохраните файл Config.xml.</span><span class="sxs-lookup"><span data-stu-id="8bce1-158">Save the Config.xml file.</span></span>

<span data-ttu-id="8bce1-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8bce1-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

