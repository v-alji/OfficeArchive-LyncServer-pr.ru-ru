---
title: 'Lync Server 2013: Test-CsAddressBookWebQuery для управления адресными книгами'
description: 'Lync Server 2013: Test-CsAddressBookWebQuery для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookWebQuery for Address Book management
ms:assetid: 977a9c1f-5f4e-4539-9a26-8748b61a57d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429716(v=OCS.15)
ms:contentKeyID: 48184865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7448733ed1477d36b887648154d66c96f9e6d0b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441258"
---
# <a name="test-csaddressbookwebquery-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="9521d-103">Test-CsAddressBookWebQuery для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9521d-103">Test-CsAddressBookWebQuery for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9521d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9521d-104">

<span> </span></span></span>

<span data-ttu-id="9521d-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9521d-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9521d-106">Кто может запустить этот командлет: по умолчанию членам указанных ниже групп разрешено выполнять командлет Test-CsAddressBookWebQuery: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="9521d-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookWebQuery cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="9521d-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9521d-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

<span data-ttu-id="9521d-108">Как и в случае с Test-CsAddressBookService синтетической транзакцией, Test-CsAddressBookWebQuery выполняет запрос для веб-запроса адресной книги, чтобы убедиться, что он работает правильно.</span><span class="sxs-lookup"><span data-stu-id="9521d-108">Similar to the Test-CsAddressBookService synthetic transaction, Test-CsAddressBookWebQuery performs a query against the Address Book Web Query to ensure that it is operating properly.</span></span> <span data-ttu-id="9521d-109">Командлет подключится к проверке подлинности веб-билета и отобразит учетные данные, указанные в – UserCredential.</span><span class="sxs-lookup"><span data-stu-id="9521d-109">The cmdlet will connect to the Web Ticket authentication and present the credentials specified in –UserCredential.</span></span> <span data-ttu-id="9521d-110">Если прошедший проверку подлинности, командлет выдает сведения о – TargetSipAddress.</span><span class="sxs-lookup"><span data-stu-id="9521d-110">If authenticated, the cmdlet then present the –TargetSipAddress information.</span></span> <span data-ttu-id="9521d-111">Командлет должен сообщить об успешном завершении, если он смог получить информацию о контакте.</span><span class="sxs-lookup"><span data-stu-id="9521d-111">The cmdlet should report success if it was able to retrieve the information about the contact.</span></span>

<span data-ttu-id="9521d-112">Например:</span><span class="sxs-lookup"><span data-stu-id="9521d-112">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com" -TargetSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a><span data-ttu-id="9521d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9521d-113">See Also</span></span>


[<span data-ttu-id="9521d-114">Test-CsAddressBookWebQuery</span><span class="sxs-lookup"><span data-stu-id="9521d-114">Test-CsAddressBookWebQuery</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery)  
  

<span data-ttu-id="9521d-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9521d-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

