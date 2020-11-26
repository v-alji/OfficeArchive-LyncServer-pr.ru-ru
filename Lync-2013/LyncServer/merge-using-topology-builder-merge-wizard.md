---
title: Слияние с помощью мастера слияния построителя топологии
description: Слияние с помощью мастера слияния построителя топологии.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Merge using Topology Builder Merge wizard
ms:assetid: c3f3c425-dab6-4dcd-bf0e-d7fde05f2ebf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205243(v=OCS.15)
ms:contentKeyID: 48185343
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d71a63eef95e3e36802dedfa9fbc1a173d283b65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446952"
---
# <a name="merge-using-topology-builder-merge-wizard"></a><span data-ttu-id="aaf76-103">Слияние с помощью мастера слияния построителя топологии</span><span class="sxs-lookup"><span data-stu-id="aaf76-103">Merge using Topology Builder Merge wizard</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aaf76-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aaf76-104">

<span> </span></span></span>

<span data-ttu-id="aaf76-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="aaf76-105">_**Topic Last Modified:** 2012-10-02_</span></span>

1.  <span data-ttu-id="aaf76-106">Скачайте существующее развертывание с помощью Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="aaf76-106">Download the existing deployment using Topology Builder.</span></span>

2.  <span data-ttu-id="aaf76-107">В меню " **действия** " выберите команду " **Слияние Office Communications Server 2007 R2**".</span><span class="sxs-lookup"><span data-stu-id="aaf76-107">From the **Action** menu, select **Merge Office Communications Server 2007 R2**.</span></span>

3.  <span data-ttu-id="aaf76-108">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-108">Click **Next**.</span></span>

4.  <span data-ttu-id="aaf76-109">В окне **задать параметры ребра** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-109">In **Specify Edge Setup**, click **Add**.</span></span>
    
    <span data-ttu-id="aaf76-110">![Мастер топологии слиянием, задание страницы настройки ребра](images/JJ205243.cdca609d-d4d5-47d9-9ff8-8b1daa4106e1(OCS.15).jpg "Мастер топологии слиянием, задание страницы настройки ребра")</span><span class="sxs-lookup"><span data-stu-id="aaf76-110">![Merge Topology Wizard, Specify Edge Setup page](images/JJ205243.cdca609d-d4d5-47d9-9ff8-8b1daa4106e1(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="aaf76-111">В поле **Укажите тип ребра** введите тип конфигурации пограничного сервера и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-111">In **Specify Edge Type**, enter the type of Edge Server configuration, and then click **Next**.</span></span> <span data-ttu-id="aaf76-112">В этом примере используется **один из вариантов пограничного сервера** .</span><span class="sxs-lookup"><span data-stu-id="aaf76-112">This example uses the **Single Edge Server** option.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="aaf76-113"><STRONG>Развернутое развертывание пограничного сервера</STRONG> не является поддерживаемой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="aaf76-113"><STRONG>Expanded Edge deployment</STRONG> is not a supported configuration.</span></span> <span data-ttu-id="aaf76-114"><STRONG>Развернутый сервер пограничного сервера</STRONG> должен сначала быть преобразован в <STRONG>однограничный сервер</STRONG> или <STRONG>Объединенный граничный сервер с балансировкой нагрузки</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="aaf76-114">An <STRONG>Expanded Edge Server</STRONG> must first be converted to a <STRONG>Single Edge Server</STRONG> or a <STRONG>Load-balanced consolidated Edge</STRONG> Server.</span></span>

    
    </div>

6.  <span data-ttu-id="aaf76-115">В разделе **Настройка параметров внутреннего края** введите нужные сведения о ВНУТРЕННЕМ полном доменном имени и портах пограничного пула и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-115">In **Specify Internal Edge Settings** , enter the relevant information for your Edge pool’s internal FQDN and ports as needed, and then click **Next**.</span></span>
    
    <span data-ttu-id="aaf76-116">![Диалоговое окно "Настройка параметров внутренней границы"](images/JJ205243.dd664761-839c-4ac8-bd1a-5525589dfbb0(OCS.15).jpg "Диалоговое окно "Настройка параметров внутренней границы"")</span><span class="sxs-lookup"><span data-stu-id="aaf76-116">![Specify Internal Edge Settings dialog](images/JJ205243.dd664761-839c-4ac8-bd1a-5525589dfbb0(OCS.15).jpg "Specify Internal Edge Settings dialog")</span></span>  

7.  <span data-ttu-id="aaf76-117">В поле **задать внешний край** введите сведения о полном доменном имени для веб-конференций для пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf76-117">In **Specify External Edge**, enter the web conferencing FQDN information for your Edge Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="aaf76-118">Прежде чем нажать кнопку <STRONG>Далее</STRONG>, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="aaf76-118">Before you click <STRONG>Next</STRONG>, do the next step in this procedure.</span></span> <span data-ttu-id="aaf76-119">Очень важно, чтобы вы не пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="aaf76-119">It is very important that you do not miss this step.</span></span>

    
    </div>

8.  <span data-ttu-id="aaf76-120">Если вы планируете использовать устаревший сервер Office Communications Server 2007 R2 для Федерации, установите флажок **этот пул пограничного сервера используется для подключения к службам федерации и общедоступного обмена мгновенными сообщениями** .</span><span class="sxs-lookup"><span data-stu-id="aaf76-120">Check the **This Edge pool is used for federation and public IM connectivity** check box if you plan to use the legacy Office Communications Server 2007 R2 Edge Server for federation.</span></span> <span data-ttu-id="aaf76-121">Если вы развернули несколько пограничных серверов, для Федерации будут включены только один из них.</span><span class="sxs-lookup"><span data-stu-id="aaf76-121">If you have multiple Edge Servers deployed, only one of them will be enabled for federation.</span></span> <span data-ttu-id="aaf76-122">Если вы не установите этот флажок, и вы решите, что вы хотите включить федерацию, необходимо запустить мастер слияния построителя топологии и повторно опубликовать свою топологию.</span><span class="sxs-lookup"><span data-stu-id="aaf76-122">If you do not check this box and you decide later that you want to enable federation, you must run the Topology Builder Merge wizard and publish your topology again.</span></span>
    
    <span data-ttu-id="aaf76-123">![Диалоговое окно пограничного сервера, укажите внешний край страницы](images/JJ205243.32e97ce5-92f0-477e-8125-5d2ece237b13(OCS.15).jpg "Диалоговое окно пограничного сервера, укажите внешний край страницы")</span><span class="sxs-lookup"><span data-stu-id="aaf76-123">![Edge Server dialog, Specify External Edge page](images/JJ205243.32e97ce5-92f0-477e-8125-5d2ece237b13(OCS.15).jpg "Edge Server dialog, Specify External Edge page")</span></span>  

9.  <span data-ttu-id="aaf76-124">В поле **Укажите следующий прыжок** введите полное доменное имя (FQDN) для расположения следующего прыжка в среде.</span><span class="sxs-lookup"><span data-stu-id="aaf76-124">In **Specify Next Hop**, enter the fully qualified domain name (FQDN) of the next hop location in your environment.</span></span> <span data-ttu-id="aaf76-125">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-125">Click **Finish**.</span></span>
    
    <span data-ttu-id="aaf76-126">![Диалоговое окно пограничного сервера с указанием следующей страницы перехода](images/JJ205243.e734ee0d-f91c-4f3f-8ae6-248ecabcf678(OCS.15).jpg "Диалоговое окно пограничного сервера с указанием следующей страницы перехода")</span><span class="sxs-lookup"><span data-stu-id="aaf76-126">![Edge Server dialog, Specify Next Hop page](images/JJ205243.e734ee0d-f91c-4f3f-8ae6-248ecabcf678(OCS.15).jpg "Edge Server dialog, Specify Next Hop page")</span></span>  

10. <span data-ttu-id="aaf76-127">В окне **Настройка параметров Edge**, если все серверы Office Communications Server 2007 R2 были добавлены, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-127">In **Specify Edge Setup**, if all your Office Communications Server 2007 R2 Edge Servers have been added, click **Next**.</span></span> <span data-ttu-id="aaf76-128">Если у вас еще есть дополнительные серверы Office Communications Server 2007 R2, повторите эту процедуру, начиная с шага 4.</span><span class="sxs-lookup"><span data-stu-id="aaf76-128">If you have more Office Communications Server 2007 R2 Edge Servers to add, repeat this procedure starting at step 4.</span></span>

11. <span data-ttu-id="aaf76-129">В поле **задать внутренний порт SIP** выберите значение по умолчанию (то есть, если вы не изменили порт SIP по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="aaf76-129">In **Specify Internal SIP port** , select the default setting (that is, if you did not modify the default SIP port).</span></span> <span data-ttu-id="aaf76-130">Внесите необходимые изменения, если вы не используете порт по умолчанию 5061, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-130">Change as appropriate if you are not using a default port of 5061, and then click **Next**.</span></span>

12. <span data-ttu-id="aaf76-131">В разделе **Сводка** нажмите кнопку **Далее** , чтобы начать объединение топологий.</span><span class="sxs-lookup"><span data-stu-id="aaf76-131">In **Summary**, click **Next** to begin merging the topologies.</span></span>

13. <span data-ttu-id="aaf76-132">На странице мастера проверяются успешные слияния топологий.</span><span class="sxs-lookup"><span data-stu-id="aaf76-132">The wizard page verifies that the merging of the topologies was successful.</span></span>

14. <span data-ttu-id="aaf76-133">В столбце **Status (состояние** ) убедитесь, что значение **успешно**, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-133">In the **Status** column, verify that the value is **Success**, and then click **Finish**.</span></span>

15. <span data-ttu-id="aaf76-134">На левой панели построителя топологии вы должны увидеть **BackCompatSite**, указывающий на то, что ваша среда Office Communications Server 2007 R2 была объединена с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf76-134">In the left pane of Topology Builder, you should now see the **BackCompatSite**, which indicates that your Office Communications Server 2007 R2 environment has been merged with Lync Server 2013.</span></span>
    
    <span data-ttu-id="aaf76-135">![Построитель топологии, демонстрирующий объединенную топологию](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Построитель топологии, демонстрирующий объединенную топологию")</span><span class="sxs-lookup"><span data-stu-id="aaf76-135">![Topology Builder showing a merged topology](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder showing a merged topology")</span></span>  

16. <span data-ttu-id="aaf76-136">В меню **действие** выберите пункт **топология публикации** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-136">From the **Action** menu, click **Publish Topology**, and then click **Next**.</span></span>

17. <span data-ttu-id="aaf76-137">После завершения работы **мастера публикации** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="aaf76-137">When the **Publishing wizard** completes, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="aaf76-138">Важно выполнить следующую тему, <A href="import-policies-and-settings.md">импортировать политики и параметры</A>, чтобы убедиться в том, что устаревшие параметры политики импортированы в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf76-138">It’s important that you complete the next topic, <A href="import-policies-and-settings.md">Import policies and settings</A>, to ensure that the legacy policy settings are imported into Lync Server 2013.</span></span>

    
    <span data-ttu-id="aaf76-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aaf76-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

