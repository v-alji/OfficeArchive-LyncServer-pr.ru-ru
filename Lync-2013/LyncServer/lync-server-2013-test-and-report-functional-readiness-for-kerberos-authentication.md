---
title: Проверка и отчет о функциональной готовности для использования проверки подлинности Kerberos
description: Тестирование и создание отчетов о готовности проверки подлинности Kerberos.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test and report functional readiness for Kerberos authentication
ms:assetid: d52c39e5-747d-4f29-88aa-30fd6f26b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398925(v=OCS.15)
ms:contentKeyID: 48185519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d32591a8cced7dce2e0bb78cc26189dce1900a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444303"
---
# <a name="test-and-report-functional-readiness-for-kerberos-authentication-in-lync-server-2013"></a>Проверка и отчет о функциональной готовности для использования проверки подлинности Kerberos в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-01-16_

Для успешного выполнения этой процедуры необходимо войти в систему в качестве пользователя, который является членом группы RTCUniversalServerAdmins.

С помощью командлета Windows PowerShell **Test-CsKerberosAccountAssignment** можно протестировать и сообщить о готовности назначения сайта для проверки подлинности Kerberos. Эта команда отправляет запрос на сайт, указанный в требуемом параметре удостоверения. Необязательный параметр отчета заставляет командлет записать отчет в формате HTML в C: \\ журналы на компьютере, на котором она выполняется. Необязательный параметр подробной информации выводит сведения о действиях на экран.

<div>

## <a name="to-test-and-report-functional-readiness-for-kerberos-authentication-for-a-site"></a>Тестирование и создание отчетов о готовности проверки подлинности Kerberos для сайта

1.  Войдя в группу RTCUniversalServerAdmins, войдите в домен на компьютере с Lync Server 2013 или на компьютер, на котором установлены средства администрирования.

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  В командной строке выполните следующую команду:
    
        Test-CsKerberosAccountAssignment -Identity "site:SiteName" -Report "c:\logs\FileName.htm" -Verbose
    
    Например:
    
        Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "c:\logs\KerberosReport.htm" -Verbose

</div>

</div>

<span> </span>

</div>

</div>

</div>

