---
title: 'Lync Server 2013: настройка политик для управления удаленным доступом пользователей'
description: 'Lync Server 2013: Настройте политики для управления доступом удаленных пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure policies to control remote user access
ms:assetid: 8f556849-692b-44a0-9514-4468fc9a39d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398725(v=OCS.15)
ms:contentKeyID: 48184825
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6408747cfbbc5e7dff8fd198c0de162f49fc5ff2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433775"
---
# <a name="configure-policies-to-control-remote-user-access-in-lync-server-2013"></a><span data-ttu-id="d3560-103">Настройка политик для управления удаленным доступом пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3560-103">Configure policies to control remote user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3560-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3560-104">

<span> </span></span></span>

<span data-ttu-id="d3560-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="d3560-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="d3560-106">Вы настраиваете одну или несколько политик доступа внешних пользователей, чтобы указать, могут ли удаленные пользователи работать вместе с внутренними пользователями Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d3560-106">You configure one or more external user access policies to control whether remote users can collaborate with internal Lync Server users.</span></span> <span data-ttu-id="d3560-107">Для управления доступом удаленных пользователей можно настроить политики на уровне Global, site и User.</span><span class="sxs-lookup"><span data-stu-id="d3560-107">To control remote user access, you can configure policies at the global, site, and user level.</span></span> <span data-ttu-id="d3560-108">Политики сайта переопределяют глобальную политику, а политики пользователей переопределяют сайт и глобальные политики.</span><span class="sxs-lookup"><span data-stu-id="d3560-108">Site policies override the global policy, and user policies override site and global policies.</span></span> <span data-ttu-id="d3560-109">Подробные сведения о типах политик, которые можно настроить, приведены в разделе [Управление интеграцией и внешним доступом к Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="d3560-109">For details about the types of policies that you can configure, see [Managing federation and external access to Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span></span> <span data-ttu-id="d3560-110">Параметры политики сервера Lync Server, примененные на одном уровне политики, могут переопределять параметры, примененные на другом уровне политики.</span><span class="sxs-lookup"><span data-stu-id="d3560-110">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="d3560-111">Приоритет политики Lync Server: политика пользователей (наибольшее влияние) переопределяет политику сайта, а затем политика сайта переопределяет глобальную политику (наименее влияние).</span><span class="sxs-lookup"><span data-stu-id="d3560-111">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="d3560-112">То есть, чем ближе параметр политики к объекту, на который она влияет, тем больше влияния она оказывает на объект.</span><span class="sxs-lookup"><span data-stu-id="d3560-112">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d3560-113">Вы можете настроить политики для управления доступом удаленных пользователей даже в том случае, если вы не включили удаленный доступ для пользователей для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="d3560-113">You can configure policies to control remote user access, even if you have not enabled remote user access for your organization.</span></span> <span data-ttu-id="d3560-114">Тем не менее, настроенные политики действуют только в том случае, если для Организации разрешен доступ к удаленному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d3560-114">However, the policies that you configure are in effect only when you have remote user access enabled for your organization.</span></span> <span data-ttu-id="d3560-115">Дополнительные сведения о включении удаленного доступа пользователей можно найти в статьях <A href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение и отключение служб федерации и общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d3560-115">For details about enabling remote user access, see <A href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</A>.</span></span> <span data-ttu-id="d3560-116">Кроме того, если указать политику пользователей для управления доступом удаленных пользователей, политика применяется только для пользователей, которые включены в Lync Server и настроены на использование политики.</span><span class="sxs-lookup"><span data-stu-id="d3560-116">Additionally, if you specify a user policy to control remote user access, the policy applies only to users that are enabled for Lync Server and configured to use the policy.</span></span> <span data-ttu-id="d3560-117">Подробные сведения об указании пользователей, которые могут входить на сервер Lync Server из удаленных местоположений, приведены в разделе <A href="lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md">назначение внешней политики доступа пользователей для пользователей Lync в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d3560-117">For details about specifying users that can sign in to Lync Server from remote locations, see <A href="lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md">Assign an external user access policy to a Lync enabled user in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="d3560-118">Для настройки каждой внешней политики доступа, которую вы хотите использовать для управления доступом удаленных пользователей, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d3560-118">Use the following procedure to configure each external access policy that you want to use to control remote user access.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d3560-119">В этой статье описано, как настроить политику только для обеспечения взаимодействия с удаленными пользователями, но каждая из политик, настроенных для поддержки удаленного доступа пользователей, также может настроить доступ федеративного пользователя и доступ Public Users.</span><span class="sxs-lookup"><span data-stu-id="d3560-119">This procedure describes how to configure a policy only to enable communications with remote users, but each policy that you configure to support remote user access can also configure federated user access and public user access.</span></span> <span data-ttu-id="d3560-120">Дополнительные сведения о настройке политик для поддержки федеративных пользователей можно найти <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">в разделе Настройка политик для управления доступом пользователей Федерации в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d3560-120">For details about configuring policies to support federated users, see <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</A>.</span></span> <span data-ttu-id="d3560-121">Дополнительные сведения о настройке политик для поддержки открытых пользователей можно найти <A href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">в статьях создание и изменение общедоступных федеративных поставщиков SIP в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d3560-121">For details about configuring policies to support public users, see <A href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-configure-an-external-access-policy-to-support-remote-user-access"></a><span data-ttu-id="d3560-122">Настройка политики внешнего доступа для поддержки удаленного доступа пользователей</span><span class="sxs-lookup"><span data-stu-id="d3560-122">To configure an external access policy to support remote user access</span></span>

1.  <span data-ttu-id="d3560-123">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d3560-123">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d3560-124">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d3560-124">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d3560-125">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d3560-125">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d3560-126">На панели навигации слева выберите **внешний доступ для пользователей** и нажмите кнопку **Политика внешних доступа**.</span><span class="sxs-lookup"><span data-stu-id="d3560-126">In the left navigation bar, click **External User Access**, and then click **External Access Policy**.</span></span>

4.  <span data-ttu-id="d3560-127">На странице " **политика внешней доступа** " выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="d3560-127">On the **External Access Policy** page, do one of the following:</span></span>
    
      - <span data-ttu-id="d3560-128">Чтобы настроить глобальную политику для поддержки удаленного доступа пользователей, щелкните глобальную политику, нажмите кнопку **изменить**, а затем выберите пункт **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="d3560-128">To configure the global policy to support remote user access, click the global policy, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="d3560-129">Чтобы создать новую политику сайта, нажмите кнопку **создать** и выберите пункт **Политика сайта**.</span><span class="sxs-lookup"><span data-stu-id="d3560-129">To create a new site policy, click **New**, and then click **Site policy**.</span></span> <span data-ttu-id="d3560-130">В разделе **выберите сайт** выберите нужный сайт из списка и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3560-130">In **Select a Site**, click the appropriate site from the list and then click **OK**.</span></span>
    
      - <span data-ttu-id="d3560-131">Чтобы создать политику пользователя, нажмите кнопку **создать** и выберите пункт **Политика пользователя**.</span><span class="sxs-lookup"><span data-stu-id="d3560-131">To create a new user policy, click **New**, and then click **User policy**.</span></span> <span data-ttu-id="d3560-132">В **новой политике внешнего доступа** Создайте уникальное имя в поле Name ( **имя** ), которое указывает политику пользователя (например, **EnableRemoteUsers** для политики пользователя, которая позволяет использовать связь для удаленных пользователей).</span><span class="sxs-lookup"><span data-stu-id="d3560-132">In **New External Access Policy**, create a unique name in the **Name** field that indicates what the user policy covers (for example, **EnableRemoteUsers** for a user policy that enables communications for remote users).</span></span>
    
      - <span data-ttu-id="d3560-133">Чтобы изменить существующую политику, выберите соответствующую политику, указанную в таблице, и нажмите кнопку **изменить**, а затем выберите команду **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="d3560-133">To change an existing policy, click the appropriate policy listed in the table, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="d3560-134">Необязательно Если вы хотите добавить или изменить описание, укажите сведения о политике в **описании**.</span><span class="sxs-lookup"><span data-stu-id="d3560-134">(Optional) If you want to add or edit a description, specify the information for the policy in **Description**.</span></span>

6.  <span data-ttu-id="d3560-135">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="d3560-135">Do one of the following:</span></span>
    
      - <span data-ttu-id="d3560-136">Чтобы разрешить удаленному пользователю доступ к политике, установите флажок **разрешить связь с удаленными пользователями** .</span><span class="sxs-lookup"><span data-stu-id="d3560-136">To enable remote user access for the policy, select the **Enable communications with remote users** check box.</span></span>
    
      - <span data-ttu-id="d3560-137">Чтобы запретить удаленному пользователю доступ к политике, снимите флажок **разрешить связь с удаленными пользователями** .</span><span class="sxs-lookup"><span data-stu-id="d3560-137">To disable remote user access for the policy, clear the **Enable communications with remote users** check box.</span></span>

7.  <span data-ttu-id="d3560-138">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="d3560-138">Click **Commit**.</span></span>

<span data-ttu-id="d3560-139">Для обеспечения удаленного доступа пользователей необходимо также включить поддержку удаленного доступа пользователей в своей организации.</span><span class="sxs-lookup"><span data-stu-id="d3560-139">To enable remote user access, you must also enable support for remote user access in your organization.</span></span> <span data-ttu-id="d3560-140">Дополнительные сведения можно найти [в разделе Включение и отключение подключения к службам интеграции и обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) в документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="d3560-140">For details, see [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="d3560-141">Если это политика пользователя, необходимо также применить политику для пользователей, которые должны иметь возможность удаленно подключаться.</span><span class="sxs-lookup"><span data-stu-id="d3560-141">If this is a user policy, you must also apply the policy to users that you want to be able to connect remotely.</span></span> <span data-ttu-id="d3560-142">Дополнительные сведения можно найти в разделе [назначение внешней политики доступа для пользователя Lync, доступного в Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md) , в документации по развертыванию или документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="d3560-142">For details, see [Assign an external user access policy to a Lync enabled user in Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="d3560-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3560-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

