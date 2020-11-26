---
title: 'Lync Server 2013: правила обновления устройств'
description: 'Lync Server 2013: правила обновления устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update rules
ms:assetid: a2f7e293-3342-4566-9605-410cb95f3b3b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994062(v=OCS.15)
ms:contentKeyID: 51803973
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd6d34c290f4a08f67143294fcc5dd18e1acf9d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429376"
---
# <a name="device-update-rules-in-lync-server-2013"></a><span data-ttu-id="c376b-103">Правила обновления устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c376b-103">Device Update rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c376b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c376b-104">

<span> </span></span></span>

<span data-ttu-id="c376b-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="c376b-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="c376b-106">Периодически Корпорация Майкрософт выпускает новый набор обновлений встроенного по устройства для Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="c376b-106">Periodically, Microsoft releases a new set of device firmware updates for Lync Phone Edition.</span></span> <span data-ttu-id="c376b-107">*Правила обновления устройства* связывают обновления встроенного по с аппаратными устройствами (телефоны и другие устройства, на которых работает Lync Phone Edition).</span><span class="sxs-lookup"><span data-stu-id="c376b-107">*Device update rules* associate firmware updates with hardware devices—phones and other devices running Lync Phone Edition.</span></span>

<span data-ttu-id="c376b-108">Чтобы получить последний набор правил обновления устройства, перейдите на страницу справки и поддержки на веб-сайте Майкрософт и выполните поиск по слову "Phone Edition".</span><span class="sxs-lookup"><span data-stu-id="c376b-108">To get the latest set of device update rules, go to the Help and Support page on the Microsoft website, and search for "Phone Edition."</span></span> <span data-ttu-id="c376b-109">Загрузите пакет обновления и извлеките файлы в папку на компьютере, куда нужно отправить обновления.</span><span class="sxs-lookup"><span data-stu-id="c376b-109">Download the update package, and extract the files to a folder on the computer where the updates are to be uploaded.</span></span> <span data-ttu-id="c376b-110">После того как файлы будут извлечены, импортируйте правила обновления устройств, найденные в извлеченном файле. CAB-файл с именем UCUpdates.cab).</span><span class="sxs-lookup"><span data-stu-id="c376b-110">After the files have been extracted, import the device update rules found in the extracted .CAB file (which have the name UCUpdates.cab).</span></span> <span data-ttu-id="c376b-111">Затем с помощью панели управления Lync Server или командлетов Windows PowerShell просмотрите эти правила для устройств организации и управляйте ими.</span><span class="sxs-lookup"><span data-stu-id="c376b-111">Then, use the Lync Server Control Panel or Windows PowerShell cmdlets to view and manage these rules for your organization’s devices.</span></span>

<span data-ttu-id="c376b-112">В следующих разделах объясняется, как импортировать, просматривать правила обновления устройств и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="c376b-112">The following topics tell you how to import, view, and manage device update rules.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c376b-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="c376b-113">In This Section</span></span>

  - [<span data-ttu-id="c376b-114">Просмотр сведений о правилах обновления устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c376b-114">View information about Device Update rules in Lync Server 2013</span></span>](lync-server-2013-view-information-about-device-update-rules.md)

  - [<span data-ttu-id="c376b-115">Импорт правил обновления устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c376b-115">Import Device Update rules in Lync Server 2013</span></span>](lync-server-2013-import-device-update-rules.md)

  - [<span data-ttu-id="c376b-116">Утверждение правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c376b-116">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)

  - [<span data-ttu-id="c376b-117">Удаление правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c376b-117">Remove a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-remove-a-device-update-rule.md)

  - [<span data-ttu-id="c376b-118">Сброс правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c376b-118">Reset a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-reset-a-device-update-rule.md)

  - [<span data-ttu-id="c376b-119">Восстановление правила обновления устройства в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c376b-119">Restore a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-restore-a-device-update-rule.md)

<span data-ttu-id="c376b-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c376b-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

