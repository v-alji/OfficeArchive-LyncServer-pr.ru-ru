---
title: 'Lync Server 2013: Установка Lync для Windows Phone'
description: 'Lync Server 2013: Установка Lync для Windows Phone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Lync for Windows Phone
ms:assetid: bf502546-ff69-489f-a92e-a78b58803d53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690996(v=OCS.15)
ms:contentKeyID: 51541513
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f5da90a5dc0babdc6944e4f9c426fe896d4f156
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427049"
---
# <a name="installing-lync-for-windows-phone-in-lync-server-2013"></a><span data-ttu-id="6af98-103">Установка Lync для Windows Phone в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6af98-103">Installing Lync for Windows Phone in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6af98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6af98-104">

<span> </span></span></span>

<span data-ttu-id="6af98-105">_**Тема последнего изменения:** 2014-02-03_</span><span class="sxs-lookup"><span data-stu-id="6af98-105">_**Topic Last Modified:** 2014-02-03_</span></span>

<span data-ttu-id="6af98-106">Lync 2013 для Windows Phone — это приложение, которое можно установить для пользователей и доступно в Windows Phone Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6af98-106">Lync 2013 for Windows Phone is a user-installable application that is available in the Windows Phone Marketplace.</span></span>

<div>

## <a name="installing-lync-for-windows-mobile"></a><span data-ttu-id="6af98-107">Установка Lync для Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="6af98-107">Installing Lync for Windows Mobile</span></span>

<span data-ttu-id="6af98-108">Вы можете подать пользователям возможность установить Lync 2013 для Windows Phone на своих устройствах, направив их на Windows Phone Marketplace по адресу <https://go.microsoft.com/fwlink/p/?linkid=231901> .</span><span class="sxs-lookup"><span data-stu-id="6af98-108">You can instruct your users to install Lync 2013 for Windows Phone on their devices by directing them to the Windows Phone Marketplace at <https://go.microsoft.com/fwlink/p/?linkid=231901>.</span></span>

</div>

<div>

## <a name="if-you-use-a-dns-srv-record-to-publish-exchange-web-services"></a><span data-ttu-id="6af98-109">Если для публикации веб-служб Exchange используется запись DNS SRV</span><span class="sxs-lookup"><span data-stu-id="6af98-109">If You Use a DNS SRV Record to Publish Exchange Web Services</span></span>

<span data-ttu-id="6af98-110">Для включения интеграции с Exchange для клиентов Lync некоторые организации публикуют URL-адрес служб Exchange, используя запись DNS SRV.</span><span class="sxs-lookup"><span data-stu-id="6af98-110">To enable Exchange integration for Lync clients, some organizations publish the Exchange Web Services URL by using a DNS SRV record.</span></span> <span data-ttu-id="6af98-111">В документе "Основные сведения и устранение неполадок при интеграции Exchange" в центре загрузки Microsoft [https://go.microsoft.com/fwlink/?LinkID=391095](https://go.microsoft.com/fwlink/?linkid=391095) описаны сценарии, в которых это может потребоваться.</span><span class="sxs-lookup"><span data-stu-id="6af98-111">The document "Understanding and Troubleshooting Exchange Integration," available in the Microsoft Download Center at [https://go.microsoft.com/fwlink/?LinkID=391095](https://go.microsoft.com/fwlink/?linkid=391095), describes scenarios in which this might be necessary.</span></span> <span data-ttu-id="6af98-112">Однако интеграция с Exchange для пользователей Windows Phone не будет работать в этом сценарии, так как платформа Windows Phone не поддерживает поиск SRV.</span><span class="sxs-lookup"><span data-stu-id="6af98-112">However, Exchange integration for Windows Phone users will not work in this scenario, because the Windows Phone platform does not support SRV lookups.</span></span> <span data-ttu-id="6af98-113">Вам потребуется указать, что пользователи Windows Phone будут указывать URL веб-службы Exchange вместо того, чтобы разрешить телефону автоматически определять сервер.</span><span class="sxs-lookup"><span data-stu-id="6af98-113">You will need to instruct Windows Phone users to specify the Exchange Web Services URL instead of allowing the phone to automatically detect the server.</span></span>

<span data-ttu-id="6af98-114">Попросите пользователей настроить параметры Lync на телефоне с Windows, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="6af98-114">Instruct your users to configure the Lync settings on their Windows Phones as follows:</span></span>

1.  <span data-ttu-id="6af98-115">На устройстве с Windows Phone в параметрах Lync щелкните экран **Exchange** .</span><span class="sxs-lookup"><span data-stu-id="6af98-115">In Windows Phone, in the Lync settings, select the **Exchange** screen.</span></span>

2.  <span data-ttu-id="6af98-116">Переместить **сервер автоматически** **.**</span><span class="sxs-lookup"><span data-stu-id="6af98-116">Move **Auto-Detect Server** to **Off**.</span></span>

3.  <span data-ttu-id="6af98-117">Коснитесь пустого поля и введите полное доменное имя (FQDN) для веб-служб Exchange.</span><span class="sxs-lookup"><span data-stu-id="6af98-117">Tap the empty field and enter the fully qualified domain name (FQDN) or URL for Exchange Web Services.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6af98-118">Вы можете указать либо полное доменное имя (FQDN), либо полный URL-адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="6af98-118">You can specify either the fully qualified domain name (FQDN) or the full URL of your Exchange Web Services server.</span></span> <span data-ttu-id="6af98-119">При указании полного доменного имени протокол (https://) и путь к веб-службам Exchange (/EWS/Exchange.asmx) добавляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="6af98-119">If you specify the FQDN, the protocol (https://) and the Exchange Web Services path (/ews/exchange.asmx) are added automatically.</span></span> <span data-ttu-id="6af98-120">Если путь к веб-службам Exchange отличается, вы можете указать полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="6af98-120">If your Exchange Web Services path is different, you can specify the full URL.</span></span>

    
    </div>

4.  <span data-ttu-id="6af98-121">Закройте экран.</span><span class="sxs-lookup"><span data-stu-id="6af98-121">Close the screen.</span></span>

</div>

<div>

## <a name="verifying-mobile-client-installation"></a><span data-ttu-id="6af98-122">Проверка установки клиента для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="6af98-122">Verifying Mobile Client Installation</span></span>

<span data-ttu-id="6af98-123">После того как вы настроили клиент и войдете в свою учетную запись, выполните следующие проверки, чтобы убедиться, что установка Lync 2013 работает правильно на вашем мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="6af98-123">After you configure the client and sign in successfully, use the following tests to verify that your installation of Lync 2013 is working correctly on your mobile device.</span></span>

<span data-ttu-id="6af98-124">**Поиск контакта в корпоративном каталоге**</span><span class="sxs-lookup"><span data-stu-id="6af98-124">**Search for a contact in the corporate directory**</span></span>

1.  <span data-ttu-id="6af98-125">В списке контактов нажмите кнопку **Поиск** в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="6af98-125">In the Contacts list, tap **Search** at the bottom.</span></span>

2.  <span data-ttu-id="6af98-126">Выполните поиск контакта, который существует только в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="6af98-126">Search for a contact that exists only in the global address list.</span></span>

3.  <span data-ttu-id="6af98-127">Убедитесь, что имя контакта отображается в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="6af98-127">Verify that the contact name appears in the search results.</span></span>

<span data-ttu-id="6af98-128">**Проверка функций обмена мгновенными сообщениями и сведений о присутствии**</span><span class="sxs-lookup"><span data-stu-id="6af98-128">**Test instant messaging and presence**</span></span>

1.  <span data-ttu-id="6af98-129">В списке контактов выберите контакт.</span><span class="sxs-lookup"><span data-stu-id="6af98-129">In the Contacts list, tap a contact.</span></span>

2.  <span data-ttu-id="6af98-130">На карточке контакта коснитесь значка **мгновенное сообщение** .</span><span class="sxs-lookup"><span data-stu-id="6af98-130">In the contact card, tap the **IM** icon.</span></span>

3.  <span data-ttu-id="6af98-131">Убедитесь, что окно программы обмена мгновенными сообщениями открывается и вы можете ввести и отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="6af98-131">Verify that an instant messaging (IM) window appears and that you can type and send an IM.</span></span>

<span data-ttu-id="6af98-132">**Проверка конференц-связи с телефонным подключением**</span><span class="sxs-lookup"><span data-stu-id="6af98-132">**Test dial-out conferencing**</span></span>

1.  <span data-ttu-id="6af98-133">В Outlook Запланируйте собрание Lync.</span><span class="sxs-lookup"><span data-stu-id="6af98-133">In Outlook, schedule a Lync meeting.</span></span>

2.  <span data-ttu-id="6af98-134">На мобильном устройстве откройте приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="6af98-134">On the mobile device, open the meeting invitation.</span></span>

3.  <span data-ttu-id="6af98-135">Щелкните ссылку в собрании, чтобы присоединиться к нему.</span><span class="sxs-lookup"><span data-stu-id="6af98-135">Click the link in the meeting to join.</span></span>

4.  <span data-ttu-id="6af98-136">Ответьте на звонок службы конференций и убедитесь, что вы можете прослушивать звук.</span><span class="sxs-lookup"><span data-stu-id="6af98-136">Answer the call from the conference service and verify that you are connected to meeting audio.</span></span>

<span data-ttu-id="6af98-137">**Проверка push-уведомлений**</span><span class="sxs-lookup"><span data-stu-id="6af98-137">**Test push notifications**</span></span>

1.  <span data-ttu-id="6af98-138">На мобильном устройстве пользователя A Войдите в Lync с помощью учетной записи пользователя A.</span><span class="sxs-lookup"><span data-stu-id="6af98-138">On user A’s mobile device, sign in to Lync with user A’s account.</span></span>

2.  <span data-ttu-id="6af98-139">Откройте другое приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="6af98-139">Open another application on the mobile device.</span></span>

3.  <span data-ttu-id="6af98-140">На другом клиенте Войдите в Lync с учетной записью пользователя B.</span><span class="sxs-lookup"><span data-stu-id="6af98-140">On a different client, sign in to Lync with user B’s account.</span></span>

4.  <span data-ttu-id="6af98-141">Отправьте мгновенное сообщение от пользователя Б пользователю А.</span><span class="sxs-lookup"><span data-stu-id="6af98-141">Send an IM from user B to user A.</span></span>

5.  <span data-ttu-id="6af98-142">Убедитесь, что уведомление о мгновенном сообщении отображается на мобильном устройстве пользователя А.</span><span class="sxs-lookup"><span data-stu-id="6af98-142">Verify that the IM notification appears on user A’s mobile device.</span></span>

<span data-ttu-id="6af98-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6af98-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

