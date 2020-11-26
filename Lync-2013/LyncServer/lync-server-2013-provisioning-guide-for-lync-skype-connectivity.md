---
title: 'Lync Server 2013: руководство по подготовке взаимодействия Lync-Skype'
description: 'Lync Server 2013: руководство по подготовке к Lync-Skype подключения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Provisioning guide for Lync-Skype connectivity
ms:assetid: 69adda9b-5b72-4538-9be6-079b2f462e09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440173(v=OCS.15)
ms:contentKeyID: 57793363
ms.date: 11/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9859a7a621ba4329fe0436fe50a0d9de1d0ae1ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436743"
---
# <a name="provisioning-guide-for-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="e8e6a-103">Руководство по подготовке взаимодействия Lync-Skype в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8e6a-103">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8e6a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8e6a-104">

<span> </span></span></span>

<span data-ttu-id="e8e6a-105">_**Тема последнего изменения:** 2014-11-26_</span><span class="sxs-lookup"><span data-stu-id="e8e6a-105">_**Topic Last Modified:** 2014-11-26_</span></span>

<span data-ttu-id="e8e6a-106">Lync Server 2013 поддерживает возможность подключения к Skype.</span><span class="sxs-lookup"><span data-stu-id="e8e6a-106">Lync Server 2013 supports connectivity with Skype.</span></span> <span data-ttu-id="e8e6a-107">Благодаря этому пользователи Lync 2013 могут добавлять контакты Skype, используя учетные записи Microsoft (MSA) пользователей Skype.</span><span class="sxs-lookup"><span data-stu-id="e8e6a-107">This connectivity enables your Lync 2013 users to add Skype contacts by using the Skype user’s Microsoft Account (MSA).</span></span> <span data-ttu-id="e8e6a-108">Клиенты Skype также могут добавлять пользователей Lync в свои списки контактов.</span><span class="sxs-lookup"><span data-stu-id="e8e6a-108">Skype clients can also add Lync users to their contact list.</span></span> <span data-ttu-id="e8e6a-109">В соответствии с политиками, заданными на сервере Lync Server, пользователи Lync и Skype смогут обмениваться мгновенными сообщениями, просматривать сведения о присутствии друг друга, а также совершать голосовые звонки и видеозвонки.</span><span class="sxs-lookup"><span data-stu-id="e8e6a-109">Based on policies administratively set in Lync Server, Lync and Skype users will be able to communicate using instant messaging, see each other’s presence, and initiate audio and video calls.</span></span> <span data-ttu-id="e8e6a-110">Lync-Skype подключение также является функцией Lync Online и может быть включена для пользователей Lync Online из центра администрирования Lync в центре управления Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e8e6a-110">Lync-Skype connectivity is also a feature of Lync Online, and can be enabled for Lync Online customers from the Lync Administration Center within the Microsoft 365 admin center.</span></span>

<div>

> [!IMPORTANT]  
> <span data-ttu-id="e8e6a-p102">Если сервер Lync Server уже настроен для взаимодействия с приложением Windows Messenger с использованием общедоступной службы обмена сообщениями (PIC), это означает, что интеграция Lync и Skype уже настроена в вашей среде, и вам достаточно будет переименовать существующую запись общедоступной службы обмена сообщениями Messenger в Skype. Подробные сведения см. в разделе, посвященном настройке параметров поставщика общедоступной службы обмена сообщениями Skype для Lync, далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="e8e6a-p102">If Lync Server is already configured to connect with Windows Messenger by using Public Instant Messaging Connectivity (PIC), your deployment is already configured for Lync-Skype connectivity. The only change you may want to consider is to rename your existing Messenger PIC entry as Skype. For details, see Configure the Skype PIC provider setting for Lync later in this guide.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e8e6a-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="e8e6a-114">In This Section</span></span>

  - [<span data-ttu-id="e8e6a-115">Примечание о подключении к Lync-Skype в Lync Server 2013 для пользователей Lync Online</span><span class="sxs-lookup"><span data-stu-id="e8e6a-115">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>](lync-server-2013-note-about-lync-skype-connectivity-for-lync-on.md)

  - [<span data-ttu-id="e8e6a-116">Доступ к сайту предоставления общедоступной службы обмена мгновенными сообщениями из Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8e6a-116">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>](lync-server-2013-accessing-the-lync-server-public-im-connectivity-provisioning-site.md)

  - [<span data-ttu-id="e8e6a-117">Обеспечение взаимодействия Lync и Skype в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8e6a-117">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-enabling-lync-skype-connectivity.md)

  - [<span data-ttu-id="e8e6a-118">Взаимодействие между конечными пользователями Lync и Skype в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8e6a-118">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

  - [<span data-ttu-id="e8e6a-119">Часто задаваемые вопросы: подготовка сервера Lync Server 2013 для подключения Skype</span><span class="sxs-lookup"><span data-stu-id="e8e6a-119">Frequently Asked Questions: Provisioning Lync Server 2013 for Skype connectivity</span></span>](lync-server-2013-frequently-asked-questions-provisioning-lync-server-for-skype-connectivity.md)

<span data-ttu-id="e8e6a-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8e6a-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

