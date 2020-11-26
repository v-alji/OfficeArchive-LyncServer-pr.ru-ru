---
title: 'Lync Server 2013: планирование интеграции единой системы обмена сообщениями Exchange'
description: 'Lync Server 2013: планирование интеграции единой системы обмена сообщениями Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Exchange Unified Messaging integration
ms:assetid: e7c63a71-2d99-4aa9-b649-36c1a431bdf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399031(v=OCS.15)
ms:contentKeyID: 48185880
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31296444d21a86a7837da3e29fc2152f3ca96ccc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443001"
---
# <a name="planning-for-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="1fd37-103">Планирование интеграции единой системы обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fd37-103">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1fd37-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1fd37-104">

<span> </span></span></span>

<span data-ttu-id="1fd37-105">_**Тема последнего изменения:** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="1fd37-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="1fd37-106">Lync Server 2013 поддерживает интеграцию с единой системой обмена сообщениями Exchange (UM) для комбинирования голосовой почты и обмена сообщениями в одной инфраструктуре обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1fd37-106">Lync Server 2013 supports integration with Exchange Unified Messaging (UM) for combining voice messaging and email messaging into a single messaging infrastructure.</span></span> <span data-ttu-id="1fd37-107">В Microsoft Exchange Server 2007 с пакетом обновления 1 (SP1) и Microsoft Exchange Server 2010 сервер единой системы обмена сообщениями Exchange (UM) — это одна из нескольких ролей Exchange Server, которые можно установить и настроить.</span><span class="sxs-lookup"><span data-stu-id="1fd37-107">In Microsoft Exchange Server 2007 Service Pack 1 (SP1) and Microsoft Exchange Server 2010, Exchange Unified Messaging (UM) is one of several Exchange server roles that you can install and configure.</span></span>

<span data-ttu-id="1fd37-108">В Microsoft Exchange Server 2013 служба единой системы обмена сообщениями работает в качестве службы сервера почтовых ящиков Exchange.</span><span class="sxs-lookup"><span data-stu-id="1fd37-108">In Microsoft Exchange Server 2013, Exchange UM runs as a service on an Exchange Mailbox server.</span></span> <span data-ttu-id="1fd37-109">Для корпоративных развертываний на Lync Server 2013, единая система обмена сообщениями объединяет голосовую почту и сообщения электронной почты в едином магазине, доступном с телефона (голосовой доступ к Outlook) или на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1fd37-109">For Lync Server 2013 Enterprise Voice deployments, Unified Messaging combines voice messaging and email messaging into a single store that is available from a telephone (Outlook Voice Access) or a computer.</span></span> <span data-ttu-id="1fd37-110">Единая система обмена сообщениями и Lync Server 2013 работают вместе для обеспечения ответа на звонки, голосового доступа к Outlook и служб автоматического ассистента для пользователей корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="1fd37-110">Unified Messaging and Lync Server 2013 work together to provide call answering, Outlook Voice Access, and auto-attendant services to users of Enterprise Voice.</span></span>

<span data-ttu-id="1fd37-111">Дополнительные сведения об изменениях архитектуры в Microsoft Exchange Server 2013 можно найти в разделе "изменения архитектуры голосовой связи" в документации по Microsoft Exchange Server 2013 по адресу [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730) .</span><span class="sxs-lookup"><span data-stu-id="1fd37-111">For more information about the architecture changes in Microsoft Exchange Server 2013, see “Voice Architecture Changes” in the Microsoft Exchange Server 2013 documentation at [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730).</span></span>

<span data-ttu-id="1fd37-112">Для того чтобы эти функции поддерживались в локальной среде Exchange UM, необходимо выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="1fd37-112">For these features to be supported in an on-premises Exchange UM deployment, you must be running one of the following:</span></span>

  - <span data-ttu-id="1fd37-113">Microsoft Exchange Server 2007 с пакетом обновления 1 (SP1) или последний пакет обновления</span><span class="sxs-lookup"><span data-stu-id="1fd37-113">Microsoft Exchange Server 2007 Service Pack 1 (SP1) or latest service pack</span></span>

  - <span data-ttu-id="1fd37-114">Microsoft Exchange Server 2010 или последний пакет обновления</span><span class="sxs-lookup"><span data-stu-id="1fd37-114">Microsoft Exchange Server 2010 or latest service pack</span></span>

  - <span data-ttu-id="1fd37-115">Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fd37-115">Microsoft Exchange Server 2013</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1fd37-116">Содержание</span><span class="sxs-lookup"><span data-stu-id="1fd37-116">In This Section</span></span>

  - [<span data-ttu-id="1fd37-117">Функции интегрированной единой системы обмена сообщениями и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fd37-117">Features of integrated Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-features-of-integrated-unified-messaging.md)

  - [<span data-ttu-id="1fd37-118">Компоненты и топологии для локальной единой системы обмена сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fd37-118">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-on-premises-unified-messaging.md)

  - [<span data-ttu-id="1fd37-119">Рекомендации по интеграции локальной единой системы обмена сообщениями и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fd37-119">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

  - [<span data-ttu-id="1fd37-120">Процесс развертывания для интеграции локальной единой системы обмена сообщениями и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fd37-120">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="1fd37-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1fd37-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

