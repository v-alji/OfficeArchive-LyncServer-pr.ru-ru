---
title: Настройка сервера Lync Server 2013 для использования архивации Microsoft Exchange Server 2013
description: Настройка сервера Lync Server 2013 для использования архивации Microsoft Exchange Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Lync Server 2013 to use Exchange Server 2013 archiving
ms:assetid: 260346d1-edc8-4a0c-8ad2-6c2401c3c377
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ679896(v=OCS.15)
ms:contentKeyID: 49557731
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 80b0673071ec38246e366fe7556b39bd495895d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398353"
---
# <a name="configuring-microsoft-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving"></a><span data-ttu-id="71efa-103">Настройка Microsoft Lync Server 2013 для использования архивации Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="71efa-103">Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71efa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71efa-104">

<span> </span></span></span>

<span data-ttu-id="71efa-105">_**Тема последнего изменения:** 2014-06-24_</span><span class="sxs-lookup"><span data-stu-id="71efa-105">_**Topic Last Modified:** 2014-06-24_</span></span>

<span data-ttu-id="71efa-106">Microsoft Lync Server 2013 предоставляет администраторам возможность отправки мгновенных сообщений и веб-конференций, архивированных в почтовом ящике сервера Microsoft Exchange Server 2013, а не в базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-106">Microsoft Lync Server 2013 gives administrators the option of having instant messaging and Web conferencing transcripts archived to a user's Microsoft Exchange Server 2013 mailbox rather than a SQL Server database.</span></span> <span data-ttu-id="71efa-107">Если выбран этот параметр, запись расшифровок выполняется в папку "Удаленные" в почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="71efa-107">If you enable this option, transcripts are written to the Purges folder in the user's mailbox.</span></span> <span data-ttu-id="71efa-108">Папка "Удаленные" представляет собой скрытую папку, размещенную в папке корзины.</span><span class="sxs-lookup"><span data-stu-id="71efa-108">The Purges folder is a hidden folder found in the Recoverable Items folder.</span></span> <span data-ttu-id="71efa-109">Несмотря на то, что эта папка не видна для конечных пользователей, она индексируется поисковой системой Exchange и может быть обнаружена с помощью функции поиска почтового ящика Exchange и (или) Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="71efa-109">Although this folder is not visible to end-users, the folder is indexed by the Exchange search engine and can be discovered by using Exchange mailbox search and/or Microsoft SharePoint Server 2013.</span></span> <span data-ttu-id="71efa-110">Поскольку информация хранится в той же папке, которая используется в компоненте Exchange In-Place Hold (ответственный за архивирование электронной почты и другие возможности обмена данными Exchange), администраторы могут использовать один инструмент для поиска всех электронных сообщений, сохраненных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="71efa-110">Because information is stored in the same folder used by the Exchange In-Place Hold feature (responsible for archiving email and other Exchange communications), administrators can use a single tool to search for all the electronic communications archived for a user.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="71efa-111">Чтобы полностью отключить архивацию бесед Lync, необходимо также отключить журнал бесед Lync.</span><span class="sxs-lookup"><span data-stu-id="71efa-111">To completely disable archiving of Lync conversation, you must also disable Lync conversation history.</span></span> <span data-ttu-id="71efa-112">Дополнительные сведения можно найти в следующих статьях: <A href="lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md">Управление архивацией внутренних и внешних сообщений в Lync Server 2013</A>, <A href="https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy">New-CsClientPolicy</A>и <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy">Set-CsClientPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="71efa-112">For more information, see the following topics: <A href="lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md">Managing the Archiving of internal and external communications in Lync Server 2013</A>, <A href="https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy">New-CsClientPolicy</A>, and <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy">Set-CsClientPolicy</A>.</span></span>



</div>

<span data-ttu-id="71efa-113">Чтобы архивировать записи в Exchange 2013, необходимо сначала настроить проверку подлинности серверов и серверов между двумя серверами.</span><span class="sxs-lookup"><span data-stu-id="71efa-113">In order to archive transcripts to Exchange 2013 you must begin by configuring server-to-server authentication between the two servers.</span></span> <span data-ttu-id="71efa-114">После того как проверка подлинности серверов будет выполнена, вы можете выполнить следующие задачи в Microsoft Lync Server 2013 (Обратите внимание, что в зависимости от настроек и конфигурации, вам может потребоваться выполнить все эти задачи).</span><span class="sxs-lookup"><span data-stu-id="71efa-114">After server-to-server authentication is in place you can then carry out the following tasks in Microsoft Lync Server 2013 (note that, depending on your setup and configuration, you might not need to complete all of these tasks):</span></span>

1.  <span data-ttu-id="71efa-115">Включите архивацию Exchange, изменив параметры конфигурации архивации в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-115">Enable Exchange archiving by modifying your Lync Server archiving configuration settings.</span></span> <span data-ttu-id="71efa-116">Это действие обязательно для всех развертываний.</span><span class="sxs-lookup"><span data-stu-id="71efa-116">This step is required for all deployments.</span></span>

2.  <span data-ttu-id="71efa-117">Включите архивацию для внутреннего и/или внешнего обмена данными пользователей.</span><span class="sxs-lookup"><span data-stu-id="71efa-117">Enable archiving for internal and/or external communications for your users.</span></span> <span data-ttu-id="71efa-118">Это действие является обязательным для всех развертываний.</span><span class="sxs-lookup"><span data-stu-id="71efa-118">This step is required for all deployments.</span></span>

3.  <span data-ttu-id="71efa-119">Настройте свойство ExchangeArchivingPolicy для каждого из пользователей.</span><span class="sxs-lookup"><span data-stu-id="71efa-119">Configure the ExchangeArchivingPolicy property for each user.</span></span> <span data-ttu-id="71efa-120">Этот этап необходим только в Lync Server и Exchange находятся в разных лесах.</span><span class="sxs-lookup"><span data-stu-id="71efa-120">This step is only required in Lync Server and Exchange are located in different forests.</span></span>

<div>

## <a name="step-1-enabling-exchange-archiving"></a><span data-ttu-id="71efa-121">Шаг 1: включение архивации Exchange</span><span class="sxs-lookup"><span data-stu-id="71efa-121">Step 1: Enabling Exchange Archiving</span></span>

<span data-ttu-id="71efa-122">Архивация в Lync Server главным образом управляется с помощью параметров конфигурации архивации.</span><span class="sxs-lookup"><span data-stu-id="71efa-122">Archiving in Lync Server is primarily managed by using the archiving configuration settings.</span></span> <span data-ttu-id="71efa-123">При установке Lync Server 2013 вы автоматически задали один глобальный набор параметров.</span><span class="sxs-lookup"><span data-stu-id="71efa-123">When you install Lync Server 2013 you are automatically given a single, global collection of these settings.</span></span> <span data-ttu-id="71efa-124">(При необходимости администраторы могут создавать новые наборы параметров архивации в области сайта.) По умолчанию архивация не включена в глобальных параметрах, а также не включена Архивация Exchange в этих параметрах.</span><span class="sxs-lookup"><span data-stu-id="71efa-124">(Administrators can optionally create new collections of archiving settings at the site scope.) By default, archiving is not enabled in the global settings, nor is Exchange archiving enabled in these settings.</span></span> <span data-ttu-id="71efa-125">Для использования администраторов архивации Exchange необходимо настроить оба свойства EnableArchiving и EnableExchangeArchiving в этих параметрах конфигурации.</span><span class="sxs-lookup"><span data-stu-id="71efa-125">In order to use Exchange archiving administrators must configure both the EnableArchiving and the EnableExchangeArchiving properties in these configuration settings.</span></span> <span data-ttu-id="71efa-126">Свойству EnableArchiving можно присвоить одно из трех возможных значений.</span><span class="sxs-lookup"><span data-stu-id="71efa-126">The EnableArchiving property can be set to one of three possible values:</span></span>

  - <span data-ttu-id="71efa-127">**None**.</span><span class="sxs-lookup"><span data-stu-id="71efa-127">**None**.</span></span> <span data-ttu-id="71efa-128">Архивация отключена.</span><span class="sxs-lookup"><span data-stu-id="71efa-128">Archiving is disabled.</span></span> <span data-ttu-id="71efa-129">Это значение используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71efa-129">This is the default value.</span></span> <span data-ttu-id="71efa-130">Если для EnableArchiving задано значение "нет", ничего не будет архивироваться ни в одной из баз данных архивации в Lync Server, ни в Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="71efa-130">If EnableArchiving is set to None then nothing will be archived in either your Lync Server archiving database or in Exchange 2013.</span></span>

  - <span data-ttu-id="71efa-131">**ImOnly**.</span><span class="sxs-lookup"><span data-stu-id="71efa-131">**ImOnly**.</span></span> <span data-ttu-id="71efa-132">Архивируются только расшифровки мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="71efa-132">Only instant message transcripts are archived.</span></span> <span data-ttu-id="71efa-133">Если включена Архивация данных Exchange, эти записи будут архивированы в Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="71efa-133">If Exchange archiving is enabled these transcripts will be archived in Exchange 2013.</span></span> <span data-ttu-id="71efa-134">Если архивация данных Exchange отключена, эти записи будут архивированы на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-134">If Exchange archiving is disabled then these transcripts will be archived to Lync Server.</span></span>

  - <span data-ttu-id="71efa-135">**ImAndWebConf**.</span><span class="sxs-lookup"><span data-stu-id="71efa-135">**ImAndWebConf**.</span></span> <span data-ttu-id="71efa-136">Архивируются расшифровки мгновенных сообщений и веб-конференций.</span><span class="sxs-lookup"><span data-stu-id="71efa-136">Both instant message transcripts and Web conferencing transcripts are archived.</span></span> <span data-ttu-id="71efa-137">Если включена Архивация данных Exchange, эти записи будут архивированы в Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="71efa-137">If Exchange archiving is enabled these transcripts will be archived in Exchange 2013.</span></span> <span data-ttu-id="71efa-138">Если архивация данных Exchange отключена, эти записи будут архивированы на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-138">If Exchange archiving is disabled then these transcripts will be archived to Lync Server.</span></span>

<span data-ttu-id="71efa-139">Свойство EnableExchangeArchiving является логическим значением: задайте для EnableExchangeArchiving значение true ($True), чтобы включить архивацию Exchange или задать для EnableExchangeArchiving значение false ($False), чтобы отключить архивацию Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-139">The EnableExchangeArchiving property is a Boolean value: set EnableExchangeArchiving to True ($True) to enable Exchange archiving or set EnableExchangeArchiving to False ($False) to disable Exchange archiving.</span></span> <span data-ttu-id="71efa-140">Например, эта команда позволяет архивировать записи о мгновенных сообщениях, а также включает архивацию Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-140">For example, this command enables the archiving of instant messaging transcripts and also enables Exchange archiving:</span></span>

    Set-CsArchivingConfiguration -Identity "global" -EnableArchiving ImOnly -EnableExchangeArchiving $True

<span data-ttu-id="71efa-141">Чтобы отключить архивацию Exchange, используйте следующую команду, которая включает архивацию мгновенных сообщений, но отключает архивацию для Exchange (другими словами, записи будут архивированы на Lync Server):</span><span class="sxs-lookup"><span data-stu-id="71efa-141">To disable Exchange archiving, use a command similar to the following, which enables instant messaging archiving but disables archiving to Exchange (in other words, transcripts will be archived to Lync Server):</span></span>

    Set-CsArchivingConfiguration -Identity "global" -EnableArchiving ImOnly -EnableExchangeArchiving $False

<div>


> [!NOTE]  
> <span data-ttu-id="71efa-142">Если для свойства EnableArchiving задано значение "нет", Lync Server не будет архивировать мгновенные сообщения и записи для веб-конференций.</span><span class="sxs-lookup"><span data-stu-id="71efa-142">If the EnableArchiving property is set to None then Lync Server will not archive instant messaging and Web conferencing transcripts at all.</span></span> <span data-ttu-id="71efa-143">В этом случае сервер просто игнорирует значение, настроенное для EnableExchangeArchiving.</span><span class="sxs-lookup"><span data-stu-id="71efa-143">In that case, the server will simply ignore the value configured for EnableExchangeArchiving.</span></span>



</div>

<span data-ttu-id="71efa-144">Архивация Exchange также может быть включена (или отключена) с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-144">Exchange archiving can also be enabled (or disabled) by using the Lync Server Control Panel.</span></span> <span data-ttu-id="71efa-145">Для этого выполните следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="71efa-145">To do that, complete the following procedure:</span></span>

1.  <span data-ttu-id="71efa-146">На панели управления нажмите **Мониторинг и архивация**, затем выберите **Конфигурация архивации**.</span><span class="sxs-lookup"><span data-stu-id="71efa-146">In Control Panel, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

2.  <span data-ttu-id="71efa-147">На вкладке **Конфигурация архивации** дважды щелкните коллекцию настроек архивации, которую необходимо изменить (например, коллекция **Глобальные**).</span><span class="sxs-lookup"><span data-stu-id="71efa-147">On the **Archiving Configuration** tab, double-click the collection of archiving settings to be modified (for example, the **Global** collection).</span></span>

3.  <span data-ttu-id="71efa-148">В области **Редактирование настроек архивации** щелкните раскрывающийся список **Настройка архивации** и выберите **Архивировать сеансы обмена мгновенными сообщениями** (архивация только сеансов мгновенных сообщений) или **Архивировать сеансы обмена мгновенными сообщениями и веб-конференции** (архивация сеансов обмена мгновенными сообщениями и веб-конференций).</span><span class="sxs-lookup"><span data-stu-id="71efa-148">In the **Edit Archiving Setting** pane, click the **Archiving setting** dropdown list and select either **Archive IM sessions** (to archive just instant messaging sessions) or **Archive IM and web conferencing sessions** (to archive both instant messaging and Web conferencing sessions).</span></span>

4.  <span data-ttu-id="71efa-149">Выбрав элементы для архивации, установите флажок **Интеграция с Exchange Server** , чтобы включить архивацию Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-149">After choosing the items to be archived, select the **Exchange Server integration** checkbox to enable Exchange archiving.</span></span> <span data-ttu-id="71efa-150">Снимите этот флажок, чтобы отключить архивацию Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-150">To disable Exchange archiving, clear this checkbox.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="71efa-151">Флажок <STRONG>Интеграция с Exchange Server</STRONG> не отображается, если для параметра <STRONG>Настройка архивации</STRONG> установлено значение <STRONG>Отключить архивацию</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="71efa-151">The <STRONG>Exchange Server integration</STRONG> checkbox will not be available if the <STRONG>Archiving setting</STRONG> is set to <STRONG>Disable archiving</STRONG>.</span></span> <span data-ttu-id="71efa-152">Необходимо сначала включить архивацию, а затем включить архивацию Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-152">You must enable archiving first and then enable Exchange archiving.</span></span>



</div>

<span data-ttu-id="71efa-153">Если Lync Server 2013 и Exchange 2013 находятся в том же лесе, то при использовании политик хранения для отдельных пользователей (или по крайней мере для пользователей с учетными записями электронной почты на сервере Exchange 2013) Управление заархивированием осуществляется с помощью политики служб Exchange In-Place.</span><span class="sxs-lookup"><span data-stu-id="71efa-153">If Lync Server 2013 and Exchange 2013 are located in the same forest then archiving for individual users (or at least for users who have email accounts on Exchange 2013) is managed by using Exchange In-Place Hold policies.</span></span> <span data-ttu-id="71efa-154">Если у вас есть пользователи, работающие в более ранней версии Exchange, эти пользователи будут управляться с помощью политик архивации Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-154">If you have users who are homed on a previous version of Exchange then archiving for those users will be managed by using Lync Server archiving policies.</span></span> <span data-ttu-id="71efa-155">Обратите внимание, что записи в Lync для пользователей с учетными записями в Exchange 2013 могут быть архивированы в Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-155">Note that only users with accounts on Exchange 2013 can have their Lync transcripts archived to Exchange.</span></span>

<span data-ttu-id="71efa-156">Если Lync Server 2013 и Exchange 2013 находятся в разных лесах, то Управление архивацией для отдельных пользователей осуществляется с помощью настройки свойства ExchangeArchivingPolicy для каждой учетной записи отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="71efa-156">If Lync Server 2013 and Exchange 2013 are located in different forests then archiving for individual users is managed by configuring the ExchangeArchivingPolicy property for each individual user account.</span></span> <span data-ttu-id="71efa-157">Дополнительные сведения см. в описании шага 3.</span><span class="sxs-lookup"><span data-stu-id="71efa-157">See Step 3 for more information.</span></span>

</div>

<div>

## <a name="step-2-enabling-the-archiving-of-internal-andor-external-communications"></a><span data-ttu-id="71efa-158">Шаг 2. Включение архивации внутреннего и/или внешнего обмена данными</span><span class="sxs-lookup"><span data-stu-id="71efa-158">Step 2: Enabling the Archiving of Internal and/or External Communications</span></span>

<span data-ttu-id="71efa-159">После включения архивации (и архивации Exchange) необходимо изменить соответствующие политики архивации, чтобы убедиться в том, что сеансы пользователей на самом деле архивируются.</span><span class="sxs-lookup"><span data-stu-id="71efa-159">After you have enabled archiving (and Exchange archiving) you must then modify the appropriate archiving policies to ensure that user sessions are actually archived.</span></span> <span data-ttu-id="71efa-160">Обратите внимание на то, что простое включение архивации (шаг 1) не приведет к тому, что Lync Server начнет архивировать мгновенные сообщения и записи для веб-конференций.</span><span class="sxs-lookup"><span data-stu-id="71efa-160">Note that simply enabling archiving (Step 1) does not cause Lync Server to begin archiving instant messaging and Web conferencing transcripts.</span></span> <span data-ttu-id="71efa-161">Вместо этого необходимо использовать политики архивации, чтобы включить архивацию внутреннего и/или внешнего обмена данными.</span><span class="sxs-lookup"><span data-stu-id="71efa-161">Instead, you must use archiving policies to enable internal and/or external archiving.</span></span> <span data-ttu-id="71efa-162">При установке Lync Server 2013 Вы также можете установить единую глобальную политику архивации, которая включает два свойства:</span><span class="sxs-lookup"><span data-stu-id="71efa-162">When you install Lync Server 2013 you also install a single, global archiving policy that contains two properties:</span></span>

  - <span data-ttu-id="71efa-p119">**ArchiveInternal**. Если для этого свойства задано значение True ($True), выполняется архивация сеансов внутреннего обмена данными, в которых участвуют только те пользователи, у которых есть учетные записи Active Directory в текущей организации.</span><span class="sxs-lookup"><span data-stu-id="71efa-p119">**ArchiveInternal**. When set to True ($True) indicates that internal communication sessions involving only users who have Active Directory accounts in your organization) will be archived.</span></span>

  - <span data-ttu-id="71efa-p120">**ArchiveЕхternal**. Если для этого свойства задано значение True ($True), выполняется архивация сеансов внешнего обмена данными, в которых участвует хотя бы один пользователь, у которого нет учетной записи Active Directory в текущей организации.</span><span class="sxs-lookup"><span data-stu-id="71efa-p120">**ArchiveExternal**. When set to True ($True) indicates that internal communication sessions (sessions involving at least one user who does not have an Active Directory account in your organization) will be archived.</span></span>

<span data-ttu-id="71efa-167">По умолчанию для обоих свойств установлено значение False, что означает, что ни внутренний, ни внешний обмен данными не архивируется.</span><span class="sxs-lookup"><span data-stu-id="71efa-167">By default, both of these property values are set to False, meaning that neither internal nor external communication sessions are archived.</span></span> <span data-ttu-id="71efa-168">Чтобы изменить глобальную политику, вы можете использовать командную консоль управления Lync Server и командлет Set-CsArchivingPolicy.</span><span class="sxs-lookup"><span data-stu-id="71efa-168">To modify the global policy, you can use the Lync Server Management Shell and the Set-CsArchivingPolicy cmdlet.</span></span> <span data-ttu-id="71efa-169">Эта команда включает архивацию сеансов как внутреннего, так и внешнего обмена данными.</span><span class="sxs-lookup"><span data-stu-id="71efa-169">This command enables the archiving of both internal and external communication sessions:</span></span>

    Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

<span data-ttu-id="71efa-p122">Также можно использовать New-CsArchivingPolicy для создания новой политики в области сайта или в области пользователя. Например, эта команда создает новую индивидуальную политику архивации с именем RedmondArchivingPolicy:</span><span class="sxs-lookup"><span data-stu-id="71efa-p122">Alternatively, you can use the New-CsArchivingPolicy to create a new policy at either the site scope or the per-user scope. For example, this command creates a new per-user archiving policy named RedmondArchivingPolicy:</span></span>

    New-CsArchivingPolicy -Identity "RedmondArchivingPolicy" -ArchiveInternal $True -ArchiveExternal $True

<span data-ttu-id="71efa-p123">Если создана индивидуальная политика, потребуется назначить ее для соответствующих пользователей. Например:</span><span class="sxs-lookup"><span data-stu-id="71efa-p123">If you create a per-user policy you will then need to assign that policy to the appropriate users. For example:</span></span>

    Grant-CsArchivingPolicy -Identity "Ken Myer" -PolicyName  "RedmondArchivingPolicy"

<span data-ttu-id="71efa-174">Политики архивации также можно управлять с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-174">Archiving policies can also be managed by using the Lync Server Control Panel.</span></span> <span data-ttu-id="71efa-175">На панели управления нажмите **Мониторинг и архивация**, затем выберите **Политика архивации**.</span><span class="sxs-lookup"><span data-stu-id="71efa-175">Within the Control Panel, click **Monitoring and Archiving** and then click **Archiving Policy**.</span></span> <span data-ttu-id="71efa-176">Чтобы изменить существующую политику, дважды щелкните политику (например, "Глобальные"), а затем в области **Редактирование политики архивации** установите или снимите флажки **Архивировать внутренний обмен данным** и **Архивировать внешний обмен данными**.</span><span class="sxs-lookup"><span data-stu-id="71efa-176">To modify an existing policy, double-click the policy (e.g., Global) and then, in the **Edit Archiving Policy** pane, select or clear the **Archive internal communications** and the **Archive external communications** checkboxes as needed.</span></span> <span data-ttu-id="71efa-177">Чтобы создать новую политику архивации, нажмите кнопку **создать** , а затем выберите **политику сайта** или **политику пользователя**.</span><span class="sxs-lookup"><span data-stu-id="71efa-177">To create a new archiving policy, click **New** and then select either **Site policy** or **User policy**.</span></span> <span data-ttu-id="71efa-178">Если создана новая политика пользователя, необходимо перейти к соответствующим пользовательским учетным записям (вкладка **Пользователи**) и назначить для этих пользователей новую политику.</span><span class="sxs-lookup"><span data-stu-id="71efa-178">If you create a new user policy then you must access the appropriate user accounts (from the **Users** tab) and assign those users the new policy.</span></span>

</div>

<div>

## <a name="step-3-configuring-the-exchangearchivingpolicy-property"></a><span data-ttu-id="71efa-179">Шаг 3. Настройка свойства ExchangeArchivingPolicy</span><span class="sxs-lookup"><span data-stu-id="71efa-179">Step 3: Configuring the ExchangeArchivingPolicy Property</span></span>

<span data-ttu-id="71efa-180">Если Lync Server 2013 и Exchange 2013 находятся в разных лесах, вам недостаточно просто включить архивацию Exchange в параметрах конфигурации архивации. Это не приведет к тому, что обмен мгновенными сообщениями и веб-конференции архивируются в Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-180">If Lync Server 2013 and Exchange 2013 are located in different forests then it is not enough to simply enable Exchange archiving in the archiving configuration settings; that will not result in instant messaging and Web conferencing transcripts being archived in Exchange.</span></span> <span data-ttu-id="71efa-181">Вместо этого необходимо также настроить свойство ExchangeArchivingPolicy для каждой из соответствующих учетных записей пользователей в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-181">Instead, you must also configure the ExchangeArchivingPolicy property on each of the relevant Lync Server user accounts.</span></span> <span data-ttu-id="71efa-182">Этому свойству можно присвоить одно из четырех возможных значений.</span><span class="sxs-lookup"><span data-stu-id="71efa-182">This property can be set to one of four possible values:</span></span>

1.  <span data-ttu-id="71efa-183">Uninitialized.</span><span class="sxs-lookup"><span data-stu-id="71efa-183">Uninitialized.</span></span> <span data-ttu-id="71efa-184">Указывает на то, что архивирование будет основано на параметрах хранения In-Place, настроенных для почтового ящика Exchange пользователя; Если на почтовом ящике пользователя не включен In-Place удержание, пользователь получит сообщение и его сообщения, а также веб-конференции, заархивированные в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-184">Indicates that archiving will be based on the In-Place Hold settings configured for the user's Exchange mailbox; if In-Place Hold has not been enabled on the user's mailbox then the user will have his or her messaging and Web conferencing transcripts archived in Lync Server.</span></span>

2.  <span data-ttu-id="71efa-185">**UseLyncArchivingPolicy**.</span><span class="sxs-lookup"><span data-stu-id="71efa-185">**UseLyncArchivingPolicy**.</span></span> <span data-ttu-id="71efa-186">Указывает на то, что при обмене мгновенными сообщениями и веб-конференций они должны быть архивированы в Lync Server, а не в Exchange.</span><span class="sxs-lookup"><span data-stu-id="71efa-186">Indicates that the user's instant messaging and Web conferencing transcripts should be archived in Lync Server rather than in Exchange.</span></span>

3.  <span data-ttu-id="71efa-187">**NoArchiving**.</span><span class="sxs-lookup"><span data-stu-id="71efa-187">**NoArchiving**.</span></span> <span data-ttu-id="71efa-188">Указывает, что архивация расшифровок обмена мгновенными сообщениями и веб-конференций для пользователя не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71efa-188">Indicates that the user's instant messaging and Web conferencing transcripts should not be archived at all.</span></span> <span data-ttu-id="71efa-189">Обратите внимание, что этот параметр переопределяет политики архивации сервера Lync Server, назначенные пользователю.</span><span class="sxs-lookup"><span data-stu-id="71efa-189">Note that this setting overrides any Lync Server archiving policies assigned to the user.</span></span>

4.  <span data-ttu-id="71efa-190">**ArchivingToExchange**.</span><span class="sxs-lookup"><span data-stu-id="71efa-190">**ArchivingToExchange**.</span></span> <span data-ttu-id="71efa-191">Указывает на то, что при обмене мгновенными сообщениями и веб-конференций они должны быть архивированы в Exchange независимо от того, какие параметры In-Place не были назначены почтовому ящику пользователя.</span><span class="sxs-lookup"><span data-stu-id="71efa-191">Indicates that the user's instant messaging and Web conferencing transcripts should be archived to Exchange regardless of the In-Place Hold settings that have (or have not) been assigned to the user's mailbox.</span></span>

<span data-ttu-id="71efa-192">Например, чтобы настроить учетную запись пользователя таким образом, чтобы средства обмена мгновенными сообщениями и веб-конференций всегда архивировались в Exchange, вы можете использовать команды, аналогичные этим в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="71efa-192">For example, to configure a user account so that instant messaging and Web conferencing transcripts are always archived to Exchange you can use a command similar to this from the Lync Server Management Shell:</span></span>

    Set-CsUser -Identity "Ken Myer" -ExchangeArchivingPolicy ArchivingToExchange

<span data-ttu-id="71efa-193">Чтобы настроить ту же политику архивации для группы пользователей (например, для всех пользователей, размещенных в указанном пуле регистратора), можно использовать команду следующего вида:</span><span class="sxs-lookup"><span data-stu-id="71efa-193">If you want to set the same archiving policy for a group of users (for example, all the users homed on a specified Registrar pool) you can use a command similar to this:</span></span>

    Get-CsUser -Filter {RegistrarPool -eq "atl-cs-001.litwareinc.com"} | Set-CsUser -ExchangeArchivingPolicy ArchivingToExchange

<span data-ttu-id="71efa-194">Обратите внимание, что для настройки значения свойства ExchangeArchivingPolicy необходимо использовать командную консоль Lync Server Management Shell (и Windows PowerShell).</span><span class="sxs-lookup"><span data-stu-id="71efa-194">Note that you must use the Lync Server Management Shell (and Windows PowerShell) in order to configure value of the ExchangeArchivingPolicy property.</span></span> <span data-ttu-id="71efa-195">Это свойство не отображается для администраторов на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71efa-195">This property is not exposed to administrators in the Lync Server Control Panel.</span></span>

<span data-ttu-id="71efa-196">Чтобы просмотреть список всех пользователей, для которых назначена конкретная политика архивации, можно использовать команду следующего вида. Эта команда возвращает отображаемые имена Active Directory всех пользователей, для которых свойству ExchangeArchivingPolicy присвоено значение Uninitialized:</span><span class="sxs-lookup"><span data-stu-id="71efa-196">If you would like to view a list of all the users who have been assigned a specific archiving policy then you can use a command similar to the following, which returns the Active Directory display name of all the users who have had the ExchangeArchivingPolicy property set to Uninitialized:</span></span>

    Get-CsUser | Where-Object {$_.ExchangeArchivingPolicy -eq "Uninitialized"} | Select-Object DisplayName

<span data-ttu-id="71efa-197">Эта команда также возвращает отображаемые имена пользователей, для которых свойству ExchangeArchivingPolicy не назначено значение UseLyncArchivingPolicy:</span><span class="sxs-lookup"><span data-stu-id="71efa-197">Likewise, this command returns the display name of the users who have not have the ExchangeArchivingPolicy property set to UseLyncArchivingPolicy:</span></span>

    Get-CsUser | Where-Object {$_.ExchangeArchivingPolicy -ne "UseLyncArchivingPolicy"} | Select-Object DisplayName

<span data-ttu-id="71efa-198"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71efa-198"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

