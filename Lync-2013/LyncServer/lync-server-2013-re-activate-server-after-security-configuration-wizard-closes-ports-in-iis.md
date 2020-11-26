---
title: Повторная активация сервера после закрытия портов в IIS мастером настройки безопасности
description: После того как мастер настройки безопасности закроет порт в службах IIS, повторно активируйте сервер.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Re-activate server after Security Configuration Wizard closes ports in IIS
ms:assetid: cb8e17cf-f8c1-4099-b63b-c242d656c26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398851(v=OCS.15)
ms:contentKeyID: 48185644
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d824845a7f89c28087a7b5d180a6ed017cb47ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436722"
---
# <a name="re-activate-server-after-security-configuration-wizard-closes-ports-in-iis"></a><span data-ttu-id="109bd-103">Повторная активация сервера после закрытия портов в IIS мастером настройки безопасности</span><span class="sxs-lookup"><span data-stu-id="109bd-103">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="109bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="109bd-104">

<span> </span></span></span>

<span data-ttu-id="109bd-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="109bd-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="109bd-106">Некоторые роли Lync Server 2013 работают на веб-службах на порте служб IIS 4443.</span><span class="sxs-lookup"><span data-stu-id="109bd-106">Some Lync Server 2013 roles run Web Services on Internet Information Services (IIS) port 4443.</span></span> <span data-ttu-id="109bd-107">При запуске мастера развертывания Lync Server, Bootstrapper.exe или с помощью командлета **Enable-CsComputer** создается в брандмауэре исключение и открывается порт.</span><span class="sxs-lookup"><span data-stu-id="109bd-107">Running the Lync Server Deployment Wizard, Bootstrapper.exe, or using the **Enable-CsComputer** cmdlet creates an exception in the firewall and opens the port.</span></span> <span data-ttu-id="109bd-108">Если вы запустите мастер настройки безопасности Windows Server 2008 R2 (или другие сценарии защиты), порт 4443 будет заблокирован, а внешние клиенты не смогут обращаться к веб-службам.</span><span class="sxs-lookup"><span data-stu-id="109bd-108">If you then run the Windows Server 2008 R2 Security Configuration Wizard (or other hardening scripts), port 4443 will be blocked, and external clients will not be able to contact Web Services.</span></span> <span data-ttu-id="109bd-109">Чтобы снова открыть порт, вы можете либо изменить исключение межсетевого экрана напрямую, либо повторно активировать сервер.</span><span class="sxs-lookup"><span data-stu-id="109bd-109">To reopen the port you can either modify the firewall exception directly or re-activate the server.</span></span>

<div>

## <a name="to-re-activate-the-server-by-using-the-deployment-wizard"></a><span data-ttu-id="109bd-110">Повторная активация сервера с помощью мастера развертывания</span><span class="sxs-lookup"><span data-stu-id="109bd-110">To re-activate the server by using the Deployment Wizard</span></span>

1.  <span data-ttu-id="109bd-111">На странице мастера развертывания Lync Server нажмите кнопку **выполнить** рядом с **шагом 2: Настройка или удаление компонентов Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="109bd-111">On the Lync Server Deployment Wizard page, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

2.  <span data-ttu-id="109bd-112">На странице **настройки серверных компонентов Lync** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="109bd-112">On **Setup Lync Server components** page, click **Next**.</span></span>

3.  <span data-ttu-id="109bd-113">На странице **выполнение команд** после того, как состояние задачи отображается как завершенное, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="109bd-113">On the **Executing Commands** page, when the task status is shown as completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="109bd-114">Вы также можете повторно активировать сервер с помощью bootstrapper.exe или <STRONG>Enable-CsComputer</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="109bd-114">You can also use bootstrapper.exe or <STRONG>Enable-CsComputer</STRONG> to re-activate the server.</span></span>

    
    <span data-ttu-id="109bd-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="109bd-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

