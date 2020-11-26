---
title: 'Lync Server 2013: управление оповещениями во время аварийного восстановления'
description: 'Lync Server 2013: Управление объявлениями во время аварийного восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage announcements during disaster recovery
ms:assetid: c33e51ea-421f-42d2-826b-b73968f6bd5b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721874(v=OCS.15)
ms:contentKeyID: 49733807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d85dfcd15c9c3650bafafa6fa7702e19ac9c4f7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426125"
---
# <a name="manage-announcements-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="193f6-103">Управление оповещениями во время аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="193f6-103">Manage announcements during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="193f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="193f6-104">

<span> </span></span></span>

<span data-ttu-id="193f6-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="193f6-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="193f6-106">Lync Server 2013 поддерживает объявления для звонков на неназначенные номера во время простоя.</span><span class="sxs-lookup"><span data-stu-id="193f6-106">Lync Server 2013 supports announcements for calls to unassigned numbers during outages.</span></span> <span data-ttu-id="193f6-107">Восстановление функций объявлений во время отключения не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="193f6-107">Restoring announcement functionality during an outage is optional.</span></span> <span data-ttu-id="193f6-108">Если вы решите восстановить объявления во время сбоя, вам потребуется заново создать конфигурацию объявлений в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="193f6-108">If you choose to restore announcements during an outage, you need recreate your announcement configuration in the backup pool.</span></span> <span data-ttu-id="193f6-109">В этом разделе описаны действия, которые необходимо выполнить, если вы решите восстановить объявления во время восстановления после аварии.</span><span class="sxs-lookup"><span data-stu-id="193f6-109">This section describes what you need to do if you choose to restore announcements during disaster recovery.</span></span>

<span data-ttu-id="193f6-110">Этот раздел относится к неназначенным диапазонам номеров, использующим приложение для объявлений.</span><span class="sxs-lookup"><span data-stu-id="193f6-110">This section applies to unassigned number ranges that use the Announcement application.</span></span> <span data-ttu-id="193f6-111">Этот раздел не относится к неназначенным диапазонам номеров, использующим автоматический секретарь единой системы обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="193f6-111">This section does not apply to unassigned number ranges that use Exchange Unified Messaging (UM) Auto Attendant.</span></span>

<div>

## <a name="before-an-outage"></a><span data-ttu-id="193f6-112">Перед отключением</span><span class="sxs-lookup"><span data-stu-id="193f6-112">Before an Outage</span></span>

<span data-ttu-id="193f6-113">Независимо от того, какие сообщения вы выбрали для объявления, вы должны использовать отдельные резервные копии всех настроенных звуковых файлов, настроенных для приложения объявлений.</span><span class="sxs-lookup"><span data-stu-id="193f6-113">Regardless of whether you choose to use announcements during outages, you should take separate backups of any customized audio files that you configured for the Announcement application.</span></span> <span data-ttu-id="193f6-114">Пользовательские извещения не записываются в ходе аварийного восстановления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="193f6-114">Customized announcements are not backed up as part of the Lync Server disaster recovery process.</span></span> <span data-ttu-id="193f6-115">Если вы не хотите создавать отдельные резервные копии файлов и файлы, отправленные на сервер или в пул, повреждены, повреждены или удалены, они будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="193f6-115">If you do not take separate backups of the files and the files that you uploaded to the server or pool are damaged, corrupted, or erased, the files will be lost.</span></span>

<span data-ttu-id="193f6-116">Если у вас нет резервных копий настроенных аудиофайлов, а исходные аудиофайлы больше недоступны, вы можете найти аудиофайлы, которые вы задаете для приложения для объявлений, изучив файл в хранилище файлов для сервера или пула, где они были первоначально импортированы.</span><span class="sxs-lookup"><span data-stu-id="193f6-116">If you do not have backup copies of customized audio files, and the original audio files are no longer available, you can find the audio files that you configured for an Announcement application by looking in the File Store for the server or pool where you originally imported the files.</span></span> <span data-ttu-id="193f6-117">Вы можете скопировать все звуковые файлы, настроенные для приложения для объявлений, из хранилища файлов.</span><span class="sxs-lookup"><span data-stu-id="193f6-117">You can copy all the audio files that you configured for the Announcement application from the File Store.</span></span>

<span data-ttu-id="193f6-118">**Копирование звуковых файлов из хранилища файлов**</span><span class="sxs-lookup"><span data-stu-id="193f6-118">**To copy audio files from the file store**</span></span>

1.  <span data-ttu-id="193f6-119">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="193f6-119">At the command line, run:</span></span>
    
        Xcopy <Source: Pool Announcement Service File Store path> <Destination>
    
    <span data-ttu-id="193f6-120">Например:</span><span class="sxs-lookup"><span data-stu-id="193f6-120">For example:</span></span>
    
        Xcopy "<Pool File Store Path>\X-ApplicationServer-X\AppServerFiles\RGS\AS" "<Destination: Backup location>"
    
    <span data-ttu-id="193f6-121">Где X-ApplicationServer-X — идентификатор службы сервера приложений пула (например, 1-ApplicationServer-1)</span><span class="sxs-lookup"><span data-stu-id="193f6-121">Where X-ApplicationServer-X refers to the service ID of the Application Server of the pool (for example, 1-ApplicationServer-1")</span></span>


</div>

<div>

## <a name="during-an-outage"></a><span data-ttu-id="193f6-122">Во время отключения</span><span class="sxs-lookup"><span data-stu-id="193f6-122">During an Outage</span></span>

<span data-ttu-id="193f6-123">Чтобы использовать приложение для объявления во время сбоя, необходимо повторно создать конфигурацию объявлений в пуле резервных копий, выполнив действия, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="193f6-123">To use the Announcement application during an outage, you need to recreate the announcement configuration in the backup pool by performing the tasks described in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="193f6-124">Мы рекомендуем выполнять эти задачи после переключения на пул резервных копий, так как при выполнении действия 2 пул резервных копий становится владельцем неназначенных диапазонов номеров.</span><span class="sxs-lookup"><span data-stu-id="193f6-124">We recommend that you perform these tasks after you fail over to the backup pool, because as soon as you perform step 2, the backup pool takes ownership of the unassigned number ranges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="193f6-125">Эти действия не требуются для диапазонов номеров, использующих телефонный номер автосекретаря UM.</span><span class="sxs-lookup"><span data-stu-id="193f6-125">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="193f6-126">**Повторное создание конфигурации объявлений в пуле резервных копий**</span><span class="sxs-lookup"><span data-stu-id="193f6-126">**To recreate the announcement configuration in the backup pool**</span></span>

1.  <span data-ttu-id="193f6-127">Повторно создайте объявления, которые вы развернули в основном пуле в пуле резервных копий, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="193f6-127">Recreate the announcements that you deployed in the primary pool in the backup pool by doing the following:</span></span>
    
    1.  <span data-ttu-id="193f6-128">Импортируйте все звуковые файлы, используемые в основном пуле, в пул резервных копий с помощью командлета **Import-CsAnnouncementFile** и указав резервный пул для родительского параметра.</span><span class="sxs-lookup"><span data-stu-id="193f6-128">Import any audio files used in the primary pool to the backup pool by using the **Import-CsAnnouncementFile** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    2.  <span data-ttu-id="193f6-129">Повторно создайте каждое объявление с помощью командлета **New-CsAnnouncement** и укажите пул резервных копий для родительского параметра.</span><span class="sxs-lookup"><span data-stu-id="193f6-129">Recreate each announcement by using the **New-CsAnnouncement** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="193f6-130">Подробнее об использовании этих параметров для создания объявлений в пуле резервных копий можно узнать <A href="lync-server-2013-create-an-announcement.md">в статьях создание объявления в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="193f6-130">For details about using these parameters to create announcements in the backup pool, see <A href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="193f6-131">После повторного создания всех извещений в пуле резервных копий переадресовать все неназначенные диапазоны номеров, использующие объявления в основном пуле, в повторно созданные объявления в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="193f6-131">After all announcements are recreated in the backup pool, redirect all the unassigned number ranges that use announcements in the primary pool to the recreated announcements in the backup pool.</span></span>
    
    <span data-ttu-id="193f6-132">Для всех неназначенных диапазонов номеров, использующих объявление в основном пуле, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="193f6-132">For each unassigned number range that uses an announcement in the primary pool, run the following:</span></span>
    
        Set-CsUnassignedNumber -Identity "<name of number range>" -AnnouncementService "<FQDN of backup pool>" -AnnouncementName "<announcement name in backup pool>"

</div>

<div>

## <a name="after-the-outage"></a><span data-ttu-id="193f6-133">После отключения</span><span class="sxs-lookup"><span data-stu-id="193f6-133">After the Outage</span></span>

<span data-ttu-id="193f6-134">После того как основной пул станет доступным, вам нужно перенаправить неназначенные диапазоны номеров, которые были изменены для отключения, в основной пул.</span><span class="sxs-lookup"><span data-stu-id="193f6-134">When the primary pool becomes available, you need to redirect the unassigned number ranges that you changed for the outage back to the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="193f6-135">Эти действия не требуются для диапазонов номеров, использующих телефонный номер автосекретаря UM.</span><span class="sxs-lookup"><span data-stu-id="193f6-135">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="193f6-136">**Восстановление объявлений в основном пуле**</span><span class="sxs-lookup"><span data-stu-id="193f6-136">**To restore announcements in the primary pool**</span></span>

1.  <span data-ttu-id="193f6-137">Если вы пришлось перестраивать основной пул во время восстановления, вам нужно будет заново создать объявления в основном пуле, импортировав аудиофайлы и создав извещения так же, как и в пуле резервных копий, за исключением того, что вы указали основной пул для родительского параметра.</span><span class="sxs-lookup"><span data-stu-id="193f6-137">If you had to rebuild the primary pool during the recovery, you need to recreate the announcements in the primary pool by importing the audio files and creating announcements, just as you did in the backup pool, except that you specify the primary pool for the Parent parameter.</span></span> <span data-ttu-id="193f6-138">Дополнительные сведения можно найти в разделе "во время отключения" ранее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="193f6-138">For details, see "During an Outage" earlier in this topic.</span></span>

2.  <span data-ttu-id="193f6-139">Для каждого неназначенного диапазона чисел, который вы изменили для отключения, выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="193f6-139">For each unassigned number range that you changed for the outage, run the following:</span></span>
    
        Set-CsUnassignedNumber [-Identity "<name of number range>"] -AnnouncementService "<FQDN of primary pool>" -AnnouncementName "<announcement name in primary pool>"

3.  <span data-ttu-id="193f6-140">При необходимости удалите объявления, которые вы воссоздали в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="193f6-140">Optionally, remove the announcements that you recreated in the backup pool.</span></span> <span data-ttu-id="193f6-141">Получение списка извещений для приложения извещения о пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="193f6-141">Get a list of announcements for the backup pool Announcement application.</span></span> <span data-ttu-id="193f6-142">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="193f6-142">At the command line, run:</span></span>
    
        Get-CsAnnouncement -Identity "<Service:service ID>"
    
    <span data-ttu-id="193f6-143">Например:</span><span class="sxs-lookup"><span data-stu-id="193f6-143">For example:</span></span>
    
        Get-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com
    
    <span data-ttu-id="193f6-144">В списке результатов найдите объявления, которые вы хотите удалить, и скопируйте идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="193f6-144">In the resulting list, locate the announcements you want to remove and copy the GUIDs.</span></span> <span data-ttu-id="193f6-145">Для каждого объявления, которое вы хотите удалить, выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="193f6-145">For each announcement you want to remove, run:</span></span>
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>"
    
    <span data-ttu-id="193f6-146">Например:</span><span class="sxs-lookup"><span data-stu-id="193f6-146">For example:</span></span>
    
        Remove-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"


<span data-ttu-id="193f6-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="193f6-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

