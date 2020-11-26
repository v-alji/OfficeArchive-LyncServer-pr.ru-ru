---
title: 'Lync Server 2013: процесс развертывания мобильного клиента'
description: 'Lync Server 2013: процесс развертывания клиента для мобильных устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobile client deployment process
ms:assetid: 6498235b-2fa9-421d-bfa0-0ccc09508dbd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690982(v=OCS.15)
ms:contentKeyID: 51541484
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fa4e9e1d272915e06009df5c06480309ce104e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425565"
---
# <a name="mobile-client-deployment-process-in-lync-server-2013"></a><span data-ttu-id="a09b0-103">Процесс развертывания мобильных клиентов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a09b0-103">Mobile client deployment process in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a09b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a09b0-104">

<span> </span></span></span>

<span data-ttu-id="a09b0-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="a09b0-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="a09b0-106">После завершения развертывания Microsoft Lync Server 2013 пользователи могут установить приложение Lync 2013 из мобильного магазина, с помощью которого они привычны для определенного устройства.</span><span class="sxs-lookup"><span data-stu-id="a09b0-106">After a deployment of Microsoft Lync Server 2013 has been completed, users can install the Lync 2013 app from the mobile marketplace that they are accustomed to using for their specific device.</span></span>

<div>

## <a name="lync-mobile-deployment-process"></a><span data-ttu-id="a09b0-107">Процесс развертывания Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="a09b0-107">Lync Mobile Deployment Process</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a09b0-108">Этап</span><span class="sxs-lookup"><span data-stu-id="a09b0-108">Phase</span></span></th>
<th><span data-ttu-id="a09b0-109">Шаги</span><span class="sxs-lookup"><span data-stu-id="a09b0-109">Steps</span></span></th>
<th><span data-ttu-id="a09b0-110">Разрешения</span><span class="sxs-lookup"><span data-stu-id="a09b0-110">Permissions</span></span></th>
<th><span data-ttu-id="a09b0-111">Документация</span><span class="sxs-lookup"><span data-stu-id="a09b0-111">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a09b0-112">Выполнять задачи, выполняемые перед настройкой.</span><span class="sxs-lookup"><span data-stu-id="a09b0-112">Perform pre-setup tasks.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a09b0-113">Убедитесь, что развертывание Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a09b0-113">Verify Lync Server 2013 deployment.</span></span></p></li>
<li><p><span data-ttu-id="a09b0-114">Проверка требований сертификата.</span><span class="sxs-lookup"><span data-stu-id="a09b0-114">Verify certificate requirements.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a09b0-115">Администратор</span><span class="sxs-lookup"><span data-stu-id="a09b0-115">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a09b0-116"><a href="lync-server-2013-planning-for-mobility.md">Планирование мобильных устройств в Lync server 2013</a> в документации по планированию сервера.</span><span class="sxs-lookup"><span data-stu-id="a09b0-116"><a href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</a> in the server planning documentation.</span></span></p>
<p><span data-ttu-id="a09b0-117"><a href="lync-server-2013-deploying-mobility.md">Развертывание мобильных устройств в Lync server 2013</a> в документации по развертыванию сервера.</span><span class="sxs-lookup"><span data-stu-id="a09b0-117"><a href="lync-server-2013-deploying-mobility.md">Deploying mobility in Lync Server 2013</a> in the server deployment documentation.</span></span></p>
<p><span data-ttu-id="a09b0-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Требования к инфраструктуре сертификатов для Lync Server 2013</a> в документации по планированию сервера.</span><span class="sxs-lookup"><span data-stu-id="a09b0-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Certificate infrastructure requirements for Lync Server 2013</a> in the server planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a09b0-119">Установите приложение Lync на тестовом устройстве.</span><span class="sxs-lookup"><span data-stu-id="a09b0-119">Install the Lync application on a test device.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a09b0-120">Установите необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="a09b0-120">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="a09b0-121">Установка из магазина, относящегося к мобильному устройству.</span><span class="sxs-lookup"><span data-stu-id="a09b0-121">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a09b0-122">Администратор</span><span class="sxs-lookup"><span data-stu-id="a09b0-122">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a09b0-123">Инструкции по установке, связанные с мобильным устройством на странице <a href="lync-server-2013-deploying-mobile-clients.md">развертывание мобильных клиентов в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="a09b0-123">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a09b0-124">Настройте клиент.</span><span class="sxs-lookup"><span data-stu-id="a09b0-124">Configure the client.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a09b0-125">Настройте параметры входа и сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="a09b0-125">Configure sign-in settings and server information.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="a09b0-126">Администратор</span><span class="sxs-lookup"><span data-stu-id="a09b0-126">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a09b0-127"><a href="lync-server-2013-deploying-mobile-clients.md">Развертывание мобильных клиентов в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a09b0-127"><a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a09b0-128">Протестируйте сценарии для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="a09b0-128">Test mobile scenarios.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a09b0-129">Протестируйте обмен мгновенными сообщениями и сведения о присутствии.</span><span class="sxs-lookup"><span data-stu-id="a09b0-129">Test instant messaging (IM) and presence.</span></span></p></li>
<li><p><span data-ttu-id="a09b0-130">Протестируйте Конференц-связь с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="a09b0-130">Test dial-out conferencing.</span></span></p></li>
<li><p><span data-ttu-id="a09b0-131">Поиск контакта в корпоративном справочнике.</span><span class="sxs-lookup"><span data-stu-id="a09b0-131">Search for a contact in the corporate directory.</span></span></p></li>
<li><p><span data-ttu-id="a09b0-132">Тест push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a09b0-132">Test push notifications.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a09b0-133">Администратор</span><span class="sxs-lookup"><span data-stu-id="a09b0-133">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a09b0-134">Инструкции для проверки, специфичные для мобильного устройства при <a href="lync-server-2013-deploying-mobile-clients.md">развертывании мобильных клиентов в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="a09b0-134">Verification instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a09b0-135">Установите приложение Lync на мобильных телефонах.</span><span class="sxs-lookup"><span data-stu-id="a09b0-135">Install the Lync application on mobile phones.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a09b0-136">Установите необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="a09b0-136">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="a09b0-137">Установка из магазина, относящегося к мобильному устройству.</span><span class="sxs-lookup"><span data-stu-id="a09b0-137">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a09b0-138">Пользователь</span><span class="sxs-lookup"><span data-stu-id="a09b0-138">User</span></span></p></td>
<td><p><span data-ttu-id="a09b0-139">Инструкции по установке, связанные с мобильным устройством на странице <a href="lync-server-2013-deploying-mobile-clients.md">развертывание мобильных клиентов в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="a09b0-139">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a09b0-140">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a09b0-140">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

