---
title: 'Lync Server 2013: взаимодействие клиентов в Lync 2013'
description: 'Lync Server 2013: взаимодействие с клиентами в Lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client interoperability in Lync 2013
ms:assetid: 0f126571-91a2-45d5-855c-1e4ddb45fc04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204672(v=OCS.15)
ms:contentKeyID: 48183417
ms.date: 03/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea6e90d9479f03dd6d946787e70a2b3cc078699
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434923"
---
# <a name="client-interoperability-in-lync-2013"></a><span data-ttu-id="8dcc6-103">Взаимодействие клиентов в Lync 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-103">Client interoperability in Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8dcc6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8dcc6-104">

<span> </span></span></span>

<span data-ttu-id="8dcc6-105">_**Тема последнего изменения:** 2016-03-04_</span><span class="sxs-lookup"><span data-stu-id="8dcc6-105">_**Topic Last Modified:** 2016-03-04_</span></span>

<span data-ttu-id="8dcc6-106">В этой статье рассказывается о том, как использовать клиенты Microsoft Lync Server 2013 для совместной работы и взаимодействия с клиентами из более ранних версий Lync Server и Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-106">This topic discusses the ability of Microsoft Lync Server 2013 clients to coexist and interact with clients from earlier versions of Lync Server and Office Communications Server.</span></span>

<div>

## <a name="server-and-client-compatibility"></a><span data-ttu-id="8dcc6-107">Совместимость сервера и клиента</span><span class="sxs-lookup"><span data-stu-id="8dcc6-107">Server and Client Compatibility</span></span>

<span data-ttu-id="8dcc6-108">В следующей таблице показаны поддерживаемые комбинации версий клиентов и сервера.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-108">The following table shows the supported combinations of client versions and server versions.</span></span> <span data-ttu-id="8dcc6-109">В этой таблице показано, поддерживается ли вход, когда клиент пытается подключиться к указанному серверу.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-109">This table indicates whether sign-in is supported when the client attempts to connect to the server indicated.</span></span> <span data-ttu-id="8dcc6-110">Lync Server 2013 поддерживает предыдущую версию клиента.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-110">Lync Server 2013 supports the previous client version.</span></span> <span data-ttu-id="8dcc6-111">Кроме того, в отличие от предыдущих выпусков, Lync Server 2010 поддерживает новые клиенты Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-111">Also, unlike previous releases, Lync Server 2010 supports the new Lync 2013 clients.</span></span> <span data-ttu-id="8dcc6-112">Это позволяет организациям, работающим с Lync Server 2010, развертывать новые клиенты независимо от того, как Lync Server выполняет обновление.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-112">This allows organizations who are upgrading from Lync Server 2010 to roll out new clients independent of Lync Server upgrades.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8dcc6-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="8dcc6-113">Client</span></span></th>
<th><span data-ttu-id="8dcc6-114">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-114">Lync Server 2013</span></span></th>
<th><span data-ttu-id="8dcc6-115">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-115">Lync Server 2010</span></span></th>
<th><span data-ttu-id="8dcc6-116">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="8dcc6-116">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-117">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-117">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-118">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-119">Supported5</span><span class="sxs-lookup"><span data-stu-id="8dcc6-119">Supported5</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-120">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-121">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="8dcc6-121">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-122">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-123">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-123">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-124">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-124">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-125">Lync Web App 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-125">Lync Web App 2013</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-126">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-127">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-127">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-128">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-128">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-129">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-129">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-130">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-131">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-132">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-132">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-133">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="8dcc6-133">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-134">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-135">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-135">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-136">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-136">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-137">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-137">Lync 2010 Group Chat</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-138">Supported1</span><span class="sxs-lookup"><span data-stu-id="8dcc6-138">Supported1</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-139">Supported2</span><span class="sxs-lookup"><span data-stu-id="8dcc6-139">Supported2</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-140">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8dcc6-140">Not Applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-141">Lync Web App 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-141">Lync Web App 2010</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-142">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-142">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-143">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-143">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-144">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-144">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-145">Участник Lync 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-145">Lync 2010 Attendee</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-146">Не Supported3</span><span class="sxs-lookup"><span data-stu-id="8dcc6-146">Not Supported3</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-147">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-147">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-148">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-148">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-149">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="8dcc6-149">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-150">Interoperable4</span><span class="sxs-lookup"><span data-stu-id="8dcc6-150">Interoperable4</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-151">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-151">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-152">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-152">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-153">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="8dcc6-153">Microsoft Office Communications Server 2007 R2 Attendant</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-154">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-154">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-155">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-156">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-156">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-157">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="8dcc6-157">Office Communicator 2007</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-158">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-158">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-159">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-159">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-160">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-160">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-161">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="8dcc6-161">Office Live Meeting 2007</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-162">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-162">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-163">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-163">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-164">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-164">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-165">Приложение Lync из Магазина Windows</span><span class="sxs-lookup"><span data-stu-id="8dcc6-165">Lync Windows Store app</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-166">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-166">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-167">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-167">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-168">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-168">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8dcc6-169">1For подробные сведения можно найти в разделе [Миграция с Lync server 2010, группового чата или Office Communications Server 2007 R2 Group Chat на Lync server 2013 и на сервер сохраняемого чата](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc6-169">1For details, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="8dcc6-170">2In Microsoft Lync Server 2010 вы можете воспользоваться функцией группового чата с помощью сервера группового чата, стороннего надежного приложения для Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-170">2In Microsoft Lync Server 2010, group chat functionality was available with Group Chat Server, a third-party trusted application for Lync Server 2010.</span></span> <span data-ttu-id="8dcc6-171">Клиенты Lync 2013 несовместимы с Lync Server 2010, групповой чат.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-171">Lync 2013 clients are not compatible with Lync Server 2010, Group Chat.</span></span>

<span data-ttu-id="8dcc6-172">3Lync веб-приложение 2013 теперь обеспечивает полное участие в собрании, в том числе звуковое сопровождение и видео компьютера, и считается заменой для участника Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-172">3Lync Web App 2013 now provides a full in-meeting experience, including computer audio and video, and is considered the replacement for Lync 2010 Attendee.</span></span> <span data-ttu-id="8dcc6-173">Участники Lync 2010 будут подключаться к Lync Server 2013 только в том случае, если вы используете неподдерживаемый браузер (Internet Explorer 6 или Internet Explorer 7) и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-173">Lync 2010 Attendee will connect to Lync Server 2013 only when you are using an unsupported browser (Internet Explorer 6 or Internet Explorer 7) and Windows XP.</span></span>

<span data-ttu-id="8dcc6-174">4The функции присутствия и обмена мгновенными сообщениями в Office Communicator 2007 R2 совместимы с Lync Server 2013, но возможности конференции не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-174">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="8dcc6-175">При переходе с Office Communications Server 2007 R2 подходящими для обеспечения взаимодействия и обмена мгновенными сообщениями является Office Communicator 2007 R2, но пользователи должны использовать Lync Web App 2013, чтобы присоединиться к собраниям Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-175">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

<span data-ttu-id="8dcc6-176">5 об ограничениях читайте в статье поддержка функции Конференции для клиентов Lync 2013 в Lync Server 2010 для собраний ниже.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-176">5 For limitations, see "Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings" later in this topic.</span></span>

</div>

<div>

## <a name="interoperability-among-clients"></a><span data-ttu-id="8dcc6-177">Взаимодействие между клиентами</span><span class="sxs-lookup"><span data-stu-id="8dcc6-177">Interoperability among Clients</span></span>

<span data-ttu-id="8dcc6-178">Благодаря выпуску Lync Server 2013 различные клиентские версии могут беспрепятственно взаимодействовать в одноранговых сценариях и конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-178">With the Lync Server 2013 release, various client versions can interact seamlessly in both peer-to-peer and conferencing scenarios.</span></span> <span data-ttu-id="8dcc6-179">Этот раздел содержит сведения о доступности функций при взаимодействии пользователей с другими пользователями, использующими разные версии клиентов и серверов.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-179">This section discusses feature availability when users interact with other users who are using different versions of clients and servers.</span></span>

<div>

## <a name="peer-to-peer-feature-support"></a><span data-ttu-id="8dcc6-180">Поддержка одноранговых функций</span><span class="sxs-lookup"><span data-stu-id="8dcc6-180">Peer-to-Peer Feature Support</span></span>

<span data-ttu-id="8dcc6-181">Одноранговые функции поддерживаются для пользователей, которые находятся в разных версиях сервера и используют разные клиентские версии.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-181">Peer-to-peer features are supported for users who are homed on different versions of the server and who are using different client versions.</span></span> <span data-ttu-id="8dcc6-182">Взаимодействие с конечным пользователем и доступные возможности соответствуют возможностям клиента пользователя и версии сервера, на котором пользователь вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-182">The end-user experience and available features are consistent with the capabilities of the user’s client and the version of the server the user is signed in to.</span></span> <span data-ttu-id="8dcc6-183">Другими словами:</span><span class="sxs-lookup"><span data-stu-id="8dcc6-183">In other words:</span></span>

  - <span data-ttu-id="8dcc6-184">Если пользователь вошел в Lync Server 2013 с более ранней версией клиента, он будет использовать тот же интерфейс, что и для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-184">If a user is signed in to Lync Server 2013 with an older client, the user will have the same experience he or she is used to.</span></span> <span data-ttu-id="8dcc6-185">Новые функции, представленные в Lync Server 2013, будут недоступны до тех пор, пока клиент пользователя не будет обновлен.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-185">None of the new features introduced in Lync Server 2013 will be available until the user’s client is upgraded.</span></span> <span data-ttu-id="8dcc6-186">Примеры: Просмотр коллекции видео, видео в формате HD, обновленный общий доступ к PowerPoint, а также возможность отключения звука и видео всех участников во время ввода собрания.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-186">Examples include video gallery view, HD video, updated PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="8dcc6-187">Новые функции, описанные в разделе [новые возможности конференции в Lync server 2013](lync-server-2013-new-conferencing-features.md) , и [новые возможности для клиентов в Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc6-187">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

  - <span data-ttu-id="8dcc6-188">Если пользователь вошел в Lync Server 2010 с помощью клиента Lync 2013, все новые возможности, не поддерживаемые Lync Server 2010, будут недоступны до тех пор, пока пользователь не будет перенесен на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-188">If a user is signed in to Lync Server 2010 with a Lync 2013 client, any new features not supported by Lync Server 2010 will be unavailable until the user is moved to Lync Server 2013.</span></span>

<span data-ttu-id="8dcc6-189">В следующей таблице сравниваются возможности, доступные в одноранговых сеансах, в которых клиент вошел на сервер Lync Server 2013 или Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-189">The following table compares feature availability in peer-to-peer sessions where the client is signed in to either Lync Server 2013 or Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8dcc6-190">Участники Lync Web App и Lync 2010 относятся к клиентам только для собраний и не включены в эту таблицу.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-190">Lync Web App and Lync 2010 Attendee are meeting-only clients and aren’t included in this table.</span></span>



</div>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8dcc6-191">Клиент</span><span class="sxs-lookup"><span data-stu-id="8dcc6-191">Client</span></span></th>
<th><span data-ttu-id="8dcc6-192">Обмен мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="8dcc6-192">Instant Messaging</span></span></th>
<th><span data-ttu-id="8dcc6-193">Присутствие</span><span class="sxs-lookup"><span data-stu-id="8dcc6-193">Presence</span></span></th>
<th><span data-ttu-id="8dcc6-194">Голос</span><span class="sxs-lookup"><span data-stu-id="8dcc6-194">Voice</span></span></th>
<th><span data-ttu-id="8dcc6-195">Видео</span><span class="sxs-lookup"><span data-stu-id="8dcc6-195">Video</span></span></th>
<th><span data-ttu-id="8dcc6-196">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="8dcc6-196">Application Sharing</span></span></th>
<th><span data-ttu-id="8dcc6-197">Передача файлов</span><span class="sxs-lookup"><span data-stu-id="8dcc6-197">File Transfer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-198">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-198">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-199">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-199">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-200">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-201">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-201">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-202">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-202">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-203">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-203">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-204">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-205">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="8dcc6-205">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-206">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-207">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-207">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-208">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-209">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-210">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-211">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-211">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-212">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-212">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-213">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-213">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-214">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-215">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-216">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-217">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-218">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-219">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="8dcc6-219">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-220">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-220">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-221">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-222">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-222">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-223">Lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="8dcc6-223">Lync 2010 Mobile</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-224">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-225">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-225">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-226">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="8dcc6-226">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-227">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-228">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-229">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-229">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-230">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="8dcc6-230">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-231">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-232">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-232">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-233">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-233">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-234">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-235">Да1</span><span class="sxs-lookup"><span data-stu-id="8dcc6-235">Yes1</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-236">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-236">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-237">Общедоступная служба обмена мгновенными сообщениями (AOL, Yahoo!)</span><span class="sxs-lookup"><span data-stu-id="8dcc6-237">Public IM (AOL, Yahoo!)</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-238">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-239">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-239">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-240">Общедоступная служба обмена мгновенными сообщениями (MSN, Windows Live Messenger)</span><span class="sxs-lookup"><span data-stu-id="8dcc6-240">Public IM (MSN, Windows Live Messenger)</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-241">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-241">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-242">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-243">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-243">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-244">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-244">Yes</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="8dcc6-245">За Сентябрь 1 сентября 2012 г. Лицензия на подписку на общедоступные пользователи Microsoft Lync (PIC USL) больше не доступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-245">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="8dcc6-246">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="8dcc6-246">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="8dcc6-247">Messenger, пока не зайдет Дата завершения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-247">Messenger until the service shutdown date.</span></span> <span data-ttu-id="8dcc6-248">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-248">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="8dcc6-249">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-249">has been announced.</span></span> <span data-ttu-id="8dcc6-250">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>..</span><span class="sxs-lookup"><span data-stu-id="8dcc6-250">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>..</span></span></P>
> <LI>
> <P><span data-ttu-id="8dcc6-251">USL PIC является лицензией на подписку "на пользователя", которая требуется для использования Lync Server или Office Communications Server для Федерации с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="8dcc6-251">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="8dcc6-252">Messenger.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-252">Messenger.</span></span> <span data-ttu-id="8dcc6-253">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого она не будет продлена.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-253">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="8dcc6-254">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-254">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="8dcc6-255">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-255">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="8dcc6-256">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут получать сотни миллионов людей с помощью голосовой почты и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-256">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="8dcc6-257">1 в Office Communicator 2007 R2 доступен только общий доступ к рабочему столу (и не общий доступ к программам).</span><span class="sxs-lookup"><span data-stu-id="8dcc6-257">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8dcc6-258">Общий доступ к рабочему столу между Office Communicator 2007 R2 и Skype для бизнеса 2015 нельзя инициировать из нового клиента, если пользовательским интерфейсом клиента Skype для бизнеса 2015 является принудительно.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-258">Desktop sharing between Office Communicator 2007 R2 and Skype for Business 2015 cannot be initiated from the newer client when the Skype for Business 2015 client user interface is enforced.</span></span>



</div>

</div>

<div>

## <a name="conferencing-feature-support-for-lync-2013-clients-in-lync-server-2010-meetings"></a><span data-ttu-id="8dcc6-259">Поддержка функций конференций для клиентов Lync 2013 в Lync Server 2010 для собраний</span><span class="sxs-lookup"><span data-stu-id="8dcc6-259">Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings</span></span>

<span data-ttu-id="8dcc6-260">Когда пользователь присоединяется к собранию Lync Server 2010 с помощью клиента Lync 2013, у него есть доступ к функциям клиента Lync 2013 со следующими исключениями:</span><span class="sxs-lookup"><span data-stu-id="8dcc6-260">When users join Lync Server 2010 meetings with a Lync 2013 client, they have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="8dcc6-261">В параметрах управления **участниками** , доступ к которым осуществляется с помощью значка "люди" в окне собрания, не будет работать параметр " **мгновенное сообщение о собрании** ".</span><span class="sxs-lookup"><span data-stu-id="8dcc6-261">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="8dcc6-262">Представление коллекции не может работать в видеоконференциях.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-262">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="8dcc6-263">Пользователь видит только активный динамик, а не все динамики.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-263">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="8dcc6-264">В списке выбора параметров **разметки** недоступен **режим коллекции**</span><span class="sxs-lookup"><span data-stu-id="8dcc6-264">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="8dcc6-265">Список участников по умолчанию отображается в видеоконференциях.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-265">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="8dcc6-266">Если щелкнуть пользователя правой кнопкой мыши в списке участников, вы не **сможете получить** **доступ к** параметрам управления участниками коллекции.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-266">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

<div>

## <a name="conferencing-feature-support-in-lync-server-2013-meetings"></a><span data-ttu-id="8dcc6-267">Поддержка функций конференций в Lync Server 2013 для собраний</span><span class="sxs-lookup"><span data-stu-id="8dcc6-267">Conferencing Feature Support in Lync Server 2013 Meetings</span></span>

<span data-ttu-id="8dcc6-268">Lync Server 2013 предлагает новые функции для конференций, которые становятся доступны пользователям после перемещения учетных записей на Lync Server 2013 и входа в систему с помощью клиента Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-268">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="8dcc6-269">В качестве примеров можно привести представление коллекции видео, видео в формате HD, общий доступ к PowerPoint, а также возможность отключить звук и видео всех участников во время ввода собрания.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-269">Examples include video gallery view, HD video, PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="8dcc6-270">Новые функции, описанные в разделе [новые возможности конференции в Lync server 2013](lync-server-2013-new-conferencing-features.md) , и [новые возможности для клиентов в Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc6-270">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="8dcc6-271">В Lync Server 2013 для собраний некоторые возможности конференции поддерживаются для пользователей, использующих разные версии сервера, и которые используют разные клиенты и клиентские версии.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-271">In Lync Server 2013 meetings, certain conferencing features are supported for users who are homed on different versions of the server and who are using different clients and client versions.</span></span> <span data-ttu-id="8dcc6-272">Когда клиенты присоединяются к собранию Lync Server 2013, пользователи имеют доступ к функциям и возможностям, представленным в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-272">When clients join a Lync Server 2013 meeting, users have access to the features and capabilities shown in this table.</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8dcc6-273">Клиент</span><span class="sxs-lookup"><span data-stu-id="8dcc6-273">Client</span></span></th>
<th><span data-ttu-id="8dcc6-274">Обмен мгновенными сообщениями в одноранговой сети</span><span class="sxs-lookup"><span data-stu-id="8dcc6-274">Peer-to-peer IM</span></span></th>
<th><span data-ttu-id="8dcc6-275">Голос</span><span class="sxs-lookup"><span data-stu-id="8dcc6-275">Voice</span></span></th>
<th><span data-ttu-id="8dcc6-276">Видео</span><span class="sxs-lookup"><span data-stu-id="8dcc6-276">Video</span></span></th>
<th><span data-ttu-id="8dcc6-277">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="8dcc6-277">Application Sharing</span></span></th>
<th><span data-ttu-id="8dcc6-278">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8dcc6-278">PowerPoint</span></span></th>
<th><span data-ttu-id="8dcc6-279">Передача файлов</span><span class="sxs-lookup"><span data-stu-id="8dcc6-279">File Transfer</span></span></th>
<th><span data-ttu-id="8dcc6-280">Доска</span><span class="sxs-lookup"><span data-stu-id="8dcc6-280">Whiteboard</span></span></th>
<th><span data-ttu-id="8dcc6-281">Опрос</span><span class="sxs-lookup"><span data-stu-id="8dcc6-281">Polling</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-282">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-282">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-283">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-283">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-284">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-285">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-285">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-286">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-286">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-287">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-287">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-288">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-289">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-289">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-290">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-290">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-291">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="8dcc6-291">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-292">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-293">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-293">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-294">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-294">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-295">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-295">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-296">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-297">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-297">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-298">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-298">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-299">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-299">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-300">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="8dcc6-300">Lync Web App</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-301">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-301">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-302">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-302">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-303">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-303">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-304">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-305">Да2</span><span class="sxs-lookup"><span data-stu-id="8dcc6-305">Yes2</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-306">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-306">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-307">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-307">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-308">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-308">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-309">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-309">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-310">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-311">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-311">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-312">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-312">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-313">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-314">Да3</span><span class="sxs-lookup"><span data-stu-id="8dcc6-314">Yes3</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-315">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-315">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-316">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-316">Yes</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-317">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-317">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-318">Office Communicator 2007 R2 4</span><span class="sxs-lookup"><span data-stu-id="8dcc6-318">Office Communicator 2007 R2 4</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-319">Да</span><span class="sxs-lookup"><span data-stu-id="8dcc6-319">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8dcc6-320">1 в Office Communicator 2007 R2 доступен только общий доступ к рабочему столу (и не общий доступ к программам).</span><span class="sxs-lookup"><span data-stu-id="8dcc6-320">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<span data-ttu-id="8dcc6-321">2 Lync Server 2013 использует обновленный механизм для отправки файлов PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-321">2 Lync Server 2013 uses an updated mechanism for uploading PowerPoint files.</span></span> <span data-ttu-id="8dcc6-322">Пользователи Lync Web App, присоединяющиеся к собранию, изначально запланированному на Lync Server 2010, могут просматривать презентации PowerPoint и перемещаться по ним, но не могут загружать файлы PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-322">Lync Web App users who join a meeting that was originally scheduled on Lync Server 2010 can view and navigate PowerPoint presentations, but cannot upload PowerPoint files.</span></span>

<span data-ttu-id="8dcc6-323">3. Если собрание запланировано на Lync Server 2013, а слайды PowerPoint были отправлены клиентом Lync 2013, пользователи Lync 2010 смогут получить доступ к слайдам только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-323">3 If the meeting was scheduled on Lync Server 2013 and PowerPoint slides were uploaded by a Lync 2013 client, Lync 2010 users have view-only access to the slides.</span></span> <span data-ttu-id="8dcc6-324">И наоборот, если слайды PowerPoint были отправлены пользователем Lync 2010, пользователи Lync Server 2013 смогут просматривать и делать слайды и, если настроены сервер Office Web Apps, получать доступ к новым возможностям, таким как отображение более высоком разрешающей способности, анимацию, переходы слайдов и внедренное видео.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-324">Conversely, if the PowerPoint slides were uploaded by a Lync 2010 user, Lync Server 2013 users will be able to view and slides and, if Office Web Apps Server is configured, access new capabilities such as higher resolution display, animations, slide transitions, and embedded video.</span></span> <span data-ttu-id="8dcc6-325">Дополнительные сведения можно найти [в разделе Настройка интеграции с Office Web Apps Server и Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc6-325">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="8dcc6-326">4The функции присутствия и обмена мгновенными сообщениями в Office Communicator 2007 R2 совместимы с Lync Server 2013, но возможности конференции не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-326">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="8dcc6-327">При переходе с Office Communications Server 2007 R2 подходящими для обеспечения взаимодействия и обмена мгновенными сообщениями является Office Communicator 2007 R2, но пользователи должны использовать Lync Web App 2013, чтобы присоединиться к собраниям Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-327">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

</div>

</div>

<div>

## <a name="scheduling-add-in-support"></a><span data-ttu-id="8dcc6-328">Поддержка планирования надстроек</span><span class="sxs-lookup"><span data-stu-id="8dcc6-328">Scheduling Add-in Support</span></span>

<span data-ttu-id="8dcc6-329">Поддержка различных надстроек для планирования в соответствии с серверной и клиентской версиями обеспечивается совместимостью.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-329">Server support for the various scheduling add-ins is consistent with server and client version compatibility.</span></span> <span data-ttu-id="8dcc6-330">Как правило, в Lync Server 2013 поддерживаются следующие надстройки для планирования.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-330">In general, the following scheduling add-ins are supported on Lync Server 2013.</span></span> <span data-ttu-id="8dcc6-331">Несмотря на то, что предыдущие версии надстроек не предоставляют новые функции надстройки Lync 2013, такие как возможность отключить Микрофоны всех участников и звуков видео при вводе собрания.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-331">However, previous versions of add-ins do not provide new Lync 2013 add-in features, such as the option to mute all attendee audio and video upon meeting entry.</span></span>

  - <span data-ttu-id="8dcc6-332">**Надстройка "собрание по сети" для Lync 2013**   Предоставляет те же функции, что и надстройка "собрание по сети" для Lync 2010, с помощью которых можно добавить элементы управления, позволяющие организаторов на собраниях планировать звук и видео по умолчанию для участников.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-332">**Online Meeting Add-in for Lync 2013**   Provides the same features as the Online Meeting Add-in for Lync 2010, with the addition of attendee mute controls, which allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span> <span data-ttu-id="8dcc6-333">Администраторы также могут настроить приглашения на собрание Организации, добавив собственный логотип, URL-адрес службы поддержки, URL-адрес юридического лица или настраиваемый текст нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-333">Administrators can also customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span>

  - <span data-ttu-id="8dcc6-334">**Надстройка "собрание по сети" для Lync 2010**   Планирование собраний Lync и удаление возможности планирования конференций Office Live для собраний.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-334">**Online Meeting Add-in for Lync 2010**   Provides scheduling for Lync meetings and removes the capability to schedule Office Live Meeting conferences.</span></span>

  - <span data-ttu-id="8dcc6-335">**Надстройка для конференц-связи Office Communicator 2007 R2**   Обеспечивает планирование для конференций Office Live для собраний и конференций Office Communicator 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-335">**Office Communicator 2007 R2 Conferencing Add-in**   Provides scheduling for both Office Live Meeting conferences and Office Communicator 2007 R2 conferences.</span></span> 

<div>


> [!NOTE]  
> <span data-ttu-id="8dcc6-336">Конференции Live Meeting невозможно запланировать на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-336">Live Meeting conferences cannot be scheduled on Lync Server 2013.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8dcc6-337">Планирование клиента</span><span class="sxs-lookup"><span data-stu-id="8dcc6-337">Scheduling Client</span></span></th>
<th><span data-ttu-id="8dcc6-338">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-338">Lync Server 2013</span></span></th>
<th><span data-ttu-id="8dcc6-339">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-339">Lync Server 2010</span></span></th>
<th><span data-ttu-id="8dcc6-340">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="8dcc6-340">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-341">Надстройка "собрание по сети" для Lync 2013 (может использоваться с Office 2013, Outlook 2010 и Outlook 2007)</span><span class="sxs-lookup"><span data-stu-id="8dcc6-341">Online Meeting Add-in for Lync 2013 (can be used with Office 2013, Outlook 2010, and Outlook 2007)</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-342">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-342">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-343">Поддерживается (недоступна новая функция надстроек)</span><span class="sxs-lookup"><span data-stu-id="8dcc6-343">Supported (new add-in features not available)</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-344">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-344">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-345">Веб-планировщик Lync 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-345">Lync 2013 Web Scheduler</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-346">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-346">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-347">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-347">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-348">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-348">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dcc6-349">собраний по сети для Lync 2010</span><span class="sxs-lookup"><span data-stu-id="8dcc6-349">Online Meeting Add-in for Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-350">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-350">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-351">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-351">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-352">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-352">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dcc6-353">Надстройка для конференц-связи Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="8dcc6-353">Office Communicator 2007 R2 Conferencing Add-in</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-354">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-354">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-355">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-355">Supported</span></span></p></td>
<td><p><span data-ttu-id="8dcc6-356">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dcc6-356">Supported</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="support-for-joining-meetings"></a><span data-ttu-id="8dcc6-357">Поддержка присоединения к собраниям</span><span class="sxs-lookup"><span data-stu-id="8dcc6-357">Support for Joining Meetings</span></span>

<span data-ttu-id="8dcc6-358">Все клиенты, поддерживаемые Lync Server 2013, могут присоединиться к собраниям Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-358">All of the clients that Lync Server 2013 supports are allowed to join Lync 2013 meetings.</span></span> <span data-ttu-id="8dcc6-359">Поскольку Lync Web App — это веб-компонент сервера, то в тех случаях, когда Lync Web App используется для присоединения к собранию Lync Server 2013, всегда используется новая версия Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-359">Because Lync Web App is a web component of the server, in cases where Lync Web App is used to join a Lync Server 2013 meeting, the newer version of Lync Web App is always used.</span></span>

<span data-ttu-id="8dcc6-360">Пользователи Lync 2013 могут присоединяться к собраниям, размещенным на Lync 2010 и Office Communications Server 2007 R2, с масштабированием функций.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-360">Lync 2013 clients can join meetings hosted on Lync 2010 and Office Communications Server 2007 R2 with scaled-down functionality.</span></span> <span data-ttu-id="8dcc6-361">Возможности, доступные в собрании, ограничиваются версией сервера, на котором размещается собрание.</span><span class="sxs-lookup"><span data-stu-id="8dcc6-361">In-meeting features are limited by the version of the server on which the meeting is hosted.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8dcc6-362">См. также</span><span class="sxs-lookup"><span data-stu-id="8dcc6-362">See Also</span></span>


[<span data-ttu-id="8dcc6-363">Требования к приложению Lync из Магазина Windows для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-363">Lync Windows Store app requirements for Lync Server 2013</span></span>](lync-server-2013-lync-windows-store-app-requirements.md)  
[<span data-ttu-id="8dcc6-364">Новые возможности конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-364">New conferencing features in Lync Server 2013</span></span>](lync-server-2013-new-conferencing-features.md)  
[<span data-ttu-id="8dcc6-365">Новые возможности для клиентов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8dcc6-365">What's new for clients in Lync Server 2013</span></span>](lync-server-2013-what-s-new-for-clients.md)  
  

<span data-ttu-id="8dcc6-366"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8dcc6-366"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

