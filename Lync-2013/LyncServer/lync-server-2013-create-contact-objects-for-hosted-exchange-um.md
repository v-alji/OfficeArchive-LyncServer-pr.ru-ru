---
title: 'Lync Server 2013: создание объектов Contact для размещенной единой системы обмена сообщениями Exchange'
description: 'Lync Server 2013: создание объектов контактов для размещенной единой системы обмена сообщениями Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create contact objects for hosted Exchange UM
ms:assetid: a39be52f-488a-4523-ad5f-ce1f0d681959
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412765(v=OCS.15)
ms:contentKeyID: 48185045
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9760e2a39b5182f9b5194e364e059bddc6a63d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431976"
---
# <a name="create-contact-objects-for-hosted-exchange-um-in-lync-server-2013"></a><span data-ttu-id="1df2e-103">Создание объектов Contact для размещенной единой системы обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1df2e-103">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1df2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1df2e-104">

<span> </span></span></span>

<span data-ttu-id="1df2e-105">_**Тема последнего изменения:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="1df2e-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="1df2e-106">Ниже описана процедура создания объектов контактов для автоматического ассистента (AA) и доступа к абонентам (SA) для единой системы обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="1df2e-106">The following procedure explains how to create Auto Attendant (AA) or Subscriber Access (SA) contact objects for hosted Exchange Unified Messaging (UM).</span></span>

<span data-ttu-id="1df2e-107">Дополнительные сведения можно найти [в разделе Управление объектами контактных данных Exchange в среде Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="1df2e-107">For details, see [Hosted Exchange Contact object management in Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="1df2e-108">Дополнительные сведения о настройке объектов контакта можно найти в документации по оболочке управления Lync Server для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="1df2e-108">For details about configuring contact objects, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="1df2e-109">New-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="1df2e-109">New-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExUmContact)

  - [<span data-ttu-id="1df2e-110">Set-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="1df2e-110">Set-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExUmContact)

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="1df2e-111">Прежде чем можно будет включить объект контакта Lync Server 2013 для размещенной единой системы обмена сообщениями Exchange, необходимо развернуть политику размещенной голосовой почты, которая применяется к ним.</span><span class="sxs-lookup"><span data-stu-id="1df2e-111">Before Lync Server 2013 contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="1df2e-112">Подробнее смотрите в разделе <A href="lync-server-2013-hosted-voice-mail-policies.md">политики размещенной голосовой почты в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1df2e-112">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-aa-or-sa-contact-objects-for-hosted-exchange-um"></a><span data-ttu-id="1df2e-113">Создание объектов контактов AA или SA для размещенной единой системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="1df2e-113">To create AA or SA contact objects for hosted Exchange UM</span></span>

1.  <span data-ttu-id="1df2e-114">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="1df2e-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1df2e-115">Запустите командлет New-CsExUmContact, чтобы создать все объекты контактов, необходимые для вашего развертывания.</span><span class="sxs-lookup"><span data-stu-id="1df2e-115">Run the New-CsExUmContact cmdlet to create any contact objects required for your deployment.</span></span> <span data-ttu-id="1df2e-116">Например, чтобы создать объект AA и контакт SA, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1df2e-116">For example, run the following to create an AA and an SA contact object:</span></span>
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumaa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101" -AutoAttendant $True
       ```
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumsa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101"
       ```
    
    <span data-ttu-id="1df2e-117">В этих примерах устанавливаются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1df2e-117">These examples set the following parameters:</span></span>
    
      - <span data-ttu-id="1df2e-118">**SipAddress** указывает адрес SIP объекта Contact.</span><span class="sxs-lookup"><span data-stu-id="1df2e-118">**SipAddress** specifies the SIP address of the contact object.</span></span> <span data-ttu-id="1df2e-119">Это должен быть адрес, который еще не использовался для настройки объекта пользователя или контакта в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1df2e-119">This must be an address that has not already been used to configure a user or contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="1df2e-120">Это значение должно быть в формате SIP:, \<*SIP address*\> как показано в предыдущих примерах.</span><span class="sxs-lookup"><span data-stu-id="1df2e-120">This value must be in the format “sip:\<*SIP address*\>“ as shown in the previous examples.</span></span>
    
      - <span data-ttu-id="1df2e-121">**RegistrarPool** указывает полное доменное имя (FQDN) пула, на котором запущена служба регистратора.</span><span class="sxs-lookup"><span data-stu-id="1df2e-121">**RegistrarPool** specifies the fully qualified domain name (FQDN) of the pool on which the Registrar service is running.</span></span>
        
        <div class=" ">
        

        > [!NOTE]  
        > <span data-ttu-id="1df2e-122">Объекты контактов Exchange UM нельзя переместить в пулы, которые являются частью развертывания Lync Server 2013 до Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1df2e-122">Exchange UM contact objects cannot be moved to pools that are part of Lync Server 2013 deployments prior to Lync Server 2013.</span></span>

        
        </div>
    
      - <span data-ttu-id="1df2e-123">**OU** . определяет подразделение Active Directory, в котором будет находиться этот объект контакта.</span><span class="sxs-lookup"><span data-stu-id="1df2e-123">**OU** specifies the Active Directory organizational unit where this contact object will be located.</span></span>
    
      - <span data-ttu-id="1df2e-124">**DisplayNumber** указывает телефонный номер объекта контакта.</span><span class="sxs-lookup"><span data-stu-id="1df2e-124">**DisplayNumber** specifies the telephone number of the contact object.</span></span> <span data-ttu-id="1df2e-125">Номер телефона для каждого объекта контакта должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="1df2e-125">The phone number for each contact object must be unique.</span></span>
    
      - <span data-ttu-id="1df2e-126">**Автосекретарь** указывает, является ли объект контакта автосекретарем.</span><span class="sxs-lookup"><span data-stu-id="1df2e-126">**AutoAttendant** specifies whether the Contact object is an Auto Attendant.</span></span> <span data-ttu-id="1df2e-127">Автосекретарь предлагает набор голосовых запросов, которые позволяют вызывающим абонентам перемещаться по телефонной системе и обращаться к ним, к которым нужно обратиться.</span><span class="sxs-lookup"><span data-stu-id="1df2e-127">Auto Attendant provides a set of voice prompts that allow callers to navigate the phone system and reach the party that they want to contact.</span></span> <span data-ttu-id="1df2e-128">Значение **false** (по умолчанию) для этого параметра указывает на объект контакта доступа абонента.</span><span class="sxs-lookup"><span data-stu-id="1df2e-128">A value of **False** (the default) for this parameter indicates a Subscriber Access contact object.</span></span>

<span data-ttu-id="1df2e-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1df2e-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

