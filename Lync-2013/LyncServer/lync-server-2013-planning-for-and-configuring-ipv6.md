---
title: 'Lync Server 2013: планирование и настройка IPv6'
description: 'Lync Server 2013: планирование и настройка IPv6.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for and configuring IPv6
ms:assetid: 01f77196-38f4-4292-9480-2e2fbd57eabe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204624(v=OCS.15)
ms:contentKeyID: 48183236
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c63268bd92fc9d3b683cfa05ab49f01ea56d6ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398455"
---
# <a name="planning-for-and-configuring-ipv6-in-lync-server-2013"></a><span data-ttu-id="ce3a0-103">Планирование и настройка IPv6 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce3a0-103">Planning for and configuring IPv6 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce3a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce3a0-104">

<span> </span></span></span>

<span data-ttu-id="ce3a0-105">_**Тема последнего изменения:** 2012-06-14_</span><span class="sxs-lookup"><span data-stu-id="ce3a0-105">_**Topic Last Modified:** 2012-06-14_</span></span>

<span data-ttu-id="ce3a0-106">Lync Server 2013 включает поддержку адресов IP версии 6 (IPv6) и продолжает поддерживать IP-адреса версии 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="ce3a0-106">Lync Server 2013 includes support for IP version 6 (IPv6) addresses, along with continued support of IP version 4 (IPv4) addresses.</span></span> <span data-ttu-id="ce3a0-107">Адреса IPv4 — 32-разрядные адреса, которые позволяют компьютеру осуществлять взаимодействие через Интернет.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-107">IPv4 addresses are 32-bit addresses that allow a computer to communicate over the Internet.</span></span> <span data-ttu-id="ce3a0-108">Из-за роста количества устройств во всем мире, доступные адреса IPv4 истекает. По этой причине многие новые устройства переходят на использование IPv6-адресов.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-108">Due to the increasing number of devices worldwide, the available IPv4 addresses have run out. Because of this, many new devices are moving to using IPv6 addresses.</span></span> <span data-ttu-id="ce3a0-109">Адреса IPv6 выполняют ту же задачу, что и адреса IPv4 (с некоторыми дополнительными возможностями), но вместо использования 32 бит в адресах IPv6 используется 128 бит.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-109">IPv6 addresses perform the same function as IPv4 addresses (with some additional features), but instead of using only 32-bits, IPv6 addresses use 128-bits.</span></span> <span data-ttu-id="ce3a0-110">Это не только предоставляет новый набор адресов, но существенно увеличивает их количество.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-110">This provides not only a new set of addresses, but also a much larger number of them.</span></span> <span data-ttu-id="ce3a0-111">Типичный адрес IPv4 выглядит следующим образом: 192.0.2.235, в то время как адрес IPv6 выглядит следующим образом: 2001:0db8:85a3:0000:0000:8a2e:0370:7334.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-111">A typical IPv4 address looks something like this: 192.0.2.235, whereas an IPv6 address looks like this: 2001:0db8:85a3:0000:0000:8a2e:0370:7334.</span></span> <span data-ttu-id="ce3a0-112">Изменение форматирования и функциональных возможностей для устройств, использующих IPv6-адреса, требует некоторых вопросов развертывания и настройки в установке Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-112">The change in formatting and functionality for devices that use IPv6 addresses requires several deployment and configuration considerations in your Lync Server 2013 installation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ce3a0-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="ce3a0-113">In This Section</span></span>

  - [<span data-ttu-id="ce3a0-114">Обзор типов IP-адресов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce3a0-114">Overview of IP address types for Lync Server 2013</span></span>](lync-server-2013-overview-of-ip-address-types.md)

  - [<span data-ttu-id="ce3a0-115">Технические требования к IPv6 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce3a0-115">Technical requirements for IPv6 in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-ipv6.md)

  - [<span data-ttu-id="ce3a0-116">Вопросы миграции и сосуществования для IPv6 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce3a0-116">Migration and coexistence considerations for IPv6 in Lync Server 2013</span></span>](lync-server-2013-migration-and-coexistence-considerations-for-ipv6.md)

  - [<span data-ttu-id="ce3a0-117">Настройка типов IP-адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce3a0-117">Configure IP address types in Lync Server 2013</span></span>](lync-server-2013-configure-ip-address-types.md)

<span data-ttu-id="ce3a0-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce3a0-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

