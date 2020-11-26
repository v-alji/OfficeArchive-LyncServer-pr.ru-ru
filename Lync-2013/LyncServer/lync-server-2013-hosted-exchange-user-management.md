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
# <a name="hosted-exchange-user-management-in-lync-server-2013"></a>Управление пользователями размещенной системы Exchange в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-18_

Чтобы предоставить услуги голосовой почты для пользователей Lync Server 2013, чьи почтовые ящики находятся на размещенной службе Exchange, необходимо включить учетные записи пользователей для размещенной голосовой почты.

<div>


> [!NOTE]  
> Прежде чем пользователи Lync Server 2013 могут быть включены для поддержки размещенной голосовой почты, необходимо развернуть политику размещенной голосовой почты, которая применяется к соответствующей учетной записи пользователя. Политика может быть глобальной, сайтовой или для пользователя в области действия, если она применяется к пользователю, который вы хотите включить. Подробнее смотрите в разделе <A href="lync-server-2013-hosted-voice-mail-policies.md">политики размещенной голосовой почты в Lync Server 2013</A>.



</div>

<div>

## <a name="the-msexchucvoicemailsettings-attribute"></a>Атрибут msExchUCVoiceMailSettings

Lync Server 2013 представляет новый пользовательский атрибут с именем **msExchUCVoiceMailSettings**, который создается в рамках подготовки схемы Active Directory для Lync Server 2013. Этот многозначный атрибут содержит параметры голосовой почты, которые являются общими для Lync Server 2013 и размещенной службы Exchange.

В некоторых случаях размещенной службе Exchange может быть задано значение атрибута msExchUCVoiceMailSettings в процессе включения UM-среды Exchange или в процессе переноса почтовых ящиков на размещенный сервер Exchange. Если этот атрибут не задан Exchange, администратор Lync Server 2013 должен настроить его, выполнив командлет Set-CsUser, как описано ранее в этой статье.

В приведенной ниже таблице указаны пары "ключ-значение" для атрибута и их авторы.

### <a name="the-msexchucvoicemailsettings-attribute-keyvalue-pairs"></a>Пары ключей и значений в атрибуте msExchUCVoiceMailSettings

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Созданные</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ExchangeHostedVoiceMail = 1</p></td>
<td><p>Exchange</p></td>
<td><p>Для пользователя разрешен доступ к размещенной единой системе обмена сообщениями через Exchange Server. Приложение маршрутизации UM Exchange будет проверять политику размещенной голосовой почты пользователя, чтобы получить сведения о маршруте.</p></td>
</tr>
<tr class="even">
<td><p>ExchangeHostedVoiceMail = 0</p></td>
<td><p>Exchange</p></td>
<td><p>Пользователь отключил доступ к размещенной единой системе обмена сообщениями сервером Exchange Server.</p></td>
</tr>
<tr class="odd">
<td><p>CsHostedVoiceMail = 1</p></td>
<td><p>Lync Server</p></td>
<td><p>Для пользователя разрешен доступ к размещению UM через Lync Server 2013. Приложение Lync Server 2013 ExUM проверит политику размещенной голосовой почты пользователя, чтобы получить сведения о маршруте.</p></td>
</tr>
<tr class="even">
<td><p>CsHostedVoiceMail = 0</p></td>
<td><p>Lync Server</p></td>
<td><p>Пользователь отключил доступ к размещенной единой системе обмена сообщениями через Lync Server 2013.</p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> Если атрибут уже имеет значения, отличные от одной из пар ключей и значений в Lync Server 2013 (CSHostedVoiceMail = 0 или CSHostedVoiceMail = 1), предупреждение будет указывать на то, что этот атрибут может управляться другим приложением. Например, предупреждение отображается, если пара ключ/значение ExchangeHostedVoiceMail = 0 или ExchangeHostedVoiceMail = 1 уже присутствует. В этом случае можно изменить значение, отредактировав его в службе каталогов Active Directory, или выполнить следующий командлет, чтобы задать для него значение NULL:<BR>Set-CsUser — пользователь с удостоверением — HostedVoicemail $null



</div>

</div>

<div>

## <a name="enabling-users-for-hosted-voice-mail"></a>Включение пользователей для размещенной голосовой почты

Чтобы включить переадресацию звонков голосовой почты пользователя в размещенную систему обмена СООБЩЕНИЯми Exchange, необходимо выполнить командлет Set-CsUser, чтобы задать значение параметра *HostedVoiceMail* . Этот параметр также указывает на Lync Server 2013 для высветки индикатора звонка голосовой почты.

  - В следующем примере включается учетная запись пользователя почтового Вронский для размещенной голосовой почты.
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $True
    
    Командлет проверяет, относится ли политика размещенной голосовой почты (глобально, на уровне сайта или на пользователя) к этому пользователю. Если политика не применяется, командлет завершается сбоем.

  - В следующем примере отключается учетная запись пользователя почтового Вронский для размещенной голосовой почты.
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $False
    
    Командлет проверяет, не применяется ли политика размещенной голосовой почты (глобальные, на уровне сайта или на пользователя) для этого пользователя. Если политика применяется, командлет завершается сбоем.

Подробнее об использовании командлета Set-CsUser можно узнать в документации на Lync Server Management Shell.

</div>

</div>

<span> </span>

</div>

</div>

</div>

