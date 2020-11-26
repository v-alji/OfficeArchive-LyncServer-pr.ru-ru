---
title: Удаление параметров контакта конференц-связи с телефонным подключением для сайта или группы пользователей
description: Удаление параметров контакта конференц-связи с телефонным подключением для сайта или группы пользователей.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete dial-in conferencing PIN settings for a site or group of users
ms:assetid: 15a9faee-d024-4c0e-b2a0-fe7e7dc00589
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520955(v=OCS.15)
ms:contentKeyID: 48183498
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a40168780d5ac5f37ceb33dfaacd25b492d6307a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430478"
---
# <a name="delete-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users-in-lync-server-2013"></a><span data-ttu-id="06c54-103">Удаление параметров контакта конференц-связи с телефонным подключением для сайта или группы пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06c54-103">Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06c54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06c54-104">

<span> </span></span></span>

<span data-ttu-id="06c54-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="06c54-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="06c54-106">Выполните эти действия, чтобы удалить политику ПИН уровня пользователя или сайта.</span><span class="sxs-lookup"><span data-stu-id="06c54-106">Follow these steps to delete a user-level or a site-level PIN policy.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="06c54-107">Глобальную политику ПИН-кодов удалить нельзя.</span><span class="sxs-lookup"><span data-stu-id="06c54-107">You cannot delete the global PIN policy.</span></span>



</div>

<div>

## <a name="to-delete-a-user-or-site-pin-policy"></a><span data-ttu-id="06c54-108">Удаление политики ПИН для пользователя или сайта</span><span class="sxs-lookup"><span data-stu-id="06c54-108">To delete a user or site PIN policy</span></span>

1.  <span data-ttu-id="06c54-109">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06c54-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="06c54-110">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06c54-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="06c54-111">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="06c54-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="06c54-112">В левой панели навигации щелкните элемент **Конференц-связь**, а затем щелкните элемент **Политика ПИН-кодов**.</span><span class="sxs-lookup"><span data-stu-id="06c54-112">In the left navigation bar, click **Conferencing**, and then click **PIN Policy**.</span></span>

4.  <span data-ttu-id="06c54-113">На странице " **политика ПИН-кода** " в поле "Поиск" введите имя или часть имени политики, которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="06c54-113">On the **PIN Policy** page, in the search field, type all or part of the name of the policy you want to delete.</span></span>

5.  <span data-ttu-id="06c54-114">В списке политик выберите необходимую политику, щелкните **Правка**, затем выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="06c54-114">In the list of policies, click the policy that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="06c54-115">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="06c54-115">Click **OK**.</span></span>

<span data-ttu-id="06c54-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06c54-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

