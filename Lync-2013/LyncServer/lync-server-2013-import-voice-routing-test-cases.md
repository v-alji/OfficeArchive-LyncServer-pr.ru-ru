---
title: 'Lync Server 2013: импорт тестовых примеров маршрутизации голосовой связи'
description: 'Lync Server 2013: Импорт тестовых случаев маршрутизации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import voice routing test cases
ms:assetid: 6546e24c-9ad2-428b-92b2-63948ed0f884
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398460(v=OCS.15)
ms:contentKeyID: 48184325
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06ce1b144de03406b7b78d6957371ed2bc303e95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399556"
---
# <a name="import-voice-routing-test-cases-in-lync-server-2013"></a>Импорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-21_

Тестовые случаи позволяют тестировать маршруты к голосовой связи в вашей организации: вы определяете, какие именно номера нужно набрать, а также о том, как будет использоваться абонентская группа и голосовая политика, а Lync Server 2013 сможет проверить, что при наличии этих условий предоставленный вами номер может успешно перенаправляться в сеть PSTN.

Тестовые случаи, которые можно создать с помощью панели управления Lync Server, обычно сохраняются только на сервере, где они были созданы и запущены. Однако эти тестовые случаи можно экспортировать как XML-файлы (с расширением vTest), а затем импортировать на другие серверы. Это позволяет выполнять одни и те же тесты на разных компьютерах, расположенных в разных точках топологии.

<div>

## <a name="to-import-a-voice-routing-test-case"></a>Импорт тестового случая голосовой маршрутизации

1.  Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator. Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  В левой области навигации щелкните элемент **Маршрутизация голосовой связи**.

4.  В меню **действия** выберите команду **Импорт тестовых случаев**.

5.  Найдите файл тестового случая (vTest), который вы хотите импортировать, и нажмите кнопку **Открыть**.

6.  Нажмите кнопку **Сохранить**, а затем нажмите кнопку **Сохранить все**.
    
    <div>
    

    > [!NOTE]  
    > Каждый раз, когда вы импортируете vTest-файл, необходимо выполнить команду <STRONG>commit all</STRONG> для публикации тестового случая. Дополнительные сведения можно найти в разделе <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</A> в документации по эксплуатации.

    
    </div>

</div>

<div>

## <a name="see-also"></a>См. также


[Экспорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013](lync-server-2013-export-voice-routing-test-cases.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

