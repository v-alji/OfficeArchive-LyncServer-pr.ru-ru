---
title: 'Lync Server 2013: настройка Lync Server для маршрутизации к шлюзу SIP/CSTA'
description: 'Lync Server 2013: Настройка сервера Lync Server для маршрутизации на шлюз SIP/CSTA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Lync Server 2013 to route to a SIP/CSTA gateway
ms:assetid: d75e4cf6-7b36-430a-a91a-0f2559306ba1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615038(v=OCS.15)
ms:contentKeyID: 48185605
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 777bcf36e6d36fc7a86b6b40460a376390dbdf01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432970"
---
# <a name="configuring-lync-server-2013-to-route-to-a-sipcsta-gateway"></a><span data-ttu-id="0b096-103">Настройка Lync Server 2013 для маршрутизации к шлюзу SIP/CSTA</span><span class="sxs-lookup"><span data-stu-id="0b096-103">Configuring Lync Server 2013 to route to a SIP/CSTA gateway</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b096-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b096-104">

<span> </span></span></span>

<span data-ttu-id="0b096-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="0b096-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="0b096-106">Шлюз SIP/CSTA — это шлюз между SIP и коммуникационной программой, поддерживаемой компьютером (CSTA).</span><span class="sxs-lookup"><span data-stu-id="0b096-106">A SIP/CSTA gateway is a gateway between SIP and a computer-supported telecommunications application (CSTA).</span></span> <span data-ttu-id="0b096-107">Шлюз SIP/CSTA предоставляет интерфейс между существующим частным обменом филиалов (УАТС) и Lync Server для маршрутизации запросов на управление удаленными звонками в УАТС.</span><span class="sxs-lookup"><span data-stu-id="0b096-107">A SIP/CSTA gateway provides the interface between an existing private branch exchange (PBX) and Lync Server for routing remote call control requests to the PBX.</span></span> <span data-ttu-id="0b096-108">После установки шлюза SIP/CSTA необходимо выполнить описанные ниже действия в каждом пуле серверов Lync, для которого вы хотите настроить удаленное управление звонками.</span><span class="sxs-lookup"><span data-stu-id="0b096-108">After you install a SIP/CSTA gateway, you must perform the following procedures on each Lync Server pool for which you want to configure remote call control:</span></span>

  - [<span data-ttu-id="0b096-109">Настройка статического маршрута для дистанционного управления вызовами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b096-109">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)

  - [<span data-ttu-id="0b096-110">Настройка записи доверенного приложения для удаленного управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b096-110">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)

<span data-ttu-id="0b096-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b096-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

