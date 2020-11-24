---
title: 'Lync Server 2013: публикация топологии'
description: 'Lync Server 2013: публикация топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish your topology
ms:assetid: bfed3829-7a54-4b5c-a7cb-28871acd35e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412935(v=OCS.15)
ms:contentKeyID: 48185287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4d27d2d3644eb1f174e2f3fab47197f2c122a97
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399037"
---
# <a name="publish-your-topology-in-lync-server-2013"></a><span data-ttu-id="91eca-103">Публикация топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91eca-103">Publish your topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91eca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91eca-104">

<span> </span></span></span>

<span data-ttu-id="91eca-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="91eca-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="91eca-106">Каждый раз, когда вы используете Topology Builder для построения топологии, необходимо опубликовать топологию в базе данных в хранилище Центрального управления, чтобы эти данные можно было использовать для развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="91eca-106">Each time you use Topology Builder to build your topology, you must publish the topology to a database in the Central Management store so that the data can be used to deploy Lync Server 2013.</span></span> <span data-ttu-id="91eca-107">Чтобы опубликовать топологию, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="91eca-107">Use the following procedure to publish your topology.</span></span>

<div>

## <a name="to-publish-the-topology"></a><span data-ttu-id="91eca-108">Публикация топологии</span><span class="sxs-lookup"><span data-stu-id="91eca-108">To publish the topology</span></span>

1.  <span data-ttu-id="91eca-109">Запустить построитель топологии: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="91eca-109">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="91eca-110">В построителе топологии в дереве консоли щелкните правой кнопкой мыши **Lync 2013** и выберите команду **топология публикации**.</span><span class="sxs-lookup"><span data-stu-id="91eca-110">In Topology Builder, in the console tree, right-click **Lync 2013**, and then click **Publish Topology**.</span></span>

3.  <span data-ttu-id="91eca-111">На странице **приветствия** в мастере нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="91eca-111">On the **Welcome** page of the wizard, click **Next**.</span></span>

4.  <span data-ttu-id="91eca-112">На странице **Topology Builder обнаружена страница хранилища CMS** , нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="91eca-112">On the **Topology Builder found a CMS store** page, click **Next**.</span></span>

5.  <span data-ttu-id="91eca-113">На странице **создания других баз данных** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="91eca-113">On the **Create other databases** page, click **Next**.</span></span>

6.  <span data-ttu-id="91eca-114">Когда состояние указывает на то, что создание базы данных прошло успешно, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="91eca-114">When the status indicates that database creation succeeded, do the following:</span></span>
    
      - <span data-ttu-id="91eca-115">Для просмотра журнала нажмите кнопку **Просмотреть журнал**.</span><span class="sxs-lookup"><span data-stu-id="91eca-115">To view the log, click **View log**.</span></span>
    
      - <span data-ttu-id="91eca-116">Для завершения работы мастера нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="91eca-116">To close the wizard, click **Finish**.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="91eca-117">Если это новая установка пограничного сервера или пула EDGE, необходимо экспортировать конфигурацию пограничного сервера на существующем сервере переднего плана, пуле переднего плана или стандартном сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="91eca-117">If this is a new installation of an Edge Server or Edge pool, you must export the Edge Server configuration from an existing Front End Server, Front End pool, or Standard Edition server.</span></span> <span data-ttu-id="91eca-118">Для экспорта конфигурации ознакомьтесь со <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">сведениями о том, как экспортировать топологию Lync Server 2013 и скопировать ее на внешние носители для установки пограничного сервера</A>.</span><span class="sxs-lookup"><span data-stu-id="91eca-118">To export the configuration, see <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A>.</span></span> <span data-ttu-id="91eca-119">Вы будете импортировать файл конфигурации из внешнего носителя или сетевого общего доступа на этапе настройки и развертывания пограничных серверов с помощью мастера развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91eca-119">You will import the configuration file from the external media or network share during the setup and deployment phase of the Edge Servers through the Lync Server Deployment Wizard.</span></span><BR><span data-ttu-id="91eca-120">После того как пограничные серверы будут работоспособны, а локальная база данных хранится в локальной конфигурации, последующие обновления конфигурации Lync Server 2013 будут опубликованы и реплицированы на пограничные серверы.</span><span class="sxs-lookup"><span data-stu-id="91eca-120">Once the Edge Servers are operational and the local configuration management store database is replicating with the internal deployment, subsequent updates to the Lync Server 2013 configuration will be published and replicated to the Edge Servers.</span></span>

        
        <span data-ttu-id="91eca-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91eca-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

