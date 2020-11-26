---
title: 'Lync Server 2013: проверка нормализации номера голоса и маршрутизации'
description: 'Lync Server 2013: проверка нормализации номера голосовой связи и маршрутизации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating voice number normalization and routing
ms:assetid: a6a825c7-6928-4e80-b7e9-803b7f7ebd13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720922(v=OCS.15)
ms:contentKeyID: 63969633
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f28f679cbb991bdb90362eb61c9c7b68879791e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438626"
---
# <a name="validating-voice-number-normalization-and-routing-in-lync-server-2013"></a><span data-ttu-id="a78fa-103">Проверка нормализации и маршрутизации номера голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a78fa-103">Validating voice number normalization and routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a78fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a78fa-104">

<span> </span></span></span>

<span data-ttu-id="a78fa-105">_**Тема последнего изменения:** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="a78fa-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="a78fa-106">Правильная нормализация номеров и маршрутизация очень важна для работы корпоративной голосовой среды.</span><span class="sxs-lookup"><span data-stu-id="a78fa-106">Correct number normalization and routing is very important for functional Enterprise Voice environment.</span></span> <span data-ttu-id="a78fa-107">Особенно при миграции из АТС в автономную среду Lync, одной из клавиш для успешной миграции является отображение и документирование всех существующих правил набора номера, а также создание соответствующих правил нормализации, политик голосовой связи, использования и маршрутов по телефону.</span><span class="sxs-lookup"><span data-stu-id="a78fa-107">Especially during migrations from private branch exchange (PBX) to stand-alone Lync Server environment, one of the keys to successful migration is to reveal and document all existing dialing rules, and create appropriate normalization rules, voice policies, phone usages and routes.</span></span>

<span data-ttu-id="a78fa-108">Проверка нормализации номера и маршрутизации важна не только при миграции, но и во время нормальной и стабильной работы системы.</span><span class="sxs-lookup"><span data-stu-id="a78fa-108">Validating number normalization and routing is important not only during migrations but also during normal, stable operation of the system.</span></span>

<span data-ttu-id="a78fa-109">Мы рекомендуем использовать эту проверку ежедневно с помощью панели управления Lync Server, начиная с разработки надежного набора тестовых случаев для текущего набора правил нормализации, которые были опубликованы в глобальных параметрах Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a78fa-109">We recommend conducting this validation daily by using the Lync Server Control Panel, starting with developing a robust set of test cases against the current set of normalization rules that were published in the Lync Server global settings.</span></span> <span data-ttu-id="a78fa-110">Эти тестовые случаи следует запускать ежедневно для выбора ненужных изменений, внесенных в абонентскую группу.</span><span class="sxs-lookup"><span data-stu-id="a78fa-110">These test cases should be run daily to highlight any unwanted changes that were made and committed to the dial plan.</span></span>

<span data-ttu-id="a78fa-111">С помощью панели управления Lync Server вы также можете наглядно представить, протестировать, изменить, заархивировать и обмениваться сведениями о маршрутизации голосовой связи и изменить правила нормализации голосовых номеров, абонентские группы, политику голосовой связи и маршруты.</span><span class="sxs-lookup"><span data-stu-id="a78fa-111">Lync Server Control Panel also helps you visualize, test, change, archive, and share configuration information about voice routing and in changing Enterprise Voice number normalization rules, dial plans, voice policy, and routes.</span></span> <span data-ttu-id="a78fa-112">У него есть дополнительные возможности для следующих действий:</span><span class="sxs-lookup"><span data-stu-id="a78fa-112">It has additional features for doing the following:</span></span>

  - <span data-ttu-id="a78fa-113">Экспорт и импорт и архивация данных голосовой маршрутизации между системами.</span><span class="sxs-lookup"><span data-stu-id="a78fa-113">Exporting and importing or backing up voice routing data between systems.</span></span>

  - <span data-ttu-id="a78fa-114">Тестирование изменений конфигурации перед их загрузкой в действующую систему.</span><span class="sxs-lookup"><span data-stu-id="a78fa-114">Testing configuration changes before uploading them to a live system.</span></span>

  - <span data-ttu-id="a78fa-115">Создание и выполнение тестовых случаев конфигурации для обеспечения удобства использования данных маршрутизации после внесения изменений, но до внесения изменений в развернутую систему.</span><span class="sxs-lookup"><span data-stu-id="a78fa-115">Creating and running configuration test cases to help ensure the usability of routing data after you make changes to it, but before committing them the changes to a deployed system.</span></span>

  - <span data-ttu-id="a78fa-116">Создавайте и изменяйте правила нормализации чисел, профили местоположений, политику голосовой связи и данные маршрутизации, не записывая необходимые регулярные выражения.</span><span class="sxs-lookup"><span data-stu-id="a78fa-116">Creating and changing number normalization rules, location profiles, voice policy, and routing data without writing the necessary regular expressions.</span></span>

  - <span data-ttu-id="a78fa-117">Анализ профиля местоположения для обеспечения совместимости с Lync Server Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="a78fa-117">Analyzing a location profile for compatibility with the Lync Server Phone Edition.</span></span>

  - <span data-ttu-id="a78fa-118">Дополнительные сведения о тестовых маршрутах можно найти на странице [Проверка голосовой маршрутизации в Lync Server 2013](lync-server-2013-test-voice-routing.md)</span><span class="sxs-lookup"><span data-stu-id="a78fa-118">More information about voice routing tests can be found at [Test voice routing in Lync Server 2013](lync-server-2013-test-voice-routing.md)</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="a78fa-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a78fa-119">See Also</span></span>


[<span data-ttu-id="a78fa-120">Тестирование голосовой маршрутизации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a78fa-120">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="a78fa-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a78fa-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

