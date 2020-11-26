---
title: 'Lync Server 2013: Установка Lync для iPhone и iPad'
description: 'Lync Server 2013: Установка Lync для iPhone и iPad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Lync for iPhone and iPad
ms:assetid: 88d1c149-5842-4ecf-a15e-fcda0330325b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690987(v=OCS.15)
ms:contentKeyID: 51541496
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b186cca023d7d65146f3f9c91149c49a5555de81
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427065"
---
# <a name="installing-lync-for-iphone-and-ipad-in-lync-server-2013"></a><span data-ttu-id="8ec61-103">Установка Lync для iPhone и iPad в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ec61-103">Installing Lync for iPhone and iPad in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ec61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ec61-104">

<span> </span></span></span>

<span data-ttu-id="8ec61-105">_**Тема последнего изменения:** 2014-03-10_</span><span class="sxs-lookup"><span data-stu-id="8ec61-105">_**Topic Last Modified:** 2014-03-10_</span></span>

<span data-ttu-id="8ec61-106">Lync 2013 для iPhone и Lync 2013 для iPad — это приложения, устанавливаемые пользователем, которые доступны в магазине Apple App Store.</span><span class="sxs-lookup"><span data-stu-id="8ec61-106">Lync 2013 for iPhone and Lync 2013 for iPad are user-installable applications that are available in the Apple App Store.</span></span>

<div>

## <a name="installing-lync-for-iphone-and-lync-for-ipad"></a><span data-ttu-id="8ec61-107">Установка Lync для iPhone и Lync для iPad</span><span class="sxs-lookup"><span data-stu-id="8ec61-107">Installing Lync for iPhone and Lync for iPad</span></span>

<span data-ttu-id="8ec61-108">Вы можете подать пользователям возможность установить Lync 2013 для iPhone и Lync 2013 для iPad, перенаправив их на свои устройства из магазина приложений.</span><span class="sxs-lookup"><span data-stu-id="8ec61-108">You can instruct your users to install Lync 2013 for iPhone and Lync 2013 for iPad by directing them to the App Store from their devices.</span></span> <span data-ttu-id="8ec61-109">Магазин приложений для каждого устройства также доступен в сети.</span><span class="sxs-lookup"><span data-stu-id="8ec61-109">The App Store for each device is also available online.</span></span>

  - <span data-ttu-id="8ec61-110">Lync для iPhone доступен в магазине App Store по адресу \< h<span> </span> TTP://www.Apple.com/iPhone/from-the-App-Store/></span><span class="sxs-lookup"><span data-stu-id="8ec61-110">Lync for iPhone is available in the App Store at \< h<span></span>ttp://www.apple.com/iphone/from-the-app-store/></span></span>

  - <span data-ttu-id="8ec61-111">Lync для iPad доступен в магазине App Store по адресу \< ht<span> </span> TP://www.Apple.com/iPad/from-the-App-Store/></span><span class="sxs-lookup"><span data-stu-id="8ec61-111">Lync for iPad is available in the App Store at \< ht<span></span>tp://www.apple.com/ipad/from-the-app-store/></span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8ec61-112">Пользователи iPhone, которые не установили приложение Lync 2013 и которые пытаются присоединиться к собранию Lync из приглашения на собрание, будут перенаправляться на страницу средства запуска присоединения.</span><span class="sxs-lookup"><span data-stu-id="8ec61-112">iPhone users who have not installed the Lync 2013 app and who try to join a Lync meeting from a meeting invitation will be redirected to a Join Launcher page.</span></span> <span data-ttu-id="8ec61-113">На этой странице содержится ссылка для установки приложения Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="8ec61-113">This page contains a link for installing the Lync 2013 app.</span></span> <span data-ttu-id="8ec61-114">Однако вместо того чтобы перенаправлять пользователя в App Store, эта ссылка открывает пустую страницу браузера Safari.</span><span class="sxs-lookup"><span data-stu-id="8ec61-114">However, instead of directing the user to the App Store, this link opens a blank Safari browser page.</span></span> <span data-ttu-id="8ec61-115">Для решения этой проблемы пользователь может выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="8ec61-115">The user can do one of two things to work around this issue:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="8ec61-116">Нажмите кнопку " <STRONG>домой</STRONG> ", чтобы отправить страницу Safari на задний план, а затем откройте браузер Safari.</span><span class="sxs-lookup"><span data-stu-id="8ec61-116">Use the <STRONG>Home</STRONG> button to send the Safari page to the background, and then reopen Safari.</span></span> <span data-ttu-id="8ec61-117">Когда появится уведомление "открыть эту страницу в App Store", нажмите кнопку <STRONG>Открыть</STRONG> , чтобы перейти в приложение Lync 2013 download в магазине App Store.</span><span class="sxs-lookup"><span data-stu-id="8ec61-117">When the notification “Open this page in App Store” appears, tap <STRONG>Open</STRONG> to be directed to Lync 2013 download in the App Store.</span></span></P>
> <LI>
> <P><span data-ttu-id="8ec61-118">Вручную Откройте App Store, выполните поиск по запросу "Lync 2013" и скачайте приложение.</span><span class="sxs-lookup"><span data-stu-id="8ec61-118">Manually open the App Store, search for "Lync 2013," and download the app.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="verifying-mobile-client-installation"></a><span data-ttu-id="8ec61-119">Проверка установки клиента для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="8ec61-119">Verifying Mobile Client Installation</span></span>

<span data-ttu-id="8ec61-120">После того как вы настроили клиент и Войди в систему, выполните следующие проверки, чтобы убедиться, что установка Lync правильно работает на вашем мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="8ec61-120">After you configure the client and sign in successfully, use the following tests to verify that your Lync installation is working correctly on your mobile device.</span></span>

<span data-ttu-id="8ec61-121">**Поиск контакта в корпоративном каталоге**</span><span class="sxs-lookup"><span data-stu-id="8ec61-121">**Search for a contact in the corporate directory**</span></span>

1.  <span data-ttu-id="8ec61-122">В списке контактов коснитесь внутри строки поиска в верхней части экрана и начните ввод имени контакта, присутствующего в глобальном списке адресов (GAL).</span><span class="sxs-lookup"><span data-stu-id="8ec61-122">In the Contacts list, tap inside the search bar at the top, and begin typing the name of a contact that exists only in the global address list (GAL).</span></span>

2.  <span data-ttu-id="8ec61-123">Убедитесь, что имя контакта отображается в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="8ec61-123">Verify that the contact name appears in the search results.</span></span>

<span data-ttu-id="8ec61-124">**Проверка функций обмена мгновенными сообщениями и сведений о присутствии**</span><span class="sxs-lookup"><span data-stu-id="8ec61-124">**Test instant messaging and presence**</span></span>

1.  <span data-ttu-id="8ec61-125">В списке контактов выберите контакт.</span><span class="sxs-lookup"><span data-stu-id="8ec61-125">In the Contacts list, tap a contact.</span></span>

2.  <span data-ttu-id="8ec61-126">На карточке контакта коснитесь значка **мгновенное сообщение** .</span><span class="sxs-lookup"><span data-stu-id="8ec61-126">In the contact card, tap the **IM** icon.</span></span>

3.  <span data-ttu-id="8ec61-127">Убедитесь, что окно программы обмена мгновенными сообщениями открывается и вы можете ввести и отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="8ec61-127">Verify that an instant messaging (IM) window appears and that you can type and send an IM.</span></span>

<span data-ttu-id="8ec61-128">**Проверка конференц-связи с телефонным подключением**</span><span class="sxs-lookup"><span data-stu-id="8ec61-128">**Test dial-out conferencing**</span></span>

1.  <span data-ttu-id="8ec61-129">В Outlook Запланируйте собрание Lync.</span><span class="sxs-lookup"><span data-stu-id="8ec61-129">In Outlook, schedule a Lync meeting.</span></span>

2.  <span data-ttu-id="8ec61-130">На мобильном устройстве откройте приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="8ec61-130">On the mobile device, open the meeting invitation.</span></span>

3.  <span data-ttu-id="8ec61-131">Щелкните ссылку в собрании, чтобы присоединиться к нему.</span><span class="sxs-lookup"><span data-stu-id="8ec61-131">Click the link in the meeting to join.</span></span>

4.  <span data-ttu-id="8ec61-132">Ответьте на звонок от службы конференц-связи и убедитесь, что вы подключены к звуковому каналу собрания.</span><span class="sxs-lookup"><span data-stu-id="8ec61-132">Answer the call from the conference service and verify that you are connected to the meeting audio.</span></span>

<span data-ttu-id="8ec61-133">**Проверка push-уведомлений**</span><span class="sxs-lookup"><span data-stu-id="8ec61-133">**Test push notifications**</span></span>

1.  <span data-ttu-id="8ec61-134">На мобильном устройстве пользователя A Войдите в Lync с помощью учетной записи пользователя A.</span><span class="sxs-lookup"><span data-stu-id="8ec61-134">On user A’s mobile device, sign in to Lync with user A’s account.</span></span>

2.  <span data-ttu-id="8ec61-135">Откройте другое приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="8ec61-135">Open another application on the mobile device.</span></span>

3.  <span data-ttu-id="8ec61-136">На другом клиенте Войдите в Lync с учетной записью пользователя B.</span><span class="sxs-lookup"><span data-stu-id="8ec61-136">On a different client, sign in to Lync with user B’s account.</span></span>

4.  <span data-ttu-id="8ec61-137">Отправьте мгновенное сообщение от пользователя Б пользователю А.</span><span class="sxs-lookup"><span data-stu-id="8ec61-137">Send an IM from user B to user A.</span></span>

5.  <span data-ttu-id="8ec61-138">Убедитесь, что уведомление о мгновенном сообщении отображается на мобильном устройстве пользователя А.</span><span class="sxs-lookup"><span data-stu-id="8ec61-138">Verify that the IM notification appears on user A’s mobile device.</span></span>

<span data-ttu-id="8ec61-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ec61-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

