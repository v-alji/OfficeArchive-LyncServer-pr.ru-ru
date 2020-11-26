---
title: 'Lync Server 2013: удаление существующих параметров конфигурации регистратора'
description: 'Lync Server 2013: удаление существующих параметров конфигурации регистратора.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete existing Registrar configuration settings
ms:assetid: ae43cd75-cae4-4f78-b037-779a2cdb583b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182571(v=OCS.15)
ms:contentKeyID: 48185132
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b625b97724edf0ecf8928ec31d89a6166230c4c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430457"
---
# <a name="delete-existing-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="6232f-103">Удаление существующих параметров конфигурации регистратора в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6232f-103">Delete existing Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6232f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6232f-104">

<span> </span></span></span>

<span data-ttu-id="6232f-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="6232f-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="6232f-106">Выполните указанные ниже действия, чтобы удалить регистратора.</span><span class="sxs-lookup"><span data-stu-id="6232f-106">Follow these steps to delete a Registrar.</span></span>

<div>

## <a name="to-delete-registrar-configuration-settings"></a><span data-ttu-id="6232f-107">Удаление параметров конфигурации регистратора</span><span class="sxs-lookup"><span data-stu-id="6232f-107">To delete Registrar configuration settings</span></span>

1.  <span data-ttu-id="6232f-108">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6232f-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="6232f-109">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6232f-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6232f-110">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6232f-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6232f-111">В левой области навигации щелкните **Безопасность**, затем **Регистратор**.</span><span class="sxs-lookup"><span data-stu-id="6232f-111">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="6232f-112">На странице **Регистратор** полностью или частично введите в поле поиска имя регистратора, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="6232f-112">On the **Registrar** page, and in the search field, type all or part of the name of the Registrar you want to delete.</span></span>

5.  <span data-ttu-id="6232f-113">Выберите в списке требуемый регистратор, затем щелкните **Изменить** и **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="6232f-113">In the list, click the Registrar that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="6232f-114">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6232f-114">Click **OK**.</span></span>

</div>

<div>

## <a name="removing-registrar-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="6232f-115">Удаление параметров конфигурации регистратора с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6232f-115">Removing Registrar Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="6232f-116">Вы можете удалить параметры конфигурации регистратора с помощью Windows PowerShell и командлета **Remove-CsProxyConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="6232f-116">You can delete the Registrar configuration settings by using Windows PowerShell and the **Remove-CsProxyConfiguration** cmdlet.</span></span> <span data-ttu-id="6232f-117">Этот командлет можно выполнить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6232f-117">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="6232f-118">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="6232f-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-set-of-registrar-security-settings"></a><span data-ttu-id="6232f-119">Удаление определенного набора параметров безопасности Регистратора</span><span class="sxs-lookup"><span data-stu-id="6232f-119">To remove a specific set of Registrar security settings</span></span>

  - <span data-ttu-id="6232f-120">Следующая команда удаляет параметры безопасности Регистратора, применяемые к пограничному серверу atl-edge-011.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="6232f-120">The following command removes the Registrar security settings applied to the edge Server atl-edge-011.litwareinc.com:</span></span>
    
        Remove-CsProxyConfiguration -Identity service:EdgeServer:atl-edge-011.litwareinc.com

</div>

<div>

## <a name="to-remove-all-of-the-registrar-security-settings-applied-to-the-site-scope"></a><span data-ttu-id="6232f-121">Удаление всех параметров безопасности Регистратора, применяемых на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="6232f-121">To remove all of the Registrar security settings applied to the site scope</span></span>

  - <span data-ttu-id="6232f-122">Следующая команда удаляет все параметры безопасности Регистратора, применяемые к службе Регистратора.</span><span class="sxs-lookup"><span data-stu-id="6232f-122">The following command removes all the Registrar security settings applied to the Registrar service:</span></span>
    
        Get-CsProxyConfiguration -Filter "service:Registrar:*" | Remove-CsProxyConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-registrar-security-settings-that-allow-ntlm-authentication"></a><span data-ttu-id="6232f-123">Удаление всех параметров безопасности Регистратора, разрешающих проверку подлинности NTLM</span><span class="sxs-lookup"><span data-stu-id="6232f-123">To remove all of the Registrar security settings that allow NTLM authentication</span></span>

  - <span data-ttu-id="6232f-124">Следующая команда удаляет все параметры безопасности Регистратора, разрешающие использование NTLM для проверки подлинности клиентов.</span><span class="sxs-lookup"><span data-stu-id="6232f-124">The following command deletes all the Registrar security settings that allow the use of NTLM for client authentication:</span></span>
    
        Get-CsProxyConfiguration | Where-Object {$_.UseNtlmForClientToProxyAuth -eq $True}| Remove-CsProxyConfiguration

</div>

<span data-ttu-id="6232f-125">Подробности можно найти в разделе [Remove-CsProxyConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsProxyConfiguration).</span><span class="sxs-lookup"><span data-stu-id="6232f-125">For details, see [Remove-CsProxyConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsProxyConfiguration).</span></span>

<span data-ttu-id="6232f-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6232f-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

