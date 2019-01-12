---
title: Действие assign
description: Н/Д
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 245530ea687c6a0ead115ff74ec8fea9f90bde90
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964223"
---
# <a name="assign-action"></a><span data-ttu-id="f803e-103">Действие assign</span><span class="sxs-lookup"><span data-stu-id="f803e-103">assign action</span></span>

> <span data-ttu-id="f803e-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f803e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f803e-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f803e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f803e-106">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="f803e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f803e-107">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f803e-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f803e-108">Необходимые разрешения</span><span class="sxs-lookup"><span data-stu-id="f803e-108">Prerequisites</span></span>
<span data-ttu-id="f803e-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f803e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f803e-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="f803e-111">Permission type</span></span>|<span data-ttu-id="f803e-112">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="f803e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f803e-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f803e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f803e-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f803e-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f803e-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="f803e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f803e-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f803e-116">Not supported.</span></span>|
|<span data-ttu-id="f803e-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="f803e-117">Application</span></span>|<span data-ttu-id="f803e-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f803e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f803e-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="f803e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="f803e-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="f803e-120">Request headers</span></span>
|<span data-ttu-id="f803e-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f803e-121">Header</span></span>|<span data-ttu-id="f803e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f803e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f803e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f803e-123">Authorization</span></span>|<span data-ttu-id="f803e-124">Требуется Bearer &lt;маркер&gt;
</span><span class="sxs-lookup"><span data-stu-id="f803e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f803e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f803e-125">Accept</span></span>|<span data-ttu-id="f803e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f803e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f803e-127">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="f803e-127">Request body</span></span>
<span data-ttu-id="f803e-128">В тело запроса добавьте параметры в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="f803e-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="f803e-129">В приведенной ниже таблице указаны параметры, которые можно использовать с этим действием.</span><span class="sxs-lookup"><span data-stu-id="f803e-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="f803e-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="f803e-130">Property</span></span>|<span data-ttu-id="f803e-131">Тип</span><span class="sxs-lookup"><span data-stu-id="f803e-131">Type</span></span>|<span data-ttu-id="f803e-132">Описание</span><span class="sxs-lookup"><span data-stu-id="f803e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f803e-133">appProvisioningConfigurationGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="f803e-133">appProvisioningConfigurationGroupAssignments</span></span>|<span data-ttu-id="f803e-134">[mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) коллекции</span><span class="sxs-lookup"><span data-stu-id="f803e-134">[mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) collection</span></span>|<span data-ttu-id="f803e-135">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f803e-135">Not yet documented</span></span>|
|<span data-ttu-id="f803e-136">iOSLobAppProvisioningConfigAssignments</span><span class="sxs-lookup"><span data-stu-id="f803e-136">iOSLobAppProvisioningConfigAssignments</span></span>|<span data-ttu-id="f803e-137">[iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) коллекции</span><span class="sxs-lookup"><span data-stu-id="f803e-137">[iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) collection</span></span>|<span data-ttu-id="f803e-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f803e-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="f803e-139">Ответ</span><span class="sxs-lookup"><span data-stu-id="f803e-139">Response</span></span>
<span data-ttu-id="f803e-140">В случае успешного выполнения это действие возвращает код отклика `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f803e-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f803e-141">Пример</span><span class="sxs-lookup"><span data-stu-id="f803e-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="f803e-142">Запрос</span><span class="sxs-lookup"><span data-stu-id="f803e-142">Request</span></span>
<span data-ttu-id="f803e-143">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="f803e-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assign

Content-type: application/json
Content-length: 578

{
  "appProvisioningConfigurationGroupAssignments": [
    {
      "@odata.type": "#microsoft.graph.mobileAppProvisioningConfigGroupAssignment",
      "targetGroupId": "Target Group Id value",
      "id": "fad873e3-73e3-fad8-e373-d8fae373d8fa"
    }
  ],
  "iOSLobAppProvisioningConfigAssignments": [
    {
      "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfigurationAssignment",
      "id": "eac7008e-008e-eac7-8e00-c7ea8e00c7ea",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="f803e-144">Ответ</span><span class="sxs-lookup"><span data-stu-id="f803e-144">Response</span></span>
<span data-ttu-id="f803e-p103">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="f803e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





