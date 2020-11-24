---
title: 'Lync Server 2013: включение сервера Office Web Apps и Lync Server 2013'
description: 'Lync Server 2013: Включение Office Web Apps Server и Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Office Web Apps Server and Lync Server 2013
ms:assetid: 3370ab55-9949-4f32-b88b-5cffed6aaad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204792(v=OCS.15)
ms:contentKeyID: 48183790
ms.date: 08/19/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a1bf4e09dc29bf344b78df50595258f0663cd731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399268"
---
# <a name="configuring-integration-with-office-web-apps-server-and-lync-server-2013"></a><span data-ttu-id="a7c3c-103">Настройка интеграции с сервером Office Web Apps и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7c3c-103">Configuring integration with Office Web Apps Server and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7c3c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7c3c-104">

<span> </span></span></span>

<span data-ttu-id="a7c3c-105">_**Тема последнего изменения:** 2016-08-19_</span><span class="sxs-lookup"><span data-stu-id="a7c3c-105">_**Topic Last Modified:** 2016-08-19_</span></span>

<span data-ttu-id="a7c3c-106">Lync Server 2013 использует сервер Office Web Apps для обработки презентаций PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-106">Lync Server 2013 employs Office Web Apps Server to handle PowerPoint presentations.</span></span> <span data-ttu-id="a7c3c-107">Дополнительные сведения о преимуществах этого подхода можно найти [в статье Обзор веб-конференций в Lync Server 2013](lync-server-2013-web-conferencing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a7c3c-107">For information about the advantages to this approach, see [Overview of web conferencing in Lync Server 2013](lync-server-2013-web-conferencing-overview.md).</span></span>

<span data-ttu-id="a7c3c-108">Для использования этих новых возможностей администраторы должны установить Office Web Apps Server, и они должны настроить Lync Server 2013 для взаимодействия с сервером Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-108">In order to use these new capabilities administrators must install Office Web Apps Server and they must configure Lync Server 2013 to communicate with Office Web Apps Server.</span></span> <span data-ttu-id="a7c3c-109">В этой документации содержатся сведения о том, как настроить Lync Server 2013 для работы с сервером Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-109">This documentation provides information on how to configure Lync Server 2013 to work with Office Web Apps Server.</span></span> <span data-ttu-id="a7c3c-110">Сведения о том, что эта документация не содержит, — информация об установке сервера Office Web Apps. Эти сведения можно найти на веб-сайте развертывания Microsoft Office Web Apps по адресу <https://go.microsoft.com/fwlink/p/?linkid=257525> .</span><span class="sxs-lookup"><span data-stu-id="a7c3c-110">What this documentation does not provide is information on how to install Office Web Apps Server itself; for that information, see the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span> <span data-ttu-id="a7c3c-111">В этом руководстве содержатся полные сведения о предварительных требованиях для сервера Office Web Apps. Обратите внимание на то, что сервер Office Web Apps необходимо установить на отдельном компьютере, на котором не запущен Lync Server, Microsoft SQL Server или другое серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-111">That guide includes complete prerequisite information for Office Web Apps Server; note that Office Web Apps Server should be installed on a stand-alone computer that is not running Lync Server, Microsoft SQL Server, or any other server application.</span></span> <span data-ttu-id="a7c3c-112">(На компьютере должна быть установлена какая-либо версия Microsoft Office.) На любом компьютере, который использовался для запуска Office Web Apps, должен быть установлен определенный набор программного обеспечения (включая .NET Framework 4,5 и Windows PowerShell 3,0); Эти требования, а также сведения о настройке сертификатов и информационных служб Интернета (IIS) подробно описаны на веб-сайте развертывания Microsoft Office Web Apps по адресу <https://go.microsoft.com/fwlink/p/?linkid=257525> .</span><span class="sxs-lookup"><span data-stu-id="a7c3c-112">(You must not have any version of Microsoft Office installed on that computer.) Any computer used to run Office Web Apps Server must also have a specific set of software installed (including .NET Framework 4.5 and Windows PowerShell 3.0); these requirements, along with information on configuring certificates and Internet Information Services (IIS), are discussed in detail in the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a7c3c-113">Для последней итерации сервера Office Web Apps используется сервер Office Online, который поддерживается приложением Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-113">The latest iteration of Office Web Apps Server is named Office Online Server, which is supported by Lync Server 2013.</span></span> <span data-ttu-id="a7c3c-114">Дополнительные сведения можно найти в документации по <A href="https://technet.microsoft.com/library/jj219456(v=office.16).aspx">серверу Office Online</A>.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-114">For more detail, refer to the <A href="https://technet.microsoft.com/library/jj219456(v=office.16).aspx">Office Online Server documentation</A>.</span></span>



</div>

<span data-ttu-id="a7c3c-115">В этом документе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="a7c3c-115">This document covers the following topic areas:</span></span>

  - [<span data-ttu-id="a7c3c-116">Настройка Lync Server 2013 для работы с сервером Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="a7c3c-116">Configuring Lync Server 2013 to work with Office Web Apps Server</span></span>](lync-server-2013-configuring-lync-server-2013-to-work-with-office-web-apps-server.md)

  - [<span data-ttu-id="a7c3c-117">Публикация сервера Office Web Apps в Lync Server 2013 с помощью обратного прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="a7c3c-117">Publishing Office Web Apps Server in Lync Server 2013 using a reverse proxy server</span></span>](lync-server-2013-publishing-office-web-apps-server-using-a-reverse-proxy-server.md)

  - [<span data-ttu-id="a7c3c-118">Проверка конфигурации сервера Office Web Apps в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7c3c-118">Validating the configuration of Office Web Apps Server in Lync Server 2013</span></span>](lync-server-2013-validating-the-configuration-of-office-web-apps-server.md)

  - [<span data-ttu-id="a7c3c-119">Настройка клиентов Lync Server 2013 для использования с сервером Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="a7c3c-119">Configuring clients of Lync Server 2013 for use with Office Web Apps Server</span></span>](lync-server-2013-configuring-clients-for-use-with-office-web-apps-server.md)

<span data-ttu-id="a7c3c-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7c3c-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

