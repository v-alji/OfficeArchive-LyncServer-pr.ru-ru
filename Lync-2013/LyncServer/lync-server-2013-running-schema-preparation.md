---
title: 'Lync Server 2013: проведение подготовки схемы'
description: 'Lync Server 2013: выполняется подготовка схемы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running schema preparation
ms:assetid: 9d02bdb1-ff29-417a-bcce-b068b31207d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412729(v=OCS.15)
ms:contentKeyID: 48184911
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0991bbff7f54f8b8b9eb01fc87f752e00f3dcbfd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442196"
---
# <a name="running-active-directory-schema-preparation-in-lync-server-2013"></a><span data-ttu-id="1647f-103">Проведение подготовки схемы Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1647f-103">Running Active Directory schema preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1647f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1647f-104">

<span> </span></span></span>

<span data-ttu-id="1647f-105">_**Тема последнего изменения:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="1647f-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="1647f-106">Вы можете подготовить схему Active Directory с помощью командлетов командной консоли Setup или Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1647f-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the Active Directory schema.</span></span> <span data-ttu-id="1647f-107">Командлет, расширяющий схему Active Directory, — **Install-CsAdServerSchema**.</span><span class="sxs-lookup"><span data-stu-id="1647f-107">The cmdlet that extends the Active Directory schema is **Install-CsAdServerSchema**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1647f-108">Командлет подготовки схемы (<STRONG>Install-CsAdServerSchema</STRONG>) должен получить доступ к хозяину схемы, при этом требуется, чтобы служба удаленного реестра выполнялась, и что ключ удаленного реестра включен.</span><span class="sxs-lookup"><span data-stu-id="1647f-108">The schema preparation cmdlet (<STRONG>Install-CsAdServerSchema</STRONG>) must access the schema master, which requires that the remote registry service is running and that the remote registry key is enabled.</span></span> <span data-ttu-id="1647f-109">Если служба удаленного реестра не может быть включена на хозяине схемы, вы можете выполнить командлет локально на хозяине схемы.</span><span class="sxs-lookup"><span data-stu-id="1647f-109">If the remote registry service cannot be enabled on the schema master, you can run the cmdlet locally on the schema master.</span></span> <span data-ttu-id="1647f-110">Подробнее об удаленном доступе к реестру можно найти в статье Microsoft Knowledge Base 314837, "как управлять удаленным доступом к реестру" по адресу <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A> .</span><span class="sxs-lookup"><span data-stu-id="1647f-110">For details about registry remote access, see Microsoft Knowledge Base article 314837, "How to Manage Remote Access to the Registry," at <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A>.</span></span>



</div>

<span data-ttu-id="1647f-111">После завершения подготовки схемы вручную убедитесь, что Секция схемы реплицирована, прежде чем переходить к подготовке леса.</span><span class="sxs-lookup"><span data-stu-id="1647f-111">After you complete schema preparation, manually verify that the schema partition has been replicated before proceeding to forest preparation.</span></span> <span data-ttu-id="1647f-112">Подробности можно найти [в разделе Проверка репликации схемы Active Directory в Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="1647f-112">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="1647f-113">Подготовка схемы текущего леса с помощью программы установки</span><span class="sxs-lookup"><span data-stu-id="1647f-113">To use Setup to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="1647f-114">Войдите на сервер в лесу как член группы «Администраторы схемы» и с правами администратора на хозяине схемы.</span><span class="sxs-lookup"><span data-stu-id="1647f-114">Log on to a server in your forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="1647f-115">В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания.</span><span class="sxs-lookup"><span data-stu-id="1647f-115">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="1647f-116">Если вам будет предложено установить распространяемый компонент Microsoft Visual C++, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="1647f-116">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>

4.  <span data-ttu-id="1647f-117">Диалоговое окно установки Lync Server 2013 предлагает указать расположение для установки файлов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1647f-117">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="1647f-118">Выберите расположение по умолчанию или **перейдите** в нужное место, а затем нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="1647f-118">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>

5.  <span data-ttu-id="1647f-119">На странице Лицензионное соглашение установите флажок **я принимаю условия лицензионного соглашения**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1647f-119">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span>

6.  <span data-ttu-id="1647f-120">Установщик установит компоненты основных компонентов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1647f-120">The installer installs the Lync Server Core Components.</span></span>

7.  <span data-ttu-id="1647f-121">Когда мастер развертывания будет готов, нажмите кнопку **подготовить Active Directory**, а затем дождитесь, когда состояние развертывания будет определено.</span><span class="sxs-lookup"><span data-stu-id="1647f-121">When the Deployment Wizard is ready, click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

8.  <span data-ttu-id="1647f-122">На **шаге 1: подготовка схемы** нажмите кнопку **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="1647f-122">At **Step 1: Prepare Schema**, click **Run**.</span></span>

9.  <span data-ttu-id="1647f-123">На странице **Подготовка схемы** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1647f-123">On the **Prepare Schema** page, click **Next**.</span></span>

10. <span data-ttu-id="1647f-124">На странице **выполнения команд** подождите, пока не появится сообщение **Состояние задачи: Завершено**, а затем нажмите **Просмотреть журнал**.</span><span class="sxs-lookup"><span data-stu-id="1647f-124">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

11. <span data-ttu-id="1647f-125">В столбце **Action (действие** ) разверните узел " **Подготовьте схему**", найдите **\<Success\>** результаты выполнения в конце каждой задачи, чтобы убедиться, что подготовка схемы завершилась успешно, закройте журнал и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="1647f-125">Under the **Action** column, expand **Schema Prep**, look for the **\<Success\>** Execution Result at the end of each task to verify that schema preparation completed successfully, close the log, and then click **Finish**.</span></span>

12. <span data-ttu-id="1647f-126">Дождитесь завершения репликации службы каталогов Active Directory или принудительной репликации.</span><span class="sxs-lookup"><span data-stu-id="1647f-126">Wait for Active Directory replication to complete or force replication.</span></span>

13. <span data-ttu-id="1647f-127">Вручную убедитесь, что изменения схемы реплицированы на все другие контроллеры домена.</span><span class="sxs-lookup"><span data-stu-id="1647f-127">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="1647f-128">Подробности можно найти [в разделе Проверка репликации схемы Active Directory в Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="1647f-128">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="1647f-129">Использование командлетов для подготовки схемы текущего леса</span><span class="sxs-lookup"><span data-stu-id="1647f-129">To use cmdlets to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="1647f-130">Войдите на компьютер в лесу как член группы "Администраторы схемы" и с правами администратора на хозяине схемы.</span><span class="sxs-lookup"><span data-stu-id="1647f-130">Log on to a computer in the forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="1647f-131">Установите основные компоненты Lync Server, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="1647f-131">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="1647f-132">В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1647f-132">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="1647f-133">Если вам будет предложено установить распространяемый компонент Microsoft Visual C++, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="1647f-133">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="1647f-134">Диалоговое окно установки Lync Server 2013 предлагает указать расположение для установки файлов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1647f-134">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="1647f-135">Выберите расположение по умолчанию или **перейдите** в нужное место, а затем нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="1647f-135">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="1647f-136">На странице Лицензионное соглашение установите флажок **я принимаю условия лицензионного соглашения**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1647f-136">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="1647f-137">Установщик установит основные компоненты Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1647f-137">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="1647f-138">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="1647f-138">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="1647f-139">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1647f-139">Run:</span></span>
    
        Install-CsAdServerSchema [-Ldf <directory where the .ldf file is located>] 
    
    <span data-ttu-id="1647f-140">Если параметр LDF не указан, значение по умолчанию — путь установки Lync Server 2013, который читается из реестра.</span><span class="sxs-lookup"><span data-stu-id="1647f-140">If you do not specify the Ldf parameter, the default value is the Lync Server 2013 installation path that is read from the registry.</span></span>
    
    <span data-ttu-id="1647f-141">Например:</span><span class="sxs-lookup"><span data-stu-id="1647f-141">For example:</span></span>
    
        Install-CsAdServerSchema -Ldf "C:\Program Files\Microsoft Lync Server 2013\Deployment\Setup"

5.  <span data-ttu-id="1647f-142">С помощью следующего командлета убедитесь в том, что подготовка схемы завершилась с завершением.</span><span class="sxs-lookup"><span data-stu-id="1647f-142">Use the following cmdlet to verify that schema preparation ran to completion.</span></span>
    
        Get-CsAdServerSchema 
    
    <span data-ttu-id="1647f-143">Этот командлет возвращает значение **\_ состояния версии схемы \_ \_ Current** , если подготовка схемы завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="1647f-143">This cmdlet returns a value of **SCHEMA\_VERSION\_STATE\_CURRENT** if schema preparation was successful.</span></span>

6.  <span data-ttu-id="1647f-144">Дождитесь завершения репликации службы каталогов Active Directory или принудительной репликации.</span><span class="sxs-lookup"><span data-stu-id="1647f-144">Wait for Active Directory replication to complete or force replication.</span></span>

7.  <span data-ttu-id="1647f-145">Вручную убедитесь, что изменения схемы реплицированы на все другие контроллеры домена.</span><span class="sxs-lookup"><span data-stu-id="1647f-145">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="1647f-146">Подробности можно найти [в разделе Проверка репликации схемы Active Directory в Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="1647f-146">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1647f-147">См. также</span><span class="sxs-lookup"><span data-stu-id="1647f-147">See Also</span></span>


[<span data-ttu-id="1647f-148">Проверка репликации схемы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1647f-148">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)  


[<span data-ttu-id="1647f-149">Подготовка схемы Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1647f-149">Preparing the Active Directory schema in Lync Server 2013</span></span>](lync-server-2013-preparing-the-active-directory-schema.md)  
  

<span data-ttu-id="1647f-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1647f-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

