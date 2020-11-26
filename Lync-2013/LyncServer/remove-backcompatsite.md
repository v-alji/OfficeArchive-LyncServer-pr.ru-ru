---
title: Удалить BackCompatSite
description: Удалите BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440305"
---
# <a name="remove-backcompatsite"></a>Удалить BackCompatSite

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-28_

После деактивации всех пулов и удаления всех пограничных серверов запустите мастер слияния построителя топологии, чтобы удалить **BackCompatSite**.

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a>Удаление несовместимого веб-сайта из построителя топологии

1.  Откройте существующее развертывание в построителе топологии.

2.  В меню **действия** выберите пункт **топология слиянием 2007 R2**.

3.  Для продолжения нажмите кнопку **Далее**.

4.  Убедитесь, что на странице **Определение устаревшего** пограничного сервера установлен пустой список пограничных серверов. Если список не пуст, удалите все старые пограничные серверы с помощью кнопки " **Удалить** ", а затем нажмите кнопку **Далее**.
    
    ![Мастер топологии слиянием, задание страницы настройки ребра](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Мастер топологии слиянием, задание страницы настройки ребра")  

5.  На странице **Определение параметров внутреннего порта SIP** нажмите кнопку **Далее**.

6.  На странице **Сводка** нажмите кнопку **Далее** , чтобы начать объединение топологий для удаления устаревшего сайта.

7.  В столбце **Status (состояние** ) убедитесь, что значение установлено **успешно** , и нажмите кнопку **Готово** , чтобы закрыть окно мастера.

8.  На левой панели построителя топологии разверните узел BackCompatSite и убедитесь, что серверы не указаны в списке.

9.  Щелкните **BackCompatSite** правой кнопкой мыши и выберите команду **Удалить**.

10. В **построителе топологии** выберите самый верхний узел **Lync Server**.

11. В меню **действие** выберите пункт **топология публикации** и нажмите кнопку **Далее**.

12. После завершения работы **мастера публикации** нажмите кнопку **Готово** , чтобы закрыть окно мастера.

</div>

</div>

<span> </span>

</div>

</div>

</div>

