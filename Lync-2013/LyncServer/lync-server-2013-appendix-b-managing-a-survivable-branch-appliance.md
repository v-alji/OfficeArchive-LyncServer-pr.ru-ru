---
title: 'Lync Server 2013: Приложение B. Управление устройством для обеспечения связи в филиалах'
description: 'Lync Server 2013: Приложение B: Управление бесперебойной подразделением.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Appendix B: Managing a Survivable Branch Appliance'
ms:assetid: 2ec9d505-6d39-491c-9524-8cf36866b855
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425797(v=OCS.15)
ms:contentKeyID: 48183773
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e66d97f538ee751d7bf12b0d0f70ff3a3f5576b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439942"
---
# <a name="appendix-b-managing-a-survivable-branch-appliance-in-lync-server-2013"></a><span data-ttu-id="8b4d7-103">Приложение B. Управление устройством для обеспечения связи в филиалах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b4d7-103">Appendix B: Managing a Survivable Branch Appliance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b4d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b4d7-104">

<span> </span></span></span>

<span data-ttu-id="8b4d7-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="8b4d7-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="8b4d7-106">В этой статье описаны процедуры для управления бесперебойно работающим устройством ветвления.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-106">This topic describes the procedures for managing a Survivable Branch Appliance.</span></span> <span data-ttu-id="8b4d7-107">В частности, замена и переименование бесперебойно работающего устройства филиалов и изменение пула интерфейсов Lync Server 2013, с которым может быть связано устройство с бесперебойной подразделением.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-107">Specifically, how to replace and rename a Survivable Branch Appliance, and how to change the Lync Server 2013 Front End pool that the Survivable Branch Appliance is associated with.</span></span>

<div>

## <a name="to-replace-a-survivable-branch-appliance"></a><span data-ttu-id="8b4d7-108">Замена бесперебойно работающего устройства филиала</span><span class="sxs-lookup"><span data-stu-id="8b4d7-108">To Replace a Survivable Branch Appliance</span></span>

1.  <span data-ttu-id="8b4d7-109">Остановите все службы Lync Server 2013 на устройстве с бесперебойной подразделением.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-109">Stop all Lync Server 2013 services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="8b4d7-110">(См. документацию поставщика устройства филиала.)</span><span class="sxs-lookup"><span data-stu-id="8b4d7-110">(See the Survivable Branch Appliance vendor documentation.)</span></span>

2.  <span data-ttu-id="8b4d7-111">Рекомендуется Удалите из домена бесперебойно работающее устройство ветвления.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-111">(Recommended) Remove the Survivable Branch Appliance from the domain.</span></span>

3.  <span data-ttu-id="8b4d7-112">Удалите бесперебойно работающее устройство управления филиалом в доменных службах Active Directory, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-112">Delete the Survivable Branch Appliance computer object in Active Directory Domain Services, by following these steps:</span></span>
    
      - <span data-ttu-id="8b4d7-113">Войдите в систему на рядовом сервере, который входит в группу администраторов предприятия.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-113">Log on to a member server as a member of the Enterprise Admins group.</span></span>
    
      - <span data-ttu-id="8b4d7-114">Нажмите кнопку **Пуск** и выберите пункт **Администрирование**, а затем — **Пользователи и компьютеры Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-114">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>
    
      - <span data-ttu-id="8b4d7-115">Щелкните правой кнопкой мыши бесперебойно работающее устройство филиала и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-115">Right-click the Survivable Branch Appliance object, and click **Delete**.</span></span>

4.  <span data-ttu-id="8b4d7-116">Снова добавьте объект компьютера, который вы проявляется устройством филиала.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-116">Add the Survivable Branch Appliance computer object again.</span></span> <span data-ttu-id="8b4d7-117">(См. раздел [Добавление работающего устройства филиалов в Active Directory в Lync Server 2013](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md).)</span><span class="sxs-lookup"><span data-stu-id="8b4d7-117">(See [Add a Survivable Branch Appliance to Active Directory in Lync Server 2013](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md).)</span></span>

5.  <span data-ttu-id="8b4d7-118">Дождитесь, пока репликация службы каталогов Active Directory не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-118">Wait for Active Directory replication to take place.</span></span>

6.  <span data-ttu-id="8b4d7-119">Откройте командную консоль Lync Server Management Shell и введите **Enable-CSTopology**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-119">Open the Lync Server Management Shell, and type **Enable-CSTopology**.</span></span>

7.  <span data-ttu-id="8b4d7-120">Подключите новое работающее устройство филиала к сети и выполните действия, описанные в статье Развертывание работающего устройства филиала [или сервера с помощью Lync server 2013 — центральные задачи сайта](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) и развертывание работающего [устройства филиала или сервера с помощью Lync Server 2013-Branch Task site](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d7-120">Connect the new Survivable Branch Appliance to the network, and follow the steps in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) and [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span></span>

</div>

<div>

## <a name="to-rename-a-survivable-branch-appliance"></a><span data-ttu-id="8b4d7-121">Переименование бесперебойно работающего устройства филиалов</span><span class="sxs-lookup"><span data-stu-id="8b4d7-121">To Rename a Survivable Branch Appliance</span></span>

1.  <span data-ttu-id="8b4d7-122">Перемещение пользователей на центральный сайт.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-122">Move users to the central site.</span></span> <span data-ttu-id="8b4d7-123">Подробности можно найти [в разделе Перемещение пользователей в другой пул в Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d7-123">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

2.  <span data-ttu-id="8b4d7-124">Остановите все службы Lync Server 2013 на устройстве с бесперебойной подразделением.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-124">Stop all Lync Server 2013 services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="8b4d7-125">(См. документацию поставщика устройства филиала.)</span><span class="sxs-lookup"><span data-stu-id="8b4d7-125">(See the Survivable Branch Appliance vendor documentation.)</span></span>

3.  <span data-ttu-id="8b4d7-126">Удалите бесперебойную ветвь устройства из топологии, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-126">Remove the Survivable Branch Appliance from the topology, by following these steps:</span></span>
    
      - <span data-ttu-id="8b4d7-127">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server**, а затем — **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-127">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="8b4d7-128">В дереве консоли разверните узел **сайты филиалов**, выберите работающее устройство филиала, а затем нажмите кнопку **Удалить** на панели действий.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-128">In the console tree, expand **Branch Sites**, click the Survivable Branch Appliance, and then click **Delete** on the Action pane.</span></span>

4.  <span data-ttu-id="8b4d7-129">Удалите из домена бесперебойно работающее устройство ветвления.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-129">Remove the Survivable Branch Appliance from the domain.</span></span>

5.  <span data-ttu-id="8b4d7-130">Удалите бесперебойно работающее устройство управления филиалом в Active Directory, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-130">Delete the Survivable Branch Appliance computer object in Active Directory, by following these steps:</span></span>
    
      - <span data-ttu-id="8b4d7-131">Войдите в систему на контроллере домена, который является членом группы администраторов предприятия.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-131">Log on to a domain controller as a member of the Enterprise Admins group.</span></span>
    
      - <span data-ttu-id="8b4d7-132">Нажмите кнопку **Пуск** и выберите пункт **Администрирование**, а затем — **Пользователи и компьютеры Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-132">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>
    
      - <span data-ttu-id="8b4d7-133">Щелкните правой кнопкой мыши бесперебойно работающее устройство филиала и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-133">Right-click the Survivable Branch Appliance object, and click **Delete**.</span></span>

6.  <span data-ttu-id="8b4d7-134">Восстановите работающее устройство филиала на заводские значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-134">Restore the Survivable Branch Appliance to factory defaults.</span></span> <span data-ttu-id="8b4d7-135">(См. документацию поставщика устройства филиала.)</span><span class="sxs-lookup"><span data-stu-id="8b4d7-135">(See the Survivable Branch Appliance vendor documentation.)</span></span>

7.  <span data-ttu-id="8b4d7-136">Выполните действия, описанные в статье Развертывание работающего [устройства филиала или сервера с помощью Lync server 2013 — централизованные задачи сайта](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) и развертывание работающего [устройства филиала или сервера с помощью Lync Server 2013-Branch Task site](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d7-136">Follow the steps in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) and [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span></span>

8.  <span data-ttu-id="8b4d7-137">Переместите пользователей на переименованную бесперебойную ветвь устройства.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-137">Move users to the renamed Survivable Branch Appliance.</span></span> <span data-ttu-id="8b4d7-138">Подробности можно найти [в разделе Перемещение пользователей в другой пул в Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d7-138">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

</div>

<div>

## <a name="to-change-the-lync-server-front-end-pool-that-the-survivable-branch-appliance-is-associated-with"></a><span data-ttu-id="8b4d7-139">Изменение пула переднего плана Lync Server, связанного с устройством с бесперебойной подразделением</span><span class="sxs-lookup"><span data-stu-id="8b4d7-139">To Change the Lync Server Front End Pool that the Survivable Branch Appliance Is Associated With</span></span>

1.  <span data-ttu-id="8b4d7-140">Перемещайте пользователей из работающего устройства филиала в пул переднего плана сервера Lync Server на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-140">Move users from the Survivable Branch Appliance to the Lync Server Front End pool at the central site.</span></span> <span data-ttu-id="8b4d7-141">Подробности можно найти [в разделе Перемещение пользователей в другой пул в Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d7-141">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

2.  <span data-ttu-id="8b4d7-142">Остановите все службы Lync Server на устройстве с бесперебойной подразделением.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-142">Stop all Lync Server services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="8b4d7-143">(См. документацию поставщика устройства филиала).</span><span class="sxs-lookup"><span data-stu-id="8b4d7-143">(See the Survivable Branch Appliance vendor documentation).</span></span>

3.  <span data-ttu-id="8b4d7-144">Обновите пул переднего плана Lync Server, с которым связано работающее устройство филиала, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-144">Update the Lync Server Front End pool that the Survivable Branch Appliance is associated with, by following these steps:</span></span>
    
      - <span data-ttu-id="8b4d7-145">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server**, а затем — **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-145">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="8b4d7-146">Разверните **сайты филиалов**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-146">Expand **Branch Sites**.</span></span>
    
      - <span data-ttu-id="8b4d7-147">Щелкните правой кнопкой мыши бесперебойно работающее устройство филиала, чтобы изменить его, и выберите команду **изменить свойства** .</span><span class="sxs-lookup"><span data-stu-id="8b4d7-147">Right-click the Survivable Branch Appliance object to modify, and click **Edit Properties**</span></span>
    
      - <span data-ttu-id="8b4d7-148">В разделе устойчивость выберите новый пул переднего плана, с которым нужно связать устройство, которое может быть установлено, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-148">Under Resiliency, select the new Front End pool the Survivable Branch Appliance is to be associated to, and then click **Next**.</span></span>
    
      - <span data-ttu-id="8b4d7-149">В дереве консоли щелкните правой кнопкой мыши новое работающее устройство филиала, выберите пункт **топология** и нажмите кнопку **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-149">In the console tree, right-click the new Survivable Branch Appliance, click **Topology**, and then click **Publish**.</span></span>

4.  <span data-ttu-id="8b4d7-150">Перезапустите все службы Lync Server на устройстве с бесперебойной подразделением.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-150">Restart all Lync Server Services on the Survivable Branch Appliance.</span></span>

5.  <span data-ttu-id="8b4d7-151">Протестируйте бесперебойно работающее устройство филиалов.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-151">Test the Survivable Branch Appliance.</span></span> <span data-ttu-id="8b4d7-152">Подробности можно найти в разделе [домашние пользователи на устройстве с бесперебойной филиалом или на сервере в Lync server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d7-152">For details, see [Home users on a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span></span>

6.  <span data-ttu-id="8b4d7-153">Перемещение пользователей из пула переднего плана Lync Server на центральном сайте в бесперебойно работающее устройство филиала.</span><span class="sxs-lookup"><span data-stu-id="8b4d7-153">Move users from the Lync Server Front End pool at the central site to the Survivable Branch Appliance.</span></span>

<span data-ttu-id="8b4d7-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b4d7-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

