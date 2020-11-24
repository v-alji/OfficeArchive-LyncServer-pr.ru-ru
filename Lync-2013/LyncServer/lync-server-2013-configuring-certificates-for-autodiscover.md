---
title: 'Lync Server 2013: Настройка сертификатов для автообнаружения'
description: 'Lync Server 2013: Настройка сертификатов для автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring certificates for Autodiscover
ms:assetid: 1842191d-df9a-41e0-9286-08c25f9b5dca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945617(v=OCS.15)
ms:contentKeyID: 51541453
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98ab9eca92685eef8bccc500dc4a91efa891dec6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397954"
---
# <a name="configuring-certificates-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="56c7a-103">Настройка сертификатов для автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56c7a-103">Configuring certificates for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56c7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56c7a-104">

<span> </span></span></span>

<span data-ttu-id="56c7a-105">_**Тема последнего изменения:** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="56c7a-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="56c7a-106">Для использования сертификатов для вашего пула каталогов, пула переднего плана и обратного прокси требуются дополнительные записи альтернативного имени для обеспечения безопасной связи с клиентами Lync.</span><span class="sxs-lookup"><span data-stu-id="56c7a-106">The certificates for your Director pool, Front End pool, and reverse proxy require additional subject alternative name entries to support secure connections with Lync clients.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="56c7a-107">Вы можете использовать командлет <STRONG>Get-CsCertificate</STRONG> для просмотра сведений о текущих назначенных сертификатах.</span><span class="sxs-lookup"><span data-stu-id="56c7a-107">You can use the <STRONG>Get-CsCertificate</STRONG> cmdlet to view information about the currently assigned certificates.</span></span> <span data-ttu-id="56c7a-108">Однако представление по умолчанию усекает свойства сертификата и не отображает все значения в свойстве SubjectAlternativeNames.</span><span class="sxs-lookup"><span data-stu-id="56c7a-108">However, the default view truncates the properties of the certificate and does not display all values in the SubjectAlternativeNames property.</span></span> <span data-ttu-id="56c7a-109">Вы можете использовать командлеты <STRONG>Get-CsCertificate</STRONG> , <STRONG>request-</STRONG>CsCertificate и <STRONG>Set-CsCertificate</STRONG> для просмотра некоторых данных и запроса и назначения сертификатов.</span><span class="sxs-lookup"><span data-stu-id="56c7a-109">You can use the <STRONG>Get-CsCertificate</STRONG> , <STRONG>Request-</STRONG>CsCertificate and the <STRONG>Set-CsCertificate</STRONG> cmdlets to view some information and to request and assign certificates.</span></span> <span data-ttu-id="56c7a-110">Тем не менее, это не лучший способ использовать, если вы не знаете, какие свойства используются для альтернативных имен субъектов (SAN) для текущего сертификата.</span><span class="sxs-lookup"><span data-stu-id="56c7a-110">However, it’s not the best method to use if you are unsure of the properties of the subject alternative names (SAN) on the current certificate.</span></span> <span data-ttu-id="56c7a-111">Для просмотра сертификата и всех участников свойств рекомендуется использовать оснастку «Сертификаты» <EM>консоли управления (MMC)</EM> или мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="56c7a-111">To view the certificate and all property members, it is suggested to use the Certificates snap-in the <EM>Microsoft Management Console (MMC)</EM> or to use the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="56c7a-112">В мастере развертывания Lync Server вы можете просматривать свойства сертификата с помощью мастера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="56c7a-112">In the Lync Server Deployment Wizard, you can use the Certificate Wizard to view the certificate properties.</span></span> <span data-ttu-id="56c7a-113">Ниже описаны процедуры для просмотра, запроса и назначения сертификата с помощью командной консоли Lync Server Management Shell и <EM>консоль управления MMC</EM> .</span><span class="sxs-lookup"><span data-stu-id="56c7a-113">The procedures for viewing, requesting and assigning a certificate using the Lync Server Management Shell and the <EM>Microsoft Management Console (MMC)</EM> are detailed in the following procedures.</span></span> <span data-ttu-id="56c7a-114">Чтобы воспользоваться мастером развертывания Lync Server, ознакомьтесь с подробными сведениями, если вы развернули необязательный режиссер или Режиссер: <A href="lync-server-2013-configure-certificates-for-the-director.md">Настройка сертификатов для режиссера в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="56c7a-114">To use the Lync Server Deployment Wizard, see details here if you have deployed the optional Director or Director pool: <A href="lync-server-2013-configure-certificates-for-the-director.md">Configure certificates for the Director in Lync Server 2013</A>.</span></span> <span data-ttu-id="56c7a-115">Сведения о том, как <A href="lync-server-2013-configure-certificates-for-servers.md">настроить сертификаты для серверов в Lync server 2013</A>, можно найти на сервере переднего плана или в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="56c7a-115">For the Front End Server or Front End pool, see the details here: <A href="lync-server-2013-configure-certificates-for-servers.md">Configure certificates for servers in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="56c7a-116">Начальные шаги в этой процедуре предназначены для подготовки, чтобы расположить вас как роль, которую воспроизводится текущими сертификатами.</span><span class="sxs-lookup"><span data-stu-id="56c7a-116">The initial steps in this procedure are preparation steps, to orient you as to what role the current certificates play.</span></span> <span data-ttu-id="56c7a-117">По умолчанию в сертификатах не будет lyncdiscover. &lt; sipdomain &gt; или lyncdiscoverinternal. &lt; внутренний доменный имя &gt; , если только вы ранее не установили службы Mobility Service или заранее подготовили свои сертификаты.</span><span class="sxs-lookup"><span data-stu-id="56c7a-117">By default, the certificates will not have a lyncdiscover.&lt;sipdomain&gt; or lyncdiscoverinternal.&lt;internal domain name&gt; entry unless you have previously installed Mobility Services or have prepared your certificates in advance.</span></span> <span data-ttu-id="56c7a-118">В этой процедуре используется пример имени домена SIP "contoso.com" и внутреннего доменного имени "contoso.net".</span><span class="sxs-lookup"><span data-stu-id="56c7a-118">This procedure uses the example SIP domain name ‘contoso.com’ and the example internal domain name ‘contoso.net’.</span></span><BR><span data-ttu-id="56c7a-119">Конфигурация сертификата по умолчанию для Lync Server 2013 и Lync Server 2010 — использование единого сертификата (по умолчанию) с целью назначения по умолчанию (для всех целей, кроме веб-служб), WebServicesExternal и WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="56c7a-119">The default certificate configuration for Lync Server 2013 and Lync Server 2010 is to use a single certificate (named ‘Default’) with the purposes Default (for all purposes except for the web services), WebServicesExternal and WebServicesInternal.</span></span> <span data-ttu-id="56c7a-120">Необязательная настройка — это использование отдельных сертификатов для каждой цели.</span><span class="sxs-lookup"><span data-stu-id="56c7a-120">An optional configuration is to use separate certificates for each purpose.</span></span> <span data-ttu-id="56c7a-121">Сертификаты можно управлять с помощью командной консоли Lync Server Management Shell и командлетов Windows PowerShell либо с помощью мастера сертификатов в мастере развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="56c7a-121">Certificates can be managed by using the Lync Server Management Shell and Windows PowerShell cmdlets, or by using the Certificate Wizard in the Lync Server Deployment Wizard.</span></span>



</div>

<div>

## <a name="to-update-certificates-with-new-subject-alternative-names-using-the-lync-server-management-shell"></a><span data-ttu-id="56c7a-122">Обновление сертификатов с использованием новых альтернативных имен для некоторых субъектов с помощью командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="56c7a-122">To update certificates with new subject alternative names using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="56c7a-123">Войдите в систему с помощью учетной записи, обладающей правами и разрешениями локального администратора.</span><span class="sxs-lookup"><span data-stu-id="56c7a-123">Log on to the computer using an account that has local administrator rights and permissions.</span></span>

2.  <span data-ttu-id="56c7a-124">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-124">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="56c7a-125">Узнайте, какие сертификаты были назначены серверу и для какого типа использования.</span><span class="sxs-lookup"><span data-stu-id="56c7a-125">Find out what certificates have been assigned to the server and for which type of use.</span></span> <span data-ttu-id="56c7a-126">Вам понадобятся эти сведения на следующем этапе, чтобы назначить обновленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="56c7a-126">You need this information in the next step to assign the updated certificate.</span></span> <span data-ttu-id="56c7a-127">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="56c7a-127">At the command line, type:</span></span>
    
        Get-CsCertificate

4.  <span data-ttu-id="56c7a-128">Просмотрите результаты предыдущего шага, чтобы узнать, назначен ли один сертификат для нескольких применений, или назначается ли другой сертификат для каждого использования.</span><span class="sxs-lookup"><span data-stu-id="56c7a-128">Look in the output from the previous step to see whether a single certificate is assigned for multiple uses or whether a different certificate is assigned for each use.</span></span> <span data-ttu-id="56c7a-129">Чтобы узнать, как используется сертификат, найдите параметр Use.</span><span class="sxs-lookup"><span data-stu-id="56c7a-129">Look in the Use parameter to find out how a certificate is used.</span></span> <span data-ttu-id="56c7a-130">Сравните параметр отпечатка для выводимых сертификатов, чтобы узнать, используется ли один и тот же сертификат несколько.</span><span class="sxs-lookup"><span data-stu-id="56c7a-130">Compare the Thumbprint parameter for the displayed certificates to see if the same certificate has multiple uses.</span></span>

5.  <span data-ttu-id="56c7a-131">Обновите сертификат.</span><span class="sxs-lookup"><span data-stu-id="56c7a-131">Update the certificate.</span></span> <span data-ttu-id="56c7a-132">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="56c7a-132">At the command line, type:</span></span>
    
        Set-CsCertificate -Type <type of certificate as displayed in the Use parameter> -Thumbprint <unique identifier>
    
    <span data-ttu-id="56c7a-133">Например, если командлет **Get-CsCertificate** показывает сертификат с использованием значения по умолчанию, другой — с помощью WebServicesInternal, а другой — с помощью WebServicesExternal, а для всех — с одинаковым значением отпечатка, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="56c7a-133">For example, if the **Get-CsCertificate** cmdlet displayed a certificate with Use of Default, another with a Use of WebServicesInternal, and another with a Use of WebServicesExternal, and they all had the same Thumbprint value, at the command line, type:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
    
    <span data-ttu-id="56c7a-134">**Важно!**</span><span class="sxs-lookup"><span data-stu-id="56c7a-134">**Important:**</span></span>
    
    <span data-ttu-id="56c7a-135">Если каждому использованию назначается отдельный сертификат (значение отпечатка отличается для каждого сертификата), важно не выполнять командлет **Set-CsCertificate** с несколькими типами.</span><span class="sxs-lookup"><span data-stu-id="56c7a-135">If a separate certificate is assigned for each use (the Thumbprint value is different for each certificate), it is important that you do not run the **Set-CsCertificate** cmdlet with multiple types.</span></span> <span data-ttu-id="56c7a-136">В этом случае выполните командлет **Set-CsCertificate** отдельно для каждого использования.</span><span class="sxs-lookup"><span data-stu-id="56c7a-136">In this case, run the **Set-CsCertificate** cmdlet separately for each use.</span></span> <span data-ttu-id="56c7a-137">Например:</span><span class="sxs-lookup"><span data-stu-id="56c7a-137">For example:</span></span>
    
        Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>

6.  <span data-ttu-id="56c7a-138">Чтобы просмотреть сертификат, нажмите кнопку **Пуск** и выберите команду **выполнить...**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-138">To view the certificate, click **Start**, click **Run…**.</span></span> <span data-ttu-id="56c7a-139">Введите MMC, чтобы открыть консоль управления MMC.</span><span class="sxs-lookup"><span data-stu-id="56c7a-139">Type MMC to open the Microsoft Management Console.</span></span>

7.  <span data-ttu-id="56c7a-140">В меню MMC выберите пункт **файл**, а затем — **Добавить или удалить оснастку...**, выберите пункт Сертификаты.</span><span class="sxs-lookup"><span data-stu-id="56c7a-140">From the MMC menu, select **File**, select **Add/Remove snap-in…**, select Certificates.</span></span> <span data-ttu-id="56c7a-141">Нажмите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-141">Click **Add**.</span></span> <span data-ttu-id="56c7a-142">При появлении соответствующего запроса выберите пункт **учетная запись компьютера**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-142">When prompted, select **Computer account**, then click **Next**.</span></span>

8.  <span data-ttu-id="56c7a-143">Если сертификат находится на этом компьютере, выберите пункт **локальный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-143">If the certificate is located on this computer, select **Local computer**.</span></span> <span data-ttu-id="56c7a-144">Если сертификат находится на другом компьютере, выберите **другой компьютер**, введите полное доменное имя компьютера или нажмите кнопку **Обзор** в поле **введите имя нужного объекта**, введите имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="56c7a-144">If the certificate is located on another computer, select **Another computer**, type in the fully qualified domain name of the computer or click **Browse** In **Enter the object name to select**, type the name of the computer.</span></span> <span data-ttu-id="56c7a-145">Нажмите кнопку **Проверить имена**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-145">Click **Check Names**.</span></span> <span data-ttu-id="56c7a-146">После разрешения имени компьютера оно будет подчеркнуто.</span><span class="sxs-lookup"><span data-stu-id="56c7a-146">When the name of the computer is resolved, it will be underlined.</span></span> <span data-ttu-id="56c7a-147">Нажмите кнопку **ОК**, а затем — **Готово**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-147">Click **OK**, then click **Finish**.</span></span> <span data-ttu-id="56c7a-148">Нажмите кнопку **ОК** , чтобы завершить выбор и закрыть диалоговое окно **Добавление и удаление оснасток** .</span><span class="sxs-lookup"><span data-stu-id="56c7a-148">Click **OK** to commit the selection and close the **Add or Remove Snap-ins** dialog.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="56c7a-149">Если сертификат не отображается на консоли, убедитесь, что вы не выбрали пользователя или службу.</span><span class="sxs-lookup"><span data-stu-id="56c7a-149">If the certificate does not show up in the console, ensure that you have not selected User or Service.</span></span> <span data-ttu-id="56c7a-150">Необходимо выбрать компьютер, или вы не сможете найти сертификат probper.</span><span class="sxs-lookup"><span data-stu-id="56c7a-150">You must select Computer, or you will not be able to locate the probper certificate.</span></span>

    
    </div>

9.  <span data-ttu-id="56c7a-151">Чтобы просмотреть свойства сертификата, разверните раздел **Сертификаты** и выберите пункт **Личные**, а затем — **Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-151">To view the properties of the certificate, expand **Certificates**, expand **Personal**, and select **Certificates**.</span></span> <span data-ttu-id="56c7a-152">Выберите сертификат для просмотра, щелкните сертификат правой кнопкой мыши и выберите команду **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-152">Select the certificate to view, right-click on the certificate and select **Open**.</span></span>

10. <span data-ttu-id="56c7a-153">В представлении **сертификата** выберите **сведения**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-153">In the **Certificate** view, select **Details**.</span></span> <span data-ttu-id="56c7a-154">Здесь вы можете выбрать имя субъекта сертификата, выделив **тему** , а также отобразить назначенное имя субъекта и связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="56c7a-154">From here, you can select the certificate subject name by selecting **Subject** and the assigned subject name and associated properties are displayed.</span></span>

11. <span data-ttu-id="56c7a-155">Чтобы просмотреть назначенные альтернативные имена для темы, выберите **дополнительное имя субъекта**.</span><span class="sxs-lookup"><span data-stu-id="56c7a-155">To view the assigned subject alternative names, select **Subject Alternative Name**.</span></span> <span data-ttu-id="56c7a-156">Отображаются все назначенные альтернативные имена для темы.</span><span class="sxs-lookup"><span data-stu-id="56c7a-156">All assigned subject alternative names are displayed.</span></span> <span data-ttu-id="56c7a-157">По умолчанию в качестве альтернативных имен для темы, которые находятся в свойстве, используется **DNS-имя** .</span><span class="sxs-lookup"><span data-stu-id="56c7a-157">The subject alternative names that are found in the property are of type **DNS Name** by default.</span></span> <span data-ttu-id="56c7a-158">Должны отобразиться следующие участники (все должны быть полные доменные имена, представленные в DNS-адресах (а или, если записи IPv6 AAAA).</span><span class="sxs-lookup"><span data-stu-id="56c7a-158">You should see the following members (all of which should be fully qualified domain names as represented in DNS host (A or, if IPv6 AAAA) records:</span></span>
    
      - <span data-ttu-id="56c7a-159">Имя пула для этого пула или имя одного сервера, если он не является пулом.</span><span class="sxs-lookup"><span data-stu-id="56c7a-159">Pool name for this pool, or the single server name if this is not a pool</span></span>
    
      - <span data-ttu-id="56c7a-160">Имя сервера, которому назначен сертификат</span><span class="sxs-lookup"><span data-stu-id="56c7a-160">Server name that the certificate is assigned to</span></span>
    
      - <span data-ttu-id="56c7a-161">Простые URL-записи, обычно соответствующие требованиям и набору номера</span><span class="sxs-lookup"><span data-stu-id="56c7a-161">Simple URL records, typically meet and dialin</span></span>
    
      - <span data-ttu-id="56c7a-162">Внутренние имена внутренних и веб-служб (например, webpool01.contoso.net, webpool01.contoso.com), основанные на вариантах, сделанных в построителе топологии, и переопределяемые выборы веб-служб.</span><span class="sxs-lookup"><span data-stu-id="56c7a-162">Web services internal and Web services external names (for example, webpool01.contoso.net, webpool01.contoso.com), based on choices made in Topology Builder and over-ridden web services selections.</span></span>
    
      - <span data-ttu-id="56c7a-163">Если уже назначено, lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="56c7a-163">If already assigned, the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="56c7a-164">и lyncdiscoverinternal.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="56c7a-164">and lyncdiscoverinternal.\<sipdomain\></span></span> <span data-ttu-id="56c7a-165">строк.</span><span class="sxs-lookup"><span data-stu-id="56c7a-165">records.</span></span>
    
    <span data-ttu-id="56c7a-166">Последний элемент является наиболее подинтересен – если имеется lyncdiscover и lyncdiscoverinternal сеть SAN.</span><span class="sxs-lookup"><span data-stu-id="56c7a-166">The last item is what you are most interested in – if there is a lyncdiscover and lyncdiscoverinternal SAN entry.</span></span>
    
    <span data-ttu-id="56c7a-167">После получения этих сведений вы можете закрыть представление сертификата и MMC.</span><span class="sxs-lookup"><span data-stu-id="56c7a-167">Once you have this information, you can close the certificate view and the MMC.</span></span>

12. <span data-ttu-id="56c7a-168">Если служба автообнаружения, то есть lyncdiscover. \> доменное имя \> и lyncdiscoverinternal.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="56c7a-168">If an Autodiscover Service, meaning the lyncdiscover.\>domain name\> and lyncdiscoverinternal.\<domain name\></span></span> <span data-ttu-id="56c7a-169">(в зависимости от того, является ли это внешнему или внутренним сертификатом), отсутствует альтернативное имя субъекта, и вы используете один сертификат по умолчанию для типов по умолчанию, WebServicesInternal и WebServiceExternal, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="56c7a-169">(based on if this is an external or internal certificate) subject alternative name is missing, and you are using a single Default certificate for the Default, WebServicesInternal and WebServiceExternal types, do the following:</span></span>
    
      - <span data-ttu-id="56c7a-170">В командной строке оболочки Lync Server Management Shell введите:</span><span class="sxs-lookup"><span data-stu-id="56c7a-170">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="56c7a-171">Если у вас много доменов SIP, вы не можете использовать новый параметр AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="56c7a-171">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="56c7a-172">Вместо этого необходимо использовать параметр DomainName.</span><span class="sxs-lookup"><span data-stu-id="56c7a-172">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="56c7a-173">Если вы используете параметр DomainName, необходимо определить полные доменные имена для записей lyncdiscoverinternal и lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="56c7a-173">When you use the DomainName parameter, you must define the FQDN for the lyncdiscoverinternal and lyncdiscover records.</span></span> <span data-ttu-id="56c7a-174">Например:</span><span class="sxs-lookup"><span data-stu-id="56c7a-174">For example:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="56c7a-175">Чтобы назначить сертификат, введите следующее:</span><span class="sxs-lookup"><span data-stu-id="56c7a-175">To assign the certificate, type the following:</span></span>
        
            Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="56c7a-176">Где "отпечаток" — это отпечаток для нового выданного сертификата.</span><span class="sxs-lookup"><span data-stu-id="56c7a-176">Where “Thumbprint” is the thumbprint displayed for the newly issued certificate.</span></span>

13. <span data-ttu-id="56c7a-177">Для отсутствующего альтернативных имен субъектов автообнаружения при использовании отдельных сертификатов для параметров по умолчанию, WebServicesInternal и WebServicesExternal выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="56c7a-177">For a missing internal Autodiscover subject alternative names when using separate certificates for Default, WebServicesInternal, and WebServicesExternal, do the following:</span></span>
    
      - <span data-ttu-id="56c7a-178">В командной строке оболочки Lync Server Management Shell введите:</span><span class="sxs-lookup"><span data-stu-id="56c7a-178">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="56c7a-179">Если у вас много доменов SIP, вы не можете использовать новый параметр AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="56c7a-179">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="56c7a-180">Вместо этого необходимо использовать параметр DomainName.</span><span class="sxs-lookup"><span data-stu-id="56c7a-180">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="56c7a-181">Если вы используете параметр DomainName, необходимо использовать соответствующий префикс для полного доменного имени домена SIP.</span><span class="sxs-lookup"><span data-stu-id="56c7a-181">When you use the DomainName parameter, you must use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="56c7a-182">Например:</span><span class="sxs-lookup"><span data-stu-id="56c7a-182">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="56c7a-183">Чтобы получить отсутствующее дополнительное имя для субъекта автообнаружения, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="56c7a-183">For a missing external Autodiscover subject alternative name, at the command line, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="56c7a-184">Если у вас много доменов SIP, вы не можете использовать новый параметр AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="56c7a-184">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="56c7a-185">Вместо этого необходимо использовать параметр DomainName.</span><span class="sxs-lookup"><span data-stu-id="56c7a-185">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="56c7a-186">Если вы используете параметр DomainName, необходимо использовать соответствующий префикс для полного доменного имени домена SIP.</span><span class="sxs-lookup"><span data-stu-id="56c7a-186">When you use the DomainName parameter, you must use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="56c7a-187">Например:</span><span class="sxs-lookup"><span data-stu-id="56c7a-187">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -DomainName "Lyncdiscover.contoso.com, Lyncdiscover.contoso.net" -verbose
    
      - <span data-ttu-id="56c7a-188">Чтобы назначить индивидуальные типы сертификатов, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="56c7a-188">To assign the individual certificate types, type the following:</span></span>
        
            Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="56c7a-189">Где "отпечаток" — это отпечаток для вновь выданных индивидуальных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="56c7a-189">Where “Thumbprint” is the thumbprint displayed for the newly issued individual certificates.</span></span>

<span data-ttu-id="56c7a-190"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56c7a-190"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

