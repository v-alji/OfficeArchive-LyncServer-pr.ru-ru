---
title: 'Lync Server 2013: Включение маршрутизации Location-Based'
description: 'Lync Server 2013: Включение маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Location-Based Routing
ms:assetid: 029ede7e-0c4e-4ad2-af99-909ae674d6fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994014(v=OCS.15)
ms:contentKeyID: 51803920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7844af5792468cd5645b6b42c857c63b943c2df1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399286"
---
# <a name="enabling-location-based-routing-in-lync-server-2013"></a>Включение маршрутизации Location-Based в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-04-26_

После развертывания корпоративной голосовой почты и регионов сети, сайтов и подсетей вы можете включить Location-Based маршрутизацию. Для следующих корпоративных элементов голосовой связи необходимо включить Location-Based маршрутизации:

  - Сетевые сайты

  - Конфигурации магистрали

  - Политики голосовой связи

  - Настройка маршрутизации

<div>

## <a name="enable-location-based-routing-to-network-sites"></a>Включение маршрутизации Location-Based на сайты сети

После того как вы развернули корпоративный голос и настроили сетевые сайты, вы можете настроить маршрутизацию Location-Based. Сначала необходимо создать политику маршрутизации голосовой связи для связи сайта сети с соответствующими использованием PSTN. Когда вы назначаете использование PSTN для политики голосовой маршрутизации, убедитесь в том, что используются только использование PSTN, связанное с голосовыми маршрутами, которые используют локальный шлюз для сайта или шлюза PSTN, который находится в регионе, где не требуется Location-Based ограничения маршрутизации. С помощью команды Lync Server Windows PowerShell, панели управления New-CsVoiceRoutingPolicy или Lync Server можно создавать политики голосовой маршрутизации.

    New-CsVoiceRoutingPolicy -Identity <voice routing policy ID> -Name <voice routing policy name> -PstnUsages <usages>

Дополнительные сведения см. в разделе [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).

В этом примере приведенная ниже таблица и команды Windows PowerShell иллюстрируют две политики маршрутизации голосовой связи и использование PSTN, описанных в этом сценарии. Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.

    New-CsVoiceRoutingPolicy -Identity "DelhiVoiceRoutingPolicy" -Name "Delhi voice routing policy" -PstnUsages @{add="Delhi usage", "PBX Del usage", "PBX Hyd usage"}
    New-CsVoiceRoutingPolicy -Identity "HyderabadVoiceRoutingPolicy" -Name " Hyderabad voice routing policy" -PstnUsages @{add="Hyderabad usage", "PBX Del usage", "PBX Hyd usage"}


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Политика маршрутизации голосовой связи 1</th>
<th>Политика маршрутизации голосовой связи 2</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Идентификатор политики голосовой связи</p></td>
<td><p>Политика маршрутизации голосовой связи Delhi</p></td>
<td><p>Политика маршрутизации голосовой связи Hyderabad</p></td>
</tr>
<tr class="even">
<td><p>Использование PSTN</p></td>
<td><p>Использование Delhi, использование АТС DELETE, использование Hyd УАТС</p></td>
<td><p>Использование Hyderabad, Hyd УАТС, использование АТС Delete</p></td>
</tr>
</tbody>
</table>

  

Затем настройте маршрутизацию Location-Based для соответствующих сайтов сети и свяжите с ними политики маршрутизации голосовой связи. Используйте команду Lync Server Windows PowerShell New-CsNetworkSite, чтобы включить Location-Based маршрутизацию и сопоставить политики маршрутизации голосовой связи с сетевыми сайтами, которые должны применять ограничения маршрутизации.

    Set-CsNetworkSite -Identity <site ID> -EnableLocationBasedRouting <$true|$false> -VoiceRoutingPolicy <voice routing policy ID>

В приведенной ниже таблице показано, Location-Based маршрутизацию для двух различных сайтов сети Delhi и Hyderabad, определенных в этом сценарии, с помощью Lync Server Windows PowerShell. Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.

    Set-CsNetworkSite -Identity "Delhi" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "DelhiVoiceRoutingPolicy"
    Set-CsNetworkSite -Identity "Hyderabad" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "HyderabadVoiceRoutingPolicy"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Сайт 1 (Delhi)</th>
<th>Сайт 2 (Hyderabad)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя сайта</p></td>
<td><p>Сайт 1 (Delhi)</p></td>
<td><p>Сайт 2 (Hyderabad)</p></td>
</tr>
<tr class="even">
<td><p>EnableLocationBasedRouting</p></td>
<td><p>Верно</p></td>
<td><p>Верно</p></td>
</tr>
<tr class="odd">
<td><p>Политика маршрутизации голосовой связи</p></td>
<td><p>Политика маршрутизации голосовой связи Delhi</p></td>
<td><p>Политика маршрутизации голосовой связи Hyderabad</p></td>
</tr>
<tr class="even">
<td><p>Подсети</p></td>
<td><p>Подсеть 1 (Delhi)</p></td>
<td><p>Подсеть 2 (Hyderabad)</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-trunks"></a>Включение маршрутизации Location-Based в магистральные магистрали

Прежде чем можно будет включить конфигурацию магистрали для маршрутизации Location-Based, необходимо создать конфигурацию магистрали для каждой магистрали или каждого из сайтов сети. Используйте команду Lync Server Windows PowerShell New-CsTrunkConfiguration для создания конфигурации канала магистрали. Если несколько магистральных каналов связаны с определенной системой (например, Gateway или УАТС), каждую из них нужно изменить, чтобы включить Location-Based ограничения маршрутизации.

    New-CsTrunkConfiguration -Identity < trunk configuration ID>

Дополнительные сведения можно найти в разделе [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).

В этом примере следующие команды Windows PowerShell иллюстрируют создание одной конфигурации магистрали для каждой магистрали в развертывании, определенном в этом сценарии.

    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 1 DEL-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 2 HYD-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 3 DEL-PBX>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 4 HYD-PBX>"

После настройки магистральной конфигурации для каждой магистрали вы можете использовать команду Lync Server Windows PowerShell Set-CsTrunkConfiguration, чтобы включить Location-Based маршрутизацию на магистральные системы, которые должны применять ограничения маршрутизации. Включите Location-Based маршрутизацию на магистральы, которые направляют звонки на шлюзы PSTN, которые перенаправляют звонки в КТСОП и связывают сетевой сайт, на котором расположен шлюз.

    Set-CsTrunkConfiguration -Identity <trunk configuration ID> -EnableLocationRestriction $true -NetworkSiteID <site ID>

Дополнительные сведения можно найти в разделе [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).

В этом примере Location-Based маршрутизация включена для каждой магистрали, связанной с шлюзами PSTN в Delhi и Hyderabad:

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 1 DEL-GW -EnableLocationRestriction $true -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 2 HYD-GW -EnableLocationRestriction $true -NetworkSiteID "Hyderabad"

  

Не включайте Location-Based маршрутизацию для каналов, которые не направляют звонки в КТСОП. Однако вы по-прежнему обязаны привязать магистраль к сетевому сайту, на котором находится система, так как Location-Based ограничения маршрутизации, которые необходимо применять для звонков по протоколу PSTN, подключенных к конечным точкам с помощью этой магистрали. В этом примере Location-Based маршрутизация не включена для каждой магистрали, связанной с системами УАТС в Delhi и Hyderabad:

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 3 DEL-PBX -EnableLocationRestriction $false -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 4 HYD-PBX -EnableLocationRestriction $false -NetworkSiteID "Hyderabad"

  
Конечные точки, которые подключены к системам, не накладываемым на протокол PSTN (например, УАТС), имеют аналогичные ограничения в качестве конечных точек Lync для пользователей, которые включены для Location-Based маршрутизации. Это означает, что эти пользователи смогут размещать и принимать звонки на пользователей Lync, независимо от местонахождения пользователя. Кроме того, они смогут принимать звонки в другие системы и из них, которые не направляют звонки в сеть PSTN (например, конечную точку, подключенную к другой УАТС) независимо от того, с какой сетевой страницы связана система. Все входящие звонки, звонки, передача звонков и переадресация звонков с использованием конечных точек PSTN будут Location-Based принудительной маршрутизацией. Такие звонки должны использовать только шлюзы PSTN, определенные как локальные для таких систем.

В приведенной ниже таблице показана конфигурация магистрали с четырьмя магистральами на двух разных сетевых сайтах: два соединения с шлюзами PSTN и двумя подключенными к системам АТС.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Имя</th>
<th>EnableLocationRestriction</th>
<th>NetworkSiteID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>PstnGateway: магистраль 1 DEL-GW</p></td>
<td><p>Верно</p></td>
<td><p>Сайт 1 (Delhi)</p></td>
</tr>
<tr class="even">
<td><p>PstnGateway: магистраль 2 HYD-GW</p></td>
<td><p>Верно</p></td>
<td><p>Сайт 2 (Hyderabad)</p></td>
</tr>
<tr class="odd">
<td><p>PstnGateway: магистраль 3 DEL-УАТС</p></td>
<td><p>False</p></td>
<td><p>Сайт 1 (Delhi)</p></td>
</tr>
<tr class="even">
<td><p>PstnGateway: HYD-УАТС (магистральная линия 4)</p></td>
<td><p>False</p></td>
<td><p>Сайт 2 (Hyderabad)</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-voice-policies"></a>Включение Location-Based маршрутизации к политикам голосовой связи

Чтобы включить Location-Based маршрутизацию для определенных пользователей, настройте политику голосовой связи пользователей, чтобы отключить бесплатный звонок. Используйте команду Lync Server Windows PowerShell New-CsVoicePolicy, чтобы создать новую политику голосовой связи или Set-CsVoicePolicy, при использовании существующей политики для включения Location-Based маршрутизации, запретив бесплатный звонок по протоколу КТСОП.

    Set-CsVoicePolicy -Identity <voice policy ID> -PreventPSTNTollBypass <$true|$false>

Дополнительные сведения можно найти в разделе [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).

В этом примере приведенная ниже таблица и команды Windows PowerShell иллюстрируют использование политик голосовой связи по Delhi и Hyderabad, описанных в этом сценарии, в целях предотвращения бесплатной поддержки PSTN. Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.

    Set-CsVoicePolicy -Identity "Delhi voice policy" -PreventPSTNTollBypass $true
    Set-CsVoicePolicy -Identity "Hyderabad voice policy" -PreventPSTNTollBypass $true


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Политика голосовой связи 1</th>
<th>Политика голосовой связи 2</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Идентификатор политики голосовой связи</p></td>
<td><p>Политика голосовой связи Delhi</p></td>
<td><p>Политика голосовой связи Hyderabad</p></td>
</tr>
<tr class="even">
<td><p>Использование PSTN</p></td>
<td><p>Использование Delhi, использование АТС DELETE, использование Hyd УАТС</p></td>
<td><p>Использование Hyderabad, Hyd УАТС, использование АТС Delete</p></td>
</tr>
<tr class="odd">
<td><p>PreventPSTNTollBypass</p></td>
<td><p>Верно</p></td>
<td><p>Верно</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-in-the-routing-configuration"></a>Включение маршрутизации Location-Based в конфигурации маршрутизации

Наконец, разрешите Location-Based маршрутизацию в конфигурацию маршрутизации. Используйте команду Lync Server Windows PowerShell New-CsRoutingConfiguration, чтобы включить маршрутизацию Location-Based.

    Set-CsRoutingConfiguration -EnableLocationBasedRouting $true

Дополнительные сведения можно найти в разделе [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).

<div>


> [!NOTE]  
> Несмотря на то, что в глобальной конфигурации должна быть включена Location-Based маршрутизация, набор применяемых правил будет применяться только для сайтов, пользователей и магистральов, для которых она настроена, как указано в этой документации.



</div>

<div>


</div>

</div>

<div>

## <a name="see-also"></a>См. также


[Настройка маршрутизации на основе расположения в Lync Server 2013](lync-server-2013-configuring-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

