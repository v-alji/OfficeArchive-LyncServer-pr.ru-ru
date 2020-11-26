---
title: 'Lync Server 2013: Просмотр сведений о параметрах конфигурации Lync Phone Edition'
description: 'Lync Server 2013: Просмотр сведений о параметрах конфигурации Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Lync Phone Edition configuration settings information
ms:assetid: 15f94478-651f-4063-9918-6a059f98df16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687976(v=OCS.15)
ms:contentKeyID: 49733564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62719b24920ee72a92b2f80498d5ea2a59288c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440418"
---
# <a name="view-lync-phone-edition-configuration-settings-information-in-lync-server-2013"></a>Просмотр сведений о параметрах конфигурации Lync Phone Edition в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Вы можете просматривать сведения о конфигурации устройств, работающих под управлением Lync Phone Edition. Информация организована в коллекции. При установке сервера Lync Server вы получаете коллекцию параметров Lync Phone Edition, которые применяются ко всем устройствам, использующим Lync Phone Edition в развертывании. Вы также можете создать новые наборы параметров для определенного сайта. Параметры сайта имеют приоритет над глобальными параметрами. Каждая коллекция параметров состоит из имени, области (глобального или сайта), настройки безопасности SIP, уровня ведения журнала, настройки качества обслуживания голоса, параметров блокировки телефона и сведений о блокировке телефона, то есть минимальной длины персонального идентификационного номера (ПИН-кода) и времени до тех пор, пока телефон не будет заблокирован.

<div>

## <a name="to-view-configuration-information-about-devices-running-lync-phone-edition"></a>Просмотр сведений о конфигурации устройств с Lync Phone Edition

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите пункт **Клиенты**, а затем нажмите кнопку Навигация по **конфигурации устройства** .

4.  На странице **Конфигурация устройства** выберите коллекцию параметров, сведения о которых вы хотите просмотреть. На главной странице указаны имя, область, параметры безопасности SIP, уровень качества голоса и параметры блокировки телефона. Чтобы просмотреть сведения о уровне ведения журнала и блокировки телефона, щелкните меню " **Правка** ", а затем выберите команду **Показать подробности**.

</div>

<div>

## <a name="viewing-lync-phone-edition-configuration-information-by-using-windows-powershell-cmdlets"></a>Просмотр сведений о конфигурации Lync Phone Edition с помощью командлетов Windows PowerShell

Вы можете просматривать параметры конфигурации Lync Phone Edition с помощью командной консоли Lync Server Management Shell и командлета **Get-CsUCPhoneConfiguration** . Этот командлет можно запустить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-lync-phone-edition-configuration-information"></a>Просмотр сведений о конфигурации Lync Phone Edition

  - Чтобы просмотреть сведения о всех параметрах конфигурации Lync Phone Edition, введите в командной консоли Lync Server указанную ниже команду и нажмите клавишу ВВОД.
    
        Get-CsUCPhoneConfiguration
    
    Команда возвращает данные, подобные приведенным ниже.
    
        Identity             : Global
        CalendarPollInterval : 00:03:00
        EnforcePhoneLock     : True
        PhoneLockTimeout     : 00:10:00
        MinPhonePinLength    : 6
        SIPSecurityMode      : High
        VoiceDiffServTag     : 40
        Voice8021p           : 0
        LoggingLevel         : Off

</div>

Подробности можно найти в [статьях Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).

</div>

<div>

## <a name="see-also"></a>См. также


[Создание и изменение коллекции параметров конфигурации Lync Phone Edition в Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md)  
[Удаление существующей коллекции параметров конфигурации Lync Phone Edition в Lync Server 2013](lync-server-2013-delete-an-existing-collection-of-lync-phone-edition-configuration-settings.md)  
[Настройка параметров безопасности для Lync Phone Edition в Lync Server 2013](lync-server-2013-configure-security-settings-for-lync-phone-edition.md)  
[Принудительная Блокировка телефона в Lync Server 2013](lync-server-2013-enforce-phone-locking.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

