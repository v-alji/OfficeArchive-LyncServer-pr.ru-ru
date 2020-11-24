---
title: 'Lync Server 2013: замена XmlAdapter с настроенным адаптером соответствия для сервера сохраняемого чата'
description: 'Lync Server 2013: замена XmlAdapter с настроенным адаптером соответствия для сервера сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter
ms:assetid: 2cb70db2-663f-40a6-abcf-89ea7d4a8b65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ680106(v=OCS.15)
ms:contentKeyID: 49558152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a90b4df7df42ffdc6c55e9b551b0eb53d07ab1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398977"
---
# <a name="replacing-the-xmladapter-with-a-customized-persistent-chat-server-compliance-adapter-in-lync-server-2013"></a>Замена XmlAdapter с помощью настроенного адаптера соответствия требованиям сервера для подключения к серверу в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Вы можете написать собственный адаптер, вместо того чтобы использовать XmlAdapter, установленный на сервере сохраняемого чата. Для этого необходимо предоставить сборку .NET Framework, которая содержит общий класс, реализующий интерфейс **IComplianceAdapter**. Эту сборку необходимо поместить в папку установки сервера сохраняемого чата для каждого сервера в пуле сервера сохраняемого чата. Данные проверки совместимости могут поступать в адаптер с любого сервера проверки совместимости, но на разные экземпляры адаптера с серверов проверки совместимости на поступают повторяющиеся данные.

<div>

## <a name="implementing-the-icomplianceadapter-interface"></a>Реализация интерфейса IComplianceAdapter

Интерфейс определен в сборке Compliance.dll в пространстве имен `Microsoft.Rtc.Internal.Chat.Server.Compliance` . Интерфейс определяет два метода, которые должен реализовать пользовательский адаптер.

    void SetConfig(AdapterConfig config)

Этот метод будет вызываться при первой загрузке адаптера с помощью постоянного чата. `AdapterConfig`Содержит постоянную конфигурацию соответствия чатов, связанную с адаптером соответствия требованиям.

    void Translate(ConversationCollection conversations)

Сервер соответствия требованиям в чате вызывает этот метод через определенные интервалы времени, пока для перевода не поступило новых данных. Этот интервал времени равен значению, заданному в параметрах `RunInterval` соответствия требованиям сохраняемого чата.

`ConversationCollection`Содержит сведения о разговоре, собранные с момента последнего вызова этого метода.

</div>

</div>

<span> </span>

</div>

</div>

</div>

