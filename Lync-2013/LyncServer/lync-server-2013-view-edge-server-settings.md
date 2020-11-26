---
title: 'Lync Server 2013: Просмотр параметров пограничного сервера'
description: 'Lync Server 2013: Просмотр параметров пограничного сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Edge Server settings
ms:assetid: 684154cc-cffc-4d2e-8baa-be52c625e5d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747890(v=OCS.15)
ms:contentKeyID: 63969612
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4318b8c97f53f267bb79953af504977f6437214d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446287"
---
# <a name="view-edge-server-settings-in-lync-server-2013"></a>Просмотр параметров пограничного сервера в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-05-20_

Общие конфигурации пограничного сервера следует проверять на основе данных в базе данных управления конфигурацией, чтобы гарантировать, что все изменения будут документированы в соответствии с определенными процедурами управления изменениями.

Дополнительные проверки могут включать в себя те, которые описаны в следующих разделах:

<div>

## <a name="verify-the-allow-and-block-lists"></a>Проверка списка разрешенных и заблокированных списков

Убедитесь, что указанные пространства имен по-прежнему являются допустимыми списками URI SIP "Allow" и "Block" для федеративных доменов.

Вы можете использовать Windows PowerShell для просмотра списка разрешенных и заблокированных списков. Чтобы просмотреть домены в списке разрешенные домены, выполните следующую команду Windows PowerShell:

`Get-CsAllowedDomain`

Эта команда возвращает сведения о доменах в списке разрешенные домены, как показано ниже.

Identity: contoso.com

Domain (домен): contoso.com

ProxyFqdn :

Примечания

MarkForMonitoring: false

Примечания

Чтобы просмотреть домены в списке блокируемых доменов, используйте следующую команду:

`Get-CsBlockedDomain`

В свою очередь, вы получите такие сведения, как, например, для всех блокируемых доменов.

Identity: tailspintoys.com

Domain (домен): tailspintoys.com

Кроме того, Windows PowerShell позволяет убедиться, что вы можете подключиться к доменам в списке разрешенные домены. Например, эта команда проверяет соединение между пограничным сервером (TargetFqdn) и федеративным доменом contoso.com:

`Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"`

Эта команда проверяет подключение между пограничным сервером и всеми доменами, которые находятся в списке разрешенных доменов:

`Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Domain}`

</div>

<div>

## <a name="verify-multiple-edge-servers-are-identical"></a>Проверка того, что несколько пограничных серверов идентичны

Если в массиве с балансировкой нагрузки развернут несколько пограничных серверов, мы рекомендуем проверить, настроены ли все пограничные серверы в массиве одинаковым образом.

Параметры для пограничных серверов можно просмотреть в области сведений в расширении Lync Server 2013 для оснастки управления компьютером.

</div>

<div>

## <a name="see-also"></a>См. также


[Get-CsAllowedDomain](https://docs.microsoft.com/powershell/module/skype/Get-CsAllowedDomain)  
[Get-CsBlockedDomain](https://docs.microsoft.com/powershell/module/skype/Get-CsBlockedDomain)  
[Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

