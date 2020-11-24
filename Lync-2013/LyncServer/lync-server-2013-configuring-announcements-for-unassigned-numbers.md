---
title: 'Lync Server 2013: настройка объявлений для неназначенных номеров'
description: 'Lync Server 2013: Настройка объявлений для неназначенных номеров.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring announcements for unassigned numbers
ms:assetid: 45633dd3-78de-4934-867e-33969fc25368
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425944(v=OCS.15)
ms:contentKeyID: 48184035
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16ab636f0c6157118a00d5e46521555086c5e520
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399175"
---
# <a name="configuring-announcements-for-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="97a26-103">Настройка объявлений для неназначенных номеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97a26-103">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97a26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97a26-104">

<span> </span></span></span>

<span data-ttu-id="97a26-105">_**Тема последнего изменения:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="97a26-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="97a26-106">Приложение извещения — это функция голосовой связи, позволяющая настроить действия, которые необходимо выполнить для звонков на неназначенные расширения (расширения, которые являются допустимыми для вашей организации, но не назначены для человека или телефона).</span><span class="sxs-lookup"><span data-stu-id="97a26-106">The Announcement application is an Enterprise Voice feature that enables you to configure what happens to calls to unassigned extensions (extensions that are valid for your organization, but are not assigned to a person or a phone).</span></span> <span data-ttu-id="97a26-107">Например, можно настроить эту функцию таким образом, чтобы при выполнении вызовов на неприсвоенные номера воспроизводилось сообщение и/или эти вызовы передавались на другое назначение.</span><span class="sxs-lookup"><span data-stu-id="97a26-107">For example, you can configure calls to unassigned numbers to play a message, or to be transferred to a different destination, or both.</span></span>

<span data-ttu-id="97a26-108">Приложение извещения устанавливается как функция приложения группы ответа на сервере переднего плана или стандартном сервере Standard Edition при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="97a26-108">The Announcement application is installed as a feature of Response Group application on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="97a26-109">Для настройки оповещений следует загрузить аудиофайлы или настроить преобразование текста в речь и сконфигурировать таблицу неприсвоенных номеров.</span><span class="sxs-lookup"><span data-stu-id="97a26-109">You need to configure Announcements by uploading your audio files or by configuring text-to-speech (TTS) and configuring the unassigned number table.</span></span>

<span data-ttu-id="97a26-110">В этом разделе рассказывается о настройке объявлений Lync Server.</span><span class="sxs-lookup"><span data-stu-id="97a26-110">This section guides you through the configuration of Lync Server Announcements.</span></span> <span data-ttu-id="97a26-111">Предполагается, что вы уже прочитали разделы планирования, связанные с объявлениями и развернули сервер Enterprise Edition или сервер Standard Edition с корпоративной голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="97a26-111">It assumes that you have already read the planning sections related to Announcements and deployed an Enterprise Edition server or a Standard Edition server with Enterprise Voice.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="97a26-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="97a26-112">In This Section</span></span>

  - [<span data-ttu-id="97a26-113">Необходимые условия и роли для настройки объявлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97a26-113">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>](lync-server-2013-announcement-configuration-prerequisites-and-roles.md)

  - [<span data-ttu-id="97a26-114">Процесс развертывания приложения для объявлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97a26-114">Deployment process for the Announcement application in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-the-announcement-application.md)

  - [<span data-ttu-id="97a26-115">Создание объявления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97a26-115">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="97a26-116">Настройка таблицы неназначенных номеров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97a26-116">Configure the unassigned number table in Lync Server 2013</span></span>](lync-server-2013-configure-the-unassigned-number-table.md)

  - [<span data-ttu-id="97a26-117">Необязательно Проверка развертывания объявления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97a26-117">(Optional) Verify Announcement deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-announcement-deployment.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="97a26-118">См. также</span><span class="sxs-lookup"><span data-stu-id="97a26-118">See Also</span></span>


[<span data-ttu-id="97a26-119">Планирование функций управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97a26-119">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="97a26-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97a26-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

