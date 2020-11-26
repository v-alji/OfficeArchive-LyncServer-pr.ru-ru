---
title: 'Lync Server 2013: советы и рекомендации для вашей базовой инфраструктуры'
description: 'Lync Server 2013: советы и рекомендации для вашей базовой инфраструктуры.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for your core infrastructure in Lync Server 2013
ms:assetid: 44aff88d-536c-4613-a81e-5398c9c6a648
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518328(v=OCS.15)
ms:contentKeyID: 61071242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0ea7cb9c7685a3b6f7c04146ec5631bbac10fe6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436043"
---
# <a name="best-practices-for-your-core-infrastructure-in-lync-server-2013"></a><span data-ttu-id="0dd7d-103">Рекомендации для базовой инфраструктуры в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0dd7d-103">Best practices for your core infrastructure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0dd7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0dd7d-104">

<span> </span></span></span>

<span data-ttu-id="0dd7d-105">_**Тема последнего изменения:** 2014-01-27_</span><span class="sxs-lookup"><span data-stu-id="0dd7d-105">_**Topic Last Modified:** 2014-01-27_</span></span>

<span data-ttu-id="0dd7d-106">Возможно, вы уже выполнили действия по проектированию отказоустойчивости вашей системы, применяя такие меры, как аппаратное резервирование, защита от потери напряжения питания, регулярная установка обновлений системы безопасности и использование средств защиты от вирусов, а также запуск сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-106">You have probably already taken steps to design fault tolerance in your system, using practices such as ensuring hardware redundancy, guarding against power loss, routinely installing security updates and antivirus measures, and Monitoring Server activity.</span></span> <span data-ttu-id="0dd7d-107">Эти рекомендации повышают эффективность не только вашей инфраструктуры Microsoft Lync Server 2013, но и всей сети.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-107">These practices benefit not only your Microsoft Lync Server 2013 infrastructure, but also your entire network.</span></span> <span data-ttu-id="0dd7d-108">Если вы не реализовали эти рекомендации, рекомендуем сделать это перед развертыванием Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-108">If you have not implemented these practices, we recommend that you do so before deploying Lync Server 2013.</span></span>

<span data-ttu-id="0dd7d-109">Чтобы защитить серверы в среде Lync Server 2013 от случайного или целенаправленнаяового ущерба, которое может привести к простою, примите следующие меры предосторожности.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-109">To help protect the servers in your Lync Server 2013 deployment from accidental or purposeful harm that might result in downtime, take the following precautions:</span></span>

  - <span data-ttu-id="0dd7d-110">Обновляйте свои серверы с помощью обновлений для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-110">Keep your servers up-to-date with security updates.</span></span> <span data-ttu-id="0dd7d-111">Подписка на Microsoft Security Notification Service гарантирует получение немедленного уведомления о выпусках бюллетеней безопасности для любого продукта Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-111">Subscribing to the Microsoft Security Notification Service helps ensure that you receive immediate notification of security bulletin releases for any Microsoft product.</span></span> <span data-ttu-id="0dd7d-112">Чтобы подписаться на подписку, перейдите на веб-сайт уведомлений Майкрософт по технической безопасности [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202) .</span><span class="sxs-lookup"><span data-stu-id="0dd7d-112">To subscribe, go to the Microsoft Technical Security Notifications website at [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202).</span></span>

  - <span data-ttu-id="0dd7d-113">Убедитесь, что настройка прав доступа выполнена правильно.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-113">Ensure that access rights are set up correctly.</span></span>

  - <span data-ttu-id="0dd7d-p103">Ваши серверы должны быть установлены в помещениях, исключающих несанкционированный доступ. Установите надежное антивирусное программное обеспечение на всех ваших серверах. Регулярно обновляйте файлы сигнатур вирусов антивирусного программного обеспечения. Для обеспечения актуальности файлов сигнатур вирусов активируйте функцию автоматического обновления в вашем антивирусном программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-p103">Keep your servers in a physical environment that prevents unauthorized access. Ensure that adequate antivirus software is installed on all your servers. Keep the software up-to-date with the latest virus signature files. Use the automatic update feature of your antivirus application to keep the virus signatures current.</span></span>

  - <span data-ttu-id="0dd7d-118">Мы рекомендуем отключить службы операционной системы Windows Server, которые не требуются на компьютерах, на которых вы установили Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-118">We recommend that you disable the Windows Server operating system services that are not required on the computers where you install Lync Server 2013.</span></span>

  - <span data-ttu-id="0dd7d-119">Зашифруйте операционные системы и дисковые устройства, на которых хранятся данные, с помощью полнодисковой системы шифрования, если вы не можете обеспечить постоянное и всестороннее управление серверами, их полную физическую изоляцию, а также надлежащий и безопасный вывод из эксплуатации замененных или отказавших дисковых устройств.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-119">Encrypt operating systems and disk drives where data is stored with a full-volume encryption system, unless you can guarantee constant and complete control of the servers, total physical isolation, and proper and secure decommissioning of replaced or failed disk drives.</span></span>

  - <span data-ttu-id="0dd7d-120">Отключите на серверах все внешние порты прямого доступа к памяти (DMA), если вы не можете гарантировать жесткий контроль за физическим доступом к серверам.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-120">Disable all external Direct Memory Access (DMA) ports of the server, unless you can guarantee very tight control over the physical access to the servers.</span></span> <span data-ttu-id="0dd7d-121">С помощью атак посредством прямого доступа к памяти, организовать которые достаточно просто, можно получить доступ к таким важным данным, как закрытые ключи шифрования.</span><span class="sxs-lookup"><span data-stu-id="0dd7d-121">DMA-based attacks, which can be initiated fairly easily, could expose very sensitive information, such as private encryption keys.</span></span>

<span data-ttu-id="0dd7d-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0dd7d-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

