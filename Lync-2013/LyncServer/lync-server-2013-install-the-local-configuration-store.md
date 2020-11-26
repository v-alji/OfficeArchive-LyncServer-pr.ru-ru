---
title: 'Lync Server 2013: установка локального хранилища конфигурации'
description: 'Lync Server 2013: установите локальное хранилище конфигураций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install the Local Configuration store
ms:assetid: b563030d-d338-411f-9611-28d5eb4b3238
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412874(v=OCS.15)
ms:contentKeyID: 48185180
ms.date: 06/28/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bbf603704a8e1bdfbe71e0a9b064013d57bceda7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427140"
---
# <a name="install-the-local-configuration-store-in-lync-server-2013"></a><span data-ttu-id="1cbf5-103">Установка локального хранилища конфигурации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cbf5-103">Install the Local Configuration store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1cbf5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1cbf5-104">

<span> </span></span></span>

<span data-ttu-id="1cbf5-105">_**Тема последнего изменения:** 2014-06-27_</span><span class="sxs-lookup"><span data-stu-id="1cbf5-105">_**Topic Last Modified:** 2014-06-27_</span></span>

<span data-ttu-id="1cbf5-106">Перед выполнением описанных ниже действий убедитесь, что вы выполнили вход на сервер с учетной записью пользователя домена, которая является и локальным администратором, и членом группы RTCUniversalReadOnlyAdmin.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-106">Before following these steps, make sure you’re logged onto the server with a domain user account that’s both a local administrator and a member of the RTCUniversalReadOnlyAdmin group.</span></span>

<span data-ttu-id="1cbf5-107">Для выполнения каких-либо действий с мастером развертывания Lync Server необходимо, чтобы локальное хранилище конфигурации существовало на сервере.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-107">To be able to do anything with the Lync Server Deployment Wizard, we need the Local Configuration store to exist on a server.</span></span> <span data-ttu-id="1cbf5-108">Локальное хранилище конфигурации — это копия хранилища центрального управления, предназначенная только для чтения, которая создается после локальной установки SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-108">The Local Configuration store is a read-only copy of the Central Management store, which gets created after the local installation of SQL Server Express.</span></span> <span data-ttu-id="1cbf5-109">Собственно центральное хранилище в базе данных SQL Server, установленной на сервере Standard Edition или на базе SQL Server Express, также добавляется в существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-109">The Central Management store itself is added to the existing SQL Server database installed on the Standard Edition server or SQL Server Express-based database.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1cbf5-110">Если вы еще не выпустили программу установки Lync Server 2013 на этом сервере, вам будет предложено указать диск и путь для установки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-110">If you haven’t run Lync Server 2013 setup on this server before, you’ll be prompted for a drive and path to install Lync Server 2013 to.</span></span> <span data-ttu-id="1cbf5-111">Это позволит установить на диск, отличный от системного, если это требуется в Организации, или если у вас есть проблемы с пространством.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-111">This will let you install to a drive other than the system drive, if your organization requires it, or if you have space concerns.</span></span> <span data-ttu-id="1cbf5-112">Вы можете просто изменить путь к расположению установочных файлов Lync Server в диалоговом окне Настройка на новый доступный диск.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-112">You can just change the installation location path for the Lync Server files in the Setup dialog box to a new, available drive.</span></span> <span data-ttu-id="1cbf5-113">Если вы установили файлы установки по этому пути, включая OCSCore.msi, остальные файлы Lync Server 2013 будут развернуты там же.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-113">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will deploy there as well.</span></span>



</div>

<div>

## <a name="to-install-the-local-configuration-store"></a><span data-ttu-id="1cbf5-114">Установка локального хранилища конфигурации</span><span class="sxs-lookup"><span data-stu-id="1cbf5-114">To install the Local Configuration store</span></span>

1.  <span data-ttu-id="1cbf5-115">На установочном носителе перейдите к \\ настройкам \\ amd64 \\Setup.exe и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-115">From your installation media, browse to \\setup\\amd64\\Setup.exe, and then click **OK**.</span></span>

2.  <span data-ttu-id="1cbf5-116">Если вам будет предложено установить распространяемый компонент Microsoft Visual C++ 2012, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-116">If you’re prompted to install the Microsoft Visual C++ 2012 Redistributable, click **Yes**.</span></span>

3.  <span data-ttu-id="1cbf5-117">На странице **Lync Server 2013 (место установки** ) нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-117">On the **Lync Server 2013 Installation Location** page, click **OK**.</span></span>

4.  <span data-ttu-id="1cbf5-118">На странице Лицензионное **соглашение конечного пользователя** ознакомьтесь с условиями лицензионного соглашения, необходимо выбрать параметр **я принимаю условия лицензионного соглашения**, а затем нажать кнопку **ОК** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-118">On the **End User License Agreement** page, review the license terms, you’ll need to select **I accept the terms in the license agreement**, and then click **OK** to be able to continue.</span></span>

5.  <span data-ttu-id="1cbf5-119">На странице мастера развертывания щелкните ссылку **Установка или обновление системы Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-119">On the Deployment Wizard page, click **Install or Update Lync Server System**.</span></span>

6.  <span data-ttu-id="1cbf5-120">На странице **Lync Server 2013** рядом с **Step1: установите локальное хранилище конфигураций**, нажмите кнопку **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-120">On the **Lync Server 2013** page, next to **Step1: Install Local Configuration Store**, click **Run**.</span></span>

7.  <span data-ttu-id="1cbf5-121">На странице **Установка локального хранилища конфигурации** установите флажок **Получить непосредственно из центрального хранилища управления** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-121">On the **Install Local Configuration Store** page, make sure that the **Retrieve directly from the Central Management store** option is selected, and then click **Next**.</span></span>

8.  <span data-ttu-id="1cbf5-122">После завершения установки конфигурации локального сервера нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-122">When the local server configuration installation is complete, you should click **Finish**.</span></span>

<span data-ttu-id="1cbf5-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1cbf5-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

