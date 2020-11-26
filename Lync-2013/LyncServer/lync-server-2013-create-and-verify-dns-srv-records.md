---
title: 'Lync Server 2013: создание и проверка записей DNS SRV'
description: 'Lync Server 2013: создание и проверка DNS SRV-записей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create and verify DNS SRV records
ms:assetid: 86888c7e-1401-458f-9a7b-08ac726deeec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398680(v=OCS.15)
ms:contentKeyID: 48184714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a71c876d0b26b9305feed7146fa6321a3983588d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432018"
---
# <a name="create-and-verify-dns-srv-records-in-lync-server-2013"></a><span data-ttu-id="09779-103">Создание и проверка записей DNS SRV в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09779-103">Create and verify DNS SRV records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09779-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09779-104">

<span> </span></span></span>

<span data-ttu-id="09779-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="09779-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="09779-106">Для успешного выполнения этой процедуры необходимо войти в систему на сервере или в домене в группу администраторов домена или в группу пользователей DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="09779-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="09779-107">В этой статье описано, как настроить записи DNS, необходимые для автоматического входа в Lync Server 2013, и те, которые необходимы для автоматической регистрации клиента.</span><span class="sxs-lookup"><span data-stu-id="09779-107">This topic describes how to configure the Domain Name System (DNS) records that you are required to create in Lync Server 2013 deployments and those required for automatic client sign in.</span></span> <span data-ttu-id="09779-108">При создании пула переднего плана программа установки создает объекты Active Directory и параметры для пула, включая полное доменное имя пула (FQDN).</span><span class="sxs-lookup"><span data-stu-id="09779-108">When you create a Front End pool, Setup creates Active Directory objects and settings for the pool, including the pool fully qualified domain name (FQDN).</span></span> <span data-ttu-id="09779-109">Аналогичные объекты и параметры создаются для сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="09779-109">Similar objects and settings are created for a Standard Edition server.</span></span> <span data-ttu-id="09779-110">Чтобы клиенты смогли подключиться к серверу пула или стандарту Standard Edition, в DNS должны быть зарегистрированы полные доменные имена для пула или сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="09779-110">For clients to be able to connect to the pool or Standard Edition server, the FQDN of the pool or Standard Edition server must be registered in DNS.</span></span> <span data-ttu-id="09779-111">Вы должны создать записи DNS SRV во внутренней DNS для каждого домена SIP.</span><span class="sxs-lookup"><span data-stu-id="09779-111">You must create DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="09779-112">В этой процедуре предполагается, что в вашей внутренней DNS-зоне есть зоны для доменов пользователей SIP.</span><span class="sxs-lookup"><span data-stu-id="09779-112">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<div>

## <a name="to-configure-a-dns-srv-record"></a><span data-ttu-id="09779-113">Настройка DNS-записи SRV</span><span class="sxs-lookup"><span data-stu-id="09779-113">To configure a DNS SRV record</span></span>

1.  <span data-ttu-id="09779-114">На DNS-сервере нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **DNS**.</span><span class="sxs-lookup"><span data-stu-id="09779-114">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="09779-115">В дереве консоли для вашего домена SIP разверните раздел **зоны прямого просмотра**, а затем щелкните правой кнопкой мыши домен SIP, в котором будет установлен Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="09779-115">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and then right-click the SIP domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="09779-116">Нажмите кнопку **другие новые записи**.</span><span class="sxs-lookup"><span data-stu-id="09779-116">Click **Other New Records**.</span></span>

4.  <span data-ttu-id="09779-117">В разделе **Выбор типа записи ресурса** выберите **Обнаружение службы (запись SRV)**, а затем нажмите кнопку **Создать запись**.</span><span class="sxs-lookup"><span data-stu-id="09779-117">In **Select a resource record type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

5.  <span data-ttu-id="09779-118">Выберите пункт **Служба**, а затем введите **\_ sipinternaltls**.</span><span class="sxs-lookup"><span data-stu-id="09779-118">Click **Service**, and then type **\_sipinternaltls**.</span></span>

6.  <span data-ttu-id="09779-119">Выберите **протокол** и введите **\_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="09779-119">Click **Protocol**, and then type **\_tcp**.</span></span>

7.  <span data-ttu-id="09779-120">Нажмите **Номер порта** и введите значение **5061**.</span><span class="sxs-lookup"><span data-stu-id="09779-120">Click **Port Number**, and then type **5061**.</span></span>

8.  <span data-ttu-id="09779-121">Нажмите **Узел этой службы** и введите полное доменное имя пула или сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="09779-121">Click **Host offering this service**, and then type the FQDN of the pool or Standard Edition server.</span></span>

9.  <span data-ttu-id="09779-122">Нажмите кнопку **ОК**, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="09779-122">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-the-creation-of-a-dns-srv-record"></a><span data-ttu-id="09779-123">Проверка создания DNS-записи SRV</span><span class="sxs-lookup"><span data-stu-id="09779-123">To verify the creation of a DNS SRV record</span></span>

1.  <span data-ttu-id="09779-124">Выполните вход на клиентский компьютер с использованием учетной записи, которая является членом группы прошедших проверку пользователей или имеет эквивалентные разрешения.</span><span class="sxs-lookup"><span data-stu-id="09779-124">Log on to a client computer in the domain with an account that is a member of the Authenticated Users group or has equivalent permissions.</span></span>

2.  <span data-ttu-id="09779-125">В меню **Пуск** выберите пункт **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="09779-125">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="09779-126">В поле **Открыть** введите **cmd** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="09779-126">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="09779-127">В командной строке введите **nslookup** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="09779-127">At the command prompt, type **nslookup**, and then press ENTER.</span></span>

5.  <span data-ttu-id="09779-128">Введите **Set Type = SRV** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="09779-128">Type **set type=srv**, and then press ENTER.</span></span>

6.  <span data-ttu-id="09779-129">Введите **\_ sipinternaltls. \_ tcp.contoso.com**, а затем нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="09779-129">Type **\_sipinternaltls.\_tcp.contoso.com**, and then press ENTER.</span></span> <span data-ttu-id="09779-130">Ниже указаны выходные данные, отображаемые для записи протокола TLS.</span><span class="sxs-lookup"><span data-stu-id="09779-130">The output displayed for the Transport Layer Security (TLS) record is as follows:</span></span>
    
    <span data-ttu-id="09779-131">Server: \<dns server\> . contoso.com</span><span class="sxs-lookup"><span data-stu-id="09779-131">Server: \<dns server\>.contoso.com</span></span>
    
    <span data-ttu-id="09779-132">Адресаци \<IP address of DNS server\></span><span class="sxs-lookup"><span data-stu-id="09779-132">Address: \<IP address of DNS server\></span></span>
    
    <span data-ttu-id="09779-133">Неофициальный ответ:</span><span class="sxs-lookup"><span data-stu-id="09779-133">Non-authoritative answer:</span></span>
    
    <span data-ttu-id="09779-134">\_sipinternaltls. \_ расположение службы tcp.contoso.com SRV:</span><span class="sxs-lookup"><span data-stu-id="09779-134">\_sipinternaltls.\_tcp.contoso.com SRV service location:</span></span>
    
    <span data-ttu-id="09779-135">Priority (приоритет) = 0</span><span class="sxs-lookup"><span data-stu-id="09779-135">priority = 0</span></span>
    
    <span data-ttu-id="09779-136">Вес = 0</span><span class="sxs-lookup"><span data-stu-id="09779-136">weight = 0</span></span>
    
    <span data-ttu-id="09779-137">порт = 5061</span><span class="sxs-lookup"><span data-stu-id="09779-137">port = 5061</span></span>
    
    <span data-ttu-id="09779-138">SVR hostname = poolname.contoso.com (или стандартный сервер выпуска A Record)</span><span class="sxs-lookup"><span data-stu-id="09779-138">svr hostname = poolname.contoso.com (or Standard Edition server A record)</span></span>
    
    <span data-ttu-id="09779-139">Интернет-адрес poolname.contoso.com = \<virtual IP Address of the load balancer\> или \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\>\<IP address of the Standard Edition server\></span><span class="sxs-lookup"><span data-stu-id="09779-139">poolname.contoso.com internet address = \<virtual IP Address of the load balancer\> or \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> or \<IP address of the Standard Edition server\></span></span>

7.  <span data-ttu-id="09779-140">Когда все будет готово, в командной строке введите **Exit** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="09779-140">When you are finished, at the command prompt, type **exit**, and then press ENTER.</span></span>

</div>

<div>

## <a name="to-verify-that-the-fqdn-of-the-front-end-pool-or-standard-edition-server-can-be-resolved"></a><span data-ttu-id="09779-141">Проверка возможности разрешения полных доменных имен в пуле или сервере Standard Edition</span><span class="sxs-lookup"><span data-stu-id="09779-141">To verify that the FQDN of the Front End pool or Standard Edition server can be resolved</span></span>

1.  <span data-ttu-id="09779-142">Войдите в домен на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="09779-142">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="09779-143">В меню **Пуск** выберите пункт **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="09779-143">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="09779-144">В поле **Открыть** введите **cmd** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="09779-144">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="09779-145">В командной строке введите **nslookup** \<FQDN of the Front End pool\> или и нажмите \<FQDN of the Standard Edition server\> клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="09779-145">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="09779-146">Убедитесь в том, что вы получили ответ на соответствующий IP-адрес для полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="09779-146">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="09779-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09779-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

