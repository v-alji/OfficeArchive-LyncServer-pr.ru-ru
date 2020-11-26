---
title: 'Lync Server 2013: усиление защиты и защита серверов и приложений'
description: 'Lync Server 2013: укрепление и защита серверов и приложений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting servers and applications for Lync Server 2013
ms:assetid: 9ca2b233-26f1-4d72-96e7-81a82c727806
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518331(v=OCS.15)
ms:contentKeyID: 62625491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed1205439208dfdadf5396b976d5d4876fb0aa24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427756"
---
# <a name="hardening-and-protecting-servers-and-applications-for-lync-server-2013"></a><span data-ttu-id="48d72-103">Усиление защиты и защита серверов и приложений для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48d72-103">Hardening and protecting servers and applications for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48d72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48d72-104">

<span> </span></span></span>

<span data-ttu-id="48d72-105">_**Тема последнего изменения:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="48d72-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="48d72-106">Вы должны защищать и защитить операционную систему и приложения в соответствии с рекомендациями для определенного компонента.</span><span class="sxs-lookup"><span data-stu-id="48d72-106">You should harden and protect your operating system and applications according to best practices for that specific component.</span></span> <span data-ttu-id="48d72-107">В этом разделе объясняется, как защитить серверы приложений и использовать групповую политику для реализации блокировки безопасности.</span><span class="sxs-lookup"><span data-stu-id="48d72-107">This section describes how to harden application servers and use Group Policy to implement security lockdowns.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="48d72-108">Вы также можете загрузить и защитить базы данных, используемые при развертывании Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48d72-108">You can also harden and protect the databases used for you Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="48d72-109">Подробные сведения можно найти в разделе Защита <A href="lync-server-2013-hardening-and-protecting-databases.md">баз данных Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="48d72-109">For details, see <A href="lync-server-2013-hardening-and-protecting-databases.md">Hardening and protecting the databases of Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="securing-application-servers"></a><span data-ttu-id="48d72-110">Защита серверов приложений</span><span class="sxs-lookup"><span data-stu-id="48d72-110">Securing Application Servers</span></span>

<span data-ttu-id="48d72-111">Для серверов приложений операционная система и приложение должны быть зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="48d72-111">For applications servers, the operating system and the application should be hardened.</span></span> <span data-ttu-id="48d72-112">Например, компьютер под управлением Windows Server 2008, предназначенный для использования Microsoft Internet Security and Acceleration (ISA) Server 2006, должен быть защищен от операционной системы и с точки зрения приложения.</span><span class="sxs-lookup"><span data-stu-id="48d72-112">For example, a Windows Server 2008 computer dedicated to running Microsoft Internet Security and Acceleration (ISA) Server 2006 should be hardened from the operating system and from the application perspective.</span></span> <span data-ttu-id="48d72-113">Свести к минимуму количество служб, запущенных и предоставленных сервером, должно быть основной задачей.</span><span class="sxs-lookup"><span data-stu-id="48d72-113">Minimizing the number of services running and provided by the server should be a primary goal.</span></span>

</div>

<div>

## <a name="securing-virtual-servers"></a><span data-ttu-id="48d72-114">Защита виртуальных серверов</span><span class="sxs-lookup"><span data-stu-id="48d72-114">Securing Virtual Servers</span></span>

<span data-ttu-id="48d72-115">Моментальные снимки виртуального сервера содержат копии дисков данных сервера и содержат дампы данных из памяти, которые могут содержать конфиденциальные криптографические данные, которые могут привести к атакам.</span><span class="sxs-lookup"><span data-stu-id="48d72-115">Virtual server snapshots contain copies of the server’s data disks and also contain dumps of in-memory data, both of which can contain sensitive cryptographic data that might lead to attacks.</span></span> <span data-ttu-id="48d72-116">Для производственных серверов, реализованных с помощью виртуализации, необходимо отключить все моментальные снимки сервера или управлять ими с очень управляемым способом.</span><span class="sxs-lookup"><span data-stu-id="48d72-116">For production servers implemented using virtualization, you should disable all server snapshots or manage them in a very controlled manner.</span></span> <span data-ttu-id="48d72-117">Подробнее об обеспечении безопасности виртуальных серверов Hyper-V можно узнать в руководстве по безопасности Hyper-V по адресу: [https://go.microsoft.com/fwlink/p/?LinkId=214176](https://go.microsoft.com/fwlink/p/?linkid=214176) .</span><span class="sxs-lookup"><span data-stu-id="48d72-117">For details about securing Hyper-V virtual servers, see the Hyper-V Security Guide at: [https://go.microsoft.com/fwlink/p/?LinkId=214176](https://go.microsoft.com/fwlink/p/?linkid=214176).</span></span>

</div>

<div>

## <a name="group-policy"></a><span data-ttu-id="48d72-118">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="48d72-118">Group Policy</span></span>

<span data-ttu-id="48d72-119">В Windows Server 2008 и Windows Server 2008 R2 групповая политика обеспечивает управление конфигурацией рабочего стола на основе каталогов.</span><span class="sxs-lookup"><span data-stu-id="48d72-119">In Windows Server 2008 and Windows Server 2008 R2, Group Policy provides directory-based desktop configuration management.</span></span> <span data-ttu-id="48d72-120">Вы можете использовать групповую политику для реализации блокировки безопасности, определяя параметры компьютера и пользователя в объекте групповой политики (GPO) для указанных ниже элементов.</span><span class="sxs-lookup"><span data-stu-id="48d72-120">You can use Group Policy to implement security lockdowns by defining Computer and User settings within a Group Policy object (GPO) for the following:</span></span>

  - <span data-ttu-id="48d72-121">Политики на основе реестра</span><span class="sxs-lookup"><span data-stu-id="48d72-121">Registry-based policies</span></span>

  - <span data-ttu-id="48d72-122">Безопасность</span><span class="sxs-lookup"><span data-stu-id="48d72-122">Security</span></span>

  - <span data-ttu-id="48d72-123">Установка программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="48d72-123">Software installation</span></span>

  - <span data-ttu-id="48d72-124">Сценарии</span><span class="sxs-lookup"><span data-stu-id="48d72-124">Scripts</span></span>

  - <span data-ttu-id="48d72-125">Перенаправление папок</span><span class="sxs-lookup"><span data-stu-id="48d72-125">Folder redirection</span></span>

  - <span data-ttu-id="48d72-126">Службы удаленной установки</span><span class="sxs-lookup"><span data-stu-id="48d72-126">Remote installation services</span></span>

<span data-ttu-id="48d72-127">Чтобы предоставить администратору пользовательский интерфейс для настройки этих параметров, административные шаблоны поставляются с выпусками операционных систем, выпусками пакетов обновления и некоторыми приложениями, включая Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48d72-127">To provide a user interface for the administrator to configure these settings, administrative templates are shipped with operating system releases, service pack releases, and some applications, including Lync Server 2013.</span></span>

<span data-ttu-id="48d72-128">Файл Communicator. adm — это административный шаблон, который поставляется с Lync Server 2013, установлен в каталог% WINDIR% \\ inf \\ и предоставляет интерфейс для параметров групповой политики.</span><span class="sxs-lookup"><span data-stu-id="48d72-128">The Communicator.adm file is an administrative template that ships with Lync Server 2013, is installed to the %windir%\\inf\\ directory, and provides an interface to the Group Policy settings.</span></span> <span data-ttu-id="48d72-129">Каждый параметр в Communicator. adm соответствует параметру в реестре, который влияет на работу приложения.</span><span class="sxs-lookup"><span data-stu-id="48d72-129">Each setting in Communicator.adm corresponds to a setting in the registry that affects application behavior.</span></span>

<span data-ttu-id="48d72-130">Доступ к параметрам можно получить с GPedit.dll, доступного в консоли "пользователи и компьютеры Active Directory", а также в консоли управления групповыми политиками (GPMC).</span><span class="sxs-lookup"><span data-stu-id="48d72-130">The settings can be accessed from GPedit.dll, which is available from the Active Directory Users and Computers console and the Group Policy Management Console (GPMC).</span></span>

</div>

<div>

## <a name="group-policy-security-settings"></a><span data-ttu-id="48d72-131">Параметры безопасности групповой политики</span><span class="sxs-lookup"><span data-stu-id="48d72-131">Group Policy Security Settings</span></span>

<span data-ttu-id="48d72-132">Групповая политика включает параметры безопасности для GPO в разделе Конфигурация компьютера/параметры Windows/параметры безопасности при доступе к GPedit.dll.</span><span class="sxs-lookup"><span data-stu-id="48d72-132">Group Policy contains security settings for a GPO under Computer Configuration/Windows Settings/Security Settings when accessed from GPedit.dll.</span></span> <span data-ttu-id="48d72-133">Вы можете импортировать шаблоны безопасности, чтобы настроить параметры безопасности для GPO.</span><span class="sxs-lookup"><span data-stu-id="48d72-133">You can import security templates to configure security settings for the GPO.</span></span> <span data-ttu-id="48d72-134">Руководство по безопасности Windows Server 2008 на странице [https://go.microsoft.com/fwlink/p/?LinkId=145186](https://go.microsoft.com/fwlink/p/?linkid=145186) набор средств управления соответствием требованиям безопасности для Windows server 2008 R2 [https://go.microsoft.com/fwlink/p/?LinkId=211882](https://go.microsoft.com/fwlink/p/?linkid=211882) содержит несколько примеров шаблонов, которые можно изменить в соответствии с вашими потребностями.</span><span class="sxs-lookup"><span data-stu-id="48d72-134">The Windows Server 2008 Security Guide at [https://go.microsoft.com/fwlink/p/?LinkId=145186](https://go.microsoft.com/fwlink/p/?linkid=145186) and the Windows Server 2008 R2 Security Compliance Management Toolkit at [https://go.microsoft.com/fwlink/p/?LinkId=211882](https://go.microsoft.com/fwlink/p/?linkid=211882) contain a number of sample templates that you can modify to meet your needs.</span></span>

</div>

<div>

## <a name="best-practices"></a><span data-ttu-id="48d72-135">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="48d72-135">Best Practices</span></span>

  - <span data-ttu-id="48d72-136">Зафиксированная защита всех серверных операционных систем и приложений.</span><span class="sxs-lookup"><span data-stu-id="48d72-136">Harden all server operating systems and applications.</span></span>

  - <span data-ttu-id="48d72-137">Защитите снимки сервера и повышайте безопасность всех виртуальных серверов.</span><span class="sxs-lookup"><span data-stu-id="48d72-137">Protect server snapshots and enhance the security of all virtual servers.</span></span>

  - <span data-ttu-id="48d72-138">Используйте групповую политику для реализации блокировки безопасности.</span><span class="sxs-lookup"><span data-stu-id="48d72-138">Use Group Policy to implement security lockdowns.</span></span>

<span data-ttu-id="48d72-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48d72-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

