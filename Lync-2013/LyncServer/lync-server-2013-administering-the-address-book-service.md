---
title: 'Lync Server 2013: Администрирование службы адресной книги'
description: 'Lync Server 2013: Администрирование службы адресной книги.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering the Address Book Service
ms:assetid: 801e4243-9670-4477-aa2f-88b61ecf5351
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429711(v=OCS.15)
ms:contentKeyID: 48184649
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86d549b06b5c6ac1c450edf9e7edb0b902ef9adf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440698"
---
# <a name="administering-the-address-book-service-in-lync-server-2013"></a><span data-ttu-id="50644-103">Администрирование службы адресной книги в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50644-103">Administering the Address Book Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50644-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50644-104">

<span> </span></span></span>

<span data-ttu-id="50644-105">_**Тема последнего изменения:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="50644-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="50644-106">Как часть развертывания Lync Server, Enterprise Edition или Standard Edition, служба адресной книги устанавливается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="50644-106">As a part of the deployment of Lync Server, Enterprise Edition or Standard Edition server, the Address Book Service is installed by default.</span></span> <span data-ttu-id="50644-107">База данных, используемая службой адресных книг — RTCab — создается на сервере SQL Server (для Enterprise Edition — это сервер SQL Server, размещенный на сервере Standard Edition, выровненный SQL Server).</span><span class="sxs-lookup"><span data-stu-id="50644-107">The database used by the Address Book Service – RTCab – is created on the SQL Server (for Enterprise Edition, this is the back-end SQL Server; for Standard Edition server, the collocated SQL Server).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="50644-108">Сведения об использовании команды " <STRONG>Редактирование ADSI</STRONG> " для редактирования атрибутов объектов доменных служб Active Directory смотрите в разделе <A href="https://go.microsoft.com/fwlink/?linkid=330427">Редактирование ADSI</A>.</span><span class="sxs-lookup"><span data-stu-id="50644-108">For information about using <STRONG>ADSI Edit</STRONG> to edit Active Directory Domain Services object attributes, see <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI Edit</A>.</span></span> <span data-ttu-id="50644-109">Сведения о средстве из набора ресурсов, специально предназначенном для службы адресной книги, можно найти в статьях <A href="https://go.microsoft.com/fwlink/?linkid=330429">инструменты Microsoft Lync Server 2013 Resource Kit</A>.</span><span class="sxs-lookup"><span data-stu-id="50644-109">For information about a tool in the Resource Kit specifically for the Address Book service, see <A href="https://go.microsoft.com/fwlink/?linkid=330429">Microsoft Lync Server 2013 Resource Kit Tools</A>.</span></span>



</div>

<div>

## <a name="address-book-server-phone-number-normalization"></a><span data-ttu-id="50644-110">Нормализация номера телефона сервера адресной книги</span><span class="sxs-lookup"><span data-stu-id="50644-110">Address Book Server Phone Number Normalization</span></span>

<span data-ttu-id="50644-111">Для Lync Server требуются стандартизированные телефонные номера RFC 3966/E. 164.</span><span class="sxs-lookup"><span data-stu-id="50644-111">Lync Server requires standardized RFC 3966/E.164 phone numbers.</span></span> <span data-ttu-id="50644-112">Чтобы использовать неструктурированные или неоднородные номера телефонов, сервер Lync Server использует сервер адресной книги для предварительной обработки телефонных номеров, прежде чем они будут переданы в правила нормализации.</span><span class="sxs-lookup"><span data-stu-id="50644-112">To use phone numbers that are unstructured or inconsistently formatted, Lync Server relies on the Address Book Server to preprocess phone numbers before they are handed off to the normalization rules.</span></span> <span data-ttu-id="50644-113">При использовании номера телефона из адресной книги и применения правила нормализации, клиенты, такие как Lync Phone Edition и Lync Mobile, могут использовать эти нормализованные номера.</span><span class="sxs-lookup"><span data-stu-id="50644-113">When a phone number is used from the address book and the normalization rule is applied, clients, such as Lync Phone Edition and Lync Mobile, can use these normalized numbers.</span></span>

<span data-ttu-id="50644-114">Правила нормализации, которые использовались в предыдущих версиях, могут работать неправильно без некоторых корректировок.</span><span class="sxs-lookup"><span data-stu-id="50644-114">The normalization rules that were used in previous versions may not work properly without some adjustments.</span></span> <span data-ttu-id="50644-115">Так как пробелы и необязательные знаки удаляются до правил нормализации, если выражение Regex специально ищет дефис или другой символ, который был удален, правило нормализации может завершиться сбоем.</span><span class="sxs-lookup"><span data-stu-id="50644-115">Because the white space and non-mandatory characters are removed prior to the normalization rules, if your regex expression is specifically looking for a dash or other character that was removed, your normalization rule might fail.</span></span> <span data-ttu-id="50644-116">Необходимо проанализировать правила нормализации, чтобы убедиться в том, что эти необязательные символы, а также в том случае, если правило не просматриваются, и продолжит работу в том случае, если этот знак не отображается в том месте, где оно будет считаться.</span><span class="sxs-lookup"><span data-stu-id="50644-116">You should review your normalization rules to ensure that either they are not looking for these non-mandatory characters, or that the rule can fail gracefully and continue in the event that the character is not present where the rule anticipates it will be.</span></span>

</div>

<div>

## <a name="user-replicator-and-address-book-server"></a><span data-ttu-id="50644-117">Репликатор пользователей и сервер адресной книги</span><span class="sxs-lookup"><span data-stu-id="50644-117">User Replicator and Address Book Server</span></span>

<span data-ttu-id="50644-118">Сервер адресной книги использует данные, предоставленные репликатором пользователей, для обновления первоначально используемых данных в глобальном списке адресов (GAL).</span><span class="sxs-lookup"><span data-stu-id="50644-118">The Address Book Server uses data provided by User Replicator to update the information that it initially obtains from the global address list (GAL).</span></span> <span data-ttu-id="50644-119">Репликатор пользователей записывает атрибуты доменных служб Active Directory для каждого пользователя, контакта и группы в таблицу AbUserEntry в базе данных, а сервер адресной книги синхронизирует данные пользователя из базы данных с файлами в хранилище файлов на сервере адресной книги и в базе данных адресной книги RTCab.</span><span class="sxs-lookup"><span data-stu-id="50644-119">User Replicator writes the Active Directory Domain Services attributes for each user, contact, and group into the AbUserEntry table in the database and the Address Book Server syncs the user data from the database into files in the Address Book Server file store and into the Address Book database RTCab.</span></span> <span data-ttu-id="50644-120">Схема для таблицы AbUserEntry использует два столбца: **UserGuid** и **UserData**.</span><span class="sxs-lookup"><span data-stu-id="50644-120">The schema for the AbUserEntry table uses two columns, **UserGuid** and **UserData**.</span></span> <span data-ttu-id="50644-121">**UserGuid** — это Индексный столбец, который содержит 16-БАЙТОВЫЙ идентификатор GUID объекта службы каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50644-121">**UserGuid** is the index column and contains the 16-byte GUID of the Active Directory object.</span></span> <span data-ttu-id="50644-122">**UserData** — это столбец с изображением, который содержит все ранее упомянутые атрибуты доменных служб Active Directory для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="50644-122">**UserData** is an image column which contains all of the previously mentioned Active Directory Domain Services attributes for that contact.</span></span>

<span data-ttu-id="50644-123">Репликатор пользователей определяет, какие атрибуты Active Directory нужно записать, прочитав таблицу конфигурации, расположенную в том же экземпляре SQL Server, что и в таблице AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="50644-123">User Replicator determines which Active Directory attributes to write by reading a configuration table located in the same SQL Server-based instance as the AbUserEntry table.</span></span> <span data-ttu-id="50644-124">Таблица AbAttribute включает в себя три столбца: **ID**, **Name**, **flags** и **Enable**.</span><span class="sxs-lookup"><span data-stu-id="50644-124">The AbAttribute table contains three columns, **ID**, **Name**, **Flags**, and **Enable**.</span></span> <span data-ttu-id="50644-125">Таблица будет создана при настройке базы данных.</span><span class="sxs-lookup"><span data-stu-id="50644-125">The table is created during database setup.</span></span> <span data-ttu-id="50644-126">Если таблица AbAttribute пуста, то репликатор пользователей пропускает свою логику обработки таблицы AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="50644-126">If the AbAttribute table is empty, User Replicator skips its AbUserEntry table processing logic.</span></span> <span data-ttu-id="50644-127">Атрибуты сервера адресной книги являются динамическими и извлекаются из таблицы AbAttribute, которая первоначально записывается сервером адресной книги при активации сервера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="50644-127">Address Book Server attributes are dynamic and are retrieved from the AbAttribute table, which is initially written by the Address Book Server when the Address Book Server is activated.</span></span>

<span data-ttu-id="50644-128">Активация сервера адресной книги заполняет таблицу AbAttribute значениями, указанными в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="50644-128">Address Book Server activation populates the AbAttribute table with the values shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50644-129">ID</span><span class="sxs-lookup"><span data-stu-id="50644-129">ID</span></span></th>
<th><span data-ttu-id="50644-130">Имя</span><span class="sxs-lookup"><span data-stu-id="50644-130">Name</span></span></th>
<th><span data-ttu-id="50644-131">Флажки</span><span class="sxs-lookup"><span data-stu-id="50644-131">Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50644-132">1</span><span class="sxs-lookup"><span data-stu-id="50644-132">1</span></span></p></td>
<td><p><span data-ttu-id="50644-133">givenName</span><span class="sxs-lookup"><span data-stu-id="50644-133">givenName</span></span></p></td>
<td><p><span data-ttu-id="50644-134">0x01400000</span><span class="sxs-lookup"><span data-stu-id="50644-134">0x01400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-135">2</span><span class="sxs-lookup"><span data-stu-id="50644-135">2</span></span></p></td>
<td><p><span data-ttu-id="50644-136">Серий</span><span class="sxs-lookup"><span data-stu-id="50644-136">Sn</span></span></p></td>
<td><p><span data-ttu-id="50644-137">0x02400000</span><span class="sxs-lookup"><span data-stu-id="50644-137">0x02400000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-138">3</span><span class="sxs-lookup"><span data-stu-id="50644-138">3</span></span></p></td>
<td><p><span data-ttu-id="50644-139">Водить</span><span class="sxs-lookup"><span data-stu-id="50644-139">displayName</span></span></p></td>
<td><p><span data-ttu-id="50644-140">0x03420000</span><span class="sxs-lookup"><span data-stu-id="50644-140">0x03420000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-141">4</span><span class="sxs-lookup"><span data-stu-id="50644-141">4</span></span></p></td>
<td><p><span data-ttu-id="50644-142">Название</span><span class="sxs-lookup"><span data-stu-id="50644-142">Title</span></span></p></td>
<td><p><span data-ttu-id="50644-143">0x04000000</span><span class="sxs-lookup"><span data-stu-id="50644-143">0x04000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-144">5</span><span class="sxs-lookup"><span data-stu-id="50644-144">5</span></span></p></td>
<td><p><span data-ttu-id="50644-145">Атрибута mailNickname</span><span class="sxs-lookup"><span data-stu-id="50644-145">mailNickname</span></span></p></td>
<td><p><span data-ttu-id="50644-146">0x05400000</span><span class="sxs-lookup"><span data-stu-id="50644-146">0x05400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-147">6</span><span class="sxs-lookup"><span data-stu-id="50644-147">6</span></span></p></td>
<td><p><span data-ttu-id="50644-148">Между</span><span class="sxs-lookup"><span data-stu-id="50644-148">Company</span></span></p></td>
<td><p><span data-ttu-id="50644-149">0x06000000</span><span class="sxs-lookup"><span data-stu-id="50644-149">0x06000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-150">7</span><span class="sxs-lookup"><span data-stu-id="50644-150">7</span></span></p></td>
<td><p><span data-ttu-id="50644-151">physicalDeliveryOfficeName</span><span class="sxs-lookup"><span data-stu-id="50644-151">physicalDeliveryOfficeName</span></span></p></td>
<td><p><span data-ttu-id="50644-152">0x07000000</span><span class="sxs-lookup"><span data-stu-id="50644-152">0x07000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-153">No8</span><span class="sxs-lookup"><span data-stu-id="50644-153">8</span></span></p></td>
<td><p><span data-ttu-id="50644-154">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="50644-154">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="50644-155">0x08520C00</span><span class="sxs-lookup"><span data-stu-id="50644-155">0x08520C00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-156">@</span><span class="sxs-lookup"><span data-stu-id="50644-156">9</span></span></p></td>
<td><p><span data-ttu-id="50644-157">telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="50644-157">telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="50644-158">0x09022800</span><span class="sxs-lookup"><span data-stu-id="50644-158">0x09022800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-159">5-10</span><span class="sxs-lookup"><span data-stu-id="50644-159">10</span></span></p></td>
<td><p><span data-ttu-id="50644-160">homePhone</span><span class="sxs-lookup"><span data-stu-id="50644-160">homePhone</span></span></p></td>
<td><p><span data-ttu-id="50644-161">0x0A302800</span><span class="sxs-lookup"><span data-stu-id="50644-161">0x0A302800</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-162">11</span><span class="sxs-lookup"><span data-stu-id="50644-162">11</span></span></p></td>
<td><p><span data-ttu-id="50644-163">Мобильный</span><span class="sxs-lookup"><span data-stu-id="50644-163">Mobile</span></span></p></td>
<td><p><span data-ttu-id="50644-164">0x0B622800</span><span class="sxs-lookup"><span data-stu-id="50644-164">0x0B622800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-165">12</span><span class="sxs-lookup"><span data-stu-id="50644-165">12</span></span></p></td>
<td><p><span data-ttu-id="50644-166">otherTelephone</span><span class="sxs-lookup"><span data-stu-id="50644-166">otherTelephone</span></span></p></td>
<td><p><span data-ttu-id="50644-167">0x0C302000</span><span class="sxs-lookup"><span data-stu-id="50644-167">0x0C302000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-168">рис</span><span class="sxs-lookup"><span data-stu-id="50644-168">13</span></span></p></td>
<td><p><span data-ttu-id="50644-169">ipPhone</span><span class="sxs-lookup"><span data-stu-id="50644-169">ipPhone</span></span></p></td>
<td><p><span data-ttu-id="50644-170">0x0D302000</span><span class="sxs-lookup"><span data-stu-id="50644-170">0x0D302000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-171">14</span><span class="sxs-lookup"><span data-stu-id="50644-171">14</span></span></p></td>
<td><p><span data-ttu-id="50644-172">Сообщения</span><span class="sxs-lookup"><span data-stu-id="50644-172">Mail</span></span></p></td>
<td><p><span data-ttu-id="50644-173">0x0E500000</span><span class="sxs-lookup"><span data-stu-id="50644-173">0x0E500000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-174">10-15</span><span class="sxs-lookup"><span data-stu-id="50644-174">15</span></span></p></td>
<td><p><span data-ttu-id="50644-175">groupType</span><span class="sxs-lookup"><span data-stu-id="50644-175">groupType</span></span></p></td>
<td><p><span data-ttu-id="50644-176">0x0F010800</span><span class="sxs-lookup"><span data-stu-id="50644-176">0x0F010800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-177">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="50644-177">16</span></span></p></td>
<td><p><span data-ttu-id="50644-178">Отдел</span><span class="sxs-lookup"><span data-stu-id="50644-178">Department</span></span></p></td>
<td><p><span data-ttu-id="50644-179">0x10000000</span><span class="sxs-lookup"><span data-stu-id="50644-179">0x10000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-180">18</span><span class="sxs-lookup"><span data-stu-id="50644-180">17</span></span></p></td>
<td><p><span data-ttu-id="50644-181">Описание</span><span class="sxs-lookup"><span data-stu-id="50644-181">Description</span></span></p></td>
<td><p><span data-ttu-id="50644-182">0x11000100</span><span class="sxs-lookup"><span data-stu-id="50644-182">0x11000100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-183">18</span><span class="sxs-lookup"><span data-stu-id="50644-183">18</span></span></p></td>
<td><p><span data-ttu-id="50644-184">Директор</span><span class="sxs-lookup"><span data-stu-id="50644-184">Manager</span></span></p></td>
<td><p><span data-ttu-id="50644-185">0x12040001</span><span class="sxs-lookup"><span data-stu-id="50644-185">0x12040001</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-186">19</span><span class="sxs-lookup"><span data-stu-id="50644-186">19</span></span></p></td>
<td><p><span data-ttu-id="50644-187">proxyAddress</span><span class="sxs-lookup"><span data-stu-id="50644-187">proxyAddress</span></span></p></td>
<td><p><span data-ttu-id="50644-188">0x00500105</span><span class="sxs-lookup"><span data-stu-id="50644-188">0x00500105</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-189">средняя</span><span class="sxs-lookup"><span data-stu-id="50644-189">20</span></span></p></td>
<td><p><span data-ttu-id="50644-190">msExchHideFromAddressLists</span><span class="sxs-lookup"><span data-stu-id="50644-190">msExchHideFromAddressLists</span></span></p></td>
<td><p><span data-ttu-id="50644-191">0xFF000003</span><span class="sxs-lookup"><span data-stu-id="50644-191">0xFF000003</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-192">99</span><span class="sxs-lookup"><span data-stu-id="50644-192">99</span></span></p></td>
<td><p><span data-ttu-id="50644-193">entryID</span><span class="sxs-lookup"><span data-stu-id="50644-193">entryID</span></span></p></td>
<td><p><span data-ttu-id="50644-194">0x99000000</span><span class="sxs-lookup"><span data-stu-id="50644-194">0x99000000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50644-195">Числа в столбце " **идентификатор** " должны быть уникальными и не должны использоваться повторно.</span><span class="sxs-lookup"><span data-stu-id="50644-195">The numbers in the **ID** column must be unique and should never be reused.</span></span> <span data-ttu-id="50644-196">Кроме того, при сохранении значений ИДЕНТИФИКАТОРов в разделе 256 сохраняются места в выходных файлах, написанных сервером адресной книги.</span><span class="sxs-lookup"><span data-stu-id="50644-196">Also, keeping the ID values under 256 saves space in the output files written by the Address Book Server.</span></span> <span data-ttu-id="50644-197">Однако максимальное значение идентификатора — 65535.</span><span class="sxs-lookup"><span data-stu-id="50644-197">However, the maximum ID value is 65535.</span></span> <span data-ttu-id="50644-198">Столбец **Name** соответствует имени атрибута Active Directory, которое репликатор пользователей должен добавить в таблицу AbUserEntry для каждого контакта.</span><span class="sxs-lookup"><span data-stu-id="50644-198">The **Name** column corresponds to the Active Directory attribute name that User Replicator should put in the AbUserEntry table for each contact.</span></span> <span data-ttu-id="50644-199">Значение в столбце **flags** используется для определения типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="50644-199">The value in the **Flags** column is used to define the type of attribute.</span></span> <span data-ttu-id="50644-200">Следующие типы атрибутов сервера адресной книги распознаются репликатором пользователей, обозначается младшим байтом значения в столбце **flags** .</span><span class="sxs-lookup"><span data-stu-id="50644-200">The following types of Address Book Server attributes are recognized by User Replicator, indicated by the low byte of the value in the **Flags** column.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50644-201">Атрибут</span><span class="sxs-lookup"><span data-stu-id="50644-201">Attribute</span></span></th>
<th><span data-ttu-id="50644-202">Описание</span><span class="sxs-lookup"><span data-stu-id="50644-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50644-203">0x0</span><span class="sxs-lookup"><span data-stu-id="50644-203">0x0</span></span></p></td>
<td><p><span data-ttu-id="50644-204">Строковый атрибут.</span><span class="sxs-lookup"><span data-stu-id="50644-204">A string attribute.</span></span> <span data-ttu-id="50644-205">Репликатор пользователей преобразует этот тип в кодировку UTF-8, прежде чем хранить его в таблице AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="50644-205">User Replicator converts this type to UTF-8 before storing it in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-206">0x1</span><span class="sxs-lookup"><span data-stu-id="50644-206">0x1</span></span></p></td>
<td><p><span data-ttu-id="50644-207">Двоичный атрибут.</span><span class="sxs-lookup"><span data-stu-id="50644-207">A binary attribute.</span></span> <span data-ttu-id="50644-208">Репликатор пользователей сохраняет этот объект в объекте BLOB без каких-либо преобразований.</span><span class="sxs-lookup"><span data-stu-id="50644-208">User Replicator stores this in the blob without any conversion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-209">0x2</span><span class="sxs-lookup"><span data-stu-id="50644-209">0x2</span></span></p></td>
<td><p><span data-ttu-id="50644-210">Атрибут String, который включается, только если значение атрибута начинается с &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="50644-210">A string attribute, but is included only if the attribute value begins with &quot;tel:&quot;.</span></span> <span data-ttu-id="50644-211">В основном это для многозначных строковых атрибутов, особенно <strong>proxyAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="50644-211">This is primarily for multi-valued string attributes, specifically <strong>proxyAddresses</strong>.</span></span> <span data-ttu-id="50644-212">В этом случае сервер адресной книги нужен только в записях <strong>proxyAddresses</strong> , начинающихся с &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="50644-212">In this case, Address Book Server is interested only in <strong>proxyAddresses</strong> entries that begin with &quot;tel:&quot;.</span></span> <span data-ttu-id="50644-213">Таким образом, в целях экономии места репликатор пользователей хранит только записи, которые начинаются с &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="50644-213">Therefore, in the interest of saving space, User Replicator stores only the entries that begin with &quot;tel:&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-214">0x3</span><span class="sxs-lookup"><span data-stu-id="50644-214">0x3</span></span></p></td>
<td><p><span data-ttu-id="50644-215">Логический атрибут String, который в случае ИСТИНности приводит к тому, что этот контакт не должен быть указан в таблице AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="50644-215">A Boolean string attribute, which if TRUE causes User Replicator to not include this contact in the AbUserEntry table.</span></span> <span data-ttu-id="50644-216">Если задано значение FALSE, то служба тиражирования пользователей будет включать атрибуты этого контакта в таблицу AbUserEntry, но не конкретный атрибут с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="50644-216">If FALSE, it causes User Replicator to include the attributes for this contact in the AbUserEntry table, but not the particular attribute with this flag.</span></span> <span data-ttu-id="50644-217">Это еще один особый тип случая, преимущественно для атрибута <strong>msExchHideFromAddressLists</strong> .</span><span class="sxs-lookup"><span data-stu-id="50644-217">This is another special case type that is primarily for the <strong>msExchHideFromAddressLists</strong> attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-218">0x4</span><span class="sxs-lookup"><span data-stu-id="50644-218">0x4</span></span></p></td>
<td><p><span data-ttu-id="50644-219">Атрибут String, который включается, только если значение атрибута начинается с &quot; SMTP: &quot; и содержит &quot; @ &quot; символ.</span><span class="sxs-lookup"><span data-stu-id="50644-219">A string attribute, but is included only if the attribute value begins with &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-220">0x5</span><span class="sxs-lookup"><span data-stu-id="50644-220">0x5</span></span></p></td>
<td><p><span data-ttu-id="50644-221">Атрибут String, который включается, только если значение атрибута начинается с &quot; Tel: &quot; или &quot; SMTP: &quot; и содержит &quot; @ &quot; символ.</span><span class="sxs-lookup"><span data-stu-id="50644-221">A string attribute, but is included only if the attribute value begins with either &quot;tel:&quot; or &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-222">0x100</span><span class="sxs-lookup"><span data-stu-id="50644-222">0x100</span></span></p></td>
<td><p><span data-ttu-id="50644-223">Если этот параметр установлен, это многозначный атрибут, который может отображаться для каждого контакта более одного раза.</span><span class="sxs-lookup"><span data-stu-id="50644-223">If set, this is a multi-valued attribute that can appear more than once for each contact.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-224">0x400</span><span class="sxs-lookup"><span data-stu-id="50644-224">0x400</span></span></p></td>
<td><p><span data-ttu-id="50644-225">Если этот параметр установлен, он определяет атрибут имени учетной записи пользователя электронной почты для контакта.</span><span class="sxs-lookup"><span data-stu-id="50644-225">If set, this identifies the email user account name attribute for a contact.</span></span> <span data-ttu-id="50644-226">Сервер адресной книги использует этот флаг, чтобы определить, какое значение атрибута отобразить в записи журнала событий нормализации телефона.</span><span class="sxs-lookup"><span data-stu-id="50644-226">Address Book Server uses this flag to identify which attribute value to show in the phone normalization event log entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-227">0x800</span><span class="sxs-lookup"><span data-stu-id="50644-227">0x800</span></span></p></td>
<td><p><span data-ttu-id="50644-228">Если этот параметр установлен, он определяет обязательный атрибут для контакта.</span><span class="sxs-lookup"><span data-stu-id="50644-228">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="50644-229">Адресная книга сервер включает пользователя в таблицу AbUserEntry только в том случае, если в службе каталогов Active Directory есть значение для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="50644-229">Address Book Server includes a user in the AbUserEntry table only if there is a value for this attribute in Active Directory.</span></span> <span data-ttu-id="50644-230">Если имеется несколько обязательных атрибутов, для включения пользователя в таблицу AbUserEntry требуется только один из них.</span><span class="sxs-lookup"><span data-stu-id="50644-230">If there is more than one required attribute, only one of them is required to have a value to include the user in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-231">0x1000</span><span class="sxs-lookup"><span data-stu-id="50644-231">0x1000</span></span></p></td>
<td><p><span data-ttu-id="50644-232">Если задано, сервер адресной книги всегда нормализует значение этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="50644-232">If set, Address Book Server always normalizes the value of this attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-233">0x2000</span><span class="sxs-lookup"><span data-stu-id="50644-233">0x2000</span></span></p></td>
<td><p><span data-ttu-id="50644-234">Если задано, сервер адресной книги использует нормализованное число из <strong>proxyAddresses</strong>, если параметр <strong>UseNormalizationRules</strong> CMS имеет значение ложь; в противном случае она будет выглядеть так же, как если бы бит флага 0x1000.</span><span class="sxs-lookup"><span data-stu-id="50644-234">If set, Address Book Server uses the normalized number from <strong>proxyAddresses</strong>, if the <strong>UseNormalizationRules</strong> CMS setting is FALSE; otherwise it behaves the same as when the flag bit is 0x1000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-235">0x4000</span><span class="sxs-lookup"><span data-stu-id="50644-235">0x4000</span></span></p></td>
<td><p><span data-ttu-id="50644-236">Если задано, сервер адресной книги не включает в таблицу AbUserEntry объекты, которые имеют это значение для указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="50644-236">If set, Address Book Server does not include objects in the AbUserEntry table that have this value for the specified attribute.</span></span> <span data-ttu-id="50644-237">Например, если в атрибуте <strong>msRTCSIP-PrimaryUserAddress</strong> установлен этот бит флага, то контакты с этим атрибутом не записываются в базу данных.</span><span class="sxs-lookup"><span data-stu-id="50644-237">For example, if the <strong>msRTCSIP-PrimaryUserAddress</strong> attribute has this flag bit set, then contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-238">0x8000</span><span class="sxs-lookup"><span data-stu-id="50644-238">0x8000</span></span></p></td>
<td><p><span data-ttu-id="50644-239">Если задано, сервер адресной книги не включает в таблицу AbUserEntry объекты, которые не имеют этого значения для указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="50644-239">If set, Address Book Server does not include objects in the AbUserEntry table that do not have this value for the specified attribute.</span></span> <span data-ttu-id="50644-240">Если для объекта заданы биты флага 0x4000 и 0x8000, атрибут с битовым значением флага, установленным на 0x4000, имеет приоритет, и объект исключается из таблицы AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="50644-240">If both the 0x4000 and 0x8000 flag bits are set on an object, the attribute with the flag bit value set to 0x4000 takes precedence, and the object is excluded from the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-241">0x10000</span><span class="sxs-lookup"><span data-stu-id="50644-241">0x10000</span></span></p></td>
<td><p><span data-ttu-id="50644-242">Если этот параметр установлен, это представляет объект Group.</span><span class="sxs-lookup"><span data-stu-id="50644-242">If set, this represents a group object.</span></span> <span data-ttu-id="50644-243">Репликатор пользователей использует этот бит флага, чтобы включить контакты с атрибутом <strong>groupType</strong> , чье присутствие указывает на группу (например, список рассылки или группу безопасности).</span><span class="sxs-lookup"><span data-stu-id="50644-243">User Replicator uses this flag bit to include contacts with the <strong>groupType</strong> attribute whose presence indicates a group (for example, a distribution list or security group).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-244">0x20000</span><span class="sxs-lookup"><span data-stu-id="50644-244">0x20000</span></span></p></td>
<td><p><span data-ttu-id="50644-245">Если задано, репликатор пользователей использует этот бит флага, чтобы включить этот атрибут в файлы сервера адресной книги для конкретных устройств (файлы с расширением Dabs).</span><span class="sxs-lookup"><span data-stu-id="50644-245">If set, User Replicator uses this flag bit to include this attribute in device-specific Address Book Server files (that is, files with a .dabs extension).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50644-246">В предыдущих версиях Lync Server при применении изменения к Active Directory администратору потребуется выполнить командлеты **Update-CSUserDatabase** и **Update – CSAddressBook** Windows PowerShell, чтобы сохранить изменения в базе данных пользователей Lync Server и в RTCab базу данных незамедлительно.</span><span class="sxs-lookup"><span data-stu-id="50644-246">In previous versions of Lync Server, when applying a change to Active Directory, the administrator would be required to run **Update -CSUserDatabase** and **Update –CSAddressBook** Windows PowerShell cmdlets to persist the change to the Lync Server user database and RTCab database immediately.</span></span> <span data-ttu-id="50644-247">В Lync Server 2013 служба репликатора пользователей Lync Server выберет изменения из Active Directory и обновит базу данных пользователей Lync Server на основе заданного интервала.</span><span class="sxs-lookup"><span data-stu-id="50644-247">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="50644-248">Служба репликации пользователей Lync Server также будет автоматически распространять изменения базы данных RTCab, не требуя администратора запускать Update-CSAddressBook.</span><span class="sxs-lookup"><span data-stu-id="50644-248">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="50644-249">Если включен веб-запрос на адресную книгу, изменения будут отражены в результатах поиска клиентами Lync.</span><span class="sxs-lookup"><span data-stu-id="50644-249">If Address Book Web query is enabled, then the changes will be reflected in search results by Lync clients.</span></span> <span data-ttu-id="50644-250">Администраторам потребуется выполнить Update-CSAddressBook только в том случае, если разрешена загрузка файла адресной книги.</span><span class="sxs-lookup"><span data-stu-id="50644-250">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="50644-251">По умолчанию репликатор пользователей Lync Server запускается автоматически каждые 5 минут.</span><span class="sxs-lookup"><span data-stu-id="50644-251">By default Lync Server User Replicator runs automatically every 5 minutes.</span></span> <span data-ttu-id="50644-252">Этот интервал можно настроить с помощью Set-CSUserReplicatorConfiguration-ReplicationCycleInterval &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="50644-252">You can configure this interval by using Set -CSUserReplicatorConfiguration -ReplicationCycleInterval &lt;&gt;.</span></span>



</div>

</div>

<div>

## <a name="filtering-the-address-book"></a><span data-ttu-id="50644-253">Фильтрация адресной книги</span><span class="sxs-lookup"><span data-stu-id="50644-253">Filtering the Address Book</span></span>

<span data-ttu-id="50644-254">Пользователи, заполненные в серверной адресной книге, могут управляться с учетом определенных атрибутов доменных служб Active Directory, перечисленных в таблице AbAttribute.</span><span class="sxs-lookup"><span data-stu-id="50644-254">The users populated in the Address Book Server files can be controlled based on certain Active Directory Domain Services attributes listed in the AbAttribute table.</span></span> <span data-ttu-id="50644-255">Один из таких атрибутов, используемых для фильтрации, — это атрибут **msExchangeHideFromAddressBook** .</span><span class="sxs-lookup"><span data-stu-id="50644-255">One such attribute used for filtering is the **msExchangeHideFromAddressBook** attribute.</span></span> <span data-ttu-id="50644-256">Это пользовательский атрибут, добавляемый в схему Exchange.</span><span class="sxs-lookup"><span data-stu-id="50644-256">This is a user attribute added by the Exchange schema.</span></span> <span data-ttu-id="50644-257">Если значение этого атрибута равно TRUE, сервер Exchange Server использует этот атрибут для скрытия контакта из глобального списка адресов Outlook (GAL).</span><span class="sxs-lookup"><span data-stu-id="50644-257">If the value of this attribute is TRUE, Exchange Server uses this attribute to hide the contact from the Outlook Global Address List (GAL).</span></span> <span data-ttu-id="50644-258">Аналогичным образом, если значение этого атрибута — TRUE, то репликатор пользователей не включит этого пользователя в таблицу AbUserEntry, и этот пользователь не будет находиться в файле адресной книги сервера.</span><span class="sxs-lookup"><span data-stu-id="50644-258">Similarly, if the value of this attribute is TRUE, User Replicator does not include that user in the AbUserEntry table and this user will not be in the Address Book Server files.</span></span>

<span data-ttu-id="50644-259">Вы можете использовать несколько битов флагов, чтобы определить фильтр для использования в атрибутах сервера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="50644-259">You can use some flag bits to define a filter to use on Address Book Server attributes.</span></span> <span data-ttu-id="50644-260">Например, наличие определенных битов флагов может определять атрибут как атрибут Include или атрибут Exclude.</span><span class="sxs-lookup"><span data-stu-id="50644-260">For example, the presence of certain flag bits can identify an attribute as an include attribute or an exclude attribute.</span></span> <span data-ttu-id="50644-261">Репликатор пользователей отфильтровывает контакты, которые содержат атрибут Exclude и отфильтровывает, что не содержит атрибут Include.</span><span class="sxs-lookup"><span data-stu-id="50644-261">User Replicator filters out contacts that contain an exclude attribute and filters out contains that do not contain an include attribute.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="50644-262">Дополнительные сведения о том, как отфильтровать адресную книгу, приведены <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">в разделе Командлеты сервера адресной книги в Lync Server 2013</A>и фильтрация записной <A href="https://go.microsoft.com/fwlink/?linkid=330430">книжки Lync 2013</A></span><span class="sxs-lookup"><span data-stu-id="50644-262">For more information about filtering the Address Book, see <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">Address Book Server cmdlets in Lync Server 2013</A>, and <A href="https://go.microsoft.com/fwlink/?linkid=330430">Filter Lync 2013 address book</A></span></span>



</div>

<span data-ttu-id="50644-263">В настоящее время есть три разных фильтра.</span><span class="sxs-lookup"><span data-stu-id="50644-263">Currently, there are three different filters.</span></span> <span data-ttu-id="50644-264">Эти фильтры перечислены в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="50644-264">The following table lists these filters.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50644-265">Атрибут</span><span class="sxs-lookup"><span data-stu-id="50644-265">Attribute</span></span></th>
<th><span data-ttu-id="50644-266">Описание</span><span class="sxs-lookup"><span data-stu-id="50644-266">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50644-267">0x800</span><span class="sxs-lookup"><span data-stu-id="50644-267">0x800</span></span></p></td>
<td><p><span data-ttu-id="50644-268">Если этот параметр установлен, он определяет обязательный атрибут для контакта.</span><span class="sxs-lookup"><span data-stu-id="50644-268">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="50644-269">Репликатор пользователей использует этот бит флага, чтобы отфильтровать контакты, которые не содержат хотя бы один обязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="50644-269">User Replicator uses this flag bit to filter out contacts that do not contain at least one required attribute.</span></span> <span data-ttu-id="50644-270">OuPathId — обязательный атрибут, который всегда задается.</span><span class="sxs-lookup"><span data-stu-id="50644-270">The OuPathId is a required attribute, which is always set.</span></span> <span data-ttu-id="50644-271">По крайней мере один из других обязательных атрибутов должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="50644-271">So at least one of other required attributes should be set.</span></span> <span data-ttu-id="50644-272">В противном случае контакт (то есть со значением требуемого атрибута OuPathId) по-прежнему не будет записываться в базу данных.</span><span class="sxs-lookup"><span data-stu-id="50644-272">Otherwise, contact (that is, with value of required attribute OuPathId) will still not be written to database.</span></span> <span data-ttu-id="50644-273">Например, если в качестве обязательных атрибутов определены <strong>telephoneNumber</strong> и <strong>homePhone</strong> , в базу данных записываются только те контакты, которые имеют по крайней мере один из этих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="50644-273">For example, if <strong>telephoneNumber</strong> and <strong>homePhone</strong> are defined as required attributes, only the contacts that have at least one of these attributes are written to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50644-274">0x4000</span><span class="sxs-lookup"><span data-stu-id="50644-274">0x4000</span></span></p></td>
<td><p><span data-ttu-id="50644-275">Если этот параметр установлен, он определяет атрибут Exclude.</span><span class="sxs-lookup"><span data-stu-id="50644-275">If set, this identifies an exclude attribute.</span></span> <span data-ttu-id="50644-276">Репликатор пользователей использует этот бит флага, чтобы отфильтровать контакты, которые содержат этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="50644-276">User Replicator uses this flag bit to filter out contacts that contain this attribute.</span></span> <span data-ttu-id="50644-277">Например, если <strong>msRTCSIP-PrimaryUserAddress</strong> определен как атрибут Exclude, контакты, имеющие этот атрибут, не записываются в базу данных.</span><span class="sxs-lookup"><span data-stu-id="50644-277">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an exclude attribute, contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50644-278">0x8000</span><span class="sxs-lookup"><span data-stu-id="50644-278">0x8000</span></span></p></td>
<td><p><span data-ttu-id="50644-279">Если этот параметр установлен, он определяет атрибут Include.</span><span class="sxs-lookup"><span data-stu-id="50644-279">If set, this identifies an include attribute.</span></span> <span data-ttu-id="50644-280">Репликатор пользователей использует этот бит флага, чтобы отфильтровать контакты, не содержащие этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="50644-280">User Replicator uses this flag bit to filter out contacts that do not contain this attribute.</span></span> <span data-ttu-id="50644-281">Например, если <strong>msRTCSIP-PrimaryUserAddress</strong> определен как атрибут Include, в базу данных записываются только те контакты, у которых есть этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="50644-281">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an include attribute, only the contacts that have this attribute are written to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="50644-282">Если заданы биты флагов 0x4000 (исключить атрибут) и 0x8000 (include Attribute), бит 0x4000 переопределяет 0x8000 бит и контакт исключен.</span><span class="sxs-lookup"><span data-stu-id="50644-282">If both the 0x4000 (exclude attribute) and 0x8000 (include attribute) flag bits are set, the 0x4000 bit overrides the 0x8000 bit and the contact is excluded.</span></span>



</div>

<span data-ttu-id="50644-283">Несмотря на то, что вы можете отфильтровать адресную книгу таким образом, чтобы она включала только некоторых пользователей, ограничение записей не ограничивает возможности других пользователей для связи с отфильтрованными пользователями или для просмотра состояния присутствия.</span><span class="sxs-lookup"><span data-stu-id="50644-283">Although you can filter the Address Book to include only certain users, limiting entries does not limit other users' ability to contact the filtered users or to see their presence status.</span></span> <span data-ttu-id="50644-284">Пользователи могут находить и отправлять мгновенные сообщения вручную, а также вручную инициировать звонки пользователям, которые не входят в адресную книгу, вводя полное доменное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="50644-284">Users can always find, manually send instant messages, or manually initiate calls to users not in the Address Book by entering a user's complete sign-in name.</span></span> <span data-ttu-id="50644-285">Кроме того, контактные данные пользователя также можно найти в Outlook.</span><span class="sxs-lookup"><span data-stu-id="50644-285">Also, contact information for a user could also be found in Outlook.</span></span>

<span data-ttu-id="50644-286">Несмотря на то, что в файлах адресной книги есть полные записи контактов, вы можете использовать Lync Server для инициирования электронной почты, телефона или корпоративной голосовой связи (то есть если на сервере включена поддержка корпоративной голосовой связи), поэтому в некоторых организациях предпочтительнее включать в записную книжку только пользователей, поддерживающих SIP.</span><span class="sxs-lookup"><span data-stu-id="50644-286">While having full contact records in the Address Book files enables you to use Lync Server to initiate email, telephone, or Enterprise Voice calls (that is, if Enterprise Voice is enabled on the server) with users that are not configured for Session Initiation Protocol (SIP), some organizations prefer to include only SIP-enabled users in their Address Book Server entries.</span></span> <span data-ttu-id="50644-287">Вы можете отфильтровать адресную книгу, чтобы включить только пользователей с поддержкой SIP, сняв флажок 0x800 в столбце **flags** следующих обязательных атрибутов: **mailNickname**, **telephoneNumber**, **homePhone** и **Mobile**.</span><span class="sxs-lookup"><span data-stu-id="50644-287">You can filter the Address Book to include only SIP-enabled users by clearing the 0x800 bit in the **Flags** column of the following required attributes: **mailNickname**, **telephoneNumber**, **homePhone**, and **mobile**.</span></span> <span data-ttu-id="50644-288">Вы также можете отфильтровать адресную книгу, чтобы включить только пользователей с поддержкой SIP, задав значение 0x8000 (include) в столбце **flags** (атрибут **msRTCSIP-PrimaryUserAddress** ).</span><span class="sxs-lookup"><span data-stu-id="50644-288">You can also filter the Address Book to include only SIP-enabled users by setting the 0x8000 (include attribute) in the **Flags** column of the **msRTCSIP-PrimaryUserAddress** attribute.</span></span> <span data-ttu-id="50644-289">Это также помогает исключить учетные записи служб из файлов из адресной книги.</span><span class="sxs-lookup"><span data-stu-id="50644-289">This also helps to exclude service accounts from the Address Book files.</span></span>

<span data-ttu-id="50644-290">После того как вы измените таблицу AbAttribute, вы можете обновить данные в таблице AbUserEntry, выполнив команду командлет **Update-CsUserDatabase** .</span><span class="sxs-lookup"><span data-stu-id="50644-290">After you modify the AbAttribute table, you can refresh the data in the AbUserEntry table by running the cmdlet **Update-CsUserDatabase** command.</span></span> <span data-ttu-id="50644-291">После завершения репликации UR вы можете обновить файл в хранилище файлов на сервере адресной книги, вручную запустив команду командлета **UpdateCsAddressBook** .</span><span class="sxs-lookup"><span data-stu-id="50644-291">After UR replication completes, you can update the file in the Address Book Server file store by manually running the cmdlet **UpdateCsAddressBook** command.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="50644-292">Сервер переднего плана, на котором размещен сервер адресной книги, не является административно настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="50644-292">The Front End Server that the Address Book Server is placed is not administratively configurable.</span></span> <span data-ttu-id="50644-293">Он выбирается во время развертывания — обычно это первый сервер переднего плана, на котором развернута.</span><span class="sxs-lookup"><span data-stu-id="50644-293">One is chosen during deployment—typically, the first Front End Server deployed.</span></span> <span data-ttu-id="50644-294">В случае сбоя служба адресной книги будет переведена на другой сервер переднего плана и не потребует вмешательства администратора.</span><span class="sxs-lookup"><span data-stu-id="50644-294">In the event of failure, the Address Book Service will move to another Front End Server, and requires no administrative attention.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="50644-295">Если ваша инфраструктура уже объединена или изменена в среде с несколькими лесами или родительским и дочерним развертыванием (например, консолидация инфраструктуры перед переходом на Lync Server), возможно, вы обнаружите, что для некоторых пользователей Служба «адресная книга» и веб-запрос адресной книги не будут работать.</span><span class="sxs-lookup"><span data-stu-id="50644-295">If you have consolidated or otherwise modified your infrastructure from a multi-forest deployment or a parent/child deployment (such as consolidating your infrastructure before moving to Lync Server), you may find that the Address Book service download and the Address Book Web Query fails for some users.</span></span> <span data-ttu-id="50644-296">Если в развертывании используется несколько доменов или лесов, атрибут <STRONG>MsRTCSIP-OriginatorSid</STRONG> заполняется для объектов пользователей, которые представляют собой неполадку.</span><span class="sxs-lookup"><span data-stu-id="50644-296">When in a deployment that had multiple domains or forests, the attribute <STRONG>MsRTCSIP-OriginatorSid</STRONG> is populated on the user objects that are exhibiting the issue.</span></span> <span data-ttu-id="50644-297">Для устранения этой проблемы атрибут <STRONG>MsRTCSIP-OriginatorSid</STRONG> должен иметь значение NULL для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="50644-297">The <STRONG>MsRTCSIP-OriginatorSid</STRONG> attribute must be set to NULL on these objects to resolve the issue.</span></span>



<span data-ttu-id="50644-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50644-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

