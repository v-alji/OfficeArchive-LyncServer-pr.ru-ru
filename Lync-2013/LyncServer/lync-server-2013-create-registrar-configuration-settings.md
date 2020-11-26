---
title: 'Lync Server 2013: Создание параметров конфигурации регистратора'
description: 'Lync Server 2013: Создание параметров конфигурации регистратора.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Registrar configuration settings
ms:assetid: eddfbdd2-cfd0-4c03-986e-443d6728db7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182601(v=OCS.15)
ms:contentKeyID: 48185758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ada10302b3c2319e0f713ce2d3bea00b6fed126
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431605"
---
# <a name="create-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="26eae-103">Создание параметров конфигурации регистратора в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26eae-103">Create Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26eae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26eae-104">

<span> </span></span></span>

<span data-ttu-id="26eae-105">_**Тема последнего изменения:** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="26eae-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="26eae-p101">Регистратор можно использовать для настройки способов проверки подлинности прокси-сервера. Заданный протокол проверки подлинности определяет, какой тип запросов серверы в пуле выдают клиентам. Далее приводятся доступные протоколы.</span><span class="sxs-lookup"><span data-stu-id="26eae-p101">You can use the Registrar to configure proxy server authentication methods. The authentication protocol you specify determines which type of challenges the servers in the pool issue to clients. The available protocols are:</span></span>

  - <span data-ttu-id="26eae-109">**Kerberos**   Это надежная схема проверки подлинности на основе паролей, доступная для клиентов, но она обычно доступна только для корпоративных клиентов, так как для этого требуется подключение клиента к центру распространения ключей (контроллер домена Kerberos).</span><span class="sxs-lookup"><span data-stu-id="26eae-109">**Kerberos**   This is the strongest password-based authentication scheme available to clients, but it is normally available only to enterprise clients because it requires client connection to a Key Distribution Center (Kerberos domain controller).</span></span> <span data-ttu-id="26eae-110">Это значение можно выбрать в том случае, если на сервере проверяется подлинность только корпоративных клиентов.</span><span class="sxs-lookup"><span data-stu-id="26eae-110">This setting is appropriate if the server authenticates only enterprise clients.</span></span>

  - <span data-ttu-id="26eae-111">**NTLM**   Это проверка подлинности на основе пароля, доступная для клиентов, использующих в пароле схему хеширования с запросом ответа.</span><span class="sxs-lookup"><span data-stu-id="26eae-111">**NTLM**   This is the password-based authentication available to clients that use a challenge-response hashing scheme on the password.</span></span> <span data-ttu-id="26eae-112">Это единственная форма проверки подлинности, доступная клиентам без подключения к центру распространения ключей (контроллеру домена Kerberos), в том числе удаленным пользователям.</span><span class="sxs-lookup"><span data-stu-id="26eae-112">This is the only form of authentication available to clients without connectivity to a Key Distribution Center (Kerberos domain controller), such as remote users.</span></span> <span data-ttu-id="26eae-113">Если на сервере проверяется подлинность только удаленных пользователей, следует выбрать значение NTLM.</span><span class="sxs-lookup"><span data-stu-id="26eae-113">If a server authenticates only remote users, you should choose NTLM.</span></span>

  - <span data-ttu-id="26eae-114">**Проверка подлинности сертификата**   Это новый способ проверки подлинности, когда сервер должен получить сертификаты от клиентов Lync Phone Edition, обычных телефонов, Lync 2013 и приложения Lync из Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="26eae-114">**Certificate authentication**   This is the new authentication method when the server needs to obtain certificates from Lync Phone Edition clients, common area phones, Lync 2013 and the Lync Windows Store app.</span></span> <span data-ttu-id="26eae-115">На клиентах Lync Phone Edition после входа пользователя в систему и успешной проверки подлинности, предоставляя персональный идентификационный номер (ПИН-код), Lync Server 2013 затем подготавливает универсальный код ресурса SIP к телефону и подготавливает сертификат для сервера Lync Server или сертификат пользователя, который определяет "Joe" (например, SN=joe@contoso.com), на телефон.</span><span class="sxs-lookup"><span data-stu-id="26eae-115">On Lync Phone Edition clients, after a user signs in and is successfully authenticated by providing a personal identification number (PIN), Lync Server 2013 then provisions the SIP URI to the phone and provisions a Lync Server signed certificate or a user certificate that identifies Joe (Ex: SN=joe@contoso.com ) to the phone.</span></span> <span data-ttu-id="26eae-116">Этот сертификат применяется при проверке подлинности с помощью регистратора и веб-служб.</span><span class="sxs-lookup"><span data-stu-id="26eae-116">This certificate is used for authenticating with the Registrar and Web Services.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="26eae-p105">Если сервер поддерживает проверку подлинности для удаленных клиентов и для клиентов предприятия, рекомендуется включить и Kerberos, и NTLM. Пограничный сервер и внутренние серверы взаимодействуют, чтобы убедиться, что для удаленных клиентов предлагается только проверка подлинности NTLM. Если на этих серверах включен только Kerberos, они не могут выполнять проверку подлинности удаленных пользователей. Если пользователи предприятия также проходят проверку подлинности на сервере, то используется Kerberos.</span><span class="sxs-lookup"><span data-stu-id="26eae-p105">We recommend that you enable both Kerberos and NTLM when a server supports authentication for both remote and enterprise clients. The Edge Server and internal servers communicate to ensure that only NTLM authentication is offered to remote clients. If only Kerberos is enabled on these servers, they cannot authenticate remote users. If enterprise users also authenticate against the server, Kerberos is used.</span></span><BR><span data-ttu-id="26eae-121">Если вы используете приложения Lync из Магазина Windows, необходимо включить проверку подлинности сертификата.</span><span class="sxs-lookup"><span data-stu-id="26eae-121">If you will use Lync Windows Store app clients, you must enable certificate authentication.</span></span>



</div>

<span data-ttu-id="26eae-122">Для создания нового регистратора выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="26eae-122">Follow these steps to create a new Registrar.</span></span>

<div>

## <a name="to-create-new-registrar-configuration-settings"></a><span data-ttu-id="26eae-123">Создание параметров конфигурации нового регистратора</span><span class="sxs-lookup"><span data-stu-id="26eae-123">To create new Registrar configuration settings</span></span>

1.  <span data-ttu-id="26eae-124">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="26eae-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="26eae-125">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="26eae-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="26eae-126">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="26eae-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="26eae-127">В левой области навигации щелкните **Безопасность**, затем **Регистратор**.</span><span class="sxs-lookup"><span data-stu-id="26eae-127">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="26eae-128">На странице **Регистратор** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="26eae-128">On the **Registrar** page, click **New**</span></span>

5.  <span data-ttu-id="26eae-129">В поле **Выбор службы** выберите службу, к которой требуется применить регистратор, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="26eae-129">In **Select a Service**, click the service to which the Registrar is to be applied and then click **OK**.</span></span>

6.  <span data-ttu-id="26eae-130">На странице **Создание новой настройки регистратора** установите один или несколько флажков в зависимости от возможностей клиентов.</span><span class="sxs-lookup"><span data-stu-id="26eae-130">In **New Registrar Setting**, select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="26eae-131">**Включить проверку подлинности Kerberos**. В этом режиме серверы в пуле выдают запросы с применением проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="26eae-131">**Enable Kerberos authentication** to have the servers in the pool issue challenges using Kerberos authentication.</span></span>
    
      - <span data-ttu-id="26eae-132">**Разрешить проверку подлинности NTLM**. В этом режиме серверы в пуле выдают запросы с применением проверки подлинности NTLM.</span><span class="sxs-lookup"><span data-stu-id="26eae-132">**Enable NTLM authentication** to have the servers in the pool issue challenges using NTLM.</span></span>
    
      - <span data-ttu-id="26eae-133">**Разрешить проверку подлинности на основе сертификатов**. В этом режиме серверы в пуле выдают сертификаты клиентам.</span><span class="sxs-lookup"><span data-stu-id="26eae-133">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>

7.  <span data-ttu-id="26eae-134">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="26eae-134">Click **Commit**.</span></span>

<span data-ttu-id="26eae-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26eae-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

