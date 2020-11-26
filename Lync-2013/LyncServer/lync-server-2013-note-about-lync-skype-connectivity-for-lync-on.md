---
title: 'Lync Server 2013: Примечание о подключении к Lync-Skype для Lync на'
description: 'Lync Server 2013: Примечание о подключении к Lync-Skype для Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Note about Lync-Skype connectivity for Lync On
ms:assetid: 1d0f5c1a-74c6-468f-9877-ad2b1ddf355f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440169(v=OCS.15)
ms:contentKeyID: 57793359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f7d9758f277f2f987677c2c0ffa0a4447ba31d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424977"
---
# <a name="note-about-lync-skype-connectivity-in-lync-server-2013-for-lync-online-customers"></a><span data-ttu-id="a7e47-103">Примечание о подключении к Lync-Skype в Lync Server 2013 для пользователей Lync Online</span><span class="sxs-lookup"><span data-stu-id="a7e47-103">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7e47-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7e47-104">

<span> </span></span></span>

<span data-ttu-id="a7e47-105">_**Тема последнего изменения:** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="a7e47-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="a7e47-106">Этот документ предназначен для того, чтобы помочь администраторам локальной сети Lync Server настроить Lync-Skype подключения.</span><span class="sxs-lookup"><span data-stu-id="a7e47-106">This document was written to help Lync Server on-premise administrators set up Lync-Skype connectivity.</span></span>  <span data-ttu-id="a7e47-107">Lync-Skype подключение также является функцией Lync Online, которая входит в состав Office 365 и Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a7e47-107">Lync-Skype connectivity is also a feature of Lync Online, which is part of Office 365 and Microsoft 365.</span></span> <span data-ttu-id="a7e47-108">Вы можете включить функцию подключения к Lync-Skype в центре администрирования Lync, в центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="a7e47-108">You can enable the Lync-Skype connectivity feature from the Lync Administration Center within the admin center.</span></span>

<span data-ttu-id="a7e47-109">Для Microsoft 365 среднего бизнеса, Office 365 корпоративный, Microsoft 365 для образовательных учреждений и Office 365 для государственных организаций: Войдите в **центр администрирования Lync** на портале Office 365 или Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a7e47-109">For Microsoft 365 Midsize Business, Office 365 Enterprise, Microsoft 365 Education, and Office 365 for Government: Sign in to the Office 365 portal or Microsoft 365 admin center and navigate to the **Lync Administration Center**.</span></span> <span data-ttu-id="a7e47-110">Переход на **внешнюю связь**.</span><span class="sxs-lookup"><span data-stu-id="a7e47-110">Go to **External Communications**.</span></span> <span data-ttu-id="a7e47-111">В разделе **поставщики общедоступной службы обмена мгновенными сообщениями** нажмите кнопку **включить**.</span><span class="sxs-lookup"><span data-stu-id="a7e47-111">Under **Public IM Service Providers**, click **Enable**.</span></span> <span data-ttu-id="a7e47-112">Если вы хотите контролировать доступ отдельных пользователей к Lync-Skype подключениям, вы можете изменить параметры внешних подключений отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="a7e47-112">If you want to control individual user access to Lync-Skype Connectivity, you can do so by editing individual users’ External Communications settings.</span></span>

<span data-ttu-id="a7e47-113">Для Microsoft 365 для малого бизнеса расширенный выполните вход в Microsoft 365 и перейдите к разделу **\> Настройка службы администрирования \> мгновенных сообщений, собраний и конференций**.</span><span class="sxs-lookup"><span data-stu-id="a7e47-113">For Microsoft 365 Small Business Premium: Sign in to Microsoft 365, and go to **Admin \> Service Settings \> Instant messaging, meetings and conferencing**.</span></span> <span data-ttu-id="a7e47-114">Включите функцию внешней связи.</span><span class="sxs-lookup"><span data-stu-id="a7e47-114">Turn on External communications.</span></span> <span data-ttu-id="a7e47-115">Коммутатор внешней связи включает и Lync-Skype связь, и связь с другими организациями, которые используют Lync.</span><span class="sxs-lookup"><span data-stu-id="a7e47-115">The External communications switch turns on both Lync-Skype connectivity and communications with other organizations that use Lync.</span></span> <span data-ttu-id="a7e47-116">В зависимости от того, когда вы начали пользоваться Lync Online, в состоянии "вкл." внешнем переключателе связи может быть указано только то, что активирована связь с другими организациями Lync.</span><span class="sxs-lookup"><span data-stu-id="a7e47-116">Depending on when you started using Lync Online, the External communications switch in an "on" state may initially indicate only that communications with other Lync organizations is activated.</span></span> <span data-ttu-id="a7e47-117">Чтобы включить Lync-Skype подключение, просто переключите его, а затем снова включите.</span><span class="sxs-lookup"><span data-stu-id="a7e47-117">To turn on Lync-Skype Connectivity, simply toggle the switch off and then back on again.</span></span>

<span data-ttu-id="a7e47-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7e47-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

