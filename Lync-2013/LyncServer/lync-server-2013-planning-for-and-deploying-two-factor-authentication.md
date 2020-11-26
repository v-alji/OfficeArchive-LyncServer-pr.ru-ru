---
title: 'Lync Server 2013: планирование и развертывание двухфакторной проверки подлинности'
description: 'Lync Server 2013: планирование и развертывание двухфакторной проверки подлинности.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for and deploying two-factor authentication
ms:assetid: 442a88df-ebc2-4335-9c59-0ce1adc1471e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308563(v=OCS.15)
ms:contentKeyID: 54973686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1e04fa7a0c1184152328882a7c7b4bea8e42ec0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437121"
---
# <a name="two-factor-authentication-in-lync-server-2013"></a><span data-ttu-id="df71d-103">Двухфакторная проверка подлинности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df71d-103">Two-factor authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df71d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df71d-104">

<span> </span></span></span>

<span data-ttu-id="df71d-105">_**Тема последнего изменения:** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="df71d-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="df71d-106">Двухфакторная проверка подлинности обеспечивает повышенную безопасность, требуя пользователей отвечать на два условия проверки подлинности: сочетание имени пользователя и пароля и маркер или сертификат.</span><span class="sxs-lookup"><span data-stu-id="df71d-106">Two-factor authentication provides improved security by requiring users to meet two authentication criteria: a user name/password combination and a token or certificate.</span></span> <span data-ttu-id="df71d-107">Это сочетание иногда называют "то, что знаешь" и "то, что имеешь".</span><span class="sxs-lookup"><span data-stu-id="df71d-107">This is also known as “something you have, something you know.”</span></span> <span data-ttu-id="df71d-108">Типичным примером двухфакторной проверки подлинности с помощью сертификата может послужить использование смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="df71d-108">A typical example of two-factor authentication with a certificate is the use of smart cards.</span></span> <span data-ttu-id="df71d-109">Смарт-карта включает в себя сертификат, связанный с учетной записью пользователя, и проверяется с помощью информации о пользователе и сертификате, хранящейся на сервере.</span><span class="sxs-lookup"><span data-stu-id="df71d-109">A smart card contains a certificate associated with the user account, and can be validated against user and certificate information stored on a server.</span></span> <span data-ttu-id="df71d-110">Сервер сравнивает информацию о пользователе (имя пользователя и пароль) с представленным сертификатом, в результате чего происходит проверка учетных данных и определяется подлинность пользователя.</span><span class="sxs-lookup"><span data-stu-id="df71d-110">By comparing the user information (user name and password) to the certificate provided, the server validates the credentials and authenticates the user.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="df71d-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="df71d-111">In This Section</span></span>

[<span data-ttu-id="df71d-112">Планирование двухфакторной проверки подлинности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df71d-112">Planning for two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-planning-for-two-factor-authentication.md)

[<span data-ttu-id="df71d-113">Настройка двухфакторной проверки подлинности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df71d-113">Configuring two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-configuring-two-factor-authentication.md)

[<span data-ttu-id="df71d-114">Использование двухфакторной проверки подлинности в клиенте Lync и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df71d-114">Using two-factor authentication with Lync client and Lync Server 2013</span></span>](lync-server-2013-using-two-factor-authentication-with-lync-client.md)

<span data-ttu-id="df71d-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df71d-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

