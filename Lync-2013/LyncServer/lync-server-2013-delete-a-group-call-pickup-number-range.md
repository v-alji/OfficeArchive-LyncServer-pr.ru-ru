---
title: 'Lync Server 2013: Удаление диапазона номеров для отправки группового звонка'
description: 'Lync Server 2013: Удаление диапазона номеров для отправки группового звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Group Call Pickup number range
ms:assetid: 521891f3-7a5d-45de-92dc-d57025453159
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945629(v=OCS.15)
ms:contentKeyID: 51541475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b40d423b64d29300741c55433864128897c3ac8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430709"
---
# <a name="delete-a-group-call-pickup-number-range-in-lync-server-2013"></a>Удаление диапазона номеров для отправки группового звонка в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-01-30_

Чтобы удалить диапазон номеров для отправки группового звонка, выполните указанные ниже действия.

<div>

## <a name="to-delete-a-call-pickup-group-number-range"></a>Удаление диапазона номеров группы для отправки звонков

1.  Войдите на компьютер, на котором установлена командная консоль Lync Server Management Shell, в группу RTCUniversalServerAdmins или с необходимыми правами пользователя, как описано в разделе [Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  В командной строке введите следующую команду:
    
        Remove-CsCallParkOrbit -Identity "<group number range name>" 
    
    Например:
    
        Remove-CsCallParkOrbit -Identity "Redmond call pickup"
    
    <div>
    

    > [!NOTE]  
    > Подробнее о дополнительных параметрах можно найти в разделе <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.

    
    </div>

</div>

<div>

## <a name="see-also"></a>См. также


[Создание или изменение диапазона орбиты на расстоянии вверх на сервере Lync Server 2013](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)  


[Remove-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit)  
[Get-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Get-CsCallParkOrbit)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

