---
title: 'Lync Server 2013: настройка соединения для общедоступных служб обмена мгновенными сообщениями'
description: 'Lync Server 2013: Настройка общедоступной службы обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up public instant messaging connectivity
ms:assetid: 816dea2a-96fa-4a36-b6c2-a9402675868b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205041(v=OCS.15)
ms:contentKeyID: 48184661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2f11c5e01de697b97395b6bc52815fadedff5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441706"
---
# <a name="setting-up-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="ba9d3-103">Настройка соединения для общедоступных служб обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba9d3-103">Setting up public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba9d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba9d3-104">

<span> </span></span></span>

<span data-ttu-id="ba9d3-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="ba9d3-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="ba9d3-106">Если ваша организация хочет поддерживать связь с Интернетом через AOL, вы не можете запросить сертификат с помощью мастера развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-106">If your organization wants to support public instant messaging (IM) connectivity with AOL, you cannot use the Lync Server Deployment Wizard to request the certificate.</span></span> <span data-ttu-id="ba9d3-107">Вместо этого выполните действия, описанные в описанной ниже процедуре.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-107">Instead, perform the steps in the following procedure.</span></span>

<div>

## <a name="setting-up-public-instant-messaging-connectivity"></a><span data-ttu-id="ba9d3-108">Настройка подключения к общедоступной службе мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="ba9d3-108">Setting Up Public Instant Messaging Connectivity</span></span>

1.  <span data-ttu-id="ba9d3-109">На сервере переднего плана откройте окно Построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-109">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="ba9d3-110">Разверните узел Edge Pools, а затем щелкните правой кнопкой мыши граничный сервер или пул пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-110">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="ba9d3-111">Нажмите кнопку изменить свойства.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-111">Select Edit properties.</span></span>

2.  <span data-ttu-id="ba9d3-112">В диалоговом окне Изменение свойств в разделе Общие установите флажок включить федерацию для этого пограничного пула (порт 5061).</span><span class="sxs-lookup"><span data-stu-id="ba9d3-112">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="ba9d3-113">Нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-113">Click OK.</span></span>

3.  <span data-ttu-id="ba9d3-114">Нажмите кнопку действие, выберите пункт топология, нажмите кнопку Опубликовать.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-114">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="ba9d3-115">При появлении запроса на публикацию топологии нажмите кнопку Далее.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-115">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="ba9d3-116">Завершив публикацию, нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-116">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="ba9d3-117">На пограничном сервере откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-117">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="ba9d3-118">Щелкните Установка или обновление операционной системы Lync Server, а затем нажмите кнопку Настройка или удалите компоненты Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-118">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="ba9d3-119">Нажмите кнопку выполнить еще раз.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-119">Click Run Again.</span></span>

5.  <span data-ttu-id="ba9d3-120">В разделе Настройка серверных компонентов Lync нажмите кнопку Далее.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-120">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="ba9d3-121">На экране сводки будут показаны действия по мере их выполнения.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-121">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="ba9d3-122">После завершения развертывания щелкните Просмотреть журнал, чтобы просмотреть доступные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-122">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="ba9d3-123">Нажмите кнопку Готово, чтобы завершить развертывание.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-123">Click Finish to complete the deployment.</span></span>

</div>

<div>

## <a name="to-create-a-certificate-request-for-the-external-interface-of-the-edge-server-to-support-public-im-connectivity-with-aol"></a><span data-ttu-id="ba9d3-124">Создание запроса на сертификат для внешнего интерфейса пограничного сервера, чтобы обеспечить поддержку общедоступной службы обмена мгновенными сообщениями с AOL</span><span class="sxs-lookup"><span data-stu-id="ba9d3-124">To create a certificate request for the external interface of the Edge Server to support public IM connectivity with AOL</span></span>

1.  <span data-ttu-id="ba9d3-125">Если необходимый шаблон доступен для центра сертификации, для запроса сертификата используйте следующий командлет Windows PowerShell из пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-125">When the required template is available to the CA, use the following Windows PowerShell cmdlet from at the Edge Server to request the certificate</span></span>
    
        Request-CsCertificate -New -Type AccessEdgeExternal  -Output C:\ <certfilename.txt or certfilename.csr>  -ClientEku $true -Template <template name>
    
    <span data-ttu-id="ba9d3-126">Имя сертификата по умолчанию для шаблона Lync Server — это веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-126">The default certificate name of the template used for Lync Server is Web Server.</span></span> <span data-ttu-id="ba9d3-127">Указывайте, только \<template name\> Если вам нужно использовать шаблон, отличный от шаблона по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-127">Only specify the \<template name\> if you need to use a template that is different from the default template.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ba9d3-128">Если в вашей организации требуется поддержка общедоступной службы обмена мгновенными сообщениями с AOL, вы должны использовать Windows PowerShell вместо мастера сертификатов, чтобы запросить назначение сертификата внешнему краю службы Edge Access.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-128">If your organization wants to support public IM connectivity with AOL, you must use Windows PowerShell instead of the Certificate Wizard to request the certificate to be assigned to the external edge for the Access Edge service.</span></span> <span data-ttu-id="ba9d3-129">Это связано с тем, что шаблон веб-сервера центра сертификации (ЦС), используемый мастером сертификатов для запроса сертификата, не поддерживает конфигурацию клиентского EKU.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-129">This is because the Certificate Authority (CA) Web Server template that the Certificate Wizard uses to request a certificate does not support client EKU configuration.</span></span> <span data-ttu-id="ba9d3-130">Прежде чем использовать Windows PowerShell для создания сертификата, администратор центра администрирования должен создать и развернуть новый шаблон, поддерживающий клиентское EKU.</span><span class="sxs-lookup"><span data-stu-id="ba9d3-130">Before using Windows PowerShell to create the certificate, the CA administrator must create and deploy a new template that supports client EKU.</span></span>

    
    <span data-ttu-id="ba9d3-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba9d3-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

