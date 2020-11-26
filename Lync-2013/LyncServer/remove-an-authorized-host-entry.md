---
title: Удаление авторизованной записи узла
description: Удаление авторизованной записи узла.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove an authorized host entry
ms:assetid: 56a04140-347e-4eef-bede-0e858534f71e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204902(v=OCS.15)
ms:contentKeyID: 48184177
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95aa8df1745ad3108654fcb9b441b5919d42ec40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443260"
---
# <a name="remove-an-authorized-host-entry"></a><span data-ttu-id="9821d-103">Удаление авторизованной записи узла</span><span class="sxs-lookup"><span data-stu-id="9821d-103">Remove an authorized host entry</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9821d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9821d-104">

<span> </span></span></span>

<span data-ttu-id="9821d-105">_**Тема последнего изменения:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="9821d-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="9821d-106">В этой статье описано, как удалить устаревшую авторизованную запись узла (которая называется *надежной записью приложения* в Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="9821d-106">This topic describes how to remove a legacy authorized host entry (known as a *trusted application entry* in Lync Server 2013).</span></span> <span data-ttu-id="9821d-107">Вы должны удалить существующие авторизованные записи узла для всех шлюзов SIP/CSTA в Office Communications Server 2007 R2, когда вы перенесете управление удаленным звонком в развертывание Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9821d-107">You must remove existing authorized host entries for any SIP/CSTA gateways in your Office Communications Server 2007 R2 deployment when you migrate remote call control to a Lync Server 2013 deployment.</span></span> <span data-ttu-id="9821d-108">Для удаления существующих авторизованных записей узла необходимо использовать средства администрирования, входящие в состав Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="9821d-108">You must use the administrative tools included with Office Communications Server 2007 R2 to remove the existing authorized host entries.</span></span>

<div>

## <a name="to-remove-an-authorized-host-entry-in-an-office-communications-server-2007-r2-deployment"></a><span data-ttu-id="9821d-109">Удаление авторизованной записи узла в развертывании Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9821d-109">To remove an authorized host entry in an Office Communications Server 2007 R2 deployment</span></span>

1.  <span data-ttu-id="9821d-110">Откройте консоль администрирования Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="9821d-110">Open the Office Communications Server 2007 R2 administrative console.</span></span>

2.  <span data-ttu-id="9821d-111">Разверните дерево и щелкните правой кнопкой мыши пул, в котором был создан авторизованный узел.</span><span class="sxs-lookup"><span data-stu-id="9821d-111">Expand the tree and right-click the pool where the authorized host was created.</span></span>

3.  <span data-ttu-id="9821d-112">Нажмите кнопку **Свойства**, а затем — **Свойства Front End**.</span><span class="sxs-lookup"><span data-stu-id="9821d-112">Click **Properties**, and then click **Front End Properties**.</span></span>

4.  <span data-ttu-id="9821d-113">Откройте вкладку **авторизация узла** .</span><span class="sxs-lookup"><span data-stu-id="9821d-113">Click the **Host Authorization** tab.</span></span>

5.  <span data-ttu-id="9821d-114">Выберите сервер, а затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="9821d-114">Select a server, and then click **Remove**.</span></span>

6.  <span data-ttu-id="9821d-115">В окне " **Свойства**" нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9821d-115">In **Properties**, click **OK**.</span></span>

<span data-ttu-id="9821d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9821d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

