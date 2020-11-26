---
title: 'Lync Server 2013: Удаление политики архивации'
description: 'Lync Server 2013: Удаление политики архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving policy
ms:assetid: 4739a691-41cc-4128-8bb8-6d5a4c02107a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520989(v=OCS.15)
ms:contentKeyID: 48184043
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ecf465a62cf8f54777b03a1634d9a95f1b565c9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430366"
---
# <a name="deleting-an-archiving-policy-in-lync-server-2013"></a><span data-ttu-id="a771c-103">Удаление политики архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a771c-103">Deleting an Archiving policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a771c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a771c-104">

<span> </span></span></span>

<span data-ttu-id="a771c-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="a771c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="a771c-106">Вы можете удалить политику пользователей или политику сайта.</span><span class="sxs-lookup"><span data-stu-id="a771c-106">You can delete a user policy or site policy.</span></span> <span data-ttu-id="a771c-107">Невозможно удалить глобальную политику.</span><span class="sxs-lookup"><span data-stu-id="a771c-107">The global policy cannot be removed.</span></span> <span data-ttu-id="a771c-108">Если вы попытаетесь удалить глобальную политику, Lync Server 2013 автоматически восстанавливает значения по умолчанию для этой политики.</span><span class="sxs-lookup"><span data-stu-id="a771c-108">If you try to delete the global policy, Lync Server 2013 automatically resets the policy to the default values.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a771c-109">Если вы включили интеграцию Microsoft Exchange для развертывания, политики Exchange определяют, включено ли архивирование для пользователей, использующих Exchange 2013, и почтовые ящики помещаются на In-Place удержание.</span><span class="sxs-lookup"><span data-stu-id="a771c-109">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="a771c-110">Подробности можно найти в разделе <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Настройка политик архивации в Lync server 2013 при использовании интеграции с Exchange Server</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="a771c-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-delete-a-user-or-site-policy-for-archiving"></a><span data-ttu-id="a771c-111">Удаление политики пользователя или сайта для архивации</span><span class="sxs-lookup"><span data-stu-id="a771c-111">To delete a user or site policy for archiving</span></span>

1.  <span data-ttu-id="a771c-112">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="a771c-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a771c-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a771c-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a771c-114">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a771c-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a771c-115">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Политика архивации**.</span><span class="sxs-lookup"><span data-stu-id="a771c-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="a771c-116">В списке политик архивации щелкните политику пользователей или сайта, которую следует удалить, щелкните **Изменить**, затем **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a771c-116">In the list of archiving policies, click the user or site policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="a771c-117">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="a771c-117">Click **Commit**.</span></span>

</div>

<div>

## <a name="removing-archiving-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a771c-118">Удаление политик архивации с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a771c-118">Removing Archiving Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="a771c-119">Политики архивации можно удалить с помощью Windows PowerShell и командлета **Remove-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="a771c-119">Archiving policies can be deleted by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="a771c-120">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a771c-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a771c-121">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="a771c-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-archiving-policy"></a><span data-ttu-id="a771c-122">Удаление указанной политики архивации</span><span class="sxs-lookup"><span data-stu-id="a771c-122">To remove a specified archiving policy</span></span>

  - <span data-ttu-id="a771c-123">Например, **Remove-CsArchivingPolicy** удаляет политику с сайтом удостоверений: Redmond.</span><span class="sxs-lookup"><span data-stu-id="a771c-123">As an example, **Remove-CsArchivingPolicy** deletes the policy with the Identity site:Redmond.</span></span> <span data-ttu-id="a771c-124">Обратите внимание на то, что при удалении политики сайта Политика сайта автоматически управляется пользователями, которые раньше настроили политикой для архивации.</span><span class="sxs-lookup"><span data-stu-id="a771c-124">Note that, when a policy configured at the site scope is deleted, users previously managed by the site policy will automatically be governed by the global archiving policy instead.</span></span> <span data-ttu-id="a771c-125">Следующая команда удаляет архивирование, примененное к сайту Redmond.</span><span class="sxs-lookup"><span data-stu-id="a771c-125">The following command removes the archiving applied to the Redmond site:</span></span>
    
        Remove-CsArchivingPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="a771c-126">Удаление всех политик архивации, примененных к области "на пользователя"</span><span class="sxs-lookup"><span data-stu-id="a771c-126">To remove all the archiving policies applied to the per-user scope</span></span>

  - <span data-ttu-id="a771c-127">Эта команда удаляет все политики архивации, примененные к области "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="a771c-127">This command removes all the archiving policies applied to the per-user scope:</span></span>
    
        Get-CsArchivingPolicy -Filter "tag:*" | Remove-CsArchivingPolicy

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-that-disable-internal-archiving"></a><span data-ttu-id="a771c-128">Удаление всех политик архивации, исключающих внутреннее архивирование</span><span class="sxs-lookup"><span data-stu-id="a771c-128">To remove all the archiving policies that disable internal archiving</span></span>

  - <span data-ttu-id="a771c-129">Данная команда удаляет все политики архивации, в которых отключена внутренняя архивация:</span><span class="sxs-lookup"><span data-stu-id="a771c-129">This command removes all the archiving policies where internal archiving has been disabled:</span></span>
    
        Get-CsArchivingPolicy | Where-Object {$_.ArchiveInternal -eq $False} | Remove-CsArchivingPolicy

</div>

<span data-ttu-id="a771c-130">Дополнительные сведения можно найти в разделе справки по командлету [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="a771c-130">For more information, see the help topic for the [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a771c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a771c-131">See Also</span></span>


[<span data-ttu-id="a771c-132">Управление архивированием внутренней и внешней связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a771c-132">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="a771c-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a771c-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

