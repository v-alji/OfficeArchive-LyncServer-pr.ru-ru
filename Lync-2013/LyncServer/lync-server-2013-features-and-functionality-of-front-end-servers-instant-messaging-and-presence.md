---
title: 'Lync Server 2013: возможности и функции серверов переднего плана, службы обмена мгновенными сообщениями и сведениями о присутствии'
description: 'Lync Server 2013: функции и функции серверов переднего плана, обмена мгновенными сообщениями и присутствия.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Features and functionality of Front End Servers, instant messaging, and presence
ms:assetid: 05b29536-dcd7-49b5-934a-2ebf20ddc45c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398109(v=OCS.15)
ms:contentKeyID: 48183294
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5c8bc3db255228da3366eb5aa142cd5adc233d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398176"
---
# <a name="features-and-functionality-of-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="408ec-103">Возможности и функции серверов переднего плана, службы обмена мгновенными сообщениями и сведениями о присутствии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="408ec-103">Features and functionality of Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="408ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="408ec-104">

<span> </span></span></span>

<span data-ttu-id="408ec-105">_**Тема последнего изменения:** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="408ec-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="408ec-106">Серверы переднего плана обеспечивают большую функциональность Lync Server.</span><span class="sxs-lookup"><span data-stu-id="408ec-106">Front End Servers provide most Lync Server functionality.</span></span> <span data-ttu-id="408ec-107">Доступно два выпусков: Lync Server Enterprise Edition, предназначенный для крупных организаций, и Lync Server Standard Edition, разработанный в основном для небольших организаций, которым требуется более производительный investement и не требует высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="408ec-107">There are two editions available: Lync Server Enterprise Edition, which is designed primarily for larger organizations, and Lync Server Standard Edition, which is designed primarily for smaller organizations which want a smaller hardware investement and do not require high availability.</span></span> <span data-ttu-id="408ec-108">В обоих выпусках поддерживаются все рабочие нагрузки Lync Server, включая обмен мгновенными сообщениями, присутствие, Конференц-связь и корпоративный голос.</span><span class="sxs-lookup"><span data-stu-id="408ec-108">Both editions support all Lync Server workloads including IM, presence, conferencing, and Enterprise Voice.</span></span>

<span data-ttu-id="408ec-109">Обмен мгновенными сообщениями дает пользователям возможность общаться друг с другом в режиме реального времени со своих компьютеров, используя текстовые сообщения.</span><span class="sxs-lookup"><span data-stu-id="408ec-109">Instant messaging (IM) enables your users to communicate with each other in real time on their computers using text-based messages.</span></span> <span data-ttu-id="408ec-110">Поддерживаются как двухсторонние, так и многосторонние сеансы обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="408ec-110">Both two-party and multiparty IM sessions are supported.</span></span> <span data-ttu-id="408ec-111">Участник двухсторонней текстовой беседы может в любое время пригласить третьего участника.</span><span class="sxs-lookup"><span data-stu-id="408ec-111">A participant in a two-party IM conversation can add a third participant to the conversation at any time.</span></span> <span data-ttu-id="408ec-112">Когда это происходит, окно беседы изменяется, чтобы поддерживать функции конференции.</span><span class="sxs-lookup"><span data-stu-id="408ec-112">When this happens, the Conversation window changes to support conferencing features.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="408ec-113">Клиенты Lync и Communicator, вовлеченные в одну и ту же связь, часто называют одноранговой.</span><span class="sxs-lookup"><span data-stu-id="408ec-113">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="408ec-114">Технически, эти два клиента взаимодействуют между собой в одном сеансе, с помощью управляющего блока обмена мгновенными сообщениями (IMMCU) в центре.</span><span class="sxs-lookup"><span data-stu-id="408ec-114">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="408ec-115">IMMCU является компонентом сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="408ec-115">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="408ec-116">Размещение IMMCU в требуемом рабочем канале связи позволяет записывать сведения о вызове и другие возможности, которые сервер переднего плана включит.</span><span class="sxs-lookup"><span data-stu-id="408ec-116">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="408ec-117">Взаимодействие осуществляется из динамического исходного порта на клиенте на серверный порт TLS/TCP/5061 (предполагается использование рекомендуемой безопасности транспортного уровня).</span><span class="sxs-lookup"><span data-stu-id="408ec-117">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="408ec-118">Связь между одноранговым и одноранговой связью (а также многосторонним СООБЩЕНИЕм) возможна только в том случае, если Lync Server и IMMCU активны и доступны.</span><span class="sxs-lookup"><span data-stu-id="408ec-118">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<span data-ttu-id="408ec-119">Сведения о *присутствии* предоставляют пользователям информацию о состоянии другого в сети.</span><span class="sxs-lookup"><span data-stu-id="408ec-119">*Presence* provides information to users about the status of other on the network.</span></span> <span data-ttu-id="408ec-120">Информация о состоянии присутствия пользователя помогает другим пользователям решить, когда следует связаться с этим пользователем, и что лучше использовать – обмен мгновенными сообщениями, телефон или электронную почту.</span><span class="sxs-lookup"><span data-stu-id="408ec-120">A user’s presence status provides information to help others decide whether they should try to contact the user and whether to use instant messaging, phone, or email.</span></span> <span data-ttu-id="408ec-121">Функция присутствия предлагает обмен мгновенными сообщениями всегда, когда это возможно, но также сообщает, когда пользователь находится на собрании или вне офиса, указывая, что обмен мгновенными сообщениями невозможен.</span><span class="sxs-lookup"><span data-stu-id="408ec-121">Presence encourages instant communication when possible, but it also provides information about whether a user is in a meeting or out of the office, indicating that instant communication is not possible.</span></span> <span data-ttu-id="408ec-122">Это состояние присутствия отображается как значок присутствия в Lync и другие приложения, поддерживающие присутствие, в том числе клиент Microsoft Outlook для обмена сообщениями и совместной работы, технологии Microsoft SharePoint и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="408ec-122">This presence status is displayed as a presence icon in Lync and other presence-aware applications, including the Microsoft Outlook messaging and collaboration client, Microsoft SharePoint technologies, Microsoft Word, and Microsoft Excel spreadsheet software.</span></span> <span data-ttu-id="408ec-123">Значок присутствия указывает текущую доступность пользователя и готовность к общению.</span><span class="sxs-lookup"><span data-stu-id="408ec-123">The presence icon represents the user’s current availability and willingness to communicate.</span></span>

<span data-ttu-id="408ec-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="408ec-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

