---
title: Настройка правил для личного идентификационного номера конференц-связи с телефонным подключением (PIN)
description: Настройка правил для личного идентификационного номера конференц-связи с телефонным подключением (PIN).
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing personal identification number (PIN) rules
ms:assetid: 27b79fb1-e2dc-4f71-bc82-b6eb61be2b16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520967(v=OCS.15)
ms:contentKeyID: 48183668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 799092ba57e9a85cd196840fc81c1f46b96e9900
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399913"
---
# <a name="configure-dial-in-conferencing-personal-identification-number-pin-rules-in-lync-server-2013"></a><span data-ttu-id="495f6-103">Настройка правил для личного идентификационного номера конференц-связи с телефонным подключением (PIN) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="495f6-103">Configure dial-in conferencing personal identification number (PIN) rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="495f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="495f6-104">

<span> </span></span></span>

<span data-ttu-id="495f6-105">_**Тема последнего изменения:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="495f6-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="495f6-106">Пользователи Lync Server 2013, у которых есть учетные данные доменных служб Active Directory (AD DS) в вашей организации, могут присоединяться к конференциям в сети для пользователей с проверкой подлинности, используя персональный идентификационный номер (ПИН-код).</span><span class="sxs-lookup"><span data-stu-id="495f6-106">Lync Server 2013 users who have Active Directory Domain Services (AD DS) credentials in your organization can join dial-in conferences as authenticated users by using a personal identification number (PIN).</span></span> <span data-ttu-id="495f6-107">Политика ПИН-кодов определяет способ работы ПИН-кодов для конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="495f6-107">PIN policy defines the rules for how dial-in conferencing PINs work.</span></span>

<span data-ttu-id="495f6-108">Чтобы применить особую политику к узлу или группе пользователей, вы можете создать новую политику ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="495f6-108">You can create a new PIN policy if you want a specific policy to apply to a site or to a certain group of users.</span></span> <span data-ttu-id="495f6-109">Если вы хотите применить одну и ту же политику ПИН-кодов ко всей организации, вы можете использовать глобальную политику ПИН-кодов, изменив ее так, как нужно.</span><span class="sxs-lookup"><span data-stu-id="495f6-109">If you want to use the same PIN policy for your entire organization, you can use the global PIN policy and modify it as needed.</span></span> <span data-ttu-id="495f6-110">Политики ПИН-кодов применяются к пользователям в очередности от самой узкой области действия до самой широкой.</span><span class="sxs-lookup"><span data-stu-id="495f6-110">PIN policies apply to users from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="495f6-111">Если вы назначили пользователю политику ПИН-кодов на уровне пользователя, ее параметры имеют приоритет.</span><span class="sxs-lookup"><span data-stu-id="495f6-111">If you assign a user-level PIN policy to a user, those settings take precedence.</span></span> <span data-ttu-id="495f6-112">Если вы не назначили политику пользователя, применяется политика ПИН-кодов на уровне узла, если она определена.</span><span class="sxs-lookup"><span data-stu-id="495f6-112">If you do not assign a user policy, the site-level PIN policy applies, if it exists.</span></span> <span data-ttu-id="495f6-113">Если политики пользователя и узла не назначены, действуют параметры по умолчанию глобальной политики ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="495f6-113">If no user or site policies apply, global PIN policy provides the default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="495f6-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="495f6-114">In This Section</span></span>

  - [<span data-ttu-id="495f6-115">Изменение параметров ПИН-кодов по умолчанию для конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="495f6-115">Modify the default dial-in conferencing PIN settings in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-dial-in-conferencing-pin-settings.md)

  - [<span data-ttu-id="495f6-116">оздание или изменение параметров ПИН-кода для конференц-связи с телефонным подключением в Lync Server 2013 для сайта или группы пользователей</span><span class="sxs-lookup"><span data-stu-id="495f6-116">Create or modify dial-in conferencing PIN settings in Lync Server 2013 for a site or group of users</span></span>](lync-server-2013-create-or-modify-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

  - [<span data-ttu-id="495f6-117">Удаление параметров контакта конференц-связи с телефонным подключением для сайта или группы пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="495f6-117">Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013</span></span>](lync-server-2013-delete-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

<span data-ttu-id="495f6-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="495f6-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

