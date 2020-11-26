---
title: 'Lync Server 2013: командлеты адресной книги сервера'
description: 'Lync Server 2013: Командлеты сервера адресной книги.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Address Book Server cmdlets
ms:assetid: 33da45da-3c57-4d04-9679-f0e5a0cfd37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415643(v=OCS.15)
ms:contentKeyID: 48183793
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4fef903d25f0d2707410e017f4eb280282bbdab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439998"
---
# <a name="address-book-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="567c5-103">Командлеты сервера адресной книги в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="567c5-103">Address Book Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="567c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="567c5-104">

<span> </span></span></span>

<span data-ttu-id="567c5-105">_**Тема последнего изменения:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="567c5-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="567c5-106">Серверы адресной книги являются посредниками между доменными службами Active Directory и Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="567c5-106">Address Book servers are intermediaries between Active Directory Domain Services and Microsoft Lync Server 2013.</span></span> <span data-ttu-id="567c5-107">Сервер адресной книги обеспечивает синхронизацию сведений о пользователях, хранящихся в Lync Server 2013, с информацией о пользователе, хранящейся в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="567c5-107">The Address Book server ensures that the user information stored in Lync Server 2013 is in synch with the user information stored in Active Directory.</span></span> <span data-ttu-id="567c5-108">Это можно сделать, периодически синхронизируя файлы адресной книги с данными, хранящимися в базе данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="567c5-108">This is done by periodically synching Address Book files with information stored in the User database.</span></span> <span data-ttu-id="567c5-109">В свою очередь, Lync Server включает несколько командлетов для управления серверами адресной книги.</span><span class="sxs-lookup"><span data-stu-id="567c5-109">In turn, Lync Server includes a number of cmdlets for managing Address Book servers.</span></span>

<div>

## <a name="address-book-server-cmdlets"></a><span data-ttu-id="567c5-110">Командлеты сервера адресной книги</span><span class="sxs-lookup"><span data-stu-id="567c5-110">Address Book Server Cmdlets</span></span>

<span data-ttu-id="567c5-111">Вы не можете настроить параметры сервера адресной книги на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="567c5-111">You cannot configure the Address Book Server settings in Lync Server Control Panel.</span></span> <span data-ttu-id="567c5-112">Windows PowerShell — это основной инструмент для управления этими параметрами.</span><span class="sxs-lookup"><span data-stu-id="567c5-112">Windows PowerShell is the primary tool for managing these settings.</span></span> <span data-ttu-id="567c5-113">Ниже приведен список командлетов, непосредственно связанных с администрированием сервера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="567c5-113">The following is a list of cmdlets that relate directly to managing the Address Book Server:</span></span>

<span data-ttu-id="567c5-114">**адресной книги**</span><span class="sxs-lookup"><span data-stu-id="567c5-114">**Address Book Server**</span></span>

  - <span></span>  
    <span data-ttu-id="567c5-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="567c5-116">[New-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-116">[New-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="567c5-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="567c5-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="567c5-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="567c5-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="567c5-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="567c5-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="567c5-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="567c5-123">См. также</span><span class="sxs-lookup"><span data-stu-id="567c5-123">See Also</span></span>


[<span data-ttu-id="567c5-124">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="567c5-124">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="567c5-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="567c5-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

