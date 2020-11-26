---
title: 'Lync Server 2013: журналы и файлы обновлений устройств'
description: 'Lync Server 2013: журналы и файлы обновлений устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update logs and files
ms:assetid: f7f822b8-0a62-4ff2-a4cb-1ab1ed7503eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994090(v=OCS.15)
ms:contentKeyID: 51804004
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50db4935f62a4c037ab81a0d11e1eb993466fa80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429390"
---
# <a name="device-update-logs-and-files-in-lync-server-2013"></a><span data-ttu-id="203b5-103">Журналы и файлы обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="203b5-103">Device Update logs and files in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="203b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="203b5-104">

<span> </span></span></span>

<span data-ttu-id="203b5-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="203b5-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="203b5-106">Журналы обновления устройства содержат важную информацию, которую можно использовать для управления веб-службой обновления устройства и устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="203b5-106">Device update logs contain important information that you can use to manage and troubleshoot the Device Update Web service.</span></span> <span data-ttu-id="203b5-107">Вы можете изменить записи, которые записываются в журнал, и удалять журналы устройств и обновления, которые вам не нужны или больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="203b5-107">You can change what is logged and remove device logs and updates that you don’t want or no longer need.</span></span> <span data-ttu-id="203b5-108">В этом разделе рассказывается о том, как можно использовать панель управления Lync Server или консоль управления Lync Server для изменения параметров ведения журнала, очистки журнала обновления устройства или удаления файлов журнала с сервера.</span><span class="sxs-lookup"><span data-stu-id="203b5-108">This section describes how you can use Lync Server Control Panel or Lync Server Management Shell to modify logging settings, clear the device update log, or remove log files from the server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="203b5-109">Дополнительные сведения о файлах журнала обновления устройств можно найти в разделе <A href="https://technet.microsoft.com/library/gg398250(v=ocs.14).aspx">типы и расположения файлов журнала</A> в библиотеке TechNet Server 2010.</span><span class="sxs-lookup"><span data-stu-id="203b5-109">For details about device update log files, see <A href="https://technet.microsoft.com/library/gg398250(v=ocs.14).aspx">Log File Types and Locations</A> in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="203b5-110">(Обратите внимание, что веб-служба обновления устройства, как и все компоненты Lync Phone Edition, работает аналогично с Lync Server 2013, как это происходит в Lync Server 2010.)</span><span class="sxs-lookup"><span data-stu-id="203b5-110">(Note that the Device Update Web service, like all Lync Phone Edition components, works the same way with Lync Server 2013 as it does with Lync Server 2010.)</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="203b5-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="203b5-111">In This Section</span></span>

  - [<span data-ttu-id="203b5-112">Изменение параметров для файлов журнала обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="203b5-112">Modify settings for Device Update log files in Lync Server 2013</span></span>](lync-server-2013-modify-settings-for-device-update-log-files.md)

  - [<span data-ttu-id="203b5-113">Удаление файлов журнала обновления устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="203b5-113">Delete Device Update log files in Lync Server 2013</span></span>](lync-server-2013-delete-device-update-log-files.md)

  - [<span data-ttu-id="203b5-114">Удаление файлов обновления устройства, не связанных с устройством в окне удаления файлов обновления устройства, не связанных с устройством в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="203b5-114">Remove Device Update files not associated with a device in Remove Device Update files not associated with a device in Lync Server 2013</span></span>](lync-server-2013-remove-device-update-files-not-associated-with-a-device.md)

<span data-ttu-id="203b5-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="203b5-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

