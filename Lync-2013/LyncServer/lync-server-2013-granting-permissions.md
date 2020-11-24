---
title: 'Lync Server 2013: предоставление разрешений'
description: 'Lync Server 2013: предоставление разрешений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting permissions
ms:assetid: d1c9ea66-bd07-480e-99a0-011108f97e42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398901(v=OCS.15)
ms:contentKeyID: 48185446
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4bdb2b1ef39b85caa89c7597f455e6e4fc08e44e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399733"
---
# <a name="granting-permissions-in-lync-server-2013"></a><span data-ttu-id="25dc3-103">Предоставление разрешений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25dc3-103">Granting permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25dc3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25dc3-104">

<span> </span></span></span>

<span data-ttu-id="25dc3-105">_**Тема последнего изменения:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="25dc3-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="25dc3-106">Для настройки можно предоставить разрешения на доступ к универсальной группе RTCUniversalServerAdmins для определенного подразделения Active Directory (OU), включив в него членов группы RTCUniversalServerAdmins для установки Lync Server 2013 в указанном домене.</span><span class="sxs-lookup"><span data-stu-id="25dc3-106">For setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain.</span></span> <span data-ttu-id="25dc3-107">При предоставлении разрешений на доступ к подразделению предоставляются следующие разрешения:</span><span class="sxs-lookup"><span data-stu-id="25dc3-107">When you grant permissions for an OU, the following permissions are granted:</span></span>

  - <span data-ttu-id="25dc3-108">Читаются</span><span class="sxs-lookup"><span data-stu-id="25dc3-108">Read</span></span>

  - <span data-ttu-id="25dc3-109">Пишу</span><span class="sxs-lookup"><span data-stu-id="25dc3-109">Write</span></span>

  - <span data-ttu-id="25dc3-110">ReadSPN</span><span class="sxs-lookup"><span data-stu-id="25dc3-110">ReadSPN</span></span>

  - <span data-ttu-id="25dc3-111">WriteSPN</span><span class="sxs-lookup"><span data-stu-id="25dc3-111">WriteSPN</span></span>

<span data-ttu-id="25dc3-112">Для администрирования вы можете добавить разрешения для указанных подразделений, чтобы участники универсальных групп RTC, созданные с помощью подготовки леса, могли получать доступ к подразделениям без необходимости входить в группу администраторов домена.</span><span class="sxs-lookup"><span data-stu-id="25dc3-112">For administration, you can add permissions to specified OUs so that members of the RTC universal groups created by forest preparation can access the OUs without needing to be members of the Domain Admins group.</span></span> <span data-ttu-id="25dc3-113">Разрешения, добавленные в указанный ОРГАНИЗАЦИОНный элемент, совпадают с разрешениями, которые командлет **Enable-CsAdDomain** добавляет к контейнерам OU Computers и Users.</span><span class="sxs-lookup"><span data-stu-id="25dc3-113">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users OU containers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="25dc3-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="25dc3-114">In This Section</span></span>

  - [<span data-ttu-id="25dc3-115">Предоставление разрешений на установку в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25dc3-115">Granting setup permissions in Lync Server 2013</span></span>](lync-server-2013-granting-setup-permissions.md)

  - [<span data-ttu-id="25dc3-116">Предоставление разрешений организационного подразделения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25dc3-116">Granting organizational unit permissions in Lync Server 2013</span></span>](lync-server-2013-granting-organizational-unit-permissions.md)

<span data-ttu-id="25dc3-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25dc3-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

