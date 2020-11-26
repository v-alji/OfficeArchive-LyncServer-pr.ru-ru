---
title: 'Lync Server 2013: Просмотр сведений о КОНТАКТах пользователя'
description: 'Lync Server 2013: Просмотр сведений о КОНТАКТах пользователя.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View user PIN information
ms:assetid: 59e38117-8112-4851-82ac-a746ffa0f89d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688067(v=OCS.15)
ms:contentKeyID: 49733661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 56f0808e645a2589841ff70d4923fa2de2c020ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444023"
---
# <a name="view-user-pin-information-in-lync-server-2013"></a><span data-ttu-id="25e72-103">Просмотр сведений о ПИН-коде пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25e72-103">View user PIN information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25e72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25e72-104">

<span> </span></span></span>

<span data-ttu-id="25e72-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="25e72-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="25e72-106">Чтобы присоединиться к Конференции с телефонным подключением в качестве пользователя, прошедшего проверку подлинности, пользователю Lync Server 2013 с учетными данными доменных служб Active Directory (AD DS) требуется персональный идентификационный номер (ПИН-код).</span><span class="sxs-lookup"><span data-stu-id="25e72-106">To join a dial-in conference as an authenticated user, a Lync Server 2013 user with Active Directory Domain Services (AD DS) credentials requires a personal identification number (PIN).</span></span> <span data-ttu-id="25e72-107">КОНТАКТНЫЕ данные пользователя можно просмотреть на панели управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25e72-107">You can view a user’s PIN information from Lync Server 2013 Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="25e72-108">Можно просмотреть сведения о состоянии ПИН, такие как когда ПИН был определен или когда был в последний раз изменен, однако сведения о состоянии не содержат самого ПИН.</span><span class="sxs-lookup"><span data-stu-id="25e72-108">You can view PIN status information such as whether the PIN has been set or when the PIN was last changed, but you cannot see the current PIN by looking at the PIN status.</span></span> <span data-ttu-id="25e72-109">Если пользователь потерял свой ПИН-код, вы можете сбросить его, следуя инструкциям в разделе <A href="lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md">Настройка контакта конференц-связи с телефонным подключением пользователя в Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="25e72-109">If a user has lost their PIN, you can reset it by following the procedures in <A href="lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md">Set a user's dial-in conferencing PIN in Lync Server 2013</A></span></span>



</div>

<div>

## <a name="to-view-a-users-pin-in-lync-server-control-panel"></a><span data-ttu-id="25e72-110">Просмотр PIN-кода пользователя на панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="25e72-110">To view a user’s PIN in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="25e72-111">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="25e72-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="25e72-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="25e72-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="25e72-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="25e72-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="25e72-114">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="25e72-114">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="25e72-115">Используйте один из следующих методов для обнаружения пользователя:</span><span class="sxs-lookup"><span data-stu-id="25e72-115">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="25e72-116">В поле **Поиск пользователей** введите отображаемое имя (полностью или первую его часть), имя, фамилию, имя учетной записи SAM (Security Accounts Manager — диспетчер учетных записей безопасности), SIP-адрес или линейный идентификатор URI (Uniform Resource Identifier — универсальный код ресурса) учетной записи пользователя, а затем щелкните **Найти**.</span><span class="sxs-lookup"><span data-stu-id="25e72-116">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="25e72-117">Если у вас есть сохраненный запрос, щелкните значок **Открыть запрос**. С помощью диалогового окна **Открыть** загрузите запрос (файл .usf), а затем щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="25e72-117">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="25e72-118">(Необязательно) Задайте дополнительные критерии поиска, чтобы сократить количество результатов:</span><span class="sxs-lookup"><span data-stu-id="25e72-118">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="25e72-119">Щелкните **Добавить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="25e72-119">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="25e72-120">Введите свойства пользователя; для это введите его или щелкните стрелку в раскрывающемся списке, чтобы выбрать свойство.</span><span class="sxs-lookup"><span data-stu-id="25e72-120">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="25e72-121">В раскрывающемся списке **Равно** щелкните оператор (например, **Равно** или **Не равно**).</span><span class="sxs-lookup"><span data-stu-id="25e72-121">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="25e72-122">В зависимости от выбранного свойства пользователя, введите условия, которые хотели бы использовать для фильтрации результатов поиска, введя их с клавиатуры или щелкнув стрелку соответствующего раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="25e72-122">Depending on the user property you selected, enter the criteria that you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        
        <div>
        

        > [!TIP]  
        > <span data-ttu-id="25e72-123">Чтобы добавить в запрос дополнительные условия поиска, щелкните <STRONG>Добавить фильтр</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="25e72-123">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

        
        </div>
    
    5.  <span data-ttu-id="25e72-124">Щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="25e72-124">Click **Find**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="25e72-p104">Если ПИН-код заблокирован, перед определением необходимо его разблокировать. Чтобы разблокировать ПИН-код, щелкните <STRONG>Действие</STRONG>, затем <STRONG>Разблокировать ПИН-код</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="25e72-p104">If the PIN is locked, you must unlock the PIN before you can set it. To unlock the PIN, click the user, click <STRONG>Action</STRONG>, and then click <STRONG>Unlock PIN</STRONG>.</span></span>

    
    </div>

6.  <span data-ttu-id="25e72-127">Щелкните пользователя в результатах поиска, щелкните **Действие**, затем щелкните **Просмотреть состояние ПИН-кода**.</span><span class="sxs-lookup"><span data-stu-id="25e72-127">Click a user in the search results, click **Action**, and then click **View PIN status**.</span></span>

</div>

<div>

## <a name="viewing-user-pin-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="25e72-128">Просмотр сведений о ПИН-коде пользователя с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="25e72-128">Viewing User PIN Information by Using Windows PowerShell cmdlets</span></span>

<span data-ttu-id="25e72-129">You can view user PIN information by using the Get-CsClientPinInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25e72-129">You can view user PIN information by using the Get-CsClientPinInfo cmdlet.</span></span> <span data-ttu-id="25e72-130">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25e72-130">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="25e72-131">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="25e72-131">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-user-pin-information"></a><span data-ttu-id="25e72-132">Порядок просмотра сведений о ПИН-коде пользователя</span><span class="sxs-lookup"><span data-stu-id="25e72-132">To view user PIN information</span></span>

  - <span data-ttu-id="25e72-133">Чтобы просмотреть сведения о ПИН-коде для пользователя, введите следующую команду в командной консоли Lync Server Management Shell и нажмите клавишу ВВОД:</span><span class="sxs-lookup"><span data-stu-id="25e72-133">To view PIN information for a user, type a command similar to the following in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsClientPinInfo -Identity "Ken Myer"
    
    <span data-ttu-id="25e72-134">Команда возвращает примерно следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="25e72-134">That will return information similar to this:</span></span>
    
        Identity          : sip:kenmyer@litwareinc.com
        IsPinSet          : False
        IsLockedOut       : False
        LastPinChangeTime : 9/25/2012 1:35:03 PM
        PinExpirationTime :

</div>

<span data-ttu-id="25e72-135">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsConferenceDisclaimer](https://docs.microsoft.com/powershell/module/skype/Get-CsConferenceDisclaimer) .</span><span class="sxs-lookup"><span data-stu-id="25e72-135">For more information, see the help topic for the [Get-CsConferenceDisclaimer](https://docs.microsoft.com/powershell/module/skype/Get-CsConferenceDisclaimer) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="25e72-136">См. также</span><span class="sxs-lookup"><span data-stu-id="25e72-136">See Also</span></span>


[<span data-ttu-id="25e72-137">Установка ПИН-кода конференц-связи с телефонным подключением пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25e72-137">Set a user's dial-in conferencing PIN in Lync Server 2013</span></span>](lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md)  
[<span data-ttu-id="25e72-138">Блокировка и Разблокировка PIN-кода пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25e72-138">Lock or unlock a user PIN in Lync Server 2013</span></span>](lync-server-2013-lock-or-unlock-a-user-pin.md)  
  

<span data-ttu-id="25e72-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25e72-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

