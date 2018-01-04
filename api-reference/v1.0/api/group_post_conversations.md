# <a name="create-conversation"></a><span data-ttu-id="89319-101">Создание беседы</span><span class="sxs-lookup"><span data-stu-id="89319-101">Create Conversation</span></span>
<span data-ttu-id="89319-102">Создание объекта [conversation](../resources/conversation.md) путем включения цепочки и записи.</span><span class="sxs-lookup"><span data-stu-id="89319-102">Create a new conversation by including a thread and a post.</span></span> 

<span data-ttu-id="89319-103">Размещать в беседе дальнейшие записи можно с помощью [ответов на цепочки](conversationthread_reply.md) и [ответов на записи](post_reply.md).</span><span class="sxs-lookup"><span data-stu-id="89319-103">Use [reply thread](conversationthread_reply.md) or [reply post](post_reply.md) to further post to that conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="89319-104">Разрешения</span><span class="sxs-lookup"><span data-stu-id="89319-104">Permissions</span></span>
<span data-ttu-id="89319-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="89319-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="89319-107">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="89319-107">Permission type</span></span>      | <span data-ttu-id="89319-108">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="89319-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="89319-109">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="89319-109">Delegated (work or school account)</span></span> | <span data-ttu-id="89319-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="89319-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="89319-111">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="89319-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89319-112">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="89319-112">Not supported.</span></span>    |
|<span data-ttu-id="89319-113">Для приложений</span><span class="sxs-lookup"><span data-stu-id="89319-113">Application</span></span> | <span data-ttu-id="89319-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="89319-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="89319-115">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="89319-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations
```

## <a name="request-headers"></a><span data-ttu-id="89319-116">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="89319-116">Request headers</span></span>
| <span data-ttu-id="89319-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="89319-117">Header</span></span>       | <span data-ttu-id="89319-118">Значение</span><span class="sxs-lookup"><span data-stu-id="89319-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="89319-119">Авторизация</span><span class="sxs-lookup"><span data-stu-id="89319-119">Authorization</span></span>  | <span data-ttu-id="89319-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="89319-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="89319-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="89319-122">Content-Type</span></span>  | <span data-ttu-id="89319-123">application/json</span><span class="sxs-lookup"><span data-stu-id="89319-123">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="89319-124">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="89319-124">Request body</span></span>
<span data-ttu-id="89319-125">Предоставьте в тексте запроса описание объекта [conversation](../resources/conversation.md), содержащего объекты [conversationThread](../resources/conversationThread.md) и [post](../resources/post.md), в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="89319-125">In the request body, supply a JSON representation of [conversation](../resources/conversation.md) object containing a [conversationThread](../resources/conversationThread.md) and a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="89319-126">Отклик</span><span class="sxs-lookup"><span data-stu-id="89319-126">Response</span></span>
<span data-ttu-id="89319-127">В случае успеха этот метод возвращает код отклика `201 Created` и объект [conversation](../resources/conversation.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="89319-127">If successful, this method returns `201 Created` response code and [conversation](../resources/conversation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="89319-128">Пример</span><span class="sxs-lookup"><span data-stu-id="89319-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="89319-129">Запрос</span><span class="sxs-lookup"><span data-stu-id="89319-129">Request</span></span>
<span data-ttu-id="89319-130">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="89319-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversation_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/conversations
Content-type: application/json

{
  "topic": "New Conversation Topic",
  "threads": [{
    "posts": [{
      "body": {
        "contentType": "html",
        "content": "this is body content"
      },
      "newParticipants": [{
        "emailAddress": {
          "name": "Alex Darrow",
          "address": "alexd@contoso.com"
        }
      }]
    }]
  }]
}
```

#### <a name="response"></a><span data-ttu-id="89319-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="89319-131">Response</span></span>
<span data-ttu-id="89319-132">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="89319-132">The following is an example of the response.</span></span>
><span data-ttu-id="89319-133">**Примечание.** Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="89319-133">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="89319-134">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="89319-134">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "datetime-value",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "preview": "preview-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->