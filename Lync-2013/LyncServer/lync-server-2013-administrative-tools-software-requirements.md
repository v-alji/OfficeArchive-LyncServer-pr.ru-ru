---
title: 'Lync Server 2013: программные требования для средств администрирования'
description: 'Lync Server 2013: требования к программному обеспечению для администрирования.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administrative tools software requirements
ms:assetid: 2fb172c3-7b84-4e49-981c-2a17e7a00a29
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg195653(v=OCS.15)
ms:contentKeyID: 48183740
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0c723d56cbda0c171fab206e3bcd3b2da0cc5b4b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398005"
---
# <a name="administrative-tools-software-requirements-in-lync-server-2013"></a><span data-ttu-id="8c80e-103">Программные требования для средств администрирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c80e-103">Administrative tools software requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c80e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c80e-104">

<span> </span></span></span>

<span data-ttu-id="8c80e-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="8c80e-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="8c80e-106">В этой статье описывается программное обеспечение, необходимое для установки и использования средств администрирования Lync Server 2013 в дополнение к требованиям к операционной системе.</span><span class="sxs-lookup"><span data-stu-id="8c80e-106">This topic describes the software required to install and use Lync Server 2013 administrative tools in addition to the operating system requirements.</span></span>

<div>

## <a name="microsoft-net-framework-45"></a><span data-ttu-id="8c80e-107">Платформа Microsoft .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="8c80e-107">Microsoft .NET Framework 4.5</span></span>

<span data-ttu-id="8c80e-108">Для Lync Server 2013 требуется 64-разрядная версия Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="8c80e-108">The 64-bit edition of Microsoft .NET Framework 4.5 is required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="windows-powershell-30"></a><span data-ttu-id="8c80e-109">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="8c80e-109">Windows PowerShell 3.0</span></span>

<span data-ttu-id="8c80e-110">Windows PowerShell 3,0 необходима для работы любого компонента Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8c80e-110">Windows PowerShell 3.0 is required for running any component of Microsoft Lync Server 2013.</span></span> <span data-ttu-id="8c80e-111">Дополнительные сведения можно найти в разделе [Установка Windows PowerShell 3,0 для Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="8c80e-111">For more information, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

</div>

<div>

## <a name="windows-installer-version-45"></a><span data-ttu-id="8c80e-112">Установщик Windows версии 4,5</span><span class="sxs-lookup"><span data-stu-id="8c80e-112">Windows Installer Version 4.5</span></span>

<span data-ttu-id="8c80e-113">Lync Server 2013 использует технологию установщика Windows для установки, удаления и обслуживания различных ролей сервера.</span><span class="sxs-lookup"><span data-stu-id="8c80e-113">Lync Server 2013 uses Windows Installer technology to install, uninstall, and maintain various server roles.</span></span> <span data-ttu-id="8c80e-114">Установщик Windows версии 4,5 можно использовать в качестве распространяемого компонента для операционной системы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8c80e-114">Windows Installer version 4.5 is available as a redistributable component for the Windows Server operating system.</span></span> <span data-ttu-id="8c80e-115">Установщик Windows 4,5 поставляется с Windows Server 2012 R2, Windows Server 2012 и Windows Server 2008 R2 означает, что вам не нужно загружать служебную программу для любого компьютера, на котором работает Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8c80e-115">Windows Installer 4.5 ships with Windows Server 2012 R2, Windows Server 2012, and Windows Server 2008 R2 meaning that you do not need to download the utility for any computer that is running Lync Server 2013.</span></span> <span data-ttu-id="8c80e-116">(Lync Server 2013 можно установить только на компьютерах под управлением Windows Server 2012 R2, Windows Server 2012 или Windows Server 2008 R2.)</span><span class="sxs-lookup"><span data-stu-id="8c80e-116">(Lync Server 2013 can only be installed on computers running Windows Server 2012 R2, Windows Server 2012 or Windows Server 2008 R2.)</span></span>

<span data-ttu-id="8c80e-117">Тем не менее, если вы хотите установить консоль управления Lync Server или построитель топологии Lync Server на рабочей станции администратора, вам может потребоваться загрузить установщик Windows 4,5.</span><span class="sxs-lookup"><span data-stu-id="8c80e-117">However, if you want to install Lync Server Management Shell or Lync Server Topology Builder on an administrator workstation you might need to download Windows Installer 4.5.</span></span> <span data-ttu-id="8c80e-118">Эта служебная программа поставляется в Windows 7 и Windows 2008 R2, но не в предыдущих версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="8c80e-118">That utility ships with Windows 7 and Windows 2008 R2 but not with any previous versions of the Windows operating system.</span></span> <span data-ttu-id="8c80e-119">Вы можете скачать установщик Windows 4,5 из центра загрузки Майкрософт по адресу <https://go.microsoft.com/fwlink/p/?linkid=197395> .</span><span class="sxs-lookup"><span data-stu-id="8c80e-119">You can download Windows Installer 4.5 from the Microsoft Download Center at <https://go.microsoft.com/fwlink/p/?linkid=197395>.</span></span>

</div>

<div>

## <a name="microsoft-silverlight-5-browser-plug-in"></a><span data-ttu-id="8c80e-120">Подключаемый модуль браузера Microsoft Silverlight 5</span><span class="sxs-lookup"><span data-stu-id="8c80e-120">Microsoft Silverlight 5 browser plug-in</span></span>

<span data-ttu-id="8c80e-121">Панель управления Lync Server 2013 — это веб-инструмент, и необходимо установить последнюю версию подключаемого модуля браузера Microsoft Silverlight 5.</span><span class="sxs-lookup"><span data-stu-id="8c80e-121">Lync Server 2013 Control Panel is a web-based tool and requires that you install the latest version of Microsoft Silverlight 5 browser plug-in.</span></span> <span data-ttu-id="8c80e-122">Если вы запускаете панель управления Lync Server 2013, если это программное обеспечение не установлено или если установлено более ранняя версия, откроется панель управления Lync Server 2013 с предложением установить требуемую версию.</span><span class="sxs-lookup"><span data-stu-id="8c80e-122">When you start Lync Server 2013 Control Panel, if this software is not installed or if an earlier version is installed, Lync Server 2013 Control Panel prompts you to install the required version.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8c80e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8c80e-123">See Also</span></span>


[<span data-ttu-id="8c80e-124">Поддержка сервера и средств в операционной системе в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c80e-124">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)  


[<span data-ttu-id="8c80e-125">Требования к инфраструктуре средств администрирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c80e-125">Administrative tools infrastructure requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-infrastructure-requirements.md)  
[<span data-ttu-id="8c80e-126">Административные права и разрешения, необходимые для установки и администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c80e-126">Administrator rights and permissions required for setup and administration of Lync Server 2013</span></span>](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md)  
  

<span data-ttu-id="8c80e-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c80e-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

