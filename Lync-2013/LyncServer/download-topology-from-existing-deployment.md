---
title: загрузка топологии из существующего развертывания;
description: Загрузка топологии из существующего развертывания.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Download topology from existing deployment
ms:assetid: e39065a2-d4b0-4f27-8c49-f56be78fa55b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721913(v=OCS.15)
ms:contentKeyID: 49733847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c22d746f8faf3fdf14a44e751eeb3c88bf3eef4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398791"
---
# <a name="download-topology-from-existing-deployment"></a><span data-ttu-id="2b3fc-103">загрузка топологии из существующего развертывания;</span><span class="sxs-lookup"><span data-stu-id="2b3fc-103">Download topology from existing deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b3fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b3fc-104">

<span> </span></span></span>

<span data-ttu-id="2b3fc-105">_**Тема последнего изменения:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="2b3fc-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="2b3fc-106">При создании пула Lync Server 2013 вы будете использовать хранилище Central Management, связанное с Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-106">When creating a Lync Server 2013 pool, you will use the Central Management Store that is associated with Lync Server 2010.</span></span> <span data-ttu-id="2b3fc-107">Когда вы запускаете построитель топологии при первом использовании и последующих сеансах редактирования, вам будет предложено указать расположение, в которое построитель топологии должен загрузить текущий документ конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-107">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="2b3fc-108">Так как вы уже определили топологию Lync Server 2010 и установили хранилище Central Management, необходимо выбрать загрузку топологии из существующего развертывания.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-108">Because you already have a Lync Server 2010 topology defined and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="2b3fc-109">Построитель топологии будет считывать базу данных и получать текущее определение.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-109">Topology Builder will read the database and retrieve the current definition.</span></span>

<span data-ttu-id="2b3fc-110">**Загрузка топологии из существующего развертывания**</span><span class="sxs-lookup"><span data-stu-id="2b3fc-110">**To download a topology from an existing deployment**</span></span>

1.  <span data-ttu-id="2b3fc-111">Запустите **Мастер развертывания Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-111">Open the **Lync Server Deployment Wizard**.</span></span>

2.  <span data-ttu-id="2b3fc-112">На странице **мастера развертывания Lync Server 2013 —** **Установка средств администрирования**.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-112">From the **Lync Server 2013 – Deployment Wizard** page, click **Install Administrative Tools**.</span></span>

3.  <span data-ttu-id="2b3fc-113">Запустить построитель топологии: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-113">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013** , and then click **Lync Server Topology Builder**.</span></span>

4.  <span data-ttu-id="2b3fc-114">Выберите пункт **топология скачивания из существующего развертывания**.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-114">Select **Download Topology from existing deployment**.</span></span>
    
    <span data-ttu-id="2b3fc-115">![Параметры Topology Builder мастера развертывания](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "Параметры Topology Builder мастера развертывания")</span><span class="sxs-lookup"><span data-stu-id="2b3fc-115">![Deployment Wizard Topology Builder settings](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "Deployment Wizard Topology Builder settings")</span></span>

5.  <span data-ttu-id="2b3fc-116">Выберите имя файла и сохраните топологию с типом файла Default. tbxml.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-116">Choose a file name and save the topology with the default .tbxml file type.</span></span>

6.  <span data-ttu-id="2b3fc-117">Разверните узел Lync Server, как показано на рисунке, чтобы показать различные роли сервера в развертывании.</span><span class="sxs-lookup"><span data-stu-id="2b3fc-117">Expand the Lync Server node, as shown, to reveal the various server roles in the deployment.</span></span>
    
    <span data-ttu-id="2b3fc-118">![Общие свойства роли сервера построителя топологии](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "Общие свойства роли сервера построителя топологии")</span><span class="sxs-lookup"><span data-stu-id="2b3fc-118">![Topology Builder server role general properties](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "Topology Builder server role general properties")</span></span>

<span data-ttu-id="2b3fc-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b3fc-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

