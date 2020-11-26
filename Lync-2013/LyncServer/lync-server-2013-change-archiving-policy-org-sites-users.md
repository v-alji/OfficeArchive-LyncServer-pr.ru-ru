---
title: 'Lync Server 2013: изменение политики архивации для включения и отключения архивирования внутренней или внешней связи для Организации, сайтов и пользователей'
description: 'Lync Server 2013: изменение политики архивации для включения или отключения архивирования внутренней или внешней связи для Организации, сайтов или пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435182"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a>Изменение политики архивации в Lync Server 2013 для включения и отключения архивирования внутренней или внешней связи для Организации, сайтов и пользователей

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

В Lync Server 2013 вы используете политики для включения и отключения архивирования для внутренних коммуникаций и внешней связи для пользователей, размещенных на Lync Server 2013. К ним относятся следующие политики архивации:

  - Глобальная политика, созданная по умолчанию при развертывании Lync Server 2013.

  - Необязательные политики уровня сайта и уровня пользователя, которые можно создавать и использовать для определения способа реализации архивации для конкретных сайтов или пользователей.

Изначально политики архивации были настроены при развертывании архивации, но вы можете изменить, добавить и удалить политики после развертывания. В панели управления Lync Server 2013 вы можете управлять политиками на глобальном уровне, уровне сайта и на уровне пользователей с помощью страницы **политики архивации** в группе **Архивация и мониторинг** . Если вы интегрирует хранилище Lync Server с хранилищем Exchange 2013, политики пользователей Exchange имеют приоритет над политиками архивации Lync Server 2013.

Сведения о том, как реализованы политики, в том числе об иерархии политик, описаны [в разделе Работа с архивацией в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.

<div>


> [!NOTE]  
> Если вы включили интеграцию Microsoft Exchange для развертывания, политики Exchange определяют, включено ли архивирование для пользователей, использующих Exchange 2013, и почтовые ящики помещаются на In-Place удержание. Подробности можно найти в разделе <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Настройка политик архивации в Lync server 2013 при использовании интеграции с Exchange Server</A> в документации по развертыванию.<BR>Перед включением архивации необходимо указать все соответствующие параметры в разделе конфигурации архивации. Дополнительные сведения можно найти в разделе <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Управление параметрами конфигурации архивации в Lync Server 2013 для Организации, сайты и пулы</A> в документации по эксплуатации.



</div>

<div>

## <a name="to-change-an-archiving-policy"></a>Изменение политики архивации

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsArchivingAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На левой панели навигации щелкните **Мониторинг и архивация**, а затем щелкните **Политика архивации**.

4.  В списке политик выполните одно из следующих действий:
    
      - Чтобы изменить политику для всего развертывания, в списке политик щелкните **Global** (Глобальная), щелкните **Edit** (Изменить), а затем — **Show details** (Показать сведения).
    
      - Чтобы изменить политику для одного сайта, выберите имя сайта в списке политик, щелкните **Edit** (Изменить) и затем щелкните **Show details** (Показать сведения).
    
      - Чтобы изменить политику для отдельного пользователя или группы пользователей, выберите имя пользователя или группы пользователей в списке политик, щелкните **Edit** (Изменить) и затем щелкните **Show details** (Показать сведения).

5.  На странице **Edit Archiving Policy** (Изменение политики архивации) выполните следующие действия:
    
      - Чтобы включить или отключить архивацию внутренних коммуникаций, установите или снимите флажок **Archive internal communications** (Архивировать внутренние коммуникации).
    
      - Чтобы включить или отключить архивацию внешних коммуникаций, установите или снимите флажок **Archive external communications** (Архивировать внешние коммуникации).

6.  Нажмите **Исполнить**.
    
    <div>
    

    > [!IMPORTANT]  
    > Параметры политики пользователя применяются только к тем пользователям и группам пользователей, к которым применяется политика. Подробнее смотрите в разделе <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">применение политики архивации для пользователей в Lync Server 2013</A>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a>Включение и отключение архивации с помощью командлетов Windows PowerShell

Архивация может быть включена и отключена (как для внутренних, так и для внешних сеансов связи) с помощью командлета **Set-CsArchivingPolicy** . Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a>Включение архивации внутренних сеансов связи

  - Чтобы включить архивацию внутренних сеансов связи, установите для свойства **ArchiveInternal** значение True ($true). Например:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a>Включение архивации внешних сеансов связи

  - Чтобы включить архивацию внешних сеансов связи, задайте для свойства **ArchiveExternal** значение True ($true). Например:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a>Включение архивации как внутренних, так и внешних сеансов связи

  - Чтобы включить архивацию внутренних и внешних сеансов связи, задайте для свойств **ArchiveInternal** и **ArchiveExternal** значение true:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a>Отключение архивации

  - Чтобы вообще отключить архивацию, установите для свойств **ArchiveInternal** и **ArchiveExternal** значение false ($false). Например:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

Дополнительные сведения можно найти в разделе справки по командлету [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) .

</div>

<div>

## <a name="see-also"></a>См. также


[Управление архивированием внутренней и внешней связи в Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

