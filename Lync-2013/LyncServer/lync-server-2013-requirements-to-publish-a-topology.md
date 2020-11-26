---
title: 'Lync Server 2013: требования к публикации топологии'
description: 'Lync Server 2013: требования для публикации топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements to publish a topology
ms:assetid: 841cdf5d-d884-414d-ab50-3bb681b622ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg195733(v=OCS.15)
ms:contentKeyID: 48184688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5699657e680b78587b8ba354e9dc538f2e280c56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436358"
---
# <a name="requirements-to-publish-a-topology-in-lync-server-2013"></a><span data-ttu-id="0ca9b-103">Требования к публикации топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ca9b-103">Requirements to publish a topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ca9b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ca9b-104">

<span> </span></span></span>

<span data-ttu-id="0ca9b-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0ca9b-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0ca9b-106">В этой статье описаны требования к инфраструктуре и программному обеспечению, специфичные для публикации топологии, будь то использование построителя топологии или интерфейса командной строки оболочки управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-106">This topic describes the infrastructure and software requirements that are specific to publishing a topology, whether by using Topology Builder or the Lync Server 2013 Management Shell command-line interface.</span></span> <span data-ttu-id="0ca9b-107">Эти требования описаны в дополнение к общим требованиям операционной системы, программного обеспечения и разрешений, применимым ко всем административным средствам Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-107">These requirements are in addition to the general operating system, software, and permissions requirements applicable to all Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="0ca9b-108">Прежде чем публиковать топологию, убедитесь, что все требования к средству администрирования соблюдены.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-108">Make sure that you satisfy all administrative tools requirements before you publish a topology.</span></span>

  - <span data-ttu-id="0ca9b-109">Вы должны запустить построитель топологии на компьютере, который присоединен к тому же домену или лесу Lync Server 2013, который вы создаете, чтобы завершить процесс подготовки доменных служб Active Directory, что позволит вам успешно публиковать свою топологию с помощью средств администрирования на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-109">You must run Topology Builder on a computer that is joined to the same domain or forest of the Lync Server 2013 deployment you are creating so that Active Directory Domain Services preparation steps are already completed, enabling you to use the administrative tools on that computer to successfully publish your topology.</span></span>

  - <span data-ttu-id="0ca9b-110">Компьютеры, определенные в топологии, должны быть присоединены к домену, за исключением пограничных серверов и доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-110">The computers defined in the topology must be joined to the domain, except for Edge Servers, and in AD DS.</span></span> <span data-ttu-id="0ca9b-111">Однако при публикации топологии компьютеры не должны быть подключены к сети.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-111">However, the computers do not need to be online when you publish the topology.</span></span>

  - <span data-ttu-id="0ca9b-112">Файловый общий доступ для пула должен быть создан и доступен для удаленных пользователей.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-112">The file share for the pool must be created and available to remote users.</span></span>

  - <span data-ttu-id="0ca9b-113">Для публикации пула переднего плана Enterprise Edition сервер должен быть присоединен к домену, в котором развертываются серверы, в сети и настроены соответствующие правила брандмауэра, чтобы сделать его доступным для удаленных пользователей.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-113">In order to publish an Enterprise Edition Front End pool, the SQL Server-based Back End Server must be joined to the domain in which you are deploying the servers, online, and configured with the appropriate firewall rules to make it available to remote users.</span></span> <span data-ttu-id="0ca9b-114">Подробнее об указании исключений межсетевого экрана можно узнать [в разделе сведения о требованиях к межсетевому экрану SQL Server с помощью Lync server 2013](lync-server-2013-understanding-firewall-requirements-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="0ca9b-114">For details about specifying firewall exceptions, see [Understanding firewall requirements for SQL Server with Lync Server 2013](lync-server-2013-understanding-firewall-requirements-for-sql-server.md).</span></span> <span data-ttu-id="0ca9b-115">Дополнительные сведения о настройке SQL Server можно найти в разделе [Настройка SQL Server для Lync server 2013](lync-server-2013-configure-sql-server-for-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="0ca9b-115">For other details about configuring SQL Server, see [Configure SQL Server for Lync Server 2013](lync-server-2013-configure-sql-server-for-lync-server.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0ca9b-116">Сервер Standard Edition имеет размещенную базу данных, которая будет поддерживать опубликованную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-116">Standard Edition server has a collocated database that will accept the published configuration.</span></span> <span data-ttu-id="0ca9b-117">Сначала необходимо запустить задачу настройки <STRONG>сервера first Standard Edition</STRONG> в мастере развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0ca9b-117">You must first run the <STRONG>Prepare first Standard Edition server</STRONG> setup task in the Lync Server Deployment Wizard.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="0ca9b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0ca9b-118">See Also</span></span>


[<span data-ttu-id="0ca9b-119">Публикация топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ca9b-119">Publish the topology in Lync Server 2013</span></span>](lync-server-2013-publish-the-topology.md)  
[<span data-ttu-id="0ca9b-120">Делегирование разрешений на установку в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ca9b-120">Delegate setup permissions in Lync Server 2013</span></span>](lync-server-2013-delegate-setup-permissions.md)  


[<span data-ttu-id="0ca9b-121">Программные требования для средств администрирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ca9b-121">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
[<span data-ttu-id="0ca9b-122">Поддержка сервера и средств в операционной системе в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ca9b-122">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)  


[<span data-ttu-id="0ca9b-123">Административные права и разрешения, необходимые для установки и администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ca9b-123">Administrator rights and permissions required for setup and administration of Lync Server 2013</span></span>](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md)  
  

<span data-ttu-id="0ca9b-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ca9b-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

