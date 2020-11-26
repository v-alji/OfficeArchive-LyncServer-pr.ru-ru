---
title: 'Lync Server 2013: Настройка телефонии для пользователя'
description: 'Lync Server 2013: Настройка телефонии для пользователя.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure telephony for a user
ms:assetid: 4546432e-c839-4517-a2c5-bc0d4d8c6a03
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520988(v=OCS.15)
ms:contentKeyID: 48183987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b82cecb67ea11928d187bd2a4a00625fbca7b23e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433656"
---
# <a name="configure-telephony-for-a-user-in-lync-server-2013"></a><span data-ttu-id="1cb17-103">Настройка телефонии для пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cb17-103">Configure telephony for a user in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1cb17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1cb17-104">

<span> </span></span></span>

<span data-ttu-id="1cb17-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1cb17-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1cb17-106">Параметры телефонии — это некоторые параметры учетной записи пользователя, которую можно настроить на панели управления Lync Server для пользователя (то есть если для этого пользователя разрешено использовать сервер Lync Server 2013 и организация поддерживает телефонную связь).</span><span class="sxs-lookup"><span data-stu-id="1cb17-106">Telephony settings are some of the individual settings of a user account that can be configured in Lync Server Control Panel for the user (that is, if the individual user has been enabled for Lync Server 2013 and the organization supports telephony).</span></span>

<span data-ttu-id="1cb17-107">Параметры телефонной связи пользователей Lync Server включают в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="1cb17-107">Lync Server user telephony options include the following:</span></span>

  - <span data-ttu-id="1cb17-108">**Звук и видео отключены**   Пользователь не может звонить с помощью звукового и видеосигнала.</span><span class="sxs-lookup"><span data-stu-id="1cb17-108">**Audio/video disabled**   The user cannot make calls with audio and video.</span></span>

  - <span data-ttu-id="1cb17-109">**Только для**   ПК   Пользователь может выполнять только голосовые и видеозвонки между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="1cb17-109">**PC-to-PC only**   The user can make only PC-to-PC audio or video calls.</span></span>

  - <span data-ttu-id="1cb17-110">**Корпоративная голосовая связь**   Пользователь может использовать инфраструктуру Lync Server 2013 для маршрутизации всех входящих и исходящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="1cb17-110">**Enterprise Voice**   The user can use the Lync Server 2013 infrastructure to route all incoming and outgoing calls.</span></span> <span data-ttu-id="1cb17-111">Пользователь также может звонить между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="1cb17-111">The user can also make PC-to-PC calls.</span></span>

  - <span data-ttu-id="1cb17-112">**Удаленное управление звонками**   Пользователь может использовать Lync Server 2013 для управления настольным телефоном, а также совершать звонки с компьютера на компьютер.</span><span class="sxs-lookup"><span data-stu-id="1cb17-112">**Remote call control**   The user can use Lync Server 2013 to control the desktop phone, and can also make PC-to-PC calls.</span></span>

<span data-ttu-id="1cb17-113">Сведения о настройке телефонии для организации можно найти в разделе [Настройка телефонии для пользователя в Lync server 2013](lync-server-2013-configure-telephony-for-a-user.md) и [Развертывание корпоративной голосовой связи в Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="1cb17-113">For details about configuring telephony for an organization, see [Configure telephony for a user in Lync Server 2013](lync-server-2013-configure-telephony-for-a-user.md) and [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span>

<div>

## <a name="to-configure-telephony-for-a-specific-user-account"></a><span data-ttu-id="1cb17-114">Настройка телефонной связи для определенной учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="1cb17-114">To configure telephony for a specific user account</span></span>

1.  <span data-ttu-id="1cb17-115">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="1cb17-115">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="1cb17-116">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1cb17-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1cb17-117">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1cb17-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1cb17-118">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="1cb17-118">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="1cb17-119">В поле **Поиск пользователей** введите все или первую часть отображаемого имени, имя, фамилию, диспетчер учетных записей безопасности (SAM), имя учетной записи, адрес SIP или универсальный код ресурса (URI) нужной учетной записи пользователя, а затем нажмите кнопку **найти**.</span><span class="sxs-lookup"><span data-stu-id="1cb17-119">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want, and then click **Find**.</span></span>

5.  <span data-ttu-id="1cb17-120">В таблице выберите учетную запись пользователя, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="1cb17-120">In the table, click the user account that you want to modify.</span></span>

6.  <span data-ttu-id="1cb17-121">В меню **Правка** выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="1cb17-121">On the **Edit** menu, click **Modify**.</span></span>

7.  <span data-ttu-id="1cb17-122">В разделе **телефония** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1cb17-122">In **Telephony**, do the following:</span></span>
    
      - <span data-ttu-id="1cb17-123">Чтобы отключить голосовые и видеозвонки для пользователя, нажмите кнопку **звук и видео отключено**.</span><span class="sxs-lookup"><span data-stu-id="1cb17-123">To disable audio and video calls for the user, click **Audio/video disabled**.</span></span>
    
      - <span data-ttu-id="1cb17-124">Чтобы включить голосовую связь между компьютерами для пользователя, но не удаленное управление звонками или голосовой телефон, выберите вариант **только для** ПК.</span><span class="sxs-lookup"><span data-stu-id="1cb17-124">To enable PC-to-PC audio communications for the user, but not remote call control or Enterprise Voice, click **PC-to-PC only**.</span></span> <span data-ttu-id="1cb17-125">Укажите значение **универсального кода ресурса (URI)** для телефона, который пользователь использует для голосовой связи между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="1cb17-125">Specify a value for **Line URI** for the telephone that the user uses for PC-to-PC audio communications.</span></span>
    
      - <span data-ttu-id="1cb17-126">Чтобы перенаправить телефонные звонки пользователя с помощью инфраструктуры Lync Server 2010 в соответствии с классом политики обслуживания, включая голосовую связь между ПК и компьютером, выберите **Корпоративный голосовой** стандарт.</span><span class="sxs-lookup"><span data-stu-id="1cb17-126">To route the user's phone calls by using the Lync Server 2010 infrastructure in accordance with the class of service policy, including PC-to-PC audio communication, click **Enterprise Voice**.</span></span> <span data-ttu-id="1cb17-127">В **URI строки** укажите номер телефона для корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="1cb17-127">In **Line URI**, specify the telephone number for Enterprise Voice.</span></span> <span data-ttu-id="1cb17-128">В **политике** и стратегии **голосовой** связи укажите соответствующие политики для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1cb17-128">In **Dial plan policy** and **Voice policy**, specify the appropriate policies for the user.</span></span> <span data-ttu-id="1cb17-129">Чтобы задать правила нормализации для перевода телефонных номеров, набранных пользователем, в формат E. 164, выберите соответствующий профиль местоположения в разделе **Политика местоположений**.</span><span class="sxs-lookup"><span data-stu-id="1cb17-129">To specify the normalization rules for translating phone numbers dialed by the user to the E.164 format, select the appropriate location profile in **Location policy**.</span></span>
    
      - <span data-ttu-id="1cb17-130">Чтобы включить удаленное управление звонками, благодаря которому пользователи смогут управлять настольными телефонными линиями из Lync Server 2013, чтобы звонить между компьютерами и телефонными звонками с компьютера на компьютер и звонить по телефону, нажмите кнопку **Удаленное управление звонками**.</span><span class="sxs-lookup"><span data-stu-id="1cb17-130">To enable remote call control, which enables users to control their desktop phone line from Lync Server 2013 to make PC-to-PC calls and PC-to-phone calls, click **Remote call control**.</span></span> <span data-ttu-id="1cb17-131">В **URI строки** укажите номер телефона для удаленного управления звонками.</span><span class="sxs-lookup"><span data-stu-id="1cb17-131">In **Line URI**, specify the telephone number for remote call control.</span></span> <span data-ttu-id="1cb17-132">Для маршрутизации звонков пользователь должен иметь подключение к рабочему столу и телефонной линии обмена филиалами.</span><span class="sxs-lookup"><span data-stu-id="1cb17-132">The user must have a desktop phone and private branch exchange (PBX) connection for call routing.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1cb17-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1cb17-133">See Also</span></span>


[<span data-ttu-id="1cb17-134">Изменение свойств учетной записи пользователя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cb17-134">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)  
  

<span data-ttu-id="1cb17-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1cb17-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

