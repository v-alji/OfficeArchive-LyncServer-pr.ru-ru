---
title: 'Lync Server 2013: импорт тестовых примеров маршрутизации голосовой связи'
description: 'Lync Server 2013: Импорт тестовых случаев маршрутизации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import voice routing test cases
ms:assetid: 6546e24c-9ad2-428b-92b2-63948ed0f884
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398460(v=OCS.15)
ms:contentKeyID: 48184325
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06ce1b144de03406b7b78d6957371ed2bc303e95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399556"
---
# <a name="import-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="46269-103">Импорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46269-103">Import voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46269-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46269-104">

<span> </span></span></span>

<span data-ttu-id="46269-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="46269-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="46269-106">Тестовые случаи позволяют тестировать маршруты к голосовой связи в вашей организации: вы определяете, какие именно номера нужно набрать, а также о том, как будет использоваться абонентская группа и голосовая политика, а Lync Server 2013 сможет проверить, что при наличии этих условий предоставленный вами номер может успешно перенаправляться в сеть PSTN.</span><span class="sxs-lookup"><span data-stu-id="46269-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server 2013 can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="46269-107">Тестовые случаи, которые можно создать с помощью панели управления Lync Server, обычно сохраняются только на сервере, где они были созданы и запущены.</span><span class="sxs-lookup"><span data-stu-id="46269-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="46269-108">Однако эти тестовые случаи можно экспортировать как XML-файлы (с расширением vTest), а затем импортировать на другие серверы.</span><span class="sxs-lookup"><span data-stu-id="46269-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="46269-109">Это позволяет выполнять одни и те же тесты на разных компьютерах, расположенных в разных точках топологии.</span><span class="sxs-lookup"><span data-stu-id="46269-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-import-a-voice-routing-test-case"></a><span data-ttu-id="46269-110">Импорт тестового случая голосовой маршрутизации</span><span class="sxs-lookup"><span data-stu-id="46269-110">To import a voice routing test case</span></span>

1.  <span data-ttu-id="46269-111">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="46269-111">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="46269-112">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="46269-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="46269-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="46269-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="46269-114">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="46269-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="46269-115">В левой области навигации щелкните элемент **Маршрутизация голосовой связи**.</span><span class="sxs-lookup"><span data-stu-id="46269-115">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="46269-116">В меню **действия** выберите команду **Импорт тестовых случаев**.</span><span class="sxs-lookup"><span data-stu-id="46269-116">On the **Actions** menu, click **Import test cases**.</span></span>

5.  <span data-ttu-id="46269-117">Найдите файл тестового случая (vTest), который вы хотите импортировать, и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="46269-117">Find the test case file (.vtest) that you want to import, and then click **Open**.</span></span>

6.  <span data-ttu-id="46269-118">Нажмите кнопку **Сохранить**, а затем нажмите кнопку **Сохранить все**.</span><span class="sxs-lookup"><span data-stu-id="46269-118">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="46269-119">Каждый раз, когда вы импортируете vTest-файл, необходимо выполнить команду <STRONG>commit all</STRONG> для публикации тестового случая.</span><span class="sxs-lookup"><span data-stu-id="46269-119">Whenever you import a .vtest file, you must run the <STRONG>Commit all</STRONG> command to publish the test case.</span></span> <span data-ttu-id="46269-120">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="46269-120">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="46269-121">См. также</span><span class="sxs-lookup"><span data-stu-id="46269-121">See Also</span></span>


[<span data-ttu-id="46269-122">Экспорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46269-122">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)  
  

<span data-ttu-id="46269-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46269-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

