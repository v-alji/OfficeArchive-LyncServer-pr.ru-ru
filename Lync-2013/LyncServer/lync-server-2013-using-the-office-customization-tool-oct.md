---
title: 'Lync Server 2013: использование средства развертывания Office (OCT)'
description: 'Lync Server 2013: использование средства развертывания Office (OCT).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Office Customization Tool (OCT)
ms:assetid: 26647cb6-ba84-4ba7-8b6f-2cf86818e530
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204748(v=OCS.15)
ms:contentKeyID: 48183654
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 602502ba4579ed6c640eee909d4c6b056ce247d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400120"
---
# <a name="using-the-office-customization-tool-oct-in-lync-server-2013"></a><span data-ttu-id="b91c6-103">Использование средства развертывания Office (OCT) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b91c6-103">Using the Office Customization Tool (OCT) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b91c6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b91c6-104">

<span> </span></span></span>

<span data-ttu-id="b91c6-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b91c6-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b91c6-106">Центр развертывания Office входит в состав программы установки и является рекомендованным средством для многих видов настройки.</span><span class="sxs-lookup"><span data-stu-id="b91c6-106">The Office Customization Tool (OCT) is part of the Setup program and is the recommended tool for many customizations.</span></span> <span data-ttu-id="b91c6-107">С помощью центра развертывания Office можно настроить Office и сохранить настройки установки в MSP-файле.</span><span class="sxs-lookup"><span data-stu-id="b91c6-107">By using the OCT, you customize Office and save your customizations in a Setup customization .msp file.</span></span> <span data-ttu-id="b91c6-108">Этот файл можно поместить в папку "Updates" в точке сетевой установки.</span><span class="sxs-lookup"><span data-stu-id="b91c6-108">You place the file in the Updates folder on the network installation point.</span></span> <span data-ttu-id="b91c6-109">Во время установки Office программа установки выполняет поиск файла настроек установки в папке "Updates" и применяет эти настройки.</span><span class="sxs-lookup"><span data-stu-id="b91c6-109">When you install Office, Setup looks for a Setup customization file in the Updates folder and applies the customizations.</span></span> <span data-ttu-id="b91c6-110">Папку Updates можно использовать только для развертывания обновлений программного обеспечения во время первоначальной установки Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b91c6-110">The Updates folder can be used only to deploy software updates during an initial installation of Office 2013.</span></span>

<span data-ttu-id="b91c6-111">Центр развертывания Office является частью программы установки и включается в версии продукта с лицензией для многократной установки.</span><span class="sxs-lookup"><span data-stu-id="b91c6-111">The OCT is part of setup and it is included in volume license versions of the product.</span></span> <span data-ttu-id="b91c6-112">Вы запускаете приложение OCT, введя `setup.exe /admin` в командной строке корневой каталог точки сетевой установки, содержащей исходные файлы Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b91c6-112">You run the OCT by typing `setup.exe /admin` at the command line from the root of the network installation point that contains the Office 2013 source files.</span></span> <span data-ttu-id="b91c6-113">Например, используйте следующий путь.</span><span class="sxs-lookup"><span data-stu-id="b91c6-113">For example, use the following:</span></span>

`\\server\share\Office15\setup.exe /admin`

<span data-ttu-id="b91c6-114">С помощью центра развертывания Office администратор может создать и настроить MSP-файл с настройками установки.</span><span class="sxs-lookup"><span data-stu-id="b91c6-114">Administrators use the OCT to create a setup customization .msp file.</span></span> <span data-ttu-id="b91c6-115">Как и в Microsoft Office 2010 OCT, администраторы могут настраивать следующие области:</span><span class="sxs-lookup"><span data-stu-id="b91c6-115">As in the Microsoft Office 2010 OCT, administrators can customize the following areas:</span></span>

  - <span data-ttu-id="b91c6-116">**Настройка** Используется для указания местоположения для установки по умолчанию на клиенте и названии организации по умолчанию, дополнительные источники сетевой установки, ключ продукта, лицензионное соглашение с конечным пользователем, уровень отображения и более ранние версии Office для удаления, пользовательские программы для запуска во время установки, параметры безопасности и свойства настройки.</span><span class="sxs-lookup"><span data-stu-id="b91c6-116">**Setup** Used to specify default installation location on the client and default organization name, additional network installation sources, product key, end-user license agreement, display level, earlier versions of Office to remove, custom programs to run during installation, security settings, and Setup properties.</span></span>

  - <span data-ttu-id="b91c6-117">**Функции** Используется для настройки параметров пользователя и для настройки способа установки компонентов Office.</span><span class="sxs-lookup"><span data-stu-id="b91c6-117">**Features** Used to configure user settings and to customize how Office features are installed.</span></span> <span data-ttu-id="b91c6-118">С помощью центра развертывания Office администратор может указать первоначальные значения по умолчанию для пользовательских параметров приложений Office.</span><span class="sxs-lookup"><span data-stu-id="b91c6-118">Administrators can use the OCT to specify initial default values of Office application settings for users.</span></span> <span data-ttu-id="b91c6-119">После установки пользователи могут изменить большинство из этих параметров.</span><span class="sxs-lookup"><span data-stu-id="b91c6-119">Users can modify most of the settings after the installation.</span></span>

  - <span data-ttu-id="b91c6-120">**Дополнительное содержимое** Используется для добавления и удаления файлов, добавления и удаления записей в реестре, а также для настройки сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="b91c6-120">**Additional content** Used to add or remove files, add or remove registry entries, and configure shortcuts.</span></span>

  - <span data-ttu-id="b91c6-121">**Приложение Outlook** Используется для настройки профиля пользователя Outlook по умолчанию, указания параметров Exchange, добавления учетных записей, удаления учетных записей и экспорта параметров и задания \\ групп получения отправки.</span><span class="sxs-lookup"><span data-stu-id="b91c6-121">**Outlook** Used to customize a user's default Outlook profile, specify Exchange settings, add accounts, remove accounts and export settings, and specify Send\\Receive groups.</span></span>

<span data-ttu-id="b91c6-122">Дополнительные сведения о программе OCT можно найти в статьях <https://go.microsoft.com/fwlink/p/?linkid=267516> .</span><span class="sxs-lookup"><span data-stu-id="b91c6-122">For information about the OCT, see <https://go.microsoft.com/fwlink/p/?linkid=267516>.</span></span>

<span data-ttu-id="b91c6-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b91c6-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

