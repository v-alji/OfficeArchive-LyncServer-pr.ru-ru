---
title: 'Lync Server 2013: Get-CsAddressBookConfiguration для управления адресными книгами'
description: 'Lync Server 2013: Get-CsAddressBookConfiguration для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsAddressBookConfiguration for Address Book management
ms:assetid: bd62f916-caf3-4e10-ada4-631bbb331ef1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429721(v=OCS.15)
ms:contentKeyID: 48185264
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91b96aead7b7038464f3166691a5952b9ff850dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427980"
---
# <a name="get-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="b0fcb-103">Get-CsAddressBookConfiguration для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0fcb-103">Get-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0fcb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0fcb-104">

<span> </span></span></span>

<span data-ttu-id="b0fcb-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b0fcb-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b0fcb-106">Кто может запустить этот командлет: по умолчанию членам следующих групп разрешено выполнять командлет Get-CsAddressBookConfiguration локально: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b0fcb-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="b0fcb-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b0fcb-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsAddressBookConfiguration"}

<span data-ttu-id="b0fcb-108">Командлет Get-CsAddressBookConfiguration возвращает сведения о уже существующей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b0fcb-108">The cmdlet Get-CsAddressBookConfiguration returns information about a configuration that already exists.</span></span>

<span data-ttu-id="b0fcb-109">Например:</span><span class="sxs-lookup"><span data-stu-id="b0fcb-109">For example:</span></span>

    Get-CsAddressBookConfiguration -Identity site:Redmond

<span data-ttu-id="b0fcb-110">Сочетание функциональных возможностей Get-CsAddressBookConfiguration и Set-CsAddressBookConfiguration позволяет администратору определить, какие конфигурации нужно изменить, а затем применить изменения.</span><span class="sxs-lookup"><span data-stu-id="b0fcb-110">Combining the functionality of Get-CsAddressBookConfiguration and Set-CsAddressBookConfiguration allows the administrator to define which configurations to modify and then apply the modifications.</span></span> <span data-ttu-id="b0fcb-111">Например, комбинированный:</span><span class="sxs-lookup"><span data-stu-id="b0fcb-111">For example, this combined:</span></span>

    Get-CsAddressBookConfiguration -Filter site:* | Set-CsAddressBookConfiguration -RunTimeOfDay 23:00

<span data-ttu-id="b0fcb-112">Возвращает все конфигурации на всех сайтах и применяет в конфигурациях RunTimeOfDay количество часов в 23:00.</span><span class="sxs-lookup"><span data-stu-id="b0fcb-112">Returns all configurations in all sites and applies the RunTimeOfDay of 23:00 hours to the configurations.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="b0fcb-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b0fcb-113">See Also</span></span>


[<span data-ttu-id="b0fcb-114">Get-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0fcb-114">Get-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAddressBookConfiguration)  
  

<span data-ttu-id="b0fcb-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0fcb-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

