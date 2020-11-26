---
title: 'Lync Server 2013: настройка файла определений XSLT'
description: 'Lync Server 2013: Настройка файла определения XSLT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Customizing the XSLT definition file
ms:assetid: f18dd78c-3598-4f38-b496-96b750c6e518
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ679898(v=OCS.15)
ms:contentKeyID: 49557733
ms.date: 09/11/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b248b44c9257fa9f30cc99a3773abf71ddbd8651
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431332"
---
# <a name="customizing-the-xslt-definition-file-in-lync-server-2013"></a><span data-ttu-id="2c4b2-103">Настройка файла определений XSLT в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c4b2-103">Customizing the XSLT definition file in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c4b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c4b2-104">

<span> </span></span></span>

<span data-ttu-id="2c4b2-105">_**Тема последнего изменения:** 2014-09-11_</span><span class="sxs-lookup"><span data-stu-id="2c4b2-105">_**Topic Last Modified:** 2014-09-11_</span></span>

<span data-ttu-id="2c4b2-106">Служба соответствия записывает и архивирует данные, связанные с каждым сервером Lync Server 2013, сохраняемым разговором с сервером чата, в том числе если участником:</span><span class="sxs-lookup"><span data-stu-id="2c4b2-106">The Compliance service records and archives data related to each Lync Server 2013, Persistent Chat Server conversation, including when a participant:</span></span>

  - <span data-ttu-id="2c4b2-107">Присоединение к сохраняемой комнате чата</span><span class="sxs-lookup"><span data-stu-id="2c4b2-107">Joins a Persistent Chat room</span></span>

  - <span data-ttu-id="2c4b2-108">покидает комнату чата;</span><span class="sxs-lookup"><span data-stu-id="2c4b2-108">Leaves a chat room</span></span>

  - <span data-ttu-id="2c4b2-109">публикует сообщение;</span><span class="sxs-lookup"><span data-stu-id="2c4b2-109">Posts a message</span></span>

  - <span data-ttu-id="2c4b2-110">просматривает историю чата;</span><span class="sxs-lookup"><span data-stu-id="2c4b2-110">Views chat history</span></span>

  - <span data-ttu-id="2c4b2-111">отправляет файл;</span><span class="sxs-lookup"><span data-stu-id="2c4b2-111">Uploads a file</span></span>

  - <span data-ttu-id="2c4b2-112">загружает файл.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-112">Downloads a file</span></span>

<span data-ttu-id="2c4b2-113">Данные доставляются в формате XML, который можно преобразовать в формат, который наилучшим образом подходит для вашей организации, с помощью файла определения XSLT.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-113">The data is delivered as XML, which you can transform into the format that best fits your organization, by using an XSLT definition file.</span></span> <span data-ttu-id="2c4b2-114">Этот раздел содержит описание файла XML, созданного с помощью службы проверки совместимости.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-114">This topic describes the XML file that the Compliance service creates.</span></span> <span data-ttu-id="2c4b2-115">Приведены также примеры файла определения XSLT и выходного файла.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-115">It also provides samples of XSLT definition and output files.</span></span>

<div>

## <a name="output-format"></a><span data-ttu-id="2c4b2-116">Выходной формат</span><span class="sxs-lookup"><span data-stu-id="2c4b2-116">Output Format</span></span>

<span data-ttu-id="2c4b2-117">Выходные данные службы соответствия подразделяются на обсуждения (элемент CONVERSATION), а затем в сообщении (элемент Messages), как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-117">The Compliance service output is categorized by conversation (the Conversation element) and then by message (the Messages element), as shown in the following code sample.</span></span>

    <?xml version="1.0" encoding="utf-8" ?> 
    <Conversations xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <Conversation>
        <Channel uri="ma-chan://litwareinc.com/300" name="ma-chan://litwareinc.com/300" islogged="" /> 
        <!--FirstMessage goes here --!>
        <Messages> 
          <!—Messages go here--!>
        </Messages>
        <StartTimeUTC since1970="1212610540953" string="2008-06-04T20:15:40.9535482Z" long="633482073409535482" /> 
        <EndTimeUTC since1970="1212610602532" string="2008-06-04T20:16:42.5324614Z" long="633482074025324614" /> 
      </Conversation>
    </Conversations>

<span data-ttu-id="2c4b2-118">Элемент Conversation содержит четыре элемента (Channel, FirstMessage, StartTimeUTC и EndTimeUTC).</span><span class="sxs-lookup"><span data-stu-id="2c4b2-118">A Conversation element contains four elements (Channel, FirstMessage, StartTimeUTC, and EndTimeUTC).</span></span> <span data-ttu-id="2c4b2-119">Элемент Channel содержит код URI, назначенный комнате чата, а элемент FirstMessage описывает первое сообщение в элементе Messages.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-119">The Channel element contains the Uniform Resource Identifier (URI) of the chat room, and the FirstMessage element describes the first message in the Messages element.</span></span> <span data-ttu-id="2c4b2-120">Элементы StartTimeUTC и EndTimeUTC предоставляют начальные и конечные значения для беседы, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-120">The StartTimeUTC and EndTimeUTC elements provide the start and end times for the conversation, as shown in the following code sample.</span></span>

    <<FirstMessage type="JOIN" content="" id="0">
          <Sender UserName="TestUser kazuto" id="10" email="kazuto@litwareinc.com" internal="true" uri="kazuto@litwareinc.com" /> 
          <DateTimeUTC since1970="1212610540953" string="2008-06-04T20:15:40.9535482Z" long="633482073409535482" /> 
    </FirstMessage>

<span data-ttu-id="2c4b2-121">Элемент Message содержит два элемента (Sender и DateTimeUTC) и три атрибута (Type, Content и ID).</span><span class="sxs-lookup"><span data-stu-id="2c4b2-121">A Message element contains two elements (Sender and DateTimeUTC) and three attributes (Type, Content, and ID).</span></span> <span data-ttu-id="2c4b2-122">Элемент sender представляет пользователя, который отправляет сообщение, а элемент DateTimeUTC — при возникновении события, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-122">The Sender element represents the user who sends the message, and the DateTimeUTC element represents when an event occurs, as shown in the following code sample.</span></span>

    <Message type="JOIN" content="" id="0">
      <Sender UserName="TestUser kazuto" id="10" email="kazuto@litwareinc.com" internal="true" uri="kazuto@litwareinc.com" /> 
      <DateTimeUTC since1970="1206211842612" string="2008-03-22T18:50:42.6127374Z" long="633418086426127374" /> 
    </Message>

<span data-ttu-id="2c4b2-123">В следующей таблице показаны атрибуты сообщений Type, Content и ID.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-123">The following table describes the message attributes Type, Content, and ID.</span></span>

### <a name="messages-element-attributes"></a><span data-ttu-id="2c4b2-124">Атрибуты элемента Messages</span><span class="sxs-lookup"><span data-stu-id="2c4b2-124">Messages Element Attributes</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c4b2-125">Атрибут</span><span class="sxs-lookup"><span data-stu-id="2c4b2-125">Attribute</span></span></th>
<th><span data-ttu-id="2c4b2-126">Описание</span><span class="sxs-lookup"><span data-stu-id="2c4b2-126">Description</span></span></th>
<th><span data-ttu-id="2c4b2-127">Применение</span><span class="sxs-lookup"><span data-stu-id="2c4b2-127">Optional/Required</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-128">Тип</span><span class="sxs-lookup"><span data-stu-id="2c4b2-128">Type</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-p104">Указывает тип сообщения. Типы сообщений описаны в таблице типов сообщений элемента Message.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-p104">Specifies the message type. The message types are described in the Message Elements Message Types table.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-131">Required</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c4b2-132">Content</span><span class="sxs-lookup"><span data-stu-id="2c4b2-132">Content</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-p105">Представляет собой содержимое сообщения. Для сообщений с типом Join или Part этот атрибут не используется.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-p105">Contains the content of the message. Messages with a Type of Join or Part do not use this attribute.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-135">Необязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-135">Optional</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-136">ID</span><span class="sxs-lookup"><span data-stu-id="2c4b2-136">ID</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-p106">Указывает уникальный идентификатор содержимого. Этот атрибут используется только с сообщениями, имеющими тип Chat.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-p106">Specifies the unique ID of the content. This attribute is used only with messages with a Type of Chat.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-139">Необязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-139">Optional</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c4b2-p107">Каждый элемент Sender содержит пять атрибутов: имя пользователя, идентификатор, адрес электронной почты, принадлежность ко внутренним пользователям и URI-код. Эти атрибуты описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-p107">Each Sender element contains five attributes: the user name, ID, email, internal, and URI. These attributes are described in the following table.</span></span>

### <a name="sender-element-attributes"></a><span data-ttu-id="2c4b2-142">Атрибуты элемента Sender</span><span class="sxs-lookup"><span data-stu-id="2c4b2-142">Sender Element Attributes</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c4b2-143">Атрибут</span><span class="sxs-lookup"><span data-stu-id="2c4b2-143">Attribute</span></span></th>
<th><span data-ttu-id="2c4b2-144">Описание</span><span class="sxs-lookup"><span data-stu-id="2c4b2-144">Description</span></span></th>
<th><span data-ttu-id="2c4b2-145">Применение</span><span class="sxs-lookup"><span data-stu-id="2c4b2-145">Optional/Required</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-146">Username</span><span class="sxs-lookup"><span data-stu-id="2c4b2-146">Username</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-147">Имя отправителя.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-147">The name of the sender.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-148">Необязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-148">Optional</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c4b2-149">ID</span><span class="sxs-lookup"><span data-stu-id="2c4b2-149">ID</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-150">Уникальный идентификатор отправителя.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-150">The sender’s unique ID.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-151">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-151">Required</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-152">Email</span><span class="sxs-lookup"><span data-stu-id="2c4b2-152">Email</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-153">Адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-153">The sender’s email address.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-154">Необязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-154">Optional</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c4b2-155">Internal</span><span class="sxs-lookup"><span data-stu-id="2c4b2-155">Internal</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-p108">Определяет, является ли пользователь внутренним или федеративным. Если задано значение true, пользователь является внутренним.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-p108">Determines whether the user is an internal user or a federated user. If the value is set to true, the user is internal.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-158">Необязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-158">Optional</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-159">Uri</span><span class="sxs-lookup"><span data-stu-id="2c4b2-159">Uri</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-160">Пользовательский URI для SIP.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-160">The user’s SIP URI.</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-161">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2c4b2-161">Required</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c4b2-p109">В следующей таблице показаны типы сообщений, которые может содержать элемент Messages. Здесь также представлен пример использования каждого из элементов.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-p109">The following table describes the message types that the Messages element can contain. It also provides examples of how each element is used.</span></span>

### <a name="message-element-message-types"></a><span data-ttu-id="2c4b2-164">Типы сообщений элемента Message</span><span class="sxs-lookup"><span data-stu-id="2c4b2-164">Message Element Message Types</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c4b2-165">Тип сообщения</span><span class="sxs-lookup"><span data-stu-id="2c4b2-165">Message Type</span></span></th>
<th><span data-ttu-id="2c4b2-166">Описание</span><span class="sxs-lookup"><span data-stu-id="2c4b2-166">Description</span></span></th>
<th><span data-ttu-id="2c4b2-167">Пример кода</span><span class="sxs-lookup"><span data-stu-id="2c4b2-167">Code example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-168">Join</span><span class="sxs-lookup"><span data-stu-id="2c4b2-168">Join</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-169">Пользователь присоединяется к комнате чата.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-169">A user joins a chat room.</span></span></p></td>
<td><pre><code>&lt;Message type=&quot;JOIN&quot; content=&quot;&quot; id=&quot;0&quot;&gt;
  &lt;Sender UserName=&quot;TestUser kazuto&quot; id=&quot;10&quot; email=&quot;kazuto@litwareinc.com&quot; internal=&quot;true&quot; uri=&quot;kazuto@litwareinc.com&quot; /&gt; 
  &lt;DateTimeUTC since1970=&quot;1206211842612&quot; string=&quot;2008-03-22T18:50:42.6127374Z&quot; long=&quot;633418086426127374&quot; /&gt; 
&lt;/Message</code></pre></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c4b2-170">Part</span><span class="sxs-lookup"><span data-stu-id="2c4b2-170">Part</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-171">Пользователь покидает комнату чата.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-171">A user leaves a chat room.</span></span></p></td>
<td><pre><code>&lt;Message type=&quot;PART&quot; content=&quot;&quot; id=&quot;0&quot;&gt;
  &lt; Sender UserName=&quot;TestUser kazuto&quot; id=&quot;10&quot; email=&quot;kazuto@litwareinc.com&quot; internal=&quot;true&quot; uri=&quot;kazuto@litwareinc.com&quot; /&gt; 
  &lt;DateTimeUTC since1970=&quot;1212610602532&quot; string=&quot;2008-06-04T20:16:42.5324614Z&quot; long=&quot;633482074025324614&quot; /&gt; 
&lt;/Message&gt;</code></pre></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-172">Chat</span><span class="sxs-lookup"><span data-stu-id="2c4b2-172">Chat</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-173">Адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-173">The sender’s email address.</span></span></p></td>
<td><pre><code>&lt;Message type=&quot;CHAT&quot; content=&quot;hello&quot; id=&quot;1&quot;&gt;
  &lt;Sender UserName=&quot;TestUser kazuto&quot; id=&quot;10&quot; email=&quot;kazuto@litwareinc.com&quot; internal=&quot;true&quot; uri=&quot;kazuto@litwareinc.com&quot; /&gt; 
  &lt;DateTimeUTC since1970=&quot;1205351800522&quot; string=&quot;2008-03-12T19:56:40.522264Z&quot; long=&quot;633409486005222640&quot; /&gt; 
&lt;/Message&gt;</code></pre></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c4b2-174">Backchat</span><span class="sxs-lookup"><span data-stu-id="2c4b2-174">Backchat</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-175">Пользователь запрашивает содержимое из истории чата.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-175">A user requests content from chat history.</span></span></p></td>
<td><pre><code>&lt;Message type=&quot;BACKCHAT&quot; content=&quot;backchatcontent&quot; id=&quot;0&quot;&gt;
  &lt;Sender UserName=&quot;TestUser kazuto&quot; id=&quot;10&quot; email=&quot;kazuto@litwareinc.com&quot; internal=&quot;true&quot; uri=&quot;kazuto@litwareinc.com&quot; /&gt; 
  &lt;DateTimeUTC since1970=&quot;1206034385284&quot; string=&quot;2008-03-20T17:33:05.2841594Z&quot; long=&quot;633416311852841594&quot; /&gt; 
&lt;/Message&gt;</code></pre></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c4b2-176">File upload</span><span class="sxs-lookup"><span data-stu-id="2c4b2-176">File upload</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-177">Пользователь отправляет файл.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-177">A user uploads a file.</span></span></p></td>
<td><pre><code>&lt;Message type=&quot;FILEUPLOAD&quot; content=&quot;0988239a-bb66-4616-90a4-b07771a2097c.txt&quot; id=&quot;0&quot;&gt;
  &lt;Sender UserName=&quot;TestUser kazuto&quot; id=&quot;10&quot; email=&quot;kazuto@litwareinc.com&quot; internal=&quot;true&quot; uri=&quot;kazuto@litwareinc.com&quot; /&gt; 
  &lt;DateTimeUTC since1970=&quot;1205351828975&quot; string=&quot;2008-03-12T19:57:08.9755711Z&quot; long=&quot;633409486289755711&quot; /&gt; 
&lt;/Message&gt;</code></pre></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c4b2-178">File download</span><span class="sxs-lookup"><span data-stu-id="2c4b2-178">File download</span></span></p></td>
<td><p><span data-ttu-id="2c4b2-179">Пользователь загружает файл.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-179">A user downloads a file.</span></span></p></td>
<td><pre><code>&lt;Message type=&quot;FILEDOWNLOAD&quot; content=&quot;006074ca-24f0-4b35-8bd8-98006a2d1aa8.txt&quot; id=&quot;0&quot;&gt;
  &lt;Sender UserName=&quot;kazuto@litwareinc.com&quot; id=&quot;10&quot; email=&quot;&quot; internal=&quot;true&quot; uri=&quot;kazuto@litwareinc.com&quot; /&gt; 
  &lt;DateTimeUTC since1970=&quot;1212611141851&quot; string=&quot;2008-06-04T20:25:41.8518646Z&quot; long=&quot;633482079418518646&quot; /&gt; 
&lt;/Message&gt;</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="default-persistent-chat-output-xsd-and-example-xsl-transform"></a><span data-ttu-id="2c4b2-180">Схема выходных данных сохраняемого чата по умолчанию и пример преобразования XSL</span><span class="sxs-lookup"><span data-stu-id="2c4b2-180">Default Persistent Chat Output XSD and Example XSL Transform</span></span>

<span data-ttu-id="2c4b2-181">В следующем образце кода показан вывод по умолчанию на сервере соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-181">The following code sample contains the default output from the Compliance Server.</span></span>

    <?xml version="1.0" encoding="utf-8"?>
    <xs:schema id="Conversations"  xmlns:xs="http://www.w3.org/2001/XMLSchema" xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">
       <xs:simpleType name="ComplianceMessageType">
          <xs:restriction base="xs:string">
            <xs:enumeration value="JOIN"/>
            <xs:enumeration value="PART"/>
            <xs:enumeration value="CHAT"/>
            <xs:enumeration value="BACKCHAT"/>
            <xs:enumeration value="FILEUPLOAD"/>
            <xs:enumeration value="FILEDOWNLOAD"/>
          </xs:restriction>
        </xs:simpleType>
      
      <xs:element name="Sender">
        <xs:complexType>
          <xs:attribute name="UserName" type="xs:string" />
          <xs:attribute name="id" type="xs:int" />
          <xs:attribute name="email" type="xs:string" use="optional" />
          <xs:attribute name="internal" type="xs:boolean" use="optional" >
            <xs:annotation><xs:documentation>If the user is internal or federated</xs:documentation></xs:annotation>
          </xs:attribute>
          <xs:attribute name="uri" type="xs:anyURI" use="optional" />
        </xs:complexType>
      </xs:element>
      <xs:element name="DateTimeUTC">
        <xs:complexType>
          <xs:attribute name="since1970" type="xs:long" />
          <xs:attribute name="string" type="xs:string" />
          <xs:attribute name="long" type="xs:long" />
        </xs:complexType>
      </xs:element>
      <xs:element name="Conversations" msdata:IsDataSet="true" msdata:UseCurrentLocale="true">
        <xs:complexType>
          <xs:choice minOccurs="0" maxOccurs="unbounded">
            <xs:element ref="Sender" />
            <xs:element ref="DateTimeUTC" />
            <xs:element name="Conversation">
              <xs:complexType>
                <xs:sequence>
                  <xs:element name="Channel" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                      <xs:attribute name="uri" type="xs:anyURI" />
                      <xs:attribute name="name" type="xs:string" use="optional" />
                    </xs:complexType>
                  </xs:element>
                  <xs:element name="FirstMessage" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                      <xs:sequence>
                        <xs:element ref="Sender" minOccurs="0" maxOccurs="unbounded" />
                        <xs:element ref="DateTimeUTC" minOccurs="0" maxOccurs="unbounded" />
                      </xs:sequence>
                      <xs:attribute name="type" type="ComplianceMessageType" />
                      <xs:attribute name="content" type="xs:string" />
                      <xs:attribute name="id" type="xs:int" />
                    </xs:complexType>
                  </xs:element>
                  <xs:element name="Messages" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                      <xs:sequence>
                        <xs:element name="Message" minOccurs="0" maxOccurs="unbounded">
                          <xs:complexType>
                            <xs:sequence>
                              <xs:element ref="Sender" minOccurs="0" maxOccurs="unbounded" />
                              <xs:element ref="DateTimeUTC" minOccurs="0" maxOccurs="unbounded" />
                            </xs:sequence>
                            <xs:attribute name="type" type="ComplianceMessageType" />
                            <xs:attribute name="content" type="xs:string" />
                            <xs:attribute name="id" type="xs:int" />
                          </xs:complexType>
                        </xs:element>
                      </xs:sequence>
                    </xs:complexType>
                  </xs:element>
                  <xs:element name="StartTimeUTC" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                      <xs:attribute name="since1970" type="xs:long" />
                      <xs:attribute name="string" type="xs:string" />
                      <xs:attribute name="long" type="xs:long" />
                    </xs:complexType>
                  </xs:element>
                  <xs:element name="EndTimeUTC" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                      <xs:attribute name="since1970" type="xs:long" />
                      <xs:attribute name="string" type="xs:string" />
                      <xs:attribute name="long" type="xs:long" />
                    </xs:complexType>
                  </xs:element>
                </xs:sequence>
              </xs:complexType>
            </xs:element>
          </xs:choice>
        </xs:complexType>
      </xs:element>
    </xs:schema>

<span data-ttu-id="2c4b2-182">В следующем образце кода показан пример преобразования XSL.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-182">The following code sample contains a sample XSL transform.</span></span>

    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xs="http://www.w3.org/2001/XMLSchema" exclude-result-prefixes="xs">
       <xsl:output method="xml" encoding="UTF-8" indent="yes" />
    
       <xsl:template match="/">
          <FileDump>
             <xsl:apply-templates />
          </FileDump>
       </xsl:template>
    
       <xsl:template match="Conversation">
          <xsl:variable name="chanName" select="Channel/@name" />
          <Conversation Perspective="{$chanName}_group_channel">
             <RoomID><xsl:value-of select="Channel/@name" /></RoomID>
             <StartTimeUTC><xsl:value-of select="StartTimeUTC/@since1970" /></StartTimeUTC>
             <xsl:apply-templates />
             <EndTimeUTC><xsl:value-of select="EndTimeUTC/@since1970" /></EndTimeUTC>
          </Conversation>
       </xsl:template>
    
       <xsl:template match="Message">
          <xsl:choose>
             <xsl:when test="@type='JOIN'">
                <ParticipantEntered>
                   <xsl:call-template name="DateTimeAndLogin" />
                   <InternalFlag><xsl:value-of select="Sender/@internal" /></InternalFlag>
                   <ConversationID><xsl:value-of select="../../Channel/@name" /></ConversationID>
                   <CorporateEmailID><xsl:value-of select="Sender/@email" /></CorporateEmailID>
                </ParticipantEntered>
             </xsl:when>
    
             <xsl:when test="@type='PART'">
                <ParticipantLeft>
                   <xsl:call-template name="DateTimeAndLogin" />
                   <InternalFlag><xsl:value-of select="Sender/@internal" /></InternalFlag>
                   <ConversationID><xsl:value-of select="../../Channel/@name" /></ConversationID>
                   <CorporateEmailID><xsl:value-of select="Sender/@email" /></CorporateEmailID>
                </ParticipantLeft>
             </xsl:when>
    
             <xsl:when test="@type='FILEUPLOAD' or @type='FILEDOWNLOAD'">
                <FileTransferStarted>
                   <xsl:call-template name="DateTimeAndLogin" />
                   <FileName><xsl:value-of select="@content" /></FileName>
                </FileTransferStarted>
                <FileTransferEnded>
                   <xsl:call-template name="DateTimeAndLogin" />
                   <FileName><xsl:value-of select="@content" /></FileName>
                   <Status>Completed</Status>
                </FileTransferEnded>
             </xsl:when>
    
             <xsl:when test="@type='CHAT' or @type='BACKCHAT'">
                <Message>
                   <xsl:call-template name="DateTimeAndLogin" />
                   <Content><xsl:value-of select="@content" /></Content>
                </Message>
             </xsl:when>
    
             <xsl:otherwise />
          </xsl:choose>
       </xsl:template>
    
       <xsl:template name="DateTimeAndLogin">
          <LoginName><xsl:value-of select="Sender/@userName" /></LoginName>
          <DateTimeUTC><xsl:value-of select="DateTimeUTC/@since1970" /></DateTimeUTC>
       </xsl:template>
    </xsl:stylesheet>

<span data-ttu-id="2c4b2-183"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c4b2-183"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

