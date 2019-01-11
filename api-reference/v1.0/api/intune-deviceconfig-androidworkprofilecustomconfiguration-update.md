---
title: Обновление androidWorkProfileCustomConfiguration
description: Обновление свойства объекта androidWorkProfileCustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e57f91398d87b8019dca00016c47ece1370c828f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860517"
---
# <a name="update-androidworkprofilecustomconfiguration"></a><span data-ttu-id="fc687-103">Обновление androidWorkProfileCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc687-103">Update androidWorkProfileCustomConfiguration</span></span>

> <span data-ttu-id="fc687-104">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="fc687-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc687-105">Обновление свойства объекта [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="fc687-105">Update the properties of a [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fc687-106">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="fc687-106">Prerequisites</span></span>
<span data-ttu-id="fc687-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc687-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc687-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="fc687-109">Permission type</span></span>|<span data-ttu-id="fc687-110">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="fc687-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fc687-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="fc687-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fc687-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc687-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="fc687-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="fc687-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fc687-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc687-114">Not supported.</span></span>|
|<span data-ttu-id="fc687-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="fc687-115">Application</span></span>|<span data-ttu-id="fc687-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc687-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fc687-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="fc687-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="fc687-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="fc687-118">Request headers</span></span>
|<span data-ttu-id="fc687-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc687-119">Header</span></span>|<span data-ttu-id="fc687-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fc687-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fc687-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc687-121">Authorization</span></span>|<span data-ttu-id="fc687-122">Требуется Bearer &lt;маркер&gt;
</span><span class="sxs-lookup"><span data-stu-id="fc687-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fc687-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fc687-123">Accept</span></span>|<span data-ttu-id="fc687-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fc687-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fc687-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="fc687-125">Request body</span></span>
<span data-ttu-id="fc687-126">В тексте запроса укажите представление JSON для объекта [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="fc687-126">In the request body, supply a JSON representation for the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>

<span data-ttu-id="fc687-127">В следующей таблице показаны свойства, которые необходимы для создания [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc687-127">The following table shows the properties that are required when you create the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span></span>

|<span data-ttu-id="fc687-128">Свойство</span><span class="sxs-lookup"><span data-stu-id="fc687-128">Property</span></span>|<span data-ttu-id="fc687-129">Тип</span><span class="sxs-lookup"><span data-stu-id="fc687-129">Type</span></span>|<span data-ttu-id="fc687-130">Описание</span><span class="sxs-lookup"><span data-stu-id="fc687-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fc687-131">id</span><span class="sxs-lookup"><span data-stu-id="fc687-131">id</span></span>|<span data-ttu-id="fc687-132">Строка</span><span class="sxs-lookup"><span data-stu-id="fc687-132">String</span></span>|<span data-ttu-id="fc687-133">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="fc687-133">Key of the entity.</span></span> <span data-ttu-id="fc687-134">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc687-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fc687-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="fc687-135">lastModifiedDateTime</span></span>|<span data-ttu-id="fc687-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fc687-136">DateTimeOffset</span></span>|<span data-ttu-id="fc687-137">Дата и время последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="fc687-137">DateTime the object was last modified.</span></span> <span data-ttu-id="fc687-138">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc687-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fc687-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fc687-139">createdDateTime</span></span>|<span data-ttu-id="fc687-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fc687-140">DateTimeOffset</span></span>|<span data-ttu-id="fc687-141">Дата и время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="fc687-141">DateTime the object was created.</span></span> <span data-ttu-id="fc687-142">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc687-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fc687-143">описание</span><span class="sxs-lookup"><span data-stu-id="fc687-143">description</span></span>|<span data-ttu-id="fc687-144">Строка</span><span class="sxs-lookup"><span data-stu-id="fc687-144">String</span></span>|<span data-ttu-id="fc687-145">Указанное администратором описание конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="fc687-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="fc687-146">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc687-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fc687-147">displayName</span><span class="sxs-lookup"><span data-stu-id="fc687-147">displayName</span></span>|<span data-ttu-id="fc687-148">Строка</span><span class="sxs-lookup"><span data-stu-id="fc687-148">String</span></span>|<span data-ttu-id="fc687-149">Указанное администратором имя конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="fc687-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="fc687-150">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc687-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fc687-151">version</span><span class="sxs-lookup"><span data-stu-id="fc687-151">version</span></span>|<span data-ttu-id="fc687-152">Int32</span><span class="sxs-lookup"><span data-stu-id="fc687-152">Int32</span></span>|<span data-ttu-id="fc687-153">Версия конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="fc687-153">Version of the device configuration.</span></span> <span data-ttu-id="fc687-154">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc687-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fc687-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="fc687-155">omaSettings</span></span>|<span data-ttu-id="fc687-156">Коллекция [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fc687-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="fc687-157">Параметры OMA.</span><span class="sxs-lookup"><span data-stu-id="fc687-157">OMA settings.</span></span> <span data-ttu-id="fc687-158">Эта коллекция может содержать не более 500 элементов.</span><span class="sxs-lookup"><span data-stu-id="fc687-158">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="fc687-159">Ответ</span><span class="sxs-lookup"><span data-stu-id="fc687-159">Response</span></span>
<span data-ttu-id="fc687-160">Успешно завершена, этот метод возвращает `200 OK` код ответа и обновленные [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) объекта в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="fc687-160">If successful, this method returns a `200 OK` response code and an updated [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc687-161">Пример</span><span class="sxs-lookup"><span data-stu-id="fc687-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="fc687-162">Запрос</span><span class="sxs-lookup"><span data-stu-id="fc687-162">Request</span></span>
<span data-ttu-id="fc687-163">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="fc687-163">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 413

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="fc687-164">Ответ</span><span class="sxs-lookup"><span data-stu-id="fc687-164">Response</span></span>
<span data-ttu-id="fc687-p109">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="fc687-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 585

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "id": "76c5d59b-d59b-76c5-9bd5-c5769bd5c576",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```



