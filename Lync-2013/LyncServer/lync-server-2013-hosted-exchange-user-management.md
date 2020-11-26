---
title: 'Lync Server 2013: управление пользователями размещенной системы Exchange'
description: 'Lync Server 2013: управление размещенными пользователями Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange user management
ms:assetid: e8723af5-0604-4d7d-bad2-463a9832efb4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399037(v=OCS.15)
ms:contentKeyID: 48185887
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ceda9352fc627fc7b762b5995d788ffafa159ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427525"
---
# <a name="hosted-exchange-user-management-in-lync-server-2013"></a><span data-ttu-id="7ba00-103">Управление пользователями размещенной системы Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ba00-103">Hosted Exchange user management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ba00-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ba00-104">

<span> </span></span></span>

<span data-ttu-id="7ba00-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="7ba00-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="7ba00-106">Чтобы предоставить услуги голосовой почты для пользователей Lync Server 2013, чьи почтовые ящики находятся на размещенной службе Exchange, необходимо включить учетные записи пользователей для размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="7ba00-106">To provide voice mail services for Lync Server 2013 users whose mailboxes are located on a hosted Exchange service, you must enable their user accounts for hosted voice mail.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7ba00-107">Прежде чем пользователи Lync Server 2013 могут быть включены для поддержки размещенной голосовой почты, необходимо развернуть политику размещенной голосовой почты, которая применяется к соответствующей учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ba00-107">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to the corresponding user account must be deployed.</span></span> <span data-ttu-id="7ba00-108">Политика может быть глобальной, сайтовой или для пользователя в области действия, если она применяется к пользователю, который вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="7ba00-108">The policy can be global, site, or per-user in scope, as long as it applies to the user whom you want to enable.</span></span> <span data-ttu-id="7ba00-109">Подробнее смотрите в разделе <A href="lync-server-2013-hosted-voice-mail-policies.md">политики размещенной голосовой почты в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7ba00-109">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="the-msexchucvoicemailsettings-attribute"></a><span data-ttu-id="7ba00-110">Атрибут msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="7ba00-110">The msExchUCVoiceMailSettings Attribute</span></span>

<span data-ttu-id="7ba00-111">Lync Server 2013 представляет новый пользовательский атрибут с именем **msExchUCVoiceMailSettings**, который создается в рамках подготовки схемы Active Directory для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ba00-111">Lync Server 2013 introduces a new user attribute named **msExchUCVoiceMailSettings**, which is created as part of the Lync Server 2013 Active Directory schema preparation.</span></span> <span data-ttu-id="7ba00-112">Этот многозначный атрибут содержит параметры голосовой почты, которые являются общими для Lync Server 2013 и размещенной службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ba00-112">This multivalued attribute holds voice mail settings that are shared by Lync Server 2013 and the hosted Exchange service.</span></span>

<span data-ttu-id="7ba00-113">В некоторых случаях размещенной службе Exchange может быть задано значение атрибута msExchUCVoiceMailSettings в процессе включения UM-среды Exchange или в процессе переноса почтовых ящиков на размещенный сервер Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ba00-113">The hosted Exchange service may in some cases set the value of the msExchUCVoiceMailSettings attribute in the process of enabling Exchange UM, or during the process of transferring mailboxes to a hosted Exchange Server.</span></span> <span data-ttu-id="7ba00-114">Если этот атрибут не задан Exchange, администратор Lync Server 2013 должен настроить его, выполнив командлет Set-CsUser, как описано ранее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="7ba00-114">If this attribute is not set by Exchange, the Lync Server 2013 administrator must set it by running the Set-CsUser cmdlet, as described earlier in this topic.</span></span>

<span data-ttu-id="7ba00-115">В приведенной ниже таблице указаны пары "ключ-значение" для атрибута и их авторы.</span><span class="sxs-lookup"><span data-stu-id="7ba00-115">The attribute’s key/value pairs and their authors are shown in the following table.</span></span>

### <a name="the-msexchucvoicemailsettings-attribute-keyvalue-pairs"></a><span data-ttu-id="7ba00-116">Пары ключей и значений в атрибуте msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="7ba00-116">The msExchUCVoiceMailSettings Attribute Key/Value Pairs</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ba00-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7ba00-117">Value</span></span></th>
<th><span data-ttu-id="7ba00-118">Созданные</span><span class="sxs-lookup"><span data-stu-id="7ba00-118">Author</span></span></th>
<th><span data-ttu-id="7ba00-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7ba00-119">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ba00-120">ExchangeHostedVoiceMail = 1</span><span class="sxs-lookup"><span data-stu-id="7ba00-120">ExchangeHostedVoiceMail=1</span></span></p></td>
<td><p><span data-ttu-id="7ba00-121">Exchange</span><span class="sxs-lookup"><span data-stu-id="7ba00-121">Exchange</span></span></p></td>
<td><p><span data-ttu-id="7ba00-122">Для пользователя разрешен доступ к размещенной единой системе обмена сообщениями через Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7ba00-122">User has been enabled for hosted UM access by Exchange Server.</span></span> <span data-ttu-id="7ba00-123">Приложение маршрутизации UM Exchange будет проверять политику размещенной голосовой почты пользователя, чтобы получить сведения о маршруте.</span><span class="sxs-lookup"><span data-stu-id="7ba00-123">The Exchange UM Routing application will check the user’s hosted voice mail policy for routing details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ba00-124">ExchangeHostedVoiceMail = 0</span><span class="sxs-lookup"><span data-stu-id="7ba00-124">ExchangeHostedVoiceMail=0</span></span></p></td>
<td><p><span data-ttu-id="7ba00-125">Exchange</span><span class="sxs-lookup"><span data-stu-id="7ba00-125">Exchange</span></span></p></td>
<td><p><span data-ttu-id="7ba00-126">Пользователь отключил доступ к размещенной единой системе обмена сообщениями сервером Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7ba00-126">User has been disabled for hosted UM access by Exchange Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ba00-127">CsHostedVoiceMail = 1</span><span class="sxs-lookup"><span data-stu-id="7ba00-127">CsHostedVoiceMail=1</span></span></p></td>
<td><p><span data-ttu-id="7ba00-128">Lync Server</span><span class="sxs-lookup"><span data-stu-id="7ba00-128">Lync Server</span></span></p></td>
<td><p><span data-ttu-id="7ba00-129">Для пользователя разрешен доступ к размещению UM через Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ba00-129">User has been enabled for hosted UM access by Lync Server 2013.</span></span> <span data-ttu-id="7ba00-130">Приложение Lync Server 2013 ExUM проверит политику размещенной голосовой почты пользователя, чтобы получить сведения о маршруте.</span><span class="sxs-lookup"><span data-stu-id="7ba00-130">The Lync Server 2013 ExUM Routing application will check the user’s hosted voice mail policy for routing details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ba00-131">CsHostedVoiceMail = 0</span><span class="sxs-lookup"><span data-stu-id="7ba00-131">CsHostedVoiceMail=0</span></span></p></td>
<td><p><span data-ttu-id="7ba00-132">Lync Server</span><span class="sxs-lookup"><span data-stu-id="7ba00-132">Lync Server</span></span></p></td>
<td><p><span data-ttu-id="7ba00-133">Пользователь отключил доступ к размещенной единой системе обмена сообщениями через Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ba00-133">User has been disabled for hosted UM access by Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="7ba00-134">Если атрибут уже имеет значения, отличные от одной из пар ключей и значений в Lync Server 2013 (CSHostedVoiceMail = 0 или CSHostedVoiceMail = 1), предупреждение будет указывать на то, что этот атрибут может управляться другим приложением.</span><span class="sxs-lookup"><span data-stu-id="7ba00-134">If the attribute already has values other than one of the Lync Server 2013 key/value pairs (CSHostedVoiceMail=0 or CSHostedVoiceMail=1), a warning will indicate that the attribute may be managed by a different application.</span></span> <span data-ttu-id="7ba00-135">Например, предупреждение отображается, если пара ключ/значение ExchangeHostedVoiceMail = 0 или ExchangeHostedVoiceMail = 1 уже присутствует.</span><span class="sxs-lookup"><span data-stu-id="7ba00-135">For example, a warning is displayed if the key/value pair ExchangeHostedVoiceMail=0 or ExchangeHostedVoiceMail=1 is already present.</span></span> <span data-ttu-id="7ba00-136">В этом случае можно изменить значение, отредактировав его в службе каталогов Active Directory, или выполнить следующий командлет, чтобы задать для него значение NULL:</span><span class="sxs-lookup"><span data-stu-id="7ba00-136">In that case, you can change the value by editing it the Active Directory, or run the following cmdlet to set the value to null:</span></span><BR><span data-ttu-id="7ba00-137">Set-CsUser — пользователь с удостоверением — HostedVoicemail $null</span><span class="sxs-lookup"><span data-stu-id="7ba00-137">Set-CsUser –identity user –HostedVoicemail $null</span></span>



</div>

</div>

<div>

## <a name="enabling-users-for-hosted-voice-mail"></a><span data-ttu-id="7ba00-138">Включение пользователей для размещенной голосовой почты</span><span class="sxs-lookup"><span data-stu-id="7ba00-138">Enabling Users for Hosted Voice Mail</span></span>

<span data-ttu-id="7ba00-139">Чтобы включить переадресацию звонков голосовой почты пользователя в размещенную систему обмена СООБЩЕНИЯми Exchange, необходимо выполнить командлет Set-CsUser, чтобы задать значение параметра *HostedVoiceMail* .</span><span class="sxs-lookup"><span data-stu-id="7ba00-139">To enable a user’s voice mail calls to be routed to hosted Exchange UM, you must run the Set-CsUser cmdlet to set the value of the *HostedVoiceMail* parameter.</span></span> <span data-ttu-id="7ba00-140">Этот параметр также указывает на Lync Server 2013 для высветки индикатора звонка голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="7ba00-140">This parameter also signals Lync Server 2013 to light up the “call voice mail” indicator.</span></span>

  - <span data-ttu-id="7ba00-141">В следующем примере включается учетная запись пользователя почтового Вронский для размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="7ba00-141">The following example enables Pilar Ackerman’s user account for hosted voice mail:</span></span>
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $True
    
    <span data-ttu-id="7ba00-142">Командлет проверяет, относится ли политика размещенной голосовой почты (глобально, на уровне сайта или на пользователя) к этому пользователю.</span><span class="sxs-lookup"><span data-stu-id="7ba00-142">The cmdlet verifies that a hosted voice mail policy (global, site-level or per-user) applies to this user.</span></span> <span data-ttu-id="7ba00-143">Если политика не применяется, командлет завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="7ba00-143">If no policy applies, the cmdlet fails.</span></span>

  - <span data-ttu-id="7ba00-144">В следующем примере отключается учетная запись пользователя почтового Вронский для размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="7ba00-144">The following example disables Pilar Ackerman’s user account for hosted voice mail:</span></span>
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $False
    
    <span data-ttu-id="7ba00-145">Командлет проверяет, не применяется ли политика размещенной голосовой почты (глобальные, на уровне сайта или на пользователя) для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ba00-145">The cmdlet verifies that no hosted voice mail policy (global, site-level or per-user) applies to this user.</span></span> <span data-ttu-id="7ba00-146">Если политика применяется, командлет завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="7ba00-146">If a policy does apply, the cmdlet fails.</span></span>

<span data-ttu-id="7ba00-147">Подробнее об использовании командлета Set-CsUser можно узнать в документации на Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="7ba00-147">For details about using the Set-CsUser cmdlet, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="7ba00-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ba00-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

