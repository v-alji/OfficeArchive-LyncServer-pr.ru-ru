---
title: Создание и изменение правила нормализации с помощью построения правила нормализации
description: Создание или изменение правила нормализации с помощью построения правила нормализации.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a normalization rule by using Build a Normalization Rule
ms:assetid: e8547d7b-f74d-4a73-9a7d-df20d7a87fcd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399036(v=OCS.15)
ms:contentKeyID: 48185889
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 824936359c070090ad4225a3ead6e8e46fe14785
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431754"
---
# <a name="create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule-in-lync-server-2013"></a><span data-ttu-id="a3cc3-103">Создание и изменение правила нормализации с помощью сборки правила нормализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3cc3-103">Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3cc3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3cc3-104">

<span> </span></span></span>

<span data-ttu-id="a3cc3-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a3cc3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a3cc3-106">Если вы хотите создать или изменить правило нормализации на панели управления Lync Server, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-106">Complete the following steps if you want to create or modify a normalization rule in Lync Server Control Panel.</span></span> <span data-ttu-id="a3cc3-107">Кроме того, если вы хотите создать или изменить правило нормализации вручную, ознакомьтесь со сведениями [Создание или изменение правила нормализации вручную в Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-manually.md).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-107">Alternatively, if you want to create or modify a normalization rule manually, see [Create or modify a normalization rule manually in Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-manually.md).</span></span>

<div>

## <a name="to-define-a-rule-by-using-build-a-normalization-rule"></a><span data-ttu-id="a3cc3-108">Определение правила с помощью построения правила нормализации</span><span class="sxs-lookup"><span data-stu-id="a3cc3-108">To define a rule by using Build a Normalization Rule</span></span>

1.  <span data-ttu-id="a3cc3-109">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="a3cc3-110">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="a3cc3-111">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a3cc3-112">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a3cc3-113">Необязательно Выполните действия, описанные в статье [Создание абонентской группы в Lync server 2013](lync-server-2013-create-a-dial-plan.md) с шагом 11, или [измените абонентскую группу в Lync Server 2013 на](lync-server-2013-modify-a-dial-plan.md) этапе 10.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-113">(Optional) Follow the steps in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) through step 11 or [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md) through step 10.</span></span>

4.  <span data-ttu-id="a3cc3-114">В разделе **создания** или **редактирования правила нормализации** в поле **Имя** введите имя, описывающее нормализуемый числовой шаблон (например, назовите правило нормализации **5DigitExtension**).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-114">In **New Normalization Rule** or **Edit Normalization Rule**, type a name that describes the number pattern being normalized in **Name** (for example, **5DigitExtension**).</span></span>

5.  <span data-ttu-id="a3cc3-115">В поле **Описание** введите описание правила нормализации (например, "Преобразование пятизначных добавочных номеров") (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-115">(Optional) In **Description**, type a description of the normalization rule (for example, "Translates 5-digit extensions").</span></span>

6.  <span data-ttu-id="a3cc3-116">В разделе **Построение правила нормализации** введите значения в следующих полях.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-116">In **Build a Normalization Rule**, enter values in the following fields:</span></span>
    
      - <span data-ttu-id="a3cc3-117">**Начальные цифры**   (необязательно) укажите начальные цифры номеров, которые должны соответствовать шаблону.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-117">**Starting digits**   (Optional) Specify the leading digits of dialed numbers you want the pattern to match.</span></span> <span data-ttu-id="a3cc3-118">Например, введите **425** , если вы хотите, чтобы шаблон соответствовал номерам, набираемым начиная с 425.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-118">For example, type **425** if you want the pattern to match dialed numbers beginning with 425.</span></span>
    
      - <span data-ttu-id="a3cc3-119">**Длина**   Укажите количество цифр в шаблоне соответствия и выберите, должен ли шаблон соответствовать номерам в точности этой длины, номерам не короче этой длины или номерам любой длины.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-119">**Length**   Specify the number of digits in the matching pattern and select whether you want the pattern to match this length exactly, match dialed numbers that are at least this length, or match dialed numbers of any length.</span></span>
    
      - <span data-ttu-id="a3cc3-120">**Цифры для удаления**   Укажите количество начальных цифр для удаления из набираемых номеров, которые должны соответствовать шаблону (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-120">**Digits to remove**   (Optional) Specify the number of starting digits to be removed from dialed numbers you want the pattern to match.</span></span>
    
      - <span data-ttu-id="a3cc3-121">**Цифры для добавления**   Укажите количество цифр для добавления к набираемым номерам, которые должны соответствовать шаблону (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-121">**Digits to add**   (Optional) Specify digits to be added to dialed numbers you want the pattern to match.</span></span>
    
    <span data-ttu-id="a3cc3-p105">Значения, введенные в этих полях, отражаются в полях **Шаблон для поиска соответствия** и **Правило трансляции**. Например, если не заполнять поле **Начальные цифры**, ввести **7** в поле **Длина**, выбрать **Точно** и ввести **0** в поле **Цифры для удаления**, в поле **Шаблон для поиска соответствия** отображается следующее итоговое регулярное выражение:</span><span class="sxs-lookup"><span data-stu-id="a3cc3-p105">The values you enter in these fields are reflected in **Pattern to match** and **Translation rule**. For example, if you leave **Starting digits** empty, type **7** into the **Length** field and select **Exactly**, and specify **0** in **Digits to remove**, the resulting regular expression in the **Pattern to match** is:</span></span>
    
    <span data-ttu-id="a3cc3-124">**^ ( \\ d {7} ) $**</span><span class="sxs-lookup"><span data-stu-id="a3cc3-124">**^(\\d{7})$**</span></span>

7.  <span data-ttu-id="a3cc3-125">В поле **Правило трансляции** укажите шаблон для формата преобразованных телефонных номеров E.164 следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-125">In **Translation rule**, specify a pattern for the format of translated E.164 phone numbers as follows:</span></span>
    
      - <span data-ttu-id="a3cc3-126">Значение количества цифр, указанных в шаблоне соответствия.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-126">A value that represents the number of digits specified in the matching pattern.</span></span> <span data-ttu-id="a3cc3-127">Например, если шаблон соответствует **^ ( \\ d {7} ) $** , **$1** в правиле перевода представляет номера из 7 цифр в наборе.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-127">For example, if the matching pattern is **^(\\d{7})$** then **$1** in the translation rule represents 7-digit dialed numbers.</span></span>
    
      - <span data-ttu-id="a3cc3-128">В поле **Цифры для добавления** введите значение, указывающее цифры, которые должны добавляться в начале преобразуемого номера, например, **+1425** (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-128">(Optional) Type a value into the **Digits to add** field to specify digits to be prepended to the translated number (for example, **+1425**).</span></span>
    
    <span data-ttu-id="a3cc3-129">Например, если **в** качестве шаблона для набора номера указан параметр **^ ( \\ d {7} ) $** , а в качестве шаблона **правила перевода** указана **+ 1425 $1** как шаблон для номеров телефонов E. 164, правило нормализует 5550100 в + 14255550100.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-129">For example, if **Pattern to match** contains **^(\\d{7})$** as the pattern for dialed numbers and **Translation rule** contains **+1425$1** as the pattern for E.164 phone numbers, the rule normalizes 5550100 to +14255550100.</span></span>

8.  <span data-ttu-id="a3cc3-130">Если в результате применения правила нормализации получается внутренний телефонный номер организации, выберите **Внутреннее расширение** (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-130">(Optional) If the normalization rule results in a phone number that is internal to your organization, select **Internal extension**.</span></span>

9.  <span data-ttu-id="a3cc3-p107">Введите номер для проверки правила нормализации, затем нажмите кнопку **Перейти** (необязательно). Результаты проверки отображаются под полем **Введите номер телефона для проверки**.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-p107">(Optional) Enter a number to test the normalization rule, and then click **Go**. The test results are displayed under **Enter a number to test**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="a3cc3-133">Вы можете сохранить правило нормализации, которое еще не прошло тест, а затем настроить его позже.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-133">You can save a normalization rule that does not yet pass the test and then reconfigure it later.</span></span> <span data-ttu-id="a3cc3-134">Подробные сведения можно найти <A href="lync-server-2013-test-voice-routing.md">в разделе Проверка маршрутизации голосовой связи в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-134">For details, see <A href="lync-server-2013-test-voice-routing.md">Test voice routing in Lync Server 2013</A>.</span></span>

    
    </div>

10. <span data-ttu-id="a3cc3-135">Нажмите кнопку **ОК** для сохранения правила нормализации.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-135">Click **OK** to save the normalization rule.</span></span>

11. <span data-ttu-id="a3cc3-136">Нажмите кнопку **ОК** для сохранения абонентской группы.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-136">Click **OK** to save the dial plan.</span></span>

12. <span data-ttu-id="a3cc3-137">На странице **Абонентская группа** нажмите кнопку **Сохранить**, затем **Сохранить все**.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-137">On the **Dial Plan** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="a3cc3-138">Каждый раз, когда вы создаете или изменяете правило нормализации, необходимо выполнить команду <STRONG>commit all</STRONG> , чтобы опубликовать изменение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-138">Whenever you create or change a normalization rule, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="a3cc3-139">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-139">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a3cc3-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a3cc3-140">See Also</span></span>


[<span data-ttu-id="a3cc3-141">Создание или изменение правила нормализации вручную в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3cc3-141">Create or modify a normalization rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)  
[<span data-ttu-id="a3cc3-142">Создание абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3cc3-142">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="a3cc3-143">Изменение абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3cc3-143">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
[<span data-ttu-id="a3cc3-144">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3cc3-144">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="a3cc3-145">Тестирование голосовой маршрутизации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3cc3-145">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="a3cc3-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3cc3-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

