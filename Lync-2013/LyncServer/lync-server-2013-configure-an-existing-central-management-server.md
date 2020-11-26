---
title: 'Lync Server 2013: настройка существующего центрального сервера управления'
description: 'Lync Server 2013: настройте существующий центральный сервер управления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure an existing Central Management Server
ms:assetid: d715b24a-1256-4a7c-a5ef-1cee41d6b733
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205315(v=OCS.15)
ms:contentKeyID: 48185584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef93281be2537ca5e4a5892a8617500ce54f3c45
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434126"
---
# <a name="configure-an-existing-central-management-server-in-lync-server-2013"></a><span data-ttu-id="79aab-103">Настройка существующего центрального сервера управления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79aab-103">Configure an existing Central Management Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79aab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79aab-104">

<span> </span></span></span>

<span data-ttu-id="79aab-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="79aab-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="79aab-106">Если вы повторно можете использовать центральный сервер управления из существующего развертывания Lync Server 2013, необходимо выполнить описанные ниже действия, чтобы убедиться, что панель управления Lync Server и функция Windows PowerShell правильно работают.</span><span class="sxs-lookup"><span data-stu-id="79aab-106">If you reuse a Central Management Server from an existing Lync Server 2013 deployment, you must run the procedure described below to make sure that Lync Server Control Panel and Windows PowerShell function correctly.</span></span>

<div>

## <a name="to-configure-an-existing-central-management-server"></a><span data-ttu-id="79aab-107">Настройка существующего центрального сервера управления</span><span class="sxs-lookup"><span data-stu-id="79aab-107">To configure an existing Central Management Server</span></span>

1.  <span data-ttu-id="79aab-108">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="79aab-108">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="79aab-109">С помощью командлета **Update-CsAdminRole** можно обновить роли управления доступом на основе РОЛЕЙ (RBAC), хранящиеся на центральном сервере управления.</span><span class="sxs-lookup"><span data-stu-id="79aab-109">Use the **Update-CsAdminRole** cmdlet to update the role-based access control (RBAC) roles stored in the Central Management Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79aab-110">Никаких выходных данных не ожидается, если не возникает ошибки.</span><span class="sxs-lookup"><span data-stu-id="79aab-110">No output is expected unless there is an error.</span></span>

    
    <span data-ttu-id="79aab-111"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79aab-111"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

