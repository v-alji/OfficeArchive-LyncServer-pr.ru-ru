---
title: 'Lync Server 2013: публикация базы данных расположения'
description: 'Lync Server 2013: опубликуйте базу данных местоположений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26892429c7bf5fd9cbfebd0d7ac62482767a541e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399055"
---
# <a name="publish-the-location-database-from-lync-server-2013"></a><span data-ttu-id="fd50d-103">Публикация базы данных местоположений из Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd50d-103">Publish the location database from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd50d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd50d-104">

<span> </span></span></span>

<span data-ttu-id="fd50d-105">_**Тема последнего изменения:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="fd50d-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="fd50d-106">Новые расположения, добавленные вами в базу данных местоположений, останутся недоступны клиенту, пока не будут опубликованы.</span><span class="sxs-lookup"><span data-stu-id="fd50d-106">The new locations that you added to the location database will not be made available to the client until they have been published.</span></span>

<span data-ttu-id="fd50d-107">Подробности можно найти в документации по оболочке управления Lync Server для следующего командлета:</span><span class="sxs-lookup"><span data-stu-id="fd50d-107">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="fd50d-108">**Publish-CsLisConfiguration**</span><span class="sxs-lookup"><span data-stu-id="fd50d-108">**Publish-CsLisConfiguration**</span></span>

<span data-ttu-id="fd50d-109">Если вы используете шлюзы ELIN, необходимо также загрузить номера ELIN в базу данных автоматического определения расположения (ALI) сети ТСОП.</span><span class="sxs-lookup"><span data-stu-id="fd50d-109">If you use Emergency Location Identification Number (ELIN) gateways, you also need to upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span> <span data-ttu-id="fd50d-110">Оператор ТСОП может потребовать использования определенного формата для записей ELIN.</span><span class="sxs-lookup"><span data-stu-id="fd50d-110">Your PSTN carrier may require you to use a specific format for the ELIN records.</span></span> <span data-ttu-id="fd50d-111">Обратитесь к оператору ТСОП для получения более подробных сведений.</span><span class="sxs-lookup"><span data-stu-id="fd50d-111">Contact your PSTN carrier for details.</span></span> <span data-ttu-id="fd50d-112">Вы можете экспортировать записи из базы данных службы сведений о расположении и отформатировать их в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="fd50d-112">You can export the records from the Location Information service database and format them as required.</span></span>

<div>

## <a name="to-publish-the-location-database"></a><span data-ttu-id="fd50d-113">Публикация базы данных местоположений</span><span class="sxs-lookup"><span data-stu-id="fd50d-113">To publish the location database</span></span>

  - <span data-ttu-id="fd50d-114">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="fd50d-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

  - <span data-ttu-id="fd50d-115">Чтобы опубликовать базу данных местоположений, выполните следующий командлет.</span><span class="sxs-lookup"><span data-stu-id="fd50d-115">Run the following cmdlet to publish the location database.</span></span>
    
        Publish-CsLisConfiguration

<span data-ttu-id="fd50d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd50d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

