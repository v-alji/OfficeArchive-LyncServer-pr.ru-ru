---
title: 'Lync Server 2013: Просмотр сведений о стандартном телефоне'
description: 'Lync Server 2013: Просмотр сведений о стандартном телефоне.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View common area phone information
ms:assetid: e652240c-6a3f-4be7-a083-32f24c08e655
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994081(v=OCS.15)
ms:contentKeyID: 51803992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4debe9a76118ac0bf1ca711426ce5487009a053
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443379"
---
# <a name="view-common-area-phone-information-in-lync-server-2013"></a><span data-ttu-id="b9e6d-103">Просмотр сведений о стандартном телефоне в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9e6d-103">View common area phone information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9e6d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9e6d-104">

<span> </span></span></span>

<span data-ttu-id="b9e6d-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="b9e6d-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="b9e6d-106">С помощью командлета **Get-CsCommonAreaPhone** вы можете просматривать сведения об общих телефонах, настроенных для использования в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="b9e6d-106">You can view information about the common area phones configured for use in your organization by using the **Get-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="b9e6d-107">При использовании без параметров этот командлет возвращает сведения обо всех ваших стандартных телефонах.</span><span class="sxs-lookup"><span data-stu-id="b9e6d-107">Used without any parameters, this cmdlet returns information about all your common area phones.</span></span> <span data-ttu-id="b9e6d-108">Необязательные параметры предоставляют различные способы фильтрации данных.</span><span class="sxs-lookup"><span data-stu-id="b9e6d-108">Optional parameters provide different ways for you to filter information.</span></span> <span data-ttu-id="b9e6d-109">Например, вы можете получить доступ ко всем общим телефонам, которые содержат объекты контактов в указанном подразделении (OU) или все объекты контактов, находящиеся в указанном здании.</span><span class="sxs-lookup"><span data-stu-id="b9e6d-109">For example, you can return all the common area phones that have contact objects in a specified organizational unit (OU) or all the contacts objects located in a specified building.</span></span> <span data-ttu-id="b9e6d-110">Дополнительные сведения о параметрах **Get-CsCommonAreaPhone** можно найти в [статьях Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone).</span><span class="sxs-lookup"><span data-stu-id="b9e6d-110">For details about **Get-CsCommonAreaPhone** parameters, see [Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone).</span></span>

<span data-ttu-id="b9e6d-111">Запустите **Get-CsCommonAreaPhone** либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9e6d-111">Run **Get-CsCommonAreaPhone** either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


<div>

## <a name="viewing-information-about-all-your-common-area-phones"></a><span data-ttu-id="b9e6d-112">Просмотр сведений обо всех общих телефонах с областями</span><span class="sxs-lookup"><span data-stu-id="b9e6d-112">Viewing Information about All Your Common Area Phones</span></span>

  - <span data-ttu-id="b9e6d-113">Чтобы просмотреть сведения обо всех обычных телефонах, введите в командной консоли Lync Server указанную ниже команду и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="b9e6d-113">To view information about all your common area phones, type the following command in the Lync Server Management Shell, and then press Enter:</span></span>
    
        Get-CsCommonAreaPhone
    
    <span data-ttu-id="b9e6d-114">Вы получите примерно такую информацию:</span><span class="sxs-lookup"><span data-stu-id="b9e6d-114">You’ll get information similar to this:</span></span>
    
        Identity           : CN=Building 14 Lobby,OU=Redmond,
                             DC=litwareinc,DC=com
        RegistrarPool      : atl-cs-001.litwareinc.com
        Enabled            : True
        SipAddress         : sip:4714e34b-9781-421d-b07a-
                             52056b5b4a56@litwareinc.com
        ClientPolicy       :
        PinPolicy          :
        VoicePolicy        :
        MobilityPolicy     :
        GroupChatPolicy    :
        ConferencingPolicy :
        LineURI            : tel:+14255550712
        DisplayNumber      : 1-425-555-0712
        DisplayName        : Building 14 Lobby
        Description        :
        ExUmEnabled        : False

</div>

<span data-ttu-id="b9e6d-115">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone) .</span><span class="sxs-lookup"><span data-stu-id="b9e6d-115">For details, see the Help topic for the [Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone) cmdlet.</span></span>

<span data-ttu-id="b9e6d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9e6d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

