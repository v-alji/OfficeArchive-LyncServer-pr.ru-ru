---
title: 'Lync Server 2013: поддержка единой системы обмена сообщениями Exchange'
description: 'Lync Server 2013: поддержка единой системы обмена сообщениями Exchange (UM).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exchange Unified Messaging (UM) support
ms:assetid: 0da62b8d-7416-4fb8-a405-381ca805c53a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398179(v=OCS.15)
ms:contentKeyID: 48183405
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 563517bb72167bbab0b08eba3b1359ae3ab52836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399736"
---
# <a name="exchange-unified-messaging-um-support-in-lync-server-2013"></a><span data-ttu-id="35eee-103">Поддержка единой системы обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35eee-103">Exchange Unified Messaging (UM) support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="35eee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="35eee-104">

<span> </span></span></span>

<span data-ttu-id="35eee-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="35eee-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="35eee-106">Lync Server 2013 поддерживает интеграцию с единой системой обмена сообщениями Exchange (UM) для комбинирования голосовой почты и обмена сообщениями в одной инфраструктуре обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="35eee-106">Lync Server 2013 supports integration with Exchange Unified Messaging (UM) for combining voice messaging and email messaging into a single messaging infrastructure.</span></span> <span data-ttu-id="35eee-107">В Exchange 2013 система обмена сообщениями Exchange состоит из службы Exchange UM, установленной на сервере почтовых ящиков и работающей на нем, а также на маршрутизаторе вызовов UM, установленном и работающем на сервере клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="35eee-107">In Exchange 2013, Exchange UM consists of the Exchange UM service, which is installed and runs on the Mailbox server, and the UM Call Router, which is installed and runs on the Client Access server.</span></span> <span data-ttu-id="35eee-108">Для развертываний корпоративных голосовых решений Lync Server 2013 в едином хранилище, которое может быть доступно с телефона (то есть с помощью голосового доступа к Outlook) или компьютера, можно объединить сообщения электронной почты Exchange.</span><span class="sxs-lookup"><span data-stu-id="35eee-108">For Lync Server 2013 Enterprise Voice deployments, Exchange UM combines voice messaging and email messaging into a single store that is accessible from a telephone (that is, Outlook Voice Access) or a computer.</span></span> <span data-ttu-id="35eee-109">Обмен UM и Lync Server 2013 работают вместе для обеспечения ответа на звонки, голосового доступа к Outlook и служб автосекретаря для пользователей корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="35eee-109">Exchange UM and Lync Server 2013 work together to provide call answering, Outlook Voice Access, and auto attendant services to users of Enterprise Voice.</span></span>

<span data-ttu-id="35eee-110">Помимо поддержки интеграции с локальными развертываниями единой системы обмена сообщениями Exchange, Lync Server 2013 поддерживает интеграцию с размещенной единой системой обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="35eee-110">In addition to the support for integration with on-premises deployments of Exchange UM, Lync Server 2013 supports integration with hosted Exchange UM.</span></span> <span data-ttu-id="35eee-111">Это позволит вам предоставлять пользователям голосовой почты, если вы перенесете некоторые или все их в размещенный поставщик услуг Exchange, например Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="35eee-111">This enables you to provide voice messaging to your users if you migrate some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="35eee-112">Lync Server 2013 поддерживает следующие версии:</span><span class="sxs-lookup"><span data-stu-id="35eee-112">Lync Server 2013 supports the following versions:</span></span>

  - <span data-ttu-id="35eee-113">Microsoft Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="35eee-113">Microsoft Exchange 2013</span></span>

  - <span data-ttu-id="35eee-114">Microsoft Exchange Server 2010 (обязательно) или последний пакет обновления (рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="35eee-114">Microsoft Exchange Server 2010 (required) or with latest service pack (recommended)</span></span>

  - <span data-ttu-id="35eee-115">Microsoft Exchange Server 2007 с пакетом обновления 1 (SP1) (обязательно) или последним пакетом обновления (рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="35eee-115">Microsoft Exchange Server 2007 with Service Pack 1 (SP1) (required) or latest service pack (recommended)</span></span>

<span data-ttu-id="35eee-116">Вы не можете разгруппировать единую систему обмена сообщениями Exchange с помощью Lync Server 2013 или базы данных Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="35eee-116">You cannot collocate Exchange UM with Lync Server 2013 or a Lync Server 2013 database.</span></span> <span data-ttu-id="35eee-117">Вы можете установить Exchange UM и Lync Server 2013 в отдельных лесах.</span><span class="sxs-lookup"><span data-stu-id="35eee-117">You can install Exchange UM and Lync Server 2013 in separate forests.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="35eee-118">Exchange UM может не потребоваться для развертывания корпоративных голосовых систем с развернутой АТС, так как УАТС может продолжать предоставлять всем пользователям голосовую почту и связанные службы.</span><span class="sxs-lookup"><span data-stu-id="35eee-118">Exchange UM may not be required for Enterprise Voice deployments that have a PBX deployed, because the PBX can continue to provide voice mail and related services to all users.</span></span> <span data-ttu-id="35eee-119">Если вы захотите отключить УАТС (например, при развертывании магистральной магистрали SIP для подключения по коммутируемой телефонной сети), необходимо заново настроить сервер UM для предоставления голосовой почты пользователям, которые ранее использовали систему голосовой почты УАТС.</span><span class="sxs-lookup"><span data-stu-id="35eee-119">If you eventually retire the PBX (for example, if you deploy SIP trunking for public switched telephone network (PSTN) connectivity), you must reconfigure Exchange UM to provide voice mail to users who previously used the PBX voice mail system.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="35eee-120">Содержание</span><span class="sxs-lookup"><span data-stu-id="35eee-120">In This Section</span></span>

  - [<span data-ttu-id="35eee-121">Компоненты и топологии для локальной единой системы обмена сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35eee-121">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-on-premises-unified-messaging.md)

  - [<span data-ttu-id="35eee-122">Поддержка интеграции размещенной единой системы обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35eee-122">Support for hosted Exchange UM integration in Lync Server 2013</span></span>](lync-server-2013-support-for-hosted-exchange-um-integration.md)

<span data-ttu-id="35eee-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="35eee-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

