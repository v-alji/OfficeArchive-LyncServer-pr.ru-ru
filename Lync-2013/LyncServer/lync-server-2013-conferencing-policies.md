---
title: 'Lync Server 2013: политики конференций'
description: 'Lync Server 2013: политики конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing policies
ms:assetid: 8f92eb7c-ee66-4df6-a726-4bff93b122cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688133(v=OCS.15)
ms:contentKeyID: 49733732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f117cfb077fc24c3e728e208d8bef78cd3284ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434314"
---
# <a name="conferencing-policies-in-lync-server-2013"></a><span data-ttu-id="47a02-103">Политики конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47a02-103">Conferencing policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47a02-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47a02-104">

<span> </span></span></span>

<span data-ttu-id="47a02-105">_**Тема последнего изменения:** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="47a02-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="47a02-106">Политика конференц-связи определяет возможности и возможности, которые пользователи смогут использовать во время конференции (также называемой собранием).</span><span class="sxs-lookup"><span data-stu-id="47a02-106">Conferencing policy defines the features and capabilities that users have available during a conference (also known as a meeting).</span></span> <span data-ttu-id="47a02-107">Настройки политики конференц-связи охватывают широкий спектр параметров расписания и участия, от возможности включения в собрание IP-аудио и видео, до максимального количества участников.</span><span class="sxs-lookup"><span data-stu-id="47a02-107">Conferencing policy settings encompass a wide variety of scheduling and participation options, ranging from whether a meeting can include IP audio and video to the maximum number of people who can attend.</span></span> <span data-ttu-id="47a02-108">Администраторы могут использовать политику конференций для управления безопасностью, пропускной способностью и юридическими аспектами собраний.</span><span class="sxs-lookup"><span data-stu-id="47a02-108">Administrators can use conferencing policy to manage security, bandwidth, and legal aspects of meetings.</span></span>

<span data-ttu-id="47a02-109">Политику конференц-связи можно определить на трех уровнях: в глобальной области действия, на уровне сайта и на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="47a02-109">You can define conferencing policy on three levels: global scope, site scope, and user scope.</span></span> <span data-ttu-id="47a02-110">Параметры применяются к конкретному пользователю от самой узкой до самой широкой области.</span><span class="sxs-lookup"><span data-stu-id="47a02-110">Settings apply to a specific user from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="47a02-111">При назначении пользователю политики пользователя эти параметры имеют приоритет.</span><span class="sxs-lookup"><span data-stu-id="47a02-111">If you assign a user policy to a user, those settings take precedence.</span></span> <span data-ttu-id="47a02-112">Если политика не назначена, применяется политика уровня сайта.</span><span class="sxs-lookup"><span data-stu-id="47a02-112">If you do not assign a user policy, site settings apply.</span></span> <span data-ttu-id="47a02-113">Если не применяется ни политика уровня пользователя, ни политика уровня сайта, то используется глобальная политика, которая определяет настройки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47a02-113">If no user or site policies apply, global policy provides the default settings.</span></span>

<span data-ttu-id="47a02-114">Глобальная политика существует по умолчанию, поэтому ее невозможно создать.</span><span class="sxs-lookup"><span data-stu-id="47a02-114">A global policy exists by default, so you cannot create a new global policy.</span></span> <span data-ttu-id="47a02-115">Существующую глобальную политику также нельзя удалить, однако ее можно изменить, чтобы настроить параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47a02-115">You also cannot delete the existing global policy, but you can change the existing global policy to customize your default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="47a02-116">Содержание</span><span class="sxs-lookup"><span data-stu-id="47a02-116">In This Section</span></span>

  - [<span data-ttu-id="47a02-117">Просмотр сведений о политике конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47a02-117">View conferencing policy information in Lync Server 2013</span></span>](lync-server-2013-view-conferencing-policy-information.md)

  - [<span data-ttu-id="47a02-118">Создание и изменение политики конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47a02-118">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)

  - [<span data-ttu-id="47a02-119">Удаление существующей политики конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47a02-119">Delete an existing conferencing policy in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-conferencing-policy.md)

  - [<span data-ttu-id="47a02-120">Справочник по параметрам политики конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47a02-120">Conferencing policy settings reference for Lync Server 2013</span></span>](lync-server-2013-conferencing-policy-settings-reference.md)

<span data-ttu-id="47a02-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47a02-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

