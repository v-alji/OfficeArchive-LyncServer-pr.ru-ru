---
title: 'Lync Server 2013: настройка DNS для балансировки нагрузки'
description: 'Lync Server 2013: Настройка DNS для балансировки нагрузки.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS for load balancing
ms:assetid: 1b2e8414-8676-4872-8ecf-ea07196f74de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398251(v=OCS.15)
ms:contentKeyID: 48183540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b13db22d65ee67723ebc0a31544137d467d5c6b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399895"
---
# <a name="configure-dns-for-load-balancing-in-lync-server-2013"></a><span data-ttu-id="5b16c-103">Настройка DNS для балансировки нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b16c-103">Configure DNS for load balancing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b16c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b16c-104">

<span> </span></span></span>

<span data-ttu-id="5b16c-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="5b16c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="5b16c-106">Для успешного выполнения этой процедуры необходимо войти в систему на сервере или в домене в группу администраторов домена или в группу пользователей DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="5b16c-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="5b16c-107">Балансировка нагрузки службы доменных имен (DNS) обеспечивает баланс сетевого трафика, уникального для Lync Server 2013, например трафик SIP и трафик мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5b16c-107">Domain Name System (DNS) Load Balancing balances the network traffic that is unique to Lync Server 2013, such as SIP traffic and media traffic.</span></span> <span data-ttu-id="5b16c-108">Балансировка нагрузки DNS поддерживается для пулов интерфейсов, пулов пограничных каталогов, пулов и изолированных пулов исправлений.</span><span class="sxs-lookup"><span data-stu-id="5b16c-108">DNS load balancing is supported for Front End pools, Edge pools, Director pools, and stand-alone Mediation pools.</span></span> <span data-ttu-id="5b16c-109">Для пула, настроенного для использования балансировки нагрузки DNS, должны быть заданы два полных доменных имени (FQDN): обычное полное доменное имя пула, используемое службой балансировки нагрузки DNS (например, pool1.contoso.com), и которое разрешается в физические IP-адреса серверов в пуле, и другое полное доменное имя (например, web1.contoso.net), которое разрешается в виртуальный IP-адрес пула.</span><span class="sxs-lookup"><span data-stu-id="5b16c-109">A pool that is configured to use DNS load balancing must have two fully qualified domain names (FQDNs) defined: the regular pool FQDN that is used by DNS load balancing (for example, pool1.contoso.com) and that resolves to the physical IPs of the servers in the pool, and another FQDN for the pool’s Web Services (for example, web1.contoso.net), which resolves to the virtual IP address of the pool.</span></span> <span data-ttu-id="5b16c-110">Подробные сведения о балансировке нагрузки DNS можно найти [в разделе Балансировка нагрузки DNS в Lync Server 2013](lync-server-2013-dns-load-balancing.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="5b16c-110">For details about DNS Load Balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5b16c-111">Балансировка нагрузки оборудования по-прежнему требуется для трафика HTTPS на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="5b16c-111">Hardware load balancing is still required for client to server HTTPS traffic.</span></span>



</div>

<span data-ttu-id="5b16c-112">Для использования балансировки нагрузки DNS необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5b16c-112">Before you can use DNS load balancing, you must do the following:</span></span>

1.  <span data-ttu-id="5b16c-113">Переопределение полного доменного имени пула внутренних веб-служб.</span><span class="sxs-lookup"><span data-stu-id="5b16c-113">Override the internal Web Services pool FQDN.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="5b16c-114">Если вы решите переопределить внутренние веб-службы с помощью самоопределенного полного доменного имени, каждое полное доменное имя должно быть уникальным из любого другого пула переднего плана, режиссера или директора пула.</span><span class="sxs-lookup"><span data-stu-id="5b16c-114">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

2.  <span data-ttu-id="5b16c-115">Создайте DNS A Records hosts, чтобы разрешить полное доменное имя пула с IP-адресами всех серверов в пуле.</span><span class="sxs-lookup"><span data-stu-id="5b16c-115">Create DNS A host records to resolve the pool FQDN to the IP addresses of all the servers in the pool.</span></span>

3.  <span data-ttu-id="5b16c-116">Включение случайного выбора IP-адреса или для DNS-сервера Windows Server включите циклическое управление.</span><span class="sxs-lookup"><span data-stu-id="5b16c-116">Enable IP Address randomization or, for Windows Server DNS, enable round robin.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5b16c-117">По умолчанию будет включена функция "циклический перебор".</span><span class="sxs-lookup"><span data-stu-id="5b16c-117">Round robin should be enabled by default.</span></span>

    
    </div>

<div>

## <a name="to-override-internal-web-services-fqdn"></a><span data-ttu-id="5b16c-118">Чтобы переопределить полное доменное имя внутренней веб-службы</span><span class="sxs-lookup"><span data-stu-id="5b16c-118">To override internal Web services FQDN</span></span>

1.  <span data-ttu-id="5b16c-119">Запустить построитель топологии: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-119">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="5b16c-120">В дереве консоли разверните узел Пулы переднего плана Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="5b16c-120">From the console tree, expand the Enterprise Edition Front End pools node.</span></span>

3.  <span data-ttu-id="5b16c-121">Щелкните пул правой кнопкой мыши, выберите команду **изменить свойства**, а затем — **веб-службы**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-121">Right-click the pool, click **Edit Properties**, and then click **Web Services**.</span></span>

4.  <span data-ttu-id="5b16c-122">В разделе **внутренние веб-службы** установите флажок **Переопределение полного доменного имени** .</span><span class="sxs-lookup"><span data-stu-id="5b16c-122">Below **Internal web services**, select the **Override FQDN** check box.</span></span>

5.  <span data-ttu-id="5b16c-123">Введите полное доменное имя пула, которое разрешается в физические IP-адреса серверов в пуле.</span><span class="sxs-lookup"><span data-stu-id="5b16c-123">Type the pool FQDN that resolves to the physical IP addresses of the servers in the pool.</span></span>

6.  <span data-ttu-id="5b16c-124">Под **внешними веб-службами** введите полное доменное имя внешнего пула, которое разрешается в виртуальные IP-адреса пула, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-124">Below **External web services**, type the external pool FQDN that resolves to the virtual IP addresses of the pool, and then click **OK**.</span></span>

7.  <span data-ttu-id="5b16c-125">В дереве консоли щелкните **Lync Server 2013**, а затем в области **действия** выберите пункт **топология публикации**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-125">From the console tree, click **Lync Server 2013**, and then in the **Actions** pane, click **Publish Topology**.</span></span>

</div>

<div>

## <a name="to-create-dns-host-a-records-for-all-internal-pool-servers"></a><span data-ttu-id="5b16c-126">Создание записей DNS Host (A) для всех внутренних серверов пула</span><span class="sxs-lookup"><span data-stu-id="5b16c-126">To create DNS Host (A) Records for all internal pool servers</span></span>

1.  <span data-ttu-id="5b16c-127">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Администрирование** и **DNS**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-127">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="5b16c-128">В **диспетчере DNS** выберите DNS-сервер для управления записями, чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="5b16c-128">In **DNS Manager**, click the DNS Server that manages your records to expand it.</span></span>

3.  <span data-ttu-id="5b16c-129">Нажмите кнопку **зоны прямого просмотра** , чтобы развернуть ее.</span><span class="sxs-lookup"><span data-stu-id="5b16c-129">Click **Forward Lookup Zones** to expand it.</span></span>

4.  <span data-ttu-id="5b16c-130">Щелкните правой кнопкой мыши домен DNS, в который нужно добавить записи, и выберите команду **создать узел (A или AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-130">Right-click the DNS domain that you need to add records to, and then click **New Host (A or AAAA)**.</span></span>

5.  <span data-ttu-id="5b16c-131">В поле **Имя** введите имя записи узла (имя домена добавляется автоматически).</span><span class="sxs-lookup"><span data-stu-id="5b16c-131">In the **Name** box, type the name of the host record (the domain name will be automatically appended).</span></span>

6.  <span data-ttu-id="5b16c-132">В поле IP-адрес введите IP-адрес отдельного сервера переднего плана, а затем выберите команду **создать соответствующую запись указателя (PTR)** или **разрешите пользователям, прошедшим проверку подлинности, обновлять записи DNS с тем же именем владельца**, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="5b16c-132">In the IP Address box, type the IP address of the individual Front End Server and then select **Create associated pointer (PTR) record** or **Allow any authenticated user to update DNS records with the same owner name**, if applicable.</span></span>

7.  <span data-ttu-id="5b16c-133">Продолжайте создавать записи для всех серверов-интерфейсов участников, которые будут принимать участие в балансировке нагрузки DNS.</span><span class="sxs-lookup"><span data-stu-id="5b16c-133">Continue creating records for all member Front End Servers that will participate in DNS Load Balancing.</span></span>
    
    <span data-ttu-id="5b16c-134">Например, если у вас есть пул с именем pool1.contoso.com и тремя серверами переднего плана, вы создадите следующие записи DNS:</span><span class="sxs-lookup"><span data-stu-id="5b16c-134">For example, if you had a pool named pool1.contoso.com and three Front End Servers, you would create the following DNS entries:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="5b16c-135">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="5b16c-135">FQDN</span></span></th>
    <th><span data-ttu-id="5b16c-136">Тип</span><span class="sxs-lookup"><span data-stu-id="5b16c-136">Type</span></span></th>
    <th><span data-ttu-id="5b16c-137">Данные</span><span class="sxs-lookup"><span data-stu-id="5b16c-137">Data</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="5b16c-138">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5b16c-138">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="5b16c-139">Узел (A)</span><span class="sxs-lookup"><span data-stu-id="5b16c-139">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="5b16c-140">192.168.1.1</span><span class="sxs-lookup"><span data-stu-id="5b16c-140">192.168.1.1</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="5b16c-141">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5b16c-141">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="5b16c-142">Узел (A)</span><span class="sxs-lookup"><span data-stu-id="5b16c-142">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="5b16c-143">192.168.1.2</span><span class="sxs-lookup"><span data-stu-id="5b16c-143">192.168.1.2</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="5b16c-144">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5b16c-144">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="5b16c-145">Узел (A)</span><span class="sxs-lookup"><span data-stu-id="5b16c-145">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="5b16c-146">192.168.1.3</span><span class="sxs-lookup"><span data-stu-id="5b16c-146">192.168.1.3</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="5b16c-147">Дополнительные сведения о создании записей DNS Hosting (A) можно найти в разделе [Настройка записей узлов DNS для Lync Server 2013](lync-server-2013-configure-dns-host-records.md).</span><span class="sxs-lookup"><span data-stu-id="5b16c-147">For details about creating DNS Host (A) records, see [Configure DNS Host records for Lync Server 2013](lync-server-2013-configure-dns-host-records.md).</span></span>

</div>

<div>

## <a name="to-enable-round-robin-for-windows-server"></a><span data-ttu-id="5b16c-148">Включение циклического переобслуживанием для Windows Server</span><span class="sxs-lookup"><span data-stu-id="5b16c-148">To enable round robin for Windows Server</span></span>

1.  <span data-ttu-id="5b16c-149">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Администрирование** и **DNS**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-149">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="5b16c-150">Разверните узел **DNS**, щелкните правой кнопкой мыши DNS-сервер, который вы хотите настроить, и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-150">Expand **DNS**, right-click the DNS server you want to configure, and then click **Properties**.</span></span>

3.  <span data-ttu-id="5b16c-151">На вкладке **Дополнительно** установите флажок **включить циклический перебор** и **включите** расстановку по сети, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b16c-151">Click the **Advanced** tab, select **Enable round robin** and **Enable netmask ordering**, and then click **OK**.</span></span>
    
    <span data-ttu-id="5b16c-152">![Диалоговое окно "циклический перебор DNS"](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg "Диалоговое окно "циклический перебор DNS"")</span><span class="sxs-lookup"><span data-stu-id="5b16c-152">![DNS Round Robin dialog box](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg "DNS Round Robin dialog box")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5b16c-153">Эта функция должна быть включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b16c-153">This feature should be enabled by default.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5b16c-154">См. также</span><span class="sxs-lookup"><span data-stu-id="5b16c-154">See Also</span></span>


[<span data-ttu-id="5b16c-155">Балансировка нагрузки DNS в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b16c-155">DNS load balancing in Lync Server 2013</span></span>](lync-server-2013-dns-load-balancing.md)  
  

<span data-ttu-id="5b16c-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b16c-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

