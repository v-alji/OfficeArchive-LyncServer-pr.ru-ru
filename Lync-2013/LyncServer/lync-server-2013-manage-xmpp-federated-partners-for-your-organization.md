---
title: 'Lync Server 2013: управление федеративными XMPP-партнерами для организации'
description: 'Lync Server 2013: Управление XMPP федеративными партнерами для вашей организации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage XMPP federated partners for your organization
ms:assetid: 48681433-725d-457f-926b-f91d95bcf082
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552450(v=OCS.15)
ms:contentKeyID: 48679561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37d6fb4104c35ffc7db9649656f7786568a48b61
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426027"
---
# <a name="manage-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="79ebe-103">Управление федеративными XMPP-партнерами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79ebe-103">Manage XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79ebe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79ebe-104">

<span> </span></span></span>

<span data-ttu-id="79ebe-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="79ebe-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="79ebe-106">Это предварительная редакция документации и она может меняться.</span><span class="sxs-lookup"><span data-stu-id="79ebe-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="79ebe-107">Пустые разделы добавлены в качестве заполнителей.</span><span class="sxs-lookup"><span data-stu-id="79ebe-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="79ebe-108">Чтобы управлять поддержкой пользователей XMPP федеративных доменов, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="79ebe-108">To manage support for users of XMPP federated domains, you need to do the following:</span></span>

  - <span data-ttu-id="79ebe-109">Настройте одну или несколько политик внешнего доступа для поддержки пользователей XMPP федеративных доменов.</span><span class="sxs-lookup"><span data-stu-id="79ebe-109">Configure one or more external access policies to support users of XMPP federated domains.</span></span>

  - <span data-ttu-id="79ebe-110">Настройка политики конфигурации пограничного доступа для поддержки Федерации.</span><span class="sxs-lookup"><span data-stu-id="79ebe-110">Configure Access Edge Configuration policy to support federation.</span></span>

  - <span data-ttu-id="79ebe-111">Создание определений федеративных партнеров XMPP.</span><span class="sxs-lookup"><span data-stu-id="79ebe-111">Create XMPP Federated Partners definitions.</span></span>

  - <span data-ttu-id="79ebe-112">Общие сведения о параметрах согласования, доступных для Федерации XMPP.</span><span class="sxs-lookup"><span data-stu-id="79ebe-112">Understand negotiation settings available for XMPP federation.</span></span>

<span data-ttu-id="79ebe-113">Чтобы выполнить эти задачи, выполните действия, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="79ebe-113">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="79ebe-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="79ebe-114">In This Section</span></span>

  - [<span data-ttu-id="79ebe-115">Создание или редактирование конфигурации XMPP-партнеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79ebe-115">Create or edit XMPP partner configuration in Lync Server 2013</span></span>](lync-server-2013-create-or-edit-xmpp-partner-configuration.md)

  - [<span data-ttu-id="79ebe-116">Параметры согласования для федеративных XMPP-партнеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79ebe-116">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md)

  - [<span data-ttu-id="79ebe-117">Пример конфигурации XMPP в Lync Server 2013 — федерация XMPP с Google Talk</span><span class="sxs-lookup"><span data-stu-id="79ebe-117">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)

<span data-ttu-id="79ebe-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79ebe-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

