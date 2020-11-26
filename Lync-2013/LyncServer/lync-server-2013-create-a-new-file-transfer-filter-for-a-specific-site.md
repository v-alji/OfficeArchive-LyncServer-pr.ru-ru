---
title: 'Lync Server 2013: создание нового фильтра передачи файлов для определенного сайта'
description: 'Lync Server 2013: создание нового фильтра передачи файлов для определенного сайта.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new file transfer filter for a specific site
ms:assetid: d0006487-5217-491c-b730-e6c551cd9825
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182589(v=OCS.15)
ms:contentKeyID: 48185577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d3b5003711c2f2e74b726809fba5da6d9fd0aa57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432172"
---
# <a name="create-a-new-file-transfer-filter-in-lync-server-2013-for-a-specific-site"></a><span data-ttu-id="233dd-103">Создание нового фильтра передачи файлов в Lync Server 2013 для определенного сайта</span><span class="sxs-lookup"><span data-stu-id="233dd-103">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="233dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="233dd-104">

<span> </span></span></span>

<span data-ttu-id="233dd-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="233dd-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="233dd-106">Помимо изменения глобального фильтра передачи файлов, вы можете настроить пользовательские фильтры передачи файлов для определенных сайтов в среде Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="233dd-106">In addition to modifying the global file transfer filter, you can configure custom file transfer filters for specific sites within your Lync Server 2013 deployment.</span></span> <span data-ttu-id="233dd-107">Сведения о фильтрации передаваемых файлов приведены [в разделе Настройка фильтрации передачи файлов и URL-адресов для обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="233dd-107">For details about file transfer filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-create-a-file-transfer-filter-for-a-specific-site"></a><span data-ttu-id="233dd-108">Создание фильтра передачи файлов для определенного сайта</span><span class="sxs-lookup"><span data-stu-id="233dd-108">To create a file transfer filter for a specific site</span></span>

1.  <span data-ttu-id="233dd-109">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="233dd-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="233dd-110">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="233dd-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="233dd-111">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="233dd-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="233dd-112">На панели навигации слева выберите пункт **сообщение и сведения о присутствии** , а затем щелкните **Фильтр файлов**.</span><span class="sxs-lookup"><span data-stu-id="233dd-112">In the left navigation bar, click **IM and Presence** and then click **File Filter**.</span></span>

4.  <span data-ttu-id="233dd-113">На странице " **Фильтр файлов** " нажмите кнопку " **создать**".</span><span class="sxs-lookup"><span data-stu-id="233dd-113">On the **File Filter** page, click **New**.</span></span>

5.  <span data-ttu-id="233dd-114">В диалоговом окне **выберите сайт** выберите сайт, для которого вы хотите создать фильтр передачи файлов, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="233dd-114">In the **Select a Site** dialog box, click the site for which you want to create the file transfer filter, and then click **OK**.</span></span>

6.  <span data-ttu-id="233dd-115">В диалоговом окне **Новый фильтр файлов** установите флажок **включить фильтр файлов** .</span><span class="sxs-lookup"><span data-stu-id="233dd-115">In **New File Filter**, click the **Enable file filter** check box.</span></span>

7.  <span data-ttu-id="233dd-116">В раскрывающемся списке **Передача файлов** выберите команду **Блокировать все** или **блокировать определенные типы файлов**.</span><span class="sxs-lookup"><span data-stu-id="233dd-116">In **File transfer** drop-down list box, click **Block All** or **Block specific file types**.</span></span>

8.  <span data-ttu-id="233dd-117">Если вы щелкните **Блокировать все**, перейдите к шагу 10.</span><span class="sxs-lookup"><span data-stu-id="233dd-117">If you clicked **Block All**, skip to step 10.</span></span>

9.  <span data-ttu-id="233dd-118">Если вы **Выблокировали определенные типы файлов**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="233dd-118">If you clicked **Block specific file types**, do the following:</span></span>
    
    1.  <span data-ttu-id="233dd-119">Нажмите кнопку **выбрать** , чтобы изменить список расширений типов файлов, которые вы хотите заблокировать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="233dd-119">Click **Select** to modify the default list of file type extensions that you want to block.</span></span>
    
    2.  <span data-ttu-id="233dd-120">В диалоговом окне **Выбор типа файлов** выберите типы файлов, которые вы хотите заблокировать или разрешить, добавив или удалив их расширения из категорий в разделе **расширения типов файлов**.</span><span class="sxs-lookup"><span data-stu-id="233dd-120">In the **Select File Type** dialog box, select the file types that you want to block or allow by adding or removing their extensions from the categories under **File type extensions**.</span></span>
    
    3.  <span data-ttu-id="233dd-121">Если вы не видите расширение для типа файла, который вы хотите заблокировать, введите его в текстовое поле в разделе **Добавление расширений типов файлов в список** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="233dd-121">If you do not see the extension for a file type that you want to block, type the extension in the text box under **Add file type extensions to the list**, and then click **Add**.</span></span>
    
    4.  <span data-ttu-id="233dd-122">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="233dd-122">Click **OK**.</span></span>

10. <span data-ttu-id="233dd-123">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="233dd-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="233dd-124">См. также</span><span class="sxs-lookup"><span data-stu-id="233dd-124">See Also</span></span>


[<span data-ttu-id="233dd-125">Настройка фильтрации файлов и URL-адресов для обмена мгновенными сообщениями (IM) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="233dd-125">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="233dd-126">Создание фильтра URL-адресов в Lync Server 2013 для обработки гиперссылок в текстовых беседах</span><span class="sxs-lookup"><span data-stu-id="233dd-126">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="233dd-127">Изменение фильтра передачи файлов по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="233dd-127">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[<span data-ttu-id="233dd-128">Изменение фильтра URL-адреса по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="233dd-128">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="233dd-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="233dd-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

