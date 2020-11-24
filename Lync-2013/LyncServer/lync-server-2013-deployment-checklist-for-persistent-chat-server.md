---
title: 'Lync Server 2013: контрольный список развертывания для сервера сохраняемого чата'
description: 'Lync Server 2013: контрольный список развертывания для сохраняемого сервера чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for Persistent Chat Server
ms:assetid: b1108f8f-88a2-4660-8086-d25ba76f7239
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412851(v=OCS.15)
ms:contentKeyID: 48185155
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28d96da5e2961634e6a81450796e5d1ae3426819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399139"
---
# <a name="deployment-checklist-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="17dba-103">Контрольный список развертывания для сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17dba-103">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17dba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17dba-104">

<span> </span></span></span>

<span data-ttu-id="17dba-105">_**Тема последнего изменения:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="17dba-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="17dba-106">Развертывание Lync Server 2013, сервер сохраняемого чата требует его развертывания в правильной последовательности, и вы закончите все необходимые шаги по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="17dba-106">Deployment of Lync Server 2013, Persistent Chat Server requires that you deploy it in the correct sequence and that you complete all required deployment steps.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="17dba-107">Последовательность развертывания</span><span class="sxs-lookup"><span data-stu-id="17dba-107">Deployment Sequence</span></span>

<span data-ttu-id="17dba-108">Вы можете развернуть сохраняемый сервер чата после развертывания начальной топологии, включая хотя бы один сервер Lync Server 2013, пул переднего плана или один сервер Lync Server 2013, Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="17dba-108">You can deploy Persistent Chat Server after you deploy your initial topology, including at least one Lync Server 2013, Front End pool or one Lync Server 2013, Standard Edition server.</span></span> <span data-ttu-id="17dba-109">В этой статье описано, как развернуть сервер сохраняемого чата, добавив его в существующее развертывание.</span><span class="sxs-lookup"><span data-stu-id="17dba-109">This topic describes how to deploy Persistent Chat Server by adding it to an existing deployment.</span></span>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="17dba-110">Процесс развертывания</span><span class="sxs-lookup"><span data-stu-id="17dba-110">Deployment Process</span></span>

<span data-ttu-id="17dba-111">В следующей таблице перечислены основные шаги по развертыванию сервера сохраняемого чата и приведены ссылки на дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="17dba-111">The following table lists the basic steps to deploy Persistent Chat Server and provides links for more details.</span></span>

### <a name="persistent-chat-server-deployment-process"></a><span data-ttu-id="17dba-112">Процесс развертывания сервера "сохраняемый чат"</span><span class="sxs-lookup"><span data-stu-id="17dba-112">Persistent Chat Server Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17dba-113">Задача</span><span class="sxs-lookup"><span data-stu-id="17dba-113">Task</span></span></th>
<th><span data-ttu-id="17dba-114">Шаги</span><span class="sxs-lookup"><span data-stu-id="17dba-114">Steps</span></span></th>
<th><span data-ttu-id="17dba-115">Требуемые роли и членство в группах</span><span class="sxs-lookup"><span data-stu-id="17dba-115">Required roles and group memberships</span></span></th>
<th><span data-ttu-id="17dba-116">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="17dba-116">Related topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17dba-117"><strong>Установка необходимого оборудования и программного обеспечения</strong></span><span class="sxs-lookup"><span data-stu-id="17dba-117"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="17dba-118">На оборудовании, удовлетворяющем требованиям, установите следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="17dba-118">On hardware that meets system requirements, install the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="17dba-119">На серверах клиентского доступа на постоянной стороне сервера:</span><span class="sxs-lookup"><span data-stu-id="17dba-119">On the Persistent Chat Server Front End Servers:</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="17dba-120">Операционная система, соответствующая требованиям</span><span class="sxs-lookup"><span data-stu-id="17dba-120">An operating system that meets system requirements</span></span></p></li>
<li><p><span data-ttu-id="17dba-121">Требования к программному обеспечению для компьютеров с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17dba-121">Software prerequisites for computers running Lync Server 2013</span></span></p></li>
<li><p><span data-ttu-id="17dba-122">Сервер SQL Server, на котором будет размещаться база данных сервера сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="17dba-122">SQL Server on the server that will host Persistent Chat Server database</span></span></p></li>
</ul>
<p><span data-ttu-id="17dba-123">Если требуется соответствие требованиям сервера сохраняемого чата, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="17dba-123">If Persistent Chat Server compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="17dba-124">Сервер SQL Server, на котором будет размещаться база данных соответствия требованиям сервера для обеспечения постоянной связи</span><span class="sxs-lookup"><span data-stu-id="17dba-124">SQL Server on the server that will host Persistent Chat Server compliance database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="17dba-125">Любой пользователь, являющийся членом локальной группы "Администраторы"</span><span class="sxs-lookup"><span data-stu-id="17dba-125">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="17dba-126"><a href="lync-server-2013-supported-hardware.md">Поддерживаемое оборудование для Lync Server 2013</a> в документации по поддержке</span><span class="sxs-lookup"><span data-stu-id="17dba-126"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="17dba-127"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Поддержка серверного программного обеспечения и инфраструктуры в Lync Server 2013</a> в документации по поддержке</span><span class="sxs-lookup"><span data-stu-id="17dba-127"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="17dba-128"><a href="lync-server-2013-determining-your-system-requirements.md">Определение требований к системе для Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="17dba-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="17dba-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Технические требования для постоянного сервера чата в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="17dba-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Technical requirements for Persistent Chat Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17dba-130"><strong>Создание соответствующей внутренней топологии для поддержки сохраняемого сервера чатов (и, при необходимости, сохранение соответствия в сохраняемом чате)</strong></span><span class="sxs-lookup"><span data-stu-id="17dba-130"><strong>Create the appropriate internal topology to support Persistent Chat Server (and optionally, Persistent Chat compliance)</strong></span></span></p></td>
<td><p><span data-ttu-id="17dba-131">Запустите построитель топологии, чтобы добавить в топологию пул серверов сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="17dba-131">Run Topology Builder to add a Persistent Chat Server pool to your topology:</span></span></p>
<ul>
<li><p><span data-ttu-id="17dba-132">Добавление серверных компонентов для временного чата в топологию</span><span class="sxs-lookup"><span data-stu-id="17dba-132">Add Persistent Chat Server components to the topology</span></span></p></li>
<li><p><span data-ttu-id="17dba-133">Создание базы данных SQL Server для сохраняемого хранилища сервера чатов (и резервного сервера SQL Server для восстановления с аварийным восстановлением)</span><span class="sxs-lookup"><span data-stu-id="17dba-133">Create a SQL Server database for the Persistent Chat Server store (and a backup SQL Server for disaster recovery)</span></span></p></li>
<li><p><span data-ttu-id="17dba-134">Определение нового хранилища файлов Lync или использование существующего хранилища файлов Lync для файлов сервера чатов</span><span class="sxs-lookup"><span data-stu-id="17dba-134">Define a new Lync File Store or use an existing Lync File Store for Persistent Chat Server files</span></span></p></li>
<li><p><span data-ttu-id="17dba-135">Свяжите пул Lync Server 2013, который может перенаправлять запросы на этот пул серверов сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="17dba-135">Associate the Lync Server 2013 pool that can route requests to this Persistent Chat Server pool</span></span></p></li>
</ul>
<p><span data-ttu-id="17dba-136">Если требуется соответствие с сохраняемым чатом:</span><span class="sxs-lookup"><span data-stu-id="17dba-136">If Persistent Chat compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="17dba-137">Добавление магазина "соответствие требованиям" для сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="17dba-137">Add Persistent Chat Compliance Store</span></span></p></li>
<li><p><span data-ttu-id="17dba-138">Чтобы включить соответствие требованиям, установите флажок "Определение пула серверов для постоянного чата".</span><span class="sxs-lookup"><span data-stu-id="17dba-138">Click the Persistent Chat Server pool definition check box for enabling compliance</span></span></p></li>
<li><p><span data-ttu-id="17dba-139">Публикация топологии</span><span class="sxs-lookup"><span data-stu-id="17dba-139">Publish the topology</span></span></p></li>
</ul>
<p><span data-ttu-id="17dba-140">Если вы установили сервер сохраняемого чата в стандартном выпуске, полное доменное имя (FQDN) пула сервера сохраняемого чата должно соответствовать стандартному серверу выпуска, а базы данных SQL Server — на экземпляре SQL Server Express на сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="17dba-140">If you install Persistent Chat Server on Standard Edition, the fully qualified domain name (FQDN) of the Persistent Chat Server pool must match the Standard Edition server, and the SQL Server databases are collocated on the SQL Server Express instance on the Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="17dba-141">Для определения топологии требуется учетная запись члена локальной группы "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="17dba-141">To define a topology, an account that is a member of the local Users group.</span></span></p>
<p><span data-ttu-id="17dba-142">Чтобы опубликовать топологию, учетную запись, которая входит в группу "Администраторы домена" и группу RTCUniversalServerAdmins, и пользователю также будут доступны разрешения на полный доступ (чтение/запись и изменение) в хранилище файлов Lync для файлов сервера чатов (чтобы Topology Builder мог настроить нужные DACL).</span><span class="sxs-lookup"><span data-stu-id="17dba-142">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and the user should also have full control permissions (read/write/modify) on the Lync File Store for Persistent Chat Server files (so that Topology Builder can configure the required DACLs).</span></span></p></td>
<td><p><span data-ttu-id="17dba-143"><a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Добавление постоянного сервера чата в развертывание в Lync Server 2013</a> в документации по развертыванию</span><span class="sxs-lookup"><span data-stu-id="17dba-143"><a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17dba-144"><strong>Развертывание сервера сохраняемого чата</strong></span><span class="sxs-lookup"><span data-stu-id="17dba-144"><strong>Deploy Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="17dba-145">Запустите настройку Lync Server на всех компьютерах, на которых запущен сервер сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="17dba-145">Run the Lync Server setup on all the computers running Persistent Chat Server.</span></span> <span data-ttu-id="17dba-146">Настройка сервера "сохраняемый чат" интегрирована в мастер развертывания Lync Server 2013, который содержит указанные ниже инструкции.</span><span class="sxs-lookup"><span data-stu-id="17dba-146">The Persistent Chat Server setup is integrated into the Lync Server 2013 Deployment wizard that provides the following instructions:</span></span></p>
<ul>
<li><p><span data-ttu-id="17dba-147">Развертывание локального хранилища управления</span><span class="sxs-lookup"><span data-stu-id="17dba-147">Deploy local management store</span></span></p></li>
<li><p><span data-ttu-id="17dba-148">Установка серверных служб сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="17dba-148">Install Persistent Chat Server services</span></span></p></li>
<li><p><span data-ttu-id="17dba-149">Запрос и назначение сертификатов</span><span class="sxs-lookup"><span data-stu-id="17dba-149">Request and assign certificates</span></span></p></li>
<li><p><span data-ttu-id="17dba-150">Запуск и выполнение служб</span><span class="sxs-lookup"><span data-stu-id="17dba-150">Run and start the services</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="17dba-151">Любой пользователь, являющийся членом локальной группы "Администраторы"</span><span class="sxs-lookup"><span data-stu-id="17dba-151">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="17dba-152"><a href="lync-server-2013-deploying-persistent-chat-server.md">Развертывание постоянного сервера чата в Lync server 2013</a> в документации по развертыванию</span><span class="sxs-lookup"><span data-stu-id="17dba-152"><a href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17dba-153"><strong>Создание администратора сохраняемого чата</strong></span><span class="sxs-lookup"><span data-stu-id="17dba-153"><strong>Create a Persistent Chat administrator</strong></span></span></p></td>
<td><p><span data-ttu-id="17dba-154">Добавьте пользователей в группу безопасности CsPersistentChatAdministrator.</span><span class="sxs-lookup"><span data-stu-id="17dba-154">Add users to the CsPersistentChatAdministrator security group.</span></span></p></td>
<td><p><span data-ttu-id="17dba-155">Любой пользователь, являющийся членом группы "Администраторы домена"</span><span class="sxs-lookup"><span data-stu-id="17dba-155">Any user who is a member of domain administrators.</span></span></p></td>
<td><p><span data-ttu-id="17dba-156"><a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Добавление постоянного администратора чата в Lync Server 2013</a> в документации по развертыванию</span><span class="sxs-lookup"><span data-stu-id="17dba-156"><a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Adding a Persistent Chat administrator in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17dba-157"><strong>Настройка сервера сохраняемого сеанса беседы</strong></span><span class="sxs-lookup"><span data-stu-id="17dba-157"><strong>Configure Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="17dba-158">Настройте пользователей:</span><span class="sxs-lookup"><span data-stu-id="17dba-158">Configure users:</span></span></p>
<ul>
<li><p><span data-ttu-id="17dba-159">Для доступа к сохраняемому серверу чата политика должна быть включена пользователем.</span><span class="sxs-lookup"><span data-stu-id="17dba-159">User has to be enabled by policy to access Persistent Chat Server.</span></span> <span data-ttu-id="17dba-160">По умолчанию политика отключена для всех пользователей и может быть определена в области Global/site/Pool/User.</span><span class="sxs-lookup"><span data-stu-id="17dba-160">By default, the policy is turned off for all users and can be defined at global/site/pool/user scopes.</span></span></p></li>
<li><p><span data-ttu-id="17dba-161">Настройка параметров</span><span class="sxs-lookup"><span data-stu-id="17dba-161">Configure settings</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="17dba-p104">Пользователь должен быть членом группы CsPersistentChatAdministrator. Для изменения политики пользователь должен быть членом группы CsUserAdministrator (или группы с более высоким уровнем прав).</span><span class="sxs-lookup"><span data-stu-id="17dba-p104">User must be a member of CsPersistentChatAdministrator. To change policy, user must be in CsUserAdministrator, at a minimum.</span></span></p></td>
<td><p><span data-ttu-id="17dba-164"><a href="lync-server-2013-configuring-persistent-chat-server.md">Настройка сервера сохраняемого чата в Lync server 2013</a> в документации по развертыванию</span><span class="sxs-lookup"><span data-stu-id="17dba-164"><a href="lync-server-2013-configuring-persistent-chat-server.md">Configuring Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="17dba-165">Вы можете развернуть один или несколько пулов серверов для постоянного чата.</span><span class="sxs-lookup"><span data-stu-id="17dba-165">You can deploy one or more Persistent Chat Server pools.</span></span> <span data-ttu-id="17dba-166">Для обеспечения соответствия нормативным требованиям Корпорация Майкрософт поддерживает несколько пулов серверов постоянного чата, поскольку данные, созданные в данной стране, должны оставаться в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="17dba-166">We support multiple Persistent Chat Server pools for regulatory reasons whereby data generated in a given region is required to stay in that region.</span></span> <span data-ttu-id="17dba-167">Например, если вы разворачиваете пул серверов сохраняемого чата в Чикаго, а другой в Zurich для обеспечения соответствия требованиям к данным в Швейцарии, пользователи могут подключаться к комнатам как в случае, так и в пулах сервера сохраняемого чата, при условии, что они имеют доступ.</span><span class="sxs-lookup"><span data-stu-id="17dba-167">For example, if you deploy a Persistent Chat Server pool in Chicago, and another in Zurich to comply with regulations for data in Switzerland, users can connect to rooms in both the Persistent Chat Server pools, provided they have access.</span></span>



<span data-ttu-id="17dba-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17dba-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

