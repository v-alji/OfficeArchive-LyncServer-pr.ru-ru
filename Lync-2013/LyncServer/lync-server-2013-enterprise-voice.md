---
title: 'Lync Server 2013: корпоративная голосовая связь'
description: Lync Server 2013 Enterprise Voice.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enterprise Voice
ms:assetid: c9da8099-6f4f-4346-ac67-f041bb96072c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417163(v=OCS.15)
ms:contentKeyID: 48185404
ms.date: 04/08/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e11f2497cf99319317a75b81f02ed0d8ca797fbf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428575"
---
# <a name="enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="c9900-103">Корпоративная голосовая связь в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9900-103">Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9900-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9900-104">

<span> </span></span></span>

<span data-ttu-id="c9900-105">_**Тема последнего изменения:** 2015-04-08_</span><span class="sxs-lookup"><span data-stu-id="c9900-105">_**Topic Last Modified:** 2015-04-08_</span></span>

<span data-ttu-id="c9900-106">С помощью корпоративной голосовой связи Lync Server представляет собой отдельное предложение голосовой связи по Интернету (VoIP) для расширения или замены традиционных компьютеров с частным подключением (АТС).</span><span class="sxs-lookup"><span data-stu-id="c9900-106">With Enterprise Voice, Lync Server delivers a stand-alone Voice over Internet Protocol (VoIP) offering to enhance or replace traditional private branch exchange (PBX) systems.</span></span> <span data-ttu-id="c9900-107">Пользователи предприятий голосовой связи могут звонить коллегам в сети VoIP или УАТС организации и звонить на обычные телефонные номера за пределами вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c9900-107">Enterprise Voice users can call colleagues on your organization’s VoIP network or PBX, and they can call traditional phone numbers outside your organization.</span></span> <span data-ttu-id="c9900-108">Корпоративная голосовая связь включает в себя распространенные функции, такие как "ответить", "вперед", "передача", "удержание", "переадресация", "выпуск", "придерживаться" и Улучшенный 9-1-1 (E9-1-1) звонок в США (E9-1-1). Корпоративная голосовая связь также поддерживает широкий спектр текущих и устаревших IP-и USB-устройств.</span><span class="sxs-lookup"><span data-stu-id="c9900-108">The Enterprise Voice solution includes common calling features such as answer, forward, transfer, hold, divert, release and park, and Enhanced 9-1-1 (E9-1-1) calling (E9-1-1 is available only in the United States.) Enterprise Voice also supports a broad range of current and older IP and USB devices.</span></span>

<div>

## <a name="placing-and-receiving-calls"></a><span data-ttu-id="c9900-109">Размещение и прием звонков</span><span class="sxs-lookup"><span data-stu-id="c9900-109">Placing and Receiving Calls</span></span>

<span data-ttu-id="c9900-110">С помощью Lync пользователи могут звонить, вводя имя или номер телефона с клавиатуры, а также с помощью панели набора номера, показанной на экране.</span><span class="sxs-lookup"><span data-stu-id="c9900-110">Using Lync, users can place calls by typing a name or phone number on their keyboard, or using a dial pad displayed on their screen.</span></span> <span data-ttu-id="c9900-111">Пользователи также могут инициировать звонки прямо из своего списка контактов.</span><span class="sxs-lookup"><span data-stu-id="c9900-111">Users can also initiate calls directly from their Contacts list.</span></span> <span data-ttu-id="c9900-112">Вы также можете развернуть устройства Lync Phone Edition, которые являются автономными устройствами IP-телефонии, предоставляемыми партнерами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c9900-112">You can also deploy Lync Phone Edition devices, which are stand-alone IP phone devices provided by Microsoft partners.</span></span>

<span data-ttu-id="c9900-113">У пользователей может быть несколько телефонных устройств, зарегистрированных с помощью Lync Server, и они могут легко переключаться между ними.</span><span class="sxs-lookup"><span data-stu-id="c9900-113">Users can have multiple phone devices registered with Lync Server, and can switch between them easily.</span></span>

<span data-ttu-id="c9900-114">Пользователи будут получать уведомления о входящих звонках на всех устройствах, используя настраиваемые мелодии звонка на устройствах с IP-телефонами, а также уведомление о том, что на своем компьютере они похожи на голосовые сообщения.</span><span class="sxs-lookup"><span data-stu-id="c9900-114">Users are alerted to incoming calls on all their devices simultaneously, with customizable ringtones on IP phone devices and a notification similar to an instant message on their PC.</span></span>

<span data-ttu-id="c9900-115">Пользователи также могут задать один номер телефона, который подключается к стационарному телефону, компьютеру и мобильному телефону, поэтому они могут быть недоступными, где бы они ни находились.</span><span class="sxs-lookup"><span data-stu-id="c9900-115">Users can also set a single telephone number that connects to their desk phone, PC and mobile phone, so they can be reached no matter where they are.</span></span>

</div>

<div>

## <a name="basic-call-features"></a><span data-ttu-id="c9900-116">Основные функции звонка</span><span class="sxs-lookup"><span data-stu-id="c9900-116">Basic Call Features</span></span>

<span data-ttu-id="c9900-117">Во время звонка пользователь может ответить на дополнительные входящие звонки или инициировать исходящие вызовы, и существующий активный звонок будет автоматически помещен на удержание.</span><span class="sxs-lookup"><span data-stu-id="c9900-117">While on a call, a user can answer additional incoming calls or initiate outgoing calls, and the existing active call is automatically put on hold.</span></span> <span data-ttu-id="c9900-118">Звонки могут быть переданы от одного пользователя другому, непосредственно или после того, как он в частном случае будет использоваться вторым пользователем.</span><span class="sxs-lookup"><span data-stu-id="c9900-118">Calls can be transferred from one user to another, either directly or after the first user speaks privately with the second user.</span></span> <span data-ttu-id="c9900-119">Пользователи также могут передавать вызовы на другое устройство; Например, они могут передавать активный Звонок на свой мобильный телефон, когда они покажут дверцу своего офиса.</span><span class="sxs-lookup"><span data-stu-id="c9900-119">Users can also transfer calls to another device; for example, they could transfer an active call to their mobile phone as they walk out the door of their office.</span></span>

</div>

<div>

## <a name="richer-communications"></a><span data-ttu-id="c9900-120">Более богатые возможности общения</span><span class="sxs-lookup"><span data-stu-id="c9900-120">Richer Communications</span></span>

<span data-ttu-id="c9900-121">При общении с другим пользователем в Lync пользователи могут легко добавить в вызов текст, видео или Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="c9900-121">When talking to another user with Lync, users can easily add text, video, or desktop sharing to the call.</span></span> <span data-ttu-id="c9900-122">Функция "не беспокоить" интегрируется с параметрами присутствия в Lync.</span><span class="sxs-lookup"><span data-stu-id="c9900-122">The Do-Not-Disturb feature is integrated with the presence settings in Lync.</span></span>

<span data-ttu-id="c9900-123">В единой системе обмена сообщениями Exchange (UM) Lync и Lync Server интегрируются с Microsoft Exchange Server 2013 и Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="c9900-123">With Exchange Unified Messaging (UM), Lync and Lync Server integrate with Microsoft Exchange Server 2013 and Microsoft Outlook 2013.</span></span> <span data-ttu-id="c9900-124">Пользователи могут видеть, есть ли у них новые голосовые сообщения в окне Lync и электронной почте.</span><span class="sxs-lookup"><span data-stu-id="c9900-124">Users can see if they have new voice mail both in their Lync window and in email.</span></span> <span data-ttu-id="c9900-125">В сообщении электронной почты они могут щелкнуть для воспроизведения звукового сообщения голосовой почты по электронной почте или просмотреть транскрипцию сообщения голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="c9900-125">While in email they can click to play the voice mail audio in an email message, or view a transcript of the voice mail message.</span></span>

</div>

<div>

## <a name="advanced-calling-features"></a><span data-ttu-id="c9900-126">Дополнительные возможности звонков</span><span class="sxs-lookup"><span data-stu-id="c9900-126">Advanced Calling Features</span></span>

<span data-ttu-id="c9900-127">Корпоративная голосовая связь включает в себя несколько дополнительных функций для звонков, например делегирование звонков в Lync, звонки групп и групп ответа.</span><span class="sxs-lookup"><span data-stu-id="c9900-127">Enterprise Voice includes several advanced calling features as well, such as Lync call delegation, team calling, Group Call Pickup, and Response Groups.</span></span>

<span data-ttu-id="c9900-128">Делегирование звонков в Lync позволяет пользователям делегировать обработку звонков одному или нескольким помощникам, перейдя в **меню Сервис** \> **Параметры** \> **переадресации звонков**.</span><span class="sxs-lookup"><span data-stu-id="c9900-128">Lync call delegation enables users to delegate call handling to one or more assistants, by going to **Tools** \> **Options** \> **Call Forwarding Settings**.</span></span> <span data-ttu-id="c9900-129">Делегат может выполнять несколько задач по звонку от имени пользователя, в том числе на вызовы для отбора, помещение звонков и инициализация конференций.</span><span class="sxs-lookup"><span data-stu-id="c9900-129">The delegate can perform multiple calling tasks on behalf of the user, including screening calls, placing calls, and initiating conferences.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c9900-130">Возможно, вы ищете другую функцию с похожим именем и делегирование календаря в Lync.</span><span class="sxs-lookup"><span data-stu-id="c9900-130">You may be looking for another similarly named feature, Lync calendar delegation.</span></span> <span data-ttu-id="c9900-131">Для этого не требуется функция корпоративной голосовой связи, и пользователи не смогут планировать собрания Lync в сети из Outlook.</span><span class="sxs-lookup"><span data-stu-id="c9900-131">It doesn't require the Enterprise Voice feature and does allow users to schedule online Lync meetings from Outlook.</span></span> <span data-ttu-id="c9900-132">Если вы ищете эти сведения, рекомендуем извлечь <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy">Set-CsClientPolicy</A> , чтобы узнать о том, как включить синхронизацию делегатов Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9900-132">If you've come here looking for that info, we recommend checking out <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy">Set-CsClientPolicy</A> for information on enabling Exchange delegate sync.</span></span>



</div>

<span data-ttu-id="c9900-133">Если вы звоните, пользователи смогут звонить другим пользователям одновременно, чтобы они могли отвечать на звонки.</span><span class="sxs-lookup"><span data-stu-id="c9900-133">Team calling enables a user to have incoming calls simultaneously ring the phones of teammates so that anyone on the team can answer the call.</span></span>

<span data-ttu-id="c9900-134">Отправка группового звонка – новая функция в накопительных обновлениях для Lync Server 2013: Февраль 2013, позволяющая пользователям отвечать на входящие звонки своим коллегам со своих телефонов.</span><span class="sxs-lookup"><span data-stu-id="c9900-134">Group Call Pickup, a new feature in Cumulative Updates for Lync Server 2013: February 2013, lets users answer incoming calls to their colleagues from their own phones.</span></span> <span data-ttu-id="c9900-135">Отправка группового звонка в основном вызовет команды, так как входящий звонок наследуется только на телефоне получателя, но любой другой пользователь может ответить на него абонентом, набрав номер группы для отправки звонков.</span><span class="sxs-lookup"><span data-stu-id="c9900-135">Group Call Pickup differs from team calling primarily in that an incoming call rings only at the intended recipient's phone, but any other user can choose to answer it by dialing a call pickup group number.</span></span>

<span data-ttu-id="c9900-136">Группы ответов можно настраивать для постановки в очередь и интеллектуального маршрутизации обращений к определенным агентам.</span><span class="sxs-lookup"><span data-stu-id="c9900-136">Response Groups can be set up for queuing and intelligently routing calls to designated agents.</span></span> <span data-ttu-id="c9900-137">Обычно используются службы поддержки ИТ, горячая модульные ресурсы и другие внутренние центры контактов.</span><span class="sxs-lookup"><span data-stu-id="c9900-137">Common uses include IT helpdesks, human resources hotlines, and other internal contact centers.</span></span>

</div>

<div>

## <a name="enterprise-voice-administration"></a><span data-ttu-id="c9900-138">Корпоративное администрирование голосовой связи</span><span class="sxs-lookup"><span data-stu-id="c9900-138">Enterprise Voice Administration</span></span>

<span data-ttu-id="c9900-139">Lync Server использует стандарты и опубликованные интерфейсы для взаимодействия с существующей инфраструктурой.</span><span class="sxs-lookup"><span data-stu-id="c9900-139">Lync Server uses standards and published interfaces to interoperate with existing infrastructure.</span></span> <span data-ttu-id="c9900-140">Она поддерживает как шлюз, так и SIP (например, магистраль SIP) для подключения к системам IP-АТС и сетям PSTN, так что вы можете перенести пользователей в корпоративную голосовую почту с течением времени и свести к минимуму перерывы.</span><span class="sxs-lookup"><span data-stu-id="c9900-140">It supports both gateway and SIP options (such as SIP trunking) for interconnection to IP PBX systems and the PSTN networks, so that you can migrate users to Enterprise Voice over time, while minimizing disruption.</span></span> <span data-ttu-id="c9900-141">Lync Server поддерживает традиционные кодеки, такие как G. 711, G. 722 и G. 723.1 для обеспечения совместимости с традиционными решениями для VoIP.</span><span class="sxs-lookup"><span data-stu-id="c9900-141">Lync Server supports traditional codecs such as G.711, G.722, and G.723.1 for interoperability with traditional VoIP solutions.</span></span>

<span data-ttu-id="c9900-142">С помощью средства управления допуском звонков (CAC) администраторы могут устанавливать ограничения на объемы голосовых и видеофайлов Lync Server, которые переносятся по сетевым связям, и определяют действия, которые необходимо выполнить, если новый звонок будет превышен лимит.</span><span class="sxs-lookup"><span data-stu-id="c9900-142">With call admission control (CAC), administrators can set limits on the amount of Lync Server voice and video traffic carried on constrained network links, and specify the action to be taken if a new call would exceed the limit.</span></span> <span data-ttu-id="c9900-143">Действия могут включать маршрутизацию по альтернативному пути или отказу в звонке.</span><span class="sxs-lookup"><span data-stu-id="c9900-143">The actions could include routing by an alternate path, or refusing the call.</span></span>

<span data-ttu-id="c9900-144">Сервер Lync Server работает с независимыми сторонними устройствами филиалов для предоставления услуг по местным звонкам и подключениям к КТСОП в филиалах в случае сбоя глобальной сети на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="c9900-144">Lync Server works with third-party Survivable Branch Appliances to provide local calling services and connection to PSTN at branch offices, in case of WAN failure at the central site.</span></span>

<span data-ttu-id="c9900-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9900-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

