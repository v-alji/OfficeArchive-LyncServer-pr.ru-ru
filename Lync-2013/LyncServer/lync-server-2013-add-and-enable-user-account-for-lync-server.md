---
title: 'Lync Server 2013: Добавление и включение учетной записи пользователя Lync Server'
description: 'Lync Server 2013: Добавление и включение учетной записи пользователя Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add and enable user account for Lync Server
ms:assetid: 1edd1c1c-307d-450b-abea-33aaf56bdf13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520961(v=OCS.15)
ms:contentKeyID: 48183578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f70ae2da122a0db3986a75677c1d29234fbe0e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439375"
---
# <a name="add-and-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="738bf-103">Добавление и включение учетной записи пользователя для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="738bf-103">Add and enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="738bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="738bf-104">

<span> </span></span></span>

<span data-ttu-id="738bf-105">_**Тема последнего изменения:** 2012-11-02_</span><span class="sxs-lookup"><span data-stu-id="738bf-105">_**Topic Last Modified:** 2012-11-02_</span></span>

<span data-ttu-id="738bf-106">После включения учетной записи пользователя в оснастке "пользователи и компьютеры Active Directory" вы можете создавать и включать новые учетные записи пользователей Lync Server 2013 с помощью панели управления Lync Server, добавив на сервер Lync Server пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="738bf-106">After enabling a user account in Active Directory Users and Computers, you can use Lync Server Control Panel to create and enable new Lync Server 2013 user accounts by adding an Active Directory user to Lync Server.</span></span>

<div>

## <a name="to-add-and-enable-a-new-lync-server-user"></a><span data-ttu-id="738bf-107">Добавление и включение нового пользователя Lync Server</span><span class="sxs-lookup"><span data-stu-id="738bf-107">To add and enable a new Lync Server user</span></span>

1.  <span data-ttu-id="738bf-108">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="738bf-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="738bf-109">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="738bf-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="738bf-110">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="738bf-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="738bf-111">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="738bf-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="738bf-112">Нажмите кнопку **включить пользователей**.</span><span class="sxs-lookup"><span data-stu-id="738bf-112">Click **Enable users**.</span></span>

5.  <span data-ttu-id="738bf-113">В диалоговом окне **Новый пользователь Lync Server** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="738bf-113">On the **New Lync Server User** dialog, click **Add**.</span></span>

6.  <span data-ttu-id="738bf-114">В поле **Поиск пользователей** введите полное имя, отображаемое имя, имя, фамилию, имя учетной записи безопасности (SAM), адрес электронной почты, имя участника-пользователя (UPN) или номер телефона нужной учетной записи пользователя Active Directory, а затем нажмите кнопку **найти**.</span><span class="sxs-lookup"><span data-stu-id="738bf-114">In the **Search users** box, type all or the first portion of the name, display name, first name, last name, Security Accounts Manager (SAM) account name, email address, User Principal Name (UPN), or phone number of the Active Directory user account that you want, and then click **Find**.</span></span>

7.  <span data-ttu-id="738bf-115">В таблице выберите учетную запись, которую вы хотите добавить в Lync Server, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="738bf-115">In the table, select the account you want to add to Lync Server, and then click **OK**.</span></span>

8.  <span data-ttu-id="738bf-116">Назначьте пользователю пул, укажите дополнительные сведения и назначьте политики для нужного пользователя, а затем нажмите кнопку **включить**.</span><span class="sxs-lookup"><span data-stu-id="738bf-116">Assign the user to a pool, specify any additional details, and assign the policies to the user you want, and then click **Enable**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="738bf-117">См. также</span><span class="sxs-lookup"><span data-stu-id="738bf-117">See Also</span></span>


[<span data-ttu-id="738bf-118">Отключение и повторное включение учетной записи пользователя для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="738bf-118">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="738bf-119">Удаление учетной записи пользователя из Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="738bf-119">Remove a user account from Lync Server 2013</span></span>](lync-server-2013-remove-a-user-account-from-lync-server.md)  


[<span data-ttu-id="738bf-120">Включение и отключение пользователей для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="738bf-120">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="738bf-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="738bf-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

