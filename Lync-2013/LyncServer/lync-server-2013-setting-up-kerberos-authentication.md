---
title: 'Lync Server 2013: настройка проверки подлинности Kerberos'
description: 'Lync Server 2013: Настройка проверки подлинности Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication
ms:assetid: dd8009ef-6265-4cc0-b2c7-e474cd1f4b09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398976(v=OCS.15)
ms:contentKeyID: 48185601
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb461968bc073edbfe640f609257f3e84c192461
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441720"
---
# <a name="setting-up-kerberos-authentication-in-lync-server-2013"></a>Настройка проверки подлинности Kerberos в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-21_

Lync Server 2013 поддерживает проверку подлинности NTLM и Kerberos для веб-служб. Office Communications Server 2007 и Office Communications Server 2007 R2 использовали параметры по умолчанию RTCComponentService и RTCService для учетных записей пользователей для выполнения пулов приложений веб-служб, позволяя назначать имена участников служб (SPN) учетным записям пользователей и выступать в качестве участника проверки подлинности. Lync Server использует сетевую службу для работы веб-служб и NetworkService не может назначать ей SPN.

Чтобы решить проблему, не позволяющую объектам Active Directory хранить SPN, панель управления Lync Server может использовать объекты учетной записи компьютера для этой цели. Объекты учетной записи компьютера могут содержать имена участников службы и не могут быть причиной истечения срока действия пароля, которая была связана с использованием учетных записей пользователей в предыдущих версиях.

Вы можете использовать командлеты Windows PowerShell для настройки объектов компьютера для обеспечения проверки подлинности Kerberos.

<div>

## <a name="in-this-section"></a>Содержание

  - [Необходимые условия для включения проверки подлинности Kerberos в Lync Server 2013](lync-server-2013-prerequisites-for-enabling-kerberos-authentication.md)

  - [Создание учетной записи для проверки подлинности Kerberos в Lync Server 2013](lync-server-2013-create-a-kerberos-authentication-account.md)

  - [Назначение учетной записи проверки подлинности Kerberos для сайта в Lync Server 2013](lync-server-2013-assign-a-kerberos-authentication-account-to-a-site.md)

  - [Настройка паролей учетных записей проверки подлинности Kerberos в Lync Server 2013](lync-server-2013-setting-up-kerberos-authentication-account-passwords.md)

  - [Добавление в Lync Server 2013 проверки подлинности Kerberos для других сайтов](lync-server-2013-add-kerberos-authentication-to-other-sites.md)

  - [В Lync Server 2013 удаление проверки подлинности Kerberos для сайта](lync-server-2013-remove-kerberos-authentication-from-a-site.md)

  - [Тестирование и отчет о состоянии и назначении проверки подлинности Kerberos в Lync Server 2013](lync-server-2013-testing-and-reporting-the-status-and-assignment-of-kerberos-authentication.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

