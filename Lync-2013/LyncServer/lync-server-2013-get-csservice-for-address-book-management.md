---
title: 'Lync Server 2013: Get-CsService для управления адресными книгами'
description: 'Lync Server 2013: Get-CsService для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsService for Address Book management
ms:assetid: 373b717d-5efa-4c36-a899-a23a5bd922b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429698(v=OCS.15)
ms:contentKeyID: 48183853
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e46173429988d87022c13fab33e3778279dd0e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427987"
---
# <a name="get-csservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="fb4aa-103">Get-CsService для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb4aa-103">Get-CsService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb4aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb4aa-104">

<span> </span></span></span>

<span data-ttu-id="fb4aa-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="fb4aa-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="fb4aa-106">Кто может запустить этот командлет: по умолчанию членам следующих групп разрешено выполнять командлет Get-CsService локально: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="fb4aa-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsService cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="fb4aa-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fb4aa-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsService"}

<span data-ttu-id="fb4aa-108">Get-CsService полезно получить и отобразить текущую конфигурацию веб-служб, определенных вашей инфраструктурой.</span><span class="sxs-lookup"><span data-stu-id="fb4aa-108">Get-CsService is valuable to retrieve and display the current configuration of your infrastructure’s defined Web Services.</span></span> <span data-ttu-id="fb4aa-109">Определив полное доменное имя (FQDN) для пула и веб-сервер параметров, командлет выводит на экран службы, предоставляемые вашим сервером, в том числе URI обработчика адресной книги и расширения списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="fb4aa-109">By defining the pool’s fully qualified domain name (FQDN) and the parameter WebServer, the cmdlet returns the web-based services offered by your server, including the Address Book handler and distribution list expansion URIs.</span></span>

<span data-ttu-id="fb4aa-110">Например:</span><span class="sxs-lookup"><span data-stu-id="fb4aa-110">For example:</span></span>

    Get-CsService -PoolFqdn "fe01.contoso.net" -WebServer

<span data-ttu-id="fb4aa-111">Этот командлет возвращает следующее:</span><span class="sxs-lookup"><span data-stu-id="fb4aa-111">This cmdlet returns the following:</span></span>

<span data-ttu-id="fb4aa-112">Identity::pool01. contoso. NET</span><span class="sxs-lookup"><span data-stu-id="fb4aa-112">Identity : WebServer:pool01.contoso.net</span></span>

<span data-ttu-id="fb4aa-113">Хранилище файлов: хранилища файлов:DC01. contoso. NET</span><span class="sxs-lookup"><span data-stu-id="fb4aa-113">FileStore : FileStore:dc01.contoso.net</span></span>

<span data-ttu-id="fb4aa-114">UserServer: UserServer:pool01. contoso. NET</span><span class="sxs-lookup"><span data-stu-id="fb4aa-114">UserServer : UserServer:pool01.contoso.net</span></span>

<span data-ttu-id="fb4aa-115">PrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="fb4aa-115">PrimaryHttpPort : 80</span></span>

<span data-ttu-id="fb4aa-116">PrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="fb4aa-116">PrimaryHttpsPort : 443</span></span>

<span data-ttu-id="fb4aa-117">ExternalHttpPort: 8080</span><span class="sxs-lookup"><span data-stu-id="fb4aa-117">ExternalHttpPort : 8080</span></span>

<span data-ttu-id="fb4aa-118">ExternalHttpsPort: 4443</span><span class="sxs-lookup"><span data-stu-id="fb4aa-118">ExternalHttpsPort : 4443</span></span>

<span data-ttu-id="fb4aa-119">PublishedPrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="fb4aa-119">PublishedPrimaryHttpPort : 80</span></span>

<span data-ttu-id="fb4aa-120">PublishedPrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="fb4aa-120">PublishedPrimaryHttpsPort : 443</span></span>

<span data-ttu-id="fb4aa-121">PublishedExternalHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="fb4aa-121">PublishedExternalHttpPort : 80</span></span>

<span data-ttu-id="fb4aa-122">PublishedExternalHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="fb4aa-122">PublishedExternalHttpsPort : 443</span></span>

<span data-ttu-id="fb4aa-123">ReachPrimaryPsomServerPort: 8060</span><span class="sxs-lookup"><span data-stu-id="fb4aa-123">ReachPrimaryPsomServerPort : 8060</span></span>

<span data-ttu-id="fb4aa-124">ReachExternalPsomServerPort: 8061</span><span class="sxs-lookup"><span data-stu-id="fb4aa-124">ReachExternalPsomServerPort : 8061</span></span>

<span data-ttu-id="fb4aa-125">AppSharingPortStart: 49152</span><span class="sxs-lookup"><span data-stu-id="fb4aa-125">AppSharingPortStart : 49152</span></span>

<span data-ttu-id="fb4aa-126">AppSharingPortCount: 16383</span><span class="sxs-lookup"><span data-stu-id="fb4aa-126">AppSharingPortCount : 16383</span></span>

<span data-ttu-id="fb4aa-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span></span>

<span data-ttu-id="fb4aa-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span><span class="sxs-lookup"><span data-stu-id="fb4aa-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span></span>

<span data-ttu-id="fb4aa-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span><span class="sxs-lookup"><span data-stu-id="fb4aa-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span></span>

<span data-ttu-id="fb4aa-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span></span>

<span data-ttu-id="fb4aa-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span></span>

<span data-ttu-id="fb4aa-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="fb4aa-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="fb4aa-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span><span class="sxs-lookup"><span data-stu-id="fb4aa-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span></span>

<span data-ttu-id="fb4aa-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span><span class="sxs-lookup"><span data-stu-id="fb4aa-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span></span>

<span data-ttu-id="fb4aa-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="fb4aa-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="fb4aa-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span></span>

<span data-ttu-id="fb4aa-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="fb4aa-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span></span>

<span data-ttu-id="fb4aa-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span><span class="sxs-lookup"><span data-stu-id="fb4aa-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span></span>

<span data-ttu-id="fb4aa-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span><span class="sxs-lookup"><span data-stu-id="fb4aa-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span></span>

<span data-ttu-id="fb4aa-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="fb4aa-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="fb4aa-143">MeetExternalUri : https://csweb.contoso.com/Meet</span><span class="sxs-lookup"><span data-stu-id="fb4aa-143">MeetExternalUri : https://csweb.contoso.com/Meet</span></span>

<span data-ttu-id="fb4aa-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span><span class="sxs-lookup"><span data-stu-id="fb4aa-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span></span>

<span data-ttu-id="fb4aa-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span><span class="sxs-lookup"><span data-stu-id="fb4aa-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span></span>

<span data-ttu-id="fb4aa-146">ReachExternalUri : https://csweb.contoso.com/Reach</span><span class="sxs-lookup"><span data-stu-id="fb4aa-146">ReachExternalUri : https://csweb.contoso.com/Reach</span></span>

<span data-ttu-id="fb4aa-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span><span class="sxs-lookup"><span data-stu-id="fb4aa-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span></span>

<span data-ttu-id="fb4aa-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="fb4aa-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="fb4aa-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="fb4aa-150">ExternalFqdn: csweb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fb4aa-150">ExternalFqdn : csweb.contoso.com</span></span>

<span data-ttu-id="fb4aa-151">InternalFqdn: internalweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="fb4aa-151">InternalFqdn : internalweb.contoso.net</span></span>

<span data-ttu-id="fb4aa-152">DependentServiceList: {регистратор:pool01. contoso. NET, ConferencingServer:pool01. contoso. NET}</span><span class="sxs-lookup"><span data-stu-id="fb4aa-152">DependentServiceList : {Registrar:pool01.contoso.net, ConferencingServer:pool01.contoso.net}</span></span>

<span data-ttu-id="fb4aa-153">ServiceId: 1 — WebService-1</span><span class="sxs-lookup"><span data-stu-id="fb4aa-153">ServiceId : 1-WebServices-1</span></span>

<span data-ttu-id="fb4aa-154">Идентификатор сайта: сайт Redmond</span><span class="sxs-lookup"><span data-stu-id="fb4aa-154">SiteId : Site:Redmond</span></span>

<span data-ttu-id="fb4aa-155">PoolFqdn: pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="fb4aa-155">PoolFqdn : pool01.contoso.net</span></span>

<span data-ttu-id="fb4aa-156">Версия: 5</span><span class="sxs-lookup"><span data-stu-id="fb4aa-156">Version : 5</span></span>

<span data-ttu-id="fb4aa-157">Роль: сервер</span><span class="sxs-lookup"><span data-stu-id="fb4aa-157">Role : WebServer</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="fb4aa-158">См. также</span><span class="sxs-lookup"><span data-stu-id="fb4aa-158">See Also</span></span>


[<span data-ttu-id="fb4aa-159">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="fb4aa-159">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="fb4aa-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb4aa-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

