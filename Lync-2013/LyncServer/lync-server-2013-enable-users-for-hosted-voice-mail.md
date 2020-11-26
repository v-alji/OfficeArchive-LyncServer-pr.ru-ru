---
title: 'Lync Server 2013: включение поддержки размещаемой голосовой почты для пользователей'
description: 'Lync Server 2013: включение пользователей для размещенной голосовой почты.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for hosted voice mail
ms:assetid: fa559f8f-ef99-43a1-b580-9e998b95efb8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413062(v=OCS.15)
ms:contentKeyID: 48185919
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3853a70d433c09029a02f2ca6256b5988defdcb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437471"
---
# <a name="enable-users-for-hosted-voice-mail-in-lync-server-2013"></a><span data-ttu-id="36ce9-103">Включение поддержки размещаемой голосовой почты для пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36ce9-103">Enable users for hosted voice mail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36ce9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36ce9-104">

<span> </span></span></span>

<span data-ttu-id="36ce9-105">_**Тема последнего изменения:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="36ce9-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="36ce9-106">Следуйте инструкциям, чтобы включить пользователей Lync Server 2013 для голосовой почты в размещенной службе единой системы обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="36ce9-106">Follow the procedure to enable Lync Server 2013 users for voice mail on a hosted Exchange Unified Messaging (UM) service.</span></span>

<span data-ttu-id="36ce9-107">Дополнительные сведения можно найти [в разделе Управление пользователями Exchange в среде Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="36ce9-107">For details, see [Hosted Exchange user management in Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="36ce9-108">Дополнительные сведения о командлете [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) можно найти в документации по оболочке Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="36ce9-108">For details about the [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="36ce9-109">Прежде чем пользователи Lync Server 2013 могут быть включены для поддержки размещенной голосовой почты, необходимо развернуть политику размещенной голосовой почты, которая применяется к учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="36ce9-109">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to their user account must be deployed.</span></span> <span data-ttu-id="36ce9-110">Подробнее смотрите в разделе <A href="lync-server-2013-hosted-voice-mail-policies.md">политики размещенной голосовой почты в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="36ce9-110">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-users-for-hosted-voice-mail"></a><span data-ttu-id="36ce9-111">Предоставление пользователям размещенной голосовой почты</span><span class="sxs-lookup"><span data-stu-id="36ce9-111">To enable users for hosted voice mail</span></span>

1.  <span data-ttu-id="36ce9-112">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="36ce9-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="36ce9-113">Запустите командлет Set-CsUser, чтобы настроить учетную запись пользователя для размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="36ce9-113">Run the Set-CsUser cmdlet to configure the user account for hosted voice mail.</span></span> <span data-ttu-id="36ce9-114">Например, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="36ce9-114">For example, run:</span></span>
    
        Set-CsUser -HostedVoiceMail $True -Identity "contoso\kenmyer"
    
    <span data-ttu-id="36ce9-115">Команда в предыдущем примере задает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="36ce9-115">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="36ce9-116">**HostedVoiceMail** позволяет перенаправлять голосовую почту пользователя на размещенную в единой системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="36ce9-116">**HostedVoiceMail** enables a user’s voice mail calls to be routed to hosted Exchange UM.</span></span> <span data-ttu-id="36ce9-117">Она также сообщает Microsoft Lync 2013 о том, что у вас есть индикатор "позвонить голосовой почте".</span><span class="sxs-lookup"><span data-stu-id="36ce9-117">It also signals Microsoft Lync 2013 to light up the “call voice mail” indicator.</span></span>
    
      - <span data-ttu-id="36ce9-118">**Identity** указывает учетную запись пользователя, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="36ce9-118">**Identity** specifies the user account to be modified.</span></span> <span data-ttu-id="36ce9-119">Значение идентификатора можно задать в одном из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="36ce9-119">The Identity value can be specified using any of the following formats:</span></span>
        
          - <span data-ttu-id="36ce9-120">Адрес SIP пользователя</span><span class="sxs-lookup"><span data-stu-id="36ce9-120">The user's SIP address</span></span>
        
          - <span data-ttu-id="36ce9-121">Имя субъекта-пользователя в службе каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="36ce9-121">The user's Active Directory User-Principal-Name</span></span>
        
          - <span data-ttu-id="36ce9-122">Доменное имя пользователя \\ (например, Contoso \\ kenmyer).</span><span class="sxs-lookup"><span data-stu-id="36ce9-122">The user's domain\\logon name (for example, contoso\\kenmyer)</span></span>
        
          - <span data-ttu-id="36ce9-123">Display-Name доменных служб Active Directory пользователя (например, Кен Myer).</span><span class="sxs-lookup"><span data-stu-id="36ce9-123">The user's Active Directory Domain Services Display-Name (for example, Ken Myer).</span></span> <span data-ttu-id="36ce9-124">Если в качестве значения идентификатора используется Display-Name, можно использовать подстановочный знак "звездочка" ( \* ).</span><span class="sxs-lookup"><span data-stu-id="36ce9-124">If using the Display-Name as the Identity value, you can use the asterisk (\*) wildcard character.</span></span> <span data-ttu-id="36ce9-125">Например, идентификатор " \* Кузнецов" возвращает всех пользователей, у которых есть Display-Name, который заканчивается строковым значением Смит.</span><span class="sxs-lookup"><span data-stu-id="36ce9-125">For example, the Identity "\* Smith" returns all the users who have a Display-Name that ends with the string value "Smith".</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="36ce9-126">Имя учетной записи SAM в Active Directory не может использоваться в качестве значения удостоверения, так как имя SAM-Account-Name не обязательно должно быть уникальным в лесу.</span><span class="sxs-lookup"><span data-stu-id="36ce9-126">The user’s Active Directory SAM-Account-Name cannot be used as the Identity value because the SAM-Account-Name is not necessarily unique in the forest.</span></span>

        
        <span data-ttu-id="36ce9-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36ce9-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

