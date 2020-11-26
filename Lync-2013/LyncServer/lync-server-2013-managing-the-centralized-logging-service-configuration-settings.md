---
title: Управление централизованными параметрами конфигурации службы ведения журналов
description: Управление централизованными параметрами конфигурации службы ведения журналов.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Centralized Logging Service configuration settings
ms:assetid: f455c3aa-0061-413d-bdfb-a3e78f82723d
ms:mtpsurl: https://technet.microsoft.com/library/JJ721938(v=OCS.15)
ms:contentKeyID: 49733875
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e25294e096b8368aa06a11e4ad851fe5d1a84c0f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425901"
---
# <a name="managing-the-centralized-logging-service-configuration-settings-in-lync-server-2013"></a>Управление централизованными параметрами конфигурации службы ведения журналов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Централизованная служба ведения журнала контролируется и настраивается с помощью параметров и параметров, создаваемых и используемых централизованным контроллером службы ведения журналов (CLSController), чтобы отправлять команды на централизованный агент служб ведения журналов (CLSAgent) отдельного компьютера. Агент обрабатывает отправляемые им команды и (в случае команды запуска) использует конфигурацию сценариев, поставщиков, размера журнала, длительности трассировки и флагов для начала сбора журналов трассировки в соответствии с предоставленными сведениями о конфигурации.

<div>


> [!IMPORTANT]
> Не все командлеты Windows PowerShell, указанные для централизованной службы ведения журналов, предназначены для использования с локальными развертываниями Lync Server 2013. Несмотря на то, что они работают, следующие командлеты не предназначены для работы с локальными развертываниями Lync Server 2013. 
> <UL>
> <LI>
> <P><STRONG>Командлеты CsClsRegion:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">Set-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-CsClsRegion</A>и <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">Remove-CsClsRegion</A>.</P>
> <LI>
> <P><STRONG>Командлеты CsClsSearchTerm:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">Get-CsClsSearchTerm</A> и <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">Set-CsClsSearchTerm</A>.</P>
> <LI>
> <P><STRONG>Командлеты CsClsSecurityGroup:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">Get-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">Set-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>и <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">Remove-CsClsSecurityGroup</A>.</P></LI></UL>Параметры, определенные в этих командлетах, не мешают или не вызывают каких-либо нежелательных действий, но они предназначены для использования с Microsoft 365 и не будут давать ожидаемые результаты в локальных развертываниях. Это не означает полную бесполезность таких командлетов в локальных развертываниях, но вопрос об их использовании выходит за рамки данной документации.


</div>

<div>

## <a name="in-this-section"></a>Содержание

В темах этого раздела определяются параметры конфигурации, параметры и параметры для централизованной службы ведения журналов. Сведения о настройке централизованной службы ведения журналов, о том, как извлекать параметры конфигурации, создавать сценарии, управлять группами безопасности для централизованной службы ведения журнала, поиска и других сведений, которые содержатся в указанных ниже разделах.

  - [Управление конфигурацией службы ведения журналов на компьютере, сайте и глобальном централизованном хранилище в Lync Server 2013](lync-server-2013-managing-computer-site-and-global-centralized-logging-service-configuration.md)

  - [Настройка поставщиков для централизованной службы ведения журналов в Lync Server 2013](lync-server-2013-configuring-providers-for-centralized-logging-service.md)

  - [Настройка сценариев для централизованной службы ведения журналов в Lync Server 2013](lync-server-2013-configuring-scenarios-for-the-centralized-logging-service.md)

</div>

<div>

## <a name="see-also"></a>См. также


[Общие сведения об централизованной службе ведения журналов в Lync Server 2013](lync-server-2013-overview-of-the-centralized-logging-service.md)  
[Командлеты централизованного ведения журналов в Lync Server 2013](lync-server-2013-centralized-logging-cmdlets.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

