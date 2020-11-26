---
title: 'Lync Server 2013: изменение параметров архивной базы данных'
description: 'Lync Server 2013: изменение параметров архивированной базы данных.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing Archiving database options
ms:assetid: 3775f09d-65b0-48bc-8a4d-d97bd0c3423c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204814(v=OCS.15)
ms:contentKeyID: 48183879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a3751be63e17688ad9258b9773a1a5397b67952
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435063"
---
# <a name="changing-archiving-database-options-in-lync-server-2013"></a><span data-ttu-id="1fda7-103">Изменение параметров базы данных для архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fda7-103">Changing Archiving database options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1fda7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1fda7-104">

<span> </span></span></span>

<span data-ttu-id="1fda7-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1fda7-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1fda7-106">Если вы разворачиваете архивацию с помощью хранилища SQL Server для хранения данных для любого из ваших пользователей, вы можете внести следующие изменения в хранилище базы данных.</span><span class="sxs-lookup"><span data-stu-id="1fda7-106">If you deploy Archiving using SQL Server storage for archiving storage for any of your users, you can make the following database storage changes:</span></span>

  - <span data-ttu-id="1fda7-107">Используйте другую базу данных SQL Server для хранения архивов.</span><span class="sxs-lookup"><span data-stu-id="1fda7-107">Use a different SQL Server database for archiving storage.</span></span> <span data-ttu-id="1fda7-108">Сюда относится основная база данных архивации и любая база данных, которую вы используете для зеркального отображения SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fda7-108">This includes the primary Archiving database and any database you use for SQL Server mirroring.</span></span>

  - <span data-ttu-id="1fda7-109">Переключение на интеграцию Microsoft Exchange для хранения данных и файлов для архивации на серверах Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1fda7-109">Switch to Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers.</span></span> <span data-ttu-id="1fda7-110">Если все пользователи находятся на серверах Exchange 2013 и вы хотите использовать хранилище Microsoft Exchange для всех пользователей в развертывании, необходимо удалить из топологии базы данных из магазина SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fda7-110">If all your users are homed on your Exchange 2013 servers and you want to use Microsoft Exchange storage for all users in your deployment, you should remove the SQL Server store databases from your topology.</span></span>

<span data-ttu-id="1fda7-111">Чтобы внести оба эти изменения, необходимо запустить построитель топологии, внести изменения, а затем опубликовать топологию еще раз.</span><span class="sxs-lookup"><span data-stu-id="1fda7-111">To make either of these changes, you must run Topology Builder, make the changes, and then publish the topology again.</span></span> <span data-ttu-id="1fda7-112">Это можно сделать с помощью Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="1fda7-112">You can use Topology Builder to do this.</span></span> <span data-ttu-id="1fda7-113">Не указывайте параметр **Архивирование хранилища SQL Server** или включите сведения о **зеркальном отображении хранилища SQL Server** , если только у вас нет пользователей Lync, не подключенных к серверам Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1fda7-113">Do not specify **Archiving SQL Server store** or **Enable SQL Server store mirroring** information, unless you have Lync users who are not homed on Exchange 2013 servers.</span></span>

<div>

## <a name="to-change-your-archiving-database-option"></a><span data-ttu-id="1fda7-114">Изменение параметров архивной базы данных</span><span class="sxs-lookup"><span data-stu-id="1fda7-114">To change your archiving database option</span></span>

1.  <span data-ttu-id="1fda7-115">На компьютере, на котором работает Lync Server 2013 или на котором установлены средства администрирования сервера Lync, войдите в систему с помощью учетной записи, которая является членом локальной группы пользователей (или учетной записи с эквивалентными правами пользователей).</span><span class="sxs-lookup"><span data-stu-id="1fda7-115">On a computer that is running Lync Server 2013, or on which the Lync Server administrative tools are installed, log on by using an account that is a member of the local Users group (or an account with equivalent user rights).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1fda7-116">Вы можете определить топологию с помощью учетной записи, которая является членом локальной группы "Пользователи", но для публикации топологии, необходимой для добавления компонента в топологию, необходимо использовать учетную запись, которая входит в группу <STRONG>"Администраторы домена"</STRONG> и в группу " <STRONG>RTCUniversalServerAdmins</STRONG> ". и у него есть разрешения на полный доступ (например, чтение, запись и изменение) в общей папке, которую вы используете для хранения файлов Lync Server 2013 (это значит, что построитель топологии может настроить нужные списки управления доступом на уровне пользователей (DACL) или учетную запись с эквивалентными правами.</span><span class="sxs-lookup"><span data-stu-id="1fda7-116">You can define a topology by using an account that is a member of the local Users group, but to publish a topology, which is required to add a component to the topology, you must use an account that is a member of the <STRONG>Domain Admins</STRONG> group and the <STRONG>RTCUniversalServerAdmins</STRONG> group, and that has full control permissions (that is, read, write, and modify) on the file share that you are using for the Lync Server 2013 file store (that is, so that Topology Builder can configure the required discretionary access control lists (DACLs), or an account with equivalent rights.</span></span>

    
    </div>

2.  <span data-ttu-id="1fda7-117">Запустите построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="1fda7-117">Start Topology Builder.</span></span>

3.  <span data-ttu-id="1fda7-118">В дереве консоли перейдите к интерфейсному пулу, в котором развернута служба архивирования, и затем щелкните название пула, где нужно изменить параметры базы данных.</span><span class="sxs-lookup"><span data-stu-id="1fda7-118">In the console tree, navigate to the Front End pool in which you deployed Archiving, and then click the name of the Front End pool where you want to change the database options.</span></span>

4.  <span data-ttu-id="1fda7-119">В меню **Действие** выберите **Изменение свойств**.</span><span class="sxs-lookup"><span data-stu-id="1fda7-119">In the **Action** menu, click **Edit Properties**.</span></span>

5.  <span data-ttu-id="1fda7-120">В диалоговом окне **Изменение свойств** щелкните **Общие**.</span><span class="sxs-lookup"><span data-stu-id="1fda7-120">In the **Edit Properties** dialog box, click **General**.</span></span>

6.  <span data-ttu-id="1fda7-121">Прокрутите вниз до раздела **Архивация**.</span><span class="sxs-lookup"><span data-stu-id="1fda7-121">Scroll down to **Archiving**.</span></span>

7.  <span data-ttu-id="1fda7-122">В разделе **Архивация** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1fda7-122">In **Archiving**, do the following:</span></span>
    
      - <span data-ttu-id="1fda7-123">Для перехода к другому существующему хранилищу SQL Server в раскрывающемся списке **Хранилище архивации SQL Server** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1fda7-123">To change to a different existing SQL Server store, under **Archiving SQL Server store**, in the drop-down list box, do the following:</span></span>
        
          - <span data-ttu-id="1fda7-124">Чтобы использовать имеющееся хранилище SQL Server в раскрывающемся списке щелкните название нужного хранилища.</span><span class="sxs-lookup"><span data-stu-id="1fda7-124">To use an existing SQL Server store, in the drop-down list box, click the name of the SQL Server store that you want to use.</span></span>
        
          - <span data-ttu-id="1fda7-125">Для задания нового хранилища SQL Server щелкните **Создать**, затем в диалоговом окне **Определение нового хранилища SQL Server** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1fda7-125">To specify a new SQL Server store, click **New**, and then in the **Define New SQL Server store** dialog box, do the following:</span></span>
            
              - <span data-ttu-id="1fda7-126">Чтобы использовать имеющееся хранилище SQL Server в раскрывающемся списке щелкните название нужного хранилища.</span><span class="sxs-lookup"><span data-stu-id="1fda7-126">To use an existing SQL Server store, in the drop-down list box, click the name of the SQL Server store that you want to use.</span></span>
            
              - <span data-ttu-id="1fda7-127">Чтобы указать новое хранилище SQL Server, нажмите кнопку **создать**, а затем в диалоговом окне **Определение нового хранилища SQL Server** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1fda7-127">To specify a new SQL Server store, click **New**, and then in the **Define New SQL Server Store** dialog box, do the following:</span></span>
                
                  - <span data-ttu-id="1fda7-128">В **доменном имени SQL Server** укажите полное доменное имя сервера, на котором вы хотите создать новое хранилище SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fda7-128">In **SQL Server FQDN**, specify the FQDN of the server on which you want to create the new SQL Server store.</span></span>
                
                  - <span data-ttu-id="1fda7-129">Для применения экземпляра по умолчанию щелкните **Экземпляр по умолчанию**; для задания другого экземпляра щелкните **Именованный экземпляр**, затем укажите требуемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1fda7-129">Either click **Default Instance** to use the default instance, or, to specify a different instance, click **Named instance**, and then specify the instance you want to use.</span></span>
                
                  - <span data-ttu-id="1fda7-130">Если указанный экземпляр SQL Server находится в отношении отражения, установите флажок **этот экземпляр SQL находится в отношении зеркального отображения** , а затем в поле **номер зеркального порта** укажите номер порта.</span><span class="sxs-lookup"><span data-stu-id="1fda7-130">If the specified SQL Server instance is in a mirroring relationship, select the **This SQL instance is in mirroring relation** check box, and then, in **Mirror port number**, specify the port number.</span></span>
    
      - <span data-ttu-id="1fda7-131">Если требуется добавить хранилище SQL Server для зеркального отображения или назначить для зеркального отображения хранилища SQL Server другое существующее хранилище, установите флажок **Включить зеркалирование хранилища SQL Server**, затем выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1fda7-131">To add SQL Server store for mirroring or change to a different existing SQL Server store for SQL Server store mirroring, select **Enable SQL Server store mirroring**, and then do the following:</span></span>
        
          - <span data-ttu-id="1fda7-132">Чтобы использовать существующее хранилище SQL Server для зеркального отображения, в раскрывающемся списке " **Архивирование хранилища SQL Server** " выберите имя хранилища SQL Server, которое вы хотите использовать для зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="1fda7-132">To use an existing SQL Server store for mirroring, in the **Archiving SQL Server store mirror** drop-down list box, click the name of the SQL Server store that you want to use for mirroring.</span></span>
        
          - <span data-ttu-id="1fda7-133">Чтобы указать новое хранилище SQL Server для зеркального отображения, нажмите кнопку **создать**, а затем в диалоговом окне **Определение нового хранилища SQL Server** выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="1fda7-133">To specify a new SQL Server store for mirroring, click **New**, and then in the **Define New SQL Server Store** dialog box, do one of the following:</span></span>
            
            1.  <span data-ttu-id="1fda7-134">В **доменном имени SQL Server** укажите полное доменное имя сервера SQL Server, на котором вы хотите создать новое хранилище SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fda7-134">In **SQL Server FQDN**, specify the FQDN of the SQL Server on which you want to create the new SQL Server store.</span></span>
            
            2.  <span data-ttu-id="1fda7-135">Для применения экземпляра по умолчанию щелкните **Экземпляр по умолчанию**; для задания другого экземпляра щелкните **Именованный экземпляр**, затем укажите требуемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1fda7-135">Either click **Default Instance** to use the default instance, or, to specify a different instance, click **Named Instance**, and then specify the instance you want to use.</span></span>
            
            3.  <span data-ttu-id="1fda7-136">Если указанный экземпляр SQL Server находится в отношении отражения, установите флажок **этот экземпляр SQL находится в отношении зеркального отображения** , а затем в поле **номер зеркального порта** укажите номер порта.</span><span class="sxs-lookup"><span data-stu-id="1fda7-136">If the specified SQL Server instance is in a mirroring relationship, select the **This SQL instance is in mirroring relation** check box, and then, in **Mirror port number**, specify the port number.</span></span>
        
          - <span data-ttu-id="1fda7-137">Если вы включите зеркальное отображение SQL Server и хотите добавить или изменить следящий сервер SQL Server (третий, отдельный экземпляр SQL Server, который может определять работоспособность основного сервера SQL Server и зеркальных экземпляров), установите флажок **использовать следящий сервер зеркального отображения SQL Server, чтобы включить автоматический переход на другой ресурс** , а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="1fda7-137">If you enable SQL Server mirroring and want to add or change a SQL Server mirroring witness (a third, separate SQL Server instance that can detect the health of the primary SQL Server server and mirror instances), select the **Use SQL Server mirroring witness to enable automatic failover** check box, and then do one of the following:</span></span>
            
            1.  <span data-ttu-id="1fda7-138">В **доменном имени SQL Server** укажите полное доменное имя сервера, на котором вы хотите создать новый следящий сервер SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fda7-138">In **SQL Server FQDN**, specify the FQDN of the server on which you want to create the new SQL Server mirroring witness.</span></span>
            
            2.  <span data-ttu-id="1fda7-139">Для применения экземпляра по умолчанию щелкните **Экземпляр по умолчанию**; для задания другого экземпляра щелкните **Именованный экземпляр**, затем укажите экземпляр, который будет служить следящим сервером зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="1fda7-139">Either click **Default Instance** to use the default instance, or, to specify a different instance, click **Named Instance**, and then specify the instance you want to use for the mirroring witness.</span></span>
            
            3.  <span data-ttu-id="1fda7-140">Если указанный экземпляр SQL Server находится в отношении отражения, установите флажок **этот экземпляр SQL находится в отношении зеркального отображения** , а затем в поле **номер зеркального порта** укажите номер порта.</span><span class="sxs-lookup"><span data-stu-id="1fda7-140">If the specified SQL Server instance is in a mirroring relationship, select the **This SQL instance is in mirroring relation** check box, and then, in **Mirror port number**, specify the port number.</span></span>
    
      - <span data-ttu-id="1fda7-141">Чтобы переключиться на Microsoft Exchange Integration для хранения архивированных данных и файлов на серверах Exchange 2013 (если все пользователи в развертывании размещены на серверах Exchange 2013), удалите все данные для архивации баз данных.</span><span class="sxs-lookup"><span data-stu-id="1fda7-141">To switch to Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers (if all users in your deployment are homed on your Exchange 2013 servers), delete all information for Archiving databases.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1fda7-142">Если у вас есть пользователи Lync, которые не размещены на серверах Exchange 2013, не удаляйте данные из магазина SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fda7-142">If you have any Lync users who are not homed on Exchange 2013 servers, do not delete the SQL Server store information.</span></span>

    
    </div>

8.  <span data-ttu-id="1fda7-143">Для сохранения конфигурации нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1fda7-143">To save the configuration, click **OK**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1fda7-144">Изменения, внесенные в построителе топологии, вступают в силу только после публикации новой топологии.</span><span class="sxs-lookup"><span data-stu-id="1fda7-144">The changes you make in Topology Builder do not take effect until you publish the new topology.</span></span> <span data-ttu-id="1fda7-145">Подробности можно найти в разделе <A href="lync-server-2013-publishing-the-updated-topology-to-add-archiving-databases.md">Публикация обновленной топологии для добавления баз данных архивации в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="1fda7-145">For details, see <A href="lync-server-2013-publishing-the-updated-topology-to-add-archiving-databases.md">Publishing the updated topology to add Archiving databases in Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    <span data-ttu-id="1fda7-146"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1fda7-146"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

