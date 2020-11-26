---
title: Удалить BackCompatSite
description: Удалите BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440305"
---
# <a name="remove-backcompatsite"></a><span data-ttu-id="7370f-103">Удалить BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="7370f-103">Remove BackCompatSite</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7370f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7370f-104">

<span> </span></span></span>

<span data-ttu-id="7370f-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="7370f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="7370f-106">После деактивации всех пулов и удаления всех пограничных серверов запустите мастер слияния построителя топологии, чтобы удалить **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="7370f-106">After all pools are deactivated and all Edge Servers have been uninstalled, run the Topology Builder Merge wizard to remove the **BackCompatSite**.</span></span>

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a><span data-ttu-id="7370f-107">Удаление несовместимого веб-сайта из построителя топологии</span><span class="sxs-lookup"><span data-stu-id="7370f-107">To remove BackCompat site from Topology Builder</span></span>

1.  <span data-ttu-id="7370f-108">Откройте существующее развертывание в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="7370f-108">Open an existing deployment from Topology Builder.</span></span>

2.  <span data-ttu-id="7370f-109">В меню **действия** выберите пункт **топология слиянием 2007 R2**.</span><span class="sxs-lookup"><span data-stu-id="7370f-109">In the **Action** menu, click **Merge 2007 R2 Topology**.</span></span>

3.  <span data-ttu-id="7370f-110">Для продолжения нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7370f-110">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="7370f-111">Убедитесь, что на странице **Определение устаревшего** пограничного сервера установлен пустой список пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="7370f-111">On the **Specify Legacy Edge** page, ensure that list of Edge Servers is empty.</span></span> <span data-ttu-id="7370f-112">Если список не пуст, удалите все старые пограничные серверы с помощью кнопки " **Удалить** ", а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7370f-112">If the list is not empty, use the **Remove** button to remove all the legacy Edge Servers, and then click **Next**.</span></span>
    
    <span data-ttu-id="7370f-113">![Мастер топологии слиянием, задание страницы настройки ребра](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Мастер топологии слиянием, задание страницы настройки ребра")</span><span class="sxs-lookup"><span data-stu-id="7370f-113">![Merge Topology Wizard, Specify Edge Setup page](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="7370f-114">На странице **Определение параметров внутреннего порта SIP** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7370f-114">On the **Specify Internal SIP port setting** page, click **Next**.</span></span>

6.  <span data-ttu-id="7370f-115">На странице **Сводка** нажмите кнопку **Далее** , чтобы начать объединение топологий для удаления устаревшего сайта.</span><span class="sxs-lookup"><span data-stu-id="7370f-115">On the **Summary** page, click **Next** to begin merging the topologies to remove the legacy site.</span></span>

7.  <span data-ttu-id="7370f-116">В столбце **Status (состояние** ) убедитесь, что значение установлено **успешно** , и нажмите кнопку **Готово** , чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="7370f-116">In the **Status** column, verify that the value is **Success** and then click **Finish** to close the wizard.</span></span>

8.  <span data-ttu-id="7370f-117">На левой панели построителя топологии разверните узел BackCompatSite и убедитесь, что серверы не указаны в списке.</span><span class="sxs-lookup"><span data-stu-id="7370f-117">In the left pane of Topology Builder, expand the BackCompatSite and ensure no servers are listed.</span></span>

9.  <span data-ttu-id="7370f-118">Щелкните **BackCompatSite** правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="7370f-118">Right-click the **BackCompatSite**, and then click **Delete**.</span></span>

10. <span data-ttu-id="7370f-119">В **построителе топологии** выберите самый верхний узел **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="7370f-119">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

11. <span data-ttu-id="7370f-120">В меню **действие** выберите пункт **топология публикации** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7370f-120">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

12. <span data-ttu-id="7370f-121">После завершения работы **мастера публикации** нажмите кнопку **Готово** , чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="7370f-121">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<span data-ttu-id="7370f-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7370f-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

