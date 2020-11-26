---
title: Удаление пула переднего плана или сервера Standard Edition
description: Удалите интерфейс пула переднего плана или сервер Standard Edition.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440278"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a>Удаление пула переднего плана или сервера Standard Edition

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-04_

В этой статье описано, как удалить интерфейс переднего плана или сервер стандартного выпуска Standard Edition. При удалении пула переднего плана удаляется каждый сервер переднего плана, который входит в состав пула, в процессе удаления пула. При удалении стандартного внешнего сервера выпусков необходимо удалить определение хранилища SQL из построителя топологии.

<div>

## <a name="to-remove-a-front-end-server-pool"></a>Удаление пула серверов переднего плана

1.  Открытие построителя топологии.

2.  Перейдите на узел Lync Server 2010.

3.  Разверните **Пулы переднего плана Enterprise Edition**, разверните пул переднего плана, щелкните правой кнопкой мыши пул переднего плана, который вы хотите удалить, и выберите команду **Удалить**.

4.  Опубликуйте топологию, проверьте состояние репликации, а затем при необходимости запустите мастер развертывания Lync Server.

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a>Удаление стандартного внешнего сервера выпуска

1.  Открытие построителя топологии.

2.  Перейдите на узел Lync Server 2010.

3.  Разверните узел **стандартные базовые серверы выпусков**, щелкните правой кнопкой мыши сервер переднего плана, который вы хотите удалить, и выберите команду **Удалить**.

4.  Разверните **хранилища SQL**, щелкните правой кнопкой мыши базу данных SQL Server, связанную со стандартным сервером переднего плана выпуска, и выберите команду **Удалить**.
    
    <div>
    

    > [!IMPORTANT]  
    > Необходимо удалить определение размещенных баз данных SQL Server на стандартном внешнем сервере выпуска.

    
    </div>

5.  Опубликуйте топологию, проверьте состояние репликации, а затем при необходимости запустите мастер развертывания Lync Server.

</div>

</div>

<span> </span>

</div>

</div>

</div>

