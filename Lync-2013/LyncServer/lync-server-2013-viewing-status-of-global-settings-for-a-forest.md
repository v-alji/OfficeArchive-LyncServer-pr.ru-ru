---
title: 'Lync Server 2013: Просмотр состояния глобальных параметров для леса'
description: 'Lync Server 2013: Просмотр состояния глобальных параметров для леса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View status of global settings for a forest
ms:assetid: 2ab0f2f1-9908-4e6f-aff3-d6b3cc474b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747889(v=OCS.15)
ms:contentKeyID: 63969590
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9f722ea66f6c54c816703bd1af1d3def57bbd84
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443911"
---
# <a name="view-status-of-global-settings-for-a-forest-in-lync-server-2013"></a>Просмотр состояния глобальных параметров для леса в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-05-20_

Администраторам ежемесячно просматривайте глобальные параметры развертывания Lync Server 2013. Цель состоит в том, чтобы проанализировать реализованные параметры для набора известных конфигураций — базовой конфигурации, чтобы гарантировать допустимость параметров, а также определить, следует ли обновлять базовую документацию. Изменения в глобальных параметрах должны быть реализованы с помощью процесса управления изменениями, который включает в себя документирование новых параметров.

Глобальные параметры, которые необходимо проверить, описаны в следующих разделах:

<div>

## <a name="check-general-settings"></a>Проверка общих параметров

Проверьте общие параметры, включая домены, поддерживаемые протоколом SIP для Lync Server 2013.

Данные домена SIP можно вернуть с помощью Windows PowerShell и командлета **Get-CsSipDomain** . Чтобы вернуть эти данные, запустите `Get-CsSipDomain` команду Windows PowerShell.

Get-CsSipDomain будет возвращать такие сведения, как для всех авторизованных доменов SIP:

Имя удостоверения по умолчанию

\-------- ---- ---------

fabrikam.com fabrikam.com истина

na.fabrikam.com na.fabrikam.com ложь

Если для свойства по умолчанию задано значение "true", соответствующий домен является доменом SIP по умолчанию. Вы можете использовать командлет Set-CsSipDomain для изменения домена SIP по умолчанию для Организации. Однако вы не можете просто удалить стандартный домен SIP, так как это оставит без домена по умолчанию. Если вы хотите удалить домен fabrikam.com (как показано в предыдущем примере), сначала необходимо настроить na.fabrikam.com в качестве домена по умолчанию.

</div>

<div>

## <a name="check-meeting-settings"></a>Проверка параметров собрания

Параметры собрания включают определения политик собраний и поддержку участия анонимных пользователей в собраниях.

Параметры конфигурации собраний можно получить с помощью Windows PowerShell и командлета **Get-CsMeetingConfiguration** . Например, эта команда возвращает сведения о глобальных параметрах конфигурации собраний.

Параметры конфигурации собрания "Глобальный" Get-CsMeetingConfiguration также можно настроить в области сайта. По этой причине вы можете использовать следующую команду, которая возвращает сведения о всех параметрах конфигурации собраний.

`Get-CsMeetingConfiguration`

Командлет **Get-CsMeetingConfiguration** возвращает информацию, подобную приведенной ниже:

Идентификация: Глобальная

PstnCallersBypassLobby: true

EnableAssignedConferenceType: true

DesignateAsPresenter: Company

AssignedConferenceTypeByDefault: true

AdmitAnonymousUsersByDefault: true

Кроме того, последний элемент в списке, **AdmitAnonymousUsersByDefault**, включает или отключает возможность анонимных пользователей принимать участие в собраниях.

При проверке параметров конфигурации собрания может оказаться полезным сравнить текущие параметры с эквивалентами по умолчанию. Вы можете просмотреть параметры конфигурации собрания по умолчанию, выполнив следующую команду:

`New-CsMeetingConfiguration -Identity "Global" -InMemory`

Предыдущая команда создает одновременный экземпляр глобальных параметров конфигурации собрания в памяти, экземпляр которого использует значение по умолчанию для каждого свойства. При выполнении команды не создаются фактические параметры конфигурации собраний. Тем не менее, на экране будут отображаться все значения свойств по умолчанию.

</div>

<div>

## <a name="check-edge-servers-and-their-settings"></a>Проверка серверов пограничного сервера и их параметров

Данные пограничного сервера можно получить с помощью Windows PowerShell. Эта команда возвращает сведения о всех пограничных серверах, настроенных для использования в вашей организации:

`Get-CsService -EdgeServer`

Возвращенные сведения включают все полные доменные значения и параметры порта для каждого пограничного сервера.

Identity: EdgeServer: dc.fabrikam.com

Регистратор: регистратор: LYNC-SE.fabrikam.com

AccessEdgeInternalSipPort: 5061

AccessEdgeExternalSipPort: 5061

AccessEdgeClientPort: 443

DataPsomServerPort: 8057

DataPsomClientPort: 444

MediaRelayAuthEdgePort: 5062

MediaRelayAuthInternalTurnTcpPort: 443

MediaRelayAuthExternalTurnTcpPort: 445

MediaRelayAuthInternalTurnUdpPort: 3478

MediaRelayAuthExternalTurnUdpPort: 3478

MediaCommunicationPortStart: 50000

MediaComunicationPortCount: 10000

AccessEdgeExternalFqdn: dc.fabrikam.com

DataEdgeExternalFqdn: dc.fabrikam.com

AVEdgeExternalFqdn :

InternalInterfaceFqdn :

ExternalMrasFqdn: dc.fabrikam.com

DependentServiceList: {регистратор: LYNC-SE.fabrikam.com,

ConferencingServer: LYNC-SE. fabrikam

com, MediationServer: LYNC-SE.

fabrikam.com}

ServiceId: fabrikam.com-EdgeServer-2

Идентификатор сайта: сайт:fabrikam. com

PoolFqdn: dc.fabrikam.com

Версия: 5

Role (роль): EdgeServer

<div>

## <a name="check-federation-settings"></a>Проверка параметров Федерации

Установите флажки для параметров Федерации, например, настроены ли они, и, если вы ответили "Да", полное доменное имя и порт. Интеграция включена и отключена с помощью глобальной коллекции параметров конфигурации пограничного доступа. Помимо прочего, это означает, что Федерация настроена на уровне "все" или "все". включена либо Федерация для всей Организации, либо Федерация отключена для всей Организации.

Параметры конфигурации Edge Access можно вернуть с помощью Windows PowerShell. Для этого выполните следующую команду Windows PowerShell:

`Get-CsAccessEdgeConfiguration`

В свою очередь она возвращает данные примерно так:

Идентификация: Глобальная

AllowAnonymousUsers: false

AllowFederatedUsers: false

AllowOutsideUsers: false

BeClearingHouse: false

EnablePartnerDiscovery: false

EnableArchivingDisclaimer: false

KeepCrlsUpToDateForPeers: true

MarkSourceVerifiableOnOutgoingMessages: true

OutgoingTlsCountForFederatedPartners: 4

RoutingMethod : UseDnsSrvRouting

Если для свойства **AllowFederatedUsers** задано значение "true", это означает, что для вашей организации включена Федерация. (Установка **AllowFederatedUsers** в true также означает, что в сценарии разделенного домена локальные пользователи смогут легко общаться с пользователями в облаке).

Чтобы получить полные доменные имена и параметры порта для пограничного сервера, ознакомьтесь с предыдущими задачами (пограничные серверы и их параметры).

Включение Федерации в глобальной области означает, что пользователи могут взаимодействовать с федеративными пользователями. Чтобы определить, могут ли какие либо пользователи самим взаимодействовать с федеративными пользователями, необходимо проверить политику доступа внешних пользователей, назначенную для этого пользователя.

Сведения о внешнем пользовательском доступе можно вернуть с помощью Windows PowerShell. Например, эта команда возвращает сведения о глобальной политике доступа внешних пользователей:

`Get-CsExternalAccessPolicy -Identity "Global"`

Эта команда возвращает сведения обо всех внешних политиках доступа пользователей.

`Get-CsExternalAccessPolicy`

Возвращенные сведения будут выглядеть примерно так:

Идентификация: ложь

Nописание

EnableFederationAccess: false

EnablePublicCloudAccess: false

EnablePublicCloudAccessAudioVideoAccess: false

EnableOutsideAccess: false

Если для **EnableFederationAccess** задано значение "true", пользователи, управляемые данной политикой, могут общаться с федеративными пользователями.

</div>

</div>

<div>

## <a name="check-archiving-settings"></a>Проверка параметров архивации

Проверка параметров архивирования для внутренних и Федеративных коммуникаций. Перед проверкой параметров внутренних и внешних архиваций убедитесь, что архивация включена.

Параметры конфигурации архивации можно проверить с помощью Windows PowerShell и командлета Get-CsArchivingConfiguration.

`Get-CsArchivingConfiguration -Identity "Global"`

Обратите внимание, что параметры архивации также можно настроить в области сайта. Чтобы получить сведения о всех параметрах архивации, используйте следующую команду:

`Get-CsArchivingConfiguration`

Командлет Get-CsArchivingConfiguration возвращает данные, подобные приведенным ниже.

Идентификация: Глобальная

EnableArchiving: false

EnablePurging: false

PurgeExportedArchivesOnly: false

BlockOnArchiveFailure: false

KeepArchivingDataForDays: 14

PurgeHourOfDay: 2

ArchiveDuplicateMessages: true

CachePurgingInterval: 24

Если свойство EnableArchiving имеет значение false, это означает, что сеансы связи не будут заархивированы. Если вы хотите архивировать сеансы мгновенных сообщений, используйте следующую команду, чтобы включить архивацию сеансов обмена мгновенными сообщениями.

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

Для архивации сеансов конференций и сеансов обмена мгновенными сообщениями используйте следующую команду:

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

Если вы хотите сравнить текущие параметры архивации с параметрами по умолчанию, выполните следующую команду Windows PowerShell:

`New-CsArchivingConfiguration -Identity "Global" -InMemory`

Эта команда создает одновременный экземпляр глобальных параметров конфигурации архивации в памяти. Это не является реальной коллекцией параметров, которые используются в Lync Server. Тем не менее, в нем отображаются значения по умолчанию для всех свойств конфигурации архивации.

Вы также можете использовать эту команду, чтобы вернуть полные доменные имена серверов архивации.

`Get-CsService -ArchivingServer`

После того как вы убедитесь, что архивация включена, вы можете просмотреть политики архивации, чтобы определить, архивируются ли внутренние и внешние сеансы связи.

Сведения о политике архивации можно получить с помощью командлета Get-CsArchivingPolicy. Например, эта команда возвращает сведения о глобальной политике архивации.

`Get-CsArchivingPolicy -Identity "Global"`

Поскольку политики архивации также можно настроить на сайте и на уровне пользователя, вам также может потребоваться использовать эту команду, которая возвращает сведения обо всех политиках архивации.

`Get-CsArchivingPolicy`

Сведения, полученные от Get-CsArchivingPolicy, будут выглядеть примерно так:

Идентификация: Глобальная

Nописание

ArchiveInternal: false

ArchiveExternal: false

Обратите внимание, что по умолчанию как внутренние, так и внешние архивации отключены в политике архивации.

</div>

<div>

## <a name="check-cdr-settings"></a>Проверка параметров CDR

Установите флажок запись с подробными сведениями о звонке (CDR) для одноранговой сети, Конференции и записи голосовых вызовов. Подробные сведения о параметрах CDR можно вернуть с помощью командлета **Get-CsCdrConfiguration** . Например, эта команда возвращает сведения о глобальной коллекции параметров конфигурации CDR:

`Get-CsCdrConfiguration -Identity "Global"`

Так как CDR также можно настроить на уровне сайта, вы также можете запустить эту команду, которая возвращает сведения обо всех параметрах конфигурации CDR:

`Get-CsCdrConfiguration`

Командлет Get-CsCdrConfiguration возвращает данные, подобные этим, для каждой коллекции параметров конфигурации CDR:

Идентификация: Глобальная

EnableCDR: true

EnablePurging: true

KeepCallDetailForDays: 60

KeepErrorReportForDays: 60

PurgeHourOfDay: 2

Аналогичные данные могут возвращаться для мониторинга QoE с помощью командлета Get-CsQoEConfiguration. Например, эта команда возвращает сведения о глобальной коллекции параметров конфигурации QoE:

`Get-QoEConfiguration -Identity "Global"`

Эти сведения будут выглядеть примерно так:

Идентификация: Глобальная

ExternalConsumerIssuedCertId :

EnablePurging: true

KeepQoEDataForDays: 60

PurgeHourOfDay: 1

EnableExternalConsumer: false

ExternalConsumerName :

ExternalConsumerURL :

EnableQoE: true

Если вы хотите сравнить текущие параметры CDR с параметрами CDR по умолчанию, можно просмотреть значения по умолчанию, выполнив следующую команду:

`New-CsCdrConfiguration -Identity "Global" -InMemory`

Также значения по умолчанию для мониторинга QoE можно получить с помощью следующей команды:

`New-CsQoEConfiguration -Identity "Global" -InMemory`

Вы также можете вернуть полные доменные имена серверов мониторинга, выполнив следующую команду:

`Get-CsService -MonitoringServer`

</div>

<div>

## <a name="check-voice-settings"></a>Проверка параметров голоса

Параметры голосовой связи, как правило, важны для администраторов в политиках голосовой связи и голосовых маршрутах: политики голосовой связи содержат параметры, определяющие возможности, доступные для отдельных пользователей (например, возможность пересылки или передачи), в то время как голосовые маршруты определяют, как звонки (и если) направляются по протоколу КТСОП.

Сведения о политике голосовой связи можно получить с помощью Windows PowerShell. Например, эта команда возвращает сведения о глобальной политике голосовой почты.

`Get-CsVoicePolicy -Identity "Global"`

Эта команда возвращает сведения обо всех голосовых политиках, настроенных для использования в Организации.

`Get-CsVoicePolicy`

Данные, возвращаемые командлетом Get-CsVoicePolicy, похожи на приведенные ниже.

Идентификация: Глобальная

PstnUsages : {}

Nописание

AllowSimulRing: true

AllowCallForwarding: true

AllowPSTNReRouting: true

Name (имя): DefaultPolicy

EnableDelegation: true

EnableTeamCall: true

EnableCallTransfer: true

EnableCallPark: false

EnableMaliciousCallTracing: false

EnableBWPolicyOverride: false

PreventPSTNTollBypass: false

Вы также можете создавать запросы, которые возвращают подмножество политик голосовой связи. Например, эта команда возвращает все политики голосовой связи, которые разрешают переадресацию звонков.

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $True}`

Эта команда возвращает все политики голосовой связи, не допускающие переадресацию звонков.

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $False}`

В Windows PowerShell используйте командлет Get-CsVoiceRouting, чтобы получить сведения о голосовых маршрутах.

`Get-CsVoiceRoute`

Эта команда возвращает такие сведения, как, например, для всех голосовых маршрутов.

Identity: LocalRoute

Priority (приоритет): 0

Nописание

NumberPattern: ^ ( \\ + 1 \[ 0-9 \] {10} ) $

PstnUsages : {}

PstnGatewayList : {}

Name (имя): LocalRoute

SuppressCallerId :

AlternateCallerId :

Lync Server позволяет создавать маршруты голосовой связи, для которых не используется PSTN, и не указывать шлюз PSTN. Однако вы не можете перенаправлять звонки через голосовой маршрут, для которого не настроены эти два значения свойств. По этой причине вам может понадобиться периодически запускать эту команду, которая возвращает идентификационные данные любого маршрута голосовой связи, для которого не используется PSTN.

`Get-CsVoiceRoute | Where-Object {$_.PstnUsages -eq $Null} | Select-Object Identity`

Аналогичным образом эта команда возвращает идентификационные данные любого маршрута голосовой связи, для которого не настроен шлюз PSTN.

`Get-CsVoiceRoute | Where-Object {$_.PstnGatewayList -eq $Null}} | Select-Object Identity`

</div>

<div>

## <a name="check-conferencing-attendant-settings"></a>Проверка параметров помощника по конференциям

Проверьте параметры помощника по конференциям для конференц-связи с телефонным подключением PSTN. Параметры помощника по конференциям можно получить только с помощью командлета **Get-CsDialInConferencingConfiguration** . Эти параметры недоступны на панели управления Lync Server. Чтобы просмотреть параметры помощника по конференциям, используйте команду Windows PowerShell, как показано ниже, и возвращающая глобальную коллекцию параметров конференц-связи.

`Get-CsDialInConferencingConfiguration -Identity "Global"`

Обратите внимание, что параметры помощника по конференциям также можно настроить в области сайта. Чтобы получить сведения о всех параметрах помощника по конференциям, используйте следующую команду:

`Get-CsDialInConferencingConfiguration`

Командлет Get-CsDialInConferencingConfiguration возвращает данные, подобные приведенным ниже.

Идентификация: Глобальная

EntryExitAnnouncementsType : UseNames

EnableNameRecording: true

EntryExitAnnouncementsEnabledByDefault: false

Если для EntryExitAnnouncementsEnabledByDefault задано значение false, объявления конференций отключены. Чтобы включить объявления входа и выхода, выполните команду Windows PowerShell, подобную следующей:

`Set-CsDialInConferencingConfiguration -Identity "Global" -EntryExitAnnouncementsEnabledByDefault $True`

</div>

<div>

## <a name="see-also"></a>См. также


[Get-CsSipDomain](https://docs.microsoft.com/powershell/module/skype/Get-CsSipDomain)  
[Get-CsMeetingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration)  
[Get-CsService](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[Get-CsAccessEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAccessEdgeConfiguration)  
[Get-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[Get-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsArchivingConfiguration)  
[Get-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration)  
[Get-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsQoEConfiguration)  
[Get-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[Get-CsVoiceRoute](https://docs.microsoft.com/powershell/module/skype/Get-CsVoiceRoute)  
[Get-CsDialInConferencingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

