---
title: 'Lync Server 2013: Установка и настройка узлов наблюдения'
description: 'Lync Server 2013: Установка и настройка узлов наблюдения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing and configuring watcher nodes
ms:assetid: 61f6deea-e3ef-4468-9be8-a65705815ebb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204943(v=OCS.15)
ms:contentKeyID: 48184284
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 87bf43e1651fabfa0137d09234d663cc905e947b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427060"
---
# <a name="installing-and-configuring-watcher-nodes-in-lync-server-2013"></a><span data-ttu-id="e2651-103">Установка и настройка узлов наблюдения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2651-103">Installing and configuring watcher nodes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2651-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2651-104">

<span> </span></span></span>

<span data-ttu-id="e2651-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="e2651-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="e2651-106">*Узлы наблюдения* — это компьютеры, периодически выполняющие синтетические транзакции Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e2651-106">*Watcher nodes* are computers that periodically run Lync Server synthetic transactions.</span></span> <span data-ttu-id="e2651-107">*Синтетические транзакции* — это командлеты Windows PowerShell, которые определяют, что ключевые сценарии для конечных пользователей (например, возможность входа в систему или возможности обмена мгновенными сообщениями) работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="e2651-107">*Synthetic transactions* are Windows PowerShell cmdlets that verify that key end user scenarios—such as the ability to sign in to the system, or the ability to exchange instant messages—are working as expected.</span></span> <span data-ttu-id="e2651-108">Для Lync Server 2013 System Center Operations Manager может выполнять синтетические транзакции, показанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e2651-108">For Lync Server 2013, System Center Operations Manager can run the synthetic transactions shown in the following table.</span></span> <span data-ttu-id="e2651-109">В таблице ниже показаны три типа виртуальных операций.</span><span class="sxs-lookup"><span data-stu-id="e2651-109">There are three different synthetic transaction types shown in the table:</span></span>

  - <span data-ttu-id="e2651-110">**По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e2651-110">**Default**.</span></span> <span data-ttu-id="e2651-111">Это искусственные транзакции, которые по умолчанию будут выполняться узлом-наблюдателем.</span><span class="sxs-lookup"><span data-stu-id="e2651-111">These are the synthetic transactions that a watcher node will run by default.</span></span> <span data-ttu-id="e2651-112">Когда вы создаете новый узел наблюдателя, у вас есть возможность указать, какие искусственные транзакции будет выполнять узел.</span><span class="sxs-lookup"><span data-stu-id="e2651-112">When you create a new watcher node, you have the option of specifying which synthetic transactions that node will run.</span></span> <span data-ttu-id="e2651-113">(Это цель параметра "тесты", используемая командлетом **New-CsWatcherNodeConfiguration** .) Если вы не используете параметр "тесты" при создании узла контрольного значения, он будет автоматически запускать все используемые по умолчанию синтетические транзакции и не будет запускать синтетические транзакции, не используемые по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2651-113">(That's the purpose of the Tests parameter used by the **New-CsWatcherNodeConfiguration** cmdlet.) If you do not use the Tests parameter when the watcher node is created, it will automatically run all the Default synthetic transactions and will not run any of the Non-default synthetic transactions.</span></span> <span data-ttu-id="e2651-114">Это означает, например, что узел наблюдателя будет настроен для выполнения теста Test-CsAddressBookService, но не будет настроен для выполнения теста Test-CsExumConnectivity.</span><span class="sxs-lookup"><span data-stu-id="e2651-114">That means, for example, that the watcher node will be configured to run the Test-CsAddressBookService test, but will not be configured to run the Test-CsExumConnectivity test.</span></span>

  - <span data-ttu-id="e2651-115">**Не по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e2651-115">**Non-default**.</span></span> <span data-ttu-id="e2651-116">Как и названия, нестандартные искусственные транзакции — это тесты, которые не выполняются по умолчанию узлами наблюдения.</span><span class="sxs-lookup"><span data-stu-id="e2651-116">As the name implies, Non-default synthetic transactions are tests that watcher nodes do not run by default.</span></span> <span data-ttu-id="e2651-117">Тем не менее, узел наблюдателя может быть активирован для выполнения любой из искусственных транзакций, не являющихся по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2651-117">However, the watcher node can be enabled to run any of the Non-default synthetic transactions.</span></span> <span data-ttu-id="e2651-118">Это можно сделать, когда вы создаете узел наблюдателя (с помощью командлета **New-CsWatcherNodeConfiguration** ) или в любое время после этого.</span><span class="sxs-lookup"><span data-stu-id="e2651-118">You can do this when you create the watcher node (by using the **New-CsWatcherNodeConfiguration** cmdlet), or at any time after that.</span></span> <span data-ttu-id="e2651-119">Многие из искусственных транзакций, не используемых по умолчанию, требуют дополнительных шагов настройки.</span><span class="sxs-lookup"><span data-stu-id="e2651-119">Many of the Non-default synthetic transactions require extra setup steps.</span></span> <span data-ttu-id="e2651-120">Подробности можно найти [в разделе Специальные инструкции по настройке для виртуальных транзакций в Lync Server 2013](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="e2651-120">For details, see [Special setup instructions for synthetic transactions in Lync Server 2013](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md).</span></span>

  - <span data-ttu-id="e2651-121">**Extended**.</span><span class="sxs-lookup"><span data-stu-id="e2651-121">**Extended**.</span></span> <span data-ttu-id="e2651-122">Расширенные тесты — это особый тип искусственной транзакции, не используемой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2651-122">Extended tests are a special type of Non-default synthetic transaction.</span></span> <span data-ttu-id="e2651-123">В отличие от других искусственных транзакций расширенные тесты могут выполняться несколько раз в течение каждого прохода.</span><span class="sxs-lookup"><span data-stu-id="e2651-123">Unlike other synthetic transactions, Extended tests can be run multiple times during each pass.</span></span> <span data-ttu-id="e2651-124">Это может быть полезно для проверки подлинности, например с несколькими коммутируемыми голосовой связью по коммутируемой телефонной сети (PSTN) для пула.</span><span class="sxs-lookup"><span data-stu-id="e2651-124">This can be useful when verifying behavior such as multiple public switched telephone network (PSTN) voice routes for a pool.</span></span> <span data-ttu-id="e2651-125">Это можно настроить, добавив несколько экземпляров расширенного теста на узел-наблюдатель.</span><span class="sxs-lookup"><span data-stu-id="e2651-125">This can be configured simply by adding multiple instances of an Extended test to a watcher node.</span></span>

<span data-ttu-id="e2651-126">Подробнее о том, как добавить другие синтетические транзакции в узел-наблюдатель, можно найти [в разделе Управление узлами-наблюдателями в Lync Server 2013](lync-server-2013-managing-watcher-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="e2651-126">For details about the process of adding other synthetic transactions to a watcher node, see [Managing watcher nodes in Lync Server 2013](lync-server-2013-managing-watcher-nodes.md).</span></span> <span data-ttu-id="e2651-127">Вы можете использовать командную консоль Lync Server для удаления искусственных транзакций из узла-наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="e2651-127">You can use the Lync Server Management Shell to remove synthetic transactions from a watcher node.</span></span>

<span data-ttu-id="e2651-128">Узлам-наблюдателям доступны следующие искусственные транзакции.</span><span class="sxs-lookup"><span data-stu-id="e2651-128">The synthetic transactions available to watcher nodes include the following:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2651-129">Имя командлета (название теста)</span><span class="sxs-lookup"><span data-stu-id="e2651-129">Cmdlet Name (Test Name)</span></span></th>
<th><span data-ttu-id="e2651-130">Описание</span><span class="sxs-lookup"><span data-stu-id="e2651-130">Description</span></span></th>
<th><span data-ttu-id="e2651-131">Тип искусственной транзакции</span><span class="sxs-lookup"><span data-stu-id="e2651-131">Synthetic Transaction Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2651-132">Test-CsAddressBookService (ABS)</span><span class="sxs-lookup"><span data-stu-id="e2651-132">Test-CsAddressBookService (ABS)</span></span></p></td>
<td><p><span data-ttu-id="e2651-133">Подтверждает, что пользователи смогут искать пользователей, которых нет в списке контактов.</span><span class="sxs-lookup"><span data-stu-id="e2651-133">Confirms that users are able to look up users that aren’t in their contact list.</span></span></p></td>
<td><p><span data-ttu-id="e2651-134">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-134">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-135">Test-CsAddressBookWebQuery (ABWQ)</span><span class="sxs-lookup"><span data-stu-id="e2651-135">Test-CsAddressBookWebQuery (ABWQ)</span></span></p></td>
<td><p><span data-ttu-id="e2651-136">Подтверждает, что пользователи могут искать пользователей, которых нет в списке контактов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="e2651-136">Confirms that users are able to look up users that aren’t in their contact list via HTTP.</span></span></p></td>
<td><p><span data-ttu-id="e2651-137">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-137">Default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-138">Test-CsIM (МГНОВЕННЫЕ СООБЩЕНИЯ)</span><span class="sxs-lookup"><span data-stu-id="e2651-138">Test-CsIM (IM)</span></span></p></td>
<td><p><span data-ttu-id="e2651-139">Проверяет, могут ли пользователи обмениваться мгновенными сообщениями друг с другом.</span><span class="sxs-lookup"><span data-stu-id="e2651-139">Confirms that users are able to send peer-to-peer instant messages.</span></span></p></td>
<td><p><span data-ttu-id="e2651-140">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-140">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-141">Test-CsP2PAV (P2PAV)</span><span class="sxs-lookup"><span data-stu-id="e2651-141">Test-CsP2PAV (P2PAV)</span></span></p></td>
<td><p><span data-ttu-id="e2651-142">Проверяет, могут ли пользователи совершать звонки другим пользователям (только сигнализация).</span><span class="sxs-lookup"><span data-stu-id="e2651-142">Confirms that users are able to place peer-to-peer audio calls (signaling only).</span></span></p></td>
<td><p><span data-ttu-id="e2651-143">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-143">Default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-144">Test-CsPresence (Присутствие)</span><span class="sxs-lookup"><span data-stu-id="e2651-144">Test-CsPresence (Presence)</span></span></p></td>
<td><p><span data-ttu-id="e2651-145">Проверяет, могут ли пользователи просматривать сведения о присутствии других пользователей.</span><span class="sxs-lookup"><span data-stu-id="e2651-145">Confirms that users are able to view other users’ presence.</span></span></p></td>
<td><p><span data-ttu-id="e2651-146">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-146">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-147">Test-CsRegistration (Регистрация)</span><span class="sxs-lookup"><span data-stu-id="e2651-147">Test-CsRegistration (Registration)</span></span></p></td>
<td><p><span data-ttu-id="e2651-148">Подтверждает, что пользователи смогут войти в Lync.</span><span class="sxs-lookup"><span data-stu-id="e2651-148">Confirms that users are able sign in to Lync.</span></span></p></td>
<td><p><span data-ttu-id="e2651-149">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-149">Default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-150">Test-CsAudioConferencingProvider (ACP)</span><span class="sxs-lookup"><span data-stu-id="e2651-150">Test-CsAudioConferencingProvider (ACP)</span></span></p></td>
<td><p><span data-ttu-id="e2651-151">Не используется в локальной версии Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2651-151">Not used with the on-premises version of Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="e2651-152">Расширенная.</span><span class="sxs-lookup"><span data-stu-id="e2651-152">Extended</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-153">Test-CsPstnPeerToPeerCall (ТСОП)</span><span class="sxs-lookup"><span data-stu-id="e2651-153">Test-CsPstnPeerToPeerCall (PSTN)</span></span></p></td>
<td><p><span data-ttu-id="e2651-154">Проверяет, могут ли пользователи совершать и принимать звонки от людей вне их предприятия (номера ТСОП).</span><span class="sxs-lookup"><span data-stu-id="e2651-154">Confirms that users are able to place and receive calls with people outside of the enterprise (PSTN numbers).</span></span></p></td>
<td><p><span data-ttu-id="e2651-155">Не по умолчанию, расширенные</span><span class="sxs-lookup"><span data-stu-id="e2651-155">Non-default, Extended</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-156">Test-CsAVConference (AvConference)</span><span class="sxs-lookup"><span data-stu-id="e2651-156">Test-CsAVConference (AvConference)</span></span></p></td>
<td><p><span data-ttu-id="e2651-157">Проверяет, могут ли пользователи создавать аудио- и видеоконференции и принимать в них участие.</span><span class="sxs-lookup"><span data-stu-id="e2651-157">Confirms that users are able to create and participate in an audio/video conference.</span></span></p></td>
<td><p><span data-ttu-id="e2651-158">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-158">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-159">Test-CsAVEdgeConnectivity (AVEdgeConnectivity)</span><span class="sxs-lookup"><span data-stu-id="e2651-159">Test-CsAVEdgeConnectivity (AVEdgeConnectivity)</span></span></p></td>
<td><p><span data-ttu-id="e2651-160">Подтверждает, что пограничные серверы A/V смогут получать соединения для одноранговых вызовов и конференций.</span><span class="sxs-lookup"><span data-stu-id="e2651-160">Confirms that the A/V Edge servers are able to accept connections for peer-to-peer calls and conference calls.</span></span></p></td>
<td><p><span data-ttu-id="e2651-161">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-161">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-162">Test-CsDataConference (DataConference)</span><span class="sxs-lookup"><span data-stu-id="e2651-162">Test-CsDataConference (DataConference)</span></span></p></td>
<td><p><span data-ttu-id="e2651-163">Подтверждает, что пользователи могут принимать участие в конференции по совместной работе с данными, собрание по сети, которое включает такие действия, как доски и опросы.</span><span class="sxs-lookup"><span data-stu-id="e2651-163">Confirms that users can participate in a data collaboration conference, an online meeting that includes activities such as whiteboards and polls.</span></span></p></td>
<td><p><span data-ttu-id="e2651-164">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-164">Non-default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-165">Test-CsExumConnectivity (ExumConnectivity)</span><span class="sxs-lookup"><span data-stu-id="e2651-165">Test-CsExumConnectivity (ExumConnectivity)</span></span></p></td>
<td><p><span data-ttu-id="e2651-166">Подтверждает, что пользователь может подключаться к единой системе обмена сообщениями Exchange (UM).</span><span class="sxs-lookup"><span data-stu-id="e2651-166">Confirms that a user can connect to Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="e2651-167">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-167">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-168">Test-CsGroupIM (GroupIM)</span><span class="sxs-lookup"><span data-stu-id="e2651-168">Test-CsGroupIM (GroupIM)</span></span></p></td>
<td><p><span data-ttu-id="e2651-169">Проверяет, могут ли пользователи отправлять мгновенные сообщения в рамках конференций и участвовать в текстовых беседах с тремя и более людьми.</span><span class="sxs-lookup"><span data-stu-id="e2651-169">Confirms that users are able to send instant messages in conferences and participate in instant message conversations with three or more people.</span></span></p></td>
<td><p><span data-ttu-id="e2651-170">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-170">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-171">Test-CsGroupIM –TestJoinLauncher (JoinLauncher)</span><span class="sxs-lookup"><span data-stu-id="e2651-171">Test-CsGroupIM –TestJoinLauncher (JoinLauncher)</span></span></p></td>
<td><p><span data-ttu-id="e2651-172">Подтверждает, что пользователи смогут создавать и присоединяться к запланированным собраниям с помощью ссылки на веб-адрес.</span><span class="sxs-lookup"><span data-stu-id="e2651-172">Confirms that users are able to create and join scheduled meetings via a web address link.</span></span></p></td>
<td><p><span data-ttu-id="e2651-173">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-173">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-174">Test-CsMCXP2PIM (MCXP2PIM)</span><span class="sxs-lookup"><span data-stu-id="e2651-174">Test-CsMCXP2PIM (MCXP2PIM)</span></span></p></td>
<td><p><span data-ttu-id="e2651-175">Проверяет, могут ли пользователи мобильных устройств регистрироваться и отправлять мгновенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2651-175">Confirms that mobile device users are able to register and send instant messages.</span></span></p></td>
<td><p><span data-ttu-id="e2651-176">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-176">Non-default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-177">Test-CsPersistentChatMessage (PersistentChatMessage)</span><span class="sxs-lookup"><span data-stu-id="e2651-177">Test-CsPersistentChatMessage (PersistentChatMessage)</span></span></p></td>
<td><p><span data-ttu-id="e2651-178">Проверяет, могут ли пользователи обмениваться сообщениями с помощью службы сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="e2651-178">Confirms that users can exchange messages by using the Persistent Chat service.</span></span></p></td>
<td><p><span data-ttu-id="e2651-179">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-179">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-180">Test-CsUnifiedContactStore (UnifiedContactStore)</span><span class="sxs-lookup"><span data-stu-id="e2651-180">Test-CsUnifiedContactStore (UnifiedContactStore)</span></span></p></td>
<td><p><span data-ttu-id="e2651-181">Проверяет возможность доступа к контактам пользователя посредством единого хранилища контактов.</span><span class="sxs-lookup"><span data-stu-id="e2651-181">Confirms that a user's contacts can be accessed through the unified contact store.</span></span> <span data-ttu-id="e2651-182">Единое хранилище контактов позволяет пользователям поддерживать один набор контактов, доступ к которому можно получить с помощью Lync 2013, Outlook и Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="e2651-182">The unified contact store provides a way for users to maintain a single set of contacts that can be accessed by using Lync 2013, Outlook, and/or Outlook Web Access.</span></span></p></td>
<td><p><span data-ttu-id="e2651-183">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-183">Non-default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-184">Test-CsXmppIM (XmppIM)</span><span class="sxs-lookup"><span data-stu-id="e2651-184">Test-CsXmppIM (XmppIM)</span></span></p></td>
<td><p><span data-ttu-id="e2651-185">Подтверждение того, что мгновенное сообщение может быть отправлено через шлюз XMPP (Extensible Messaging Protocol и протокол присутствия).</span><span class="sxs-lookup"><span data-stu-id="e2651-185">Confirms that an instant message can be sent across the XMPP (Extensible Messaging and Presence Protocol) gateway.</span></span></p></td>
<td><p><span data-ttu-id="e2651-186">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2651-186">Non-default</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2651-187">Для использования System Center Operations Manager вам не нужно устанавливать узлы наблюдателей.</span><span class="sxs-lookup"><span data-stu-id="e2651-187">You do not need to install watcher nodes in order to use System Center Operations Manager.</span></span> <span data-ttu-id="e2651-188">Если вы не установили эти узлы, вы по-прежнему можете получать оповещения в реальном времени от компонентов Lync Server 2013 при возникновении проблем.</span><span class="sxs-lookup"><span data-stu-id="e2651-188">If you do not install these nodes, you can still get real-time alerts from Lync Server 2013 components when an issue occurs.</span></span> <span data-ttu-id="e2651-189">(Пакет управления компонентом и пользовательским интерфейсом не использует узлы-наблюдатели). Однако узлы-наблюдатели необходимы для мониторинга сквозных сценариев с помощью активного пакета управления мониторингом.</span><span class="sxs-lookup"><span data-stu-id="e2651-189">(The Component and User Management Pack does not use watcher nodes.) However, watcher nodes are required if you want to monitor end-to-end scenarios by using the Active Monitoring Management pack.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e2651-190">Кроме того, администраторы могут выполнять синтетические транзакции вручную, не требуя использования или установки Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="e2651-190">Administrators can also run synthetic transactions manually, without needing to use, or install, Operations Manager.</span></span> <span data-ttu-id="e2651-191">Сведения о различных командлетах Test-Cs можно найти в <A href="https://docs.microsoft.com/powershell/module/skype/?view=skype-ps">индексе командлетов Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e2651-191">For details about the various Test-Cs cmdlets, see the <A href="https://docs.microsoft.com/powershell/module/skype/?view=skype-ps">Lync Server 2013 cmdlets index</A>.</span></span>



</div>

<span data-ttu-id="e2651-192">В зависимости от размера вашего развертывания синтетические транзакции могут использовать большой объем памяти компьютера и процессорного времени.</span><span class="sxs-lookup"><span data-stu-id="e2651-192">Depending on the size of your deployment, synthetic transactions may use a large amount of computer memory and processor time.</span></span> <span data-ttu-id="e2651-193">По этой причине мы рекомендуем использовать выделенный компьютер в качестве узла-наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="e2651-193">For this reason, we recommend that you use a dedicated computer as a watcher node.</span></span> <span data-ttu-id="e2651-194">Например, не следует настраивать сервер переднего плана так, чтобы он действовал как узел-наблюдатель.</span><span class="sxs-lookup"><span data-stu-id="e2651-194">For example, you should not configure a Front End Server to act as a watcher node.</span></span> <span data-ttu-id="e2651-195">Узлы наблюдателей должны соответствовать следующим спецификациям оборудования:</span><span class="sxs-lookup"><span data-stu-id="e2651-195">Watcher nodes should meet the following hardware specifications:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e2651-196">На том же компьютере, на котором не разразделена версия устаревшего сервера Microsoft Lync Server 2010, с узлом-наблюдателем Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e2651-196">A legacy Microsoft Lync Server 2010 watcher node cannot be collocated on the same machine with a Lync Server 2013 watcher node.</span></span> <span data-ttu-id="e2651-197">Это связано с тем, что основные системные файлы Lync Server 2010 и Lync Server 2013 нельзя установить на один и тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="e2651-197">This is because the core system files for Lync Server 2010 and Lync Server 2013 cannot be installed on the same computer.</span></span><BR><span data-ttu-id="e2651-198">Однако узлы Lync Server 2013 могут одновременно отслеживать как Lync Server 2013, так и Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="e2651-198">However, Lync Server 2013 watcher nodes can simultaneously monitor both Lync Server 2013 and Lync Server 2010.</span></span> <span data-ttu-id="e2651-199">Синтетические транзакции по умолчанию поддерживаются для обеих версий продукта.</span><span class="sxs-lookup"><span data-stu-id="e2651-199">The Default synthetic transactions are supported on both product versions.</span></span>



</div>

<span data-ttu-id="e2651-200">Узлы Lync Server 2013 могут развертываться внутри или вне Организации, чтобы убедиться в том, что:</span><span class="sxs-lookup"><span data-stu-id="e2651-200">Lync Server 2013 watcher nodes may be deployed inside or outside of an enterprise to help verify:</span></span>

  - <span></span>  
    <span data-ttu-id="e2651-201">Подключение пользователей внутри предприятия к пулам</span><span class="sxs-lookup"><span data-stu-id="e2651-201">Connectivity to pools for users inside the enterprise.</span></span>

  - <span></span>  
    <span data-ttu-id="e2651-202">Связь через сети периметра для удаленных пользователей, которые работают за пределами Организации.</span><span class="sxs-lookup"><span data-stu-id="e2651-202">Connectivity through perimeter networks for remote users who work outside the enterprise.</span></span>

  - <span></span>  
    <span data-ttu-id="e2651-203">Подключение к устройствам обеспечения связи в филиалах.</span><span class="sxs-lookup"><span data-stu-id="e2651-203">Connectivity to branch office appliances.</span></span>

  - <span></span>  
    <span data-ttu-id="e2651-204">Связь с Lync Server 2010 внутри предприятия и через сети периметра.</span><span class="sxs-lookup"><span data-stu-id="e2651-204">Connectivity to Lync Server 2010 inside the enterprise and through perimeter networks.</span></span>

<span data-ttu-id="e2651-205">Для упрощения администрирования доступны различные варианты проверки подлинности в рамках предприятия и за ее пределами.</span><span class="sxs-lookup"><span data-stu-id="e2651-205">Different authentication options are available for inside and outside of the enterprise to help simplify administration.</span></span> <span data-ttu-id="e2651-206">Подробности можно найти [в разделе Настройка узла-наблюдателя для запуска виртуальных транзакций в Lync Server 2013](lync-server-2013-configuring-a-watcher-node-to-run-synthetic-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="e2651-206">For details, see [Configuring a watcher node to run synthetic transactions in Lync Server 2013](lync-server-2013-configuring-a-watcher-node-to-run-synthetic-transactions.md).</span></span>

<span data-ttu-id="e2651-207">Чтобы настроить компьютер для работы в качестве узла-наблюдателя, необходимо выполнить указанные ниже действия после установки System Center Operations Manager и импорта пакетов управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e2651-207">To configure a computer to act as a watcher node, you must complete the following steps after you have installed System Center Operations Manager and imported the Lync Server 2013 management packs.</span></span>

<span data-ttu-id="e2651-208">Перед установкой основных файлов Lync Server 2013 и файлов агента System Center необходимо также убедиться, что компьютер-узел-наблюдатель отвечает всем требованиям, необходимым для установки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e2651-208">Before you install the Lync Server 2013 core files and the System Center agent files, you should also make sure that the watcher node computer meets all the prerequisites for installing Lync Server 2013.</span></span> <span data-ttu-id="e2651-209">Кроме того, на компьютере с узлом-наблюдателем также должны быть установлены следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="e2651-209">In addition, the watcher node computer should also have the following items installed:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2651-210">Аппаратный компонент</span><span class="sxs-lookup"><span data-stu-id="e2651-210">Hardware component</span></span></th>
<th><span data-ttu-id="e2651-211">Минимальное требование</span><span class="sxs-lookup"><span data-stu-id="e2651-211">Minimum requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2651-212">ЦП</span><span class="sxs-lookup"><span data-stu-id="e2651-212">CPU</span></span></p></td>
<td><p><span data-ttu-id="e2651-213">Один из следующих:</span><span class="sxs-lookup"><span data-stu-id="e2651-213">One of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e2651-214">Четырехъядерный 64-разрядный процессор с частотой 2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="e2651-214">64-bit processor, quad-core, 2.33 GHz or higher</span></span></p></li>
<li><p><span data-ttu-id="e2651-215">64-разрядный процессор с 2-канальным кэшем, двухъядерный, 2,33 ГГц и выше</span><span class="sxs-lookup"><span data-stu-id="e2651-215">64-bit 2-way processor, dual-core, 2.33 GHz or higher</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2651-216">Память</span><span class="sxs-lookup"><span data-stu-id="e2651-216">Memory</span></span></p></td>
<td><p><span data-ttu-id="e2651-217">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="e2651-217">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2651-218">Сетевая операционная система</span><span class="sxs-lookup"><span data-stu-id="e2651-218">Network operating system</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e2651-219">1 сетевой адаптер 1 Гбит/с</span><span class="sxs-lookup"><span data-stu-id="e2651-219">1 network adapter 1 Gbps</span></span></p></li>
<li><p><span data-ttu-id="e2651-220">Windows Server 2008 R2, Windows Server 2012 или</span><span class="sxs-lookup"><span data-stu-id="e2651-220">Windows Server 2008 R2, Windows Server 2012, or</span></span></p>
<p><span data-ttu-id="e2651-221">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e2651-221">Windows Server 2012 R2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


  - <span data-ttu-id="e2651-222">Полная версия платформы .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="e2651-222">The full version of .NET Framework 4.5.</span></span>

  - <span data-ttu-id="e2651-223">Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2651-223">Windows Identity Foundation.</span></span>

  - <span data-ttu-id="e2651-224">Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="e2651-224">Windows PowerShell 3.0.</span></span>

<span data-ttu-id="e2651-225">После того как все необходимые условия будут выполнены, вы можете настроить узел наблюдателя, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e2651-225">As soon as all these prerequisites have been met, you can configure the watcher node by:</span></span>

  - <span data-ttu-id="e2651-226">Установка основных файлов Lync Server 2013 на компьютере с узлом-наблюдателем.</span><span class="sxs-lookup"><span data-stu-id="e2651-226">Installing the Lync Server 2013 core files on the watcher node computer.</span></span>

  - <span data-ttu-id="e2651-227">Установка агента System Center Operations Manager на компьютере с узлом-наблюдателем.</span><span class="sxs-lookup"><span data-stu-id="e2651-227">Installing System Center Operations Manager agent on the watcher node computer.</span></span>

  - <span data-ttu-id="e2651-228">Запуск исполняемого файла Watchernode.msi.</span><span class="sxs-lookup"><span data-stu-id="e2651-228">Running the Watchernode.msi executable file.</span></span>

  - <span data-ttu-id="e2651-229">Использование командлетов **CsWatcherNodeConfiguration** для настройки тестовых пользователей для использования узлом-наблюдателем.</span><span class="sxs-lookup"><span data-stu-id="e2651-229">Using the **CsWatcherNodeConfiguration** cmdlets to configure test users to be employed by the watcher node.</span></span>

<span data-ttu-id="e2651-230"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2651-230"></div>

<span> </span>

</div>

</div>

</span></span></div>

