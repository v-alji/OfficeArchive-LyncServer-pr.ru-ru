---
title: 'Lync Server 2013: командлеты пограничного сервера'
description: 'Lync Server 2013: командлеты пограничного сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edge Server cmdlets
ms:assetid: 1a5427f4-a0d1-4652-8135-91333158ffc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415635(v=OCS.15)
ms:contentKeyID: 48183534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b73172331ddcde76672cccda682669f71dd7262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397897"
---
# <a name="edge-server-cmdlets-in-lync-server-2013"></a>Командлеты пограничного сервера в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-10-07_

Пограничные серверы предоставляют способ продления возможностей Microsoft Lync Server 2013 для пользователей, не вошедших в внутреннюю сеть. Например, если у вас есть удаленные пользователи, прошедшие проверку подлинности, которые входят в состав сервера Lync Server 2013 через Интернет, а не через внутреннюю сеть, вам потребуется настроить пограничный сервер, на котором запущена служба Edge Access для доступа к Lync Server. Кроме того, пограничные серверы требуются, если вы хотите установить Федерацию с другой организацией или вы хотите предоставить пользователям право общаться с людьми, у которых есть учетные записи с помощью общедоступной службы обмена мгновенными сообщениями, например Yahoo \! , AOL или MSN.

<div>


> [!IMPORTANT]
> <UL>
> <LI>
> <P>По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров. Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo! Messenger, пока служба не отключается. Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня. было объявлено. Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</P>
> <LI>
> <P>USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!. Messenger. Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</P>
> <LI>
> <P>В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру. Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync. В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</P></LI></UL>



</div>

<div>

## <a name="edge-server-cmdlets"></a>Командлеты пограничного сервера

Ниже приведен список командлетов, которые непосредственно относятся к управлению пограничными серверами.

**Пограничный сервер**

  - <span></span>  
    [Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))

  - <span></span>  
    [Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))

  - <span></span>  
    [New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))

  - <span></span>  
    [Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))

  - <span></span>  
    [Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))

</div>

<div>

## <a name="see-also"></a>См. также


[Блог Lync Server PowerShell](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

