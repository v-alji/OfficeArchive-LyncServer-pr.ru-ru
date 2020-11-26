---
title: Проверка выполнения пользовательской репликации
description: Проверка того, что репликация пользователей завершена.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify user replication has completed
ms:assetid: 119e9896-45e5-4f8b-af43-7b09360ada0b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204680(v=OCS.15)
ms:contentKeyID: 48183441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 60bca44fcce811c29b1633bd4d3a39f832851885
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446074"
---
# <a name="verify-user-replication-has-completed"></a><span data-ttu-id="7d336-103">Проверка выполнения пользовательской репликации</span><span class="sxs-lookup"><span data-stu-id="7d336-103">Verify user replication has completed</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d336-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d336-104">

<span> </span></span></span>

<span data-ttu-id="7d336-105">_**Тема последнего изменения:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="7d336-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="7d336-106">При запуске командлета **Move-CsUser** может возникнуть сбой из-за того, что сведения о пользователе между доменными службами Active Directory (AD DS) и базами данных Lync Server 2013 не синхронизованы, так как начальная репликация не завершена.</span><span class="sxs-lookup"><span data-stu-id="7d336-106">When running the **Move-CsUser** cmdlet, you may experience a failure because user information between Active Directory Domain Services (AD DS) and the Lync Server 2013 databases are out of sync because the initial replication is incomplete.</span></span> <span data-ttu-id="7d336-107">Время, необходимое для успешного завершения начальной синхронизации службы репликации пользователей Lync Server 2013, зависит от количества контроллеров домена, размещенных в лесу Active Directory, на котором размещается пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7d336-107">The time it takes for the successful completion of the Lync Server 2013 User Replicator service's initial synchronization depends on the number of domain controllers that are hosted in the Active Directory forest that hosts the Lync Server 2013 pool.</span></span> <span data-ttu-id="7d336-108">Начальная синхронизация службы репликатора пользователей Lync Server 2013 происходит при первом запуске сервера переднего плана Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7d336-108">The Lync Server 2013 User Replicator service initial synchronization process occurs when the Lync Server 2013 Front End Server is started for the first time.</span></span> <span data-ttu-id="7d336-109">После этого синхронизация будет основана на интервале репликатора пользователей.</span><span class="sxs-lookup"><span data-stu-id="7d336-109">After that, the synchronization is then based on the User Replicator interval.</span></span> <span data-ttu-id="7d336-110">Выполните описанные ниже действия, чтобы убедиться, что репликация пользователей завершилась, прежде чем запускать командлет **Move-CsUser** .</span><span class="sxs-lookup"><span data-stu-id="7d336-110">Complete the following steps to verify user replication has completed before running the **Move-CsUser** cmdlet.</span></span>

<div>

## <a name="to-verify-user-replication-has-completed"></a><span data-ttu-id="7d336-111">Проверка завершения репликации пользователя</span><span class="sxs-lookup"><span data-stu-id="7d336-111">To verify user replication has completed</span></span>

1.  <span data-ttu-id="7d336-112">Войдите на компьютер, где установлен построитель топологий, с использованием учетной записи, входящей в группу администраторов домена и группу RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="7d336-112">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="7d336-113">Откройте меню **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="7d336-113">Click the **Start** menu, and then click **Run**.</span></span>

3.  <span data-ttu-id="7d336-114">Введите **eventvwr.exe** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7d336-114">Enter **eventvwr.exe** and then click **OK**.</span></span>

4.  <span data-ttu-id="7d336-115">В окне просмотра событий щелкните **журналы приложений и служб** , чтобы развернуть его, а затем выберите Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7d336-115">In Event Viewer, click **Applications and Services logs** to expand it, and then select Lync Server.</span></span>

5.  <span data-ttu-id="7d336-116">В области **действия** щелкните **фильтр текущего журнала**.</span><span class="sxs-lookup"><span data-stu-id="7d336-116">In the **Actions** pane click **Filter Current Log**.</span></span>

6.  <span data-ttu-id="7d336-117">В списке **источники событий** выберите пункт **репликатор пользователей Ls**.</span><span class="sxs-lookup"><span data-stu-id="7d336-117">From the **Event sources** list, click **LS User Replicator**.</span></span>

7.  <span data-ttu-id="7d336-118">В **\<All Event IDs\>** введите **30024** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7d336-118">In **\<All Event IDs\>** enter **30024** and then click **OK**.</span></span>

8.  <span data-ttu-id="7d336-119">В списке отфильтрованных событий на вкладке **Общие** найдите запись, в которой указано, что репликация пользователей успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="7d336-119">In the filtered events list, on the **General** tab, look for an entry that states user replication has completed successfully.</span></span>

<span data-ttu-id="7d336-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d336-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

