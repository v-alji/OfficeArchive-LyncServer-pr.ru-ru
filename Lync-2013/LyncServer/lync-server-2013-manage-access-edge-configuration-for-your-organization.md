---
title: 'Lync Server 2013: управление конфигурацией пограничного сервера в организации'
description: 'Lync Server 2013: Управление настройкой Edge для Access в Организации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Access Edge Configuration for your organization
ms:assetid: 0145eb08-984f-4ecd-bf9c-364817619c2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552443(v=OCS.15)
ms:contentKeyID: 48679555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2161385f9c03f025bcf6f5e599b7e0276f6d592c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426139"
---
# <a name="manage-access-edge-configuration-for-your-organization-in-lync-server-2013"></a>Управление конфигурацией пограничного сервера в организации в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Это предварительная редакция документации и она может меняться. Пустые разделы добавлены в качестве заполнителей.

После развертывания одного или нескольких пограничных серверов необходимо разрешить типы доступа к внешнему домену или поставщику, получить доступ к удаленному пользователю, а также анонимный доступ пользователей к конференциям с помощью пограничных серверов, которые будут поддерживаться в вашей организации.

Эти параметры включают следующие типы доступа, которые можно настроить на странице **конфигурации пограничного доступа** .

  - **Включение подключения к службам федерации и общедоступных мгновенных сообщений**   Включите этот параметр, если вы хотите поддерживать доступ пользователей к доменам федеративных партнеров. Этот параметр применяется к обеим федерациям SIP и XMPP Федерации, настроенным для глобальных областей, сайтов или пользователей на странице **политики внешней доступа** . Для применения параметров Федерации необходимо настроить поддержку Федерации на обеих страницах.
    
    Существует два варианта, которые являются необязательными параметрами, определяющими способ обнаружения федеративных партнеров, а также в том случае, если вы не хотите, чтобы они были включены в список контактов
    
      - **Включение обнаружения доменных партнеров**   Выберите этот параметр, чтобы включить автоматическое обнаружение доменов, с которыми вы можете использовать федерацию. Lync Server 2013 использует DNS-записи для обнаружения доменов, не указанных в списке разрешенные домены, автоматически оценивает входящий трафик от обнаруженных федеративных партнеров и ограничивает или блокирует трафик в зависимости от уровня доверия, количества трафика и настроек администратора. Если этот флажок не установлен, для пользователей из доменов, включенных в список разрешенных доменов, будет разрешен доступ федеративного пользователя. Если вы выберете этот параметр, вы можете указать, что отдельные домены должны быть заблокированы или разрешены, включая ограничение доступа к определенным серверам, на которых запущена служба EDGE в федеративных доменах. Подробности можно найти [в разделе Настройка поддержки разрешенных внешних доменов в Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).
    
      - **Отправка заявления об отказе от архивации федеративным партнерам**   Если выбрать этот параметр, вы можете отправить сообщение об отказе на архивацию федеративным партнерам, чтобы они были извещены о том, что записываются сведения о общении. При архивации внешней связи с доменами федеративных партнеров следует включить уведомление об отказе в архивации, чтобы предупредить партнеров о том, что их сообщения и сведения о общении заархивированы вашим развертыванием. Подробнее об архивации можно найти [в разделе Определение требований для архивации в Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md).

  - **Разрешение удаленного доступа пользователей**   Включите этот параметр, если вы хотите, чтобы пользователи в вашей организации, которые находятся за пределами межсетевого экрана (например, подключены к сети, и пользователи, которые находятся в дороге), смогли подключиться к серверу Lync Server. Дополнительные сведения можно найти [в разделе Включение и отключение удаленного доступа пользователей в Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).

  - **Разрешение доступа анонимных пользователей к конференциям**   Включите этот параметр, если вы хотите, чтобы внутренние пользователи могли пригласить внешних анонимных пользователей на Конференции, которые они упорядочивают. Если этот параметр включен, анонимные пользователи не могут быть подключены к Конференции. Чтобы настроить возможности конференц-связи и параметры, определяющие, как и какие пользователи могут выполнять Конференции и как включить анонимных пользователей, ознакомьтесь со сведениями о [создании или изменении взаимодействия пользователя с Конференцией для сайта, пользователей](https://technet.microsoft.com/library/gg429715\(v=ocs.15\)) и [параметров политики конференций в Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).

<div>


> [!NOTE]  
> Помимо включения поддержки внешних пользователей, вы также можете настроить политики для управления использованием удаленного доступа пользователей в Организации, прежде чем пользователи смогут получить доступ к любому типу внешних пользователей. Дополнительные сведения о создании и настройке политик доступа внешних пользователей см. <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">в разделе Управление политикой внешнего доступа в Lync Server 2013</A>.



</div>

**Просмотр сведений о конфигурации Edge для Access с помощью командлетов Windows PowerShell**

  - Сведения о конфигурации Edge Access можно просмотреть с помощью Windows PowerShell и командлета **Get-CsAccessEdgeConfiguration** . Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .
    
    Чтобы просмотреть сведения о всех параметрах конфигурации Edge Access, введите в командной консоли Lync Server указанную ниже команду и нажмите клавишу ВВОД.
    
        Get-CsAccessEdgeConfiguration
    
    Команда возвращает примерно следующую информацию:
    
        Identity                               : Global
        AllowAnonymousUsers                    : False
        AllowFederatedUsers                    : False
        AllowOutsideUsers                      : True
        BeClearingHouse                        : False
        EnablePartnerDiscovery                 : False
        EnableArchivingDisclaimer              : False
        EnableUserReplicator                   : True
        KeepCrlsUpToDateForPeers               : True
        MarkSourceVerifiableOnOutgoingMessages : True
        OutgoingTlsCountForFederatedPartners   : 4
        DiscoveredPartnerStandardRate          : 20
        EnableDiscoveredPartnerContactsLimit   : True
        MaxContactsPerDiscoveredPartner        : 1000
        DiscoveredPartnerReportPeriodMinutes   : 60
        MaxAcceptedCertificatesStored          : 1000
        MaxRejectedCertificatesStored          : 500
        CertificatesDeletedPercentage          : 20
        RoutingMethod                          : UseDnsSrvRouting

<div>

## <a name="in-this-section"></a>Содержание

  - [Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)

  - [Включение или отключение обнаружения федеративных партнеров в Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)

  - [Включение и отключение отправки отказа от архивирования федеративным партнерам в Lync Server 2013](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

  - [Включение или отключения удаленного доступа пользователей в Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md)

  - [Включение или отключение анонимного доступа пользователей в Lync Server 2013](lync-server-2013-enable-or-disable-anonymous-user-access.md)

  - [Назначение политик конференции для поддержки анонимных пользователей в Lync Server 2013](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

