---
title: 'Lync Server 2013: удаление подсетей сети'
description: 'Lync Server 2013: удаление подсетей сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network subnets
ms:assetid: c1850f38-40a3-48c9-b6f1-f181c5e63b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721873(v=OCS.15)
ms:contentKeyID: 49733806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6635ec99b68c4ceb10d1cda343fef35c951bf152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430282"
---
# <a name="deleting-network-subnets-in-lync-server-2013"></a><span data-ttu-id="0ab53-103">Удаление подсетей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ab53-103">Deleting network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ab53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ab53-104">

<span> </span></span></span>

<span data-ttu-id="0ab53-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0ab53-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0ab53-106">Для удаления подсети вы можете использовать описанную ниже процедуру.</span><span class="sxs-lookup"><span data-stu-id="0ab53-106">You can use the following procedure to delete a subnet.</span></span> <span data-ttu-id="0ab53-107">С помощью панели управления Lync Server вы можете создавать, изменять и удалять сетевые подсети.</span><span class="sxs-lookup"><span data-stu-id="0ab53-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="0ab53-108">Сведения о создании и изменении подсетей сети можно найти [в разделе Создание или изменение подсетей сети в Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="0ab53-108">For details on creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<span data-ttu-id="0ab53-109">В большинстве развертываний Microsoft Lync Server 2013 там, где реализовано управление допуском звонков (CAC), обычно это большое количество подсетей.</span><span class="sxs-lookup"><span data-stu-id="0ab53-109">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="0ab53-110">По этой причине лучше всего настроить подсети из командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0ab53-110">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="0ab53-111">Из него вы можете вызвать **New-CsNetworkSubnet** в сочетании с командлетом Windows PowerShell **Import-CSV**.</span><span class="sxs-lookup"><span data-stu-id="0ab53-111">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="0ab53-112">Используя эти командлеты вместе, вы можете прочитать параметры подсети из CSV-файла и одновременно создать несколько подсетей.</span><span class="sxs-lookup"><span data-stu-id="0ab53-112">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="0ab53-113">Примеры создания подсетей из CSV-файла можно найти в разделе [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="0ab53-113">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-delete-a-network-subnet"></a><span data-ttu-id="0ab53-114">Удаление сетевой подсети</span><span class="sxs-lookup"><span data-stu-id="0ab53-114">To delete a network subnet</span></span>

1.  <span data-ttu-id="0ab53-115">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="0ab53-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0ab53-116">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0ab53-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0ab53-117">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0ab53-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0ab53-118">На панели навигации слева выберите пункт **Настройка сети** , а затем — **подсеть**.</span><span class="sxs-lookup"><span data-stu-id="0ab53-118">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="0ab53-119">На странице **Subnet (подсеть** ) выберите подсеть, которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="0ab53-119">On the **Subnet** page, click the subnet that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0ab53-120">Вы можете удалить более одной подсети за один раз.</span><span class="sxs-lookup"><span data-stu-id="0ab53-120">You can delete more than one subnet at a time.</span></span> <span data-ttu-id="0ab53-121">Для этого нажмите клавишу CTRL и выберите несколько подсетей, удерживая нажатой клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="0ab53-121">To do this, press CTRL and select multiple subnets while holding down the CTRL key.</span></span> <span data-ttu-id="0ab53-122">Кроме того, чтобы выбрать все подсети, в меню <STRONG>Правка</STRONG> выберите команду <STRONG>выделить все</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="0ab53-122">Or, to select all subnets, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="0ab53-123">В меню **Правка** выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="0ab53-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="0ab53-124">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0ab53-124">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0ab53-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0ab53-125">See Also</span></span>


[<span data-ttu-id="0ab53-126">Создание и изменение подсетей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ab53-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
  

<span data-ttu-id="0ab53-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ab53-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

