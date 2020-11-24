---
title: 'Lync Server 2013: настройка хранилища файлов'
description: 'Lync Server 2013: Настройка хранилища файлов DFS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DFS file storage
ms:assetid: a985be20-5a00-4f38-b45b-83dc82de3827
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205150(v=OCS.15)
ms:contentKeyID: 48185037
ms.date: 05/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d70ae93db188ec51d04dd33d6c3cb5659db5a2c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399934"
---
# <a name="configure-dfs-file-storage-for-lync-server-2013"></a>Настройка хранилища файлов для Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2016-05-23_

Lync Server 2013 поддерживает использование общих файловых ресурсов в распределенной файловой системе (DFS). Подробные сведения о DFS для Windows Server 2008 можно найти в пошаговом руководстве по DFS для Windows Server 2008 по адресу [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) . Для использования DFS сервер Lync Server 2013 должен выполнить указанные ниже действия.

  - Пространства имен основываются на доменах

  - На всех серверах пространства имен установлен минимум Windows 2008

Для установки Lync Server 2013 необходимо, чтобы разрешение на доступ к общей папке было разрешено администратору. В этом случае Lync Server 2013 будет использовать разрешения на доступ к файлам NTFS для папок ACL. Унаследованные разрешения для общего доступа к DFS не будут использоваться для ограничения доступа.

Дополнительные сведения о требованиях к общему доступу можно найти [в разделе Поддержка хранения файлов в Lync Server 2013](lync-server-2013-file-storage-support.md) в документации по поддержке.

<div>


> [!NOTE]  
> Возможно, вы ищете информацию о настройке общего доступа к сети, не относящейся к DFS. Если это так, изучите <A href="lync-server-2013-hardware-setup.md">настройку оборудования для Lync Server 2013</A>.



</div>

Ниже описано, как правильно настроить разрешения на доступ к общей папке с помощью мастера пространства имен DFS (как описано в руководстве по настройке DFS).

<div>

## <a name="to-configure-shared-folder-permissions"></a>Настройка разрешений для общей папки

1.  Нажмите кнопку **Пуск**, наведите указатель на пункт **все программы**, выберите **Администрирование**, а затем — **Управление DFS**.

2.  В дереве консоли оснастки управления DFS щелкните правой кнопкой мыши сервер пространства имен (например, filesrv1.contoso.com), а затем выберите команду **изменить параметры**.

3.  Выберите **разрешения для общей папки**.

4.  Выберите **использовать пользовательские разрешения**.

5.  Для группы администраторов выберите в разделе **разрешено** следующее:
    
      - **Полный доступ**
    
      - **Изменение**
    
      - **Читаются**

6.  Нажмите кнопку **Применить**, а затем — кнопку **ОК**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

