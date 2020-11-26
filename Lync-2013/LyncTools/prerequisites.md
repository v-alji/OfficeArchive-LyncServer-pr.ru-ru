---
title: Необходимые компоненты
description: Требованиям.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prerequisites
ms:assetid: 48016bea-be3b-4ba5-8df8-d8ad4d9243d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945592(v=OCS.15)
ms:contentKeyID: 51541417
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 936e52961539ed57fe1b610d42fb1c9cf35589b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446413"
---
# <a name="prerequisites"></a><span data-ttu-id="a6f90-103">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="a6f90-103">Prerequisites</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6f90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6f90-104">

<span> </span></span></span>

<span data-ttu-id="a6f90-105">_**Тема последнего изменения:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="a6f90-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="a6f90-106">Существуют различные требования к оборудованию, программному обеспечению и конфигурации системы, которые необходимы для работы с инструментом "выгрузка и производительность" Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6f90-106">There are various hardware, software, and system configuration requirements that you’ll need to run the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="client-hardware-requirements"></a><span data-ttu-id="a6f90-107">Требования к оборудованию клиента</span><span class="sxs-lookup"><span data-stu-id="a6f90-107">Client Hardware Requirements</span></span>

<span data-ttu-id="a6f90-108">Для запуска средства нагрузки и производительности Lync Server 2013 в развертывании Lync Server 2013 для каждых пользователей 4 500 для каждого пользователя, у которого вы хотите смоделировать, вам потребуется по крайней мере один выделенный компьютер, отвечающий указанным ниже минимальным требованиям к оборудованию.</span><span class="sxs-lookup"><span data-stu-id="a6f90-108">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, for every 4,500 users whose load you want to simulate, you’ll need at least one dedicated computer that meets the following minimum hardware requirements:</span></span>

  - <span data-ttu-id="a6f90-109">гигабитный сетевой адаптер;</span><span class="sxs-lookup"><span data-stu-id="a6f90-109">1 gigabit network adapter</span></span>

  - <span data-ttu-id="a6f90-110">8 ГБ ОЗУ</span><span class="sxs-lookup"><span data-stu-id="a6f90-110">8-GB ram</span></span>

  - <span data-ttu-id="a6f90-111">два двухъядерных процессора (ЦП)</span><span class="sxs-lookup"><span data-stu-id="a6f90-111">2 dual-core central processing units (CPUs)</span></span>

</div>

<div>

## <a name="client-software-requirements"></a><span data-ttu-id="a6f90-112">Требования к клиентскому программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="a6f90-112">Client Software Requirements</span></span>

<span data-ttu-id="a6f90-113">Для запуска средства нагрузки и производительности Lync Server 2013 при развертывании Lync Server 2013 поддерживаются следующие операционные системы:</span><span class="sxs-lookup"><span data-stu-id="a6f90-113">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, the supported operating systems are:</span></span>

  - <span data-ttu-id="a6f90-114">Операционная система Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6f90-114">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="a6f90-115">Операционная система Windows Server 2008 (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="a6f90-115">Windows Server 2008 operating system (64-bit edition)</span></span>

<span data-ttu-id="a6f90-116">Клиентский компьютер должен соответствовать следующим требованиям к программному обеспечению:</span><span class="sxs-lookup"><span data-stu-id="a6f90-116">Your client computer must meet the following software requirements:</span></span>

  - <span data-ttu-id="a6f90-117">На вашем компьютере должна быть установлена среда выполнения [Microsoft .NET Framework 4,5](https://go.microsoft.com/fwlink/?linkid=143212) .</span><span class="sxs-lookup"><span data-stu-id="a6f90-117">You must have the [Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?linkid=143212) runtime installed.</span></span>

  - <span data-ttu-id="a6f90-118">В Windows Server 2008 и Windows Server 2012 функция "возможности рабочего стола" должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="a6f90-118">On Windows Server 2008/Windows Server 2012, the Desktop Experience feature must be enabled.</span></span>

  - <span data-ttu-id="a6f90-119">На вашем компьютере должен быть установлен [распространяемый пакет Microsoft Visual C++ 2012](https://go.microsoft.com/fwlink/?linkid=143216) (x64).</span><span class="sxs-lookup"><span data-stu-id="a6f90-119">You must have the [Microsoft Visual C++ 2012 redistributable package](https://go.microsoft.com/fwlink/?linkid=143216) (x64) installed.</span></span>

  - <span data-ttu-id="a6f90-120">Полностью настроенное развертывание Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6f90-120">A fully configured Lync Server 2013 deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a6f90-121">Библиотеки 4,0 API единой системы обмена сообщениями (UCMA) входят в пакет установки, поэтому UCMA не требуется и не должен устанавливаться на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="a6f90-121">Microsoft Unified Communications Managed API (UCMA) 4.0 libraries are included in the installation package, so UCMA is not required and should not be installed on client computers.</span></span>



</div>

</div>

<div>

## <a name="configuration-requirements"></a><span data-ttu-id="a6f90-122">Требования к конфигурации</span><span class="sxs-lookup"><span data-stu-id="a6f90-122">Configuration Requirements</span></span>

<span data-ttu-id="a6f90-123">Компьютеры, на которых будет работать средство нагрузки и производительности Lync Server 2013, должны быть настроены в соответствии с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="a6f90-123">The computers that will run the Lync Server 2013 Stress and Performance Tool must be configured according to the following requirements:</span></span>

1.  <span data-ttu-id="a6f90-124">Вы должны войти в систему как член группы домен или локальная группа администраторов.</span><span class="sxs-lookup"><span data-stu-id="a6f90-124">You must be logged on as a member of the Domain or Local Admins group.</span></span>

2.  <span data-ttu-id="a6f90-125">Инструмент Lync Server 2013 (LyncPerfTool.exe) не может быть запущен на компьютере, на котором также запущены компоненты Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6f90-125">Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) cannot be run on a computer that is also running Lync Server 2013 components.</span></span>

3.  <span data-ttu-id="a6f90-126">Вы должны запустить средство создания пользователей Lync Server 2013 (UserProvisioningTool.exe) на сервере переднего плана или на сервере Standard Edition, где будут храниться учетные записи пользователей.</span><span class="sxs-lookup"><span data-stu-id="a6f90-126">You must run the Lync Server 2013 User Creation tool (UserProvisioningTool.exe) on the Front End Server or on the Standard Edition server where the user accounts will reside.</span></span> <span data-ttu-id="a6f90-127">Если средство запускается несколько, каждый пользователь, для которого включена единая связь с Microsoft, должен иметь уникальный номер телефона.</span><span class="sxs-lookup"><span data-stu-id="a6f90-127">When the tool is run multiple times, each user who is enabled for Microsoft Unified Communications must have a unique phone number.</span></span>

4.  <span data-ttu-id="a6f90-128">Размер файла подкачки должен быть управляемым системой или не менее 1,5, чем объем оперативной памяти в системе.</span><span class="sxs-lookup"><span data-stu-id="a6f90-128">The page file size should be system-managed, or should be at least 1.5 times the amount of RAM on the system.</span></span>

<span data-ttu-id="a6f90-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6f90-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

