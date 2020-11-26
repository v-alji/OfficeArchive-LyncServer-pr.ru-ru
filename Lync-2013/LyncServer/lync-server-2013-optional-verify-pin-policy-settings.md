---
title: 'Lync Server 2013: проверка параметров политики ПИН-кодов (необязательно)'
description: 'Lync Server 2013: (необязательный) Проверка параметров политики для ПИН-кода.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify PIN policy settings
ms:assetid: d000d2e7-dfd8-4dea-b1ff-f5385d0cfff3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398892(v=OCS.15)
ms:contentKeyID: 48185415
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa1598d3bf2def6f999ed1588f35a9d0d4f161cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445201"
---
# <a name="optional-verify-pin-policy-settings-in-lync-server-2013"></a><span data-ttu-id="9c8c1-103">Проверка параметров политики ПИН-кодов в Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="9c8c1-103">(Optional) Verify PIN policy settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c8c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c8c1-104">

<span> </span></span></span>

<span data-ttu-id="9c8c1-105">_**Тема последнего изменения:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="9c8c1-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="9c8c1-106">Пользователи Lync Server 2013, у которых есть учетные данные доменных служб Active Directory, могут ввести персональный идентификационный номер (ПИН-код), чтобы присоединиться к конференциям в качестве зарегистрированных пользователей.</span><span class="sxs-lookup"><span data-stu-id="9c8c1-106">Lync Server 2013 users who have Active Directory Domain Services credentials can enter a personal identification number (PIN) to join dial-in conferences as authenticated users.</span></span> <span data-ttu-id="9c8c1-107">Политика ПИН-кода определяет правила работы контактов конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="9c8c1-107">A PIN policy defines the rules for how dial-in conferencing PINs work.</span></span>

<span data-ttu-id="9c8c1-108">Если вы развертываете Конференц-связь с телефонным подключением, убедитесь, что в соответствии с вашими требованиями соответствует политика глобального ПИН-кода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c8c1-108">When you deploy dial-in conferencing, you should verify that the default global PIN policy meets your requirements.</span></span> <span data-ttu-id="9c8c1-109">Если вам нужно внести изменения, вы можете изменить глобальную политику по умолчанию или создать новую политику ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="9c8c1-109">If you need to make changes, you can modify the default global policy or you can create a new PIN policy.</span></span> <span data-ttu-id="9c8c1-110">Вы можете создавать политики закрепления, которые применяются к определенному сайту, определенному пользователю или определенной группе пользователей.</span><span class="sxs-lookup"><span data-stu-id="9c8c1-110">You can create PIN policies that apply to a specific site, a specific user, or a specific group of users.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9c8c1-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="9c8c1-111">In This Section</span></span>

  - [<span data-ttu-id="9c8c1-112">Изменение параметров ПИН-кодов по умолчанию для конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c8c1-112">Modify the default dial-in conferencing PIN settings in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-dial-in-conferencing-pin-settings.md)

  - [<span data-ttu-id="9c8c1-113">оздание или изменение параметров ПИН-кода для конференц-связи с телефонным подключением в Lync Server 2013 для сайта или группы пользователей</span><span class="sxs-lookup"><span data-stu-id="9c8c1-113">Create or modify dial-in conferencing PIN settings in Lync Server 2013 for a site or group of users</span></span>](lync-server-2013-create-or-modify-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

<span data-ttu-id="9c8c1-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c8c1-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

