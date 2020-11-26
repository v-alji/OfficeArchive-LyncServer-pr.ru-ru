---
title: Настройка записи доверенного приложения для удаленного управления звонками
description: Настройка записи надежного приложения для удаленного управления звонками.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trusted application entry for remote call control
ms:assetid: 37777f93-8b24-40cf-808e-7c6230eb2132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558636(v=OCS.15)
ms:contentKeyID: 48183829
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa5341dc220853670cf000f5b0d5dc379c02fa51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434155"
---
# <a name="configure-a-trusted-application-entry-for-remote-call-control-in-lync-server-2013"></a>Настройка записи доверенного приложения для удаленного управления звонками в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2015-11-02_

Шлюз SIP/CSTA должен быть настроен как доверенное приложение, чтобы Lync Server может применять статический маршрут для маршрутизации звонков на шлюз.

<div>


> [!IMPORTANT]
> Если вы переносите пользователей из предыдущей версии развертывания Lync Server, убедитесь, что вы удалили все существующие записи надежного приложения (ранее известные как авторизованные записи узла), созданные для шлюза SIP/CSTA, прежде чем выполнять действия, описанные в этой статье. Подробности можно найти <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">в разделе Удаление устаревшего авторизованного узла в Lync Server 2013 (необязательно)</A>.<BR>Если вы планируете развертывать новое удаленное управление звонками с помощью протокола TCP, вам нужно подтвердить, что для существующих доверенных приложений и пулов нужно задать <STRONG>ограничение использования службы, чтобы</STRONG> использовать один и тот же порт TCP для нового надежного приложения.



</div>

<div>

## <a name="to-configure-a-trusted-application-entry-for-the-sipcsta-gateway"></a>Настройка записи надежного приложения для шлюза SIP/CSTA

1.  Войдите на компьютер, на котором установлена командная консоль Lync Server Management Shell, в группу RTCUniversalServerAdmins или роль управления доступом на основе ролей (RBAC), для которой вы назначили командлет **New-CsTrustedApplicationPool** .

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Чтобы создать запись надежного приложения, выполните одно из указанных ниже действий.
    
      - Для подключения к протоколу TLS введите в командной строке следующую команду:
        
            New-CsTrustedApplicationPool -Identity <FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        Например:
        
            New-CsTrustedApplicationPool -Identity rccgateway.contoso.net -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true
    
      - Для подключения по протоколу TCP введите в командной строке следующую команду:
        
            New-CsTrustedApplicationPool -Identity <IP address or FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        Например:
        
            New-CsTrustedApplicationPool -Identity 192.168.0.240 -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true

4.  Чтобы добавить в пул доверенное приложение, выполните одно из указанных ниже действий.
    
      - Для подключения TLS введите в командной строке следующую команду:
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway>
        
        Например:
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn rccgateway.contoso.net -Port 5065
    
      - Для подключения по протоколу TCP введите в командной строке следующую команду:
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <IP address or FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway> -EnableTcp
        
        Например:
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn 192.169.0.240 -Port 5065 -EnableTcp

5.  Чтобы применить опубликованные изменения, внесенные в топологию, введите в командной строке следующую команду:
    
        Enable-CsTopology

</div>

<div>

## <a name="see-also"></a>См. также


[Настройка статического маршрута для дистанционного управления вызовами в Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md)  
[Определение IP-адреса для шлюза SIP/CSTA в Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

