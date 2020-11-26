---
title: Вопросы и ответы по работе с Lync Server 2013 с помощью средств нагрузки и производительности
description: Вопросы и ответы по работе с Lync Server 2013 с помощью средств нагрузки и производительности.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Stress and Performance Tool FAQ
ms:assetid: a5aff705-320c-4916-8094-23046b2a1b18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945600(v=OCS.15)
ms:contentKeyID: 51541426
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 716325390bc33df209be3bdc67ed8b6cd7d1ec30
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446439"
---
# <a name="lync-server-2013-stress-and-performance-tool-faq"></a><span data-ttu-id="24f7f-103">Вопросы и ответы по работе с Lync Server 2013 с помощью средств нагрузки и производительности</span><span class="sxs-lookup"><span data-stu-id="24f7f-103">Lync Server 2013 Stress and Performance Tool FAQ</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24f7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24f7f-104">

<span> </span></span></span>

<span data-ttu-id="24f7f-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="24f7f-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<div>

## <a name="frequently-asked-questions"></a><span data-ttu-id="24f7f-106">Ответы на часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="24f7f-106">Frequently Asked Questions</span></span>

<span data-ttu-id="24f7f-107">Ниже приведены ответы на часто задаваемые вопросы о средстве быстрой и высокопроизводительной нагрузки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24f7f-107">Here are some frequently asked questions about the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="can-i-run-lyncperftoolexe-in-production"></a><span data-ttu-id="24f7f-108">Можно ли запускать LyncPerfTool.exe в производстве?</span><span class="sxs-lookup"><span data-stu-id="24f7f-108">Can I run LyncPerfTool.exe in production?</span></span>

<span data-ttu-id="24f7f-109">Мы не рекомендуем использовать эту задачу.</span><span class="sxs-lookup"><span data-stu-id="24f7f-109">We do not recommend this.</span></span> <span data-ttu-id="24f7f-110">Это средство влияет на производительность сервера, безопасность и взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="24f7f-110">This tool will impact server performance, security, and user experience.</span></span>

</div>

<div>

## <a name="i-am-logging-on-my-users-for-the-first-time-why-are-the-servers-running-at-such-high-load"></a><span data-ttu-id="24f7f-111">Я занимаюсь регистрацией моих пользователей в первый раз.</span><span class="sxs-lookup"><span data-stu-id="24f7f-111">I am logging on my users for the first time.</span></span> <span data-ttu-id="24f7f-112">Почему серверы работают с такой высокой загрузкой?</span><span class="sxs-lookup"><span data-stu-id="24f7f-112">Why are the servers running at such high load?</span></span>

<span data-ttu-id="24f7f-113">При первом входе пользователя в систему возникают дополнительные операции.</span><span class="sxs-lookup"><span data-stu-id="24f7f-113">The first time the users log on, there are additional operations that occur.</span></span> <span data-ttu-id="24f7f-114">В результате производительность серверного сервера Microsoft SQL Server будет снижена.</span><span class="sxs-lookup"><span data-stu-id="24f7f-114">As a result, the performance on the Microsoft SQL Server Back End Server will be degraded.</span></span> <span data-ttu-id="24f7f-115">Рекомендуется запустить короткий тест для входа на всех пользователей, а затем перезапустить его перед тем, как оценивать результаты.</span><span class="sxs-lookup"><span data-stu-id="24f7f-115">We recommend that you run a short test that logs on all of the users, and then restart the clients before you measure results.</span></span> <span data-ttu-id="24f7f-116">Мы не поддерживаем более 12 одновременных сеансов входа пользователей в секунду, но это зависит от конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="24f7f-116">We do not support more than 12 concurrent user logon sessions per second, but this depends on your hardware configuration.</span></span>

</div>

<div>

## <a name="my-clients-are-running-out-of-memory-what-should-i-do"></a><span data-ttu-id="24f7f-117">Недостаточно памяти для моих клиентов.</span><span class="sxs-lookup"><span data-stu-id="24f7f-117">My clients are running out of memory.</span></span> <span data-ttu-id="24f7f-118">Что делать?</span><span class="sxs-lookup"><span data-stu-id="24f7f-118">What should I do?</span></span>

<span data-ttu-id="24f7f-119">Если на ваших клиентах недостаточно памяти, нужно уменьшить количество пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="24f7f-119">If your clients are running out of memory, you need to reduce the number of users per computer.</span></span>

</div>

<div>

## <a name="my-clients-are-at-100-percent-cpu-all-the-time-what-should-i-do"></a><span data-ttu-id="24f7f-120">У моих клиентов в 100 процентов ЦП все время.</span><span class="sxs-lookup"><span data-stu-id="24f7f-120">My clients are at 100 percent CPU all the time.</span></span> <span data-ttu-id="24f7f-121">Что делать?</span><span class="sxs-lookup"><span data-stu-id="24f7f-121">What should I do?</span></span>

<span data-ttu-id="24f7f-122">Если ваши клиенты работают с очень высокими ЦП после входа в систему, необходимо уменьшить количество пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="24f7f-122">If your clients are running with very high CPU after all the users have logged on, you need to reduce the number of users per computer.</span></span> <span data-ttu-id="24f7f-123">Высокие выгрузки ЦП приемлемы, но если они постоянны, вам нужно уменьшить нагрузку.</span><span class="sxs-lookup"><span data-stu-id="24f7f-123">High CPU spikes are acceptable, but if it is sustained, you need to reduce the load.</span></span>

</div>

<div>

## <a name="can-i-run-the-tool-on-the-server-itself"></a><span data-ttu-id="24f7f-124">Можно ли запускать средство на самом сервере?</span><span class="sxs-lookup"><span data-stu-id="24f7f-124">Can I run the tool on the server itself?</span></span>

<span data-ttu-id="24f7f-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="24f7f-125">No.</span></span> <span data-ttu-id="24f7f-126">Этот сценарий не поддерживается и может завершиться сбоем из-за несоответствия двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="24f7f-126">This scenario is not supported and may fail due to a binary mismatch.</span></span> <span data-ttu-id="24f7f-127">Кроме того, так как точка предназначена для измерения потребления ресурсов на сервере, при запуске этого средства будут вырисовываться небессмысленные измерения.</span><span class="sxs-lookup"><span data-stu-id="24f7f-127">Also, because the point is to measure resource consumption on the server, running the tool there would render the measurements meaningless.</span></span>

</div>

<div>

## <a name="can-i-run-lyncperftoolexe-on-a-virtual-server-or-on-microsoft-hyper-v-server-20082012"></a><span data-ttu-id="24f7f-128">Можно ли запускать LyncPerfTool.exe на виртуальном сервере или на сервере Microsoft Hyper-V 2008/2012?</span><span class="sxs-lookup"><span data-stu-id="24f7f-128">Can I run LyncPerfTool.exe on a Virtual Server or on Microsoft Hyper-V Server 2008/2012?</span></span>

<span data-ttu-id="24f7f-129">Да.</span><span class="sxs-lookup"><span data-stu-id="24f7f-129">Yes.</span></span>

</div>

<div>

## <a name="what-does-mpop-mean"></a><span data-ttu-id="24f7f-130">Что означает MPOP?</span><span class="sxs-lookup"><span data-stu-id="24f7f-130">What does MPOP mean?</span></span>

<span data-ttu-id="24f7f-131">MPOP означает несколько точек присутствия.</span><span class="sxs-lookup"><span data-stu-id="24f7f-131">MPOP stands for multiple points of presence.</span></span> <span data-ttu-id="24f7f-132">Она предназначена для моделирования ситуации, когда пользователи входят в состав Lync 2013 с нескольких компьютеров.</span><span class="sxs-lookup"><span data-stu-id="24f7f-132">It is meant to simulate the scenario where users are logged on to Lync 2013 from multiple machines.</span></span> <span data-ttu-id="24f7f-133">Обратите внимание, что в LyncPerfTool.exe каждая конечная точка использует профиль по умолчанию (то есть профиль не разбивается между двумя точками присутствия).</span><span class="sxs-lookup"><span data-stu-id="24f7f-133">Note that in LyncPerfTool.exe, each endpoint uses the default profile (that is, the profile is not split between the two points of presence).</span></span>

</div>

<div>

## <a name="i-started-lyncperftoolexe-but-nothing-is-happening-whats-going-on"></a><span data-ttu-id="24f7f-134">Я начал LyncPerfTool.exe, но ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="24f7f-134">I started LyncPerfTool.exe but nothing is happening.</span></span> <span data-ttu-id="24f7f-135">Что происходит?</span><span class="sxs-lookup"><span data-stu-id="24f7f-135">What’s going on?</span></span>

<span data-ttu-id="24f7f-136">Установите флажок Общий счетчик активных конечных точек на клиентах, чтобы проверить, подключаются ли пользователи.</span><span class="sxs-lookup"><span data-stu-id="24f7f-136">Check the Total Active Endpoints counter on the clients to see if the users are connecting.</span></span> <span data-ttu-id="24f7f-137">Если пользователи не подключаются, проверьте конфигурацию Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24f7f-137">If users are not connecting, verify your Lync Server 2013 configuration.</span></span> <span data-ttu-id="24f7f-138">Как правило, эта проблема возникает из-за того, что имя сервера, префикс пользователя или пароль неверны.</span><span class="sxs-lookup"><span data-stu-id="24f7f-138">This issue usually occurs because the server name, the user prefix, or the password is incorrect.</span></span> <span data-ttu-id="24f7f-139">Обратите внимание, что внешние клиенты должны указать прокси-сервер доступа в качестве значения TargetServer.</span><span class="sxs-lookup"><span data-stu-id="24f7f-139">Note that external clients should specify the Access Proxy as the TargetServer value.</span></span> <span data-ttu-id="24f7f-140">Проверьте порт в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="24f7f-140">Verify the port in the configuration file.</span></span>

</div>

<div>

## <a name="how-do-i-know-something-is-happening"></a><span data-ttu-id="24f7f-141">Как узнать, что происходит?</span><span class="sxs-lookup"><span data-stu-id="24f7f-141">How do I know something is happening?</span></span>

<span data-ttu-id="24f7f-142">Различные счетчики производительности LyncPerfTool указывают, нужно ли пользователям подключаться к ним и выполнять действия.</span><span class="sxs-lookup"><span data-stu-id="24f7f-142">The various LyncPerfTool performance counters indicate whether or not users are connecting and performing actions.</span></span> <span data-ttu-id="24f7f-143">Однако простой способ проверки — войти в одну из учетных записей с помощью Lync 2013 и выполнить нужное действие.</span><span class="sxs-lookup"><span data-stu-id="24f7f-143">However, an easy way to check is to log on to one of the accounts by using Lync 2013 and performing the action you want.</span></span>

</div>

<div>

## <a name="i-have-live-communications-server-2007-r2-capacity-planning-tools-andor-lync-server-2010-installed-is-that-ok"></a><span data-ttu-id="24f7f-144">У меня установлено средство планирования производительности Live Communications Server 2007 R2 и/или Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="24f7f-144">I have Live Communications Server 2007 R2 Capacity Planning Tools and/or Lync Server 2010 installed.</span></span> <span data-ttu-id="24f7f-145">Это нормально?</span><span class="sxs-lookup"><span data-stu-id="24f7f-145">Is that OK?</span></span>

<span data-ttu-id="24f7f-146">Нет.</span><span class="sxs-lookup"><span data-stu-id="24f7f-146">No.</span></span> <span data-ttu-id="24f7f-147">Возникли проблемы с совместимостью, и вы должны удалить все предыдущие версии этого продукта.</span><span class="sxs-lookup"><span data-stu-id="24f7f-147">There are interoperability issues, and you must uninstall all previous versions of this product.</span></span>

</div>

<div>

## <a name="will-the-stress-and-performance-tools-set-up-the-caa-call-information-server-topology"></a><span data-ttu-id="24f7f-148">Настроили ли средства для работы с загрузкой и производительностью топология сервера информации о звонке CAA?</span><span class="sxs-lookup"><span data-stu-id="24f7f-148">Will the Stress and Performance tools set up the CAA Call Information server topology?</span></span>

<span data-ttu-id="24f7f-149">Нет.</span><span class="sxs-lookup"><span data-stu-id="24f7f-149">No.</span></span> <span data-ttu-id="24f7f-150">Средства создают только пользователи, контакты и списки рассылки, а также имитируют нагрузку пользователей.</span><span class="sxs-lookup"><span data-stu-id="24f7f-150">The tools only create users, contacts, and distribution lists, and simulate user load.</span></span>

</div>

<div>

## <a name="what-is-the-maximum-number-of-users-that-the-tools-support"></a><span data-ttu-id="24f7f-151">Каково максимальное число пользователей, которые поддерживаются средствами?</span><span class="sxs-lookup"><span data-stu-id="24f7f-151">What is the maximum number of users that the tools support?</span></span>

<span data-ttu-id="24f7f-152">С помощью этих средств мы создали общее количество пользователей 80 000 и выполнили тестирование с учетом всех пользователей 30 000.</span><span class="sxs-lookup"><span data-stu-id="24f7f-152">We have created up to a total of 80,000 users and executed tests totaling 30,000 users, using these tools.</span></span> <span data-ttu-id="24f7f-153">Мы рекомендуем использовать не более 120 000 пользователей, хотя в соответствии с техническими ограничениями допускают более высокие значения (в зависимости от того, какое оборудование доступно для клиента и сервера).</span><span class="sxs-lookup"><span data-stu-id="24f7f-153">We suggest a maximum of 120,000 users, although the technical limitations allow for a higher value, depending on the client and server hardware available.</span></span>

<span data-ttu-id="24f7f-154"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24f7f-154"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

