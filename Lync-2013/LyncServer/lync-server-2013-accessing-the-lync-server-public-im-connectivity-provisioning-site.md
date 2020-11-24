---
title: Доступ к сайту предоставления общедоступной службы обмена мгновенными сообщениями Lync Server
description: Доступ к сайту подготовки службы подключения к общедоступным службам обмена мгновенными сообщениями Lync Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Accessing the Lync Server public IM connectivity provisioning site
ms:assetid: 77a08234-6bcf-4f59-b43b-ee5fc1926585
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440174(v=OCS.15)
ms:contentKeyID: 57793364
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e12916b12de1ef3a3f990c6bee54c312ba6c1992
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398050"
---
# <a name="accessing-the-lync-server-public-im-connectivity-provisioning-site-from-lync-server-2013"></a><span data-ttu-id="df440-103">Доступ к сайту предоставления общедоступной службы обмена мгновенными сообщениями из Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df440-103">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df440-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df440-104">

<span> </span></span></span>

<span data-ttu-id="df440-105">_**Тема последнего изменения:** 2019-03-22_</span><span class="sxs-lookup"><span data-stu-id="df440-105">_**Topic Last Modified:** 2019-03-22_</span></span>

<span data-ttu-id="df440-106">Процесс подготовки к подключению к Lync-Skype изменился по сравнению с предыдущими методами подготовки PIC.</span><span class="sxs-lookup"><span data-stu-id="df440-106">The provisioning process for Lync-Skype connectivity has changed, as compared to previous PIC provisioning methods.</span></span> <span data-ttu-id="df440-107">Для завершения процесса подготовки может потребоваться до тридцати дней.</span><span class="sxs-lookup"><span data-stu-id="df440-107">This provisioning process can take up to thirty days to complete.</span></span> <span data-ttu-id="df440-108">Мы рекомендуем начать этот процесс, прежде чем приступать к выполнению следующих действий, описанных в этом документе.</span><span class="sxs-lookup"><span data-stu-id="df440-108">We recommend that you start this process first, prior to completing the remaining steps in this document.</span></span> <span data-ttu-id="df440-109">После завершения процесса подготовки Lync-Skype для учетной записи, учетная запись активируется, и пользователи, которым разрешено подключаются к ней, смогут подключиться к ней через службу обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="df440-109">After the Lync-Skype provisioning process is completed for your account, the account is activated and your eligible users are enabled for public IM connectivity.</span></span>

### <a name="to-provision-lync-skype-connectivity-you-need-the-following-information"></a><span data-ttu-id="df440-110">Для подготовки Lync-Skype подключения Вам понадобятся следующие данные:</span><span class="sxs-lookup"><span data-stu-id="df440-110">To provision Lync-Skype connectivity, you need the following information:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="df440-111">Номер соглашения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="df440-111">Microsoft Agreement Number</span></span></p></li>
<li><p><span data-ttu-id="df440-112">Полное доменное имя службы пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="df440-112">Access Edge service fully qualified domain name (FQDN)</span></span></p></li>
<li><p><span data-ttu-id="df440-113">Домены протокола SIP.</span><span class="sxs-lookup"><span data-stu-id="df440-113">Session Initiation Protocol (SIP) domain(s)</span></span></p></li>
<li><p><span data-ttu-id="df440-114">Дополнительные полные доменные имена службы пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="df440-114">Any additional Access Edge service FQDNs</span></span></p></li>
<li><p><span data-ttu-id="df440-115">Контактные данные.</span><span class="sxs-lookup"><span data-stu-id="df440-115">Contact information</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df440-116">Начиная с апреля 2019, мы прекращаем сбор и хранение контактных данных для клиентов, которые настроены для Федерации Skype с помощью веб-сайта pic.lync.com.</span><span class="sxs-lookup"><span data-stu-id="df440-116">Beginning in April 2019, we will stop the collection and retention of contact information for customers who are provisioned for Skype Federation via the pic.lync.com website.</span></span> <span data-ttu-id="df440-117">Это изменение делается для того, чтобы убедиться в том, что система подготовки pic.lync.com придерживается политик конфиденциальности корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="df440-117">This change is being made to ensure that the pic.lync.com provisioning system adheres to Microsoft privacy policies.</span></span> 

<span data-ttu-id="df440-118">После того как это изменение станет активным, мы больше не сможете предоставлять обновления по электронной почте для ожидающих изменений в процессе подготовки.</span><span class="sxs-lookup"><span data-stu-id="df440-118">Once this change goes live, we will no longer be able to provide email updates on pending provisioning changes.</span></span> <span data-ttu-id="df440-119">Изменения подготовки PIC обычно загружаются в течение 24-48 часов после ввода.</span><span class="sxs-lookup"><span data-stu-id="df440-119">PIC provisioning changes typically complete within 24-48 hours after being entered.</span></span> <span data-ttu-id="df440-120">Если у вас по-прежнему возникают проблемы с активацией Skype 48 часов после отправки запроса на подготовку, обратитесь в службу технической поддержки Майкрософт, чтобы проанализировать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="df440-120">If you are still experiencing Skype Federation issues 48 hours after submitting a provisioning request, please engage Microsoft Technical Support to investigate further.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df440-121">В рамках этого изменения все ранее введенные контактные данные будут очищены с нашей системы на конец апреля 2019 г.</span><span class="sxs-lookup"><span data-stu-id="df440-121">As part of this change, all previously entered contact information will be purged from our system by the end of April, 2019.</span></span>

### <a name="to-initiate-the-provisioning-process-for-lync-skype-connectivity"></a><span data-ttu-id="df440-122">Чтобы инициировать процесс подготовки к Lync-Skype подключений:</span><span class="sxs-lookup"><span data-stu-id="df440-122">To initiate the provisioning process for Lync-Skype connectivity:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="df440-123">Войдите на веб-сайт <strong>https://pic.lync.com</strong> с помощью идентификатора Microsoft Windows Live ID.</span><span class="sxs-lookup"><span data-stu-id="df440-123">Sign in to the website, <strong>https://pic.lync.com</strong>, using your Microsoft Windows Live ID.</span></span></p></li>
<li><p><span data-ttu-id="df440-124">Выберите тип лицензионного соглашения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="df440-124">Select the Microsoft licensing agreement type.</span></span></p></li>
<li><p><span data-ttu-id="df440-125">Установите флажок, чтобы проверить, что вы прочитали и приняли права на использование продукта для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df440-125">Select the check box, verifying that you have read and accept the Product Use Rights for Lync Server.</span></span></p></li>
<li><p><span data-ttu-id="df440-126">На странице <strong>Инициация запроса на подготовку</strong> щелкните соответствующую ссылку, чтобы инициировать запрос на подготовку:</span><span class="sxs-lookup"><span data-stu-id="df440-126">On the <strong>Initiate a Provisioning Request</strong> page, click the appropriate link to initiate a provisioning request:</span></span></p></li>
<li><p><span data-ttu-id="df440-127">На странице <strong>Определение сведений о подготовке</strong> введите <strong>полное доменное имя службы Edge Access</strong>.</span><span class="sxs-lookup"><span data-stu-id="df440-127">On the <strong>Specify Provisioning Information</strong> page, enter the <strong>Access Edge service FQDN</strong>.</span></span> <span data-ttu-id="df440-128">Например, <strong>SIP.contoso.com</strong>.</span><span class="sxs-lookup"><span data-stu-id="df440-128">For example, <strong>sip.contoso.com</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="df440-129">После 1 июля 2017 Корпорация Майкрософт дополнительно требует, чтобы у пользователей была развернута DNS SRV-запись Федерации для общедоступной службы обмена мгновенными сообщениями, чтобы продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="df440-129">After July 1st, 2017 Microsoft will additionally require customers have the Federation DNS SRV record deployed for Public IM connectivity to continue to work.</span></span>

</li>
<li><p><span data-ttu-id="df440-130">Введите по крайней мере один или несколько доменных имен SIP, а затем нажмите кнопку <strong>Добавить</strong>.</span><span class="sxs-lookup"><span data-stu-id="df440-130">Enter at least one or more SIP domain names, and then click <strong>Add</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="df440-131">Для завершения процесса подготовки необходимы хотя бы один пограничный сервер доступа и один домен SIP.</span><span class="sxs-lookup"><span data-stu-id="df440-131">At least one Access Edge server and one SIP domain are required to complete the provisioning process.</span></span> <span data-ttu-id="df440-132">Домен SIP и пограничный сервер доступа должны быть активными, функционирующими и достижимыми по сети.</span><span class="sxs-lookup"><span data-stu-id="df440-132">The SIP domain and the Access Edge server must be active, functioning, and reachable on the network.</span></span>

</li>
<li><p><span data-ttu-id="df440-133">В списке <strong>поставщиков общедоступной службы обмена мгновенными сообщениями</strong>выберите <strong>Skype</strong> и нажмите кнопку <strong>Далее</strong> , чтобы добавить контактные данные и отправить запрос на подготовку.</span><span class="sxs-lookup"><span data-stu-id="df440-133">In the list of <strong>Public IM Service providers</strong>, select <strong>Skype,</strong> and click <strong>Next</strong> to add contact information, and submit the provisioning request.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


<span data-ttu-id="df440-134">После отправки запроса на подготовку может потребоваться до 30 дней для активации учетной записи и для пользователей, которые должны быть доступны для использования общедоступной службы обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="df440-134">After the provisioning request has been submitted, it can take up to 30 days for the account to activate and for users to be enabled for public IM connectivity.</span></span>

<div>

## <a name="enabling-federation-and-public-im-connectivity-pic"></a><span data-ttu-id="df440-135">Включение федерации и возможности подключения к общедоступным службам обмена мгновенными сообщениями (PIC)</span><span class="sxs-lookup"><span data-stu-id="df440-135">Enabling Federation and Public IM Connectivity (PIC)</span></span>

<span data-ttu-id="df440-136">После отправки запроса на подготовку вы можете сосредоточиться на среде Lync Server и административных задачах, необходимых для настройки подключения к Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="df440-136">After you have submitted the provisioning request, you can focus on the Lync Server environment and administrative tasks required to configure Lync-Skype connectivity.</span></span> <span data-ttu-id="df440-137">В этом разделе предполагается, что администратор сервера Lync Server развернул сервер Lync Server и настроил внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="df440-137">In this section, we assume that the Lync Server administrator has deployed Lync Server and configured external access.</span></span> <span data-ttu-id="df440-138">Дополнительные сведения о настройке внешнего доступа для Lync Server можно найти в разделе Планирование доступа внешних пользователей к сети [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) и "развертывание внешних пользователей Access" [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378) .</span><span class="sxs-lookup"><span data-stu-id="df440-138">For additional information on configuring external access for Lync Server, see "Planning for External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) and "Deploying External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378).</span></span>

<span data-ttu-id="df440-139">Для подготовки среды Lync Server к Lync-Skype подключениям администратор сервера Lync Server должен выполнить следующие три задачи:</span><span class="sxs-lookup"><span data-stu-id="df440-139">To prepare the Lync Server environment for Lync-Skype connectivity, the Lync Server administrator must complete the following three tasks:</span></span>

<div>

## <a name="1-configure-federation-and-pic"></a><span data-ttu-id="df440-140">1 \.</span><span class="sxs-lookup"><span data-stu-id="df440-140">1\.</span></span> <span data-ttu-id="df440-141">настройка федерации и PIC;</span><span class="sxs-lookup"><span data-stu-id="df440-141">Configure Federation and PIC</span></span>

<span data-ttu-id="df440-142">Для того чтобы пользователи Skype могли общаться с пользователями Lync в вашей организации, требуется Федерация.</span><span class="sxs-lookup"><span data-stu-id="df440-142">Federation is required to enable Skype users to communicate with Lync users in your organization.</span></span> <span data-ttu-id="df440-143">Общедоступная служба обмена мгновенными сообщениями (PIC) — это класс Федерации, и он должен быть настроен для предоставления пользователям Lync возможности общаться с пользователями Skype.</span><span class="sxs-lookup"><span data-stu-id="df440-143">Public Instant Messaging Connectivity (PIC) is a class of federation, and it must be configured to enable your Lync users to communicate with Skype users.</span></span> <span data-ttu-id="df440-144">Федерация и PIC настраиваются с помощью панели управления Lync Server, показанной ниже.</span><span class="sxs-lookup"><span data-stu-id="df440-144">Federation and PIC are configured by using the Lync Server Control Panel, shown below.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="df440-145">Федерация PIC больше не поддерживается в Live Communication Server 2005 с пакетом обновления 1 (SP1) и Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="df440-145">PIC federation is no longer supported by Live Communication Server 2005 SP1 or by Office Communications Server 2007.</span></span> <span data-ttu-id="df440-146">Поддерживаются следующие платформы для интеграции PIC: Lync Server 2013, Lync Server 2010 и Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="df440-146">The supported platforms for PIC federation include Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2.</span></span>



</div>

</div>

<div>

## <a name="2-configure-at-least-one-policy-to-support-federated-user-access"></a><span data-ttu-id="df440-147">2 \.</span><span class="sxs-lookup"><span data-stu-id="df440-147">2\.</span></span> <span data-ttu-id="df440-148">настройка не менее одной политики для поддержки доступа федеративных пользователей;</span><span class="sxs-lookup"><span data-stu-id="df440-148">Configure at least one policy to support federated user access</span></span>

<span data-ttu-id="df440-149">С помощью панели управления Lync Server администратор должен настроить одну или несколько политик доступа внешних пользователей, чтобы указать, могут ли пользователи Skype работать вместе с внутренними пользователями Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df440-149">Using the Lync Server Control Panel, an administrator must configure one or more external user access policies to control whether Skype users can collaborate with internal Lync Server users.</span></span>

</div>

<div>

## <a name="3-configure-the-skype-pic-provider-setting-for-lync"></a><span data-ttu-id="df440-150">3 \.</span><span class="sxs-lookup"><span data-stu-id="df440-150">3\.</span></span> <span data-ttu-id="df440-151">Настройка параметров поставщика в Skype PIC для Lync</span><span class="sxs-lookup"><span data-stu-id="df440-151">Configure the Skype PIC provider setting for Lync</span></span>

<span data-ttu-id="df440-152">С помощью командной консоли Lync Server администратор должен настроить политику клиента Lync, чтобы показать Skype как дополнительный поставщик PIC.</span><span class="sxs-lookup"><span data-stu-id="df440-152">Using the Lync Server Management Shell, an administrator must configure the Lync client policy to display Skype as an additional PIC provider.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="df440-153">Пользователи поставщиков общедоступной службы обмена мгновенными сообщениями (PIC) не смогут участвовать в обмене мгновенными сообщениями и конференциях организации, пока не будет настроена хотя бы одна политика поддержки этой службы (действие 2, описанное выше). </span><span class="sxs-lookup"><span data-stu-id="df440-153">Users of the Public Instant Messaging Connectivity (PIC) service providers can’t participate in IM or conferences in your organization until you also configure at least one policy (step 2, earlier in this procedure) to support public IM connectivity.</span></span><BR><span data-ttu-id="df440-154">Чтобы настроить федерацию и PIC, обратитесь к разделу "Включение и отключение служб федерации и общедоступной службы обмена мгновенными сообщениями" <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A> .</span><span class="sxs-lookup"><span data-stu-id="df440-154">To configure federation and PIC, see "Enable or Disable Federation and Public IM Connectivity" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A>.</span></span><BR><span data-ttu-id="df440-155">Для настройки хотя бы одной политики для поддержки федеративного доступа пользователей обратитесь к разделу Настройка политики для управления доступом пользователей (Public Users) <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A> .</span><span class="sxs-lookup"><span data-stu-id="df440-155">To configure at least one policy to support federated user access, see "Configure Policies to Control Public User Access" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A>.</span></span>



</div>

1.  <span data-ttu-id="df440-156">На сервере переднего плана Lync Server откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="df440-156">From a Lync Server Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="df440-157">Выполните две следующие команды:</span><span class="sxs-lookup"><span data-stu-id="df440-157">Run the following two commands:</span></span>
    
      - `Remove-CsPublicProvider -Identity <identity-name>`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="df440-158">Если у вас еще нет провайдера PIC в вашей среде и вы создаете новый поставщик PIC, вам не нужно запускать командлет <STRONG>Remove-CsPublicProvider</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="df440-158">If you do not already have a PIC provider in your environment and are creating a new PIC provider then you do not need to run the <STRONG>Remove-CsPublicProvider</STRONG> cmdlet.</span></span>

        
        </div>
    
      - `New-CsPublicProvider -ProxyFqdn federation.messenger.msn.com -Enabled 1 -Identity Skype  -VerificationLevel 2 -NameDecorationRoutingDomain msn.com -NameDecorationExcludedDomainList "msn.com,outlook.com,live.com,hotmail.com" -IconUrl "https://images.edge.messenger.live.com/Messenger_16x16.png"`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="df440-159">Добавлена в Lync Server 2013 CU5 &amp; Lync для настольных компьютеров в Office 2013 с пакетом обновления 1 (SP1), NameDecorationRoutingDomain и NameDecorationExcludedDomainList улучшают ситуацию, когда пользователи Lync добавляют контакты Skype, необходимые для того, чтобы "выявлять" домены, не связанные с Microsoft, для идентификации и направления их в Skype (формат: User (contoso. com) @msn. com)</span><span class="sxs-lookup"><span data-stu-id="df440-159">Added in Lync Server 2013 CU5 &amp; Lync desktop client in Office 2013 SP1, the NameDecorationRoutingDomain and NameDecorationExcludedDomainList improve the situation where Lync users adding Skype contacts needed to “decorate” non-Microsoft domains to identify and route them to Skype (the format of: user(contoso.com)@msn.com).</span></span> <span data-ttu-id="df440-160">Эти новые параметры позволят автоматически выполнять форматирование адреса пользователя, указанного в диалоговом окне "Добавление контактов Skype" с параметром NameDecorationRoutingDomain (для которого должно быть указано значение "msn.com"), если отсутствуют домены из NameDecorationExcludedDomainList (в настоящее время возможна поддержка доменов msn.com, live.com, Hotmail.com, outlook.com).</span><span class="sxs-lookup"><span data-stu-id="df440-160">These new settings will allow automatic formatting of the address user’s enter in the “Add Skype contact” dialog box with the NameDecorationRoutingDomain (which should be set to msn.com) if it does not contain the domains in the NameDecorationExcludedDomainList (we currently can support msn.com, live.com, Hotmail.com, outlook.com).</span></span>

        
        </div>

3.  <span data-ttu-id="df440-161">В клиенте Lync теперь вы можете выбрать Skype в качестве поставщика PIC и добавить клиент Skype, указав учетную запись Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="df440-161">From a Lync client, you can now select Skype as the PIC provider, and add a Skype client by specifying their Microsoft account.</span></span> <span data-ttu-id="df440-162">Кроме того, пользователь Skype, выполнивший слияние и выполнившего вход с помощью учетной записи Майкрософт, может отправлять запросы на контакт пользователям Lync.</span><span class="sxs-lookup"><span data-stu-id="df440-162">In addition, a Skype user who has merged and logged in with their Microsoft account can send contact request to Lync users.</span></span> <span data-ttu-id="df440-163">Дополнительные сведения об учетных записях Майкрософт можно найти [в статье что такое учетная запись Майкрософт?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span><span class="sxs-lookup"><span data-stu-id="df440-163">For more information about Microsoft accounts, see [What is a Microsoft account?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span></span> <span data-ttu-id="df440-164">Дополнительные сведения о добавлении клиентов в Lync можно найти [в разделе использование подключения к Lync-Skype в Lync Server 2013 в качестве конечного пользователя](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span><span class="sxs-lookup"><span data-stu-id="df440-164">For additional information on adding clients to Lync, see [Using Lync-Skype connectivity in Lync Server 2013 as an end user](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span></span>

4.  <span data-ttu-id="df440-165">Подробные сведения об изменении размещенных поставщиков можно найти в разделе Создание или изменение размещенных служб федерации SIP [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065) .</span><span class="sxs-lookup"><span data-stu-id="df440-165">For detailed information on modifying hosted providers, see "Create or Edit Hosted SIP Federated Providers" at [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065).</span></span>

<span data-ttu-id="df440-166">Это все административные задачи, которые нужно выполнить на сервере.</span><span class="sxs-lookup"><span data-stu-id="df440-166">This completes the administrative tasks that must be performed on the server.</span></span> <span data-ttu-id="df440-167">Теперь вы можете настроить подключение к Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="df440-167">You are now set up for Lync-Skype connectivity.</span></span>

</div>

</div>

<div>

## <a name="additional-resources"></a><span data-ttu-id="df440-168">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df440-168">Additional Resources</span></span>

[<span data-ttu-id="df440-169">Взаимодействие между конечными пользователями Lync и Skype в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df440-169">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

[<span data-ttu-id="df440-170">Руководство по подготовке взаимодействия Lync-Skype в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df440-170">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-provisioning-guide-for-lync-skype-connectivity.md)

<span data-ttu-id="df440-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df440-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

