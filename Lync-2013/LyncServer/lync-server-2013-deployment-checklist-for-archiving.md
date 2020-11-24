---
title: 'Lync Server 2013: контрольный список развертывания для архивации'
description: 'Lync Server 2013: контрольный список развертывания для архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for Archiving
ms:assetid: 7479734d-be01-40d9-ad82-320a09d19d04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205009(v=OCS.15)
ms:contentKeyID: 48184516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e9fb3085950aa1e8a750d36a0aeb8592bc18113
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397945"
---
# <a name="deployment-checklist-for-archiving-in-lync-server-2013"></a><span data-ttu-id="0feed-103">Контрольный список развертывания для архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0feed-103">Deployment checklist for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0feed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0feed-104">

<span> </span></span></span>

<span data-ttu-id="0feed-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="0feed-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="0feed-106">Архивация автоматически устанавливается на каждый сервер переднего плана в Lync Server 2013, но необходимо настроить его, прежде чем вы сможете использовать его.</span><span class="sxs-lookup"><span data-stu-id="0feed-106">Archiving is automatically installed on each Front End Server in your Lync Server 2013 deployment, but you still need to set it up before you can use it.</span></span> <span data-ttu-id="0feed-107">Действия, которые необходимо выполнить для настройки, как описано в этом разделе, составляют развертывание архивации.</span><span class="sxs-lookup"><span data-stu-id="0feed-107">The steps required to set it up, as summarized in this section, constitute the deployment of Archiving.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="0feed-108">Последовательность развертывания</span><span class="sxs-lookup"><span data-stu-id="0feed-108">Deployment Sequence</span></span>

<span data-ttu-id="0feed-109">Способ настройки архивации зависит от того, какой вариант хранилища вы выбираете:</span><span class="sxs-lookup"><span data-stu-id="0feed-109">How you set up Archiving depends on which storage option you choose:</span></span>

  - <span data-ttu-id="0feed-110">Если вы используете Microsoft Exchange Integration для всех пользователей в развертывании, вам не нужно настраивать политики архивирования для Lync Server 2013 для пользователей.</span><span class="sxs-lookup"><span data-stu-id="0feed-110">If you use Microsoft Exchange integration for all users in your deployment, you don’t need to configure Lync Server 2013 Archiving policies for your users.</span></span> <span data-ttu-id="0feed-111">Вместо этого настройте политики хранения In-Place Exchange для поддержки архивации пользователей, размещенных на Exchange 2013, с почтовыми ящиками на In-Place удержанием.</span><span class="sxs-lookup"><span data-stu-id="0feed-111">Instead, configure your Exchange In-Place Hold policies to support archiving for users homed on Exchange 2013, with their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="0feed-112">Подробные сведения о настройке этих политик можно найти в документации по продукту Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0feed-112">For details about configuring these policies, see the Exchange 2013 product documentation.</span></span>

  - <span data-ttu-id="0feed-113">Если вы не используете интеграцию Microsoft Exchange для всех пользователей в развертывании, необходимо добавить в топологию базы данных архивации в Lync Server (базы данных SQL Server), а затем опубликовать ее, а также настроить политики и параметры для пользователей, прежде чем можно будет архивировать данные для этих пользователей.</span><span class="sxs-lookup"><span data-stu-id="0feed-113">If you do not use Microsoft Exchange integration for all users in your deployment, you need to add Lync Server Archiving databases (SQL Server databases) to your topology and then publish it, as well as configure policies and settings for your users, before you can archive data for those users.</span></span> <span data-ttu-id="0feed-114">Вы можете развернуть базу данных архивации одновременно с развертыванием начальной топологии или после развертывания по крайней мере одного пула переднего плана или сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="0feed-114">You can deploy Archiving databases at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span> <span data-ttu-id="0feed-115">В этом документе описано, как развернуть архивные базы данных, добавив их в существующее развертывание.</span><span class="sxs-lookup"><span data-stu-id="0feed-115">This document describes how to deploy Archiving databases by adding them to an existing deployment.</span></span>

<span data-ttu-id="0feed-116">Если вы включите архивацию на одном интерфейсном пуле или на сервере Standard Edition, необходимо включить ее для всех других пулов интерфейсов и серверов Standard Edition в развертывании.</span><span class="sxs-lookup"><span data-stu-id="0feed-116">If you enable archiving in one Front End pool or Standard Edition server, you should enable it for all other Front End pools and Standard Edition servers in your deployment.</span></span> <span data-ttu-id="0feed-117">Это следует сделать, поскольку пользователи, чьи коммуникации требуется архивировать, могут быть приглашены в текстовую беседу или на собрания, размещаемые в другом пуле.</span><span class="sxs-lookup"><span data-stu-id="0feed-117">This is because users whose communications are required to be archived can be invited to a group IM conversation or meetings hosted on a different pool.</span></span> <span data-ttu-id="0feed-118">Если там архивация не включена, то сеанс может быть архивирован не полностью.</span><span class="sxs-lookup"><span data-stu-id="0feed-118">If archiving is not enabled on the pool where the conversation or meeting is hosted, the complete session may not be archived.</span></span> <span data-ttu-id="0feed-119">В этих случаях мгновенные сообщения пользователей с включенной архивацией могут быть архивированы, но не для файлов содержимого конференций, а также событий присоединения и выхода из конференций.</span><span class="sxs-lookup"><span data-stu-id="0feed-119">In these cases, IMs with archiving-enabled users still can be archived, but not for conferencing content files, and conference join or leave events.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0feed-120">Если в вашей организации важна архивация в целях соответствия требованиям, не забудьте развернуть архивацию, настроить политики и другие параметры на соответствующем уровне и включить ее для всех нужных пользователей, прежде чем включать пользователей для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0feed-120">If archiving is critical in your organization for compliance reasons, be sure to deploy Archiving, configure policies and other options at the appropriate level, and enable it for all appropriate users, before you enable those users for Lync Server 2013.</span></span>



</div>

</div>

<div>

## <a name="archiving-deployment-process"></a><span data-ttu-id="0feed-121">Процесс развертывания архивации</span><span class="sxs-lookup"><span data-stu-id="0feed-121">Archiving Deployment Process</span></span>

<span data-ttu-id="0feed-122">В следующей таблице дается обзор действий, необходимых для развертывания архивации в существующей топологии.</span><span class="sxs-lookup"><span data-stu-id="0feed-122">The following table provides an overview of the steps required to deploy archiving in an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0feed-123">Этап</span><span class="sxs-lookup"><span data-stu-id="0feed-123">Phase</span></span></th>
<th><span data-ttu-id="0feed-124">Шаги</span><span class="sxs-lookup"><span data-stu-id="0feed-124">Steps</span></span></th>
<th><span data-ttu-id="0feed-125">Роли и членство в группах</span><span class="sxs-lookup"><span data-stu-id="0feed-125">Roles and group memberships</span></span></th>
<th><span data-ttu-id="0feed-126">Документация</span><span class="sxs-lookup"><span data-stu-id="0feed-126">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0feed-127"><strong>Установка необходимого оборудования и программного обеспечения</strong></span><span class="sxs-lookup"><span data-stu-id="0feed-127"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="0feed-128">Для использования интеграции с Microsoft Exchange (с помощью Exchange 2013 для хранения архивов некоторых или всех пользователей) необходимо установить существующее развертывание Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0feed-128">To use Microsoft Exchange integration (using Exchange 2013 for archiving storage for some or all users), you need an existing Exchange 2013 deployment.</span></span></p></li>
<li><p><span data-ttu-id="0feed-129">Чтобы использовать отдельные архивные базы данных (с помощью баз данных SQL Server) для хранения архивов для некоторых или всех пользователей, SQL Server на сервере, который будет хранить данные для архивации.</span><span class="sxs-lookup"><span data-stu-id="0feed-129">To use separate Archiving databases (using SQL Server databases) for archiving storage for some or all users, SQL Server on the server that will store archiving data.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="0feed-130">Архивация выполняется на серверах переднего плана корпоративного пула и стандартных серверах выпуска.</span><span class="sxs-lookup"><span data-stu-id="0feed-130">Archiving runs on Front End Servers of an Enterprise pool and Standard Edition servers.</span></span> <span data-ttu-id="0feed-131">Для нее не существует дополнительных требований к оборудованию или программному обеспечению помимо требований для установки этих серверов.</span><span class="sxs-lookup"><span data-stu-id="0feed-131">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span>


</div></td>
<td><p><span data-ttu-id="0feed-132">Пользователь домена, являющийся членом локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="0feed-132">Domain user who is a member of the local administrators group.</span></span></p></td>
<td><p><span data-ttu-id="0feed-133"><a href="lync-server-2013-supported-hardware.md">Поддерживаемое оборудование для Lync Server 2013</a> в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="0feed-133"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation.</span></span></p>
<p><span data-ttu-id="0feed-134"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Поддержка серверного программного обеспечения и инфраструктуры в Lync Server 2013</a> в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="0feed-134"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation.</span></span></p>
<p><span data-ttu-id="0feed-135"><a href="lync-server-2013-technical-requirements-for-archiving.md">Технические требования для архивации в Lync Server 2013</a> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="0feed-135"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="0feed-136"><a href="lync-server-2013-setting-up-systems-and-infrastructure-for-archiving.md">Настройка системы и инфраструктуры для архивации в Lync Server 2013</a> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="0feed-136"><a href="lync-server-2013-setting-up-systems-and-infrastructure-for-archiving.md">Setting up systems and infrastructure for Archiving in Lync Server 2013</a> in the Deployment documentation.</span></span></p>
<p><span data-ttu-id="0feed-137"><a href="lync-server-2013-exchange-and-sharepoint-integration-support.md">Поддержка интеграции Exchange Server и SharePoint в Lync server 2013</a> в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="0feed-137"><a href="lync-server-2013-exchange-and-sharepoint-integration-support.md">Exchange Server and SharePoint integration support in Lync Server 2013</a> in the Supportability documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feed-138"><strong>Создание соответствующей внутренней топологии для поддержки архивации (только в том случае, если не используется интеграция Microsoft Exchange для всех пользователей в развертывании)</strong></span><span class="sxs-lookup"><span data-stu-id="0feed-138"><strong>Create the appropriate internal topology to support archiving (only if not using Microsoft Exchange integration for all users in your deployment)</strong></span></span></p></td>
<td><p><span data-ttu-id="0feed-139">Запустите построитель топологии, чтобы добавить в топологию базы данных сервера Lync Server 2013 (базы данных SQL Server), а затем опубликуйте топологию.</span><span class="sxs-lookup"><span data-stu-id="0feed-139">Run Topology Builder to add Lync Server 2013 Archiving databases (SQL Server databases) to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="0feed-140">Чтобы определить топологию для включения архивированных баз данных, необходимо иметь учетную запись, которая является членом локальной группы "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="0feed-140">To define a topology to incorporate Archiving databases, an account that is a member of the local users group.</span></span></p>
<p><span data-ttu-id="0feed-141">Чтобы опубликовать топологию, учетную запись, которая входит в группу "Администраторы домена" и RTCUniversalServerAdmins, и у нее есть разрешения полного доступа (чтение/запись и изменение) в общей папке, которая будет использоваться для хранения файлов Lync Server 2013 (чтобы Topology Builder мог настроить нужные DACL).</span><span class="sxs-lookup"><span data-stu-id="0feed-141">To publish the topology, an account that is a member of the domain admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs).</span></span></p></td>
<td><p><span data-ttu-id="0feed-142"><a href="lync-server-2013-adding-archiving-databases-to-an-existing-lync-server-2013-deployment.md">Добавление баз данных архивации в существующий развертывание Lync Server 2013</a> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="0feed-142"><a href="lync-server-2013-adding-archiving-databases-to-an-existing-lync-server-2013-deployment.md">Adding Archiving databases to an existing Lync Server 2013 Deployment</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0feed-143"><strong>Настройка проверки подлинности "сервер-сервер" (только при использовании интеграции с Microsoft Exchange)</strong></span><span class="sxs-lookup"><span data-stu-id="0feed-143"><strong>Configure server-to-server authentication (only if using Microsoft Exchange integration)</strong></span></span></p></td>
<td><p><span data-ttu-id="0feed-144">Настройте серверы для включения проверки подлинности в Lync Server 2013 и Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0feed-144">Configure servers to enable authentication between Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="0feed-145">Для проверки подключения к хранилищу архивации Exchange рекомендуется запустить <strong>CsExchangeStorageConnectivity testuser_sipUri-Folder</strong> .</span><span class="sxs-lookup"><span data-stu-id="0feed-145">We recommend running <strong>Test-CsExchangeStorageConnectivity testuser_sipUri –Folder Dumpster</strong> to validate Exchange Archiving storage connectivity before enabling archiving.</span></span></p></td>
<td><p><span data-ttu-id="0feed-146">Учетная запись с соответствующими разрешениями для управления сертификатами на серверах.</span><span class="sxs-lookup"><span data-stu-id="0feed-146">An account with the appropriate permissions for managing certificates on the servers.</span></span></p></td>
<td><p><span data-ttu-id="0feed-147"><a href="lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md">Управление проверкой подлинности серверов (OAuth) и партнерских приложений в Lync server 2013</a> в документации по развертыванию или документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="0feed-147"><a href="lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md">Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013</a> in the Deployment documentation or the Operations documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feed-148"><strong>Настройка политик и конфигураций архивации</strong></span><span class="sxs-lookup"><span data-stu-id="0feed-148"><strong>Configure archiving policies and configurations</strong></span></span></p></td>
<td><p><span data-ttu-id="0feed-149">Настройте архивацию, в том числе сведения о том, следует ли использовать интеграцию с Microsoft Exchange, глобальную политику и политики сайтов и пользователей (если не используется интеграция Microsoft Exchange для хранения данных), а также специальные параметры архивации, такие как критический режим и экспорт данных и очистка.</span><span class="sxs-lookup"><span data-stu-id="0feed-149">Configure archiving, including whether to use Microsoft Exchange integration, the global policy and any site and user policies (when not using Microsoft Exchange integration for all data storage), and specific archiving options, such as critical mode and data export and purging.</span></span></p>
<p><span data-ttu-id="0feed-150">Если используется интеграция с Microsoft Exchange, настройте политики для Exchange In-Place, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="0feed-150">If using Microsoft Exchange integration, configure Exchange In-Place Hold policies as appropriate.</span></span></p></td>
<td><p><span data-ttu-id="0feed-151">Группа RTCUniversalServerAdmins (только Windows PowerShell) или назначение пользователям роли CSArchivingAdministrator или CSAdministrator.</span><span class="sxs-lookup"><span data-stu-id="0feed-151">RTCUniversalServerAdmins group (Windows PowerShell only) or assign users to the CSArchivingAdministrator or CSAdministrator role.</span></span></p></td>
<td><p><span data-ttu-id="0feed-152"><a href="lync-server-2013-configuring-support-for-archiving.md">Настройка поддержки архивации в Lync Server 2013</a> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="0feed-152"><a href="lync-server-2013-configuring-support-for-archiving.md">Configuring support for Archiving in Lync Server 2013</a> in the Deployment documentation.</span></span></p>
<p><span data-ttu-id="0feed-153">Документация по продукту Exchange (при использовании интеграции с Microsoft Exchange).</span><span class="sxs-lookup"><span data-stu-id="0feed-153">Exchange product documentation (if using Microsoft Exchange integration).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="deploying-lync-server-and-microsoft-exchange-in-different-forests"></a><span data-ttu-id="0feed-154">Развертывание Lync Server и Microsoft Exchange в разных лесах</span><span class="sxs-lookup"><span data-stu-id="0feed-154">Deploying Lync Server and Microsoft Exchange in Different Forests</span></span>

<span data-ttu-id="0feed-155">Если сервер Microsoft Exchange Server не развернут в том же лесу, что и Lync Server, необходимо убедиться, что указанные ниже атрибуты Exchange Active Directory синхронизированы с лесом, на котором развернут сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0feed-155">If Microsoft Exchange Server is not deployed in the same forest as Lync Server, you must make sure that the following Exchange Active Directory attributes are synchronized to the forest where Lync Server is deployed:</span></span>

1.  <span data-ttu-id="0feed-156">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="0feed-156">msExchUserHoldPolicies</span></span>

2.  <span data-ttu-id="0feed-157">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="0feed-157">proxyAddresses</span></span>

<span data-ttu-id="0feed-p107">Это атрибут со множеством значений. При его синхронизации необходимо объединить значения, а не заменить их, чтобы текущие значения не были потеряны.</span><span class="sxs-lookup"><span data-stu-id="0feed-p107">This is a multi-value attribute. When synchronizing this attribute, you need to merge the values, not replace them to ensure the existing values are not lost.</span></span>

<span data-ttu-id="0feed-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0feed-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

