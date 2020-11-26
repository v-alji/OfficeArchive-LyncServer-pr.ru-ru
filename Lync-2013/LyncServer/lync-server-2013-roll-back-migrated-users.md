---
title: 'Lync Server 2013: откат перенесенных пользователей'
description: 'Lync Server 2013: откат пользователей, для которых выполнена миграция.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Roll back migrated users
ms:assetid: bfabaf0b-9a42-4057-b729-a7ab9eee8c72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205224(v=OCS.15)
ms:contentKeyID: 48185286
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c5993bfd530c84307d3ee5be627b3ed33814be73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442348"
---
# <a name="roll-back-migrated-users-in-lync-server-2013"></a><span data-ttu-id="f15e3-103">Откат перенесенных пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f15e3-103">Roll back migrated users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f15e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f15e3-104">

<span> </span></span></span>

<span data-ttu-id="f15e3-105">_**Тема последнего изменения:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="f15e3-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="f15e3-106">Если вы хотите выполнить откат в едином хранилище контактов, изменяйте контакты только в том случае, если вы вернете пользователя на Exchange 2010 или Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="f15e3-106">If you need to roll back the unified contact store feature, roll back the contacts only if you move the user back to Exchange 2010 or Lync Server 2010.</span></span> <span data-ttu-id="f15e3-107">Чтобы выполнить откат, отключите политику для пользователя, а затем выполните командлет **Invoke-CsUcsRollback** .</span><span class="sxs-lookup"><span data-stu-id="f15e3-107">To roll back, disable the policy for the user, and then run the **Invoke-CsUcsRollback** cmdlet.</span></span> <span data-ttu-id="f15e3-108">Просто запустить функцию **Invoke-CsUcsRollback** недостаточно для обеспечения постоянной процедуры отката, так как единая миграция хранилища контактов инициируется повторно, если она не отключена.</span><span class="sxs-lookup"><span data-stu-id="f15e3-108">Just running **Invoke-CsUcsRollback** alone is not enough to ensure permanent rollback, because unified contact store migration will be initiated again if the policy is not disabled.</span></span> <span data-ttu-id="f15e3-109">Например, если пользователь выполняет откат, так как Exchange 2013 возвращается в Exchange 2010, а затем почтовый ящик пользователя перемещается в Exchange 2013, то единая миграция в магазине контактов будет запущена еще раз в семь дней после отката, пока единая база данных контактов по-прежнему включена для пользователя в политике служб пользователей.</span><span class="sxs-lookup"><span data-stu-id="f15e3-109">For example, if a user is rolled back because Exchange 2013 is rolled back to Exchange 2010, and then the user’s mailbox is moved to Exchange 2013, the unified contact store migration will be initiated again seven days after the rollback, as long as unified contact store is still enabled for the user in the user services policy.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f15e3-110">Командлет <STRONG>Move-CsUser</STRONG> автоматически откатывает хранилище контактов пользователя Exchange 2013 на Lync Server 2013 в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="f15e3-110">The <STRONG>Move-CsUser</STRONG> cmdlet automatically rolls back the user's contact store from Exchange 2013 to Lync Server 2013 in the following situations:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="f15e3-111">При перемещении пользователей из Lync Server 2013 в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="f15e3-111">When users are moved from Lync Server 2013 to Lync Server 2010.</span></span></P>
> <LI>
> <P><span data-ttu-id="f15e3-112">Если миграция пользователей осуществляется между организациями, например, когда пользователь перемещается из Lync Online в Lync Server 2013 в локальной среде или наоборот.</span><span class="sxs-lookup"><span data-stu-id="f15e3-112">When users are migrated cross premises, such as when a user is moved from Lync Online to Lync Server 2013 on-premises, or vice versa.</span></span></P></LI></UL>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f15e3-113">Импорт данных из хранилища Объединенных контактов из резервной базы данных может привести к повреждению данных из хранилища контактов и данных пользователя, если в процессе экспорта и импорта изменился режим хранилища единого контакта.</span><span class="sxs-lookup"><span data-stu-id="f15e3-113">Importing unified contact store data from a backup database can cause unified contact store data and user data to become corrupted if the unified contact store mode changed between the export and the import.</span></span> <span data-ttu-id="f15e3-114">Например:</span><span class="sxs-lookup"><span data-stu-id="f15e3-114">For example:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="f15e3-115">Если вы экспортируете списки контактов перед тем, как контакты пользователей будут перенесены в Exchange 2013, а затем, после миграции, импортируйте эти данные в единое хранилище контактов и списки контактов, которые будут повреждены.</span><span class="sxs-lookup"><span data-stu-id="f15e3-115">If you export contact lists before the users' contacts are migrated to Exchange 2013 and then, after the migration, import the same data, the unified contact store data and contact lists will be corrupted.</span></span></P>
> <LI>
> <P><span data-ttu-id="f15e3-116">Если вы экспортируете учетные данные после миграции пользователей в Exchange 2013, откати миграции, а также по какой – либо причине импорт данных из нее после миграции, данные в едином хранилище контактов и списки контактов будут повреждены.</span><span class="sxs-lookup"><span data-stu-id="f15e3-116">If you export userdata after you migrate users to Exchange 2013, roll back the migration, and then for some reason you import the data from after the migration, the unified contact store data and contact lists will be corrupted.</span></span></P></LI></UL>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f15e3-117">Перед перемещением почтового ящика Exchange из Exchange 2013 в Exchange 2010 администратор Exchange должен удостовериться, что администратор сервера Lync Server отключил контакты пользователей Lync Server с Exchange 2013 на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f15e3-117">Before you move an Exchange mailbox from Exchange 2013 to Exchange 2010, the Exchange administrator must make sure that the Lync Server administrator has first rolled back the Lync Server user contacts from Exchange 2013 to Lync Server.</span></span> <span data-ttu-id="f15e3-118">Чтобы вернуть контакты из хранилища Объединенных контактов в Lync Server, ознакомьтесь с процедурой "откатить контакты из хранилища контактов из Exchange 2013 на Lync Server 2013" Далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="f15e3-118">To roll back unified contact store contacts to Lync Server, see procedure "To roll back unified contact store contacts from Exchange 2013 to Lync Server 2013," later in this section.</span></span>



</div>

<span data-ttu-id="f15e3-119">Ниже описана процедура отката контактов пользователей.</span><span class="sxs-lookup"><span data-stu-id="f15e3-119">The following procedure describes how to roll back user contacts.</span></span> <span data-ttu-id="f15e3-120">Если вы используете командлет **Move-CsUser** для перемещения пользователей между lync Server 2013 и Lync Server 2010, вы можете пропустить эти действия, так как командлет **Move-CsUser** автоматически откатывает unifed Store Contact при перемещении пользователей с Lync Server 2013 на Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="f15e3-120">If you use the **Move-CsUser** cmdlet to move users between Lync Server 2013 and Lync Server 2010, you can skip these steps because the **Move-CsUser** cmdlet automatically rolls back unifed contact store when it moves users from Lync Server 2013 to Lync Server 2010.</span></span> <span data-ttu-id="f15e3-121">В разделе **Move-CsUser** не отключена политика хранилища контактов, поэтому миграция в единое хранилище контактов будет повторяться, если пользователь перейдет на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f15e3-121">**Move-CsUser** does not disable unified contact store policy, so the migration to unified contact store will recur if the user is moved back to Lync Server 2013.</span></span>

<div>

## <a name="to-roll-back-user-contacts-from-lync-server-2013-to-lync-server-2010"></a><span data-ttu-id="f15e3-122">Откат контактов пользователей из Lync Server 2013 и Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="f15e3-122">To roll back user contacts from Lync Server 2013 to Lync Server 2010</span></span>

1.  <span data-ttu-id="f15e3-123">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f15e3-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="f15e3-124">Отключите единое хранилище контактов, чтобы пользователи могли выполнить откат, чтобы они не были повторно перенесены после отката.</span><span class="sxs-lookup"><span data-stu-id="f15e3-124">Disable unified contact store for the users to be rolled back so that they will not be remigrated after rollback.</span></span> <span data-ttu-id="f15e3-125">(Выполните это действие только в том случае, если вы хотите убедиться, что пользователи не будут переноситься в будущем.) Чтобы отключить единое хранилище контактов для отдельных пользователей, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="f15e3-125">(Perform this step only if you want to make sure that users will not remigrate in the future.) To disable unified contact store for individual users, at the command line, type:</span></span>
    
        Set-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $False
    
    <span data-ttu-id="f15e3-126">Например:</span><span class="sxs-lookup"><span data-stu-id="f15e3-126">For example:</span></span>
    
        Set-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $False

3.  <span data-ttu-id="f15e3-127">Перед перемещением пользователя из Lync Server 2013 в Lync Server 2010 верните список контактов для указанных пользователей на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f15e3-127">Before moving a user from Lync Server 2013 to Lync Server 2010, roll back the Buddy List for the specified users on Lync Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f15e3-128">Если это действие не задано, список собеседников будет потерян.</span><span class="sxs-lookup"><span data-stu-id="f15e3-128">If this step is omitted, the Buddy List will be lost.</span></span>

    
    </div>

4.  <span data-ttu-id="f15e3-129">Выполнять откат указанных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f15e3-129">Roll back the specified users.</span></span> <span data-ttu-id="f15e3-130">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f15e3-130">At the command line, type:</span></span>
    
        Invoke-CsUcsRollback -Identity "<user display name>"
    
    <span data-ttu-id="f15e3-131">Например:</span><span class="sxs-lookup"><span data-stu-id="f15e3-131">For example:</span></span>
    
        Invoke-CsUcsRollback -Identity "Ken Myer"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f15e3-132">Мы не рекомендуем использовать параметр – Force для принудительного отката.</span><span class="sxs-lookup"><span data-stu-id="f15e3-132">We do not recommend using the –Force option to force the rollback.</span></span> <span data-ttu-id="f15e3-133">Если вы используете этот параметр, контакты пользователей будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="f15e3-133">If you use this option, the users' contacts will be lost.</span></span>

    
    </div>

</div>

<div>

## <a name="to-roll-back-unified-contact-store-contacts-from-exchange-2013-to-lync-server-2013"></a><span data-ttu-id="f15e3-134">Откат Объединенных Объединенных контактов из Exchange 2013 на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f15e3-134">To roll back unified contact store contacts from Exchange 2013 to Lync Server 2013</span></span>

1.  <span data-ttu-id="f15e3-135">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f15e3-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="f15e3-136">Отключите единое хранилище контактов, чтобы пользователи могли выполнить откат, чтобы они не были повторно перенесены после отката.</span><span class="sxs-lookup"><span data-stu-id="f15e3-136">Disable unified contact store for the users to be rolled back so that they will not be remigrated after rollback.</span></span> <span data-ttu-id="f15e3-137">Чтобы отключить единое хранилище контактов для отдельных пользователей, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="f15e3-137">To disable unified contact store for individual users, at the command line, type:</span></span>
    
        Set-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $False
    
    <span data-ttu-id="f15e3-138">Например:</span><span class="sxs-lookup"><span data-stu-id="f15e3-138">For example:</span></span>
    
        Set-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $False

3.  <span data-ttu-id="f15e3-139">Выполнять откат указанных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f15e3-139">Roll back the specified users.</span></span> <span data-ttu-id="f15e3-140">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f15e3-140">At the command line, type:</span></span>
    
        Invoke-CsUcsRollback -Identity "<user display name>"
    
    <span data-ttu-id="f15e3-141">Например:</span><span class="sxs-lookup"><span data-stu-id="f15e3-141">For example:</span></span>
    
        Invoke-CsUcsRollback -Identity "Ken Myer"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f15e3-142">Сначала необходимо выполнить откат пользователя Lync Server, а затем переместить почтовый ящик Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="f15e3-142">You must first roll back the Lync Server user, and then move the Exchange 2013 mailbox.</span></span> <span data-ttu-id="f15e3-143">Администратор Exchange блокирует переход на Exchange, пока не завершится откат сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f15e3-143">The Exchange administrator is blocked from rolling back Exchange until the Lync Server rollback is complete.</span></span> <span data-ttu-id="f15e3-144">Мы не рекомендуем использовать параметр – Force для принудительного отката.</span><span class="sxs-lookup"><span data-stu-id="f15e3-144">We do not recommend using the –Force option to force the rollback.</span></span> <span data-ttu-id="f15e3-145">Если вы используете этот параметр, контакты пользователей будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="f15e3-145">If you use this option, the users' contacts will be lost.</span></span>

    
    </div>

4.  <span data-ttu-id="f15e3-146">После того как вы перейдете на сервер Lync Server, администратор Exchange может восстановить пользователя Exchange из Exchange 2013 в Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="f15e3-146">After you roll back the user to Lync Server, the Exchange administrator can roll back the Exchange user from Exchange 2013 to Exchange 2010.</span></span>

<span data-ttu-id="f15e3-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f15e3-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

