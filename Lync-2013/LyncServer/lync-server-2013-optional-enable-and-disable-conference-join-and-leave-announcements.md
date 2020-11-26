---
title: Включение и отключение объявлений о присоединении и выходе из конференции (необязательно)
description: Необязательно Включение и отключение присоединения к Конференции и выход из объявлений.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Enable and disable conference join and leave announcements
ms:assetid: c9529568-e66c-48d8-aef2-9072f9c336ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398834(v=OCS.15)
ms:contentKeyID: 48185403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 70cd6b452a44d7d40f23d5ca96b6e4b7b063d2ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445241"
---
# <a name="optional-enable-and-disable-conference-join-and-leave-announcements-in-lync-server-2013"></a><span data-ttu-id="4a44b-103">Включение и отключение объявлений о присоединении и выходе из конференции в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="4a44b-103">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a44b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a44b-104">

<span> </span></span></span>

<span data-ttu-id="4a44b-105">_**Тема последнего изменения:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="4a44b-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="4a44b-106">При присоединении к Конференции или выходе из нее пользователи могут сообщать о своем входе в приложение и выходить из него с помощью звукового сопровождения или произнесения их имен.</span><span class="sxs-lookup"><span data-stu-id="4a44b-106">When dial-in users join or leave a conference, the Conferencing Announcement application can announce their entrance or exit by playing a tone or saying their names.</span></span> <span data-ttu-id="4a44b-107">Вы можете изменить способ работы объявлений, выполнив командлеты.</span><span class="sxs-lookup"><span data-stu-id="4a44b-107">You can change how announcements work by running cmdlets.</span></span> <span data-ttu-id="4a44b-108">Этот шаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4a44b-108">This step is optional.</span></span>

<div>

## <a name="to-modify-the-conference-join-and-leave-announcement-behavior"></a><span data-ttu-id="4a44b-109">Изменение объявлений при присоединении к конференции и выходе из нее</span><span class="sxs-lookup"><span data-stu-id="4a44b-109">To modify the conference join and leave announcement behavior</span></span>

1.  <span data-ttu-id="4a44b-110">Войдите в систему под учетной записью члена группы RTCUniversalServerAdmins или члена роли **CS-ServerAdministrator** или **CsAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="4a44b-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="4a44b-111">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="4a44b-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="4a44b-112">Выполните следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="4a44b-112">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingConfiguration
    
    <span data-ttu-id="4a44b-113">Этот командлет извлекает сведения о том, требуется ли участникам записывать свое имя при присоединении к Конференции, а также о том, как Lync Server отвечает за присоединение или выход из конференции с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="4a44b-113">This cmdlet retrieves information about whether participants are required to record their name when joining a conference and how Lync Server responds when participants join or leave a dial-in conference.</span></span>

4.  <span data-ttu-id="4a44b-114">Выполните следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="4a44b-114">Run the following at the command prompt:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity <identity of dial-in conferencing settings to be modified>
        [-EnableNameRecording <$true | $false>]
        [-EntryExitAnnouncementsEnabledByDefault <$true | $false>]
        [-EntryExitAnnouncementsType <UseNames | ToneOnly]
    
    <span data-ttu-id="4a44b-115">**EnableNameRecording**   Определяет, запрашивать ли анонимные участники записать свое имя перед входом в конференцию.</span><span class="sxs-lookup"><span data-stu-id="4a44b-115">**EnableNameRecording**   Determines whether anonymous participants are asked to record their name before entering the conference.</span></span> <span data-ttu-id="4a44b-116">По умолчанию используется значение "$true", что означает, что анонимным участникам будет предложено указать свое имя при присоединении к Конференции.</span><span class="sxs-lookup"><span data-stu-id="4a44b-116">The default value is "$true," which means that anonymous participants are prompted to state their name when joining a conference.</span></span> <span data-ttu-id="4a44b-117">(Участники, прошедшие проверку подлинности, не записывают свое имя, так как вместо этого используется отображаемое имя.)</span><span class="sxs-lookup"><span data-stu-id="4a44b-117">(Authenticated participants do not record their name because their display name is used instead.)</span></span>
    
    <span data-ttu-id="4a44b-118">**EntryExitAnnouncementsEnabledByDefault**   Указывает, включены ли извещения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a44b-118">**EntryExitAnnouncementsEnabledByDefault**   Indicates whether announcements are turned on or off by default.</span></span> <span data-ttu-id="4a44b-119">Значением по умолчанию является "$false, что означает, что по умолчанию при присоединении к Конференции или выходе участников из нее не будет извещений.</span><span class="sxs-lookup"><span data-stu-id="4a44b-119">The default value is "$false," which means that by default there are no announcements when participants join or leave a conference.</span></span> <span data-ttu-id="4a44b-120">Организатор собрания может переопределить этот параметр при планировании собрания.</span><span class="sxs-lookup"><span data-stu-id="4a44b-120">The meeting organizer can override this setting when scheduling a meeting.</span></span>
    
    <span data-ttu-id="4a44b-121">**EntryExitAnnouncementsType**   Указывает действие, предпринимаемое при каждом присоединении или выходе из конференции, для которой включены извещения.</span><span class="sxs-lookup"><span data-stu-id="4a44b-121">**EntryExitAnnouncementsType**   Indicates the action taken whenever a participant joins or leaves a conference for which announcements are enabled.</span></span> <span data-ttu-id="4a44b-122">По умолчанию используется значение "UseNames", которое означает, что на Конференции было объявлено извещение о том, что "Кен Myer входит в конференцию", когда извещения включены.</span><span class="sxs-lookup"><span data-stu-id="4a44b-122">The default value is "UseNames," which means there is an announcement similar to the following: "Ken Myer has joined the conference" when announcements are turned on.</span></span>
    
    <span data-ttu-id="4a44b-p105">Эти параметры можно настроить в глобальной области или в области узла. Параметры, настроенные в области узла, имеют более высокий приоритет, чем параметры, настроенные в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="4a44b-p105">You can configure these settings at the global scope or at the site scope. Settings configured at the site scope take precedence over settings configured at the global scope.</span></span>
    
    <span data-ttu-id="4a44b-125">Например:</span><span class="sxs-lookup"><span data-stu-id="4a44b-125">For example:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity site:Redmond
        -EnableNameRecording $false
        -EntryExitAnnouncementsEnabledByDefault $true
        -EntryExitAnnouncementsType ToneOnly
    
    <span data-ttu-id="4a44b-126">В этом примере параметры задаются в области сайта для Redmond.</span><span class="sxs-lookup"><span data-stu-id="4a44b-126">In this example, settings are configured at the site scope for Redmond.</span></span> <span data-ttu-id="4a44b-127">Объявления включены, но у участников не запрашивается имя при подключении к конференции.</span><span class="sxs-lookup"><span data-stu-id="4a44b-127">Announcements are turned on, but participants are not prompted to say their name when they join a conference.</span></span> <span data-ttu-id="4a44b-128">Звуковой сигнал воспроизводится, когда участники вводят или покидают Конференцию.</span><span class="sxs-lookup"><span data-stu-id="4a44b-128">A tone is played when participants enter or leave a conference.</span></span>

<span data-ttu-id="4a44b-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a44b-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

