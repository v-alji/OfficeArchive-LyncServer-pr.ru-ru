---
title: 'Lync Server 2013: Проверка наличия обновлений анализатора соответствия рекомендациям'
description: 'Lync Server 2013: Проверка наличия обновлений анализатора соответствия рекомендациям.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking for updates to Best Practices Analyzer
ms:assetid: 06f1da8b-99a7-4871-911e-bfb7542baced
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204645(v=OCS.15)
ms:contentKeyID: 48183307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c2662f143be9fc672461715d1c3da867886e686
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434916"
---
# <a name="checking-for-updates-to-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="592c2-103">Проверка обновлений анализатора соответствия рекомендациям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="592c2-103">Checking for updates to Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="592c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="592c2-104">

<span> </span></span></span>

<span data-ttu-id="592c2-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="592c2-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="592c2-106">Когда вы запускаете анализатор соответствия рекомендациям, с помощью этого средства вы можете найти последние обновления для этого средства.</span><span class="sxs-lookup"><span data-stu-id="592c2-106">When you start Best Practices Analyzer, the tool provides you with an option to search for the latest updates to the tool.</span></span> <span data-ttu-id="592c2-107">Если обновление доступно, вы можете скачать обновление.</span><span class="sxs-lookup"><span data-stu-id="592c2-107">If an update is available, you can download the update.</span></span> <span data-ttu-id="592c2-108">Если вы решили не загружать обновления или не можете получить доступ к Интернету, вы можете продолжать пользоваться версией, уже установленной на компьютере.</span><span class="sxs-lookup"><span data-stu-id="592c2-108">If you choose not to download updates, or if Best Practices Analyzer cannot access the Internet, you can continue to use the version that is already on the computer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="592c2-109">Если для доступа к Интернету требуется проверка подлинности прокси-сервера, анализатору соответствия рекомендациям не удается получить доступ к новым обновлениям, которые вы хотите скачать.</span><span class="sxs-lookup"><span data-stu-id="592c2-109">If you need proxy authentication to access the Internet, Best Practices Analyzer cannot access new updates for you to download.</span></span> <span data-ttu-id="592c2-110">Тем не менее, вы можете вручную загрузить последнюю версию RtcBPA.msi из центра загрузки Майкрософт по адресу <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A> .</span><span class="sxs-lookup"><span data-stu-id="592c2-110">However, you can manually download the latest version of RtcBPA.msi from the Microsoft Download Center at <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A>.</span></span> <span data-ttu-id="592c2-111">После загрузки файла вы можете скопировать его на компьютер, на котором вы хотите обновить анализатор соответствия рекомендациям, и с помощью MSI-файла установить новую версию средства на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="592c2-111">After downloading the file, you can copy it to the computer on which you want to update Best Practices Analyzer and use the .msi file to install the new version of the tool on that computer.</span></span>



</div>

<span data-ttu-id="592c2-112">Чтобы обновить правила анализатора соответствия рекомендациям, необходимо запустить средство в качестве администратора на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="592c2-112">To update Best Practices Analyzer rules, you must run the tool as an Administrator on the local computer.</span></span> <span data-ttu-id="592c2-113">Если вы не вошли в систему с помощью учетной записи, которая входит в группу администраторов, и обнаружены обновления, закройте анализатор соответствия рекомендациям, а затем выполните указанные ниже действия, чтобы запустить программу.</span><span class="sxs-lookup"><span data-stu-id="592c2-113">If you are not logged on using an account that is a member of the Administrators group and updates are detected, close Best Practices Analyzer, and then use the following procedure to start the program.</span></span>

<div>

## <a name="to-open-best-practices-analyzer-as-administrator-to-check-for-updates"></a><span data-ttu-id="592c2-114">Чтобы открыть анализатор соответствия рекомендациям в качестве администратора, чтобы проверить наличие обновлений, выполните описанные выше.</span><span class="sxs-lookup"><span data-stu-id="592c2-114">To open Best Practices Analyzer as Administrator to check for updates</span></span>

1.  <span data-ttu-id="592c2-115">На компьютере, на котором установлен анализатор соответствия рекомендациям, нажмите кнопку **Пуск**, выберите пункт **Microsoft Lync Server 2013**, щелкните правой кнопкой **анализатор соответствия рекомендациям** и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="592c2-115">On a computer on which Best Practices Analyzer is installed, click **Start**, point to **Microsoft Lync Server 2013**, right-click **Best Practices Analyzer**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="592c2-116">Укажите учетные данные для учетной записи, которая входит в группу "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="592c2-116">Specify credentials of an account that is a member of the Administrators group.</span></span>

<span data-ttu-id="592c2-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="592c2-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

