---
title: 'Lync Server 2013: выполнение и мониторинг резервных копий'
description: 'Lync Server 2013: выполнение и мониторинг резервных копий.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Performing and monitoring backups
ms:assetid: 2df415d4-0f37-460e-99ff-4035a9a2f445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720912(v=OCS.15)
ms:contentKeyID: 63969595
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fb8ce99e850f0918974be08eb10796ef1397225
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424627"
---
# <a name="performing-and-monitoring-backups-in-lync-server-2013"></a>Выполнение и мониторинг резервных копий в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-05-15_

Ваши бизнес-приоритеты должны заключать требования к резервному копированию и восстановлению для вашей организации. Резервное копирование серверов и данных является первой строкой обороны при планировании аварии.

Компьютеры, на которых работают службы Lync Server 2013 или серверные роли, должны иметь копию текущей топологии, текущих параметров конфигурации и текущих политик, прежде чем они смогут работать в своей роли. Lync Server отвечает за то, что эти сведения передаются на каждый компьютер, на котором она требуется.

Командлеты **Export-CsConfiguration** и **Import-CsConfiguration** используются для резервного копирования и восстановления топологии сервера Lync, параметров конфигурации и политик во время обновления центрального хранилища управления. Командлеты **Export-CsConfiguration** позволяют экспортировать данные в. ZIP-файл. Затем можно использовать командлет **Import-CsConfiguration** для чтения. ZIP-файл и восстановите топологию, параметры конфигурации и политики в хранилище Центрального управления. После этого службы репликации Lync Server будут реплицировать восстановленные данные на другие компьютеры, на которых запущены службы Lync Server.

Возможность экспорта и импорта данных конфигурации также используется при начальной настройке компьютеров, расположенных в сети периметра (например, пограничных серверов). При настройке компьютера в демилитаризованной зоне сначала необходимо выполнить репликацию вручную с помощью командлетов CsConfiguration: необходимо экспортировать данные конфигурации с помощью функции **Export-CsConfiguration** , а затем скопировать. ZIP-файл на компьютер в сети периметра. После этого вы можете импортировать данные с помощью параметров **Import-CsConfiguration** и localstore. Это можно сделать только один раз. После этого репликация будет выполняться автоматически.

Кто может запустить этот командлет: по умолчанию членам указанных ниже групп разрешено локальное выполнение командлета **Export-CsConfiguration** : RTCUniversalServerAdmins. Чтобы возвратить список всех ролей RBAC, которому назначен этот командлет (в том числе любые пользовательские роли RBAC, созданные вами), выполните в командной строке Windows PowerShell следующую команду:

`Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Export-CsConfiguration"}`

Все серверные базы данных SQL 2012 должны быть архивированы в соответствии с рекомендациями [SQL](https://go.microsoft.com/fwlink/p/?linkid=290716).

Регулярное тестирование плана аварийного восстановления для инфраструктуры Lync Server 2013 следует выполнять в лабораторной среде, насколько это возможно. Дополнительные сведения об испытаниях с аварийным восстановлением можно найти в разделе ежемесячные задачи.

Обратите внимание на то, что периодичность резервного копирования можно настроить в соответствии с целями точки восстановления и точки восстановления. Рекомендуется регулярно периодически создавать моментальные снимки в течение дня. Как правило, создание полных резервных копий выполняется каждые 24 часа.

<div>

## <a name="see-also"></a>См. также


[Import-CsConfiguration](https://docs.microsoft.com/powershell/module/skype/Import-CsConfiguration)  
[Export-CsConfiguration](https://docs.microsoft.com/powershell/module/skype/Export-CsConfiguration)  
[Рекомендации по SQL](https://go.microsoft.com/fwlink/p/?linkid=290716)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

