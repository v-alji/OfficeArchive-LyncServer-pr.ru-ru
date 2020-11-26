---
title: 'Lync Server 2013: классы и описания схемы'
description: 'Lync Server 2013: классы и описания схемы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema classes and descriptions
ms:assetid: 7d43b920-ac37-40cc-adfe-be289bda6e9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398625(v=OCS.15)
ms:contentKeyID: 48184612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec27c2e00a7f969dbc13c91b06313c8045894a9e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441972"
---
# <a name="schema-classes-and-descriptions-in-lync-server-2013"></a>Классы схем и описания в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-30_

В этом разделе описаны все классы схем, используемые в Lync Server 2013.

<div>

## <a name="schema-classes-and-descriptions"></a>Классы и описания схемы


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Классов</th>
<th>Описание</th>
<th>Комментарии</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Mail-Recipient</p></td>
<td><p>Сообщение электронной почты в единой системе обмена сообщениями Exchange (UM).</p></td>
<td><p>Этот вспомогательный класс предоставляется в единой системе обмена сообщениями Exchange.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-ApplicationContacts</p></td>
<td><p>Этот класс является контейнером для нескольких контактов приложения и не содержит самих атрибутов.</p></td>
<td><p>Новые возможности Microsoft Office Communications Server 2007 R2.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-ApplicationServer</p></td>
<td><p>Этот класс содержит запись для точки управления службой для экземпляра служб единой системы обмена сообщениями (UCAS).</p></td>
<td><p>Новые возможности Office Communications Server 2007 R2.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-ApplicationServerService</p></td>
<td><p>Этот класс предоставляет ассоциацию от определенного пула к его службе приложения.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-ApplicationServerSettings</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-ApplicationServer содержит атрибуты, представляющие параметры для экземпляров службы приложения.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP — Архив (устарело)</p></td>
<td><p>Этот вспомогательный класс в msRTCSIP-GlobalContainer содержит все параметры, связанные с архивацией.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-ArchivingServer (устарело)</p></td>
<td><p>Этот класс представляет собой один сервер архивирования для обмена мгновенными сообщениями. Экземпляр этого класса создается, когда компьютер активируется в качестве сервера архивации мгновенных сообщений, например с компьютера, на котором установлена служба архивации мгновенных сообщений.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-ConferenceDirectories</p></td>
<td><p>Этот класс является контейнером для нескольких экземпляров каталогов конференций и не содержит самих атрибутов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-ConferenceDirectory</p></td>
<td><p>Этот класс содержит атрибуты, представляющие параметры для определенного каталога конференций.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-ConnectionPoint</p></td>
<td><p>Общая точка управления службой (SCP) для указания компьютера в качестве сервера, на котором работает Lync Server.</p></td>
<td><p>Новые возможности в Lync 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-DefaultCWABank</p></td>
<td><p>Этот вспомогательный класс содержит параметры банка Microsoft Lync Web App.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-Domain (домен)</p></td>
<td><p>Этот класс содержит атрибуты, определяющие настроенные домены регистратора SIP.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-EdgeProxy</p></td>
<td><p>Этот контейнер класса представляет одну службу пограничного доступа. Поскольку служба Edge Access развернута в демилитаризованной зоне, а пользователи обычно не разрешают доступ доменных служб Active Directory из сети периметра, то экземпляры службы Edge Access не присоединяются к сети Active Directory в интрасети. Таким образом, прокси-серверы доступа не регистрируются автоматически в доменных СЛУЖБах Active Directory. Администратор должен вручную настроить существование каждого экземпляра службы пограничного доступа в AD DS.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-EnterpriseMCUSettings</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-MCU содержит атрибуты, представляющие параметры серверов конференций.</p></td>
<td><p>Новые возможности Microsoft Office Communications Server 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-EnterpriseMediationServerSettings</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-MediationServer содержит атрибуты, представляющие параметры серверов-исправлений.</p></td>
<td><p>Новые возможности Office Communications Server 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-EnterpriseServerSettings</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-Server содержит атрибуты, представляющие параметры для серверов SIP.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-Federation</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит все параметры, связанные с интеграцией.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-GlobalContainer</p></td>
<td><p>Этот класс содержит все параметры, которые применяются во время развертывания Lync Server.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-GlobalUserPolicy (устарело)</p></td>
<td><p>Этот класс представляет одну политику собраний Office Communications Server.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-GlobalTopologySetting</p></td>
<td><p>Объект локального глобального параметра топологии.</p></td>
<td><p>Новые возможности Lync Server 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-GlobalTopologySettings</p></td>
<td><p>Контейнер для размещения глобальных объектов параметров топологии.</p></td>
<td><p>Новые возможности Lync Server 2010.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-LocalNormalization</p></td>
<td><p>Этот класс является контейнером, представляющим экземпляр правила нормализации расположения.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-LocationContactMapping</p></td>
<td><p>Этот класс создается приложением для проведения конференций и содержит атрибуты, которые используются для классификации телефонных номеров конференций по регионам.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-LocationContactMappings</p></td>
<td><p>Этот класс является контейнером для нескольких экземпляров сопоставлений контактов местоположения и не содержит самих атрибутов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-LocationProfile</p></td>
<td><p>Этот класс является контейнером, представляющим определенный профиль расположения.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-LocationProfiles (устарело)</p></td>
<td><p>Этот класс является контейнером для нескольких профилей местоположения и не содержит самих атрибутов.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-LocalNormalizations (устарело)</p></td>
<td><p>Этот класс является контейнером для нескольких локальных правил нормализации и не содержит самих атрибутов.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-MCU</p></td>
<td><p>Этот класс представляет один сервер конференц-связи.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-MCUFactories</p></td>
<td><p>Этот класс содержит несколько классов msRTCSIP-MCUFactory и не имеет самих атрибутов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-MCUFactory</p></td>
<td><p>Этот класс является контейнером, представляющим фабрику серверов конференций для одного типа носителя. Экземпляр этого класса создается при активации первого сервера конференций для этого конкретного типа и поставщика.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-MCUFactoryService</p></td>
<td><p>Этот класс обеспечивает связь определенного пула с его фабрикой серверов конференций.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-MediationServer</p></td>
<td><p>Этот класс содержит запись для точки управления службой для сервера-посредника.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP — собрание (устарело)</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, которые представляют настраиваемые параметры собрания.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP — мобильность</p></td>
<td><p>Контейнер, в котором хранятся глобальные параметры мобильности.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-MonitoringServer</p></td>
<td><p>Этот класс содержит атрибуты, представляющие параметры для одного сервера мониторинга.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007 R2.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-PhoneRoute (устарело)</p></td>
<td><p>Этот класс является контейнером, представляющим собой экземпляр наименее затратный маршрут к шлюзу или набору шлюзов. Эти сведения используются всеми корпоративными пулами или серверами Standard Edition для маршрутизации исходящих звонков в коммутируемую телефонную сеть общего пользования (PSTN) в наиболее экономичном виде.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-PhoneRoutes (устарело)</p></td>
<td><p>Этот класс является контейнером для нескольких маршрутов с наименьшей стоимостью и не содержит самих атрибутов.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP — стратегии (устаревшие)</p></td>
<td><p>Этот класс содержит несколько классов политики Lync Server и не имеет самих атрибутов.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP — пул</p></td>
<td><p>Этот класс представляет один пул сервера Lync Server.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP (пулы)</p></td>
<td><p>Этот класс содержит несколько пулов серверов Lync и не имеет самих атрибутов.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-PoolService</p></td>
<td><p>Этот класс представляет контрольную точку элемента управления pointservice для пула. Пользователи, размещенные в пуле, имеют в качестве точки атрибута msRTCSIP-PrimaryHomeServer экземпляр этого класса.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP — присутствие</p></td>
<td><p>Контейнер, в котором хранятся глобальные параметры присутствия.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-регистратор</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, представляющие параметры пользователя, поддерживаемые серверами регистратора SIP.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-RouteUsage (устарело)</p></td>
<td><p>Этот класс является контейнером, представляющим экземпляр использования телефонной маршрутизации. Класс использования для телефонных маршрутов состоит из поля атрибута и поля Описание. Поле атрибута определяет тип использования. Поле «Описание» позволяет администраторам описать использование этого атрибута в телефонном маршруте.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-RouteUsages (устарело)</p></td>
<td><p>Этот класс содержит несколько экземпляров класса msRTCSIP-RouteUsage и не содержит самих атрибутов.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-Поиск</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, которые ограничивают область результатов поиска и управляют ей.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-Server (сервер)</p></td>
<td><p>Этот класс представляет один сервер, на котором работает Lync Server.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-Service</p></td>
<td><p>Этот класс содержит контейнер глобальных параметров и объект msRTCSIP-domain.</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-TrustedMCU</p></td>
<td><p>Этот класс содержит атрибуты, представляющие параметры для надежного сервера конференц-связи.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-TrustedMCUs</p></td>
<td><p>Этот класс содержит несколько экземпляров класса msRTCSIP-TrustedMCU и не содержит самих атрибутов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-TrustedProxies</p></td>
<td><p>Этот класс содержит несколько классов msRTCSIP-TrustedProxy и не содержит самих атрибутов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-TrustedProxy</p></td>
<td><p>Этот класс является контейнером, представляющим сервер, на котором запущен прокси-сервер. Экземпляр этого класса создается при активации нового прокси-сервера на компьютере, Соединенном с AD DS.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-TrustedServer</p></td>
<td><p>Этот класс содержит атрибуты, представляющие параметры для доверенного сервера.</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-TrustedService</p></td>
<td><p>Этот класс является контейнером, представляющим доверенную службу, которая поддерживает маршрутизацию с помощью глобально маршрутизируемой URL-адреса агента пользователя (GRUU). Экземпляр этого класса создается, когда активируется новый сервер, являющийся надежным для сервера Lync Server. Этот доверенный сервер должен быть присоединен к домену Active Directory.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-TrustedServices</p></td>
<td><p>Этот класс является контейнером для нескольких серверов GRUU и не содержит самих атрибутов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-TrustedWebComponentsServer</p></td>
<td><p>Этот класс содержит атрибуты, представляющие параметры надежного веб-компонента.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-TrustedWebComponentsServers</p></td>
<td><p>Этот класс содержит несколько экземпляров класса msRTCSIP-TrustedWebComponentServer и не содержит самих атрибутов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-UnifiedCommunications (устарело)</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, связанные с единым обменом данными.</p></td>
<td><p>Устаревшие в Lync Server 2010.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP — компоненты</p></td>
<td><p>Этот класс содержит контрольную точку управления службой pointservice для сервера IIS. Он определяет сервер как сервер веб-компонентов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="even">
<td><p>msRTCSIP-WebComponentsService</p></td>
<td><p>Этот класс предоставляет ассоциацию из определенного пула к веб-компонентам, которые будут использоваться пулом.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
<tr class="odd">
<td><p>msRTCSIP-WebComponentSettings</p></td>
<td><p>Этот вспомогательный класс для msRTCSIP-компонентов содержит атрибуты, представляющие параметры для веб-компонентов.</p></td>
<td><p>Новые возможности коммуникационного сервера 2007.</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

