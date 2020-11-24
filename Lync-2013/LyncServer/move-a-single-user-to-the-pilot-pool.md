---
title: Перемещение отдельного пользователя в пилотный пул
description: Переместить отдельного пользователя в проект пилотного пула.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move a single user to the pilot pool
ms:assetid: e9de81a8-40dd-4446-81e7-a2b810eaea50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205401(v=OCS.15)
ms:contentKeyID: 48185905
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5f7396ed2d92c7015f01ff6cd6e90fd3998219d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398638"
---
# <a name="move-a-single-user-to-the-pilot-pool"></a><span data-ttu-id="b359e-103">Перемещение отдельного пользователя в пилотный пул</span><span class="sxs-lookup"><span data-stu-id="b359e-103">Move a single user to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b359e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b359e-104">

<span> </span></span></span>

<span data-ttu-id="b359e-105">_**Тема последнего изменения:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="b359e-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="b359e-106">Вы можете переместить пользователя из пула Lync Server 2010 на сервер Lync Server 2013 для пилотного пула с помощью панели управления Lync Server 2013 или консоли управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b359e-106">You can move a user from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="b359e-107">В приведенном ниже примере в столбце пула регистратора **pool01.contoso.NET** используется пул Lync Server 2010, а в этот пул будут подключены все шесть пользователей.</span><span class="sxs-lookup"><span data-stu-id="b359e-107">In the example below, in the Registrar pool column, **pool01.contoso.net** is the Lync Server 2010 pool, and all six of these users are connected to this pool.</span></span> <span data-ttu-id="b359e-108">Используйте описанные ниже процедуры для перемещения пользователя в пул Lync Server 2013 с помощью панели управления Lync Server 2013 и командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b359e-108">Use the following procedures to move a user to your Lync Server 2013 pool using Lync Server 2013 Control Panel and Lync Server Management Shell.</span></span>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="b359e-109">Перемещение пользователя с помощью панели управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b359e-109">To move a user by using the Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="b359e-110">**Список пользователей на панели управления Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="b359e-110">**List of users in the Lync Server 2013 Control Panel**</span></span>

<span data-ttu-id="b359e-111">![Панель управления Lync Server, диалоговое окно перемещения пользователя](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Панель управления Lync Server, диалоговое окно перемещения пользователя")</span><span class="sxs-lookup"><span data-stu-id="b359e-111">![Lync Server Control Panel, Move User dialog](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server Control Panel, Move User dialog")</span></span>

1.  <span data-ttu-id="b359e-112">Войдите на сервер переднего плана с помощью учетной записи, являющейся членом группы RTCUniversalServerAdmins или членом административной роли CsAdministrator или CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="b359e-112">Log on to the Front End Server with an account that is a member of the RTCUniversalServerAdmins group or a member of the CsAdministrator or CsUserAdministrator administrative role.</span></span>

2.  <span data-ttu-id="b359e-113">Откройте **Панель управления Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b359e-113">Open **Lync Server Control Panel**.</span></span>

3.  <span data-ttu-id="b359e-114">Нажмите **Пользователи**, затем "Поиск" и **Найти**.</span><span class="sxs-lookup"><span data-stu-id="b359e-114">Click **Users**, click Search, and then click **Find**.</span></span>

4.  <span data-ttu-id="b359e-115">Выберите пользователя, которого вы хотите переместить в пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b359e-115">Select a user that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="b359e-116">В данном примере мы будем перемещать пользователя Sara Davis.</span><span class="sxs-lookup"><span data-stu-id="b359e-116">In this example, we will move user Sara Davis.</span></span>

5.  <span data-ttu-id="b359e-117">В меню **Макрокоманда** выберите **Переместить выбранных пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="b359e-117">On the **Action** menu, select **Move selected users to pool**.</span></span>

6.  <span data-ttu-id="b359e-118">В раскрывающемся списке выберите пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b359e-118">From the drop-down list, select the Lync Server 2013 pool.</span></span>

7.  <span data-ttu-id="b359e-119">Нажмите **Макрокоманда** и затем **Переместить выбранных пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="b359e-119">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="b359e-120">Нажмите **OK**.</span><span class="sxs-lookup"><span data-stu-id="b359e-120">Click **OK**.</span></span>
    
    <span data-ttu-id="b359e-121">![Перемещение пользователей, диалоговое окно «пул конечных регистраторов»](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Перемещение пользователей, диалоговое окно «пул конечных регистраторов»")</span><span class="sxs-lookup"><span data-stu-id="b359e-121">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

8.  <span data-ttu-id="b359e-122">Убедитесь в том, что столбец **пула регистратора** для пользователя теперь содержит пул Lync Server 2013, указывающий на то, что пользователь успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="b359e-122">Verify that the **Registrar pool** column for the user now contains the Lync Server 2013 pool, which indicates that the user has been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="b359e-123">Перемещение пользователя с помощью управляющей оболочки Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b359e-123">To move a user by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="b359e-124">Откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b359e-124">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="b359e-125">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b359e-125">At the command line, type the following:</span></span>
    
        Move-CsUser -Identity "David Pelton" -Target "pool02.contoso.net"

3.  <span data-ttu-id="b359e-126">Затем в командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b359e-126">Next, at the command line, type the following:</span></span>
    
        Get-CsUser -Identity "David Pelton"

4.  <span data-ttu-id="b359e-127">Идентификатор **RegistrarPool** теперь указывает на пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b359e-127">The **RegistrarPool** identity now points to the Lync Server 2013 pool.</span></span> <span data-ttu-id="b359e-128">Присутствие этого удостоверения подтверждает, что пользователь успешно переместился.</span><span class="sxs-lookup"><span data-stu-id="b359e-128">The presence of this identity confirms that the user has been successfully moved.</span></span>
    
    <span data-ttu-id="b359e-129">![Вывод из командлета Get-CsUser с фильтром идентификаторов](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Вывод из командлета Get-CsUser с фильтром идентификаторов")</span><span class="sxs-lookup"><span data-stu-id="b359e-129">![Output from Get-CsUser cmdlet with Identity filter](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Output from Get-CsUser cmdlet with Identity filter")</span></span>  
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b359e-130">Дополнительные сведения о командлете <STRONG>Get-CsUser</STRONG> : <STRONG>Get-Help Get-CsUser-Detailed</STRONG></span><span class="sxs-lookup"><span data-stu-id="b359e-130">For details about the <STRONG>Get-CsUser</STRONG> cmdlet, run: <STRONG>Get-Help Get-CsUser –Detailed</STRONG></span></span>

    
    <span data-ttu-id="b359e-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b359e-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

