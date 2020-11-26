---
title: Необходимые условия и разрешения для настройки конференц-связи с телефонным подключением
description: Необходимые условия и разрешения для настройки конференц-связи с телефонным подключением.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing configuration prerequisites and permissions
ms:assetid: b3b251e5-78ac-44a2-8c36-2a061c9b2314
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412865(v=OCS.15)
ms:contentKeyID: 48185165
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eced67f33e35c711c4fcd31120480b6d5c2e41ce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429263"
---
# <a name="dial-in-conferencing-configuration-prerequisites-and-permissions-in-lync-server-2013"></a><span data-ttu-id="4cb3d-103">Необходимые условия и разрешения для настройки конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cb3d-103">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cb3d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cb3d-104">

<span> </span></span></span>

<span data-ttu-id="4cb3d-105">_**Тема последнего изменения:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="4cb3d-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="4cb3d-106">Конференц-связь с телефонным подключением — это необязательный компонент рабочей нагрузки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-106">Dial-in conferencing is an optional component of the Lync Server 2013 Conferencing workload.</span></span> <span data-ttu-id="4cb3d-107">Компоненты, которые необходимо установить перед тем, как настроить Конференц-связь с телефонным подключением, развертываются при использовании построителя топологии для создания топологии и последующем настройке пула переднего плана или сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-107">The components you need to install before you can configure dial-in conferencing are deployed when you use the Topology Builder to design your topology and then set up your Front End pool or Standard Edition server.</span></span> <span data-ttu-id="4cb3d-108">В этой статье описаны действия, которые необходимо выполнить, прежде чем можно будет настроить Конференц-связь с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-108">This topic describes what you need to have accomplished before you can configure dial-in conferencing.</span></span>

<span data-ttu-id="4cb3d-109">В этом разделе предполагается, что вы прочитали разделы планирование, связанные с рабочей нагрузкой и конференцстью с телефонным подключением, в частности.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-109">This section assumes that you have read the planning sections related to the Conferencing workload and dial-in conferencing in particular.</span></span>

<div>

## <a name="dial-in-conferencing-configuration-prerequisites"></a><span data-ttu-id="4cb3d-110">Необходимые условия для настройки конференц-связи с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="4cb3d-110">Dial-in Conferencing Configuration Prerequisites</span></span>

<span data-ttu-id="4cb3d-111">Для конференц-связи с телефонным подключением необходимы следующие компоненты Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="4cb3d-111">Dial-in conferencing requires the following Lync Server 2013 components:</span></span>

  - <span data-ttu-id="4cb3d-112">служба приложения объединенных коммуникаций (UCAS) (называемая просто *службой приложения*);</span><span class="sxs-lookup"><span data-stu-id="4cb3d-112">Unified Communications Application Service (UCAS) (called the *Application service*)</span></span>

  - <span data-ttu-id="4cb3d-113">приложение помощника по конференц-связи;</span><span class="sxs-lookup"><span data-stu-id="4cb3d-113">Conferencing Attendant application</span></span>

  - <span data-ttu-id="4cb3d-114">приложение оповещения для конференц-связи;</span><span class="sxs-lookup"><span data-stu-id="4cb3d-114">Conferencing Announcement application</span></span>

  - <span data-ttu-id="4cb3d-115">веб-страница "Параметры конференц-связи с телефонным подключением";</span><span class="sxs-lookup"><span data-stu-id="4cb3d-115">Dial-in Conferencing Settings webpage</span></span>

  - <span data-ttu-id="4cb3d-116">Хотя бы один сервер исправлений Lync Server 2013 и хотя бы один шлюз PSTN</span><span class="sxs-lookup"><span data-stu-id="4cb3d-116">At least one Lync Server 2013 Mediation Server and at least one PSTN gateway</span></span>

<span data-ttu-id="4cb3d-117">Эти компоненты развертываются при использовании построителя топологии для определения и публикации топологии и последующего развертывания пула переднего плана или стандартного сервера выпусков.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-117">You deploy these components when you use the Topology Builder to define and publish your topology and then deploy a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="4cb3d-118">Если вы выполняете развертывание корпоративной голосовой связи, перед настройкой конференц-связи с телефонным подключением вы должны развернуть ее.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-118">If you are deploying Enterprise Voice, you should deploy it before you configure dial-in conferencing.</span></span> <span data-ttu-id="4cb3d-119">Если вы не развертываете корпоративную голосовую почту, вы можете развернуть сервер-посредник и шлюз общественной коммутируемой телефонной сети (PSTN) при развертывании пула переднего плана или сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-119">If you are not deploying Enterprise Voice, you can deploy a Mediation Server and a public switched telephone network (PSTN) gateway when you deploy your Front End pool or Standard Edition server.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="4cb3d-120">Если вы обновляете Office Communications Server 2007 R2 на Lync Server 2013, разместите Конференц-связь с телефонным подключением в каждом пуле, который планируется использовать для размещения конференции Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-120">If you are upgrading from Office Communications Server 2007 R2 to Lync Server 2013, deploy dial-in conferencing in every pool that you plan to use to host Lync Server 2013 conferences.</span></span> <span data-ttu-id="4cb3d-121">Дополнительные сведения о переносе конференц-связи с телефонным подключением можно найти <A href="migration-from-office-communications-server-2007-r2-to-lync-server-2013.md">в разделе Миграция с Office Communications Server 2007 R2 на Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-121">For details about migrating dial-in conferencing, see <A href="migration-from-office-communications-server-2007-r2-to-lync-server-2013.md">Migration from Office Communications Server 2007 R2 to Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="4cb3d-122">В этом разделе предполагается, что вы выполнили описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-122">This section assumes that you have done the following:</span></span>

  - <span data-ttu-id="4cb3d-123">Последние обновления для среды Office Communications Server 2007 R2 применяются при переходе на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-123">Applied the latest updates to your Office Communications Server 2007 R2 environment, if you are migrating to Lync Server 2013.</span></span>

  - <span data-ttu-id="4cb3d-124">Использование построителя топологии для создания и настройки топологии.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-124">Used Topology Builder to design and configure your topology.</span></span> <span data-ttu-id="4cb3d-125">При указании рабочей нагрузки для Конференции вы выбрали вариант конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-125">While specifying the Conferencing workload, you selected the dial-in conferencing option.</span></span> <span data-ttu-id="4cb3d-126">Подробнее об определении топологии можно узнать в разделе [Определение и Настройка топологии в Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-126">For details about defining your topology, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="4cb3d-127">Вы опубликовали свою топологию и настроили интерфейс пула и сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-127">Published your topology, and set up the Front End pool or Standard Edition server.</span></span> <span data-ttu-id="4cb3d-128">Подробнее о публикации топологии и установке Lync Server 2013 можно найти в документации развертывание [Lync server 2013](lync-server-2013-deploying-lync-server.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb3d-128">For details about publishing the topology and installing Lync Server 2013, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="4cb3d-129">При установке топологии публикации веб-страница параметров конференций с телефонным подключением устанавливается на сервере переднего плана или стандартном сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-129">When you install your published topology, the Dial-in Conferencing Settings webpage is installed on the Front End Server or Standard Edition server as part of Web Services.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="4cb3d-130">Если вы изменили путь к хранилищу файлов в построителе топологии после развертывания Lync Server 2013, необходимо перезапустить помощника по конференциям и конференц-связь, чтобы использовать новый путь.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-130">If you change the path for the File Store in Topology Builder after you deploy Lync Server 2013, you need to restart the Conferencing Attendant and Conferencing Announcement applications to use the new path.</span></span>

    
    </div>

  - <span data-ttu-id="4cb3d-131">Развернутая Корпоративная голосовая связь.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-131">Deployed Enterprise Voice.</span></span> <span data-ttu-id="4cb3d-132">Если вы не развертываете корпоративную голосовую почту, вы либо развернули сервер-посредник на сервере переднего плана Enterprise Edition либо на сервер Standard Edition, либо разворачиваете отдельный сервер-посредник, и вы развернули шлюз PSTN.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-132">If you are not deploying Enterprise Voice, you either collocated a Mediation Server on the Enterprise Edition Front End Server or the Standard Edition server, or you deployed a stand-alone Mediation Server, and you deployed a PSTN gateway.</span></span> <span data-ttu-id="4cb3d-133">Подробнее о внедрении корпоративной голосовой связи можно найти [в разделе Развертывание корпоративной голосовой связи в Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-133">For details about deploying Enterprise Voice, see [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span> <span data-ttu-id="4cb3d-134">Подробнее об установке отдельного сервера-посредника и шлюза PSTN можно узнать в разделе [развертывание серверов обновлений и определение одноранговых узлов в Lync Server 2013](lync-server-2013-deploying-mediation-servers-and-defining-peers.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-134">For details about installing a stand-alone Mediation Server and PSTN gateway, see [Deploying Mediation Servers and defining peers in Lync Server 2013](lync-server-2013-deploying-mediation-servers-and-defining-peers.md) in the Deployment documentation.</span></span>

<span data-ttu-id="4cb3d-135">В следующей блок-схеме показаны действия, которые необходимо выполнить, прежде чем можно будет настроить Конференц-связь с телефонным подключением и действия, которые необходимо выполнить, чтобы настроить Конференц-связь с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-135">The following flowchart shows the steps that you must perform before you can configure dial-in conferencing and the steps that you perform to configure dial-in conferencing.</span></span>

<span data-ttu-id="4cb3d-136">**Развертывание конференц-связи с телефонным подключением**</span><span class="sxs-lookup"><span data-stu-id="4cb3d-136">**Deploying dial-in conferencing**</span></span>

<span data-ttu-id="4cb3d-137">![Блок-схема развертывания конференций с телефонным подключением](images/Gg412865.fde8c246-b5ed-4323-a6e7-af1983a5ec86(OCS.15).jpg "Блок-схема развертывания конференций с телефонным подключением")</span><span class="sxs-lookup"><span data-stu-id="4cb3d-137">![Dial-in Conferencing Deployment flowchart](images/Gg412865.fde8c246-b5ed-4323-a6e7-af1983a5ec86(OCS.15).jpg "Dial-in Conferencing Deployment flowchart")</span></span>

</div>

<div>

## <a name="dial-in-conferencing-permissions"></a><span data-ttu-id="4cb3d-138">Разрешения на Конференц-связь с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="4cb3d-138">Dial-in Conferencing Permissions</span></span>

<span data-ttu-id="4cb3d-139">Чтобы настроить Конференц-связь с телефонным подключением, необходимо использовать указанные ниже средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-139">To configure dial-in conferencing, you need to use the following administrative tools:</span></span>

  - <span data-ttu-id="4cb3d-140">управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cb3d-140">Lync Server 2013 Control Panel</span></span>

  - <span data-ttu-id="4cb3d-141">Командная консоль Lync Server</span><span class="sxs-lookup"><span data-stu-id="4cb3d-141">Lync Server Management Shell</span></span>

<span data-ttu-id="4cb3d-142">С помощью этих средств администрирования можно настраивать параметры конференц-связи с телефонным подключением, а также группы абонентов, политики и другие параметры, необходимые для конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-142">You use these administrative tools to configure dial-in conferencing settings, and the dial plans, policies, and other settings that dial-in conferencing requires.</span></span>

<span data-ttu-id="4cb3d-143">Для настройки конференц-связи с телефонным подключением требуются следующие административные роли, зависящие от задачи.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-143">Configuring dial-in conferencing requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="4cb3d-144">**CsVoiceAdministrator**   Эта роль администратора может создавать, настраивать параметры и политики, связанные с голосовой связью, и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-144">**CsVoiceAdministrator**   This administrator role can create, configure, and manage voice-related settings and policies.</span></span>

  - <span data-ttu-id="4cb3d-145">**CsUserAdministrator**   Эта роль администратора может включать и отключать пользователей для Lync Server и назначать существующим политикам, таким как политики Конференции и политики ПИН-кодов, пользователям.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-145">**CsUserAdministrator**   This administrator role can enable and disable users for Lync Server and assign existing policies, such as conferencing policies and PIN policies, to users.</span></span>

  - <span data-ttu-id="4cb3d-146">**CsAdministrator**   Эта роль администратора может выполнять все задачи CsVoiceAdministrator и CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="4cb3d-146">**CsAdministrator**   This administrator role can perform all of the tasks of CsVoiceAdministrator and CsUserAdministrator.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4cb3d-147">См. также</span><span class="sxs-lookup"><span data-stu-id="4cb3d-147">See Also</span></span>


[<span data-ttu-id="4cb3d-148">Развертывание корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cb3d-148">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  
  

<span data-ttu-id="4cb3d-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cb3d-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

