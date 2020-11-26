---
title: 'Lync Server 2013: изменение существующей политики для ПИН-кода'
description: 'Lync Server 2013: изменение существующей политики для ПИН-кода.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify an existing PIN policy
ms:assetid: 517caaee-3349-4fa6-8d86-e4da3258a445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520993(v=OCS.15)
ms:contentKeyID: 48184143
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec67b2ff4cae02ef54a0d37d80ce55c53a9b8a5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445773"
---
# <a name="modify-an-existing-pin-policy-in-lync-server-2013"></a><span data-ttu-id="3e0da-103">Изменение существующей политики ПИН-кода в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e0da-103">Modify an existing PIN policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e0da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e0da-104">

<span> </span></span></span>

<span data-ttu-id="3e0da-105">_**Тема последнего изменения:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="3e0da-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="3e0da-106">С помощью вкладки " **политика закрепления** " вы можете предоставить персональный идентификационный номер (ПИН-код) пользователям, которые подключаются к Lync 2013 с IP-телефонами.</span><span class="sxs-lookup"><span data-stu-id="3e0da-106">You can use the **PIN Policy** tab to provide personal identification number (PIN) authentication to users who are connecting to Lync 2013 with IP Phones.</span></span> <span data-ttu-id="3e0da-107">Чтобы использовать проверку подлинности по ПИН-коду, необходимо установить флажок **Разрешить проверку подлинности на основе ПИН-кода** в настройках веб-службы.</span><span class="sxs-lookup"><span data-stu-id="3e0da-107">To use PIN authentication, make sure that **Enable PIN Authentication** is selected in Web Service settings.</span></span> <span data-ttu-id="3e0da-108">Дополнительные сведения можно найти [в разделе изменение существующих параметров конфигурации веб-службы в Lync Server 2013](lync-server-2013-modify-existing-web-service-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3e0da-108">For details, see [Modify existing Web Service configuration settings in Lync Server 2013](lync-server-2013-modify-existing-web-service-configuration-settings.md).</span></span>

<span data-ttu-id="3e0da-109">Выполните следующие действия, чтобы изменить политику ПИН-кода на уровне пользователя или узла.</span><span class="sxs-lookup"><span data-stu-id="3e0da-109">Follow these steps to modify a user-level or a site-level PIN policy.</span></span>

<div>

## <a name="to-modify-an-existing-pin-policy"></a><span data-ttu-id="3e0da-110">Изменение существующей политики ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="3e0da-110">To modify an existing PIN policy</span></span>

1.  <span data-ttu-id="3e0da-111">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3e0da-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="3e0da-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3e0da-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3e0da-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3e0da-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3e0da-114">В левой панели навигации последовательно выберите пункты **Безопасность** и **Политика ПИН-кода**.</span><span class="sxs-lookup"><span data-stu-id="3e0da-114">In the left navigation bar, click **Security** and then click **PIN Policy**.</span></span>

4.  <span data-ttu-id="3e0da-115">На странице **Политика в отношении ПИН-кодов** выберите политику, нажмите кнопку **Изменить**, а затем щелкните **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="3e0da-115">On the **PIN Policy** page, click a policy, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="3e0da-p103">В окне **Изменение политики ПИН-кода** введите или выберите в поле **Минимальная длина ПИН-кода** минимальную длину ПИН-кода. Минимальная длина по умолчанию составляет пять цифр.</span><span class="sxs-lookup"><span data-stu-id="3e0da-p103">In **Edit PIN Policy**, in **Minimum PIN length**, type or select the minimum PIN length that you want to allow. The default minimum length is five digits.</span></span>

6.  <span data-ttu-id="3e0da-p104">Чтобы иметь возможность задать максимальное число попыток входа перед блокированием пользователя, установите флажок **Задать максимальное число попыток входа**. Если этот параметр не выбран, максимальное число разрешенных попыток входа автоматически определяется в зависимости от длины ПИН-кода. По умолчанию максимальное число попыток определяется автоматически.</span><span class="sxs-lookup"><span data-stu-id="3e0da-p104">To be able to specify the maximum number of logon attempts before a user is locked out, select the **Specify maximum logon attempts** check box. If you do not select this option, the maximum number of allowed attempts is automatically determined based on the PIN length. By default, the maximum number of attempts is automatically determined.</span></span>

7.  <span data-ttu-id="3e0da-121">Если установлен флажок **Задать максимальное число попыток входа**, в поле **Максимальное число попыток входа** введите или выберите максимальное число попыток входа, которое требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="3e0da-121">If you selected the **Specify maximum logon attempts** check box, in **Maximum logon attempts**, type or select the maximum number of logon attempts that you want to allow.</span></span>

8.  <span data-ttu-id="3e0da-p105">Чтобы ПИН-коды имели конечный срок действия, установите флажок **Включить конечный срок действия ПИН-кодов**. Если этот параметр не выбран, ПИН-коды не будут иметь ограничений по сроку действия. По умолчанию ПИН-коды не имеют ограничений по сроку действия.</span><span class="sxs-lookup"><span data-stu-id="3e0da-p105">To have PINs expire, select the **Enable PIN expiration** check box. If you do not select this option, PINs will never expire. By default, PINs never expire.</span></span>

9.  <span data-ttu-id="3e0da-125">Если флажок **Разрешить окончание срока действия ПИН-кода** установлен, то в поле **Срок действия ПИН-кода истекает после (дней)** введите или выберите максимальное число дней, после которых ПИН-коды становятся недействительными.</span><span class="sxs-lookup"><span data-stu-id="3e0da-125">If you selected the **Enable PIN expiration** check box, in **PIN expires after (days)**, type or select the number of days after which PINs expire.</span></span>

10. <span data-ttu-id="3e0da-p106">В поле **История значений ПИН-кода** введите число ПИН-кодов, которое пользователь должен создать перед тем, как он сможет использовать их повторно. По умолчанию пользователи могут повторно использовать ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="3e0da-p106">In **PIN history count**, type the number of PINs that a user must create before the user can reuse a PIN. By default, users can reuse their PINs.</span></span>

11. <span data-ttu-id="3e0da-p107">Чтобы разрешить распространенные последовательности цифр в ПИН-кодах, такие как последовательные номера и повторяющиеся наборы номеров, установите флажок **Разрешить общие шаблоны**. Если не выбрать этот параметр, будут разрешены только сложные наборы цифр. По умолчанию разрешены только сложные наборы цифр.</span><span class="sxs-lookup"><span data-stu-id="3e0da-p107">To allow common patterns of digits in PINs, such as sequential numbers and repetitive sets of numbers, select the **Allow common patterns** check box. If you do not select this option, only complex patterns of digits are allowed. By default, only complex patterns of digits are allowed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3e0da-131">Мы рекомендуем не разрешать использование распространенных последовательностей.</span><span class="sxs-lookup"><span data-stu-id="3e0da-131">We recommend that you do not allow common patterns.</span></span>

    
    </div>

12. <span data-ttu-id="3e0da-132">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="3e0da-132">Click **Commit**.</span></span>

<span data-ttu-id="3e0da-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e0da-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

