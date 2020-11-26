---
title: 'Lync Server 2013: Настройка дополнительной службы сведений о расположении'
description: 'Lync Server 2013: Настройка дополнительной службы сведений о расположении.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a secondary Location Information service
ms:assetid: 083ffbc6-7c18-4141-85f9-8825b62c3d10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398138(v=OCS.15)
ms:contentKeyID: 48183334
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1721299a0c70535dff8dd05e31712ee6a8d93691
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434216"
---
# <a name="configure-a-secondary-location-information-service-in-lync-server-2013"></a><span data-ttu-id="53f8d-103">Настройка дополнительной службы сведений о расположении в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f8d-103">Configure a secondary Location Information service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="53f8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="53f8d-104">

<span> </span></span></span>

<span data-ttu-id="53f8d-105">_**Тема последнего изменения:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="53f8d-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="53f8d-106">Lync Server 2013 предоставляет интерфейс веб-службы, который можно использовать для указания службы сведений о расположении в базу данных дополнительного расположения (SLS).</span><span class="sxs-lookup"><span data-stu-id="53f8d-106">Lync Server 2013 provides a web service interface that you can use to point the Location Information service to a Secondary Location Source (SLS) database.</span></span> <span data-ttu-id="53f8d-107">Интерфейс веб-службы, который подключается к базе данных SLS, должен соответствовать WSDL службы сведений о расположении.</span><span class="sxs-lookup"><span data-stu-id="53f8d-107">The web service interface that connects to the SLS database must conform to Location Information service WSDL.</span></span> <span data-ttu-id="53f8d-108">Если вы настроили базу данных расположения и дополнительную базу данных расположения, Служба сведений о расположении сначала запрашивает базу данных расположения, а если совпадений не найдено, отправляет запрос на расположение от клиента в базу данных SLS.</span><span class="sxs-lookup"><span data-stu-id="53f8d-108">If both a location database and secondary location database are configured, the Location Information service first queries the location database, and if no match is found, sends the location request from the client to the SLS database.</span></span> <span data-ttu-id="53f8d-109">Если расположение находится в SLS, служба сведения о местоположении затем отправляет клиенту расположение обратно.</span><span class="sxs-lookup"><span data-stu-id="53f8d-109">If the location exists in the SLS, the Location Information service then sends the location back to the client.</span></span>

<span data-ttu-id="53f8d-110">Подробности можно найти в документации по оболочке управления Lync Server для следующего командлета:</span><span class="sxs-lookup"><span data-stu-id="53f8d-110">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="53f8d-111">**Set-CsWebServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="53f8d-111">**Set-CsWebServiceConfiguration**</span></span>

<div>

## <a name="to-configure-secondary-location-database"></a><span data-ttu-id="53f8d-112">Настройка дополнительной базы данных расположения</span><span class="sxs-lookup"><span data-stu-id="53f8d-112">To configure Secondary Location database</span></span>

1.  <span data-ttu-id="53f8d-113">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="53f8d-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="53f8d-114">Чтобы настроить URL-адрес базы данных дополнительных расположений, выполните следующий командлет.</span><span class="sxs-lookup"><span data-stu-id="53f8d-114">Run the following cmdlet to configure the URL for the location of the secondary location database.</span></span>
    
        Set-CsWebServiceConfiguration -SecondaryLocationSourceURL "<web service url>" 

<span data-ttu-id="53f8d-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="53f8d-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

