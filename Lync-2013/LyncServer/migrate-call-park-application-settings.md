---
title: Перенос параметров приложения приостановки звонков
description: Перенесите параметры приложения на приостановке звонков.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Call Park application settings
ms:assetid: 23b192d2-93ec-42a8-b175-b6ed502a2c35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687993(v=OCS.15)
ms:contentKeyID: 49733583
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da90ca4ee4dd53451c29b8c39861dc76a17ca3c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446901"
---
# <a name="migrate-call-park-application-settings"></a><span data-ttu-id="0186e-103">Перенос параметров приложения приостановки звонков</span><span class="sxs-lookup"><span data-stu-id="0186e-103">Migrate Call Park application settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0186e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0186e-104">

<span> </span></span></span>

<span data-ttu-id="0186e-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="0186e-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="0186e-106">Миграция приложения на приостановку работы из Lync Server 2010 в Lync Server 2013 включает подготовку пула Lync Server 2013 со всеми пользовательскими музыкальными файлами для хранения файлов, которые были загружены в Lync Server 2010, восстановление параметров уровня обслуживания и назначение всех орбитных координат в пуле Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0186e-106">The migration of the Call Park application from Lync Server 2010 to Lync Server 2013 includes provisioning the Lync Server 2013 pool with any custom music on hold files that have been uploaded in Lync Server 2010, restoring the service level settings and retargeting all Call Park orbits to the Lync Server 2013 pool.</span></span> <span data-ttu-id="0186e-107">Если настроенные файлы на удержании с хранением сконфигурированы в пуле Lync Server 2010, эти файлы необходимо скопировать в новый пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0186e-107">If customized music-on-hold files have been configured in the Lync Server 2010 pool, these files need to be copied to the new Lync Server 2013 pool.</span></span> <span data-ttu-id="0186e-108">Кроме того, рекомендуется создать резервную копию всех настроенных файлов для сохранения музыки на месте из Lync Server 2010 в другую папку назначения, чтобы сохранить отдельные резервные копии всех настроенных музыкальных файлов, которые были переданы на приостановку звонков.</span><span class="sxs-lookup"><span data-stu-id="0186e-108">Additionally, it is recommended that you back up any Call Park customized music-on-hold files from Lync Server 2010 to another destination to keep a separate backup copy of any customized music-on-hold files that have been uploaded for Call Park.</span></span> <span data-ttu-id="0186e-109">Настроенные на хранение музыкальные файлы для приложения для приостановки звонков хранятся в хранилище файлов пула.</span><span class="sxs-lookup"><span data-stu-id="0186e-109">The customized music-on-hold files for the Call Park application are stored in the file store of the pool.</span></span> <span data-ttu-id="0186e-110">Чтобы скопировать звуковые файлы из хранилища файлов пула Lync Server 2010 в хранилище файлов Lync Server 2013, используйте команду **xcopy** со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="0186e-110">To copy the audio files from a Lync Server 2010 pool file store to a Lync Server 2013 file store, use the **Xcopy** command with the following parameters:</span></span>

   ```console
    Xcopy <Source: Lync Server 2010 Pool CPS File Store Path> <Destination: Lync Server 2013 Pool CPS File Store Path>
   ```

   ```console
    Example usage:  Xcopy "<Lync Server 2010 File Store Path>\OcsFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\"  "<Lync Server 2013 File Store Path>\OcsFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\" 
   ```

<span data-ttu-id="0186e-111">После того как все настроенные аудиофайлы будут скопированы в хранилище файлов Lync Server 2013, должны быть настроены параметры приложения парковки для пула Lync Server 2013 и диапазоны на орбите, связанные с пулом Lync Server 2010, должны быть переназначены в пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0186e-111">When all customized audio files have been copied to the Lync Server 2013 file store, the Call Park application settings of the Lync Server 2013 pool must be configured, and the Call Park orbit ranges that are associated with the Lync Server 2010 pool must be reassigned to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="0186e-112">Параметры приложения для приема звонков включают пороговое значение тайм-аута отправки, включение или отключение музыки на удержании, максимальное количество попыток раскладки звонков и запрос времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="0186e-112">The Call Park application settings include the pickup timeout threshold, enabling or disabling music on hold, the maximum call pickup attempts and the timeout request.</span></span> <span data-ttu-id="0186e-113">Чтобы запустить командлет **Set-CsCpsConfiguration** , необходимо управлять параметрами приложения на приостановке звонков с помощью командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0186e-113">You must manage Call Park application settings by using the Lync Server Management Shell to run the **Set-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="0186e-114">Вы не можете управлять параметрами приложения на приостановке звонков с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0186e-114">You cannot manage the Call Park application settings using the Lync Server Control Panel.</span></span>

<span data-ttu-id="0186e-115">**Изменение параметров службы "Приостановка звонка"**</span><span class="sxs-lookup"><span data-stu-id="0186e-115">**Reconfigure the Call Park Service Settings**</span></span>

1.  <span data-ttu-id="0186e-116">На сервере переднего плана Lync Server 2013 откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0186e-116">From the Lync Server 2013 Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="0186e-117">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0186e-117">At the command line, type the following:</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0186e-118">Если параметры приложения для прикрепления звонков в Lync Server 2013 идентичны параметрам устаревшего сервера Lync Server 2010, вы можете пропустить выполнение этого действия.</span><span class="sxs-lookup"><span data-stu-id="0186e-118">If your Lync Server 2013 Call Park application settings are identical to the legacy Lync Server 2010 settings, you can skip running this step.</span></span> <span data-ttu-id="0186e-119">Если параметры приложения приостановки для Lync Server 2013 и Lync Server 2010 отличаются, для обновления этих изменений используйте командлет ниже в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="0186e-119">If Call Park application settings are different for the Lync Server 2013 and Lync Server 2010 environments, use the cmdlet below as a template to update those changes.</span></span>

    
    <span data-ttu-id="0186e-120"></div>
    ```powershell
        Set-CsCpsConfiguration -Identity "<LS2013 Call Park Service ID>"-CallPickupTimeoutThreshold" <LS2010 CPS TimeSpan> -EnableMusicOnHold " <LS2010 CPS value> "-MaxCallPickupAttempts " <LS2010 CPS pickup attempts> -OnTimeoutURI" <LS2010 CPS timeout URI>```</span><span class="sxs-lookup"><span data-stu-id="0186e-120"></div>
    ```powershell
        Set-CsCpsConfiguration -Identity "<LS2013 Call Park Service ID>" -CallPickupTimeoutThreshold "<LS2010 CPS TimeSpan>" -EnableMusicOnHold "<LS2010 CPS value>" -MaxCallPickupAttempts "<LS2010 CPS pickup attempts>" -OnTimeoutURI "<LS2010 CPS timeout URI>" ```</span></span>

<span data-ttu-id="0186e-121">Чтобы переназначить все диапазоны орбиты на приостановку, из пула Lync Server 2010 в пул Lync Server 2013, вы можете использовать либо панель управления Lync Server, либо консоль управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0186e-121">To reassign all Call Park orbit ranges from Lync Server 2010 pool to the Lync Server 2013 pool, you can use either the Lync Server Control Panel or the Lync Server Management Shell.</span></span>

<span data-ttu-id="0186e-122">**Переназначение всех диапазонов на орбиту на приостановку работы с помощью панели управления Lync Server**</span><span class="sxs-lookup"><span data-stu-id="0186e-122">**Reassign all Call Park Orbit Ranges using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="0186e-123">Откройте Панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0186e-123">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="0186e-124">В левой области выберите пункт **функции голосовой связи**.</span><span class="sxs-lookup"><span data-stu-id="0186e-124">In the left pane, select **Voice Features**.</span></span>

3.  <span data-ttu-id="0186e-125">Откройте вкладку " **приостановить Звонок** ".</span><span class="sxs-lookup"><span data-stu-id="0186e-125">Select the **Call Park** tab.</span></span>

4.  <span data-ttu-id="0186e-126">Для каждого диапазона на расстоянии по орбите, назначенного для пула Lync Server 2010, измените **полное доменное имя** в параметрах конечного сервера и выберите пул Lync Server 2013, который будет обрабатывать запросы на остановку звонков.</span><span class="sxs-lookup"><span data-stu-id="0186e-126">For each Call Park orbit range assigned to a Lync Server 2010 pool, edit the **FQDN of destination server** setting and select the Lync Server 2013 pool that will process the Call Park requests.</span></span>

5.  <span data-ttu-id="0186e-127">Нажмите **кнопку Сохранить,** чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="0186e-127">Select **Commit** to save the changes.</span></span>

<span data-ttu-id="0186e-128">**Переназначение всех диапазонов на орбиту на приостановку работы с помощью командной консоли Lync Server Management Shell**</span><span class="sxs-lookup"><span data-stu-id="0186e-128">**Reassign all Call Park Orbit Ranges using Lync Server Management Shell**</span></span>

1.  <span data-ttu-id="0186e-129">Откройте командную консоль Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0186e-129">Open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="0186e-130">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0186e-130">At the command line, type the following:</span></span>
    ```powershell
    Get-CsCallParkOrbit
    ```
    
    <span data-ttu-id="0186e-131">Этот командлет выводит список всех диапазонов орбиты на вкладке "приостановить".</span><span class="sxs-lookup"><span data-stu-id="0186e-131">This cmdlet lists all of the Call Park orbit ranges in the deployment.</span></span> <span data-ttu-id="0186e-132">Все орбиты, в которых параметры **CallParkServiceId** и **CallParkServerFqdn** устанавливаются в качестве пула Lync Server 2010, должны быть переназначены.</span><span class="sxs-lookup"><span data-stu-id="0186e-132">All Call Park orbits that have the **CallParkServiceId** and **CallParkServerFqdn** parameters set as the Lync Server 2010 pool must be reassigned.</span></span>
    
    <span data-ttu-id="0186e-133">Чтобы переназначить диапазоны орбиты для сервера Lync Server 2010 в пул Lync Server 2013, в командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0186e-133">To reassign the Lync Server 2010 Call Park orbit ranges to the Lync Server 2013 pool, at the command line, type the following:</span></span>
    
    ```powershell
    Set-CsCallParkOrbit -Identity "<Call Park Orbit Identity>" -CallParkService "service:ApplicationServer:<Lync Server 2013 Pool FQDN>"
    ```

<span data-ttu-id="0186e-134">После того как переназначить все диапазоны орбиты на приостановку звонков в пул Lync Server 2013, процесс миграции для приложения парковки на приостановке будет завершен, а пул Lync Server 2013 будет обрабатывать все будущие запросы на приостановку звонков.</span><span class="sxs-lookup"><span data-stu-id="0186e-134">After reassigning all Call Park orbit ranges to the Lync Server 2013 pool, the migration process for the Call Park application will be completed and the Lync Server 2013 pool will handle all future Call Park requests.</span></span>

<span data-ttu-id="0186e-135"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0186e-135"></div>

<span> </span>

</div>

</div>

</span></span></div>

