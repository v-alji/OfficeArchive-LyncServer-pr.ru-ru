---
title: Отображение фотографий пользователей в Lync
description: Сведения о том, как отображаются фотографии пользователей в Lync.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: How user photos are displayed in Lync
ms:assetid: b44a364d-a1d2-4d45-b27a-b5f77775e233
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn783119(v=OCS.15)
ms:contentKeyID: 62835297
ms.date: 08/27/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12ea9e19b3965994c025659f1b2249c49ec32a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399421"
---
# <a name="how-user-photos-are-displayed-in-lync"></a><span data-ttu-id="1868f-103">Отображение фотографий пользователей в Lync</span><span class="sxs-lookup"><span data-stu-id="1868f-103">How user photos are displayed in Lync</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1868f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1868f-104">

<span> </span></span></span>

<span data-ttu-id="1868f-105">_**Тема последнего изменения:** 2014-08-25_</span><span class="sxs-lookup"><span data-stu-id="1868f-105">_**Topic Last Modified:** 2014-08-25_</span></span>

<span data-ttu-id="1868f-106">**Сводка:** Фотографии пользователей, отображаемые в клиенте Lync, могут различаться в зависимости от того, какой компонент Lync вы используете, например в ходе Конференции или в чате.</span><span class="sxs-lookup"><span data-stu-id="1868f-106">**Summary:** User photos displayed in Lync client can be different depending on which Lync feature you are using, such as when in a conference or an IM chat.</span></span>

<span data-ttu-id="1868f-107">В Lync 2010 появилась возможность включения фотографии с профилем Lync, который отображается для других пользователей Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-107">Lync 2010 introduced the ability to include a photo with your Lync profile that is displayed to other Lync users.</span></span> <span data-ttu-id="1868f-108">Вы также можете указать, нужно ли отображать фотографии для контактов в клиенте Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-108">You can also choose whether or not to display photos for your contacts in Lync client.</span></span> <span data-ttu-id="1868f-109">В Lync 2013 поддерживается поддержка фотографий высокого разрешения для пользователей.</span><span class="sxs-lookup"><span data-stu-id="1868f-109">In Lync 2013, support for high-resolution photos for users.</span></span> <span data-ttu-id="1868f-110">В этой статье объясняется, как клиент Lync получает и отображает фотографии пользователей, в которых хранятся изображения, ограничения для каждого источника изображения и способы использования фотографий пользователей различными службами Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-110">This topic describes how Lync client gets and displays user photos, where the images are stored, the limitations for each image source, and how user photos are used by different Lync services.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="1868f-111">Вопросы планирования</span><span class="sxs-lookup"><span data-stu-id="1868f-111">Planning considerations</span></span>

<span data-ttu-id="1868f-112">При планировании реализации поддержки фотографий пользователей следует руководствоваться описанной ниже процедурой.</span><span class="sxs-lookup"><span data-stu-id="1868f-112">You should consider the following when planning to implement support for user photos.</span></span>

  - <span data-ttu-id="1868f-113">Для поддержки фото в высоком разрешении требуется, чтобы почтовый ящик пользователя находился на сервере Exchange 2013, а учетная запись пользователя Lync — в пуле Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="1868f-113">High-definition user photo support requires that the user’s mailbox be located on Exchange 2013 and the Lync user account to be in Lync 2013 pool.</span></span>

  - <span data-ttu-id="1868f-114">Пользовательские фотографии High Definition поддерживаются только в среде, в которой используются как Lync Server 2013, так и Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1868f-114">High-definition user photos are supported only in an environment where both Lync Server 2013 and Exchange 2013 are used.</span></span>

  - <span data-ttu-id="1868f-115">Пользователи с почтовыми ящиками в Exchange 2010 всегда будут использовать атрибут **Фотоэскиз** из доменных служб Active Directory в качестве источника фотографии пользователя.</span><span class="sxs-lookup"><span data-stu-id="1868f-115">Users with Mailboxes on Exchange 2010 will always use the **thumbnailPhoto** attribute from AD DS as the source for their user photo.</span></span>

  - <span data-ttu-id="1868f-116">Пользовательская фотография, сохраненная в качестве атрибута **Фотоэскиз** из доменных служб Active Directory, не будет отображаться для внешних и Федеративных контактов.</span><span class="sxs-lookup"><span data-stu-id="1868f-116">A user photo stored as the **thumbnailPhoto** attribute from AD DS will not be displayed to external / federated contacts.</span></span>

  - <span data-ttu-id="1868f-117">Если фотографии контактов пользователей хранятся в доменных СЛУЖБах Active Directory, то размер используемого файла изображения ограничен 96 × 96 пикселей и размером файла 100 КБ.</span><span class="sxs-lookup"><span data-stu-id="1868f-117">If the photos for user contacts are stored in AD DS, the image file used is limited to 96×96 pixels and no more than 100 KB file size.</span></span>

  - <span data-ttu-id="1868f-118">Если связь между Lync Server и Exchange Server потеряна, будет отображаться **Фотоэскиз** с низким разрешением пользователя из доменных служб Active Directory и только для внутренних пользователей.</span><span class="sxs-lookup"><span data-stu-id="1868f-118">If connectivity between Lync Server and Exchange Server is lost, the user’s low resolution **thumbnailPhoto** from AD DS will be displayed, and to internal users only.</span></span>

  - <span data-ttu-id="1868f-119">Фотографии пользователей с высоким разрешением отображаются в собраниях Lync 2013, когда активный динамик не поддерживает видео.</span><span class="sxs-lookup"><span data-stu-id="1868f-119">High-resolution user photos are displayed in Lync 2013 meetings when an active speaker does not have video enabled.</span></span> <span data-ttu-id="1868f-120">Кроме того, если переместить указатель мыши на фотографию эскиз в галерее, будет отображаться фотография высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="1868f-120">Also, moving the mouse over thumbnail photo in the gallery will display the high-resolution photo.</span></span>

</div>

<div>

## <a name="user-photos-in-lync-2010"></a><span data-ttu-id="1868f-121">Фотографии пользователей в Lync 2010</span><span class="sxs-lookup"><span data-stu-id="1868f-121">User Photos in Lync 2010</span></span>

<span data-ttu-id="1868f-122">В клиенте Lync 2010 вы можете выбрать один из двух вариантов для отображения фотографии вашего профиля, **корпоративного изображения по умолчанию** и **отображения изображения с веб-адреса**.</span><span class="sxs-lookup"><span data-stu-id="1868f-122">In the Lync 2010 client, you can choose from two options to display a photo for your profile, **Default corporate picture** and **Show picture from a web address**.</span></span>

<div>

## <a name="default-corporate-picture"></a><span data-ttu-id="1868f-123">Корпоративный рисунок по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1868f-123">Default corporate picture</span></span>

<span data-ttu-id="1868f-124">Когда вы выбираете вариант **корпоративного аватара по умолчанию** , Lync получает фотографию, которая отображается для вас из доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-124">When you choose the **Default corporate picture** option, Lync gets the photo displayed for you from Active Directory Domain Services.</span></span> <span data-ttu-id="1868f-125">Используемое изображение — это изображение, определенное как значение атрибута **Фотоэскиз** в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-125">The image used is the image defined as the value for the **thumbnailPhoto** attribute in Active Directory Domain Services.</span></span> <span data-ttu-id="1868f-126">Это тот же файл, который используется в Exchange для отображения изображений в Outlook.</span><span class="sxs-lookup"><span data-stu-id="1868f-126">This is the same file that is used by Exchange to display images in Outlook.</span></span>

<span data-ttu-id="1868f-127">Ниже приведены рекомендации по использованию изображений из доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-127">Considerations for using images from Active Directory Domain Services include the following:</span></span>

  - <span data-ttu-id="1868f-128">Поддерживаются только изображения с измерениями размером до 96 пикселей на 96 пикселей.</span><span class="sxs-lookup"><span data-stu-id="1868f-128">Only images with dimensions up to 96 pixels by 96 pixels are supported.</span></span> <span data-ttu-id="1868f-129">Размер файла изображения ограничен до 100 КБ.</span><span class="sxs-lookup"><span data-stu-id="1868f-129">The file size for the image is limited to 100 KB.</span></span>

  - <span data-ttu-id="1868f-130">По умолчанию пользователи имеют возможность изменить изображение, используемое для атрибута **Фотоэскиз** , несмотря на то, что непосредственно с помощью клиента Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-130">By default, users are able to change the image used for the **thumbnailPhoto** attribute, though not directly through Lync client.</span></span> <span data-ttu-id="1868f-131">Вы можете отключить это с помощью доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-131">You can disable this through Active Directory Domain Services.</span></span>

  - <span data-ttu-id="1868f-132">Изображения, хранящиеся в доменных службах Active Directory, не отображаются для контактов, находящихся вне Организации, даже если они являются федеративными контактами.</span><span class="sxs-lookup"><span data-stu-id="1868f-132">Images stored in Active Directory Domain Services are not displayed to contacts external to your organization, even if they are federated contacts.</span></span>

  - <span data-ttu-id="1868f-133">В крупных организациях хранение и Извлечение изображений для большого количества пользователей может повлиять на размер и производительность базы данных доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-133">In large organizations, storing and retrieving the images for large numbers of users may impact the Active Directory Domain Services database size and performance.</span></span>

  - <span data-ttu-id="1868f-134">Ограниченные размеры изображения и размер файла означают, что могут использоваться только изображения с низким разрешением.</span><span class="sxs-lookup"><span data-stu-id="1868f-134">The limited image dimensions and file size mean that only low resolution images can be used.</span></span>

<div>

## <a name="how-users-manage-their-user-photos-in-active-directory-domain-services"></a><span data-ttu-id="1868f-135">Управление фотографиями пользователей в доменных службах Active Directory</span><span class="sxs-lookup"><span data-stu-id="1868f-135">How users manage their user photos in Active Directory Domain Services</span></span>

<span data-ttu-id="1868f-136">Пользователь не может изменить изображение, используемое в своем профиле доменных служб Active Directory прямо через клиент Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="1868f-136">User cannot change the image used in their Active Directory Domain Services profile directly through Lync 2010 client.</span></span> <span data-ttu-id="1868f-137">Для этого они могут использовать один из указанных ниже параметров, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="1868f-137">They can use one of the following options to do so, if available:</span></span>

  - <span data-ttu-id="1868f-138">**SharePoint Server**   Пользователи могут отправить фотографию на сайт SharePoint Server, а затем [настроить синхронизацию профилей в SharePoint](https://go.microsoft.com/fwlink/p/?linkid=507466) , чтобы синхронизировать фотографию с атрибутом **Фотоэскиз** в доменных службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-138">**SharePoint Server**   Users can upload a photo to ‘My Site’ on a SharePoint Server and then [configure profile synchronization in SharePoint](https://go.microsoft.com/fwlink/p/?linkid=507466) to synchronize the photo to the **thumbnailPhoto** attribute in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="1868f-139">**Фотография, сохраненная в общедоступном URL-адресе**   Пользователи могут настроить свою фотографию пользователя, указав общедоступный URL-адрес для изображения, которое они хотят использовать.</span><span class="sxs-lookup"><span data-stu-id="1868f-139">**Photo stored on publicly accessible URL**   Users can configure their user photo specifying a publicly accessible URL for the image that they want to use.</span></span> <span data-ttu-id="1868f-140">Изображение должно быть открыто для общего доступа без пароля.</span><span class="sxs-lookup"><span data-stu-id="1868f-140">The image must be publicly accessible without a password.</span></span> <span data-ttu-id="1868f-141">Изображение, хранящееся в указанном веб-адресе, передается другим пользователям с помощью категории карточки контакта в сведениях о присутствии.</span><span class="sxs-lookup"><span data-stu-id="1868f-141">The image stored at the specified web address is transferred to other users through the contact card category in the presence information.</span></span> <span data-ttu-id="1868f-142">Когда клиент Lync должен отобразить фотографию пользователя, он извлекает изображение с указанного веб-адреса.</span><span class="sxs-lookup"><span data-stu-id="1868f-142">When Lync client needs to display a user photo, it retrieves the image from the specified web address.</span></span>

  - <span data-ttu-id="1868f-143">**Командлеты Exchange 2010 для Windows PowerShell**   Администраторы могут запускать командлет [Import-RecipientDataProperty](https://go.microsoft.com/fwlink/p/?linkid=507468) в командной консоли Exchange 2010 для управления атрибутом **Фотоэскиз** .</span><span class="sxs-lookup"><span data-stu-id="1868f-143">**Exchange 2010 cmdlets for Windows PowerShell**   Administrators can run the [Import-RecipientDataProperty](https://go.microsoft.com/fwlink/p/?linkid=507468) cmdlet in the Exchange 2010 Management Shell in to manage the **thumbnailPhoto** attribute.</span></span> <span data-ttu-id="1868f-144">При импорте изображений с помощью командлетов Exchange 2010 размер файла ограничен 10 КБ.</span><span class="sxs-lookup"><span data-stu-id="1868f-144">When images are imported with Exchange 2010 cmdlets, the file size is limited to 10 KB.</span></span>

  - <span data-ttu-id="1868f-145">**Сторонние инструменты**   Пользователи могут отправлять собственное фото для атрибута **Фотоэскиз** .</span><span class="sxs-lookup"><span data-stu-id="1868f-145">**Third Party tools**   Users can upload only their own photo to for the **thumbnailPhoto** attribute.</span></span>

</div>

</div>

<div>

## <a name="show-a-picture-from-a-web-address"></a><span data-ttu-id="1868f-146">Отображение изображения с веб-адреса</span><span class="sxs-lookup"><span data-stu-id="1868f-146">Show a picture from a web address</span></span>

<span data-ttu-id="1868f-147">Если вы выбрали вариант **Показать рисунок с помощью веб-адреса** , Lync получает изображение по адресу, который вы ввели, и отображает его для фотографии пользователя в Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-147">When you choose the **Show a picture from a web address** option, Lync gets the image at the address you enter and displays it for your user photo in Lync.</span></span>

<span data-ttu-id="1868f-148">Ниже приведены рекомендации по использованию изображений с веб-адресом.</span><span class="sxs-lookup"><span data-stu-id="1868f-148">Considerations for using images from a web address include the following:</span></span>

  - <span data-ttu-id="1868f-149">Ограничения размера файлов определяются атрибутом **MaxPhotoSizeKB** в политике клиента, который определяется с помощью командлета [New-CsClientPolicy](https://go.microsoft.com/fwlink/p/?linkid=507463) .</span><span class="sxs-lookup"><span data-stu-id="1868f-149">File size limits are determined by the **MaxPhotoSizeKB** attribute in the client policy, defined with the [New-CsClientPolicy](https://go.microsoft.com/fwlink/p/?linkid=507463) cmdlet.</span></span> <span data-ttu-id="1868f-150">По умолчанию предельный размер составляет 30 КБ.</span><span class="sxs-lookup"><span data-stu-id="1868f-150">The default size limit is 30 KB.</span></span> <span data-ttu-id="1868f-151">Максимальное значение — 100 КБ.</span><span class="sxs-lookup"><span data-stu-id="1868f-151">The maximum value is 100 KB.</span></span> <span data-ttu-id="1868f-152">Разрешение изображения не ограничивается, но если вы попытаетесь использовать файл изображения, размер которого превышает предельный, он не будет загружен в клиенты Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-152">There is no restriction on the resolution of the image, but if you try to use an image file that exceeds the size limit it will not be downloaded to Lync clients.</span></span> <span data-ttu-id="1868f-153">Вы можете установить для этого параметра значение 0, чтобы отключить все фотографии пользователей в Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-153">You can set the value to 0 to disable all user photos from being used in Lync.</span></span>

  - <span data-ttu-id="1868f-154">Фотографии пользователей на веб-адресах можно просматривать с помощью внешних федеративных контактов.</span><span class="sxs-lookup"><span data-stu-id="1868f-154">User photos from a web address can be seen by external federated contacts.</span></span>

</div>

<div>

## <a name="managing-users-photo-with-client-policy-cmdlets"></a><span data-ttu-id="1868f-155">Управление фото пользователя с помощью командлетов клиентской политики</span><span class="sxs-lookup"><span data-stu-id="1868f-155">Managing user’s photo with Client Policy cmdlets</span></span>

<span data-ttu-id="1868f-156">В Lync Server 2010 параметры клиентской политики настраиваются с помощью командлетов CsClientPolicy.</span><span class="sxs-lookup"><span data-stu-id="1868f-156">In Lync Server 2010, client policy settings are configured with the CsClientPolicy cmdlets.</span></span> <span data-ttu-id="1868f-157">Настроенные параметры политики отправляются клиентам через стандартную подготовку.</span><span class="sxs-lookup"><span data-stu-id="1868f-157">The configured policy settings are sent to clients through in-band provisioning.</span></span> <span data-ttu-id="1868f-158">Два параметра командлетов CsClientPolicy, которые определяют пользовательский интерфейс фотографии, — **DisplayPhoto** и **MaxPhotoSizeKB**.</span><span class="sxs-lookup"><span data-stu-id="1868f-158">The two parameters of the CsClientPolicy cmdlets that determine the user photo experience are **DisplayPhoto** and **MaxPhotoSizeKB**.</span></span> <span data-ttu-id="1868f-159">Соответствующий параметр подготовки по стандарту для **DisplayPhoto** и **MaxPhotoSizeKB** называется " **фотоиспользование**".</span><span class="sxs-lookup"><span data-stu-id="1868f-159">The corresponding in-band provisioning parameter for **DisplayPhoto** and **MaxPhotoSizeKB** is named **PhotoUsage**.</span></span> <span data-ttu-id="1868f-160">Значения параметра " **фотоиспользование** " отправляются клиентам через **endpointConfiguration** **provisionGroup**.</span><span class="sxs-lookup"><span data-stu-id="1868f-160">Values for the **PhotoUsage** parameter are send to clients through the **endpointConfiguration** **provisionGroup**.</span></span> <span data-ttu-id="1868f-161">Для получения дополнительных сведений ознакомьтесь со статьей [Общие сведения о политиках клиентов и параметрах](https://go.microsoft.com/fwlink/?linkid=507470) .</span><span class="sxs-lookup"><span data-stu-id="1868f-161">See [Overview of Client Policies and Settings](https://go.microsoft.com/fwlink/?linkid=507470) for more information.</span></span>

<span data-ttu-id="1868f-162">Значение параметра **DisplayPhoto** определяет источник изображения фотографии пользователя.</span><span class="sxs-lookup"><span data-stu-id="1868f-162">The **DisplayPhoto** parameter value determines the source of the user's photo image.</span></span> <span data-ttu-id="1868f-163">Поддерживаемые значения приведены в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="1868f-163">The supported values are included in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1868f-164">Значение параметра DisplayPhoto</span><span class="sxs-lookup"><span data-stu-id="1868f-164">DisplayPhoto parameter value</span></span></th>
<th><span data-ttu-id="1868f-165">Источник изображения</span><span class="sxs-lookup"><span data-stu-id="1868f-165">Image source</span></span></th>
<th><span data-ttu-id="1868f-166">Параметры клиента Lync 2010</span><span class="sxs-lookup"><span data-stu-id="1868f-166">Lync 2010 client settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1868f-167">"Фотография"</span><span class="sxs-lookup"><span data-stu-id="1868f-167">NoPhoto</span></span></p></td>
<td><p><span data-ttu-id="1868f-168">нет</span><span class="sxs-lookup"><span data-stu-id="1868f-168">none</span></span></p></td>
<td><p><span data-ttu-id="1868f-169"><strong>Не показывать мою фотографию</strong></span><span class="sxs-lookup"><span data-stu-id="1868f-169"><strong>Do not show my picture</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1868f-170">PhotoFromADOnly</span><span class="sxs-lookup"><span data-stu-id="1868f-170">PhotoFromADOnly</span></span></p></td>
<td><p><span data-ttu-id="1868f-171">Active Directory</span><span class="sxs-lookup"><span data-stu-id="1868f-171">Active Directory</span></span></p></td>
<td><p><span data-ttu-id="1868f-172"><strong>Корпоративный рисунок по умолчанию</strong></span><span class="sxs-lookup"><span data-stu-id="1868f-172"><strong>Default corporate picture</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1868f-173">AllPhotos</span><span class="sxs-lookup"><span data-stu-id="1868f-173">AllPhotos</span></span></p></td>
<td><p><span data-ttu-id="1868f-174">Веб-адрес</span><span class="sxs-lookup"><span data-stu-id="1868f-174">Web address</span></span></p></td>
<td><p><span data-ttu-id="1868f-175"><strong>Отображение изображения с веб-адреса</strong></span><span class="sxs-lookup"><span data-stu-id="1868f-175"><strong>Show a picture from a web address</strong></span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="how-lync-2010-client-gets-photos"></a><span data-ttu-id="1868f-176">Как клиент Lync 2010 получает фотографии</span><span class="sxs-lookup"><span data-stu-id="1868f-176">How Lync 2010 client gets photos</span></span>

<span data-ttu-id="1868f-177">В Lync 2010 пользовательские фотографии на сервере управляются службой адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1868f-177">In Lync 2010, user photos are managed on the server by the Address Book Service.</span></span> <span data-ttu-id="1868f-178">Клиент Lync получает фотографии пользователей с помощью предварительного запроса службы веб-запроса адресной книги (ABWQ) на сервере, доступ к которому осуществляется с помощью веб-службы расширения списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="1868f-178">Lync client gets user photos by first querying the Address Book Web Query (ABWQ) service on the server, which is exposed through the Distribution List Expansion web service.</span></span> <span data-ttu-id="1868f-179">Клиент получает файл изображения, а затем копирует его в кэш пользователя, чтобы избежать загрузки изображения каждый раз, когда необходимо его отобразить.</span><span class="sxs-lookup"><span data-stu-id="1868f-179">The client receives the image file and then copies it to the user's cache to avoid downloading the image each time it needs to be displayed.</span></span> <span data-ttu-id="1868f-180">Значения атрибутов, возвращаемые из запроса, также хранятся в записи службы кэшированных адресных книг для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1868f-180">The attribute values returned from the query are also stored in the cached Address Book Service entry for the user.</span></span> <span data-ttu-id="1868f-181">Служба адресной книги удаляет все кэшированные изображения каждые 24 часа, что означает, что новые образы пользователей будут обновляться в кэше на сервере в течение 24 часов.</span><span class="sxs-lookup"><span data-stu-id="1868f-181">The Address Book Service deletes all cached images every 24 hours, which means that it can take up to 24 hours for new user images to be updated in the cache on the server.</span></span> <span data-ttu-id="1868f-182">Вы можете принудительно обновить кэш с помощью командлета [Update-CsAddressBook](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook) .</span><span class="sxs-lookup"><span data-stu-id="1868f-182">You can force an update to the cache by using the [Update-CsAddressBook](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook) cmdlet.</span></span>

<span data-ttu-id="1868f-183">Фотографии пользователей, включенные в состояние присутствия, также имеют связанное хэш-значение, используемое приложением Lync для определения того, доступно ли более новое изображение.</span><span class="sxs-lookup"><span data-stu-id="1868f-183">User photos included in Presence status also have an associated hash value that Lync client uses to determine whether there is a newer image available.</span></span> <span data-ttu-id="1868f-184">Клиент автоматически сообщает об изменениях файла изображения, используемого в состоянии присутствия.</span><span class="sxs-lookup"><span data-stu-id="1868f-184">The client is automatically notified of changes to the image file used in Presence status.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="1868f-185">Поскольку фотографии не хранятся в базе данных GalContacts. DB, Загрузка фотографий пользователя не зависит от параметра <STRONG>AddressBookAvailability</STRONG> политики клиента (<A href="https://go.microsoft.com/fwlink/p/?linkid=507508">Set-CsClientPolicy</A>).</span><span class="sxs-lookup"><span data-stu-id="1868f-185">Because photos are not stored in the GalContacts.db database, downloading user photos is not dependent on the <STRONG>AddressBookAvailability</STRONG> setting in the client policy (<A href="https://go.microsoft.com/fwlink/p/?linkid=507508">Set-CsClientPolicy</A>).</span></span>



</div>

<span data-ttu-id="1868f-186">Запрос к службе ABWQ включает следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="1868f-186">The query to the ABWQ service includes the following attributes:</span></span>

  - <span data-ttu-id="1868f-187">**Фотохэш**   Хэш-значение двоичных данных фотографии и используется для определения того, изменилось ли текущее фото.</span><span class="sxs-lookup"><span data-stu-id="1868f-187">**PhotoHash**   The hash value of the binary photo data, and is used to determine whether the current photo has changed.</span></span>

  - <span data-ttu-id="1868f-188">**PhotoRelPath**   Относительный путь к файлу изображения, хранящемуся на сервере.</span><span class="sxs-lookup"><span data-stu-id="1868f-188">**PhotoRelPath**   The relative path to the image file stored on the server.</span></span>

  - <span data-ttu-id="1868f-189">**Фоторазмер**   Размер файла изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="1868f-189">**PhotoSize**   The size of the image file, in bytes.</span></span>

  - <span data-ttu-id="1868f-190">**Метка времени**   Дата и время последнего скачивания файла изображения с сервера и его копирование в кэш клиента.</span><span class="sxs-lookup"><span data-stu-id="1868f-190">**TimeStamp**   The date and time at which the image file was last downloaded from the server and copied to the client cache.</span></span>

<span data-ttu-id="1868f-191">Затем, после получения файла изображения, клиент Lync 2010 сравнивает значения атрибутов, возвращенные из запроса, с использованием значений атрибутов, полученных клиентом из встроенной программы подготовки, чтобы выяснить, различаются ли они.</span><span class="sxs-lookup"><span data-stu-id="1868f-191">Next, after retrieving the image file, Lync 2010 client compares the attribute values returned from the query against the attribute values received by the client from in-band provisioning to see if they are different.</span></span> <span data-ttu-id="1868f-192">Если значения различаются, клиент извлекает файл изображения пользователя, выполнившего вход, с помощью HTTP-запроса GET.</span><span class="sxs-lookup"><span data-stu-id="1868f-192">If the values are different, the client retrieves the image file of the signed-in user with an HTTP GET request.</span></span>

<span data-ttu-id="1868f-193">Кроме того, клиент сверяет с сервером каждые 24 часа с момента создания кэшированной версии файла изображения для сравнения значения атрибута " **Фотохэш** " на сервере со значением на клиенте.</span><span class="sxs-lookup"><span data-stu-id="1868f-193">Additionally, the client checks with the server every 24 hours from the time at which the cached version of the image file was created to compare the value of the **PhotoHash** attribute on the server with the value on the client.</span></span> <span data-ttu-id="1868f-194">Если значения различаются, клиент знает, что файл изображения изменился.</span><span class="sxs-lookup"><span data-stu-id="1868f-194">If the values are different, the client knows that the image file has changed.</span></span> <span data-ttu-id="1868f-195">Чтобы получить обновленный файл изображения, клиент снова запрашивает службу ABWQ, чтобы обновить файл изображения в кэше клиента с помощью файла изображения на сервере, который также сбрасывает **метку времени** для файла в клиентском кэше.</span><span class="sxs-lookup"><span data-stu-id="1868f-195">To obtain the updated image file, the client again queries the ABWQ service to update the image file in the client cache with the image file on the server, which also resets the **TimeStamp** on the file in the client cache.</span></span>

<span data-ttu-id="1868f-196">Ниже приведен пример ответа на запрос к службе ABWQ:</span><span class="sxs-lookup"><span data-stu-id="1868f-196">The following is an example response to a query to the ABWQ service:</span></span>
```xml
    <Attribute>
              <Name>PhotoRelPath</Name>
              <Value>efa6096aed2746cb9ab2037f7dbdde9d.f2eeeb5946db54a7aa607ecd3ae09d
              95.photo</Value>
              <Values xmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" i:nil="true" />
    </Attribute>
    <Attribute>
              <Name>PhotoHash</Name>
              <Value>f2eeeb5946db54a7aa607ecd3ae09d95</Value>
              <Values xmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" i:nil="true" />
    </Attribute>
    <Attribute>
         <Name>PhotoSize</Name>
         <Value>4620</Value>
         <Valuesxmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
    i:nil="true" />
    </Attribute>
```

</div>

</div>

<div>

## <a name="user-photos-in-lync-2013"></a><span data-ttu-id="1868f-197">Фотографии пользователей в Lync 2013</span><span class="sxs-lookup"><span data-stu-id="1868f-197">User photos in Lync 2013</span></span>

<span data-ttu-id="1868f-198">В Lync 2013 добавлена поддержка изображений с высоким разрешением для фотографий пользователей.</span><span class="sxs-lookup"><span data-stu-id="1868f-198">Lync 2013 introduced support for high-resolution images for user photos.</span></span> <span data-ttu-id="1868f-199">В Lync 2013 также поддерживается хранение фотографий пользователей в почтовом ящике пользователя на сервере Exchange 2013, в результате чего удаляются разрешения и ограничения размеров, представленные в Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="1868f-199">Lync 2013 also includes support for storing user photos in the user's mailbox on Exchange 2013, which removes the image resolution and size limitations present in Lync 2010.</span></span> <span data-ttu-id="1868f-200">Фотографии пользователей в Lync 2013 могут иметь размер до 648 пикселей на 648 пикселов размером до 20 МБ.</span><span class="sxs-lookup"><span data-stu-id="1868f-200">User photos in Lync 2013 can be up to 648 pixels by 648 pixels with a file size of up to 20 MB.</span></span> <span data-ttu-id="1868f-201">Фотографии высокого разрешения в Lync 2013 должны находиться в почтовом ящике пользователя на сервере Exchange 2013 и поддерживаются только в клиенте Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="1868f-201">High-resolution photos in Lync 2013 must be located in the user's mailbox on Exchange 2013, and are supported only with Lync 2013 client.</span></span> <span data-ttu-id="1868f-202">Интеграция с Exchange использует преимущества новой платформы авторизации, включенной в версии 2013 для Lync, Exchange и SharePoint, именуемые OAuth.</span><span class="sxs-lookup"><span data-stu-id="1868f-202">This integration with Exchange takes advantage of the new authorization framework included in the 2013 versions of Lync, Exchange, and SharePoint called Oauth.</span></span>

<span data-ttu-id="1868f-203">Если в развертывании не используется Exchange 2013, поддержка пользовательских фотографий будет такой же, как в Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="1868f-203">If Exchange 2013 is not used in your deployment, support for user photos is the same as with Lync 2010.</span></span> <span data-ttu-id="1868f-204">Однако параметры пользователя для выбора фотографии отличаются в клиенте Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="1868f-204">However, the user options to choose the photo to use are different in Lync 2013 client.</span></span> <span data-ttu-id="1868f-205">В клиенте Lync 2013 пользователи могут выбрать либо **скрыть мою фотографию** , либо **Показать мою фотографию**.</span><span class="sxs-lookup"><span data-stu-id="1868f-205">In Lync 2013 client, users can select either **Hide my picture** or **Show my picture**.</span></span> <span data-ttu-id="1868f-206">Параметр **Показать рисунок с веб-сайта** по умолчанию недоступен, но его можно включить, назначая политику клиента.</span><span class="sxs-lookup"><span data-stu-id="1868f-206">The option **Show a picture from a website** is not available by default, but can be enabled by assigning a client policy.</span></span>

<div>

## <a name="hide-my-picture"></a><span data-ttu-id="1868f-207">Скрыть мою фотографию</span><span class="sxs-lookup"><span data-stu-id="1868f-207">Hide my picture</span></span>

<span data-ttu-id="1868f-208">Параметры фотографий пользователей находятся в диалоговом окне " **Параметры** " в Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="1868f-208">Settings for user photos are on the **Options** dialog in Lync 2013.</span></span> <span data-ttu-id="1868f-209">Когда вы выбираете команду **скрыть мою** фотографию, в клиенте Lync не отображаются фотографии пользователей, но ваши фото по-прежнему отображаются в карточке контакта и вне Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-209">When you choose **Hide my picture**, no user photo is displayed for you in Lync client, but your photo is still displayed on your contact card and outside of Lync.</span></span>

</div>

<div>

## <a name="show-my-picture"></a><span data-ttu-id="1868f-210">Показать мою фотографию</span><span class="sxs-lookup"><span data-stu-id="1868f-210">Show my picture</span></span>

<span data-ttu-id="1868f-211">Если вы выберете параметр **Показать мои рисунки** , ваша фотография пользователя будет отображаться в клиенте Lync и другим пользователям в беседах Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-211">When you choose the **Show my picture** option, your user photo is displayed in your Lync client and to other users in Lync conversations.</span></span> <span data-ttu-id="1868f-212">Используется изображение, которое хранится в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-212">The image used is the one stored in AD DS.</span></span>

</div>

<div>

## <a name="show-a-picture-from-a-website"></a><span data-ttu-id="1868f-213">Показать фотографию с веб-сайта</span><span class="sxs-lookup"><span data-stu-id="1868f-213">Show a picture from a website</span></span>

<span data-ttu-id="1868f-214">Параметр **Показать рисунок с веб-сайта** становится доступен в Lync 2013 после того, как политика клиента настроена на ее включение.</span><span class="sxs-lookup"><span data-stu-id="1868f-214">The **Show picture from a website** option becomes available in Lync 2013 after a client policy is set to enable it.</span></span> <span data-ttu-id="1868f-215">Версия клиента должна быть более новой, чем 15.0.4535.1002, которая устанавливается вместе с [накопительными обновлениями Lync: ноябрь 2013](https://go.microsoft.com/fwlink/p/?linkid=509908)г.</span><span class="sxs-lookup"><span data-stu-id="1868f-215">The client version must be newer than 15.0.4535.1002, which is installed with the [Lync Cumulative Updates: November 2013](https://go.microsoft.com/fwlink/p/?linkid=509908).</span></span> <span data-ttu-id="1868f-216">Пользователям может потребоваться выйти из программы, а затем снова войти в систему, чтобы увидеть изменения в клиенте.</span><span class="sxs-lookup"><span data-stu-id="1868f-216">Users may need to log out and then back in again to see the changes in the client.</span></span>

<span data-ttu-id="1868f-217">Вы можете настроить политику клиента так, чтобы она **отображалась на веб-сайте** , запустив политику [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1868f-217">You can set the client policy to enable to **Show picture from a website** setting by running the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) policy in the Lync Server Management Shell.</span></span> <span data-ttu-id="1868f-218">В следующем примере командлетов показано, как настроить политику глобально для всех пользователей в развертывании:</span><span class="sxs-lookup"><span data-stu-id="1868f-218">The following example cmdlets demonstrate how to set the policy globally for all users in your deployment:</span></span>

   ```powershell
    $pe=New-CsClientPolicyEntry -Name EnablePresencePhotoOptions -Value True
   ```

   ```powershell
    $po=Get-CsClientPolicy -Identity Global
   ```

   ```powershell
    $po.PolicyEntry.Add($pe)
   ```

   ```powershell
    Set-CsClientPolicy -Instance $po
   ```


<span data-ttu-id="1868f-219">При загрузке изображения в почтовый ящик пользователя Exchange автоматически создает более низкую версию изображения, которую можно использовать в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="1868f-219">When an image is uploaded to the user’s mailbox, Exchange automatically creates a lower resolution version of the image which can be used in client applications.</span></span> <span data-ttu-id="1868f-220">Фотография пользователя также обновлена в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-220">The user photo is also updated in AD DS.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="1868f-221">При обновлении файла изображения в доменных СЛУЖБах Active Directory создается и используется для Фотоэскиз в AD DS изображение пикселя 48 x 48.</span><span class="sxs-lookup"><span data-stu-id="1868f-221">When an image file is updated in AD DS, a 48 x 48 pixel image is created and used for the thumbnailPhoto in AD DS.</span></span> <span data-ttu-id="1868f-222">Все существующие изображения будут заменены.</span><span class="sxs-lookup"><span data-stu-id="1868f-222">Any existing image is replaced.</span></span> <span data-ttu-id="1868f-223">Таким образом, если вы добавили в AD DS изображение 96 x 96, оно будет заменено новым образом 48 x 48.</span><span class="sxs-lookup"><span data-stu-id="1868f-223">So if you added a 96 x 96 image to AD DS, it will be overwritten with the new 48 x 48 image.</span></span> <span data-ttu-id="1868f-224">Это важно только в том случае, если у вас есть пользователи в вашей среде с помощью клиентов Lync 2010, так как эти клиенты будут получать фотографии пользователей из доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1868f-224">This is only important is you have users in your environment using Lync 2010 clients, as those clients will obtain user photos from AD DS.</span></span> <span data-ttu-id="1868f-225">Вы можете импортировать изображения пикселов 96 x 96 пикселей, чтобы заменить созданные AD DS, если у вас есть клиенты Lync 2010 в своей организации.</span><span class="sxs-lookup"><span data-stu-id="1868f-225">You can import 96 x 96 pixel images to replace the ones created by AD DS if you have Lync 2010 clients in your organization.</span></span>



</div>

</div>

<div>

## <a name="user-photo-support-in-lync-2013"></a><span data-ttu-id="1868f-226">Поддержка Фото пользователей в Lync 2013</span><span class="sxs-lookup"><span data-stu-id="1868f-226">User photo support in Lync 2013</span></span>

<span data-ttu-id="1868f-227">В Lync 2013 для пользовательских фотографий поддерживаются три разрешения изображений, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1868f-227">In Lync 2013, three image resolutions are supported for user photos as described in the following table.</span></span> <span data-ttu-id="1868f-228">Используемое изображение определяется параметром клиентской политики, назначенным пользователям Lync.</span><span class="sxs-lookup"><span data-stu-id="1868f-228">The image that is used is determined by the client policy setting assigned to Lync users.</span></span> <span data-ttu-id="1868f-229">Дополнительные сведения можно найти в разделе "Управление фото пользователя с помощью командлетов клиентской политики".</span><span class="sxs-lookup"><span data-stu-id="1868f-229">See “Managing user’s photo with Client Policy cmdlets” in this topic for more information.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1868f-230">Разрешение изображения (в пикселях)</span><span class="sxs-lookup"><span data-stu-id="1868f-230">Image resolution (pixels)</span></span></th>
<th><span data-ttu-id="1868f-231">Приложение</span><span class="sxs-lookup"><span data-stu-id="1868f-231">Application</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1868f-232">48 x 48</span><span class="sxs-lookup"><span data-stu-id="1868f-232">48 x 48</span></span></p></td>
<td><p><span data-ttu-id="1868f-233">Используется, если не выбрано изображение с более высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="1868f-233">Used if no higher resolution image is selected</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1868f-234">96 x 96</span><span class="sxs-lookup"><span data-stu-id="1868f-234">96 x 96</span></span></p></td>
<td><p><span data-ttu-id="1868f-235">Используется в Outlook Web App и Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="1868f-235">Used in Outlook Web App and Outlook 2013</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1868f-236">648 x 648</span><span class="sxs-lookup"><span data-stu-id="1868f-236">648 x 648</span></span></p></td>
<td><p><span data-ttu-id="1868f-237">Используется в классическом клиенте Lync 2013 и веб-приложении Lync 2013</span><span class="sxs-lookup"><span data-stu-id="1868f-237">Used in Lync 2013 desktop client and Lync 2013 Web App</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1868f-238">Любой пользователь с включенным в Exchange 2013 почтовым ящиком может загрузить другое изображение, включая фотографии высокого разрешения, с помощью Outlook Web Access или параметров клиента Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="1868f-238">Any user with a mailbox enabled in Exchange 2013 can upload a different image, including high-resolution photos, through Outlook Web Access or Lync 2013 client options.</span></span> <span data-ttu-id="1868f-239">Для используемых изображений рекомендуются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1868f-239">The recommended settings for images used include:</span></span>

  - <span data-ttu-id="1868f-240">**Разрешение изображения**   648 на 648 пикселей</span><span class="sxs-lookup"><span data-stu-id="1868f-240">**Image Resolution**   648 by 648 pixels</span></span>

  - <span data-ttu-id="1868f-241">**Глубина цвета**   24-разрядная</span><span class="sxs-lookup"><span data-stu-id="1868f-241">**Color Depth**   24-bit</span></span>

  - <span data-ttu-id="1868f-242">**Размер файла изображения**   до 20 МБ</span><span class="sxs-lookup"><span data-stu-id="1868f-242">**Image file size**   up to 20 MB</span></span>

  - <span data-ttu-id="1868f-243">**Формат файла**   JPEG</span><span class="sxs-lookup"><span data-stu-id="1868f-243">**File format**   JPEG</span></span>

<span data-ttu-id="1868f-244">Типичный 24-битный формат JPEG, 648 пикселей на 648 пикселей, имеет размер файла около 240 КБ, поэтому для каждых 4 фотографий пользователей потребуется 1 МБАЙТ свободного места.</span><span class="sxs-lookup"><span data-stu-id="1868f-244">A typical 24-bit JPEG image that is 648 pixels by 648 pixels has a file size of about 240 KB, so 1 MB of storage space is needed for every 4 user photos.</span></span>

<span data-ttu-id="1868f-245"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1868f-245"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

