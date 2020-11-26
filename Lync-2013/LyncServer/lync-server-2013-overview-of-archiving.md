---
title: 'Lync Server 2013: обзор архивации'
description: 'Lync Server 2013: Общие сведения о том, как архивировать.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Archiving
ms:assetid: 1e3c2ef1-f561-4f57-8b6a-7d78addc1ed1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204729(v=OCS.15)
ms:contentKeyID: 48183570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 548d82d6731fd28fafbde5816a7a0dc77a1fcc02
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424830"
---
# <a name="overview-of-archiving-in-lync-server-2013"></a>Обзор архивации в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-09-30_

Архивация в Lync Server 2013 предоставляет способ архивации сообщений, отправленных с помощью Lync Server 2013.

Вы можете внедрить архивацию как часть первоначального развертывания Lync Server 2013 или добавить ее в существующее развертывание. Чтобы использовать базу данных архивации Lync Server 2013 (базы данных SQL Server) для хранения данных архивации, используйте Topology Builder, чтобы добавить базы данных в топологию, а затем опубликуйте топологию еще раз. Если все пользователи находятся в Exchange 2013 и почтовые ящики помещаются на In-Place удержание, вам не нужно обновлять топологию, но для того чтобы хранить архивированные данные в Exchange 2013, вам нужно будет только включить интеграцию с Microsoft Exchange.

При внедрении архива вы настраиваете его, чтобы указать, что заархивировано. По умолчанию ничего не архивируется. Настраивать архивирование и управлять ими можно с помощью панели управления Lync Server 2013. Вы можете реализовать архивацию для внутренней связи, внешней связи или и того, и для других. Вы можете настроить параметры архивирования всей Организации и, при необходимости, для определенных сайтов, определенных пулов и определенных пользователей и групп пользователей. Подробнее о том, как определить соответствующие параметры для Организации, можно найти [в разделе Определение требований для архивации в Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) в документации по планированию. Сведения о том, как выполняются политики архивирования и конфигурации, а также сведения о том, как [работает архивация в Lync Server 2013](lync-server-2013-how-archiving-works.md) , можно найти в документации по планированию, документации по развертыванию или документации по операциям.

</div>

<span> </span>

</div>

</div>

</div>

