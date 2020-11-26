---
title: 'Lync Server 2013: включение приостановки звонков для пользователей'
description: 'Lync Server 2013: Включите приостановку звонков для пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Call Park for users
ms:assetid: 9430763f-3394-467c-9c6d-426bf761604e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398753(v=OCS.15)
ms:contentKeyID: 48184814
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7f9ab23b9fa71943efafd588b8c57a2af781b08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428939"
---
# <a name="enable-call-park-for-users-in-lync-server-2013"></a><span data-ttu-id="0639a-103">Включение приостановки звонков для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0639a-103">Enable Call Park for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0639a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0639a-104">

<span> </span></span></span>

<span data-ttu-id="0639a-105">_**Тема последнего изменения:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="0639a-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="0639a-106">Пользователи не могут приостановить звонки или получить припаркованные звонки, пока они не будут включены в политику голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="0639a-106">Users cannot park calls or retrieve parked calls until they are enabled for Call Park in voice policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0639a-107">По умолчанию приостановление звонков для всех пользователей отключено.</span><span class="sxs-lookup"><span data-stu-id="0639a-107">By default, Call Park is disabled for all users.</span></span>



</div>

<span data-ttu-id="0639a-108">Вы можете включить приостановку звонков в глобальной области или в области действия сайта или пользователя.</span><span class="sxs-lookup"><span data-stu-id="0639a-108">You can enable Call Park at the global scope, or at the site scope or user scope.</span></span> <span data-ttu-id="0639a-109">Уровень пользователя имеет приоритет перед уровнем сайта, а тот в свою очередь – перед глобальным уровнем.</span><span class="sxs-lookup"><span data-stu-id="0639a-109">User scope takes precedence over site scope, and site scope takes precedence over global scope.</span></span> <span data-ttu-id="0639a-110">Если у вас несколько политик голосовой связи, проверьте все политики, чтобы включить приостановку звонков, а не только глобальную политику.</span><span class="sxs-lookup"><span data-stu-id="0639a-110">If you have multiple voice policies, review all the policies to enable Call Park, not just the global policy.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-enable-call-park-for-users"></a><span data-ttu-id="0639a-111">Использование панели управления Lync Server для поддержки приостановки звонков для пользователей</span><span class="sxs-lookup"><span data-stu-id="0639a-111">To Use Lync Server Control Panel to Enable Call Park for Users</span></span>

1.  <span data-ttu-id="0639a-112">Войдите на компьютер в качестве члена группы **RTCUniversalServerAdmins** или роли администратора **CsVoiceAdministrator**, **CsServerAdministrator** или **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="0639a-112">Log on to the computer as a member of the **RTCUniversalServerAdmins** group, or as a member of the **CsVoiceAdministrator**, **CsServerAdministrator**, or **CsAdministrator** administrative role.</span></span>

2.  <span data-ttu-id="0639a-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0639a-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0639a-114">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0639a-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0639a-115">В левой области навигации щелкните элемент **Маршрутизация голосовой связи**.</span><span class="sxs-lookup"><span data-stu-id="0639a-115">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="0639a-116">Перейдите на вкладку **Политика голосовой связи**.</span><span class="sxs-lookup"><span data-stu-id="0639a-116">Click the **Voice Policy** tab.</span></span>

5.  <span data-ttu-id="0639a-117">Дважды щелкните существующую политику голосовой связи, чтобы открыть диалоговое окно **Изменение политики голосовой связи**.</span><span class="sxs-lookup"><span data-stu-id="0639a-117">Double-click an existing voice policy to open the **Edit Voice Policy** dialog box.</span></span>

6.  <span data-ttu-id="0639a-118">В разделе **Функции звонков** установите флажок **Разрешить парковку вызовов**.</span><span class="sxs-lookup"><span data-stu-id="0639a-118">Under **Calling features**, select **Enable call park**.</span></span>

7.  <span data-ttu-id="0639a-119">Чтобы сохранить политику голосовой связи, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0639a-119">Click **OK** to save the voice policy</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-enable-call-park-for-users"></a><span data-ttu-id="0639a-120">Использование командлетов для поддержки приостановки звонков для пользователей</span><span class="sxs-lookup"><span data-stu-id="0639a-120">To Use Cmdlets to Enable Call Park for Users</span></span>

1.  <span data-ttu-id="0639a-121">Войдите на компьютер в качестве члена группы RTCUniversalServerAdmins или роли администратора CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="0639a-121">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator administrative role.</span></span>

2.  <span data-ttu-id="0639a-122">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="0639a-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="0639a-123">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0639a-123">Run:</span></span>
    
        Set-CsVoicePolicy -Identity <VoicePolicy> -EnableCallPark $true
    
    <span data-ttu-id="0639a-124">Например, чтобы включить приостановку звонков для глобальной политики голосовой связи по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="0639a-124">For example, to enable Call Park for the default global voice policy:</span></span>
    
        Set-CsVoicePolicy -EnableCallPark $true

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0639a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0639a-125">See Also</span></span>


[<span data-ttu-id="0639a-126">Создание политики голосовой связи и настройка записей об использовании PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0639a-126">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)  
  

<span data-ttu-id="0639a-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0639a-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

