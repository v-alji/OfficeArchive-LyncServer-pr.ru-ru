---
title: 'Lync Server 2013: процедуры аварийного восстановления группы ответа'
description: Процедуры аварийного восстановления для групп ответов Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group disaster recovery procedures
ms:assetid: b49577b7-0ca3-4f20-b614-f3a2a0046b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205186(v=OCS.15)
ms:contentKeyID: 48185171
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9021fb75c8f937bfd298578a9241d6256d26d85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436302"
---
# <a name="response-group-disaster-recovery-procedures-in-lync-server-2013"></a><span data-ttu-id="0b5a3-103">Процедуры аварийного восстановления группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b5a3-103">Response group disaster recovery procedures in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b5a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b5a3-104">

<span> </span></span></span>

<span data-ttu-id="0b5a3-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0b5a3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0b5a3-106">На этапе восстановления после сбоя в аварийном восстановлении группы ответа находятся в нескольких пулах: в основном пуле (который недоступен) и в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-106">During the failover phase of disaster recovery, the response groups reside in multiple pools: in the primary pool (which is unavailable) and in the backup pool.</span></span> <span data-ttu-id="0b5a3-107">Группы ответа в обоих пулах имеют одинаковое имя и одного и того же владельца (основного пула), но у них разные родители.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-107">The response groups in both pools have the same name and the same owner (the primary pool), but they have different parents.</span></span> <span data-ttu-id="0b5a3-108">В течение этого времени командлеты группы ответа работают немного по-другому.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-108">During this time, Response Group cmdlets work a little differently.</span></span> <span data-ttu-id="0b5a3-109">Не забудьте использовать параметры, как указано в описанной ниже процедуре.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-109">Be sure to use parameters as specified in the following procedure.</span></span> <span data-ttu-id="0b5a3-110">Сведения о том, как работают командлеты на этапе перехода на другой ресурс, приведены в статье сведения о переходе на веб – странице блога "Lync Server 2013: восстановление групп ответов во время аварийного восстановления" [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957)</span><span class="sxs-lookup"><span data-stu-id="0b5a3-110">For details about how cmdlets work during the failover phase, see NextHop blog article "Lync Server 2013: Recovering Response Groups During Disaster Recovery" at [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957).</span></span> <span data-ttu-id="0b5a3-111">Эта статья в блоге также относится к выпущенной версии Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-111">This blog article also applies to the released version of Lync Server 2013.</span></span>

<span data-ttu-id="0b5a3-112">Выполните действия, описанные в приведенной ниже процедуре, для подготовки и выполнения аварийного восстановления для службы группы ответа Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-112">Use the steps in the following procedure to prepare for and perform disaster recovery for Lync Server Response Group service.</span></span>

<div>

## <a name="to-fail-over-and-fail-back-response-group"></a><span data-ttu-id="0b5a3-113">Группа ответа для отработки отказа и отката</span><span class="sxs-lookup"><span data-stu-id="0b5a3-113">To fail over and fail back Response Group</span></span>

1.  <span data-ttu-id="0b5a3-114">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="0b5a3-115">Регулярное выполнение резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-115">Routinely perform backups.</span></span> <span data-ttu-id="0b5a3-116">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-116">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="0b5a3-117">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-117">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimary.zip"

3.  <span data-ttu-id="0b5a3-118">Во время сбоя после перехода на другой ресурс в пул резервной копии импортируйте группы ответа в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-118">During an outage, after failover to the backup pool, import the response groups to the backup pool.</span></span> <span data-ttu-id="0b5a3-119">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-119">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<backup pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="0b5a3-120">Если вы хотите заменить параметры уровня приложения в пуле резервных копий параметрами из основного пула, добавьте параметр – ReplaceExistingSettings.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-120">If you want to replace the application-level settings in the backup pool with the settings from the primary pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="0b5a3-121">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-121">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:backup.contoso.com" -FileName "C:\RgsExportPrimary.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="0b5a3-122">Если вы не заменили параметры в пуле резервных копий и не сможете восстановить основной пул, настройки основного пула будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-122">If you do not replace the settings in the backup pool and the primary pool can't be recovered, the primary pool settings will be lost.</span></span> <span data-ttu-id="0b5a3-123">Подробные сведения можно найти <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">в разделе Планирование аварийного восстановления групп ответов в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-123">For details, see <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">Planning for response group disaster recovery in Lync Server 2013</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="0b5a3-124">Убедитесь, что импорт прошел успешно, отображая импортированные группы ответа.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-124">Verify that the import was successful by displaying the imported response groups.</span></span> <span data-ttu-id="0b5a3-125">Импортированные группы ответов по-прежнему принадлежат основным пулам.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-125">The imported response groups are still owned by the primary pool.</span></span> <span data-ttu-id="0b5a3-126">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-126">Do the following:</span></span>
    
      - <span data-ttu-id="0b5a3-127">Отобразите все рабочие процессы в пуле резервных копий, которым владеет основной пул, и убедитесь, что все основные рабочие процессы пула включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-127">Display all the workflows in the backup pool that are owned by the primary pool, and verify that all the primary pool workflows are included.</span></span> <span data-ttu-id="0b5a3-128">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-128">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0b5a3-129">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-129">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com"
    
      - <span data-ttu-id="0b5a3-130">Отобразите все очереди в пуле резервных копий, владельцем которых является основной пул, и убедитесь, что все очереди основного пула включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-130">Display all the queues in the backup pool that are owned by the primary pool, and verify that all the primary pool queues are included.</span></span> <span data-ttu-id="0b5a3-131">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-131">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0b5a3-132">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-132">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="0b5a3-133">Отобразить все группы агентов в пуле резервных копий, владельцем которых является основной пул, и убедиться в том, что все группы агентов основного пула включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-133">Display all the agent groups in the backup pool that are owned by the primary pool, and verify that all the primary pool agent groups are included.</span></span> <span data-ttu-id="0b5a3-134">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-134">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0b5a3-135">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-135">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="0b5a3-136">Отображение всех рабочих часов в пуле резервных копий, принадлежащих основным пулам, и проверка того, что все основные часы бизнеса включены в бизнес-пул.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-136">Display all the hours of business in the backup pool that are owned by the primary pool, and verify that all the primary pool hours of business are included.</span></span> <span data-ttu-id="0b5a3-137">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-137">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0b5a3-138">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-138">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="0b5a3-139">Отобразить все наборы праздников в пуле резервных копий, владельцем которых является основной пул, и убедиться, что все наборы праздников основного пула включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-139">Display all the holiday sets in the backup pool that are owned by the primary pool, and verify that all the primary pool holiday sets are included.</span></span> <span data-ttu-id="0b5a3-140">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-140">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0b5a3-141">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-141">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
    <span data-ttu-id="0b5a3-142">Кроме того, вы можете отобразить все группы ответов в пуле резервных копий, в том числе владельцами основного пула и владельцами из пула резервных копий с помощью параметра – ShowAll вместо параметра – owner.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-142">Alternatively, you can display all the response groups in the backup pool, including the ones owned by the primary pool and the ones owned by the backup pool by using the –ShowAll parameter instead of the –Owner parameter.</span></span> <span data-ttu-id="0b5a3-143">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-143">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -ShowAll
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0b5a3-144">Необходимо использовать либо параметр – ShowAll, либо параметр – owner.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-144">You must use either the –ShowAll parameter or the –Owner parameter.</span></span> <span data-ttu-id="0b5a3-145">Если вы не используете ни один из этих параметров, группы ответа, импортированные в пул резервных копий, не будут указаны в результатах, возвращенных командлетами.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-145">If you do not use either of these parameters, the response groups that you imported to the backup pool will not be listed in the results returned by the cmdlets.</span></span>

    
    </div>

5.  <span data-ttu-id="0b5a3-146">Убедитесь, что импорт выполнен успешно, поместив вызов в импортированную группу ответа и подтверждаю, что вызов обрабатывается правильно.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-146">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="0b5a3-147">Агенты запросов, являющиеся членами формальных групп агента, для входа в группы агента в пуле резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-147">Request agents who are members of formal agent groups to sign in to their agent groups in the backup pool.</span></span>

7.  <span data-ttu-id="0b5a3-148">Управление импортированными группами ответа и их изменение в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-148">Manage and modify the imported response groups as usual.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0b5a3-149">Группы ответа находятся в пуле резервных копий, поэтому для управления ими вы должны использовать командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-149">While the response groups are in the backup pool, you need to use Lync Server Management Shell to manage them.</span></span> <span data-ttu-id="0b5a3-150">Вы не можете использовать панель управления Lync Server для управления группами ответа, которые вы импортировали в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-150">You cannot use Lync Server Control Panel to manage the response groups that you imported to the backup pool.</span></span>

    
    </div>

8.  <span data-ttu-id="0b5a3-151">После восстановления основного пула и завершения восстановления, экспортируйте группы ответов основного пула, которые были импортированы в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-151">After the primary pool is restored and failback is complete, export the primary pool response groups that were imported to the backup pool.</span></span> <span data-ttu-id="0b5a3-152">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-152">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:<backup pool FQDN> -Owner ApplicationServer:<primary pool FQDN> -FileName "<backup path and file name>"

9.  <span data-ttu-id="0b5a3-153">Импортируйте группы ответа обратно в основной пул.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-153">Import the response groups back to the primary pool.</span></span> <span data-ttu-id="0b5a3-154">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-154">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>"
    
    <span data-ttu-id="0b5a3-155">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-155">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:primary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0b5a3-156">Если вы перестраиваете пул во время восстановления, независимо от того, есть ли у него другое полное доменное имя (FQDN), необходимо использовать параметр – OverwriteOwner.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-156">If you rebuild a pool during recovery, whether with the same or a different fully qualified domain name (FQDN), you need to use the –OverwriteOwner parameter.</span></span> <span data-ttu-id="0b5a3-157">Как правило, вы всегда можете использовать параметр – OverwriteOwner при импорте групп ответа обратно в основной пул.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-157">As a rule of thumb, you can always use the –OverwriteOwner parameter when you import response groups back to the primary pool.</span></span>

    
    </div>
    
    <span data-ttu-id="0b5a3-158">Если вы развернули новый пул (с таким же или другим полным доменным именем) для замены основного пула и хотите использовать параметры уровня приложения из пула резервного копирования для нового пула, добавьте параметр – ReplaceExistingSettings.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-158">If you deployed a new pool (with the same or a different FQDN) to replace the primary pool, and you want to use the application-level settings from the backup pool for the new pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="0b5a3-159">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-159">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<new primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>" -ReplaceExistingSettings
    
    <span data-ttu-id="0b5a3-160">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-160">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:newprimary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0b5a3-161">Если вы не хотите заменять параметры уровня приложения и звуковой файл для хранения музыки по умолчанию для нового пула с параметрами из пула резервных копий, в новом пуле будут использоваться параметры по умолчанию на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-161">If you don't want to replace the application-level settings and default music-on-hold audio file for the new pool with the settings from the backup pool, the new pool will use the default application-level settings.</span></span>

    
    </div>

10. <span data-ttu-id="0b5a3-162">Убедитесь, что импорт возвращен в основной пул, отображая импортированную конфигурацию группы ответа.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-162">Verify that the import back to the primary pool was successful by displaying the imported response group configuration.</span></span> <span data-ttu-id="0b5a3-163">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-163">Do the following:</span></span>
    
      - <span data-ttu-id="0b5a3-164">Отобразите все рабочие процессы в основном пуле и убедитесь, что все импортированные рабочие процессы включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-164">Display all the workflows in the primary pool, and verify that all the imported workflows are included.</span></span> <span data-ttu-id="0b5a3-165">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-165">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0b5a3-166">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-166">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer: primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0b5a3-167">Отобразите все очереди в основном пуле и убедитесь, что все импортированные очереди включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-167">Display all the queues in the primary pool, and verify that all the imported queues are included.</span></span> <span data-ttu-id="0b5a3-168">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-168">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0b5a3-169">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-169">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0b5a3-170">Отобразить все группы агентов в основном пуле и убедиться, что все импортированные группы агентов включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-170">Display all the agent groups in the primary pool, and verify that all the imported agent groups are included.</span></span> <span data-ttu-id="0b5a3-171">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-171">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer: <primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0b5a3-172">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-172">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0b5a3-173">Отображение всех рабочих часов в основном пуле и проверка того, что все импортированные часы бизнеса включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-173">Display all the hours of business in the primary pool, and verify that all the imported hours of business are included.</span></span> <span data-ttu-id="0b5a3-174">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-174">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0b5a3-175">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-175">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0b5a3-176">Отобразите все наборы праздников в основном пуле и убедитесь, что все импортированные наборы праздников включены.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-176">Display all the holiday sets in the primary pool, and verify that all the imported holiday sets are included.</span></span> <span data-ttu-id="0b5a3-177">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-177">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0b5a3-178">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-178">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll

11. <span data-ttu-id="0b5a3-179">Убедитесь, что импорт выполнен успешно, поместив вызов в импортированную группу ответа и подтверждаю, что вызов обрабатывается правильно.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-179">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

12. <span data-ttu-id="0b5a3-180">При необходимости удалите группы ответа, принадлежащие основным пулам из пула резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-180">Optionally, remove the response groups owned by the primary pool from the backup pool.</span></span> <span data-ttu-id="0b5a3-181">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-181">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>" -RemoveExportedConfiguration
    
    <span data-ttu-id="0b5a3-182">Например:</span><span class="sxs-lookup"><span data-stu-id="0b5a3-182">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimaryUpdated.zip" -RemoveExportedConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0b5a3-183">На этом этапе создается новый файл с экспортированной конфигурацией, а затем он удаляется из пула резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-183">This step creates a new file with the exported configuration, and then removes it from the backup pool.</span></span>

    
    <span data-ttu-id="0b5a3-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b5a3-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

