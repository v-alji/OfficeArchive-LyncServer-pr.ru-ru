---
title: 'Lync Server 2013: Настройка политик сайта для архивации'
description: 'Lync Server 2013: Настройка политик сайта для архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up site policies for Archiving
ms:assetid: dc2ea206-8b9c-44dd-a479-efb217593c89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205325(v=OCS.15)
ms:contentKeyID: 48185613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 27e5b80b7f62ddc18d418415307457c7f2c4010d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441692"
---
# <a name="setting-up-site-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="6bc4c-103">Настройка политик сайта для архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6bc4c-103">Setting up site policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bc4c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bc4c-104">

<span> </span></span></span>

<span data-ttu-id="6bc4c-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="6bc4c-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="6bc4c-106">Вы можете включить или отключить архивацию для определенных сайтов, создав и настроив политику архивации для каждого из этих сайтов.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-106">You can enable or disable Archiving for specific sites by creating and configuring an Archiving policy for each of those sites.</span></span> <span data-ttu-id="6bc4c-107">Политика сайта переопределяет глобальную политику, а политики пользователей — политики сайта.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-107">A site policy overrides the global policy, but user policies override site policies.</span></span> <span data-ttu-id="6bc4c-108">Правила архивации применяются только в том случае, если вы не используете интеграцию с Microsoft Exchange или если вы используете интеграцию с Microsoft Exchange, но у вас есть несколько пользователей, которые не подключены к Exchange 2013 и почтовые ящики помещаются на In-Place удержание.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-108">Archiving policies only apply if you do not use Microsoft Exchange integration or, if you do use Microsoft Exchange integration, but have some users who are not homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="6bc4c-109">Сведения о том, как работают политики архивации, в том числе иерархия для глобальных политик, политики сайтов и пользователей, описаны [в разделе Архивация в среде Lync Server 2013](lync-server-2013-how-archiving-works.md) , документация по планированию и документация по операциям.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-109">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6bc4c-110">Если вы включили интеграцию Microsoft Exchange для развертывания, In-Place политики хранения данных управляют тем, разрешено ли архивирование для пользователей, использующих Exchange 2013, и почтовые ящики, которые помещаются на In-Place удержание.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-110">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="6bc4c-111">Подробности можно найти в разделе <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Настройка политик архивации в Lync server 2013 при использовании интеграции с Exchange Server</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-111">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="6bc4c-112">Перед активацией архивации внутренних или внешних взаимодействий в политиках архивации необходимо указать все надлежащие параметры в конфигурациях архивации.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-112">You should specify all appropriate options in the Archiving configurations before enabling Archiving of internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="6bc4c-113">Подробности можно найти <A href="lync-server-2013-configuring-archiving-options.md">в разделе Настройка параметров архивации в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-113">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site"></a><span data-ttu-id="6bc4c-114">Создание политики архивации для сайта</span><span class="sxs-lookup"><span data-stu-id="6bc4c-114">To create an archiving policy for a site</span></span>

1.  <span data-ttu-id="6bc4c-115">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-115">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="6bc4c-116">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-116">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span>

3.  <span data-ttu-id="6bc4c-117">На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Политика архивации**.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>
    
    <span data-ttu-id="6bc4c-118">Сведения о том, как работают политики архивации, в том числе иерархия для глобальных политик, политики сайтов и пользователей, описаны [в разделе Архивация в среде Lync Server 2013](lync-server-2013-how-archiving-works.md) , документация по планированию и документация по операциям.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-118">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

4.  <span data-ttu-id="6bc4c-119">Нажмите кнопку **Создать** и выберите **Политика сайта**.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-119">Click **New**, and then click **Site policy**.</span></span>

5.  <span data-ttu-id="6bc4c-120">В окне **Выбор сайта** выберите сайт, к которому нужно применить эту политику.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-120">In **Select a site**, click the site to which the policy is to be applied.</span></span>

6.  <span data-ttu-id="6bc4c-121">В области **Создание новой политики архивации** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-121">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="6bc4c-122">В поле **Имя** укажите имя для политики сайта.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-122">In **Name**, specify the name for the site policy.</span></span>
    
      - <span data-ttu-id="6bc4c-123">В поле **Описание** укажите сведения о назначении политики сайта (например, "политика сайта для Redmond").</span><span class="sxs-lookup"><span data-stu-id="6bc4c-123">In **Description**, provide information about what the site policy is (for example, site policy for Redmond).</span></span>
    
      - <span data-ttu-id="6bc4c-124">Чтобы выбрать управление архивацией внутренних коммуникаций для указанного сайта, установите или снимите флажок **Архивация внутренних взаимодействий**.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-124">To control archiving of internal communications for the specified site, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="6bc4c-125">Чтобы выбрать управление архивацией внешних коммуникаций для указанного сайта, установите или снимите флажок **Архивация внешних взаимодействий**.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-125">To control archiving of external communications for the specified site, select or clear the **Archive external communications** check box.</span></span>

7.  <span data-ttu-id="6bc4c-126">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="6bc4c-126">Click **Commit**.</span></span>

<span data-ttu-id="6bc4c-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bc4c-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

