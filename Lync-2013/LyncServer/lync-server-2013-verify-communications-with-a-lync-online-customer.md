---
title: 'Lync Server 2013: Проверка связи с клиентом Lync Online'
description: 'Lync Server 2013: Проверка связи с клиентом Lync Online.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify communications with a Lync Online customer
ms:assetid: c8287b15-e1bb-4b26-8354-0ec90b2fcfe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202189(v=OCS.15)
ms:contentKeyID: 48185378
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 867b0f7ffffd563c869b9bcd5443a3cb91b156af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399802"
---
# <a name="verify-communications-with-a-lync-online-customer-in-lync-server-2013"></a><span data-ttu-id="08d87-103">Проверка связи с клиентом Lync Online в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="08d87-103">Verify communications with a Lync Online customer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="08d87-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="08d87-104">

<span> </span></span></span>

<span data-ttu-id="08d87-105">_**Тема последнего изменения:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="08d87-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="08d87-106">Чтобы разрешить пользователям Lync в организации взаимодействовать с пользователями Microsoft Lync Online 2010, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="08d87-106">To enable Lync users in your organization to communicate with users of a Microsoft Lync Online 2010 customer, you must have completed the following steps:</span></span>

  - <span data-ttu-id="08d87-107">Выполнены все необходимые условия.</span><span class="sxs-lookup"><span data-stu-id="08d87-107">Met all prerequisites.</span></span> <span data-ttu-id="08d87-108">Сюда входит развертывание внутренних и пограничных серверов, включение поддержки федерации для Организации и Настройка учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="08d87-108">This includes deploying your internal and edge servers, enabling federation support for your organization, and setting up user accounts.</span></span> <span data-ttu-id="08d87-109">Дополнительные сведения можно найти [в разделе Предварительные требования для Федерации с клиентом Lync Online в Lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md).</span><span class="sxs-lookup"><span data-stu-id="08d87-109">For details, see [Prerequisites for federating with a Lync Online customer in Lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md).</span></span>

  - <span data-ttu-id="08d87-110">Настройка поддержки доступа к доменам во внутренней среде.</span><span class="sxs-lookup"><span data-stu-id="08d87-110">Configured domain access support in your internal deployment.</span></span> <span data-ttu-id="08d87-111">Сюда входит создание записи поставщика узла и Настройка развертывания для разрешения доступа из домена клиента Lync Online.</span><span class="sxs-lookup"><span data-stu-id="08d87-111">This includes creating a host provider entry and configuring your deployment to allow access from the Lync Online customer’s domain.</span></span> <span data-ttu-id="08d87-112">Подробности можно найти [в разделе Настройка поддержки федерации для домена Lync Online в Lync Server 2013](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md).</span><span class="sxs-lookup"><span data-stu-id="08d87-112">For details, see [Configure federation support for a Lync Online domain in Lync Server 2013](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md).</span></span>

  - <span data-ttu-id="08d87-113">Настройка учетных записей пользователей для поддержки Федерации.</span><span class="sxs-lookup"><span data-stu-id="08d87-113">Configured your user accounts to support federation.</span></span> <span data-ttu-id="08d87-114">Подробности можно найти [в разделе Настройка доступа пользователей к интеграции с клиентом Lync Online в Lync Server 2013](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md).</span><span class="sxs-lookup"><span data-stu-id="08d87-114">For details, see [Configure user access for federation with a Lync Online customer in Lync Server 2013](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md).</span></span>

<span data-ttu-id="08d87-115">После выполнения всех этих действий и администратором пользователя Lync Online 2010 завершается вся настройка интернет-служб для поддержки Федерации с вашей организацией, проверка связи путем проверки связи между внутренним пользователем в Организации и пользователем клиента Lync Online.</span><span class="sxs-lookup"><span data-stu-id="08d87-115">After you complete all of these steps and the administrator of the Lync Online 2010 customer completes all configuration of their online services to support federation with your organization, verify communications by testing communications between an internal user in your organization and a user of the Lync Online customer.</span></span> <span data-ttu-id="08d87-116">Если связь не была успешной, для устранения проблемы используйте средство ведения журналов из пограничного сервера для захвата файлов журнала и трассировки.</span><span class="sxs-lookup"><span data-stu-id="08d87-116">If communication is not successful, use the Logging Tool from your Edge Server to capture log and trace files in order to troubleshoot the problem.</span></span> <span data-ttu-id="08d87-117">Подробнее об использовании средства ведения журнала можно найти в разделе [Открытие средства администрирования Lync Server 2013](lync-server-2013-open-lync-server-administrative-tools.md) в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="08d87-117">For details about using the Logging Tool, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md) in the Operations documentation.</span></span> <span data-ttu-id="08d87-118">Подробные сведения о средстве ведения журнала можно найти в документации по средству ведения журнала Lync Server 2010 в библиотеке TechNet по адресу [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265) .</span><span class="sxs-lookup"><span data-stu-id="08d87-118">For details about the Logging Tool, see the Lync Server 2010 Logging Tool documentation on the TechNet Library at [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265).</span></span>

<span data-ttu-id="08d87-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="08d87-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

