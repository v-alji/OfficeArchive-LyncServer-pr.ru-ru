---
title: 'Lync Server 2013: развертывание типов IP-адресов на сервере переднего плана'
description: 'Lync Server 2013: развертывание типов IP-адресов на сервере переднего плана.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy IP address types on a Front End Server
ms:assetid: b6c8e0f9-ec8e-4a4e-a525-756f9cd6b9d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205191(v=OCS.15)
ms:contentKeyID: 48185193
ms.date: 07/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57d27cbc6ae23af1f15e28b19e1871c0aaf35dde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430267"
---
# <a name="deploy-ip-address-types-on-a-front-end-server-for-lync-server-2013"></a><span data-ttu-id="17ff4-103">Развертывание типов IP-адресов на сервере переднего плана для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17ff4-103">Deploy IP address types on a Front End Server for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17ff4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17ff4-104">

<span> </span></span></span>

<span data-ttu-id="17ff4-105">_**Тема последнего изменения:** 2016-07-28_</span><span class="sxs-lookup"><span data-stu-id="17ff4-105">_**Topic Last Modified:** 2016-07-28_</span></span>

<span data-ttu-id="17ff4-106">С помощью построителя топологии выполните действия, описанные в описанной ниже процедуре, чтобы развернуть типы IP-адресов на сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="17ff4-106">Using Topology Builder, perform the steps in the following procedure to deploy IP address types on a Front End Server.</span></span>

<div>

## <a name="to-deploy-ip-address-types-on-a-front-end-server"></a><span data-ttu-id="17ff4-107">Развертывание типов IP-адресов на сервере переднего плана</span><span class="sxs-lookup"><span data-stu-id="17ff4-107">To deploy IP address types on a Front End Server</span></span>

1.  <span data-ttu-id="17ff4-p101">В узле **Enterprise Edition Front End pools** (Интерфейсные пулы Enterprise Edition) щелкните правой кнопкой мыши сервер пула и затем выберите команду **Edit Properties** (Изменить свойства). (Либо выберите сервер и затем в меню **Action** (Действие) выберите команду **Edit Properties** (Изменить свойства).)</span><span class="sxs-lookup"><span data-stu-id="17ff4-p101">Under **Enterprise Edition Front End pools**, right-click the server within a pool, and then select **Edit Properties**. (Alternatively, select the server, and then click **Edit Properties** from the **Action** menu.)</span></span>

2.  <span data-ttu-id="17ff4-p102">В диалоговом окне **Edit Properties** (Изменение свойств) выберите тип IP-адреса, который необходимо настроить. Для конфигурации двойного стека установите флажки **Enable IPv4** (Включить IP версии 4) и **Enable IPv6** (Включить IP версии 6), как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="17ff4-p102">In the **Edit Properties** dialog box, select the IP address type that you want to configure. For a dual-stack configuration, select **Enable IPv4** and **Enable IPv6**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="17ff4-112">**Диалоговое окно "Изменение свойств" для пула серверов переднего плана**</span><span class="sxs-lookup"><span data-stu-id="17ff4-112">**Edit Properties dialog box for the Front End Server pool**</span></span>
    
    <span data-ttu-id="17ff4-113">![Диалоговое окно "изменение свойств" сервера переднего плана](images/JJ205191.737a9d71-c0bc-4a54-9608-9e028dacc814(OCS.15).png "Диалоговое окно "изменение свойств" сервера переднего плана")</span><span class="sxs-lookup"><span data-stu-id="17ff4-113">![Front End Server Edit Properties dialog box](images/JJ205191.737a9d71-c0bc-4a54-9608-9e028dacc814(OCS.15).png "Front End Server Edit Properties dialog box")</span></span>
    
      - <span data-ttu-id="17ff4-p103">**Use all configured IP addresses** (Использовать все заданные IP-адреса). Выберите этот параметр, если требуется разрешить использование любых IP-адресов, заданных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="17ff4-p103">**Use all configured IP addresses**. Select this option if you want to allow any IP address defined on the computer to be used.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="17ff4-116">Этот параметр рекомендуется использовать для конфигураций IP версии 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="17ff4-116">This is the recommended option for IP version 6 (IPv6) configurations.</span></span>

        
        </div>
    
      - <span data-ttu-id="17ff4-p104">**Limit service usage to selected IP addresses** (Разрешить использовать службу только указанным IP-адресам). Выберите этот параметр, чтобы указать адрес, используемый на новом сервере. Если вы выберете этот параметр, потребуется ввести значение в поле **Primary IP address** (Основной IP-адрес).</span><span class="sxs-lookup"><span data-stu-id="17ff4-p104">**Limit service usage to selected IP addresses**. Select this option to specify a specific address to use on the new server. If you select this option, you must enter a value for **Primary IP address**.</span></span>
    
      - <span data-ttu-id="17ff4-p105">**Primary IP address** (Основной IP-адрес). Введите IP-адрес, который будет использовать сервер для всех коммуникаций, за исключением ТСОП. Введенный IP-адрес должен соответствовать формату выбранного типа адресов.</span><span class="sxs-lookup"><span data-stu-id="17ff4-p105">**Primary IP address**. Enter an IP address that the server will use for all communications except public switched telephone network (PSTN). The IP address entered must match the format of the select address type.</span></span>
    
      - <span data-ttu-id="17ff4-123">**PSTN IP address** (IP-адрес ТСОП).</span><span class="sxs-lookup"><span data-stu-id="17ff4-123">**PSTN IP address**.</span></span> <span data-ttu-id="17ff4-124">Установка дополнительных сетевых интерфейсных карт (NIC) для поддержки конфигурации IP-адреса PSTN для Lync Server 2013 не поддерживается на размещенных ролях серверов с разрешениями.</span><span class="sxs-lookup"><span data-stu-id="17ff4-124">The installation of additional network interface cards (NIC)s to support the PSTN IP address configuration for Lync Server 2013 is not supported on collocated Mediation Server roles.</span></span> <span data-ttu-id="17ff4-125">Дополнительные сведения о поддерживаемых конфигурациях сетевых адаптеров для Lync Server 2013 можно найти в разделе [аппаратные платформы сервера для Lync server 2013](lync-server-2013-server-hardware-platforms.md).</span><span class="sxs-lookup"><span data-stu-id="17ff4-125">For more information about supported NIC configurations for Lync Server 2013, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="17ff4-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17ff4-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

