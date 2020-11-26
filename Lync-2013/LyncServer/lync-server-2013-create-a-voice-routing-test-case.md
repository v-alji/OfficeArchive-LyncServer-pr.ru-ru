---
title: 'Lync Server 2013: создание тестового примера маршрутизации голосовой связи'
description: 'Lync Server 2013: Создание тестового случая голосовой маршрутизации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a voice routing test case
ms:assetid: 43a07a5b-2f20-462a-81e5-d628c18391e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425935(v=OCS.15)
ms:contentKeyID: 48183979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d81f4d39a6e3972ebf036fdaca59936f3f6b86bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432039"
---
# <a name="create-a-voice-routing-test-case-in-lync-server-2013"></a><span data-ttu-id="60952-103">Создание тестового примера маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60952-103">Create a voice routing test case in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="60952-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="60952-104">

<span> </span></span></span>

<span data-ttu-id="60952-105">_**Тема последнего изменения:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="60952-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<div>

## <a name="to-create-a-test-case"></a><span data-ttu-id="60952-106">Создание тестового случая</span><span class="sxs-lookup"><span data-stu-id="60952-106">To create a test case</span></span>

1.  <span data-ttu-id="60952-107">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="60952-107">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="60952-108">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="60952-108">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="60952-109">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="60952-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="60952-110">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="60952-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="60952-111">На панели навигации слева выберите пункт **Маршрутизация голосовых сообщений** и нажмите кнопку **проверить голосовую связь**.</span><span class="sxs-lookup"><span data-stu-id="60952-111">In the left navigation bar, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

4.  <span data-ttu-id="60952-112">На странице **Проверка маршрутизации голоса** нажмите кнопку **создать** , чтобы создать новый тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="60952-112">On the **Test Voice Routing** page, click **New** to create a new test case.</span></span>

5.  <span data-ttu-id="60952-113">В поле **имя** введите уникальное имя тестового случая.</span><span class="sxs-lookup"><span data-stu-id="60952-113">In **Name**, type in a unique name for the test case.</span></span>
    
    <span data-ttu-id="60952-114">Это имя должно быть уникальным среди всех тестовых случаев голосовой маршрутизации при развертывании вашей корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="60952-114">The name must be unique among all voice routing test cases in your Enterprise Voice deployment.</span></span> <span data-ttu-id="60952-115">Длина может составлять до 32 знаков и может содержать любые алфавитно-цифровые символы, а также символ обратной косой черты ( \\ ), точку (.) или символ подчеркивания ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="60952-115">It can be up to 32 characters in length and may contain any alphanumeric characters, in addition to the backslash (\\), period (.), or underscore (\_).</span></span>

6.  <span data-ttu-id="60952-116">В поле **номер для проверки** введите номер, который вы хотите использовать для проверки конфигурации маршрутизации, которую вы указали для этого тестового случая.</span><span class="sxs-lookup"><span data-stu-id="60952-116">In **Dialed number to test**, type in the dialed number that you want to use to test the routing configuration that you specify for this test case.</span></span> <span data-ttu-id="60952-117">На основе абонентской группы, маршрута и политики голосовой связи этот номер будет нормализован и отображен как OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="60952-117">Based on the dial plan, route, and voice policy, this number will be normalized and displayed as output.</span></span>

7.  <span data-ttu-id="60952-118">В списке **абонентская группа** выберите абонентскую группу, которая будет использоваться при выполнении теста.</span><span class="sxs-lookup"><span data-stu-id="60952-118">In the **Dial Plan** list, select the dial plan to use when running the test.</span></span> <span data-ttu-id="60952-119">По умолчанию используется глобальная абонентская группа.</span><span class="sxs-lookup"><span data-stu-id="60952-119">Default is the Global dial plan.</span></span>

8.  <span data-ttu-id="60952-120">В списке **политика голосовой связи** выберите политику голосовой связи, которую следует использовать при запуске теста.</span><span class="sxs-lookup"><span data-stu-id="60952-120">In the **Voice Policy** list, select the voice policy to use when running the test.</span></span> <span data-ttu-id="60952-121">По умолчанию используется глобальная политика голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="60952-121">Default is the Global voice policy.</span></span>

9.  <span data-ttu-id="60952-122">В поле **ожидаемый перевод** введите номер телефона в том формате, в котором оно должно отображаться после перевода.</span><span class="sxs-lookup"><span data-stu-id="60952-122">In **Expected translation**, type in the phone number in the format you expect to see it after translation.</span></span> <span data-ttu-id="60952-123">Это значение номера телефона, который вы тестируете после его перевода на первое правило нормализации, которое соответствует выбранной абонентской группе.</span><span class="sxs-lookup"><span data-stu-id="60952-123">This is the value of the phone number that you are testing after it has been translated by the first normalization rule that matches in the selected dial plan.</span></span> <span data-ttu-id="60952-124">При выполнении тестового случая, если проверяемое число не приводит к значению в **ожидаемом переводе**, тест завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="60952-124">When you run the test case, if the number you are testing does not result in the value in **Expected translation**, the test fails.</span></span>

10. <span data-ttu-id="60952-125">Необязательно В списке **ожидаемых сетей PSTN** вы можете выбрать запись использования общественной коммутируемой телефонной сети (PSTN), которая должна использоваться при запуске тестового случая на основе указанной абонентской группы и политики голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="60952-125">(Optional) In the **Expected PSTN usage** list, you can select the public switched telephone network (PSTN) usage record that you expect to be used when you run the test case, based on the specified dial plan and voice policy.</span></span> <span data-ttu-id="60952-126">Если используется другая запись использования PSTN, тест завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="60952-126">If a different PSTN usage record is used, the test fails.</span></span>

11. <span data-ttu-id="60952-127">Необязательно В списке **Ожидаемый маршрут** вы можете выбрать маршрут голосовой связи, который будет использоваться при запуске тестового случая на основе указанной абонентской группы и политики голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="60952-127">(Optional) In the **Expected route** list, you can select the voice route that you expect to be used when you run the test case, based on the specified dial plan and voice policy.</span></span> <span data-ttu-id="60952-128">Если используется другой голосовой маршрут, тест завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="60952-128">If a different voice route is used, the test fails.</span></span>

12. <span data-ttu-id="60952-129">Необязательно Нажмите кнопку **выполнить** , чтобы запустить тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="60952-129">(Optional) Click **Run** to run the test case.</span></span> <span data-ttu-id="60952-130">Результаты отображаются на правой панели страницы.</span><span class="sxs-lookup"><span data-stu-id="60952-130">The results are shown in the right panel of the page.</span></span>

13. <span data-ttu-id="60952-131">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="60952-131">Click **OK**.</span></span>

14. <span data-ttu-id="60952-132">Нажмите кнопку **Сохранить**, а затем нажмите кнопку **Сохранить все**.</span><span class="sxs-lookup"><span data-stu-id="60952-132">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="60952-133">Каждый раз, когда вы создаете тестовый случай для голосовой маршрутизации, необходимо выполнить команду <STRONG>commit all</STRONG> , чтобы опубликовать изменение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="60952-133">Whenever you create a voice routing test case, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="60952-134">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="60952-134">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="60952-135">Если абонентская группа, используемая в тесте, нормализует телефонные номера, которые начинаются со знака плюс (например, + 12065551219), этот план может вызвать сбой теста маршрутизации голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="60952-135">If the dial plan being employed in the test normalizes phone numbers that begin with a plus sign (for example, +12065551219), that plan might cause the voice routing test to fail.</span></span> <span data-ttu-id="60952-136">(Абонентская группа и маршрут голосовой связи будут работать, и на самом деле Test-CsDialPlan будет выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="60952-136">(The dial plan and the voice route will work; in fact, Test-CsDialPlan will succeed.</span></span> <span data-ttu-id="60952-137">Однако проверка маршрутизации голосовой связи может завершиться ошибкой.) Это то, что следует учитывать при тестировании голосовых маршрутов.</span><span class="sxs-lookup"><span data-stu-id="60952-137">However, the voice routing test might fail.) This is something to keep in mind when testing voice routes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="60952-138">См. также</span><span class="sxs-lookup"><span data-stu-id="60952-138">See Also</span></span>


[<span data-ttu-id="60952-139">Экспорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60952-139">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)  
[<span data-ttu-id="60952-140">Импорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60952-140">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  


[<span data-ttu-id="60952-141">Настройка абонентских групп в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60952-141">Configuring dial plans in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-plans.md)  
[<span data-ttu-id="60952-142">Настройка политик голосовой связи, записей использования КТСОП и голосовых маршрутов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60952-142">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)  
  

<span data-ttu-id="60952-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="60952-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

