---
title: 'Lync Server 2013: поддержка инфраструктуры сертификатов'
description: Поддержка инфраструктуры сертификата Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure support
ms:assetid: 47aa5c95-eb60-4d4b-81d5-7fdaef1a1145
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425950(v=OCS.15)
ms:contentKeyID: 48184047
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc08719e5b1c58a4dc3c1cab07db5e9842d46d5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435406"
---
# <a name="certificate-infrastructure-support-in-lync-server-2013"></a><span data-ttu-id="69817-103">Поддержка инфраструктуры сертификатов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69817-103">Certificate infrastructure support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69817-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69817-104">

<span> </span></span></span>

<span data-ttu-id="69817-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="69817-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="69817-106">Lync Server 2013 требует наличия инфраструктуры открытых ключей (PKI) для поддержки протоколов TLS и взаимного TLS-соединения (MTLS).</span><span class="sxs-lookup"><span data-stu-id="69817-106">Lync Server 2013 requires a public key infrastructure (PKI) to support Transport Layer Security (TLS) and mutual TLS (MTLS) connections.</span></span> <span data-ttu-id="69817-107">По умолчанию Lync Server 2013 настроен на использование протокола TLS для подключений между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="69817-107">By default, Lync Server 2013 is configured to use TLS for client-to-server connections.</span></span> <span data-ttu-id="69817-108">MTLS используется для подключений между серверами.</span><span class="sxs-lookup"><span data-stu-id="69817-108">MTLS is used for connections between servers.</span></span>

<span data-ttu-id="69817-109">Сертификаты MTLS должны выдаваться доверенными центрами сертификации (ЦС) для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="69817-109">MTLS certificates must be issued by trusted certification authorities (CAs) for Lync Server 2013.</span></span> <span data-ttu-id="69817-110">Lync Server поддерживает сертификаты, выданные следующими центрами сертификации:</span><span class="sxs-lookup"><span data-stu-id="69817-110">Lync Server supports certificates that are issued from the following CAs:</span></span>

  - <span data-ttu-id="69817-111">Сертификаты, выданные внутренним центром сертификации:</span><span class="sxs-lookup"><span data-stu-id="69817-111">Certificates issued from an internal CA:</span></span>
    
      - <span data-ttu-id="69817-112">Центр сертификации операционной системы Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69817-112">The Windows Server 2003 operating system CA</span></span>
    
      - <span data-ttu-id="69817-113">Центр сертификации операционной системы Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69817-113">The Windows Server 2008 operating system CA</span></span>
    
      - <span data-ttu-id="69817-114">Центр сертификации операционной системы Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69817-114">The Windows Server 2008 R2 operating system CA</span></span>
    
      - <span data-ttu-id="69817-115">Центр сертификации операционной системы Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69817-115">The Windows Server 2012 operating system CA</span></span>
    
      - <span data-ttu-id="69817-116">Центр сертификации операционной системы Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="69817-116">The Windows Server 2012 R2 operating system CA</span></span>

  - <span data-ttu-id="69817-117">Сертификаты, выданные общедоступным центром сертификации</span><span class="sxs-lookup"><span data-stu-id="69817-117">Certificates issued from a public CA</span></span>

<span data-ttu-id="69817-118">Для связи с другими приложениями и серверами, такими как Exchange 2013, требуется сертификат, который поддерживается другими приложениями и продуктами.</span><span class="sxs-lookup"><span data-stu-id="69817-118">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="69817-119">В выпуске 2013, Lync Server 2013 и других серверных продуктах Microsoft, включая Exchange 2013 и SharePoint Server, поддерживается протокол OAuth для проверки подлинности и авторизации сервера и сервера.</span><span class="sxs-lookup"><span data-stu-id="69817-119">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="69817-120">Дополнительные сведения можно найти [в разделе Управление проверкой подлинности серверов (OAuth) и партнерским приложением в Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) в документации по развертыванию или документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="69817-120">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="69817-121">Для подключений клиентов, работающих под управлением операционной системы Windows 7, Windows Server 2008 R2 и Microsoft Office Communicator 2007 Phone Edition, Lync Server 2013 включает поддержку (но не обязательно) сертификатов, подписанных с помощью криптографической хэш-функции SHA-256.</span><span class="sxs-lookup"><span data-stu-id="69817-121">For connections from clients running Windows 7 operating system, Windows Server 2008 R2 operating system, and Microsoft Office Communicator 2007 Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="69817-122">Для поддержки внешнего доступа с помощью SHA-256 внешний сертификат выдается общедоступным центром сертификации с помощью SHA-256.</span><span class="sxs-lookup"><span data-stu-id="69817-122">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="69817-123">Сведения о требованиях к сертификатам можно найти в разделе [требования к инфраструктуре сертификатов для Lync Server 2013](lync-server-2013-certificate-infrastructure-requirements.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="69817-123">For details about certificate requirements, see [Certificate infrastructure requirements for Lync Server 2013](lync-server-2013-certificate-infrastructure-requirements.md) in the Planning documentation.</span></span> <span data-ttu-id="69817-124">Подробнее об использовании подстановочных знаков в сертификатах можно узнать [в разделе Поддержка сертификатов с помощью подстановочных знаков в Lync Server 2013](lync-server-2013-wildcard-certificate-support.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="69817-124">For details about use of wildcards with certificates, see [Wildcard certificate support in Lync Server 2013](lync-server-2013-wildcard-certificate-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="69817-125"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69817-125"></div>

<span> </span>

</div>

</div>

</span></span></div>

