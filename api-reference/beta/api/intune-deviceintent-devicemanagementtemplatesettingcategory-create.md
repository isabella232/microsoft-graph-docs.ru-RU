---
title: Создание Девицеманажементтемплатесеттингкатегори
description: Создание нового объекта Девицеманажементтемплатесеттингкатегори.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: c5aac70346509c526f365253ff2925bda6c00906
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2019
ms.locfileid: "37188957"
---
# <a name="create-devicemanagementtemplatesettingcategory"></a><span data-ttu-id="6685d-103">Создание Девицеманажементтемплатесеттингкатегори</span><span class="sxs-lookup"><span data-stu-id="6685d-103">Create deviceManagementTemplateSettingCategory</span></span>

> <span data-ttu-id="6685d-104">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6685d-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="6685d-105">**Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="6685d-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="6685d-106">Создание нового объекта [девицеманажементтемплатесеттингкатегори](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md) .</span><span class="sxs-lookup"><span data-stu-id="6685d-106">Create a new [deviceManagementTemplateSettingCategory](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6685d-107">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="6685d-107">Prerequisites</span></span>
<span data-ttu-id="6685d-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6685d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6685d-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6685d-110">Permission type</span></span>|<span data-ttu-id="6685d-111">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="6685d-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6685d-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6685d-112">Delegated (work or school account)</span></span>|<span data-ttu-id="6685d-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6685d-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6685d-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6685d-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6685d-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6685d-115">Not supported.</span></span>|
|<span data-ttu-id="6685d-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="6685d-116">Application</span></span>|<span data-ttu-id="6685d-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6685d-117">DeviceManagementConfiguration.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="6685d-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6685d-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/templates/{deviceManagementTemplateId}/categories
```

## <a name="request-headers"></a><span data-ttu-id="6685d-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6685d-119">Request headers</span></span>
|<span data-ttu-id="6685d-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6685d-120">Header</span></span>|<span data-ttu-id="6685d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6685d-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6685d-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="6685d-122">Authorization</span></span>|<span data-ttu-id="6685d-123">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6685d-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6685d-124">Accept</span><span class="sxs-lookup"><span data-stu-id="6685d-124">Accept</span></span>|<span data-ttu-id="6685d-125">application/json</span><span class="sxs-lookup"><span data-stu-id="6685d-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6685d-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="6685d-126">Request body</span></span>
<span data-ttu-id="6685d-127">В тексте запроса добавьте представление объекта Девицеманажементтемплатесеттингкатегори в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6685d-127">In the request body, supply a JSON representation for the deviceManagementTemplateSettingCategory object.</span></span>

<span data-ttu-id="6685d-128">В следующей таблице приведены свойства, необходимые при создании Девицеманажементтемплатесеттингкатегори.</span><span class="sxs-lookup"><span data-stu-id="6685d-128">The following table shows the properties that are required when you create the deviceManagementTemplateSettingCategory.</span></span>

|<span data-ttu-id="6685d-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="6685d-129">Property</span></span>|<span data-ttu-id="6685d-130">Тип</span><span class="sxs-lookup"><span data-stu-id="6685d-130">Type</span></span>|<span data-ttu-id="6685d-131">Описание</span><span class="sxs-lookup"><span data-stu-id="6685d-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6685d-132">id</span><span class="sxs-lookup"><span data-stu-id="6685d-132">id</span></span>|<span data-ttu-id="6685d-133">String</span><span class="sxs-lookup"><span data-stu-id="6685d-133">String</span></span>|<span data-ttu-id="6685d-134">Идентификатор категории, наследуемый от [девицеманажементсеттингкатегори](../resources/intune-deviceintent-devicemanagementsettingcategory.md)</span><span class="sxs-lookup"><span data-stu-id="6685d-134">The category ID Inherited from [deviceManagementSettingCategory](../resources/intune-deviceintent-devicemanagementsettingcategory.md)</span></span>|
|<span data-ttu-id="6685d-135">displayName</span><span class="sxs-lookup"><span data-stu-id="6685d-135">displayName</span></span>|<span data-ttu-id="6685d-136">Строка</span><span class="sxs-lookup"><span data-stu-id="6685d-136">String</span></span>|<span data-ttu-id="6685d-137">Имя категории, унаследованное от [девицеманажементсеттингкатегори](../resources/intune-deviceintent-devicemanagementsettingcategory.md)</span><span class="sxs-lookup"><span data-stu-id="6685d-137">The category name Inherited from [deviceManagementSettingCategory](../resources/intune-deviceintent-devicemanagementsettingcategory.md)</span></span>|



## <a name="response"></a><span data-ttu-id="6685d-138">Отклик</span><span class="sxs-lookup"><span data-stu-id="6685d-138">Response</span></span>
<span data-ttu-id="6685d-139">В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [девицеманажементтемплатесеттингкатегори](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="6685d-139">If successful, this method returns a `201 Created` response code and a [deviceManagementTemplateSettingCategory](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6685d-140">Пример</span><span class="sxs-lookup"><span data-stu-id="6685d-140">Example</span></span>

### <a name="request"></a><span data-ttu-id="6685d-141">Запрос</span><span class="sxs-lookup"><span data-stu-id="6685d-141">Request</span></span>
<span data-ttu-id="6685d-142">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6685d-142">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/templates/{deviceManagementTemplateId}/categories
Content-type: application/json
Content-length: 121

{
  "@odata.type": "#microsoft.graph.deviceManagementTemplateSettingCategory",
  "displayName": "Display Name value"
}
```

### <a name="response"></a><span data-ttu-id="6685d-143">Отклик</span><span class="sxs-lookup"><span data-stu-id="6685d-143">Response</span></span>
<span data-ttu-id="6685d-p102">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="6685d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 170

{
  "@odata.type": "#microsoft.graph.deviceManagementTemplateSettingCategory",
  "id": "cd213562-3562-cd21-6235-21cd623521cd",
  "displayName": "Display Name value"
}
```




