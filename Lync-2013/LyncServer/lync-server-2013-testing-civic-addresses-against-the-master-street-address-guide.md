---
title: Тестирование многоадресных адресов в главном руководстве почтового адреса
description: Проверка административного адреса в соответствии с основным адресом в главном почтовом руководстве.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing civic addresses against the master street address guide
ms:assetid: dc680de9-2a0f-4fd3-a99e-9bab0bc30ae5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690132(v=OCS.15)
ms:contentKeyID: 63969657
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16e0d721b70e3db175b2d23ddee6f59d13a13c4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439830"
---
# <a name="testing-civic-addresses-against-the-master-street-address-guide-in-lync-server-2013"></a><span data-ttu-id="d98ae-103">Проверка многоадресных адресов в главном руководстве почтового адреса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d98ae-103">Testing civic addresses against the master street address guide in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d98ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d98ae-104">

<span> </span></span></span>

<span data-ttu-id="d98ae-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="d98ae-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d98ae-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="d98ae-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="d98ae-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="d98ae-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d98ae-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="d98ae-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="d98ae-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d98ae-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d98ae-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="d98ae-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="d98ae-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d98ae-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="d98ae-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsRegistration.</span><span class="sxs-lookup"><span data-stu-id="d98ae-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="d98ae-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d98ae-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisCivicAddress &quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="d98ae-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d98ae-114">Description</span></span>

<span data-ttu-id="d98ae-115">Командлет Test-CsLisCivicAddress используется для проверки местоположений, добавленных в базу данных службы сведений о расположении (LIS).</span><span class="sxs-lookup"><span data-stu-id="d98ae-115">The Test-CsLisCivicAddress cmdlet is used to verify locations that were added to your Location Information service (LIS) database.</span></span> <span data-ttu-id="d98ae-116">Командлет выполняет сравнение расположений с расположениями в главном руководстве по адресу (MSAG), которые относятся к поставщику сетевой маршрутизации E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="d98ae-116">The cmdlet works by comparing locations against the locations found in the Master Street Address Guide (MSAG) that belongs to your E9-1-1 Network Routing Provider.</span></span> <span data-ttu-id="d98ae-117">Если у вас нет провайдера сетевой маршрутизации или если поставщик недоступен, тесты завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="d98ae-117">If you do not have a network routing provider or if the provider cannot be reached, then your tests will fail.</span></span>

<span data-ttu-id="d98ae-118">Если вы добавите в команду необязательный параметр ключа UpdateValidationStatus, для соответствующего свойства базы данных MSAGValid будет задано значение "true" для каждого адреса, продающего проверку.</span><span class="sxs-lookup"><span data-stu-id="d98ae-118">If you add the optional switch parameter UpdateValidationStatus to your command, then the corresponding MSAGValid database property will be set to True for each address passing the test.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="d98ae-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="d98ae-119">Running the test</span></span>

<span data-ttu-id="d98ae-120">Командлет Test-CsLisCivicAddress можно использовать для проверки отдельных адресов или проверки нескольких адресов.</span><span class="sxs-lookup"><span data-stu-id="d98ae-120">The Test-CsLisCivicAddress cmdlet can be used to test individual addresses or to test multiple addresses.</span></span> <span data-ttu-id="d98ae-121">Например, эта команда проверяет один адрес, указанный в Редмонде, WA:</span><span class="sxs-lookup"><span data-stu-id="d98ae-121">For example, this command tests a single address located in Redmond, WA:</span></span>

    Test-CsLisCivicAddress -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName Main -StreetSuffix St -PostDirectional "" -City Redmond -State WA -PostalCode 98052 -Country US -UpdateValidationStatus

<span data-ttu-id="d98ae-122">По сравнению с этой командой проверяются все адреса, находящиеся в базе данных LIS.</span><span class="sxs-lookup"><span data-stu-id="d98ae-122">By comparison, this command tests all the addresses currently in your LIS database:</span></span>

    Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus

<span data-ttu-id="d98ae-123">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="d98ae-123">For more information, see the Help documentation for the [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="d98ae-124">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="d98ae-124">Determining success or failure</span></span>

<span data-ttu-id="d98ae-125">Test-CsLisCivicAddress сообщит об успешном завершении или сбое для указанных адресов.</span><span class="sxs-lookup"><span data-stu-id="d98ae-125">Test-CsLisCivicAddress will report back Success or Failure for the supplied addresses.</span></span> <span data-ttu-id="d98ae-126">Если адрес не удается найти или не удается связаться с поставщиком услуг, проверка адреса завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="d98ae-126">An address test will fail if the address cannot be found or if the service provider cannot be contacted.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="d98ae-127">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="d98ae-127">Reasons why the test might have failed</span></span>

<span data-ttu-id="d98ae-128">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsLisCivicAddress.</span><span class="sxs-lookup"><span data-stu-id="d98ae-128">Here are some common reasons why Test-CsLisCivicAddress might fail:</span></span>

  - <span data-ttu-id="d98ae-129">Поставщик услуг LIS может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="d98ae-129">The LIS service provider might not be available.</span></span> <span data-ttu-id="d98ae-130">Вы можете получить URL-адрес поставщика услуг LIS, выполнив командлет Get-CsLisConfiguration:</span><span class="sxs-lookup"><span data-stu-id="d98ae-130">You can retrieve the URL of your LIS service provider by running the Get-CsLisConfiguration cmdlet:</span></span>
    
        Get-CsLisConfiguration 
    
    <span data-ttu-id="d98ae-131">Затем вы можете проверить связь с этим URL-адресом, чтобы убедиться, что поставщик услуг доступен.</span><span class="sxs-lookup"><span data-stu-id="d98ae-131">You can then ping that URL to verify that the service provider is available.</span></span>

<span data-ttu-id="d98ae-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d98ae-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

