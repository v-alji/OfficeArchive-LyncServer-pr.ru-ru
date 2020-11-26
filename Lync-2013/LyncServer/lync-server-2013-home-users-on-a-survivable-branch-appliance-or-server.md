---
title: 'Lync Server 2013: нользователи, работающие дома на устройстве или сервере для обеспечения связи в филиалах'
description: 'Lync Server 2013: домашние пользователи на устройстве с бесперебойной филиалом или на сервере.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Home users on a Survivable Branch Appliance or Server
ms:assetid: faf1ebb9-6d7d-4a58-8ff7-801b7b31d3ba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413066(v=OCS.15)
ms:contentKeyID: 48185926
ms.date: 12/11/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 124eb7a51a8d5ff672d720fdad8956f682e29090
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427618"
---
# <a name="home-users-on-a-survivable-branch-appliance-or-server-in-lync-server-2013"></a><span data-ttu-id="10926-103">Пользователи, работающие дома на устройстве или сервере для обеспечения связи в филиалах, в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10926-103">Home users on a Survivable Branch Appliance or Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10926-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10926-104">

<span> </span></span></span>

<span data-ttu-id="10926-105">_**Тема последнего изменения:** 2014-12-10_</span><span class="sxs-lookup"><span data-stu-id="10926-105">_**Topic Last Modified:** 2014-12-10_</span></span>

<span data-ttu-id="10926-106">Процесс доступа пользователей к сети с бесперебойной подразделением или работающем на нем сервере аналогичен процессу служб доступа к сети в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="10926-106">The process of homing users on a Survivable Branch Appliance or a Survivable Branch Server is similar to the process of homing users on a Front End pool.</span></span> <span data-ttu-id="10926-107">Проведите бесперебойную подсеть устройства филиалов или бесперебойно работающую процедуру сервера ветвей на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="10926-107">Perform the Survivable Branch Appliance or Survivable Branch Server procedure at the central site.</span></span>

<div>

## <a name="to-home-users-on-survivable-branch-appliance-or-survivable-branch-server"></a><span data-ttu-id="10926-108">Для домашних пользователей на бесперебойно работающем устройстве филиалов или на сервере, который находится в бесперебойном отделении</span><span class="sxs-lookup"><span data-stu-id="10926-108">To home users on Survivable Branch Appliance or Survivable Branch Server</span></span>

1.  <span data-ttu-id="10926-109">Прежде чем переносить пользователей на сервер или бесперебойную подписку, откройте командную консоль Lync Server Management Shell, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="10926-109">Before moving users to the Survivable Branch Server or Survivable Branch Server, open the Lync Server Management Shell, and then do all of the following:</span></span>
    
      - <span data-ttu-id="10926-110">Запустите командлет **Test-CsPstnOutboundCall** , чтобы убедиться в том, что запущенный сервер филиала работает и настроено подключение к телефонной сети общего пользования (PSTN).</span><span class="sxs-lookup"><span data-stu-id="10926-110">Run the cmdlet **Test-CsPstnOutboundCall** to verify that the Survivable Branch Server is running and that the public switched telephone network (PSTN) connectivity is configured.</span></span> <span data-ttu-id="10926-111">Если вам нужно изменить свойства шлюза PSTN, используйте командлет **Set-CsPstnGateway**.</span><span class="sxs-lookup"><span data-stu-id="10926-111">If you need to modify PSTN gateway properties, use the cmdlet **Set-CsPstnGateway**.</span></span>
    
      - <span data-ttu-id="10926-112">Запустите командлет **Get-CsVoicePolicy** , чтобы убедиться в том, что пользователи, которые будут размещены на сервере для работающего филиала, имеют соответствующую политику маршрутизации VoIP.</span><span class="sxs-lookup"><span data-stu-id="10926-112">Run the cmdlet **Get-CsVoicePolicy** to verify that the users who will be homed on the Survivable Branch Server have the appropriate VoIP routing policy.</span></span> <span data-ttu-id="10926-113">Если необходимо изменить политику VoIP, используйте командлет **Set-CsVoicePolicy**.</span><span class="sxs-lookup"><span data-stu-id="10926-113">If you need to modify the VoIP policy, use the cmdlet **Set-CsVoicePolicy**.</span></span>
    
      - <span data-ttu-id="10926-114">Запустите командлет **Get-CsVoicemailReroutingConfiguration** , чтобы убедиться, что параметры перенаправления голосовой почты настроены.</span><span class="sxs-lookup"><span data-stu-id="10926-114">Run the cmdlet **Get-CsVoicemailReroutingConfiguration** to verify that the voice mail rerouting settings are configured.</span></span> <span data-ttu-id="10926-115">Если вам нужно изменить параметры перенаправления голосовой почты, используйте командлет **Set-CsVoicemailReroutingConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="10926-115">If you need to modify the voice mail rerouting settings, use the cmdlet **Set-CsVoicemailReroutingConfiguration**.</span></span>

2.  <span data-ttu-id="10926-116">В командной консоли Lync Server выполните командлет **Move-CsUser** , чтобы переместить домашних пользователей.</span><span class="sxs-lookup"><span data-stu-id="10926-116">In the Lync Server Management Shell, run the cmdlet **Move-CsUser** to move home users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="10926-117">Вы также можете использовать панель управления Lync Server для проверки необходимых и домашних пользователей.</span><span class="sxs-lookup"><span data-stu-id="10926-117">You can also use Lync Server Control Panel to verify prerequisites and home users.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="10926-118">Пользователи, расположенные на устройстве с бесперебойной подразделением Lync Server, не могут создавать новые комнаты чата и просматривать открытку для существующих комнат.</span><span class="sxs-lookup"><span data-stu-id="10926-118">Users who are homed on a Lync Server Survivable Branch Appliance are unable to create new chat rooms or view the room card for existing rooms.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="10926-119">См. также</span><span class="sxs-lookup"><span data-stu-id="10926-119">See Also</span></span>


[<span data-ttu-id="10926-120">Test-CsPstnOutboundCall</span><span class="sxs-lookup"><span data-stu-id="10926-120">Test-CsPstnOutboundCall</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall)  
[<span data-ttu-id="10926-121">Get-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="10926-121">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="10926-122">Get-CsVoicemailReroutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="10926-122">Get-CsVoicemailReroutingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicemailReroutingConfiguration)  
[<span data-ttu-id="10926-123">Move-CsUser</span><span class="sxs-lookup"><span data-stu-id="10926-123">Move-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Move-CsUser)  
  

<span data-ttu-id="10926-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10926-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

