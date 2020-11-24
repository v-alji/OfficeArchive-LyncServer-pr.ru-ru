---
title: 'Lync Server 2013: использование Microsoft SQL Server 2008 R2 в качестве базы данных System Center Operations Manager'
description: 'Lync Server 2013: использование Microsoft SQL Server 2008 R2 в качестве базы данных System Center Operations Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database
ms:assetid: 0efe76da-8854-499e-bdc7-3623244a8e85
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687969(v=OCS.15)
ms:contentKeyID: 49733555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 870c079e7e5e871fc62358e9bdd21653193fad7c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399430"
---
# <a name="using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database-for-lync-server-2013"></a><span data-ttu-id="af0b6-103">Использование Microsoft SQL Server 2008 R2 в качестве базы данных System Center Operations Manager для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af0b6-103">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af0b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af0b6-104">

<span> </span></span></span>

<span data-ttu-id="af0b6-105">_**Тема последнего изменения:** 2013-07-29_</span><span class="sxs-lookup"><span data-stu-id="af0b6-105">_**Topic Last Modified:** 2013-07-29_</span></span>

<span data-ttu-id="af0b6-106">Чтобы использовать в качестве серверной части базу данных SQL Server 2008 R2, выполните действия, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="af0b6-106">To use SQL Server 2008 R2 as your back-end database, complete the steps detailed in this topic.</span></span>

<div>

## <a name="configuring-sql-server-2008-r2-and-sql-server-reporting-services"></a><span data-ttu-id="af0b6-107">Настройка SQL Server 2008 R2 и служб SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="af0b6-107">Configuring SQL Server 2008 R2 and SQL Server Reporting Services</span></span>

<span data-ttu-id="af0b6-108">Прежде чем приступить к установке System Center Operations Manager, вы должны внести два изменения в сервер SQL Server 2008 R2 и настройку служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="af0b6-108">Before you begin installing System Center Operations Manager you must make two changes to your SQL Server 2008 R2 and your SQL Server Reporting Services configuration.</span></span> <span data-ttu-id="af0b6-109">(Эти изменения необходимы только в том случае, если в качестве базы данных Operations Manager используется SQL Server 2008 R2). Для начала сделайте следующее на компьютере, на котором будет размещена база данных Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="af0b6-109">(These changes are required only if you are using SQL Server 2008 R2 as your Operations Manager database.) First, do the following on the computer that will host your Operations Manager database:</span></span>

1.  <span data-ttu-id="af0b6-110">Нажмите кнопку **Пуск** и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-110">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="af0b6-111">В диалоговом окне **выполнить** введите **C: \\ Program Files \\ Microsoft SQL Server \\ MSRS10 \_ 50. ARCHINST \\ Reporting Services \\ ReportServer** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="af0b6-111">In the **Run** dialog box, type **C:\\Program Files\\Microsoft SQL Server\\ MSRS10\_50.ARCHINST\\Reporting Services\\ReportServer** and then press ENTER.</span></span>

3.  <span data-ttu-id="af0b6-112">В папке **ReportServer** откройте файл **rsreportserver.config** в блокноте или любом другом текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="af0b6-112">In the **ReportServer** folder, open the file **rsreportserver.config** in Notepad or any other text editor.</span></span>

4.  <span data-ttu-id="af0b6-113">В начале файла будет показан ряд узлов "добавить ключ".</span><span class="sxs-lookup"><span data-stu-id="af0b6-113">Near the beginning of the file you will see a series of "Add Key" nodes.</span></span> <span data-ttu-id="af0b6-114">Найдите запись, которая начинается с **\< ключевого слова Add = "SecureConnectionLevel"** , и установите для параметра значение **0**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-114">Find the entry that begins **\<Add Key="SecureConnectionLevel"** and set the value to **0**:</span></span>
    
        <Add Key="SecureConnectionLevel" Value="0"/>

5.  <span data-ttu-id="af0b6-115">Сохраните файл **rsreportserver.config** и закройте текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="af0b6-115">Save the file **rsreportserver.config** and then close your text editor.</span></span>

<span data-ttu-id="af0b6-116">После обновления файла конфигурации сервера отчетов необходимо назначить для служб SQL Server Reporting Services правильный сертификат.</span><span class="sxs-lookup"><span data-stu-id="af0b6-116">After updating the Report Server configuration file you must then assign the correct certificate to SQL Server Reporting Services.</span></span> <span data-ttu-id="af0b6-117">Для этого:</span><span class="sxs-lookup"><span data-stu-id="af0b6-117">To do that:</span></span>

1.  <span data-ttu-id="af0b6-118">Нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft SQL Server 2008 R2**, выберите пункт **средства настройки**, а затем — **Диспетчер конфигурации служб Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-118">Click **Start**, click **All Programs**, click **Microsoft SQL Server 2008 R2**, click **Configuration Tools**, and then click **Reporting Services Configuration Manager**.</span></span>

2.  <span data-ttu-id="af0b6-119">В диалоговом окне **Подключение к конфигурации служб Reporting Services** убедитесь в том, что имя сервера отображается в поле **имя сервера** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-119">In the **Reporting Services Configuration Connection** dialog box, make sure that the name of your server appears in the **Server Name** box.</span></span> <span data-ttu-id="af0b6-120">Выберите экземпляр SQL Server, на котором будет размещена база данных Operations Manager (например, **ARCHINST**), из раскрывающегося списка **экземпляр сервера отчетов** и нажмите кнопку **подключить**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-120">Select the SQL Server instance that will host your Operations Manager database (for example, **ARCHINST**) from the **Report Server Instance** drop-down list and then click **Connect**.</span></span>

3.  <span data-ttu-id="af0b6-121">В диспетчере конфигураций служб Reporting Services щелкните **URL-адрес Web Service**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-121">In Reporting Services Configuration Manager, click **Web Service URL**.</span></span>

4.  <span data-ttu-id="af0b6-122">На странице **URL веб-служба** выберите сертификат, который будет использоваться в службах отчетов в раскрывающемся списке **сертификата SSL** , и нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-122">On the **Web Service URL** page, select the certificate to be used for your Reporting Services from the **SSL Certificate** dropdown list and then click **Apply**.</span></span> <span data-ttu-id="af0b6-123">Через несколько секунд вы увидите пару URL-адресов, которые указаны в разделе **URL — ссылки на службы сервера отчетов**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-123">After a few seconds, you will see a pair of URLs listed under **Report Server Web Service URLs**.</span></span>

5.  <span data-ttu-id="af0b6-124">Щелкните оба URL-адреса, чтобы убедиться, что у вас есть доступ к службам SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="af0b6-124">Click both of the URLs to verify that you can access SQL Server Reporting Services.</span></span>

6.  <span data-ttu-id="af0b6-125">Закройте Диспетчер конфигураций служб Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="af0b6-125">Close Reporting Services Configuration Manager.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-database-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="af0b6-126">Создание базы данных System Center Operations Manager для использования с SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af0b6-126">Creating a System Center Operations Manager database for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="af0b6-127">Если вы хотите настроить System Center Operations Manager на использование базы данных SQL Server 2008 R2, вам потребуется выполнить вручную создание базы данных Operations Manager на компьютере с SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="af0b6-127">If you want to configure System Center Operations Manager to use a SQL Server 2008 R2 database, you will need to "manually" create the Operations Manager database on the computer running SQL Server 2008 R2.</span></span> <span data-ttu-id="af0b6-128">(Опять же, эти действия не требуются, если в качестве серверной базы данных используется SQL Server 2005 или SQL Server 2008.)</span><span class="sxs-lookup"><span data-stu-id="af0b6-128">(Again, these steps are not required if you are using SQL Server 2005 or SQL Server 2008 as your back-end database.)</span></span>

<span data-ttu-id="af0b6-129">Чтобы вручную создать базу данных Operations Manager, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="af0b6-129">To manually create an Operations Manager database do the following:</span></span>

1.  <span data-ttu-id="af0b6-130">На странице System Center Operations Manager 2007 R2 с помощью установочного носителя в \\ папке SupportTools AMD64 дважды щелкните **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-130">On the System Center Operations Manager 2007 R2 setup media, in the SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="af0b6-131">В мастере настройки базы данных на странице **Добро пожаловать в мастер настройки базы данных** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-131">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="af0b6-132">На странице **сведения о базе данных** оставьте все параметры как есть и нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-132">On the **Database Information** page leave all the settings as-is and then click **Next**</span></span>

4.  <span data-ttu-id="af0b6-133">На странице **Конфигурация группы управления** введите имя группы управления (например, " **наблюдение за Lync Server**") в поле **имя группы управления** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-133">On the **Management Group Configuration** page type a name for your Management Group (for example, **Lync Server Monitoring**) in the **Management Group name** box and then click **Next**.</span></span>

5.  <span data-ttu-id="af0b6-134">На странице " **отчеты об ошибках Operations Manager** " нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-134">On the **Operations Manager Error Reports** page click **Next**.</span></span>

6.  <span data-ttu-id="af0b6-135">На странице **Сводка** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-135">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-data-warehouse-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="af0b6-136">Создание хранилища данных System Center Operations Manager для использования с SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af0b6-136">Creating a System Center Operations Manager data warehouse for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="af0b6-137">Microsoft Lync Server 2013 поставляется с тремя новыми отчетами System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="af0b6-137">Microsoft Lync Server 2013 ships with three new System Center Operations Manager reports:</span></span>

  - <span data-ttu-id="af0b6-138">**Отчет о доступности сценариев "на**   конец"   В этом отчете подробно описана доступность и время бесперебойной работы для основных служб Lync Server, таких как регистрация или присутствие.</span><span class="sxs-lookup"><span data-stu-id="af0b6-138">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="af0b6-139">**Отчет о произв**   .   С помощью данных счетчиков производительности этот отчет показывает тенденции для системных компонентов, таких как доступность памяти и использование процессора.</span><span class="sxs-lookup"><span data-stu-id="af0b6-139">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="af0b6-140">**Отчет о компонентах**   В этом отчете перечислены основные генераторы оповещений, сгруппированные по компоненту Lync Server.</span><span class="sxs-lookup"><span data-stu-id="af0b6-140">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="af0b6-141">Для использования этих новых отчетов необходимо установить хранилище данных System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="af0b6-141">In order to use these new reports you must install a System Center Operations Manager data warehouse.</span></span> <span data-ttu-id="af0b6-142">(Хранилище данных обеспечивает долгосрочное хранение данных операций.) Для использования хранилища данных с SQL Server 2008 R2 необходимо выполнить следующие действия на компьютере, на котором размещается база данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af0b6-142">(A data warehouse provides for long-term storage of operations data.) To use a data warehouse with SQL Server 2008 R2 you must carry out the following steps on the computer that hosts your SQL Server database:</span></span>

1.  <span data-ttu-id="af0b6-143">На носителе с программой установки System Center Operations Manager в \\ папке Setup SupportTools \\ AMD64 дважды щелкните **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-143">On the System Center Operations Manager setup media, in the Setup\\SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="af0b6-144">В мастере настройки базы данных на странице **Добро пожаловать в мастер настройки базы данных** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-144">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="af0b6-145">На странице **сведения о базе данных** выберите **базу данных хранилища данных Operations Manager** из раскрывающегося списка **тип базы данных** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-145">On the **Database Information** page, select **Operations Manager Data Warehouse Database** from the **Database Type** dropdown list and then click **Next**.</span></span>

4.  <span data-ttu-id="af0b6-146">На странице **Сводка** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-146">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="installing-the-system-center-operations-manager-console"></a><span data-ttu-id="af0b6-147">Установка консоли System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="af0b6-147">Installing the System Center Operations Manager console</span></span>

<span data-ttu-id="af0b6-148">Консоль Operations Manager — это основное средство, используемое для управления System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="af0b6-148">The Operations Manager console is the primary tool used to manage System Center Operations Manager.</span></span> <span data-ttu-id="af0b6-149">Перед установкой консоли Operations Manager убедитесь в том, что вы установили поддерживаемую версию SQL Server и службу SQL Server Reporting Service.</span><span class="sxs-lookup"><span data-stu-id="af0b6-149">Before you install the Operations Manager console, make sure that you have installed a supported version of SQL Server along with the SQL Server Reporting Service.</span></span> <span data-ttu-id="af0b6-150">Кроме того, для проверки правильности установки и настройки службы отчетов рекомендуется запустить диспетчер конфигурации служб отчетов SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af0b6-150">It is also recommended that you run SQL Server's Reporting Services Configuration Manager to verify that the Reporting Service has been correctly installed and configured.</span></span>

<span data-ttu-id="af0b6-151">Чтобы установить консоль System Center Operations Manager, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="af0b6-151">To install the System Center Operations Manager console:</span></span>

1.  <span data-ttu-id="af0b6-152">На носителе с программой установки System Center Operations Manager дважды щелкните **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-152">On the System Center Operations Manager setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="af0b6-153">В программе System Center Operations Manager 2007 R2 нажмите кнопку **проверить необходимые компоненты**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-153">In System Center Operations Manager 2007 R2 Setup, click **Check Prerequisites**.</span></span>

3.  <span data-ttu-id="af0b6-154">В средстве просмотра требований System Center Operations Manager выберите компоненты System Center, которые необходимо установить: (**сервер**; **Консоль**; и **PowerShell**), а затем нажмите кнопку **проверить**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-154">In the System Center Operations Manager Prerequisite Viewer, select the System Center components to be installed: (**Server**; **Console**; and **PowerShell**) and then click **Check**.</span></span> <span data-ttu-id="af0b6-155">Убедитесь, что блокирующие проблемы не обнаружены, и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-155">Verify that no blocking issues have been reported and then click **Close**.</span></span> <span data-ttu-id="af0b6-156">Если была обнаружена проблема с блокировкой, исправьте ее и нажмите кнопку **проверить** , чтобы повторно запустить проверку готовности.</span><span class="sxs-lookup"><span data-stu-id="af0b6-156">If a blocking issue has been reported, correct the problem and then click **Check** to re-run the prerequisite testing.</span></span>

4.  <span data-ttu-id="af0b6-157">В программе System Center Operations Manager нажмите кнопку **установить Operations Manager**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-157">In System Center Operations Manager Setup, click **Install Operations Manager**.</span></span>

5.  <span data-ttu-id="af0b6-158">В мастере настройки System Center Operations Manager на странице **Добро пожаловать на страницу мастера установки System Center Operations Manager** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-158">In the System Center Operations Manager Setup wizard, on the **Welcome to the System Center Operations Manager Setup Wizard** page, click **Next**.</span></span>

6.  <span data-ttu-id="af0b6-159">На странице **лицензионного соглашения для конечных пользователей** выберите **я принимаю условия лицензионного соглашения** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-159">On the **End-User License Agreement** page, select **I accept the terms in the license agreement** and then click **Next**.</span></span>

7.  <span data-ttu-id="af0b6-160">На странице **Регистрация продукта** введите свое имя в поле **имя пользователя** и имя Организации в поле **Организация** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-160">On the **Product Registration** page, type your name in the **User Name** box and name of your organization in the **Organization** box.</span></span> <span data-ttu-id="af0b6-161">Введите ключ продукта System Center Operations Manager в поле **введите 25-значный ключ** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-161">Type your System Center Operations Manager product key in the **Enter your 25 digit CD Key** box and then click **Next**.</span></span>

8.  <span data-ttu-id="af0b6-162">На странице **Выборочная установка** выберите параметры System Center, которые нужно установить, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-162">On the **Custom Setup** page select the System Center options to be installed and then click **Next**.</span></span> <span data-ttu-id="af0b6-163">Необходимо выбрать **сервер управления**, **пользовательские интерфейсы** и **веб-консоль** для установки.</span><span class="sxs-lookup"><span data-stu-id="af0b6-163">You should select **Management Server**, **User Interfaces**, and **Web Console** to be installed.</span></span> <span data-ttu-id="af0b6-164">**Базу данных** не следует выделять и не нужно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="af0b6-164">**Database** should not be selected and should not be installed.</span></span>

9.  <span data-ttu-id="af0b6-165">На странице **экземпляр сервера базы данных SC** убедитесь в том, что имя компьютера, на котором установлены базы данных Operations Manager, отображается в поле **сервер System Center Database Server** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-165">On the **SC Database Server Instance** page, verify that the name of the computer where the Operations Manager databases are installed appears in the **System Center Database Server** box.</span></span> <span data-ttu-id="af0b6-166">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-166">Click **Next**.</span></span>

10. <span data-ttu-id="af0b6-167">На странице **учетной записи действия сервера управления** выберите **Доменная или локальная учетная запись компьютера** , а затем введите нужные значения в поля **учетная запись пользователя**, **пароль**, **домен или локальный компьютер** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-167">On the **Management Server Action Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="af0b6-168">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-168">Click **Next**.</span></span>

11. <span data-ttu-id="af0b6-169">На странице **SDK и учетной записи службы настройки** выберите **Доменная или локальная учетная запись компьютера** , а затем введите нужные значения в поля **учетная запись пользователя**, **пароль**, **домен или локальный компьютер** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-169">On the **SDK and Config Service Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="af0b6-170">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-170">Click **Next**.</span></span>

12. <span data-ttu-id="af0b6-171">На странице " **отчеты об ошибках Operations Manager** " нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-171">On the **Operations Manager Error Reports** page click **Next**.</span></span>

13. <span data-ttu-id="af0b6-172">На странице **программы улучшения качества программного** обеспечения нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-172">On the **Customer Experience Improvement Program** page click **Next**.</span></span>

14. <span data-ttu-id="af0b6-173">На странице **готовность к установке программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-173">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="af0b6-174">На странице **Завершение установки System Center Operations Manager** снимите флажок **резервное копирование ключа шифрования** и установите **флажки для консоли** и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-174">On the **Completing the System Center Operations Manager Setup** page, clear the **Backup Encryption Key** and **Start the console checkboxes** and then click **Finish**.</span></span>

16. <span data-ttu-id="af0b6-175">В программе System Center Operations Manager щелкните **выход**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-175">In System Center Operations Manager Setup click **Exit**.</span></span>

</div>

<div>

## <a name="installing-system-center-reporting-services"></a><span data-ttu-id="af0b6-176">Установка служб отчетов System Center</span><span class="sxs-lookup"><span data-stu-id="af0b6-176">Installing System Center Reporting Services</span></span>

<span data-ttu-id="af0b6-177">После установки и настройки консоли System Center Operations Manager необходимо установить System Center Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="af0b6-177">After installing and configuring the System Center Operations Manager console you must then install System Center Reporting Services.</span></span> <span data-ttu-id="af0b6-178">Если в качестве серверной базы данных Operations Manager используется SQL Server 2008 R2, это означает, что вы должны сначала внести временное изменение в группу безопасности, связанную со службами SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="af0b6-178">If you are using SQL Server 2008 R2 as your Operations Manager back-end database, that means that you must first make a temporary change to the security group associated with SQL Server Reporting Services.</span></span> <span data-ttu-id="af0b6-179">Если вы используете SQL Server 2008 R2, необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="af0b6-179">If you are using SQL Server 2008 R2, you must do the following:</span></span>

1.  <span data-ttu-id="af0b6-180">Нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Диспетчер сервера**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-180">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="af0b6-181">В диспетчере серверов разверните узел **Конфигурация**, разверните раздел **Локальные пользователи и группы**, а затем выберите пункт **группы**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-181">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="af0b6-182">Найдите следующую группу, в которой ATL-SC-001 представляет имя вашего компьютера и ARCHINST представляет экземпляр SQL Server для базы данных System Center: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-182">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the System Center database: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

4.  <span data-ttu-id="af0b6-183">Щелкните группу правой кнопкой мыши и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-183">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="af0b6-184">Переименуйте группу, удалив **\_ 50** из имени группы.</span><span class="sxs-lookup"><span data-stu-id="af0b6-184">Rename the group by deleting **\_50** from the group name.</span></span> <span data-ttu-id="af0b6-185">Например: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-185">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

5.  <span data-ttu-id="af0b6-186">Закройте Диспетчер серверов.</span><span class="sxs-lookup"><span data-stu-id="af0b6-186">Close Server Manager.</span></span>

<span data-ttu-id="af0b6-187">На этом этапе вы можете установить службы отчетов System Center.</span><span class="sxs-lookup"><span data-stu-id="af0b6-187">At this point you are ready to install System Center Reporting Services.</span></span> <span data-ttu-id="af0b6-188">Для этого выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="af0b6-188">To do this:</span></span>

1.  <span data-ttu-id="af0b6-189">На диске System Center Operations Manager 2007 R2 дважды щелкните **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-189">On the System Center Operations Manager 2007 R2 Setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="af0b6-190">В программе System Center Operations Manager 2007 R2 щелкните **установить Отчеты Operations Manager**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-190">In System Center Operations Manager 2007 R2 Setup, click **Install Operations Manager Reporting**.</span></span>

3.  <span data-ttu-id="af0b6-191">В мастере настройки отчетов System Center Operations Manager 2007 R2 на странице **Добро пожаловать в отчеты Operations Manager Настройка** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-191">In the System Center Operations Manager 2007 R2 Reporting Setup wizard, on the **Welcome to Operations Manager Reporting Setup** page, click **Next**.</span></span>

4.  <span data-ttu-id="af0b6-192">На странице **лицензионного соглашения для конечных пользователей** установите флажок **я принимаю условия лицензионного соглашения** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-192">On the **End-user License Agreement** page select **I accept the terms of the license agreement** and then click **Next**.</span></span>

5.  <span data-ttu-id="af0b6-193">На странице **Регистрация продукта** убедитесь, что имя и имя вашей организации указаны в полях **имя пользователя** и **Организация** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-193">On the **Product Registration** page, ensure that your name and the name of your organization appear in the **User Name** and **Organization** boxes and then click **Next**.</span></span>

6.  <span data-ttu-id="af0b6-194">На странице **Выборочная настройка** выберите пункт **сервер отчетов** , а затем — **этот компонент и все зависимые компоненты будут установлены на локальном жестком** диске.</span><span class="sxs-lookup"><span data-stu-id="af0b6-194">On the **Custom Setup** page, click **Reporting Server** and select **This component, and all dependent components, will be installed on local disk drive**.</span></span> <span data-ttu-id="af0b6-195">Нажмите кнопку **хранилище данных** и выберите **этот компонент будет недоступен**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-195">Click **Data Warehouse** and select **This component will not be available**, and then click **Next**.</span></span>

7.  <span data-ttu-id="af0b6-196">На странице **Подключение к корневому серверу управления** введите имя корневого сервера управления Operations Manager в поле **корневой сервер управления** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-196">On the **Connect to the Root Management Server** page, type the name of your Operations Manager root management server in the **Root Management Server** box and then click **Next**.</span></span>

8.  <span data-ttu-id="af0b6-197">На странице **Подключение к хранилищу данных Operations Manager** введите экземпляр SQL Server, на котором находится хранилище данных, в поле **экземпляр SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-197">On the **Connect to the Operations Manager Data Warehouse** page, type the SQL Server instance where your data warehouse is located in the **SQL Server Instance** box.</span></span> <span data-ttu-id="af0b6-198">(Если хранилище данных находится в экземпляре по умолчанию, просто введите имя сервера, например ATL-SQL-001.) Убедитесь в том, что имя базы данных **OperationsManagerDW** отображается в поле **имя** , а этот порт **1433** отображается в поле Port ( **порт) сервера SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-198">(If your data warehouse is located in the Default instance then simply type the server name; for example: atl-sql-001.) Verify that the database name **OperationsManagerDW** appears in the **Name** box, and that port **1433** appears in the **SQL Server port** box.</span></span> <span data-ttu-id="af0b6-199">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-199">Click **Next**.</span></span>

9.  <span data-ttu-id="af0b6-200">На странице **экземпляра SQL Server Reporting** выберите сервер отчетов SQL Server из раскрывающегося списка **введите сервер служб SQL Server Reporting Services** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-200">On the **SQL Server Reporting Instance** page, select your SQL Server reporting server from the **Enter the SQL Server Reporting Services Server** dropdown list and then click **Next**.</span></span>

10. <span data-ttu-id="af0b6-201">На странице запись **учетной записи хранилища данных** введите имя и пароль пользователя, которому должны быть первоначально назначены разрешения на запись в хранилище данных в полях **учетная запись пользователя** и **пароль** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-201">On the **Data Warehouse Write Account** page, enter the name and password of the user to be initially assigned write permissions to the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="af0b6-202">Выберите домен пользователя из раскрывающегося списка **домен** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-202">Select the user's domain from the **Domain** dropdown list and then click **Next**.</span></span>

11. <span data-ttu-id="af0b6-203">На странице **учетной записи средства чтения данных** введите имя и пароль учетной записи пользователя, которая будет использоваться при запросе службами SQL Reporting Services хранилища данных в полях **учетной записи пользователя** и **пароля** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-203">On the **Data Reader Account** page, enter the name and password of the user account to be used when SQL Reporting Services queries the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="af0b6-204">Выберите домен учетной записи из раскрывающегося списка **домена** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-204">Select the account domain from the **Domain** dropdown list and then click **Next**.</span></span>

12. <span data-ttu-id="af0b6-205">На странице **оперативные отчеты данных** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-205">On the **Operational Data Reports** page, click **Next**.</span></span>

13. <span data-ttu-id="af0b6-206">На странице **центра обновления Майкрософт** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-206">On the **Microsoft Update** page, click **Next**.</span></span>

14. <span data-ttu-id="af0b6-207">На странице **готовность к установке программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-207">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="af0b6-208">На странице **Завершение работы мастера настройки компонентов отчетов Operations Manager** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-208">On the **Completing the Operations Manager Reporting Components Setup Wizard** page, click **Finish**.</span></span>

16. <span data-ttu-id="af0b6-209">В программе System Center Operations Manager 2007 R2 нажмите кнопку **выход**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-209">In System Center Operations Manager 2007 R2 Setup, click **Exit**.</span></span>

<span data-ttu-id="af0b6-210">После установки System Center Reporting вы можете сбросить имя группы безопасности, связанной с отчетом SQL Server, с помощью описанной ниже процедуры.</span><span class="sxs-lookup"><span data-stu-id="af0b6-210">After System Center reporting has been installed you then use the following procedure to reset the name of the security group associated with SQL Server reporting.</span></span> <span data-ttu-id="af0b6-211">Эта процедура может потребоваться, только если вы используете SQL Server:</span><span class="sxs-lookup"><span data-stu-id="af0b6-211">Again, this procedure is only required if you are using SQL Server:</span></span>

1.  <span data-ttu-id="af0b6-212">Нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем — **Диспетчер сервера**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-212">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="af0b6-213">В диспетчере серверов разверните узел **Конфигурация**, разверните раздел **Локальные пользователи и группы**, а затем выберите пункт **группы**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-213">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="af0b6-214">Найдите следующую группу, в которой ATL-SC-001 представляет имя вашего компьютера и ARCHINST представляет экземпляр SQL Server для баз данных архивации и мониторинга: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-214">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the archiving and monitoring databases: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

4.  <span data-ttu-id="af0b6-215">Щелкните группу правой кнопкой мыши и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-215">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="af0b6-216">Переименуйте группу, добавив **\_ 50** в конец имени группы, прямо перед именем экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af0b6-216">Rename the group by adding **\_50** to the end of the group name, right before the SQL Server instance name.</span></span> <span data-ttu-id="af0b6-217">Например: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="af0b6-217">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

5.  <span data-ttu-id="af0b6-218">Закройте Диспетчер серверов.</span><span class="sxs-lookup"><span data-stu-id="af0b6-218">Close Server Manager.</span></span>

<span data-ttu-id="af0b6-219">Если открыта консоль Operations Center, необходимо закрыть приложение, а затем перезапустить его. Если этого не сделать, вкладка " **отчеты** " не появится в пользовательском интерфейсе консоли операций.</span><span class="sxs-lookup"><span data-stu-id="af0b6-219">If the System Center Operations Console is open you will need to close the application and then restart it; if you do not do this the **Reporting** tab will not appear in the Operations Console user interface.</span></span> <span data-ttu-id="af0b6-220">Обратите внимание, что после первого запуска консоли операций может пройти несколько минут, прежде чем все отчеты наблюдения будут отображены на вкладке **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="af0b6-220">Note that, after restarting the Operations Console the first time, it could take several minutes before all the Monitoring Reports appear on the **Reporting** tab.</span></span>

<span data-ttu-id="af0b6-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af0b6-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

