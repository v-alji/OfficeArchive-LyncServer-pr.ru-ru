---
title: 'Lync Server 2013: Настройка ЦС предприятия для проверки подлинности с помощью смарт-карты'
description: 'Lync Server 2013: Настройка ЦС предприятия для проверки подлинности с помощью смарт-карты.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise CA for smart card authentication
ms:assetid: c24e0891-e108-4cb6-9902-c6a4c8e68455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308571(v=OCS.15)
ms:contentKeyID: 54973692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98044c96dd04d02fd87609918f309cf65227b133
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433152"
---
# <a name="configuring-enterprise-ca-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="bd8bc-103">Настройка ЦС предприятия для проверки подлинности с помощью смарт-карты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd8bc-103">Configuring Enterprise CA for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd8bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd8bc-104">

<span> </span></span></span>

<span data-ttu-id="bd8bc-105">_**Тема последнего изменения:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="bd8bc-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="bd8bc-106">В следующем разделе описано, как настроить корневой центр сертификации (ЦС) предприятия для поддержки проверки подлинности с помощью смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-106">The following section describes how to configure an Enterprise Root Certification Authority (CA) to support smart card authentication.</span></span> <span data-ttu-id="bd8bc-107">Сведения о том, как установить корневой центр сертификации предприятия, можно найти в разделе Установка корневого ЦС предприятия по адресу [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364) .</span><span class="sxs-lookup"><span data-stu-id="bd8bc-107">For information on how to install an Enterprise Root CA, see Install an Enterprise Root Certification Authority at [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364).</span></span>

<div>

## <a name="configuring-an-enterprise-root-certificate-authority-to-support-smart-card-authentication"></a><span data-ttu-id="bd8bc-108">Настройка корневого центра сертификации предприятия для поддержки проверки подлинности с помощью смарт-карты</span><span class="sxs-lookup"><span data-stu-id="bd8bc-108">Configuring an Enterprise Root Certificate Authority to Support Smart Card Authentication</span></span>

<span data-ttu-id="bd8bc-109">Ниже описан порядок действий по настройке корневого ЦС предприятия для проверки подлинности с помощью смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-109">The following steps describe how to configure an Enterprise Root CA to support Smart Card Authentication:</span></span>

1.  <span data-ttu-id="bd8bc-110">Войдите на компьютер ЦС предприятия с учетной записью администратора домена.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-110">Log in to the Enterprise CA computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="bd8bc-111">Запустите приложение System Manager и убедитесь в том, что установлена роль регистрации сертификатов через Интернет.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-111">Launch System Manager, and verify that the Certificate Authority Web Enrollment role is installed.</span></span>

3.  <span data-ttu-id="bd8bc-112">В меню **Администрирование** откройте консоль управления **Центр сертификации**.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-112">From the **Administrative Tools** menu, open the **Certification Authority** management console.</span></span>

4.  <span data-ttu-id="bd8bc-113">В области навигации разверните элемент **Центр сертификации**.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-113">In the Navigation pane, expand **Certification Authority**.</span></span>

5.  <span data-ttu-id="bd8bc-114">Щелкните правой кнопкой **Шаблоны сертификатов** и выберите **Создать**, затем **Выдаваемый шаблон сертификата**.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-114">Right click on **Certificate Templates**, select **New**, then select **Certificate Template to Issue**.</span></span>

6.  <span data-ttu-id="bd8bc-115">Выберите **Агент подачи заявок**, **Пользователь со смарт-картой** и **Вход со смарт-картой**.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-115">Select **Enrollment Agent**, **Smartcard User**, and **Smartcard Logon**.</span></span>

7.  <span data-ttu-id="bd8bc-116">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-116">Click **OK**.</span></span>

8.  <span data-ttu-id="bd8bc-117">Щелкните **Шаблоны сертификатов** правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-117">Right click on **Certificate Templates**.</span></span>

9.  <span data-ttu-id="bd8bc-118">Выберите **Управление**.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-118">Select **Manage**.</span></span>

10. <span data-ttu-id="bd8bc-119">Откройте свойства шаблона пользователя смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-119">Open the properties of the Smartcard User template.</span></span>

11. <span data-ttu-id="bd8bc-120">Перейдите на вкладку **Безопасность**.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-120">Click on the **Security** tab.</span></span>

12. <span data-ttu-id="bd8bc-121">Задайте указанные ниже разрешения.</span><span class="sxs-lookup"><span data-stu-id="bd8bc-121">Change the permissions as follows:</span></span>
    
      - <span data-ttu-id="bd8bc-122">Добавьте учетные записи отдельных пользователей Active Directory с разрешениями на чтение и подачу заявок (разрешить).</span><span class="sxs-lookup"><span data-stu-id="bd8bc-122">Add individual user AD accounts with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="bd8bc-123">Добавьте группу безопасности с пользователями смарт-карт, обладающую разрешениями на чтение и подачу заявок (разрешить).</span><span class="sxs-lookup"><span data-stu-id="bd8bc-123">Add a security group containing smart card users with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="bd8bc-124">Добавьте группу пользователей домена с разрешениями на чтение и подачу заявок (разрешить).</span><span class="sxs-lookup"><span data-stu-id="bd8bc-124">Add the Domain Users group with Read/Enroll (Allow) permissions</span></span>

<span data-ttu-id="bd8bc-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd8bc-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

