---
title: 'Lync Server 2013: проведение подготовки домена'
description: 'Lync Server 2013: выполнение подготовки домена.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running domain preparation
ms:assetid: 95dab800-1f2c-4506-b36c-99986643b149
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398761(v=OCS.15)
ms:contentKeyID: 48184847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f2c4ebe94d07ed2d1fd9be013cd8e88204312f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442259"
---
# <a name="running-domain-preparation-for-lync-server-2013"></a>Проведение подготовки домена для Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-04-16_

Для подготовки доменов можно использовать командлеты командной консоли Setup или Lync Server Management Shell. Командлет, подготавливающий домен, — **Enable-CsAdDomain**.

Подготовка домена — это заключительный этап подготовки доменных служб Active Directory для Lync Server 2013.

<div>

## <a name="to-use-setup-to-prepare-domains"></a>Использование программы установки для подготовки доменов

1.  Войдите на любой сервер домена, который является членом группы "Администраторы домена".

2.  В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания Lync Server.

3.  Нажмите **Подготовить Active Directory** и подождите, пока будет определено состояние развертывания.

4.  Когда появится окно **Шаг 5. Подготовка текущего домена**, нажмите кнопку **Запустить**.

5.  На странице **Подготовка домена** нажмите кнопку **Далее**.

6.  На странице **выполнения команд** подождите, пока не появится сообщение **Состояние задачи: Завершено**, а затем нажмите **Просмотреть журнал**.

7.  В столбце **Action (действие** ) разверните **доменную версию домена**, найдите **\<Success\>** результаты выполнения в конце каждой задачи, чтобы убедиться в том, что подготовка домена успешно завершена, закройте журнал и нажмите кнопку **Готово**.

8.  Дождитесь завершения репликации Active Directory или принудительно выполните репликацию на все контроллеры домена, указанные в оснастке "сайты и службы" Active Directory для корневого контроллера домена леса.

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-domain"></a>Использование командлетов для подготовки домена

1.  Войдите на любой сервер домена, который является членом группы "Администраторы домена".

2.  Установите основные компоненты Lync Server, как описано ниже.
    
    1.  В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания Lync Server.
    
    2.  Если вам будет предложено установить распространяемый компонент Microsoft Visual C++, нажмите кнопку **Да**.
    
    3.  Диалоговое окно установки Lync Server 2013 предлагает указать расположение для установки файлов Lync Server. Выберите расположение по умолчанию или **перейдите** в нужное место, а затем нажмите кнопку **установить**.
    
    4.  На странице Лицензионное соглашение установите флажок **я принимаю условия лицензионного соглашения**, а затем нажмите кнопку **ОК**. Установщик установит основные компоненты Lync Server 2013.

3.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

4.  Выполните следующую команду:
    
        Enable-CsAdDomain [-Domain <DomainFQDN>] 
    
    Например:
    
        Enable-CsAdDomain -Domain domain1.contoso.net 
    
    Если параметр Domain не указан, по умолчанию используется локальный домен.

5.  Убедитесь, что подготовка домена выполнена успешно. Выполните следующую команду:
    
        Get-CsAdDomain [-Domain <Domain FQDN>] [-DomainController <Domain controller FQDN>] [-GlobalCatalog <Global catalog server FQDN>] [-GlobalSettingsDomainController <Domain controller FQDN where global settings are stored>] 
    
    Например:
    
        Get-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.com
    
    <div>
    

    > [!NOTE]  
    > Параметр GlobalSettingsDomainController позволяет указать, где хранятся глобальные параметры. Если параметры хранятся в системном контейнере (обычно при развертывании обновлений без глобальных параметров, перенесенных в контейнер), вы определяете контроллер домена в корне леса Active Directory. Если глобальные параметры хранятся в контейнере Configuration (это обычная ситуация для новых развертываний или обновленных развертываний, в которых параметры перенесены в контейнер Configuration), определите любой контроллер домена в лесу. Если этот параметр не указан, командлет предполагает, что параметры хранятся в контейнере конфигурации и ссылаются на любой контроллер домена в доменных &nbsp; службах Active Directory.

    
    </div>
    
    Если параметр **domain** не указан, по умолчанию используется локальный домен.
    
    Этот командлет возвращает значение **\_ DOMAINSETTINGS \_ состояния \_ "LC** ", если подготовка домена выполнена успешно.

</div>

<div>

## <a name="see-also"></a>См. также


[Использование командлетов для отмены подготовки доменов для Lync Server 2013](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)  


[Подготовка доменов для Lync Server 2013](lync-server-2013-preparing-domains.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

