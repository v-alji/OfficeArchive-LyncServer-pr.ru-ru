---
title: 'Lync Server 2013: требования DNS для простых URL-адресов'
description: 'Lync Server 2013: требования DNS для простых URL-адресов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for simple URLs
ms:assetid: 3a3c9b22-892f-45a7-b05c-539d358a1a86
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425874(v=OCS.15)
ms:contentKeyID: 48183912
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 84cc893fc06e9c57dcad6506d692b4484827b56a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437761"
---
# <a name="dns-requirements-for-simple-urls-in-lync-server-2013"></a><span data-ttu-id="18da4-103">Требования DNS для простых URL-адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="18da4-103">DNS requirements for simple URLs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18da4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18da4-104">

<span> </span></span></span>

<span data-ttu-id="18da4-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="18da4-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="18da4-106">Lync Server 2013 поддерживает простые URL-адреса, благодаря которым пользователи могут легко присоединиться к собраниям, а затем упростить работу с администрированием Lync Server для администраторов.</span><span class="sxs-lookup"><span data-stu-id="18da4-106">Lync Server 2013 supports simple URLs, which make joining meetings easier for your users, and make getting to Lync Server administrative tools easier for your administrators.</span></span> <span data-ttu-id="18da4-107">Подробнее об использовании простых URL-адресов можно найти [в разделе Планирование простых URL-адресов в Lync Server 2013](lync-server-2013-planning-for-simple-urls.md).</span><span class="sxs-lookup"><span data-stu-id="18da4-107">For details about simple URLs, see [Planning for simple URLs in Lync Server 2013](lync-server-2013-planning-for-simple-urls.md).</span></span>

<span data-ttu-id="18da4-108">Lync Server поддерживает три простых URL-адреса: "Встреча", "Входящие звонки" и "Администратор". Вам необходимо настроить простые URL-адреса для "Встреча" и "Входящие звонки", а простой URL-адрес администратора — необязательный.</span><span class="sxs-lookup"><span data-stu-id="18da4-108">Lync Server supports the following three simple URLs: Meet, Dial-In, and Admin. You are required to set up simple URLs for Meet and Dial-In, and the Admin simple URL is optional.</span></span> <span data-ttu-id="18da4-109">DNS-записи, необходимые для поддержки простых URL-адресов, зависят от того, как вы определили эти простые URL-адреса, и нужно ли поддерживать аварийное восстановление для простых URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="18da4-109">The Domain Name System (DNS) records that you need to support simple URLs depend on how you have defined these simple URLs, and whether you want to support disaster recovery for Simple URLs.</span></span>

<div>

## <a name="simple-url-option-1"></a><span data-ttu-id="18da4-110">Простой URL-адрес (вариант 1)</span><span class="sxs-lookup"><span data-stu-id="18da4-110">Simple URL Option 1</span></span>

<span data-ttu-id="18da4-111">В варианте 1 вы создаете базовый URL-адрес для каждого простого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="18da4-111">In Option 1, you create a new base URL for each simple URL.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="18da4-112">Когда пользователь щелкает простую ссылку для собрания по URL-адресу, сервер, к которому разрешается запись DNS, определяет корректное клиентское программное обеспечение для запуска.</span><span class="sxs-lookup"><span data-stu-id="18da4-112">When a user clicks a simple URL meeting link, the server that the DNS A record resolves to determines the correct client software to start.</span></span> <span data-ttu-id="18da4-113">После запуска клиентское программное обеспечение автоматически связывается с пулом, на котором размещена конференция.</span><span class="sxs-lookup"><span data-stu-id="18da4-113">After the client software is started, it automatically communicates with the pool where the conference is hosted.</span></span> <span data-ttu-id="18da4-114">Таким образом, пользователи направляются на соответствующий сервер для содержимого собраний независимо от того, на каком сервере или в каком пуле вы хотите разрешить записи DNS.</span><span class="sxs-lookup"><span data-stu-id="18da4-114">This way, users are directed to the appropriate server for meeting content no matter which server or pool the simple URL DNS A records resolve to.</span></span>



</div>

### <a name="simple-url-option-1"></a><span data-ttu-id="18da4-115">Простой URL-адрес (вариант 1)</span><span class="sxs-lookup"><span data-stu-id="18da4-115">Simple URL Option 1</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18da4-116"><strong>Простой URL-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="18da4-116"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="18da4-117"><strong>Пример</strong></span><span class="sxs-lookup"><span data-stu-id="18da4-117"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18da4-118">Подходит</span><span class="sxs-lookup"><span data-stu-id="18da4-118">Meet</span></span></p></td>
<td><p><span data-ttu-id="18da4-119"> https://meet.contoso.com, https://meet.fabrikam.com и т. д. (для каждого домена SIP в вашей организации)</span><span class="sxs-lookup"><span data-stu-id="18da4-119">https://meet.contoso.com, https://meet.fabrikam.com, and so on (one for each SIP domain in your organization)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18da4-120">Телефонные подключения</span><span class="sxs-lookup"><span data-stu-id="18da4-120">Dial-in</span></span></p></td>
<td><p>https://dialin.contoso.com</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18da4-121">RAS</span><span class="sxs-lookup"><span data-stu-id="18da4-121">Admin</span></span></p></td>
<td><p>https://admin.contoso.com</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18da4-122">Если вы используете вариант 1, необходимо определить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="18da4-122">If you use Option 1, you must define the following:</span></span>

  - <span data-ttu-id="18da4-123">Для каждого такого простого URL-адреса вам понадобится запись DNS A, которая разрешает URL-адрес в каталог, если у вас есть один из развертываний.</span><span class="sxs-lookup"><span data-stu-id="18da4-123">For each Meet simple URL, you need a DNS A record that resolves the URL to the IP address of the Director, if you have one deployed.</span></span> <span data-ttu-id="18da4-124">В противном случае оно должно разрешаться в IP-адрес подсистемы балансировки нагрузки в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="18da4-124">Otherwise, it should resolve to the IP address of the load balancer of a Front End pool.</span></span> <span data-ttu-id="18da4-125">Если вы не развернули пул и используете стандартное развертывание сервера выпусков, запись DNS A должна разрешаться в IP-адрес одного стандартного выпуска сервера в Организации.</span><span class="sxs-lookup"><span data-stu-id="18da4-125">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>
    
    <span data-ttu-id="18da4-126">Если у вас есть несколько доменов SIP в Организации и вы используете этот параметр, необходимо создать для каждого домена SIP простые URL-адреса, и для каждого из них требуется запись DNS A для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="18da4-126">If you have more than one SIP domain in your organization and you use this option, you must create Meet simple URLs for each SIP domain and you need a DNS A record for each Meet simple URL.</span></span> <span data-ttu-id="18da4-127">Например, если у вас есть и contoso.com, и fabrikam.com, вы создадите записи A для обоих типов https://meet.contoso.com и https://meet.fabrikam.com .</span><span class="sxs-lookup"><span data-stu-id="18da4-127">For example, if you have both contoso.com and fabrikam.com, you will create DNS A records for both https://meet.contoso.com and https://meet.fabrikam.com.</span></span>
    
    <span data-ttu-id="18da4-128">Кроме того, если у вас есть несколько доменов SIP и вы хотите минимизировать требования к записям DNS и сертификатам для этих простых URL-адресов, воспользуйтесь вариантом 3, описанным ниже в этой статье.</span><span class="sxs-lookup"><span data-stu-id="18da4-128">Alternatively, if you have multiple SIP domains and you want to minimize the DNS record and certificate requirements for these simple URLs, use Option 3 as described later in this topic.</span></span>

  - <span data-ttu-id="18da4-129">Для простого URL-адреса с телефонным подключением вам понадобится запись DNS A, которая разрешает URL-адрес в каталог, если у вас есть один из развертываний.</span><span class="sxs-lookup"><span data-stu-id="18da4-129">For the Dial-in simple URL, you need a DNS A record that resolves the URL to the IP address of the Director, if you have one deployed.</span></span> <span data-ttu-id="18da4-130">В противном случае оно должно разрешаться в IP-адрес подсистемы балансировки нагрузки в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="18da4-130">Otherwise, it should resolve to the IP address of the load balancer of a Front End pool.</span></span> <span data-ttu-id="18da4-131">Если вы не развернули пул и используете стандартное развертывание сервера выпусков, запись DNS A должна разрешаться в IP-адрес одного стандартного выпуска сервера в Организации.</span><span class="sxs-lookup"><span data-stu-id="18da4-131">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>

  - <span data-ttu-id="18da4-132">Простой URL-адрес администратора является внутренним.</span><span class="sxs-lookup"><span data-stu-id="18da4-132">The Admin simple URL is internal only.</span></span> <span data-ttu-id="18da4-133">Для этого требуется запись DNS A, которая разрешает URL-адрес в каталог, если один из них развернут.</span><span class="sxs-lookup"><span data-stu-id="18da4-133">It requires a DNS A record that resolves the URL to the IP address of the Director, if you have one deployed.</span></span> <span data-ttu-id="18da4-134">В противном случае оно должно разрешаться в IP-адрес подсистемы балансировки нагрузки в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="18da4-134">Otherwise, it should resolve to the IP address of the load balancer of a Front End pool.</span></span> <span data-ttu-id="18da4-135">Если вы не развернули пул и используете стандартное развертывание сервера выпусков, запись DNS A должна разрешаться в IP-адрес одного стандартного выпуска сервера в Организации.</span><span class="sxs-lookup"><span data-stu-id="18da4-135">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>

</div>

<div>

## <a name="simple-url-option-2"></a><span data-ttu-id="18da4-136">Параметр простого URL-адреса 2</span><span class="sxs-lookup"><span data-stu-id="18da4-136">Simple URL Option 2</span></span>

<span data-ttu-id="18da4-137">В параметре 2 простые URL-адреса для "Встреча", "Входящие" и "Администратор" имеют общий базовый URL-адрес, например lync.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="18da4-137">With Option 2, the Meet, Dial-in, and Admin simple URLs all have a common base URL, such as lync.contoso.com.</span></span> <span data-ttu-id="18da4-138">Таким образом, для простых URL-адресов требуется только одна запись DNS A, которая разрешает lync.contoso.com IP-адресу пула пулов или интерфейсов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="18da4-138">Therefore, you need only one DNS A record for these simple URLs, which resolves lync.contoso.com to the IP address of a Director pool or Front End pool.</span></span> <span data-ttu-id="18da4-139">Если вы не развернули пул и используете стандартное развертывание сервера выпусков, запись DNS A должна разрешаться в IP-адрес одного стандартного выпуска сервера в Организации.</span><span class="sxs-lookup"><span data-stu-id="18da4-139">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>

<span data-ttu-id="18da4-140">Обратите внимание, что если у вас есть несколько доменов SIP в вашей организации, вам по-прежнему необходимо создавать простые URL-адреса для каждого домена SIP, и для каждого из них требуется запись DNS A.</span><span class="sxs-lookup"><span data-stu-id="18da4-140">Note that if you have more than one SIP domain in your organization, you must still create Meet simple URLs for each SIP domain and you need a DNS A record for each Meet simple URL.</span></span> <span data-ttu-id="18da4-141">В данном примере три простых URL-адреса в соответствии с lync.contoso.com, для дополнительного простого URL-адреса для fabrikam.com настраивается с использованием другого базового URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="18da4-141">In this example, while three simple URLs are all based on lync.contoso.com, an additional Meet simple URL for fabrikam.com is set up with a different base URL.</span></span> <span data-ttu-id="18da4-142">В этом примере необходимо создать записи DNS A для обоих типов https://lync.contoso.com и https://lync.fabrikam.com .</span><span class="sxs-lookup"><span data-stu-id="18da4-142">In this example, you must create DNS A records for both https://lync.contoso.com and https://lync.fabrikam.com.</span></span> <span data-ttu-id="18da4-143">Параметр "простой URL-адрес 3" показывает другой способ обработки именования и DNS-записей A, если у вас есть несколько доменов SIP.</span><span class="sxs-lookup"><span data-stu-id="18da4-143">Simple URL Option 3 shows another way to handle naming and DNS A records if you have multiple SIP domains.</span></span>

### <a name="simple-url-option-2"></a><span data-ttu-id="18da4-144">Параметр простого URL-адреса 2</span><span class="sxs-lookup"><span data-stu-id="18da4-144">Simple URL Option 2</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18da4-145"><strong>Простой URL-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="18da4-145"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="18da4-146"><strong>Пример</strong></span><span class="sxs-lookup"><span data-stu-id="18da4-146"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18da4-147">Подходит</span><span class="sxs-lookup"><span data-stu-id="18da4-147">Meet</span></span></p></td>
<td><p><span data-ttu-id="18da4-148"> https://lync.contoso.com/Meet, https://lync.fabrikam.com/Meet и т. д. (для каждого домена SIP в вашей организации)</span><span class="sxs-lookup"><span data-stu-id="18da4-148">https://lync.contoso.com/Meet, https://lync.fabrikam.com/Meet, and so on (one for each SIP domain in your organization)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18da4-149">Телефонные подключения</span><span class="sxs-lookup"><span data-stu-id="18da4-149">Dial-in</span></span></p></td>
<td><p>https://lync.contoso.com/Dialin</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18da4-150">RAS</span><span class="sxs-lookup"><span data-stu-id="18da4-150">Admin</span></span></p></td>
<td><p>https://lync.contoso.com/Admin</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simple-url-option-3"></a><span data-ttu-id="18da4-151">Простой URL-адрес (вариант 3)</span><span class="sxs-lookup"><span data-stu-id="18da4-151">Simple URL Option 3</span></span>

<span data-ttu-id="18da4-152">Вариант 3 полезен, если у вас есть большое количество доменов SIP и вы хотите, чтобы они были разными простыми URL-адресами, но хотели минимизировать требования к записям DNS и сертификатам для этих простых URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="18da4-152">Option 3 is most useful if you have many SIP domains, and you want them to have separate simple URLs but want to minimize the DNS record and certificate requirements for these simple URLs.</span></span> <span data-ttu-id="18da4-153">В этом примере требуется только одна запись DNS A, которая разрешается в lync.contoso.com с IP-адресом пула директоров или интерфейсного пула.</span><span class="sxs-lookup"><span data-stu-id="18da4-153">In this example, you need only one DNS A record, which resolves lync.contoso.com to the IP address of a Director pool or Front End pool.</span></span>

### <a name="simple-url-option-3"></a><span data-ttu-id="18da4-154">Простой URL-адрес (вариант 3)</span><span class="sxs-lookup"><span data-stu-id="18da4-154">Simple URL Option 3</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18da4-155"><strong>Простой URL-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="18da4-155"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="18da4-156"><strong>Пример</strong></span><span class="sxs-lookup"><span data-stu-id="18da4-156"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18da4-157">Подходит</span><span class="sxs-lookup"><span data-stu-id="18da4-157">Meet</span></span></p></td>
<td><p>https://lync.contoso.com/contosoSIPdomain/Meet</p>
<p>https://lync.contoso.com/fabrikamSIPdomain/Meet</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18da4-158">Телефонные подключения</span><span class="sxs-lookup"><span data-stu-id="18da4-158">Dial-in</span></span></p></td>
<td><p>https://lync.contoso.com/contosoSIPdomain/Dialin</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18da4-159">RAS</span><span class="sxs-lookup"><span data-stu-id="18da4-159">Admin</span></span></p></td>
<td><p>https://lync.contoso.com/contosoSIPdomain/Admin</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="disaster-recovery-option-for-simple-urls"></a><span data-ttu-id="18da4-160">Параметры аварийного восстановления для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="18da4-160">Disaster Recovery Option for Simple URLs</span></span>

<span data-ttu-id="18da4-161">Если у вас есть несколько сайтов, которые содержат пулы интерфейсов и поставщик DNS поддерживает GeoDNS, вы можете настроить записи DNS для простых URL-адресов, чтобы обеспечить поддержку аварийного восстановления, чтобы сделать простые функции URL-адресов более близкими, даже если весь пул переднего плана выйдет из резервной точки.</span><span class="sxs-lookup"><span data-stu-id="18da4-161">If you have multiple sites that contain Front End pools and your DNS provider supports GeoDNS, you can set up your DNS records for Simple URLs to support disaster recovery, so that Simple URL functionality continues even if one entire Front End pool goes down.</span></span> <span data-ttu-id="18da4-162">Это средство аварийного восстановления поддерживает простые URL-адреса для "Встреча" и "телефон-подключение".</span><span class="sxs-lookup"><span data-stu-id="18da4-162">This disaster recovery feature supports the Meet and Dial-In simple URLs.</span></span>

<span data-ttu-id="18da4-163">Чтобы настроить это, создайте два адреса GeoDNS.</span><span class="sxs-lookup"><span data-stu-id="18da4-163">To configure this, create two GeoDNS addresses.</span></span> <span data-ttu-id="18da4-164">У каждого адреса есть две записи DNS A или CNAME, которые разрешают два пула, которые сопоставлены вместе для целей аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="18da4-164">Each address has two DNS A or CNAME records that resolve to two pools which are paired together for disaster recovery purposes.</span></span> <span data-ttu-id="18da4-165">Для внутреннего доступа используется один адрес GeoDNS и разрешение на внутренние доменные имена и IP-адреса подсистемы балансировки нагрузки для двух пулов.</span><span class="sxs-lookup"><span data-stu-id="18da4-165">One GeoDNS address is used for internal access, and resolves to the internal web FQDN or load balancer IP address for the two pools.</span></span> <span data-ttu-id="18da4-166">Другой адрес GeoDNS используется для внешнего доступа и разрешается в внешнем полном доменном имени или IP-адресе подсистемы балансировки нагрузки для двух пулов.</span><span class="sxs-lookup"><span data-stu-id="18da4-166">The other GeoDNS address is used for external access and resolves to the external web FQDN or load balancer IP address for the two pools.</span></span> <span data-ttu-id="18da4-167">Ниже приведен пример для простого URL-адреса, используя полные доменные имена для пулов.</span><span class="sxs-lookup"><span data-stu-id="18da4-167">The following is an example for the Meet simple URL, using the FQDNs for the pools.</span></span>

   ```console
    Meet-int.geolb.contoso.com
         Pool1InternalWebFQDN.contoso.com
         Pool2InternalWebFQDN.contoso.com
   ```

   ```console
   Meet-ext.geolb.contoso.com
         Pool1ExternalWebFQDN.contoso.com
         Pool2ExternalWebFQDN.contoso.com
   ``` 

<span data-ttu-id="18da4-168">Затем создайте записи CNAME, которые разрешают выполнение вашего простого URL-адреса (например, meet.contoso.com) для двух адресов GeoDNS.</span><span class="sxs-lookup"><span data-stu-id="18da4-168">Then create CNAME records that resolve your Meet simple URL (such as meet.contoso.com) to the two GeoDNS addresses.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="18da4-169">Если в вашей сети используется <EM>hairpinning</EM> (маршрутизация всего простого трафика по URL-адресу с помощью внешней ссылки, включая трафик из вашей организации), вы можете просто настроить внешний адрес GeoDNS и разрешить всему ПРОСТОМУ URL-адресу только этот внешний адрес.</span><span class="sxs-lookup"><span data-stu-id="18da4-169">If your network uses <EM>hairpinning</EM> (routing all your Simple URL traffic through the external link, including traffic that comes from within your organization), then you can just configure the external GeoDNS address and resolve your Meet simple URL to only that external address.</span></span>



</div>

<span data-ttu-id="18da4-170">При использовании этого метода вы можете настроить каждый адрес GeoDNS таким образом, чтобы он использовал метод циклического перераспределения, чтобы распределять запросы к двум пулам, или подключаться преимущественно к одному пулу (например, пул, который расположен географически ближе), и использовать другой пул только в случае сбоя подключения.</span><span class="sxs-lookup"><span data-stu-id="18da4-170">When you use this method, you can configure each GeoDNS address to use either a round robin method to distribute requests to the two pools, or to connect primarily to one pool (such as the pool located geographically closer) and use the other pool only in case of connectivity failure.</span></span>

<span data-ttu-id="18da4-171">Вы можете настроить такую же конфигурацию для простого URL-адреса с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="18da4-171">You can set up the same configuration for the Dial-In simple URL.</span></span> <span data-ttu-id="18da4-172">Для этого создайте дополнительные записи, такие как в предыдущем примере, с заменой `dialin` `meet` в DNS-записях.</span><span class="sxs-lookup"><span data-stu-id="18da4-172">To do so, create additional records like those in the previous example, substituting `dialin` for `meet` in the DNS records.</span></span> <span data-ttu-id="18da4-173">Для простого URL-адреса администратора используйте один из трех описанных выше параметров в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="18da4-173">For the Admin simple URL, use one of the three options listed earlier in this section.</span></span>

<span data-ttu-id="18da4-174">После настройки конфигурации вы должны использовать приложение мониторинга для настройки наблюдения HTTP для отслеживания сбоев.</span><span class="sxs-lookup"><span data-stu-id="18da4-174">Once this configuration is set up, you must use a monitoring application to set up HTTP monitoring to watch for failures.</span></span> <span data-ttu-id="18da4-175">Для внешнего доступа убедитесь в том, что протокол HTTPS получил запросы на автообнаружение полного доменного имени или IP-адреса подсистемы балансировки нагрузки для двух пулов.</span><span class="sxs-lookup"><span data-stu-id="18da4-175">For external access, monitor to make sure that HTTPS GET autodiscovery requests to the external web FQDN or load balancer IP address for the two pools are successful.</span></span> <span data-ttu-id="18da4-176">Например, следующие запросы не должны содержать заголовков **приема** и должны возвращать **200 ОК**.</span><span class="sxs-lookup"><span data-stu-id="18da4-176">For example, the following requests must not contain any **ACCEPT** header and must return **200 OK**.</span></span>

```console
    HTTPS GET Pool1ExternalWebFQDN.contoso.com/autodiscover/autodiscoverservice.svc/root
    HTTPS GET Pool2ExternalWebFQDN.contoso.com/autodiscover/autodiscoverservice.svc/root
```

<span data-ttu-id="18da4-177">Для внутреннего доступа необходимо следить за портом 5061 на внутреннем полном доменном имени или IP-адресе подсистемы балансировки нагрузки для двух пулов.</span><span class="sxs-lookup"><span data-stu-id="18da4-177">For internal access, you must monitor port 5061 on the internal web FQDN or load balancer IP address for the two pools.</span></span> <span data-ttu-id="18da4-178">Если обнаружены ошибки подключения, VIP для этих пулов должен закрыть порты 80, 443 и 444.</span><span class="sxs-lookup"><span data-stu-id="18da4-178">If any connectivity failures are detected, the VIP for these pools must close ports 80, 443 and 444.</span></span>

<span data-ttu-id="18da4-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18da4-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

