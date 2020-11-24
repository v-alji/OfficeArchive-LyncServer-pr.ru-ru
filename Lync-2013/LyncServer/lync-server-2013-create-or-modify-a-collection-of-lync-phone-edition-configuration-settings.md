---
title: Создание и изменение коллекции параметров конфигурации Lync Phone Edition
description: Создание или изменение коллекции параметров конфигурации Lync Phone Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of Lync Phone Edition configuration settings
ms:assetid: 6cf714af-8f57-4a71-89ad-0a776302b2ba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688086(v=OCS.15)
ms:contentKeyID: 49733683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82a4becadf581ec965952e507c3eb2839b622d9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399340"
---
# <a name="create-or-modify-a-collection-of-lync-phone-edition-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="8e3bc-103">Создание и изменение коллекции параметров конфигурации Lync Phone Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3bc-103">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e3bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e3bc-104">

<span> </span></span></span>

<span data-ttu-id="8e3bc-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="8e3bc-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="8e3bc-106">При установке сервера Lync Server вы получаете глобальную коллекцию параметров Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-106">When you install Lync Server, you get a global collection of Lync Phone Edition settings.</span></span> <span data-ttu-id="8e3bc-107">Эти параметры применяются ко всем устройствам, на которых работает Lync Phone Edition в развертывании.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-107">These settings apply to all devices running Lync Phone Edition in your deployment.</span></span> <span data-ttu-id="8e3bc-108">Вы можете в любое время изменить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-108">You can change these settings at any time.</span></span> <span data-ttu-id="8e3bc-109">Вы также можете настроить новый набор параметров, которые применяются к устройствам на определенном сайте.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-109">You can also set up a new collection of settings that apply to the devices in a specific site.</span></span> <span data-ttu-id="8e3bc-110">Параметры сайта имеют приоритет над глобальными параметрами.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-110">Site settings take precedence over global settings.</span></span>

<span data-ttu-id="8e3bc-111">Параметры конфигурации включают имя коллекции, область (Global или site), параметр безопасности SIP, уровень ведения журнала, уровень обслуживания голосовой связи (QoS), параметр блокировки телефона и сведения о блокировке телефона, то есть как долго a) разблокировать персональный идентификационный номер (ПИН-код) и b) телефон будет бездействует до тех пор, пока не будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-111">Configuration settings consist of the collection name, scope (global or site), SIP security setting, logging level, voice quality of service (QoS) level, phone-lock setting, and phone-lock details, that is, how long the a) unlock personal identification number (PIN) must be and b) phone stays idle before locking itself.</span></span>

<div>

## <a name="to-create-a-collection-of-lync-phone-edition-configuration-settings-or-edit-settings-for-an-existing-collection"></a><span data-ttu-id="8e3bc-112">Создание коллекции параметров конфигурации Lync Phone Edition или изменение параметров для существующей коллекции</span><span class="sxs-lookup"><span data-stu-id="8e3bc-112">To create a collection of Lync Phone Edition configuration settings or edit settings for an existing collection</span></span>

1.  <span data-ttu-id="8e3bc-113">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8e3bc-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8e3bc-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8e3bc-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8e3bc-116">На панели навигации слева выберите пункт **Клиенты**, а затем нажмите кнопку Навигация по **конфигурации устройства** .</span><span class="sxs-lookup"><span data-stu-id="8e3bc-116">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="8e3bc-117">На странице **Конфигурация устройства** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-117">On the **Device Configuration** page, do one of the following:</span></span>
    
      - <span data-ttu-id="8e3bc-118">Чтобы создать коллекцию параметров конфигурации Lync Phone Edition, нажмите кнопку **создать**, выберите сайт, нажмите кнопку **ОК**, проверьте параметры по умолчанию и, если нужно, внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-118">To create a new collection of Lync Phone Edition configuration settings, click **New**, select a site, click **OK**, review the default settings, and, if you want to, make any changes.</span></span>
    
      - <span data-ttu-id="8e3bc-119">Чтобы изменить параметры в существующей коллекции, щелкните ее, выберите в меню **Правка** команду **Показать подробности** и внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-119">To edit any of the settings in an existing collection, click the collection, click the **Edit** menu, click **Show details**, and then make your changes.</span></span>
        
        <div>
        

        > [!TIP]
        > <span data-ttu-id="8e3bc-120">Чтобы вернуться к использованию параметров по умолчанию для глобальной коллекции, щелкните глобальную коллекцию, выберите в меню <STRONG>Правка</STRONG> команду <STRONG>Удалить</STRONG>, а затем нажмите кнопку <STRONG>ОК</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-120">To go back to using the default settings for the global collection, click the global collection, click the <STRONG>Edit</STRONG> menu, click <STRONG>Delete</STRONG>, and then click <STRONG>OK</STRONG>.</span></span> <span data-ttu-id="8e3bc-121">Это не приведет к удалению глобальной коллекции; оно просто восстанавливает значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-121">This will not delete the global collection; it just resets the settings to the defaults.</span></span>

        
        </div>

5.  <span data-ttu-id="8e3bc-122">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-new-lync-phone-edition-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="8e3bc-123">Создание новых параметров конфигурации Lync Phone Edition с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8e3bc-123">Creating New Lync Phone Edition Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="8e3bc-124">Вы можете создавать параметры конфигурации Lync Phone Edition (только на уровне сайта) с помощью Windows PowerShell и командлета **New-CsUCPhoneConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="8e3bc-124">You can create Lync Phone Edition configuration settings can (at the site scope only) by using Windows PowerShell and the **New-CsUCPhoneConfiguration** cmdlet.</span></span> <span data-ttu-id="8e3bc-125">Этот командлет можно выполнить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-125">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="8e3bc-126">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="8e3bc-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-new-lync-phone-edition-configuration-settings-that-use-the-default-values"></a><span data-ttu-id="8e3bc-127">Создание новых параметров конфигурации Lync Phone Edition, использующих значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8e3bc-127">To create new Lync Phone Edition configuration settings that use the default values</span></span>

  - <span data-ttu-id="8e3bc-128">Эта команда создает новый набор параметров конфигурации телефона в UC для сайта Redmond.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-128">This command creates a new set of UC phone configuration settings for the Redmond site:</span></span>
    
        New-CsUCPhoneConfiguration -Identity "site:Redmond"
    
    <span data-ttu-id="8e3bc-129">Поскольку в предыдущей команде не было указано никаких параметров, кроме обязательного параметра Identity, новая коллекция параметров конфигурации будет использовать значения по умолчанию для всех своих свойств.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-129">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span>

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-new-lync-phone-edition-configuration-settings"></a><span data-ttu-id="8e3bc-130">Изменение одного значения свойства при создании новых параметров конфигурации Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="8e3bc-130">To change a single property value when creating new Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="8e3bc-131">Чтобы создать параметры, использующие другие значения свойств, просто включите соответствующий параметр и его значение.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-131">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="8e3bc-132">Например, чтобы создать коллекцию параметров настройки телефонной связи UC, которая по умолчанию требует блокировки на телефоне, используйте такую команду:</span><span class="sxs-lookup"><span data-stu-id="8e3bc-132">For example, to create a collection of UC phone configuration settings that, by default, require phone locking, use a command like this:</span></span>
    
        New-CsUCPhoneConfiguration -Identity "site:Redmond" -EnforcePhoneLock $True

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-new-lync-phone-edition-configuration-settings"></a><span data-ttu-id="8e3bc-133">Изменение нескольких значений свойства при создании новых параметров конфигурации Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="8e3bc-133">To change multiple property values when creating new Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="8e3bc-134">Чтобы изменить несколько значений свойств, можно включить несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-134">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="8e3bc-135">Например, эта команда обеспечивает принудительную блокировку телефона, а также задает минимальную длину ПИН-кода в 8 цифр.</span><span class="sxs-lookup"><span data-stu-id="8e3bc-135">For example, this command enforces phone locking and also sets the minimum PIN length to 8 digits:</span></span>
    
        New-CsUCPhoneConfiguration -Identity "site:Redmond" -EnforcePhoneLock $True -MinPhonePinLength 8

</div>

<span data-ttu-id="8e3bc-136">Подробности можно найти в разделе [New-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398445(v=OCS.15)).</span><span class="sxs-lookup"><span data-stu-id="8e3bc-136">For details, see [New-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398445(v=OCS.15)).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8e3bc-137">См. также</span><span class="sxs-lookup"><span data-stu-id="8e3bc-137">See Also</span></span>


[<span data-ttu-id="8e3bc-138">Удаление существующей коллекции параметров конфигурации Lync Phone Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3bc-138">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-lync-phone-edition-configuration-settings.md)  
[<span data-ttu-id="8e3bc-139">Настройка параметров безопасности для Lync Phone Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3bc-139">Configure security settings for Lync Phone Edition in Lync Server 2013</span></span>](lync-server-2013-configure-security-settings-for-lync-phone-edition.md)  
[<span data-ttu-id="8e3bc-140">Принудительная Блокировка телефона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3bc-140">Enforce phone locking in Lync Server 2013</span></span>](lync-server-2013-enforce-phone-locking.md)  
  

<span data-ttu-id="8e3bc-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e3bc-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

