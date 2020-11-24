---
title: Настройка политик доступа и сертификатов шлюза XMPP
description: Настройте политики доступа к шлюзу XMPP и сертификаты.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure XMPP gateway access policies and certificates
ms:assetid: fac02f4e-d14d-4be3-b53c-74c82436fd93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721945(v=OCS.15)
ms:contentKeyID: 49733882
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e958100501ad9ca87d1ab970162f4be8c7692a99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398356"
---
# <a name="configure-xmpp-gateway-access-policies-and-certificates"></a>Настройка политик доступа и сертификатов шлюза XMPP

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-15_

XMPP Федерация определяет внешнее развертывание на основе расширяемого протокола обмена сообщениями и присутствия (XMPP). Конфигурация XMPP позволяет пользователям Lync получать доступ к XMPP доменам, выполнив указанные ниже действия.

  - Обмен сообщениями и присутствие — только для человека

  - Создание федеративных контактов XMPP в клиенте Lync

Если вы настраиваете политики для поддержки федеративных партнеров по протоколу расширенного обмена сообщениями (XMPP), политики применяются к пользователям XMPP федеративных доменов, но не к пользователям служб мгновенных сообщений в протоколе SIP (например, Windows Live) или федеративных доменах SIP. Вы настраиваете федеративного партнера XMPP для каждого XMPP федеративного домена, с которым вы хотите разрешить пользователям добавлять контакты и взаимодействовать с ними. После того как политики будут установлены, необходимо настроить сертификаты шлюза XMPP.

<div>


> [!NOTE]  
> Чтобы начать миграцию шлюза XMPP, необходимо развернуть шлюз Lync Server 2013 XMPP и настроить политики доступа, чтобы включить пользователей для Lync Server 2013 XMPP Gateway. Перед выполнением описанных ниже действий необходимо переместить всех пользователей в развертывание Lync Server 2013. Подробности можно найти <A href="configure-xmpp-gateway-on-lync-server-2013.md">в разделе Настройка шлюза XMPP на Lync Server 2013</A>.



</div>

<div>

## <a name="configure-an-external-access-policy-to-enable-users-for-lync-server-2013-xmpp-gateway"></a>Настройка политики внешнего доступа для поддержки пользователей Lync Server 2013 XMPP Gateway

1.  Откройте Панель управления Lync Server.

2.  На панели навигации слева выберите пункт **интеграция и внешний доступ**, а затем — **Политика внешнего доступа**.

3.  Нажмите кнопку **создать** , а затем выберите пункт **Политика пользователя**.

4.  Введите имя для политики пользователей внешнего доступа.

5.  Введите описание для политики пользователей внешнего доступа.

6.  Выберите **включить связь с федеративными пользователями**.

7.  Выберите **включить связь с федеративными пользователями XMPP**.

8.  Нажмите **кнопку Сохранить,** чтобы сохранить изменения в политике сайта или пользователя.

</div>

</div>

<span> </span>

</div>

</div>

</div>

