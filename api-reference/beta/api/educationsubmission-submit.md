---
title: 'educationSubmission: Отправка'
description: Действие, которое указывает, что студента выполняется с работой и готов к передаче в назначении. Это действие может быть занято только учащегося.
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 3f67e5b07ed1093ee63e9b6fdf7647fa6891dacc
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29510773"
---
# <a name="educationsubmission-submit"></a><span data-ttu-id="1b7ca-104">educationSubmission: Отправка</span><span class="sxs-lookup"><span data-stu-id="1b7ca-104">educationSubmission: submit</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="1b7ca-105">Действие, которое указывает, что студента выполняется с работой и готов к передаче в назначении.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-105">An action that indicates that a student is done with the work and is ready to hand in the assignment.</span></span> <span data-ttu-id="1b7ca-106">Это действие может быть занято только учащегося.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-106">This action can only be taken by the student.</span></span> <span data-ttu-id="1b7ca-107">Это будет изменено состояние отправки из «рабочий» на «отправленные».</span><span class="sxs-lookup"><span data-stu-id="1b7ca-107">This will change the status of the submission from "working" to "submitted".</span></span> <span data-ttu-id="1b7ca-108">Во время процесса отправки интервалов submittedResources будут скопированы все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-108">During the submit process, all the resources will be copied to the submittedResources bucket.</span></span> <span data-ttu-id="1b7ca-109">Преподаватель выполнит поиск в списке добавленных ресурсы для ранжирования.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-109">The teacher will be looking at the submitted resources list for grading.</span></span>

## <a name="permissions"></a><span data-ttu-id="1b7ca-110">Разрешения</span><span class="sxs-lookup"><span data-stu-id="1b7ca-110">Permissions</span></span>
<span data-ttu-id="1b7ca-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b7ca-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1b7ca-113">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="1b7ca-113">Permission type</span></span>      | <span data-ttu-id="1b7ca-114">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="1b7ca-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1b7ca-115">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="1b7ca-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="1b7ca-116">EduAssignments.ReadWriteBasic EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1b7ca-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="1b7ca-117">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="1b7ca-117">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="1b7ca-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-118">Not supported.</span></span>  |
|<span data-ttu-id="1b7ca-119">Для приложений</span><span class="sxs-lookup"><span data-stu-id="1b7ca-119">Application</span></span> | <span data-ttu-id="1b7ca-120">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-120">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1b7ca-121">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="1b7ca-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/submit

```
## <a name="request-headers"></a><span data-ttu-id="1b7ca-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="1b7ca-122">Request headers</span></span>
| <span data-ttu-id="1b7ca-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1b7ca-123">Header</span></span>       | <span data-ttu-id="1b7ca-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1b7ca-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1b7ca-125">Авторизация</span><span class="sxs-lookup"><span data-stu-id="1b7ca-125">Authorization</span></span>  | <span data-ttu-id="1b7ca-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1b7ca-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="1b7ca-128">Request body</span></span>
<span data-ttu-id="1b7ca-129">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1b7ca-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="1b7ca-130">Response</span></span>
<span data-ttu-id="1b7ca-p105">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b7ca-133">Пример</span><span class="sxs-lookup"><span data-stu-id="1b7ca-133">Example</span></span>
<span data-ttu-id="1b7ca-134">В приведенном ниже примере показано, как вызывать этот API.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-134">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1b7ca-135">Запрос</span><span class="sxs-lookup"><span data-stu-id="1b7ca-135">Request</span></span>
<span data-ttu-id="1b7ca-136">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_submit"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/submit
```

##### <a name="response"></a><span data-ttu-id="1b7ca-137">Ответ</span><span class="sxs-lookup"><span data-stu-id="1b7ca-137">Response</span></span>
<span data-ttu-id="1b7ca-138">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="1b7ca-138">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "educationSubmission: submit",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/educationsubmission-submit.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
