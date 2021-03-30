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
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="b6482-103">Настройка федерации в Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6482-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6482-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6482-104">

<span> </span></span></span>

<span data-ttu-id="b6482-105">_**Тема последнего изменения:** 27.03.2014_</span><span class="sxs-lookup"><span data-stu-id="b6482-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="b6482-106">Если вы уже развернули edge server или серверы, вам будут сразу же добавлены федераированные сценарии.</span><span class="sxs-lookup"><span data-stu-id="b6482-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="b6482-107">Если вы не настроили edge Servers, необходимо сначала сделать это.</span><span class="sxs-lookup"><span data-stu-id="b6482-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="b6482-108">Дополнительные сведения см. в документации по планированию и развертывании доступа внешних пользователей к [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) в документации по развертыванию. [](lync-server-2013-planning-for-external-user-access.md)</span><span class="sxs-lookup"><span data-stu-id="b6482-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b6482-109">Если вы собираетесь настроить любое сочетание федерации XMPP, федерации Lync или подключения к общедоступным службам обмена мгновенными сообщениями, их можно развернуть одновременно или по одному.</span><span class="sxs-lookup"><span data-stu-id="b6482-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="b6482-110">Если параметры настроены с помощью построитель топологии и оболочки управления Lync Server, запустите мастер развертывания на edge-сервере после настройки параметров одного, двух или трех типов федерации, можно уменьшить количество необходимых действий.</span><span class="sxs-lookup"><span data-stu-id="b6482-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="b6482-111">Настройка федерации Lync в конструкторе топологии и мастере развертывания</span><span class="sxs-lookup"><span data-stu-id="b6482-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="b6482-112">На переднем сервере откройте построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="b6482-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="b6482-113">Развернув пул Edge, щелкните его правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="b6482-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="b6482-114">Выберите "Изменить свойства".</span><span class="sxs-lookup"><span data-stu-id="b6482-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="b6482-115">В оке "Изменение свойств в области "Общие" выберите "Включить федерацию для этого границы (порт 5061)".</span><span class="sxs-lookup"><span data-stu-id="b6482-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="b6482-116">Нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="b6482-116">Click OK.</span></span>

3.  <span data-ttu-id="b6482-117">Щелкните "Действие", выберите "Топология" и "Опубликовать".</span><span class="sxs-lookup"><span data-stu-id="b6482-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="b6482-118">Когда будет предложено опубликовать топологию, нажмите кнопку "Далее".</span><span class="sxs-lookup"><span data-stu-id="b6482-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="b6482-119">По завершению публикации нажмите кнопку "Готово".</span><span class="sxs-lookup"><span data-stu-id="b6482-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="b6482-120">На edge server откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b6482-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="b6482-121">Нажмите кнопку "Установить" или "Обновить систему Lync Server", а затем выберите "Настройка" или "Удаление компонентов сервера Lync Server".</span><span class="sxs-lookup"><span data-stu-id="b6482-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="b6482-122">Нажмите кнопку "Выполнить еще раз".</span><span class="sxs-lookup"><span data-stu-id="b6482-122">Click Run Again.</span></span>

5.  <span data-ttu-id="b6482-123">На этапе настройки компоненты Lync Server нажмите кнопку "Далее".</span><span class="sxs-lookup"><span data-stu-id="b6482-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="b6482-124">На экране сводки будут выводится действия по мере их выполнения.</span><span class="sxs-lookup"><span data-stu-id="b6482-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="b6482-125">После развертывания нажмите кнопку "Просмотреть журнал", чтобы просмотреть доступные файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="b6482-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="b6482-126">Нажмите кнопку "Готово", чтобы завершить развертывание.</span><span class="sxs-lookup"><span data-stu-id="b6482-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b6482-127">Вы можете выбрать этот параметр, но только один edge pool или Edge Server в вашей организации может быть опубликован за ее границу.</span><span class="sxs-lookup"><span data-stu-id="b6482-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="b6482-128">Все возможности доступа федераированных пользователей, включая пользователей общедоступных служб обмена мгновенными сообщениями, проходят через один edge pool или один edge Server.</span><span class="sxs-lookup"><span data-stu-id="b6482-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="b6482-129">Например, если в вашем развертывании есть пул Edge или один edge Server, развернутый в Нью-Йорке, и один из них развернут в Лондоне, и вы включили поддержку федерации для пула в Нью-Йорке или одного edge Server, сигнальный трафик федераированных пользователей будет проходить через пул в Нью-Йорке или один edge Server.</span><span class="sxs-lookup"><span data-stu-id="b6482-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="b6482-130">Это справедливо даже для пользователей в Лондоне, хотя при вызове внутренним пользователем лондонского филиала федеративного пользователя в Лондоне трафик аудио- и видеосвязи будет идти через лондонский пограничный пул или сервер.</span><span class="sxs-lookup"><span data-stu-id="b6482-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="b6482-131">Настройка федерации с партнерами</span><span class="sxs-lookup"><span data-stu-id="b6482-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="b6482-132">Чтобы настроить успешную федерацию с другой службой Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 или Office Communicator 2007, выберите тип федерации из таблицы ниже и определите записи DNS SRV, DNS-сервер (A или AAAA для IPv6) и настройте политики, применимые к типу федерации:</span><span class="sxs-lookup"><span data-stu-id="b6482-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="b6482-133">Тип федерации</span><span class="sxs-lookup"><span data-stu-id="b6482-133">Federation type</span></span></th>
    <th><span data-ttu-id="b6482-134">DNS Records</span><span class="sxs-lookup"><span data-stu-id="b6482-134">DNS Records</span></span></th>
    <th><span data-ttu-id="b6482-135">Определение политики</span><span class="sxs-lookup"><span data-stu-id="b6482-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="b6482-136">Notes</span><span class="sxs-lookup"><span data-stu-id="b6482-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="b6482-137">Discovered Partner Domain</span><span class="sxs-lookup"><span data-stu-id="b6482-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="b6482-138">Настройте запись SRV формата _sipfederationtls._tcp. &lt; внешнее доменное имя, где значением порта для &gt; записи SRV является TCP 5061, а хост, предлагающий эту службу, определен как <strong></strong> sip.</span><span class="sxs-lookup"><span data-stu-id="b6482-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="b6482-139">&lt;внешнее доменное &gt; имя — FQDN службы Access Edge.</span><span class="sxs-lookup"><span data-stu-id="b6482-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="b6482-140">Дополнительные сведения о создании записи SRV см. в сведениях о настройке DNS для поддержки edge в <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="b6482-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="b6482-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="b6482-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Включение или отключение обнаружения федеративных партнеров в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="b6482-143">В предыдущих версиях такой тип федерации назывался <strong>Open Enhanced Federation.</strong></span><span class="sxs-lookup"><span data-stu-id="b6482-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="b6482-144">Создание записи SRV является обязательной для этого типа федерации и позволяет другим партнерам обнаружить вашу федерацию.</span><span class="sxs-lookup"><span data-stu-id="b6482-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="b6482-145">Разрешенный домен партнера</span><span class="sxs-lookup"><span data-stu-id="b6482-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="b6482-146">Настройте запись SRV формата _sipfederationtls._tcp. &lt; внешнее доменное имя, где значением порта для &gt; записи SRV является TCP 5061, а хост, предлагающий эту службу, определен как <strong></strong> sip.</span><span class="sxs-lookup"><span data-stu-id="b6482-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="b6482-147">&lt;внешнее доменное &gt; имя — FQDN службы Access Edge.</span><span class="sxs-lookup"><span data-stu-id="b6482-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="b6482-148">Дополнительные сведения о создании записи SRV см. в сведениях о настройке DNS для поддержки edge в <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="b6482-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="b6482-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="b6482-150">В предыдущих версиях такой тип федерации назывался <strong>расширенной федерацией.</strong></span><span class="sxs-lookup"><span data-stu-id="b6482-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="b6482-151">Запись SRV необязательна для этого типа федерации и позволяет другим партнерам обнаружить вашу федерацию.</span><span class="sxs-lookup"><span data-stu-id="b6482-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="b6482-152">Конечно же, это будет <strong>открытая</strong>расширенная федерация или <strong>обнаруженный домен партнера.</strong></span><span class="sxs-lookup"><span data-stu-id="b6482-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="b6482-153">Разрешенный сервер партнера</span><span class="sxs-lookup"><span data-stu-id="b6482-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="b6482-154">Настройка доменного имени SIP и FQDN сервера edge server партнера в качестве партнера федерации в политиках</span><span class="sxs-lookup"><span data-stu-id="b6482-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="b6482-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="b6482-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Настройка поддержки для разрешенных внешних доменов в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="b6482-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Настройка поддержки заблокированных внешних доменов в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="b6482-158">Этот тип федерации — это определение отношения "один к одному" и не позволяет обнаруживать других партнеров федерации.</span><span class="sxs-lookup"><span data-stu-id="b6482-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="b6482-159">Все партнеры федерации настроены явным образом.</span><span class="sxs-lookup"><span data-stu-id="b6482-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="b6482-160">В предыдущих версиях эта под названием "Прямая <strong>федерация"</strong></span><span class="sxs-lookup"><span data-stu-id="b6482-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="b6482-161">Поставщик услуг размещения и общедоступный поставщик услуг мгновенных услуг</span><span class="sxs-lookup"><span data-stu-id="b6482-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="b6482-162">Для этого типа федерации не определены какие-либо особые требования к DNS</span><span class="sxs-lookup"><span data-stu-id="b6482-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="b6482-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Включение или отключение федерации и подключение для общедоступного обмена мгновенными сообщениями в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="b6482-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Создание или изменение общедоступных федеративных поставщиков SIP в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="b6482-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Создание или изменение размещенных федеративных поставщиков SIP в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b6482-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="b6482-166">Этот тип федерации определяет службы и поставщики услуг размещения, которые вы хотите настроить для пользователей.</span><span class="sxs-lookup"><span data-stu-id="b6482-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="b6482-167">Обычно используется конфигурация для общедоступных поставщиков услуг мгновенных Windows Live Messenger, Yahoo!</span><span class="sxs-lookup"><span data-stu-id="b6482-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="b6482-168">и AOL, а также поставщиков услуг размещения, таких как Lync Online и Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b6482-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="b6482-169">С 1 сентября 2012 г. лицензия пользователя на подключение к общедоступным мгновенным службам Microsoft Lync (PIC USL) больше не доступна для приобретения для новых или продленных соглашений.</span><span class="sxs-lookup"><span data-stu-id="b6482-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="b6482-170">Клиенты с активными лицензиями смогут по-прежнему федерироваться с Yahoo!</span><span class="sxs-lookup"><span data-stu-id="b6482-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="b6482-171">Messenger до даты отключения службы.</span><span class="sxs-lookup"><span data-stu-id="b6482-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="b6482-172">Окончание жизненного срока для AOL и Yahoo! в июне 2014 г.</span><span class="sxs-lookup"><span data-stu-id="b6482-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="b6482-173">была озвучина.</span><span class="sxs-lookup"><span data-stu-id="b6482-173">has been announced.</span></span> <span data-ttu-id="b6482-174">Подробные сведения см. в поддержке подключения к общедоступным средствам обмена мгновенными сообщениями <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в Lync Server 2013.</A></span><span class="sxs-lookup"><span data-stu-id="b6482-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="b6482-175">PIC USL — это лицензия на месячную подписку, которая требуется для Lync Server или Office Communications Server для федерации с Yahoo!</span><span class="sxs-lookup"><span data-stu-id="b6482-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="b6482-176">Messenger.</span><span class="sxs-lookup"><span data-stu-id="b6482-176">Messenger.</span></span> <span data-ttu-id="b6482-177">Возможность корпорации Майкрософт предоставлять эту службу была рассчитана на поддержку Yahoo! — соглашения, на основе которого она будет огорубиться.</span><span class="sxs-lookup"><span data-stu-id="b6482-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="b6482-178">Lync — это мощный инструмент для связи между организациями и отдельными людьми по всему миру как никогда.</span><span class="sxs-lookup"><span data-stu-id="b6482-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="b6482-179">Для федерации Windows Live Messenger не требуются дополнительные лицензии пользователя и устройства после cal Lync Standard.</span><span class="sxs-lookup"><span data-stu-id="b6482-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="b6482-180">Федерация Skype будет добавлена в этот список, что позволит пользователям Lync звонить и звонить сотням миллионов людей.</span><span class="sxs-lookup"><span data-stu-id="b6482-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="b6482-181">Определение и настройка необходимых записей DNS (A или AAAA для IPv6) и SRV DNS</span><span class="sxs-lookup"><span data-stu-id="b6482-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="b6482-182">Определите и настройте любые политики с помощью панели управления Lync Server или с помощью диспетчерской оболочки Lync Server и соответствующих cmdlets.</span><span class="sxs-lookup"><span data-stu-id="b6482-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="b6482-183">Подробные сведения о оболочке управления Lync Server см. в сведениях о федерации и внешнем доступе [в Lync Server 2013.](https://docs.microsoft.com/powershell/module/skype/)</span><span class="sxs-lookup"><span data-stu-id="b6482-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b6482-184">В Lync Room System (LRS) нет кнопки присоединиться к собраниям, отправленным организаторами в федераированных партнерах Lync.</span><span class="sxs-lookup"><span data-stu-id="b6482-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="b6482-185">Чтобы ссылка на собрание была отображаться в LRS, отправляя организация должна включить TNEF с помощью следующего cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b6482-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="b6482-186">Обратите внимание, что это не особенности LRS.</span><span class="sxs-lookup"><span data-stu-id="b6482-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="b6482-187">В этом случае связи в Outlook и Lync также не будут показываться, так как свойства MAPI не переноситься, но в случае с Outlook пользователь может открыть приглашение на собрание и щелкнуть URL-адрес собрания.</span><span class="sxs-lookup"><span data-stu-id="b6482-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="b6482-188">Если для TNEFEnabled заказано истинное в Exchange 2013, свойства MAPI не отключатся, включая OnlineMeetingExternalLink, и в напоминаниях будет показана кнопка "Присоединиться".</span><span class="sxs-lookup"><span data-stu-id="b6482-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b6482-189">См. также</span><span class="sxs-lookup"><span data-stu-id="b6482-189">See Also</span></span>


[<span data-ttu-id="b6482-190">Планирование федерации SIP, XMPP и обмена общедоступными мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6482-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="b6482-191">Управление федерацией и внешним доступом к Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6482-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="b6482-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6482-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

