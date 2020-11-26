---
title: 'Lync Server 2013: (необязательно) Проверка развертывания для остановки вызова'
description: 'Lync Server 2013: (необязательный) Проверка развертывания приостановки звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Call Park deployment
ms:assetid: fcfe0962-1a9c-4cbd-847c-fed40e3b1480
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413076(v=OCS.15)
ms:contentKeyID: 48185952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 772392a3a791ed57c3220d80e9bd510d8803debb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424865"
---
# <a name="optional-verify-call-park-deployment-in-lync-server-2013"></a><span data-ttu-id="a511d-103">Необязательно Проверка развертывания парковки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a511d-103">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a511d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a511d-104">

<span> </span></span></span>

<span data-ttu-id="a511d-105">_**Тема последнего изменения:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="a511d-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="a511d-106">После установки и настройки парковки звонка необходимо проверить конфигурацию, чтобы убедиться, что стоянки и получение вызовов работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="a511d-106">After you install and configure Call Park, you need to verify the configuration to make sure that parking and retrieving calls works as expected.</span></span> <span data-ttu-id="a511d-107">At minimum, verify the following:</span><span class="sxs-lookup"><span data-stu-id="a511d-107">At minimum, verify the following:</span></span>

  - <span data-ttu-id="a511d-108">Позвоните пользователю, для которого установлен флажок "припаркованный Звонок", и приостановить Звонок абонентом.</span><span class="sxs-lookup"><span data-stu-id="a511d-108">Call a user who has Call Park enabled and have the user park the call.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a511d-109">Если вы включили переадресацию звонков в голосовой политике прямо перед выполнением этого теста, пользователь, который применяет приостановку, должен выйти из Lync Server, а затем снова войти, чтобы можно было видеть параметр "дозвониться" в списке "передача звонков".</span><span class="sxs-lookup"><span data-stu-id="a511d-109">If you enabled Call Park in voice policy just before performing this test, the user who is parking the call needs to sign out of Lync Server, and then sign back in, to be able to see the Call Park option in the transfer call list.</span></span>

    
    </div>

  - <span data-ttu-id="a511d-110">Для извлечения вызова наберите номер орбиты.</span><span class="sxs-lookup"><span data-stu-id="a511d-110">Dial the orbit number to retrieve the call.</span></span>

  - <span data-ttu-id="a511d-p102">Приостановите другой вызов, дождитесь истечения времени ожидания и не поднимайте трубку при переключении на удерживаемого абонента. Убедитесь в том, что вызов с истекшим временем ожидания перенаправляется в резервное место назначения, заданное параметром **OnTimeoutURI**.</span><span class="sxs-lookup"><span data-stu-id="a511d-p102">Park another call, let the parked call time out, and do not pick up the ringback. Verify that the timed-out call is correctly routed to the fallback destination that is specified for **OnTimeoutURI**.</span></span>

<span data-ttu-id="a511d-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a511d-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

