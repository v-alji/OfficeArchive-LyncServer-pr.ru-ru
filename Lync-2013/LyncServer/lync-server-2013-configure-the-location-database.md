---
title: 'Lync Server 2013: Настройка базы данных местоположений'
description: 'Lync Server 2013: Настройка базы данных местоположений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the location database
ms:assetid: 8544be31-6958-47ef-b926-fdc80d56191c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398679(v=OCS.15)
ms:contentKeyID: 48184704
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 877c83976ca0db9abc3a9e57d4a1cf5adaa1291a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433614"
---
# <a name="configure-the-location-database-in-lync-server-2013"></a><span data-ttu-id="476c9-103">Configure the location database in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="476c9-103">Configure the location database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="476c9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="476c9-104">

<span> </span></span></span>

<span data-ttu-id="476c9-105">_**Тема последнего изменения:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="476c9-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="476c9-106">Чтобы включить автоматическое определение клиентами своего местоположения в сети, сначала необходимо настроить базу данных местоположений.</span><span class="sxs-lookup"><span data-stu-id="476c9-106">To enable clients to automatically detect their location within a network, you first need to configure the location database.</span></span> <span data-ttu-id="476c9-107">Если вы не настраиваете базу данных местоположений и для **расположения, требуемого** в политике расположения, задано значение **Да** или **отказ**, пользователю будет предложено ввести расположение вручную.</span><span class="sxs-lookup"><span data-stu-id="476c9-107">If you do not configure a location database, and **Location Required** in the location policy is set to **Yes** or **Disclaimer**, the user will be prompted to manually enter a location.</span></span>

<span data-ttu-id="476c9-108">Чтобы настроить базу данных местоположений, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="476c9-108">To configure the location database, you will perform the following tasks:</span></span>

1.  <span data-ttu-id="476c9-109">Заполните базу данных с сопоставлением сетевых элементов местоположениям.</span><span class="sxs-lookup"><span data-stu-id="476c9-109">Populate the database with a mapping of network elements to locations.</span></span> <span data-ttu-id="476c9-110">При использовании шлюза идентификационный номер места для экстренного реагирования (ELIN) необходимо включить в поле ELIN \<CompanyName\> .</span><span class="sxs-lookup"><span data-stu-id="476c9-110">If you use an Emergency Location Identification Number (ELIN) gateway, you need to include the ELIN in the \<CompanyName\> field.</span></span>

2.  <span data-ttu-id="476c9-111">Поверьте адрес по руководству MSAG, которое поддерживается поставщиком услуг E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="476c9-111">Validate the addresses against the master street address guide (MSAG) that is maintained by the E9-1-1 service provider.</span></span>

3.  <span data-ttu-id="476c9-112">Опубликуйте обновленную базу данных.</span><span class="sxs-lookup"><span data-stu-id="476c9-112">Publish the updated database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="476c9-113">Кроме того, вы можете определить вспомогательную базу данных расположения, которую можно использовать при размещении базы данных местоположений.</span><span class="sxs-lookup"><span data-stu-id="476c9-113">Alternately, you can define a secondary location source database that can be used in placed of the location database.</span></span> <span data-ttu-id="476c9-114">Подробности можно найти <A href="lync-server-2013-configure-a-secondary-location-information-service.md">в разделе Настройка дополнительной службы сведений о расположении в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="476c9-114">For details, see <A href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="476c9-115">Содержание</span><span class="sxs-lookup"><span data-stu-id="476c9-115">In This Section</span></span>

  - [<span data-ttu-id="476c9-116">Заполнение базы данных местоположений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="476c9-116">Populate the location database in Lync Server 2013</span></span>](lync-server-2013-populate-the-location-database.md)

  - [<span data-ttu-id="476c9-117">Проверка адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="476c9-117">Validate addresses in Lync Server 2013</span></span>](lync-server-2013-validate-addresses.md)

  - [<span data-ttu-id="476c9-118">Публикация базы данных местоположений из Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="476c9-118">Publish the location database from Lync Server 2013</span></span>](lync-server-2013-publish-the-location-database.md)

<span data-ttu-id="476c9-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="476c9-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

