---
title: 'Lync Server 2013: Общие сведения о гибридной среде Lync Server'
description: 'Lync Server 2013: Общие сведения о гибридной среде Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Lync Server 2013 hybrid environment
ms:assetid: 0d16ec3a-28f0-4483-96e7-8e68f30398fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204669(v=OCS.15)
ms:contentKeyID: 48183399
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95b0ae433dafad349d7ef9b6328e43dbc308579c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445045"
---
# <a name="overview-of-the-lync-server-2013-hybrid-environment"></a><span data-ttu-id="3795c-103">Общие сведения о гибридной среде Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3795c-103">Overview of the Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3795c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3795c-104">

<span> </span></span></span>

<span data-ttu-id="3795c-105">_**Тема последнего изменения:** 2014-05-28_</span><span class="sxs-lookup"><span data-stu-id="3795c-105">_**Topic Last Modified:** 2014-05-28_</span></span>

<span data-ttu-id="3795c-106">Гибридная Среда Lync Server 2013 имеет отношение к развертыванию, в котором некоторые пользователи находятся на локальном сервере Lync Server 2013 и других пользователях, подключенных к Lync Online, но пользователи имеют доступ к тому же домену, например user@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="3795c-106">Lync Server 2013 hybrid environment refers to a deployment in which there are some users homed to the on-premises Lync Server 2013 and other users homed to Lync Online, but users share the same domain, such as user@contoso.com.</span></span>

<div>

## <a name="about-this-guide"></a><span data-ttu-id="3795c-107">Сведения об этом руководстве</span><span class="sxs-lookup"><span data-stu-id="3795c-107">About this Guide</span></span>

<span data-ttu-id="3795c-108">В этом руководстве описаны задачи, необходимые для настройки среды Lync Server 2013 для взаимодействия с Lync Online, а также перемещения пользователей из локального развертывания для использования Lync Online.</span><span class="sxs-lookup"><span data-stu-id="3795c-108">This guide describes the tasks necessary to configure your Lync Server 2013 environment for interoperability with Lync Online, and then to move users from your on-premises deployment to use Lync Online.</span></span>

</div>

<div>

## <a name="prerequisites"></a><span data-ttu-id="3795c-109">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="3795c-109">Prerequisites</span></span>

<span data-ttu-id="3795c-110">Для выполнения задач по настройке гибридного развертывания на компьютере должны быть установлены следующие приложения и служебные программы.</span><span class="sxs-lookup"><span data-stu-id="3795c-110">You will need to have the following applications and utilities installed to complete the tasks for configuring a deployment for hybrid.</span></span> <span data-ttu-id="3795c-111">Установщики для этих файлов будут включены в установочный носитель, указанный для развертывания, а также ссылки, приведенные в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="3795c-111">The installers for these files are included on the installation media provided for your deployment, as well as at the links included in the following list.</span></span>

  - [<span data-ttu-id="3795c-112">Службы федерации Active Directory (AD FS) 2,0</span><span class="sxs-lookup"><span data-stu-id="3795c-112">Active Directory Federation Services (AD FS) 2.0</span></span>](https://go.microsoft.com/fwlink/p/?linkid=257305)

  - [<span data-ttu-id="3795c-113">Средство синхронизации каталогов Microsoft 9,1</span><span class="sxs-lookup"><span data-stu-id="3795c-113">Microsoft Directory Synchronization Tool 9.1</span></span>](https://go.microsoft.com/fwlink/p/?linkid=257307)

  - [<span data-ttu-id="3795c-114">Установка Windows PowerShell для единого входа с помощью AD FS</span><span class="sxs-lookup"><span data-stu-id="3795c-114">Install Windows PowerShell for single sign-on with AD FS</span></span>](https://go.microsoft.com/fwlink/p/?linkid=398710)

  - <span data-ttu-id="3795c-115">Помощник по входу в Microsoft Online Services (msoidcli-7.0.msi) входит в настройку настольного компьютера для Microsoft 365, которую можно получить на странице загрузки, связанной с центром администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3795c-115">Microsoft Online Services Sign-in Assistant (msoidcli-7.0.msi) is included with the Desktop Setup for Microsoft 365, which can be obtained from the Downloads page linked to from the Microsoft 365 admin center.</span></span>

</div>

<div>

## <a name="administrator-credentials"></a><span data-ttu-id="3795c-116">Учетные данные администратора</span><span class="sxs-lookup"><span data-stu-id="3795c-116">Administrator Credentials</span></span>

<span data-ttu-id="3795c-117">Когда вам будет предложено ввести учетные данные администратора, введите имя пользователя и пароль для учетной записи администратора для своей организации Microsoft 365 или Office 365.</span><span class="sxs-lookup"><span data-stu-id="3795c-117">When you are asked to provide your administrator credentials, use the username and password for the administrator account for your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="3795c-118">Эти учетные данные также будут использоваться при настройке служб федерации Active Directory (AD FS) 2,0, синхронизации каталогов, единого входа, Федерации и перемещения пользователей на Lync Online.</span><span class="sxs-lookup"><span data-stu-id="3795c-118">You will also use these credentials when you configure Active Directory Federation Services (AD FS) 2.0, Directory Synchronization, Single sign-on, federation, and moving users to Lync Online.</span></span>

</div>

<div>

## <a name="connecting-to-lync-online-powershell"></a><span data-ttu-id="3795c-119">Подключение к Lync Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="3795c-119">Connecting to Lync Online PowerShell</span></span>

<span data-ttu-id="3795c-120">Администраторы теперь могут использовать Windows PowerShell для управления Lync Online и их учетными записями пользователей Lync Online.</span><span class="sxs-lookup"><span data-stu-id="3795c-120">Administrators now have the ability to use Windows PowerShell to manage Lync Online and their Lync Online user accounts.</span></span> <span data-ttu-id="3795c-121">Для этого сначала необходимо скачать и установить модуль соединительной линии Lync Online из центра загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=294688) .</span><span class="sxs-lookup"><span data-stu-id="3795c-121">To do this, you must first download and install the Lync Online Connector Module from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=294688).</span></span> <span data-ttu-id="3795c-122">Дополнительные сведения о загрузке, установке и использовании модуля соединительной линии Lync Online и подробные сведения об использовании Windows PowerShell для управления Lync Online можно найти [в разделе Использование Windows PowerShell для управления Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="3795c-122">For more information on downloading, installing, and using the Lync Online Connector Module, and for detailed information on using Windows PowerShell to manage Lync Online, see [Using Windows PowerShell to manage Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

<span data-ttu-id="3795c-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3795c-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

