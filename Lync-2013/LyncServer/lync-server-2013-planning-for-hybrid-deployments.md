---
title: 'Lync Server 2013: планирование гибридного развертывания'
description: 'Lync Server 2013: планирование гибридного развертывания.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424550"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="6bd89-103">Планирование гибридного развертывания Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6bd89-103">Planning for Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bd89-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bd89-104">

<span> </span></span></span>

<span data-ttu-id="6bd89-105">_**Тема последнего изменения:** 25.05.2016_</span><span class="sxs-lookup"><span data-stu-id="6bd89-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="6bd89-106">При планировании гибридного развертывания необходимо учесть следующие требования для пользователей и вашей сетевой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="6bd89-106">You should consider the following requirements for users and your network infrastructure while planning for a hybrid deployment.</span></span>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="6bd89-107">Требования к инфраструктуре</span><span class="sxs-lookup"><span data-stu-id="6bd89-107">Infrastructure Requirements</span></span>

<span data-ttu-id="6bd89-108">Для реализации и развертывания гибридного развертывания в вашей среде должны быть настроены следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="6bd89-108">You must have the following configured in your environment in order to implement and deploy a hybrid deployment.</span></span>

  - <span data-ttu-id="6bd89-109">Организация Microsoft 365 или Office 365 с включенной службой Skype для бизнеса Online.</span><span class="sxs-lookup"><span data-stu-id="6bd89-109">A Microsoft 365 or Office 365 organization with Skype for Business Online enabled.</span></span> <span data-ttu-id="6bd89-110">Имейте в виду, что в гибридной конфигурации с локальной конфигурацией можно использовать только один клиент.</span><span class="sxs-lookup"><span data-stu-id="6bd89-110">Note that you can use only a single tenant for a hybrid configuration with your on-premises deployment.</span></span>

  - <span data-ttu-id="6bd89-111">Одно локальное развертывание (инфраструктура) Skype для бизнеса Server или Lync Server, развернутого в поддерживаемой топологии.</span><span class="sxs-lookup"><span data-stu-id="6bd89-111">A single on-premises deployment (infrastructure) of Skype for Business Server or Lync Server that is deployed in a supported topology.</span></span> <span data-ttu-id="6bd89-112">См. требования к топологии.</span><span class="sxs-lookup"><span data-stu-id="6bd89-112">See Topology Requirements.</span></span>
    
    <span data-ttu-id="6bd89-113">Сведения о настройке развертывания Lync Server 2013 или Lync Server 2010 для гибридного развертывания см. в гибридных развертываниях [Lync Server 2013.](lync-server-2013-configuring-hybrid-deployments.md)</span><span class="sxs-lookup"><span data-stu-id="6bd89-113">For information about configuring your Lync Server 2013 or Lync Server 2010 deployment for hybrid, see [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span></span>

  - <span data-ttu-id="6bd89-114">Средства администрирования Skype для бизнеса Server 2015.</span><span class="sxs-lookup"><span data-stu-id="6bd89-114">Skype for Business Server 2015 administrative tools.</span></span> <span data-ttu-id="6bd89-115">Если вы используете Lync Server 2013 или Lync Server 2010, вы можете использовать средства администрирования Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6bd89-115">If you are using Lync Server 2013 or Lync Server 2010, you can use the Lync Server 2013 administrative tools.</span></span>

  - <span data-ttu-id="6bd89-116">Для поддержки единого входа в Microsoft 365 или Office 365, чтобы пользователи могли использовать те же учетные данные для входа в Office, что и в локальной службе, вы можете использовать функции синхронизации паролей Azure Active Directory (AAD) Connect.</span><span class="sxs-lookup"><span data-stu-id="6bd89-116">To support Single Sign-on with Microsoft 365 or Office 365 so that users can use the same login credentials for signing in to Office as they do on-premises, you can use the password sync features of Azure Active Directory (AAD) Connect.</span></span> <span data-ttu-id="6bd89-117">Вы также можете использовать службы федерации Active Directory (AD FS) для единого регистрации в Microsoft 365 или Office 365.</span><span class="sxs-lookup"><span data-stu-id="6bd89-117">You can also use Active Directory Federation Services (AD FS) for single sign-on with Microsoft 365 or Office 365.</span></span>
    
    <span data-ttu-id="6bd89-118">Дополнительные сведения см. в дополнительных сведениях об интеграции локального удостоверения [с Azure Active Directory.](https://go.microsoft.com/fwlink/p/?linkid=619754)</span><span class="sxs-lookup"><span data-stu-id="6bd89-118">For more information, see [Integrating your on-premises identities with Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span></span>

  - <span data-ttu-id="6bd89-119">Единое решение для синхронизации локальной и сетевой службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6bd89-119">A single directory synchronization solution to keep your on-premises and online Active Directory objects synchronized.</span></span> <span data-ttu-id="6bd89-120">Подробные сведения о синхронизации каталогов см. в инструментах [интеграции каталогов.](https://go.microsoft.com/fwlink/p/?linkid=530320)</span><span class="sxs-lookup"><span data-stu-id="6bd89-120">For details about Directory Synchronization, see [Directory Integration Tools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span></span>

</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="6bd89-121">Поддержка клиентов Lync</span><span class="sxs-lookup"><span data-stu-id="6bd89-121">Lync Client Support</span></span>

<span data-ttu-id="6bd89-122">Функции, поддерживаемые в клиентах Lync, а также функции, доступные в локальной и сетевой средах, немного отличаются.</span><span class="sxs-lookup"><span data-stu-id="6bd89-122">There are some differences in the features supported in Lync clients, as well as the features available in on-premises and online environments.</span></span> <span data-ttu-id="6bd89-123">Прежде чем выбрать расположение для домашнего пользователя, можно просмотреть поддержку клиентов для различных конфигураций Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6bd89-123">Before you decide where you want to home users in your organization, you can view the client support for the various configurations of Lync Server.</span></span> <span data-ttu-id="6bd89-124">В гибридном развертывании Lync поддерживаются следующие клиенты Skype для бизнеса Online:</span><span class="sxs-lookup"><span data-stu-id="6bd89-124">The following clients are supported with Skype for Business Online in a Lync hybrid deployment:</span></span>

  - <span data-ttu-id="6bd89-125">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="6bd89-125">Lync 2010</span></span>

  - <span data-ttu-id="6bd89-126">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="6bd89-126">Lync 2013</span></span>

  - <span data-ttu-id="6bd89-127">Приложение Lync из Магазина Windows</span><span class="sxs-lookup"><span data-stu-id="6bd89-127">Lync Windows Store app</span></span>

  - <span data-ttu-id="6bd89-128">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="6bd89-128">Lync Web App</span></span>

  - <span data-ttu-id="6bd89-129">Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="6bd89-129">Lync Mobile</span></span>

  - <span data-ttu-id="6bd89-130">Lync для Mac 2011</span><span class="sxs-lookup"><span data-stu-id="6bd89-130">Lync for Mac 2011</span></span>

  - <span data-ttu-id="6bd89-131">Lync Room System</span><span class="sxs-lookup"><span data-stu-id="6bd89-131">Lync Room System</span></span>

  - <span data-ttu-id="6bd89-132">Lync Basic 2013</span><span class="sxs-lookup"><span data-stu-id="6bd89-132">Lync Basic 2013</span></span>

<span data-ttu-id="6bd89-133">Подробные сведения о поддержке клиентов см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="6bd89-133">For details about client support, see the following topics:</span></span>

  - [<span data-ttu-id="6bd89-134">Клиенты для Lync Online</span><span class="sxs-lookup"><span data-stu-id="6bd89-134">Clients for Lync Online</span></span>](https://go.microsoft.com/fwlink/?linkid=281902)

  - [<span data-ttu-id="6bd89-135">Таблица сравнения клиентов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6bd89-135">Client comparison tables for Lync Server 2013</span></span>](lync-server-2013-desktop-client-comparison-tables.md)

  - [<span data-ttu-id="6bd89-136">Таблицы сравнения мобильных клиентов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6bd89-136">Mobile client comparison tables for Lync Server 2013</span></span>](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="6bd89-137">Требования к топологии</span><span class="sxs-lookup"><span data-stu-id="6bd89-137">Topology Requirements</span></span>

<span data-ttu-id="6bd89-138">Чтобы настроить гибридное развертывание со Skype для бизнеса Online, вам потребуется одна из следующих поддерживаемых топорологий:</span><span class="sxs-lookup"><span data-stu-id="6bd89-138">To configure your deployment for hybrid with Skype for Business Online, you need to have one of the following supported topologies:</span></span>

  - <span data-ttu-id="6bd89-139">Развертывание Skype для бизнеса Server 2015 со всеми серверами под управлением Skype для бизнеса Server 2015.</span><span class="sxs-lookup"><span data-stu-id="6bd89-139">A Skype for Business Server 2015 deployment with all servers running Skype for Business Server 2015.</span></span>

  - <span data-ttu-id="6bd89-140">Развертывание Lync Server 2013 со всеми серверами с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6bd89-140">A Lync Server 2013 deployment with all servers running Lync Server 2013.</span></span>

  - <span data-ttu-id="6bd89-141">Развертывание Lync Server 2010 со всеми серверами с Lync Server 2010 с последними накопительными обновлениями.</span><span class="sxs-lookup"><span data-stu-id="6bd89-141">A Lync Server 2010 deployment with all servers running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="6bd89-142">Для Lync Server 2010 с последним накопительным совокупным обновлением сервер федерации и сервер следующего перехода из сервера федерации должны быть запущены.</span><span class="sxs-lookup"><span data-stu-id="6bd89-142">The federation Edge Server and next hop server from the federation Edge Server must be running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="6bd89-143">Средства администрирования Skype для бизнеса Server 2015 или Lync Server 2013 должны быть установлены по крайней мере на одном сервере или рабочей станции управления.</span><span class="sxs-lookup"><span data-stu-id="6bd89-143">The Skype for Business Server 2015 or Lync Server 2013 Administrative Tools must be installed on at least one server or management workstation.</span></span>

  - <span data-ttu-id="6bd89-144">Смешанное развертывание Lync Server 2013 и Skype для бизнеса Server 2015 со следующими ролями сервера хотя бы на одном сайте со Skype для бизнеса Server 2015:</span><span class="sxs-lookup"><span data-stu-id="6bd89-144">A mixed Lync Server 2013 and Skype for Business Server 2015 deployment with the following server roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="6bd89-145">как минимум один пул серверов Enterprise Edition или Standard Edition; </span><span class="sxs-lookup"><span data-stu-id="6bd89-145">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="6bd89-146">пул директоров, связанный с федерацией SIP (при наличии);</span><span class="sxs-lookup"><span data-stu-id="6bd89-146">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="6bd89-147">пул пограничных серверов, связанный с федерацией SIP.</span><span class="sxs-lookup"><span data-stu-id="6bd89-147">The Edge Pool associated with SIP federation</span></span>

  - <span data-ttu-id="6bd89-148">Смешанное развертывание Lync Server 2010 и Skype для бизнеса Server 2015 со следующими ролями серверов хотя бы на одном сайте со Skype для бизнеса Server 2015:</span><span class="sxs-lookup"><span data-stu-id="6bd89-148">A mixed Lync Server 2010 and Skype for Business Server 2015 deployment with the following servers roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="6bd89-149">как минимум один пул серверов Enterprise Edition или Standard Edition; </span><span class="sxs-lookup"><span data-stu-id="6bd89-149">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="6bd89-150">пул директоров, связанный с федерацией SIP (при наличии);</span><span class="sxs-lookup"><span data-stu-id="6bd89-150">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="6bd89-151">пул пограничных серверов, связанный с федерацией SIP для сайта.</span><span class="sxs-lookup"><span data-stu-id="6bd89-151">The Edge Pool associated with SIP federation for the Site</span></span>

  - <span data-ttu-id="6bd89-152">Смешанное развертывание Lync Server 2010 и Lync Server 2013 с следующими ролями сервера хотя бы на одном сайте с Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="6bd89-152">A mixed Lync Server 2010 and Lync Server 2013 deployment with the following server roles in at least one site running Lync Server 2013:</span></span>
    
      - <span data-ttu-id="6bd89-153">как минимум один пул серверов Enterprise Edition или Standard Edition на сайте;</span><span class="sxs-lookup"><span data-stu-id="6bd89-153">At least one Enterprise Pool or Standard Edition server in the site</span></span>
    
      - <span data-ttu-id="6bd89-154">пул директоров, связанный с федерацией SIP (при наличии на сайте);</span><span class="sxs-lookup"><span data-stu-id="6bd89-154">The Director Pool associated with SIP federation, if it exists in the site</span></span>
    
      - <span data-ttu-id="6bd89-155">пул пограничных серверов, связанный с федерацией SIP для сайта.</span><span class="sxs-lookup"><span data-stu-id="6bd89-155">The Edge Pool associated with SIP federation for the site</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6bd89-156">Управление всеми пользователями, включая перемещение пользователей между локальной UNRESOLVED_TOKEN_VAL (skypeforbusiness) Online, необходимо делать с помощью последней установленной версии средств администрирования.</span><span class="sxs-lookup"><span data-stu-id="6bd89-156">All user management, including user moves between on-premises and UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, needs to be done using the latest installed version of the administrative tools.</span></span> <span data-ttu-id="6bd89-157">Средства администрирования должны быть установлены на отдельном сервере, который имеет доступ к существующему локальному развертыванию и Интернету.</span><span class="sxs-lookup"><span data-stu-id="6bd89-157">The administrative tools must be installed on a separate server that has connect access to the existing on-premises deployment and to the Internet.</span></span> <span data-ttu-id="6bd89-158">Для <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">перемещения</A> пользователей из локального развертывания в UNRESOLVED_TOKEN_VAL(skype16_online) необходимо использовать средства администрирования, подключенные к локальному развертыванию.</span><span class="sxs-lookup"><span data-stu-id="6bd89-158">The <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet to move users from your on-premises deployment to UNRESOLVED_TOKEN_VAL(skype16_online) must be run from the administrative tools connected to your on-premises deployment.</span></span>



</div>

<span data-ttu-id="6bd89-159">Дополнительные сведения о поддерживаемых топологи см. в поддерживаемых топорологах [в Lync Server 2013](lync-server-2013-supported-topologies.md)и [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments.](https://go.microsoft.com/fwlink/p/?linkid=398709)</span><span class="sxs-lookup"><span data-stu-id="6bd89-159">For more information about supported topologies, see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md), and [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments](https://go.microsoft.com/fwlink/p/?linkid=398709).</span></span>

<span data-ttu-id="6bd89-160">Сведения об устранении неполадок с гибридными развертываниями и подключении PowerShell к Lync Online см. в [Lync Online: Lync PowerShell и гибридное устранение неполадок.](https://go.microsoft.com/fwlink/p/?linkid=306718)</span><span class="sxs-lookup"><span data-stu-id="6bd89-160">For troubleshooting information about hybrid deployments and connecting PowerShell to Lync Online, see [Lync Online: Lync PowerShell and Hybrid Troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span></span>

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a><span data-ttu-id="6bd89-161">Требования для списков разрешенных и заблокированных федерации</span><span class="sxs-lookup"><span data-stu-id="6bd89-161">Requirements for Federation Allowed/Blocked Lists</span></span>

<span data-ttu-id="6bd89-p108">В список разрешенных доменов включены домены, для которых задано полное доменное имя пограничного сервера-партнера. Иногда они также называются *разрешенными серверами-партнерами* или *прямыми партнерами федерации*. Следует понимать различие между открытой и закрытой федерацией, которые в локальных развертываниях также называются соответственно *обнаружением партнера* и *списком разрешенных доменов-партнеров*.</span><span class="sxs-lookup"><span data-stu-id="6bd89-p108">The Allowed domains list includes domains that have a partner Edge fully qualified domain name (FQDN) configured. These are sometimes referred to as *allowed partner servers* or *direct federation partners*. You should be familiar with the difference between Open Federation and Closed Federation, referred to as *partner discovery* and *allowed partner domain list*, respectively, in on-premises deployments.</span></span>

<span data-ttu-id="6bd89-165">Для успешного настройки гибридного развертывания необходимо соблюдение следующих требований:</span><span class="sxs-lookup"><span data-stu-id="6bd89-165">The following requirements must be met to successfully configure a hybrid deployment:</span></span>

  - <span data-ttu-id="6bd89-166">Для локального развертывания и организации Microsoft 365 или Office 365 должно быть настроено одинаковое соответствие доменов.</span><span class="sxs-lookup"><span data-stu-id="6bd89-166">Domain matching must be configured the same for your on-premises deployment and your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="6bd89-167">Если в локальном развертывании включено обнаружение партнеров, для интерактивного клиента должна быть настроена открытая федерация.</span><span class="sxs-lookup"><span data-stu-id="6bd89-167">If partner discovery is enabled on the on-premises deployment, then open federation must be configured for your online tenant.</span></span> <span data-ttu-id="6bd89-168">Если обнаружение партнеров отключено, для интерактивного клиента должна быть настроена закрытая федерация.</span><span class="sxs-lookup"><span data-stu-id="6bd89-168">If partner discovery is not enabled, then closed federation must be configured for your online tenant.</span></span>

  - <span data-ttu-id="6bd89-169">Список заблокированных доменов в локальном развертывании должен полностью совпадать со списком заблокированных доменов для интерактивного клиента.</span><span class="sxs-lookup"><span data-stu-id="6bd89-169">The Blocked domains list in the on-premises deployment must exactly match the Blocked domains list for your online tenant.</span></span>

  - <span data-ttu-id="6bd89-170">Список разрешенных доменов в локальном развертывании должен полностью совпадать со списком разрешенных доменов для интерактивного клиента.</span><span class="sxs-lookup"><span data-stu-id="6bd89-170">The Allowed domains list in the on-premises deployment must exactly match the Allowed domains list for your online tenant.</span></span>

  - <span data-ttu-id="6bd89-171">Для сетевого клиента, настроенного с помощью панели управления Lync Online, должна быть включена федерация для внешней связи.</span><span class="sxs-lookup"><span data-stu-id="6bd89-171">Federation must be enabled for the external communications for the online tenant, which is configured by using the Lync Online Control Panel.</span></span>

</div>

<div>

## <a name="dns-settings"></a><span data-ttu-id="6bd89-172">Параметры DNS</span><span class="sxs-lookup"><span data-stu-id="6bd89-172">DNS Settings</span></span>

<span data-ttu-id="6bd89-173">При создании записей DNS для гибридного развертывания все внешние записи DNS Lync должны указать на локальное развертывание.</span><span class="sxs-lookup"><span data-stu-id="6bd89-173">When creating DNS records for hybrid deployments, all Lync external DNS records should point to the on-premises infrastructure.</span></span> <span data-ttu-id="6bd89-174">Подробные сведения о необходимых записях DNS см. в требованиях к системе доменных имен [(DNS) для Lync Server 2013.](lync-server-2013-domain-name-system-dns-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="6bd89-174">For details on required DNS records, please refer to [Domain Name System (DNS) requirements for Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span></span>

<span data-ttu-id="6bd89-175">Кроме того, обязательно убедитесь, что описанное в таблице ниже разрешение DNS работает в вашем локальном развертывании.</span><span class="sxs-lookup"><span data-stu-id="6bd89-175">Additionally you need to ensure that the DNS resolution described in the following table works in your on-premises deployment:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bd89-176">Запись DNS</span><span class="sxs-lookup"><span data-stu-id="6bd89-176">DNS record</span></span></p></td>
<td><p><span data-ttu-id="6bd89-177">Кем разрешено</span><span class="sxs-lookup"><span data-stu-id="6bd89-177">Resolvable by</span></span></p></td>
<td><p><span data-ttu-id="6bd89-178">Требование DNS</span><span class="sxs-lookup"><span data-stu-id="6bd89-178">DNS requirement</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bd89-179">Запись SRV DNS для _sipfederationtls._tcp. &lt; sipdomain.com &gt; для всех поддерживаемых доменов SIP, разрешающих внешние IP-адреса Access Edge</span><span class="sxs-lookup"><span data-stu-id="6bd89-179">DNS SRV record for _sipfederationtls._tcp.&lt;sipdomain.com&gt; for all supported SIP domains resolving to Access Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="6bd89-180">Пограничные серверы</span><span class="sxs-lookup"><span data-stu-id="6bd89-180">Edge server(s)</span></span></p></td>
<td><p><span data-ttu-id="6bd89-p111">Включите федеративное подключение в гибридной конфигурации. Пограничному серверу необходимо знать, куда направлять федеративный трафик для домена SIP, который разделяется на локальный и сетевой.</span><span class="sxs-lookup"><span data-stu-id="6bd89-p111">Enable federated communication in a hybrid configuration. The Edge Server needs to know where to route federated traffic for the SIP domain that is split between on premises and online.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bd89-183">Записи DNS A для полного доменного имени пограничной службы веб-конференций, например, webcon.contoso.com, разрешается во внешние IP-адреса пограничного сервера веб-конференций</span><span class="sxs-lookup"><span data-stu-id="6bd89-183">DNS A record(s) for Edge Web Conferencing Service FQDN, e.g. webcon.contoso.com resolving to Web Conferencing Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="6bd89-184">Компьютеры пользователей, подключенные к внутренней корпоративной сети</span><span class="sxs-lookup"><span data-stu-id="6bd89-184">Internal corporate network connected users’ computers</span></span></p></td>
<td><p><span data-ttu-id="6bd89-p112">Включите для пользователей в сети возможность представлять или просматривать содержимое во время собраний, которые проводятся локально. К содержимому относятся файлы PowerPoint, доски, опросы и общие заметки. </span><span class="sxs-lookup"><span data-stu-id="6bd89-p112">Enable online users to present or view content in on-premises hosted meetings. Content includes PowerPoint files, whiteboards, polls, and shared notes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6bd89-187">В зависимости от настройки DNS в вашей организации может потребоваться добавить эти записи во внутреннюю зону DNS, чтобы соответствующие домены SIP предоставляли внутреннее разрешение DNS для этих записей.</span><span class="sxs-lookup"><span data-stu-id="6bd89-187">Depending on how DNS is configured in your organization, you may need to add these records to the internal hosted DNS zone for the corresponding SIP domain(s) to provide internal DNS resolution to these records.</span></span>

</div>

<div>

## <a name="firewall-considerations"></a><span data-ttu-id="6bd89-188">Аспекты брандмауэра</span><span class="sxs-lookup"><span data-stu-id="6bd89-188">Firewall Considerations</span></span>

<span data-ttu-id="6bd89-p113">Компьютеры в сети должны поддерживать выполнение стандартных уточняющих интернет-запросов DNS. Если эти компьютеры могут осуществлять доступ к стандартным интернет-сайтам, сеть отвечает этому требованию.</span><span class="sxs-lookup"><span data-stu-id="6bd89-p113">Computers on your network must be able to perform standard Internet DNS lookups. If these computers can reach standard Internet sites, your network meets this requirement.</span></span>

<span data-ttu-id="6bd89-191">В зависимости от расположения центра обработки данных Microsoft Online Services необходимо также настроить сетевые брандмауэры так, чтобы они могли принимать подключения на основе доменных имен с подмигными знаками (например, всего трафика с \* outlook.com).</span><span class="sxs-lookup"><span data-stu-id="6bd89-191">Depending on the location of your Microsoft Online Services data center, you must also configure your network firewall devices to accept connections based on wildcard domain names (for example, all traffic from \*.outlook.com).</span></span> <span data-ttu-id="6bd89-192">Если брандмауэры организации не поддерживают конфигурации с подстановочными именами, необходимо вручную определить диапазоны IP-адресов, которые необходимо разрешить, и указанные порты.</span><span class="sxs-lookup"><span data-stu-id="6bd89-192">If your organization’s firewalls do not support wildcard name configurations, you will have to manually determine the IP address ranges that you would like to allow and the specified ports.</span></span>

<span data-ttu-id="6bd89-193">Обратитесь к разделу справки по URL-адресам [и диапазонам IP-адресов Office 365.](https://go.microsoft.com/fwlink/p/?linkid=252942)</span><span class="sxs-lookup"><span data-stu-id="6bd89-193">Refer to the Help topic [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=252942).</span></span>

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a><span data-ttu-id="6bd89-194">Требования к порту и протоколу</span><span class="sxs-lookup"><span data-stu-id="6bd89-194">Port and Protocol Requirements</span></span>

<span data-ttu-id="6bd89-195">Кроме портов для внутреннего взаимодействия с Lync Server 2013, необходимо также настроить следующие порты:</span><span class="sxs-lookup"><span data-stu-id="6bd89-195">In addition to the port requirements for internal Lync Server 2013 communication, you must also configure the following ports.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bd89-196">Протокол/порт</span><span class="sxs-lookup"><span data-stu-id="6bd89-196">Protocol / Port</span></span></th>
<th><span data-ttu-id="6bd89-197">Приложения</span><span class="sxs-lookup"><span data-stu-id="6bd89-197">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bd89-198">TCP 443</span><span class="sxs-lookup"><span data-stu-id="6bd89-198">TCP 443</span></span></p></td>
<td><p><span data-ttu-id="6bd89-199">Открытый входящий</span><span class="sxs-lookup"><span data-stu-id="6bd89-199">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="6bd89-200">Службы федерации Active Directory (роль сервера федерации)</span><span class="sxs-lookup"><span data-stu-id="6bd89-200">Active Directory Federation Services (federation server role)</span></span></p>
<p><span data-ttu-id="6bd89-201">Дополнительные сведения см. в <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">дополнительных сведениях о службах ролей AD FS.</a></span><span class="sxs-lookup"><span data-stu-id="6bd89-201">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span></span></p></li>
<li><p><span data-ttu-id="6bd89-202">Службы федерации Active Directory (роль прокси-сервера)</span><span class="sxs-lookup"><span data-stu-id="6bd89-202">Active Directory Federation Services (proxy server role)</span></span></p></li>
<li><p><span data-ttu-id="6bd89-203">Microsoft Online Services портала</span><span class="sxs-lookup"><span data-stu-id="6bd89-203">Microsoft Online Services Portal</span></span></p></li>
<li><p><span data-ttu-id="6bd89-204">Портал организации</span><span class="sxs-lookup"><span data-stu-id="6bd89-204">My Company Portal</span></span></p></li>
<li><p><span data-ttu-id="6bd89-205">Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="6bd89-205">Outlook Web App</span></span></p></li>
<li><p><span data-ttu-id="6bd89-206">Клиент Lync (связь с Lync Online с локального сервера Lync Server)</span><span class="sxs-lookup"><span data-stu-id="6bd89-206">Lync client (communication to Lync Online from on-premises Lync Server)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bd89-207">TCP 80 и 443</span><span class="sxs-lookup"><span data-stu-id="6bd89-207">TCP 80 and 443</span></span></p></td>
<td><p><span data-ttu-id="6bd89-208">Открытый входящий</span><span class="sxs-lookup"><span data-stu-id="6bd89-208">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="6bd89-209">средство синхронизации Microsoft Online Services со службой каталогов</span><span class="sxs-lookup"><span data-stu-id="6bd89-209">Microsoft Online Services Directory Synchronization Tool</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bd89-210">TCP 5061</span><span class="sxs-lookup"><span data-stu-id="6bd89-210">TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="6bd89-211">Открытый входящий и исходящие на границе сервера</span><span class="sxs-lookup"><span data-stu-id="6bd89-211">Open inbound/outbound on the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bd89-212">PSOM/TLS 443</span><span class="sxs-lookup"><span data-stu-id="6bd89-212">PSOM/TLS 443</span></span></p></td>
<td><p><span data-ttu-id="6bd89-213">Открытый для входящий и исходящие для сеансов общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="6bd89-213">Open inbound/outbound for data sharing sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bd89-214">STUN/TCP 443</span><span class="sxs-lookup"><span data-stu-id="6bd89-214">STUN/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="6bd89-215">Открытый для входящий и исходящие сеансы аудио- и видеосвязи, общего доступа к приложениям</span><span class="sxs-lookup"><span data-stu-id="6bd89-215">Open inbound/outbound for audio, video, application sharing sessions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bd89-216">STUN/UDP 3478</span><span class="sxs-lookup"><span data-stu-id="6bd89-216">STUN/UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="6bd89-217">Открытый для входящие и исходящие сеансы аудио- и видеосвязи</span><span class="sxs-lookup"><span data-stu-id="6bd89-217">Open inbound/outbound for audio and video sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bd89-218">RTP/TCP 50000-59999</span><span class="sxs-lookup"><span data-stu-id="6bd89-218">RTP/TCP 50000-59999</span></span></p></td>
<td><p><span data-ttu-id="6bd89-219">Открытый для исходящие сеансы аудио- и видеосвязи</span><span class="sxs-lookup"><span data-stu-id="6bd89-219">Open outbound for audio and video sessions</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a><span data-ttu-id="6bd89-220">Учетные записи и данные пользователей</span><span class="sxs-lookup"><span data-stu-id="6bd89-220">User Accounts and Data</span></span>

<span data-ttu-id="6bd89-221">В гибридном развертывании Lync Server 2013 необходимо создать в локальном развертывании любого пользователя, который будет размещен в Lync Online, чтобы учетная запись пользователя была создана в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6bd89-221">In a Lync Server 2013 hybrid deployment, any user that you want to home in Lync Online must first be created in the on-premises deployment, so that the user account is created in Active Directory Domain Services.</span></span> <span data-ttu-id="6bd89-222">Затем вы можете переместить пользователя в Skype для бизнеса Online, чтобы переместить его список контактов.</span><span class="sxs-lookup"><span data-stu-id="6bd89-222">You can then move the user to Skype for Business Online, which will move the user’s contact list.</span></span>

<span data-ttu-id="6bd89-223">При синхронизации учетных записей пользователей между локальной и сетевой развертываниями Lync Online с AD FS и Dirsync необходимо синхронизировать учетные записи AD для всех пользователей Lync в организации между локальной и сетевой развертываниями Lync, даже если пользователи не перемещены в Lync Online.</span><span class="sxs-lookup"><span data-stu-id="6bd89-223">When you synchronize user accounts between your Lync on-premises and Lync Online deployments with AD FS and Dirsync, you need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="6bd89-224">Если не все пользователи синхронизированы, связь между локальными и сетевыми пользователи в организации может функционировать неправильно.</span><span class="sxs-lookup"><span data-stu-id="6bd89-224">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6bd89-225">Если пользователь создан с помощью веб-портала для Центра администрирования Microsoft 365, учетная запись пользователя не будет синхронизироваться с локальной службой Active Directory и пользователь не будет существовать в локальной службе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6bd89-225">If the user is created by using the online portal for Microsoft 365 admin center, the user account will not be synchronized with on-premises Active Directory, and the user will not exist in the on-premises Active Directory.</span></span> <span data-ttu-id="6bd89-226">Если вы уже создали пользователей в Lync Online и хотите настроить гибридную конфигурацию с помощью локального сервера Lync Server, см. статью "Перемещение пользователей из Lync Online в локальное <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013".</A></span><span class="sxs-lookup"><span data-stu-id="6bd89-226">If you have already created users in Lync Online, and want to configure hybrid with an on-premises Lync Server, see <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="6bd89-227">Следует также принять во внимание следующие моменты, касающиеся пользователя, при планировании гибридного развертывания.</span><span class="sxs-lookup"><span data-stu-id="6bd89-227">You should also consider the following user-related issues when planning for a hybrid deployment.</span></span>

  - <span data-ttu-id="6bd89-228">**Контакты пользователя**   Предельное количество контактов для пользователей Lync Online — 250.</span><span class="sxs-lookup"><span data-stu-id="6bd89-228">**User contacts**   The limit for contacts for Lync Online users is 250.</span></span> <span data-ttu-id="6bd89-229">Все контакты, превышающие это количество, удаляются из списка контактов пользователя при перемещении учетной записи в Lync Online.</span><span class="sxs-lookup"><span data-stu-id="6bd89-229">Any contacts beyond that number will be removed from the user’s contact list when the account is moved to Lync Online.</span></span>

  - <span data-ttu-id="6bd89-230">**Обмен мгновенными сообщениями и оповещение о присутствии**   Списки контактов пользователя, группы и списки управления доступом (ACL) переносятся вместе с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="6bd89-230">**Instant Messaging and Presence**   User contact lists, groups, and access control lists (ACLs) are migrated with the user account.</span></span>

  - <span data-ttu-id="6bd89-231">**Данные о собрании, содержимое собрания и запланированные собрания**   Это содержимое не переносится вместе с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="6bd89-231">**Conferencing data, meeting content, and scheduled meetings**   This content is not migrated with the user account.</span></span> <span data-ttu-id="6bd89-232">После переноса учетных записей пользователей в Lync Online они должны заново запланировать собрания.</span><span class="sxs-lookup"><span data-stu-id="6bd89-232">Users must reschedule meetings after their accounts are migrated to Lync Online.</span></span>

</div>

<div>

## <a name="user-policies-and-features"></a><span data-ttu-id="6bd89-233">Политики и компонентов пользователей</span><span class="sxs-lookup"><span data-stu-id="6bd89-233">User Policies and Features</span></span>

  - <span data-ttu-id="6bd89-234">В гибридной среде Lync Server 2013 пользователи могут использовать мгновенные сообщения, голосовые сообщения и собрания как локально, так и через Интернет, но не одновременно.</span><span class="sxs-lookup"><span data-stu-id="6bd89-234">In a Lync Server 2013 hybrid environment, users can be enabled for Instant Messaging, voice, and meetings either on-premises or online, but not both simultaneously.</span></span>

  - <span data-ttu-id="6bd89-235">**Клиент Lync**    При перемещении в Lync Online некоторым пользователям может потребоваться новая версия клиента.</span><span class="sxs-lookup"><span data-stu-id="6bd89-235">**Lync Client**    Some users may require a new client version when they are moved to Lync Online.</span></span> <span data-ttu-id="6bd89-236">Для Office Communications Server 2007 R2 перед миграцией на Lync Online пользователей необходимо перена перемещать в пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6bd89-236">For Office Communications Server 2007 R2, users must be moved to a Lync Server 2013 pool prior to migration to Lync Online.</span></span>
    
    <span data-ttu-id="6bd89-237">Дополнительные сведения о поддержке клиентов см. в клиентах [Lync Online,](https://go.microsoft.com/fwlink/p/?linkid=281902) поддерживаемых клиентах [Lync и конфигурациях сетевых портов.](https://go.microsoft.com/fwlink/p/?linkid=281901)</span><span class="sxs-lookup"><span data-stu-id="6bd89-237">For more information about client support, see [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span></span>

  - <span data-ttu-id="6bd89-238">Политики и конфигурация локальной **системы (не пользователь)**   Веб-и локальной политикам требуется отдельная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="6bd89-238">**On-premises policies and configuration (non-user)**   Online and on-premises policies require separate configuration.</span></span> <span data-ttu-id="6bd89-239">Невозможно задать глобальные политики, применимые к обеим средам.</span><span class="sxs-lookup"><span data-stu-id="6bd89-239">You cannot set global policies that apply to both.</span></span>

<span data-ttu-id="6bd89-240"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bd89-240"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
