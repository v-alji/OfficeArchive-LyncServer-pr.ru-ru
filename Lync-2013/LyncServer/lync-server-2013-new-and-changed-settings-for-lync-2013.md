---
title: 'Lync Server 2013: новые и измененные параметры Lync 2013'
description: 'Lync Server 2013: новые и измененные параметры Lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New and changed settings for Lync 2013
ms:assetid: bb13789c-7eda-461c-a387-02ea8ca4dabe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205204(v=OCS.15)
ms:contentKeyID: 48185241
ms.date: 12/08/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bf744e1bae774904733390ec624be523ad32bc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445486"
---
# <a name="new-and-changed-settings-for-lync-2013"></a><span data-ttu-id="25bd4-103">Новые и измененные параметры для Lync 2013</span><span class="sxs-lookup"><span data-stu-id="25bd4-103">New and changed settings for Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25bd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25bd4-104">

<span> </span></span></span>

<span data-ttu-id="25bd4-105">_**Тема последнего изменения:** 2014-12-05_</span><span class="sxs-lookup"><span data-stu-id="25bd4-105">_**Topic Last Modified:** 2014-12-05_</span></span>

<span data-ttu-id="25bd4-106">В этом разделе рассматриваются изменения командлетов командной консоли Lync Server, которые непосредственно связаны с управлением клиентом.</span><span class="sxs-lookup"><span data-stu-id="25bd4-106">This topic discusses changes to Lync Server Management Shell cmdlets that relate directly to client management.</span></span> <span data-ttu-id="25bd4-107">Lync Server 2013 предлагает несколько новых параметров и устаревшие параметры для функций, которые можно настроить с помощью других средств.</span><span class="sxs-lookup"><span data-stu-id="25bd4-107">Lync Server 2013 introduces several new parameters, and deprecates parameters for features that can be configured through other means.</span></span>

<div>

## <a name="new-client-management-parameters"></a><span data-ttu-id="25bd4-108">Новые параметры управления клиентом</span><span class="sxs-lookup"><span data-stu-id="25bd4-108">New Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="25bd4-109">Новые функции</span><span class="sxs-lookup"><span data-stu-id="25bd4-109">New</span></span></th>
<th><span data-ttu-id="25bd4-110">Командлет командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="25bd4-110">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="25bd4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="25bd4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-112">TracingLevel</span><span class="sxs-lookup"><span data-stu-id="25bd4-112">TracingLevel</span></span></p></td>
<td><p><span data-ttu-id="25bd4-113">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-113">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-114">Если установлено значение true, трассировка программного обеспечения будет включена в Lync; Если задано значение false, трассировка программного обеспечения будет отключена.</span><span class="sxs-lookup"><span data-stu-id="25bd4-114">When set to True, software tracing will be enabled in Lync; when set to False, software tracing will be disabled.</span></span> <span data-ttu-id="25bd4-115">Отслеживание программного обеспечения включает в себя хранение подробной информации о всех функциях программы (в том числе о вызовах API отслеживания).</span><span class="sxs-lookup"><span data-stu-id="25bd4-115">Software tracing involves keeping a detailed record of everything that a program does (including tracking API calls).</span></span> <span data-ttu-id="25bd4-116">Трассировка особенно полезна разработчикам и сотрудникам службы поддержки приложений. Этот параметр аналогичен параметру групповой политики Communications Server 2007 R2 &quot; включить трассировку для Communicator. &quot; Ниже указаны параметры.</span><span class="sxs-lookup"><span data-stu-id="25bd4-116">Tracing is mostly useful to developers and to application support personnel.This setting is equivalent to the Communications Server 2007 R2 Group Policy setting &quot;Turn on tracing for Communicator.&quot; The settings are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="25bd4-117">Off = трассировка отключена, и пользователь не может изменить этот параметр.</span><span class="sxs-lookup"><span data-stu-id="25bd4-117">Off = Tracing is disabled and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="25bd4-118">Light = выполняется минимальная трассировка, и пользователь не может изменить этот параметр.</span><span class="sxs-lookup"><span data-stu-id="25bd4-118">Light = Minimal tracing is performed, and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="25bd4-119">On = подробный трассировка выполняется, и пользователь не может изменить этот параметр.</span><span class="sxs-lookup"><span data-stu-id="25bd4-119">On = Verbose tracing is performed, and the user cannot change this setting.</span></span></p></li>
</ul>
<p><span data-ttu-id="25bd4-120">По умолчанию для TracingLevel задано значение null.</span><span class="sxs-lookup"><span data-stu-id="25bd4-120">By default TracingLevel is set to a null value.</span></span> <span data-ttu-id="25bd4-121">Это означает, что выполняется минимальная трассировка, но пользователь может включить или отключить эту минимальную трассировку.</span><span class="sxs-lookup"><span data-stu-id="25bd4-121">That means that minimal tracing is performed, but the user can enable or disable this minimal tracing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-122">EnableMediaRedirection</span><span class="sxs-lookup"><span data-stu-id="25bd4-122">EnableMediaRedirection</span></span></p></td>
<td><p><span data-ttu-id="25bd4-123">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-123">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-124">Если для этого параметра установлено значение true ($True), звуковые и видеопотоки можно отделить от другого сетевого трафика, в свою очередь это позволяет клиентским устройствам кодировать и декодировать аудио-и видеофайлы локально.</span><span class="sxs-lookup"><span data-stu-id="25bd4-124">When set to True ($True) allows audio and video streams to be separated from other network traffic, In turn, this allows client devices to do encoding and decoding of audio and video locally.</span></span> <span data-ttu-id="25bd4-125">Перенаправление мультимедиа обычно приводит к снижению использования пропускной способности, повышенной масштабируемости сервера и более удобному взаимодействию с пользователем по сравнению с похожими методиками, такими как удаленное взаимодействие устройств или кодек кодирования кодека.</span><span class="sxs-lookup"><span data-stu-id="25bd4-125">Media redirection typically results in lower bandwidth usage, higher server scalability, and a more-optimal user experience compared to similar techniques such as device remoting or codec compression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-126">AllowLargeMeetings</span><span class="sxs-lookup"><span data-stu-id="25bd4-126">AllowLargeMeetings</span></span></p></td>
<td><p><span data-ttu-id="25bd4-127">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="25bd4-127">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="25bd4-128">Если установлено значение true, все собрания Lync обрабатываются как &quot; большие собрания. &quot; С большим собранием ограничения размещаются на количестве уведомлений, которые отправляются участникам, в дополнение к размеру списка собраний, который передается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25bd4-128">When set to True, all Lync Meetings are treated as &quot;large meetings.&quot; With a large meeting, restrictions are placed on the number of notifications that are sent to participants, in addition to the size of the meeting roster that is transmitted by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-129">DisablePowerPointAnnotations</span><span class="sxs-lookup"><span data-stu-id="25bd4-129">DisablePowerPointAnnotations</span></span></p></td>
<td><p><span data-ttu-id="25bd4-130">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="25bd4-130">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="25bd4-131">Если установлено значение true ($True), пользователи не смогут добавлять примечания к слайдам PowerPoint, используемым на Конференции.</span><span class="sxs-lookup"><span data-stu-id="25bd4-131">When set to True ($True) users won’t be able to add annotations to PowerPoint slides used in a conference.</span></span> <span data-ttu-id="25bd4-132">Тем не менее (в зависимости от значения свойства AllowAnnotations) пользователи по-прежнему имеют доступ к другим функциям доски.</span><span class="sxs-lookup"><span data-stu-id="25bd4-132">However (depending on the value of the AllowAnnotations property), users will still have access to other whiteboarding features.</span></span> <span data-ttu-id="25bd4-133">По умолчанию используется значение false, означающее, что заметки PowerPoint разрешены.</span><span class="sxs-lookup"><span data-stu-id="25bd4-133">The default value is False, meaning that PowerPoint annotations are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-134">AllowSharedNotes</span><span class="sxs-lookup"><span data-stu-id="25bd4-134">AllowSharedNotes</span></span></p></td>
<td><p><span data-ttu-id="25bd4-135">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="25bd4-135">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="25bd4-136">Если задано значение true (по умолчанию), все открытые записные книжки OneNote, связанные с конференции, автоматически обновляются данными, например участниками Конференции, и сведения о содержимом, доступном во время конференции.</span><span class="sxs-lookup"><span data-stu-id="25bd4-136">When set to True (the default value) any open OneNote notebooks linked to the conference will automatically be updated with information such as conference participants and details about content shared during the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-137">EnableInviteCustomization</span><span class="sxs-lookup"><span data-stu-id="25bd4-137">EnableInviteCustomization</span></span></p></td>
<td><p><span data-ttu-id="25bd4-138">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="25bd4-138">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="25bd4-139">Используется вместе с другими новыми параметрами CsMeetingConfiguration для настройки приглашений на собрания, созданных с помощью надстройки "собрание по сети" для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-139">Used along with the other new CsMeetingConfiguration parameters to customize the meeting invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-140">LogoURL</span><span class="sxs-lookup"><span data-stu-id="25bd4-140">LogoURL</span></span></p></td>
<td><p><span data-ttu-id="25bd4-141">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="25bd4-141">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="25bd4-142">Добавляет логотип организации ко всем приглашениям, созданным с помощью надстройки "собрание по сети" для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-142">Adds your organization’s logo to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="25bd4-143">Вы задаете URL-адрес изображения в формате GIF или JPG.</span><span class="sxs-lookup"><span data-stu-id="25bd4-143">You specify the URL of a GIF or JPG image.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-144">HelpURL</span><span class="sxs-lookup"><span data-stu-id="25bd4-144">HelpURL</span></span></p></td>
<td><p><span data-ttu-id="25bd4-145">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="25bd4-145">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="25bd4-146">Добавляет URL-адрес справки или поддержки вашей организации во все приглашения, созданные надстройкой "собрание по сети" для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-146">Adds your organization’s help or support URL to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-147">LegalURL</span><span class="sxs-lookup"><span data-stu-id="25bd4-147">LegalURL</span></span></p></td>
<td><p><span data-ttu-id="25bd4-148">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="25bd4-148">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="25bd4-149">Добавление юридического текста или текста отказа во все приглашения, созданные с помощью надстройки "собрание по сети" для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-149">Adds legal text or disclaimer text to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="25bd4-150">Вы задаете URL-адрес расположения текста.</span><span class="sxs-lookup"><span data-stu-id="25bd4-150">You specify the URL for the location of the text.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-151">CustomFooterText</span><span class="sxs-lookup"><span data-stu-id="25bd4-151">CustomFooterText</span></span></p></td>
<td><p><span data-ttu-id="25bd4-152">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="25bd4-152">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="25bd4-153">Добавление настраиваемого нижнего колонтитула ко всем приглашениям, созданным с помощью надстройки "собрание по сети" для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-153">Adds a custom footer to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="25bd4-154">Вы задаете URL-адрес для расположения настраиваемого текста нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="25bd4-154">You specify the URL for the location of the custom footer text.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="deprecated-client-management-parameters"></a><span data-ttu-id="25bd4-155">Устаревшие параметры управления клиентом</span><span class="sxs-lookup"><span data-stu-id="25bd4-155">Deprecated Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="25bd4-156">Параметр</span><span class="sxs-lookup"><span data-stu-id="25bd4-156">Parameter</span></span></th>
<th><span data-ttu-id="25bd4-157">Командлет командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="25bd4-157">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="25bd4-158">Описание</span><span class="sxs-lookup"><span data-stu-id="25bd4-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-159">CustomizedHelpUrl</span><span class="sxs-lookup"><span data-stu-id="25bd4-159">CustomizedHelpUrl</span></span></p></td>
<td><p><span data-ttu-id="25bd4-160">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-160">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-161">Этот параметр не рекомендуется использовать с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-161">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="25bd4-162">При использовании в сочетании с EnableEnterpriseCustomizedHelp этот параметр позволил Организации указать URL-адрес, чтобы при нажатии пользователем пункта меню Справка в Lync отображалась настроенная Справка.</span><span class="sxs-lookup"><span data-stu-id="25bd4-162">When used in conjunction with EnableEnterpriseCustomizedHelp, this parameter enabled an organization to specify a URL so that when users clicked the Help menu in Lync, customized help would display.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-163">EnableEnterpriseCustomizedHelp</span><span class="sxs-lookup"><span data-stu-id="25bd4-163">EnableEnterpriseCustomizedHelp</span></span></p></td>
<td><p><span data-ttu-id="25bd4-164">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-164">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-165">Этот параметр не рекомендуется использовать с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-165">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="25bd4-166">При использовании в сочетании с CustomizedHelpUrl этот параметр позволяет организациям отображать настроенную справку.</span><span class="sxs-lookup"><span data-stu-id="25bd4-166">When used in conjunction with CustomizedHelpUrl, this parameter enabled organizations to display customized help.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-167">EnableSQMData</span><span class="sxs-lookup"><span data-stu-id="25bd4-167">EnableSQMData</span></span></p></td>
<td><p><span data-ttu-id="25bd4-168">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-168">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-169">Параметр EnableSQMData командлета Set-CSClientPolicy удален в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-169">The EnableSQMData parameter of the Set-CSClientPolicy cmdlet has been removed in Lync Server 2013.</span></span> <span data-ttu-id="25bd4-170">Вместо этого вы можете использовать параметр общей групповой политики для данных управления качеством программ (SQM), чтобы определить пользовательский интерфейс для параметра улучшения качества по на странице Общие параметры клиента Lync.</span><span class="sxs-lookup"><span data-stu-id="25bd4-170">Instead, you can use the shared Group Policy setting for Software Quality Management (SQM) data to determine the user interface for the Customer Experience Improvement option in the Lync client General options page:</span></span></p>
<p><span data-ttu-id="25bd4-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span><span class="sxs-lookup"><span data-stu-id="25bd4-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span></span></p>
<p><span data-ttu-id="25bd4-172">Данные</span><span class="sxs-lookup"><span data-stu-id="25bd4-172">Values:</span></span></p>
<p><span data-ttu-id="25bd4-173">1 = Отображение и установка флажка (пользователь может снять флажок)</span><span class="sxs-lookup"><span data-stu-id="25bd4-173">1 = Display and select the check box (the user can clear the check box)</span></span></p>
<p><span data-ttu-id="25bd4-174">0 = отключить и отключить флажок (пользователь не может переопределить)</span><span class="sxs-lookup"><span data-stu-id="25bd4-174">0 = Turn off and disable the check box (user can't override)</span></span></p>
<p><span data-ttu-id="25bd4-175">NULL = значение определяется программой установки Office, и этот флажок отображается, чтобы пользователи могли задать его по мере выбора.</span><span class="sxs-lookup"><span data-stu-id="25bd4-175">Null = The value is determined by Office setup, and the check box is displayed for users to set as they choose</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-176">AllowExchangeContactStore</span><span class="sxs-lookup"><span data-stu-id="25bd4-176">AllowExchangeContactStore</span></span></p></td>
<td><p><span data-ttu-id="25bd4-177">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-177">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-178">Этот параметр удален.</span><span class="sxs-lookup"><span data-stu-id="25bd4-178">This parameter has been removed.</span></span> <span data-ttu-id="25bd4-179">Вместо этого при развертывании сервера Lync Server 2013 и публикации топологии единое хранилище контактов включается для всех пользователей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25bd4-179">Instead, when you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="25bd4-180">Это означает, что все контакты пользователя хранятся в Exchange и доступны в Lync, Outlook и Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="25bd4-180">This means that all a user’s contacts are kept in Exchange and are available in Lync, Outlook, and Outlook Web Access.</span></span> <span data-ttu-id="25bd4-181">Вы можете использовать командлет Set-CsUserServicesPolicy, чтобы настроить, какие пользователи будут доступны в едином хранилище контактов.</span><span class="sxs-lookup"><span data-stu-id="25bd4-181">You can use the Set-CsUserServicesPolicy cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="25bd4-182">Вы можете включить пользователей глобально, по сайту, по клиенту или по отдельным пользователям или группам пользователей.</span><span class="sxs-lookup"><span data-stu-id="25bd4-182">You can enable users globally, by site, by tenant, or by individuals or groups of individuals.</span></span> <span data-ttu-id="25bd4-183">Дополнительные сведения можно найти <a href="lync-server-2013-enable-users-for-unified-contact-store.md">в разделе Включение пользователей единого магазина контактов в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="25bd4-183">For details, see <a href="lync-server-2013-enable-users-for-unified-contact-store.md">Enable users for unified contact store in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25bd4-184">MAPIPollInterval</span><span class="sxs-lookup"><span data-stu-id="25bd4-184">MAPIPollInterval</span></span></p></td>
<td><p><span data-ttu-id="25bd4-185">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-185">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-186">Этот параметр не используется в Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-186">This parameter is not used by Lync 2013.</span></span> <span data-ttu-id="25bd4-187">В предыдущих выпусках этот параметр указывает, как часто клиент извлекает данные MAPI из общедоступных папок Exchange.</span><span class="sxs-lookup"><span data-stu-id="25bd4-187">In previous releases, this parameter specified how often the client retrieved MAPI data from Exchange public folders</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25bd4-188">DisableICE</span><span class="sxs-lookup"><span data-stu-id="25bd4-188">DisableICE</span></span></p></td>
<td><p><span data-ttu-id="25bd4-189">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="25bd4-189">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="25bd4-190">Этот параметр устарел в Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="25bd4-190">This parameter was deprecated in Lync 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="25bd4-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25bd4-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

