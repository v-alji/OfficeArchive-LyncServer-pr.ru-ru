---
title: Командлеты в Skype для бизнеса Online, использующие только глобальную область
description: Командлеты в Skype для бизнеса Online, использующие только глобальную область.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use only the global scope
ms:assetid: 0ffd3bc9-a6a1-4c2e-8d52-e599acc49d2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362771(v=OCS.15)
ms:contentKeyID: 56558800
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a2f59806128ceea825a4cdd966e85852b98079b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398878"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-only-the-global-scope"></a><span data-ttu-id="aef40-103">Командлеты в Skype для бизнеса Online, использующие только глобальную область</span><span class="sxs-lookup"><span data-stu-id="aef40-103">Cmdlets in Skype for Business Online that use only the global scope</span></span>

 


<span data-ttu-id="aef40-104">Ряд параметров Skype для бизнеса Online доступен только в *глобальной области*.</span><span class="sxs-lookup"><span data-stu-id="aef40-104">A number of Skype for Business Online settings are available only at the *global scope*.</span></span> <span data-ttu-id="aef40-105">Это означает, что существует единственная коллекция параметров, которая применяется ко всем пользователям, которые назначены этому клиенту.</span><span class="sxs-lookup"><span data-stu-id="aef40-105">This means that there is a single collection of settings that applies to all the users who are assigned to that tenant.</span></span> <span data-ttu-id="aef40-106">(У каждого клиента есть своя уникальная коллекция глобальных параметров.) При использовании командлетов, ограниченных глобальной областью, параметр Identity является необязательным.</span><span class="sxs-lookup"><span data-stu-id="aef40-106">(Each tenant has its own unique collection of global settings.) When you are using cmdlets that are limited to the global scope, the Identity parameter is optional.</span></span> <span data-ttu-id="aef40-107">Например, чтобы получить параметры конфигурации собрания, можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="aef40-107">For example, to retrieve meeting configuration settings, you can use this command:</span></span>

    Get-CsMeetingConfiguration -Identity "global"

<span data-ttu-id="aef40-108">Кроме того, вы можете опустить параметр Identity и использовать эту простую команду вместо этого:</span><span class="sxs-lookup"><span data-stu-id="aef40-108">Alternatively, you can omit the Identity parameter and use this simpler command instead:</span></span>

    Get-CsMeetingConfiguration

<span data-ttu-id="aef40-109">Так как имеется только одна глобальная коллекция параметров конфигурации собрания, две команды возвращают одни и те же данные.</span><span class="sxs-lookup"><span data-stu-id="aef40-109">Because there is only one global collection of meeting configuration settings, the two commands return the exact same information.</span></span> <span data-ttu-id="aef40-110">Параметр Identity также можно опустить при использовании одного из командлетов **Set-CS** .</span><span class="sxs-lookup"><span data-stu-id="aef40-110">The Identity parameter can also be omitted when using one of the **Set-Cs** cmdlets.</span></span> <span data-ttu-id="aef40-111">Эти две команды идентичны:</span><span class="sxs-lookup"><span data-stu-id="aef40-111">These two commands are identical:</span></span>

    Set-CsMeetingConfiguration -Identity "global" -AdmitAnonymousUsersByDefault $False
    Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $False

<span data-ttu-id="aef40-112">Две команды идентичны, так как по умолчанию Windows PowerShell изменит глобальную коллекцию, если не включить параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="aef40-112">The two commands are identical because, by default, Windows PowerShell will modify the global collection if you do not include the Identity parameter.</span></span>

<span data-ttu-id="aef40-113">Следующие командлеты работают только в глобальной области:</span><span class="sxs-lookup"><span data-stu-id="aef40-113">The following cmdlets operate only at the global scope:</span></span>

  - <span data-ttu-id="aef40-114">[Get-CsImFilterConfiguration](https://technet.microsoft.com/library/gg398980\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-114">[Get-CsImFilterConfiguration](https://technet.microsoft.com/library/gg398980\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-115">[Get-CsMeetingConfiguration](https://technet.microsoft.com/library/gg425875\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-115">[Get-CsMeetingConfiguration](https://technet.microsoft.com/library/gg425875\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-116">[Get-CsPrivacyConfiguration](https://technet.microsoft.com/library/gg413002\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-116">[Get-CsPrivacyConfiguration](https://technet.microsoft.com/library/gg413002\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-117">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-117">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-118">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-118">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-119">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-119">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-120">[Get-CsTenantPublicProvider](https://technet.microsoft.com/library/jj994016\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-120">[Get-CsTenantPublicProvider](https://technet.microsoft.com/library/jj994016\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-121">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/gg398309\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-121">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/gg398309\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-122">[Set-CsMeetingConfiguration](https://technet.microsoft.com/library/gg398648\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-122">[Set-CsMeetingConfiguration](https://technet.microsoft.com/library/gg398648\(v=ocs.15\))</span></span>

  - <span data-ttu-id="aef40-123">[Set-CsPrivacyConfiguration](https://technet.microsoft.com/library/gg398484\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-123">[Set-CsPrivacyConfiguration](https://technet.microsoft.com/library/gg398484\(v=ocs.15\))</span></span>

<span data-ttu-id="aef40-124">Обратите внимание, что командлет **Remove-CsVoicePolicy** является какой-либо аномалией.</span><span class="sxs-lookup"><span data-stu-id="aef40-124">Note that the **Remove-CsVoicePolicy** cmdlet is something of an anomaly.</span></span> <span data-ttu-id="aef40-125">Для начала для этого командлета требуется включить параметр Identity:</span><span class="sxs-lookup"><span data-stu-id="aef40-125">First, this cmdlet does require you to include the Identity parameter:</span></span>

    Remove-CsVoicePolicy -Identity "global"

<span data-ttu-id="aef40-126">Во-вторых, командлет **Remove-CsVoicePolicy** фактически не удаляет глобальную политику голосовой связи; В Skype для бизнеса Online запрещено удалять глобальные политики и параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="aef40-126">Second, the **Remove-CsVoicePolicy** cmdlet does not actually delete the global voice policy; Skype for Business Online does not allow you to delete global policies or configuration settings.</span></span> <span data-ttu-id="aef40-127">Действие командлета — это возможность сброса всех свойств в глобальной политике голосовой связи в значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aef40-127">What the cmdlet does do is enable you to reset all the properties in the global voice policy to their default values.</span></span> <span data-ttu-id="aef40-128">Например, по умолчанию для свойства AllowCallForwarding задано значение false.</span><span class="sxs-lookup"><span data-stu-id="aef40-128">For example, by default, the AllowCallForwarding property is set to False.</span></span> <span data-ttu-id="aef40-129">Тем не менее, AllowCallForwarding может быть изменено, и теперь для него установлено значение true.</span><span class="sxs-lookup"><span data-stu-id="aef40-129">However, AllowCallForwarding may have been modified, with the value now set to True.</span></span> <span data-ttu-id="aef40-130">При запуске командлета **Remove-CsVoicePolicy** свойству AllowCallForwarding будет возвращено значение по умолчанию: false.</span><span class="sxs-lookup"><span data-stu-id="aef40-130">When you run the **Remove-CsVoicePolicy** cmdlet, the AllowCallForwarding property will revert to its default value: False.</span></span> <span data-ttu-id="aef40-131">В приведенной ниже таблице перечислены сценарии.</span><span class="sxs-lookup"><span data-stu-id="aef40-131">The following table summarizes this scenario:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aef40-132">Значение AllowCallForwarding</span><span class="sxs-lookup"><span data-stu-id="aef40-132">AllowCallForwarding Value</span></span></th>
<th><span data-ttu-id="aef40-133">Сценарий</span><span class="sxs-lookup"><span data-stu-id="aef40-133">Scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aef40-134">False</span><span class="sxs-lookup"><span data-stu-id="aef40-134">False</span></span></p></td>
<td><p><span data-ttu-id="aef40-135">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="aef40-135">Default value</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef40-136">Верно</span><span class="sxs-lookup"><span data-stu-id="aef40-136">True</span></span></p></td>
<td><p><span data-ttu-id="aef40-137">После изменения глобальной политики</span><span class="sxs-lookup"><span data-stu-id="aef40-137">After the global policy has been modified</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef40-138">False</span><span class="sxs-lookup"><span data-stu-id="aef40-138">False</span></span></p></td>
<td><p><span data-ttu-id="aef40-139">После запуска командлета <strong>Remove-CsVoicePolicy</strong></span><span class="sxs-lookup"><span data-stu-id="aef40-139">After <strong>Remove-CsVoicePolicy</strong> cmdlet has been run</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="aef40-140">См. также</span><span class="sxs-lookup"><span data-stu-id="aef40-140">See Also</span></span>


[<span data-ttu-id="aef40-141">Удостоверения, области и клиенты в Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="aef40-141">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="aef40-142">[Командлеты Lync Online](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="aef40-142">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

