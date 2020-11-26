---
title: 'Lync Server 2013: изменение фильтра передачи файлов по умолчанию'
description: 'Lync Server 2013: Измените фильтр передачи файлов по умолчанию.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default file transfer filter
ms:assetid: 791774a2-0bb6-4b5b-aeb0-ff69abb170f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521017(v=OCS.15)
ms:contentKeyID: 48184584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8091dfebea87b793c56b9a670cfeeeab15ce6c44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445724"
---
# <a name="modify-the-default-file-transfer-filter-in-lync-server-2013"></a><span data-ttu-id="c03ea-103">Изменение фильтра передачи файлов по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c03ea-103">Modify the default file transfer filter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c03ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c03ea-104">

<span> </span></span></span>

<span data-ttu-id="c03ea-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="c03ea-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="c03ea-106">Lync Server 2013 предоставляет глобальный фильтр передачи файлов, который блокирует определенные типы файлов во время выполнения следующих действий, связанных с файлами, в среде Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c03ea-106">Lync Server 2013 provides a global file transfer filter that blocks specific types of files during the following file-related activities within your Lync Server 2013 deployment:</span></span>

  - <span data-ttu-id="c03ea-107">Запросы на передачу файлов в текстовых беседах (мгновенных сообщений)</span><span class="sxs-lookup"><span data-stu-id="c03ea-107">File transfer requests during instant messaging (IM) conversations</span></span>

  - <span data-ttu-id="c03ea-108">Загрузка и загрузка файлов с помощью функции выдач в клиенте Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="c03ea-108">File uploads and downloads while using the handout feature in the Office Live Meeting 2007 client</span></span>

  - <span data-ttu-id="c03ea-109">Воспроизведение мультимедиа во время конференций</span><span class="sxs-lookup"><span data-stu-id="c03ea-109">Multimedia playback during conferences</span></span>

<span data-ttu-id="c03ea-110">В зависимости от типа файлов, которые вы хотите заблокировать или разрешить, вы можете изменить глобальный фильтр с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c03ea-110">Depending on the types of files you want to block or allow, you can use Lync Server Control Panel to modify the global filter.</span></span> <span data-ttu-id="c03ea-111">Сведения о фильтрации передаваемых файлов приведены [в разделе Настройка фильтрации передачи файлов и URL-адресов для обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="c03ea-111">For details about file transfer filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-modify-the-default-file-transfer-filter"></a><span data-ttu-id="c03ea-112">Изменение фильтра передачи файлов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c03ea-112">To modify the default file transfer filter</span></span>

1.  <span data-ttu-id="c03ea-113">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="c03ea-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="c03ea-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c03ea-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c03ea-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c03ea-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c03ea-116">На панели навигации слева выберите пункт **сообщение и сведения о присутствии** , а затем щелкните **Фильтр файлов**.</span><span class="sxs-lookup"><span data-stu-id="c03ea-116">In the left navigation bar, click **IM and Presence** and then click **File Filter**.</span></span>

4.  <span data-ttu-id="c03ea-117">На странице " **Фильтр файлов** " дважды щелкните **глобальный** фильтр.</span><span class="sxs-lookup"><span data-stu-id="c03ea-117">On the **File Filter** page, double-click the **Global** filter.</span></span>

5.  <span data-ttu-id="c03ea-118">В диалоговом окне **Изменение фильтра файлов** установите флажок **включить фильтр файлов** .</span><span class="sxs-lookup"><span data-stu-id="c03ea-118">In **Edit File Filter**, select the **Enable file filter** check box.</span></span>

6.  <span data-ttu-id="c03ea-119">В раскрывающемся списке **Пересылка файлов** выберите команду **Блокировать все** или **блокировать определенные типы файлов**.</span><span class="sxs-lookup"><span data-stu-id="c03ea-119">In the **File transfer** drop-down list box, click **Block All** or **Block specific file types**.</span></span>

7.  <span data-ttu-id="c03ea-120">Если вы щелкните **Блокировать все**, перейдите к шагу 9.</span><span class="sxs-lookup"><span data-stu-id="c03ea-120">If you clicked **Block All**, skip to step 9.</span></span>

8.  <span data-ttu-id="c03ea-121">Если вы **Выблокировали определенные типы файлов**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c03ea-121">If you clicked **Block specific file types**, do the following:</span></span>
    
    1.  <span data-ttu-id="c03ea-122">Нажмите кнопку **выбрать** , чтобы изменить список расширений типов файлов, которые вы хотите заблокировать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c03ea-122">Click **Select** to modify the default list of file type extensions that you want to block.</span></span>
    
    2.  <span data-ttu-id="c03ea-123">В списке **выберите тип файла** выберите типы файлов, которые вы хотите заблокировать или разрешить, добавив или удалив их расширения из категорий в разделе **расширения типов файлов**.</span><span class="sxs-lookup"><span data-stu-id="c03ea-123">In **Select File Type**, select the file types that you want to block or allow by adding or removing their extensions from the categories under **File type extensions**.</span></span>
    
    3.  <span data-ttu-id="c03ea-124">Если вы не видите расширение для типа файла, который вы хотите заблокировать, введите его в текстовое поле в разделе **Добавление расширений типов файлов в список** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c03ea-124">If you do not see the extension for a file type that you want to block, type the extension in the text box under **Add file type extensions to the list**, and then click **Add**.</span></span>
    
    4.  <span data-ttu-id="c03ea-125">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c03ea-125">Click **OK**.</span></span>

9.  <span data-ttu-id="c03ea-126">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="c03ea-126">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c03ea-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c03ea-127">See Also</span></span>


[<span data-ttu-id="c03ea-128">Настройка фильтрации файлов и URL-адресов для обмена мгновенными сообщениями (IM) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c03ea-128">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="c03ea-129">Создание нового фильтра передачи файлов в Lync Server 2013 для определенного сайта</span><span class="sxs-lookup"><span data-stu-id="c03ea-129">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="c03ea-130">Создание фильтра URL-адресов в Lync Server 2013 для обработки гиперссылок в текстовых беседах</span><span class="sxs-lookup"><span data-stu-id="c03ea-130">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  


[<span data-ttu-id="c03ea-131">Изменение фильтра URL-адреса по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c03ea-131">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="c03ea-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c03ea-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

