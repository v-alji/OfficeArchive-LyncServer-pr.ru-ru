---
title: 'Lync Server 2013: развертывание подключаемого модуля VDI Lync'
description: 'Lync Server 2013: развертывание плагина Lync VDI.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying the Lync VDI plug-in
ms:assetid: 11d3bd5d-6dd3-471c-b842-b072fa197714
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204683(v=OCS.15)
ms:contentKeyID: 48183449
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3addecb07f269e4524f3da835f479439639935ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398191"
---
# <a name="deploying-the-lync-vdi-plug-in-in-lync-server-2013"></a><span data-ttu-id="c2569-103">Развертывание подключаемого модуля VDI Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2569-103">Deploying the Lync VDI plug-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2569-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2569-104">

<span> </span></span></span>

<span data-ttu-id="c2569-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="c2569-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="c2569-106">Клиент Lync 2013 поддерживает звук и видео в среде инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="c2569-106">The Lync 2013 client supports audio and video in a Virtual Desktop Infrastructure (VDI) environment.</span></span> <span data-ttu-id="c2569-107">Пользователь может подключить звуковое или видеоустройство (например, гарнитуру или камеру) к локальному компьютеру (например, на компьютере с тонким клиентом или переназначенным компьютером).</span><span class="sxs-lookup"><span data-stu-id="c2569-107">A user can connect an audio or video device (for example, a headset or a camera) to the local computer (for example, a thin client or repurposed computer).</span></span> <span data-ttu-id="c2569-108">Пользователь может подключиться к виртуальной машине, войти в клиент Lync 2013, который запущен на виртуальной машине, и принять участие в голосовой и видеосвязи в режиме реального времени, как если бы клиент работал на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c2569-108">The user can connect to the virtual machine, sign in to the Lync 2013 client that is running on the virtual machine, and participate in real-time audio and video communications as though the client is running locally.</span></span>

<span data-ttu-id="c2569-109">Плагин Lync VDI — это отдельное приложение, которое устанавливается на локальном компьютере и позволяет использовать локальные аудио-и видеоустройства в клиенте Lync 2013, работающем на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c2569-109">The Lync VDI Plug-in is a stand-alone application that installs on the local computer and allows the use of local audio and video devices with the Lync 2013 client running on the virtual machine.</span></span> <span data-ttu-id="c2569-110">Для этого плагина не требуется установка Lync на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c2569-110">The plug-in does not require Lync to be installed on the local computer.</span></span> <span data-ttu-id="c2569-111">После того как пользователь войдет в клиент Lync 2013, работающий на виртуальной машине, Lync предложит пользователю повторно ввести свои учетные данные, чтобы установить соединение с помощью плагина Lync VDI, запущенного на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c2569-111">After the user signs in to the Lync 2013 client that is running on the virtual machine, Lync prompts the user to re-enter his or her credentials to establish a connection with the Lync VDI Plug-in that is running on the local computer.</span></span> <span data-ttu-id="c2569-112">После того как соединение установлено, пользователь сможет звонить и принимать голосовые и видеозвонки.</span><span class="sxs-lookup"><span data-stu-id="c2569-112">After this connection is established, the user is ready to make and receive audio and video calls.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c2569-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="c2569-113">In This Section</span></span>

  - [<span data-ttu-id="c2569-114">Необходимые условия для подключаемого модуля Lync VDI в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2569-114">Lync VDI plug-in prerequisites in Lync Server 2013</span></span>](lync-server-2013-lync-vdi-plug-in-prerequisites.md)

  - [<span data-ttu-id="c2569-115">Подготовка среды Lync Server 2013 к VDI</span><span class="sxs-lookup"><span data-stu-id="c2569-115">Preparing your Lync Server 2013 environment for VDI</span></span>](lync-server-2013-preparing-your-environment-for-vdi.md)

  - [<span data-ttu-id="c2569-116">Вход в виртуальную машину и использование на ней Lync 2013</span><span class="sxs-lookup"><span data-stu-id="c2569-116">Signing in and using Lync 2013 on the virtual machine</span></span>](lync-server-2013-signing-in-and-using-lync-2013-on-the-virtual-machine.md)

  - [<span data-ttu-id="c2569-117">Устранение неполадок с внешним модулем Lync VDI в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2569-117">Troubleshooting the Lync VDI plug-in in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-the-lync-vdi-plug-in.md)

  - [<span data-ttu-id="c2569-118">Поддерживаемые технологии виртуализации и известные ограничения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2569-118">Supported virtualization technologies and known limitations in Lync Server 2013</span></span>](lync-server-2013-supported-virtualization-technologies-and-known-limitations.md)

<span data-ttu-id="c2569-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2569-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

