---
title: 'Lync Server 2013: обеспечение взаимодействия Lync и Skype'
description: 'Lync Server 2013: включение Lync-Skype подключения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Lync-Skype connectivity
ms:assetid: 34c4db3e-582f-41fb-85c4-3438ae02f09f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440170(v=OCS.15)
ms:contentKeyID: 57793361
ms.date: 12/16/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f31856299b05af7d6b8e934d6e9784d1571b7e29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428813"
---
# <a name="enabling-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="8b480-103">Обеспечение взаимодействия Lync и Skype в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b480-103">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b480-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b480-104">

<span> </span></span></span>

<span data-ttu-id="8b480-105">_**Тема последнего изменения:** 2014-12-16_</span><span class="sxs-lookup"><span data-stu-id="8b480-105">_**Topic Last Modified:** 2014-12-16_</span></span>

<span data-ttu-id="8b480-106">После отправки запроса на подготовку вы можете сосредоточиться на среде Lync Server и административных задачах, необходимых для настройки подключения к Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="8b480-106">After you have submitted the provisioning request, you can focus on the Lync Server environment and administrative tasks required to configure Lync-Skype connectivity.</span></span> <span data-ttu-id="8b480-107">В этом разделе предполагается, что администратор сервера Lync Server развернул сервер Lync Server и настроил внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="8b480-107">In this section, we assume that the Lync Server administrator has deployed Lync Server and configured external access.</span></span> <span data-ttu-id="8b480-108">Дополнительные сведения о настройке внешнего доступа для Lync Server можно найти [в разделе Планирование доступа внешних пользователей в Lync server 2013](lync-server-2013-planning-for-external-user-access.md) и [развертывание внешних пользователей в Lync Server 2013](lync-server-2013-deploying-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="8b480-108">For additional information on configuring external access for Lync Server, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md).</span></span>

<span data-ttu-id="8b480-109">Для подготовки среды Lync Server к Lync-Skype подключениям администратор сервера Lync Server должен выполнить следующие три задачи:</span><span class="sxs-lookup"><span data-stu-id="8b480-109">To prepare the Lync Server environment for Lync-Skype connectivity, the Lync Server administrator must complete the following three tasks:</span></span>

<div>

## <a name="1-configure-federation-and-pic"></a><span data-ttu-id="8b480-110">1 \.</span><span class="sxs-lookup"><span data-stu-id="8b480-110">1\.</span></span> <span data-ttu-id="8b480-111">настройка федерации и PIC;</span><span class="sxs-lookup"><span data-stu-id="8b480-111">Configure Federation and PIC</span></span>

<span data-ttu-id="8b480-112">Для того чтобы пользователи Skype могли общаться с пользователями Lync в вашей организации, требуется Федерация.</span><span class="sxs-lookup"><span data-stu-id="8b480-112">Federation is required to enable Skype users to communicate with Lync users in your organization.</span></span> <span data-ttu-id="8b480-113">Общедоступная служба обмена мгновенными сообщениями (PIC) — это класс Федерации, и он должен быть настроен для предоставления пользователям Lync возможности общаться с пользователями Skype.</span><span class="sxs-lookup"><span data-stu-id="8b480-113">Public Instant Messaging Connectivity (PIC) is a class of federation, and it must be configured to enable your Lync users to communicate with Skype users.</span></span> <span data-ttu-id="8b480-114">Федерация и PIC настраиваются с помощью панели управления Lync Server, показанной ниже.</span><span class="sxs-lookup"><span data-stu-id="8b480-114">Federation and PIC are configured by using the Lync Server Control Panel, shown below.</span></span>

<span data-ttu-id="8b480-115">![Отображение PIC](images/Dn440170.451b94e3-0b38-488c-835f-1f25690e8074(OCS.15).jpg "Отображение PIC")</span><span class="sxs-lookup"><span data-stu-id="8b480-115">![Showing PIC](images/Dn440170.451b94e3-0b38-488c-835f-1f25690e8074(OCS.15).jpg "Showing PIC")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8b480-116">Федерация PIC больше не поддерживается в Live Communication Server 2005 с пакетом обновления 1 (SP1) и Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="8b480-116">PIC federation is no longer supported by Live Communication Server 2005 SP1 or by Office Communications Server 2007.</span></span> <span data-ttu-id="8b480-117">Поддерживаются следующие платформы для интеграции PIC: Lync Server 2013, Lync Server 2010 и Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="8b480-117">The supported platforms for PIC federation include Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2.</span></span>



</div>

</div>

<div>

## <a name="2-configure-at-least-one-policy-to-support-federated-user-access"></a><span data-ttu-id="8b480-118">2 \.</span><span class="sxs-lookup"><span data-stu-id="8b480-118">2\.</span></span> <span data-ttu-id="8b480-119">настройка не менее одной политики для поддержки доступа федеративных пользователей;</span><span class="sxs-lookup"><span data-stu-id="8b480-119">Configure at least one policy to support federated user access</span></span>

<span data-ttu-id="8b480-120">С помощью панели управления Lync Server администратор должен настроить одну или несколько политик доступа внешних пользователей, чтобы указать, могут ли пользователи Skype работать вместе с внутренними пользователями Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8b480-120">Using the Lync Server Control Panel, an administrator must configure one or more external user access policies to control whether Skype users can collaborate with internal Lync Server users.</span></span>

<span data-ttu-id="8b480-121">![Политики](images/Dn440170.8fd46ad1-9749-422c-8c47-c16ac9032cdb(OCS.15).jpg "Политики")</span><span class="sxs-lookup"><span data-stu-id="8b480-121">![Policies](images/Dn440170.8fd46ad1-9749-422c-8c47-c16ac9032cdb(OCS.15).jpg "Policies")</span></span>

</div>

<div>

## <a name="3-configure-the-skype-pic-provider-setting-for-lync"></a><span data-ttu-id="8b480-122">3 \.</span><span class="sxs-lookup"><span data-stu-id="8b480-122">3\.</span></span> <span data-ttu-id="8b480-123">Настройка параметров поставщика в Skype PIC для Lync</span><span class="sxs-lookup"><span data-stu-id="8b480-123">Configure the Skype PIC provider setting for Lync</span></span>

<span data-ttu-id="8b480-124">С помощью командной консоли Lync Server администратор должен настроить политику клиента Lync, чтобы показать Skype как дополнительный поставщик PIC.</span><span class="sxs-lookup"><span data-stu-id="8b480-124">Using the Lync Server Management Shell, an administrator must configure the Lync client policy to display Skype as an additional PIC provider.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8b480-125">Пользователи поставщиков услуг общедоступной службы обмена мгновенными сообщениями (PIC) не могут принимать участие в СООБЩЕНИЯх, голосовых и видеоконференциях в вашей организации, пока не настроите по крайней мере одну политику (шаг 2, ранее в этой процедуре), чтобы обеспечить поддержку подключения к общедоступным СООБЩЕНИЯм</span><span class="sxs-lookup"><span data-stu-id="8b480-125">Users of the Public Instant Messaging Connectivity (PIC) service providers can’t participate in IM or audio or video conferences in your organization until you also configure at least one policy (step 2, earlier in this procedure) to support public IM connectivity.</span></span>



</div>

1.  <span data-ttu-id="8b480-126">Чтобы настроить федерацию и PIC, обратитесь к разделу "Включение и отключение служб федерации и общедоступной службы обмена мгновенными сообщениями" [https://go.microsoft.com/fwlink/p/?LinkId=306063](https://go.microsoft.com/fwlink/p/?linkid=306063) .</span><span class="sxs-lookup"><span data-stu-id="8b480-126">To configure federation and PIC, see "Enable or Disable Federation and Public IM Connectivity" at [https://go.microsoft.com/fwlink/p/?LinkId=306063](https://go.microsoft.com/fwlink/p/?linkid=306063).</span></span>

2.  <span data-ttu-id="8b480-127">Для настройки хотя бы одной политики для поддержки федеративного доступа пользователей обратитесь к разделу Настройка политики для управления доступом пользователей (Public Users) [https://go.microsoft.com/fwlink/p/?LinkId=306064](https://go.microsoft.com/fwlink/p/?linkid=306064) .</span><span class="sxs-lookup"><span data-stu-id="8b480-127">To configure at least one policy to support federated user access, see "Configure Policies to Control Public User Access" at [https://go.microsoft.com/fwlink/p/?LinkId=306064](https://go.microsoft.com/fwlink/p/?linkid=306064).</span></span>

<span data-ttu-id="8b480-128">**Изменение существующего поставщика Messenger или Skype PIC и его настройка для Skype**</span><span class="sxs-lookup"><span data-stu-id="8b480-128">**To edit an existing Messenger or Skype PIC provider and configure it for Skype**</span></span>

1.  <span data-ttu-id="8b480-129">На сервере переднего плана Lync Server откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="8b480-129">From a Lync Server Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="8b480-130">Выполните две следующие команды:</span><span class="sxs-lookup"><span data-stu-id="8b480-130">Run the following two commands:</span></span>
    
    `Remove-CsPublicProvider -Identity <identity-name>`
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8b480-131">Если у вас еще нет провайдера PIC в вашей среде и вы создаете новый поставщик PIC, вам не нужно запускать командлет <STRONG>Remove-CsPublicProvider</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8b480-131">If you do not already have a PIC provider in your environment and are creating a new PIC provider then you do not need to run the <STRONG>Remove-CsPublicProvider</STRONG> cmdlet.</span></span>

    
    </div>
    
    `New-CsPublicProvider -ProxyFqdn federation.messenger.msn.com -Enabled 1 -Identity Skype  -VerificationLevel 2 -NameDecorationRoutingDomain msn.com -NameDecorationExcludedDomainList "msn.com,outlook.com,live.com,hotmail.com" -IconUrl "https://images.edge.messenger.live.com/Messenger_16x16.png"`
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8b480-132">Добавлена в Lync Server 2013 CU5 &amp; Lync для настольных компьютеров в Office 2013 с пакетом обновления 1 (SP1), NameDecorationRoutingDomain и NameDecorationExcludedDomainList улучшают ситуацию, когда пользователи Lync добавляют контакты Skype, необходимые для того, чтобы "выявлять" домены, не связанные с Microsoft, для идентификации и направления их в Skype (формат: User (contoso. com) @msn. com)</span><span class="sxs-lookup"><span data-stu-id="8b480-132">Added in Lync Server 2013 CU5 &amp; Lync desktop client in Office 2013 SP1, the NameDecorationRoutingDomain and NameDecorationExcludedDomainList improve the situation where Lync users adding Skype contacts needed to “decorate” non-Microsoft domains to identify and route them to Skype (the format of: user(contoso.com)@msn.com).</span></span> <span data-ttu-id="8b480-133">Эти новые параметры позволят автоматически выполнять форматирование адреса пользователя, указанного в диалоговом окне "Добавление контактов Skype" с параметром NameDecorationRoutingDomain (для которого должно быть указано значение "msn.com"), если отсутствуют домены из NameDecorationExcludedDomainList (в настоящее время возможна поддержка доменов msn.com, live.com, Hotmail.com, outlook.com).</span><span class="sxs-lookup"><span data-stu-id="8b480-133">These new settings will allow automatic formatting of the address user’s enter in the “Add Skype contact” dialog box with the NameDecorationRoutingDomain (which should be set to msn.com) if it does not contain the domains in the NameDecorationExcludedDomainList (we currently can support msn.com, live.com, Hotmail.com, outlook.com).</span></span>

    
    </div>

3.  <span data-ttu-id="8b480-134">В клиенте Lync теперь вы можете выбрать Skype в качестве поставщика PIC и добавить клиент Skype, указав учетную запись Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8b480-134">From a Lync client, you can now select Skype as the PIC provider, and add a Skype client by specifying their Microsoft account.</span></span> <span data-ttu-id="8b480-135">Кроме того, пользователь Skype, выполнивший слияние и выполнившего вход с помощью учетной записи Майкрософт, может отправлять запросы на контакт пользователям Lync.</span><span class="sxs-lookup"><span data-stu-id="8b480-135">In addition, a Skype user who has merged and logged in with their Microsoft account can send contact request to Lync users.</span></span> <span data-ttu-id="8b480-136">Дополнительные сведения об учетных записях Майкрософт можно найти [в статье что такое учетная запись Майкрософт?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span><span class="sxs-lookup"><span data-stu-id="8b480-136">For more information about Microsoft accounts, see [What is a Microsoft account?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span></span> <span data-ttu-id="8b480-137">Дополнительные сведения о добавлении клиентов в Lync можно найти [в разделе использование подключения к Lync-Skype в Lync Server 2013 в качестве конечного пользователя](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span><span class="sxs-lookup"><span data-stu-id="8b480-137">For additional information on adding clients to Lync, see [Using Lync-Skype connectivity in Lync Server 2013 as an end user](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span></span>
    
    <span data-ttu-id="8b480-138">![Добавить абонента Skype](images/Dn440170.df0e6ed9-2374-4dfa-a815-87281989487c(OCS.15).jpg "Добавить абонента Skype")</span><span class="sxs-lookup"><span data-stu-id="8b480-138">![Add Skype Contact](images/Dn440170.df0e6ed9-2374-4dfa-a815-87281989487c(OCS.15).jpg "Add Skype Contact")</span></span>

4.  <span data-ttu-id="8b480-139">Подробные сведения об изменении размещенных поставщиков можно найти в разделе Создание или изменение размещенных служб федерации SIP [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065) .</span><span class="sxs-lookup"><span data-stu-id="8b480-139">For detailed information on modifying hosted providers, see "Create or Edit Hosted SIP Federated Providers" at [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065).</span></span>

<span data-ttu-id="8b480-140">Это все административные задачи, которые нужно выполнить на сервере.</span><span class="sxs-lookup"><span data-stu-id="8b480-140">This completes the administrative tasks that must be performed on the server.</span></span> <span data-ttu-id="8b480-141">Теперь вы можете настроить подключение к Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="8b480-141">You are now set up for Lync-Skype connectivity.</span></span>

<span data-ttu-id="8b480-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b480-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

