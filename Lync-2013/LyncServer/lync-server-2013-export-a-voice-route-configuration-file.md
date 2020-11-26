---
title: 'Lync Server 2013: экспорт файла конфигурации голосового маршрута'
description: 'Lync Server 2013: экспорт файла конфигурации голосового маршрута.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export a voice route configuration file
ms:assetid: 02ce922d-9ca8-4513-b09f-9de51f5c5bdc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398081(v=OCS.15)
ms:contentKeyID: 48183248
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 30bf342e11be41015df3cfd76f6a875381cb8b64
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428372"
---
# <a name="export-a-voice-route-configuration-file-in-lync-server-2013"></a>Экспорт файла конфигурации голосового маршрута в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Если вы хотите сохранить конфигурацию голосовой связи, не публикуя ее, выполните указанные ниже действия, чтобы использовать команды экспорта и импорта на панели управления Lync Server, чтобы сохранить и извлечь снимок конфигурации голосовой маршрутизации. При импорте файла конфигурации голосовой маршрутизации (. vcfg) изменения, внесенные в конфигурацию голосовой маршрутизации на сервере, будут указывать на наличие незафиксированных изменений, внесенных в голосовую почту, на странице в группе " **Маршрутизация** голосовых сообщений" на панели управления Lync Server. Those uncommitted changes are the differences between the two configurations that require reconciliation.

Если вы внесли какие-либо незафиксированные изменения параметров на любой странице в группе, изменения будут сохранены в файле экспортированной конфигурации голосовой связи (. vcfg). Это позволит вам вносить изменения в конфигурацию голосовой маршрутизации во время нескольких сеансов, прежде чем публиковать изменения.

<div>

## <a name="to-export-a-voice-routing-configuration"></a>Экспорт конфигурации маршрутизации голосовых данных

1.  Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator. Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  В левой области навигации щелкните элемент **Маршрутизация голосовой связи**.

4.  В меню **Действия** щелкните пункт **Экспорт конфигурации**.

5.  Укажите расположение и имя файла, а затем нажмите кнопку **Сохранить**.

</div>

<div>

## <a name="see-also"></a>См. также


[Импорт файла конфигурации маршрута голосовых вызовов в Lync Server 2013](lync-server-2013-import-a-voice-route-configuration-file.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

