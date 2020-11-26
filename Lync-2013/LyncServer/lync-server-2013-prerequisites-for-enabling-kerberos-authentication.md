---
title: 'Lync Server 2013: необходимые условия для включения проверки подлинности Kerberos'
description: 'Lync Server 2013: предварительные условия для включения проверки подлинности Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for enabling Kerberos authentication
ms:assetid: 3f276a21-7476-4bc0-9fd1-59e844d2e9c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425909(v=OCS.15)
ms:contentKeyID: 48183945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65a45bad0eb249fdbc717fe05f080ce737c87c6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436974"
---
# <a name="prerequisites-for-enabling-kerberos-authentication-in-lync-server-2013"></a>Необходимые условия для включения проверки подлинности Kerberos в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-21_

Перед включением проверки подлинности Kerberos убедитесь, что выполнены все необходимые требования к конфигурации и инфраструктуре.

  - Схема Active Directory расширена для Lync Server 2013.

  - Подготовка леса Active Directory для Lync Server 2013 завершена.

  - Подготовка домена Active Directory для Lync Server 2013 завершена.

  - Хранилище Central Management успешно установлено и доступно.

  - Топология создана и опубликована с помощью построителя топологии.

  - Серверы и роли, для которых требуются веб-службы, были определены и развернуты, в том числе серверы переднего плана, серверы Standard Edition и режиссеры.

  - Службы IIS настраиваются и развертываются с помощью рекомендованных служб ролей для поддержки веб-служб в Lync Server 2013.

После выполнения необходимых условий вы должны будете создать одну или несколько учетных записей для веб-служб, которые будут использоваться для проверки подлинности Kerberos для развертывания. Как минимум, вам нужно создать для каждого развертывания один из учетных записей проверки подлинности Kerberos. Однако вы можете создать учетную запись для каждого сайта, чтобы предоставить локальную проверку подлинности Kerberos на сайте. Вы можете указать только одну учетную запись для проверки подлинности Kerberos для сайта.

</div>

<span> </span>

</div>

</div>

</div>

