---
title: Развертывание нестандартного порта SQL Server и псевдонима в Lync Server 2013
description: Развертывание нестандартного порта и псевдонима SQL Server в Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a SQL Server nonstandard port and alias in Lync Server 2013
ms:assetid: 2da92c1f-250e-407a-8651-fb2aec76aeb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn776290(v=OCS.15)
ms:contentKeyID: 62634609
ms.date: 09/17/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da76db2b946a47e13fe3549d7184b0b12894a83a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398263"
---
# <a name="deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="c045a-103">Развертывание нестандартного порта SQL Server и псевдонима в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c045a-103">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c045a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c045a-104">

<span> </span></span></span>

<span data-ttu-id="c045a-105">_**Тема последнего изменения:** 2015-09-16_</span><span class="sxs-lookup"><span data-stu-id="c045a-105">_**Topic Last Modified:** 2015-09-16_</span></span>

<span data-ttu-id="c045a-106">Microsoft Lync Server 2013 поддерживает использование нестандартного порта и псевдонима в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-106">Microsoft Lync Server 2013 supports using a non-standard port and alias in SQL Server.</span></span> <span data-ttu-id="c045a-107">Использование нестандартного порта SQL Server и псевдоним повышает безопасность и создает более гибкую среду для развертывания Lync.</span><span class="sxs-lookup"><span data-stu-id="c045a-107">Using a SQL Server non-standard port and an alias increases security and creates a more flexible environment for the Lync deployment.</span></span> <span data-ttu-id="c045a-108">Эти действия являются единственным шагом в обеспечении надлежащей защиты среды Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c045a-108">These steps are only a single step in properly securing your Lync Server 2013 environment.</span></span> <span data-ttu-id="c045a-109">Чтобы уменьшить контактную зону реализации Lync Server 2013, необходимо предпринять дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="c045a-109">Additional steps should be taken to reduce the attack surface of a Lync Server 2013 implementation.</span></span>

<span data-ttu-id="c045a-110">В следующей статье описаны действия, которые необходимо выполнить для настройки нестандартного порта и псевдонима SQL Server в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c045a-110">The following article describes the steps required to setup a SQL Server non-standard port and alias in Lync Server 2013.</span></span>

<div>

## <a name="deploying-a-sql-server-non-standard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="c045a-111">Развертывание нестандартного порта и псевдонима SQL Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c045a-111">Deploying a SQL Server Non-Standard Port and Alias in Lync Server 2013</span></span>

<span data-ttu-id="c045a-112">Сервер Lync Server 2013 Topology Builder поддерживает использование псевдонима SQL Server в качестве полного доменного имени (FQDN) вместо фактического FQDN SQL Server при настройке Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c045a-112">Lync Server 2013 Topology Builder supports using a SQL Server alias as the Fully Qualified Domain Name (FQDN) instead of the actual SQL Server FQDN when configuring Lync Server 2013.</span></span> <span data-ttu-id="c045a-113">Это позволяет скрыть реальное полное доменное имя SQL Server от вредоносных злоумышленников.</span><span class="sxs-lookup"><span data-stu-id="c045a-113">This allows the actual SQL Server FQDN to be hidden from any malicious attacker.</span></span> <span data-ttu-id="c045a-114">Кроме того, использование нестандартного порта приводит к тому, что сам порт злоумышленника не попытается атаковать базу данных на стандартном порте 1433, как показано на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c045a-114">In addition, using a non-standard port obscures the actual port from any would be attacker attempting to attack the database on the standard port 1433, as shown in the following figure.</span></span>

<span data-ttu-id="c045a-115">![Злоумышленник не знает номер порта, чтобы атаковать.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "Злоумышленник не знает номер порта, чтобы атаковать.")</span><span class="sxs-lookup"><span data-stu-id="c045a-115">![A hacker doesn't know the port number to attack.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "A hacker doesn't know the port number to attack.")</span></span>

<span data-ttu-id="c045a-116">Чтобы получить успешный способ определения порта Lync Server 2013, который используется для взаимодействия с SQL Server, злоумышленнику потребуется проверить все порты, чтобы получать сведения о порте.</span><span class="sxs-lookup"><span data-stu-id="c045a-116">In order to be successful in determining the port Lync Server 2013 is using to communicate with SQL Server, the attacker would need to scan all ports to obtain the port information.</span></span> <span data-ttu-id="c045a-117">Просмотр порта злоумышленник повышает вероятность того, что система безопасности может обнаружить и остановить эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="c045a-117">A port scan by an attacker increases the chances that security can detect and stop the instruction.</span></span> <span data-ttu-id="c045a-118">Помимо добавления усиленной защиты с помощью нестандартного порта, вы также можете использовать псевдоним SQL Server для обеспечения гибкости развертывания.</span><span class="sxs-lookup"><span data-stu-id="c045a-118">In addition to adding increased security with a non-standard port, you can also use a SQL Server alias to provide flexibility for the deployment.</span></span> <span data-ttu-id="c045a-119">Это полезно, если вы хотите уменьшить изменения конфигурации в ситуациях, когда требуется изменить имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-119">This is valuable in order to reduce configuration changes in situations where a SQL Server name change is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c045a-120">В SQL Server имеется два метода обеспечения отказоустойчивости (отказоустойчивая кластеризация и зеркальное отображение).</span><span class="sxs-lookup"><span data-stu-id="c045a-120">SQL Server provides two fault tolerance methods (Failover Clustering and Mirroring).</span></span> <span data-ttu-id="c045a-121">Оба метода отказоустойчивости сервера SQL Server поддерживаются с помощью нестандартного порта и псевдонима сервера SQL Server с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c045a-121">Both SQL Server fault tolerance methods are supported using a SQL Server non-standard port and alias with Lync Server 2013.</span></span> <span data-ttu-id="c045a-122">Если серверная база данных SQL Server, используемая пулом, находится в зеркальной конфигурации, то служба браузера SQL на внутреннем сервере SQL Server должна выполняться для того, чтобы сервер переднего плана подключается к зеркальной, когда происходит сбой базы данных на зеркальном сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-122">If the SQL Server backend used by the pool is in a mirrored configuration, then the SQL browser service on the SQL Server backend servers should be running for Front End servers to connect to the mirrored database when the databases are failed over to the mirrored SQL Server.</span></span>



</div>

<span data-ttu-id="c045a-123">При настройке подключения к базам данных SQL Server из построителя топологии или при использовании командлета Install-CsDatabase невозможно явно определить нестандартный номер порта SQL Server и связать его с экземпляром SQL.</span><span class="sxs-lookup"><span data-stu-id="c045a-123">When configuring SQL Server database connectivity from within Topology Builder, or when using the Install-CsDatabase cmdlet, it’s not possible to explicitly define a SQL Server non-standard port number and associate it with a SQL instance.</span></span> <span data-ttu-id="c045a-124">Для задания нестандартного порта вам потребуется использовать сервер SQL Server и служебные программы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-124">To set a non-standard port, you’ll need to use SQL Server and Windows Server utilities.</span></span>

<span data-ttu-id="c045a-125">Чтобы настроить нестандартный порт и псевдоним SQL Server для использования с Lync Server 2013, вам потребуется выполнить три основные действия.</span><span class="sxs-lookup"><span data-stu-id="c045a-125">To set up a SQL Server non-standard port and alias for use with Lync Server 2013, you will need to complete three primary steps.</span></span> <span data-ttu-id="c045a-126">Эти действия описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-126">These steps are:</span></span>

  - <span data-ttu-id="c045a-127">Убедитесь, что к Lync Server 2013 применены последние обновления.</span><span class="sxs-lookup"><span data-stu-id="c045a-127">Confirm that Lync Server 2013 has the Latest Updates Applied.</span></span>

  - <span data-ttu-id="c045a-128">Настройка нестандартного порта и псевдонима SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-128">Setup the SQL Server Non-Standard Port and Alias.</span></span>

  - <span data-ttu-id="c045a-129">Настройте Lync Server 2013 с псевдонимом SQL Server с помощью Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="c045a-129">Configure Lync Server 2013 with the SQL Server alias using Topology Builder.</span></span>

  - <span data-ttu-id="c045a-130">Опубликуйте топологию и проверьте базу данных.</span><span class="sxs-lookup"><span data-stu-id="c045a-130">Publish the Topology, and Verify the Database.</span></span>

<div>

## <a name="confirm-that-lync-server-2013-has-the-latest-updates-applied"></a><span data-ttu-id="c045a-131">Подтверждение применения последних обновлений для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c045a-131">Confirm that Lync Server 2013 has the Latest Updates Applied</span></span>

<span data-ttu-id="c045a-132">Важно поддерживать приложение Lync Server 2013 в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c045a-132">It is important to keep Lync Server 2013 up to date.</span></span> <span data-ttu-id="c045a-133">Чтобы узнать о последних обновлениях и о том, как их применять, ознакомьтесь с разделами [обновления для Lync Server 2013](https://support.microsoft.com/kb/2809243).</span><span class="sxs-lookup"><span data-stu-id="c045a-133">To check for the most recent updates and information on how to apply them, see [Updates for Lync Server 2013](https://support.microsoft.com/kb/2809243).</span></span>

</div>

<div>

## <a name="setup-the-sql-server-non-standard-port-and-alias"></a><span data-ttu-id="c045a-134">Настройка нестандартного порта и псевдонима SQL Server</span><span class="sxs-lookup"><span data-stu-id="c045a-134">Setup the SQL Server Non-Standard Port and Alias</span></span>

<span data-ttu-id="c045a-135">Нестандартный порт и псевдоним SQL Server необходимо настроить в экземпляре базы данных, прежде чем на него можно будет ссылаться из сервера Lync Server 2013 Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="c045a-135">The SQL Server non-standard port and alias must be set up on the database instance before it can be referenced from Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="c045a-136">Для настройки нестандартного порта и псевдонима SQL Server вам потребуется выполнить три основные действия.</span><span class="sxs-lookup"><span data-stu-id="c045a-136">To set up a SQL Server non-standard port and alias, you will have to complete three primary steps.</span></span> <span data-ttu-id="c045a-137">Ниже указаны эти действия.</span><span class="sxs-lookup"><span data-stu-id="c045a-137">These steps are as follows:</span></span>

  - <span data-ttu-id="c045a-138">Измените значения по умолчанию для протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c045a-138">Change the Default TCP/IP Protocol Values.</span></span>

  - <span data-ttu-id="c045a-139">Создайте и настройте псевдоним SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-139">Create and Configure a SQL Server Alias.</span></span>

  - <span data-ttu-id="c045a-140">Создайте запись ресурса DNS с каноническим именем (CNAME).</span><span class="sxs-lookup"><span data-stu-id="c045a-140">Create a Domain Name System (DNS) Canonical Name (CNAME) Resource Record.</span></span>

<span data-ttu-id="c045a-141">**Изменение значений протокола TCP/IP, используемых по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="c045a-141">**Modify the Default TCP/IP Protocol Values**</span></span>

1.  <span data-ttu-id="c045a-142">Нажмите кнопку **Пуск** и выберите **Диспетчер конфигурации SQL Server**, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-142">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-143">![Значок SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Значок SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="c045a-143">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="c045a-144">В области навигации щелкните, чтобы развернуть **экземпляр SQL Server**, затем разверните **конфигурацию сети SQL Server** и выберите **протоколы для \<instance name\>**, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-144">In the navigation pane, choose to expand the **SQL Server instance**, choose to expand **SQL Server Network Configuration**, and choose **Protocols for \<instance name\>**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-145">![Перейти к свойствам TCP/IP](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Перейти к свойствам TCP/IP")</span><span class="sxs-lookup"><span data-stu-id="c045a-145">![Navigate to TCP/IP Properties](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navigate to TCP/IP Properties")</span></span>

3.  <span data-ttu-id="c045a-146">На правой панели щелкните правой кнопкой мыши **TCP/IP** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="c045a-146">In the right pane, right-click **TCP/IP**, and select **Properties**.</span></span> <span data-ttu-id="c045a-147">Откроется диалоговое окно "свойства TCP/IP".</span><span class="sxs-lookup"><span data-stu-id="c045a-147">The TCP/IP Properties dialog box is displayed.</span></span>

4.  <span data-ttu-id="c045a-148">Перейдите на вкладку **IP-адреса** . На вкладке адреса IP отображаются все активные IP-адреса на сервере.</span><span class="sxs-lookup"><span data-stu-id="c045a-148">Select the **IP Addresses** tab. The IP Addresses tab shows all of the active IP addresses on the server.</span></span> <span data-ttu-id="c045a-149">Эти данные находятся в формате IP1, IP2, до IPAll, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-149">These are in the format IP1, IP2, up to IPAll, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-150">![Откройте свойства TCP/IP.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Откройте свойства TCP/IP.")</span><span class="sxs-lookup"><span data-stu-id="c045a-150">![Open TCP/IP properties.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Open TCP/IP properties.")</span></span>

5.  <span data-ttu-id="c045a-151">Очистите поле **динамических портов TCP** для всех IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c045a-151">Clear the **TCP Dynamic Ports** field for all IP addresses.</span></span> <span data-ttu-id="c045a-152">Если поле содержит нулевой знак, это означает, что SQL Server прослушивает динамические порты.</span><span class="sxs-lookup"><span data-stu-id="c045a-152">If the field contains a zero character, then it means SQL Server is listening on dynamic ports.</span></span> <span data-ttu-id="c045a-153">Убедитесь, что эти поля очищены и не содержат нуль.</span><span class="sxs-lookup"><span data-stu-id="c045a-153">Make sure these fields are cleared and do not contain a zero.</span></span>

6.  <span data-ttu-id="c045a-154">Для IP-адреса, который Lync Server будет использовать для подключения к базе данных, убедитесь, что для **Enabled** задано значение **Да**, как показано на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c045a-154">For the IP address that Lync Server will be using to connect to the database, make sure that **Enabled** is set to **Yes**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-155">![Разрешите, задав "Да" для правильного IP-адреса.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Разрешите, задав "Да" для правильного IP-адреса.")</span><span class="sxs-lookup"><span data-stu-id="c045a-155">![Set enabled as Yes for the correct IP.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Set enabled as Yes for the correct IP.")</span></span>

7.  <span data-ttu-id="c045a-156">В разделе **IPAll** в нижней части диалогового окна введите нужный порт в поле **TCP Port (порт** ), как показано на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c045a-156">In the **IPAll** section at the bottom of the dialog, enter the desired port in the **TCP Port** field, as shown in the following figure.</span></span> <span data-ttu-id="c045a-157">В этом примере мы используем порт 50062, но можете использовать любой порт между 49152 и 65535.</span><span class="sxs-lookup"><span data-stu-id="c045a-157">In this example, we use port 50062, but you can use any port between 49152 and 65535.</span></span> <span data-ttu-id="c045a-158">Это порты, назначенные динамическому и частному использованию, и это гарантирует, что вы не будете конфликтовать с другими портами, используемыми в развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c045a-158">These are the ports assigned to dynamic and private use, and this ensures you won’t conflict with other ports being used in the Lync Server 2013 deployment.</span></span>
    
    <span data-ttu-id="c045a-159">![Задайте порт в разделе IPAll.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Задайте порт в разделе IPAll.")</span><span class="sxs-lookup"><span data-stu-id="c045a-159">![Set port in IPAll section.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Set port in IPAll section.")</span></span>

8.  <span data-ttu-id="c045a-160">Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно свойств TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c045a-160">Choose **OK** to exit the TCP/IP Properties dialog.</span></span>

9.  <span data-ttu-id="c045a-161">Перезапустите экземпляр SQL Server, выбрав пункт **службы SQL Server** на левой панели ДИСПЕТЧЕРА конфигурации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-161">Restart the SQL Server instance by selecting **SQL Server Services** in the left pane of SQL Server Configuration Manager.</span></span> <span data-ttu-id="c045a-162">Щелкните правой кнопкой мыши **SQL Server \<instance name\>** на правой панели и выберите команду **перезапустить**, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-162">Then right-click **SQL Server \<instance name\>** in the right pane, and select **Restart**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-163">![Выполните сброс службы SQL Server для экземпляра.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Выполните сброс службы SQL Server для экземпляра.")</span><span class="sxs-lookup"><span data-stu-id="c045a-163">![Reset the SQL Server service for instance.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Reset the SQL Server service for instance.")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c045a-164">Убедитесь, что вы обновили параметры брандмауэра для размещения нового порта SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-164">Make sure you update your firewall settings to accommodate the new SQL Server port.</span></span>



</div>

<span data-ttu-id="c045a-165">**Создание и Настройка псевдонима SQL Server**</span><span class="sxs-lookup"><span data-stu-id="c045a-165">**Create and Configure a SQL Server Alias**</span></span>

1.  <span data-ttu-id="c045a-166">Нажмите кнопку **Пуск** и выберите **Диспетчер конфигурации SQL Server**, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-166">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-167">![Значок SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Значок SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="c045a-167">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="c045a-168">В левой области выберите пункт **экземпляр SQL Server**, затем разверните **\<version\> конфигурацию собственного клиента SQL** и выберите **псевдонимы**, как показано на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c045a-168">In the left pane, choose to expand **SQL Server instance**, choose to expand **SQL Native Client \<version\> Configuration**, and then choose **Aliases**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-169">![Псевдонимы в диспетчере конфигурации SQL Server.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Псевдонимы в диспетчере конфигурации SQL Server.")</span><span class="sxs-lookup"><span data-stu-id="c045a-169">![Aliases in SQL Server Configuration Manager.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliases in SQL Server Configuration Manager.")</span></span>

3.  <span data-ttu-id="c045a-170">Щелкните правой кнопкой мыши **псевдонимы** и выберите команду **создать псевдоним..**..</span><span class="sxs-lookup"><span data-stu-id="c045a-170">Right-click **Aliases**, and select **New Alias…**.</span></span>

4.  <span data-ttu-id="c045a-171">Введите **имя псевдонима**, **номер порта**, **протокол** и **сервер**, как показано на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c045a-171">Enter the **Alias Name**, **Port Number**, **Protocol**, and **Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-172">![Создание нового псевдонима](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Создание нового псевдонима")</span><span class="sxs-lookup"><span data-stu-id="c045a-172">![Creating a new alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Creating a new alias")</span></span>
    
    <div>
    

    > [!CAUTION]  
    > <span data-ttu-id="c045a-173">Убедитесь, что вы ввели один и тот же нестандартный порт, который вы использовали в предыдущем шаге, так как этот порт будет прослушиваться сервером SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-173">Make sure to enter the same non-standard port you used in the previous step since that is the port SQL Server will be listening on.</span></span> <span data-ttu-id="c045a-174">Если настроенный псевдоним подключается к неправильному полному доменному имени или экземпляру SQL Server, отключите и снова включите связанный сетевой протокол.</span><span class="sxs-lookup"><span data-stu-id="c045a-174">If a configured alias is connecting to the wrong SQL Server FQDN or Instance, disable and then re-enable the associated network protocol.</span></span> <span data-ttu-id="c045a-175">Это приведет к сбросу всех кэшированных сведений о соединении и позволяет клиенту подключаться правильно.</span><span class="sxs-lookup"><span data-stu-id="c045a-175">Doing this clears any cached connection information and allows the client to connect correctly.</span></span>

    
    </div>

<span data-ttu-id="c045a-176">**Создание записи ресурса CNAME DNS**</span><span class="sxs-lookup"><span data-stu-id="c045a-176">**Create a DNS CNAME Resource Record**</span></span>

1.  <span data-ttu-id="c045a-177">Войдите на компьютер, управляющий DNS.</span><span class="sxs-lookup"><span data-stu-id="c045a-177">Sign into the computer managing DNS.</span></span>

2.  <span data-ttu-id="c045a-178">Нажмите кнопку **Пуск** и выберите **Диспетчер сервера**, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-178">Select **Start**, and choose **Server Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-179">![Открытие диспетчера серверов](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Открытие диспетчера серверов")</span><span class="sxs-lookup"><span data-stu-id="c045a-179">![Opening Server Manager](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Opening Server Manager")</span></span>

3.  <span data-ttu-id="c045a-180">Щелкните раскрывающийся список **Сервис** и выберите **DNS**, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-180">Choose the **Tools** drop-down, and select **DNS**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-181">![Открытие DNS из диспетчера серверов.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Открытие DNS из диспетчера серверов.")</span><span class="sxs-lookup"><span data-stu-id="c045a-181">![Opening DNS from Server Manager.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Opening DNS from Server Manager.")</span></span>

4.  <span data-ttu-id="c045a-182">На левой панели разверните узел имя сервера, разверните узел зоны прямого просмотра и выберите нужный домен.</span><span class="sxs-lookup"><span data-stu-id="c045a-182">In the left pane, expand the server name node, expand the Forward Lookup Zones node, and choose the relevant domain.</span></span>

5.  <span data-ttu-id="c045a-183">Щелкните домен правой кнопкой мыши и выберите команду **создать псевдоним (CNAME)...**, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c045a-183">Right-click the domain, and select **New Alias (CNAME)…**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-184">![Выбор параметра для создания нового псевдонима CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Выбор параметра для создания нового псевдонима CNAME")</span><span class="sxs-lookup"><span data-stu-id="c045a-184">![Selecting option to create a new alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selecting option to create a new alias CNAME")</span></span>

6.  <span data-ttu-id="c045a-185">Введите **псевдоним** и **полное доменное имя SQL Server**, как показано на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c045a-185">Enter the **Alias Name** and the **FQDN for SQL Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-186">![Заполните диалоговое окно Создание CNAME псевдонима.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Заполните диалоговое окно Создание CNAME псевдонима.")</span><span class="sxs-lookup"><span data-stu-id="c045a-186">![Filling in the new alias CNAME dialog.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Filling in the new alias CNAME dialog.")</span></span>

7.  <span data-ttu-id="c045a-187">Нажмите кнопку **ОК** , чтобы сохранить CNAME и просмотреть ее в диспетчере DNS.</span><span class="sxs-lookup"><span data-stu-id="c045a-187">Choose **OK** to save the CNAME and view it in DNS Manager.</span></span>

</div>

<div>

## <a name="validate-database-connectivity"></a><span data-ttu-id="c045a-188">Проверка подключения к базе данных</span><span class="sxs-lookup"><span data-stu-id="c045a-188">Validate Database Connectivity</span></span>

<span data-ttu-id="c045a-189">Существует множество различных способов убедиться в том, что он работает.</span><span class="sxs-lookup"><span data-stu-id="c045a-189">There are many different ways to make sure it is working.</span></span> <span data-ttu-id="c045a-190">Необходимо убедиться, что база данных SQL Server прослушивает указанный порт с помощью псевдонима.</span><span class="sxs-lookup"><span data-stu-id="c045a-190">You want to make sure that the SQL Server database is listening on the specified port using the alias.</span></span> <span data-ttu-id="c045a-191">Быстрая проверка может быть завершена с помощью команд **netstat** и **Telnet** .</span><span class="sxs-lookup"><span data-stu-id="c045a-191">A quick check can be completed using the **netstat** and **telnet** commands.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c045a-192">Клиент Telnet — это функция, которая входит в состав Windows Server, но должна быть установлена.</span><span class="sxs-lookup"><span data-stu-id="c045a-192">Telnet Client is a Feature that comes with Windows Server but that must be installed.</span></span> <span data-ttu-id="c045a-193">Компонент Windows Server можно установить, открыв диспетчер серверов и выбрав в меню Управление пункт Добавить роли и компоненты.</span><span class="sxs-lookup"><span data-stu-id="c045a-193">A Windows Server Feature can be installed by opening Server Manager and selecting Add Roles and Features from the Manage menu.</span></span>



</div>

<span data-ttu-id="c045a-194">**Проверка подключения к базе данных с помощью средства netstat и Telnet**</span><span class="sxs-lookup"><span data-stu-id="c045a-194">**Use netstat and telnet to verify database connectivity**</span></span>

1.  <span data-ttu-id="c045a-195">Нажмите кнопку **Пуск** и введите **cmd** , чтобы открыть командную подсказку.</span><span class="sxs-lookup"><span data-stu-id="c045a-195">Select **Start**, and type **cmd** to open a command prompt.</span></span>

2.  <span data-ttu-id="c045a-196">Введите **netstat-a-f** и убедитесь, что SQL Server запущен с правильным портом, как показано на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="c045a-196">Type **netstat -a -f**, and confirm that SQL Server is running with the correct port, as shown in the following figure.</span></span>
    
    <span data-ttu-id="c045a-197">![Использование средства netstat для проверки порта.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Использование средства netstat для проверки порта.")</span><span class="sxs-lookup"><span data-stu-id="c045a-197">![Using netstat to verify port.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Using netstat to verify port.")</span></span>

3.  <span data-ttu-id="c045a-198">Введите **Telnet \<alias name\> \<port \#\>** , чтобы подтвердить подключение к экземпляру SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c045a-198">Type **telnet \<alias name\> \<port \#\>** to confirm the connection to the SQL Server instance.</span></span> <span data-ttu-id="c045a-199">Если подключение прошло успешно, программа Telnet будет подключаться, и вы не увидите сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c045a-199">If the connection is successful, telnet will connect and you shouldn’t see an error.</span></span> <span data-ttu-id="c045a-200">Это указывает на то, что экземпляр SQL Server прослушивает правильный порт с правильным псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="c045a-200">This shows that the SQL Server instance is listening on the correct port with the correct alias.</span></span> <span data-ttu-id="c045a-201">Если у вас возникла проблема с подключением к базе данных SQL Server, программа Telnet выведет сообщение о том, что соединение не может быть установлено.</span><span class="sxs-lookup"><span data-stu-id="c045a-201">If there’s a problem connecting to the SQL Server database, then telnet shows an error that the connection cannot be made.</span></span> <span data-ttu-id="c045a-202">Теперь, когда вы проверили подключение к базе данных на сервере базы данных, вы можете сделать то же самое в Lync Server (в сети) и убедиться в отсутствии брандмауэров, блокирующих доступ.</span><span class="sxs-lookup"><span data-stu-id="c045a-202">Now that you have checked database connectivity on the database server, you can do the same thing from Lync Server (over the network) and make sure there aren’t any firewalls blocking access along the way.</span></span>

</div>

<div>

## <a name="conclusion"></a><span data-ttu-id="c045a-203">Заключение</span><span class="sxs-lookup"><span data-stu-id="c045a-203">Conclusion</span></span>

<span data-ttu-id="c045a-204">После того как вы настроили псевдоним SQL Server, вы можете использовать его для создания топологии Lync Server 2013 в инструменте Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="c045a-204">Once the SQL Server alias has been configured, you can use it to create a Lync Server 2013 topology in the Topology Builder tool.</span></span> <span data-ttu-id="c045a-205">Дополнительные сведения о топологиях можно найти [в разделе Определение и Настройка топологии в Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="c045a-205">For more information about topologies, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c045a-206">См. также</span><span class="sxs-lookup"><span data-stu-id="c045a-206">See Also</span></span>


<span data-ttu-id="c045a-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md)  
 [Планирование безопасности в Lync Server 2013](lync-server-2013-planning-for-security.md)</span><span class="sxs-lookup"><span data-stu-id="c045a-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md) 
[Planning for security in Lync Server 2013](lync-server-2013-planning-for-security.md)</span></span>  
[<span data-ttu-id="c045a-208">Определение и настройка топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c045a-208">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)  
[<span data-ttu-id="c045a-209">Развертывание Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c045a-209">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="c045a-210"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c045a-210"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

