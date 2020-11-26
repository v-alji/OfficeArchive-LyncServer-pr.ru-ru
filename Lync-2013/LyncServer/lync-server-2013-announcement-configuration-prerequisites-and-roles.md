---
title: 'Lync Server 2013: необходимые условия и роли для настройки объявлений'
description: 'Lync Server 2013: требования для настройки объявлений и роли.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439970"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a><span data-ttu-id="4dfe0-103">Необходимые условия и роли для настройки объявлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dfe0-103">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4dfe0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4dfe0-104">

<span> </span></span></span>

<span data-ttu-id="4dfe0-105">_**Тема последнего изменения:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="4dfe0-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="4dfe0-106">Объявление — это функция управления голосовым звонком в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-106">Announcement is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="4dfe0-107">В этой статье описаны действия, которые необходимо выполнить, прежде чем можно будет настроить объявление и назначения ролей, необходимые для выполнения задач настройки.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-107">This topic describes what you need to have in place before you can configure Announcement and the role assignments that you need to perform configuration tasks.</span></span>

<span data-ttu-id="4dfe0-108">В этом разделе предполагается, что вы прочитали документацию по планированию, относящуюся к объявлению (см. раздел [Планирование функций управления звонками в Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="4dfe0-108">This section assumes that you have read the planning documentation related to Announcement (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="announcement-configuration-prerequisites"></a><span data-ttu-id="4dfe0-109">Предварительные требования для конфигурации объявлений</span><span class="sxs-lookup"><span data-stu-id="4dfe0-109">Announcement Configuration Prerequisites</span></span>

<span data-ttu-id="4dfe0-110">Для приложения извещения необходимы следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="4dfe0-110">The Announcement application requires the following components:</span></span>

  - <span data-ttu-id="4dfe0-111">приложения</span><span class="sxs-lookup"><span data-stu-id="4dfe0-111">Application service</span></span>

  - <span data-ttu-id="4dfe0-112">"Группа ответа"</span><span class="sxs-lookup"><span data-stu-id="4dfe0-112">Response Group application</span></span>

  - <span data-ttu-id="4dfe0-113">Хранилище файлов, для хранения звуковых файлов</span><span class="sxs-lookup"><span data-stu-id="4dfe0-113">File Store, to hold audio files</span></span>

<span data-ttu-id="4dfe0-114">Все эти компоненты устанавливаются по умолчанию при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-114">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="announcement-configuration-roles"></a><span data-ttu-id="4dfe0-115">Роли конфигурации объявлений</span><span class="sxs-lookup"><span data-stu-id="4dfe0-115">Announcement Configuration Roles</span></span>

<span data-ttu-id="4dfe0-116">Для настройки объявлений можно использовать следующие средства администрирования:</span><span class="sxs-lookup"><span data-stu-id="4dfe0-116">You can use the following administrative tools to configure announcements:</span></span>

  - <span data-ttu-id="4dfe0-117">Панель управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="4dfe0-117">Lync Server Control Panel</span></span>

  - <span data-ttu-id="4dfe0-118">Командная консоль Lync Server</span><span class="sxs-lookup"><span data-stu-id="4dfe0-118">Lync Server Management Shell</span></span>

<span data-ttu-id="4dfe0-119">Для настройки приложения объявления требуется одна из следующих административных ролей:</span><span class="sxs-lookup"><span data-stu-id="4dfe0-119">Configuring Announcement application requires one of the following administrative roles:</span></span>

  - <span data-ttu-id="4dfe0-120">**CsVoiceAdministrator**   Эта роль администратора может создавать, настраивать и управлять всеми параметрами и политиками голосовой связи, включая параметры объявлений.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-120">**CsVoiceAdministrator**   This administrator role can create, configure, and manage all voice-related settings and policies, including Announcement settings.</span></span>

  - <span data-ttu-id="4dfe0-121">**CsServerAdministrator**   Эта роль администратора позволяет управлять серверами и службами и устранять неполадки с ними, а также настраивать все параметры объявлений.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-121">**CsServerAdministrator**   This administrator role can manage, monitor, and troubleshoot servers and services, and configure all Announcement settings.</span></span>

  - <span data-ttu-id="4dfe0-122">**CsAdministrator**   Эта роль администратора может выполнять все административные задачи и изменять все параметры.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-122">**CsAdministrator**   This administrator role can perform all administrative tasks and modify all settings.</span></span>

  - <span data-ttu-id="4dfe0-123">**CsViewOnlyAdministrator**   Эта роль администратора может просматривать развертывание для наблюдения за работоспособностью развертывания.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-123">**CsViewOnlyAdministrator**   This administrator role can view the deployment to monitor deployment health.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4dfe0-124">Подробнее об административных правах пользователей можно узнать в разделе <A href="lync-server-2013-planning-for-role-based-access-control.md">Планирование управления доступом на основе ролей в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="4dfe0-124">For details about administrative user rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4dfe0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4dfe0-125">See Also</span></span>


[<span data-ttu-id="4dfe0-126">Развертывание корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dfe0-126">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="4dfe0-127">Планирование функций управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dfe0-127">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="4dfe0-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4dfe0-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

