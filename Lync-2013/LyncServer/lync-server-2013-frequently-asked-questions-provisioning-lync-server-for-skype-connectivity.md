---
title: 'Часто задаваемые вопросы: подготовка сервера Lync Server для подключения Skype'
description: 'Вопросы и ответы: Подготовка сервера Lync Server для подключения к Skype.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Frequently Asked Questions: Provisioning Lync Server for Skype connectivity'
ms:assetid: 4d1b2bfc-780b-4b8c-afd5-11c2e59203b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440172(v=OCS.15)
ms:contentKeyID: 57793362
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bd9e9089f4b17f8b439bf11be05bfb6ce7c6d9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428064"
---
# <a name="frequently-asked-questions-provisioning-lync-server-2013-for-skype-connectivity"></a><span data-ttu-id="19147-103">Часто задаваемые вопросы: подготовка сервера Lync Server 2013 для подключения Skype</span><span class="sxs-lookup"><span data-stu-id="19147-103">Frequently Asked Questions: Provisioning Lync Server 2013 for Skype connectivity</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19147-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19147-104">

<span> </span></span></span>

<span data-ttu-id="19147-105">_**Тема последнего изменения:** 2019-03-22_</span><span class="sxs-lookup"><span data-stu-id="19147-105">_**Topic Last Modified:** 2019-03-22_</span></span>

<span data-ttu-id="19147-106">Начиная с апреля 2019, мы прекращаем сбор и хранение контактных данных для клиентов, которые настроены для Федерации Skype с помощью веб-сайта pic.lync.com.</span><span class="sxs-lookup"><span data-stu-id="19147-106">Beginning in April 2019, we will stop the collection and retention of contact information for customers who are provisioned for Skype Federation via the pic.lync.com website.</span></span> <span data-ttu-id="19147-107">Это изменение делается для того, чтобы убедиться в том, что система подготовки pic.lync.com придерживается политик конфиденциальности корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="19147-107">This change is being made to ensure that the pic.lync.com provisioning system adheres to Microsoft privacy policies.</span></span> 
 
<span data-ttu-id="19147-108">После того как это изменение станет активным, мы больше не сможете предоставлять обновления по электронной почте для ожидающих изменений в процессе подготовки.</span><span class="sxs-lookup"><span data-stu-id="19147-108">Once this change goes live, we will no longer be able to provide email updates on pending provisioning changes.</span></span> <span data-ttu-id="19147-109">Изменения подготовки PIC обычно загружаются в течение 24-48 часов после ввода.</span><span class="sxs-lookup"><span data-stu-id="19147-109">PIC provisioning changes typically complete within 24-48 hours after being entered.</span></span> <span data-ttu-id="19147-110">Если у вас по-прежнему возникают проблемы с активацией Skype 48 часов после отправки запроса на подготовку, обратитесь в службу технической поддержки Майкрософт, чтобы проанализировать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="19147-110">If you are still experiencing Skype Federation issues 48 hours after submitting a provisioning request, please engage Microsoft Technical Support to investigate further.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19147-111">В рамках этого изменения все ранее введенные контактные данные будут очищены с нашей системы на конец апреля 2019 г.</span><span class="sxs-lookup"><span data-stu-id="19147-111">As part of this change, all previously entered contact information will be purged from our system by the end of April, 2019.</span></span>


<span data-ttu-id="19147-112">**Вопрос: какие функции поддерживаются в Microsoft Lync и Skype?**</span><span class="sxs-lookup"><span data-stu-id="19147-112">**Q: What features are supported between Microsoft Lync and Skype?**</span></span>

<span data-ttu-id="19147-113">**A:** С помощью Skype теперь вы можете получить доступ к новым возможностям, которые позволят вам разнимать сотни миллионов пользователей, использующих Skype, для расширения распространенных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="19147-113">**A:** With Skype now part of the Microsoft family, new possibilities open up for extending unified communications scenarios to the hundreds of millions of people who use Skype.</span></span> <span data-ttu-id="19147-114">Благодаря этой комбинации Пользователи Lync смогут подключаться и сотрудничать с поставщиками, клиентами и партнерами, полагаться на богатую работу Lync и предоставление доступа к Skype.</span><span class="sxs-lookup"><span data-stu-id="19147-114">This combination will enable Lync customers to connect and collaborate with suppliers, customers, and partners, relying on the richness of Lync and the reach of Skype.</span></span>

  - <span data-ttu-id="19147-115">Обмен мгновенными сообщениями, голосовые и видеозвонки и обмен сообщениями между Lync и пользователями Skype</span><span class="sxs-lookup"><span data-stu-id="19147-115">Instant Message and Audio and Video Calls—Federated audio and video calling and instant messaging between Lync and Skype users</span></span>

  - <span data-ttu-id="19147-116">Совместное использование сведений о присутствии, Обмен данными о присутствии между федеративными контактами</span><span class="sxs-lookup"><span data-stu-id="19147-116">Presence Sharing— Exchange presence information between federated contacts</span></span>

  - <span data-ttu-id="19147-117">Простое администрирование — параметры и элементы управления для настройки федеративных коммуникаций в соответствии с политиками и стандартами Организации.</span><span class="sxs-lookup"><span data-stu-id="19147-117">Simple Administration—Settings and controls to configure federated communications in accordance with your organization’s policies and standards</span></span>

<span data-ttu-id="19147-118">**В: как определить, как подключаться к развертыванию Lync с помощью Skype?**</span><span class="sxs-lookup"><span data-stu-id="19147-118">**Q: How do I qualify to connect my Lync deployment with Skype?**</span></span>

<span data-ttu-id="19147-119">**A:** Лицензировано для связи с абонентом Skype, если вы используете один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="19147-119">**A:** You are licensed for Skype connectivity if you have either:</span></span>

  - <span data-ttu-id="19147-120">Lync Server (2010 или 2013) и клиентские лицензии на Lync Server Standard ("лицензии"; 2010 или 2013) для пользователей и (или) устройств в вашей организации, которые будут подключаться к Skype.</span><span class="sxs-lookup"><span data-stu-id="19147-120">Lync Server (2010 or 2013) plus Lync Server Standard Client Access Licenses (“CALs”; 2010 or 2013) for the users and/or devices in your organization that will connect to Skype.</span></span> 

  - <span data-ttu-id="19147-121">Lync Online (как отдельные лицензии, так и в составе пакета Office 365).</span><span class="sxs-lookup"><span data-stu-id="19147-121">Lync Online (as standalone licenses or as part of an Office 365 suite).</span></span>  <span data-ttu-id="19147-122">Однако эта служба (pic.lync.com) предназначена только для подготовки к развертыванию Lync Server и гибридного развертывания Lync Server и Lync Online.</span><span class="sxs-lookup"><span data-stu-id="19147-122">However, this service (pic.lync.com) is only for provisioning Lync Server and hybrid Lync Server and Lync Online deployments.</span></span>  <span data-ttu-id="19147-123">Подготовка к работе с Lync Online PIC осуществляется на панели управления Lync Online (LOCP).</span><span class="sxs-lookup"><span data-stu-id="19147-123">Lync Online PIC provisioning is done in Lync Online Control Panel (LOCP).</span></span>

<span data-ttu-id="19147-124">**Вопрос: что необходимо для того, чтобы пользователи Lync были подключены к контактам Skype?**</span><span class="sxs-lookup"><span data-stu-id="19147-124">**Q: What must Lync end users do to connect to Skype contacts?**</span></span>

<span data-ttu-id="19147-125">**A:** После активации домена и включения функций администратором Lync Пользователи Lync могут добавлять контакты Skype в свои списки контактов в клиенте Lync.</span><span class="sxs-lookup"><span data-stu-id="19147-125">**A:** After a domain is activated and the features are enabled by an organization’s Lync administrator, Lync users can add Skype contacts to their contact lists within the Lync client.</span></span>

<span data-ttu-id="19147-126">**Вопрос: что необходимо для того, чтобы пользователи Skype были подключены к контактам Lync?**</span><span class="sxs-lookup"><span data-stu-id="19147-126">**Q: What must Skype end users do to connect to Lync contacts?**</span></span>

<span data-ttu-id="19147-127">**A:** Все пользователи Skype, желающие подключиться к пользователю Lync, должны иметь учетную запись Майкрософт, связанную с идентификаторами Skype, и входить в нее с помощью учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="19147-127">**A:** All Skype users wishing to connect to a Lync user must have a Microsoft Account associated with their Skype IDs and sign in using the Microsoft Account.</span></span>  <span data-ttu-id="19147-128">Это можно включить в клиенте Skype.</span><span class="sxs-lookup"><span data-stu-id="19147-128">This can be enabled within the Skype client.</span></span>

<span data-ttu-id="19147-129">**Вопрос: интеграция с Windows Live по-прежнему доступна?**</span><span class="sxs-lookup"><span data-stu-id="19147-129">**Q: Is federation with Windows Live still available?**</span></span>

<span data-ttu-id="19147-130">**A:** Начиная с октября, 2012 Корпорация Майкрософт приступила к переходу на Skype для Windows Live Messenger (WLM), а в конечном итоге выпустили WLM.</span><span class="sxs-lookup"><span data-stu-id="19147-130">**A:** Beginning in October, 2012, Microsoft started helping Windows Live Messenger (WLM) users move to Skype, en route to eventually retiring WLM.</span></span> <span data-ttu-id="19147-131">Lync продолжит поддерживать Федерацию с WLM, пока WLM находится на рынке, но никакие дополнительные активации доменов для Windows Live не будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="19147-131">Lync will continue to support federation with WLM as long as WLM is in market, but no additional Windows Live domain activations will be allowed.</span></span> <span data-ttu-id="19147-132">Передвижение WLM пользователей поддерживается Skype 6,0 для Mac и Windows (выпущено 25 октября 2012 г.), что позволяет входить в систему с помощью учетной записи Майкрософт (например, тех же учетных данных, что и WLM).</span><span class="sxs-lookup"><span data-stu-id="19147-132">The movement of WLM users is enabled by the Skype 6.0 for Mac and Windows (released October 25, 2012) which allows signing in with a Microsoft Account (i.e., the same credentials as WLM).</span></span> <span data-ttu-id="19147-133">После того как вы просто входите в Skype, WLM контакты автоматически заполняются в Skype, и пользователи могут воспользоваться преимуществами расширенных возможностей связи в Skype, такими как звонки на стационарные телефоныные и мобильные телефоны, демонстрацию экрана, групповые видеозвонки и поддержка широкого спектра устройств.</span><span class="sxs-lookup"><span data-stu-id="19147-133">After simply signing in to Skype, WLM buddy lists automatically populate into Skype, and users can take advantage of Skype’s expanded communication capabilities such as calling landlines and mobiles, screen sharing, group video calling, and support for a wide variety of devices.</span></span> <span data-ttu-id="19147-134">Кроме того, Объединенные контакты Lync пользователей WLM подключаются к Skype вместе с другими списками контактов, и обмен мгновенными сообщениями между Skype и Lync для этих абонентов будет возможен немедленно.</span><span class="sxs-lookup"><span data-stu-id="19147-134">Moreover, WLM users’ federated Lync contacts follow the transition into Skype with the rest of their buddy lists, and IM between Skype and Lync for these contacts will be available immediately.</span></span> <span data-ttu-id="19147-135">Пользователям Lync не нужно ничего делать для обеспечения бесперебойности обслуживания.</span><span class="sxs-lookup"><span data-stu-id="19147-135">Lync customers do not need to do anything to enable this continuity of service.</span></span>

<span data-ttu-id="19147-136">**Вопрос: интеграция с Yahoo \! или AOL по-прежнему доступна?**</span><span class="sxs-lookup"><span data-stu-id="19147-136">**Q: Is federation with Yahoo\! or AOL still available?**</span></span>

<span data-ttu-id="19147-137">**A:** Нет.</span><span class="sxs-lookup"><span data-stu-id="19147-137">**A:** No.</span></span> <span data-ttu-id="19147-138">Интеграция с Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="19147-138">Federation with Yahoo\!</span></span> <span data-ttu-id="19147-139">и AOL в зависимости от поддержки Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="19147-139">and AOL were contingent upon support from Yahoo\!</span></span> <span data-ttu-id="19147-140">и AOL.</span><span class="sxs-lookup"><span data-stu-id="19147-140">and AOL.</span></span> <span data-ttu-id="19147-141">Как для Yahoo, так и для\!</span><span class="sxs-lookup"><span data-stu-id="19147-141">For both Yahoo\!</span></span> <span data-ttu-id="19147-142">и AOL, служба заканчивается 30 июня 2014 г.</span><span class="sxs-lookup"><span data-stu-id="19147-142">and AOL, the service ended on June 30, 2014.</span></span> 

<span data-ttu-id="19147-143">**Вопрос: Могу ли я запробовать подключение к Skype перед покупкой Lync?**</span><span class="sxs-lookup"><span data-stu-id="19147-143">**Q: Can I trial Skype connectivity before purchasing Lync?**</span></span>

<span data-ttu-id="19147-144">**A:** Возможность подключения к Skype не предоставляется для пробной версии.</span><span class="sxs-lookup"><span data-stu-id="19147-144">**A:** Skype connectivity is not offered on a trial basis.</span></span> <span data-ttu-id="19147-145">Вместо пробной версии пользователи Lync с подходящими лицензиями должны просто зарегистрироваться в службе для проверки.</span><span class="sxs-lookup"><span data-stu-id="19147-145">In place of a trial, Lync customers with eligible licenses are encouraged to simply sign up for the service to test.</span></span>

<span data-ttu-id="19147-146">**Вопрос: какая информация нужна для подготовки?**</span><span class="sxs-lookup"><span data-stu-id="19147-146">**Q: What information is required for provisioning?**</span></span>

<span data-ttu-id="19147-147">**A:** Чтобы отправить запрос на подготовку в рамках квалифицированной лицензии, вам понадобятся следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="19147-147">**A:** To submit a provisioning request under a qualified license, you need the following:</span></span>

  - <span data-ttu-id="19147-148">Номер соглашения (Майкрософт):</span><span class="sxs-lookup"><span data-stu-id="19147-148">Microsoft agreement number:</span></span>
    
      - <span data-ttu-id="19147-149">Поддержка по программе корпоративного лицензирования Майкрософт: номер соглашения корпоративного лицензирования Майкрософт</span><span class="sxs-lookup"><span data-stu-id="19147-149">Microsoft Volume Licensing Support: Microsoft Volume Licensing Agreement number</span></span>
    
      - <span data-ttu-id="19147-150">Сеть партнера Майкрософт: идентификатор партнера в штаб-Квартирае</span><span class="sxs-lookup"><span data-stu-id="19147-150">Microsoft Partner Network: Headquarter partner ID</span></span>
    
      - <span data-ttu-id="19147-151">Лицензионное соглашение поставщика услуг: первоначальный регистрационный номер</span><span class="sxs-lookup"><span data-stu-id="19147-151">Service Provider Licensing Agreement: Initial enrollment number</span></span>
    
      - <span data-ttu-id="19147-152">Большие объемы услуг: номер регистрации продукта</span><span class="sxs-lookup"><span data-stu-id="19147-152">High Volume Services: Product enrollment number</span></span>

  - <span data-ttu-id="19147-153">Полные доменные имена (FQDN) для службы пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="19147-153">Fully qualified domain names (FQDNs) for the Access Edge service.</span></span>
    
      - <span data-ttu-id="19147-154">Требуется полное доменное имя по крайней мере одной службы пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="19147-154">FQDN for at least one Access Edge service is required.</span></span>
    
      - <span data-ttu-id="19147-155">Если в вашей организации более одного сервера, на котором запущена служба пограничного доступа, укажите полные доменные имена для каждой дополнительной службы доступа к доступу.</span><span class="sxs-lookup"><span data-stu-id="19147-155">If your organization has more than one server running the Access Edge service, specify the FQDNs for each additional Access Edge service.</span></span> <span data-ttu-id="19147-156">Внимание! если вы ранее указали полное доменное имя для службы Edge Access и хотите изменить его, подготовка к изменению может занять несколько дней, и это может привести к нарушению обслуживания.</span><span class="sxs-lookup"><span data-stu-id="19147-156">Important: If you previously specified an FQDN for the Access Edge service and want to change it, provisioning for the change can take several days to complete and can result in a disruption in service.</span></span> <span data-ttu-id="19147-157">Чтобы предотвратить прерывание работы службы, рекомендуется сохранить ранее указанное ДОМЕНное имя службы Edge Access.</span><span class="sxs-lookup"><span data-stu-id="19147-157">To prevent service disruption, we recommend that you maintain the previously specified FQDN of the Access Edge service.</span></span>

  - <span data-ttu-id="19147-158">Домены протокола запуска сеансов (SIP).</span><span class="sxs-lookup"><span data-stu-id="19147-158">Session Initiation Protocol (SIP) domain(s).</span></span> <span data-ttu-id="19147-159">Это доменный суффикс URI SIP, который пользователи в настоящее время используют для обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="19147-159">This is the domain suffix of the SIP URI that users currently use for instant messaging.</span></span> <span data-ttu-id="19147-160">Если в вашей организации есть несколько доменов SIP, укажите доменные суффиксы для каждого домена, используемого для обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="19147-160">If your organization has more than one SIP domain, specify the domain suffix for each domain used for instant messaging.</span></span> <span data-ttu-id="19147-161">Например, для user1@contoso.com укажите contoso.com для домена SIP. в user1@example.fabrikam.com укажите example.fabrikam.com в качестве домена SIP.</span><span class="sxs-lookup"><span data-stu-id="19147-161">For example, for user1@contoso.com, specify contoso.com for the SIP domain; for user1@example.fabrikam.com, specify example.fabrikam.com as the SIP domain.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="19147-162">Указывайте только доменные суффиксы для домена SIP.</span><span class="sxs-lookup"><span data-stu-id="19147-162">Specify only the domain suffix for the SIP domain.</span></span> <span data-ttu-id="19147-163">Не указывайте полные доменные имена, включая полное доменное имя для службы EDGE, для домена SIP.</span><span class="sxs-lookup"><span data-stu-id="19147-163">Do not specify any FQDNs, including the FQDN for the Access Edge service, for the SIP domain.</span></span>

    
    </div>

  - <span data-ttu-id="19147-164">Контактные данные.</span><span class="sxs-lookup"><span data-stu-id="19147-164">Contact information.</span></span> <span data-ttu-id="19147-165">Укажите адрес электронной почты для администратора каждого из указанных доменов SIP.</span><span class="sxs-lookup"><span data-stu-id="19147-165">Specify an e-mail address for the administrator of each SIP domain that you specify.</span></span>

<span data-ttu-id="19147-166">**Вопрос: как включить Lync-Skype подключение в сценарии с разделением доменов?**</span><span class="sxs-lookup"><span data-stu-id="19147-166">**Q: How do I enable Lync-Skype Connectivity in a split-domain scenario?**</span></span>

<span data-ttu-id="19147-167">**A:** Если у вас есть сценарий Lync Online 2013 и Lync Server с локальным доменом с разделением (пользователи находятся в сети и локально с помощью одного и того же домена SIP), включите Lync-Skype подключение, выполнив эти два действия в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="19147-167">**A:** If you have a Lync Online 2013 and Lync Server on-premise split-domain scenario (with users on both online and on-premise using the same SIP domain), enable Lync-Skype Connectivity by doing these two steps in the following order</span></span>

1.  <span data-ttu-id="19147-168">Настройка подключения к локальной сети Lync-Skype, как описано в руководстве по подготовке PIC.</span><span class="sxs-lookup"><span data-stu-id="19147-168">Set up on-premise Lync-Skype Connectivity as explained in the PIC Provisioning Guide.</span></span>

2.  <span data-ttu-id="19147-169">Дождитесь появления подтверждения о том, что ваш домен был предоставлен корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="19147-169">Wait until you see confirmation that your domain has been provisioned by Microsoft.</span></span>

3.  <span data-ttu-id="19147-170">После появления подтверждения с помощью центра администрирования Lync включите функцию "внешняя связь".</span><span class="sxs-lookup"><span data-stu-id="19147-170">After you see the confirmation, use the Lync admin center to turn on “external communications”.</span></span> <span data-ttu-id="19147-171">Дополнительные сведения можно найти в разделе [https://office.microsoft.com/support/configure-external-communications-HA102817865.aspx?CTT=5\&origin=HA102817356](https://office.microsoft.com/support/configure-external-communications-ha102817865.aspx?ctt=5%26origin=ha102817356)</span><span class="sxs-lookup"><span data-stu-id="19147-171">For more information, see [https://office.microsoft.com/support/configure-external-communications-HA102817865.aspx?CTT=5\&origin=HA102817356](https://office.microsoft.com/support/configure-external-communications-ha102817865.aspx?ctt=5%26origin=ha102817356)</span></span>

<span data-ttu-id="19147-172">Этот порядок важен.</span><span class="sxs-lookup"><span data-stu-id="19147-172">This order is important.</span></span>  <span data-ttu-id="19147-173">Прежде чем включать связь в Lync Online, необходимо настроить подключение к локальной сети.</span><span class="sxs-lookup"><span data-stu-id="19147-173">You must set up the on-premise connectivity before you enable the communications in Lync Online.</span></span> <span data-ttu-id="19147-174">При обратном порядке данные, введенные для локального использования, <https://pic.lync.com> не будут проходить через.</span><span class="sxs-lookup"><span data-stu-id="19147-174">If the order is reversed, the information entered for on-premise in <https://pic.lync.com> will not go through.</span></span> <span data-ttu-id="19147-175">Если вы уже настроили Lync Online для внешней связи с этим доменом, вы должны отключить его, подождать 24 часа, а <https://pic.lync.com> затем включить внешнюю связь для Lync Online.</span><span class="sxs-lookup"><span data-stu-id="19147-175">If you have already set up Lync Online for external communications with this domain, you must turn it off, wait for 24 hours, and start again, first by entering your on-premise information at <https://pic.lync.com> and then turning on external communications for Lync Online.</span></span>

<span data-ttu-id="19147-176">**Вопрос: можно ли подготовить несколько полных доменных имен службы доступа к сети для подключения к Skype?**</span><span class="sxs-lookup"><span data-stu-id="19147-176">**Q: Can I provision multiple Access Edge service FQDNs for Skype connectivity?**</span></span>

<span data-ttu-id="19147-177">**A:** Вы можете подготовить только одно полное доменное имя для доступа к одному или нескольким доменам.</span><span class="sxs-lookup"><span data-stu-id="19147-177">**A:** You can provision only one access edge FQDN for one or more domains.</span></span> <span data-ttu-id="19147-178">Вы можете подготовить несколько полных доменных имен EDGE, до 10 для одного запроса, если у них есть отдельные домены.</span><span class="sxs-lookup"><span data-stu-id="19147-178">You can provision multiple access edge FQDNs, up to 10 per request, if they have distinct domains.</span></span>

<span data-ttu-id="19147-179">**В: я могу получить список адресов электронной почты Майкрософт, которые вы нашли для Организации, запрашивающей подготовку к работе.**</span><span class="sxs-lookup"><span data-stu-id="19147-179">**Q: Can I obtain the list of Microsoft Account e-mail addresses that you find for the organization requesting provisioning?**</span></span>

<span data-ttu-id="19147-180">**A:** Нет.</span><span class="sxs-lookup"><span data-stu-id="19147-180">**A:** No.</span></span> <span data-ttu-id="19147-181">Эти адреса рассматриваются как личные данные и не являются общими.</span><span class="sxs-lookup"><span data-stu-id="19147-181">These addresses are considered personally identifiable information and are not shared.</span></span>

<span data-ttu-id="19147-182">**Вопрос: как добавить контакт Windows Live Messenger с ИДЕНТИФИКАТОРом, который содержит домен, отличный от того, который поддерживается Windows Live?**</span><span class="sxs-lookup"><span data-stu-id="19147-182">**Q: How do I add a Windows Live Messenger contact that has an ID containing a domain other than those supported by Windows Live?**</span></span>

<span data-ttu-id="19147-183">**A:** Если вы добавляете пользователя Windows Live Messenger с учетной записью или ИДЕНТИФИКАТОРом в домен, не относящийся к Windows Live, введите адрес в следующем формате: \<user name\> ( \<domain name\> ) @msn. com, где \<domain name\> — имя домена в адресе электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="19147-183">**A:** If you are adding a Windows Live Messenger user with an account or ID with a non-Windows Live domain, enter the address in the following format: \<user name\>(\<domain name\>)@msn.com, where \<domain name\> is the domain name in the e-mail address of the user.</span></span> <span data-ttu-id="19147-184">Например, если вы хотите добавить ted@contoso.com, вы можете использовать следующий формат: \ мои (contoso. com) @msn. com.</span><span class="sxs-lookup"><span data-stu-id="19147-184">For example, if you wanted to add ted@contoso.com, you would use the following format: ted(contoso.com)@msn.com.</span></span> <span data-ttu-id="19147-185">Список доменов, администрируемых с помощью Windows Live, можно найти в разделе Поддерживаемые домены на странице "известные проблемы, связанные с обменом мгновенными сообщениями после установки пакета обновления 1 (SP1) для Live Communications Server) https://support.microsoft.com/?kbid=897567 .</span><span class="sxs-lookup"><span data-stu-id="19147-185">For a list of domains that are administered by Windows Live, see the Supported Domains section in “Known Issues That Occur with Public Instant Messaging After You Install Live Communications Server Service Pack 1” at https://support.microsoft.com/?kbid=897567.</span></span>

<span data-ttu-id="19147-186">**Вопрос: сколько времени займет процесс подготовки?**</span><span class="sxs-lookup"><span data-stu-id="19147-186">**Q: How long does the provisioning process take?**</span></span>

<span data-ttu-id="19147-187">**A:** Для подготовки может потребоваться до 30 дней.</span><span class="sxs-lookup"><span data-stu-id="19147-187">**A:** Provisioning can take up to 30 days.</span></span>

<span data-ttu-id="19147-188">**Вопрос: как узнать, когда будет выполнена подготовка?**</span><span class="sxs-lookup"><span data-stu-id="19147-188">**Q: How will I know when provisioning is complete?**</span></span>

<span data-ttu-id="19147-189">**A:** Корпорация Майкрософт отправит уведомление по электронной почте о завершении подготовки.</span><span class="sxs-lookup"><span data-stu-id="19147-189">**A:** Microsoft will send e-mail notification when provisioning is complete.</span></span>

<span data-ttu-id="19147-190">**Вопрос: как обновить конфигурацию или контактные данные, которые вы отправляете?**</span><span class="sxs-lookup"><span data-stu-id="19147-190">**Q: How can I update the configuration or contact details that I submit?**</span></span>

<span data-ttu-id="19147-191">**A:** Вы можете обновить сведения на том же веб-сайте, который использовался для запроса подготовки, после завершения подготовки.</span><span class="sxs-lookup"><span data-stu-id="19147-191">**A:** You can update your information at the same web site that you used to request provisioning, after provisioning is complete.</span></span> <span data-ttu-id="19147-192">Введите номер своего соглашения и нажмите кнопку Обновить службу.</span><span class="sxs-lookup"><span data-stu-id="19147-192">Enter your agreement number, and then click Update service.</span></span>

<span data-ttu-id="19147-193"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19147-193"></div>

<span> </span>

</div>

</div>

</span></span></div>
