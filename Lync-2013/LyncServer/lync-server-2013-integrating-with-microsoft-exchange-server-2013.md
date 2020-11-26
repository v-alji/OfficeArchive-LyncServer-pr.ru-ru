---
title: 'Lync Server 2013: интеграция с Microsoft Exchange Server 2013'
description: 'Lync Server 2013: интеграция с Microsoft Exchange Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating Lync Server 2013 and Exchange Server 2013
ms:assetid: 795dc1c6-524f-4012-8b66-103b55198044
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688098(v=OCS.15)
ms:contentKeyID: 49733697
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54ab4a81e5455bc0a44677b1509876f39ff4d985
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426881"
---
# <a name="integrating-microsoft-lync-server-2013-and-microsoft-exchange-server-2013"></a><span data-ttu-id="4a4fd-103">Интеграция Microsoft Lync Server 2013 и Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a4fd-103">Integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a4fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a4fd-104">

<span> </span></span></span>

<span data-ttu-id="4a4fd-105">_**Тема последнего изменения:** 2014-07-09_</span><span class="sxs-lookup"><span data-stu-id="4a4fd-105">_**Topic Last Modified:** 2014-07-09_</span></span>

<span data-ttu-id="4a4fd-106">В Exchange и Lync Server есть продолжительная история интеграции и совместимости.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-106">Exchange and Lync Server have a long history of integration and compatibility.</span></span> <span data-ttu-id="4a4fd-107">Эта интеграция особенно заметна в соответствующем клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-107">This integration is most noticeable within their respective client application.</span></span> <span data-ttu-id="4a4fd-108">Например, информацию о присутствии Lync можно сообщить в Microsoft Outlook; Аналогичным образом Lync может автоматически обновлять сведения о присутствии с помощью календаря Outlook.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-108">For example, Lync presence information can be reported in Microsoft Outlook; likewise, Lync can use Outlook calendar to automatically update that presence information.</span></span> <span data-ttu-id="4a4fd-109">(Например, Lync может изменить свое состояние на "занят" в любое время, когда в календаре отображается запланированное собрание.) Несмотря на то, что вам не нужно запускать Exchange для работы с Lync Server (или наоборот), у вас есть сомнения в том, что использование двух продуктов вместе epitomizes в определении термина "лучше вместе".</span><span class="sxs-lookup"><span data-stu-id="4a4fd-109">(For example, Lync can change your status to Busy any time your calendar shows that you have a meeting scheduled.) Although you do not have to run Exchange in order to run Lync Server (or vice-versa) there's little doubt that using the two products together epitomizes the very definition of the term "better together."</span></span>

<span data-ttu-id="4a4fd-110">Это особенно актуально при выпуске Microsoft Lync Server 2013 и Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-110">This is especially true with the release of Microsoft Lync Server 2013 and Microsoft Exchange Server 2013.</span></span> <span data-ttu-id="4a4fd-111">Помимо функций, таких как единая система обмена сообщениями и обмен сообщениями и присутствие, которые находятся в Microsoft Exchange Server 2010 и Microsoft Lync Server 2010, выпуски 2013 из серверных продуктов включают ряд новых возможностей.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-111">In addition to features, such as unified messaging and IM and presence, that are found in Microsoft Exchange Server 2010 and Microsoft Lync Server 2010, the 2013 releases of the server products include a number of new capabilities.</span></span> <span data-ttu-id="4a4fd-112">Эти возможности включают в себя следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="4a4fd-112">These capabilities include such things as:</span></span>

  - <span data-ttu-id="4a4fd-113">**Интеграция с архивацией Lync**.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-113">**Lync Archiving Integration**.</span></span> <span data-ttu-id="4a4fd-114">В Lync Server 2013 администраторы по-прежнему могут получать мгновенные сообщения и записи для веб-конференций, архивированные в SQL Server (аналогично тому, как они были архивированы в Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="4a4fd-114">In Lync Server 2013 administrators still have the option of having instant messaging and Web conferencing transcripts archived to SQL Server (the same way these transcripts were archived in Lync Server 2010).</span></span> <span data-ttu-id="4a4fd-115">Кроме того, администраторы могут выбрать, что вы заархивированы в Exchange 2013, сохранив эти записи в почтовых ящиках отдельных пользователей точно так же, как и при обмене сообщениями в архиве Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-115">Alternatively, however, administrators can choose to have transcripts archived to Exchange 2013, storing those transcripts in the individual user mailboxes in the same way in which Exchange archives communications.</span></span> <span data-ttu-id="4a4fd-116">Это означает единое хранилище для всех электронных коммуникаций (из Exchange и Lync Server), что значительно упрощает поиск и получение архивных данных, которые могут возникнуть.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-116">That means a single repository for all your electronic communications (from both Exchange and Lync Server), which makes it much easier to search for and retrieve those archived communications should the need arise.</span></span>

  - <span data-ttu-id="4a4fd-117">**Единое хранилище контактов**.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-117">**Unified Contact Store**.</span></span> <span data-ttu-id="4a4fd-118">В Lync Server 2010 пользователям пришлось поддерживать отдельные списки контактов в Outlook и Lync; на самом деле, чтобы убедиться в том, что у вас есть одинаковые контакты в обоих продуктах, вы должны поддерживать дубликаты списков контактов, для Outlook и для Lync.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-118">In Lync Server 2010, users had to maintain separate contact lists in Outlook and Lync; in fact, to ensure that you had the same contacts available in both products you had to maintain duplicate contact lists, one for Outlook and one for Lync.</span></span> <span data-ttu-id="4a4fd-119">Однако при использовании Lync Server 2013 контакты пользователей могут храниться в Exchange 2013 и едином банке контактов.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-119">With Lync Server 2013, however, user contacts can be stored in Exchange 2013 and the unified contact store.</span></span> <span data-ttu-id="4a4fd-120">С помощью одного магазина контактов пользователи смогут поддерживать только один набор контактов, с тем же набором контактов, который доступен в Lync 2013, Outlook 2013 и Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-120">Using a single contact store enables users to maintain just one set of contacts, with that same set of contacts being available in Lync 2013, Outlook 2013, and Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="4a4fd-121">**Планирование собраний Lync из Outlook Web** App.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-121">**Lync Meeting Scheduling from OWA**.</span></span> <span data-ttu-id="4a4fd-122">С помощью Lync Server 2013 и Exchange 2013 интеграция пользователи могут планировать собрания Lync из Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-122">With Lync Server 2013 and Exchange 2013 integration, users can schedule Lync meetings from Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="4a4fd-123">**Фотографии высокого разрешения**.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-123">**High resolution photos**.</span></span> <span data-ttu-id="4a4fd-124">Lync 2010 может показывать только небольшие фотографии контактов; Это объясняется тем, что эти фотографии хранились в службе каталогов Active Directory, а служба каталогов Active Directory накладывает на 48 точку 48 с ограничением размера в пикселях для сохраненных фотографий.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-124">Lync 2010 could only display small photos of your contacts; that's because those photos were stored in Active Directory, and Active Directory imposes a 48 pixel by 48 pixel size limitation on stored photos.</span></span> <span data-ttu-id="4a4fd-125">Однако в Lync Server 2013 фотографии могут храниться в Microsoft Exchange; Это позволяет создавать фотографии высокого разрешения размером в 648 пикселей на 648 пикселей.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-125">With Lync Server 2013, however, photos can be stored in Microsoft Exchange; that allows for high-resolution photos as large as 648 pixels by 648 pixels.</span></span> <span data-ttu-id="4a4fd-126">Как вы можете ожидать, Lync 2013 был обновлен таким образом, чтобы иметь возможность отображать фотографии высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-126">As you might expect, Lync 2013 has been upgraded to allow for the display of these high-resolution photographs.</span></span>

<span data-ttu-id="4a4fd-127">Имейте в виду, что для этих новых функций требуется использование как Lync Server 2013, так и Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-127">Keep in mind that these new features require the use of both Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="4a4fd-128">Кроме того, пользователи, которые хотят воспользоваться всеми преимуществами этих новых возможностей, должны иметь учетные записи на Lync Server 2013 и Exchange 2013 и должны использовать последние версии клиентского программного обеспечения (например, Lync 2013).</span><span class="sxs-lookup"><span data-stu-id="4a4fd-128">In addition to that, users who hope to take full advantage of these new capabilities must have accounts on Lync Server 2013 and Exchange 2013, and must be using the latest versions of the client software (e.g., Lync 2013).</span></span> <span data-ttu-id="4a4fd-129">Например, единое хранилище контактов недоступно для пользователей, которые были размещены на сервере Lync Server 2010; Кроме того, в Lync 2010 не отображаются фотографии высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-129">For example, the unified contact store is not available to users who have been homed on Lync Server 2010; likewise, high-resolution photos cannot be displayed in Lync 2010.</span></span>

<span data-ttu-id="4a4fd-130">В этой документации содержатся сведения о том, как интегрировать Lync Server 2013 и Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-130">This documentation provides information on integrating Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="4a4fd-131">включая пошаговые инструкции по включению новых функций, таких как интеграция архивирования и единое хранилище контактов.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-131">including step-by-step information on enabling new features such archiving Integration and the unified contact store.</span></span> <span data-ttu-id="4a4fd-132">Это не относится к рассмотрению первоначальной настройки и конфигурации этих двух продуктов.</span><span class="sxs-lookup"><span data-stu-id="4a4fd-132">What this documentation does not do is discuss the initial setup and configuration of these two products.</span></span> <span data-ttu-id="4a4fd-133">Подробнее о том, как развертывать Lync Server 2013, можно найти в разделе Lync Server 2013 Tech Center по адресу [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127) .</span><span class="sxs-lookup"><span data-stu-id="4a4fd-133">For details about deploying Lync Server 2013 see the Lync Server 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127).</span></span> <span data-ttu-id="4a4fd-134">Подробнее о том, как развертывать Exchange 2013, можно найти в центре Exchange 2013 Tech Center по адресу [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528) .</span><span class="sxs-lookup"><span data-stu-id="4a4fd-134">For details about deploying Exchange 2013 see the Exchange 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4a4fd-135">Содержание</span><span class="sxs-lookup"><span data-stu-id="4a4fd-135">In This Section</span></span>

[<span data-ttu-id="4a4fd-136">Необходимые условия для интеграции Microsoft Lync Server 2013 и Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a4fd-136">Prerequisites for integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-prerequisites-for-integrating-with-exchange-server-2013.md)

[<span data-ttu-id="4a4fd-137">Настройка партнерских приложений в Microsoft Lync Server 2013 и Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a4fd-137">Configuring partner applications in Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-configuring-partner-applications-in-lync-server-2013-and-exchange-server-2013.md)

[<span data-ttu-id="4a4fd-138">Настройка Microsoft Lync Server 2013 для использования архивации Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a4fd-138">Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving</span></span>](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md)

[<span data-ttu-id="4a4fd-139">Настройка Microsoft SharePoint Server 2013 для поиска архивированных данных Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a4fd-139">Configuring Microsoft SharePoint Server 2013 to search for archived Microsoft Lync Server 2013 data</span></span>](lync-server-2013-configuring-microsoft-sharepoint-server-2013-to-search-for-archived-lync-server-2013-data.md)

[<span data-ttu-id="4a4fd-140">Настройка Microsoft Lync Server 2013 для работы с единым хранилищем контактов</span><span class="sxs-lookup"><span data-stu-id="4a4fd-140">Configuring Microsoft Lync Server 2013 to use the unified contact store</span></span>](lync-server-2013-configuring-lync-server-to-use-the-unified-contact-store.md)

[<span data-ttu-id="4a4fd-141">Настройка использования фотографий высокого разрешения в Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a4fd-141">Configuring the use of high-resolution photos in Microsoft Lync Server 2013</span></span>](lync-server-2013-configuring-the-use-of-high-resolution-photos.md)

[<span data-ttu-id="4a4fd-142">Настройка единой системы обмена сообщениями Microsoft Exchange Server 2013 для Microsoft Lync Server 2013 для голосовой почты</span><span class="sxs-lookup"><span data-stu-id="4a4fd-142">Configuring Microsoft Exchange Server 2013 Unified Messaging for Microsoft Lync Server 2013 voice mail</span></span>](lync-server-2013-configuring-microsoft-exchange-server-2013-unified-messaging-for-lync-server-2013-voice-mail.md)

[<span data-ttu-id="4a4fd-143">Интеграция Microsoft Lync Server 2013 и Microsoft Outlook Web App 2013</span><span class="sxs-lookup"><span data-stu-id="4a4fd-143">Integrating Microsoft Lync Server 2013 and Microsoft Outlook Web App 2013</span></span>](lync-server-2013-integrating-lync-server-and-outlook-web-app-2013.md)

<span data-ttu-id="4a4fd-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a4fd-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

