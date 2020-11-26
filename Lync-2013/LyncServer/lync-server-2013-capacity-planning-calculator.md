---
title: Калькулятор планирования производительности Lync Server 2013
description: Калькулятор для Lync Server 2013 с планированием пропускной способности.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Lync Server 2013 capacity planning calculator
ms:assetid: e86c1f05-1393-408a-9549-6001572ec50d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362852(v=OCS.15)
ms:contentKeyID: 56280894
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9f78019c98cf280f38249ac52cd063cede5319af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435581"
---
# <a name="using-the-capacity-planning-calculator-for-lync-server-2013"></a><span data-ttu-id="00666-103">Использование калькулятора планирования производственных мощностей для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00666-103">Using the capacity planning calculator for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00666-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00666-104">

<span> </span></span></span>

<span data-ttu-id="00666-105">_**Тема последнего изменения:** 2013-11-21_</span><span class="sxs-lookup"><span data-stu-id="00666-105">_**Topic Last Modified:** 2013-11-21_</span></span>

<span data-ttu-id="00666-106">Microsoft® Lync™ Server 2013 replannings можно загрузить по адресу <https://www.microsoft.com/download/details.aspx?id=36828> .</span><span class="sxs-lookup"><span data-stu-id="00666-106">The Microsoft® Lync™ Server 2013 capacity planning calculator is available for download at <https://www.microsoft.com/download/details.aspx?id=36828>.</span></span> <span data-ttu-id="00666-107">Она предназначена для того, чтобы помочь вам определять требования к серверу на основе количества пользователей и модальностей связи, которые включены в вашу организацию.</span><span class="sxs-lookup"><span data-stu-id="00666-107">It is designed to assist you in determining server requirements based on numbers of users and communication modalities that are enabled at your organization.</span></span> <span data-ttu-id="00666-108">Вы вводите профиль своей организации, и калькулятор предоставляет рекомендации, которые помогут вам спланировать топологию.</span><span class="sxs-lookup"><span data-stu-id="00666-108">You enter your organization’s profile, and the calculator provides recommendations that help you plan your topology.</span></span>

<span data-ttu-id="00666-109">Рекомендации, создаваемые калькулятором, предназначены только для целей планирования.</span><span class="sxs-lookup"><span data-stu-id="00666-109">The recommendations created by the calculator are for planning purposes only.</span></span> <span data-ttu-id="00666-110">Для обеспечения адекватной подготовки Lync Server 2013 требуется Эмуляция нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00666-110">Actual load simulation is required to ensure that Lync Server 2013 is adequately provisioned.</span></span> <span data-ttu-id="00666-111">Для выполнения стресс-тестирования в моделируемой загрузке используйте [средство Lync Server 2013 и производительность](https://go.microsoft.com/fwlink/?linkid=282724).</span><span class="sxs-lookup"><span data-stu-id="00666-111">To perform stress testing under a simulated load, use the [Lync Server 2013 Stress and Performance Tool](https://go.microsoft.com/fwlink/?linkid=282724).</span></span>

<span data-ttu-id="00666-112">После определения профиля пользователя и модальностей, который вы хотите включить для пользователей, можно использовать калькулятор для планирования количества серверов, памяти и пропускной способности, которые вам понадобятся.</span><span class="sxs-lookup"><span data-stu-id="00666-112">After you have determined your user profile and the modalities that you want to enable for your users, it is time to use the calculator to plan the number of servers, memory, and bandwidth that you need.</span></span> <span data-ttu-id="00666-113">Для этой версии калькулятора не предусмотрены инструкции относительно требований диска касательно ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="00666-113">This version of the calculator does not provide guidance for disk I/O requirements.</span></span>

<span data-ttu-id="00666-114">Этот калькулятор дополняет [Microsoft Lync Server](https://go.microsoft.com/fwlink/?linkid=282725) и [Microsoft Lync Server](lync-server-2013-planning.md).</span><span class="sxs-lookup"><span data-stu-id="00666-114">This calculator complements the [Microsoft Lync Server](https://go.microsoft.com/fwlink/?linkid=282725) and [Microsoft Lync Server](lync-server-2013-planning.md).</span></span> <span data-ttu-id="00666-115">Чтобы использовать калькулятор, сначала ознакомьтесь с руководством и создайте рекомендованную топологию с помощью средства планирования.</span><span class="sxs-lookup"><span data-stu-id="00666-115">Use the calculator after you have reviewed the guide and created a recommended topology by using the Planning Tool.</span></span>

<span data-ttu-id="00666-p105">Воспользоваться всеми преимуществами калькулятора можно, если вы владеете точной и подробной информацией о конкретном профиле пользователя. Например, процент пользователей голосовых служб, среднее число вызовов пользователя в час, продолжительность вызова, а также процент одновременно подключенных пользователей в конференции могут оказать существенное влияние на требования к серверу. Точность рекомендаций, которые дает калькулятор, зависит от точности предоставляемых сведений.</span><span class="sxs-lookup"><span data-stu-id="00666-p105">You can benefit most from the calculator if you have accurate, detailed information about your specific user profile. For example, the percentage of voice-enabled users, average calls per user per hour, call duration, and the percentage of concurrent users in conferences can make a huge difference in server requirements. The accuracy of the recommendations created by the calculator depends on the accuracy of the information that you provide.</span></span>

<div>

## <a name="using-the-capacity-calculator"></a><span data-ttu-id="00666-119">Использование калькулятора мощности</span><span class="sxs-lookup"><span data-stu-id="00666-119">Using the Capacity Calculator</span></span>

<span data-ttu-id="00666-120">Калькулятор — это электронная таблица Microsoft Excel®.</span><span class="sxs-lookup"><span data-stu-id="00666-120">The calculator is a Microsoft Excel® spreadsheet.</span></span> <span data-ttu-id="00666-121">Оранжевые цветные ячейки предназначены для ввода данных от вас.</span><span class="sxs-lookup"><span data-stu-id="00666-121">Orange-colored cells are for input from you.</span></span> <span data-ttu-id="00666-122">Значения по умолчанию вводятся (пользователи 80 000 в одном пуле с двенадцать интерфейсных серверов), но вы можете изменить эти значения в соответствии с потребностями Организации.</span><span class="sxs-lookup"><span data-stu-id="00666-122">Default values are entered (80,000 users in one pool with twelve Front End Servers), but you can change these values according to your organization’s needs.</span></span>

<span data-ttu-id="00666-123">Модель использования состоит из следующих разделов.</span><span class="sxs-lookup"><span data-stu-id="00666-123">The usage model contains the following sections.</span></span> <span data-ttu-id="00666-124">Чтобы вычислить требования к емкости, введите данные, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="00666-124">To calculate your capacity requirements, enter data as described:</span></span>

<span data-ttu-id="00666-125">**Обмен мгновенными сообщениями и оповещение о присутствии**</span><span class="sxs-lookup"><span data-stu-id="00666-125">**Instant Messaging and Presence**</span></span>

  - <span data-ttu-id="00666-126">В разделе количество пользователей введите количество пользователей, которые будут одновременно вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="00666-126">Under Number of Users, type the number of users who will be concurrently signed in.</span></span> <span data-ttu-id="00666-127">Это число обычно составляет 80% от общего количества пользователей.</span><span class="sxs-lookup"><span data-stu-id="00666-127">This number is typically 80% of the total number of provisioned users.</span></span> <span data-ttu-id="00666-128">В большинстве случаев для обмена мгновенными сообщениями и присутствия можно включить 100% пользователей одновременно.</span><span class="sxs-lookup"><span data-stu-id="00666-128">In most situations, 100% of your concurrent users will be enabled for IM and Presence.</span></span> <span data-ttu-id="00666-129">Значение по умолчанию равно 80 000 пользователей.</span><span class="sxs-lookup"><span data-stu-id="00666-129">The default is 80,000.</span></span>

  - <span data-ttu-id="00666-130">Среднее количество контактов в списке контактов обозначает число контактов, которые используются для проверки требований к системе.</span><span class="sxs-lookup"><span data-stu-id="00666-130">Average number of contacts in Contact list indicates the number of contacts that we are using to validate your system requirements.</span></span> <span data-ttu-id="00666-131">Этот номер не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="00666-131">This number is not changeable.</span></span>

<span data-ttu-id="00666-132">**Корпоративная голосовая связь**</span><span class="sxs-lookup"><span data-stu-id="00666-132">**Enterprise Voice**</span></span>

  - <span data-ttu-id="00666-133">В разделе Пользователи, для которых включена Корпоративная голосовая связь, введите процентные значения пользователей, для которых разрешена Корпоративная голосовая связь.</span><span class="sxs-lookup"><span data-stu-id="00666-133">In Users enabled for Enterprise Voice, type the percentage of your users who are enabled for Enterprise Voice.</span></span> <span data-ttu-id="00666-134">Значение по умолчанию равно 60%</span><span class="sxs-lookup"><span data-stu-id="00666-134">The default is 60%.</span></span>

  - <span data-ttu-id="00666-135">В среднем число вызовов на одного пользователя за час (пик) введите количество вызовов в час, в течение которых будет выполняться среднее время, в течение которого пользователь будет принимать участие в течение пиковой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00666-135">In Average number of calls per user per hour (peak), type the number of calls per hour that you expect the average user to participate in during times of peak load.</span></span> <span data-ttu-id="00666-136">Значение по умолчанию равно 4.</span><span class="sxs-lookup"><span data-stu-id="00666-136">The default is 4.</span></span>

  - <span data-ttu-id="00666-137">В процентах между вызовами, использующих функцию мультимедиа, введите процент звонков, размещенных пользователями, которые будут обходить сервер по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="00666-137">In Percentage of calls that use media bypass, type the percentage of calls placed by your users that will bypass the Mediation Server.</span></span> <span data-ttu-id="00666-138">Значение по умолчанию — 65%.</span><span class="sxs-lookup"><span data-stu-id="00666-138">The default is 65%.</span></span>

  - <span data-ttu-id="00666-139">Для показателя Процент пользователей голосовых служб, которые участвуют в звонках из объединенных коммуникаций в ТСОП укажите процент звонков организации, на который приходятся телефонные вызовы "объединенные коммуникации – ТСОП".</span><span class="sxs-lookup"><span data-stu-id="00666-139">In Percentage of voice users involved in UC-PSTN calls, type the percentage of your organization’s calls which are UC-PSTN phone calls.</span></span> <span data-ttu-id="00666-140">Значение по умолчанию — 60%</span><span class="sxs-lookup"><span data-stu-id="00666-140">The default is 60%</span></span>

  - <span data-ttu-id="00666-141">В процентах от голосовых пользователей, участвующих в Объединенных звонках UC, показывает процент пользователей, для которых разрешено Корпоративная голосовая связь, и они будут включены только для звонков UC-UC.</span><span class="sxs-lookup"><span data-stu-id="00666-141">In Percentage of voice users involved in UC-UC calls shows the percentage of users who are enabled for Enterprise Voice who will be enabled only for UC-UC calls.</span></span> <span data-ttu-id="00666-142">Это число рассчитывается на основе данных, указанных для показателя Процент пользователей голосовых служб, которые участвуют в звонках из объединенных коммуникаций в ТСОП.</span><span class="sxs-lookup"><span data-stu-id="00666-142">This number is calculated based on what you input for Percentage of voice users enabled for UC-PSTN calls.</span></span>

<span data-ttu-id="00666-143">**Конференции**</span><span class="sxs-lookup"><span data-stu-id="00666-143">**Conferencing**</span></span>

  - <span data-ttu-id="00666-144">В процентах от пользователей на параллельных конференциях введите процент пользователей, которые будут одновременно участвовать в конференциях.</span><span class="sxs-lookup"><span data-stu-id="00666-144">In Percentage of users in concurrent conferences, type the percentage of users who will be concurrently participating in conferences.</span></span> <span data-ttu-id="00666-145">По умолчанию используется значение 5%.</span><span class="sxs-lookup"><span data-stu-id="00666-145">The default is 5%.</span></span>

  - <span data-ttu-id="00666-146">В процентах от конференций только для групповых мгновенных сообщений (без голосовой связи) введите процентное соотношение конференций, конференции которого оботносятся только для мгновенных сообщений; Таким образом, не включайте звуковой компонент.</span><span class="sxs-lookup"><span data-stu-id="00666-146">In Percentage of conferences with group IM only (no voice), type the percentage of conferences whose conferences will involve instant messaging only; that is, that do not include an audio component.</span></span> <span data-ttu-id="00666-147">Значение по умолчанию — 10%</span><span class="sxs-lookup"><span data-stu-id="00666-147">The default is 10%</span></span>

  - <span data-ttu-id="00666-148">В процентах от пользователей, использующих Конференц-связь с телефонным подключением, введите процент одновременных участников на конференциях, которые будут использовать конференц-связь с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="00666-148">In Percentage of users using dial-in conferencing, type the percentage of concurrent participants in conferences who will be using dial-in conferencing.</span></span> <span data-ttu-id="00666-149">Значение по умолчанию равно 15%.</span><span class="sxs-lookup"><span data-stu-id="00666-149">The default is 15%.</span></span>

  - <span data-ttu-id="00666-150">В процентах от Конференции с помощью голоса введите процент конференций, которые будут содержать звуковой компонент.</span><span class="sxs-lookup"><span data-stu-id="00666-150">In Percentage of conferences using voice, type the percentage of conferences that will include an audio component.</span></span>
    
      - <span data-ttu-id="00666-151">Если в 20% процентах случаев на конференциях голосовой связи будет также использоваться обычное видео, установите флажок Включая видео (не видео Multiview).</span><span class="sxs-lookup"><span data-stu-id="00666-151">If 20% of your voice conferences will also include regular video, select the Including video (no Multi View) check box.</span></span>
    
      - <span data-ttu-id="00666-152">Если в 20% процентах случаев на конференциях будет также использоваться видео Multi-View, установите флажок Включая видео Multiview.</span><span class="sxs-lookup"><span data-stu-id="00666-152">If 20% of your conferences will also include Multi-View video, select the Including Multi View check box.</span></span>
    
      - <span data-ttu-id="00666-153">Если в 50% процентах случаев на конференциях с использованием голосовой связи будет также использоваться общий доступ к приложениям, установите флажок Включая общий доступ к приложениям.</span><span class="sxs-lookup"><span data-stu-id="00666-153">If 50% of your voice conferences will also include application sharing, select the Including application sharing check box.</span></span>
    
      - <span data-ttu-id="00666-154">Если на 20% ваших голосовых конференций есть отправка данных, например Microsoft PowerPoint® презентаций, установите флажок Включить веб-конференции.</span><span class="sxs-lookup"><span data-stu-id="00666-154">If 20% of your voice conferences include data uploads, such as Microsoft PowerPoint® presentations, select the Including web conferencing check box.</span></span>

<span data-ttu-id="00666-155">**Мобильность**</span><span class="sxs-lookup"><span data-stu-id="00666-155">**Mobility**</span></span>

  - <span data-ttu-id="00666-156">В процентах от числа пользователей, включенных для мобильных устройств, введите процентные значения пользователей, которые будут разрешены для подключения к серверу Lync Server с помощью мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="00666-156">In Percentage of users enabled for Mobility, type the percentage of your users who will be enabled to connect to Lync Server using mobile devices.</span></span> <span data-ttu-id="00666-157">По умолчанию используется значение 40%.</span><span class="sxs-lookup"><span data-stu-id="00666-157">The default is 40%.</span></span>

<span data-ttu-id="00666-158">После ввода всей необходимой информации калькулятор мощности оценивает требования.</span><span class="sxs-lookup"><span data-stu-id="00666-158">When you have entered all the necessary information, the capacity calculator estimates your requirements.</span></span> <span data-ttu-id="00666-159">В желтых ячейках отображаются вычисляемые значения ЦП, памяти и требования к пропускной способности, основанные на тестах, выполненных в лаборатории Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="00666-159">The yellow cells show calculated values for CPU, memory, and bandwidth requirements based on tests performed in Lync Server 2013 performance labs.</span></span> <span data-ttu-id="00666-160">Цифры приведены в качестве примера и не каждый из показателей был проверен и подтвержден.</span><span class="sxs-lookup"><span data-stu-id="00666-160">The numbers are provided as a guideline, not every single variation is tested and validated.</span></span> <span data-ttu-id="00666-161">Рассчитываются перечисленные ниже значения.</span><span class="sxs-lookup"><span data-stu-id="00666-161">The following values are calculated:</span></span>

  - <span data-ttu-id="00666-162">ЦП переднего плана: процент использования ЦП, если нагрузка обрабатывалась на одном сервере переднего плана с теми же характеристиками, что и у сервера, который использовался при тестировании Microsoft.</span><span class="sxs-lookup"><span data-stu-id="00666-162">Front End CPU: Percentage of CPU usage if the entire load were being handled by one Front End Server of the same specifications as the server that was used in Microsoft testing.</span></span>

  - <span data-ttu-id="00666-163">Сеть в Мбит/с: требования к пропускной способности в мегабитах за секунду (Мбит/с) для соответствующей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00666-163">Network in Mbps: Bandwidth requirements in megabits per second (Mbps) for the corresponding workload.</span></span>

  - <span data-ttu-id="00666-164">Память в ГБ: объем памяти в гигабайтах (ГБ), необходимый для соответствующей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00666-164">Memory in GB: Memory required in gigabytes (GB) for the corresponding workload.</span></span>

<span data-ttu-id="00666-165">В ячейках зеленого цвета указаны рекомендации для модели использования, которую вы ввели.</span><span class="sxs-lookup"><span data-stu-id="00666-165">The green cells show recommendations for the usage model that you entered.</span></span>

  - <span data-ttu-id="00666-166">Общее число серверов переднего плана: требуемое количество физических серверов основано на выделенных серверах Lync Server 2013 с двумя процессорами, Hex и шестым, с 2 260 megacycles.</span><span class="sxs-lookup"><span data-stu-id="00666-166">Total Front End Servers: The number of physical servers required are based on dedicated servers running Lync Server 2013 with dual processor, hex-core, with 2,260 megacycles.</span></span>

  - <span data-ttu-id="00666-167">Обратите внимание, что рекомендуется включить технологию Hyper-Threading, которая, как доказано, повышает производительности серверов с поддержкой видео и аудио.</span><span class="sxs-lookup"><span data-stu-id="00666-167">Note that enabling hyperthreading is recommended and has been proven to improve performance for servers that support audio/video.</span></span>

  - <span data-ttu-id="00666-168">Пограничные серверы: количество необходимых пограничных серверов, исходя из того, что 30% всех одновременно подключенных пользователей используют для связи пограничные серверы.</span><span class="sxs-lookup"><span data-stu-id="00666-168">Edge Servers: The number of Edge Servers required, based on 30% of all concurrent users communicating through the Edge Servers.</span></span> <span data-ttu-id="00666-169">Этот процент нельзя изменить в калькуляторе.</span><span class="sxs-lookup"><span data-stu-id="00666-169">This percentage cannot be changed in the calculator.</span></span>

  - <span data-ttu-id="00666-170">Архивация / Запись сведений о звонке / Хранилище служб качества взаимодействия: количество хранилищ, необходимых для функций архивации или мониторинга, если они требуются в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="00666-170">Archiving/Call Detail Recording/Quality of Experience services Store: The number of stores required for Archiving or Monitoring features, if they are enabled in your organization.</span></span>

  - <span data-ttu-id="00666-171">Обязательный внутренний сервер баз данных (обязательные пулы): количество внутренних серверов баз данных, необходимых для поддержки выбранной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00666-171">Back End Database Server Required (Pools Required): The number of back-end database servers required to support the selected workload.</span></span>

<span data-ttu-id="00666-172">Кроме того, в строке рядом с общим числом серверов переднего плана указаны дополнительные сведения о нагрузках на серверах и в сети для всех объединенных запланированных нагрузок.</span><span class="sxs-lookup"><span data-stu-id="00666-172">Additionally, in the row next to Total Front End Servers, more information is provided about the load on your servers and network for all the planned workloads combined.</span></span>

  - <span data-ttu-id="00666-173">Средняя загрузка процессора: средний показатель ресурсов ЦП на сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="00666-173">Average CPU Load: The average CPU usage per Front End server.</span></span>

  - <span data-ttu-id="00666-174">Сеть в Мбит/с: распределение требуемой пропускной способности для поддержки модели использования, которую вы ввели.</span><span class="sxs-lookup"><span data-stu-id="00666-174">Network in Mbps: The required bandwidth allocation to support the usage model that you entered.</span></span>

  - <span data-ttu-id="00666-175">Память в ГБ: необходимый объем памяти в гигабайтах (ГБ) для каждого сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="00666-175">Memory in GB: Memory, in gigabytes, required for each Front End server.</span></span>

</div>

<div>

## <a name="adjusting-for-your-processors"></a><span data-ttu-id="00666-176">Соответствие вашим процессорам</span><span class="sxs-lookup"><span data-stu-id="00666-176">Adjusting For Your Processors</span></span>

<span data-ttu-id="00666-177">Все показатели ресурсов ЦП в электронной таблице дают основания предполагать, что для каждого сервера используются два шестиядерных процессора 2,26 ГГц, память не менее 32 ГБ, не менее 8 жестких дисков с частотой вращения шпинделя 10000 об/мин и с минимальным свободным пространством в 72 ГБ.</span><span class="sxs-lookup"><span data-stu-id="00666-177">All the CPU usage figures in the spreadsheet assume that each server has a dual processor, hex-core with 2.26 GHz, at least 32 GB of memory, and 8 or more 10,000-RPM hard disk drives with at least 72 GB free disk space.</span></span>

<span data-ttu-id="00666-178">Если для ваших серверов используются другие процессоры, показатели можно изменить в соответствии с вашим оборудованием.</span><span class="sxs-lookup"><span data-stu-id="00666-178">If your servers have different processors, you can adjust the figures to match your hardware.</span></span>

<span data-ttu-id="00666-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00666-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

