---
title: Создание раздела
description: Создание нового раздела в указанной группе разделов.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: 25c66aa1b1db1f40e3cd9d2b9902288f36ccd766
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32537575"
---
# <a name="create-section"></a><span data-ttu-id="4e45d-103">Создание раздела</span><span class="sxs-lookup"><span data-stu-id="4e45d-103">Create section</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="4e45d-104">Создание нового [раздела](../resources/section.md) в указанной группе разделов.</span><span class="sxs-lookup"><span data-stu-id="4e45d-104">Create a new [section](../resources/section.md) in the specified section group.</span></span>
## <a name="permissions"></a><span data-ttu-id="4e45d-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4e45d-105">Permissions</span></span>
<span data-ttu-id="4e45d-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4e45d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4e45d-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4e45d-108">Permission type</span></span>      | <span data-ttu-id="4e45d-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="4e45d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4e45d-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4e45d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4e45d-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4e45d-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="4e45d-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4e45d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4e45d-113">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4e45d-113">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="4e45d-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="4e45d-114">Application</span></span> | <span data-ttu-id="4e45d-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4e45d-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4e45d-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4e45d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sectionGroups/{id}/sections
POST /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sections
POST /groups/{id}/onenote/sectionGroups/{id}/sections
POST /sites/{id}/onenote/sectionGroups/{id}/sections
```
## <a name="request-headers"></a><span data-ttu-id="4e45d-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4e45d-117">Request headers</span></span>
| <span data-ttu-id="4e45d-118">Имя</span><span class="sxs-lookup"><span data-stu-id="4e45d-118">Name</span></span>       | <span data-ttu-id="4e45d-119">Тип</span><span class="sxs-lookup"><span data-stu-id="4e45d-119">Type</span></span> | <span data-ttu-id="4e45d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4e45d-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4e45d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4e45d-121">Authorization</span></span>  | <span data-ttu-id="4e45d-122">string</span><span class="sxs-lookup"><span data-stu-id="4e45d-122">string</span></span>  | <span data-ttu-id="4e45d-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4e45d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4e45d-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4e45d-125">Content-Type</span></span> | <span data-ttu-id="4e45d-126">string</span><span class="sxs-lookup"><span data-stu-id="4e45d-126">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="4e45d-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="4e45d-127">Request body</span></span>
<span data-ttu-id="4e45d-128">В тексте запроса укажите имя раздела.</span><span class="sxs-lookup"><span data-stu-id="4e45d-128">In the request body, supply a name for the section.</span></span>

<span data-ttu-id="4e45d-p103">В рамках одного и того же уровня иерархии имена разделов должны быть уникальными. Имя должно содержать не более 50 символов, в нем не должно быть следующих знаков:  ?\*\/:<>|&#''%~</span><span class="sxs-lookup"><span data-stu-id="4e45d-p103">Within the same hierarchy level, section names must be unique. The name cannot contain more than 50 characters or contain the following characters:  ?\*\/:<>|&#''%~</span></span>

## <a name="response"></a><span data-ttu-id="4e45d-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="4e45d-131">Response</span></span>

<span data-ttu-id="4e45d-132">В случае успешного выполнения этот метод возвращает код ответа `201 Created` и объект [section](../resources/section.md) в тексте ответа.</span><span class="sxs-lookup"><span data-stu-id="4e45d-132">If successful, this method returns a `201 Created` response code and a [section](../resources/section.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4e45d-133">Пример</span><span class="sxs-lookup"><span data-stu-id="4e45d-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4e45d-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="4e45d-134">Request</span></span>
<span data-ttu-id="4e45d-135">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4e45d-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_section_from_sectiongroup"
}-->
```http
POST https://graph.microsoft.com/beta/me/onenote/sectionGroups/{id}/sections
Content-type: application/json
Content-length: 27

{
  "displayName": "Section name"
}
```

##### <a name="response"></a><span data-ttu-id="4e45d-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="4e45d-136">Response</span></span>
<span data-ttu-id="4e45d-p104">Ниже приведен пример отклика. Примечание. Показанный здесь объект ответа усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="4e45d-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteSection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 272

{
  "isDefault": true,
  "pagesUrl": "pagesUrl-value",
  "displayName": "name-value",  
  "createdBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  },
  "lastModifiedBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create Section",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/sectiongroup-post-sections.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
