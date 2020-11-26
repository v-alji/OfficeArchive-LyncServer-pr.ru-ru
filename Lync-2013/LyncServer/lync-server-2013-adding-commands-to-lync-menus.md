---
title: 'Lync Server 2013: Добавление команд в меню Lync'
description: 'Lync Server 2013: Добавление команд в меню Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding commands to Lync menus
ms:assetid: a8443bc2-e234-4022-870a-00700f38b1ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412788(v=OCS.15)
ms:contentKeyID: 48185091
ms.date: 04/11/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed4d62d085eaf115d107244ae50a7cc69e0aacd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439242"
---
# <a name="adding-commands-to-lync-menus-in-lync-server-2013"></a><span data-ttu-id="6f7a3-103">Добавление команд в меню Lync на сервере Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f7a3-103">Adding commands to Lync menus in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f7a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f7a3-104">

<span> </span></span></span>

<span data-ttu-id="6f7a3-105">_**Тема последнего изменения:** 2016-04-11_</span><span class="sxs-lookup"><span data-stu-id="6f7a3-105">_**Topic Last Modified:** 2016-04-11_</span></span>

<span data-ttu-id="6f7a3-106">Вы можете добавить пользовательские команды в меню Lync 2013 и передать ей универсальный код ресурса (URI) текущего пользователя и выбранные контакты в приложение, с которого запускается пользовательская команда.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-106">You can add custom commands to Lync 2013 menus and pass the SIP Uniform Resource Identifier (URI) of the current user and selected contacts to the application that the custom command starts.</span></span>

<span data-ttu-id="6f7a3-107">Пользовательские команды, которые вы добавляете, могут отображаться в одном или нескольких из следующих меню:</span><span class="sxs-lookup"><span data-stu-id="6f7a3-107">The custom commands that you add can appear on one or more of the following menus:</span></span>

  - <span data-ttu-id="6f7a3-108">Меню "Инструменты" в строке меню главного окна Lync</span><span class="sxs-lookup"><span data-stu-id="6f7a3-108">The Tools menu, on the menu bar in the Lync main window</span></span>

  - <span data-ttu-id="6f7a3-109">Контекстное меню контактов из списка контактов</span><span class="sxs-lookup"><span data-stu-id="6f7a3-109">The shortcut menu for contacts in the Contacts list</span></span>

  - <span data-ttu-id="6f7a3-110">Меню "Дополнительные параметры" в окне беседы</span><span class="sxs-lookup"><span data-stu-id="6f7a3-110">The More Options menu, in the Conversation window</span></span>

  - <span data-ttu-id="6f7a3-111">Контекстное меню пользователей, перечисленных в списке участников в окне беседы</span><span class="sxs-lookup"><span data-stu-id="6f7a3-111">The shortcut menu for people listed in the Conversation window participant list</span></span>

  - <span data-ttu-id="6f7a3-112">Меню "Параметры" в карточке контакта</span><span class="sxs-lookup"><span data-stu-id="6f7a3-112">The options menu in a contact card</span></span>

<span data-ttu-id="6f7a3-113">Вы можете определять пользовательские команды для двух типов приложений — приложений, которые выполняют одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="6f7a3-113">You can define custom commands for two types of applications—applications that do either of the following:</span></span>

  - <span data-ttu-id="6f7a3-114">Применимо только к текущему пользователю и запущены на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-114">Apply only to the current user and are started on the local computer.</span></span>

  - <span data-ttu-id="6f7a3-115">Включение дополнительных пользователей, например программы для совместной работы, которые должны быть запущены на компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-115">Involve additional users, such as an online collaboration program, and must be started on each user's computer.</span></span>

<span data-ttu-id="6f7a3-116">Настраиваемая команда может быть вызвана следующими способами:</span><span class="sxs-lookup"><span data-stu-id="6f7a3-116">The custom command can be invoked in the following ways:</span></span>

  - <span data-ttu-id="6f7a3-117">Выберите одного или нескольких пользователей, а затем выберите команду настраиваемая.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-117">Select one or more users, and then choose the custom command.</span></span>

  - <span data-ttu-id="6f7a3-118">Начните двустороннюю или многосторонний разговор, а затем выберите команду "Настраиваемая".</span><span class="sxs-lookup"><span data-stu-id="6f7a3-118">Start a two-party or multiparty conversation, and then choose the custom command.</span></span>

<div>

## <a name="to-add-a-custom-command"></a><span data-ttu-id="6f7a3-119">Добавление настраиваемой команды</span><span class="sxs-lookup"><span data-stu-id="6f7a3-119">To add a custom command</span></span>

<span data-ttu-id="6f7a3-120">Добавьте команду в меню с помощью параметров реестра в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-120">Use the registry settings in the following table to add a command to the menus.</span></span> <span data-ttu-id="6f7a3-121">Эти записи размещаются в реестре в одном из следующих расположений:</span><span class="sxs-lookup"><span data-stu-id="6f7a3-121">These entries are placed in the registry at one of the following locations:</span></span>

  - <span data-ttu-id="6f7a3-122">Для 32-разрядной ОС: HKEY, \_ \_ \\ программное обеспечение для локального компьютера \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ Apps</span><span class="sxs-lookup"><span data-stu-id="6f7a3-122">For 32bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

  - <span data-ttu-id="6f7a3-123">Для 64-разрядных версий ОС: HKEY для \_ локального \_ компьютера \\ \\ WOW6432Node \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ Apps</span><span class="sxs-lookup"><span data-stu-id="6f7a3-123">For 64bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

### <a name="custom-command-registry-entries"></a><span data-ttu-id="6f7a3-124">Элементы реестра для настраиваемой команды</span><span class="sxs-lookup"><span data-stu-id="6f7a3-124">Custom Command Registry Entries</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f7a3-125">Имя</span><span class="sxs-lookup"><span data-stu-id="6f7a3-125">Name</span></span></th>
<th><span data-ttu-id="6f7a3-126">Тип</span><span class="sxs-lookup"><span data-stu-id="6f7a3-126">Type</span></span></th>
<th><span data-ttu-id="6f7a3-127">Данные</span><span class="sxs-lookup"><span data-stu-id="6f7a3-127">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f7a3-128">Имя</span><span class="sxs-lookup"><span data-stu-id="6f7a3-128">Name</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-129">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6f7a3-129">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-130">Имя приложения в том виде, в каком оно отображается в меню.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-130">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f7a3-131">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="6f7a3-131">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-132">@</span><span class="sxs-lookup"><span data-stu-id="6f7a3-132">DWORD</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-133">0 = исполняемый файл (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f7a3-133">0 = Executable (default)</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="6f7a3-134">Требуется ApplicationInstallPath.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-134">Requires ApplicationInstallPath.</span></span>


</div>
<p><span data-ttu-id="6f7a3-135">1 = протокол</span><span class="sxs-lookup"><span data-stu-id="6f7a3-135">1 = Protocol</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f7a3-136">ApplicationInstallPath</span><span class="sxs-lookup"><span data-stu-id="6f7a3-136">ApplicationInstallPath</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6f7a3-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-138">Полный путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-138">Full path of the executable.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="6f7a3-139">Должен быть указан, если ApplicationType имеет значение 0 (исполняемый объект).</span><span class="sxs-lookup"><span data-stu-id="6f7a3-139">Must be specified if ApplicationType is 0 (Executable).</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f7a3-140">Путь</span><span class="sxs-lookup"><span data-stu-id="6f7a3-140">Path</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-141">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6f7a3-141">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-142">Полный путь, который необходимо запустить вместе с любыми параметрами, включая параметры по умолчанию <em>% ID пользователя</em> % и <em>% Contact-ID%</em>.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-142">Full path to be started along with any parameters, including the default parameters <em>%user-id%</em> and <em>%contact-id%</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f7a3-143">SessionType</span><span class="sxs-lookup"><span data-stu-id="6f7a3-143">SessionType</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-144">@</span><span class="sxs-lookup"><span data-stu-id="6f7a3-144">DWORD</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-145">0 = локальный сеанс.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-145">0 = Local session.</span></span> <span data-ttu-id="6f7a3-146">Приложение будет запущено на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-146">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="6f7a3-147">1 = два сеанса (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6f7a3-147">1 = Two-party session (default).</span></span> <span data-ttu-id="6f7a3-148">Lync 2013 запускает приложение локально и отправляет уведомление на рабочем столе другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-148">Lync 2013 starts the application locally and then sends a desktop notification to the other user.</span></span> <span data-ttu-id="6f7a3-149">Другой пользователь щелкает уведомление, чтобы запустить приложение на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-149">The other user clicks the notification to start the application on their computer.</span></span></p>
<p><span data-ttu-id="6f7a3-150">2 = многокомпонентный сеанс.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-150">2 = Multiparty session.</span></span> <span data-ttu-id="6f7a3-151">Lync 2013 запускает приложение локально, а затем отправляет уведомления о рабочем столе другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-151">Lync 2013 starts the application locally and then sends desktop notifications to the other users.</span></span> <span data-ttu-id="6f7a3-152">Другой пользователь щелкает уведомление, чтобы запустить указанное приложение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-152">The other user clicks the notification to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f7a3-153">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="6f7a3-153">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-154">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6f7a3-154">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6f7a3-155">Список меню, в котором будет отображаться эта команда, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-155">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="6f7a3-156">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6f7a3-156">Possible values are:</span></span></p>
<p><span data-ttu-id="6f7a3-157">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="6f7a3-157">MainWindowActions</span></span></p>
<p><span data-ttu-id="6f7a3-158">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="6f7a3-158">MainWindowRightClick</span></span></p>
<p><span data-ttu-id="6f7a3-159">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="6f7a3-159">ConversationWindowActions</span></span></p>
<p><span data-ttu-id="6f7a3-160">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="6f7a3-160">ConversationWindowRightClick</span></span></p>
<p><span data-ttu-id="6f7a3-161">ContactCardMenu</span><span class="sxs-lookup"><span data-stu-id="6f7a3-161">ContactCardMenu</span></span></p>
<p><span data-ttu-id="6f7a3-162">Если ExtensibleMenu не определен, используются значения по умолчанию MainWindowRightClick и ConversationWindowActions.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-162">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6f7a3-163">Например, следующий редактор реестра (. REG-файл, в котором показано, как добавить элемент меню "продажи" для продаж Contoso в меню "действия" в окне беседы:</span><span class="sxs-lookup"><span data-stu-id="6f7a3-163">For example, the following Registry Editor (.REG) file shows the results of adding a Contoso Sales Contact Manager menu item to Actions menu in the Conversation window:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Lync\SessionManager\Apps\{1F9F07C6-7E0B-462B-AAD7-98C6DBEA8F69}]
    "Name"="Contoso Sales Contact Manager"
    "HelpMessage"="The Contoso Sales Contact Manager is not installed. Contact the Help Desk for more information."
    "ApplicationType"=dword:00000000
    "ApplicationInstallPath"="C:\\cscm.exe"
    "Path"="C:\\cscm.exe %user-id% %contact-id%"
    "SessionType"=dword:00000001
    "ExtensibleMenu"="ConversationWindowActions;MainWindowRightClick"

</div>

<div>

## <a name="to-access-a-custom-command"></a><span data-ttu-id="6f7a3-164">Чтобы получить доступ к настраиваемой команде</span><span class="sxs-lookup"><span data-stu-id="6f7a3-164">To access a custom command</span></span>

<span data-ttu-id="6f7a3-165">Чтобы получить доступ к настраиваемой команде после ее добавления, выполните одно из указанных ниже действий в зависимости от указанных значений ExtensibleMenu.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-165">To access a custom command after it is added, do one of the following, depending on the ExtensibleMenu values that you define:</span></span>

  - <span data-ttu-id="6f7a3-166">**MainWindowActions**   В главном окне Lync нажмите кнопку **Сервис** и выберите пункт Настраиваемая команда.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-166">**MainWindowActions**   In the Lync main window, click **Tools**, and then click your custom command.</span></span>

  - <span data-ttu-id="6f7a3-167">**MainWindowRightClick**   В главном окне Lync щелкните контакт правой кнопкой мыши и выберите нужную команду.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-167">**MainWindowRightClick**   In the Lync main window, right-click a contact, and then click your custom command.</span></span>

  - <span data-ttu-id="6f7a3-168">**ConversationWindowActions**   В окне беседы щелкните значок **Дополнительные параметры** и выберите нужную команду.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-168">**ConversationWindowActions**   In the Conversation window, click the **More Options** icon, and then click your custom command.</span></span>

  - <span data-ttu-id="6f7a3-169">**ConversationWindowRightClick**   В окне беседы щелкните правой кнопкой мыши имя контакта, а затем выберите настраиваемую команду.</span><span class="sxs-lookup"><span data-stu-id="6f7a3-169">**ConversationWindowRightClick**   In the Conversation window, right-click a contact name, and then click your custom command.</span></span>

<span data-ttu-id="6f7a3-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f7a3-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

