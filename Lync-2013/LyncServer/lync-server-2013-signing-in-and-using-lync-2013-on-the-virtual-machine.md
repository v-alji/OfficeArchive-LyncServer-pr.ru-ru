---
title: 'Lync Server 2013: вход в виртуальную машину и использование на ней Lync 2013'
description: 'Lync Server 2013: вход и использование Lync 2013 на виртуальной машине.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Signing in and using Lync 2013 on the virtual machine
ms:assetid: 6140fc19-5bef-4b58-9b0f-19112b5ecd00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204948(v=OCS.15)
ms:contentKeyID: 48184318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad9a92d450fb9d60aed70617089d95280528892f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444701"
---
# <a name="signing-in-and-using-lync-2013-on-the-virtual-machine"></a><span data-ttu-id="fe429-103">Вход в виртуальную машину и использование на ней Lync 2013</span><span class="sxs-lookup"><span data-stu-id="fe429-103">Signing in and using Lync 2013 on the virtual machine</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe429-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe429-104">

<span> </span></span></span>

<span data-ttu-id="fe429-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="fe429-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="fe429-106">После включения надстройки VDI выполняются описанные ниже действия, когда пользователь входит в Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="fe429-106">After the VDI plug-in is enabled, the following steps occur when the user signs in to Lync 2013.</span></span>

1.  <span data-ttu-id="fe429-107">Пользователь вводит свои учетные данные в клиент Lync 2013, работающий на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fe429-107">The user types his or her credentials in to the Lync 2013 client running on the virtual machine.</span></span>

2.  <span data-ttu-id="fe429-108">После того как Lync обнаружит доступность плагина VDI, Lync предложит пользователю повторно ввести свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="fe429-108">After Lync detects the availability of the VDI plug-in, Lync prompts the user to re-enter his or her credentials.</span></span> <span data-ttu-id="fe429-109">In this dialog box, we recommend that the user select the **Save my password** check box so that he or she will not be required to enter credentials during subsequent sign in.</span><span class="sxs-lookup"><span data-stu-id="fe429-109">In this dialog box, we recommend that the user select the **Save my password** check box so that he or she will not be required to enter credentials during subsequent sign in.</span></span>

3.  <span data-ttu-id="fe429-110">Lync начинает связывание с помощью плагина VDI.</span><span class="sxs-lookup"><span data-stu-id="fe429-110">Lync begins pairing with the VDI plug-in.</span></span> <span data-ttu-id="fe429-111">Перед завершением связывания клиент отображает в строке состояния Lync два значка.</span><span class="sxs-lookup"><span data-stu-id="fe429-111">Before pairing is complete, the client displays two icons in the Lync status bar.</span></span> <span data-ttu-id="fe429-112">Значок внизу слева указывает на то, что звуковое устройство недоступно, а значок мигания справа внизу указывает на то, что связывание VDI выполняется, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fe429-112">The icon in the lower left indicates that no audio devices are available, and the blinking icon in the lower right indicates that the VDI pairing is in progress, as shown:</span></span>
    
    <span data-ttu-id="fe429-113">![Значок Lync VDI, показывающий успешное связывание](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Значок Lync VDI, показывающий успешное связывание")</span><span class="sxs-lookup"><span data-stu-id="fe429-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>  

4.  <span data-ttu-id="fe429-114">После успешного сопряжения подключаемого модуля VDI значки изменяются и теперь обозначают аудиоустройство, которое будет использоваться для выполнения вызовов, а также успешное сопряжение VDI:</span><span class="sxs-lookup"><span data-stu-id="fe429-114">After VDI pairing is successful, the icons change to indicate the audio device that will be used for calls and the VDI pairing success:</span></span>
    
    <span data-ttu-id="fe429-115">![Значок связывания в Lync VDI, демонстрирующий успешное создание](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Значок связывания в Lync VDI, демонстрирующий успешное создание")</span><span class="sxs-lookup"><span data-stu-id="fe429-115">![Lync VDI pairing icon showing success](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Lync VDI pairing icon showing success")</span></span>  

5.  <span data-ttu-id="fe429-116">После пар Lync с подключаемым модулем VDI пользователь может видеть свое присутствие на устройствах, совместимых с Lync, которые подключены к локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="fe429-116">After Lync pairs with the VDI plug-in, the user can see his or her presence on Lync compatible devices that are connected to the local computer.</span></span> <span data-ttu-id="fe429-117">Теперь пользователь может размещать и отвечать на звонки в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="fe429-117">The user can now place and answer calls as usual.</span></span>

<span data-ttu-id="fe429-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe429-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

