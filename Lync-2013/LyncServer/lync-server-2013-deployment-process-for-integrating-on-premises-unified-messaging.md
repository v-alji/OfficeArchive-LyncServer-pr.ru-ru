---
title: Процесс развертывания для интеграции локальной системы обработки сообщений
description: Процесс развертывания для интеграции локальной единой системы обмена сообщениями.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for integrating on-premises Unified Messaging and Lync Server
ms:assetid: 269a4436-f09f-415b-96ab-49a64370a385
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425737(v=OCS.15)
ms:contentKeyID: 48183664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6c1b8f528edb970893198ed06b821535a398f09d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399592"
---
# <a name="deployment-process-for-integrating-on-premises-unified-messaging-and-lync-server-2013"></a><span data-ttu-id="f2402-103">Процесс развертывания для интеграции локальной единой системы обмена сообщениями и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2402-103">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2402-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2402-104">

<span> </span></span></span>

<span data-ttu-id="f2402-105">_**Тема последнего изменения:** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="f2402-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="f2402-106">Если вы хотите интегрировать единую систему обмена сообщениями Exchange с Lync Server 2013, необходимо выполнить задачи, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="f2402-106">If you want to integrate Exchange Unified Messaging (UM) with Lync Server 2013, you must perform the tasks described in this topic.</span></span> <span data-ttu-id="f2402-107">Также убедитесь в том, что вы просматриваете рекомендации по планированию и развертыванию, описанные в [руководстве по интеграции локальной системы обработки сообщений и Lync Server 2013](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="f2402-107">Also be sure that you review the planning and deployment best practices described in [Guidelines for integrating on-premises Unified Messaging and Lync Server 2013](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md).</span></span> <span data-ttu-id="f2402-108">В этой статье предполагается, что вы развернули сервер Lync Server 2013 с размещенным сервером исправлений, и что вы включили пользователей для Lync Server 2013, но не обязательно выполнять все действия по развертыванию и настройке для включения корпоративной голосовой связи, как описано в разделе [Развертывание корпоративной голосовой связи в Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="f2402-108">This topic assumes that you have deployed Lync Server 2013 with a collocated Mediation Server and that you have enabled users for Lync Server 2013, but not necessarily that you have performed all deployment and configuration steps to enable Enterprise Voice, as described in [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span>

<div>

## <a name="unified-messaging-integration-process"></a><span data-ttu-id="f2402-109">Процесс интеграции единой системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="f2402-109">Unified Messaging Integration Process</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="f2402-110">Важно скоординировать администраторов Exchange вашей организации, чтобы подтвердить задачи, которые они будут выполнять для обеспечения успешной интеграции.</span><span class="sxs-lookup"><span data-stu-id="f2402-110">It is important that you coordinate with your organization’s Exchange administrators to confirm the tasks that each of you will perform to help ensure a smooth, successful integration.</span></span>



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
<th><span data-ttu-id="f2402-111">Этап</span><span class="sxs-lookup"><span data-stu-id="f2402-111">Phase</span></span></th>
<th><span data-ttu-id="f2402-112">Шаги</span><span class="sxs-lookup"><span data-stu-id="f2402-112">Steps</span></span></th>
<th><span data-ttu-id="f2402-113">Необходимые группы и роли</span><span class="sxs-lookup"><span data-stu-id="f2402-113">Required groups and roles</span></span></th>
<th><span data-ttu-id="f2402-114">Документация по развертыванию</span><span class="sxs-lookup"><span data-stu-id="f2402-114">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2402-115">Выполните развертывание одного из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="f2402-115">Deploy one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2402-116">Microsoft Exchange Server 2007 с пакетом обновления 1 (SP2) или последний пакет обновления</span><span class="sxs-lookup"><span data-stu-id="f2402-116">Microsoft Exchange Server 2007 Service Pack 1 (SP2) or latest service pack</span></span></p></li>
<li><p><span data-ttu-id="f2402-117">Microsoft Exchange Server 2010 или последний пакет обновления</span><span class="sxs-lookup"><span data-stu-id="f2402-117">Microsoft Exchange Server 2010 or latest service pack</span></span></p></li>
<li><p><span data-ttu-id="f2402-118">Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2402-118">Microsoft Exchange Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="f2402-119">Если вы используете Microsoft Exchange Server 2013, установите следующие роли Exchange Server в одном лесу или другом лесе в качестве Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="f2402-119">If you are using Microsoft Exchange Server 2013, install the following Exchange Server roles in either the same forest or a different forest as Lync Server 2013:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2402-120">клиентский доступ;</span><span class="sxs-lookup"><span data-stu-id="f2402-120">Client Access</span></span></p></li>
<li><p><span data-ttu-id="f2402-121">почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="f2402-121">Mailbox</span></span></p></li>
</ul>
<p><span data-ttu-id="f2402-122">Если Microsoft Exchange Server 2013 и единая система обмена сообщениями Exchange установлены в разных лесах, настройте каждый лес Exchange таким образом, чтобы он доверял лесу Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2402-122">If Microsoft Exchange Server 2013 and Exchange Unified Messaging (UM) are installed in different forests, configure each Exchange forest to trust the Lync Server 2013 forest.</span></span></p>
<p><span data-ttu-id="f2402-123">Если вы используете Exchange 2010, установите следующие роли Exchange Server либо в том же лесе, либо в другом лесе в составе Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="f2402-123">If you are using Exchange 2010, install the following Exchange Server roles in either the same forest or a different forest as Lync Server 2013:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2402-124">единая система обмена сообщениями;</span><span class="sxs-lookup"><span data-stu-id="f2402-124">Unified Messaging</span></span></p></li>
<li><p><span data-ttu-id="f2402-125">транспортный сервер-концентратор;</span><span class="sxs-lookup"><span data-stu-id="f2402-125">Hub Transport</span></span></p></li>
<li><p><span data-ttu-id="f2402-126">клиентский доступ;</span><span class="sxs-lookup"><span data-stu-id="f2402-126">Client Access</span></span></p></li>
<li><p><span data-ttu-id="f2402-127">почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="f2402-127">Mailbox</span></span></p></li>
</ul>
<p><span data-ttu-id="f2402-128">Если в разных лесах установлено приложение Lync Server 2013 и единая система обмена сообщениями Exchange (UM), настройте каждый лес Exchange таким образом, чтобы он доверял лесу Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2402-128">If Lync Server 2013 and Exchange Unified Messaging (UM) are installed in different forests, configure each Exchange forest to trust the Lync Server 2013 forest.</span></span></p></td>
<td><p><span data-ttu-id="f2402-129">Администраторы предприятия (если это первый сервер Exchange Server в организации)</span><span class="sxs-lookup"><span data-stu-id="f2402-129">Enterprise administrators (if this is the first Exchange Server in the organization)</span></span></p>
<p><span data-ttu-id="f2402-130">-ИЛИ-</span><span class="sxs-lookup"><span data-stu-id="f2402-130">-OR-</span></span></p>
<p><span data-ttu-id="f2402-131">Администратор организации Exchange (если это не первый сервер Exchange Server в организации)</span><span class="sxs-lookup"><span data-stu-id="f2402-131">Exchange Organization administrator (if this is not the first Exchange Server in the organization)</span></span></p></td>
<td><p><span data-ttu-id="f2402-132">Изучите соответствующую документацию для своей версии Exchange Server:</span><span class="sxs-lookup"><span data-stu-id="f2402-132">See the appropriate documentation for your version of Exchange Server:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="f2402-133">Документация по развертыванию Exchange Server 2007 по адресу <a href="https://go.microsoft.com/fwlink/p/?linkid=268694">https://go.microsoft.com/fwlink/p/?LinkId=268694</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-133">Exchange Server 2007 deployment documentation at <a href="https://go.microsoft.com/fwlink/p/?linkid=268694">https://go.microsoft.com/fwlink/p/?LinkId=268694</a>.</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="f2402-134">Документация по развертыванию пакета обновления для Exchange Server 2010 или последней версии <a href="https://go.microsoft.com/fwlink/p/?linkid=268695">https://go.microsoft.com/fwlink/p/?LinkId=268695</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-134">Exchange Server 2010 or latest service pack deployment documentation at <a href="https://go.microsoft.com/fwlink/p/?linkid=268695">https://go.microsoft.com/fwlink/p/?LinkId=268695</a>.</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="f2402-135">Microsoft Exchange Server 2013: планирование и развертывание <a href="https://go.microsoft.com/fwlink/p/?linkid=266569">https://go.microsoft.com/fwlink/p/?LinkId=266569</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-135">Microsoft Exchange Server 2013 Planning and Deployment at <a href="https://go.microsoft.com/fwlink/p/?linkid=266569">https://go.microsoft.com/fwlink/p/?LinkId=266569</a>.</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2402-136">Установите сертификаты.</span><span class="sxs-lookup"><span data-stu-id="f2402-136">Install certificates.</span></span></p></td>
<td><p><span data-ttu-id="f2402-137">Скачайте и установите сертификаты для каждого сервера UM Exchange в доверенном корневом центре сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="f2402-137">Download and install certificates for each Exchange UM server from a trusted root certificate authority (CA).</span></span> <span data-ttu-id="f2402-138">Сертификаты необходимы для взаимной защиты на уровне транспорта (MTLS) между серверами, на которых запущены службы Exchange UM и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2402-138">The certificates are required for mutual Transport Level Security (MTLS) between the servers running Exchange UM and Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="f2402-139">Администраторы</span><span class="sxs-lookup"><span data-stu-id="f2402-139">Administrators</span></span></p></td>
<td><p><span data-ttu-id="f2402-140"><a href="lync-server-2013-configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging.md">Настройка сертификатов на сервере, на котором работает единая система обмена сообщениями Microsoft Exchange Server</a></span><span class="sxs-lookup"><span data-stu-id="f2402-140"><a href="lync-server-2013-configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging.md">Configure certificates on the server running Microsoft Exchange Server Unified Messaging</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2402-141">Создайте и настройте новую абонентскую группу Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="f2402-141">Create and configure a new Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="f2402-142">На сервере Exchange UM Создайте абонентскую группу SIP, основываясь на конкретных требованиях к развертыванию вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f2402-142">On the Exchange UM server, create a SIP dial plan based on your organization’s specific deployment requirements.</span></span></p></td>
<td><p><span data-ttu-id="f2402-143">Администратор организации Exchange</span><span class="sxs-lookup"><span data-stu-id="f2402-143">Exchange Organization administrator</span></span></p></td>
<td><p><span data-ttu-id="f2402-144">Для Exchange 2007 SP1 или новейшего пакета обновления ознакомьтесь со &quot; сведениями о том, как создать универсальный код ресурса (URI) для единой системы обмена сообщениями &quot; в <a href="https://go.microsoft.com/fwlink/p/?linkid=268632">https://go.microsoft.com/fwlink/p/?linkId=268632</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-144">For Exchange 2007 SP1 or latest service pack, see &quot;How to Create a Unified Messaging SIP URI Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268632">https://go.microsoft.com/fwlink/p/?linkId=268632</a>.</span></span></p>
<p><span data-ttu-id="f2402-145">2010 или более поздней версии пакета обновления можно найти &quot; в разделе Создание абонентской группы единой системы обмена сообщениями &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268674">https://go.microsoft.com/fwlink/p/?linkId=268674</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-145">For Exchange 2010 or latest service pack, see &quot;Create a UM Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268674">https://go.microsoft.com/fwlink/p/?linkId=268674</a>.</span></span></p>
<p><span data-ttu-id="f2402-146">Для Exchange 2013 вы найдете в разделе Единая система обмена сообщениями <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-146">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2402-147">Настройте параметры безопасности для абонентской группы Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="f2402-147">Configure security settings for the Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="f2402-148">Чтобы зашифровать голосовой трафик для предприятия, настройте параметры безопасности в абонентской группе Exchange UM с помощью <strong>SIP Secure</strong> или <strong>Secure</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2402-148">To encrypt Enterprise Voice traffic, configure the security settings on the Exchange UM SIP dial plan as <strong>SIP Secured</strong> or <strong>Secured</strong>.</span></span> <span data-ttu-id="f2402-149">Это особенно важный шаг, если вы развернули или планируете развертывание устройств Lync Phone Edition в своей среде.</span><span class="sxs-lookup"><span data-stu-id="f2402-149">This is an especially important step if you have deployed or plan to deploy Lync Phone Edition devices in your environment.</span></span> <span data-ttu-id="f2402-150">Для функционирования устройств Lync Phone Edition в среде с интегрированной функцией интегрированной системы обмена сообщениями, параметры шифрования Lync Server должны быть согласованы с параметрами безопасности для абонентской группы Exchange.</span><span class="sxs-lookup"><span data-stu-id="f2402-150">For Lync Phone Edition devices to function in an environment with Exchange UM integration, Lync Server encryption settings must align with the Exchange UM dial plan security settings.</span></span> <span data-ttu-id="f2402-151">For details, refer to the Deployment documentation.</span><span class="sxs-lookup"><span data-stu-id="f2402-151">For details, refer to the Deployment documentation.</span></span></p></td>
<td><p><span data-ttu-id="f2402-152">Администратор организации Exchange</span><span class="sxs-lookup"><span data-stu-id="f2402-152">Exchange Organization administrator</span></span></p></td>
<td><p><span data-ttu-id="f2402-153"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Настройка единой системы обмена сообщениями в Microsoft Exchange для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f2402-153"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="f2402-154">2007 и более поздних версий пакета обновления можно найти в статье:</span><span class="sxs-lookup"><span data-stu-id="f2402-154">For Exchange 2007 SP1 or latest service pack, see also:</span></span></p>
<p><span data-ttu-id="f2402-155">&quot;Настройка безопасности для абонентской группы единой системы обмена сообщениями &quot; по адресу <a href="https://go.microsoft.com/fwlink/p/?linkid=268696">https://go.microsoft.com/fwlink/p/?LinkId=268696</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-155">&quot;How to Configure Security on a Unified Messaging Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268696">https://go.microsoft.com/fwlink/p/?LinkId=268696</a>.</span></span></p>
<p><span data-ttu-id="f2402-156">Для Exchange 2010 или более поздней версии пакета обновления см. также следующие статьи:</span><span class="sxs-lookup"><span data-stu-id="f2402-156">For Exchange 2010 or latest service pack, see also:</span></span></p>
<p><span data-ttu-id="f2402-157">&quot;Настройте безопасность VoIP для абонентской группы единой системы обмена сообщениями &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268697">https://go.microsoft.com/fwlink/p/?LinkId=268697</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-157">&quot;Configure VoIP Security on a UM Dial Plan&quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268697">https://go.microsoft.com/fwlink/p/?LinkId=268697</a>.</span></span></p>
<p><span data-ttu-id="f2402-158">Для Exchange 2013 вы найдете в разделе Единая система обмена сообщениями <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-158">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2402-159">Добавьте серверы единой системы обмена сообщениями в абонентскую группу Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="f2402-159">Add Unified Messaging servers to the Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="f2402-160">To enable a newly installed Unified Messaging server to answer and process incoming calls, you must add the Unified Messaging server to a UM dial plan.</span><span class="sxs-lookup"><span data-stu-id="f2402-160">To enable a newly installed Unified Messaging server to answer and process incoming calls, you must add the Unified Messaging server to a UM dial plan.</span></span> <span data-ttu-id="f2402-161">В этом случае добавьте сервер в абонентскую группу Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="f2402-161">In this case, add the server to the Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="f2402-162">Администраторы</span><span class="sxs-lookup"><span data-stu-id="f2402-162">Administrators</span></span></p>
<p><span data-ttu-id="f2402-163">Администраторы Exchange Server</span><span class="sxs-lookup"><span data-stu-id="f2402-163">Exchange Server administrators</span></span></p></td>
<td><p><span data-ttu-id="f2402-164">Инструкции по &quot; добавлению сервера единой системы обмена сообщениями в телефонную группу для Exchange 2007 SP1 или новейшего пакета обновления &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268681">https://go.microsoft.com/fwlink/p/?linkId=268681</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-164">For Exchange 2007 SP1 or latest service pack, see &quot;How to Add Unified Messaging Server to a Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268681">https://go.microsoft.com/fwlink/p/?linkId=268681</a>.</span></span></p>
<p><span data-ttu-id="f2402-165">Для Exchange 2010 или новейшего пакета обновления ознакомьтесь со сведениями &quot; Просмотр и Настройка свойств сервера UM &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268682">https://go.microsoft.com/fwlink/p/?linkId=268682</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-165">For Exchange 2010 or latest service pack, see &quot;View or Configure the Properties of a UM Server&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268682">https://go.microsoft.com/fwlink/p/?linkId=268682</a>.</span></span></p>
<p><span data-ttu-id="f2402-166">Для Exchange 2013 вы найдете в разделе Единая система обмена сообщениями <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-166">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2402-167">Настройте SIP-адреса для почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="f2402-167">Configure mailboxes with SIP addresses.</span></span></p></td>
<td><p><span data-ttu-id="f2402-168">Назначьте адреса SIP почтовым ящикам пользователей корпоративной голосовой связи, которые будут использовать возможности Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="f2402-168">Assign SIP addresses to the mailboxes of Enterprise Voice users who will be using Exchange UM features.</span></span></p></td>
<td><p><span data-ttu-id="f2402-169">Администратор Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2402-169">Lync Server 2013 administrator</span></span></p>
<p><span data-ttu-id="f2402-170">Администратор получателей Exchange</span><span class="sxs-lookup"><span data-stu-id="f2402-170">Exchange Recipient administrator</span></span></p></td>
<td><p><span data-ttu-id="f2402-171">В 2007 и более поздних пакетах обновления можно узнать &quot; , как добавить, удалить или изменить адрес SIP для пользователя UM-Enabled &quot; по адресу <a href="https://go.microsoft.com/fwlink/p/?linkid=268698">https://go.microsoft.com/fwlink/p/?LinkId=268698</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-171">For Exchange 2007 SP1 or latest service pack, see &quot;How to Add, Remove, or Modify a SIP Address for a UM-Enabled User&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268698">https://go.microsoft.com/fwlink/p/?LinkId=268698</a>.</span></span></p>
<p><span data-ttu-id="f2402-172">2010 или более поздней версии пакета обновления можно узнать в разделе &quot; изменение адреса SIP для пользователя UM-Enabled &quot; по адресу <a href="https://go.microsoft.com/fwlink/p/?linkid=268699">https://go.microsoft.com/fwlink/p/?LinkId=268699</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-172">For Exchange 2010 or latest service pack, see &quot;Modify a SIP Address for a UM-Enabled User&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268699">https://go.microsoft.com/fwlink/p/?LinkId=268699</a>.</span></span></p>
<p><span data-ttu-id="f2402-173">Для Exchange 2013 вы найдете в разделе Единая система обмена сообщениями <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-173">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2402-174">Запустите скрипт exchucutil.ps1.</span><span class="sxs-lookup"><span data-stu-id="f2402-174">Run the exchucutil.ps1 script.</span></span></p></td>
<td><p><span data-ttu-id="f2402-175">На сервере с запущенными службами Exchange UM откройте командную консоль Exchange и запустите сценарий exchucutil.ps1, который выполняет указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f2402-175">On the server running Exchange UM services, open the Exchange Management Shell and run the exchucutil.ps1 script, which does the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2402-176">Предоставляет Lync Server 2013 разрешение на чтение объектов доменных служб Active Directory для Exchange UM, а именно, абонентские группы SIP, созданные в предыдущей задаче.</span><span class="sxs-lookup"><span data-stu-id="f2402-176">Grants Lync Server 2013 permission to read Exchange UM Active Directory Domain Services objects, specifically, the SIP dial plans created in the previous task.</span></span></p></li>
<li><p><span data-ttu-id="f2402-177">Создает объект шлюза для единой системы обмена сообщениями в службе каталогов Active Directory для каждого пула Lync Server 2013 Enterprise Edition или Standard Edition Server, на котором размещаются пользователи, поддерживающие корпоративную голосовую почту.</span><span class="sxs-lookup"><span data-stu-id="f2402-177">Creates a Unified Messaging IP gateway object in Active Directory for each Lync Server 2013 Enterprise Edition pool or Standard Edition server that hosts users who are enabled for Enterprise Voice.</span></span></p></li>
<li><p><span data-ttu-id="f2402-178">Создает группу слежения UM для каждого шлюза.</span><span class="sxs-lookup"><span data-stu-id="f2402-178">Creates an Exchange UM hunt group for each gateway.</span></span> <span data-ttu-id="f2402-179">The hunt group pilot identifier will be the name of the dial plan that is associated with the corresponding gateway.</span><span class="sxs-lookup"><span data-stu-id="f2402-179">The hunt group pilot identifier will be the name of the dial plan that is associated with the corresponding gateway.</span></span> <span data-ttu-id="f2402-180">These need to be mapped 1:1 if there is more than one dial plan.</span><span class="sxs-lookup"><span data-stu-id="f2402-180">These need to be mapped 1:1 if there is more than one dial plan.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="f2402-181">Администратор организации Exchange</span><span class="sxs-lookup"><span data-stu-id="f2402-181">Exchange Organization administrator</span></span></p>
<p><span data-ttu-id="f2402-182">Администратор получателей Exchange</span><span class="sxs-lookup"><span data-stu-id="f2402-182">Exchange Recipient administrator</span></span></p></td>
<td><p><span data-ttu-id="f2402-183"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Настройка единой системы обмена сообщениями в Microsoft Exchange для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f2402-183"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2402-184">Настройте абонентские группы Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2402-184">Configure Lync Server 2013 dial plans.</span></span></p></td>
<td><p><span data-ttu-id="f2402-185">Если вы интегрируется с Exchange 2007 с пакетом обновления 1 (SP1) или более поздним пакетом обновления или Exchange 2010, создайте новый план голосовой коммутируемой телефонной связи с именем, совпадающим с полным доменным именем Exchange для абонентского плана.</span><span class="sxs-lookup"><span data-stu-id="f2402-185">If you are integrating with Exchange 2007 SP1 or latest service pack, or Exchange 2010, create a new Enterprise Voice dial plan with a name that matches the Exchange UM dial plan fully qualified domain name (FQDN).</span></span></p>



> [!NOTE]
> <span data-ttu-id="f2402-186">Это потребуется сделать для каждой абонентской группы единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f2402-186">You will need to do this for each UM Dial plan.</span></span>


<p><span data-ttu-id="f2402-187">Если вы интегрируется с Exchange 2010 с пакетом обновления 1 (SP1), убедитесь в том, что настроены подходящие планы глобальных абонентов или уровней сайтов или пулов.</span><span class="sxs-lookup"><span data-stu-id="f2402-187">If you are integrating with Exchange 2010 SP1, ensure that suitable global/site-level or pool-level Enterprise Voice dial plans have been configured.</span></span></p>



> [!NOTE]
> <span data-ttu-id="f2402-188">При интеграции с Exchange 2010 с пакетом обновления 1 (SP1) абонентская группа Lync Server и имена абонентских групп UM Exchange не должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="f2402-188">If you are integrating with Exchange 2010 SP1, the Lync Server dial plan and Exchange UM SIP dial plan names do not need to match.</span></span>

</td>
<td><p><span data-ttu-id="f2402-189">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="f2402-189">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="f2402-190"><a href="lync-server-2013-configuring-dial-plans.md">Настройка абонентских групп в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f2402-190"><a href="lync-server-2013-configuring-dial-plans.md">Configuring dial plans in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2402-191">Запустите средство интеграции единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f2402-191">Run the Exchange UM Integration tool.</span></span></p></td>
<td><p><span data-ttu-id="f2402-192">На сервере Lync Server 2013 выполните <strong>ocsumutil.exe</strong>, который:</span><span class="sxs-lookup"><span data-stu-id="f2402-192">On the Lync Server 2013, run <strong>ocsumutil.exe</strong>, which:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2402-193">создает объекты контактов абонентского доступа и автосекретаря;</span><span class="sxs-lookup"><span data-stu-id="f2402-193">Creates Subscriber Access and Auto Attendant contact objects.</span></span></p></li>
<li><p><span data-ttu-id="f2402-194">Проверка наличия корпоративной телефонной группы с именем, совпадающим с полным доменным планом Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="f2402-194">Validates that there is an Enterprise Voice dial plan with a name that matches the Exchange UM dial plan FQDN.</span></span> <span data-ttu-id="f2402-195">Если вы используете Exchange 2010 с пакетом обновления 1 (SP1) или более поздней версии, имена абонентской группы не должны совпадать, и вы можете пропустить предупреждение этого средства.</span><span class="sxs-lookup"><span data-stu-id="f2402-195">If you are running Exchange 2010 SP1 or later, the dial plan names do not need to match, and you can ignore the tool’s warning about this.</span></span></p></li>
</ul>
<p><span data-ttu-id="f2402-196">Это средство работает, проверяя параметры службы единой системы обмена сообщениями в Active Directory и разрешая администратору Lync Server 2013 просматривать, создавать и редактировать объекты контактов.</span><span class="sxs-lookup"><span data-stu-id="f2402-196">This tool works by scanning the Active Directory for Exchange UM settings and allowing the Lync Server 2013 administrator to view, create, and edit contact objects.</span></span></p></td>
<td><p><span data-ttu-id="f2402-197">RTCUniversalServerAdmins <em>и</em> RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="f2402-197">RTCUniversalServerAdmins <em>and</em> RTCUniversalUserAdmins</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="f2402-198">Для успешного выполнения ocsumutil.exe пользователь должен принадлежать обеим этим группам.</span><span class="sxs-lookup"><span data-stu-id="f2402-198">To run ocsumutil.exe successfully, the user must belong to both of these groups.</span></span>





> [!NOTE]
> <span data-ttu-id="f2402-199">To create Contact objects, the user who runs ocsumutil.exe must have the correct permission to the Active Directory organizational unit (OU) where the new contact objects are stored.</span><span class="sxs-lookup"><span data-stu-id="f2402-199">To create Contact objects, the user who runs ocsumutil.exe must have the correct permission to the Active Directory organizational unit (OU) where the new contact objects are stored.</span></span> <span data-ttu-id="f2402-200">This permission can be granted by running the <STRONG>Grant-CsOUPermission</STRONG> cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2402-200">This permission can be granted by running the <STRONG>Grant-CsOUPermission</STRONG> cmdlet.</span></span> <span data-ttu-id="f2402-201">Подробные сведения можно найти в руководстве по среде Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="f2402-201">For details, see the Lync Server Management Shell documentation.</span></span>

</td>
<td><p><span data-ttu-id="f2402-202"><a href="lync-server-2013-configure-lync-server-2013-to-work-with-unified-messaging-on-microsoft-exchange-server.md">Настройка Lync Server 2013 для работы с единой системой обмена сообщениями на Microsoft Exchange Server</a></span><span class="sxs-lookup"><span data-stu-id="f2402-202"><a href="lync-server-2013-configure-lync-server-2013-to-work-with-unified-messaging-on-microsoft-exchange-server.md">Configure Lync Server 2013 to work with Unified Messaging on Microsoft Exchange Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2402-203">При необходимости выполните другие действия по настройке голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="f2402-203">If necessary, perform other Enterprise Voice configuration steps.</span></span></p></td>
<td><p><span data-ttu-id="f2402-204">Если вы еще не настроили параметры корпоративной голосовой связи на серверах или пользователях, выполните одно или несколько из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="f2402-204">If you have not already configured Enterprise Voice settings on your servers or users, do one or more of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2402-205">разверните и настройте</span><span class="sxs-lookup"><span data-stu-id="f2402-205">Deploy and configure</span></span></p>
<p><span data-ttu-id="f2402-206">шлюзы и серверы-посредники телефонной сети общего пользования (ТСОП);</span><span class="sxs-lookup"><span data-stu-id="f2402-206">Public switched telephone network (PSTN) gateways and Mediation Servers</span></span></p></li>
<li><p><span data-ttu-id="f2402-207">определите политики голосовой связи, записи использования ТСОП и маршруты исходящих вызовов;</span><span class="sxs-lookup"><span data-stu-id="f2402-207">Define voice policies, PSTN usage records, and outbound call routes.</span></span></p></li>
<li><p><span data-ttu-id="f2402-208">активируйте корпоративную голосовую связь для пользователей;</span><span class="sxs-lookup"><span data-stu-id="f2402-208">Enable users for Enterprise Voice.</span></span></p></li>
<li><p><span data-ttu-id="f2402-209">при необходимости настройте абонентские группы для определенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f2402-209">Optionally, configure specific users with dial plans.</span></span></p></li>
</ul>
<p><span data-ttu-id="f2402-210">В зависимости от того, какие возможности поддерживаются корпоративными голосовыми функциями, могут потребоваться другие этапы настройки.</span><span class="sxs-lookup"><span data-stu-id="f2402-210">Other configuration steps may be required depending on the Enterprise Voice features that you enable.</span></span></p></td>
<td><p><span data-ttu-id="f2402-211">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="f2402-211">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="f2402-212">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="f2402-212">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="f2402-213">См. следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="f2402-213">See topics in the following sections:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2402-214"><a href="lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md">Настройка политик голосовой связи, записей использования КТСОП и голосовых маршрутов в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f2402-214"><a href="lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</a></span></span></p></li>
<li><p><span data-ttu-id="f2402-215"><a href="lync-server-2013-deploying-enterprise-voice.md">Развертывание корпоративной голосовой связи в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f2402-215"><a href="lync-server-2013-deploying-enterprise-voice.md">Deploying Enterprise Voice in Lync Server 2013</a></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2402-216">Включите пользователей корпоративной голосовой почты для Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="f2402-216">Enable Enterprise Voice users for Exchange UM.</span></span></p></td>
<td><p><span data-ttu-id="f2402-217">На сервере Exchange UM убедитесь, что политика почтового ящика единой системы обмена сообщениями создана и у каждого пользователя есть уникальное назначение добавочного номера, а затем включите ее для единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f2402-217">On the Exchange UM server, ensure that a Unified Messaging mailbox policy has been created and that each user has a unique extension number assignment, and then enable the user for Unified Messaging.</span></span></p></td>
<td><p><span data-ttu-id="f2402-218">Администратор получателей Exchange</span><span class="sxs-lookup"><span data-stu-id="f2402-218">Exchange Recipient administrator</span></span></p></td>
<td><p><span data-ttu-id="f2402-219">Для Exchange 2007 SP1 или более поздней версии ознакомьтесь со сведениями &quot; о том, как разрешить пользователям единую систему обмена сообщениями на веб- &quot; странице <a href="https://go.microsoft.com/fwlink/p/?linkid=268700">https://go.microsoft.com/fwlink/p/?LinkId=268700</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-219">For Exchange 2007 SP1 or latest service pack, see &quot;How to Enable a User for Unified Messaging&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268700">https://go.microsoft.com/fwlink/p/?LinkId=268700</a>.</span></span></p>
<p><span data-ttu-id="f2402-220">2010 или более поздней версии пакета обновления можно узнать &quot; в разделе Включение поддержки единой системы обмена сообщениями для пользователей Exchange &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268701">https://go.microsoft.com/fwlink/p/?LinkId=268701</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-220">For Exchange 2010 or latest service pack, see &quot;Enable a User for Unified Messaging&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268701">https://go.microsoft.com/fwlink/p/?LinkId=268701</a>.</span></span></p>
<p><span data-ttu-id="f2402-221">Для Exchange 2013 вы найдете в разделе Единая система обмена сообщениями <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="f2402-221">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr><span data-ttu-id="f2402-222">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2402-222">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

