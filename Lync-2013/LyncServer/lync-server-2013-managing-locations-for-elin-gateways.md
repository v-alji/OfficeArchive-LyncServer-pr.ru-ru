---
title: 'Lync Server 2013: Управление расположением для шлюзов ELIN'
description: 'Lync Server 2013: Управление расположением для шлюзов ELIN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing locations for ELIN gateways
ms:assetid: ced79c13-4e7e-4034-95cd-6fc913f4f222
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205288(v=OCS.15)
ms:contentKeyID: 48185496
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 94fe7797c0f25adb219512cef4a6c0fb7d84b48d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437401"
---
# <a name="managing-locations-for-elin-gateways-in-lync-server-2013"></a><span data-ttu-id="b9ea4-103">Управление расположением для шлюзов ELIN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9ea4-103">Managing locations for ELIN gateways in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9ea4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9ea4-104">

<span> </span></span></span>

<span data-ttu-id="b9ea4-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b9ea4-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b9ea4-106">Чтобы сервер Lync Server автоматически предоставил вам расположение для клиентов в сети, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-106">To have Lync Server automatically provide locations for clients within a network, you need to perform the following tasks:</span></span>

  - <span data-ttu-id="b9ea4-107">Заполните базу данных службы сведений о расположении с помощью сети Wiremap и включите в поле CompanyName идентификационные номера расположения для экстренного реагирования (ELINs).</span><span class="sxs-lookup"><span data-stu-id="b9ea4-107">Populate the Location Information service database with a network wiremap, and include the Emergency Location Identification Numbers (ELINs) in the CompanyName field.</span></span>

  - <span data-ttu-id="b9ea4-108">Опубликовать расположения, чтобы они были доступны клиентам в сети.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-108">Publish the locations so that they are available for clients in your network.</span></span>

  - <span data-ttu-id="b9ea4-109">Отправить номера ELIN в базу данных автоматического определения расположения (ALI) поставщика PSTN.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-109">Upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span>

<span data-ttu-id="b9ea4-110">Подробнее о том, как выполнять эти задачи, можно найти [в статье Настройка базы данных местоположений в Lync Server 2013](lync-server-2013-configure-the-location-database.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-110">For details about how to perform these tasks, see [Configure the location database in Lync Server 2013](lync-server-2013-configure-the-location-database.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b9ea4-111">Расположения, добавленные в центральную базу данных, недоступно для клиента, пока они не опубликованы с помощью команды командной консоли Lync Server и реплицируются в локальные магазины пула.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-111">Locations added to the central location database are not available to the client until they have been published by using a Lync Server Management Shell command and are replicated to the pool's local stores.</span></span> <span data-ttu-id="b9ea4-112">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-publish-the-location-database.md">Публикация базы данных местоположений из Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-112">For details, see <A href="lync-server-2013-publish-the-location-database.md">Publish the location database from Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="b9ea4-113">В данном разделе описываются вопросы, которые необходимо рассмотреть во время планирования обновления и поддержки базы данных расположений.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-113">This section describes things to consider as you plan to update and maintain the location database.</span></span>

<div>

## <a name="planning-emergency-locations"></a><span data-ttu-id="b9ea4-114">Планирование сведений о расположении для экстренных служб</span><span class="sxs-lookup"><span data-stu-id="b9ea4-114">Planning Emergency Locations</span></span>

<span data-ttu-id="b9ea4-115">При использовании ELIN Gateways вы заполняете базу данных сведений о расположении на административный адрес, определенное расположение в здании и по крайней мере один ELIN для каждого места.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-115">When you use ELIN gateways, you populate the Location Information service database with the civic address, a specific location within a building, and at least one ELIN for each location .</span></span> <span data-ttu-id="b9ea4-116">Во время этапа планирования рекомендуется решить вопрос о присвоении имен расположений и определить способ назначения номеров ELIN.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-116">During the planning phase, it is a good idea to decide how you want to name the locations and how you want to assign ELINs.</span></span>

<div>

## <a name="planning-location-names"></a><span data-ttu-id="b9ea4-117">Планирование имен расположений</span><span class="sxs-lookup"><span data-stu-id="b9ea4-117">Planning Location Names</span></span>

<span data-ttu-id="b9ea4-118">В поле " **Расположение** службы сведений о расположении", которое содержит конкретное расположение в здании, имеет максимальную длину 20 символов (включая пробелы).</span><span class="sxs-lookup"><span data-stu-id="b9ea4-118">The Location Information service **Location** field, which holds the specific location within a building, has a maximum length of 20 characters (including spaces).</span></span> <span data-ttu-id="b9ea4-119">Учитывая это ограничение, в поле рекомендуется включить следующие данные.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-119">Within that limited length, try to include the following:</span></span>

  - <span data-ttu-id="b9ea4-p104">Понятное имя, идентифицирующее расположение звонящего в аварийную службу, которое позволит агентам аварийной службы быстрее находить указанное расположение в момент прибытия по адресу. Это имя расположения может включать номер здания, номер этажа, обозначение корпусов, номер комнаты и т. д. Избегайте употребления неявных сокращенных названий, известных только сотрудникам, что может привести к направлению аварийной службы по неправильному адресу.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-p104">An easy-to-understand name that identifies the location of the 911 caller to help ensure that emergency responders find the specific location promptly when they arrive at the civic address. This location name may include a building number, floor number, wing designator, room number, and so on. Avoid nicknames that are known only to employees, which might cause emergency responders to go to the wrong location.</span></span>

  - <span data-ttu-id="b9ea4-123">Идентификатор места, с помощью которого пользователи смогут легко видеть, что клиент Lync берет на себя нужное расположение.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-123">A location identifier that helps users to easily see that their Lync client picked up the correct location.</span></span> <span data-ttu-id="b9ea4-124">Клиент Lync автоматически объединяет и отображает обнаруженные поля " **место** " и " **город** " в заголовке.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-124">The Lync client automatically concatenates and displays the discovered **Location** and **City** fields in its header.</span></span> <span data-ttu-id="b9ea4-125">Рекомендуется добавить почтовый адрес здания в каждый идентификатор местоположения (например, "1-й этаж \<street number\> ").</span><span class="sxs-lookup"><span data-stu-id="b9ea4-125">A good practice is to add the street address of the building to each location identifier (for example, "1st Floor \<street number\>").</span></span> <span data-ttu-id="b9ea4-126">Без почтового адреса общий идентификатор расположения, такой как "1‑й этаж" может применяться к любому зданию в городе.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-126">Without the street address, a generic location identifier such as "1st Floor" could apply to any building in the city.</span></span>

  - <span data-ttu-id="b9ea4-127">Если расположение определяется приблизительно, например по точке беспроводного доступа, можно добавить слово Near (например, "примерно 1-й этаж 1234").</span><span class="sxs-lookup"><span data-stu-id="b9ea4-127">If the location is approximate because it’s determined by a wireless access point, you may want to add the word Near (for example, "Near 1st Floor 1234").</span></span>

</div>

<div>

## <a name="planning-elins"></a><span data-ttu-id="b9ea4-128">Планирование номеров ELIN</span><span class="sxs-lookup"><span data-stu-id="b9ea4-128">Planning ELINs</span></span>

<span data-ttu-id="b9ea4-p106">После того как вы определите, каким образом следует разделить строение на расположения, необходимо решить, сколько номеров ELIN следует назначить каждому расположению. Например, в здании с несколькими этажами или корпусами различным областям можно назначить разные аварийные зоны. Обычно каждый этаж в здании считается отдельным расположением. Каждому расположению затем назначается один или несколько номеров ELIN, которые используются в качестве номеров вызова во время экстренных звонков. Обратитесь к поставщику PSTN, чтобы получить телефонные номера, которые можно использовать для ELIN. В следующей таблице представлен пример расположений для определенного почтового адреса.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-p106">After you decide how you want to divide your building space into locations, you need to decide how many ELINs to assign to each location. For example, in a multifloor or multitenant building, different areas in the building can be assigned different emergency zones. Typically, each floor in a building is designated as a location. Each location is then assigned one or more ELINs, which are used as the calling number(s) during an emergency call. Contact your PSTN carrier for phone numbers that you can use for ELINs. The following table provides an example of locations for a specific street address.</span></span>

### <a name="sample-location-and-elin-assignments"></a><span data-ttu-id="b9ea4-135">Пример назначений расположений и ELIN</span><span class="sxs-lookup"><span data-stu-id="b9ea4-135">Sample Location and ELIN Assignments</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9ea4-136">Область здания</span><span class="sxs-lookup"><span data-stu-id="b9ea4-136">Building Area</span></span></th>
<th><span data-ttu-id="b9ea4-137">Расположение</span><span class="sxs-lookup"><span data-stu-id="b9ea4-137">Location</span></span></th>
<th><span data-ttu-id="b9ea4-138">ELIN</span><span class="sxs-lookup"><span data-stu-id="b9ea4-138">ELIN</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9ea4-139">Первый этаж</span><span class="sxs-lookup"><span data-stu-id="b9ea4-139">First floor</span></span></p></td>
<td><p><span data-ttu-id="b9ea4-140">1</span><span class="sxs-lookup"><span data-stu-id="b9ea4-140">1</span></span></p></td>
<td><p><span data-ttu-id="b9ea4-141">425-555-0100</span><span class="sxs-lookup"><span data-stu-id="b9ea4-141">425-555-0100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9ea4-142">Второй этаж</span><span class="sxs-lookup"><span data-stu-id="b9ea4-142">Second floor</span></span></p></td>
<td><p><span data-ttu-id="b9ea4-143">2</span><span class="sxs-lookup"><span data-stu-id="b9ea4-143">2</span></span></p></td>
<td><p><span data-ttu-id="b9ea4-144">425-555-0111</span><span class="sxs-lookup"><span data-stu-id="b9ea4-144">425-555-0111</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9ea4-145">Третий этаж</span><span class="sxs-lookup"><span data-stu-id="b9ea4-145">Third floor</span></span></p></td>
<td><p><span data-ttu-id="b9ea4-146">3</span><span class="sxs-lookup"><span data-stu-id="b9ea4-146">3</span></span></p></td>
<td><p><span data-ttu-id="b9ea4-147">425-555-0123</span><span class="sxs-lookup"><span data-stu-id="b9ea4-147">425-555-0123</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9ea4-148">Задаваемые расположения должны удовлетворять следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-148">The locations you define should meet the following requirements:</span></span>

  - <span data-ttu-id="b9ea4-149">Соответствовать местным и общегосударственным правилам в отношении максимальной области для расположения и числа расположений на каждый почтовый адрес.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-149">Comply with local and national/regional regulations in terms of maximum area per location and number of locations per street address.</span></span>

  - <span data-ttu-id="b9ea4-150">Быть достаточно конкретными, чтобы можно было легко определить местонахождение абонента, совершающего экстренный вызов.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-150">Are specific enough to make it easy to locate the emergency caller.</span></span>

</div>

</div>

<div>

## <a name="populating-the-location-database"></a><span data-ttu-id="b9ea4-151">Заполнение базы данных расположений</span><span class="sxs-lookup"><span data-stu-id="b9ea4-151">Populating the Location Database</span></span>

<span data-ttu-id="b9ea4-152">Ниже приведены вопросы, которые помогут определить порядок заполнения базы данных расположений.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-152">The following questions will help you determine how to will populate the location database.</span></span>

  - <span data-ttu-id="b9ea4-153">**Какой процесс будет использоваться для заполнения базы данных расположений?**</span><span class="sxs-lookup"><span data-stu-id="b9ea4-153">**What process will you use to populate the location database?**</span></span>  
    <span data-ttu-id="b9ea4-p107">Где хранятся данные и какие действия необходимо выполнить, чтобы преобразовать данные в формат, требуемый базой данных расположений? Будут ли расположения добавляться по отдельности или массово, используя CSV-файл?</span><span class="sxs-lookup"><span data-stu-id="b9ea4-p107">Where does the data exist, and what steps do you need to take to convert the data into the format required by the location database? Will you add locations individually, or in bulk, by using a CSV file?</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ea4-156">**Используется ли сторонняя база данных, которая уже содержит сопоставление расположений?**</span><span class="sxs-lookup"><span data-stu-id="b9ea4-156">**Do you have a third party database that already contains a mapping of locations?**</span></span>  
    <span data-ttu-id="b9ea4-157">С помощью параметра службы дополнительных сведений о расположении Lync Server для подключения к базе данных третьих лиц вы можете группировать и управлять ими с помощью автономной платформы.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-157">By using Lync Server's Secondary Location Information service option to connect to a third-party database, you can group and manage locations by using an offline platform.</span></span> <span data-ttu-id="b9ea4-158">Преимущество этого метода заключается в том, что он позволяет связывать расположения не только с идентификаторами сети, но и с пользователями.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-158">A benefit to this approach is that in addition to associating locations to network identifiers, you can associate locations to a user.</span></span> <span data-ttu-id="b9ea4-159">Это означает, что служба сведений о расположении может возвращать несколько адресов, исходящих из дополнительной службы сведений о расположении, в клиенте Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-159">This means that the Location Information service can return multiple addresses, originating from the Secondary Location Information service, to a Lync Server client.</span></span> <span data-ttu-id="b9ea4-160">Пользователь затем может выбрать наиболее подходящее расположение.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-160">The user can then choose the most appropriate location.</span></span>
    
    <span data-ttu-id="b9ea4-161">Для интеграции со службой сведений о расположении база данных стороннего поставщика должна следовать схеме запроса на расположение на сервере Lync Server/ответа.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-161">To integrate with the Location Information service, the third-party database must follow the Lync Server Location Request/Response schema.</span></span> <span data-ttu-id="b9ea4-162">Подробности можно найти в разделе <https://go.microsoft.com/fwlink/p/?linkid=213819> .</span><span class="sxs-lookup"><span data-stu-id="b9ea4-162">For details, see <https://go.microsoft.com/fwlink/p/?linkid=213819>.</span></span> <span data-ttu-id="b9ea4-163">Дополнительные сведения о развертывании дополнительной службы сведений о расположении можно найти [в разделе Настройка дополнительной службы сведений о расположении в Lync Server 2013](lync-server-2013-configure-a-secondary-location-information-service.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-163">For details about deploying a Secondary Location Information service, see [Configure a secondary Location Information service in Lync Server 2013](lync-server-2013-configure-a-secondary-location-information-service.md) in the Deployment documentation.</span></span>

<span data-ttu-id="b9ea4-164">Сведения о заполнении базы данных местоположений содержатся в разделе [Настройка базы данных местоположений в Lync Server 2013](lync-server-2013-configure-the-location-database.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-164">For details about populating the location database, see [Configure the location database in Lync Server 2013](lync-server-2013-configure-the-location-database.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="maintaining-the-location-database"></a><span data-ttu-id="b9ea4-165">Обслуживание базы данных расположений</span><span class="sxs-lookup"><span data-stu-id="b9ea4-165">Maintaining the Location Database</span></span>

<span data-ttu-id="b9ea4-p110">После заполнения базы данных необходимо разработать стратегию обновления базы данных по мере внесения изменений в конфигурацию сети. Ниже приведены вопросы, которые помогут определить порядок обслуживания базы данных расположений.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-p110">After you populate the location database, you need to develop a strategy for updating the database as the network configuration changes. The following questions will help you determine how to maintain the location database.</span></span>

  - <span data-ttu-id="b9ea4-168">**Как будет обновляться база данных расположений?**</span><span class="sxs-lookup"><span data-stu-id="b9ea4-168">**How will you update the location database?**</span></span>  
    <span data-ttu-id="b9ea4-p111">Существует несколько сценариев, которые требуют обновления базы данных расположений, включая добавление протоколов WAP, изменение разводки в офисе (в связи с разными назначениями коммутаторов) и расширение подсети. Будет ли выполняться прямое обновление каждого отдельного расположения или массовое обновление всех расположений с помощью CSV-файла?</span><span class="sxs-lookup"><span data-stu-id="b9ea4-p111">There are several scenarios that require an update to the location database, including adding wireless access points (WAPs), office recabling (resulting in different switch assignments), and subnet expansion. Will you directly update each individual location, or will you perform a bulk update of all the locations by using a CSV file?</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ea4-171">**Будет ли использоваться для сопоставления MAC-адресов клиентов Lync с портами и идентификаторами коммутаторов приложение SNMP?**</span><span class="sxs-lookup"><span data-stu-id="b9ea4-171">**Will you use an SNMP application to match Lync client MAC addresses to port and switch identifiers?**</span></span>  
    <span data-ttu-id="b9ea4-172">При использовании приложения SNMP потребуется разработать ручную процедуру, которая позволит поддерживать согласованность данных о портах и корпусах коммутаторов между приложением SNMP и базой данных расположений.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-172">If you use an SNMP application, you need to develop a manual process for keeping the switch chassis and port information consistent between the SNMP application and the location database.</span></span> <span data-ttu-id="b9ea4-173">Если приложение SNMP возвращает IP-адрес или идентификатор порта, не включенный в базу данных, Служба сведений о расположении не сможет возвращать данные о расположении клиенту.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-173">If the SNMP application returns a chassis IP address or port ID that is not included in the database, the Location Information service will not be able to return a location to the client.</span></span>

<span data-ttu-id="b9ea4-174"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9ea4-174"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

