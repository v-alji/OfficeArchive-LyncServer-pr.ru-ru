---
title: 'Lync Server 2013: Настройка установки клиента'
description: 'Lync Server 2013: Настройка установки клиента.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Customizing client installation
ms:assetid: 5c1a85f1-5ebb-48fb-acb7-3bf46decbf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204934(v=OCS.15)
ms:contentKeyID: 48184254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8dd1942c298ccbc8b6a2950baf4f24cc2f797a92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431374"
---
# <a name="customizing-client-installation-in-lync-server-2013"></a><span data-ttu-id="7bb66-103">Настройка установки клиента в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bb66-103">Customizing client installation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7bb66-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7bb66-104">

<span> </span></span></span>

<span data-ttu-id="7bb66-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="7bb66-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="7bb66-106">Администраторы предприятий могут настроить установку Office 2013 на базе установщика Windows (MSI-файла) с помощью описанных в этом разделе способов.</span><span class="sxs-lookup"><span data-stu-id="7bb66-106">Enterprise administrators can customize the Office 2013 Windows Installer-based (.msi) installation by using the methods discussed in this section.</span></span> <span data-ttu-id="7bb66-107">Так как ни один из средств не предоставляет никаких вариантов настройки, скорее всего, вы будете использовать сочетание этих методов в развертывании Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7bb66-107">Because no single tool provides all customization options, you’ll likely use a combination of these methods in your Lync 2013 deployment.</span></span> <span data-ttu-id="7bb66-108">Как минимум, вы можете использовать инструменты, описанные в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7bb66-108">At a minimum, you might use the tools described in the following sections:</span></span>

  - <span data-ttu-id="7bb66-109">[С помощью средства развертывания Office (OCT) в Lync Server 2013](lync-server-2013-using-the-office-customization-tool-oct.md) вы можете настроить параметры и функции настройки для Lync и других программ Office.</span><span class="sxs-lookup"><span data-stu-id="7bb66-109">[Using the Office Customization Tool (OCT) in Lync Server 2013](lync-server-2013-using-the-office-customization-tool-oct.md) to customize setup options and features for Lync and other Office programs.</span></span>

  - <span data-ttu-id="7bb66-110">[С помощью Config.xml можно выполнять задачи установки в Lync Server 2013](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) , чтобы указать путь к точке сетевой установки и выполнить автоматическую установку.</span><span class="sxs-lookup"><span data-stu-id="7bb66-110">[Using Config.xml to perform installation tasks in Lync Server 2013](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) to specify the path of the network installation point and perform silent installation.</span></span>

  - <span data-ttu-id="7bb66-111">[Использование параметров командной строки программы установки в Lync Server 2013](lync-server-2013-using-setup-command-line-options.md) для указания файла Config.xml для использования во время установки.</span><span class="sxs-lookup"><span data-stu-id="7bb66-111">[Using Setup command-line options in Lync Server 2013](lync-server-2013-using-setup-command-line-options.md) to specify the Config.xml file to use during installation.</span></span>

  - <span data-ttu-id="7bb66-112">[Настройка политик начальной настройки клиента в Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) с помощью оснастки MMC "Редактор объектов групповой политики".</span><span class="sxs-lookup"><span data-stu-id="7bb66-112">[Configuring client bootstrapping policies in Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) by using the Group Policy Object Editor MMC snap-in.</span></span>

<span data-ttu-id="7bb66-113">Скорее всего, будут другие параметры, которые нужно будет настроить при развертывании пакета продуктов Office.</span><span class="sxs-lookup"><span data-stu-id="7bb66-113">There will probably be other options you’ll want to configure as you deploy the Office suite of products.</span></span> <span data-ttu-id="7bb66-114">В этом разделе представлены общие сведения о средствах настройки и обсуждаются вопросы, связанные с Lync.</span><span class="sxs-lookup"><span data-stu-id="7bb66-114">The topics in this section give an overview of these customization tools and discuss Lync-specific considerations.</span></span> <span data-ttu-id="7bb66-115">Здесь предоставляются ссылки на подробную справку Office по каждому средству.</span><span class="sxs-lookup"><span data-stu-id="7bb66-115">Included are links to detailed Office help for each tool.</span></span>

<span data-ttu-id="7bb66-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7bb66-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

