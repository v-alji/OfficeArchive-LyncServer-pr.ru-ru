---
title: 'Lync Server 2013: проверка доступа через обратный прокси-сервер'
description: 'Lync Server 2013: Проверка доступа с помощью обратного прокси-сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify access through your reverse proxy
ms:assetid: 3076a786-e022-4d41-91ec-1bf252b2a468
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429697(v=OCS.15)
ms:contentKeyID: 48183753
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593aac5574f0dcf683351f12a6392f6116480ac5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443477"
---
# <a name="verify-access-through-your-reverse-proxy-in-lync-server-2013"></a>Проверка доступа через обратный прокси-сервер в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-03-29_

Выполните описанные ниже действия, чтобы убедиться в том, что пользователи могут получить доступ к данным на обратном прокси-сервере. Для правильной работы Access может потребоваться завершить настройку брандмауэра и конфигурацию DNS (Domain Name System).

<div>

## <a name="to-verify-that-you-can-access-the-website-through-the-internet"></a>Проверка возможности доступа к веб-сайту через Интернет

  - Откройте веб-браузер, введите URL-адреса в **адресную** строку, которую клиенты используют для доступа к файлам адресной книги и веб-сайту для конференций, как описано ниже.
    
      - Введите URL-адрес для сервера адресной книги, как показано ниже: **https://externalwebfarmFQDN/abs** где externalwebfarmFQDN — это внешнее полное доменное имя внешних веб-служб, которые размещаются в службах адресной книги. Пользователь должен получить запрос HTTP, так как для безопасности каталогов в папке сервера адресной книги по умолчанию настроена проверка подлинности Windows.
    
      - Для конференций введите URL-адрес, подобный следующему: **https://externalwebfarmFQDN/meet** где externalwebfarmFQDN — это внешнее полное доменное имя веб-фермы, на которой размещено содержимое собрания. Этот URL-адрес должен показывать страницу устранения неполадок для конференций. Кроме того, убедитесь, что простой URL-адрес для Конференции работает правильно. Пример простого URL-адреса для присоединения к Конференции может быть https://meet.contoso.com
    
      - Введите URL-адрес для расширения группы рассылки следующим образом: **https://externalwebfarmFQDN/GroupExpansion/service.svc** . Пользователь должен получить запрос HTTP, так как для безопасности каталогов в службе расширения групп рассылки по умолчанию настроена проверка подлинности Windows.
    
      - Для телефонного подключения введите простой URL-адрес примерно так, как показано ниже, **https://externalwebfarmFQDN/dialin** где externalwebfarmFQDN — это внешнее полное доменное имя веб-фермы, в которой размещена страница подключения для конференц-связи с телефонным подключением. Пользователь должен быть перенаправлен на страницу с телефонным подключением. Кроме того, убедитесь, что ваш простой URL-адрес работает правильно. Пример простого URL-адреса для коммутируемого подключения может быть https://dialin.contoso.com
    
      - Чтобы проверить, работает ли URL-адрес автообнаружения, введите https://lyncdiscover . externaldomainFQDN. Браузер должен предложить вам открыть файл. Выберите Блокнот, чтобы открыть его. Типичный ответ будет выглядеть примерно так:
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

</div>

</div>

<span> </span>

</div>

</div>

</div>

