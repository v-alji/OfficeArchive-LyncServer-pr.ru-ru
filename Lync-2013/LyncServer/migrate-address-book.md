---
title: Перенос адресной книги
description: Перенесите адресную книгу.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Address Book
ms:assetid: ac7f0f39-4c6d-4702-8e25-93a73e3d800f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205160(v=OCS.15)
ms:contentKeyID: 48185064
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad6acd8cca58aa4e09e21b9b45cbdddec527b5f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438612"
---
# <a name="migrate-address-book"></a><span data-ttu-id="a0e35-103">Перенос адресной книги</span><span class="sxs-lookup"><span data-stu-id="a0e35-103">Migrate Address Book</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0e35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0e35-104">

<span> </span></span></span>

<span data-ttu-id="a0e35-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="a0e35-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="a0e35-106">Как правило, адресная книга Lync Server 2010 переносится вместе с оставшейся частью вашей топологии.</span><span class="sxs-lookup"><span data-stu-id="a0e35-106">In general, the Lync Server 2010 Address Book is migrated along with the rest of your topology.</span></span> <span data-ttu-id="a0e35-107">Тем не менее, если вы настроили указанные ниже действия в среде Lync Server 2010, вам может потребоваться выполнить некоторые шаги после миграции.</span><span class="sxs-lookup"><span data-stu-id="a0e35-107">However, you might need to perform some post-migration steps if you customized the following in your Lync Server 2010 environment:</span></span>

  - <span data-ttu-id="a0e35-108">Установите свойство WMI **PartitionbyOU** для группировки записей в адресную книгу по организационному подразделению (OU).</span><span class="sxs-lookup"><span data-stu-id="a0e35-108">Set the **PartitionbyOU** WMI property to group Address Book entries by organizational unit (OU).</span></span>

  - <span data-ttu-id="a0e35-109">Настроены правила нормализации адресных книг.</span><span class="sxs-lookup"><span data-stu-id="a0e35-109">Customized the Address Book normalization rules.</span></span>

  - <span data-ttu-id="a0e35-110">Изменение значения по умолчанию для параметра **UseNormalizationRules** на false.</span><span class="sxs-lookup"><span data-stu-id="a0e35-110">Changed the default value for the **UseNormalizationRules** parameter to False.</span></span>

<span data-ttu-id="a0e35-111">**Группировка записей в адресную книгу**</span><span class="sxs-lookup"><span data-stu-id="a0e35-111">**Grouped Address Book Entries**</span></span>

<span data-ttu-id="a0e35-112">Если для свойства **PartitionbyOU** WMI установлено значение true, чтобы создать адресные книги для каждого подразделения, необходимо задать атрибут **msRTCSIP-GroupingId** Active Directory для пользователей и контактов, если вы хотите продолжить группировку записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="a0e35-112">If you set the **PartitionbyOU** WMI property to True to create address books for each OU, you need to set the **msRTCSIP-GroupingId** Active Directory attribute on users and contacts if you want to continue grouping address book entries.</span></span> <span data-ttu-id="a0e35-113">Возможно, вам потребуется сгруппировать записи в адресную книгу, чтобы ограничить область поиска в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="a0e35-113">You might want to group address book entries to limit the scope of Address Book searches.</span></span> <span data-ttu-id="a0e35-114">Чтобы использовать атрибут **msRTCSIP-GroupingId** , напишите сценарий для заполнения атрибута и назначайте одинаковые значения для всех пользователей, которые нужно сгруппировать.</span><span class="sxs-lookup"><span data-stu-id="a0e35-114">To use the **msRTCSIP-GroupingId** attribute, write a script to populate the attribute, assigning the same value for all of the users that you want to group together.</span></span> <span data-ttu-id="a0e35-115">Например, вы назначаете одно значение для всех пользователей в подразделении.</span><span class="sxs-lookup"><span data-stu-id="a0e35-115">For example, assign a single value for all the users in an OU.</span></span>

<span data-ttu-id="a0e35-116">**Правила нормализации адресных книг**</span><span class="sxs-lookup"><span data-stu-id="a0e35-116">**Address Book Normalization Rules**</span></span>

<span data-ttu-id="a0e35-117">Если вы настроили правила нормализации адресных книг в среде Lync Server 2010, вы должны перенести настроенные правила в ваш пилотный пул.</span><span class="sxs-lookup"><span data-stu-id="a0e35-117">If you customized Address Book normalization rules in your Lync Server 2010 environment, you must migrate the customized rules to your pilot pool.</span></span> <span data-ttu-id="a0e35-118">Если вы не настраиваете правила нормализации адресных книг, вы не можете выполнить миграцию для службы адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a0e35-118">If you did not customize Address Book normalization rules, you have nothing to migrate for Address Book service.</span></span> <span data-ttu-id="a0e35-119">Правила нормализации по умолчанию для Lync Server 2013 совпадают с правилами по умолчанию для Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="a0e35-119">The default normalization rules for Lync Server 2013 are the same as the default rules for Lync Server 2010.</span></span> <span data-ttu-id="a0e35-120">Выполните действия, описанные ниже в этом разделе, чтобы перенести настраиваемые правила нормализации.</span><span class="sxs-lookup"><span data-stu-id="a0e35-120">Follow the procedure later in this section to migrate customized normalization rules.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a0e35-121">Если в вашей организации используется удаленное управление звонками и настроены правила нормализации адресных книг, необходимо выполнить описанные ниже действия, прежде чем можно будет использовать удаленное управление звонками.</span><span class="sxs-lookup"><span data-stu-id="a0e35-121">If your organization uses remote call control and you customized Address Book normalization rules, you must perform the procedure in this topic before you can use remote call control.</span></span> <span data-ttu-id="a0e35-122">Процедура требует членства в группе RTCUniversalServerAdmins или эквивалентных прав.</span><span class="sxs-lookup"><span data-stu-id="a0e35-122">The procedure requires membership in the RTCUniversalServerAdmins group or equivalent rights.</span></span>



</div>

<span data-ttu-id="a0e35-123">**Для UseNormalizationRules задано значение false**</span><span class="sxs-lookup"><span data-stu-id="a0e35-123">**UseNormalizationRules Set to False**</span></span>

<span data-ttu-id="a0e35-124">Если задать для **UseNormalizationRules** значение false, чтобы пользователи могли использовать номера телефонов в соответствии с параметрами, определенными в доменных службах Active Directory без применения правил нормализации для Lync Server 2013, необходимо задать для параметров **UseNormalizationRules** и **IgnoreGenericRules** значение true.</span><span class="sxs-lookup"><span data-stu-id="a0e35-124">If you set the value for **UseNormalizationRules** to False so that users can use phone numbers as they are defined in Active Directory Domain Services without having Lync Server 2013 apply normalization rules, you need to set the **UseNormalizationRules** and **IgnoreGenericRules** parameters to True.</span></span> <span data-ttu-id="a0e35-125">Выполните действия, описанные ниже в этом разделе, чтобы установить для этих параметров значение true.</span><span class="sxs-lookup"><span data-stu-id="a0e35-125">Follow the procedure later in this section to set these parameters to True.</span></span>

<div>

## <a name="to-migrate-address-book-customized-normalization-rules"></a><span data-ttu-id="a0e35-126">Миграция настроенных правил нормализации в адресной книге</span><span class="sxs-lookup"><span data-stu-id="a0e35-126">To migrate Address Book customized normalization rules</span></span>

1.  <span data-ttu-id="a0e35-127">Найдите \_ \_ \_Rules.txt файл Нормализация номера компании \_ в корне общей папки адресной книги, а затем скопируйте его в корневой каталог в общей папке адресной книги в Lync Server 2013 Pilot pooling.</span><span class="sxs-lookup"><span data-stu-id="a0e35-127">Find the Company\_Phone\_Number\_Normalization\_Rules.txt file in the root of the Address Book shared folder, and copy it to the root of the Address Book shared folder in your Lync Server 2013 pilot pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a0e35-128">Примеры правил нормализации адресных книг установлены в каталог файлов веб-компонентов ABS.</span><span class="sxs-lookup"><span data-stu-id="a0e35-128">The sample Address Book normalization rules have been installed in your ABS Web component file directory.</span></span> <span data-ttu-id="a0e35-129">Путь <STRONG>$installedDriveLetter: \Program Files\Microsoft Lync Server 2013 \ Web Components\Address Book Files\Files\ Sample_Company_Phone_Number_Normalization_Rules.txt</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a0e35-129">The path is <STRONG>$installedDriveLetter:\Program Files\Microsoft Lync Server 2013\Web Components\Address Book Files\Files\ Sample_Company_Phone_Number_Normalization_Rules.txt,</STRONG>.</span></span> <span data-ttu-id="a0e35-130">Этот файл можно скопировать и переименовать как &nbsp; <STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp; в корневой каталог общей папки адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a0e35-130">This file can be copied and renamed as &nbsp;<STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp;to the address book shared folder’s root directory.</span></span> <span data-ttu-id="a0e35-131">Например, адресная книга, доступная в <STRONG>$serverX</STRONG>, &nbsp; будет выглядеть примерно так: <STRONG> \\ $serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a0e35-131">For example, the address book shared in <STRONG>$serverX</STRONG>,&nbsp;the path will be similar to: <STRONG>\\$serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>.</span></span>

    
    </div>

2.  <span data-ttu-id="a0e35-132">Откройте в текстовом редакторе, например в блокноте, \_ \_ \_Rules.txt файл Нормализация номера телефона компании \_ .</span><span class="sxs-lookup"><span data-stu-id="a0e35-132">Use a text editor, such as Notepad, to open the Company\_Phone\_Number\_Normalization\_Rules.txt file.</span></span>

3.  <span data-ttu-id="a0e35-133">Некоторые типы записей не будут правильно работать в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0e35-133">Certain types of entries will not work correctly in Lync Server 2013.</span></span> <span data-ttu-id="a0e35-134">Просмотрите файл на предмет типов записей, описанных в этом шаге, внесите необходимые изменения и сохраните изменения в общей папке адресной книги в вашем пилотном пуле.</span><span class="sxs-lookup"><span data-stu-id="a0e35-134">Look through the file for the types of entries described in this step, edit them as necessary, and save the changes to the Address Book shared folder in your pilot pool.</span></span>
    
    <span data-ttu-id="a0e35-135">Строки, содержащие требуемый пробел или знаки препинания, приводят к сбою правил нормализации, так как эти символы удаляются из строки, вводимой в правила нормализации.</span><span class="sxs-lookup"><span data-stu-id="a0e35-135">Strings that include required whitespace or punctuation cause normalization rules to fail because these characters are stripped out of the string that is input to the normalization rules.</span></span> <span data-ttu-id="a0e35-136">Если у вас есть строки, содержащие необходимые пробелы или знаки препинания, необходимо изменить строки.</span><span class="sxs-lookup"><span data-stu-id="a0e35-136">If you have strings that include required whitespace or punctuation, you need to modify the strings.</span></span> <span data-ttu-id="a0e35-137">Например, следующая строка может привести к сбою правила нормализации:</span><span class="sxs-lookup"><span data-stu-id="a0e35-137">For example, the following string would cause the normalization rule to fail:</span></span>
    
        \s*\(\s*\d\d\d\s*\)\s*\-\s*\d\d\d\s*\-\s*\d\d\d\d
    
    <span data-ttu-id="a0e35-138">Следующая строка не приводила к сбою правила нормализации:</span><span class="sxs-lookup"><span data-stu-id="a0e35-138">The following string would not cause the normalization rule to fail:</span></span>
    
        \s*\(?\s*\d\d\d\s*\)?\s*\-?\s*\d\d\d\s*\-?\s*\d\d\d\d

</div>

<div>

## <a name="to-set-usenormalizationrules-and-ignoregenericrules-to-true"></a><span data-ttu-id="a0e35-139">Чтобы установить для UseNormalizationRules и IgnoreGenericRules значение true,</span><span class="sxs-lookup"><span data-stu-id="a0e35-139">To set UseNormalizationRules and IgnoreGenericRules to true</span></span>

1.  <span data-ttu-id="a0e35-140">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="a0e35-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a0e35-141">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="a0e35-141">Do one of the following:</span></span>
    
      - <span data-ttu-id="a0e35-142">Если развертывание включает только сервер Lync Server 2013, выполните следующий командлет на глобальном уровне, чтобы изменить значения для **UseNormalizationRules** и **IgnoreGenericRules** на true:</span><span class="sxs-lookup"><span data-stu-id="a0e35-142">If your deployment includes only Lync Server 2013, run the following cmdlet at the global level to change the values for **UseNormalizationRules** and **IgnoreGenericRules** to True:</span></span>
        
            Set-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true
    
      - <span data-ttu-id="a0e35-143">Если в развертывании есть сочетание Lync Server 2013 и Lync Server 2010 или Office Communications Server 2007 R2, запустите следующий командлет и назначьте его каждому пулу Lync Server 2013 в топологии.</span><span class="sxs-lookup"><span data-stu-id="a0e35-143">If your deployment includes a combination of Lync Server 2013 and Lync Server 2010 or Office Communications Server 2007 R2, run the following cmdlet and assign it to each Lync Server 2013 pool in the topology:</span></span>
        
            New-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true

3.  <span data-ttu-id="a0e35-144">Дождитесь, когда репликация хранилища центрального управления будет выполняться на всех пулах.</span><span class="sxs-lookup"><span data-stu-id="a0e35-144">Wait for Central Management store replication to occur on all pools.</span></span>

4.  <span data-ttu-id="a0e35-145">Измените файл правил нормализации телефонной линии " \_ \_ нормализация номера телефона компании \_ \_Rules.txt", чтобы ваше развертывание было очищено от содержимого.</span><span class="sxs-lookup"><span data-stu-id="a0e35-145">Modify the phone normalization rules file, "Company\_Phone\_Number\_Normalization\_Rules.txt", for your deployment to clear the content.</span></span> <span data-ttu-id="a0e35-146">Файл находится в общей папке каждого пула Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0e35-146">The file is on the file share of each Lync Server 2013 pool.</span></span> <span data-ttu-id="a0e35-147">Если файл не отображается, создайте пустой файл с именем " \_ \_ нормализация номера телефона компании \_ \_Rules.txt".</span><span class="sxs-lookup"><span data-stu-id="a0e35-147">If the file is not present, then create an empty file named "Company\_Phone\_Number\_Normalization\_Rules.txt".</span></span>

5.  <span data-ttu-id="a0e35-148">Подождите несколько минут, пока все клиентские пулы смогут прочитать новые файлы.</span><span class="sxs-lookup"><span data-stu-id="a0e35-148">Wait several minutes for all Front End pools to read the new files.</span></span>

6.  <span data-ttu-id="a0e35-149">Выполните следующий командлет на каждом пуле Lync Server 2013 в развертывании:</span><span class="sxs-lookup"><span data-stu-id="a0e35-149">Run the following cmdlet on each Lync Server 2013 pool in your deployment:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="a0e35-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0e35-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

