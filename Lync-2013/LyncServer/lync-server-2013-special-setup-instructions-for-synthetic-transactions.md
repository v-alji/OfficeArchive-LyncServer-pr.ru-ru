---
title: 'Lync Server 2013: специальные инструкции по настройке для виртуальных операций'
description: 'Lync Server 2013: специальные инструкции по настройке для виртуальных операций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Special setup instructions for synthetic transactions
ms:assetid: 694cbe05-5dba-4035-a01c-c87ebfb0478b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688080(v=OCS.15)
ms:contentKeyID: 49733676
ms.date: 11/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e288a9d7f15f4b84df591d152a912509c77129a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441601"
---
# <a name="special-setup-instructions-for-synthetic-transactions-in-lync-server-2013"></a>Специальные инструкции по настройке для виртуальных транзакций в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2015-11-16_

Большинство искусственных транзакций могут выполняться на узле наблюдателя как есть; Это значит, что при добавлении виртуальной транзакции в параметры конфигурации узла-наблюдателя узел-наблюдатель может приступить к использованию искусственной транзакции во время тестовых этапов. Однако это не справедливо для всех виртуальных транзакций. Исключения — искусственные транзакции, требующие специальных инструкций по настройке — рассматриваются в следующих разделах.

<div>

## <a name="dealing-with-server-timeout-errors"></a>Работа с ошибками времени ожидания сервера

В некоторых случаях вы можете столкнуться со сбоем виртуальных транзакций с ошибками таймаута сервера (код ошибки 504). Эти ошибки обычно возникают из-за проблем с брандмауэром. При выполнении искусственной транзакции эта транзакция выполняется в MonitoringHost.exe процессе. в свою очередь MonitoringHost.exe запускает экземпляр PowerShell.exe процесса. Если ваш брандмауэр блокирует MonitoringHost.exe или PowerShell.exe, искусственная транзакция завершится сбоем и создаст ошибку 504.

Чтобы устранить эту проблему, необходимо вручную создать правила брандмауэра для входящих подключений для MonitoringHost.exe и PowerShell.exe на локальном компьютере. Это можно сделать с помощью брандмауэра Windows или стороннего местного межсетевого экрана в зависимости от конфигурации, установленной на сервере.

Если вы используете сетевое подключение устройства между хост-компьютером виртуальной транзакции и серверами Lync, которые вы пытаетесь отслеживать, вы должны считать его клиентским компьютером, а все требования к порту [и протоколам для внутренних серверов в Lync Server 2013](lync-server-2013-ports-and-protocols-for-internal-servers.md).

</div>

<div>

## <a name="data-conferencing-synthetic-transactions"></a>Синтетические транзакции для конференций с данными

Если компьютер-наблюдатель находится за пределами сети периметра, возможно, вы не сможете выполнить виртуальную транзакцию для конференц-связи с данными, если только вы не отключите параметры прокси-сервера Internet Explorer для учетной записи сетевой службы. Чтобы отключить параметры прокси-сервера для этой службы, выполните указанные ниже действия.

1.  На компьютере с узлом-наблюдателем нажмите кнопку **Пуск**, **выберите все программы**, затем **стандартные**, щелкните правой кнопкой мыши **Командная строка** и выберите пункт **Запуск от имени администратора**.

2.  В окне консоли введите указанную ниже команду и нажмите клавишу ВВОД.
    
        bitsadmin /util /SetIEProxy NetworkService NO_PROXY

В окне командной строки появится следующее сообщение:

    BITSAdmin is deprecated and is not guaranteed to be available in future versions of Windows. Administration tools for the BITS service are now provided by BITS PowerShell cmdlets.
    
    Internet proxy settings for account NetworkService set to NO_PROXY. 
    (connection = default)

Это сообщение означает, что вы отключили параметры прокси-сервера Internet Explorer для учетной записи сетевой службы.

</div>

<div>

## <a name="exchange-unified-messaging-synthetic-transactions"></a>Синтетические транзакции в единой системе обмена сообщениями Exchange

Искусственная транзакция обмена сообщениями Exchange (UM) проверяет, что тестовые пользователи могут подключаться к учетным записям голосовой почты, которые размещаются в Exchange. Эти тестовые пользователи должны быть предварительно настроены с учетными записями голосовой почты, прежде чем они смогут использовать проверки UM Exchange.

</div>

<div>

## <a name="persistent-chat-synthetic-transactions"></a>Синтетическые транзакции для сохраняемого чата

Для использования искусственной транзакции "сохраняемый чат" администраторам необходимо сначала создать канал, а также дать тестовым пользователям разрешения на его использование. Командлет [Test-CsPersistentChatMessage](https://docs.microsoft.com/powershell/module/skype/Test-CsPersistentChatMessage) можно использовать для правильной настройки этих тестовых пользователей.

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-cs-001.litwareinc.com -SenderSipAddress sip:kenmyer@litwareinc.com -SenderCredential $cred1 -ReceiverSipAddress sip:pilar@litwareinc.com -ReceiverCredential $cred2 -TestUser1SipAddress sip:kenmyer@litwareinc.com -TestUser2SipAddress sip:pilar@litwareinc.com -Setup $True

Эта задача по установке должна выполняться в рамках предприятия.

  - При запуске с несерверного компьютера пользователь, который запускает командлет, должен быть членом роли PersistentChatAdministrators для управления доступом Role-Based (RBAC).

  - При запуске с сервера сам пользователь, который запускает командлет, должен быть членом группы RTCUniversalServerAdmins.

В приведенной выше команде параметр настройки включен и имеет значение true ($True). Если вы включите параметр настройки, Test-CsPersistentChatMessage создаст специальную комнату для чата и заполните ее с помощью тестовых пользователей. Это поможет удостовериться в том, что в настоящее время есть комната чата в целях тестирования. Обратите внимание, что параметр Setup должен выполняться только с сервера переднего плана.

Комната чата, созданная Test-CsPersistentChatMessage, может быть удалена только администратором.

</div>

<div>

## <a name="pstn-peer-to-peer-call-synthetic-transactions"></a>Синтетические транзакции одноранговых вызовов PSTN

Синтетические транзакции [Test-CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall) проверяют возможность размещения и приема звонков через коммутируемую телефонную сеть общего пользования (КТСОП).

Для выполнения этой искусственной транзакции администраторы должны настроить следующие параметры:

  - Два тестовых пользователя (вызывающего абонента и приемника), разрешенные для корпоративной голосовой связи.

  - Прямые входные номера для каждой учетной записи пользователя.

  - Голосовые и видеомаршрутные политики, позволяющие звонить по номеру приемника для доступа к шлюзу PSTN.

  - Шлюз PSTN, принимающий звонки, и носители, которые перенаправляют вызовы обратно на пул домашнего пула получателя в соответствии с набранным номером.

</div>

<div>

## <a name="unified-contact-store-synthetic-transactions"></a>Синтетические транзакции в магазине контактов

Виртуальная транзакция в магазине единой системы обмена сообщениями удостоверяется в том, что Lync Server 2013 может получать контакты от имени пользователя из Microsoft Exchange Server 2013.

Чтобы использовать эту искусственную транзакцию, следует выполнить следующие условия:

  - [Управление проверкой подлинности между сервером (OAuth) и приложениями-партнерами в Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) должно быть настроено между lync Server 2013 и Exchange 2013.

  - Тестовые пользователи должны иметь действительный почтовый ящик Exchange 2013.

После того как эти условия будут выполнены, администраторы могут выполнить следующую команду, чтобы убедиться в том, что пользователь с SIP Address kenmyer@litwareinc.com может получать свои контакты из хранилища единого контакта:

    Test-CsUnifiedContactStore -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -RegistrarPort 5061 -Authentication TrustedServer -Setup

Обратите внимание на использование параметра настройки, используемого в предыдущей команде. Если параметр настройки включается при запуске Test-CsUnifiedContactStore то указанные контакты пользователя (в данном случае — sip:kenmyer@litwareinc.com) будут перемещены в единое хранилище контактов. (Разумеется, если контакты пользователя уже находятся в едином хранилище контактов, они не нужно перемещать.) Параметр "Настройка" обычно используется только один раз (при первом запуске Test-CsUnifiedContactStore), и его следует использовать только с тестами пользователей; то есть учетные записи пользователей, которые никогда не будут входить на сервер Lync Server. После того как тестовый пользователь будет перенесен в единое хранилище контактов, вы можете убедиться, что контакты пользователя можно получить, вызвав Test-CsUnifiedContactStore без параметра установки:

    Test-CsUnifiedContactStore -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -RegistrarPort 5061 -Authentication TrustedServer

</div>

<div>

## <a name="xmpp-synthetic-transactions"></a>XMPP Синтетическые транзакции

Для искусственной транзакции обмена мгновенными сообщениями в XMPP (Extensible Mailing Protocol и присутствие) необходимо, чтобы функция XMPP была настроена с использованием одного или нескольких федеративных доменов.

Чтобы включить виртуальную транзакцию XMPP, необходимо указать параметр XmppTestReceiverMailAddress с учетной записью пользователя в маршрутизируемой XMPP домене. Например:

    Set-CsWatcherNodeConfiguration -Identity pool0.contoso.com -Tests @{Add="XmppIM"} -XmppTestReceiverMailAddress user1@litwareinc.com

В этом примере для маршрутизации сообщений для litwareinc.com на шлюз XMPP необходимо наличие правила Lync Server 2013.

</div>

</div>

<span> </span>

</div>

</div>

</div>

