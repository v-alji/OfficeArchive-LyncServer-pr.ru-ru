---
title: Перенос номеров доступа
description: Перенос номеров доступа для телефонного подключения.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate dial-in access numbers
ms:assetid: e0dfaed2-64c7-45cb-aaa9-d6117a26625d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721909(v=OCS.15)
ms:contentKeyID: 49733843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2c8bd34a30bc4b3f8999144cd84a1eee62e2ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446894"
---
# <a name="migrate-dial-in-access-numbers"></a><span data-ttu-id="df2a1-103">Перенос номеров доступа</span><span class="sxs-lookup"><span data-stu-id="df2a1-103">Migrate dial-in access numbers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df2a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df2a1-104">

<span> </span></span></span>

<span data-ttu-id="df2a1-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="df2a1-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="df2a1-106">Для миграции номеров доступа для телефонного подключения с Lync Server 2010 на Lync Server 2013 требуется запуск командлета **Move-CsApplicationEndpoint** для миграции объектов контакта.</span><span class="sxs-lookup"><span data-stu-id="df2a1-106">Migrating dial-in access numbers from Lync Server 2010 to Lync Server 2013 requires running the **Move-CsApplicationEndpoint** cmdlet to migrate the contact objects.</span></span> <span data-ttu-id="df2a1-107">В течение периода сосуществования Lync Server 2010 и Lync Server 2013 номера доступа для телефонного подключения, созданные в Lync Server 2013, будут вести себя аналогично номерам доступа для телефонного подключения, которые вы создаете в Lync Server 2010, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="df2a1-107">During the Lync Server 2010 and Lync Server 2013 coexistence period, dial-in access numbers that you created in Lync Server 2013 behave similarly to the dial-in access numbers that you create in Lync Server 2010, as described in this section.</span></span>

<span data-ttu-id="df2a1-108">Номера доступа для телефонного подключения, созданные в Lync Server 2010, но перенесенные на Lync Server 2013 или созданные в Lync Server 2013, после или после миграции, обладают следующими характеристиками.</span><span class="sxs-lookup"><span data-stu-id="df2a1-108">Dial-in access numbers that you created in Lync Server 2010 but moved to Lync Server 2013 or that you created in Lync Server 2013 before, during or after migration have the following characteristics:</span></span>

  - <span data-ttu-id="df2a1-109">Не отображаются в приглашениях на собрание Office Communications Server 2007 R2 и на странице номера доступа для подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="df2a1-109">Do not appear on Office Communications Server 2007 R2 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="df2a1-110">Отображаются в приглашениях на собрания Lync Server 2010 и на странице номера доступа для подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="df2a1-110">Appear on Lync Server 2010 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="df2a1-111">Отображаются в приглашениях на собрания Lync Server 2013 и на странице номера доступа для подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="df2a1-111">Appear on Lync Server 2013 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="df2a1-112">В средстве администрирования Office Communications Server 2007 R2 нельзя просматривать и изменять.</span><span class="sxs-lookup"><span data-stu-id="df2a1-112">Cannot be viewed or modified in the Office Communications Server 2007 R2 administrative tool.</span></span>

  - <span data-ttu-id="df2a1-113">Можно просмотреть и изменить на панели управления Lync Server 2010 и в командной консоли Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="df2a1-113">Can be viewed and modified in the Lync Server 2010 Control Panel and in Lync Server 2010 Management Shell.</span></span>

  - <span data-ttu-id="df2a1-114">Можно просмотреть и изменить на панели управления Lync Server 2013 и в командной консоли Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="df2a1-114">Can be viewed and modified in the Lync Server 2013 Control Panel and in Lync Server 2013 Management Shell.</span></span>

  - <span data-ttu-id="df2a1-115">Возможность повторной нумерации в области с помощью командлета Set-CsDialinConferencingAccessNumber с параметром priority.</span><span class="sxs-lookup"><span data-stu-id="df2a1-115">Can be re-sequenced within the region by using the Set-CsDialinConferencingAccessNumber cmdlet with the Priority parameter.</span></span>

<span data-ttu-id="df2a1-116">Перед списанием пула Lync Server 2010 необходимо завершить перенос номеров доступа с телефонным подключением, указывающих на пул Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="df2a1-116">You must finish migrating dial-in access numbers that point to a Lync Server 2010 pool before you decommission the Lync Server 2010 pool.</span></span> <span data-ttu-id="df2a1-117">Если вы не закончите перенос номеров доступа для телефонного подключения, как описано в приведенной ниже процедуре, входящие звонки на номера доступа завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="df2a1-117">If you do not complete dial-in access number migration as described in the following procedure, incoming calls to the access numbers will fail.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="df2a1-118">Эту процедуру необходимо выполнить перед списанием пула Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="df2a1-118">You must perform this procedure prior to decommissioning the Lync Server 2010 pool.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="df2a1-119">Мы рекомендуем вам перемещать номера доступа для телефонного подключения при низком использовании сети в случае короткого периода простоя службы.</span><span class="sxs-lookup"><span data-stu-id="df2a1-119">We recommend that you move dial-in access numbers when network usage is low, in case there is a short period of service outage.</span></span>



</div>

<span data-ttu-id="df2a1-120">**Для идентификации и перемещения номеров доступа с телефонным подключением**</span><span class="sxs-lookup"><span data-stu-id="df2a1-120">**To identify and move dial-in access numbers**</span></span>

1.  <span data-ttu-id="df2a1-121">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="df2a1-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="df2a1-122">Чтобы переместить каждый номер доступа с телефонным подключением в пул, размещенный на Lync Server 2013, в командной строке выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="df2a1-122">To move each dial-in access number to a pool hosted on Lync Server 2013, from the command line run:</span></span>
    
        Move-CsApplicationEndpoint -Identity <SIP URI of the access number to be moved> -Target <FQDN of the pool to which the access number is moving>

3.  <span data-ttu-id="df2a1-123">Откройте Панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df2a1-123">Open Lync Server Control Panel.</span></span>

4.  <span data-ttu-id="df2a1-124">На левой панели навигации щелкните элемент **Конференция**.</span><span class="sxs-lookup"><span data-stu-id="df2a1-124">In the left navigation bar, click **Conferencing**.</span></span>

5.  <span data-ttu-id="df2a1-125">Откройте вкладку **номер доступа для телефонного подключения** .</span><span class="sxs-lookup"><span data-stu-id="df2a1-125">Click the **Dial-in Access Number** tab.</span></span>

6.  <span data-ttu-id="df2a1-126">Убедитесь, что для пула Lync Server 2010, из которого выполняется миграция, нет номеров доступа для телефонного подключения.</span><span class="sxs-lookup"><span data-stu-id="df2a1-126">Verify that no dial-in access numbers remain for the Lync Server 2010 pool from which you are migrating.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="df2a1-127">Если все номера доступа для телефонного подключения указывают на пул Lync Server 2013, вы можете списать пул Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="df2a1-127">When all dial-in access numbers point to the Lync Server 2013 pool, you can then decommission the Lync Server 2010 pool.</span></span>

    
    </div>

<span data-ttu-id="df2a1-128">**Проверка миграции номеров доступа для телефонного подключения с помощью панели управления Lync Server**</span><span class="sxs-lookup"><span data-stu-id="df2a1-128">**Verify the dial-in access number migration using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="df2a1-129">Из учетной записи пользователя, которой назначена роль **CsUserAdministrator** или роль **CsAdministrator** , войдите на любой компьютер во внутренней среде.</span><span class="sxs-lookup"><span data-stu-id="df2a1-129">From a user account that is assigned to the **CsUserAdministrator** role or the **CsAdministrator** role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="df2a1-130">Откройте Панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df2a1-130">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="df2a1-131">На левой панели навигации щелкните элемент **Конференция**.</span><span class="sxs-lookup"><span data-stu-id="df2a1-131">In the left navigation bar, click **Conferencing**.</span></span>

4.  <span data-ttu-id="df2a1-132">Откройте вкладку **номер доступа для телефонного подключения** .</span><span class="sxs-lookup"><span data-stu-id="df2a1-132">Click the **Dial-in Access Number** tab.</span></span>

5.  <span data-ttu-id="df2a1-133">Убедитесь, что все номера доступа для телефонного подключения перенесены в пул, размещенный на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="df2a1-133">Verify all the dial-in access number are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="df2a1-134">**Проверка миграции номеров доступа для телефонного подключения с помощью командной консоли Lync Server Management Shell**</span><span class="sxs-lookup"><span data-stu-id="df2a1-134">**Verify the dial-in access number migration using Lync Server Management Shell**</span></span>

1.  <span data-ttu-id="df2a1-135">Откройте командную консоль Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df2a1-135">Open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="df2a1-136">Чтобы вернуть все номера доступа для конференц-связи с телефонным подключением, перенесенные из командной строки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="df2a1-136">To return all the dial-in conferencing access numbers migrated, from the command line run:</span></span>
    
        Get-CsDialInConferencingAccessNumber -Filter {Pool -eq "<FQDN of the pool to which the access number is moved>"}

3.  <span data-ttu-id="df2a1-137">Убедитесь, что все номера доступа для телефонного подключения перенесены в пул, размещенный на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="df2a1-137">Verify all the dial-in access numbers are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="df2a1-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df2a1-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

