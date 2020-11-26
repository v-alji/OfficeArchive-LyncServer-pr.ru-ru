---
title: 'Lync Server 2013: функции и возможности мобильной работы'
description: 'Lync Server 2013: функции и возможности мобильной связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility features and capabilities
ms:assetid: 12517a88-2531-44a5-bea5-d8884aff53eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh689983(v=OCS.15)
ms:contentKeyID: 48183457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20713145c18260f22d9635c34af291e9a7c5ea9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445955"
---
# <a name="mobility-features-and-capabilities-in-lync-server-2013"></a><span data-ttu-id="10c29-103">Функции и возможности мобильной работы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10c29-103">Mobility features and capabilities in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10c29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10c29-104">

<span> </span></span></span>

<span data-ttu-id="10c29-105">_**Тема последнего изменения:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="10c29-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="10c29-106">Функция мобильной связи, представленная в накопительных обновлениях для Lync Server 2013: Февраль 2013 поддерживает функции мобильных клиентов Lync 2010 Mobile и Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="10c29-106">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2010 Mobile and Lync 2013 Mobile clients functionality.</span></span> <span data-ttu-id="10c29-107">При развертывании службы Lync Server 2013 Mobility Service пользователи могут использовать поддерживаемые устройства Apple iOS, Android и Windows Phone или Nokia Symbian на мобильных устройствах для выполнения таких операций, как отправка и получение мгновенных сообщений, просмотр контактов и Просмотр сведений о присутствии.</span><span class="sxs-lookup"><span data-stu-id="10c29-107">When you deploy the Lync Server 2013 Mobility Service, users can use supported Apple iOS, Android, and Windows Phone, or Nokia Symbian mobile devices to perform activities such as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="10c29-108">Кроме того, некоторые мобильные устройства поддерживают такие функции службы "Корпоративная голосовая связь", как присоединение к конференции одним щелчком, звонки с рабочего телефона, доступ по одному номеру, голосовая почта и пропущенные звонки.</span><span class="sxs-lookup"><span data-stu-id="10c29-108">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed calls.</span></span> <span data-ttu-id="10c29-109">Новые функции, представленные в накопительных обновлениях для Lync Server 2013: Февраль 2013 включают возможности голосовой связи по протоколу IP (VoIP) и видео (H. 264) для участника собрания.</span><span class="sxs-lookup"><span data-stu-id="10c29-109">New features introduced in the Cumulative Updates for Lync Server 2013: February 2013 include Voice over IP (VoIP) capability and video (H.264) for meeting attendee.</span></span>

<span data-ttu-id="10c29-110">Функция мобильной связи, представленная в накопительных обновлениях для Lync Server 2013: Февраль 2013 поддерживает функции мобильных клиентов Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="10c29-110">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2013 Mobile client functionality.</span></span> <span data-ttu-id="10c29-111">Накопительные обновления для Lync Server 2013: Февраль 2013 установите веб-API единой системы обмена сообщениями или UCWA.</span><span class="sxs-lookup"><span data-stu-id="10c29-111">The Cumulative Updates for Lync Server 2013: February 2013 install Unified Communications Web API, or UCWA.</span></span> <span data-ttu-id="10c29-112">UCWA является компонентом, используемым для мобильных клиентов Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="10c29-112">UCWA is the component used for Lync 2013 Mobile clients.</span></span> <span data-ttu-id="10c29-113">В Lync Server 2013 MCX используется для мобильных клиентов Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="10c29-113">In Lync Server 2013, Mcx is used for Lync 2010 Mobile clients.</span></span> <span data-ttu-id="10c29-114">Накопительные обновления для Lync Server 2013: Февраль 2013 вводят UCWA как новую точку входа для служб Mobility Service.</span><span class="sxs-lookup"><span data-stu-id="10c29-114">Cumulative Updates for Lync Server 2013: February 2013 introduce UCWA as the new entry point for mobility services.</span></span> <span data-ttu-id="10c29-115">Lync Server 2013 параллельно реализует службу Mobility Service (MCX), которая представлена в накопительных обновлениях для Lync Server 2010: Ноябрь 2011, и обеспечивает поддержку Lync 2010 Mobile.</span><span class="sxs-lookup"><span data-stu-id="10c29-115">Lync Server 2013 concurrently implements the Mobility Service (Mcx), introduced in the Cumulative Updates for Lync Server 2010: November 2011, and provides support for Lync 2010 Mobile.</span></span> <span data-ttu-id="10c29-116">При развертывании накопительных обновлений для Lync Server 2013: Февраль 2013, пользователи могут использовать поддерживаемые мобильные устройства Apple iOS, Android и Windows Phone для выполнения таких действий, как:</span><span class="sxs-lookup"><span data-stu-id="10c29-116">When you deploy the Cumulative Updates for Lync Server 2013: February 2013, users can use supported Apple iOS, Android, and Windows Phone mobile devices to perform such activities as:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="10c29-117">Возможности, поддерживаемые службой Mobility Service из накопительных обновлений для Lync Server 2010: Ноябрь 2011 отмечены вместе с (MCX).</span><span class="sxs-lookup"><span data-stu-id="10c29-117">Features supported by the Mobility Service from the Cumulative Updates for Lync Server 2010: November 2011 are noted with (Mcx).</span></span> <span data-ttu-id="10c29-118">Все перечисленные функции поддерживаются UCWA, представленными в накопительных обновлениях для Lync Server 2013: Февраль 2013.</span><span class="sxs-lookup"><span data-stu-id="10c29-118">All listed features are supported by the UCWA, introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

  - <span data-ttu-id="10c29-119">Отправка и получение мгновенных сообщений (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-119">Send and receive instant messages (Mcx)</span></span>

  - <span data-ttu-id="10c29-120">Просмотр сведений о присутствии (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-120">View presence (Mcx)</span></span>

  - <span data-ttu-id="10c29-121">Просмотр контактов (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-121">View contacts (Mcx)</span></span>

  - <span data-ttu-id="10c29-122">Щелкните, чтобы присоединиться к Конференции (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-122">Click to join a conference (Mcx)</span></span>

  - <span data-ttu-id="10c29-123">Позвонить с помощью работы (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-123">Call via work (Mcx)</span></span>

  - <span data-ttu-id="10c29-124">Однозначный номер (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-124">Single number reach (Mcx)</span></span>

  - <span data-ttu-id="10c29-125">Голосовая почта (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-125">Voice mail (Mcx)</span></span>

  - <span data-ttu-id="10c29-126">Уведомление о пропущенном звонке (MCX)</span><span class="sxs-lookup"><span data-stu-id="10c29-126">Missed call notification (Mcx)</span></span>

  - <span data-ttu-id="10c29-127">Протокол VoIP</span><span class="sxs-lookup"><span data-stu-id="10c29-127">Voice over IP (VoIP)</span></span>

  - <span data-ttu-id="10c29-128">Видео участника (H.264)</span><span class="sxs-lookup"><span data-stu-id="10c29-128">Attendee video (H.264)</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="10c29-129">Lync 2010 Mobile предоставил клиента для устройств Nokia Symbian.</span><span class="sxs-lookup"><span data-stu-id="10c29-129">Lync 2010 Mobile provided a client for Nokia Symbian devices.</span></span> <span data-ttu-id="10c29-130">Lync 2013 Mobile не будет иметь клиента для устройств на базе Symbian Nokia.</span><span class="sxs-lookup"><span data-stu-id="10c29-130">Lync 2013 Mobile will not have a client for Nokia Symbian-based devices.</span></span>



</div>

<span data-ttu-id="10c29-131">Пользователи Apple iPad смогут получить доступ к расширенным возможностям.</span><span class="sxs-lookup"><span data-stu-id="10c29-131">Apple iPad users will have access to enhanced capabilities.</span></span> <span data-ttu-id="10c29-132">После присоединения к собранию с помощью голосового звонка пользователь iPad сможет просматривать загруженные презентации Microsoft PowerPoint в собрании, совместно использовать приложения и настольные компьютеры, просматривать список участников собрания и получать уведомления о других типах контента, к которым предоставлен общий доступ в собрании.</span><span class="sxs-lookup"><span data-stu-id="10c29-132">After joining a meeting by using audio call back, an iPad user will be able to view uploaded Microsoft PowerPoint presentations within a meeting, share applications and desktops, view the meeting participant list, and receive notifications of other content types that are being shared within the meeting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="10c29-133">При наличии одного номера пользователь принимает звонки на мобильный телефон, набираемый на рабочий номер.</span><span class="sxs-lookup"><span data-stu-id="10c29-133">With single number reach, a user receives calls on a mobile phone that were dialed to the work number.</span></span> <span data-ttu-id="10c29-134">С помощью функции "звонок через Work" пользователь походит на исходящий звонок из клиента Lync Mobile, используя рабочий телефон, а не номер мобильного телефона.</span><span class="sxs-lookup"><span data-stu-id="10c29-134">With Call via Work, the user places an outbound call from the Lync Mobile client by using a work phone number instead of the mobile phone number.</span></span> <span data-ttu-id="10c29-135">При использовании удаленного доступа клиент отправляет запрос на MCX или UCWA (на основе версии Lync Mobile) для осуществления звонка.</span><span class="sxs-lookup"><span data-stu-id="10c29-135">With dial-out, the client sends a request to Mcx or UCWA (based on the Lync Mobile version) to make the call for them.</span></span> <span data-ttu-id="10c29-136">Сервер инициирует звонок, а затем снова вызывает пользователя на мобильном телефоне.</span><span class="sxs-lookup"><span data-stu-id="10c29-136">The server initiates the call and then calls the user back on the mobile phone.</span></span> <span data-ttu-id="10c29-137">После того как пользователь ответит, сервер завершает звонок, набрав другого абонента.</span><span class="sxs-lookup"><span data-stu-id="10c29-137">When the user answers, the server completes the call by dialing the other party.</span></span> <span data-ttu-id="10c29-138">Используя функцию "звонок с помощью работы", пользователи могут сохранять свою работу во время звонка, что означает, что получатель звонка не видит номер мобильного телефона вызывающего абонента, и вызывающий объект не позволяет устранить подлинность исходящих звонков.</span><span class="sxs-lookup"><span data-stu-id="10c29-138">By using Call via Work, users can maintain their work identity during a call, which means that the call recipient does not see the caller's mobile number, and the caller avoids incurring outbound calling charges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="10c29-139">Некоторые функции работают одинаково на всех мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="10c29-139">Not all features work exactly the same on all mobile devices.</span></span> <span data-ttu-id="10c29-140">Дополнительные сведения о функциях, поддерживаемых на мобильных устройствах, можно найти в таблице сравнения мобильных клиентов <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A> .</span><span class="sxs-lookup"><span data-stu-id="10c29-140">For details about features supported on mobile devices, see the Mobile Client Comparison Tables at <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A>.</span></span> <span data-ttu-id="10c29-141">Подробные сведения о поддерживаемых устройствах и операционных системах можно найти в разделах требования в разделе <A href="lync-server-2013-planning-for-mobile-clients.md">планирование для мобильных клиентов в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="10c29-141">For details about supported devices and operating systems, see the requirements topics under <A href="lync-server-2013-planning-for-mobile-clients.md">Planning for mobile clients in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="10c29-142">Если вы используете функцию автообнаружения Lync Server 2013, мобильные приложения смогут автоматически находить веб-службы Lync Server 2013, не требуя вручную вводить URL-адреса в параметры устройства.</span><span class="sxs-lookup"><span data-stu-id="10c29-142">When you use the Lync Server 2013 Autodiscover feature, mobile applications can automatically locate Lync Server 2013 Web Services without requiring users to manually enter the URLs in their device settings.</span></span> <span data-ttu-id="10c29-143">Кроме того, в параметрах мобильного устройства поддерживается ввод URL-адресов вручную, в основном для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="10c29-143">Manually entering URLs in mobile device settings is also supported, primarily for troubleshooting purposes.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="10c29-144">MCX и UCWA — это бесплатные услуги, и они развертываются для поддержки мобильных клиентов Lync 2010 для мобильных устройств и Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="10c29-144">The Mcx and UCWA are complimentary services and both are deployed to support Lync 2010 Mobile and Lync 2013 Mobile clients.</span></span> <span data-ttu-id="10c29-145">Lync 2013 Mobile не сможет войти в развертывание Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="10c29-145">Lync 2013 Mobile will not be able to sign in to Lync Server 2010 deployments.</span></span> <span data-ttu-id="10c29-146">Lync 2010 Mobile и Lync 2013 Mobile также смогут использовать развертывание Lync Server 2013 с накопительными обновлениями для Lync Server 2013: применено обновлений за Февраль 2013 г.</span><span class="sxs-lookup"><span data-stu-id="10c29-146">Lync 2010 Mobile and Lync 2013 Mobile will be able to use a Lync Server 2013 deployment with the Cumulative Updates for Lync Server 2013: February 2013 applied.</span></span>



</div>

<span data-ttu-id="10c29-147">Функция Mobility также поддерживает *Push-уведомления* для мобильных устройств, которые не поддерживают приложения, работающие в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="10c29-147">The mobility feature also supports *push notifications* for mobile devices that do not support applications running in the background.</span></span> <span data-ttu-id="10c29-148">Push-уведомление — это передаваемое на мобильное устройство уведомление о событии, которое произошло в то время, когда мобильное приложение было неактивно.</span><span class="sxs-lookup"><span data-stu-id="10c29-148">A push notification is a notification that is sent to a mobile device about an event that occurs while a mobile application is inactive.</span></span> <span data-ttu-id="10c29-149">Например, сообщение с приглашением на обмен мгновенными сообщениями может привести к появлению push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="10c29-149">For example, a missed instant messaging (IM) invitation can result in a push notification.</span></span>

<span data-ttu-id="10c29-150">MCX, UCWA, служба автообнаружения и поддержка push-уведомлений предоставляются в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="10c29-150">Mcx, UCWA, Autodiscover Service, and support for push notifications are provided in Lync Server 2013.</span></span> <span data-ttu-id="10c29-151">Обновленные функции клиента, возможности и использование UCWA в качестве точки входа для мобильных устройств представлены в накопительных обновлениях для Lync Server 2013: Февраль 2013.</span><span class="sxs-lookup"><span data-stu-id="10c29-151">Updated client features, capabilities, and the use of UCWA as the mobility entry point are introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="10c29-152"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10c29-152"></div>

<span> </span>

</div>

</div>

</span></span></div>

