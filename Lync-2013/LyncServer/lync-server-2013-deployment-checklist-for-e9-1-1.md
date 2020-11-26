---
title: 'Lync Server 2013: контрольный список развертывания для E9-1-1'
description: 'Lync Server 2013: контрольный список развертывания для E9-1-1.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for E9-1-1
ms:assetid: cc6a656a-6043-4b9b-85c2-5708b9bb1c06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398864(v=OCS.15)
ms:contentKeyID: 48185655
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0c93762e2acef5e065249ced17bfa0eab2f159e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429715"
---
# <a name="deployment-checklist-for-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="6c811-103">Контрольный список развертывания для E9-1-1 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c811-103">Deployment checklist for E9-1-1 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c811-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c811-104">

<span> </span></span></span>

<span data-ttu-id="6c811-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="6c811-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="6c811-106">Чтобы эффективно спланировать Улучшенный 9-1-1 (E9-1-1), включите следующие требования к развертыванию:</span><span class="sxs-lookup"><span data-stu-id="6c811-106">To plan effectively for Enhanced 9-1-1 (E9-1-1), be sure to include the following deployment requirements:</span></span>

  - <span data-ttu-id="6c811-107">Необходимые условия для развертывания E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="6c811-107">Prerequisites for deploying E9-1-1.</span></span>

  - <span data-ttu-id="6c811-108">Шаги, необходимые для развертывания E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="6c811-108">Steps that are required to deploy E9-1-1.</span></span>

<div>

## <a name="deployment-prerequisites-for-e9-1-1"></a><span data-ttu-id="6c811-109">Необходимые компоненты для развертывания E9-1-1</span><span class="sxs-lookup"><span data-stu-id="6c811-109">Deployment Prerequisites for E9-1-1</span></span>

<span data-ttu-id="6c811-110">Прежде чем развертывать E9-1-1, вы должны уже разворачивать внутренние серверы Lync Server, в том числе централизованное хранилище управления, пул переднего плана или сервер стандартных выпусков, один или несколько серверов или пулов серверов-исправлений, а также клиенты Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6c811-110">Before you deploy E9-1-1, you must already have deployed your Lync Server internal servers, including a Central Management store, a Front End pool or a Standard Edition server, one or more Mediation Servers or Mediation Server pools, and Lync Server clients.</span></span> <span data-ttu-id="6c811-111">In addition, an E9-1-1 deployment requires a SIP trunk to a qualified E9-1-1 service provider or an Emergency Location Identification Number (ELIN) gateway to your public switched telephone network (PSTN).</span><span class="sxs-lookup"><span data-stu-id="6c811-111">In addition, an E9-1-1 deployment requires a SIP trunk to a qualified E9-1-1 service provider or an Emergency Location Identification Number (ELIN) gateway to your public switched telephone network (PSTN).</span></span> <span data-ttu-id="6c811-112">Lync Server поддерживает использование поставщиков услуг E9-1-1 только в США.</span><span class="sxs-lookup"><span data-stu-id="6c811-112">Lync Server supports using E9-1-1 service providers only inside the United States.</span></span>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="6c811-113">Процесс развертывания</span><span class="sxs-lookup"><span data-stu-id="6c811-113">Deployment Process</span></span>

<span data-ttu-id="6c811-114">В следующей таблице представлен обзор процесса развертывания E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="6c811-114">The following table provides an overview of the E9-1-1 deployment process.</span></span> <span data-ttu-id="6c811-115">Дополнительные сведения о действиях по развертыванию можно найти в статье [Настройка улучшенных 9-1-1 в Lync Server 2013](lync-server-2013-configure-enhanced-9-1-1.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="6c811-115">For details about deployment steps, see [Configure Enhanced 9-1-1 in Lync Server 2013](lync-server-2013-configure-enhanced-9-1-1.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c811-116">Этап</span><span class="sxs-lookup"><span data-stu-id="6c811-116">Phase</span></span></th>
<th><span data-ttu-id="6c811-117">Шаги</span><span class="sxs-lookup"><span data-stu-id="6c811-117">Steps</span></span></th>
<th><span data-ttu-id="6c811-118">Роли</span><span class="sxs-lookup"><span data-stu-id="6c811-118">Roles</span></span></th>
<th><span data-ttu-id="6c811-119">Документация по развертыванию</span><span class="sxs-lookup"><span data-stu-id="6c811-119">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c811-120">Настройка использования, маршрутов и конфигурации магистрали для голосовой связи</span><span class="sxs-lookup"><span data-stu-id="6c811-120">Configure voice usages, routes, and trunk configurations</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="6c811-p103">Создайте новую запись об использовании ТСОП. Ее имя совпадает с именем, которое используется для параметра <strong>Использование ТСОП</strong> в политике расположения.</span><span class="sxs-lookup"><span data-stu-id="6c811-p103">Create a new PSTN usage record. This is the same name that is used for the <strong>PSTN Usage</strong> setting in the location policy.</span></span></p></li>
<li><p><span data-ttu-id="6c811-123">Создайте или назначьте голосовой маршрут в записи использования ТСОП, созданную на предыдущем шаге, а затем укажите в атрибуте шлюза SIP-магистраль E9-1-1 или шлюз ELIN. </span><span class="sxs-lookup"><span data-stu-id="6c811-123">Create or assign a voice route to the PSTN usage record created in the previous step and then point the gateway attribute to the E9-1-1 SIP trunk or ELIN gateway.</span></span></p></li>
<li><p><span data-ttu-id="6c811-124">Для поставщика услуг E9-1-1 магистрали SIP установите магистраль, которая будет обрабатывать вызовы E9-1-1 в SIP для передачи данных PIDF-LO, используя командлет <strong>Set-CsTrunkConfiguration –EnablePIDFLOSupport</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c811-124">For a SIP trunk E9-1-1 service provider, set the trunk that will be handling E9-1-1 calls over the SIP to pass PIDF-LO data by using the <strong>Set-CsTrunkConfiguration –EnablePIDFLOSupport</strong> cmdlet.</span></span></p></li>
<li><p><span data-ttu-id="6c811-p104">При необходимости для поставщика услуг E9-1-1 SIP-магистрали создайте или назначьте локальный маршрут PSTN для вызовов, которые не обрабатываются SIP-магистралью поставщика услуг E9-1-1. Этот маршрут будет использоваться, если связь с поставщиком услуг E9-1-1 недоступна. Если это поддерживается поставщиком услуг E9-1-1, назначьте правило конфигурации магистрали шлюзу, который преобразует строку набора 911 в номер DID национальной или региональной экстренной службы (ECRC).</span><span class="sxs-lookup"><span data-stu-id="6c811-p104">Optionally, for a SIP trunk E9-1-1 service provider, create or assign a local PSTN route for calls that are not handled by the E9-1-1 service provider’s SIP trunk. This route will be used if the connection to the E9-1-1 service provider is not available. If supported by your E9-1-1 service provider, assign a trunk configuration rule to the gateway that translates the 911 dial string into the direct inward dialing (DID) number of the national/regional Emergency Call Response Center (ECRC).</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="6c811-128">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="6c811-128">CSVoiceAdmin</span></span></p></td>
<td><p><span data-ttu-id="6c811-129"><a href="lync-server-2013-configure-an-e9-1-1-voice-route.md">Настройка маршрута голосовой связи E9-1-1 в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6c811-129"><a href="lync-server-2013-configure-an-e9-1-1-voice-route.md">Configure an E9-1-1 voice route in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c811-130">Создайте политики местоположения и назначьте их пользователям и подсетям</span><span class="sxs-lookup"><span data-stu-id="6c811-130">Create location policies and assign them to users and subnets</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="6c811-131">Изучите глобальную политику расположения.</span><span class="sxs-lookup"><span data-stu-id="6c811-131">Review the global location policy.</span></span></p></li>
<li><p><span data-ttu-id="6c811-132">Создайте политику расположения в области на уровне пользователя; или, если в организации несколько узлов с различными способами использования экстренных вызовов, создайте политику расположения в области на уровне сети.</span><span class="sxs-lookup"><span data-stu-id="6c811-132">Create a location policy with a user-level scope; or, if the organization has more than one site with different emergency usages, create a location policy with a network-level scope.</span></span></p></li>
<li><p><span data-ttu-id="6c811-133">Назначьте политику расположения сетевым узлам.</span><span class="sxs-lookup"><span data-stu-id="6c811-133">Assign the location policy to network sites.</span></span></p></li>
<li><p><span data-ttu-id="6c811-134">Добавьте соответствующие подсети к сетевому узлу.</span><span class="sxs-lookup"><span data-stu-id="6c811-134">Add the appropriate subnets to the network site.</span></span></p></li>
<li><p><span data-ttu-id="6c811-135">(Необязательно) Назначьте политику расположения политикам пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c811-135">(Optional) Assign the location policy to user policies.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="6c811-136">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="6c811-136">CSVoiceAdmin</span></span></p>
<p><span data-ttu-id="6c811-137">CSLocationAdmin (кроме создания политик расположения)</span><span class="sxs-lookup"><span data-stu-id="6c811-137">CSLocationAdmin (except for creating Location Policies)</span></span></p></td>
<td><p><span data-ttu-id="6c811-138"><a href="lync-server-2013-create-location-policies.md">Создание политик местоположений в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6c811-138"><a href="lync-server-2013-create-location-policies.md">Create location policies in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="6c811-139"><a href="lync-server-2013-add-a-location-policy-to-a-network-site.md">Добавление политики расположения на сайт сети в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6c811-139"><a href="lync-server-2013-add-a-location-policy-to-a-network-site.md">Add a location policy to a network site in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="6c811-140"><a href="lync-server-2013-associate-subnets-with-network-sites-for-e9-1-1.md">Связывание подсетей с сетевыми сайтами для E9-1-1 в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6c811-140"><a href="lync-server-2013-associate-subnets-with-network-sites-for-e9-1-1.md">Associate subnets with network sites for E9-1-1 in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c811-141">Настройка базы данных местоположений</span><span class="sxs-lookup"><span data-stu-id="6c811-141">Configure the location database</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="6c811-142">Заполните базу данных с сопоставлением сетевых элементов местоположениям.</span><span class="sxs-lookup"><span data-stu-id="6c811-142">Populate the database with a mapping of network elements to locations.</span></span></p></li>
<li><p><span data-ttu-id="6c811-143">Для шлюзов ELIN добавьте ELINs в &lt; &gt; столбец CompanyName.</span><span class="sxs-lookup"><span data-stu-id="6c811-143">For ELIN gateways, add the ELINs to the &lt;CompanyName&gt; column.</span></span></p></li>
<li><p><span data-ttu-id="6c811-144">Настройте подключение к поставщику услуг E9-1-1 для проверки адресов.</span><span class="sxs-lookup"><span data-stu-id="6c811-144">Configure the connection to the E9-1-1 service provider for validating addresses.</span></span></p></li>
<li><p><span data-ttu-id="6c811-145">Сверьте адреса у поставщика услуг E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="6c811-145">Validate the addresses with the E9-1-1 service provider.</span></span></p></li>
<li><p><span data-ttu-id="6c811-146">Опубликуйте обновленную базу данных.</span><span class="sxs-lookup"><span data-stu-id="6c811-146">Publish the updated database.</span></span></p></li>
<li><p><span data-ttu-id="6c811-147">Для шлюзов ELIN загрузите ELIN в базу данных ALI вашего поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="6c811-147">For ELIN gateways, upload the ELINs to your PSTN carrier's Automatic Location Identification (ALI) database.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="6c811-148">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="6c811-148">CSVoiceAdmin</span></span></p>
<p><span data-ttu-id="6c811-149">CSLocationAdmin</span><span class="sxs-lookup"><span data-stu-id="6c811-149">CSLocationAdmin</span></span></p></td>
<td><p><span data-ttu-id="6c811-150"><a href="lync-server-2013-configure-the-location-database.md">Configure the location database in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6c811-150"><a href="lync-server-2013-configure-the-location-database.md">Configure the location database in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c811-151">(Необязательно) Настройка дополнительных функций</span><span class="sxs-lookup"><span data-stu-id="6c811-151">Configure Advanced Features (optional)</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="6c811-152">Настройте URL-адрес для приложения SNMP.</span><span class="sxs-lookup"><span data-stu-id="6c811-152">Configure the URL for the SNMP application.</span></span></p></li>
<li><p><span data-ttu-id="6c811-153">Настройте URL-адрес расположения дополнительной службы сведений о расположении.</span><span class="sxs-lookup"><span data-stu-id="6c811-153">Configure the URL for the location of the Secondary Location Information service.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="6c811-154">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="6c811-154">CSVoiceAdmin</span></span></p></td>
<td><p><span data-ttu-id="6c811-155"><a href="lync-server-2013-configure-an-snmp-application.md">Настройка приложения SNMP в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6c811-155"><a href="lync-server-2013-configure-an-snmp-application.md">Configure an SNMP application in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="6c811-156"><a href="lync-server-2013-configure-a-secondary-location-information-service.md">Настройка дополнительной службы сведений о расположении в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6c811-156"><a href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6c811-157">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c811-157">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

