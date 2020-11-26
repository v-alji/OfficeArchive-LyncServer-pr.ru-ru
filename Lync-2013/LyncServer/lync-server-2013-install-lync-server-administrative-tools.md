---
title: 'Lync Server 2013: установка средств администрирования Lync Server'
description: 'Lync Server 2013: Установка средств администрирования Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server administrative tools
ms:assetid: 842b85e4-2eeb-464f-b1c1-ceb8cc04f8d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398665(v=OCS.15)
ms:contentKeyID: 48184695
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca1ad96299197c3339d06c4f094784edc632e6b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427196"
---
# <a name="install-lync-server-2013-administrative-tools"></a><span data-ttu-id="e73d6-103">Установка средств администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e73d6-103">Install Lync Server 2013 administrative tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e73d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e73d6-104">

<span> </span></span></span>

<span data-ttu-id="e73d6-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="e73d6-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="e73d6-106">В этой статье описано, как установить средства администрирования, которые необходимо использовать для развертывания Lync Server 2013 и управления ими.</span><span class="sxs-lookup"><span data-stu-id="e73d6-106">This topic describes how to install the administrative tools you need to use to deploy and manage Lync Server 2013.</span></span> <span data-ttu-id="e73d6-107">Средства администрирования устанавливаются по умолчанию на каждом сервере, работающем под управлением Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e73d6-107">The administrative tools are installed by default on each server running Lync Server 2013.</span></span> <span data-ttu-id="e73d6-108">Кроме того, вы можете установить средства администрирования на других компьютерах, таких как специальные консоли администрирования.</span><span class="sxs-lookup"><span data-stu-id="e73d6-108">Additionally, you can install the administrative tools on other computers, such as dedicated administrative consoles.</span></span> <span data-ttu-id="e73d6-109">Настоятельно рекомендуется установить средства администрирования на компьютере, который находится в том же домене или лесе, что и в составе сервера Lync Server 2013, который вы создаете, так как в этом случае вы убедитесь, что подготовительные действия для доменных служб Active Directory уже завершены, что позволит вам в дальнейшем использовать средства администрирования на этом компьютере для публикации топологии.</span><span class="sxs-lookup"><span data-stu-id="e73d6-109">We strongly recommend that you install the administrative tools on a computer that is in the same domain or forest as the Lync Server 2013 deployment you are creating because by doing so you make sure that Active Directory Domain Services preparation steps are already complete, which enables you to use the administrative tools on that computer later to publish your topology.</span></span>

<span data-ttu-id="e73d6-110">Убедитесь, что вы просматриваете требования инфраструктуры, операционной системы, программного обеспечения и прав администратора, прежде чем устанавливать или использовать средства администрирования Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e73d6-110">Make sure that you review infrastructure, operating system, software, and administrator rights requirements before you install or use the Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="e73d6-111">Сведения о требованиях к инфраструктуре описаны [в разделе Требования к инфраструктуре средств администрирования в Lync Server 2013](lync-server-2013-administrative-tools-infrastructure-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e73d6-111">For details about infrastructure requirements, see [Administrative tools infrastructure requirements in Lync Server 2013](lync-server-2013-administrative-tools-infrastructure-requirements.md).</span></span> <span data-ttu-id="e73d6-112">Сведения о требованиях к операционной системе и программному обеспечению для установки средств администрирования Lync Server 2013 можно найти [в разделе Поддержка серверов и инструментальных средств операционной системы в Lync server 2013](lync-server-2013-server-and-tools-operating-system-support.md), [Дополнительные требования к программному обеспечению для Lync Server 2013, дополнительные сведения о](lync-server-2013-additional-software-requirements.md) [поддержке и требованиях сервера в Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e73d6-112">For details about operating system and software requirements to install the Lync Server 2013 administrative tools, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md), [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md), and [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md).</span></span> <span data-ttu-id="e73d6-113">Подробные сведения о правах пользователей и разрешениях, необходимых для установки и использования средств, приведены в разделе [права и разрешения администратора, необходимые для настройки и администрирования Lync Server 2013](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md).</span><span class="sxs-lookup"><span data-stu-id="e73d6-113">For details about the user rights and permissions required to install and use the tools, see [Administrator rights and permissions required for setup and administration of Lync Server 2013](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e73d6-114">Если в вашей организации требуется найти службы IIS и все веб-службы на диске, отличном от системного, вы можете изменить путь к папке установки для файлов Lync Server в диалоговом окне Настройка.</span><span class="sxs-lookup"><span data-stu-id="e73d6-114">If your organization requires that you locate Internet Information Services (IIS) and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server files in the Setup dialog box.</span></span> <span data-ttu-id="e73d6-115">Если вы установили файлы установки по этому пути, включая OCSCore.msi, остальные файлы Lync Server 2013 будут развернуты на этом диске.</span><span class="sxs-lookup"><span data-stu-id="e73d6-115">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span>



</div>

<div>

## <a name="to-install-the-lync-server-2013-administrative-tools"></a><span data-ttu-id="e73d6-116">Установка средств администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e73d6-116">To install the Lync Server 2013 administrative tools</span></span>

1.  <span data-ttu-id="e73d6-117">Войдите в систему под учетной записью локального администратора (минимально требование) на компьютер, на котором вы хотите установить средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="e73d6-117">Log on as a local administrator (minimum requirement) to the computer where you want to install the administrative tools.</span></span> <span data-ttu-id="e73d6-118">Если вы вошли в операционную систему Windows Vista или Windows 7 с учетной записью обычного пользователя, то при включенном параметре UAC вам будет предложено указать локального администратора или имя пользователя и пароль, эквивалентные домену.</span><span class="sxs-lookup"><span data-stu-id="e73d6-118">If you are logged on as an a standard user on the Windows Vista or Windows 7 operating systems, and User Account Control (UAC) is enabled, you will be prompted for the local administrator or a domain equivalent user name and password.</span></span>

2.  <span data-ttu-id="e73d6-119">Найдите установочный носитель на компьютере, а затем дважды щелкните файл \\ Setup \\ \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="e73d6-119">Locate the installation media on your computer, and then double-click \\Setup\\amd64\\Setup.exe.</span></span>

3.  <span data-ttu-id="e73d6-120">Если вам будет предложено установить распространяемый компонент Microsoft Visual C++ 2008, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="e73d6-120">If you are prompted to install the Microsoft Visual C++ 2008 distributable, click **Yes**.</span></span>

4.  <span data-ttu-id="e73d6-121">На странице **Microsoft Lync Server 2013, расположенной по пути установки** , нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e73d6-121">On the **Microsoft Lync Server 2013 Installation Location** page, click **OK**.</span></span> <span data-ttu-id="e73d6-122">Если вы хотите, чтобы файлы были установлены в другое место, измените этот путь на другое место или на диск.</span><span class="sxs-lookup"><span data-stu-id="e73d6-122">Change this path to another location or drive if you need to have the files installed to another location.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e73d6-123">Если для организации требуется найти службы IIS и все веб-службы на диске, отличном от системного, вы можете изменить путь к папке установки для файлов Lync Server 2013 в диалоговом окне Настройка.</span><span class="sxs-lookup"><span data-stu-id="e73d6-123">If your organization requires that you locate Internet Information Services (IIS) and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box.</span></span> <span data-ttu-id="e73d6-124">Если вы установили файлы установки по этому пути, включая OCSCore.msi, остальные файлы Lync Server 2013 будут развернуты на этом диске.</span><span class="sxs-lookup"><span data-stu-id="e73d6-124">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive too.</span></span>

    
    </div>

5.  <span data-ttu-id="e73d6-125">На странице Лицензионное **соглашение конечного пользователя** ознакомьтесь с условиями лицензионного соглашения, нажмите кнопку **я принимаю**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e73d6-125">On the **End User License Agreement** page, review the license terms, click **I accept**, and then click **OK**.</span></span> <span data-ttu-id="e73d6-126">Чтобы продолжить, необходимо выполнить это действие.</span><span class="sxs-lookup"><span data-stu-id="e73d6-126">This step is required before you can continue.</span></span>

6.  <span data-ttu-id="e73d6-127">На странице **мастера развертывания Microsoft Lync Server 2013 —** **Установка средств администрирования**.</span><span class="sxs-lookup"><span data-stu-id="e73d6-127">On the **Microsoft Lync Server 2013 – Deployment Wizard** page, click **Install Administrator Tools**.</span></span>

7.  <span data-ttu-id="e73d6-128">Когда установка завершится успешно, нажмите кнопку **выход**.</span><span class="sxs-lookup"><span data-stu-id="e73d6-128">When the installation successfully completes, click **Exit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e73d6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e73d6-129">See Also</span></span>


[<span data-ttu-id="e73d6-130">Открытие меню администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e73d6-130">Open Lync Server 2013 administrative tools</span></span>](lync-server-2013-open-lync-server-administrative-tools.md)  


[<span data-ttu-id="e73d6-131">Средства администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e73d6-131">Lync Server 2013 administrative tools</span></span>](lync-server-2013-lync-server-administrative-tools.md)  
  

<span data-ttu-id="e73d6-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e73d6-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

