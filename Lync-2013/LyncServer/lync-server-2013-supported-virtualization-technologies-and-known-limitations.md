---
title: 'Lync Server 2013: поддерживаемые технологии виртуализации и известные ограничения'
description: 'Lync Server 2013: Поддерживаемые технологии виртуализации и известные ограничения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported virtualization technologies and known limitations
ms:assetid: 6d3d749d-e840-4c05-afae-d6e69e7616aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204982(v=OCS.15)
ms:contentKeyID: 48184428
ms.date: 02/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 745fa535462d29342f4c0a58674ee6487db42a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423563"
---
# <a name="supported-virtualization-technologies-and-known-limitations-in-lync-server-2013"></a><span data-ttu-id="a6e53-103">Поддерживаемые технологии виртуализации и известные ограничения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6e53-103">Supported virtualization technologies and known limitations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6e53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6e53-104">

<span> </span></span></span>

<span data-ttu-id="a6e53-105">_**Тема последнего изменения:** 2017-02-06_</span><span class="sxs-lookup"><span data-stu-id="a6e53-105">_**Topic Last Modified:** 2017-02-06_</span></span>

<span data-ttu-id="a6e53-106">Подключаемый модулей Lync VDI позволяет осуществлять голосовую и видеосвязь в поддерживаемых технологиях виртуализации.</span><span class="sxs-lookup"><span data-stu-id="a6e53-106">The Lync VDI plug-in allows audio and video calling for supported virtualization technologies.</span></span> <span data-ttu-id="a6e53-107">Это расширяет возможности, описанные в статье Microsoft Lync Server 2010 в [виртуализации клиента в техническом документе Microsoft lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) .</span><span class="sxs-lookup"><span data-stu-id="a6e53-107">This extends the functionality outlined for Microsoft Lync Server 2010 in the [Client Virtualization in Microsoft Lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) white paper.</span></span> <span data-ttu-id="a6e53-108">В соответствии с требованиями обычной телефонной сети поддержка стандарта E911 также включена.</span><span class="sxs-lookup"><span data-stu-id="a6e53-108">In compliance with standard telephone regulations, support for E911 is also included.</span></span> <span data-ttu-id="a6e53-109">В следующих разделах описаны технологии виртуализации, поддерживаемые внешним модулем Lync VDI и известными ограничениями функций.</span><span class="sxs-lookup"><span data-stu-id="a6e53-109">The following sections describe the virtualization technologies that are supported by the Lync VDI plug-in and the known feature limitations.</span></span>

<div>

## <a name="support-for-virtualization-technologies"></a><span data-ttu-id="a6e53-110">Поддержка технологий виртуализации</span><span class="sxs-lookup"><span data-stu-id="a6e53-110">Support for Virtualization Technologies</span></span>

<span data-ttu-id="a6e53-111">Плагин Lync VDI поддерживает весь классическое удаленное взаимодействие в сценарии личного виртуального рабочего стола, но не в сценарии подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="a6e53-111">The Lync VDI plug-in supports full desktop remoting in the personal virtual desktop scenario, but not in the remote desktop session scenario.</span></span> <span data-ttu-id="a6e53-112">Эти сценарии можно описать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a6e53-112">These scenarios can be described as follows:</span></span>

  - <span data-ttu-id="a6e53-113">**Поддерживается: персонализированные виртуальные рабочие столы или инфраструктура виртуальных рабочих столов (VDI)**.</span><span class="sxs-lookup"><span data-stu-id="a6e53-113">**Supported: Personalized Virtual Desktops or Virtual Desktop Infrastructure (VDI).**</span></span>   <span data-ttu-id="a6e53-114">В этом сценарии каждый пользователь входит в настраиваемый виртуальный рабочий стол и может сохранять файлы на рабочем столе на протяжении всего периода сеанса.</span><span class="sxs-lookup"><span data-stu-id="a6e53-114">In this scenario, each user logs on to a customizable virtual desktop and is able to save files on the desktop that persist across sessions.</span></span> <span data-ttu-id="a6e53-115">Службы удаленных рабочих столов Microsoft, представление горизонта VMware и Citrix XenDesktop являются реализациями, которые были протестированы для использования с Lync.</span><span class="sxs-lookup"><span data-stu-id="a6e53-115">Microsoft Remote Desktop Services, VMware Horizon View, and Citrix XenDesktop are implementations that have been tested for use with Lync.</span></span> <span data-ttu-id="a6e53-116">Сведения о специфических средах VDI и клиентском оборудовании, проверенных корпорацией Майкрософт, описаны в разделе [инфраструктура, определенная для Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span><span class="sxs-lookup"><span data-stu-id="a6e53-116">For information about vendor-specific VDI environments and client hardware that have been tested by Microsoft, see [Infrastructure qualified for Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span></span>

  - <span data-ttu-id="a6e53-117">**Не поддерживается. Сеансы удаленного рабочего стола.**</span><span class="sxs-lookup"><span data-stu-id="a6e53-117">**Not supported: Remote Desktop Sessions.**</span></span>   <span data-ttu-id="a6e53-118">В этом сценарии каждый пользователь выполняет вход в общий сеанс виртуального рабочего стола, настройка которого невозможна.</span><span class="sxs-lookup"><span data-stu-id="a6e53-118">In this scenario, each user logs on to a generic virtual desktop session that cannot be customized.</span></span> <span data-ttu-id="a6e53-119">Примеры реализации: сеансы удаленного рабочего стола от Microsoft (RDSH) и Citrix XenApp вместе с Citrix Receiver.</span><span class="sxs-lookup"><span data-stu-id="a6e53-119">Example implementations include Microsoft Remote Desktop Sessions (RDSH) and Citrix XenApp combined with Citrix Receiver.</span></span>

<span data-ttu-id="a6e53-120">Плагин Lync VDI не поддерживает другие технологии виртуализации, такие как виртуализация приложений, что позволяет использовать приложение, не требуя установки полного приложения локально.</span><span class="sxs-lookup"><span data-stu-id="a6e53-120">The Lync VDI plug-in does not support other virtualization technologies, such as application virtualization, which allows the use of an application without requiring installation of the full application locally.</span></span> <span data-ttu-id="a6e53-121">Пример реализации: Citrix XenApp и Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="a6e53-121">Example implementations include Citrix XenApp and Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="a6e53-122">Потоковое использование приложений, удаленное использование приложений и смешанные режимы виртуализации (например, удаленное использование приложений в полном наборе функций удаленной работы рабочего стола) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a6e53-122">Application streaming, application remoting, and mixed virtualization modes (for example, application remoting in full desktop remoting) are not supported.</span></span>

<span data-ttu-id="a6e53-123">Чтобы разрешить расширение среды, плагин Lync VDI был разработан для использования независимых от платформы API-интерфейсов динамических виртуальных каналов (DVCs).</span><span class="sxs-lookup"><span data-stu-id="a6e53-123">To allow extensibility, the Lync VDI plug-in was designed to use platform-independent APIs called Dynamic Virtual Channels (DVCs).</span></span> <span data-ttu-id="a6e53-124">Для сценариев, которые не поддерживаются в Lync явным образом, ознакомьтесь с инструкциями по поддержке, предоставленными поставщиком решений VDI.</span><span class="sxs-lookup"><span data-stu-id="a6e53-124">For scenarios that are not explicitly supported by Lync, refer to support statements from the VDI solution provider.</span></span>

</div>

<div>

## <a name="known-feature-limitations"></a><span data-ttu-id="a6e53-125">Известные ограничения функций</span><span class="sxs-lookup"><span data-stu-id="a6e53-125">Known Feature Limitations</span></span>

<span data-ttu-id="a6e53-126">Ниже перечислены известные ограничения при использовании Lync 2013 в среде VDI.</span><span class="sxs-lookup"><span data-stu-id="a6e53-126">The following are known limitations when you use Lync 2013 in a VDI environment:</span></span>

  - <span data-ttu-id="a6e53-127">Ограниченная поддержка функций делегирования звонков и анонимного агента групп ответов.</span><span class="sxs-lookup"><span data-stu-id="a6e53-127">There is limited support for Call Delegation and Response Group Agent Anonymization features.</span></span>

  - <span data-ttu-id="a6e53-128">Следующие функции не поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="a6e53-128">There is no support for the following features:</span></span>
    
      - <span data-ttu-id="a6e53-129">интегрированные страницы настройки аудио- и видеоустройств;</span><span class="sxs-lookup"><span data-stu-id="a6e53-129">Integrated Audio Device and Video Device tuning pages.</span></span>
    
      - <span data-ttu-id="a6e53-130">видео с несколькими представлениями;</span><span class="sxs-lookup"><span data-stu-id="a6e53-130">Multiple-view video.</span></span>
    
      - <span data-ttu-id="a6e53-131">запись бесед;</span><span class="sxs-lookup"><span data-stu-id="a6e53-131">Recording of conversations.</span></span>
    
      - <span data-ttu-id="a6e53-132">Службы удаленных рабочих столов (RDS).</span><span class="sxs-lookup"><span data-stu-id="a6e53-132">Remote Desktop Services (RDS).</span></span>
    
      - <span data-ttu-id="a6e53-133">Анонимное присоединение к собраниям (то есть присоединение к собраниям Lync, размещенным в Организации, которая не является федерациюм в вашей организации).</span><span class="sxs-lookup"><span data-stu-id="a6e53-133">Joining meetings anonymously (that is, joining Lync meetings hosted by an organization that does not federate with your organization).</span></span>
    
      - <span data-ttu-id="a6e53-134">Использование плагина Lync VDI вместе с устройством Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="a6e53-134">Using the Lync VDI plug-in along with a Lync Phone Edition device.</span></span>
    
      - <span data-ttu-id="a6e53-135">непрерывность звонка при сбое сети;</span><span class="sxs-lookup"><span data-stu-id="a6e53-135">Call continuity in case of a network outage.</span></span>
    
      - <span data-ttu-id="a6e53-136">настраиваемые мелодии звонков и музыка при удержании звонка.</span><span class="sxs-lookup"><span data-stu-id="a6e53-136">Customized ringtones and music-on-hold features.</span></span>

  - <span data-ttu-id="a6e53-137">Плагин Lync VDI не поддерживается в среде Microsoft 365 или Office 365.</span><span class="sxs-lookup"><span data-stu-id="a6e53-137">The Lync VDI plug-in is not supported in a Microsoft 365 or Office 365 environment.</span></span>

<span data-ttu-id="a6e53-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6e53-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

