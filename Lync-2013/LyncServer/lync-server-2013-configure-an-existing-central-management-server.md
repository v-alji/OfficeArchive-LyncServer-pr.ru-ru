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
# <a name="configure-an-existing-central-management-server-in-lync-server-2013"></a>Настройка существующего центрального сервера управления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-21_

Если вы повторно можете использовать центральный сервер управления из существующего развертывания Lync Server 2013, необходимо выполнить описанные ниже действия, чтобы убедиться, что панель управления Lync Server и функция Windows PowerShell правильно работают.

<div>

## <a name="to-configure-an-existing-central-management-server"></a>Настройка существующего центрального сервера управления

1.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

2.  С помощью командлета **Update-CsAdminRole** можно обновить роли управления доступом на основе РОЛЕЙ (RBAC), хранящиеся на центральном сервере управления.
    
    <div>
    

    > [!NOTE]  
    > Никаких выходных данных не ожидается, если не возникает ошибки.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

