---
title: 'Lync Server 2013: Просмотр списка надежных приложений'
description: 'Lync Server 2013: Просмотр списка надежных приложений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View a list of trusted applications
ms:assetid: f09300b3-67cf-4e70-a51a-23d62479b913
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182604(v=OCS.15)
ms:contentKeyID: 48185844
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01d45c682550640c3fc7284e0b60ca6844896b5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444114"
---
# <a name="view-a-list-of-trusted-applications-in-lync-server-2013"></a><span data-ttu-id="bd610-103">Просмотр списка надежных приложений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd610-103">View a list of trusted applications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd610-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd610-104">

<span> </span></span></span>

<span data-ttu-id="bd610-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="bd610-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="bd610-106">Вы можете использовать панель управления Lync Server 2013 для просмотра списка доверенных приложений, развернутых в среде Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bd610-106">You can use Lync Server 2013 Control Panel to view a list of the trusted applications that you have deployed in your Lync Server 2013 environment.</span></span> <span data-ttu-id="bd610-107">Надежное приложение — это приложение, основанное на управляемом наборе API Microsoft Unified Communications (UCMA 3,0), который является надежным для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bd610-107">A trusted application is an application based on Microsoft Unified Communications Managed API (UCMA) 3.0 Core SDK that is trusted by Lync Server 2013.</span></span> <span data-ttu-id="bd610-108">Это отношение доверия представлено в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="bd610-108">This trust relationship is summarized in the following list:</span></span>

  - <span data-ttu-id="bd610-109">Доверенные приложения не предназначены для проверки подлинности на сервере Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd610-109">Trusted applications are not challenged for authentication by Lync Server.</span></span>

  - <span data-ttu-id="bd610-110">Доверенные приложения не заменяются на Lync Server для транзакций SIP, подключений и исходящих голосовых вызовов по протоколу VoIP.</span><span class="sxs-lookup"><span data-stu-id="bd610-110">Trusted applications are not throttled by Lync Server for SIP transactions, connections or outgoing Voice over Internet Protocol (VoIP) calls.</span></span>

  - <span data-ttu-id="bd610-111">Доверенные приложения могут олицетворять любого пользователя и могут присоединиться к конференциям без отображения в списке.</span><span class="sxs-lookup"><span data-stu-id="bd610-111">Trusted applications can impersonate any user and can join conferences without appearing in rosters.</span></span>

  - <span data-ttu-id="bd610-112">Доверенные приложения являются высокодоступными и устойчивыми.</span><span class="sxs-lookup"><span data-stu-id="bd610-112">Trusted applications are highly available and resilient.</span></span>

<span data-ttu-id="bd610-113">На панели управления Lync Server вы можете просматривать имена приложений, пула, в которых они выполняются, и используемого ими порта.</span><span class="sxs-lookup"><span data-stu-id="bd610-113">In Lync Server Control Panel, you can see the name of the applications, the pool where they run, and the port they use.</span></span>

<div>

## <a name="to-view-a-list-of-trusted-applications"></a><span data-ttu-id="bd610-114">Просмотр списка надежных приложений</span><span class="sxs-lookup"><span data-stu-id="bd610-114">To view a list of trusted applications</span></span>

1.  <span data-ttu-id="bd610-115">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи, назначенной роли CsServerAdministrator, CsAdministrator, CsHelpDesk или CsViewOnlyAdministrator.</span><span class="sxs-lookup"><span data-stu-id="bd610-115">From a user account that is assigned to the CsServerAdministrator, CsAdministrator, CsHelpDesk, or CsViewOnlyAdministrator role, log on to any computer in your internal deployment.</span></span> <span data-ttu-id="bd610-116">Подробные сведения о стандартных ролях администратора, доступных в Lync Server 2013, можно найти [в разделе Планирование управления доступом на основе ролей в Lync server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="bd610-116">For details about the predefined administrative roles available in Lync Server 2013, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span></span>

2.  <span data-ttu-id="bd610-117">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd610-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bd610-118">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bd610-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bd610-119">На панели навигации слева щелкните **топология** и выберите пункт **доверенное приложение**.</span><span class="sxs-lookup"><span data-stu-id="bd610-119">In the left navigation bar, click **Topology** and the click **Trusted Application**.</span></span>

4.  <span data-ttu-id="bd610-120">На странице **Trusted Application (доверенное приложение** ) щелкните заголовок столбца, чтобы отсортировать приложения, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="bd610-120">On the **Trusted Application** page, click a column heading to sort the applications, if needed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bd610-121">См. также</span><span class="sxs-lookup"><span data-stu-id="bd610-121">See Also</span></span>


[<span data-ttu-id="bd610-122">Управление топологией Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd610-122">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="bd610-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd610-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

