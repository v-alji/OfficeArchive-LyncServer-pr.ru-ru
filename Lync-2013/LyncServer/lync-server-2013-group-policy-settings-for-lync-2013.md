---
title: 'Lync Server 2013: параметры групповой политики для Lync 2013'
description: 'Lync Server 2013: параметры групповой политики для Lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Policy settings for Lync 2013
ms:assetid: 5917a52b-dae0-4ec0-8548-a68dc20ab71c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204924(v=OCS.15)
ms:contentKeyID: 48184235
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c6f2b26fc19653b0098ed4775df1f9c8146986c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427784"
---
# <a name="group-policy-settings-for-lync-2013"></a><span data-ttu-id="a1026-103">Параметры групповой политики для Lync 2013</span><span class="sxs-lookup"><span data-stu-id="a1026-103">Group Policy settings for Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a1026-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a1026-104">

<span> </span></span></span>

<span data-ttu-id="a1026-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="a1026-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="a1026-106">В предыдущих версиях Lync и Office Communicator вы можете настроить параметры групповой политики клиента с помощью отдельного административного шаблона Communicator. adm.</span><span class="sxs-lookup"><span data-stu-id="a1026-106">In previous versions of Lync and Office Communicator, a stand-alone Communicator.adm administrative template was available for configuring client Group Policy settings.</span></span> <span data-ttu-id="a1026-107">Для Lync 2013 новые файлы административных шаблонов (ADMX и ADML) включаются вместе с административным шаблоном групповой политики Office.</span><span class="sxs-lookup"><span data-stu-id="a1026-107">For Lync 2013, new administrative template files (.admx and .adml files) are included along with the Office Group Policy Administrative Template.</span></span> <span data-ttu-id="a1026-108">Доступность файлов Lync 2013. ADMX и. ADML позволяет загружать шаблоны и централизованно управлять параметрами групповой политики для всех программ Office и языковых пакетов.</span><span class="sxs-lookup"><span data-stu-id="a1026-108">The availability of Lync 2013 .admx and .adml files allows you to download templates and centrally manage Group Policy settings for all your Office programs and language packs.</span></span> <span data-ttu-id="a1026-109">Подробные сведения можно найти в разделе "файлы административных шаблонов Office 2013 (ADMX, ADML)" в документации Office 2013 по адресу <https://go.microsoft.com/fwlink/p/?linkid=267516> .</span><span class="sxs-lookup"><span data-stu-id="a1026-109">For details, see “Office 2013 Administrative Template files (ADMX, ADML)” in the Office 2013 documentation at <https://go.microsoft.com/fwlink/p/?linkid=267516>.</span></span>

<div>

## <a name="client-bootstrapping-policies"></a><span data-ttu-id="a1026-110">Политики начальной загрузки клиента</span><span class="sxs-lookup"><span data-stu-id="a1026-110">Client Bootstrapping Policies</span></span>

<span data-ttu-id="a1026-111">Существует несколько политик начальной настройки клиентов, которые необходимо настроить, прежде чем пользователи будут впервые входить на сервер.</span><span class="sxs-lookup"><span data-stu-id="a1026-111">There are several client bootstrapping policies that you should configure before users sign in to the server for the first time.</span></span> <span data-ttu-id="a1026-112">Поскольку эти политики вступают в силу перед входом клиента и начинают получать параметры подготовки по каналу с сервера, вы можете настроить их с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="a1026-112">Because these policies take effect before the client signs in and begins receiving in-band provisioning settings from the server, you can use Group Policy to configure them.</span></span> <span data-ttu-id="a1026-113">Дополнительные сведения можно найти в разделе [Настройка политик начальной настройки клиента в Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="a1026-113">For more information, see [Configuring client bootstrapping policies in Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) in the Deployment documentation.</span></span>

<span data-ttu-id="a1026-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a1026-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

