---
title: Восстановление зеркального сервера выпуска Enterprise Edition на обратной стороне
description: Восстановление зеркального сервера выпуска Enterprise Edition, зеркально отображении.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a mirrored Enterprise Edition Back End Server - mirror
ms:assetid: 4b3c8eae-6f1f-4377-b39b-6699e725c517
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945626(v=OCS.15)
ms:contentKeyID: 51541471
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 011c0aaa10ffed6fef7d579dbc16993fd3341070
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436239"
---
# <a name="restoring-a-mirrored-enterprise-edition-back-end-server-in-lync-server-2013---mirror"></a><span data-ttu-id="242e6-103">Восстановление зеркального сервера выпуска Enterprise Edition на сервере Lync Server 2013 — зеркало</span><span class="sxs-lookup"><span data-stu-id="242e6-103">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="242e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="242e6-104">

<span> </span></span></span>

<span data-ttu-id="242e6-105">_**Тема последнего изменения:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="242e6-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="242e6-106">Если в зеркальной конфигурации есть сервер, на котором установлен выпуск Enterprise Edition, и только зеркало не удалось выполнить, выполните действия, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="242e6-106">If you have an Enterprise Edition Back End Server in a mirrored configuration and only the mirror fails, follow the procedures in this section.</span></span> <span data-ttu-id="242e6-107">В случае сбоя основной базы данных и зеркала ознакомьтесь со сведениями о [восстановлении сервера выпуска Enterprise Edition в Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span><span class="sxs-lookup"><span data-stu-id="242e6-107">If both the primary database and mirror fail, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span></span> <span data-ttu-id="242e6-108">Если происходит сбой, ознакомьтесь со сведениями о том, [как восстановить зеркальный сервер выпуска Enterprise Edition в Lync server 2013-PRIMARY](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md).</span><span class="sxs-lookup"><span data-stu-id="242e6-108">If only the primary fails, see [Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md).</span></span> <span data-ttu-id="242e6-109">Если база данных, на которой размещено центральное хранилище, не проходит, ознакомьтесь со сведениями о том, как [восстановить сервер, на котором размещено центральное хранилище в Lync server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span><span class="sxs-lookup"><span data-stu-id="242e6-109">If the database hosting the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span> <span data-ttu-id="242e6-110">Если сервер, на котором выводится сообщение, не входит в состав сервера Enterprise Edition, ознакомьтесь со сведениями о [восстановлении рядового сервера выпуска Enterprise Edition в Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="242e6-110">If an Enterprise Edition member server that is not the Back End Server fails, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="242e6-111">Прежде чем начать восстановление, мы рекомендуем использовать копию системы с изображением.</span><span class="sxs-lookup"><span data-stu-id="242e6-111">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="242e6-112">Вы можете использовать это изображение как точку отката, если что-то пойдет не так во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="242e6-112">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="242e6-113">После установки операционной системы и сервера SQL Server вы можете использовать копию изображения, а также восстановить или подать заявку на сертификаты.</span><span class="sxs-lookup"><span data-stu-id="242e6-113">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>

<div>

## <a name="to-restore-an-enterprise-edition-back-end-server-mirror-database"></a><span data-ttu-id="242e6-114">Восстановление зеркальной базы данных сервера Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="242e6-114">To restore an Enterprise Edition Back End Server Mirror Database</span></span>

1.  <span data-ttu-id="242e6-115">Войдите на сервер переднего плана из учетной записи пользователя, который является членом группы RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="242e6-115">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

2.  <span data-ttu-id="242e6-116">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="242e6-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="242e6-117">Удаление зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="242e6-117">Uninstall mirroring.</span></span> <span data-ttu-id="242e6-118">Сначала введите следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="242e6-118">First, type the following cmdlet:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn <PrimaryServerFqdn> -SqlInstanceName <SQLInstance> -verbose
    
    <span data-ttu-id="242e6-119">Например:</span><span class="sxs-lookup"><span data-stu-id="242e6-119">For example:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn server4.contoso.com -SqlInstanceName archinst -verbose
    
    <span data-ttu-id="242e6-120">Сделайте это для всех типов баз данных на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="242e6-120">Do this for all database types on this server.</span></span>

4.  <span data-ttu-id="242e6-121">Создайте чистый или новый сервер с таким же полным доменным именем (FQDN) (DB1.contoso.com) в качестве компьютера, на котором произошел сбой, установите операционную систему, а затем восстановите или порегистрируйте сертификаты.</span><span class="sxs-lookup"><span data-stu-id="242e6-121">Create a clean or new server that has the same fully qualified domain name (FQDN) (DB1.contoso.com) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span> <span data-ttu-id="242e6-122">Этот сервер будет работать в качестве новой зеркальной копии.</span><span class="sxs-lookup"><span data-stu-id="242e6-122">This server will function as the new mirror.</span></span>

5.  <span data-ttu-id="242e6-123">Войдите в учетную запись пользователя, которая входит в группу RTCUniversalServerAdmins, на новый сервер.</span><span class="sxs-lookup"><span data-stu-id="242e6-123">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the new server.</span></span>

6.  <span data-ttu-id="242e6-124">Установите SQL Server 2012 или SQL Server 2008 R2, сохранив имена экземпляров так же, как и до сбоя.</span><span class="sxs-lookup"><span data-stu-id="242e6-124">Install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>

7.  <span data-ttu-id="242e6-125">Войдите на сервер переднего плана из учетной записи пользователя, который является членом группы RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="242e6-125">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

8.  <span data-ttu-id="242e6-126">Используйте построитель топологии, чтобы установить зеркальную базу данных.</span><span class="sxs-lookup"><span data-stu-id="242e6-126">Use Topology Builder to install the mirror database.</span></span> <span data-ttu-id="242e6-127">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="242e6-127">Perform the following:</span></span>
    
      - <span data-ttu-id="242e6-128">Запустить построитель топологии: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="242e6-128">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="242e6-129">Щелкните правой кнопкой мыши узел Lync Server 2013, выберите пункт **топология** и щелкните **установить базу данных**.</span><span class="sxs-lookup"><span data-stu-id="242e6-129">Right-click the Lync Server 2013 node, click **Topology**, and then click **Install Database**.</span></span>
    
      - <span data-ttu-id="242e6-130">Следуйте указаниям мастера **установки базы данных** .</span><span class="sxs-lookup"><span data-stu-id="242e6-130">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="242e6-131">На странице **Создание баз данных** выберите базы данных, которые вы хотите повторно создать.</span><span class="sxs-lookup"><span data-stu-id="242e6-131">On the **Create databases** page, select the databases that you want to recreate.</span></span>
    
      - <span data-ttu-id="242e6-132">Следуйте указаниям мастера, пока не появится запрос на **Создание зеркальной базы данных** .</span><span class="sxs-lookup"><span data-stu-id="242e6-132">Follow the wizard until a prompt of **Create Mirror Database** appears.</span></span> <span data-ttu-id="242e6-133">Выберите базу данных, которую вы хотите установить, и выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="242e6-133">Select the database that you want to install and complete this process.</span></span>
        
        <div>
        

        > [!TIP]
        > <span data-ttu-id="242e6-134">Вместо того чтобы запустить построитель топологии, вы можете использовать командлет <STRONG>Install-CsMirrorDatabase</STRONG> для настройки зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="242e6-134">Instead of running Topology Builder, you can use the <STRONG>Install-CsMirrorDatabase</STRONG> cmdlet to configure mirroring.</span></span> <span data-ttu-id="242e6-135">Подробные сведения можно найти в руководстве по среде Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="242e6-135">For details, see the Lync Server Management Shell documentation.</span></span>

        
        <span data-ttu-id="242e6-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="242e6-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

