---
title: 'Lync Server 2013: определение устройства или сервера для обеспечения связи в филиалах'
description: 'Lync Server 2013: определение бесперебойно работающего устройства филиала или сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a Survivable Branch Appliance or Server
ms:assetid: 1f49cfbe-30b3-4600-af15-47cb2f58d18a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398280(v=OCS.15)
ms:contentKeyID: 48183583
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 946aec82f33dffe268fefb3548b8db2f5c19e1a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431101"
---
# <a name="define-a-survivable-branch-appliance-or-server-in-lync-server-2013"></a><span data-ttu-id="97cd7-103">Определение устройства или сервера для обеспечения связи в филиалах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97cd7-103">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97cd7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97cd7-104">

<span> </span></span></span>

<span data-ttu-id="97cd7-105">_**Тема последнего изменения:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="97cd7-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="97cd7-106">Если вы не определили работающее устройство филиала или сервер при добавлении в топологию, выполните эту процедуру на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="97cd7-106">Perform this procedure at the central site if you did not define the Survivable Branch Appliance or Server when you added it to your topology.</span></span>

<div>

## <a name="to-define-a-survivable-branch-appliance-or-survivable-branch-server"></a><span data-ttu-id="97cd7-107">Определение бесперебойно работающего устройства филиала или работающего сервера подразделения</span><span class="sxs-lookup"><span data-stu-id="97cd7-107">To define a Survivable Branch Appliance or Survivable Branch Server</span></span>

1.  <span data-ttu-id="97cd7-108">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="97cd7-108">Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="97cd7-109">В дереве консоли разверните узел центрального сайта, разверните **узлы филиалов**, а затем разверните имя сайта ветви, на котором вы планируете развернуть работающее устройство филиала или его бесперебойный сервер.</span><span class="sxs-lookup"><span data-stu-id="97cd7-109">In the console tree, expand the central site, expand **Branch sites**, and then expand the name of the branch site where you plan to deploy the Survivable Branch Appliance or Survivable Branch Server.</span></span>

3.  <span data-ttu-id="97cd7-110">Щелкните правой кнопкой мыши **бесперебойно работающие филиалы**, а затем выберите команду создать работающее **устройство филиала**.</span><span class="sxs-lookup"><span data-stu-id="97cd7-110">Right-click **Survivable Branch Appliances**, and then click **New Survivable Branch Appliance**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="97cd7-111"><STRONG>Бесперебойно работающих филиалы</STRONG> — это область, в которой вы определяете бесперебойные серверы филиалов и бесперебойные устройства ветвления.</span><span class="sxs-lookup"><span data-stu-id="97cd7-111"><STRONG>Survivable Branch Appliances</STRONG> is where you define Survivable Branch Servers and Survivable Branch Appliances.</span></span>

    
    </div>

4.  <span data-ttu-id="97cd7-112">В диалоговом окне **Определение бесперебойной работы устройства филиала** выберите полное доменное имя **(FQDN)** для работающего устройства филиала или его бесперебойный сервер, который будет развертываться на этом сайте филиала, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="97cd7-112">In the **Define Survivable Branch Appliance** dialog box, click **FQDN**, type the fully qualified domain name (FQDN) of the Survivable Branch Appliance or Survivable Branch Server you will deploy at this branch site, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="97cd7-113">Если вы определяете бесперебойную подстановку, имя, которое вы ввели в <STRONG>полном доменном</STRONG> имени, должно совпадать с именем бесперебойного устройства, которое вы назначили атрибуту "пользовательское <STRONG>устройство".</STRONG></span><span class="sxs-lookup"><span data-stu-id="97cd7-113">If you are defining a Survivable Branch Appliance, the name you enter in <STRONG>FQDN</STRONG> must be the same as the Survivable Branch Appliance FQDN you assigned to the <STRONG>servicePrincipalName</STRONG> attribute.</span></span> <span data-ttu-id="97cd7-114">Дополнительные сведения можно найти <A href="lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md">в разделе Добавление работающего устройства филиала в Active Directory в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="97cd7-114">For details, see <A href="lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md">Add a Survivable Branch Appliance to Active Directory in Lync Server 2013</A>.</span></span>

    
    </div>

5.  <span data-ttu-id="97cd7-115">Щелкните элемент **пул переднего плана**, щелкните сервер переднего плана (пул служб пользователей) на центральном сайте, к которому можно подключиться, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="97cd7-115">Click **Front End pool**, click the Front End Server (User Services pool) at the central site that this Survivable Branch Appliance or Survivable Branch Server will connect to, and then click **Next**.</span></span>

6.  <span data-ttu-id="97cd7-116">Щелкните **граничный сервер**, выберите пул пограничного пула, который будет подключаться к сети, чтобы обеспечить подключение к ним для удаленных пользователей на сайте филиала, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="97cd7-116">Click **Edge Server**, click the Edge pool that this Survivable Branch Appliance or Survivable Branch Server will connect to provide PSTN connectivity to remote users of the branch site, and then click **Next**.</span></span>

7.  <span data-ttu-id="97cd7-117">Выберите **полное доменное имя или IP-адрес шлюза**, а затем введите полное доменное имя или IP-адрес узла шлюза, с которым может быть установлено подключение для входящей или исходящей маршрутизации по протоколу PSTN.</span><span class="sxs-lookup"><span data-stu-id="97cd7-117">Click **Gateway FQDN or IP Address**, and then type the FQDN or IP address of the gateway peer that the Survivable Branch Appliance or Survivable Branch Server is associated with for routing inbound or outbound PSTN calls.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="97cd7-118">Если вы определяете бесперебойно работающее устройство ветвления, это шлюз, на который сервер-посредник может находиться в работающем устройстве филиала, подключается к сети PSTN.</span><span class="sxs-lookup"><span data-stu-id="97cd7-118">If you are defining a Survivable Branch Appliance, this is the gateway to which the Mediation Server inside the Survivable Branch Appliance will connect for PSTN connectivity.</span></span>

    
    </div>

8.  <span data-ttu-id="97cd7-119">Выберите **прослушивающий порт для IP/КТСОП** и подтвердите порт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97cd7-119">Click **Listening Port for IP/PSTN Gateway**, and then accept the default port.</span></span>

9.  <span data-ttu-id="97cd7-120">В **транспортном протоколе SIP** выберите транспортный протокол, который будет использоваться для работающего устройства филиала или для работающего филиала, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="97cd7-120">In **Sip Transport Protocol**, click the transport protocol the Survivable Branch Appliance or Survivable Branch Server will use, and then click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="97cd7-121">По соображениям безопасности мы настоятельно рекомендуем использовать TLS-защиту.</span><span class="sxs-lookup"><span data-stu-id="97cd7-121">For security reasons, we strongly recommend that you use Transport Layer Security (TLS).</span></span> <span data-ttu-id="97cd7-122">Если вы определяете работающее устройство филиала, ознакомьтесь с соответствующей документацией поставщика филиала, чтобы убедиться в том, что устройство, поддерживающее бесперебойную ветвь, поддерживает протокол TLS.</span><span class="sxs-lookup"><span data-stu-id="97cd7-122">If you are defining a Survivable Branch Appliance, refer to your Survivable Branch Appliance vendor documentation to verify that your Survivable Branch Appliance supports the TLS protocol.</span></span>

    
    </div>

10. <span data-ttu-id="97cd7-123">В дереве консоли щелкните правой кнопкой мыши новое работающее устройство или сервер филиала, выберите пункт **топология** и нажмите кнопку **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="97cd7-123">In the console tree, right-click the new Survivable Branch Appliance or Server, click **Topology**, and then click **Publish**.</span></span>

<span data-ttu-id="97cd7-124">**Следующий этап**: [развертывание бесперебойно работающего устройства филиала или сервера с помощью Lync Server 2013 — задачи сайта ответвления](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)</span><span class="sxs-lookup"><span data-stu-id="97cd7-124">**Next step**: [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)</span></span>

<span data-ttu-id="97cd7-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97cd7-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

