---
title: 'Lync Server 2013: процесс развертывания для группы ответа'
description: 'Lync Server 2013: процесс развертывания для группы ответа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Response Group
ms:assetid: d390c8a1-dc6e-44d8-b386-2be1fca9877c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205270(v=OCS.15)
ms:contentKeyID: 48185437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b50fb7903a2fcc301bbf435013b8f8df4e775a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429659"
---
# <a name="deployment-process-for-response-group-in-lync-server-2013"></a><span data-ttu-id="26004-103">Процесс развертывания группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26004-103">Deployment process for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26004-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26004-104">

<span> </span></span></span>

<span data-ttu-id="26004-105">_**Тема последнего изменения:** 2012-09-27_</span><span class="sxs-lookup"><span data-stu-id="26004-105">_**Topic Last Modified:** 2012-09-27_</span></span>

<span data-ttu-id="26004-106">В этом разделе приводятся общие этапы и инструкции по развертыванию приложения группы ответа.</span><span class="sxs-lookup"><span data-stu-id="26004-106">This section provides an overview of the phases and steps involved in deploying the Response Group application.</span></span>

### <a name="response-group-deployment-process"></a><span data-ttu-id="26004-107">Процедура развертывания группы ответа</span><span class="sxs-lookup"><span data-stu-id="26004-107">Response Group Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26004-108">Этап</span><span class="sxs-lookup"><span data-stu-id="26004-108">Phase</span></span></th>
<th><span data-ttu-id="26004-109">Шаги</span><span class="sxs-lookup"><span data-stu-id="26004-109">Steps</span></span></th>
<th><span data-ttu-id="26004-110">Разрешения</span><span class="sxs-lookup"><span data-stu-id="26004-110">Permissions</span></span></th>
<th><span data-ttu-id="26004-111">Документация по развертыванию</span><span class="sxs-lookup"><span data-stu-id="26004-111">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26004-112">Установка приложения группы ответа</span><span class="sxs-lookup"><span data-stu-id="26004-112">Install the Response Group application</span></span></p></td>
<td><p><span data-ttu-id="26004-113">Приложение группы ответа устанавливается и активируется по умолчанию при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="26004-113">The Response Group application is installed and activated by default when you deploy Enterprise Voice.</span></span></p></td>
<td><p><span data-ttu-id="26004-114">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="26004-114">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="26004-115"><a href="lync-server-2013-deploying-enterprise-voice.md">Развертывание корпоративной голосовой связи в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-115"><a href="lync-server-2013-deploying-enterprise-voice.md">Deploying Enterprise Voice in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26004-116">Установка компонентов для группы ответа</span><span class="sxs-lookup"><span data-stu-id="26004-116">Install components for Response Group</span></span></p></td>
<td><p><span data-ttu-id="26004-117">Командлеты Lync Server, панель управления Lync Server, средство настройки группы ответа, агент "вход и выход из консоли" и клиентская веб-служба "группа ответа" устанавливается как часть веб-служб.</span><span class="sxs-lookup"><span data-stu-id="26004-117">Lync Server cmdlets, the Lync Server Control Panel, Response Group Configuration Tool, agents' sign-in and sign-out console, and Response Group Client Web service are installed as part of Web Services.</span></span> <span data-ttu-id="26004-118">Веб-службы устанавливаются при развертывании пула Enterprise Edition или стандартного сервера выпусков.</span><span class="sxs-lookup"><span data-stu-id="26004-118">Web Services is installed when you deploy an Enterprise Edition pool or a Standard Edition server.</span></span></p></td>
<td><p><span data-ttu-id="26004-119">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="26004-119">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="26004-120"><a href="lync-server-2013-deploying-lync-server.md">Развертывание Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-120"><a href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26004-121">Включение пользователей для Lync 2013 и для корпоративного голосовой связи</span><span class="sxs-lookup"><span data-stu-id="26004-121">Enable users for Lync 2013 and for Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="26004-122">Включите пользователей, которые будут агентами для Lync Server и корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="26004-122">Enable users who will be agents for Lync Server and Enterprise Voice.</span></span> <span data-ttu-id="26004-123">Пользователей необходимо включить до того, как их можно будет добавлять в группы агентов.</span><span class="sxs-lookup"><span data-stu-id="26004-123">Users must be enabled before you can add them to agent groups.</span></span> <span data-ttu-id="26004-124">Как правило, пользователи работают с Lync Server во время развертывания Enterprise Edition или Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="26004-124">Typically, users are enabled for Lync Server during the Enterprise Edition or Standard Edition server deployment.</span></span> <span data-ttu-id="26004-125">Для пользователей, использующих корпоративную голосовую раскладку, включены пользователи.</span><span class="sxs-lookup"><span data-stu-id="26004-125">Users are enabled for Enterprise Voice during the Enterprise Voice deployment.</span></span></p></td>
<td><p><span data-ttu-id="26004-126">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="26004-126">RTCUniversalUserAdmins</span></span></p>
<p><span data-ttu-id="26004-127">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-127">CsUserAdministrator</span></span></p>
<p><span data-ttu-id="26004-128">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-128">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="26004-129"><a href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Отключение и повторное включение учетной записи пользователя для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-129"><a href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Disable or re-enable user account for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="26004-130"><a href="lync-server-2013-enable-users-for-enterprise-voice.md">Включение пользователей корпоративной голосовой связи в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-130"><a href="lync-server-2013-enable-users-for-enterprise-voice.md">Enable users for Enterprise Voice in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26004-131">Создание и настройка групп ответа, которые состоят из групп агентов, очередей и рабочих процессов</span><span class="sxs-lookup"><span data-stu-id="26004-131">Create and configure response groups, which consist of agent groups, queues, and workflows</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="26004-132">С помощью панели управления Lync Server или командной консоли Lync Server вы можете сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="26004-132">Use the Lync Server Control Panel or Lync Server Management Shell to do the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="26004-133">Создайте и настройте группы агентов.</span><span class="sxs-lookup"><span data-stu-id="26004-133">Create and configure agent groups.</span></span></p></li>
<li><p><span data-ttu-id="26004-134">Создайте и настройте очереди.</span><span class="sxs-lookup"><span data-stu-id="26004-134">Create and configure queues.</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="26004-135">Кроме того, можно использовать командную консоль Lync Server для создания стандартных рабочих часов и праздников для группы ответа.</span><span class="sxs-lookup"><span data-stu-id="26004-135">Optionally, use Lync Server Management Shell to create predefined response group business hours and holidays.</span></span></p></li>
<li><p><span data-ttu-id="26004-136">С помощью средства настройки группы ответа или командной консоли Lync Server вы можете создавать рабочие процессы (группы слежения или потоки звонков для голосовой связи), в том числе пользовательские группы ответов и рабочие часы и праздники.</span><span class="sxs-lookup"><span data-stu-id="26004-136">Use the Response Group Configuration Tool or Lync Server Management Shell to create workflows (hunt groups or interactive voice response (IVR) call flows), including custom response group business hours and holidays.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="26004-137">Вы можете получить доступ к средству настройки группы ответа с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="26004-137">You can access the Response Group Configuration Tool through Lync Server Control Panel.</span></span>


</div></li>
</ol></td>
<td><p><span data-ttu-id="26004-138">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="26004-138">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="26004-139">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-139">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="26004-140">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-140">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="26004-141">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-141">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="26004-142">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-142">CsAdministrator</span></span></p>
<p><span data-ttu-id="26004-143">CsResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="26004-143">CsResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="26004-144"><a href="lync-server-2013-create-response-group-agent-groups.md">Создание групп агента группы ответа Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-144"><a href="lync-server-2013-create-response-group-agent-groups.md">Create Response Group agent groups Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="26004-145"><a href="lync-server-2013-create-response-group-queues.md">Создание очередей группы ответа в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-145"><a href="lync-server-2013-create-response-group-queues.md">Create Response Group queues in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="26004-146"><a href="lync-server-2013-optional-define-response-group-business-hours.md">Необязательно Определение группы ответа в рабочее время в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-146"><a href="lync-server-2013-optional-define-response-group-business-hours.md">(Optional) Define Response Group business hours in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="26004-147"><a href="lync-server-2013-optional-define-response-group-holiday-sets.md">Необязательно Определение наборов праздников группы ответа в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-147"><a href="lync-server-2013-optional-define-response-group-holiday-sets.md">(Optional) Define Response Group holiday sets in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="26004-148"><a href="lync-server-2013-create-or-modify-a-workflow.md">Создание или изменение рабочего процесса в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-148"><a href="lync-server-2013-create-or-modify-a-workflow.md">Create or modify a workflow in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26004-149">(Необязательно) Задание настроек на уровне приложения</span><span class="sxs-lookup"><span data-stu-id="26004-149">(Optional) Customize application-level settings</span></span></p></td>
<td><p><span data-ttu-id="26004-150">Используйте командную консоль Lync Server для настройки стандартной конфигурации сохранения музыки, используемого по умолчанию звукового файла для сохранения музыки, периода отсрочки агента Ringback и контекстной конфигурации вызова.</span><span class="sxs-lookup"><span data-stu-id="26004-150">Use Lync Server Management Shell to customize the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span></p></td>
<td><p><span data-ttu-id="26004-151">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="26004-151">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="26004-152">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-152">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="26004-153">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-153">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="26004-154">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-154">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="26004-155">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-155">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="26004-156"><a href="lync-server-2013-managing-application-level-response-group-settings.md">Управление параметрами группы ответа уровня приложения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-156"><a href="lync-server-2013-managing-application-level-response-group-settings.md">Managing application-level Response Group settings in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26004-157">(Необязательно) Делегирование управления группами реагирования</span><span class="sxs-lookup"><span data-stu-id="26004-157">(Optional) Delegate management of response groups</span></span></p></td>
<td><p><span data-ttu-id="26004-158">Назначьте пользователям роль CsResponseGroupManager для делегирования конфигурации групп ответов.</span><span class="sxs-lookup"><span data-stu-id="26004-158">Assign users the CsResponseGroupManager role to delegate configuration of response groups.</span></span> <span data-ttu-id="26004-159">После этого диспетчер групп ответов может настроить назначенные им группы ответа.</span><span class="sxs-lookup"><span data-stu-id="26004-159">Response Group Managers can then configure the response groups assigned to them.</span></span></p></td>
<td><p><span data-ttu-id="26004-160">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="26004-160">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="26004-161">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-161">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="26004-162">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-162">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="26004-163">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-163">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="26004-164">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="26004-164">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="26004-165"><a href="lync-server-2013-planning-for-role-based-access-control.md">Планирование контроля доступа на основе ролей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="26004-165"><a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26004-166">Проверка развертывания группы ответа</span><span class="sxs-lookup"><span data-stu-id="26004-166">Verify your Response Group deployment</span></span></p></td>
<td><p><span data-ttu-id="26004-167">Протестируйте ответ на звонки в сервисную группу и рабочие процессы IVR, чтобы гарантировать правильную работу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="26004-167">Test answering calls to your hunt group and interactive voice response workflows to ensure that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr><span data-ttu-id="26004-168">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26004-168">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

