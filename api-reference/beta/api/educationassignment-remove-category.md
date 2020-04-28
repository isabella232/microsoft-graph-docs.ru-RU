---
title: Удаление Едукатионкатегори
description: Удаление существующего Едукатионкатегори из educationAssignment
localization_priority: Normal
author: dipakboyed
ms.prod: education
doc_type: apiPageType
ms.openlocfilehash: d154f4c46eaeaa84807966b3f78947e09ba01be0
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42427342"
---
# <a name="remove-educationcategory"></a><span data-ttu-id="d3cdf-103">Удаление Едукатионкатегори</span><span class="sxs-lookup"><span data-stu-id="d3cdf-103">Remove educationCategory</span></span>

<span data-ttu-id="d3cdf-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="d3cdf-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d3cdf-105">Удаление [едукатионкатегори](../resources/educationcategory.md) из [educationAssignment](../resources/educationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d3cdf-105">Remove an [educationCategory](../resources/educationcategory.md) from an [educationAssignment](../resources/educationassignment.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="d3cdf-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d3cdf-106">Permissions</span></span>
<span data-ttu-id="d3cdf-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d3cdf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d3cdf-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d3cdf-109">Permission type</span></span>      | <span data-ttu-id="d3cdf-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d3cdf-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d3cdf-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d3cdf-111">Delegated (work or school account)</span></span> |  <span data-ttu-id="d3cdf-112">EduAssignments. Реадвритебасик, EduAssignments. ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d3cdf-112">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="d3cdf-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d3cdf-113">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="d3cdf-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-114">Not supported.</span></span>  |
|<span data-ttu-id="d3cdf-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d3cdf-115">Application</span></span> | <span data-ttu-id="d3cdf-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-116">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="d3cdf-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d3cdf-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/assignments/{id}/categories/{id}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="d3cdf-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d3cdf-118">Request headers</span></span>
| <span data-ttu-id="d3cdf-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d3cdf-119">Header</span></span>       | <span data-ttu-id="d3cdf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d3cdf-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d3cdf-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="d3cdf-121">Authorization</span></span>  | <span data-ttu-id="d3cdf-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d3cdf-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d3cdf-124">Content-Type</span></span>  | <span data-ttu-id="d3cdf-125">application/json</span><span class="sxs-lookup"><span data-stu-id="d3cdf-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d3cdf-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="d3cdf-126">Request body</span></span>
<span data-ttu-id="d3cdf-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-127">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="d3cdf-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="d3cdf-128">Response</span></span>
<span data-ttu-id="d3cdf-129">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-129">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="d3cdf-130">Пример</span><span class="sxs-lookup"><span data-stu-id="d3cdf-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d3cdf-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="d3cdf-131">Request</span></span>
<span data-ttu-id="d3cdf-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "add_educationcategory_to_educationassignment"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/categories/ec98f158-341d-4fea-9f8c-14a250d489ac/$ref
```

##### <a name="response"></a><span data-ttu-id="d3cdf-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="d3cdf-133">Response</span></span>
<span data-ttu-id="d3cdf-134">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-134">The following is an example of the response.</span></span> 

><span data-ttu-id="d3cdf-135">**Примечание.** Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-135">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="d3cdf-136">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-136">All of the properties will be returned from an actual call.</span></span>


<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignmentResource"
} -->
```http
HTTP/1.1 204 No Content
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Remove an educationCategory from an educationAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
