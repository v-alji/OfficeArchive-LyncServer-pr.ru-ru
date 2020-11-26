---
title: 'Lync Server 2013: подготовка схемы Active Directory'
description: 'Lync Server 2013: подготовка схемы Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the Active Directory schema
ms:assetid: 067726ae-fd3f-4133-a32f-26d2603ac674
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398119(v=OCS.15)
ms:contentKeyID: 48183300
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3df7533dcbabe278fd366b441cfd8daa83f54b23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424116"
---
# <a name="preparing-the-active-directory-schema-in-lync-server-2013"></a><span data-ttu-id="17207-103">Подготовка схемы Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17207-103">Preparing the Active Directory schema in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17207-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17207-104">

<span> </span></span></span>

<span data-ttu-id="17207-105">_**Тема последнего изменения:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="17207-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="17207-106">Прежде чем приступить к подготовке доменных служб Active Directory, вы можете открыть файлы схемы в текстовом редакторе, например в блокноте Windows, или [2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) ознакомиться с расширениями схемы доменных служб Active Directory, которые будут изменены для lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="17207-106">Before you begin preparing Active Directory Domain Services, you can open the schema files by using a text editor, such as Windows Notepad, or see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) to review all the Active Directory Domain Services schema extensions that will be modified for Lync Server 2013.</span></span> <span data-ttu-id="17207-107">Lync Server использует четыре файла схемы:</span><span class="sxs-lookup"><span data-stu-id="17207-107">Lync Server uses four schema files:</span></span>

  - <span data-ttu-id="17207-108">ExternalSchema. ldf, который используется для взаимодействия с сервером Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="17207-108">ExternalSchema.ldf, which is used for interoperability with Microsoft Exchange Server</span></span>

  - <span data-ttu-id="17207-109">ServerSchema. ldf, являющийся основным файлом схемы Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17207-109">ServerSchema.ldf, which is the primary Lync Server 2013 schema file</span></span>

  - <span data-ttu-id="17207-110">BackCompatSchema. ldf, который используется для взаимодействия с любыми компонентами предыдущих выпусков</span><span class="sxs-lookup"><span data-stu-id="17207-110">BackCompatSchema.ldf, which is used for interoperability with any components from prior releases</span></span>

  - <span data-ttu-id="17207-111">VersionSchema. ldf, который используется для получения сведений о версии подготовленной схемы</span><span class="sxs-lookup"><span data-stu-id="17207-111">VersionSchema.ldf, which is used for version information of the prepared schema</span></span>

<span data-ttu-id="17207-112">Все LDF-файлы устанавливаются во время подготовки схемы, независимо от того, выполняется ли миграция из предыдущего выпуска или выполняется чистая установка.</span><span class="sxs-lookup"><span data-stu-id="17207-112">All .ldf files are installed during schema preparation, regardless of whether you are migrating from a previous release or performing a clean installation.</span></span> <span data-ttu-id="17207-113">Эти файлы схемы устанавливаются в последовательности, указанной в предыдущем списке, и находятся в \\ \\ папке схемы поддержки на установочном носителе.</span><span class="sxs-lookup"><span data-stu-id="17207-113">These schema files are installed in the sequence shown in the preceding list and are located in the \\Support\\schema folder on the installation media.</span></span>

<span data-ttu-id="17207-114">Расширения схемы Lync Server реплицируются по всем доменам, что влияет на сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="17207-114">The Lync Server schema extensions are replicated across all domains, which impacts network traffic.</span></span> <span data-ttu-id="17207-115">Выполняйте подготовку схемы по истечении уровня использования сети.</span><span class="sxs-lookup"><span data-stu-id="17207-115">Run schema preparation at a time when network usage is low.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="17207-116">Если вам нужно добавить поддержку для Microsoft® Office Communicator Mobile 2007 R2 для Java и Microsoft® Office Communicator Mobile 1,0 для мобильных клиентов в среде Lync Server 2013, вам нужно подготовить схему Active Directory для Microsoft Office Communications Server 2007 R2 во время установки Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="17207-116">If you need to add support for Microsoft® Office Communicator Mobile 2007 R2 for Java and Microsoft® Office Communicator Mobile for Nokia 1.0 mobile clients to your Lync Server 2013 deployment, you need to prepare the Active Directory schema for Microsoft Office Communications Server 2007 R2 during installation of Lync Server 2013.</span></span> <span data-ttu-id="17207-117">Необходимое программное обеспечение и документацию можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A> .</span><span class="sxs-lookup"><span data-stu-id="17207-117">For the necessary software and documentation, see <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A>.</span></span>



</div>

<div>

## <a name="adsi-edit"></a><span data-ttu-id="17207-118">Редактирование ADSI</span><span class="sxs-lookup"><span data-stu-id="17207-118">ADSI Edit</span></span>

<span data-ttu-id="17207-119">Редактор интерфейсов служб Active Directory (Редактирование ADSI) — это средство администрирования доменных служб, которое можно использовать для проверки подготовки и репликации схемы.</span><span class="sxs-lookup"><span data-stu-id="17207-119">Active Directory Service Interfaces Editor (ADSI Edit) is an AD DS administration tool that you can use to verify schema preparation and replication.</span></span>

<span data-ttu-id="17207-120">Редактирование ADSI устанавливается по умолчанию при установке роли AD DS, чтобы сделать сервер контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="17207-120">ADSI Edit is installed by default when you install the AD DS role to make a server a domain controller.</span></span> <span data-ttu-id="17207-121">В Windows Server 2008 и Windows Server 2008 R2 средство редактирования ADSI (adsiedit. msc) входит в состав средств удаленного администрирования сервера (RSAT).</span><span class="sxs-lookup"><span data-stu-id="17207-121">For Windows Server 2008 and Windows Server 2008 R2, ADSI Edit (adsiedit.msc) is included with the Remote Server Administration Tools (RSAT).</span></span> <span data-ttu-id="17207-122">Вы также можете установить RSAT на рядовые серверы домена или отдельные серверы.</span><span class="sxs-lookup"><span data-stu-id="17207-122">You can also install RSAT on domain member servers or stand-alone servers.</span></span> <span data-ttu-id="17207-123">Пакет RSAT копируется на эти серверы по умолчанию при установке Windows, но не устанавливается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17207-123">The RSAT package is copied to these servers by default when you install Windows, but it is not installed by default.</span></span> <span data-ttu-id="17207-124">Отдельные инструменты устанавливаются с помощью диспетчера сервера.</span><span class="sxs-lookup"><span data-stu-id="17207-124">You install individual tools by using Server Manager.</span></span> <span data-ttu-id="17207-125">Редактирование ADSI входит в раздел **средства администрирования ролей**, **средства доменных служб Active Directory**, **средства контроллера домена Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="17207-125">ADSI Edit is included under **Role Administration Tools**, **Active Directory Domain Services Tools**, **Active Directory Domain Controller Tools**.</span></span>

<span data-ttu-id="17207-126">В Windows Server 2003 Редактирование ADSI входит в состав средств поддержки.</span><span class="sxs-lookup"><span data-stu-id="17207-126">For Windows Server 2003, ADSI Edit is included with the Support Tools.</span></span> <span data-ttu-id="17207-127">Средства поддержки доступны на компакт-диске Windows Server 2003 в \\ \\ папке "средства поддержки", а также в разделе "windows Server 2003 с пакетом обновления 2 32-разрядная версия для поддержки" [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770) .</span><span class="sxs-lookup"><span data-stu-id="17207-127">The Support Tools are available from the Windows Server 2003 CD in the \\SUPPORT\\TOOLS folder, or you can download them from “Windows Server 2003 Service Pack 2 32-bit Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770).</span></span> <span data-ttu-id="17207-128">Инструкции по установке средств поддержки с компакт-диска продукта можно найти в разделе "Установка средств поддержки Windows" на сайте [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771) .</span><span class="sxs-lookup"><span data-stu-id="17207-128">Instructions for installing the Support Tools from the product CD are available from “Install Windows Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771).</span></span> <span data-ttu-id="17207-129">Adsiedit.dll автоматически регистрируется при установке средств поддержки.</span><span class="sxs-lookup"><span data-stu-id="17207-129">Adsiedit.dll is automatically registered when you install the support tools.</span></span> <span data-ttu-id="17207-130">Тем не менее, если вы скопировали файлы на свой компьютер, необходимо выполнить команду **regsvr32** , чтобы зарегистрировать файл adsiedit.dll, прежде чем можно будет запустить средство.</span><span class="sxs-lookup"><span data-stu-id="17207-130">If, however, you copied the files to your computer, you must run the **regsvr32** command to register the adsiedit.dll file before you can run the tool.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="17207-131">Содержание</span><span class="sxs-lookup"><span data-stu-id="17207-131">In This Section</span></span>

  - [<span data-ttu-id="17207-132">Проведение подготовки схемы Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17207-132">Running Active Directory schema preparation in Lync Server 2013</span></span>](lync-server-2013-running-schema-preparation.md)

  - [<span data-ttu-id="17207-133">Проверка репликации схемы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17207-133">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="17207-134">См. также</span><span class="sxs-lookup"><span data-stu-id="17207-134">See Also</span></span>


[<span data-ttu-id="17207-135">Подготовка леса для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17207-135">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
[<span data-ttu-id="17207-136">Подготовка доменов для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17207-136">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="17207-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17207-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

