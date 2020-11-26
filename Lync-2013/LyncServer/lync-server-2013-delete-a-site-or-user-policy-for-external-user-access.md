---
title: 'Lync Server 2013: удаление сайта или пользовательской политики для доступа внешних пользователей'
description: 'Lync Server 2013: Удаление политики сайта или пользователя для доступа внешних пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a site or user policy for external user access
ms:assetid: 6d907507-825b-4354-9c03-337a459f72de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521013(v=OCS.15)
ms:contentKeyID: 48184455
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6aac81e7b50603e5eb80cde8877cdc06f138d872
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430674"
---
# <a name="delete-a-site-or-user-policy-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="b8ddd-103">Удаление сайта или пользовательской политики для доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8ddd-103">Delete a site or user policy for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8ddd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8ddd-104">

<span> </span></span></span>

<span data-ttu-id="b8ddd-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="b8ddd-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="b8ddd-106">Вы можете удалить политику сайта или пользователя, указанную на панели управления Lync Server на странице " **политика внешней доступа** ".</span><span class="sxs-lookup"><span data-stu-id="b8ddd-106">You can delete any site or user policy that is listed in Lync Server Control Panel on the **External Access Policy** page.</span></span> <span data-ttu-id="b8ddd-107">При удалении глобальной политики фактически она не удаляется, но только восстанавливает параметры, заданные по умолчанию, которые не включают поддержку каких – либо параметров доступа внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-107">Deleting the global policy does not actually delete it, but only resets it to the default settings, which do not include support for any external user access options.</span></span> <span data-ttu-id="b8ddd-108">Дополнительные сведения о сбросе глобальной политики можно найти [в разделе Восстановление глобальной политики доступа внешних пользователей в Lync Server 2013](lync-server-2013-reset-the-global-policy-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="b8ddd-108">For details about resetting the global policy, see [Reset the global policy for external user access in Lync Server 2013](lync-server-2013-reset-the-global-policy-for-external-user-access.md).</span></span>

<div>

## <a name="to-delete-a-site-or-user-policy-for-external-user-access"></a><span data-ttu-id="b8ddd-109">Удаление политики сайта или пользователя для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="b8ddd-109">To delete a site or user policy for external user access</span></span>

1.  <span data-ttu-id="b8ddd-110">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b8ddd-111">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b8ddd-112">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b8ddd-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b8ddd-113">Выберите **внешний доступ пользователей** и нажмите кнопку **Политика внешних доступа**.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-113">Click **External User Access**, click **External Access Policy**.</span></span>

4.  <span data-ttu-id="b8ddd-114">На вкладке **внешняя политика доступа** выберите сайт или политику пользователей, которые вы хотите удалить, и нажмите кнопку **изменить**, а затем — **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-114">On the **External Access Policy** tab, click the site or user policy you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="b8ddd-115">Когда появится запрос на подтверждение удаления, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-115">When prompted to confirm the deletion, click **OK**.</span></span>

</div>

<div>

## <a name="removing-pin-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="b8ddd-116">Удаление политик закрепления с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8ddd-116">Removing PIN Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="b8ddd-117">Внешние политики доступа можно удалить с помощью Windows PowerShell и командлета Remove-CsExternalAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-117">External access policies can be deleted by using Windows PowerShell and the Remove-CsExternalAccessPolicy cmdlet.</span></span> <span data-ttu-id="b8ddd-118">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="b8ddd-119">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="b8ddd-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-external-access-policy"></a><span data-ttu-id="b8ddd-120">Удаление особой политики внешнего доступа</span><span class="sxs-lookup"><span data-stu-id="b8ddd-120">To remove a specific external access policy</span></span>

  - <span data-ttu-id="b8ddd-121">Эта команда удаляет политику внешней политики доступа, примененную к сайту Redmond.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-121">This command removes the external access policy applied to the Redmond site:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-external-access-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="b8ddd-122">Чтобы удалить все внешние политики доступа, примененные к области "на пользователя"</span><span class="sxs-lookup"><span data-stu-id="b8ddd-122">To remove all the external access policies applied to the per-user scope</span></span>

  - <span data-ttu-id="b8ddd-123">Эта команда удаляет все политики внешней доступа, настроенные для области "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="b8ddd-123">This command removes all the external access policies configured at the per-user scope:</span></span>
    
        Get-CsExternalAccessPolicy -Filter "tag:*" | Remove-CsExternalAccessPolicy

</div>

<div>

## <a name="to-remove-all-the-external-access-policies-where-outside-user-access-is-disabled"></a><span data-ttu-id="b8ddd-124">Удаление всех внешних политик доступа, для которых отключен доступ за пределами пользователей</span><span class="sxs-lookup"><span data-stu-id="b8ddd-124">To remove all the external access policies where outside user access is disabled</span></span>

  - <span data-ttu-id="b8ddd-125">Эта команда удаляет все внешние политики доступа, в которых отключен доступ за пределы пользователей.</span><span class="sxs-lookup"><span data-stu-id="b8ddd-125">This command deletes all the external access policies where outside user access has been disabled:</span></span>
    
        Get-CsExternalAccessPolicy | Where-Object {$_.EnableOutsideAccess -eq $False} | Remove-CsExternalAccessPolicy

</div>

<span data-ttu-id="b8ddd-126">Дополнительные сведения можно найти в разделе справки по командлету [Remove-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy) .</span><span class="sxs-lookup"><span data-stu-id="b8ddd-126">For more information, see the help topic for the [Remove-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy) cmdlet.</span></span>

<span data-ttu-id="b8ddd-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8ddd-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

