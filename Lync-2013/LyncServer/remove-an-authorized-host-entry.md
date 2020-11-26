---
title: Удаление авторизованной записи узла
description: Удаление авторизованной записи узла.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove an authorized host entry
ms:assetid: 56a04140-347e-4eef-bede-0e858534f71e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204902(v=OCS.15)
ms:contentKeyID: 48184177
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95aa8df1745ad3108654fcb9b441b5919d42ec40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443260"
---
# <a name="remove-an-authorized-host-entry"></a>Удаление авторизованной записи узла

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-26_

В этой статье описано, как удалить устаревшую авторизованную запись узла (которая называется *надежной записью приложения* в Lync Server 2013). Вы должны удалить существующие авторизованные записи узла для всех шлюзов SIP/CSTA в Office Communications Server 2007 R2, когда вы перенесете управление удаленным звонком в развертывание Lync Server 2013. Для удаления существующих авторизованных записей узла необходимо использовать средства администрирования, входящие в состав Office Communications Server 2007 R2.

<div>

## <a name="to-remove-an-authorized-host-entry-in-an-office-communications-server-2007-r2-deployment"></a>Удаление авторизованной записи узла в развертывании Office Communications Server 2007 R2

1.  Откройте консоль администрирования Office Communications Server 2007 R2.

2.  Разверните дерево и щелкните правой кнопкой мыши пул, в котором был создан авторизованный узел.

3.  Нажмите кнопку **Свойства**, а затем — **Свойства Front End**.

4.  Откройте вкладку **авторизация узла** .

5.  Выберите сервер, а затем нажмите кнопку **Удалить**.

6.  В окне " **Свойства**" нажмите кнопку **ОК**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

