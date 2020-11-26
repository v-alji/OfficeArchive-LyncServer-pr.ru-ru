---
title: Настройка фильтрации передачи файлов и URL-адресов для обмена мгновенными сообщениями (IM)
description: Настройка передачи файлов и фильтрации URL-адресов для обмена мгновенными сообщениями (IM).
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring file transfer and URL filtering for instant messaging (IM)
ms:assetid: 115a1a2c-599f-474c-a063-52f7144b5246
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520952(v=OCS.15)
ms:contentKeyID: 48183440
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92f11c3f3bb924c1d92361c2635bfb37e1f03175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433110"
---
# <a name="configuring-file-transfer-and-url-filtering-for-instant-messaging-im-in-lync-server-2013"></a><span data-ttu-id="4fdc8-103">Настройка фильтрации файлов и URL-адресов для обмена мгновенными сообщениями (IM) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4fdc8-103">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4fdc8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4fdc8-104">

<span> </span></span></span>

<span data-ttu-id="4fdc8-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="4fdc8-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="4fdc8-106">Инструмент интеллектуального фильтра мгновенных сообщений помогает защитить развертывание Lync Server 2013 от распространения наиболее распространенных форм вирусов с минимальным снижением качества для взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-106">The Intelligent IM Filter tool helps protect your Lync Server 2013 deployment against the spread of the most common forms of viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="4fdc8-107">Используйте интеллектуальный фильтр мгновенных сообщений для настройки фильтров, чтобы блокировать непредусмотренные или потенциально опасные мгновенные сообщения от неизвестных конечных точек за пределами корпоративного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-107">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="4fdc8-108">Вы можете настроить фильтры, указав условия, которые будут использоваться для определения того, что следует блокировать (например, мгновенные сообщения, содержащие гиперссылки с определенными префиксами и файлами с определенными расширениями).</span><span class="sxs-lookup"><span data-stu-id="4fdc8-108">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks with specific prefixes and files with specific extensions.</span></span>

<span data-ttu-id="4fdc8-109">Интеллектуальный фильтр мгновенных сообщений предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="4fdc8-109">Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="4fdc8-110">Улучшенная фильтрация URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-110">Enhanced URL filtering.</span></span>

  - <span data-ttu-id="4fdc8-111">Улучшенная фильтрация передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-111">Enhanced file transfer filtering.</span></span>

<span data-ttu-id="4fdc8-112">Настройка интеллектуального фильтра мгновенных сообщений включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="4fdc8-112">Configuring Intelligent IM Filter includes the following:</span></span>

  - <span data-ttu-id="4fdc8-113">Настройка фильтрации URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-113">Configuring URL filtering.</span></span>

  - <span data-ttu-id="4fdc8-114">Настройка фильтрации передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-114">Configuring file transfer filtering.</span></span>

<div>

## <a name="how-filtering-options-are-applied-to-instant-messages"></a><span data-ttu-id="4fdc8-115">Применение параметров фильтрации к мгновенным сообщениям</span><span class="sxs-lookup"><span data-stu-id="4fdc8-115">How Filtering Options Are Applied to Instant Messages</span></span>

<span data-ttu-id="4fdc8-116">Прежде чем развертывать инструмент интеллектуального фильтра сообщений, необходимо понять, как будут применяться параметры фильтрации, так как сообщения пересылаются с одного сервера Lync Server 2013 на другой.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-116">Before you deploy the Intelligent IM Message Filter tool, you need to understand how filtering options are applied as messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="4fdc8-117">Способ применения этих параметров фильтрации одинаков, независимо от того, находятся ли серверы в одной организации или на разных организационных границах.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-117">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="4fdc8-118">Это соответствие распространяется на то, как настроенные тексты уведомлений и предупреждений вставляются в сообщения и отправляются на другие серверы.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-118">This consistency applies to the way that the customized notice and warning texts are inserted into messages and sent across servers.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="4fdc8-119">Фильтр мгновенных сообщений увеличивает объем ресурсов ЦП, необходимых для обработки URL-адресов в сообщении.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-119">The instant message filter increases the amount of CPU resources required to process URLs in a message.</span></span> <span data-ttu-id="4fdc8-120">Это повышение спроса на ЦП также влияет на производительность сервера Lync.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-120">This increase in CPU demand also affects the performance of Lync Server.</span></span>



</div>

<span data-ttu-id="4fdc8-121">С помощью страницы **фильтра URL-адреса** в группе " **мгновенные сообщения и присутствие** " на панели управления Lync Server вы можете заблокировать некоторые или все гиперссылки или настроить предупреждение.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-121">By using the **URL Filter** page in the **IM and Presence** group in Lync Server Control Panel, you can block some or all hyperlinks or configure a warning.</span></span> <span data-ttu-id="4fdc8-122">Предупреждение будет вставлено в начало мгновенного сообщения, которое содержит гиперссылку, если вы выбрали параметр **префикс гиперссылки** **Отправить сообщение с предупреждением**.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-122">The warning is inserted at the beginning of an instant message that contains a hyperlink when you choose the **Hyperlink prefix** option **Send warning message**.</span></span>

<span data-ttu-id="4fdc8-123">Если мгновенное сообщение передается с одного сервера на другой, применяются следующие общие правила.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-123">When an instant message travels from one server to another, the following general guidelines apply:</span></span>

  - <span data-ttu-id="4fdc8-124">Если сервер блокирует мгновенное сообщение (так как на странице **фильтра URL-адреса** вы установили флажок **блокировать URL-адреса с расширением файла** или если вы **выбрали параметр** **префикс гиперссылки** ), клиенту будет возвращено сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-124">If a server blocks an instant message (because you selected the **Block URLs with file extension** check box on the **URL Filter** page or because you chose the **Hyperlink prefix** option **Block hyperlinks**), an error message is returned to the client.</span></span> <span data-ttu-id="4fdc8-125">Последующие серверы не получают это мгновенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-125">Subsequent servers do not receive this instant message.</span></span>

  - <span data-ttu-id="4fdc8-126">Если сервер (Server1) добавляет предупреждение в мгновенное сообщение, содержащее активную гиперссылку, последующий сервер (Server2), получающий это мгновенное сообщение, по-прежнему может выполнить различные действия на основе этой активной гиперссылки в мгновенном сообщении и заблокировать мгновенное сообщение или добавить предупреждение.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-126">If a server (Server1) adds a warning to an instant message that contains an active hyperlink, a subsequent server (Server2) that receives this instant message can still take a different action based on this active hyperlink present in the instant message and block the instant message or add a warning.</span></span> <span data-ttu-id="4fdc8-127">Если Server2 настроен только на добавление предупреждений для этого URL-адреса, то предыдущее предупреждение, добавленное с помощью Server1, удаляется, а предупреждение, настроенное на Server2, добавляется в начало мгновенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-127">If Server2 is configured only to add a warning for this URL, the earlier warning added by Server1 is removed, and the warning configured on Server2 is added to the beginning of the instant message.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="4fdc8-128">Если на компьютере установлено приложение Lync Server 2013 в смешанной среде, то для использования интеллектуального фильтра мгновенных сообщений требуется минимальная версия сервера Live Communications Server 2005 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4fdc8-128">If you are running Lync Server 2013 in a mixed environment, Live Communications Server 2005 with SP1 is the minimum version required to use the Intelligent IM Filter application.</span></span> <span data-ttu-id="4fdc8-129">Интеллектуальный фильтр для обмена мгновенными сообщениями не поддерживается на сервере Live Communications Server 2005 без пакета обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4fdc8-129">The Intelligent IM Filter is not supported on Live Communications Server 2005 without SP1.</span></span>



</div>

<div>

## <a name="url-filtering"></a><span data-ttu-id="4fdc8-130">Фильтрация URL-адресов</span><span class="sxs-lookup"><span data-stu-id="4fdc8-130">URL Filtering</span></span>

<span data-ttu-id="4fdc8-131">URL-адреса фильтруются в соответствии с префиксом гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-131">URLs are filtered according to their hyperlink prefix.</span></span> <span data-ttu-id="4fdc8-132">Ниже приведены примеры допустимых префиксов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-132">The following examples are valid prefixes:</span></span>

  - <span data-ttu-id="4fdc8-133">www \* .</span><span class="sxs-lookup"><span data-stu-id="4fdc8-133">www\*.</span></span>

  - <span data-ttu-id="4fdc8-134">адреса.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-134">ftp.</span></span>

  - <span data-ttu-id="4fdc8-135">через</span><span class="sxs-lookup"><span data-stu-id="4fdc8-135">http:</span></span>

<span data-ttu-id="4fdc8-136">Если вы не настраиваете фильтр мгновенных сообщений для фильтрации URL-адресов, все URL-адреса, содержащиеся в мгновенных сообщениях, будут передаваться без изменений с сервера.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-136">If you do not configure the instant message filter to perform any URL filtering, all URLs contained in instant messages are passed unmodified through the server.</span></span> <span data-ttu-id="4fdc8-137">Если настроить фильтр мгновенных сообщений для фильтрации URL-адресов, URL-адреса в мгновенных сообщениях фильтруются в соответствии с параметрами, выбранными в диалоговом окне **Изменение фильтра URL-адреса** или **фильтра по новому URL-адресу** .</span><span class="sxs-lookup"><span data-stu-id="4fdc8-137">If you configure the instant message filter to perform URL filtering, URLs in instant messages are filtered according to the options that you select in the **Edit URL Filter** or **New URL Filter** dialog box.</span></span>

  - <span data-ttu-id="4fdc8-138">**Включить фильтр URL-адресов**   Этот параметр позволяет фильтровать URL-адреса для глобального развертывания или для выбранного сайта.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-138">**Enable URL filter**   This option enables URL filtering for the global deployment or for the site that you select.</span></span>

  - <span data-ttu-id="4fdc8-139">**Блокировать URL-адреса с помощью расширения файла**   Фильтр мгновенных сообщений блокирует любой активный URL-адрес в интрасети или Интернете, содержащий файл с расширением, указанным в поле **расширения типа файлов, которое будет заблокировано** в диалоговом окне **Изменение фильтра файлов** .</span><span class="sxs-lookup"><span data-stu-id="4fdc8-139">**Block URLs with file extension**   The instant message filter blocks any active intranet or Internet URL that contains a file with an extension listed under **File type extensions to block** in the **Edit File Filter** dialog box.</span></span> <span data-ttu-id="4fdc8-140">Если URL-адрес заблокирован, для отправителя выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-140">When a URL is blocked, an error message is displayed to the sender.</span></span> <span data-ttu-id="4fdc8-141">Если установлен этот флажок, этот параметр имеет приоритет над всеми остальными параметрами фильтрации для всех расширений файлов, определенных в разделе **расширения типа файла для блокировки**.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-141">When selected, this option takes precedence over all other filtering options for any file extensions defined under **File type extensions to block**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="4fdc8-142">Фильтрация расширений файлов ограничена стандартными именами файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-142">Filtering of file extensions is limited to standard file names.</span></span> <span data-ttu-id="4fdc8-143">Фильтрация не работает с расширениями файлов, внедренными в другие имена.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-143">Filtering may not work with file extensions embedded in other names.</span></span>

    
    </div>

<span data-ttu-id="4fdc8-144">Чтобы настроить способ обработки гиперссылок в текстовых беседах, выберите один из следующих параметров в разделе **префикс гиперссылки**:</span><span class="sxs-lookup"><span data-stu-id="4fdc8-144">To configure how hyperlinks are handled in instant message conversations, select one of the following options under **Hyperlink prefix**:</span></span>

  - <span data-ttu-id="4fdc8-145">Не **Фильтровать**   URL-адреса в сообщениях отправляются на сервер.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-145">**Do not filter**   URLs in messages are sent through the server.</span></span> <span data-ttu-id="4fdc8-146">Если выбрать этот параметр, появится диалоговое окно **Разрешить сообщение** .</span><span class="sxs-lookup"><span data-stu-id="4fdc8-146">When you choose this option, the **Allow message** box appears.</span></span> <span data-ttu-id="4fdc8-147">В диалоговом окне **Разрешить введите текст** уведомления, которое вы хотите вставить в начало каждого мгновенного сообщения, содержащего гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-147">In the **Allow message** box, specify the notice that you want to insert at the beginning of each instant message containing hyperlinks.</span></span> <span data-ttu-id="4fdc8-148">Это уведомление может состоять не более чем из 65535 знаков.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-148">This notice can consist of no more than 65535 characters.</span></span>

  - <span data-ttu-id="4fdc8-149">**Блокировка гиперссылок**   Передача мгновенных сообщений с активными гиперссылками блокируется сервером Lync Server, и для отправителя выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-149">**Block hyperlinks**   Delivery of instant messages containing active hyperlinks is blocked by Lync Server, and an error message is displayed to the sender.</span></span>

  - <span data-ttu-id="4fdc8-150">**Отправка предупреждающего сообщения**   Lync Server разрешает активные гиперссылки в мгновенных сообщениях, но содержит предупреждение.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-150">**Send warning message**   Lync Server permits active hyperlinks in instant messages, but it includes a warning.</span></span> <span data-ttu-id="4fdc8-151">При выборе этого параметра появится окно **сообщения с предупреждением** .</span><span class="sxs-lookup"><span data-stu-id="4fdc8-151">When you choose this option, the **Warning message** box appears.</span></span> <span data-ttu-id="4fdc8-152">В диалоговом окне **предупреждение** необходимо ввести предупреждение, которое вы хотите включить в мгновенные сообщения, содержащие действительные гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-152">In the **Warning message** box, you must type the warning that you want to include with instant messages containing valid hyperlinks.</span></span> <span data-ttu-id="4fdc8-153">Например, это предупреждение может выдать список возможных опасностей выбора неизвестной ссылки или ссылаться на нужные политики и требования вашей организации.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-153">For example, this warning might state the potential dangers of clicking an unknown link, or it might refer to your organization’s relevant policies and requirements.</span></span> <span data-ttu-id="4fdc8-154">Предупреждение может состоять не более чем из 65535 символов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-154">The warning can be no more than 65535 characters.</span></span>

<span data-ttu-id="4fdc8-155">Если выбрать команду **блокировать гиперссылки** или **Отправить предупреждение**, будут доступны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4fdc8-155">If you select **Block hyperlinks** or **Send warning message**, the following options are available:</span></span>

  - <span data-ttu-id="4fdc8-156">**Исключение гиперссылок местной интрасети**   Фильтр мгновенных сообщений блокирует только URL-адреса в Интернете.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-156">**Exclude local intranet hyperlinks**   The instant message filter blocks only Internet URLs.</span></span> <span data-ttu-id="4fdc8-157">URL-адреса для расположений в интрасети передаются без изменений с сервера.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-157">URLs for locations within your intranet are passed unmodified through the server.</span></span> <span data-ttu-id="4fdc8-158">Тем не менее URL-адреса в интрасети, на которых работают индивидуальные серверы Lync Server, зависят от того, какие типы локальных сайтов считаются частью своей зоны интрасети.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-158">However, the intranet URLs that individual servers running Lync Server pass depend on which types of local websites are considered part of their intranet zone.</span></span> <span data-ttu-id="4fdc8-159">Чтобы проверить параметры зоны интрасети сервера, в разделе "Настройка параметров интрасети в Internet Explorer" [измените фильтр URL-адресов по умолчанию в Lync server 2013](lync-server-2013-modify-the-default-url-filter.md).</span><span class="sxs-lookup"><span data-stu-id="4fdc8-159">To check a server’s intranet zone settings, see the “To configure your intranet settings in Internet Explorer” procedure in [Modify the default URL filter in Lync Server 2013](lync-server-2013-modify-the-default-url-filter.md).</span></span>

  - <span data-ttu-id="4fdc8-160">**Фильтрация префиксов гиперссылок**   Чтобы выбрать префиксы, которые вы хотите заблокировать, нажмите кнопку **выбрать**, а затем в списке **выберите** один из предложенных исправлений добавьте префиксы для **гиперссылок** .</span><span class="sxs-lookup"><span data-stu-id="4fdc8-160">**Filter these hyperlink prefixes**   To choose which prefixes you want to block, click **Select**, and then, in **Select Hyperlink Prefix**, add the prefixes to the **Hyperlink prefixes** list.</span></span>
    
    <span data-ttu-id="4fdc8-161">Все префиксы, кроме **href** , должны заканчиваться точкой или двоеточием или звездочкой, за которой следует точка.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-161">All prefixes except **href** must end with a period or a colon, or an asterisk followed by a period.</span></span> <span data-ttu-id="4fdc8-162">Допустимые префиксы могут содержать символы из набора допустимых URL-знаков, кроме звездочки ( \* ).</span><span class="sxs-lookup"><span data-stu-id="4fdc8-162">Valid prefixes can contain any characters in the set of valid URL characters except the asterisk (\*).</span></span> <span data-ttu-id="4fdc8-163">Набор допустимых символов URL-адреса: \# \* +/0123456789 = @ABCDEFGHIJKLMNOPQRSTUVWXYZ ^ \_ \` ABCDEFGHIJKLMNOPQRSTUVWXYZ | ~</span><span class="sxs-lookup"><span data-stu-id="4fdc8-163">The set of valid URL characters is: \#\*+/0123456789=@ABCDEFGHIJKLMNOPQRSTUVWXYZ^\_\` abcdefghijklmnopqrstuvwxyz|~</span></span>

</div>

<div>

## <a name="file-transfer-filtering"></a><span data-ttu-id="4fdc8-164">Фильтрация передачи файлов</span><span class="sxs-lookup"><span data-stu-id="4fdc8-164">File Transfer Filtering</span></span>

<span data-ttu-id="4fdc8-165">Фильтрация передаваемых фильтров влияет на мгновенные сообщения и конференции.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-165">Filter transfer filtering affects both instant messages and conferences.</span></span> <span data-ttu-id="4fdc8-166">Для конференций эти параметры влияют на функцию раздаточных материалов в клиенте Office Live Meeting 2007 и в средствах воспроизведения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-166">For conferences, these settings affect the handout feature in the Office Live Meeting 2007 client and multimedia playback features.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="4fdc8-167">Lync Server также включает параметры настройки передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-167">Lync Server also offers file transfer setting options.</span></span> <span data-ttu-id="4fdc8-168">Этот параметр на стороне сервера предлагается в дополнение к элементам управления на стороне клиента, доступным в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-168">This server-side option is offered in addition to the client-side controls available in Lync Server.</span></span>



</div>

<span data-ttu-id="4fdc8-169">Вы можете отфильтровать передачу файлов в текстовых беседах, когда вы используете функцию выдач в клиенте Office Live Meeting 2007 и для воспроизведения мультимедиа для всех типов файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-169">You can filter file transfers during instant message conversations, when you are using the handout feature in the Office Live Meeting 2007 client, and for multimedia playback features for all file types.</span></span> <span data-ttu-id="4fdc8-170">Для управления передачей файлов можно настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4fdc8-170">You can set the following options to control file transfers:</span></span>

  - <span data-ttu-id="4fdc8-171">**Включить фильтр файлов**   Этот параметр включает фильтрацию файлов для глобального развертывания или для выбранного сайта.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-171">**Enable file filter**   This option enables file filtering for the global deployment or for the site that you select.</span></span>
    
    <span data-ttu-id="4fdc8-172">Если вы включите фильтр файлов, вы можете выбрать один из следующих вариантов **передачи файлов**.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-172">When you enable the file filter, you can choose one of the following options in **File transfer**:</span></span>
    
      - <span data-ttu-id="4fdc8-173">**Блокировка определенных типов файлов**   Вы можете указать, какие запросы на передачу файлов фильтруются сервером, указав список блокируемых расширений файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-173">**Block specific file types**   You specify which file transfer requests are filtered by the server by specifying a list of file extensions to block.</span></span> <span data-ttu-id="4fdc8-174">Записи в списке могут содержать все стандартные символы, но не подстановочные знаки ( \* ).</span><span class="sxs-lookup"><span data-stu-id="4fdc8-174">Entries in the list can contain all standard characters, but not the wildcard character (\*).</span></span> <span data-ttu-id="4fdc8-175">В клиенте Office Live Meeting 2007 функция выдач включена, но любой файл с этим расширением не удается загрузить или загрузить.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-175">In the Office Live Meeting 2007 client the handout feature is enabled, but any file with this extension cannot be uploaded or downloaded.</span></span> <span data-ttu-id="4fdc8-176">Если установить флажок **блокировать URL-адреса с расширением файла** на вкладке **Фильтр** URL-адреса, то фильтр URL-адреса использует тот же список для блокирования активных гиперссылок, которые содержат любое из этих расширений файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-176">If you select the **Block URLs with file extension** check box on the settings for a URL filter listed on the **URL Filter** tab, the URL filter uses this same list to block active hyperlinks that contain any of these file extensions.</span></span> <span data-ttu-id="4fdc8-177">Чтобы выбрать типы файлов, которые вы хотите заблокировать, нажмите кнопку **выбрать**, а затем в списке **выберите тип файла** добавьте расширения типов файлов в список **выбранные расширения типов файлов** .</span><span class="sxs-lookup"><span data-stu-id="4fdc8-177">To choose which file types you want to block, click **Select**, and then, in **Select File Type**, add the file type extensions to the **Selected file type extensions** list.</span></span>
    
      - <span data-ttu-id="4fdc8-178">**Блокировать все**   Сервер удаляет все мгновенные сообщения, содержащие запросы на передачу файлов, и возвращает сообщение об ошибке отправителю запроса.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-178">**Block All**   The server drops all instant messages that contain file transfer requests and returns an error message to the sender of the request.</span></span> <span data-ttu-id="4fdc8-179">Функция выдач в клиенте Office Live Meeting 2007 отключена.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-179">The handout feature in the Office Live Meeting 2007 client is disabled.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="4fdc8-180">Фильтрация расширений файлов ограничена стандартными именами файлов.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-180">Filtering of file extensions is limited to standard file names.</span></span> <span data-ttu-id="4fdc8-181">Фильтрация не работает с расширениями файлов, внедренными в другие имена.</span><span class="sxs-lookup"><span data-stu-id="4fdc8-181">Filtering may not work with file extensions embedded in other names.</span></span>



</div>

</div>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4fdc8-182">Содержание</span><span class="sxs-lookup"><span data-stu-id="4fdc8-182">In This Section</span></span>

  - [<span data-ttu-id="4fdc8-183">Изменение фильтра передачи файлов по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4fdc8-183">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)

  - [<span data-ttu-id="4fdc8-184">Создание нового фильтра передачи файлов в Lync Server 2013 для определенного сайта</span><span class="sxs-lookup"><span data-stu-id="4fdc8-184">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)

  - [<span data-ttu-id="4fdc8-185">Изменение фильтра URL-адреса по умолчанию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4fdc8-185">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)

  - [<span data-ttu-id="4fdc8-186">Создание фильтра URL-адресов в Lync Server 2013 для обработки гиперссылок в текстовых беседах</span><span class="sxs-lookup"><span data-stu-id="4fdc8-186">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4fdc8-187">См. также</span><span class="sxs-lookup"><span data-stu-id="4fdc8-187">See Also</span></span>


[<span data-ttu-id="4fdc8-188">Управление параметрами обмена мгновенными сообщениями и сведениями о присутствии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4fdc8-188">Managing IM and presence settings in Lync Server 2013</span></span>](lync-server-2013-managing-im-and-presence-settings.md)  
  

<span data-ttu-id="4fdc8-189"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4fdc8-189"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

