---
title: 'Lync Server 2013: Назначение пользователям номеров для отправки групповых звонков'
description: 'Lync Server 2013: Назначьте пользователям номера для отправки групповых звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign Group Call Pickup numbers to users
ms:assetid: b8e79275-8e7e-4799-b908-f34f61df22f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945647(v=OCS.15)
ms:contentKeyID: 51541508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d550b4556af427e11e99ffb26fb2a6c34d019490
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438346"
---
# <a name="assign-group-call-pickup-numbers-to-users-in-lync-server-2013"></a><span data-ttu-id="2250e-103">Назначение номеров группового звонка пользователям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2250e-103">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2250e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2250e-104">

<span> </span></span></span>

<span data-ttu-id="2250e-105">_**Тема последнего изменения:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="2250e-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="2250e-106">После добавления номеров групп отправки группового звонка в таблицу "приостановить Звонок" можно назначить группы пользователям.</span><span class="sxs-lookup"><span data-stu-id="2250e-106">After you add Group Call Pickup group numbers to the call park orbit table, you can assign the groups to users.</span></span> <span data-ttu-id="2250e-107">Используйте вспомогательный набор ресурсов для активации дополнительных функций расширения (SEFAUtil), чтобы назначить пользователям группы для отправки звонков.</span><span class="sxs-lookup"><span data-stu-id="2250e-107">Use the secondary extension feature activation (SEFAUtil ) resource kit tool to assign call pickup groups to users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2250e-108">В гибридном развертывании не назначайте группу отправки группового звонка пользователям, которые находятся в сети.</span><span class="sxs-lookup"><span data-stu-id="2250e-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="2250e-109">Пользователи, которые подключены к сети, не могут принимать участие в расправке групповых звонков.</span><span class="sxs-lookup"><span data-stu-id="2250e-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="2250e-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span><span class="sxs-lookup"><span data-stu-id="2250e-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-call-pickup-group-to-a-user"></a><span data-ttu-id="2250e-111">Назначение группе отправки группового звонка пользователю</span><span class="sxs-lookup"><span data-stu-id="2250e-111">To assign a Group Call Pickup group to a user</span></span>

1.  <span data-ttu-id="2250e-112">Войдите в систему компьютера, на котором установлено средство SEFAUtil, с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="2250e-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="2250e-113">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2250e-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="2250e-114">Например:</span><span class="sxs-lookup"><span data-stu-id="2250e-114">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2250e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="2250e-115">See Also</span></span>


[<span data-ttu-id="2250e-116">Включение отправки группового звонка для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2250e-116">Enable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-group-call-pickup-for-users.md)  
[<span data-ttu-id="2250e-117">Отключение отправки группового вызова для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2250e-117">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="2250e-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2250e-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

