---
title: 'Lync Server 2013: планирование аварийного восстановления для группы ответа'
description: 'Lync Server 2013: Планирование аварийного восстановления группы ответов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for response group disaster recovery
ms:assetid: 14e0f5dc-77cd-42cd-a9c9-4d0da38fb1cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204699(v=OCS.15)
ms:contentKeyID: 48183482
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5294ddf7dbd42d95c5eb17acd6be6a5abc7a5917
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400207"
---
# <a name="planning-for-response-group-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="fce66-103">Планирование аварийного восстановления для группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fce66-103">Planning for response group disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fce66-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fce66-104">

<span> </span></span></span>

<span data-ttu-id="fce66-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="fce66-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="fce66-106">В этом разделе описаны некоторые способы подготовки групп ответов для аварийного восстановления и обзор процесса аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="fce66-106">This section describes some ways to prepare response groups for disaster recovery and provides an overview of the disaster recovery process.</span></span>

<div>

## <a name="preparing-for-response-group-disaster-recovery"></a><span data-ttu-id="fce66-107">Подготовка к аварийному восстановлению группы ответов</span><span class="sxs-lookup"><span data-stu-id="fce66-107">Preparing for Response Group Disaster Recovery</span></span>

<span data-ttu-id="fce66-108">При подготовке и выполнении процедур аварийного восстановления следует учитывать следующее:</span><span class="sxs-lookup"><span data-stu-id="fce66-108">Keep the following in mind when you prepare for and carry out disaster recovery procedures.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fce66-109">В среде сосуществования для процедур аварийного восстановления, описанных в этом документе, поддерживаются только группы ответов Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fce66-109">In a coexistence environment, only the Lync Server 2013 response groups are supported for the disaster recovery procedures described in this document.</span></span>



</div>

  - <span data-ttu-id="fce66-110">Планирование аварийного восстановления при планировании производственных мощностей.</span><span class="sxs-lookup"><span data-stu-id="fce66-110">Plan for disaster recovery when you do your capacity planning.</span></span> <span data-ttu-id="fce66-111">Для производительности аварийного восстановления каждый пул в Объединенном пуле должен иметь возможность обрабатывать рабочие нагрузки всех групп ответов в обоих пулах.</span><span class="sxs-lookup"><span data-stu-id="fce66-111">For disaster recovery capacity, each pool in a paired pool should be able to handle the workloads of all the response groups in both pools.</span></span> <span data-ttu-id="fce66-112">Подробные сведения о планировании мощности групп ответов можно найти [в разделе Планирование ресурсов для группы ответа в Lync Server 2013](lync-server-2013-capacity-planning-for-response-group.md).</span><span class="sxs-lookup"><span data-stu-id="fce66-112">For details about Response Group capacity planning, see [Capacity planning for Response Group in Lync Server 2013](lync-server-2013-capacity-planning-for-response-group.md).</span></span>

  - <span data-ttu-id="fce66-113">Регулярно заполните резервные копии всех конфигураций групп ответа во всех пулах интерфейсов, в которых вы развернули приложение группы ответа с помощью процедуры экспорта, описанной в этом документе.</span><span class="sxs-lookup"><span data-stu-id="fce66-113">Take regular backup copies of all the response group configurations in all the Front End pools where you deployed the Response Group application by using the export procedure described in this document.</span></span> <span data-ttu-id="fce66-114">Дополнительные сведения можно найти [в разделе процедуры аварийного восстановления группы ответа в Lync Server 2013](lync-server-2013-response-group-disaster-recovery-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="fce66-114">For details, see [Response group disaster recovery procedures in Lync Server 2013](lync-server-2013-response-group-disaster-recovery-procedures.md).</span></span> <span data-ttu-id="fce66-115">Храните резервные копии в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="fce66-115">Keep the backup copies in a safe location.</span></span>

  - <span data-ttu-id="fce66-116">Храните резервные копии всех исходных аудиофайлов, которые вы использовали для приложения группы ответа, включая любые записи и файлы на удержании музыки.</span><span class="sxs-lookup"><span data-stu-id="fce66-116">Keep a separate backup copy of all the original audio files you used for the Response Group application, including any recordings and music-on-hold files.</span></span> <span data-ttu-id="fce66-117">Храните архивные файлы в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="fce66-117">Keep the backup files in a safe location.</span></span>

  - <span data-ttu-id="fce66-118">Для Lync Server 2013 с аварийным восстановлением все параметры группы ответа должны иметь уникальные имена в рамках развертывания.</span><span class="sxs-lookup"><span data-stu-id="fce66-118">For Lync Server 2013 disaster recovery, all Response Group settings must have unique names across your deployment.</span></span> <span data-ttu-id="fce66-119">Это требование относится к рабочим процессам, очередям, группам агентов, наборам праздников и часам бизнеса.</span><span class="sxs-lookup"><span data-stu-id="fce66-119">This requirement applies to workflows, queues, agent groups, holiday sets, and hours of business.</span></span> <span data-ttu-id="fce66-120">Убедитесь в том, что это требование выполняется, когда основной пул и пулы резервных копий по-прежнему активны, а перед тем, как вы захотите инициировать резервную процедуру.</span><span class="sxs-lookup"><span data-stu-id="fce66-120">You should verify that this requirement is met when the primary and backup pools are still active, and before you need to initiate any failover procedure.</span></span> <span data-ttu-id="fce66-121">Если при импорте данных группы ответа в пул резервных копий возникло конфликт имен, импорт завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="fce66-121">If you encounter name conflicts while importing response group data to the backup pool, the import fails.</span></span> <span data-ttu-id="fce66-122">Чтобы завершить импорт и отработку отказа, необходимо устранить конфликты имен, переопределив объект группы ответа в пуле резервных копий или воспользовавшись командлетом **Import-CsRgsConfiguration** с параметром – ResolveNameConflicts для автоматического разрешения конфликта путем добавления уникального идентификационного номера к объекту группы ответа.</span><span class="sxs-lookup"><span data-stu-id="fce66-122">To complete the import and failover procedure, you need to resolve the name conflicts by renaming the response group object in the backup pool or by using the **Import-CsRgsConfiguration** cmdlet with the –ResolveNameConflicts parameter to automatically resolve the conflict by appending a unique identifying number to the response group object.</span></span>

  - <span data-ttu-id="fce66-123">Как правило, мы рекомендуем выполнять ежедневные архивации, но если у вас много изменений, вам может понадобиться запланировать более частые резервные копии.</span><span class="sxs-lookup"><span data-stu-id="fce66-123">In general, we recommend that you perform daily backups, but if you have a high volume of changes, you might want to schedule more frequent backups.</span></span> <span data-ttu-id="fce66-124">Объем данных, которые можно потерять в случае аварии, зависит от частоты резервных копий, а также частоты и объема изменений.</span><span class="sxs-lookup"><span data-stu-id="fce66-124">The amount of information you can lose in the event of a disaster depends on the frequency of your backups, as well as the frequency and volume of changes.</span></span>

  - <span data-ttu-id="fce66-125">Вы можете импортировать группы ответа в пул резервных копий перед выполнением аварийной или резервной операции.</span><span class="sxs-lookup"><span data-stu-id="fce66-125">It is possible to import response groups to a backup pool before a disaster or failover operation occurs.</span></span> <span data-ttu-id="fce66-126">Импорт групп ответа в заранее сокращает время простоя, так как служба группы ответа Lync Server может быть восстановлена в пуле резервного копирования сразу после того, как звонки пересылаются в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-126">Importing response groups in advance reduces downtime, because the Lync Server Response Group service can be restored in the backup pool as soon as calls are routed to the backup pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fce66-127">Приложение группы ответа не может связаться ни с одним агентом в неактивном пуле, пока не завершится отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="fce66-127">The Response Group application cannot reach any agents homed in an inactive pool until failover is complete.</span></span> <span data-ttu-id="fce66-128">В течение этого времени приложение "группа ответа" обрабатывает звонки так, как если бы эти агенты были недоступны.</span><span class="sxs-lookup"><span data-stu-id="fce66-128">During this time, the Response Group application processes calls as if those agents are unavailable.</span></span>

    
    </div>

</div>

<div>

## <a name="response-group-disaster-recovery-process"></a><span data-ttu-id="fce66-129">Процесс аварийного восстановления группы ответов</span><span class="sxs-lookup"><span data-stu-id="fce66-129">Response Group Disaster Recovery Process</span></span>

<span data-ttu-id="fce66-130">В случае аварии вы можете восстановить группы ответа, используя один из указанных ниже подходов к восстановлению.</span><span class="sxs-lookup"><span data-stu-id="fce66-130">In the event of a disaster, you can recover response groups by using either of the following recovery approaches:</span></span>

  - <span data-ttu-id="fce66-131">Отработка отказа в резервной копии пула, после чего он не будет восстановлен в исходном пуле.</span><span class="sxs-lookup"><span data-stu-id="fce66-131">Fail over to a backup pool and then fail back to the original pool.</span></span>

  - <span data-ttu-id="fce66-132">Отработка отказа в резервной копии пула, создание нового пула с другим полным доменным именем (FQDN), а затем импорт групп ответа в новый пул.</span><span class="sxs-lookup"><span data-stu-id="fce66-132">Fail over to a backup pool, create a new pool with a different fully qualified domain name (FQDN), and then import the response groups to the new pool.</span></span>

<span data-ttu-id="fce66-133">На этапе восстановления после сбоя в аварийном восстановлении группы ответа находятся в нескольких пулах: в основном пуле (который недоступен) и в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-133">During the failover phase of disaster recovery, the response groups reside in multiple pools: in the primary pool (which is unavailable) and in the backup pool.</span></span> <span data-ttu-id="fce66-134">Группы ответа в обоих пулах имеют одинаковое имя и одного и того же владельца (основного пула), но у них разные родители.</span><span class="sxs-lookup"><span data-stu-id="fce66-134">The response groups in both pools have the same name and the same owner (the primary pool), but they have different parents.</span></span>

<span data-ttu-id="fce66-135">При восстановлении путем создания нового пула с другим полным доменным именем необходимо назначить новый пул владельцем групп ответа при импорте.</span><span class="sxs-lookup"><span data-stu-id="fce66-135">When you recover by creating a new pool with a different FQDN, you need to assign the new pool as the owner of the response groups when you import them.</span></span> <span data-ttu-id="fce66-136">Владелец групп ответов остается в исходном пуле, если только вы не переназначьте владение с помощью параметра – OverwriteOwner с командлетом **Import-CsRgsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="fce66-136">Ownership of response groups remains with the original pool unless or until you explicitly reassign ownership by using the –OverwriteOwner parameter with the **Import-CsRgsConfiguration** cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fce66-137">Кроме того, вы также можете использовать параметр – OverwriteOwner, если вы перестроили пул во время восстановления (то есть она пуста), независимо от того, используется ли это полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="fce66-137">You also need to use the –OverwriteOwner parameter if you rebuilt the pool during the recovery (that is, the Response Group database is empty), whether or not you use the same FQDN.</span></span> <span data-ttu-id="fce66-138">Если вы не перестроены в пул, вам не нужно использовать параметр – OverwriteOwner, но этот параметр можно использовать при импорте групп ответа обратно в основной пул.</span><span class="sxs-lookup"><span data-stu-id="fce66-138">You do not need to use the –OverwriteOwner parameter if you did not rebuild the pool, but it is permissible to use this parameter whenever you import response groups back to the primary pool.</span></span>



</div>

<span data-ttu-id="fce66-139">Вы можете задать только один набор параметров конфигурации группы ответов на уровне приложения для каждого пула.</span><span class="sxs-lookup"><span data-stu-id="fce66-139">You can define only one set of application-level Response Group configuration settings per pool.</span></span> <span data-ttu-id="fce66-140">Эти параметры включают стандартную конфигурацию сохранения музыки, используемую по умолчанию в качестве звукового файла для сохранения музыки, агент Ringback льготный период и контекстную конфигурацию вызова.</span><span class="sxs-lookup"><span data-stu-id="fce66-140">These settings include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="fce66-141">Чтобы просмотреть эти параметры конфигурации, запустите командлет **Get-CsRgsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="fce66-141">To view these configuration settings, run the **Get-CsRgsConfiguration** cmdlet.</span></span> <span data-ttu-id="fce66-142">Дополнительные сведения о командлете **Get-CsRgsConfiguration** можно найти в [статьях Get-CsRgsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration).</span><span class="sxs-lookup"><span data-stu-id="fce66-142">For details about the **Get-CsRgsConfiguration** cmdlet, see [Get-CsRgsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration).</span></span>

<span data-ttu-id="fce66-143">Вы можете перенести эти параметры уровня приложения из одного пула в другой с помощью командлета **Import-CsRgsConfiguration** с параметром – ReplaceExistingSettings, но это переопределит параметры в целевом пуле.</span><span class="sxs-lookup"><span data-stu-id="fce66-143">You can transfer these application-level settings from one pool to another by using the **Import-CsRgsConfiguration** cmdlet with the –ReplaceExistingSettings parameter, but doing so overrides the settings in the destination pool.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="fce66-144">Это ограничение для перемещения параметров в другой пул имеет значение true только для параметров уровня приложения и звукового файла, используемого по умолчанию при хранении музыки.</span><span class="sxs-lookup"><span data-stu-id="fce66-144">This constraint about transferring settings to another pool is true only for the application-level settings and the default music-on-hold audio file.</span></span> <span data-ttu-id="fce66-145">Это не относится к группам агентов, очередям, рабочим процессам, часам и наборам праздников.</span><span class="sxs-lookup"><span data-stu-id="fce66-145">It does not apply to agent groups, queues, workflows, business hours, and holiday sets.</span></span>



</div>

<span data-ttu-id="fce66-146">Если вы не хотите заменять параметры уровня приложения в пуле резервных копий во время аварии, и основной пул невозможно восстановить, параметры уровня приложения из основного пула будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="fce66-146">If you don't want to replace the application-level settings in the backup pool during a disaster and the primary pool can't be recovered, the application-level settings from the primary pool will be lost.</span></span> <span data-ttu-id="fce66-147">Если необходимо создать новый пул для замены основного пула при восстановлении с таким же полным доменным именем или с другим полным доменным именем, вы не сможете восстановить исходные параметры уровня приложения.</span><span class="sxs-lookup"><span data-stu-id="fce66-147">If you need to create a new pool to replace the primary pool during recovery, either with the same FQDN or with a different FQDN, you can't recover the original application-level settings.</span></span> <span data-ttu-id="fce66-148">В этом случае необходимо настроить новый пул с помощью этих параметров и добавить звуковой файл для сохранения музыки.</span><span class="sxs-lookup"><span data-stu-id="fce66-148">In this case, you need to configure the new pool with these settings and include the music-on-hold audio file.</span></span>

<span data-ttu-id="fce66-149">Если вы решили использовать командлет **Import-CsRgsConfiguration** для переноса параметров уровня приложения из основного пула в пул резервных копий во время аварии, вы можете передать параметры из пула резервных копий в новый пул в процессе восстановления так же, как и из основного пула, в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-149">If you decide to use the **Import-CsRgsConfiguration** cmdlet to transfer application-level settings from the primary pool to the backup pool during a disaster, you can then transfer the settings from the backup pool to the new pool during recovery in the same way that you transferred them from the primary pool to the backup pool.</span></span>

<span data-ttu-id="fce66-150">В таблице ниже приведены инструкции по восстановлению групп ответа.</span><span class="sxs-lookup"><span data-stu-id="fce66-150">The following table is an overview of the steps involved in recovering response groups.</span></span>

<span data-ttu-id="fce66-151">Дополнительные сведения о выполнении этих действий можно найти [в разделе процедуры аварийного восстановления группы ответа в Lync Server 2013](lync-server-2013-response-group-disaster-recovery-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="fce66-151">For details about performing these steps, see [Response group disaster recovery procedures in Lync Server 2013](lync-server-2013-response-group-disaster-recovery-procedures.md).</span></span>

### <a name="response-group-disaster-recovery-steps"></a><span data-ttu-id="fce66-152">Инструкции по аварийному восстановлению группы ответа</span><span class="sxs-lookup"><span data-stu-id="fce66-152">Response Group Disaster Recovery Steps</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fce66-153">Этап</span><span class="sxs-lookup"><span data-stu-id="fce66-153">Phase</span></span></th>
<th><span data-ttu-id="fce66-154">Шаги</span><span class="sxs-lookup"><span data-stu-id="fce66-154">Steps</span></span></th>
<th><span data-ttu-id="fce66-155">Необходимые группы и роли</span><span class="sxs-lookup"><span data-stu-id="fce66-155">Required groups and roles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fce66-156">Перед отключением</span><span class="sxs-lookup"><span data-stu-id="fce66-156">Before outage</span></span></p></td>
<td><p><span data-ttu-id="fce66-157">С помощью командлета <strong>Export-CsRgsConfiguration</strong> можно создавать резервные копии всех конфигураций групп ответа во всех пулах интерфейсных служб, в которых развернуто приложение группы ответа.</span><span class="sxs-lookup"><span data-stu-id="fce66-157">On a routine basis, run the <strong>Export-CsRgsConfiguration</strong> cmdlet to create backups of all Response Group configurations in all Front End pools where Response Group application is deployed.</span></span></p></td>
<td><p><span data-ttu-id="fce66-158">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="fce66-158">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="fce66-159">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="fce66-159">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fce66-160">Во время отключения</span><span class="sxs-lookup"><span data-stu-id="fce66-160">During outage</span></span></p></td>
<td><p><span data-ttu-id="fce66-161">Запустите командлет <strong>Import-CsRgsConfiguration</strong> , чтобы импортировать из резервной копии конфигурации службы ответов на Lync Server из основного пула в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-161">Run the <strong>Import-CsRgsConfiguration</strong> cmdlet to import the backed up Lync Server Response Group service configuration from the primary pool to the backup pool.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="fce66-162">Используйте параметр – ReplaceExistingSettings, если вы хотите заменить параметры группы ответа уровня приложения в пуле резервного копирования на параметры из основного пула.</span><span class="sxs-lookup"><span data-stu-id="fce66-162">Use the –ReplaceExistingSettings parameter if you want to replace application-level Response Group settings in the backup pool with the settings from the primary pool.</span></span> <span data-ttu-id="fce66-163">Если вы не переносите параметры уровня приложения из основного пула в пул резервных копий, и основной пул восстановить невозможно, параметры из основного пула будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="fce66-163">If you do not transfer the application-level settings from the primary pool to the backup pool, and the primary pool can't be recovered, you will lose the settings from the primary pool.</span></span>


</div></td>
<td><p><span data-ttu-id="fce66-164">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="fce66-164">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="fce66-165">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="fce66-165">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fce66-166">После импорта</span><span class="sxs-lookup"><span data-stu-id="fce66-166">After importing</span></span></p></td>
<td><p><span data-ttu-id="fce66-167">Запустите командлеты группы ответа с параметром – ShowAll (для отображения всех групп ответа) или параметр – владелец (чтобы отобразить только импортированные группы ответов), чтобы убедиться в том, что все конфигурации группы ответа были импортированы в резервный пул.</span><span class="sxs-lookup"><span data-stu-id="fce66-167">Run Response Group cmdlets with either the –ShowAll parameter (to display all response groups) or the –Owner parameter (to display only imported response groups) to verify that all response group configurations were imported to the backup pool.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="fce66-168">Если вы не используете либо параметр – ShowAll, либо параметр – владелец, группы ответа, импортированные в пул резервных копий, не будут указаны в результатах, возвращенных командлетами.</span><span class="sxs-lookup"><span data-stu-id="fce66-168">If you do not use either the –ShowAll parameter or the –Owner parameter, the response groups that you imported to the backup pool will not be listed in the results returned by the cmdlets.</span></span>


</div>
<p><span data-ttu-id="fce66-169">Выполните следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="fce66-169">Run the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="fce66-170"><strong>Get-CsRgsWorkflow</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-170"><strong>Get-CsRgsWorkflow</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-171"><strong>Get-CsRgsQueue</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-171"><strong>Get-CsRgsQueue</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-172"><strong>Get-CsRgsAgentGroup</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-172"><strong>Get-CsRgsAgentGroup</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-173"><strong>Get-CsRgsHoursOfBusiness</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-173"><strong>Get-CsRgsHoursOfBusiness</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-174"><strong>Get-CsRgsHolidaySet</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-174"><strong>Get-CsRgsHolidaySet</strong></span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fce66-175">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="fce66-175">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="fce66-176">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="fce66-176">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fce66-177">После перехода на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="fce66-177">After failover</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fce66-178">Наведите тестовый звонок в группу ответа, которая была импортирована в пул резервных копий, и убедитесь, что звонок обрабатывается должным образом.</span><span class="sxs-lookup"><span data-stu-id="fce66-178">Place a test call to a response group that was imported to the backup pool and verify that the call is handled correctly.</span></span></p></li>
<li><p><span data-ttu-id="fce66-179">Все формальные агенты должны повторно входить в их формальные группы в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-179">All formal agents must sign in again to their formal groups on backup pool.</span></span></p></li>
<li><p><span data-ttu-id="fce66-180">Управление изменениями конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fce66-180">Manage configuration changes:</span></span></p>
<p><span data-ttu-id="fce66-181">Группы ответа в пуле резервных копий, импортированные в резервную копию или принадлежащую пулу резервных копий, можно изменять в обычном режиме простоя.</span><span class="sxs-lookup"><span data-stu-id="fce66-181">Response groups in the backup pool, whether imported to the backup pool or owned by the backup pool, can be modified as usual during the outage.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="fce66-182">Вы должны использовать командную консоль Lync Server для управления группами ответов, которые вы импортировали в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-182">You must use Lync Server Management Shell to manage the response groups that you imported to the backup pool.</span></span> <span data-ttu-id="fce66-183">Вы не можете использовать панель управления Lync Server для управления этими группами ответа, пока они находятся в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-183">You cannot use Lync Server Control Panel to manage these response groups while they are in the backup pool.</span></span>


</div></li>
</ul></td>
<td><p><span data-ttu-id="fce66-184">Н/Д</span><span class="sxs-lookup"><span data-stu-id="fce66-184">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fce66-185">После восстановления перед восстановлением после сбоя</span><span class="sxs-lookup"><span data-stu-id="fce66-185">After recovery, before failback</span></span></p></td>
<td><p><span data-ttu-id="fce66-186">Запустите командлет <strong>Export-CsRgsConfiguration</strong> , указав параметр-Source в качестве пула резервных копий, и параметр – владелец в качестве основного пула для экспорта групп ответов, принадлежащих основным пулам из пула резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-186">Run the <strong>Export-CsRgsConfiguration</strong> cmdlet specifying the -Source parameter as the backup pool and the –Owner parameter as the primary pool to export the response groups owned by the primary pool from the backup pool.</span></span></p></td>
<td><p><span data-ttu-id="fce66-187">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="fce66-187">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="fce66-188">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="fce66-188">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fce66-189">После восстановления после сбоя</span><span class="sxs-lookup"><span data-stu-id="fce66-189">After failback</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fce66-190">Запустите командлет <strong>Import-CsRgsConfiguration</strong> , чтобы импортировать группы ответа обратно в основной пул.</span><span class="sxs-lookup"><span data-stu-id="fce66-190">Run the <strong>Import-CsRgsConfiguration</strong> cmdlet to import the response groups back to the primary pool.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="fce66-191">Если основной пул не поддается восстановлению и вы развертываете новый пул для его замены, используйте параметр – ReplaceExistingSettings для переноса параметров уровня приложения из пула резервных копий в новый пул.</span><span class="sxs-lookup"><span data-stu-id="fce66-191">If the primary pool can't be recovered and you deploy a new pool to replace it, use the –ReplaceExistingSettings parameter to transfer the application-level settings from the backup pool to the new pool.</span></span> <span data-ttu-id="fce66-192">Если вы не переносяте параметры из пула резервных копий, для нового пула будут использоваться параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fce66-192">If you do not transfer the settings from the backup pool, the new pool will use the default settings.</span></span>


</div></li>
<li><p><span data-ttu-id="fce66-193">Выполните следующие командлеты с параметром – ShowAll (для отображения всех групп ответа) или параметр – владелец (для отображения только импортированных групп ответа), чтобы убедиться в том, что все конфигурации группы ответа успешно импортированы в основной пул.</span><span class="sxs-lookup"><span data-stu-id="fce66-193">Run the following cmdlets with either the –ShowAll parameter (to display all response groups) or the –Owner parameter (to display only imported response groups) to verify that all response group configurations were successfully imported back to the primary pool:</span></span></p>
<ul>
<li><p><span data-ttu-id="fce66-194"><strong>Get-CsRgsWorkflow</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-194"><strong>Get-CsRgsWorkflow</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-195"><strong>Get-CsRgsQueue</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-195"><strong>Get-CsRgsQueue</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-196"><strong>Get-CsRgsAgentGroup</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-196"><strong>Get-CsRgsAgentGroup</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-197"><strong>Get-CsRgsHoursOfBusiness</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-197"><strong>Get-CsRgsHoursOfBusiness</strong></span></span></p></li>
<li><p><span data-ttu-id="fce66-198"><strong>Get-CsRgsHolidaySet</strong></span><span class="sxs-lookup"><span data-stu-id="fce66-198"><strong>Get-CsRgsHolidaySet</strong></span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="fce66-199">Наведите тестовый звонок в группу ответа, которая была импортирована обратно в основной пул, и убедитесь, что звонок обрабатывается должным образом.</span><span class="sxs-lookup"><span data-stu-id="fce66-199">Place a test call to a response group that was imported back to the primary pool and verify that the call is handled correctly.</span></span></p></li>
<li><p><span data-ttu-id="fce66-200">При необходимости выполните командлет <strong>Export-CsRgsConfiguration</strong> в пуле резервных копий с параметром – RemoveExportedConfiguration, чтобы удалить группы ответов, принадлежащие основным пулам из пула резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fce66-200">Optionally, run the <strong>Export-CsRgsConfiguration</strong> cmdlet on the backup pool with the –RemoveExportedConfiguration parameter to remove the response groups owned by the primary pool from the backup pool.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="fce66-201">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="fce66-201">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="fce66-202">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="fce66-202">CsResponseGroupAdministrator</span></span></p></td><span data-ttu-id="fce66-203">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fce66-203">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

