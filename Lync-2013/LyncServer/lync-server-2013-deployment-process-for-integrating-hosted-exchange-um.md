---
title: 'Lync Server 2013: процесс развертывания для интеграции размещенной единой системы обмена сообщениями Exchange'
description: 'Lync Server 2013: процесс развертывания для интеграции размещенной единой системы обмена сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for integrating hosted Exchange UM with Lync Server
ms:assetid: dbec9c38-7f66-419d-b8c3-c61380052cac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398968(v=OCS.15)
ms:contentKeyID: 48185586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 83239c6534dfdaa65109c8880cc4cb4946bffab6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429680"
---
# <a name="deployment-process-for-integrating-hosted-exchange-um-with-lync-server-2013"></a><span data-ttu-id="c966d-103">Процесс развертывания для интеграции размещенной единой системы обмена сообщениями Exchange с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c966d-103">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c966d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c966d-104">

<span> </span></span></span>

<span data-ttu-id="c966d-105">_**Тема последнего изменения:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="c966d-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="c966d-106">Для эффективного планирования интеграции Lync Server 2013 с размещенной единой системой обмена сообщениями Exchange необходимо учитывать следующее:</span><span class="sxs-lookup"><span data-stu-id="c966d-106">Effective planning for integrating Lync Server 2013 with hosted Exchange Unified Messaging (UM) requires that you take into account the following:</span></span>

  - <span data-ttu-id="c966d-107">Предварительные требования для интеграции Lync Server 2013 с размещенной единой системой обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="c966d-107">Prerequisites for integrating Lync Server 2013 with hosted Exchange UM</span></span>

  - <span data-ttu-id="c966d-108">Шаги, необходимые для процесса интеграции</span><span class="sxs-lookup"><span data-stu-id="c966d-108">Steps required during the integration process</span></span>

<div>

## <a name="deployment-prerequisites-for-integrating-with-hosted-exchange-um"></a><span data-ttu-id="c966d-109">Требования к развертыванию для интеграции с размещенной единой системой обмена сообщениями Exchange</span><span class="sxs-lookup"><span data-stu-id="c966d-109">Deployment Prerequisites for Integrating with Hosted Exchange UM</span></span>

<span data-ttu-id="c966d-110">Прежде чем начать процесс интеграции, необходимо предварительно развернуть Lync Server 2013 (как минимум, пул переднего плана или сервер Standard Edition), пограничный сервер, а также клиенты Lync 2013 или Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="c966d-110">Before you can begin the integration process, you must already have deployed Lync Server 2013 (at a minimum, a Front End pool or a Standard Edition server), an Edge Server, and Lync 2013 or Lync 2010 clients.</span></span>

</div>

<div>

## <a name="integration-process"></a><span data-ttu-id="c966d-111">Процесс интеграции</span><span class="sxs-lookup"><span data-stu-id="c966d-111">Integration Process</span></span>

<span data-ttu-id="c966d-112">В следующей таблице представлены общие сведения о размещенном процессе интеграции Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="c966d-112">The following table provides an overview of the hosted Exchange UM integration process.</span></span> <span data-ttu-id="c966d-113">Дополнительные сведения о действиях по развертыванию можно найти в статье [предоставление пользователям Lync Server 2013 голосовой почты в размещенной единой системе обмена сообщениями Exchange](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="c966d-113">For details about deployment steps, see [Providing Lync Server 2013 users voice mail on hosted Exchange UM](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c966d-114">Этап</span><span class="sxs-lookup"><span data-stu-id="c966d-114">Phase</span></span></th>
<th><span data-ttu-id="c966d-115">Шаги</span><span class="sxs-lookup"><span data-stu-id="c966d-115">Steps</span></span></th>
<th><span data-ttu-id="c966d-116">Права и разрешения</span><span class="sxs-lookup"><span data-stu-id="c966d-116">Rights and permissions</span></span></th>
<th><span data-ttu-id="c966d-117">Документация по развертыванию</span><span class="sxs-lookup"><span data-stu-id="c966d-117">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c966d-118">Настройте пограничный сервер.</span><span class="sxs-lookup"><span data-stu-id="c966d-118">Configure the Edge Server.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="c966d-119">Настроить пограничный сервер для федерации.</span><span class="sxs-lookup"><span data-stu-id="c966d-119">Configure the Edge Server for federation.</span></span></p></li>
<li><p><span data-ttu-id="c966d-120">Ручная репликация данных на пограничный сервер.</span><span class="sxs-lookup"><span data-stu-id="c966d-120">Manually replicate data to the Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="c966d-121">Настройте поставщика услуг размещения на пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="c966d-121">Configure the hosting provider on the Edge Server.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="c966d-122">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="c966d-122">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="c966d-123"><a href="lync-server-2013-configure-the-edge-server-for-integration-with-hosted-exchange-um.md">Настройка пограничного сервера для интеграции с размещенной единой системой обмена сообщениями Exchange</a></span><span class="sxs-lookup"><span data-stu-id="c966d-123"><a href="lync-server-2013-configure-the-edge-server-for-integration-with-hosted-exchange-um.md">Configure the Edge Server for integration with hosted Exchange UM</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c966d-124">Настройка политики размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="c966d-124">Configure hosted voice mail policy.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="c966d-125">Либо измените политику глобальной размещенной голосовой почты, либо создайте новую политику размещенной голосовой почты с помощью сайта или Per-User области.</span><span class="sxs-lookup"><span data-stu-id="c966d-125">Either modify the global hosted voice mail policy or create a new hosted voice mail policy with Site or Per-User scope.</span></span></p></li>
<li><p><span data-ttu-id="c966d-126">Для политик с областью Per-User назначьте политику пользователям или группам.</span><span class="sxs-lookup"><span data-stu-id="c966d-126">For policies with Per-User scope, assign the policy to users or groups.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="c966d-127">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="c966d-127">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="c966d-128"><a href="lync-server-2013-manage-hosted-voice-mail-policies.md">Управление политиками размещенной голосовой почты в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c966d-128"><a href="lync-server-2013-manage-hosted-voice-mail-policies.md">Manage hosted voice mail policies in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c966d-129">Включите пользователей для размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="c966d-129">Enable users for hosted voice mail.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c966d-130">Настройте учетные записи пользователей, чьи почтовые ящики находятся в размещенной службе Exchange.</span><span class="sxs-lookup"><span data-stu-id="c966d-130">Configure user accounts for users whose mailboxes are on a hosted Exchange service.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c966d-131">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c966d-131">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c966d-132"><a href="lync-server-2013-enable-users-for-hosted-voice-mail.md">Включение поддержки размещаемой голосовой почты для пользователей в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c966d-132"><a href="lync-server-2013-enable-users-for-hosted-voice-mail.md">Enable users for hosted voice mail in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c966d-133">Настройка объектов размещенных контактов.</span><span class="sxs-lookup"><span data-stu-id="c966d-133">Configure hosted contact objects.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="c966d-134">Создание объектов контактов для автоматического ассистента для размещенной единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c966d-134">Create auto-attendant Contact objects for hosted Exchange UM.</span></span></p></li>
<li><p><span data-ttu-id="c966d-135">Создание объектов контактов для доступа абонента для размещенной единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c966d-135">Create Subscriber Access contact objects for hosted Exchange UM.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="c966d-136">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c966d-136">RTCUniversalUserAdmins</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="c966d-137">Чтобы создать, изменить или удалить объекты контакта, пользователь, который запускает командлет New-CsExUmContact, Set-CsExUmContact или Remove-CsExUmContact, должен иметь соответствующее разрешение на доступ к организационному подразделению Active Directory, в котором хранятся новые объекты контакта.</span><span class="sxs-lookup"><span data-stu-id="c966d-137">To create, modify or remove contact objects, the user who runs the New-CsExUmContact, Set-CsExUmContact or Remove-CsExUmContact cmdlet must have the correct permission to the Active Directory organizational unit where the new contact objects are stored.</span></span> <span data-ttu-id="c966d-138">This permission can be granted by running the Grant-CsOUPermission cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c966d-138">This permission can be granted by running the Grant-CsOUPermission cmdlet.</span></span> <span data-ttu-id="c966d-139">Подробные сведения можно найти в руководстве по среде Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="c966d-139">For details, see the Lync Server Management Shell documentation.</span></span>


</div></td>
<td><p><span data-ttu-id="c966d-140"><a href="lync-server-2013-create-contact-objects-for-hosted-exchange-um.md">Создание объектов Contact для размещенной единой системы обмена сообщениями Exchange в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c966d-140"><a href="lync-server-2013-create-contact-objects-for-hosted-exchange-um.md">Create contact objects for hosted Exchange UM in Lync Server 2013</a></span></span></p></td><span data-ttu-id="c966d-141">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c966d-141">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

