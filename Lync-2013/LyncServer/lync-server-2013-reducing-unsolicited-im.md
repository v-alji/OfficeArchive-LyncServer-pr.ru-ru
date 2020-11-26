---
title: 'Lync Server 2013: уменьшение количества нежелательных мгновенных сообщений'
description: 'Lync Server 2013: сокращение количества нежелательных мгновенных сообщений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reducing unsolicited IM for Lync Server 2013
ms:assetid: d2998708-e699-4465-a918-e1d9ea4c49c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518335(v=OCS.15)
ms:contentKeyID: 62625493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 294c53a6b82b4dc345fbb9afcf9983d5bd35893a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436673"
---
# <a name="reducing-unsolicited-im-for-lync-server-2013"></a><span data-ttu-id="3fd0b-103">Уменьшение количества нежелательных мгновенных сообщений для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fd0b-103">Reducing unsolicited IM for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fd0b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fd0b-104">

<span> </span></span></span>

<span data-ttu-id="3fd0b-105">_**Тема последнего изменения:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="3fd0b-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="3fd0b-106">Интеллектуальный фильтр для обмена мгновенными сообщениями помогает защитить развертывание Microsoft Lync Server 2013 от наиболее распространенных вирусов с минимальным снижением качества взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-106">The Intelligent IM Filter application helps protect your Microsoft Lync Server 2013 deployment against the most common viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="3fd0b-107">Интеллектуальный фильтр мгновенных сообщений предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="3fd0b-107">The Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="3fd0b-108">Улучшенная фильтрация URL-адресов</span><span class="sxs-lookup"><span data-stu-id="3fd0b-108">Enhanced URL filtering</span></span>

  - <span data-ttu-id="3fd0b-109">Улучшенная фильтрация передачи файлов</span><span class="sxs-lookup"><span data-stu-id="3fd0b-109">Enhanced file transfer filtering</span></span>

<span data-ttu-id="3fd0b-110">Используйте интеллектуальный фильтр мгновенных сообщений для настройки фильтров, чтобы блокировать непредусмотренные или потенциально опасные мгновенные сообщения от неизвестных конечных точек за пределами корпоративного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-110">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="3fd0b-111">Вы можете настроить фильтры, указав условия, которые будут использоваться для определения того, что следует блокировать (например, мгновенные сообщения, содержащие гиперссылки и файлы с определенными расширениями).</span><span class="sxs-lookup"><span data-stu-id="3fd0b-111">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks and files with specific extensions.</span></span>

<span data-ttu-id="3fd0b-112">Перед развертыванием приложения для фильтрации сообщений в чате вы должны понять, как применяются параметры фильтрации, когда сообщения пересылаются с одного сервера Lync Server 2013 на другой.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-112">Before you deploy the Intelligent IM Message Filter application, you should understand how filtering options are applied when messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="3fd0b-113">Способ применения этих параметров фильтрации одинаков, независимо от того, находятся ли серверы в одной организации или на разных организационных границах.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-113">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="3fd0b-114">Это соответствие распространяется на то, как настроенные уведомления и тексты предупреждаются в сообщениях и отправляются между серверами.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-114">This consistency applies to the way that the customized notice, and warning texts are inserted into messages and sent across servers.</span></span>

<span data-ttu-id="3fd0b-115">Рекомендуемым вариантом фильтрации является разрешение мгновенных сообщений с гиперссылками, но для отключения ссылки путем вставки знака подчеркивания перед ним требуется интеллектуальный фильтр сообщений.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-115">The recommended filtering option is to allow instant messages with hyperlinks but require the Intelligent IM Filter to disable the link by inserting an underscore before it.</span></span> <span data-ttu-id="3fd0b-116">Если выбрать этот параметр, у вас есть дополнительный параметр создания уведомления для пользователей, которые отображаются в начале каждого мгновенного сообщения, содержащего гиперссылку.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-116">If you choose this option, you have the additional option of composing a notice to users that appears at the beginning of each instant message that contains a hyperlink.</span></span>

<span data-ttu-id="3fd0b-117">Второй вариант фильтрации — разрешить мгновенные сообщения с неизмененными гиперссылками.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-117">A second filtering option is to allow instant messages with unmodified hyperlinks.</span></span> <span data-ttu-id="3fd0b-118">Если выбрать этот параметр, у вас есть дополнительный параметр (рекомендуется) для составления предупреждений для пользователей, которые вставляются в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-118">If you choose this option, you have the additional option (recommended) of composing a warning to users that is inserted in each message.</span></span>

<span data-ttu-id="3fd0b-119">Третьим вариантом является блокировка всех мгновенных сообщений, содержащих гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-119">A third option is to block all instant messages that contain hyperlinks.</span></span> <span data-ttu-id="3fd0b-120">Если выбрать этот параметр, сервер отправляет предупреждение пользователю.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-120">If you choose this option, the server sends a warning to the user.</span></span> <span data-ttu-id="3fd0b-121">Это предупреждение необходимо написать.</span><span class="sxs-lookup"><span data-stu-id="3fd0b-121">You must write this warning.</span></span>

<span data-ttu-id="3fd0b-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fd0b-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

