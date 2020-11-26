---
title: 'Lync Server 2013: New-CsAddressBookConfiguration для управления адресными книгами'
description: 'Lync Server 2013: New-CsAddressBookConfiguration для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsAddressBookConfiguration for Address Book management
ms:assetid: a58ddc8c-ae04-4141-b69e-e45374a67d72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429718(v=OCS.15)
ms:contentKeyID: 48184985
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c85d85fefe701456ad253f1afc69b73093b30996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445451"
---
# <a name="new-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="63ac4-103">New-CsAddressBookConfiguration для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="63ac4-103">New-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63ac4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63ac4-104">

<span> </span></span></span>

<span data-ttu-id="63ac4-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="63ac4-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="63ac4-106">Кто может запустить этот командлет: по умолчанию членам следующих групп разрешено выполнять командлет New-CsAddressBookConfiguration локально: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="63ac4-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="63ac4-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="63ac4-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsAddressBookConfiguration"}

<span data-ttu-id="63ac4-108">Командлет New-CsAddressBookConfiguration создает новую конфигурацию для управления поведением адресной книги.</span><span class="sxs-lookup"><span data-stu-id="63ac4-108">The New-CsAddressBookConfiguration cmdlet creates a new configuration to manage the behavior of the Address book.</span></span> <span data-ttu-id="63ac4-109">Для этого командлета вы можете определить, создает ли служба адресных книг клиентские файлы для скачивания, как и при использовании правил нормализации, как долго следует сохранять разностные и сжатые файлы Дельта и сжатия перед включением нового полного создания файлов, время суток, в котором вы создаете полную адресную книгу, а также то, что должно быть для синхронизации информации в базе данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="63ac4-109">Specific to this cmdlet is the ability to define if the Address Book Service creates the client download files, how and if normalization rules are used, how long to retain delta and compact delta files, delta file size before incorporating a new full file creation, what time of day the full file Address Book is created, and what the internal should be for synchronization of information in the User database.</span></span>

<span data-ttu-id="63ac4-110">Например:</span><span class="sxs-lookup"><span data-stu-id="63ac4-110">For example:</span></span>

    New-CsAddressBookConfiguration -Identity site:Redmond -KeepDuration 15 -SynchronizePollingInterval 00:10:00

<div>

## <a name="see-also"></a><span data-ttu-id="63ac4-111">См. также</span><span class="sxs-lookup"><span data-stu-id="63ac4-111">See Also</span></span>


[<span data-ttu-id="63ac4-112">New-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="63ac4-112">New-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsAddressBookConfiguration)  
  

<span data-ttu-id="63ac4-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63ac4-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

