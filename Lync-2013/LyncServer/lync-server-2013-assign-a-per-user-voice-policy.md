---
title: 'Lync Server 2013: назначение политики голосовой связи для отдельных пользователей'
description: 'Lync Server 2013: назначение политики голосовой связи для каждого пользователя.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user voice policy
ms:assetid: 9ee47ee7-1030-43b8-a4dc-bf685ea24659
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688155(v=OCS.15)
ms:contentKeyID: 49733758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7ea0b171e10302b4c466187c54324cc2548e821
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443164"
---
# <a name="assign-a-per-user-voice-policy-in-lync-server-2013"></a>Назначение политики голосовой связи для пользователя в Lync Server 2013

 


Глобальные и высокоуровневые политики на уровне сайта автоматически назначаются всем учетным записям пользователей Lync Server 2013, которые включены для корпоративной голосовой связи. Вы также можете назначать политики голосовой связи определенным пользователям с помощью панели управления Lync Server 2013 или командной консоли Lync Server 2013. С помощью процедур, описанных в этом разделе, явным образом назначьте политики для пользователей Lync Server.

## <a name="to-assign-a-user-specific-voice-policy-using-the-lync-server-control-panel"></a>Назначение особой политики голосовой связи с помощью панели управления Lync Server

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  В левой панели навигации нажмите **Пользователи** и выполните поиск учетной записи, которую вы хотите настроить.

4.  В таблице с результатами поиска выберите нужную учетную запись, нажмите кнопку **Изменить** и выберите пункт **Показать сведения**.

5.  В диалоговом окне **изменение пользователя Lync Server** в разделе **политика голосовой связи** выберите политику пользователей, которую вы хотите применить.
    

    > [!NOTE]  
    > Параметры <STRONG> &lt; автоматической &gt; </STRONG> настройки применяются к параметрам сервера или глобальной политики, используемым по умолчанию.



## <a name="assign-per-user-voice-policies"></a>Назначение политик голосовой связи для пользователей

Вы можете назначать политики голосовой связи для пользователей с помощью Windows PowerShell и командлета **Grant-CsVoicePolicy** . Этот командлет можно выполнить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell. Чтобы узнать об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server, прочитайте запись блога Windows PowerShell в Lync Server: Краткое руководство: [Управление Microsoft Lync server 2010 с помощью удаленной оболочки PowerShell](https://go.microsoft.com/fwlink/p/?linkId=255876).

### <a name="assign-a-per-user-voice-policy-to-a-single-user"></a>Назначение пользователю политики голосовой связи для отдельного пользователя

  - Следующая команда назначает пользовательскую политику голосовой связи "на пользователя", RedmondVoicePolicy с пользователем Кен Myer.
    
        Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "RedmondVoicePolicy"

## <a name="assign-a-per-user-voice-policy-to-multiple-users"></a>Назначение политики голосовой почты для каждого пользователя нескольким пользователям

  - Эта команда назначает политику голосовой связи для пользователя FinanceVoicePolicy всем пользователям, у которых есть учетные записи в подразделении "Финансы" в Active Directory. Дополнительные сведения о параметре OU, используемом в этой команде, можно найти в документации по командлету [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .
    
        Get-CsUser -OU "ou=Finance,ou=North America,dc=litwareinc,dc=com" | Grant-CsVoicePolicy -PolicyName "FinanceVoicePolicy"

## <a name="unassign-a-per-user-voice-policy"></a>Отмена назначения голосовой политики для пользователя

  - Следующая команда отменяет назначение любой политики голосовой почты для каждого пользователя, ранее назначенной для Кен Myer. После отмены назначения для Кена Майера будет автоматически действовать глобальная политика или локальная политика сайта, если такая существует. Политика сайта имеет приоритет над глобальной политикой.
    
        Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName $Null

Дополнительные сведения можно найти в разделе справки о командлете [Grant-CsVoicePolicy](https://technet.microsoft.com/library/gg398828\(v=ocs.15\)) .

## <a name="see-also"></a>См. также


[Отключение пользователя для корпоративного голосовой связи в Lync Server 2013](lync-server-2013-disable-a-user-for-enterprise-voice.md)  


[командная консоль Lync Server 2013](lync-server-2013-lync-server-management-shell.md)

