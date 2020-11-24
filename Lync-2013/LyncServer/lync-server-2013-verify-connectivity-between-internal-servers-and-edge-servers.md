---
title: Проверка подключения между внутренними и пограничными серверами
description: Проверка соединения между внутренними и пограничными серверами.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity between internal servers and Edge Servers
ms:assetid: 219f706e-2b8a-46c5-b394-c384240eef50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398292(v=OCS.15)
ms:contentKeyID: 48183602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f86f87428d7eaf91b8f70422cfee712584252fad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399799"
---
# <a name="verify-connectivity-between-internal-servers-and-edge-servers-in-lync-server-2013"></a><span data-ttu-id="45a9b-103">Проверка подключения между внутренними и пограничными серверами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45a9b-103">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45a9b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45a9b-104">

<span> </span></span></span>

<span data-ttu-id="45a9b-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="45a9b-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="45a9b-106">В Lync Server 2013 имеется отдельный мастер проверки, помогающий проверить связь между пограничными серверами и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="45a9b-106">In Lync Server 2013, a separate validation wizard was available to help validate connectivity between Edge Servers and internal servers.</span></span> <span data-ttu-id="45a9b-107">В Lync Server 2013 проверка подключения выполняется автоматически при установке пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="45a9b-107">In Lync Server 2013 validation of connectivity is done automatically when you install your Edge Servers.</span></span>

<span data-ttu-id="45a9b-108">Вы можете проверить репликацию сведений о конфигурации до края, запустив командлет Windows PowerShell **Get-CsManagementStoreReplicationStatus** на внутреннем компьютере, на котором расположено хранилище Центрального управления (или на любом компьютере, подключенном к домену, на котором установлен компонент Lync Server 2013 Core Components (OcsCore.msi).</span><span class="sxs-lookup"><span data-stu-id="45a9b-108">You can validate the replication of configuration information to the edge by running the Windows PowerShell **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located (or any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span> <span data-ttu-id="45a9b-109">Начальные результаты могут содержать состояние "false", а не "истина" для репликации.</span><span class="sxs-lookup"><span data-stu-id="45a9b-109">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="45a9b-110">Если это так, запустите командлет **Invoke-CsManagementStoreReplication** и разрешите время завершения репликации, прежде чем запускать командлет **Get-CsManagementStoreReplicationStatus** еще раз.</span><span class="sxs-lookup"><span data-stu-id="45a9b-110">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="45a9b-111">Вы можете проверить подключение внешних пользователей по отдельности, в том числе с помощью анализатора удаленных подключений Office Communications Server для проверки подключения удаленных пользователей.</span><span class="sxs-lookup"><span data-stu-id="45a9b-111">You can verify external user connectivity separately, including using the Office Communications Server Remote Connectivity Analyzer to verify remote user connectivity.</span></span> <span data-ttu-id="45a9b-112">Дополнительные сведения можно найти [в разделе Проверка подключения внешних пользователей в Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span><span class="sxs-lookup"><span data-stu-id="45a9b-112">For details, see [Verify connectivity for external users in Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span></span>

<span data-ttu-id="45a9b-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45a9b-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

