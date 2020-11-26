---
title: 'Lync Server 2013: отчеты об использовании системы'
description: 'Lync Server 2013: отчеты об использовании системы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: System usage reports
ms:assetid: 187d316d-2456-417e-b636-05527a18ef06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558618(v=OCS.15)
ms:contentKeyID: 48183529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6fffaf22dacbc68958e64090fd4c7d44e32f8ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423556"
---
# <a name="system-usage-reports-in-lync-server-2013"></a><span data-ttu-id="040b3-103">Отчеты об использовании системы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-103">System usage reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="040b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="040b3-104">

<span> </span></span></span>

<span data-ttu-id="040b3-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="040b3-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="040b3-106">Отчеты об использовании системы предоставляют сведения об использовании системы на основе данных записи сведений о вызовах (CDR), собранных сервером Lync.</span><span class="sxs-lookup"><span data-stu-id="040b3-106">The System Usage Reports provide system usage information based on call detail recording (CDR) data collected by the Lync Server.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="040b3-107">Содержание</span><span class="sxs-lookup"><span data-stu-id="040b3-107">In This Section</span></span>

  - [<span data-ttu-id="040b3-108">Отчет о регистрации пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-108">User Registration Report in Lync Server 2013</span></span>](lync-server-2013-user-registration-report.md)
    
    <span data-ttu-id="040b3-109">Общие сведения о подключении пользователей к развертыванию Lync Server 2013 на основе событий регистрации, например входов пользователей.</span><span class="sxs-lookup"><span data-stu-id="040b3-109">Provides a summary of user connectivity to the Lync Server 2013 deployment based on registration events such as user logons.</span></span> <span data-ttu-id="040b3-110">В отчете представлен способ просмотра как внутренних, так и внешних входов, а также для сравнения числа пользователей, которые вошли в Lync Server 2013 с учетом количества пользователей, которые действительно использовали эту службу, пока они были зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="040b3-110">The report provides a way to view both internal and external logons, and to compare the number of users who logged on to Lync Server 2013 with the number of users who actually used the service while they were logged on.</span></span>

  - [<span data-ttu-id="040b3-111">Сводный отчет о действиях одноранговых узлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-111">Peer-to-Peer Activity Summary Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-summary-report.md)
    
    <span data-ttu-id="040b3-p102">Содержит сводку по одноранговым мгновенным сообщениям, аудио- и видеовызовам, передаче файлов и сеансам совместного использования приложений. Одноранговые сеансы – это сеансы с участием всего двух пользователей.</span><span class="sxs-lookup"><span data-stu-id="040b3-p102">Provides a summary of peer-to-peer instant messaging (IM), audio, video, file transfer, and application sharing sessions. Peer-to-peer sessions are sessions involving just two users.</span></span>

  - [<span data-ttu-id="040b3-114">Сводный отчет о конференциях в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-114">Conference Summary Report in Lync Server 2013</span></span>](lync-server-2013-conference-summary-report.md)
    
    <span data-ttu-id="040b3-115">Сводка по всем действиям, связанным с конференциями.</span><span class="sxs-lookup"><span data-stu-id="040b3-115">Provides a summary of all conference activities.</span></span> <span data-ttu-id="040b3-116">Конференции – это сеансы с участием трех или более пользователей.</span><span class="sxs-lookup"><span data-stu-id="040b3-116">Conferences are sessions involving three or more people.</span></span>

  - [<span data-ttu-id="040b3-117">Сводный отчет о конференции по PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-117">PSTN Conference Summary Report in Lync Server 2013</span></span>](lync-server-2013-pstn-conference-summary-report.md)
    
    <span data-ttu-id="040b3-p104">Сводка по всем конференциям ТСОП. Это конференции, к которым хотя бы один пользователь подключается по телефонной сети общего пользования (ТСОП) (т.н. *конференц-связь с телефонным подключением*).</span><span class="sxs-lookup"><span data-stu-id="040b3-p104">Provides a summary of all PSTN conferences. These are conferences where at least one user dials in using the public switched telephone network (PSTN), which is also referred to as *dial-in conferencing*.</span></span>

  - [<span data-ttu-id="040b3-120">Отчет об использовании группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-120">Response Group Usage Report in Lync Server 2013</span></span>](lync-server-2013-response-group-usage-report.md)
    
    <span data-ttu-id="040b3-121">Общие сведения об использовании групп ответов.</span><span class="sxs-lookup"><span data-stu-id="040b3-121">Provides a summary of Response Group usage.</span></span> <span data-ttu-id="040b3-122">Приложение "группа ответа" дает возможность автоматически перенаправлять телефонные звонки в такие сущности, как служба поддержки пользователей или линия обслуживания клиентов.</span><span class="sxs-lookup"><span data-stu-id="040b3-122">The Response Group application provides a way for you to automatically route phone calls to entities such as a help desk or customer support line.</span></span>

  - [<span data-ttu-id="040b3-123">Отчет о запасах IP-телефона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-123">IP Phone Inventory Report in Lync Server 2013</span></span>](lync-server-2013-ip-phone-inventory-report.md)
    
    <span data-ttu-id="040b3-124">Сведения об IP-телефонах, которые в настоящее время используются в Организации.</span><span class="sxs-lookup"><span data-stu-id="040b3-124">Provides information about the IP phones currently in use in the organization.</span></span> <span data-ttu-id="040b3-125">Отчет основывается на регистрации и входах в телефон.</span><span class="sxs-lookup"><span data-stu-id="040b3-125">The report is based on phone registrations and logons.</span></span> <span data-ttu-id="040b3-126">Его не следует рассматривать как полную инвентаризацию.</span><span class="sxs-lookup"><span data-stu-id="040b3-126">It should not be considered a complete inventory.</span></span> <span data-ttu-id="040b3-127">Например, возможно, вы удалили телефоны, которые еще не указаны в отчете, так как они вошли как минимум один раз.</span><span class="sxs-lookup"><span data-stu-id="040b3-127">For example, you might have removed phones that are still listed in the report because they logged on at least once.</span></span> <span data-ttu-id="040b3-128">Кроме того, вы также можете использовать новые телефоны, которые не отображаются в отчете, просто потому, что пользователи еще не выполнили вход на Lync Server с новыми телефонами.</span><span class="sxs-lookup"><span data-stu-id="040b3-128">Likewise, you might also have new phones that do not show up in the report simply because users have not logged on to Lync Server with their new phones yet.</span></span>

  - [<span data-ttu-id="040b3-129">Отчет по контролю за допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b3-129">Call Admission Control Report in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-report.md)
    
    <span data-ttu-id="040b3-p107">Предоставляет список действий с одноранговыми сеансами и конференциями, которые используют контроль допуска звонков. Контроль допуска звонков (CAC) позволяет определить, следует ли разрешить сеансы общения в реальном времени, например голосовые или видеовызовы, на основе ограничения пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="040b3-p107">Provides a list of peer-to-peer and conference activities that use call admission control. Call admission control (CAC) is a way of determining whether you should allow real-time communications sessions, such as voice or video calls, based on bandwidth constraints.</span></span>

<span data-ttu-id="040b3-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="040b3-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

