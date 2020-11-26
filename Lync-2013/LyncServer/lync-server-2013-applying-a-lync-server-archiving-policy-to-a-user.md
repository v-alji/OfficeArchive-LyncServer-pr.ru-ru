---
title: 'Lync Server 2013: применение политики архивации сервера Lync Server для пользователя'
description: 'Lync Server 2013: применение политики архивации сервера Lync Server к пользователю.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Applying a Lync Server Archiving policy to a user
ms:assetid: a23e4876-aa8d-4f49-a3bd-3696616e8290
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205143(v=OCS.15)
ms:contentKeyID: 48185024
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69dcca5601185d65735b963673322a0630af6ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440579"
---
# <a name="applying-a-lync-server-archiving-policy-to-a-user-in-lync-server-2013"></a><span data-ttu-id="cdf21-103">Применение политики архивации в Lync Server к пользователю в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cdf21-103">Applying a Lync Server Archiving policy to a user in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cdf21-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cdf21-104">

<span> </span></span></span>

<span data-ttu-id="cdf21-105">_**Тема последнего изменения:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="cdf21-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="cdf21-106">После создания политики пользователя Lync Server вы должны применить ее к определенным пользователям или группам пользователей, которые размещены на Lync Server 2013, прежде чем он сможет вступить в силу.</span><span class="sxs-lookup"><span data-stu-id="cdf21-106">After creating a Lync Server user policy, you must apply it to specific the users or user groups that are homed on Lync Server 2013 before it can take effect.</span></span> <span data-ttu-id="cdf21-107">Дополнительные сведения о создании политик пользователей для конкретных пользователей можно найти в разделе [Создание и Настройка политик пользователей для архивации в Lync Server 2013](lync-server-2013-creating-and-configuring-user-policies-for-archiving-in-lync-server.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="cdf21-107">For details about creating user policies for specific users, see [Creating and configuring user policies for Archiving in Lync Server 2013](lync-server-2013-creating-and-configuring-user-policies-for-archiving-in-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="cdf21-108">Сведения о том, как работают политики архивации, в том числе иерархия глобальных, сайтов и пользовательских политик, описаны в разделе [Использование архивации в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="cdf21-108">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cdf21-109">Для конфигурации и использования архивации необходимо сначала развернуть ее.</span><span class="sxs-lookup"><span data-stu-id="cdf21-109">In order to configure and use archiving, you must first deploy archiving.</span></span> <span data-ttu-id="cdf21-110">Подробности можно найти <A href="lync-server-2013-deploying-archiving.md">в разделе Развертывание архивации в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="cdf21-110">For details, see <A href="lync-server-2013-deploying-archiving.md">Deploying Archiving in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="cdf21-111">Если вы включили для развертывания интеграцию с Microsoft Exchange, политики хранения Exchange In-Place управляют тем, разрешено ли архивация для пользователей, использующих Exchange 2013, и почтовые ящики помещаются на In-Place удержание.</span><span class="sxs-lookup"><span data-stu-id="cdf21-111">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="cdf21-112">Подробности можно найти в разделе <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Настройка политик архивации в Lync server 2013 при использовании интеграции с Exchange Server</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="cdf21-112">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="cdf21-113">Перед включением архивации необходимо указать все соответствующие параметры в разделе конфигурации архивации.</span><span class="sxs-lookup"><span data-stu-id="cdf21-113">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="cdf21-114">Подробности можно найти <A href="lync-server-2013-configuring-archiving-options.md">в разделе Настройка параметров архивации в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="cdf21-114">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-apply-a-lync-server-archiving-policy-to-a-user"></a><span data-ttu-id="cdf21-115">Применение политики архивации сервера Lync Server для пользователя</span><span class="sxs-lookup"><span data-stu-id="cdf21-115">To apply a Lync Server archiving policy to a user</span></span>

1.  <span data-ttu-id="cdf21-116">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="cdf21-116">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="cdf21-117">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cdf21-117">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="cdf21-118">Дополнительные сведения о различных способах запуска панели управления Lync Server 2013 можно найти в разделе [Открытие средства администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="cdf21-118">For details about the different methods you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="cdf21-119">На панели навигации слева нажмите **Пользователи** и затем найдите учетную запись пользователя, которую необходимо настроить.</span><span class="sxs-lookup"><span data-stu-id="cdf21-119">In the left navigation bar, click **Users**, and then search for the user account that you want to configure.</span></span>

4.  <span data-ttu-id="cdf21-120">В таблице с результатами поиска выберите нужную учетную запись, нажмите кнопку **Изменить** и выберите пункт **Показать сведения**.</span><span class="sxs-lookup"><span data-stu-id="cdf21-120">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="cdf21-121">В диалоговом окне **изменение пользователя Lync Server** в разделе **Политика архивации** выберите политику архивации пользователей, которую вы хотите применить.</span><span class="sxs-lookup"><span data-stu-id="cdf21-121">In **Edit Lync Server user** under **Archiving policy**, select the archiving user policy that you want to apply.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cdf21-122">Для параметров <STRONG> &lt; автоматической &gt; </STRONG> настройки применяются параметры установки сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cdf21-122">The <STRONG>&lt;Automatic&gt;</STRONG> settings apply the default server installation settings.</span></span> <span data-ttu-id="cdf21-123">Данные параметры автоматически применяются сервером.</span><span class="sxs-lookup"><span data-stu-id="cdf21-123">These settings are applied automatically by the server.</span></span>

    
    </div>

6.  <span data-ttu-id="cdf21-124">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="cdf21-124">Click **Commit**.</span></span>

<span data-ttu-id="cdf21-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cdf21-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

