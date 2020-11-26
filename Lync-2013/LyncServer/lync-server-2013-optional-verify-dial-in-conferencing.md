---
title: 'Lync Server 2013: проверка конференц-связи с телефонным подключением (необязательно)'
description: 'Lync Server 2013: (необязательно) Проверьте Конференц-связь с телефонным подключением.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify dial-in conferencing
ms:assetid: 3e2b4220-8fb3-442f-98b1-78447adb321f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425905(v=OCS.15)
ms:contentKeyID: 48183941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5e8d3734e89555bf4b298ac68e1e3bd67b1d901
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424858"
---
# <a name="optional-verify-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="712fb-103">Проверка конференц-связи с телефонным подключением в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="712fb-103">(Optional) Verify dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="712fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="712fb-104">

<span> </span></span></span>

<span data-ttu-id="712fb-105">_**Тема последнего изменения:** 2011-01-21_</span><span class="sxs-lookup"><span data-stu-id="712fb-105">_**Topic Last Modified:** 2011-01-21_</span></span>

<span data-ttu-id="712fb-106">Чтобы убедиться, что веб-страница «Параметры конференц-связи с телефонным подключением» и номера доступа к телефонному подключению работают правильно, выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="712fb-106">To verify that the Dial-in Conferencing Settings webpage and the dial-in access numbers work correctly, you need to do the following:</span></span>

  - <span data-ttu-id="712fb-107">Протестируйте веб-страницу «Параметры конференц-связи с телефонным подключением», выполнив вход с использованием простого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="712fb-107">Test the Dial-in Conferencing Settings webpage by signing in to the simple URL.</span></span>

  - <span data-ttu-id="712fb-p101">Протестируйте правильность работы номеров доступа для определенного пула, запустив описанный ниже сценарий. Этот сценарий имитирует звонки на номера доступа. Для его использования вам требуется SIP-адрес и учетные данные одного клиента объединенных коммуникаций, размещенного в этом заданном пуле.</span><span class="sxs-lookup"><span data-stu-id="712fb-p101">Test that access numbers work correctly for a specific pool by running the script later in this topic. This script simulates calls to access numbers. You need the SIP address and credentials of one unified communications (UC) client that is hosted on the specific pool to use this script.</span></span>

<span data-ttu-id="712fb-111">Этот шаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="712fb-111">This step is optional.</span></span>

<div>

## <a name="to-test-access-numbers-for-a-specific-pool"></a><span data-ttu-id="712fb-112">Тестирование номеров доступа для определенного пула</span><span class="sxs-lookup"><span data-stu-id="712fb-112">To test access numbers for a specific pool</span></span>

1.  <span data-ttu-id="712fb-113">Войдите в систему под учетной записью члена группы RTCUniversalServerAdmins или члена роли **CS-ServerAdministrator** или **CsAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="712fb-113">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="712fb-114">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="712fb-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="712fb-115">Выполните следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="712fb-115">Run the following at the command prompt:</span></span>
    
        $credentials = Get-Credential
           User name:  testuser1@contoso.com
           Password:   ********
        Test-CsDialInConferencing -UserSipAddress sip:testuser1@contoso.com -UserCredential $credentials -TargetFqdn <serverName>.<domainName>.com -Verbose
    
    <span data-ttu-id="712fb-p102">Полученный отчет показывает успешность или сбой операции, а также содержит диагностические сведения. Флаг -Verbose позволяет получить более подробные сведения о количестве найденных номеров доступа и их описание.</span><span class="sxs-lookup"><span data-stu-id="712fb-p102">The resulting report shows either Success or Failure, along with specific diagnostic information. The –Verbose flag provides more detailed information about how many access numbers were found and details about them.</span></span>

<span data-ttu-id="712fb-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="712fb-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

