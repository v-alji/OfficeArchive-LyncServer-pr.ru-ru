---
title: 'Lync Server 2013: принятие решения о способе развертывания Microsoft Lync'
description: 'Lync Server 2013: решение для развертывания Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431234"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a><span data-ttu-id="f75f8-103">Принятие решения о способе развертывания Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f75f8-103">Deciding how to deploy Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f75f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f75f8-104">

<span> </span></span></span>

<span data-ttu-id="f75f8-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="f75f8-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="f75f8-106">При планировании для Lync первым основным решением будет развертывание Microsoft Lync: в локальной среде Lync Server 2013 или Lync Online с Microsoft 365 или Office 365 в облаке.</span><span class="sxs-lookup"><span data-stu-id="f75f8-106">When planning for Lync, the first major decision is how to deploy Microsoft Lync: as Lync Server 2013 on premises, or Lync Online with Microsoft 365 or Office 365 in the cloud.</span></span>

  - <span data-ttu-id="f75f8-107">**Lync Server 2013 в локальной среде** : этот выбор обеспечивает полный комплект функций Lync и обеспечивает максимальную гибкость при настройке, настройке и работе развертывания.</span><span class="sxs-lookup"><span data-stu-id="f75f8-107">**Lync Server 2013 on-premises** : This choice provides the complete Lync feature set and provides ultimate flexibility in configuring, customizing, and operating your deployment.</span></span> <span data-ttu-id="f75f8-108">Все серверы устанавливаются на сайт и обслуживаются вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="f75f8-108">All servers are installed onsite and maintained by your organization.</span></span> <span data-ttu-id="f75f8-109">Локальное развертывание обеспечивает полный диапазон возможностей Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f75f8-109">An on-premises deployment provides the full range of Lync Server features.</span></span>

  - <span data-ttu-id="f75f8-110">**Lync Online в облаке** Lync Online разработан для организаций, которые хотят использовать стоимость и динамичность обмена мгновенными сообщениями, присутствия и собраний на основе облачных служб, не жертвуя возможностями бизнес-класса в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f75f8-110">**Lync Online in the cloud** Lync Online is designed for organizations that want the cost and agility benefits of cloud-based instant messaging, presence, and meetings without sacrificing the business-class capabilities of Lync Server.</span></span> <span data-ttu-id="f75f8-111">С помощью Lync Online корпорация Майкрософт развертывает и поддерживает требуемую серверную инфраструктуру, а также обрабатывает непрерывное обслуживание, исправления и обновления.</span><span class="sxs-lookup"><span data-stu-id="f75f8-111">With Lync Online, Microsoft deploys and maintains the required server infrastructure, and handles ongoing maintenance, patches, and upgrades.</span></span> <span data-ttu-id="f75f8-112">Некоторые возможности, доступные в локальном развертывании, недоступны в Lync Online.</span><span class="sxs-lookup"><span data-stu-id="f75f8-112">Some features available in an on-premises deployment are not available in Lync Online.</span></span>

<span data-ttu-id="f75f8-113">Какой тип развертывания наилучшим образом зависит от нагрузки, которую вы хотите развернуть, а также от географического и бизнес-статуса Организации.</span><span class="sxs-lookup"><span data-stu-id="f75f8-113">Which type of deployment would be best for you depends on the workloads you want to deploy, and your organization’s geographical and business status.</span></span>

<div>

## <a name="lync-server"></a><span data-ttu-id="f75f8-114">Lync Server</span><span class="sxs-lookup"><span data-stu-id="f75f8-114">Lync Server</span></span>

<span data-ttu-id="f75f8-115">Развертывание с помощью локального сервера Lync Server наилучшим образом подходит для следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="f75f8-115">An on-premises Lync Server deployment is best for the following scenarios:</span></span>

  - <span data-ttu-id="f75f8-116">**Возможности поддержки голосовой связи в корпоративной среде**   Если вы планируете развернуть полноценную корпоративную голосовую почту, чтобы заменить АТС или использовать дополнительные функции звонков, требуется локальное развертывание Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f75f8-116">**Full Enterprise Voice Capabilities**   If you plan to deploy a full Enterprise Voice solution to replace your PBX or which uses advanced calling features, an on-premises Lync Server deployment is required.</span></span> <span data-ttu-id="f75f8-117">Локальная поддержка прямого подключения к системам АТС и магистрали и дополнительным функциям, таким как группы ответа и переадресация звонков.</span><span class="sxs-lookup"><span data-stu-id="f75f8-117">On-premises supports direct connectivity with PBX systems and trunks, and advanced phone features such as response groups and call park.</span></span> <span data-ttu-id="f75f8-118">Lync Online в настоящее время не поддерживает эти функции.</span><span class="sxs-lookup"><span data-stu-id="f75f8-118">Lync Online does not currently support these features.</span></span>

  - <span data-ttu-id="f75f8-119">**Элементы управления качеством мультимедиа**   Если вы хотите использовать все функции контроля качества мультимедиа, такие как управление допуском звонков (CAC) и функции качества обслуживания (QoS), вам потребуется локальное развертывание.</span><span class="sxs-lookup"><span data-stu-id="f75f8-119">**Media Quality Controls**   If you want the full range of media quality assurance features, such as Call Admission Control (CAC) and Quality of Service (QoS) features, you will want an on-premises deployment .</span></span>

  - <span data-ttu-id="f75f8-120">**Сохраняемый чат**   Если вам нужно развернуть сохраняемый чат для Организации, необходимо выбрать локальное развертывание.</span><span class="sxs-lookup"><span data-stu-id="f75f8-120">**Persistent Chat**   If you need to deploy Persistent chat for your organization, you must choose an on-premises deployment.</span></span>

  - <span data-ttu-id="f75f8-121">**серверные приложения третьих лиц**   Только локальные развертывания могут работать с надежными приложениями сторонних разработчиков, использующими API Microsoft Unified Communications (UCMA).</span><span class="sxs-lookup"><span data-stu-id="f75f8-121">**3rd-Party Server Applications**   Only on-premises deployments can work with trusted 3rd-party applications that use the Microsoft Unified Communications Managed API (UCMA).</span></span>

  - <span data-ttu-id="f75f8-122">**Компании с несколькими национальными региональными стандартными и национальными стандартами, которым нужна региональная поддержка**   Если у вас есть центры обработки данных в нескольких странах или регионах и нужно развертывать и управлять ими на разных региональных стандартах, лучше использовать локальное развертывание, так как это обеспечивает этот тип региональных возможностей управления.</span><span class="sxs-lookup"><span data-stu-id="f75f8-122">**Multi-National/Multi-Regional Companies Needing Regional Support**   If you have datacenters in multiple countries or regions and need servers to be deployed and managed on a regional basis, an on-premises deployment is best, as it provides this type of regional management capabilities.</span></span>

  - <span data-ttu-id="f75f8-123">**Полный контроль над политиками, отчетами и обновлениями**   С помощью локального развертывания Lync Server вы можете получить доступ ко всем наборам политик сервера и клиента, мониторингу и другим отчетам, а также время обновления.</span><span class="sxs-lookup"><span data-stu-id="f75f8-123">**Complete control over policies, reports, and upgrades**   With an on premises Lync Server deployment, you have access to the full set of server and client policies, Monitoring and other reports, and timing of upgrades.</span></span> <span data-ttu-id="f75f8-124">Lync Online предоставляет подмножество параметров политики и отчетов, а также предоставляет ограниченные, но важные окна для принятия обновлений.</span><span class="sxs-lookup"><span data-stu-id="f75f8-124">Lync Online provides a subset of policy setting and reports, and provides a limited, though significant, window for accepting upgrades.</span></span>

</div>

<div>

## <a name="lync-online"></a><span data-ttu-id="f75f8-125">Lync Online</span><span class="sxs-lookup"><span data-stu-id="f75f8-125">Lync Online</span></span>

<span data-ttu-id="f75f8-126">Если ни один из перечисленных выше факторов не является критическим, вы можете выбрать Lync Online для упрощения развертывания и управления.</span><span class="sxs-lookup"><span data-stu-id="f75f8-126">If none of the factors in the preceding list are critical for you, you may want to choose Lync Online, for simpler deployment and manageability.</span></span> <span data-ttu-id="f75f8-127">Lync Online обеспечивает надежное средство обмена мгновенными сообщениями, присутствие и конференц-связь, а также включает голосовые и видеозвонки по протоколу IP между пользователями в Организации.</span><span class="sxs-lookup"><span data-stu-id="f75f8-127">Lync Online provides a robust IM, presence and conferencing feature set, and also enables voice and video calls over IP between users in your organization.</span></span>

<span data-ttu-id="f75f8-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f75f8-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
