---
title: 'Lync Server 2013: настройка хранилища файлов'
description: 'Lync Server 2013: Настройка хранилища файлов DFS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DFS file storage
ms:assetid: a985be20-5a00-4f38-b45b-83dc82de3827
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205150(v=OCS.15)
ms:contentKeyID: 48185037
ms.date: 05/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d70ae93db188ec51d04dd33d6c3cb5659db5a2c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399934"
---
# <a name="configure-dfs-file-storage-for-lync-server-2013"></a><span data-ttu-id="eded7-103">Настройка хранилища файлов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eded7-103">Configure DFS file storage for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eded7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eded7-104">

<span> </span></span></span>

<span data-ttu-id="eded7-105">_**Тема последнего изменения:** 2016-05-23_</span><span class="sxs-lookup"><span data-stu-id="eded7-105">_**Topic Last Modified:** 2016-05-23_</span></span>

<span data-ttu-id="eded7-106">Lync Server 2013 поддерживает использование общих файловых ресурсов в распределенной файловой системе (DFS).</span><span class="sxs-lookup"><span data-stu-id="eded7-106">Lync Server 2013 supports using file shares on a Distributed File System (DFS).</span></span> <span data-ttu-id="eded7-107">Подробные сведения о DFS для Windows Server 2008 можно найти в пошаговом руководстве по DFS для Windows Server 2008 по адресу [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) . Для использования DFS сервер Lync Server 2013 должен выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="eded7-107">For details about DFS for Windows Server 2008, see the DFS Step-by-Step Guide for Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835).To use a DFS, Lync Server 2013 requires the following:</span></span>

  - <span data-ttu-id="eded7-108">Пространства имен основываются на доменах</span><span class="sxs-lookup"><span data-stu-id="eded7-108">Namespaces are domain based</span></span>

  - <span data-ttu-id="eded7-109">На всех серверах пространства имен установлен минимум Windows 2008</span><span class="sxs-lookup"><span data-stu-id="eded7-109">All namespace servers are running a minimum of Windows 2008</span></span>

<span data-ttu-id="eded7-110">Для установки Lync Server 2013 необходимо, чтобы разрешение на доступ к общей папке было разрешено администратору.</span><span class="sxs-lookup"><span data-stu-id="eded7-110">Lync Server 2013 setup requires that permissions on shared folder allow full access to Administrator.</span></span> <span data-ttu-id="eded7-111">В этом случае Lync Server 2013 будет использовать разрешения на доступ к файлам NTFS для папок ACL.</span><span class="sxs-lookup"><span data-stu-id="eded7-111">Lync Server 2013 will then use NTFS file permissions to ACL the folders.</span></span> <span data-ttu-id="eded7-112">Унаследованные разрешения для общего доступа к DFS не будут использоваться для ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="eded7-112">Inherited DFS share permissions will not be used to restrict access.</span></span>

<span data-ttu-id="eded7-113">Дополнительные сведения о требованиях к общему доступу можно найти [в разделе Поддержка хранения файлов в Lync Server 2013](lync-server-2013-file-storage-support.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="eded7-113">For more details about File Share requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md) in the Supportability documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="eded7-114">Возможно, вы ищете информацию о настройке общего доступа к сети, не относящейся к DFS.</span><span class="sxs-lookup"><span data-stu-id="eded7-114">You may be looking for information on configuring a non-DFS share.</span></span> <span data-ttu-id="eded7-115">Если это так, изучите <A href="lync-server-2013-hardware-setup.md">настройку оборудования для Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="eded7-115">If so, check out <A href="lync-server-2013-hardware-setup.md">Hardware setup for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="eded7-116">Ниже описано, как правильно настроить разрешения на доступ к общей папке с помощью мастера пространства имен DFS (как описано в руководстве по настройке DFS).</span><span class="sxs-lookup"><span data-stu-id="eded7-116">The following procedure describes how to correctly configure shared folder permissions using the DFS Namespace Wizard (as described in DFS setup guide).</span></span>

<div>

## <a name="to-configure-shared-folder-permissions"></a><span data-ttu-id="eded7-117">Настройка разрешений для общей папки</span><span class="sxs-lookup"><span data-stu-id="eded7-117">To configure shared folder permissions</span></span>

1.  <span data-ttu-id="eded7-118">Нажмите кнопку **Пуск**, наведите указатель на пункт **все программы**, выберите **Администрирование**, а затем — **Управление DFS**.</span><span class="sxs-lookup"><span data-stu-id="eded7-118">Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **DFS Management**.</span></span>

2.  <span data-ttu-id="eded7-119">В дереве консоли оснастки управления DFS щелкните правой кнопкой мыши сервер пространства имен (например, filesrv1.contoso.com), а затем выберите команду **изменить параметры**.</span><span class="sxs-lookup"><span data-stu-id="eded7-119">In the console tree of the DFS Management snap-in, right-click the namespace server (for example filesrv1.contoso.com), and then click **Edit Settings**.</span></span>

3.  <span data-ttu-id="eded7-120">Выберите **разрешения для общей папки**.</span><span class="sxs-lookup"><span data-stu-id="eded7-120">Select **Shared Folder Permissions**.</span></span>

4.  <span data-ttu-id="eded7-121">Выберите **использовать пользовательские разрешения**.</span><span class="sxs-lookup"><span data-stu-id="eded7-121">Select **Use Custom Permissions**.</span></span>

5.  <span data-ttu-id="eded7-122">Для группы администраторов выберите в разделе **разрешено** следующее:</span><span class="sxs-lookup"><span data-stu-id="eded7-122">For the Administrator group, select the following under **Allow**:</span></span>
    
      - <span data-ttu-id="eded7-123">**Полный доступ**</span><span class="sxs-lookup"><span data-stu-id="eded7-123">**Full Control**</span></span>
    
      - <span data-ttu-id="eded7-124">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="eded7-124">**Change**</span></span>
    
      - <span data-ttu-id="eded7-125">**Читаются**</span><span class="sxs-lookup"><span data-stu-id="eded7-125">**Read**</span></span>

6.  <span data-ttu-id="eded7-126">Нажмите кнопку **Применить**, а затем — кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="eded7-126">Click **Apply**, and then click **OK**.</span></span>

<span data-ttu-id="eded7-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eded7-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

