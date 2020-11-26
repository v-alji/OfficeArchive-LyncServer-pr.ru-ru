---
title: 'Lync Server 2013: обзор архивации'
description: 'Lync Server 2013: Общие сведения о том, как архивировать.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Archiving
ms:assetid: 1e3c2ef1-f561-4f57-8b6a-7d78addc1ed1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204729(v=OCS.15)
ms:contentKeyID: 48183570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 548d82d6731fd28fafbde5816a7a0dc77a1fcc02
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424830"
---
# <a name="overview-of-archiving-in-lync-server-2013"></a><span data-ttu-id="5b242-103">Обзор архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b242-103">Overview of Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b242-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b242-104">

<span> </span></span></span>

<span data-ttu-id="5b242-105">_**Тема последнего изменения:** 2013-09-30_</span><span class="sxs-lookup"><span data-stu-id="5b242-105">_**Topic Last Modified:** 2013-09-30_</span></span>

<span data-ttu-id="5b242-106">Архивация в Lync Server 2013 предоставляет способ архивации сообщений, отправленных с помощью Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b242-106">Archiving in Lync Server 2013 provides a way for you to archive communications that are sent through Lync Server 2013.</span></span>

<span data-ttu-id="5b242-107">Вы можете внедрить архивацию как часть первоначального развертывания Lync Server 2013 или добавить ее в существующее развертывание.</span><span class="sxs-lookup"><span data-stu-id="5b242-107">You can implement Archiving as part of your initial Lync Server 2013 deployment, or you can add it to an existing deployment.</span></span> <span data-ttu-id="5b242-108">Чтобы использовать базу данных архивации Lync Server 2013 (базы данных SQL Server) для хранения данных архивации, используйте Topology Builder, чтобы добавить базы данных в топологию, а затем опубликуйте топологию еще раз.</span><span class="sxs-lookup"><span data-stu-id="5b242-108">To use Lync Server 2013 Archiving databases (SQL Server databases) for storage of archiving data, you use Topology Builder to add the databases to your topology, and then publish the topology again.</span></span> <span data-ttu-id="5b242-109">Если все пользователи находятся в Exchange 2013 и почтовые ящики помещаются на In-Place удержание, вам не нужно обновлять топологию, но для того чтобы хранить архивированные данные в Exchange 2013, вам нужно будет только включить интеграцию с Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="5b242-109">If all your users are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, you do not have to update your topology, but only need to enable Microsoft Exchange integration to store archived data in Exchange 2013.</span></span>

<span data-ttu-id="5b242-110">При внедрении архива вы настраиваете его, чтобы указать, что заархивировано.</span><span class="sxs-lookup"><span data-stu-id="5b242-110">When you implement Archiving, you configure it to specify what is archived.</span></span> <span data-ttu-id="5b242-111">По умолчанию ничего не архивируется.</span><span class="sxs-lookup"><span data-stu-id="5b242-111">By default, nothing is archived.</span></span> <span data-ttu-id="5b242-112">Настраивать архивирование и управлять ими можно с помощью панели управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b242-112">You configure and manage Archiving by using Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="5b242-113">Вы можете реализовать архивацию для внутренней связи, внешней связи или и того, и для других.</span><span class="sxs-lookup"><span data-stu-id="5b242-113">You can implement Archiving for internal communications, external communications, or both.</span></span> <span data-ttu-id="5b242-114">Вы можете настроить параметры архивирования всей Организации и, при необходимости, для определенных сайтов, определенных пулов и определенных пользователей и групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="5b242-114">You can configure archiving settings your entire organization and, optionally, for specific sites, specific pools, and specific users and user groups.</span></span> <span data-ttu-id="5b242-115">Подробнее о том, как определить соответствующие параметры для Организации, можно найти [в разделе Определение требований для архивации в Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="5b242-115">For details about determining the appropriate options for your organization, see [Defining your requirements for Archiving in Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) in the Planning documentation.</span></span> <span data-ttu-id="5b242-116">Сведения о том, как выполняются политики архивирования и конфигурации, а также сведения о том, как [работает архивация в Lync Server 2013](lync-server-2013-how-archiving-works.md) , можно найти в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="5b242-116">For details about how Archiving policies and configurations are implemented, and details about what information can or cannot be archived, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<span data-ttu-id="5b242-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b242-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

