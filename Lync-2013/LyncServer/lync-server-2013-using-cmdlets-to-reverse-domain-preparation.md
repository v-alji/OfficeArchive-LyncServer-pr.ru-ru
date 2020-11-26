---
title: 'Lync Server 2013: использование командлетов для отмены подготовки доменов'
description: 'Lync Server 2013: использование командлетов для реверсирования подготовки домена.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse domain preparation
ms:assetid: 014dba5d-fcb3-44c9-9d63-ae0755276dac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398071(v=OCS.15)
ms:contentKeyID: 48183227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d26cc97ee934ee959838f38f4e2f52f9bf89566
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439018"
---
# <a name="using-cmdlets-to-reverse-domain-preparation-for-lync-server-2013"></a><span data-ttu-id="d90e7-103">Использование командлетов для отмены подготовки доменов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d90e7-103">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d90e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d90e7-104">

<span> </span></span></span>

<span data-ttu-id="d90e7-105">_**Тема последнего изменения:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="d90e7-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="d90e7-106">Используйте командлет **Disable-CsAdDomain** для реверсирования этапа подготовки домена.</span><span class="sxs-lookup"><span data-stu-id="d90e7-106">Use the **Disable-CsAdDomain** cmdlet to reverse the domain preparation step.</span></span>

<div>

## <a name="to-use-cmdlets-to-reverse-domain-preparation"></a><span data-ttu-id="d90e7-107">Использование командлетов для реверсирования подготовки домена</span><span class="sxs-lookup"><span data-stu-id="d90e7-107">To use cmdlets to reverse domain preparation</span></span>

1.  <span data-ttu-id="d90e7-108">Войдите на любой сервер домена, который является членом группы "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="d90e7-108">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="d90e7-109">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="d90e7-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d90e7-110">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d90e7-110">Run:</span></span>
    
        Disable-CsAdDomain [-Domain <Fqdn>] [-DomainController <Fqdn>] [-Force <SwitchParameter>] 
        [-GlobalCatalog <Fqdn>] [-GlobalSettingsDomainController <Fqdn>] 
    
    <span data-ttu-id="d90e7-111">Например:</span><span class="sxs-lookup"><span data-stu-id="d90e7-111">For example:</span></span>
    
        Disable-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.net -Force
    
    <span data-ttu-id="d90e7-112">Если параметр принудительно присутствует, подготовка домена откатывается, даже если активирован один или несколько серверов переднего или видеоконференций в домене.</span><span class="sxs-lookup"><span data-stu-id="d90e7-112">If the Force parameter is present, domain preparation is rolled back, even if one or more Front End Servers or A/V Conferencing Servers in the domain are activated.</span></span> <span data-ttu-id="d90e7-113">Если параметр Force не указан, откат подготовки домена завершается, если активированы какие-либо серверы переднего плана или серверы конференций/V в домене.</span><span class="sxs-lookup"><span data-stu-id="d90e7-113">If the Force parameter is not present, domain preparation rollback is terminated if any Front End Servers or A/V Conferencing Servers in the domain are activated.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d90e7-114">Параметр GlobalSettingsDomainController позволяет указать, где хранятся глобальные параметры.</span><span class="sxs-lookup"><span data-stu-id="d90e7-114">The parameter GlobalSettingsDomainController allows you to indicate where global settings are stored.</span></span> <span data-ttu-id="d90e7-115">Если ваши параметры хранятся в системном контейнере (обычно это происходит при развертывании обновлений без глобального параметра, перенесенного в контейнер конфигурации), вы можете определить контроллер домена в корне леса Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d90e7-115">If your settings are stored in the System container (which is typical with upgrade deployments that have not had the global setting migrated to the Configuration container), you define a domain controller in the root of your Active Directory forest.</span></span> <span data-ttu-id="d90e7-116">Если глобальные параметры хранятся в контейнере Configuration (это обычная ситуация для новых развертываний или обновленных развертываний, в которых параметры перенесены в контейнер Configuration), определите любой контроллер домена в лесу.</span><span class="sxs-lookup"><span data-stu-id="d90e7-116">If the global settings are in the Configuration container (which is typical with new deployments or upgrade deployments where the settings have been migrated to the Configuration container), you define any domain controller in the forest.</span></span> <span data-ttu-id="d90e7-117">Если этот параметр не указан, командлет предполагает, что параметры хранятся в контейнере конфигурации и ссылаются на любой контроллер домена в доменных &nbsp; службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d90e7-117">If you do not specify this parameter, the cmdlet assumes that the settings are stored in the Configuration container and refers to any domain controller in AD&nbsp;DS.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d90e7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d90e7-118">See Also</span></span>


[<span data-ttu-id="d90e7-119">Проведение подготовки домена для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d90e7-119">Running domain preparation for Lync Server 2013</span></span>](lync-server-2013-running-domain-preparation.md)  


[<span data-ttu-id="d90e7-120">Подготовка доменов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d90e7-120">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="d90e7-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d90e7-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

