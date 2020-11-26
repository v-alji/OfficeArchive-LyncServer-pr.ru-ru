---
title: 'Lync Server 2013: TLS и MTLS'
description: 'Lync Server 2013: TLS и MTLS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TLS and MTLS for Lync Server 2013
ms:assetid: b32a5b85-fc82-42dc-a9b2-96400f8cd2b8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481133(v=OCS.15)
ms:contentKeyID: 59893873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ccee47e635435dd5f0d5eae03711c0cd5e517b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439703"
---
# <a name="tls-and-mtls-for-lync-server-2013"></a><span data-ttu-id="3fffa-103">TLS и MTLS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fffa-103">TLS and MTLS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fffa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fffa-104">

<span> </span></span></span>

<span data-ttu-id="3fffa-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="3fffa-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="3fffa-106">Протоколы TLS и MTLS предоставляют зашифрованный обмен данными и проверку подлинности конечной точки в Интернете.</span><span class="sxs-lookup"><span data-stu-id="3fffa-106">Transport Layer Security (TLS) and Mutual Transport Layer Security (MTLS) protocols provide encrypted communications and endpoint authentication on the Internet.</span></span> <span data-ttu-id="3fffa-107">Microsoft Lync Server 2013 использует эти два протокола для создания сети доверенных серверов и для проверки того, что все коммуникации в сети зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="3fffa-107">Microsoft Lync Server 2013 uses these two protocols to create the network of trusted servers and to ensure that all communications over that network are encrypted.</span></span> <span data-ttu-id="3fffa-108">Весь обмен данными по протоколу SIP между серверами происходит по протоколу MTLS.</span><span class="sxs-lookup"><span data-stu-id="3fffa-108">All SIP communications between servers occur over MTLS.</span></span> <span data-ttu-id="3fffa-109">Обмен данными по протоколу SIP от клиента к серверу выполняется по протоколу TLS.</span><span class="sxs-lookup"><span data-stu-id="3fffa-109">SIP communications from client to server occur over TLS.</span></span>

<span data-ttu-id="3fffa-110">Протокол TLS позволяет пользователям с помощью клиентского программного обеспечения проверять подлинность серверов Lync Server 2013, к которым они подключаются.</span><span class="sxs-lookup"><span data-stu-id="3fffa-110">TLS enables users, through their client software, to authenticate the Lync Server 2013 servers to which they connect.</span></span> <span data-ttu-id="3fffa-111">При подключении по протоколу TLS клиент запрашивает от сервера действительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="3fffa-111">On a TLS connection, the client requests a valid certificate from the server.</span></span> <span data-ttu-id="3fffa-112">Чтобы сертификат был действительным, он должен быть выдан ЦС, который также является доверенным объектом клиента, а имя DNS должно соответствовать имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="3fffa-112">To be valid, the certificate must have been issued by a CA that is also trusted by the client and the DNS name of the server must match the DNS name on the certificate.</span></span> <span data-ttu-id="3fffa-113">Если сертификат действительный, клиент использует открытый ключ в сертификате для шифрования симметричных ключей шифрования, которые будут использоваться для обмена данными, поэтому только исходный владелец сертификата может использовать закрытый ключ для шифрования содержимого сеанса обмена данными.</span><span class="sxs-lookup"><span data-stu-id="3fffa-113">If the certificate is valid, the client uses the public key in the certificate to encrypt the symmetric encryption keys to be used for the communication, so only the original owner of the certificate can use its private key to decrypt the contents of the communication.</span></span> <span data-ttu-id="3fffa-114">Результатом является доверенное подключение, которое после этого уже не проверяется другими доверенными серверами или клиентами.</span><span class="sxs-lookup"><span data-stu-id="3fffa-114">The resulting connection is trusted and from that point is not challenged by other trusted servers or clients.</span></span> <span data-ttu-id="3fffa-115">В рамках этого контекста протокол SSL, используемый веб-службами, может быть связан как протокол на базе TLS.</span><span class="sxs-lookup"><span data-stu-id="3fffa-115">Within this context, Secure Sockets Layer (SSL) as used with Web services can be associated as TLS-based.</span></span>

<span data-ttu-id="3fffa-116">Для подключений типа "сервер-сервер" используется протокол MTLS для взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="3fffa-116">Server-to-server connections rely on MTLS for mutual authentication.</span></span> <span data-ttu-id="3fffa-117">В подключениях по протоколу MTLS создавший сообщение сервер и сервер, который получает его, обмениваются сертификатами из ЦС со взаимным доверием.</span><span class="sxs-lookup"><span data-stu-id="3fffa-117">On an MTLS connection, the server originating a message and the server receiving it exchange certificates from a mutually trusted CA.</span></span> <span data-ttu-id="3fffa-118">Сертификаты подтверждают идентичность каждого из серверов с другим.</span><span class="sxs-lookup"><span data-stu-id="3fffa-118">The certificates prove the identity of each server to the other.</span></span> <span data-ttu-id="3fffa-119">При развертывании Lync Server 2013 сертификаты, выданные центром сертификации предприятия и не отозванные центром сертификации, автоматически считаются действительными на всех внутренних клиентах и серверах, так как все участники домена Active Directory доверяете центру сертификации предприятия в этом домене.</span><span class="sxs-lookup"><span data-stu-id="3fffa-119">In Lync Server 2013 deployments, certificates issued by the enterprise CA that are during their validity period and not revoked by the issuing CA are automatically considered valid by all internal clients and servers because all members of an Active Directory domain trust the Enterprise CA in that domain.</span></span> <span data-ttu-id="3fffa-120">В федеративных сценариях оба федеративных партнера должны доверять выдающему ЦС.</span><span class="sxs-lookup"><span data-stu-id="3fffa-120">In federated scenarios, the issuing CA must be trusted by both federated partners.</span></span> <span data-ttu-id="3fffa-121">Каждый партнер может использовать разные ЦС (при необходимости), пока другой партнер доверяет этому ЦС.</span><span class="sxs-lookup"><span data-stu-id="3fffa-121">Each partner can use a different CA, if desired, so long as that CA is also trusted by the other partner.</span></span> <span data-ttu-id="3fffa-122">Обеспечить это доверие легко, указав корневой сертификат ЦС партнера для пограничных серверов в их доверенных корневых ЦС или при использовании сторонних ЦС в качестве доверенных объектов обоих сторон.</span><span class="sxs-lookup"><span data-stu-id="3fffa-122">This trust is most easily accomplished by the Edge Servers having the partner’s root CA certificate in their trusted root CAs, or by use of a third-party CA that is trusted by both parties.</span></span>

<span data-ttu-id="3fffa-123">TLS and MTLS help prevent both eavesdropping and man-in-the middle attacks.</span><span class="sxs-lookup"><span data-stu-id="3fffa-123">TLS and MTLS help prevent both eavesdropping and man-in-the middle attacks.</span></span> <span data-ttu-id="3fffa-124">В атаке "злоумышленник в середине" злоумышленник перенаправляет связь между двумя сетевыми объектами через компьютер злоумышленника без ведома любой из сторон.</span><span class="sxs-lookup"><span data-stu-id="3fffa-124">In a man-in-the-middle attack, the attacker reroutes communications between two network entities through the attacker’s computer without the knowledge of either party.</span></span> <span data-ttu-id="3fffa-125">Спецификации TLS и Lync Server 2013 (только те, которые указаны в Topology Builder) снижают риск частичной атаки на уровне приложения, используя для этого шифрование с открытым ключом между двумя конечными точками. и злоумышленник должен иметь действительный и доверенный сертификат с соответствующим закрытым ключом и выдан для имени службы, с которой клиент взаимодействует для расшифровки связи.</span><span class="sxs-lookup"><span data-stu-id="3fffa-125">TLS and Lync Server 2013 specification of trusted servers (only those specified in Topology Builder) mitigate the risk of a man-in-the middle attack partially on the application layer by using end-to-end encryption coordinated using the Public Key cryptography between the two endpoints, and an attacker would have to have a valid and trusted certificate with the corresponding private key and issued to the name of the service to which the client is communicating to decrypt the communication.</span></span> <span data-ttu-id="3fffa-126">Ultimately, however, you must follow best security practices with your networking infrastructure (in this case corporate DNS).</span><span class="sxs-lookup"><span data-stu-id="3fffa-126">Ultimately, however, you must follow best security practices with your networking infrastructure (in this case corporate DNS).</span></span> <span data-ttu-id="3fffa-127">Lync Server 2013 предполагает, что DNS-сервер является надежным, так же, как контроллеры домена и глобальные каталоги являются надежными, но DNS обеспечивает уровень защиты от атак с помощью DNS-захвата, предотвращая успешный отклик сервера на запрос на поддельное имя.</span><span class="sxs-lookup"><span data-stu-id="3fffa-127">Lync Server 2013 assumes that the DNS server is trusted in the same way that domain controllers and global catalogs are trusted, but DNS does provide a level of safeguard against DNS hijack attacks by preventing an attacker’s server from responding successfully to a request to the spoofed name.</span></span>

<span data-ttu-id="3fffa-128">На приведенном ниже рисунке показано, как Lync Server 2013 использует MTLS для создания сети надежных серверов.</span><span class="sxs-lookup"><span data-stu-id="3fffa-128">The following figure shows at a high level how Lync Server 2013 uses MTLS to create a network of trusted servers.</span></span>

<span data-ttu-id="3fffa-129">**Доверенные соединения в сети Lync Server**</span><span class="sxs-lookup"><span data-stu-id="3fffa-129">**Trusted connections in a Lync Server network**</span></span>

<span data-ttu-id="3fffa-130">![437749da-c372-4f0d-ac72-ccfd5191696b](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f0d-ac72-ccfd5191696b")</span><span class="sxs-lookup"><span data-stu-id="3fffa-130">![437749da-c372-4f0d-ac72-ccfd5191696b](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f0d-ac72-ccfd5191696b")</span></span>

<span data-ttu-id="3fffa-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fffa-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

