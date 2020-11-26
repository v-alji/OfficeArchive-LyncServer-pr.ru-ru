---
title: 'Lync Server 2013: назначение политик конференции для поддержки анонимных пользователей'
description: 'Lync Server 2013: назначение политик конференц-связи для поддержки анонимных пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign conferencing policies to support anonymous users
ms:assetid: 662de022-1111-40f7-bad4-f2b686f30973
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521007(v=OCS.15)
ms:contentKeyID: 48184333
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e94c3097e3e21f854e91fdee1ad0b33c3b9f53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443213"
---
# <a name="assign-conferencing-policies-to-support-anonymous-users-in-lync-server-2013"></a><span data-ttu-id="9e559-103">Назначение политик конференции для поддержки анонимных пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e559-103">Assign conferencing policies to support anonymous users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e559-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e559-104">

<span> </span></span></span>

<span data-ttu-id="9e559-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="9e559-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="9e559-106">По умолчанию всем пользователям запрещено приглашать анонимных пользователей для участия в собрании.</span><span class="sxs-lookup"><span data-stu-id="9e559-106">By default, all users are prevented from inviting anonymous users to participate in a meeting.</span></span> <span data-ttu-id="9e559-107">Вы можете управлять тем, кто может приглашать анонимных пользователей, настроив политику конференций для поддержки анонимных пользователей и применяя эту политику конференций к определенным пользователям.</span><span class="sxs-lookup"><span data-stu-id="9e559-107">You control who can invite anonymous users by configuring a conferencing policy to support anonymous users, and applying that conferencing policy to specific users.</span></span> <span data-ttu-id="9e559-108">Дополнительные сведения о настройке политик конференц-связи для поддержки анонимных пользователей можно найти [в разделе Создание или изменение политики конференц-связи в Lync server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md) и [Управление интеграцией и внешним доступом к Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="9e559-108">For details about how to configure a conferencing policies to support anonymous users, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md) and [Managing federation and external access to Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span></span>

<span data-ttu-id="9e559-109">В этом разделе описана процедура применения политики конференц-связи, уже созданной для одного или нескольких пользователей или групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="9e559-109">Use the procedure in this section to apply a conferencing policy that you have already created to one or more users or user groups.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9e559-110">Помимо настройки и применения политики для предоставления пользователям возможности приглашать анонимных пользователей, необходимо также включить поддержку анонимных пользователей для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="9e559-110">In addition to configuring and applying a policy to enable users to invite anonymous users, you must also enable support for anonymous users for your organization.</span></span> <span data-ttu-id="9e559-111">Подробности можно найти <A href="lync-server-2013-configure-policies-to-control-public-user-access.md">в разделе Настройка политик для доступа пользователей Public в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9e559-111">For details, see <A href="lync-server-2013-configure-policies-to-control-public-user-access.md">Configure policies to control public user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-configure-a-user-policy-for-anonymous-participation-in-meetings"></a><span data-ttu-id="9e559-112">Настройка политики пользователя для анонимного участия в собраниях</span><span class="sxs-lookup"><span data-stu-id="9e559-112">To configure a user policy for anonymous participation in meetings</span></span>

1.  <span data-ttu-id="9e559-113">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="9e559-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9e559-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9e559-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9e559-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9e559-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9e559-116">На панели навигации слева выберите **Конференц**-связь, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="9e559-116">In the left navigation bar, click **Conferencing**, and then do one of the following:</span></span>
    
    1.  <span data-ttu-id="9e559-117">Чтобы создать политику пользователя, нажмите кнопку **создать** и выберите пункт **Политика пользователя**.</span><span class="sxs-lookup"><span data-stu-id="9e559-117">To create a new user policy, click **New**, and then click **User policy**.</span></span> <span data-ttu-id="9e559-118">Создайте уникальное имя в поле **Name (имя** ), которое указывает политику пользователя (например, **EnableAnonymous** для политики пользователя, которая включает связь с анонимными пользователями).</span><span class="sxs-lookup"><span data-stu-id="9e559-118">Create a unique name in the **Name** field that indicates what the user policy covers (for example, **EnableAnonymous** for a user policy that enables communications with anonymous users).</span></span>
    
    2.  <span data-ttu-id="9e559-119">Чтобы настроить существующую политику пользователей, щелкните соответствующую политику, указанную в таблице, и выберите команду **изменить**, а затем — **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="9e559-119">To configure an existing user policy, click the appropriate policy listed in the table, click **Edit**, and then click **Show details**.</span></span>

4.  <span data-ttu-id="9e559-120">В диалоговом окне **политики Конференц** -связи установите флажок **Разрешить участникам приглашать анонимных пользователей** .</span><span class="sxs-lookup"><span data-stu-id="9e559-120">In the **Conferencing Policies** dialog box, select the **Allow participants to invite anonymous users** check box.</span></span>

5.  <span data-ttu-id="9e559-121">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="9e559-121">Click **Commit**.</span></span>

6.  <span data-ttu-id="9e559-122">На панели навигации слева выберите пункт **Пользователи**, а затем выполните поиск по учетной записи пользователя, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="9e559-122">In the left navigation bar, click **Users**, search on the user account that you want to configure.</span></span>

7.  <span data-ttu-id="9e559-123">В таблице с результатами поиска выберите нужную учетную запись, нажмите кнопку **Изменить** и выберите пункт **Показать сведения**.</span><span class="sxs-lookup"><span data-stu-id="9e559-123">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

8.  <span data-ttu-id="9e559-124">В диалоговом окне **изменение пользователя Lync Server** в разделе **Политика Конференц**-связи выберите политику пользователей с конфигурацией "анонимный доступ", которую вы хотите применить для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e559-124">In **Edit Lync Server User** under **Conferencing policy**, select the user policy with the anonymous user access configuration that you want to apply to this user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9e559-125">Параметры <STRONG> &lt; автоматической &gt; </STRONG> настройки применяются к параметрам установки сервера по умолчанию и автоматически применяются сервером.</span><span class="sxs-lookup"><span data-stu-id="9e559-125">The <STRONG>&lt;Automatic&gt;</STRONG> settings apply the default server installation settings and are applied automatically by the server.</span></span>

    
    </div>

<span data-ttu-id="9e559-126">Чтобы разрешить пользователям приглашать анонимных пользователей на Конференции, необходимо также включить поддержку анонимных пользователей в Организации.</span><span class="sxs-lookup"><span data-stu-id="9e559-126">To enable users to invite anonymous users to conferences, you must also enable support for anonymous users in your organization.</span></span> <span data-ttu-id="9e559-127">Подробности можно найти в разделе [Настройка политик для управления доступом пользователей в Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md) в документации по развертыванию или документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="9e559-127">For details, see [Configure policies to control public user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="9e559-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e559-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

