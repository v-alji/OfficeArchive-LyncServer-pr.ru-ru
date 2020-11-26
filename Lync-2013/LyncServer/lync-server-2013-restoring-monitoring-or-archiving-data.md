---
title: 'Lync Server 2013: восстановление данных мониторинга или архивация'
description: 'Lync Server 2013: восстановление данных мониторинга или архивация.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring monitoring or archiving data
ms:assetid: 60118526-13bb-4b03-803e-6ffae219d436
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202175(v=OCS.15)
ms:contentKeyID: 51541483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 169a5da2d606b97c7cd3f59d6cbae3d4c584e6e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442525"
---
# <a name="restoring-monitoring-or-archiving-data-in-lync-server-2013"></a><span data-ttu-id="a19f0-103">Восстановление данных мониторинга или архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a19f0-103">Restoring monitoring or archiving data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a19f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a19f0-104">

<span> </span></span></span>

<span data-ttu-id="a19f0-105">_**Тема последнего изменения:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="a19f0-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="a19f0-106">Для восстановления данных мониторинга и архивации не требуется, чтобы приложение Lync Server выработало после сбоя.</span><span class="sxs-lookup"><span data-stu-id="a19f0-106">Restoring monitoring and archiving data is not required to get Lync Server up and running after a failure.</span></span> <span data-ttu-id="a19f0-107">Однако если данные мониторинга и архивация критически важны для вашей организации, то после повторного создания баз данных вам потребуется восстановить данные.</span><span class="sxs-lookup"><span data-stu-id="a19f0-107">However, if monitoring and archiving data is critical to your organization, you will want to restore the data after you re-create the databases.</span></span>

<span data-ttu-id="a19f0-108">Ниже описано, как использовать SQL Server Management Studio для восстановления архивирования или наблюдения за данными.</span><span class="sxs-lookup"><span data-stu-id="a19f0-108">The following procedure describes how to use SQL Server Management Studio to restore archiving or monitoring data.</span></span>

<div>

## <a name="to-restore-monitoring-or-archiving-data-from-a-backup-file"></a><span data-ttu-id="a19f0-109">Восстановление или архивация данных из файла резервной копии</span><span class="sxs-lookup"><span data-stu-id="a19f0-109">To restore monitoring or archiving data from a backup file</span></span>

1.  <span data-ttu-id="a19f0-110">Войдите на сервер, который вы восстанавливаете в качестве участника группы администраторов на локальном компьютере или в группе с эквивалентными правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="a19f0-110">Log on to the server that you are restoring as a member of the Administrators group on the local computer or a group with equivalent user rights.</span></span>

2.  <span data-ttu-id="a19f0-111">Откройте приложение SQL Server Management Studio: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft SQL Server 2012** или **Microsoft SQL Server 2008 R2**, а затем щелкните **SQL Server Management Studio**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-111">Open SQL Server Management Studio: click **Start**, click **All Programs**, click **Microsoft SQL Server 2012** or **Microsoft SQL Server 2008 R2**, and then click **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="a19f0-112">В разделе **Подключение к серверу** подключитесь к экземпляру SQL Server, указав по крайней мере имя сервера и данные для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a19f0-112">In **Connect to Server**, connect to the SQL Server instance by providing at least the name of the server and the authentication information.</span></span>

4.  <span data-ttu-id="a19f0-113">В **обозревателе объектов** щелкните правой кнопкой мыши **базу данных** и выберите команду **восстановить базу данных**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-113">In **Object Explorer**, right-click **Databases**, and then click **Restore Database**.</span></span>

5.  <span data-ttu-id="a19f0-114">В разделе **Выбор страницы** выберите пункт **Общие**, а затем в поле **база данных** выберите имя базы данных, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="a19f0-114">Under **Select a page**, click **General**, and then in **To database** select the database name as follows:</span></span>
    
      - <span data-ttu-id="a19f0-115">Для базы данных архивации выберите **LcsLog**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-115">For an Archiving database, select **LcsLog**.</span></span>
    
      - <span data-ttu-id="a19f0-116">Для базы данных записи сведений о звонке (CDR) выберите **LcsCDR**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-116">For a call detail recording (CDR) database, select **LcsCDR**.</span></span>
    
      - <span data-ttu-id="a19f0-117">В качестве базы данных качества взаимодействия (QoE) выберите **QoEMetrics**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-117">For a Quality of Experience (QoE) database, select **QoEMetrics**.</span></span>

6.  <span data-ttu-id="a19f0-118">Щелкните **с устройства**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-118">Click **From device**.</span></span>

7.  <span data-ttu-id="a19f0-119">В разделе **Выберите резервные наборы данных для восстановления** щелкните файл резервной копии, а затем нажмите кнопку **восстановить**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-119">Under **Select the backup sets to restore**, click the backup file, and then click **Restore**.</span></span>

8.  <span data-ttu-id="a19f0-120">В разделе **выберите страницу** нажмите кнопку **Параметры**, убедитесь, что путь к файлу данных и путь к журналу находятся в нужной папке, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-120">Under **Select a page**, click **Options**, verify that the data file path and log path are in the correct folder, and then click **OK**.</span></span>

</div>

<div>

## <a name="to-make-sure-that-access-control-lists-acls-are-correct"></a><span data-ttu-id="a19f0-121">Проверка правильности списков контроля доступа (ACL)</span><span class="sxs-lookup"><span data-stu-id="a19f0-121">To make sure that access control lists (ACLs) are correct</span></span>

1.  <span data-ttu-id="a19f0-122">Разверните **базу данных, разверните** папку Архивация или мониторинг, разверните раздел **Безопасность**, а затем разверните раздел **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-122">Expand **Databases**, expand the archiving or monitoring database, expand **Security**, and then expand **Users**.</span></span>

2.  <span data-ttu-id="a19f0-123">Убедитесь, что группа домена RTCComponentUniversalServices существует в качестве пользователя.</span><span class="sxs-lookup"><span data-stu-id="a19f0-123">Verify that the domain group RTCComponentUniversalServices exists as a user.</span></span>

3.  <span data-ttu-id="a19f0-124">Если RTCComponentUniversalServices не существует в разделе **Пользователи**, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="a19f0-124">If RTCComponentUniversalServices does not exist under **Users**, do the following:</span></span>
    
    1.  <span data-ttu-id="a19f0-125">Щелкните правой кнопкой мыши **пользователей** и выберите команду **создать пользователя**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-125">Right-click **Users**, and then click **New User**.</span></span>
    
    2.  <span data-ttu-id="a19f0-126">В поле **имя пользователя** введите имя отсутствующей группы RTCComponentUniversalServices.</span><span class="sxs-lookup"><span data-stu-id="a19f0-126">In **Login name**, type the missing group name, RTCComponentUniversalServices.</span></span>
    
    3.  <span data-ttu-id="a19f0-127">В разделе **членство в роли базы данных** выберите разрешение **serverRole** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a19f0-127">Under **Database role membership**, select the **ServerRole** permission, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a19f0-128">Вам не нужно перезапускать службу архивации или наблюдения.</span><span class="sxs-lookup"><span data-stu-id="a19f0-128">You do not need to restart the archiving or monitoring service.</span></span>

    
    <span data-ttu-id="a19f0-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a19f0-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

