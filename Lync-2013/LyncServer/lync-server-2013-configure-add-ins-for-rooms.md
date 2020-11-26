---
title: 'Lync Server 2013: настройка надстроек для чатов'
description: 'Lync Server 2013: Настройка надстроек для помещений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure add-ins for rooms
ms:assetid: 4eeaf19e-8369-4f6f-af65-a283cf7daa1c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204878(v=OCS.15)
ms:contentKeyID: 48184090
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 803bff81fa76bf5a7d2d408c93ba9247ead72510
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434163"
---
# <a name="configure-add-ins-for-rooms-in-lync-server-2013"></a><span data-ttu-id="0f121-103">Настройка надстроек для чатов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0f121-103">Configure add-ins for rooms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0f121-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0f121-104">

<span> </span></span></span>

<span data-ttu-id="0f121-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0f121-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0f121-106">В панели управления Lync Server 2013 можно использовать раздел **надстройки** на странице **сохраняемый чат** , чтобы сопоставить URL-адреса с сохраняемыми комнатами чата.</span><span class="sxs-lookup"><span data-stu-id="0f121-106">In Lync Server 2013 Control Panel, you can use the **Add-in** section of the **Persistent Chat** page to associate URLs with Persistent Chat rooms.</span></span> <span data-ttu-id="0f121-107">Эти URL-адреса отображаются в клиенте Lync 2013 в комнате чата в области расширение беседы.</span><span class="sxs-lookup"><span data-stu-id="0f121-107">These URLs appear in the Lync 2013 client in the chat room in the conversation extensibility pane.</span></span> <span data-ttu-id="0f121-108">Администратор должен добавить надстройки в список зарегистрированных надстроек и добавить в него диспетчеры комнат (создатели), чтобы связать помещения с одной из зарегистрированных надстроек, прежде чем пользователи смогут увидеть это обновление в своем клиенте Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="0f121-108">An administrator must add Add-ins to the list of registered add-ins, and chat room managers/Creators have to associate rooms with one of the registered add-ins before users can see this upgrade in their Lync 2013 client.</span></span>

<span data-ttu-id="0f121-109">Надстройки используются для расширения доступных в комнате возможностей.</span><span class="sxs-lookup"><span data-stu-id="0f121-109">Add-ins are used to extend the in-room experience.</span></span> <span data-ttu-id="0f121-110">Типичная надстройка может включать URL-адрес, указывающий на приложение Silverlight, которое перехватывается, когда Биржевая сводка размещается в комнате чата, и на панели расширяемости отображается история акций.</span><span class="sxs-lookup"><span data-stu-id="0f121-110">A typical add-in might include a URL pointing to a Silverlight application that intercepts when a stock ticker is posted to a chat room, and shows the stock history in the extensibility pane.</span></span> <span data-ttu-id="0f121-111">К другим примерам относится внедрение URL-адреса OneNote в комнату чата в качестве надстройки, чтобы включить некоторый общий контекст — "Важные размышления" или "Тема дня".</span><span class="sxs-lookup"><span data-stu-id="0f121-111">Other examples include embedding a OneNote 2013 URL in the chat room as an add-in to include some shared context, such as "Top of mind" or "Topic of the day."</span></span>

<div>

## <a name="to-configure-add-ins-for-chat-rooms"></a><span data-ttu-id="0f121-112">Настройка надстроек для комнат чата</span><span class="sxs-lookup"><span data-stu-id="0f121-112">To configure Add-ins for chat rooms</span></span>

1.  <span data-ttu-id="0f121-113">Из учетной записи пользователя, назначенной роли CsPersistentChatAdministrator или CsAdministrator, выполните вход на любой компьютер во внутреннем развертывании.</span><span class="sxs-lookup"><span data-stu-id="0f121-113">From a user account that is assigned to the CsPersistentChatAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0f121-114">В меню **Пуск** выберите Панель управления Lync Server или откройте окно браузера и введите URL-адрес администратора.</span><span class="sxs-lookup"><span data-stu-id="0f121-114">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="0f121-115">Дополнительные сведения о различных способах запуска панели управления Lync Server можно найти в разделе [Открытие средства администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0f121-115">For details about the different methods that you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0f121-116">Вы также можете использовать командлеты Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f121-116">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="0f121-117">Дополнительные сведения можно найти в разделе <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Настройка сервера сохраняемого чата с помощью командлетов Windows PowerShell</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="0f121-117">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="0f121-118">В левой панели навигации нажмите **Сохраняемый чат** и выберите пункт **Надстройка**.</span><span class="sxs-lookup"><span data-stu-id="0f121-118">In the left navigation bar, click **Persistent Chat**, and then click **Add-in**.</span></span>
    
    <span data-ttu-id="0f121-119">Для нескольких развертываний пула серверов с постоянным подключением выберите нужный пул из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="0f121-119">For multiple Persistent Chat Server pool deployments, select the appropriate pool from the drop-down list.</span></span>

4.  <span data-ttu-id="0f121-120">На странице **Надстройка** нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0f121-120">On the **Add-in** page, click **New**.</span></span>

5.  <span data-ttu-id="0f121-121">В окне **Выбор службы** выберите службу, соответствующую пулу серверов сохраняемого чата, в котором необходимо создать надстройку.</span><span class="sxs-lookup"><span data-stu-id="0f121-121">In **Select a Service**, select the service corresponding to the Persistent Chat Server pool where you need to create the Add-in.</span></span> <span data-ttu-id="0f121-122">Надстройки нельзя перемещать из одного пула в другой или совместно использовать разными пулами.</span><span class="sxs-lookup"><span data-stu-id="0f121-122">Add-ins cannot be moved from one pool to another or shared between different pools.</span></span>

6.  <span data-ttu-id="0f121-123">В окне **Новая надстройка** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0f121-123">In **New Add-in**, do the following:</span></span>
    
      - <span data-ttu-id="0f121-124">В поле **Имя** укажите имя новой надстройки.</span><span class="sxs-lookup"><span data-stu-id="0f121-124">In **Name**, specify a name for the new add-in.</span></span>
    
      - <span data-ttu-id="0f121-p106">В поле **URL-адрес** укажите URL-адрес, который должен быть сопоставлен с данной надстройкой. Эти URL-адреса ограничены протоколами HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0f121-p106">In **URL**, specify the URL to be associated with the add-in. URLs are limited to http and https protocols.</span></span>

7.  <span data-ttu-id="0f121-127">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="0f121-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0f121-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0f121-128">See Also</span></span>


[<span data-ttu-id="0f121-129">Открытие меню администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0f121-129">Open Lync Server 2013 administrative tools</span></span>](lync-server-2013-open-lync-server-administrative-tools.md)  


[<span data-ttu-id="0f121-130">Настройка сервера сохраняемого сеанса беседы с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0f121-130">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)  
  

<span data-ttu-id="0f121-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0f121-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

