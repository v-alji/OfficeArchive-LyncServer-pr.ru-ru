---
title: 'Lync Server 2013: Настройка служб федерации Active Directory (AD FS 2,0)'
description: 'Lync Server 2013: Настройка служб федерации Active Directory (AD FS 2,0).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Active Directory Federation Services (AD FS 2.0)
ms:assetid: 0ba8657f-55b8-41b3-960c-fdc5eeee6978
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308561(v=OCS.15)
ms:contentKeyID: 54973682
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bc21500273d8576f54f6110783e61764ec9723a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433404"
---
# <a name="configuring-active-directory-federation-services-ad-fs-20-for-lync-server-2013"></a><span data-ttu-id="d17e4-103">Настройка служб федерации Active Directory (AD FS 2,0) для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d17e4-103">Configuring Active Directory Federation Services (AD FS 2.0) for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d17e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d17e4-104">

<span> </span></span></span>

<span data-ttu-id="d17e4-105">_**Тема последнего изменения:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="d17e4-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="d17e4-106">В этом разделе рассматривается настройка служб федерации Active Directory (AD FS 2.0) для поддержки многофакторной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d17e4-106">The following section describes how to configure Active Directory Federation Services (AD FS 2.0) to support multi-factor authentication.</span></span> <span data-ttu-id="d17e4-107">Сведения о том, как установить AD FS 2,0, приведены пошаговые инструкции для AD FS 2,0 и инструкции по [https://go.microsoft.com/fwlink/p/?LinkId=313374](https://go.microsoft.com/fwlink/p/?linkid=313374) .</span><span class="sxs-lookup"><span data-stu-id="d17e4-107">For information on how to install AD FS 2.0, see AD FS 2.0 Step-by-Step and How To Guides at [https://go.microsoft.com/fwlink/p/?LinkId=313374](https://go.microsoft.com/fwlink/p/?linkid=313374).</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="d17e4-108">При установке AD FS 2.0 не добавляйте роль службы федерации Active Directory с помощью диспетчера серверов Windows.</span><span class="sxs-lookup"><span data-stu-id="d17e4-108">When installing AD FS 2.0, do not use the Windows Server Manager to add the Active Directory Federation Services role.</span></span> <span data-ttu-id="d17e4-109">Вместо этого загрузите и установите пакет служб федерации Active Directory 2,0 RTW at <A href="https://go.microsoft.com/fwlink/p/?linkid=313375">https://go.microsoft.com/fwlink/p/?LinkId=313375</A> .</span><span class="sxs-lookup"><span data-stu-id="d17e4-109">Instead, download and install the Active Directory Federation Services 2.0 RTW package at <A href="https://go.microsoft.com/fwlink/p/?linkid=313375">https://go.microsoft.com/fwlink/p/?LinkId=313375</A>.</span></span>



</div>

<div>


<span data-ttu-id="d17e4-110">**Настройка AD FS для двухфакторной проверки подлинности**</span><span class="sxs-lookup"><span data-stu-id="d17e4-110">**To configure AD FS for two-factor Authentication**</span></span>

1.  <span data-ttu-id="d17e4-111">Войдите в систему на компьютере с AD FS 2.0 с помощью учетной записи администратора домена.</span><span class="sxs-lookup"><span data-stu-id="d17e4-111">Log in to the AD FS 2.0 computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="d17e4-112">Запустите Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d17e4-112">Start Windows PowerShell.</span></span>

3.  <span data-ttu-id="d17e4-113">Введите в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d17e4-113">From the Windows PowerShell command-line, run the following command:</span></span>
    ```powershell
    add-pssnapin Microsoft.Adfs.PowerShell
    ```
4.  <span data-ttu-id="d17e4-114">Установите связь с каждым сервером Lync Server 2013 с накопительными обновлениями для Lync Server 2013: Июль 2013 режиссер, корпоративный пул и сервер Standard Edition, на котором будет включена пассивная проверка подлинности, заменив имя сервера, относящееся к развертыванию, выполните указанные ниже команды.</span><span class="sxs-lookup"><span data-stu-id="d17e4-114">Establish a partnership with each Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Director, Enterprise Pool, and Standard Edition server that will be enabled for passive authentication by running the following command, replacing the server name specific to your deployment:</span></span>
    ```powershell
    Add-ADFSRelyingPartyTrust -Name LyncPool01-PassiveAuth -MetadataURL https://lyncpool01.contoso.com/passiveauth/federationmetadata/2007-06/federationmetadata.xml
     ```
5.  <span data-ttu-id="d17e4-115">Запустите консоль управления AD FS 2.0 в меню "Средства администрирования".</span><span class="sxs-lookup"><span data-stu-id="d17e4-115">From the Administrative Tools menu, launch the AD FS 2.0 Management console.</span></span>

6.  <span data-ttu-id="d17e4-116">Разверните **Trust Relationships** элемент \> **доверия проверяющей стороны** отношений доверия.</span><span class="sxs-lookup"><span data-stu-id="d17e4-116">Expand **Trust Relationships** \> **Relying Party Trusts**.</span></span>

7.  <span data-ttu-id="d17e4-117">Убедитесь в том, что для Lync Server 2013 установлены новые доверительные отношения с накопительными обновлениями для Lync Server 2013: Июль 2013 корпоративным пулом или Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d17e4-117">Verify that a new trust has been created for your Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Enterprise Pool or Standard Edition server.</span></span>

8.  <span data-ttu-id="d17e4-118">С помощью Windows PowerShell и следующих команд создайте и назначьте для отношения доверия с проверяющей стороны правило утверждения авторизации:</span><span class="sxs-lookup"><span data-stu-id="d17e4-118">Create and assign an Issuance Authorization Rule for your relying party trust using Windows PowerShell by running the following commands:</span></span>
    
       ```powershell
        $IssuanceAuthorizationRules = '@RuleTemplate = "AllowAllAuthzRule" => issue(Type = "http://schemas.microsoft.com/authorization/claims/permit", Value = "true");'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName LyncPool01-PassiveAuth 
        -IssuanceAuthorizationRules $IssuanceAuthorizationRules
       ```

9.  <span data-ttu-id="d17e4-119">С помощью Windows PowerShell и следующих команд создайте и назначьте для отношения доверия с проверяющей стороны правило утверждения преобразования:</span><span class="sxs-lookup"><span data-stu-id="d17e4-119">Create and assign an Issuance Transform Rule for your relying party trust using Windows PowerShell by running the following commands:</span></span>
    
       ```powershell
        $IssuanceTransformRules = '@RuleTemplate = "PassThroughClaims" @RuleName = "Sid" c:[Type == "http://schemas.microsoft.com/ws/2008/06/identity/claims/primarysid"]=> issue(claim = c);'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName LyncPool01-PassiveAuth -IssuanceTransformRules $IssuanceTransformRules
       ```

10. <span data-ttu-id="d17e4-120">В консоли управления AD FS 2.0 щелкните отношение доверия с проверяющей стороной правой кнопкой мыши и выберите команду **редактирования правил утверждений**.</span><span class="sxs-lookup"><span data-stu-id="d17e4-120">From the AD FS 2.0 Management console, right click on your relying party trust and select **Edit Claim Rules**.</span></span>

11. <span data-ttu-id="d17e4-121">Перейдите на вкладку **правил разрешения выпуска** и убедитесь в том, что новое правило разрешения успешно создано.</span><span class="sxs-lookup"><span data-stu-id="d17e4-121">Select the **Issuance Authorization Rules** tab and verify that the new authorization rule was created successfully.</span></span>

12. <span data-ttu-id="d17e4-122">Перейдите на вкладку **правил преобразования выпуска** и убедитесь в том, что новое правило преобразования успешно создано.</span><span class="sxs-lookup"><span data-stu-id="d17e4-122">Select the **Issuance Transform Rules** tab and verify that the new transform rule was created successfully.</span></span>

<span data-ttu-id="d17e4-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d17e4-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

