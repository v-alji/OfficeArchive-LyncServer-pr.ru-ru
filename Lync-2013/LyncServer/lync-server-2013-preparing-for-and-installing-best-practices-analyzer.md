---
title: 'Lync Server 2013: подготовка к установке и установка анализатора соответствия рекомендациям'
description: 'Lync Server 2013: подготовка к установке и установка анализатора соответствия рекомендациям.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing for and installing Best Practices Analyzer
ms:assetid: 550613dd-dc08-482e-9980-a3fe187cd162
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591347(v=OCS.15)
ms:contentKeyID: 48184149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 005c5ac372a3564e74af549832830ebae899e9d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424144"
---
# <a name="preparing-for-and-installing-best-practices-analyzer-in-lync-server-2013"></a>Подготовка и установка анализатора соответствия рекомендациям в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-11-07_

Для выполнения задач, описанных в этом разделе, необходимо войти в систему в качестве члена группы администраторов.

<div>

## <a name="system-requirements-for-best-practices-analyzer-installation"></a>Требования к системе для установки анализатора соответствия рекомендациям

Для запуска Lync Server 2013, анализатора соответствия рекомендациям для проверки среды на компьютере должна быть установлена версия 64-bit Edition одной из указанных ниже операционных систем.

  - Стандартная операционная система Windows Server 2008 R2 с пакетом обновления 1 (SP1)

  - Операционная система Windows Server 2008 R2 с пакетом обновления 1 (SP1)

  - Windows Server 2008 R2 с пакетом обновления 1 (SP1) для операционной системы Datacenter

  - Операционная система Windows Server 2012 Datacenter

  - Операционная система Windows Server 2012 Standard

  - Операционная система Windows Server 2012 Enterprise

  - Операционная система Windows Server 2012 R2 Datacenter

  - Операционная система Windows Server 2012 R2 Standard

  - Операционная система Windows Server 2012 R2 Enterprise

  - Операционная система Windows 8

  - Операционная система Windows 7

На компьютере должны быть также запущены следующие возможности:

  - Microsoft .NET Framework 4,5. Для Lync Server 2013 необходимо вручную установить 64-разрядную версию Microsoft .NET Framework 4,5 на сервере перед установкой Lync Server 2013.

  - Lync Server 2013, основные компоненты.

  - Пакет обратной совместимости WMI. Дополнительные сведения можно найти в разделе [Установка пакета обратной СОВМЕСТИМОСТИ WMI](install-wmi-backward-compatibility-package.md) в документации по миграции.

  - Windows PowerShell 3,0. Дополнительные сведения можно найти в разделе [Установка Windows PowerShell 3,0 для Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) в документации по развертыванию.

Вы можете установить анализатор соответствия рекомендациям на компьютерах с поддерживаемой операционной системой, не использующей Lync Server 2013, основные компоненты или пакет обратной совместимости WMI, но вы можете использовать анализатор соответствия рекомендациям только для того, чтобы просматривать отчеты, а не выполнять проверки.

</div>

<div>

## <a name="choosing-a-computer-for-installation"></a>Выбор компьютера для установки

Мы рекомендуем установить Lync Server 2013, анализатор соответствия рекомендациям на компьютере, специально предназначенном для управления Lync Server 2013. Вы можете установить этот инструмент на сервер, на котором работает Lync Server 2013 или административный компьютер, на котором запущены средства администрирования Lync Server 2013. Если вы установили средство на сервер, на котором работает Lync Server, мы рекомендуем использовать это средство для проверки только этого сервера.

</div>

<div>

## <a name="installing-best-practices-analyzer"></a>Установка анализатора соответствия рекомендациям

Вы можете скачать анализатор соответствия рекомендациям для Lync Server 2013 по адресу [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539) .

Чтобы установить анализатор соответствия рекомендациям, запустите файл установщика Microsoft RtcBPA.msi на компьютере, на котором вы хотите установить средство, и следуйте инструкциям на экране. По умолчанию для установки программных файлов устанавливаются файлы \<system drive\> \\ программы \\ Lync Server 2013 \\ BPA.

</div>

</div>

<span> </span>

</div>

</div>

</div>

