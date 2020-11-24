---
title: 'Lync Server 2013: поддержка интеграции размещенной единой системы обмена сообщениями Exchange'
description: Платформа Lync Server 2013, поддерживающая интеграцию интегрированной среды обмена сообщениями.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for hosted Exchange UM integration
ms:assetid: c7573ec3-013c-48d9-b59b-2a5427e6da35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398821(v=OCS.15)
ms:contentKeyID: 48185376
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88920667d703bc634921903e8e3995cb65db6873
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398119"
---
# <a name="support-for-hosted-exchange-um-integration-in-lync-server-2013"></a>Поддержка интеграции размещенной единой системы обмена сообщениями Exchange в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-21_

Приложение Lync Server 2013 ExUM поддерживает интеграцию с единой системой обмена сообщениями Exchange (UM) в локальной среде, где Lync Server 2013 и Exchange UM установлены локально внутри организации, или в единой системе обмена сообщениями Exchange, размещенной поставщиком услуг, как показано на следующей схеме.

![Развертывание локальной системы обмена сообщениями на сервере Lync Server](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "Развертывание локальной системы обмена сообщениями на сервере Lync Server")

Поддерживаются перечисленные ниже режимы.

  - **Локальный режим**   Lync Server 2013 и Exchange разворачиваются на локальных серверах в рамках предприятия.

  - **Режим взаимодействия с несколькими организациями**   Lync Server 2013 развертывается на локальных серверах организации, а UM-служба Exchange размещается в средстве поставщика Интернет-услуг, например в центре обработки данных Microsoft Exchange Online.

  - **Смешанный режим**   В развертывании Lync Server 2013 есть некоторые почтовые ящики пользователей, расположенные на локальных серверах, на которых работает Microsoft Exchange Server, а некоторые почтовые ящики расположены в центре данных размещенных служб Exchange.
    
    <div>
    

    > [!NOTE]  
    > Смешанный режим можно использовать в качестве переходного решения во время оценки и Stepwise миграции пользователей на размещенную систему обмена СООБЩЕНИЯми Exchange или как постоянное решение, если вы не хотите, чтобы некоторые пользователи работали в локальной среде обмена СООБЩЕНИЯми после миграции других пользователей.

    
    </div>

Чтобы интегрировать Lync Server 2013 с размещенной единой системой обмена сообщениями Exchange, необходимо настроить *Общее адресное пространство SIP* (также называемое *разделенным доменом*). В этой конфигурации как в Lync Server 2013, так и в поставщике служб UM стороннего поставщика могут получить доступ к тому же адресному пространству домена SIP. Подробности можно найти [в разделе Архитектура интеграции единой системы обмена сообщениями Exchange в Lync Server 2013](lync-server-2013-hosted-exchange-um-integration-architecture.md) в документации по планированию.

</div>

<span> </span>

</div>

</div>

</div>

