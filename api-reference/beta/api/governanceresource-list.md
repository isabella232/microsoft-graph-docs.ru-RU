---
title: Список governanceResources
description: Получите коллекцию governanceResource с доступом к инициатора запроса.
localization_priority: Normal
ms.openlocfilehash: 4527c7a5f59832fe69181a815af40a0e0e073c90
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838299"
---
# <a name="list-governanceresources"></a><span data-ttu-id="f9c1d-103">Список governanceResources</span><span class="sxs-lookup"><span data-stu-id="f9c1d-103">List governanceResources</span></span>

> <span data-ttu-id="f9c1d-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9c1d-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f9c1d-106">Получите коллекцию [governanceResource](../resources/governanceresource.md) с доступом к инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-106">Retrieve a collection of [governanceResource](../resources/governanceresource.md) that the requestor has access to.</span></span>

## <a name="permissions"></a><span data-ttu-id="f9c1d-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="f9c1d-107">Permissions</span></span>
<span data-ttu-id="f9c1d-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9c1d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9c1d-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="f9c1d-110">Permission type</span></span>      | <span data-ttu-id="f9c1d-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="f9c1d-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f9c1d-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f9c1d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f9c1d-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="f9c1d-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="f9c1d-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="f9c1d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9c1d-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-115">Not supported.</span></span>    |
|<span data-ttu-id="f9c1d-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="f9c1d-116">Application</span></span> | <span data-ttu-id="f9c1d-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="f9c1d-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="f9c1d-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="f9c1d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/resources
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f9c1d-119">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="f9c1d-119">Optional query parameters</span></span>
<span data-ttu-id="f9c1d-120">Этот метод поддерживает [Параметры запроса OData](/graph/query-parameters) , которые помогут при настройке клиентов ответа.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-120">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f9c1d-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="f9c1d-121">Request headers</span></span>
| <span data-ttu-id="f9c1d-122">Имя</span><span class="sxs-lookup"><span data-stu-id="f9c1d-122">Name</span></span>      |<span data-ttu-id="f9c1d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="f9c1d-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f9c1d-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9c1d-124">Authorization</span></span>  | <span data-ttu-id="f9c1d-125">Bearer {code}</span><span class="sxs-lookup"><span data-stu-id="f9c1d-125">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9c1d-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="f9c1d-126">Request body</span></span>
<span data-ttu-id="f9c1d-127">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-127">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="f9c1d-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="f9c1d-128">Response</span></span>
<span data-ttu-id="f9c1d-129">Успешно завершена, этот метод возвращает `200 OK` код ответа и коллекцию объектов [governanceResource](../resources/governanceresource.md) в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-129">If successful, this method returns a `200 OK` response code and collection of [governanceResource](../resources/governanceresource.md) objects in the response body.</span></span>
## <a name="examples"></a><span data-ttu-id="f9c1d-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="f9c1d-130">Examples</span></span>

<span data-ttu-id="f9c1d-131">В этом примере выводятся все ресурсы, которые в настоящее время доступна.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-131">This example lists all resources I can currently access.</span></span>
##### <a name="request"></a><span data-ttu-id="f9c1d-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="f9c1d-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceresources"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources
```
##### <a name="response"></a><span data-ttu-id="f9c1d-133">Ответ</span><span class="sxs-lookup"><span data-stu-id="f9c1d-133">Response</span></span>
<span data-ttu-id="f9c1d-134">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-134">Here is an example of the response.</span></span> 

><span data-ttu-id="f9c1d-p103">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="f9c1d-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.governanceResource",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1289

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceResources",
    "value":[
        {
            "id": "fb016e3a-c3ed-4d9d-96b6-a54cd4f0b735",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/resourceGroups/AnujRG/providers/Microsoft.Storage/storageAccounts/anujstoragefimdev",
            "type": "Microsoft.Storage/storageAccounts",
            "displayName": "anujstoragefimdev",
            "status": "Active",
            "registeredDateTime": "2018-04-05T22:30:37.13Z",
            "registeredRoot": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d",  
        },
        {
            "id": "0e0e4461-0c46-4d13-bf69-7cacbec75471",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/resourceGroups/ARPJ-TESTRG-01/providers/Microsoft.Compute/virtualMachines/APRJ-VM-01-T",
            "type": "Microsoft.Compute/virtualMachines",
            "displayName": "APRJ-VM-01-T",
            "status": "Active",
            "registeredDateTime": "2018-04-05T22:30:37.13Z",
            "registeredRoot": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d",  
        },
        {
            "id": "c072eb85-e47b-4627-81cb-5af82a8fc9fb",
            "externalId": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/resourceGroups/ARPJ-TESTRG-01/providers/Microsoft.Compute/virtualMachines/APRJ-VM-01-T/extensions/IaaSAntimalware",
            "type": "Microsoft.Compute/virtualMachines/extensions",
            "displayName": "APRJ-VM-01-T/IaaSAntimalware",
            "status": "Active",
            "registeredDateTime": "2018-04-05T22:30:37.13Z",
            "registeredRoot": "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d",  
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List governanceResources",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
