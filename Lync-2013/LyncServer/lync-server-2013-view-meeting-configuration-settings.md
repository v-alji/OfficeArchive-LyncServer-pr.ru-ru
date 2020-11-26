---
title: 'Lync Server 2013: Просмотр параметров конфигурации собраний'
description: 'Lync Server 2013: Просмотр параметров конфигурации собраний.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View meeting configuration settings
ms:assetid: d03a4684-9d8b-4728-917d-5b5c91511e2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721894(v=OCS.15)
ms:contentKeyID: 49733828
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 190b9d331a8cd0a08e17c482dbc3b0bc27590003
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446978"
---
# <a name="view-meeting-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="3fcb9-103">Просмотр параметров конфигурации собрания в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fcb9-103">View meeting configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fcb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fcb9-104">

<span> </span></span></span>

<span data-ttu-id="3fcb9-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="3fcb9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="3fcb9-106">В панели управления Lync Server 2013 вы можете управлять реализацией собраний в развертывании с помощью параметров настройки собраний.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-106">In Lync Server 2013 Control Panel, you use meeting configuration setting to control how meetings are implemented in your deployment.</span></span> <span data-ttu-id="3fcb9-107">Сюда входят следующие конфигурации собрания:</span><span class="sxs-lookup"><span data-stu-id="3fcb9-107">This includes the following meeting configurations:</span></span>

  - <span data-ttu-id="3fcb9-108">Глобальная конфигурация, создаваемая по умолчанию при развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="3fcb9-109">Необязательные конфигурации уровня сайта и уровня пользователя, которые можно создать и использовать для определения способа реализации собраний для конкретных сайтов или пользователей.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-109">Optional site-level and user-level configurations that you can create and use to specify how meetings are implemented for specific sites or users.</span></span>

<div>

## <a name="to-view-meeting-configuration-settings"></a><span data-ttu-id="3fcb9-110">Просмотр параметров конфигурации собрания</span><span class="sxs-lookup"><span data-stu-id="3fcb9-110">To view meeting configuration settings</span></span>

1.  <span data-ttu-id="3fcb9-111">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3fcb9-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3fcb9-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3fcb9-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3fcb9-114">На панели навигации слева выберите **Конференц** -связь, а затем — **Конфигурация собрания**.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-114">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="3fcb9-115">На странице **Конфигурация собрания** (Конфигурация собраний) щелкните конфигурацию собраний, которую требуется просмотреть.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-115">On the **Meeting Configuration** page, click the meeting configuration that you would like to view.</span></span>

5.  <span data-ttu-id="3fcb9-116">В окне " **Изменение фильтра файлов**" выберите **Показать подробности...**</span><span class="sxs-lookup"><span data-stu-id="3fcb9-116">In **Edit File Filter**, select the **Show Details…**</span></span> <span data-ttu-id="3fcb9-117">флажок.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-117">check box.</span></span>
    
    <span data-ttu-id="3fcb9-118">**Изменение конфигурации собрания — \<policy\>** Открытие отображения параметров выбранной политики.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-118">**Edit Meeting Configuration - \<policy\>** opens displaying the settings for the selected policy.</span></span> <span data-ttu-id="3fcb9-119">Сведения о настройке параметров можно найти в разделе [Создание или изменение коллекции параметров конфигурации собраний в Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3fcb9-119">For details about configuring the settings, see [Create or modify a collection of meeting configuration settings in Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md).</span></span>

</div>

<div>

## <a name="viewing-meeting-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="3fcb9-120">Просмотр сведений о конфигурации собраний с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3fcb9-120">Viewing Meeting Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="3fcb9-121">Параметры конфигурации собраний можно просматривать с помощью Windows PowerShell и командлета Get-CsMeetingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-121">Meeting configuration settings can be viewed by using Windows PowerShell and the Get-CsMeetingConfiguration cmdlet.</span></span> <span data-ttu-id="3fcb9-122">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="3fcb9-123">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="3fcb9-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-meeting-configuration-information"></a><span data-ttu-id="3fcb9-124">Просмотр сведений о настройке собрания</span><span class="sxs-lookup"><span data-stu-id="3fcb9-124">To view meeting configuration information</span></span>

  - <span data-ttu-id="3fcb9-125">Чтобы просмотреть сведения о всех параметрах конфигурации собрания, введите в командной консоли Lync Server указанную ниже команду и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="3fcb9-125">To view information about all your meeting configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsMeetingConfiguration
    
    <span data-ttu-id="3fcb9-126">Команда возвращает примерно следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="3fcb9-126">That will return information similar to this:</span></span>
    
        Identity                        : Global
        PstnCallersBypassLobby          : True
        EnableAssignedConferenceType    : True
        DesignateAsPresenter            : Company
        AssignedConferenceTypeByDefault : True
        AdmitAnonymousUsersByDefault    : True
        RequireRoomSystemsAuthorization : False
        LogoURL                         :
        LegalURL                        :
        HelpURL                         :
        CustomFooterText                :
        AllowConferenceRecording        : True

</div>

<span data-ttu-id="3fcb9-127">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsMeetingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="3fcb9-127">For more information, see the help topic for the [Get-CsMeetingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration) cmdlet.</span></span>

<span data-ttu-id="3fcb9-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fcb9-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

