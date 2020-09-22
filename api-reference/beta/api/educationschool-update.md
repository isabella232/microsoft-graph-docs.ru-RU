---
title: Обновление свойств educationSchool
description: Обновление свойств объекта school.
author: mmast-msft
localization_priority: Normal
ms.prod: education
doc_type: apiPageType
ms.openlocfilehash: c4fb5d13264a653c8eda5856103334e348e66512
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47991336"
---
# <a name="update-educationschool-properties"></a><span data-ttu-id="a5f53-103">Обновление свойств educationSchool</span><span class="sxs-lookup"><span data-stu-id="a5f53-103">Update educationschool properties</span></span>

<span data-ttu-id="a5f53-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="a5f53-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="a5f53-105">Обновление свойств объекта school.</span><span class="sxs-lookup"><span data-stu-id="a5f53-105">Update the properties of a school object.</span></span>

## <a name="permissions"></a><span data-ttu-id="a5f53-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="a5f53-106">Permissions</span></span>

<span data-ttu-id="a5f53-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5f53-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a5f53-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="a5f53-109">Permission type</span></span>                        | <span data-ttu-id="a5f53-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="a5f53-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="a5f53-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a5f53-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="a5f53-112">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a5f53-112">Not supported.</span></span>                              |
| <span data-ttu-id="a5f53-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a5f53-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5f53-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a5f53-114">Not supported.</span></span>                              |
| <span data-ttu-id="a5f53-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="a5f53-115">Application</span></span>                            | <span data-ttu-id="a5f53-116">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a5f53-116">EduRoster.ReadWrite.All</span></span>                     |

## <a name="http-request"></a><span data-ttu-id="a5f53-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="a5f53-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/schools/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a5f53-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="a5f53-118">Request headers</span></span>

| <span data-ttu-id="a5f53-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a5f53-119">Header</span></span>        | <span data-ttu-id="a5f53-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a5f53-120">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="a5f53-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="a5f53-121">Authorization</span></span> | <span data-ttu-id="a5f53-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a5f53-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a5f53-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a5f53-124">Content-Type</span></span>  | <span data-ttu-id="a5f53-125">application/json</span><span class="sxs-lookup"><span data-stu-id="a5f53-125">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="a5f53-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="a5f53-126">Request body</span></span>

<span data-ttu-id="a5f53-127">В тексте запроса укажите значения для соответствующих полей, которые необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="a5f53-127">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="a5f53-128">Предыдущие значения существующих свойств, не включенных в текст запроса, останутся прежними или будут повторно вычислены с учетом измененных значений других свойств.</span><span class="sxs-lookup"><span data-stu-id="a5f53-128">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="a5f53-129">Для достижения оптимальной производительности не включайте существующие значения, которые не изменились.</span><span class="sxs-lookup"><span data-stu-id="a5f53-129">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a5f53-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="a5f53-130">Property</span></span>            | <span data-ttu-id="a5f53-131">Тип</span><span class="sxs-lookup"><span data-stu-id="a5f53-131">Type</span></span>                                               | <span data-ttu-id="a5f53-132">Описание</span><span class="sxs-lookup"><span data-stu-id="a5f53-132">Description</span></span>                        |
| :------------------ | :------------------------------------------------- | :--------------------------------- |
| <span data-ttu-id="a5f53-133">displayName</span><span class="sxs-lookup"><span data-stu-id="a5f53-133">displayName</span></span>         | <span data-ttu-id="a5f53-134">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-134">String</span></span>                                             | <span data-ttu-id="a5f53-135">Отображаемое имя школы</span><span class="sxs-lookup"><span data-stu-id="a5f53-135">Display name of the school</span></span>         |
| <span data-ttu-id="a5f53-136">description</span><span class="sxs-lookup"><span data-stu-id="a5f53-136">description</span></span>         | <span data-ttu-id="a5f53-137">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-137">String</span></span>                                             | <span data-ttu-id="a5f53-138">Описание школы</span><span class="sxs-lookup"><span data-stu-id="a5f53-138">Description of the school</span></span>          |
| <span data-ttu-id="a5f53-139">principalEmail</span><span class="sxs-lookup"><span data-stu-id="a5f53-139">principalEmail</span></span>      | <span data-ttu-id="a5f53-140">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-140">String</span></span>                                             | <span data-ttu-id="a5f53-141">Адрес электронной почты директора</span><span class="sxs-lookup"><span data-stu-id="a5f53-141">Email address of the principal</span></span>     |
| <span data-ttu-id="a5f53-142">principalName</span><span class="sxs-lookup"><span data-stu-id="a5f53-142">principalName</span></span>       | <span data-ttu-id="a5f53-143">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-143">String</span></span>                                             | <span data-ttu-id="a5f53-144">Имя директора</span><span class="sxs-lookup"><span data-stu-id="a5f53-144">Name of the principal</span></span>              |
| <span data-ttu-id="a5f53-145">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a5f53-145">externalPrincipalId</span></span> | <span data-ttu-id="a5f53-146">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-146">String</span></span>                                             | <span data-ttu-id="a5f53-147">Идентификатор директора в системе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a5f53-147">Id of principal in syncing system.</span></span> |
| <span data-ttu-id="a5f53-148">highestGrade</span><span class="sxs-lookup"><span data-stu-id="a5f53-148">highestGrade</span></span>        | <span data-ttu-id="a5f53-149">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-149">String</span></span>                                             | <span data-ttu-id="a5f53-150">Самый старший класс.</span><span class="sxs-lookup"><span data-stu-id="a5f53-150">Highest grade taught.</span></span>              |
| <span data-ttu-id="a5f53-151">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="a5f53-151">lowestGrade</span></span>         | <span data-ttu-id="a5f53-152">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-152">String</span></span>                                             | <span data-ttu-id="a5f53-153">Самый младший класс.</span><span class="sxs-lookup"><span data-stu-id="a5f53-153">Lowest grade taught.</span></span>               |
| <span data-ttu-id="a5f53-154">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="a5f53-154">schoolNumber</span></span>        | <span data-ttu-id="a5f53-155">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-155">String</span></span>                                             | <span data-ttu-id="a5f53-156">Номер школы.</span><span class="sxs-lookup"><span data-stu-id="a5f53-156">School Number.</span></span>                     |
| <span data-ttu-id="a5f53-157">externalId</span><span class="sxs-lookup"><span data-stu-id="a5f53-157">externalId</span></span>          | <span data-ttu-id="a5f53-158">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-158">String</span></span>                                             | <span data-ttu-id="a5f53-159">Идентификатор учебного заведения в системе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a5f53-159">Id of school in syncing system.</span></span>    |
| <span data-ttu-id="a5f53-160">phone</span><span class="sxs-lookup"><span data-stu-id="a5f53-160">phone</span></span>               | <span data-ttu-id="a5f53-161">String</span><span class="sxs-lookup"><span data-stu-id="a5f53-161">String</span></span>                                             | <span data-ttu-id="a5f53-162">Номер телефона учебного заведения.</span><span class="sxs-lookup"><span data-stu-id="a5f53-162">Phone number of school.</span></span>            |
| <span data-ttu-id="a5f53-163">address</span><span class="sxs-lookup"><span data-stu-id="a5f53-163">address</span></span>             | [<span data-ttu-id="a5f53-164">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="a5f53-164">physicalAddress</span></span>](../resources/physicaladdress.md) | <span data-ttu-id="a5f53-165">Адрес учебного заведения.</span><span class="sxs-lookup"><span data-stu-id="a5f53-165">Address of the School.</span></span>             |
| <span data-ttu-id="a5f53-166">createdBy</span><span class="sxs-lookup"><span data-stu-id="a5f53-166">createdBy</span></span>           | [<span data-ttu-id="a5f53-167">identitySet</span><span class="sxs-lookup"><span data-stu-id="a5f53-167">identitySet</span></span>](../resources/identityset.md)         | <span data-ttu-id="a5f53-168">Объект, который создал учебное заведение.</span><span class="sxs-lookup"><span data-stu-id="a5f53-168">Entity who created the school.</span></span>     |

## <a name="response"></a><span data-ttu-id="a5f53-169">Отклик</span><span class="sxs-lookup"><span data-stu-id="a5f53-169">Response</span></span>
<span data-ttu-id="a5f53-170">При успешном выполнении этот метод возвратит код отклика `200 OK` и обновленный объект [educationSchool](../resources/educationschool.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="a5f53-170">If successful, this method returns a `200 OK` response code and an updated [educationSchool](../resources/educationschool.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5f53-171">Пример</span><span class="sxs-lookup"><span data-stu-id="a5f53-171">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a5f53-172">Запрос</span><span class="sxs-lookup"><span data-stu-id="a5f53-172">Request</span></span>

<span data-ttu-id="a5f53-173">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="a5f53-173">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="a5f53-174">HTTP</span><span class="sxs-lookup"><span data-stu-id="a5f53-174">HTTP</span></span>](#tab/http)

<!-- {
  "blockType": "request",
  "name": "update_educationschool"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/schools/10002
Content-type: application/json
Content-length: 292

{
  "displayName": "Fabrikam Arts High School",
  "description": "Magnate school for the arts. Los Angeles School District"
}
```
# <a name="c"></a>[<span data-ttu-id="a5f53-175">C#</span><span class="sxs-lookup"><span data-stu-id="a5f53-175">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-educationschool-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]
# <a name="javascript"></a>[<span data-ttu-id="a5f53-176">JavaScript</span><span class="sxs-lookup"><span data-stu-id="a5f53-176">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-educationschool-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]
# <a name="objective-c"></a>[<span data-ttu-id="a5f53-177">Objective-C</span><span class="sxs-lookup"><span data-stu-id="a5f53-177">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-educationschool-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="a5f53-178">Отклик</span><span class="sxs-lookup"><span data-stu-id="a5f53-178">Response</span></span>

<span data-ttu-id="a5f53-179">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="a5f53-179">The following is an example of the response.</span></span>

><span data-ttu-id="a5f53-p104">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="a5f53-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 292

{
  "id": "10002",
  "displayName": "Fabrikam Arts High School",
  "description": "Magnate school for the arts. Los Angeles School District",
  "status": "String",
  "externalSource": "String",
  "principalEmail": "AmyR@fabrikam.com",
  "principalName": "Amy Roebuck",
  "externalPrincipalId": "14007",
  "highestGrade": "12",
  "lowestGrade": "9",
  "schoolNumber": "10002",
  "address": {
    "city": "Los Angeles",
    "countryOrRegion": "United States",
    "postalCode": "98055",
    "state": "CA",
    "street": "12345 Main St."
  },
  "externalId": "10002",
  "phone": "+1 (253) 555-0102"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Update educationschool",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


