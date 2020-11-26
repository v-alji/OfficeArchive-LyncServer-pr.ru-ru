---
title: 'Lync Server 2013: Просмотр сведений о политике конференц-связи'
description: 'Lync Server 2013: Просмотр сведений о политике конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View conferencing policy information
ms:assetid: e99fdc4d-926a-4e36-ac99-ab5035568847
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721918(v=OCS.15)
ms:contentKeyID: 49733852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e463c500e48f4032c8dab3a3787715f7265be9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438654"
---
# <a name="view-conferencing-policy-information-in-lync-server-2013"></a><span data-ttu-id="d07eb-103">Просмотр сведений о политике конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d07eb-103">View conferencing policy information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d07eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d07eb-104">

<span> </span></span></span>

<span data-ttu-id="d07eb-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="d07eb-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="d07eb-106">В панели управления Lync Server 2013 вы можете управлять реализацией конференций в развертывании с помощью политик конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="d07eb-106">In Lync Server 2013 Control Panel, you use conferencing policies to control how conferencing is implemented in your deployment.</span></span> <span data-ttu-id="d07eb-107">Сюда относятся следующие политики конференц-связи:</span><span class="sxs-lookup"><span data-stu-id="d07eb-107">This includes the following conferencing policies:</span></span>

  - <span data-ttu-id="d07eb-108">Глобальная политика, созданная по умолчанию при развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d07eb-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="d07eb-109">Необязательная политика уровня сайта и пользовательского уровня, которую можно создать и использовать для определения способа реализации конференции для конкретных сайтов или пользователей.</span><span class="sxs-lookup"><span data-stu-id="d07eb-109">Optional site-level and user-level policy that you can create and use to specify how conferencing is implemented for specific sites or users.</span></span>

<div>

## <a name="to-view-conferencing-policy-settings"></a><span data-ttu-id="d07eb-110">Просмотр параметров политики конференций</span><span class="sxs-lookup"><span data-stu-id="d07eb-110">To view conferencing policy settings</span></span>

1.  <span data-ttu-id="d07eb-111">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d07eb-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d07eb-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d07eb-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d07eb-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d07eb-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d07eb-114">На панели навигации слева выберите **Конференц** -связь, а затем — **Политика Конференц**-связи.</span><span class="sxs-lookup"><span data-stu-id="d07eb-114">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="d07eb-115">На странице **Политика конференц-связи** дважды щелкните политику, которую вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="d07eb-115">On the **Conferencing Policy** page, double-click the conferencing policy that you would like to view.</span></span>

5.  <span data-ttu-id="d07eb-116">В окне " **Изменение фильтра файлов**" выберите **Показать подробности...**</span><span class="sxs-lookup"><span data-stu-id="d07eb-116">In **Edit File Filter**, select the **Show Details…**</span></span> <span data-ttu-id="d07eb-117">флажок.</span><span class="sxs-lookup"><span data-stu-id="d07eb-117">check box.</span></span>
    
    <span data-ttu-id="d07eb-118">**Изменение политики Конференц- \<policy\>** связи Открытие отображения параметров выбранной политики.</span><span class="sxs-lookup"><span data-stu-id="d07eb-118">**Edit Conferencing Policy - \<policy\>** opens displaying the settings for the selected policy.</span></span> <span data-ttu-id="d07eb-119">Подробнее о настройке параметров можно узнать в разделе [Создание или изменение политики конференц-связи в Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span><span class="sxs-lookup"><span data-stu-id="d07eb-119">For details about configuring the settings, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span></span>

</div>

<div>

## <a name="viewing-conferencing-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d07eb-120">Просмотр политик конференц-связи с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d07eb-120">Viewing Conferencing Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d07eb-121">Политики конференц-связи можно просматривать с помощью Windows PowerShell и командлета Get-CsConferencingPolicy.</span><span class="sxs-lookup"><span data-stu-id="d07eb-121">Conferencing policies can be viewed by using Windows PowerShell and the Get-CsConferencingPolicy cmdlet.</span></span> <span data-ttu-id="d07eb-122">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d07eb-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d07eb-123">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d07eb-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-conferencing-policies"></a><span data-ttu-id="d07eb-124">Просмотр политик конференц-связи</span><span class="sxs-lookup"><span data-stu-id="d07eb-124">To view conferencing policies</span></span>

  - <span data-ttu-id="d07eb-125">Чтобы просмотреть сведения обо всех политиках конференц-связи, введите следующую команду в командной консоли Lync Server Management Shell и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="d07eb-125">To view information about all your conferencing policies, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsConferencingPolicy
    
    <span data-ttu-id="d07eb-126">Команда возвращает примерно следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="d07eb-126">That will return information similar to this:</span></span>
    
        Identity                                  : Global
        AllowIPAudio                              : True
        AllowIPVideo                              : True
        AllowMultiView                            : True
        Description                               :
        AllowParticipantControl                   : True
        AllowAnnotations                          : True
        DisablePowerPointAnnotations              : False
        AllowUserToScheduleMeetingsWithAppSharing : True
        AllowNonEnterpriseVoiceUsersToDialOut     : False
        AllowAnonymousUsersToDialOut              : False
        AllowAnonymousParticipantsInMeetings      : True
        AllowExternalUsersToSaveContent           : True
        AllowExternalUserControl                  : False
        AllowExternalUsersToRecordMeeting         : False
        AllowPolls                                : True
        AllowSharedNotes                          : True
        EnableDialInConferencing                  : True
        EnableAppDesktopSharing                   : Desktop
        AllowConferenceRecording                  : False
        EnableP2PRecording                        : False
        EnableFileTransfer                        : True
        EnableP2PFileTransfer                     : True
        EnableP2PVideo                            : True
        AllowLargeMeetings                        : False
        EnableDataCollaboration                   : True
        MaxVideoConferenceResolution              : VGA
        MaxMeetingSize                            : 250
        AudioBitRateKb                            : 200
        VideoBitRateKb                            : 50000
        AppSharingBitRateKb                       : 50000
        FileTransferBitRateKb                     : 50000
        TotalReceiveVideoBitRateKb                : 6000
        EnableMultiViewJoin                       : True

</div>

<span data-ttu-id="d07eb-127">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsConferencingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="d07eb-127">For more information, see the help topic for the [Get-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsConferencingPolicy) cmdlet.</span></span>

<span data-ttu-id="d07eb-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d07eb-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

