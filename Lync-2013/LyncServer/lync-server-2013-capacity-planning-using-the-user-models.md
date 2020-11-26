---
title: Планирование мощностей Lync Server 2013 с помощью пользовательских моделей
description: Lync Server 2013 планирование мощностей с помощью пользовательских моделей.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning using the user models
ms:assetid: 902ab23e-94d6-482a-9d6e-c0b28dc3e03d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615015(v=OCS.15)
ms:contentKeyID: 49733733
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b710f7ec88dd75c872d704f2169fa2f161fc186
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435511"
---
# <a name="capacity-planning-for-lync-server-2013-using-the-user-models"></a><span data-ttu-id="34532-103">Планирование мощностей для Lync Server 2013 с помощью пользовательских моделей</span><span class="sxs-lookup"><span data-stu-id="34532-103">Capacity planning for Lync Server 2013 using the user models</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34532-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34532-104">

<span> </span></span></span>

<span data-ttu-id="34532-105">_**Тема последнего изменения:** 2014-01-14_</span><span class="sxs-lookup"><span data-stu-id="34532-105">_**Topic Last Modified:** 2014-01-14_</span></span>

<span data-ttu-id="34532-106">В этом разделе приводятся рекомендации о том, сколько серверов нужно на сайте для числа пользователей на сайте в соответствии с описанием использования в [моделях пользователей в Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="34532-106">This section provides guidance on how many servers you need at a site for the number of users at that site, according to the usage described in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<div>

## <a name="tested-hardware-platform"></a><span data-ttu-id="34532-107">Аппаратная платформа для тестирования</span><span class="sxs-lookup"><span data-stu-id="34532-107">Tested Hardware Platform</span></span>

<span data-ttu-id="34532-108">Все результаты и рекомендации по развертыванию в этом разделе основаны на тестировании производительности на серверах с оборудованием, описанных в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="34532-108">All the performance results and deployment recommendations in this section are based on performance testing on servers running the hardware described in the following table.</span></span> <span data-ttu-id="34532-109">Мы рекомендуем использовать похожие аппаратные средства.</span><span class="sxs-lookup"><span data-stu-id="34532-109">We recommend that you use similar hardware.</span></span> <span data-ttu-id="34532-110">Если вы используете менее мощное оборудование, то могут возникать проблемы с функциональностью или с низкой производительностью.</span><span class="sxs-lookup"><span data-stu-id="34532-110">If you use less powerful hardware, you may experience functionality problems or poor performance.</span></span> <span data-ttu-id="34532-111">Обратите внимание на то, что эти рекомендации по оборудованию выше, чем в предыдущих версиях Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34532-111">Note that these hardware recommendations are higher than those of previous versions of Lync Server.</span></span>

### <a name="hardware-used-in-performance-testing"></a><span data-ttu-id="34532-112">Оборудование, использованное при проведении тестирования</span><span class="sxs-lookup"><span data-stu-id="34532-112">Hardware Used in Performance Testing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34532-113">Аппаратный компонент</span><span class="sxs-lookup"><span data-stu-id="34532-113">Hardware component</span></span></th>
<th><span data-ttu-id="34532-114">Рекомендуется</span><span class="sxs-lookup"><span data-stu-id="34532-114">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34532-115">ЦП</span><span class="sxs-lookup"><span data-stu-id="34532-115">CPU</span></span></p></td>
<td><p><span data-ttu-id="34532-116">64-разрядный двухпроцессорный комплекс, шестиядерный, 2,26 ГГц и выше</span><span class="sxs-lookup"><span data-stu-id="34532-116">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher</span></span></p>
<p><span data-ttu-id="34532-117">Процессоры Intel Itanium не поддерживаются для ролей сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34532-117">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-118">Память</span><span class="sxs-lookup"><span data-stu-id="34532-118">Memory</span></span></p></td>
<td><p><span data-ttu-id="34532-119">32 ГБ </span><span class="sxs-lookup"><span data-stu-id="34532-119">32 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34532-120">Диск</span><span class="sxs-lookup"><span data-stu-id="34532-120">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="34532-121">8 или больше дисков со скоростью вращения 10 000 об/мин и как минимум 72 ГБ свободного места.</span><span class="sxs-lookup"><span data-stu-id="34532-121">8 or more 10,000-RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="34532-122">Два диска должны использовать массив RAID 1, а остальные шесть – RAID 10.</span><span class="sxs-lookup"><span data-stu-id="34532-122">Two of the disks should use RAID 1, and six should use RAID 10.</span></span></p>
<p><span data-ttu-id="34532-123">- /</span><span class="sxs-lookup"><span data-stu-id="34532-123">- OR -</span></span></p></li>
<li><p><span data-ttu-id="34532-124">Твердотельные накопители (SSD) с производительностью, аналогичной производительности 8 жестких дисков с частотой вращения шпинделя 10 000 об/мин. </span><span class="sxs-lookup"><span data-stu-id="34532-124">Solid state drives (SSDs) which provide performance similar to 8 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-125">Сеть</span><span class="sxs-lookup"><span data-stu-id="34532-125">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="34532-126">1 двухпортовый сетевой адаптер, 1 Гбит/с или выше (рекомендуется 2 Гбит/с, для этого требуется объединение через один MAC-адрес и один IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="34532-126">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="summary-of-results"></a><span data-ttu-id="34532-127">Сводка результатов</span><span class="sxs-lookup"><span data-stu-id="34532-127">Summary of Results</span></span>

<span data-ttu-id="34532-128">Эти рекомендации описаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="34532-128">The following table summarizes these recommendations.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34532-129">Роль сервера</span><span class="sxs-lookup"><span data-stu-id="34532-129">Server role</span></span></th>
<th><span data-ttu-id="34532-130">Максимальное число поддерживаемых пользователей</span><span class="sxs-lookup"><span data-stu-id="34532-130">Maximum number of users supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34532-131">Пул переднего плана с двенадцать серверными интерфейсами и одним сервером или зеркальным набором серверных пар серверов.</span><span class="sxs-lookup"><span data-stu-id="34532-131">Front End pool with twelve Front End Servers and one Back End Server or a mirrored pair of Back End Servers.</span></span></p></td>
<td><p><span data-ttu-id="34532-132">80 000 одновременно зарегистрированных уникальных пользователей, плюс 50% пользователей с несколькими точками присутствия, представляющими немобильные экземпляры, плюс 40% пользователей Mobility; итого 152 000 конечных точек.</span><span class="sxs-lookup"><span data-stu-id="34532-132">80,000 unique users simultaneously logged in, plus 50% multiple points of presence (MPOP) representing non-mobile instances, plus 40% of users enabled for Mobility for a total of 152,000 endpoints.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-133">Аудио- и видеоконференции</span><span class="sxs-lookup"><span data-stu-id="34532-133">A/V Conferencing</span></span></p></td>
<td><p><span data-ttu-id="34532-134">Служба конференц-связи A/V, предоставляемая пулом переднего плана, поддерживает конференции пула, предоставили максимальный размер конференции для пользователей 250 и только одну такую крупную конференцию, запущенную за один раз.</span><span class="sxs-lookup"><span data-stu-id="34532-134">The A/V Conferencing service provided by a Front End pool supports the pool’s conferences assuming a maximum conference size of 250 users, and only one such large conference running at a time.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="34532-135">Кроме того, вы можете поддерживать большие конференции пользователей 250 и 1000 путем развертывания отдельного пула переднего плана с двумя серверами переднего плана для размещения больших конференций.</span><span class="sxs-lookup"><span data-stu-id="34532-135">Additionally, you can support large conferences of between 250 and 1000 users by deploying a separate Front End pool with two Front End Servers to host the large conferences.</span></span> <span data-ttu-id="34532-136">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-supporting-large-meetings.md">Поддержка собраний большого размера с помощью Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="34532-136">For details, see <A href="lync-server-2013-supporting-large-meetings.md">Supporting large meetings using Lync Server 2013</A>.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34532-137">Один пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="34532-137">One Edge Server</span></span></p></td>
<td><p><span data-ttu-id="34532-138">12 000 одновременные удаленные пользователи</span><span class="sxs-lookup"><span data-stu-id="34532-138">12,000 concurrent remote users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-139">Один режиссер</span><span class="sxs-lookup"><span data-stu-id="34532-139">One Director</span></span></p></td>
<td><p><span data-ttu-id="34532-140">12 000 одновременные удаленные пользователи</span><span class="sxs-lookup"><span data-stu-id="34532-140">12,000 concurrent remote users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34532-141">Мониторинг и архивирование</span><span class="sxs-lookup"><span data-stu-id="34532-141">Monitoring and Archiving</span></span></p></td>
<td><p><span data-ttu-id="34532-142">В Lync Server 2013 теперь можно выполнять мониторинг и архивация интерфейсных служб на каждом внешнем сервере, а не на отдельных ролях сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-142">In Lync Server 2013, the Monitoring and Archiving front end services now run on each Front End Server, instead of on separate server roles.</span></span></p>
<p><span data-ttu-id="34532-143">Для мониторинга и архивирования требуются собственные хранилища баз данных.</span><span class="sxs-lookup"><span data-stu-id="34532-143">Monitoring and Archiving each still require their own database stores.</span></span> <span data-ttu-id="34532-144">Если вы также запускаете Exchange 2013, вы можете хранить данные архивации в Exchange, а не в выделенной базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="34532-144">If you also run Exchange 2013, you can keep your Archiving data in Exchange, rather than in a dedicated SQL database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-145">Один сервер обновлений</span><span class="sxs-lookup"><span data-stu-id="34532-145">One Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="34532-146">Сервер-посредник, выровненный по внешнему серверу, запускается на каждом сервере переднего плана в пуле и должен обеспечивать достаточную емкость для пользователей в пуле.</span><span class="sxs-lookup"><span data-stu-id="34532-146">Mediation Server collocated with Front End Server runs on every Front End Server in a pool, and should provide enough capacity for the users in the pool.</span></span> <span data-ttu-id="34532-147">Для изолированного сервера-посредника ознакомьтесь с разделом "сервер-посредник" Далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="34532-147">For stand-alone Mediation Server, see the “Mediation Server” section later in this topic.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34532-148">Один стандартный сервер выпуска</span><span class="sxs-lookup"><span data-stu-id="34532-148">One Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="34532-149">Мы настоятельно рекомендуем использовать для размещения пользователей сервер стандартных выпусков, используя рекомендации по <a href="lync-server-2013-planning-for-high-availability-and-disaster-recovery.md">планированию высокой доступности и аварийного восстановления в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34532-149">We strongly recommend that if you use Standard Edition servers to host users, you always use two servers, paired using the recommendations in <a href="lync-server-2013-planning-for-high-availability-and-disaster-recovery.md">Planning for high availability and disaster recovery in Lync Server 2013</a>.</span></span> <span data-ttu-id="34532-150">Each server in the pair can host up to 2,500 users, and if one server fails the remaining server can support 5,000 users in a failover scenario.</span><span class="sxs-lookup"><span data-stu-id="34532-150">Each server in the pair can host up to 2,500 users, and if one server fails the remaining server can support 5,000 users in a failover scenario.</span></span></p>
<p><span data-ttu-id="34532-151">If your deployment includes a significant amount of audio or video traffic, server performance may suffer with more than 2,500 users per server.</span><span class="sxs-lookup"><span data-stu-id="34532-151">If your deployment includes a significant amount of audio or video traffic, server performance may suffer with more than 2,500 users per server.</span></span> <span data-ttu-id="34532-152">В этом случае рекомендуется добавить другие серверы стандартных выпусков или перейти в Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="34532-152">In this case, you should consider adding more Standard Edition servers or moving to Lync Server Enterprise Edition.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-server"></a><span data-ttu-id="34532-153">переднего плана</span><span class="sxs-lookup"><span data-stu-id="34532-153">Front End Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34532-154">Растянутые пулы для этой роли сервера не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="34532-154">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="34532-155">В пуле переднего плана вы должны иметь один сервер переднего плана для всех пользователей 6 660, размещенных в пуле, предполагая, что технология Hyper-Threading включена на всех серверах пула, и что оборудование сервера соответствует рекомендациям, приведенным в разделе [аппаратные платформы сервера для Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span><span class="sxs-lookup"><span data-stu-id="34532-155">In a Front End pool, you should have one Front End Server for every 6,660 users homed in the pool, assuming that hyper-threading is enabled on all servers in the pool, and that the server hardware meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span> <span data-ttu-id="34532-156">Максимальное количество пользователей в одном пуле переднего плана — 80 000, предполагая, что технология Hyper-Threading включена на всех серверах в пуле.</span><span class="sxs-lookup"><span data-stu-id="34532-156">The maximum number of users in one Front End pool is 80,000, assuming that hyper-threading is enabled on all the servers in the pool.</span></span> <span data-ttu-id="34532-157">Если у вас более 80 000 пользователей на сайте, вы можете развернуть более одного пула переднего плана.</span><span class="sxs-lookup"><span data-stu-id="34532-157">If you have more than 80,000 users at a site, you can deploy more than one Front End pool.</span></span>

<span data-ttu-id="34532-158">Если вы захотите количество пользователей в пуле переднего плана, включите пользователей, которые размещаются на устройствах с бесперебойной ветвлением и бесперебойно работающих серверах филиалов в филиалах, связанных с этим пулом переднего плана.</span><span class="sxs-lookup"><span data-stu-id="34532-158">When you account for the number of users in a Front End pool, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with this Front End pool.</span></span>

<span data-ttu-id="34532-159">When an active server is unavailable, its connections are transferred automatically to the other servers in the pool.</span><span class="sxs-lookup"><span data-stu-id="34532-159">When an active server is unavailable, its connections are transferred automatically to the other servers in the pool.</span></span> <span data-ttu-id="34532-160">Например, если у вас есть 30 000 пользователей и пять серверов переднего плана, то если один сервер недоступен, то при подключении к нему для пользователей 6000 необходимо передать их на четыре сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-160">For example, if you have 30,000 users and five Front End Servers, then if one server is unavailable, the connections of 6000 users need to be transferred to the other four servers.</span></span> <span data-ttu-id="34532-161">Оставшиеся четыре сервера будут иметь 7500 пользователей, что превышает рекомендованное число.</span><span class="sxs-lookup"><span data-stu-id="34532-161">The remaining four servers will each have 7500 users, which is a larger number than recommended.</span></span>

<span data-ttu-id="34532-162">Если вместо этого вы начали работать с шестью серверами переднего плана для пользователей 30 000, а затем они становятся недоступными, общее количество пользователей 5000 будет перенесено на оставшиеся пять серверов.</span><span class="sxs-lookup"><span data-stu-id="34532-162">If instead you had started with six Front End Servers for your 30,000 users and subsequently one became unavailable, a total of 5000 users will be moved to the remaining five servers.</span></span> <span data-ttu-id="34532-163">Пять серверов будут каждому узлу 6000, который входит в рекомендуемый диапазон.</span><span class="sxs-lookup"><span data-stu-id="34532-163">These five servers will each host 6000 users, which is in the recommended range.</span></span>

<span data-ttu-id="34532-164">Максимальное количество пользователей в пуле переднего плана — 80 000.</span><span class="sxs-lookup"><span data-stu-id="34532-164">The maximum number of users in a Front End pool is 80,000.</span></span> <span data-ttu-id="34532-165">Максимальное число серверов переднего плана в пуле составляет 12.</span><span class="sxs-lookup"><span data-stu-id="34532-165">The maximum number of Front End Servers in a pool is 12.</span></span>

<span data-ttu-id="34532-166">Для пула переднего плана с пользователями 80 000 для повышения производительности достаточно двенадцати серверов переднего плана в типичных развертываниях, которые следуют за [пользовательскими моделями в Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="34532-166">For a Front End pool with 80,000 users, twelve Front End Servers is sufficient for performance, in typical deployments that follow the [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span> <span data-ttu-id="34532-167">В развертываниях, разработанных для поддержки перехода на аварийный план восстановления, предполагается, что в каждом из двух групп интерфейсов, в которых каждый из них может быть размещено в обоих пулах, должен быть доступен один и тот 40 000 же пул.</span><span class="sxs-lookup"><span data-stu-id="34532-167">Deployments designed to support disaster recovery failover assume that a maximum of 40,000 users can be hosted in each of two paired Front End pools, in which each pool has enough Front End Servers to accommodate the users in both pools should one pool need to be failed over to the other.</span></span>

<span data-ttu-id="34532-168">Количество пользователей, которые поддерживают хорошую производительность с помощью определенного пула переднего плана, может отличаться от приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="34532-168">The number of users supported with good performance by a particular Front End pool may differ from these numbers for the following reasons:</span></span>

  - <span data-ttu-id="34532-169">Оборудование для серверов переднего плана не соответствует рекомендациям, описанным в разделе [аппаратные платформы сервера Lync server 2013](lync-server-2013-server-hardware-platforms.md).</span><span class="sxs-lookup"><span data-stu-id="34532-169">The hardware for your Front End Servers does not meet the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

  - <span data-ttu-id="34532-170">Использование вашей организации значительно отличается от пользовательских моделей, например значительно больше трафика для проведения конференций.</span><span class="sxs-lookup"><span data-stu-id="34532-170">Your organization’s usage differs significantly from the user models, such as significantly more conferencing traffic.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="34532-171">В Lync Server 2013 базы данных присутствия теперь размещаются на серверах переднего плана, в отличие от Lync Server 2010, где они были размещены на обратном стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-171">In Lync Server 2013, the presence databases are now hosted on Front End Servers, unlike in Lync Server 2010 where they were hosted on the Back End Server.</span></span> <span data-ttu-id="34532-172">Это означает, что производительность диска и пропускная способность серверов переднего плана не должны быть скомпрометированы в рекомендациях, описанных выше в этом разделе, и в <A href="lync-server-2013-server-hardware-platforms.md">серверных аппаратных платформах для Lync Server 2013</A>независимо от количества пользователей, размещенных на серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="34532-172">This means that the disk performance and capacity of your Front End Servers should not be compromised from the recommendations listed earlier in this section and in <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A>, regardless of the number of users hosted by your Front End Servers.</span></span>



</div>

<span data-ttu-id="34532-173">В приведенной ниже таблице показана средняя пропускная способность для обмена сообщениями и присутствия, если пользовательская модель определена в [пользовательских моделях в Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="34532-173">The following table shows the average bandwidth for IM and presence, given the user model, as defined in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34532-174">Средняя пропускная способность на пользователя</span><span class="sxs-lookup"><span data-stu-id="34532-174">Average bandwidth per user</span></span></th>
<th><span data-ttu-id="34532-175">Требования к пропускной способности на сервер переднего плана с пользователями 6 660</span><span class="sxs-lookup"><span data-stu-id="34532-175">Bandwidth requirements per Front End Server with 6,660 users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34532-176">1,3 Кбит/с</span><span class="sxs-lookup"><span data-stu-id="34532-176">1.3 Kpbs</span></span></p></td>
<td><p><span data-ttu-id="34532-177">13 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="34532-177">13 Mbps</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="34532-178">Чтобы повысить производительность мультимедиа для совместной работы серверов конференц-связи и сервера-посредников на серверах переднего плана, необходимо включить масштабирование на стороне приема (RSS) на сетевых адаптерах на серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="34532-178">To improve the media performance of the co-located A/V Conferencing and Mediation Server functionality on your Front End Servers, you should enable receive-side scaling (RSS) on the network adapters on your Front End Servers.</span></span> <span data-ttu-id="34532-179">RSS поддерживает параллельную обработку входящих пакетов несколькими процессорами сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-179">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="34532-180">Дополнительные сведения можно найти в разделе улучшенные возможности масштабирования на стороне приема в Windows Server 2008 <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> .</span><span class="sxs-lookup"><span data-stu-id="34532-180">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="34532-181">Сведения о том, как включить RSS, см. в документации сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="34532-181">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="conferencing-maximums"></a><span data-ttu-id="34532-182">Максимумы конференц-связи</span><span class="sxs-lookup"><span data-stu-id="34532-182">Conferencing Maximums</span></span>

<span data-ttu-id="34532-183">Если пользовательская модель, в которой 5% пользователей в пуле, может находиться в одной конференции, пул пользователей 80 000 может иметь около 4 000 пользователей на конференциях одновременно.</span><span class="sxs-lookup"><span data-stu-id="34532-183">Given the user model that 5% of users in a pool may be in a conference at any one time, a pool of 80,000 users could have about 4,000 users in conferences at one time.</span></span> <span data-ttu-id="34532-184">These conferences are expected to be a mix of media (some IM-only, some IM with audio, some audio/video, for example) and number of participants.</span><span class="sxs-lookup"><span data-stu-id="34532-184">These conferences are expected to be a mix of media (some IM-only, some IM with audio, some audio/video, for example) and number of participants.</span></span> <span data-ttu-id="34532-185">Ограничения для фактического количества конференций не ограничены, а фактическое использование определяет фактическую производительность.</span><span class="sxs-lookup"><span data-stu-id="34532-185">There is no hard limit for the actual number of conferences allowed, and actual usage determines the actual performance.</span></span> <span data-ttu-id="34532-186">Например, если ваша организация имеет гораздо больше конференций смешанного режима, чем предполагается для пользовательской модели, возможно, вам потребуется развернуть другие серверы переднего плана или серверы конференций/V, чем рекомендации, описанные в этом документе.</span><span class="sxs-lookup"><span data-stu-id="34532-186">For example, if your organization has many more mixed-mode conferences than are assumed in the user model, you might need to deploy more Front End Servers or A/V Conferencing Servers than the recommendations in this document.</span></span> <span data-ttu-id="34532-187">Подробные сведения о допущениях в пользовательской модели можно найти в разделе [модели пользователей в Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="34532-187">For details about the assumptions in the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<span data-ttu-id="34532-188">Максимально допустимый размер Конференции, размещенный на обычном пуле внешних интерфейсов Lync Server 2013, в котором также размещены пользователи, — 250 участников.</span><span class="sxs-lookup"><span data-stu-id="34532-188">The maximum supported conference size hosted by a regular Lync Server 2013 Front End pool which also hosts users is 250 participants.</span></span> <span data-ttu-id="34532-189">While a 250-user conference is happening, the pool still supports other conferences as well, such that a total of 5% of pool users are in concurrent conferences.</span><span class="sxs-lookup"><span data-stu-id="34532-189">While a 250-user conference is happening, the pool still supports other conferences as well, such that a total of 5% of pool users are in concurrent conferences.</span></span> <span data-ttu-id="34532-190">Например, в пуле двенадцати серверов переднего плана и пользователей 80 000, а также при Конференции 250-User, Lync Server поддерживает 3 750 других пользователей, участвующих в небольших конференциях.</span><span class="sxs-lookup"><span data-stu-id="34532-190">For example, in a pool of twelve Front End Servers and 80,000 users, while the 250-user conference is happening, Lync Server supports 3,750 other users participating in smaller conferences.</span></span>

<span data-ttu-id="34532-191">Независимо от количества пользователей, подключенного к пулу или стандартному серверному выпуску, Lync Server поддерживает минимум 125 других пользователей, участвующих в небольших конференциях в том же пуле или на сервере, где размещается конференция 250-пользователи.</span><span class="sxs-lookup"><span data-stu-id="34532-191">Regardless of the number of users homed on the Front End pool or Standard Edition server, Lync Server supports a minimum of 125 other users participating in smaller conferences on the same pool or server which is hosting a 250-user conference.</span></span>

<span data-ttu-id="34532-192">Чтобы включить конференции между пользователями 250 и 1000, вы можете настроить отдельный пул переднего плана только для того, чтобы разместить эти конференции.</span><span class="sxs-lookup"><span data-stu-id="34532-192">To enable conferences with between 250 and 1000 users, you can set up a separate Front End pool just to host those conferences.</span></span> <span data-ttu-id="34532-193">Этот пул переднего плана не будет содержать пользователей.</span><span class="sxs-lookup"><span data-stu-id="34532-193">This Front End pool will not host any users.</span></span> <span data-ttu-id="34532-194">Дополнительные сведения можно найти в разделе [Поддержка собраний большого размера с помощью Lync Server 2013](lync-server-2013-supporting-large-meetings.md).</span><span class="sxs-lookup"><span data-stu-id="34532-194">For details, see [Supporting large meetings using Lync Server 2013](lync-server-2013-supporting-large-meetings.md).</span></span>

<span data-ttu-id="34532-195">Если в вашей организации есть больше конференций смешанного режима, чем предполагается для пользовательской модели, вам может потребоваться развернуть другие серверы переднего плана, чем рекомендации в этом документе (до 12 FEs).</span><span class="sxs-lookup"><span data-stu-id="34532-195">If your organization has many more mixed-mode conferences than are assumed in the user model, you might need to deploy more Front End Servers than the recommendations in this document (up to a limit of 12 FEs).</span></span> <span data-ttu-id="34532-196">Подробные сведения о допущениях в пользовательской модели можно найти в разделе [модели пользователей в Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="34532-196">For details about the assumptions in the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

</div>

<div>

## <a name="edge-server"></a><span data-ttu-id="34532-197">Пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="34532-197">Edge Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34532-198">Растянутые пулы для этой роли сервера не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="34532-198">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="34532-199">Вы должны развернуть один пограничный сервер для каждого удаленного пользователя 12 000, который будет одновременно получать доступ к сайту.</span><span class="sxs-lookup"><span data-stu-id="34532-199">You should deploy one Edge Server for every 12,000 remote users who will access a site concurrently.</span></span> <span data-ttu-id="34532-200">Как минимум, мы рекомендуем использовать два пограничных сервера для обеспечения высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="34532-200">At a minimum we recommend two Edge Servers for high availability.</span></span> <span data-ttu-id="34532-201">Эти рекомендации предполагают, что оборудование пограничных серверов соответствует рекомендациям, приведенным в разделе [аппаратные платформы сервера для Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span><span class="sxs-lookup"><span data-stu-id="34532-201">These recommendations assume that the hardware for your Edge Servers meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="34532-202">При указании числа пользователей для пограничных серверов включите пользователей, относящихся к бесперебойным устройствам филиалов и к бесперебойным серверам филиалов в филиалах, которые связаны с пулом переднего плана на этом сайте.</span><span class="sxs-lookup"><span data-stu-id="34532-202">When you account for the number of users for the Edge Servers, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with a Front End pool at this site.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34532-203">Чтобы повысить производительность службы пограничного конференц-связи A/V на пограничных серверах, необходимо включить масштабирование на стороне приема (RSS) на сетевых адаптерах пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-203">To improve the performance of the A/V Conferencing Edge service on your Edge Servers, you should enable receive-side scaling (RSS) on the network adapters on your Edge Servers.</span></span> <span data-ttu-id="34532-204">RSS поддерживает параллельную обработку входящих пакетов несколькими процессорами сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-204">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="34532-205">Дополнительные сведения можно найти в разделе улучшенные возможности масштабирования на стороне приема в Windows Server 2008 <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> .</span><span class="sxs-lookup"><span data-stu-id="34532-205">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="34532-206">Сведения о том, как включить RSS, см. в документации сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="34532-206">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="director"></a><span data-ttu-id="34532-207">Директор</span><span class="sxs-lookup"><span data-stu-id="34532-207">Director</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34532-208">Растянутые пулы для этой роли сервера не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="34532-208">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="34532-209">При развертывании роли режиссера рекомендуется развернуть один режиссер для каждого удаленного пользователя 12 000, который будет одновременно получать доступ к сайту.</span><span class="sxs-lookup"><span data-stu-id="34532-209">If you deploy the Director server role we recommend that you deploy one Director for every 12,000 remote users who will access a site concurrently.</span></span> <span data-ttu-id="34532-210">Как минимум мы рекомендуем использовать двух директоров для обеспечения высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="34532-210">At a minimum we recommend two Directors for high availability.</span></span> <span data-ttu-id="34532-211">Эти рекомендации предполагают, что оборудование пограничных серверов соответствует рекомендациям, приведенным в разделе [аппаратные платформы сервера для Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span><span class="sxs-lookup"><span data-stu-id="34532-211">These recommendations assume that the hardware for your Edge Servers meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="34532-212">При указании количества пользователей для режиссеров Включите пользователей, которые размещаются на устройствах с бесперебойной ветвлением, и бесперебойно работающих серверах филиалов в филиалах, связанных с пулом переднего плана на этом сайте.</span><span class="sxs-lookup"><span data-stu-id="34532-212">When you account for the number of users for the Directors, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with a Front End pool at this site.</span></span>

</div>

<div>

## <a name="mediation-server"></a><span data-ttu-id="34532-213">Сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="34532-213">Mediation Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34532-214">Растянутые пулы для этой роли сервера не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="34532-214">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="34532-215">Если вы разгруппирование сервера обновлений на сервере переднего плана, сервер обработает на каждом сервере переднего плана в пуле и должен предоставить достаточную емкость для пользователей в пуле.</span><span class="sxs-lookup"><span data-stu-id="34532-215">If you collocate Mediation Server with Front End Server, Mediation Server runs on every Front End Server in the pool, and should provide enough capacity for the users in the pool.</span></span>

<span data-ttu-id="34532-216">Если вы разворачиваете пул серверов с изолированными исправлениями, то сколько серверов-посредников нужно развернуть, зависит от многих факторов, в том числе аппаратных средств, используемых для сервера-партнера, количества пользователей VoIP, количества одноранговых узлов, которые каждый из них контролирует, трафик с помощью этих шлюзов и процент звонков с носителя, минуя сервер-посредник.</span><span class="sxs-lookup"><span data-stu-id="34532-216">If you deploy a stand-alone Mediation Server pool, then how many Mediation Servers to deploy depends on many factors, including the hardware used for Mediation Server, the number of VoIP users you have, the number of gateway peers that each Mediation Server pool controls, the busy hour traffic through those gateways, and the percentage of calls with media that bypasses the Mediation Server.</span></span>

<span data-ttu-id="34532-217">В приведенных ниже таблицах приведены рекомендации о том, сколько одновременных вызовов может обрабатывать сервер-посредник, предполагая, что оборудование для серверов-исправлений соответствует требованиям в [серверных платформах для Lync server 2013](lync-server-2013-server-hardware-platforms.md) и включена технология Hyper-Threading.</span><span class="sxs-lookup"><span data-stu-id="34532-217">The following tables provide a guideline for how many concurrent calls a Mediation Server can handle, assuming that the hardware for the Mediation Servers meets the requirements in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) and that hyper-threading is enabled.</span></span> <span data-ttu-id="34532-218">Подробные сведения об масштабируемости сервера исправлений можно найти в разделе [Оценка использования голоса и трафик для Lync server 2013](lync-server-2013-estimating-voice-usage-and-traffic.md) и [рекомендации по развертыванию сервера исправлений в Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md).</span><span class="sxs-lookup"><span data-stu-id="34532-218">For details about Mediation Server scalability, see [Estimating voice usage and traffic for Lync Server 2013](lync-server-2013-estimating-voice-usage-and-traffic.md) and [Deployment guidelines for Mediation Server in Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md).</span></span>

<span data-ttu-id="34532-219">Во всех приведенных ниже таблицах предполагается использование, как обобщено в [пользовательских моделях в Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="34532-219">All the following tables assume usage as summarized in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

### <a name="stand-alone-mediation-server-capacity-70-internal-users-30-external-users-with-non-bypass-call-capacity-media-transcoding-performed-by-mediation-server"></a><span data-ttu-id="34532-220">Бесплатная емкость сервера исправлений: 70% внутренних пользователей, 30% внешних пользователей с емкостью обоснованных звонков (перекодировка мультимедиа, выполненная сервером исправлений)</span><span class="sxs-lookup"><span data-stu-id="34532-220">Stand-alone Mediation Server Capacity: 70% Internal Users, 30% External users with non-bypass call capacity (media transcoding performed by Mediation Server)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34532-221">Серверное оборудование</span><span class="sxs-lookup"><span data-stu-id="34532-221">Server hardware</span></span></th>
<th><span data-ttu-id="34532-222">Максимальное количество звонков</span><span class="sxs-lookup"><span data-stu-id="34532-222">Maximum number of calls</span></span></th>
<th><span data-ttu-id="34532-223">Максимальное количество линий T1</span><span class="sxs-lookup"><span data-stu-id="34532-223">Maximum number of T1 lines</span></span></th>
<th><span data-ttu-id="34532-224">Максимальное количество линий E1</span><span class="sxs-lookup"><span data-stu-id="34532-224">Maximum number of E1 lines</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34532-225">Два шестиядерных процессора 2,26 ГГц с поддержкой технологии Hyper-Threading (<strong>технология Hyper-Threading отключена</strong>), память 32 ГБ и одна двухпортовая сетевая карта.</span><span class="sxs-lookup"><span data-stu-id="34532-225">Dual processor, hex core, 2.26 GHz hyper-threaded CPU <strong>with hyper-threading disabled</strong>, with 32 GB memory and one dual-port network adapter card.</span></span></p></td>
<td><p><span data-ttu-id="34532-226">1100</span><span class="sxs-lookup"><span data-stu-id="34532-226">1100</span></span></p></td>
<td><p><span data-ttu-id="34532-227">46</span><span class="sxs-lookup"><span data-stu-id="34532-227">46</span></span></p></td>
<td><p><span data-ttu-id="34532-228">35</span><span class="sxs-lookup"><span data-stu-id="34532-228">35</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-229">Два шестиядерных процессора 2,26 ГГц с поддержкой технологии Hyper-Threading, память 32 ГБ и одна двухпортовая сетевая карта.</span><span class="sxs-lookup"><span data-stu-id="34532-229">Dual processor, hex core, 2.26 GHz hyper-threaded CPU, with 32 GB memory and one dual-port network adapter card.</span></span></p></td>
<td><p><span data-ttu-id="34532-230">1500</span><span class="sxs-lookup"><span data-stu-id="34532-230">1500</span></span></p></td>
<td><p><span data-ttu-id="34532-231">63</span><span class="sxs-lookup"><span data-stu-id="34532-231">63</span></span></p></td>
<td><p><span data-ttu-id="34532-232">47</span><span class="sxs-lookup"><span data-stu-id="34532-232">47</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="34532-233">Несмотря на то, что при тестировании производительности использовались серверы размером 32 ГБ, серверы с объемом памяти 16 ГБ поддерживаются для изолированного сервера-посредника и достаточно для обеспечения производительности, представленной в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="34532-233">Although servers with 32 GB of memory were used for performance testing, servers with 16 GB of memory are supported for stand-alone Mediation Server, and are sufficient to provide the performance shown in this table.</span></span>



</div>

### <a name="mediation-server-capacity-mediation-server-collocated-with-front-end-server-70-internal-users-30-external-users-non-bypass-call-capacity-media-processing-performed-by-mediation-server"></a><span data-ttu-id="34532-234">Емкость сервера ресурсов (сервер-посредник, выровненный по внешнему серверу) 70% внутренних пользователей, 30% внешних пользователей, не пропуская емкость звонка (обработка носителей, выполненная сервером-исправлением)</span><span class="sxs-lookup"><span data-stu-id="34532-234">Mediation Server Capacity (Mediation Server Collocated with Front End Server) 70% Internal Users, 30% External Users, Non-Bypass Call Capacity (Media Processing Performed by Mediation Server)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34532-235">Серверное оборудование</span><span class="sxs-lookup"><span data-stu-id="34532-235">Server hardware</span></span></th>
<th><span data-ttu-id="34532-236">Максимальное количество звонков</span><span class="sxs-lookup"><span data-stu-id="34532-236">Maximum number of calls</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34532-237">Два шестиядерных процессора 2,26 ГГц с поддержкой технологии Hyper-Threading, память 32 ГБ и две сетевых карты со скоростью 1 Гбит/с.</span><span class="sxs-lookup"><span data-stu-id="34532-237">Dual processor, hex core, 2.26 GHz hyper-threaded CPU, with 32 GB memory and 2 1GB network adapter cards.</span></span></p></td>
<td><p><span data-ttu-id="34532-238">150</span><span class="sxs-lookup"><span data-stu-id="34532-238">150</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="34532-239">Это число значительно меньше числа на сервере автономных обновлений, так как сервер переднего плана должен обрабатывать другие функции и функции для пользователей 6600, которые потребуются для голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="34532-239">This number is much smaller than the numbers for the stand-alone Mediation Server because the Front End Server has to handle other features and functions for the 6600 users homed on it, in addition to the transcoding needed for voice calls.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="34532-240">Чтобы повысить производительность сервера-посредника, необходимо включить масштабирование на стороне приема (RSS) на сетевых адаптерах серверов-исправлений.</span><span class="sxs-lookup"><span data-stu-id="34532-240">To improve the performance of the Mediation Server, you should enable receive-side scaling (RSS) on the network adapters on your Mediation Servers.</span></span> <span data-ttu-id="34532-241">RSS поддерживает параллельную обработку входящих пакетов несколькими процессорами сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-241">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="34532-242">Дополнительные сведения можно найти в разделе улучшенные возможности масштабирования на стороне приема в Windows Server 2008 <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> .</span><span class="sxs-lookup"><span data-stu-id="34532-242">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="34532-243">Сведения о том, как включить RSS, см. в документации сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="34532-243">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="back-end-server"></a><span data-ttu-id="34532-244">внутренний сервер</span><span class="sxs-lookup"><span data-stu-id="34532-244">Back End Server</span></span>

<span data-ttu-id="34532-245">В Lync Server 2013 базы данных присутствия находятся на серверах переднего плана, а не на обратном сервере.</span><span class="sxs-lookup"><span data-stu-id="34532-245">In Lync Server 2013, the presence databases are located on the Front End Servers instead of the Back End Server.</span></span> <span data-ttu-id="34532-246">Это является более простым требованием для каждого серверного сервера в Lync Server 2013 и соответствует требованиям к оборудованию для серверного переднего плана.</span><span class="sxs-lookup"><span data-stu-id="34532-246">This has resulted in a much simpler requirement for each Back End Server in Lync Server 2013, equivalent to the hardware requirement for the Front End Server.</span></span> <span data-ttu-id="34532-247">Сравните это с Lync Server 2010, где сервер должен быть на более высоком уровне сервера с 25 дисками.</span><span class="sxs-lookup"><span data-stu-id="34532-247">Contrast this to Lync Server 2010, where the Back End Server was required to be a much higher grade server with 25 disks.</span></span> <span data-ttu-id="34532-248">Тем не менее, если вы не хотите отвечать требованиям к оборудованию, описанным выше в этом разделе, и в [серверных аппаратных платформах для Lync Server 2013](lync-server-2013-server-hardware-platforms.md), вы все равно должны быть в процессе работы серверов.</span><span class="sxs-lookup"><span data-stu-id="34532-248">However, the workload of Back End Servers is still such that you should not fail to meet the hardware recommendations listed earlier in this section and in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="34532-249">Для обеспечения высокого уровня доступности серверного сервера рекомендуется развертывание зеркального отображения сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-249">To provide high availability of your Back End Server, we recommend deploying server mirroring.</span></span> <span data-ttu-id="34532-250">Дополнительные сведения можно найти в разделе о [высокой доступности сервера в Lync server 2013](lync-server-2013-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="34532-250">For more information, see [Back End Server high availability in Lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span></span>

</div>

<div>

## <a name="monitoring-and-archiving"></a><span data-ttu-id="34532-251">Мониторинг и архивирование</span><span class="sxs-lookup"><span data-stu-id="34532-251">Monitoring and Archiving</span></span>

<span data-ttu-id="34532-252">В Lync Server 2013 при развертывании мониторинга или архивации интерфейсные функции этих служб выполняются на серверах переднего плана, а не на отдельных ролях сервера.</span><span class="sxs-lookup"><span data-stu-id="34532-252">In Lync Server 2013, if you deploy Monitoring or Archiving, the front end functionality of these services runs on the Front End Servers, instead of on separate server roles.</span></span> <span data-ttu-id="34532-253">Для наблюдения и архивации по-прежнему используется собственное хранилище базы данных, отделенное от хранилища сзади.</span><span class="sxs-lookup"><span data-stu-id="34532-253">Monitoring and Archiving each still use their own database store, separate from the Back End store.</span></span> <span data-ttu-id="34532-254">Кроме того, если вы развернули Exchange 2013, вы можете хранить данные для архивации мгновенных сообщений в Exchange, а не в специальном хранилище SQL.</span><span class="sxs-lookup"><span data-stu-id="34532-254">Alternatively, if you have Exchange 2013 deployed, you can store instant message Archiving data in Exchange instead of in a dedicated SQL store.</span></span>

<span data-ttu-id="34532-255">В следующей таблице показаны приблизительные значения размера хранилища базы данных на пользователя в день, необходимые для данных мониторинга и архивирования.</span><span class="sxs-lookup"><span data-stu-id="34532-255">The following table indicates approximately how much database storage is required per user per day for Monitoring and Archiving data.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="34532-256"><strong>CDR (мониторинг)</strong></span><span class="sxs-lookup"><span data-stu-id="34532-256"><strong>CDR (Monitoring)</strong></span></span></p></td>
<td><p><span data-ttu-id="34532-257"><strong>QoE (мониторинг)</strong></span><span class="sxs-lookup"><span data-stu-id="34532-257"><strong>QoE (Monitoring)</strong></span></span></p></td>
<td><p><span data-ttu-id="34532-258"><strong>Архивирование</strong></span><span class="sxs-lookup"><span data-stu-id="34532-258"><strong>Archiving</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-259">Дисковое пространство на пользователя в день</span><span class="sxs-lookup"><span data-stu-id="34532-259">Disk space required per user per day</span></span></p></td>
<td><p><span data-ttu-id="34532-260">49 КБ</span><span class="sxs-lookup"><span data-stu-id="34532-260">49 KB</span></span></p></td>
<td><p><span data-ttu-id="34532-261">28 КБ</span><span class="sxs-lookup"><span data-stu-id="34532-261">28 KB</span></span></p></td>
<td><p><span data-ttu-id="34532-262">57 КБ</span><span class="sxs-lookup"><span data-stu-id="34532-262">57 KB</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="34532-263">Microsoft used the hardware in the following table for the database server for Monitoring and Archiving during its performance testing.</span><span class="sxs-lookup"><span data-stu-id="34532-263">Microsoft used the hardware in the following table for the database server for Monitoring and Archiving during its performance testing.</span></span> <span data-ttu-id="34532-264">Тестирование собрало данные двух пулов интерфейсов, каждый из которых содержал 80 000 пользователей.</span><span class="sxs-lookup"><span data-stu-id="34532-264">The testing collected the data of two Front End pools, each of which contained 80,000 users.</span></span>

### <a name="hardware-used-in-monitoring-and-archiving-performance-testing"></a><span data-ttu-id="34532-265">Оборудование, использованное при тестировании производительности мониторинга и архивирования</span><span class="sxs-lookup"><span data-stu-id="34532-265">Hardware Used in Monitoring and Archiving Performance Testing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34532-266">Аппаратный компонент</span><span class="sxs-lookup"><span data-stu-id="34532-266">Hardware component</span></span></th>
<th><span data-ttu-id="34532-267">Рекомендуется</span><span class="sxs-lookup"><span data-stu-id="34532-267">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34532-268">ЦП</span><span class="sxs-lookup"><span data-stu-id="34532-268">CPU</span></span></p></td>
<td><p><span data-ttu-id="34532-269">64-разрядный двухпроцессорный комплекс, шестиядерный, 26 ГГц и выше</span><span class="sxs-lookup"><span data-stu-id="34532-269">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-270">Память</span><span class="sxs-lookup"><span data-stu-id="34532-270">Memory</span></span></p></td>
<td><p><span data-ttu-id="34532-271">48 ГБ</span><span class="sxs-lookup"><span data-stu-id="34532-271">48 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34532-272">Диск</span><span class="sxs-lookup"><span data-stu-id="34532-272">Disk</span></span></p></td>
<td><p><span data-ttu-id="34532-273">25 дисков со скоростью вращения 10 000 об/мин по 300 ГБ со следующей конфигурацией</span><span class="sxs-lookup"><span data-stu-id="34532-273">25 10,000-RPM hard disk drives with 300 GB on each disk, with the following configuration</span></span></p>
<h3 id="section-3"> </h3>
<div>
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34532-274"><strong>Диск</strong></span><span class="sxs-lookup"><span data-stu-id="34532-274"><strong>Drive</strong></span></span></p></td>
<td><p><span data-ttu-id="34532-275"><strong>Конфигурация RAID</strong></span><span class="sxs-lookup"><span data-stu-id="34532-275"><strong>RAID Configuration</strong></span></span></p></td>
<td><p><span data-ttu-id="34532-276"><strong>Количество дисков</strong></span><span class="sxs-lookup"><span data-stu-id="34532-276"><strong>Number of disks</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-277">Файлы баз данных CDR, QoE и архивирования, на одном диске</span><span class="sxs-lookup"><span data-stu-id="34532-277">CDR, QoE, and Archiving database data files, on a single drive</span></span></p></td>
<td><p><span data-ttu-id="34532-278">1+0</span><span class="sxs-lookup"><span data-stu-id="34532-278">1+0</span></span></p></td>
<td><p><span data-ttu-id="34532-279">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="34532-279">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34532-280">Файл журнала базы данных CDR</span><span class="sxs-lookup"><span data-stu-id="34532-280">CDR database log file</span></span></p></td>
<td><p><span data-ttu-id="34532-281">1</span><span class="sxs-lookup"><span data-stu-id="34532-281">1</span></span></p></td>
<td><p><span data-ttu-id="34532-282">2</span><span class="sxs-lookup"><span data-stu-id="34532-282">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-283">Файл журнала базы данных QoE</span><span class="sxs-lookup"><span data-stu-id="34532-283">QoE database log file</span></span></p></td>
<td><p><span data-ttu-id="34532-284">1</span><span class="sxs-lookup"><span data-stu-id="34532-284">1</span></span></p></td>
<td><p><span data-ttu-id="34532-285">2</span><span class="sxs-lookup"><span data-stu-id="34532-285">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34532-286">Файл журнала базы данных архивирования</span><span class="sxs-lookup"><span data-stu-id="34532-286">Archiving database log file</span></span></p></td>
<td><p><span data-ttu-id="34532-287">1</span><span class="sxs-lookup"><span data-stu-id="34532-287">1</span></span></p></td>
<td><p><span data-ttu-id="34532-288">2</span><span class="sxs-lookup"><span data-stu-id="34532-288">2</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34532-289">Сеть</span><span class="sxs-lookup"><span data-stu-id="34532-289">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="34532-290">1 двухпортовый сетевой адаптер, 1 Гбит/с или выше (рекомендуется 2 Гбит/с, для этого требуется объединение через один MAC-адрес и один IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="34532-290">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="34532-291">Содержание</span><span class="sxs-lookup"><span data-stu-id="34532-291">In This Section</span></span>

  - [<span data-ttu-id="34532-292">Оценка объема использования и трафика голосовой связи для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34532-292">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="34532-293">Рекомендации по развертыванию сервера обновлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34532-293">Deployment guidelines for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-mediation-server.md)

<span data-ttu-id="34532-294"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34532-294"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

