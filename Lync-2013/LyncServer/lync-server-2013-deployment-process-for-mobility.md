---
title: 'Lync Server 2013: процесс развертывания для организации мобильной работы'
description: 'Lync Server 2013: процесс развертывания для мобильных устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for mobility
ms:assetid: 5a1cebda-c14b-4ff4-9c36-f7caa868160f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690023(v=OCS.15)
ms:contentKeyID: 48184220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b49d69af899f6d9f2ac1db5040d017a9d62ce9eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399562"
---
# <a name="deployment-process-for-mobility-in-lync-server-2013"></a><span data-ttu-id="8f1f4-103">Процесс развертывания для организации мобильной работы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f1f4-103">Deployment process for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f1f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f1f4-104">

<span> </span></span></span>

<span data-ttu-id="8f1f4-105">_**Тема последнего изменения:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="8f1f4-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013. It is noted accordingly.

<span data-ttu-id="8f1f4-106">В этом разделе описывается последовательность действий, необходимых для развертывания функции Lync Server 2013 Mobility.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-106">This section describes the sequence of steps required to deploy the Lync Server 2013 mobility feature.</span></span>

### <a name="mobility-deployment-process"></a><span data-ttu-id="8f1f4-107">Процесс развертывания для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="8f1f4-107">Mobility Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1f4-108">Этап</span><span class="sxs-lookup"><span data-stu-id="8f1f4-108">Phase</span></span></th>
<th><span data-ttu-id="8f1f4-109">Шаги</span><span class="sxs-lookup"><span data-stu-id="8f1f4-109">Steps</span></span></th>
<th><span data-ttu-id="8f1f4-110">Разрешения</span><span class="sxs-lookup"><span data-stu-id="8f1f4-110">Permissions</span></span></th>
<th><span data-ttu-id="8f1f4-111">Документация по развертыванию</span><span class="sxs-lookup"><span data-stu-id="8f1f4-111">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f1f4-112">Создание записей DNS (Domain Name System)</span><span class="sxs-lookup"><span data-stu-id="8f1f4-112">Create Domain Name System (DNS) records</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8f1f4-113">Создайте внутреннюю запись DNS CNAME или A (Host, если IPv6, AAAA) для разрешения URL-адреса внутренней службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-113">Create an internal DNS CNAME or A (host, if IPv6, AAAA) record to resolve the internal Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-114">Создайте внешнюю запись DNS CNAME или (Host, если IPv6, AAAA) для разрешения внешнего URL-адреса службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-114">Create an external DNS CNAME or A (host, if IPv6, AAAA) record to resolve the external Autodiscover Service URL.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="8f1f4-115">Администраторы домена</span><span class="sxs-lookup"><span data-stu-id="8f1f4-115">Domain Admins</span></span></p>
<p><span data-ttu-id="8f1f4-116">DnsAdmins</span><span class="sxs-lookup"><span data-stu-id="8f1f4-116">DnsAdmins</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Создание DNS-записей для службы автообнаружения в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8f1f4-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Creating DNS records for the Autodiscover Service in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f1f4-118">Изменение сертификатов</span><span class="sxs-lookup"><span data-stu-id="8f1f4-118">Modify certificates</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-119">Добавьте записи альтернативного имени субъекта в следующие сертификаты для поддержки безопасных подключений для мобильных пользователей:</span><span class="sxs-lookup"><span data-stu-id="8f1f4-119">Add subject alternative name entries to the following certificates to support secure connections for mobile users:</span></span></p>
<ul>
<li><p><span data-ttu-id="8f1f4-120">Сертификат директора</span><span class="sxs-lookup"><span data-stu-id="8f1f4-120">Director certificate</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-121">Сертификат пула на стороне переднего плана</span><span class="sxs-lookup"><span data-stu-id="8f1f4-121">Front End pool certificate</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-122">Обратный сертификат прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="8f1f4-122">Reverse proxy certificate</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="8f1f4-123">Локальный администратор</span><span class="sxs-lookup"><span data-stu-id="8f1f4-123">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Изменение сертификатов для мобильной работы в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8f1f4-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Modifying certificates for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f1f4-125">Настройка обратного прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="8f1f4-125">Configure the reverse proxy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8f1f4-126">Назначьте сертификаты, обновленные с помощью альтернативных имен субъектов, в прослушиватель SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="8f1f4-126">Assign certificates updated with subject alternative names to the Secure Sockets Layer (SSL) Listener.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-127">Измените параметры правила веб-публикации для внешнего URL-адреса службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-127">Reconfigure the web publishing rule for the external Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-128">Убедитесь, что для внешнего URL-адреса служб Lync Server 2013 в пуле переднего плана существует правило веб-публикации.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-128">Be sure that a web publishing rule exists for the external Lync Server 2013 Web Services URL on your Front End pool.</span></span></p></li>
</ul>
<p><span data-ttu-id="8f1f4-129">Или</span><span class="sxs-lookup"><span data-stu-id="8f1f4-129">Or</span></span></p>
<ul>
<li><p><span data-ttu-id="8f1f4-130">Если вы решили использовать HTTP для начального запроса автообнаружения и не обновили списки альтернативных имен субъектов в сертификатах, настройте новое правило публикации веб-публикации или перенастройте существующее правило для порта 80 HTTP.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-130">If you choose to use HTTP for the initial Autodiscover request and do not update subject alternative name lists on the certificates, configure a new web publishing rule or reconfigure an existing publishing rule for port 80 HTTP.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="8f1f4-131">Локальный администратор</span><span class="sxs-lookup"><span data-stu-id="8f1f4-131">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Настройка обратного прокси-сервера для мобильной работы в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8f1f4-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f1f4-133">Проверка развертывания Mobility Service для Lync 2010 Mobile с помощью службы Mobility MCX</span><span class="sxs-lookup"><span data-stu-id="8f1f4-133">Test your mobility deployment for Lync 2010 Mobile using the Mcx Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-134">Запустите <strong>Test-CsMcxP2PIM</strong> , чтобы протестировать отправку мгновенного сообщения от одного пользователя другому.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-134">Run <strong>Test-CsMcxP2PIM</strong> to test sending an instant message from one person to another.</span></span></p>
<p><span data-ttu-id="8f1f4-135">Ознакомьтесь с документацией по командлету командной консоли Lync Server для <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">Test-CsMcxP2PIM</a> , чтобы просмотреть полный список вариантов.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-135">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">Test-CsMcxP2PIM</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-136">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="8f1f4-136">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Проверка развертывания среды для мобильной работы в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8f1f4-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f1f4-138">Проверка развертывания Mobility Service для мобильных клиентов Lync 2013 с помощью веб-компонентов UCWA</span><span class="sxs-lookup"><span data-stu-id="8f1f4-138">Test your mobility deployment for Lync 2013 Mobile clients using the UCWA Web components</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-139">С помощью командлета <strong>Test-CsUcwaConference</strong> вы можете протестировать и проверить, что предварительно определенные пользователи теста и пользователи могут использовать UCWA для создания Конференции и участия в ней.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-139">Use the <strong>Test-CsUcwaConference</strong> cmdlet to test and verify that pre-defined test users or a pair of actual users can use UCWA to create and participate in a conference.</span></span></p>
<p><span data-ttu-id="8f1f4-140">Ознакомьтесь с документацией по командлету командной консоли Lync Server для <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">Test-CsUcwaConference</a> , чтобы просмотреть полный список вариантов.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-140">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">Test-CsUcwaConference</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-141">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="8f1f4-141">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Проверка развертывания среды для мобильной работы в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8f1f4-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f1f4-143">Настройка для использования push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="8f1f4-143">Configure for push notifications</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8f1f4-144">На серверах пограничного сервера Lync Server 2013 добавьте поставщик услуг размещения Lync Server Online и настройте Федерацию поставщика услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-144">For Lync Server 2013 Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-145">На серверах пограничного сервера Lync Server 2010 добавьте поставщик услуг размещения Lync Server Online и настройте Федерацию поставщика услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-145">For Lync Server 2010  Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-146">Для пограничного сервера Office Communications Server 2007 R2 добавьте федеративного партнера.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-146">For Office Communications Server 2007 R2 Edge Servers, add a federated partner.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-147">Если вы хотите поддерживать push-уведомления по сети Wi-Fi, настройте для порта TCP 5223 правило брандмауэра, которое исходит.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-147">If you want to support push notifications over a Wi-Fi network, configure a firewall rule outbound for TCP port 5223.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-148">Используйте командлет <strong>Set-CsPushNotificationConfiguration</strong> , чтобы включить извещающие уведомления в службу push-уведомлений Apple (APNs) и службу push-уведомлений Майкрософт (MPNS).</span><span class="sxs-lookup"><span data-stu-id="8f1f4-148">Use the <strong>Set-CsPushNotificationConfiguration</strong> cmdlet to enable push notifications to the Apple Push Notification Service (APNS) and Microsoft Push Notification Service (MPNS).</span></span> <span data-ttu-id="8f1f4-149">Эта функция отключена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-149">This feature is disabled by default.</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-150">С помощью командлета <strong>Test-CsFederatedPartner</strong> можно протестировать конфигурацию Федерации и командлет <strong>Test-CsMCXPushNotification</strong> для проверки извещающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-150">Use the <strong>Test-CsFederatedPartner</strong> cmdlet to test the federation configuration and the <strong>Test-CsMCXPushNotification</strong> cmdlet to test push notifications.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="8f1f4-151">Push-уведомления используются для мобильных клиентов Lync 2010 на устройствах Apple и Windows Phone</span><span class="sxs-lookup"><span data-stu-id="8f1f4-151">Push notifications are used for Lync 2010 Mobile clients on Apple devices and Windows Phone</span></span><BR><span data-ttu-id="8f1f4-152">Push-уведомление требуется для мобильных клиентов Lync 2013 только на Windows Phone</span><span class="sxs-lookup"><span data-stu-id="8f1f4-152">Push notification is required for Lync 2013 Mobile clients on Windows Phone only</span></span>


</div></li>
</ul></td>
<td><p><span data-ttu-id="8f1f4-153">RtcUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="8f1f4-153">RtcUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Настройка для использования push-уведомлений в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8f1f4-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Configuring for push notifications in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f1f4-155">Настройка политики мобильности</span><span class="sxs-lookup"><span data-stu-id="8f1f4-155">Configure mobility policy</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-156">Используйте командлет <strong>Set-CsMobilityPolicy</strong> , чтобы разрешить или запретить.</span><span class="sxs-lookup"><span data-stu-id="8f1f4-156">Use the <strong>Set-CsMobilityPolicy</strong> cmdlet to allow or disallow:</span></span></p>
<ul>
<li><p><span data-ttu-id="8f1f4-157">Вызов с рабочего телефона</span><span class="sxs-lookup"><span data-stu-id="8f1f4-157">Call via Work</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-158">Включение IP-звука и IP-видео</span><span class="sxs-lookup"><span data-stu-id="8f1f4-158">Enable IP Audio and IP Video</span></span></p></li>
<li><p><span data-ttu-id="8f1f4-159">Требуется WiFi для IP и/или IP-видео</span><span class="sxs-lookup"><span data-stu-id="8f1f4-159">Require WiFi for IP Audio and/or IP Video</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="8f1f4-160">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="8f1f4-160">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="8f1f4-161"><a href="lync-server-2013-configuring-mobility-policy.md">Настройка политики мобильных устройств в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8f1f4-161"><a href="lync-server-2013-configuring-mobility-policy.md">Configuring mobility policy in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="8f1f4-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f1f4-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

