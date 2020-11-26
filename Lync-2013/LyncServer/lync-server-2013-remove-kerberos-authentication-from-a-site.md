---
title: 'Lync Server 2013: удаление проверки подлинности Kerberos для сайта'
description: 'Lync Server 2013: Удаление проверки подлинности Kerberos с сайта.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Kerberos authentication from a site
ms:assetid: 93171b02-bb36-42dc-943d-86d9dde45b59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398749(v=OCS.15)
ms:contentKeyID: 48184806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a3d9100d07d37e98800cfce106bc75fcfaeaa59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436386"
---
# <a name="in-lync-server-2013-remove-kerberos-authentication-from-a-site"></a><span data-ttu-id="f3efe-103">В Lync Server 2013 удаление проверки подлинности Kerberos для сайта</span><span class="sxs-lookup"><span data-stu-id="f3efe-103">In Lync Server 2013 remove Kerberos authentication from a site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3efe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3efe-104">

<span> </span></span></span>

<span data-ttu-id="f3efe-105">_**Тема последнего изменения:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="f3efe-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="f3efe-106">Для успешного выполнения этой процедуры необходимо войти в систему в качестве пользователя, который является членом группы RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f3efe-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="f3efe-107">Если необходимо удалить проверку подлинности Kerberos с сайта или снять с учета сайта, необходимо удалить назначение учетной записи для проверки подлинности Kerberos с сайта с помощью командлета **Remove-CsKerberosAccountAssignment** .</span><span class="sxs-lookup"><span data-stu-id="f3efe-107">If you need to remove Kerberos authentication from a site or retire a site, you must remove the Kerberos authentication account assignment from the site by using the **Remove-CsKerberosAccountAssignment** cmdlet.</span></span> <span data-ttu-id="f3efe-108">Выполните описанные ниже действия, чтобы удалить назначение учетной записи проверки подлинности Kerberos, удаляя назначение со всех компьютеров сайта.</span><span class="sxs-lookup"><span data-stu-id="f3efe-108">Use the following procedure to remove the Kerberos authentication account assignment, which removes the assignment from all computers in the site.</span></span>

<div class=" ">


> [!WARNING]  
> <span data-ttu-id="f3efe-109">Если вы безвозвратно удаляете учетную запись с поддержкой Kerberos, вы должны использовать оснастку "пользователи и компьютеры Active Directory", чтобы удалить ее из доменных служб Active Directory после удаления задания.</span><span class="sxs-lookup"><span data-stu-id="f3efe-109">If you are permanently retiring the Kerberos-enabled account, you should use Active Directory Users and Computers to delete it from Active Directory Domain Services after you have removed the assignment.</span></span> <span data-ttu-id="f3efe-110">Если вы планируете использовать объект в будущем, вам может понадобиться сохранить объект Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3efe-110">If you plan to use the object in the future, you might want to keep the Active Directory object.</span></span>



</div>

<div>

## <a name="to-remove-kerberos-authentication-from-a-site"></a><span data-ttu-id="f3efe-111">Удаление проверки подлинности Kerberos с сайта</span><span class="sxs-lookup"><span data-stu-id="f3efe-111">To remove Kerberos authentication from a site</span></span>

1.  <span data-ttu-id="f3efe-112">Войдя в группу RTCUniversalServerAdmins, войдите в домен на компьютере с Lync Server 2013 или на компьютер, на котором установлены средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="f3efe-112">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="f3efe-113">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f3efe-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f3efe-114">В командной строке выполните следующие две команды:</span><span class="sxs-lookup"><span data-stu-id="f3efe-114">From the command line, run the following two commands:</span></span>
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:SiteName"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    <span data-ttu-id="f3efe-115">Например:</span><span class="sxs-lookup"><span data-stu-id="f3efe-115">For example:</span></span>
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:Redmond"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f3efe-116">После внесения изменений в проверку подлинности Kerberos (например, для добавления учетной записи или удаления учетной записи) необходимо запустить команду <STRONG>Enable-CsTopology</STRONG> в командной строке оболочки Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="f3efe-116">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="f3efe-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3efe-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

