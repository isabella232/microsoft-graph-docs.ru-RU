---
title: Обновление оповещения
description: Обновление редактируемого свойства оповещения в любом интегрированном решении для обеспечения синхронизации состояния и назначений оповещений между решениями.
localization_priority: Normal
author: preetikr
ms.prod: security
doc_type: apiPageType
ms.openlocfilehash: 93a395f78baeec0a6609ea7dee0b9cfbc3e3224b
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36318820"
---
# <a name="update-alert"></a><span data-ttu-id="8db1d-103">Обновление оповещения</span><span class="sxs-lookup"><span data-stu-id="8db1d-103">Update alert</span></span>

 [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="8db1d-104">Обновление редактируемого свойства **оповещения** в любом интегрированном решении для обеспечения синхронизации состояния и назначений оповещений между решениями.</span><span class="sxs-lookup"><span data-stu-id="8db1d-104">Update an editable **alert** property within any integrated solution to keep alert status and assignments in sync across solutions.</span></span> <span data-ttu-id="8db1d-105">Этот метод обновляет любое решение, имеющее запись идентификатора оповещения, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="8db1d-105">This method updates any solution that has a record of the referenced alert ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="8db1d-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="8db1d-106">Permissions</span></span>

<span data-ttu-id="8db1d-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8db1d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8db1d-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="8db1d-109">Permission type</span></span>      | <span data-ttu-id="8db1d-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="8db1d-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8db1d-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8db1d-111">Delegated (work or school account)</span></span> |   <span data-ttu-id="8db1d-112">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8db1d-112">SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="8db1d-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8db1d-113">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="8db1d-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8db1d-114">Not supported.</span></span>  |
|<span data-ttu-id="8db1d-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="8db1d-115">Application</span></span> | <span data-ttu-id="8db1d-116">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8db1d-116">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8db1d-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="8db1d-117">HTTP request</span></span>

> <span data-ttu-id="8db1d-118">**Примечание:** Необходимо включить идентификатор **оповещения** в качестве параметра и вендоринформатион, содержащего метод `provider` и `vendor` с этим методом.</span><span class="sxs-lookup"><span data-stu-id="8db1d-118">**Note:** You must include the **alert** ID as a parameter and vendorInformation containing the `provider` and `vendor` with this method.</span></span>
<!-- { "blockType": "ignored" } -->

```http
PATCH /security/alerts/{alert_id}
```

## <a name="request-headers"></a><span data-ttu-id="8db1d-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="8db1d-119">Request headers</span></span>

| <span data-ttu-id="8db1d-120">Имя</span><span class="sxs-lookup"><span data-stu-id="8db1d-120">Name</span></span>       | <span data-ttu-id="8db1d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8db1d-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="8db1d-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="8db1d-122">Authorization</span></span>  | <span data-ttu-id="8db1d-123">Bearer {код}.</span><span class="sxs-lookup"><span data-stu-id="8db1d-123">Bearer {code}.</span></span> <span data-ttu-id="8db1d-124">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="8db1d-124">Required.</span></span>|
|<span data-ttu-id="8db1d-125">Prefer</span><span class="sxs-lookup"><span data-stu-id="8db1d-125">Prefer</span></span> | <span data-ttu-id="8db1d-126">Возврат = представление</span><span class="sxs-lookup"><span data-stu-id="8db1d-126">return=representation</span></span> |

## <a name="request-body"></a><span data-ttu-id="8db1d-127">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="8db1d-127">Request body</span></span>

<span data-ttu-id="8db1d-128">В тексте запроса добавьте представление значений в формате JSON для соответствующих полей, которые необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="8db1d-128">In the request body, supply a JSON representation of the values for relevant fields that should be updated.</span></span> <span data-ttu-id="8db1d-129">Текст **должен** содержать `vendorInformation` свойство Valid `provider` и `vendor` Fields.</span><span class="sxs-lookup"><span data-stu-id="8db1d-129">The body **must** contain the `vendorInformation` property with valid `provider` and `vendor` fields.</span></span> <span data-ttu-id="8db1d-130">В следующей таблице перечислены поля, которые можно обновить для оповещения.</span><span class="sxs-lookup"><span data-stu-id="8db1d-130">The following table lists the fields that can be updated for an alert.</span></span> <span data-ttu-id="8db1d-131">Значения для существующих свойств, не включенных в текст запроса, не изменятся.</span><span class="sxs-lookup"><span data-stu-id="8db1d-131">The values for existing properties that are not included in the request body will not change.</span></span> <span data-ttu-id="8db1d-132">Для достижения оптимальной производительности не включайте существующие значения, которые не изменились.</span><span class="sxs-lookup"><span data-stu-id="8db1d-132">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8db1d-133">Свойство</span><span class="sxs-lookup"><span data-stu-id="8db1d-133">Property</span></span>   | <span data-ttu-id="8db1d-134">Тип</span><span class="sxs-lookup"><span data-stu-id="8db1d-134">Type</span></span> |<span data-ttu-id="8db1d-135">Описание</span><span class="sxs-lookup"><span data-stu-id="8db1d-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8db1d-136">assignedTo</span><span class="sxs-lookup"><span data-stu-id="8db1d-136">assignedTo</span></span>|<span data-ttu-id="8db1d-137">String</span><span class="sxs-lookup"><span data-stu-id="8db1d-137">String</span></span>|<span data-ttu-id="8db1d-138">Имя аналитика, которому назначено оповещение для рассмотрения, исследования или исправления.</span><span class="sxs-lookup"><span data-stu-id="8db1d-138">Name of the analyst the alert is assigned to for triage, investigation, or remediation.</span></span>|
|<span data-ttu-id="8db1d-139">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="8db1d-139">closedDateTime</span></span>|<span data-ttu-id="8db1d-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8db1d-140">DateTimeOffset</span></span>|<span data-ttu-id="8db1d-141">Время закрытия оповещения.</span><span class="sxs-lookup"><span data-stu-id="8db1d-141">Time at which the alert was closed.</span></span> <span data-ttu-id="8db1d-142">Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC).</span><span class="sxs-lookup"><span data-stu-id="8db1d-142">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="8db1d-143">Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="8db1d-143">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="8db1d-144">comments</span><span class="sxs-lookup"><span data-stu-id="8db1d-144">comments</span></span>|<span data-ttu-id="8db1d-145">Коллекция String</span><span class="sxs-lookup"><span data-stu-id="8db1d-145">String collection</span></span>|<span data-ttu-id="8db1d-146">Комментарии аналитика в оповещении (для управления оповещениями клиентов).</span><span class="sxs-lookup"><span data-stu-id="8db1d-146">Analyst comments on the alert (for customer alert management).</span></span>|
|<span data-ttu-id="8db1d-147">feedback</span><span class="sxs-lookup"><span data-stu-id="8db1d-147">feedback</span></span>|<span data-ttu-id="8db1d-148">Перечисление Алертфидбакк</span><span class="sxs-lookup"><span data-stu-id="8db1d-148">alertFeedback enum</span></span>|<span data-ttu-id="8db1d-149">Отзыв аналитика об оповещении.</span><span class="sxs-lookup"><span data-stu-id="8db1d-149">Analyst feedback on the alert.</span></span> <span data-ttu-id="8db1d-150">Возможные значения: `unknown`, `truePositive`, `falsePositive`, `benignPositive`.</span><span class="sxs-lookup"><span data-stu-id="8db1d-150">Possible values are: `unknown`, `truePositive`, `falsePositive`, `benignPositive`.</span></span>|
|<span data-ttu-id="8db1d-151">status</span><span class="sxs-lookup"><span data-stu-id="8db1d-151">status</span></span>|<span data-ttu-id="8db1d-152">Перечисление Алертстатус</span><span class="sxs-lookup"><span data-stu-id="8db1d-152">alertStatus enum</span></span>|<span data-ttu-id="8db1d-153">Состояние жизненного цикла оповещений (Stage).</span><span class="sxs-lookup"><span data-stu-id="8db1d-153">Alert life cycle status (stage).</span></span> <span data-ttu-id="8db1d-154">Возможные значения: `unknown`, `newAlert`, `inProgress`, `resolved`.</span><span class="sxs-lookup"><span data-stu-id="8db1d-154">Possible values are: `unknown`, `newAlert`, `inProgress`, `resolved`.</span></span>|
|<span data-ttu-id="8db1d-155">tags</span><span class="sxs-lookup"><span data-stu-id="8db1d-155">tags</span></span>|<span data-ttu-id="8db1d-156">Коллекция String</span><span class="sxs-lookup"><span data-stu-id="8db1d-156">String collection</span></span>|<span data-ttu-id="8db1d-157">Определяемые пользователями метки, которые могут быть применены к оповещению и могут использоваться в качестве условий фильтрации (например, "Хва", "показано").</span><span class="sxs-lookup"><span data-stu-id="8db1d-157">User-definable labels that can be applied to an alert and can serve as filter conditions (for example, "HVA", "SAW).</span></span>|
|<span data-ttu-id="8db1d-158">vendorInformation</span><span class="sxs-lookup"><span data-stu-id="8db1d-158">vendorInformation</span></span> |[<span data-ttu-id="8db1d-159">securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="8db1d-159">securityVendorInformation</span></span>](../resources/securityvendorinformation.md)|<span data-ttu-id="8db1d-160">Сложный тип, содержащий подробные сведения о безопасности продавца продукта или услуги, поставщика субпоставщика (например, продавец = Майкрософт; поставщик = ATP в Защитнике Windows; субпоставщик = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="8db1d-160">Complex type containing details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span> <span data-ttu-id="8db1d-161">**Требуются поля поставщика и поставщика.**</span><span class="sxs-lookup"><span data-stu-id="8db1d-161">**Provider and vendor fields are required.**</span></span>|

## <a name="response"></a><span data-ttu-id="8db1d-162">Отклик</span><span class="sxs-lookup"><span data-stu-id="8db1d-162">Response</span></span>

<span data-ttu-id="8db1d-163">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="8db1d-163">If successful, this method returns a `204 No Content` response code.</span></span>

<span data-ttu-id="8db1d-164">Если используется заголовок необязательного запроса, метод возвращает код `200 OK` отклика и обновленный объект [Alert](../resources/alert.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="8db1d-164">If the optional request header is used, the method returns a `200 OK` response code and the updated [alert](../resources/alert.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="8db1d-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="8db1d-165">Examples</span></span>

### <a name="example-1-request-without-prefer-header"></a><span data-ttu-id="8db1d-166">Пример 1: запрос без верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="8db1d-166">Example 1: Request without Prefer header</span></span>

#### <a name="request"></a><span data-ttu-id="8db1d-167">Запрос</span><span class="sxs-lookup"><span data-stu-id="8db1d-167">Request</span></span>

<span data-ttu-id="8db1d-168">Ниже приведен пример запроса без `Prefer` заголовка.</span><span class="sxs-lookup"><span data-stu-id="8db1d-168">The following is an example of the request without the `Prefer` header.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="8db1d-169">HTTP</span><span class="sxs-lookup"><span data-stu-id="8db1d-169">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/beta/security/alerts/{alert_id}
Content-type: application/json

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="8db1d-170">C#</span><span class="sxs-lookup"><span data-stu-id="8db1d-170">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-alert-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="8db1d-171">JavaScript</span><span class="sxs-lookup"><span data-stu-id="8db1d-171">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-alert-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="8db1d-172">Цель — C</span><span class="sxs-lookup"><span data-stu-id="8db1d-172">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-alert-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="8db1d-173">Java</span><span class="sxs-lookup"><span data-stu-id="8db1d-173">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-alert-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


<!-- markdownlint-disable MD024 -->

#### <a name="response"></a><span data-ttu-id="8db1d-174">Отклик</span><span class="sxs-lookup"><span data-stu-id="8db1d-174">Response</span></span>

<span data-ttu-id="8db1d-175">Ниже представлен пример успешного отклика.</span><span class="sxs-lookup"><span data-stu-id="8db1d-175">The following is an example of a successful response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 204 No Content
```

### <a name="example-2-request-with-prefer-header"></a><span data-ttu-id="8db1d-176">Пример 2: запрос с заголовком предпочтения</span><span class="sxs-lookup"><span data-stu-id="8db1d-176">Example 2: Request with Prefer header</span></span>

#### <a name="request"></a><span data-ttu-id="8db1d-177">Запрос</span><span class="sxs-lookup"><span data-stu-id="8db1d-177">Request</span></span>

<span data-ttu-id="8db1d-178">В приведенном ниже примере показан запрос, включающий заголовок `Prefer` запроса.</span><span class="sxs-lookup"><span data-stu-id="8db1d-178">The following example shows a request that includes the `Prefer` request header.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/beta/security/alerts/{alert_id}
Content-type: application/json
Prefer: return=representation

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```

#### <a name="response"></a><span data-ttu-id="8db1d-179">Отклик</span><span class="sxs-lookup"><span data-stu-id="8db1d-179">Response</span></span>

<span data-ttu-id="8db1d-180">Ниже приведен пример отклика при использовании заголовка необязательного `Prefer: return=representation` запроса.</span><span class="sxs-lookup"><span data-stu-id="8db1d-180">The following is an example of the response when the optional `Prefer: return=representation` request header is used.</span></span>

><span data-ttu-id="8db1d-p109">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="8db1d-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "activityGroupName": "activityGroupName-value",
  "assignedTo": "assignedTo-value",
  "azureSubscriptionId": "azureSubscriptionId-value",
  "azureTenantId": "azureTenantId-value",
  "category": "category-value",
  "closedDateTime": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Update alert",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
