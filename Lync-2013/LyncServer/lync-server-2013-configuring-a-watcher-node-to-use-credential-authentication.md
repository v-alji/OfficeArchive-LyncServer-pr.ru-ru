---
title: 'Lync Server 2013: Настройка узла-наблюдателя для использования проверки подлинности учетных данных'
description: 'Lync Server 2013: Настройка узла-наблюдателя для использования проверки подлинности учетных данных.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to use credential authentication
ms:assetid: 032e33f3-9483-42e6-a33c-347eb6779597
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204632(v=OCS.15)
ms:contentKeyID: 48183255
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b65d4e3f90b27aac69b8569472ac9896766e093e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433446"
---
# <a name="configuring-a-watcher-node-to-use-credential-authentication-in-lync-server-2013"></a><span data-ttu-id="e1fb2-103">Настройка узла-наблюдателя для использования проверки подлинности учетных данных в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1fb2-103">Configuring a watcher node to use credential authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1fb2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1fb2-104">

<span> </span></span></span>

<span data-ttu-id="e1fb2-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="e1fb2-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="e1fb2-106">Если ваш компьютер-наблюдатель находится за пределами периметра сети, необходимо выполнить несколько других действий, чтобы настроить этот узел-наблюдатель для выполнения искусственных транзакций.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-106">If your watcher node computer lies outside the perimeter network, then you must follow a slightly different procedure in order to configure that watcher node to run synthetic transactions.</span></span> <span data-ttu-id="e1fb2-107">В частности, не следует создавать доверенный пул приложений и надежное приложение, и необходимо установить сертификат, который позволит узлу-наблюдателю отправлять оповещения на компьютер в демилитаризованной зоне.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-107">Specifically, you should not create a trusted application pool and a trusted application, and you must install a certificate that enables the watcher node to send alerts to a computer inside the perimeter network.</span></span> <span data-ttu-id="e1fb2-108">Это означает, что вам потребуется выполнить две отдельные задачи:</span><span class="sxs-lookup"><span data-stu-id="e1fb2-108">This means that you will need to complete two separate tasks:</span></span>

  - <span data-ttu-id="e1fb2-109">Обновление сведений о членстве в локальной группе администраторов, доступной только для чтения на компьютере реального времени</span><span class="sxs-lookup"><span data-stu-id="e1fb2-109">Update the membership in the computer's RTC Local Read-only Administrators Group</span></span>

  - <span data-ttu-id="e1fb2-110">Установка файлов конфигурации узла-наблюдателя</span><span class="sxs-lookup"><span data-stu-id="e1fb2-110">Install the watcher node configuration files</span></span>

<div>

## <a name="updating-membership-in-the-rtc-local-read-only-administrators-group"></a><span data-ttu-id="e1fb2-111">Обновление сведений о членстве в локальной группе администраторов Read-Only администратора часов</span><span class="sxs-lookup"><span data-stu-id="e1fb2-111">Updating Membership in the RTC Local Read-Only Administrators Group</span></span>

<span data-ttu-id="e1fb2-112">Если узел-наблюдатель находится за пределами периметра сети, необходимо добавить учетную запись Network Service в группу локальных администраторов локального администратора на компьютере с узлом-наблюдателем.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-112">If your watcher node lies outside the perimeter network, you must add the Network Service account to the RTC Local Read-only Administrators group on the watcher node computer.</span></span> <span data-ttu-id="e1fb2-113">Для этого выполните указанные ниже действия на узле "наблюдатель".</span><span class="sxs-lookup"><span data-stu-id="e1fb2-113">To do this, complete the following procedure on the watcher node:</span></span>

1.  <span data-ttu-id="e1fb2-114">Нажмите кнопку **Пуск**, щелкните правой кнопкой мыши пункт **компьютер**, а затем выберите пункт **Управление**.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-114">Click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="e1fb2-115">В диспетчере серверов разверните узел **Конфигурация**, разверните раздел **Локальные пользователи и группы**, а затем выберите пункт **группы**.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-115">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="e1fb2-116">В области группы дважды щелкните **Локальные администраторы реального времени**, предназначенные только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-116">In the Groups pane, double-click **RTC Local Read-only Administrators**.</span></span>

4.  <span data-ttu-id="e1fb2-117">В диалоговом окне **Свойства локального администратора RTC "только для чтения** " нажмите кнопку " **Добавить**".</span><span class="sxs-lookup"><span data-stu-id="e1fb2-117">In the **RTC Local Read-only Administrators Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="e1fb2-118">В диалоговом окне **выберите пользователей, компьютеры, учетные записи служб или группы** нажмите кнопку **места**.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-118">In the **Select Users, Computers, Service Accounts, or Groups** dialog box, click **Locations**.</span></span>

6.  <span data-ttu-id="e1fb2-119">В диалоговом окне **расположения** выберите имя компьютера с узлом-наблюдателем и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-119">In the **Locations** dialog box, select the name of the watcher node computer, and then click **OK**.</span></span>

7.  <span data-ttu-id="e1fb2-120">В поле **Введите имена объектов для выбора** введите **Сетевая служба** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-120">In the **Enter object names to select** box, type **Network Service**, and then click **OK**.</span></span>

8.  <span data-ttu-id="e1fb2-121">В диалоговом окне **свойства локальных администраторов RTC только для чтения** нажмите кнопку **ОК**, а затем закройте **Диспетчер серверов**.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-121">In the **RTC Local Read-only Administrators Properties** dialog box, click **OK**, and then close **Server Manager**.</span></span>

<span data-ttu-id="e1fb2-122">Перезапустите компьютер-узел-наблюдатель.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-122">Restart the watcher node computer.</span></span>

</div>

<div>

## <a name="installing-the-watcher-node-configuration-files"></a><span data-ttu-id="e1fb2-123">Установка файлов конфигурации узла-наблюдателя</span><span class="sxs-lookup"><span data-stu-id="e1fb2-123">Installing the Watcher Node Configuration Files</span></span>

<span data-ttu-id="e1fb2-124">После перезапуска компьютера узла-наблюдателя вы должны запустить файл Watchernode.msi.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-124">After the watcher node computer has restarted, your next step is to run the file Watchernode.msi.</span></span> <span data-ttu-id="e1fb2-125">Чтобы запустить этот файл, откройте командную консоль Lync Server 2013, нажмите кнопку **Пуск**, выберите пункт **все программы**, затем — **Lync Server 2013** и щелкните **Командная консоль управления Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-125">To run this file, open the Lync Server 2013 Management Shell by clicking **Start**, clicking **All Programs**, clicking **Lync Server 2013**, and then clicking **Lync Server Management Shell**.</span></span> <span data-ttu-id="e1fb2-126">В командной консоли Lync Server введите указанную ниже команду и нажмите клавишу ВВОД (укажите фактический путь к копии Watchernode.msi):</span><span class="sxs-lookup"><span data-stu-id="e1fb2-126">In the Lync Server Management Shell, type the following command and then press ENTER (be sure and specify the actual path to your copy of Watchernode.msi):</span></span>

    C:\Tools\Watchernode.msi Authentication=Negotiate

<div>


> [!NOTE]  
> <span data-ttu-id="e1fb2-127">Как отмечалось ранее, Watchernode.msi также можно выполнить в командном окне.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-127">As noted previously, Watchernode.msi can also be run from a command window.</span></span> <span data-ttu-id="e1fb2-128">Чтобы открыть командное окно, нажмите кнопку <STRONG>Пуск</STRONG>, щелкните правой кнопкой мыши <STRONG>Командная строка</STRONG>и выберите пункт <STRONG>Запуск от имени администратора</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-128">To open a command window, click <STRONG>Start</STRONG>, right-click <STRONG>Command Prompt</STRONG>, and then click <STRONG>Run as administrator</STRONG>.</span></span> <span data-ttu-id="e1fb2-129">Когда откроется окно команд, введите ту же команду, которая была показана выше.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-129">When the command window opens, type the same command as shown earlier.</span></span>



</div>

<span data-ttu-id="e1fb2-130">Режим согласования используется в любой момент времени, когда узел-наблюдатель не может быть настроен как доверенный пул приложений.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-130">The Negotiate mode is used any time the watcher node cannot be set up as a trusted application pool.</span></span> <span data-ttu-id="e1fb2-131">В этом режиме администраторам нужно будет управлять тестовыми паролями пользователей в узле "наблюдатель".</span><span class="sxs-lookup"><span data-stu-id="e1fb2-131">In this mode, administrators will need to manage test user passwords on the watcher node.</span></span>

<span data-ttu-id="e1fb2-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1fb2-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

