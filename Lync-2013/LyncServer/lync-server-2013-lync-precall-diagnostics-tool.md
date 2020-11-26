---
title: 'Lync Server 2013: средство диагностики предзвонков для Lync'
description: 'Lync Server 2013: средство диагностики предзвонков для Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync PreCall Diagnostics Tool
ms:assetid: 0ff291ec-cfb4-43eb-b5d6-a7a325681e3f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn451255(v=OCS.15)
ms:contentKeyID: 56708404
ms.date: 11/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c2c51551fe0991eb354a628b1d4660baa1532b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426337"
---
# <a name="lync-precall-diagnostics-tool-in-lync-server-2013"></a><span data-ttu-id="b41f6-103">Средство диагностики предзвонков для Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b41f6-103">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b41f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b41f6-104">

<span> </span></span></span>

<span data-ttu-id="b41f6-105">_**Тема последнего изменения:** 2016-11-04_</span><span class="sxs-lookup"><span data-stu-id="b41f6-105">_**Topic Last Modified:** 2016-11-04_</span></span>

<span data-ttu-id="b41f6-106">Средство диагностики предварительных вызовов Lync (PCD) — это клиентское приложение, позволяющее узнать, как текущее состояние сети может повлиять на качество звука при предстоящем звонке в корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="b41f6-106">The Lync PreCall Diagnostics Tool (PCD) is a client-based application that allows you to see how the current state of your network might impact the audio quality in an upcoming Enterprise Voice call.</span></span>

<span data-ttu-id="b41f6-107">PCD наиболее полезен в ситуациях, когда последний прыжок сети, скорее всего, является самым слабым (например, при наличии ноутбуков в общедоступной сети Wi-Fi или домашних пользователей).</span><span class="sxs-lookup"><span data-stu-id="b41f6-107">PCD is most useful in situations where the last hop of a network is likely to be the weakest (for example, with laptops on a public WiFi network or home users).</span></span> <span data-ttu-id="b41f6-108">PCD создает небольшой потоковый пакет, который проходит по этому заключительному этапу сети.</span><span class="sxs-lookup"><span data-stu-id="b41f6-108">PCD creates a small packet stream that traverses this final leg of the network.</span></span> <span data-ttu-id="b41f6-109">Затем средство анализирует поток пакета, чтобы оценить, как нарушение и убытки в этой области могут повлиять на качество связи, а затем предоставляет отчет.</span><span class="sxs-lookup"><span data-stu-id="b41f6-109">The tool then analyzes the packet stream to estimate how the jitter and loss along this leg might impact call quality, and then provides a report.</span></span> <span data-ttu-id="b41f6-110">Вы можете запускать PCD на клиенте постоянно, даже при помещении звонков.</span><span class="sxs-lookup"><span data-stu-id="b41f6-110">You can run PCD continuously on the client, even while calls are being placed.</span></span> <span data-ttu-id="b41f6-111">Поток пакетов не оказывает существенного воздействия на пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="b41f6-111">The packet stream does not have a significant effect on bandwidth.</span></span>

<span data-ttu-id="b41f6-112">**Последний выпуск PCD версии 1,1 включает следующие улучшения:**</span><span class="sxs-lookup"><span data-stu-id="b41f6-112">**The latest release of the PCD, version 1.1, includes the following enhancements:**</span></span>

  - <span data-ttu-id="b41f6-113">Поддержка более длинных паролей, которые теперь могут содержать до 127 символов</span><span class="sxs-lookup"><span data-stu-id="b41f6-113">Support for longer passwords, which can now be up to 127 characters</span></span>

  - <span data-ttu-id="b41f6-114">Дополнительная диагностика проблем со входом для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b41f6-114">Additional diagnostics for authentication sign-in issues</span></span>

  - <span data-ttu-id="b41f6-115">Улучшенная поддержка гибридных развертываний Lync</span><span class="sxs-lookup"><span data-stu-id="b41f6-115">Better support for Lync hybrid deployments</span></span>

  - <span data-ttu-id="b41f6-116">Обновления средства выбора учетных данных</span><span class="sxs-lookup"><span data-stu-id="b41f6-116">Updates to credential picker</span></span>

  - <span data-ttu-id="b41f6-117">Улучшенная стабильность</span><span class="sxs-lookup"><span data-stu-id="b41f6-117">Stability improvements</span></span>

<span data-ttu-id="b41f6-118">Благодарим за отзыв.</span><span class="sxs-lookup"><span data-stu-id="b41f6-118">We appreciate any feedback.</span></span> <span data-ttu-id="b41f6-119">Пожалуйста, отправляйте вопросы и ответы по вопросам поддержки по адресу [PCD отзыва](mailto:pcdfb@microsoft.com) <pcdfb@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="b41f6-119">Please send all support questions or issues to the [PCD Feedback](mailto:pcdfb@microsoft.com) alias at <pcdfb@microsoft.com>.</span></span>

<span data-ttu-id="b41f6-120">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="b41f6-120">This topic includes the following sections:</span></span>

  - <span data-ttu-id="b41f6-121">Версии PCD для Lync</span><span class="sxs-lookup"><span data-stu-id="b41f6-121">Lync PCD Versions</span></span>

  - <span data-ttu-id="b41f6-122">Требования к системе для Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-122">Lync PCD System Requirements</span></span>

  - <span data-ttu-id="b41f6-123">Возможности Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-123">Lync PCD Features</span></span>

  - <span data-ttu-id="b41f6-124">Выполнение Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-124">Running Lync PCD</span></span>

  - <span data-ttu-id="b41f6-125">Удаление Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-125">Uninstalling Lync PCD</span></span>

<span id="Version"></span>

<div>

## <a name="lync-pcd-versions"></a><span data-ttu-id="b41f6-126">Версии PCD для Lync</span><span class="sxs-lookup"><span data-stu-id="b41f6-126">Lync PCD Versions</span></span>

<span data-ttu-id="b41f6-127">В этой статье описаны следующие версии средства, которые можно загрузить бесплатно.</span><span class="sxs-lookup"><span data-stu-id="b41f6-127">This topic describes the following versions of the tool, available for free download:</span></span>

  - <span data-ttu-id="b41f6-128">Классическое приложение для Windows ( [https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914) )</span><span class="sxs-lookup"><span data-stu-id="b41f6-128">Windows Desktop App ([https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914))</span></span>

</div>

<span id="Requirements"></span>

<div>

## <a name="lync-pcd-system-requirements"></a><span data-ttu-id="b41f6-129">Требования к системе для Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-129">Lync PCD System Requirements</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b41f6-130">Для PCD требуется, чтобы веб-интерфейс единой системы обмена сообщениями (UCWA) был установлен и настроен для поддержки мобильных клиентов в развертывании Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b41f6-130">PCD requires that Unified Communications Web API (UCWA) be installed and configured to support mobile clients in the Lync Server deployment.</span></span> <span data-ttu-id="b41f6-131">UCWA устанавливается вместе с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b41f6-131">UCWA is installed with Lync Server.</span></span>



</div>

<div>

## <a name="windows-desktop-app-requirements"></a><span data-ttu-id="b41f6-132">Требования для классических приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="b41f6-132">Windows Desktop App Requirements</span></span>

  - <span data-ttu-id="b41f6-133">Любая версия операционной системы Windows 7 или Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b41f6-133">Any edition of the Windows 7 or Windows 8 operating system</span></span>

  - <span data-ttu-id="b41f6-134">Microsoft .NET Framework 4,5, на котором можно найти по адресу [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span><span class="sxs-lookup"><span data-stu-id="b41f6-134">Microsoft .NET Framework 4.5 available at [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span></span>

</div>

</div>

<span id="features"></span>

<div>

## <a name="lync-pcd-features"></a><span data-ttu-id="b41f6-135">Возможности Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-135">Lync PCD Features</span></span>

<span data-ttu-id="b41f6-136">Lync PCD включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="b41f6-136">Lync PCD includes the following features:</span></span>

  - <span data-ttu-id="b41f6-137">Запускать по запросу (2-минутные пакеты)</span><span class="sxs-lookup"><span data-stu-id="b41f6-137">Run in default On Demand (2 minute bursts)</span></span>

  - <span data-ttu-id="b41f6-138">Всегда запускать в режиме "включено" (до 24 часов в привязанном представлении)</span><span class="sxs-lookup"><span data-stu-id="b41f6-138">Run in Always On (up to 24 hours in snapped view) mode</span></span>

  - <span data-ttu-id="b41f6-139">Исторический вид тестовых запусков</span><span class="sxs-lookup"><span data-stu-id="b41f6-139">Historical view of your test runs</span></span>

  - <span data-ttu-id="b41f6-140">Диагностика сбоев при входе (только Lync PCD для Windows 8)</span><span class="sxs-lookup"><span data-stu-id="b41f6-140">Diagnose sign-in failures (Lync PCD for Windows 8 only)</span></span>

<span data-ttu-id="b41f6-141">![Снимок экрана с индикатором выполнения входных компонентов Lync PCD](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Снимок экрана с индикатором выполнения входных компонентов Lync PCD")</span><span class="sxs-lookup"><span data-stu-id="b41f6-141">![Lync PCD features Sign in progress screen shot](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Lync PCD features Sign in progress screen shot")</span></span>

  - <span data-ttu-id="b41f6-142">Графическое представление метрик сети — сетевые MOS, потеря пакетов и нарушение колебаний в полноэкранном режиме и прикрепленном представлении.</span><span class="sxs-lookup"><span data-stu-id="b41f6-142">Graphical view of network metrics – Network MOS, Packet Loss and Interarrival Jitter in full screen and snapped view.</span></span>

<span data-ttu-id="b41f6-143">**Полноэкранный режим**</span><span class="sxs-lookup"><span data-stu-id="b41f6-143">**Full screen view**</span></span>

<span data-ttu-id="b41f6-144">![Графики с результатами тестирования с помощью средства диагностики PreCall](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "Графики с результатами тестирования с помощью средства диагностики PreCall")</span><span class="sxs-lookup"><span data-stu-id="b41f6-144">![PreCall Diagnostic Tool test result graphs](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "PreCall Diagnostic Tool test result graphs")</span></span>

<span data-ttu-id="b41f6-145">**Привязанное представление**</span><span class="sxs-lookup"><span data-stu-id="b41f6-145">**Snapped view**</span></span>

<span data-ttu-id="b41f6-146">![Средство диагностики PreCall, результаты тестирования использования](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "Средство диагностики PreCall, результаты тестирования использования")</span><span class="sxs-lookup"><span data-stu-id="b41f6-146">![PreCall Diagnostic Tool Utilization test results](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "PreCall Diagnostic Tool Utilization test results")</span></span>

</div>

<span id="running"></span>

<div>

## <a name="running-lync-pcd"></a><span data-ttu-id="b41f6-147">Выполнение Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-147">Running Lync PCD</span></span>

<div>

## <a name="running-windows-desktop-app"></a><span data-ttu-id="b41f6-148">Запущен классическое приложение Windows</span><span class="sxs-lookup"><span data-stu-id="b41f6-148">Running Windows Desktop App</span></span>

1.  <span data-ttu-id="b41f6-149">Чтобы запустить PCD в системе Windows 7, в меню " **Пуск** " выберите пункт " **Диагностика перед вызовом** ".</span><span class="sxs-lookup"><span data-stu-id="b41f6-149">To start the PCD on a Windows 7 system, select **PreCall Diagnostics** from the **Start** menu.</span></span>
    
    <span data-ttu-id="b41f6-150">Чтобы запустить PCD в системе Windows 8, щелкните значок на начальном экране или выполните поиск по запросу "Диагностика для предзвонков".</span><span class="sxs-lookup"><span data-stu-id="b41f6-150">To start the PCD on a Windows 8 system, select the icon on your Start screen, or search for “PreCall Diagnostics.”</span></span>
    
    <span data-ttu-id="b41f6-151">![Значок средства диагностики PreCall](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "Значок средства диагностики PreCall")</span><span class="sxs-lookup"><span data-stu-id="b41f6-151">![PreCall Diagnostic tool icon](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "PreCall Diagnostic tool icon")</span></span>

2.  <span data-ttu-id="b41f6-152">При запуске средства выберите предпочтительный способ предоставления учетных данных, а затем в диалоговом окне **Параметры средства диагностики** для подготовки к диагностике выберите команду " **ОК**".</span><span class="sxs-lookup"><span data-stu-id="b41f6-152">When the tool starts, select your preferred method of providing credentials and select the network operating mode in the **PreCall Diagnostics Tool Options** dialog box, then select **OK**:</span></span>

3.  <span data-ttu-id="b41f6-153">Нажмите кнопку **начать проверку** , чтобы начать работу с диагностикой.</span><span class="sxs-lookup"><span data-stu-id="b41f6-153">Select the **Start Test** button to start running diagnostics.</span></span>
    
    <span data-ttu-id="b41f6-154">Если вы выбрали параметр **использовать сетевые учетные данные** , проверка начнется немедленно.</span><span class="sxs-lookup"><span data-stu-id="b41f6-154">If you selected the **Use network credentials** option, the test begins immediately.</span></span>
    
    <span data-ttu-id="b41f6-155">Если вы выбрали параметр **предоставить учетные данные** , откроется диалоговое окно " **Безопасность Windows** ".</span><span class="sxs-lookup"><span data-stu-id="b41f6-155">If you selected the **Let me enter my credentials** option, the **Windows Security** dialog box opens.</span></span> <span data-ttu-id="b41f6-156">После ввода учетных данных начинается проверка.</span><span class="sxs-lookup"><span data-stu-id="b41f6-156">After you enter your credentials, the test starts.</span></span>

</div>

</div>

<span id="uninstall"></span>

<div>

## <a name="uninstalling-lync-pcd"></a><span data-ttu-id="b41f6-157">Удаление Lync PCD</span><span class="sxs-lookup"><span data-stu-id="b41f6-157">Uninstalling Lync PCD</span></span>

<span data-ttu-id="b41f6-158">Чтобы удалить Lync PCD, выполните действия, описанные в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="b41f6-158">To remove Lync PCD, follow the procedure for your operating system:</span></span>

  - <span data-ttu-id="b41f6-159">В системе Windows 7 откройте **Панель управления**, выберите " **программы и компоненты**", а затем дважды щелкните элемент "Диагностика предварительных **вызовов Lync 2013**".</span><span class="sxs-lookup"><span data-stu-id="b41f6-159">On a Windows 7 system, open the **Control Panel**, select **Programs and Features**, and double-click **Lync 2013 PreCall Diagnostics**.</span></span>

  - <span data-ttu-id="b41f6-160">В системе Windows 8 щелкните правой кнопкой мыши плитку PCD и выберите команду **Удалить** на панели приложения в нижней части начального экрана.</span><span class="sxs-lookup"><span data-stu-id="b41f6-160">On a Windows 8 system, right-click on the PCD tile and click **Uninstall** from the app bar at the bottom of the start screen.</span></span>

<span data-ttu-id="b41f6-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b41f6-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

