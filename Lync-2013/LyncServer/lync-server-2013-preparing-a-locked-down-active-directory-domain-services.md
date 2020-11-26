---
title: 'Lync Server 2013: подготовка заблокированных доменных служб Active Directory'
description: 'Lync Server 2013: подготовка заблокированных доменных служб Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aea04b138de2630935713eda7cbef9e4d21572a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424228"
---
# <a name="preparing-a-locked-down-active-directory-domain-services-in-lync-server-2013"></a><span data-ttu-id="8567f-103">Подготовка заблокированных доменных служб Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8567f-103">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8567f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8567f-104">

<span> </span></span></span>

<span data-ttu-id="8567f-105">_**Тема последнего изменения:** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="8567f-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="8567f-106">Организации часто заблокировали доменные службы Active Directory, чтобы снизить риски безопасности.</span><span class="sxs-lookup"><span data-stu-id="8567f-106">Organizations often lock down Active Directory Domain Services to help mitigate security risks.</span></span> <span data-ttu-id="8567f-107">Однако заблокированная среда Active Directory может ограничивать разрешения, необходимые для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8567f-107">However, a locked-down Active Directory environment can limit the permissions that Lync Server 2013 requires.</span></span> <span data-ttu-id="8567f-108">Правильная подготовка заблокированной среды Active Directory для Lync Server 2013 включает некоторые дополнительные аспекты и инструкции.</span><span class="sxs-lookup"><span data-stu-id="8567f-108">Properly preparing a locked-down Active Directory environment for Lync Server 2013 involves some additional considerations and steps.</span></span>

<span data-ttu-id="8567f-109">Два распространенных способа ограничения разрешений в заблокированной среде Active Directory описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="8567f-109">Two common ways in which permissions are limited in a locked-down Active Directory environment are as follows:</span></span>

  - <span data-ttu-id="8567f-110">Элементы управления доступом пользователей, прошедшие проверку подлинности, удаляются из контейнеров.</span><span class="sxs-lookup"><span data-stu-id="8567f-110">Authenticated user access control entries (ACEs) are removed from containers.</span></span>

  - <span data-ttu-id="8567f-111">Наследование разрешений отключено для контейнеров пользователей, контактов, InetOrgPerson или объектов компьютера.</span><span class="sxs-lookup"><span data-stu-id="8567f-111">Permissions inheritance is disabled on containers of User, Contact, InetOrgPerson, or Computer objects.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8567f-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="8567f-112">In This Section</span></span>

  - [<span data-ttu-id="8567f-113">Удаление разрешений пользователей, прошедших проверку подлинности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8567f-113">Authenticated user permissions are removed in Lync Server 2013</span></span>](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [<span data-ttu-id="8567f-114">Заблокировано наследование разрешений для компьютеров, пользователей и контейнеров inetOrgPerson в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8567f-114">Permissions inheritance Is disabled on computers, users, or InetOrgPerson containers in Lync Server 2013</span></span>](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

<span data-ttu-id="8567f-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8567f-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

