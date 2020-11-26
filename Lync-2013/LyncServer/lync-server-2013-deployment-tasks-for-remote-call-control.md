---
title: 'Lync Server 2013: задачи развертывания для удаленного управления звонками'
description: 'Lync Server 2013: задачи развертывания для удаленного управления звонками.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment tasks for remote call control
ms:assetid: 20218871-4f27-4611-9b7e-c0ca55908284
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558624(v=OCS.15)
ms:contentKeyID: 48183599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61d0d57489bd93d7e6ce0209c605f05a2417bded
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429610"
---
# <a name="deployment-tasks-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="774f4-103">Задачи развертывания для удаленного управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="774f4-103">Deployment tasks for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="774f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="774f4-104">

<span> </span></span></span>

<span data-ttu-id="774f4-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="774f4-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="774f4-106">В этой статье описаны задачи развертывания, которые необходимо выполнить, чтобы включить удаленное управление звонками для пользователей в среде Lync Server.</span><span class="sxs-lookup"><span data-stu-id="774f4-106">This topic describes the deployment tasks that you must perform to enable remote call control for users in your Lync Server environment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="774f4-107">Если вы переносите в Microsoft Office Communicator 2007 R2 пользователей, для которых уже разрешено удаленное управление звонками, необходимо выполнить дополнительные действия по развертыванию, прежде чем приступить к выполнению задач по удалению удаленного управления звонками, описанным в этой статье.</span><span class="sxs-lookup"><span data-stu-id="774f4-107">If you are migrating users previously enabled for remote call control in Microsoft Office Communicator 2007 R2, you must perform an additional deployment task before you begin performing the remote call control deployment tasks described in this topic.</span></span> <span data-ttu-id="774f4-108">В процессе миграции на Lync Server вы должны удалить доверенные записи приложения (ранее известные как <EM>Авторизованные записи узла</EM>) с помощью средств администрирования Office Communications Server 2007 R2, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="774f4-108">During the migration process to Lync Server, trusted application entries (previously known as <EM>authorized host entries</EM>) must be removed by using the Office Communications Server 2007 R2 administrative tools, as appropriate.</span></span><BR><span data-ttu-id="774f4-109">Подробнее об удалении авторизованных узлов можно узнать <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">в разделе Удаление устаревшего авторизованного узла в Lync Server 2013 (необязательно)</A>.</span><span class="sxs-lookup"><span data-stu-id="774f4-109">For details about removing authorized hosts, see <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Remove a legacy authorized host in Lync Server 2013 (optional)</A>.</span></span>



</div>

<div>

## <a name="step-1-install-and-configure-the-sipcsta-gateway-to-communicate-with-your-pbx"></a><span data-ttu-id="774f4-110">Шаг 1: Установка и Настройка шлюза SIP/CSTA для связи с АТС</span><span class="sxs-lookup"><span data-stu-id="774f4-110">Step 1: Install and Configure the SIP/CSTA Gateway to Communicate with Your PBX</span></span>

<span data-ttu-id="774f4-111">Для обеспечения функций управления удаленными звонками для пользователей необходимо установить по крайней мере один шлюз SIP/CSTA, который может подключаться к обоим серверам Lync и существующим частным филиалам (УАТС) в своей среде.</span><span class="sxs-lookup"><span data-stu-id="774f4-111">You need to install at least one SIP/CSTA gateway that can connect to both Lync Server and the existing private branch exchange (PBX) in your environment in order to provide remote call control features to your users.</span></span> <span data-ttu-id="774f4-112">Шлюз SIP/CSTA — это шлюз между SIP и коммуникационной программой, поддерживаемой компьютером (CSTA).</span><span class="sxs-lookup"><span data-stu-id="774f4-112">A SIP/CSTA gateway is a gateway between SIP and a computer-supported telecommunications application (CSTA).</span></span> <span data-ttu-id="774f4-113">При установке нескольких шлюзов или только одного из них можно настроить только один шлюз или УАТС.</span><span class="sxs-lookup"><span data-stu-id="774f4-113">Whether you install multiple gateways or just one, each user can be configured with only one gateway or PBX.</span></span> <span data-ttu-id="774f4-114">Если у существующей АТС нет интерфейса SIP/CSTA, убедитесь, что вы разворачиваете шлюз SIP/CSTA, поддерживающий УАТС, в том числе поддержку специальных протоколов передачи сигналов для фирменной АТС.</span><span class="sxs-lookup"><span data-stu-id="774f4-114">If your existing PBX does not have a SIP/CSTA interface, ensure you deploy a SIP/CSTA gateway that can support the PBX, including support for proprietary PBX vendor-specific signaling protocols.</span></span> <span data-ttu-id="774f4-115">Сведения о возможностях можно найти в статьях каждого поставщика напрямую.</span><span class="sxs-lookup"><span data-stu-id="774f4-115">For details about capabilities, consult each vendor directly.</span></span>

<span data-ttu-id="774f4-116">Когда вы будете готовы к развертыванию шлюза SIP/CSTA, который может интегрироваться с сервером Lync Server для удаленного управления звонками, также обратитесь к поставщику шлюза или документации поставщика, в соответствии с синтаксисом, требуемым шлюзом для указанных ниже данных.</span><span class="sxs-lookup"><span data-stu-id="774f4-116">When you are ready to deploy a SIP/CSTA gateway that can integrate with Lync Server for remote call control, also consult with your gateway vendor or the vendor’s gateway documentation regarding the syntax required by the gateway for the following information:</span></span>

  - <span data-ttu-id="774f4-117">Универсальный код ресурса (URI) основного сервера</span><span class="sxs-lookup"><span data-stu-id="774f4-117">Line server URI of the gateway</span></span>

  - <span data-ttu-id="774f4-118">Универсальный код ресурса (URI) для пользователей, которые будут назначены шлюзу</span><span class="sxs-lookup"><span data-stu-id="774f4-118">Line URI for users that will be assigned to the gateway</span></span>

<span data-ttu-id="774f4-119">Указанные выше параметры необходимы во время настройки пользователя и должны быть указаны надлежащим образом шлюзом для маршрутизации и подключения к УАТС.</span><span class="sxs-lookup"><span data-stu-id="774f4-119">The preceding settings are required during user configuration and must be specified as expected by the gateway to route and connect to the PBX properly.</span></span>

<span data-ttu-id="774f4-120">Вы можете обратиться к разработчикам на веб-сайте Microsoft Unified Communications Open Program для взаимодействия по адресу [https://go.microsoft.com/fwlink/p/?linkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309) .</span><span class="sxs-lookup"><span data-stu-id="774f4-120">You can refer to vendors on the Microsoft Unified Communications Open Interoperability Program website at [https://go.microsoft.com/fwlink/p/?linkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309).</span></span>

</div>

<div>

## <a name="step-2-configure-lync-server-to-route-csta-requests-to-the-sipcsta-gateway"></a><span data-ttu-id="774f4-121">Шаг 2: Настройка сервера Lync Server для маршрутизации запросов CSTA на шлюз SIP/CSTA</span><span class="sxs-lookup"><span data-stu-id="774f4-121">Step 2: Configure Lync Server to Route CSTA Requests to the SIP/CSTA Gateway</span></span>

<span data-ttu-id="774f4-122">Вы должны создать статические маршруты для групп Lync Server на целевом адресе (URI сервера) всех шлюзов SIP/CSTA в развертывании, которому планируется перенаправлять запросы на управление удаленными звонками.</span><span class="sxs-lookup"><span data-stu-id="774f4-122">You must create static routes on Lync Server pools to the destination address (server URI) of all SIP/CSTA gateways in your deployment to which you intend to route remote call control requests.</span></span> <span data-ttu-id="774f4-123">Кроме того, необходимо создать надежную запись приложения, соответствующую каждому адресу назначения.</span><span class="sxs-lookup"><span data-stu-id="774f4-123">You must also create a trusted application entry that corresponds to each destination address.</span></span> <span data-ttu-id="774f4-124">Назначение шлюза в качестве надежного приложения означает, что состояние Trusted является надежным для работы в рамках среды Lync Server, несмотря на то, что оно создано сторонним производителем (и запускается как *внешняя служба* , так как это служба, которая не является встроенной частью продукта).</span><span class="sxs-lookup"><span data-stu-id="774f4-124">When you designate the gateway as a trusted application, it is given trusted status to run as part of the Lync Server environment even though it is developed by a third party (and runs what is referred to as an *external service* because it is a service that is not a built-in part of the product).</span></span> <span data-ttu-id="774f4-125">Наконец, если Lync Server подключается к шлюзу SIP/CSTA с помощью TCP-соединения вместо подключения TLS, необходимо также определить IP-адрес шлюза с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="774f4-125">Finally, if Lync Server will connect to the SIP/CSTA gateway using a Transmission Control Protocol (TCP) connection instead of a Transport Layer Security (TLS) connection, you must also define the gateway IP address by using Topology Builder.</span></span>

<span data-ttu-id="774f4-126">Дополнительные сведения о настройке статических маршрутов можно найти [в разделе Настройка статического маршрута для удаленного управления звонком в Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md).</span><span class="sxs-lookup"><span data-stu-id="774f4-126">For details about configuring static routes, see [Configure a static route for remote call control in Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md).</span></span>

<span data-ttu-id="774f4-127">Подробнее о настройке записей доверенных приложений можно узнать [в разделе Настройка надежной записи приложения для удаленного управления звонками в Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md).</span><span class="sxs-lookup"><span data-stu-id="774f4-127">For details about configuring trusted application entries, see [Configure a trusted application entry for remote call control in Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md).</span></span>

<span data-ttu-id="774f4-128">Сведения о том, как определить IP-адрес шлюза SIP/CSTA в построителе топологии, можно найти в разделе [Определение IP-адреса шлюза SIP/CSTA в Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md).</span><span class="sxs-lookup"><span data-stu-id="774f4-128">For details about defining a SIP/CSTA gateway IP address in Topology Builder, see [Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md).</span></span>

</div>

<div>

## <a name="step-3-configure-lync-users-for-remote-call-control"></a><span data-ttu-id="774f4-129">Шаг 3: Настройка пользователей Lync для удаленного управления звонками</span><span class="sxs-lookup"><span data-stu-id="774f4-129">Step 3: Configure Lync Users for Remote Call Control</span></span>

<span data-ttu-id="774f4-130">После того как пользователи будут включены в Lync Server, вы можете включить их для удаленного управления звонками с помощью панели управления Lync Server или командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="774f4-130">After users have been enabled for Lync Server, you can use Lync Server Control Panel or Lync Server Management Shell to enable them for remote call control.</span></span> <span data-ttu-id="774f4-131">На этом этапе развертывания вы назначаете каждому пользователю URI сервера линии и универсальный код ресурса (URI) для строки.</span><span class="sxs-lookup"><span data-stu-id="774f4-131">It is during this deployment step that you assign each user a line server URI and a line URI.</span></span> <span data-ttu-id="774f4-132">Универсальный код ресурса (URI) сервера линии — это URI SIP шлюза SIP/CSTA, который вы планируете назначить пользователю.</span><span class="sxs-lookup"><span data-stu-id="774f4-132">The line server URI is the SIP URI of the SIP/CSTA gateway that you plan to assign to the user.</span></span> <span data-ttu-id="774f4-133">Универсальный код ресурса (URI) строки — это уникальный номер телефона, назначенный пользователю.</span><span class="sxs-lookup"><span data-stu-id="774f4-133">The line URI is the unique phone number assigned to the user.</span></span>

<span data-ttu-id="774f4-134">Подробнее о настройке пользователей для удаленного управления звонками можно узнать [в разделе Включение пользователей Lync для удаленного управления звонками в Lync Server 2013](lync-server-2013-enable-lync-users-for-remote-call-control.md).</span><span class="sxs-lookup"><span data-stu-id="774f4-134">For details about configuring users for remote call control, see [Enable Lync users for remote call control in Lync Server 2013](lync-server-2013-enable-lync-users-for-remote-call-control.md).</span></span>

</div>

<div>

## <a name="step-4-define-the-lync-server-phone-number-normalization-rules"></a><span data-ttu-id="774f4-135">Действие 4: определение правил нормализации номера телефона сервера Lync Server</span><span class="sxs-lookup"><span data-stu-id="774f4-135">Step 4: Define the Lync Server Phone Number Normalization Rules</span></span>

<span data-ttu-id="774f4-136">В сценариях удаленного управления звонками Lync Server использует правила нормализации номера телефона для преобразования телефонных номеров, полученных от шлюза SIP/CSTA, в формат E. 164.</span><span class="sxs-lookup"><span data-stu-id="774f4-136">In remote call control scenarios, Lync Server uses phone number normalization rules to convert phone numbers it receives from the SIP/CSTA gateway to E.164 format.</span></span> <span data-ttu-id="774f4-137">Для правильного функционирования функций удаленного управления звонками номера телефонов должны быть в этом стандартном формате.</span><span class="sxs-lookup"><span data-stu-id="774f4-137">Phone numbers must be in this standardized format for certain remote call control features to function properly.</span></span> <span data-ttu-id="774f4-138">Удаленное управление звонками использует те же правила нормализации номеров телефонов, которые настроены для нормализации номеров телефонов службы адресной книги, которые отличаются от правил нормализации номеров телефонов, используемых для корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="774f4-138">Remote call control uses the same phone number normalization rules that you configure for Address Book Service phone number normalization, which are different from the phone number normalization rules used for Enterprise Voice.</span></span>

<span data-ttu-id="774f4-139">Сведения о том, как удаленное управление звонками использует правила нормализации номера телефона, описаны [в разделе Удаленное управление звонками и нормализация номеров в Lync Server 2013](lync-server-2013-remote-call-control-and-phone-number-normalization.md).</span><span class="sxs-lookup"><span data-stu-id="774f4-139">For details about how remote call control uses phone number normalization rules, see [Remote call control and phone number normalization in Lync Server 2013](lync-server-2013-remote-call-control-and-phone-number-normalization.md).</span></span> <span data-ttu-id="774f4-140">Дополнительные сведения о правилах нормализации номеров телефонов в службе "Адресная книга" можно найти в разделе [Администрирование службы адресной книги в Lync Server 2013](lync-server-2013-administering-the-address-book-service.md) в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="774f4-140">For details about phone number normalization rules for Address Book Service, see [Administering the Address Book Service in Lync Server 2013](lync-server-2013-administering-the-address-book-service.md) topic in the Operations documentation.</span></span>

<span data-ttu-id="774f4-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="774f4-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

