---
title: 'Lync Server 2013: Администрирование пользователей в гибридном развертывании'
description: 'Lync Server 2013: Администрирование пользователей в гибридном развертывании.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398008"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a><span data-ttu-id="c17d3-103">Администрирование пользователей в гибридном развертывании Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c17d3-103">Administering users in a hybrid Lync Server 2013 deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c17d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c17d3-104">

<span> </span></span></span>

<span data-ttu-id="c17d3-105">_**Тема последнего изменения:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="c17d3-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="c17d3-106">Вы можете управлять параметрами пользователей и политиками для пользователей, перенесенных на Lync Online с помощью функций управления пользователями, которые доступны в центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c17d3-106">You can manage user settings and policies for users migrated to Lync Online by using the User Management features available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="c17d3-107">Для выполнения задач администрирования необходимо войти по учетной записи администратора клиента.</span><span class="sxs-lookup"><span data-stu-id="c17d3-107">You must sign in by using your tenant administrator account to perform administration tasks.</span></span>

<div>

## <a name="moving-users-back-to-on-premises"></a><span data-ttu-id="c17d3-108">Перемещение пользователей на локальный сервер</span><span class="sxs-lookup"><span data-stu-id="c17d3-108">Moving Users Back to On-premises</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="c17d3-109">Этот раздел относится только к пользователям, которые были созданы и включены в локальной среде Lync, а затем перенесено из локального развертывания в Lync Online.</span><span class="sxs-lookup"><span data-stu-id="c17d3-109">This section applies only to users that were created and enabled for Lync on-premises and then moved from an on-premises deployment to Lync Online.</span></span> <span data-ttu-id="c17d3-110">Если вы хотите переместить пользователей, которые были созданы в Lync Online (и не включены для Lync в локальном развертывании), ознакомьтесь с разрешениями: <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Перемещение пользователей из Lync Online в локальное приложение Lync в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c17d3-110">If you want to move users that were created in Lync Online (and not ever enabled for Lync in an on-premises deployment) see, <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

  - <span data-ttu-id="c17d3-111">Чтобы переместить пользователя из Lync Online обратно в локальное Lync, выполните следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="c17d3-111">Run the following cmdlets to move a user from Lync Online back to Lync on-premises:</span></span>
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

<span data-ttu-id="c17d3-112">В качестве параметра **HostedMigrationOverrideUrl** следует указать URL-адрес пула, где работает служба миграции с размещением, в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="c17d3-112">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format:</span></span>

<span data-ttu-id="c17d3-113"> Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc.</span><span class="sxs-lookup"><span data-stu-id="c17d3-113">Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc.</span></span> <span data-ttu-id="c17d3-114">Вы можете определить URL-адрес размещенной службы миграции, просмотрев URL-адрес панели управления Lync Online для своей учетной записи Microsoft 365 или Office 365.</span><span class="sxs-lookup"><span data-stu-id="c17d3-114">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>

<span data-ttu-id="c17d3-115">**Определение URL-адреса размещенной службы миграции для организации Microsoft 365 или Office 365**</span><span class="sxs-lookup"><span data-stu-id="c17d3-115">**To determine the Hosted Migration Service URL for your Microsoft 365 or Office 365 organization**</span></span>

1.  <span data-ttu-id="c17d3-116">Войдите в свою организацию в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="c17d3-116">Log in to your organization as an administrator.</span></span>

2.  <span data-ttu-id="c17d3-117">Откройте **центр администрирования Lync**.</span><span class="sxs-lookup"><span data-stu-id="c17d3-117">Open the **Lync admin center**.</span></span>

3.  <span data-ttu-id="c17d3-118">В **центре администрирования Lync** выберите и скопируйте URL-адрес в адресной строке на **Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="c17d3-118">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="c17d3-119">Ниже показан возможны пример URL-адреса</span><span class="sxs-lookup"><span data-stu-id="c17d3-119">An example URL looks similar to the following:</span></span>
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  <span data-ttu-id="c17d3-120">После замены фрагмента **webdir** в URL-адресе фрагментом **admin** получается следующий результат:</span><span class="sxs-lookup"><span data-stu-id="c17d3-120">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
    
    `https://admin0a.online.lync.com`

5.  <span data-ttu-id="c17d3-121">Добавьте к URL-адресу следующую строку: **/HostedMigration/hostedmigrationservice.svc**.</span><span class="sxs-lookup"><span data-stu-id="c17d3-121">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
    
    <span data-ttu-id="c17d3-122">Итоговый URL-адрес, который служит значением параметра **HostedMigrationOverrideUrl**, должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c17d3-122">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

<span data-ttu-id="c17d3-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c17d3-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

