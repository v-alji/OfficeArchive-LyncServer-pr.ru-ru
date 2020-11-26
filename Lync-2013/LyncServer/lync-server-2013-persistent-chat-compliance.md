---
title: 'Lync Server 2013: соблюдение норм в сохряняемом чате'
description: 'Lync Server 2013: соответствие сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat compliance
ms:assetid: 508933b6-bf17-4fb7-9147-f06ff6bc886f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204882(v=OCS.15)
ms:contentKeyID: 48184099
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4524ab38b5d7faa76123a156dd9b726f57ac6ed1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443183"
---
# <a name="persistent-chat-compliance-in-lync-server-2013"></a><span data-ttu-id="101ec-103">Соблюдение норм в сохряняемом чате в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="101ec-103">Persistent Chat compliance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="101ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="101ec-104">

<span> </span></span></span>

<span data-ttu-id="101ec-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="101ec-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="101ec-106">Создание новой конфигурации соответствия сохраняемым Чатам</span><span class="sxs-lookup"><span data-stu-id="101ec-106">To create a new Persistent Chat compliance configuration</span></span>

    New-CsPersistentChatComplianceConfiguration -Identity <XdsIdentity> [-AdapterName <String>] [-AdapterOutputDirectory <String>] [-AdapterType <String>] [-AddChatRoomDetails <$true | $false>] [-AddUserDetails <$true | $false>] [-Confirm [<Switch Parameter>]] [-CreateFileAttachmentsManifest <$true | $false>] [-CustomConfiguration <String>] [-Force <Switch Parameter>] [-InMemory <Switch Parameter>] [-OneChatRoomPerOutputFile <$true | $false>] [-RunInterval <TimeSpan>] [-WhatIf [<Switch Parameter>]]

<span data-ttu-id="101ec-107">Чтобы получить конфигурацию соответствия требованиям для сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="101ec-107">To get Persistent Chat compliance configuration</span></span>

    Get-CsPersistentChatComplianceConfiguration [-Identity <XdsIdentity>] [-LocalStore <Switch Parameter>]

<span data-ttu-id="101ec-108">Настройка конфигурации соответствия требованиям сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="101ec-108">To set Persistent Chat compliance configuration</span></span>

    Set-CsPersistentChatComplianceConfiguration -Identity <XdsIdentity> [-AdapterName <String>] [-AdapterOutputDirectory <String>] [-AdapterType <String>] [-AddChatRoomDetails <$true | $false>] [-AddUserDetails <$true | $false>] [-Confirm [<Switch Parameter>]] [-CreateFileAttachmentsManifest <$true | $false>] [-CustomConfiguration <String>] [-Force <Switch Parameter>] [-InMemory <Switch Parameter>] [-OneChatRoomPerOutputFile <$true | $false>] [-RunInterval <TimeSpan>] [-WhatIf [<Switch Parameter>]]

<span data-ttu-id="101ec-109">Удаление конфигурации соответствия требованиям сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="101ec-109">To remove Persistent Chat compliance configuration</span></span>

    Remove-CsPersistentChatComplianceConfiguration -Identity <XdsIdentity> [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

<span data-ttu-id="101ec-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="101ec-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

