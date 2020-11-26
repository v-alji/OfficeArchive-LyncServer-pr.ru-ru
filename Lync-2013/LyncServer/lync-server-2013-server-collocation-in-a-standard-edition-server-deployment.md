---
title: Выровненное размещение серверов Lync Server 2013 в развертывании сервера Standard Edition
description: Размещение Lync Server 2013 на сервере в стандартном развертывании сервера выпусков.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server collocation in a Standard Edition server deployment
ms:assetid: 0763ffab-4fd6-463a-8e62-d97876b376d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398131(v=OCS.15)
ms:contentKeyID: 48183314
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af44761d36c472de1a3da5cd3b3938dc1a130836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441895"
---
# <a name="server-collocation-in-a-standard-edition-server-deployment-for-lync-server-2013"></a><span data-ttu-id="f954e-103">Выровненное размещение серверов в развертывании сервера Standard Edition для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f954e-103">Server collocation in a Standard Edition server deployment for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f954e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f954e-104">

<span> </span></span></span>

<span data-ttu-id="f954e-105">_**Тема последнего изменения:** 2013-01-20_</span><span class="sxs-lookup"><span data-stu-id="f954e-105">_**Topic Last Modified:** 2013-01-20_</span></span>

<span data-ttu-id="f954e-106">В этом разделе описаны роли сервера, базы данных и общие папки, которые можно отформатировать в развертывании сервера Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="f954e-106">This section describes the server roles, databases, and file shares that you can collocate in a Lync Server 2013 Standard Edition server deployment.</span></span>

<div>

## <a name="server-roles"></a><span data-ttu-id="f954e-107">Роли сервера</span><span class="sxs-lookup"><span data-stu-id="f954e-107">Server Roles</span></span>

<span data-ttu-id="f954e-108">В Lync Server 2013, служба конференц-связи, служба исправлений, мониторинг и архивация размещаются на сервере Standard Edition, но для их включения требуется дополнительная настройка.</span><span class="sxs-lookup"><span data-stu-id="f954e-108">In Lync Server 2013, A/V Conferencing service, Mediation service, Monitoring, and Archiving are collocated on the Standard Edition Server, but additional configuration is required to enable them.</span></span> <span data-ttu-id="f954e-109">Вы можете выбрать развертывание службы исправлений на отдельных серверах.</span><span class="sxs-lookup"><span data-stu-id="f954e-109">You can choose to deploy Mediation service on separate servers.</span></span>

<span data-ttu-id="f954e-110">Вы можете разпрограммировать доверенный сервер приложений с помощью стандартного сервера выпуска Standard.</span><span class="sxs-lookup"><span data-stu-id="f954e-110">You can collocate a trusted application server with a Standard Edition server.</span></span>

<span data-ttu-id="f954e-111">Следующие роли сервера должны развертываться на отдельном компьютере:</span><span class="sxs-lookup"><span data-stu-id="f954e-111">The following server roles must each be deployed on a separate computer:</span></span>

  - <span data-ttu-id="f954e-112">Директор</span><span class="sxs-lookup"><span data-stu-id="f954e-112">Director</span></span>

  - <span data-ttu-id="f954e-113">Пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="f954e-113">Edge Server</span></span>

  - <span data-ttu-id="f954e-114">Сервер-посредник (если он не размещен на сервере Standard Edition)</span><span class="sxs-lookup"><span data-stu-id="f954e-114">Mediation Server (if not collocated with the Standard Edition server)</span></span>

  - <span data-ttu-id="f954e-115">Сервер Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="f954e-115">Office Web Apps Server</span></span>

</div>

<div>

## <a name="databases"></a><span data-ttu-id="f954e-116">Базы данных</span><span class="sxs-lookup"><span data-stu-id="f954e-116">Databases</span></span>

<span data-ttu-id="f954e-117">По умолчанию серверная база данных SQL Server Express выровнена на сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="f954e-117">By default, the SQL Server Express back-end database is collocated on the Standard Edition server.</span></span> <span data-ttu-id="f954e-118">Вы не можете переместить его на отдельный компьютер.</span><span class="sxs-lookup"><span data-stu-id="f954e-118">You cannot move it to a separate computer.</span></span> <span data-ttu-id="f954e-119">С одним исключением нельзя выдавать общие базы данных на сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="f954e-119">With one exception, you cannot collocate other databases on the Standard Edition server.</span></span> <span data-ttu-id="f954e-120">Если вы решили развернуть сервер сохраняемого чата на сервере Standard Edition, вы можете разгруппировать базу данных сохраняемого чата и базу данных соответствия требованиям сохраняемого чата на одном стандартном сервере выпуске.</span><span class="sxs-lookup"><span data-stu-id="f954e-120">If you choose to deploy Persistent Chat Server on a Standard Edition server, you can collocate the Persistent chat database and the Persistent Chat Compliance database on the same Standard Edition server.</span></span>

<span data-ttu-id="f954e-121">Вы можете разадресовать каждую из следующих баз данных на одном сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="f954e-121">You can collocate each of the following databases on a single database server:</span></span>

  - <span data-ttu-id="f954e-122">база данных мониторинга;</span><span class="sxs-lookup"><span data-stu-id="f954e-122">Monitoring database</span></span>

  - <span data-ttu-id="f954e-123">база данных архивации;</span><span class="sxs-lookup"><span data-stu-id="f954e-123">Archiving database</span></span>

  - <span data-ttu-id="f954e-124">Серверная база данных для пула предварительных интерфейсов Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="f954e-124">A back-end database for an Enterprise Edition Front End pool</span></span>

<span data-ttu-id="f954e-125">Вы можете выделять любые из этих баз данных или любые из них в одном экземпляре SQL или использовать отдельные экземпляры SQL для каждого из них с указанными ниже ограничениями.</span><span class="sxs-lookup"><span data-stu-id="f954e-125">You can collocate any or any or all of these databases in a single SQL instance or use a separate SQL instances for each, with the following limitations:</span></span>

  - <span data-ttu-id="f954e-126">Каждый экземпляр SQL может содержать только одну серверную базу данных (для пула переднего плана Enterprise Edition), одну базу данных мониторинга, одну базу данных для архивации, единую базу данных чата и единую постоянную базу данных соответствия чатов.</span><span class="sxs-lookup"><span data-stu-id="f954e-126">Each SQL instance can contain only a single back-end database (for an Enterprise Edition Front End pool), single Monitoring database, single Archiving database, single persistent chat database, and single persistent chat compliance database.</span></span>

  - <span data-ttu-id="f954e-127">Сервер базы данных не может поддерживать более одного пула переднего плана выпуска Enterprise Edition, один сервер, на котором выполняется архивация, один сервер, на котором запущена функция "Мониторинг", единая база данных чата и единая сохраняемая база данных для проверки подлинности, но поддерживает один из них независимо от того, используют ли базы данных один экземпляр SQL Server или отдельные экземпляры SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f954e-127">The database server cannot support more than one Enterprise Edition Front End pool, one server running Archiving, one server running Monitoring, single Persistent Chat database, and single Persistent Chat compliance database, but it can support one of each, regardless of whether the databases use the same instance of SQL Server or separate instances of SQL Server.</span></span>

<span data-ttu-id="f954e-128">Вы можете предоставить общий доступ к файлам с помощью баз данных, как описано далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="f954e-128">You can collocate a file share with the databases, as described later in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f954e-129">В Lync Server 2013 имеется возможность интеграции наблюдения и архивации данных с хранилищем Exchange 2013 для некоторых или всех пользователей в развертывании.</span><span class="sxs-lookup"><span data-stu-id="f954e-129">In Lync Server 2013, you have the option of integrating Monitoring and Archiving storage with Exchange 2013 storage for some or all users in your deployment.</span></span> <span data-ttu-id="f954e-130">Вы не можете развернуть серверы, на которых запущен Lync Server или компоненты, на тех же серверах, что и в хранилище Exchange.</span><span class="sxs-lookup"><span data-stu-id="f954e-130">You cannot deploy any servers running Lync Server or components on the same servers as the Exchange storage.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f954e-131">Несмотря на то, что размещение баз данных поддерживается, размер баз данных может быстро увеличиваться.</span><span class="sxs-lookup"><span data-stu-id="f954e-131">Although collocation of databases is supported, the size of the databases can grow quickly.</span></span> <span data-ttu-id="f954e-132">Например, если вы рассматриваете различную базу данных архивации с другими базами данных, имейте в виду, что при архивации сообщений, которые не являются несколькими пользователями, объем дискового пространства, необходимого для базы данных архивации, может увеличиваться очень большим.</span><span class="sxs-lookup"><span data-stu-id="f954e-132">For example, when you consider collocating the Archiving database with other databases, be aware that if you are archiving the messages of more than a few users, the disk space needed by the Archiving database can grow very large.</span></span> <span data-ttu-id="f954e-133">По этой причине мы не рекомендуем выписывать несколько баз данных, особенно базу данных архивации, сохраняемый чат и сохраняемую базу данных соответствия чатов с серверной базой данных корпоративного пула.</span><span class="sxs-lookup"><span data-stu-id="f954e-133">For this reason, we do not recommend collocating multiple databases, especially the Archiving database, Persistent Chat database, and Persistent Chat compliance database with the back-end database of an Enterprise pool.</span></span>



</div>

</div>

<div>

## <a name="file-shares"></a><span data-ttu-id="f954e-134">Общие файлы</span><span class="sxs-lookup"><span data-stu-id="f954e-134">File Shares</span></span>

<span data-ttu-id="f954e-135">Общий файловый объект может быть размещен на отдельном сервере или может быть размещен на том же сервере, что и любые из указанных ниже элементов.</span><span class="sxs-lookup"><span data-stu-id="f954e-135">The file share can be a separate server or can be collocated on the same server as any or all of the following:</span></span>

  - <span data-ttu-id="f954e-136">сервер баз данных, в том числе тыловой сервер из интерфейсного пула Enterprise Edition;</span><span class="sxs-lookup"><span data-stu-id="f954e-136">Database server, including the Back End Server of an Enterprise Edition Front End pool</span></span>

  - <span data-ttu-id="f954e-137">база данных архивации;</span><span class="sxs-lookup"><span data-stu-id="f954e-137">Archiving database</span></span>

  - <span data-ttu-id="f954e-138">база данных мониторинга;</span><span class="sxs-lookup"><span data-stu-id="f954e-138">Monitoring database</span></span>

  - <span data-ttu-id="f954e-139">база данных сохраняемого чата;</span><span class="sxs-lookup"><span data-stu-id="f954e-139">Persistent Chat database</span></span>

  - <span data-ttu-id="f954e-140">база данных соответствия сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="f954e-140">Persistent Chat compliance database</span></span>

<span data-ttu-id="f954e-141">Один общий файловый объект может использоваться для нескольких пулов переднего плана, серверов Standard Edition (на одном сайте).</span><span class="sxs-lookup"><span data-stu-id="f954e-141">A single file share can be used for multiple Front End pools, Standard Edition servers (all in the same site).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f954e-142">В Lync Server 2013 для мониторинга и архивации используется общий доступ к файлам Lync Server в качестве сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="f954e-142">In Lync Server 2013, Monitoring and Archiving use the Lync Server file share as the Standard Edition server.</span></span>



</div>

</div>

<div>

## <a name="other-components"></a><span data-ttu-id="f954e-143">Другие компоненты</span><span class="sxs-lookup"><span data-stu-id="f954e-143">Other Components</span></span>

<span data-ttu-id="f954e-144">Вы не можете разадресовать обратный прокси-сервер, который не является компонентом Lync Server 2013, но является обязательным в развертывании, если вы хотите поддерживать общий доступ к веб-контенту для федеративных пользователей с любой ролью сервера Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f954e-144">You cannot collocate a reverse proxy server, which is not a Lync Server 2013 component, but is required in your deployment if you want to support sharing of web content for federated users with any Lync Server 2013 server role.</span></span> <span data-ttu-id="f954e-145">Однако вы можете реализовать обратную поддержку прокси-сервера для развертывания Lync Server 2013, настроив поддержку на существующем обратном прокси-сервере в Организации, который используется для других приложений.</span><span class="sxs-lookup"><span data-stu-id="f954e-145">You can, however, implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span>

<span data-ttu-id="f954e-146">Вы не можете разгруппировать любой компонент Exchange UM или компонент SharePoint с помощью любой роли Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f954e-146">You cannot collocate any Exchange UM component or SharePoint component with any Lync Server 2013 role.</span></span>

<span data-ttu-id="f954e-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f954e-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

