---
title: 'Lync Server 2013: настройка паролей учетных записей проверки подлинности Kerberos'
description: 'Lync Server 2013: Настройка паролей для проверки подлинности учетной записи Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication account passwords
ms:assetid: b435f88e-4a77-4be7-b7e5-c17484303b74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412870(v=OCS.15)
ms:contentKeyID: 48185167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614b1411f9454c39843f4e69cabbfc3b02986e51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423975"
---
# <a name="setting-up-kerberos-authentication-account-passwords-in-lync-server-2013"></a><span data-ttu-id="b0f2b-103">Настройка паролей учетных записей проверки подлинности Kerberos в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0f2b-103">Setting up Kerberos authentication account passwords in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0f2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0f2b-104">

<span> </span></span></span>

<span data-ttu-id="b0f2b-105">_**Тема последнего изменения:** 2010-11-03_</span><span class="sxs-lookup"><span data-stu-id="b0f2b-105">_**Topic Last Modified:** 2010-11-03_</span></span>

<span data-ttu-id="b0f2b-106">После того как вы создадите объект компьютера для учетной записи проверки подлинности Kerberos, вы можете настроить пароль для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-106">After you create the computer object for the Kerberos authentication account, you can set up the password for the account.</span></span> <span data-ttu-id="b0f2b-107">Вы запускаете командлет Windows PowerShell для задания пароля учетной записи Kerberos на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-107">You run the Windows PowerShell cmdlet for setting the Kerberos account password on one server.</span></span> <span data-ttu-id="b0f2b-108">Вы можете установить пароль для объекта, созданного для проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-108">You can set the password on the object that you created for the Kerberos authentication.</span></span> <span data-ttu-id="b0f2b-109">Для пароля может быть задано известное значение, но по умолчанию используется случайный пароль.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-109">The password can be set to a known value, but by default is a random password.</span></span> <span data-ttu-id="b0f2b-110">Пароль доступен для всех источников проверки подлинности Kerberos, использующих эту учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-110">The password is available to all Kerberos authentication sources that use the account.</span></span> <span data-ttu-id="b0f2b-111">Вы можете использовать командлеты Windows PowerShell для настройки и управления паролями учетной записи Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-111">You use Windows PowerShell cmdlets to set up and manage Kerberos account passwords.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b0f2b-112">Объект учетной записи Kerberos является объектом компьютера, но использует параметр UserAccount для операций в командлетах Windows PowerShell, на которые указывают ссылки.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-112">The Kerberos account object is a computer object, but uses the UserAccount parameter for operations in the Windows PowerShell cmdlets that are referenced.</span></span> <span data-ttu-id="b0f2b-113">Обратите внимание, что это не ошибка, но предполагаемое поведение командлета при создании и обслуживании учетной записи Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b0f2b-113">Note that this is not a mistake, but the intended behavior of the cmdlet when used with the Kerberos account creation and maintenance.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b0f2b-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="b0f2b-114">In This Section</span></span>

  - [<span data-ttu-id="b0f2b-115">Установка пароля учетной записи Kerberos для проверки подлинности на сервере в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0f2b-115">Set a Kerberos authentication account password on a server in Lync Server 2013</span></span>](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)

  - [<span data-ttu-id="b0f2b-116">Синхронизация пароля учетной записи проверки подлинности Kerberos с IIS в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0f2b-116">Synchronize a Kerberos authentication account password to IIS in Lync Server 2013</span></span>](lync-server-2013-synchronize-a-kerberos-authentication-account-password-to-iis.md)

<span data-ttu-id="b0f2b-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0f2b-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

