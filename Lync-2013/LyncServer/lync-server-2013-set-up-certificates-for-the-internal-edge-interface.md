---
title: 'Lync Server 2013: настройка сертификатов для внутреннего интерфейса пограничного сервера'
description: 'Lync Server 2013: Настройка сертификатов для внутреннего интерфейса Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the internal edge interface
ms:assetid: a1963cc9-87c5-4935-86c0-6bedc6afd0ac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412750(v=OCS.15)
ms:contentKeyID: 48184949
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 52473069735d4f48c247367194139c479e71293f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424004"
---
# <a name="set-up-certificates-for-the-internal-edge-interface-in-lync-server-2013"></a><span data-ttu-id="cbaed-103">Настройка сертификатов для внутреннего интерфейса пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cbaed-103">Set up certificates for the internal edge interface in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cbaed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cbaed-104">

<span> </span></span></span>

<span data-ttu-id="cbaed-105">_**Тема последнего изменения:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="cbaed-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cbaed-106">При запуске мастера сертификатов убедитесь, что вы вошли в систему под учетной записью, которая является членом группы, которой назначены соответствующие разрешения для типа шаблона сертификата, который вы будете использовать.</span><span class="sxs-lookup"><span data-stu-id="cbaed-106">When you run the Certificate Wizard, ensure that you are logged in using an account that is a member of a group that has been assigned the appropriate permissions for the type of certificate template you will use.</span></span> <span data-ttu-id="cbaed-107">По умолчанию запрос сертификата Lync Server 2013 будет использовать шаблон сертификата веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="cbaed-107">By default, a Lync Server 2013 certificate request will use the Web Server certificate template.</span></span> <span data-ttu-id="cbaed-108">Если вы используете учетную запись, которая входит в группу RTCUniversalServerAdmins, чтобы запросить сертификат с помощью этого шаблона, убедитесь, что группе назначены разрешения, необходимые для использования этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="cbaed-108">If you use an account that is a member of the RTCUniversalServerAdmins group to request a certificate using this template, verify that the group has been assigned the Enroll permissions required to use that template.</span></span>



</div>

<span data-ttu-id="cbaed-109">На внутреннем интерфейсе каждого пограничного сервера требуется один сертификат.</span><span class="sxs-lookup"><span data-stu-id="cbaed-109">A single certificate is required on the internal interface of each Edge Server.</span></span> <span data-ttu-id="cbaed-110">Сертификаты для внутреннего интерфейса могут выдаваться внутренним центром сертификации предприятия (ЦС) или общедоступным ЦС.</span><span class="sxs-lookup"><span data-stu-id="cbaed-110">Certificates for the internal interface can be issued by an internal enterprise certification authority (CA) or a public CA.</span></span> <span data-ttu-id="cbaed-111">Если в вашей организации есть внутренний центр сертификации, вы можете сэкономить на расходах на использование общедоступных сертификатов с помощью внутреннего ЦС для выдаче сертификата для внутреннего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cbaed-111">If your organization has an internal CA deployed you can save on the expense of using public certificates by using the internal CA to issue the certificate for the internal interface.</span></span> <span data-ttu-id="cbaed-112">Вы можете использовать внутренний центр сертификации Windows Server 2008 или центр сертификации Windows Server 2008 R2 для создания этих сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cbaed-112">You can use an internal Windows Server 2008 CA or Windows Server 2008 R2 CA to create these certificates.</span></span>

<span data-ttu-id="cbaed-113">Подробнее об этих и других требованиях к сертификатам можно узнать в статьях [требования к сертификатам для доступа внешних пользователей в Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="cbaed-113">For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span></span>

<span data-ttu-id="cbaed-114">Чтобы настроить сертификаты на внутреннем интерфейсе EDGE на сайте, выполните указанные ниже действия, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="cbaed-114">To set up certificates on the internal edge interface at a site, use the procedures in this section to do the following:</span></span>

1.  <span data-ttu-id="cbaed-115">Скачайте цепочку сертификатов ЦС для внутреннего интерфейса на каждый пограничный сервер.</span><span class="sxs-lookup"><span data-stu-id="cbaed-115">Download the CA certification chain for the internal interface to each Edge Server.</span></span>

2.  <span data-ttu-id="cbaed-116">Импортируйте цепочку сертификации ЦС для внутреннего интерфейса на каждом пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="cbaed-116">Import the CA certification chain for the internal interface, on each Edge Server.</span></span>

3.  <span data-ttu-id="cbaed-117">Создайте запрос сертификата для внутреннего интерфейса на одном пограничном сервере, который называется первым пограничным сервером.</span><span class="sxs-lookup"><span data-stu-id="cbaed-117">Create the certificate request for the internal interface, on one Edge Server, called the first Edge Server.</span></span>

4.  <span data-ttu-id="cbaed-118">Импортируйте сертификат внутреннего интерфейса на первом пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="cbaed-118">Import the certificate for the internal interface on the first Edge Server.</span></span>

5.  <span data-ttu-id="cbaed-119">Импортируйте сертификат на других серверах пограничного сайта (или развернут за этот балансировщик нагрузки).</span><span class="sxs-lookup"><span data-stu-id="cbaed-119">Import the certificate on the other Edge Servers at this site (or deployed behind this load balancer).</span></span>

6.  <span data-ttu-id="cbaed-120">Назначьте сертификат внутреннему интерфейсу каждого пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="cbaed-120">Assign the certificate for the internal interface of every Edge Server.</span></span>

<span data-ttu-id="cbaed-121">Если у вас несколько сайтов с пограничного сервера (то есть топология с несколькими сайтами) или отдельные наборы пограничных серверов, развернутые за различными балансировщикми нагрузки, вам нужно выполнить эти действия для каждого сайта с пограничными серверами и для каждого набора пограничных серверов, развернутого за другой балансировщик нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cbaed-121">If you have more than one site with Edge Servers (that is, a multiple-site edge topology), or separate sets of Edge Servers deployed behind different load balancers, you need to follow these steps for each site that has Edge Servers, and for each set of Edge Servers deployed behind a different load balancer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cbaed-122">Действия, описанные в этом разделе, основываются на использовании &nbsp; центра сертификации Windows server 2008, Windows server &nbsp; 2008 R2, центра сертификации windows Server &nbsp; 2012 или центра сертификации Windows Server 2012 R2 для создания сертификата для каждого пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="cbaed-122">The steps for procedures in this section are based on using a Windows Server&nbsp;2008 CA, Windows Server&nbsp;2008&nbsp;R2 CA, Windows Server 2012 CA, or Windows Server 2012 R2 CA to create a certificate for each Edge Server.</span></span> <span data-ttu-id="cbaed-123">Пошаговое руководство для любого другого ЦС можно найти в документации по этому центру сертификации.</span><span class="sxs-lookup"><span data-stu-id="cbaed-123">For step-by-step guidance for any other CA, consult the documentation for that CA.</span></span> <span data-ttu-id="cbaed-124">По умолчанию все пользователи, прошедшие проверку подлинности, имеют соответствующие права для запроса сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cbaed-124">By default, all authenticated users have the appropriate user rights to request certificates.</span></span><BR><span data-ttu-id="cbaed-125">Процедуры, описанные в этом разделе, основываются на создании запросов на получение сертификата на пограничном сервере в рамках процесса развертывания пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="cbaed-125">The procedures in this section are based on creating certificate requests on the Edge Server as part of the Edge Server deployment process.</span></span> <span data-ttu-id="cbaed-126">Вы можете создавать запросы на сертификат с помощью сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="cbaed-126">It is possible to create certificate requests using the Front End Server.</span></span> <span data-ttu-id="cbaed-127">Это можно сделать, чтобы выполнить запрос сертификата на раннем этапе планирования и развертывания, прежде чем приступать к развертыванию пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="cbaed-127">You can do this to complete the certificate request early in the planning and deployment process, before you start deployment of the Edge Servers.</span></span> <span data-ttu-id="cbaed-128">Для этого необходимо убедиться в том, что запрашиваемый сертификат определен с помощью экспортируемого закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="cbaed-128">To do this, you must ensure that the certificate you request is defined with an exportable private key.</span></span><BR><span data-ttu-id="cbaed-129">Процедуры, описанные в этом разделе, описывают использование файла. cer и. p7b для сертификата.</span><span class="sxs-lookup"><span data-stu-id="cbaed-129">The procedures in this section describe using a .cer and a .p7b file for the certificate.</span></span> <span data-ttu-id="cbaed-130">Если вы используете файл другого типа, измените эти процедуры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="cbaed-130">If you use a different type of file, modify these procedures as appropriate.</span></span>



</div>

<div>

## <a name="to-download-the-ca-certification-chain-for-the-internal-interface-using-certsrv-web-site"></a><span data-ttu-id="cbaed-131">Загрузка цепочки сертификатов ЦС для внутреннего интерфейса с помощью веб-сайта certsrv</span><span class="sxs-lookup"><span data-stu-id="cbaed-131">To download the CA certification chain for the internal interface using certsrv Web site</span></span>

1.  <span data-ttu-id="cbaed-132">Войдите на сервер Lync Server 2013 во внутренней сети (то есть не на пограничном сервере), который входит в группу **администраторов** .</span><span class="sxs-lookup"><span data-stu-id="cbaed-132">Log on to an Lync Server 2013 server in the internal network (that is, not the Edge Server) as a member of the **Administrators** group.</span></span>

2.  <span data-ttu-id="cbaed-133">Чтобы открыть командную строку, в командной строке нажмите кнопку **Пуск**, выберите команду **выполнить** и введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cbaed-133">Run the following command at a command prompt by clicking **Start**, clicking **Run**, and then typing the following:</span></span>
    
        https://<name of your Issuing CA Server>/certsrv
    
    <span data-ttu-id="cbaed-134">Например:</span><span class="sxs-lookup"><span data-stu-id="cbaed-134">For example:</span></span>
    
        https://ca01.contoso.net/certsrv
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cbaed-135">Если вы используете центр сертификации предприятия Windows Server 2008 или Windows Server 2008 R2, необходимо использовать HTTPS, а не HTTP.</span><span class="sxs-lookup"><span data-stu-id="cbaed-135">If you are using a Windows Server 2008 or Windows Server 2008 R2 enterprise CA, you must use https, not http.</span></span>

    
    </div>

3.  <span data-ttu-id="cbaed-136">На веб-странице certsrv выдающего ЦС в списке **Выберите нужное действие** щелкните **Загрузка сертификата ЦС, цепочки сертификатов или CRL**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-136">On the issuing CA’s certsrv web page, under **Select a task**, click **Download a CA certificate, certificate chain, or CRL**.</span></span>

4.  <span data-ttu-id="cbaed-137">В разделе **Загрузка сертификата ЦС, цепочки сертификатов или CRL** нажмите кнопку **Загрузить цепочку сертификатов ЦС**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-137">Under **Download a CA Certificate, Certificate Chain, or CRL**, click **Download CA certificate chain**.</span></span>

5.  <span data-ttu-id="cbaed-138">В диалоговом окне **Загрузка файла** нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-138">In the **File Download** dialog box, click **Save**.</span></span>

6.  <span data-ttu-id="cbaed-139">Сохраните файл. p7b на жестком диске на сервере, а затем скопируйте его в папку на каждом пограничном сервере.</span><span class="sxs-lookup"><span data-stu-id="cbaed-139">Save the .p7b file to the hard disk drive on the server, and then copy it to a folder on each Edge Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cbaed-140">Файл. p7b включает все сертификаты, которые находятся в пути сертификации.</span><span class="sxs-lookup"><span data-stu-id="cbaed-140">The .p7b file contains all of the certificates that are in the certification path.</span></span> <span data-ttu-id="cbaed-141">Чтобы просмотреть путь сертификации, откройте сертификат сервера и щелкните путь сертификации.</span><span class="sxs-lookup"><span data-stu-id="cbaed-141">To view the certification path, open the server certificate and click the certification path.</span></span>

    
    </div>

</div>

<div>

## <a name="to-export-the-ca-certification-chain-for-the-internal-interface-using-mmc"></a><span data-ttu-id="cbaed-142">Экспорт цепочки сертификатов ЦС для внутреннего интерфейса с помощью MMC</span><span class="sxs-lookup"><span data-stu-id="cbaed-142">To export the CA certification chain for the internal interface using MMC</span></span>

1.  <span data-ttu-id="cbaed-143">Вы можете экспортировать корневой сертификат ЦС из любого компьютера, подключенного к домену, с помощью консоли управления (MMC).</span><span class="sxs-lookup"><span data-stu-id="cbaed-143">You can export the CA root certificate from any domain joined machine using the Microsoft Management Console (MMC).</span></span> <span data-ttu-id="cbaed-144">Нажмите кнопку **Пуск** и выберите команду **выполнить**, а затем — команду **MMC**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-144">Click **Start**, click **Run**, and then type **MMC**.</span></span>

2.  <span data-ttu-id="cbaed-145">На консоли MMC щелкните **файл**, а затем — **Добавить/удалить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-145">In the MMC console, click **File**, click **Add/Remove**.</span></span>

3.  <span data-ttu-id="cbaed-146">В диалоговом окне **Добавление и удаление оснасток** выберите пункт **Сертификаты** и нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-146">From the **Add or Remove Snap-ins** dialog list, select **Certificates**, then click **Add**.</span></span> <span data-ttu-id="cbaed-147">При появлении запроса выберите пункт **учетная запись компьютера**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-147">When prompted, select **Computer Account**.</span></span> <span data-ttu-id="cbaed-148">On the **Select Computer** dialog, select **Local Computer**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-148">On the **Select Computer** dialog, select **Local Computer**.</span></span> <span data-ttu-id="cbaed-149">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-149">Click **Finish**.</span></span> <span data-ttu-id="cbaed-150">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-150">Click **OK**.</span></span>

4.  <span data-ttu-id="cbaed-151">Разверните раздел **Сертификаты (локальный компьютер)**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-151">Expand **Certificates (Local Computer)**.</span></span> <span data-ttu-id="cbaed-152">Разверните узел **Доверенные корневые центры сертификации** и выберите пункт **Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-152">Expand **Trusted Root Certification Authorities**, select **Certificates**.</span></span>

5.  <span data-ttu-id="cbaed-153">Щелкните корневой сертификат, выпущенный вашим ЦС.</span><span class="sxs-lookup"><span data-stu-id="cbaed-153">Click the root certificate issued by your CA.</span></span> <span data-ttu-id="cbaed-154">Щелкните сертификат правой кнопкой мыши, выберите **все задачи**, нажмите кнопку **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-154">Right click the certificate, select **All Tasks**, select **Export**.</span></span> <span data-ttu-id="cbaed-155">Откроется **Мастер экспорта сертификатов** .</span><span class="sxs-lookup"><span data-stu-id="cbaed-155">The **Certificate Export Wizard** will open.</span></span>

6.  <span data-ttu-id="cbaed-156">In the **Certificate Export Wizard**, click **Next**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-156">In the **Certificate Export Wizard**, click **Next**.</span></span>

7.  <span data-ttu-id="cbaed-157">В диалоговом окне **Экспорт формата файла** выберите формат для экспорта.</span><span class="sxs-lookup"><span data-stu-id="cbaed-157">On the **Export File Format** dialog, select a format to export to.</span></span> <span data-ttu-id="cbaed-158">Мы рекомендуем использовать **стандартные синтаксисы криптографических сообщений \# (PKCS 7) (. P7B)**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-158">We recommend the **Cryptographic Message Syntax Standard – PKCS \#7 Certificates (.P7B)**.</span></span> <span data-ttu-id="cbaed-159">Если вы выбрали **стандартный синтаксис для криптографических сообщений: PKCS \# 7 (. P7B)** установите флажок **включить все сертификаты в путь сертификации, если это возможно** , чтобы экспортировать цепочку сертификатов, включая сертификат корневого ЦС и любые сертификаты промежуточного ЦС.</span><span class="sxs-lookup"><span data-stu-id="cbaed-159">If you select the **Cryptographic Message Syntax Standard – PKCS \#7 Certificates (.P7B)**, select the **Include all certificates in the certification path if possible** checkbox to export the certificate chain, including the root CA certificate and any Intermediate CA certificates.</span></span> <span data-ttu-id="cbaed-160">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-160">Click **Next**.</span></span>

8.  <span data-ttu-id="cbaed-161">В диалоговом окне **файл для экспорта** в поле имя файла введите путь к файлу и его имя (расширение по умолчанию. p7b) для экспортированного сертификата.</span><span class="sxs-lookup"><span data-stu-id="cbaed-161">On the **File to Export** dialog in the file name entry, type a path and file name (default extension is .p7b) for the exported certificate.</span></span> <span data-ttu-id="cbaed-162">При необходимости нажмите кнопку **Обзор**, найдите каталог, в который нужно поместить экспортированный сертификат, и укажите имя экспортированного сертификата.</span><span class="sxs-lookup"><span data-stu-id="cbaed-162">Optionally, click **Browse**, locate a directory to place the exported certificate in and provide a name for the exported certificate.</span></span> <span data-ttu-id="cbaed-163">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-163">Click **Save**.</span></span> <span data-ttu-id="cbaed-164">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-164">Click **Next**.</span></span>

9.  <span data-ttu-id="cbaed-165">Проверьте сводку действий и нажмите кнопку **Готово** , чтобы завершить экспорт сертификата.</span><span class="sxs-lookup"><span data-stu-id="cbaed-165">Review the summary of actions, and click **Finish** to complete the export of the certificate.</span></span> <span data-ttu-id="cbaed-166">Нажмите кнопку **ОК**, чтобы подтвердить успешное выполнение экспорта.</span><span class="sxs-lookup"><span data-stu-id="cbaed-166">Click **OK** to confirm the successful export.</span></span>

</div>

<div>

## <a name="to-import-the-ca-certification-chain-for-the-internal-interface"></a><span data-ttu-id="cbaed-167">Импорт цепочки сертификатов ЦС для внутреннего интерфейса</span><span class="sxs-lookup"><span data-stu-id="cbaed-167">To import the CA certification chain for the internal interface</span></span>

1.  <span data-ttu-id="cbaed-168">На каждом пограничном сервере откройте консоль управления (MMC), нажав кнопку **Пуск**, выберите **выполнить**, введите **MMC** в поле **Открыть** , а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-168">On each Edge Server, open the Microsoft Management Console (MMC) by clicking **Start**, clicking **Run**, typing **mmc** in the **Open** box, and then clicking **OK**.</span></span>

2.  <span data-ttu-id="cbaed-169">В меню **файл** выберите команду **Добавить или удалить оснастку**, а затем нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-169">On the **File** menu, click **Add/Remove Snap-in**, and then click **Add**.</span></span>

3.  <span data-ttu-id="cbaed-170">В диалоговом окне **Добавление изолированных оснасток** выберите пункт **Сертификаты** и нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-170">In the **Add Standalone Snap-ins** box, click **Certificates**, and then click **Add**.</span></span>

4.  <span data-ttu-id="cbaed-171">В диалоговом окне **Оснастка диспетчера сертификатов** выберите **Учетная запись компьютера** и затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-171">In the **Certificate snap-in** dialog box, click **Computer account**, and then click **Next**.</span></span>

5.  <span data-ttu-id="cbaed-172">В диалоговом окне **Выбор компьютера** убедитесь, что на **локальном компьютере установлен флажок (компьютер, на котором запущена эта консоль)** , и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-172">In the **Select Computer** dialog box, ensure that the **Local computer: (the computer this console is running on)** check box is selected, and then click **Finish**.</span></span>

6.  <span data-ttu-id="cbaed-173">Нажмите кнопку **Закрыть**, а затем — кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-173">Click **Close**, and then click **OK**.</span></span>

7.  <span data-ttu-id="cbaed-174">В дереве консоли разверните узел **Сертификаты (локальный компьютер)**, щелкните правой кнопкой мыши **Доверенные корневые центры сертификации**, наведите указатель на пункт **все задачи** и выберите команду **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-174">In the console tree, expand **Certificates (Local Computer)**, right-click **Trusted Root Certification Authorities**, point to **All Tasks**, and then click **Import**.</span></span>

8.  <span data-ttu-id="cbaed-175">В мастере в поле **файл для импорта** укажите имя файла сертификата (то есть имя, указанное при загрузке цепочки сертификатов ЦС для внутреннего интерфейса в предыдущей процедуре).</span><span class="sxs-lookup"><span data-stu-id="cbaed-175">In the wizard, in **File to Import**, specify the file name of the certificate (that is, the name of that you specified when you downloaded the CA certification chain for the internal interface in the previous procedure).</span></span>

9.  <span data-ttu-id="cbaed-176">Повторите эти действия для каждого пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="cbaed-176">Repeat this procedure on each Edge Server.</span></span>

</div>

<div>

## <a name="to-create-the-certificate-request-for-the-internal-interface"></a><span data-ttu-id="cbaed-177">Создание запроса на сертификат для внутреннего интерфейса</span><span class="sxs-lookup"><span data-stu-id="cbaed-177">To create the certificate request for the internal interface</span></span>

1.  <span data-ttu-id="cbaed-178">На одном из пограничных серверов запустите мастер развертывания и рядом с **шагом 3: запрос, установка и назначение сертификатов** нажмите кнопку **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-178">On one of the Edge Servers, start the Deployment Wizard, and next to **Step 3: Request, Install, or Assign Certificates**, click **Run**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cbaed-179">Если в одном месте пула есть несколько пограничных серверов, вы можете запустить мастер сертификатов на любом из серверов пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="cbaed-179">If you have multiple Edge Servers in one location in a pool, you can run the Certificate Wizard on any one of the Edge Servers.</span></span><BR><span data-ttu-id="cbaed-180">После первого запуска шага 3 кнопка будет изменена на <STRONG>выполнение</STRONG>, а зеленая галочка, указывающая на то, что задача была успешно завершена, будет скрыта, пока не будут запрошены, установлены и назначены все нужные сертификаты.</span><span class="sxs-lookup"><span data-stu-id="cbaed-180">After you run Step 3 the first time, the button changes to <STRONG>Run again</STRONG>, and a green check mark that indicates successful completion of the task is not displayed until all require certificates have been requested, installed, and assigned.</span></span>

    
    </div>

2.  <span data-ttu-id="cbaed-181">На странице **Доступные задачи сертификатов** щелкните команду **Создать новый запрос сертификата**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-181">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

3.  <span data-ttu-id="cbaed-182">На странице **запроса сертификата** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-182">On the **Certificate Request** page, click **Next**.</span></span>

4.  <span data-ttu-id="cbaed-183">На странице **Отложенные и мгновенные запросы** выберите **Подготовить запрос сейчас, чтобы отправить его позже**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-183">On the **Delayed or Immediate Requests** page, click **Prepare the request now, but send it later**.</span></span>

5.  <span data-ttu-id="cbaed-184">На странице " **файл запроса сертификата** " введите полный путь и имя файла, в который нужно сохранить запрос (например, **c: \\ \_ внутренний \_ Edge. cer**).</span><span class="sxs-lookup"><span data-stu-id="cbaed-184">On the **Certificate Request File** page, type the full path and file name to which the request is to be saved (for example, **c:\\cert\_internal\_edge.cer**).</span></span>

6.  <span data-ttu-id="cbaed-185">На странице " **Укажите другой шаблон сертификата** ", чтобы использовать шаблон, отличный от шаблона веб-сервера по умолчанию, установите флажок **использовать альтернативный шаблон сертификата для выбранного центра** сертификации.</span><span class="sxs-lookup"><span data-stu-id="cbaed-185">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected Certificate Authority** check box.</span></span>

7.  <span data-ttu-id="cbaed-186">На странице **имя и параметры безопасности** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cbaed-186">On the **Name and Security Settings** page, do the following:</span></span>
    
      - <span data-ttu-id="cbaed-187">В поле **понятное имя** введите отображаемое имя сертификата (например, внутренний край).</span><span class="sxs-lookup"><span data-stu-id="cbaed-187">In **Friendly name**, type a display name for the certificate (for example, Internal Edge).</span></span>
    
      - <span data-ttu-id="cbaed-188">В качестве **битовой длины** укажите длину в битах (обычно это значение по умолчанию — **2048**).</span><span class="sxs-lookup"><span data-stu-id="cbaed-188">In **Bit length**, specify the bit length (typically, the default of **2048**).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="cbaed-189">Более высокая длина в битах обеспечивает более высокий уровень безопасности, но отрицательно сказывается на скорости.</span><span class="sxs-lookup"><span data-stu-id="cbaed-189">Higher bit lengths offer more security, but they have a negative impact on speed.</span></span>

        
        </div>
    
      - <span data-ttu-id="cbaed-190">Если необходимо экспортировать сертификат, установите флажок **помечать закрытым ключом сертификата как экспортируемым** .</span><span class="sxs-lookup"><span data-stu-id="cbaed-190">If the certificate needs to be exportable, select the **Mark certificate private key as exportable** check box.</span></span>

8.  <span data-ttu-id="cbaed-191">На странице " **сведения об организации** " введите имя Организации и подразделения (OU) (например, "подразделение" или "Отдел").</span><span class="sxs-lookup"><span data-stu-id="cbaed-191">On the **Organization Information** page, type the name for the organization and the organizational unit (OU) (for example, a division or department).</span></span>

9.  <span data-ttu-id="cbaed-192">На странице **сведения о географическом** расположении укажите сведения о местоположении.</span><span class="sxs-lookup"><span data-stu-id="cbaed-192">On the **Geographical Information** page, specify the location information.</span></span>

10. <span data-ttu-id="cbaed-193">На странице **имя субъекта/альтернативная тема** отображается информация, которая будет автоматически заполнена мастером.</span><span class="sxs-lookup"><span data-stu-id="cbaed-193">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span>

11. <span data-ttu-id="cbaed-194">На странице **Настройка дополнительных имен для других тем** укажите необходимые дополнительные имена субъектов.</span><span class="sxs-lookup"><span data-stu-id="cbaed-194">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>

12. <span data-ttu-id="cbaed-195">На странице **сводки запроса** ознакомьтесь с информацией о сертификате, которая будет использоваться для создания запроса.</span><span class="sxs-lookup"><span data-stu-id="cbaed-195">On the **Request Summary** page, review the certificate information that is going to be used to generate the request.</span></span>

13. <span data-ttu-id="cbaed-196">Завершив выполнение команд, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cbaed-196">After the commands complete, do the following:</span></span>
    
      - <span data-ttu-id="cbaed-197">Чтобы просмотреть журнал для запроса сертификата, нажмите кнопку **Просмотреть журнал**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-197">To view the log for the certificate request, click **View Log**.</span></span>
    
      - <span data-ttu-id="cbaed-198">Чтобы завершить запрос сертификата, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-198">To complete the certificate request, click **Next**.</span></span>

14. <span data-ttu-id="cbaed-199">На странице " **файл запроса сертификата** " выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cbaed-199">On the **Certificate Request File** page, do the following:</span></span>
    
      - <span data-ttu-id="cbaed-200">Чтобы просмотреть созданный файл запроса подписи сертификата (CSR), нажмите кнопку **Просмотр**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-200">To view the generated certificate signing request (CSR) file, click **View**.</span></span>
    
      - <span data-ttu-id="cbaed-201">Для завершения работы мастера нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-201">To close the wizard, click **Finish**.</span></span>

15. <span data-ttu-id="cbaed-202">Отправьте этот файл в центр сертификации (по электронной почте или другим методам, которые поддерживаются вашей организацией для вашего корпоративного центра сертификации) и при получении файла ответа скопируйте новый сертификат на этот компьютер, чтобы его можно было импортировать.</span><span class="sxs-lookup"><span data-stu-id="cbaed-202">Submit this file to your CA (by email or other method supported by your organization for your enterprise CA) and, when you receive the response file, copy the new certificate to this computer so that it is available for import.</span></span>

</div>

<div>

## <a name="to-import-the-certificate-for-the-internal-interface"></a><span data-ttu-id="cbaed-203">Импорт сертификата для внутреннего интерфейса</span><span class="sxs-lookup"><span data-stu-id="cbaed-203">To import the certificate for the internal interface</span></span>

1.  <span data-ttu-id="cbaed-204">Войдите на пограничный сервер, на котором вы создали запрос на сертификат, как член локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="cbaed-204">Log on to the Edge Server on which you created the certificate request as a member of the local Administrators group.</span></span>

2.  <span data-ttu-id="cbaed-205">В мастере развертывания рядом с **шагом 3: запрос, установка и назначение сертификатов** нажмите кнопку **выполнить еще раз**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-205">In the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <span data-ttu-id="cbaed-206">После первого запуска шага 3 кнопка будет изменена на **выполнение**, но зеленая галочка (указывающая на успешное завершение задачи) не отображается, пока не будут запрошены, установлены и назначены все необходимые сертификаты.</span><span class="sxs-lookup"><span data-stu-id="cbaed-206">After you run Step 3 the first time, the button changes to **Run again**, but a green check mark (indicating successful completion of the task) is not displayed until all require certificates have been requested, installed, and assigned.</span></span>

3.  <span data-ttu-id="cbaed-207">На странице **Доступные задачи для сертификатов** щелкните **Импорт сертификата из. P7b, PFX или CER-файл**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-207">On the **Available Certificate Tasks** page, click **Import a certificate from a .P7b, .pfx or .cer file**.</span></span>

4.  <span data-ttu-id="cbaed-208">На странице **Импорт сертификата** введите полный путь и имя файла сертификата, который вы просили и получили для внутреннего интерфейса этого пограничного сервера (или нажмите кнопку **Обзор** , чтобы найти и выбрать файл).</span><span class="sxs-lookup"><span data-stu-id="cbaed-208">On the **Import Certificate** page, type the full path and file name of the certificate that you requested and received for the internal interface of this Edge Server (or, click **Browse** to locate and select the file).</span></span>

5.  <span data-ttu-id="cbaed-209">При импорте сертификатов для других пользователей из пула, содержащего закрытые ключи, установите флажок **файл сертификата содержит certifcate закрытый ключ** и укажите пароль.</span><span class="sxs-lookup"><span data-stu-id="cbaed-209">If you are importing certificates for other members of the pool a certificate containing a private key, select the **Certificate file contains certifcate’s private key** check box and specify the password.</span></span>

</div>

<div>

## <a name="to-export-the-certificate-with-the-private-key-for-edge-servers-in-a-pool"></a><span data-ttu-id="cbaed-210">Экспорт сертификата с закрытым ключом для пограничных серверов в пуле</span><span class="sxs-lookup"><span data-stu-id="cbaed-210">To export the certificate with the private key for Edge Servers in a pool</span></span>

1.  <span data-ttu-id="cbaed-211">Войдите в систему как участник группы Администраторы на тот же самый граничный сервер, на котором вы импортировали сертификат.</span><span class="sxs-lookup"><span data-stu-id="cbaed-211">Log on as a member of the Administrators group to the same Edge Server on which you imported the certificate.</span></span>

2.  <span data-ttu-id="cbaed-212">Нажмите кнопку **Пуск** и выберите пункт **выполнить**, а затем — команду **MMC**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-212">Click **Start**, click **Run**, and type **MMC**.</span></span>

3.  <span data-ttu-id="cbaed-213">На консоли MMC щелкните **файл**, а затем — **Добавить/удалить оснастку**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-213">From the MMC console, click **File**, click **Add/Remove Snap-in**.</span></span>

4.  <span data-ttu-id="cbaed-214">На странице Добавление и удаление оснасток выберите пункт **Сертификаты** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-214">From Add or Remove Snap-ins page, click **Certificates**, click **Add**.</span></span>

5.  <span data-ttu-id="cbaed-215">В диалоговом окне Оснастка «Сертификаты» выберите пункт **учетная запись компьютера**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-215">In the Certificates snap-in dialog, select **Computer account**.</span></span> <span data-ttu-id="cbaed-216">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-216">Click **Next**.</span></span> <span data-ttu-id="cbaed-217">В списке выберите компьютер выберите **локальный компьютер: (компьютер, на котором запущена эта консоль)**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-217">In Select Computer, select **Local computer: (the computer this console is running on)**.</span></span> <span data-ttu-id="cbaed-218">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-218">Click **Finish**.</span></span> <span data-ttu-id="cbaed-219">Нажмите кнопку **ОК** , чтобы завершить настройку консоли MMC.</span><span class="sxs-lookup"><span data-stu-id="cbaed-219">Click **OK** to complete configuration of the MMC console.</span></span>

6.  <span data-ttu-id="cbaed-220">Дважды щелкните пункт **Сертификаты (локальный компьютер)**, чтобы развернуть хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cbaed-220">Double-click **Certificates (Local Computer)** to expand the certificate stores.</span></span> <span data-ttu-id="cbaed-221">Дважды щелкните пункт **Личные**, а затем дважды щелкните **Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-221">Double-click **Personal**, then double-click **Certificates**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="cbaed-222">Если в личном хранилище сертификатов локального компьютера нет сертификатов, закрытый ключ, связанный с сертификатом, который был импортирован, отсутствует.</span><span class="sxs-lookup"><span data-stu-id="cbaed-222">If there are no certificates in the Certificates Personal store for the local computer, there is no private key associated with the certificate that was imported.</span></span> <span data-ttu-id="cbaed-223">Просматривайте шаги запроса и импорта.</span><span class="sxs-lookup"><span data-stu-id="cbaed-223">Review the request and import steps.</span></span> <span data-ttu-id="cbaed-224">Если проблема сохранится, обратитесь к администратору или поставщику центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="cbaed-224">If the problem persists, contact your certification authority administrator or provider.</span></span>

    
    </div>

7.  <span data-ttu-id="cbaed-225">В личном хранилище сертификатов локального компьютера щелкните правой кнопкой мыши экспортируемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="cbaed-225">In the Certificates Personal store for the local computer, right-click the certificate that you are exporting.</span></span> <span data-ttu-id="cbaed-226">Выберите **все задачи**, нажмите кнопку **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-226">Click **All Tasks**, click **Export**.</span></span>

8.  <span data-ttu-id="cbaed-227">В мастере экспорта сертификатов нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-227">In the Certificate Export Wizard, click **Next**.</span></span> <span data-ttu-id="cbaed-228">Select **Yes, export the private key**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-228">Select **Yes, export the private key**.</span></span> <span data-ttu-id="cbaed-229">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-229">Click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cbaed-230">Если выделение <STRONG>Да, экспорт закрытого ключа</STRONG> недоступен, закрытый ключ, связанный с этим сертификатом, не был помечен для экспорта.</span><span class="sxs-lookup"><span data-stu-id="cbaed-230">If the selection <STRONG>Yes, export the private key</STRONG> is not available, the private key associated with this certificate was not marked for export.</span></span> <span data-ttu-id="cbaed-231">Вам потребуется еще раз запросить сертификат, убедившись в том, что сертификат помечен для экспорта закрытого ключа, прежде чем можно будет продолжить экспорт.</span><span class="sxs-lookup"><span data-stu-id="cbaed-231">You will need to request the certificate again, ensuring that the certificate is marked to allow for the export of the private key before you can continue with the export.</span></span> <span data-ttu-id="cbaed-232">Обратитесь к своему администратору или поставщику центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="cbaed-232">Contact your certification authority administrator or provider.</span></span>

    
    </div>

9.  <span data-ttu-id="cbaed-233">В диалоговом окне Экспорт форматов файлов выберите пункт **Exchange для персональных данных — PKCS \# 12 (. PFX)** и выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="cbaed-233">On the Export File Formats dialog, select **Personal Information Exchange – PKCS\#12 (.PFX)** and then select the following:</span></span>
    
      - <span data-ttu-id="cbaed-234">Включите по возможности все сертификаты в путь сертификации.</span><span class="sxs-lookup"><span data-stu-id="cbaed-234">Include all certificates in the certification path if possible</span></span>
    
      - <span data-ttu-id="cbaed-235">Экспорт всех расширенных свойств</span><span class="sxs-lookup"><span data-stu-id="cbaed-235">Export all extended properties</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="cbaed-236">При экспорте сертификата с пограничного сервера не выбирайте параметр <STRONG>Удаление закрытого ключа при успешном завершении экспорта</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="cbaed-236">When exporting the certificate from an Edge server, do not select <STRONG>Delete the private key if the export is successful</STRONG>.</span></span> <span data-ttu-id="cbaed-237">При выборе этого параметра потребуется импортировать сертификат и закрытый ключ на этот граничный сервер.</span><span class="sxs-lookup"><span data-stu-id="cbaed-237">Selecting this option will require that you import the certificate and the private key to this Edge server.</span></span>

        
        </div>
    
    <span data-ttu-id="cbaed-238">Для продолжения нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-238">Click **Next** to continue.</span></span>

10. <span data-ttu-id="cbaed-239">Если вы хотите назначить пароль для защиты закрытого ключа, введите пароль для закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="cbaed-239">If you want to assign password to protect the private key, type a password for the private key.</span></span> <span data-ttu-id="cbaed-240">Введите пароль еще раз для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cbaed-240">Re-enter the password to confirm.</span></span> <span data-ttu-id="cbaed-241">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-241">Click **Next**.</span></span>

11. <span data-ttu-id="cbaed-242">Type a path and file name for the exported certificate, using a file extension of .pfx.</span><span class="sxs-lookup"><span data-stu-id="cbaed-242">Type a path and file name for the exported certificate, using a file extension of .pfx.</span></span> <span data-ttu-id="cbaed-243">Путь должен быть доступен для всех других пограничных серверов в пуле или доступен для транспортировки с помощью съемных носителей (например, USB-устройства флэш-памяти).</span><span class="sxs-lookup"><span data-stu-id="cbaed-243">The path must either be accessible to all other Edge servers in the pool or available to transport by means of removable media - for example, a USB flash drive.</span></span> <span data-ttu-id="cbaed-244">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-244">Click **Next**.</span></span>

12. <span data-ttu-id="cbaed-245">Просмотр сводных данных в диалоговом окне "завершение работы мастера экспорта сертификатов".</span><span class="sxs-lookup"><span data-stu-id="cbaed-245">Review the summary on the Completing the Certificate Export Wizard dialog.</span></span> <span data-ttu-id="cbaed-246">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-246">Click **Finish**.</span></span>

13. <span data-ttu-id="cbaed-247">В диалоговом окне с сообщением об успешном экспорте нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-247">Click **OK** in the successful export dialog.</span></span>

14. <span data-ttu-id="cbaed-248">Импортируйте экспортированный файл сертификата на другие пограничные серверы, выполнив действия, описанные в разделе [Настройка сертификатов внешнего граничного интерфейса для Lync Server 2013](lync-server-2013-set-up-certificates-for-the-external-edge-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="cbaed-248">Import the exported certificate file to the other Edge servers following the steps outlined in the [Set up certificates for the external edge interface for Lync Server 2013](lync-server-2013-set-up-certificates-for-the-external-edge-interface.md) procedures.</span></span>

</div>

<div>

## <a name="to-assign-the-internal-certificate-on-the-edge-servers"></a><span data-ttu-id="cbaed-249">Назначение внутреннего сертификата на пограничном сервере</span><span class="sxs-lookup"><span data-stu-id="cbaed-249">To assign the internal certificate on the Edge Servers</span></span>

1.  <span data-ttu-id="cbaed-250">На каждом пограничном сервере в мастере развертывания рядом с **шагом 3: запрос, установка и назначение сертификатов** нажмите кнопку **выполнить еще раз**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-250">On each Edge Server, in the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>

2.  <span data-ttu-id="cbaed-251">На странице **Доступные задачи для сертификатов** выберите команду **назначить существующий сертификат**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-251">On the **Available Certificate Tasks** page, click **Assign an existing certificate**.</span></span>

3.  <span data-ttu-id="cbaed-252">На странице **Назначение сертификата** выберите в списке **Внутренний пограничный сервер**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-252">On the **Certificate Assignment** page, select **Edge Internal** in the list.</span></span>

4.  <span data-ttu-id="cbaed-253">На странице **хранилище сертификатов** выберите сертификат, который вы импортировали для внутреннего края (из предыдущей процедуры).</span><span class="sxs-lookup"><span data-stu-id="cbaed-253">On the **Certificate Store** page, select the certificate that you imported for the internal edge (from the previous procedure).</span></span>

5.  <span data-ttu-id="cbaed-254">На странице **Сводка назначения сертификата** проверьте параметры и нажмите кнопку **Далее** , чтобы назначить сертификаты.</span><span class="sxs-lookup"><span data-stu-id="cbaed-254">On the **Certificate Assignment Summary** page, review your settings, and then click **Next** to assign the certificates.</span></span>

6.  <span data-ttu-id="cbaed-255">На странице завершения работы мастера нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="cbaed-255">On the wizard completion page, click **Finish**.</span></span>

7.  <span data-ttu-id="cbaed-256">После использования этой процедуры для назначения внутреннего сертификата откройте оснастку сертификат на каждом сервере, разверните раздел **Сертификаты (локальный компьютер)**, а затем — **Личные**, выберите пункт **Сертификаты** и проверьте в области сведений, что в списке указан внутренний Граничный сертификат.</span><span class="sxs-lookup"><span data-stu-id="cbaed-256">After using this procedure to assign the internal edge certificate, open the Certificate snap-in on each server, expand **Certificates (Local computer)**, expand **Personal**, click **Certificates**, and then verify in the details pane that the internal edge certificate is listed.</span></span>

8.  <span data-ttu-id="cbaed-257">Если в развертывании есть несколько пограничных серверов, повторите эти действия для каждого пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="cbaed-257">If your deployment includes multiple Edge Servers, repeat this procedure for each Edge Server.</span></span>

<span data-ttu-id="cbaed-258"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cbaed-258"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

