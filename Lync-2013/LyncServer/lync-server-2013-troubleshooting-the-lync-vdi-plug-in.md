---
title: 'Lync Server 2013: Устранение неполадок с внешним модулем VDI Lync'
description: 'Lync Server 2013: Устранение неполадок с внешним модулем VDI Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting the Lync VDI plug-in
ms:assetid: 183c9449-b907-409c-b5ed-b02af3bd93ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204713(v=OCS.15)
ms:contentKeyID: 48183525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cd2c0e3c8a47225f00ce280706dea2287e4dc8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398683"
---
# <a name="troubleshooting-the-lync-vdi-plug-in-in-lync-server-2013"></a><span data-ttu-id="05988-103">Устранение неполадок с внешним модулем Lync VDI в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="05988-103">Troubleshooting the Lync VDI plug-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="05988-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="05988-104">

<span> </span></span></span>

<span data-ttu-id="05988-105">_**Тема последнего изменения:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="05988-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<div>

## <a name="troubleshooting-issues-with-installing-the-lync-vdi-plug-in-on-a-thin-client"></a><span data-ttu-id="05988-106">Устранение неполадок, возникающих при установке плагина Lync VDI на тонком клиенте</span><span class="sxs-lookup"><span data-stu-id="05988-106">Troubleshooting Issues with Installing the Lync VDI Plug-in on a Thin Client</span></span>

<span data-ttu-id="05988-107">Если у вас возникли проблемы при установке надстройки VDI на тонком клиенте, проверьте следующее:</span><span class="sxs-lookup"><span data-stu-id="05988-107">If there are issues with installing the VDI plug-in on a thin client, check the following:</span></span>

  - <span data-ttu-id="05988-108">Убедитесь в наличии достаточного свободного пространства в папке, указанной в системных переменных TEMP и TMP.</span><span class="sxs-lookup"><span data-stu-id="05988-108">Ensure that there is sufficient space in the folder that you specified in the TEMP and TMP system variables.</span></span>

  - <span data-ttu-id="05988-p101">Убедитесь в том, что защита от записи отключена. Инструкции см. в документации, предоставленной производителем устройства.</span><span class="sxs-lookup"><span data-stu-id="05988-p101">Ensure that write-protect is turned off. Refer to your device manufacturer’s documentation for instructions.</span></span>

</div>

<div>

## <a name="troubleshooting-issues-with-pairing"></a><span data-ttu-id="05988-111">Устранение неполадок сопряжения</span><span class="sxs-lookup"><span data-stu-id="05988-111">Troubleshooting Issues with Pairing</span></span>

<span data-ttu-id="05988-112">При возникновении ошибки связывания с внешним подключением VDI значок связывания в правом нижнем углу отображается как красный крестик, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="05988-112">When VDI plug-in pairing fails, the pairing icon in the lower right displays as a red “X” as shown:</span></span>

<span data-ttu-id="05988-113">![Значок Lync VDI, показывающий успешное связывание](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Значок Lync VDI, показывающий успешное связывание")</span><span class="sxs-lookup"><span data-stu-id="05988-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>

<span data-ttu-id="05988-114">Ниже приведены возможные причины сбоя и действия по их исправлению.</span><span class="sxs-lookup"><span data-stu-id="05988-114">The following are possible reasons for failures and the corrective actions you can take.</span></span>

  - <span data-ttu-id="05988-115">**Пользователем введены неправильные учетные данные при входе в систему.**</span><span class="sxs-lookup"><span data-stu-id="05988-115">**The user entered incorrect credentials during sign-in.**</span></span>
    
    <span data-ttu-id="05988-116">Пользователь должен выйти из Lync и войти в систему с правильными учетными данными.</span><span class="sxs-lookup"><span data-stu-id="05988-116">The user should sign out of Lync and sign in again with the correct credentials.</span></span> <span data-ttu-id="05988-117">В повторно открывшемся диалоговом окне отобразится уведомление об успешном сопряжении.</span><span class="sxs-lookup"><span data-stu-id="05988-117">The pairing dialog box will reappear and show whether pairing is successful.</span></span>

  - <span data-ttu-id="05988-118">**Выполняется другой экземпляр клиента удаленного рабочего стола.**</span><span class="sxs-lookup"><span data-stu-id="05988-118">**Another instance of the remote desktop client is running.**</span></span>
    
    <span data-ttu-id="05988-119">Если они используют подключение к удаленному рабочему столу в Windows, пользователи должны выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="05988-119">If they are using Remote Desktop Connection in Windows, users should do the following:</span></span>
    
    1.  <span data-ttu-id="05988-120">Запустите диспетчер задач: нажмите клавиши **ALT+CTRL+DELETE** и выберите пункт **Запустить диспетчер задач**.</span><span class="sxs-lookup"><span data-stu-id="05988-120">Start Task Manager: Press **Alt+Ctrl+Delete**, and then click **Start Task Manager**.</span></span>
    
    2.  <span data-ttu-id="05988-121">Перейдите на вкладку **Процессы** и найдите все процессы с именем **mstsc.exe** в списке.</span><span class="sxs-lookup"><span data-stu-id="05988-121">Click the **Processes** tab and look for all processes named **mstsc.exe** in the list.</span></span>
    
    3.  <span data-ttu-id="05988-122">Выделите каждый процесс **mstsc.exe** и нажмите кнопку **Завершить процесс**. </span><span class="sxs-lookup"><span data-stu-id="05988-122">Highlight each **mstsc.exe** process and then click **End Process**.</span></span>
    
    4.  <span data-ttu-id="05988-123">Запустите новый сеанс удаленного рабочего стола и повторите попытку подключения. </span><span class="sxs-lookup"><span data-stu-id="05988-123">Start a new remote desktop session and try connecting again.</span></span>

  - <span data-ttu-id="05988-124">**Не удалось установить необходимые файлы.**</span><span class="sxs-lookup"><span data-stu-id="05988-124">**The necessary files did not install correctly.**</span></span>
    
    <span data-ttu-id="05988-125">После того как плагин установлен на локальном компьютере, в разделе C: \\ Program Files \\ Microsoft Office \\ Office15 (или соответствующую букву диска) должны быть указаны следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="05988-125">After the plug-in is installed on the local computer, the following files should be present under C:\\Program Files\\Microsoft Office\\Office15 (or the appropriate drive letter):</span></span>
    
      - <span data-ttu-id="05988-126">LyncVdiPlugin.dll</span><span class="sxs-lookup"><span data-stu-id="05988-126">LyncVdiPlugin.dll</span></span>
    
      - <span data-ttu-id="05988-127">UcVdi.dll</span><span class="sxs-lookup"><span data-stu-id="05988-127">UcVdi.dll</span></span>
    
    <span data-ttu-id="05988-128">Если при связывании с помощью VDI возникли проблемы, убедитесь, что эти файлы находятся на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="05988-128">If there are any issues with VDI pairing, check to make sure that these files are present on the local computer.</span></span>

  - <span data-ttu-id="05988-129">**Клиент Lync запущен на локальном компьютере.**</span><span class="sxs-lookup"><span data-stu-id="05988-129">**The Lync client is running on the local computer.**</span></span>
    
    <span data-ttu-id="05988-130">Чтобы использовать подключаемый модуль VDI Lync, клиент Lync не должен выполняться на локальном компьютере, в противном случае связывание завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="05988-130">To use the Lync VDI plugin, a Lync client must not be running on the local computer, otherwise pairing will fail.</span></span> <span data-ttu-id="05988-131">Рекомендуется не устанавливать клиент Lync на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="05988-131">As a best practice, the user should not install a Lync client on the local computer.</span></span>

<span data-ttu-id="05988-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="05988-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

