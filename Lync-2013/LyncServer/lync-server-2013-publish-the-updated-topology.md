---
title: 'Lync Server 2013: публикация обновленной топологии'
description: 'Lync Server 2013: публикация обновленной топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the updated topology
ms:assetid: 59455dd1-6a9e-433f-a714-d3636c068100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204910(v=OCS.15)
ms:contentKeyID: 48184203
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c27cca2eae86eadaf1ff37e2c3520eaec3f86c98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399049"
---
# <a name="publish-the-updated-topology-in-lync-server-2013"></a><span data-ttu-id="54eb7-103">Публикация обновленной топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54eb7-103">Publish the updated topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54eb7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54eb7-104">

<span> </span></span></span>

<span data-ttu-id="54eb7-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="54eb7-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="54eb7-106">После обновления топологии в построителе топологии необходимо опубликовать топологию в хранилище Central Management, прежде чем можно будет настроить и использовать сохраняемый сервер чата.</span><span class="sxs-lookup"><span data-stu-id="54eb7-106">After updating your topology in Topology Builder, you must publish the topology to the Central Management store before you can configure and use Persistent Chat Server.</span></span> <span data-ttu-id="54eb7-107">Копии данных, доступные только для чтения, реплицируются на все серверы в топологии, чтобы они были синхронизированы с топологией и другими изменениями конфигурации.</span><span class="sxs-lookup"><span data-stu-id="54eb7-107">Read-only copies of the data are replicated to all servers in the topology to keep all servers in sync with topology and other configuration changes.</span></span>

<div>

## <a name="to-publish-an-updated-topology"></a><span data-ttu-id="54eb7-108">Публикация обновленной топологии</span><span class="sxs-lookup"><span data-stu-id="54eb7-108">To publish an updated topology</span></span>

<span data-ttu-id="54eb7-109">Прежде чем публиковать топологию, установите для сервера сохраняемого чата базы данных.</span><span class="sxs-lookup"><span data-stu-id="54eb7-109">Before you publish your topology, install the databases for Persistent Chat Server.</span></span> <span data-ttu-id="54eb7-110">Используйте построитель топологии для установки баз данных, выбрав **действие** и **установить базу данных**.</span><span class="sxs-lookup"><span data-stu-id="54eb7-110">Use Topology Builder to install databases by selecting **Action** and **Install Database**.</span></span>

1.  <span data-ttu-id="54eb7-111">На компьютере с Lync Server 2013 или на котором установлены средства администрирования Lync Server, войдите в систему с помощью учетной записи, которая входит в группу **администраторов домена** и **RTCUniversalServerAdmins** . и у него есть разрешения на полный доступ (то есть чтение, запись и изменение) в хранилище файлов, которое будет использоваться для хранения файлов на сервере сохраняемого чата (чтобы Topology Builder мог настроить нужные списки управления доступом на уровне пользователей) или учетную запись с эквивалентными правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="54eb7-111">On a computer that is running Lync Server 2013 or on which the Lync Server administrative tools are installed, log on using an account that is a member of both the **Domain Admins** group and the **RTCUniversalServerAdmins** group, and that has full control permissions (that is, read, write, and modify) on the file store to be used for the Persistent Chat Server file store (so that Topology Builder can configure the required discretionary access control lists (DACLs)), or an account with equivalent user rights.</span></span>

2.  <span data-ttu-id="54eb7-112">Запустите построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="54eb7-112">Start Topology Builder.</span></span> <span data-ttu-id="54eb7-113">Выберите параметр **топология скачивания из существующего развертывания** или **открывайте топологию локального файла** , если вы сохранили его локально.</span><span class="sxs-lookup"><span data-stu-id="54eb7-113">Select **Download Topology from existing deployment**, or **Open Topology from a local file** if you saved it locally.</span></span>

3.  <span data-ttu-id="54eb7-114">В дереве консоли щелкните правой кнопкой мыши **Lync Server 2013** и выберите команду **топология публикации**.</span><span class="sxs-lookup"><span data-stu-id="54eb7-114">In the console tree, right-click **Lync Server 2013**, and then click **Publish Topology**.</span></span>

4.  <span data-ttu-id="54eb7-115">На странице **Публикация топологии** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="54eb7-115">On the **Publish the topology** page, click **Next**.</span></span>

5.  <span data-ttu-id="54eb7-116">На странице **Работа мастера публикации завершена** убедитесь, что топология успешно опубликована, а затем щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="54eb7-116">On the **Publishing wizard complete** page, verify that the topology was successfully published, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="54eb7-117">После публикации топологии необходимо настроить поддержку сервера сохраняемого чата, прежде чем можно будет архивировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="54eb7-117">After publishing the topology, you must configure support for Persistent Chat Server before any content can be archived.</span></span>

    
    <span data-ttu-id="54eb7-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54eb7-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

