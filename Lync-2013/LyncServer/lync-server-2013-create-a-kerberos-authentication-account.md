---
title: 'Lync Server 2013: создание учетной записи для проверки подлинности Kerberos'
description: 'Lync Server 2013: создание учетной записи для проверки подлинности Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a Kerberos authentication account
ms:assetid: 63f0cef6-562a-4209-ae25-71f8dc7c7295
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398449(v=OCS.15)
ms:contentKeyID: 48184348
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f8e87a8ffcc95af4a44e516ac4e1f4d635d737
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432179"
---
# <a name="create-a-kerberos-authentication-account-in-lync-server-2013"></a><span data-ttu-id="cfef7-103">Создание учетной записи для проверки подлинности Kerberos в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cfef7-103">Create a Kerberos authentication account in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cfef7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cfef7-104">

<span> </span></span></span>

<span data-ttu-id="cfef7-105">_**Тема последнего изменения:** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="cfef7-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="cfef7-106">Для успешного выполнения этой процедуры необходимо войти в группу администраторов домена с учетной записью сервера или домена.</span><span class="sxs-lookup"><span data-stu-id="cfef7-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group.</span></span>

<span data-ttu-id="cfef7-107">Вы можете создать учетные записи для проверки подлинности Kerberos для каждого сайта или создать одну учетную запись для проверки подлинности Kerberos и использовать ее для всех сайтов.</span><span class="sxs-lookup"><span data-stu-id="cfef7-107">You can create Kerberos authentication accounts for each site or you can create a single Kerberos authentication account and use it for all sites.</span></span> <span data-ttu-id="cfef7-108">Вы используете командлеты Windows PowerShell для создания учетных записей и управления ими, в том числе для идентификации учетных записей, назначенных каждому сайту.</span><span class="sxs-lookup"><span data-stu-id="cfef7-108">You use Windows PowerShell cmdlets to create and manage the accounts, including identifying the accounts assigned to each site.</span></span> <span data-ttu-id="cfef7-109">В построителе топологии и на панели управления Lync Server 2013 не отображаются учетные записи проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="cfef7-109">Topology Builder and the Lync Server 2013 Control Panel do not display Kerberos authentication accounts.</span></span> <span data-ttu-id="cfef7-110">Чтобы создать одну или несколько учетных записей пользователей, используемых для проверки подлинности Kerberos, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cfef7-110">Use the following procedure to create one or more user accounts to be used for Kerberos authentication.</span></span>

<div>

## <a name="to-create-a-kerberos-account"></a><span data-ttu-id="cfef7-111">Создание учетной записи Kerberos</span><span class="sxs-lookup"><span data-stu-id="cfef7-111">To create a Kerberos account</span></span>

1.  <span data-ttu-id="cfef7-112">Войдя в группу администраторов домена, войдите на компьютер домена, на котором работает Lync Server 2013 или на компьютер, на котором установлены средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="cfef7-112">As a member of the Domain Admins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="cfef7-113">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="cfef7-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="cfef7-114">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cfef7-114">From the command line, run the following command:</span></span>
    
        New-CsKerberosAccount -UserAccount "Domain\UserAccount" -ContainerDN "CN=Users,DC=DomainName,DC=DomainExtension"
    
    <span data-ttu-id="cfef7-115">Например:</span><span class="sxs-lookup"><span data-stu-id="cfef7-115">For example:</span></span>
    
        New-CsKerberosAccount -UserAccount "Contoso\KerbAuth" -ContainerDN "CN=Users,DC=contoso,DC=com"

4.  <span data-ttu-id="cfef7-116">Убедитесь, что объект компьютера был создан с помощью оснастки "пользователи и компьютеры Active Directory", разверните контейнер **пользователей** и убедитесь, что объект компьютера для учетной записи пользователя находится в контейнере.</span><span class="sxs-lookup"><span data-stu-id="cfef7-116">Confirm that the Computer object was created by opening Active Directory User and Computers, expand the **Users** container, and then confirm that the Computer object for the user account is in the container.</span></span>

<span data-ttu-id="cfef7-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cfef7-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

