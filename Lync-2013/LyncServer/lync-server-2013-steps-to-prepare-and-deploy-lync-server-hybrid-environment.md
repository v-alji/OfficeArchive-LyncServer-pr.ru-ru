---
title: 'Lync Server 2013: действия по подготовке и развертыванию гибридной среды Lync Server'
description: 'Lync Server 2013: шаги для подготовки и развертывания гибридной среды Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Steps to prepare and deploy Lync Server 2013 hybrid environment
ms:assetid: a50d4f7b-63f4-4663-af63-56ca87e4e3e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205157(v=OCS.15)
ms:contentKeyID: 48185060
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ffb791a8a45b2220d8987c8d688f346447747c00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398128"
---
# <a name="steps-to-prepare-and-deploy-lync-server-2013-hybrid-environment"></a><span data-ttu-id="26cb7-103">Действия по подготовке и развертыванию гибридной среды Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26cb7-103">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26cb7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26cb7-104">

<span> </span></span></span>

<span data-ttu-id="26cb7-105">_**Тема последнего изменения:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="26cb7-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="26cb7-106">В следующей таблице перечислены шаги, необходимые для подготовки среды для гибридного развертывания в Skype для бизнеса Online и Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="26cb7-106">The following table lists the steps required to prepare your environment for a hybrid deployment with Skype for Business Online and Microsoft Office 365.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26cb7-107">Выполнение</span><span class="sxs-lookup"><span data-stu-id="26cb7-107">Completed?</span></span></th>
<th><span data-ttu-id="26cb7-108">Шаг</span><span class="sxs-lookup"><span data-stu-id="26cb7-108">Step</span></span></th>
<th><span data-ttu-id="26cb7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="26cb7-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="26cb7-110">Создание учетной записи клиента для Office 365 и включение Lync Online</span><span class="sxs-lookup"><span data-stu-id="26cb7-110">Create a tenant account for Office 365 and enable Lync Online</span></span></p></td>
<td><p><span data-ttu-id="26cb7-111">Узнайте о Office 365 и Lync Online в <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-111">Learn about Office 365 and Lync Online at <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">Office 365</a>.</span></span></p>
<p><span data-ttu-id="26cb7-112">Чтобы убедиться в том, что ваша среда готова к работе с Office 365, ознакомьтесь с <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">требованиями к системе</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-112">To make sure that your environment is ready for Office 365, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">System Requirements</a>.</span></span></p>
<p><span data-ttu-id="26cb7-113">Подробные сведения о настройке Office 365 можно найти <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">в разделе Начало работы с office 365</a> и <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Настройка Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-113">For details about setting up Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Getting Started with Office 365</a> and <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Set Up Office 365</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="26cb7-114">Добавление домена и проверка прав на владение доменом</span><span class="sxs-lookup"><span data-stu-id="26cb7-114">Add your domain and verify ownership</span></span></p></td>
<td><p><span data-ttu-id="26cb7-115">Домен иногда также называется <em>доменом запоминающиеся</em>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-115">Your domain is sometimes also referred to as your <em>vanity domain</em>.</span></span> <span data-ttu-id="26cb7-116">Необходимо добавить домен в организацию Office 365, а затем выполнить необходимые действия для проверки домена с помощью Office 365.</span><span class="sxs-lookup"><span data-stu-id="26cb7-116">You must add your domain to your Office 365 organization, and then follow the steps to validate the domain with Office 365.</span></span> <span data-ttu-id="26cb7-117">Это необходимо для подтверждения того, что вы являетесь владельцем домена.</span><span class="sxs-lookup"><span data-stu-id="26cb7-117">This is to confirm that you are the owner of the domain.</span></span></p>
<p><span data-ttu-id="26cb7-118">Чтобы добавить домен в организацию Office 365, выполните действия, описанные в статье <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Добавление домена в office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-118">To add your domain to your Office 365 organization, follow the steps described at <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Add your domain to Office 365</a>.</span></span></p>
<p><span data-ttu-id="26cb7-119">Выполните все действия, описанные в каждом разделе раздела, в том числе &quot; изменить записи DNS для служб Office 365.&quot;</span><span class="sxs-lookup"><span data-stu-id="26cb7-119">Complete all of the steps in each section in the topic, including &quot;Edit DNS records for your Office 365 services.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="26cb7-120">Проверка готовности среды</span><span class="sxs-lookup"><span data-stu-id="26cb7-120">Verify environment readiness</span></span></p></td>
<td><p><span data-ttu-id="26cb7-121">Вы можете использовать помощник по установке Office 365, который поможет вам развернуть Office 365.</span><span class="sxs-lookup"><span data-stu-id="26cb7-121">You can use the Office 365 Setup Assistant to help you deploy Office 365.</span></span> <span data-ttu-id="26cb7-122">Дополнительные сведения можно найти <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">в разделе Использование помощника по настройке, чтобы определить готовность Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-122">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">Use Setup Assistant to determine Office 365 readiness</a>.</span></span></p>
<p><span data-ttu-id="26cb7-123">Подробнее об использовании этого средства и развертывании Office 365 можно найти в <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">руководстве по развертыванию office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-123">For details about using the tool and deploying Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Office 365 deployment guide</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="26cb7-124">Подготовка к синхронизации Active Directory</span><span class="sxs-lookup"><span data-stu-id="26cb7-124">Prepare for Active Directory synchronization</span></span></p></td>
<td><p><span data-ttu-id="26cb7-125">Синхронизация службы каталогов Active Directory позволяет постоянно синхронизировать локальную службу Active Directory с Office 365.</span><span class="sxs-lookup"><span data-stu-id="26cb7-125">Active Directory synchronization keeps your on-premises Active Directory continuously synchronized with Office 365.</span></span> <span data-ttu-id="26cb7-126">Это позволяет создавать синхронизированные версии каждой учетной записи пользователя и группы, а также выполнять синхронизацию глобального списка адресов (GAL) из локальной среды Microsoft Exchange Server с Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="26cb7-126">This lets you create synchronized versions of each user account and group, and also enables global address list (GAL) synchronization from your local Microsoft Exchange Server environment to Microsoft Exchange Online.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="26cb7-127">Вы должны синхронизировать учетные записи для всех пользователей Lync в вашей организации между локальными и Интернет-развертываниями Lync, даже если пользователи не перемещаются в Lync Online.</span><span class="sxs-lookup"><span data-stu-id="26cb7-127">You need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="26cb7-128">Если не все пользователи синхронизированы, связь между локальными и сетевыми пользователи в организации может функционировать неправильно.</span><span class="sxs-lookup"><span data-stu-id="26cb7-128">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>


</div>
<p><span data-ttu-id="26cb7-129">Чтобы подготовить среду для синхронизации Active Directory, выполните действия, описанные в разделе <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">схема синхронизации службы каталогов</a>, в том числе Настройка единого входа.</span><span class="sxs-lookup"><span data-stu-id="26cb7-129">To prepare your environment for Active Directory synchronization, follow the steps described in <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Directory synchronization Roadmap</a>, including setting up single sign-on.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="26cb7-130">Создание сертификатов для служб федерации Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="26cb7-130">Create certificates for Active Directory Federation Services (AD FS)</span></span></p></td>
<td><p><span data-ttu-id="26cb7-131">Вам потребуется создать сертификаты, которые будут использоваться для федерации удостоверений с Office 365.</span><span class="sxs-lookup"><span data-stu-id="26cb7-131">You will need to create the certificates that are used for identity federation with Office 365.</span></span> <span data-ttu-id="26cb7-132">Дополнительные сведения можно найти в разделе "сертификаты сервера федерации" плана и развертывания AD FS для использования с одним разделом для единого входа в <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">контрольном списке: использование служб ADFS для реализации единого входа и управления ими</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-132">For more information, see the “Federation server certificates” section of the Plan for and deploy AD FS for use with single sign-on topic at <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">Checklist: Use AD FS to implement and manage single sign-on</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="26cb7-133">Назначение сертификатов для AD FS</span><span class="sxs-lookup"><span data-stu-id="26cb7-133">Assign certificates for AD FS</span></span></p></td>
<td><p><span data-ttu-id="26cb7-134">После создания сертификатов, используемых для федерации удостоверений с Office 365, необходимо установить и назначить их.</span><span class="sxs-lookup"><span data-stu-id="26cb7-134">After you create the certificates that are used for identity federation with Office 365, you must install and assign them.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="26cb7-135">Перемещение пилотных пользователей в Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="26cb7-135">Move pilot users to Skype for Business Online</span></span></p></td>
<td><p><span data-ttu-id="26cb7-136">После того как вы закончите процедуру подготовки и настройки среды для Skype для бизнеса Online, вы сможете переместить пилотных пользователей в Lync Online.</span><span class="sxs-lookup"><span data-stu-id="26cb7-136">After you have completed the steps to prepare and configure your environment for Skype for Business Online, you can start moving pilot users to Lync Online.</span></span></p>
<p><span data-ttu-id="26cb7-137">Дополнительные сведения <a href="lync-server-2013-move-users-to-lync-online.md">можно найти в разделе Перемещение пользователей в Lync Online в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-137">See <a href="lync-server-2013-move-users-to-lync-online.md">Move users to Lync Online in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="26cb7-138">Администрирование пользователей в гибридном развертывании</span><span class="sxs-lookup"><span data-stu-id="26cb7-138">Administering users in a hybrid deployment</span></span></p></td>
<td><p><span data-ttu-id="26cb7-139">Подробнее об администрировании пользователей в гибридном развертывании можно узнать в разделе <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Администрирование пользователей в гибридном развертывании Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="26cb7-139">For details about how to administer users in a hybrid deployment, see <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</a>.</span></span></p></td>
</tr><span data-ttu-id="26cb7-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26cb7-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

