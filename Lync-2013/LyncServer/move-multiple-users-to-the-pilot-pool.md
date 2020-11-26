---
title: Перемещение нескольких пользователей в пилотный пул
description: Перемещение нескольких пользователей в пилотный пул.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move multiple users to the pilot pool
ms:assetid: 90d0590c-922c-4933-b778-9dd850b59310
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205096(v=OCS.15)
ms:contentKeyID: 48184838
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 121509fbad863b0ce2d6cc9c7e9afaef360e2eb6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438508"
---
# <a name="move-multiple-users-to-the-pilot-pool"></a><span data-ttu-id="faa27-103">Перемещение нескольких пользователей в пилотный пул</span><span class="sxs-lookup"><span data-stu-id="faa27-103">Move multiple users to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="faa27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="faa27-104">

<span> </span></span></span>

<span data-ttu-id="faa27-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="faa27-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="faa27-106">Вы можете переместить нескольких пользователей из пула Lync Server 2010 на сервер Lync Server 2013 для пилотного пула с помощью панели управления Lync Server 2013 или консоли управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="faa27-106">You can move multiple users from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="faa27-107">Перемещение нескольких пользователей с помощью панели управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa27-107">To move multiple users by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="faa27-108">Откройте **Панель управления Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="faa27-108">Open **Lync Server Control Panel**.</span></span>

2.  <span data-ttu-id="faa27-109">Нажмите **Пользователи**, затем "Поиск" и **Найти**.</span><span class="sxs-lookup"><span data-stu-id="faa27-109">Click **Users**, click Search, and then click **Find**.</span></span>

3.  <span data-ttu-id="faa27-110">Выберите двух пользователей, которых вы хотите переместить в пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="faa27-110">Select two users that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="faa27-111">В этом примере мы перейдем пользователей Чена Маслов и предложения Хансен.</span><span class="sxs-lookup"><span data-stu-id="faa27-111">In this example, we will move users Chen Yang and Claus Hansen.</span></span>
    
    <span data-ttu-id="faa27-112">![Перемещение пользователей в определенную группу регистров](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Перемещение пользователей в определенную группу регистров")</span><span class="sxs-lookup"><span data-stu-id="faa27-112">![Move users to specific register pool](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Move users to specific register pool")</span></span>  

4.  <span data-ttu-id="faa27-113">В меню **действия** выберите пункт **переместить выбранных пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="faa27-113">From the **Action** menu, select **Move selected users to pool**.</span></span>

5.  <span data-ttu-id="faa27-114">В раскрывающемся списке выберите пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="faa27-114">From the drop-down list, select the Lync Server 2013 pool.</span></span>

6.  <span data-ttu-id="faa27-115">Нажмите **Макрокоманда** и затем **Переместить выбранных пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="faa27-115">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="faa27-116">Нажмите OK.</span><span class="sxs-lookup"><span data-stu-id="faa27-116">Click OK.</span></span>
    
    <span data-ttu-id="faa27-117">![Перемещение пользователей, диалоговое окно «пул конечных регистраторов»](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Перемещение пользователей, диалоговое окно «пул конечных регистраторов»")</span><span class="sxs-lookup"><span data-stu-id="faa27-117">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

7.  <span data-ttu-id="faa27-118">Убедитесь в том, что столбец **пула регистратора** для пользователей теперь содержит пул Lync Server 2013, указывающий на то, что пользователи успешно перемещены.</span><span class="sxs-lookup"><span data-stu-id="faa27-118">Verify that the **Registrar pool** column for the users now contains the Lync Server 2013 pool, which indicates that the users have been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="faa27-119">Перемещение нескольких пользователей с помощью управляющей оболочки Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa27-119">To move multiple users by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="faa27-120">Откройте консоль управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="faa27-120">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="faa27-121">В командной строке введите следующую команду и замените **Пользователь1** и **Пользователь2** именами пользователей, которым вы хотите переместить и заменить **\_ FQDN пула** именем конечного пула.</span><span class="sxs-lookup"><span data-stu-id="faa27-121">At the command line, type the following and replace **User1** and **User2** with specific user names you want to move and replace **pool\_FQDN** with the name of the destination pool.</span></span> <span data-ttu-id="faa27-122">В этом примере мы перейдем пользователей Hao Чен и Katie Иордания.</span><span class="sxs-lookup"><span data-stu-id="faa27-122">In this example we will move users Hao Chen and Katie Jordan.</span></span>
    
        Get-CsUser -Filter {DisplayName -eq "User1" -or DisplayName - eq "User2"} | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="faa27-123">![Пример Get-CsUser командлета PowerShell](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Пример Get-CsUser командлета PowerShell")</span><span class="sxs-lookup"><span data-stu-id="faa27-123">![Example of PowerShell Get-CsUser cmdlet](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Example of PowerShell Get-CsUser cmdlet")</span></span>  

3.  <span data-ttu-id="faa27-124">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="faa27-124">At the command line, type the following</span></span>
    
        Get-CsUser -Identity "User1"

4.  <span data-ttu-id="faa27-125">Удостоверение **пула регистратора** теперь должно указывать на пул, указанный в предыдущем шаге, в качестве **\_ полного доменного имени пула** .</span><span class="sxs-lookup"><span data-stu-id="faa27-125">The **Registrar Pool** identity should now point to the pool you specified as **pool\_FQDN** in the previous step.</span></span> <span data-ttu-id="faa27-126">Присутствие этого удостоверения подтверждает, что пользователь успешно переместился.</span><span class="sxs-lookup"><span data-stu-id="faa27-126">The presence of this identity confirms that the user has been successfully moved.</span></span> <span data-ttu-id="faa27-127">Повторите действия, чтобы проверить, был ли перемещен **Пользователь2** .</span><span class="sxs-lookup"><span data-stu-id="faa27-127">Repeat step to verify **User2** has been moved.</span></span>
    
    <span data-ttu-id="faa27-128">![Результат командлета PowerShell Get-UsUser-Identity](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Результат командлета PowerShell Get-UsUser-Identity")</span><span class="sxs-lookup"><span data-stu-id="faa27-128">![Output of PowerShell Get-UsUser -Identity cmdlet](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Output of PowerShell Get-UsUser -Identity  cmdlet")</span></span>  

</div>

<div>

## <a name="to-move-all-users-at-the-same-time-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="faa27-129">Перемещение всех пользователей одновременно с помощью управляющей оболочки Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa27-129">To move all users at the same time by using the Lync Server 2013 Management Shell</span></span>

<span data-ttu-id="faa27-130">В этом примере все пользователи возвращены в пул Lync Server 2010 (pool01.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="faa27-130">In this example, all users have been returned to the Lync Server 2010 pool (pool01.contoso.net).</span></span> <span data-ttu-id="faa27-131">С помощью командной консоли Lync Server 2013 мы одновременно перейдем всех пользователей к группе Lync Server 2013 (pool02.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="faa27-131">Using the Lync Server 2013 Management Shell, we will move all users at the same time to the Lync Server 2013 pool (pool02.contoso.net).</span></span>

1.  <span data-ttu-id="faa27-132">Откройте **консоль управления Lync Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="faa27-132">Open the **Lync Server 2013 Management Shell**.</span></span>

2.  <span data-ttu-id="faa27-133">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="faa27-133">At the command line, type the following:</span></span>
    
        Get-CsUser -OnLyncServer | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="faa27-134">![Командлет PowerShell и результаты в командной консоли](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "Командлет PowerShell и результаты в командной консоли")</span><span class="sxs-lookup"><span data-stu-id="faa27-134">![PowerShell cmdlet and results in Management Shell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell cmdlet and results in Management Shell")</span></span>  

3.  <span data-ttu-id="faa27-135">Затем выполните **Get-CsUser** для одного из пилотных пользователей.</span><span class="sxs-lookup"><span data-stu-id="faa27-135">Next, run **Get-CsUser** for one of the pilot users.</span></span>
    
        Get-CsUser -Identity "Hao Chen"

4.  <span data-ttu-id="faa27-136">Удостоверение **пула регистраторов** для каждого пользователя теперь указывает на пул, указанный \_ в предыдущем шаге в качестве полного доменного имени пула.</span><span class="sxs-lookup"><span data-stu-id="faa27-136">The **Registrar Pool** identity for each user now points to the pool you specified as “pool\_FQDN” in the previous step.</span></span> <span data-ttu-id="faa27-137">Присутствие этого удостоверения подтверждает, что пользователь успешно переместился.</span><span class="sxs-lookup"><span data-stu-id="faa27-137">The presence of this identity confirms that the user has been successfully moved.</span></span>

5.  <span data-ttu-id="faa27-138">Кроме того, вы можете просмотреть список пользователей на панели управления Lync Server 2013 и убедиться, что значение пула регистратора теперь указывает на пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="faa27-138">Additionally, we can view the list of users in the Lync Server 2013 Control Panel and verify that the Registrar Pool value now points to the Lync Server 2013 pool.</span></span>
    
    <span data-ttu-id="faa27-139">![Список пользователей панели управления Lync Server 2013](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Список пользователей панели управления Lync Server 2013")</span><span class="sxs-lookup"><span data-stu-id="faa27-139">![Lync Server 2013 Control Panel user list](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 Control Panel user list")</span></span>  

<span data-ttu-id="faa27-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="faa27-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

