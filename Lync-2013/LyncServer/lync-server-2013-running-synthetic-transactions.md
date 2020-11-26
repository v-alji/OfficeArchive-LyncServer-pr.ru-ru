---
title: 'Lync Server 2013: выполнение искусственных транзакций'
description: 'Lync Server 2013: выполнение виртуальных транзакций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running synthetic transactions
ms:assetid: 2b56c7bd-8956-4fa1-8232-1876b959b258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720911(v=OCS.15)
ms:contentKeyID: 63969593
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26b0c26024f361dac196319eaf849c1847033cc9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442182"
---
# <a name="running-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="bba5a-103">Выполнение виртуальных транзакций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bba5a-103">Running synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bba5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bba5a-104">

<span> </span></span></span>

<span data-ttu-id="bba5a-105">_**Тема последнего изменения:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="bba5a-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="bba5a-106">Синтетические транзакции обычно выполняются двумя способами.</span><span class="sxs-lookup"><span data-stu-id="bba5a-106">Synthetic transactions are typically conducted in two ways.</span></span> <span data-ttu-id="bba5a-107">Вы можете использовать командлеты CsHealthMonitoringConfiguration, чтобы настроить пользователей для каждого из своих пулов регистраторов.</span><span class="sxs-lookup"><span data-stu-id="bba5a-107">You can use the CsHealthMonitoringConfiguration cmdlets to set up test users for each of their Registrar pools.</span></span> <span data-ttu-id="bba5a-108">Эти тестовые пользователи — это пары пользователей, которые были предварительно настроены для использования с искусственными транзакциями.</span><span class="sxs-lookup"><span data-stu-id="bba5a-108">These test users are a pair of users who were preconfigured for use with synthetic transactions.</span></span> <span data-ttu-id="bba5a-109">(Как правило, они являются тестовыми учетными записями, а не учетными записями, принадлежащими реальным пользователям.) При использовании тестовых пользователей, настроенных для пула, вы можете выполнить искусственную транзакцию для этого пула, не задавая удостоверения (и учетные данные для) учетных записей пользователей, участвующих в тестировании.</span><span class="sxs-lookup"><span data-stu-id="bba5a-109">(Typically these are test accounts and not accounts that belong to actual users.) With test users configured for a pool, you can run a synthetic transaction against that pool without having to specify the identities of (and supply the credentials for) the user accounts involved in the test.</span></span>

<span data-ttu-id="bba5a-110">Вы также можете выполнить искусственную транзакцию с помощью реальных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="bba5a-110">Or, you can run a synthetic transaction by using actual user accounts.</span></span> <span data-ttu-id="bba5a-111">Например, если два пользователя не могут обмениваться мгновенными сообщениями, вы можете выполнить искусственную транзакцию с помощью этих двух учетных записей пользователей (а не для пары тестовых учетных записей), а затем попробовать диагностировать и устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="bba5a-111">For example, if two users cannot exchange instant messages, you could run a synthetic transaction using those two user accounts (instead of a pair of test accounts), and then try to diagnose and resolve the issue.</span></span> <span data-ttu-id="bba5a-112">Если вы решите провести искусственную транзакцию с использованием фактических учетных записей пользователей, необходимо указать имена для входа и пароли для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="bba5a-112">If you decide to conduct a synthetic transaction using actual user accounts, you must supply the logon names and passwords for each user.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="bba5a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="bba5a-113">See Also</span></span>


[<span data-ttu-id="bba5a-114">Настройка пользователей и параметров конфигурации для проверки узла-наблюдателя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bba5a-114">Configuring watcher node test users and configuration settings in Lync Server 2013</span></span>](lync-server-2013-configuring-watcher-node-test-users-and-configuration-settings.md)  
[<span data-ttu-id="bba5a-115">Специальные инструкции по настройке для виртуальных транзакций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bba5a-115">Special setup instructions for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md)  
  

<span data-ttu-id="bba5a-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bba5a-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

