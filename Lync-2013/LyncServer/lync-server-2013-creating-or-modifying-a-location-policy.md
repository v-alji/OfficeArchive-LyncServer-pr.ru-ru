---
title: 'Lync Server 2013: создание или изменение политики расположения'
description: 'Lync Server 2013: создание или изменение политики расположения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying a location policy
ms:assetid: 10338418-4da4-42df-b231-f52098c08dae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687971(v=OCS.15)
ms:contentKeyID: 49733557
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba097ddb6e4ca8515c1eb33ae9d7e033821aef31
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431458"
---
# <a name="creating-or-modifying-a-location-policy-in-lync-server-2013"></a><span data-ttu-id="5d148-103">Создание и изменение политики расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d148-103">Creating or modifying a location policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d148-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d148-104">

<span> </span></span></span>

<span data-ttu-id="5d148-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5d148-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5d148-106">В Lync Server 2013 вы можете использовать политику расположения для применения параметров, которые относятся к расширенным функциям 9-1-1 (E9-1-1), а также к параметрам расположения для пользователей и контактов.</span><span class="sxs-lookup"><span data-stu-id="5d148-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="5d148-107">Политика расположения определяет, разрешено ли пользователю E9-1-1, и в каких случаях может происходить вызов экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="5d148-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="5d148-108">Например, вы можете использовать политику расположения, чтобы определить, какой номер является вызовом экстренной помощи (например, 911 в США), следует ли автоматически уведомлять корпоративную безопасность, а также как перенаправлять этот звонок.</span><span class="sxs-lookup"><span data-stu-id="5d148-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="5d148-109">Политики местоположений можно настроить в группе **Конфигурация сети** в Lync Server 2013 панели управления.</span><span class="sxs-lookup"><span data-stu-id="5d148-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="5d148-110">На панели управления Lync Server вы можете просматривать, создавать, изменять и удалять политики расположения.</span><span class="sxs-lookup"><span data-stu-id="5d148-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="5d148-111">Для создания и изменения политики расположения используйте процедуры, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="5d148-111">Use the procedures in this section to create or modify a location policy.</span></span> <span data-ttu-id="5d148-112">Подробнее об удалении политик местоположений можно узнать [в разделе Удаление политики расположения в Lync Server 2013](lync-server-2013-deleting-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="5d148-112">For details on deleting location policies, see [Deleting a location policy in Lync Server 2013](lync-server-2013-deleting-a-location-policy.md).</span></span>

<span data-ttu-id="5d148-113">В Lync Server 2013 вы можете переопределить интервал времени по умолчанию между запросами клиентов на обновление расположения в службе сведений о расположении.</span><span class="sxs-lookup"><span data-stu-id="5d148-113">In Lync Server 2013, you can override the default amount of time between client requests for a location update from the Location Information service.</span></span> <span data-ttu-id="5d148-114">Значение по умолчанию — 4 часа.</span><span class="sxs-lookup"><span data-stu-id="5d148-114">The default value is 4 hours.</span></span> <span data-ttu-id="5d148-115">Используйте командлет **Set-CsLocationPolicy** с параметром LocationRefreshInterval для переопределения значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d148-115">Use the **Set-CsLocationPolicy** cmdlet with the LocationRefreshInterval parameter to override the default value.</span></span>

<div>

## <a name="to-create-a-new-location-policy-in-lync-server-control-panel"></a><span data-ttu-id="5d148-116">Создание политики местоположений на панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="5d148-116">To create a new location policy in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="5d148-117">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="5d148-117">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5d148-118">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d148-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5d148-119">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5d148-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5d148-120">На панели навигации слева выберите пункт **Настройка сети** , а затем — **Политика расположения**.</span><span class="sxs-lookup"><span data-stu-id="5d148-120">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="5d148-121">На странице " **Политика расположения** " нажмите кнопку **создать** , а затем выберите тип политики, которую вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="5d148-121">On the **Location Policy** page, click **New** and then select the type of policy you want to create:</span></span>
    
      - <span data-ttu-id="5d148-122">Чтобы создать политику сайта, нажмите кнопку **Политика сайта**.</span><span class="sxs-lookup"><span data-stu-id="5d148-122">To create a site policy, click **Site policy**.</span></span> <span data-ttu-id="5d148-123">В списке **выберите сайт** выберите сайт, к которому требуется применить политику, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5d148-123">In **Select a Site**, choose the site to which you want the policy applied and click **OK**.</span></span> <span data-ttu-id="5d148-124">На странице " **Создание политики расположения** " в поле " **область** " отображается значение " **сайт**", а в поле " **имя** " — имя выбранного сайта.</span><span class="sxs-lookup"><span data-stu-id="5d148-124">On the **New Location Policy** page, the **Scope** field contains the value **Site**, and the **Name** field contains the name of the site you chose.</span></span> <span data-ttu-id="5d148-125">Ни одно из этих полей изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="5d148-125">You cannot modify either of these fields.</span></span> <span data-ttu-id="5d148-126">Политика сайта автоматически применяется ко всем пользователям на указанном сайте и переопределяет глобальную политику для этих пользователей.</span><span class="sxs-lookup"><span data-stu-id="5d148-126">A site policy is automatically applied to all users on the specified site and overrides the global policy for those users.</span></span>
    
      - <span data-ttu-id="5d148-127">Чтобы создать **политику пользователя**, нажмите кнопку **Политика пользователя**.</span><span class="sxs-lookup"><span data-stu-id="5d148-127">To create a **User policy**, click **User policy**.</span></span> <span data-ttu-id="5d148-128">В **новой политике расположения** поле « **область** » будет содержать значение **User**.</span><span class="sxs-lookup"><span data-stu-id="5d148-128">In the **New Location Policy**, the **Scope** field contains the value **User**.</span></span> <span data-ttu-id="5d148-129">Изменить это значение нельзя.</span><span class="sxs-lookup"><span data-stu-id="5d148-129">You cannot modify this value.</span></span> <span data-ttu-id="5d148-130">В поле **Name (имя** ) введите имя, которое вы хотите назначить этой политике.</span><span class="sxs-lookup"><span data-stu-id="5d148-130">In the **Name** field, type the name you want to give this policy.</span></span> <span data-ttu-id="5d148-131">Политика пользователя не применяется автоматически к каким-либо пользователям.</span><span class="sxs-lookup"><span data-stu-id="5d148-131">A user policy does not automatically apply to any users.</span></span> <span data-ttu-id="5d148-132">После создания политики пользователя вы должны вручную предоставить политику для пользователей или сайтов сети, к которым вы хотите применить политику.</span><span class="sxs-lookup"><span data-stu-id="5d148-132">After creating the user policy, you must manually grant the policy to the users or network sites to which you want to policy to apply.</span></span>

5.  <span data-ttu-id="5d148-133">Заполните остальные поля, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="5d148-133">Fill in the remaining fields as follows:</span></span>
    
      - <span data-ttu-id="5d148-134">**Включение расширенных служб экстренной**   помощи   Установите этот флажок, чтобы включить пользователей, связанных с этой политикой, для E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="5d148-134">**Enable enhanced emergency services**   Select this check box to enable the users associated with this policy for E9-1-1.</span></span> <span data-ttu-id="5d148-135">При включении служб экстренной помощи Пользователи Lync Server будут получать сведения о расположении при регистрации и включать эти данные при совершении экстренного звонка.</span><span class="sxs-lookup"><span data-stu-id="5d148-135">When emergency services are enabled, Lync Server clients will retrieve location information on registration and include that information when an emergency call is made.</span></span>
    
      - <span data-ttu-id="5d148-136">**Расположение**   Укажите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5d148-136">**Location**   Specify one of the following values:</span></span>
        
          - <span data-ttu-id="5d148-137">**Обязательное требование**   Пользователю будет предложено ввести сведения о расположении, когда клиент регистрируется в новом расположении.</span><span class="sxs-lookup"><span data-stu-id="5d148-137">**Required**   The user will be prompted to input location information when the client registers at a new location.</span></span> <span data-ttu-id="5d148-138">Пользователь может закрыть приглашение без ввода каких бы то ни было данных.</span><span class="sxs-lookup"><span data-stu-id="5d148-138">The user can dismiss the prompt without entering any information.</span></span> <span data-ttu-id="5d148-139">Если введены данные, поставщик услуг может сначала ответить на вызов экстренной помощи, чтобы проверить расположение перед тем, как перенаправляться в оператор PSAP (оператор 911).</span><span class="sxs-lookup"><span data-stu-id="5d148-139">If information is entered, an emergency call will first be answered by the emergency services provider to verify the location before being routed to the Public Safety Answering Point (PSAP) operator (that is, the 911 operator).</span></span>
        
          - <span data-ttu-id="5d148-140">**Не требуется**   Пользователю не будет предложено указать расположение.</span><span class="sxs-lookup"><span data-stu-id="5d148-140">**Not Required**   The user will not be prompted for a location.</span></span> <span data-ttu-id="5d148-141">Если при выполнении звонка не указана информация о местонахождении, поставщик услуг службы экстренной помощи будет отвечать на звонок и запрашивать расположение.</span><span class="sxs-lookup"><span data-stu-id="5d148-141">When a call is made with no location information, the emergency services provider will answer the call and ask for a location.</span></span>
        
          - <span data-ttu-id="5d148-142">**Заявление об отказе от ответственности**   Этот параметр аналогичен указанному **, только если** пользователь не может закрыть приглашение без ввода сведений о расположении.</span><span class="sxs-lookup"><span data-stu-id="5d148-142">**Disclaimer**   This option is the same as **Required** except that the user cannot dismiss the prompt without entering location information.</span></span> <span data-ttu-id="5d148-143">Пользователь по-прежнему может выполнить вызов экстренной помощи, но никакие другие звонки нельзя будет завершить, не вводя нужных данных.</span><span class="sxs-lookup"><span data-stu-id="5d148-143">The user can still complete an emergency call, but no other calls can be completed without entering the information.</span></span> <span data-ttu-id="5d148-144">Кроме того, текст заявления об отказе будет отображаться для пользователя, который может предупредить его последствия для ввода сведений о местоположении.</span><span class="sxs-lookup"><span data-stu-id="5d148-144">In addition, disclaimer text will be displayed to the user that can alert them to the consequences of declining to enter location information.</span></span> <span data-ttu-id="5d148-145">Чтобы настроить текст заявления об отказе, необходимо использовать командную консоль Lync Server Management Shell для запуска командлета **Set-CsLocationPolicy** или командлета **New-CsLocationPolicy** с параметром EnhancedEmergencyServiceDisclaimer.</span><span class="sxs-lookup"><span data-stu-id="5d148-145">To set the disclaimer text, you must use Lync Server Management Shell to run the **Set-CsLocationPolicy** cmdlet or the **New-CsLocationPolicy** cmdlet with the EnhancedEmergencyServiceDisclaimer parameter.</span></span> <span data-ttu-id="5d148-146">Подробные сведения можно найти в разделе [Set-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy) или [New-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy) в документации по среде управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d148-146">For details, see [Set-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy) or [New-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy) in the Lync Server Management Shell documentation.</span></span>
            
            <div>
            

            > [!NOTE]  
            > <span data-ttu-id="5d148-147">В Lync Server 2013 вы можете использовать политику расположения для установки различных отказов на использование разных национальных настроек и разных групп пользователей, в отличие от Lync Server 2010, где вы можете указать только глобальный отказ для всей Организации.</span><span class="sxs-lookup"><span data-stu-id="5d148-147">In Lync Server 2013, you can use location policy to set different disclaimers for different locales or different sets of users, unlike in Lync Server 2010 where you could specify only a global disclaimer for the entire organization.</span></span>

            
            </div>
    
      - <span data-ttu-id="5d148-148">**Использовать место только для экстренных служб**   Lync может использовать сведения о расположении по различным причинам (например, для уведомления коллег о текущем местоположении).</span><span class="sxs-lookup"><span data-stu-id="5d148-148">**Use location for emergency services only**   Lync can use location information for various reasons (for example, to notify teammates of your current location).</span></span> <span data-ttu-id="5d148-149">Установите этот флажок, чтобы убедиться, что сведения о расположении доступны только для вызова экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="5d148-149">Select this check box to ensure location information is available only for use with an emergency call.</span></span>
    
      - <span data-ttu-id="5d148-150">**Использование PSTN**   Использование общественной коммутируемой телефонной сети (PSTN), которая будет использоваться для определения направления голоса, которое будет использоваться для маршрутизации экстренных вызовов с клиентов, использующих этот профиль.</span><span class="sxs-lookup"><span data-stu-id="5d148-150">**PSTN usage**   The public switched telephone network (PSTN) usage that will be used to determine which voice route will be used to route emergency calls from clients using this profile.</span></span> <span data-ttu-id="5d148-151">Маршрут, связанный с этим использованием, должен указывать на магистраль SIP, выделенный для вызова экстренной помощи, или на шлюз с идентификационным номером для экстренной помощи (ELIN), который маршрутизирует экстренные вызовы в ближайшую точку ответа на общедоступную безопасность (PSAP).</span><span class="sxs-lookup"><span data-stu-id="5d148-151">The route associated with this usage should point to a SIP trunk dedicated to emergency calls or to an Emergency Location Identification Number (ELIN) gateway that routes emergency calls to the nearest Public Safety Answering Point (PSAP).</span></span>
    
      - <span data-ttu-id="5d148-152">**Номер для экстренного звонка**   Номер, на который можно звонить со службами экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="5d148-152">**Emergency dial number**   The number that is dialed to reach emergency services.</span></span> <span data-ttu-id="5d148-153">В США это значение 911.</span><span class="sxs-lookup"><span data-stu-id="5d148-153">In the United States this value is 911.</span></span> <span data-ttu-id="5d148-154">Строка должна состоять из цифр от 0 до 9 и может содержать от 1 до 10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5d148-154">The string must be made of the digits 0 through 9 and can be from 1 to 10 digits in length.</span></span>
    
      - <span data-ttu-id="5d148-155">**Маска вызова для экстренного набора**   Число, которое вы хотите переводить на значение номера экстренного набора номера при наборе номера.</span><span class="sxs-lookup"><span data-stu-id="5d148-155">**Emergency dial mask**   A number that you want to translate into the value of the emergency dial number value when it is dialed.</span></span> <span data-ttu-id="5d148-156">Например, если ввести значение 212 в это поле, а в поле «номер экстренного набора» — значение 911, то при попытке пользователя выполнить вызов 212 будет произведена 911.</span><span class="sxs-lookup"><span data-stu-id="5d148-156">For example, if you enter a value of 212 in this field and the emergency dial number field has a value of 911, if a user dials 212 the call will be made to 911.</span></span> <span data-ttu-id="5d148-157">Это позволяет использовать альтернативные номера для экстренного реагирования (например, если кто-то из страны или региона с другим номером для экстренного реагирования пытается набрать номер страны или региона, а не номер страны или региона, который в настоящее время находится в данный момент).</span><span class="sxs-lookup"><span data-stu-id="5d148-157">This allows for alternate emergency numbers to be dialed and still have the call reach emergency services (for example, if someone from a country or region with a different emergency number attempts to dial that country or region’s number rather than the number for the country or region they are currently in).</span></span> <span data-ttu-id="5d148-158">Вы можете определить несколько масок для экстренного набора номера, разделяя их точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="5d148-158">You can define multiple emergency dial masks by separating the values with semicolons.</span></span> <span data-ttu-id="5d148-159">Например, 212; 414.</span><span class="sxs-lookup"><span data-stu-id="5d148-159">For example, 212;414.</span></span> <span data-ttu-id="5d148-160">Максимальная длина строки — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="5d148-160">Maximum length of the string is 100 characters.</span></span> <span data-ttu-id="5d148-161">Каждый символ должен быть цифрой от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="5d148-161">Each character must be a digit 0 through 9.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="5d148-162">Убедитесь, что указанное значение маски звонка не совпадает с числом в диапазоне на расстоянии по орбите.</span><span class="sxs-lookup"><span data-stu-id="5d148-162">Ensure that the specified dial mask value is not the same as a number in a call park orbit range.</span></span> <span data-ttu-id="5d148-163">Маршрутизация на припаркованных звонках имеет приоритет над преобразованием строк в экстренном наборе.</span><span class="sxs-lookup"><span data-stu-id="5d148-163">Call park routing will take precedence over emergency dial string conversion.</span></span> <span data-ttu-id="5d148-164">Чтобы просмотреть диапазон по орбите, нажмите кнопку <STRONG>функции голоса</STRONG> на левой панели навигации, а затем выберите команду <STRONG>приостановить Звонок</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5d148-164">To see the existing call park orbit ranges, click <STRONG>Voice Features</STRONG> in the left navigation bar and then click <STRONG>Call Park</STRONG>.</span></span> <span data-ttu-id="5d148-165">Подробности можно найти <A href="lync-server-2013-configure-phone-number-extensions-for-parking-calls.md">в разделе Настройка расширений номеров телефонов для вызовов парковки в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5d148-165">For details, see <A href="lync-server-2013-configure-phone-number-extensions-for-parking-calls.md">Configure phone number extensions for parking calls in Lync Server 2013</A>.</span></span>

        
        </div>
    
      - <span data-ttu-id="5d148-166">**Универсальный код ресурса (URI) уведомления**   Один или несколько универсальных кодов ресурсов (URI) SIP, которые будут уведомлены при совершении вызова экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="5d148-166">**Notification URI**   One or more SIP Uniform Resource Identifiers (URIs) to be notified when an emergency call is made.</span></span> <span data-ttu-id="5d148-167">Например, Office для защиты компании может получать уведомления о мгновенных сообщениях во время вызова экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="5d148-167">For example, the company security office could be notified through an instant message whenever an emergency call is made.</span></span> <span data-ttu-id="5d148-168">Если расположение вызывающего абонента доступно, оно будет включено в уведомление.</span><span class="sxs-lookup"><span data-stu-id="5d148-168">If the caller’s location is available that location will be included in the notification.</span></span> <span data-ttu-id="5d148-169">В виде списка с разделителями-запятыми можно указывать несколько URI SIP.</span><span class="sxs-lookup"><span data-stu-id="5d148-169">Multiple SIP URIs can be included as a comma-separated list.</span></span> <span data-ttu-id="5d148-170">Например, "SIP: security@litwareinc. com", "SIP: kmyer@litwareinc. com".</span><span class="sxs-lookup"><span data-stu-id="5d148-170">For example, "sip:security@litwareinc.com","sip:kmyer@litwareinc.com".</span></span> <span data-ttu-id="5d148-171">Поддерживаются списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="5d148-171">Distribution lists are supported.</span></span> <span data-ttu-id="5d148-172">Строка должна содержать от 1 до 256 знаков длиной и начинаться с префикса SIP:.</span><span class="sxs-lookup"><span data-stu-id="5d148-172">The string must be from 1 to 256 characters in length and must begin with the prefix "sip:".</span></span> <span data-ttu-id="5d148-173">Пример отображения в поле URI уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5d148-173">Before you click in the Notification URI field an example is displayed.</span></span>
    
      - <span data-ttu-id="5d148-174">**URI конференции**   Универсальный код ресурса (URI) SIP, в данном случае номер телефона третьей стороны, который будет использоваться в любых совершенных звонках в экстренных случаях.</span><span class="sxs-lookup"><span data-stu-id="5d148-174">**Conference URI**   The SIP URI, in this case the telephone number, of a third party that will be conferenced in to any emergency calls that are made.</span></span> <span data-ttu-id="5d148-175">Например, Office Security Company может получать звонок при совершении вызова экстренной помощи и принимать участие в этом звонке (в зависимости от значения, заданного в поле **режим конференции** ).</span><span class="sxs-lookup"><span data-stu-id="5d148-175">For example, the company security office could receive a call when an emergency call is made and listen in or participate in that call (depending on the value supplied in the **Conference mode** field).</span></span> <span data-ttu-id="5d148-176">Строка должна содержать от 1 до 256 символов и должна начинаться с префикса SIP:.</span><span class="sxs-lookup"><span data-stu-id="5d148-176">The string must be from 1 to 256 characters in length and must begin with the prefix sip:.</span></span> <span data-ttu-id="5d148-177">Пример отображается, пока вы не щелкните внутри этого поля.</span><span class="sxs-lookup"><span data-stu-id="5d148-177">An example is displayed until you click inside this field.</span></span>
    
      - <span data-ttu-id="5d148-178">**Режим конференции**   Если вы укажете значение в поле " **URI конференции** ", **режим конференции** определяет, может ли третьим абонентом участвовать в звонке или только прослушивать ее.</span><span class="sxs-lookup"><span data-stu-id="5d148-178">**Conference mode**   If you specify a value in the **Conference URI** field, the **Conference mode** determines whether a third party can participate in the call or can only listen in.</span></span> <span data-ttu-id="5d148-179">Укажите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="5d148-179">Specify one of the following options:</span></span>
        
          - <span data-ttu-id="5d148-180">**Односторонне**   Третьим абонентом может быть только прослушивание беседы между вызывающим и оператором PSAP.</span><span class="sxs-lookup"><span data-stu-id="5d148-180">**One-way**   A third party can only listen to the conversation between the caller and the PSAP operator.</span></span>
        
          - <span data-ttu-id="5d148-181">**Двухстороннее**   Третьим абонентом может быть прослушивание и участие в вызове между вызывающим абонентом и оператором PSAP.</span><span class="sxs-lookup"><span data-stu-id="5d148-181">**Two-way**   A third party can listen in and participate in the call between the caller and the PSAP operator.</span></span>

6.  <span data-ttu-id="5d148-182">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="5d148-182">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5d148-183">При создании политики пользователя изначально политика не применяется для пользователей и сайтов сети.</span><span class="sxs-lookup"><span data-stu-id="5d148-183">When you create a user policy, initially that policy does not apply to any users or network sites.</span></span> <span data-ttu-id="5d148-184">Чтобы применить политику к пользователю, нажмите кнопку <STRONG>Пользователи</STRONG> на панели навигации слева.</span><span class="sxs-lookup"><span data-stu-id="5d148-184">To apply the policy to a user, click <STRONG>Users</STRONG> in the left navigation bar.</span></span> <span data-ttu-id="5d148-185">Найдите пользователя, которому требуется применить политику.</span><span class="sxs-lookup"><span data-stu-id="5d148-185">Find the user to which you want to apply the policy.</span></span> <span data-ttu-id="5d148-186">В меню <STRONG>Правка</STRONG> щелкните <STRONG>Подробнее</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5d148-186">On the <STRONG>Edit</STRONG> menu, click <STRONG>Show details</STRONG>.</span></span> <span data-ttu-id="5d148-187">На странице " <STRONG>изменение пользователя Lync Server</STRONG> " выберите новую политику расположения в раскрывающемся списке " <STRONG>Политика расположения</STRONG> " и нажмите кнопку " <STRONG>зафиксировать</STRONG>".</span><span class="sxs-lookup"><span data-stu-id="5d148-187">On the <STRONG>Edit Lync Server User</STRONG> page, select the new location policy from the <STRONG>Location policy</STRONG> drop-down list and then click <STRONG>Commit</STRONG>.</span></span><BR><span data-ttu-id="5d148-188">Чтобы применить политику к сетевому сайту, на левой панели навигации нажмите кнопку <STRONG>Конфигурация сети</STRONG> , а затем выберите пункт <STRONG>сайт</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5d148-188">To apply the policy to a network site, click <STRONG>Network Configuration</STRONG> in the left navigation bar and then click <STRONG>Site</STRONG>.</span></span> <span data-ttu-id="5d148-189">Найдите сетевой сайт, к которому вы хотите применить политику.</span><span class="sxs-lookup"><span data-stu-id="5d148-189">Find the network site to which you want to apply the policy.</span></span> <span data-ttu-id="5d148-190">В меню <STRONG>Правка</STRONG> щелкните <STRONG>Подробнее</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5d148-190">On the <STRONG>Edit</STRONG> menu, click <STRONG>Show details</STRONG>.</span></span> <span data-ttu-id="5d148-191">В окне " <STRONG>изменение сайта</STRONG>" выберите политику "новое расположение" в раскрывающемся списке " <STRONG>Политика расположения</STRONG> " и нажмите кнопку " <STRONG>зафиксировать</STRONG>".</span><span class="sxs-lookup"><span data-stu-id="5d148-191">In <STRONG>Edit Site</STRONG>, select the new location policy from the <STRONG>Location policy</STRONG> drop-down list and then click <STRONG>Commit</STRONG>.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-a-location-policy-in-lync-server-control-panel"></a><span data-ttu-id="5d148-192">Изменение политики расположения на панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="5d148-192">To modify a location policy in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="5d148-193">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="5d148-193">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5d148-194">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d148-194">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5d148-195">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5d148-195">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5d148-196">На панели навигации слева выберите пункт **Настройка сети** , а затем — **Политика расположения**.</span><span class="sxs-lookup"><span data-stu-id="5d148-196">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="5d148-197">На странице " **Политика расположения** " выберите политику расположения, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="5d148-197">On the **Location Policy** page, select the location policy that you want to modify.</span></span>

5.  <span data-ttu-id="5d148-198">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="5d148-198">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="5d148-199">На странице " **изменение расположения** " внесите необходимые изменения в поля (Дополнительные сведения можно найти в разделе действие 5 в описанных выше процедурах "Создание новой политики местоположений").</span><span class="sxs-lookup"><span data-stu-id="5d148-199">On the **Edit Location Policy** page, modify the fields as necessary (for details, see Step 5 in the "To create a new location policy" procedures earlier in this topic).</span></span>

7.  <span data-ttu-id="5d148-200">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="5d148-200">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5d148-201">См. также</span><span class="sxs-lookup"><span data-stu-id="5d148-201">See Also</span></span>


[<span data-ttu-id="5d148-202">Удаление политики расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d148-202">Deleting a location policy in Lync Server 2013</span></span>](lync-server-2013-deleting-a-location-policy.md)  


[<span data-ttu-id="5d148-203">Определение политики расположения для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d148-203">Defining the location policy for Lync Server 2013</span></span>](lync-server-2013-defining-the-location-policy.md)  


[<span data-ttu-id="5d148-204">Настройка расширений номеров телефонов для вызовов парковки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d148-204">Configure phone number extensions for parking calls in Lync Server 2013</span></span>](lync-server-2013-configure-phone-number-extensions-for-parking-calls.md)  
  

<span data-ttu-id="5d148-205"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d148-205"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

