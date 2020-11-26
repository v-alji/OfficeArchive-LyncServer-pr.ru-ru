---
title: 'Lync Server 2013: перенос пользователей в единое хранилище контактов'
description: 'Lync Server 2013: перенос пользователей в единое хранилище контактов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrate users to unified contact store
ms:assetid: 215a8ec1-d63e-4fdf-b73d-75aeb9dddb43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204737(v=OCS.15)
ms:contentKeyID: 48183600
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e9ee9850cc723ae132f15d7c0c6b3769e1240ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425593"
---
# <a name="migrate-users-to-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="eab08-103">Перенос пользователей в единое хранилище контактов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eab08-103">Migrate users to unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eab08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eab08-104">

<span> </span></span></span>

<span data-ttu-id="eab08-105">_**Тема последнего изменения:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="eab08-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="eab08-106">Пользовательские контакты автоматически переносятся на сервер Exchange 2013, когда пользователь:</span><span class="sxs-lookup"><span data-stu-id="eab08-106">A user's contacts are automatically migrated to the Exchange 2013 server when the user:</span></span>

  - <span data-ttu-id="eab08-107">Назначена политика пользовательских служб, у которой UcsAllowed установлено значение true.</span><span class="sxs-lookup"><span data-stu-id="eab08-107">Has been assigned a user services policy that has UcsAllowed set to True.</span></span>

  - <span data-ttu-id="eab08-108">Была настроена с помощью почтового ящика Exchange 2013 и один раз вошел в почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="eab08-108">Has been provisioned with an Exchange 2013 mailbox and has signed into the mailbox at least once.</span></span>

  - <span data-ttu-id="eab08-109">Войдите в систему с помощью клиента Lync 2013 с богатыми возможностями.</span><span class="sxs-lookup"><span data-stu-id="eab08-109">Logs in by using a Lync 2013 rich client.</span></span>

<span data-ttu-id="eab08-110">Если пользователь входит в систему с помощью клиента Lync 2010 или более ранней версии или пользователь не подключен к серверу Exchange 2013, политика служб пользователей игнорируется, а контакты пользователя остаются в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eab08-110">If the user logs in with a Lync 2010 or earlier client, or if the user is not connected to an Exchange 2013 server, the user services policy is ignored and the user's contacts remain in Lync Server.</span></span>

<span data-ttu-id="eab08-111">Чтобы определить, перенесены ли контакты пользователя, используйте один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="eab08-111">You can determine whether a user's contacts have been migrated by using either of the following methods:</span></span>

  - <span data-ttu-id="eab08-112">На клиентском компьютере проверьте следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="eab08-112">Check the following registry key on the client computer:</span></span>
    
    <span data-ttu-id="eab08-113">Приложение hKey для \_ текущего \_ пользователя \\ \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ \<SIP URL\> \\ UCS</span><span class="sxs-lookup"><span data-stu-id="eab08-113">HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\\<SIP URL\>\\UCS</span></span>
    
    <span data-ttu-id="eab08-114">Если контакты пользователя хранятся в Exchange 2013, в этом разделе содержится значение InUCSMode со значением 2165.</span><span class="sxs-lookup"><span data-stu-id="eab08-114">If the user's contacts are stored in Exchange 2013, this key contains a value of InUCSMode with a value of 2165.</span></span>

  - <span data-ttu-id="eab08-115">Запустите командлет **Test-CsUnifiedContactStore** .</span><span class="sxs-lookup"><span data-stu-id="eab08-115">Run the **Test-CsUnifiedContactStore** cmdlet.</span></span> <span data-ttu-id="eab08-116">В командной строке оболочки Lync Server Management Shell введите:</span><span class="sxs-lookup"><span data-stu-id="eab08-116">At the Lync Server Management Shell command line, type:</span></span>
    
        Test-CsUnifiedContactStore -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="eab08-117">Если **тест-CsUnifiedContactStore** выполняется успешно, контакты пользователя были перенесены в единое хранилище контактов.</span><span class="sxs-lookup"><span data-stu-id="eab08-117">If **Test-CsUnifiedContactStore** succeeds, the user's contacts were migrated to unified contact store.</span></span>

<span data-ttu-id="eab08-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eab08-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

