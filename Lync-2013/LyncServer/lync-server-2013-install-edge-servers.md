---
title: 'Lync Server 2013: установка пограничных серверов'
description: 'Lync Server 2013: Установка пограничных серверов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Edge Servers
ms:assetid: 1655ab69-3899-4ee4-a1cc-8243bc1bfa0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398230(v=OCS.15)
ms:contentKeyID: 48183503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e699a7f41b0ee554bc85fb2d9a72a2d9a42870cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427210"
---
# <a name="install-edge-servers-for-lync-server-2013"></a><span data-ttu-id="9e8ed-103">Установка пограничных серверов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e8ed-103">Install Edge Servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e8ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e8ed-104">

<span> </span></span></span>

<span data-ttu-id="9e8ed-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="9e8ed-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="9e8ed-106">Вы устанавливаете Lync Server 2013 на пограничные серверы с помощью мастера развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-106">You install Lync Server 2013 on Edge Servers by using Lync Server Deployment Wizard.</span></span> <span data-ttu-id="9e8ed-107">Запустив мастер развертывания на каждом пограничном сервере, вы можете выполнять большинство задач, необходимых для настройки пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-107">By running the Deployment Wizard on each Edge Server, you can complete most of the tasks required to set up the Edge Server.</span></span> <span data-ttu-id="9e8ed-108">Для развертывания Lync Server 2013 на пограничном сервере необходимо уже запустить построитель топологии, чтобы определить и опубликовать топологию пограничного сервера, а затем экспортировать его на носители, доступные на пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-108">In order to deploy Lync Server 2013 on an Edge Server, you must have already run Topology Builder to define and publish your Edge Server topology, and exported it to media that is available from the Edge Server.</span></span> <span data-ttu-id="9e8ed-109">Подробности можно найти [в разделе сценарии доступа внешних пользователей в Lync server 2013](lync-server-2013-scenarios-for-external-user-access.md) и [экспортировать топологию Lync Server 2013 и скопировать ее на внешние носители для установки пограничного сервера](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span><span class="sxs-lookup"><span data-stu-id="9e8ed-109">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<span data-ttu-id="9e8ed-110">После использования мастера развертывания для установки каждого пограничного сервера установите и назначьте необходимые сертификаты и запустите необходимые службы. Вы можете завершить настройку, используя сведения о [настройке поддержки внешних пользователей в Lync server 2013](lync-server-2013-configuring-support-for-external-user-access.md) для включения и настройки внешних пользователей, а также сведения о [проверке пограничного развертывания в Lync Server 2013](lync-server-2013-verifying-your-edge-deployment.md) для проверки настройки, включая подключение к серверу и клиенту.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-110">After using the Deployment Wizard to install each Edge Server, install and assign the required certificates, and start the required services, you can complete the setup by using the information in [Configuring support for external user access in Lync Server 2013](lync-server-2013-configuring-support-for-external-user-access.md) to enable and configure external user access and the information in [Verifying your edge deployment in Lync Server 2013](lync-server-2013-verifying-your-edge-deployment.md) to validate the setup, including server and client connectivity.</span></span>

<div>

## <a name="to-install-an-edge-server"></a><span data-ttu-id="9e8ed-111">Установка пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9e8ed-111">To install an Edge Server</span></span>

1.  <span data-ttu-id="9e8ed-112">Войдите в систему на компьютере, на котором вы хотите установить пограничный сервер, в группу локальных администраторов или в учетную запись с эквивалентными правами пользователей и разрешениями.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-112">Log on to the computer on which you want to install your Edge Server as a member of the local Administrators group or an account with equivalent user rights and permissions.</span></span>

2.  <span data-ttu-id="9e8ed-113">Убедитесь, что файл конфигурации топологии, созданный с помощью Topology Builder, а затем экспортирован и скопирован на внешний носитель, доступен на пограничном сервере (например, доступ к USB-диску, на который вы скопировали файл конфигурации топологии, или проверка доступа к сетевой папке, в которую вы скопировали файл).</span><span class="sxs-lookup"><span data-stu-id="9e8ed-113">Ensure that the topology configuration file you created using Topology Builder, and then exported and copied to external media, is available on the Edge Server (for example, access to the USB drive onto which you copied the topology configuration file, or verify access to the network share where you copied the file).</span></span>

3.  <span data-ttu-id="9e8ed-114">Запустите мастер развертывания.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-114">Start the Deployment Wizard.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9e8ed-115">Если вы получили сообщение о том, что вам нужно установить распространяемый компонент Microsoft Visual C++, нажмите кнопку <STRONG>Да</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-115">If you get a message saying that you need to install Microsoft Visual C++ Redistributable, click <STRONG>Yes</STRONG>.</span></span> <span data-ttu-id="9e8ed-116">В следующем диалоговом окне вы можете оставить <STRONG>расположение для установки</STRONG> по умолчанию или нажать кнопку <STRONG>Обзор</STRONG> , чтобы выбрать другое расположение, а затем нажать кнопку <STRONG>установить</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-116">In the next dialog box, you can accept the default <STRONG>Installation Location</STRONG> or click the <STRONG>Browse</STRONG> to select an alternate location, and then click <STRONG>Install</STRONG>.</span></span> <span data-ttu-id="9e8ed-117">В следующем диалоговом окне установите флажок <STRONG>я принимаю условия лицензионного соглашения</STRONG> и нажмите кнопку <STRONG>ОК</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-117">In the next dialog box, select the <STRONG>I accept the terms in the license agreement</STRONG> check box, and then click <STRONG>OK</STRONG>.</span></span>

    
    </div>

4.  <span data-ttu-id="9e8ed-118">В мастере развертывания нажмите кнопку **Установка или обновление системы Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-118">In the Deployment Wizard, click **Install or Update Lync Server System**.</span></span>

5.  <span data-ttu-id="9e8ed-119">После того как мастер определит состояние развертывания, для **шага 1. Установите локальное хранилище конфигураций**, нажмите кнопку **выполнить** , а затем выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-119">After the wizard determines the deployment state, for **Step 1. Install Local Configuration Store**, click **Run** and then do the following:</span></span>
    
      - <span data-ttu-id="9e8ed-120">В диалоговом окне **Настройка локальной реплики центрального хранилища Central Management** выберите **Импорт из файла (рекомендуется для пограничных серверов)**, перейдите в папку, в которой находится экспортированный файл конфигурации топологии, выберите ZIP-файл, нажмите кнопку **Открыть** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-120">In the **Configure Local Replica of Central Management Store** dialog box, click **Import from a file (Recommended for Edge Servers)**, go to the location of the exported topology configuration file, select the .zip file, click **Open**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="9e8ed-121">Мастер развертывания считывает сведения о конфигурации из файла конфигурации и записывает XML-файл конфигурации на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-121">The Deployment Wizard reads the configuration information from the configuration file and writes the XML configuration file to the local computer.</span></span>
    
      - <span data-ttu-id="9e8ed-122">После завершения процесса **выполнения команд** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-122">After the **Executing Commands** process is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="9e8ed-123">В мастере развертывания выберите **Шаг 2: Настройка или удаление компонентов Lync** Server, чтобы установить компоненты lync Server 2013, указанные в XML-файле конфигурации, который хранится на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-123">In the Deployment Wizard, click **Step 2: SetUp or Remove Lync Server Components** to install the Lync Server 2013 edge components specified in the XML configuration file that is stored on the local computer.</span></span>

7.  <span data-ttu-id="9e8ed-124">После завершения установки используйте сведения в разделе [Настройка сертификатов Edge для Lync Server 2013](lync-server-2013-set-up-edge-certificates.md) , чтобы установить и назначить необходимые сертификаты перед запуском служб.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-124">After completing the installation, use the information in [Set up Edge certificates for Lync Server 2013](lync-server-2013-set-up-edge-certificates.md) to install and assign the required certificates before you start services.</span></span>

<span data-ttu-id="9e8ed-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e8ed-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

