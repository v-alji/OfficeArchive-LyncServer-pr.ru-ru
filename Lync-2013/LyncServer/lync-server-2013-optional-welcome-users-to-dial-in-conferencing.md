---
title: 'Lync Server 2013: приветствие пользователей в конференции с телефонным подключением (необязательно)'
description: 'Lync Server 2013: (необязательно) Добро пожаловать пользователям в Конференц-связь с телефонным подключением.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Welcome users to dial-in conferencing
ms:assetid: caa4fd61-f506-4c09-bb5b-1aa260d7a720
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398846(v=OCS.15)
ms:contentKeyID: 48185443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d33c7184a8cf22699b4ebe8d8ea8b4ef1c133a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424844"
---
# <a name="optional-welcome-users-to-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="02b95-103">Приветствие пользователей в конференции с телефонным подключением Lync Server 2013 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="02b95-103">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02b95-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02b95-104">

<span> </span></span></span>

<span data-ttu-id="02b95-105">_**Тема последнего изменения:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="02b95-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="02b95-106">После настройки конференц-связи с телефонным подключением и проверки правильности ее функционирования вы должны задать начальные личные коды (PIN) для пользователей и уведомлять пользователей о доступности функции, включая вводные инструкции, такие как начальный ПИН-код и ссылка на веб-страницу параметров конференции с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="02b95-106">After you configure dial-in conferencing and test to verify that it is functioning properly, you should set initial personal identification numbers (PINs) for users and notify users about the availability of the feature, including introductory instructions such as the initial PIN and the link to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="02b95-107">Этот шаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="02b95-107">This step is optional.</span></span> <span data-ttu-id="02b95-108">Как правило, вы можете сбросить контакты с помощью командлета **Set-CsClientPin** , но если вы хотите отправить приветственное сообщение электронной почты с данными, воспользуйтесь процедурой, описанной в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="02b95-108">Typically, you use the **Set-CsClientPin** cmdlet to reset PINs, but you can use the procedure in this topic the first time if you want to send a welcome email with the information.</span></span> <span data-ttu-id="02b95-109">Если в таком сообщении нет необходимости, следует выполнить командлет **Set-CsClientPin**.</span><span class="sxs-lookup"><span data-stu-id="02b95-109">If you do not want to send the email, you can use **Set-CsClientPin** instead.</span></span>

<span data-ttu-id="02b95-110">Сценарий **Set-CsPinSendCAWelcomeMail** позволяет задать ПИН‑код и отправить приветственное сообщение электронной почты одному пользователю.</span><span class="sxs-lookup"><span data-stu-id="02b95-110">You can use the **Set-CsPinSendCAWelcomeMail** script to set the PIN and send a welcome email to a single user.</span></span> <span data-ttu-id="02b95-111">По умолчанию этот сценарий не сбрасывает ПИН-код, если он уже установлен, но вы можете использовать параметр **Force** для принудительного сброса ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="02b95-111">By default, the script does not reset a PIN if it is already set, but you can use the **Force** parameter to force reset a PIN.</span></span> <span data-ttu-id="02b95-112">Сообщение передается по протоколу SMTP.</span><span class="sxs-lookup"><span data-stu-id="02b95-112">The email message is sent using Simple Mail Transfer Protocol (SMTP).</span></span>

<span data-ttu-id="02b95-113">Можно создать сценарий, предусматривающий многократное выполнение сценариев **Set-CsPinSendCAWelcomeMail** для задания ПИН‑кодов и передачи сообщения электронной почты группе пользователей.</span><span class="sxs-lookup"><span data-stu-id="02b95-113">You can create a script that runs the **Set-CsPinSendCAWelcomeMail** script iteratively to set PINs and send email to a group of users.</span></span> <span data-ttu-id="02b95-114">Вы можете изменить шаблон электронной почты (файл **CAWelcomeEmailTemplate.html** ), чтобы добавить дополнительные ссылки на страницы интрасети или изменить текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="02b95-114">You can modify the email template (that is, the **CAWelcomeEmailTemplate.html** file) to add more links to intranet pages or modify the email text.</span></span>

<div>

## <a name="to-set-an-initial-pin-and-send-welcome-email"></a><span data-ttu-id="02b95-115">Настройка начального ПИН-кода и отправка приветственного сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="02b95-115">To set an initial PIN and send welcome email</span></span>

1.  <span data-ttu-id="02b95-116">Войдите в систему как участник группы RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="02b95-116">Log on as a member of the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="02b95-117">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="02b95-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="02b95-118">Выполните следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="02b95-118">Run the following at the command prompt:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri <user identifier>
        -From <email address of sender> [-Subject <subject for email message>]
        [-UserEmailAddress <destination email address>]
        [-Cc <email address of recipients who receive copy of email>]
        [-Bcc <email address of recipients who receive blind copies>]
        [-TemplatePath <path for email template>]
        [-SmtpServer] <SMTP server name>]
        [-BodyAsPlainText] [-UseSsl]
        [-Pin <new numeric PIN>] [-Force] `
        [-Credential <SMTP server credentials used to send email with the specified From address>]
    
    <span data-ttu-id="02b95-119">**SmtpServer**   По умолчанию сценарий использует значение зарезервированной переменной среды **$PSEmailServer** для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="02b95-119">**SmtpServer**   By default, the script uses the value of the reserved environment variable **$PSEmailServer** for this parameter.</span></span> <span data-ttu-id="02b95-120">Если переменной **$PSEmailServer** не назначено значение, необходимо задать этот параметр вручную.</span><span class="sxs-lookup"><span data-stu-id="02b95-120">If the **$PSEmailServer** variable is not set, you must specify this parameter.</span></span>
    
    <span data-ttu-id="02b95-121">**Учетные данные**   По умолчанию сценарий использует учетные данные текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="02b95-121">**Credential**   By default, the script uses the credentials of the current user.</span></span> <span data-ttu-id="02b95-122">Если текущему пользователю не предоставлено разрешение на передачу сообщений электронной почты с адреса, указанного в поле "От", необходимо задать этот параметр вручную.</span><span class="sxs-lookup"><span data-stu-id="02b95-122">If the current user does not have permission to send email on behalf of the specified From address, you must specify this parameter.</span></span> <span data-ttu-id="02b95-123">Как правило, этот параметр задает пользователь, адрес которого не указан в поле "От".</span><span class="sxs-lookup"><span data-stu-id="02b95-123">As a general rule, specify this parameter if you do not specify your email address as the From address.</span></span>
    
    <span data-ttu-id="02b95-124">Например:</span><span class="sxs-lookup"><span data-stu-id="02b95-124">For example:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri "bob@contoso.com"
        -From "marco@contoso.com"
    
    <span data-ttu-id="02b95-125">В этом примере создается новый ПИН-код, а затем отправляется приветственное сообщение от Marco на Боба.</span><span class="sxs-lookup"><span data-stu-id="02b95-125">This example creates a new PIN and then sends a welcome email from Marco to Bob.</span></span> <span data-ttu-id="02b95-126">Текст формируется на основе шаблона по умолчанию, а сообщение создается в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="02b95-126">It uses the email text from the default template and creates the email message in HTML format.</span></span> <span data-ttu-id="02b95-127">По умолчанию используется тема "Добро пожаловать в Конференц-связь".</span><span class="sxs-lookup"><span data-stu-id="02b95-127">The default Subject is "Welcome to Dial In Conferencing".</span></span>
    
    <span data-ttu-id="02b95-128">Еще один пример:</span><span class="sxs-lookup"><span data-stu-id="02b95-128">Another example:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri "bob@contoso.com"
        -From "marco@contoso.com" -Subject "Your new dial-in conferencing PIN"
        -Pin "383042650" -Force
        -Credential Admin@contoso.com -UseSsl
    
    <span data-ttu-id="02b95-129">В этом примере в качестве нового ПИН-кода принудительно задается значение "383042650" для Боба, несмотря на то, что Боб имел существующий ПИН-код, а затем отправляет приветственное сообщение от Marco на Боба.</span><span class="sxs-lookup"><span data-stu-id="02b95-129">This example forces a new PIN with a value of "383042650" for Bob, even though Bob had an existing PIN, and then sends a welcome email from Marco to Bob.</span></span> <span data-ttu-id="02b95-130">Поскольку задан параметр Credential, пользователю, выполняющему команду, предлагается ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="02b95-130">Because the Credential parameter is specified, the person running the command is prompted to enter a password.</span></span> <span data-ttu-id="02b95-131">Сообщение электронной почты отправляется с использованием протокола SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="02b95-131">The email is sent by using the Secure Sockets Layer (SSL).</span></span>

<span data-ttu-id="02b95-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02b95-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

