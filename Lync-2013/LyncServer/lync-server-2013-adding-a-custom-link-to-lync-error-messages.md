---
title: 'Lync Server 2013: добавление настраиваемой ссылки в сообщения об ошибках Lync'
description: 'Lync Server 2013: Добавление настраиваемой ссылки на сообщения об ошибках Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding a custom link to Lync error messages
ms:assetid: de756088-fcc3-4e47-bde8-4fa4cc852fd1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398979(v=OCS.15)
ms:contentKeyID: 48185607
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a5d333b6f27e10e5092de23fcdf1d37fd75e75a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439284"
---
# <a name="adding-a-custom-link-to-lync-error-messages-in-lync-server-2013"></a><span data-ttu-id="0cebf-103">Добавление настраиваемой ссылки в сообщения об ошибках Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0cebf-103">Adding a custom link to Lync error messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0cebf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0cebf-104">

<span> </span></span></span>

<span data-ttu-id="0cebf-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="0cebf-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="0cebf-106">Настройка сообщений об ошибках Lync 2013 путем добавления ссылки на сведения о поиске и устранении неполадок в службе поддержки.</span><span class="sxs-lookup"><span data-stu-id="0cebf-106">Customize Lync 2013 error messages by adding a link to your own troubleshooting or help desk information.</span></span> <span data-ttu-id="0cebf-107">Для этого используйте командлеты командной консоли **New-CSClientPolicy** или **Set-CSClientPolicy** Lync Server с параметром CustomLinkInErrorMessages.</span><span class="sxs-lookup"><span data-stu-id="0cebf-107">To do this, use the **New-CSClientPolicy** or **Set-CSClientPolicy** Lync Server Management Shell cmdlets with the CustomLinkInErrorMessages parameter.</span></span> <span data-ttu-id="0cebf-108">Текст настраиваемой ссылки: "щелкните здесь, чтобы найти разделы поддержки от администратора", и его нельзя настроить.</span><span class="sxs-lookup"><span data-stu-id="0cebf-108">The text of the custom link is "Click here for support topics from your administrator," and it cannot be customized.</span></span>

<span data-ttu-id="0cebf-109">Например, следующая команда приводит к появлению настраиваемой ссылки в области сносок каждого сообщения об ошибке Lync 2013 и задает для конечной ссылки значение http://contoso.com/help/LyncHelpDesk.aspx:</span><span class="sxs-lookup"><span data-stu-id="0cebf-109">For example, the following command causes the custom link to appear in the footnote area of every Lync 2013 error message and sets the link destination to http://contoso.com/help/LyncHelpDesk.aspx:</span></span>

    New-CsClientPolicy -Identity LyncErrorLink -CustomLinkInErrorMessages "http://contoso/help/LyncHelpDesk.aspx"

<span data-ttu-id="0cebf-110">С помощью **Grant-CSClientPolicy** можно назначить пользователям новую политику.</span><span class="sxs-lookup"><span data-stu-id="0cebf-110">Use **Grant-CSClientPolicy** to assign this new policy to users.</span></span> <span data-ttu-id="0cebf-111">Подробные сведения можно найти в разделе **New-CSClientPolicy** и **Grant-CSClientPolicy** в документации по среде управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0cebf-111">For details, see **New-CSClientPolicy** and **Grant-CSClientPolicy** in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="0cebf-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0cebf-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

