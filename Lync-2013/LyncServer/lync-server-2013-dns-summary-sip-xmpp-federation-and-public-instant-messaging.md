---
title: Сводка DNS-SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями
description: Общие сведения о DNS — SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - SIP, XMPP federation, and public instant messaging
ms:assetid: 1ed24fb8-a849-44c0-a52e-7aef7527e644
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618369(v=OCS.15)
ms:contentKeyID: 49105656
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f40013b8346cc049f844a827b21bef81a66f6950
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397936"
---
# <a name="dns-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="52c16-103">Сводка DNS-SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52c16-103">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52c16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52c16-104">

<span> </span></span></span>

<span data-ttu-id="52c16-105">_**Тема последнего изменения:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="52c16-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="52c16-106">Записи DNS, которые требуются для определения Федерации с помощью Office Communications Server или Lync Server, определяются вашим решением для разрешения автоматического обнаружения DNS вашего домена другими партнерами по перспективам.</span><span class="sxs-lookup"><span data-stu-id="52c16-106">The Domain Name System (DNS) records that will be required for defining a federation with Office Communications Server or Lync Server partners is determined by your decision to either allow automatic DNS discovery of your domain by other perspective partners.</span></span> <span data-ttu-id="52c16-107">Если вы публикуете \_ sipfederationtls. \_ Номера.</span><span class="sxs-lookup"><span data-stu-id="52c16-107">If you publish the \_sipfederationtls.\_tcp.</span></span> <span data-ttu-id="52c16-108">*\<SIP domain name\>* SRV-запись, любой другой федеративный домен SIP сможет "найти" Федерацию.</span><span class="sxs-lookup"><span data-stu-id="52c16-108">*\<SIP domain name\>* SRV record, any other SIP federated domain will be able to “discover” your federation.</span></span> <span data-ttu-id="52c16-109">Вы можете управлять тем, какие федеративные домены смогут общаться с вами с помощью параметров "разрешить домены и заблокированные домены" на панели управления Lync Server, или путем настройки разрешенных и заблокированных доменов с помощью командной консоли Lync Server и командлетов PowerShell **Get**, **Set**, **New**, **Remove-CsAllowedDomain** и **-CsBlockedDomain** .</span><span class="sxs-lookup"><span data-stu-id="52c16-109">You can control which federated domains can communicate with you by using the Allows domains and Blocked Domains settings in the Lync Server Control Panel, or by setting the allowed or blocked domains configuration using the Lync Server Management Shell and the **Get**, **Set**, **New**, **Remove-CsAllowedDomain** and **-CsBlockedDomain** PowerShell cmdlets.</span></span> <span data-ttu-id="52c16-110">Дополнительные сведения о том, как настроить эти параметры и использование командлетов PowerShell, можно найти в разделе **связанные темы** в конце этой статьи.</span><span class="sxs-lookup"><span data-stu-id="52c16-110">For additional information on how to configure theses settings and the use of the PowerShell cmdlets, see **Related Topics** at the end of this topic.</span></span>

<span data-ttu-id="52c16-111">В таблице "Сводка DNS-записей" показаны необходимые записи для открытой или обнаруживаемой интеграции.</span><span class="sxs-lookup"><span data-stu-id="52c16-111">The DNS records summary table depicts the required entries for an open, or discoverable, federation.</span></span> <span data-ttu-id="52c16-112">Если вы не хотите реализовывать обнаружение Федерации, вы можете не настраивать \_ sipfederationtls. \_ Номера.</span><span class="sxs-lookup"><span data-stu-id="52c16-112">If you do not want to implement Federation Discovery, You can decide to not configure the \_sipfederationtls.\_tcp.</span></span> <span data-ttu-id="52c16-113">*\<SIP domain name\>* Табель.</span><span class="sxs-lookup"><span data-stu-id="52c16-113">*\<SIP domain name\>* record.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="52c16-114">Существуют определенные сценарии, в которых необходимо использовать _sipfederationtls. _tcp.</span><span class="sxs-lookup"><span data-stu-id="52c16-114">There are specific scenarios in which you must have the _sipfederationtls._tcp.</span></span> <span data-ttu-id="52c16-115">Запись SRV для <EM> &lt; доменного имени &gt; SIP</EM> , но вы не хотите иметь обнаруживаемую Федерацию.</span><span class="sxs-lookup"><span data-stu-id="52c16-115"><EM>&lt;SIP domain name&gt;</EM> SRV record, but you do not want to have a discoverable federation.</span></span> <span data-ttu-id="52c16-116">Один из таких экземпляров — это область, в которой вы развернули мобильность для пользователей.</span><span class="sxs-lookup"><span data-stu-id="52c16-116">One such instance is where you have deployed mobility for your users.</span></span> <span data-ttu-id="52c16-117">Расчетная палата для push-уведомлений для мобильных устройств (PNCH) — это особый тип Федерации, который используется для мобильных клиентов Microsoft Lync на устройствах Apple iPhone или iPad с помощью мобильных клиентов Lync 2010 2010 Mobile или Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="52c16-117">The mobility push notification clearinghouse (PNCH) is a special type of federation that is used for Microsoft Lync Mobile clients on Apple iPhone or iPad using the Lync 2010 Mobile client or Windows Phone using the Lync 2010 Mobile or Lync 2013 Mobile clients.</span></span> <span data-ttu-id="52c16-118">_Sipfederationtls. _tcp.</span><span class="sxs-lookup"><span data-stu-id="52c16-118">The _sipfederationtls._tcp.</span></span> <span data-ttu-id="52c16-119">Запись SRV для <EM> &lt; доменного имени &gt; SIP</EM> используется в случае мобильных устройств и push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="52c16-119"><EM>&lt;SIP domain name&gt;</EM> SRV record is used in the case of mobility and push notification.</span></span> <span data-ttu-id="52c16-120">Чтобы устранить эту ошибку и контролировать свое обнаружение, снимите флажок <STRONG>включить обнаружение домена партнера</STRONG> , чтобы отключить функцию обнаружения.</span><span class="sxs-lookup"><span data-stu-id="52c16-120">To mitigate this issue and control your discoverability, clear the setting <STRONG>Enable partner domain discovery</STRONG> to turn off discovery.</span></span>



</div>

<span data-ttu-id="52c16-121">Чтобы настроить расширенный протокол обмена сообщениями (XMPP) для развертывания, вы создаете две записи DNS (Domain Name System) на внешнем DNS-сервере, который будет разрешать записи в службу Edge EDGE на пограничном сервере или пуле Edge.</span><span class="sxs-lookup"><span data-stu-id="52c16-121">To configure extensible messaging and presence protocol (XMPP) for your deployment, you create two domain name system (DNS) records in an external DNS server that will resolve the records to the Access Edge service of your Edge Server or Edge pool.</span></span>

<span data-ttu-id="52c16-122">При настройке службы доменных имен (DNS) для общедоступной службы обмена мгновенными сообщениями вы обнаружите, что конфигурация, поддерживающая внешних пользователей, будет поддерживать подключение к службе обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="52c16-122">When you configure domain name system (DNS) for public instant messaging connectivity, you will find that the configuration that supports external users will support public IM connectivity.</span></span> <span data-ttu-id="52c16-123">Если вы уже настроили пограничный сервер или пул EDGE, вы должны иметь DNS-записи, необходимые для поддержки подключения к общедоступной службе обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="52c16-123">If you have already configured your Edge Server or Edge pool, you should have the DNS records necessary to support public IM connectivity.</span></span>

<div>

## <a name="dns-summary---sip-federation-including-public-instant-messaging-connectivity"></a><span data-ttu-id="52c16-124">Сводка DNS-Федерация SIP, включая общедоступную службу обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="52c16-124">DNS Summary - SIP Federation including Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52c16-125">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="52c16-125">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="52c16-126">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="52c16-126">FQDN</span></span></th>
<th><span data-ttu-id="52c16-127">IP-адрес или полное доменное имя записи узла</span><span class="sxs-lookup"><span data-stu-id="52c16-127">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="52c16-128">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="52c16-128">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52c16-129">Внешние DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="52c16-129">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="52c16-130">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="52c16-130">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="52c16-131">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="52c16-131">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="52c16-132">Внешний интерфейс службы Edge для доступа, необходимый для автоматического обнаружения DNS для Федерации с другими потенциальными партнерами Федерации, также называется "разрешенные домены SIP" ("Расширенные возможности Федерации в предыдущих выпусках)". При необходимости повторите эти действия для всех доменов SIP с пользователями, поддерживающими Lync.</span><span class="sxs-lookup"><span data-stu-id="52c16-132">Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="52c16-133">Эта запись SRV требуется для мобильных устройств и для очищенных push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="52c16-133">This SRV record is required for mobility and the push notification clearing house.</span></span> <span data-ttu-id="52c16-134">В случаях, когда имеется несколько доменов SIP, создайте и опубликуйте SRV-запись для каждого домена, который будет содержать мобильные клиенты Lync.</span><span class="sxs-lookup"><span data-stu-id="52c16-134">In cases where there is more than one SIP domain, create and publish an SRV record for each domain that will have Lync Mobile clients.</span></span> <span data-ttu-id="52c16-135">Служба push-уведомлений и Служба push-уведомлений Apple могут работать неправильно, если не существует явной записи SRV для каждого домена SIP, поддерживаемого развертыванием.</span><span class="sxs-lookup"><span data-stu-id="52c16-135">The Push Notification Service and Apple Push Notification service may not operate as expected if there is not an explicit SRV record for each SIP domain that the deployment supports.</span></span>

</td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="52c16-136">Сводка DNS: протокол расширенного обмена сообщениями и присутствия (XMPP)</span><span class="sxs-lookup"><span data-stu-id="52c16-136">DNS Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52c16-137">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="52c16-137">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="52c16-138">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="52c16-138">FQDN</span></span></th>
<th><span data-ttu-id="52c16-139">IP-адрес или полное доменное имя записи узла</span><span class="sxs-lookup"><span data-stu-id="52c16-139">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="52c16-140">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="52c16-140">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52c16-141">Внешние DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="52c16-141">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="52c16-142">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="52c16-142">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="52c16-143">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="52c16-143">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="52c16-144">Внешний интерфейс XMPP прокси-сервера в службе пограничного доступа или пуле Edge. При необходимости повторите эти действия для всех внутренних доменов SIP, в которых пользователи Lync поддерживают доступ к контактам с контактами XMPP с помощью глобальной политики, политики сайта, в которой находится пользователь, или политики пользователя, примененной к пользователю с поддержкой Lync.</span><span class="sxs-lookup"><span data-stu-id="52c16-144">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="52c16-145">Разрешенный домен XMPP также должен быть настроен в политике федеративных партнеров XMPP.</span><span class="sxs-lookup"><span data-stu-id="52c16-145">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="52c16-146">Дополнительные сведения <strong>можно</strong> найти в разделах.</span><span class="sxs-lookup"><span data-stu-id="52c16-146">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c16-147">Внешние DNS/A</span><span class="sxs-lookup"><span data-stu-id="52c16-147">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="52c16-148">xmpp.contoso.com (например)</span><span class="sxs-lookup"><span data-stu-id="52c16-148">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="52c16-149">IP-адрес службы пограничного доступа на пограничном сервере или в пограничном пуле, где размещен прокси-сервер XMPP</span><span class="sxs-lookup"><span data-stu-id="52c16-149">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="52c16-150">Указывает на службу пограничного доступа или пул EDGE, на котором размещена служба прокси XMPP.</span><span class="sxs-lookup"><span data-stu-id="52c16-150">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="52c16-151">Как правило, создаваемая SRV-запись будет указывать на эту запись узла (A или AAAA).</span><span class="sxs-lookup"><span data-stu-id="52c16-151">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="52c16-152">См. также</span><span class="sxs-lookup"><span data-stu-id="52c16-152">See Also</span></span>


[<span data-ttu-id="52c16-153">Настройка федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52c16-153">Setting up XMPP federation in Lync Server 2013</span></span>](lync-server-2013-setting-up-xmpp-federation.md)  
[<span data-ttu-id="52c16-154">Настройка для использования push-уведомлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52c16-154">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
[<span data-ttu-id="52c16-155">Включение или отключение обнаружения федеративных партнеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52c16-155">Enable or disable discovery of federation partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)  


[<span data-ttu-id="52c16-156">Сценарии доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52c16-156">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="52c16-157">Определение требований DNS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52c16-157">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="52c16-158">Управление федеративными доменами SIP для организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52c16-158">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
  

<span data-ttu-id="52c16-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52c16-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

