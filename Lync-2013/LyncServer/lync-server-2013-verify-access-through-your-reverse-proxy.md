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
# <a name="verify-access-through-your-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="3aa36-103">Проверка доступа через обратный прокси-сервер в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3aa36-103">Verify access through your reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3aa36-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3aa36-104">

<span> </span></span></span>

<span data-ttu-id="3aa36-105">_**Тема последнего изменения:** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="3aa36-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="3aa36-106">Выполните описанные ниже действия, чтобы убедиться в том, что пользователи могут получить доступ к данным на обратном прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="3aa36-106">Use the following procedure to verify that your users can access information on the reverse proxy.</span></span> <span data-ttu-id="3aa36-107">Для правильной работы Access может потребоваться завершить настройку брандмауэра и конфигурацию DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="3aa36-107">You might need to complete the firewall configuration and Domain Name System (DNS) configuration before access will work correctly.</span></span>

<div>

## <a name="to-verify-that-you-can-access-the-website-through-the-internet"></a><span data-ttu-id="3aa36-108">Проверка возможности доступа к веб-сайту через Интернет</span><span class="sxs-lookup"><span data-stu-id="3aa36-108">To verify that you can access the website through the Internet</span></span>

  - <span data-ttu-id="3aa36-109">Откройте веб-браузер, введите URL-адреса в **адресную** строку, которую клиенты используют для доступа к файлам адресной книги и веб-сайту для конференций, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="3aa36-109">Open a web browser, type the URLs in the **Address** bar that clients use to access the Address Book files and the website for conferencing as follows:</span></span>
    
      - <span data-ttu-id="3aa36-110">Введите URL-адрес для сервера адресной книги, как показано ниже: **https://externalwebfarmFQDN/abs** где externalwebfarmFQDN — это внешнее полное доменное имя внешних веб-служб, которые размещаются в службах адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3aa36-110">For Address Book Server, type a URL similar to the following: **https://externalwebfarmFQDN/abs** where externalwebfarmFQDN is the external FQDN of the external web services that hosts Address Book services.</span></span> <span data-ttu-id="3aa36-111">Пользователь должен получить запрос HTTP, так как для безопасности каталогов в папке сервера адресной книги по умолчанию настроена проверка подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="3aa36-111">The user should receive an HTTP challenge, because directory security on the Address Book Server folder is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="3aa36-112">Для конференций введите URL-адрес, подобный следующему: **https://externalwebfarmFQDN/meet** где externalwebfarmFQDN — это внешнее полное доменное имя веб-фермы, на которой размещено содержимое собрания.</span><span class="sxs-lookup"><span data-stu-id="3aa36-112">For conferencing, type a URL similar to the following: **https://externalwebfarmFQDN/meet** where externalwebfarmFQDN is the external FQDN of the web farm that hosts meeting content.</span></span> <span data-ttu-id="3aa36-113">Этот URL-адрес должен показывать страницу устранения неполадок для конференций.</span><span class="sxs-lookup"><span data-stu-id="3aa36-113">This URL should display the troubleshooting page for conferencing.</span></span> <span data-ttu-id="3aa36-114">Кроме того, убедитесь, что простой URL-адрес для Конференции работает правильно.</span><span class="sxs-lookup"><span data-stu-id="3aa36-114">Alternatively, confirm that your Simple URL for conferencing functions correctly.</span></span> <span data-ttu-id="3aa36-115">Пример простого URL-адреса для присоединения к Конференции может быть https://meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3aa36-115">An example Simple URL for the conference join might be https://meet.contoso.com</span></span>
    
      - <span data-ttu-id="3aa36-116">Введите URL-адрес для расширения группы рассылки следующим образом: **https://externalwebfarmFQDN/GroupExpansion/service.svc** .</span><span class="sxs-lookup"><span data-stu-id="3aa36-116">For distribution group expansion, type a URL similar to the following: **https://externalwebfarmFQDN/GroupExpansion/service.svc**.</span></span> <span data-ttu-id="3aa36-117">Пользователь должен получить запрос HTTP, так как для безопасности каталогов в службе расширения групп рассылки по умолчанию настроена проверка подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="3aa36-117">The user should receive an HTTP challenge, because directory security on the distribution group expansion service is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="3aa36-118">Для телефонного подключения введите простой URL-адрес примерно так, как показано ниже, **https://externalwebfarmFQDN/dialin** где externalwebfarmFQDN — это внешнее полное доменное имя веб-фермы, в которой размещена страница подключения для конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="3aa36-118">For dial-in, type the simple URL similar to the following **https://externalwebfarmFQDN/dialin** where externalwebfarmFQDN is the external FQDN of the web farm that hosts the dial-in page for dial-in conferencing.</span></span> <span data-ttu-id="3aa36-119">Пользователь должен быть перенаправлен на страницу с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="3aa36-119">The user should be directed to the dial-in page.</span></span> <span data-ttu-id="3aa36-120">Кроме того, убедитесь, что ваш простой URL-адрес работает правильно.</span><span class="sxs-lookup"><span data-stu-id="3aa36-120">Alternatively, confirm that your Simple URL dial-in functions correctly.</span></span> <span data-ttu-id="3aa36-121">Пример простого URL-адреса для коммутируемого подключения может быть https://dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3aa36-121">An example Simple URL for dial-in might be https://dialin.contoso.com</span></span>
    
      - <span data-ttu-id="3aa36-122">Чтобы проверить, работает ли URL-адрес автообнаружения, введите https://lyncdiscover .</span><span class="sxs-lookup"><span data-stu-id="3aa36-122">To confirm that the autodiscover URL is working, type https://lyncdiscover.</span></span> <span data-ttu-id="3aa36-123">externaldomainFQDN.</span><span class="sxs-lookup"><span data-stu-id="3aa36-123">externaldomainFQDN.</span></span> <span data-ttu-id="3aa36-124">Браузер должен предложить вам открыть файл.</span><span class="sxs-lookup"><span data-stu-id="3aa36-124">The browser should prompt you to open a file.</span></span> <span data-ttu-id="3aa36-125">Выберите Блокнот, чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="3aa36-125">Select Notepad to open it.</span></span> <span data-ttu-id="3aa36-126">Типичный ответ будет выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="3aa36-126">A typical response would be similar to:</span></span>
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

<span data-ttu-id="3aa36-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3aa36-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

