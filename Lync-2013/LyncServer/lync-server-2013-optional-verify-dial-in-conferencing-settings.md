---
title: 'Lync Server 2013: проверка параметров конференц-связи с телефонным подключением (необязательно)'
description: 'Lync Server 2013: (необязательный) Проверка параметров конференц-связи с телефонным подключением.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify dial-in conferencing settings
ms:assetid: a85efdda-97b0-4f3b-bd26-04416bee8ef5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412789(v=OCS.15)
ms:contentKeyID: 48185027
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec002cfbd7cdd67498768a360143f88ab4f8e1b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445206"
---
# <a name="optional-verify-dial-in-conferencing-settings-in-lync-server-2013"></a><span data-ttu-id="3a53b-103">Проверка параметров конференц-связи с телефонным подключением в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3a53b-103">(Optional) Verify dial-in conferencing settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3a53b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3a53b-104">

<span> </span></span></span>

<span data-ttu-id="3a53b-105">_**Тема последнего изменения:** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="3a53b-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="3a53b-106">Чтобы завершить проверку конфигурации конференц-связи с телефонным подключением, выполните поиск абонентских групп с регионом, для которого не задан ни один номер доступа, а также номеров доступа, для которых не задан ни один регион конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="3a53b-106">As final verification of your dial-in conferencing configuration, you can search for dial plans that have a dial-in conferencing region that is not used by any access number and for access numbers that have not specified a dial-in conferencing region.</span></span> <span data-ttu-id="3a53b-107">Этот шаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a53b-107">This step is optional.</span></span>

<div>

## <a name="to-find-dial-plans-with-a-dial-in-conferencing-region-that-is-not-used-by-an-access-number"></a><span data-ttu-id="3a53b-108">Чтобы найти абонентские группы с областью конференц-связи с телефонным подключением, которая не используется номером доступа</span><span class="sxs-lookup"><span data-stu-id="3a53b-108">To find dial plans with a dial-in conferencing region that is not used by an access number</span></span>

1.  <span data-ttu-id="3a53b-109">Войдите в систему под учетной записью члена группы RTCUniversalServerAdmins или члена роли **CS-ServerAdministrator** или **CsAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="3a53b-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="3a53b-110">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="3a53b-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3a53b-111">Выполните следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="3a53b-111">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingAccessNumber -EmptyRegion
    
    <span data-ttu-id="3a53b-112">Этот командлет возвращает все абонентские группы с регионом конференц-связи с телефонным подключением, для которого не задан ни один номер доступа.</span><span class="sxs-lookup"><span data-stu-id="3a53b-112">This cmdlet returns all of the dial plans that have a dial-in conferencing region that is not used by an access number.</span></span>

</div>

<div>

## <a name="to-find-access-numbers-without-assigned-regions"></a><span data-ttu-id="3a53b-113">Поиск номеров доступа без назначенных регионов</span><span class="sxs-lookup"><span data-stu-id="3a53b-113">To find access numbers without assigned regions</span></span>

1.  <span data-ttu-id="3a53b-114">Войдите в систему под учетной записью члена группы RTCUniversalServerAdmins или члена роли **CS-ServerAdministrator** или **CsAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="3a53b-114">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="3a53b-115">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="3a53b-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3a53b-116">Выполните следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="3a53b-116">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingAccessNumber -Region NULL
    
    <span data-ttu-id="3a53b-117">Этот командлет возвращает все номера доступа к конференц-связи с телефонным подключением, которые не связаны ни с одним регионом.</span><span class="sxs-lookup"><span data-stu-id="3a53b-117">This cmdlet returns all the dial-in conferencing access numbers that are not associated with a region.</span></span>

<span data-ttu-id="3a53b-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3a53b-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

