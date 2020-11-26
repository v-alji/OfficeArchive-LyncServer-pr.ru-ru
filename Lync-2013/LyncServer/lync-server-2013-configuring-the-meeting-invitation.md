---
title: 'Lync Server 2013: Настройка приглашения на собрание'
description: 'Lync Server 2013: Настройка приглашения на собрание.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the meeting invitation
ms:assetid: 7faa4797-0344-418b-9fa3-59dfb9c2baf7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398638(v=OCS.15)
ms:contentKeyID: 48184641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 64438d7a451cb794c125207fa594e1c00b534c80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432550"
---
# <a name="configuring-the-meeting-invitation-in-lync-server-2013"></a><span data-ttu-id="20818-103">Настройка приглашения на собрание в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20818-103">Configuring the meeting invitation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20818-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20818-104">

<span> </span></span></span>

<span data-ttu-id="20818-105">_**Тема последнего изменения:** 2013-07-16_</span><span class="sxs-lookup"><span data-stu-id="20818-105">_**Topic Last Modified:** 2013-07-16_</span></span>

<span data-ttu-id="20818-106">Вы можете настроить приглашения на собрание, отправленные надстройкой "собрание по сети" для Lync 2013, добавив следующие необязательные элементы в тексте приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="20818-106">You can customize meeting invitations sent by the Online Meeting Add-in for Lync 2013 by including the following optional items in the body of the meeting invitation:</span></span>

  - <span data-ttu-id="20818-107">**Логотип вашей организации** Добавьте логотип своей организации в приглашения на собрание с помощью параметра URL-адрес эмблемы.</span><span class="sxs-lookup"><span data-stu-id="20818-107">**Your organization’s logo** Add your organization’s logo to meeting invitations by using the Logo URL option.</span></span> <span data-ttu-id="20818-108">Если приглашения на собрание будут отправляться людям, которые являются внешними по отношению к вашей организации, это изображение должно находиться по общедоступному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="20818-108">If meeting invitations will be sent to people external to your organization, the image should be located at a publicly available URL.</span></span> <span data-ttu-id="20818-109">Поддерживаются форматы изображений GIF и JPG.</span><span class="sxs-lookup"><span data-stu-id="20818-109">The supported image formats are GIF and JPG.</span></span> <span data-ttu-id="20818-110">Несмотря на то, что в Lync Server 2013 хранится URL-адрес без ограничений на размер изображения, для достижения наилучших результатов максимальный размер изображения должен составлять 30 пикселей в высоту на 188 пикселей по ширине.</span><span class="sxs-lookup"><span data-stu-id="20818-110">Although Lync Server 2013 stores the URL with no size restrictions on the image, for best results, the maximum size of the image should be 30 pixels high by 188 pixels wide.</span></span>

  - <span data-ttu-id="20818-111">**Ссылка на специальную справку или службу поддержки** Добавьте URL-адрес сайта группы справки или поддержки своей организации.</span><span class="sxs-lookup"><span data-stu-id="20818-111">**A Custom Help or Support Link** Add a URL for your organization’s help or support team website.</span></span> <span data-ttu-id="20818-112">Если приглашения на собрание будут отправляться людям, которые являются внешними по отношению к вашей организации, этот URL-адрес должен быть общедоступным.</span><span class="sxs-lookup"><span data-stu-id="20818-112">If meeting invitations will be sent to people external to your organization, the URL should be publicly available.</span></span> <span data-ttu-id="20818-113">Максимальная длина URL-адреса составляет 1 КБ.</span><span class="sxs-lookup"><span data-stu-id="20818-113">The maximum URL length is 1 KB.</span></span>

  - <span data-ttu-id="20818-114">**Текст заявления об отказе от ответственности** Добавьте URL-адрес для юридического текста или заявление об отказе, которое будет отображаться во всех приглашениях на собрания.</span><span class="sxs-lookup"><span data-stu-id="20818-114">**Legal disclaimer text** Add a URL for legal text or a disclaimer that will be displayed in all meeting invitations.</span></span> <span data-ttu-id="20818-115">Если приглашения на собрание будут отправляться людям, которые являются внешними по отношению к вашей организации, этот URL-адрес должен быть общедоступным.</span><span class="sxs-lookup"><span data-stu-id="20818-115">If meeting invitations will be sent to people external to your organization, the URL should be publicly available.</span></span> <span data-ttu-id="20818-116">Максимальная длина URL-адреса составляет 1 КБ.</span><span class="sxs-lookup"><span data-stu-id="20818-116">The maximum URL length is 1 KB.</span></span>

  - <span data-ttu-id="20818-117">**Настраиваемый текст нижнего колонтитула** Добавьте текст, который будет отображаться в приглашении в качестве настраиваемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="20818-117">**Custom footer text** Add text that will be rendered as a custom footer in the invitation.</span></span> <span data-ttu-id="20818-118">Максимальная длина текста, который может быть добавлен, составляет 2 КБ.</span><span class="sxs-lookup"><span data-stu-id="20818-118">The maximum length of text that can be added is 2 KB.</span></span>

<span data-ttu-id="20818-119">Эти параметры можно настроить с помощью панели управления Lync Server либо из командной консоли Lync Server Management.</span><span class="sxs-lookup"><span data-stu-id="20818-119">You can configure these options by using either Lync Server Control Panel or Lync Server Management Shell.</span></span>

<div>


<span data-ttu-id="20818-120">**Настройка приглашения на собрание с помощью панели управления Lync Server**</span><span class="sxs-lookup"><span data-stu-id="20818-120">**To Customize the Meeting Invitation by using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="20818-121">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20818-121">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="20818-122">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="20818-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="20818-123">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="20818-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="20818-124">На панели навигации слева выберите **Конференц** -связь, а затем — **Конфигурация собрания**.</span><span class="sxs-lookup"><span data-stu-id="20818-124">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="20818-125">На странице **Конфигурация собрания** нажмите кнопку **Создать**, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="20818-125">On the **Meeting Configuration** page, click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="20818-p106">Чтобы создать политику уровня сайта, выберите вариант **Настройка сайта**. В поле поиска **Выбор сайта** частично или полностью введите имя сайта, для которого требуется определить параметры присоединения к собранию. В полученном списке сайтов выберите нужный сайт и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="20818-p106">To create a site-level policy, click **Site configuration**. In the **Select a Site** search field, type all or part of the name of the site for which you want to define meeting join settings. In the resulting list of sites, click the site you want, and then click **OK**.</span></span>
    
      - <span data-ttu-id="20818-p107">Чтобы создать политику уровня пула, выберите вариант **Конфигурация пула**. В поле поиска **Выбор службы** частично или полностью введите имя службы пула, для которой требуется определить параметры присоединения к собранию. В полученном списке служб выберите нужную службу и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="20818-p107">To create a pool-level policy, click **Pool configuration**. In the **Select a Service** search field, type all or part of the name of the pool service for which you want to define meeting join settings. In the resulting list of services, click the pool you want, and then click **OK**.</span></span>

5.  <span data-ttu-id="20818-132">Выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="20818-132">Do any of the following:</span></span>
    
      - <span data-ttu-id="20818-133">В поле **URL-адрес логотипа** введите URL-адрес изображения логотипа Организации.</span><span class="sxs-lookup"><span data-stu-id="20818-133">In the **Logo URL** field, type the URL for your organization’s logo image.</span></span>
    
      - <span data-ttu-id="20818-134">В поле **URL-адрес справки** введите URL-адрес сайта справки или службы поддержки Организации.</span><span class="sxs-lookup"><span data-stu-id="20818-134">In the **Help URL** field, type the URL to your organization’s help or support site.</span></span>
    
      - <span data-ttu-id="20818-135">В поле **юридическое текстовое** введите URL-адрес юридического или отказа, который вы хотите включить в приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="20818-135">In the **Legal text** field, type the URL to the legal text or disclaimer that you want to include in meeting invitations.</span></span>
    
      - <span data-ttu-id="20818-136">В **текстовом поле настраиваемый нижний колонтитул** введите текст нижнего колонтитула длиной до 2 КБ.</span><span class="sxs-lookup"><span data-stu-id="20818-136">In the **Custom footer text** field, type footer text, up to 2 KB.</span></span>

<span data-ttu-id="20818-137">**Настройка приглашения на собрание с помощью командной консоли Lync Server Management Shell**</span><span class="sxs-lookup"><span data-stu-id="20818-137">**To Customize the Meeting Invitation by using Lync Server Management Shell**</span></span>

1.  <span data-ttu-id="20818-138">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="20818-138">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="20818-139">Запустите командлет **New-CsMeetingConfiguration** или **Set-CsMeetingConfiguration** , чтобы создать или настроить параметры приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="20818-139">Run the **New-CsMeetingConfiguration** or **Set-CsMeetingConfiguration** cmdlet to create or configure the meeting invitation options.</span></span> <span data-ttu-id="20818-140">Например, выполните командлет:</span><span class="sxs-lookup"><span data-stu-id="20818-140">For example, run:</span></span>
    
        New-CsMeetingConfiguration -Identity site:Redmond -LogoURL "http://www.contoso.com/logo/contosobanner.gif" -HelpURL "http://www.contoso.com/support" -LegalURL "http://www.contoso.com/disclaimer" -CustomFooterText "Communications may be monitored or recorded."

<span data-ttu-id="20818-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20818-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

