---
title: 'Lync Server 2013: изменение существующих параметров конфигурации веб-службы'
description: 'Lync Server 2013: изменение существующих параметров конфигурации веб-службы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify existing Web Service configuration settings
ms:assetid: bd9c7aa5-d31c-4fab-b31d-8baae26b1296
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182580(v=OCS.15)
ms:contentKeyID: 48185272
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 455ddf60d171fe584115d646b16f63595285a906
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445759"
---
# <a name="modify-existing-web-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="4a309-103">Изменение существующих параметров конфигурации веб-службы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a309-103">Modify existing Web Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a309-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a309-104">

<span> </span></span></span>

<span data-ttu-id="4a309-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="4a309-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="4a309-106">На странице **веб-службы** можно настроить методы проверки подлинности для доступа к веб-серверам, связанным с Lync Server 2013 и веб-службам.</span><span class="sxs-lookup"><span data-stu-id="4a309-106">You can use the **Web Service** page to configure the authentication methods for accessing Lync Server 2013 related web servers and Web Services.</span></span>

<span data-ttu-id="4a309-107">Чтобы изменить политику существующей веб-службы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4a309-107">Follow these steps to modify an existing Web Service policy.</span></span>

<div>

## <a name="to-modify-existing-web-service-configuration-settings"></a><span data-ttu-id="4a309-108">Изменение параметров конфигурации существующей веб-службы</span><span class="sxs-lookup"><span data-stu-id="4a309-108">To modify existing Web service configuration settings</span></span>

1.  <span data-ttu-id="4a309-109">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4a309-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="4a309-110">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4a309-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4a309-111">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4a309-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4a309-112">В левой панели навигации щелкните **Безопасность**, а затем щелкните **Веб-служба**.</span><span class="sxs-lookup"><span data-stu-id="4a309-112">In the left navigation bar, click **Security** and then click **Web Service**.</span></span>

4.  <span data-ttu-id="4a309-113">На странице **Веб-служба** выберите конфигурацию, щелкните **Правка**, затем щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="4a309-113">On the **Web Service** page, click a configuration, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="4a309-114">На странице **Изменение параметров веб-службы** в раскрывающемся списке **Интегрированная проверка подлинности Windows** выберите **Согласование**, **Интегрированная проверка подлинности Windows** или **Отсутствует**.</span><span class="sxs-lookup"><span data-stu-id="4a309-114">In **Edit Web Service Setting**, in **Integrated Windows authentication**, select **Negotiate**, **Integrated Windows authentication**, or **None**.</span></span>

6.  <span data-ttu-id="4a309-115">Установите один флажок или несколько флажков в соответствии с возможностями клиентов и среды:</span><span class="sxs-lookup"><span data-stu-id="4a309-115">Select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="4a309-116">**Включить проверку подлинности с помощью ПИН-кода**, чтобы разрешить клиентам проходить проверку подлинности с помощью ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="4a309-116">**Enable PIN Authentication** to enable clients to be authenticated using PIN numbers.</span></span>
    
      - <span data-ttu-id="4a309-117">**Включить проверку подлинности с помощью сертификата** — чтобы серверы в пуле выдавали сертификаты клиентам.</span><span class="sxs-lookup"><span data-stu-id="4a309-117">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>
    
      - <span data-ttu-id="4a309-118">**Включить загрузку цепочки сертификатов**, чтобы серверы, представляющие сертификат проверки подлинности, загружали цепочку сертификатов для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a309-118">**Enable certificate chain download** to have servers presented with an authentication certificate download the certificate chain for that certificate.</span></span>

7.  <span data-ttu-id="4a309-119">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="4a309-119">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4a309-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4a309-120">See Also</span></span>


[<span data-ttu-id="4a309-121">Настройка проверки подлинности на панели управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a309-121">Configuring authentication in the Lync Server 2013 Control Panel</span></span>](lync-server-2013-configuring-authentication-in-the-lync-server-control-panel.md)  
  

<span data-ttu-id="4a309-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a309-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

