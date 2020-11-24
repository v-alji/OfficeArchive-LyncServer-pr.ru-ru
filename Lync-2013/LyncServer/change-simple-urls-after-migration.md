---
title: Изменение простых URL-адресов после миграции
description: Изменение простых URL-адресов после миграции.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change simple URLs after migration
ms:assetid: addb0dc8-8324-42b1-9a00-f4bd14fdf5c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721844(v=OCS.15)
ms:contentKeyID: 49733777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f9974106d28bcfdc64c2255337baf721a937e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398581"
---
# <a name="change-simple-urls-after-migration"></a><span data-ttu-id="79f71-103">Изменение простых URL-адресов после миграции</span><span class="sxs-lookup"><span data-stu-id="79f71-103">Change simple URLs after migration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79f71-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79f71-104">

<span> </span></span></span>

<span data-ttu-id="79f71-105">_**Тема последнего изменения:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="79f71-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="79f71-106">Lync Server поддерживает три простых URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="79f71-106">Lync Server supports three simple URLs:</span></span>

  - <span data-ttu-id="79f71-107">" **Встреча** " используется в качестве базового URL-адреса для всех конференций на сайте или в Организации.</span><span class="sxs-lookup"><span data-stu-id="79f71-107">**Meet** is used as the base URL for all conferences in the site or organization.</span></span> <span data-ttu-id="79f71-108">С помощью простого URL-адреса вы можете легко усвоеновать ссылки на собрания, а также легко и распространены.</span><span class="sxs-lookup"><span data-stu-id="79f71-108">With the Meet simple URL, links to join meetings are easy to comprehend, and easy to communicate and distribute.</span></span>

  - <span data-ttu-id="79f71-109">С помощью **телефонного подключения** можно получить доступ к веб-странице параметров конференций с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="79f71-109">**Dial-in** enables access to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="79f71-110">Простой URL-адрес телефонного подключения включается во все приглашения на собрания. Таким образом пользователи, которые хотят подключиться к собранию по телефону, могут найти в нем необходимый номер телефона и ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="79f71-110">The Dial-in simple URL is included in all meeting invitations so that users who want to dial in to the meeting can access the necessary phone number and PIN information.</span></span>

  - <span data-ttu-id="79f71-111">**Администратор** обеспечивает быстрый доступ к панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="79f71-111">**Admin** enables quick access to the Lync Server Control Panel.</span></span> <span data-ttu-id="79f71-112">Этот URL-адрес используется внутри организации.</span><span class="sxs-lookup"><span data-stu-id="79f71-112">The Admin simple URL is internal to your organization.</span></span>

<span data-ttu-id="79f71-113">После перехода на Lync Server 2013 необходимо учитывать, как это изменение влияет на записи DNS и сертификаты для простых URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="79f71-113">After migrating to Lync Server 2013, you must be aware of how the change impacts your DNS records and certificates for simple URLs.</span></span> <span data-ttu-id="79f71-114">Если в вашей топологии используется устаревший режиссер Lync Server 2010, изменения, внесенные в простой URL-адрес, не требуются.</span><span class="sxs-lookup"><span data-stu-id="79f71-114">If the legacy Lync Server 2010 Director remains in use in the topology, no changes to your simple URLs are required.</span></span> <span data-ttu-id="79f71-115">Если режиссер Lync Server 2010 удаляется из топологии после миграции, необходимо обновить простые DNS-записи, чтобы они указывали на один из пулов Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="79f71-115">If the Lync Server 2010 Director is removed from the topology after migration, the simple URL DNS records must be updated to point to one of the Lync Server 2013 pools.</span></span> <span data-ttu-id="79f71-116">Однако каждый раз, когда вы изменяете простое имя URL-адреса, необходимо выполнить Enable-CsComputer для каждого директора и сервера переднего плана для регистрации изменения.</span><span class="sxs-lookup"><span data-stu-id="79f71-116">Whenever you change a simple URL name, however, you must run Enable-CsComputer on each Director and Front End Server to register the change.</span></span>

<div>

## <a name="changing-simple-urls-after-migration"></a><span data-ttu-id="79f71-117">Изменение простых URL-адресов после миграции</span><span class="sxs-lookup"><span data-stu-id="79f71-117">Changing Simple URLs after Migration</span></span>

<span data-ttu-id="79f71-118">**Обновление простого URL-адреса для собрания**</span><span class="sxs-lookup"><span data-stu-id="79f71-118">**To update the Meet simple URL**</span></span>

1.  <span data-ttu-id="79f71-119">В построителе топологии щелкните правой кнопкой мыши верхний узел **Lync Server** и выберите команду **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="79f71-119">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="79f71-120">В левой области выберите **простые URL** -адреса, а затем — URL-адреса для **собраний:** выберите в поле "адрес для собрания" и нажмите кнопку **изменить URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="79f71-120">Select **Simple URLs** in the left pane, then below **Meeting URLs:** select the Meet URL and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="79f71-121">Установите для URL-адреса нужное значение и нажмите кнопку **ОК**, чтобы сохранить измененный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="79f71-121">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span>

<span data-ttu-id="79f71-122">**Обновление простого URL-адреса администратора**</span><span class="sxs-lookup"><span data-stu-id="79f71-122">**To update the Admin simple URL**</span></span>

1.  <span data-ttu-id="79f71-123">В построителе топологии щелкните правой кнопкой мыши верхний узел **Lync Server** и выберите команду **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="79f71-123">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="79f71-124">Выберите **простые URL-адреса** в левой области, а затем в поле **URL-адрес администратора** введите простой URL-адрес, который вы хотите использовать для административного доступа к панели управления Lync Server 2013, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="79f71-124">Select **Simple URLs** in the left pane, then below **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="79f71-125">В качестве URL-адреса администрирования рекомендуется использовать максимально простой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="79f71-125">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="79f71-126">Это самый простой вариант <STRONG> https://admin .</STRONG> &lt; Domain (домен) &gt; .</span><span class="sxs-lookup"><span data-stu-id="79f71-126">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="79f71-127">См. также</span><span class="sxs-lookup"><span data-stu-id="79f71-127">See Also</span></span>


[<span data-ttu-id="79f71-128">Планирование простых URL-адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79f71-128">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="79f71-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79f71-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

