---
title: Развертывание пула Lync Server 2013 Pilot
description: Развертывание пула Lync Server 2013 Pilot.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy Lync Server 2013 pilot pool
ms:assetid: a81aba1e-e636-434b-8c56-4150435bb55d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205144(v=OCS.15)
ms:contentKeyID: 48185028
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a599cee1719f773ebbf3cf5a71405aa9b7259261
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398329"
---
# <a name="deploy-lync-server-2013-pilot-pool"></a><span data-ttu-id="3d5b3-103">Развертывание пула Lync Server 2013 Pilot</span><span class="sxs-lookup"><span data-stu-id="3d5b3-103">Deploy Lync Server 2013 pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d5b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d5b3-104">

<span> </span></span></span>

<span data-ttu-id="3d5b3-105">_**Тема последнего изменения:** 2013-11-22_</span><span class="sxs-lookup"><span data-stu-id="3d5b3-105">_**Topic Last Modified:** 2013-11-22_</span></span>

<span data-ttu-id="3d5b3-106">Один из первых шагов, необходимых для перехода на Lync Server 2013, — это развертывание пилотного пула.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-106">One of the first steps required for migration to Lync Server 2013 is to deploy a pilot pool.</span></span> <span data-ttu-id="3d5b3-107">Пилотный пул — это то, что вы тестируете сосуществование Lync Server 2013 с помощью развертывания Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-107">The pilot pool is where you test coexistence of Lync Server 2013 with your Lync Server 2010 deployment.</span></span> <span data-ttu-id="3d5b3-108">Сосуществование — это временное состояние, которое продолжается до тех пор, пока вы не переместит всех пользователей и пулы на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-108">Coexistence is a temporary state that lasts until you have moved all users and pools to Lync Server 2013.</span></span>

<span data-ttu-id="3d5b3-109">При развертывании пилотного пула вы используете мастер определения нового пула переднего плана.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-109">When you deploy a pilot pool, you use the Define New Front End Pool wizard.</span></span> <span data-ttu-id="3d5b3-110">Вы должны развернуть те же функции и рабочие нагрузки в пуле Lync Server 2013 Pilot, который есть в вашем пуле Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-110">You should deploy the same features and workloads in your Lync Server 2013 pilot pool that you have in your Lync Server 2010 pool.</span></span> <span data-ttu-id="3d5b3-111">Если вы развернули сервер архивации, сервер мониторинга или System Center Operations Manager для архивации или наблюдения за средой Lync Server 2010 и хотите продолжить архивацию или мониторинг во время миграции, необходимо также развернуть эти функции в среде пилотной среды.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-111">If you deployed Archiving Server, Monitoring Server, or System Center Operations Manager for archiving or monitoring your Lync Server 2010 environment, and you want to continue archiving or monitoring throughout the migration, you need to also deploy these features in your pilot environment.</span></span> <span data-ttu-id="3d5b3-112">Версия, развернутая для архивации или наблюдения за средой Lync Server 2010, не захватывает данные в среде Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-112">The version you deployed to archive or monitor your Lync Server 2010 environment will not capture data in your Lync Server 2013 environment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3d5b3-113">В приведенной ниже процедуре описаны возможности и параметры, которые следует рассмотреть в рамках всего процесса развертывания пилотного пула.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-113">The following procedure discusses features and settings you should consider as part of your overall pilot pool deployment process.</span></span> <span data-ttu-id="3d5b3-114">В этом разделе выделены только ключевые моменты, которые следует принимать во время развертывания пилотного пула.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-114">This section only highlights key points you should consider as part of your pilot pool deployment.</span></span> <span data-ttu-id="3d5b3-115">Подробные инструкции можно найти в руководстве <A href="lync-server-2013-deploying-lync-server.md">развертывание Lync Server 2013</A> .</span><span class="sxs-lookup"><span data-stu-id="3d5b3-115">For detailed steps, refer to the <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A> deployment guide.</span></span>



</div>

<span data-ttu-id="3d5b3-116">**Развертывание пула Lync Server 2013 Pilot**</span><span class="sxs-lookup"><span data-stu-id="3d5b3-116">**To deploy a Lync Server 2013 pilot pool**</span></span>

1.  <span data-ttu-id="3d5b3-117">Войдите на компьютер, где установлен построитель топологий, с использованием учетной записи, входящей в группу администраторов домена и группу RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-117">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="3d5b3-118">Разверните дерево, пока не дойдете до уровня "внешние **серверные пулы Lync Server 2013** **Enterprise Edition**".</span><span class="sxs-lookup"><span data-stu-id="3d5b3-118">Expand the tree until you reach **Lync Server 2013** **Enterprise Edition Front End pools**.</span></span>

3.  <span data-ttu-id="3d5b3-119">Щелкните правой кнопкой мыши **Пулы переднего плана Enterprise Edition** и выберите **создать пул переднего плана**.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-119">Right click **Enterprise Edition Front End pools**, and select **New Front End Pool**.</span></span>
    
    <span data-ttu-id="3d5b3-120">![Подменю "Выбор пула серверов Topology Builder"](images/JJ205144.c2feed27-3418-42a6-a254-76e83607db9c(OCS.15).jpg "Подменю "Выбор пула серверов Topology Builder"")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-120">![Topology Builder Server pool selection submenu](images/JJ205144.c2feed27-3418-42a6-a254-76e83607db9c(OCS.15).jpg "Topology Builder Server pool selection submenu")</span></span>

4.  <span data-ttu-id="3d5b3-121">Введите полное доменное имя пула.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-121">Enter the pool FQDN.</span></span> <span data-ttu-id="3d5b3-122">При определении пилотного пула вы можете выбрать развертывание пула переднего плана Enterprise Edition или сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-122">When you define your pilot pool, you can choose to deploy an Enterprise Edition Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="3d5b3-123">Для Lync Server 2013 не требуется, чтобы функции пилотного пула соответствовали развернутым в пуле старого.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-123">Lync Server 2013 does not require that your pilot pool features match what was deployed in your legacy pool.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="3d5b3-124">Полное доменное имя (FQDN) для пула, которое вы определяете для пилотного пула, должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-124">The pool or server fully qualified domain name (FQDN) that you define for the pilot pool must be unique.</span></span> <span data-ttu-id="3d5b3-125">Оно не может совпадать с именем развернутого пула Lync Server 2010 или других серверов, развернутых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-125">It cannot match the name of the currently deployed Lync Server 2010 pool, or any other servers currently deployed.</span></span>

    
    </div>
    
    <span data-ttu-id="3d5b3-126">![Страница определения полного доменного имени мастера создания пула переднего плана](images/JJ205144.c5fd138c-e75a-413a-827f-b1461c996d40(OCS.15).jpg "Страница определения полного доменного имени мастера создания пула переднего плана")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-126">![Define New Front End Pool Wizard FQDN page](images/JJ205144.c5fd138c-e75a-413a-827f-b1461c996d40(OCS.15).jpg "Define New Front End Pool Wizard FQDN page")</span></span>

5.  <span data-ttu-id="3d5b3-127">На странице " **Выбор компонентов** " установите флажки для нужных функций в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-127">On the **Select features** page, select the check boxes for the features that you want on this Front End pool.</span></span> <span data-ttu-id="3d5b3-128">Например, если вы разворачиваете только возможности обмена мгновенными сообщениями и сведениями о присутствии, установите флажок Конференц-связь, чтобы разрешить многофакторную передачу мгновенных сообщений, но не устанавливайте флажки конференции с телефонным подключением, корпоративной голосовой связи и управления допуском звонков, так как они представляют собой голосовую, видеосвязь и возможности совместной конференции.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-128">For example, if you are deploying only instant messaging (IM) and presence features, you would select the Conferencing check box to allow multiparty IM, but would not select the Dial-in (PSTN) conferencing, Enterprise Voice, or Call Admission Control check boxes, because they represent voice, video, and collaborative conferencing features.</span></span> <span data-ttu-id="3d5b3-129">Дополнительные сведения о выборе функций можно найти в разделе [Определение и Настройка внешнего пула и сервера Standard Edition в Lync server 2013](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-129">For additional information on selecting features, see [Define and configure a Front End pool or Standard Edition server in Lync Server 2013](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md) in the Deployment documentation.</span></span>
    
    <span data-ttu-id="3d5b3-130">![Страница выбора компонентов в пуле интерфейса пользователя](images/JJ204718.5c3f3ff9-6e17-4d66-9b13-3bd55b38246b(OCS.15).jpg "Страница выбора компонентов в пуле интерфейса пользователя")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-130">![Front End Pool Select features page](images/JJ204718.5c3f3ff9-6e17-4d66-9b13-3bd55b38246b(OCS.15).jpg "Front End Pool Select features page")</span></span>

6.  <span data-ttu-id="3d5b3-131">На странице **Выбор размещенных ролей сервера** мы рекомендуем вам разделять сервер-посредник в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-131">On the **Select collocated server roles** page, we recommend you collocate the Mediation Server in Lync Server 2013.</span></span> <span data-ttu-id="3d5b3-132">При объединении устаревшей топологии с Lync Server 2013 необходимо сначала выписать сервер исправлений Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-132">When merging a legacy topology with Lync Server 2013, we require that you first collocate the Lync Server 2010 Mediation Server.</span></span> <span data-ttu-id="3d5b3-133">После слияния топологий и настройки сервера-исправления Lync Server 2013 вы можете решить, нужно ли сохранять Объединенный сервер или изменить его на отдельный сервер, когда вы перемещаете роль сервера-посредника на Lync Server 2013 позже в процессе развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-133">After merging the topologies and configuring the Lync Server 2013 Mediation Server, you can decide whether to keep the collocated Mediation Server, or change it to a stand-alone server when you move the Mediation Server role to Lync Server 2013 later in the deployment process.</span></span>
    
    <span data-ttu-id="3d5b3-134">![Пул переднего плана выберите страницу "размещенные роли сервера"](images/JJ204718.e00b7eba-010b-44ed-b0a6-6ab3e534fb8c(OCS.15).jpg "Пул переднего плана выберите страницу "размещенные роли сервера"")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-134">![Front End Pool Select collocated server roles page](images/JJ204718.e00b7eba-010b-44ed-b0a6-6ab3e534fb8c(OCS.15).jpg "Front End Pool Select collocated server roles page")</span></span>

7.  <span data-ttu-id="3d5b3-135">**В процессе** развертывания пилотного пула не выбирайте **пул краев, который будет использоваться компонентом мультимедиа для этого параметра пула переднего плана** .</span><span class="sxs-lookup"><span data-stu-id="3d5b3-135">On the **Associate server roles with this Front End pool** page, during pilot pool deployment, do not choose the **Enable an Edge pool to be used by the media component of this Front End pool** option.</span></span> <span data-ttu-id="3d5b3-136">Это функция, которую вы сможете включить и подключить к Интернету на более поздней стадии миграции.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-136">This is a feature you will enable and bring online in a later phase of migration.</span></span> <span data-ttu-id="3d5b3-137">Не Запусти этот параметр, пока не будет снят флажок.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-137">Keep this setting cleared for now.</span></span>
    
    <span data-ttu-id="3d5b3-138">![Связывание ролей сервера со страницей пула переднего плана](images/JJ204718.2d95a798-ad76-4dad-9392-ce41f4d938d1(OCS.15).jpg "Связывание ролей сервера со страницей пула переднего плана")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-138">![Associate server roles with Front End pool page](images/JJ204718.2d95a798-ad76-4dad-9392-ce41f4d938d1(OCS.15).jpg "Associate server roles with Front End pool page")</span></span>

8.  <span data-ttu-id="3d5b3-139">На странице **выберите сервер Office Web Apps** нажмите кнопку **создать** и укажите полное доменное имя сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-139">On the **Select an Office Web Apps Server** page, click **New**, and specify the FQDN of the application server.</span></span>
    
    <span data-ttu-id="3d5b3-140">![Определение новых свойств полного доменного имени сервера Office Web Apps](images/JJ204718.25c6b455-f1b8-4326-a569-6e338153d398(OCS.15).jpg "Определение новых свойств полного доменного имени сервера Office Web Apps")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-140">![Define New Office Web Apps Server FQDN properties](images/JJ204718.25c6b455-f1b8-4326-a569-6e338153d398(OCS.15).jpg "Define New Office Web Apps Server FQDN properties")</span></span>

9.  <span data-ttu-id="3d5b3-141">На странице **Определение хранилища сервера SQL** Server при определении хранилища SQL Server для архивации и мониторинга сервера Lync Server выберите экземпляр SQL Server, созданный ранее для lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-141">On the **Define the Archiving SQL Server store** page, when defining the SQL Server store for both Lync Server Archiving and Monitoring, select the SQL Server instance created earlier for Lync Server 2013.</span></span>
    
    <span data-ttu-id="3d5b3-142">![Страница "определение архива SQL Server — хранилище"](images/JJ204718.0f76f1dc-d0d7-42a0-aea3-400b8e1f35cd(OCS.15).jpg "Страница "определение архива SQL Server — хранилище"")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-142">![Define Archiving SQL Server store page](images/JJ204718.0f76f1dc-d0d7-42a0-aea3-400b8e1f35cd(OCS.15).jpg "Define Archiving SQL Server store page")</span></span>

10. <span data-ttu-id="3d5b3-143">Чтобы опубликовать топологию, щелкните узел **Lync Server** правой кнопкой мыши и выберите команду **топология публикации**.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-143">To publish your topology, right-click the **Lync Server** node, and then click **Publish Topology**.</span></span>
    
    <span data-ttu-id="3d5b3-144">![Построитель топологии, отображающий настроенную топологию](images/JJ205144.c3eafa20-159e-4355-a23d-9f72aeb26037(OCS.15).jpg "Построитель топологии, отображающий настроенную топологию")</span><span class="sxs-lookup"><span data-stu-id="3d5b3-144">![Topology Builder displaying a configured topology](images/JJ205144.c3eafa20-159e-4355-a23d-9f72aeb26037(OCS.15).jpg "Topology Builder displaying a configured topology")</span></span>

11. <span data-ttu-id="3d5b3-145">После завершения процесса публикации нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-145">When the publish process has completed, click **Finish**.</span></span>

<span data-ttu-id="3d5b3-146">Чтобы установить локальную копию хранилища конфигурации и запустить необходимые службы, ознакомьтесь со сведениями [о настройке внешних серверов и пулов интерфейсов для Lync Server 2013](lync-server-2013-setting-up-front-end-servers-and-front-end-pools.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-146">To install a local copy of the configuration store and start the required services, see [Setting up Front End Servers and Front End pools for Lync Server 2013](lync-server-2013-setting-up-front-end-servers-and-front-end-pools.md) in the Deployment documentation.</span></span>


<span data-ttu-id="3d5b3-147"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d5b3-147"></div>

<span> </span>

</div>

</div>

</span></span></div>

