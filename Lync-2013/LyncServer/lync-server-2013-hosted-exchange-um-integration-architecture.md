---
title: 'Lync Server 2013: архитектура интеграции размещенной единой системы обмена сообщениями Exchange'
description: 'Lync Server 2013: размещена интегрированная архитектура UM Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange UM integration architecture
ms:assetid: 0094d5dc-1836-441c-b6e2-f88e35203a8d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398067(v=OCS.15)
ms:contentKeyID: 48183222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2399fa421b59a5ea1fd83b1a86225fc12de1f2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427609"
---
# <a name="hosted-exchange-um-integration-architecture-in-lync-server-2013"></a><span data-ttu-id="968c6-103">Архитектура интеграции размещенной единой системы обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="968c6-103">Hosted Exchange UM integration architecture in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="968c6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="968c6-104">

<span> </span></span></span>

<span data-ttu-id="968c6-105">_**Тема последнего изменения:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="968c6-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="968c6-106">Приложение Lync Server 2013 ExUM поддерживает интеграцию с развертыванием в локальной системе обмена сообщениями Exchange (UM), используя службу обмена СООБЩЕНИЯми Exchange, размещенную поставщиком услуг, или сочетанием этих двух возможностей.</span><span class="sxs-lookup"><span data-stu-id="968c6-106">The Lync Server 2013 ExUM Routing application supports integration with an on-premises Exchange Unified Messaging (UM) deployment, with Exchange UM hosted by a service provider, or with a combination of the two.</span></span> <span data-ttu-id="968c6-107">На следующей схеме показаны все три возможности.</span><span class="sxs-lookup"><span data-stu-id="968c6-107">The following diagram shows all three possibilities.</span></span>

<span data-ttu-id="968c6-108">**Интеграция с локальным развертыванием единой системы обмена сообщениями Exchange и двумя поставщиками размещенных служб Exchange**</span><span class="sxs-lookup"><span data-stu-id="968c6-108">**Integration with an on-premises Exchange UM deployment and two hosted Exchange providers**</span></span>

<span data-ttu-id="968c6-109">![Развертывание локальной системы обмена сообщениями на сервере Lync Server](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "Развертывание локальной системы обмена сообщениями на сервере Lync Server")</span><span class="sxs-lookup"><span data-stu-id="968c6-109">![On-premises Lync Server Exchange UM Deployment](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "On-premises Lync Server Exchange UM Deployment")</span></span>

<span data-ttu-id="968c6-110">Поддерживаются перечисленные ниже режимы.</span><span class="sxs-lookup"><span data-stu-id="968c6-110">The following modes are supported:</span></span>

  - <span data-ttu-id="968c6-111">**Локальное развертывание:** Lync Server 2013 и Exchange разворачиваются на локальных серверах в рамках предприятия.</span><span class="sxs-lookup"><span data-stu-id="968c6-111">**On-premises deployment:** Lync Server 2013 and Exchange UM are both deployed on local servers within your enterprise.</span></span>

  - <span data-ttu-id="968c6-112">**Развертывание между локальными** средами: Lync Server 2013 развертывается на локальных серверах организации, а UM-служба Exchange размещается в средстве поставщика Интернет-услуг, например в центре обработки данных Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="968c6-112">**Cross-premises deployment:** Lync Server 2013 is deployed on local servers within your enterprise and Exchange UM is hosted in an online service provider’s facility, such as a Microsoft Exchange Online data center.</span></span>

  - <span data-ttu-id="968c6-113">**Смешанное развертывание:** В составе сервера Lync Server 2013 есть некоторые почтовые ящики пользователей, расположенные на локальных серверах Exchange, и некоторые почтовые ящики, расположенные в центре обработки данных служб Exchange.</span><span class="sxs-lookup"><span data-stu-id="968c6-113">**Mixed deployment:** Your Lync Server 2013 deployment has some user mailboxes homed on local Exchange servers within your enterprise and some mailboxes homed in a hosted Exchange service data center.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="968c6-114">Смешанное развертывание может использоваться в качестве переходного решения во время оценки и поэтапной миграции пользователей на размещенную UM-среду Exchange или постоянное решение, если вы не хотите, чтобы некоторые пользователи работали в локальной среде обмена СООБЩЕНИЯми, после того как вы перенесите другие.</span><span class="sxs-lookup"><span data-stu-id="968c6-114">The mixed deployment can be used as a transitional solution during evaluation and phased migration of users to hosted Exchange UM, or a permanent solution if you opt to keep some users’ Exchange UM services on-premises after transferring others.</span></span>

    
    </div>

<div>

## <a name="shared-sip-address-space"></a><span data-ttu-id="968c6-115">Общее адресное пространство SIP</span><span class="sxs-lookup"><span data-stu-id="968c6-115">Shared SIP Address Space</span></span>

<span data-ttu-id="968c6-116">Чтобы интегрировать Lync Server 2013 с локальной развертыванием UM, вы предоставляете разрешение Lync Server 2013 для чтения объектов доменных служб Active Directory в Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="968c6-116">To integrate Lync Server 2013 with an on-premises Exchange UM deployment, you grant Lync Server 2013 permission to read Exchange UM Active Directory Domain Services objects.</span></span> <span data-ttu-id="968c6-117">Тем не менее, этот подход не работает для интеграции с размещенной единой системой обмена сообщениями Exchange, поскольку Lync Server 2013 и Exchange UM установлены в разных лесах, не имеющих доверительных отношений между ними.</span><span class="sxs-lookup"><span data-stu-id="968c6-117">This approach does not work for integration with hosted Exchange UM, however, because Lync Server 2013 and Exchange UM are installed in separate forests with no trust between them.</span></span>

<span data-ttu-id="968c6-118">Чтобы интегрировать Lync Server 2013 с размещенной единой системой обмена сообщениями Exchange, необходимо настроить *Общее адресное пространство SIP*.</span><span class="sxs-lookup"><span data-stu-id="968c6-118">To integrate Lync Server 2013 with hosted Exchange UM, you must configure a *shared SIP address space*.</span></span> <span data-ttu-id="968c6-119">В этой конфигурации одно и то же адресное пространство домена SIP доступно как для Lync Server 2013, так и для размещенного поставщика служб единой системы обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="968c6-119">In this configuration, the same SIP domain address space is available to both Lync Server 2013 and the hosted Exchange UM service provider.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="968c6-120">Использование общедоступного адресного пространства SIP сходно с подходом, используемым в гибридной среде Lync Server 2013, в которой некоторые пользователи находятся в локальном развертывании, а некоторые — в размещенном развертывании (например, Lync Online).</span><span class="sxs-lookup"><span data-stu-id="968c6-120">Use of the shared SIP address space is similar to the approach used in a cross-premises Lync Server 2013 environment, in which some users are homed in the on-premises deployment and some are homed in a hosted deployment (such as Lync Online).</span></span> <span data-ttu-id="968c6-121">Домен SIP делится между собой.</span><span class="sxs-lookup"><span data-stu-id="968c6-121">The SIP domain is split between them.</span></span> <span data-ttu-id="968c6-122">При интеграции Lync Server 2013 с размещенной UM-службой Exchange убедитесь в том, что в общее адресное пространство SIP включается поставщик служб Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="968c6-122">When you integrate Lync Server 2013 with hosted Exchange UM, ensure that you include the Exchange UM service provider in the shared SIP address space.</span></span>



</div>

<span data-ttu-id="968c6-123">Чтобы настроить общее адресное пространство SIP для интеграции с поставщиком служб Exchange UM, необходимо настроить пограничный сервер следующим образом:</span><span class="sxs-lookup"><span data-stu-id="968c6-123">To configure the shared SIP address space for integrating with an Exchange UM service provider, you need to configure your Edge Server as follows:</span></span>

1.  <span data-ttu-id="968c6-124">Настройте пограничный сервер для Федерации, запустив командлет **Set-CsAccessEdgeConfiguration** , чтобы задать указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="968c6-124">Configure the Edge Server for federation by running the **Set-CsAccessEdgeConfiguration** cmdlet to set the following parameters:</span></span>
    
      - <span data-ttu-id="968c6-125">**UseDnsSrvRouting** указывает, что пограничные серверы будут основываться на записях DNS SRV при отправке и получении запросов федерации.</span><span class="sxs-lookup"><span data-stu-id="968c6-125">**UseDnsSrvRouting** specifies that Edge Servers will rely on DNS SRV records when sending and receiving federation requests.</span></span>
    
      - <span data-ttu-id="968c6-p105">**AllowFederatedUsers** указывает, разрешено ли внутренним пользователям взаимодействовать с пользователями из федеративных доменов. Это свойство также определяет, разрешено ли внутренним пользователям связываться с пользователями в сценарии разделенного домена.</span><span class="sxs-lookup"><span data-stu-id="968c6-p105">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains. This property also determines whether internal users can communicate with users in a split domain scenario.</span></span>
    
      - <span data-ttu-id="968c6-128">**EnablePartnerDiscovery** указывает, будет ли Lync Server 2013 использовать DNS-записи для определения доменных партнеров, не указанных в списке разрешенных доменов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="968c6-128">**EnablePartnerDiscovery** specifies whether Lync Server 2013 will use DNS records to try to discover partner domains that are not listed in the Active Directory allowed domains list.</span></span> <span data-ttu-id="968c6-129">Если значение "ложь", Lync Server 2013 будет включать только те домены, которые находятся в списке разрешенных доменов.</span><span class="sxs-lookup"><span data-stu-id="968c6-129">If False, Lync Server 2013 will federate only with domains that are found on the allowed domains list.</span></span> <span data-ttu-id="968c6-130">Этот параметр обязателен, если используется маршрутизация службы DNS.</span><span class="sxs-lookup"><span data-stu-id="968c6-130">This parameter is required if you use DNS service routing.</span></span> <span data-ttu-id="968c6-131">В большинстве развертываний устанавливается значение False, чтобы исключить открытие федерации со всеми партнерами.</span><span class="sxs-lookup"><span data-stu-id="968c6-131">In most deployments, the value is set to false to avoid opening up federation to all partners.</span></span>

2.  <span data-ttu-id="968c6-132">Репликация центрального хранилища управления на пограничном сервере и проверка репликации.</span><span class="sxs-lookup"><span data-stu-id="968c6-132">Replicate the Central Management store to the Edge Server and verify the replication.</span></span> <span data-ttu-id="968c6-133">Подробности можно найти в разделе [Экспорт топологии Lync Server 2013 и копирование на внешние носители для установки Edge](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="968c6-133">For details, see [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) in the Deployment documentation.</span></span>

3.  <span data-ttu-id="968c6-134">Настройте *поставщик услуг размещения* на пограничном сервере, запустив командлет **New-CsHostingProvider** , чтобы задать указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="968c6-134">Configure a *hosting provider* on the Edge Server by running the **New-CsHostingProvider** cmdlet to set the following parameters:</span></span>
    
      - <span data-ttu-id="968c6-135">**Identity** указывает уникальный идентификатор строкового значения для поставщика услуг размещения, который вы создаете, например **размещенной UM-среды Exchange**.</span><span class="sxs-lookup"><span data-stu-id="968c6-135">**Identity** specifies a unique string value identifier for the hosting provider that you are creating, for example, **Hosted Exchange UM**.</span></span>
    
      - <span data-ttu-id="968c6-136">Параметр **Enabled** указывает, разрешено ли сетевое подключение между вашим доменом и поставщиком услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="968c6-136">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="968c6-137">Необходимо установить значение **true**.</span><span class="sxs-lookup"><span data-stu-id="968c6-137">Must be set to **True**.</span></span>
    
      - <span data-ttu-id="968c6-138">Параметр **EnabledSharedAddressSpace** определяет, используется ли поставщик услуг размещения в общем адресном пространстве SIP.</span><span class="sxs-lookup"><span data-stu-id="968c6-138">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="968c6-139">Необходимо установить значение **true**.</span><span class="sxs-lookup"><span data-stu-id="968c6-139">Must be set to **True**.</span></span>
    
      - <span data-ttu-id="968c6-140">**HostsOCSUsers** указывает, используется ли поставщик услуг размещения для размещения учетных записей Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="968c6-140">**HostsOCSUsers** indicates whether the hosting provider is used to host Lync Server 2013 accounts.</span></span> <span data-ttu-id="968c6-141">Для него должно быть задано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="968c6-141">Must be set to **False**.</span></span>
    
      - <span data-ttu-id="968c6-142">**ProxyFQDN** указывает полное доменное имя (FQDN) для прокси-сервера, используемого поставщиком услуг размещения, например **proxyserver.fabrikam.com**.</span><span class="sxs-lookup"><span data-stu-id="968c6-142">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider, for example, **proxyserver.fabrikam.com**.</span></span> <span data-ttu-id="968c6-143">Обратитесь к поставщику услуг хостинга для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="968c6-143">Contact your hosting provider for this information.</span></span> <span data-ttu-id="968c6-144">Это значение нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="968c6-144">This value cannot be modified.</span></span> <span data-ttu-id="968c6-145">Если поставщик услуг размещения изменит свой прокси-сервер, необходимо удалить и повторно создать запись для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="968c6-145">If the hosting provider changes its proxy server, you will need to delete and then recreate the entry for that provider.</span></span>
    
      - <span data-ttu-id="968c6-146">"WebProxy **" показывает,** является ли прокси-сервер, используемый поставщиком услуг размещения, включен в топологию Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="968c6-146">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server 2013 topology.</span></span> <span data-ttu-id="968c6-147">Для него должно быть задано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="968c6-147">Must be set to **False**.</span></span>

<span data-ttu-id="968c6-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="968c6-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

