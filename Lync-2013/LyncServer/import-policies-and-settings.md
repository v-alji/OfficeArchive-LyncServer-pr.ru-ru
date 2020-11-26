---
title: Импорт политик и параметров
description: Импорт политик и параметров.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Import policies and settings
ms:assetid: b25decee-2ee5-4836-b370-454411d39252
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205178(v=OCS.15)
ms:contentKeyID: 48185147
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e014b7e8f0498742104118eec9eb313394ae6a94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439606"
---
# <a name="import-policies-and-settings"></a><span data-ttu-id="b0ab2-103">Импорт политик и параметров</span><span class="sxs-lookup"><span data-stu-id="b0ab2-103">Import policies and settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0ab2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0ab2-104">

<span> </span></span></span>

<span data-ttu-id="b0ab2-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b0ab2-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b0ab2-106">После того как вы объедините информацию о топологии Office Communications Server 2007 R2 с помощью административного пула Lync Server 2013, вам необходимо запустить командлет командной консоли Lync Server 2013, чтобы перенести политики и параметры конфигурации Office Communications Server 2007 R2 в пул Lync Server 2013 для пилотного пула.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-106">After you merge your Office Communications Server 2007 R2 topology information with your Lync Server 2013 pilot pool, you need to run a Lync Server 2013 Management Shell cmdlet to migrate your Office Communications Server 2007 R2 policies and configuration settings to your Lync Server 2013 pilot pool.</span></span>

<span data-ttu-id="b0ab2-107">Командлет **Import-CsLegacyConfiguration** импортирует политики, маршруты голосовой связи, абонентские группы, URL-адреса Communicator Web Access и номера доступа для телефонного подключения в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-107">The **Import-CsLegacyConfiguration** cmdlet imports policies, voice routes, dial plans, Communicator Web Access URLs, and dial-in access numbers to Lync Server 2013.</span></span>

<div>

## <a name="to-migrate-policies-and-settings"></a><span data-ttu-id="b0ab2-108">Миграция политик и параметров</span><span class="sxs-lookup"><span data-stu-id="b0ab2-108">To migrate policies and settings</span></span>

1.  <span data-ttu-id="b0ab2-109">На сервере переднего плана Lync Server 2013 запустите командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-109">On the Lync Server 2013 Front End server, start the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="b0ab2-110">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b0ab2-110">At the command line, type the following:</span></span>
    
        Import-CsLegacyConfiguration
    
    <span data-ttu-id="b0ab2-111">После импорта политик воспользуйтесь приведенными ниже инструкциями, чтобы просмотреть импортированные политики на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-111">After the policies are imported, use the procedure that follows to see the imported policies in the Lync Server Control Panel .</span></span>

</div>

<div>

## <a name="to-view-imported-policies"></a><span data-ttu-id="b0ab2-112">Просмотр импортированных политик</span><span class="sxs-lookup"><span data-stu-id="b0ab2-112">To view imported policies</span></span>

1.  <span data-ttu-id="b0ab2-113">Откройте панель управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-113">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="b0ab2-114">Нажмите кнопку **Маршрутизация голоса** и просмотрите импортированные политики.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-114">Click **Voice Routing** and view the imported policies.</span></span>

3.  <span data-ttu-id="b0ab2-115">Выберите **Конференц** -связь и просмотрите импортированные политики.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-115">Click **Conferencing** and view the imported policies.</span></span>

4.  <span data-ttu-id="b0ab2-116">Выберите пункт **Федерация и внешний доступ** и просмотрите импортированные политики.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-116">Click **Federation and External Access** and view the imported policies.</span></span>

5.  <span data-ttu-id="b0ab2-117">Нажмите кнопку **мониторинг и архивация** и просмотрите импортированные политики.</span><span class="sxs-lookup"><span data-stu-id="b0ab2-117">Click **Monitoring and Archiving** and view the imported policies.</span></span>

<span data-ttu-id="b0ab2-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0ab2-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

