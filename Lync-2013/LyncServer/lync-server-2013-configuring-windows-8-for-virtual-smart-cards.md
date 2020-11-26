---
title: 'Lync Server 2013: Настройка Windows 8 для виртуальных смарт-карт'
description: 'Lync Server 2013: Настройка Windows 8 для виртуальных смарт-карт.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Windows 8 for Virtual Smart Cards
ms:assetid: 4916c167-4ee3-4f3e-b65c-33e588595112
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308564(v=OCS.15)
ms:contentKeyID: 54973684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 112047f91a20dd552c628fb33eba7bb9ad3d0f01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432319"
---
# <a name="configuring-windows-8-for-using-virtual-smart-cards-with-lync-server-2013"></a><span data-ttu-id="d4976-103">Настройка Windows 8 для использования виртуальных смарт-карт с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4976-103">Configuring Windows 8 for using Virtual Smart Cards with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4976-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4976-104">

<span> </span></span></span>

<span data-ttu-id="d4976-105">_**Тема последнего изменения:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="d4976-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="d4976-106">Одним их факторов, которые следует учитывать при развертывании двухфакторной проверки подлинности и технологии смарт-карт, является его стоимость.</span><span class="sxs-lookup"><span data-stu-id="d4976-106">One factor to consider when deploying two-factor authentication and smart card technology is the cost of implementation.</span></span> <span data-ttu-id="d4976-107">Windows 8 предлагает ряд новых возможностей обеспечения безопасности, а одна из наиболее интересных новых возможностей — поддержка виртуальных смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="d4976-107">Windows 8 provides a number of new security capabilities, and one of the most interesting new features is support for virtual smart cards.</span></span>

<span data-ttu-id="d4976-108">Если компьютеры оборудованы микросхемами доверенного платформенного модуля (TPM), соответствующими спецификации версии 1.2, организации могут пользоваться преимуществами регистрации по смарт-картам без дополнительных капиталовложений в оборудование.</span><span class="sxs-lookup"><span data-stu-id="d4976-108">For computers equipped with a Trusted Platform Module (TPM) chip that meets specification version 1.2, organizations can now get the benefits of smart card logon without making any additional investments in hardware.</span></span> <span data-ttu-id="d4976-109">Дополнительные сведения можно найти в разделе Использование виртуальных смарт-карт в Windows 8 [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365) .</span><span class="sxs-lookup"><span data-stu-id="d4976-109">For more information, see Using Virtual Smart Cards with Windows 8 at [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365).</span></span>

<div>

## <a name="to-configure-windows-8-for-virtual-smart-cards"></a><span data-ttu-id="d4976-110">Настройка конфигурации Windows 8 для виртуальных смарт-карт</span><span class="sxs-lookup"><span data-stu-id="d4976-110">To Configure Windows 8 for Virtual Smart Cards</span></span>

1.  <span data-ttu-id="d4976-111">Войдите в систему на компьютере с Windows 8, используя учетные данные пользователя с поддержкой Lync.</span><span class="sxs-lookup"><span data-stu-id="d4976-111">Log in to the Windows 8 computer using the credentials of a Lync-enabled user.</span></span>

2.  <span data-ttu-id="d4976-112">На начальном экране Windows 8 переместите курсор в нижний правый угол.</span><span class="sxs-lookup"><span data-stu-id="d4976-112">At the Windows 8 Start screen, move your cursor to the bottom right corner of the screen.</span></span>

3.  <span data-ttu-id="d4976-113">Выберите команду **Поиск** и найдите элемент **Command Prompt**.</span><span class="sxs-lookup"><span data-stu-id="d4976-113">Select the **Search** option, and then search for **Command Prompt**.</span></span>

4.  <span data-ttu-id="d4976-114">Щелкните **Командная строка** правой кнопкой мыши, затем выберите **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="d4976-114">Right click on **Command Prompt**, and then select **Run as Administrator**.</span></span>

5.  <span data-ttu-id="d4976-115">Откройте консоль управления TPM, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d4976-115">Open the Trusted Platform Module (TPM) Management console by running the following command:</span></span>
    
        Tpm.msc

6.  <span data-ttu-id="d4976-116">Убедитесь в том, что спецификация вашего TPM имеет версию 1.2 или выше.</span><span class="sxs-lookup"><span data-stu-id="d4976-116">From the TPM management console, verify that your TPM specification version is at least 1.2</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d4976-117">При появлении диалогового окна с сообщением, что совместимый TPM не найден, убедитесь в том, что ваш компьютер имеет совместимый модуль TPM и что он включен в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="d4976-117">If you receive a dialog stating that a Compatible Trust Platform Module (TPM) cannot be found, verify that the computer has a compatible TPM module and that it is enabled in the system BIOS.</span></span>

    
    </div>

7.  <span data-ttu-id="d4976-118">Закройте консоль управления TPM</span><span class="sxs-lookup"><span data-stu-id="d4976-118">Close the TPM management console</span></span>

8.  <span data-ttu-id="d4976-119">Создайте новую виртуальную смарт-карту, введя в командную строку следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d4976-119">From the command prompt, create a new virtual smart card using the following command:</span></span>
    
        TpmVscMgr create /name MyVSC /pin default /adminkey random /generate
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d4976-120">Чтобы сообщить настраиваемое значение ПИН-кода, используйте ключ командной строки /pin.</span><span class="sxs-lookup"><span data-stu-id="d4976-120">To provide a custom PIN value when creating the virtual smart card, use /pin prompt instead.</span></span>

    
    </div>

9.  <span data-ttu-id="d4976-121">Откройте консоль управления компьютером, введя в командную строку следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d4976-121">From the command prompt, open the Computer Management console by running the following command:</span></span>
    
        CompMgmt.msc

10. <span data-ttu-id="d4976-122">В консоли управления компьютером выберите **Управление устройствами**.</span><span class="sxs-lookup"><span data-stu-id="d4976-122">In the Computer Management console, select **Device Management**.</span></span>

11. <span data-ttu-id="d4976-123">Разверните элемент **Устройства чтения смарт-карт**.</span><span class="sxs-lookup"><span data-stu-id="d4976-123">Expand **Smart card readers**.</span></span>

12. <span data-ttu-id="d4976-124">Убедитесь в том, что создание нового устройства для чтения виртуальной смарт-карты успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="d4976-124">Verify that the new virtual smart card reader has been created successfully.</span></span>

<span data-ttu-id="d4976-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4976-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

