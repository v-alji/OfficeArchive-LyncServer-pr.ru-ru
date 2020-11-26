---
title: 'Lync Server 2013: Настройка поддержки автообнаружения'
description: 'Lync Server 2013: Настройка поддержки автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Autodiscover
ms:assetid: 3a266456-69a0-4539-ba99-d388b83799a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945622(v=OCS.15)
ms:contentKeyID: 51541463
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23991f2f9467035f4ba461ff1b6a84fa8ed1a11d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432613"
---
# <a name="configuring-support-for-autodiscover-in-lync-server-2013"></a>Настройка поддержки автообнаружения в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-01-21_

**Служба автообнаружения** веб-служб Lync Server впервые появилась в накопительном обновлении lync Server 2010: Ноябрь 2011. Это обновление сопровождается первоначальным выпуском мобильных клиентов Lync. Служба автообнаружения предоставляет службы Mobility Services, называемые службой MCX.

Служба автообнаружения действует как единое место для всех клиентов, которые запрашивают сведения о доступных службах и функциях, а также о том, как связаться с sevices — либо полным доменным именем, либо ссылкой на указатель URL-адреса. Функция автообнаружения предоставляет ряд функций, и каждый клиент будет выполнять запросы на основании функций, которые может использовать клиент. Например, классическое приложение Lync 2013 будет использовать autodiscvoer для определения внешней веб-службы, но не будет использовать службы Mobility (MCX). Чтобы правильно определить и позволить клиентам использовать доступные для них функции, необходимо определить сценарии, позволяющие клиенту эффективно находить и использовать записи автообнаружения. Для использования autodoscover необходимо, чтобы на обратном прокси публикуются веб-службы Lync Server, что записи DNS настроены для разрешения запросов DNS для службы автообнаружения сервера Lync Server и веб-служб Lync Server, а также для того, чтобы службы сертификации правильно настроились для вашего конкретного сценария.

<div>


> [!TIP]  
> Технические сведения о том, какие элементы содержатся в запросе и ответе автообнаружения, приведены <A href="lync-server-2013-understanding-autodiscover.md">в разделе Общие сведения о автообнаружения в Lync Server 2013</A>.



</div>

Следующие данные и таблицы определяют, какие конфигурации (если таковые имеются) необходимо реализовать для обеспечения полного и эффективного использования службы автообнаружения. Сведения в указанных ниже разделах относятся к Microsoft Lync Server 2013. Если вы ищете руководство по планированию мобильных устройств для Lync Server 2010, ознакомьтесь с разрешениями [https://go.microsoft.com/fwlink/?LinkId=275113](https://go.microsoft.com/fwlink/?linkid=275113) . Развертывание мобильных устройств для Lync Server 2010 можно найти в разделе [https://go.microsoft.com/fwlink/?LinkId=275114](https://go.microsoft.com/fwlink/?linkid=275114)

<div>

## <a name="in-this-section"></a>Содержание

  - [Настройка DNS для автообнаружения в Lync Server 2013](lync-server-2013-configuring-dns-for-autodiscover.md)

  - [Настройка сертификатов для автообнаружения в Lync Server 2013](lync-server-2013-configuring-certificates-for-autodiscover.md)

  - [Настройка обратного прокси-сервера для автообнаружения в Lync Server 2013](lync-server-2013-configuring-a-reverse-proxy-for-autodiscover.md)

  - [Настройка автообнаружения в Lync Server 2013 для гибридных развертываний](lync-server-2013-configuring-autodiscover-for-hybrid-deployments.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

