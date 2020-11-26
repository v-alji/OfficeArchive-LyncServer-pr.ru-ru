---
title: 'Lync Server 2013: отчет о назначениях для учетной записи Kerberos'
description: 'Lync Server 2013: отчет о назначениях учетных записей Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Report Kerberos account assignments
ms:assetid: 523231f6-81b3-454b-996d-663d9bd5cf83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398343(v=OCS.15)
ms:contentKeyID: 48184151
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23e40dddfc4538db70e2101b1bfcbbce2fe3fa8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442742"
---
# <a name="report-kerberos-account-assignments-in-lync-server-2013"></a><span data-ttu-id="bf274-103">Отчет о назначениях для учетной записи Kerberos в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf274-103">Report Kerberos account assignments in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf274-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf274-104">

<span> </span></span></span>

<span data-ttu-id="bf274-105">_**Тема последнего изменения:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="bf274-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="bf274-106">Для успешного выполнения этой процедуры необходимо войти в систему в качестве пользователя, который является членом группы RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="bf274-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="bf274-107">Вы можете использовать командлет **Get-CsKerberosAccountAssignment** , чтобы запросить сведения о назначениях учетных записей проверки подлинности Kerberos и сообщить о текущих заданиях в развертывании.</span><span class="sxs-lookup"><span data-stu-id="bf274-107">You can use the **Get-CsKerberosAccountAssignment** cmdlet to query information about the Kerberos authentication account assignments and report information about the current assignments in your deployment.</span></span>

<div>

## <a name="to-query-kerberos-authentication-account-assignments-for-a-site"></a><span data-ttu-id="bf274-108">Запрос назначений учетной записи для проверки подлинности Kerberos для сайта</span><span class="sxs-lookup"><span data-stu-id="bf274-108">To query Kerberos authentication account assignments for a site</span></span>

1.  <span data-ttu-id="bf274-109">Войдя в группу RTCUniversalServerAdmins, войдите в домен на компьютере с Lync Server 2013 или на компьютер, на котором установлены средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="bf274-109">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="bf274-110">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="bf274-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="bf274-111">В командной строке выполните одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="bf274-111">From the command line, run one of the following commands:</span></span>
    
      - <span data-ttu-id="bf274-112">Чтобы запросить все назначения учетной записи для проверки подлинности Kerberos в Организации и вернуть сведения о назначениях для каждого из них, запустите командлет без параметров.</span><span class="sxs-lookup"><span data-stu-id="bf274-112">To query all Kerberos authentication account assignments in your organization and return assignment information about each of them, run the cmdlet without any parameters:</span></span>
        
            Get-CsKerberosAccountAssignment
    
      - <span data-ttu-id="bf274-113">Чтобы запросить все назначения учетной записи для проверки подлинности Kerberos в развертывании и вернуть сведения о назначениях сайтов для каждого из них, выполните командлет с параметром Identity.</span><span class="sxs-lookup"><span data-stu-id="bf274-113">To query all Kerberos authentication account assignments in your deployment and return site assignment information about each of them, run the cmdlet with the Identity parameter:</span></span>
        
            Get-CsKerberosAccountAssignment -Identity "site:SiteName"
        
        <span data-ttu-id="bf274-114">Например:</span><span class="sxs-lookup"><span data-stu-id="bf274-114">For example:</span></span>
        
            Get-CsKerberosAccountAssignment -Identity "site:Redmond"
    
      - <span data-ttu-id="bf274-115">Чтобы запросить все назначения учетной записи проверки подлинности Kerberos на одном сайте и вернуть сведения о назначениях для каждого из них, запустите командлет с параметром Filter.</span><span class="sxs-lookup"><span data-stu-id="bf274-115">To query all Kerberos authentication account assignments in a single site and return assignment information about each of them, run the cmdlet with the Filter parameter:</span></span>
        
            Get-CsKerberosAccountAssignment -Filter "SiteName"
        
        <span data-ttu-id="bf274-116">Например:</span><span class="sxs-lookup"><span data-stu-id="bf274-116">For example:</span></span>
        
            Get-CsKerberosAccountAssignment -Filter "*Redmond"
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="bf274-117">Указание \* SiteName для параметра Filter возвращает сведения обо всех сайтах, которые содержат указанное имя сайта в любом месте идентификатора сайта (например, все сайты, содержащие строку Redmond в идентификаторе сайта).</span><span class="sxs-lookup"><span data-stu-id="bf274-117">Specifying \*SiteName for the Filter parameter returns information about all sites that contain the specified site name anywhere in the site identifier (for example, all sites that contain the string Redmond in the site identifier).</span></span>

        
        <span data-ttu-id="bf274-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf274-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

