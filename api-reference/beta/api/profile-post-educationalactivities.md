---
title: Создание Едукатионалактивити
description: Создание нового Едукатионалактивити.
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: apiPageType
ms.openlocfilehash: 9725e105b59fe941d1842f6cdb49da6d457be6a9
ms.sourcegitcommit: a6d284b3726139f11194aa3d23b8bb79165cc09e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "46808027"
---
# <a name="create-educationalactivity"></a><span data-ttu-id="80203-103">Создание Едукатионалактивити</span><span class="sxs-lookup"><span data-stu-id="80203-103">Create educationalActivity</span></span>

<span data-ttu-id="80203-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="80203-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="80203-105">Создайте новый [едукатионалактивити](../resources/educationalactivity.md) в [профиле](../resources/profile.md)пользователя.</span><span class="sxs-lookup"><span data-stu-id="80203-105">Create a new [educationalActivity](../resources/educationalactivity.md) in a user's [profile](../resources/profile.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="80203-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="80203-106">Permissions</span></span>

<span data-ttu-id="80203-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="80203-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="80203-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="80203-109">Permission type</span></span>                        | <span data-ttu-id="80203-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="80203-110">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="80203-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="80203-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="80203-112">User. ReadWrite, User. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="80203-112">User.ReadWrite, User.ReadWrite.All</span></span>          |
| <span data-ttu-id="80203-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="80203-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="80203-114">User. ReadWrite, User. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="80203-114">User.ReadWrite, User.ReadWrite.All</span></span>          |
| <span data-ttu-id="80203-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="80203-115">Application</span></span>                            | <span data-ttu-id="80203-116">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80203-116">User.ReadWrite.All</span></span>                          |

## <a name="http-request"></a><span data-ttu-id="80203-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="80203-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /user/profile/educationalActivities
POST /users/{id | userPrincipalName}/profile/educationalActivities
```

## <a name="request-headers"></a><span data-ttu-id="80203-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="80203-118">Request headers</span></span>

| <span data-ttu-id="80203-119">Имя</span><span class="sxs-lookup"><span data-stu-id="80203-119">Name</span></span>           |<span data-ttu-id="80203-120">Описание</span><span class="sxs-lookup"><span data-stu-id="80203-120">Description</span></span>                  |
|:---------------|:----------------------------|
| <span data-ttu-id="80203-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="80203-121">Authorization</span></span>  | <span data-ttu-id="80203-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="80203-p102">Bearer {token}. Required.</span></span>   |
| <span data-ttu-id="80203-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="80203-124">Content-Type</span></span>   | <span data-ttu-id="80203-p103">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="80203-p103">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="80203-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="80203-127">Request body</span></span>

<span data-ttu-id="80203-128">В тексте запроса добавьте представление объекта [едукатионалактивити](../resources/educationalactivity.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="80203-128">In the request body, supply a JSON representation of an [educationalActivity](../resources/educationalactivity.md) object.</span></span>

<span data-ttu-id="80203-129">В следующей таблице приведены свойства, которые можно задать при создании нового объекта [едукатионалактивити](../resources/educationalactivity.md) в [профиле](../resources/profile.md)пользователя.</span><span class="sxs-lookup"><span data-stu-id="80203-129">The following table shows the properties that are possible to set when creating a new [educationalActivity](../resources/educationalactivity.md) object in a user's [profile](../resources/profile.md).</span></span>

|<span data-ttu-id="80203-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="80203-130">Property</span></span>|<span data-ttu-id="80203-131">Тип</span><span class="sxs-lookup"><span data-stu-id="80203-131">Type</span></span>|<span data-ttu-id="80203-132">Описание</span><span class="sxs-lookup"><span data-stu-id="80203-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80203-133">алловедаудиенцес</span><span class="sxs-lookup"><span data-stu-id="80203-133">allowedAudiences</span></span>|<span data-ttu-id="80203-134">String</span><span class="sxs-lookup"><span data-stu-id="80203-134">String</span></span>|<span data-ttu-id="80203-135">Аудитории, которые могут видеть значения, содержащиеся в сущности.</span><span class="sxs-lookup"><span data-stu-id="80203-135">The audiences that are able to see the values contained within the entity.</span></span> <span data-ttu-id="80203-136">Наследуется от [итемфацет](../resources/itemfacet.md).</span><span class="sxs-lookup"><span data-stu-id="80203-136">Inherited from [itemFacet](../resources/itemfacet.md).</span></span> <span data-ttu-id="80203-137">Возможные значения: `me`, `family`, `contacts`, `groupMembers`, `organization`, `federatedOrganizations`, `everyone`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="80203-137">Possible values are: `me`, `family`, `contacts`, `groupMembers`, `organization`, `federatedOrganizations`, `everyone`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="80203-138">комплетионмонсеар</span><span class="sxs-lookup"><span data-stu-id="80203-138">completionMonthYear</span></span>|<span data-ttu-id="80203-139">Дата</span><span class="sxs-lookup"><span data-stu-id="80203-139">Date</span></span>|<span data-ttu-id="80203-140">Месяц и год, когда пользователь выполнит или выполнил действие.</span><span class="sxs-lookup"><span data-stu-id="80203-140">The month and year the user graduated or completed the activity.</span></span> |
|<span data-ttu-id="80203-141">ендмонсеар</span><span class="sxs-lookup"><span data-stu-id="80203-141">endMonthYear</span></span>|<span data-ttu-id="80203-142">Дата</span><span class="sxs-lookup"><span data-stu-id="80203-142">Date</span></span>|<span data-ttu-id="80203-143">Месяц и год, когда пользователь завершил действие учебного заведения.</span><span class="sxs-lookup"><span data-stu-id="80203-143">The month and year the user completed the educational activity referenced.</span></span>|
|<span data-ttu-id="80203-144">выводов</span><span class="sxs-lookup"><span data-stu-id="80203-144">inference</span></span>|[<span data-ttu-id="80203-145">инференцедата</span><span class="sxs-lookup"><span data-stu-id="80203-145">inferenceData</span></span>](../resources/inferencedata.md)|<span data-ttu-id="80203-146">Содержит сведения о выводе, если объект создается или изменяется приложением.</span><span class="sxs-lookup"><span data-stu-id="80203-146">Contains inference detail if the entity is inferred by the creating or modifying application.</span></span> <span data-ttu-id="80203-147">Наследуется от [итемфацет](../resources/itemfacet.md).</span><span class="sxs-lookup"><span data-stu-id="80203-147">Inherited from [itemFacet](../resources/itemfacet.md).</span></span>|
|<span data-ttu-id="80203-148">Организация</span><span class="sxs-lookup"><span data-stu-id="80203-148">institution</span></span>|[<span data-ttu-id="80203-149">институтиондата</span><span class="sxs-lookup"><span data-stu-id="80203-149">institutionData</span></span>](../resources/institutiondata.md)|<span data-ttu-id="80203-150">Содержит подробные сведения о учебном заведения.</span><span class="sxs-lookup"><span data-stu-id="80203-150">Contains details of the institution studied at.</span></span> |
|<span data-ttu-id="80203-151">Программа</span><span class="sxs-lookup"><span data-stu-id="80203-151">program</span></span>|[<span data-ttu-id="80203-152">едукатионалактивитидетаил</span><span class="sxs-lookup"><span data-stu-id="80203-152">educationalActivityDetail</span></span>](../resources/educationalactivitydetail.md)|<span data-ttu-id="80203-153">Содержит расширенные сведения о программе или курсе.</span><span class="sxs-lookup"><span data-stu-id="80203-153">Contains extended information about the program or course.</span></span>|
|<span data-ttu-id="80203-154">source</span><span class="sxs-lookup"><span data-stu-id="80203-154">source</span></span>|[<span data-ttu-id="80203-155">персондатасаурце</span><span class="sxs-lookup"><span data-stu-id="80203-155">personDataSource</span></span>](../resources/persondatasource.md)|<span data-ttu-id="80203-156">Источник значений при синхронизации от другой службы.</span><span class="sxs-lookup"><span data-stu-id="80203-156">Where the values originated if synced from another service.</span></span> <span data-ttu-id="80203-157">Наследуется от [итемфацет](../resources/itemfacet.md).</span><span class="sxs-lookup"><span data-stu-id="80203-157">Inherited from [itemFacet](../resources/itemfacet.md).</span></span>|
|<span data-ttu-id="80203-158">стартмонсеар</span><span class="sxs-lookup"><span data-stu-id="80203-158">startMonthYear</span></span>|<span data-ttu-id="80203-159">Дата</span><span class="sxs-lookup"><span data-stu-id="80203-159">Date</span></span>|<span data-ttu-id="80203-160">Месяц и год, когда пользователь присвоено указанному действию.</span><span class="sxs-lookup"><span data-stu-id="80203-160">The month and year the user commenced the activity referenced.</span></span>|

## <a name="response"></a><span data-ttu-id="80203-161">Ответ</span><span class="sxs-lookup"><span data-stu-id="80203-161">Response</span></span>

<span data-ttu-id="80203-162">В случае успешного выполнения этот метод возвращает `201 Created` код отклика и новый объект [едукатионалактивити](../resources/educationalactivity.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="80203-162">If successful, this method returns a `201 Created` response code and a new [educationalActivity](../resources/educationalactivity.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="80203-163">Примеры</span><span class="sxs-lookup"><span data-stu-id="80203-163">Examples</span></span>

### <a name="request"></a><span data-ttu-id="80203-164">Запрос</span><span class="sxs-lookup"><span data-stu-id="80203-164">Request</span></span>

<span data-ttu-id="80203-165">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="80203-165">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="80203-166">HTTP</span><span class="sxs-lookup"><span data-stu-id="80203-166">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_educationalactivity_from_profile"
}-->

```http
POST /me/profile/educationalActivities
Content-type: application/json

{
  "completionMonthYear": "Date",
  "endMonthYear": "Date",
  "institution": {
    "description": null,
    "displayName": "Colorado State University",
    "location": {
      "type": "business",
      "postOfficeBox": null,
      "street": "12000 E Prospect Rd",
      "city": "Fort Collins",
      "state": "Colorado",
      "countryOrRegion": "USA",
      "postalCode": "80525"
    },
    "webUrl": "https://www.colostate.edu"
  },
  "program": {
    "abbreviation": "MBA",
    "activities": null,
    "awards": null,
    "description": "Master of Business Administration with a major in Entreprenuership and Finance.",
    "displayName": "Master of Business Administration",
    "fieldsOfStudy": null,
    "grade": "3.9",
    "notes": null,
    "webUrl": "https://biz.colostate.edu"
  },
  "startMonthYear": "Date"
}
```
# <a name="c"></a>[<span data-ttu-id="80203-167">C#</span><span class="sxs-lookup"><span data-stu-id="80203-167">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-educationalactivity-from-profile-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="80203-168">JavaScript</span><span class="sxs-lookup"><span data-stu-id="80203-168">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-educationalactivity-from-profile-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="80203-169">Objective-C</span><span class="sxs-lookup"><span data-stu-id="80203-169">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-educationalactivity-from-profile-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="80203-170">Отклик</span><span class="sxs-lookup"><span data-stu-id="80203-170">Response</span></span>

<span data-ttu-id="80203-171">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="80203-171">The following is an example of the response.</span></span>

> <span data-ttu-id="80203-p107">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="80203-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationalActivity"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "0fb4c1e3-c1e3-0fb4-e3c1-b40fe3c1b40f",
  "allowedAudiences": "organization",
  "inference": null,
  "createdDateTime": "2020-07-06T06:34:12.2294868Z",
  "createdBy": {
    "application": null,
    "device": null,
    "user": {
      "displayName": "Innocenty Popov",
      "id": "db789417-4ccb-41d1-a0a9-47b01a09ea49"
    }
  },
  "lastModifiedDateTime": "2020-07-06T06:34:12.2294868Z",
  "lastModifiedBy": {
    "application": null,
    "device": null,
    "user": {
      "displayName": "Innocenty Popov",
      "id": "db789417-4ccb-41d1-a0a9-47b01a09ea49"
    }
  },
  "source": null,
  "completionMonthYear": "Date",
  "endMonthYear": "Date",
  "institution": {
    "description": null,
    "displayName": "Colorado State University",
    "location": {
      "type": "business",
      "postOfficeBox": null,
      "street": "12000 E Prospect Rd",
      "city": "Fort Collins",
      "state": "Colorado",
      "countryOrRegion": "USA",
      "postalCode": "80525"
    },
    "webUrl": "https://www.colostate.edu"
  },
  "program": {
    "abbreviation": "MBA",
    "activities": null,
    "awards": null,
    "description": "Master of Business Administration with a major in Entreprenuership and Finance.",
    "displayName": "Master of Business Administration",
    "fieldsOfStudy": null,
    "grade": "3.9",
    "notes": null,
    "webUrl": "https://biz.colostate.edu"
  },
  "startMonthYear": "Date"
}
```
