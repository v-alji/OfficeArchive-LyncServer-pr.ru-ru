---
title: 'Lync Server 2013: проведение подготовки леса'
description: 'Lync Server 2013: запуск подготовки леса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running forest preparation
ms:assetid: 9d62f7be-bcfe-421d-8d8a-225567102a35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412732(v=OCS.15)
ms:contentKeyID: 48184991
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad3ef2d7583d541701d6606946ca1df1bbd8cf23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442217"
---
# <a name="running-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="1a138-103">Проведение подготовки леса для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a138-103">Running forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1a138-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1a138-104">

<span> </span></span></span>

<span data-ttu-id="1a138-105">_**Тема последнего изменения:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="1a138-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="1a138-106">Для подготовки леса можно использовать командлеты командной консоли Setup или Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1a138-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the forest.</span></span> <span data-ttu-id="1a138-107">Командлет, подготавливающий лес, — **Enable-CsAdForest**.</span><span class="sxs-lookup"><span data-stu-id="1a138-107">The cmdlet that prepares the forest is **Enable-CsAdForest**.</span></span>

<span data-ttu-id="1a138-108">После подготовки леса необходимо убедиться, что глобальные параметры были реплицированы перед выполнением подготовки домена.</span><span class="sxs-lookup"><span data-stu-id="1a138-108">After you prepare the forest, you must verify that global settings have been replicated before running domain preparation.</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-forest"></a><span data-ttu-id="1a138-109">Подготовка леса с помощью программы установки</span><span class="sxs-lookup"><span data-stu-id="1a138-109">To use Setup to prepare the forest</span></span>

1.  <span data-ttu-id="1a138-110">Войдите в систему на компьютере, который входит в состав домена, в качестве участника группы администраторов предприятия для корневого домена леса.</span><span class="sxs-lookup"><span data-stu-id="1a138-110">Log on to a computer that is joined to a domain as a member of the Enterprise Admins group for the forest root domain.</span></span>

2.  <span data-ttu-id="1a138-111">В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания.</span><span class="sxs-lookup"><span data-stu-id="1a138-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="1a138-112">Нажмите **Подготовить Active Directory** и подождите, пока будет определено состояние развертывания.</span><span class="sxs-lookup"><span data-stu-id="1a138-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="1a138-113">На **шаге 3: подготовка текущего леса** нажмите кнопку **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="1a138-113">At **Step 3: Prepare Current Forest**, click **Run**.</span></span>

5.  <span data-ttu-id="1a138-114">На странице **Подготовка леса** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1a138-114">On the **Prepare Forest** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1a138-115">С помощью подготовки леса вы можете выбрать, куда следует поместить универсальные группы для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1a138-115">Forest Preparation allows you to choose where to place the Universal Groups for Lync Server 2013.</span></span> <span data-ttu-id="1a138-116">Выберите расположение в соответствии с требованиями организации.</span><span class="sxs-lookup"><span data-stu-id="1a138-116">Choose a location that is consistent with the requirements of your organization.</span></span>

    
    </div>

6.  <span data-ttu-id="1a138-117">На странице **Выполнение команд** найдите запись **Состояние задачи: Завершено**, затем нажмите кнопку **Просмотр журнала**.</span><span class="sxs-lookup"><span data-stu-id="1a138-117">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="1a138-118">В столбце **Action (действие** ) разверните элемент " **Подготовка леса**", найдите **\<Success\>** результаты выполнения в конце каждой задачи, чтобы убедиться, что подготовка леса успешно завершена, закройте журнал и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="1a138-118">Under the **Action** column, expand **Forest Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that forest preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="1a138-119">Дождитесь завершения репликации Active Directory или принудительно выполните репликацию на все контроллеры домена, указанные в оснастке " **сайты и службы" в службе каталогов Active Directory** для корневого контроллера домена леса, перед тем как выполнять подготовку домена.</span><span class="sxs-lookup"><span data-stu-id="1a138-119">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span> <span data-ttu-id="1a138-120">Принудительная репликация между контроллерами домена на всех сайтах Active Directory для репликации в течение минут между сайтами.</span><span class="sxs-lookup"><span data-stu-id="1a138-120">Force replication between the domain controllers in all Active Directory sites to cause replication within the sites to occur within minutes.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-forest"></a><span data-ttu-id="1a138-121">Использование командлетов для подготовки леса</span><span class="sxs-lookup"><span data-stu-id="1a138-121">To use cmdlets to prepare the forest</span></span>

1.  <span data-ttu-id="1a138-122">Войдите в систему на компьютере, который входит в состав домена, в качестве члена группы администраторов домена в корневом домене леса.</span><span class="sxs-lookup"><span data-stu-id="1a138-122">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="1a138-123">Установите основные компоненты Lync Server, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="1a138-123">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="1a138-124">В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1a138-124">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="1a138-125">Если вам будет предложено установить распространяемый компонент Microsoft Visual C++, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="1a138-125">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="1a138-126">Диалоговое окно установки Lync Server 2013 предлагает указать расположение для установки файлов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1a138-126">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="1a138-127">Выберите расположение по умолчанию или **перейдите** в нужное место, а затем нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="1a138-127">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="1a138-128">На странице Лицензионное соглашение установите флажок **я принимаю условия лицензионного соглашения**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1a138-128">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="1a138-129">Установщик установит основные компоненты Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1a138-129">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="1a138-130">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="1a138-130">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="1a138-131">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1a138-131">Run:</span></span>
    
        Enable-CsAdForest [-GroupDomain <FQDN of the domain in which to create the universal groups>]
    
    <span data-ttu-id="1a138-132">Например:</span><span class="sxs-lookup"><span data-stu-id="1a138-132">For example:</span></span>
    
        Enable-CsAdForest -GroupDomain domain1.contoso.com 
    
    <span data-ttu-id="1a138-133">Если параметр GroupDomain не указан, значение по умолчанию — локальный домен.</span><span class="sxs-lookup"><span data-stu-id="1a138-133">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span> <span data-ttu-id="1a138-134">Если универсальные группы были созданы ранее в домене, который не является доменом по умолчанию, необходимо явно задать параметр GroupDomain.</span><span class="sxs-lookup"><span data-stu-id="1a138-134">If universal groups were created previously in a domain that is not the default domain, you must specify the GroupDomain parameter explicitly.</span></span>

5.  <span data-ttu-id="1a138-135">Дождитесь завершения репликации Active Directory или принудительно выполните репликацию на все контроллеры домена, указанные в оснастке " **сайты и службы" в службе каталогов Active Directory** для корневого контроллера домена леса, перед тем как выполнять подготовку домена.</span><span class="sxs-lookup"><span data-stu-id="1a138-135">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span>

6.  <span data-ttu-id="1a138-136">Убедитесь, что подготовка леса выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1a138-136">Verify that forest preparation was successful.</span></span> <span data-ttu-id="1a138-137">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1a138-137">Run:</span></span>
    
        Get-CsAdForest 
    
    <span data-ttu-id="1a138-138">Этот командлет возвращает значение **\_ FORESTSETTINGS \_ состоянием \_ "LC** ", если подготовка леса была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1a138-138">This cmdlet returns a value of **LC\_FORESTSETTINGS\_STATE\_READY** if forest preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1a138-139">См. также</span><span class="sxs-lookup"><span data-stu-id="1a138-139">See Also</span></span>


[<span data-ttu-id="1a138-140">Использование командлетов для отмены подготовки леса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a138-140">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)  


[<span data-ttu-id="1a138-141">Подготовка леса для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a138-141">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="1a138-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1a138-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

