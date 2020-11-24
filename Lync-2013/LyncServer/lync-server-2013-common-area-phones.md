---
title: 'Lync Server 2013: общие телефоны с областями'
description: 'Lync Server 2013: общие телефоны с областями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Common area phones
ms:assetid: d63bb3de-154e-4347-9251-9fa94e7d593a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994076(v=OCS.15)
ms:contentKeyID: 51803987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af8a68f875bba1d43a91e5a252259841d7a6bbda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400072"
---
# <a name="common-area-phones-in-lync-server-2013"></a><span data-ttu-id="02d09-103">Общие Телефоны на мобильных телефонах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02d09-103">Common area phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02d09-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02d09-104">

<span> </span></span></span>

<span data-ttu-id="02d09-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="02d09-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="02d09-106">Обычные телефоны — это IP-телефоны, не связанные с конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="02d09-106">Common area phones are IP phones that are not associated with an individual user.</span></span> <span data-ttu-id="02d09-107">Вместо того чтобы находились в офисе другого пользователя, обычно они размещаются в здании приемных, cafeterias, мягких для сотрудников, комнатах собраний и в других местах, где часто может быть собрано большое количество людей.</span><span class="sxs-lookup"><span data-stu-id="02d09-107">Instead of being located in someone’s office, common area phones are typically located in building lobbies, cafeterias, employee lounges, meeting rooms, and other locations where a large number of people are likely to gather.</span></span> <span data-ttu-id="02d09-108">В отличие от других телефонов в Lync Server, обычно использующих политики голосовой связи и абонентские группы, которым назначены индивидуальные пользователи, для них не могут быть назначены индивидуальные пользователи.</span><span class="sxs-lookup"><span data-stu-id="02d09-108">Unlike other phones in Lync Server, which are typically maintained by using voice policies and dial plans that are assigned to individual users, common area phones do not have individual users assigned to them.</span></span> <span data-ttu-id="02d09-109">Это означает, что они должны управляться иначе, чем ваши другие телефоны.</span><span class="sxs-lookup"><span data-stu-id="02d09-109">This means that they must be managed differently than your other phones.</span></span>

<span data-ttu-id="02d09-110">Чтобы управлять стандартными телефонами, вы создаете объекты контактов доменных служб Active Directory для всех распространенных телефонов, например для учетных записей пользователей, могут назначаться политики и голосовые планы.</span><span class="sxs-lookup"><span data-stu-id="02d09-110">To manage common area phones, you create Active Directory Domain Services contact objects for all your common area phones that, like user accounts, can be assigned policies and voice plans.</span></span> <span data-ttu-id="02d09-111">Этот подход позволяет поддерживать контроль над распространенными телефонами, даже если они не связаны с конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="02d09-111">This approach enables you to maintain control over common area phones, even though those phones are not associated with an individual user.</span></span>

<span data-ttu-id="02d09-112">В этом разделе приведены сведения о том, как создавать объекты контактов для обычных телефонов, изменять и удалять их, а также настраивать и просматривать сведения о конфигурации для телефонной сети, используемой в развертывании.</span><span class="sxs-lookup"><span data-stu-id="02d09-112">Use the topics in this section to learn how to create contact objects for common area phones, modify and delete them, and configure and view configuration information about the common area phones in your deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="02d09-113">У вас есть три варианта для стационарных телефонов: Aastra 6721ip Common Area Phone, телефонный номер HP 4110 IP и Polycom CX500 IP на стандартном телефоне.</span><span class="sxs-lookup"><span data-stu-id="02d09-113">You have three options for common area phones: the Aastra 6721ip common area phone, the HP 4110 IP Phone, and the Polycom CX500 IP common area phone.</span></span> <span data-ttu-id="02d09-114">Телефон конференц-связи по Polycom CX3000 является другим вариантом универсального телефона.</span><span class="sxs-lookup"><span data-stu-id="02d09-114">The Polycom CX3000 IP conferencing phone is another variant common area phone.</span></span> <span data-ttu-id="02d09-115">Однако она предназначена для использования в конференц-залах.</span><span class="sxs-lookup"><span data-stu-id="02d09-115">However, it is intended for use in conference rooms.</span></span> <span data-ttu-id="02d09-116">Подробнее об общих телефонах с областями можно узнать в разделе телефоны в области " <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">Выбор новых устройств</A>".</span><span class="sxs-lookup"><span data-stu-id="02d09-116">For details about common area phones, see the Common Area Phones section of <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">Choosing New Devices</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="02d09-117">Содержание</span><span class="sxs-lookup"><span data-stu-id="02d09-117">In This Section</span></span>

  - [<span data-ttu-id="02d09-118">Просмотр сведений о стандартном телефоне в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02d09-118">View common area phone information in Lync Server 2013</span></span>](lync-server-2013-view-common-area-phone-information.md)

  - [<span data-ttu-id="02d09-119">Создание или изменение объекта контактного телефона для общего города в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02d09-119">Create or modify a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="02d09-120">Включение и отключение функции поддержки горячей замены в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02d09-120">Enable or disable hot desking in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-hot-desking.md)

  - [<span data-ttu-id="02d09-121">Удаление объекта контактного телефона из общей области в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02d09-121">Delete a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-delete-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="02d09-122">Назначение политик в Lync Server 2013 на стандартном телефоне</span><span class="sxs-lookup"><span data-stu-id="02d09-122">Assign policies in Lync Server 2013 to a common area phone</span></span>](lync-server-2013-assign-policies-to-a-common-area-phone.md)

<span data-ttu-id="02d09-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02d09-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

