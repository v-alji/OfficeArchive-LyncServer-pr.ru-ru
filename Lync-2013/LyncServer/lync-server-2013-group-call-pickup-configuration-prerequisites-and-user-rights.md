---
title: Необходимые условия для настройки раскладки группового звонка и права пользователей
description: Необходимые условия для настройки раскладки группового звонка и права пользователей.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Call Pickup configuration prerequisites and user rights
ms:assetid: 8757b1d3-751d-49c3-b1b8-b678f663f18e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945641(v=OCS.15)
ms:contentKeyID: 51541495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74d2a758b7199634e14ee387d2554b30bf2ae8d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427875"
---
# <a name="group-call-pickup-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a>Необходимые условия для настройки раскладки группового звонка и права пользователей в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-01-30_

Отправка группового звонка — это функция управления звонками, которая устанавливается по умолчанию при развертывании корпоративной голосовой связи. В этой статье описаны действия, которые необходимо выполнить перед настройкой отправки групповых звонков и правами пользователей, которые необходимо выполнить для выполнения задач настройки.

В этом разделе предполагается, что вы прочитали документацию по планированию, связанную с получением группового звонка (см. раздел [Планирование отправки групп в Lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).

<div>

## <a name="group-call-pickup-configuration-prerequisites"></a>Требования для настройки раскладки группового звонка

Для отправки групповых звонков требуются следующие компоненты:

  - приложения

  - приостановки вызовов

Эти компоненты устанавливаются автоматически при развертывании корпоративной голосовой связи.

</div>

<div>

## <a name="group-call-pickup-configuration-user-rights"></a>Права пользователя на настройку раскладки группового звонка

Для настройки отправки группового звонка используются следующие средства администрирования:

  - Командная консоль Lync Server

  - Инструмент "набор ресурсов SEFAUtil"

Используйте командную консоль Lync Server для создания групп отправки звонков и управления ими в таблице "приостановить Звонок". С помощью средства SEFAUtil Resource Kit вы можете назначить группу для подбора звонков, а также включить или отключить функцию отправки групп для пользователей.

Для настройки отправки группового вызова требуются следующие административные роли в зависимости от задачи.

  - **CsVoiceAdministrator:** Эта роль администратора может создавать, настраивать и управлять всеми параметрами и политиками, связанными с голосовой связью.

  - **CsUserAdministrator:** Эта роль администратора может активировать раскладки групповых звонков для пользователей. Эта роль администратора также имеет доступ к просмотру только для чтения для всех конфигураций голосовой связи.

  - **CsServerAdministrator:** Эта роль администратора может управлять работой серверов и служб, а также отслеживать их и устранять неполадки.

  - **CsAdministrator:** Эта роль администратора может выполнять все задачи CsVoiceAdministrator, CsServerAdministrator и CsUserAdministrator.

<div>


> [!NOTE]
> Подробные сведения о правах администратора можно найти <A href="lync-server-2013-planning-for-role-based-access-control.md">в разделе Планирование управления доступом на основе ролей в Lync Server 2013</A> в документации по планированию.



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

