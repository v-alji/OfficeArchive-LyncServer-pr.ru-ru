---
title: 'Lync Server 2013: Включение и отключение серверного приложения на языке обработки Microsoft SIP (MSPL)'
description: 'Lync Server 2013: Включение или отключение серверного приложения на языке обработки Microsoft SIP (MSPL).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a Microsoft SIP Processing Language (MSPL) server application
ms:assetid: b20af38d-224a-4459-991d-0b7eabb3ca7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182573(v=OCS.15)
ms:contentKeyID: 48185145
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f919599d6c6a39fea73424f4e287f00636c0982
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398485"
---
# <a name="enable-or-disable-a-microsoft-sip-processing-language-mspl-server-application-in-lync-server-2013"></a>Включение и отключение серверного приложения Microsoft SIP Languageing (MSPL) в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-21_

С помощью панели управления Lync Server можно включать и отключать серверные приложения Microsoft SIP Language (MSPL), которые выполняются в среде Lync Server 2013. Эти приложения предназначены только для приложений, использующих язык сценариев вместо API Microsoft Lync 2013 Preview.

Не все сценарии можно включать и отключать. Например, сценарий DefaultRouting включается, и этот параметр невозможно изменить для DefaultRouting.

<div>

## <a name="to-enable-or-disable-an-mspl-server-application"></a>Включение и отключение серверного приложения MSPL

1.  Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите пункт **топология** и щелкните **серверное приложение**.

4.  На странице **серверное приложение** щелкните заголовок столбца, чтобы отсортировать приложения, если необходимо, а затем выберите серверное приложение, которое вы хотите изменить.

5.  Нажмите кнопку **действие**.

6.  Нажмите кнопку **включить приложение** или **отключить приложение** (то есть, если сценарий поддерживает этот параметр).

</div>

<div>

## <a name="see-also"></a>См. также


[Пометка приложения на языке обработки Microsoft SIP (MSPL) как критическое или некритическое в Lync Server 2013](lync-server-2013-mark-a-microsoft-sip-processing-language-mspl-application-as-critical-or-not-critical.md)  


[Просмотр серверных приложений Microsoft SIP Processing Language (MSPL) в Lync Server 2013](lync-server-2013-view-microsoft-sip-processing-language-mspl-server-applications.md)  


[Управление топологией Lync Server 2013](lync-server-2013-managing-the-lync-server-topology.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

