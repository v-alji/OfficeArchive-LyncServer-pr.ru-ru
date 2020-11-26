---
title: 'Lync Server 2013: включение или отключение обнаружения федеративных партнеров'
description: 'Lync Server 2013: Включение и отключение обнаружения партнеров Федерации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable discovery of federation partners
ms:assetid: 91fd036b-b1af-47cf-b1cf-0aa0a783c2aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182550(v=OCS.15)
ms:contentKeyID: 48184857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36b91120ffc1ce2bd6cd8b8114f0330e6d39d996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428904"
---
# <a name="enable-or-disable-discovery-of-federation-partners-in-lync-server-2013"></a>Включение или отключение обнаружения федеративных партнеров в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

На момент развертывания пограничных серверов и включения Федерации для Организации необходимо указать, следует ли поддерживать автоматическое обнаружение доменов федеративных партнеров. Чтобы изменить конфигурацию, воспользуйтесь процедурой, описанной в этом разделе.

<div>


> [!NOTE]  
> В описанной ниже процедуре предполагается, что вы уже включили Федерацию для своей организации. Дополнительные сведения о включении Федерации можно найти <A href="lync-server-2013-enable-or-disable-remote-user-access.md">в разделе Включение и отключение удаленного доступа пользователей в Lync Server 2013</A> в документации по развертыванию или документации по эксплуатации.



</div>

<div>

## <a name="to-enable-or-disable-automatic-discovery-of-federated-domains-for-your-organization"></a>Включение и отключение автоматического обнаружения федеративных доменов для Организации

1.  Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите **внешний пользовательский доступ**, а затем — **Конфигурация Edge Access**.

4.  На странице **конфигурации Edge Access** щелкните **Глобальная**, выберите пункт **изменить**, а затем — **Показать подробности**.

5.  В диалоговом окне **изменение конфигурации Edge для доступа** в разделе **включить связь с федеративными пользователями** установите или снимите флажок **включить обнаружение домена партнера** , чтобы включить или отключить автоматическое обнаружение доменных партнеров.

6.  Нажмите **Исполнить**.

Чтобы включить Федеративные пользователи для совместной работы с пользователями в развертывании Lync Server, необходимо также настроить по крайней мере одну политику внешнего доступа для поддержки федеративного доступа пользователей. Дополнительные сведения можно найти [в разделе Включение и отключение подключения к службам интеграции и обмена мгновенными сообщениями в Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) в документации по развертыванию или документации по операциям. Дополнительные сведения об управлении доступом для определенных федеративных доменов можно найти [в разделе Управление федеративными доменами SIP для Организации в](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)lync Server 2013, [управлять ФЕДЕРАТИВНЫМИ поставщиками SIP для Организации в Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) и [управлять XMPP федеративных партнерами в Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) в документации по эксплуатации.

</div>

<div>

## <a name="enabling-or-disabling-discovery-of-federation-partners-by-using-windows-powershell-cmdlets"></a>Включение и отключение обнаружения партнеров Федерации с помощью командлетов Windows PowerShell

Можно управлять обнаружением партнеров Федерации с помощью Windows PowerShell и командлетом Set-CsAccessEdgeConfiguration. Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-enable-discovery-of-federation-partners"></a>Включение обнаружения партнеров Федерации

  - Чтобы включить обнаружение партнеров Федерации, задайте для свойства **EnablePartnerDiscovery** значение True ($true). Обратите внимание, что для изменения значения этого свойства необходимо включить маршрутизацию DNS SRV.
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $True

</div>

<div>

## <a name="to-disable-discovery-of-federation-partners"></a>Отключение обнаружения партнеров Федерации

  - Чтобы отключить обнаружение партнеров Федерации, установите для свойства **EnablePartnerDiscovery** значение False ($false):
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $False

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

