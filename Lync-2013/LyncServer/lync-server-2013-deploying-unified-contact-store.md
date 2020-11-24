---
title: 'Lync Server 2013: развертывание единого хранилища контактов'
description: 'Lync Server 2013: развертывание единого хранилища контактов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying unified contact store
ms:assetid: 68959d58-ac8a-45de-afcd-b9de2c36799c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204963(v=OCS.15)
ms:contentKeyID: 48184373
ms.date: 06/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 056792d2e4ea66699b276d0d571e83c8a0256483
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398188"
---
# <a name="deploying-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="07780-103">Развертывание единого хранилища контактов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07780-103">Deploying unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07780-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07780-104">

<span> </span></span></span>

<span data-ttu-id="07780-105">_**Тема последнего изменения:** 2016-06-06_</span><span class="sxs-lookup"><span data-stu-id="07780-105">_**Topic Last Modified:** 2016-06-06_</span></span>

<span data-ttu-id="07780-106">Для включения единого магазина контактов в Lync Server 2013 не требуется никаких параметров топологии.</span><span class="sxs-lookup"><span data-stu-id="07780-106">Enabling unified contact store in Lync Server 2013 does not require any topology settings.</span></span> <span data-ttu-id="07780-107">Чтобы включить единое хранилище контактов для пользователей, необходимо следующее:</span><span class="sxs-lookup"><span data-stu-id="07780-107">Enabling unified contact store for users requires the following:</span></span>

  - <span data-ttu-id="07780-108">Включена политика единого магазина контактов (по умолчанию включена).</span><span class="sxs-lookup"><span data-stu-id="07780-108">Unified contact store policy is enabled (default is enabled).</span></span>

  - <span data-ttu-id="07780-109">Пользователи, которые входят в состав Lync 2013 хотя бы один раз.</span><span class="sxs-lookup"><span data-stu-id="07780-109">Users log in with Lync 2013 at least once.</span></span>

<span data-ttu-id="07780-110">После того как контакты пользователей будут перенесены, что происходит автоматически, когда пользователь входит в систему с помощью Lync 2013, пользователь может получить доступ к своим контактам Lync и управлять ими из Lync 2013, Outlook 2013 или Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="07780-110">After a user’s contacts have been migrated, which happens automatically when a user logs in with Lync 2013, the user can access and manage their Lync contacts from Lync 2013, Outlook 2013, or Outlook Web Access.</span></span> <span data-ttu-id="07780-111">Пользователю не нужно входить в Lync для управления контактами из Outlook или Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="07780-111">The user does not have to be logged in to Lync to manage their contacts from Outlook or Outlook Web Access.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="07780-112">Если пользователь входит в Lync 2010 после миграции, контакты и группы доступны и обновляются, но пользователи не могут управлять ими (то есть добавлять, удалять, перемещать, помечать, присвоенной или изменять).</span><span class="sxs-lookup"><span data-stu-id="07780-112">If a user logs in from Lync 2010 after migration, contacts and groups are available and up-to-date, but the user cannot manage (that is, add, delete, move, tag, untag, or modify) those contacts.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="07780-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="07780-113">In This Section</span></span>

  - [<span data-ttu-id="07780-114">Включение для пользователей единого хранилища контактов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07780-114">Enable users for unified contact store in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-unified-contact-store.md)

  - [<span data-ttu-id="07780-115">Перенос пользователей в единое хранилище контактов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07780-115">Migrate users to unified contact store in Lync Server 2013</span></span>](lync-server-2013-migrate-users-to-unified-contact-store.md)

  - [<span data-ttu-id="07780-116">Откат перенесенных пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07780-116">Roll back migrated users in Lync Server 2013</span></span>](lync-server-2013-roll-back-migrated-users.md)

<span data-ttu-id="07780-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07780-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

