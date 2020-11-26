---
title: Развертывание устройства или сервера для обеспечения связи в филиалах — задача сайта филиала
description: Развертывание бесперебойно работающего устройства филиалов или задачи сайта серверной ветви.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy a Survivable Branch Appliance or Server - branch site task
ms:assetid: 7989ba29-0419-46dd-892c-4ad3238afd56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398599(v=OCS.15)
ms:contentKeyID: 48184586
ms.date: 10/29/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b84f603f185bd507111d4767a22e9009fc0e8b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430254"
---
# <a name="deploy-a-survivable-branch-appliance-or-server-with-lync-server-2013---branch-site-task"></a><span data-ttu-id="0db63-103">Развертывание устройства или сервера для обеспечения связи в филиалах с помощью Lync Server 2013 — задача сайта филиала</span><span class="sxs-lookup"><span data-stu-id="0db63-103">Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0db63-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0db63-104">

<span> </span></span></span>

<span data-ttu-id="0db63-105">_**Тема последнего изменения:** 2014-10-28_</span><span class="sxs-lookup"><span data-stu-id="0db63-105">_**Topic Last Modified:** 2014-10-28_</span></span>

<span data-ttu-id="0db63-106">Выполните одну из двух процедур, описанных в этой статье, на сайте филиала, после того как они успешно завершили развертывание работающего [устройства филиала или сервера с помощью задач Lync server 2013 — центральное место](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="0db63-106">Perform one of the two procedures described in this topic at the branch site, after successfully completing the tasks in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md).</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="0db63-107">Для выполнения этой процедуры необходимо быть членом группы RTCUniversalSBATechnicians.</span><span class="sxs-lookup"><span data-stu-id="0db63-107">To perform this procedure, you must be a member of the RTCUniversalSBATechnicians group.</span></span>



</div>

<div>

## <a name="to-deploy-the-survivable-branch-appliance"></a><span data-ttu-id="0db63-108">Развертывание бесперебойно работающего устройства филиалов</span><span class="sxs-lookup"><span data-stu-id="0db63-108">To deploy the Survivable Branch Appliance</span></span>

  - <span data-ttu-id="0db63-109">Бесперебойное развертывание управляющего устройства филиала включается в работающем разработчике устройства филиала с помощью ПОЛЬЗОВАТЕЛЬСКОГО интерфейса веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="0db63-109">Survivable Branch Appliance deployment is enabled by the Survivable Branch Appliance vendor through a web user interface (UI).</span></span> <span data-ttu-id="0db63-110">Сведения о том, как развертывать бесперебойно работающее устройство филиала, можно найти в документации, поставляемой с производителем устройства филиала.</span><span class="sxs-lookup"><span data-stu-id="0db63-110">For information about deploying the Survivable Branch Appliance, see your Survivable Branch Appliance vendor documentation.</span></span>

</div>

<div>

## <a name="to-deploy-the-survivable-branch-server"></a><span data-ttu-id="0db63-111">Развертывание бесперебойно работающего сервера филиалов</span><span class="sxs-lookup"><span data-stu-id="0db63-111">To deploy the Survivable Branch Server</span></span>

  - <span data-ttu-id="0db63-112">Установите Lync Server 2013 на компьютере под управлением Windows Server 2008 R2, Windows Server 2012 или Windows Server 2012 R2 так же, как и любую другую роль сервера Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0db63-112">Install Lync Server 2013 on a computer running Windows Server 2008 R2, Windows Server 2012, or Windows Server 2012 R2, just as you would install any other Lync Server 2013 server role.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="0db63-113">Сведения об установке Lync Server можно найти в разделе <A href="lync-server-2013-deploying-lync-server.md">развертывание Lync server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="0db63-113">For information about installing Lync Server, see <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="0db63-114">**Следующий шаг**: [Настройка пользователей для обеспечения устойчивости сайтов филиалов в Lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span><span class="sxs-lookup"><span data-stu-id="0db63-114">**Next step**: [Configuring users for branch site resiliency in Lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0db63-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0db63-115">See Also</span></span>


[<span data-ttu-id="0db63-116">Приложение A. Использование командлетов для развертывания устройств для обеспечения связи в филиалах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0db63-116">Appendix A: Using cmdlets to deploy a Survivable Branch Appliance in Lync Server 2013</span></span>](lync-server-2013-appendix-a-using-cmdlets-to-deploy-a-survivable-branch-appliance.md)  
  

<span data-ttu-id="0db63-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0db63-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

