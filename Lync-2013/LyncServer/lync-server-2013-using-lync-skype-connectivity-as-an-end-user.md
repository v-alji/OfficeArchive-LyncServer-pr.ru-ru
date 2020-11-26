---
title: 'Lync Server 2013: Взаимодействие между конечными пользователями Lync и Skype'
description: 'Lync Server 2013: использование Lync-Skype подключения в качестве конечного пользователя.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Lync-Skype connectivity as an end user
ms:assetid: ad22f731-118c-4349-8790-b1a72941cbdd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440175(v=OCS.15)
ms:contentKeyID: 57793365
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd669a5cf0b15f7fb2d411e4456553f5469d9f96
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438920"
---
# <a name="using-lync-skype-connectivity-in-lync-server-2013-as-an-end-user"></a><span data-ttu-id="c506c-103">Взаимодействие между конечными пользователями Lync и Skype в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c506c-103">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c506c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c506c-104">

<span> </span></span></span>

<span data-ttu-id="c506c-105">_**Тема последнего изменения:** 2016-12-27_</span><span class="sxs-lookup"><span data-stu-id="c506c-105">_**Topic Last Modified:** 2016-12-27_</span></span>

<span data-ttu-id="c506c-106">Возможность подключения к Lync-Skype позволяет пользователям Skype и пользователям Lync добавлять друг друга в список контактов, обмениваться мгновенными сообщениями, а также выполнять голосовые и видеозвонки.</span><span class="sxs-lookup"><span data-stu-id="c506c-106">Lync-Skype Connectivity enables Skype users and Lync users to add each other as contacts, exchange instant messages and make audio and video calls.</span></span> <span data-ttu-id="c506c-107">Когда пользователь Skype добавляет пользователя Lync, пользователь Skype создаст контакт в Skype, содержащий универсальный код ресурса (SIP) для пользователя Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-107">When a Skype user adds a Lync user, a Skype user will create a contact in Skype containing the session initiation protocol (SIP) uniform resource identifier (URI) of the Lync user.</span></span> <span data-ttu-id="c506c-108">И наоборот, когда пользователь Lync добавляет контакт Skype, пользователь Lync создаст в Lync контакт, который будет содержать учетную запись Майкрософт (MSA) пользователя Skype, а не имя пользователя Skype.</span><span class="sxs-lookup"><span data-stu-id="c506c-108">Conversely, when a Lync user adds a Skype contact, the Lync user will create a contact in Lync that will contain the Microsoft Account (MSA) of the Skype user, and not the Skype user name.</span></span>

<span data-ttu-id="c506c-109">**Что такое MSA?**</span><span class="sxs-lookup"><span data-stu-id="c506c-109">**What is an MSA?**</span></span> <span data-ttu-id="c506c-110">Чтобы общаться с контактами Lync, пользователи Skype должны войти в Skype с помощью учетной записи Майкрософт (ранее — Windows Live ID).</span><span class="sxs-lookup"><span data-stu-id="c506c-110">Skype users must sign in to Skype with a Microsoft account (previously called Windows Live ID) in order to communicate with Lync contacts.</span></span> <span data-ttu-id="c506c-111">Учетная запись Майкрософт состоит из комбинации адреса электронной почты и пароля, который можно также использовать для входа в такие службы, как Microsoft OneDrive, Windows Phone, служба игрового приложения Microsoft Outlook и клиент сообщений и совместной работы (и, ранее, веб-службы электронной почты Microsoft Hotmail или Windows Live Messenger).</span><span class="sxs-lookup"><span data-stu-id="c506c-111">A Microsoft account consists of the combination of an email address and a password, which you can also use to sign in to services such as Microsoft OneDrive storage technology, Windows Phone, Microsoft Xbox LIVE online game service, and Microsoft Outlook messaging and collaboration client (and, previously, Microsoft Hotmail web-based e-mail service or Windows Live Messenger).</span></span> <span data-ttu-id="c506c-112">Если вы используете адрес электронной почты и пароль для входа в эти или другие службы, у вас уже есть учетная запись Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c506c-112">If you use an email address and a password to sign in to these or other services, you already have a Microsoft account.</span></span> <span data-ttu-id="c506c-113">Дополнительные сведения о создании учетной записи Майкрософт можно найти на странице Регистрация в учетной записи Майкрософт [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061) .</span><span class="sxs-lookup"><span data-stu-id="c506c-113">For details about creating a Microsoft Account, see the Microsoft account sign-up page at [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061).</span></span> <span data-ttu-id="c506c-114">Вы можете объединить существующую учетную запись Skype с учетной записью Майкрософт для единого входа в систему в различных приложениях и службах.</span><span class="sxs-lookup"><span data-stu-id="c506c-114">You can merge your existing Skype account with your Microsoft account for single sign-on, across a variety of applications and services.</span></span> <span data-ttu-id="c506c-115">После того как учетная запись будет объединена, пользователь Skype сможет отправлять запросы на контакт пользователям Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-115">Once the account is merged a Skype user can send a contact request to Lync users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c506c-116">Для того чтобы пользователи Lync и Skype могли полностью взаимодействовать друг с другом, должны быть выполнены следующие требования:</span><span class="sxs-lookup"><span data-stu-id="c506c-116">In order for Lync and Skype users to fully communicate with each other, the following requirements must be met:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="c506c-117">Пользователи Skype должны войти в систему своего клиента Skype с помощью учетной записи Майкрософт (MSA).</span><span class="sxs-lookup"><span data-stu-id="c506c-117">Skype users must be logged into their Skype client with a Microsoft Account (MSA).</span></span></P>
> <LI>
> <P><span data-ttu-id="c506c-118">Пользователи Lync должны быть включены для доступа к общедоступному мгновенному тексту с помощью своего администратора Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-118">Lync users must be enabled for public IM connectivity by their Lync administrator.</span></span></P>
> <LI>
> <P><span data-ttu-id="c506c-119">Когда пользователь Skype добавляет контакт Lync, проверьте, отображается ли слово Lync под именем контакта.</span><span class="sxs-lookup"><span data-stu-id="c506c-119">When a Skype user adds a Lync contact, verify that the word Lync appears below the contact’s name.</span></span> <span data-ttu-id="c506c-120">Это указывает на то, что URI Lync найден.</span><span class="sxs-lookup"><span data-stu-id="c506c-120">This indicates that a Lync URI has been found.</span></span></P>
> <LI>
> <P><span data-ttu-id="c506c-121">Когда пользователь Skype добавляет контакт Lync и возвращаются нулевые результаты поиска для этого домена Lync, процесс подготовки PIC может не завершиться, либо домен Lync еще не настроен.</span><span class="sxs-lookup"><span data-stu-id="c506c-121">When a Skype user adds a Lync contact and zero search results are returned for that Lync domain, the PIC provisioning process may not have completed, or the Lync domain has not yet been set up.</span></span></P>
> <LI>
> <P><span data-ttu-id="c506c-122">В зависимости от параметров конфиденциальности пользователей Lync и Skype, Обмен мгновенными сообщениями, видео и присутствие может быть недоступен, пока новые контакты не будут приниматься каждым пользователем.</span><span class="sxs-lookup"><span data-stu-id="c506c-122">Depending on the privacy settings of the Lync and Skype users, IM, video, and presence may not work until the new contacts are accepted by each user.</span></span></P></LI></UL>



</div>

<span data-ttu-id="c506c-123">**Добавление контакта Skype в Lync 2013**</span><span class="sxs-lookup"><span data-stu-id="c506c-123">**To add a Skype contact to Lync 2013**</span></span>

1.  <span data-ttu-id="c506c-124">В Lync нажмите кнопку " **Добавить контакт", чтобы добавить контакт не из моей организации**.</span><span class="sxs-lookup"><span data-stu-id="c506c-124">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="c506c-125">В списке доступных поставщиков контактов выберите пункт **Skype**.</span><span class="sxs-lookup"><span data-stu-id="c506c-125">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="c506c-126">В поле **адрес для обмена мгновенными сообщениями** введите учетную запись Майкрософт (MSA) пользователя Skype.</span><span class="sxs-lookup"><span data-stu-id="c506c-126">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user.</span></span>

4.  <span data-ttu-id="c506c-127">В раскрывающемся списке **Добавить в группу контактов** выберите группу контактов, в которую нужно добавить пользователя.</span><span class="sxs-lookup"><span data-stu-id="c506c-127">In the **Add to contact group** dropdown box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="c506c-128">В раскрывающемся списке **настроить отношение к конфиденциальности** выберите соответствующий параметр контакта и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c506c-128">In the **Set privacy relationship** dropdown box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="c506c-129">Теперь пользователь появится в Lync как контакт.</span><span class="sxs-lookup"><span data-stu-id="c506c-129">The user will now appear as a contact in Lync.</span></span> <span data-ttu-id="c506c-130">Выберите пользователя, щелкните правой кнопкой мыши имя пользователя и выберите команду **просмотреть карточку контакта** , чтобы просмотреть свойства пользователя.</span><span class="sxs-lookup"><span data-stu-id="c506c-130">Select the user, right-click the user name, and click **See Contact Card** to view the user properties.</span></span> <span data-ttu-id="c506c-131">Теперь вы можете создать звуковой или видеозвонок с новым пользователем Skype.</span><span class="sxs-lookup"><span data-stu-id="c506c-131">You can now establish an audio or video call with the newly added Skype user.</span></span>

<span data-ttu-id="c506c-132">Дополнительные сведения о поддержке контактов можно найти в разделе [Добавление контакта в Lync](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a).</span><span class="sxs-lookup"><span data-stu-id="c506c-132">For additional information on support for contacts, see [Add a contact in Lync](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a).</span></span>

<span data-ttu-id="c506c-133">Если учетная запись Майкрософт пользователя Skype использует собственное доменное имя, например <strong>Bob@contoso.com</strong> , пользователь Lync может добавить эту учетную запись Майкрософт в Lync двумя способами:</span><span class="sxs-lookup"><span data-stu-id="c506c-133">When a Skype user’s Microsoft account uses a custom domain name, such as <strong>bob@contoso.com</strong> , a Lync user can add that Microsoft account to Lync in two ways:</span></span>

1.  <span data-ttu-id="c506c-134">С помощью значка **Добавить контакт** или</span><span class="sxs-lookup"><span data-stu-id="c506c-134">Use the **Add a Contact** icon, or</span></span>

2.  <span data-ttu-id="c506c-135">Используйте поле **найти человека или комнату или набрать номер** .</span><span class="sxs-lookup"><span data-stu-id="c506c-135">Use the **Find someone or a room, or a dial a number** field.</span></span>

<span data-ttu-id="c506c-136">В каждом экземпляре пользователь Lync должен ввести адрес электронной почты пользователя Skype в следующем формате: <strong>User (доменное имя) @msn. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="c506c-136">In each instance, the Lync user must enter the Skype user’s email in the following format: <strong>user(domain name)@msn.com</strong> .</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c506c-137">Это действие не требуется для учетных записей Майкрософт, в которых используются следующие доменные имена: <STRONG>@live. com, @hotmail. com или @outlook. com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c506c-137">This step is not required for Microsoft accounts that use the following domain names: <STRONG>@live.com, @hotmail.com or @outlook.com</STRONG>.</span></span> <span data-ttu-id="c506c-138">Дополнительные сведения о поддерживаемых доменных именах см. в разделе <A href="https://support.microsoft.com/kb/897567">Поддерживаемые общедоступные домены обмена мгновенными сообщениями</A>.</span><span class="sxs-lookup"><span data-stu-id="c506c-138">For more information on supported custom domain names, see <A href="https://support.microsoft.com/kb/897567">Supported public IM domains</A>.</span></span>



</div>

<span data-ttu-id="c506c-139">**Добавление контакта Skype в Lync при использовании собственного имени домена**</span><span class="sxs-lookup"><span data-stu-id="c506c-139">**To add a Skype contact to Lync when using a custom domain name**</span></span>

1.  <span data-ttu-id="c506c-140">В Lync нажмите кнопку " **Добавить контакт", чтобы добавить контакт не из моей организации**.</span><span class="sxs-lookup"><span data-stu-id="c506c-140">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="c506c-141">В списке доступных поставщиков контактов выберите пункт **Skype**.</span><span class="sxs-lookup"><span data-stu-id="c506c-141">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="c506c-142">В поле **адрес для обмена мгновенными сообщениями** введите учетную запись Майкрософт (MSA) пользователя Skype в формате <strong>User (доменное имя) @msn. com</strong>.</span><span class="sxs-lookup"><span data-stu-id="c506c-142">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user in the format <strong>user(domain name)@msn.com</strong>.</span></span> <span data-ttu-id="c506c-143">Итак, для пользователя bob@contoso.com будет введено значение <strong> Bob (contoso. com) @msn. com <strong> .</span><span class="sxs-lookup"><span data-stu-id="c506c-143">So for user bob@contoso.com, the entry would be <strong>bob(contoso.com)@msn.com<strong> .</span></span>

4.  <span data-ttu-id="c506c-144">В раскрывающемся списке **Добавить в группу контактов** выберите группу контактов, в которую нужно добавить пользователя.</span><span class="sxs-lookup"><span data-stu-id="c506c-144">In the **Add to contact group** drop-down list box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="c506c-145">В раскрывающемся списке **задать уровень конфиденциальности** выберите соответствующий параметр контакта и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c506c-145">In the **Set privacy relationship** drop-down list box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="c506c-146">Пользователь Lync также может использовать поле **найти человека или комнату или набрать номер** в Lync и добавить адрес, похожий на приведенный ниже <strong>пользователь (доменное имя) @msn. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="c506c-146">A Lync user can also use the **Find someone or a room, or dial a number** field in Lync, and add an address that resembles the following <strong>user(domain name)@msn.com</strong> .</span></span> <span data-ttu-id="c506c-147">Итак, для учетной записи Microsoft bob@contoso.com элемент будет представлять <strong>Бобу (contoso. com) @msn. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="c506c-147">So for the bob@contoso.com Microsoft account, the entry would be <strong>bob(contoso.com)@msn.com</strong> .</span></span>

7.  <span data-ttu-id="c506c-148">Выполните действия 4 и 5, описанные выше, чтобы добавить контакт в группу контактов и выбрать подходящее отношение конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="c506c-148">Follow steps 4 and 5 earlier in this procedure to add the contact to a contact group and to select the appropriate privacy relationship.</span></span>

<span data-ttu-id="c506c-149">**Добавление контакта Lync в Skype**</span><span class="sxs-lookup"><span data-stu-id="c506c-149">**To add a Lync contact to Skype**</span></span>

1.  <span data-ttu-id="c506c-150">Войдите в Skype.</span><span class="sxs-lookup"><span data-stu-id="c506c-150">Sign in to Skype.</span></span> <span data-ttu-id="c506c-151">Пользователь Skype должен войти в Skype с помощью учетной записи Майкрософт (MSA).</span><span class="sxs-lookup"><span data-stu-id="c506c-151">The Skype user must be logged into their Skype client with a Microsoft Account (MSA).</span></span>

2.  <span data-ttu-id="c506c-152">Щелкните значок Добавить контакты.</span><span class="sxs-lookup"><span data-stu-id="c506c-152">Select the Add Contacts icon.</span></span>

3.  <span data-ttu-id="c506c-153">Введите URI SIP для пользователя Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-153">Enter the SIP URI of the Lync user.</span></span> <span data-ttu-id="c506c-154">Например, bob@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c506c-154">For example, bob@contoso.com.</span></span>

4.  <span data-ttu-id="c506c-155">Если в результатах поиска найдено совпадение, найдите в списке слово **Lync** под именем пользователя Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-155">When Skype finds the match in the search results, look for the word **Lync** below the Lync user’s name.</span></span> <span data-ttu-id="c506c-156">Это указывает на то, что Skype успешно размещает URI SIP клиента Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-156">This indicates Skype successfully located the Lync client’s SIP URI.</span></span> <span data-ttu-id="c506c-157">Щелкните имя.</span><span class="sxs-lookup"><span data-stu-id="c506c-157">Click the name.</span></span>

5.  <span data-ttu-id="c506c-158">В правом верхнем углу окна нажмите кнопку Добавить в контакты.</span><span class="sxs-lookup"><span data-stu-id="c506c-158">In the top right corner of the window, click Add to Contacts.</span></span>

6.  <span data-ttu-id="c506c-159">Новый контакт будет добавлен в список контактов, но вы увидите вопросительный знак вместо значка состояния, пока он не примет ваш запрос.</span><span class="sxs-lookup"><span data-stu-id="c506c-159">The new contact is now added to your contact list, but you’ll see a question mark instead of their status icon until they accept your request.</span></span> <span data-ttu-id="c506c-160">Когда новый контакт примет ваш запрос, вы сможете видеть, когда он находится в сети, инициировать текстовые беседы, а также выполнять голосовые и видеозвонки.</span><span class="sxs-lookup"><span data-stu-id="c506c-160">When your new contact accepts your request, you will be able to see when they are online, initiate IM conversations, and make audio and video calls.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c506c-161">Администратор Lync Server должен настроить параметры политики пользователя Lync, чтобы разрешить входящие запросы.</span><span class="sxs-lookup"><span data-stu-id="c506c-161">The Lync Server administrator must configure the Lync user’s policy settings to allow incoming requests.</span></span> <span data-ttu-id="c506c-162">В противном случае пользователь Lync не будет получать запросы контактных лиц от пользователя Skype.</span><span class="sxs-lookup"><span data-stu-id="c506c-162">If not, the Lync user will not receive contact requests from the Skype user.</span></span> <span data-ttu-id="c506c-163">В зависимости от настройки параметров политики пользователя Lync запрос на добавление пользователя Skype появится на вкладке " <STRONG>создать</STRONG> " клиента Lync. Чтобы начать общение с пользователем Skype, пользователь Lync должен добавить пользователя Skype в список "Избранное" или список контактов.</span><span class="sxs-lookup"><span data-stu-id="c506c-163">Depending on the configuration of the Lync user’s policy settings, the request to add the Skype user will appear on the Lync client’s <STRONG>New</STRONG> tab. To begin communicating with the Skype user, the Lync user must add the Skype user to either the Favorites list or a contact list.</span></span> <span data-ttu-id="c506c-164">На рисунке ниже показано расположение <STRONG>новой</STRONG> вкладки в клиенте Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-164">The image below shows the location of the <STRONG>New</STRONG> tab in the Lync client.</span></span>

    
    </div>

<span data-ttu-id="c506c-165">Пользователи Lync должны настроить оповещения Lync, чтобы убедиться, что запросы, отправленные от пользователя Skype, появятся и могут быть обнаружены пользователем Lync.</span><span class="sxs-lookup"><span data-stu-id="c506c-165">A Lync user must configure Lync alerts to ensure that requests sent from a Skype user appear and are discoverable by the Lync user.</span></span> <span data-ttu-id="c506c-166">Чтобы настроить оповещения Lync, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c506c-166">To configure Lync alerts, complete the procedure that follows.</span></span>

<span data-ttu-id="c506c-167">**Настройка оповещений Lync**</span><span class="sxs-lookup"><span data-stu-id="c506c-167">**To configure Lync Alerts**</span></span>

1.  <span data-ttu-id="c506c-168">В клиенте Lync щелкните значок " **Параметры** ".</span><span class="sxs-lookup"><span data-stu-id="c506c-168">From the Lync client, click the **Options** icon.</span></span>

2.  <span data-ttu-id="c506c-169">Выберите **оповещения**.</span><span class="sxs-lookup"><span data-stu-id="c506c-169">Select **Alerts**.</span></span>

3.  <span data-ttu-id="c506c-170">В разделе **Общие оповещения** установите флажок **уведомлять, когда кто-то добавляет меня в свой список контактов**.</span><span class="sxs-lookup"><span data-stu-id="c506c-170">Under **General alerts**, check **Tell me when someone adds me to his or her contact list**.</span></span>

4.  <span data-ttu-id="c506c-171">В разделе **Контакты, не использующие Lync**, выберите **Разрешить приглашения, но блокировать все прочие сообщения**.</span><span class="sxs-lookup"><span data-stu-id="c506c-171">Under **Contacts not using Lync**, select **Allow invites but block all other communications**.</span></span>

5.  <span data-ttu-id="c506c-172">Нажмите кнопку **ОК** , чтобы закрыть окно "Параметры".</span><span class="sxs-lookup"><span data-stu-id="c506c-172">Click **OK** to close the Options window.</span></span>

<span data-ttu-id="c506c-173"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c506c-173"></div>

<span> </span>

</div>

</div>

</span></span></div>

