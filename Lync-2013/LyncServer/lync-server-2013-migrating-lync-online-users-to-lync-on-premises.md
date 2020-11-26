---
title: 'Lync Server 2013: переход пользователей Lync Online в локальное Lync'
description: 'Lync Server 2013: переход пользователей Lync Online в локальное Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrating Lync Online users to Lync on-premises
ms:assetid: 0e29605b-db2d-4cbf-b6a9-15db6b9fdabc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689115(v=OCS.15)
ms:contentKeyID: 62258120
ms.date: 11/13/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 620bc07def8e3c1f6b761c6398b452b4dbcd3b04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445983"
---
# <a name="migrating-lync-online-users-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="9f9e1-103">Миграция пользователей Lync Online в локальное Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f9e1-103">Migrating Lync Online users to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f9e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f9e1-104">

<span> </span></span></span>

<span data-ttu-id="9f9e1-105">_**Тема последнего изменения:** 2015-11-13_</span><span class="sxs-lookup"><span data-stu-id="9f9e1-105">_**Topic Last Modified:** 2015-11-13_</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="9f9e1-106">Эти действия необходимы только для миграции учетных записей пользователей, изначально включенных для Lync в Lync Online, до того как вы разрешаете локальное развертывание Lync.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-106">These steps are necessary only for migrating user accounts that were originally enabled for Lync in Lync Online, before you deployed Lync on-premises.</span></span> <span data-ttu-id="9f9e1-107">Чтобы переместить пользователей, изначально подключенных к локальной среде Lync, а затем переместить их в Lync Online, читайте в разделе <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Администрирование пользователей в гибридном развертывании Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-107">To move users who were originally enabled for Lync on-premises, then later moved to Lync Online, see <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</A>.</span></span><BR><span data-ttu-id="9f9e1-108">Кроме того, у всех перемещаемых пользователей должны быть учетные записи в локальной службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-108">Additionally, all users being moved must have accounts in the on-premises Active Directory.</span></span>



</div>

<div>

## <a name="migrating-user-accounts-originally-enabled-in-lync-online-to-lync-on-premises"></a><span data-ttu-id="9f9e1-109">Перенос учетных записей пользователей, изначально включенных в Lync Online, в локальное Lync</span><span class="sxs-lookup"><span data-stu-id="9f9e1-109">Migrating User Accounts Originally Enabled in Lync Online to Lync On-Premises</span></span>

1.  <span data-ttu-id="9f9e1-110">Сначала убедитесь в том, что ваша организация настроена для гибридного развертывания.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-110">First, make sure that your organization is configured for hybrid.</span></span>
    
      - <span data-ttu-id="9f9e1-111">Установите средство синхронизации Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-111">Install the Azure Active Directory Sync Tool.</span></span> <span data-ttu-id="9f9e1-112">Дополнительные сведения см. в статье <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-112">For more information, see <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span></span>
    
      - <span data-ttu-id="9f9e1-113">Чтобы разрешить пользователям использовать единый вход для Lync Online, установите службы федерации Active Directory <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx> .</span><span class="sxs-lookup"><span data-stu-id="9f9e1-113">To enable your users to use single sign-on for Lync Online, install Active Directory Federation Services <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx>.</span></span>
    
      - <span data-ttu-id="9f9e1-114">В локальной среде Lync Server Management Shell введите следующие командлеты, чтобы создать поставщика услуг размещения для Lync Online:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-114">On your on-premises deployment, in Lync Server Management Shell, type the following cmdlets to create the hosting provider for Lync Online:</span></span>
        
           ```PowerShell
           Set-CsAccessEdgeConfiguration -AllowOutsideUsers 1 -AllowFederatedUsers 1 -UseDnsSrvRouting -EnablePartnerDiscovery $true
           ```
        
           ```PowerShell
            New-CsHostingProvider -Identity LyncOnline -ProxyFqdn "sipfed.online.lync.com" -Enabled $true -EnabledSharedAddressSpace $true -HostsOCSUsers $true -VerificationLevel UseSourceVerification -IsLocal $false -AutodiscoverUrl https://webdir.online.lync.com/Autodiscover/AutodiscoverService.svc/root
           ```

2.  <span data-ttu-id="9f9e1-115">Убедитесь, что на локальных серверах пограничного сервера есть цепочка сертификатов, обеспечивающая подключение к Lync Online, как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-115">Confirm that, on your on-premises Edge Servers, you have the certificate chain that enables connection to Lync Online, as shown in the following table.</span></span> <span data-ttu-id="9f9e1-116">Вы можете загрузить эту цепь здесь: https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span><span class="sxs-lookup"><span data-stu-id="9f9e1-116">You can download this chain here: https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span></span>


    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="9f9e1-117">Сертификат</span><span class="sxs-lookup"><span data-stu-id="9f9e1-117">Certificate</span></span></th>
    <th><span data-ttu-id="9f9e1-118">Хранилище сертификатов</span><span class="sxs-lookup"><span data-stu-id="9f9e1-118">Certificate Store</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="9f9e1-119">Корневой Baltimore CyberTrust</span><span class="sxs-lookup"><span data-stu-id="9f9e1-119">Baltimore CyberTrust Root</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-120">Доверенный корневой ЦС</span><span class="sxs-lookup"><span data-stu-id="9f9e1-120">Trusted Root CA</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="9f9e1-121">Microsoft Internet Authority (сертификат нового ЦС)</span><span class="sxs-lookup"><span data-stu-id="9f9e1-121">Microsoft Internet Authority (New CA certificate)</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-122">Промежуточный ЦС</span><span class="sxs-lookup"><span data-stu-id="9f9e1-122">Intermediate CA</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="9f9e1-123">MSIT Machine Auth CA2 (новый выдающий ЦС2)</span><span class="sxs-lookup"><span data-stu-id="9f9e1-123">MSIT Machine Auth CA2 (New Issuing CA2)</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-124">Промежуточный ЦС</span><span class="sxs-lookup"><span data-stu-id="9f9e1-124">Intermediate CA</span></span></p></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="9f9e1-125">В локальной службе каталогов Active Directory включите затронутые учетные записи пользователей в локальной среде Lync.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-125">In your on-premises Active Directory, enable the affected user accounts for Lync on-premises.</span></span> <span data-ttu-id="9f9e1-126">Для отдельных пользователей это можно сделать путем ввода следующего командлета:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-126">You can do this for an individual user by typing the following cmdlet:</span></span>
    
        Enable-CsUser
        -Identity "username" 
        -SipAddress "sip: username@contoso.com"
        -HostingProviderProxyFqdn "sipfed.online.lync.com"
    
    <span data-ttu-id="9f9e1-127">Или можно создать сценарий для считывания имен пользователей из файла и передачи их как входных данных командлету Enable-CsUser:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-127">Or you can create a script that reads user names from a file and provides them as input to the Enable-CsUser cmdlet:</span></span>
    
        Enable-CsUser
        -Identity $Identity 
        -SipAddress $SipAddress 
        -HostingProviderProxyFqdn "sipfed.online.lync.com"

4.  <span data-ttu-id="9f9e1-128">Запустите DirSync, чтобы синхронизировать пользователей Lync Online с обновленными локальными пользователями Lync.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-128">Run DirSync to sync the Lync Online users with the updated Lync on-premises users.</span></span>

5.  <span data-ttu-id="9f9e1-129">Обновите некоторые записи DNS, чтобы направить весь трафик SIP на локальный Lync:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-129">Update some DNS records to direct all SIP traffic to Lync on-premises:</span></span>
    
      - <span data-ttu-id="9f9e1-130">Обновите запись **lyncdiscover.contoso.com** A, указав полное доменное имя локального обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-130">Update the **lyncdiscover.contoso.com** A record to point to the FQDN of the on-premises reverse proxy server.</span></span>
    
      - <span data-ttu-id="9f9e1-131">Обновите **_\_ SIP_. \_ tls.contoso.com** SRV-запись, разрешаемая на общедоступный IP-адрес или виртуальную ЛС для службы Edge Access в локальной среде Lync.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-131">Update the **_\_sip_.\_tls.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="9f9e1-132">Обновите **_\_ sipfederationtls_. \_ tcp.contoso.com** SRV-запись, разрешаемая на общедоступный IP-адрес или виртуальную ЛС для службы Edge Access в локальной среде Lync.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-132">Update the **_\_sipfederationtls_.\_tcp.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="9f9e1-133">Если в организации используется комбинированная DNS (иногда называется "разделенной DNS"), убедитесь, что пользователи, разрешающие имена во внутренней зоне DNS, направляются в интерфейсный пул.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-133">If your organization uses split DNS (sometimes called “split-brain DNS”), make sure that users resolving names through the internal DNS zone are directed to the Front End Pool.</span></span>

6.  <span data-ttu-id="9f9e1-134">Введите `Get-CsUser` командлет для проверки некоторых свойств пользователей, которых вы хотите переместить.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-134">Type the `Get-CsUser` cmdlet to check some properties about the users you’ll be moving.</span></span> <span data-ttu-id="9f9e1-135">Необходимо убедиться в том, что в HostingProviderProxyFQDN задано значение `"sipfed.online.lync.com"` и правильно заданы адреса SIP.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-135">You want to make sure that the HostingProviderProxyFQDN is set to `"sipfed.online.lync.com"` and that the SIP addresses are set correctly.</span></span>

7.  <span data-ttu-id="9f9e1-136">Переместить пользователей Lync Online в локальное Lync.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-136">Move Lync Online users to Lync on-premises.</span></span>
    
    <span data-ttu-id="9f9e1-137">Чтобы переместить одного пользователя, введите следующее:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-137">To move a single user, type this:</span></span>
    
       ```PowerShell
       $cred = Get-Credential
       ```
    
       ```PowerShell
       Move-CsUser -Identity <username>@contoso.com -Target "<fe-pool>.contoso.com" -Credential $cred -HostedMigrationOverrideURL <URL>
       ```
    
    <span data-ttu-id="9f9e1-138">Командлет **Get-CsUSer** позволяет переместить несколько пользователей, выбрав их по некоторому свойству.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-138">You can move multiple users by using the **Get-CsUSer** cmdlet with the –Filter parameter to select the users with a specific property.</span></span> <span data-ttu-id="9f9e1-139">Например, вы можете выбрать всех пользователей Lync Online с помощью фильтрации для {Host Provider-EQ "sipfed.online.lync.om"}.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-139">For example, you could select all Lync Online users by filtering for {Hosting Provider –eq “sipfed.online.lync.om”}.</span></span> <span data-ttu-id="9f9e1-140">Возвращенных пользователей можно затем передать командлету **Move-CsUSer**, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-140">You can then pipe the returned users to the **Move-CsUSer** cmdlet, as shown below.</span></span>
    
        Get-CsUser -Filter {Hosting Provider -eq "sipfed.online.lync.com"} | Move-CsUser -Target "<fe-pool>.contoso.com" -Credential $creds -HostedMigrationOverrideURL <URL>
    
    <span data-ttu-id="9f9e1-141">Формат URL-адреса, заданный для параметра **HostedMigrationOverrideUrl** , должен быть URL-адресом пула, на котором запущена служба размещенной миграции, в следующем формате: *https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc*.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-141">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format: *Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc*.</span></span>
    
    <span data-ttu-id="9f9e1-142">Вы можете определить URL-адрес размещенной службы миграции, просмотрев URL-адрес панели управления Lync Online для своей учетной записи Microsoft 365 или Office 365.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-142">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>
    
    <div>
    
    ## <a name="to-determine-the-hosted-migration-service-url-for-your-organizaton"></a><span data-ttu-id="9f9e1-143">Определение URL-адреса размещенной службы миграции для Организации</span><span class="sxs-lookup"><span data-stu-id="9f9e1-143">To determine the Hosted Migration Service URL for your organizaton</span></span>
    
    1.  <span data-ttu-id="9f9e1-144">Войдите в свою организацию Microsoft 365 или Office 365 с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-144">Log in to your Microsoft 365 or Office 365 organization as an administrator.</span></span>
    
    2.  <span data-ttu-id="9f9e1-145">Откройте **центр администрирования Lync**.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-145">Open the **Lync admin center**.</span></span>
    
    3.  <span data-ttu-id="9f9e1-146">В **центре администрирования Lync** выберите и скопируйте URL-адрес в адресной строке на **Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-146">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="9f9e1-147">Ниже показан возможны пример URL-адреса</span><span class="sxs-lookup"><span data-stu-id="9f9e1-147">An example URL looks similar to the following:</span></span>
        
        `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`
    
    4.  <span data-ttu-id="9f9e1-148">После замены фрагмента **webdir** в URL-адресе фрагментом **admin** получается следующий результат:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-148">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
        
        `https://admin0a.online.lync.com`
    
    5.  <span data-ttu-id="9f9e1-149">Добавьте к URL-адресу следующую строку: **/HostedMigration/hostedmigrationservice.svc**.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-149">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
        
        <span data-ttu-id="9f9e1-150">Итоговый URL-адрес, который служит значением параметра **HostedMigrationOverrideUrl**, должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-150">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
        
        `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`
    
    </div>
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="9f9e1-151">По умолчанию максимальный размер файлов журналов транзакций базы данных rtcxds составляет 16 ГБ.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-151">The default maximum size for transaction log files of the rtcxds database is 16 GB.</span></span> <span data-ttu-id="9f9e1-152">Это может оказаться недостаточным для одновременного перемещения большого количества пользователей, особенно если включено зеркальное отображение.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-152">This might not be big enough if you’re moving a large number of users at once, especially if you have mirroring enabled.</span></span> <span data-ttu-id="9f9e1-153">Во избежание такой ситуации можно увеличить размер файлов или регулярно создавать резервные копии файлов журналов.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-153">To get around this you can increase the file size or back up the log files regularly.</span></span> <span data-ttu-id="9f9e1-154">Дополнительные сведения см. в статье <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-154">For more information, see <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span></span>

    
    </div>

8.  <span data-ttu-id="9f9e1-155">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-155">This is an optional step.</span></span> <span data-ttu-id="9f9e1-156">Если вам нужно интегрироваться с Exchange 2013 Online, необходимо использовать дополнительного поставщика услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-156">If you need to integrate with Exchange 2013 Online, you need to use an additional hosting provider.</span></span> <span data-ttu-id="9f9e1-157">Подробности можно найти [в разделе Настройка локальной интеграции Lync Server 2013 с Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="9f9e1-157">For details, see [Configuring on-premises Lync Server 2013 integration with Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span></span>

9.  <span data-ttu-id="9f9e1-p110">Теперь пользователи перемещаются. Чтобы проверить, что пользователь имеет правильные значения для атрибутов, показанных в таблице ниже, введите следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-p110">The users are now moved. To check that a user has correct values for the attributes shown in the following table, type this cmdlet:</span></span>
    
        Get-CsUser | fl DisplayName,HostingProvider,SipAddress,Enabled
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="9f9e1-160">Атрибут Active Directory</span><span class="sxs-lookup"><span data-stu-id="9f9e1-160">Active Directory attribute</span></span></th>
    <th><span data-ttu-id="9f9e1-161">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="9f9e1-161">Attribute name</span></span></th>
    <th><span data-ttu-id="9f9e1-162">Правильное значение для пользователя Lync Online</span><span class="sxs-lookup"><span data-stu-id="9f9e1-162">Correct value for Lync Online user</span></span></th>
    <th><span data-ttu-id="9f9e1-163">Правильное значение для локальных пользователей Lync</span><span class="sxs-lookup"><span data-stu-id="9f9e1-163">Correct value for Lync on–premises users</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="9f9e1-164">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="9f9e1-164">msRTCSIP-DeploymentLocator</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-165">HostingProvider</span><span class="sxs-lookup"><span data-stu-id="9f9e1-165">HostingProvider</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-166">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="9f9e1-166">sipfed.online.lync.com</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-167">SRV:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-167">SRV:</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="9f9e1-168">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="9f9e1-168">msRTCSIP-PrimaryUserAddress</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-169">SIPAddress</span><span class="sxs-lookup"><span data-stu-id="9f9e1-169">SIPAddress</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-170">sip:userName@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9f9e1-170">sip:userName@contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-171">sip:userName@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9f9e1-171">sip:userName@contoso.com</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="9f9e1-172">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="9f9e1-172">msRTCSIP-UserEnabled</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-173">Включено</span><span class="sxs-lookup"><span data-stu-id="9f9e1-173">Enabled</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-174">True</span><span class="sxs-lookup"><span data-stu-id="9f9e1-174">True</span></span></p></td>
    <td><p><span data-ttu-id="9f9e1-175">Верно</span><span class="sxs-lookup"><span data-stu-id="9f9e1-175">True</span></span></p></td>
    </tr>
    </tbody>
    </table>


10. <span data-ttu-id="9f9e1-176">Каждый пользователь, который был перемещен, должен выйти из Lync, а затем снова войти в систему.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-176">Each user who has been moved will need to log out of Lync, then log back in.</span></span> <span data-ttu-id="9f9e1-177">При входе они должны проверить свои списки контактов и в случае необходимости добавить контакты.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-177">When they log in they should verify their contact lists, and add contacts if needed.</span></span>
    
    <span data-ttu-id="9f9e1-178">Обратите внимание, что запланированные собрания не переносятся из Lync Online в локальное Lync.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-178">Note that scheduled meetings are not migrated from Lync Online to Lync on-premises.</span></span> <span data-ttu-id="9f9e1-179">После перемещения пользователям потребуется запланировать такие собрания заново.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-179">Users will need to reschedule these meetings after being moved.</span></span>
    
    <span data-ttu-id="9f9e1-180">После того как DNS-записи обновлены и все пользователи направлены на локальные, атрибут HostingProvider направляет пользователю Lync команду либо использовать записи SRV, либо направить их на Интернет-провайдер "sipfed.online.lync.com".</span><span class="sxs-lookup"><span data-stu-id="9f9e1-180">After the DNS records are updated and all users are directed to On premise, the HostingProvider attribute directs the Lync user to either use SRV records or direct them to the Online provider “sipfed.online.lync.com.”</span></span>

<span data-ttu-id="9f9e1-181"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f9e1-181"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

