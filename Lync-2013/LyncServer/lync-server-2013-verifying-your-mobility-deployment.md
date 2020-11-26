---
title: 'Lync Server 2013: проверка развертывания среды для мобильной работы'
description: 'Lync Server 2013: Проверка развертывания для мобильных устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verifying your mobility deployment
ms:assetid: 72f9b4d3-57b0-4705-9480-cfdca313a70c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690024(v=OCS.15)
ms:contentKeyID: 48184477
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eadda35438961e469fdd5fa7976762141b26a385
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438878"
---
# <a name="verifying-your-mobility-deployment-in-lync-server-2013"></a><span data-ttu-id="db753-103">Проверка развертывания среды для мобильной работы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db753-103">Verifying your mobility deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db753-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db753-104">

<span> </span></span></span>

<span data-ttu-id="db753-105">_**Тема последнего изменения:** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="db753-105">_**Topic Last Modified:** 2013-02-12_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="db753-106">После развертывания службы Lync Server Mobility Service и службы автообнаружения Lync Server выполните тестовую транзакцию, чтобы убедиться, что развертывание работает правильно.</span><span class="sxs-lookup"><span data-stu-id="db753-106">After you deploy the Lync Server Mobility Service and Lync Server Autodiscover Service, run a test transaction to verify that your deployment works correctly.</span></span> <span data-ttu-id="db753-107">С помощью **теста-CsUcwaConference** можно протестировать возможность двух пользователей, которые используют мобильные клиенты Lync 2013 для создания, присоединения к Конференции и связи с ними.</span><span class="sxs-lookup"><span data-stu-id="db753-107">You can run **Test-CsUcwaConference** to test the ability of two users who are using Lync 2013 Mobile clients to create, join and communicate in a conference.</span></span> <span data-ttu-id="db753-108">Для использования этой тестовой транзакции вам понадобятся два фактических пользователя или тестовых пользователя, а также полные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="db753-108">To use this test transaction, you need two actual users or test users, and their full credentials.</span></span>

<span data-ttu-id="db753-109">С помощью **теста-CsMcxP2PIM** можно протестировать отправку мгновенных сообщений между двумя пользователями, которые используют Lync 2010 Mobile.</span><span class="sxs-lookup"><span data-stu-id="db753-109">You use **Test-CsMcxP2PIM** to test sending an instant message between two users who are using Lync 2010 Mobile.</span></span> <span data-ttu-id="db753-110">Как и в случае с **тестовой CsUcwaConference**, вы используете двух реальных пользователей или двух предопределенных тестовых пользователей.</span><span class="sxs-lookup"><span data-stu-id="db753-110">Similar to **Test-CsUcwaConference**, you use two actual users or two predefined test users.</span></span>

<div>

## <a name="to-test-conferencing-for-lync-2013-mobile-clients"></a><span data-ttu-id="db753-111">Проверка конференций для мобильных клиентов Lync 2013</span><span class="sxs-lookup"><span data-stu-id="db753-111">To test conferencing for Lync 2013 Mobile clients</span></span>

1.  <span data-ttu-id="db753-112">Войдите с правами члена роли CsAdministrator на любой компьютер, на котором установлена командная консоль Lync Server и Ocscore.</span><span class="sxs-lookup"><span data-stu-id="db753-112">Log on as a member of the CsAdministrator role on any computer where Lync Server Management Shell and Ocscore are installed.</span></span>

2.  <span data-ttu-id="db753-113">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="db753-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="db753-114">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="db753-114">At the command line, type:</span></span>
    
        Test-CsUcwaConference -TargetFqdn <FQDN of Front End pool> -Authentication <TrustedServer | Negotiate | ClientCertificate | LiveID> -OrganizerSipAddress sip:<SIP address of test user 1> -OrganizerCredential <test user 1 credentials> -ParticipantSipAddress sip:<SIP address of test user 2> -ParticipantCredential <test user 2 credentials> -v
    
    <span data-ttu-id="db753-115">Вы можете настроить учетные данные в сценарии и передать их в командлет теста.</span><span class="sxs-lookup"><span data-stu-id="db753-115">You can set credentials in a script and pass them to the test cmdlet.</span></span> <span data-ttu-id="db753-116">Например:</span><span class="sxs-lookup"><span data-stu-id="db753-116">For example:</span></span>
    
        $passwd1 = ConvertTo-SecureString "Password01" -AsPlainText -Force
        $passwd2 = ConvertTo-SecureString "Password02" -AsPlainText -Force
        $testuser1 = New-Object Management.Automation.PSCredential("contoso\UserName1", $passwd1)
        $testuser2 = New-Object Management.Automation.PSCredential("contoso\UserName2", $passwd2)
        Test-CsUcwaConference -TargetFqdn pool01.contoso.com -Authentication Negotiate -OrganizerSipAddress sip:UserName1@contoso.com -OrganizerCredential $testuser1 -ParticipantSipAddress sip:UserName2@contoso.com -ParticipantCredential $testuser2 -v

</div>

<div>

## <a name="to-test-person-to-person-instant-messaging-im-for-lync-2010-mobile"></a><span data-ttu-id="db753-117">Проверка обмена мгновенными сообщениями между пользователями в Lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="db753-117">To test person-to-person instant messaging (IM) for Lync 2010 Mobile</span></span>

1.  <span data-ttu-id="db753-118">Войдите с правами члена роли CsAdministrator на любой компьютер, на котором установлена командная консоль Lync Server и Ocscore.</span><span class="sxs-lookup"><span data-stu-id="db753-118">Log on as a member of the CsAdministrator role on any computer where Lync Server Management Shell and Ocscore are installed.</span></span>

2.  <span data-ttu-id="db753-119">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="db753-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="db753-120">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="db753-120">At the command line, type:</span></span>
    
        Test-CsMcxP2PIM -TargetFqdn <FQDN of Front End pool> -Authentication <TrustedServer | Negotiate | ClientCertificate | LiveID> -SenderSipAddress sip:<SIP address of test user 1> -SenderCredential <test user 1 credentials> -ReceiverSipAddress sip:<SIP address of test user 2> -ReceiverCredential <test user 2 credentials> -v
    
    <span data-ttu-id="db753-121">Вы можете настроить учетные данные в сценарии и передать их в командлет теста.</span><span class="sxs-lookup"><span data-stu-id="db753-121">You can set credentials in a script and pass them to the test cmdlet.</span></span> <span data-ttu-id="db753-122">Например:</span><span class="sxs-lookup"><span data-stu-id="db753-122">For example:</span></span>
    
        $passwd1 = ConvertTo-SecureString "Password01" -AsPlainText -Force
        $passwd2 = ConvertTo-SecureString "Password02" -AsPlainText -Force
        $tuc1 = New-Object Management.Automation.PSCredential("contoso\UserName1", $passwd1)
        $tuc2 = New-Object Management.Automation.PSCredential("contoso\UserName2", $passwd2)
        Test-CsMcxP2PIM -TargetFqdn pool01.contoso.com -Authentication Negotiate -SenderSipAddress sip:UserName1@contoso.com -SenderCredential $tuc1 -ReceiverSipAddress sip:UserName2@contoso.com -ReceiverCredential $tuc2 -v

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="db753-123">См. также</span><span class="sxs-lookup"><span data-stu-id="db753-123">See Also</span></span>


[<span data-ttu-id="db753-124">Test-CsMcxP2PIM</span><span class="sxs-lookup"><span data-stu-id="db753-124">Test-CsMcxP2PIM</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM)  
[<span data-ttu-id="db753-125">Test-CsUcwaConference</span><span class="sxs-lookup"><span data-stu-id="db753-125">Test-CsUcwaConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference)  
  

<span data-ttu-id="db753-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db753-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

