---
title: 'Lync Server 2013: первые шаги перед началом миграции пользователей из Lync Online в локальное Lync'
description: 'Lync Server 2013: первые шаги перед началом миграции пользователей из Lync Online в локальное Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: First steps before you start migrating users from Lync Online to Lync on-premises
ms:assetid: 98245b04-ded4-4186-8da3-ba1c554b5c39
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689118(v=OCS.15)
ms:contentKeyID: 62258123
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 408820e461c0a9f7c0beaaaae3a502802048d3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428120"
---
# <a name="first-steps-before-you-start-migrating-users-from-lync-online-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="16afa-103">Прежде чем приступить к переносу пользователей из Lync Online в локальную версию Lync в Lync Server 2013, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="16afa-103">First steps before you start migrating users from Lync Online to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16afa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16afa-104">

<span> </span></span></span>

<span data-ttu-id="16afa-105">_**Тема последнего изменения:** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="16afa-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="16afa-106">Прежде чем приступить к перемещению пользователей Lync Online в локальную среду, убедитесь в том, что выполняются все указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="16afa-106">Before you start moving Lync Online users to your on-premises environment, check that all of the following are true:</span></span>

  - <span data-ttu-id="16afa-107">Локальная среда Lync Server должна быть полностью развернута и проверена.</span><span class="sxs-lookup"><span data-stu-id="16afa-107">Your Lync Server on-premises environment must be fully deployed and validated.</span></span> <span data-ttu-id="16afa-108">Дополнительные сведения можно найти в разделе [развертывание Lync Server 2013](lync-server-2013-deploying-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="16afa-108">For more information, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md).</span></span>

  - <span data-ttu-id="16afa-109">Клиент Lync Online должен быть настроен для доступа к удаленной оболочке PowerShell.</span><span class="sxs-lookup"><span data-stu-id="16afa-109">Your Lync Online tenant must be configured for remote PowerShell Access.</span></span>
    
    <span data-ttu-id="16afa-110">Для этого сначала установите модуль Lync Online для Windows PowerShell, который вы можете найти [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911) ниже.</span><span class="sxs-lookup"><span data-stu-id="16afa-110">To do this, first install the Lync Online module for Windows PowerShell, which you can get here: [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911).</span></span>
    
    <span data-ttu-id="16afa-111">После установки модуля вы можете установить удаленный сеанс, введя следующие командлеты в командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="16afa-111">After you install the module, you can establish a remote session by typing the following cmdlets in the Lync Server Management Shell:</span></span>
    
       ```PowerShell
        Import-Module LyncOnlineConnector
       ```  
    
       ```PowerShell
        $cred = Get-Credential
       ``` 
    
       ```PowerShell
        $CSSession = New-CsOnlineSession -Credential $cred
       ```
    
       ```PowerShell
        Import-PSSession $CSSession -AllowClobber
       ```
    
    <span data-ttu-id="16afa-112">Дополнительные сведения о том, как установить удаленный сеанс PowerShell в Lync Online, можно найти [в разделе Подключение к Lync Online с помощью Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="16afa-112">For more information about how to establish a remote PowerShell session with Lync Online, see [Connecting to Lync Online by using Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>
  
    <span data-ttu-id="16afa-113">Дополнительные сведения об использовании модуля Lync Online PowerShell можно найти в разделе [Использование Windows PowerShell для управления Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="16afa-113">For more information about using the Lync Online PowerShell module, see [Using Windows PowerShell to manage Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

  - <span data-ttu-id="16afa-114">В Lync Online необходимо настроить общее адресное пространство SIP.</span><span class="sxs-lookup"><span data-stu-id="16afa-114">Your Lync Online must be configured for Shared SIP Address Space.</span></span> <span data-ttu-id="16afa-115">Для этого сначала запустите удаленный сеанс PowerShell с помощью Lync Online.</span><span class="sxs-lookup"><span data-stu-id="16afa-115">To do this, first start a remote Powershell session with Lync Online.</span></span> <span data-ttu-id="16afa-116">Затем выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="16afa-116">Then run the following cmdlet:</span></span>
    
        Set-CsTenantFederationConfiguration -SharedSipAddressSpace $True

<span data-ttu-id="16afa-117">После выполнения этих действий вы можете перейти к [миграции пользователей Lync Online в локальное Lync Server 2013](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md).</span><span class="sxs-lookup"><span data-stu-id="16afa-117">After you’ve finished these steps, you can move on to [Migrating Lync Online users to Lync on-premises in Lync Server 2013](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md).</span></span>

<span data-ttu-id="16afa-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16afa-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

