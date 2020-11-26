---
title: 'Lync Server 2013: развертывание средства SEFAUtil'
description: 'Lync Server 2013: развертывание средства SEFAUtil.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy the SEFAUtil tool
ms:assetid: fb556e50-88dd-4404-a3d5-be36f5ba41e6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945659(v=OCS.15)
ms:contentKeyID: 51541534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 311f14f33dff30b388836a7f02483c4afe5da1b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430156"
---
# <a name="deploy-the-sefautil-tool-in-lync-server-2013"></a><span data-ttu-id="6b311-103">Deploy the SEFAUtil tool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b311-103">Deploy the SEFAUtil tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b311-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b311-104">

<span> </span></span></span>

<span data-ttu-id="6b311-105">_**Тема последнего изменения:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="6b311-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="6b311-106">Для развертывания и управления получением группового звонка необходимо использовать средство SEFAUtil Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="6b311-106">To deploy and manage Group Call Pickup, you need to use the SEFAUtil resource kit tool.</span></span> <span data-ttu-id="6b311-107">Это средство входит в состав набора средств для Lync Server 2013 Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="6b311-107">The tool is part of the Lync Server 2013 resource kit tools.</span></span> <span data-ttu-id="6b311-108">Прежде чем устанавливать SEFAUtil, необходимо иметь доверенный пул приложений в топологии, указать SEFAUtil как надежное приложение и включить топологию.</span><span class="sxs-lookup"><span data-stu-id="6b311-108">Before you can install SEFAUtil, you must have a trusted application pool in your topology, specify SEFAUtil as a trusted application, and enable the topology.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6b311-109">На всех компьютерах, на которых планируется запускать инструмент SEFAUtil, должен быть установлен Microsoft Unified Communications Managed API (UCMA) 3.0 Core SDK.</span><span class="sxs-lookup"><span data-stu-id="6b311-109">Microsoft Unified Communications Managed API (UCMA) 3.0 Core SDK must be installed on any computer where you plan to run the SEFAUtil tool.</span></span>



</div>

<span data-ttu-id="6b311-110">Вы можете запустить SEFAUtil в любом пуле переднего плана в развертывании.</span><span class="sxs-lookup"><span data-stu-id="6b311-110">You can run the SEFAUtil in any Front End pool in your deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6b311-111">Дополнительные сведения об использовании SEFAUtil можно найти в статье блогов TechNet: "как запустить SEFAutil?"</span><span class="sxs-lookup"><span data-stu-id="6b311-111">For more details about running SEFAUtil, see the Technet blog article, "How to get SEFAutil running?"</span></span> <span data-ttu-id="6b311-112">по адресу <A href="https://go.microsoft.com/fwlink/?linkid=278940">https://go.microsoft.com/fwlink/?LinkId=278940</A> .</span><span class="sxs-lookup"><span data-stu-id="6b311-112">at <A href="https://go.microsoft.com/fwlink/?linkid=278940">https://go.microsoft.com/fwlink/?LinkId=278940</A>.</span></span>



</div>

<div>

## <a name="to-deploy-sefautil"></a><span data-ttu-id="6b311-113">Развертывание SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="6b311-113">To deploy SEFAUtil</span></span>

1.  <span data-ttu-id="6b311-114">Войдите на компьютер, на котором установлена командная консоль Lync Server Management Shell, в группу RTCUniversalServerAdmins или с необходимыми правами пользователя, как описано в разделе [Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="6b311-114">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="6b311-115">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="6b311-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="6b311-116">The SEFAUtil tool can be run only on a computer that is part of a trusted application pool.</span><span class="sxs-lookup"><span data-stu-id="6b311-116">The SEFAUtil tool can be run only on a computer that is part of a trusted application pool.</span></span> <span data-ttu-id="6b311-117">При необходимости определите доверенный пул приложений для пула переднего плана, в котором планируется запускать SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="6b311-117">If needed, define a trusted application pool for the Front End pool where you plan to run SEFAUtil.</span></span> <span data-ttu-id="6b311-118">At the command line, run:</span><span class="sxs-lookup"><span data-stu-id="6b311-118">At the command line, run:</span></span>
    
        New-CsTrustedApplicationPool -id <Pool FQDN> -Registrar <Pool Registrar FQDN> -site Site:<Pool Site>

4.  <span data-ttu-id="6b311-p104">Определите инструмент SEFAUtil как доверенное приложение. В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6b311-p104">Define the SEFAUtil tool as a trusted application. At the command line, run:</span></span>
    
        New-CsTrustedApplication -ApplicationId sefautil -TrustedApplicationPoolFqdn <Pool FQDN>  -Port 7489
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6b311-121">При необходимости можно использовать другой порт.</span><span class="sxs-lookup"><span data-stu-id="6b311-121">You can use a different port if needed.</span></span>

    
    </div>

5.  <span data-ttu-id="6b311-p105">Включите топологию с внесенными изменениями. В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6b311-p105">Enable the topology with your changes. At the command line, run:</span></span>
    
        Enable-CsTopology

6.  <span data-ttu-id="6b311-124">Установите средства набора ресурсов Lync Server 2013 на сервер переднего плана, который находится в надежном пуле приложений, созданном на этапе 3.</span><span class="sxs-lookup"><span data-stu-id="6b311-124">Install the Lync Server 2013 resource kit tools on a Front End Server that is in the trusted application pool that you created in step 3.</span></span>

7.  <span data-ttu-id="6b311-125">Проверьте правильность работы инструмента SEFAUtil следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6b311-125">Verify that the SEFAUtil tool is running correctly, as follows:</span></span>
    
    1.  <span data-ttu-id="6b311-126">Запустите этот инструмент из командной строки Windows с привилегиями администратора, чтобы отобразить параметры переадресации звонков пользователя в текущем развертывании.</span><span class="sxs-lookup"><span data-stu-id="6b311-126">Run the tool from the Windows command prompt with administrator privileges to display the call forwarding settings of a user in your deployment.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="6b311-127">Это средство находится в \Program Files\Microsoft Lync Server 2013 \ reskit.</span><span class="sxs-lookup"><span data-stu-id="6b311-127">The tool is located at \Program Files\Microsoft Lync Server 2013\Reskit.</span></span>

        
        </div>
    
    2.  <span data-ttu-id="6b311-p106">Отобразите параметры переадресации звонков пользователя. В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6b311-p106">Display the call forwarding settings of a user. At the command line, run:</span></span>
        
            SEFAUtil.exe <user SIP address> /server:<Lync Server/Pool FQDN>
        
        <span data-ttu-id="6b311-130">На экране появятся параметры переадресации звонков пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b311-130">The call forwarding settings for the user will be displayed.</span></span>

<span data-ttu-id="6b311-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b311-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

