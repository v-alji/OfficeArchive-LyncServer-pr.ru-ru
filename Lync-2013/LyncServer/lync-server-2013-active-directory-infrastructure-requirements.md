---
title: 'Lync Server 2013: требования к инфраструктуре Active Directory'
description: 'Lync Server 2013: требования инфраструктуры Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory infrastructure requirements
ms:assetid: c2086f7b-662f-4179-ab99-2c0311ebd903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412955(v=OCS.15)
ms:contentKeyID: 48185318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62218605c9b3fac20743d0b6bb475515c9498f9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439417"
---
# <a name="active-directory-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="b349e-103">Требования к инфраструктуре Active Directory для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b349e-103">Active Directory infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b349e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b349e-104">

<span> </span></span></span>

<span data-ttu-id="b349e-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="b349e-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="b349e-106">Прежде чем приступить к подготовке доменных служб Active Directory для Lync Server 2013, убедитесь, что инфраструктура Active Directory удовлетворяет следующим требованиям:</span><span class="sxs-lookup"><span data-stu-id="b349e-106">Before you start the process of preparing Active Directory Domain Services for Lync Server 2013, make sure that your Active Directory infrastructure meets the following prerequisites:</span></span>

  - <span data-ttu-id="b349e-107">Все контроллеры домена (включая все серверы глобального каталога) в лесу, где развертывается сервер Lync Server, работают под управлением одной из следующих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="b349e-107">All domain controllers (which include all global catalog servers) in the forest where you deploy Lync Server run one of the following operating systems:</span></span>
    
      - <span data-ttu-id="b349e-108">Операционная система Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b349e-108">Windows Server 2012 R2 operating system</span></span>
    
      - <span data-ttu-id="b349e-109">Операционная система Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b349e-109">Windows Server 2012 operating system</span></span>
    
      - <span data-ttu-id="b349e-110">Операционная система Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b349e-110">Windows Server 2008 R2 operating system</span></span>
    
      - <span data-ttu-id="b349e-111">Операционная система Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b349e-111">Windows Server 2008 operating system</span></span>
    
      - <span data-ttu-id="b349e-112">Windows Server 2008 Enterprise 32-bit</span><span class="sxs-lookup"><span data-stu-id="b349e-112">Windows Server 2008 Enterprise 32-Bit</span></span>
    
      - <span data-ttu-id="b349e-113">32-разрядная или 64-разрядная версии операционной системы Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b349e-113">32-bit or 64-bit versions of the Windows Server 2003 R2 operating system</span></span>
    
      - <span data-ttu-id="b349e-114">32-разрядная или 64-разрядная версии операционной системы Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b349e-114">32-bit or 64-bit versions of the Windows Server 2003 operating system</span></span>

  - <span data-ttu-id="b349e-115">Все домены, в которых развертывается сервер Lync Server, порождаются на функциональном уровне домена Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 или не ниже Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b349e-115">All domains in which you deploy Lync Server are raised to a domain functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

  - <span data-ttu-id="b349e-116">Лес, в котором развертывается сервер Lync Server, передается на функциональный уровень леса Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 или хотя бы Windows Server 2003 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b349e-116">The forest in which you deploy Lync Server is raised to a forest functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b349e-117">Чтобы изменить функциональный уровень домена или леса, ознакомьтесь со статьей "создание функциональных уровней домена и леса" в библиотеке TechNet по адресу <A href="https://go.microsoft.com/fwlink/p/?linkid=263775">https://go.microsoft.com/fwlink/p/?LinkId=263775</A> .</span><span class="sxs-lookup"><span data-stu-id="b349e-117">To change your domain or forest functional level, see "Raising domain and forest functional levels" in the TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=263775">https://go.microsoft.com/fwlink/p/?LinkId=263775</A>.</span></span>

    
    </div>

  - <span data-ttu-id="b349e-118">Глобальный каталог разворачивается во всех доменах, где развертываются компьютеры или пользователи Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b349e-118">A global catalog is deployed in every domain where you deploy Lync Server computers or users.</span></span>

<span data-ttu-id="b349e-119">Lync Server 2013 поддерживает универсальные группы в операционных системах Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b349e-119">Lync Server 2013 supports the universal groups in the Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b349e-120">Members of universal groups can include other groups and accounts from any domain in the domain tree or forest and can be assigned permissions in any domain in the domain tree or forest.</span><span class="sxs-lookup"><span data-stu-id="b349e-120">Members of universal groups can include other groups and accounts from any domain in the domain tree or forest and can be assigned permissions in any domain in the domain tree or forest.</span></span> <span data-ttu-id="b349e-121">Поддержка универсальной группы в сочетании с делегированием администратора упрощает управление развертыванием Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b349e-121">Universal group support, combined with administrator delegation, simplifies the management of a Lync Server deployment.</span></span> <span data-ttu-id="b349e-122">For example, it is not necessary to add one domain to another to enable an administrator to manage both.</span><span class="sxs-lookup"><span data-stu-id="b349e-122">For example, it is not necessary to add one domain to another to enable an administrator to manage both.</span></span>

<span data-ttu-id="b349e-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b349e-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

