---
title: 'Lync Server 2013: вопросы миграции для собраний'
description: 'Lync Server 2013: вопросы миграции для собраний.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration considerations for meetings
ms:assetid: a9807d58-99a3-4cff-b4c6-74950d106a2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412800(v=OCS.15)
ms:contentKeyID: 61097556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e238405acf7bc2a96fd2efd4cca761c1f1f258fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425586"
---
# <a name="migration-considerations-for-meetings-in-lync-server-2013"></a><span data-ttu-id="087fd-103">Вопросы миграции для собраний в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="087fd-103">Migration considerations for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="087fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="087fd-104">

<span> </span></span></span>

<span data-ttu-id="087fd-105">_**Тема последнего изменения:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="087fd-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="087fd-106">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="087fd-106">The following topics are discussed in this section:</span></span>

  - <span data-ttu-id="087fd-107">Изменения в собраниях в Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="087fd-107">Changes to meetings in Microsoft Lync Server 2013</span></span>

  - <span data-ttu-id="087fd-108">Миграция пользователей в соответствии с их потребностями в конференц-связи</span><span class="sxs-lookup"><span data-stu-id="087fd-108">Migrating users based on their conferencing needs</span></span>

  - <span data-ttu-id="087fd-109">Миграция существующих собраний и содержимого собраний</span><span class="sxs-lookup"><span data-stu-id="087fd-109">Migrating existing meetings and meeting content</span></span>

  - <span data-ttu-id="087fd-110">Взаимодействие с пользователем во время миграции Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="087fd-110">User experience during Lync Server 2010 migration</span></span>

  - <span data-ttu-id="087fd-111">Взаимодействие с пользователем во время миграции Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="087fd-111">User Experience during Office Communications Server 2007 R2 migration</span></span>

  - <span data-ttu-id="087fd-112">Совместимость Microsoft Lync 2013 с собраниями в более ранних версиях сервера</span><span class="sxs-lookup"><span data-stu-id="087fd-112">Microsoft Lync 2013 compatibility with meetings on earlier server versions</span></span>

<div>

## <a name="changes-to-meetings-in-lync-server-2013"></a><span data-ttu-id="087fd-113">Изменения собраний в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="087fd-113">Changes to Meetings in Lync Server 2013</span></span>

<span data-ttu-id="087fd-114">**Возможности Lync Server 2013.**</span><span class="sxs-lookup"><span data-stu-id="087fd-114">**Lync Server 2013 features.**</span></span>   <span data-ttu-id="087fd-115">Lync Server 2013 предлагает новые функции для конференций, которые становятся доступны пользователям после перемещения учетных записей на Lync Server 2013 и входа в систему с помощью клиента Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="087fd-115">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="087fd-116">Новые возможности, описанные в [новых функциях Конференции в Lync server 2013](lync-server-2013-new-conferencing-features.md) и [новые возможности для клиентов в Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="087fd-116">New features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="087fd-117">**URL-адрес собрания.**</span><span class="sxs-lookup"><span data-stu-id="087fd-117">**Meeting URL.**</span></span>   <span data-ttu-id="087fd-118">Как и в Lync Server 2010, для всех новых запланированных собраний в Lync Server 2013 есть префикс URL-адреса https://, а существующие собрания переносятся вместе с учетными записями пользователей.</span><span class="sxs-lookup"><span data-stu-id="087fd-118">As in Lync Server 2010, all newly scheduled meetings in Lync Server 2013 have a URL prefix of https:// and existing meetings migrate along with user accounts.</span></span> <span data-ttu-id="087fd-119">Однако Lync Server 2013 не поддерживает вызов конференции Office Communications Server 2007 R2 (префикс URL-адреса conf://) или веб-конференция (префикс URL-адреса meet://).</span><span class="sxs-lookup"><span data-stu-id="087fd-119">However, Lync Server 2013 does not support the Office Communications Server 2007 R2 conference call (conf:// URL prefix) or web conference (meet:// URL prefix).</span></span> <span data-ttu-id="087fd-120">Дополнительные сведения приведены в разделе "перенос собраний из Office Communications Server 2007 R2" ниже.</span><span class="sxs-lookup"><span data-stu-id="087fd-120">See “Migrating Meetings from Office Communications Server 2007 R2” later in this topic for more information.</span></span>

<span data-ttu-id="087fd-121">**Поддержка клиентов.**</span><span class="sxs-lookup"><span data-stu-id="087fd-121">**Client support.**</span></span>   <span data-ttu-id="087fd-122">В отличие от Lync Server 2010, Lync Server 2013 не поддерживает клиентов Office Communicator для конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="087fd-122">Unlike Lync Server 2010, Lync Server 2013 does not support Office Communicator clients for conferencing.</span></span> <span data-ttu-id="087fd-123">Вы не можете использовать следующие клиенты для присоединения к собраниям, запланированным с помощью надстройки "собрание по сети" для Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="087fd-123">You cannot use the following clients to join meetings scheduled through the Online Meeting Add-in for Lync 2013:</span></span>

  - <span data-ttu-id="087fd-124">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="087fd-124">Office Communicator 2007 R2</span></span>

  - <span data-ttu-id="087fd-125">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="087fd-125">Microsoft Office Communications Server 2007 R2 Attendant</span></span>

  - <span data-ttu-id="087fd-126">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="087fd-126">Office Communicator 2007</span></span>

  - <span data-ttu-id="087fd-127">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="087fd-127">Office Live Meeting 2007</span></span>

<span data-ttu-id="087fd-128">Во время миграции пользователи Office Communicator 2007 R2 должны использовать Lync Web App 2013 для присоединения к собраниям Lync Server 2013, пока их клиенты не будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="087fd-128">During migration, Office Communicator 2007 R2 users should use Lync Web App 2013 to join Lync Server 2013 meetings until their clients are upgraded.</span></span> <span data-ttu-id="087fd-129">Обратите внимание, что пользователи Office Communicator 2007 R2 могут по-прежнему использовать существующий клиент для Lync Server 2013 для функций присутствия и обмена мгновенными сообщениями, но функции Конференции не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="087fd-129">Note that Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

<div>


</div>

</div>

<div>

## <a name="migrating-users-based-on-their-conferencing-needs"></a><span data-ttu-id="087fd-130">Миграция пользователей в соответствии с их потребностями в конференц-связи</span><span class="sxs-lookup"><span data-stu-id="087fd-130">Migrating Users Based on Their Conferencing Needs</span></span>

<span data-ttu-id="087fd-131">**Частые организаторов собраний.**</span><span class="sxs-lookup"><span data-stu-id="087fd-131">**Frequent meeting organizers.**</span></span>   <span data-ttu-id="087fd-132">Рассматривайте организаторов на раннем этапе собрания, чтобы они могли использовать новые функции Lync Server 2013 и Lync 2013, описанные в разделе [новые возможности конференции в Lync server 2013](lync-server-2013-new-conferencing-features.md) и [новые версии для клиентов в Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="087fd-132">Consider migrating frequent meeting organizers early in the process so that they can take advantage of the new Lync Server 2013 and Lync 2013 features outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="087fd-133">**Пользователи Live Meeting.**</span><span class="sxs-lookup"><span data-stu-id="087fd-133">**Live Meeting users.**</span></span>   <span data-ttu-id="087fd-134">Если вы выполняете миграцию с Office Communications Server 2007 R2 и у вас есть пользователи, которым нужны возможности веб-конференций, специфичные для собрания по сети, особенно поддержка крупных собраний и перерывов, вы можете использовать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="087fd-134">If you are migrating from Office Communications Server 2007 R2 and you have users who need web conferencing features specific to Live Meeting—particularly support for large meetings and break-out rooms—you have the following options:</span></span>

  - <span data-ttu-id="087fd-135">Посоветуйте организаторов использовать службу Live Meeting, если она доступна в Организации.</span><span class="sxs-lookup"><span data-stu-id="087fd-135">Advise organizers to use the Live Meeting service, if available in your organization.</span></span>

  - <span data-ttu-id="087fd-136">Оставьте организаторов на веб-сайте более ранней версии Office Communications Server, чтобы они могли планировать сетевые конференции в реальном собрании на основе сервера.</span><span class="sxs-lookup"><span data-stu-id="087fd-136">Leave the organizers homed on the earlier version of Office Communications Server, so they can continue to schedule server-based Live Meeting web conferences.</span></span>

</div>

<div>

## <a name="migrating-existing-meetings-and-meeting-content"></a><span data-ttu-id="087fd-137">Миграция существующих собраний и содержимого собраний</span><span class="sxs-lookup"><span data-stu-id="087fd-137">Migrating Existing Meetings and Meeting Content</span></span>

<div>

## <a name="migrating-meetings-from-lync-server-2010"></a><span data-ttu-id="087fd-138">Перенос собраний из Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="087fd-138">Migrating Meetings from Lync Server 2010</span></span>

<span data-ttu-id="087fd-139">При перемещении пользователя из Lync Server 2010 в Lync Server 2013 следующие данные перемещаются с помощью учетной записи пользователя:</span><span class="sxs-lookup"><span data-stu-id="087fd-139">When you move a user from Lync Server 2010 to Lync Server 2013, the following information moves with the user’s account:</span></span>

  - <span data-ttu-id="087fd-140">Собрания, уже запланированные пользователем.</span><span class="sxs-lookup"><span data-stu-id="087fd-140">Meetings already scheduled by the user.</span></span> <span data-ttu-id="087fd-141">Сюда входят каталоги конференций и данные конференций.</span><span class="sxs-lookup"><span data-stu-id="087fd-141">This includes conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="087fd-142">Персональный идентификационный номер пользователя (ПИН-код).</span><span class="sxs-lookup"><span data-stu-id="087fd-142">The user’s personal identification number (PIN).</span></span> <span data-ttu-id="087fd-143">Текущий ПИН-код пользователя продолжает работать, пока не истечет срок действия или пользователь запросит новый ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="087fd-143">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="087fd-144">Однако указанные ниже сведения об учетной записи пользователя не перемещаются на новый сервер.</span><span class="sxs-lookup"><span data-stu-id="087fd-144">However, the following user account information does not move to the new server:</span></span>

  - <span data-ttu-id="087fd-145">Содержимое собрания (например, презентации PowerPoint, содержимое доски и данные опросов)</span><span class="sxs-lookup"><span data-stu-id="087fd-145">Meeting content, for example PowerPoint presentations, whiteboard content, and poll data</span></span>

<span data-ttu-id="087fd-146">Чтобы переместить содержимое, к которому предоставлен общий доступ в собраниях, используйте параметр MoveMeetingContent командлета Move-CsUser.</span><span class="sxs-lookup"><span data-stu-id="087fd-146">To move the content that has been shared in meetings, use the MoveMeetingContent parameter of the Move-CsUser cmdlet.</span></span> <span data-ttu-id="087fd-147">Подробнее об использовании этого командлета можно найти в документации по командлетам Lync Server 2013, описанным в разделе [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) .</span><span class="sxs-lookup"><span data-stu-id="087fd-147">For details about using this cmdlet, see [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) in the Lync Server 2013 cmdlets documentation.</span></span>

</div>

<div>

## <a name="migrating-meetings-from-office-communications-server-2007-r2"></a><span data-ttu-id="087fd-148">Миграция собраний из Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="087fd-148">Migrating Meetings from Office Communications Server 2007 R2</span></span>

<span data-ttu-id="087fd-149">Office Communications Server 2007 R2 — это либо телефонные конференции (префикс URL-адреса conf://), либо веб-конференции (meet://prefix URL-адрес).</span><span class="sxs-lookup"><span data-stu-id="087fd-149">Office Communications Server 2007 R2 meetings are either conference calls (conf:// URL prefix) or web conferences (meet:// URL prefix).</span></span> <span data-ttu-id="087fd-150">Lync Server 2013 не поддерживает эти более ранние конференции conf://и meet://, и они не переносятся вместе с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="087fd-150">Lync Server 2013 does not support these earlier conf:// and meet:// conferences, and they are not migrated along with the user account.</span></span> <span data-ttu-id="087fd-151">После миграции вы должны попросить пользователей обновить ссылки для запланированных собраний по сети.</span><span class="sxs-lookup"><span data-stu-id="087fd-151">After migration, you should instruct users to update the links for any online meetings they have scheduled.</span></span> <span data-ttu-id="087fd-152">Они могут сделать это после установки клиента Lync 2013, открыв запланированное приглашение на собрание (которое обновляет URL-адрес собрания) и повторно отправляет приглашение участникам.</span><span class="sxs-lookup"><span data-stu-id="087fd-152">They can do this after installing the Lync 2013 client by opening a scheduled meeting invitation—which updates the meeting URL—and resending the invitation to participants.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-lync-server-2010-migration"></a><span data-ttu-id="087fd-153">Взаимодействие с пользователем во время миграции Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="087fd-153">User Experience during Lync Server 2010 Migration</span></span>

<span data-ttu-id="087fd-154">В этом разделе приведены краткие сведения о средствах конференц-связи пользователей при переходе с Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="087fd-154">This section provides a summary of users’ conferencing experience when migrating from Lync 2010.</span></span> <span data-ttu-id="087fd-155">Дополнительные сведения о том, как пользователи Lync Server 2013 могут сосуществовать и взаимодействовать с предыдущими версиями клиента и сервера, приведены [в разделе взаимодействие с клиентами в Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="087fd-155">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="joining-lync-server-2010-meetings-with-a-lync-2013-client"></a><span data-ttu-id="087fd-156">Присоединение к собраниям Lync Server 2010 с помощью клиента Lync 2013</span><span class="sxs-lookup"><span data-stu-id="087fd-156">Joining Lync Server 2010 Meetings with a Lync 2013 Client</span></span>

<span data-ttu-id="087fd-157">Во время миграции с Lync Server 2010 может возникнуть срок сосуществования, когда пользователи присоединяются к собраниям Lync Server 2010 с помощью клиента Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="087fd-157">During migration from Lync Server 2010, there may be a period of coexistence when users join Lync Server 2010 meetings with a Lync 2013 client.</span></span> <span data-ttu-id="087fd-158">Эти пользователи имеют доступ к функциям клиента Lync 2013 со следующими исключениями:</span><span class="sxs-lookup"><span data-stu-id="087fd-158">These users have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="087fd-159">В параметрах управления **участниками** , доступ к которым осуществляется с помощью значка "люди" в окне собрания, не будет работать параметр " **мгновенное сообщение о собрании** ".</span><span class="sxs-lookup"><span data-stu-id="087fd-159">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="087fd-160">Представление коллекции не может работать в видеоконференциях.</span><span class="sxs-lookup"><span data-stu-id="087fd-160">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="087fd-161">Пользователь видит только активный динамик, а не все динамики.</span><span class="sxs-lookup"><span data-stu-id="087fd-161">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="087fd-162">В списке выбора параметров **разметки** недоступен **режим коллекции**</span><span class="sxs-lookup"><span data-stu-id="087fd-162">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="087fd-163">Список участников по умолчанию отображается в видеоконференциях.</span><span class="sxs-lookup"><span data-stu-id="087fd-163">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="087fd-164">Если щелкнуть пользователя правой кнопкой мыши в списке участников, вы не **сможете получить** **доступ к** параметрам управления участниками коллекции.</span><span class="sxs-lookup"><span data-stu-id="087fd-164">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-office-communications-server-2007-r2-migration"></a><span data-ttu-id="087fd-165">Взаимодействие с пользователем во время миграции Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="087fd-165">User Experience during Office Communications Server 2007 R2 Migration</span></span>

<span data-ttu-id="087fd-166">В этом разделе приведены краткие сведения о средствах конференц-связи пользователей при переходе с Office Communications Server 2007 R2 до и после установки Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="087fd-166">This section provides a summary of users’ conferencing experience when migrating from Office Communications Server 2007 R2, both before and after Lync 2013 is installed.</span></span> <span data-ttu-id="087fd-167">Дополнительные сведения о том, как пользователи Lync Server 2013 могут сосуществовать и взаимодействовать с предыдущими версиями клиента и сервера, приведены [в разделе взаимодействие с клиентами в Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="087fd-167">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="after-user-account-is-migrated-before-lync-2013-is-installed"></a><span data-ttu-id="087fd-168">После миграции учетной записи пользователя до установки Lync 2013</span><span class="sxs-lookup"><span data-stu-id="087fd-168">After User Account is Migrated, Before Lync 2013 Is Installed</span></span>

<span data-ttu-id="087fd-169">После того как пользователь будет перенесен на сервер Lync Server 2013, но перед установкой новых клиентов, пользователи Office Communicator 2007 R2 смогут продолжать использовать существующий клиент для Lync Server 2013 для функций присутствия и обмена мгновенными сообщениями, но функции Конференции не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="087fd-169">After a user is migrated to the Lync Server 2013 server, but before new clients are installed, Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

</div>

<div>

## <a name="after-user-account-is-migrated-after-lync-2013-is-installed"></a><span data-ttu-id="087fd-170">После того как вы переносите учетную запись пользователя, после установки Lync 2013</span><span class="sxs-lookup"><span data-stu-id="087fd-170">After User Account is Migrated, After Lync 2013 Is Installed</span></span>

<span data-ttu-id="087fd-171">При установке Lync 2013 для пользователя, для которого выполнена миграция, будет установлена надстройка "собрание по сети" для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="087fd-171">When a migrated user installs Lync 2013, the Online Meeting Add-in for Lync 2013 is installed too.</span></span> <span data-ttu-id="087fd-172">Ниже перечислены некоторые последствия.</span><span class="sxs-lookup"><span data-stu-id="087fd-172">This has the following effects:</span></span>

  - <span data-ttu-id="087fd-173">Во всех запланированных собраниях используется новый формат собрания, который использует https://адрес вместо старого адреса meet://Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="087fd-173">All subsequently scheduled meetings use the new meeting format, which uses an https:// address instead of the legacy meet:// Live Meeting address.</span></span>

  - <span data-ttu-id="087fd-174">При развертывании Lync 2013 администратор может удалить надстройку конференц-связи для Microsoft Office Outlook, которая используется для планирования сервера Live Meeting и собраний на основе служб.</span><span class="sxs-lookup"><span data-stu-id="087fd-174">In an IT-managed deployment of Lync 2013, the administrator has the option of uninstalling the Conferencing Add-in for Microsoft Office Outlook, which is used to schedule Live Meeting server and service-based meetings.</span></span> <span data-ttu-id="087fd-175">Однако вы можете иметь пользователей, которые должны продолжать планировать собрания в службе Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="087fd-175">However, you may have users who need to continue to schedule Live Meeting service meetings.</span></span> <span data-ttu-id="087fd-176">В этом случае обе надстройки можно разрешать сосуществование.</span><span class="sxs-lookup"><span data-stu-id="087fd-176">In this case, you can allow both add-ins to coexist.</span></span>

</div>

<div>

## <a name="meetings-with-federated-organizations-that-use-previous-clients"></a><span data-ttu-id="087fd-177">Собрания с федеративными организациями, которые используют предыдущие клиенты</span><span class="sxs-lookup"><span data-stu-id="087fd-177">Meetings with Federated Organizations that Use Previous Clients</span></span>

<span data-ttu-id="087fd-178">Пользователи в федеративных организациях, использующих Microsoft Office Communicator 2007, не могут присоединиться к собраниям Lync Server 2013 в вашей организации, если эти собрания заблокированы организатором.</span><span class="sxs-lookup"><span data-stu-id="087fd-178">Users in federated organizations who are using Microsoft Office Communicator 2007 cannot join Lync Server 2013 meetings in your organization if those meetings are locked by the organizer.</span></span> <span data-ttu-id="087fd-179">Вы должны перепланировать эти собрания в Lync Server 2013, чтобы присоединиться к собранию с помощью нового URL-адреса собрания https://, в котором они могут использовать Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="087fd-179">You have to reschedule these meetings in Lync Server 2013 so when federated participants join the meeting by using the new https:// meeting URL, they can use Lync Web App.</span></span>

<span data-ttu-id="087fd-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="087fd-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

