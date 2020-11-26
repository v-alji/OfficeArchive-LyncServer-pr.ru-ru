---
title: 'Lync Server 2013: необходимые условия и роли для настройки объявлений'
description: 'Lync Server 2013: требования для настройки объявлений и роли.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439970"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a>Необходимые условия и роли для настройки объявлений в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-25_

Объявление — это функция управления голосовым звонком в корпоративной среде. В этой статье описаны действия, которые необходимо выполнить, прежде чем можно будет настроить объявление и назначения ролей, необходимые для выполнения задач настройки.

В этом разделе предполагается, что вы прочитали документацию по планированию, относящуюся к объявлению (см. раздел [Планирование функций управления звонками в Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).

<div>

## <a name="announcement-configuration-prerequisites"></a>Предварительные требования для конфигурации объявлений

Для приложения извещения необходимы следующие компоненты:

  - приложения

  - "Группа ответа"

  - Хранилище файлов, для хранения звуковых файлов

Все эти компоненты устанавливаются по умолчанию при развертывании корпоративной голосовой связи.

</div>

<div>

## <a name="announcement-configuration-roles"></a>Роли конфигурации объявлений

Для настройки объявлений можно использовать следующие средства администрирования:

  - Панель управления Lync Server

  - Командная консоль Lync Server

Для настройки приложения объявления требуется одна из следующих административных ролей:

  - **CsVoiceAdministrator**   Эта роль администратора может создавать, настраивать и управлять всеми параметрами и политиками голосовой связи, включая параметры объявлений.

  - **CsServerAdministrator**   Эта роль администратора позволяет управлять серверами и службами и устранять неполадки с ними, а также настраивать все параметры объявлений.

  - **CsAdministrator**   Эта роль администратора может выполнять все административные задачи и изменять все параметры.

  - **CsViewOnlyAdministrator**   Эта роль администратора может просматривать развертывание для наблюдения за работоспособностью развертывания.

<div>


> [!NOTE]  
> Подробнее об административных правах пользователей можно узнать в разделе <A href="lync-server-2013-planning-for-role-based-access-control.md">Планирование управления доступом на основе ролей в Lync Server 2013</A> в документации по планированию.



</div>

</div>

<div>

## <a name="see-also"></a>См. также


[Развертывание корпоративной голосовой связи в Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md)  


[Планирование функций управления звонками в Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

