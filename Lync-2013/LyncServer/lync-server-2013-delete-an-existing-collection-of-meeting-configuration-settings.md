---
title: Удаление существующей коллекции параметров конфигурации собрания
description: Удаление существующей коллекции параметров конфигурации собраний.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of meeting configuration settings
ms:assetid: 92ff8a91-05c5-4047-a533-5dff12f22299
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688136(v=OCS.15)
ms:contentKeyID: 49733736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc0985023a1459130c7d589327535436145a0ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430534"
---
# <a name="delete-an-existing-collection-of-meeting-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="24dab-103">Удаление существующей коллекции параметров конфигурации собрания в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24dab-103">Delete an existing collection of meeting configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24dab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24dab-104">

<span> </span></span></span>

<span data-ttu-id="24dab-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="24dab-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="24dab-106">Вы можете удалить сайт или конфигурацию пользователя.</span><span class="sxs-lookup"><span data-stu-id="24dab-106">You can delete a site or user configuration.</span></span> <span data-ttu-id="24dab-107">Невозможно удалить глобальную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="24dab-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="24dab-108">При удалении глобальной конфигурации она автоматически восстанавливает значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24dab-108">If you delete the global configuration, it is automatically reset to the default values.</span></span>

<div>

## <a name="to-delete-a-site-or-user-meeting-configuration"></a><span data-ttu-id="24dab-109">Удаление конфигурации сайта или собрания пользователя</span><span class="sxs-lookup"><span data-stu-id="24dab-109">To delete a site or user meeting configuration</span></span>

1.  <span data-ttu-id="24dab-110">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="24dab-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="24dab-111">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="24dab-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="24dab-112">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="24dab-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="24dab-113">На панели навигации слева выберите **Конференц** -связь, а затем — **Конфигурация собрания**.</span><span class="sxs-lookup"><span data-stu-id="24dab-113">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="24dab-114">В списке конфигураций собрания выберите конфигурацию сайта или пула, щелкните **Изменить**, а затем **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="24dab-114">In the list of meeting configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-meeting-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="24dab-115">Удаление параметров конфигурации собраний с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="24dab-115">Removing Meeting Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="24dab-116">Параметры собрания можно удалить с помощью Windows PowerShell и командлета Remove-CsMeetingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="24dab-116">Meeting settings can be deleted by using Windows PowerShell and the Remove-CsMeetingConfiguration cmdlet.</span></span> <span data-ttu-id="24dab-117">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="24dab-117">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="24dab-118">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="24dab-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-meeting-configuration-settings"></a><span data-ttu-id="24dab-119">Удаление заданной коллекции параметров конфигурации собрания</span><span class="sxs-lookup"><span data-stu-id="24dab-119">To remove a specified collection of meeting configuration settings</span></span>

  - <span data-ttu-id="24dab-120">Эта команда удаляет параметры конфигурации собрания, примененные к сайту Redmond.</span><span class="sxs-lookup"><span data-stu-id="24dab-120">This command removes the meeting configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsMeetingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="24dab-121">Удаление всех параметров конфигурации собрания, примененных к области сайта</span><span class="sxs-lookup"><span data-stu-id="24dab-121">To remove all the meeting configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="24dab-122">Эта команда удаляет все параметры конфигурации собрания, примененные к области сайта.</span><span class="sxs-lookup"><span data-stu-id="24dab-122">This command removes all the meeting configuration settings applied to the site scope:</span></span>
    
        Get-CsMeetingConfiguration -Filter "site:*" | Remove-CsMeetingConfiguration

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-that-admit-anonymous-users-by-default"></a><span data-ttu-id="24dab-123">Удаление всех параметров конфигурации собрания, которые по умолчанию применяют анонимные пользователи</span><span class="sxs-lookup"><span data-stu-id="24dab-123">To remove all the meeting configuration settings that admit anonymous users by default</span></span>

  - <span data-ttu-id="24dab-124">И этот параметр удаляет все параметры, которые позволяют принимать анонимные пользователи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24dab-124">And this one removes all the settings that allow anonymous users to be admitted by default:</span></span>
    
        Get-CsMeetingConfiguration | Where-Object {$_.AdmitAnonymousUsersByDefault -eq $True} | Remove-CsMeetingConfiguration

</div>

<span data-ttu-id="24dab-125">Дополнительные сведения можно найти в разделе справки по командлету [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="24dab-125">For more information, see the help topic for the [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="24dab-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24dab-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

