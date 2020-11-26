---
title: Настройка локальной интеграции Lync Server с Exchange Online
description: Настройка локальной интеграции Lync Server с Exchange Online.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring on-premises Lync Server integration with Exchange Online
ms:assetid: 95a20117-2064-43c4-94fe-cac892cadb6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh533880(v=OCS.15)
ms:contentKeyID: 48184900
ms.date: 03/30/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59c612bcdcdf4803bd6f9f2b38f1f9bb7dbad016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432837"
---
# <a name="configuring-on-premises-lync-server-2013-integration-with-exchange-online"></a><span data-ttu-id="627c1-103">Настройка локальной интеграции Lync Server 2013 с Exchange Online</span><span class="sxs-lookup"><span data-stu-id="627c1-103">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="627c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="627c1-104">

<span> </span></span></span>

<span data-ttu-id="627c1-105">_**Тема последнего изменения:** 2018-03-30_</span><span class="sxs-lookup"><span data-stu-id="627c1-105">_**Topic Last Modified:** 2018-03-30_</span></span>

<span data-ttu-id="627c1-106">Клиенты, использующие локальные развертывания Lync Server 2013, могут настраивать взаимодействие с приложением Microsoft Outlook Web App в Microsoft Exchange Online в режиме гибридной развертки.</span><span class="sxs-lookup"><span data-stu-id="627c1-106">Customers who are using on-premises Lync Server 2013 deployments can configure interoperability with Microsoft Outlook Web App in Microsoft Exchange Online in a hybrid deployment mode.</span></span> <span data-ttu-id="627c1-107">Возможности взаимодействия включают единый вход и интеграцию обмена мгновенными сообщениями и сведениями о присутствии в интерфейс Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="627c1-107">Interoperability features include single sign on and instant messaging (IM) and presence integration with the Outlook Web App interface.</span></span> <span data-ttu-id="627c1-108">Чтобы включить эту интеграцию, необходимо настроить граничный сервер в локальной среде развертывания Lync Server, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="627c1-108">To enable this integration, you must configure the Edge Server in your on-premises Lync Server deployment by completing the following tasks:</span></span>

  - <span data-ttu-id="627c1-109">настройте общее адресное пространство SIP;</span><span class="sxs-lookup"><span data-stu-id="627c1-109">Configure a shared SIP address space</span></span>

  - <span data-ttu-id="627c1-110">Настройка поставщика услуг размещения на пограничном сервере</span><span class="sxs-lookup"><span data-stu-id="627c1-110">Configure a hosting provider on the Edge Server</span></span>

  - <span data-ttu-id="627c1-111">Проверка репликации обновленного центрального хранилища в центре администрирования</span><span class="sxs-lookup"><span data-stu-id="627c1-111">Verify replication of the updated Central Management store</span></span>

<span data-ttu-id="627c1-112">Если Lync Server 2013 интегрирован с Exchange Online, пользователь, который пытается войти в мгновенном сообщении из OWA, считается удаленным или внешним пользователем.</span><span class="sxs-lookup"><span data-stu-id="627c1-112">If Lync Server 2013 is integrated with Exchange Online, a user who is trying to sign in to IM from OWA is considered a remote or external user.</span></span> <span data-ttu-id="627c1-113">В этом случае пользователю должна быть назначена политика внешней доступа, для которой выбраны указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="627c1-113">In this scenario, this user must have an external access policy assigned that has the following option selected:</span></span>

<span data-ttu-id="627c1-114">**Включение связи с удаленными пользователями**</span><span class="sxs-lookup"><span data-stu-id="627c1-114">**Enable communications with remote users**</span></span>

<span data-ttu-id="627c1-115">Включите этот параметр, если вы хотите, чтобы пользователи в вашей организации, которые находятся за пределами межсетевого экрана (например, подключены к сети и пользователи, которые находятся в дороге), смогли подключиться к серверу Lync через Интернет.</span><span class="sxs-lookup"><span data-stu-id="627c1-115">Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

<span data-ttu-id="627c1-116">Дополнительные сведения можно найти [в разделе Управление политикой внешнего доступа в Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="627c1-116">For more information, see [Manage external access policy in Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span></span>

<div>

## <a name="configure-a-shared-sip-address-space"></a><span data-ttu-id="627c1-117">Настройка общего адресного пространства SIP</span><span class="sxs-lookup"><span data-stu-id="627c1-117">Configure a Shared SIP Address Space</span></span>

<span data-ttu-id="627c1-118">Для интеграции локального сервера Lync Server 2013 с Exchange Online необходимо настроить общее адресное пространство SIP.</span><span class="sxs-lookup"><span data-stu-id="627c1-118">To integrate on-premises Lync Server 2013 with Exchange Online, you must configure a shared SIP address space.</span></span> <span data-ttu-id="627c1-119">Одно и то же адресное пространство домена SIP поддерживается как в Lync Server, так и в службе Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="627c1-119">The same SIP domain address space is supported by both Lync Server and the Exchange Online service.</span></span>

<span data-ttu-id="627c1-120">С помощью командной консоли Lync Server настройте сервер граничного сервера для Федерации, запустив командлет **Set-CSAccessEdgeConfiguration** , используя параметры, показанные в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="627c1-120">Using the Lync Server Management Shell, configure the Edge Server for federation by running the **Set-CSAccessEdgeConfiguration** cmdlet, using the parameters that are displayed in the following example:</span></span>

    Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

  - <span data-ttu-id="627c1-121">**AllowFederatedUsers** указывает, разрешено ли внутренним пользователям взаимодействовать с пользователями из федеративных доменов.</span><span class="sxs-lookup"><span data-stu-id="627c1-121">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains.</span></span> <span data-ttu-id="627c1-122">Это свойство также определяет, могут ли внутренние пользователи общаться с пользователями в общем пространстве адресного пространства SIP с Lync Server и Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="627c1-122">This property also determines whether internal users can communicate with users in a shared SIP address space scenario with Lync Server and Exchange Online.</span></span>

<span data-ttu-id="627c1-123">Подробнее об использовании командной консоли Lync Server можно узнать в разделе [Lync server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="627c1-123">For details about how to use the Lync Server Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="configure-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="627c1-124">Настройка поставщика услуг размещения на пограничном сервере</span><span class="sxs-lookup"><span data-stu-id="627c1-124">Configure a Hosting Provider on the Edge Server</span></span>

<span data-ttu-id="627c1-125">Для настройки поставщика услуг размещения на пограничном сервере используйте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="627c1-125">Use the Lync Server Management Shell to configure a hosting provider on the Edge Server.</span></span> <span data-ttu-id="627c1-126">Для этого выполните командлет **New-CsHostingProvider** с помощью параметров, описанных в приведенном ниже примере.</span><span class="sxs-lookup"><span data-stu-id="627c1-126">To do this, run the **New-CsHostingProvider** cmdlet, using the parameters in the following example:</span></span>

    New-CsHostingProvider -Identity "Exchange Online" -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFqdn "exap.um.outlook.com" -IsLocal $False -VerificationLevel UseSourceVerification

<div>


> [!NOTE]
> <span data-ttu-id="627c1-127">При использовании Office 365 под управлением 21Vianet в Китае замените значение для параметра <STRONG>ProxyFqdn</STRONG> (например, exap.um.outlook.com) на полное доменное имя для службы под управлением 21Vianet: "exap.um.partner.outlook.cn".</span><span class="sxs-lookup"><span data-stu-id="627c1-127">If you are using Office 365 operated by 21Vianet in China, replace the value for the <STRONG>ProxyFqdn</STRONG> parameter in this example ("exap.um.outlook.com") with the FQDN for the service operated by 21Vianet: "exap.um.partner.outlook.cn".</span></span>



</div>

  - <span data-ttu-id="627c1-128">Параметр **Identity** определяет строковое значение уникального идентификатора для создаваемого поставщика услуг размещения (например, "Exchange Online").</span><span class="sxs-lookup"><span data-stu-id="627c1-128">**Identity** specifies a unique string value identifier for the hosting provider that you are creating (for example, "Exchange Online").</span></span> <span data-ttu-id="627c1-129">Значения, содержащие пробелы, должны быть заключены в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="627c1-129">Values that contain spaces must be in double quotation marks.</span></span>

  - <span data-ttu-id="627c1-130">Параметр **Enabled** указывает, разрешено ли сетевое подключение между вашим доменом и поставщиком услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="627c1-130">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="627c1-131">Должно быть задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="627c1-131">This must be set to **True**.</span></span>

  - <span data-ttu-id="627c1-132">Параметр **EnabledSharedAddressSpace** определяет, используется ли поставщик услуг размещения в общем адресном пространстве SIP.</span><span class="sxs-lookup"><span data-stu-id="627c1-132">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="627c1-133">Должно быть задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="627c1-133">This must be set to **True**.</span></span>

  - <span data-ttu-id="627c1-134">**HostsOCSUsers** указывает, используется ли поставщик услуг размещения для размещения Office Communications Server или Lync Server.</span><span class="sxs-lookup"><span data-stu-id="627c1-134">**HostsOCSUsers** indicates whether the hosting provider is used to host Office Communications Server or Lync Server.</span></span> <span data-ttu-id="627c1-135">Для него должно быть задано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="627c1-135">This must be set to **False**.</span></span>

  - <span data-ttu-id="627c1-136">Параметр **ProxyFQDN** определяет полное доменное имя прокси-сервера, используемого поставщиком услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="627c1-136">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider.</span></span> <span data-ttu-id="627c1-137">Полное доменное имя Exchange Online: exap.um.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="627c1-137">For Exchange Online, the FQDN is exap.um.outlook.com.</span></span>

  - <span data-ttu-id="627c1-138">"WebProxy **" показывает,** является ли прокси-сервер, используемый поставщиком услуг размещения, включен в топологию сервера Lync.</span><span class="sxs-lookup"><span data-stu-id="627c1-138">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server topology.</span></span> <span data-ttu-id="627c1-139">Для него должно быть задано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="627c1-139">This must be set to **False**.</span></span>

  - <span data-ttu-id="627c1-140">**VerificationLevel** указывает уровень проверки, разрешенный для сообщений, отправляемых и получаемых поставщиком услуг хостинга.</span><span class="sxs-lookup"><span data-stu-id="627c1-140">**VerificationLevel** indicates the verification level allowed for messages that are sent to and from the hosted provider.</span></span> <span data-ttu-id="627c1-141">Укажите **UseSourceVerification**.</span><span class="sxs-lookup"><span data-stu-id="627c1-141">Specify **UseSourceVerification**.</span></span> <span data-ttu-id="627c1-142">Этот параметр основывается на уровне проверки, который включен в сообщения, отправляемые поставщиком услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="627c1-142">This option relies on the verification level that is included in messages that are sent from the hosting provider.</span></span> <span data-ttu-id="627c1-143">Если этот уровень не указан, сообщение будет отвергнуто как Непроверяемое.</span><span class="sxs-lookup"><span data-stu-id="627c1-143">If this level is not specified, the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="verify-replication-of-the-updated-central-management-store"></a><span data-ttu-id="627c1-144">Проверка репликации обновленного центрального хранилища управления</span><span class="sxs-lookup"><span data-stu-id="627c1-144">Verify Replication of the Updated Central Management Store</span></span>

<span data-ttu-id="627c1-145">Изменения, внесенные с помощью командлетов в предыдущих разделах, автоматически применяются к пограничного сервера, и для их репликации обычно требуется менее одной минуты.</span><span class="sxs-lookup"><span data-stu-id="627c1-145">The changes that you made by using the cmdlets in the preceding sections are automatically applied to the Edge Server, and generally take less than one minute to replicate.</span></span> <span data-ttu-id="627c1-146">Вы можете проверить состояние репликации и применить изменения на пограничном сервере с помощью следующих командлетов.</span><span class="sxs-lookup"><span data-stu-id="627c1-146">You can verify the replication status and that the changes were applied to your Edge Server by using the following cmdlets.</span></span>

<span data-ttu-id="627c1-147">Чтобы проверить наличие обновлений репликации на внутреннем сервере в развертывании Lync Server, выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="627c1-147">To verify replication updates on a server internal in your Lync Server deployment, run the following cmdlet:</span></span>

    Get-CsManagementStoreReplicationStatus

<span data-ttu-id="627c1-148">Чтобы убедиться в том, что изменения применены, выполните на пограничном сервере следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="627c1-148">To verify that the changes were applied, run the following cmdlet on the Edge Server:</span></span>

    Get-CsHostingProvider -LocalStore

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="627c1-149">См. также</span><span class="sxs-lookup"><span data-stu-id="627c1-149">See Also</span></span>


[<span data-ttu-id="627c1-150">Предоставление пользователям Lync Server 2013 голосовой почты в размещенной единой системе обмена сообщениями Exchange</span><span class="sxs-lookup"><span data-stu-id="627c1-150">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)  
[<span data-ttu-id="627c1-151">Интеграция с размещенной единой системой обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="627c1-151">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-unified-messaging-integration.md)  
  

<span data-ttu-id="627c1-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="627c1-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
