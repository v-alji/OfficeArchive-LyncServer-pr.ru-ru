---
title: 'Lync Server 2013: для установка базы данных сервера Standard Edition'
description: 'Lync Server 2013: Установите стандартную базу данных сервера Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Standard Edition server database
ms:assetid: 0bd3a804-aad6-48cb-981b-54725af032db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398167(v=OCS.15)
ms:contentKeyID: 48183385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a20d2c01de94ad88960555db78c57c6b79d92f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427154"
---
# <a name="install-standard-edition-server-database-for-lync-server-2013"></a><span data-ttu-id="99fb3-103">Установка базы данных сервера Standard Edition для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99fb3-103">Install Standard Edition server database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99fb3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99fb3-104">

<span> </span></span></span>

<span data-ttu-id="99fb3-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="99fb3-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="99fb3-106">Настройка стандартного сервера выпусков в качестве единственного сервера в инфраструктуре, которой пользователи не отличаются от других установок сервера в том случае, если у вас есть выбор в **мастере развертывания** специально для настройки первоначального сервера.</span><span class="sxs-lookup"><span data-stu-id="99fb3-106">Setting up a Standard Edition server as the only server in your infrastructure that homes users differs from other server installations in that there is a selection in the **Deployment Wizard** specifically for setting up the initial server.</span></span>

<div>

## <a name="to-install-a-standard-edition-server"></a><span data-ttu-id="99fb3-107">Установка сервера Standard Edition</span><span class="sxs-lookup"><span data-stu-id="99fb3-107">To install a Standard Edition server</span></span>

1.  <span data-ttu-id="99fb3-108">Войдите на сервер, на котором вы собираетесь установить стандартный выпуск для локального администратора или эквивалент домена.</span><span class="sxs-lookup"><span data-stu-id="99fb3-108">Log on to the server where you are going to install Standard Edition server as a local administrator or a domain equivalent.</span></span>

2.  <span data-ttu-id="99fb3-109">Если вы не предготовили доменные службы Active Directory, сначала выполните эти действия.</span><span class="sxs-lookup"><span data-stu-id="99fb3-109">If you have not prepared Active Directory Domain Services, then first perform those procedures.</span></span> <span data-ttu-id="99fb3-110">Дополнительные сведения можно найти в разделе [Подготовка доменных служб Active Directory для Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="99fb3-110">For details, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

3.  <span data-ttu-id="99fb3-111">В мастере развертывания Lync Server нажмите кнопку **подготовить первый сервер Standard Edition**.</span><span class="sxs-lookup"><span data-stu-id="99fb3-111">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="99fb3-112">На странице **подготовить один стандартный выпуск на сервере** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="99fb3-112">On the **Prepare single Standard Edition Server** page, click **Next**.</span></span>

5.  <span data-ttu-id="99fb3-113">На странице **выполнение команд** сервер SQL Server 2012 Express установлен в качестве хранилища центрального управления.</span><span class="sxs-lookup"><span data-stu-id="99fb3-113">On the **Executing Commands** page, the SQL Server 2012 Express is installed as the Central Management store.</span></span> <span data-ttu-id="99fb3-114">Создаются необходимые правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="99fb3-114">Necessary firewall rules are created.</span></span> <span data-ttu-id="99fb3-115">После завершения установки базы данных и необходимого программного обеспечения нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="99fb3-115">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="99fb3-116">Начальная установка может занять некоторое время и не отменять заметные обновления экрана сводки вывода команды.</span><span class="sxs-lookup"><span data-stu-id="99fb3-116">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="99fb3-117">Это происходит из-за установки SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="99fb3-117">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="99fb3-118">Если вам нужно наблюдать за установкой базы данных, используйте диспетчер задач для наблюдения за настройкой.</span><span class="sxs-lookup"><span data-stu-id="99fb3-118">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

6.  <span data-ttu-id="99fb3-119">На странице мастера развертывания Lync Server щелкните **установить построитель топологии** , если вы ранее не установили средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="99fb3-119">On the Lync Server Deployment Wizard page, click **Install Topology Builder** if you have not previously installed the administrative tools.</span></span> <span data-ttu-id="99fb3-120">Подробности можно найти в разделе [Установка средств администрирования Lync Server 2013](lync-server-2013-install-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="99fb3-120">For details, see [Install Lync Server 2013 administrative tools](lync-server-2013-install-lync-server-administrative-tools.md).</span></span>

7.  <span data-ttu-id="99fb3-121">Убедитесь, что рядом с пунктом "Подготовка Active Directory" установлены зеленые галочки, "подготовить первый сервер Standard Edition" и "установить построитель топологии".</span><span class="sxs-lookup"><span data-stu-id="99fb3-121">Confirm that there are green check marks next to “Prepare Active Directory,” “Prepare first Standard Edition server,” and “Install Topology Builder.”</span></span>

<span data-ttu-id="99fb3-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99fb3-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

