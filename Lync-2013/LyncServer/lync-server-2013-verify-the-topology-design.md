---
title: 'Lync Server 2013: проверка структуры топологии'
description: 'Lync Server 2013: Проверьте структуру топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438913"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a><span data-ttu-id="8b75e-103">Проверка структуры топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b75e-103">Verify the topology design in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b75e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b75e-104">

<span> </span></span></span>

<span data-ttu-id="8b75e-105">_**Тема последнего изменения:** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="8b75e-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="8b75e-106">Построитель топологии автоматически проверяет топологию.</span><span class="sxs-lookup"><span data-stu-id="8b75e-106">Topology Builder automatically verifies the topology.</span></span> <span data-ttu-id="8b75e-107">Любая ошибка топологии определяется как ошибка проверки, указанная значком ошибки проверки рядом с ролью сервера.</span><span class="sxs-lookup"><span data-stu-id="8b75e-107">Any topology error is identified as a validation error, indicated by the validation error icon next to the server role.</span></span> <span data-ttu-id="8b75e-108">Важно также убедиться, что топология правильно представляет топологию для развертывания.</span><span class="sxs-lookup"><span data-stu-id="8b75e-108">It is important to also verify that the topology correctly represents the topology for your deployment.</span></span>

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a><span data-ttu-id="8b75e-109">Проверка топологии перед публикацией</span><span class="sxs-lookup"><span data-stu-id="8b75e-109">To verify the topology prior to publication</span></span>

1.  <span data-ttu-id="8b75e-110">Проверьте, что все простые URL-адреса настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="8b75e-110">Check that all simple URLs are configured correctly.</span></span>

2.  <span data-ttu-id="8b75e-111">Проверьте, что сервер на основе SQL Server включен и доступен компьютеру, на котором установлен построитель топологий, включая все необходимые правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8b75e-111">Confirm that the SQL Server-based server is online and available to the computer where Topology Builder is installed, including any necessary firewall rules.</span></span>

3.  <span data-ttu-id="8b75e-112">Убедитесь в том, что общий доступ к файлам доступен, и у него есть соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="8b75e-112">Confirm that the file share is available and has the proper permissions defined.</span></span>

4.  <span data-ttu-id="8b75e-113">Проверьте, что в топологии заданы правильные роли сервера, удовлетворяющие требованиям развертывания.</span><span class="sxs-lookup"><span data-stu-id="8b75e-113">Confirm that the correct server roles that meet the deployment requirements are defined in the topology.</span></span>

5.  <span data-ttu-id="8b75e-114">Убедитесь в том, что серверы находятся в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8b75e-114">Verify that the servers exist in Active Directory Domain Services.</span></span> <span data-ttu-id="8b75e-115">Это происходит автоматически, если вы присоединили серверы к домену.</span><span class="sxs-lookup"><span data-stu-id="8b75e-115">This will happen automatically if you have joined the servers to the domain.</span></span>

<span data-ttu-id="8b75e-116">Когда топология проверена и ошибки проверки отсутствуют, все должно быть готово к публикации топологии.</span><span class="sxs-lookup"><span data-stu-id="8b75e-116">When you have verified the topology and there are no validation errors, you should be ready to publish the topology.</span></span> <span data-ttu-id="8b75e-117">Если обнаружены ошибки проверки, необходимо исправить эти значения, прежде чем можно будет опубликовать топологию.</span><span class="sxs-lookup"><span data-stu-id="8b75e-117">If there are validation errors, you must correct these before you can publish the topology.</span></span> <span data-ttu-id="8b75e-118">Подробнее о публикации топологии можно найти в разделе [Публикация топологии в Lync Server 2013](lync-server-2013-publish-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="8b75e-118">For details about publishing your topology, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md).</span></span>

<span data-ttu-id="8b75e-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b75e-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

