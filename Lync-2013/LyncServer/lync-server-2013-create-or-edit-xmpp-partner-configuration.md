---
title: 'Lync Server 2013: создание или редактирование конфигурации XMPP-партнеров'
description: 'Lync Server 2013: создание и изменение конфигурации XMPP партнера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit XMPP partner configuration
ms:assetid: 362dbe5e-8ee9-4aba-8c26-5907312b4a60
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552447(v=OCS.15)
ms:contentKeyID: 48679558
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19289df1920287984f104bb1bdfa214d6f83f5cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431857"
---
# <a name="create-or-edit-xmpp-partner-configuration-in-lync-server-2013"></a><span data-ttu-id="090bf-103">Создание или редактирование конфигурации XMPP-партнеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="090bf-103">Create or edit XMPP partner configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="090bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="090bf-104">

<span> </span></span></span>

<span data-ttu-id="090bf-105">_**Тема последнего изменения:** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="090bf-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="090bf-106">Microsoft Lync Server 2013 интегрирует на пограничном сервере прокси-сервер с расширенными сообщениями и протоколом присутствия (XMPP) и шлюз XMPP на сервере переднего плана или пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="090bf-106">Microsoft Lync Server 2013 integrates an Extensible Messaging and Presence Protocol (XMPP) proxy on the Edge Server and an XMPP Gateway on the Front End Server or Front End pool.</span></span> <span data-ttu-id="090bf-107">Чтобы разрешить подключения из других развертываний XMPP, необходимо настроить XMPP на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="090bf-107">To allow connections from other XMPP deployments, you must configure XMPP in the Lync Server Control Panel.</span></span> <span data-ttu-id="090bf-108">Вы настраиваете параметры на основе домена XMPP.</span><span class="sxs-lookup"><span data-stu-id="090bf-108">You configure settings on an XMPP domain basis.</span></span> <span data-ttu-id="090bf-109">Чтобы создать связь с партнером, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="090bf-109">To create a new partner association, you do the following:</span></span>

<div>

## <a name="to-create-a-new-federated-partner-or-edit-an-existing-configuration"></a><span data-ttu-id="090bf-110">Создание нового федеративного партнера или изменение существующей конфигурации</span><span class="sxs-lookup"><span data-stu-id="090bf-110">To create a new federated partner or edit an existing configuration</span></span>

1.  <span data-ttu-id="090bf-111">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="090bf-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="090bf-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="090bf-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="090bf-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="090bf-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="090bf-114">На панели навигации слева выберите пункт **интеграция и внешний доступ**, а затем — **XMPP Федеративные партнеры**.</span><span class="sxs-lookup"><span data-stu-id="090bf-114">In the left navigation bar, click **Federation and External Access**, and then click **XMPP Federated Partners**.</span></span>

4.  <span data-ttu-id="090bf-115">Чтобы создать новую конфигурацию, нажмите кнопку **создать** .</span><span class="sxs-lookup"><span data-stu-id="090bf-115">To create a new configuration, click **New**</span></span>

5.  <span data-ttu-id="090bf-116">Чтобы изменить существующую конфигурацию, выберите ее и нажмите кнопку **изменить** .</span><span class="sxs-lookup"><span data-stu-id="090bf-116">To edit an existing configuration, select the configuration and click **Edit**</span></span>

6.  <span data-ttu-id="090bf-117">Чтобы создать или изменить конфигурации **федеративных партнеров XMPP**, вы можете определить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="090bf-117">To create or edit configurations for **XMPP Federated Partners**, you define the following settings:</span></span>

7.  <span data-ttu-id="090bf-118">**Основной домен** (обязательно).</span><span class="sxs-lookup"><span data-stu-id="090bf-118">**Primary domain** (Required).</span></span> <span data-ttu-id="090bf-119">Основной домен — это базовый домен партнера XMPP.</span><span class="sxs-lookup"><span data-stu-id="090bf-119">The primary domain is the base domain of the XMPP partner.</span></span> <span data-ttu-id="090bf-120">Например, вы можете ввести **Fabrikam.com** для доменного имени XMPP партнера.</span><span class="sxs-lookup"><span data-stu-id="090bf-120">For example, you would enter **fabrikam.com** for the XMPP partner domain name.</span></span> <span data-ttu-id="090bf-121">Это обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="090bf-121">This is a required entry.</span></span>

8.  <span data-ttu-id="090bf-122">**Description (описание**).</span><span class="sxs-lookup"><span data-stu-id="090bf-122">**Description**.</span></span> <span data-ttu-id="090bf-123">Описание для заметок и другой идентифицирующей информации о конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="090bf-123">The description is for notes or other identifying information for this particular configuration.</span></span> <span data-ttu-id="090bf-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="090bf-124">This entry is optional.</span></span>

9.  <span data-ttu-id="090bf-125">**Дополнительные домены**.</span><span class="sxs-lookup"><span data-stu-id="090bf-125">**Additional domains**.</span></span> <span data-ttu-id="090bf-126">Дополнительные домены — это домены, являющиеся частью домена вашего партнера XMPP, которые должны быть включены в рамках разрешенного XMPP общения.</span><span class="sxs-lookup"><span data-stu-id="090bf-126">Additional domains are domains that are a part of your XMPP partner’s domain that should be included as part of the allowed XMPP communication.</span></span> <span data-ttu-id="090bf-127">Например, если основной домен — **Fabrikam.com**, вы увидите список всех остальных доменов, которые находятся в Fabrikam.com, с которыми вы будете общаться с помощью XMPP.</span><span class="sxs-lookup"><span data-stu-id="090bf-127">For example, if the primary domain is **fabrikam.com**, then you would list all other domains that are under fabrikam.com that you will communicate with by way of XMPP.</span></span> <span data-ttu-id="090bf-128">Например, вы можете ввести **Corp.fabrikam.com** и **IT.fabrikam.com** для корпоративного XMPP домена и информационных технологий XMPP домена компании Fabrikam. com для основного домена XMPP.</span><span class="sxs-lookup"><span data-stu-id="090bf-128">For example, you might enter **corp.fabrikam.com** and **it.fabrikam.com** for the Corporate XMPP domain and the Information Technologies XMPP domain under fabrikam.com’s main XMPP domain.</span></span>

10. <span data-ttu-id="090bf-129">**Тип партнера**.</span><span class="sxs-lookup"><span data-stu-id="090bf-129">**Partner type**.</span></span> <span data-ttu-id="090bf-130">**Тип Partner** является обязательным параметром, и в раскрывающемся меню выводятся три варианта выбора.</span><span class="sxs-lookup"><span data-stu-id="090bf-130">The **Partner type** is a required setting and gives you a selection of three choices in a drop-down menu.</span></span> <span data-ttu-id="090bf-131">Чтобы описать и принудительно добавить контакты, необходимо выбрать один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="090bf-131">You must choose one of the following to describe and enforce what contacts can be added.</span></span> <span data-ttu-id="090bf-132">Вы можете выбрать один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="090bf-132">You can select from:</span></span>
    
      - <span data-ttu-id="090bf-133">**Федеративное**.</span><span class="sxs-lookup"><span data-stu-id="090bf-133">**Federated**.</span></span> <span data-ttu-id="090bf-134">Тип **федеративного** партнера — это надежное соединение между сервером Lync Server или Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="090bf-134">A **Federated** partner type is a trusted connection between a Lync Server or Office Communications Server 2007 R2 partner deployment.</span></span>
    
      - <span data-ttu-id="090bf-135">**Общедоступная проверка подлинности**.</span><span class="sxs-lookup"><span data-stu-id="090bf-135">**Public verified**.</span></span> <span data-ttu-id="090bf-136">**Общедоступный проверенный** партнер — это то, что контакты, являющиеся частью развертывания, проверяемого поставщиком, можно добавить в список контактов вашего пользователя.</span><span class="sxs-lookup"><span data-stu-id="090bf-136">A **Public verified** partner is when contacts that are part of a deployment that are verified by the provider can be added to your user’s list of contacts.</span></span> <span data-ttu-id="090bf-137">Приглашения можно отправлять из пользователя Lync или пользователя Lync, чтобы принимать приглашения от контакта партнера.</span><span class="sxs-lookup"><span data-stu-id="090bf-137">Invites can be sent from the Lync user or the Lync user can accept invites from the partner contact.</span></span>
    
      - <span data-ttu-id="090bf-138">**Общедоступный, непроверенный**.</span><span class="sxs-lookup"><span data-stu-id="090bf-138">**Public unverified**.</span></span> <span data-ttu-id="090bf-139">**Общедоступное непроверенное** отношение предполагает, что в двух развертываниях нет установленного и проверяемого состояния.</span><span class="sxs-lookup"><span data-stu-id="090bf-139">A **Public unverified** relationship implies that there is no established and verifiable status between the two deployments.</span></span> <span data-ttu-id="090bf-140">Пользователь Lync должен пригласить непроверенного контакта на этот контакт, чтобы он мог добавить пользователя Lync в свой список контактов.</span><span class="sxs-lookup"><span data-stu-id="090bf-140">A Lync user must invite the unverified contact for that contact to be able to add the Lync user to his contact list.</span></span> <span data-ttu-id="090bf-141">Например, Google GTalk не является службой общедоступной проверки подлинности XMPP, связанной с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="090bf-141">For example, Google GTalk is not a public verified XMPP service as it relates to Lync Server.</span></span> <span data-ttu-id="090bf-142">Пользователь GTalk не сможет добавить пользователя Lync в качестве контакта, если только вы не получили явно приглашение от пользователя Lync.</span><span class="sxs-lookup"><span data-stu-id="090bf-142">A GTalk user will not be able to add the Lync user as a contact unless there is an explicit invite sent from the Lync user.</span></span>

11. <span data-ttu-id="090bf-143">Заметка о согласовании потоков и методах безопасности (TLS) и проверки подлинности и безопасности программного обеспечения (SASL).</span><span class="sxs-lookup"><span data-stu-id="090bf-143">Notes on stream negotiation and the security methods Transport Layer Security (TLS) and Software Authentication and Security Layer (SASL):</span></span>
    
    <span data-ttu-id="090bf-144">**XMPP Standards Foundation** (XSF) и **Task Engineering (Интернет** ) (IETF) определяют набор правил и стандартов для использования и управления сертификатами клиентов TLS, сертификатами сервера TLS и механизмом SASL.</span><span class="sxs-lookup"><span data-stu-id="090bf-144">The **XMPP Standards Foundation** (XSF) and the **Internet Engineering Task Force** (IETF) define a set of rules and standards for using and managing TLS client certificates, TLS server certificates, and the SASL mechanism.</span></span> <span data-ttu-id="090bf-145">Использование TLS и SASL — это необходимый процесс для защиты потока XMPP.</span><span class="sxs-lookup"><span data-stu-id="090bf-145">Using TLS and SASL is the required process for securing the XMPP stream.</span></span> <span data-ttu-id="090bf-146">Из XMPP стандартов **XEP-0178**"указывает рекомендуемый поток протокола для использования внешнего механизма SASL с сертификатами pkix, особенно если служба XMPP указывает на то, что TLS является обязательным для согласования."</span><span class="sxs-lookup"><span data-stu-id="090bf-146">From the XMPP Standards document **XEP-0178**, “specifies a recommended protocol flow for use of the SASL EXTERNAL mechanism with PKIX certificates, especially when an XMPP service indicates that TLS is mandatory-to-negotiate.”</span></span> <span data-ttu-id="090bf-147">PKIX, как указано в документации по XSF, относится к инфраструктуре открытого ключа, также называемой PKI.</span><span class="sxs-lookup"><span data-stu-id="090bf-147">PKIX, as stated in the XSF documentation, refers to public key infrastructure, also known as PKI.</span></span>
    
    <span data-ttu-id="090bf-148">Дополнительные сведения о требованиях к XMPP можно найти в документе XSF XEP-0178.</span><span class="sxs-lookup"><span data-stu-id="090bf-148">Refer to the XSF document XEP-0178 for more details on the XMPP requirements.</span></span> <span data-ttu-id="090bf-149">Подробнее читайте в статье "XEP-0178: советы и рекомендации по использованию внешних сертификатов SASL с сертификатами".</span><span class="sxs-lookup"><span data-stu-id="090bf-149">For details, refer to “XEP-0178: Best Practices for Use of SASL EXTERNAL with Certificates”.</span></span> <http://xmpp.org/extensions/xep-0178.html>
    
    <span data-ttu-id="090bf-150">Обратитесь к документу IETF "Протокол расширенной передачи сообщений и доступности (XMPP): ядро", раздел 5,0, согласование STARTTLS <https://tools.ietf.org/html/rfc6120> .</span><span class="sxs-lookup"><span data-stu-id="090bf-150">Refer to the IETF document “Extensible Messaging and Presence Protocol (XMPP): Core“, Section 5.0, STARTTLS Negotiation <https://tools.ietf.org/html/rfc6120>.</span></span>
    
      - <span data-ttu-id="090bf-151">**Согласование TLS**.</span><span class="sxs-lookup"><span data-stu-id="090bf-151">**TLS Negotiation**.</span></span> <span data-ttu-id="090bf-152">Определяет правила согласования TLS.</span><span class="sxs-lookup"><span data-stu-id="090bf-152">Defines the TLS negotiation rules.</span></span> <span data-ttu-id="090bf-153">Для службы XMPP может потребоваться TLS, может быть необязательным TLS или определено, что TLS не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="090bf-153">An XMPP service can require TLS, can make TLS optional, or you define that TLS is not supported.</span></span> <span data-ttu-id="090bf-154">Если выбрать необязательный вариант, вы не сможете получить требование к службе XMPP для решения, которое является обязательным для согласования.</span><span class="sxs-lookup"><span data-stu-id="090bf-154">Choosing Optional leaves the requirement up to the XMPP service for a mandatory-to-negotiate decision.</span></span> <span data-ttu-id="090bf-155">Чтобы просмотреть все возможные параметры и сведения о согласовании SASL, TLS и Dialback, в том числе недопустимых и известных конфигураций ошибок, — [в разделе Параметры согласования XMPP федеративных партнеров в Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span><span class="sxs-lookup"><span data-stu-id="090bf-155">To view all possible settings and details for SASL, TLS and Dialback negotiation –including not valid and known error configurations - see [Negotiation settings for XMPP federated partners in Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span></span>
        
          - <span></span>  
            <span data-ttu-id="090bf-156">**Обязательный**.</span><span class="sxs-lookup"><span data-stu-id="090bf-156">**Required**.</span></span> <span data-ttu-id="090bf-157">Службе XMPP требуется согласование TLS.</span><span class="sxs-lookup"><span data-stu-id="090bf-157">The XMPP service requires TLS negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="090bf-158">**Необязательный**.</span><span class="sxs-lookup"><span data-stu-id="090bf-158">**Optional**.</span></span> <span data-ttu-id="090bf-159">Служба XMPP указывает, что протокол TLS является обязательным для согласования.</span><span class="sxs-lookup"><span data-stu-id="090bf-159">The XMPP service indicates that TLS is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="090bf-160">**Не поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="090bf-160">**Not Supported**.</span></span> <span data-ttu-id="090bf-161">Служба XMPP не поддерживает TLS.</span><span class="sxs-lookup"><span data-stu-id="090bf-161">The XMPP service does not support TLS.</span></span>
    
      - <span data-ttu-id="090bf-162">**Согласование SASL**.</span><span class="sxs-lookup"><span data-stu-id="090bf-162">**SASL negotiation**.</span></span> <span data-ttu-id="090bf-163">Определяет правила согласования SASL.</span><span class="sxs-lookup"><span data-stu-id="090bf-163">Defines the SASL negotiation rules.</span></span> <span data-ttu-id="090bf-164">Служба XMPP может потребовать SASL, может сделать SASL необязательной или определить, что SASL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="090bf-164">An XMPP service can require SASL, can make SASL optional, or you define that SASL is not supported.</span></span> <span data-ttu-id="090bf-165">Если выбрать необязательный вариант, вы не сможете получить требование к службе XMPP партнера, чтобы принять решение для принудительного согласования.</span><span class="sxs-lookup"><span data-stu-id="090bf-165">Choosing Optional leaves the requirement up to the partner XMPP service for a mandatory-to-negotiate decision.</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="090bf-166">Для SASL требуется TLS.</span><span class="sxs-lookup"><span data-stu-id="090bf-166">SASL requires TLS.</span></span> <span data-ttu-id="090bf-167">Для использования SASL требуется TLS или обязательным.</span><span class="sxs-lookup"><span data-stu-id="090bf-167">To use SASL, TLS must either be required or optional.</span></span> <span data-ttu-id="090bf-168">Любые настройки, определяющие SASL как обязательные или необязательные, должны поддерживать TLS.</span><span class="sxs-lookup"><span data-stu-id="090bf-168">Any configuration that defines SASL as either required or optional must have TLS support.</span></span> <span data-ttu-id="090bf-169">При нажатии кнопки "Сохранить" для сохранения <STRONG>изменений в случае</STRONG> , если вы не настроили TLS на обязательное или необязательное, появится предупреждение о том, что SASL должен поддерживать TLS, и ваши изменения не будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="090bf-169">When clicking <STRONG>Commit</STRONG> to save your changes, if you have not set TLS to required or optional, you will be warned that SASL must have TLS support and your changes are not saved.</span></span> <span data-ttu-id="090bf-170">Чтобы устранить эту ошибку, настройте TLS на <STRONG>Обязательное</STRONG> или <STRONG>необязательное</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="090bf-170">To resolve the error, set TLS to <STRONG>Required</STRONG> or <STRONG>Optional</STRONG>.</span></span> <span data-ttu-id="090bf-171">Если использование SASL является необязательным и поддержка согласования TLS не <STRONG>поддерживается</STRONG>, необходимо установить параметр согласования SASL.</span><span class="sxs-lookup"><span data-stu-id="090bf-171">If use of SASL is optional and TLS negotiation support is not possible, you must set SASL negotiation to <STRONG>Not Supported</STRONG>.</span></span> <span data-ttu-id="090bf-172">Убедитесь в том, что служба XMPP должна иметь соответствующие потоки согласования для TLS и SASL или перерывов в работе служб.</span><span class="sxs-lookup"><span data-stu-id="090bf-172">Confirm with the XMPP service what the proper negotiation streams must be for TLS and SASL or service interruption will occur.</span></span>

        
        </div>
        
          - <span></span>  
            <span data-ttu-id="090bf-173">**Обязательный**.</span><span class="sxs-lookup"><span data-stu-id="090bf-173">**Required**.</span></span> <span data-ttu-id="090bf-174">Для службы XMPP требуется согласование SASL.</span><span class="sxs-lookup"><span data-stu-id="090bf-174">The XMPP service requires SASL negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="090bf-175">**Необязательный**.</span><span class="sxs-lookup"><span data-stu-id="090bf-175">**Optional**.</span></span> <span data-ttu-id="090bf-176">Служба XMPP указывает, что SASL является обязательным для согласования.</span><span class="sxs-lookup"><span data-stu-id="090bf-176">The XMPP service indicates that SASL is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="090bf-177">**Не поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="090bf-177">**Not Supported**.</span></span> <span data-ttu-id="090bf-178">Служба XMPP не поддерживает SASL.</span><span class="sxs-lookup"><span data-stu-id="090bf-178">The XMPP service does not support SASL.</span></span>
    
      - <span data-ttu-id="090bf-179">**Dialback согласование**.</span><span class="sxs-lookup"><span data-stu-id="090bf-179">**Dialback negotiation**.</span></span> <span data-ttu-id="090bf-180">Dialback согласование определяется с помощью XSF в документе **XEP-220: Server Dialback** <http://xmpp.org/extensions/xep-0220.html> .</span><span class="sxs-lookup"><span data-stu-id="090bf-180">Dialback negotiation is defined by the XSF in document **XEP-220 : Server Dialback** <http://xmpp.org/extensions/xep-0220.html>.</span></span> <span data-ttu-id="090bf-181">Серверный процесс dialback использует систему доменных имен (DNS) и удостоверяющий сервер, чтобы убедиться, что запрос был получен от действующего партнера XMPP.</span><span class="sxs-lookup"><span data-stu-id="090bf-181">The server dialback process uses the domain name system (DNS) and an authoritative server to verify that the request came from a valid XMPP partner.</span></span> <span data-ttu-id="090bf-182">Для этого на исходном сервере создается сообщение определенного типа с созданным ключом dialback и выполняется поиск сервера-получателя в DNS.</span><span class="sxs-lookup"><span data-stu-id="090bf-182">To do this, the originating server creates a message of a specific type with a generated dialback key and looks up the receiving server in DNS.</span></span> <span data-ttu-id="090bf-183">Сервер-источник отправляет ключ в потоке XML в конечный поиск DNS, предположительно на получающем сервере.</span><span class="sxs-lookup"><span data-stu-id="090bf-183">The originating server sends the key in an XML stream to the resulting DNS lookup, presumably the receiving server.</span></span> <span data-ttu-id="090bf-184">При получении ключа над потоком XML, принимающий сервер не отвечает на исходный сервер, но отправляет ключ на известный полномочный сервер.</span><span class="sxs-lookup"><span data-stu-id="090bf-184">On receipt of the key over the XML stream, the receiving server does not respond to the originating server, but sends the key to a known authoritative server.</span></span> <span data-ttu-id="090bf-185">Удостоверяющий сервер проверяет, является ли ключ допустимым или недействительным.</span><span class="sxs-lookup"><span data-stu-id="090bf-185">The authoritative server verifies that the key is either valid or not valid.</span></span> <span data-ttu-id="090bf-186">Если это значение недействительно, принимающий сервер не отвечает на исходящий сервер.</span><span class="sxs-lookup"><span data-stu-id="090bf-186">If not valid, the receiving server does not respond to the originating server.</span></span> <span data-ttu-id="090bf-187">Если ключ является действительным, принимающий сервер информирует сервер источника о том, что удостоверение и ключ являются допустимыми, и может быть инициировано обсуждение.</span><span class="sxs-lookup"><span data-stu-id="090bf-187">If the key is valid, the receiving server informs the originating server that the identity and key is valid and the conversation can commence.</span></span>
        
        <span data-ttu-id="090bf-188">Существует два допустимых состояния для **согласования Dialback**:</span><span class="sxs-lookup"><span data-stu-id="090bf-188">There are two valid states for **Dialback negotiation**:</span></span>
        
          - <span></span>  
            <span data-ttu-id="090bf-189">**Истина**.</span><span class="sxs-lookup"><span data-stu-id="090bf-189">**True**.</span></span> <span data-ttu-id="090bf-190">Сервер XMPP настроен на использование согласования Dialback, если требуется получить запрос от исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="090bf-190">The XMPP server is configured to use Dialback negotiation if a request should be received from an originating server</span></span>
        
          - <span></span>  
            <span data-ttu-id="090bf-191">**Ложь**.</span><span class="sxs-lookup"><span data-stu-id="090bf-191">**False**.</span></span> <span data-ttu-id="090bf-192">Сервер XMPP не настроен на использование согласования Dialback и если запрос должен быть получен от сервера-источника, он будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="090bf-192">The XMPP server is not configured to use Dialback negotiation and if a request should be received from an originating server, it will be ignored</span></span>

<span data-ttu-id="090bf-193"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="090bf-193"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

