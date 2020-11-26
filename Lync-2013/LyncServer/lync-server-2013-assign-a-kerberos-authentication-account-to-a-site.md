---
title: 'Lync Server 2013: назначение учетной записи проверки подлинности Kerberos для сайта'
description: 'Lync Server 2013: назначьте сайту учетную запись для проверки подлинности Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a Kerberos authentication account to a site
ms:assetid: 3d9c587c-c8b8-4f81-8ed9-1458a31fc292
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425901(v=OCS.15)
ms:contentKeyID: 48183929
ms.date: 04/18/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: edcd80ef3ae15ae91dfab73ee8789054d897fe5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439844"
---
# <a name="assign-a-kerberos-authentication-account-to-a-site-in-lync-server-2013"></a><span data-ttu-id="7cae7-103">Назначение учетной записи проверки подлинности Kerberos для сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cae7-103">Assign a Kerberos authentication account to a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7cae7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7cae7-104">

<span> </span></span></span>

<span data-ttu-id="7cae7-105">_**Тема последнего изменения:** 2017-04-18_</span><span class="sxs-lookup"><span data-stu-id="7cae7-105">_**Topic Last Modified:** 2017-04-18_</span></span>

<span data-ttu-id="7cae7-106">Для успешного выполнения этой процедуры необходимо войти в систему в качестве пользователя, который является членом группы RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="7cae7-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="7cae7-107">После создания учетной записи Kerberos ее необходимо назначить сайту.</span><span class="sxs-lookup"><span data-stu-id="7cae7-107">After creating the Kerberos account, you must assign it to a site.</span></span> <span data-ttu-id="7cae7-108">Это сайт Lync Server 2013, а не сайт Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7cae7-108">This is a Lync Server 2013 site, not an Active Directory site.</span></span> <span data-ttu-id="7cae7-109">Вы можете создать несколько учетных записей проверки подлинности Kerberos для каждого развертывания, но вы можете назначить сайту только одну учетную запись.</span><span class="sxs-lookup"><span data-stu-id="7cae7-109">You can create multiple Kerberos authentication accounts per deployment, but you can assign only one account to a site.</span></span> <span data-ttu-id="7cae7-110">Чтобы назначить сайту ранее созданную учетную запись для проверки подлинности Kerberos, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7cae7-110">Use the following procedure to assign a previously created Kerberos authentication account to a site.</span></span> <span data-ttu-id="7cae7-111">Подробнее о том, как создать учетную запись Kerberos, можно найти [в разделе Создание учетной записи проверки подлинности Kerberos в Lync Server 2013](lync-server-2013-create-a-kerberos-authentication-account.md).</span><span class="sxs-lookup"><span data-stu-id="7cae7-111">For details about creating the Kerberos account, see [Create a Kerberos authentication account in Lync Server 2013](lync-server-2013-create-a-kerberos-authentication-account.md).</span></span>

<div>

## <a name="to-assign-a-kerberos-authentication-account-to-a-site"></a><span data-ttu-id="7cae7-112">Назначение учетной записи проверки подлинности Kerberos сайту</span><span class="sxs-lookup"><span data-stu-id="7cae7-112">To assign a Kerberos authentication account to a site</span></span>

1.  <span data-ttu-id="7cae7-113">Войдя в группу RTCUniversalServerAdmins, войдите в домен на компьютере с Lync Server 2013 или на компьютер, на котором установлены средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="7cae7-113">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="7cae7-114">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="7cae7-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7cae7-115">В командной строке выполните следующие две команды:</span><span class="sxs-lookup"><span data-stu-id="7cae7-115">From the command line, run the following two commands:</span></span>
    
       ```powershell
        New-CsKerberosAccountAssignment -UserAccount "Domain\UserAccount"
                  -Identity "site:SiteName"
       ```          
    
       ```powershell
        Enable-CsTopology
       ```
    
    <span data-ttu-id="7cae7-116">Например:</span><span class="sxs-lookup"><span data-stu-id="7cae7-116">For example:</span></span>
    
       ```powershell
        New-CsKerberosAccountAssignment -UserAccount "contoso\kerbauth"
                  -Identity "site:redmond"
       ```
    
       ```powershell
        Enable-CsTopology
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="7cae7-117">Параметр UserAccount необходимо указать с помощью формата домен \ пользователь.</span><span class="sxs-lookup"><span data-stu-id="7cae7-117">You must specify the UserAccount parameter by using the Domain\User format.</span></span> <span data-ttu-id="7cae7-118">Формат User@Domain. расширение не поддерживается для ссылок на объекты компьютера, созданные для проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="7cae7-118">The User@Domain.extension format is not supported for referring to the computer objects created for Kerberos authentication purposes.</span></span>

    
    </div>

4.  <span data-ttu-id="7cae7-119">**Необязательно**: возможно, вы настроили для своих веб-служб полное доменное имя (FQDN), как и в случае [изменения URL — в Lync Server 2013](lync-server-2013-change-the-web-services-url.md).</span><span class="sxs-lookup"><span data-stu-id="7cae7-119">**OPTIONAL**: You may have configured an override FQDN (fully qualified domain name) for your WebServices, as per [Change the Web Services URL in Lync Server 2013](lync-server-2013-change-the-web-services-url.md).</span></span> <span data-ttu-id="7cae7-120">В этом случае вам потребуется также добавить SPN для этого полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="7cae7-120">If that's the case, you'll need to add a SPN for this FQDN as well.</span></span> <span data-ttu-id="7cae7-121">Например, если полное доменное имя — WebService. contoso. local, вы можете выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7cae7-121">For example, if the FQDN was webservices.contoso.local, you would run:</span></span>
    
    ```console
    setspn -S http/webservices.contoso.local kerbauth
    ```
5.     
    <div class="">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7cae7-122">После внесения изменений в проверку подлинности Kerberos (например, для добавления учетной записи или удаления учетной записи) необходимо запустить команду <STRONG>Enable-CsTopology</STRONG> в командной строке оболочки Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="7cae7-122">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="7cae7-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7cae7-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

