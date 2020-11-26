---
title: Настройка различных политик
description: Настройка различных политик.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring the Various Policies
ms:assetid: e3b3cbda-7c17-470b-acb0-82fdcc473184
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945610(v=OCS.15)
ms:contentKeyID: 51541436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 746d299ac605c7dfe89a957246d47309dfbc0a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440063"
---
# <a name="configuring-the-various-policies"></a>Настройка различных политик

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-24_

<div>

Ниже приведены различные политики, которые можно настроить в топологии Lync Server 2013 перед запуском средства нагрузки и производительности Lync Server 2013.

<div>

## <a name="configuring-the-archiving-policy"></a>Настройка политики архивации

Просмотрите пример сценария ArchivingPolicy.ps1. Этот сценарий следует использовать только в том случае, если в вашей топологии развернут сервер архивирования. Дополнительные сведения можно найти в документации по Lync Server 2013 и командлетов для [архивации и мониторинга командлетов в Lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a>Настройка политики конференц-связи

Просмотрите пример сценария MeetingPolicy.ps1. Дополнительные сведения можно найти в документации Lync Server 2013 и в справке по командлетам [веб-конференций в Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-contacts-policy"></a>Настройка политики контактов

Посмотрите пример ContactsPolicy.ps1. Подробные сведения можно найти в документации Lync Server 2013 и в справке по командлетам для [обмена мгновенными сообщениями и проверки присутствия в Lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-federation-policy"></a>Настройка политики Федерации

Посмотрите пример FederationPolicy.ps1. Дополнительные сведения можно найти в документации по Lync Server 2013 и о командлетах [пограничного сервера в командлетах Lync server 2013](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) и [Федерации и внешнего доступа в Lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a>Настройка политики управления допуском звонков

Посмотрите пример BandwidthPolicy.ps1. Дополнительные сведения можно найти в документации Lync Server 2013, посвященной [управлению допуском звонков в Lync server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) , и Справка по командлетам [управления допуском звонков в Lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a>Настройка правил для маршрутизации голосовых сообщений

Посмотрите пример RoutingRules.ps1. Настроив правила маршрутизации голосовой связи, запишите контекст телефона (то есть,/Location Profile или/SimpleName), а также внутренние и внешние коды города, чтобы их можно было указывать при создании пользователей и настройке конфигурации LyncPerfTool (специально для PSTN-UC и UC-КТСОП). Например, параметр SimpleName в вызове командлета **New-CsDialPlan** в примере RoutingRules.ps1 следует использовать для значения LocationProfile на следующем рисунке UserProfileGenerator.exe.

![Правило маршрутизации образца записи голоса.](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Правило маршрутизации образца записи голоса.")

Дополнительные сведения можно найти в документации по Lync Server 2013 и о командлетах для [корпоративных голосовых команд в Lync server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a>Настройка приложения-участника конференц-связи

Посмотрите пример ConferenceAutoAttendantConfiguration.ps1. Обратите внимание на ConferencingAutoAttendant номер телефона (1121111111 по умолчанию), чтобы можно было ввести его в средство настройки средств LyncPerf для создания конфигурации.

![Конфигурация приложения Conferencing Attendant](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Конфигурация приложения Conferencing Attendant")

Дополнительные сведения можно найти в документации Lync Server 2013 и в разделе Справка по командлетам для [веб-конференций в](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) lync Server 2013 и [командлетах конференции с телефонным подключением в Lync сервер 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a>Настройка службы приостановки звонков в Lync Server

По умолчанию метод приостановки звонка отключен. Посмотрите пример CallParkConfiguration.ps1. Дополнительные сведения можно найти в документации по Lync Server 2013 и о командлетах [приложения для приостановки звонков в Lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-emergency-calls"></a>Настройка экстренных вызовов

Выполните указанные ниже действия, чтобы настроить стресс и тестирование производительности для экстренных вызовов.

1.  Настройте голосовой маршрут для вызова экстренной помощи. Пример настройки этого голосового маршрута можно найти в RoutingRules.ps1 сценарии под комментарием "Route E911 to КТСОП".
    
    <div>
    

    > [!WARNING]  
    > Пример команды в RoutingRules.ps1 имеет числовой шаблон, который включает число 119, а не 911. Следует избегать использования 911 (или фактического местного номера для экстренного реагирования), чтобы предотвратить случайные вызовы локальных аварийных операторов в ходе нагрузочного тестирования. Эта конфигурация предназначена только для целей моделирования.

    
    </div>

2.  Настройте адреса, заполнив значения на вкладке **LIS** в UserProvisioningTool, как показано на приведенном ниже рисунке.
    
    ![Конфигурация сервиса данных о местоположении.](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Конфигурация сервиса данных о местоположении.")  

3.  Щелкните **создать файлы конфигурации LIS**.

4.  Создаются файлы CSV для портов, подсетей, переключателей и точек доступа к беспроводной сети (WAPs), а также XML-файла для средства нагрузки и производительности Lync Server 2013. CSV-файлы будут использоваться в качестве входных данных (в той же папке) при настройке службы сведений о расположении (LIS) со сценарием LisConfiguration.ps1. Переместите созданный Locations0.xml файл в ту же папку, в которой находится исполняемая программа Lync Server 2013 (LyncPerfTool.exe), которая будет запускать сценарии для профилей местоположений (абонентской группы).

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a>Создание, включение, Настройка и отключение пользователей

Перед выполнением следующих сценариев необходимо создать все пользователи. Следуйте инструкциям в разделе [Создание пользователей и контактов](create-users-and-contacts.md) , чтобы создать пользователей. Дополнительные сведения можно найти в документации по командлетам Lync Server 2013 для командлетов [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)), [Set-CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))и [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) .

</div>

<div>

## <a name="configuring-response-group-application"></a>Настройка приложения группы ответа

Посмотрите пример ResponseGroupConfiguration.ps1. Дополнительные сведения можно найти в документации по Lync Server 2013 и о командлетах [приложения группы ответа в Lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)). Чтобы просмотреть конфигурацию приложения группы ответа, посмотрите `https://<poolfqdn>/RgsConfig/` , как показано на рисунке ниже.

![Инструмент Response Group Configuration Tool.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "Инструмент Response Group Configuration Tool.")

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

