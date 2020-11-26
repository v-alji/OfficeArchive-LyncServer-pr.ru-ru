---
title: 'Lync Server 2013: восстановление содержимого конференций с помощью службы резервного копирования'
description: 'Lync Server 2013: восстановление содержимого конференции с помощью службы резервного копирования.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring conference contents using the Backup Service
ms:assetid: 3e0f18ec-7319-4c07-a59b-2938e7787bc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688030(v=OCS.15)
ms:contentKeyID: 49733620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3a0037af711948c008e74c5444373ed995f0e6e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442546"
---
# <a name="restoring-conference-contents-using-the-backup-service-in-lync-server-2013"></a><span data-ttu-id="bcd14-103">Восстановление содержимого конференций с помощью службы резервного копирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bcd14-103">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bcd14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bcd14-104">

<span> </span></span></span>

<span data-ttu-id="bcd14-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="bcd14-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="bcd14-106">Если сведения о конференции, хранящиеся в хранилище файлов в пуле переднего плана, становятся недоступными.</span><span class="sxs-lookup"><span data-stu-id="bcd14-106">If the conference information stored in the file store of a Front End pool becomes unavailable.</span></span> <span data-ttu-id="bcd14-107">Эти данные необходимо восстановить таким образом, чтобы пользователи, расположенные в пуле, сохраняли свои данные на Конференции.</span><span class="sxs-lookup"><span data-stu-id="bcd14-107">you must restore this information so that users homed on the pool retain their conference data.</span></span> <span data-ttu-id="bcd14-108">Если пул переднего плана, который потерял данные конференции, связан с другим пулом переднего плана, вы можете восстановить данные с помощью службы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bcd14-108">If the Front End pool which has lost conference data is paired with another Front End pool, you can use the Backup Service to restore the data.</span></span>

<span data-ttu-id="bcd14-109">Кроме того, вы должны выполнить эту задачу в случае сбоя всего пула, после чего вы должны переключиться между пользователями в резервный пул.</span><span class="sxs-lookup"><span data-stu-id="bcd14-109">You must also perform this task if an entire pool has failed and you have to fail over its users to a backup pool.</span></span> <span data-ttu-id="bcd14-110">Если эти пользователи не переносятся в исходный пул, необходимо выполнить описанные ниже действия, чтобы снова скопировать содержимое конференции в первоначальный пул.</span><span class="sxs-lookup"><span data-stu-id="bcd14-110">When these users are failed back over to their original pool, you must use this procedure to copy their conference content back to their original pool as well.</span></span>

<span data-ttu-id="bcd14-111">Предположим, что Pool1 связан с Pool2, а данные конференции в Pool1 теряются.</span><span class="sxs-lookup"><span data-stu-id="bcd14-111">Assume that Pool1 is paired with Pool2, and the conference data in Pool1 is lost.</span></span> <span data-ttu-id="bcd14-112">Вы можете использовать следующий командлет для вызова службы резервного копирования для восстановления содержимого:</span><span class="sxs-lookup"><span data-stu-id="bcd14-112">You can use the following cmdlet to invoke the Backup Service to restore the contents:</span></span>

    Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="bcd14-113">Восстановление содержимого конференции может занять некоторое время в зависимости от его размера.</span><span class="sxs-lookup"><span data-stu-id="bcd14-113">Restoring the conference contents may take some time, depending on their size.</span></span> <span data-ttu-id="bcd14-114">Вы можете проверить состояние процесса с помощью следующего командлета:</span><span class="sxs-lookup"><span data-stu-id="bcd14-114">You can use the following cmdlet to check the process status:</span></span>

    Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="bcd14-115">Процесс выполняется, если этот командлет возвращает значение стабильного состояния для модуля конференции с данными.</span><span class="sxs-lookup"><span data-stu-id="bcd14-115">The process is done when this cmdlet returns a value of Steady State for the data conference module.</span></span>

<span data-ttu-id="bcd14-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bcd14-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

