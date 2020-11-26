---
title: 'Lync Server 2013: проверка отчета о сертификатах'
description: 'Lync Server 2013: проверка отчета о сертификатах.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reviewing the Certificates Report
ms:assetid: 549cfc9b-3cc5-4483-a93c-fc0738c7f622
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558651(v=OCS.15)
ms:contentKeyID: 51541477
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2133e2f70c78217788d84251c2035a9115bc3283
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442461"
---
# <a name="reviewing-the-certificates-report-in-lync-server-2013"></a><span data-ttu-id="3064d-103">Просмотр отчета о сертификатах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3064d-103">Reviewing the Certificates Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3064d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3064d-104">

<span> </span></span></span>

<span data-ttu-id="3064d-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="3064d-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="3064d-106">Отчет о сертификатах включает все сертификаты, необходимые для рекомендуемого развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3064d-106">The Certificates Report contains all certificates that are required in the recommended Lync Server 2013 deployment.</span></span> <span data-ttu-id="3064d-107">Инструмент "планирование" используется для ввода имен субъектов и альтернативных имен субъектов.</span><span class="sxs-lookup"><span data-stu-id="3064d-107">The Planning Tool accounts for the subject names and subject alternative names that are entered.</span></span> <span data-ttu-id="3064d-108">Default text that is left unedited may represent a potential challenge for the team responsible for requesting and issuing the certificates.</span><span class="sxs-lookup"><span data-stu-id="3064d-108">Default text that is left unedited may represent a potential challenge for the team responsible for requesting and issuing the certificates.</span></span> <span data-ttu-id="3064d-109">Certificate information also contains information about where the certificate can typically be issued from.</span><span class="sxs-lookup"><span data-stu-id="3064d-109">Certificate information also contains information about where the certificate can typically be issued from.</span></span> <span data-ttu-id="3064d-110">If the infrastructure does not have an internal public key infrastructure (PKI) in place, all certificates can be requested through a public certificate provider.</span><span class="sxs-lookup"><span data-stu-id="3064d-110">If the infrastructure does not have an internal public key infrastructure (PKI) in place, all certificates can be requested through a public certificate provider.</span></span> <span data-ttu-id="3064d-111">Extended key usages (EKU) and Assign To fields in the report are very helpful in understanding what the purpose and location for each certificate should be.</span><span class="sxs-lookup"><span data-stu-id="3064d-111">Extended key usages (EKU) and Assign To fields in the report are very helpful in understanding what the purpose and location for each certificate should be.</span></span>

<span data-ttu-id="3064d-112">![Отчет по сертификатам для администратора](images/Gg558651.63a29335-d9e4-41ae-97ec-3c9d9fd30d8a(OCS.15).jpg "Отчет по сертификатам для администратора")</span><span class="sxs-lookup"><span data-stu-id="3064d-112">![Certificates Admin Report](images/Gg558651.63a29335-d9e4-41ae-97ec-3c9d9fd30d8a(OCS.15).jpg "Certificates Admin Report")</span></span>

<span data-ttu-id="3064d-113">Тщательно рассмотрите и осознайте использование и назначение каждого сертификата в развертывании.</span><span class="sxs-lookup"><span data-stu-id="3064d-113">Carefully review, and be sure to understand, the use and purpose of each certificate in the deployment.</span></span> <span data-ttu-id="3064d-114">Если возникает вопрос о том, для чего именно нужен определенный сертификат, определите взаимодействие серверов и служб.</span><span class="sxs-lookup"><span data-stu-id="3064d-114">If there is a question about what a certificate does, determine which server or service is talking to what.</span></span> <span data-ttu-id="3064d-115">Сертификаты в Lync Server 2013 используются в двух основных целях:</span><span class="sxs-lookup"><span data-stu-id="3064d-115">Certificates in Lync Server 2013 are used for two primary purposes:</span></span>

  - <span data-ttu-id="3064d-p103">Протокол MTLS — каждый из взаимодействующих компьютеров предоставляет сертификат, подтверждающий его удостоверение другому компьютеру. Это называется проверкой подлинности сервера. Взаимодействие не начинается до тех пор, пока каждый из компьютеров не будет доверять удостоверению другого компьютера.</span><span class="sxs-lookup"><span data-stu-id="3064d-p103">Mutual Transport Layer Security (MTLS) – The computers involved in the communication each present a certificate that proves their identity to another computer. This is known as server authentication. Communication cannot begin until each computer trusts the other computer’s identity.</span></span>

  - <span data-ttu-id="3064d-119">Шифрование — шифрование (по протоколам SSL и TLS) имеет критически важное значение для обеспечения безопасности связи, конфиденциальности, а также создания системы доверенного взаимодействия и совместной работы.</span><span class="sxs-lookup"><span data-stu-id="3064d-119">Encryption – Encryption (Secure Sockets Layer, or SSL, and Transport Layer Security, or TLS) is a critical means to help secure communications, help ensure privacy, and to create a trusted communications and collaboration system.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="3064d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3064d-120">See Also</span></span>


[<span data-ttu-id="3064d-121">Просмотр отчетов администратора в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3064d-121">Reviewing the Administrator Reports in Lync Server 2013</span></span>](lync-server-2013-reviewing-the-administrator-reports.md)  
  

<span data-ttu-id="3064d-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3064d-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

