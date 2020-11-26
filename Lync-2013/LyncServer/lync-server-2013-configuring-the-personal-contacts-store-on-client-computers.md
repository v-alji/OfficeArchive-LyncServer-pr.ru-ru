---
title: 'Lync Server 2013: Настройка хранилища личных контактов на клиентских компьютерах'
description: 'Lync Server 2013: Настройка хранилища личных контактов на клиентских компьютерах.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the personal contacts store on client computers
ms:assetid: ec69a6cb-07f2-4057-9544-55035f83eeae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721922(v=OCS.15)
ms:contentKeyID: 49733857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1040b3eb9aa38e3e0c537d690b9292ab8f1ead2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432522"
---
# <a name="configuring-the-personal-contacts-store-on-client-computers-for-lync-server-2013"></a><span data-ttu-id="acca3-103">Настройка хранилища личных контактов на клиентских компьютерах для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="acca3-103">Configuring the personal contacts store on client computers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="acca3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="acca3-104">

<span> </span></span></span>

<span data-ttu-id="acca3-105">_**Тема последнего изменения:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="acca3-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="acca3-106">При интеграции Microsoft Lync Server 2013 и Microsoft Exchange Server 2013 рекомендуется настроить хранилище персональных контактов на любом клиентском компьютере, работающем под управлением Microsoft Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="acca3-106">If you are integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013 then it is recommended that you configure the personal contact store on any client computers running Microsoft Lync 2010.</span></span> <span data-ttu-id="acca3-107">В частности, вы должны настроить Lync для использования Exchange в качестве личного хранилища контактов и, в то же время, убедиться, что пользователи не могут переопределять это решение.</span><span class="sxs-lookup"><span data-stu-id="acca3-107">In particular, you should configure Lync to use Exchange as the personal contact store, and, at the same time, ensure that users are not able to override that decision.</span></span> <span data-ttu-id="acca3-108">Это можно сделать, создав и настроив значение реестра на каждом клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="acca3-108">This can be done by creating and configuring a Registry value on each client computer.</span></span>

<span data-ttu-id="acca3-109">Обратите внимание, что это не требуется на компьютерах с Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="acca3-109">Note that this is not required on computers running Lync 2013.</span></span>

<span data-ttu-id="acca3-110">Чтобы настроить данное значение на одном компьютере, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="acca3-110">To configure this value on a single computer, complete the following procedure:</span></span>

1.  <span data-ttu-id="acca3-111">На клиентском компьютере нажмите кнопку **Пуск** и выберите команду **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="acca3-111">On the client computer, click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="acca3-112">В диалоговом окне **Выполнить** введите regedit, а затем нажмите ВВОД.</span><span class="sxs-lookup"><span data-stu-id="acca3-112">In the **Run** dialog box, type regedit and then press ENTER.</span></span>

3.  <span data-ttu-id="acca3-113">В редакторе реестра разверните узел **hKey \_ локального \_ компьютера**, разверните раздел **программы**, **а затем разверните** раздел **Microsoft**, а затем — **Communicator**.</span><span class="sxs-lookup"><span data-stu-id="acca3-113">In Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **Software**, expand **Policies**, expand **Microsoft**, and then expand **Communicator**.</span></span>

4.  <span data-ttu-id="acca3-114">Щелкните элемент **Communicator** правой кнопкой мыши, наведите указатель на пункт **Создать** и выберите пункт **Параметр DWORD (32-разрядный)**.</span><span class="sxs-lookup"><span data-stu-id="acca3-114">Right-click **Communicator**, point to **New**, and then click **DWORD (32-bit) Value**.</span></span>

5.  <span data-ttu-id="acca3-115">После создания параметра введите **PersonalContactStoreOverride** и нажмите клавишу ВВОД, чтобы переименовать параметр.</span><span class="sxs-lookup"><span data-stu-id="acca3-115">After the new value is created, type **PersonalContactStoreOverride** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="acca3-116">Убедитесь, что значение PersonalContactStoreOverride равно 0, а затем закройте редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="acca3-116">Verify that the value of PersonalContactStoreOverride is set to 0 and then close Registry Editor.</span></span>

<span data-ttu-id="acca3-117">Если нужно внести это изменение на нескольких компьютерах, это можно сделать, создав пользовательский объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="acca3-117">If you need to make this same change on multiple computers you can do so by creating a custom Group Policy object.</span></span> <span data-ttu-id="acca3-118">Подробные сведения можно найти в документации по групповой политике [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543) .</span><span class="sxs-lookup"><span data-stu-id="acca3-118">For details, see the Group Policy documentation at [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543).</span></span>

<span data-ttu-id="acca3-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="acca3-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

