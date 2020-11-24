---
title: Настройка политик доступа и сертификатов шлюза XMPP
description: Настройте политики доступа к шлюзу XMPP и сертификаты.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure XMPP gateway access policies and certificates
ms:assetid: fac02f4e-d14d-4be3-b53c-74c82436fd93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721945(v=OCS.15)
ms:contentKeyID: 49733882
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e958100501ad9ca87d1ab970162f4be8c7692a99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398356"
---
# <a name="configure-xmpp-gateway-access-policies-and-certificates"></a><span data-ttu-id="94071-103">Настройка политик доступа и сертификатов шлюза XMPP</span><span class="sxs-lookup"><span data-stu-id="94071-103">Configure XMPP gateway access policies and certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="94071-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="94071-104">

<span> </span></span></span>

<span data-ttu-id="94071-105">_**Тема последнего изменения:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="94071-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="94071-106">XMPP Федерация определяет внешнее развертывание на основе расширяемого протокола обмена сообщениями и присутствия (XMPP).</span><span class="sxs-lookup"><span data-stu-id="94071-106">XMPP federation defines an external deployment based on the eXtensible Messaging and Presence Protocol (XMPP).</span></span> <span data-ttu-id="94071-107">Конфигурация XMPP позволяет пользователям Lync получать доступ к XMPP доменам, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="94071-107">An XMPP configuration allows Lync users access to XMPP domain users by:</span></span>

  - <span data-ttu-id="94071-108">Обмен сообщениями и присутствие — только для человека</span><span class="sxs-lookup"><span data-stu-id="94071-108">IM and Presence – person to person only</span></span>

  - <span data-ttu-id="94071-109">Создание федеративных контактов XMPP в клиенте Lync</span><span class="sxs-lookup"><span data-stu-id="94071-109">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="94071-110">Если вы настраиваете политики для поддержки федеративных партнеров по протоколу расширенного обмена сообщениями (XMPP), политики применяются к пользователям XMPP федеративных доменов, но не к пользователям служб мгновенных сообщений в протоколе SIP (например, Windows Live) или федеративных доменах SIP.</span><span class="sxs-lookup"><span data-stu-id="94071-110">When you configure policies for support of extensible messaging and presence protocol (XMPP) federated partners, the policies apply to users of XMPP federated domains, but not to users of session initiation protocol (SIP) instant messaging (IM) service providers (for example, Windows Live), or SIP federated domains.</span></span> <span data-ttu-id="94071-111">Вы настраиваете федеративного партнера XMPP для каждого XMPP федеративного домена, с которым вы хотите разрешить пользователям добавлять контакты и взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="94071-111">You configure an XMPP Federated Partner for each XMPP federated domain that you want to allow your users to add contacts and communicate with.</span></span> <span data-ttu-id="94071-112">После того как политики будут установлены, необходимо настроить сертификаты шлюза XMPP.</span><span class="sxs-lookup"><span data-stu-id="94071-112">Once the policies are in place, you need to configure the XMPP Gateway certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="94071-113">Чтобы начать миграцию шлюза XMPP, необходимо развернуть шлюз Lync Server 2013 XMPP и настроить политики доступа, чтобы включить пользователей для Lync Server 2013 XMPP Gateway.</span><span class="sxs-lookup"><span data-stu-id="94071-113">To begin the XMPP Gateway migration, you need to deploy the Lync Server 2013 XMPP Gateway, and configure access policies to enable users for Lync Server 2013 XMPP Gateway.</span></span> <span data-ttu-id="94071-114">Перед выполнением описанных ниже действий необходимо переместить всех пользователей в развертывание Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="94071-114">All users must be moved to the Lync Server 2013 deployment before you perform these steps.</span></span> <span data-ttu-id="94071-115">Подробности можно найти <A href="configure-xmpp-gateway-on-lync-server-2013.md">в разделе Настройка шлюза XMPP на Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="94071-115">For details, see <A href="configure-xmpp-gateway-on-lync-server-2013.md">Configure XMPP gateway on Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="configure-an-external-access-policy-to-enable-users-for-lync-server-2013-xmpp-gateway"></a><span data-ttu-id="94071-116">Настройка политики внешнего доступа для поддержки пользователей Lync Server 2013 XMPP Gateway</span><span class="sxs-lookup"><span data-stu-id="94071-116">Configure an External Access Policy to Enable Users for Lync Server 2013 XMPP Gateway</span></span>

1.  <span data-ttu-id="94071-117">Откройте Панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="94071-117">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="94071-118">На панели навигации слева выберите пункт **интеграция и внешний доступ**, а затем — **Политика внешнего доступа**.</span><span class="sxs-lookup"><span data-stu-id="94071-118">In the left navigation bar, click **Federation and External Access**, and then click **External Access Policy**.</span></span>

3.  <span data-ttu-id="94071-119">Нажмите кнопку **создать** , а затем выберите пункт **Политика пользователя**.</span><span class="sxs-lookup"><span data-stu-id="94071-119">Click **New** and then click **User policy**.</span></span>

4.  <span data-ttu-id="94071-120">Введите имя для политики пользователей внешнего доступа.</span><span class="sxs-lookup"><span data-stu-id="94071-120">Enter a name for the external access user policy.</span></span>

5.  <span data-ttu-id="94071-121">Введите описание для политики пользователей внешнего доступа.</span><span class="sxs-lookup"><span data-stu-id="94071-121">Provide a description for external access user policy.</span></span>

6.  <span data-ttu-id="94071-122">Выберите **включить связь с федеративными пользователями**.</span><span class="sxs-lookup"><span data-stu-id="94071-122">Select **Enable communications with federated users**.</span></span>

7.  <span data-ttu-id="94071-123">Выберите **включить связь с федеративными пользователями XMPP**.</span><span class="sxs-lookup"><span data-stu-id="94071-123">Select **Enable communications with XMPP federated users**.</span></span>

8.  <span data-ttu-id="94071-124">Нажмите **кнопку Сохранить,** чтобы сохранить изменения в политике сайта или пользователя.</span><span class="sxs-lookup"><span data-stu-id="94071-124">Click **Commit** to save your changes to the site or user policy.</span></span>

<span data-ttu-id="94071-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="94071-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

