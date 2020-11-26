---
title: 'Lync Server 2013: роли сервера'
description: Роли сервера Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server roles
ms:assetid: 7137fc06-fca2-4e5f-9db5-10c7c29a788c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398536(v=OCS.15)
ms:contentKeyID: 48184456
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ee4636e602e5bfb8ce6eacdccb3d190f5728d1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441860"
---
# <a name="server-roles-in-lync-server-2013"></a><span data-ttu-id="398ee-103">Роли сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="398ee-103">Server roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="398ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="398ee-104">

<span> </span></span></span>

<span data-ttu-id="398ee-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="398ee-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="398ee-106">Каждый сервер, на котором работает Lync Server, выполняет одну или несколько *ролей сервера*.</span><span class="sxs-lookup"><span data-stu-id="398ee-106">Each server running Lync Server runs one or more *server roles*.</span></span> <span data-ttu-id="398ee-107">Роль сервера — это определенный набор функциональных возможностей Lync Server, предоставляемых этим сервером.</span><span class="sxs-lookup"><span data-stu-id="398ee-107">A server role is a defined set of Lync Server functionalities provided by that server.</span></span> <span data-ttu-id="398ee-108">Вам не нужно развертывать все доступные роли сервера в сети.</span><span class="sxs-lookup"><span data-stu-id="398ee-108">You do not need to deploy all available server roles in your network.</span></span> <span data-ttu-id="398ee-109">Установите только те роли сервера, которые предоставляют нужные функции.</span><span class="sxs-lookup"><span data-stu-id="398ee-109">Install only the server roles that contain the functionality that you want.</span></span>

<span data-ttu-id="398ee-110">Даже если вы не знакомы с ролями сервера в Lync Server, в средстве планирования вы можете воспользоваться лучшим решением для серверов, которые нужно развернуть, в зависимости от необходимых функций.</span><span class="sxs-lookup"><span data-stu-id="398ee-110">Even if you are not familiar with server roles in Lync Server, the Planning Tool can guide you to the best solution for the servers that you need to deploy, based on the features that you want.</span></span> <span data-ttu-id="398ee-111">В этом разделе представлен краткий обзор ролей сервера и общих функций, которые они предоставляют.</span><span class="sxs-lookup"><span data-stu-id="398ee-111">This section provides a brief overview of the server roles and the general features that they provide:</span></span>

  - <span data-ttu-id="398ee-112">Сервер выпуска Standard Edition</span><span class="sxs-lookup"><span data-stu-id="398ee-112">Standard Edition Server</span></span>

  - <span data-ttu-id="398ee-113">Сервер переднего плана и тыловой сервер</span><span class="sxs-lookup"><span data-stu-id="398ee-113">Front End Server and Back End Server</span></span>

  - <span data-ttu-id="398ee-114">Пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="398ee-114">Edge Server</span></span>

  - <span data-ttu-id="398ee-115">Сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="398ee-115">Mediation Server</span></span>

  - <span data-ttu-id="398ee-116">Директор</span><span class="sxs-lookup"><span data-stu-id="398ee-116">Director</span></span>

  - <span data-ttu-id="398ee-117">Сервер переднего плана сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="398ee-117">Persistent Chat Front End Server</span></span>

  - <span data-ttu-id="398ee-118">Хранилище сохраняемого чата (сохраняемый сервер обратного чата)</span><span class="sxs-lookup"><span data-stu-id="398ee-118">Persistent Chat Store (Persistent Chat Back End Server)</span></span>

  - <span data-ttu-id="398ee-119">Хранилище соответствия требованиям сохраняемого чата (сохраняемый сервер соответствия требованиям к чат)</span><span class="sxs-lookup"><span data-stu-id="398ee-119">Persistent Chat Compliance Store (Persistent Chat Compliance Back End Server)</span></span>

<span data-ttu-id="398ee-120">В целях улучшения масштабируемости и высокой доступности для большинства ролей серверов можно развертывать *пулы*, состоящие из нескольких серверов, на которых запущена одна и та же роль сервера.</span><span class="sxs-lookup"><span data-stu-id="398ee-120">For most server roles, for scalability and high availability you can deploy *pools* of multiple servers all running the same server role.</span></span> <span data-ttu-id="398ee-121">Каждый сервер в пуле должен содержать идентичные роли сервера.</span><span class="sxs-lookup"><span data-stu-id="398ee-121">Each server in a pool must run an identical server role or roles.</span></span> <span data-ttu-id="398ee-122">Для большинства типов пулов в Lync Server необходимо развернуть подсистему балансировки нагрузки, чтобы распределить трафик между различными серверами в пуле.</span><span class="sxs-lookup"><span data-stu-id="398ee-122">For most types of pools in Lync Server, you must deploy a load balancer to spread traffic between the various servers in the pool.</span></span> <span data-ttu-id="398ee-123">Lync Server поддерживает как службу доменных имен (DNS), так и подсистемы балансировки нагрузки для оборудования.</span><span class="sxs-lookup"><span data-stu-id="398ee-123">Lync Server supports both Domain Name System (DNS) load balancing and hardware load balancers.</span></span>

<div>

## <a name="standard-edition-server"></a><span data-ttu-id="398ee-124">Сервер выпуска Standard Edition</span><span class="sxs-lookup"><span data-stu-id="398ee-124">Standard Edition Server</span></span>

<span data-ttu-id="398ee-125">Сервер Standard Edition разработан для малых организаций, а также для пилотных проектов больших организаций.</span><span class="sxs-lookup"><span data-stu-id="398ee-125">The Standard Edition server is designed for small organizations, and for pilot projects of large organizations.</span></span> <span data-ttu-id="398ee-126">Она включает многие возможности Lync Server, в том числе необходимые базы данных, которые можно запускать на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="398ee-126">It enables many of the features of Lync Server, including the necessary databases, to run on a single server.</span></span> <span data-ttu-id="398ee-127">Это позволяет использовать функциональность Lync Server для более ранних расходов, но не предоставляет полноценное решение для высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="398ee-127">This enables you to have Lync Server functionality for a lower cost, but does not provide a true high-availability solution.</span></span>

<span data-ttu-id="398ee-128">Сервер Standard Edition позволяет использовать обмен мгновенными сообщениями, сведения о присутствии, Конференц-связь и корпоративное голосовое приложение на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="398ee-128">Standard Edition server enables you to use instant messaging (IM), presence, conferencing, and Enterprise Voice, all running on one server.</span></span>

<span data-ttu-id="398ee-129">Для решения с высокой степенью доступности используйте Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="398ee-129">For a high-availability solution, use Lync Server Enterprise Edition.</span></span>

</div>

<div>

## <a name="front-end-server-and-back-end-server"></a><span data-ttu-id="398ee-130">Сервер переднего плана и тыловой сервер</span><span class="sxs-lookup"><span data-stu-id="398ee-130">Front End Server and Back End Server</span></span>

<span data-ttu-id="398ee-131">В Lync Server Enterprise Edition сервер переднего плана является основным серверной ролью и выполняет большое количество основных функций Lync Server.</span><span class="sxs-lookup"><span data-stu-id="398ee-131">In Lync Server Enterprise Edition, the Front End Server is the core server role, and runs many basic Lync Server functions.</span></span> <span data-ttu-id="398ee-132">Сервер переднего плана наряду с серверами обратной связи — это единственные роли сервера, необходимые для развертывания Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="398ee-132">The Front End Server, along with the Back End Servers, are the only server roles required to be in any Lync Server Enterprise Edition deployment.</span></span>

<span data-ttu-id="398ee-133">*Пул переднего плана* — это набор серверов переднего плана, настроенных одинаково, совместное использование для предоставления служб для общей группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="398ee-133">A *Front End pool* is a set of Front End Servers, configured identically, that work together to provide services for a common group of users.</span></span> <span data-ttu-id="398ee-134">Пул предоставляет пользователям возможности масштабирования и отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="398ee-134">A pool of multiple servers running the same role provides scalability and failover capability.</span></span>

<span data-ttu-id="398ee-135">Сервер переднего плана предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="398ee-135">The Front End Server includes the following:</span></span>

  - <span data-ttu-id="398ee-136">Проверка подлинности и регистрация пользователей</span><span class="sxs-lookup"><span data-stu-id="398ee-136">User authentication and registration</span></span>

  - <span data-ttu-id="398ee-137">Сведения о присутствии и обмен карточками контактов</span><span class="sxs-lookup"><span data-stu-id="398ee-137">Presence information and contact card exchange</span></span>

  - <span data-ttu-id="398ee-138">Развертывание службы адресной книги и списка рассылки</span><span class="sxs-lookup"><span data-stu-id="398ee-138">Address book services and distribution list expansion</span></span>

  - <span data-ttu-id="398ee-139">Возможности обмена мгновенными сообщениями, в том числе многосторонние конференции</span><span class="sxs-lookup"><span data-stu-id="398ee-139">IM functionality, including multiparty IM conferences</span></span>

  - <span data-ttu-id="398ee-140">Интернет-конференции, одновременная Конференц-связь с телефонным подключением и видеоконференции (если она развернута)</span><span class="sxs-lookup"><span data-stu-id="398ee-140">Web conferencing, PSTN Dial-in conferencing and A/V conferencing (if deployed)</span></span>

  - <span data-ttu-id="398ee-141">Размещение приложений для обоих приложений, входящих в состав Lync Server (например, "участие в конференциях" и "группа ответа"), а сторонние приложения</span><span class="sxs-lookup"><span data-stu-id="398ee-141">Application hosting, for both applications included with Lync Server (for example, Conferencing Attendant and Response Group application), and third-party applications</span></span>

  - <span data-ttu-id="398ee-142">дополнительно: мониторинг для сбора сведений об использовании в форме записей регистрации вызовов и записей ошибок вызовов.</span><span class="sxs-lookup"><span data-stu-id="398ee-142">Optionally, Monitoring, to collect usage information in the form of call detail records (CDRs) and call error records (CERs).</span></span> <span data-ttu-id="398ee-143">Эти сведения содержат метрики о качестве мультимедиа-содержимого (аудио и видео), передаваемого по сети при вызове службы "Корпоративная голосовая связь", а также во время аудио- и видеоконференций;</span><span class="sxs-lookup"><span data-stu-id="398ee-143">This information provides metrics about the quality of the media (audio and video) traversing your network for both Enterprise Voice calls and A/V conferences.</span></span>

  - <span data-ttu-id="398ee-144">веб-компоненты для поддержки веб-задач, таких как веб-планировщик и компонент обеспечения процесса присоединения.</span><span class="sxs-lookup"><span data-stu-id="398ee-144">Web components to supported web-based tasks such as web scheduler and join launcher.</span></span>

  - <span data-ttu-id="398ee-145">дополнительно: архивация как отдельных мгновенных сообщений, так и собраний для соответствия нормативным требованиям.</span><span class="sxs-lookup"><span data-stu-id="398ee-145">Optionally, Archiving, to archive IM communications and meeting content for compliance reasons.</span></span> <span data-ttu-id="398ee-146">Подробности можно найти [в разделе Планирование архивации в Lync Server 2013](lync-server-2013-planning-for-archiving.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="398ee-146">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>
    
    <span data-ttu-id="398ee-147">В Lync Server 2010 и более ранних версиях мониторинг и архивация были разными ролями сервера, которые не могли работать вместе на сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="398ee-147">In Lync Server 2010 and prior versions, Monitoring and Archiving were separate server roles, not collocated on Front End Server.</span></span>

  - <span data-ttu-id="398ee-148">При необходимости, если сохраняемый чат включен, веб-службы сохраняемого чата для управления комнатами чата и веб-службы сохраняемого чата для передачи и загрузки файлов.</span><span class="sxs-lookup"><span data-stu-id="398ee-148">Optionally, if Persistent chat is enabled, Persistent Chat Web Services for Chat Room Management and Persistent Chat Web Services for File Upload/Download.</span></span>

<span data-ttu-id="398ee-p109">Пулы переднего плана – это также основное хранилище для данных пользователей и конференций. Информация о каждом пользователе реплицируется среди трех серверов переднего плана в пуле, а ее резервная копия создается на фоновых серверах.</span><span class="sxs-lookup"><span data-stu-id="398ee-p109">Front End Pools are also the primary store for user and conference data. Information about each user is replicated among three Front End Servers in the pool, and backed up on the Back End Servers.</span></span>

<span data-ttu-id="398ee-151">Кроме того, для одного пула переднего плана в развертывании также запускается *центральный сервер управления*, который управляет и разворачивает основные данные конфигурации для всех серверов, на которых работает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="398ee-151">Additionally, one Front End pool in the deployment also runs the *Central Management Server*, which manages and deploys basic configuration data to all servers running Lync Server.</span></span> <span data-ttu-id="398ee-152">Центральный сервер управления также предоставляет возможности командной консоли Lync Server и передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="398ee-152">The Central Management Server also provides Lync Server Management Shell and file transfer capabilities.</span></span>

<span data-ttu-id="398ee-153">Тыловые серверы — это серверы баз данных, на которых работает Microsoft SQL Server. Они предоставляют службы баз данных для интерфейсного пула.</span><span class="sxs-lookup"><span data-stu-id="398ee-153">The Back End Servers are database servers running Microsoft SQL Server that provide the database services for the Front End pool.</span></span> <span data-ttu-id="398ee-154">Фоновые серверы служат хранилищем резервного копирования для данных пользователей и конференций пула и основным хранилищем для других баз данных, таких как база данных группы ответа.</span><span class="sxs-lookup"><span data-stu-id="398ee-154">The Back End Servers serve as backup stores for the pool’s user and conference data, and are the primary stores for other databases such as the Response Group database.</span></span> <span data-ttu-id="398ee-155">Вы можете использовать один сервер, но решение, в котором используется зеркальное отображение SQL Server, рекомендуется для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="398ee-155">You can have a single Back End Server, but a solution that uses SQL Server mirroring is recommended for failover.</span></span> <span data-ttu-id="398ee-156">Серверные программы Lync Server не работают на серверах с обратной стороны.</span><span class="sxs-lookup"><span data-stu-id="398ee-156">Back End Servers do not run any Lync Server software.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="398ee-157">Мы не рекомендуем выполняйте размещение баз данных Lync Server вместе с другими базами данных.</span><span class="sxs-lookup"><span data-stu-id="398ee-157">We do not recommend collocating Lync Server databases with other databases.</span></span> <span data-ttu-id="398ee-158">В противном случае может пострадать доступность и производительность.</span><span class="sxs-lookup"><span data-stu-id="398ee-158">If you do so, availability and performance may be affected.</span></span>



</div>

<span data-ttu-id="398ee-159">Данные, хранящиеся в базах данных фонового сервера, включают сведения о присутствии, контактные списки пользователей, данные конференций, включая постоянные данные о состоянии всех текущих конференций, а также данные планирования конференций.</span><span class="sxs-lookup"><span data-stu-id="398ee-159">Information stored in the Back End Server databases includes presence information, users' Contacts lists, conferencing data, including persistent data about the state of all current conferences, and conference scheduling data.</span></span>

</div>

<div>

## <a name="edge-server"></a><span data-ttu-id="398ee-160">Пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="398ee-160">Edge Server</span></span>

<span data-ttu-id="398ee-161">Пограничный сервер позволяет пользователям общаться и работать совместно с пользователями за пределами брандмауэров организации.</span><span class="sxs-lookup"><span data-stu-id="398ee-161">Edge Server enables your users to communicate and collaborate with users outside the organization’s firewalls.</span></span> <span data-ttu-id="398ee-162">Эти внешние пользователи могут включать пользователей, которые в настоящее время работают за пределами Организации, и пользователей из организаций федеративных партнеров, а также пользователей, которые были приглашены на участие в конференциях, размещенных на вашем развертывании Lync Server.</span><span class="sxs-lookup"><span data-stu-id="398ee-162">These external users can include the organization’s own users who are currently working offsite, users from federated partner organizations, and outside users who have been invited to join conferences hosted on your Lync Server deployment.</span></span> <span data-ttu-id="398ee-163">Кроме того, пограничный сервер предоставляет возможность подключения к общедоступным службам обмена мгновенными сообщениями, включая Windows Live, AOL, Yahoo \! и Google.</span><span class="sxs-lookup"><span data-stu-id="398ee-163">Edge Server also enables connectivity to public IM connectivity services, including Windows Live, AOL, Yahoo\!, and Google Talk.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="398ee-164">По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="398ee-164">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="398ee-165">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="398ee-165">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="398ee-166">Messenger, пока служба не отключается.</span><span class="sxs-lookup"><span data-stu-id="398ee-166">Messenger until the service shut down date.</span></span> <span data-ttu-id="398ee-167">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="398ee-167">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="398ee-168">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="398ee-168">has been announced.</span></span> <span data-ttu-id="398ee-169">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="398ee-169">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="398ee-170">USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="398ee-170">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="398ee-171">Messenger.</span><span class="sxs-lookup"><span data-stu-id="398ee-171">Messenger.</span></span> <span data-ttu-id="398ee-172">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</span><span class="sxs-lookup"><span data-stu-id="398ee-172">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="398ee-173">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="398ee-173">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="398ee-174">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="398ee-174">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="398ee-175">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="398ee-175">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="398ee-176">Развертывание пограничного сервера также дает возможность использовать службы мобильности, поддерживающие функции Lync на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="398ee-176">Deploying Edge Server also enables mobility services, which supports Lync functionality on mobile devices.</span></span> <span data-ttu-id="398ee-177">Пользователи могут использовать поддерживаемые мобильные устройства на платформе Apple iOS, Android, Windows Phone или Nokia, чтобы выполнять такие действия, как отправка и прием мгновенных сообщений, просмотр контактов и просмотр сведений о присутствии.</span><span class="sxs-lookup"><span data-stu-id="398ee-177">Users can use supported Apple iOS, Android, Windows Phone, or Nokia mobile devices to perform activities such as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="398ee-178">Кроме того, некоторые мобильные устройства поддерживают такие функции службы "Корпоративная голосовая связь", как присоединение к конференции одним щелчком, звонки с рабочего телефона, доступ по одному номеру, голосовая почта и пропущенные звонки.</span><span class="sxs-lookup"><span data-stu-id="398ee-178">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed calls.</span></span> <span data-ttu-id="398ee-179">Функция Mobility также поддерживает *Push-уведомления* для мобильных устройств, которые не поддерживают приложения, работающие в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="398ee-179">The mobility feature also supports *push notifications* for mobile devices that do not support applications running in the background.</span></span> <span data-ttu-id="398ee-180">Push-уведомление — это передаваемое на мобильное устройство уведомление о событии, которое произошло в то время, когда мобильное приложение было неактивно.</span><span class="sxs-lookup"><span data-stu-id="398ee-180">A push notification is a notification that is sent to a mobile device about an event that occurs while a mobile application is inactive.</span></span>

<span data-ttu-id="398ee-181">Пограничные серверы также включают полностью интегрированный прокси-сервер XMPP, при этом шлюз XMPP встроен в серверы переднего плана.</span><span class="sxs-lookup"><span data-stu-id="398ee-181">Edge Servers also include a fully-integrated Extensible Messaging and Presence Protocol (XMPP) proxy, with an XMPP gateway included on Front End Servers.</span></span> <span data-ttu-id="398ee-182">Эти компоненты XMPP можно настроить таким образом, чтобы пользователи Lync Server 2013 могли добавлять контакты из XMPP-партнеров (например, Google чата) для обмена мгновенными сообщениями и их присутствия.</span><span class="sxs-lookup"><span data-stu-id="398ee-182">You can configure these XMPP components to enable your Lync Server 2013 users to add contacts from XMPP-based partners (such as Google Talk) for instant messaging and presence.</span></span>

<span data-ttu-id="398ee-183">Подробности можно найти [в разделе Планирование доступа внешних пользователей в Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="398ee-183">For details, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="mediation-server"></a><span data-ttu-id="398ee-184">Сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="398ee-184">Mediation Server</span></span>

<span data-ttu-id="398ee-185">Сервер-посредник является обязательным компонентом для внедрения корпоративной голосовой связи и конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="398ee-185">Mediation Server is a necessary component for implementing Enterprise Voice and dial-in conferencing.</span></span> <span data-ttu-id="398ee-186">Сервер-посредник переводит сигналы, а также в некоторых конфигурациях, носители между внутренней инфраструктурой сервера Lync и шлюзом КОММУТИРУЕМой телефонной сети, IP-УАТС или SIP.</span><span class="sxs-lookup"><span data-stu-id="398ee-186">Mediation Server translates signaling, and, in some configurations, media between your internal Lync Server infrastructure and a public switched telephone network (PSTN) gateway, IP-PBX, or a Session Initiation Protocol (SIP) trunk.</span></span> <span data-ttu-id="398ee-187">Сервер-посредник может работать на одном компьютере с сервером переднего плана или может быть выделен в отдельный пул серверов-посредников.</span><span class="sxs-lookup"><span data-stu-id="398ee-187">You can run Mediation Server collocated on the same server as Front End Server, or separated into a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="398ee-188">Подробности можно найти [в разделе Сервер исправлений в Lync server 2013](lync-server-2013-mediation-server-component.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="398ee-188">For details, see [Mediation Server component in Lync Server 2013](lync-server-2013-mediation-server-component.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="398ee-189">Директор</span><span class="sxs-lookup"><span data-stu-id="398ee-189">Director</span></span>

<span data-ttu-id="398ee-190">Режиссеры могут проверять подлинность запросов пользователей Lync Server, но они не являются домашними учетными записями пользователей или предоставляют услуги по обеспечению присутствия или конференции.</span><span class="sxs-lookup"><span data-stu-id="398ee-190">Directors can authenticate Lync Server user requests, but they do not home user accounts or provide presence or conferencing services.</span></span> <span data-ttu-id="398ee-191">Директоры оказываются особенно полезными при необходимости повышения уровня безопасности в развертываниях, где необходим доступ внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="398ee-191">Directors are most useful to enhance security in deployments that enable external user access.</span></span> <span data-ttu-id="398ee-192">Директор может выполнять проверку подлинности запросов, прежде чем передавать эти запросы на внутренние серверы.</span><span class="sxs-lookup"><span data-stu-id="398ee-192">The Director can authenticate requests before sending them on to internal servers.</span></span> <span data-ttu-id="398ee-193">При начале атак по принципу отказа в обслуживании атаки заканчиваются на директоре и не достигают серверов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="398ee-193">In the case of a denial-of-service attack, the attack ends with the Director and does not reach the Front End servers.</span></span> <span data-ttu-id="398ee-194">Дополнительные сведения можно найти в разделе [сценарии для режиссера в Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="398ee-194">For details, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="persistent-chat-server-roles"></a><span data-ttu-id="398ee-195">Роли серверов сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="398ee-195">Persistent Chat Server Roles</span></span>

<span data-ttu-id="398ee-p121">Возможности сохраняемого чата позволяют пользователям участвовать в многопользовательских тематических беседах, которые подлежат сохранению. На сервере переднего плана сохраняемого чата работает служба сохраняемого чата. Внутренний сервер сохраняемого чата хранит данные журнала бесед и сведения о категориях и комнатах чата. Дополнительный внутренний сервер сохраняемого чата для соответствия требованиям может хранить содержимое чата и события соответствия, которые будут использоваться для обеспечения соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="398ee-p121">Persistent chat enables users to participate in multiparty, topic-based conversations that persist over time. The Persistent Chat Front End Server runs the persistent chat service. The Persistent Chat Back End Server stores the chat history data, and information about categories and chat rooms. The optional Persistent Chat Compliance Back End Server can store the chat content and compliance events for the purpose of compliance.</span></span>

<span data-ttu-id="398ee-200">Серверы, на которых работает Lync Server Standard Edition, также могут запускать сохраняемый чат, размещенный на одном и том же сервере.</span><span class="sxs-lookup"><span data-stu-id="398ee-200">Servers running Lync Server Standard Edition can also run Persistent chat collocated on the same server.</span></span> <span data-ttu-id="398ee-201">Сервер переднего плана для сохраняемого чата невозможно размещать совместно с сервером переднего плана Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="398ee-201">You cannot collocate the Persistent Chat Front End Server with Enterprise Edition Front End Server.</span></span>

<span data-ttu-id="398ee-202">Подробные сведения можно найти [в разделе Планирование сохраняемого сервера чата в Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="398ee-202">For details, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="398ee-203">См. также</span><span class="sxs-lookup"><span data-stu-id="398ee-203">See Also</span></span>


[<span data-ttu-id="398ee-204">Компонент сервера «исправления» в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="398ee-204">Mediation Server component in Lync Server 2013</span></span>](lync-server-2013-mediation-server-component.md)  


[<span data-ttu-id="398ee-205">Планирование архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="398ee-205">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
[<span data-ttu-id="398ee-206">Планирование доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="398ee-206">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)  
[<span data-ttu-id="398ee-207">Сценарии для директора в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="398ee-207">Scenarios for the Director in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-the-director.md)  
[<span data-ttu-id="398ee-208">Планирование сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="398ee-208">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
  

<span data-ttu-id="398ee-209"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="398ee-209"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

