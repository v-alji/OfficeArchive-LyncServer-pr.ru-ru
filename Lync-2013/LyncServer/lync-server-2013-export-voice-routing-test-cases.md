---
title: 'Lync Server 2013: экспорт тестовых примеров маршрутизации голосовой связи'
description: 'Lync Server 2013: экспорт тестовых случаев маршрутизации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export voice routing test cases
ms:assetid: 489ac472-1a35-4755-b390-48f7cdf31e94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425957(v=OCS.15)
ms:contentKeyID: 48184050
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 934bd183a17c46cf82fe5bc04faaa55a9bbe4731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428351"
---
# <a name="export-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="c3820-103">Экспорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c3820-103">Export voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3820-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3820-104">

<span> </span></span></span>

<span data-ttu-id="c3820-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="c3820-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="c3820-106">С помощью тестовых случаев вы можете проверить Голосовые маршруты в вашей организации: вы определяете, как набираемый номер, а также с помощью абонентской группы и политики голосовой связи, и Lync Server может проверить, что при условии, что при наличии этих условий предоставленный вами номер может успешно перенаправляться в сеть PSTN.</span><span class="sxs-lookup"><span data-stu-id="c3820-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="c3820-107">Тестовые случаи, которые можно создать с помощью панели управления Lync Server, обычно сохраняются только на сервере, где они были созданы и запущены.</span><span class="sxs-lookup"><span data-stu-id="c3820-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="c3820-108">Однако эти тестовые случаи можно экспортировать как XML-файлы (с расширением vTest), а затем импортировать на другие серверы.</span><span class="sxs-lookup"><span data-stu-id="c3820-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="c3820-109">Это позволяет выполнять одни и те же тесты на разных компьютерах, расположенных в разных точках топологии.</span><span class="sxs-lookup"><span data-stu-id="c3820-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-export-a-voice-routing-test-case"></a><span data-ttu-id="c3820-110">Экспорт тестового случая голосовой маршрутизации</span><span class="sxs-lookup"><span data-stu-id="c3820-110">To export a voice routing test case</span></span>

1.  <span data-ttu-id="c3820-111">На панели управления Lync Server откройте вкладку **Маршрутизация голоса** и выберите пункт **Проверка маршрутизации голоса**.</span><span class="sxs-lookup"><span data-stu-id="c3820-111">In Lync Server Control Panel, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

2.  <span data-ttu-id="c3820-112">На вкладке **Проверка маршрутизации голоса** выберите тестовый случай (или тестовые случаи), который нужно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="c3820-112">On the **Test Voice Routing** tab, select the test case (or test cases) to be exported.</span></span> <span data-ttu-id="c3820-113">Чтобы выбрать несколько тестовых случаев, щелкните первый из них, а затем, удерживая нажатой клавишу CTRL, выберите дополнительные экспортируемые варианты.</span><span class="sxs-lookup"><span data-stu-id="c3820-113">To select multiple test cases, click the first case to be exported, then hold down the Ctrl key and select the additional cases to be exported.</span></span>

3.  <span data-ttu-id="c3820-114">Нажмите кнопку **действие** и выберите пункт **Экспорт тестовых случаев**.</span><span class="sxs-lookup"><span data-stu-id="c3820-114">Click **Action**, then click **Export test cases**.</span></span>

4.  <span data-ttu-id="c3820-115">В диалоговом окне **Сохранить как** выберите папку для хранения экспортированных тестовых случаев и введите имя для РЕЗУЛЬТИРУЮЩЕГО XML-файла в поле **имя файла** .</span><span class="sxs-lookup"><span data-stu-id="c3820-115">In the **Save As** dialog box, select a folder to store the exported test cases and type a name for the resulting XML file in the **File name** box.</span></span> <span data-ttu-id="c3820-116">Обратите внимание, что при экспорте нескольких тестов все эти тестовые случаи будут сохранены в одном XML-файле.</span><span class="sxs-lookup"><span data-stu-id="c3820-116">Note that if you are exporting multiple tests cases all of these test cases will be saved to a single XML file.</span></span>

5.  <span data-ttu-id="c3820-117">Чтобы сохранить тестовые случаи, нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c3820-117">To save the test cases, click **Save**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c3820-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c3820-118">See Also</span></span>


[<span data-ttu-id="c3820-119">Импорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c3820-119">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  
  

<span data-ttu-id="c3820-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3820-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

