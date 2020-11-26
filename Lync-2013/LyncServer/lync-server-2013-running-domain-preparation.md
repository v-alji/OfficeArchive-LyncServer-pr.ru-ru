---
title: 'Lync Server 2013: проведение подготовки домена'
description: 'Lync Server 2013: выполнение подготовки домена.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running domain preparation
ms:assetid: 95dab800-1f2c-4506-b36c-99986643b149
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398761(v=OCS.15)
ms:contentKeyID: 48184847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f2c4ebe94d07ed2d1fd9be013cd8e88204312f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442259"
---
# <a name="running-domain-preparation-for-lync-server-2013"></a><span data-ttu-id="05e3e-103">Проведение подготовки домена для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="05e3e-103">Running domain preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="05e3e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="05e3e-104">

<span> </span></span></span>

<span data-ttu-id="05e3e-105">_**Тема последнего изменения:** 2013-04-16_</span><span class="sxs-lookup"><span data-stu-id="05e3e-105">_**Topic Last Modified:** 2013-04-16_</span></span>

<span data-ttu-id="05e3e-106">Для подготовки доменов можно использовать командлеты командной консоли Setup или Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="05e3e-106">You can use Setup or Lync Server Management Shell cmdlets to prepare domains.</span></span> <span data-ttu-id="05e3e-107">Командлет, подготавливающий домен, — **Enable-CsAdDomain**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-107">The cmdlet that prepares a domain is **Enable-CsAdDomain**.</span></span>

<span data-ttu-id="05e3e-108">Подготовка домена — это заключительный этап подготовки доменных служб Active Directory для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="05e3e-108">Domain preparation is the final step in preparing Active Directory Domain Services for Lync Server 2013.</span></span>

<div>

## <a name="to-use-setup-to-prepare-domains"></a><span data-ttu-id="05e3e-109">Использование программы установки для подготовки доменов</span><span class="sxs-lookup"><span data-stu-id="05e3e-109">To use Setup to prepare domains</span></span>

1.  <span data-ttu-id="05e3e-110">Войдите на любой сервер домена, который является членом группы "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="05e3e-110">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="05e3e-111">В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="05e3e-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>

3.  <span data-ttu-id="05e3e-112">Нажмите **Подготовить Active Directory** и подождите, пока будет определено состояние развертывания.</span><span class="sxs-lookup"><span data-stu-id="05e3e-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="05e3e-113">Когда появится окно **Шаг 5. Подготовка текущего домена**, нажмите кнопку **Запустить**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-113">At **Step 5: Prepare Current Domain**, click **Run**.</span></span>

5.  <span data-ttu-id="05e3e-114">На странице **Подготовка домена** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-114">On the **Prepare Domain** page, click **Next**.</span></span>

6.  <span data-ttu-id="05e3e-115">На странице **выполнения команд** подождите, пока не появится сообщение **Состояние задачи: Завершено**, а затем нажмите **Просмотреть журнал**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-115">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="05e3e-116">В столбце **Action (действие** ) разверните **доменную версию домена**, найдите **\<Success\>** результаты выполнения в конце каждой задачи, чтобы убедиться в том, что подготовка домена успешно завершена, закройте журнал и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-116">Under the **Action** column, expand **Domain Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that domain preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="05e3e-117">Дождитесь завершения репликации Active Directory или принудительно выполните репликацию на все контроллеры домена, указанные в оснастке "сайты и службы" Active Directory для корневого контроллера домена леса.</span><span class="sxs-lookup"><span data-stu-id="05e3e-117">Wait for Active Directory replication to complete or force replication to all the domain controllers listed in the Active Directory Sites and Services snap-in for the forest root domain controller.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-domain"></a><span data-ttu-id="05e3e-118">Использование командлетов для подготовки домена</span><span class="sxs-lookup"><span data-stu-id="05e3e-118">To use cmdlets to prepare the domain</span></span>

1.  <span data-ttu-id="05e3e-119">Войдите на любой сервер домена, который является членом группы "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="05e3e-119">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="05e3e-120">Установите основные компоненты Lync Server, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="05e3e-120">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="05e3e-121">В установочной папке или носителе для Lync Server 2013 выполните Setup.exe, чтобы запустить мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="05e3e-121">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="05e3e-122">Если вам будет предложено установить распространяемый компонент Microsoft Visual C++, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-122">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="05e3e-123">Диалоговое окно установки Lync Server 2013 предлагает указать расположение для установки файлов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="05e3e-123">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="05e3e-124">Выберите расположение по умолчанию или **перейдите** в нужное место, а затем нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-124">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="05e3e-125">На странице Лицензионное соглашение установите флажок **я принимаю условия лицензионного соглашения**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-125">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="05e3e-126">Установщик установит основные компоненты Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="05e3e-126">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="05e3e-127">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="05e3e-127">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="05e3e-128">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="05e3e-128">Run:</span></span>
    
        Enable-CsAdDomain [-Domain <DomainFQDN>] 
    
    <span data-ttu-id="05e3e-129">Например:</span><span class="sxs-lookup"><span data-stu-id="05e3e-129">For example:</span></span>
    
        Enable-CsAdDomain -Domain domain1.contoso.net 
    
    <span data-ttu-id="05e3e-130">Если параметр Domain не указан, по умолчанию используется локальный домен.</span><span class="sxs-lookup"><span data-stu-id="05e3e-130">If you do not specify the Domain parameter, the default is the local domain.</span></span>

5.  <span data-ttu-id="05e3e-131">Убедитесь, что подготовка домена выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="05e3e-131">Verify that domain preparation was successful.</span></span> <span data-ttu-id="05e3e-132">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="05e3e-132">Run:</span></span>
    
        Get-CsAdDomain [-Domain <Domain FQDN>] [-DomainController <Domain controller FQDN>] [-GlobalCatalog <Global catalog server FQDN>] [-GlobalSettingsDomainController <Domain controller FQDN where global settings are stored>] 
    
    <span data-ttu-id="05e3e-133">Например:</span><span class="sxs-lookup"><span data-stu-id="05e3e-133">For example:</span></span>
    
        Get-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.com
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="05e3e-134">Параметр GlobalSettingsDomainController позволяет указать, где хранятся глобальные параметры.</span><span class="sxs-lookup"><span data-stu-id="05e3e-134">The parameter GlobalSettingsDomainController allows you to indicate where global settings are stored.</span></span> <span data-ttu-id="05e3e-135">Если параметры хранятся в системном контейнере (обычно при развертывании обновлений без глобальных параметров, перенесенных в контейнер), вы определяете контроллер домена в корне леса Active Directory.</span><span class="sxs-lookup"><span data-stu-id="05e3e-135">If your settings are stored in the System container (which is typical with upgrade deployments that have not had the global settings migrated to the Configuration container), you define a domain controller in the root of your Active Directory forest.</span></span> <span data-ttu-id="05e3e-136">Если глобальные параметры хранятся в контейнере Configuration (это обычная ситуация для новых развертываний или обновленных развертываний, в которых параметры перенесены в контейнер Configuration), определите любой контроллер домена в лесу.</span><span class="sxs-lookup"><span data-stu-id="05e3e-136">If the global settings are in the Configuration container (which is typical with new deployments or upgrade deployments where the settings have been migrated to the Configuration container), you define any domain controller in the forest.</span></span> <span data-ttu-id="05e3e-137">Если этот параметр не указан, командлет предполагает, что параметры хранятся в контейнере конфигурации и ссылаются на любой контроллер домена в доменных &nbsp; службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="05e3e-137">If you do not specify this parameter, the cmdlet assumes that the settings are stored in the Configuration container and refers to any domain controller in AD&nbsp;DS.</span></span>

    
    </div>
    
    <span data-ttu-id="05e3e-138">Если параметр **domain** не указан, по умолчанию используется локальный домен.</span><span class="sxs-lookup"><span data-stu-id="05e3e-138">If you do not specify the **Domain** parameter, the default is the local domain.</span></span>
    
    <span data-ttu-id="05e3e-139">Этот командлет возвращает значение **\_ DOMAINSETTINGS \_ состояния \_ "LC** ", если подготовка домена выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="05e3e-139">This cmdlet returns a value of **LC\_DOMAINSETTINGS\_STATE\_READY** if domain preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="05e3e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="05e3e-140">See Also</span></span>


[<span data-ttu-id="05e3e-141">Использование командлетов для отмены подготовки доменов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="05e3e-141">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)  


[<span data-ttu-id="05e3e-142">Подготовка доменов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="05e3e-142">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="05e3e-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="05e3e-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

