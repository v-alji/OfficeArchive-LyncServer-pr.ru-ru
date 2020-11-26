---
title: Управление категориями
description: Управление категориями.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Manage categories
ms:assetid: 1b118d91-b4c4-4b2f-b842-b451417ec2c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204719(v=OCS.15)
ms:contentKeyID: 48183543
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf335b96c455647ebeb665364944e15d2e463fbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446964"
---
# <a name="manage-categories"></a><span data-ttu-id="7549f-103">Manage categories</span><span class="sxs-lookup"><span data-stu-id="7549f-103">Manage categories</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7549f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7549f-104">

<span> </span></span></span>

<span data-ttu-id="7549f-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="7549f-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="7549f-106">Создание новой категории сервера для сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="7549f-106">To create a new Persistent Chat Server Category</span></span>

    New-CsPersistentChatCategory -Name Foo -PersistentChatPoolFqdn client.contoso1b118d91-b4c4-4b2f-b842-b451417ec2c6.com [other parameters]

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7549f-107">PersistentChatPoolFqdn необходим только в том случае, если существует несколько пулов серверов сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="7549f-107">PersistentChatPoolFqdn is needed only if there is more than one Persistent Chat Server pool.</span></span>



</div>

<span data-ttu-id="7549f-108">Чтобы внести изменения в существующую категорию сервера сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="7549f-108">To make changes to existing Persistent Chat Server Category</span></span>

    Set-CsPersistentChatCategory -Identity testCat -AllowedMembers @{Add="sip:user1@contoso.com", "CN=container,DC=contoso,DC=com"}  -DeniedMembers @{Add="sip:user2@contoso.com"}
    Set-CsPersistentChatCategory -Identity testCat -Creators @{Add="sip:user1@contoso.com"}

<span data-ttu-id="7549f-109">Windows PowerShell: AllowedMembers, DeniedMembers и Creators могут быть установлены одновременно.</span><span class="sxs-lookup"><span data-stu-id="7549f-109">Windows PowerShell: AllowedMembers, DeniedMembers, and Creators can be set simultaneously.</span></span> <span data-ttu-id="7549f-110">Создатели должны быть подмножеством AllowedMembers за вычетом DeniedMembers.</span><span class="sxs-lookup"><span data-stu-id="7549f-110">Creators should be the subset of AllowedMembers minus DeniedMembers.</span></span> <span data-ttu-id="7549f-111">Вы также можете задать свойства категории одновременно с членами и авторами.</span><span class="sxs-lookup"><span data-stu-id="7549f-111">You can also set the properties of a category at the same time as the members and creators.</span></span>

<div>

## <a name="create-get-set-or-remove-a-category"></a><span data-ttu-id="7549f-112">Создание, получение, задание и удаление категории</span><span class="sxs-lookup"><span data-stu-id="7549f-112">Create, Get, Set, or Remove a Category</span></span>

<span data-ttu-id="7549f-113">Создание новой категории</span><span class="sxs-lookup"><span data-stu-id="7549f-113">To create a new Category</span></span>

    New-CsPersistentChatCategory -Name <String> [-PersistentChatPoolFqdn <String>] [-Description <String>] [-EnableInvitations<Switch Parameter>] [-EnableFileUpload <Switch Parameter>] [-RemoveChatHistory <Switch Parameter>] [-MaxContentSize <Integer>]

<span data-ttu-id="7549f-114">Получение категории</span><span class="sxs-lookup"><span data-stu-id="7549f-114">To get a Category</span></span>

    Get-CsPersistentChatCategory -Identity <String>

<span data-ttu-id="7549f-115">или</span><span class="sxs-lookup"><span data-stu-id="7549f-115">or</span></span>

    Get-CsPersistentChatCategory -PersistentChatPoolFqdn <String>

<span data-ttu-id="7549f-116">Настройка категории</span><span class="sxs-lookup"><span data-stu-id="7549f-116">To set a Category</span></span>

    Set-CsPersistentChatCategory -Instance <CategoryObject> [-WhatIf] [-Confirm] [<CommonParameters>]

<span data-ttu-id="7549f-117">или</span><span class="sxs-lookup"><span data-stu-id="7549f-117">or</span></span>

    Set-CsPersistentChatCategory [-Identity] <string> [-Name <string>] [-Description <string>] [-Invitations <bool>] [-FileUpload <bool>] [-ChatHistory <bool>] [-AllowedMembers <PSListModifier[string]>] [-DeniedMembers <PSListModifier[string]>] [-Creators <PSListModifier[string]>] [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="7549f-118">Удаление категории</span><span class="sxs-lookup"><span data-stu-id="7549f-118">To remove a Category</span></span>

    Remove-CsPersistentChatCategory -Instance <CategoryObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="7549f-119">или</span><span class="sxs-lookup"><span data-stu-id="7549f-119">or</span></span>

    Remove-CsPersistentChatCategory -Identity <String> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="7549f-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7549f-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

