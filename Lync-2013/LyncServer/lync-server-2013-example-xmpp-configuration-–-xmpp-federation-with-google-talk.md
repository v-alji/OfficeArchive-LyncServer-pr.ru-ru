---
title: Пример конфигурации XMPP – федерация XMPP с Google Talk
description: Пример настройки XMPP – XMPP Federation в Google поговорить.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428454"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a><span data-ttu-id="911f0-103">Пример конфигурации XMPP в Lync Server 2013 — федерация XMPP с Google Talk</span><span class="sxs-lookup"><span data-stu-id="911f0-103">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="911f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="911f0-104">

<span> </span></span></span>

<span data-ttu-id="911f0-105">_**Тема последнего изменения:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="911f0-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="911f0-106">Пример конфигурации для развертывания прокси-сервера XMPP определяет Федерацию с использованием Google разговора.</span><span class="sxs-lookup"><span data-stu-id="911f0-106">An example configuration for deploying the XMPP Proxy defines a federation with Google Talk.</span></span>

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a><span data-ttu-id="911f0-107">Пример конфигурации XMPP – федерация XMPP с Google Talk</span><span class="sxs-lookup"><span data-stu-id="911f0-107">Example XMPP configuration – XMPP federation with Google Talk</span></span>

1.  <span data-ttu-id="911f0-108">На сервере переднего плана откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="911f0-108">On the Front End Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="911f0-109">Щелкните **Установка** или **обновление операционной системы Lync Server**, а затем нажмите кнопку **Настройка** или **удалите компоненты Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="911f0-109">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="911f0-110">Нажмите кнопку **выполнить еще раз**.</span><span class="sxs-lookup"><span data-stu-id="911f0-110">Click **Run Again**.</span></span>

2.  <span data-ttu-id="911f0-111">В разделе **Настройка серверных компонентов Lync** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="911f0-111">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="911f0-112">На экране сводки будут показаны действия по мере их выполнения.</span><span class="sxs-lookup"><span data-stu-id="911f0-112">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="911f0-113">После завершения развертывания щелкните **Просмотреть журнал** , чтобы просмотреть доступные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="911f0-113">After the deployment is complete, click **View Log** to view available log files.</span></span> <span data-ttu-id="911f0-114">Нажмите кнопку **Готово** , чтобы завершить развертывание.</span><span class="sxs-lookup"><span data-stu-id="911f0-114">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="911f0-115">На пограничном сервере откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="911f0-115">On the Edge Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="911f0-116">Щелкните **Установка** или **обновление операционной системы Lync Server**, а затем нажмите кнопку **Настройка** или **удалите компоненты Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="911f0-116">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="911f0-117">Нажмите кнопку **выполнить еще раз**.</span><span class="sxs-lookup"><span data-stu-id="911f0-117">Click **Run Again**.</span></span>

4.  <span data-ttu-id="911f0-118">Добавьте Google поговорить в качестве XMPP разрешенного партнера.</span><span class="sxs-lookup"><span data-stu-id="911f0-118">Add Google Talk as an XMPP allowed partner.</span></span> <span data-ttu-id="911f0-119">В настоящее время Google поговорить поддерживает только нешифрованные подключения по протоколу TCP для сервера федерации XMPP и поддерживает только Dialback сервера для проверки личности.</span><span class="sxs-lookup"><span data-stu-id="911f0-119">Google Talk currently only supports unencrypted, TCP connections for server-to-server XMPP federation and only supports Server Dialback for identity verification.</span></span> <span data-ttu-id="911f0-120">(См <http://xmpp.org/extensions/xep-0220.html> .).</span><span class="sxs-lookup"><span data-stu-id="911f0-120">(See <http://xmpp.org/extensions/xep-0220.html>).</span></span>
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  <span data-ttu-id="911f0-121">Чтобы включить пограничный Федерацию, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="911f0-121">To enable Edge Federation, type the following:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  <span data-ttu-id="911f0-122">В разделе **Настройка серверных компонентов Lync** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="911f0-122">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="911f0-123">На экране сводки будут показаны действия по мере их выполнения.</span><span class="sxs-lookup"><span data-stu-id="911f0-123">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="911f0-124">После завершения развертывания щелкните **Просмотреть журнал** , чтобы просмотреть доступные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="911f0-124">After the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="911f0-125">Нажмите кнопку **Готово** , чтобы завершить развертывание.</span><span class="sxs-lookup"><span data-stu-id="911f0-125">Click **Finish** to complete the deployment.</span></span>

7.  <span data-ttu-id="911f0-126">На пограничном сервере в мастере развертывания Lync Server рядом с **шагом 3: запрос, установка и назначение сертификатов** нажмите кнопку **выполнить еще раз**.</span><span class="sxs-lookup"><span data-stu-id="911f0-126">On the Edge Server, in the Lync Server Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="911f0-127">Если пограничный сервер развертывается в первый раз, вместо повторного запуска вы увидите "запустить".</span><span class="sxs-lookup"><span data-stu-id="911f0-127">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

8.  <span data-ttu-id="911f0-128">На странице **Доступные задачи сертификатов** щелкните команду **Создать новый запрос сертификата**.</span><span class="sxs-lookup"><span data-stu-id="911f0-128">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

9.  <span data-ttu-id="911f0-129">На странице **запроса сертификата** выберите **внешний Граничный сертификат**.</span><span class="sxs-lookup"><span data-stu-id="911f0-129">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

10. <span data-ttu-id="911f0-130">На странице **отложенный или немедленный запрос** установите флажок **подготовить запрос сейчас, но отправить позже** .</span><span class="sxs-lookup"><span data-stu-id="911f0-130">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

11. <span data-ttu-id="911f0-131">На странице " **файл запроса сертификата** " введите полный путь и имя файла, в который нужно сохранить запрос (например, c: \\ CERT \_ exernal \_ Edge. cer).</span><span class="sxs-lookup"><span data-stu-id="911f0-131">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

12. <span data-ttu-id="911f0-132">На странице " **Укажите другой шаблон сертификата** ", чтобы использовать шаблон, отличный от шаблона веб-сервера по умолчанию, установите флажок **использовать альтернативный шаблон сертификата для выбранного центра сертификации** .</span><span class="sxs-lookup"><span data-stu-id="911f0-132">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

13. <span data-ttu-id="911f0-133">На странице **имя и параметры безопасности** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="911f0-133">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="911f0-134">В поле **понятное имя** введите отображаемое имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="911f0-134">In **Friendly name**, type a display name for the certificate</span></span>
    
    2.  <span data-ttu-id="911f0-135">В качестве **битовой длины** укажите длину в битах (обычно это значение по умолчанию — **2048**).</span><span class="sxs-lookup"><span data-stu-id="911f0-135">In **Bit length**, specify the bit length (typically, the default of **2048**)</span></span>
    
    3.  <span data-ttu-id="911f0-136">Убедитесь, что установлен флажок " **помечать закрытый ключ сертификата как экспортируемый** "</span><span class="sxs-lookup"><span data-stu-id="911f0-136">Verify that the **Mark certificate private key as exportable** check box is selected</span></span>

14. <span data-ttu-id="911f0-137">На странице " **сведения об организации** " введите имя Организации и организационное подразделение (например, "подразделение" или "Отдел")</span><span class="sxs-lookup"><span data-stu-id="911f0-137">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department)</span></span>

15. <span data-ttu-id="911f0-138">На странице **сведения о географическом** расположении укажите сведения о местоположении.</span><span class="sxs-lookup"><span data-stu-id="911f0-138">On the **Geographical Information** page, specify the location information</span></span>

16. <span data-ttu-id="911f0-139">На странице **имя субъекта/альтернативная тема** отображается информация, которая будет автоматически заполнена мастером.</span><span class="sxs-lookup"><span data-stu-id="911f0-139">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="911f0-140">Если требуются дополнительные альтернативные имена субъектов, их можно указать в следующих двух шагах.</span><span class="sxs-lookup"><span data-stu-id="911f0-140">If additional subject alternative names are needed, you specify them in the next two steps</span></span>

17. <span data-ttu-id="911f0-141">В **параметрах домена SIP на странице "альтернативные имена тем" (SAN)** установите флажок домен, чтобы добавить SIP.</span><span class="sxs-lookup"><span data-stu-id="911f0-141">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.</span></span> <span data-ttu-id="911f0-142">\<sipdomain\> элемент в список альтернативных имен субъектов.</span><span class="sxs-lookup"><span data-stu-id="911f0-142">\<sipdomain\> entry to the subject alternative names list.</span></span>

18. <span data-ttu-id="911f0-143">На странице **Настройка дополнительных имен для других тем** укажите необходимые дополнительные имена субъектов.</span><span class="sxs-lookup"><span data-stu-id="911f0-143">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="911f0-144">Если установлен прокси-сервер XMPP, по умолчанию доменное имя (например, contoso.com) заполнено в записях сети SAN.</span><span class="sxs-lookup"><span data-stu-id="911f0-144">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="911f0-145">Если вам нужны дополнительные элементы, добавьте их на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="911f0-145">If you require more entries, add them in this step.</span></span>

    
    </div>

19. <span data-ttu-id="911f0-146">На странице **сводки запроса** ознакомьтесь со сведениями о сертификате, которые будут использоваться для создания запроса.</span><span class="sxs-lookup"><span data-stu-id="911f0-146">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

20. <span data-ttu-id="911f0-147">После завершения выполнения команд можно **Просмотреть журнал** или нажать кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="911f0-147">After the commands finish running, you can **View Log**, or click **Next** to continue.</span></span>

21. <span data-ttu-id="911f0-148">На странице " **файл запроса на сертификат** " можно просмотреть созданный файл запроса на подписывание сертификата (CSR), щелкнув **Просмотреть** или выйти из мастера сертификатов, нажав кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="911f0-148">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

22. <span data-ttu-id="911f0-149">Скопируйте файл запроса и отправьте его в общедоступный центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="911f0-149">Copy the request file and submit to your public certification authority.</span></span>

23. <span data-ttu-id="911f0-150">После получения, импорта и назначения общедоступного сертификата вы должны остановить и перезапустить службы пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="911f0-150">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="911f0-151">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**...</span><span class="sxs-lookup"><span data-stu-id="911f0-151">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**..</span></span> <span data-ttu-id="911f0-152">В командной консоли Lync Server введите:</span><span class="sxs-lookup"><span data-stu-id="911f0-152">In the Lync Server Management Shell, type:</span></span>
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. <span data-ttu-id="911f0-153">Чтобы настроить DNS для XMPP Федерации, добавьте следующую запись SRV для внешнего DNS: \_ XMPP-Server. \_ Номера.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="911f0-153">To configure DNS for XMPP federation, you add the following SRV record to external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="911f0-154">SRV-запись будет разрешаться для полного доменного имени Edge-сервера, при этом значение порта 5269</span><span class="sxs-lookup"><span data-stu-id="911f0-154">The SRV record will resolve to the access edge FQDN of the Edge server, with a port value of 5269</span></span>

25. <span data-ttu-id="911f0-155">Настройте новую политику внешнего доступа, чтобы включить всех пользователей, открыв командную консоль Lync Server Management Shell на сервере переднего плана и введя:</span><span class="sxs-lookup"><span data-stu-id="911f0-155">Configure a new External Access Policy to enable all users by opening the Lync Server Management Shell on a Front End Server and typing:</span></span>
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

<span data-ttu-id="911f0-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="911f0-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

