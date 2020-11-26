---
title: 'Lync Server 2013: требования служб IIS'
description: 'Lync Server 2013: требования к службам IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Internet Information Services (IIS) requirements
ms:assetid: 4f57a605-a8a9-4c5a-9a18-05ecb3d9ab6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398321(v=OCS.15)
ms:contentKeyID: 48184128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd8de55fa4611c3ab29eac7d7c28c522b418e77d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426859"
---
# <a name="internet-information-services-iis-requirements-in-lync-server-2013"></a><span data-ttu-id="db804-103">Требования служб IIS в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db804-103">Internet Information Services (IIS) requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db804-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db804-104">

<span> </span></span></span>

<span data-ttu-id="db804-105">_**Тема последнего изменения:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="db804-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="db804-106">Для некоторых компонентов Lync Server 2013 требуются информационные службы Интернета (IIS).</span><span class="sxs-lookup"><span data-stu-id="db804-106">Several Lync Server 2013 components require Internet Information Services (IIS).</span></span> <span data-ttu-id="db804-107">В этой статье описаны особые возможности IIS, необходимые для поддержки сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="db804-107">This topic describes the specific IIS features required to support Lync Server.</span></span> <span data-ttu-id="db804-108">В подразделах этого раздела описаны требования конкретных компонентов IIS.</span><span class="sxs-lookup"><span data-stu-id="db804-108">The topics in this section describe the requirements of specific components for IIS.</span></span>

<span data-ttu-id="db804-109">Если роль веб-сервера (IIS) включена в Windows Server 2008, по умолчанию устанавливаются различные службы ролей.</span><span class="sxs-lookup"><span data-stu-id="db804-109">When the Web Server (IIS) role is enabled on Windows Server 2008, various role services are installed by default.</span></span> <span data-ttu-id="db804-110">В приведенной ниже таблице описаны дополнительные службы ролей, которые необходимо установить, если в Windows Server 2008 включена роль веб-сервера (IIS).</span><span class="sxs-lookup"><span data-stu-id="db804-110">The following table describes the additional role services that must be installed when the Web Server (IIS) role is enabled on Windows Server 2008.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db804-111">Служба ролей</span><span class="sxs-lookup"><span data-stu-id="db804-111">Role service</span></span></th>
<th><span data-ttu-id="db804-112">Компонент</span><span class="sxs-lookup"><span data-stu-id="db804-112">Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db804-113">Основные возможности HTTP</span><span class="sxs-lookup"><span data-stu-id="db804-113">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="db804-114">Перенаправление HTTP</span><span class="sxs-lookup"><span data-stu-id="db804-114">HTTP Redirection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db804-115">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="db804-115">Application Development</span></span></p></td>
<td><p><span data-ttu-id="db804-116">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="db804-116">ASP.NET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db804-117">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="db804-117">Application Development</span></span></p></td>
<td><p><span data-ttu-id="db804-118">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="db804-118">.NET Extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db804-119">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="db804-119">Application Development</span></span></p></td>
<td><p><span data-ttu-id="db804-120">Расширения ISAPI</span><span class="sxs-lookup"><span data-stu-id="db804-120">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db804-121">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="db804-121">Application Development</span></span></p></td>
<td><p><span data-ttu-id="db804-122">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="db804-122">ISAPI Filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db804-123">Работоспособность и диагностика</span><span class="sxs-lookup"><span data-stu-id="db804-123">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="db804-124">Средства ведения журналов</span><span class="sxs-lookup"><span data-stu-id="db804-124">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db804-125">Работоспособность и диагностика</span><span class="sxs-lookup"><span data-stu-id="db804-125">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="db804-126">Трассировка</span><span class="sxs-lookup"><span data-stu-id="db804-126">Tracing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db804-127">Безопасность</span><span class="sxs-lookup"><span data-stu-id="db804-127">Security</span></span></p></td>
<td><p><span data-ttu-id="db804-128">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="db804-128">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db804-129">Безопасность</span><span class="sxs-lookup"><span data-stu-id="db804-129">Security</span></span></p></td>
<td><p><span data-ttu-id="db804-130">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="db804-130">Windows Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db804-131">Средства управления</span><span class="sxs-lookup"><span data-stu-id="db804-131">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="db804-132">Сценарии и средства управления для служб IIS</span><span class="sxs-lookup"><span data-stu-id="db804-132">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db804-133">Средства управления</span><span class="sxs-lookup"><span data-stu-id="db804-133">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="db804-134">Совместимость управления IIS 6</span><span class="sxs-lookup"><span data-stu-id="db804-134">IIS 6 Management Compatibility</span></span></p></td>
</tr>
</tbody>
</table>


<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="разрешения" alt="security" /><span data-ttu-id="db804-136">Примечание о безопасности:</span><span class="sxs-lookup"><span data-stu-id="db804-136">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db804-137">Если вы используете сервер IIS 7,0 в операционной системе Windows Server 2008, Настройка сервера Lync Server отключает проверку подлинности в режиме ядра в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="db804-137">If you are using IIS 7.0 on a Windows Server 2008 operating system, Lync Server Setup disables kernel mode authentication in IIS.</span></span></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="db804-138">Содержание</span><span class="sxs-lookup"><span data-stu-id="db804-138">In This Section</span></span>

  - [<span data-ttu-id="db804-139">Требования IIS для пулов переднего плана и серверов Standard Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db804-139">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)

<span data-ttu-id="db804-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db804-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

