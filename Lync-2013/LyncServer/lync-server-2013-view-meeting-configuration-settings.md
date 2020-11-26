---
title: 'Lync Server 2013: Просмотр параметров конфигурации собраний'
description: 'Lync Server 2013: Просмотр параметров конфигурации собраний.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View meeting configuration settings
ms:assetid: d03a4684-9d8b-4728-917d-5b5c91511e2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721894(v=OCS.15)
ms:contentKeyID: 49733828
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 190b9d331a8cd0a08e17c482dbc3b0bc27590003
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446978"
---
# <a name="view-meeting-configuration-settings-in-lync-server-2013"></a>Просмотр параметров конфигурации собрания в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

В панели управления Lync Server 2013 вы можете управлять реализацией собраний в развертывании с помощью параметров настройки собраний. Сюда входят следующие конфигурации собрания:

  - Глобальная конфигурация, создаваемая по умолчанию при развертывании Lync Server 2013.

  - Необязательные конфигурации уровня сайта и уровня пользователя, которые можно создать и использовать для определения способа реализации собраний для конкретных сайтов или пользователей.

<div>

## <a name="to-view-meeting-configuration-settings"></a>Просмотр параметров конфигурации собрания

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите **Конференц** -связь, а затем — **Конфигурация собрания**.

4.  На странице **Конфигурация собрания** (Конфигурация собраний) щелкните конфигурацию собраний, которую требуется просмотреть.

5.  В окне " **Изменение фильтра файлов**" выберите **Показать подробности...** флажок.
    
    **Изменение конфигурации собрания — \<policy\>** Открытие отображения параметров выбранной политики. Сведения о настройке параметров можно найти в разделе [Создание или изменение коллекции параметров конфигурации собраний в Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md).

</div>

<div>

## <a name="viewing-meeting-configuration-information-by-using-windows-powershell-cmdlets"></a>Просмотр сведений о конфигурации собраний с помощью командлетов Windows PowerShell

Параметры конфигурации собраний можно просматривать с помощью Windows PowerShell и командлета Get-CsMeetingConfiguration. Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-meeting-configuration-information"></a>Просмотр сведений о настройке собрания

  - Чтобы просмотреть сведения о всех параметрах конфигурации собрания, введите в командной консоли Lync Server указанную ниже команду и нажмите клавишу ВВОД.
    
        Get-CsMeetingConfiguration
    
    Команда возвращает примерно следующую информацию:
    
        Identity                        : Global
        PstnCallersBypassLobby          : True
        EnableAssignedConferenceType    : True
        DesignateAsPresenter            : Company
        AssignedConferenceTypeByDefault : True
        AdmitAnonymousUsersByDefault    : True
        RequireRoomSystemsAuthorization : False
        LogoURL                         :
        LegalURL                        :
        HelpURL                         :
        CustomFooterText                :
        AllowConferenceRecording        : True

</div>

Дополнительные сведения можно найти в разделе справки по командлету [Get-CsMeetingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

