---
title: 'Lync Server 2013: развертывание системы комнат Lync на веб-портале администрирования'
description: 'Lync Server 2013: развертывание системы управления комнатой на Lync Web портал.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying the Lync Room System Administrative Web Portal
ms:assetid: ecba5b36-632e-40b9-9c2e-ab825baf7a46
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436324(v=OCS.15)
ms:contentKeyID: 56737621
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e67723b3ddf3f452c53411e560420bb0b043128e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398197"
---
# <a name="deploying-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="98019-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98019-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98019-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98019-104">

<span> </span></span></span>

<span data-ttu-id="98019-105">_**Тема последнего изменения:** 2015-05-04_</span><span class="sxs-lookup"><span data-stu-id="98019-105">_**Topic Last Modified:** 2015-05-04_</span></span>

<span data-ttu-id="98019-106">Портал администрирования Microsoft Lync Server 2013 Lync (LRS) — это веб-портал, с помощью которого организации могут сохранять Конференц-зал системы Lync.</span><span class="sxs-lookup"><span data-stu-id="98019-106">The Microsoft Lync Server 2013 Lync Room System (LRS) Administrative Web Portal is a web portal that organizations can use to maintain their Lync Room System conference rooms.</span></span> <span data-ttu-id="98019-107">Администраторы могут использовать веб-портал LRS администрирования для мониторинга работоспособности LRS, например за счет наблюдения за подключением аудио-и видеоустройств.</span><span class="sxs-lookup"><span data-stu-id="98019-107">Administrators can use the LRS Administrative Web Portal to monitor LRS health, for example by monitoring audio/video devices that are connected.</span></span> <span data-ttu-id="98019-108">С помощью этого портала, администраторы могут удаленно собирать диагностические сведения, чтобы отслеживать работоспособность конференц-зала.</span><span class="sxs-lookup"><span data-stu-id="98019-108">With this portal, administrators can remotely collect diagnostic information to monitor conference room health.</span></span>

<span data-ttu-id="98019-109">Веб-портал LRS администрирования разворачивается на каждом сервере клиентского доступа Lync.</span><span class="sxs-lookup"><span data-stu-id="98019-109">The LRS Administrative Web Portal is deployed on every Lync Front End Server.</span></span> <span data-ttu-id="98019-110">Это руководство содержит инструкции для администраторов о том, как установить и настроить веб-портал LRS администрирования.</span><span class="sxs-lookup"><span data-stu-id="98019-110">This guide provides instructions for administrators about how to install and configure the LRS Administrative Web Portal.</span></span> <span data-ttu-id="98019-111">Она предназначена для администраторов, которые имеют опыт администрирования Lync Server и имеют права администратора на изменение топологии сервера Lync.</span><span class="sxs-lookup"><span data-stu-id="98019-111">It is intended for administrators who have knowledge of Lync Server administration, and who have administrator user rights to modify the Lync Server topology.</span></span>

<span data-ttu-id="98019-112">После развертывания веб-портала LRS на сервере администраторы могут проверить состояние всех комнат LRS, войдя на сайт со своих компьютеров или ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="98019-112">After LRS Administrative Web Portal is deployed on the server, administrators can check the status of all LRS rooms by logging on to the site from their own computers or laptops.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="98019-113">Когда вы устанавливаете веб-портал LRS на сайте Microsoft Lync Server 2013, вы должны использовать <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">веб-портал для Microsoft Lync на комнатной подсистеме для Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="98019-113">When you install the LRS Administrative Web Portal in a Microsoft Lync Server 2013 deployment, you should use the <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">Microsoft Lync Room System Administrative Web Portal for Lync Server 2013</A>.</span></span><BR><span data-ttu-id="98019-114">Для Skype для бизнеса Server 2015 доступна новая версия веб-портала LRS, но ее не следует устанавливать, если вы не развернули версию Skype для бизнеса Server 2015.</span><span class="sxs-lookup"><span data-stu-id="98019-114">A new version of the LRS Administrative Web Portal is available for Skype for Business Server 2015, but you should not install that version unless you have deployed Skype for Business Server 2015.</span></span> <span data-ttu-id="98019-115">Скачайте <A href="https://go.microsoft.com/fwlink/?linkid=544807">веб-портал для Microsoft Lync комнатной подсистемы для Skype для бизнеса Server 2015</A>.</span><span class="sxs-lookup"><span data-stu-id="98019-115">Download the <A href="https://go.microsoft.com/fwlink/?linkid=544807">Microsoft Lync Room System Administrative Web Portal for Skype for Business Server 2015</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="98019-116">Содержание</span><span class="sxs-lookup"><span data-stu-id="98019-116">In This Section</span></span>

[<span data-ttu-id="98019-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span><span class="sxs-lookup"><span data-stu-id="98019-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span></span>](lync-server-2013-configuring-your-environment-for-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="98019-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98019-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-installing-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="98019-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98019-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-using-the-lync-room-system-administrative-web-portal.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="98019-120">См. также</span><span class="sxs-lookup"><span data-stu-id="98019-120">See Also</span></span>


[<span data-ttu-id="98019-121">Развертывание конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98019-121">Deploying conferencing in Lync Server 2013</span></span>](lync-server-2013-deploying-conferencing.md)  
  

<span data-ttu-id="98019-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98019-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

