---
title: 'Lync Server 2013: параметры согласования для федеративных XMPP-партнеров'
description: 'Lync Server 2013: параметры согласования для федеративных партнеров XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445590"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a>Параметры согласования для федеративных XMPP-партнеров в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-21_

Параметры типов согласования в конфигурации XMPP партнера имеют широкий спектр возможных комбинаций. Не все из этих сочетаний являются допустимыми. В таблице, подробно описанной в этом разделе, определяются допустимые и недопустимые параметры. Общие конфигурации представлены в первой таблице, во второй — на всех возможных комбинациях. Обратите внимание на то, что вы не можете использовать *простую проверку подлинности и уровень безопасности* (SASL), **если** также не доступен TLS- *Безопасность* . SASL отправляется в незашифрованном (читаемом) формате, и его не следует передавать, если только они не защищены другим способом, например TLS.

### <a name="common-xmpp-federation-negotiation-methods"></a>Распространенные методы согласования XMPP Федерации

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Безопасность уровня транспорта (TLS)</th>
<th>Простая проверка подлинности и уровень безопасности (SASL)</th>
<th>Проверка подлинности Dialback</th>
<th>Ожидаемый метод проверки подлинности (-ов)</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> Обязательно</p></td>
<td><p>Обязательно</p></td>
<td><p>False</p></td>
<td><p>SASL по протоколу TLS</p></td>
<td><p>TLS и SASL должны обеспечивать безопасность потока сообщений SASL. Dialback недоступен и не может использоваться для резервного метода в том случае, если для федеративного партнера XMPP не задано обязательное или необязательное значение TLS.</p></td>
</tr>
<tr class="even">
<td><p>Обязательный</p></td>
<td><p>Необязательно </p></td>
<td><p>Верно</p></td>
<td><p>SASL over TLS, TLS Dialback, TCP Dialback</p></td>
<td><p>Если для федеративного партнера XMPP задано значение SASL для необязательного или требуемого SASL, используется TLS. Если SASL недоступен, будет использоваться Dialback по TLS.</p></td>
</tr>
<tr class="odd">
<td><p>Необязательно </p></td>
<td><p>Необязательно</p></td>
<td><p>Верно</p></td>
<td><p>SASL over TLS, TLS Dialback, TCP Dialback</p></td>
<td><p>Несмотря на то, что предлагаемые методы согласования очень гибки, эти параметры основываются на параметрах партнера XMPP Федерации. Если у партнера есть TLS, необязательный или обязательный, но SASL не поддерживается, TLS Dialback будет доступен. Если у партнера есть TLS и SASL, для которых установлен необязательный или обязательный вариант, используется оптимальный выбор TLS более SASL.</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>Не поддерживается</p></td>
<td><p>Верно</p></td>
<td><p>TCP Dialback</p></td>
<td><p>Во многих случаях TCP Dialback является единственным возможным решением. Менее предпочтительнее, чем другие параметры, она обеспечивает некоторый уровень доверия.</p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a>Матрица методов согласования XMPP Федерации — завершено

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Безопасность уровня транспорта (TLS)</th>
<th>Простая проверка подлинности и уровень безопасности (SASL)</th>
<th>Проверка подлинности Dialback</th>
<th>Ожидаемый метод проверки подлинности</th>
<th>Заметки, предупреждение или ошибка для недействительной конфигурации</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> Обязательно</p></td>
<td><p>Обязательно</p></td>
<td><p>Верно</p></td>
<td><p>SASL по протоколу TLS</p></td>
<td><div>

> [!WARNING]  
> Dialback не будет работать, если требуются оба SASL и TLS.


</div></td>
</tr>
<tr class="even">
<td><p> Обязательно</p></td>
<td><p>Обязательно</p></td>
<td><p>False</p></td>
<td><p>SASL по протоколу TLS</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Необязательно </p></td>
<td><p>Обязательный</p></td>
<td><p>Верно</p></td>
<td><p>SASL over TLS, TLS Dialback, TCP Dialback</p></td>
<td><div>

> [!WARNING]  
> Для SASL требуется TLS. Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.


</div></td>
</tr>
<tr class="even">
<td><p>Необязательно </p></td>
<td><p>Обязательный</p></td>
<td><p>False</p></td>
<td><p>SASL по протоколу TLS</p></td>
<td><div>

> [!WARNING]  
> Для SASL требуется TLS. Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.


</div></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>Обязательный</p></td>
<td><p>Верно</p></td>
<td><p>TCP Dialback</p></td>
<td><div>

> [!WARNING]  
> Для SASL требуется TLS. Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.


</div></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>Обязательный</p></td>
<td><p>False</p></td>
<td><div>

> [!WARNING]  
> Недействительная конфигурация


</div></td>
<td><div>

> [!WARNING]  
> Так как для SASL требуется протокол TLS, а протокол TLS недоступен, SASL/TLS выполнить не удастся. Для TCP Dialback задано значение false, и его нельзя использовать.


</div></td>
</tr>
<tr class="odd">
<td><p>Обязательный</p></td>
<td><p>Необязательно </p></td>
<td><p>Верно</p></td>
<td><p>SASL over TLS, Dialback TLS</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Обязательный</p></td>
<td><p>Необязательно </p></td>
<td><p>False</p></td>
<td><p>SASL по протоколу TLS</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Необязательно </p></td>
<td><p>Необязательно</p></td>
<td><p>Верно</p></td>
<td><p>SASL over TLS, TLS Dialback, TCP Dialback</p></td>
<td><div>

> [!WARNING]  
> Для SASL требуется TLS. Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.


</div></td>
</tr>
<tr class="even">
<td><p>Необязательно </p></td>
<td><p>Необязательно</p></td>
<td><p>False</p></td>
<td><p>SASL по протоколу TLS</p></td>
<td><div>

> [!WARNING]  
> Для SASL требуется TLS. Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.


</div></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>Необязательно </p></td>
<td><p>Верно</p></td>
<td><p>TCP Dialback</p></td>
<td><div>

> [!WARNING]  
> Для SASL требуется TLS. Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.


</div></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>Необязательно </p></td>
<td><p>False</p></td>
<td><div>

> [!WARNING]  
> Недействительная конфигурация


</div></td>
<td><div>

> [!WARNING]  
> Для SASL требуется TLS. Если вы разрешаете использовать TLS, может возникнуть сбой согласования сеанса.


</div></td>
</tr>
<tr class="odd">
<td><p>Обязательный</p></td>
<td><p>Не поддерживается</p></td>
<td><p>Верно</p></td>
<td><p>TLS Dialback</p></td>
<td><p>Настройка позволяет TLS Dialback.</p></td>
</tr>
<tr class="even">
<td><p>Обязательный</p></td>
<td><p>Не поддерживается</p></td>
<td><p>False</p></td>
<td><p>Недействительная конфигурация</p></td>
<td><div>

> [!WARNING]  
> Необходимо включить SASL или Dialback.


</div></td>
</tr>
<tr class="odd">
<td><p>Необязательно </p></td>
<td><p>Не поддерживается</p></td>
<td><p>Верно</p></td>
<td><p>TLS Dialback, TCP Dialback</p></td>
<td><p>На основе вариантов согласования для другой конечной точки, TCP или TLS Dialback будут приняты.</p></td>
</tr>
<tr class="even">
<td><p>Необязательно </p></td>
<td><p>Не поддерживается</p></td>
<td><p>False</p></td>
<td><p>Недействительная конфигурация</p></td>
<td><div>

> [!WARNING]  
> Необходимо включить SASL или Dialback.


</div></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>Не поддерживается</p></td>
<td><p>Верно</p></td>
<td><p>TCP Dialback</p></td>
<td><p>Протокол TCP Dialback является единственным доступным способом согласования</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>Не поддерживается</p></td>
<td><p>False</p></td>
<td><p>Недействительная конфигурация</p></td>
<td><div>

> [!WARNING]  
> Необходимо включить SASL или Dialback.


</div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

