---
title: 'Lync Server 2013: компоненты, используемые для отправки группового звонка'
description: 'Lync Server 2013: компоненты, используемые при отправке группового звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398524"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="94d66-103">Компоненты, используемые для отправки группового звонка в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="94d66-103">Components used by Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="94d66-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="94d66-104">

<span> </span></span></span>

<span data-ttu-id="94d66-105">_**Тема последнего изменения:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="94d66-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="94d66-106">Отправка группового звонка автоматически разворачивается при развертывании корпоративной голосовой связи и приложения для приостановки звонков.</span><span class="sxs-lookup"><span data-stu-id="94d66-106">Group Call Pickup is automatically deployed when you deploy Enterprise Voice and the Call Park application.</span></span> <span data-ttu-id="94d66-107">Вы включаете функцию отправки группового звонка, настраивая в таблице на приостановку соединения различные диапазоны номеров, обозначенные как номера групп для отправки звонков, а затем назначая пользователям доступ к группам для отправки звонков и обеспечивая пользователям возможность раскладки группового звонка.</span><span class="sxs-lookup"><span data-stu-id="94d66-107">You enable Group Call Pickup by configuring the Call Park orbit table with separate ranges of numbers designated as call pickup group numbers, and then by assigning users to call pickup groups and enabling the users for Group Call Pickup.</span></span> <span data-ttu-id="94d66-108">Следующие компоненты Lync Server поддерживают раскладки групповых звонков.</span><span class="sxs-lookup"><span data-stu-id="94d66-108">The following Lync Server components support Group Call Pickup:</span></span>

  - <span data-ttu-id="94d66-109">**Служба приложений**   Служба приложений предоставляет платформу для развертывания, размещения и управления едиными приложениями для обмена информацией, например с помощью приложения для приостановки звонков.</span><span class="sxs-lookup"><span data-stu-id="94d66-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="94d66-110">Служба приложений устанавливается автоматически на каждый сервер переднего плана в пуле переднего плана и на каждом сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="94d66-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="94d66-111">**Приложение для приостановки звонков**   Приложение для парковки звонков — это одно из Объединенных приложений для обмена данными, размещенных в службе приложений.</span><span class="sxs-lookup"><span data-stu-id="94d66-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="94d66-112">Отправка группового звонка осуществляется на основе заявления на приостановку звонков.</span><span class="sxs-lookup"><span data-stu-id="94d66-112">Group Call Pickup is based on the Call Park application.</span></span>

  - <span data-ttu-id="94d66-113">**Командная консоль Lync Server Management Shell**   Вы используете командную консоль Lync Server для управления группами раскладки группового звонка.</span><span class="sxs-lookup"><span data-stu-id="94d66-113">**Lync Server Management Shell**   You use Lync Server Management Shell to manage Group Call Pickup groups.</span></span>

  - <span data-ttu-id="94d66-114">**Инструмент "набор ресурсов SEFAUtil**   "   Вы используете вспомогательную служебную программу активации компонентов (SEFAUtil), чтобы назначить пользователей группе для отправки звонков, а также включить или отключить функцию отправки звонков для пользователей.</span><span class="sxs-lookup"><span data-stu-id="94d66-114">**SEFAUtil resource kit tool**   You use the secondary extension feature activation utility (SEFAUtil) to assign users to a call pickup group and to enable or disable call pickup for users.</span></span>

<span data-ttu-id="94d66-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="94d66-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

