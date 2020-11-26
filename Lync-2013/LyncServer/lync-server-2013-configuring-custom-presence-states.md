---
title: 'Lync Server 2013: Настройка настраиваемых состояний присутствия'
description: 'Lync Server 2013: Настройка настраиваемых состояний присутствия.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring custom presence states
ms:assetid: e17364a8-8b93-45fc-a614-c80e45435d42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398997(v=OCS.15)
ms:contentKeyID: 48185534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28b277f096ff17ffa63615468ac9b4f21dead68e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433222"
---
# <a name="configuring-custom-presence-states-in-lync-server-2013"></a><span data-ttu-id="b27b1-103">Настройка настраиваемых состояний присутствия в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b27b1-103">Configuring custom presence states in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b27b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b27b1-104">

<span> </span></span></span>

<span data-ttu-id="b27b1-105">_**Тема последнего изменения:** 2013-01-10_</span><span class="sxs-lookup"><span data-stu-id="b27b1-105">_**Topic Last Modified:** 2013-01-10_</span></span>

<span data-ttu-id="b27b1-106">Для определения настраиваемых состояний присутствия в Lync 2013 создайте настраиваемый XML-файл конфигурации присутствия и укажите его расположение с помощью командлетов командной консоли Lync Server **New-CSClientPolicy** или **Set-CSClientPolicy** с параметром CustomStateURL.</span><span class="sxs-lookup"><span data-stu-id="b27b1-106">To define custom presence states in Lync 2013, create an XML custom presence configuration file, and then specify its location by using the Lync Server Management Shell cmdlets **New-CSClientPolicy** or **Set-CSClientPolicy** with the parameter CustomStateURL.</span></span>

<span data-ttu-id="b27b1-107">Файлы конфигурации обладают следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="b27b1-107">Configuration files have the following properties:</span></span>

  - <span data-ttu-id="b27b1-108">Настраиваемые состояния присутствия можно настроить с индикаторами присутствия "доступно", "занят" и "не беспокоить".</span><span class="sxs-lookup"><span data-stu-id="b27b1-108">Custom presence states can be configured with the Available, Busy, and Do Not Disturb presence indicators.</span></span>

  - <span data-ttu-id="b27b1-109">Атрибут доступности определяет, какой индикатор присутствия связан с текстом состояния для настраиваемого состояния.</span><span class="sxs-lookup"><span data-stu-id="b27b1-109">The availability attribute determines which presence indicator is associated with the status text of the custom state.</span></span> <span data-ttu-id="b27b1-110">В примере ниже в этом разделе текст состояния, работающий из дома, отображается справа от зеленого (доступного) индикатора присутствия.</span><span class="sxs-lookup"><span data-stu-id="b27b1-110">In the example later in this topic, the status text Working from Home is displayed to the right of the green (Available) presence indicator.</span></span>

  - <span data-ttu-id="b27b1-111">Максимальная длина текста состояния составляет 64 символов.</span><span class="sxs-lookup"><span data-stu-id="b27b1-111">The maximum length of the status text is 64 characters.</span></span>

  - <span data-ttu-id="b27b1-112">Можно добавить не более четырех настраиваемых состояний присутствия.</span><span class="sxs-lookup"><span data-stu-id="b27b1-112">A maximum of four custom presence states can be added.</span></span>

  - <span data-ttu-id="b27b1-113">Параметр CustomStateURL указывает расположение файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b27b1-113">The CustomStateURL parameter specifies the location of the configuration file.</span></span> <span data-ttu-id="b27b1-114">В Lync 2013 режим высокой безопасности SIP включен по умолчанию, поэтому необходимо сохранить настраиваемый файл конфигурации присутствия на веб-сервере с включенным HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b27b1-114">In Lync 2013, SIP high security mode is enabled by default, so you will need to store the custom presence configuration file on a web server that has HTTPS enabled.</span></span> <span data-ttu-id="b27b1-115">В противном случае пользователи Lync 2013 не смогут подключиться к нему.</span><span class="sxs-lookup"><span data-stu-id="b27b1-115">Otherwise, Lync 2013 clients will be unable to connect to it.</span></span> <span data-ttu-id="b27b1-116">Например, допустимый адрес `https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml` .</span><span class="sxs-lookup"><span data-stu-id="b27b1-116">For example, a valid address would be `https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml`.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b27b1-117">Несмотря на то, что его не рекомендуется использовать в производственной среде, вы можете протестировать файл конфигурации, расположенный на общем файловом адресе (не HTTPS), с помощью параметра реестра EnableSIPHighSecurityMode, чтобы отключить режим высокой безопасности SIP на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="b27b1-117">Although it is not recommended in a production environment, you can test a configuration file that is located on a non-HTTPS file share by using the EnableSIPHighSecurityMode registry setting to disable SIP high security mode on the client.</span></span> <span data-ttu-id="b27b1-118">Затем вы можете использовать параметр реестра CustomStateURL, чтобы указать расположение для файла конфигурации, отличное от HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b27b1-118">Then you can use the CustomStateURL registry setting to specify a non-HTTPS location for the configuration file.</span></span> <span data-ttu-id="b27b1-119">Обратите внимание, что в Lync 2013 учитываются параметры реестра Lync 2010, но куст реестра обновлен.</span><span class="sxs-lookup"><span data-stu-id="b27b1-119">Note that Lync 2013 honors Lync 2010 registry settings, but the registry hive has been updated.</span></span> <span data-ttu-id="b27b1-120">Вы можете создать параметры реестра следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b27b1-120">You would create the registry settings as follows:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="b27b1-121">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\EnableSIPHighSecurityMode</span><span class="sxs-lookup"><span data-stu-id="b27b1-121">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\EnableSIPHighSecurityMode</span></span></P>
> <P><span data-ttu-id="b27b1-122">Type (тип): DWORD</span><span class="sxs-lookup"><span data-stu-id="b27b1-122">Type: DWORD</span></span></P>
> <P><span data-ttu-id="b27b1-123">Данные значения: 0</span><span class="sxs-lookup"><span data-stu-id="b27b1-123">Value data: 0</span></span></P>
> <LI>
> <P><span data-ttu-id="b27b1-124">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\CustomStateURL</span><span class="sxs-lookup"><span data-stu-id="b27b1-124">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\CustomStateURL</span></span></P>
> <P><span data-ttu-id="b27b1-125">Тип: строка (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="b27b1-125">Type: String (REG_SZ)</span></span></P>
> <P><span data-ttu-id="b27b1-126">Данные значения (примеры): file:// \\lspool.corp.contoso.com\LSFileShare\ClientConfigFolder\Presence.xml или file:///c:/LSFileShare/ClientConfigFolder/Group_1_Pres.xml</span><span class="sxs-lookup"><span data-stu-id="b27b1-126">Value data (examples): file://\\lspool.corp.contoso.com\LSFileShare\ClientConfigFolder\Presence.xml or file:///c:/LSFileShare/ClientConfigFolder/Group_1_Pres.xml</span></span></P></LI></UL>



</div>

<span data-ttu-id="b27b1-127">Локализовать свое собственное состояние присутствия, указав одну или несколько схем ИДЕНТИФИКАТОРов языков (LCID) в XML-файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b27b1-127">Localize your custom presence state by specifying one or more locale ID (LCID) schema in the XML configuration file.</span></span> <span data-ttu-id="b27b1-128">В примере ниже показана локализация на английский (США) (1033), Норвежский (букмол, 1044), французский (Франция) (1036) и на турецком (1055).</span><span class="sxs-lookup"><span data-stu-id="b27b1-128">The example later in this topic shows localization into English - United States (1033), Norwegian - Bokmål (1044), French - France (1036), and Turkish (1055).</span></span> <span data-ttu-id="b27b1-129">Список LCID можно найти в разделе Коды языков, назначенные корпорацией Майкрософт <https://go.microsoft.com/fwlink/p/?linkid=157331> .</span><span class="sxs-lookup"><span data-stu-id="b27b1-129">For a list of LCIDs, see Locale IDs Assigned by Microsoft at <https://go.microsoft.com/fwlink/p/?linkid=157331>.</span></span>

<div>

## <a name="to-add-custom-presence-states-to-lync-2013"></a><span data-ttu-id="b27b1-130">Добавление настраиваемых состояний присутствия в Lync 2013</span><span class="sxs-lookup"><span data-stu-id="b27b1-130">To add custom presence states to Lync 2013</span></span>

1.  <span data-ttu-id="b27b1-131">Создайте XML-файл конфигурации, в котором используется формат следующего примера:</span><span class="sxs-lookup"><span data-stu-id="b27b1-131">Create an XML configuration file that uses the format of the following example:</span></span>
    
        <?xml version="1.0"?>
        <customStates xmlns="http://schemas.microsoft.com/09/2009/communicator/customStates">
          <customState ID="1" availability="online">
            <activity LCID="1033">Working from Home</activity>
            <activity LCID="1044">activity 2 for 1044</activity>
            <activity LCID="1055">activity 3 for 1055</activity>
          </customState>
          <customState ID="2" availability="busy">
            <activity LCID="1033">In a Live Meeting</activity>
            <activity LCID="1036">Equivalent French String for - In a Live Meeting </activity>
          </customState>
          <customState ID="3" availability="busy">
            <activity LCID="1033">Meeting with Customer</activity>
            <activity LCID="1055">meeting with client</activity>
            <activity LCID="1036">Equivalent French String for - Meeting with Customer</activity>
          </customState>
          <customState ID="4" availability="do-not-disturb">
            <activity LCID="1033">Interviewing</activity>
          </customState>
        </customStates>

2.  <span data-ttu-id="b27b1-132">Сохраните файл конфигурации XML на веб-сервере с включенным HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b27b1-132">Save the XML configuration file to a web server with HTTPS enabled.</span></span> <span data-ttu-id="b27b1-133">В этом примере файл называется Presence.xml и сохраняется в указанном месте https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml .</span><span class="sxs-lookup"><span data-stu-id="b27b1-133">In this example, the file is named Presence.xml and saved to the location https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml.</span></span>

3.  <span data-ttu-id="b27b1-134">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="b27b1-134">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="b27b1-135">В командной консоли Lync Server укажите расположение XML-файла конфигурации, выполнив команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="b27b1-135">In the Lync Server Management Shell, define the location of your XML configuration file by using a command similar to the following:</span></span>
    
        New-CsClientPolicy -Identity ContosoCustomStates 
        -CustomStateURL "https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml"

5.  <span data-ttu-id="b27b1-136">С помощью командлета **Grant-CSClientPolicy** можно назначить пользователям новую политику.</span><span class="sxs-lookup"><span data-stu-id="b27b1-136">Use the **Grant-CSClientPolicy** cmdlet to assign this new policy to users.</span></span>

<span data-ttu-id="b27b1-137">Подробные сведения можно найти в разделе [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) и [Grant-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsClientPolicy) в документации по среде управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b27b1-137">For details, see [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) and [Grant-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsClientPolicy) in the Lync Server Management Shell documentation.</span></span>

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="b27b1-138">По умолчанию Lync Server 2013 &nbsp; обновляет политики клиентов и параметры каждые три часа.</span><span class="sxs-lookup"><span data-stu-id="b27b1-138">By default, Lync Server 2013&nbsp;updates client policies and settings every three hours.</span></span></P>
> <LI>
> <P><span data-ttu-id="b27b1-139">Если вы хотите продолжить использовать параметры групповой политики из предыдущих выпусков, например CustomStateURL, Lync 2013 будет распознавать параметры, если они находятся в новом кусте реестра (HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync).</span><span class="sxs-lookup"><span data-stu-id="b27b1-139">If you want to continue using Group Policy settings from previous releases, such as CustomStateURL, Lync 2013 will recognize the settings if they are located in the new policy registry hive (HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync).</span></span> <span data-ttu-id="b27b1-140">Тем не менее, приоритетом обладают серверные политики на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b27b1-140">However, server-based client policies take precedence.</span></span></P></LI></UL><span data-ttu-id="b27b1-141">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b27b1-141">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

