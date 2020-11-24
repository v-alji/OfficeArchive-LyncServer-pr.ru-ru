---
title: 'Lync Server 2013: изменить или настроить простые URL-адреса'
description: 'Lync Server 2013: Редактирование и настройка простых URL-адресов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edit or configure simple URLs
ms:assetid: 0008aeea-4ae9-4e36-83cd-ef7ff7b6e128
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398063(v=OCS.15)
ms:contentKeyID: 48183216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9152a65083f71510f4cdb1189b3982afdd68b4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397885"
---
# <a name="edit-or-configure-simple-urls-in-lync-server-2013"></a>Изменить или настроить простые URL-адреса в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-02-04_

Для этой процедуры не требуется членство в группе локального администратора или привилегированного домена. Войдите в систему как обычный пользователь.

Lync Server 2013 использует простые URL-адреса для прямого внутренних и внешних звонков к службам на сервере переднего плана или в директории, если она была развернута. Дополнительные сведения об простых URL-адресах можно найти [в разделе Планирование простых URL-адресов в Lync Server 2013](lync-server-2013-planning-for-simple-urls.md) в документации по планированию. Вы можете выбрать формат для простых URL-адресов из нескольких вариантов. Подробнее об этих параметрах можно узнать [в разделе Требования к DNS для простых URL-адресов в Lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) в документации по планированию.

По умолчанию простые URL-адреса будут настраиваться в форме (например, простой URL-адрес для подключения https://dialin ).\<SIP Domain\>

<div>

## <a name="to-configure-simple-urls"></a>Настройка простых URL-адресов

1.  В построителе топологии щелкните правой кнопкой мыши узел **Lync Server** и выберите команду **изменить свойства**.

2.  В области **простых URL-адресов** выберите для изменения свойство **URL-адреса телефонного доступа:** (Dial-in) или свойство **URL-адреса собраний:** (Meet). Затем нажмите команду **Изменить URL-адрес**.

3.  Установите для URL-адреса нужное значение и нажмите кнопку **ОК**, чтобы сохранить измененный URL-адрес. Приведенный здесь пример изменил URL-адрес для подключения https://pool01.contoso.net/dialin .

4.  При необходимости тем же способом измените URL-адрес Meet.

</div>

<div>

## <a name="to-define-the-optional-admin-simple-url"></a>Определение дополнительного URL-адреса Admin

1.  В построителе топологии щелкните правой кнопкой мыши узел **Lync Server** и выберите команду **изменить свойства**.

2.  В диалоговом окне **URL-адрес администрирования** введите простой URL-адрес, который вы хотите использовать для административного доступа к панели управления Lync Server 2013, а затем нажмите кнопку **ОК**.
    
    <div>
    

    > [!TIP]  
    > В качестве URL-адреса администрирования рекомендуется использовать максимально простой URL-адрес. Это самый простой вариант <STRONG> https://admin .</STRONG> &lt; Domain (домен) &gt; .

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > В случае изменения простого URL-адреса после исходного развертывания необходимо помнить, что такие изменения влияют на записи службы доменных имен (DNS) и сертификаты для простых URL-адресов. Если это изменение повлияет на базу простого URL-адреса, необходимо также изменить записи DNS и сертификаты. Например, https://lync.contoso.com/Meet чтобы изменить https://meet.contoso.com базовый URL-адрес с lync.contoso.com на Meet.contoso.com, измените его, чтобы он ссылался на Meet.contoso.com. Если вы изменили простой URL-адрес с " https://lync.contoso.com/Meet на" https://lync.contoso.com/Meetings , то основной URL-адрес Lync.contoso.com остается таким же, поэтому изменения DNS или сертификата не требуются. Однако при каждом изменении простого URL-адреса необходимо выполнить командлет <STRONG>Enable-CsComputer</STRONG> на каждом из каталогов и на сервере переднего плана для регистрации изменения.

    
    </div>

</div>

<div>

## <a name="see-also"></a>См. также


[Планирование простых URL-адресов в Lync Server 2013](lync-server-2013-planning-for-simple-urls.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

