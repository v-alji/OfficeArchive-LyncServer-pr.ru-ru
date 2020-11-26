---
title: Создание записи DNS SRV для интеграции с размещенной единой системой обмена сообщениями
description: Создание записи DNS SRV для интеграции с размещенной единой системой обмена сообщениями Exchange.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a DNS SRV record for integration with hosted Exchange UM
ms:assetid: 8ea590ae-58ea-4ca5-9853-e0708b3ea760
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh500728(v=OCS.15)
ms:contentKeyID: 48184770
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694a595977abe33bebbb5fbcf2a508c9bb4e35a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432235"
---
# <a name="create-a-dns-srv-record-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="fd68d-103">Создание записи DNS SRV для интеграции с размещенной единой системой обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="fd68d-103">Create a DNS SRV record for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd68d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd68d-104">

<span> </span></span></span>

<span data-ttu-id="fd68d-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="fd68d-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="fd68d-106">В этой статье описано, как настроить запись SRV службы доменных имен (DNS), необходимую для того, чтобы сервер Lync Server 2013 Edge направлялся на размещенную службу Exchange, например Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fd68d-106">This topic describes how to configure the Domain Name System (DNS) SRV record that is required for a Lync Server 2013 Edge Server to route to a hosted Exchange service such as Microsoft Exchange Online.</span></span>

<div>

## <a name="to-create-an-external-dns-srv-record-for-the-hosted-exchange-service"></a><span data-ttu-id="fd68d-107">Создание внешней записи SRV DNS для размещенной службы Exchange</span><span class="sxs-lookup"><span data-stu-id="fd68d-107">To create an external DNS SRV record for the hosted Exchange service</span></span>

1.  <span data-ttu-id="fd68d-108">Войдите на внешний DNS-сервер в качестве участника группы DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="fd68d-108">Log on to the external DNS server as a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="fd68d-109">Нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **DNS**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-109">Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="fd68d-110">В дереве консоли для вашего домена SIP разверните раздел **зоны прямого просмотра** и выберите домен SIP, в который будет установлен Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fd68d-110">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and select the SIP domain in which Lync Server 2013 will be installed.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="fd68d-111">Вы должны создать SRV-запись DNS в домене SIP, в котором установлен или будет устанавливаться сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd68d-111">You must create the DNS SRV record in the SIP domain in which Lync Server is or will be installed.</span></span> <span data-ttu-id="fd68d-112">Когда вы создаете SRV-запись, полное доменное имя, используемое узлом для этого поля службы, должно быть внешним доменным именем пограничного пула.</span><span class="sxs-lookup"><span data-stu-id="fd68d-112">When you create the SRV record, the FQDN used for the Host offering this service field must be the external FQDN of the Edge pool.</span></span> <span data-ttu-id="fd68d-113">Например, если внешнее полное доменное имя пограничного пула — edge01.contoso.net, введите это значение.</span><span class="sxs-lookup"><span data-stu-id="fd68d-113">For example, if the external FQDN of your Edge pool is edge01.contoso.net, enter that value.</span></span> <span data-ttu-id="fd68d-114">Этот элемент также должен находиться в том же домене, что и DNS-записи HOSTS (A).</span><span class="sxs-lookup"><span data-stu-id="fd68d-114">This must also be in the same domain as the DNS Hosts (A) record.</span></span>

    
    </div>

4.  <span data-ttu-id="fd68d-115">Щелкните выбранный домен правой кнопкой мыши и выберите пункт **другие новые записи**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-115">Right-click the selected domain, and then click **Other New Records**.</span></span>

5.  <span data-ttu-id="fd68d-116">В списке **тип записи ресурсов** выберите пункт **расположение службы (SRV)** и нажмите кнопку **создать запись**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-116">In **Resource Record Type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

6.  <span data-ttu-id="fd68d-117">В **новой записи ресурса** выберите пункт **Служба**, а затем введите **\_ sipfederationtls**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-117">In **New Resource Record**, click **Service**, and then type **\_sipfederationtls**.</span></span>

7.  <span data-ttu-id="fd68d-118">Выберите **протокол** и введите **\_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-118">Click **Protocol**, and then type **\_tcp**.</span></span>

8.  <span data-ttu-id="fd68d-119">Нажмите **Номер порта** и введите значение **5061**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-119">Click **Port Number**, and then type **5061**.</span></span>

9.  <span data-ttu-id="fd68d-120">Щелкните **узел, предлагающий эту службу**, и введите полное доменное имя (FQDN) пула lync Server 2013 EDGE, который предоставляет доступ к системе lync Server 2013 для доверенных внешних клиентов.</span><span class="sxs-lookup"><span data-stu-id="fd68d-120">Click **Host offering this service**, and then type the fully qualified domain name (FQDN) of the Lync Server 2013 Edge pool that provides access to your Lync Server 2013 system for trusted external clients.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="fd68d-121">Кроме того, домен необходимо настроить в качестве полномочного, обслуживаемого домена в параметрах Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fd68d-121">The domain must also be set up as an authoritative, accepted domain in your Exchange Online settings.</span></span> <span data-ttu-id="fd68d-122">Дополнительные сведения можно найти в разделе Создание обслуживаемых доменов по адресу <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A> .</span><span class="sxs-lookup"><span data-stu-id="fd68d-122">For details, see Create Accepted Domains at <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A>.</span></span>

    
    </div>

10. <span data-ttu-id="fd68d-123">Нажмите кнопку **ОК**, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-123">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-that-the-dns-srv-record-was-created-successfully"></a><span data-ttu-id="fd68d-124">Проверка успешности создания DNS SRV-записи</span><span class="sxs-lookup"><span data-stu-id="fd68d-124">To verify that the DNS SRV record was created successfully</span></span>

1.  <span data-ttu-id="fd68d-125">Войдите в домен на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="fd68d-125">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="fd68d-126">В меню **Пуск** выберите пункт **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="fd68d-126">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="fd68d-127">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fd68d-127">At the command prompt, run the following command:</span></span>
    
        nslookup <FQDN Lync Edge Pool>

4.  <span data-ttu-id="fd68d-128">Убедитесь в том, что вы получили ответ на соответствующий IP-адрес для полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="fd68d-128">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fd68d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fd68d-129">See Also</span></span>


[<span data-ttu-id="fd68d-130">Создание DNS-записей для обратных прокси-серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd68d-130">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)  
  

<span data-ttu-id="fd68d-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd68d-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

