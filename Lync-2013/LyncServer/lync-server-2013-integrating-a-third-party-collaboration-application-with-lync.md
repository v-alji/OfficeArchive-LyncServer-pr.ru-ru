---
title: Интеграция стороннего приложения для совместной работы с Lync
description: Интеграция стороннего приложения для совместной работы с Lync.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating a third-party collaboration application with Lync
ms:assetid: 00b9312c-b0c8-4f79-8b76-05b2d820e197
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398068(v=OCS.15)
ms:contentKeyID: 48183224
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adbe1abab83a569f581af034fc46abfef4cf819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399850"
---
# <a name="integrating-a-third-party-collaboration-application-with-lync-server-2013"></a><span data-ttu-id="4d650-103">Интеграция стороннего приложения для совместной работы с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d650-103">Integrating a third-party collaboration application with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d650-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d650-104">

<span> </span></span></span>

<span data-ttu-id="4d650-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="4d650-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="4d650-106">Вы можете интегрировать Lync 2013 с любым сторонним приложением для совместной работы, добавив сведения о приложении в реестр.</span><span class="sxs-lookup"><span data-stu-id="4d650-106">You can integrate Lync 2013 with any third-party online collaboration application by adding information about the application to the registry.</span></span> <span data-ttu-id="4d650-107">Вы можете использовать Lync 2013 для начала сеансов конференций данных, размещенных на внутреннем сервере, в Интернете или в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="4d650-107">You can use Lync 2013 to start data conferencing sessions hosted on an in-house server, an Internet-based service, or both.</span></span> <span data-ttu-id="4d650-108">Сеанс совместной работы или конференц-связи можно запустить из списка контактов или из существующего сеанса обмена мгновенными сообщениями, голосовых и видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="4d650-108">The collaboration or data conferencing session can be started from the Contacts list or from an existing instant messaging, voice, or video session.</span></span> <span data-ttu-id="4d650-109">Lync 2013 действует только в качестве транспортного средства для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="4d650-109">Lync 2013 acts only as the vehicle for starting the application.</span></span> <span data-ttu-id="4d650-110">Любые существующие беседы Lync 2013 остаются активными после начала сеанса совместной работы через Интернет.</span><span class="sxs-lookup"><span data-stu-id="4d650-110">Any existing Lync 2013 conversations remain active after the online collaboration session has begun.</span></span>

<span data-ttu-id="4d650-111">В следующих разделах описано, как интегрировать Lync 2013 с приложениями для совместной работы на основе Интернета и сервера.</span><span class="sxs-lookup"><span data-stu-id="4d650-111">The following sections describe how to integrate Lync 2013 with Internet-based and server-based collaboration applications.</span></span>

<div>

## <a name="integrating-an-internet-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="4d650-112">Интеграция приложения для совместной работы Internet-Based с помощью Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4d650-112">Integrating an Internet-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="4d650-113">Как правило, для интеграции стороннего приложения для совместной работы используются следующие этапы:</span><span class="sxs-lookup"><span data-stu-id="4d650-113">Generally, the steps involved in integrating a third-party collaboration application are as follows:</span></span>

1.  <span data-ttu-id="4d650-114">Сведения о приложении добавляются в реестр.</span><span class="sxs-lookup"><span data-stu-id="4d650-114">Information about the application is added to the registry.</span></span>

2.  <span data-ttu-id="4d650-115">Организатор входит в Lync 2013 и выбирает контакты для совместного использования данных и совместной работы.</span><span class="sxs-lookup"><span data-stu-id="4d650-115">The organizer signs in to Lync 2013 and selects contacts for data sharing and collaboration.</span></span> <span data-ttu-id="4d650-116">Возможно также, что Организатор уже находится в беседе и решает добавить Конференц-связь с данными.</span><span class="sxs-lookup"><span data-stu-id="4d650-116">Or, the organizer may already be in a conversation and decide to add data conferencing.</span></span>

3.  <span data-ttu-id="4d650-117">Lync 2013 считывает реестр, запускает приложение для совместной работы, а затем отправляет настраиваемое сообщение SIP (appINVITE) выбранным участникам.</span><span class="sxs-lookup"><span data-stu-id="4d650-117">Lync 2013 reads the registry, starts the collaboration application, and then sends a custom SIP message—an appINVITE—to the selected participants.</span></span>

4.  <span data-ttu-id="4d650-118">Участники приняли приглашение, и приложение для совместной работы запущено на компьютере каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d650-118">Participants accept the invitation, and the collaboration application is started on each person’s computer.</span></span> <span data-ttu-id="4d650-119">Lync 2013 использует реестр для определения приложения для совместной работы, а затем запускает приложение, используя параметры, включенные в сообщение appINVITE.</span><span class="sxs-lookup"><span data-stu-id="4d650-119">Lync 2013 uses the registry to determine which collaboration application to use, and then starts that application by using the parameters included in the appINVITE message.</span></span>

<span data-ttu-id="4d650-120">В приведенной ниже таблице описаны записи реестра, необходимые для интеграции приложения для совместной работы в Интернете с Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="4d650-120">The following table describes the registry entries required to integrate an Internet-based collaboration application with Lync 2013.</span></span> <span data-ttu-id="4d650-121">Эти записи размещаются в реестре в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="4d650-121">These entries are placed in the registry in the following location:</span></span>

  - <span data-ttu-id="4d650-122">\_ \_ Программное обеспечение для ЛОКАЛЬНОГО компьютера hKey \\ \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ \\ Параметры приложений</span><span class="sxs-lookup"><span data-stu-id="4d650-122">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="4d650-123">Записи реестра для приложения для совместной работы через Интернет</span><span class="sxs-lookup"><span data-stu-id="4d650-123">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d650-124">Имя</span><span class="sxs-lookup"><span data-stu-id="4d650-124">Name</span></span></th>
<th><span data-ttu-id="4d650-125">Тип</span><span class="sxs-lookup"><span data-stu-id="4d650-125">Type</span></span></th>
<th><span data-ttu-id="4d650-126">Данные</span><span class="sxs-lookup"><span data-stu-id="4d650-126">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d650-127">Имя</span><span class="sxs-lookup"><span data-stu-id="4d650-127">Name</span></span></p></td>
<td><p><span data-ttu-id="4d650-128">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-128">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-129">Меню "имя приложения" для Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="4d650-129">The application name for Lync 2013 menus.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d650-130">SmallIcon</span><span class="sxs-lookup"><span data-stu-id="4d650-130">SmallIcon</span></span></p></td>
<td><p><span data-ttu-id="4d650-131">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-131">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-132">Путь к 16-пиксельному значку x 16 пикселей, BMP или PNG.</span><span class="sxs-lookup"><span data-stu-id="4d650-132">Path to 16-pixel x 16-pixel icon, BMP or PNG.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d650-133">Путь</span><span class="sxs-lookup"><span data-stu-id="4d650-133">Path</span></span></p></td>
<td><p><span data-ttu-id="4d650-134">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-134">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-135">Путь участника для запуска приложения для совместной работы в Интернете.</span><span class="sxs-lookup"><span data-stu-id="4d650-135">Participant path for starting the online collaboration application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d650-136">OriginatorPath</span><span class="sxs-lookup"><span data-stu-id="4d650-136">OriginatorPath</span></span></p></td>
<td><p><span data-ttu-id="4d650-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-138">Путь организатора для веб-приложения совместной работы.</span><span class="sxs-lookup"><span data-stu-id="4d650-138">Organizer path for starting the online collaboration application.</span></span> <span data-ttu-id="4d650-139">Этот путь может содержать один или несколько настраиваемых параметров, определенных в подразделе "Параметры".</span><span class="sxs-lookup"><span data-stu-id="4d650-139">This path can contain one or more custom parameters as defined in the Parameters subkey.</span></span> <span data-ttu-id="4d650-140">Например <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span><span class="sxs-lookup"><span data-stu-id="4d650-140">For example, <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d650-141">SessionType</span><span class="sxs-lookup"><span data-stu-id="4d650-141">SessionType</span></span></p></td>
<td><p><span data-ttu-id="4d650-142">@</span><span class="sxs-lookup"><span data-stu-id="4d650-142">DWORD</span></span></p></td>
<td><p><span data-ttu-id="4d650-143">0 = локальный сеанс.</span><span class="sxs-lookup"><span data-stu-id="4d650-143">0 = Local session.</span></span> <span data-ttu-id="4d650-144">Приложение будет запущено на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4d650-144">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="4d650-145">1 = два сеанса (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4d650-145">1 = Two-party session (default).</span></span> <span data-ttu-id="4d650-146">Lync 2013 запускает приложение локально, а затем отправляет системное уведомление другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="4d650-146">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="4d650-147">Другой пользователь щелкает уведомление и запускает указанное приложение на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="4d650-147">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="4d650-148">2 = многокомпонентный сеанс.</span><span class="sxs-lookup"><span data-stu-id="4d650-148">2 = Multiparty session.</span></span> <span data-ttu-id="4d650-149">Lync 2013 запускает приложение локально, а затем отправляет системные уведомления другим пользователям, запрашивая их, чтобы запустить указанное приложение на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="4d650-149">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their own computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d650-150">ExensibleMenu</span><span class="sxs-lookup"><span data-stu-id="4d650-150">ExensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="4d650-151">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-151">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-152">Список меню, в котором будет отображаться эта команда, отделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="4d650-152">A list of the menus where this command will appear, separated by semi-colons.</span></span> <span data-ttu-id="4d650-153">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4d650-153">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="4d650-154">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="4d650-154">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="4d650-155">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="4d650-155">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="4d650-156">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="4d650-156">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="4d650-157">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="4d650-157">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="4d650-158">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="4d650-158">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="4d650-159">Если ExtensibleMenu не определен, используются значения по умолчанию MainWindowRightClick и ConversationWindowActions.</span><span class="sxs-lookup"><span data-stu-id="4d650-159">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4d650-160">В приведенной ниже таблице описаны элементы реестра для параметров.</span><span class="sxs-lookup"><span data-stu-id="4d650-160">The following table describes the registry entries for parameters.</span></span> <span data-ttu-id="4d650-161">Эти записи будут находиться на странице HKEY \_ текущего \_ пользователя, \\ \\ \\ \\ \\ \\ SessionManager \\ Параметры приложений Microsoft Office 15,0 Lync \\ .</span><span class="sxs-lookup"><span data-stu-id="4d650-161">These entries are place at HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters.</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="4d650-162">Записи реестра для приложения для совместной работы через Интернет</span><span class="sxs-lookup"><span data-stu-id="4d650-162">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d650-163">Имя</span><span class="sxs-lookup"><span data-stu-id="4d650-163">Name</span></span></th>
<th><span data-ttu-id="4d650-164">Тип</span><span class="sxs-lookup"><span data-stu-id="4d650-164">Type</span></span></th>
<th><span data-ttu-id="4d650-165">Данные</span><span class="sxs-lookup"><span data-stu-id="4d650-165">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d650-166">Параметр1</span><span class="sxs-lookup"><span data-stu-id="4d650-166">Param1</span></span></p></td>
<td><p><span data-ttu-id="4d650-167">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-167">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-168">Используется в размеченом формате ( <code>%Parm1%</code> ) для добавления значений, связанных с пользователем, в раздел реестра OriginatorPath.</span><span class="sxs-lookup"><span data-stu-id="4d650-168">Used in tokenized format (<code>%Parm1%</code>) to add user-specific values to the OriginatorPath registry key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d650-169">Параметр2</span><span class="sxs-lookup"><span data-stu-id="4d650-169">Param2</span></span></p></td>
<td><p><span data-ttu-id="4d650-170">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-170">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-171">Просмотрите раздел Param1.</span><span class="sxs-lookup"><span data-stu-id="4d650-171">See Param1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d650-172">Param3</span><span class="sxs-lookup"><span data-stu-id="4d650-172">Param3</span></span></p></td>
<td><p><span data-ttu-id="4d650-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-174">Просмотрите раздел Param1.</span><span class="sxs-lookup"><span data-stu-id="4d650-174">See Param1.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4d650-175">В следующем примере параметры реестра интегрируют клиент ADatum для совместной работы с помощью Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="4d650-175">The following example registry settings integrate ADatum Collaboration Client with Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Path"="https://meetingservice.adatum.com/cc/%param1%/meet/%param2%"
    "OriginatorPath"="https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&role=present&pw=%param3%"
    "SessionType"=dword:00000002
    "ApplicationType"=dword:00000001
    "LiveServerIntegration"=dword:00000000
    "Name"="ADatum Online Collaboration Service"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"
    
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Param1"="meetserv"
    "Param2"="admin"
    "Param3"="abcdefg123"

</div>

<div>

## <a name="integrating-a-server-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="4d650-176">Интеграция приложения для совместной работы Server-Based с помощью Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4d650-176">Integrating a Server-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="4d650-177">Параметры, необходимые для запуска приложения для совместной работы на базе сервера в Lync 2013, похожи на возможности, описанные в предыдущем разделе, интеграция приложения для совместной работы Internet-Based с Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="4d650-177">The settings to add commands for starting a server-based collaboration application from within Lync 2013 are similar to those described in the previous section, Integrating an Internet-Based Collaboration Application with Lync 2013.</span></span> <span data-ttu-id="4d650-178">Однако OriginatorPath не требуется, а некоторые значения изменяются.</span><span class="sxs-lookup"><span data-stu-id="4d650-178">However, the OriginatorPath is not required, and some values are changed.</span></span> <span data-ttu-id="4d650-179">Записи в реестре размещаются в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="4d650-179">Registry entries are placed in the following location:</span></span>

  - <span data-ttu-id="4d650-180">\_ \_ Программное обеспечение для ЛОКАЛЬНОГО компьютера hKey \\ \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ \\ Параметры приложений</span><span class="sxs-lookup"><span data-stu-id="4d650-180">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-a-server-based-collaboration-application"></a><span data-ttu-id="4d650-181">Записи реестра для приложения для совместной работы на базе сервера</span><span class="sxs-lookup"><span data-stu-id="4d650-181">Registry Entries for a Server-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d650-182">Имя</span><span class="sxs-lookup"><span data-stu-id="4d650-182">Name</span></span></th>
<th><span data-ttu-id="4d650-183">Тип</span><span class="sxs-lookup"><span data-stu-id="4d650-183">Type</span></span></th>
<th><span data-ttu-id="4d650-184">Данные</span><span class="sxs-lookup"><span data-stu-id="4d650-184">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d650-185">Имя</span><span class="sxs-lookup"><span data-stu-id="4d650-185">Name</span></span></p></td>
<td><p><span data-ttu-id="4d650-186">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-186">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-187">Имя приложения в том виде, в каком оно отображается в меню.</span><span class="sxs-lookup"><span data-stu-id="4d650-187">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d650-188">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="4d650-188">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="4d650-189">@</span><span class="sxs-lookup"><span data-stu-id="4d650-189">DWORD</span></span></p></td>
<td><p><span data-ttu-id="4d650-190">Значение = 1.</span><span class="sxs-lookup"><span data-stu-id="4d650-190">Value = 1.</span></span> <span data-ttu-id="4d650-191">Задает тип приложения "протокол".</span><span class="sxs-lookup"><span data-stu-id="4d650-191">Sets the application type to protocol.</span></span> <span data-ttu-id="4d650-192">Другие возможные значения в этом случае не применяются.</span><span class="sxs-lookup"><span data-stu-id="4d650-192">The other possible values do not apply in this case.</span></span> <span data-ttu-id="4d650-193">Если он отсутствует, ApplicationType имеет значение 0 (исполняемый объект).</span><span class="sxs-lookup"><span data-stu-id="4d650-193">If not present, ApplicationType is set to 0 (executable).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d650-194">Путь</span><span class="sxs-lookup"><span data-stu-id="4d650-194">Path</span></span></p></td>
<td><p><span data-ttu-id="4d650-195">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-195">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-196">Протокол, используемый для запуска приложения для совместной работы.</span><span class="sxs-lookup"><span data-stu-id="4d650-196">Protocol used to start the collaboration application.</span></span> <span data-ttu-id="4d650-197">Для Live Meeting 2007 для параметра путь задано значение Path <code>meet:%conf-uri%</code> .</span><span class="sxs-lookup"><span data-stu-id="4d650-197">For Live Meeting 2007, the value of Path is set to <code>meet:%conf-uri%</code>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d650-198">SessionType</span><span class="sxs-lookup"><span data-stu-id="4d650-198">SessionType</span></span></p></td>
<td><p><span data-ttu-id="4d650-199">@</span><span class="sxs-lookup"><span data-stu-id="4d650-199">DWORD</span></span></p></td>
<td><p><span data-ttu-id="4d650-200">0 = локальный сеанс.</span><span class="sxs-lookup"><span data-stu-id="4d650-200">0 = Local session.</span></span> <span data-ttu-id="4d650-201">Приложение будет запущено на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4d650-201">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="4d650-202">1 = два сеанса (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4d650-202">1 = Two-party session (default).</span></span> <span data-ttu-id="4d650-203">Lync 2013 запускает приложение локально, а затем отправляет системное уведомление другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="4d650-203">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="4d650-204">Другой пользователь щелкает уведомление и запускает указанное приложение на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="4d650-204">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="4d650-205">2 = многокомпонентный сеанс.</span><span class="sxs-lookup"><span data-stu-id="4d650-205">2 = Multiparty session.</span></span> <span data-ttu-id="4d650-206">Lync 2013 запускает приложение локально, а затем отправляет пользователям системные уведомления о том, чтобы запустить указанное приложение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4d650-206">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d650-207">MCUType</span><span class="sxs-lookup"><span data-stu-id="4d650-207">MCUType</span></span></p></td>
<td><p><span data-ttu-id="4d650-208">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-208">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-209">DATA (данные) — тип сервера.</span><span class="sxs-lookup"><span data-stu-id="4d650-209">DATA = The type of server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d650-210">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="4d650-210">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="4d650-211">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4d650-211">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="4d650-212">Список меню, в котором будет отображаться эта команда, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="4d650-212">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="4d650-213">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4d650-213">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="4d650-214">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="4d650-214">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="4d650-215">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="4d650-215">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="4d650-216">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="4d650-216">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="4d650-217">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="4d650-217">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="4d650-218">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="4d650-218">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="4d650-219">Если ExtensibleMenu не определен, используются значения по умолчанию MainWindowRightClick и ConversationWindowActions.</span><span class="sxs-lookup"><span data-stu-id="4d650-219">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4d650-220">В следующем примере показано, как добавить команды для запуска клиента совместной работы ADatum в Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="4d650-220">The following example adds commands to start ADatum Collaboration Client from within Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{27877e66-615c-4582-ab88-0cb2ca05d951}]
    "Path"="meet:%conf-uri%"
    "SessionType"=dword:00000002
    "LiveServerIntegration"=dword:00000001
    "ApplicationType"=dword:00000001
    "Name"="ADatum Collaboration Client"
    "MCUType"="Data"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"

<span data-ttu-id="4d650-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d650-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

