---
title: 'Lync Server 2013: настройка конференц-связи с телефонным подключением'
description: 'Lync Server 2013: Настройка конференц-связи с телефонным подключением.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring dial-in conferencing
ms:assetid: 79a98c5d-a0a8-4729-828d-b9166842432c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398600(v=OCS.15)
ms:contentKeyID: 48184587
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9c3353caa1344b717b0f64c271149f078f194e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433208"
---
# <a name="configuring-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="22762-103">Настройка конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-103">Configuring dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22762-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22762-104">

<span> </span></span></span>

<span data-ttu-id="22762-105">_**Тема последнего изменения:** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="22762-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="22762-106">В этом разделе рассказывается, как настроить Конференц-связь с телефонным подключением в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="22762-106">This section guides you through the configuration of Lync Server 2013 dial-in conferencing.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="22762-107">Содержание</span><span class="sxs-lookup"><span data-stu-id="22762-107">In This Section</span></span>

  - [<span data-ttu-id="22762-108">Необходимые условия и разрешения для настройки конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-108">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-configuration-prerequisites-and-permissions.md)

  - [<span data-ttu-id="22762-109">Контрольный список развертывания для конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-109">Deployment checklist for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-dial-in-conferencing.md)

  - [<span data-ttu-id="22762-110">Настройка абонентских групп для конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-110">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)

  - [<span data-ttu-id="22762-111">Проверка абонентских планов Lync Server 2013 назначенные регионы</span><span class="sxs-lookup"><span data-stu-id="22762-111">Make sure dial plans Lync Server 2013 have assigned regions</span></span>](lync-server-2013-make-sure-dial-plans-have-assigned-regions.md)

  - [<span data-ttu-id="22762-112">Проверка параметров политики ПИН-кодов в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="22762-112">(Optional) Verify PIN policy settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-pin-policy-settings.md)

  - [<span data-ttu-id="22762-113">Настройка политики конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-113">Configure conferencing policy for dial-in in Lync Server 2013</span></span>](lync-server-2013-configure-conferencing-policy-for-dial-in.md)

  - [<span data-ttu-id="22762-114">Настройка номеров доступа для конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-114">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>](lync-server-2013-configure-dial-in-conferencing-access-numbers.md)

  - [<span data-ttu-id="22762-115">Проверка параметров конференц-связи с телефонным подключением в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="22762-115">(Optional) Verify dial-in conferencing settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing-settings.md)

  - [<span data-ttu-id="22762-116">Изменение назначенных клавиш для команд DTMF в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="22762-116">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</span></span>](lync-server-2013-optional-modify-key-mapping-for-dtmf-commands.md)

  - [<span data-ttu-id="22762-117">Включение и отключение объявлений о присоединении и выходе из конференции в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="22762-117">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>](lync-server-2013-optional-enable-and-disable-conference-join-and-leave-announcements.md)

  - [<span data-ttu-id="22762-118">Проверка конференц-связи с телефонным подключением в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="22762-118">(Optional) Verify dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing.md)

  - [<span data-ttu-id="22762-119">Развертывание надстройки собраний по сети для Lync 2013</span><span class="sxs-lookup"><span data-stu-id="22762-119">Deploy the Online Meeting Add-in for Lync 2013</span></span>](lync-server-2013-deploy-the-online-meeting-add-in-for-lync-2013.md)

  - [<span data-ttu-id="22762-120">Настройка параметров учетных записей пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-120">Configure user account settings in Lync Server 2013</span></span>](lync-server-2013-configure-user-account-settings.md)

  - [<span data-ttu-id="22762-121">(Recommended) Create Conference Directories</span><span class="sxs-lookup"><span data-stu-id="22762-121">(Recommended) Create Conference Directories</span></span>](recommended-create-conference-directories.md)

  - [<span data-ttu-id="22762-122">Приветствие пользователей в конференции с телефонным подключением Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="22762-122">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-welcome-users-to-dial-in-conferencing.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="22762-123">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="22762-123">Related Sections</span></span>

[<span data-ttu-id="22762-124">Развертывание Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22762-124">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)

<span data-ttu-id="22762-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22762-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

