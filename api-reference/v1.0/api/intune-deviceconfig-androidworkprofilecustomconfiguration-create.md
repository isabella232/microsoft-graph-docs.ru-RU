---
title: Создание androidWorkProfileCustomConfiguration
description: Создание нового объекта androidWorkProfileCustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0d05aee835dfe98d78b3afc31e0ec2af0e7775be
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850815"
---
# <a name="create-androidworkprofilecustomconfiguration"></a><span data-ttu-id="140cc-103">Создание androidWorkProfileCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="140cc-103">Create androidWorkProfileCustomConfiguration</span></span>

> <span data-ttu-id="140cc-104">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="140cc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="140cc-105">Создание нового объекта [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="140cc-105">Create a new [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="140cc-106">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="140cc-106">Prerequisites</span></span>
<span data-ttu-id="140cc-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="140cc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="140cc-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="140cc-109">Permission type</span></span>|<span data-ttu-id="140cc-110">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="140cc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="140cc-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="140cc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="140cc-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="140cc-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="140cc-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="140cc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="140cc-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="140cc-114">Not supported.</span></span>|
|<span data-ttu-id="140cc-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="140cc-115">Application</span></span>|<span data-ttu-id="140cc-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="140cc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="140cc-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="140cc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="140cc-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="140cc-118">Request headers</span></span>
|<span data-ttu-id="140cc-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="140cc-119">Header</span></span>|<span data-ttu-id="140cc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="140cc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="140cc-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="140cc-121">Authorization</span></span>|<span data-ttu-id="140cc-122">Требуется Bearer &lt;маркер&gt;
</span><span class="sxs-lookup"><span data-stu-id="140cc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="140cc-123">Accept</span><span class="sxs-lookup"><span data-stu-id="140cc-123">Accept</span></span>|<span data-ttu-id="140cc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="140cc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="140cc-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="140cc-125">Request body</span></span>
<span data-ttu-id="140cc-126">В тексте запроса укажите представление JSON для объекта androidWorkProfileCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="140cc-126">In the request body, supply a JSON representation for the androidWorkProfileCustomConfiguration object.</span></span>

<span data-ttu-id="140cc-127">В следующей таблице показаны свойства, которые необходимы для создания androidWorkProfileCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="140cc-127">The following table shows the properties that are required when you create the androidWorkProfileCustomConfiguration.</span></span>

|<span data-ttu-id="140cc-128">Свойство</span><span class="sxs-lookup"><span data-stu-id="140cc-128">Property</span></span>|<span data-ttu-id="140cc-129">Тип</span><span class="sxs-lookup"><span data-stu-id="140cc-129">Type</span></span>|<span data-ttu-id="140cc-130">Описание</span><span class="sxs-lookup"><span data-stu-id="140cc-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="140cc-131">id</span><span class="sxs-lookup"><span data-stu-id="140cc-131">id</span></span>|<span data-ttu-id="140cc-132">Строка</span><span class="sxs-lookup"><span data-stu-id="140cc-132">String</span></span>|<span data-ttu-id="140cc-133">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="140cc-133">Key of the entity.</span></span> <span data-ttu-id="140cc-134">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="140cc-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="140cc-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="140cc-135">lastModifiedDateTime</span></span>|<span data-ttu-id="140cc-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="140cc-136">DateTimeOffset</span></span>|<span data-ttu-id="140cc-137">Дата и время последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="140cc-137">DateTime the object was last modified.</span></span> <span data-ttu-id="140cc-138">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="140cc-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="140cc-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="140cc-139">createdDateTime</span></span>|<span data-ttu-id="140cc-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="140cc-140">DateTimeOffset</span></span>|<span data-ttu-id="140cc-141">Дата и время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="140cc-141">DateTime the object was created.</span></span> <span data-ttu-id="140cc-142">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="140cc-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="140cc-143">описание</span><span class="sxs-lookup"><span data-stu-id="140cc-143">description</span></span>|<span data-ttu-id="140cc-144">Строка</span><span class="sxs-lookup"><span data-stu-id="140cc-144">String</span></span>|<span data-ttu-id="140cc-145">Указанное администратором описание конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="140cc-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="140cc-146">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="140cc-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="140cc-147">displayName</span><span class="sxs-lookup"><span data-stu-id="140cc-147">displayName</span></span>|<span data-ttu-id="140cc-148">Строка</span><span class="sxs-lookup"><span data-stu-id="140cc-148">String</span></span>|<span data-ttu-id="140cc-149">Указанное администратором имя конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="140cc-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="140cc-150">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="140cc-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="140cc-151">version</span><span class="sxs-lookup"><span data-stu-id="140cc-151">version</span></span>|<span data-ttu-id="140cc-152">Int32</span><span class="sxs-lookup"><span data-stu-id="140cc-152">Int32</span></span>|<span data-ttu-id="140cc-153">Версия конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="140cc-153">Version of the device configuration.</span></span> <span data-ttu-id="140cc-154">Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="140cc-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="140cc-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="140cc-155">omaSettings</span></span>|<span data-ttu-id="140cc-156">Коллекция [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="140cc-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="140cc-157">Параметры OMA.</span><span class="sxs-lookup"><span data-stu-id="140cc-157">OMA settings.</span></span> <span data-ttu-id="140cc-158">Эта коллекция может содержать не более 500 элементов.</span><span class="sxs-lookup"><span data-stu-id="140cc-158">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="140cc-159">Ответ</span><span class="sxs-lookup"><span data-stu-id="140cc-159">Response</span></span>
<span data-ttu-id="140cc-160">Успешно завершена, этот метод возвращает `201 Created` код ответа и объект [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="140cc-160">If successful, this method returns a `201 Created` response code and a [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="140cc-161">Пример</span><span class="sxs-lookup"><span data-stu-id="140cc-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="140cc-162">Запрос</span><span class="sxs-lookup"><span data-stu-id="140cc-162">Request</span></span>
<span data-ttu-id="140cc-163">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="140cc-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="140cc-164">Ответ</span><span class="sxs-lookup"><span data-stu-id="140cc-164">Response</span></span>
<span data-ttu-id="140cc-p109">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="140cc-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



