---
title: 'Lync Server 2013: Настройка параметров безопасности для Lync Phone Edition'
description: 'Lync Server 2013: Настройка параметров безопасности для Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure security settings for Lync Phone Edition
ms:assetid: 6e7cec17-8a79-4428-9300-8821256c46cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521014(v=OCS.15)
ms:contentKeyID: 48184464
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82e6a6488db66a8497930ee6b2d1aec6fc8b0b2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433768"
---
# <a name="configure-security-settings-for-lync-phone-edition-in-lync-server-2013"></a><span data-ttu-id="21042-103">Настройка параметров безопасности для Lync Phone Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21042-103">Configure security settings for Lync Phone Edition in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21042-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21042-104">

<span> </span></span></span>

<span data-ttu-id="21042-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="21042-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="21042-106">Улучшите безопасность устройств с Lync Phone Edition, используя настройки безопасности SIP и параметры блокировки телефона.</span><span class="sxs-lookup"><span data-stu-id="21042-106">Help improve the security of devices running Lync Phone Edition via your SIP security setting and phone lock settings.</span></span>

<div>

## <a name="to-configure-security-settings-for-lync-phone-edition"></a><span data-ttu-id="21042-107">Настройка параметров безопасности для Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="21042-107">To configure security settings for Lync Phone Edition</span></span>

1.  <span data-ttu-id="21042-108">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="21042-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="21042-109">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="21042-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="21042-110">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="21042-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="21042-111">На панели навигации слева выберите пункт **Клиенты**, а затем — **Конфигурация устройства**.</span><span class="sxs-lookup"><span data-stu-id="21042-111">In the left navigation bar, click **Clients**, and then click **Device Configuration**.</span></span>

4.  <span data-ttu-id="21042-112">На странице **Конфигурация устройства** в списке конфигураций устройств дважды щелкните конфигурацию, для которой вы хотите изменить параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="21042-112">On the **Device Configuration** page, in the list of device configurations, double-click the configuration for which you want to change security settings.</span></span>

5.  <span data-ttu-id="21042-113">В разделе **изменение конфигурации устройства** в **системе безопасности SIP** укажите уровень безопасности SIP.</span><span class="sxs-lookup"><span data-stu-id="21042-113">In **Edit Device Configuration**, in **SIP security**, specify the SIP security level.</span></span> <span data-ttu-id="21042-114">Уровень по умолчанию — **High**, поэтому мы рекомендуем использовать.</span><span class="sxs-lookup"><span data-stu-id="21042-114">The default level is **High**, which we recommend using.</span></span>

6.  <span data-ttu-id="21042-115">В диалоговом окне **изменение конфигурации устройства** в разделе **Блокировка телефона** установите или снимите флажок **Принудительная Блокировка устройства** (выбрано по умолчанию) и укажите минимальную длину PIN-кода (по умолчанию) и период ожидания (по умолчанию — по 5 минутам).</span><span class="sxs-lookup"><span data-stu-id="21042-115">In **Edit Device Configuration**, under **Phone Lock**, select or clear the **Enforce device locking** check box (selected by default) and specify the minimum PIN length (6 characters by default) and timeout period (10 minutes by default).</span></span> <span data-ttu-id="21042-116">Мы рекомендуем использовать эти значения по умолчанию или увеличив длину PIN-кода и (или) уменьшить период ожидания.</span><span class="sxs-lookup"><span data-stu-id="21042-116">We recommend using these defaults or increasing the PIN length and/or decreasing the timeout period.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="21042-117">Подробнее смотрите в разделе <A href="lync-server-2013-enforce-phone-locking.md">принудительное использование блокировки телефона в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="21042-117">For details, see <A href="lync-server-2013-enforce-phone-locking.md">Enforce phone locking in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-security-settings-for-lync-phone-edition-phones-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="21042-118">Настройка параметров безопасности для телефонов Lync Phone Edition с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="21042-118">Configuring Security Settings for Lync Phone Edition Phones by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="21042-119">Параметры безопасности можно управлять с помощью командной консоли Lync Server Management Shell и командлета **Get-CsUCPhoneConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="21042-119">Security settings can be managed by using Lync Server Management Shell and the **Get-CsUCPhoneConfiguration** cmdlet.</span></span> <span data-ttu-id="21042-120">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21042-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="21042-121">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="21042-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-modify-the-sip-security-mode"></a><span data-ttu-id="21042-122">Изменение режима безопасности SIP</span><span class="sxs-lookup"><span data-stu-id="21042-122">To modify the SIP security mode</span></span>

  - <span data-ttu-id="21042-123">Эта команда задает средний уровень SIPSecurityMode для глобальной коллекции параметров телефонной связи UC.</span><span class="sxs-lookup"><span data-stu-id="21042-123">This command sets the SIPSecurityMode for the global collection of UC phone settings to Medium.</span></span> <span data-ttu-id="21042-124">Также можно установить низкий или высокий уровень безопасности SIP (значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="21042-124">SIP security could also be set to Low or High (the default value).</span></span>
    
        Set-CsUCPhoneConfiguration -Identity global -SIPSecurityMode "Medium"

</div>

<div>

## <a name="to-modify-the-minimum-pin-length"></a><span data-ttu-id="21042-125">Изменение минимальной длины PIN-кода</span><span class="sxs-lookup"><span data-stu-id="21042-125">To modify the minimum PIN length</span></span>

  - <span data-ttu-id="21042-126">В этом примере все параметры телефонной связи по УНИКАЛЬности изменяются для использования минимальной длины в 7 цифр.</span><span class="sxs-lookup"><span data-stu-id="21042-126">In this example, all the UC phone settings are modified to require a minimum PIN length of 7 digits.</span></span>
    
        Get-CsUCPhoneConfiguration | Set-CsUCPhoneConfiguration -MinPhonePinLength 7

</div>

<span data-ttu-id="21042-127">Подробности можно найти в [статьях Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).</span><span class="sxs-lookup"><span data-stu-id="21042-127">For details, see [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="21042-128">См. также</span><span class="sxs-lookup"><span data-stu-id="21042-128">See Also</span></span>


[<span data-ttu-id="21042-129">Управление проверкой подлинности Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21042-129">Managing Lync Server 2013 authentication</span></span>](lync-server-2013-managing-lync-server-authentication.md)  


[<span data-ttu-id="21042-130">Управление устройствами, телефонами и клиентскими приложениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21042-130">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="21042-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21042-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

