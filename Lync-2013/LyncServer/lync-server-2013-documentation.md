---
title: 'Lync Server 2013: Документация'
description: 'Lync Server 2013: документация.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Documentation
ms:assetid: 5a69c0a2-0986-49c3-809c-89bc175a34ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720335(v=OCS.15)
ms:contentKeyID: 63969609
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f128daa7941db8ae461b4bb12bcc9b97bbb5876e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397933"
---
# <a name="documentation-in-lync-server-2013"></a><span data-ttu-id="5f19d-103">Документация в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f19d-103">Documentation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f19d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f19d-104">

<span> </span></span></span>

<span data-ttu-id="5f19d-105">_**Тема последнего изменения:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="5f19d-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="5f19d-106">Модель MOF состоит из многочисленных функций управления службами.</span><span class="sxs-lookup"><span data-stu-id="5f19d-106">The MOF model is composed of many service management functions.</span></span> <span data-ttu-id="5f19d-107">Документация о том, как и когда выполняются задачи, может быть предоставлена участникам одной и той же команды или другим группам.</span><span class="sxs-lookup"><span data-stu-id="5f19d-107">Documentation about how and when tasks are performed can be shared with members of the same team or with other teams.</span></span> <span data-ttu-id="5f19d-108">Метод хранения и совместного использования документации может различаться в зависимости от типа функции.</span><span class="sxs-lookup"><span data-stu-id="5f19d-108">The method of storing and sharing documentation can vary according to the type of function.</span></span> <span data-ttu-id="5f19d-109">Например, процедуры для администрирования системы могут храниться в документах Word, так как они, скорее всего, будут напечатаны и часто встречаются в них.</span><span class="sxs-lookup"><span data-stu-id="5f19d-109">For example, the procedures for system administration may be stored as Word documents because they are likely to be printed and referenced frequently.</span></span> <span data-ttu-id="5f19d-110">Сведения об управлении конфигурацией могут автоматически создаваться и храниться в базе данных для упрощения поиска и индексирования.</span><span class="sxs-lookup"><span data-stu-id="5f19d-110">Configuration management information may be automatically generated and stored in a database for easy searching and indexing.</span></span> <span data-ttu-id="5f19d-111">Некоторые документы могут быть конфиденциальными и должны быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="5f19d-111">Some documentation may be sensitive and should be restricted.</span></span>

<div>

## <a name="document-management-systems"></a><span data-ttu-id="5f19d-112">Системы управления документами</span><span class="sxs-lookup"><span data-stu-id="5f19d-112">Document management systems</span></span>

<span data-ttu-id="5f19d-113">Система управления документами выступает в качестве центрального репозитория для документов и обеспечивает доступность только последней редакции документа.</span><span class="sxs-lookup"><span data-stu-id="5f19d-113">A documentation management system acts as a central repository for documents and helps ensure that only the latest revision of a document is available.</span></span> <span data-ttu-id="5f19d-114">Вы также можете заархивировать более старую версию документа, чтобы ознакомиться со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="5f19d-114">You can also consider archiving the older version of the document for reference.</span></span> <span data-ttu-id="5f19d-115">Lync Server предоставляет функциональные возможности, применимые к этой задаче.</span><span class="sxs-lookup"><span data-stu-id="5f19d-115">Lync Server provides functionality suitable to this task.</span></span>

</div>

<div>

## <a name="databases"></a><span data-ttu-id="5f19d-116">Базы данных</span><span class="sxs-lookup"><span data-stu-id="5f19d-116">Databases</span></span>

<span data-ttu-id="5f19d-117">Обсуждалось несколько средств и функций управления, которые подходят для работы с базами данных.</span><span class="sxs-lookup"><span data-stu-id="5f19d-117">Several tools and management functions were discussed that are suited to using databases.</span></span> <span data-ttu-id="5f19d-118">Процесс управления конфигурацией, как правило, использует автоматизированные процессы, которые хранят большие объемы данных, требующих индексирования и поиска.</span><span class="sxs-lookup"><span data-stu-id="5f19d-118">The configuration management process is likely to use automated processes that store large amounts of data that require indexing and searching.</span></span> <span data-ttu-id="5f19d-119">Специалисты службы поддержки могут найти в базе данных прошлые проблемы и разрешения при устранении неполадок с новыми проблемами.</span><span class="sxs-lookup"><span data-stu-id="5f19d-119">Support staff may search a database of past issues and resolutions when troubleshooting new issues.</span></span>

<span data-ttu-id="5f19d-120">Возможно, для разных целей используются разные базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f19d-120">It is likely that there will be different databases being used for different purposes.</span></span> <span data-ttu-id="5f19d-121">Определите, должны ли эти базы данных быть связаны или объединены.</span><span class="sxs-lookup"><span data-stu-id="5f19d-121">Decide if these databases should be linked or combined.</span></span> <span data-ttu-id="5f19d-122">Например, если служба обслуживания определяет некоторые проблемы с общей темой (например, новое программное обеспечение, вызывающее проблему с определенным сетевым адаптером), сотрудники службы поддержки могут запрашивать базу данных конфигурации, чтобы предсказать количество компьютеров, на которых может быть оказано влияние.</span><span class="sxs-lookup"><span data-stu-id="5f19d-122">For example, if the service desk identifies several issues with a common theme (such as new software causing an issue with a particular network adapter), the support staff can query the configuration database to predict how many computers might be affected.</span></span>

<span data-ttu-id="5f19d-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f19d-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

