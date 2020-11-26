---
title: 'Lync Server 2013: Просмотр состояния глобальных параметров для леса'
description: 'Lync Server 2013: Просмотр состояния глобальных параметров для леса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View status of global settings for a forest
ms:assetid: 2ab0f2f1-9908-4e6f-aff3-d6b3cc474b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747889(v=OCS.15)
ms:contentKeyID: 63969590
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9f722ea66f6c54c816703bd1af1d3def57bbd84
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443911"
---
# <a name="view-status-of-global-settings-for-a-forest-in-lync-server-2013"></a><span data-ttu-id="107cd-103">Просмотр состояния глобальных параметров для леса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="107cd-103">View status of global settings for a forest in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="107cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="107cd-104">

<span> </span></span></span>

<span data-ttu-id="107cd-105">_**Тема последнего изменения:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="107cd-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="107cd-106">Администраторам ежемесячно просматривайте глобальные параметры развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="107cd-106">Administrators should review the global settings for a Lync Server 2013 deployment monthly.</span></span> <span data-ttu-id="107cd-107">Цель состоит в том, чтобы проанализировать реализованные параметры для набора известных конфигураций — базовой конфигурации, чтобы гарантировать допустимость параметров, а также определить, следует ли обновлять базовую документацию.</span><span class="sxs-lookup"><span data-stu-id="107cd-107">The objective would be to review implemented settings against a set of known configurations—a baseline configuration to help guarantee that settings are valid and to determine whether the baseline documentation should be updated.</span></span> <span data-ttu-id="107cd-108">Изменения в глобальных параметрах должны быть реализованы с помощью процесса управления изменениями, который включает в себя документирование новых параметров.</span><span class="sxs-lookup"><span data-stu-id="107cd-108">Changes to global setting should be implemented through a Change Control process which should include documenting the new settings.</span></span>

<span data-ttu-id="107cd-109">Глобальные параметры, которые необходимо проверить, описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="107cd-109">Global settings that should be reviewed are described in the following sections:</span></span>

<div>

## <a name="check-general-settings"></a><span data-ttu-id="107cd-110">Проверка общих параметров</span><span class="sxs-lookup"><span data-stu-id="107cd-110">Check general settings</span></span>

<span data-ttu-id="107cd-111">Проверьте общие параметры, включая домены, поддерживаемые протоколом SIP для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="107cd-111">Check general settings, including the supported Session Initiation Protocol (SIP) domains for Lync Server 2013.</span></span>

<span data-ttu-id="107cd-112">Данные домена SIP можно вернуть с помощью Windows PowerShell и командлета **Get-CsSipDomain** .</span><span class="sxs-lookup"><span data-stu-id="107cd-112">SIP domain information can be returned by using Windows PowerShell and the **Get-CsSipDomain** cmdlet.</span></span> <span data-ttu-id="107cd-113">Чтобы вернуть эти данные, запустите `Get-CsSipDomain` команду Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="107cd-113">To return this information, run the `Get-CsSipDomain` Windows PowerShell command.</span></span>

<span data-ttu-id="107cd-114">Get-CsSipDomain будет возвращать такие сведения, как для всех авторизованных доменов SIP:</span><span class="sxs-lookup"><span data-stu-id="107cd-114">Get-CsSipDomain will return information similar to this for all the authorized SIP domains:</span></span>

<span data-ttu-id="107cd-115">Имя удостоверения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="107cd-115">Identity Name IsDefault</span></span>

<span data-ttu-id="107cd-116">\-------- ---- ---------</span><span class="sxs-lookup"><span data-stu-id="107cd-116">\-------- ---- ---------</span></span>

<span data-ttu-id="107cd-117">fabrikam.com fabrikam.com истина</span><span class="sxs-lookup"><span data-stu-id="107cd-117">fabrikam.com fabrikam.com True</span></span>

<span data-ttu-id="107cd-118">na.fabrikam.com na.fabrikam.com ложь</span><span class="sxs-lookup"><span data-stu-id="107cd-118">na.fabrikam.com na.fabrikam.com False</span></span>

<span data-ttu-id="107cd-119">Если для свойства по умолчанию задано значение "true", соответствующий домен является доменом SIP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="107cd-119">If the IsDefault property is set to True, the corresponding domain is your default SIP domain.</span></span> <span data-ttu-id="107cd-120">Вы можете использовать командлет Set-CsSipDomain для изменения домена SIP по умолчанию для Организации.</span><span class="sxs-lookup"><span data-stu-id="107cd-120">You can use the Set-CsSipDomain cmdlet to change the default SIP domain for your organization.</span></span> <span data-ttu-id="107cd-121">Однако вы не можете просто удалить стандартный домен SIP, так как это оставит без домена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="107cd-121">However, you can't just delete the default SIP domain because that would leave you without a default domain.</span></span> <span data-ttu-id="107cd-122">Если вы хотите удалить домен fabrikam.com (как показано в предыдущем примере), сначала необходимо настроить na.fabrikam.com в качестве домена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="107cd-122">If you wanted to delete the fabrikam.com domain (as shown in the previous example), you would first have to configure na.fabrikam.com to be your default domain.</span></span>

</div>

<div>

## <a name="check-meeting-settings"></a><span data-ttu-id="107cd-123">Проверка параметров собрания</span><span class="sxs-lookup"><span data-stu-id="107cd-123">Check meeting settings</span></span>

<span data-ttu-id="107cd-124">Параметры собрания включают определения политик собраний и поддержку участия анонимных пользователей в собраниях.</span><span class="sxs-lookup"><span data-stu-id="107cd-124">Meeting settings include meeting policy definitions and support for participation of anonymous users in meetings.</span></span>

<span data-ttu-id="107cd-125">Параметры конфигурации собраний можно получить с помощью Windows PowerShell и командлета **Get-CsMeetingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="107cd-125">Meeting configuration settings can be retrieved by using Windows PowerShell and the **Get-CsMeetingConfiguration** cmdlet.</span></span> <span data-ttu-id="107cd-126">Например, эта команда возвращает сведения о глобальных параметрах конфигурации собраний.</span><span class="sxs-lookup"><span data-stu-id="107cd-126">For example, this command returns information about the global meeting configuration settings:</span></span>

<span data-ttu-id="107cd-127">Параметры конфигурации собрания "Глобальный" Get-CsMeetingConfiguration также можно настроить в области сайта.</span><span class="sxs-lookup"><span data-stu-id="107cd-127">Get-CsMeetingConfiguration –Identity "Global"Meeting configuration settings can also be configured at the site scope.</span></span> <span data-ttu-id="107cd-128">По этой причине вы можете использовать следующую команду, которая возвращает сведения о всех параметрах конфигурации собраний.</span><span class="sxs-lookup"><span data-stu-id="107cd-128">Because of that, you might want to use the following command, which returns information about all the meeting configuration settings:</span></span>

`Get-CsMeetingConfiguration`

<span data-ttu-id="107cd-129">Командлет **Get-CsMeetingConfiguration** возвращает информацию, подобную приведенной ниже:</span><span class="sxs-lookup"><span data-stu-id="107cd-129">The **Get-CsMeetingConfiguration** cmdlet returns information similar to the following:</span></span>

<span data-ttu-id="107cd-130">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-130">Identity : Global</span></span>

<span data-ttu-id="107cd-131">PstnCallersBypassLobby: true</span><span class="sxs-lookup"><span data-stu-id="107cd-131">PstnCallersBypassLobby : True</span></span>

<span data-ttu-id="107cd-132">EnableAssignedConferenceType: true</span><span class="sxs-lookup"><span data-stu-id="107cd-132">EnableAssignedConferenceType : True</span></span>

<span data-ttu-id="107cd-133">DesignateAsPresenter: Company</span><span class="sxs-lookup"><span data-stu-id="107cd-133">DesignateAsPresenter : Company</span></span>

<span data-ttu-id="107cd-134">AssignedConferenceTypeByDefault: true</span><span class="sxs-lookup"><span data-stu-id="107cd-134">AssignedConferenceTypeByDefault : True</span></span>

<span data-ttu-id="107cd-135">AdmitAnonymousUsersByDefault: true</span><span class="sxs-lookup"><span data-stu-id="107cd-135">AdmitAnonymousUsersByDefault : True</span></span>

<span data-ttu-id="107cd-136">Кроме того, последний элемент в списке, **AdmitAnonymousUsersByDefault**, включает или отключает возможность анонимных пользователей принимать участие в собраниях.</span><span class="sxs-lookup"><span data-stu-id="107cd-136">Again, the final item in the list, **AdmitAnonymousUsersByDefault**, enables or disables the ability of anonymous users to participate in meetings.</span></span>

<span data-ttu-id="107cd-137">При проверке параметров конфигурации собрания может оказаться полезным сравнить текущие параметры с эквивалентами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="107cd-137">When checking meeting configuration settings, you might find it useful to compare the current settings against the default equivalents.</span></span> <span data-ttu-id="107cd-138">Вы можете просмотреть параметры конфигурации собрания по умолчанию, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="107cd-138">You can view the default meeting configuration settings by running the following command:</span></span>

`New-CsMeetingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="107cd-139">Предыдущая команда создает одновременный экземпляр глобальных параметров конфигурации собрания в памяти, экземпляр которого использует значение по умолчанию для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="107cd-139">The previous command creates an in-memory-only instance of the global meeting configuration settings, an instance that uses the default value for each property.</span></span> <span data-ttu-id="107cd-140">При выполнении команды не создаются фактические параметры конфигурации собраний.</span><span class="sxs-lookup"><span data-stu-id="107cd-140">No actual meeting configuration settings are created when you run the command.</span></span> <span data-ttu-id="107cd-141">Тем не менее, на экране будут отображаться все значения свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="107cd-141">However, all the default property values will be displayed on-screen.</span></span>

</div>

<div>

## <a name="check-edge-servers-and-their-settings"></a><span data-ttu-id="107cd-142">Проверка серверов пограничного сервера и их параметров</span><span class="sxs-lookup"><span data-stu-id="107cd-142">Check Edge Servers and their settings</span></span>

<span data-ttu-id="107cd-143">Данные пограничного сервера можно получить с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="107cd-143">Edge Server information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="107cd-144">Эта команда возвращает сведения о всех пограничных серверах, настроенных для использования в вашей организации:</span><span class="sxs-lookup"><span data-stu-id="107cd-144">This command returns information about all the Edge Servers configured for use in your organization:</span></span>

`Get-CsService -EdgeServer`

<span data-ttu-id="107cd-145">Возвращенные сведения включают все полные доменные значения и параметры порта для каждого пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="107cd-145">The returned information includes all of the FQDN and port settings for each Edge Server:</span></span>

<span data-ttu-id="107cd-146">Identity: EdgeServer: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="107cd-146">Identity : EdgeServer: dc.fabrikam.com</span></span>

<span data-ttu-id="107cd-147">Регистратор: регистратор: LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="107cd-147">Registrar : Registrar: LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="107cd-148">AccessEdgeInternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="107cd-148">AccessEdgeInternalSipPort : 5061</span></span>

<span data-ttu-id="107cd-149">AccessEdgeExternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="107cd-149">AccessEdgeExternalSipPort : 5061</span></span>

<span data-ttu-id="107cd-150">AccessEdgeClientPort: 443</span><span class="sxs-lookup"><span data-stu-id="107cd-150">AccessEdgeClientPort : 443</span></span>

<span data-ttu-id="107cd-151">DataPsomServerPort: 8057</span><span class="sxs-lookup"><span data-stu-id="107cd-151">DataPsomServerPort : 8057</span></span>

<span data-ttu-id="107cd-152">DataPsomClientPort: 444</span><span class="sxs-lookup"><span data-stu-id="107cd-152">DataPsomClientPort : 444</span></span>

<span data-ttu-id="107cd-153">MediaRelayAuthEdgePort: 5062</span><span class="sxs-lookup"><span data-stu-id="107cd-153">MediaRelayAuthEdgePort : 5062</span></span>

<span data-ttu-id="107cd-154">MediaRelayAuthInternalTurnTcpPort: 443</span><span class="sxs-lookup"><span data-stu-id="107cd-154">MediaRelayAuthInternalTurnTcpPort : 443</span></span>

<span data-ttu-id="107cd-155">MediaRelayAuthExternalTurnTcpPort: 445</span><span class="sxs-lookup"><span data-stu-id="107cd-155">MediaRelayAuthExternalTurnTcpPort : 445</span></span>

<span data-ttu-id="107cd-156">MediaRelayAuthInternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="107cd-156">MediaRelayAuthInternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="107cd-157">MediaRelayAuthExternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="107cd-157">MediaRelayAuthExternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="107cd-158">MediaCommunicationPortStart: 50000</span><span class="sxs-lookup"><span data-stu-id="107cd-158">MediaCommunicationPortStart : 50000</span></span>

<span data-ttu-id="107cd-159">MediaComunicationPortCount: 10000</span><span class="sxs-lookup"><span data-stu-id="107cd-159">MediaComunicationPortCount : 10000</span></span>

<span data-ttu-id="107cd-160">AccessEdgeExternalFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="107cd-160">AccessEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="107cd-161">DataEdgeExternalFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="107cd-161">DataEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="107cd-162">AVEdgeExternalFqdn :</span><span class="sxs-lookup"><span data-stu-id="107cd-162">AVEdgeExternalFqdn :</span></span>

<span data-ttu-id="107cd-163">InternalInterfaceFqdn :</span><span class="sxs-lookup"><span data-stu-id="107cd-163">InternalInterfaceFqdn :</span></span>

<span data-ttu-id="107cd-164">ExternalMrasFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="107cd-164">ExternalMrasFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="107cd-165">DependentServiceList: {регистратор: LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="107cd-165">DependentServiceList : {Registrar:LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="107cd-166">ConferencingServer: LYNC-SE. fabrikam</span><span class="sxs-lookup"><span data-stu-id="107cd-166">ConferencingServer:LYNC-SE.fabrikam</span></span>

<span data-ttu-id="107cd-167">com, MediationServer: LYNC-SE.</span><span class="sxs-lookup"><span data-stu-id="107cd-167">com, MediationServer:LYNC-SE.</span></span>

<span data-ttu-id="107cd-168">fabrikam.com}</span><span class="sxs-lookup"><span data-stu-id="107cd-168">fabrikam.com}</span></span>

<span data-ttu-id="107cd-169">ServiceId: fabrikam.com-EdgeServer-2</span><span class="sxs-lookup"><span data-stu-id="107cd-169">ServiceId : fabrikam.com-EdgeServer-2</span></span>

<span data-ttu-id="107cd-170">Идентификатор сайта: сайт:fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="107cd-170">SiteId : site:fabrikam.com</span></span>

<span data-ttu-id="107cd-171">PoolFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="107cd-171">PoolFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="107cd-172">Версия: 5</span><span class="sxs-lookup"><span data-stu-id="107cd-172">Version : 5</span></span>

<span data-ttu-id="107cd-173">Role (роль): EdgeServer</span><span class="sxs-lookup"><span data-stu-id="107cd-173">Role : EdgeServer</span></span>

<div>

## <a name="check-federation-settings"></a><span data-ttu-id="107cd-174">Проверка параметров Федерации</span><span class="sxs-lookup"><span data-stu-id="107cd-174">Check federation settings</span></span>

<span data-ttu-id="107cd-175">Установите флажки для параметров Федерации, например, настроены ли они, и, если вы ответили "Да", полное доменное имя и порт.</span><span class="sxs-lookup"><span data-stu-id="107cd-175">Check Federation settings, such as whether it is configured and, if the answer is "yes,", the FQDN and port.</span></span> <span data-ttu-id="107cd-176">Интеграция включена и отключена с помощью глобальной коллекции параметров конфигурации пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="107cd-176">Federation is enabled and disabled by using the global collection of Access Edge configuration settings.</span></span> <span data-ttu-id="107cd-177">Помимо прочего, это означает, что Федерация настроена на уровне "все" или "все". включена либо Федерация для всей Организации, либо Федерация отключена для всей Организации.</span><span class="sxs-lookup"><span data-stu-id="107cd-177">Among other things, these mean that federation is configured on an all-or-nothing basis: either federation is enabled for the whole organization or federation is disabled for the whole organization</span></span>

<span data-ttu-id="107cd-178">Параметры конфигурации Edge Access можно вернуть с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="107cd-178">Your Access Edge configuration settings can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="107cd-179">Для этого выполните следующую команду Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="107cd-179">To do that, run the following Windows PowerShell command:</span></span>

`Get-CsAccessEdgeConfiguration`

<span data-ttu-id="107cd-180">В свою очередь она возвращает данные примерно так:</span><span class="sxs-lookup"><span data-stu-id="107cd-180">In turn, that command will return data similar to this:</span></span>

<span data-ttu-id="107cd-181">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-181">Identity : Global</span></span>

<span data-ttu-id="107cd-182">AllowAnonymousUsers: false</span><span class="sxs-lookup"><span data-stu-id="107cd-182">AllowAnonymousUsers : False</span></span>

<span data-ttu-id="107cd-183">AllowFederatedUsers: false</span><span class="sxs-lookup"><span data-stu-id="107cd-183">AllowFederatedUsers : False</span></span>

<span data-ttu-id="107cd-184">AllowOutsideUsers: false</span><span class="sxs-lookup"><span data-stu-id="107cd-184">AllowOutsideUsers : False</span></span>

<span data-ttu-id="107cd-185">BeClearingHouse: false</span><span class="sxs-lookup"><span data-stu-id="107cd-185">BeClearingHouse : False</span></span>

<span data-ttu-id="107cd-186">EnablePartnerDiscovery: false</span><span class="sxs-lookup"><span data-stu-id="107cd-186">EnablePartnerDiscovery : False</span></span>

<span data-ttu-id="107cd-187">EnableArchivingDisclaimer: false</span><span class="sxs-lookup"><span data-stu-id="107cd-187">EnableArchivingDisclaimer : False</span></span>

<span data-ttu-id="107cd-188">KeepCrlsUpToDateForPeers: true</span><span class="sxs-lookup"><span data-stu-id="107cd-188">KeepCrlsUpToDateForPeers : True</span></span>

<span data-ttu-id="107cd-189">MarkSourceVerifiableOnOutgoingMessages: true</span><span class="sxs-lookup"><span data-stu-id="107cd-189">MarkSourceVerifiableOnOutgoingMessages : True</span></span>

<span data-ttu-id="107cd-190">OutgoingTlsCountForFederatedPartners: 4</span><span class="sxs-lookup"><span data-stu-id="107cd-190">OutgoingTlsCountForFederatedPartners : 4</span></span>

<span data-ttu-id="107cd-191">RoutingMethod : UseDnsSrvRouting</span><span class="sxs-lookup"><span data-stu-id="107cd-191">RoutingMethod : UseDnsSrvRouting</span></span>

<span data-ttu-id="107cd-192">Если для свойства **AllowFederatedUsers** задано значение "true", это означает, что для вашей организации включена Федерация.</span><span class="sxs-lookup"><span data-stu-id="107cd-192">If the **AllowFederatedUsers** property is set to True, that means that federation is enabled for your organization.</span></span> <span data-ttu-id="107cd-193">(Установка **AllowFederatedUsers** в true также означает, что в сценарии разделенного домена локальные пользователи смогут легко общаться с пользователями в облаке).</span><span class="sxs-lookup"><span data-stu-id="107cd-193">(Setting **AllowFederatedUsers** to True also means that, in a split domain scenario, your on-premises users will be able to communicate seamlessly with your in-the-cloud users.)</span></span>

<span data-ttu-id="107cd-194">Чтобы получить полные доменные имена и параметры порта для пограничного сервера, ознакомьтесь с предыдущими задачами (пограничные серверы и их параметры).</span><span class="sxs-lookup"><span data-stu-id="107cd-194">To retrieve the FQDN and port settings for your Edge Server, see the previous task (Edge Servers and their settings).</span></span>

<span data-ttu-id="107cd-195">Включение Федерации в глобальной области означает, что пользователи могут взаимодействовать с федеративными пользователями.</span><span class="sxs-lookup"><span data-stu-id="107cd-195">Enabling federation at the global scope only means that users can potentially communicate with federated users.</span></span> <span data-ttu-id="107cd-196">Чтобы определить, могут ли какие либо пользователи самим взаимодействовать с федеративными пользователями, необходимо проверить политику доступа внешних пользователей, назначенную для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="107cd-196">To determine whether any individual users can actually communicate with federated users requires you to examine the external user access policy assigned to that user.</span></span>

<span data-ttu-id="107cd-197">Сведения о внешнем пользовательском доступе можно вернуть с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="107cd-197">External user access information can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="107cd-198">Например, эта команда возвращает сведения о глобальной политике доступа внешних пользователей:</span><span class="sxs-lookup"><span data-stu-id="107cd-198">For example, this command returns information for the global external user access policy:</span></span>

`Get-CsExternalAccessPolicy -Identity "Global"`

<span data-ttu-id="107cd-199">Эта команда возвращает сведения обо всех внешних политиках доступа пользователей.</span><span class="sxs-lookup"><span data-stu-id="107cd-199">And this command returns information for all the external user access policies:</span></span>

`Get-CsExternalAccessPolicy`

<span data-ttu-id="107cd-200">Возвращенные сведения будут выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="107cd-200">The returned information will resemble this:</span></span>

<span data-ttu-id="107cd-201">Идентификация: ложь</span><span class="sxs-lookup"><span data-stu-id="107cd-201">Identity : False</span></span>

<span data-ttu-id="107cd-202">Nописание</span><span class="sxs-lookup"><span data-stu-id="107cd-202">Description :</span></span>

<span data-ttu-id="107cd-203">EnableFederationAccess: false</span><span class="sxs-lookup"><span data-stu-id="107cd-203">EnableFederationAccess : False</span></span>

<span data-ttu-id="107cd-204">EnablePublicCloudAccess: false</span><span class="sxs-lookup"><span data-stu-id="107cd-204">EnablePublicCloudAccess : False</span></span>

<span data-ttu-id="107cd-205">EnablePublicCloudAccessAudioVideoAccess: false</span><span class="sxs-lookup"><span data-stu-id="107cd-205">EnablePublicCloudAccessAudioVideoAccess : False</span></span>

<span data-ttu-id="107cd-206">EnableOutsideAccess: false</span><span class="sxs-lookup"><span data-stu-id="107cd-206">EnableOutsideAccess : False</span></span>

<span data-ttu-id="107cd-207">Если для **EnableFederationAccess** задано значение "true", пользователи, управляемые данной политикой, могут общаться с федеративными пользователями.</span><span class="sxs-lookup"><span data-stu-id="107cd-207">If **EnableFederationAccess** is set to True, then users managed by the given policy can communicate with federated users.</span></span>

</div>

</div>

<div>

## <a name="check-archiving-settings"></a><span data-ttu-id="107cd-208">Проверка параметров архивации</span><span class="sxs-lookup"><span data-stu-id="107cd-208">Check archiving settings</span></span>

<span data-ttu-id="107cd-209">Проверка параметров архивирования для внутренних и Федеративных коммуникаций. Перед проверкой параметров внутренних и внешних архиваций убедитесь, что архивация включена.</span><span class="sxs-lookup"><span data-stu-id="107cd-209">Check archiving settings for internal and federated communications.Before verifying the settings for internal and external archiving, you should verify that archiving is enabled.</span></span>

<span data-ttu-id="107cd-210">Параметры конфигурации архивации можно проверить с помощью Windows PowerShell и командлета Get-CsArchivingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="107cd-210">Archiving configuration settings can be verified by using Windows PowerShell and the Get-CsArchivingConfiguration cmdlet:</span></span>

`Get-CsArchivingConfiguration -Identity "Global"`

<span data-ttu-id="107cd-211">Обратите внимание, что параметры архивации также можно настроить в области сайта.</span><span class="sxs-lookup"><span data-stu-id="107cd-211">Note that archiving settings can also be configured at the site scope.</span></span> <span data-ttu-id="107cd-212">Чтобы получить сведения о всех параметрах архивации, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="107cd-212">To return information about all the archiving settings, use this command:</span></span>

`Get-CsArchivingConfiguration`

<span data-ttu-id="107cd-213">Командлет Get-CsArchivingConfiguration возвращает данные, подобные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="107cd-213">The Get-CsArchivingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="107cd-214">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-214">Identity : Global</span></span>

<span data-ttu-id="107cd-215">EnableArchiving: false</span><span class="sxs-lookup"><span data-stu-id="107cd-215">EnableArchiving : False</span></span>

<span data-ttu-id="107cd-216">EnablePurging: false</span><span class="sxs-lookup"><span data-stu-id="107cd-216">EnablePurging : False</span></span>

<span data-ttu-id="107cd-217">PurgeExportedArchivesOnly: false</span><span class="sxs-lookup"><span data-stu-id="107cd-217">PurgeExportedArchivesOnly : False</span></span>

<span data-ttu-id="107cd-218">BlockOnArchiveFailure: false</span><span class="sxs-lookup"><span data-stu-id="107cd-218">BlockOnArchiveFailure : False</span></span>

<span data-ttu-id="107cd-219">KeepArchivingDataForDays: 14</span><span class="sxs-lookup"><span data-stu-id="107cd-219">KeepArchivingDataForDays : 14</span></span>

<span data-ttu-id="107cd-220">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="107cd-220">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="107cd-221">ArchiveDuplicateMessages: true</span><span class="sxs-lookup"><span data-stu-id="107cd-221">ArchiveDuplicateMessages : True</span></span>

<span data-ttu-id="107cd-222">CachePurgingInterval: 24</span><span class="sxs-lookup"><span data-stu-id="107cd-222">CachePurgingInterval : 24</span></span>

<span data-ttu-id="107cd-223">Если свойство EnableArchiving имеет значение false, это означает, что сеансы связи не будут заархивированы.</span><span class="sxs-lookup"><span data-stu-id="107cd-223">If the EnableArchiving property is set to False, that means that no communication sessions will be archived.</span></span> <span data-ttu-id="107cd-224">Если вы хотите архивировать сеансы мгновенных сообщений, используйте следующую команду, чтобы включить архивацию сеансов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="107cd-224">If you want to archive instant messaging sessions only, use a command such as the following to enable the archiving of IM sessions:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="107cd-225">Для архивации сеансов конференций и сеансов обмена мгновенными сообщениями используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="107cd-225">To archive conferencing sessions and instant messaging sessions, use this command:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="107cd-226">Если вы хотите сравнить текущие параметры архивации с параметрами по умолчанию, выполните следующую команду Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="107cd-226">If you’d like to compare your current archiving settings with the default settings, run the following Windows PowerShell command:</span></span>

`New-CsArchivingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="107cd-227">Эта команда создает одновременный экземпляр глобальных параметров конфигурации архивации в памяти.</span><span class="sxs-lookup"><span data-stu-id="107cd-227">That command creates an in-memory-only instance of the global archiving configuration settings.</span></span> <span data-ttu-id="107cd-228">Это не является реальной коллекцией параметров, которые используются в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="107cd-228">This is not a real collection of settings that is used by Lync Server.</span></span> <span data-ttu-id="107cd-229">Тем не менее, в нем отображаются значения по умолчанию для всех свойств конфигурации архивации.</span><span class="sxs-lookup"><span data-stu-id="107cd-229">However, it does display the default values for all the archiving configuration properties.</span></span>

<span data-ttu-id="107cd-230">Вы также можете использовать эту команду, чтобы вернуть полные доменные имена серверов архивации.</span><span class="sxs-lookup"><span data-stu-id="107cd-230">You can also use this command to return the FQDN of your Archiving servers:</span></span>

`Get-CsService -ArchivingServer`

<span data-ttu-id="107cd-231">После того как вы убедитесь, что архивация включена, вы можете просмотреть политики архивации, чтобы определить, архивируются ли внутренние и внешние сеансы связи.</span><span class="sxs-lookup"><span data-stu-id="107cd-231">After you have verified that archiving is enabled, you can then view your archiving policies to determine whether internal and external communication sessions are being archived.</span></span>

<span data-ttu-id="107cd-232">Сведения о политике архивации можно получить с помощью командлета Get-CsArchivingPolicy.</span><span class="sxs-lookup"><span data-stu-id="107cd-232">Archiving policy information can be retrieved by using the Get-CsArchivingPolicy cmdlet.</span></span> <span data-ttu-id="107cd-233">Например, эта команда возвращает сведения о глобальной политике архивации.</span><span class="sxs-lookup"><span data-stu-id="107cd-233">For example, this command returns information about the global archiving policy:</span></span>

`Get-CsArchivingPolicy -Identity "Global"`

<span data-ttu-id="107cd-234">Поскольку политики архивации также можно настроить на сайте и на уровне пользователя, вам также может потребоваться использовать эту команду, которая возвращает сведения обо всех политиках архивации.</span><span class="sxs-lookup"><span data-stu-id="107cd-234">Because archiving policies can also be configured at the site and the per-user scope, you might also want to use this command, which returns information about all the archiving policies:</span></span>

`Get-CsArchivingPolicy`

<span data-ttu-id="107cd-235">Сведения, полученные от Get-CsArchivingPolicy, будут выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="107cd-235">The information that you receive from Get-CsArchivingPolicy will resemble this:</span></span>

<span data-ttu-id="107cd-236">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-236">Identity : Global</span></span>

<span data-ttu-id="107cd-237">Nописание</span><span class="sxs-lookup"><span data-stu-id="107cd-237">Description :</span></span>

<span data-ttu-id="107cd-238">ArchiveInternal: false</span><span class="sxs-lookup"><span data-stu-id="107cd-238">ArchiveInternal : False</span></span>

<span data-ttu-id="107cd-239">ArchiveExternal: false</span><span class="sxs-lookup"><span data-stu-id="107cd-239">ArchiveExternal : False</span></span>

<span data-ttu-id="107cd-240">Обратите внимание, что по умолчанию как внутренние, так и внешние архивации отключены в политике архивации.</span><span class="sxs-lookup"><span data-stu-id="107cd-240">Note that, by default, both internal and external archiving are disabled in an archiving policy.</span></span>

</div>

<div>

## <a name="check-cdr-settings"></a><span data-ttu-id="107cd-241">Проверка параметров CDR</span><span class="sxs-lookup"><span data-stu-id="107cd-241">Check CDR settings</span></span>

<span data-ttu-id="107cd-242">Установите флажок запись с подробными сведениями о звонке (CDR) для одноранговой сети, Конференции и записи голосовых вызовов.</span><span class="sxs-lookup"><span data-stu-id="107cd-242">Check Call Detail Record (CDR) settings for peer-to-peer, conferencing, and Voice call detail recording.</span></span> <span data-ttu-id="107cd-243">Подробные сведения о параметрах CDR можно вернуть с помощью командлета **Get-CsCdrConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="107cd-243">Detailed information about your CDR settings can be returned by using the **Get-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="107cd-244">Например, эта команда возвращает сведения о глобальной коллекции параметров конфигурации CDR:</span><span class="sxs-lookup"><span data-stu-id="107cd-244">For example, this command returns information about the global collection of CDR configuration settings:</span></span>

`Get-CsCdrConfiguration -Identity "Global"`

<span data-ttu-id="107cd-245">Так как CDR также можно настроить на уровне сайта, вы также можете запустить эту команду, которая возвращает сведения обо всех параметрах конфигурации CDR:</span><span class="sxs-lookup"><span data-stu-id="107cd-245">Because CDR can also be configured at the site scope, you might also want to run this command, which returns information about all the CDR configuration settings:</span></span>

`Get-CsCdrConfiguration`

<span data-ttu-id="107cd-246">Командлет Get-CsCdrConfiguration возвращает данные, подобные этим, для каждой коллекции параметров конфигурации CDR:</span><span class="sxs-lookup"><span data-stu-id="107cd-246">The Get-CsCdrConfiguration cmdlet returns information similar to this for each collection of CDR configuration settings:</span></span>

<span data-ttu-id="107cd-247">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-247">Identity : Global</span></span>

<span data-ttu-id="107cd-248">EnableCDR: true</span><span class="sxs-lookup"><span data-stu-id="107cd-248">EnableCDR : True</span></span>

<span data-ttu-id="107cd-249">EnablePurging: true</span><span class="sxs-lookup"><span data-stu-id="107cd-249">EnablePurging : True</span></span>

<span data-ttu-id="107cd-250">KeepCallDetailForDays: 60</span><span class="sxs-lookup"><span data-stu-id="107cd-250">KeepCallDetailForDays : 60</span></span>

<span data-ttu-id="107cd-251">KeepErrorReportForDays: 60</span><span class="sxs-lookup"><span data-stu-id="107cd-251">KeepErrorReportForDays : 60</span></span>

<span data-ttu-id="107cd-252">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="107cd-252">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="107cd-253">Аналогичные данные могут возвращаться для мониторинга QoE с помощью командлета Get-CsQoEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="107cd-253">Similar information can be returned for QoE monitoring by using the Get-CsQoEConfiguration cmdlet.</span></span> <span data-ttu-id="107cd-254">Например, эта команда возвращает сведения о глобальной коллекции параметров конфигурации QoE:</span><span class="sxs-lookup"><span data-stu-id="107cd-254">For example, this command returns information about the global collection of QoE configuration settings:</span></span>

`Get-QoEConfiguration -Identity "Global"`

<span data-ttu-id="107cd-255">Эти сведения будут выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="107cd-255">That information will resemble this:</span></span>

<span data-ttu-id="107cd-256">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-256">Identity : Global</span></span>

<span data-ttu-id="107cd-257">ExternalConsumerIssuedCertId :</span><span class="sxs-lookup"><span data-stu-id="107cd-257">ExternalConsumerIssuedCertId :</span></span>

<span data-ttu-id="107cd-258">EnablePurging: true</span><span class="sxs-lookup"><span data-stu-id="107cd-258">EnablePurging : True</span></span>

<span data-ttu-id="107cd-259">KeepQoEDataForDays: 60</span><span class="sxs-lookup"><span data-stu-id="107cd-259">KeepQoEDataForDays : 60</span></span>

<span data-ttu-id="107cd-260">PurgeHourOfDay: 1</span><span class="sxs-lookup"><span data-stu-id="107cd-260">PurgeHourOfDay : 1</span></span>

<span data-ttu-id="107cd-261">EnableExternalConsumer: false</span><span class="sxs-lookup"><span data-stu-id="107cd-261">EnableExternalConsumer : False</span></span>

<span data-ttu-id="107cd-262">ExternalConsumerName :</span><span class="sxs-lookup"><span data-stu-id="107cd-262">ExternalConsumerName :</span></span>

<span data-ttu-id="107cd-263">ExternalConsumerURL :</span><span class="sxs-lookup"><span data-stu-id="107cd-263">ExternalConsumerURL :</span></span>

<span data-ttu-id="107cd-264">EnableQoE: true</span><span class="sxs-lookup"><span data-stu-id="107cd-264">EnableQoE : True</span></span>

<span data-ttu-id="107cd-265">Если вы хотите сравнить текущие параметры CDR с параметрами CDR по умолчанию, можно просмотреть значения по умолчанию, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="107cd-265">If you want to compare your current CDR settings with the default CDR settings, the default values can be reviewed by running this command:</span></span>

`New-CsCdrConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="107cd-266">Также значения по умолчанию для мониторинга QoE можно получить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="107cd-266">Likewise, the default values for QoE monitoring can be retrieved by using this command:</span></span>

`New-CsQoEConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="107cd-267">Вы также можете вернуть полные доменные имена серверов мониторинга, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="107cd-267">You can also return the FQDN of your Monitoring servers by running this command:</span></span>

`Get-CsService -MonitoringServer`

</div>

<div>

## <a name="check-voice-settings"></a><span data-ttu-id="107cd-268">Проверка параметров голоса</span><span class="sxs-lookup"><span data-stu-id="107cd-268">Check voice settings</span></span>

<span data-ttu-id="107cd-269">Параметры голосовой связи, как правило, важны для администраторов в политиках голосовой связи и голосовых маршрутах: политики голосовой связи содержат параметры, определяющие возможности, доступные для отдельных пользователей (например, возможность пересылки или передачи), в то время как голосовые маршруты определяют, как звонки (и если) направляются по протоколу КТСОП.</span><span class="sxs-lookup"><span data-stu-id="107cd-269">The voice settings typically important to administrators are contained in voice policies and voice routes: voice policies contain the settings that determine the capabilities exposed to individual users (such as the ability to forward or transfer calls), while voice routes determine how (and if) calls are routed across the PSTN.</span></span>

<span data-ttu-id="107cd-270">Сведения о политике голосовой связи можно получить с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="107cd-270">Voice policy information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="107cd-271">Например, эта команда возвращает сведения о глобальной политике голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="107cd-271">For example, this command returns information about the global voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global"`

<span data-ttu-id="107cd-272">Эта команда возвращает сведения обо всех голосовых политиках, настроенных для использования в Организации.</span><span class="sxs-lookup"><span data-stu-id="107cd-272">And this command returns information about all the voice policies configured for use in the organization:</span></span>

`Get-CsVoicePolicy`

<span data-ttu-id="107cd-273">Данные, возвращаемые командлетом Get-CsVoicePolicy, похожи на приведенные ниже.</span><span class="sxs-lookup"><span data-stu-id="107cd-273">The information returned by the Get-CsVoicePolicy cmdlet resembles the following:</span></span>

<span data-ttu-id="107cd-274">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-274">Identity : Global</span></span>

<span data-ttu-id="107cd-275">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="107cd-275">PstnUsages : {}</span></span>

<span data-ttu-id="107cd-276">Nописание</span><span class="sxs-lookup"><span data-stu-id="107cd-276">Description :</span></span>

<span data-ttu-id="107cd-277">AllowSimulRing: true</span><span class="sxs-lookup"><span data-stu-id="107cd-277">AllowSimulRing : True</span></span>

<span data-ttu-id="107cd-278">AllowCallForwarding: true</span><span class="sxs-lookup"><span data-stu-id="107cd-278">AllowCallForwarding : True</span></span>

<span data-ttu-id="107cd-279">AllowPSTNReRouting: true</span><span class="sxs-lookup"><span data-stu-id="107cd-279">AllowPSTNReRouting : True</span></span>

<span data-ttu-id="107cd-280">Name (имя): DefaultPolicy</span><span class="sxs-lookup"><span data-stu-id="107cd-280">Name : DefaultPolicy</span></span>

<span data-ttu-id="107cd-281">EnableDelegation: true</span><span class="sxs-lookup"><span data-stu-id="107cd-281">EnableDelegation : True</span></span>

<span data-ttu-id="107cd-282">EnableTeamCall: true</span><span class="sxs-lookup"><span data-stu-id="107cd-282">EnableTeamCall : True</span></span>

<span data-ttu-id="107cd-283">EnableCallTransfer: true</span><span class="sxs-lookup"><span data-stu-id="107cd-283">EnableCallTransfer : True</span></span>

<span data-ttu-id="107cd-284">EnableCallPark: false</span><span class="sxs-lookup"><span data-stu-id="107cd-284">EnableCallPark : False</span></span>

<span data-ttu-id="107cd-285">EnableMaliciousCallTracing: false</span><span class="sxs-lookup"><span data-stu-id="107cd-285">EnableMaliciousCallTracing : False</span></span>

<span data-ttu-id="107cd-286">EnableBWPolicyOverride: false</span><span class="sxs-lookup"><span data-stu-id="107cd-286">EnableBWPolicyOverride : False</span></span>

<span data-ttu-id="107cd-287">PreventPSTNTollBypass: false</span><span class="sxs-lookup"><span data-stu-id="107cd-287">PreventPSTNTollBypass : False</span></span>

<span data-ttu-id="107cd-288">Вы также можете создавать запросы, которые возвращают подмножество политик голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="107cd-288">You can also create queries that returned a subset of your voice policies.</span></span> <span data-ttu-id="107cd-289">Например, эта команда возвращает все политики голосовой связи, которые разрешают переадресацию звонков.</span><span class="sxs-lookup"><span data-stu-id="107cd-289">For example, this command returns all the voice policies that allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $True}`

<span data-ttu-id="107cd-290">Эта команда возвращает все политики голосовой связи, не допускающие переадресацию звонков.</span><span class="sxs-lookup"><span data-stu-id="107cd-290">And this command returns all the voice policies that don’t allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $False}`

<span data-ttu-id="107cd-291">В Windows PowerShell используйте командлет Get-CsVoiceRouting, чтобы получить сведения о голосовых маршрутах.</span><span class="sxs-lookup"><span data-stu-id="107cd-291">In Windows PowerShell, use the Get-CsVoiceRouting cmdlet to return information about your voice routes:</span></span>

`Get-CsVoiceRoute`

<span data-ttu-id="107cd-292">Эта команда возвращает такие сведения, как, например, для всех голосовых маршрутов.</span><span class="sxs-lookup"><span data-stu-id="107cd-292">That command returns information such as this for all the voice routes:</span></span>

<span data-ttu-id="107cd-293">Identity: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="107cd-293">Identity : LocalRoute</span></span>

<span data-ttu-id="107cd-294">Priority (приоритет): 0</span><span class="sxs-lookup"><span data-stu-id="107cd-294">Priority : 0</span></span>

<span data-ttu-id="107cd-295">Nописание</span><span class="sxs-lookup"><span data-stu-id="107cd-295">Description :</span></span>

<span data-ttu-id="107cd-296">NumberPattern: ^ ( \\ + 1 \[ 0-9 \] {10} ) $</span><span class="sxs-lookup"><span data-stu-id="107cd-296">NumberPattern : ^(\\+1\[0-9\]{10})$</span></span>

<span data-ttu-id="107cd-297">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="107cd-297">PstnUsages : {}</span></span>

<span data-ttu-id="107cd-298">PstnGatewayList : {}</span><span class="sxs-lookup"><span data-stu-id="107cd-298">PstnGatewayList : {}</span></span>

<span data-ttu-id="107cd-299">Name (имя): LocalRoute</span><span class="sxs-lookup"><span data-stu-id="107cd-299">Name : LocalRoute</span></span>

<span data-ttu-id="107cd-300">SuppressCallerId :</span><span class="sxs-lookup"><span data-stu-id="107cd-300">SuppressCallerId :</span></span>

<span data-ttu-id="107cd-301">AlternateCallerId :</span><span class="sxs-lookup"><span data-stu-id="107cd-301">AlternateCallerId :</span></span>

<span data-ttu-id="107cd-302">Lync Server позволяет создавать маршруты голосовой связи, для которых не используется PSTN, и не указывать шлюз PSTN.</span><span class="sxs-lookup"><span data-stu-id="107cd-302">Lync Server allows you to create voice routes that do not have a PSTN usage and do not specify a PSTN gateway.</span></span> <span data-ttu-id="107cd-303">Однако вы не можете перенаправлять звонки через голосовой маршрут, для которого не настроены эти два значения свойств.</span><span class="sxs-lookup"><span data-stu-id="107cd-303">However, you can't actually route calls over a voice route that does not have these two property values configured.</span></span> <span data-ttu-id="107cd-304">По этой причине вам может понадобиться периодически запускать эту команду, которая возвращает идентификационные данные любого маршрута голосовой связи, для которого не используется PSTN.</span><span class="sxs-lookup"><span data-stu-id="107cd-304">Because of that, you might find it useful to periodically run this command, which returns the identity of any voice route that does not have a PSTN usage:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnUsages -eq $Null} | Select-Object Identity`

<span data-ttu-id="107cd-305">Аналогичным образом эта команда возвращает идентификационные данные любого маршрута голосовой связи, для которого не настроен шлюз PSTN.</span><span class="sxs-lookup"><span data-stu-id="107cd-305">Similarly, this command returns the identity of any voice route that has not been configured to have a PSTN gateway:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnGatewayList -eq $Null}} | Select-Object Identity`

</div>

<div>

## <a name="check-conferencing-attendant-settings"></a><span data-ttu-id="107cd-306">Проверка параметров помощника по конференциям</span><span class="sxs-lookup"><span data-stu-id="107cd-306">Check Conferencing Attendant settings</span></span>

<span data-ttu-id="107cd-307">Проверьте параметры помощника по конференциям для конференц-связи с телефонным подключением PSTN.</span><span class="sxs-lookup"><span data-stu-id="107cd-307">Check conferencing Attendant settings for PSTN dial-in conferencing.</span></span> <span data-ttu-id="107cd-308">Параметры помощника по конференциям можно получить только с помощью командлета **Get-CsDialInConferencingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="107cd-308">Conferencing Attendant settings can only be retrieved by using the **Get-CsDialInConferencingConfiguration** cmdlet.</span></span> <span data-ttu-id="107cd-309">Эти параметры недоступны на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="107cd-309">These settings are not available in the Lync Server Control Panel.</span></span> <span data-ttu-id="107cd-310">Чтобы просмотреть параметры помощника по конференциям, используйте команду Windows PowerShell, как показано ниже, и возвращающая глобальную коллекцию параметров конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="107cd-310">To view your Conferencing Attendant settings, use a Windows PowerShell command similar to the following, which returns the global collection of Conferencing Attendant settings:</span></span>

`Get-CsDialInConferencingConfiguration -Identity "Global"`

<span data-ttu-id="107cd-311">Обратите внимание, что параметры помощника по конференциям также можно настроить в области сайта.</span><span class="sxs-lookup"><span data-stu-id="107cd-311">Note that Conferencing Attendant settings can also be configured at the site scope.</span></span> <span data-ttu-id="107cd-312">Чтобы получить сведения о всех параметрах помощника по конференциям, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="107cd-312">To return information about all the Conferencing Attendant settings, use this command instead:</span></span>

`Get-CsDialInConferencingConfiguration`

<span data-ttu-id="107cd-313">Командлет Get-CsDialInConferencingConfiguration возвращает данные, подобные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="107cd-313">The Get-CsDialInConferencingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="107cd-314">Идентификация: Глобальная</span><span class="sxs-lookup"><span data-stu-id="107cd-314">Identity : Global</span></span>

<span data-ttu-id="107cd-315">EntryExitAnnouncementsType : UseNames</span><span class="sxs-lookup"><span data-stu-id="107cd-315">EntryExitAnnouncementsType : UseNames</span></span>

<span data-ttu-id="107cd-316">EnableNameRecording: true</span><span class="sxs-lookup"><span data-stu-id="107cd-316">EnableNameRecording : True</span></span>

<span data-ttu-id="107cd-317">EntryExitAnnouncementsEnabledByDefault: false</span><span class="sxs-lookup"><span data-stu-id="107cd-317">EntryExitAnnouncementsEnabledByDefault : False</span></span>

<span data-ttu-id="107cd-318">Если для EntryExitAnnouncementsEnabledByDefault задано значение false, объявления конференций отключены.</span><span class="sxs-lookup"><span data-stu-id="107cd-318">If EntryExitAnnouncementsEnabledByDefault is set to False, that means the conferencing announcements are disabled.</span></span> <span data-ttu-id="107cd-319">Чтобы включить объявления входа и выхода, выполните команду Windows PowerShell, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="107cd-319">To enable entry and exit announcements, run a Windows PowerShell command similar to this:</span></span>

`Set-CsDialInConferencingConfiguration -Identity "Global" -EntryExitAnnouncementsEnabledByDefault $True`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="107cd-320">См. также</span><span class="sxs-lookup"><span data-stu-id="107cd-320">See Also</span></span>


[<span data-ttu-id="107cd-321">Get-CsSipDomain</span><span class="sxs-lookup"><span data-stu-id="107cd-321">Get-CsSipDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsSipDomain)  
[<span data-ttu-id="107cd-322">Get-CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="107cd-322">Get-CsMeetingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration)  
[<span data-ttu-id="107cd-323">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="107cd-323">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="107cd-324">Get-CsAccessEdgeConfiguration</span><span class="sxs-lookup"><span data-stu-id="107cd-324">Get-CsAccessEdgeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAccessEdgeConfiguration)  
[<span data-ttu-id="107cd-325">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="107cd-325">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="107cd-326">Get-CsArchivingConfiguration</span><span class="sxs-lookup"><span data-stu-id="107cd-326">Get-CsArchivingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsArchivingConfiguration)  
[<span data-ttu-id="107cd-327">Get-CsCdrConfiguration</span><span class="sxs-lookup"><span data-stu-id="107cd-327">Get-CsCdrConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration)  
[<span data-ttu-id="107cd-328">Get-CsQoEConfiguration</span><span class="sxs-lookup"><span data-stu-id="107cd-328">Get-CsQoEConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsQoEConfiguration)  
[<span data-ttu-id="107cd-329">Get-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="107cd-329">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="107cd-330">Get-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="107cd-330">Get-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoiceRoute)  
[<span data-ttu-id="107cd-331">Get-CsDialInConferencingConfiguration</span><span class="sxs-lookup"><span data-stu-id="107cd-331">Get-CsDialInConferencingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingConfiguration)  
  

<span data-ttu-id="107cd-332"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="107cd-332"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

