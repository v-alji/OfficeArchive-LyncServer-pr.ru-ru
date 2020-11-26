---
title: 'Lync Server 2013: пользовательские модели'
description: 'Lync Server 2013: пользовательские модели.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 user models
ms:assetid: c551371c-d740-4372-bada-f0d713ec0d33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398811(v=OCS.15)
ms:contentKeyID: 49733811
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15be3f4c002de6cfb9ade4f13d80aedb59d76a82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439151"
---
# <a name="user-models-in-lync-server-2013"></a><span data-ttu-id="f1efb-103">Пользовательские модели в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1efb-103">User models in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1efb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1efb-104">

<span> </span></span></span>

<span data-ttu-id="f1efb-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="f1efb-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="f1efb-106">Описанные здесь модели пользователей предоставляют основу для измерения и рекомендации по планированию производительности, описанные в статье [Планирование загрузки для Lync Server 2013 с помощью пользовательских моделей](lync-server-2013-capacity-planning-using-the-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-106">The user models described here provide the basis for the capacity planning measurements and recommendations described in [Capacity planning for Lync Server 2013 using the user models](lync-server-2013-capacity-planning-using-the-user-models.md).</span></span>

<div>

## <a name="lync-server-2013-user-models"></a><span data-ttu-id="f1efb-107">Пользовательские модели Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1efb-107">Lync Server 2013 User Models</span></span>

<span data-ttu-id="f1efb-108">В приведенной ниже таблице описаны пользовательские модели для регистрации, контактов, обмена мгновенными сообщениями и присутствия в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1efb-108">The following table describes the user model for registration, contacts, instant messaging (IM), and presence for Lync Server 2013.</span></span>

### <a name="environment-and-registration-user-model"></a><span data-ttu-id="f1efb-109">Пользовательская модель среды и регистрации</span><span class="sxs-lookup"><span data-stu-id="f1efb-109">Environment and Registration User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-110">Категория</span><span class="sxs-lookup"><span data-stu-id="f1efb-110">Category</span></span></th>
<th><span data-ttu-id="f1efb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-112">Размер и распределение развертывания</span><span class="sxs-lookup"><span data-stu-id="f1efb-112">Deployment size and distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-113">Мы моделируем большое развертывание с тремя центральными сайтами и с одним интерфейсным пулом на каждом сайте.</span><span class="sxs-lookup"><span data-stu-id="f1efb-113">We model a large deployment with three central sites, with one Front End pool per site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-114">Процент пользователей Active Directory</span><span class="sxs-lookup"><span data-stu-id="f1efb-114">Percentage of Active Directory users</span></span></p></td>
<td><p><span data-ttu-id="f1efb-115">Предполагается, что 70% от всех пользователей Active Directory в организации разрешено для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f1efb-115">We assume that 70% of all Active Directory users in the organization are enabled for Lync Server.</span></span> <span data-ttu-id="f1efb-116">80% от пользователей, которые работают с этой учетной записью, входят в состав сервера Lync Server каждый день (80% параллелизма).</span><span class="sxs-lookup"><span data-stu-id="f1efb-116">80% of those enabled users are logged on to Lync Server each day (80% concurrency).</span></span> <span data-ttu-id="f1efb-117">На основе количества параллельных пользователей рассчитываются числа в оставшейся части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="f1efb-117">The concurrent users are the basis for the numbers in the rest of this section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-118">Изменения в службе каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="f1efb-118">Active Directory changes</span></span></p></td>
<td><p><span data-ttu-id="f1efb-119">Предполагается, что 0,5% от общего числа пользователей созданы и включены для Lync в Active Directory, а это 0,5% от общего числа пользователей отключаются из Active Directory и из Lync на каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="f1efb-119">We assume that 0.5% of total users are created and enabled for Lync in Active Directory each week, and that 0.5% of total users are disabled from Active Directory and from Lync each week.</span></span> <span data-ttu-id="f1efb-120">5% пользователей по крайней мере один атрибут Active Directory изменялся каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="f1efb-120">5% of users have at least one Active Directory attribute changed each week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-121">Группы рассылки Active Directory</span><span class="sxs-lookup"><span data-stu-id="f1efb-121">Active Directory distribution groups</span></span></p></td>
<td><p><span data-ttu-id="f1efb-122">Предполагается, что количество групп рассылки Active Directory в Организации равно трем большему числу пользователей в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f1efb-122">We assume that the number of Active Directory distribution groups in the organization is equal to three times the number of all users in Active Directory.</span></span> <span data-ttu-id="f1efb-123">Эти группы рассылки имеют следующие размеры:</span><span class="sxs-lookup"><span data-stu-id="f1efb-123">The distribution groups have the following sizes:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1efb-124">64 % имеют от 2 до 30 пользователей;</span><span class="sxs-lookup"><span data-stu-id="f1efb-124">64% have 2-30 users</span></span></p></li>
<li><p><span data-ttu-id="f1efb-125">13 % имеют от 31 до 50 пользователей;</span><span class="sxs-lookup"><span data-stu-id="f1efb-125">13% have 31-50 users</span></span></p></li>
<li><p><span data-ttu-id="f1efb-126">10 % имеют от 51 до 100 пользователей;</span><span class="sxs-lookup"><span data-stu-id="f1efb-126">10% have 51-100 users</span></span></p></li>
<li><p><span data-ttu-id="f1efb-127">13 % имеют от 101 до 500 пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-127">13% have 101-500 users</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-128">Пользователи протокола VoIP</span><span class="sxs-lookup"><span data-stu-id="f1efb-128">Voice over IP (VoIP) users</span></span></p></td>
<td><p><span data-ttu-id="f1efb-129">60% пользователей Lync Server включены в единую систему обмена сообщениями (UC) (то есть их номера телефонов принадлежат Lync Server).</span><span class="sxs-lookup"><span data-stu-id="f1efb-129">60% of Lync Server users are enabled for unified communications (UC) (that is, their phone numbers are owned by Lync Server).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-130">Распределение зарегистрированных клиентов</span><span class="sxs-lookup"><span data-stu-id="f1efb-130">Registered client distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-131">65% клиентов работают с программным обеспечением Lync 2013, включая Lync и Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="f1efb-131">65% of clients run Lync 2013 software, including Lync and Lync Phone Edition.</span></span></p>
<p><span data-ttu-id="f1efb-132">30% клиентов с запущенным клиентским программным обеспечением из предыдущей версии Lync.</span><span class="sxs-lookup"><span data-stu-id="f1efb-132">30% of clients running client software from a previous version of Lync.</span></span></p>
<p><span data-ttu-id="f1efb-133">5% клиентов, использующих Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="f1efb-133">5% of clients using Lync Web App.</span></span></p>
<p><span data-ttu-id="f1efb-p104">Мы предполагаем, что если мобильность включена, то 40 % пользователей используют эту функцию параллельно с другими вышеуказанными зарегистрированными клиентами. В этом случае коэффициент нескольких точек подключения клиента (MPOP) составляет 1:1,9. Если мобильность отключена, то коэффициент MPOP составляет 1:1,5.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p104">If mobility is enabled, we assume that 40% of users are using mobility concurrently with the other previously cited registered client options. In this case the client multiple point of presence (MPOP) ratio is 1:1.9. If mobility is disabled, the MPOP ratio is 1:1.5.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-137">Распределение удаленных пользователей</span><span class="sxs-lookup"><span data-stu-id="f1efb-137">Remote user distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-138">70 % пользователей подключается внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="f1efb-138">70% of users connecting internally.</span></span></p>
<p><span data-ttu-id="f1efb-139">30% пользователей, подключающихся через пограничный сервер и режиссер.</span><span class="sxs-lookup"><span data-stu-id="f1efb-139">30% of users connecting through an Edge Server and a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-140">Распределение контактов</span><span class="sxs-lookup"><span data-stu-id="f1efb-140">Contact distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p105">Пользователь имеет не более 1000 контактов. Менее 1 % пользователей имеет 1000 контактов. Менее 25 % пользователей имеет как минимум 100 контактов.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p105">The maximum number of contacts a user has is 1,000. Less than 1% of users have 1,000 contacts. Less than 25% of users have 100 or more contacts.</span></span></p>
<p><span data-ttu-id="f1efb-p106">Пользователи с подключением к общедоступному облаку в среднем имеют по 80 контактов. Среди них:</span><span class="sxs-lookup"><span data-stu-id="f1efb-p106">Average of 80 contacts for users with public cloud connectivity. Of these users:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1efb-p107">50 % контактов находятся внутри организации; 10 % пользователей являются удаленными, подключающимися извне через брандмауэр;</span><span class="sxs-lookup"><span data-stu-id="f1efb-p107">50% of the contacts are within the organization. 10% of those users are remote users, connecting from outside the firewall.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-148">40% контактов — это пользователи общедоступного облачного облака (например, пользователи AOL, Yahoo!, MSN или Google поговорить).</span><span class="sxs-lookup"><span data-stu-id="f1efb-148">40% of the contacts are public cloud users (such as users of AOL, Yahoo!, MSN, or Google Talk).</span></span></p></li>
<li><p><span data-ttu-id="f1efb-149">10 % контактов приходятся на федеративных партнеров.</span><span class="sxs-lookup"><span data-stu-id="f1efb-149">10% of the contacts are from federated partners.</span></span></p>
<div>

> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="f1efb-150">По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="f1efb-150">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="f1efb-151">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f1efb-151">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="f1efb-152">Messenger, пока служба не отключается.</span><span class="sxs-lookup"><span data-stu-id="f1efb-152">Messenger until the service shut down date.</span></span> <span data-ttu-id="f1efb-153">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="f1efb-153">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="f1efb-154">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="f1efb-154">has been announced.</span></span> <span data-ttu-id="f1efb-155">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f1efb-155">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="f1efb-156">USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="f1efb-156">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="f1efb-157">Messenger.</span><span class="sxs-lookup"><span data-stu-id="f1efb-157">Messenger.</span></span> <span data-ttu-id="f1efb-158">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</span><span class="sxs-lookup"><span data-stu-id="f1efb-158">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="f1efb-159">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="f1efb-159">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="f1efb-160">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="f1efb-160">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="f1efb-161">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="f1efb-161">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


</div></li>
</ul>
<p><span data-ttu-id="f1efb-p111">Пользователи без возможности подключения к общедоступному облаку в среднем имеют по 50 контактов. Среди них:</span><span class="sxs-lookup"><span data-stu-id="f1efb-p111">Average of 50 contacts for users without public cloud connectivity. Of these users:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1efb-p112">80 % контактов находятся внутри организации; 10 % пользователей являются удаленными, подключающимися извне через брандмауэр;</span><span class="sxs-lookup"><span data-stu-id="f1efb-p112">80% of the contacts are within the organization. 10% of those users are remote users, connecting from outside the firewall.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-166">20 % контактов приходятся на федеративных партнеров.</span><span class="sxs-lookup"><span data-stu-id="f1efb-166">20% of the contacts are from federated partners.</span></span></p>
<p><span data-ttu-id="f1efb-p113">Каждый пользователь имеет одну группу рассылки в своем списке контактов. Для тестирования производительности мы предполагаем, что группы рассылки всегда расширенные.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p113">Each user has 1 distribution group in their contact list. For performance testing, we assume that distribution groups are always expanded.</span></span></p></li>
</ul>
<p><span data-ttu-id="f1efb-169">25% контактов пользователя используют XMPP.</span><span class="sxs-lookup"><span data-stu-id="f1efb-169">25% of a user’s contacts use XMPP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-170">Время сеанса</span><span class="sxs-lookup"><span data-stu-id="f1efb-170">Session time</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p114">Среднее время сеанса входа пользователя в систему составляет 12 часов. Все пользователи выполняют вход в течение 120 минут после начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p114">The average user logon session lasts 12 hours. All users log on within 120 minutes of the start of the session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="im-and-presence-user-model"></a><span data-ttu-id="f1efb-173">Пользовательская модель обмена мгновенными сообщениями и присутствия</span><span class="sxs-lookup"><span data-stu-id="f1efb-173">IM and Presence User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-174">Категория</span><span class="sxs-lookup"><span data-stu-id="f1efb-174">Category</span></span></th>
<th><span data-ttu-id="f1efb-175">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-176">Одноранговые сеансы обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="f1efb-176">Peer-to-peer IM sessions</span></span></p></td>
<td><p><span data-ttu-id="f1efb-177">Каждый пользователь в среднем имеет по шесть одноранговых сеансов обмена мгновенными сообщениями в день.</span><span class="sxs-lookup"><span data-stu-id="f1efb-177">Each user averages six peer-to-peer IM sessions per day.</span></span></p>
<p><span data-ttu-id="f1efb-178">10 мгновенных сообщений на сеанс.</span><span class="sxs-lookup"><span data-stu-id="f1efb-178">10 instant messages per session.</span></span></p>
<p><span data-ttu-id="f1efb-179">Каждое сообщение соответствует двум ИНФОРМАЦИОНным сообщениям SIP и 2 сообщениям SIP 200 ОК (для индикаторов состояния, таких как " &lt; имя &gt; является вводом")</span><span class="sxs-lookup"><span data-stu-id="f1efb-179">Each message is matched by two SIP INFO messages and 2 SIP 200 OK messages (for the status indicators such as “&lt;Name&gt; is Typing”)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-180">Опрос присутствия</span><span class="sxs-lookup"><span data-stu-id="f1efb-180">Presence polling</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p115">В основном для опроса присутствия мы предполагаем по 60 опросов на каждого пользователя в час. Для каждого пользователя предполагаются следующие средние значения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p115">Overall, we assume presence polling at an average of 60 polls per user per hour. For each user, assume an average of:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1efb-p116">Один опрос в день присутствия пользователей со вкладки "Организация" пользователя (но не из списка контактов). В среднем на вкладке "Организация" пользователя имеется 15 пользователей, не являющихся контактами. В день выполняется две операции просмотра карточки контакта.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p116">One poll per day of the presence of users in the user’s organization tab (but not Contacts list). Average number of non-contacts in the user’s organization tab is 15 users. Two contact card viewing operations per day.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-186">Оценивается, что один опрос присутствия каждый раз, когда пользователь щелкает имя другого пользователя для начала беседы, выполняется раз в час.</span><span class="sxs-lookup"><span data-stu-id="f1efb-186">One presence poll every time the user clicks another user to start a conversation, estimated at once per hour.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-p117">Выполняется по шесть поисков пользователей в час. При каждом выполнении поиска пакетный опрос отправляется каждому пользователю в списке результатов поиска. Мы предполагаем, что средний размер результатов поиска — 20. Если результаты поиска остаются на экране, то пакетный опрос обновляется каждые 5 минут; мы предполагаем, что будет два таких обновления в час.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p117">Six user searches per hour. Every time a search is performed, a batch poll is sent for everyone in the search result list. We assume the average size of search results is 20. If the search results stay on screen, the batch poll is refreshed every 5 minutes; we assume that there will be two such refreshes per hour.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-191">Когда пользователь открывает или предварительно просматривает электронное письмо в Outlook, выполняется опрос присутствия пользователей, указанных в полях "Кому" и "Копия". Оценивается, что просматривается по пять электронных писем в час, и в каждом письме указывается по пять пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-191">When the user opens or previews an email in Outlook, a poll of the presence of users in the To: and CC: fields of the email, estimated at five emails per hour and four users per email.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-192">Подписки на сведения о присутствии</span><span class="sxs-lookup"><span data-stu-id="f1efb-192">Presence subscriptions</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p118">Когда пользователь добавляет другого пользователя в качестве контакта, он <em>подписывается</em> на пять категорий сведений об этом пользователе. Обновления этих категорий сведений автоматически отправляются первому пользователю.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p118">When one user adds another as a contact, the first user is <em>subscribing</em> to five categories of information about the second user. Updates of these categories of information are automatically sent to the first user.</span></span></p>
<p><span data-ttu-id="f1efb-195">Для каждого клиента отправляется один пакетный запрос подписки, чтобы получить сведения о присутствии в среднем 40 контактов, с дополнительными 40 диалогами, чтобы получить сведения о присутствии для федеративных контактов.</span><span class="sxs-lookup"><span data-stu-id="f1efb-195">For each client, a single batch subscription request is sent to obtain the presence state of an average of 40 contacts, with an additional 40 dialogs to obtain presence for federated contacts.</span></span></p>
<p><span data-ttu-id="f1efb-196">Сведения о присутствии для членов расширенной группы рассылки извлекаются с помощью постоянных подписок на сведения о присутствии, а не опросов, и моделируются как 1 расширение на пользователя каждые 2 часа.</span><span class="sxs-lookup"><span data-stu-id="f1efb-196">Presence for members of an expanded distribution group is found through persistent presence subscriptions, not polling, and is modeled as 1 expansion per user for each 2 hours.</span></span></p>
<p><span data-ttu-id="f1efb-p119"><em>Краткие подписки</em> происходят, когда пользователь входит. Для всех контактов этого пользователя выполняется пакетная подписка, а затем происходит выход пользователя. Мы предполагаем 6 кратких подписок на пользователя в час, при этом каждая подписка продолжается 10 минут.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p119"><em>Short subscriptions</em> happen when a user logs in, there is a batch subscription for all the user’s contacts, and then the user soon logs off. We assume 6 short subscriptions per user per hour, where each subscription lasts 10 minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-199">Публикация сведений о присутствии</span><span class="sxs-lookup"><span data-stu-id="f1efb-199">Presence Publication</span></span></p></td>
<td><p><span data-ttu-id="f1efb-200">Состояние присутствия публикуется в среднем 4 раза на пользователя в час, максимально 6 раз на пользователя в час.</span><span class="sxs-lookup"><span data-stu-id="f1efb-200">Presence state is published at an average of 4 publications per user per hour, with a maximum 6 per user per hour.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-201">Размер документа сведений о присутствии</span><span class="sxs-lookup"><span data-stu-id="f1efb-201">Presence Document Size</span></span></p></td>
<td><p><span data-ttu-id="f1efb-202">Средний размер полного документа сведений о присутствии оценивается в 4 КБ, максимальный размер — 25 КБ.</span><span class="sxs-lookup"><span data-stu-id="f1efb-202">The average size of a complete presence document is assumed to be 4K, with a maximum of 25K.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1efb-203">В следующей таблице описывается пользовательская модель для использования адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f1efb-203">The following table describes the user model for address book use.</span></span>

### <a name="address-book-usage-user-model"></a><span data-ttu-id="f1efb-204">Пользовательская модель использования адресной книги</span><span class="sxs-lookup"><span data-stu-id="f1efb-204">Address Book Usage User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-205">Режим поиска в адресной книге</span><span class="sxs-lookup"><span data-stu-id="f1efb-205">Address Book search mode</span></span></th>
<th><span data-ttu-id="f1efb-206">Использование</span><span class="sxs-lookup"><span data-stu-id="f1efb-206">Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-207">Только веб-запрос к адресной книге (все запросы выполняются службой веб-запросов к адресной книге)</span><span class="sxs-lookup"><span data-stu-id="f1efb-207">Address Book Web Query only (all queries performed by Address Book Web Query service)</span></span></p></td>
<td><p><span data-ttu-id="f1efb-208">Четыре запроса префикса на пользователя в день.</span><span class="sxs-lookup"><span data-stu-id="f1efb-208">Four prefix queries per user per day.</span></span></p>
<p><span data-ttu-id="f1efb-p120">60 запросов точного поиска на пользователя в день. 40 % этих запросов являются пакетными, имеющими в среднем по 20 контактов на запрос. Остальные 60 % запросов имеют по одному контакту.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p120">60 exact search queries per user per day. 40% of those are batched, with an average of 20 contacts per query. The other 60% of the queries are for a single contact.</span></span></p>
<p><span data-ttu-id="f1efb-p121">25 запросов фотографий на пользователя в день. 24 являются запросами одной фотографии, один является пакетным запросом, в среднем имеющим 20 контактов.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p121">25 photo queries per user per day. 24 are for a single photo, the other is a batch query with an average of 20 contacts.</span></span></p>
<p><span data-ttu-id="f1efb-214">Один запрос поиска по всей организации на пользователя в день.</span><span class="sxs-lookup"><span data-stu-id="f1efb-214">One total organization search query per user per day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-p122">Смешанный режим, в котором используются как файл адресной книги, так и веб-запросы. Это режим по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p122">Mixed mode, both address book file and web queries used. This is the default mode.</span></span></p></td>
<td><p><span data-ttu-id="f1efb-217">В сеть приходят только два типа запросов: запрос фотографий и запрос поиска по всей организации.</span><span class="sxs-lookup"><span data-stu-id="f1efb-217">Only two types of queries go to the network, the photo and total organizational search queries.</span></span></p>
<p><span data-ttu-id="f1efb-p123">25 запросов фотографий на пользователя в день. 24 являются запросами одной фотографии, один является пакетным запросом, в среднем имеющим 20 контактов.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p123">25 photo queries per user per day. 24 are for a single photo, the other is a batch query with an average of 20 contacts.</span></span></p>
<p><span data-ttu-id="f1efb-220">Один запрос поиска по всей организации на пользователя в день.</span><span class="sxs-lookup"><span data-stu-id="f1efb-220">One total organization search query per user per day.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1efb-221">В следующей таблице описывается модель конференций.</span><span class="sxs-lookup"><span data-stu-id="f1efb-221">The following table describes the conferencing model.</span></span>

### <a name="conferencing-model"></a><span data-ttu-id="f1efb-222">Модель конференций</span><span class="sxs-lookup"><span data-stu-id="f1efb-222">Conferencing Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-223">Категория</span><span class="sxs-lookup"><span data-stu-id="f1efb-223">Category</span></span></th>
<th><span data-ttu-id="f1efb-224">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-225">Запланированные собрания и собрания за собрание &quot; &quot;</span><span class="sxs-lookup"><span data-stu-id="f1efb-225">Scheduled meetings versus &quot;Meet now&quot; meetings</span></span></p></td>
<td><p><span data-ttu-id="f1efb-226">60 % запланированных, 40 % незапланированных.</span><span class="sxs-lookup"><span data-stu-id="f1efb-226">60% scheduled, 40% unscheduled.</span></span></p>
<p><span data-ttu-id="f1efb-227">Запланированные собрания предполагают, что в 80% назначены конференции, которые представляют собой ряд повторяющихся конференций; 10% — это единовременно открытые собрания; 8% — это одновременные анонимные собрания, а 2% — разовые закрытые собрания.</span><span class="sxs-lookup"><span data-stu-id="f1efb-227">Of the scheduled meetings, we assume that 80% are assigned conferences, which are occurences of recurring conferences; 10% are one-time open meetings; 8% are one-time anonymous meetings, and 2% are one-time closed meetings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-228">Распределение клиентов конференций</span><span class="sxs-lookup"><span data-stu-id="f1efb-228">Conferencing client distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-229">Для запланированных собраний:</span><span class="sxs-lookup"><span data-stu-id="f1efb-229">For scheduled meetings:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1efb-230">65% пользователей конференц-связи используют Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f1efb-230">65% of conferencing users use Lync 2013.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-231">5% пользователей конференц-связи используют Microsoft Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="f1efb-231">5% of conferencing users use Microsoft Lync Web App.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-232">30% пользователей конференц-связи используют более ранние клиенты, в том числе Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007 и Microsoft Office Communicator Web Access (выпуск 2007).</span><span class="sxs-lookup"><span data-stu-id="f1efb-232">30% of conferencing users use earlier clients, including Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007, and Microsoft Office Communicator Web Access (2007 release).</span></span></p></li>
</ul>
<p><span data-ttu-id="f1efb-233">Для незапланированных собраний:</span><span class="sxs-lookup"><span data-stu-id="f1efb-233">For unscheduled meetings:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1efb-234">70% пользователей конференц-связи используют Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f1efb-234">70% of conferencing users use Lync 2013.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-235">30% пользователей конференц-связи используют более ранние клиенты, в том числе Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007 и Microsoft Office Communicator Web Access (выпуск 2007).</span><span class="sxs-lookup"><span data-stu-id="f1efb-235">30% of conferencing users use earlier clients, including Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007, and Microsoft Office Communicator Web Access (2007 release).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-236">Параллелизм собраний</span><span class="sxs-lookup"><span data-stu-id="f1efb-236">Meeting concurrency</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p124">5 % пользователей будут принимать участие в конференциях в рабочее время. Следовательно, в пуле из 80 000 пользователей в любое время могут принимать участие в конференции 4 000 пользователей одновременно.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p124">5% of users will be in conferences during working hours. Thus, in an 80,000-user pool, as many as 4,000 users might be in conferences at any one time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-239">Распределение собраний по использованию звука</span><span class="sxs-lookup"><span data-stu-id="f1efb-239">Meeting audio distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-240">40 % смешанных конференций, использующих звук по протоколу VoIP и по телефонному подключению, с отношением 3:1 пользователей протокола VoIP к пользователям с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="f1efb-240">40% mixed VoIP audio and dial-in conferencing, with a 3:1 ratio of VoIP users to dial-in users.</span></span></p>
<p><span data-ttu-id="f1efb-241">35 % конференций только со звуком по протоколу VoIP.</span><span class="sxs-lookup"><span data-stu-id="f1efb-241">35% VoIP audio only.</span></span></p>
<p><span data-ttu-id="f1efb-242">15 % конференций только со звуком по телефонному подключению.</span><span class="sxs-lookup"><span data-stu-id="f1efb-242">15% dial-in conferencing audio only.</span></span></p>
<p><span data-ttu-id="f1efb-243">10 % конференций без звука (конференции только с обменом мгновенными сообщениями, в среднем по пять отправленных сообщений на пользователя).</span><span class="sxs-lookup"><span data-stu-id="f1efb-243">10% no audio (IM-only conferences, with an average of five messages sent per user).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-244">Комбинирование средств представления для конференций</span><span class="sxs-lookup"><span data-stu-id="f1efb-244">Media mix for conferences</span></span></p></td>
<td><p><span data-ttu-id="f1efb-245">75 % конференций — это веб-конференции, включающие звук и некоторые другие способы совместной работы.</span><span class="sxs-lookup"><span data-stu-id="f1efb-245">75% of conferences are web conferences, which include audio plus some other collaboration modalities.</span></span></p>
<p><span data-ttu-id="f1efb-246">Для таких конференций другие способы совместной работы используются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f1efb-246">For these conferences, the other collaboration methods are as follows:</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="f1efb-247">Эти значения добавляют более 100 %, поскольку в одной конференции может использоваться несколько способов совместной работы.</span><span class="sxs-lookup"><span data-stu-id="f1efb-247">These numbers add up to more than 100% because one conference can have multiple collaboration methods.</span></span>


</div>
<ul>
<li><p><span data-ttu-id="f1efb-p125">50 % добавляют общий доступ к приложениям. Мы предполагаем, что один пользователь отправляет данные с максимальной скоростью 1,1 МБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p125">50% add application sharing. We assume one users sends data at a peak of 1.1 MB per second.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-250">50 % добавляют обмен мгновенными сообщениями (в среднем по 2 сообщения на пользователя).</span><span class="sxs-lookup"><span data-stu-id="f1efb-250">50% add instant messaging (with an average of 2 messages per user).</span></span></p></li>
<li><p><span data-ttu-id="f1efb-p126">20 % добавляют совместную работу с данными, включая использование PowerPoint или доски. Мы предполагаем, что в каждой конференции представляется 2 файла PowerPoint со средним размером в 10 МБ (без внедренного видео) или 30 МБ (с внедренным видео). В среднем используется 20 заметок на доску.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p126">20% add data collaboration, including PowerPoint or whiteboard In these, an average of 2 PowerPoint files presented per conference, with an average PowerPoint file size of 10 MB (without embedded video) or 30 MB (with embedded video). Average of 20 annotations per whiteboard.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-p127">20 % добавляют видео. Для 70 % из этих пользователей включена поддержка видео MultiView, и каждый пользователь получает 2–3 видеопотока.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p127">20% add video. Of these users, 70% are in conferences enabled for multiview video, where each user receives 2-3 video streams.</span></span></p></li>
<li><p><span data-ttu-id="f1efb-255">15 % добавляют общие заметки.</span><span class="sxs-lookup"><span data-stu-id="f1efb-255">15% add shared notes.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-256">Распределение участников собраний</span><span class="sxs-lookup"><span data-stu-id="f1efb-256">Meeting participant distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-257">50 % внутренних, прошедших проверку пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-257">50% internal, authenticated users.</span></span></p>
<p><span data-ttu-id="f1efb-258">25 % удаленных, прошедших проверку пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-258">25% remote access, authenticated users.</span></span></p>
<p><span data-ttu-id="f1efb-259">15 % анонимных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-259">15% anonymous users.</span></span></p>
<p><span data-ttu-id="f1efb-260">10 % федеративных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-260">10% federated users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-261">Распределение присоединений к собраниям</span><span class="sxs-lookup"><span data-stu-id="f1efb-261">Meeting join distribution</span></span></p></td>
<td><p><span data-ttu-id="f1efb-262">Моделируется присоединение пользователей к собраниям в течение первых 5 минут.</span><span class="sxs-lookup"><span data-stu-id="f1efb-262">Users are simulated as joining the meeting within the first 5 minutes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1efb-263">В обычных интерфейсных пулах Lync Server 2013 имеет максимально поддерживаемый размер собрания 250 пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-263">In regular Front End pools, Lync Server 2013 has a maximum supported meeting size of 250 users.</span></span> <span data-ttu-id="f1efb-264">В каждом пуле в каждый момент времени может быть размещено одно собрание в 250 пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-264">Each pool can host one 250-user meeting at a time.</span></span> <span data-ttu-id="f1efb-265">Во время проведения такого большого собрания в пуле также могут размещаться другие небольшие конференции.</span><span class="sxs-lookup"><span data-stu-id="f1efb-265">While this large meeting is occurring, the pool can also host other smaller conferences.</span></span> <span data-ttu-id="f1efb-266">Кроме того, можно поддерживать собрания до 1000 пользователей, настраивая выделенный пул для размещения таких собраний.</span><span class="sxs-lookup"><span data-stu-id="f1efb-266">Additionally, you can support meetings of up to 1000 users by setting up a dedicated pool to host these meetings.</span></span> <span data-ttu-id="f1efb-267">Подробные сведения можно найти [в разделе Поддержка для крупных собраний в Lync Server 2013](lync-server-2013-support-for-large-meetings.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-267">For details, see [Support for large meetings in Lync Server 2013](lync-server-2013-support-for-large-meetings.md).</span></span>

<span data-ttu-id="f1efb-268">Конференции моделировались следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1efb-268">Conferences were simulated as follows:</span></span>

  - <span data-ttu-id="f1efb-269">85 % конференций имели четырех участников;</span><span class="sxs-lookup"><span data-stu-id="f1efb-269">85% of conferences had four participants.</span></span>

  - <span data-ttu-id="f1efb-270">10 % конференций имели шесть участников;</span><span class="sxs-lookup"><span data-stu-id="f1efb-270">10% of conferences had six participants.</span></span>

  - <span data-ttu-id="f1efb-271">5 % конференций имели одиннадцать участников;</span><span class="sxs-lookup"><span data-stu-id="f1efb-271">5% of conferences had 11 participants.</span></span>

  - <span data-ttu-id="f1efb-272">одна большая конференция с 250 участниками.</span><span class="sxs-lookup"><span data-stu-id="f1efb-272">One large conference of 250 users.</span></span>

<span data-ttu-id="f1efb-273">В следующей таблице приводятся подробные сведения о пользовательской модели конференций, в которых участвовали пользователи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="f1efb-273">The following table provides details about the user model for conferences involving dial-in users.</span></span>

### <a name="dial-in-conferencing-user-model"></a><span data-ttu-id="f1efb-274">Пользовательская модель конференции с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="f1efb-274">Dial-In Conferencing User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-275">Категория</span><span class="sxs-lookup"><span data-stu-id="f1efb-275">Category</span></span></th>
<th><span data-ttu-id="f1efb-276">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-277">Прошедшие проверку и анонимные участники</span><span class="sxs-lookup"><span data-stu-id="f1efb-277">Authenticated/anonymous</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p129">70 % участников присоединяются как анонимные, и им предлагается указать записанное имя. 30 % присоединяются как прошедшие проверку пользователи.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p129">70% of callers join as anonymous and are prompted for a recorded name. 30% join as authenticated users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-280">Продолжительность вызова и музыка при удержании</span><span class="sxs-lookup"><span data-stu-id="f1efb-280">Call duration and music on hold</span></span></p></td>
<td><p><span data-ttu-id="f1efb-281">Средняя продолжительность вызова без воспроизведения музыки при удержании: 50 секунд.</span><span class="sxs-lookup"><span data-stu-id="f1efb-281">Average call duration without music on hold: 50 seconds.</span></span></p>
<p><span data-ttu-id="f1efb-282">50 % звонящих пользователей прослушивают музыку при удержании в среднем 5 минут.</span><span class="sxs-lookup"><span data-stu-id="f1efb-282">50% of call-in users hear music on hold, for an average of 5 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-283">Двухтональный многочастотный набор (DTMF)</span><span class="sxs-lookup"><span data-stu-id="f1efb-283">Dual-tone multifrequency (DTMF)</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p130">15 % конференций с подключением по телефону имеют ведущих по телефону. 10 % смешанных конференций, включающих пользователей с телефонным подключением, также имеют ведущих по телефону.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p130">15% of conferences that are dial-in only have phone leaders. 10% of mixed conferences that include dial-in users also have phone leaders.</span></span></p>
<p><span data-ttu-id="f1efb-286">20 % ведущих по телефону используют по 2 команды DTMF на конференцию.</span><span class="sxs-lookup"><span data-stu-id="f1efb-286">20% of phone leaders use 2 DTMF commands per conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-287">Языки оповещений</span><span class="sxs-lookup"><span data-stu-id="f1efb-287">Announcement languages</span></span></p></td>
<td><p><span data-ttu-id="f1efb-288">При моделировании в качестве языка оповещений использовался английский.</span><span class="sxs-lookup"><span data-stu-id="f1efb-288">Simulations use English as the announcement language.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1efb-289">В следующей таблице предоставляются сведения по пользовательской модели "залов ожидания" конференций.</span><span class="sxs-lookup"><span data-stu-id="f1efb-289">The following table provides details about the user model for conference lobbies.</span></span>

### <a name="conference-lobby-user-model"></a><span data-ttu-id="f1efb-290">Пользовательская модель "залов ожидания" конференций</span><span class="sxs-lookup"><span data-stu-id="f1efb-290">Conference Lobby User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-291">Категория</span><span class="sxs-lookup"><span data-stu-id="f1efb-291">Category</span></span></th>
<th><span data-ttu-id="f1efb-292">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-293">Количество пользователей в "зале ожидания"</span><span class="sxs-lookup"><span data-stu-id="f1efb-293">Number of users in lobby</span></span></p></td>
<td><p><span data-ttu-id="f1efb-294">5 % пользователей с телефонным подключением и 25 % других пользователей проходят через "зал ожидания"</span><span class="sxs-lookup"><span data-stu-id="f1efb-294">5% of dial-in users go through the lobby, and 25% of other users go through the lobby</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-295">Приглашение из "зала ожидания"</span><span class="sxs-lookup"><span data-stu-id="f1efb-295">Admitting from lobby</span></span></p></td>
<td><p><span data-ttu-id="f1efb-296">При моделировании все пользователи приглашались выступающим до истечения времени ожидания клиента.</span><span class="sxs-lookup"><span data-stu-id="f1efb-296">In simulations, all users were admitted by the presenter before client timeout.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1efb-297">В следующей таблице описывается пользовательская модель для прочих одноранговых сеансов.</span><span class="sxs-lookup"><span data-stu-id="f1efb-297">The following table describes the user model for other peer-to-peer sessions.</span></span>

### <a name="peer-to-peer-sessions-user-model"></a><span data-ttu-id="f1efb-298">Пользовательская модель одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="f1efb-298">Peer-to-Peer Sessions User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-299">Категория</span><span class="sxs-lookup"><span data-stu-id="f1efb-299">Category</span></span></th>
<th><span data-ttu-id="f1efb-300">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-300">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-301">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="f1efb-301">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="f1efb-302">Каждый пользователь участвует в 5 одноранговых сеансах общего доступа к приложениям в месяц, в среднем по 0,25 сеанса в день.</span><span class="sxs-lookup"><span data-stu-id="f1efb-302">Each user participates in 5 peer-to-peer application sharing sessions per month, for an average of 0.25 sessions per day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-303">Передача файлов</span><span class="sxs-lookup"><span data-stu-id="f1efb-303">File transfer</span></span></p></td>
<td><p><span data-ttu-id="f1efb-p131">Каждый пользователь участвует в 1 одноранговом сеансе передачи файлов в месяц (в качестве части сеанса обмена мгновенными сообщениями), в среднем по 0,05 сеанса в день. Средний размер передаваемого файла в сеансе составляет 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p131">Each user participates in 1 peer-to-peer file transfer session per month (as part of an IM session), for an average of 0.05 sessions per day. The average session file size transferred is 1 MB.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1efb-306">В следующей таблице описывается пользовательская модель для политик.</span><span class="sxs-lookup"><span data-stu-id="f1efb-306">The following table describes the user model for policies.</span></span>

### <a name="policies-user-model"></a><span data-ttu-id="f1efb-307">Пользовательская модель политик</span><span class="sxs-lookup"><span data-stu-id="f1efb-307">Policies User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1efb-308">Категория</span><span class="sxs-lookup"><span data-stu-id="f1efb-308">Category</span></span></th>
<th><span data-ttu-id="f1efb-309">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-309">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1efb-310">Политики конференц-связи, присутствия и архивации</span><span class="sxs-lookup"><span data-stu-id="f1efb-310">Conferencing, Presence, and Archiving Policies</span></span></p></td>
<td><p><span data-ttu-id="f1efb-311">Мы предполагаем, что существует одна глобальная политика, 10 помеченных политик конференц-связи, 4 политики архивации и 10 помеченных политик присутствия.</span><span class="sxs-lookup"><span data-stu-id="f1efb-311">We assume that there is one global policy, 10 tag conferencing policies, 4 Archiving policies, and 10 tag presence policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1efb-312">Политика голосовой связи</span><span class="sxs-lookup"><span data-stu-id="f1efb-312">Voice Policy</span></span></p></td>
<td><p><span data-ttu-id="f1efb-313">Мы предполагаем, что существует одна глобальная политика и по 2 помеченные политики на сайт.</span><span class="sxs-lookup"><span data-stu-id="f1efb-313">We assume that there is one global policy and 2 tag policies per site.</span></span> <span data-ttu-id="f1efb-314">100 % сайтов имеют политику сайта, и 30 % пользователей назначена политика на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="f1efb-314">100% of sites have a site policy, and 30% of users have a per-user policy assigned.</span></span> <span data-ttu-id="f1efb-315">Мы предполагаем также по одной абонентской группе и по два маршрута на сайт.</span><span class="sxs-lookup"><span data-stu-id="f1efb-315">We assume one dial plan per site and two routes per site.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="busy-hour"></a><span data-ttu-id="f1efb-316">Период максимальной нагрузки</span><span class="sxs-lookup"><span data-stu-id="f1efb-316">Busy Hour</span></span>

<span data-ttu-id="f1efb-p133">Для одноранговых сеансов пиковая нагрузка вычисляется с помощью попыток вызовов в час наибольшей нагрузки (BHCA). Этот термин из сферы голосовой связи предполагает, что 50 % всех вызовов в день будут выполняться в 20 % времени. Это значение вычисляется по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="f1efb-p133">For peer-to-peer sessions, peak load is calculated using busy hour call attempts (BHCA). This voice industry term assumes that 50% of all calls for the day will be completed in 20% of the time. It is calculated using the following formula:</span></span>

`BHCA=(total calls * 0.5) / 1.6`

<span data-ttu-id="f1efb-320">При тестировании производительности период максимальной нагрузки моделируется путем запуска сеансов VoIP и других одноранговых сеансов с уровнем максимальной нагрузки по крайней мере 1,6 часов в день.</span><span class="sxs-lookup"><span data-stu-id="f1efb-320">Performance testing simulated busy hour by running VoIP and other peer-to-peer sessions at a busy hour load for at least 1.6 hours per day.</span></span>

<span data-ttu-id="f1efb-p134">Пиковая нагрузка конференц-связи предполагает, что 75 % всех конференций для восьмичасового дня происходит в 4 часа максимальной нагрузки. В эти часы нагрузка в полтора раза выше средней нагрузки конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p134">Conferencing peak load assumes that 75% of all conferences for an eight-hour day happen in 4 peak time hours. Those peak hours have 1.5 times the average conferencing load.</span></span>

</div>

<div>

## <a name="enterprise-voice-to-pstn-calls"></a><span data-ttu-id="f1efb-323">Корпоративная голосовая связь по КОММУТИРУЕМым звонкам</span><span class="sxs-lookup"><span data-stu-id="f1efb-323">Enterprise Voice to PSTN Calls</span></span>

<span data-ttu-id="f1efb-324">Следующие предположения применимы к голосовым звонкам для предприятий:</span><span class="sxs-lookup"><span data-stu-id="f1efb-324">The following assumptions apply to Enterprise Voice calls:</span></span>

  - <span data-ttu-id="f1efb-325">50% пользователей разрешено для поддержки корпоративной голосовой связи, а 60% от этих пользователей разрешено звонить через PSTN.</span><span class="sxs-lookup"><span data-stu-id="f1efb-325">50% of users are enabled for Enterprise Voice, and 60% of these users are enabled for PSTN calling.</span></span>

  - <span data-ttu-id="f1efb-p135">Каждый из пользователей, которым разрешены звонки в ТСОП, выполняет 4 звонка в ТСОП в течение часов максимальной нагрузки. Каждый звонок длится 3 минуты.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p135">Each of these users enabled for PSTN calling makes 4 PSTN calls during the busy hour. Each call duration is 3 minutes.</span></span>

  - <span data-ttu-id="f1efb-328">В 65 % этих голосовых звонков в ТСОП используется обход сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="f1efb-328">65% of these PSTN voice calls use media bypass.</span></span>

</div>

<div>

## <a name="mobility"></a><span data-ttu-id="f1efb-329">Мобильность</span><span class="sxs-lookup"><span data-stu-id="f1efb-329">Mobility</span></span>

<span data-ttu-id="f1efb-p136">Предполагается, что для 40 % зарегистрированных пользователей включена поддержка мобильности. Для каждого из пользователей с поддержкой мобильности предполагается, что использование мобильного клиента является дополнительным к использованию других экземпляров MPOP для этого пользователя, за исключением взаимодействий в конференциях, в которых мобильный клиент является просто еще одним типом клиента, используемым для участия в конференциях.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p136">40% of registered users are assumed to be enabled for Mobility. For each user that has mobility enabled, we assume that the activity of the mobile client is additive to that of the other MPOP instances for that user, with the exception of conferencing interactions, for which the mobility client is just another client type that can be used to participate in conferences.</span></span>

</div>

<div>

## <a name="persistent-chat"></a><span data-ttu-id="f1efb-332">Сохраняемый сеанс беседы</span><span class="sxs-lookup"><span data-stu-id="f1efb-332">Persistent Chat</span></span>

<span data-ttu-id="f1efb-333">Мы предполагаем, что 25 % зарегистрированных пользователей будут принимать участие в сеансах сохраняемого чата со следующими характеристиками:</span><span class="sxs-lookup"><span data-stu-id="f1efb-333">We assume that 25% of registered users will be involved in Persistent chat sessions, with the following characteristics:</span></span>

  - <span data-ttu-id="f1efb-334">В среднем по 1,5 комнаты чата на пользователя</span><span class="sxs-lookup"><span data-stu-id="f1efb-334">An average of 1.5 chat rooms per user</span></span>

  - <span data-ttu-id="f1efb-335">Каждая комната чата приводит к выполнению 12 запросов опроса в час, и каждый из опросов в среднем выполняется для 10 пользователей.</span><span class="sxs-lookup"><span data-stu-id="f1efb-335">Each chat room results in 12 polling requests per hour, targeting an average of 10 users each</span></span>

</div>

<div>

## <a name="response-group-and-call-park"></a><span data-ttu-id="f1efb-336">Группа ответа и парковка вызовов</span><span class="sxs-lookup"><span data-stu-id="f1efb-336">Response Group and Call Park</span></span>

<span data-ttu-id="f1efb-p137">Мы предполагаем, что 0,15 % зарегистрированных пользователей входят в группы ответа. Мы также предполагаем, что в каждый момент времени 0,02 % зарегистрированных пользователей имеют запаркованные вызовы.</span><span class="sxs-lookup"><span data-stu-id="f1efb-p137">We assume that 0.15% of registered users belong to response groups. We assume that 0.02% of registered users have parked calls at any given point of time.</span></span>

<span data-ttu-id="f1efb-339"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1efb-339"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

