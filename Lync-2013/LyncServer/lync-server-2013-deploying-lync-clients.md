---
title: 'Lync Server 2013: развертывание клиентов Lync'
description: 'Lync Server 2013: развертывание клиентов Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync clients
ms:assetid: 3d10abf2-d484-4fa0-8f10-4a5f9dfba4f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204827(v=OCS.15)
ms:contentKeyID: 48183925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09b501fc721ac880c5cf7da0293e3aa9c6443722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429988"
---
# <a name="deploying-lync-clients-in-lync-server-2013"></a>Развертывание клиентов Lync в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-03_

В Lync 2013 представлен другой подход к развертыванию клиента. В отъезде из предыдущих выпусков Lync 2013 больше не имеет собственного установщика. Вместо этого Lync входит в состав программы установки Office 2013. Чтобы развернуть Lync 2013 для пользователей, вы можете использовать способы установки Office 2013 и средства настройки.

  - **Установщик windows 2013 Office** — это установочный пакет установщика Windows, состоящий из нескольких MSI-файлов. Не зависящий от языка основной пакет MSI объединен с одним или несколькими языковыми пакетами, что в совокупности и представляет полный продукт. При настройке отдельные пакеты собираются вместе и выполняются задачи настройки и обслуживания во время и после установки Office на пользовательские компьютеры. В этой статье описано, как использовать и настраивать установщик Windows 2013 для развертывания Lync 2013.

  - **Office 2013 нажми и работай** — это программа установки, с помощью которой вы отправляете файлы установки Office пользователям из центра администрирования Microsoft 365. Администраторы могут настраивать установку с помощью средства развертывания Office для технологии "Нажми и работай". Поскольку в Office 2013 технология "нажми и работай" используется преимущественно в среде Microsoft 365, этот способ установки не подробно описан в этом разделе. Подробные сведения об использовании и настройке установки "нажми и работай" можно найти в документации по набору ресурсов Office 2013. Кроме того, вы можете скачать программы Office 2013 нажми и работай и языковых файлов в локальное расположение, что полезно, если вы хотите минимизировать потребность в сети или запретить пользователям устанавливать программное обеспечение из Интернета в соответствии с корпоративными требованиями к безопасности.

В этом разделе содержатся сведения о развертывании клиентов с помощью установщика Office 2013 на базе MSI. Основной ссылкой является документация по набору ресурсов Office 2013, в которой подробно описана процедура подготовки инфраструктуры, Настройка настройки и развертывание Office 2013. Тем не менее, вы должны использовать документацию Office в сочетании с разделами в этом разделе, которые указывают на вопросы по развертыванию, специфичные для Lync 2013.

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P>Надстройка "собрание по сети" для Lync 2013, которая поддерживает управление собраниями в клиенте обмена сообщениями и совместной работы в Outlook, устанавливается автоматически с помощью Lync 2013.</P>
> <LI>
> <P>Программа установки Office 2013 не удаляет предыдущие версии Lync и Office Communicator. Клиент Lync 2013 устанавливается параллельно с другими клиентами Lync или Office Communicator</P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a>Содержание

  - [Настройка установки клиента в Lync Server 2013](lync-server-2013-customizing-client-installation.md)

  - [Настройка поведения Lync и пользовательского интерфейса в Lync Server 2013](lync-server-2013-customizing-lync-behavior-and-the-user-interface.md)

  - [Настройка надстройки "собрание по сети" в Lync Server 2013](lync-server-2013-customizing-the-online-meeting-add-in.md)

  - [Конфигурация страницы присоединения к собранию в Lync Server 2013](lync-server-2013-configuring-the-meeting-join-page.md)

  - [Настройка поддерживаемых клиентских версий в Lync Server 2013](lync-server-2013-configuring-supported-client-versions.md)

  - [Настройка режима конфиденциальности для расширенного присутствия в Lync Server 2013](lync-server-2013-configuring-enhanced-presence-privacy-mode.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

