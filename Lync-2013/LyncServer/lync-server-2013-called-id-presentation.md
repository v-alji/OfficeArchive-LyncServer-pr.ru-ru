---
title: 'Lync Server 2013: вызываемый идентификационный номер презентации'
description: 'Lync Server 2013: вызываемый ID презентация.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Called ID presentation
ms:assetid: cf6c6af5-3418-411e-a50b-7a9cf8e100d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721892(v=OCS.15)
ms:contentKeyID: 49733826
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b438c7c19bc3c4ad641a8b9f8dac319c9fc2b1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435651"
---
# <a name="called-id-presentation-in-lync-server-2013"></a>Презентация с именем "идентификатор" в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-21_

При использовании Lync Server 2010 номер телефона вызываемого абонента (т. е. номер телефона) можно перевести из формата E. 164 в локальный формат набора номера, который требуется магистральным одноранговым узлом (то есть шлюзом, частным обменом филиалов или телефонной магистральной панелью SIP). Для этого необходимо определить одно или несколько правил преобразования для преобразования URI запроса перед переадресованием на магистральный узел.

<div>


> [!IMPORTANT]  
> Возможность связывать одно или несколько правил трансляции с конфигурацией магистрали корпоративной голосовой связи предназначена для использования в качестве <EM>альтернативы</EM> настройке правил перевода на магистральном одноранговом узле. Не применяйте правила перевода с конфигурацией корпоративной магистрали, если вы настроили правила трансляции для однорангового канала, так как эти правила могут конфликтовать.



</div>

Чтобы создать или изменить правило трансляции, можно использовать один из следующих способов:

  - С помощью инструмента " **Создание правил перевода** " можно указать значения для начальных цифр, длину, цифр для удаления и цифр, которые нужно добавить, а затем позволить панели управления Lync Server создать соответствующий шаблон сопоставления и правило перевода.

  - Напишите регулярные выражения вручную, чтобы задать шаблон сопоставления и правило трансляции.

<div>


> [!NOTE]  
> Сведения о том, как создавать регулярные выражения, приведены в разделе "регулярные выражения .NET Framework" <A href="https://go.microsoft.com/fwlink/p/?linkid=140927">https://go.microsoft.com/fwlink/p/?linkId=140927</A> .



</div>

<div>

## <a name="in-this-section"></a>Содержание

  - [Создание или изменение правила трансляции с помощью инструмента "Создание правил перевода" в Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md)

  - [Создание и изменение правила трансляции вручную в Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-manually.md)

</div>

<div>

## <a name="see-also"></a>См. также


[Презентация идентификации вызывающего абонента в Lync Server 2013](lync-server-2013-caller-id-presentation.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

