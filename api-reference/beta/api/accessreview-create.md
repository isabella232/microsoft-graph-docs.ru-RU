---
title: Создание Акцессревиев
description: В средстве проверки доступа Azure AD создайте новый объект Акцессревиев.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: e4bf6715f5c762ffc1b04d29d655cc170d3313cc
ms.sourcegitcommit: ed03445225e98cf0881de08273c36be8d0e576ea
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "40951636"
---
# <a name="create-accessreview"></a><span data-ttu-id="e1d63-103">Создание Акцессревиев</span><span class="sxs-lookup"><span data-stu-id="e1d63-103">Create accessReview</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="e1d63-104">В средстве проверки [доступа](../resources/accessreviews-root.md) Azure AD создайте новый объект [акцессревиев](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d63-104">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, create a new [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="e1d63-105">Перед выполнением этого запроса абонент должен был [получить список шаблонов бизнес-процесса](businessflowtemplate-list.md), чтобы включить в запрос значение `businessFlowTemplateId` для включения в запрос.</span><span class="sxs-lookup"><span data-stu-id="e1d63-105">Before making this request, the caller must have previously [retrieved the list of business flow templates](businessflowtemplate-list.md), to have the value of `businessFlowTemplateId` to include in the request.</span></span>

<span data-ttu-id="e1d63-106">После выполнения этого запроса вызывающий абонент должен [создать програмконтрол](programcontrol-create.md), чтобы связать проверку доступа с программой.</span><span class="sxs-lookup"><span data-stu-id="e1d63-106">After making this request, the caller should [create a programControl](programcontrol-create.md), to link the access review to a program.</span></span>  

## <a name="permissions"></a><span data-ttu-id="e1d63-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="e1d63-107">Permissions</span></span>

<span data-ttu-id="e1d63-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1d63-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1d63-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="e1d63-110">Permission type</span></span>                        | <span data-ttu-id="e1d63-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="e1d63-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1d63-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e1d63-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="e1d63-113">Акцессревиев. ReadWrite. Membership, Акцессревиев. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="e1d63-113">AccessReview.ReadWrite.Membership, AccessReview.ReadWrite.All</span></span> |
|<span data-ttu-id="e1d63-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="e1d63-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1d63-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e1d63-115">Not supported.</span></span> |
|<span data-ttu-id="e1d63-116">Приложение</span><span class="sxs-lookup"><span data-stu-id="e1d63-116">Application</span></span>                            | <span data-ttu-id="e1d63-117">AccessReview.ReadWrite.Membership</span><span class="sxs-lookup"><span data-stu-id="e1d63-117">AccessReview.ReadWrite.Membership</span></span> |

<span data-ttu-id="e1d63-118">Вызывающая сторона также должна иметь разрешение Програмконтрол. ReadWrite. ALL, чтобы после создания проверки доступа вызывающий абонент может создать [програмконтрол](../resources/programcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="e1d63-118">The caller should also have ProgramControl.ReadWrite.All permission, so that after creating an access review, the caller can create a [programControl](../resources/programcontrol.md).</span></span>
<span data-ttu-id="e1d63-119">Кроме того, пользователь, вошедшего в систему, должен быть членом роли каталога, который позволяет им создавать проверку доступа.</span><span class="sxs-lookup"><span data-stu-id="e1d63-119">In addition, the signed in user must also be in a directory role that permits them to create an access review.</span></span>  <span data-ttu-id="e1d63-120">Более подробную информацию можно узнать в статье требования к ролям и разрешениям для [рецензирования Access](../resources/accessreviews-root.md).</span><span class="sxs-lookup"><span data-stu-id="e1d63-120">For more details, see the role and permission requirements for [access reviews](../resources/accessreviews-root.md).</span></span>

## <a name="http-request"></a><span data-ttu-id="e1d63-121">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="e1d63-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews
```
## <a name="request-headers"></a><span data-ttu-id="e1d63-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="e1d63-122">Request headers</span></span>
| <span data-ttu-id="e1d63-123">Имя</span><span class="sxs-lookup"><span data-stu-id="e1d63-123">Name</span></span>         | <span data-ttu-id="e1d63-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e1d63-124">Description</span></span> |
|:-------------|:------------|
| <span data-ttu-id="e1d63-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1d63-125">Authorization</span></span> | <span data-ttu-id="e1d63-126">Носитель \{токен\}.</span><span class="sxs-lookup"><span data-stu-id="e1d63-126">Bearer \{token\}.</span></span> <span data-ttu-id="e1d63-127">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e1d63-127">Required.</span></span> |
| <span data-ttu-id="e1d63-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e1d63-128">Content-type</span></span> | <span data-ttu-id="e1d63-p104">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e1d63-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e1d63-131">Основной текст запроса</span><span class="sxs-lookup"><span data-stu-id="e1d63-131">Request body</span></span>
<span data-ttu-id="e1d63-132">В тексте запроса добавьте представление объекта [акцессревиев](../resources/accessreview.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e1d63-132">In the request body, supply a JSON representation of an [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="e1d63-133">В следующей таблице приведены свойства, необходимые при создании Акцессревиев.</span><span class="sxs-lookup"><span data-stu-id="e1d63-133">The following table shows the properties that are required when you create an accessReview.</span></span>

| <span data-ttu-id="e1d63-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="e1d63-134">Property</span></span>     | <span data-ttu-id="e1d63-135">Тип</span><span class="sxs-lookup"><span data-stu-id="e1d63-135">Type</span></span>        | <span data-ttu-id="e1d63-136">Описание</span><span class="sxs-lookup"><span data-stu-id="e1d63-136">Description</span></span> |
|:-------------|:------------|:------------|
| `displayName`             |`String`                                                        | <span data-ttu-id="e1d63-137">Имя проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="e1d63-137">The access review name.</span></span>  |
| `startDateTime`           |`DateTimeOffset`                                                | <span data-ttu-id="e1d63-138">Дата и время, когда выполняется запланированное начало проверки.</span><span class="sxs-lookup"><span data-stu-id="e1d63-138">The DateTime when the review is scheduled to be start.</span></span>  <span data-ttu-id="e1d63-139">Это должна быть Дата в будущем.</span><span class="sxs-lookup"><span data-stu-id="e1d63-139">This must be a date in the future.</span></span>   |
| `endDateTime`             |`DateTimeOffset`                                                | <span data-ttu-id="e1d63-140">Дата и время окончания запланированного рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="e1d63-140">The DateTime when the review is scheduled to end.</span></span> <span data-ttu-id="e1d63-141">Это должен быть по крайней мере один день позже даты начала.</span><span class="sxs-lookup"><span data-stu-id="e1d63-141">This must be at least one day later than the start date.</span></span>   |
| `description`             |`String`                                                        | <span data-ttu-id="e1d63-142">Описание, которое будет отображаться для рецензентов.</span><span class="sxs-lookup"><span data-stu-id="e1d63-142">The description, to show to the reviewers.</span></span> |
| `businessFlowTemplateId`  |`String`                                                        | <span data-ttu-id="e1d63-143">Идентификатор шаблона рабочего процесса, полученный из объекта [бусинессфловтемплате](../resources/businessflowtemplate.md).</span><span class="sxs-lookup"><span data-stu-id="e1d63-143">The business flow template identifier, obtained from a [businessFlowTemplate](../resources/businessflowtemplate.md).</span></span>  |
| `reviewerType`            |`String`                                                        | <span data-ttu-id="e1d63-144">Тип отношения проверяющего к правам доступа проверенного объекта, один из `self`, `delegated`или. `entityOwners`</span><span class="sxs-lookup"><span data-stu-id="e1d63-144">The relationship type of reviewer to the access rights of the reviewed object, one of `self`, `delegated`, or `entityOwners`.</span></span> | 
| `reviewedEntity`          |`microsoft.graph.identity`                                      | <span data-ttu-id="e1d63-145">Объект, для которого создается проверка доступа, например членство в группе или назначения пользователей приложению.</span><span class="sxs-lookup"><span data-stu-id="e1d63-145">The object for which an access review is created, such as the membership of a group or the assignments of users to an application.</span></span> | 


<span data-ttu-id="e1d63-146">Если предоставленное значение Ревиевертипе имеет значение `delegated`, вызывающая сторона также должна содержать `reviewers` свойство с коллекцией [userIdentity](../resources/useridentity.md) рецензентов.</span><span class="sxs-lookup"><span data-stu-id="e1d63-146">If the reviewerType being supplied has the value `delegated`, then the caller must also include the `reviewers` property, with a collection of [userIdentity](../resources/useridentity.md) of the reviewers.</span></span>

<span data-ttu-id="e1d63-147">Если приложение вызывает этот API без вошедшего пользователя, вызывающая сторона также должна включать свойство **createdBy** , значение которого является [userIdentity](../resources/useridentity.md) пользователя, который будет идентифицирован как создатель проверки.</span><span class="sxs-lookup"><span data-stu-id="e1d63-147">If your app is calling this API without a signed-in user, then the caller must also include the **createdBy** property, the value for which is a [userIdentity](../resources/useridentity.md) of the user who will be identified as the creator of the review.</span></span>

<span data-ttu-id="e1d63-148">Кроме того, вызывающий может включать в себя параметры для создания повторяющихся рядов проверки или для изменения поведения проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1d63-148">In addition, the caller can include settings, to create a recurring review series or to change from the default review behavior.</span></span> <span data-ttu-id="e1d63-149">В частности, чтобы создать повторяющуюся проверку, вызывающая сторона должна включать в себя `accessReviewRecurrenceSettings` параметры проверки доступа,</span><span class="sxs-lookup"><span data-stu-id="e1d63-149">In particular, to create a recurring review, the caller must include the `accessReviewRecurrenceSettings` within the access review settings,</span></span>


## <a name="response"></a><span data-ttu-id="e1d63-150">Отклик</span><span class="sxs-lookup"><span data-stu-id="e1d63-150">Response</span></span>
<span data-ttu-id="e1d63-151">В случае успешного выполнения этот метод возвращает `201, Created` код отклика и объект [акцессревиев](../resources/accessreview.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="e1d63-151">If successful, this method returns a `201, Created` response code and an [accessReview](../resources/accessreview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1d63-152">Пример</span><span class="sxs-lookup"><span data-stu-id="e1d63-152">Example</span></span>

<span data-ttu-id="e1d63-153">Это пример создания одноразовой (не повторяющейся) проверки доступа, явно указав двух пользователей в качестве проверяющих.</span><span class="sxs-lookup"><span data-stu-id="e1d63-153">This is an example of creating a one-time (not recurring) access review, explicitly specifying two users as the reviewers.</span></span>

### <a name="request"></a><span data-ttu-id="e1d63-154">Запрос</span><span class="sxs-lookup"><span data-stu-id="e1d63-154">Request</span></span>
<span data-ttu-id="e1d63-155">В тексте запроса добавьте представление объекта [акцессревиев](../resources/accessreview.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e1d63-155">In the request body, supply a JSON representation of the [accessReview](../resources/accessreview.md) object.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_accessReview_from_accessReviews"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews
Content-type: application/json

{
    "displayName":"TestReview",
    "startDateTime":"2017-02-10T00:35:53.214Z",
    "endDateTime":"2017-03-12T00:35:53.214Z",
    "reviewedEntity": {
        "id": "99025615-a0b1-47ec-9117-35377b10998b",
    },
    "reviewerType" : "delegated",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "description":"Sample description",
    "reviewers":
    [
        {
            "id":"f260246a-09b1-4fd5-8d18-daed736071ec"
        },
        {
            "id":"5a4e184c-4ee5-4883-96e9-b371f8da88e3"
        }
    ],
    "settings":
    {
        "mailNotificationsEnabled": true,
        "remindersEnabled": true,
        "justificationRequiredOnApproval":true,
        "autoReviewEnabled":false,
        "activityDurationInDays":30,
        "autoApplyReviewResultsEnabled":false,
        "accessRecommendationsEnabled":false,
        "recurrenceSettings":{
            "recurrenceType":"onetime",
            "recurrenceEndType":"endBy",
            "durationInDays":0,
            "recurrenceCount":0
        },
        "autoReviewSettings":{
            "notReviewedResult":"Deny"
        }
    }
}
```

### <a name="response"></a><span data-ttu-id="e1d63-156">Отклик</span><span class="sxs-lookup"><span data-stu-id="e1d63-156">Response</span></span>
><span data-ttu-id="e1d63-p108">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="e1d63-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "006111db-0810-4494-a6df-904d368bd81b",
    "displayName": "TestReview",
    "startDateTime": "2017-02-10T00:35:53.214Z",
    "endDateTime": "2017-03-12T00:35:53.214Z",
    "status": "Initializing",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "reviewerType": "delegated",
    "description": "Sample description"
}
```

<!--
{
  "type": "#page.annotation",
  "description": "Create accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
