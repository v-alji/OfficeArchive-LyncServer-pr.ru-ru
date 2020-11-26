---
title: 'Lync Server 2013: командлеты Lync Server по категориям'
description: 'Lync Server 2013: командлеты Lync Server по категориям.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 cmdlets by category
ms:assetid: 4ce274d7-b0ec-40b8-b85e-9a0613916ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398306(v=OCS.15)
ms:contentKeyID: 48184106
ms.date: 09/20/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: df562bd11d54c9ecda4fe3d6172ed1d8bd2627d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426279"
---
# <a name="lync-server-2013-cmdlets-by-category"></a><span data-ttu-id="927d0-103">Командлеты Lync Server 2013 по категориям</span><span class="sxs-lookup"><span data-stu-id="927d0-103">Lync Server 2013 cmdlets by category</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="927d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="927d0-104">

<span> </span></span></span>

<span data-ttu-id="927d0-105">_**Тема последнего изменения:** 2017-09-20_</span><span class="sxs-lookup"><span data-stu-id="927d0-105">_**Topic Last Modified:** 2017-09-20_</span></span>

<span data-ttu-id="927d0-106">Microsoft Lync Server 2013 поставляется с практическими командлетами 550, разработанными специально для разрешения администраторам управления сервером Lync Server из командной строки.</span><span class="sxs-lookup"><span data-stu-id="927d0-106">Microsoft Lync Server 2013 ships with almost 550 cmdlets specifically designed to allow administrators to manage Lync Server from the command line.</span></span> <span data-ttu-id="927d0-107">Вы получите доступ к командлетам из командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="927d0-107">You access the cmdlets from the Lync Server Management Shell.</span></span> <span data-ttu-id="927d0-108">Вы можете получить справку по командлету прямо из командной строки, введя команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="927d0-108">You can retrieve help on a cmdlet directly from the command line by typing a command similar to the following:</span></span>

    Get-Help New-CsVoicePolicy -Full

<span data-ttu-id="927d0-109">Предыдущая команда извлечет все справочные материалы, доступные для командлета **New-CsVoicePolicy** .</span><span class="sxs-lookup"><span data-stu-id="927d0-109">The preceding command will retrieve all the help available for the **New-CsVoicePolicy** cmdlet.</span></span> <span data-ttu-id="927d0-110">Замените ссылку на **New-CsVoicePolicy** именем командлета, для которого требуется получить справку.</span><span class="sxs-lookup"><span data-stu-id="927d0-110">Substitute the reference to **New-CsVoicePolicy** with the name of the cmdlet for which you want to retrieve help.</span></span>

<span data-ttu-id="927d0-111">Чтобы получить полный список командлетов, доступных для управления Microsoft Lync Server 2013, в командной строке оболочки Lync Server Management Shell введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="927d0-111">To retrieve a full list of cmdlets available for managing Microsoft Lync Server 2013, type the following at the Lync Server Management Shell command prompt:</span></span>

    Get-Command * -Module Lync -CommandType cmdlet

<span data-ttu-id="927d0-112">Если вы не знаете, какие командлеты вам нужны, мы также предоставили список командлетов и их справочные разделы.</span><span class="sxs-lookup"><span data-stu-id="927d0-112">If you are unsure which cmdlets you need, we have also provided a categorized list of cmdlets and their help topics.</span></span> <span data-ttu-id="927d0-113">Вы обнаружите, что некоторые командлеты отображаются в нескольких категориях, которые были намеренно применены к нескольким областям продукта.</span><span class="sxs-lookup"><span data-stu-id="927d0-113">You will find that some of the cmdlets show up in more than one category, which was intentional as they apply to multiple areas of the product.</span></span> <span data-ttu-id="927d0-114">Ниже приведен список категорий.</span><span class="sxs-lookup"><span data-stu-id="927d0-114">The following is a list of categories:</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="927d0-115">Справочник по командлетам Skype для бизнеса перенесен на веб-сайт docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="927d0-115">Skype for Business cmdlet reference has moved to docs.microsoft.com.</span></span> <span data-ttu-id="927d0-116">По представленным ниже ссылкам вы можете перейти на новую страницу портала docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="927d0-116">Clicking on the links below will take you to the new docs.microsoft.com page.</span></span> <span data-ttu-id="927d0-117">Теперь весь контент предлагается с открытым исходным кодом и доступен в сообществе GitHub.</span><span class="sxs-lookup"><span data-stu-id="927d0-117">The content is now open sourced and available for community contributions through GitHub.</span></span> <span data-ttu-id="927d0-118">Хотите принять участие в работе с ним?</span><span class="sxs-lookup"><span data-stu-id="927d0-118">Interested in contributing?</span></span> <span data-ttu-id="927d0-119">Ознакомьтесь с ФАЙЛОМ README в репозитории здесь: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span><span class="sxs-lookup"><span data-stu-id="927d0-119">Check out the README in the repo here: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="927d0-120">Содержание</span><span class="sxs-lookup"><span data-stu-id="927d0-120">In This Section</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="927d0-121"><a href="lync-server-2013-user-management-cmdlets.md">Командлеты управления пользователями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-121"><a href="lync-server-2013-user-management-cmdlets.md">User management cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-122"><a href="lync-server-2013-voice-application-cmdlets.md">Командлеты голосовых приложений в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-122"><a href="lync-server-2013-voice-application-cmdlets.md">Voice application cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="927d0-123"><a href="lync-server-2013-client-management-cmdlets.md">Командлеты управления клиентом в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-123"><a href="lync-server-2013-client-management-cmdlets.md">Client management cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-124"><a href="lync-server-2013-advanced-enterprise-voice-cmdlets.md">Дополнительные командлеты для корпоративных голосовых команд в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-124"><a href="lync-server-2013-advanced-enterprise-voice-cmdlets.md">Advanced Enterprise Voice cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="927d0-125"><a href="lync-server-2013-im-and-presence-cmdlets.md">Командлеты для обмена мгновенными сообщениями и присутствия в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-125"><a href="lync-server-2013-im-and-presence-cmdlets.md">IM and presence cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-126"><a href="lync-server-2013-pstn-connectivity-cmdlets.md">Командлеты подключения PSTN в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-126"><a href="lync-server-2013-pstn-connectivity-cmdlets.md">PSTN connectivity cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="927d0-127"><a href="lync-server-2013-conferencing-cmdlets.md">Командлеты конференц-связи в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-127"><a href="lync-server-2013-conferencing-cmdlets.md">Conferencing cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-128"><a href="lync-server-2013-phones-and-devices-cmdlets.md">Командлеты для телефонов и устройств в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-128"><a href="lync-server-2013-phones-and-devices-cmdlets.md">Phones and devices cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="927d0-129"><a href="lync-server-2013-infrastructure-and-deployment-cmdlets.md">Командлеты инфраструктуры и развертывания в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-129"><a href="lync-server-2013-infrastructure-and-deployment-cmdlets.md">Infrastructure and deployment cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-130"><a href="lync-server-2013-migration-and-coexistence-cmdlets.md">Командлеты миграции и сосуществования в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-130"><a href="lync-server-2013-migration-and-coexistence-cmdlets.md">Migration and coexistence cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="927d0-131"><a href="lync-server-2013-security-cmdlets.md">Командлеты безопасности в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-131"><a href="lync-server-2013-security-cmdlets.md">Security cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-132"><a href="lync-server-2013-lync-server-management-shell-configuration-cmdlets.md">Командлеты конфигурации оболочки Lync Server Management Shell в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-132"><a href="lync-server-2013-lync-server-management-shell-configuration-cmdlets.md">Lync Server Management Shell configuration cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="927d0-133"><a href="lync-server-2013-server-roles-and-services-cmdlets.md">Командлеты серверных ролей и служб в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-133"><a href="lync-server-2013-server-roles-and-services-cmdlets.md">Server roles and services cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-134"><a href="lync-server-2013-mobility-cmdlets.md">Командлеты для мобильных устройств в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-134"><a href="lync-server-2013-mobility-cmdlets.md">Mobility cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="927d0-135"><a href="lync-server-2013-application-management-cmdlets.md">Командлеты управления приложениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-135"><a href="lync-server-2013-application-management-cmdlets.md">Application management cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-136"><a href="lync-server-2013-persistent-chat-server-cmdlets.md">Командлеты сервера сохраняемого чата в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-136"><a href="lync-server-2013-persistent-chat-server-cmdlets.md">Persistent Chat Server cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="927d0-137"><a href="lync-server-2013-federation-and-external-access-cmdlets.md">Командлеты интеграции и внешнего доступа в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-137"><a href="lync-server-2013-federation-and-external-access-cmdlets.md">Federation and external access cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="927d0-138"><a href="lync-server-2013-centralized-logging-cmdlets.md">Командлеты централизованного ведения журналов в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-138"><a href="lync-server-2013-centralized-logging-cmdlets.md">Centralized Logging cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="927d0-139"><a href="lync-server-2013-enterprise-voice-cmdlets.md">Командлеты для корпоративных голосовых команд в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="927d0-139"><a href="lync-server-2013-enterprise-voice-cmdlets.md">Enterprise Voice cmdlets in Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="927d0-140">См. также</span><span class="sxs-lookup"><span data-stu-id="927d0-140">See Also</span></span>


[<span data-ttu-id="927d0-141">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="927d0-141">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="927d0-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="927d0-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

