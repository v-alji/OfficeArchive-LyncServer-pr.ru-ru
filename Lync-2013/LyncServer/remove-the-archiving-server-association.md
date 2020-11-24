---
title: Удаление связи с сервером архивирования
description: Удалите сервер архивации связи.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the Archiving server association
ms:assetid: dabac157-71ee-4afe-b0b6-4a083d165ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721903(v=OCS.15)
ms:contentKeyID: 49733837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f6c34e49b0217a8318a83752b3878a7625e5d58
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400084"
---
# <a name="remove-the-archiving-server-association"></a><span data-ttu-id="8ea03-103">Удаление связи с сервером архивирования</span><span class="sxs-lookup"><span data-stu-id="8ea03-103">Remove the Archiving server association</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ea03-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ea03-104">

<span> </span></span></span>

<span data-ttu-id="8ea03-105">_**Тема последнего изменения:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="8ea03-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="8ea03-106">Для удаления сервера архивации необходимо изменить или снять зависимость на связанном пуле интерфейсов, сервере переднего плана, работающем устройстве филиала и бесперебойном сервере подразделения.</span><span class="sxs-lookup"><span data-stu-id="8ea03-106">To remove an Archiving Server, you need to change or clear the dependency on the associated Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server.</span></span> <span data-ttu-id="8ea03-107">Вы можете изменить свойства пула переднего плана, сервер переднего плана, бесперебойно работающее устройство филиалов и бесперебойный сервер филиала, чтобы удалить зависимость.</span><span class="sxs-lookup"><span data-stu-id="8ea03-107">You edit the properties of the Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server to remove the dependency.</span></span> <span data-ttu-id="8ea03-108">После очистки зависимости и удаления сервера в построителе топологии вы будете уведомлены о том, что связанный объект хранилища базы данных в построителе топологии также будет удален.</span><span class="sxs-lookup"><span data-stu-id="8ea03-108">After you clear the dependency and you delete the server in Topology Builder, you are notified that the associated database store object in Topology Builder will also be deleted.</span></span>

<div>

## <a name="to-remove-the-archiving-server-association"></a><span data-ttu-id="8ea03-109">Удаление сопоставления сервера архивации</span><span class="sxs-lookup"><span data-stu-id="8ea03-109">To remove the Archiving Server association</span></span>

1.  <span data-ttu-id="8ea03-110">Откройте сервер клиентского доступа Lync Server 2013, откройте построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="8ea03-110">Open the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="8ea03-111">Перейдите на узел Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="8ea03-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="8ea03-112">В построителе топологии разворачивание **пулов переднего плана Enterprise Edition**, **серверов переднего плана Standard Edition** и **сайтов филиалов** в зависимости от того, где определен сервер архивации.</span><span class="sxs-lookup"><span data-stu-id="8ea03-112">In Topology Builder, expand **Enterprise Edition Front End pools**, **Standard Edition Front End Servers**, or **Branch sites**, based on where the Archiving Server is defined.</span></span>

4.  <span data-ttu-id="8ea03-113">Если у вас есть связанный сервер филиалов, разверните **сайты филиалов**, разверните имя сайта филиала, а затем разверните **бесперебойно управляемые устройства филиалов**.</span><span class="sxs-lookup"><span data-stu-id="8ea03-113">If you have Survivable Branch Server associated, expand **Branch sites**, expand the branch site name, and then expand **Survivable Branch Appliances**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8ea03-114"><STRONG>Бесперебойно управляемые устройства ветвления</STRONG> в пользовательском интерфейсе применяются как к бесперебойному, так и к бесперебойному устройству филиала.</span><span class="sxs-lookup"><span data-stu-id="8ea03-114"><STRONG>Survivable Branch Appliances</STRONG> in the user interface applies to both Survivable Branch Server and Survivable Branch Appliance.</span></span>

    
    </div>

5.  <span data-ttu-id="8ea03-115">Щелкните правой кнопкой мыши пул, сервер или устройство, связанные с сервером архивации, а затем выберите команду **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="8ea03-115">Right-click the pool, server, or device that is associated with the Archiving Server, and then click **Edit Properties**.</span></span>

6.  <span data-ttu-id="8ea03-116">В диалоговом окне **изменение свойств** в разделе **Общие** в группе **сопоставления** снимите флажок **сопоставить сервер архивации** , а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ea03-116">In **Edit Properties**, under **General**, under **Associations**, clear the **Associate Archiving Server** check box, and then click **OK**.</span></span>

7.  <span data-ttu-id="8ea03-117">Повторите предыдущий шаг для любого другого пула, сервера или устройства, связанного с сервером архивации, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="8ea03-117">Repeat the previous step for any other pool, server or device associated with the Archiving Server that you want to remove.</span></span>

8.  <span data-ttu-id="8ea03-118">Щелкните сервер архивации правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="8ea03-118">Right-click the Archiving Server, and then click **Delete**.</span></span>

9.  <span data-ttu-id="8ea03-119">На вкладке **удалить зависимые магазины** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ea03-119">On **Delete Dependent Stores**, click **OK**.</span></span>

10. <span data-ttu-id="8ea03-120">Опубликуйте топологию, проверьте состояние репликации, а затем при необходимости запустите мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8ea03-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="8ea03-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ea03-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

