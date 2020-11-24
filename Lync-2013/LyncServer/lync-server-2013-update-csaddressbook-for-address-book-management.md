---
title: 'Lync Server 2013: Update-CsAddressBook для управления адресными книгами'
description: 'Lync Server 2013: Update-CsAddressBook для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Update-CsAddressBook for Address Book management
ms:assetid: 0ffd2ef8-201c-44aa-8c64-1c7b0eaa7d48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429695(v=OCS.15)
ms:contentKeyID: 48183428
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4adc7f94e2f31f64f6517b8cdf9bbcb0649f6c8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399478"
---
# <a name="update-csaddressbook-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="f8b7c-103">Update-CsAddressBook для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8b7c-103">Update-CsAddressBook for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8b7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8b7c-104">

<span> </span></span></span>

<span data-ttu-id="f8b7c-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f8b7c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f8b7c-106">Кто может запустить этот командлет: по умолчанию членам следующих групп разрешено выполнять командлет Update-CsAddressBook локально: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Update-CsAddressBook cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="f8b7c-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f8b7c-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Update-CsAddressBook"}

<span data-ttu-id="f8b7c-108">Командлет Update-CsAddressBook заменяет команду **abserver.exe – syncNow** из Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-108">The Update-CsAddressBook cmdlet replaces the **abserver.exe –syncNow** command from Office Communications Server.</span></span> <span data-ttu-id="f8b7c-109">Цель командлета состоит в том, чтобы начать синхронизацию немедленно, вместо того чтобы ждать запланированного времени.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-109">The cmdlet’s purpose is to initiate a synchronization immediately rather than waiting for the scheduled time.</span></span> <span data-ttu-id="f8b7c-110">Первый пример команды обновляет все адресные книги в Организации.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-110">The first example command updates all Address Books in the organization.</span></span> <span data-ttu-id="f8b7c-111">Вторая обновляет только адресную книгу, связанную с определенным сервером.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-111">The second updates only the Address Book associated with the defined server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f8b7c-112">В Lync Server 2013 служба репликатора пользователей Lync Server выберет изменения из Active Directory и обновит базу данных пользователей Lync Server на основе заданного интервала.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-112">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="f8b7c-113">Служба репликации пользователей Lync Server также будет автоматически распространять изменения базы данных RTCab, не требуя администратора запускать Update-CSAddressBook.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-113">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="f8b7c-114">Администраторам потребуется выполнить Update-CSAddressBook только в том случае, если разрешена загрузка файла адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f8b7c-114">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>



</div>

<span data-ttu-id="f8b7c-115">Например:</span><span class="sxs-lookup"><span data-stu-id="f8b7c-115">For example:</span></span>

   ```PowerShell
    Update-CsAddressBook
   ```

   ```PowerShell
    Update-CsAddressBook -Fqdn atl-abs-001.contoso.com
   ```

<div>

## <a name="see-also"></a><span data-ttu-id="f8b7c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f8b7c-116">See Also</span></span>


[<span data-ttu-id="f8b7c-117">Update-CsAddressBook</span><span class="sxs-lookup"><span data-stu-id="f8b7c-117">Update-CsAddressBook</span></span>](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook)  
  

<span data-ttu-id="f8b7c-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8b7c-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

