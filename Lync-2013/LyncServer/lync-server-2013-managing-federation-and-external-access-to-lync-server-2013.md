---
title: 'Lync Server 2013: Управление федерацией и внешним доступом к Lync Server 2013'
description: 'Lync Server 2013: Управление интеграцией и внешним доступом к Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing federation and external access to Lync Server 2013
ms:assetid: 26f806c1-f284-4637-b06b-06270336c540
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520966(v=OCS.15)
ms:contentKeyID: 48183665
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1d389c7490fd1884631ed2fc184d590eb42141b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437457"
---
# <a name="managing-federation-and-external-access-to-lync-server-2013"></a><span data-ttu-id="f13b7-103">Управление федерацией и внешним доступом к Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13b7-103">Managing federation and external access to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f13b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f13b7-104">

<span> </span></span></span>

<span data-ttu-id="f13b7-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="f13b7-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="f13b7-106">Развертывание пограничного сервера или пограничного пула является первым этапом поддержки внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="f13b7-106">Deploying an Edge Server or Edge pool is the first step to supporting external users.</span></span> <span data-ttu-id="f13b7-107">Подробнее о том, как развертывать пограничные серверы, можно узнать в разделе [развертывание внешних пользователей Access в Lync Server 2013](lync-server-2013-deploying-external-user-access.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="f13b7-107">For details about deploying Edge Servers, see [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<span data-ttu-id="f13b7-108">После установки и настройки внутреннего развертывания Lync Server 2013 внутренние пользователи в организации могут совместно работать с другими внутренними пользователями, у которых есть учетные записи SIP в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f13b7-108">After installing and configuring your internal deployment of Lync Server 2013, internal users in your organization can collaborate with other internal users who have SIP accounts in your Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="f13b7-109">Совместная работа может включать в себя отправка и получение мгновенных сообщений, а также обновление состояния присутствия и участие в конференциях (например, собраниях).</span><span class="sxs-lookup"><span data-stu-id="f13b7-109">Collaboration can include sending and receiving instant messages, and update of presence status and participating in conferences (also known as "meetings").</span></span> <span data-ttu-id="f13b7-110">Вы включаете и настраиваете доступ внешних пользователей, чтобы управлять тем, может ли пользователь поддерживать совместную работу с внутренними пользователями Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f13b7-110">You enable and configure external user access to control whether supported external users can collaborate with internal Lync Server users.</span></span> <span data-ttu-id="f13b7-111">Внешние пользователи могут включать удаленных пользователей вашего развертывания, федеративных пользователей (включая поддерживаемых пользователей общедоступных служб обмена мгновенными сообщениями), Федерации XMPP и анонимных участников в конференциях.</span><span class="sxs-lookup"><span data-stu-id="f13b7-111">External users can include remote users of your deployment, federated users (including supported users of public instant messaging (IM) service providers), XMPP federation and anonymous participants in conferences.</span></span>

<span data-ttu-id="f13b7-112">Если развертывание включало установку пограничного сервера Lync Server 2013 или пограничного пула, область возможных типов связи значительно расширяется с учетом ряда возможностей для доступа внешних пользователей, взаимодействия с членами других федеративных доменов SIP, служб федерации SIP и XMPP федеративных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f13b7-112">If your deployment included the installation of a Lync Server 2013 Edge Server or an Edge pool, the scope of possible communication types is greatly expanded with a number of options for external user access, communication with members of other SIP federated domains, SIP federated providers, and XMPP federated users.</span></span> <span data-ttu-id="f13b7-113">После настройки пограничного сервера или пула Edge вы включите типы доступа внешних пользователей, которые вы хотите предоставить, и настройте политики для управления внешним доступом.</span><span class="sxs-lookup"><span data-stu-id="f13b7-113">After setting up the Edge Server or Edge pool, you enable the types of external user access that you want to provide, and configure the policies to control for the external access.</span></span> <span data-ttu-id="f13b7-114">В Lync Server 2013 вы включаете и настраиваете доступ к внешним пользователям и политикам с помощью панели управления Lync Server, командной консоли Lync Server Management Shell или обоих, в зависимости от требований к задачам.</span><span class="sxs-lookup"><span data-stu-id="f13b7-114">In Lync Server 2013, you enable and configure external user access and policies using the Lync Server Control Panel, the Lync Server Management Shell or both, based on the task requirements.</span></span> <span data-ttu-id="f13b7-115">Подробные сведения об этих средствах управления можно найти в разделе Администрирование на [Lync server 2013](lync-server-2013-lync-server-administrative-tools.md) в документации по операциям, [командной консоли Lync Server 2013](lync-server-2013-lync-server-management-shell.md) в документации по эксплуатации и [установке средств администрирования Lync Server 2013](lync-server-2013-install-lync-server-administrative-tools.md) в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="f13b7-115">For details about these management tools, see [Lync Server 2013 administrative tools](lync-server-2013-lync-server-administrative-tools.md) in the Operations documentation, [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) in the Operations documentation, and [Install Lync Server 2013 administrative tools](lync-server-2013-install-lync-server-administrative-tools.md) in the Operations documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f13b7-116">При проектировании конфигурации и политик для внешнего доступа пользователей необходимо знать приоритет политик и способ применения политик.</span><span class="sxs-lookup"><span data-stu-id="f13b7-116">When you design your configuration and policies for external user access, you must understand the precedence of policies and how the policies are applied.</span></span> <span data-ttu-id="f13b7-117">Параметры политики сервера Lync Server, примененные на одном уровне политики, могут переопределять параметры, примененные на другом уровне политики.</span><span class="sxs-lookup"><span data-stu-id="f13b7-117">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="f13b7-118">Приоритет политики Lync Server: политика пользователей (наибольшее влияние) переопределяет политику сайта, а затем политика сайта переопределяет глобальную политику (наименее влияние).</span><span class="sxs-lookup"><span data-stu-id="f13b7-118">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="f13b7-119">То есть, чем ближе параметр политики к объекту, на который она влияет, тем больше влияния она оказывает на объект.</span><span class="sxs-lookup"><span data-stu-id="f13b7-119">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>



</div>

<span data-ttu-id="f13b7-120">По умолчанию ни одна политика не настроена для поддержки внешних пользователей, включая удаленный доступ пользователей, доступ федеративных пользователей, даже если вы уже включили поддержку внешних пользователей для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f13b7-120">By default, no policies are configured to support external user access, including remote user access, federated user access, even if you have already enabled external user access support for your organization.</span></span> <span data-ttu-id="f13b7-121">Чтобы управлять использованием внешнего доступа пользователей, необходимо настроить одну или несколько политик, указав тип доступа внешних пользователей, которые поддерживаются для каждой политики.</span><span class="sxs-lookup"><span data-stu-id="f13b7-121">To control the use of external user access, you must configure one or more policies, specifying the type of external user access supported for each policy.</span></span> <span data-ttu-id="f13b7-122">К ним относятся следующие политики внешнего доступа:</span><span class="sxs-lookup"><span data-stu-id="f13b7-122">This includes the following external access policies:</span></span>

  - <span data-ttu-id="f13b7-123">**Глобальная политика**   Глобальная политика создается при развертывании пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="f13b7-123">**Global policy**   The global policy is created when you deploy your Edge Servers.</span></span> <span data-ttu-id="f13b7-124">По умолчанию в глобальной политике не включены параметры доступа внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="f13b7-124">By default, no external user access options are enabled in the global policy.</span></span> <span data-ttu-id="f13b7-125">Для поддержки внешнего доступа пользователей на глобальном уровне вы можете настроить глобальную политику для поддержки одного или нескольких типов внешних параметров доступа пользователей.</span><span class="sxs-lookup"><span data-stu-id="f13b7-125">To support external user access at the global level, you configure the global policy to support one or more types of external user access options.</span></span> <span data-ttu-id="f13b7-126">Глобальная политика применяется ко всем пользователям в Организации, но политики сайтов и политики пользователей переопределяют глобальную политику.</span><span class="sxs-lookup"><span data-stu-id="f13b7-126">The global policy applies to all users in your organization, but site policies and user policies override the global policy.</span></span> <span data-ttu-id="f13b7-127">Если вы удалите глобальную политику, она не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="f13b7-127">If you delete the global policy, you do not remove it.</span></span> <span data-ttu-id="f13b7-128">Вместо этого вы восстанавливаете значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f13b7-128">Instead, you reset it to the default setting.</span></span>

  - <span data-ttu-id="f13b7-129">**Политика сайта**   Вы можете создать и настроить одну или несколько политик сайта для ограничения поддержки внешних пользователей для доступа к определенным сайтам.</span><span class="sxs-lookup"><span data-stu-id="f13b7-129">**Site policy**   You can create and configure one or more site policies to limit support for external user access to specific sites.</span></span> <span data-ttu-id="f13b7-130">Конфигурация в политике сайта переопределяет глобальную политику, но только для сайта, к которому применяется эта политика.</span><span class="sxs-lookup"><span data-stu-id="f13b7-130">The configuration in the site policy overrides the global policy, but only for the specific site covered by the site policy.</span></span> <span data-ttu-id="f13b7-131">Например, если вы разрешите удаленному пользователю доступ в глобальной политике, вы можете указать политику сайта, запрещающую доступ удаленных пользователей для определенного сайта.</span><span class="sxs-lookup"><span data-stu-id="f13b7-131">For example, if you enable remote user access in the global policy, you might specify a site policy that disables remote user access for a specific site.</span></span> <span data-ttu-id="f13b7-132">По умолчанию политика сайта применяется ко всем пользователям этого сайта, но вы можете назначить пользователю политику, чтобы перекрыть параметр политики сайта.</span><span class="sxs-lookup"><span data-stu-id="f13b7-132">By default, a site policy is applied to all users of that site, but you can assign a user policy to a user to override the site policy setting.</span></span>

  - <span data-ttu-id="f13b7-133">**Политика пользователя**   Вы можете создать и настроить одну или несколько политик пользователей для ограничения поддержки доступа удаленных пользователей к определенным пользователям.</span><span class="sxs-lookup"><span data-stu-id="f13b7-133">**User policy**   You can create and configure one or more user policies to limit support for remote user access to specific users.</span></span> <span data-ttu-id="f13b7-134">Конфигурация политики пользователя переопределяет глобальную политику и ее сайта, но только для определенных пользователей, которым назначена политика пользователя.</span><span class="sxs-lookup"><span data-stu-id="f13b7-134">The configuration in the user policy overrides the global and site policy, but only for the specific users to whom the user policy is assigned.</span></span> <span data-ttu-id="f13b7-135">Например, если вы разрешите удаленному пользователю доступ в глобальной политике и в политике сайта, вы можете указать политику пользователей, запрещающую доступ к удаленному пользователю, а затем назначить эту политику пользователей конкретным пользователям.</span><span class="sxs-lookup"><span data-stu-id="f13b7-135">For example, if you enable remote user access in the global policy and site policy, you might specify a user policy that disables remote user access and then assign that user policy to specific users.</span></span> <span data-ttu-id="f13b7-136">Если вы создаете политику пользователя, необходимо применить ее для одного или нескольких пользователей, прежде чем она вступит в силу.</span><span class="sxs-lookup"><span data-stu-id="f13b7-136">If you create a user policy, you must apply it to one or more users before it takes effect.</span></span>

<span data-ttu-id="f13b7-137">Чтобы определить, какие параметры конфигурации и какие политики требуется создать или изменить, ознакомьтесь со следующими положениями:</span><span class="sxs-lookup"><span data-stu-id="f13b7-137">To determine which configuration settings and which policies you need to create or edit, refer to the following decision points:</span></span>

<span data-ttu-id="f13b7-138">**Вы хотите разрешить внутренним и внешним пользователям домена возможность совместной работы с помощью мгновенных сообщений, веб-конференций, аудио-и видеосвязи?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-138">**Do you want to allow internal and external users of your domain to be able to collaborate using instant messaging, Web conferencing, and Audio/Video?**</span></span>

<span data-ttu-id="f13b7-139">Настройте параметры так, как описано в разделах [Настройка политик для доступа к удаленным пользователям в Lync server 2013](lync-server-2013-configure-policies-to-control-remote-user-access.md), [Включение и отключение службы федерации и общедоступного обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)</span><span class="sxs-lookup"><span data-stu-id="f13b7-139">Configure the settings as detailed in the topics [Configure policies to control remote user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-remote-user-access.md), and [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)</span></span>

<span data-ttu-id="f13b7-140">**Разрешить анонимным пользователям посещать и принимать приглашения на Конференции, размещенные пользователями в развертывании?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-140">**Do you want to allow anonymous users to attend and be invited to conferences hosted by users in your deployment?**</span></span>

<span data-ttu-id="f13b7-141">Настройте параметры так, как описано в разделе [назначение политик конференц-связи для анонимных пользователей в Lync server 2013](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md), [Создание или изменение политики конференций](lync-server-2013-create-or-modify-a-conferencing-policy.md) на странице Lync Server 2013 и [Параметры политики конференций для Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md)</span><span class="sxs-lookup"><span data-stu-id="f13b7-141">Configure the settings as detailed in the topic [Assign conferencing policies to support anonymous users in Lync Server 2013](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md), [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md) and [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md)</span></span>

<span data-ttu-id="f13b7-142">**Вы хотите разрешить пользователям общаться с контактами из федеративного домена SIP?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-142">**Do you want to allow users to communicate with SIP Federated Domain contacts?**</span></span>

<span data-ttu-id="f13b7-143">Настройте параметры так, как описано в разделах [Настройка политик для управления доступом пользователей Федерации в Lync server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md), [Включение и отключение подключения к службам федеративных и общедоступных мгновенных сообщений в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md), а также [Управление федеративными доменами SIP для Организации в Lync Server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)</span><span class="sxs-lookup"><span data-stu-id="f13b7-143">Configure the settings as detailed in the topics [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md), [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md), and [Manage SIP federated domains for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)</span></span>

<span data-ttu-id="f13b7-144">**Если вы включили связь с доменами Федерации SIP, хотите включить связь с контактами для XMPP федеративного партнера?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-144">**If you have enabled communication with SIP Federation Domains, do you want to enable communications with XMPP Federated Partner contacts?**</span></span>

<span data-ttu-id="f13b7-145">Настройте параметры так, как описано в разделе [Настройка политик для управления XMPPом федеративного доступа пользователей в Lync server 2013](lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md) и [Управление XMPP федеративными партнерами в Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="f13b7-145">Configure the settings as detailed in the topic [Configure policies to control XMPP federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md) and [Manage XMPP federated partners in Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md).</span></span>

<span data-ttu-id="f13b7-146">**Если вы включили связь с федеративными доменами SIP, хотите включить автоматическое обнаружение модулей SIP?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-146">**If you have enabled communication with SIP Federated Domains, do you want to enable SIP Federation automatic discovery?**</span></span>

<span data-ttu-id="f13b7-147">Настройте параметры, как описано в разделе [Включение и отключение обнаружения партнеров Федерации в Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md).</span><span class="sxs-lookup"><span data-stu-id="f13b7-147">Configure the settings as detailed in the topic [Enable or disable discovery of federation partners in Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md).</span></span>

<span data-ttu-id="f13b7-148">**Если вы включили связь с доменами Федерации SIP, хотите разрешить отправлять заявление об отказе в Федеративные контакты с уведомлением о том, что вы используете архивацию и можете ли они архивироваться?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-148">**If you have enabled communication with SIP Federation Domains, do you want to enable sending a disclaimer to Federated contacts notifying them that you use archiving and that communications may be archived?**</span></span>

<span data-ttu-id="f13b7-149">Настройте параметры, как описано в разделе [Включение и отключение отправки сообщений об отказе в архивы федеративным партнерам в Lync Server 2013](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md).</span><span class="sxs-lookup"><span data-stu-id="f13b7-149">Configure the settings as detailed in the topic [Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md).</span></span>

<span data-ttu-id="f13b7-150">**Вы хотите разрешить пользователям взаимодействовать с поставщиками услуг SIP, которые обеспечивают связь с общедоступными поставщиками, такими как Windows Live Messenger, AOL и Yahoo \! ?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-150">**Do you want to allow users to communicate with SIP Federated Providers that enable communication with public providers, such as Windows Live Messenger, AOL, and Yahoo\!?**</span></span>

<span data-ttu-id="f13b7-151">Настройте параметры так, как описано в разделах [Настройка политик для управления доступом пользователей в Lync server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md)[Включение и отключение службы федерации и общедоступного обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md), а [также создание и изменение общедоступных федеративных служб SIP в Lync Server 2013](lync-server-2013-create-or-edit-public-sip-federated-providers.md).</span><span class="sxs-lookup"><span data-stu-id="f13b7-151">Configure the settings as detailed in the topics [Configure policies to control public user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md)[Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md), and [Create or edit public SIP federated providers in Lync Server 2013](lync-server-2013-create-or-edit-public-sip-federated-providers.md).</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="f13b7-152">По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="f13b7-152">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="f13b7-153">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f13b7-153">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="f13b7-154">Messenger, пока служба не отключается.</span><span class="sxs-lookup"><span data-stu-id="f13b7-154">Messenger until the service shut down date.</span></span> <span data-ttu-id="f13b7-155">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="f13b7-155">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="f13b7-156">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="f13b7-156">has been announced.</span></span> <span data-ttu-id="f13b7-157">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f13b7-157">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="f13b7-158">USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="f13b7-158">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="f13b7-159">Messenger.</span><span class="sxs-lookup"><span data-stu-id="f13b7-159">Messenger.</span></span> <span data-ttu-id="f13b7-160">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</span><span class="sxs-lookup"><span data-stu-id="f13b7-160">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="f13b7-161">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="f13b7-161">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="f13b7-162">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="f13b7-162">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="f13b7-163">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="f13b7-163">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="f13b7-164">**Вы хотите разрешить пользователям взаимодействовать с поставщиками услуг SIP, которые являются службами, использующими Microsoft 365, Microsoft Lync Online и Microsoft Lync Online 2010?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-164">**Do you want to allow users to communicate with SIP Federated Providers that are hosted providers running Microsoft 365, Microsoft Lync Online, and Microsoft Lync Online 2010?**</span></span>

<span data-ttu-id="f13b7-165">Настройте параметры, как описано в разделах [Создание и изменение общедоступных федеративных поставщиков SIP в Lync server 2013](lync-server-2013-create-or-edit-public-sip-federated-providers.md), [Включение и отключение службы федерации и общедоступного обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) , [Создание и редактирование размещенных федеративных поставщиков услуг SIP Lync Server 2013](lync-server-2013-create-or-edit-hosted-sip-federated-providers.md)</span><span class="sxs-lookup"><span data-stu-id="f13b7-165">Configure the settings as detailed in the topics [Create or edit public SIP federated providers in Lync Server 2013](lync-server-2013-create-or-edit-public-sip-federated-providers.md), [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) and [Create or edit hosted SIP federated providers Lync Server 2013](lync-server-2013-create-or-edit-hosted-sip-federated-providers.md)</span></span>

<span data-ttu-id="f13b7-166">**Задано ли развертывание в разделе с разделением (гибридным) доменом, в котором у некоторых пользователей есть домашний сервер в рамках локального развертывания, а другие пользователи настроены на работу с домашним сервером в Интернет-среде?**</span><span class="sxs-lookup"><span data-stu-id="f13b7-166">**Is your deployment configured in a split (also known as a hybrid) domain, where some users have their home server in an on-premise deployment, and other users are configured with a home server in an online environment?**</span></span>

<span data-ttu-id="f13b7-167">Настройте параметры так, как описано в разделах [Настройка политик для управления доступом пользователей Федерации в Lync server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md), включение и отключение подключения к службам федеративных [и общедоступных мгновенных сообщений в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) , а также [Создание или изменение размещенных федеративных поставщиков SIP для Lync Server 2013](lync-server-2013-create-or-edit-hosted-sip-federated-providers.md)</span><span class="sxs-lookup"><span data-stu-id="f13b7-167">Configure the settings as detailed in the topics [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md), [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) and [Create or edit hosted SIP federated providers Lync Server 2013](lync-server-2013-create-or-edit-hosted-sip-federated-providers.md)</span></span>

<span data-ttu-id="f13b7-168">Если вы предпочитаете таблицу, в которой перечислены требования:</span><span class="sxs-lookup"><span data-stu-id="f13b7-168">If you prefer a table that lists the requirements:</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f13b7-169">Вкладка в Федерации и внешнем доступе (на уровне) (вниз)</span><span class="sxs-lookup"><span data-stu-id="f13b7-169">Tab in Federation and External Access (Across) Federation or External Access Type (Down)</span></span></th>
<th><span data-ttu-id="f13b7-170">Политика внешнего доступа</span><span class="sxs-lookup"><span data-stu-id="f13b7-170">External Access Policy</span></span></th>
<th><span data-ttu-id="f13b7-171">Настройка Edge Access</span><span class="sxs-lookup"><span data-stu-id="f13b7-171">Access Edge Config</span></span></th>
<th><span data-ttu-id="f13b7-172">Федеративные домены SIP</span><span class="sxs-lookup"><span data-stu-id="f13b7-172">SIP Federated Domains</span></span></th>
<th><span data-ttu-id="f13b7-173">Федеративные поставщики SIP</span><span class="sxs-lookup"><span data-stu-id="f13b7-173">SIP Federated Providers</span></span></th>
<th><span data-ttu-id="f13b7-174">Федеративный партнер XMPP</span><span class="sxs-lookup"><span data-stu-id="f13b7-174">XMPP Federated Partner</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f13b7-175">Удаленные пользователи</span><span class="sxs-lookup"><span data-stu-id="f13b7-175">Remote Users</span></span></p></td>
<td><p><span data-ttu-id="f13b7-176"><a href="lync-server-2013-configure-policies-to-control-remote-user-access.md">Настройка политик для управления удаленным доступом пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-176"><a href="lync-server-2013-configure-policies-to-control-remote-user-access.md">Configure policies to control remote user access in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f13b7-177"><a href="lync-server-2013-enable-or-disable-remote-user-access.md">Включение или отключения удаленного доступа пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-177"><a href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</a></span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f13b7-178">Федеративные контакты SIP</span><span class="sxs-lookup"><span data-stu-id="f13b7-178">SIP Federated Contacts</span></span></p></td>
<td><p><span data-ttu-id="f13b7-179"><a href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Настройка политик управления доступом федеративных пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-179"><a href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f13b7-180"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-180"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="f13b7-181"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Включение или отключение обнаружения федеративных партнеров в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-181"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="f13b7-182"><a href="lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md">Включение и отключение отправки отказа от архивирования федеративным партнерам в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-182"><a href="lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f13b7-183"><a href="lync-server-2013-manage-sip-federated-domains-for-your-organization.md">Управление федеративными доменами SIP для организации в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-183"><a href="lync-server-2013-manage-sip-federated-domains-for-your-organization.md">Manage SIP federated domains for your organization in Lync Server 2013</a></span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f13b7-184">XMPP Федеративные контакты</span><span class="sxs-lookup"><span data-stu-id="f13b7-184">XMPP Federated Contacts</span></span></p></td>
<td><p><span data-ttu-id="f13b7-185"><a href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Настройка политик управления доступом федеративных пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-185"><a href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="f13b7-186"><a href="lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md">Настройка политик управления доступом федеративных XMPP-пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-186"><a href="lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md">Configure policies to control XMPP federated user access in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f13b7-187"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-187"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="f13b7-188"><a href="lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md">Управление федеративными XMPP-партнерами в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-188"><a href="lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md">Manage XMPP federated partners in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f13b7-189">Разделение доменов домена и гибридных пользователей</span><span class="sxs-lookup"><span data-stu-id="f13b7-189">Split Domain / Hybrid Users</span></span></p></td>
<td><p><span data-ttu-id="f13b7-190"><a href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Настройка политик управления доступом федеративных пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-190"><a href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f13b7-191"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-191"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f13b7-192"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Создание или изменение размещенных федеративных поставщиков SIP в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-192"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f13b7-193">Контакты общедоступной службы обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="f13b7-193">Public IM Service Contacts</span></span></p></td>
<td><p><span data-ttu-id="f13b7-194"><a href="lync-server-2013-configure-policies-to-control-public-user-access.md">Конфигурация политик для управления общим доступом пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-194"><a href="lync-server-2013-configure-policies-to-control-public-user-access.md">Configure policies to control public user access in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f13b7-195"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-195"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f13b7-196"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Создание или изменение общедоступных федеративных поставщиков SIP в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-196"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f13b7-197">Анонимный доступ пользователей к собраниям и конференциям</span><span class="sxs-lookup"><span data-stu-id="f13b7-197">Anonymous user access to meetings and conferences</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f13b7-198"><a href="lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md">Назначение политик конференции для поддержки анонимных пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f13b7-198"><a href="lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md">Assign conferencing policies to support anonymous users in Lync Server 2013</a></span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="f13b7-199">Кроме того, вы должны принять следующие параметры конфигурации в разделе политики конференц-связи: <A href="lync-server-2013-create-or-modify-a-conferencing-policy.md">Создание и изменение политики конференц-связи в Lync server 2013</A> и <A href="lync-server-2013-conferencing-policy-settings-reference.md">Параметры политики конференций на Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="f13b7-199">You must also consider the following configuration settings under Conferencing policies: <A href="lync-server-2013-create-or-modify-a-conferencing-policy.md">Create or modify a conferencing policy in Lync Server 2013</A> and <A href="lync-server-2013-conferencing-policy-settings-reference.md">Conferencing policy settings reference for Lync Server 2013</A></span></span>


</div></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f13b7-200">Вы можете настроить параметры доступа внешних пользователей, включая политики, которые вы хотите использовать для управления доступом внешних пользователей, даже если вы не включили доступ внешних пользователей для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f13b7-200">You can configure external user access settings, including any policies that you want to use to control external user access, even if you have not enabled external user access for your organization.</span></span> <span data-ttu-id="f13b7-201">Тем не менее политики и другие параметры настройки действуют только в том случае, если к вашей организации разрешен доступ внешним пользователям.</span><span class="sxs-lookup"><span data-stu-id="f13b7-201">However, the policies and other settings that you configure are in effect only when you have external user access enabled for your organization.</span></span> <span data-ttu-id="f13b7-202">Внешние пользователи не могут взаимодействовать с пользователями вашей организации, если доступ к внешним пользователям отключен или политики доступа к внешним пользователям не настроены для ее поддержки.</span><span class="sxs-lookup"><span data-stu-id="f13b7-202">External users cannot communicate with users of your organization when external user access is disabled or if no external user access policies are configured to support it.</span></span>

<span data-ttu-id="f13b7-203">В развертывании пограничного сервера проверяются типы внешних пользователей (за исключением анонимных пользователей, которые проверяются с помощью идентификатора Конференции и ключа доступа, который отправляется анонимному участнику, когда вы создаете конференц-связь и приглашаете участников) и управляете доступом в зависимости от настройки поддержки Edge.</span><span class="sxs-lookup"><span data-stu-id="f13b7-203">Your edge deployment authenticates the types of external users (except for anonymous users, who are authenticated by the conference ID and a passkey that is sent to the anonymous participant when you create the conference and invite participants) and controls access based on how you configure your edge support.</span></span> <span data-ttu-id="f13b7-204">Чтобы управлять связью, вы можете настроить одну или несколько политик и настроить параметры, определяющие взаимодействие пользователей внутри и за пределами развертывания друг с другом.</span><span class="sxs-lookup"><span data-stu-id="f13b7-204">In order to control communications, you can configure one or more policies and configure settings that define how users inside and outside your deployment communicate with each other.</span></span> <span data-ttu-id="f13b7-205">Политики и параметры включают глобальную политику по умолчанию для внешних пользователей, а также политики сайтов и пользователей, которые можно создавать и настраивать для разрешения доступа к одному или нескольким типам внешних пользователей для определенных сайтов или пользователей.</span><span class="sxs-lookup"><span data-stu-id="f13b7-205">The policies and settings include the default global policy for external user access, in addition to site and user policies that you can create and configure to enable one or more types of external user access for specific sites or users.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f13b7-206">Содержание</span><span class="sxs-lookup"><span data-stu-id="f13b7-206">In This Section</span></span>

  - [<span data-ttu-id="f13b7-207">Управление политикой внешнего доступа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13b7-207">Manage external access policy in Lync Server 2013</span></span>](lync-server-2013-manage-external-access-policy-for-your-organization.md)

  - [<span data-ttu-id="f13b7-208">Управление конфигурацией пограничного сервера в организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13b7-208">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-access-edge-configuration-for-your-organization.md)

  - [<span data-ttu-id="f13b7-209">Управление федеративными доменами SIP для организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13b7-209">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)

  - [<span data-ttu-id="f13b7-210">Управление федеративными поставщиками SIP в организации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13b7-210">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)

  - [<span data-ttu-id="f13b7-211">Управление федеративными XMPP-партнерами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13b7-211">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)

  - [<span data-ttu-id="f13b7-212">Настройка поддержки федерации для клиента Lync Online в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13b7-212">Configuring federation support for a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-configuring-federation-support-for-a-lync-online-customer.md)

<span data-ttu-id="f13b7-213"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f13b7-213"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

