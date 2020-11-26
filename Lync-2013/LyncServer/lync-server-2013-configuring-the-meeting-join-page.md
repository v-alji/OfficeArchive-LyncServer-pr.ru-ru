---
title: 'Lync Server 2013: конфигурация страницы присоединения к собранию'
description: 'Lync Server 2013: Настройка страницы "присоединение к собранию".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the meeting join page
ms:assetid: 45880423-47f4-49af-b825-cbd8e3fc1046
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204861(v=OCS.15)
ms:contentKeyID: 48184037
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e7c9dde0fdb6829da7bd11e16261a4bd76b7554
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432536"
---
# <a name="configuring-the-meeting-join-page-in-lync-server-2013"></a><span data-ttu-id="d3d69-103">Конфигурация страницы присоединения к собранию в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3d69-103">Configuring the meeting join page in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3d69-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3d69-104">

<span> </span></span></span>

<span data-ttu-id="d3d69-105">_**Тема последнего изменения:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="d3d69-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="d3d69-106">Когда пользователь щелкает ссылку на собрание в приглашении на собрание, страница присоединения к собранию определяет, уже установлен ли клиент Lync 2013 на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="d3d69-106">When a user clicks a meeting link in a meeting request, the meeting join page detects whether a Lync 2013 client is already installed on the user’s computer.</span></span> <span data-ttu-id="d3d69-107">Если клиент уже установлен, клиент открывает и присоединяется к собранию.</span><span class="sxs-lookup"><span data-stu-id="d3d69-107">If a client is already installed, the client opens and joins the meeting.</span></span> <span data-ttu-id="d3d69-108">Если клиент не установлен, по умолчанию открывается версия 2013 для Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="d3d69-108">If a client is not installed, by default the 2013 version of Lync Web App opens.</span></span>

<span data-ttu-id="d3d69-109">Вы можете изменить поведение страницы присоединения к собранию, если вы хотите разрешить пользователям присоединяться к собраниям с помощью Office Communicator 2007 R2 или Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="d3d69-109">You can modify the behavior of the meeting join page if you want to allow users to join meetings with Office Communicator 2007 R2 or Lync 2010 Attendant.</span></span> <span data-ttu-id="d3d69-110">Эти параметры конфигурации были удалены из панели управления Lync Server 2013, но их можно настроить с помощью командлета Set-CsWebServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d3d69-110">These configuration options have been removed from the Lync Server 2013 Control Panel, but you configure them by using the Set-CsWebServiceConfiguration cmdlet.</span></span>

### <a name="meeting-join-page-set-cswebserviceconfiguration-parameters"></a><span data-ttu-id="d3d69-111">Set-CsWebServiceConfiguration параметры страницы присоединения к собранию</span><span class="sxs-lookup"><span data-stu-id="d3d69-111">Meeting Join Page Set-CsWebServiceConfiguration Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3d69-112">Параметр Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3d69-112">Set-CsWebServiceConfiguration Parameter</span></span></th>
<th><span data-ttu-id="d3d69-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d3d69-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3d69-114">ShowJoinUsingLegacyClientLink</span><span class="sxs-lookup"><span data-stu-id="d3d69-114">ShowJoinUsingLegacyClientLink</span></span></p></td>
<td><p><span data-ttu-id="d3d69-115">Если установлено значение true, пользователи, присоединяющиеся к собранию с помощью клиентского приложения, отличного от Lync, получают возможность присоединиться к собранию с помощью Office Communicator 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d3d69-115">If set to True, users joining a meeting by using a client application other than Lync will be given the opportunity to join the meeting by using Office Communicator 2007 R2.</span></span> <span data-ttu-id="d3d69-116">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="d3d69-116">The default value is False.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d69-117">ShowAlternateJoinOptionsExpanded</span><span class="sxs-lookup"><span data-stu-id="d3d69-117">ShowAlternateJoinOptionsExpanded</span></span></p></td>
<td><p><span data-ttu-id="d3d69-118">Если установлено значение true, дополнительные параметры для присоединения к онлайн-конференции (например, Office Communicator 2007 R2) автоматически развертываются и появятся для пользователей.</span><span class="sxs-lookup"><span data-stu-id="d3d69-118">When set to True then alternate options for joining an online conference (such as Office Communicator 2007 R2) will automatically be expanded and shown to users.</span></span> <span data-ttu-id="d3d69-119">Если задано значение false (по умолчанию), эти параметры будут доступны, но пользователю потребуется отобразить список параметров.</span><span class="sxs-lookup"><span data-stu-id="d3d69-119">When set to False (the default value) these options will be available, but the user will have to display the list of options for themselves.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-the-meeting-join-page-by-using-lync-server-2013-management-shell"></a><span data-ttu-id="d3d69-120">Настройка страницы присоединения к собранию с помощью управляющей оболочки Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3d69-120">To configure the meeting join page by using Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="d3d69-121">Запустите командную консоль Lync Server 2013: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и щелкните **Командная консоль управления Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d3d69-121">Start the Lync Server 2013 Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="d3d69-122">Чтобы просмотреть параметры конфигурации веб-службы, выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="d3d69-122">To view the web service configuration settings, run the following cmdlet:</span></span>
    
        Get-CsWebServiceConfiguration

3.  <span data-ttu-id="d3d69-123">Выполните следующую команду, если для параметров задано значение истина или ложь, в зависимости от предпочтения (Дополнительные сведения о параметрах этого командлета можно найти в статье [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration) в документации по среде управления Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="d3d69-123">Run the following command, with the parameters set to True or False, depending on your preference (for details about the parameters for this cmdlet, see [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration) in the Lync Server 2013 Management Shell documentation):</span></span>
    
        Set-CsWebServiceConfiguration -Identity global -ShowJoinUsingLegacyClientLink $True

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d3d69-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d3d69-124">See Also</span></span>


[<span data-ttu-id="d3d69-125">Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3d69-125">Set-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)  
  

<span data-ttu-id="d3d69-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3d69-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

