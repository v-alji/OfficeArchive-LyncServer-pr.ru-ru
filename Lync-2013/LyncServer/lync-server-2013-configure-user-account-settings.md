---
title: 'Lync Server 2013: настройка параметров учетных записей пользователей'
description: 'Lync Server 2013: Настройка параметров учетной записи пользователя.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure user account settings
ms:assetid: b7c74ecc-b924-4efc-8a56-3a5f94a9ef13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412896(v=OCS.15)
ms:contentKeyID: 48185200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e6ab4c57ba3d3e8c084314e1093736334312d0c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400060"
---
# <a name="configure-user-account-settings-in-lync-server-2013"></a><span data-ttu-id="12d0d-103">Настройка параметров учетных записей пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12d0d-103">Configure user account settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12d0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12d0d-104">

<span> </span></span></span>

<span data-ttu-id="12d0d-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="12d0d-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="12d0d-106">Для присоединения к конференции в качестве пользователей, прошедших проверку подлинности, пользователи конференц-связи с телефонным подключением вводят номера телефонов или добавочные номера и ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="12d0d-106">Dial-in users enter their phone number or extension and a PIN to join conferences as authenticated users.</span></span> <span data-ttu-id="12d0d-107">Для проверки подлинности требуется **универсальный код ресурса (URI)** телефонной линии, указанный в учетных записях пользователей Lync Server.</span><span class="sxs-lookup"><span data-stu-id="12d0d-107">The telephony **Line URI** specified on Lync Server user accounts is required for authentication.</span></span>

<span data-ttu-id="12d0d-108">В этом разделе описывается назначение **URI линии** отдельной учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="12d0d-108">The procedure in this topic describes how to assign a **Line URI** for a single user account.</span></span> <span data-ttu-id="12d0d-109">Чтобы назначить **URI линии** нескольким учетным записям пользователей, можно создать сценарий, использующий командлет **Set-CsUser**.</span><span class="sxs-lookup"><span data-stu-id="12d0d-109">If you need to assign a **Line URI** for multiple user accounts, you can create a script that uses the **Set-CsUser** cmdlet.</span></span> <span data-ttu-id="12d0d-110">Подробнее об использовании примера сценария для назначения **универсального кода ресурса (URI)** для нескольких учетных записей пользователей можно узнать в разделе "Назначение URI для разных строк нескольким пользователям" [https://go.microsoft.com/fwlink/p/?linkId=196945](https://go.microsoft.com/fwlink/p/?linkid=196945) .</span><span class="sxs-lookup"><span data-stu-id="12d0d-110">For details about using a sample script to assign **Line URI** to multiple user accounts, see "Assign Line URIs to Multiple Users" at [https://go.microsoft.com/fwlink/p/?linkId=196945](https://go.microsoft.com/fwlink/p/?linkid=196945).</span></span>

<div>

## <a name="to-configure-user-account-settings"></a><span data-ttu-id="12d0d-111">Настройка параметров учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="12d0d-111">To configure user account settings</span></span>

1.  <span data-ttu-id="12d0d-112">Выполните вход на компьютер с учетной записью члена группы RTCUniversalServerAdmins или члена роли **Cs-UserAdministrator** или **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="12d0d-112">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-UserAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="12d0d-113">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="12d0d-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="12d0d-114">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="12d0d-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="12d0d-115">На левой панели навигации щелкните **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="12d0d-115">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="12d0d-116">В поле поиска введите имя пользователя, которого нужно настроить для конференц-связи с телефонным подключением, или щелкните **Добавить фильтр**, чтобы задать поля поиска, а затем щелкните **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="12d0d-116">In the search field, type the name of the user you want to configure for dial-in conferencing or click **Add filter** to specify search fields, and then click **Find**.</span></span>

5.  <span data-ttu-id="12d0d-117">Дважды щелкните имя пользователя, чтобы открыть диалоговое окно " **изменение пользователя Lync Server** ".</span><span class="sxs-lookup"><span data-stu-id="12d0d-117">Double-click the user name to open the **Edit Lync Server User** dialog box.</span></span>

6.  <span data-ttu-id="12d0d-118">В разделе **Телефония** введите уникальный нормализованный номер телефона в поле **URI линии** (пример: tel:+14255550200).</span><span class="sxs-lookup"><span data-stu-id="12d0d-118">Under **Telephony**, in the **Line URI** field, type a unique, normalized phone number (for example, tel:+14255550200).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="12d0d-119">Вы можете указать <STRONG>URI линии</STRONG>, только если для параметра <STRONG>Телефония</STRONG> выбрано значение <STRONG>Только с одного ПК на другой</STRONG>, <STRONG>Корпоративная голосовая связь</STRONG>, <STRONG>Удаленное управление звонками</STRONG> или <STRONG>Только удаленное управление звонками</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="12d0d-119">You can specify <STRONG>Line URI</STRONG> only if <STRONG>Telephony</STRONG> is set to <STRONG>PC-to-PC only</STRONG>, <STRONG>Enterprise Voice</STRONG>, <STRONG>Remote call control</STRONG> or <STRONG>Remote call control only</STRONG>.</span></span>

    
    </div>

7.  <span data-ttu-id="12d0d-120">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="12d0d-120">Click **Commit**.</span></span>

<span data-ttu-id="12d0d-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12d0d-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

