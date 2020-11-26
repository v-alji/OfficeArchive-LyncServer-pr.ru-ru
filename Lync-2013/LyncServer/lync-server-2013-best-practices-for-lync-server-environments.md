---
title: 'Lync Server 2013: советы и рекомендации по работе с серверными средами Lync'
description: 'Lync Server 2013: советы и рекомендации по работе с серверными средами Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for Lync Server environments
ms:assetid: b0e45d84-09c8-4d3e-aad0-bc6f34ce233b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720348(v=OCS.15)
ms:contentKeyID: 63969642
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae6c02621bd6506d2a1d379aeaf92b20ce3f7ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436064"
---
# <a name="best-practices-for-lync-server-2013-environments"></a><span data-ttu-id="89c3b-103">Рекомендации по работе с средами Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-103">Best practices for Lync Server 2013 environments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89c3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89c3b-104">

<span> </span></span></span>

<span data-ttu-id="89c3b-105">_**Тема последнего изменения:** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="89c3b-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="89c3b-106">Следующие общие принципы должны применяться к текущим операциям системы:</span><span class="sxs-lookup"><span data-stu-id="89c3b-106">The following general principles should be applied to ongoing operations of your system:</span></span>

  - <span data-ttu-id="89c3b-107">**Общие сведения и использование MOF**   MOF — это набор рекомендаций, принципов и моделей, которые предоставляют организациям технические рекомендации по управлению ИТ-ресурсами, например ежедневные операции Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="89c3b-107">**Understand and utilize MOF**   MOF is a collection of best practices, principles, and models that provide organizations technical guidance about the management of IT assets, such as daily Lync Server 2013 operations.</span></span> <span data-ttu-id="89c3b-108">Ниже приведены рекомендации по использованию MOF, которые помогут вам добиться критической надежности, доступности, обеспечения поддержки и управляемости продуктов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="89c3b-108">Following MOF guidelines can help you achieve mission-critical production system reliability, availability, supportability, and manageability for Microsoft products.</span></span> <span data-ttu-id="89c3b-109">Дополнительные сведения можно найти в разделе [Microsoft Operations Framework 4,0](https://go.microsoft.com/fwlink/p/?linkid=40939).</span><span class="sxs-lookup"><span data-stu-id="89c3b-109">For more information, see [Microsoft Operations Framework 4.0](https://go.microsoft.com/fwlink/p/?linkid=40939).</span></span>

  - <span data-ttu-id="89c3b-110">Ознакомьтесь с рекомендациями **по работе с Lync Server 2013**   Рекомендуется реализовать практичные и проверенные процедуры для управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="89c3b-110">**Learn about best practices for Lync Server 2013**   We recommend that you implement practical and proven procedures to manage Lync Server 2013.</span></span> <span data-ttu-id="89c3b-111">Использование проверенных, протестированных и документированных методов управления операциями может быть более эффективной, чем разработка собственных методов.</span><span class="sxs-lookup"><span data-stu-id="89c3b-111">By using tried, tested, and documented methods of managing operations may be more efficient than developing your own methods.</span></span>

  - <span data-ttu-id="89c3b-112">**Разделение операций на ежедневные, еженедельные и ежемесячные процессы**   Задокументируйте необходимые рабочие задачи, которые будут регулярно выполняться.</span><span class="sxs-lookup"><span data-stu-id="89c3b-112">**Separate operations into daily, weekly, and monthly processes**   Document the required operational tasks that you'll regularly perform.</span></span> <span data-ttu-id="89c3b-113">Сведения о том, как выполнять задачи, помогают удостовериться в том, что информация сохраняется при изменении в рабочей среде, например при развертывании новых технологий или изменении штатных обязанностей.</span><span class="sxs-lookup"><span data-stu-id="89c3b-113">Documenting how you perform tasks helps make sure that your information is preserved when there is a change in your operational environment such as when new technologies are deployed or staff changes occur.</span></span> <span data-ttu-id="89c3b-114">Рекомендуется разделить операционные задачи на управляемые рабочие нагрузки, где задачи выполняются ежедневно, еженедельно и ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="89c3b-114">We recommend that operational tasks be separated into manageable workloads where tasks are performed daily, weekly, and monthly.</span></span> <span data-ttu-id="89c3b-115">Ежедневные задачи будут сосредоточиться на работе системы, а ежемесячные задачи — сосредоточиться на долгосрочной работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="89c3b-115">Daily tasks would focus efforts on the functioning of a system, and monthly tasks would focus more on ensuring the long-term health of a system.</span></span>
    
    <span data-ttu-id="89c3b-116">Этот документ можно использовать в средах, в которых развертываются только компоненты обмена мгновенными сообщениями и присутствия (IM/P), а также обмен мгновенными сообщениями с корпоративной голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="89c3b-116">This document can be used in environments deploying only instant messaging/presence (IM/P) components or IM/P with Enterprise Voice.</span></span> <span data-ttu-id="89c3b-117">Если задачи или контрольный список относятся к корпоративной голосовой связи, это упомянуто, и если в вашей среде не указана корпоративная голосовая связь, часть может быть пропущена.</span><span class="sxs-lookup"><span data-stu-id="89c3b-117">When tasks or checklist items are specific to Enterprise Voice, this is mentioned and if your environment does not include Enterprise Voice the portion may be skipped.</span></span>

  - <span data-ttu-id="89c3b-118">**Развертывание средств, необходимых для работы сервера Lync Server 2013**   Доступно множество средств, помогающих в устранении неполадок, автоматизации задач, а также для отслеживания и обслуживания среды Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="89c3b-118">**Deploy the tools that are required for operating Lync Server 2013**   Many tools are available to help troubleshoot issues, automate tasks, and help monitor and maintain the Lync Server 2013 environment.</span></span> <span data-ttu-id="89c3b-119">Определите стандартный набор инструментов для Организации, чтобы задачи, выполняемые командой операций, выполнялись корректно, эффективно, своевременно и в контролируемом виде.</span><span class="sxs-lookup"><span data-stu-id="89c3b-119">Define a standard set of tools for your organization so the tasks that are performed by the operations team are performed accurately, efficiently, consistently, and in a controlled manner.</span></span> <span data-ttu-id="89c3b-120">Кроме того, необходимо реализовать процессы для отслеживания происшествий и существенных изменений в конфигурации.</span><span class="sxs-lookup"><span data-stu-id="89c3b-120">You should also implement processes to track incidents and major configuration changes.</span></span>

<div>

## <a name="reference"></a><span data-ttu-id="89c3b-121">Справка</span><span class="sxs-lookup"><span data-stu-id="89c3b-121">Reference</span></span>

<span data-ttu-id="89c3b-122">Для тех, кто еще не знаком с основами управления серверами в целом, мы предлагаем общие рекомендации по управлению сервером.</span><span class="sxs-lookup"><span data-stu-id="89c3b-122">For the benefit of readers not already familiar with the basics of server management in general, we provide an overview of server management practices.</span></span> <span data-ttu-id="89c3b-123">Читатели, уже знакомые с управлением сервером, могут пропустить этот раздел.</span><span class="sxs-lookup"><span data-stu-id="89c3b-123">Readers already familiar with server management may choose to skip this section.</span></span>

<span data-ttu-id="89c3b-124">Рекомендации — это рекомендации, которые основываются на наборе знаний и опыте, когда ИТ-специалисты посмотрелись в разных средах.</span><span class="sxs-lookup"><span data-stu-id="89c3b-124">Best practices are recommendations that are based on the knowledge and experience that IT professionals have gained across many environments.</span></span> <span data-ttu-id="89c3b-125">Они предоставляют стандартные процедуры для типичных задач, которые администраторы сервера Lync Server должны выполнять ежедневно, и перечень средств, которые должны использоваться для управления средой Lync Server.</span><span class="sxs-lookup"><span data-stu-id="89c3b-125">They provide standard procedures for typical tasks that your Lync Server administrators must perform daily, and list the tools that they should use to manage a Lync Server environment.</span></span>

<span data-ttu-id="89c3b-126">К типичным задачам для администраторов Lync относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="89c3b-126">Typical tasks for Lync administrators include the following:</span></span>

  - <span data-ttu-id="89c3b-127">**Управление емкостью и**   обеспечением доступности   Определите, как и что следует измерять, чтобы прогнозировать будущие требования к мощности и сообщать о емкости, надежности и доступности систем.</span><span class="sxs-lookup"><span data-stu-id="89c3b-127">**Capacity and Availability Management**   Define how and what to measure to predict future capacity requirements and to report about the capacity, reliability, and availability of your systems.</span></span> <span data-ttu-id="89c3b-128">Необходимо убедиться в том, что на серверах, на которых работает Lync Server, определена размер для обработки нагрузки системы, а незапланированные простои остаются на уровнях, определенных в соглашении об уровне обслуживания (SLA).</span><span class="sxs-lookup"><span data-stu-id="89c3b-128">You must verify that servers that are running Lync Server are sized to handle the load on the system, and that unplanned downtime is kept under the levels defined in the service level agreement (SLA).</span></span> <span data-ttu-id="89c3b-129">Кроме того, вам потребуется обновить оборудование, чтобы оно продолжало соответствовать определенным требованиям.</span><span class="sxs-lookup"><span data-stu-id="89c3b-129">Additionally, you'll have to upgrade hardware to continue to meet the defined requirements.</span></span>

  - <span data-ttu-id="89c3b-130">Управление **изменениями и конфигурацией**   Управление изменениями, внесенными в ИТ – системы.</span><span class="sxs-lookup"><span data-stu-id="89c3b-130">**Change Management and Configuration Management**   Control how changes are made to IT systems.</span></span> <span data-ttu-id="89c3b-131">Это должно включать тестирование, планы обратной связи с приложениями и ограничений на непредвиденные случаи, документацию по всем изменениям и одобрение управления в случае возникновения проблем.</span><span class="sxs-lookup"><span data-stu-id="89c3b-131">This should include testing, application feedback and contingency plans, documentation of all changes, and approval from management if issues occur.</span></span> <span data-ttu-id="89c3b-132">Храните запись программного обеспечения и ресурсов оборудования и их конфигураций.</span><span class="sxs-lookup"><span data-stu-id="89c3b-132">Keep a record of your software and hardware assets and their configurations.</span></span>

  - <span data-ttu-id="89c3b-133">**Администрирование системы**   Структурирование стандартных методов для выполнения административных задач, таких как администрирование базы данных и администрирование сайта.</span><span class="sxs-lookup"><span data-stu-id="89c3b-133">**System Administration**   Outline standard methods for doing administrative tasks such as database administration and site administration.</span></span>

  - <span data-ttu-id="89c3b-134">**Администрирование безопасности**   Подробное описание политики и плана, защищающего конфиденциальность данных, целостность данных и доступность данных в ИТ-инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="89c3b-134">**Security Administration**   Have a detailed policy and plan that protects data confidentiality, data integrity, and data availability of the IT infrastructure.</span></span> <span data-ttu-id="89c3b-135">Сюда входят повседневные мероприятия и задачи, связанные с обслуживанием и настройкой инфраструктуры ИТ-безопасности.</span><span class="sxs-lookup"><span data-stu-id="89c3b-135">This includes day-to-day activities and tasks that are related to maintaining and adjusting the IT security infrastructure.</span></span>

  - <span data-ttu-id="89c3b-136">**Устранение неполадок системы**   Способы решения проблем, связанных с неожиданными неполадками, в том числе шаги для предотвращения подобных проблем в будущем.</span><span class="sxs-lookup"><span data-stu-id="89c3b-136">**System Troubleshooting**   Outline methods for dealing with unexpected issues, including steps to prevent similar issues in the future.</span></span>

  - <span data-ttu-id="89c3b-137">**Соглашения об уровне обслуживания**   Обеспечьте набор целей для производительности ИТ-систем и регулярно Измерьте производительность по сравнению с этими целями.</span><span class="sxs-lookup"><span data-stu-id="89c3b-137">**Service Level Agreements**   Maintain a set of goals for the performance of the IT systems and regularly measure performance against these goals.</span></span>

  - <span data-ttu-id="89c3b-138">**Документация**   Стандартные процедуры для документов, такие как сведения о конфигурации и выводы, и они могут быть доступны сотрудникам, которым они нужны.</span><span class="sxs-lookup"><span data-stu-id="89c3b-138">**Documentation**   Document standard procedures, such as configuration information and lessons learned, and make them available to the staff members that need them.</span></span> <span data-ttu-id="89c3b-139">После внесения изменений в конфигурацию Обновите документацию соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="89c3b-139">As changes to the configuration are made, update the documentation accordingly.</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="89c3b-140">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="89c3b-140">Related Sections</span></span>

<span data-ttu-id="89c3b-141">Прежде чем продолжить, ознакомьтесь со следующими разделами, посвященными системным операциям.</span><span class="sxs-lookup"><span data-stu-id="89c3b-141">Review the following topics concerning system operations before proceeding:</span></span>

  - [<span data-ttu-id="89c3b-142">Управление емкостью и доступностью в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-142">Capacity and availability management in Lync Server 2013</span></span>](lync-server-2013-capacity-and-availability-management.md)

  - [<span data-ttu-id="89c3b-143">Управление изменениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-143">Change management in Lync Server 2013</span></span>](lync-server-2013-change-management.md)

  - [<span data-ttu-id="89c3b-144">Управление конфигурацией в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-144">Configuration management in Lync Server 2013</span></span>](lync-server-2013-configuration-management.md)

  - [<span data-ttu-id="89c3b-145">Администрирование системы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-145">System administration in Lync Server 2013</span></span>](lync-server-2013-system-administration.md)

  - [<span data-ttu-id="89c3b-146">Соглашения об уровне обслуживания в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-146">Service level agreements in Lync Server 2013</span></span>](lync-server-2013-service-level-agreements.md)

  - [<span data-ttu-id="89c3b-147">Документация в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-147">Documentation in Lync Server 2013</span></span>](lync-server-2013-documentation.md)

  - [<span data-ttu-id="89c3b-148">Стандартные процедуры в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-148">Standard procedures in Lync Server 2013</span></span>](lync-server-2013-standard-procedures.md)

  - [<span data-ttu-id="89c3b-149">Процедуры для экстренного реагирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89c3b-149">Emergency procedures in Lync Server 2013</span></span>](lync-server-2013-emergency-procedures.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="89c3b-150">См. также</span><span class="sxs-lookup"><span data-stu-id="89c3b-150">See Also</span></span>


[<span data-ttu-id="89c3b-151">Microsoft Operations Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="89c3b-151">Microsoft Operations Framework 4.0</span></span>](https://go.microsoft.com/fwlink/p/?linkid=40939)  
  

<span data-ttu-id="89c3b-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89c3b-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

