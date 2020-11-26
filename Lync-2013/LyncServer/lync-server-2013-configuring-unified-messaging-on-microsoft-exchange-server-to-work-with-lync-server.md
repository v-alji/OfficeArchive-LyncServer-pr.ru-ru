---
title: 'Lync Server 2013: Настройка единой системы обмена сообщениями на сервере Microsoft Exchange Server для работы с Lync Server'
description: 'Lync Server 2013: Настройка единой системы обмена сообщениями на сервере Microsoft Exchange Server для работы с Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Unified Messaging on Microsoft Exchange Server to work with Lync Server 2013
ms:assetid: 058da9c4-23af-4ddb-9f63-70133a8aafc6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398106(v=OCS.15)
ms:contentKeyID: 48183289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 53c303f0ae659536aafcbdfcd829ed236e35a0ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432431"
---
# <a name="configuring-unified-messaging-on-microsoft-exchange-server-to-work-with-lync-server-2013"></a><span data-ttu-id="ef88e-103">Настройка единой системы обмена сообщениями на сервере Microsoft Exchange Server для работы с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef88e-103">Configuring Unified Messaging on Microsoft Exchange Server to work with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef88e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef88e-104">

<span> </span></span></span>

<span data-ttu-id="ef88e-105">_**Тема последнего изменения:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="ef88e-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ef88e-106">Если вы хотите использовать единую систему обмена сообщениями Exchange для обеспечения ответа на звонки, голосового доступа к Outlook или служб автоматического ассистента для пользователей корпоративной голосовой связи, читайте <A href="lync-server-2013-planning-for-exchange-unified-messaging-integration.md">план интеграции единой системы обмена сообщениями в Lync Server 2013</A> в документации по планированию, а затем следуйте инструкциям, приведенным в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ef88e-106">If you want to use Exchange Unified Messaging (UM) to provide call answering, Outlook Voice Access, or auto-attendant services for Enterprise Voice users, read <A href="lync-server-2013-planning-for-exchange-unified-messaging-integration.md">Planning for Exchange Unified Messaging integration in Lync Server 2013</A> in the Planning documentation, and then follow the instructions in this section.</span></span>



</div>

<span data-ttu-id="ef88e-107">Чтобы настроить единую систему обмена сообщениями Exchange для работы с корпоративной голосовой связью, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ef88e-107">To configure Exchange Unified Messaging (UM) to work with Enterprise Voice, you’ll need to perform the following tasks:</span></span>

  - <span data-ttu-id="ef88e-108">Настройка сертификатов на сервере, на котором запущены службы единой системы обмена сообщениями Exchange</span><span class="sxs-lookup"><span data-stu-id="ef88e-108">Configure certificates on the server running Exchange Unified Messaging (UM) services</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ef88e-109">Добавляйте все серверы клиентского доступа и почтовых ящиков ко всем абонентам SIP URI для UM.</span><span class="sxs-lookup"><span data-stu-id="ef88e-109">Add all Client Access and Mailbox servers to all UM SIP URI dial plans.</span></span> <span data-ttu-id="ef88e-110">Если нет, Маршрутизация исходящих вызовов не будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="ef88e-110">If not, outbound call routing won’t work as expected.</span></span>

    
    </div>

  - <span data-ttu-id="ef88e-111">Создайте одну или несколько абонентов SIP с помощью URI для обмена сообщениями, а также с телефонными номерами абонентов, а затем создайте соответствующие абонентские планы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef88e-111">Create one or more UM SIP URI dial plans, along with the subscriber access phone numbers, as needed, and then create corresponding Lync Server dial plans.</span></span>

  - <span data-ttu-id="ef88e-112">Используйте сценарий **exchucutil.ps1** , чтобы:</span><span class="sxs-lookup"><span data-stu-id="ef88e-112">Use the **exchucutil.ps1** script to:</span></span>
    
      - <span data-ttu-id="ef88e-113">Создание IP-шлюзов UM.</span><span class="sxs-lookup"><span data-stu-id="ef88e-113">Create UM IP gateways.</span></span>
    
      - <span data-ttu-id="ef88e-114">Создание групп слежения UM.</span><span class="sxs-lookup"><span data-stu-id="ef88e-114">Create UM hunt groups.</span></span>
    
      - <span data-ttu-id="ef88e-115">Предоставьте Lync Server 2013 разрешение на чтение объектов доменных служб Active Directory UM.</span><span class="sxs-lookup"><span data-stu-id="ef88e-115">Grant Lync Server 2013 permission to read UM Active Directory Domain Services objects.</span></span>

  - <span data-ttu-id="ef88e-116">Создайте объект автоматического ассистента UM.</span><span class="sxs-lookup"><span data-stu-id="ef88e-116">Create a UM auto-attendant object.</span></span>

  - <span data-ttu-id="ef88e-117">Создайте объект абонентского доступа.</span><span class="sxs-lookup"><span data-stu-id="ef88e-117">Create a subscriber access object.</span></span>

  - <span data-ttu-id="ef88e-118">Создание универсального кода ресурса (URI) SIP для каждого пользователя и сопоставление пользователей с помощью абонентской группы SIP URI.</span><span class="sxs-lookup"><span data-stu-id="ef88e-118">Create a SIP URI for each user and associating users with a UM SIP URI dial plan.</span></span>

<div>

## <a name="requirements-and-recommendations"></a><span data-ttu-id="ef88e-119">Требования и рекомендации</span><span class="sxs-lookup"><span data-stu-id="ef88e-119">Requirements and Recommendations</span></span>

<span data-ttu-id="ef88e-120">Прежде чем приступить к работе, в документации в этом разделе предполагается, что вы развернули следующие роли Exchange 2013: клиентский доступ и почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="ef88e-120">Before you begin, the documentation in this section assumes that you have deployed the following Exchange 2013 roles: Client Access and Mailbox.</span></span> <span data-ttu-id="ef88e-121">В Microsoft Exchange Server 2013 служба единой системы обмена сообщениями Exchange работает в качестве службы на этих серверах.</span><span class="sxs-lookup"><span data-stu-id="ef88e-121">In Microsoft Exchange Server 2013, Exchange UM runs as a service on these servers.</span></span>

<span data-ttu-id="ef88e-122">Дополнительные сведения о развертывании Exchange 2013 можно найти в библиотеке Exchange 2013 TechNet по адресу [https://go.microsoft.com/fwlink/p/?LinkId=266637](https://go.microsoft.com/fwlink/p/?linkid=266637)</span><span class="sxs-lookup"><span data-stu-id="ef88e-122">For details about deploying Exchange 2013, see the Exchange 2013 TechNet Library at [https://go.microsoft.com/fwlink/p/?LinkId=266637](https://go.microsoft.com/fwlink/p/?linkid=266637)</span></span>

<span data-ttu-id="ef88e-123">Также обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="ef88e-123">Also note the following:</span></span>

  - <span data-ttu-id="ef88e-124">Если в нескольких лесах установлено приложение Exchange UM, для каждого леса UM необходимо выполнить инструкции интеграции с Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef88e-124">If Exchange UM is installed in multiple forests, the Exchange Server integration steps must be performed for each UM forest.</span></span> <span data-ttu-id="ef88e-125">Кроме того, каждый лес UM необходимо настроить для доверия к лесу, в котором развернут сервер Lync Server 2013, и в лесу, в котором развернут Lync Server 2013, должен быть настроен для доверия к каждому лесу UM.</span><span class="sxs-lookup"><span data-stu-id="ef88e-125">In addition, each UM forest must be configured to trust the forest in which Lync Server 2013 is deployed, and the forest in which Lync Server 2013 is deployed must be configured to trust each UM forest.</span></span>

  - <span data-ttu-id="ef88e-126">Этапы интеграции выполняются как на ролях сервера Exchange, так и на серверах, на которых работает служба единой системы обмена сообщениями, а также на сервере с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef88e-126">Integration steps are performed on both the Exchange Server roles where Unified Messaging services are running, and on the server running Lync Server 2013.</span></span> <span data-ttu-id="ef88e-127">Перед выполнением шагов интеграции Lync Server 2013 необходимо выполнить инструкции интеграции с единой системой обмена сообщениями Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef88e-127">You should perform the Exchange Server Unified Messaging integration steps before you perform the Lync Server 2013 integration steps.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ef88e-128">Чтобы узнать, какие этапы интеграции выполняются на каких серверах и для каких ролей администратора, ознакомьтесь со статьей <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">процесс развертывания для интеграции локальной единой системы обмена сообщениями и Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ef88e-128">To see which integration steps are performed on which servers and by which administrator roles, see <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</A>.</span></span>

    
    </div>

<span data-ttu-id="ef88e-129">Следующие средства должны быть доступны на каждом сервере, на котором запущена служба единой системы обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef88e-129">The following tools must be available on each server running Exchange UM:</span></span>

  - <span data-ttu-id="ef88e-130">Консоль управления Exchange</span><span class="sxs-lookup"><span data-stu-id="ef88e-130">Exchange Management Shell</span></span>

  - <span data-ttu-id="ef88e-131">**exchucutil.ps1** сценария, который выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="ef88e-131">The script **exchucutil.ps1**, which performs the following tasks:</span></span>
    
      - <span data-ttu-id="ef88e-132">Создает IP-шлюз UM для каждого сервера Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef88e-132">Creates a UM IP gateway for each Lync Server 2013.</span></span>
    
      - <span data-ttu-id="ef88e-133">Создание группы слежения для каждого шлюза.</span><span class="sxs-lookup"><span data-stu-id="ef88e-133">Creates a hunt group for each gateway.</span></span> <span data-ttu-id="ef88e-134">Идентификатор пилотной программы для каждой из групп слежения указывает абонентскую группу UM SIP, используемую интерфейсным пулом или сервером Standard Edition, который связан с шлюзом.</span><span class="sxs-lookup"><span data-stu-id="ef88e-134">The pilot identifier of each hunt group specifies the UM SIP URI dial plan used by the Front End pool or Standard Edition server that is associated with the gateway.</span></span>
    
      - <span data-ttu-id="ef88e-135">Предоставляет Lync Server 2013 разрешение на чтение объектов единой системы обмена сообщениями Exchange в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ef88e-135">Grants Lync Server 2013 permission to read Exchange UM objects in Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ef88e-136">Содержание</span><span class="sxs-lookup"><span data-stu-id="ef88e-136">In This Section</span></span>

  - [<span data-ttu-id="ef88e-137">Настройка сертификатов на сервере, на котором работает единая система обмена сообщениями Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="ef88e-137">Configure certificates on the server running Microsoft Exchange Server Unified Messaging</span></span>](lync-server-2013-configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging.md)

  - [<span data-ttu-id="ef88e-138">Настройка единой системы обмена сообщениями в Microsoft Exchange для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef88e-138">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</span></span>](lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md)

<span data-ttu-id="ef88e-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef88e-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

