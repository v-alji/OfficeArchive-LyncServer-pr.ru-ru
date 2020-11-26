---
title: 'Lync Server 2013: отключение обхода сетевых мультимедийных файлов'
description: 'Lync Server 2013: отключение обхода сетевого мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling network media bypass
ms:assetid: 936d2678-d712-4589-b172-b5793013652f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688141(v=OCS.15)
ms:contentKeyID: 49733741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1472711417218aa87936a3ccabe1bb465dd07c20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429100"
---
# <a name="disabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="ee842-103">Отключение обхода сетевых мультимедийных файлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee842-103">Disabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee842-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee842-104">

<span> </span></span></span>

<span data-ttu-id="ee842-105">_**Тема последнего изменения:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="ee842-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="ee842-106">Параметры обхода мультимедиа применяются глобально в рамках развертывания Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ee842-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="ee842-107">Обойти функцию мультимедиа позволяет обходить сервер.</span><span class="sxs-lookup"><span data-stu-id="ee842-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="ee842-108">Сведения о том, когда следует использовать обход мультимедиа, приведены в статье [Планирование обхода мультимедиа в Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) в разделе Планирование. Вы можете отключить обход мультимедиа с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ee842-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.You can disable media bypass from the Lync Server Control Panel.</span></span> <span data-ttu-id="ee842-109">Дополнительные сведения о включении и настройке Medial обхода можно найти [в разделе Включение обхода сетевого мультимедиа в Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span><span class="sxs-lookup"><span data-stu-id="ee842-109">For details on enabling and configuring medial bypass, see [Enabling network media bypass in Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span></span>

<div>

## <a name="to-disable-media-bypass"></a><span data-ttu-id="ee842-110">Отключение обхода мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ee842-110">To disable media bypass</span></span>

1.  <span data-ttu-id="ee842-111">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ee842-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ee842-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ee842-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ee842-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ee842-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ee842-114">На панели навигации слева выберите пункт **Конфигурация сети** , а затем — **Глобальная**.</span><span class="sxs-lookup"><span data-stu-id="ee842-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="ee842-115">На **глобальной** странице щелкните **глобальную** конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ee842-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="ee842-116">Всегда существует только одна конфигурация, и она всегда имеет имя Global.</span><span class="sxs-lookup"><span data-stu-id="ee842-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="ee842-117">В меню **Правка** выберите команду **Просмотреть сведения**.</span><span class="sxs-lookup"><span data-stu-id="ee842-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="ee842-118">На странице **изменение глобальных параметров** снимите флажок **включить обход мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="ee842-118">On the **Edit Global Setting** page, clear the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="ee842-119">Нажмите **кнопку Сохранить,** чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="ee842-119">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee842-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ee842-120">See Also</span></span>


[<span data-ttu-id="ee842-121">Включение обхода сетевых мультимедийных файлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee842-121">Enabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-network-media-bypass.md)  
  

<span data-ttu-id="ee842-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee842-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

