---
title: Обновление Девицехеалсскриптдевицестате
description: Обновление свойств объекта Девицехеалсскриптдевицестате.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: ec3c9cb2825afb4c94ea0be9ddb947e370b16661
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "37531086"
---
# <a name="update-devicehealthscriptdevicestate"></a>Обновление Девицехеалсскриптдевицестате

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Обновление свойств объекта [девицехеалсскриптдевицестате](../resources/intune-devices-devicehealthscriptdevicestate.md) .

## <a name="prerequisites"></a>Необходимые компоненты
Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

|Тип разрешения|Разрешения (в порядке убывания привилегий)|
|:---|:---|
|Делегированные (рабочая или учебная учетная запись)|DeviceManagementManagedDevices.ReadWrite.All|
|Делегированные (личная учетная запись Майкрософт)|Не поддерживается.|
|Приложение|DeviceManagementManagedDevices.ReadWrite.All|

## <a name="http-request"></a>HTTP-запрос
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceHealthScripts/{deviceHealthScriptId}/deviceRunStates/{deviceHealthScriptDeviceStateId}
```

## <a name="request-headers"></a>Заголовки запросов
|Заголовок|Значение|
|:---|:---|
|Авторизация|Bearer &lt;token&gt;. Обязательный.|
|Accept|application/json|

## <a name="request-body"></a>Текст запроса
В тексте запроса добавьте представление объекта [девицехеалсскриптдевицестате](../resources/intune-devices-devicehealthscriptdevicestate.md) в формате JSON.

В следующей таблице приведены свойства, необходимые при создании [девицехеалсскриптдевицестате](../resources/intune-devices-devicehealthscriptdevicestate.md).

|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ объекта состояния устройства сценария работоспособности. Это свойство доступно только для чтения.|
|детектионстате|[рунстате](../resources/intune-shared-runstate.md)|Состояние обнаружения с последнего выполнения сценария работоспособности устройства. Возможные значения: `unknown`, `success`, `fail`, `scriptError`, `pending`, `notApplicable`.|
|ластстатеупдатедатетиме|DateTimeOffset|Последняя метка времени выполнения сценария работоспособности устройства|
|експектедстатеупдатедатетиме|DateTimeOffset|Следующий штамп времени, когда ожидается выполнение сценария работоспособности устройства.|
|lastSyncDateTime|DateTimeOffset|Время последнего синхронизации расширения управления Intune с Intune|
|преремедиатиондетектионскриптаутпут|String|Выходные данные сценария обнаружения перед исправлением|
|преремедиатиондетектионскриптеррор|String|Ошибка сценария обнаружения перед исправлением|
|ремедиатионскриптеррор|String|Вывод ошибок сценария исправления|
|постремедиатиондетектионскриптаутпут|String|Выходные данные сценария обнаружения после исправления|
|постремедиатиондетектионскриптеррор|String|Ошибка сценария обнаружения после исправления|
|ремедиатионстате|[ремедиатионстате](../resources/intune-devices-remediationstate.md)|Состояние исправления с последнего выполнения скрипта работоспособности устройства. Возможные значения: `unknown`, `skipped`, `success`, `remediationFailed`, `scriptError`.|



## <a name="response"></a>Отклик
В случае успешного выполнения этот метод возвращает `200 OK` код отклика и обновленный объект [девицехеалсскриптдевицестате](../resources/intune-devices-devicehealthscriptdevicestate.md) в тексте отклика.

## <a name="example"></a>Пример

### <a name="request"></a>Запрос
Ниже приведен пример запроса.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceHealthScripts/{deviceHealthScriptId}/deviceRunStates/{deviceHealthScriptDeviceStateId}
Content-type: application/json
Content-length: 762

{
  "@odata.type": "#microsoft.graph.deviceHealthScriptDeviceState",
  "detectionState": "success",
  "lastStateUpdateDateTime": "2017-01-01T00:02:58.4418045-08:00",
  "expectedStateUpdateDateTime": "2016-12-31T23:58:26.9294641-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "preRemediationDetectionScriptOutput": "Pre Remediation Detection Script Output value",
  "preRemediationDetectionScriptError": "Pre Remediation Detection Script Error value",
  "remediationScriptError": "Remediation Script Error value",
  "postRemediationDetectionScriptOutput": "Post Remediation Detection Script Output value",
  "postRemediationDetectionScriptError": "Post Remediation Detection Script Error value",
  "remediationState": "skipped"
}
```

### <a name="response"></a>Отклик
Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 811

{
  "@odata.type": "#microsoft.graph.deviceHealthScriptDeviceState",
  "id": "fd2e4505-4505-fd2e-0545-2efd05452efd",
  "detectionState": "success",
  "lastStateUpdateDateTime": "2017-01-01T00:02:58.4418045-08:00",
  "expectedStateUpdateDateTime": "2016-12-31T23:58:26.9294641-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "preRemediationDetectionScriptOutput": "Pre Remediation Detection Script Output value",
  "preRemediationDetectionScriptError": "Pre Remediation Detection Script Error value",
  "remediationScriptError": "Remediation Script Error value",
  "postRemediationDetectionScriptOutput": "Post Remediation Detection Script Output value",
  "postRemediationDetectionScriptError": "Post Remediation Detection Script Error value",
  "remediationState": "skipped"
}
```





