---
title: 'Lync Server 2013: настройка для использования push-уведомлений'
description: 'Lync Server 2013: Настройка push-уведомлений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring for push notifications
ms:assetid: d77f2c06-0fe6-45d5-8f08-808ab871b3e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690047(v=OCS.15)
ms:contentKeyID: 48185574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24c22ff42f666add9eac4966134c88b9bf680046
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433085"
---
# <a name="configuring-for-push-notifications-in-lync-server-2013"></a><span data-ttu-id="f1b5f-103">Настройка для использования push-уведомлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1b5f-103">Configuring for push notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1b5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1b5f-104">

<span> </span></span></span>

<span data-ttu-id="f1b5f-105">_**Тема последнего изменения:** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="f1b5f-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<span data-ttu-id="f1b5f-106">Push-уведомления, в форме индикаторов, значков или оповещений, могут отправляться на мобильное устройство, даже если мобильное приложение неактивно.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="f1b5f-107">Push-уведомления извещать пользователей о таких событиях, как новое или пропущенное приглашение на обмен мгновенными сообщениями и голосовая почта.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="f1b5f-108">Служба Lync Server 2013 Mobility Service отправляет уведомления на облачную службу push-уведомлений Lync Server, которая затем отправляет уведомления в службу извещающих уведомлений Apple (для устройства Apple, работающего на мобильном клиенте Lync 2010) или службу push-уведомлений Майкрософт (MPNS) (для устройства с Windows Phone, работающего под управлением Lync 2010 Mobile или Lync 2013 Mobile).</span><span class="sxs-lookup"><span data-stu-id="f1b5f-108">The Lync Server 2013 Mobility Service sends the notifications to the cloud-based Lync Server Push Notification Service, which then sends the notifications to the Apple Push Notification Service (APNS) (for an Apple device running the Lync 2010 Mobile client) or the Microsoft Push Notification Service (MPNS) (for a Windows Phone device running the Lync 2010 Mobile or the Lync 2013 Mobile client).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f1b5f-109">Если вы используете Windows Phone с мобильным клиентом Lync 2010 Mobile или Lync 2013 для мобильных устройств, следует учитывать push-уведомление.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-109">If you use Windows Phone with Lync 2010 Mobile or Lync 2013 Mobile client, push notification is an important consideration.</span></span><BR><span data-ttu-id="f1b5f-110">Если вы используете Lync 2010 Mobile на устройствах Apple, следует учитывать push-уведомление.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-110">If you use Lync 2010 Mobile on Apple devices, push notification is an important consideration.</span></span><BR><span data-ttu-id="f1b5f-111">Если вы используете Lync 2013 Mobile на устройствах Apple, вам больше не нужно push-уведомление.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-111">If you use Lync 2013 Mobile on Apple devices, you no longer need push notification.</span></span>



</div>

<span data-ttu-id="f1b5f-112">Настройте топологию для поддержки push-уведомлений, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-112">Configure your topology to support push notifications by doing the following:</span></span>

  - <span data-ttu-id="f1b5f-113">Если в вашей среде есть сервер Lync Server 2010 или Lync Server 2013 EDGE, вам нужно добавить нового поставщика услуг размещения, Microsoft Lync Online, а затем настроить федерацию поставщика услуг размещения между вашей организацией и Lync Online.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-113">If your environment has a Lync Server 2010 or Lync Server 2013 Edge Server, you need to add a new hosting provider, Microsoft Lync Online, and then set up hosting provider federation between your organization and Lync Online.</span></span>

  - <span data-ttu-id="f1b5f-114">Если в вашей среде есть сервер Office Communications Server 2007 R2, вам нужно настроить прямую федерацию SIP с помощью push.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-114">If your environment has a Office Communications Server 2007 R2 Edge Server, you need to set up direct SIP federation with push.lync.com.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1b5f-115">Push.lync.com — домен Microsoft Office 365 для службы push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-115">Push.lync.com is a Microsoft Office 365 domain for Push Notification Service.</span></span>

    
    </div>

  - <span data-ttu-id="f1b5f-116">Чтобы включить push-уведомления, необходимо выполнить командлет **Set – CsPushNotificationConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f1b5f-116">To enable push notifications, you need to run the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="f1b5f-117">По умолчанию push-уведомления отключены.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-117">By default, push notifications are turned off.</span></span>

  - <span data-ttu-id="f1b5f-118">Проверка конфигурации Федерации и push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-118">Test the federation configuration and push notifications.</span></span>

<div>

## <a name="to-configure-for-push-notifications-with-lync-server-2013-or-lync-server-2010-edge-server"></a><span data-ttu-id="f1b5f-119">Настройка push-уведомлений с помощью Lync Server 2013 или Lync Server 2010 Edge Server</span><span class="sxs-lookup"><span data-stu-id="f1b5f-119">To configure for push notifications with Lync Server 2013 or Lync Server 2010 Edge Server</span></span>

1.  <span data-ttu-id="f1b5f-120">Войдите в систему на компьютере, на котором оболочка Lync Server Management Shell и OCSCore устанавливается как участник группы RtcUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-120">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="f1b5f-121">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f1b5f-122">Добавьте поставщика услуг размещения Lync Server Online.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-122">Add a Lync Server online hosting provider.</span></span> <span data-ttu-id="f1b5f-123">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-123">At the command line, type:</span></span>
    
        New-CsHostingProvider -Identity <unique identifier for Lync Online hosting provider> -Enabled $True -ProxyFqdn <FQDN for the Access Server used by the hosting provider> -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="f1b5f-124">Например:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-124">For example:</span></span>
    
        New-CsHostingProvider -Identity "LyncOnline" -Enabled $True -ProxyFqdn "sipfed.online.lync.com" -VerificationLevel UseSourceVerification
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1b5f-125">У вас не может быть более одной связи Федерации с одним поставщиком услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-125">You cannot have more than one federation relationship with a single hosting provider.</span></span> <span data-ttu-id="f1b5f-126">Таким образом, если вы уже настроили поставщика услуг размещения с отношением Федерации с sipfed.online.lync.com, не добавляйте для него другого поставщика услуг размещения, даже если удостоверение поставщика услуг размещения не является LyncOnline.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-126">That is, if you have already set up a hosting provider that has a federation relationship with sipfed.online.lync.com, do not add another hosting provider for it, even if the identity of the hosting provider is something other than LyncOnline.</span></span>

    
    </div>

4.  <span data-ttu-id="f1b5f-127">Настройте федерацию поставщика услуг хостинга между вашей организацией и службой push-уведомлений в Lync Online.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-127">Set up hosting provider federation between your organization and the Push Notification Service at Lync Online.</span></span> <span data-ttu-id="f1b5f-128">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-128">At the command line, type:</span></span>
    
        New-CsAllowedDomain -Identity "push.lync.com"

</div>

<div>

## <a name="to-configure-for-push-notifications-with-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="f1b5f-129">Настройка push-уведомлений с помощью пограничного сервера Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="f1b5f-129">To configure for push notifications with Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="f1b5f-130">Войдите на пограничный сервер в качестве участника группы RtcUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-130">Log on to the Edge Server as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="f1b5f-131">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Администрирование**, а затем — **Управление компьютером**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-131">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Computer Management**.</span></span>

3.  <span data-ttu-id="f1b5f-132">В дереве консоли разверните узел **службы и приложения**, щелкните правой кнопкой мыши **Microsoft Office Communications Server 2007 R2** и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-132">In the console tree, expand **Services and Applications**, right-click **Microsoft Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="f1b5f-133">На вкладке **Разрешить** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-133">On the **Allow** tab, click **Add**.</span></span>

5.  <span data-ttu-id="f1b5f-134">В диалоговом окне **Добавление федеративного партнера** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-134">In the **Add Federated Partner** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="f1b5f-135">В **доменном имени федеративного партнера** введите **Push.Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-135">In **Federated partner domain name**, type **push.lync.com**.</span></span>
    
      - <span data-ttu-id="f1b5f-136">В **пограничный сервер для федеративного партнера Access** введите **sipfed.Online.Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-136">In **Federated partner Access Edge Server**, type **sipfed.online.lync.com**.</span></span>
    
      - <span data-ttu-id="f1b5f-137">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-137">Click **OK**.</span></span>

</div>

<div>

## <a name="to-enable-push-notifications"></a><span data-ttu-id="f1b5f-138">Включение push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="f1b5f-138">To enable push notifications</span></span>

1.  <span data-ttu-id="f1b5f-139">Войдите в систему на компьютере, на котором оболочка Lync Server Management Shell и OCSCore установлен в качестве участника роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-139">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="f1b5f-140">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f1b5f-141">Включение push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-141">Enable push notifications.</span></span> <span data-ttu-id="f1b5f-142">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-142">At the command line, type:</span></span>
    
        Set-CsPushNotificationConfiguration -EnableApplePushNotificationService $True -EnableMicrosoftPushNotificationService $True

4.  <span data-ttu-id="f1b5f-143">Включите Федерацию.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-143">Enable federation.</span></span> <span data-ttu-id="f1b5f-144">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-144">At the command line, type:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

</div>

<div>

## <a name="to-test-federation-and-push-notifications"></a><span data-ttu-id="f1b5f-145">Тестирование Федерации и push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="f1b5f-145">To test federation and push notifications</span></span>

1.  <span data-ttu-id="f1b5f-146">Войдите в систему на компьютере, на котором оболочка Lync Server Management Shell и OCSCore установлен в качестве участника роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-146">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="f1b5f-147">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f1b5f-148">Проверьте конфигурацию Федерации.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-148">Test the federation configuration.</span></span> <span data-ttu-id="f1b5f-149">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-149">At the command line, type:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn <FQDN of Access Edge server used for federated SIP traffic> -Domain <FQDN of federated domain> -ProxyFqdn <FQDN of the Access Edge server used by the federated organization>
    
    <span data-ttu-id="f1b5f-150">Например:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-150">For example:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn accessproxy.contoso.com -Domain push.lync.com -ProxyFqdn sipfed.online.lync.com

4.  <span data-ttu-id="f1b5f-151">Тест push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f1b5f-151">Test push notifications.</span></span> <span data-ttu-id="f1b5f-152">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-152">At the command line, type:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn <Access Edge service FQDN>
    
    <span data-ttu-id="f1b5f-153">Например:</span><span class="sxs-lookup"><span data-stu-id="f1b5f-153">For example:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn accessproxy.contoso.com

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f1b5f-154">См. также</span><span class="sxs-lookup"><span data-stu-id="f1b5f-154">See Also</span></span>


[<span data-ttu-id="f1b5f-155">Test-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="f1b5f-155">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
[<span data-ttu-id="f1b5f-156">Test-CsMcxPushNotification</span><span class="sxs-lookup"><span data-stu-id="f1b5f-156">Test-CsMcxPushNotification</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification)  
  

<span data-ttu-id="f1b5f-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1b5f-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

