---
title: 'Lync Server 2013: Проверка серверных сертификатов Lync Server 2013'
description: 'Lync Server 2013: Проверьте серверные сертификаты Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check server certificates
ms:assetid: 7b0474e8-0efe-47f0-84eb-a1ba575dabfd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725210(v=OCS.15)
ms:contentKeyID: 63969620
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 641651cb425b4fe8bd820bcebfa277084233bb1d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435021"
---
# <a name="check-lync-server-2013-server-certificates"></a><span data-ttu-id="5b572-103">Проверка серверных сертификатов Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b572-103">Check Lync Server 2013 server certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b572-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b572-104">

<span> </span></span></span>

<span data-ttu-id="5b572-105">_**Тема последнего изменения:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="5b572-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b572-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="5b572-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5b572-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="5b572-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b572-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="5b572-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5b572-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b572-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b572-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="5b572-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5b572-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5b572-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5b572-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Get-CsCertificate.</span><span class="sxs-lookup"><span data-stu-id="5b572-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Get-CsCertificate cmdlet.</span></span> <span data-ttu-id="5b572-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5b572-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Get-CsCertificate&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5b572-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5b572-114">Description</span></span>

<span data-ttu-id="5b572-115">Командлет Get-CsCertificate позволяет получить сведения о каждом из сертификатов сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5b572-115">The Get-CsCertificate cmdlet enables you to retrieve information about each of your Lync Server certificates.</span></span> <span data-ttu-id="5b572-116">Это особенно важно, так как у сертификатов есть встроенная Дата окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="5b572-116">That’s especially important because certificates have a built-in expiration date.</span></span> <span data-ttu-id="5b572-117">Например, просроченные сертификаты, как правило, истекает через 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="5b572-117">For example,, privately-issued certificates typically expire after 12 months.</span></span> <span data-ttu-id="5b572-118">Если срок действия одного из сертификатов вашего сервера Lync Server истек, то все возможности будут потеряны до тех пор, пока сертификат не будет обновлен или заменен.</span><span class="sxs-lookup"><span data-stu-id="5b572-118">If any of your Lync Server certificates expire then you'll lose the accompanying functionality until that certificate is renewed or replaced.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5b572-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="5b572-119">Running the test</span></span>

<span data-ttu-id="5b572-120">Чтобы получить сведения о каждом из ваших сертификатов сервера Lync Server, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5b572-120">To return information about each of your Lync Server certificates just run the following command:</span></span>

`Get-CsCertificate`

<span data-ttu-id="5b572-121">Вы также можете отфильтровать сведения о сертификате возврата на основе даты окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="5b572-121">Or, you can filter the return certificate information based on expiration date.</span></span> <span data-ttu-id="5b572-122">Например, эта команда ограничивает возвращаемые данные сертификатами с истекшим сроком действия (не может использоваться после) июня 1, 2014:</span><span class="sxs-lookup"><span data-stu-id="5b572-122">For example, this command limits the returned data to certificates that expire (cannot be used after) June 1, 2014:</span></span>

`Get-CsCertificate | Where-Object {$_.NotAfter -lt "6/1/2014"}`

<span data-ttu-id="5b572-123">Дополнительные сведения можно найти в справочной документации по командлету Get-CsCertificate.</span><span class="sxs-lookup"><span data-stu-id="5b572-123">For more information, see the Help documentation for the Get-CsCertificate cmdlet.</span></span>

<span data-ttu-id="5b572-124">Обратите внимание, что несмотря на то, что существует командлет Test-CsCertificateConfiguration, он не очень полезен администраторам.</span><span class="sxs-lookup"><span data-stu-id="5b572-124">Note that, although the Test-CsCertificateConfiguration cmdlet exists, it is not very useful to administrators.</span></span> <span data-ttu-id="5b572-125">(Вместо этого этот командлет используется преимущественно мастером сертификатов.) Несмотря на то что командлет работает, возвращаемые им данные имеют минимальное значение, как показано в следующем примере вывода:</span><span class="sxs-lookup"><span data-stu-id="5b572-125">(Instead, that cmdlet is primarily used by the Certificate wizard.) Although the cmdlet works, the information that it returns is of minimal value as shown in the following output example:</span></span>

<span data-ttu-id="5b572-126">Использование отпечатка</span><span class="sxs-lookup"><span data-stu-id="5b572-126">Thumbprint Use</span></span>

<span data-ttu-id="5b572-127">\---------- ---</span><span class="sxs-lookup"><span data-stu-id="5b572-127">\---------- ---</span></span>

<span data-ttu-id="5b572-128">A9D51A2911C74FABFF7F2A8A994B20857D399107 по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5b572-128">A9D51A2911C74FABFF7F2A8A994B20857D399107 Default</span></span>

</div>

<div>

## <a name="reviewing-the-output"></a><span data-ttu-id="5b572-129">Просмотр результатов</span><span class="sxs-lookup"><span data-stu-id="5b572-129">Reviewing the output</span></span>

<span data-ttu-id="5b572-130">Командлет Get-CsCertificate возвращает сведения о каждом из сертификатов сервера Lync Server, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="5b572-130">The Get-CsCertificate cmdlet returns information similar to the following for each of your Lync Server certificates:</span></span>

<span data-ttu-id="5b572-131">Issuer: CN = FabrikamCA</span><span class="sxs-lookup"><span data-stu-id="5b572-131">Issuer : CN=FabrikamCA</span></span>

<span data-ttu-id="5b572-132">NotAfter: 12/28/2015 3:35:41 PM</span><span class="sxs-lookup"><span data-stu-id="5b572-132">NotAfter : 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="5b572-133">NotBefore: 1/2/2014 12:49:37 PM</span><span class="sxs-lookup"><span data-stu-id="5b572-133">NotBefore : 1/2/2014 12:49:37 PM</span></span>

<span data-ttu-id="5b572-134">SerialNumber: 611BB01200000000000C</span><span class="sxs-lookup"><span data-stu-id="5b572-134">SerialNumber : 611BB01200000000000C</span></span>

<span data-ttu-id="5b572-135">Тема: CN = LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="5b572-135">Subject : CN=LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="5b572-136">AlternativeNames: {sip.fabrikam.com, LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="5b572-136">AlternativeNames : {sip.fabrikam.com, LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="5b572-137">meet.fabrikam.com, admin.fabrikam.com...}</span><span class="sxs-lookup"><span data-stu-id="5b572-137">meet.fabrikam.com, admin.fabrikam.com...}</span></span>

<span data-ttu-id="5b572-138">Отпечаток: A9D51A2911C74FABFF7F2A8A994B20857D399107</span><span class="sxs-lookup"><span data-stu-id="5b572-138">Thumbprint : A9D51A2911C74FABFF7F2A8A994B20857D399107</span></span>

<span data-ttu-id="5b572-139">Использование: Default</span><span class="sxs-lookup"><span data-stu-id="5b572-139">Use : Default</span></span>

<span data-ttu-id="5b572-140">Как правило, основные проблемы, связанные с сертификатами Lync Server, включают в себя даты и время, например время вступления в силу сертификатов (NotBefore) или срок их действия (NotAfter).</span><span class="sxs-lookup"><span data-stu-id="5b572-140">As a rule, the top issues involving Lync Server certificates involve dates and times, such as when certificates take effect (NotBefore) or when they expire (NotAfter).</span></span> <span data-ttu-id="5b572-141">Поскольку эти значения даты и времени настолько важны, возможно, потребуется ограничить возвращаемые данные такими данными, как использование сертификата, серийный номер сертификата и Дата окончания срока действия сертификата; После этого вы сможете быстро просмотреть все сертификаты и срок их действия.</span><span class="sxs-lookup"><span data-stu-id="5b572-141">Because these dates and times are so important, you might want to limit the returned data to information such as the certificate use, the certificate serial number, and the certificate expiration date; then you can quickly review all the certificates and when they will expire.</span></span> <span data-ttu-id="5b572-142">Чтобы вернуть эти данные, используйте команду вместе с параметрами, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="5b572-142">To return just that information, use the command together with the options as shown:</span></span>

`Get-CsCertificate | Select-Object Use, SerialNumber, NotAfter | Sort-Object NotAfter`

<span data-ttu-id="5b572-143">Эта команда возвращает данные, похожие на приведенные ниже, при этом сертификаты сортируются в порядке их истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="5b572-143">That command returns data similar to the following, with the certificates sorted in order of their expiration date:</span></span>

<span data-ttu-id="5b572-144">Использование NotAfter SerialNumber</span><span class="sxs-lookup"><span data-stu-id="5b572-144">Use SerialNumber NotAfter</span></span>

<span data-ttu-id="5b572-145">\--- ------------ --------</span><span class="sxs-lookup"><span data-stu-id="5b572-145">\--- ------------ --------</span></span>

<span data-ttu-id="5b572-146">611BB01200000000000C по умолчанию 12/28/2015 3:35:41 PM</span><span class="sxs-lookup"><span data-stu-id="5b572-146">Default 611BB01200000000000C 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="5b572-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 PM</span><span class="sxs-lookup"><span data-stu-id="5b572-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 PM</span></span>

<span data-ttu-id="5b572-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 AM</span><span class="sxs-lookup"><span data-stu-id="5b572-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 AM</span></span>

<span data-ttu-id="5b572-149">Если у вас возникли проблемы с сертификатом, возможно, вы захотите просмотреть AlternativeNames, настроенный для сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b572-149">If you have certificate problems, you might want to review the AlternativeNames configured for a certificate.</span></span> <span data-ttu-id="5b572-150">На первый взгляд, это похоже на проблему.</span><span class="sxs-lookup"><span data-stu-id="5b572-150">At first glance, that seems to be a problem.</span></span> <span data-ttu-id="5b572-151">По умолчанию в зависимости от размера окна консоли Get-CsCertificate может не отображать все имена:</span><span class="sxs-lookup"><span data-stu-id="5b572-151">By default, and depending on the size of your console window, Get-CsCertificate might not be able to display all the names:</span></span>

<span data-ttu-id="5b572-152">AlternativeNames: {sip.fabrikam.com, LYNC.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="5b572-152">AlternativeNames : {sip.fabrikam.com, LYNC.fabrikam.com,</span></span>

<span data-ttu-id="5b572-153">meet.fabrikam.com, admin. Fabrika...}</span><span class="sxs-lookup"><span data-stu-id="5b572-153">meet.fabrikam.com, admin.fabrika...}</span></span>

<span data-ttu-id="5b572-154">Чтобы просмотреть все альтернативные имена, назначенные сертификату, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5b572-154">To see all the alternative names assigned to a certificate use a command similar to this one:</span></span>

`Get-CsCertificate | Where-Object {$_.SerialNumber -eq "611BB01200000000000C"} | Select-Object -ExpandProperty AlternativeNames`

<span data-ttu-id="5b572-155">Для отображения всех альтернативных имен в сертификате:</span><span class="sxs-lookup"><span data-stu-id="5b572-155">That should show you all of the alternative names on the certificate:</span></span>

<span data-ttu-id="5b572-156">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="5b572-156">sip.fabrikam.com</span></span>

<span data-ttu-id="5b572-157">LYNC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="5b572-157">LYNC.fabrikam.com</span></span>

<span data-ttu-id="5b572-158">meet.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="5b572-158">meet.fabrikam.com</span></span>

<span data-ttu-id="5b572-159">admin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="5b572-159">admin.fabrikam.com</span></span>

<span data-ttu-id="5b572-160">LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="5b572-160">LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="5b572-161">Dialin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="5b572-161">Dialin.fabrikam.com</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5b572-162">См. также</span><span class="sxs-lookup"><span data-stu-id="5b572-162">See Also</span></span>


[<span data-ttu-id="5b572-163">Get-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="5b572-163">Get-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCertificate)  
  

<span data-ttu-id="5b572-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b572-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

