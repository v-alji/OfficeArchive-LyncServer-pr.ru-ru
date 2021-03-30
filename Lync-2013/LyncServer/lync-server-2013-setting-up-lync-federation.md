---
title: 'Lync Server 2013: настройка федерации в Lync'
description: 'Lync Server 2013: настройка федерации Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399811"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a>Настройка федерации в Lync в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 27.03.2014_

Если вы уже развернули edge server или серверы, вам будут сразу же добавлены федераированные сценарии. Если вы не настроили edge Servers, необходимо сначала сделать это. Дополнительные сведения см. в документации по планированию и развертывании доступа внешних пользователей к [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) в документации по развертыванию. [](lync-server-2013-planning-for-external-user-access.md)

<div>


> [!NOTE]  
> Если вы собираетесь настроить любое сочетание федерации XMPP, федерации Lync или подключения к общедоступным службам обмена мгновенными сообщениями, их можно развернуть одновременно или по одному. Если параметры настроены с помощью построитель топологии и оболочки управления Lync Server, запустите мастер развертывания на edge-сервере после настройки параметров одного, двух или трех типов федерации, можно уменьшить количество необходимых действий.



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>Настройка федерации Lync в конструкторе топологии и мастере развертывания

1.  На переднем сервере откройте построитель топологии. Развернув пул Edge, щелкните его правой кнопкой мыши. Выберите "Изменить свойства".

2.  В оке "Изменение свойств в области "Общие" выберите "Включить федерацию для этого границы (порт 5061)". Нажмите кнопку ОК.

3.  Щелкните "Действие", выберите "Топология" и "Опубликовать". Когда будет предложено опубликовать топологию, нажмите кнопку "Далее". По завершению публикации нажмите кнопку "Готово".

4.  На edge server откройте мастер развертывания Lync Server. Нажмите кнопку "Установить" или "Обновить систему Lync Server", а затем выберите "Настройка" или "Удаление компонентов сервера Lync Server". Нажмите кнопку "Выполнить еще раз".

5.  На этапе настройки компоненты Lync Server нажмите кнопку "Далее". На экране сводки будут выводится действия по мере их выполнения. После развертывания нажмите кнопку "Просмотреть журнал", чтобы просмотреть доступные файлы журналов. Нажмите кнопку "Готово", чтобы завершить развертывание.
    
    <div>
    

    > [!IMPORTANT]  
    > Вы можете выбрать этот параметр, но только один edge pool или Edge Server в вашей организации может быть опубликован за ее границу. Все возможности доступа федераированных пользователей, включая пользователей общедоступных служб обмена мгновенными сообщениями, проходят через один edge pool или один edge Server. Например, если в вашем развертывании есть пул Edge или один edge Server, развернутый в Нью-Йорке, и один из них развернут в Лондоне, и вы включили поддержку федерации для пула в Нью-Йорке или одного edge Server, сигнальный трафик федераированных пользователей будет проходить через пул в Нью-Йорке или один edge Server. Это справедливо даже для пользователей в Лондоне, хотя при вызове внутренним пользователем лондонского филиала федеративного пользователя в Лондоне трафик аудио- и видеосвязи будет идти через лондонский пограничный пул или сервер.

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>Настройка федерации с партнерами

1.  Чтобы настроить успешную федерацию с другой службой Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 или Office Communicator 2007, выберите тип федерации из таблицы ниже и определите записи DNS SRV, DNS-сервер (A или AAAA для IPv6) и настройте политики, применимые к типу федерации:
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Тип федерации</th>
    <th>DNS Records</th>
    <th>Определение политики</th>
    <th>Notes</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Discovered Partner Domain</p></td>
    <td><p>Настройте запись SRV формата _sipfederationtls._tcp. &lt; внешнее доменное имя, где значением порта для &gt; записи SRV является TCP 5061, а хост, предлагающий эту службу, определен как <strong></strong> sip. &lt;внешнее доменное &gt; имя — FQDN службы Access Edge. Дополнительные сведения о создании записи SRV см. в сведениях о настройке DNS для поддержки edge в <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013.</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Включение или отключение обнаружения федеративных партнеров в Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>В предыдущих версиях такой тип федерации назывался <strong>Open Enhanced Federation.</strong> Создание записи SRV является обязательной для этого типа федерации и позволяет другим партнерам обнаружить вашу федерацию.</p></td>
    </tr>
    <tr class="even">
    <td><p>Разрешенный домен партнера</p></td>
    <td><p>Настройте запись SRV формата _sipfederationtls._tcp. &lt; внешнее доменное имя, где значением порта для &gt; записи SRV является TCP 5061, а хост, предлагающий эту службу, определен как <strong></strong> sip. &lt;внешнее доменное &gt; имя — FQDN службы Access Edge. Дополнительные сведения о создании записи SRV см. в сведениях о настройке DNS для поддержки edge в <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013.</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>В предыдущих версиях такой тип федерации назывался <strong>расширенной федерацией.</strong> Запись SRV необязательна для этого типа федерации и позволяет другим партнерам обнаружить вашу федерацию. Конечно же, это будет <strong>открытая</strong>расширенная федерация или <strong>обнаруженный домен партнера.</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>Разрешенный сервер партнера</p></td>
    <td><p>Настройка доменного имени SIP и FQDN сервера edge server партнера в качестве партнера федерации в политиках</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Настройка поддержки для разрешенных внешних доменов в Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Настройка поддержки заблокированных внешних доменов в Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Этот тип федерации — это определение отношения "один к одному" и не позволяет обнаруживать других партнеров федерации. Все партнеры федерации настроены явным образом. В предыдущих версиях эта под названием "Прямая <strong>федерация"</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>Поставщик услуг размещения и общедоступный поставщик услуг мгновенных услуг</p></td>
    <td><p>Для этого типа федерации не определены какие-либо особые требования к DNS</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Создание или изменение общедоступных федеративных поставщиков SIP в Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Создание или изменение размещенных федеративных поставщиков SIP в Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Этот тип федерации определяет службы и поставщики услуг размещения, которые вы хотите настроить для пользователей. Обычно используется конфигурация для общедоступных поставщиков услуг мгновенных Windows Live Messenger, Yahoo! и AOL, а также поставщиков услуг размещения, таких как Lync Online и Microsoft 365</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>С 1 сентября 2012 г. лицензия пользователя на подключение к общедоступным мгновенным службам Microsoft Lync (PIC USL) больше не доступна для приобретения для новых или продленных соглашений. Клиенты с активными лицензиями смогут по-прежнему федерироваться с Yahoo! Messenger до даты отключения службы. Окончание жизненного срока для AOL и Yahoo! в июне 2014 г. была озвучина. Подробные сведения см. в поддержке подключения к общедоступным средствам обмена мгновенными сообщениями <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в Lync Server 2013.</A></P>
    > <LI>
    > <P>PIC USL — это лицензия на месячную подписку, которая требуется для Lync Server или Office Communications Server для федерации с Yahoo! Messenger. Возможность корпорации Майкрософт предоставлять эту службу была рассчитана на поддержку Yahoo! — соглашения, на основе которого она будет огорубиться.</P>
    > <LI>
    > <P>Lync — это мощный инструмент для связи между организациями и отдельными людьми по всему миру как никогда. Для федерации Windows Live Messenger не требуются дополнительные лицензии пользователя и устройства после cal Lync Standard. Федерация Skype будет добавлена в этот список, что позволит пользователям Lync звонить и звонить сотням миллионов людей.</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  Определение и настройка необходимых записей DNS (A или AAAA для IPv6) и SRV DNS

3.  Определите и настройте любые политики с помощью панели управления Lync Server или с помощью диспетчерской оболочки Lync Server и соответствующих cmdlets. Подробные сведения о оболочке управления Lync Server см. в сведениях о федерации и внешнем доступе [в Lync Server 2013.](https://docs.microsoft.com/powershell/module/skype/)
    
    <div>
    

    > [!NOTE]  
    > В Lync Room System (LRS) нет кнопки присоединиться к собраниям, отправленным организаторами в федераированных партнерах Lync. Чтобы ссылка на собрание была отображаться в LRS, отправляя организация должна включить TNEF с помощью следующего cmdlet:<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>Обратите внимание, что это не особенности LRS. В этом случае связи в Outlook и Lync также не будут показываться, так как свойства MAPI не переноситься, но в случае с Outlook пользователь может открыть приглашение на собрание и щелкнуть URL-адрес собрания. Если для TNEFEnabled заказано истинное в Exchange 2013, свойства MAPI не отключатся, включая OnlineMeetingExternalLink, и в напоминаниях будет показана кнопка "Присоединиться".

    
    </div>

</div>

<div>

## <a name="see-also"></a>См. также


[Планирование федерации SIP, XMPP и обмена общедоступными мгновенными сообщениями в Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[Управление федерацией и внешним доступом к Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

