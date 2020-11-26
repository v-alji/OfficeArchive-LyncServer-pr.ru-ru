---
title: 'Lync Server 2013: New-CsClientPolicy для управления адресными книгами'
description: 'Lync Server 2013: New-CsClientPolicy для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsClientPolicy for Address Book management
ms:assetid: ef4415fc-82c4-4dc8-97d1-37a084553343
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429726(v=OCS.15)
ms:contentKeyID: 48185771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12c14534c7af447f30a01b1bbbd1679a8375c705
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425112"
---
# <a name="new-csclientpolicy-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="353d0-103">New-CsClientPolicy для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="353d0-103">New-CsClientPolicy for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="353d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="353d0-104">

<span> </span></span></span>

<span data-ttu-id="353d0-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="353d0-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="353d0-106">Кто может запустить этот командлет: по умолчанию членам указанных ниже групп разрешено выполнять командлет New-CsClientPolicy: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="353d0-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsClientPolicy cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="353d0-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="353d0-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsClientPolicy"}

<span data-ttu-id="353d0-108">Командлет New-CsClientPolicy определяет большое количество параметров для подготовки клиентов к функциям, которые доступны в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="353d0-108">The cmdlet New-CsClientPolicy defines a large number of settings for provisioning clients for features that are available in Lync Server 2013.</span></span> <span data-ttu-id="353d0-109">Для службы адресной книги AddressBookAvailability параметра.</span><span class="sxs-lookup"><span data-stu-id="353d0-109">For the Address Book Service, the parameter AddressBookAvailability is of interest.</span></span> <span data-ttu-id="353d0-110">Этот параметр, непосредственно влияющий на доступные клиентам варианты, имеет три возможных параметра:</span><span class="sxs-lookup"><span data-stu-id="353d0-110">This parameter, which directly impacts the options available to clients, has three possible options:</span></span>

  - <span data-ttu-id="353d0-111">WebSearchAndFileDownload</span><span class="sxs-lookup"><span data-stu-id="353d0-111">WebSearchAndFileDownload</span></span>

  - <span data-ttu-id="353d0-112">WebSearchOnly</span><span class="sxs-lookup"><span data-stu-id="353d0-112">WebSearchOnly</span></span>

  - <span data-ttu-id="353d0-113">FileDownloadOnly</span><span class="sxs-lookup"><span data-stu-id="353d0-113">FileDownloadOnly</span></span>

<span data-ttu-id="353d0-114">При определении определяет способ доступа к адресной книге клиентам.</span><span class="sxs-lookup"><span data-stu-id="353d0-114">When defined, it determines how the Address Book is accessed by clients.</span></span> <span data-ttu-id="353d0-115">Если вы определяете этот параметр, необходимо задать один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="353d0-115">If you define this parameter, you must define one of the options.</span></span> <span data-ttu-id="353d0-116">Если вы не измените этот параметр, WebSearchAndFileDownload по умолчанию остается в силе.</span><span class="sxs-lookup"><span data-stu-id="353d0-116">If you do not modify this setting, the default WebSearchAndFileDownload remains in effect.</span></span>

<span data-ttu-id="353d0-117">Например:</span><span class="sxs-lookup"><span data-stu-id="353d0-117">For example:</span></span>

    New-CsClientPolicy -Identity RedmondClientPolicy -DisableCalendarPresence $True -DisablePhonePresence $True -DisplayPhoto "PhotosFromADOnly" -AddressBookAvailability "WebSearchOnly"

<div>

## <a name="see-also"></a><span data-ttu-id="353d0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="353d0-118">See Also</span></span>


[<span data-ttu-id="353d0-119">New-CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="353d0-119">New-CsClientPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy)  
  

<span data-ttu-id="353d0-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="353d0-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

