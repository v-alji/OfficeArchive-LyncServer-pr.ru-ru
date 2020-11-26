---
title: 'Lync Server 2013: планирование конференц-связи'
description: 'Lync Server 2013: планирование конференций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for conferencing
ms:assetid: 983a272a-e1b3-4d70-8f84-836b092fe526
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398781(v=OCS.15)
ms:contentKeyID: 48184937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28e71d185b7be8971c451351aac60dcaaf7eaeda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443022"
---
# <a name="planning-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="1d63d-103">Планирование конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d63d-103">Planning for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d63d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d63d-104">

<span> </span></span></span>

<span data-ttu-id="1d63d-105">_**Тема последнего изменения:** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="1d63d-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="1d63d-106">Lync Server 2013 имеет широкий набор возможностей для конференц-связи:</span><span class="sxs-lookup"><span data-stu-id="1d63d-106">Lync Server 2013 offers a rich set of conferencing capabilities:</span></span>

  - <span data-ttu-id="1d63d-107">Веб-конференции, в том числе взаимодействие с документами, общий доступ к приложениям и совместный доступ к рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="1d63d-107">Web conferencing, which includes document collaboration, application sharing, and desktop sharing.</span></span> <span data-ttu-id="1d63d-108">Lync Server 2013 использует Office Web Apps и сервер Office Web Apps для обработки общего просмотра и отрисовки презентаций PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="1d63d-108">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="1d63d-109">Подробнее об установке и настройке сервера Office Web Apps можно узнать в разделе [Настройка интеграции с Office Web Apps Server и Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="1d63d-109">For details about installing and configuring the Office Web Apps Server, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

  - <span data-ttu-id="1d63d-110">Голосовая или видеосвязь (A/V), позволяющая пользователям использовать голосовые и видеоконференции в реальном времени, не требуя использования внешних служб, таких как служба Microsoft Live Meeting или независимый звуковой мост.</span><span class="sxs-lookup"><span data-stu-id="1d63d-110">Audio/video (A/V) conferencing, which enables users to have real-time audio or video conferences without the need for external services such as the Microsoft Live Meeting service or a third-party audio bridge.</span></span>

  - <span data-ttu-id="1d63d-111">Конференц-связь с телефонным подключением, благодаря которой пользователи могут присоединиться к звуковой части конференции Lync Server 2013 с помощью коммутируемого телефона с коммутируемой телефонной сетью, не требуя от стороннего поставщика услуг голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="1d63d-111">Dial-in conferencing, which allows users to join the audio portion of a Lync Server 2013 conference by using a public switched telephone network (PSTN) phone without requiring a third-party audio conferencing provider.</span></span>

  - <span data-ttu-id="1d63d-112">Конференц-связь с помощью мгновенных сообщений, в которой более двух сторон обмениваются данными в одном сеансе обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1d63d-112">Instant messaging (IM) conferencing, in which more than two parties communicate in a single IM session.</span></span> <span data-ttu-id="1d63d-113">Подробные сведения о конференц-связи можно найти [в разделе Планирование серверов переднего плана, обмена мгновенными сообщениями и сведений о присутствии в Lync Server 2013](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="1d63d-113">For details about IM conferencing, see [Planning for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<span data-ttu-id="1d63d-114">Lync Server 2013 поддерживает как запланированные конференции, так и конференции незапланированное.</span><span class="sxs-lookup"><span data-stu-id="1d63d-114">Lync Server 2013 supports both scheduled conferences and impromptu conferences.</span></span>

<span data-ttu-id="1d63d-115">При развертывании Lync Server 2013, сервер переднего плана вы можете выбрать, следует ли также развертывать веб-конференции, Конференции и возможности конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="1d63d-115">When you deploy Lync Server 2013, Front End Server, you can choose whether to also deploy the web conferencing, A/V conferencing, and dial-in conferencing capabilities.</span></span> <span data-ttu-id="1d63d-116">Возможности конференц-связи с СООБЩЕНИЯми всегда развертываются автоматически вместе с возможностями обмена мгновенными сообщениями на серверах переднего плана Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1d63d-116">IM conferencing capabilities are always automatically deployed along with IM conversation capabilities on Lync Server 2013 Front End Servers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1d63d-117">Если в развертывании есть собрания, упорядоченные с помощью клиентов Office Communicator 2007 R2 (включая консоль Live Meeting или надстройка конференц-связи для Microsoft Office Outlook), после миграции на Lync Server 2013 эти ограничения будут заключаться в указанных ниже случаях.</span><span class="sxs-lookup"><span data-stu-id="1d63d-117">If your deployment includes meetings organized using Office Communicator 2007 R2 clients (including the Live Meeting console or Conferencing Add-in for Microsoft Office Outlook), the meetings will have the following limitations after they are migrated to Lync Server 2013:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="1d63d-118">Пользователи на собрании не смогут использовать возможности совместной работы с данными, в том числе совместную работу с документами, общий доступ к приложениям и совместный доступ к рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="1d63d-118">Users in the meeting will not be able to use data collaboration features, including document collaboration, application sharing, and desktop sharing.</span></span></P>
> <LI>
> <P><span data-ttu-id="1d63d-119">Проблемы с стабильностью могут возникать, так как клиенты Office Communicator 2007 R2 не поддерживаются в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1d63d-119">Stability issues may arise since Office Communicator 2007 R2 clients are not supported with Lync Server 2013.</span></span></P></LI></UL><span data-ttu-id="1d63d-120">Чтобы избежать этих проблем, измените расписание собраний, упорядоченных на клиентах Office Communicator 2007 R2 с помощью Outlook 2010 или Outlook 2013, с помощью надстройки "собрание по сети" для Lync 2010 или для собрания по сети для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="1d63d-120">To avoid these issues, reschedule any meeting organized using Office Communicator 2007 R2 clients with Outlook 2010 or Outlook 2013 using either the Online Meeting Add-in for Lync 2010 or Online Meeting Add-in for Lync 2013.</span></span>



</div>

<span data-ttu-id="1d63d-121">В следующих разделах описаны вопросы, необходимые для развертывания различных типов возможностей Конференции, включая процесс планирования, компоненты, требования к оборудованию и программному обеспечению, а также процесс развертывания.</span><span class="sxs-lookup"><span data-stu-id="1d63d-121">The following sections describe what is required to deploy the various types of conferencing capabilities, including the planning process, components, hardware and software requirements, and the deployment process.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1d63d-122">Содержание</span><span class="sxs-lookup"><span data-stu-id="1d63d-122">In This Section</span></span>

  - [<span data-ttu-id="1d63d-123">Обзор конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d63d-123">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)

  - [<span data-ttu-id="1d63d-124">Определение требований для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d63d-124">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)

  - [<span data-ttu-id="1d63d-125">Компоненты и топологии для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d63d-125">Components and topologies for conferencing in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-conferencing.md)

  - [<span data-ttu-id="1d63d-126">Технические требования для проведения конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d63d-126">Technical requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-conferencing.md)

  - [<span data-ttu-id="1d63d-127">Контрольный список развертывания для конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d63d-127">Deployment checklist for conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-conferencing.md)

  - [<span data-ttu-id="1d63d-128">Поддержка больших собраний в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d63d-128">Support for large meetings in Lync Server 2013</span></span>](lync-server-2013-support-for-large-meetings.md)

<span data-ttu-id="1d63d-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d63d-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

