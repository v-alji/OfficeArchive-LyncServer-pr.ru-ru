---
title: 'Lync Server 2013: поддержка доменных служб Active Directory'
description: 'Lync Server 2013: поддержка доменных служб Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory Domain Services support
ms:assetid: aeb62d5e-e424-473a-b795-9452150c98dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412831(v=OCS.15)
ms:contentKeyID: 48185136
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb2a85bab90557c28c4802721d4202f6188cb3f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398032"
---
# <a name="active-directory-domain-services-support-in-lync-server-2013"></a><span data-ttu-id="fb1f7-103">Поддержка доменных служб Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb1f7-103">Active Directory Domain Services support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb1f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb1f7-104">

<span> </span></span></span>

<span data-ttu-id="fb1f7-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="fb1f7-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="fb1f7-106">Lync Server 2013 использует центральное хранилище для хранения данных конфигурации для серверов и служб, вместо того чтобы полагаться на доменные службы Active Directory для этих данных, как в прошлом.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-106">Lync Server 2013 uses the Central Management store to store configuration data for servers and services, instead of relying on Active Directory Domain Services for this information, as in the past.</span></span> <span data-ttu-id="fb1f7-107">Lync Server 2013 по-прежнему хранит указанные ниже в службах AD DS.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-107">Lync Server 2013 still stores the following in AD DS:</span></span>

  - <span data-ttu-id="fb1f7-108">**Расширения схемы**</span><span class="sxs-lookup"><span data-stu-id="fb1f7-108">**Schema extensions**</span></span>
    
      - <span data-ttu-id="fb1f7-109">Расширения объекта пользователя</span><span class="sxs-lookup"><span data-stu-id="fb1f7-109">User object extensions</span></span>
    
      - <span data-ttu-id="fb1f7-110">Расширения классов для Lync Server 2010 и Office Communications Server 2007 R2 для обеспечения обратной совместимости с предыдущими поддерживаемыми версиями</span><span class="sxs-lookup"><span data-stu-id="fb1f7-110">Extensions for Lync Server 2010 and Office Communications Server 2007 R2 classes to maintain backward compatibility with previous supported versions</span></span>

  - <span data-ttu-id="fb1f7-111">**Данные** (хранящиеся в расширенной схеме Lync Server 2013 и в существующих классах)</span><span class="sxs-lookup"><span data-stu-id="fb1f7-111">**Data** (stored in Lync Server 2013 extended schema and in existing classes)</span></span>
    
      - <span data-ttu-id="fb1f7-112">URI SIP пользователя и другие пользовательские параметры</span><span class="sxs-lookup"><span data-stu-id="fb1f7-112">User SIP URI and other user settings</span></span>
    
      - <span data-ttu-id="fb1f7-113">Объекты контактов для приложений (например, приложение группы ответа и приложение для конференц-связи);</span><span class="sxs-lookup"><span data-stu-id="fb1f7-113">Contact objects for applications (for example, the Response Group application and the Conferencing Attendant application)</span></span>
    
      - <span data-ttu-id="fb1f7-114">Данные, опубликованные для обеспечения обратной совместимости</span><span class="sxs-lookup"><span data-stu-id="fb1f7-114">Data published for backward compatibility</span></span>
    
      - <span data-ttu-id="fb1f7-115">Точка управления службой для центрального хранилища управления</span><span class="sxs-lookup"><span data-stu-id="fb1f7-115">A service control point (SCP) for the Central Management store</span></span>
    
      - <span data-ttu-id="fb1f7-116">Учетная запись для проверки подлинности Kerberos (необязательный объект-компьютер)</span><span class="sxs-lookup"><span data-stu-id="fb1f7-116">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="fb1f7-117">В этом разделе описаны требования поддержки AD DS для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-117">This section describes the AD DS support requirements for Lync Server 2013.</span></span> <span data-ttu-id="fb1f7-118">Дополнительные сведения о поддержке топологии: [Поддерживаемые топологии Active Directory в Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-118">For details about topology support, see [Supported Active Directory topologies in Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) in the Supportability documentation.</span></span>

<div>

## <a name="supported-domain-controller-operating-systems"></a><span data-ttu-id="fb1f7-119">Поддерживаемые операционные системы контроллера домена</span><span class="sxs-lookup"><span data-stu-id="fb1f7-119">Supported Domain Controller Operating Systems</span></span>

<span data-ttu-id="fb1f7-120">Lync Server 2013 поддерживает контроллеры домена под управлением следующих операционных систем:</span><span class="sxs-lookup"><span data-stu-id="fb1f7-120">Lync Server 2013 supports domain controllers running the following operating systems:</span></span>

  - <span data-ttu-id="fb1f7-121">Операционная система Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fb1f7-121">Windows Server 2012 R2 operating system</span></span>

  - <span data-ttu-id="fb1f7-122">Операционная система Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb1f7-122">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="fb1f7-123">Операционная система Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb1f7-123">Windows Server 2008 R2 operating system</span></span>

  - <span data-ttu-id="fb1f7-124">Операционная система Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb1f7-124">Windows Server 2008 operating system</span></span>

  - <span data-ttu-id="fb1f7-125">Windows Server 2008 Enterprise 32-bit</span><span class="sxs-lookup"><span data-stu-id="fb1f7-125">Windows Server 2008 Enterprise 32-Bit</span></span>

  - <span data-ttu-id="fb1f7-126">Версия операционной системы Windows Server 2003 R2 (32-разрядная или 64-разрядная)</span><span class="sxs-lookup"><span data-stu-id="fb1f7-126">The 32-bit or 64-bit versions of the Window Server 2003 R2 operating system</span></span>

  - <span data-ttu-id="fb1f7-127">32-разрядная или 64-разрядная версии операционной системы Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb1f7-127">The 32-bit or 64-bit versions of the Windows Server 2003 operating system</span></span>

</div>

<div>

## <a name="forest-and-domain-functional-level"></a><span data-ttu-id="fb1f7-128">Функциональный уровень леса и домена</span><span class="sxs-lookup"><span data-stu-id="fb1f7-128">Forest and Domain Functional Level</span></span>

<span data-ttu-id="fb1f7-129">Вы должны вызвать все домены, в которых развертывается сервер Lync Server 2013, на функциональном уровне домена Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 или хотя бы Windows Server 2003 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-129">You must raise all domains in which you deploy Lync Server 2013 to a domain functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

<span data-ttu-id="fb1f7-130">Все леса, в которых развертывается Lync Server 2013, должны порождаться на функциональный уровень леса Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 или не ниже Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-130">All forests in which you deploy Lync Server 2013 must be raised to a forest functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

</div>

<div>

## <a name="support-for-read-only-domain-controllers"></a><span data-ttu-id="fb1f7-131">Поддержка Read-Only контроллеры домена</span><span class="sxs-lookup"><span data-stu-id="fb1f7-131">Support for Read-Only Domain Controllers</span></span>

<span data-ttu-id="fb1f7-132">Lync Server 2013 поддерживает развертывание доменных служб Active Directory, включающее контроллеры домена только для чтения или серверы глобального каталога только для чтения, если доступны контроллеры домена с возможностью записи.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-132">Lync Server 2013 supports Active Directory Domain Services deployments that include read-only domain controllers or read-only global catalog servers, as long as there are writable domain controllers available.</span></span>

</div>

<div>

## <a name="domain-names"></a><span data-ttu-id="fb1f7-133">Доменные имена</span><span class="sxs-lookup"><span data-stu-id="fb1f7-133">Domain Names</span></span>

<span data-ttu-id="fb1f7-134">Lync Server не поддерживает домены с одной меткой.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-134">Lync Server does not support single-labeled domains.</span></span> <span data-ttu-id="fb1f7-135">Например, лес с корневым доменом с именем **contoso. local** поддерживается, но корневой домен с именем **Local** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-135">For example, a forest with a root domain named **contoso.local** is supported, but a root domain named **local** is not supported.</span></span> <span data-ttu-id="fb1f7-136">Подробные сведения о том, как настроить Windows для доменов с DNS-именами, сопоставленными с одной меткой, можно найти в статье 300684 в Microsoft Knowledge Base [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752) .</span><span class="sxs-lookup"><span data-stu-id="fb1f7-136">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fb1f7-137">Lync Server не поддерживает переименование доменов.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-137">Lync Server does not support renaming domains.</span></span> <span data-ttu-id="fb1f7-138">Если необходимо переименовать домен, на котором развернут сервер Lync Server, сначала необходимо удалить Lync Server, затем переименовать домен, а затем повторно установить Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-138">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

</div>

<div>

## <a name="locked-down-ad-ds-environments"></a><span data-ttu-id="fb1f7-139">Заблокированные среды AD DS</span><span class="sxs-lookup"><span data-stu-id="fb1f7-139">Locked Down AD DS Environments</span></span>

<span data-ttu-id="fb1f7-140">В заблокированной среде доменных служб Active Directory пользователи и объекты компьютеров часто размещаются в определенных организационных подразделениях (OU) с отключенным наследованием разрешений для обеспечения безопасности административного делегирования и включения использования объектов групповой политики (GPO) для принудительного применения политик безопасности.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-140">In a locked-down AD DS environment, Users and Computer objects are often placed in specific organizational units (OUs) with permissions inheritance disabled to help secure administrative delegation and to enable use of Group Policy objects (GPOs) to enforce security policies.</span></span> <span data-ttu-id="fb1f7-141">Lync Server 2013 можно развертывать в заблокированной среде Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-141">Lync Server 2013 can be deployed in a locked-down Active Directory environment.</span></span> <span data-ttu-id="fb1f7-142">Сведения о том, что необходимо для развертывания Lync Server в заблокированной среде, приведены в разделе [Подготовка заблокированных доменных служб Active Directory в Lync server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="fb1f7-142">For details about what is required to deploy Lync Server in a locked-down environment, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) in the Deployment documentation.</span></span>

<span data-ttu-id="fb1f7-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb1f7-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

