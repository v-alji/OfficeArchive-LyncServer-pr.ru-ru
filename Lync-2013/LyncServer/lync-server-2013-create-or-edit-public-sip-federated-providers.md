---
title: 'Lync Server 2013: создание или изменение общедоступных федеративных поставщиков SIP'
description: 'Lync Server 2013: создание и изменение общедоступных федеративных служб SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit public SIP federated providers
ms:assetid: 5321598c-1ab1-40e3-b739-4b2e6d0a3a3b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398349(v=OCS.15)
ms:contentKeyID: 48184167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0ef5850b5e8016e0bd90512db45c2917c16a104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431878"
---
# <a name="create-or-edit-public-sip-federated-providers-in-lync-server-2013"></a><span data-ttu-id="f0632-103">Создание или изменение общедоступных федеративных поставщиков SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0632-103">Create or edit public SIP federated providers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0632-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0632-104">

<span> </span></span></span>

<span data-ttu-id="f0632-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="f0632-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="f0632-106">Общедоступная служба обмена мгновенными сообщениями позволяет пользователям в вашей организации общаться с пользователями служб обмена мгновенными сообщениями, предоставляемыми поставщиками Интернет-сообщений, в том числе с помощью Windows Live Messenger, Yahoo \! и AOL.</span><span class="sxs-lookup"><span data-stu-id="f0632-106">Public instant messaging (IM) connectivity enables users in your organization to use IM to communicate with users of IM services provided by public IM service providers, including the Windows Live Messenger, Yahoo\!, and AOL.</span></span>

<span data-ttu-id="f0632-107">Lync Server 2013 имеет настройки общедоступного поставщика для America Online, Windows Live и Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="f0632-107">Lync Server 2013 has public provider configurations for America Online, Windows Live and Yahoo\!</span></span> <span data-ttu-id="f0632-108">Обмен мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f0632-108">instant messaging.</span></span> <span data-ttu-id="f0632-109">У каждого общедоступного поставщика задано полное доменное имя поставщика, а уровень проверки по умолчанию **позволяет пользователям общаться только с людьми из списка контактов, который использует этот поставщик**.</span><span class="sxs-lookup"><span data-stu-id="f0632-109">Each public provider is configured with the provider’s Edge server fully qualified domain name, and the default verification level **Allow users to communicate only with people on their Contacts list who use this provider**.</span></span>

<span data-ttu-id="f0632-110">Как параметр по умолчанию, ни один из открытых поставщиков не включен.</span><span class="sxs-lookup"><span data-stu-id="f0632-110">As a default setting, none of the public providers are enabled.</span></span> <span data-ttu-id="f0632-111">Прежде чем включать общедоступные поставщики, необходимо завершить лицензионное соглашение и подготовиться к работе.</span><span class="sxs-lookup"><span data-stu-id="f0632-111">You should complete license agreement and provisioning work before enabling the public providers.</span></span> <span data-ttu-id="f0632-112">Вы можете включить поставщик, прежде чем приступить к работе с лицензией и обеспечением подготовки.</span><span class="sxs-lookup"><span data-stu-id="f0632-112">You can enable the provider before completing the licensing and provisioning work.</span></span> <span data-ttu-id="f0632-113">Пользователи не смогут общаться с контактами этих поставщиков, пока не завершится работа, необходимая предварительно.</span><span class="sxs-lookup"><span data-stu-id="f0632-113">Users will not be able to communicate with contacts on those providers until the pre-requisite work is completed.</span></span> <span data-ttu-id="f0632-114">Сведения о лицензировании и подготовке общедоступных поставщиков можно найти [в разделе Настройка политик для управления доступом пользователей в Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="f0632-114">For details on licensing and provisioning of public providers, see [Configure policies to control public user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md).</span></span>

<span data-ttu-id="f0632-115">Для создания и изменения общедоступных поставщиков выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f0632-115">Use the following procedure to create or edit Public providers:</span></span>

<div>

## <a name="to-create-or-edit-public-providers"></a><span data-ttu-id="f0632-116">Создание и изменение общедоступных поставщиков</span><span class="sxs-lookup"><span data-stu-id="f0632-116">To create or edit public providers</span></span>

1.  <span data-ttu-id="f0632-117">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="f0632-117">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f0632-118">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f0632-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f0632-119">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f0632-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f0632-120">На панели навигации слева выберите пункт **интеграция и внешний доступ**, а затем — **Федеративные поставщики SIP**.</span><span class="sxs-lookup"><span data-stu-id="f0632-120">In the left navigation bar, click **Federation and External Access**, and then click **SIP Federated Providers**.</span></span>

4.  <span data-ttu-id="f0632-121">Если вам нужно создать нового общедоступного поставщика, нажмите кнопку **создать** , а затем выберите пункт **общедоступный поставщик**.</span><span class="sxs-lookup"><span data-stu-id="f0632-121">If you need to create a new Public provider, click **New** and then click **Public provider**.</span></span>

5.  <span data-ttu-id="f0632-122">Если вам нужно изменить запись из списка общедоступных поставщиков, выберите общедоступного поставщика, нажмите кнопку **изменить**, а затем выберите команду **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="f0632-122">If you need to edit an entry from the list of Public providers, select a public provider, click **Edit**, then click **Show details**.</span></span>

6.  <span data-ttu-id="f0632-123">На странице " **Изменение поставщика SIP-Федерации** " можно ввести или изменить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f0632-123">On the **Edit SIP Federated Provider** page, you can type or edit the following settings:</span></span>
    
      - <span data-ttu-id="f0632-124">**Включение связи с этим поставщиком**   Выберите этот параметр, чтобы включить обмен мгновенными сообщениями с пользователями этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="f0632-124">**Enable communications with this provider**   Selecting this setting enables IM with this provider’s users.</span></span>
    
      - <span data-ttu-id="f0632-125">**Имя поставщика:**   Обязательное свойство введите имя поставщика, так как оно будет отображаться в списке поставщиков услуг-Федерации SIP.</span><span class="sxs-lookup"><span data-stu-id="f0632-125">**Provider name:**   A required property, type the name of the provider as it will be reflected in the listing of SIP Federated Providers.</span></span>
    
      - <span data-ttu-id="f0632-126">**Служба пограничного доступа (FQDN):**   Обязательное свойство введите полное доменное имя службы пограничного доступа для поставщика, который вы настраиваете.</span><span class="sxs-lookup"><span data-stu-id="f0632-126">**Access Edge service (FQDN):**   A required property, type the fully qualified domain name of the Access Edge service of the provider that you are configuring.</span></span> <span data-ttu-id="f0632-127">Эти сведения предоставлены как элемент по умолчанию и должны изменяться только в том случае, если общедоступный поставщик вносит изменения в полное доменное имя службы Edge Access на общедоступном поставщике.</span><span class="sxs-lookup"><span data-stu-id="f0632-127">This information is provided as a default item, and should only be changed if the public provider makes a change to the FQDN of the Access Edge service at the public provider.</span></span>
    
      - <span data-ttu-id="f0632-128">**Уровень проверки по умолчанию:**   Параметр по умолчанию, **разрешающий пользователям общаться с людьми из списка контактов, который использует этот поставщик** , будет ограничивать общение с контактами, которые вы приняли, и которые находятся в списке контактов.</span><span class="sxs-lookup"><span data-stu-id="f0632-128">**Default verification level:**   The default setting, **Allow users to communicate with people on their Contacts list who use this provider** will limit communication to contacts that you have accepted and are in your contact list.</span></span>
        
        <span data-ttu-id="f0632-129">Выбрав **параметр Разрешить пользователям общаться с кем угодно с помощью этого поставщика** , вы удаляете ограничение, которое вы должны получить и принять приглашение на контакт.</span><span class="sxs-lookup"><span data-stu-id="f0632-129">Selecting **Allow users to communicate with everyone using this provider** removes the restriction that you must have received and accepted a contact invite.</span></span> <span data-ttu-id="f0632-130">Этот параметр не ограничивает круг пользователей, которые могут общаться с вами в сети общедоступного поставщика.</span><span class="sxs-lookup"><span data-stu-id="f0632-130">This setting does not limit who can contact you from the public provider’s network.</span></span>

7.  <span data-ttu-id="f0632-131">Завершив настройку параметров **, нажмите кнопку Сохранить для** сохранения или кнопку **Отмена** , чтобы отменить изменения.</span><span class="sxs-lookup"><span data-stu-id="f0632-131">When you are done configuring the settings, click **Commit** to save, or click **Cancel** to discard your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f0632-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f0632-132">See Also</span></span>


[<span data-ttu-id="f0632-133">Конфигурация политик для управления общим доступом пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0632-133">Configure policies to control public user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-public-user-access.md)  
[<span data-ttu-id="f0632-134">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0632-134">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
  

<span data-ttu-id="f0632-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0632-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

