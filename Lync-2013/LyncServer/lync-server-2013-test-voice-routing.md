---
title: 'Lync Server 2013: тестирование голосовой маршрутизации'
description: 'Lync Server 2013: Проверка маршрутизации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice routing
ms:assetid: d3aae909-fef6-440f-b144-0b62dc82bf5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398915(v=OCS.15)
ms:contentKeyID: 48185444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e641e68ccecfe7d1d0e64dc9eb1b1f5016e68e22
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441153"
---
# <a name="test-voice-routing-in-lync-server-2013"></a><span data-ttu-id="0dc78-103">Тестирование голосовой маршрутизации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0dc78-103">Test voice routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0dc78-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0dc78-104">

<span> </span></span></span>

<span data-ttu-id="0dc78-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="0dc78-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="0dc78-106">Вы можете настроить сценарии тестовых случаев с помощью панели управления Lync Server на странице **Проверка маршрутизации голосовых сообщений** .</span><span class="sxs-lookup"><span data-stu-id="0dc78-106">You can use the Lync Server Control Panel **Test Voice Routing** tab to configure test case scenarios.</span></span> <span data-ttu-id="0dc78-107">Для определения тестового случая Вы можете указать абонентскую группу, политику голосовой связи, использование КТСОП и голосовой маршрут, с помощью которых можно протестировать указанный номер телефона.</span><span class="sxs-lookup"><span data-stu-id="0dc78-107">To define a test case, you specify the dial plan, voice policy, PSTN usage, and voice route against which to test a specified phone number.</span></span>

<span data-ttu-id="0dc78-108">Прежде чем приступить к развертыванию конфигурации голосовой маршрутизации, мы рекомендуем проверить ее на различных телефонных номерах, чтобы убедиться в том, что результаты ожидаются.</span><span class="sxs-lookup"><span data-stu-id="0dc78-108">Before you actually deploy your voice routing configuration, we recommend that you test it on various phone numbers to make sure that the results are what you're expecting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="0dc78-109">С помощью команд <STRONG>экспорта тестовых случаев</STRONG> и <STRONG>импорта тестовых случаев</STRONG> можно сохранять тестовые случаи голосовой маршрутизации и импортировать их для использования на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="0dc78-109">You can use the <STRONG>Export test cases</STRONG> and <STRONG>Import test cases</STRONG> commands to save voice routing test cases and import them for use on another computer.</span></span>



</div>

<div>


> [!WARNING]  
> <span data-ttu-id="0dc78-110">Если вы удалите все части конфигурации голосовой связи, такие как абонентская группа, политика голосовой связи, маршрут голосовой связи или использование телефона, необходимо просмотреть и изменить тестовые случаи для маршрутизации голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="0dc78-110">If you delete any part of your voice routing configuration, such as a dial plan, voice policy, voice route, or phone usage, you should review and update your voice routing test cases.</span></span> <span data-ttu-id="0dc78-111">На панели управления Lync Server не выводится предупреждение о том, что они больше не действительны из-за измененных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="0dc78-111">The Lync Server Control Panel will not alert you to test cases that are no longer valid due to changed configurations.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0dc78-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="0dc78-112">In This Section</span></span>

  - [<span data-ttu-id="0dc78-113">Создание тестового примера маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0dc78-113">Create a voice routing test case in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-routing-test-case.md)

  - [<span data-ttu-id="0dc78-114">Экспорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0dc78-114">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)

  - [<span data-ttu-id="0dc78-115">Импорт тестовых примеров маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0dc78-115">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)

  - [<span data-ttu-id="0dc78-116">Проведение тестов маршрутизации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0dc78-116">Running voice routing tests in Lync Server 2013</span></span>](lync-server-2013-running-voice-routing-tests.md)

<span data-ttu-id="0dc78-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0dc78-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

