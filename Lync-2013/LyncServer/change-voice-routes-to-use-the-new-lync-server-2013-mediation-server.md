---
title: Изменение маршрутов голосовой связи для использования нового сервера исправлений Lync Server 2013
description: Изменение маршрутов голосовой связи для использования нового сервера исправлений Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change voice routes to use the new Lync Server 2013 Mediation Server
ms:assetid: acd487b3-377c-46bf-9f71-fe6152002664
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205162(v=OCS.15)
ms:contentKeyID: 48185069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef58ba61512b5de31a74b79e554dbb3f94b67d99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398584"
---
# <a name="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server"></a><span data-ttu-id="c2230-103">Изменение маршрутов голосовой связи для использования нового сервера исправлений Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2230-103">Change voice routes to use the new Lync Server 2013 Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2230-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2230-104">

<span> </span></span></span>

<span data-ttu-id="c2230-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="c2230-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="c2230-106">Эта процедура изменяет маршруты голосовой связи на использование сервера обновлений Lync Server 2013 вместо устаревшего сервера Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c2230-106">This procedure changes the voice routes to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<div>

## <a name="to-change-the-voice-routes-to-use-the-new-mediation-server"></a><span data-ttu-id="c2230-107">Изменение голосовых маршрутов для использования нового сервера обновлений</span><span class="sxs-lookup"><span data-stu-id="c2230-107">To change the voice routes to use the new Mediation Server</span></span>

1.  <span data-ttu-id="c2230-108">управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2230-108">Lync Server 2013 Control Panel</span></span>

2.  <span data-ttu-id="c2230-109">На левой панели выберите пункт **Маршрутизация голоса** и щелкните **маршрут**.</span><span class="sxs-lookup"><span data-stu-id="c2230-109">In the left pane, select **Voice Routing** and then **Route**.</span></span>

3.  <span data-ttu-id="c2230-110">Нажмите кнопку **создать** , чтобы создать новый голосовой маршрут.</span><span class="sxs-lookup"><span data-stu-id="c2230-110">Click **New** to create a New Voice Route.</span></span>

4.  <span data-ttu-id="c2230-111">Заполните следующие поля:</span><span class="sxs-lookup"><span data-stu-id="c2230-111">Fill in the following fields:</span></span>
    
      - <span data-ttu-id="c2230-112">**Name (имя**): введите описательное имя маршрута голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="c2230-112">**Name**: Type a descriptive name of the voice route.</span></span> <span data-ttu-id="c2230-113">Для этого документа мы будем использовать **W15PSTNRoute**.</span><span class="sxs-lookup"><span data-stu-id="c2230-113">For this document we will use **W15PSTNRoute**.</span></span>
    
      - <span data-ttu-id="c2230-114">**Описание**: введите краткое описание голосового маршрута.</span><span class="sxs-lookup"><span data-stu-id="c2230-114">**Description**: Type a short description of the voice route.</span></span>

5.  <span data-ttu-id="c2230-115">Пропускать все оставшиеся разделы, пока не дойдете до **соответствующих шлюзов**.</span><span class="sxs-lookup"><span data-stu-id="c2230-115">Skip all remaining sections until you reach **Associated gateways**.</span></span> <span data-ttu-id="c2230-116">Нажмите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c2230-116">Click **Add**.</span></span> <span data-ttu-id="c2230-117">Выберите новый шлюз по умолчанию и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2230-117">Select the new default gateway and click **OK**.</span></span>

6.  <span data-ttu-id="c2230-118">В разделе **связанные использование PSTN** нажмите кнопку **выбрать**.</span><span class="sxs-lookup"><span data-stu-id="c2230-118">Under **Associated PSTN Usages**, click **Select**.</span></span>

7.  <span data-ttu-id="c2230-119">На странице **Выбор записи по использованию PSTN** выберите имя записи и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2230-119">From the **Select PSTN Usage Record** page, select a record name and then click **OK**.</span></span>

8.  <span data-ttu-id="c2230-120">На странице **Новый голосовой маршрут** нажмите кнопку **ОК** , чтобы создать **голосовой маршрут**.</span><span class="sxs-lookup"><span data-stu-id="c2230-120">From the **New Voice Route** page, click **OK** to create the **Voice Route**.</span></span>

9.  <span data-ttu-id="c2230-121">На странице **Маршрутизация голоса** нажмите кнопку **маршрут**.</span><span class="sxs-lookup"><span data-stu-id="c2230-121">From the **Voice Routing** page, select **Route**.</span></span>

10. <span data-ttu-id="c2230-122">Переместите созданный маршрут в верхнюю часть списка и нажмите кнопку **Commit (сохранить**).</span><span class="sxs-lookup"><span data-stu-id="c2230-122">Move the newly created route to the top of the list and then select **Commit**.</span></span>

<span data-ttu-id="c2230-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2230-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

