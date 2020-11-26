---
title: Создание фильтра URL-адресов для обработки гиперссылок в текстовых беседах
description: Создайте новый фильтр URL-адресов для обработки гиперссылок в текстовых беседах.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new URL filter to handle hyperlinks in IM conversations
ms:assetid: d0ee01e5-f039-4a34-ac9d-659fe4e9e879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182590(v=OCS.15)
ms:contentKeyID: 48185426
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e583b3e8cbd04279ab7f54b4138a349fa0d1e85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432123"
---
# <a name="create-a-new-url-filter-in-lync-server-2013-to-handle-hyperlinks-in-im-conversations"></a><span data-ttu-id="e35ae-103">Создание фильтра URL-адресов в Lync Server 2013 для обработки гиперссылок в текстовых беседах</span><span class="sxs-lookup"><span data-stu-id="e35ae-103">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e35ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e35ae-104">

<span> </span></span></span>

<span data-ttu-id="e35ae-105">_**Тема последнего изменения:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="e35ae-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="e35ae-106">Помимо изменения глобального фильтра URL-адреса вы можете настроить пользовательские фильтры URL-адресов для отдельных сайтов в среде Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e35ae-106">In addition to modifying the global URL filter, you can configure custom URL filters for individual sites within your Lync Server 2013 deployment.</span></span> <span data-ttu-id="e35ae-107">Подробнее об фильтрации URL-адресов можно узнать [в разделе Настройка параметров передачи файлов и фильтрации URL-адресов для обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="e35ae-107">For details about URL filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-create-a-new-url-filter"></a><span data-ttu-id="e35ae-108">Создание фильтра для нового URL-адреса</span><span class="sxs-lookup"><span data-stu-id="e35ae-108">To create a new URL filter</span></span>

1.  <span data-ttu-id="e35ae-109">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="e35ae-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e35ae-110">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e35ae-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e35ae-111">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e35ae-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e35ae-112">На панели навигации слева выберите пункт **сообщение и сведения о присутствии**, а затем щелкните **Фильтр URL-адресов**.</span><span class="sxs-lookup"><span data-stu-id="e35ae-112">In the left navigation bar, click **IM and Presence**, and then click **URL Filter**.</span></span>

4.  <span data-ttu-id="e35ae-113">На странице **Фильтр URL-адресов** нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="e35ae-113">On the **URL Filter** page, click **New**.</span></span>

5.  <span data-ttu-id="e35ae-114">В списке **выберите сайт** выберите сайт, для которого вы хотите создать фильтр URL-адресов, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e35ae-114">In **Select a Site**, click the site for which you want to create the URL filter, and then click **OK**.</span></span>

6.  <span data-ttu-id="e35ae-115">В диалоговом окне **Новый фильтр URL-адресов** установите флажок **включить фильтр URL** -адресов, чтобы включить фильтрацию URL-адресов для сайта.</span><span class="sxs-lookup"><span data-stu-id="e35ae-115">In the **New URL Filter** dialog box, select the **Enable URL Filter** check box to enable URL filtering for the site.</span></span>

7.  <span data-ttu-id="e35ae-116">Чтобы заблокировать любой активный URL-адрес, содержащий файл с расширением, указанным в разделе **расширения типа файла, который будет заблокирован** в диалоговом окне **Изменение фильтра файлов**, установите флажок **блокировать URL-адреса с использованием расширения файла** .</span><span class="sxs-lookup"><span data-stu-id="e35ae-116">To block any active URL that contains a file with an extension listed under **File type extensions to block** in **Edit File Filter**, select the **Block URLs with file extension** check box.</span></span>

8.  <span data-ttu-id="e35ae-117">В раскрывающемся списке " **префикс гиперссылки** " выберите параметр, соответствующий тому, как вы хотите обрабатывать URL-адреса в мгновенных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="e35ae-117">In the **Hyperlink prefix** drop-down list box, click the option that corresponds to how you want to handle URLs in instant message conversations.</span></span>
    
    <span data-ttu-id="e35ae-118">Окно **Разрешить сообщение** позволяет отправлять пользователю предупреждение при отправке гиперссылок, которые разрешено отправлять.</span><span class="sxs-lookup"><span data-stu-id="e35ae-118">The **Allow message** box enables a warning message to be sent to the user when sending hyperlinks that are allowed to be sent.</span></span>

9.  <span data-ttu-id="e35ae-119">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="e35ae-119">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e35ae-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e35ae-120">See Also</span></span>


[<span data-ttu-id="e35ae-121">Настройка фильтрации файлов и URL-адресов для обмена мгновенными сообщениями (IM) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e35ae-121">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="e35ae-122">Создание нового фильтра передачи файлов в Lync Server 2013 для определенного сайта</span><span class="sxs-lookup"><span data-stu-id="e35ae-122">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="e35ae-123">Изменение фильтра передачи файлов по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e35ae-123">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[<span data-ttu-id="e35ae-124">Изменение фильтра URL-адреса по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e35ae-124">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="e35ae-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e35ae-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

