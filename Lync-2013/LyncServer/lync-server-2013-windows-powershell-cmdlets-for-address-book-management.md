---
title: 'Lync Server 2013: командлеты Windows PowerShell для управления адресными книгами'
description: 'Lync Server 2013: командлеты Windows PowerShell для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows PowerShell cmdlets for Address Book management
ms:assetid: 73bfa949-5628-4156-ad20-fe07a0dc6216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429708(v=OCS.15)
ms:contentKeyID: 48184512
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b598d91a4d1a29a67d8f8ceb2477f2d9b96f1319
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446179"
---
# <a name="windows-powershell-cmdlets-for-address-book-services-in-lync-server-2013"></a><span data-ttu-id="bb376-103">Командлеты Windows PowerShell для служб адресной книги в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-103">Windows PowerShell cmdlets for Address Book Services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb376-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb376-104">

<span> </span></span></span>

<span data-ttu-id="bb376-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="bb376-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="bb376-106">Lync Server предоставляет несколько командлетов интерфейса командной строки Windows PowerShell для управления и настройки службы адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bb376-106">Lync Server provides a number of Windows PowerShell command-line interface cmdlets to manage and configure the Address Book service.</span></span> <span data-ttu-id="bb376-107">Некоторые из этих командлетов являются заменой для команд ABServer.exe, используемых в предыдущих версиях Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="bb376-107">Some of these cmdlets are replacements for the ABServer.exe commands used in previous versions of Office Communications Server.</span></span> <span data-ttu-id="bb376-108">В следующих разделах приведены командлеты, которые используются для задания, создания и получения сведений о службе адресной книги, ее конфигурации и сведения о веб-службах, используемых службой адресной книги, когда клиенты извлекают файлы и параметры адресной книги службы.</span><span class="sxs-lookup"><span data-stu-id="bb376-108">In the following topics are the cmdlets that are used to set, create, and retrieve information about the Address Book service, its configuration and information about the Web services that the Address Book service uses when clients retrieve Address Book service files and settings.</span></span>

<span data-ttu-id="bb376-109">Все эти командлеты выдаются в командной консоли Lync Server Management Shell, которую можно найти на сервере или на рабочей станции, где установлены средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="bb376-109">All of these cmdlets are issued through the Lync Server Management Shell found in the Lync Server tools on a server or workstation where the administration tools have been installed.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bb376-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="bb376-110">In This Section</span></span>

  - [<span data-ttu-id="bb376-111">New-CsAddressBookConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-111">New-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-New-CsAddressBookConfiguration-for-address-book-management.md)

  - [<span data-ttu-id="bb376-112">Set-CsAddressBookConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-112">Set-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-set-csaddressbookconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="bb376-113">Get-CsAddressBookConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-113">Get-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-get-csaddressbookconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="bb376-114">Remove-CsAddressBookConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-114">Remove-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-remove-csaddressbookconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="bb376-115">Test-CsAddressBookService для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-115">Test-CsAddressBookService for Address Book management in Lync Server 2013</span></span>](lync-server-2013-test-csaddressbookservice-for-address-book-management.md)

  - [<span data-ttu-id="bb376-116">Test-CsAddressBookWebQuery для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-116">Test-CsAddressBookWebQuery for Address Book management in Lync Server 2013</span></span>](lync-server-2013-test-csaddressbookwebquery-for-address-book-management.md)

  - [<span data-ttu-id="bb376-117">Update-CsAddressBook для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-117">Update-CsAddressBook for Address Book management in Lync Server 2013</span></span>](lync-server-2013-update-csaddressbook-for-address-book-management.md)

  - [<span data-ttu-id="bb376-118">New-CsClientPolicy для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-118">New-CsClientPolicy for Address Book management in Lync Server 2013</span></span>](lync-server-2013-new-csclientpolicy-for-address-book-management.md)

  - [<span data-ttu-id="bb376-119">Set-CsClientPolicy для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-119">Set-CsClientPolicy for Address Book management in Lync Server 2013</span></span>](lync-server-2013-set-csclientpolicy-for-address-book-management.md)

  - [<span data-ttu-id="bb376-120">Get-CsService для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-120">Get-CsService for Address Book management in Lync Server 2013</span></span>](lync-server-2013-get-csservice-for-address-book-management.md)

  - [<span data-ttu-id="bb376-121">New-CsWebServiceConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-121">New-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-New-CsWebServiceConfiguration-for-address-book-management.md)

  - [<span data-ttu-id="bb376-122">Get-CsWebServiceConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-122">Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-get-cswebserviceconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="bb376-123">Set-CsWebServiceConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-123">Set-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-set-cswebserviceconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="bb376-124">Remove-CsWebServiceConfiguration для управления адресными книгами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb376-124">Remove-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-remove-cswebserviceconfiguration-for-address-book-management.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="bb376-125">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="bb376-125">Related Sections</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bb376-126">См. также</span><span class="sxs-lookup"><span data-stu-id="bb376-126">See Also</span></span>


[https://go.microsoft.com/fwlink/p/?linkId=205826](https://go.microsoft.com/fwlink/p/?linkid=205826)  
  

<span data-ttu-id="bb376-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb376-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

