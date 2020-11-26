---
title: 'Lync Server 2013: создание политик расположения'
description: 'Lync Server 2013: создание политик расположения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create location policies
ms:assetid: f1878194-c756-4794-8fa1-15dd2118b4b3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413006(v=OCS.15)
ms:contentKeyID: 48185794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 464ea9893890ab6185f180434e2dad13818123d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431934"
---
# <a name="create-location-policies-in-lync-server-2013"></a><span data-ttu-id="3d73f-103">Создание политик местоположений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3d73f-103">Create location policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d73f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d73f-104">

<span> </span></span></span>

<span data-ttu-id="3d73f-105">_**Тема последнего изменения:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="3d73f-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="3d73f-106">Lync Server использует политику расположения для включения клиентов Lync для E9-1-1 во время регистрации клиента.</span><span class="sxs-lookup"><span data-stu-id="3d73f-106">Lync Server uses a location policy to enable Lync clients for E9-1-1 during client registration.</span></span> <span data-ttu-id="3d73f-107">Политика расположения содержит параметры, которые определяют порядок реализации E911.</span><span class="sxs-lookup"><span data-stu-id="3d73f-107">A location policy contains the settings that define how E9-1-1 will be implemented.</span></span>

<span data-ttu-id="3d73f-p102">Глобальную политику расположения можно редактировать, кроме того, можно создавать новые именованные политики расположения. Клиент получает глобальную политику, если он расположен не в подсети, для которой имеется связанная локальная политика, или если локальная политика не назначена ему напрямую. Именованные политики назначаются подсетям или пользователям.  </span><span class="sxs-lookup"><span data-stu-id="3d73f-p102">You can edit the global location policy and create new tagged location policies. A client obtains a global policy when it is not located within a subnet with an associated location policy, or when the client has not been directly assigned a location policy. Tagged policies are assigned to subnets or users.</span></span>

<span data-ttu-id="3d73f-111">Чтобы создать политику расположения, следует использовать учетную запись, являющуюся членом группы RTCUniversalServerAdmins или административной роли CsVoiceAdministrator или обладает эквивалентными правами и разрешениями администратора.</span><span class="sxs-lookup"><span data-stu-id="3d73f-111">To create a location policy, you must use an account that is a member of the RTCUniversalServerAdmins group, or is a member of the CsVoiceAdministrator administrative role, or has equivalent administrator rights and permissions.</span></span>

<span data-ttu-id="3d73f-112">Полное описание политик местоположений показано в разделе [Определение политики расположения для Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="3d73f-112">For a complete description of Location policies, see [Defining the location policy for Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span></span> <span data-ttu-id="3d73f-113">Командлеты в этой процедуре используют политику расположения, определенную с помощью следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3d73f-113">Cmdlets in this procedure use a location policy defined using the following values:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d73f-114">Элемент</span><span class="sxs-lookup"><span data-stu-id="3d73f-114">Element</span></span></th>
<th><span data-ttu-id="3d73f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3d73f-115">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d73f-116">EnhancedEmergencyServicesEnabled</span><span class="sxs-lookup"><span data-stu-id="3d73f-116">EnhancedEmergencyServicesEnabled</span></span></p></td>
<td><p><span data-ttu-id="3d73f-117"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-117"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d73f-118">LocationRequired</span><span class="sxs-lookup"><span data-stu-id="3d73f-118">LocationRequired</span></span></p></td>
<td><p><span data-ttu-id="3d73f-119"><strong>Заявление об отказе</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-119"><strong>Disclaimer</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d73f-120">EnhancedEmergencyServiceDisclaimer</span><span class="sxs-lookup"><span data-stu-id="3d73f-120">EnhancedEmergencyServiceDisclaimer</span></span></p></td>
<td><p><span data-ttu-id="3d73f-p104">Политика вашей компании требует задать расположение. В противном случае в экстренной ситуации соответствующие службы не смогут определить ваше расположение. Задайте расположение.</span><span class="sxs-lookup"><span data-stu-id="3d73f-p104">Your company policy requires you to set a location. If you do not set a location, emergency services will not be able to locate you in an emergency. Please set a location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d73f-124">UseLocationForE911Only</span><span class="sxs-lookup"><span data-stu-id="3d73f-124">UseLocationForE911Only</span></span></p></td>
<td><p><span data-ttu-id="3d73f-125"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-125"><strong>False</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d73f-126">PstnUsage</span><span class="sxs-lookup"><span data-stu-id="3d73f-126">PstnUsage</span></span></p></td>
<td><p><span data-ttu-id="3d73f-127"><strong>EmergencyUsage</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-127"><strong>EmergencyUsage</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d73f-128">EmergencyDialString</span><span class="sxs-lookup"><span data-stu-id="3d73f-128">EmergencyDialString</span></span></p></td>
<td><p><span data-ttu-id="3d73f-129"><strong>911</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-129"><strong>911</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d73f-130">EmergencyDialMask</span><span class="sxs-lookup"><span data-stu-id="3d73f-130">EmergencyDialMask</span></span></p></td>
<td><p><span data-ttu-id="3d73f-131"><strong>112</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-131"><strong>112</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d73f-132">NotificationUri</span><span class="sxs-lookup"><span data-stu-id="3d73f-132">NotificationUri</span></span></p></td>
<td><p><span data-ttu-id="3d73f-133"><strong>sip:security@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-133"><strong>sip:security@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d73f-134">ConferenceUri</span><span class="sxs-lookup"><span data-stu-id="3d73f-134">ConferenceUri</span></span></p></td>
<td><p><span data-ttu-id="3d73f-135"><strong>sip:+14255550123@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-135"><strong>sip:+14255550123@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d73f-136">ConferenceMode</span><span class="sxs-lookup"><span data-stu-id="3d73f-136">ConferenceMode</span></span></p></td>
<td><p><span data-ttu-id="3d73f-137"><strong>twoway</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-137"><strong>twoway</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d73f-138">LocationRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="3d73f-138">LocationRefreshInterval</span></span></p></td>
<td><p><span data-ttu-id="3d73f-139"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="3d73f-139"><strong>2</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d73f-140">Подробные сведения о работе с политиками расположения можно найти в документации по оболочке управления Lync Server для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3d73f-140">For details about working with location policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="3d73f-141">New-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3d73f-141">New-CsLocationPolicy</span></span>

  - <span data-ttu-id="3d73f-142">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3d73f-142">Get-CsLocationPolicy</span></span>

  - <span data-ttu-id="3d73f-143">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3d73f-143">Set-CsLocationPolicy</span></span>

  - <span data-ttu-id="3d73f-144">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3d73f-144">Remove-CsLocationPolicy</span></span>

  - <span data-ttu-id="3d73f-145">Grant-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3d73f-145">Grant-CsLocationPolicy</span></span>

<div>

## <a name="to-create-location-policies"></a><span data-ttu-id="3d73f-146">Создание политик расположения</span><span class="sxs-lookup"><span data-stu-id="3d73f-146">To create location policies</span></span>

1.  <span data-ttu-id="3d73f-147">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="3d73f-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3d73f-148">Командлет CsLocationPolicy завершится с ошибкой, если значение для параметра <STRONG>PstnUsage</STRONG> не будет содержаться в глобальном списке параметров PstnUsage.</span><span class="sxs-lookup"><span data-stu-id="3d73f-148">CsLocationPolicy will fail if the setting for <STRONG>PstnUsage</STRONG> is not already in the Global list of PstnUsages.</span></span>

    
    </div>

2.  <span data-ttu-id="3d73f-149">Чтобы изменить глобальную политику расположения, можно дополнительно выполнить следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="3d73f-149">Optionally, run the following cmdlet to edit the global Location Policy:</span></span>
    
        Set-CsLocationPolicy -Identity Global -EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -PstnUsage "emergencyUsage" -EmergencyDialString "911" -ConferenceMode "twoway" -ConferenceUri "sip:+14255550123@litwareinc.com" -EmergencyDialMask "112" NotificationUri "sip:security@litwareinc.com" -UseLocationForE911Only $true -LocationRefreshInterval 2

3.  <span data-ttu-id="3d73f-150">Выполните следующие действия, чтобы создать именованную политику расположения.</span><span class="sxs-lookup"><span data-stu-id="3d73f-150">Run the following to create a tagged Location Policy.</span></span>
    
        New-CsLocationPolicy -Identity Tag:Redmond - EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -UseLocationForE911Only $false -PstnUsage "EmergencyUsage" -EmergencyDialString "911" -EmergencyDialMask "112" -NotificationUri "sip:security@litwareinc.com" -ConferenceUri "sip:+14255550123@litwareinc.com" -ConferenceMode "twoway" -LocationRefreshInterval 2

4.  <span data-ttu-id="3d73f-151">Выполните следующий командлет, чтобы применить именованную политику расположения, созданную в шаге 3, к политике пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d73f-151">Run the following cmdlet to apply the tagged Location Policy created in step 3 to a user policy.</span></span>
    
        (Get-CsUser | where { $_.Name -match "UserName" }) | Grant-CsLocationPolicy -PolicyName Redmond

<span data-ttu-id="3d73f-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d73f-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

