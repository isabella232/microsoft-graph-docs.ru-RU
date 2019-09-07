---
title: Создание валют
description: Создает объект Currency в Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
localization_priority: Normal
ms.prod: dynamics-365-business-central
doc_type: apiPageType
ms.openlocfilehash: 32e506869991ca7ee19b280caae8bee9d4e5eeef
ms.sourcegitcommit: c68a83d28fa4bfca6e0618467934813a9ae17b12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2019
ms.locfileid: "36792123"
---
# <a name="create-currencies"></a><span data-ttu-id="2db79-103">Создание валют</span><span class="sxs-lookup"><span data-stu-id="2db79-103">Create currencies</span></span>
<span data-ttu-id="2db79-104">Создайте объект Currency в Dynamics 365 Business Central.</span><span class="sxs-lookup"><span data-stu-id="2db79-104">Create a currency object in Dynamics 365 Business Central.</span></span>

## <a name="permissions"></a><span data-ttu-id="2db79-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="2db79-105">Permissions</span></span>
<span data-ttu-id="2db79-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2db79-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2db79-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="2db79-108">Permission type</span></span> |<span data-ttu-id="2db79-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="2db79-109">Permissions (from least to most privileged)</span></span>|
|:---------------|:------------------------------------------|
|<span data-ttu-id="2db79-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2db79-110">Delegated (work or school account)</span></span>|<span data-ttu-id="2db79-111">Financials.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2db79-111">Financials.ReadWrite.All</span></span> |
|<span data-ttu-id="2db79-112">Делегированная учетная запись (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="2db79-112">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="2db79-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2db79-113">Not supported.</span></span>|
|<span data-ttu-id="2db79-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="2db79-114">Application</span></span>|<span data-ttu-id="2db79-115">Financials.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2db79-115">Financials.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="2db79-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="2db79-116">HTTP request</span></span>
```
POST /financials/companies/{id}/currencies
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2db79-117">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="2db79-117">Optional query parameters</span></span>
<span data-ttu-id="2db79-118">Этот метод поддерживает [параметры запросов OData](/graph/query-parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="2db79-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2db79-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="2db79-119">Request headers</span></span>
|<span data-ttu-id="2db79-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2db79-120">Header</span></span>         |<span data-ttu-id="2db79-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2db79-121">Value</span></span>                    |
|---------------|-------------------------|
|<span data-ttu-id="2db79-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="2db79-122">Authorization</span></span>  |<span data-ttu-id="2db79-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2db79-p102">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="2db79-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2db79-125">Content-Type</span></span>   |<span data-ttu-id="2db79-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2db79-126">application/json</span></span>         |

## <a name="request-body"></a><span data-ttu-id="2db79-127">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="2db79-127">Request body</span></span>
<span data-ttu-id="2db79-128">В тексте запроса добавьте представление объекта **денежных единиц** в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2db79-128">In the request body, supply a JSON representation of **currencies** object.</span></span>

## <a name="response"></a><span data-ttu-id="2db79-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="2db79-129">Response</span></span>
<span data-ttu-id="2db79-130">В случае успешного выполнения этот метод ```201 Created``` возвращает код отклика и объект **валюты** в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="2db79-130">If successful, this method returns ```201 Created``` response code and a **currencies** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2db79-131">Пример</span><span class="sxs-lookup"><span data-stu-id="2db79-131">Example</span></span>

<span data-ttu-id="2db79-132">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="2db79-132">**Request**</span></span>

<span data-ttu-id="2db79-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="2db79-133">Here is an example of a request.</span></span>

```json
POST https://graph.microsoft.com/beta/financials/companies/{id}/currencies
Content-type: application/json

{
  "code": "US",
  "displayName": "US Dollar",
  "symbol": "$",
  "amountDecimalPlaces": "2:2",
  "amountRoundingPrecision": 0.01
}
```

<span data-ttu-id="2db79-134">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="2db79-134">**Response**</span></span>

<span data-ttu-id="2db79-135">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="2db79-135">Here is an example of the response.</span></span> 

> <span data-ttu-id="2db79-136">**Note**: объект Response, показанный здесь, может быть укорочен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="2db79-136">**Note**: The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2db79-137">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="2db79-137">All the properties will be returned from an actual call.</span></span>

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "id-value",
  "code": "US",
  "displayName": "US Dollar",
  "symbol": "$",
  "amountDecimalPlaces": "2:2",
  "amountRoundingPrecision": 0.01,
  "lastModifiedDateTime": "2017-03-22T21:05:09.002Z"
}

```
