---
title: 'Lync Server 2013: Настройка сертификатов на сервере, на котором работает единая система обмена сообщениями сервера Microsoft Exchange Server'
description: 'Lync Server 2013: Настройка сертификатов на сервере, на котором работает единая система обмена сообщениями сервера Microsoft Exchange Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure certificates on the server running Microsoft Exchange Server Unified Messaging
ms:assetid: 74c883b4-cef6-41a9-b2eb-7212be32fea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398564(v=OCS.15)
ms:contentKeyID: 48184521
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a7d1e0aec3ec36723ee68c0a1dcd7f60050f9ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399943"
---
# <a name="configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging"></a><span data-ttu-id="650ea-103">Настройка сертификатов на сервере, на котором работает единая система обмена сообщениями Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="650ea-103">Configure certificates on the server running Microsoft Exchange Server Unified Messaging</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="650ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="650ea-104">

<span> </span></span></span>

<span data-ttu-id="650ea-105">_**Тема последнего изменения:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="650ea-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="650ea-106">Если вы развернули единую систему обмена сообщениями Exchange (UM) в соответствии с инструкциями по [планированию интеграции единой системы обмена сообщениями в Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) в документации по планированию и хотите предоставить функции Exchange UM пользователям корпоративной голосовой связи в вашей организации, вы можете использовать описанные ниже процедуры для настройки сертификата на сервере, на котором запущено приложение Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="650ea-106">If you have deployed Exchange Unified Messaging (UM), as described in [Planning for Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) in the Planning documentation, and you want to provide Exchange UM features to Enterprise Voice users in your organization, you can use the following procedures to configure the certificate on the server running Exchange UM.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="650ea-107">Для внутренних сертификатов оба сервера, на которых запущены приложения Lync Server 2013 и серверы Microsoft Exchange, должны иметь взаимно Доверенные корневые доверенные центры сертификации.</span><span class="sxs-lookup"><span data-stu-id="650ea-107">For internal certificates, both the servers running Lync Server 2013 and the servers running Microsoft Exchange must have trusted root authority certificates that are mutually trusted.</span></span> <span data-ttu-id="650ea-108">Центр сертификации (ЦС) может быть либо тем же, либо другим центром сертификации, если корневой сертификат центра сертификации зарегистрирован в хранилище сертификатов доверенного корневого центра.</span><span class="sxs-lookup"><span data-stu-id="650ea-108">The certification authority (CA) can either be the same, or a different certification authority, as long as the servers have the certification authority’s root certificate registered in their trusted root authority certificate store.</span></span>



</div>

<span data-ttu-id="650ea-109">Для подключения к серверу Lync Server 2013 необходимо настроить сервер Exchange с сертификатом сервера.</span><span class="sxs-lookup"><span data-stu-id="650ea-109">The Exchange Server must be configured with a server certificate in order to connect to Lync Server 2013:</span></span>

1.  <span data-ttu-id="650ea-110">Скачайте сертификат ЦС для сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="650ea-110">Download the CA certificate for the Exchange Server.</span></span>

2.  <span data-ttu-id="650ea-111">Установите сертификат ЦС для сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="650ea-111">Install the CA certificate for the Exchange Server.</span></span>

3.  <span data-ttu-id="650ea-112">Убедитесь, что центр сертификации входит в список доверенных корневых ЦС сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="650ea-112">Verify that the CA is in the list of trusted root CAs of the Exchange Server.</span></span>

4.  <span data-ttu-id="650ea-113">Создайте запрос на сертификат для сервера Exchange и установите сертификат.</span><span class="sxs-lookup"><span data-stu-id="650ea-113">Create a certificate request for the Exchange Server and install the certificate.</span></span>

5.  <span data-ttu-id="650ea-114">Назначьте сертификат для сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="650ea-114">Assign the certificate for the Exchange Server.</span></span>

<div>

## <a name="to-download-the-ca-certificate"></a><span data-ttu-id="650ea-115">Загрузка сертификата ЦС</span><span class="sxs-lookup"><span data-stu-id="650ea-115">To download the CA certificate</span></span>

1.  <span data-ttu-id="650ea-116">На сервере с Exchange UM нажмите кнопку **Пуск**, выберите команду **выполнить**, введите **http:// \<name of your Issuing CA Server\> /certsrv** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="650ea-116">On the server running Exchange UM, click **Start**, click **Run**, type **http://\<name of your Issuing CA Server\>/certsrv**, and then click **OK**.</span></span>

2.  <span data-ttu-id="650ea-117">В разделе **выберите задачу** нажмите **загрузить сертификат ЦС, цепочку сертификатов или CRL**.</span><span class="sxs-lookup"><span data-stu-id="650ea-117">Under **Select a task**, click **Download a CA certificate, certificate chain, or CRL**.</span></span>

3.  <span data-ttu-id="650ea-118">В разделе **Загрузка сертификата ЦС, цепочки сертификатов или CRL** выберите **метод кодирования для базового 64**, а затем нажмите кнопку **загрузить сертификат ЦС**.</span><span class="sxs-lookup"><span data-stu-id="650ea-118">Under **Download a CA Certificate, Certificate Chain, or CRL**, select **Encoding Method to Base 64**, and then click **Download CA certificate**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="650ea-119">Вы также можете задать кодировку DER (правила кодирования) на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="650ea-119">You can also specify Distinguished Encoding Rules (DER) encoding at this step.</span></span> <span data-ttu-id="650ea-120">Если вы выбрали кодировку DER, тип файла на следующем этапе и на этапе 10 <STRONG>для установки сертификата ЦС</STRONG> —. p7b, а не. cer.</span><span class="sxs-lookup"><span data-stu-id="650ea-120">If you select DER encoding, the file type in the next step of this procedure and in step 10 of <STRONG>To Install the CA certificate</STRONG> is .p7b rather than .cer.</span></span>

    
    </div>

4.  <span data-ttu-id="650ea-121">В диалоговом окне **Загрузка файла** нажмите кнопку **сохранить**, а затем сохраните файл на жестком диске сервера.</span><span class="sxs-lookup"><span data-stu-id="650ea-121">In the **File Download** dialog box, click **Save**, and then save the file to the hard disk on the server.</span></span> <span data-ttu-id="650ea-122">(В зависимости от кодировки, выбранной на предыдущем шаге, файл будет содержать расширение. cer или. p7b.)</span><span class="sxs-lookup"><span data-stu-id="650ea-122">(The file will have either a .cer or a .p7b file extension, depending on the encoding that you selected in the previous step.)</span></span>

</div>

<div>

## <a name="to-install-the-ca-certificate"></a><span data-ttu-id="650ea-123">Установка сертификата ЦС</span><span class="sxs-lookup"><span data-stu-id="650ea-123">To install the CA certificate</span></span>

1.  <span data-ttu-id="650ea-124">На сервере с Exchange UM откройте консоль управления (MMC), нажав кнопку **Пуск**, выберите команду **выполнить**, введите в поле **Открыть** значение **MMC** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="650ea-124">On the server running Exchange UM, open Microsoft Management Console (MMC) by clicking **Start**, clicking **Run**, typing **mmc** in the **Open** box, and then clicking **OK**.</span></span>

2.  <span data-ttu-id="650ea-125">В меню **файл** выберите команду **Добавить или удалить оснастку**, а затем нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="650ea-125">On the **File** menu, click **Add/Remove Snap-in**, and then click **Add**.</span></span>

3.  <span data-ttu-id="650ea-126">В диалоговом окне **Добавление изолированных оснасток** выберите пункт **Сертификаты** и нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="650ea-126">In the **Add Standalone Snap-ins** box, click **Certificates**, and then click **Add**.</span></span>

4.  <span data-ttu-id="650ea-127">В диалоговом окне **Оснастка диспетчера сертификатов** выберите **Учетная запись компьютера** и затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="650ea-127">In the **Certificate snap-in** dialog box, click **Computer account**, and then click **Next**.</span></span>

5.  <span data-ttu-id="650ea-128">В диалоговом окне **Выбор компьютера** убедитесь, что на **локальном компьютере установлен флажок (компьютер, на котором запущена эта консоль)** , и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="650ea-128">In the **Select Computer** dialog box, verify that the **Local computer: (the computer this console is running on)** check box is selected, and then click **Finish**.</span></span>

6.  <span data-ttu-id="650ea-129">Нажмите кнопку **Закрыть**, а затем — кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="650ea-129">Click **Close**, and then click **OK**.</span></span>

7.  <span data-ttu-id="650ea-130">В дереве консоли разверните узел **Сертификаты (локальный компьютер)**, а затем разверните узел **Доверенные корневые центры сертификации** и выберите пункт **Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="650ea-130">In the console tree, expand **Certificates (Local Computer)**, expand **Trusted Root Certification Authorities**, and then click **Certificates**.</span></span>

8.  <span data-ttu-id="650ea-131">Щелкните правой кнопкой мыши пункт **Сертификаты**, выберите пункт **все задачи** и нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="650ea-131">Right-click **Certificates**, click **All Tasks**, and click **Import**.</span></span>

9.  <span data-ttu-id="650ea-132">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="650ea-132">Click **Next**.</span></span>

10. <span data-ttu-id="650ea-133">Нажмите кнопку **Обзор** , чтобы найти файл, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="650ea-133">Click **Browse** to locate the file, and then click **Next**.</span></span> <span data-ttu-id="650ea-134">(В зависимости от кодировки, выбранной на этапе 3 **для скачивания сертификата ЦС**, файл будет содержать расширение. cer или. p7b.</span><span class="sxs-lookup"><span data-stu-id="650ea-134">(The file will have either a .cer or a .p7b file extension, depending on the encoding that you selected in step 3 of **To download the CA certificate**.</span></span>

11. <span data-ttu-id="650ea-135">Нажмите кнопку **поместить все сертификаты в следующее хранилище**.</span><span class="sxs-lookup"><span data-stu-id="650ea-135">Click **Place All Certificates in the following store**.</span></span>

12. <span data-ttu-id="650ea-136">Нажмите кнопку **Обзор** и выберите пункт **Доверенные корневые центры сертификации**.</span><span class="sxs-lookup"><span data-stu-id="650ea-136">Click **Browse**, and then select **Trusted Root Certification Authorities**.</span></span>

13. <span data-ttu-id="650ea-137">Нажмите кнопку **Далее** , чтобы проверить настройки, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="650ea-137">Click **Next** to verify the settings, and then click **Finish**.</span></span>

</div>

<div>

## <a name="to-verify-that-the-ca-is-in-the-list-of-trusted-root-cas"></a><span data-ttu-id="650ea-138">Проверка того, что центр сертификации входит в список доверенных корневых ЦС</span><span class="sxs-lookup"><span data-stu-id="650ea-138">To verify that the CA is in the list of trusted root CAs</span></span>

1.  <span data-ttu-id="650ea-139">На сервере, на котором запущена служба единой системы обмена сообщениями, в MMC разверните раздел **Сертификаты (локальный компьютер)**, разверните узел **Доверенные корневые центры сертификации** и выберите пункт **Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="650ea-139">On the server running Exchange UM, in MMC expand **Certificates (Local Computer)**, expand **Trusted Root Certification Authorities**, and then click **Certificates**.</span></span>

2.  <span data-ttu-id="650ea-140">В области сведений убедитесь, что ваш центр сертификации входит в список доверенных центров сертификации.</span><span class="sxs-lookup"><span data-stu-id="650ea-140">In the details pane, verify that your CA is on the list of trusted CAs.</span></span>

</div>

<div>

## <a name="to-configure-exchange-server-2013-um-with-lync-server"></a><span data-ttu-id="650ea-141">Настройка Exchange Server 2013 UM с Lync Server</span><span class="sxs-lookup"><span data-stu-id="650ea-141">To configure Exchange Server 2013 UM with Lync Server</span></span>

1.  <span data-ttu-id="650ea-142">Подробные сведения можно найти в разделе "Интеграция Exchange 2013 UM с Lync Server" в документации Exchange Server по адресу [https://go.microsoft.com/fwlink/p/?LinkId=265372](https://go.microsoft.com/fwlink/p/?linkid=265372) .</span><span class="sxs-lookup"><span data-stu-id="650ea-142">For details, see "Integrate Exchange 2013 UM with Lync Server" in the Exchange Server documentation at [https://go.microsoft.com/fwlink/p/?LinkId=265372](https://go.microsoft.com/fwlink/p/?linkid=265372).</span></span>

</div>

<div>

## <a name="to-create-a-certificate-request-and-install-the-certificate-on-exchange-server-2007-sp1"></a><span data-ttu-id="650ea-143">Создание запроса на сертификат и установка сертификата на сервере Exchange Server 2007 (SP1)</span><span class="sxs-lookup"><span data-stu-id="650ea-143">To create a certificate request and install the certificate on Exchange Server 2007 (SP1)</span></span>

1.  <span data-ttu-id="650ea-144">На сервере с Exchange UM нажмите кнопку **Пуск**, выберите команду **выполнить**, введите **http:// \<**name of your Issuing CA Server**\> /certsrv** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="650ea-144">On the server running Exchange UM, click **Start**, click **Run**, type **http://\<**name of your Issuing CA Server**\>/certsrv**, and then click **OK**.</span></span>

2.  <span data-ttu-id="650ea-145">В разделе **выберите задачу** щелкните **запросить сертификат**.</span><span class="sxs-lookup"><span data-stu-id="650ea-145">Under **Select a task**, click **Request a Certificate**.</span></span>

3.  <span data-ttu-id="650ea-146">В разделе **запрос сертификата** щелкните **Расширенный запрос сертификата**.</span><span class="sxs-lookup"><span data-stu-id="650ea-146">Under **Request a Certificate**, click **Advanced certificate request**.</span></span>

4.  <span data-ttu-id="650ea-147">В разделе **Расширенный запрос сертификата** выберите команду **создать и отправить запрос этому ЦС**.</span><span class="sxs-lookup"><span data-stu-id="650ea-147">Under **Advanced Certificate Request**, click **Create and submit a request to this CA**.</span></span>

5.  <span data-ttu-id="650ea-148">В разделе **Расширенный запрос сертификата** выберите **веб-сервер** или другой шаблон сертификата сервера, настроенный для проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="650ea-148">Under **Advanced Certificate Request**, select **Web server** or another server certificate template configured for server authentication.</span></span>

6.  <span data-ttu-id="650ea-149">В разделе **идентифицирующая информация для автономного шаблона** в поле **имя** введите полное доменное имя (FQDN) сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="650ea-149">Under **Identifying Information for Offline Template**, in the **Name** box, type the fully qualified domain name (FQDN) of the Exchange Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="650ea-150">Необходимо ввести полное доменное имя сервера Exchange для работы с данными.</span><span class="sxs-lookup"><span data-stu-id="650ea-150">You must enter the FQDN of the Exchange Server for communications to work.</span></span>

    
    </div>

7.  <span data-ttu-id="650ea-151">В разделе **Параметры ключа** щелкните **сертификат магазина в хранилище сертификатов локального компьютера** .</span><span class="sxs-lookup"><span data-stu-id="650ea-151">Under **Key Options**, click the **Store certificate in the local computer certificate store** check box.</span></span>

8.  <span data-ttu-id="650ea-152">Нажмите кнопку " **Отправить** " в нижней части веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="650ea-152">Click the **Submit** button in the bottom of the webpage.</span></span>

9.  <span data-ttu-id="650ea-153">В открывшемся диалоговом окне с запросом подтверждения нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="650ea-153">In the dialog box that opens asking for confirmation, click **Yes**.</span></span>

10. <span data-ttu-id="650ea-154">На странице Сертификат выдан в разделе **сертификат выдан** выберите **установить этот сертификат**.</span><span class="sxs-lookup"><span data-stu-id="650ea-154">On the Certificate Issued page, under **Certificate Issued**, click **Install this certificate**.</span></span>

11. <span data-ttu-id="650ea-155">В открывшемся диалоговом окне с запросом подтверждения нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="650ea-155">In the dialog box that opens asking for confirmation, click **Yes**.</span></span>

12. <span data-ttu-id="650ea-156">Убедитесь, что на экране появится сообщение "ваш новый сертификат успешно установлен".</span><span class="sxs-lookup"><span data-stu-id="650ea-156">Verify that the message "Your new certificate has been successfully installed" appears.</span></span>

</div>

<div>

## <a name="to-create-a-certificate-on-exchange-server-2010"></a><span data-ttu-id="650ea-157">Создание сертификата на сервере Exchange Server 2010</span><span class="sxs-lookup"><span data-stu-id="650ea-157">To create a certificate on Exchange Server 2010</span></span>

1.  <span data-ttu-id="650ea-158">Войдите на сервер, на котором запущена служба единой системы обмена сообщениями с необходимыми правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="650ea-158">Log on to the server running Exchange UM with appropriate user rights.</span></span> <span data-ttu-id="650ea-159">Дополнительные сведения можно найти в разделе "разрешения клиентского доступа" [https://go.microsoft.com/fwlink/p/?linkId=195499](https://go.microsoft.com/fwlink/p/?linkid=195499) .</span><span class="sxs-lookup"><span data-stu-id="650ea-159">For details, see "Client Access Permissions" at [https://go.microsoft.com/fwlink/p/?linkId=195499](https://go.microsoft.com/fwlink/p/?linkid=195499).</span></span>

2.  <span data-ttu-id="650ea-160">Чтобы создать сертификат, ознакомьтесь с приведенными ниже инструкциями.</span><span class="sxs-lookup"><span data-stu-id="650ea-160">Refer to the following procedures to create the certificate:</span></span>
    
    1.  <span data-ttu-id="650ea-161">"Создать новый сертификат Exchange" на [https://go.microsoft.com/fwlink/p/?linkId=195494](https://go.microsoft.com/fwlink/p/?linkid=195494)</span><span class="sxs-lookup"><span data-stu-id="650ea-161">"Create a New Exchange Certificate" at [https://go.microsoft.com/fwlink/p/?linkId=195494](https://go.microsoft.com/fwlink/p/?linkid=195494)</span></span>
    
    2.  <span data-ttu-id="650ea-162">"Импортировать сертификат Exchange" на [https://go.microsoft.com/fwlink/p/?linkId=195496](https://go.microsoft.com/fwlink/p/?linkid=195496)</span><span class="sxs-lookup"><span data-stu-id="650ea-162">"Import an Exchange Certificate" at [https://go.microsoft.com/fwlink/p/?linkId=195496](https://go.microsoft.com/fwlink/p/?linkid=195496)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="650ea-163">Для <STRONG>имени субъекта</STRONG>сертификата необходимо ввести полное доменное имя сервера Exchange, чтобы связь работала.</span><span class="sxs-lookup"><span data-stu-id="650ea-163">For the certificate <STRONG>Subject Name</STRONG>, you must enter the FQDN of the Exchange Server for communications to work.</span></span>

    
    </div>

</div>

<div>

## <a name="to-assign-the-certificate-on-exchange-server-2007-sp1"></a><span data-ttu-id="650ea-164">Назначение сертификата на сервере Exchange Server 2007 (SP1)</span><span class="sxs-lookup"><span data-stu-id="650ea-164">To assign the certificate on Exchange Server 2007 (SP1)</span></span>

1.  <span data-ttu-id="650ea-165">На сервере, на котором запущена служба единой системы обмена сообщениями, откройте консоль MMC.</span><span class="sxs-lookup"><span data-stu-id="650ea-165">On the server running Exchange UM, open MMC.</span></span>

2.  <span data-ttu-id="650ea-166">В дереве консоли разверните узел **Личные** и выберите пункт **Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="650ea-166">In the console tree, expand **Personal** and then click **Certificates**.</span></span>

3.  <span data-ttu-id="650ea-167">Убедитесь, что в области сведений отображается персональный сертификат.</span><span class="sxs-lookup"><span data-stu-id="650ea-167">In the details pane, verify that personal certificate is displayed.</span></span>

4.  <span data-ttu-id="650ea-168">Дважды щелкните сертификат, чтобы прочитать его сведения, и убедитесь, что он является действительным.</span><span class="sxs-lookup"><span data-stu-id="650ea-168">Double-click the certificate to read its details and verify that it is valid.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="650ea-169">Для правильного отображения сертификата может пройти несколько минут.</span><span class="sxs-lookup"><span data-stu-id="650ea-169">It may take a few minutes before the certificate displays as valid.</span></span>

    
    </div>

5.  <span data-ttu-id="650ea-170">Перезапустите службу единой системы обмена сообщениями Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="650ea-170">Restart the Microsoft Exchange Unified Messaging service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="650ea-171">Сервер, на котором работает Exchange Server 2007 с пакетом обновления 1 (SP1), UM автоматически получает правильный сертификат.</span><span class="sxs-lookup"><span data-stu-id="650ea-171">The server running Exchange Server 2007 SP1 Unified Messaging automatically retrieves the correct certificate.</span></span>

    
    </div>

6.  <span data-ttu-id="650ea-172">Откройте средство просмотра событий и найдите событие с кодом 1112, которое указывает, какой сертификат был извлечен сервером, на котором работает сервер Exchange Server 2007 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="650ea-172">Open Event Viewer and look for Event ID 1112, which specifies what certificate the server running Exchange Server 2007 SP1 Unified Messaging has retrieved.</span></span>

</div>

<div>

## <a name="to-assign-the-certificate-on-exchange-server-2010"></a><span data-ttu-id="650ea-173">Назначение сертификата на сервере Exchange Server 2010</span><span class="sxs-lookup"><span data-stu-id="650ea-173">To assign the certificate on Exchange Server 2010</span></span>

1.  <span data-ttu-id="650ea-174">Войдите на сервер, на котором запущена служба единой системы обмена сообщениями с необходимыми правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="650ea-174">Log on to the server running Exchange UM with appropriate user rights.</span></span> <span data-ttu-id="650ea-175">Дополнительные сведения можно найти в разделе "разрешения клиентского доступа" [https://go.microsoft.com/fwlink/p/?linkId=195499](https://go.microsoft.com/fwlink/p/?linkid=195499) .</span><span class="sxs-lookup"><span data-stu-id="650ea-175">For details, see "Client Access Permissions" at [https://go.microsoft.com/fwlink/p/?linkId=195499](https://go.microsoft.com/fwlink/p/?linkid=195499).</span></span>

2.  <span data-ttu-id="650ea-176">Процедура назначения сертификата приведена в разделе "назначение служб сертификату" [https://go.microsoft.com/fwlink/p/?linkId=195497](https://go.microsoft.com/fwlink/p/?linkid=195497) .</span><span class="sxs-lookup"><span data-stu-id="650ea-176">For the procedure to assign the certificate, see "Assign Services to a Certificate" at [https://go.microsoft.com/fwlink/p/?linkId=195497](https://go.microsoft.com/fwlink/p/?linkid=195497).</span></span>

<span data-ttu-id="650ea-177"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="650ea-177"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

