---
title: 'Lync Server 2013: инфраструктура безопасности для Lync Server'
description: 'Lync Server 2013: инфраструктура безопасности для Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Security framework for Lync Server 2013
ms:assetid: 01131e28-b38e-40d9-8524-06725b9c6608
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481316(v=OCS.15)
ms:contentKeyID: 59893866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d30c26929ddedbf653abd1fc353b6873ad8f36f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441902"
---
# <a name="security-framework-for-lync-server-2013"></a><span data-ttu-id="20daf-103">Платформа безопасности для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-103">Security framework for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20daf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20daf-104">

<span> </span></span></span>

<span data-ttu-id="20daf-105">_**Тема последнего изменения:** 2013-11-08_</span><span class="sxs-lookup"><span data-stu-id="20daf-105">_**Topic Last Modified:** 2013-11-08_</span></span>

<span data-ttu-id="20daf-106">В этом разделе приводятся общие сведения об основных элементах, которые формируют структуру безопасности для Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20daf-106">This section provides an overview of the fundamental elements that form the security framework for Microsoft Lync Server 2013.</span></span> <span data-ttu-id="20daf-107">Понимание того, как эти элементы работают вместе, очень важно для принятия обоснованных решений по обеспечению безопасности конкретного развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20daf-107">Understanding how these elements work together is essential to making informed decisions about securing your particular Lync Server 2013 deployment.</span></span>

<span data-ttu-id="20daf-108">Ниже представлены эти элементы.</span><span class="sxs-lookup"><span data-stu-id="20daf-108">These elements are as follows:</span></span>

  - <span data-ttu-id="20daf-109">Доменные службы Active Directory (AD DS) предоставляют единый доверенный серверный репозиторий для учетных записей пользователей и сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20daf-109">Active Directory Domain Services (AD DS) provides a single trusted back-end repository for user accounts and network resources.</span></span>

  - <span data-ttu-id="20daf-110">Управление доступом на основе ролей (RBAC) позволяет делегировать административные задачи, обеспечивая при этом поддержку высоких стандартов безопасности.</span><span class="sxs-lookup"><span data-stu-id="20daf-110">Role-Based Access Control (RBAC) enables you to delegate administrative tasks while maintaining high standards for security.</span></span>

  - <span data-ttu-id="20daf-111">Инфраструктура открытых ключей (PKI) использует сертификаты, выданные доверенными центрами сертификации (ЦС) с целью проверки подлинности серверов и обеспечения целостности данных.</span><span class="sxs-lookup"><span data-stu-id="20daf-111">Public Key Infrastructure (PKI) uses certificates issued by trusted certification authorities (CAs) to authenticate servers and ensure data integrity.</span></span>

  - <span data-ttu-id="20daf-p102">Безопасность на транспортном уровне (TLS), передача HTTPS по SSL (HTTPS) и взаимные подключения по протоколу TLS (MTLS) позволяют выполнять проверку подлинности конечной точки и шифровать обмен мгновенными сообщениями. Потоки информации одноранговых сеансов обмена аудио- и видеоданными и общего доступа к приложениям шифруются с использованием протокола SRTP.</span><span class="sxs-lookup"><span data-stu-id="20daf-p102">Transport Layer Security (TLS), HTTPS over SSL (HTTPS), and mutual TLS (MTLS) enable endpoint authentication and IM encryption. Point-to-point audio, video, and application sharing streams are encrypted using Secure Real-Time Transport Protocol (SRTP).</span></span>

  - <span data-ttu-id="20daf-114">Протоколы отраслевых стандартов для проверки подлинности пользователя (по мере возможности).</span><span class="sxs-lookup"><span data-stu-id="20daf-114">Industry-standard protocols for user authentication, where possible.</span></span>

  - <span data-ttu-id="20daf-115">Windows PowerShell предоставляет функции безопасности, которые включены по умолчанию, чтобы пользователи не могли легко или непреднамеренно запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="20daf-115">Windows PowerShell provides security features that are enabled by default so that users cannot easily or unknowingly run scripts.</span></span>

<span data-ttu-id="20daf-116">Эти фундаментальные элементы безопасности вместе используются для определения доверенных пользователей, серверов, подключений и операций, чтобы обеспечить надежную основу для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20daf-116">These fundamental security elements work together to define trusted users, servers, connections, and operations to help ensure a secure foundation for Lync Server 2013.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="20daf-117">Содержание</span><span class="sxs-lookup"><span data-stu-id="20daf-117">In This Section</span></span>

<span data-ttu-id="20daf-118">В этом разделе объясняется, как все эти фундаментальные элементы помогают повысить безопасность инфраструктуры Lync Server.</span><span class="sxs-lookup"><span data-stu-id="20daf-118">The topics in this section describe how each of these fundamental elements works to enhance the security of your Lync Server infrastructure.</span></span>

  - [<span data-ttu-id="20daf-119">Доменные службы Active Directory для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-119">Active Directory Domain Services for Lync Server 2013</span></span>](lync-server-2013-active-directory-domain-services-for-lync-server.md)

  - [<span data-ttu-id="20daf-120">Управление доступом на основе ролей (RBAC) для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-120">Role-based access control (RBAC) for Lync Server 2013</span></span>](lync-server-2013-role-based-access-control-rbac.md)

  - [<span data-ttu-id="20daf-121">Инфраструктура открытых ключей для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-121">Public Key Infrastructure for Lync Server 2013</span></span>](lync-server-2013-public-key-infrastructure.md)

  - [<span data-ttu-id="20daf-122">TLS и MTLS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-122">TLS and MTLS for Lync Server 2013</span></span>](lync-server-2013-tls-and-mtls.md)

  - [<span data-ttu-id="20daf-123">Шифрование для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-123">Encryption for Lync Server 2013</span></span>](lync-server-2013-encryption.md)

  - [<span data-ttu-id="20daf-124">Проверка подлинности пользователей и клиентов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-124">User and client authentication for Lync Server 2013</span></span>](lync-server-2013-user-and-client-authentication.md)

  - [<span data-ttu-id="20daf-125">Средства управления для Windows PowerShell и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20daf-125">Windows PowerShell and Lync Server 2013 management tools</span></span>](lync-server-2013-windows-powershell-and-lync-server-management-tools.md)

<span data-ttu-id="20daf-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20daf-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

