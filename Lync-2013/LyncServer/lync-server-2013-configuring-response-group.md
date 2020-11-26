---
title: 'Lync Server 2013: настройка группы ответа'
description: 'Lync Server 2013: Настройка группы ответа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Response Group
ms:assetid: c56db929-cb21-4af0-be3f-c8f807b78a5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205249(v=OCS.15)
ms:contentKeyID: 48185359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92674bb971ec5216051d75d788dc58b9c7ca641c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432690"
---
# <a name="configuring-response-group-in-lync-server-2013"></a>Настройка группы ответа в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-30_

Группа ответа — это корпоративная функция голосовой связи, которая направляет входящие звонки на группы пользователей, называемые *агентами*, например службой поддержки пользователей или рабочим столом.

Компоненты, необходимые для группы ответа, устанавливаются и включаются автоматически на сервере переднего плана или стандартном сервере Standard Edition при развертывании корпоративной голосовой связи. Чтобы предоставить доступ к группе ответа пользователям, необходимо настроить группы агента, затем очереди и рабочие процессы. Кроме того, администратор группы ответа может делегировать настройку существующего рабочего процесса в Диспетчер групп ответа, который может затем изменить и повторно настроить рабочий процесс, а также связанные группы агентов и очереди.

В этом разделе рассказывается, как настроить группу ответа Lync Server 2013. Предполагается, что вы уже прочитали разделы планирование, связанные с группой ответа и развернули сервер Enterprise Edition либо сервер Standard Edition с корпоративной голосовой связью.

<div>


> [!TIP]  
> Сведения о создании группы ответа с помощью командной консоли Lync Server Management Shell, включая пример сценария, приведены в разделе "Создание первой группы ответа с помощью командной консоли Lync Server" <A href="https://go.microsoft.com/fwlink/p/?linkid=204108">https://go.microsoft.com/fwlink/p/?linkId=204108</A> .



</div>

<div>

## <a name="in-this-section"></a>Содержание

  - [Разрешения и необходимые условия для настройки группы ответа в Lync Server 2013](lync-server-2013-response-group-configuration-permissions-and-prerequisites.md)

  - [Процесс развертывания группы ответа в Lync Server 2013](lync-server-2013-deployment-process-for-response-group.md)

  - [Обзор сценариев создания рабочих процессов в Lync Server 2013](lync-server-2013-overview-of-workflow-creation-scenarios.md)

  - [Создание групп агента группы ответа Lync Server 2013](lync-server-2013-create-response-group-agent-groups.md)

  - [Создание очередей группы ответа в Lync Server 2013](lync-server-2013-create-response-group-queues.md)

  - [Необязательно Определение группы ответа в рабочее время в Lync Server 2013](lync-server-2013-optional-define-response-group-business-hours.md)

  - [Необязательно Определение наборов праздников группы ответа в Lync Server 2013](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [Создание рабочих процессов для группы ответа в Lync Server 2013](lync-server-2013-create-response-group-workflows.md)

  - [Необязательно Проверка развертывания группы ответа в Lync Server 2013](lync-server-2013-optional-verify-response-group-deployment.md)

</div>

<div>

## <a name="see-also"></a>См. также


[Планирование функций управления звонками в Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

