---
title: 'Lync Server 2013: создание или изменение нового правила политики для версии клиента'
description: 'Lync Server 2013: создание или изменение нового правила политики для версии клиента.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a new client version policy rule
ms:assetid: 6f879d99-8401-41e0-a562-195c890d63ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898478(v=OCS.15)
ms:contentKeyID: 50873758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11ebcf17d5cb14fd519fba8ad36be10894fabdb9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399169"
---
# <a name="create-or-modify-a-new-client-version-policy-rule-in-lync-server-2013"></a><span data-ttu-id="2a205-103">Создание или изменение правила политики для новой версии клиента в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a205-103">Create or modify a new client version policy rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a205-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a205-104">

<span> </span></span></span>

<span data-ttu-id="2a205-105">_**Тема последнего изменения:** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="2a205-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="2a205-106">Правила политики клиентской версии определяют действия, которые должны выполняться при попытке входа пользователя в систему с определенными клиентами и клиентскими версиями.</span><span class="sxs-lookup"><span data-stu-id="2a205-106">Client version policy rules define the actions that should be taken when users attempt to log on with specific clients and client versions.</span></span> <span data-ttu-id="2a205-107">Вы можете создавать и изменять индивидуальные правила для политики версии клиента с помощью панели управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2a205-107">You can create or modify individual rules for a client version policy from Lync Server 2013 Control Panel.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="2a205-108">Правила перечислены в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="2a205-108">Rules are listed in order of precedence.</span></span> <span data-ttu-id="2a205-109">Например, если у вас есть правило, разрешающее клиентам с установленной версией 1,5, а затем правило, которое блокирует работу клиентов, использующих более раннюю версию, чем 2,0, правило имеет приоритет, а клиенты с версией 1,5 могут подключаться.</span><span class="sxs-lookup"><span data-stu-id="2a205-109">For example, if you have a rule that allows clients running version 1.5 to connect, followed by a rule that blocks clients running a version earlier than 2.0, the first rule takes precedence, and clients running version 1.5 are allowed to connect.</span></span>



</div>

<div>

## <a name="to-create-or-modify-client-version-policy-rules-with-lync-server-control-panel"></a><span data-ttu-id="2a205-110">Создание или изменение правил политики версий клиента с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="2a205-110">To create or modify client version policy rules with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="2a205-111">[Создавайте и изменяйте новую политику версии клиента в Lync server 2013](lync-server-2013-create-or-modify-a-new-client-version-policy.md) с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2a205-111">[Create or modify a new client version policy in Lync Server 2013](lync-server-2013-create-or-modify-a-new-client-version-policy.md) with Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="2a205-112">На странице **изменение политики версии клиента** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="2a205-112">On the **Edit Client Version Policy** page, do one of the following:</span></span>
    
      - <span data-ttu-id="2a205-113">Нажмите кнопку **создать** , чтобы создать новое правило для версии клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-113">Click **New** to create a new client version rule.</span></span>
    
      - <span data-ttu-id="2a205-114">Выберите в списке один из определенных типов клиентов и нажмите кнопку **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="2a205-114">Click one of the defined client types in the list, and then click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2a205-115">Вы можете использовать подстановочные знаки, чтобы указать тип клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-115">You can use wildcards to indicate the client type.</span></span>

    
    </div>

3.  <span data-ttu-id="2a205-116">В **агенте пользователя** выберите тип клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-116">In **User agent**, select a client type.</span></span>

4.  <span data-ttu-id="2a205-117">В разделе **номер версии** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2a205-117">Under **Version number**, do the following:</span></span>
    
      - <span data-ttu-id="2a205-118">В поле **основная версия** введите номер, соответствующий главному выпуску клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-118">In **Major version**, type the number that corresponds to the major release of the client.</span></span>
    
      - <span data-ttu-id="2a205-119">В поле **Дополнительная версия** введите номер, соответствующий вспомогательному выпуску клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-119">In **Minor version**, type the number that corresponds to the minor release of the client.</span></span>
    
      - <span data-ttu-id="2a205-120">В поле **Сборка** введите номер, соответствующий основной и вспомогательной выпуску клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-120">In **Build**, type the number that corresponds to the major and minor release of the client.</span></span>
    
      - <span data-ttu-id="2a205-121">В поле **Обновление** введите номер, соответствующий обновленному выпуску клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-121">In **Update**, type the number that corresponds to the updated release of the client.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2a205-122">Вы можете использовать подстановочные знаки, чтобы указать номер версии клиента.</span><span class="sxs-lookup"><span data-stu-id="2a205-122">You can use wildcards to indicate the client version number.</span></span>

    
    </div>

5.  <span data-ttu-id="2a205-123">Чтобы указать операцию сопоставления для версии клиента, указанной на предыдущих шагах, в **операции сравнения** выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="2a205-123">To specify the matching operation for the client version you specified in the preceding steps, in **Comparison operation**, click one of the following:</span></span>
    
      - <span data-ttu-id="2a205-124">**Cовпадает с**</span><span class="sxs-lookup"><span data-stu-id="2a205-124">**Same as**</span></span>
    
      - <span data-ttu-id="2a205-125">**Не является**</span><span class="sxs-lookup"><span data-stu-id="2a205-125">**Is not**</span></span>
    
      - <span data-ttu-id="2a205-126">**Новее**</span><span class="sxs-lookup"><span data-stu-id="2a205-126">**Newer than**</span></span>
    
      - <span data-ttu-id="2a205-127">**Новее или совпадает с**</span><span class="sxs-lookup"><span data-stu-id="2a205-127">**Newer than or same as**</span></span>
    
      - <span data-ttu-id="2a205-128">**Старше**</span><span class="sxs-lookup"><span data-stu-id="2a205-128">**Older than**</span></span>
    
      - <span data-ttu-id="2a205-129">**Старше или совпадает с**</span><span class="sxs-lookup"><span data-stu-id="2a205-129">**Older than or same as**</span></span>

6.  <span data-ttu-id="2a205-130">Чтобы указать действие, которое будет выполняться при выполнении условий, описанных в предыдущих шагах, выберите один из указанных ниже **действий**.</span><span class="sxs-lookup"><span data-stu-id="2a205-130">To specify the action to perform when the criteria in the preceding steps are met, click one of the following in **Action**:</span></span>
    
      - <span data-ttu-id="2a205-131">Чтобы разрешить клиенту вход, нажмите кнопку **Разрешить**.</span><span class="sxs-lookup"><span data-stu-id="2a205-131">To allow the client to log on, click **Allow**.</span></span>
    
      - <span data-ttu-id="2a205-132">Чтобы разрешить клиенту входить и получать обновления из службы обновления Windows Server Update Service или центра обновления Майкрософт, нажмите кнопку **Разрешить и обновить**.</span><span class="sxs-lookup"><span data-stu-id="2a205-132">To allow the client to log on and receive updates from Windows Server Update Service or Microsoft Update, click **Allow and Upgrade**.</span></span> <span data-ttu-id="2a205-133">Это действие доступно только в том случае, если выбран агент пользователя **OC** .</span><span class="sxs-lookup"><span data-stu-id="2a205-133">This action is available only when user agent **OC** is selected.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2a205-134">При выборе этого действия уведомление появляется при следующем входе в Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="2a205-134">Selecting this action causes a notification to appear the next time users sign in to Lync 2013.</span></span> <span data-ttu-id="2a205-135">В уведомлении говорится, что обновление доступно, даже если они еще не были выпущены в службе обновления Windows Server или Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="2a205-135">The notification states that an update is available, even if updates have not yet been released to Windows Server Update Service or Microsoft Update.</span></span> <span data-ttu-id="2a205-136">Чтобы избежать путаницы, выбирайте это действие только после того, как обновления станут доступны.</span><span class="sxs-lookup"><span data-stu-id="2a205-136">To avoid confusion, you should choose this action only after updates become available.</span></span>

        
        </div>
    
      - <span data-ttu-id="2a205-137">Чтобы разрешить клиенту вход в систему и отобразить сообщение о том, где нужно скачать другую версию клиента, выберите **Разрешить с URL-адресом**.</span><span class="sxs-lookup"><span data-stu-id="2a205-137">To allow the client to log on and display a message about where to download another client version, click **Allow with URL**.</span></span> <span data-ttu-id="2a205-138">Вы задаете URL-адрес позже в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="2a205-138">You specify the URL later in this procedure.</span></span>
    
      - <span data-ttu-id="2a205-139">Чтобы запретить клиенту входить в систему, нажмите кнопку **блокировать**.</span><span class="sxs-lookup"><span data-stu-id="2a205-139">To prevent the client from logging on, click **Block**.</span></span>
    
      - <span data-ttu-id="2a205-140">Чтобы запретить клиенту входить в систему и разрешить клиенту получать обновления из службы Windows Server Update Service или центра обновления Майкрософт, нажмите кнопку **заблокировать и обновить**.</span><span class="sxs-lookup"><span data-stu-id="2a205-140">To prevent the client from logging on and allow the client to receive updates from Windows Server Update Service or Microsoft Update, click **Block and Upgrade**.</span></span> <span data-ttu-id="2a205-141">Это действие доступно только в том случае, если выбран агент пользователя **OC** .</span><span class="sxs-lookup"><span data-stu-id="2a205-141">This action is available only when user agent **OC** is selected.</span></span>
    
      - <span data-ttu-id="2a205-142">Чтобы запретить клиенту входить в систему и отобразить сообщение о том, куда можно скачать другую версию клиента, нажмите кнопку **блокировать с URL-адресом**.</span><span class="sxs-lookup"><span data-stu-id="2a205-142">To prevent the client from logging on and display a message about where to download another client version, click **Block with URL**.</span></span> <span data-ttu-id="2a205-143">Вы задаете URL-адрес позже в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="2a205-143">You specify the URL later in this procedure.</span></span>

7.  <span data-ttu-id="2a205-144">Необязательно Если вы щелкните **Разрешить с URL-** адресом или **блоком с URL-адресом** на предыдущем шаге, введите URL-адрес скачивания клиента для включения в сообщение **URL**-адрес.</span><span class="sxs-lookup"><span data-stu-id="2a205-144">(Optional) If you clicked **Allow with URL** or **Block with URL** in the previous step, type the client download URL to include in the message in **URL**.</span></span>

8.  <span data-ttu-id="2a205-145">Нажмите кнопку **ОК**, а затем — **Commit (сохранить**).</span><span class="sxs-lookup"><span data-stu-id="2a205-145">Click **OK**, and then click **Commit**.</span></span>

<span data-ttu-id="2a205-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a205-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

