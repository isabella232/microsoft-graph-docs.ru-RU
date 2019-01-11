---
title: Создание объекта mobileAppCategory
description: Создание объекта mobileAppCategory.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a84d141a15a55d95d5429511a8db208f24ed984c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887285"
---
# <a name="create-mobileappcategory"></a><span data-ttu-id="75813-103">Создание объекта mobileAppCategory</span><span class="sxs-lookup"><span data-stu-id="75813-103">Create mobileAppCategory</span></span>

> <span data-ttu-id="75813-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="75813-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75813-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="75813-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="75813-106">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="75813-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75813-107">Создание объекта [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="75813-107">Create a new [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="75813-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="75813-108">Prerequisites</span></span>
<span data-ttu-id="75813-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75813-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="75813-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="75813-111">Permission type</span></span>|<span data-ttu-id="75813-112">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="75813-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="75813-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="75813-113">Delegated (work or school account)</span></span>|<span data-ttu-id="75813-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="75813-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="75813-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="75813-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="75813-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="75813-116">Not supported.</span></span>|
|<span data-ttu-id="75813-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="75813-117">Application</span></span>|<span data-ttu-id="75813-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="75813-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="75813-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="75813-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppCategories
POST /deviceAppManagement/mobileApps/{mobileAppId}/categories
```

## <a name="request-headers"></a><span data-ttu-id="75813-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="75813-120">Request headers</span></span>
|<span data-ttu-id="75813-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="75813-121">Header</span></span>|<span data-ttu-id="75813-122">Значение</span><span class="sxs-lookup"><span data-stu-id="75813-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="75813-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="75813-123">Authorization</span></span>|<span data-ttu-id="75813-124">Требуется Bearer &lt;маркер&gt;
</span><span class="sxs-lookup"><span data-stu-id="75813-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="75813-125">Accept</span><span class="sxs-lookup"><span data-stu-id="75813-125">Accept</span></span>|<span data-ttu-id="75813-126">application/json</span><span class="sxs-lookup"><span data-stu-id="75813-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="75813-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="75813-127">Request body</span></span>
<span data-ttu-id="75813-128">В тексте запроса добавьте представление объекта mobileAppCategory в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="75813-128">In the request body, supply a JSON representation for the mobileAppCategory object.</span></span>

<span data-ttu-id="75813-129">В таблице ниже приведены свойства, которые необходимо указывать при создании объекта mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="75813-129">The following table shows the properties that are required when you create the mobileAppCategory.</span></span>

|<span data-ttu-id="75813-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="75813-130">Property</span></span>|<span data-ttu-id="75813-131">Тип</span><span class="sxs-lookup"><span data-stu-id="75813-131">Type</span></span>|<span data-ttu-id="75813-132">Описание</span><span class="sxs-lookup"><span data-stu-id="75813-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75813-133">id</span><span class="sxs-lookup"><span data-stu-id="75813-133">id</span></span>|<span data-ttu-id="75813-134">String</span><span class="sxs-lookup"><span data-stu-id="75813-134">String</span></span>|<span data-ttu-id="75813-135">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="75813-135">The key of the entity.</span></span>|
|<span data-ttu-id="75813-136">displayName</span><span class="sxs-lookup"><span data-stu-id="75813-136">displayName</span></span>|<span data-ttu-id="75813-137">String</span><span class="sxs-lookup"><span data-stu-id="75813-137">String</span></span>|<span data-ttu-id="75813-138">Имя категории приложений.</span><span class="sxs-lookup"><span data-stu-id="75813-138">The name of the app category.</span></span>|
|<span data-ttu-id="75813-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="75813-139">lastModifiedDateTime</span></span>|<span data-ttu-id="75813-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="75813-140">DateTimeOffset</span></span>|<span data-ttu-id="75813-141">Дата и время последнего изменения объекта mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="75813-141">The date and time the mobileAppCategory was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="75813-142">Отклик</span><span class="sxs-lookup"><span data-stu-id="75813-142">Response</span></span>
<span data-ttu-id="75813-143">В случае успешного выполнения этот метод возвращает код отклика `201 Created` и объект [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="75813-143">If successful, this method returns a `201 Created` response code and a [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75813-144">Пример</span><span class="sxs-lookup"><span data-stu-id="75813-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="75813-145">Запрос</span><span class="sxs-lookup"><span data-stu-id="75813-145">Request</span></span>
<span data-ttu-id="75813-146">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="75813-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppCategories
Content-type: application/json
Content-length: 163

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="75813-147">Ответ</span><span class="sxs-lookup"><span data-stu-id="75813-147">Response</span></span>
<span data-ttu-id="75813-p103">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="75813-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 212

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "d85d9cee-9cee-d85d-ee9c-5dd8ee9c5dd8",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```





