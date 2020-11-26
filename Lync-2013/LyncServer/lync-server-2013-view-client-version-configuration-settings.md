---
title: 'Lync Server 2013: Просмотр параметров конфигурации версии клиента'
description: 'Lync Server 2013: Просмотр параметров конфигурации версии клиента.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View client version configuration settings
ms:assetid: c72df4e6-a889-4cb6-86f7-8334d7774c6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ923062(v=OCS.15)
ms:contentKeyID: 50675353
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04fc25a1ab4904cbc6ca7871e1568ac8bc488bdf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443421"
---
# <a name="view-client-version-configuration-settings-in-lync-server-2013"></a>Просмотр параметров конфигурации клиентской версии в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Параметры конфигурации используются для включения и отключения управления версиями клиентов. Конфигурация глобальной версии клиента устанавливается вместе с Lync Server 2013 и используется для включения или отключения управления версиями для всего развертывания сервера. Когда включена глобальная конфигурация, при попытке пользователя войти в систему применяются все заданные политики версий клиентов. Вы можете просматривать параметры конфигурации для версии клиента с панели управления Lync Server 2013 или оболочки управления Lync Server 2013.

<div>


> [!NOTE]  
> Поскольку анонимные пользователи не связаны с пользователями, сайтами или службами, к ним могут применяться только политики глобального уровня.



</div>

<div>

## <a name="to-view-client-version-configuration-settings-by-using-lync-server-control-panel"></a>Просмотр параметров конфигурации клиентской системы с помощью панели управления Lync Server

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите пункт **Клиенты**, а затем нажмите кнопку Навигация по **конфигурации версии клиента** .

4.  Дважды щелкните имя конфигурации клиентской версии, которую вы хотите просмотреть.

</div>

<div>

## <a name="viewing-client-version-configuration-settings-by-using-windows-powershell-cmdlets"></a>Просмотр параметров конфигурации клиентской версии с помощью командлетов Windows PowerShell

С помощью командлета **Get-CsClientVersionConfiguration** можно просмотреть параметры конфигурации клиентской версии. Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-client-version-configuration-information"></a>Просмотр сведений о конфигурации клиентской версии

  - Чтобы просмотреть сведения о всех параметрах конфигурации клиента, введите следующую команду в командной консоли Lync Server Management Shell и нажмите клавишу ВВОД.
    
        Get-CsClientVersionConfiguration
    
    Команда возвращает примерно следующую информацию:
    
        Identity      : Global
        DefaultAction : Allow
        DefaultURL    :
        Enabled       : True

</div>

Дополнительные сведения можно найти в разделе справки по командлету [Get-CsClientVersionConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsClientVersionConfiguration) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

