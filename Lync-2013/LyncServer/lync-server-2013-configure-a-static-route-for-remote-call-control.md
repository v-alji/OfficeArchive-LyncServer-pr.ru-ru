---
title: 'Lync Server 2013: настройка статического маршрута для дистанционного управления вызовами'
description: 'Lync Server 2013: Настройка статического маршрута для удаленного управления звонками.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a static route for remote call control
ms:assetid: f7003023-443d-48ee-989b-71e8b0b0abbd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615051(v=OCS.15)
ms:contentKeyID: 48185855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ecf6478d4fb7ab4f04f8a452d4837b327ba254a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434209"
---
# <a name="configure-a-static-route-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="e0b74-103">Настройка статического маршрута для дистанционного управления вызовами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0b74-103">Configure a static route for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0b74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0b74-104">

<span> </span></span></span>

<span data-ttu-id="e0b74-105">_**Тема последнего изменения:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="e0b74-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="e0b74-106">Удаленное управление звонками требует, чтобы каждый пул серверов Lync Server настроился с помощью пути из этого пула на шлюз SIP/CSTA, который подключается к частной сети обмена филиалами (УАТС).</span><span class="sxs-lookup"><span data-stu-id="e0b74-106">Remote call control requires that every Lync Server pool is configured with a path from that pool to the SIP/CSTA gateway that connects to the private branch exchange (PBX).</span></span> <span data-ttu-id="e0b74-107">Этот путь требует, чтобы каждый пул выделил один статический маршрут для каждого шлюза, на который будет прокси-сервер, управляющие сообщениями, связанные с вызовами УАТС.</span><span class="sxs-lookup"><span data-stu-id="e0b74-107">This path requires that each pool has one static route for each gateway to which the pool will proxy SIP call control messages associated with calls to the PBX.</span></span> <span data-ttu-id="e0b74-108">Если вы настроили глобальный статический маршрут для удаленного управления звонком, то каждый пул, для которого не настроен статический маршрут на уровне пула, будет использовать глобальный статический маршрут.</span><span class="sxs-lookup"><span data-stu-id="e0b74-108">If you configure a global static route for remote call control, each pool that is not configured with a static route at the pool level will use the global static route.</span></span>

<div>

## <a name="to-configure-a-static-route-for-remote-call-control"></a><span data-ttu-id="e0b74-109">Настройка статического маршрута для удаленного управления звонками</span><span class="sxs-lookup"><span data-stu-id="e0b74-109">To configure a static route for remote call control</span></span>

1.  <span data-ttu-id="e0b74-110">Войдите на компьютер, на котором установлена командная консоль Lync Server Management Shell, в группу RTCUniversalServerAdmins или роль управления доступом на основе ролей (RBAC), для которой вы назначили командлет **New-CsStaticRoute** .</span><span class="sxs-lookup"><span data-stu-id="e0b74-110">Log on to a computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or a role-based access control (RBAC) role to which you have assigned the **New-CsStaticRoute** cmdlet.</span></span>

2.  <span data-ttu-id="e0b74-111">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="e0b74-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e0b74-112">Чтобы создать статический маршрут и вставить его в переменную $TLSRoute или $TCPRoute, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="e0b74-112">To create a static route and put it in the variable $TLSRoute or $TCPRoute, do one of the following:</span></span>
    
    <div class="">
    

    > [!TIP]  
    > <span data-ttu-id="e0b74-113">Чтобы сопоставить дочерние домены домена, можно задать подстановочное значение в параметре MatchUri.</span><span class="sxs-lookup"><span data-stu-id="e0b74-113">To match child domains of a domain, you can specify a wildcard value in the MatchUri parameter.</span></span> <span data-ttu-id="e0b74-114">Например, <STRONG>\*. contoso.NET</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e0b74-114">For example, <STRONG>\*.contoso.net</STRONG>.</span></span> <span data-ttu-id="e0b74-115">Это значение соответствует любому домену, который заканчивается на суффикс <STRONG>contoso.NET</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e0b74-115">That value matches any domain that ends with the suffix <STRONG>contoso.net</STRONG>.</span></span>

    
    </div>
    
      - <span data-ttu-id="e0b74-116">Для подключения к протоколу TLS введите в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e0b74-116">For a Transport Layer Security (TLS) connection, type the following at the command prompt:</span></span>
        
        ```powershell
        $TLSRoute = New-CsStaticRoute -TLSRoute -Destination <gateway FQDN> -Port <gateway SIP listening port> -UseDefaultCertificate $true -MatchUri <destination domain>
        ```
        <span data-ttu-id="e0b74-117">Например:</span><span class="sxs-lookup"><span data-stu-id="e0b74-117">For example:</span></span>
        ```powershell
        $TLSRoute = New-CsStaticRoute -TLSRoute -Destination rccgateway.contoso.net -Port 5065 -UseDefaultCertificate $true -MatchUri *.contoso.net
        ```
        <span data-ttu-id="e0b74-118">Если для UseDefaultCertificate задано значение false, необходимо указать параметры TLSCertIssuer и TLSCertSerialNumber.</span><span class="sxs-lookup"><span data-stu-id="e0b74-118">If UseDefaultCertificate is set to False, you must specify TLSCertIssuer and TLSCertSerialNumber parameters.</span></span> <span data-ttu-id="e0b74-119">Эти параметры указывают имя центра сертификации (ЦС), который выдал сертификат, используемый в статическом маршруте, и порядковый номер этого TLS-сертификата соответственно.</span><span class="sxs-lookup"><span data-stu-id="e0b74-119">These parameters indicate the name of the certification authority (CA) that issued the certificate used in the static route, and the serial number of that TLS certificate, respectively.</span></span> <span data-ttu-id="e0b74-120">Подробнее об этих параметрах можно узнать в справке Lync Server Management Shell, введя следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="e0b74-120">For details about these parameters, see Lync Server Management Shell Help by typing the following at the command prompt:</span></span>
        ```powershell
        Get-Help New-CsStaticRoute -Full
        ```
      - <span data-ttu-id="e0b74-121">Для подключения по протоколу TCP введите в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e0b74-121">For a Transmission Control Protocol (TCP) connection, type the following at the command prompt:</span></span>
        
        <div class="">
        

        > [!NOTE]  
        > <span data-ttu-id="e0b74-122">Если вы указали полное доменное имя (FQDN), необходимо сначала настроить DNS A Record (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="e0b74-122">If you specify a fully qualified domain name (FQDN), you must configure a Domain Name System (DNS) A record first.</span></span>

        
        </div>
        
        ```powershell
        $TCPRoute = New-CsStaticRoute -TCPRoute -Destination <gateway IP address or FQDN> -Port <gateway SIP listening port> -MatchUri <destination domain>
        ```
        <span data-ttu-id="e0b74-123">Например:</span><span class="sxs-lookup"><span data-stu-id="e0b74-123">For example:</span></span>
        ```powershell
        $TCPRoute = New-CsStaticRoute -TCPRoute -Destination 192.168.0.240 -Port 5065 -MatchUri *.contoso.net
        ```
        <span data-ttu-id="e0b74-124">Ниже указаны значения по умолчанию для статических маршрутов с необязательными параметрами.</span><span class="sxs-lookup"><span data-stu-id="e0b74-124">The following are default values for optional parameters for static routes:</span></span>
        
          - <span data-ttu-id="e0b74-125">Enabled = True</span><span class="sxs-lookup"><span data-stu-id="e0b74-125">Enabled = True</span></span>
        
          - <span data-ttu-id="e0b74-126">MatchOnlyPhoneUri = false</span><span class="sxs-lookup"><span data-stu-id="e0b74-126">MatchOnlyPhoneUri = False</span></span>
        
          - <span data-ttu-id="e0b74-127">ReplaceHostInRequestUri = false</span><span class="sxs-lookup"><span data-stu-id="e0b74-127">ReplaceHostInRequestUri = False</span></span>
        
        <span data-ttu-id="e0b74-128">Мы настоятельно рекомендуем не менять эти значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0b74-128">We strongly recommend that you do not change these default values.</span></span> <span data-ttu-id="e0b74-129">Однако если вы должны изменить любой из этих параметров, ознакомьтесь со справкой оболочки среды управления Lync Server, введя в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e0b74-129">However, if you must change any of these parameters, see Lync Server Management Shell Help by typing the following at the command prompt:</span></span>
        ```powershell
        Get-Help New-CsStaticRoute -Full
        ```
4.  <span data-ttu-id="e0b74-130">Чтобы сохранить созданный статический маршрут в хранилище Центрального управления, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="e0b74-130">To persist a newly created static route in the Central Management store, run one of the following, as appropriate:</span></span>
    
       ```powershell
        Set-CsStaticRoutingConfiguration -Route @{Add=$TLSRoute}
       ```
    
       ```powershell
        Set-CsStaticRoutingConfiguration -Route @{Add=$TCPRoute}
       ```

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e0b74-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e0b74-131">See Also</span></span>


[<span data-ttu-id="e0b74-132">Настройка записи доверенного приложения для удаленного управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0b74-132">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)  
[<span data-ttu-id="e0b74-133">Определение IP-адреса для шлюза SIP/CSTA в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0b74-133">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)  
  

<span data-ttu-id="e0b74-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0b74-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

