---
title: 'Lync Server 2013: настройка политик голосовой связи и записей использования ТСОП для авторизации функций звонков и предоставления привилегий'
description: 'Lync Server 2013: Настройка политик голосовой связи и использования PSTN для авторизации функций и привилегий звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring voice policies and PSTN usage records to authorize calling features and privileges
ms:assetid: 63f22010-a3d7-4cbd-86e8-6fc0e13c2b84
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398450(v=OCS.15)
ms:contentKeyID: 48184307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a12c9c64c3f02effba7c7709321eda91350ebb75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432396"
---
# <a name="configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges-in-lync-server-2013"></a><span data-ttu-id="9e517-103">Настройка политик голосовой связи и записей использования ТСОП для авторизации функций звонков и предоставления привилегий в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e517-103">Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e517-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e517-104">

<span> </span></span></span>

<span data-ttu-id="9e517-105">_**Тема последнего изменения:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="9e517-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="9e517-106">*Политика голосовой связи* включает набор функций звонка и связывает одну или несколько записей использования PSTN для определения функций звонков и разрешений пользователей, которым назначена политика.</span><span class="sxs-lookup"><span data-stu-id="9e517-106">A *voice policy* enables a set of calling features and associates one or more PSTN usage records to define the calling features and permissions of users who are assigned the policy.</span></span>

<span data-ttu-id="9e517-107">Область политики голосовой связи может быть либо *сайтом* (которая определяет возможности и разрешения по умолчанию для сайта сети), либо *пользователем* (который определяет возможности и разрешения, назначаемые для отдельных пользователей или групп).</span><span class="sxs-lookup"><span data-stu-id="9e517-107">Voice policy scope can be either *Site* (which defines the default features and permissions for a network site) or *User* (which defines the features and permissions to be assigned on a per-user or group basis).</span></span> <span data-ttu-id="9e517-108">Пользователям, которым не назначена политика голосовой связи, будет автоматически назначаться Глобальная политика, которая является политикой голосовой связи по умолчанию, установленной вместе с продуктом.</span><span class="sxs-lookup"><span data-stu-id="9e517-108">Users not assigned to a voice policy will automatically be assigned to the global policy, which is the default voice policy that is installed with the product.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9e517-109">Подробные сведения можно найти <A href="lync-server-2013-voice-policies.md">в разделе политики голосовой связи в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="9e517-109">For details, see <A href="lync-server-2013-voice-policies.md">Voice policies in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9e517-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="9e517-110">In This Section</span></span>

  - [<span data-ttu-id="9e517-111">Создание политики голосовой связи и настройка записей об использовании PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e517-111">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="9e517-112">Изменение политики голосовой связи и настройка записей использования PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e517-112">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="9e517-113">Настройка escape-последовательности голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e517-113">Configuring voice mail escape in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-mail-escape.md)

<span data-ttu-id="9e517-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e517-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

