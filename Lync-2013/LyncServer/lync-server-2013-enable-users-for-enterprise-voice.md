---
title: 'Lync Server 2013: включение пользователей для корпоративной голосовой связи'
description: 'Lync Server 2013: включение пользователей для корпоративного голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for Enterprise Voice
ms:assetid: f252b23b-9641-4160-aa81-bf06dc2eced3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413011(v=OCS.15)
ms:contentKeyID: 48185800
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8aa8dbbeb507ced5217e517c1608c3a2a9259668
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400024"
---
# <a name="enable-users-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="11558-103">Включение пользователей корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="11558-103">Enable users for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="11558-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="11558-104">

<span> </span></span></span>

<span data-ttu-id="11558-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="11558-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="11558-106">После установки файлов для одного или нескольких серверов-исправлений Настройте маршрутизацию исходящих вызовов и, при необходимости, развернуть один или несколько дополнительных функций для корпоративной голосовой связи, вы можете использовать описанные ниже действия, чтобы разрешить пользователю совершать звонки с помощью корпоративного голоса.</span><span class="sxs-lookup"><span data-stu-id="11558-106">After you install files for one or more Mediation Servers, configure outbound call routing, and optionally deploy one or more advanced Enterprise Voice features, you can use the following procedures to enable a user to make calls by using Enterprise Voice:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="11558-107">Из описанных ниже процедур можно выполнить только первую операцию с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="11558-107">Of the following procedures, only the first can be performed by using Lync Server Control Panel.</span></span> <span data-ttu-id="11558-108">Остальные процедуры можно использовать только в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="11558-108">For the remaining procedures, you can use only Lync Server Management Shell.</span></span>



</div>

  - <span data-ttu-id="11558-109">Включение учетной записи пользователя для корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="11558-109">Enable the user account for Enterprise Voice.</span></span>

  - <span data-ttu-id="11558-110">(Необязательно) Назначьте учетной записи пользователя определенную политику голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="11558-110">(Optional) Assign the user account a user-specific voice policy.</span></span>

  - <span data-ttu-id="11558-111">(Необязательно) Назначьте учетной записи пользователя определенную абонентскую группу.</span><span class="sxs-lookup"><span data-stu-id="11558-111">(Optional) Assign the user account a user-specific dial plan.</span></span>

<div>

## <a name="to-enable-a-user-account-for-enterprise-voice"></a><span data-ttu-id="11558-112">Включение учетной записи пользователя для корпоративной голосовой связи</span><span class="sxs-lookup"><span data-stu-id="11558-112">To enable a user account for Enterprise Voice</span></span>

1.  <span data-ttu-id="11558-113">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="11558-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="11558-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="11558-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="11558-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="11558-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="11558-116">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="11558-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="11558-117">В поле **Поиск пользователей** введите отображаемое имя или его начальный фрагмент, имя, фамилию, имя учетной записи (диспетчера учетных записей безопасности (SAM), SIP-адрес или строку универсального кода ресурса (URI) из учетной записи пользователя, которому требуется предоставить доступ, затем нажмите кнопку **Найти**.</span><span class="sxs-lookup"><span data-stu-id="11558-117">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="11558-118">В таблице выберите учетную запись пользователя, которую вы хотите включить для корпоративного голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="11558-118">In the table, click the user account that you want to enable for Enterprise Voice.</span></span>

6.  <span data-ttu-id="11558-119">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="11558-119">On the **Edit** menu, click **Show details**.</span></span>

7.  <span data-ttu-id="11558-120">На странице " **изменение пользователя Lync Server** " в разделе **телефония** выберите **Корпоративный голосовой звонок**.</span><span class="sxs-lookup"><span data-stu-id="11558-120">On the **Edit Lync Server User** page, under **Telephony**, click **Enterprise Voice**.</span></span>

8.  <span data-ttu-id="11558-121">Щелкните **URI строки** и введите уникальный нормализованный номер телефона (например, tel:+14255550200).</span><span class="sxs-lookup"><span data-stu-id="11558-121">Click **Line URI**, and then type a unique, normalized phone number (for example, tel:+14255550200).</span></span>

9.  <span data-ttu-id="11558-122">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="11558-122">Click **Commit**.</span></span>

<span data-ttu-id="11558-123">Чтобы завершить включение пользователя для корпоративного голосовой связи, убедитесь, что пользователю назначена политика голосовой связи и абонентская группа, будь это глобальная (назначена по умолчанию) или для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="11558-123">To finish enabling a user for Enterprise Voice, be sure that the user is assigned a voice policy and a dial plan, whether global (assigned by default) or user-specific.</span></span>

<span data-ttu-id="11558-124">По умолчанию всем пользователям назначается Глобальная политика голосовой связи и абонентская группа.</span><span class="sxs-lookup"><span data-stu-id="11558-124">By default, all users are assigned a global voice policy and dial plan.</span></span> <span data-ttu-id="11558-125">Если политика голосовой связи или абонентские группы находятся на уровне сайта для сайта, на котором находится учетная запись пользователя, эти политики сайта будут автоматически применены к пользователю.</span><span class="sxs-lookup"><span data-stu-id="11558-125">If a voice policy or dial plan exists at the site level for the site on which the user account is homed, those site policies will automatically apply to the user.</span></span> <span data-ttu-id="11558-126">Чтобы применить политику голосовой почты или абонентскую группу для пользователя, необходимо запустить командлеты **Grant-CsVoicePolicy** и **Grant-CsDialPlan** .</span><span class="sxs-lookup"><span data-stu-id="11558-126">To apply a per-user voice policy or dial plan to a user, you must run the **Grant-CsVoicePolicy** and **Grant-CsDialPlan** cmdlets.</span></span> <span data-ttu-id="11558-127">Подробные сведения можно найти в руководстве по [среде управления Lync Server 2013](lync-server-2013-lync-server-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="11558-127">For details, see the [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) documentation.</span></span>

</div>

<div>

## <a name="voice-policy-assignment"></a><span data-ttu-id="11558-128">Назначение политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="11558-128">Voice Policy Assignment</span></span>

<span data-ttu-id="11558-129">Глобальные политики и стратегии голосовой связи на уровне сайта автоматически назначаются всем учетным записям пользователей, которые включены в корпоративный голосовую почту.</span><span class="sxs-lookup"><span data-stu-id="11558-129">Global and site-level voice policies are automatically assigned to all user accounts that are enabled for Enterprise Voice.</span></span> <span data-ttu-id="11558-130">Можно также создавать политики, применимые к определенным пользователям или группам.</span><span class="sxs-lookup"><span data-stu-id="11558-130">You can also create voice policies that apply to specific users or groups.</span></span> <span data-ttu-id="11558-131">Такие политики необходимо назначать пользователям или группам в явном виде.</span><span class="sxs-lookup"><span data-stu-id="11558-131">These per-user policies must be explicitly assigned to the users or groups.</span></span> <span data-ttu-id="11558-132">Если вы хотите использовать глобальную политику голосовой почты для всех пользователей, которым разрешена Корпоративная голосовая связь, вы можете пропустить этот раздел и перейти к разделу назначение абонентской группы ниже в этой статье.</span><span class="sxs-lookup"><span data-stu-id="11558-132">If you want to use the global or site voice policy for all users who are enabled for Enterprise Voice, you can skip this section and continue to Dial Plan Assignment section later in this topic.</span></span>

<div>

## <a name="to-assign-a-user-specific-voice-policy"></a><span data-ttu-id="11558-133">Назначение политики голосовой связи для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="11558-133">To assign a user-specific voice policy</span></span>

1.  <span data-ttu-id="11558-134">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="11558-134">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="11558-135">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="11558-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="11558-136">Чтобы назначить существующую политику голосовой связи пользователю, выполните следующую команду в окне командной строки:</span><span class="sxs-lookup"><span data-stu-id="11558-136">To assign an existing user voice policy to a user, run the following at the command prompt:</span></span>
    
        Grant-CsVoicePolicy -Identity <UserIdParameter> -PolicyName <String>
    
    <span data-ttu-id="11558-137">Например:</span><span class="sxs-lookup"><span data-stu-id="11558-137">For example:</span></span>
    
        Grant-CsVoicePolicy -Identity "Bob Kelly" -PolicyName VoicePolicyJapan
    
    <span data-ttu-id="11558-138">В этом примере пользователь с отображаемым именем Bob Юлия назначается политике голосовой связи с именем **VoicePolicyJapan**.</span><span class="sxs-lookup"><span data-stu-id="11558-138">In this example, the user with the display name Bob Kelly is assigned the voice policy with the name **VoicePolicyJapan**.</span></span>

<span data-ttu-id="11558-139">Сведения о назначении политики голосовой связи для определенного пользователя или о том, как запускать командлет **Grant-CsVoicePolicy** , можно найти в документации по [командной консоли Lync Server 2013](lync-server-2013-lync-server-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="11558-139">For details about assigning a user-specific voice policy or about running the **Grant-CsVoicePolicy** cmdlet, see the [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) documentation.</span></span>

</div>

</div>

<span id="BKMK_DialPlanAssignment"></span>

<div>

## <a name="dial-plan-assignment"></a><span data-ttu-id="11558-140">Назначение абонентской группы</span><span class="sxs-lookup"><span data-stu-id="11558-140">Dial Plan Assignment</span></span>

<span data-ttu-id="11558-141">Чтобы завершить настройку учетной записи пользователя либо для пользователей корпоративной голосовой связи, либо для пользователей конференц-связи с телефонным подключением, пользователю должна быть назначена абонентская группа.</span><span class="sxs-lookup"><span data-stu-id="11558-141">To complete user account configuration for either users of Enterprise Voice or users of dial-in conferencing, the user must be assigned a dial plan.</span></span> <span data-ttu-id="11558-142">Учетные записи пользователей будут автоматически использовать глобальную абонентскую группу или, если таковая существует, это абонентская группа на уровне сайта, если вы не хотите явно назначать существующий абонентский набор для пользователей.</span><span class="sxs-lookup"><span data-stu-id="11558-142">User accounts will automatically use the global dial plan or, if one exists, the site-level dial plan, when you do not explicitly assign an existing per-user dial plan.</span></span> <span data-ttu-id="11558-143">Если вы хотите использовать глобальную или общую абонентскую группу для всех пользователей, для которых разрешена Корпоративная голосовая связь, вы можете пропустить этот раздел.</span><span class="sxs-lookup"><span data-stu-id="11558-143">If you want to use the global or site dial plan for all users who are enabled for Enterprise Voice, you can skip this section.</span></span>

<div>

## <a name="to-assign-a-dial-plan"></a><span data-ttu-id="11558-144">Назначение абонентской группы</span><span class="sxs-lookup"><span data-stu-id="11558-144">To assign a dial plan</span></span>

1.  <span data-ttu-id="11558-145">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="11558-145">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="11558-146">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="11558-146">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="11558-147">Чтобы назначить абонентскую группу для отдельных пользователей, выполните следующую команду в окне командной строки:</span><span class="sxs-lookup"><span data-stu-id="11558-147">To assign a user-specific dial plan, run the following at the command prompt:</span></span>
    
        Grant-CsDialPlan -Identity <UserIdParameter> -PolicyName <String>
    
    <span data-ttu-id="11558-148">Например:</span><span class="sxs-lookup"><span data-stu-id="11558-148">For example:</span></span>
    
        Grant-CsDialPlan -Identity "Bob Kelly" -PolicyName DialPlanJapan
    
    <span data-ttu-id="11558-149">В этом примере пользователю с отображаемым именем Bob Юлия назначается абонентская группа с именем **DialPlanJapan**.</span><span class="sxs-lookup"><span data-stu-id="11558-149">In this example, the user with the display name Bob Kelly is assigned the user dial plan with the name **DialPlanJapan**.</span></span>

<span data-ttu-id="11558-150">Сведения о назначении абонентской группы или о том, как запустить командлет **Grant-CsDialPlan** , можно найти в документации по [командной консоли Lync Server 2013](lync-server-2013-lync-server-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="11558-150">For details about assigning a user dial plan or about running the **Grant-CsDialPlan** cmdlet, see the [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) documentation.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="11558-151">См. также</span><span class="sxs-lookup"><span data-stu-id="11558-151">See Also</span></span>


[<span data-ttu-id="11558-152">Отключение пользователя для корпоративного голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="11558-152">Disable a user for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-disable-a-user-for-enterprise-voice.md)  
  

<span data-ttu-id="11558-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="11558-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

