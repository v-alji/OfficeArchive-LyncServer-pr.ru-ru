---
title: 'Lync Server 2013: настройка шифрования мультимедиа для общедоступных поставщиков'
description: 'Lync Server 2013: Настройка шифрования мультимедиа для общедоступных поставщиков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media encryption for public providers
ms:assetid: a95814cf-c5a9-4652-8ffc-c469a2653153
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205149(v=OCS.15)
ms:contentKeyID: 48185036
ms.date: 12/13/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 177c19f151b67d741c7e26506f7ebc98b3ce831a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433887"
---
# <a name="configure-media-encryption-for-public-providers-in-lync-server-2013"></a><span data-ttu-id="f2fef-103">Настройка шифрования мультимедиа для общедоступных поставщиков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2fef-103">Configure media encryption for public providers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2fef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2fef-104">

<span> </span></span></span>

<span data-ttu-id="f2fef-105">_**Тема последнего изменения:** 2014-12-12_</span><span class="sxs-lookup"><span data-stu-id="f2fef-105">_**Topic Last Modified:** 2014-12-12_</span></span>

<span data-ttu-id="f2fef-106">Если вы реализуете Федерацию аудио-и видеосвязи (A/V) с Windows Live Messenger, необходимо изменить два параметра: уровень шифрования Lync Server и политика EnablePublicCloudAccess.</span><span class="sxs-lookup"><span data-stu-id="f2fef-106">If you are implementing audio/video (A/V) federation with Windows Live Messenger, there are two parameters that you need to modify: the Lync Server encryption level and the EnablePublicCloudAccess policy.</span></span> <span data-ttu-id="f2fef-107">По умолчанию задано значение "обязательный уровень шифрования".</span><span class="sxs-lookup"><span data-stu-id="f2fef-107">By default, the encryption level is set to Required.</span></span> <span data-ttu-id="f2fef-108">Этот параметр необходимо изменить на "поддерживается".</span><span class="sxs-lookup"><span data-stu-id="f2fef-108">You must change this setting to Supported.</span></span> <span data-ttu-id="f2fef-109">Если для политики EnablePublicCloudAccess задано значение false, необходимо установить **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f2fef-109">If the EnablePublicCloudAccess policy is set to false, this needs to be set to **True**.</span></span> <span data-ttu-id="f2fef-110">Это можно сделать в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="f2fef-110">You can do this from the Lync Server Management Shell.</span></span>

<div>

## <a name="configure-federation-for-windows-live"></a><span data-ttu-id="f2fef-111">Настройка Федерации для Windows Live</span><span class="sxs-lookup"><span data-stu-id="f2fef-111">Configure Federation for Windows Live</span></span>

1.  <span data-ttu-id="f2fef-112">Запустите командную консоль Lync Server на сервере переднего плана: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f2fef-112">Start the Lync Server Management Shell on the Front End server: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="f2fef-113">В командной строке введите следующие команды:</span><span class="sxs-lookup"><span data-stu-id="f2fef-113">From the command prompt, type the following commands:</span></span>
    
       ```powershell
        Set-CsMediaConfiguration -EncryptionLevel SupportEncryption
       ```
    
       ```powershell
        Set-CsExternalAccessPolicy Global -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true
       ```
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="f2fef-114">Это действие является обязательным, так как в Windows Live Messenger не поддерживается шифрование аудио-и видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="f2fef-114">This is required step because Windows Live Messenger does not support encryption of audio/video.</span></span> <span data-ttu-id="f2fef-115">В команде для глобальной политики задано значение параметра шифрование поддержки, а не необходимость шифрования аудио-и видеоданных.</span><span class="sxs-lookup"><span data-stu-id="f2fef-115">The command sets your global policy to a support encryption setting instead of requiring encryption of the audio/video data.</span></span> <span data-ttu-id="f2fef-116">Клиенты, которые поддерживают шифрование, по-прежнему будут использовать шифрование, например Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f2fef-116">Clients that support encryption will still use encryption, such as Lync 2013.</span></span>

    
    <span data-ttu-id="f2fef-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2fef-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

