---
title: 'Lync Server 2013: проблемы с проверкой топологии'
description: 'Lync Server 2013: проблемы с проверкой топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the topology test
ms:assetid: 821e8916-7b5d-4f64-8fb0-e5cc392ec1bb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205045(v=OCS.15)
ms:contentKeyID: 48184670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a0f24942844bcf371eff94ee04c8faafcf513d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426713"
---
# <a name="issues-with-the-topology-test-in-lync-server-2013"></a><span data-ttu-id="6ca42-103">Проблемы с проверкой топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ca42-103">Issues with the topology test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ca42-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ca42-104">

<span> </span></span></span>

<span data-ttu-id="6ca42-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="6ca42-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="6ca42-106">Как и командлет **Test-CsTopology** , анализатор соответствия рекомендациям предоставляет способ проверки правильности функционирования Lync Server 2013 на глобальном уровне.</span><span class="sxs-lookup"><span data-stu-id="6ca42-106">Like the **Test-CsTopology** cmdlet, Best Practice Analyzer provides a way for you to verify that Lync Server 2013 is functioning correctly at a global level.</span></span> <span data-ttu-id="6ca42-107">По умолчанию анализатором соответствия рекомендациям, например командлет, проверяется вся инфраструктура Lync Server 2013, проверка того, что запущены нужные службы, и установлены ли соответствующие права и разрешения пользователей для этих служб, а также для универсальных групп безопасности, созданных при установке Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6ca42-107">By default, Best Practice Analyzer, like the cmdlet, checks your entire Lync Server 2013 infrastructure, verifying that the required services are running, and that the appropriate user rights and permissions have been set for these services and for the universal security groups created when you install Lync Server 2013.</span></span>

<span data-ttu-id="6ca42-108">Помимо проверки действительности сервера Lync Server, **Test-CsTopology** также проверяет правильность определенной службы.</span><span class="sxs-lookup"><span data-stu-id="6ca42-108">In addition to verifying the validity of Lync Server as a whole, **Test-CsTopology** also checks the validity of a specific service.</span></span> <span data-ttu-id="6ca42-109">Подробные сведения об использовании командлета для проверки конкретных служб можно найти в разделе [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) в документации по среде управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6ca42-109">For details about using the cmdlet to test specific services, see [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) in the Lync Server Management Shell documentation.</span></span> <span data-ttu-id="6ca42-110">Чтобы устранить проблемы с топологией, воспользуйтесь приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="6ca42-110">Use the following information to help resolve issues with your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6ca42-111">В зависимости от конфигурации пограничных серверов и всех связанных с ней параметров периметра сети, включая параметры брандмауэра и разрешения, анализатор соответствия рекомендациям может не получить доступ к пограничным серверам и их проверку.</span><span class="sxs-lookup"><span data-stu-id="6ca42-111">Depending on the configuration of your Edge Servers and any related perimeter network settings, including firewall settings and permissions, Best Practices Analyzer might not be able to access and scan your Edge Servers.</span></span> <span data-ttu-id="6ca42-112">Если вы включаете пограничные серверы в вашем сканировании, а отчеты указывают на то, что возникают неполадки при доступе к пограничным серверам, снимите флажок <STRONG>пограничные серверы</STRONG> и снова запустите проверку, чтобы предотвратить возникновение этой ошибки в отчетах.</span><span class="sxs-lookup"><span data-stu-id="6ca42-112">If you include Edge Servers in your scan and the reports indicate that there is an issue accessing Edge Servers, clear the <STRONG>Edge Servers</STRONG> check box and run the scan again to prevent the issue from showing up in reports.</span></span>



</div>

<div>

## <a name="resolving-issues-with-your-topology"></a><span data-ttu-id="6ca42-113">Устранение проблем с топологией</span><span class="sxs-lookup"><span data-stu-id="6ca42-113">Resolving Issues with Your Topology</span></span>

<span data-ttu-id="6ca42-114">Если при тестировании топологии возникли проблемы с топологией, это может быть вызвано проблемами, возникающими при публикации или включении топологии.</span><span class="sxs-lookup"><span data-stu-id="6ca42-114">If the topology test found issues with your topology, these issues are probably caused by issues that occurred when you published or enabled your topology.</span></span>

<span data-ttu-id="6ca42-115">После внесения изменений в топологию изменения вступают в силу только после того, как они были опубликованы и включены.</span><span class="sxs-lookup"><span data-stu-id="6ca42-115">When you make changes to your topology, the changes take effect only when they have been both published and enabled.</span></span> <span data-ttu-id="6ca42-116">Для внесения изменений в топологию необходимо использовать Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="6ca42-116">You must use Topology Builder to make topology changes.</span></span> <span data-ttu-id="6ca42-117">После внесения изменений вы можете опубликовать и включить эти изменения с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="6ca42-117">After you make changes, you can then publish and enable those changes by using Topology Builder.</span></span>

<span data-ttu-id="6ca42-118">Когда вы публикуете изменения, новые сведения (например, новый сайт или роль новой серверной роли) записываются в хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="6ca42-118">When you publish the changes, the new information (for example, a new site or a new server role) is written to the Central Management store.</span></span> <span data-ttu-id="6ca42-119">Однако эти новые (или только что измененные) объекты не присоединяются к топологии сразу.</span><span class="sxs-lookup"><span data-stu-id="6ca42-119">However, these new (or the newly modified) objects do not immediately join your topology.</span></span> <span data-ttu-id="6ca42-120">Объекты подключаются к топологии только в том случае, если вы включите обновленную топологию.</span><span class="sxs-lookup"><span data-stu-id="6ca42-120">Objects join your topology only when you enable the updated topology.</span></span> <span data-ttu-id="6ca42-121">Если выбрать параметр Опубликовать в построителе топологии, выполняются оба указанных ниже действия. изменения публикуются (то есть они записываются в хранилище Центрального управления), а затем включена новая топология.</span><span class="sxs-lookup"><span data-stu-id="6ca42-121">If you select the Publish option in Topology Builder both of these steps occur: the changes are published (that is, they are written to the Central Management store) and then the new topology is enabled.</span></span>

<span data-ttu-id="6ca42-122">По умолчанию членам группы RTCUniversalServerAdmins разрешено выполнять командлет **Publish-CsTopology** и командлет **Enable-CsTopology** .</span><span class="sxs-lookup"><span data-stu-id="6ca42-122">By default, members of the RTCUniversalServerAdmins group are authorized to run the **Publish-CsTopology** cmdlet and the **Enable-CsTopology** cmdlet.</span></span> <span data-ttu-id="6ca42-123">Однако если разрешения на установку не делегированы, необходимо войти в учетную запись администратора домена, чтобы запустить команду **Publish-CsTopology**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-123">However, if setup permissions have not been delegated, you must be logged on as a domain administrator to run **Publish-CsTopology**.</span></span> <span data-ttu-id="6ca42-124">Чтобы предоставить RTCUniversalServerAdmins право на фактическое использование командлета **Publish-CsTopology** , необходимо выполнить командлет **Grant-CsSetupPermission** в каждом контейнере Active Directory, содержащем компьютеры, на которых выполняются службы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6ca42-124">To give RTCUniversalServerAdmins the right to actually use the **Publish-CsTopology** cmdlet, you must run the **Grant-CsSetupPermission** cmdlet on every Active Directory container that contains computers running Lync Server services.</span></span> <span data-ttu-id="6ca42-125">Чтобы предоставить RTCUniversalServerAdmins право на использование командлета **Enable-CsTopology** , необходимо выполнить командлет **Set-CsSetupPermission** для каждого контейнера доменных служб Active Directory, содержащего компьютеры, на которых выполняются службы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6ca42-125">To give RTCUniversalServerAdmins the right to use the **Enable-CsTopology** cmdlet, you must run the **Set-CsSetupPermission** cmdlet against every Active Directory Domain Services container that contains computers running Lync Server services.</span></span> <span data-ttu-id="6ca42-126">Обратите внимание, что это касается включения и публикации топологии с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="6ca42-126">Note that this applies to enabling and publishing a topology by using Topology Builder.</span></span> <span data-ttu-id="6ca42-127">Если вы не делегированы разрешения с помощью **Set-CsSetupPermission**, только администратор домена может включать и публиковать топологию с помощью Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="6ca42-127">If you have not delegated permissions by using **Set-CsSetupPermission**, only a domain administrator can enable and publish a topology through Topology Builder.</span></span>

<span data-ttu-id="6ca42-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ca42-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

