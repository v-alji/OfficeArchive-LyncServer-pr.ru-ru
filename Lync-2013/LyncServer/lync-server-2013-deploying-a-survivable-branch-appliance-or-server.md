---
title: 'Lync Server 2013: развертывание устройства или сервера обеспечения связи в филиалах'
description: 'Lync Server 2013: развертывание бесперебойно работающего устройства или сервера филиалов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server
ms:assetid: cb780c14-dc5f-41ba-8092-f20ae905bd16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398849(v=OCS.15)
ms:contentKeyID: 48185643
ms.date: 12/11/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8c8610ab85b61d33a5f181f1d5f51d0e5095f49
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430121"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013"></a><span data-ttu-id="2afcf-103">Развертывание устройства или сервера обеспечения связи в филиалах с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2afcf-103">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2afcf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2afcf-104">

<span> </span></span></span>

<span data-ttu-id="2afcf-105">_**Тема последнего изменения:** 2014-12-10_</span><span class="sxs-lookup"><span data-stu-id="2afcf-105">_**Topic Last Modified:** 2014-12-10_</span></span>

<span data-ttu-id="2afcf-106">Отказоустойчивая Корпоративная голосовая связь — это возможность предоставления постоянной корпоративной голосовой связи пользователям сайтов филиалов в случае, если ссылка на центральный сайт станет недоступна.</span><span class="sxs-lookup"><span data-stu-id="2afcf-106">Resilient Enterprise Voice refers to branch-site resiliency, that is, the ability to provide continuous Enterprise Voice service to branch site users in the event that the link to the central site becomes unavailable.</span></span>

<span data-ttu-id="2afcf-107">Для небольших и средних сайтов филиалов (сайтов филиалов с 25 до 1 000 пользователей) рекомендуется развертывание работающего устройства филиалов, которое будет прерывать вызовы по коммутируемой телефонной сети (PSTN), используя встроенный шлюз PSTN или магистральный канал SIP для поставщика услуг телефонной связи.</span><span class="sxs-lookup"><span data-stu-id="2afcf-107">For small and medium-sized branch sites (branch sites with 25 to 1,000 users), we recommend deploying a Survivable Branch Appliance, which will terminate public switched telephone network (PSTN) calls by using its built-in PSTN gateway or a SIP trunk to a telephone service provider.</span></span> <span data-ttu-id="2afcf-108">Бесперебойно работающее приложение-ветвь — это стороннее устройство, включающее в себя сервер с операционной системой Windows Server 2008 R2, регистратор Lync Server 2013, программное обеспечение сервера-посредников и шлюз PSTN в одном корпусе устройства.</span><span class="sxs-lookup"><span data-stu-id="2afcf-108">A Survivable Branch Appliance is a third-party device that includes a blade server running the Windows Server 2008 R2 operating system, Lync Server 2013 Registrar, Mediation Server software, and a PSTN gateway, all in a single appliance chassis.</span></span>

<span data-ttu-id="2afcf-109">Для сайтов филиалов с 1 000 до 5 000 и без гибкой глобальной сети рекомендуется подключить одноадресный сервер к поставщику услуг телефонной связи либо к шлюзу PSTN, либо к магистрали SIP.</span><span class="sxs-lookup"><span data-stu-id="2afcf-109">For branch sites with 1,000 to 5,000 users and no resilient WAN, we recommend a Survivable Branch Server connected to either a PSTN gateway or a SIP trunk to a telephone service provider.</span></span> <span data-ttu-id="2afcf-110">Бесперебойный сервер подразделения — это компьютер под управлением Windows, на котором установлено программное обеспечение регистратора и сервер-посредника.</span><span class="sxs-lookup"><span data-stu-id="2afcf-110">A Survivable Branch Server is a Windows Server-based computer that has Registrar and Mediation Server software installed on it.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2afcf-111">Для сайтов филиалов, в которых более 5 000 пользователей и выделенные администраторы сервера Lync Server, рекомендуется использовать полное развертывание Lync Server 2013, отделенное от центрального сайта.</span><span class="sxs-lookup"><span data-stu-id="2afcf-111">For branch sites with more than 5,000 users and dedicated Lync Server administrators, we recommend a full Lync Server 2013 deployment, separate from that of the central site.</span></span><BR><span data-ttu-id="2afcf-112">Подробные сведения о выборе наилучшего решения для обеспечения устойчивости для сайтов филиалов в Организации, в том числе о предварительных требованиях и планировании, приведены в разделе <A href="lync-server-2013-branch-site-resiliency-requirements.md">требования к устойчивости сайтов для Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="2afcf-112">For details about choosing the best resiliency solution for the branch sites in your organization, including prerequisites and planning considerations, see <A href="lync-server-2013-branch-site-resiliency-requirements.md">Branch-site resiliency requirements for Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="2afcf-113">Пользователи, расположенные на устройстве с бесперебойной подразделением Lync Server, не могут создавать новые комнаты чата и просматривать открытку для существующих комнат.</span><span class="sxs-lookup"><span data-stu-id="2afcf-113">Users who are homed on a Lync Server Survivable Branch Appliance are unable to create new chat rooms or view the room card for existing rooms.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2afcf-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="2afcf-114">In This Section</span></span>

  - [<span data-ttu-id="2afcf-115">Развертывание устройства или сервера для обеспечения связи в филиалах с помощью Lync Server 2013 — задачи центрального сайта</span><span class="sxs-lookup"><span data-stu-id="2afcf-115">Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks</span></span>](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md)

  - [<span data-ttu-id="2afcf-116">Развертывание устройства или сервера для обеспечения связи в филиалах с помощью Lync Server 2013 — задача сайта филиала</span><span class="sxs-lookup"><span data-stu-id="2afcf-116">Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task</span></span>](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)

  - [<span data-ttu-id="2afcf-117">Настройка пользователей для организации устойчивости на сайтах филиалов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2afcf-117">Configuring users for branch site resiliency in Lync Server 2013</span></span>](lync-server-2013-configuring-users-for-branch-site-resiliency.md)

  - [<span data-ttu-id="2afcf-118">Пользователи, работающие дома на устройстве или сервере для обеспечения связи в филиалах, в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2afcf-118">Home users on a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md)

  - [<span data-ttu-id="2afcf-119">Приложения: устройства и серверы для обеспечения связи в филиалах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2afcf-119">Appendices: Survivable Branch Appliances and Servers in Lync Server 2013</span></span>](lync-server-2013-appendices-survivable-branch-appliances-and-servers.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2afcf-120">См. также</span><span class="sxs-lookup"><span data-stu-id="2afcf-120">See Also</span></span>


[<span data-ttu-id="2afcf-121">Развертывание Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2afcf-121">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="2afcf-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2afcf-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

