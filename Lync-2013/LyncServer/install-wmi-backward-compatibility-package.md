---
title: Установка пакета обратной совместимости WMI
description: Установка пакета обратной совместимости WMI.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439584"
---
# <a name="install-wmi-backward-compatibility-package"></a><span data-ttu-id="04118-103">Установка пакета обратной совместимости WMI</span><span class="sxs-lookup"><span data-stu-id="04118-103">Install WMI Backward Compatibility package</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04118-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04118-104">

<span> </span></span></span>

<span data-ttu-id="04118-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="04118-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="04118-106">Если вы попытаетесь запустить мастер слияния построителя топологии без установки пакета обратной совместимости WMI, появится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="04118-106">If you attempt to run the Topology Builder Merge wizard without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="04118-107">![Сообщение об ошибке WMI](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "Сообщение об ошибке WMI")</span><span class="sxs-lookup"><span data-stu-id="04118-107">![WMI error message](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI error message")</span></span>

<span data-ttu-id="04118-108">При попытке выполнить командлет **Merge-CsLegacytopology** без установки пакета обратной совместимости WMI появляется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="04118-108">If you attempt to run the **Merge-CsLegacytopology** cmdlet without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="04118-109">![Ошибка поставщика Windows PowerShell WMI](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Ошибка поставщика Windows PowerShell WMI")</span><span class="sxs-lookup"><span data-stu-id="04118-109">![Windows PowerShell WMI Provider Error](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI Provider Error")</span></span>

<span data-ttu-id="04118-110">Установка пакета обратной совместимости WMI</span><span class="sxs-lookup"><span data-stu-id="04118-110">To install the WMI Backward Compatibility Package</span></span>

1.  <span data-ttu-id="04118-111">С установочного носителя перейдите в раздел \\ настройка \\ \\OCSWMIBC.MSI установки amd64 \\ .</span><span class="sxs-lookup"><span data-stu-id="04118-111">From your installation media, navigate to \\SETUP\\AMD64\\SETUP\\OCSWMIBC.MSI.</span></span>

2.  <span data-ttu-id="04118-112">Установите OCSWMIBC.MSI.</span><span class="sxs-lookup"><span data-stu-id="04118-112">Install OCSWMIBC.MSI.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="04118-113">OCSWMIBC.msi необходимо установить на компьютере, на котором запущен мастер объединения Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="04118-113">OCSWMIBC.msi must be installed on the computer where the Topology Builder Merge wizard is run.</span></span> <span data-ttu-id="04118-114">Однако рекомендуется устанавливать OCSWMIBC.msi на всех серверах переднего плана в топологии.</span><span class="sxs-lookup"><span data-stu-id="04118-114">However, we recommend installing OCSWMIBC.msi on all Front End servers in your topology.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="04118-115">OCSWMIBC.msi можно установить на любом компьютере домена, на котором установлены основные компоненты Lync Server 2013 и Командная консоль Lync Server 2013, и у него есть доступ к топологии Office Communications Server 2007 R2 (поставщик WMI для доменных служб Active Directory) и SQL Server.</span><span class="sxs-lookup"><span data-stu-id="04118-115">OCSWMIBC.msi can be installed on any computer in the domain that has the Lync Server 2013 Core Components and the Lync Server 2013 Management Shell installed, and has access to the Office Communications Server 2007 R2 topology (WMI provider to Active Directory Domain Services (AD DS) and SQL Server).</span></span>

    
    <span data-ttu-id="04118-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04118-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

