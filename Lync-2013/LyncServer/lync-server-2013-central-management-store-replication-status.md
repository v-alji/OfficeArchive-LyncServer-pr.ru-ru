---
title: 'Lync Server 2013: состояние репликации центрального хранилища управления'
description: 'Lync Server 2013: состояние репликации в магазине Central Management Store.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central management store replication status
ms:assetid: f514f88d-986b-4e45-b79b-e04a7616c1fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720926(v=OCS.15)
ms:contentKeyID: 63969663
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f1f9008a966040cf34ac0499c023f9dbe53a541
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435462"
---
# <a name="central-management-store-replication-status-in-lync-server-2013"></a><span data-ttu-id="8ecc5-103">Состояние репликации центрального хранилища управления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ecc5-103">Central management store replication status in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ecc5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ecc5-104">

<span> </span></span></span>

<span data-ttu-id="8ecc5-105">_**Тема последнего изменения:** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="8ecc5-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="8ecc5-106">Если администратор вносит изменения в сервер Lync Server (например, при создании администратором новой политики голосовой почты или изменении параметров конфигурации сервера адресной книги), то изменения записываются в хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-106">When an administrator makes a change of some kind to Lync Server (for example, when an administrator creates a new voice policy or changes the Address Book Server configuration settings) that change is recorded in the Central Management store.</span></span> <span data-ttu-id="8ecc5-107">После этого изменения должны быть реплицированы на все компьютеры, на которых запущены службы или роли сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-107">In turn, the change must then be replicated to all the computers that are running Lync Server services or server roles.</span></span>

<span data-ttu-id="8ecc5-108">Для репликации данных основная служба репликации (запущенная на центральном сервере управления) создает снимок измененных данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-108">To replicate data, the Master Replicator (running on the Central Management Server) creates a snapshot of the changed configuration data.</span></span> <span data-ttu-id="8ecc5-109">Затем на каждый компьютер, на котором выполняются службы Lync Server или серверные роли, отправляется копия этого снимка.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-109">A copy of this snapshot is then sent to each computer that is running Lync Server services or server roles.</span></span> <span data-ttu-id="8ecc5-110">На этих компьютерах агент репликации получает снимок и загружает измененные данные.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-110">On those computers, a replication agent receives the snapshot and uploads the changed data.</span></span> <span data-ttu-id="8ecc5-111">После этого агент отправляет основной службе репликации сообщение о последнем состоянии репликации.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-111">The agent then sends the Master Replicator a message reporting the latest replication status.</span></span>

<span data-ttu-id="8ecc5-112">Командлет Get-CsManagementStoreReplicationStatus позволяет проверить состояние репликации для всех (или всех) компьютеров Lync Server в Организации.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-112">The Get-CsManagementStoreReplicationStatus cmdlet enables you to verify the replication status for any (or all) of the Lync Server computers in your organization.</span></span>

<span data-ttu-id="8ecc5-113">Кто может выполнить этот командлет?</span><span class="sxs-lookup"><span data-stu-id="8ecc5-113">Who can run this cmdlet?</span></span> <span data-ttu-id="8ecc5-114">По умолчанию право на локальное выполнение командлета Get-CsManagementStoreReplicationStatus имеют участники следующих групп: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="8ecc5-114">By default, members of the following groups are authorized to run the Get-CsManagementStoreReplicationStatus cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span>

<span data-ttu-id="8ecc5-115">Чтобы возвратить список всех ролей RBAC, которым был назначен этот командлет (включая любые пользовательские роли RBAC, созданные вами), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8ecc5-115">To return a list of all RBAC roles this cmdlet was assigned to (including any custom RBAC roles that you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsManagementStoreReplicationStatus"}

<div>

## <a name="see-also"></a><span data-ttu-id="8ecc5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="8ecc5-116">See Also</span></span>


[<span data-ttu-id="8ecc5-117">Get-CsManagementStoreReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="8ecc5-117">Get-CsManagementStoreReplicationStatus</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsManagementStoreReplicationStatus)  
  

<span data-ttu-id="8ecc5-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ecc5-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

